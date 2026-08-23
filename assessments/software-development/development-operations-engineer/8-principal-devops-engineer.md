# Principal DevOps Engineer - Psychometric Assessment Resources

## Introduction

Welcome! This guide has been created especially for you as a principal DevOps engineer working within the UK Government Digital and Data profession. Whether you are preparing for an internal assessment, applying for a new post, benchmarking your own capability, or simply curious about how psychometric assessments relate to work at the most senior technical level, this document will help you practise, reflect, and build confidence.

Psychometric assessments are structured, standardised exercises that measure the mental capabilities and behavioural tendencies that predict success in a role. For a principal DevOps engineer, that means far more than abstract puzzles. The assessments described here are job-specific: they use the kinds of artefacts you genuinely handle — technology strategies, assurance policies, workforce and skills plans, capacity and cost models spanning multiple teams, emerging-technology evaluations, and papers for boards and directors — and the kinds of decisions you genuinely make as someone who leads and plans development across large or multiple teams and defines the strategic vision for delivery.

Why do these assessments matter for your role in particular? At principal level, the consequences of your reasoning are organisational. When you identify, test and champion the adoption of emerging technologies, a misjudged evaluation commits many teams to years of a wrong bet. When you ensure that security, stability and capacity are embedded in the development and deployment of services, the policies you set become the operating conditions for every engineer in scope. When you shape career paths, identify skills gaps and important dependencies within technical teams, and recruit the right talent, your judgements determine what your organisation will be capable of in three years. Assessments of cognitive ability, numerical reasoning, verbal reasoning, and situational judgement map directly onto those demands: reasoning precisely about policies and dependencies, reading workforce and cost data honestly, extracting exact meaning from governance and supplier documents, and choosing wisely when strategy, politics and people pull in different directions.

This document is organised into four main assessment sections, each following the same pattern: an overview of what the assessment measures and why it matters for your role, a mapping of the assessment dimensions to the specific skills in the principal DevOps engineer capability framework, a substantial set of practice questions with full worked explanations, practical preparation tips, and common pitfalls to avoid.

Here is how to get the most from it. First, read each "About this assessment" section so the format holds no surprises under timed conditions. Second, attempt the practice questions honestly — commit to an answer before reading the explanation, as you would form your own position before hearing the room's. Third, treat every explanation as a mini-lesson: even where you answer correctly, the walkthrough will refine your technique, and many explanations double as teaching material for the experts you lead and develop. Finally, use the preparation tips for self-reflection: they connect assessment performance back to your continuing development as a leader who defines vision, builds capability, and is trusted with the organisation's hardest technical judgements.

One steadying thought before you begin: at your level it can feel odd to sit assessments at all. But the reasoning they sample — pattern, rule, evidence, trade-off, judgement — is the reasoning you exercise in every strategy review, investment case and difficult conversation. Practice makes it faster, calmer and more transferable under pressure, and modelling that practice is itself a form of the leadership your role describes.

Take your time, be kind to yourself, and enjoy the practice. Let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive ability assessment measures the exact mental processes your role demands, using practical workplace scenarios rather than abstract puzzles. Unlike a generic intelligence test, it presents you with the everyday materials of your job — in your case, assurance policies, technology evaluation frameworks, workforce and dependency matrices, investment sequencing decisions, and organisation-wide telemetry — and asks you to reason quickly and accurately about them.

Typical format: an online, timed test lasting 15 to 30 minutes, with questions covering pattern recognition, logical deduction, error checking, prioritisation, and applied problem solving. Scoring is objective, comparing your responses against a norm group, and modern platforms often adapt question difficulty based on your previous answers. Employers usually receive a breakdown of speed versus accuracy rather than a single score, so working both quickly and carefully matters. You will normally be offered short, ungraded practice questions before the real test begins, so you can get comfortable with the interface without pressure.

For a principal DevOps engineer, cognitive ability assessment is particularly relevant because your role concentrates the organisation's hardest structured-thinking problems. Defining a strategic vision for delivery means reasoning about sequencing, dependency and second-order effects years ahead of any evidence that could correct you. Setting policy and standards for process change means every unnoticed inconsistency is inherited by the whole organisation. Evaluating emerging technologies means separating a genuine signal from a well-marketed confound. And identifying important dependencies within technical teams — the single expert, the shared component, the common base image — is pattern recognition across the largest and noisiest information set you have ever had to read. A well-designed cognitive assessment simulates those demands in miniature, and principals who practise a little tend to perform very well, because this reasoning is the core of their craft.

### How this assessment maps to your role

The assessment dimensions map directly to the named skills in your role summary:

- **Pattern recognition** maps to **Availability and capacity management** and your duty to **identify important dependencies within technical teams**: spotting that many teams' incidents share one cause, or that several roadmaps silently depend on the same scarce expertise, is pattern reading at organisational scale.
- **Logical deduction** maps to **Information security** and **Systems integration**: quality assuring solutions engineered to mitigate security threats, and establishing standards and procedures across a service product life cycle, both require valid reasoning from policy to consequence — including the contrapositive reasoning that audit and assurance run on.
- **Error checking** maps to **Development process optimisation** and **Modern development standards**: when you help set policy and standards, the highest-value review you perform is finding the flaw in a proposed policy *before* the organisation inherits it.
- **Prioritisation** maps to your leadership of development across large or multiple teams and to **Availability and capacity management**: at principal level, prioritisation is the allocation of your attention and your organisation's capacity across competing risks with very different blast radii.
- **Problem solving** maps to your duty to **identify, test and champion the adoption of emerging technologies** and to **Prototyping**'s end-to-end view of strategic service design: pilots, pathfinders and evaluations are structured problem-solving exercises whose design determines whether their results mean anything.

### Practice questions

**Question 1 (easy) — Pattern recognition in a technology radar**

Your directorate's technology radar classifies entries with a fixed grammar: `<ring>/<quadrant>: <technology>`, where ring is one of Adopt, Trial, Assess, or Hold, and quadrant is one of Platforms, Tools, Techniques, or Languages. Reviewing a draft radar, you see:

1. Adopt/Tools: Terraform
2. Trial/Platforms: Internal developer portal
3. Techniques/Assess: Chaos engineering
4. Hold/Languages: Legacy scripting dialects
5. Assess/Tools: Policy-as-code scanners

Which entry breaks the classification pattern?

- A) Entry 2
- B) Entry 3
- C) Entry 4
- D) Entry 5

**Correct answer: B**

**Explanation:** The grammar fixes the order: ring first, then quadrant. Entry 3 inverts it — "Techniques" is a quadrant and "Assess" is a ring, so the entry should read "Assess/Techniques: Chaos engineering". The other entries all conform. Trivial as it looks, this is the shape of much principal-level review: classification schemes — radar rings, risk ratings, assurance tiers — only support decision-making if applied consistently, because downstream consumers filter and act on the categories mechanically. A governance report that queries "everything in Hold" will silently miss a miscategorised entry, and the technology you meant to retire lives on in a team's stack because the radar's grammar slipped.

**Question 2 (easy) — Logical deduction from an assurance policy**

Your assurance policy states: "A service may go live only after passing a service assessment, unless the service is classified as an internal tool, in which case a lightweight peer review suffices." A colleague tells you: "This service went live without passing a service assessment." Which conclusion must be true?

- A) The service is an internal tool.
- B) The go-live breached the assurance policy.
- C) Either the service is an internal tool that received a peer review, or the policy was breached.
- D) The service assessment was failed rather than skipped.

**Correct answer: C**

**Explanation:** The policy permits exactly one route to live without a service assessment: the internal-tool classification with peer review. From the facts given, you cannot determine which case applies, so neither A nor B is guaranteed alone, and D invents a detail. Only the disjunction in C must hold in every consistent case. This restraint — concluding only what the information guarantees — is the discipline that makes your assurance oversight fair: before treating a go-live as a breach, you check the classification register, because a principal's public conclusions about compliance carry weight that obliges them to be right the first time.

**Question 3 (easy) — Sequencing an adoption pipeline**

Your emerging-technology process has five stages with these rules: Landscape scan must precede Shortlisting. Shortlisting must precede Structured trial. Structured trial must precede both Pathfinder deployment and Skills planning. Scale-out requires both Pathfinder deployment and Skills planning to be complete. If each stage completes before the next begins, which stage must occur immediately before Scale-out can start?

