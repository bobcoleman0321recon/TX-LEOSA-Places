# CLAUDE.md — TX LEOSA & Sensitive Places (research for the LEOSA Places app)

Read `../CLAUDE.md`, `../STATE_WORKFLOW.md`, then this folder's CHECKLIST.md and docs/sources.md.

## Project boundary

This folder lives at `/Users/bobcoleman/LEOSA-Places/TX-LEOSA-Places`. It holds Texas's research. Texas ships as an update inside the one LEOSA Places app (bundle ID `com.bobcoleman.LEOSAPlaces`): users download one App Store listing and pick Texas in the state, territory, possession picker. When Texas is ready, its rules and map data merge into the app codebase. Do not read from or write to Bob's other projects (GS1811-FieldGuide, PensionOps-HonorableService) unless Bob asks.

## Reference build

`../NJ-LEOSA-Places` is the reference. Match its file names, its three statuses, its source discipline (docs/sources.md, verified or unverified, with dates), and its rule that all legal text lives in `src/rules.js`. Federal material lives once, in `../STATE_WORKFLOW.md` Layer 1; reference it, do not copy it here.

## Core design rule: the map never says "clear"

Three statuses only: **Restricted (cited)**, **Restricted for most carriers — check your status (cited)**, **No known restriction mapped — not a clearance**. Every status shows its source and an as-of date. Location stays on the device.

## Texas legal frame (verify each line against docs/sources.md)

1. Texas exempts a qualified retired officer from its carry and place laws (Penal Code §§ 46.02, 46.03) only with a **Texas** certificate of proficiency under Occupations Code § 1701.357 and an agency photo ID (§ 46.15(a)(5)). TCOLE issues the certificate to any § 926C retiree who qualifies with a certified instructor, out-of-state and federal retirees included; it lasts one year.
2. A retiree without that certificate relies on LEOSA alone. Which § 46.03 places LEOSA overrides is the key open question: government property and parks stay under § 926C(b)(2); state bans on private places (bars, private hospitals, racetracks, amusement parks) are not owner rules.
3. Owner bans run through signs. The 30.06 and 30.07 signs bind license holders; a carrier without a Texas license who gets notice that entry with a handgun is forbidden faces general criminal trespass (§ 30.05), which becomes a Class A misdemeanor when the person carries a deadly weapon, and the license-holder defense in § 30.05(f) does not apply.
4. Texas bars state agencies and local governments from posting 30.06 or 30.07 signs on their property unless § 46.03 or other law bars license holders there (Government Code § 411.209), but that protects license holders. Retirees can get a fee-waived license under § 411.199, including retired federal officers under (g).

## Rules for content

- All Texas legal text the app shows lives in the app codebase: `../NJ-LEOSA-Places/src/rules_tx.js` (`TX_RULES`). Run that folder's `tools/test.sh` after changing it. This folder keeps the research behind it.
- Every legal statement needs a source in docs/sources.md, marked verified or unverified.
- Paraphrase statutes; quote only short operative phrases, with pin cites.
- Track litigation as its own field, with whom each injunction binds (STATE_WORKFLOW.md Layer 5).
- The Texas watch list lives in `../STATE_WORKFLOW.md` ("TX — watch list"). Other states' items never go in this folder.
