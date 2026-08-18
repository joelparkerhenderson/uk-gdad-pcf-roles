# Lead Application Operations Engineer - Psychometric Assessment Resources

## Introduction

Welcome! This guide has been created for you as a lead application operations engineer working within the UK Government Digital and Data profession. At your level, the role changes shape: you define the application strategy and the strategy for security administration, you liaise with other leads across IT operations on how applications are performing and what changes need to be put in place, and you remain close enough to delivery to manage and maintain aspects of an application when a project's complexity and business impact warrant it. You lead incident investigations rather than merely participating in them; you manage high-impact, complex changes rather than routine ones; you set standards rather than only following them; and you develop the engineers around you. Whether you are preparing for an internal assessment, a promotion board, a move into a new department, or simply benchmarking yourself against the capability framework, this document will help you practise deliberately and reflect honestly.

Psychometric assessments are structured, standardised exercises measuring the cognitive capabilities and professional judgement that predict success in a role. For a lead application operations engineer, the relevant assessments are emphatically job-specific: they use the artefacts you genuinely handle — release policies, incident command timelines, capacity and availability reports spanning multiple services, security standards, test strategies, cross-team change schedules — and the decisions you genuinely make, such as arbitrating between conflicting priorities across teams, judging when a complex change is safe to approve, deciding what an incident review should conclude, and choosing how to develop a struggling engineer.

Why do these assessments matter at your level in particular? Because leadership in operations is applied judgement at scale. Every dimension the four assessments measure — pattern recognition across noisy data, precise deduction from policy, numerical fluency with service data, exact reading of dense documents, and situational judgement under competing pressures — is a dimension of decisions whose consequences now extend beyond your own work to your team's delivery, your peers' services, and your organisation's users. Practising them sharpens the instrument your role actually runs on.

This document is organised into four main assessment sections, each following the same pattern: an overview of what the assessment measures and its typical format, a mapping of its dimensions to the named skills in your role summary, a substantial set of practice questions with full worked explanations, practical preparation tips, and common pitfalls to avoid. The scenarios feature the textures of lead-level work: cross-team dependencies, strategy trade-offs, governance, mentoring, and ambiguity.

Here is how to get the most from it. Attempt each question honestly and commit to an answer before reading the explanation — leads are particularly prone to reading solutions with hindsight-flavoured agreement. Treat every explanation as a mini-lesson in technique, and notice where a question's reasoning mirrors a live decision on your desk this month. Finally, consider using parts of this guide with your team: several of the scenarios make excellent discussion material for developing the judgement of the engineers you lead.

Take your time, and enjoy the practice. Let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive assessment measures the mental processes your role demands, using practical scenarios rather than abstract puzzles. For a lead application operations engineer it presents the materials of your working day — multi-service dashboards, release calendars, security standards, incident timelines, cross-team dependency maps — and asks you to reason about them quickly and accurately: recognising patterns, deducing consequences from rules and policies, checking artefacts for inconsistency, prioritising under competing demands, and solving problems with several interacting constraints.

The typical format is an online, timed test lasting 15 to 30 minutes with 20 to 30 questions of graduated difficulty. Scoring is objective against a norm group; adaptive platforms adjust difficulty to your performance, and employers typically receive a speed-versus-accuracy profile rather than a single figure. For senior and lead candidates, norm groups are often more demanding, and questions lean toward multi-step reasoning: not "which entry breaks the pattern?" but "which combination of facts breaks which rule, and what follows?"

For your role, cognitive assessment is particularly relevant because your leadership decisions are structured reasoning with organisational consequences. Defining an application strategy means deducing where current trajectories lead and which interventions change them. Managing high-impact, complex changes means holding a dependency graph, a risk register, and a calendar in mind simultaneously. Leading incident investigation means running hypothesis elimination while directing others and communicating upward. Setting standards for the definition, security and integrity of objects means detecting precisely the inconsistencies that standards exist to prevent. A well-designed cognitive assessment samples these demands in miniature — and at lead level, your accuracy is inherited by everyone who acts on your conclusions.

### How this assessment maps to your role

- **Pattern recognition** maps to **Problem management** and **Ownership and topic**: initiating investigations into patterns and trends, and being proactive in searching for potential problems, both mean seeing structure in operational noise before it becomes an outage — the proactive half of your accountability.
- **Logical deduction** maps to **Change management** and **Service management framework knowledge**: managing high-impact, complex change requests and ensuring release policies are applied requires deducing exactly what a policy permits, forbids, and implies — the ITIL life cycle knowledge your role requires is itself a system of definitions to reason from.
- **Error checking** maps to **Asset and configuration management** and **Technical specialism**: maintaining secure configuration and accurate information, and setting standards for the definition, security and integrity of objects, both come down to detecting the record, procedure, or artefact that contradicts the standard or reality.
- **Prioritisation** maps to **Incident management** and **Availability and capacity management**: leading the investigation and resolution of incidents while managing service components against business needs and KPIs demands rapid, defensible ranking across your own and others' demands.
- **Applied problem solving** maps to **Service focus** and **Testing**: establishing coherent frameworks that work, and managing the planning of system and acceptance tests across functional and non-functional specifications, are constraint-satisfaction problems at the scale of processes and programmes.

### Practice questions

**Question 1 (easy) — Pattern recognition across service dashboards**

You review the weekly error-rate summary (errors per 10,000 requests) for the four applications in your portfolio over four weeks:

| Application | W1 | W2 | W3 | W4 |
|---|---|---|---|---|
| Case Tracker | 3 | 3 | 4 | 3 |
| Document Store | 5 | 5 | 5 | 5 |
| Licensing | 2 | 4 | 8 | 16 |
| Notifications | 7 | 6 | 7 | 6 |

Which application most warrants proactive investigation, and why?

- A) Notifications — it has the highest average error rate.
- B) Licensing — its error rate is doubling weekly, a compounding trend that will dominate within weeks.
- C) Document Store — a perfectly flat rate suggests the monitoring is broken.
- D) Case Tracker — any variation deserves investigation.

**Correct answer: B**

**Explanation:** Distinguish level from trajectory. Notifications runs the highest level (average 6.5) but is stable — worth scheduled attention, not urgency. Licensing runs the lowest starting level but shows geometric growth: 2, 4, 8, 16 doubles weekly; extrapolated, week 6 reaches 64 and week 8 reaches 256, overtaking everything in the portfolio. Trajectory outranks level when the trajectory compounds. Option C's suspicion is worth a passing check — flat metrics can indicate a stuck collector — but a stable 5 across four weeks is unremarkable for a mature service, and elevating that hunch above a doubling error rate inverts the evidence. Option D dissolves prioritisation entirely. This is your **Ownership and topic** skill's proactive clause in miniature: leads are accountable for spotting the compounding curve while it is still small, because by the time it is large, it is an incident with your name on the review.

**Question 2 (easy) — Deduction from a release policy**

Your release policy states: "High-impact changes require both CAB approval and a named rollback owner. Changes touching security infrastructure additionally require sign-off from the security administration lead. No change may have the same person as implementer and rollback owner." A proposed change is high-impact and touches security infrastructure; Priya is listed as implementer and rollback owner, and CAB approval is recorded. Which conditions remain unsatisfied?

- A) CAB approval only.
- B) Security sign-off only.
- C) Security sign-off, plus the rollback owner must be someone other than Priya.
- D) None — the change is ready.

**Correct answer: C**

**Explanation:** Enumerate the policy's conditions for this change class and check each against the record. High-impact: CAB approval — recorded, satisfied; named rollback owner — named, but test the separation rule next. Security-touching: security administration lead sign-off — absent from the record, unsatisfied. Separation: implementer and rollback owner must differ — Priya holds both, violated. Two defects remain, exactly as option C states. The method matters more than the instance: policies are conjunctions of conditions, and the reliable technique is a checklist sweep, never a gestalt impression of "looks approved". Ensuring that release policies, procedures and processes are applied is your **Change management** skill verbatim — and the separation-of-duties clause you just enforced is a control your own security administration strategy would contain, because a person rolling back their own failed work is a person marking their own homework at the worst possible moment.

**Question 3 (easy) — Error checking against a security standard**

Your object security standard requires: (i) every database view exposing citizen data must be named with the prefix "sec_"; (ii) access to such views is granted to roles, never to individual accounts; (iii) every grant must have an expiry date. An audit extract shows four grants:

1. View sec_case_summary → role CASEWORK_READ, expires 2027-03-31
2. View sec_payments_detail → account j_donovan, expires 2027-01-31
3. View sec_referrals → role REFERRAL_READ, expires 2026-12-31
4. View case_notes_open (exposes citizen data) → role CASEWORK_READ, expires 2027-03-31

Which grants breach the standard?

- A) Grant 2 only
- B) Grants 2 and 4
- C) Grant 4 only
- D) Grants 2, 3 and 4

**Correct answer: B**

**Explanation:** Test each grant against all three rules. Grant 1: prefixed view, role-based, expiry present — clean. Grant 2: the view is properly prefixed and an expiry exists, but the grantee "j_donovan" is an individual account, breaching rule (ii). Grant 3: all three rules satisfied — an expiry in 2026 is still an expiry; nothing requires a distant date. Grant 4: role-based with expiry, but the view exposes citizen data without the "sec_" prefix, breaching rule (i) — and note the operational consequence: unprefixed views escape whatever automated tooling keys on the naming convention, which is why naming standards are security controls and not cosmetics. Two breaches: grants 2 and 4. Setting standards for the definition, security and integrity of objects — and ensuring conformity — is your **Technical specialism** skill, and conformity checking is precisely this: every object, every rule, no gestalt.

**Question 4 (moderate) — Prioritisation across a lead's morning**

It is 09:00 Monday. Five demands compete:

1. A severity 1 incident on the licensing application started 20 minutes ago; your senior engineer is leading it competently and has not requested help.
2. The IT operations leads' meeting at 10:00 needs your quarterly performance summary, not yet finalised.
3. A departmental security bulletin requires you to confirm by noon whether your applications use a newly vulnerable library.
4. A junior engineer is waiting for the 09:30 development conversation you have already postponed twice.
5. A peer lead has emailed asking to discuss a change conflict for next month's release calendar.

Which ordering of attention is most defensible?

- A) 1 (take over), 3, 2, 4, 5 — a severity 1 demands the lead in command
- B) 3, 1 (brief check-in), 2, 4, 5 — start the security confirmation, verify incident command is sound, finalise the summary, keep the development conversation, schedule the peer discussion
- C) 2, 3, 1, 4, 5 — the leads' meeting is soonest
- D) 3, 2, 5, 1, 4 — externally imposed deadlines first, people last

**Correct answer: B**

**Explanation:** The discriminating judgement is item 1. A lead's instinct to command every severity 1 is a trap: your senior engineer is leading competently and has not asked for help — taking over (option A) undermines their development, signals distrust, and adds no diagnostic value; but ignoring it wholly is also wrong, because accountability remains yours. The calibrated move is a brief check-in: confirm command is sound, offer escalation support, step back. Item 3 starts first because its noon deadline is external and hard, and the check may take unpredictable time across four applications — start the clock early, possibly delegating the inventory query while you handle other items. Item 2 fits before 10:00 once items 3 and 1 are in motion. Item 4 is the quiet leadership test: a twice-postponed development conversation cancelled a third time teaches the junior exactly how much they matter; option B keeps it. Item 5 is important and genuinely schedulable — next month's calendar tolerates an afternoon slot. Option C puts an internal meeting above a security deadline; option D deprioritises a live severity 1 below routine work and postpones the junior again. Lead-level prioritisation is delegation-aware: the question is never only "what matters most?" but "what needs *me*, and what needs me only to verify it is handled?"

**Question 5 (moderate) — Deduction in a cross-team incident**

A cross-cutting outage affects three services. You establish: (i) the shared authentication service was patched last night; (ii) Service A, which uses the shared authentication service, is down; (iii) Service B, which does not use it, is also down; (iv) Service C, which uses it, is healthy; (v) Services A and B — but not C — depend on the message queue cluster. Which hypothesis best fits all the evidence?

- A) The authentication patch broke dependent services.
- B) The message queue cluster is the common cause: it explains A and B being down and C being healthy.
- C) Two unrelated failures coincidentally began together.
- D) Service C is actually down but its monitoring is lying.

**Correct answer: B**

**Explanation:** Test each hypothesis for consistency with all five facts. The authentication patch (A) is the seductive answer — it is the thing that changed, and "what changed?" is usually the right first question — but it fails twice: Service B is down without using authentication, and Service C uses authentication yet is healthy. A cause must explain both the affected and the unaffected. The message queue hypothesis (B) fits perfectly: A and B share the queue dependency and are down; C lacks it and is healthy. Option C multiplies entities without need — coincidence is the hypothesis of last resort, adopted only when correlation genuinely fails. Option D rescues a broken hypothesis by impeaching the evidence; monitoring can lie, but you verify that claim rather than assume it to save a theory. Note the leadership dimension: in a cross-team incident, the patch hypothesis will be championed loudly by whoever distrusts last night's change, and part of leading the investigation — your **Incident management** skill — is steering the room from the most *recent* cause to the most *consistent* one, out loud, with the dependency facts on a whiteboard.

**Question 6 (moderate) — Error checking a test strategy**

