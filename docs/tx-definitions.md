# TX — Layers 2 and 3: who Texas treats as a qualified retiree

As of Nov 7, 2026. Every line rests on a source in `sources.md`. Draft: not reviewed by an attorney.

## The Texas retiree exemption

Penal Code § 46.15(a)(5) takes a retiree out of Texas's carry law (§ 46.02) and its places law (§ 46.03) when three things are true:

1. The person is an honorably retired peace officer or another qualified retired law enforcement officer as § 926C defines it.
2. The person holds a certificate of proficiency under Occupations Code § 1701.357.
3. The person carries a photo ID from a federal, state or local law enforcement agency that verifies the retired status.

The exemption does not mention §§ 30.05, 30.06 or 30.07 (trespass after notice), so owner bans still reach the retiree. The § 30.05(i) trespass exemption covers peace officers (including commissioned officers of a "recognized state"), not retirees. Federal rules (§§ 922(q), 930, the airport sterile-area rule, postal and VA rules) are untouched.

## Carry without any license (Penal Code § 46.02)

Since 2021, § 46.02 makes handgun carry an offense only for someone under 21, someone with listed recent assault, deadly-conduct, terroristic-threat or disorderly-conduct convictions, or someone barred from possessing a firearm ((a), (a-7)). So a LEOSA retiree who is 21 or older and not barred may carry a handgun in Texas under state law alone, licensed or not. That does not lift § 46.03 places; only § 46.15(a)(5) (the certificate) or LEOSA can do that. The duties that bind every carrier still apply: no display in plain view unless holstered ((a-5)), and no carry while intoxicated off one's own property or vehicle ((a-6)).

## The certificate (Occupations Code § 1701.357)

- **Who can get it:** the statute reaches any qualified retired law enforcement officer entitled to carry under § 926C ((a-1)); it has no residency rule. **TCOLE's application adds one:** the applicant must be "residing in Texas" and send a government ID showing a current Texas address (TCOLE form IUF 03.002, Apr 23, 2026, under its (c-1) power to set procedures). That tracks § 926C(d)(2)(B), which accepts proficiency certified by the state where the retiree resides. Federal and out-of-state retirees who live in Texas qualify (they also send an agency ID stating retired or separated status and a PID form, C-1). **A visiting retiree who lives elsewhere cannot get the certificate, so is in the `retired` group while in Texas.**
- **Course of fire (Commission Rule § 218.9(c)(1), as printed on the form):** B-27 or similar target, combat scoring, at least 50 rounds from point blank to at least 15 yards (20 or more at or beyond 7 yards), at least one timed reload, 70% to pass (175 of 250). A TCOLE firearms instructor or an LTC instructor signs. Fee $35, money order or cashier's check; notarized affidavit. Renew 30 days before expiry.
- **How:** demonstrate weapons proficiency to a qualified handgun instructor certified under Government Code § 411.190 and give TCOLE a sworn affidavit (926C eligibility; license never revoked or suspended; no disqualifying disability) ((b-1), (b-2)). A Texas state or local agency may also certify its own retirees ((b), (c)), and a state agency may certify other retirees ((h)).
- **How long:** one year from issue ((d)). This matches LEOSA's 12-month qualification window.
- **ID:** a certificate holder may ask the former agency for a photo ID showing honorable retirement or separation, and the agency must issue it ((i)). That is a Texas agency duty; it cannot bind a federal or out-of-state agency.
- **Proof of status** may include the Texas retired peace officer ID card (Government Code ch. 614, subch. H) ((c-2)). Under §§ 614.124 and 614.1241, a Texas agency must issue that card on request to a former officer who holds a current § 1701.357 certificate; the agency sets its expiration (§ 614.125). These duties bind Texas agencies only; a federal or out-of-state agency's retired ID comes from that agency's own policy.

## The retiree license (Government Code § 411.199)

