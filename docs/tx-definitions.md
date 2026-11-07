# TX — Layers 2 and 3: who Texas treats as a qualified retiree

As of Nov 7, 2026. Every line rests on a source in `sources.md`. Draft: not reviewed by an attorney.

## The Texas retiree exemption

Penal Code § 46.15(a)(5) takes a retiree out of Texas's carry law (§ 46.02) and its places law (§ 46.03) when three things are true:

1. The person is an honorably retired peace officer or another qualified retired law enforcement officer as § 926C defines it.
2. The person holds a certificate of proficiency under Occupations Code § 1701.357.
3. The person carries a photo ID from a federal, state or local law enforcement agency that verifies the retired status.

The exemption does not mention §§ 30.05, 30.06 or 30.07 (trespass after notice), so owner bans still reach the retiree. Federal rules (§§ 922(q), 930, the airport sterile-area rule, postal and VA rules) are untouched.

## The certificate (Occupations Code § 1701.357)

- **Who can get it:** any qualified retired law enforcement officer entitled to carry under § 926C ((a-1)). Out-of-state and federal retirees are not excluded.
- **How:** demonstrate weapons proficiency to a qualified handgun instructor certified under Government Code § 411.190 and give TCOLE a sworn affidavit (926C eligibility; license never revoked or suspended; no disqualifying disability) ((b-1), (b-2)). A Texas state or local agency may also certify its own retirees ((b), (c)), and a state agency may certify other retirees ((h)).
- **How long:** one year from issue ((d)). This matches LEOSA's 12-month qualification window.
- **ID:** a certificate holder may ask the former agency for a photo ID showing honorable retirement or separation, and the agency must issue it ((i)). That is a Texas agency duty; it cannot bind a federal or out-of-state agency.
- **Proof of status** may include the Texas retired peace officer ID card (Government Code ch. 614, subch. H) ((c-2); not yet read).

## The retiree license (Government Code § 411.199)

- Honorably retired Texas peace officers may apply for a license to carry (LTC) at any time after retirement. The former agency must give a statement and may not refuse.
- Retired U.S. officers who carried on duty may apply too ((g)).
- Fees are waived ((d)). Classroom instruction is waived ((e)); range instruction is waived with a current § 1701.357 certificate ((e-1)).
- Why it matters: a license brings the license-holder defenses and rules: § 30.05(f) (trespass defense), § 30.06 and § 30.07 (sign-based trespass, Class C), and § 411.209 (government may not post signs on its property except where § 46.03 or other law bars license holders).

## Proposed carrier groups for the app

| Group | Who | Carry authority | Texas place law |
| --- | --- | --- | --- |
| `txcert` | LEOSA retiree with a current Texas § 1701.357 certificate and qualifying agency photo ID | § 926C and § 46.15(a)(5) | §§ 46.02, 46.03 do not apply. Owner notice (§ 30.05) and federal rules do |
| `retired` | LEOSA retiree relying on another state's or agency's qualification, with no Texas certificate | § 926C only | § 46.03 applies unless LEOSA overrides it. Government property and parks stay under § 926C(b)(2); the private-place bans are the open question |
| `txltc` | Texas license holder (including a § 411.199 retiree license) carrying under the license, not LEOSA | Government Code ch. 411, subch. H | § 46.03 applies in full, with the license-holder exceptions. Signs under §§ 30.06, 30.07 |

A retiree who holds both a certificate and a license can choose. The app should say which authority each answer assumes.

## Open questions (also in CHECKLIST.md)

1. For the `retired` group, which § 46.03 places does § 926C override?
2. Does a 30.06 or 30.07 sign count as notice under § 30.05 for someone who holds no Texas license?
3. Does a federal agency photo ID that does not say "retired" satisfy § 46.15(a)(5)?
4. Is "honorably retired peace officer" in § 46.15(a)(5) read with the § 411.199(c) definition (eligible to retire, not in lieu of discipline)?
