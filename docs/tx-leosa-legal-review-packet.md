# Legal review packet — Texas

For the reviewing attorney. Prepared Nov 8, 2026. Every Texas status and sentence in the app comes from `../../NJ-LEOSA-Places/src/rules_tx.js`, and the same statuses appear on the app's Places tab. The research behind them is in this folder's `docs/`, with every source in `sources.md`. Nothing here is settled until counsel signs off. The app says on every screen that it has not been reviewed by an attorney.

## How the statuses were set

1. Find the rule that restricts the place: federal first, then Texas (Penal Code § 46.03, owner notice under §§ 30.05–30.07).
2. Ask who the carrier is. The app has three groups:
   - `txcert`: a LEOSA retiree with a current Texas certificate under Occupations Code § 1701.357 and an agency photo ID. § 46.15(a)(5) takes this retiree outside §§ 46.02 and 46.03.
   - `retired`: a LEOSA retiree without the certificate. This includes most visitors, because TCOLE certifies only Texas residents; a Texas agency may certify a retired Texas officer wherever they live, and a state agency may certify others.
   - `txltc`: a carrier relying on a Texas license to carry, not LEOSA.
3. Ask whether LEOSA reaches the rule. § 926C(b) preserves owner bans and state or local bans on government property. Following Bob's decision of Nov 7, 2026, § 46.03 bans on **privately owned** places are "Restricted for most carriers — check your status" for `retired`; government property and federal rules are Restricted.
4. Where the answer depends on the carrier, the owner or an open question, the status is "check your status". Where unsure, the more restrictive status. No place is ever shown as clear.

## Review done Nov 8, 2026

- **Sources:** every authority in `rules_tx.js` was matched to an entry in `sources.md` or STATE_WORKFLOW.md Layer 1.
- **§ 46.03 re-read in full.**
  - The airport checkpoint defense ((e-1)) and the officer's duty to offer it before arresting ((e-2)) are for license holders only. The DFW scenario now says so.
  - § 46.03(a)(7) uses TABC's own 51% determination under Alco. Bev. Code § 104.06 as the test. That determination is what the red sign under Gov't Code § 411.204 marks (both read).
  - Penalty grades ((g)–(g-2)) match the app.
- **Federal rules:**
  - 49 C.F.R. § 1540.111 (airports) is verified on eCFR.
  - 36 C.F.R. § 327.13 (Corps of Engineers) is unchanged since 2000, and no Fifth Circuit, Texas or post-*Bruen* ruling was found. *Morris* (D. Idaho 2014) relieved only its own plaintiffs; *GeorgiaCarry.org* (11th Cir. 2015; N.D. Ga. 2016) upheld the rule.
- **Post offices:** two developments were found and read:
  - **OLC opinion (Aug 12, 2026):** no federal enforcement against law-abiding self-defense carry in public post offices.
  - ***FPC v. Bondi*** (N.D. Tex.): a permanent injunction for members of FPC and SAF; the appeal was dismissed July 23, 2026.

  Post offices stay Restricted under the existing Layer 1 decision, with both developments shown in the reason. See question P1.
- **Corps layer:** PAD-US labels 35 Fort Worth records as Corps land. All 35 are in the City of Fort Worth's 2025 park inventory, so they stay off the Corps layer.
- **Not re-verified, so check by hand:**
  - 31 TAC § 59.134(d), the state park rule: read on LII. The Secretary of State's code viewer has moved to a portal that does not open by link.
  - 37 TAC ch. 6, the DPS licensing rules: not read.

## Questions for counsel

**Q1, Q2 and P1 change the most statuses.**