- Honorably retired Texas peace officers may apply for a license to carry (LTC) at any time after retirement. The former agency must give a statement and may not refuse.
- Retired U.S. officers who carried on duty may apply too ((g)).
- Fees are waived ((d)). Classroom instruction is waived ((e)); range instruction is waived with a current § 1701.357 certificate ((e-1)).
- **In practice (DPS's special-conditions page, read Nov 7):** a retired Texas officer applies with affidavit LTC-84 or an agency letter; a retired federal officer with a good-standing letter and retirement credentials. Both pay $0, need no training, and are fingerprinted. A retiree of another state's agency (for example a retired NJ or NY officer who moves to Texas) is not covered by § 411.199 and would use the ordinary license process, or carry under § 46.02 and rely on LEOSA and the § 1701.357 certificate.
- Why it matters: a license brings the license-holder defenses and rules: § 30.05(f) (trespass defense), § 30.06 and § 30.07 (sign-based trespass, Class C), and § 411.209 (government may not post signs on its property except where § 46.03 or other law bars license holders).

## Proposed carrier groups for the app

| Group | Who | Carry authority | Texas place law |
| --- | --- | --- | --- |
| `txcert` | LEOSA retiree who lives in Texas, with a current Texas § 1701.357 certificate and qualifying agency photo ID | § 926C and § 46.15(a)(5) | §§ 46.02, 46.03 do not apply. Owner notice (§ 30.05) and federal rules do |
| `retired` | LEOSA retiree relying on another state's or agency's qualification, with no Texas certificate. Includes every visiting retiree (TCOLE issues only to Texas residents) | § 926C only | § 46.03 applies unless LEOSA overrides it. Government property and parks stay under § 926C(b)(2); the private-place bans are the open question |
| `txltc` | Texas license holder (including a § 411.199 retiree license) carrying under the license, not LEOSA | Government Code ch. 411, subch. H | § 46.03 applies in full, with the license-holder exceptions. Signs under §§ 30.06, 30.07 |

A retiree who holds both a certificate and a license can choose. The app should say which authority each answer assumes.

## Open questions (also in CHECKLIST.md)

6. Does § 46.03(a)(14) (open meetings of a governmental body, with notice) reach legislative committee hearings at the Capitol?
7. Does LEOSA displace any tribal firearm law? The text of § 926C(a) names only state and local law; this project reads tribal law as untouched.
8. A retiree 21 or older may carry a holstered handgun openly under Texas law (§ 46.02(a), (a-5)), but that is not LEOSA carry, which is concealed only. Does a retiree without the certificate who carries openly lose the LEOSA argument behind the app's C status at private § 46.03 places? The app tells retirees to carry concealed (`tx-hardware.md`).
5. Can a state agency exclude a LEOSA-only carrier (no Texas license) from its property by § 30.05 notice? § 411.209 protects license holders only, and cities and counties are preempted outright (Local Gov't Code §§ 229.001, 236.002).

1. For the `retired` group, which § 46.03 places does § 926C override? **Decided Nov 7, 2026 for the app:** private-place bans are C (check your status), government-property bans and federal rules are R; see the crosswalk. The legal question stays open for counsel.
2. Does a 30.06 or 30.07 sign count as § 30.05 notice for someone who holds no Texas license? § 30.05(c) gives non-license carriers their own firearms sign, and a general sign "indicating that entry is forbidden" is notice under (b)(2)(C); whether a sign addressed to license holders reaches others is not settled by the text. Either way the penalty is Class C under (d-3) unless the carrier is told in person and stays.
3. Does a federal agency photo ID that does not say "retired" satisfy § 46.15(a)(5)? Concrete example (Nov 8): the DoD retiree card required by DoD Instruction 5525.12 reads "DoD Law Enforcement Officer (Separated)" (see `tx-profiles.md` question 10).
4. Is "honorably retired peace officer" in § 46.15(a)(5) read with the § 411.199(c) or § 614.121(2) definition (Texas service; eligible to retire; not in lieu of discipline)? It matters little in practice: the same clause also covers any "other qualified retired law enforcement officer" under § 926C.