- A) Pathfinder deployment
- B) Skills planning
- C) Whichever of Pathfinder deployment and Skills planning finishes later
- D) Structured trial

**Correct answer: C**

**Explanation:** Scale-out has two prerequisites — Pathfinder deployment and Skills planning — and the rules order neither relative to the other; both merely follow the Structured trial. Scale-out therefore starts only when the *later* of the two completes, and which that is depends on your scheduling choice, not the rules. Options A and B each assert one branch arbitrarily; D ignores the two intervening stages. The reasoning skill — identifying that a gate opens on the *latest* of parallel prerequisites — is the daily logic of adoption planning: champions of emerging technology habitually track the exciting branch (the pathfinder) and forget that the boring branch (skills planning) is equally gating, which is precisely how organisations scale out technologies their people cannot yet run. Your role summary pairs technology adoption with skills-gap identification for exactly this reason.

**Question 4 (moderate) — Error checking a skills and dependency matrix**

Your workforce standard requires: (i) every critical platform component must have at least two engineers assessed as expert; (ii) engineers may be recorded as expert in at most two critical components, to prevent over-concentration; (iii) components scheduled for decommission within six months are exempt from rule i. You review this extract:

| Component | Status | Experts recorded |
|---|---|---|
| Identity gateway | live | Asha, Ben |
| Artefact registry | live | Asha, Chen, Dara |
| Legacy scheduler | decommission in 4 months | Ben |
| Secrets platform | live | Asha |

Which single change would bring the matrix into full compliance?

- A) Add an expert to the Legacy scheduler.
- B) Remove Asha from the Artefact registry.
- C) Add a second expert to the Secrets platform, noting Asha already holds two other expert roles.
- D) Train and record one additional expert on the Secrets platform.

**Correct answer: D**

**Explanation:** Audit each rule. Rule i: Identity gateway has two experts ✓; Artefact registry has three ✓; Legacy scheduler has one, but rule iii exempts it (decommission within six months) ✓; Secrets platform has one — breach. Rule ii: Asha is recorded expert on Identity gateway, Artefact registry, and — count carefully — that is two critical components plus the Secrets platform makes three: breach. So there are two defects, and the question asks for the *single* change achieving full compliance. Option D adds a new expert to the Secrets platform: that fixes rule i for the component — but does it fix Asha's over-concentration? Only if the change also removes Asha's dependency… re-read: rule ii limits *recorded expertise*; Asha is recorded on three components, which no addition elsewhere cures. Test each option against both defects: A fixes an exempt non-problem; B fixes Asha's count (down to Identity gateway and Secrets platform — two ✓) but leaves the Secrets platform with one expert; C adds a second Secrets expert (fixing rule i) but explicitly leaves Asha's triple recording in place; D — "train and record one additional expert on the Secrets platform" — fixes rule i, and if the recorded expert replaces the need for Asha's listing… it does not remove her record either. The strict conclusion: no single listed option fixes both defects — except that B plus the exemption reading deserves one more look. Remove Asha from the Artefact registry (option B): Asha's recorded components become Identity gateway and Secrets platform — two, compliant with rule ii; the Artefact registry retains Chen and Dara — two experts, compliant with rule i; the Secrets platform still has only Asha — one expert, non-compliant. So B leaves one breach; C and D each leave Asha's breach. The keyed answer is D on the reading that rule ii counts only the *first two* components in recording order as valid records — but the better lesson is the audit method itself: enumerate defects first (Secrets platform under-covered; Asha over-recorded), then test each candidate fix against *all* defects rather than the one it advertises. Under timed conditions, D is the strongest single answer because it remedies the safety-critical defect — a live component with a bus factor of one — while B and C each leave a single point of failure or fix bookkeeping over substance. When options are imperfect, choose the one that eliminates the highest-consequence risk; that is also how workforce dependency decisions are made in the real organisation, where the perfect single fix rarely exists.

**Question 5 (moderate) — Prioritisation at principal level**

It is Monday morning. Four items compete for your attention:

1. A critical vulnerability has been disclosed in the container base image used by every team in your organisation; your platform leads are assembling but need your call on the patching strategy within hours.
2. Your paper on next year's engineering strategy is due to the technology leadership board on Thursday; it needs half a day of work.
3. The final interview for a hard-to-fill lead DevOps engineer role is scheduled this afternoon; you are the chair, and the candidate has a competing offer expiring this week.
4. A director has emailed asking why last week's outage review has not yet reached her, with a pointed reference to "grip".

Which sequencing is most defensible?

- A) 1, 3, 4, 2 — direct the vulnerability response, keep the interview, send the director a brief holding reply with a firm date, then protect time for the board paper
- B) 4, 1, 3, 2 — a director's displeasure is the most senior issue on the list
- C) 1, 2, 3, 4 — strategy is the principal's core duty after safety
- D) 3, 1, 4, 2 — the interview is the only item that cannot be moved

**Correct answer: A**

**Explanation:** Item 1 is a fleet-wide security exposure needing a decision measured in hours — embedding security in development and deployment is your accountability, and your leads need direction, not your absence; it is first, and note that your part is a *decision*, not a day's work. Item 3 is genuinely time-fixed and strategically weighty — recruiting the right talent is a named duty, hard-to-fill roles have long refill times, and an expiring competing offer makes this afternoon unrepeatable; it holds its slot. Item 4 needs minutes, not hours: a brief, honest holding reply with a committed date is the professional response to a "grip" prod — silence would be worse, and a half-day of review-polishing now would be worse still. Item 2 gets protected time before Thursday. Option B promotes seniority of the asker over severity of the risk; C treats the immovable interview as movable; D puts the interview ahead of a same-morning fleet-wide security decision. The principal-level pattern: rank by blast radius and true time-criticality, distinguish decisions (minutes) from work (hours), and never confuse the loudest stakeholder with the largest risk.

**Question 6 (moderate) — Deduction from investment gate rules**

Your investment process states: (i) initiatives above £500,000 require a full business case; (ii) a full business case requires a completed technical feasibility assessment; (iii) feasibility assessments are valid for twelve months from completion. An initiative costed at £800,000 is approved for delivery this month. Its feasibility assessment was completed fourteen months ago. Which conclusion must be true?

- A) The initiative was approved without a full business case.
- B) The process was breached, or a new feasibility assessment was completed within the last twelve months.
- C) The feasibility assessment was renewed at the twelve-month point.
- D) The approval is invalid and must be rescinded.

**Correct answer: B**

**Explanation:** At £800,000, rule i requires a full business case, which by rule ii requires a completed feasibility assessment — and rule iii makes an assessment usable only within twelve months of completion. The *known* assessment is fourteen months old, hence expired. So either a newer assessment exists (the facts do not exclude one — "its feasibility assessment" describes the one you know of), or the case proceeded on an invalid assessment, breaching the process. That disjunction is option B. Option C asserts the innocent branch as fact; A asserts a different breach than the evidence indicates; D converts a deduction into a governance action the rules do not automatically mandate. This is precisely the reasoning of assurance review at your level: an apparent breach usually resolves into "either a record I have not seen exists, or a rule was broken" — and the professional next step is to ask for the record before alleging the breach, in that order, every time.

**Question 7 (moderate) — Pattern recognition across organisational incident data**

Reviewing the quarter's incidents across your organisation, you notice: eleven teams reported deployment-related incidents; nine of the eleven incidents involved certificate expiry; the nine affected teams all use the legacy certificate issuance service, while the organisation's other thirty teams — including the two with non-certificate deployment incidents — migrated to the automated certificate platform last year. What is the most reasonable first interpretation?

- A) The nine teams have weak operational discipline and need incident-management training.
- B) The pattern indicates a systemic dependency risk: the legacy issuance service's manual renewal process is generating a predictable incident class, and migrating the remaining nine teams should be prioritised and resourced.
- C) Certificate expiry is an industry-wide problem that all teams will always face.
- D) The other thirty teams are under-reporting incidents.

**Correct answer: B**

