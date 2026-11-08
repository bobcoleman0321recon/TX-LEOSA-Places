# Texas — Build Checklist

Copied from LEOSA-Places/templates/STATE_CHECKLIST.md. Follow LEOSA-Places/STATE_WORKFLOW.md. Tick each item when it is done and its sources are in docs/sources.md.

Started: Nov 7, 2026 · Last updated: Nov 7, 2026 (Layers 2, 3, 5, 7 and 7F started; ch. 9, §§ 30.05, 30.07, 46.02 read in full)

## Research (STATE_WORKFLOW.md layers)

- [x] 01-federal — reference Layer 1 of STATE_WORKFLOW.md (no state copy)
- [ ] 02-definitions — started Nov 7: docs/tx-definitions.md (§ 46.15(a)(5), § 1701.357, § 411.199 read). Gov't Code ch. 614 subch. H read (retired ID cards). Still to do: CCP art. 2A.001, decision tree
- [ ] 03-implementation — started Nov 7: certificate and retiree license in docs/tx-definitions.md. DPS retiree-license page and TCOLE certificate form (IUF 03.002) logged; TCOLE issues only to Texas residents. Still to do: 37 TAC § 218.9 and ch. 6, preemption check
- [ ] 04-profiles — answers for profiles A–E (state retiree, out-of-state retiree, federal retiree, visitor, military police/DoD)
- [ ] 05-places — draft Nov 7: docs/tx-leosa-sensitive-places-crosswalk.md (§§ 46.03, 30.05, 30.06, 30.07 read in full; Class C correction under § 30.05(d-3)). Still to do: state parks, local preemption, tribal gaming, map layers
- [ ] 06-hardware — ammunition, magazines, firearm type, vehicles and transport, possession licensing
- [ ] 07-guidance — started Nov 7: DPS special-conditions page in docs/sources.md. AG directives, state police FAQs, DA policies, case list; each dated and tagged binding / persuasive / informal
- [ ] 07f-force — draft Nov 7: docs/tx-force-first-hour.md (ch. 9, §§ 2.03, 22.01–22.05, CPRC § 83.001 verified; procedure, jury charge, who investigates and cases still open). Justification statute, retreat rule, property and arrest rules, official jury charge, silence and counsel, charging and bail, who investigates, real cases (STATE_WORKFLOW.md Layer 7F)
- [ ] 08-maps — layer inventory (source URL, format, license, update cycle, pulled date) + data pulled
- [ ] 09-scenarios — scenario records in the NJ format, three statuses only
- [ ] 10-sources — docs/sources.md started Nov 7 (ongoing)

## Build (in the one LEOSA Places app)

- [ ] Legal text added to the app's rules file (`src/rules_<st>.js`), with LAW_AS_OF and LAW_STATUS for this state
- [ ] Guide tabs filled: VIEW, NOW, DRILLS (10+), CASES (5+) and CASES_NOTE; every tab checked on a device
- [ ] Picker entry in `src/states.js`; app code still state-neutral (no state names or cite lists in app.js or index.html)
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

- Nov 7, 2026: For a LEOSA retiree without the Texas § 1701.357 certificate, which § 46.03 places does § 926C override? Government property and parks stay under (b)(2); the private-place bans (bars, racetracks, amusement parks, private hospitals) are state bans, not owner rules.
- Nov 7, 2026: Is a 30.06 or 30.07 sign "notice that entry with a handgun was forbidden" under § 30.05 for a carrier who holds no Texas license? (Penalty is Class C either way under § 30.05(d-3) unless told in person and the carrier stays.)
- Nov 7, 2026: Layer 7F counsel questions 1–4 in docs/tx-force-first-hour.md (retiree arrest authority; whether carrying in a § 46.03 place is "criminal activity" defeating no-retreat; CPRC § 83.001 and bystanders; § 9.31(b)(5)).
- Nov 7, 2026: A visiting retiree cannot get the TCOLE certificate (Texas residents only), so the `retired` group's open question 1 decides most visitors' answers. Confirm with TCOLE that non-residents are refused, and whether a Texas agency under § 1701.357(b) or (h) may certify a non-resident.
- Nov 7, 2026: Does § 46.15(a)(5)'s photo-ID requirement accept an ID from a federal agency that does not say "retired", if it otherwise meets § 926C(d)?
