# TX — Layer 8: map layer inventory

As of Nov 7, 2026. Sources found and probed Nov 7, 2026. Pulled by the app's `tools/tx_fetch_data.py` (branch `add-texas` in `../../NJ-LEOSA-Places`) into `data/tx/raw/`; `manifest.json` there records each source, date and count. The build script (`tools/tx_build_data.py`) comes after the Texas statuses in `tx-leosa-sensitive-places-crosswalk.md` are settled.

Pulled Nov 7, 2026 (`tools/tx_fetch_data.py --no-osm`): TEA campuses 8,932 (Elementary 4,774; High School 1,817; Middle/Jr. High 1,665; K-12 676); TPWD state park boundaries 116; racetracks 4 (three Census-geocoded, Gillespie County Fair by OSM name search); TABC active red-sign licenses 7,057, of which 6,122 Census-geocoded (935 to place in the build; MB 3,992, BG 2,310, other 755); PAD-US Corps records 103 (owner and manager USACE 61, owner unknown and manager USACE 24 recreation areas, Corps-owned and state-managed 12, other 6); PAD-US federal 194. OpenStreetMap extract pulled separately (counts below when read).

Every record will carry the two fields from the regions design note in `../../STATE_WORKFLOW.md`: `enforcingAgency` and `jurisdiction`.

## What the Texas map shows, and what it leaves out

Texas restricts carry mostly by **place type** (Penal Code § 46.03) and by **owner notice** (§§ 30.05–30.07), not by government property in general: cities and counties are preempted (Local Gov't Code §§ 229.001, 236.002), and state parks bar only display or discharge (31 TAC § 59.134(d)). So the Texas map is mostly § 46.03 places plus federal land. State parks are pulled only to find the units on Corps of Engineers land; they are not a restricted category.

## State sources (preferred)

| Layer | Map category (§) | Source | Format | Probed Nov 7 | Notes |
| --- | --- | --- | --- | --- | --- |
| Public and charter school campuses | school_grounds (§ 46.03(a)(1)); school_zone buffer (§ 922(q)) | TEA "districts_schools_2026_1105_C" (campus layer, service dated Nov 5, 2026; layer named districts_schools_2025_1201): `https://services2.arcgis.com/5MVN2jsqIrNZD4tP/ArcGIS/rest/services/districts_schools_2026_1105_C/FeatureServer/0` | ArcGIS REST, points | 8,932 campuses | Fields: id, district_name, campus_type, low_grade, high_grade, name, address, lat/lon. Public and charter only; private schools come from OSM. TEA republishes this service often under new dated names; the fetch script should look up the newest `districts_schools_*_C` |
| 51% alcohol businesses | bar51 (§ 46.03(a)(7)) | TABC "TABC License Information" (data.texas.gov `7hf9-qc9f`), filtered to `gun_sign = 'RED'` and `primary_status = 'Active'`, geocoded by address (U.S. Census batch geocoder) | Socrata, addresses | 7,057 active RED | TABC's sign page: holders of MB, BG, BE or private club permits where 51% or more of income is on-premises alcohol sales must post the Red Handgun Warning Sign (Alco. Bev. Code § 104.06; Gov't Code § 411.204). The `gun_sign` field is TABC's record of which sign applies; the legal test is the income share, so the app labels these "TABC 51% (red sign) license" |
| Racetracks | racetrack (§ 46.03(a)(4)) | Texas Racing Commission "Race Parks & County Fairs" page (txrc.texas.gov/racetracks): Sam Houston Race Park, Lone Star Park, Retama Park, Gillespie County Fair & Festival | Hand list, geocoded | 4 sites | Outlines from OSM where they match |
| State parks (TPWD) | Used only to find parks on Corps land; not a restricted category | TPWD "Texas_State_Parks_Boundaries": `https://services1.arcgis.com/1mtXwieMId59thmg/ArcGIS/rest/services/Texas_State_Parks_Boundaries/FeatureServer/0` | ArcGIS REST, polygons | 116 features | Described as provisional boundaries; fields ParkName, PropType, County1–2 |
| Civil commitment facility | civil_commitment (§ 46.03(a)(10)) | Texas Civil Commitment Office (one center) | Hand entry | — | To confirm the current facility and address from TCCO |
| Execution site | Not mapped | — | — | — | § 46.03(a)(6) applies only within 1,000 feet of the execution site on execution days, with notice. Listed in "Not on this map" |

## Federal and national sources