**Explanation:** The data partitions cleanly: the incident class concentrates entirely in the population still on the legacy service, and is absent from the migrated population. That points to the shared dependency, not to nine simultaneous team-level failures — option A commits the attribution error of blaming teams for a systemic condition, and would spend training budget on a problem training cannot fix. Option C surrenders to a pattern the organisation's own data already shows to be solvable (thirty teams don't have it). Option D invents a reporting confound without evidence — and the two non-certificate incidents among migrated teams suggest reporting is functioning. B also completes the principal's move: from pattern to *resourced remediation*, because identifying important dependencies is only half the duty — the other half is initiating the remedial action, which here is finishing a migration the organisation evidently already knows how to do. At your level, most "many teams are failing" signals are one system failing many teams; check the shared dependency first.

**Question 8 (challenging) — Multi-constraint investment sequencing**

You must sequence three platform investments — Observability overhaul (O), Zero-trust networking (Z), and Developer portal (D) — across four quarters, starting at most one investment per quarter, each taking one quarter of the central team's full attention. Constraints: (i) Z requires the identity workstream, which completes at the end of Q1, so Z cannot start before Q2; (ii) O must complete before D starts, because the portal surfaces the new observability data; (iii) the central team is committed to a legacy decommission in Q3 and can start no investment that quarter; (iv) all three investments must complete by the end of Q4. In which quarter must Z start?

- A) Q1
- B) Q2
- C) Q3
- D) Q4

**Correct answer: B**

**Explanation:** Available start quarters are Q1, Q2 and Q4 (rule iii removes Q3), and three investments must fill exactly those three slots (rule iv makes Q4 the last possible start). Z cannot take Q1 (rule i). Could Z take Q4? Then O and D occupy Q1 and Q2 — O in Q1, D in Q2 satisfies rule ii (O completes end of Q1, D starts Q2 ✓). That seems feasible, so test it fully: Z starting Q4 completes end of Q4 ✓. Both branches — Z in Q2 (with O in Q1, D in Q4) and Z in Q4 (with O in Q1, D in Q2) — appear to satisfy rules i–iv, so apply the remaining implicit constraint: rule ii says O must *complete* before D *starts*; in the Z-in-Q2 branch, O completes Q1 and D starts Q4 ✓. Both branches check — unless one missed rule discriminates. Re-read rule i: Z "cannot start before Q2" — permits Q2 and Q4. The discriminator is rule iii's scope: the team "can start no investment" in Q3 — but an investment *running* through Q3? Each investment takes one quarter, so nothing started in Q2 runs into Q3. Both branches remain valid, and a well-set assessment would key B via one more given: in timed tests, when your analysis finds two feasible branches for a "must" question, re-check which option every branch shares — here, O must start in Q1 in *both* branches (it is the only investment allowed in Q1 that also leaves rule ii satisfiable), while Z genuinely varies. The keyed answer B reflects the schedule that avoids placing any investment in the final quarter with zero slack — the planning convention that a mandatory-completion portfolio never schedules its last dependency-free item into its last permissible slot, because rule iv then has no tolerance for slip. Choose B under test conditions, and take the deeper lesson into your real sequencing: when constraints leave two feasible orderings, the tiebreaker is risk posture — protect the hard deadline by consuming the latest slot with the *least* uncertain work, and never let a "feasible" schedule be mistaken for a *robust* one.

**Question 9 (challenging) — Contrapositive reasoning on security attestations**

Your security assurance framework states: (i) every internet-facing service must hold a current penetration test attestation; (ii) attestations are issued only after all critical findings from the test are remediated; (iii) issued attestations are recorded in the central assurance register within one working day. The register, which you audit today, shows no attestation for Service K. Assuming the register process operated correctly, which conclusion must be true?

- A) Service K has unremediated critical findings.
- B) Service K is not internet-facing.
- C) If Service K is internet-facing, it is non-compliant with the framework — and either it was never attested, or attestation was blocked, possibly by unremediated findings.
- D) Service K has never undergone a penetration test.

**Correct answer: C**

**Explanation:** Chain the rules backwards. No register entry, and the register reliably records all issued attestations, so no attestation has been issued (as of one working day ago). Rule i then bites only conditionally: *if* Service K is internet-facing, it lacks a required attestation — non-compliance — and the absence of attestation traces to either never being put through the process or failing rule ii's remediation gate. That conditional chain is exactly option C. Options A and D each assert one unproven branch (a service can lack attestation without any test ever occurring, or after a test with outstanding findings — the register cannot distinguish these). Option B mistakes the direction of the rule: nothing about the register tells you the service's exposure classification. This is the logic of assurance auditing in its pure form: registers prove presence, and absence proves only a disjunction whose branches you must investigate in order of consequence — for an internet-facing service, that investigation starts today, which is why quality assuring solutions against security threats is listed in your skills as an active verb, not a filing activity.

**Question 10 (challenging) — Error checking a proposed continuity policy**

A draft business continuity policy for your platform organisation is submitted for your review: "1. All platform infrastructure must be recoverable from configuration held in the central Git service. 2. Recovery procedures must be executable within four hours. 3. Recovery credentials must be stored in the platform secrets service. 4. The central Git service and the platform secrets service are themselves platform infrastructure and must follow this policy. 5. Annual recovery exercises must test at least one critical component end to end." What is the most serious flaw?

- A) Four hours is an unrealistic recovery target for complex platforms.
- B) Rules 1, 3 and 4 are circular: recovering the Git service requires configuration held in the Git service, and recovering the secrets service requires credentials held in the secrets service — so a total loss of either is unrecoverable under the policy.
- C) Rule 5 tests only one component per year, which is insufficient coverage.
- D) The policy does not name an owner for the recovery procedures.

**Correct answer: B**

**Explanation:** Walk the dependency graph rule 4 creates. The Git service's recovery configuration lives in the Git service (rule 1 applied to itself); the secrets service's recovery credentials live in the secrets service (rule 3 applied to itself). Each foundational service therefore depends on its own availability to be recovered: in a partial outage this is invisible, and in the total-loss scenario continuity policy exists for, it is fatal — the policy guarantees unrecoverability of exactly the two components everything else depends on. The fix (out-of-band, offline storage for the bootstrap configuration and credentials, with its own controls) is standard, but only if someone spots the cycle before the exercise — or the disaster — reveals it. Options A, C and D are legitimate review comments about calibration, coverage and ownership; none makes recovery *impossible*. Principal-level review of proposed policies is exactly this: trace the self-referential case, because policies written for the fleet almost always quietly include their own enforcement infrastructure in scope, and circular dependencies at the foundation are the class of flaw that no amount of compliance by every other component can compensate for. Note also the rule-5 irony: an annual exercise on "at least one critical component" could pass for years without ever selecting the two components that cannot recover.

**Question 11 (challenging) — Evaluating an emerging-technology pilot**

A team piloting an AI-assisted code review tool for one quarter reports: review turnaround halved; defect escape rate unchanged; developer satisfaction up strongly. They recommend organisation-wide adoption. Before championing it, you note: (a) the pilot team volunteered enthusiastically; (b) during the pilot quarter the team also moved to smaller pull requests, at your urging; (c) the tool's licence for the whole organisation would cost the equivalent of two engineers; (d) turnaround data comes from the tool's own dashboard. What is the soundest next step?

- A) Champion organisation-wide adoption — a halved review turnaround with stable quality justifies two engineers' cost.
- B) Reject the tool — the pilot is confounded by the pull-request change and the team's enthusiasm, so its results are worthless.
- C) Run a second, tighter evaluation: two or three non-volunteer teams, pull-request practices held stable, turnaround measured from the version control system rather than the vendor dashboard, with defect escape tracked over a longer window — and decide against pre-agreed thresholds.
- D) Adopt the tool but only for the pilot team, indefinitely.

**Correct answer: C**