A test manager submits an acceptance test plan for a major release. It states: (i) "Functional coverage: all 14 user-facing workflows will be tested." (ii) "Non-functional coverage: performance testing will confirm the service sustains 500 concurrent users." (iii) "The performance environment is provisioned at 40% of production capacity." (iv) "Performance results will be reported as production-ready without adjustment." Assuming statements (i)-(iii) are accurate, which statement creates the problem, and why?

- A) Statement (i) — fourteen workflows is too many to test.
- B) Statement (ii) — 500 concurrent users is an arbitrary target.
- C) Statement (iv) — results from a 40%-capacity environment cannot be reported as production-ready without scaling analysis or caveat.
- D) There is no problem; the plan is coherent.

**Correct answer: C**

**Explanation:** The defect is the inference leap between (iii) and (iv). Testing on 40% of production capacity is common and legitimate — full-scale environments are expensive — but results from it require extrapolation, stated assumptions, and caveats before they say anything about production behaviour, because performance rarely scales linearly: connection pools, cache sizes, and database contention all behave differently at scale. Statement (iv) launders environment-limited results into an unqualified production claim, which is exactly how a release passes testing and fails its first busy morning. Options A and B attack reasonable content: fourteen workflows is a countable, plausible scope, and 500 concurrent users is presented as the target the business set, not an arbitrary figure. Your **Testing** skill at lead level is precisely this review: managing the planning of system and acceptance tests, co-ordinating functional *and non-functional* specifications, and providing authoritative advice — here, the authoritative advice is "report the results with the scaling caveat, or provision a representative environment for the critical paths". Identifying this class of gap before sign-off is what separates test governance from test theatre.

**Question 7 (moderate) — Applying ITIL life cycle knowledge**

Your department is standing up a new citizen-facing application. Four pieces of work are proposed: (1) define the service's availability targets with the business; (2) design the monitoring and alerting for the service; (3) agree the process by which future changes to the service will be assessed; (4) run the service desk that handles its live incidents. In ITIL life cycle terms, which sequencing principle is soundest?

- A) All four belong to service operation and can proceed in parallel after go-live.
- B) Targets (1) belong to design-stage thinking and shape monitoring (2); change assessment (3) belongs to transition and must exist before go-live; incident handling (4) is operation — so 1 and 2 precede 3, which precedes live running of 4.
- C) The service desk (4) should be designed first, since incidents are inevitable.
- D) Change assessment (3) is only needed once the first change is requested.

**Correct answer: B**

**Explanation:** Map each item to its life cycle home and the dependencies follow. Availability targets are service design decisions made with the business — and they *drive* monitoring design, because you instrument what you have promised to measure: alerting thresholds derive from targets, not vice versa. So 1 shapes 2. Change assessment machinery belongs to service transition and must exist *before* go-live, because the first urgent post-launch fix will otherwise arrive with no assessment route — option D discovers this the expensive way, improvising governance during an incident. Incident handling is service operation, running once live. Option A collapses the life cycle into operations, which is precisely the anti-pattern the framework exists to prevent: services "stood up" without designed targets or transition controls become permanently reactive. Option C inverts priorities — a service desk answering calls about a service with no availability targets or monitoring cannot even say what "broken" means. Your **Service management framework knowledge** requires demonstrating life cycle understanding, and this is its practical form: knowing which decisions belong upstream so that operations inherits a manageable service rather than an accident in progress.

**Question 8 (moderate) — Pattern recognition in change outcomes**

Reviewing six months of change records across your portfolio, you find: changes implemented by the originating team alone have a 4% failure rate; changes involving two teams have a 9% failure rate; changes involving three or more teams have a 23% failure rate. Volumes are similar across the categories. Multi-team changes also show clustering of failures around handover steps. What is the most useful conclusion for your change strategy?

- A) Ban changes involving three or more teams.
- B) The data suggests co-ordination — particularly at handovers — is the dominant failure driver; strengthen multi-team change controls: mandatory joint planning, explicit handover criteria, and a single named co-ordinator for 3+ team changes.
- C) The multi-team failure rate is acceptable because such changes are inherently harder.
- D) Redistribute engineers so every change can be done by one team.

**Correct answer: B**

**Explanation:** The pattern is steep — 4%, 9%, 23% — and the clustering around handover steps localises the mechanism: it is not that multi-team work is uniformly harder, but that failures concentrate where responsibility transfers. A useful conclusion converts pattern into targeted intervention, which is option B: joint planning attacks assumption mismatches, explicit handover criteria attack the identified cluster, and a named co-ordinator attacks diffuse accountability. Option A amputates capability the organisation needs — some changes are irreducibly cross-team — and drives work into evasive re-labelling. Option C normalises the signal: "inherently harder" is where improvement goes to die, and a 5.75× failure multiplier is a process defect, not physics. Option D solves co-ordination by reorganising the org chart around it, an intervention whose cost dwarfs the problem and whose premise (every change single-team) is unachievable for shared platforms. This is your **Change management** skill at strategy altitude — managing high-impact complex changes includes noticing *which kinds* fail and engineering the process, and it is equally your **Problem management** pattern-and-trend duty applied to the change process itself.

**Question 9 (hard) — Multi-constraint release calendar arbitration**

Four teams need production windows in the same fortnight. Constraints: (i) the payments release (team P) must complete before the 15th for regulatory compliance; (ii) the infrastructure upgrade (team I) needs a full weekend and invalidates any release made in the 48 hours before it, because those releases would need re-certification on the upgraded platform; (iii) the casework release (team C) depends on the infrastructure upgrade being complete; (iv) the notifications release (team N) has no dependencies but its only available engineers are on training after the 10th; (v) weekends fall on the 6th-7th and 13th-14th. Which schedule satisfies all constraints?

- A) N on the 3rd, P on the 9th, I on the weekend of the 13th-14th, C on the 16th
- B) P on the 12th, I on the weekend of the 13th-14th, C on the 16th, N on the 17th
- C) N on the 3rd, I on the weekend of the 6th-7th, P on the 9th, C on the 11th
- D) I on the weekend of the 6th-7th, C on the 9th, P on the 14th, N on the 5th

**Correct answer: C**

**Explanation:** Encode the rules, then test every option against every rule. The hard constraints: P complete before the 15th; I occupies a full weekend (6th-7th or 13th-14th); any release in the 48 hours before I needs re-certification on the upgraded platform; C only after I; N by the 10th. Option B fails immediately: P on the 12th sits inside the 48-hour invalidation window before the 13th-14th upgrade, forcing re-certification of a regulatory release with no margin before the 15th. Option D also fails: N on the 5th falls within 48 hours of the 6th-7th upgrade and is invalidated, and P on the 14th leaves the regulatory deadline hostage to a weekend upgrade running alongside it. That leaves A and C, and both technically satisfy the letter of the constraints — in A (I on the 13th-14th), the invalidation window covers the 11th-12th, which P on the 9th escapes; in C, everything post-dates the upgrade. The discriminator is risk, not feasibility. Under option A, the payments release ships on the 9th certified against the *old* platform, and the platform is then upgraded beneath it on the 13th-14th — so regulatory-critical code runs on infrastructure it was never released against, with a single day's margin before the 15th if anyone demands re-certification. Under option C, the platform change happens *first* (6th-7th), so every subsequent release — including regulated payments on the 9th — is certified on the platform it will actually run on, with days of margin, and N on the 3rd safely clears both its training deadline and the 4th-5th invalidation window. When two schedules both pass the constraint checklist, the lead's job — liaising with peer leads on the changes that need to be put in place — is to choose the one that minimises certification risk and preserves margin around regulatory dates: option C. Constraint satisfaction gets you to feasible; risk-aware sequencing gets you to defensible, and defensible is what you present at the leads' meeting.

**Question 10 (hard) — Proactive problem detection from weak signals**

No incidents have been raised, but during a routine review you notice three weak signals about the document store: (a) nightly backup duration has grown from 2 to 5 hours over six months; (b) two "disk latency" warnings appeared last month, each self-clearing within minutes; (c) the storage array's firmware version appears on the supplier's "recommended upgrade" list, with release notes mentioning "improved handling of degraded disk conditions". What is the strongest reading of these signals together?

- A) Three unrelated observations; note them individually and move on.
- B) The signals cohere into a hypothesis: storage performance is degrading (backup growth, latency warnings) and the supplier's firmware note hints at known degraded-disk handling issues — investigate the array's health now, before this becomes an unplanned outage.
- C) The backup growth is the only real issue; schedule a backup redesign for next quarter.
- D) Wait for an actual incident to confirm the hypothesis, since acting on weak signals wastes resources.

**Correct answer: B**

**Explanation:** Individually, each signal has an innocent explanation: backups grow with data volume; transient latency happens; suppliers always recommend upgrades. The lead-level skill is *conjunction*: three independent weak signals pointing at the same subsystem multiply, not add. Backup duration growing 2.5× while data likely grew far less suggests throughput decline; self-clearing latency warnings are how failing disks and degraded RAID states introduce themselves; and firmware notes about "degraded disk conditions" tell you the supplier has seen this movie. The composite hypothesis — the array is quietly degrading — is testable cheaply now (health diagnostics, disk error counters, throughput benchmarks) and catastrophically expensive later (an array failure during business hours with 5-hour restore times... from backups whose own integrity depends on the same array's health). Option A refuses to synthesise. Option C treats a symptom as the disease. Option D inverts your role: **Ownership and topic** at lead level says *be proactive in searching for potential problems* — waiting for the confirming incident means waiting for the harm, and "the signals were all there" is the sentence every post-incident review dreads. Proactive investigation on converging weak evidence is not resource waste; it is the cheapest moment you will ever get to buy this particular outage back.

**Question 11 (hard) — Designing a coherent operational framework**

You inherit responsibility for a portfolio of five applications previously run by five separate teams, each with different practices: different severity definitions, different change categories, different on-call arrangements, and different monitoring tools. Leads across IT operations are asking for consistent reporting. You cannot change everything at once without destabilising delivery. Which sequencing establishes coherence most effectively?

- A) Mandate a single toolset first — shared tooling will force practice convergence naturally.
- B) Standardise the shared *language* first (one severity scale, one change taxonomy, mapped from each team's current terms), so reporting and cross-team comparison work immediately; then converge processes (on-call, change flow) team by team by risk priority; migrate tooling last, once practices are stable enough to encode.
- C) Let each team keep its practices but build a translation layer in the reporting spreadsheet.
- D) Converge everything simultaneously in a single quarter with a hard cutover date.

**Correct answer: B**

**Explanation:** Test each option against what "coherent frameworks that work" (**Service focus**) actually requires: comparability now, convergence over time, and no self-inflicted outages. Option B sequences by dependency and cost: a shared severity scale and change taxonomy are cheap to adopt (definitions and mappings, not retooling), unblock the leads' reporting need immediately, and — critically — create the common language that every later convergence conversation is conducted *in*. Process convergence follows, ordered by risk (unify on-call before monitoring dashboards, because inconsistent on-call is a 03:00 failure mode), each transition small enough to roll back. Tooling migrates last because tools encode practices: migrating tools before practices converge either forces five practice changes at once (option D's chaos, compressed) or configures the new tool five different ways, recreating the divergence at higher licence cost — which is also why option A's "tooling forces convergence" usually delivers convergence-by-outage. Option C makes divergence permanent and load-bearing: the translation spreadsheet becomes unowned critical infrastructure, and five teams' practices continue drifting beneath it. Note the deep pattern, which recurs from data modelling to constitutional design: standardise semantics before processes, processes before tools. That ordering is what makes the framework coherent rather than merely uniform.

**Question 12 (hard) — Strategy deduction under uncertainty**

You are drafting the application strategy for a case management application. Facts: (i) the supplier has committed support until 2031, with no commitment beyond; (ii) the department's digital strategy mandates cloud hosting for all services by 2029; (iii) the application's current version cannot run in cloud environments, but the supplier's next major version (available 2027) can; (iv) a full replacement procurement would take an estimated three years; (v) user satisfaction with current functionality is high. Which strategic conclusion follows most soundly?

- A) Begin replacement procurement now — supplier support beyond 2031 is uncertain.
- B) Do nothing until 2030 — support runs to 2031 and users are satisfied.
- C) Plan to adopt the supplier's cloud-capable version around 2027-2028, satisfying the 2029 cloud mandate within the supported product line; simultaneously set a decision point around 2027 for the post-2031 question, when the supplier's roadmap and the version upgrade's success will be visible — preserving the replacement option (three-year lead time) against a 2031 horizon.
- D) Seek an exemption from the cloud mandate — migration is disruptive and users are happy.

**Correct answer: C**

**Explanation:** Lay the timelines against each other. The 2029 cloud mandate is the nearer, harder constraint; the current version cannot meet it, but the 2027 cloud-capable version can, with a year's margin for a 2027-2028 upgrade — so the mandate is satisfiable *inside* the current product line, without discarding functionality users value (fact v). The 2031 support horizon is the second constraint, and here the three-year procurement lead time (iv) is the strategic arithmetic that matters: a replacement must *begin* by roughly 2028 to be safe if support truly ends in 2031 — so option C's 2027 decision point is not procrastination but option-preservation timed to the last responsible moment, when two currently-unknowable facts (the upgrade's success, the supplier's post-2031 intentions) will be known. Option A spends three years and a procurement's cost hedging a risk that fact (iii) suggests may resolve itself, while abandoning high user satisfaction prematurely. Option B is the mirror error: by 2030, the replacement option has already expired — 2030 plus three years overshoots 2031 — so "do nothing" quietly forecloses the fallback while feeling safe. Option D gambles the strategy on an exemption the department may refuse, and buys, at best, deferral of a migration the supplier's own roadmap is making inevitable. Defining the application strategy — your role's headline duty — is exactly this: sequencing commitments against constraint timelines so that every future decision is made at the moment of maximum information *while the alternatives are still alive*.

