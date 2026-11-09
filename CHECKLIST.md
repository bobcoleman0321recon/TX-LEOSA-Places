# Texas — Build Checklist

Copied from LEOSA-Places/templates/STATE_CHECKLIST.md. Follow LEOSA-Places/STATE_WORKFLOW.md. Tick each item when it is done and its sources are in docs/sources.md.

Started: Nov 7, 2026 · Last updated: Nov 8, 2026 (Layers 4, 6 and 7 drafted; map data, rules and all four guide tabs built into the app on branch add-texas)

## Research (STATE_WORKFLOW.md layers)

- [x] 01-federal — reference Layer 1 of STATE_WORKFLOW.md (no state copy)
- [ ] 02-definitions — started Nov 7: docs/tx-definitions.md (§ 46.15(a)(5), § 1701.357, § 411.199 read). Gov't Code ch. 614 subch. H read (retired ID cards). Still to do: CCP art. 2A.001, decision tree
- [ ] 03-implementation — started Nov 7: certificate and retiree license in docs/tx-definitions.md. DPS retiree-license page and TCOLE certificate form (IUF 03.002) logged; TCOLE issues only to Texas residents. 37 TAC § 218.9 read (LII copy); preemption read. Still to do: 37 TAC ch. 6
- [ ] 04-profiles — answers for profiles A–E (state retiree, out-of-state retiree, federal retiree, visitor, military police/DoD) — draft Nov 8: docs/tx-profiles.md. Residence decides the certificate (A, B, C, likely E yes; D no). New Nov 8: S.B. 706 (2025) recognizes every state's license (§ 411.173(b)); § 411.205 duty to show a license at a stop. Open: questions 9–11 in tx-profiles.md
- [ ] 05-places — draft Nov 7: docs/tx-leosa-sensitive-places-crosswalk.md (§§ 46.03, 30.05, 30.06, 30.07 read in full; Class C correction under § 30.05(d-3)); state parks (31 TAC § 59.134(d)) and local preemption (LG §§ 229.001, 236.002) read Nov 7. Corps land (36 C.F.R. § 327.13: Restricted), Capitol (no written ban found) and tribal land (note only) done Nov 7. Corps litigation checked Nov 8 (no Fifth Circuit, Texas or post-Bruen ruling; rule stands). Post offices changed to C for every state on Nov 8 (Bob's decision: open to the public, law-abiding, LEOSA fits; OLC opinion Aug. 12, 2026). Still to do: tribal codes
- [ ] 06-hardware — ammunition, magazines, firearm type, vehicles and transport, possession licensing — draft Nov 8: docs/tx-hardware.md (Penal Code ch. 46 through § 46.14, §§ 42.01, 42.12, Labor Code §§ 52.061–.062, S.B. 1596 read Nov 8). No magazine limit, hollow-point ban, registration or roster; armor-piercing ammunition is a felony with no retiree exemption; short-barrel firearms left § 46.05 on Sept. 1, 2025. Still to do: search the other codes (Education § 37.125, Gov't § 411.2032, Parks and Wildlife) for ammunition, magazine and stun-gun rules
- [ ] 07-guidance — draft Nov 8: docs/tx-guidance-cases.md. Procedure read (CCP arts. 14.01, 14.03, 14.06, 15.17, 17.03, 17.15, 38.22; Tex. Const. art. I, §§ 10, 11). No Texas DA, DPS or TCOLE LEOSA guidance and no Texas appellate LEOSA opinion found. Cases read: Cuevas (2026), Gamino, Braughton, Guyger; two grand-jury reports (news). Still to do: pattern jury charge (paid), § 1.07, Fifth Circuit on LEOSA § 1983
- [x] 07f-force — docs/tx-force-first-hour.md; procedure, who investigates, training and cases filled Nov 8 from docs/tx-guidance-cases.md. Pattern jury charge not read (State Bar sells it)
- [ ] 08-maps — started Nov 7: docs/tx-map-layers.md; state and federal layers pulled by the app's tools/tx_fetch_data.py (branch add-texas): TEA 8,932, TABC 51% 7,057 (6,122 geocoded), racetracks 4, TPWD parks 116, PAD-US Corps 103 and federal 194. OSM extract read (58,745 places). Built Nov 8 by `tools/tx_build_data.py`: about 23,700 places in 23 categories; added Census county and city outlines and the six VA national cemeteries (VA list read Nov 8). Corps review done Nov 8 (35 Fort Worth records are city parks, left out). Still to do: place the 931 unmatched TABC addresses, civil commitment facility. Layer inventory (source URL, format, license, update cycle, pulled date) + data pulled
- [ ] 09-scenarios — scenario records in the NJ format, three statuses only
- [ ] 10-sources — docs/sources.md started Nov 7 (ongoing)

## Build (in the one LEOSA Places app)

- [x] Legal text added to the app's rules file (`src/rules_tx.js`), with LAW_AS_OF and LAW_STATUS for this state (Nov 8)
- [ ] Guide tabs filled: VIEW, NOW, DRILLS (10+), CASES (5+) and CASES_NOTE; every tab checked on a device — all four built Nov 8 (12 drills, 7 cases) and checked in the browser at phone width; device check pending
- [x] Entry in `src/states.js` with `region: "South Central"` (STATE_WORKFLOW.md "Regions") and `neighbors`; app code still state-neutral (no state names or cite lists in app.js or index.html)
- [x] Map layers added to the fetch and build tools; manifest records source and date (Nov 8)
- [x] Tests pass: no place marked clear; government property and federal courts stay Restricted for retirees (Nov 8: 616 rules checks, 108 real-place checks)
- [x] App says which states it covers, and this state's as-of date shows on every status (picker by Region; checked in the browser at phone width Nov 8)

## Review before submission

- [ ] 11-review — every statute and cite checked against the primary source — done Nov 8 (every rules_tx.js authority traced to sources.md or Layer 1; § 46.03 re-read; TABC sign statutes, 49 C.F.R. § 1540.111 and the Corps rule verified). Left: 31 TAC § 59.134(d) at the Secretary of State portal and 37 TAC ch. 6, by hand
- [x] Refresh dates set for litigation-driven items — recheck at each release: post office OLC opinion and FPC v. Bondi, Corps § 327.13 cases, Cuevas line of cases, Texas LEOSA opinions (none yet)
- [x] Notices from STATE_WORKFLOW.md in place, naming this state's sources (not legal advice, how updates work, your responsibility, not reviewed by an attorney) — app gate and Sources tab; Texas AUTH shows on Sources
- [x] Legal review packet written (docs/tx-leosa-legal-review-packet.md) — Nov 8, 26 questions plus P1 (post offices, all states)

## Release (STATE_WORKFLOW.md, "Releasing a state in the one app")

- [ ] 12-release — version and build bumped; tests pass; run on a physical iPhone and iPad
- [x] Listing updated: state-neutral subtitle, states named in description and What's New, state name in keywords, this state's screenshots — drafted Nov 8 in NJ-LEOSA-Places/docs/app-store/listing.md ("Version 1.3 listing"); paste into App Store Connect after 1.2 is released
- [x] Store assets: three captioned screenshots per device; optional app preview; header and search images updated if they name the states — Nov 8: region picker, Texas map (UT Austin) and TX's view for iPhone and iPad; creative/1.3 header and search images; no Texas app preview yet
- [ ] Archived on the Mac and uploaded (Xcode Cloud is off), version added in App Store Connect, submitted
- [ ] 13-announce — training post drafted; every cite Verified in docs/sources.md; as-of date and not-legal-advice line included

## Open questions

- Nov 7, 2026 (**decided for the app Nov 7: private-place bans C, government property and federal rules R; still a counsel question**): For a LEOSA retiree without the Texas § 1701.357 certificate, which § 46.03 places does § 926C override? Government property and parks stay under (b)(2); the private-place bans (bars, racetracks, amusement parks, private hospitals) are state bans, not owner rules.
- Nov 7, 2026: Is a 30.06 or 30.07 sign "notice that entry with a handgun was forbidden" under § 30.05 for a carrier who holds no Texas license? (Penalty is Class C either way under § 30.05(d-3) unless told in person and the carrier stays.)
- Nov 7, 2026: Layer 7F counsel questions 1–4 in docs/tx-force-first-hour.md (retiree arrest authority; whether carrying in a § 46.03 place is "criminal activity" defeating no-retreat; CPRC § 83.001 and bystanders; § 9.31(b)(5)).
- Nov 7, 2026: A visiting retiree cannot get the TCOLE certificate (Texas residents only), so the `retired` group's open question 1 decides most visitors' answers. Confirm with TCOLE that non-residents are refused. Answered Nov 8 from the statute: (b) and (h) have no residence rule, and UT System Police Policy 410 certifies other agencies' retirees with the chief's approval; retired Texas officers can be certified wherever they live.
- Nov 7, 2026: Can a state agency exclude a LEOSA-only carrier (no license) by § 30.05 notice? § 411.209 protects license holders only (tx-definitions.md question 5).
- Nov 7, 2026: Does § 46.03(a)(14) reach legislative hearings at the Capitol? Does LEOSA displace any tribal firearm law (§ 926C(a) names only state and local law)? (tx-definitions.md questions 6, 7)
- Nov 7, 2026: Does § 46.15(a)(5)'s photo-ID requirement accept an ID from a federal agency that does not say "retired", if it otherwise meets § 926C(d)?
- Nov 8, 2026: Does a retiree without the certificate who carries openly (lawful under § 46.02 for anyone 21+, but not LEOSA carry) lose the LEOSA argument behind the C status at private § 46.03 places? (tx-definitions.md question 8)
- Nov 8, 2026: Is a visitor with a recognized home-state license (§ 411.173(b)) a "license holder" under Texas law? Does TCOLE certify retired military police, and is a service branch a "law enforcement agency" for § 46.15(a)(5)? What does TLETS show? (tx-profiles.md questions 9–11)
- Nov 8, 2026: Does a jury weigh a retiree's training for or against reasonableness (Guyger)? After Cuevas, would a prosecutor call carrying in a § 46.03 place without the certificate "criminal activity"? (tx-guidance-cases.md questions 5–6)
- Nov 8, 2026 (**decided by Bob Nov 8: check your status in every state**): post offices. OLC (Aug 12, 2026) says no federal enforcement against law-abiding self-defense carry in public post offices; FPC v. Bondi (N.D. Tex.) enjoins enforcement for FPC and SAF members. Keep Restricted (current Layer 1 decision) or move every state to check-your-status? (packet P1)
