# TX — Layer 7F: force and the first hour (draft)

As of Nov 7, 2026. Feeds the app's four guide tabs for Texas: Now what?, Texas's view, Drill and Real cases. Every line rests on a source in `sources.md`. Draft: not reviewed by an attorney.

A retiree's force in Texas is judged as a private person's, under Penal Code chapter 9. LEOSA gives carry authority, not arrest or use-of-force authority (this project reads it that way; counsel question 1). Agency policy gives a retiree no authority.

## Research targets (STATE_WORKFLOW.md Layer 7F table)

| Target | Texas answer | Source | Status |
| --- | --- | --- | --- |
| Self-defense and deadly force statute | Force when the actor reasonably believes it is immediately necessary against another's unlawful force (§ 9.31(a)). Deadly force against unlawful deadly force, or to prevent the imminent commission of aggravated kidnapping, murder, sexual assault, aggravated sexual assault, robbery or aggravated robbery (§ 9.32(a)). Deadly force is force intended or known to cause, or capable in its use of causing, death or serious bodily injury (§ 9.01(3)) | §§ 9.01, 9.31, 9.32 | Verified |
| Retreat | No duty to retreat for a person who has a right to be present, did not provoke, and is not engaged in criminal activity; the jury may not consider failure to retreat for that person (§§ 9.31(e)–(f), 9.32(c)–(d)). No officer exception is needed, and none applies to a retiree | §§ 9.31, 9.32 | Verified |
| Presumption of reasonableness | Presumed reasonable if the actor knew or had reason to believe the other was forcibly entering or had entered the actor's occupied habitation, vehicle or place of business or employment, was forcibly removing the actor from one, or was committing a listed violent felony, and the actor did not provoke and was not engaged in criminal activity other than a Class C traffic offense (§§ 9.31(a), 9.32(b)) | §§ 9.31, 9.32 | Verified |
| Limits | Not justified: against words alone; to resist a known peace officer's arrest or search (unless the officer uses excessive force first); by a provoker who has not abandoned the encounter; or when the actor sought a discussion of differences while carrying illegally under § 46.02 (§ 9.31(b)) | § 9.31(b), (c) | Verified |
| Defense of others | Justified if, as the actor reasonably believes the facts to be, the actor could use the same force to protect himself, and believes intervention is immediately necessary (§ 9.33) | § 9.33 | Verified |
| Property and theft | Texas allows deadly force for property: against imminent arson, burglary, robbery, aggravated robbery, theft during the nighttime or criminal mischief during the nighttime, or to stop flight with the property after burglary, robbery or nighttime theft, if the actor reasonably believes the property cannot be protected or recovered another way, or that lesser force would expose someone to a substantial risk of death or serious bodily injury (§ 9.42). A third person's property is covered in listed cases (§ 9.43). This is broader than NJ or NY; the app must state the conditions, not the headline | §§ 9.41–9.43 | Verified |
| Arrest by a private person | A person other than a peace officer may use force to make a lawful arrest after making the purpose and reason known (§ 9.51(b)); deadly force only in the narrow cases of (d), which require acting in a peace officer's presence and at his direction. A retiree is a private person here (counsel question 1). The underlying warrantless-arrest rules (Code of Criminal Procedure ch. 14) not yet read | § 9.51(b), (d) | Verified (ch. 9); CCP not read |
| When justification ends | Every test is "immediately necessary" and "when and to the degree" (§§ 9.31, 9.32). Case law on continuing force not yet read | §§ 9.31, 9.32 | Cases not researched |
| Bystanders and stray rounds | Justification is unavailable in a prosecution for recklessly injuring or killing an innocent third person (§ 9.05). Civil remedies are not affected by justification (§ 9.06), but civil immunity covers the person the force was used against (CPRC § 83.001; whether it reaches a bystander's claim is a counsel question) | §§ 9.05, 9.06; CPRC § 83.001 | Verified |
| Drawing without firing | Producing a weapon to create apprehension that deadly force will be used if necessary is not deadly force, and a threat is justified when force is (§ 9.04). If not justified: aggravated assault by threat while exhibiting a deadly weapon, second-degree felony (§§ 22.01(a)(2), 22.02(a)(2)); deadly conduct, with pointing a firearm presumed reckless and dangerous whether or not loaded (§ 22.05(a), (c)); unlawful display in plain view (§ 46.02(a-5)) | §§ 9.04, 22.01, 22.02, 22.05, 46.02 | Verified |
| Pattern jury charge | Texas Criminal Pattern Jury Charges, State Bar of Texas. Not yet read; check for a free official text | — | Not researched |
| Burden of proof | Justification is a defense, not an affirmative defense (§ 9.02). Once evidence raises it, the jury is told a reasonable doubt on it requires acquittal (§ 2.03(c), (d)). It does not stop an arrest or a grand jury referral | §§ 2.03, 9.02 | Verified |
| Silence and counsel | Federal floor: *Salinas v. Texas*, 570 U.S. 178 (2013), a Texas case, holds that pre-arrest silence can be used unless the privilege is expressly invoked. Texas statement rules (Code of Criminal Procedure art. 38.22) not yet read | *Salinas*; CCP | Partly (Salinas is in the NY and NJ AUTH tables) |
| Charging and procedure | Magistrate warnings, bail and grand jury not yet read. Check article numbers after the 2023 recodification (H.B. 4504) | CCP | Not researched |
| The carry charge if LEOSA status fails | For most retirees, carrying is lawful under § 46.02 anyway (21 or older, not barred). The exposure is the place law: § 46.03, mostly a third-degree felony, and trespass after notice | §§ 46.02, 46.03, 30.05 | Verified |
| Who investigates | Not yet researched (Texas Rangers, local agency, county DA and grand jury) | — | Not researched |
| Agency use-of-force policy | Not yet researched (TCOLE model policies, if any). A yardstick only; gives a retiree no authority | — | Not researched |
| Training as evidence | "Reasonably believes" is defined in Penal Code § 1.07 (not yet read). Whether a jury weighs a retiree's training is a counsel question | — | Not researched |
| Civil exposure | Civil immunity for force justified under ch. 9 (CPRC § 83.001) | CPRC § 83.001 | Verified |
| Real cases | Not yet researched. Leads: Court of Criminal Appeals cases on the presumption, provocation, and § 9.31(b)(5); off-duty and retired officer cases; DA releases | — | Not researched |

## What Texas changes in the tabs (draft notes for `rules_tx.js`)

- **Now what?** The Texas carry crime is unlikely to be the issue (permitless carry); the place law and the force law are. Catches to draft: the property-at-night rule has conditions; the presumption is lost if the carrier provoked or was "engaged in criminal activity" (carrying in a § 46.03 place could be argued as that; counsel question 2); pointing a gun is presumed reckless under § 22.05(c), and the on-duty exception does not reach a retiree.
- **Texas's view.** Prove rows will be § 46.03 (place), § 30.05/30.06/30.07 (notice), and the § 46.15(a)(5) certificate as the retiree's answer. Officer and prosecutor rows wait on the procedure research.
- **Drill.** Good questions: Class C vs Class A trespass (d-3); what the certificate does and does not lift; when deadly force for property applies; who has no duty to retreat.
- **Real cases.** Not yet researched; do not fill from general knowledge.

## Counsel questions

1. Does a LEOSA retiree have any Texas arrest or force authority beyond a private person's? This project reads LEOSA as carry authority only.
2. Is carrying in a § 46.03 place (without the certificate) "criminal activity" that defeats the § 9.31(e) and § 9.32(c) no-retreat rule and the presumption?
3. Does CPRC § 83.001 reach a bystander's claim, given § 9.05?
4. Does § 9.31(b)(5) ever reach a LEOSA carrier (it names carrying "in violation of Section 46.02")?