### Preparation tips

- **Practise conjunction, not just detection.** Leads are rarely shown one clean signal. Take three unrelated-looking observations from your own estate this week and ask what hypothesis would explain all of them. That synthesis habit is the hardest-to-fake cognitive skill at your level.
- **Sweep policies as checklists.** For deduction questions — and real approvals — enumerate every condition and mark each satisfied/unsatisfied/unknown. Gestalt approval is where separation-of-duties breaches hide.
- **Run timeline arithmetic on strategies.** For any strategic question, write the constraint dates and lead times on one line and look for the last responsible decision moment. Most strategy errors are timeline errors in disguise.
- **Rehearse delegation-aware prioritisation.** For each demand, ask "what needs me, and what needs me only to verify?" Practising this converts prioritisation questions from ranking puzzles into leadership questions — which is what lead-level assessments intend.
- **Use elimination with explicit facts.** In diagnosis questions, write the facts down and strike hypotheses that any fact contradicts — including the hypothesis everyone in the room would prefer.
- **Bank easy marks fast.** Lead-level tests still open with pattern and rule questions. Take them quickly and cleanly; hoard your minutes for the multi-constraint finale.

### Common pitfalls to avoid

- **Commanding what you should verify.** In prioritisation scenarios, taking over a competently-led incident is the seductive wrong answer. Accountability is exercised through verification and support, not seizure.
- **Preferring the recent cause to the consistent one.** "What changed last night?" is a great first question and a terrible final answer when the dependency facts contradict it.
- **Accepting feasible when defensible is available.** Two schedules can both satisfy the constraints; the one preserving certification integrity and regulatory margin is the answer. Look past the letter of the constraints to their purpose.
- **Normalising bad trends.** "Multi-team changes are inherently harder" and "backups just grow" are analysis-terminating clichés. Quantified patterns deserve mechanisms and interventions.
- **Standardising tools before semantics.** In framework questions, any option that leads with tooling or a big-bang cutover is almost always the decoy. Language, then process, then tools.
- **Closing strategic options while feeling prudent.** "Wait and see" answers can silently overrun a lead time and kill the fallback. Check every deferral against the longest procurement or migration clock in the question.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment measures how accurately and insightfully you work with the quantitative material a lead's decisions run on: portfolio-level availability and incident statistics, capacity and cost projections, change failure rates, test coverage figures, and user research data. Beyond calculating percentages, ratios, weighted averages, and rates of change, the lead-level emphasis falls on interpretation and decision: what does this trend commit us to, which of these two honest calculations should govern the decision, and what will this number cost or save?

The typical format is an online, timed test of 20 to 30 minutes with 15 to 20 data-based questions, calculators permitted. Adaptive difficulty and speed-accuracy profiling are standard. For senior and lead candidates, questions increasingly present *two or more* datasets to reconcile — a table and a target, a forecast and a lead time, a before and an after — because reconciling datasets is what leads actually do with numbers.

Why do employers use numeric assessments for this role? Because your numbers now travel. The performance summary you present at the IT operations leads' meeting shapes cross-team decisions; the capacity forecast you sign drives procurement; the change failure statistics you report calibrate the organisation's risk appetite; the KPI figures you publish are how the business knows whether its services work. Your role summary commits you to managing service components against business needs and KPIs, and to liaising with leads on how applications are performing — both are numerical acts performed in public. A lead whose arithmetic is reliable, whose baselines are honest, and whose forecasts include lead times becomes the person whose numbers end arguments; the alternative kind of lead starts them.

Every question below uses data of the kind your portfolio genuinely produces, and every explanation shows the arithmetic step by step — because at your level, showing the working is not just test technique, it is how you will defend the figure when a peer lead or a finance partner challenges it.

### How this assessment maps to your role

- **KPI and availability arithmetic** maps to **Availability and capacity management**: managing service components against business needs and KPIs means fluent conversion between availability percentages, downtime budgets, and user impact — across a portfolio, not just a service.
- **Trend analysis and forecasting** maps to **Ownership and topic** and **Technical specialism**: being proactive in searching for potential problems is often numerical — projecting when a trend crosses a threshold — and drafting procedures and standards includes the capacity assumptions inside them.
- **Change and release statistics** map to **Change management**: managing high-impact changes and ensuring release policies are applied both depend on failure rates, and on knowing what those rates do and do not prove.
- **Test metrics** map to **Testing**: managing test planning across functional and non-functional specifications requires reading pass rates, coverage percentages, and performance results — including spotting when a number is being asked to claim more than it can.
- **Incident and problem statistics** map to **Incident management** and **Problem management**: leading investigations and initiating trend analysis mean computing rates, comparing baselines, and verifying that remedies actually moved the numbers.
- **User data interpretation** maps to **User focus**: representing users internally is frequently done with numbers — satisfaction rates, task completion, adoption — and championing user research includes keeping those numbers honest.

### Practice questions

**Question 1 (easy) — Portfolio availability**

Your portfolio's four applications recorded these availability figures last month: 99.8%, 99.5%, 99.9%, and 98.8%. What was the simple average availability across the four applications?

- A) 99.5%
- B) 99.6%
- C) 99.4%
- D) 99.0%

**Correct answer: A**

**Explanation:** Step 1: sum the figures: 99.8 + 99.5 + 99.9 + 98.8 = 398.0. Step 2: divide by 4: 398.0 ÷ 4 = 99.5%. Sense-check: the values range from 98.8 to 99.9, and 99.5 sits within that range, closer to the cluster of high values — consistent. Note for your reporting practice what this average conceals: three healthy services and one (98.8%) that missed a typical 99.5% target by a wide margin. A portfolio average is a legitimate headline, but presented alone at the leads' meeting it would bury the one number requiring action. Lead-level numeracy is calculating correctly *and* choosing which figures must accompany the summary.

**Question 2 (easy) — Change failure rate comparison**

Last quarter your portfolio implemented 150 changes with 12 failures. The quarter before, it implemented 120 changes with 12 failures. What happened to the change failure rate?

- A) It stayed the same — 12 failures both quarters.
- B) It fell from 10% to 8%.
- C) It rose from 8% to 10%.
- D) It fell from 12% to 10%.

**Correct answer: B**

**Explanation:** Compute each quarter's rate. Earlier quarter: 12 ÷ 120 = 0.10 = 10%. Last quarter: 12 ÷ 150 = 0.08 = 8%. The rate fell from 10% to 8% — option B. Option A is the trap the question is built around: identical failure *counts* conceal different failure *rates* when volumes differ, and volume grew 25%. This distinction is politically live in change governance: a peer lead glancing at raw counts might claim "no improvement", while the rate shows the process absorbed a quarter more change at lower risk per change. As the lead who ensures release policies are applied, you are also the lead who ensures the improvement statistics are read correctly — rates for comparison, counts for workload.

**Question 3 (easy) — Downtime budget across services**

A shared platform underpins three of your applications. Its availability KPI is 99.95% over a 30-day month (24-hour service). To the nearest minute, what is its monthly downtime budget?

- A) About 216 minutes
- B) About 43 minutes
- C) About 22 minutes
- D) About 130 minutes

**Correct answer: C**

**Explanation:** Step 1: minutes in the month = 30 × 24 × 60 = 43,200. Step 2: permitted downtime fraction = 100% − 99.95% = 0.05% = 0.0005. Step 3: 43,200 × 0.0005 = 21.6 minutes ≈ 22 minutes. Option A is the 99.5% budget (0.5%), option B the 99.9% budget (0.1%) — decimal-place neighbours designed to punish haste. The operational meaning is sobering and worth internalising: a shared platform at 99.95% has a downtime budget shorter than most incident *response* times, which is why platforms underpinning multiple services carry tighter targets than the services themselves — one platform outage consumes three services' user trust simultaneously. When you liaise with peer leads about shared infrastructure, this is the number that frames every maintenance window negotiation.

**Question 4 (moderate) — Weighted portfolio incident rate**

Your four applications handled these volumes last month: Case Tracker 400,000 transactions with 32 incidents; Document Store 250,000 with 30 incidents; Licensing 100,000 with 18 incidents; Notifications 50,000 with 4 incidents. Which application has the highest incident rate per 100,000 transactions?

- A) Case Tracker
- B) Document Store
- C) Licensing
- D) Notifications

**Correct answer: C**

**Explanation:** Normalise each to incidents per 100,000 transactions. Case Tracker: 32 ÷ 4 = 8.0. Document Store: 30 ÷ 2.5 = 12.0. Licensing: 18 ÷ 1 = 18.0. Notifications: 4 ÷ 0.5 = 8.0. Licensing leads at 18 incidents per 100,000 — more than double Case Tracker's rate despite producing barely half its incident count. The trap is Case Tracker's raw 32, the biggest absolute number. Normalisation is the entire game in portfolio comparison: raw counts follow size; rates reveal reliability. This is where your **Problem management** trend work should point its effort — and note the compound insight available: Licensing was also the application with the doubling error rate in the cognitive section's Question 1. When two independent normalised metrics converge on the same service, the portfolio is telling you where its next major incident lives.

**Question 5 (moderate) — Cost of an availability improvement**

The business asks what it would take to move a service from 99.5% to 99.9% availability. Analysis shows the main driver is recovery time: the service suffers about 4 significant failures per year, and mean recovery currently runs 11 hours per failure. Assuming failure frequency is unchanged, what mean recovery time per failure would meet 99.9% over a 365-day year (24-hour service)?

- A) About 2.2 hours
- B) About 4.4 hours
- C) About 8.8 hours
- D) About 1.1 hours

**Correct answer: A**

**Explanation:** Step 1: annual hours = 365 × 24 = 8,760. Step 2: the 99.9% target permits 0.1% downtime = 8,760 × 0.001 = 8.76 hours per year. Step 3: spread across 4 failures: 8.76 ÷ 4 = 2.19 ≈ 2.2 hours mean recovery per failure. Current state check: 4 × 11 = 44 hours ≈ 99.5% (44 ÷ 8,760 = 0.50%), confirming the model matches the present figure. The strategic content is the ratio: the target demands recovery *five times faster* — 11 hours down to 2.2 — which is rarely achievable by "trying harder"; it implies architectural investment (automated failover, faster restore paths, warm standby). This is the arithmetic behind honest strategy conversations: when you define the application strategy, the difference between 99.5% and 99.9% is not one decimal place of ambition but a fivefold operational capability change with a budget attached. Leads who can show this working convert vague availability aspirations into fundable engineering decisions.

**Question 6 (moderate) — Test coverage reconciliation**

A release has 40 functional requirements. The test report states: 34 requirements fully covered by passing tests, 4 partially covered (some test conditions passing, some not yet run), 2 not covered. The delivery manager's slide says "95% test coverage". Which statement most accurately characterises the claim?

- A) Accurate: 38 of 40 requirements have some coverage, and 38 ÷ 40 = 95%.
- B) The 95% conflates full and partial coverage: only 85% of requirements (34 ÷ 40) are fully covered by passing tests, and the slide should say so — with the 4 partial and 2 uncovered requirements listed for the release decision.
- C) Inaccurate: coverage is 92.5%.
- D) The distinction does not matter if the covered requirements are the important ones.

**Correct answer: B**

**Explanation:** Reconstruct the 95%: 34 full + 4 partial = 38 requirements with *some* coverage; 38 ÷ 40 = 95% — so option A correctly explains where the number came from, but "some coverage" and the slide's implication of "tested" are different claims. Fully-covered-and-passing is 34 ÷ 40 = 85%. Option C's 92.5% (37 ÷ 40) has no derivation in the data. Option D smuggles in an untested assumption — nothing establishes which requirements matter most, and a release decision deserves the actual list. The governing principle, central to your **Testing** skill's authoritative-advice clause: a coverage percentage is only as honest as its definition, and release decisions should see the definition, the number, *and the named gaps*. "95% coverage" that includes partially-run test conditions is how untested code reaches production wearing a tested number. The lead's added value in test governance is often exactly this two-minute reconciliation performed before the slide leaves the building.

**Question 7 (moderate) — Capacity trend with seasonal spike**

A service's peak daily transaction volume has grown 3% per month (compounding) for the past year, currently standing at 200,000. Each January, renewals season adds a further 50% to that month's peak on top of the underlying trend. Tested capacity is 320,000 transactions per day. It is now the start of September (four months before January). What will the January peak be, and does capacity hold?

- A) About 225,000; capacity holds comfortably.
- B) About 337,000; capacity is exceeded — action is needed this autumn.
- C) About 300,000; capacity holds with a small margin.
- D) About 260,000; capacity holds.

**Correct answer: B**

