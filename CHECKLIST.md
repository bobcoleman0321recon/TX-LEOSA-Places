# Texas — Build Checklist

Copied from LEOSA-Places/templates/STATE_CHECKLIST.md. Follow LEOSA-Places/STATE_WORKFLOW.md. Tick each item when it is done and its sources are in docs/sources.md.

Started: Nov 7, 2026 · Last updated: Nov 7, 2026 (Layers 2, 3, 5, 7 and 7F started; ch. 9, §§ 30.05, 30.07, 46.02 read in full)

## Research (STATE_WORKFLOW.md layers)

- [x] 01-federal — reference Layer 1 of STATE_WORKFLOW.md (no state copy)
- [ ] 02-definitions — started Nov 7: docs/tx-definitions.md (§ 46.15(a)(5), § 1701.357, § 411.199 read). Gov't Code ch. 614 subch. H read (retired ID cards). Still to do: CCP art. 2A.001, decision tree
- [ ] 03-implementation — started Nov 7: certificate and retiree license in docs/tx-definitions.md. DPS retiree-license page and TCOLE certificate form (IUF 03.002) logged; TCOLE issues only to Texas residents. 37 TAC § 218.9 read (LII copy); preemption read. Still to do: 37 TAC ch. 6
- [ ] 04-profiles — answers for profiles A–E (state retiree, out-of-state retiree, federal retiree, visitor, military police/DoD)
- [ ] 05-places — draft Nov 7: docs/tx-leosa-sensitive-places-crosswalk.md (§§ 46.03, 30.05, 30.06, 30.07 read in full; Class C correction under § 30.05(d-3)); state parks (31 TAC § 59.134(d)) and local preemption (LG §§ 229.001, 236.002) read Nov 7. Corps land (36 C.F.R. § 327.13: Restricted), Capitol (no written ban found) and tribal land (note only) done Nov 7. Still to do: Corps litigation check, tribal codes, map layers
- [ ] 06-hardware — ammunition, magazines, firearm type, vehicles and transport, possession licensing — draft Nov 8: docs/tx-hardware.md (Penal Code ch. 46 through § 46.14, §§ 42.01, 42.12, Labor Code §§ 52.061–.062, S.B. 1596 read Nov 8). No magazine limit, hollow-point ban, registration or roster; armor-piercing ammunition is a felony with no retiree exemption; short-barrel firearms left § 46.05 on Sept. 1, 2025. Still to do: search the other codes (Education § 37.125, Gov't § 411.2032, Parks and Wildlife) for ammunition, magazine and stun-gun rules
- [ ] 07-guidance — started Nov 7: DPS special-conditions, 89th Legislation and laws pages; AG Ops. GA-0564 and KP-0332 (persuasive) in docs/sources.md. AG directives, state police FAQs, DA policies, case list; each dated and tagged binding / persuasive / informal
- [ ] 07f-force — draft Nov 7: docs/tx-force-first-hour.md (ch. 9, §§ 2.03, 22.01–22.05, CPRC § 83.001 verified; procedure, jury charge, who investigates and cases still open). Justification statute, retreat rule, property and arrest rules, official jury charge, silence and counsel, charging and bail, who investigates, real cases (STATE_WORKFLOW.md Layer 7F)
- [ ] 08-maps — started Nov 7: docs/tx-map-layers.md; state and federal layers pulled by the app's tools/tx_fetch_data.py (branch add-texas): TEA 8,932, TABC 51% 7,057 (6,122 geocoded), racetracks 4, TPWD parks 116, PAD-US Corps 103 and federal 194. OSM extract read (58,745 places). Still to do: Corps review, build script. Layer inventory (source URL, format, license, update cycle, pulled date) + data pulled
- [ ] 09-scenarios — scenario records in the NJ format, three statuses only
- [ ] 10-sources — docs/sources.md started Nov 7 (ongoing)

## Build (in the one LEOSA Places app)

- [ ] Legal text added to the app's rules file (`src/rules_<st>.js`), with LAW_AS_OF and LAW_STATUS for this state
- [ ] Guide tabs filled: VIEW, NOW, DRILLS (10+), CASES (5+) and CASES_NOTE; every tab checked on a device
- [ ] Entry in `src/states.js` with `region: "South Central"` (STATE_WORKFLOW.md "Regions") and `neighbors`; app code still state-neutral (no state names or cite lists in app.js or index.html)
- [ ] Map layers added to the fetch and build tools; manifest records source and date
- [ ] Tests pass: no place marked clear; government property and federal courts stay Restricted for retirees
- [ ] App says which states it covers, and this state's as-of date shows on every status

## Review before submission

- [ ] 11-review — every statute and cite checked against the primary source
- [ ] Refresh dates set for litigation-driven items
- [ ] Notices from STATE_WORKFLOW.md in place, naming this state's sources (not legal advice, how updates work, your responsibility, not reviewed by an attorney)
- [ ] Legal review packet written (docs/tx-leosa-legal-review-packet.md)

## Release (STATE_WORKFLOW.md, "Releasing a state in the one app")

- [ ] 12-release — version and build bumped; tests pass; run on a physical iPhone and iPad
- [ ] Listing updated: state-neutral subtitle, states named in description and What's New, state name in keywords, this state's screenshots
- [ ] Store assets: three captioned screenshots per device; optional app preview; header and search images updated if they name the states
- [ ] Archived on the Mac and uploaded (Xcode Cloud is off), version added in App Store Connect, submitted
- [ ] 13-announce — training post drafted; every cite Verified in docs/sources.md; as-of date and not-legal-advice line included

## Open questions

- Nov 7, 2026 (**decided for the app Nov 7: private-place bans C, government property and federal rules R; still a counsel question**): For a LEOSA retiree without the Texas § 1701.357 certificate, which § 46.03 places does § 926C override? Government property and parks stay under (b)(2); the private-place bans (bars, racetracks, amusement parks, private hospitals) are state bans, not owner rules.
- Nov 7, 2026: Is a 30.06 or 30.07 sign "notice that entry with a handgun was forbidden" under § 30.05 for a carrier who holds no Texas license? (Penalty is Class C either way under § 30.05(d-3) unless told in person and the carrier stays.)
- Nov 7, 2026: Layer 7F counsel questions 1–4 in docs/tx-force-first-hour.md (retiree arrest authority; whether carrying in a § 46.03 place is "criminal activity" defeating no-retreat; CPRC § 83.001 and bystanders; § 9.31(b)(5)).
- Nov 7, 2026: A visiting retiree cannot get the TCOLE certificate (Texas residents only), so the `retired` group's open question 1 decides most visitors' answers. Confirm with TCOLE that non-residents are refused, and whether a Texas agency under § 1701.357(b) or (h) may certify a non-resident.
- Nov 7, 2026: Can a state agency exclude a LEOSA-only carrier (no license) by § 30.05 notice? § 411.209 protects license holders only (tx-definitions.md question 5).
- Nov 7, 2026: Does § 46.03(a)(14) reach legislative hearings at the Capitol? Does LEOSA displace any tribal firearm law (§ 926C(a) names only state and local law)? (tx-definitions.md questions 6, 7)
- Nov 7, 2026: Does § 46.15(a)(5)'s photo-ID requirement accept an ID from a federal agency that does not say "retired", if it otherwise meets § 926C(d)?
- Nov 8, 2026: Does a retiree without the certificate who carries openly (lawful under § 46.02 for anyone 21+, but not LEOSA carry) lose the LEOSA argument behind the C status at private § 46.03 places? (tx-definitions.md question 8)