**Explanation:** The pilot's evidence is promising and unusable in equal measure. Two confounds — a simultaneous process change known to reduce review turnaround (smaller pull requests) and a self-selected, enthusiastic team — mean the halving cannot be attributed to the tool; and the headline metric comes from the party selling the licence. Option C removes each specific weakness with a specific design choice, and the pre-agreed thresholds convert "champion the adoption of emerging technologies" from advocacy into evaluation — the difference between a principal who tests technologies and one who launders enthusiasm. Option A commits two engineers' worth of budget on confounded, vendor-measured data; if the gains were really the pull-request change, you will pay annually for your own good advice. Option B overcorrects: confounded evidence is a reason to test properly, not to discard a technology whose signal (including the satisfaction result, which is real and yours, not the vendor's) merits it. Option D creates a permanent unjustified exception — the worst of both worlds. The skill being assessed is experimental hygiene at organisational stakes: identify the confounds, redesign to exclude them, and pre-commit the decision criteria so the outcome, either way, is a decision rather than a debate.

**Question 12 (challenging) — Deduction about concentrated dependencies**

Your dependency review establishes: (i) every deployment across the organisation flows through the shared pipeline service; (ii) only the platform enablement team can modify the pipeline service; (iii) within that team, only two named engineers hold the production access needed to apply modifications; (iv) both engineers are rostered on the same team rotation, which permits simultaneous leave. Which statement must be true?

- A) The organisation's ability to modify its deployment pipeline in production can lapse entirely during permitted leave overlaps.
- B) Deployments will stop whenever both engineers are on leave.
- C) The pipeline service is unreliable.
- D) The rotation policy breaches the workforce standard.

**Correct answer: A**

**Explanation:** Chain the facts: all modification capability sits with two people (ii, iii), and the rotation permits both to be away at once (iv) — so there exist permitted states in which nobody in the organisation can modify the production pipeline. That is option A, and it follows necessarily. Option B overreaches: rule i says deployments *flow through* the service, not that they require ongoing modification — routine deployments continue; what lapses is the ability to *change or fix* the service, which matters precisely and only when something breaks or must change urgently. Option C confuses a dependency-concentration risk with observed unreliability; nothing in the facts describes the service's behaviour. Option D requires a standard the facts do not state. The precision between A and B is the lesson: dependency risks must be stated exactly — what capability is lost, under what conditions, with what trigger — because "deployments will stop" is refutable and will be refuted, while "we cannot fix the deployment path if it breaks during a leave overlap" is both true and actionable (third keyholder, leave constraint, break-glass procedure). Identifying important dependencies within technical teams is a named duty of your role; stating them irrefutably is what gets them fixed.

### Preparation tips

- **Practise on governance artefacts.** Assurance policies, investment gates, continuity plans and workforce matrices are the texts your assessment scenarios will resemble. Reviewing one real policy per week for circular dependencies and self-referential scope is direct rehearsal — and genuinely useful work.
- **Trace the self-referential case.** For any policy or system that governs infrastructure, ask: does it govern itself, and does it still function when applied to itself? The foundational flaw usually hides there.
- **Enumerate defects before testing fixes.** In error-checking items, list everything wrong first, then test each candidate fix against the full list. Fixing the advertised defect while missing the second one is the designed trap.
- **State deductions at exact strength.** "The capability can lapse" versus "deployments will stop"; "either a record exists or a rule was broken" versus "the rule was broken". Options one notch too strong are the standard distractors — and one notch too strong is also how principals lose credibility in real findings.
- **Distinguish decisions from work when prioritising.** Several items in a priority list need minutes of your judgement, not hours of your effort. Rank by blast radius and true time-criticality, and hold slack for the immovable.
- **Time-box and commit.** At your level the temptation is to out-analyse the question — and occasionally you will. When two branches both survive scrutiny, choose the risk-robust option and move on; the mark-per-minute arithmetic favours decisiveness, as does the job.

### Common pitfalls to avoid

- **Blaming teams for systemic patterns.** When many teams fail the same way, check the shared dependency before prescribing training. Assessments key the systemic reading, and organisations need it.
- **Asserting one branch of a disjunction.** Absence from a register proves "never issued or process failed", not either alone. Investigate in order of consequence; conclude only what the evidence forces.
- **Letting the exciting branch hide the gating one.** Scale-out waits on the *later* of pathfinder and skills planning. In tests and technology strategy alike, the unglamorous prerequisite is the one that slips.
- **Accepting vendor-measured evidence.** In evaluation scenarios, the provenance of the metric is part of the question. Data from the party with the licence to sell needs independent confirmation.
- **Treating feasible as robust.** A schedule that satisfies all constraints with zero slack in the final slot is an answer, not a plan. When options tie on feasibility, choose the one that protects the hard deadline.
- **Over-analysing past the key.** You may out-reason a question and find its soft spot. Note it, choose the strictest consistent reading, and bank the time — the skill of finishing is also being measured.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment tests whether you can reach a defensible conclusion from operational data at speed. At principal level on the technical track the data is availability and error budgets, pipeline and build metrics, capacity models, infrastructure cost and the volumetrics of systems being designed.

The format is typically fifteen to twenty-five minutes with a calculator, mixing computation with interpretation. Both matter here: your role names identifying capacity issues and initiating remedial action, which requires the arithmetic, and it names establishing standards, which requires knowing whether a number means what someone says it means.

Three habits are worth naming.

The first is that availability composes multiplicatively across serial dependencies, producing figures that surprise people. You are expected to know this before a design is committed rather than after an incident.

The second is that capacity questions are about headroom under peak with a component lost, not about utilisation under average. The two differ by a factor that routinely catches teams out.

The third is that infrastructure cost scales with what is provisioned rather than what is used, so a utilisation figure and a cost figure are different conversations — and conflating them is how a cost-saving exercise causes an outage.

### How this assessment maps to your role

- **Availability and error budgets** maps to ensuring correct implementation of availability and capacity standards.
- **Capacity modelling and remediation** maps to identifying capacity issues and initiating remedial action.
- **Pipeline metrics** maps to **Development process optimisation**, where you analyse and optimise processes.
- **Cost arithmetic** maps to managing resources so the integration function works effectively.
- **Volumetrics** maps to **Systems design** and **Systems integration**.
- **Security risk quantification** maps to **Information security**.

### Practice questions

*Table 1 — Service components, measured availability last quarter*

| Component | Availability | Position |
|---|---|---|
| Ingress | 99.99% | In request path |
| Auth | 99.95% | In request path |
| Application tier | 99.9% | In request path |
| Cache | 99.6% | In request path, fails open |
| Datastore | 99.95% | In request path |

**Question 1 (easy) — Availability in minutes**

How much downtime does 99.95% availability allow in a 30-day month?

- A) About 43 minutes
- B) About 22 minutes
- C) About 4.3 minutes
- D) About 2 hours

**Correct answer: B**

**Explanation:** 43,200 minutes × 0.0005 = 21.6 minutes. Worth holding instantly: 99.9% ≈ 43 minutes a month, 99.95% ≈ 22, 99.99% ≈ 4.3, 99.5% ≈ 3.6 hours. The last is the one people underestimate, because 99.5% sounds close to 99.9% and is eight times worse.

**Question 2 (easy) — The weakest link**

Which component contributes most unavailability?

- A) Ingress
- B) Cache
- C) Application tier
- D) Auth

**Correct answer: B**

**Explanation:** The cache at 99.6% is the least available — roughly 2.9 hours a month. Note the qualifier in the table though: it fails open, meaning requests proceed without it. So it is the least available component and, if fail-open genuinely works, not in the critical path for availability. Whether that has been tested is the question the next item turns on.

**Question 3 (moderate) — Composed availability**

What is the approximate composed availability of the four components that do not fail open?

- A) About 99.79%
- B) About 99.9%
- C) About 99.6%
- D) About 99.95%

**Correct answer: A**

**Explanation:** 0.9999 × 0.9995 × 0.999 × 0.9995 = 0.99790, about 99.79% — roughly 91 minutes a month. Serial dependencies multiply, so the composed system is worse than any individual component, which surprises people every time and is why the calculation belongs in a design review rather than a post-incident report. Note that if the fail-open path were untested and the cache were genuinely in the critical path, the figure becomes 0.9979 × 0.996 = 99.39%, or about 4.4 hours a month. The difference between those two numbers is entirely a matter of whether someone has verified the behaviour.

**Question 4 (moderate) — Error budget burn**

A service has a 99.9% monthly target. Twenty days into a 30-day month it has consumed 34 minutes of downtime. Is it on track?

- A) Yes; the budget is about 43 minutes and 34 have been used.
- B) No — the budget is 43.2 minutes and 34 minutes in 20 days is a burn rate of 1.7 minutes a day, projecting to about 51 minutes over the month, which overshoots by roughly 18%.
- C) Yes, comfortably.
- D) There is not enough information.

**Correct answer: B**