**Explanation:** Two effects compound and both must be applied. Step 1: underlying growth from September to January is four months at 3% compounding: 200,000 × 1.03⁴. Compute 1.03⁴: 1.03² = 1.0609; 1.0609² ≈ 1.1255. So the January baseline ≈ 200,000 × 1.1255 = 225,100. Step 2: apply the seasonal multiplier: 225,100 × 1.5 ≈ 337,650. Step 3: compare with capacity: 337,650 > 320,000 — exceeded by roughly 5.5%. Option A stops after step 1 (trend without season); option D applies 30% instead of 50%; option C guesses between them. The answer is B, and the September timing is the point: you have four months to add capacity, optimise, or arrange demand management — ample if you start now, desperate if this arithmetic first gets done in December. This is **Availability and capacity management** as leads practise it: the KPI is protected in September spreadsheets, not in January war rooms. Note also the reporting obligation: the peer leads whose services share your infrastructure need this forecast at the next leads' meeting, not after procurement is already tight.

**Question 8 (moderate) — Problem remedy verification with a confounder**

A preventative measure for a recurring fault was deployed on 1 June. Monthly incident counts for the fault: March 60, April 64, May 62, June 30, July 28. However, you also know June and July are historically the service's quietest months, with transaction volumes about 25% below the March-May average. What is the soundest assessment of the remedy?

- A) The remedy roughly halved incidents — a clear success, case closed.
- B) Incidents fell about 53% while volume fell only 25%; even volume-adjusted, the incident *rate* fell substantially (roughly 38%), so the remedy shows real effect — but confirm after volumes recover in autumn before closing the problem record.
- C) The drop is entirely seasonal; the remedy did nothing.
- D) The data cannot say anything because two things changed at once.

**Correct answer: B**

**Explanation:** Quantify both effects instead of letting either narrative win. Raw incident fall: baseline (March-May average) = (60 + 64 + 62) ÷ 3 = 62; post-remedy average = (30 + 28) ÷ 2 = 29; fall = (62 − 29) ÷ 62 ≈ 53%. Volume fell 25%, so if incidents merely tracked volume, expect about 62 × 0.75 = 46.5 incidents — the observed 29 is far below that. Rate per unit volume: before = 62 (per normalised volume 1.0); after = 29 ÷ 0.75 ≈ 38.7; rate reduction = (62 − 38.7) ÷ 62 ≈ 38%. So a substantial volume-adjusted improvement remains — the remedy is working — but the honest caveat stands: seasonality could interact with the fault mechanism in ways a two-month window cannot exclude, so the problem record stays open pending an autumn data point. Option A ignores the confounder; option C ignores the arithmetic that survives it; option D surrenders to the confounder when normalisation partially defeats it. This is your **Problem management** verification duty performed to lead standard: adjust for what you can, quantify the residual effect, and schedule the confirming observation before declaring victory.

**Question 9 (hard) — Consolidation business case**

Two applications with overlapping functions cost, per year: App X £380,000 (hosting £120k, licences £90k, support effort £170k); App Y £240,000 (hosting £70k, licences £60k, support effort £110k). Consolidating onto App X would: eliminate App Y's hosting and licences entirely; migrate App Y's users at a one-off cost of £150,000; increase App X's support effort by 40% (absorbing App Y's workload); and take effect from the start of Year 1. What is the cumulative net saving by the end of Year 2?

- A) £year-by-year impossible to determine
- B) £110,000
- C) £194,000
- D) £344,000

**Correct answer: C**

**Explanation:** Build the annual saving first. Step 1: costs eliminated per year: App Y hosting £70k + licences £60k + support effort £110k = £240k. Step 2: new costs per year: App X support rises 40% of £170k = £68k. Step 3: net annual saving = £240k − £68k = £172k. Step 4: apply the one-off migration cost: Year 1 net = £172k − £150k = £22k; Year 2 net = £172k. Step 5: cumulative by end of Year 2 = £22k + £172k = £194k — option C. Option D (£344k) forgets the migration cost entirely; option B (£110k) double-counts by also removing App Y's support effort from the savings side while adding App X's uplift — the classic consolidation-case error, since App Y's support *effort* saving is real only to the extent the uplift on App X doesn't consume it, which is exactly what steps 1-3 net off correctly. This is application strategy — your headline duty — expressed in finance: consolidation cases live or die on support-effort assumptions (is 40% uplift realistic, or optimistic?), and the lead who can walk a finance partner through this arithmetic, sensitivity and all, is the lead whose strategy gets funded.

**Question 10 (hard) — Incident review statistics across teams**

Preparing for the leads' meeting, you compare two teams' incident resolution over the quarter. Team Alpha: 90 incidents, mean resolution 6.0 hours, median 2.0 hours. Team Beta: 90 incidents, mean resolution 4.5 hours, median 4.0 hours. A peer lead concludes: "Beta resolves incidents faster — Alpha should adopt Beta's practices." What do the numbers actually support?

- A) The peer lead is right: Beta's mean is lower, so Beta is faster.
- B) Alpha resolves the *typical* incident twice as fast (median 2.0 vs 4.0 hours); Alpha's higher mean indicates a tail of long-running incidents dragging the average — so the teams likely differ in incident mix or tail handling, and the actionable comparison is of their distributions and their worst cases, not their means.
- C) The teams are equivalent since both handled 90 incidents.
- D) Alpha is better on both measures.

**Correct answer: B**

**Explanation:** When mean and median disagree, the disagreement *is* the finding. Alpha: median 2.0 but mean 6.0 — a heavily right-skewed distribution: most incidents resolve fast, but a minority run very long (a mean three times the median implies a substantial tail; e.g. if 80 incidents took ~2 hours, the remaining 10 must average ~38 hours to produce a 6.0 mean). Beta: median 4.0, mean 4.5 — a compact distribution: consistently moderate, few extremes. So "Beta is faster" is true of means and false of typical experience; "Alpha is faster" is true of medians and false of tails. Neither headline supports wholesale practice adoption — the useful questions are *why Alpha's tail exists* (complex incidents? stalled escalations? one catastrophic outlier?) and whether Beta's consistency or Alpha's speed better fits each incident class. Option B alone reads the distribution. The lead-level lesson: at the leads' meeting, any comparison resting on a single summary statistic deserves the question "what does the median say?" — skew is where operational truth hides, and your **Incident management** leadership includes protecting cross-team comparisons from statistically confident nonsense.

**Question 11 (hard) — User research sampling judgement**

You are championing user research for a case management redesign. The application has 3,000 registered users: 2,400 caseworkers, 450 team leaders, 150 administrators. The research plan proposes interviewing 30 users recruited by open invitation, and the sign-up list so far is: 6 caseworkers, 14 team leaders, 10 administrators. What is the most important numerical observation about this sample?

- A) Thirty interviews is 1% of users — too few to learn anything.
- B) The sample inverts the population: caseworkers are 80% of users but 20% of the sample, while administrators are 5% of users but 33% of the sample — self-selection has skewed recruitment, and findings would systematically underweight the majority user group unless recruitment is rebalanced.
- C) The sample is fine because all three user types are represented.
- D) Interview more administrators, since their high sign-up rate shows they care most.

**Correct answer: B**

**Explanation:** Compare sample proportions with population proportions. Population: caseworkers 2,400 ÷ 3,000 = 80%; team leaders 450 ÷ 3,000 = 15%; administrators 150 ÷ 3,000 = 5%. Sample: caseworkers 6 ÷ 30 = 20%; team leaders 14 ÷ 30 ≈ 47%; administrators 10 ÷ 30 ≈ 33%. The sample nearly inverts the population — a classic self-selection artefact (open invitations recruit the engaged and the aggrieved, and administrators' high sign-up rate likely signals unmet needs worth hearing, but not license to let them speak *as* the user base). Option A misunderstands qualitative research: 30 well-chosen interviews can be richly informative — the issue is composition, not size. Option C settles for token representation. Option D doubles down on the bias, mistaking enthusiasm for representativeness. Option B states the finding and the fix: purposive rebalancing toward the population structure, perhaps with a deliberate administrator sub-study. This is your **User focus** skill with numbers attached — championing user research *to focus on all users* means exactly this check, and "explain the difference between user needs and the desires of the user" begins with knowing whose voice your sample is amplifying.

**Question 12 (hard) — KPI target negotiation**

The business wants a new KPI: "95% of severity 2 incidents resolved within 4 hours". Your last 200 severity 2 incidents show: 120 resolved within 2 hours, 40 more within 4 hours, 24 more within 8 hours, and 16 beyond 8 hours. Meeting the proposed target would require what change, and what is the honest negotiating position?

- A) Current performance is 80% within 4 hours (160 of 200); the target needs the 4-hour figure to rise by 15 percentage points, meaning 30 of the current 40 slower incidents must move inside 4 hours — describe the investment required, or negotiate the target toward current capability plus a funded improvement path.
- B) Current performance is 60% within 4 hours; the target is unreachable and should be refused.
- C) Current performance is 95% — accept the target; it is already met.
- D) Accept the target now and hope the tail incidents were one-offs.

**Correct answer: A**

**Explanation:** Establish the baseline first. Within 4 hours: 120 + 40 = 160 of 200 = 80%. (Option B's 60% counts only the 2-hour band; option C's 95% mistakenly includes the 8-hour band: 184 ÷ 200 = 92%, and even that is not 95%.) The target demands 95% of 200 = 190 incidents inside 4 hours — 30 more than today's 160, meaning three-quarters of the 40 incidents currently landing in the 4-to-8-hour-plus bands must accelerate. That is not a stretch goal; it is a capability change with candidates you can cost: faster escalation to specialists, out-of-hours cover, automated diagnostics, or re-architecting the components whose failures dominate the tail. Option A is the honest position: quantified baseline, quantified gap, and a choice offered to the business — fund the capability or set the target where capability is (say, 85% now, 95% in four quarters with investment). Option D signs a commitment the data says you will miss, spending your credibility on hope; agreeing to targets you cannot meet is not customer focus, it is deferred dishonesty. This is the negotiating arithmetic behind **Availability and capacity management**'s "meet business needs and KPIs" — the lead's job is ensuring the KPI is a contract both sides can honour, and the working shown above is the contract negotiation.

### Preparation tips

- **Normalise before comparing, always.** Counts follow size; rates reveal character. Whether it is incidents, failures, or costs, divide by the relevant volume before ranking anything — and expect assessment questions built to punish raw-count rankings.
- **Interrogate every summary statistic.** When given a mean, ask what the median would show; when given a percentage, ask for its definition and denominator. The lead-level questions hide their content in the gap between summaries.
- **Practise two-effect arithmetic.** Compounding growth plus seasonal multipliers, remedies plus confounders, savings plus one-off costs — real decisions stack effects, and so do the harder questions. Apply effects one at a time, in order, on paper.
- **Keep the conversion table in your head.** 99.5%, 99.9%, 99.95% monthly and annual downtime budgets; percentage-points versus relative change; per-100,000 normalisations. Fluency here buys time for the genuinely hard questions.
- **Rehearse the business-case skeleton.** Annual savings, annual new costs, net, then one-offs by year, then cumulative. Five steps, always in that order — it prevents the double-counting that sinks consolidation arithmetic.
- **Check answers against their story.** A recovery-time target five times tougher than today, a January peak above tested capacity, a sample inverting its population — the correct answer usually *means* something actionable. If your calculated answer implies nothing, recheck it.

### Common pitfalls to avoid

- **Ranking portfolios by raw counts.** The biggest application will almost always have the most incidents. Rate per transaction, per user, or per change is the comparison that means anything.
- **Reading identical counts as identical performance.** Twelve failures out of 120 and out of 150 are different risk levels. Volumes move; insist on rates.
- **Letting one summary statistic carry a cross-team comparison.** Means hide tails; medians hide means. When they disagree, the disagreement is the story — investigate before recommending.
- **Forgetting one-off costs and lead times.** Business cases without migration costs, and forecasts without procurement lead times, are systematically optimistic — in tests and in strategy papers alike.
- **Accepting a target without computing the gap.** "95% in 4 hours" sounds like ambition; against an 80% baseline it is a capability programme. Compute before committing.
- **Treating a confounded result as either proof or nothing.** Volume changes, seasonality, and simultaneous fixes can usually be partially adjusted for. Quantify what survives adjustment, state the residual uncertainty, and schedule the confirming measurement.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment measures how precisely you extract meaning, obligations, and implications from the dense written material a lead's role runs on: policies and standards, supplier contracts and notices, governance papers, incident reviews, and cross-team correspondence. The core format presents a passage followed by statements to classify as **True** (supported by the passage), **False** (contradicted by it), or **Cannot say** (the passage provides insufficient basis). Complementary formats test inference, best-summary selection, and clear-writing judgement.

The typical format is an online, timed test of 15 to 25 minutes with 20 to 30 statements across several passages. The governing discipline — answer from the passage alone — bears hardest on experienced leaders: you know how release policies, security standards, and framework definitions *usually* read, and the test deliberately includes texts that deviate from convention to detect whether you read the document or your memory of documents like it. This is not an artificial trap: the supplier's actual contract clause and your department's actual security standard are what bind you, and lead-level mistakes are disproportionately "I assumed it said what these things always say".

Why do employers use verbal reasoning assessments for this role? Because at lead level you are both a consumer and a producer of binding text. You interpret standards to settle cross-team disputes; you draft and maintain procedures and documentation that others must follow exactly; you write the incident reviews and strategy papers that become the organisation's memory of events and intentions. A misread clause at your level propagates through everyone who takes your interpretation on trust, and a vaguely drafted procedure fails at 03:00 in the hands of an engineer who cannot ask you what you meant. The assessment's two halves — precise reading, clear-writing judgement — are the two halves of that responsibility.