| Layer | Map category | Source | Probed Nov 7 | Notes |
| --- | --- | --- | --- | --- |
| Corps of Engineers project land and water, including state parks on Corps land | corps_land (36 C.F.R. § 327.13): Restricted for every retiree group | USGS PAD-US Fee Managers (same service NJ and NY use), `State_Nm='TX' AND (Own_Name='USACE' OR Mang_Name='USACE')` | 79 features with Own_Name USACE (Mang_Name: USACE 61, state parks 12, city 2, other 4) plus recreation areas with Mang_Name USACE | **Needs review.** PAD-US records Corps recreation areas with owner "UNK" and manager USACE, and lists some Fort Worth city parks as Corps-owned. Corps-owned state park units found: Cooper Lake (3 units), Eisenhower, Lake Somerville (3 units), Martin Dies Jr., Ray Roberts Lake, plus B.A. Steinhagen and Corps WMAs. Check each against the Corps district or TPWD before release |
| Other federal land | federal_park; federal_other; military | PAD-US, `State_Nm='TX' AND Mang_Type='FED'` | — | Same pipeline as NJ and NY. National parks follow state law (36 C.F.R. § 2.4); see Layer 1 for the license-tied exception |
| VA national cemeteries | va_cemetery | PAD-US or OSM cemetery + VA name match | — | Houston, Dallas–Fort Worth, Fort Sam Houston, Central Texas (Killeen), Coastal Bend, Fort Bliss, San Antonio, and others; confirm the list from the VA |
| Tribal land | Note only | Census TIGER AIANNH, Texas | — | Kickapoo (Eagle Pass), Alabama-Coushatta (Livingston), Ysleta del Sur (El Paso). Shown as a note: tribal law applies; not a mapped status |
| Cities and counties | Browse pickers | Census TIGER places and counties, Texas | — | For the browse list only |

## OpenStreetMap (gap fill and outlines)

Geofabrik extract `https://download.geofabrik.de/north-america/us/texas-latest-free.shp.zip` (redirected Nov 7, 2026 to `texas-261107-free.shp.zip`, 1.39 GB). © OpenStreetMap contributors, ODbL. Same class table as NJ's `FCLASS`, plus colleges and universities.

| OSM class | Map category (§) | Notes |
| --- | --- | --- |
| amenity=school not matched to TEA | school_grounds (private schools) | § 46.03(a)(1) covers any "school or educational institution"; flag as "possible school, not confirmed" like NY |
| amenity=university, college | college (§ 46.03(a)(1); licensed concealed carry allowed except posted areas) | Outlines |
| amenity=courthouse | court (§ 46.03(a)(3)) | Includes municipal and justice courts where tagged |
| amenity=prison | correctional (§ 46.03(a)(9)) | Cross-check with TDCJ unit list (lead) |
| amenity=hospital | hospital (§ 46.03(a)(11)); mental hospital (§ 46.03(a)(12)) | HHSC licensed-hospital list is a lead for a state source |
| leisure=stadium | sporting_event (§ 46.03(a)(8)) | The ban applies during high school, college or professional events; label it that way |
| tourism=theme_park | amusement_park (§ 46.03(a)(13)) | Only parks meeting the statute's narrow definition count; hand-review the list (Six Flags Over Texas, Six Flags Fiesta Texas, SeaWorld San Antonio and similar) |
| aeroway=aerodrome (commercial service) | airport (§ 46.03(a)(5): secured area only) | Map the terminal, label "secured area past screening"; FAA commercial-service list to filter |
| amenity=post_office | post_office (federal) | Same as NJ and NY |
| landuse=military | military | Same as NJ and NY |

## Not mappable (listed in the app's "Not on this map")

Polling places during voting (§ 46.03(a)(2)); open meetings of a governmental body after notice (§ 46.03(a)(14)); the execution site on execution days (§ 46.03(a)(6)); sporting events when no event is on; private property posted under §§ 30.05, 30.06 or 30.07; areas a college excludes by notice; tribal land rules; the Capitol (screening decides entry).

## Open items for the build

1. Review PAD-US Corps records. The 24 owner-unknown, Corps-managed records are the lake recreation areas (Aquilla, Bardwell, Belton, Benbrook, Canyon, Cooper, Georgetown, Granger, Grapevine, Hords Creek, Joe Pool, Lake O' the Pines, Lavon, Lewisville, Navarro Mills, O.C. Fisher, Proctor, Ray Roberts, Sam Rayburn, Somerville, Stillhouse Hollow, Waco, Whitney, Wright Patman). Most of the 61 owner-and-manager USACE records are named Fort Worth parks (Trinity River flood-control land); confirm with the Fort Worth District before mapping them Restricted.
1a. Place the 935 TABC addresses the Census batch did not match (single-line retry, then OSM name search).
2. Settle the statuses in the crosswalk for the `retired` group (open question 1) before the build assigns R or C.
3. Hand-review amusement parks against § 46.03's definition.
4. Confirm the civil commitment facility and the VA cemetery list.