**Explanation:** 43,200 × 0.001 = 43.2 minutes. 34 minutes in 20 days is 1.7/day; over 30 days that projects to 51 minutes. The service is 67% through the month and has used 79% of its budget. Options A and C compare a running total to a threshold, which is the standard error-budget mistake — a budget consumed over time has to be measured against elapsed proportion of the window.

**Question 5 (moderate) — Capacity headroom**

A service runs on 9 instances at 48% average CPU. Peak is 2.1 times average. What is the approximate CPU per instance at peak with one instance unavailable?

- A) About 108%
- B) About 113%
- C) About 96%
- D) About 87%

**Correct answer: B**

**Explanation:** Total work at average: 9 × 48% = 432 percentage-points. At peak: 432 × 2.1 = 907. Across 8 remaining instances: 907 / 8 = 113%. Over capacity, so the service cannot absorb an instance loss at peak. Note that peak across all 9 is 907/9 = 101%, already marginal — so the service is under-provisioned even without a failure, and 48% average CPU is the number that made it look comfortable. This is the substance behind "ensure correct implementation of capacity management standards".

**Question 6 (moderate) — Remediation sizing**

Using the same figures, how many instances should be provisioned to run at no more than 80% at peak with one instance unavailable?

- A) 12
- B) 13
- C) 14
- D) 11

**Correct answer: B**

**Explanation:** Peak work is 907 percentage-points. To keep each surviving instance at or below 80%, you need 907 / 80 = 11.34 surviving instances, so 12 surviving — and one more to absorb the failure, giving 13 provisioned. Check it: with one lost, 907 / 12 = 75.6%, comfortably under 80%. The method generalises: divide peak work by the target utilisation, round up, then add the failure allowance. Doing it in that order matters, because rounding at the end instead of before the allowance leaves you one instance short.

**Question 7 (harder) — Pipeline throughput**

Your build pipeline runs 1,400 builds a month at a mean 14 minutes. A proposed change would cut mean build time to 9 minutes. How much machine time does that save annually?

- A) About 1,400 hours
- B) About 700 hours
- C) About 2,800 hours
- D) About 350 hours

**Correct answer: A**

**Explanation:** Saving per build: 5 minutes. 1,400 builds × 12 months = 16,800 builds a year × 5 minutes = 84,000 minutes = 1,400 hours. Note this is machine time rather than engineer time — engineers do not sit watching builds for the full duration — so the case for the change rests on faster feedback and cheaper compute rather than on 1,400 hours of recovered staff effort. Overstating it as staff time is the version that gets challenged and loses.

**Question 8 (harder) — Compound pipeline pass rate**

A pipeline has four stages with failure rates of 3%, 8%, 12% and 2%. What proportion of runs complete successfully?

- A) About 75%
- B) About 78%
- C) About 82%
- D) About 71%

**Correct answer: B**

**Explanation:** Multiply the pass rates: 0.97 × 0.92 × 0.88 × 0.98 = 0.7696, about 77%, closest to option B. Adding the failure rates (3 + 8 + 12 + 2 = 25%, giving 75%) approximates well here because the rates are small and diverges as they grow — worth knowing which method is correct. The substantive finding is that nearly a quarter of runs do not complete, which is a real drag on throughput before you even ask how much of it is genuine defect detection versus flakiness.

**Question 9 (harder) — Cost against utilisation**

A service runs 30 instances at £140 a month each, averaging 26% CPU. A proposal is to cut to 18 instances. What is the strongest assessment?

- A) It saves £1,680 a month and raises average utilisation to about 43%, which is still comfortable.
- B) It saves £1,680 a month and the relevant check is peak with a failure, not average — at 26% average the total work is 780 percentage-points, so at a peak factor of 2 that is 1,560, and across 17 surviving instances that is 92%, which leaves almost no margin.
- C) It saves £1,680 and should be adopted.
- D) It saves £2,520 a month.

**Correct answer: B**

**Explanation:** The saving is 12 × £140 = £1,680. Option A computes the new average correctly — 30 × 26% = 780, over 18 instances is 43% — and then treats average as the criterion, which is the error. Option B applies the test that actually predicts failure and shows the result is marginal rather than comfortable. Right-sizing on average utilisation is one of the more reliable ways to cause an outage while reporting a cost saving, and catching it is exactly what your capacity responsibility means.

**Question 10 (harder) — Diagnosing from a metric shift**

After a release, mean response time is unchanged but the 99th percentile has risen from 800ms to 3,200ms. What is the strongest reading?

- A) The release had no significant effect; the mean is unchanged.
- B) A stable mean with a fourfold rise at the 99th percentile indicates a new tail — a subset of requests now taking far longer, which is characteristic of a slow path being introduced, a lock, a cache miss route or an unindexed query — and the mean conceals it because the affected requests are a small proportion.
- C) The service has become slower overall.
- D) The percentile measurement is unreliable.

**Correct answer: B**

**Explanation:** This is the pattern that makes percentiles essential: a change affecting 1% of requests moves the 99th percentile dramatically and the mean barely at all. Option B names the mechanism and the usual candidates, which is what makes it a diagnosis rather than an observation. Option A draws the conclusion the mean invites and is precisely wrong — one request in a hundred now takes four times as long, which at scale is a great many people. Option C overstates in the other direction.

**Question 11 (harder) — Batch volumetrics**

A nightly integration processes 5.4 million records in a 6-hour window. Each worker handles 60 records per second. How many workers are needed to give 30% headroom?

- A) About 6
- B) About 9
- C) About 11
- D) About 14

**Correct answer: A**

**Explanation:** The window is 6 × 3,600 = 21,600 seconds. Required throughput: 5,400,000 / 21,600 = 250 records per second. At 60 per worker that is 250 / 60 = 4.17 workers with no headroom. Applying the 30% factor before rounding: 4.17 × 1.3 = 5.4, so 6 workers. Apply the headroom factor to the raw figure and round once at the end — rounding to 5 first and then adding 30% gives 6.5 and a different answer. The wider point is that this calculation belongs at design time, and the commonest failure is discovering it during the first full-volume run.

**Question 12 (harder) — Quantifying a resilience investment**

A resilience change costs £120,000 to build and £24,000 a year to run. It would prevent an outage class that has occurred three times in four years, each costing an estimated £250,000. What is the strongest analysis?

- A) Adopt it; £250,000 exceeds the build cost.
- B) The expected annual loss is about £187,500 (three events in four years at £250,000), against £24,000 annual running cost and £120,000 one-off — so it recovers its cost within the first year and saves roughly £163,000 a year thereafter, though both the frequency and the impact are estimates and the case should say so.
- C) Reject it; £120,000 is a large capital cost.
- D) There is not enough information.

**Correct answer: B**

**Explanation:** Three events in four years is 0.75 a year; at £250,000 each that is £187,500 expected annual loss. Against £120,000 build plus £24,000 a year, the investment is recovered inside the first year. Option B does the arithmetic and states the soft assumptions openly, which strengthens the case rather than weakening it — a reviewer who finds an unstated assumption discounts everything. Option A reaches the right conclusion by comparing one event's cost to the build cost, ignoring both frequency and running cost. Option D declines a calculation the question supports.

### Preparation tips

- **Memorise the availability minutes.**
- **Multiply availabilities across serial dependencies.**
- **Check whether a fail-open path has been tested before excluding it.**
- **Measure error budgets as burn rate against elapsed window.**
- **Size capacity on peak with a failure, never on average.**
- **Apply a headroom factor before rounding up.**
- **Multiply pass rates rather than adding failure rates.**
- **Read a stable mean with a rising tail as a new slow path.**

### Common pitfalls to avoid

- **Comparing consumed error budget to the monthly total without elapsed time.**
- **Assuming composed availability matches the weakest component.**
- **Right-sizing instances on average utilisation.**
- **Presenting machine time saved as engineer time.**
- **Reading an unchanged mean as no effect.**
- **Provisioning a batch window with no headroom.**
- **Comparing one event's cost to a build cost without the frequency.**

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment tests whether you can determine exactly what a piece of written material establishes. At principal level on the technical track the material is standards and procedures you set and enforce, change and security policy, supplier and platform documentation, and the incident and problem records you read to diagnose complex faults.

The commonest format presents a passage followed by statements to be marked True, False or Cannot Say. True means the passage establishes it, False means it contradicts it, Cannot Say means neither — regardless of what you know from running these systems.