The passages below reflect your genuine document diet: a security administration standard, an inter-lead governance exchange, and a post-incident review with strategic implications. Read them as you would a clause you were about to enforce.

### How this assessment maps to your role

- **Precise reading of standards and policies** maps to **Technical specialism** and **Change management**: setting standards for the definition, security and integrity of objects — and ensuring conformity, and ensuring release policies are applied — requires clause-level accuracy about what a standard actually mandates versus what it merely recommends.
- **Inference discipline** maps to **Incident management** and **Problem management**: leading investigations means holding the line between what evidence states, what it implies, and what it fails to exclude — the true/false/cannot-say partition is that line, formalised.
- **Framework-definition comprehension** maps to **Service management framework knowledge**: ITIL life cycle and capability knowledge is a system of precise definitions; demonstrating it means reading and applying them exactly.
- **Reading stakeholder and user language** maps to **User focus**: representing users internally, and explaining the difference between user needs and user desires, both begin with exact comprehension of what users and stakeholders actually said — and did not say.
- **Clear-writing judgement** maps to **Technical specialism**'s drafting duty and **Ownership and topic**: procedures, reviews, and handovers succeed exactly insofar as they cannot be reasonably misread — and accountability includes accountability for what your documents caused readers to do.

### Practice questions

**Passage 1 — Security administration standard extract**

*"Privileged access to production applications must be granted only through the role-based access system, must be time-limited to a maximum of 90 days per grant, and must be re-certified by the application's lead engineer before renewal. Emergency ('break-glass') access may bypass the role-based system, but every use of break-glass credentials must be logged automatically, reviewed by the security administration lead within two working days, and reported quarterly to the service governance board. Break-glass credentials must be rotated within 24 hours of each use. Where an application cannot technically support time-limited grants, a documented exception must be approved by the security administration lead and reviewed every six months; applications operating under such exceptions must not process citizen data."*

**Question 1 (easy) — True, false, or cannot say**

Statement: "A privileged access grant may last up to six months before renewal."

- A) True
- B) False
- C) Cannot say
- D) True, where an exception is documented

**Correct answer: B**

**Explanation:** The standard sets the maximum grant at 90 days — roughly three months — so "up to six months" contradicts it: False. Option D tries to rescue the statement via the exceptions clause, but read what that clause actually excepts: it covers applications that *cannot technically support time-limited grants* — a different situation from extending a grant's duration — and even there, it imposes six-*monthly review of the exception*, not six-month grants. The six-month figure in the passage belongs to exception reviews, and the statement's author has transplanted it onto grant duration. Numbers migrating between clauses is the signature verbal-reasoning trap at every level, and in security standards it is also the signature audit finding: always trace a duration, threshold, or figure back to the clause that owns it before acting on it — or approving someone else's action on it.

**Question 2 (easy) — True, false, or cannot say**

Statement: "Every use of break-glass credentials must be reviewed by the service governance board within two working days."

- A) True
- B) False
- C) Cannot say
- D) True, but only quarterly

**Correct answer: B**

**Explanation:** The passage assigns two different obligations to two different bodies on two different clocks: review of each break-glass use falls to *the security administration lead* within two working days, while *the service governance board* receives *quarterly reporting*. The statement splices the board into the lead's two-day review duty — contradicted on both actor and cadence: False. Option D compounds the splice rather than fixing it. Governance text is dense with exactly this structure — multiple actors, multiple obligations, multiple clocks — and the reliable reading technique is to build a small mental (or margin-scribbled) table: who / must do what / by when. As the person who defines the security administration strategy, you will also *write* clauses like these; the actor-obligation-deadline discipline you apply as a reader is the same one that keeps your drafting enforceable.

**Question 3 (moderate) — True, false, or cannot say**

Statement: "An application that cannot technically support time-limited grants may continue to process citizen data provided the exception is approved and reviewed."

- A) True
- B) False
- C) Cannot say
- D) True, if the security administration lead approves

**Correct answer: B**

**Explanation:** The exceptions clause ends with an unconditional prohibition: "applications operating under such exceptions must not process citizen data." The statement claims the opposite — that approval plus review licenses citizen data processing — and no reading of the clause supports it; approval and review are necessary conditions for the exception to exist at all, not compensating controls that unlock the prohibited activity. False, and option D fails identically by promoting the approver into an override authority the text does not create. The design of this trap is worth studying: it stacks legitimate-sounding safeguards ("approved and reviewed") to make a prohibited outcome feel governed. Real security arguments fail the same way — "we documented it and someone senior signed" is not the same as "the standard permits it". When you ensure conformity to the standards you set, the terminal clause — the flat prohibition — is the one to check first, because it is the one process theatre most often obscures.

**Question 4 (moderate) — Inference from the standard**

Which one of the following can properly be inferred from the passage?

- A) Break-glass access has never been misused.
- B) The standard treats break-glass access as an auditable exception pathway: it trades the role-based system's preventive control for compensating detective controls — automatic logging, prompt review, credential rotation, and board visibility.
- C) The role-based access system logs all access automatically.
- D) Re-certification of privileged grants happens quarterly.

**Correct answer: B**

**Explanation:** Option B is a synthesis of stated facts, which is what sound inference is: break-glass "may bypass the role-based system" (the preventive control is surrendered) while every use attracts logging, two-day review, 24-hour rotation, and quarterly board reporting (detective and corrective controls compensate). Characterising this structure as an auditable exception pathway adds no fact the passage lacks — it names the pattern the facts form. Option A infers an operational history the text never mentions. Option C transplants the logging requirement from break-glass credentials to the role-based system; the passage requires logging of break-glass use and says nothing about the role-based system's logging. Option D invents a cadence: re-certification is required "before renewal", which — given 90-day maximum grants — implies at most 90-day cycles, not quarterly-as-stated; close, but the passage does not say quarterly, and inference questions punish the near-miss paraphrase precisely because it feels safe. The lead-level takeaway: inferring the *control pattern* from a standard is legitimate and useful; inferring unstated *facts* is neither.

**Passage 2 — Inter-lead governance exchange**

*"From: Head of Service Transition. To: All IT operations leads. Following October's release collisions, the release calendar will operate as follows from 1 December. Each lead may reserve at most two production windows per month per application. Reservations become firm five working days before the window; before that point, the transition team may move them with 48 hours' notice to resolve conflicts. Firm reservations may only be moved with the owning lead's consent, except where a security-critical release requires the slot, in which case the transition team decides after consulting both leads. Unused firm windows are released back to the pool 24 hours before their start time. Leads wishing to exceed the two-window limit must present the business case at the fortnightly leads' meeting; the limit does not apply to emergency changes, which follow the existing emergency process."*

**Question 5 (moderate) — True, false, or cannot say**

Statement: "Once a reservation becomes firm, the transition team can never move it without the owning lead's consent."

- A) True
- B) False
- C) Cannot say
- D) True, except during October

**Correct answer: B**

**Explanation:** The passage grants firm reservations consent protection — "may only be moved with the owning lead's consent" — and then immediately carves the exception: "except where a security-critical release requires the slot, in which case the transition team decides after consulting both leads." Consulting is not consent: in the security-critical case, the transition team may move a firm reservation over the owning lead's objection, having heard it. "Never without consent" is therefore contradicted: False. The consult/consent distinction is among the most consequential in governance reading — one obliges a conversation, the other confers a veto — and misreading it in either direction causes real conflict: a lead who believes they hold a veto they do not have will feel betrayed by a legitimate override; a transition team that believes consultation is optional will breach the clause. When you liaise with leads across IT operations, precision about who holds decision rights versus voice rights is the difference between governance and grievance.

**Question 6 (moderate) — True, false, or cannot say**

Statement: "A lead who needs three production windows for one application in a single month has no route to obtain them."

- A) True
- B) False
- C) Cannot say
- D) True, unless the changes are emergencies

**Correct answer: B**

**Explanation:** The passage provides the route explicitly: "Leads wishing to exceed the two-window limit must present the business case at the fortnightly leads' meeting." A third window is therefore obtainable — through a defined governance path — so "no route" is contradicted: False. Option D is half-right about emergencies (which bypass the limit via the existing emergency process) but still endorses the false core claim by treating the business-case route as non-existent. Notice the reading pattern the question rewards: limits in well-drafted governance are usually *defaults with escape valves*, and the escape valves are where the text's real flexibility lives. This mirrors the change-freeze scenario logic from operational practice: the professional response to a constraint is rarely "impossible" and rarely "bypass" — it is "here is the route the document itself provides". Leads who read documents for their routes, not just their restrictions, become the people others consult before escalating.

**Question 7 (hard) — Applying the rules to a scenario**

It is Tuesday. Your firm reservation for a normal release is Thursday 22:00. Monday morning (three working days before... in fact four calendar days), you learn your release will not be ready. According to the passage, what happens to your window if you do nothing, and what should you conclude?

- A) Nothing happens; firm windows belong to you until used.
- B) The window is released back to the pool 24 hours before Thursday 22:00 — that is, Wednesday 22:00 — only if it is actually unused at that point; but "doing nothing" until then hoards a slot other leads could plan against, so the cooperative move is to release it as soon as you know.
- C) The transition team will move your reservation with 48 hours' notice.
- D) You lose your right to reserve windows next month.

**Correct answer: B**

**Explanation:** Apply the clauses in order. The reservation is firm, so the pre-firm 48-hour-move power (option C) no longer applies — that power exists only before the five-working-day threshold. No forfeiture-of-future-rights rule exists in the passage (option D invents one). The operative clause is: "Unused firm windows are released back to the pool 24 hours before their start time" — so at Wednesday 22:00, a still-unused window returns to the pool automatically; option A's "belong to you until used" contradicts this. Option B adds the judgement layer the scenario is really probing: the automatic release exists as a backstop, but a lead who *knows* on Monday that the window is dead and sits on it until Wednesday night denies peer leads two days of planning certainty — legal under the text, corrosive to the system the text exists to create. The strongest verbal reasoners at lead level do exactly this double reading: first, what does the document require; second, what behaviour does the document's *purpose* invite beyond its requirements. Assessments score the first; your peer leads remember the second.

**Passage 3 — Post-incident review extract**

*"PIR-88: The 14 March outage of the grants application lasted 6 hours 40 minutes. The trigger was a routine certificate renewal performed correctly by the operations team; the renewed certificate, however, exceeded the maximum key length supported by a legacy integration component, which failed closed. The component's limitation was documented in the supplier's compatibility notes but not in our own configuration records, and the renewal procedure did not include an integration compatibility check. The incident lead's decision to restore service via the backup integration path at hour two was sound; the further four hours were consumed by data reconciliation, for which no rehearsed procedure existed. Recommendations: R1 — add compatibility constraints to configuration records for all integration components; R2 — extend the certificate renewal procedure to include integration checks; R3 — develop and rehearse a data reconciliation runbook; R4 — assess all legacy integration components for similar constraints within 90 days. The review notes that the same legacy component was flagged as 'requiring modernisation' in the 2024 application strategy, but the work was deferred in two successive planning rounds."*

**Question 8 (moderate) — True, false, or cannot say**

Statement: "The operations team performed the certificate renewal incorrectly."

- A) True
- B) False
- C) Cannot say
- D) True, since the renewal triggered the outage

**Correct answer: B**

**Explanation:** The passage states the renewal was "performed correctly by the operations team"; the failure arose from an undocumented constraint in a legacy component interacting with a correct action. The statement is contradicted: False. Option D exhibits the exact reasoning error post-incident reviews exist to prevent — collapsing "triggered" into "performed incorrectly". A trigger is the event that exposed a latent condition; culpability language ("incorrectly") requires a deviation from procedure, and the procedure — as the review notes — contained no compatibility check to deviate from. This distinction is not pedantry; it determines what gets fixed. Blame the operator and you retrain someone who did nothing wrong while the latent condition waits for the next correct action to trigger it; locate the gap in the procedure and the records (R1, R2) and the class of failure closes. Leads who read — and write — incident reviews with the trigger/cause/latent-condition vocabulary intact are the ones whose organisations actually learn.

**Question 9 (hard) — True, false, or cannot say**

Statement: "Had the 2024 modernisation work not been deferred, the outage would not have occurred."

- A) True
- B) False
- C) Cannot say
- D) True, because the legacy component caused the failure

**Correct answer: C**

**Explanation:** The counterfactual is tempting — the legacy component's limitation caused the failure, and modernisation was flagged and deferred — but examine what the passage actually establishes. It does not state what the modernisation would have entailed, whether it would have replaced or merely wrapped the component, whether the replacement would have supported longer key lengths, or when the work would have completed relative to 14 March. "Would not have occurred" asserts certainty about an unrealised alternative history that the text cannot underwrite: Cannot say. Option D mistakes a causal contribution in the actual world for proof about a hypothetical one. Note the review's own craft here: it *notes* the deferral without claiming the counterfactual — a deliberate discipline, because deferred-work observations in PIRs exist to inform future prioritisation, not to allocate retrospective blame with false precision. When you carry this review into your strategy conversations (as R4 and the deferral note invite), the defensible sentence is "deferral left a flagged risk in production, and that risk materialised" — supported — rather than "the deferral caused the outage" — not established. Precision about counterfactuals is what keeps incident reviews credible enough to change planning decisions.

**Question 10 (hard) — True, false, or cannot say**