| # | Question | App's current position |
| --- | --- | --- |
| 1 | For a LEOSA retiree without the Texas certificate, does § 926C override § 46.03 bans on **privately owned** places (51% bars, racetracks, private hospitals, stadiums, amusement parks, private colleges)? § 926C(b) keeps only owner bans and bans on government property | Check-your-status (decision of Nov 7, 2026). Government property Restricted |
| 2 | Does the Texas certificate satisfy § 922(q)(2)(B)(ii) (the school-zone license exception)? Does a LEOSA credential? | Check-your-status in the 1,000-foot zone; on school grounds, check-your-status for certificate holders, Restricted for others |
| 3 | Does a 30.06 or 30.07 sign (addressed to license holders) count as § 30.05 notice for a carrier with no Texas license? | Treated as a "no" (the safer reading); check-your-status |
| 4 | Does a federal ID reading "Separated" (DoD; some DHS components) satisfy § 46.15(a)(5)'s ID "verifying retired status"? § 1701.357(i) uses "honorably retired or separated" for Texas agency IDs | Stated as open on the carry card |
| 5 | Is "honorably retired peace officer" in § 46.15(a)(5) read with § 411.199(c) or § 614.121(2)? Little practical effect, since the clause also covers any § 926C retiree | Not relied on |
| 6 | Can a state agency exclude a LEOSA-only carrier (no license) by § 30.05 notice? § 411.209 protects license holders only | State agency property outside § 46.03 not mapped |
| 7 | Does § 46.03(a)(14) (open meetings with notice) reach legislative hearings at the Capitol? | Capitol not mapped; note that screening decides entry |
| 8 | Does LEOSA displace any tribal firearm law? § 926C(a) names only state and local law | Tribal land not mapped; note only |
| 9 | A retiree may carry holstered openly under Texas law (§ 46.02), but that is not LEOSA carry. Does open carry weaken the LEOSA argument behind the check-your-status answers at private § 46.03 places? | App tells retirees to carry concealed |
| 10 | Is a visitor with a recognized home-state license (§ 411.173(b), S.B. 706) a "license holder" under Subchapter H for the Penal Code (campus carry, 30.06 and 30.07 signs, § 411.205)? | Stated as open |
| 11 | Does TCOLE certify retired military police, and is a service branch a "law enforcement agency" for § 46.15(a)(5)? Is a military retiree a "retired officer of the United States" under § 411.199(g)? | Profile E treated as likely eligible, stated as open |
| 12 | What does a Texas officer see on a TLETS check: an LTC, a recognized license, a TCOLE certificate? | Not stated in the app |
| 13 | Does a LEOSA retiree have any Texas arrest or force authority beyond a private person's? | Read as carry authority only |
| 14 | Is carrying in a § 46.03 place without the certificate "criminal activity" that costs the no-retreat rule and the presumption of reasonableness (§§ 9.31(e), 9.32(b)–(d))? After *Cuevas* (2026), would a prosecutor argue it? | Stated as open in Now what?, Texas's view and Real cases |
| 15 | Does CPRC § 83.001 civil immunity reach a bystander's claim, given § 9.05? | Not stated |
| 16 | Can § 9.31(b)(5) (seeking a discussion while carrying in violation of § 46.02) ever reach a LEOSA carrier? | Not stated |
| 17 | Does a jury weigh a retiree's training for or against reasonableness (*Guyger*)? Penal Code § 1.07 "reasonable belief" not yet read | "This project reads training as cutting both ways" |
| 18 | Amusement parks: do Six Flags Over Texas, Six Flags Fiesta Texas and SeaWorld San Antonio meet § 46.03(c)(1) (75 acres, controlled entries, more than 120 days, guards at all times)? Do any others? | Those three mapped; others not |
| 19 | Is a nonprofit hospital-district hospital "government property" under § 926C(b)(2)? | Hospitals check-your-status for `retired` |

## Federal question (all states)

| # | Question | App's current position |
| --- | --- | --- |
| P1 | Post offices: 39 C.F.R. § 232.1(l) and § 930(a) are unchanged. But the Executive Branch has said it will not enforce them against law-abiding self-defense carry in public post offices (OLC, Aug 12, 2026), and *FPC v. Bondi* enjoins enforcement against FPC and SAF members, surrounding post office property included. Should the status be "check your status" instead of Restricted? Does the OLC reasoning (§ 930(d)(3), "lawful purposes") help a LEOSA carrier at other federal facilities? It says it does not reach them | Restricted, with both developments in the reason (Layer 1 decision). Pending Bob's decision for every state |

## Now what?, Texas's view and Real cases (priority review)

This is the highest-risk text in the app. A Texas criminal defense attorney must approve it before anyone relies on it. The steps and the "what to say" list are common training practice drawn on general knowledge, not law, and no source in this project prescribes them. Questions:

| # | Question | App's current position |
| --- | --- | --- |
| 20 | Is the short statement wise ("I'm the one who called 911... I want a lawyer"), given art. 38.22 § 5 (statements at the scene are admissible)? | Short statement, then ask for a lawyer |
| 21 | Should the 911 call say the caller is armed and describe them? | Yes, without narrative |
| 22 | Who investigates a retiree's shooting in practice (local agency, Texas Rangers on request, county DA, grand jury)? No statute found | Local agency and DA; Rangers only on request |
| 23 | Is the bail statement right (no personal bond for murder or aggravated assault, art. 17.03(b-2))? | Stated |
| 24 | The Texas property rule (§ 9.42): is the app's summary safe, and is the Pasadena grand-jury example fair? | Summary of the conditions; example from a news report |
| 25 | The State Bar's Texas Criminal Pattern Jury Charges (Criminal Defenses; deadly force ch. 32) were not read (sold, not free). Does the force page match them? | Built from ch. 9, § 2.03, *Gamino*, *Braughton*, *Cuevas* |
| 26 | The real cases use news reports for two grand-jury outcomes and do not name the people. Is that presentation fair and accurate? | News subjects described, not named |

## Data limits counsel should know

- **Bars:** 931 of TABC's 7,057 active red-sign licenses could not be placed by the Census geocoder and are not on the map. The app says so.
- **Schools:** TEA lists public and charter schools only. About 3,100 OpenStreetMap schools TEA does not list (mostly private, some closed) are shown as "possible school, not confirmed."
- **Colleges:** split public and private by name. An unrecognized name counts as public, which is Restricted for `retired`.
- **Airports:** the map draws the whole commercial airport, though the ban is the secured area only.
- **Not mapped:** polling places, open meetings, the execution site, the civil commitment facility, tribal land and owner-posted places.