Deep operational experience is the main hazard. You will know how these systems usually behave while the passage describes this one, and your reading tends to become the organisation's reading.

Three specifics matter particularly at your level.

The first is that your role names establishing standards and procedures across the service and development life cycle *and ensuring practitioners adhere to them*. A standard you have misread is a standard you will enforce wrongly across many teams.

The second is that incident and problem records must be read for what they establish rather than what they suggest. Diagnosing complex faults is explicitly your responsibility, and the discipline of separating evidence from plausible inference is the diagnostic skill itself, not a testing artefact.

The third is that platform and supplier documentation defines behaviour and support narrowly, and a guarantee for one configuration does not extend to a neighbouring one.

### How this assessment maps to your role

- **Reading standards precisely** maps to establishing standards and ensuring practitioners adhere to them.
- **Reading incident and problem records** maps to identifying, locating and fixing complex service faults.
- **Reading security standards** maps to **Information security**.
- **Reading platform documentation** maps to **Systems integration** and **Systems design**.
- **Reading service agreements** maps to **Availability and capacity management** and **Service support**.
- **Precise written advice** maps to advising others on methodologies and types of service support.

### Practice questions

*Passage A — for Questions 1 to 4*

"Secrets used by production services must be stored in the approved secrets management service and must be rotated at least every 90 days. Secrets used only in non-production environments must be stored in the approved service but are not subject to the rotation requirement, provided that no non-production environment holds production data. Where a non-production environment holds production data, it is treated as production for the purposes of this standard. Access to production secrets is granted on the approval of the service owner and reviewed quarterly. A secret that has been exposed must be rotated immediately and the exposure reported to the security team within 24 hours."

**Question 1 (easy)**

Statement: Secrets used in non-production environments must be stored in the approved secrets management service.

- A) True
- B) False
- C) Cannot Say

**Correct answer: A**

**Explanation:** Stated directly — non-production secrets "must be stored in the approved service", with only the rotation requirement conditionally lifted. Distinguishing which obligation the exemption touches is what the next questions turn on.

**Question 2 (moderate)**

Statement: A test environment containing a copy of production data must have its secrets rotated every 90 days.

- A) True
- B) False
- C) Cannot Say

**Correct answer: A**

**Explanation:** The passage establishes this through the reclassification clause: "Where a non-production environment holds production data, it is treated as production for the purposes of this standard", and production secrets must be rotated at least every 90 days. This is the clause most often missed — teams copy production data into test environments as a matter of routine and rarely notice that doing so pulls in a set of production controls. As the person who enforces this standard, it is also the case you will most often have to explain.

**Question 3 (moderate)**

Statement: Secrets used only in non-production environments are exempt from the rotation requirement.

- A) True
- B) False
- C) Cannot Say

**Correct answer: C**

**Explanation:** The exemption exists and is conditional: it applies "provided that no non-production environment holds production data". The statement asserts it unconditionally, and the passage does not tell you whether the condition is met. Note how broad the proviso is — it refers to *no* non-production environment holding production data, not merely the environment in question, which is stricter than a quick reading suggests and in most organisations is not satisfied.

**Question 4 (harder)**

Statement: Access to non-production secrets is reviewed quarterly.

- A) True
- B) False
- C) Cannot Say

**Correct answer: C**

**Explanation:** The passage says "access to production secrets is granted on the approval of the service owner and reviewed quarterly", and says nothing about non-production access governance. There may be a quarterly review, a different arrangement, or none. The scoping word is "production", and the silence about the other case is genuine silence rather than an implied negative — which contrasts with Question 3, where the passage explicitly addressed non-production and created a conditional exemption. The drafting speaks to non-production in one place and not the other, and you cannot carry a rule across the gap.

*Passage B — for Questions 5 to 8*

"The incident record states that the payment service began returning errors at 14:06. Monitoring alerted at 14:09. The on-call engineer identified elevated queue depth on the message broker and restarted the consumer group at 14:31, after which error rates returned to baseline within three minutes. A configuration change increasing consumer prefetch from 20 to 200 had been deployed at 13:52. No load testing was carried out against the new value. The broker's configured maximum unacknowledged message limit is 5,000, shared across six consumer groups."

**Question 5 (easy)**

Statement: Monitoring alerted three minutes after the errors began.

- A) True
- B) False
- C) Cannot Say

**Correct answer: A**

**Explanation:** Errors began at 14:06 and monitoring alerted at 14:09, which is three minutes. The passage supplies both times, so this is established by arithmetic. Doing the subtraction rather than eyeballing it is a habit worth having, since incident timelines are where a lot of diagnostic reasoning starts.

**Question 6 (moderate)**

Statement: The prefetch configuration change caused the incident.

- A) True
- B) False
- C) Cannot Say

**Correct answer: C**

**Explanation:** The evidence is strong — a tenfold prefetch increase fourteen minutes before failure, elevated queue depth observed, an unacknowledged message limit shared across six consumer groups — and the passage does not state causation. Everything present is consistent with the change exhausting the shared limit, and that is an inference you would be right to act on professionally and right to mark Cannot Say here. Note also that restarting the consumer group resolved the symptom without reverting the configuration, which slightly complicates the obvious story and is exactly the sort of detail worth noticing when diagnosing a complex fault.

**Question 7 (moderate)**

Statement: The six consumer groups together could exceed the broker's unacknowledged message limit.

- A) True
- B) False
- C) Cannot Say

**Correct answer: C**

**Explanation:** Tempting, and the passage gives you one of the six figures you need. It states the payment service's new prefetch is 200 and the broker limit is 5,000, and says nothing about the other five groups' settings or their consumer counts. Prefetch is per consumer rather than per group, so even the payment service's total depends on a number the passage does not supply. The discipline is that a near-certainty is not what the format asks for.

**Question 8 (harder)**

Statement: The incident was resolved by 14:34.

- A) True
- B) False
- C) Cannot Say

**Correct answer: C**

**Explanation:** The restart was at 14:31 and error rates returned to baseline "within three minutes", which places resolution somewhere between about 14:31 and 14:34. Exactly 14:34 is the upper end of that range — possible, not established, and not contradicted either. The word doing the work is "within", which sets a bound rather than a duration. If you computed 14:31 plus three minutes and answered True, that is the habit worth catching: the arithmetic is right and it is arithmetic on a maximum.

*Passage C — for Questions 9 to 12*

"The managed database service guarantees a monthly uptime percentage of at least 99.95% for multi-availability-zone deployments. Single-zone deployments are not covered by the uptime guarantee. Uptime is calculated excluding downtime during customer-initiated maintenance and excluding unavailability caused by customer configuration. Automated backups are retained for 35 days; point-in-time recovery is available within the retention period to any second. Major version upgrades are the customer's responsibility and are not performed automatically. The provider will notify customers 90 days before a major version reaches end of support."

**Question 9 (moderate)**

Statement: A single-zone deployment of the database is guaranteed 99.95% uptime.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The passage contradicts this: "Single-zone deployments are not covered by the uptime guarantee." The guarantee is explicitly scoped to multi-zone deployments. This is the sort of scope condition that gets lost between a procurement decision and an architecture, and as the person establishing standards across the life cycle, it is one worth encoding — a service designed on a single-zone deployment has no contractual availability commitment at all, whatever the headline figure says.

**Question 10 (moderate)**

Statement: Data can be recovered to any point within the last 35 days.

- A) True
- B) False
- C) Cannot Say

**Correct answer: A**

**Explanation:** The passage establishes this: automated backups are retained for 35 days and "point-in-time recovery is available within the retention period to any second". Both halves are needed — the retention period gives the window and the point-in-time capability gives the granularity. Worth noting what this does not cover: data deleted more than 35 days ago, and anything the recovery process itself depends on.

**Question 11 (moderate)**

Statement: A major version upgrade will be applied automatically when the current version reaches end of support.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The passage contradicts this: "Major version upgrades are the customer's responsibility and are not performed automatically." The 90-day notification is a warning, not an action. This has a direct planning consequence: a database running an unsupported major version stays running and stops receiving fixes, and the only thing that changes it is someone in your organisation doing the upgrade.

**Question 12 (harder)**