Statement: "The incident lead's handling of the incident is criticised by the review."

- A) True
- B) False
- C) Cannot say
- D) True, since four hours were consumed by reconciliation under their command

**Correct answer: B**

**Explanation:** The review explicitly evaluates the incident lead's key decision: restoring via the backup integration path at hour two "was sound". The four reconciliation hours are attributed to the absence of a rehearsed procedure — a systemic gap generating recommendation R3 — not to the lead's conduct. The passage therefore contains praise for the lead's decision and criticism of a missing organisational capability; "criticised by the review" is contradicted: False. Option D repeats the attribution error from Question 8 in a new costume — events occurring on someone's watch are not thereby that person's failings, and the review's own language carefully separates the two. This separation is the load-bearing wall of blameless review culture: if leading an incident competently through an unrehearsed situation earns criticism, no capable engineer will volunteer to lead incidents. As the lead who conducts such reviews, you will write these sentences yourself; as a verbal reasoner, your job is to read attribution exactly as drafted, because the difference between "the lead consumed four hours" and "four hours were consumed by a gap the lead did not create" determines careers.

**Question 11 (hard) — Best summary for the leads' meeting**

Which option best summarises PIR-88 for the IT operations leads' meeting?

- A) "A certificate renewal error caused a 6-hour 40-minute grants outage; the team has been reminded to check compatibility."
- B) "A correctly performed certificate renewal exposed an undocumented key-length limit in a legacy integration component, causing a 6h40m grants outage — two-thirds of it spent on unrehearsed data reconciliation. Fixes: compatibility constraints into configuration records, renewal procedure extended, reconciliation runbook rehearsed, and a 90-day sweep of similar legacy components. Strategic note: this component's modernisation was flagged in 2024 and deferred twice — the deferral decision merits revisiting."
- C) "Legacy systems are risky and should all be replaced as soon as possible."
- D) "The outage lasted 6 hours 40 minutes and four recommendations were made. Details available on request."

**Correct answer: B**

**Explanation:** Judge each against what a leads' meeting needs: accurate mechanism, honest impact, actionable fixes, and the cross-portfolio implications peers can act on. Option A misstates the mechanism ("renewal error" contradicts the review's "performed correctly" — the exact error Question 8 rehearsed) and shrinks four recommendations into a reminder, which is how systemic fixes decay into email folklore. Option C inflates one finding into an unfunded ideology; leads' meetings discount speakers who generalise past their evidence. Option D is administratively true and informationally empty — peers cannot assess their own exposure from it, though the 90-day sweep (R4) is precisely the item that needs their engagement. Option B preserves the causal chain (correct action, latent constraint, failed-closed), quantifies where the time actually went (reconciliation — the finding peer leads should test against their own services), carries all four recommendations, and surfaces the deferral note as a planning question rather than an accusation. Summary questions at lead level test altitude control: high enough to fit the meeting, low enough that nothing decision-relevant is lost — and option B is also, not coincidentally, the version of events your **Ownership and topic** accountability would want on record.

**Question 12 (hard) — Clear-writing judgement in a procedure**

Recommendation R2 requires extending the certificate renewal procedure. Which drafting of the new step is most likely to be executed correctly by an engineer working alone at 02:00?

- A) "Before renewing any certificate, consider whether integration components might be affected and act accordingly."
- B) "Before renewal: (1) list the application's integration components from the configuration record; (2) for each, check the 'maximum supported key length' field against the new certificate's key length; (3) if any component's maximum is below the new key length, STOP — do not renew; raise a change task to resolve the constraint first. If the field is blank for any component, STOP and escalate to the on-call lead: a blank field means the check cannot be passed."
- C) "Renewals must be compatibility-validated in line with best practice and the relevant supplier documentation, which should be consulted as appropriate."
- D) "Check key lengths before renewing. See supplier notes."

**Correct answer: B**

**Explanation:** Test each draft against the 02:00 standard: an engineer alone, mid-procedure, no one to ask. Option A delegates the entire judgement ("consider", "might", "accordingly") back to the reader — it is a wish, not a step, and the engineer who caused no problem in March followed exactly this kind of implicit expectation. Option C is polished vagueness: "best practice", "as appropriate", and unnamed documentation give the 02:00 reader nothing executable — it would pass a document review and fail its first use. Option D has the right instinct compressed past usability: which key lengths, checked where, against what, and then what? Option B is executable by construction: enumerated steps, a named data source (the configuration record R1 is populating — note the recommendations interlock), an explicit comparison, and defined outcomes for *both* failure modes — including the subtle one, the blank field, which it correctly treats as a stop condition rather than a pass; absence of evidence of incompatibility is not evidence of compatibility, and encoding that logic into the procedure is what "failing safe" looks like in prose. Drafting and maintaining procedures is your **Technical specialism** skill, and this is its acceptance test: a procedure is well written exactly when the least-contextualised competent reader, at the worst hour, does the right thing by following it literally.

### Preparation tips

- **Build who/what/when tables as you read.** Governance and security passages multiplex actors, obligations, and deadlines. Thirty seconds of margin-tabling prevents the actor-splice and clause-migration errors the hardest statements are built from.
- **Trace every number to its owning clause.** Durations, thresholds, and cadences migrate between clauses in memory. Before judging any statement containing a figure, re-find the clause that owns it.
- **Treat consult, consent, inform, and approve as different words.** They allocate power differently, and both assessments and inter-lead disputes turn on the difference.
- **Guard the trigger/cause/blame distinctions.** In incident-review passages, "triggered by", "performed correctly", and "no procedure existed" are precise allocations. Statements that blur them are usually False — and reviews that blur them are usually yours to send back.
- **Refuse confident counterfactuals.** "Would have prevented" claims about unrealised histories are Cannot say unless the passage itself establishes the mechanism and timing. This discipline doubles as PIR-writing craft.
- **Apply the 02:00 test to writing questions.** The best-drafted option is the one a competent stranger executes correctly alone at the worst hour. Enumerated steps, named sources, and defined failure modes beat polish every time.

### Common pitfalls to avoid

- **Reading your experience instead of the passage.** The more standards you have written, the stronger the pull to answer from convention. The test — like an audit — is about what *this* document says.
- **Letting stacked safeguards launder a prohibition.** "Approved, documented, and reviewed" can still sit inside a clause ending "must not". Check the terminal prohibition before crediting the process wrapper.
- **Confusing voice with veto.** "After consulting both leads" means the decision can go against you. Statements — and colleagues — that read consultation as consent are misreading the power allocation.
- **Collapsing "triggered" into "caused by error".** Correct actions expose latent conditions. Blame-shaped paraphrases of blameless findings are contradictions, not summaries.
- **Endorsing the near-miss paraphrase.** "Quarterly" for "before renewal of 90-day grants", "six-month grants" for "six-monthly exception reviews" — close is False. Precision is the entire test.
- **Choosing polished vagueness in drafting questions.** The option that sounds most professional while committing to nothing is the designed decoy. Executability, not register, is the criterion.

## Workplace job-specific situational judgement assessment

### About this assessment

A situational judgement assessment (SJT) presents realistic workplace dilemmas and asks you to evaluate possible responses — most effective, least effective, or full rankings. For lead-level roles, the scenarios change character fundamentally: the question is rarely "what should you do with your hands?" and almost always "what should you do with your influence?" Scenarios feature team members' mistakes and development, peer-lead conflicts, strategic pressure from above, standards being quietly eroded, and moments where accountability, honesty, and relationships pull in different directions.

The typical format is 12 to 20 scenarios, untimed or generously timed, four responses each, scored against the judgements of experienced professionals and the organisation's valued behaviours: user focus, ownership and accountability, collaboration across boundaries, developing others, integrity in reporting and governance, and proportionate escalation. At lead level, scorers particularly discriminate on delegation calibration (doing versus verifying versus letting go), on whether responses build or consume organisational trust, and on whether the candidate protects systems and cultures — not just outcomes — because leads shape the environment in which hundreds of future decisions get made by other people.

Why do employers use SJTs for lead roles? Because at your level, judgement is the job. Your role summary makes you accountable for issues that occur *and* proactively responsible for finding potential ones; it has you leading incident investigations, managing high-impact changes, liaising with peer leads, and achieving excellent user outcomes through other people. Technical mastery is assumed; what distinguishes a strong lead is what they do when a peer's project threatens their service, when a team member fails, when governance is inconvenient, and when the truthful number is the unwelcome one.

As you practise, notice the recurring anatomy of strong lead-level answers: they secure the service and the user first; they keep records, reports, and communications truthful; they operate governance skilfully rather than bypassing or weaponising it; they develop people through events rather than around them; and they address systems — the process, the standard, the incentive — not just instances. Weak answers hide, hoard, blame, bypass, or win the moment at the culture's expense.

### How this assessment maps to your role

- **Incident leadership scenarios** map to **Incident management** and **Ownership and topic**: leading investigations under pressure, communicating honestly upward, holding accountability without seizing your team's agency, and staying with an issue until genuinely resolved or handed over.
- **Change and release dilemmas** map to **Change management**: managing high-impact complex changes means arbitrating collisions between teams, holding release policy when it is inconvenient, and knowing when the emergency route is legitimate.
- **Standards-erosion scenarios** map to **Technical specialism** and **Asset and configuration management**: standards you set are tested not on the day you publish them but on the day compliance is expensive; conformity is a behaviour you cultivate, not a document you own.
- **Team development scenarios** map to your leadership of engineers: SJTs probe whether you convert mistakes into learning, distribute growth opportunities honestly, and give difficult feedback early.
- **Cross-boundary and supplier scenarios** map to **Problem management** and **Service focus**: consulting specialists effectively, holding ownership across organisational seams, and building frameworks that survive contact with other teams' incentives.
- **User-versus-stakeholder scenarios** map to **User focus**: representing users internally, distinguishing user needs from user desires, and championing research when opinion is louder than evidence.

### Practice questions

**Question 1 (easy) — Your engineer's mistake becomes visible upward**

An engineer on your team misconfigured a deployment last week, causing a 40-minute outage. You handled it: incident run properly, fix verified, lessons captured, the engineer coached. Today the service owner emails you, copying your head of profession: "I hear this was human error. Who was responsible? We need accountability." What is the most effective response?

- A) Name the engineer, since the service owner asked directly and transparency matters.
- B) Reply that the accountable person is you, as the lead responsible for the service and its safeguards; describe the systemic gap (the deployment pipeline permitted an invalid configuration) and the fixes now in place; and offer to walk the service owner through the review.
- C) Reply that it was a process failure and no individual was involved.
- D) Forward the email to the engineer and ask them to respond with an explanation.

**Correct answer: B**

**Explanation:** The email conflates two meanings of "accountability", and the lead's job is to answer the legitimate one. Accountability for the service and its defences sits with you — that is not noble self-sacrifice; it is the actual org chart, and option B says so while delivering what the service owner genuinely needs: the mechanism, the fix, and confidence that recurrence is engineered against. Option A converts a coached, corrected mistake into a career event, teaching your team that errors surfaced honestly become names in executive email — after which errors stop being surfaced honestly, and your incident data quietly rots. Option C is a detectable evasion: "no individual was involved" is false, and when the truth emerges (it will), it costs your credibility and reframes a defensible position as a cover-up. Option D abandons the engineer to an audience they should never have to face alone and outsources your accountability downward — the inverse of leadership. The pattern scorers look for: leads absorb blame upward and pass learning downward, never the reverse. Protecting the psychological safety that keeps your team honest *is* protecting the service.

**Question 2 (easy) — Standards versus a deadline, in public**

At a cross-team planning meeting, a delivery manager announces that their team will skip your configuration documentation standard for this release "because the deadline is fixed and the standard is heavy — we'll backfill the records next month". Several other teams' representatives are present. What is the most effective response?

- A) Let it pass in the meeting to avoid conflict, then quietly note the exception.
- B) In the meeting, state clearly that undocumented production configuration is a risk you cannot accept for released services, and propose resolving it today: either scope the documentation to the minimum viable record so it fits the deadline, or bring the exception to the governance forum where risk acceptance belongs — then follow up constructively with the delivery manager afterwards.
- C) Publicly overrule the delivery manager and threaten to block the release.
- D) Agree to the backfill plan on condition it is done within a month.

**Correct answer: B**

**Explanation:** The public setting is the scenario's real content: whatever happens next will be witnessed by every team deciding how seriously your standards bind *them*. Option A teaches the room that the standard is negotiable by announcement — the cheapest possible price — and "quietly noting" an unaccepted risk manages nothing. Option D is subtler but structurally similar: backfill promises after go-live compete against the next deadline and reliably lose; more importantly, accepting it makes you, not the governance forum, the person absorbing an organisational risk on a handshake. Option C wins the exchange and poisons the well — humiliating a peer in public converts a solvable compliance problem into a durable alliance against your standards. Option B holds the line without hostility and, crucially, offers *routes*: a scoped minimum record (standards worth having usually have a viable core), or the governance forum where risk acceptance is legitimately decided by people authorised to accept it. That combination — firm on the risk, flexible on the path, generous in private follow-up — is how standards survive their first expensive collision, which is the only test that matters. Your **Technical specialism** skill says "ensure conformity"; conformity is manufactured in exactly these meetings.

**Question 3 (moderate) — The incident your senior engineer is mishandling**

You are accountable for a live severity 2 incident that one of your senior engineers is leading. Ninety minutes in, you observe: the investigation is fixated on a single hypothesis despite contrary evidence, stakeholder updates are overdue, and two team members' suggestions have been talked over. The engineer is capable but visibly stressed. What is the most effective response?

- A) Take over command immediately — the incident is suffering.
- B) Say nothing during the incident; give thorough feedback afterwards.
- C) Intervene minimally and structurally: join the bridge, ask the questions that reopen the hypothesis space ("what evidence would rule this out? what are our other two candidates?"), take the stakeholder-update burden off the engineer's plate at their agreement, and make space for the overridden voices — leaving command with the engineer unless the service impact demands more.
- D) Privately message the two overridden team members to pursue their ideas separately without telling the incident lead.

**Correct answer: C**

**Explanation:** The incident has three live defects — hypothesis lock, communication debt, suppressed input — and none of them yet requires decapitating the command structure. Option C fixes each with the lightest touch that works: good questions reopen thinking without countermanding (and model exactly the technique the engineer should internalise); absorbing the update burden removes the task stress is dropping, visibly as support rather than rebuke; inviting the quiet voices repairs the information flow the incident depends on. Command stays where it is, which matters beyond this incident: seniors who are rescued-by-replacement at the first wobble never become leads. Option A pays that development cost immediately and permanently, and is only right when service impact genuinely outruns coaching — a severity 2 with a functioning (if imperfect) investigation does not clear that bar. Option B honours development theory while the service and stakeholders absorb ninety more minutes of drift — feedback later is not a substitute for stewardship now. Option D creates a shadow investigation: uncoordinated production access during an incident is how second incidents start, and discovering it destroys the incident lead's trust in you twice over. The lead-level skill being scored is graduated intervention: your **Incident management** accountability exercised at the minimum altitude that restores the investigation — and not one metre lower.

**Question 4 (moderate) — Peer lead's change threatens your service**

A peer lead's team is deploying a shared-platform upgrade next week. Reviewing the change, your team finds its database migration will lock tables your case application reads during the deployment window, likely causing user-facing timeouts — the change record scopes impact as "platform services only". You raised it with the peer lead, who replied: "Our testing shows minimal impact; we're not delaying a programme milestone for a theoretical timeout." What is the most effective response?

- A) Accept their assessment — it is their change, their accountability.
- B) Escalate to the CAB immediately with a formal objection to force a delay.
- C) Offer a joint technical session within a day: your engineers demonstrate the lock behaviour against a realistic read load; if the risk is confirmed, agree mitigations together (window shift, read-replica routing, or staged migration) and correct the change record's impact scope; if their testing withstands the demonstration, withdraw the concern and say so.
- D) Quietly schedule your application into read-only mode during their window without telling them, protecting your users either way.

**Correct answer: C**

**Explanation:** This is an evidence dispute wearing a governance costume, and the strong move resolves the evidence before invoking the governance. Option C does exactly that: a joint session with a realistic load is cheap, fast, and decisive in both directions — and its symmetry is the point. Committing in advance to withdraw if wrong makes the challenge collegial rather than territorial, which is what keeps peer-lead relationships usable for the next twenty collisions. If the risk confirms, the change record's impact scope gets corrected — not a bureaucratic nicety, but the mechanism by which the CAB approves reality rather than optimism, which is your **Change management** skill's entire premise. Option A abdicates: their change, but your users — "achieve excellent user outcomes" does not pause at organisational seams. Option B escalates a resolvable technical question into a formal conflict *before* attempting resolution; CABs exist for impasses, not first disagreements, and leads who weaponise governance early find it weaponised back. Option D is the quietly disastrous one: it degrades your own users' service to hedge a risk you have not proven, conceals material information from a change decision, and — when discovered — brands you as the lead who acts unilaterally behind peers' backs. Escalation remains available if the demonstration is refused; run the evidence first.

**Question 5 (moderate) — The flattering misuse of your report**

Your quarterly performance report showed portfolio availability of 99.7%, up from 99.4%. You later see a programme board pack quoting your figures under the heading "Application modernisation programme delivers reliability gains" — but you know the improvement came almost entirely from your team's incident-response work and a decommissioned flaky component; the modernisation programme has not yet touched your applications. The programme director is influential and the attribution flatters your portfolio too. What is the most effective response?

- A) Let it stand — the numbers are accurate, only the interpretation is generous, and the goodwill is useful.
- B) Contact the programme director before the board meets: the availability figures are right, but the attribution is not supportable — offer corrected wording crediting the actual drivers, and offer to help define measures that will genuinely track the programme's future impact on your portfolio.
- C) Email the board directly to correct the record over the director's head.
- D) Correct the attribution only if someone at the board questions it.

**Correct answer: B**

**Explanation:** The numbers are yours, so the inferences drawn from them travel on your credibility — and this attribution error is not victimless: a board believing modernisation *already* delivers reliability will fund, sequence, and expect on that belief, and when the programme's real (later, different) effects arrive, the baseline confusion lands on your future reports. Option B corrects the error at the cheapest possible point — before the board sees it — through the person who owns the pack, preserving both truth and relationship; the constructive coda (help define genuine programme measures) converts the correction from a rebuke into an alliance, and incidentally protects your evidence base for years. Option A prices integrity against goodwill and sells too cheap: "accurate numbers, generous interpretation" is how organisational self-deception is always laundered, and you flagged the flattery to yourself, which means you knew. Option C corrects the record while maximising the relational damage — going over the director's head *before* offering them the chance to fix their own pack is escalation without cause. Option D gambles the truth on someone else's diligence; boards rarely audit congenial numbers. The scored behaviour is proactive stewardship of what your data is used to claim — **Ownership and topic** extended to the information layer, where a lead's accountability increasingly lives.

**Question 6 (moderate) — Distributing the golden opportunity**

A high-profile go-live needs one engineer seconded to the programme for three months — visible work, career-making. Two of your team volunteer: Sam, your strongest engineer, who delivered the last two such secondments flawlessly and whom the programme has asked for by name; and Aisha, slightly less experienced, consistently excellent, who has told you in development conversations that she needs precisely this exposure and has never had it. Losing either is manageable. What is the most effective response?

- A) Send Sam — the programme asked for Sam, and go-lives deserve the strongest available engineer.
- B) Send Aisha, telling the programme she is your choice and you stand behind her readiness; brief her thoroughly, arrange Sam as her named consultation point, and tell Sam candidly why — pairing it with a growth commitment that actually stretches Sam, whose development now needs novelty, not repetition.
- C) Ask the two of them to decide between themselves.
- D) Split the secondment: each does six weeks.

**Correct answer: B**

**Explanation:** Interrogate option A's premise: what does *Sam* gain from a third identical secondment? Nothing developmental — Sam's growth now lies elsewhere, so routing the opportunity by past performance serves the programme's convenience and nobody's development, while teaching your team that visibility compounds: the already-visible get more visible, and development conversations like Aisha's are pleasant fictions. Option B is the leadership answer because it treats the secondment as what it is — a development asset you steward — and de-risks the choice properly: public backing (your credibility spent on her, which is what backing means), thorough briefing, and a consultation line to Sam that converts his experience into infrastructure rather than incumbency. The candid conversation with Sam matters equally; unexplained passings-over corrode your best people, while "your next stretch is X, and this one is Aisha's" is the sentence strong leads can say. Option C abdicates a judgement that is specifically yours — it hands Aisha a contest against the incumbent asked for by name, which is no contest, while sparing you the accountability. Option D halves the value of the experience for both, disrupts the programme with a mid-flight handover, and is the classic false compromise: fairness-shaped, development-empty. SJTs at lead level score whether you distribute growth deliberately; go-lives are staffed for the service *and* the pipeline of people who will run the next five.

**Question 7 (moderate) — Least effective: the strategy consultation**

You are drafting the application strategy for your portfolio. A consultation draft is with peer leads, your team, and the service owner. Feedback arrives: two peer leads challenge your consolidation timeline as optimistic; your own senior engineers flag that a proposed platform choice conflicts with the department's cloud mandate; the service owner asks why user research does not appear in the evidence base. Which response is LEAST effective?

- A) Extend the timeline analysis with the peer leads' delivery data, and publish the revised assumptions with the change noted.
- B) Thank everyone for the feedback, note that consultation has now concluded, and publish the strategy substantively unchanged to maintain momentum.
- C) Commission the missing user research input, adjusting the strategy's evidence base and acknowledging the gap the service owner identified.
- D) Convene your senior engineers to work through the platform-mandate conflict and either change the choice or document the exemption case honestly.

**Correct answer: B**

**Explanation:** Polarity check first: LEAST effective. Options A, C, and D are the three feedback threads handled properly — each takes the challenge seriously, does the work it implies, and leaves an honest audit trail (revised assumptions noted, gap acknowledged, exemption case documented rather than hoped past). Option B is consultation theatre: the process ran, the feedback arrived, and none of it altered anything — which is worse than not consulting, because it converts three sets of engaged stakeholders into three sets of people who now know their engagement is decorative. The specific feedback makes it damning: a mandate conflict flagged by your own engineers is not an opinion to weigh but a defect to resolve — publishing across it means your strategy is non-compliant *knowingly*; peer leads' delivery data is exactly the evidence a timeline needs; and a service owner asking "where are the users?" of an application strategy has identified a hole below the waterline, given your **User focus** duty to champion research and represent users internally. "Momentum" is the tell — strategies gain real momentum from stakeholders who recognise their fingerprints in the final text, not from publication dates. Defining the application strategy is your headline duty; defining it *through* consultation rather than despite it is what makes the strategy executable by the people it needs.

**Question 8 (hard) — The velvet request to reclassify**

End of quarter. Your portfolio breached its availability KPI, driven by one major incident. Your head of operations says, in a corridor conversation: "That March outage — a fair chunk was really the network team's fault, wasn't it? Seems harsh for it all to land on your KPI. Have another look at the attribution before the figures go up — no pressure." Reattributing the network-related portion would bring your portfolio back within target. The incident genuinely did involve a network component, though your application's slow failover amplified the impact. What is the most effective response?

- A) Reattribute the network portion — it is arguably accurate and your head of operations has effectively endorsed it.
- B) Review the attribution honestly because the question is legitimate, but apply the standing measurement rules rather than the desired outcome: if the rules attribute user-facing downtime to the affected service regardless of cause, report the breach with a clear causal narrative — network trigger, amplified by your failover gap, with the improvement actions for the part you own — and tell your head of operations exactly that before publication.
- C) Refuse to look at the attribution at all, since reviewing it under pressure is already compromised.
- D) Split the difference: reattribute half the outage.

**Correct answer: B**

**Explanation:** The request's velvet construction — "arguably accurate", "seems harsh", "no pressure" — is the scenario's point: real integrity tests rarely announce themselves; they arrive as reasonable-sounding invitations with a desired answer pre-loaded. Option B finds the honest line: the attribution question is *legitimate* (multi-cause incidents genuinely raise it), so refusing to examine it (option C) confuses integrity with rigidity and leaves a fair question unanswered — but the examination must run on the standing measurement rules, decided before this quarter's answer was wanted, not on what makes the KPI green. Most availability regimes attribute user-facing downtime to the affected service precisely so that "whose fault" games cannot soften accountability for user experience — and your failover gap genuinely amplified the impact, which the causal narrative owns along with its fix. Option A launders a metric rescue through a corridor endorsement that will evaporate under audit ("I only asked him to have a look"). Option D treats truth as a negotiation — half a reattribution is a number with no methodology, indefensible in both directions. The strong close is telling your head of operations the outcome *before* publication: it respects their question, removes any ambush, and quietly establishes that your figures are rule-governed — which, over a career, is why your figures are the ones that end arguments. Breaching a KPI honestly costs a quarter; rescuing one dishonestly costs the currency your role runs on.

**Question 9 (hard) — Ranking: the failing framework you built**

Eighteen months ago you designed the portfolio's on-call framework. Evidence now accumulates that it is failing: two strong engineers cite on-call load in exit interviews; incident response times degrade on weekends; and a near-miss occurred when a fatigued engineer almost applied the wrong fix. Your head of operations praised the framework publicly last quarter. Rank these responses from most to least effective:

1. Present the evidence to your head of operations and peer leads as a framework failure requiring redesign, owning the original design decisions that aged badly, and propose a revision co-designed with the engineers who carry the load.
2. Make quiet incremental tweaks — rota adjustments, an extra escalation tier — without announcing a problem, protecting the framework's (and your) reputation while easing the worst symptoms.
3. Commission an independent review of on-call across the portfolio, delaying any change until it reports in two months, so the redesign is evidence-based and externally validated.
4. Defend the framework: exit interviews are multi-causal, weekend degradation has other explanations, and one near-miss is an anecdote — the framework is sound and the narrative of failure is premature.

- A) 1, 3, 2, 4
- B) 1, 2, 3, 4
- C) 3, 1, 2, 4
- D) 1, 3, 4, 2

**Correct answer: A**