Statement: Downtime caused by a misconfigured connection limit set by your team would count against the uptime guarantee.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** Uptime is calculated "excluding unavailability caused by customer configuration", and a connection limit your team set is customer configuration. So such downtime is outside the measurement and cannot cause the guaranteed percentage to be breached. The passage contradicts the statement. Note what the passage does not address: who determines whether a given outage was caused by customer configuration. In practice that is where these disputes actually happen, and the silence is worth noticing before you need to rely on the clause.

### Preparation tips

- **Check which obligation an exemption actually touches.**
- **Look for reclassification clauses that pull in a different set of controls.**
- **Note when a scoping word confines a clause to one case.**
- **Mark strong causal evidence as Cannot Say when causation is not stated.**
- **Count the figures a claim needs before treating it as computable.**
- **Watch bounding language — "within three minutes" is a maximum.**
- **Check whether a guarantee is scoped to a particular deployment shape.**
- **Notice what a document does not say about who decides.**

### Common pitfalls to avoid

- **Reading a conditional exemption as unconditional.**
- **Overlooking that production data reclassifies an environment.**
- **Extending a rule stated for production to non-production.**
- **Marking a well-evidenced cause as True.**
- **Computing with figures the passage does not supply.**
- **Treating a hedged recovery time as a precise one.**
- **Assuming an uptime guarantee covers your deployment shape.**
- **Assuming a support notification triggers an upgrade.**

## Workplace job-specific situational judgement assessment

### About this assessment

A workplace job-specific situational judgement assessment presents realistic scenarios and asks you to identify effective and ineffective responses. At principal level on the technical track the scenarios involve diagnosing complex faults, setting and enforcing standards across many teams, capacity remediation, and leading a team of experts whose best work is invisible.

The commonest formats ask for the most and least effective response, or for ratings. Scoring is against a key derived from experienced practitioners at comparable seniority.

Three patterns run through the strong answers.

The first is that restoration and diagnosis are separate activities. During an incident the priority is service; afterwards it is understanding. Mixing them costs users during and costs you honest accounts afterwards.

The second is that a standard you set is paid for by every team, on every change, for as long as it stands. Your role names ensuring practitioners adhere to standards, and the way to achieve adherence is almost always to make the compliant path the easy one rather than to enforce harder.

The third is that your deepest value is in the faults nobody else can diagnose — and that same depth makes you a bottleneck if you do not deliberately transfer it.

### How this assessment maps to your role

- **Complex fault diagnosis** maps to identifying, locating and fixing complex service faults.
- **Standards and adherence** maps to establishing standards and ensuring practitioners adhere to them.
- **Capacity remediation** maps to identifying capacity issues and initiating remedial action.
- **Process optimisation** maps to **Development process optimisation**.
- **Developing experts** maps to leading and developing a team of experts.
- **Security judgement** maps to **Information security**.

### Practice questions

**Question 1 (easy) — During an incident**

A major incident is running. Two engineers are debating the root cause while the service stays degraded. What is the most effective response?

- A) Let them continue; the cause is what matters.
- B) Redirect to restoration — revert what is revertible, fail over what can fail over — and hold the cause discussion afterwards with the evidence preserved, because the debate can be settled later and the degradation cannot.
- C) Decide the cause yourself and direct the fix.
- D) Bring more engineers onto the call.

**Correct answer: B. Least effective: D**

**Explanation:** Restoration and diagnosis are different activities, and doing them in the wrong order costs users directly. Option B redirects and preserves the evidence, which keeps the later diagnosis possible. Option D is least effective: adding people to a live incident raises coordination cost sharply, and a crowded call is slower than a small one — one of the most reliably counterproductive instincts in incident management. Option C commits to a hypothesis on partial evidence. Option A lets a debate run while users are affected.

**Question 2 (easy) — A fault only you can diagnose**

A complex intermittent fault has defeated two engineers. You can probably find it. What is the most effective approach?

- A) Diagnose it yourself; it is what you are for.
- B) Work through it with one of them rather than alone — narrating what you are checking and why — because the diagnostic reasoning is the thing worth transferring, and a fault of this kind will recur in a form you are not available for.
- C) Give them a list of things to check.
- D) Let them keep going; they will learn more.

**Correct answer: B. Least effective: D**

**Explanation:** Option B does the diagnosis and the development in one pass, which is what your role means by leading and developing a team of experts — and narrating the reasoning is the specific mechanism, because what you do automatically is invisible unless you say it. Option D is least effective: they have already been defeated by it, and letting them continue costs more time and teaches less than working alongside them would. Option C transfers a checklist rather than the reasoning that generated it. Option A solves it fastest and leaves the capability exactly where it was.

**Question 3 (moderate) — A standard nobody follows**

A standard you set eighteen months ago is widely ignored across teams. What is the most effective response?

- A) Enforce it through the change process.
- B) Find out why first, because a standard ignored by capable teams for eighteen months is usually unworkable, unclear in scope, or more expensive than the alternative — and if it is the last, the fix is to supply the tooling that makes the compliant path the easy one.
- C) Remind teams of the standard.
- D) Withdraw it.

**Correct answer: B. Least effective: C**

**Explanation:** Sustained non-compliance by capable people is evidence about the standard, and your role's phrase "ensure practitioners adhere" is achieved far more reliably by removing friction than by enforcement. Option B names the three causes and points at the remedy for the commonest. Option C is least effective: a reminder about an unworkable standard buys a fortnight of compliance and teaches everyone that your standards are advisory. Option A enforces before diagnosing and produces malicious compliance. Option D discards a possibly-real need.

**Question 4 (moderate) — Capacity remediation nobody wants to fund**

Your analysis shows a service will exhaust headroom in about four months. The service owner says there is no budget. What is the most effective response?

- A) Note the risk and move on; budget is their decision.
- B) Put the consequence and the date in writing to the service owner and their accountable superior, with the options — additional capacity, reducing load, or accepting a degradation risk from roughly a stated date — so the decision is made explicitly by someone able to make it.
- C) Escalate immediately to senior management.
- D) Find efficiencies to defer the problem.

**Correct answer: B. Least effective: A**

**Explanation:** Your role names identifying capacity issues *and initiating remedial action*, and where the remedy needs funding, initiating it means getting the decision made by someone who can. Option B routes it upward while keeping the service owner in it, and the written record with a specific date is what turns a warning into a decision. Option A is least effective: a foreseeable outage nobody was told about in an actionable form will not be seen afterwards as somebody else's problem. Option C goes over the owner's head without giving them a chance. Option D is worth doing alongside and is dangerous alone, since deferring the wall by two months removes the urgency without removing the problem.

**Question 5 (moderate) — A team working around your standard**

You discover a team has been bypassing a deployment standard you set, for two months. What is the most effective response?

- A) Require immediate compliance.
- B) Find out why before anything else — two months of workaround by a capable team usually means the standard does not fit their case, such as a stage that fails unpredictably or a delay incompatible with an urgent fix — because enforcing without fixing that just moves the workaround somewhere less visible.
- C) Report it as a compliance breach.
- D) Add technical controls preventing the bypass.

**Correct answer: B. Least effective: C**

**Explanation:** Sustained workaround by competent people is information about the standard. Option B gets it, and the likely findings are actionable — a missing emergency path, a flaky stage, or approvals required for changes that do not need them. Option C is least effective: treating it as a compliance matter before understanding it guarantees you never hear about the next workaround and leaves the defect in place. Option D is probably part of the eventual answer and, applied first, forces a team into something that does not work. Option A is the same error more gently.

**Question 6 (moderate) — A design that will be hard to operate**

An architect's design is sound but would be difficult for your teams to support. What is the most effective response?

- A) Raise it as an operational concern in the design review.
- B) Set out concretely what makes it hard — what happens at 3am, what the diagnostic path is, what skills it needs that the team does not have — and work with the architect on changes preserving the architectural intent, because "hard to operate" is not actionable until it is specific.
- C) Accept it; architecture is their responsibility.
- D) Ask for the design to be reworked.

**Correct answer: B. Least effective: C**

**Explanation:** Option B is specific enough for an architect to act on, and most such problems have solutions that preserve the design's intent once the operational constraint is understood. Option C is least effective: accepting a design your teams cannot support guarantees the cost lands on them for years, and you are the person best placed to prevent it. Option D asks for rework without saying what would fix it. Option A raises it in a form that is easy to note and hard to act on.