**Explanation:** Response 1 leads decisively: the evidence is convergent (retention, performance, safety — three independent failure signals), the near-miss makes timing urgent, and owning your own design's failure publicly is the highest-value move available — it models the exact accountability you ask of engineers after incidents, and co-designing the fix with the people on the rota repairs both the framework and the trust it burned. Ranking 3 against 2 is the discriminating judgement, because each holds one virtue the other lacks. Response 3's virtue is honesty: commissioning a review is a visible, on-the-record acknowledgment that something may be wrong, its independence de-biases a question you have a stake in, and its terms of reference can include interim mitigations while it runs. Its vice is the two-month stall as framed — deferral wearing rigour's clothes when a safety signal is live. Response 2's virtue is immediacy: rota adjustments give fatigued engineers real relief this week. Its vice is concealment, and concealment is the deeper poison: unannounced tweaks mean the organisation never learns the framework failed, the engineers who flagged it in exit interviews go unvindicated, the near-miss's lesson is buried, and your head of operations goes on publicly praising a thing you know is broken — spending their credibility without their knowledge, exactly the corrosion that destroys leads when discovered. Honest-but-slow outranks helpful-but-hidden: a review's delay can be compressed and its scope amended once it exists in daylight, whereas a concealed fix corrupts the record indefinitely and forecloses the systemic redesign the evidence demands. Hence 3 above 2, and the order 1, 3, 2, 4. Response 4 is last without contest: each individual rebuttal is *technically* arguable, which is exactly what makes motivated reasoning dangerous — three independent signals converging on your own artefact is the moment for curiosity, and defending it is ego wearing analysis. Order: 1, 3, 2, 4 — option A. The meta-lesson is the hardest lead skill on the list: the frameworks you build are hypotheses, and your **Service focus** duty — coherent frameworks *that work* — includes being their most willing falsifier.

**Question 10 (hard) — User needs versus the loudest user**

A director-level "super user" of your case application lobbies persistently for a configurable dashboard — meetings, emails, a slot at your programme board. Your user research tells a different story: caseworkers' dominant needs are reliability during morning peaks and a simpler document upload flow; dashboards rank near the bottom of every study; and the director's own team's usage data shows the current dashboard features barely used. Budget allows one major workstream this year. What is the most effective response?

- A) Build the dashboard — director-level sponsorship secures budget, and visible senior satisfaction benefits the whole portfolio.
- B) Bring the evidence to the decision: present the research and usage data at the programme board alongside the director's request, explicitly distinguishing expressed desires from evidenced needs; recommend the reliability-and-upload workstream; and offer the director a cheap evidence test — a prototype dashboard evaluated with real caseworkers — so their idea is respected as a hypothesis rather than rejected as a claim.
- C) Split the budget: half the dashboard, half the reliability work.
- D) Decline the dashboard privately and hope the director's attention moves on.

**Correct answer: B**

**Explanation:** Your **User focus** skill contains, verbatim, the distinction this scenario weaponises: *explain the difference between user needs and the desires of the user* — and at lead level you must make that distinction stick against seniority, in a governance setting, without making an enemy of a director. Option B is that manoeuvre executed completely: the evidence and the request meet in the same forum (so the decision is the board's, made informed — not yours, made covertly); the recommendation follows the research; and the prototype offer is the masterstroke, because it treats the director's conviction as a testable hypothesis — which is respectful, cheap, and lets the evidence do the disagreeing. Championing research *to focus on all users* means exactly this: the 2,400 caseworkers who will never attend your programme board outvote one director in every study you have run, and someone must be their representative in the room. Option A spends the year's budget on the portfolio's least-evidenced need to purchase senior comfort — and when adoption data eventually shows another barely-used dashboard, the director's sponsorship will not be attached to the failure, but your delivery record will. Option C halves both workstreams into ineffectiveness — reliability engineering particularly resists half-funding — and reads as decision-avoidance because it is. Option D declines without the evidence and without the forum, achieving the disagreement while forfeiting its legitimacy; directors outlast hope. The scored behaviour: leads bring evidence to power respectfully, in the room where the decision lives.

**Question 11 (hard) — The supplier boundary and the peer lead's patience**

A persistent fault in a supplier-hosted integration degrades referrals between your case application and a peer lead's service. The supplier has cycled three engineers through the ticket in six weeks with no progress. Your peer lead, whose users are equally affected, wants to invoke contractual penalties immediately and has drafted a joint escalation letter for your signature. Your own assessment: the supplier's efforts have been genuinely incompetent rather than negligent, the contract's technical escalation route (a named senior architect) has never actually been invoked, and penalties would likely entrench positions while the fault continues. What is the most effective response?

- A) Sign the letter — peer solidarity matters, and six weeks is long enough.
- B) Refuse to sign and let the peer lead escalate alone if they insist.
- C) Propose to the peer lead a sequenced joint position: first invoke the contract's technical escalation route immediately — named architect, joint evidence pack, a two-week deadline with defined success criteria — with the penalty letter agreed, drafted, and explicitly next if the deadline fails; meanwhile stand up whatever interim mitigation protects both services' users.
- D) Bypass the dispute by building a workaround that re-routes referrals away from the supplier's component permanently.

**Correct answer: C**

**Explanation:** Both leads hold a piece of the truth: six weeks of cycling engineers *is* unacceptable (the peer is right about that), and unused escalation routes plus premature penalties *is* a losing sequence (your assessment is right about that) — so the strong answer synthesises rather than picks a side. Option C does so with craft: the technical escalation route is invoked *immediately* (urgency honoured), jointly (solidarity delivered — the peer lead gets a stronger joint action than the letter, not a refusal), with deadline and criteria (so "escalation" cannot become another six-week cycle), and with the penalty letter *pre-agreed as the next step* — which transforms it from a relationship-burning first move into a credible, visible consequence that concentrates supplier minds wonderfully. Interim mitigation runs in parallel because users do not care whose escalation theory wins; your **Ownership and topic** accountability and both teams' user outcomes demand protection *now*. Option A signs up to a sequence you believe will prolong the fault — solidarity that serves the relationship at the users' expense. Option B fractures the joint front the supplier most fears, and hands the supplier two uncoordinated customers instead of one alliance. Option D answers a different question: a permanent re-architecture as a dispute-avoidance move is unassessed change (**Change management**), probably unfunded, and concedes the contracted service without extracting either fix or remedy — though its instinct, protecting users by engineering, belongs in C's interim-mitigation slot at appropriate scale. Effective specialist consultation — your **Problem management** skill — includes consulting the *contract's* specialists: escalation clauses are unused capability, and leads who exhaust the designed routes before the punitive ones win both the fault and the relationship.

**Question 12 (hard) — Proactive discovery with a governance sting**

While preparing the quarterly configuration audit, you discover that a widely-used internal reporting tool — built years ago by a developer who has left, now embedded in four teams' daily work — runs on an unsupported framework version with two published critical vulnerabilities, has no entry in the CMDB, no owner, and direct read access to the case application's production database through credentials that predate your access standard. Nothing is currently on fire. What is the most effective response?

- A) Shut off the tool's database access today — unsupported software with critical vulnerabilities touching production citizen data is an unacceptable risk, whatever the workflow cost.
- B) Register the tool and its access in the CMDB as found; assess the actual exploitability of the vulnerabilities and the sensitivity of the accessed data within days, applying immediate low-disruption mitigations (credential rotation onto the standard, read scope reduction, network restriction); brief the four consuming teams and the security administration function honestly; and take an owned remediation decision — supported rebuild, managed replacement, or scheduled decommission — through governance with a dated plan.
- C) Add the tool to the risk register and schedule its consideration in next quarter's planning cycle.
- D) Quietly ask a developer on your team to patch the framework version informally, avoiding the bureaucracy since the tool is unofficial anyway.

**Correct answer: B**

**Explanation:** This is the scenario your role summary's proactive clause describes — *be proactive in searching for potential problems* — and it tests what you do when proactivity succeeds: you now hold an unowned risk that stops being unowned the moment you found it. Option B sequences by the record-understand-mitigate-decide pattern that governs all discovered-configuration work. Registration first (**Asset and configuration management**: the record must match reality *before* decisions rely on it); then real assessment, because "two critical CVEs" is a headline, not an exposure analysis — exploitability, data sensitivity, and network position determine whether this is a today-problem or a this-month-problem; immediate cheap mitigations (credential rotation, scope and network reduction) buy risk reduction without breaking four teams' mornings; honest briefing converts the tool's users from surprised victims of any later action into participants in the remediation choice; and the endgame runs through governance with a date, because unowned tools got this way precisely through undated good intentions. Option A pays maximum disruption for unmeasured risk — four teams' workflow destroyed by lunchtime on a vulnerability you have not yet established is exploitable is how security earns its enemies; act-first is right only when assessment confirms active exposure. Option C is the pattern that *created* this situation: unowned risk, politely deferred — and a quarter is a long time to knowingly leave pre-standard credentials on citizen data. Option D compounds every original sin: still no owner, no record, no assessment, plus an informal change to production-adjacent software — the tool's biography, volume two. The discriminating lead behaviour: found risks get owners, records, measured urgency, and dated decisions — not heroics, and not calendars.

### Preparation tips

- **Rehearse graduated intervention.** For every scenario involving your team, generate the minimal intervention first — the question, the offloaded task, the named support — and escalate only as service impact demands. Seizure is almost never the scored answer; neither is absence.
- **Check the polarity, then the constituency.** Confirm most/least effective, then ask whose interests each option serves: the user, the team, the record, the relationship, your reputation. Options serving mainly the last one are decoys.
- **Practise the accountability direction.** Blame absorbs upward, learning flows downward, credit flows outward. Options that reverse any arrow — naming engineers to executives, quiet fixes protecting your artefacts, claiming systemic wins personally — score poorly.
- **Pre-decide your integrity lines.** Velvet requests — "have another look", "arguably accurate", "just this once" — are easiest to refuse if the rule was chosen calmly in advance. Know which measurements, records, and attributions you will not bend, and rehearse the respectful sentence that says so.
- **Sequence evidence before governance, governance before penalties.** In cross-boundary disputes, the strong answers run: joint evidence, then designed escalation routes with deadlines, then formal consequences — with user-protecting mitigation running parallel throughout.
- **Debrief real dilemmas weekly.** Ten minutes reflecting on one live judgement call — options, choice, and what the best lead you know would have done — builds the judgement bank SJTs sample. Consider running the same exercise with your seniors; their calibration is your legacy.

### Common pitfalls to avoid

- **Rescuing competence into dependency.** Taking over your senior's wobbling incident, redoing your engineer's imperfect work — each rescue is a lesson in not being trusted. Intervene at the minimum effective altitude.
- **Buying senior comfort with user budget.** Director-sponsored features, flattering attributions, KPI rescues — any option purchasing upward goodwill at the expense of evidence, users, or truth is a designed trap.
- **Weaponising or worshipping governance.** Escalating first to force outcomes, and refusing legitimate routes out of process purity, fail identically: governance is a tool you operate skilfully, at the right point in the sequence.
- **Concealing the failure of your own artefacts.** Quiet tweaks to your failing framework, informal patches to embarrassing discoveries — concealment converts a design that aged badly into a character question. Own it first, loudly.
- **Solidarity against your own judgement.** Signing the peer's letter, accepting the head of operations' framing — alignment is valuable and purchasable too dearly. The strong option almost always offers allies something better than agreement: a sequenced plan.
- **Deferring discovered risk to the calendar.** Risk registers and next-quarter plans are where found problems go to become next year's incidents. Discovered risks get owners, mitigations, and dates — this week.

## Conclusion

You have now worked through a complete set of practice materials for the four assessment types most relevant to a lead application operations engineer: cognitive, numeric reasoning, verbal reasoning, and situational judgement. Completing it is a meaningful act of professional maintenance — the kind leads prescribe for their teams more readily than for themselves.

Look back at what you actually exercised. In the cognitive section, you synthesised weak signals into proactive investigations, swept policies as checklists, arbitrated release calendars past feasible to defensible, and ran strategy timelines to their last responsible decision points — the structured thinking beneath your application strategy and your **Change management** and **Problem management** duties. In the numeric section, you normalised portfolio comparisons, priced availability ambitions in recovery-time capability, verified remedies through confounders, built consolidation arithmetic that survives finance scrutiny, and negotiated KPI targets from quantified baselines — the numerical spine of **Availability and capacity management** and of every leads' meeting where your figures must end arguments rather than start them. In the verbal section, you read security standards, governance rules, and incident reviews at clause level — consult versus consent, trigger versus blame, prohibition versus process theatre — and judged drafting by the 02:00 test that your **Technical specialism** documentation duty ultimately answers to. And in the situational judgement section, you rehearsed the decisions that define lead careers: absorbing blame upward and passing learning downward, intervening at minimum altitude, holding standards in public, bringing evidence to power, owning your own artefacts' failures, and giving discovered risks owners and dates.

A single thread runs through all of it: at lead level, your accuracy and integrity are infrastructure. Other people build on your attributions, your forecasts, your summaries, and your example — which means every practised improvement in your reasoning compounds through everyone who relies on it. That is also the quiet answer to "why should a lead practise assessment questions?": because the instrument being sharpened is the one your whole portfolio runs on.

Keep the practice light and continuous. Once a week: recompute one figure before it is published, re-read one clause before you enforce it, and replay one judgement call against the best version of yourself. And consider sharing selected scenarios from this guide with your senior engineers — calibrating their judgement is both the best development you can give them and a rehearsal of your own.

Whatever assessment lies ahead — promotion board, internal benchmark, or a new department's selection process — walk in the way you would walk into a major go-live: prepared, paced, and with your decision points identified in advance. You lead complex operations for a living. This guide has simply let you watch yourself do it, one deliberate question at a time.

Good luck — and pass it on.