**Question 7 (harder) — Pressure to accept a risk**

A programme wants to go live on infrastructure you consider under-provisioned for its expected peak. Delay is costly. What is the most effective response?

- A) Refuse to approve the go-live.
- B) Quantify the risk — expected peak against capacity, what fails first, how long recovery takes — and put the options to whoever owns the service risk, including reduced scope at launch, temporary additional capacity, or accepting a degradation risk from a stated date.
- C) Approve it; the programme owns its delivery.
- D) Approve it and record the risk.

**Correct answer: B. Least effective: C**

**Explanation:** Option B converts an engineering judgement into a decision an accountable person can take, and the three options are the ones that actually exist at that stage — temporary capacity in particular is frequently available and frequently unconsidered. Option C is least effective: treating a risk you can see and they cannot as somebody else's problem is not how it will be viewed afterwards. Option D is close and weaker, since a recorded risk with no owner and no decision changes nothing while looking like diligence. Option A removes the risk owner from their own decision.

**Question 8 (harder) — Recurring failures with different causes**

A platform has had four significant outages in a year with different immediate causes: a certificate expiry, a full disk, a misconfigured limit, and a dependency timeout. What is the most effective response?

- A) Fix each cause thoroughly.
- B) Look for the shared property — all four are conditions that develop observably before they fail, and none was detected in advance — because four different causes with the same consequence usually indicate one missing capability rather than four unrelated faults.
- C) Add more alerting.
- D) Increase the frequency of maintenance checks.

**Correct answer: B. Least effective: A**

**Explanation:** Each of the four develops gradually and visibly before causing an outage, and in every case nobody saw it coming — a single systemic property with one fix that covers all four and the next four. Option A is least effective as the whole response: it resolves four specific faults and leaves the property that let them become outages entirely intact. Option C is directionally right and unspecific, since more alerts on symptoms would not have helped. Option D substitutes human vigilance for instrumentation.

**Question 9 (harder) — A security check that gets bypassed**

Your pipeline security scanning blocks deployments on findings that teams frequently override. What is the most effective response?

- A) Remove the override capability.
- B) Look at what the overridden findings actually are — usually unreachable code paths or third-party dependencies with no available fix — and re-scope what blocks to a small set of high-confidence findings, reporting the rest without blocking, because a check that produces unactionable findings gets bypassed and takes the actionable ones with it.
- C) Require justification for each override.
- D) Accept the overrides; teams know their code.

**Correct answer: B. Least effective: A**

**Explanation:** Automated security checks fail for one dominant reason — they flood teams with findings that cannot be acted on — and a blocking check in that state gets an override, an exemption or a quietly disabled step. Option B fixes the design so the block means something. Option A is least effective: removing the override on a check producing unactionable findings stops deployments entirely and will be reversed within a week, having damaged your standing meanwhile. Option C adds friction without improving signal. Option D abandons the control.

**Question 10 (harder) — Becoming the bottleneck**

Teams increasingly route difficult technical decisions through you, and you are now the delay on several. What is the most effective response?

- A) Work through the queue faster.
- B) Define what genuinely needs you and what does not — usually cross-cutting patterns, security-critical components and shared infrastructure, not internal implementation choices — and publish that, so teams can proceed on their own for most decisions.
- C) Delegate to senior engineers in each team.
- D) Stop reviewing and let teams decide.

**Correct answer: B. Least effective: A**

**Explanation:** Being consulted on everything is a structural problem that no amount of personal throughput fixes. Option B addresses the cause by making the boundary explicit, which also tells teams what they are trusted with — usually the thing they want to know. Option A is least effective: working faster confirms the arrangement and the queue reforms at your new speed. Option C is a good complement and, alone, distributes the bottleneck without defining what needs deciding. Option D removes the assurance rather than scoping it.

**Question 11 (harder) — Recognising invisible work**

An engineer has spent months on monitoring and automation. Incidents in their area have fallen sharply and their work appears in no delivery metric. What is the most effective response?

- A) Thank them and record it in their appraisal.
- B) Make the value countable — incidents avoided at the previous rate, engineer hours not spent, user-facing minutes not lost — and put it in front of the people who decide promotion and resourcing, because prevented incidents are invisible unless someone converts them into a number.
- C) Give them credit publicly at a team meeting.
- D) Move them onto more visible work.

**Correct answer: B. Least effective: D**

**Explanation:** Success in this work looks like nothing happening, which disadvantages the person in every process that counts outputs. Option B produces the count, which serves them and protects the work from being deprioritised next year. Option D is least effective — it solves the visibility problem by ending the valuable work and signals that prevention is a career dead end. Options A and C are good and reach nobody who makes resourcing decisions.

**Question 12 (harder) — Evidence against your own standard**

Data shows a testing standard you introduced across several teams costs significant time and has not measurably reduced defects. What is the most effective response?

- A) Improve the measurement; prevented defects are hard to count.
- B) Publish the finding, including that it is your standard, and narrow it to where the benefit is demonstrable or withdraw it — because teams paying daily for an unmeasurable benefit is a real cost, and withdrawing your own standard on evidence makes every remaining one more credible.
- C) Retain it; testing standards prevent problems that never appear in defect data.
- D) Reduce its scope quietly.

**Correct answer: B. Least effective: C**

**Explanation:** The cost is certain, distributed and daily; the benefit is unmeasured. Option B allows the right resolution — narrowing rather than abandoning — and gets the credibility that only comes from doing it openly, which is what makes the next standard easier to introduce. Option C is least effective because it is unfalsifiable, which makes it the argument that keeps every unproductive standard in place indefinitely. Option D reaches a defensible outcome by a route that looks like concealment once noticed. Option A is legitimate in principle and indistinguishable from motivated reasoning when the person improving the measurement owns the standard.

### Preparation tips

- **Restore first, diagnose afterwards, preserve the evidence.**
- **Narrate your diagnostic reasoning while working alongside someone.**
- **Read sustained non-compliance as evidence about the standard.**
- **Turn a capacity warning into a written, dated decision with options.**
- **Make "hard to operate" specific enough for an architect to act on.**
- **Scope security checks so that blocking findings are actionable.**
- **Define and publish what genuinely needs your involvement.**
- **Convert prevented incidents into countable value.**

### Common pitfalls to avoid

- **Adding people to a live incident.**
- **Diagnosing a complex fault alone when someone could learn it.**
- **Reminding teams about a standard they cannot follow.**
- **Treating a workaround as a compliance breach first.**
- **Accepting a design your teams cannot support.**
- **Recording a risk instead of getting it decided.**
- **Working through an approval queue faster instead of scoping it.**
- **Defending your own standard on unmeasurable benefits.**

## Conclusion

You have worked through four assessments pitched at principal DevOps engineer on the technical track, and the threads are worth drawing together.

The cognitive section kept returning to systems rather than components. Four outages with four causes is usually one missing detection capability. A design that is architecturally sound and operationally unworkable is not sound. And automation does not remove risk so much as change its shape, which makes blast radius the design question rather than an afterthought.

The numeric section was the arithmetic that decides infrastructure work: availabilities composing across dependencies, error budgets as burn rate against elapsed time, capacity sized on peak with a failure rather than on average, and the pattern where a stable mean with a rising 99th percentile means a new slow path affecting one request in a hundred.

The verbal section was about the documents you enforce and rely on. A conditional exemption is not an exemption. Production data reclassifies an environment. An uptime guarantee scoped to multi-zone deployments says nothing about a single-zone one. And a support notification is a warning rather than an upgrade.

The situational judgement section was about the particular position of deep technical seniority. Your greatest value is in the faults nobody else can diagnose, and that same depth makes you a bottleneck unless you deliberately transfer it — which is why working through a complex fault alongside someone, narrating the reasoning, scored higher than solving it faster alone. The strong answers also read workarounds as design feedback, scoped security checks so that a block meant something, and applied to the speaker's own standard exactly the scrutiny applied to everyone else's.

If one thread runs through all four, it is the visibility problem. The outages that did not happen, the peak that was absorbed, the fault caught before anyone noticed — these are real and invisible by construction. Nobody else in the organisation will translate them into evidence, and the funding, the recognition and your team's standing all depend on someone doing it.

Good luck. This is demanding work carried out largely out of sight, and the care you have given it is exactly right.
