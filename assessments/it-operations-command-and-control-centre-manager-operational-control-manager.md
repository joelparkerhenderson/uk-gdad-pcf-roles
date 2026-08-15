# Operational Control Manager - Psychometric Assessment Resources

## Introduction

Welcome. This guide has been prepared for you as an operational control manager working in a command and control centre within the UK Government Digital and Data profession. You may be preparing for an internal assessment or promotion board, benchmarking yourself against the demands of the next level, or using structured practice to sharpen the judgement your role exercises daily. Whatever your purpose, this document offers deliberate, role-grounded practice with full reasoning walkthroughs.

Psychometric assessments are standardised exercises measuring the cognitive capabilities and professional judgement that predict effectiveness in a role. At your level, the assessments worth taking seriously are job-specific ones, and that is what this guide provides. Every scenario here is drawn from the territory you are accountable for: day-to-day IT operations, incident and problem escalation, high-impact change requests, release governance, continuity runbooks and their testing, availability and capacity KPIs across groups of services, and the on-call accountability that follows you beyond working hours. The questions use the artefacts you actually handle — major incident timelines, change advisory board papers, capacity models, runbook test results, post-incident reviews — and the decisions you actually make: when to invoke continuity procedures, how to sequence a risky release, whether a problem investigation has genuinely found root cause, and how to balance a service owner's demands against the stability of the wider estate.

Why do these assessments matter at your level? Because your role concentrates risk. You are the escalation point: incidents and problems arrive at your desk precisely when they have exceeded someone else's judgement or authority. You are accountable for change management processes that preserve availability, which means your reading of an impact assessment — its logic, its numbers, its gaps — directly protects live public services. You lead incident investigations where the cost of a wrong deduction is measured in citizen-facing downtime. And you operate across IT operations as a whole, seeing the bigger picture across groups of services, which demands exactly the pattern recognition, numerical fluency, precise reading, and situational judgement that these four assessments measure. Practising them is not a compliance exercise; it is rehearsal for the sharpest moments of your job.

The document is organised into four main assessment sections, each with the same structure: what the assessment measures and why employers use it for this role, a mapping of its dimensions to the named skills in your role summary, a substantial set of practice questions with complete worked explanations, preparation tips, and common pitfalls.

To get the most from it: read each "About this assessment" section first; attempt every question and commit to an answer before reading the explanation; treat the explanations as the core content — they model reasoning techniques and connect each one back to operational leadership; and use the preparation tips as prompts for reflection on your own practice, particularly where they suggest exercises against your own estate's data, runbooks and records. Several questions are deliberately uncomfortable — ambiguity, conflicting stakeholders, imperfect options — because that is the honest texture of your role. Work through them steadily. Let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive assessment measures the mental operations your role demands — pattern recognition, logical deduction, error checking, prioritisation, and applied problem solving — using operational scenarios rather than abstract puzzles. For an operational control manager, that means reasoning over major incident evidence, change schedules and their dependency chains, runbook logic, cross-service failure patterns, and the governance artefacts of release and problem management.

The typical format is an online, timed test of 15 to 30 minutes with 15 to 30 questions, adaptive difficulty, and norm-referenced scoring that reports accuracy and speed separately. At senior levels, norm groups are typically managerial, so the comparison is against peers who also lead investigations and chair incident calls — the bar is correspondingly higher, and questions lean toward multi-constraint and multi-source reasoning rather than single-rule application.

Employers use cognitive assessment for this role because the role is, cognitively, a concentration point. When an incident escalates to you, the easy diagnoses have failed: what remains is differential reasoning under pressure, across services, with incomplete and partly contradictory evidence. When a high-impact change request reaches you, the question is rarely "does this follow the template?" but "what does this change *actually* touch, in what order, with what failure modes, and does the rollback logic survive contact with the dependency graph?" When you review a problem investigation, you are error-checking someone else's causal reasoning. And your accountability for proactive and preventative measures means the patterns you fail to notice become next month's major incidents. A well-designed cognitive assessment compresses these demands into minutes; practising it sharpens exactly the reasoning your accountability rests on.

### How this assessment maps to your role

The assessment dimensions map directly to the named skills in your role summary:

- **Pattern recognition** maps to **Service focus** and your duty of **proactive and preventative measures**: seeing the bigger picture across groups of services means recognising when apparently unrelated events across the estate form one pattern — correlated degradations, recurring failure signatures, common-cause risks in shared components.
- **Logical deduction** maps to **Incident management** and **Change management**: leading the investigation and resolution of incidents is structured differential diagnosis; managing high-impact, complex change requests means deducing consequences through dependency chains, release constraints and rollback paths.
- **Error checking** maps to **Problem management**, **Asset and configuration management** and **Continuity management**: reviewing investigations for unsound causal leaps, verifying secure configuration and asset records, and testing runbooks are all forms of finding the defect in an artefact others believe is sound.
- **Prioritisation** maps to your role as **escalation point** and to **Ownership and initiative**: everything reaching you is already urgent to someone; accountability means ranking by genuine impact across IT operations, not by volume of noise.
- **Applied problem solving** maps to **Availability and capacity management** and your **service management framework knowledge**: working through multi-constraint operational problems — recovery sequencing, capacity trade-offs, release scheduling — using ITIL lifecycle discipline as a scaffold rather than a script.

### Practice questions

**Question 1 (easy) — Pattern across services**

Overnight logs show: 02:10 — case system slow responses; 02:12 — licensing portal slow responses; 02:11 — HR tool slow responses; 02:40 — all three recover simultaneously. The three services run on separate application servers but share a storage array and an authentication service. Database servers are dedicated per service. What is the most productive first hypothesis?

- A) Three independent application faults occurring coincidentally.
- B) A fault in a shared dependency — the storage array or authentication service — affecting all three.
- C) A fault in the case system's dedicated database that spread to the others.
- D) Network issues at three separate user sites.

**Correct answer: B**

**Explanation:** Three services degrading within two minutes and recovering in the same minute is a synchronisation signature: independent faults (option A) do not start together and stop together. The dedicated databases (option C) cannot produce cross-service correlation — a per-service component fails per-service. Site network issues (option D) would affect users by location, not services by shared infrastructure, and the recovery pattern would be ragged. The shared dependencies — storage array, authentication service — are the only components whose failure modes predict exactly this signature, so option B directs investigation where the evidence points. This is the bigger-picture reasoning your service focus skill names: at escalation level, the diagnostic unit is not the service but the estate, and the highest-value question on any multi-service incident call is "what do the affected services share that the unaffected ones don't?" Asking it first routinely cuts hours from investigations.

**Question 2 (easy) — Deduction through a release rule**

Your release policy states: (i) high-impact changes require CAB approval and a tested rollback plan; (ii) changes to the authentication service are always high-impact; (iii) a rollback plan is "tested" only if executed successfully in the staging environment within the 30 days preceding implementation. A team proposes an authentication service change for the 20th, with a rollback plan last executed in staging 45 days before that date. Which statement must be true?

- A) The change may proceed if CAB approves it, since approval can substitute for testing.
- B) The change cannot proceed compliantly on the 20th unless the rollback plan is re-executed successfully in staging beforehand.
- C) The change is low-impact if the team classifies it as routine.
- D) The rollback plan is invalid and must be rewritten from scratch.

**Correct answer: B**

**Explanation:** Chain the rules. Rule (ii) makes the change high-impact by definition — team classification (option C) cannot override a categorical rule. Rule (i) then requires both CAB approval *and* a tested rollback plan: conjunction, so approval cannot substitute for testing (option A). Rule (iii) defines "tested" with a 30-day window; 45 days exceeds it, so the plan is currently untested in the policy's sense. The only path to compliant implementation on the 20th is re-execution in staging within the window — option B. Option D overreaches: the plan is stale, not necessarily wrong; the remedy the rules imply is re-execution, not rewriting. This is the exact reading discipline your accountability for release policies demands: definitions ("tested", "high-impact") are load-bearing, and the manager who lets "we tested it recently-ish" through is the manager explaining an unrolled-back failure to a post-incident review. Note also the leadership move the deduction sets up: the conversation with the team is not "no" but "re-run the rollback in staging this week and you're compliant" — governance as an enabling path, precisely because you read the rules well enough to find it.

**Question 3 (easy) — Error checking a major incident timeline**

A draft post-incident timeline reads: "14:02 monitoring alert fired. 14:10 incident declared SEV1. 14:25 service restored via failover. 14:20 failover initiated. 14:45 incident closed. Total user impact: 23 minutes." Which criticism of the draft is most accurate?

- A) The timeline is internally consistent and the impact figure is correct.
- B) The entries are out of order and the impact figure of 23 minutes matches restoration (14:25) minus alert (14:02), which may understate impact if users were affected before the alert fired.
- C) The impact should be 43 minutes, measured to incident closure.
- D) The failover cannot have been initiated before restoration was complete.

**Correct answer: B**

**Explanation:** Two defects, one subtlety. First, sequence: 14:20 (failover initiated) is listed after 14:25 (service restored) — the entries are disordered, which matters because timelines are evidence and reviewers reason from their order. Second, the impact arithmetic: 14:25 − 14:02 = 23 minutes, so the figure is computed from *alert* to *restoration*. But alerts fire when monitoring notices, not when impact begins — if degradation preceded the alert threshold, real user impact exceeds 23 minutes, and an honest timeline says "impact from no later than 14:02" or corroborates onset from user reports and logs. Option C errs oppositely: closure (14:45) is an administrative event; users were restored at 14:25, and measuring impact to closure inflates it. Option D misreads the (disordered) entries — initiation at 14:20 completing by 14:25 is perfectly coherent once re-sequenced. Reviewing incident artefacts for exactly these defects — ordering, denominator choice, measurement anchors — is the error-checking core of leading investigations: the timeline you sign off becomes the organisation's memory of the incident, and its subtle understatements become next year's under-investment in monitoring coverage.

**Question 4 (moderate) — Prioritisation at the escalation point**

It is 09:30. Four items compete for your personal attention as duty escalation manager:

1. A SEV2 on the licensing portal, 90 minutes old, being competently worked by a senior analyst who has just given you a confident update; resolution expected within the hour.
2. A junior team's request that you approve an emergency change to fix the SEV2 — the change record looks thin on rollback detail.
3. A director's office chasing a promised briefing note on last week's major incident, due at noon.
4. A pattern you noticed twenty minutes ago: the storage array serving three services is showing intermittent latency spikes of a kind that preceded a major outage two months ago — no service impact yet, no one else has flagged it.

What should you attend to first?

- A) Item 1 — the live incident always comes first.
- B) Item 2 — the emergency change is blocking incident resolution.
- C) Item 4 — a precursor pattern to a multi-service outage, currently unowned.
- D) Item 3 — commitments to directors protect the centre's credibility.

**Correct answer: C**

**Explanation:** Rank by expected impact given ownership, not by noise. Item 1 is serious but *owned and progressing* — a competent analyst, a confident update, resolution in sight; your intervention adds little. Item 2 needs you soon, but scrutinising a rollback plan is a bounded task that can follow immediately after. Item 3 has a deadline hours away. Item 4 is the discriminating case: a recognised precursor signature to a multi-service outage, affecting shared infrastructure, and — the critical property — *unowned*: no analyst is watching it, so its risk is compounding silently. Your role summary is explicit that you take proactive and preventative measures and are proactive in searching for potential problems; item 4 is that duty materialised. First action: spend the ten minutes to get it owned — task an analyst to investigate with a clear brief, alert the storage specialist, set a check interval — then turn to the rollback scrutiny in item 2, which likely resolves item 1 faster. The deeper principle, which distinguishes escalation-level prioritisation from queue-level: at your desk, the scarcest resource is attention to *what nobody else is holding*, and the highest-value use of your seniority is converting unowned risk into owned work. Options A and D anchor on visibility and rank; option B mistakes the urgent-adjacent for the urgent — the SEV2 has a workaround path with or without the thin change.

**Question 5 (moderate) — Runbook logic under test**

You are reviewing a continuity runbook test result. The runbook states: "Step 3: initiate database failover to the secondary site. Step 4: once failover completes (typically 8 minutes), redirect application traffic. Step 5: verify transactions succeed end-to-end. Note: if failover has not completed within 20 minutes, abort and fail back." In the test, failover completed in 26 minutes, the team proceeded to Steps 4 and 5, and all verifications passed. The test report concludes: "Runbook validated — all steps completed successfully." What is the soundest assessment?

- A) The test validates the runbook: every step ultimately succeeded.
- B) The test invalidates the failover mechanism and it must be replaced.
- C) The test reveals two findings: the failover breached its 20-minute abort threshold (so the runbook as written was not followed and its timing assumption failed), and the team's decision to continue past a mandatory abort point went untested for risk — the report's conclusion is unsound.
- D) The test is void and must simply be re-run.

**Correct answer: C**

**Explanation:** Separate outcome from process. The verifications passed — but the runbook was not executed as written: at minute 20, the mandated action was abort-and-fail-back, and the team instead waited and continued. So the test proves neither that the runbook works (its timing assumption — completion "typically 8 minutes", abort at 20 — failed) nor that ignoring the abort is safe (in a real event, continuing past the abort point with live users would have been a gamble; in the test it was merely lucky). "All steps completed successfully" is therefore doubly unsound: a step performed in breach of its own precondition did not "succeed" in any sense a continuity manager can bank. The genuine findings: why did failover take 26 minutes (capacity? data growth since the runbook was written?), and should the threshold or the mechanism change? Option A mistakes a passed verification for a validated procedure — the precise conflation runbook testing exists to catch. Option B overcorrects: one slow failover indicts the timing model, not necessarily the mechanism. Option D wastes the test's information — a test that falsifies assumptions is a *successful* test of exactly the kind your "test the runbooks to ensure availability is maintained" duty is for; the failure would be filing it as a pass. The habit this trains: when reviewing any test report, check whether "success" means "the procedure worked as designed" or "we deviated and got away with it" — continuity assurance lives entirely in that distinction.

**Question 6 (moderate) — Deduction across a change collision**

Friday's schedule contains: Change A (network team): core switch firmware upgrade, 20:00–22:00, requires the monitoring platform to be suppressed for the affected segment during the window. Change B (application team): case system release with post-deployment verification 21:00–21:30, whose verification plan states "confirm via monitoring dashboards that error rates remain below 1%". Both changes are individually approved. What has the approval process missed?

- A) Nothing — the changes touch different systems and different teams.
- B) Change B's verification depends on monitoring that Change A suppresses during the overlap: at 21:00–21:30 the dashboards cannot evidence the error rates, so B's success criteria are unverifiable as scheduled.
- C) Change A should never be scheduled on a Friday.
- D) Change B should be cancelled permanently.

**Correct answer: B**

**Explanation:** Trace each change's *dependencies*, not just its targets. A and B touch different systems — the collision is not technical but evidential: B's verification method (monitoring dashboards) is exactly what A's window suppresses. Deployed at 21:00, the case system release would be declared "verified" against dashboards that are blind — meaning a bad release could sail through its own success criteria and surface as Saturday's incident, with the change record showing green. That is the deduction option B makes, and it is the characteristic failure mode of change processes that assess requests *individually*: each was sound alone; the calendar made them jointly unsound. Remedies follow easily once seen — shift B outside the suppression window, or verify by direct log inspection instead of dashboards — but only the manager who reads the schedule as a *system* sees it. Options C and D reach for policy bluntness where sequencing precision is needed, and option A is the individual-assessment blind spot itself. Your accountability for effective change processes that maintain availability is, in large part, accountability for this class of cross-change reasoning: the CAB approves changes; someone must approve the *combination*, and at your level that someone is you.

**Question 7 (moderate) — Error checking a problem investigation**

A problem record submitted for your sign-off reads: "Recurring Monday-morning case system slowness investigated. Analysis: slowness correlates with the weekend backup completing late. Root cause: backup overrun. Action: backup window moved earlier. Result: next two Mondays showed no slowness. Problem closed — root cause confirmed." What is the most important weakness?

- A) Two clean Mondays is decent evidence, but the record never establishes *why* the backup overran — the true root cause remains uninvestigated, so recurrence risk (backup drifting late again as data grows) is unmanaged.
- B) The correlation with backups was probably coincidental.
- C) Two Mondays of confirmation is excessive; one would have sufficed.
- D) The record should not have been closed until six months of Mondays were observed.

**Correct answer: A**

**Explanation:** The investigation found a genuine causal link (backup overrun → slowness) and a working mitigation (earlier window), and the two-Monday confirmation is proportionate evidence the mitigation works. The weakness is one level down: "backup overrun" is a *mechanism*, not a root cause. Nothing explains why a backup that presumably once fitted its window stopped fitting — data growth? a slowed target? contention with a new job? Whatever the driver, it is still operating: if it is growth, the backup will in time overrun the *new* window, and the problem returns wearing a different timestamp. Determining preventative measures — your problem management skill's explicit language — means chasing causation to the level at which prevention is possible: cap the driver (archiving, incremental backups) or instrument it (alert on backup duration trend, not just completion). Option B contradicts the evidence without grounds. Options C and D quibble the confirmation period in opposite directions, treating the record's strongest element as its weakest. The reviewing habit this builds: for every "root cause" in a record you sign, ask "could this cause recur by the same mechanism that produced it?" If yes, the analysis stopped one "why" short — and your signature is the last control before that shortfall becomes institutional memory.

**Question 8 (moderate) — Capacity reasoning across a group of services**

Three services share a database cluster rated at 10,000 transactions per second (TPS). Current peaks: case system 4,200 TPS, licensing portal 2,800 TPS, reporting 1,500 TPS — total 8,500 TPS, though their daily peaks do not currently coincide. Two facts arrive: (i) the licensing portal expects a 50% peak increase at next month's renewal deadline; (ii) a proposed change would move reporting's heavy extracts into the same morning window as the other services' peaks. What does the combined picture imply?

- A) No issue: 8,500 TPS is within rating, and growth can be absorbed.
- B) The licensing increase alone (2,800 → 4,200) brings the non-coincident total to 9,900 TPS — tight but survivable if peaks stay separated; the reporting-window change is what converts it to a coincident ~9,900+ TPS peak against a 10,000 rating, leaving no headroom for incident-driven spikes. The change and the growth are individually absorbable but jointly unsafe as scheduled.
- C) The cluster must be replaced immediately regardless of the change.
- D) Reporting should be deleted from the cluster.

**Correct answer: B**

**Explanation:** Work the arithmetic, then the interaction. Licensing at +50%: 2,800 × 1.5 = 4,200 TPS. New total if all peaks coincided: 4,200 + 4,200 + 1,500 = 9,900 TPS against a 10,000 rating — 1% headroom, which in operational terms is none: failover transients, retry storms and month-end surges all exceed 1%. Today that coincidence doesn't happen — peaks are separated in time, which is an unpriced capacity subsidy. The proposed reporting change spends exactly that subsidy: moving extracts into the shared morning window manufactures the coincident peak. So the correct managerial reading is B's: two individually reasonable developments whose *combination* is the risk, and whose remedy is sequencing and separation (keep reporting's window apart, or defer the change past the renewal peak, or add capacity first) rather than panic procurement (C) or service amputation (D). Option A reads the current total against the rating and misses both dynamics. This is availability and capacity management exercised at estate level — the KPI protected is not one service's but the shared component's, and the analysis that protects it is precisely this: model the peaks, model their timing, and treat temporal separation as capacity you must not spend by accident.

**Question 9 (moderate) — Pattern in post-incident data**

Reviewing six months of major incident reviews, you tabulate contributing factors: of 14 majors, 9 involved a change implemented within the preceding 48 hours; of those 9, 7 were changes classified "low-impact" and therefore not CAB-reviewed; the 2 CAB-reviewed changes had both received conditions that were not verified before implementation. What is the most defensible conclusion?

- A) Changes cause most incidents, so change volume should be halved.
- B) The change process has two specific control gaps concentrated where scrutiny is lightest: "low-impact" classification is admitting risky changes unreviewed, and CAB conditions lack a verification step — both are addressable process defects the data localises precisely.
- C) The CAB is ineffective and should be disbanded.
- D) Fourteen incidents is too small a sample to conclude anything.

**Correct answer: B**

**Explanation:** Read the pattern's *structure*, not just its headline. The headline — 9 of 14 majors follow recent changes — invites option A's blunt response, but halving change volume punishes the many safe changes for the sins of a locatable few and throttles delivery. The data localises the defect twice over: 7 of the 9 change-related majors came through the *unreviewed* path, indicting the classification gate (either the criteria or their application let high-consequence changes self-declare as low-impact); and both reviewed changes failed at the *same* point — conditions imposed but never verified — indicting not the CAB's judgement (its conditions were evidently pertinent) but the absent enforcement step. So the remedies write themselves: tighten or audit the impact-classification criteria, and add condition-verification as a release gate. That is option B, and it exemplifies the preventative analysis your role owns: patterns across incidents are process telemetry, and the skill is resolving them to the *specific control* that failed. Option C reads the CAB data exactly backwards. Option D deserves a real answer: 14 is small for statistical inference, but 7-of-9 concentrating in one path and 2-of-2 failing identically are structural findings about *how* failures route, not marginal frequencies — and operational governance rightly acts on localised mechanism at this evidence level, while continuing to gather data. Waiting for statistical purity while the mechanism keeps firing is not rigour; it is deferred prevention.

**Question 10 (hard) — Multi-constraint major incident sequencing**

A storage failure at 05:30 has taken down four services. Constraints: (i) authentication must be restored before the case system and licensing portal (dependency); (ii) restoring any service requires a 30-minute engineer slot, one restoration at a time; (iii) the payments batch must be dispatched from the case system by 09:00 or the day's payments slip 24 hours — dispatch requires the case system up and a 30-minute batch run; (iv) the licensing portal's citizen peak begins at 09:00; (v) reporting has no morning deadline; (vi) one engineer is available until 08:00, when a second arrives, allowing parallel restorations from 08:00. It is 06:00. Which plan meets the hard deadlines?

- A) Auth 06:00–06:30; case 06:30–07:00; batch 07:00–07:30; portal 07:30–08:00; reporting 08:00–08:30.
- B) Auth 06:00–06:30; portal 06:30–07:00; case 07:00–07:30; batch 07:30–08:00; reporting 08:00–08:30.
- C) Case 06:00–06:30; auth 06:30–07:00; batch 07:00–07:30; portal 07:30–08:00.
- D) Auth 06:00–06:30; case 06:30–07:00; portal 07:00–07:30 and batch 07:00–07:30 in parallel; reporting 08:00.

**Correct answer: A**

**Explanation:** Fix the invariants first. Authentication precedes case and portal (constraint i), eliminating option C, which restores the case system before its dependency — a plan that fails at 06:30, not on paper but in production. Single-threaded restoration until 08:00 (constraints ii, vi) eliminates option D, whose 07:00 parallelism arrives an hour before the second engineer does. Options A and B both respect the dependency; the discriminator is deadline arithmetic. Option A: auth by 06:30, case by 07:00, batch run 07:00–07:30 — payments dispatched 90 minutes inside the 09:00 cut-off — portal restored by 08:00, an hour before its citizen peak; reporting, deadline-free, last. Every hard constraint met with margin. Option B restores the portal first: case completes 07:30, batch 07:30–08:00 — still inside 09:00, but with the margin halved and, more tellingly, for nothing: the portal needed 09:00 and option A already delivers it by 08:00. B spends deadline margin on the payments batch — the estate's tightest constraint — to buy earliness the portal cannot use. Under real incident conditions, margin on the binding constraint *is* the plan's resilience: any 15-minute overrun in A's sequence still dispatches payments; the same overrun in B starts consuming the cut-off. The technique to internalise for incident leadership: identify the binding deadline, sequence to maximise its slack, and treat "earlier than needed" on non-binding items as a cost, not a virtue. Then communicate the sequence with its rationale — because on a live bridge, a plan whose logic the teams understand is a plan that survives its first surprise.

**Question 11 (hard) — Deduction from conflicting evidence on an incident bridge**

07:40, major incident bridge. Evidence: the application team reports their servers healthy, blaming the database; the database team shows normal query times for completed queries, blaming the network; the network team shows clean links, blaming the application. Additional facts: connection counts on the database have climbed steadily since 07:00 and are near the configured maximum; application logs show rising "connection timeout" errors; a change record shows the application's connection-pool settings were modified last night to "improve reuse". As incident lead, what does the evidence best support?

- A) Someone is wrong and the three teams should each re-run their diagnostics until the guilty component confesses.
- B) The evidence pattern is consistent with connection-pool exhaustion: last night's pool change is leaking or hoarding connections; the database is healthy for queries that *get* connections (explaining its clean metrics), the network is genuinely clean, and the application's timeouts are queue-for-connection symptoms. Working hypothesis: the pool change; test by inspecting pool metrics and staged rollback.
- C) The database's configured connection maximum should be raised immediately to make the errors stop.
- D) All three teams' evidence cannot be simultaneously true.

**Correct answer: B**

**Explanation:** The bridge's trap is that all three teams are *right* — about their own components. The lead's job is the synthesis no single team owns: find the failure mode under which every team's clean evidence is simultaneously true. Option D asserts the evidence conflicts; it doesn't — it only conflicts with the assumption that some team must be lying or mistaken. Connection-pool exhaustion satisfies everything: completed queries run fast (database metrics clean), packets flow (network clean), servers compute (application infrastructure healthy), yet requests starve queuing for connections — and the climbing connection count plus last night's pool-behaviour change supplies both mechanism and trigger. Option B also does what a hypothesis must at your level: it names its test (pool metrics, staged rollback of the change) — leadership of an investigation is choosing the next *discriminating* action, not the next plausible story. Option C treats the symptom: raising the connection cap feeds a leak and defers exhaustion twenty minutes while destroying the cleanest natural experiment (the near-max plateau). Option A is abdication dressed as diligence — re-running diagnostics that already returned clean answers generates confidence, not information. The transferable pattern for everyone who chairs bridges: when every component reports healthy and the system is down, stop interrogating components and start interrogating *interactions* — and give recent changes to the interaction layer first claim on suspicion. That is "lead the investigation" as your skill defines it: not out-teching the specialists, but owning the reasoning between their silos.

**Question 12 (hard) — Preventative design against a recurrence pattern**

The storage latency signature from Question 4 was investigated: intermittent spikes recur every few weeks, each preceded two months ago by the same sequence — a firmware bug degrades one array controller, load shifts to the second controller, and if a busy period hits before the degraded controller is reset, a multi-service outage follows. The permanent firmware fix ships in "one to two quarters". Which interim control set best reflects your accountability for preventative measures?

- A) Wait for the firmware fix; interim engineering would be wasted work.
- B) Rely on staff vigilance: brief all analysts to watch latency dashboards more closely.
- C) Layered interim controls: an automated alert on the specific precursor signature (controller degradation, not just latency); a documented, tested runbook for the reset procedure with a defined trigger threshold; a standing agenda check on controller state before known busy periods; and a review date tied to the firmware fix's arrival — with the residual risk and its acceptance recorded.
- D) Declare the storage array unusable and migrate all services off it this month.

**Correct answer: C**

**Explanation:** Evaluate against the failure mechanism, which is fully characterised: known precursor, known window (degradation → busy period), known manual remedy (controller reset), known horizon (fix in one to two quarters). Option A accepts a recurring multi-service outage risk for up to six months on the grounds that mitigation is temporary — but *interim* is what mitigation is for; the cost of a precursor alert and a tested runbook is trivial against one avoided outage. Option B is the control that always fails: vigilance decays in weeks, doesn't survive shift boundaries or leave, and converts a detectable machine signature into a human attention tax. Option D exceeds the risk: a known, monitorable, resettable degradation with a shipping fix does not justify an emergency migration whose own change risk likely exceeds the threat. Option C is textbook layered interim control, and each layer maps to your named skills: the precursor-specific alert operationalises proactive monitoring (detect the *cause* signature, not the symptom); the tested reset runbook with a trigger threshold is continuity management as your summary defines it — manage the runbooks, test the runbooks; the pre-busy-period check institutionalises the vigilance option B left informal; and the review date plus recorded residual risk is the governance seal — interim controls without expiry dates become permanent scar tissue, and accepted risks without records become surprises in the next review. The design principle worth carrying: for a characterised failure mechanism, build one control per stage of the mechanism (detect the precursor, break the propagation, bound the exposure window) and one governance wrapper (review, record, expire). That is what "accountable for preventative measures" looks like written down.

### Preparation tips

- **Practise estate-level diagnosis on your own architecture.** Sketch your services' shared dependencies from memory, then verify against records. Most cross-service reasoning questions — and most real multi-service incidents — are solved by knowing this graph cold.
- **Review one closed problem record weekly with the "one more why" test.** Does the stated root cause explain why it happened *now*, and could the same driver reproduce it? This is the highest-yield error-checking drill for investigation review.
- **Read change schedules as combinations.** For next week's calendar, deliberately look for pairs: shared windows, suppressed monitoring, dependent verifications. Collision-spotting is a trainable reflex.
- **Rehearse binding-constraint sequencing.** For any planned window or recovery scenario, identify the tightest deadline and check the plan maximises its slack. Ten minutes with last quarter's incident timelines makes this instinctive.
- **Do timed practice in your second week.** Build accuracy first, then pace. Senior norm groups reward controlled speed: roughly 60–90 seconds per question with no panic guessing at the hard tail.
- **After each question, articulate the technique in one line.** "Shared-dependency signature"; "conjunction not substitution"; "margin on the binding constraint." Named patterns transfer to the bridge at 03:00; unnamed ones stay in the practice book.

### Common pitfalls to avoid

- **Diagnosing components when the fault is an interaction.** When every team's evidence is clean and the system is down, the answer lives between the silos — and recent changes to the interfaces get first suspicion.
- **Accepting mechanisms as root causes.** "The backup overran" explains the symptom, not the recurrence. Signing off one "why" short is how problems return with new timestamps.
- **Treating "we got away with it" as validation.** A test or incident where mandated thresholds were breached without consequence proves luck, not procedure. Audit what "success" means before you bank it.
- **Assessing changes individually when risk is combinatorial.** The calendar, not the change record, is where Friday night's outage hides.
- **Spending margin on non-binding constraints.** Restoring the wrong service "early" while the payments cut-off approaches is activity masquerading as progress. Sequence to the binding deadline.
- **Anchoring on the loudest item.** At the escalation point, everything arrives urgent. The discriminating question is ownership: competently-held incidents need your attention less than unowned precursors nobody has flagged.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment measures fluency with the quantitative material your role is accountable for: availability and error-budget arithmetic across service groups, capacity models and their projections, incident and change statistics, KPI reporting, and the cost-benefit reasoning behind preventative investment. It is not a mathematics examination; it is a test of whether the numbers that flow through your decisions — and outward under your signature — are handled with precision.

The typical format is an online, timed test of 20 to 30 minutes with 15 to 20 questions, calculator permitted, difficulty often adaptive, and scoring norm-referenced against managerial peers. Question data arrives as tables, chart descriptions, and short scenarios; multi-step calculations are common at senior levels, as are questions testing whether you notice when a presented figure is misleading.

For an operational control manager, numeric reasoning is inseparable from accountability. You are answerable for availability KPIs across groups of services, and availability is arithmetic: percentages, downtime budgets, burn rates, weighted aggregations. You approve high-impact changes on the strength of quantified impact assessments — and an assessment whose denominator you didn't check is a risk you accepted without knowing it. You review capacity cases, where the difference between a defensible projection and an extrapolated guess is exactly the kind of reasoning this assessment probes. And because your reports travel upward — to service owners, boards, directors — numerical errors at your level don't stay yours: they become the organisation's picture of its own operations. The questions below therefore emphasise not just calculation but *interrogation*: spotting the flattering average, the wrong baseline, the survivor-biased sample, the trend projected past its regime.

Every explanation shows its arithmetic step by step. Where a question turns on a judgement about the numbers rather than the numbers themselves, the explanation separates the two — a discipline worth importing into your own reporting.

### How this assessment maps to your role

- **Availability arithmetic and error budgets** map to **Availability and capacity management**: managing service components against KPIs at estate level means converting fluently between percentages, downtime minutes, burn rates and weighted aggregates — and knowing which representation informs and which flatters.
- **Capacity modelling and projection** map to **Service focus** and **Asset and configuration management**: seeing the bigger picture across groups of services includes modelling shared-component load, headroom, and the timing of peaks; verifying the state of assets includes verifying the numbers claimed about them.
- **Incident and change statistics** map to **Incident management**, **Problem management** and **Change management**: leading investigations and reviewing problem records means judging what counts, rates, and before/after comparisons actually evidence; managing high-impact changes means auditing the quantified impact case.
- **Cost and risk quantification** map to your accountability for **proactive and preventative measures** and your **service management framework knowledge**: preventative investment is justified numerically — expected downtime avoided, risk-weighted cost — and ITIL-style reporting disciplines depend on defensible figures.
- **Report interrogation** maps to **Ownership and initiative** and **User focus**: taking accountability for what goes out under your name, and ensuring the numbers reported reflect what users actually experienced rather than what the aggregation method preferred.

### Practice questions

**Question 1 (easy) — Downtime budget across a quarter**

A service has a 99.7% availability KPI measured quarterly. Taking a 91-day quarter as 91 × 24 × 60 = 131,040 minutes, what is the quarterly downtime budget, to the nearest minute?

- A) 131 minutes
- B) 393 minutes
- C) 262 minutes
- D) 1,310 minutes

**Correct answer: B**

**Explanation:** Permitted downtime = (100% − 99.7%) = 0.3% of the quarter. Step by step: 1% of 131,040 = 1,310.4 minutes; 0.3 × 1,310.4 = 393.12, which rounds to 393 minutes — about 6.5 hours per quarter. Option A is 0.1%, option C is 0.2%, option D is 1%. Knowing budgets in minutes rather than percentages changes conversations: "we have 393 minutes per quarter" makes a proposed 4-hour maintenance window (240 minutes) visible as 61% of the entire quarterly budget spent on one planned event — the kind of framing that turns an abstract KPI into a governance decision about whether the window needs re-design. As the manager accountable for these KPIs across services, budget-in-minutes should be a figure you can produce for each major service without looking it up.

**Question 2 (easy) — Burn rate against elapsed time**

Thirty-eight days into the 91-day quarter, the case system has consumed 250 of its 393-minute downtime budget. What percentage of budget is consumed versus percentage of quarter elapsed, and what does the comparison indicate?

- A) 64% consumed vs 42% elapsed — burning roughly 1.5 times too fast; on current trend the budget exhausts around day 60, well before quarter end.
- B) 64% consumed vs 42% elapsed — comfortably on track since consumption is below 100%.
- C) 36% consumed vs 58% elapsed — under-burning.
- D) The comparison is meaningless because incidents are random.

**Correct answer: A**

**Explanation:** Consumption: 250 ÷ 393 = 0.636 → 64%. Elapsed: 38 ÷ 91 = 0.418 → 42%. The ratio 64/42 ≈ 1.52 means downtime is accruing about one and a half times faster than time is passing. Projected exhaustion: at 250 minutes per 38 days, the burn rate is 6.58 minutes/day; remaining budget 393 − 250 = 143 minutes lasts 143 ÷ 6.58 ≈ 21.7 days — exhaustion near day 60, leaving a month of quarter with zero budget. Option B commits the definitive burn-rate error: comparing consumption against 100% instead of against elapsed time — "under budget" is only meaningful relative to how much period remains. Option D mistakes stochastic arrival for unanalysable arrival: individual incidents are unpredictable; aggregate burn is exactly what trend management is for. The managerial value is the *early* conversation this arithmetic enables at day 38 — tightening change risk appetite for the service, accelerating a known problem fix — rather than the explanatory conversation at day 61. Burn-rate review across your service group belongs in your weekly rhythm precisely because the KPI is only manageable while budget remains.

**Question 3 (easy) — Weighted availability for a service group**

Your monthly report aggregates three services: case system 99.2% availability, 6 million requests; licensing portal 99.8%, 3 million; reporting 98.9%, 1 million. What is the request-weighted availability for the group, and how does it compare with the simple average?

- A) Weighted 99.35%, simple 99.30% — weighting flatters slightly.
- B) Weighted 99.32%, simple 99.30% — effectively identical.
- C) Weighted 99.35%, simple 99.30% — the weighted figure is higher because the busiest service performed mid-pack.
- D) Weighted 99.30%, simple 99.35%.

**Correct answer: C**

**Explanation:** Weighted: (99.2 × 6) + (99.8 × 3) + (98.9 × 1) = 595.2 + 299.4 + 98.9 = 993.5; divide by 10 (million requests): 99.35%. Simple: (99.2 + 99.8 + 98.9) ÷ 3 = 297.9 ÷ 3 = 99.30%. The weighted figure is 0.05 points *higher* here — worth pausing on, because weighting is often assumed to punish. It moves the aggregate toward the traffic: the 6-million-request case system (99.2%) dominates, the strong portal (99.8%) carries 3 million, and the weak reporting service (98.9%) carries only 1 million, so its poor month barely dents user experience. Both A and C state the right numbers; C states the right *reason*, and the reason is the reportable content — an aggregate should come with one sentence on what drives it. The governance edge: weighting by requests answers "what did users experience?"; a simple average answers "how did our services do on average?" — different questions, both legitimate, and your report should say which it is answering. The manipulation risk runs both ways: a supplier aggregating with the method that flatters is exactly what your review should catch, which requires computing both in your head to one decimal, as you just did.

**Question 4 (easy) — Change success rate with a base-rate twist**

Last quarter: 480 standard changes with 6 failures; 45 high-impact changes with 4 failures. A report states: "Overall change success rate: 98.1% — process healthy." What is the more informative reading?

- A) The overall figure is correct and sufficient; 98.1% is healthy.
- B) Overall (515 changes, 10 failures → 98.06%) is arithmetically right but blends two populations: standard changes fail at 1.25%, high-impact at 8.9% — seven times the rate, on exactly the changes with the largest blast radius. The blended figure conceals the concentration of risk.
- C) The overall figure is wrong: 10 failures in 515 changes is 94%.
- D) High-impact changes should be compared only with other organisations' benchmarks.

**Correct answer: B**

**Explanation:** Verify the overall: 515 − 10 = 505 successes; 505 ÷ 515 = 0.9806 → 98.1% — arithmetically sound (eliminating C, whose 94% miscomputes). Now decompose: standard 6 ÷ 480 = 0.0125 → 1.25% failure; high-impact 4 ÷ 45 = 0.0889 → 8.9% failure. The 7× disparity is the finding: the blended rate is dominated by the 480 routine changes, so the headline is effectively a statement about the easy population, while the risky population — where one failure can mean a multi-service outage — fails nearly one time in eleven. For the manager accountable for high-impact change processes, 8.9% is the number that should drive action (are rollback tests being skipped? are impact assessments thin? — compare Question 9 of the cognitive section, where post-incident data localised similar gaps). The reporting lesson generalises: any rate computed over a mixed population should be decomposed before it reassures — blended KPIs are where concentrated risks go to hide. Option D defers a decision your own data already supports.

**Question 5 (moderate) — Impact quantification for a change window**

A proposed emergency change requires taking the licensing portal offline for 40 minutes. Traffic data: daily average 6,000 requests/hour; the proposed slot (14:00–14:40) runs at 1.8× daily average; 25% of afternoon requests are new applications that fail hard offline (the rest can be deferred with a retry page); the alternative slot (05:00–05:40) runs at 0.15× daily average with the same 25% application share. How many hard-failing requests does each slot cost, and what is the ratio?

- A) 14:00 slot: 1,800; 05:00 slot: 150; ratio 12:1.
- B) 14:00 slot: 1,080; 05:00 slot: 90; ratio 12:1.
- C) 14:00 slot: 2,700; 05:00 slot: 225; ratio 12:1.
- D) 14:00 slot: 1,080; 05:00 slot: 150; ratio about 7:1.

**Correct answer: A**

**Explanation:** Stage the model: rate × multiplier × duration × affected share. Afternoon slot: 6,000 × 1.8 = 10,800 requests/hour; the window is 40 minutes = 2/3 hour, so in-window traffic is 10,800 × 2/3 = 7,200 requests; hard-failing share 25% → 7,200 × 0.25 = 1,800 failed applications. Early slot: 6,000 × 0.15 = 900 requests/hour; × 2/3 = 600 in-window; × 0.25 = 150. Ratio: 1,800:150 = 12:1 — option A. The distractors encode staged-model slips a reviewing manager must recognise in submitted impact assessments: option B's 1,080 comes from converting the 40 minutes as 0.4 of an hour instead of 2/3 (10,800 × 0.25 × 0.4 = 1,080) — a decimal-looking duration that isn't decimal; option C's 2,700 stops at the hourly application rate (10,800 × 0.25) without applying the window duration at all; option D mixes a correct afternoon slip with a correct early-slot figure, which is why checking *each* stage beats pattern-matching the totals. Each stage is trivial; the errors live in the transitions — units of duration, order of shares — which is precisely where your review attention should sit. And note what the finished numbers buy: a 12:1 impact ratio makes the 05:00 slot overwhelmingly preferable unless the emergency genuinely cannot wait sixteen hours, and "genuinely cannot wait" is now priceable — waiting costs the overnight risk of the unfixed fault; not waiting costs roughly 1,650 additional failed citizen applications. Quantified both ways, the CAB conversation is short, and your accountability for the decision rests on arithmetic anyone can audit.

**Question 6 (moderate) — Trend with seasonality**

Monthly incident counts for the estate over twelve months: 82, 79, 85, 88, 84, 90, 118, 121, 92, 95, 91, 97 (January to December; July and August contain the annual licensing renewal peak). A report claims: "Incidents rose 18% over the year (82 → 97): sustained deterioration." What is the sounder analysis?

- A) The claim is correct: 97 is 18% above 82.
- B) Comparing single endpoint months overstates certainty; excluding the known July–August seasonal peak, the series runs roughly 82–97 with a mild upward drift (~1.3/month by simple trend), and 97 in December versus 82 in January is consistent with that drift — real but modest, and the "18%" framing anchored on the lowest early month exaggerates it. The July–August spike is seasonal load, not deterioration, and should be analysed separately against last year's peak.
- C) There is no trend: the differences are noise.
- D) The July–August figures should be averaged into the trend to avoid bias.

**Correct answer: B**

**Explanation:** Endpoint-to-endpoint percentage change is the weakest possible trend claim: it stakes everything on two months' idiosyncrasies. Check the claim's arithmetic first — (97 − 82) ÷ 82 = 15 ÷ 82 = 18.3%, so the calculation is right — then interrogate the inference. The series ex-peak (82, 79, 85, 88, 84, 90, 92, 95, 91, 97) does drift upward: crude slope ≈ (97 − 82) ÷ 11 ≈ 1.4 incidents/month, or compare first-quarter mean (82) with last-quarter mean (94.3) — a ~15% rise on quarter-averages, more robust than endpoints but confirming genuine drift. So option C's "no trend" is wrong; the drift is real. What option B correctly rejects is the *framing*: "sustained deterioration" powered by an 18% endpoint figure and implicitly by the 118–121 peak months, which are seasonal demand (renewals), not process decline — the peak's proper comparator is last year's peak, answering "is our seasonal resilience improving?" separately from "is baseline load growing?" Option D would smear a known structural event into the baseline, corrupting both analyses. The reporting standard this models for your own sign-offs: separate seasonal from secular, prefer period-averages to endpoints, and never let a percentage anchored on a favourable base carry the headline. A ~15% annual drift in baseline incidents is a genuine capacity-and-prevention signal deserving a measured response — which credibility-destroying overstatement makes harder, not easier, to resource.

**Question 7 (moderate) — Problem investigation: before/after with a denominator check**

A problem fix for recurring printing failures was deployed on 1 June. Evidence offered for closure: "May: 40 printing incidents. June: 22 — a 45% reduction, fix confirmed." Additional context you request reveals: May had 21 working days, June 20; and on 10 June the largest user site (historically ~35% of printing incidents) began a phased office move, with roughly half its staff off-site for the rest of the month. What is the sound assessment?

- A) 45% reduction confirms the fix; close the record.
- B) Adjust for working days: May 40 ÷ 21 = 1.90/day, June 22 ÷ 20 = 1.10/day — a 42% daily-rate reduction, so the conclusion stands unchanged.
- C) The working-day adjustment still shows ~42% down, but the site move removed a large share of exposure for two-thirds of June: the site contributing ~35% of incidents halved its usage from 10 June, plausibly accounting for a sizeable slice of the reduction on its own. The fix may well be working, but the evidence is confounded; require either site-level incident breakdown or another clean month before closure.
- D) The fix clearly failed because incidents did not fall to zero.

**Correct answer: C**

**Explanation:** Layer the checks. First, denominators: per-working-day rates (1.90 vs 1.10) survive the adjustment — option B does this correctly and stops there. The deeper issue is *exposure*: incident counts are driven by usage, and the confound arrived on 10 June. Rough sizing: the big site contributes ~35% of incidents; halving its staffing for ~two-thirds of the month removes roughly 0.35 × 0.5 × 0.67 ≈ 12% of expected incidents — not the whole 42% reduction, but enough that the fix's true effect is materially uncertain (is it 42%, or nearer 30%?). Option C draws the right managerial conclusion: promising but confounded, and it specifies the cheap resolution — site-level breakdown (if incidents fell proportionally at *unaffected* sites, the fix's effect is clean) or one more month. Option A closes on headline arithmetic; option D demands a standard ("zero") the fix never promised. This is the statistical spine of your problem management sign-off duty: before/after comparisons are only evidence when denominators (time) and exposure (usage) are held level, and the reviewing habit is two questions — "per what?" and "what else changed?" — asked of every closure figure. Note the phrase "another clean month": patience is itself a control; problem records closed one month early on confounded data are how recurring problems earn their adjective.

**Question 8 (moderate) — Capacity cost-benefit for a preventative measure**

The storage precursor alert from your cognitive section (Question 12) needs a business case. Engineering estimate: 5 days' effort at £600/day to build alert plus runbook. Historical data: the failure mechanism produced one multi-service outage in the past two quarters, costing an estimated 6 hours of degraded service across three services, with an internal cost model valuing such an outage at £45,000 (staff time, recovery effort, and citizen-service disruption). Firmware fix expected in at most two quarters; assume without controls the outage recurs once per two quarters until then, and with controls the recurrence probability is cut by 80%. What is the expected net benefit of building the controls?

- A) £45,000 − £3,000 = £42,000.
- B) Expected loss avoided = £45,000 × 1 occurrence × 80% = £36,000; cost = 5 × £600 = £3,000; expected net benefit ≈ £33,000, an ~11:1 return.
- C) £3,000 cost with no benefit, since the firmware fix makes controls redundant.
- D) The case cannot be made because outage costs are estimates.

**Correct answer: B**

**Explanation:** Structure the expected-value calculation. Exposure window: up to two quarters, in which the mechanism historically fires once. Without controls: expected loss ≈ 1 × £45,000. With controls: recurrence cut 80%, so expected loss avoided = £45,000 × 0.8 = £36,000. Control cost: 5 days × £600 = £3,000. Expected net benefit: £36,000 − £3,000 = £33,000; return ratio 36,000 ÷ 3,000 = 12, so roughly an order of magnitude — option B (its "~11:1" reflects netting the cost; either framing is defensible, the magnitude is the point). Option A claims the full outage cost as benefit, ignoring both the probability structure and the 20% residual — the classic overselling that gets preventative cases discounted by reviewers. Option C repeats the "interim work is waste" fallacy the cognitive question dismantled, now numerically refuted: £3,000 against £36,000 expected. Option D deserves the serious answer: yes, £45,000 is a model estimate, so flex it — even at half the cost (£22,500), the return is ~6:1; the decision is insensitive to the estimate's uncertainty, which is exactly what sensitivity checking is for and exactly what makes the case robust in front of a sceptical finance reviewer. This is the numeric form of your accountability for proactive and preventative measures: prevention competes for resources through expected-value arithmetic, and the manager who can run it — honestly, with the 80% and the sensitivity — is the manager whose preventative work gets funded.

**Question 9 (moderate) — Reading a percentile, not an average**

A service's response-time report shows: mean 380 ms, median 210 ms, 95th percentile 1,900 ms, 99th percentile 4,800 ms, against a user-experience target of "95% of requests under 2,000 ms". A stakeholder reads the mean and concludes: "380 ms — miles under 2,000; excellent month." What is the accurate reading?

- A) The stakeholder is right: 380 ms is well under target.
- B) The service technically meets the stated target (95th percentile 1,900 < 2,000) but by only 5%, and the tail is severe: the worst 1% of requests take over 4,800 ms — nearly 23 times the median. The mean (380) sits far above the median (210) precisely because that tail drags it; the target is met with almost no margin, and any tail worsening breaches it. "Excellent" misreads a distribution as a number.
- C) The service breaches the target because 4,800 > 2,000.
- D) Mean and median should be averaged to give a fair summary (295 ms).

**Correct answer: B**

**Explanation:** Match each statistic to what it measures. The target is a 95th-percentile statement, so the compliant comparison is 1,900 vs 2,000: met, with 100 ms — about 5% — of margin. Option C errs by testing the 99th percentile against a 95th-percentile target; the worst 1% is *permitted* to exceed 2,000 under this SLA (whether the SLA *should* allow 4.8-second experiences for 1% of users is a legitimate service-design question — but it is a different question from compliance). Option A reads the mean as if typical: with median 210 and mean 380, the distribution is heavily right-skewed — the mean is nearly double the median because a small number of very slow requests pull it — so the mean here describes neither the typical user (median) nor the guaranteed experience (percentiles). Option D invents a statistic. The operational content of B is the *margin and trajectory*: 5% headroom on the binding percentile means the KPI is one bad deploy or one capacity notch from breach, so the management action is tail investigation now (what do the >1,900 ms requests share — an endpoint, a query, a site?), which is your proactive duty expressed in distribution terms. The reporting habit for your sign-offs: response-time summaries lead with the percentile the SLA binds on and its margin, never with the mean — and any mean/median gap this large is itself a finding worth a sentence.

**Question 10 (hard) — Reconciling KPI figures from two systems**

Your monthly availability figure for the case system comes from two sources. The monitoring platform reports 99.42% (measured by synthetic checks every 60 seconds from the data centre). The user-experience tool reports 98.9% (measured from real user sessions). The service desk logged 214 minutes of user-reported disruption; the monitoring platform's outage log totals 253 minutes for a 43,800-minute month. Which reconciliation is soundest?

- A) Report 99.42% — the monitoring platform is the system of record.
- B) Report 98.9% — real users outrank synthetic checks.
- C) First check internal consistency: 253 outage minutes ÷ 43,800 = 0.578% unavailability → 99.42%, so the platform's own figures cohere. The user-experience gap (98.9% → ~482 user-impacted minutes) exceeds the platform's 253 minutes by ~229 minutes, indicating impact the synthetic checks miss — partial degradations, specific user paths, or site-level issues (and the 214 desk-logged minutes confirm substantial user-visible disruption). Report both figures with the gap explained, and open an action on monitoring coverage: the 229-minute blind spot is itself a finding.
- D) Average the two: 99.16%.

**Correct answer: C**

**Explanation:** Verify before reconciling. Platform internal check: 253 ÷ 43,800 = 0.005776 → 0.578% down → 99.422% available — matches its reported 99.42%, so the platform is at least self-consistent. Translate the user-experience figure into minutes for comparability: (100 − 98.9)% = 1.1% × 43,800 = 481.8 minutes of user-impacted time. Gap: 482 − 253 = 229 minutes of user impact invisible to the synthetic checks. Mechanically this is expected — a 60-second synthetic check from the data centre tests one path at one frequency, and misses degradations that are partial (some users, some transactions), path-specific, or upstream of users but downstream of the check — and the service desk's 214 logged minutes corroborate that users experienced substantially more disruption than the platform saw. Now the reporting judgement: options A and B each pick a winner, but the figures answer different questions (infrastructure availability versus experienced availability), and option D's average answers no question at all — averaging two valid measurements of *different things* produces a number with no referent, the cardinal sin of KPI aggregation. Option C reports both with the reconciliation — which is what accountability looks like in a report: the reader learns what happened *and* what your measurement can and cannot see — and converts the gap into an action, because a 229-minute monitoring blind spot is a defect in your detection estate exactly as real as a failing service. The habit for your monthly cycle: reconcile experienced against measured availability every month; a stable small gap is measurement physics, a growing gap is your monitoring aging out of the architecture it watches.

**Question 11 (hard) — Queue dynamics during a major incident**

During a major incident, the service desk receives calls at 150/hour (normal: 20/hour). Desk capacity is 90 calls/hour; calls not answered within the hour abandon. The incident is expected to run 3 more hours. Two mitigations are available, separately or together: (i) a recorded status message expected to deflect 40% of incoming calls before they need an agent; (ii) borrowing staff to raise capacity to 130 calls/hour, available from one hour from now. What best characterises the options?

- A) Neither helps: 150 > 130, so calls are lost regardless.
- B) Message alone: effective arrivals 150 × 0.6 = 90/hour = capacity, so abandonment stops immediately. Borrowed staff alone: hour 1 loses 60 calls, hours 2–3 lose 20/hour — 100 abandoned over 3 hours. Both together: arrivals 90 vs capacity 130 from hour 2 — 40/hour of spare capacity but only after an hour in which the message alone already sufficed. The status message is the decisive mitigation; staff add resilience if deflection underperforms its estimate.
- C) Borrowed staff alone solve it: 130 > 90.
- D) Both must be implemented because more capacity is always better.

**Correct answer: B**

**Explanation:** Model each configuration. Baseline: arrivals 150, capacity 90 → 60 abandoned/hour → 180 over 3 hours. Message only: effective arrivals 150 × (1 − 0.4) = 90/hour, exactly matching capacity → abandonment ≈ 0 from activation (knife-edge, but bounded). Staff only: hour 1 unchanged (60 lost); hours 2–3: 150 − 130 = 20 lost/hour → total 60 + 40 = 100 abandoned — better than 180, far worse than the message. Together: from hour 2, arrivals 90 against capacity 130 → 40/hour headroom. Option B captures all three computations and — the senior part — the *decision structure*: the message dominates because it acts immediately and attacks demand rather than supply, while the staffing option is late and insufficient alone (option C misses that 130 exceeds *deflected* arrivals but not raw arrivals — it "solves it" only in combination with the message it ignores). Option D reaches the same implementation as B might, but by reflex rather than reasoning — and reflex fails the next scenario, where borrowing staff carries a real cost elsewhere in the operation. The knife-edge deserves its sentence: 90 vs 90 leaves zero margin, so if deflection lands at 35% rather than 40%, abandonment resumes at 7.5 calls/hour — which is precisely why B frames the staff as *resilience against estimate error* rather than redundancy. During real majors, this demand-vs-supply framing is a leadership tool: the fastest fix for an overwhelmed desk is almost always upstream (better status communication cutting call volume) rather than downstream (more agents), and the manager who models both in two minutes chooses upstream first, every time. That instinct — communicate to reduce demand, staff to insure the estimate — is user focus and incident leadership arithmetic working together.

**Question 12 (hard) — Interrogating a supplier's SLA report**

A managed-infrastructure supplier reports: "Q2 SLA performance: 99.95% availability achieved (target 99.9%). Note: figures exclude the emergency maintenance of 14 May (4 hours), performed to prevent imminent disk failure, as emergency preventative maintenance is excludable under contract clause 7.3." The 4-hour window fell at 10:00–14:00 on a Wednesday. Your own monitoring shows the affected platform hosted services totalling 91 days × 24 hours = 2,184 hours in the quarter. What is the availability *including* the excluded window, and what should your governance response be?

- A) Including the window: 4 hours ÷ 2,184 = 0.183% additional unavailability → ~99.77%, below the 99.9% target. Response: accept the exclusion since clause 7.3 permits it, but record that experienced availability was 99.77%, challenge whether preventative maintenance necessitated a peak-hours window — emergency prevention of a *predicted* failure implies schedulable lead time — and take the pattern to the contract review: exclusions that convert a breached quarter into a bonus-qualifying one merit scrutiny of both the clause and its invocation.
- B) 99.95% stands; contract clauses are not operational business.
- C) Including the window: ~99.77%; response: refuse payment and declare the supplier in breach.
- D) The exclusion is irrelevant because 4 hours is negligible.

**Correct answer: A**

**Explanation:** Arithmetic first: 4 ÷ 2,184 = 0.001832 → 0.183% additional downtime; 99.95% − 0.18% ≈ 99.77% experienced availability — below the 99.9% target, meaning the exclusion is doing decisive work: it converts a missed SLA into a comfortably-met one. Now the governance reasoning, which is where the question actually lives. The clause may be validly invoked (option C's breach declaration ignores that the contract *permits* the exclusion — refusing payment on a permitted exclusion loses the dispute and the relationship). But valid invocation does not end the matter, and option B's deference mistakes contractual truth for operational truth: your users experienced 99.77%, your reports should say so alongside the contractual figure (the dual-reporting discipline from Question 10 again), and two challenges are squarely yours to make. First, the timing: "emergency preventative" is near-oxymoronic — prevention of a predicted failure implies enough foresight to schedule, and 10:00–14:00 Wednesday is the most expensive window on the clock; whether clause 7.3 was designed for genuinely unschedulable interventions is a fair contractual question, and whether *this* one was unschedulable is a fair factual one. Second, the incentive structure: a clause that lets the supplier reclassify their way from breach to bonus will, over time, be used exactly that way, and contract review is where that gets repriced. Option D's "negligible" is refuted by the arithmetic — 0.18% is nearly double this SLA's entire quarterly failure allowance (0.1%). The transferable discipline for every supplier report you countersign: recompute the headline including all exclusions, report both figures, and treat any exclusion that flips the compliance verdict as a governance event, not a footnote. That is asset-and-configuration-level scepticism applied to contracts — verify the claimed state of what you are accountable for, in numbers, before your signature makes the claim yours.

### Preparation tips

- **Keep your estate's key figures at your fingertips.** Downtime budgets in minutes per service, current burn rates, shared-component headroom, high-impact change failure rate. Assessment fluency and management fluency are the same rehearsal.
- **Recompute one signed-off figure per week.** Take a number from a report you would normally accept — an availability aggregate, a reduction claim, a supplier SLA — and rebuild it from raw data, exclusions included. Most weeks you'll confirm it; the exceptions justify the habit.
- **Practise the decomposition reflex.** For every blended rate (change success, incident reduction, group availability), split by population before accepting the headline. Concentrated risk hides in mixed denominators.
- **Run sensitivity checks on your own business cases.** Halve the benefit estimate, double the cost: does the decision survive? Cases that survive rough handling are the ones worth your signature — and the technique is directly examinable.
- **Drill percentile literacy.** For each SLA you own, know which statistic it binds on and the current margin. Practise explaining a mean/median gap in one sentence; skewed distributions are the norm in operations, not the exception.
- **Time-box multi-step questions.** At senior level the hard questions have four or five stages. Write each stage's result down; the errors live in the transitions, and a visible chain lets you audit backwards in seconds.

### Common pitfalls to avoid

- **Comparing consumption to 100% instead of to elapsed time.** Budget health is burn rate versus time passed. "Under budget" at day 38 can still mean exhaustion by day 60.
- **Accepting blended rates.** Overall success rates, whole-estate averages and full-quarter figures are where a 7× risk concentration disappears. Decompose first, then conclude.
- **Endpoint-to-endpoint trend claims.** Two cherry-picked months can manufacture or hide any trend. Use period averages, separate seasonality, and distrust percentages anchored on convenient bases.
- **Before/after without exposure control.** Working days, usage changes, site moves and season all masquerade as fix effectiveness. Ask "per what?" and "what else changed?" before closing any problem record on a reduction figure.
- **Averaging measurements of different things.** Synthetic and real-user availability, contractual and experienced figures — report both with the gap explained. An average of two answers to two questions answers neither.
- **Letting exclusions pass unrecomputed.** Any figure that arrives with a footnote excluding something should be rebuilt inclusive. If the exclusion flips the verdict, it is a governance item, not a technicality.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment measures precision in reading, interpreting and reasoning from written material — using the document classes your role turns on: incident and problem records, change and release policies, continuity procedures, supplier contracts and reports, post-incident reviews, governance papers, and the escalation correspondence that arrives when situations have already gone wrong once.

The typical format is an online, timed test of 15 to 25 minutes: short passages followed by true/false/cannot-say judgements, best-summary selection, inference identification, argument evaluation, and clear-writing judgement. Scoring is objective and norm-referenced; at managerial levels, passages trend longer, contain deliberate tensions between documents, and reward the reader who tracks exactly what each text commits to versus what it merely invites you to assume.

For an operational control manager, verbal precision is a governance instrument. You are the escalation point, which means the documents reaching you have already been read once by someone whose reading proved insufficient — your value is the second, exact reading. You are accountable for change processes, and change governance is textual: policies, conditions, exemptions, and the definitions that decide whether a change was compliant. You sign off problem records and post-incident reviews, where a conclusion worded one notch stronger than its evidence becomes tomorrow's false institutional memory. You manage supplier relationships through contracts and reports whose every exclusion clause is a reading test with a price attached. And what you write travels with authority: an ambiguous instruction from you propagates as confident error through every team that receives it. The questions below train the habits this responsibility demands — and several deliberately practise the hardest one: refusing to let operational plausibility, sympathy, or seniority adjust what a text actually says.

The cardinal rule for true/false/cannot-say questions bears repeating even at your level — especially at your level, because experience supplies such convincing whispers: judge only from the passage. If the text neither guarantees nor contradicts the statement, the answer is "cannot say", however strongly your estate's history suggests otherwise.

### How this assessment maps to your role

- **Precise policy and procedure comprehension** maps to **Change management** and **Service management framework knowledge**: ensuring release policies, procedures and processes are applied begins with reading their conditions, definitions and exemptions exactly; ITIL-informed governance is applied through documents, not despite them.
- **Evidence-conclusion discipline** maps to **Incident management** and **Problem management**: leading investigations and signing off records means holding the line between what evidence establishes, what it suggests, and what it cannot say — in your reading and, more consequentially, in your sign-offs.
- **Cross-document reasoning** maps to **Continuity management** and **Asset and configuration management**: runbooks, change records and configuration data must be read against each other; stale or conflicting documents are operational risks your role catches.
- **Argument evaluation** maps to **Availability and capacity management** and your accountability for **preventative measures**: capacity cases, supplier claims and improvement proposals arrive as arguments whose weakest step your approval either catches or inherits.
- **Clear-writing judgement** maps to **Community collaboration**, **User focus** and **Ownership and initiative**: adapting feedback so it is effective and lasting, representing users faithfully in operational decisions, and writing instructions and reviews that carry exact meaning under pressure — accountability includes being unambiguous.

### Practice questions

**Question 1 (easy) — What a policy commits to**

Passage (release policy extract): "Releases to production may occur on any weekday. Releases affecting citizen-facing services must not occur on the last two working days of the month, when transaction volumes peak. The release manager may grant exemptions to the end-of-month restriction where a critical security fix is required."

Statement: "A release affecting a citizen-facing service can never compliantly occur on the last working day of the month."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** The restriction is explicit — but so is its exemption mechanism: the release manager may grant exemptions for critical security fixes. "Never compliantly" is therefore contradicted by the passage itself: a citizen-facing release on the last working day, under a granted security exemption, is compliant. The statement is false. The reading error this catches is absolutising a rule while skimming past its exception clause — the mirror image of the more famous error (treating exceptions as general permissions). Policies are rule-plus-exception structures, and governance-level reading means holding both: the restriction binds by default; the exemption exists, is bounded ("critical security fix"), and is gated through a named authority. As the person accountable for release policy application, both halves are yours to enforce — blocking the routine end-of-month release *and* enabling the exempted security fix — and both failures (rigidity and looseness) are policy failures. One word of the statement — "never" — decided the answer; at your level, single quantifiers usually do.

**Question 2 (easy) — Evidence versus conclusion in an incident update**

Passage (update from an incident bridge): "18:40 update: error rates on the case system returned to baseline at 18:22, eleven minutes after the network team rolled back this afternoon's routing change. The network team consider the routing change the likely cause. Application logs from the affected period are still being analysed."

Statement: "The routing change caused the case system errors."

- A) True
- B) False
- C) Cannot say

**Correct answer: C**

**Explanation:** The passage offers strong circumstantial evidence — recovery eleven minutes after rollback — and an expert team's stated *opinion* ("consider... the likely cause"), while explicitly flagging that analysis is incomplete. Opinion plus correlation plus open analysis does not equal established fact: the passage never asserts causation, so the statement is neither guaranteed (not "true") nor contradicted (not "false"). Cannot say. The senior-level relevance is in what you *do* with such updates: as escalation manager you would rightly act on the hypothesis (hold the rollback, monitor, direct the log analysis), and simultaneously refuse to let the incident record say "cause: routing change" until the analysis lands. Acting-on and asserting are different speech acts, and the discipline of keeping them separate — in bridges, updates and reviews — is what stops "likely" hardening into "confirmed" through nothing but repetition. Post-incident reviews built on prematurely hardened causes produce preventative actions aimed at the wrong mechanism; your signature is the checkpoint where that hardening is supposed to be caught.

**Question 3 (easy) — Reading a continuity test requirement**

Passage (continuity standard): "Each critical service's runbook must be tested at least every six months. A test is valid only if conducted against the production-equivalent environment and observed by a person independent of the team that maintains the runbook. Desk-based walkthroughs may supplement, but do not replace, environment tests."

The case system's runbook was tested four months ago in the production-equivalent environment, observed by the runbook team's own lead. Last month the team completed a thorough desk-based walkthrough observed by an independent quality manager. Statement: "The case system currently holds a valid runbook test under the standard."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** Test each event against the validity conditions, which are conjunctive. The four-month-old environment test: right environment, but observed by the team's own lead — the independence condition fails, so that test is invalid under the standard. The recent walkthrough: independent observer, but the standard states walkthroughs "do not replace" environment tests — so it cannot supply validity either. Neither event satisfies both conditions simultaneously; no valid test exists; the statement is false. The trap is compositional: each event satisfies one condition, and a hopeful reading merges them into compliance — but standards do not average across events; each test stands or falls whole. This is precisely the reading your runbook-testing duty ("test the runbooks to ensure that service availability is maintained") requires when reviewing assurance evidence: a schedule full of activity can still contain zero valid tests, and the reviewer who checks conditions *per event* is the one who notices before an invocation does. Note also the practical remedy the analysis hands you: the gap is one independent observer at the next environment test — cheap, specific, and schedulable this month.

**Question 4 (moderate) — Best summary of a governance paper**

Passage: "The change advisory board's remit is to assess risk, not to guarantee outcomes. Approval indicates that a change's documented risk is acceptable given its documented benefit, on the information presented. Teams remain accountable for the accuracy of what they present, and implementation teams remain accountable for executing as approved. Where a change fails despite approval, the review question is whether the failure arose from information the CAB should have probed, from inaccurate submission, or from execution divergence — each indicating a different remedy."

Which option best summarises the passage?

- A) "The CAB is accountable for change failures because it approved them."
- B) "CAB approval transfers risk acceptance, not accountability: submission accuracy stays with the proposing team, execution fidelity with the implementers, and post-failure review sorts which link failed to target the right remedy."
- C) "Change failures are usually caused by inaccurate submissions."
- D) "The CAB should probe information more thoroughly."

**Correct answer: B**

**Explanation:** The passage's architecture is a three-way accountability allocation (assessment on presented information → CAB; accuracy of presentation → proposing team; fidelity of execution → implementers) plus a diagnostic rule for failures (identify which link broke, because each implies a different fix). Option B preserves the whole structure. Option A inverts the passage's central point — approval explicitly does *not* make the CAB the owner of outcomes. Options C and D each promote one branch of the diagnostic taxonomy into a general claim the passage never makes: it presents "inaccurate submission" and "should have probed" as *possibilities to be distinguished in review*, not as findings. Summary questions at this level test structural fidelity — whether you can compress a governance text without collapsing its allocations — and the stakes are practical: this passage is exactly the text you would reach for in the awkward meeting after an approved change fails, and the manager who mis-summarises it as option A conducts a blame exercise, while the one who holds option B conducts the three-question review the framework intends. Your accountability for change processes includes being the person in the room who keeps such distinctions intact under post-failure pressure.

**Question 5 (moderate) — Inference from a supplier notification**

Passage (supplier email): "As part of our platform modernisation, the legacy reporting API your organisation uses will be deprecated on 1 March. Deprecated APIs remain operational but receive no further fixes, and are removed no earlier than twelve months after deprecation. Migration guides for the replacement API are attached. We recommend beginning migration promptly, as the replacement API's authentication model differs significantly."

Which statement is best supported by the passage?

- A) The legacy API will stop working on 1 March.
- B) The legacy API will be removed on 1 March of the following year.
- C) After 1 March, a newly discovered fault in the legacy API would remain unfixed, and removal could come as soon as twelve months later — so the safe migration window is bounded and the risk of staying grows from deprecation day, not removal day.
- D) The replacement API requires no significant changes to integrate.

**Correct answer: C**

**Explanation:** Extract what each claim would need. Option A confuses deprecation with removal — the passage says deprecated APIs "remain operational". Option B converts "no earlier than twelve months" (a floor) into a scheduled date (a fact); the passage guarantees a minimum notice, not a removal date. Option D is contradicted — the authentication model "differs significantly". Option C assembles only what the text supports: post-deprecation faults go unfixed (stated), removal is possible from month twelve (the floor read correctly), and therefore — the licensed inference — the *risk* of remaining on the legacy API begins accruing at deprecation, because from 1 March you run unsupported software with a removal clock whose earliest expiry is known but whose actual expiry is not. That final step is inference, but disciplined inference: it introduces no new facts, only the consequence of combining stated ones. This is the reading that turns supplier notices into risk register entries with correct dates — the entry reads "unsupported from 1 March; removal possible from 1 March next year", not "problem in twelve months". Sequencing your estate's migration before the *floor*, with margin, is then an availability decision your capacity planning owns. Suppliers write in modernisation language; operational accountability reads in risk language; translation between the two is precisely this exercise.

**Question 6 (moderate) — The instruction you are about to send**

A release will proceed tonight under condition that it aborts if error rates rise. You are drafting the instruction to the overnight team. Which version carries your intent with least ambiguity?

- A) "Proceed with tonight's release, but abort if things look bad."
- B) "Proceed with tonight's release. Abort criteria: sustained error rate above 2% for 10 consecutive minutes on the case system dashboard (link), measured from deployment completion. On abort: execute rollback plan RB-114, notify me regardless of hour, and record timings in the change record. If the dashboard itself is unavailable, treat as abort."
- C) "Proceed with tonight's release. Abort if error rates rise significantly. Use your judgement — you're a capable team."
- D) "Proceed with tonight's release. Abort if the error rate exceeds 2%."

**Correct answer: B**

**Explanation:** Judge each against what the overnight team must decide at 02:00 without you. Option B specifies the metric and its source (which dashboard), the threshold (2%), the persistence requirement (10 consecutive minutes — excluding transient deploy spikes that would trigger option D's bare "exceeds 2%" on a single sample), the measurement anchor (from deployment completion), the abort action (a named, presumably tested rollback plan), the communication rule (notify regardless of hour — removing the courtesy hesitation that delays escalations), the record-keeping duty, and — the mark of an instruction written by someone who has led incidents — the failure mode of the criterion itself: a blind dashboard defaults to abort, not to hope. Option A delegates the entire decision disguised as an instruction. Option C dresses the same delegation in flattery; "use your judgement" is respectful in genuinely open situations, but here *you* hold the risk acceptance and the team holds the night shift — exporting your decision to them under pressure is not empowerment, it is unowned risk. Option D is the plausible near-miss: a real threshold, but no persistence window, no source, no action, no default-on-failure — four ambiguities, each one a 02:00 phone call or a wrong guess. The principle your ownership skill implies: an instruction is complete when the recipient can execute every branch of it — including the branch where the instruction's own instruments fail — without waking you; anything less transfers your accountability downward without transferring the authority to discharge it.

**Question 7 (moderate) — Two records in tension**

Passage 1 (configuration record, updated January): "Database failover for the case system: automatic, initiated within 60 seconds of primary failure, no manual action required."

Passage 2 (post-incident review, June): "During the 12 June incident, database failover did not initiate automatically. The on-call DBA initiated manual failover 34 minutes after primary failure. Cause: automatic failover was disabled during the April storage migration and not re-enabled. Action 7: re-enable automatic failover and verify. Action owner: database team. Status at review sign-off: open."

It is September. Statement: "The case system's database failover will initiate automatically if the primary fails today."

- A) True
- B) False
- C) Cannot say

**Correct answer: C**

**Explanation:** Sequence the evidence. The January record's claim was falsified by events in April–June: automatic failover was disabled and stayed so through 12 June. The review's Action 7 exists to restore it — but its status *at sign-off* was "open", and the passage offers nothing about the intervening months. Today's state therefore depends on whether Action 7 has since been completed — which the texts do not say. Not "true" (the January record is discredited and the action was open at last report); not "false" (three months have passed and completion is entirely possible); cannot say. Both wrong answers have instructive aetiologies: "true" comes from trusting the configuration record — the exact document the incident proved stale; "false" comes from freezing the world at the review's timestamp, treating "open at sign-off" as "open forever". The operational translation is the sharpest part: "cannot say" is an *unacceptable* answer about your own estate's failover capability, and the manager who reaches it correctly on paper should hear it as an instruction in life — chase Action 7's current status, verify (not ask — verify, per the action's own wording) and fix the January record. Open post-incident actions decay precisely because their reviews are signed off and filed; your accountability for preventative measures includes being the person whose September question reopens June's action list. A configuration record contradicted by an incident and "corrected" by an open action is, until verification, a document describing an aspiration.

**Question 8 (moderate) — Argument evaluation: the outsourcing case**

Passage (from a proposal): "Our command and control centre resolved 71% of incidents without specialist escalation last year. VendorCo's managed operations centre advertises a 90% non-escalation rate. Moving our monitoring and first response to VendorCo would therefore improve our resolution performance by 19 points, freeing specialist teams. VendorCo's rate is audited and genuine."

Which is the strongest criticism of the argument?

- A) The 71% figure is probably measured wrongly.
- B) Even granting both figures as accurate, the comparison assumes the rates are commensurable — but non-escalation rate depends on incident mix, escalation policy and what counts as "resolved"; VendorCo's 90% on its portfolio does not transfer to our estate's mix, and a high non-escalation rate can even indicate under-escalation. The inference from "their rate is higher" to "our rate would become theirs" is the unsupported step.
- C) Outsourcing is always a mistake for public services.
- D) VendorCo's audit was probably not independent.

**Correct answer: B**

**Explanation:** Note what the passage pre-empts: it stipulates VendorCo's figure is "audited and genuine", which disarms attacks on the number itself (options A and D probe data quality the question has fenced off — a common assessment device to force engagement with the *logic*). The logical gap is transferability: a non-escalation rate is a joint property of the incident population, the escalation policy, and the resolution definitions — three things that differ between organisations. VendorCo's 90% describes VendorCo's mix under VendorCo's rules; nothing licenses projecting it onto your estate, and the argument's arithmetic flourish ("improve by 19 points") dresses the unsupported transfer in false precision. Option B also lands the operationally sharpest sub-point: non-escalation is not unambiguously good — a centre can inflate it by holding incidents it should escalate, which for *your* estate (where the specialists are one flight of stairs away and the services are citizen-critical) may be exactly the wrong optimisation. Option C substitutes ideology for analysis. This evaluation pattern — grant the premises, attack the transfer — is the highest-yield skill for reading vendor cases, benchmark comparisons and "industry standard" claims, all of which reach your desk because you control the budget line they want. The follow-up a strong manager writes in the margin: "what is VendorCo's rate *on an incident mix like ours*, under *our* escalation policy, and who bears the cost when under-escalation meets a SEV1?"

**Question 9 (moderate) — False versus cannot-say at the contract boundary**

Passage: "Under the support contract, SEV1 incidents must receive a supplier response within 15 minutes, 24/7. On Saturday at 03:10 the centre raised INC-7201 with the supplier as SEV1. The supplier's first response arrived at 03:52."

Statement: "The supplier breached the support contract."

- A) True
- B) False
- C) Cannot say

**Correct answer: A**

**Explanation:** Compute against the rule: response due within 15 minutes of 03:10, i.e. by 03:25; first response 03:52 — 27 minutes late. The obligation is unconditional in the passage ("must... 24/7"), the incident was raised as SEV1, and the response time is stated. Every element of a breach is on the page: the statement is true by deduction. This question earns its place as a discipline check in the *other* direction: after several "cannot say" answers, experienced candidates start manufacturing uncertainty — "perhaps the contract has an exclusions schedule", "perhaps the SEV1 grading was later disputed", "perhaps 'response' is defined non-obviously". All possible in life; none in the passage — and cannot-say discipline cuts both ways: you may not import doubt any more than you may import knowledge. When a text supplies rule, trigger and violating fact, the deduction closes. The paired operational lesson: in a real dispute, those imported doubts are exactly what the supplier's account manager will raise, which is why your incident records — raised-as grading, timestamps, response definitions — are drafted to make the deduction closable on documents alone. You enforce contracts with the evidence your centre's record-keeping disciplines captured months before anyone knew which incident would matter.

**Question 10 (hard) — Reconciling three documents under supersession**

Passage 1 (standing change policy): "All production changes require CAB approval no less than 48 hours before implementation."

Passage 2 (emergency procedure, referenced by the policy): "Emergency changes — those addressing active or imminent service failure — may be approved by the duty operational control manager, with full documentation completed within 24 hours after implementation and retrospective CAB review at its next sitting."

Passage 3 (email from the head of operations, Tuesday): "Following this morning's board discussion of audit findings, with immediate effect all uses of the emergency change route require my personal approval in addition to existing controls, pending the review of emergency change governance. Standing policy is otherwise unchanged."

On Thursday night, an active service failure requires an immediate production change. The head of operations is uncontactable. Statement: "The duty operational control manager can tonight authorise the change in full compliance with the applicable rules."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** Layer the instruments. The standing policy's 48-hour rule is relieved by the emergency procedure for active failures — under Passages 1 and 2 alone, tonight's authorisation by the duty manager would be fully compliant. But Passage 3, the most recent authority, adds a conjunctive control: emergency route usage now requires the head of operations' personal approval *in addition to* existing controls, with immediate effect and no stated exception for unavailability. Tonight, that approval is unobtainable; therefore full compliance with all applicable rules is not achievable by the duty manager alone. The statement is false. The tempting "cannot say" imagines implicit exceptions ("surely the head would want the service saved") — but that is imported charity, not text; the email's only softening is temporal ("pending the review"), not situational. Now the part beyond the test, which your level is paid for: false-on-compliance does not mean frozen-in-action. The professional course tonight is to act on the operational imperative with maximum procedural honesty — attempt and log the contact attempts, take the nearest available senior approval as best-endeavour substitute, implement, document within the emergency procedure's 24 hours, and self-report the deviation to the head of operations and the CAB at first light with the rationale. Knowingly deviating *visibly and accountably* is a governance event survivable by honest process; deviating silently, or letting a citizen-facing service fail while compliant, are the two genuinely career-defining failures. And Friday's second duty: flag to the governance review that Passage 3, as drafted, contains no unavailability provision — the gap you just fell through is a defect in the control, and the person who found it owes the system the fix. Reading rules exactly, acting under them honestly, and improving them afterwards: all three are the job.

**Question 11 (hard) — The post-incident review's quiet overstatement**

Passage (draft post-incident review conclusion, submitted for your sign-off): "The outage was caused by the failed disk controller. The incident demonstrates that our monitoring performed well, generating the initial alert within 90 seconds of failure. Staff response followed procedure throughout. No process changes are required; the hardware has been replaced and the risk is closed."

Earlier sections of the same review record: the alert fired at 04:31; it was acknowledged at 05:14 because the overnight alert routing sent it to a mailbox rather than the on-call phone (a known configuration issue logged three weeks earlier); service restoration began at 05:20.

Which criticism of the conclusion is most important?

- A) The disk controller cause is probably wrong.
- B) "Monitoring performed well" is half-true and the conclusion's closure claim doesn't follow: detection was fast (90 seconds) but the alert then sat unacknowledged for 43 minutes due to a *known, logged* routing defect — so "staff response followed procedure" may be literally true while the procedure's delivery mechanism failed, and "no process changes are required" is contradicted by the review's own body. The risk closed is the hardware instance; the routing defect — which turned a 90-second detection into a 49-minute response — remains open and pre-dates the incident.
- C) The review is too short.
- D) The replacement hardware should have been a different model.

**Correct answer: B**

**Explanation:** Read the conclusion against the review's own evidence — the defining act of sign-off. The causal claim (disk controller) is consistent with the body; options A and D attack it without textual basis. The overstatement is in the evaluative claims: "monitoring performed well" merges two separable stages — detection (excellent: 90 seconds) and notification (failed: 43 minutes in a mailbox) — and the merged praise buries the failed stage. "Staff response followed procedure" deserves particular attention as a sentence-type: it may be perfectly true *and* is doing exculpatory work that redirects attention from the system defect to the vindicated humans — precisely the pattern by which reviews stay comfortable and organisations stay unimproved. And "no process changes are required" is not merely optimistic but *internally contradicted*: the body documents a known, logged, three-week-old routing defect that converted fast detection into slow response; the process change required is specific, cheap and already half-specified in the earlier log entry. The closure claim then closes the wrong risk — the hardware instance rather than the response-path defect that will attend every future 04:31 alert of any cause. Option B assembles all of this; option C mistakes length for quality. The sign-off habit this trains: for every evaluative sentence in a conclusion ("performed well", "followed procedure", "no changes required"), locate its evidence in the body and check the sentence's *scope* matches the evidence's scope. Conclusions drift wider than their evidence under social pressure to close cleanly — and the reviewer who narrows them back is doing prevention, one sentence at a time, which is your accountability in its most literal textual form.

**Question 12 (hard) — Precision under modal and temporal load**

Passage (from the major incident procedure): "The duty manager must declare a major incident when two or more citizen-facing services are simultaneously degraded, or when any single citizen-facing service is fully unavailable for longer than 15 minutes. The duty manager may declare a major incident at their discretion in other circumstances. Once declared, a major incident may be stood down only when all triggering conditions have ceased and the duty manager has confirmed stability for 30 continuous minutes. Declaration obligations are assessed on service status, not on incident ticket status."

At 11:00, the licensing portal (citizen-facing) becomes fully unavailable. At 11:10, the case system (citizen-facing) becomes degraded. At 11:13, the portal recovers fully; the case system remains degraded. No declaration has yet been made. Statement: "As of 11:14, the duty manager is in breach of the mandatory declaration duty."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** Test each mandatory trigger against the timeline — carefully, because both *almost* fired. Trigger one: two or more citizen-facing services *simultaneously degraded*. From 11:10 to 11:13, the portal (fully unavailable — a fortiori degraded) and the case system (degraded) overlapped: the condition was *met* during those three minutes. But re-read the obligation: "must declare when..." — at 11:14, the simultaneity has ceased (portal recovered at 11:13). Was the duty manager obliged to declare *during* 11:10–11:13, such that 11:14 finds them in breach? Three minutes is a window in which a reasonable declaration process could barely begin; more decisively, examine trigger two: full unavailability "for longer than 15 minutes" — the portal was fully down from 11:00 to 11:13, thirteen minutes: never crossed. So trigger two never fired, and trigger one fired for a three-minute window that had already closed by the assessment time. The strict question — in breach *as of 11:14* — turns on whether a duty that crystallised at 11:10 survives its condition's cessation unperformed. The passage says "must declare when [conditions hold]": the natural reading is a duty operative while its conditions obtain, and the stand-down clause (conditions ceased) reinforces that the procedure tracks *current* status — as does the final sentence anchoring assessment to service status. At 11:14 the mandatory conditions do not hold and the 15-minute clock never completed: no subsisting mandatory duty is being breached — false. (The discretionary power remains, and given a case system still degraded and a portal that just returned, a prudent duty manager might well use it — but "may" cannot ground a breach.) If you answered "true", you likely back-dated the three-minute window into a standing obligation; if "cannot say", you treated a genuinely computable timeline as ambiguous. The examinable skill is running modal words (must/may), temporal conditions (simultaneously, longer than 15 minutes, 30 continuous minutes) and an assessment timestamp *together* without letting any of the three slip — which is, precisely, what reading your own major incident procedure at 11:14 on a bad morning requires. Managers who have rehearsed this arithmetic declare correctly under pressure; those who haven't either over-declare (eroding the signal) or under-declare (eroding the response). The procedure is a text; the 11:14 decision is a reading.

### Preparation tips

- **Re-read your own governing documents as an examiner.** Take your actual major incident procedure, release policy and one supplier contract; for each, extract the definitions, the modal verbs, the temporal conditions and the exception clauses. Most questions at this level are your own documents wearing disguises.
- **Practise scope-checking evaluative sentences.** In the next review or report you sign, underline every "performed well", "followed procedure", "no action required" and trace each to its evidence. Sentence-scope versus evidence-scope is the highest-yield sign-off discipline.
- **Drill the grant-the-premise attack.** For one vendor claim or business case a month, accept every number as true and hunt only the inferential transfer. It sharpens argument evaluation faster than data scepticism does.
- **Time-order multi-document questions before judging.** Date every passage, establish supersession, then reason. The reflex of building the instrument stack first prevents both anchoring errors.
- **Write one zero-ambiguity instruction per week.** Threshold, source, persistence, action, notification rule, and the criterion's own failure mode. Then ask the recipient what they would do in each branch — their answer audits your writing.
- **Keep the two-way discipline on cannot-say.** Import neither knowledge nor doubt. When rule, trigger and fact are all on the page, close the deduction; when any is absent, hold the line.

### Common pitfalls to avoid

- **Absolutising rules past their exception clauses — or vice versa.** Policies are rule-plus-exception structures; governance reading holds both. "Never" and "always" in a statement are invitations to re-check the exemption paragraph.
- **Letting "likely cause" harden into "cause" through repetition.** Bridges and updates repeat hypotheses; records must not promote them. Your sign-off is the checkpoint.
- **Merging separable stages under one verdict.** "Monitoring performed well" covering both detection and notification; "the test passed" covering both procedure and luck. Split stages before evaluating.
- **Compositional compliance.** Two events each satisfying half a standard's conditions do not sum to compliance. Check conditions per event, per test, per approval.
- **Reading floors as schedules.** "No earlier than twelve months" is a minimum, not a date. Risk begins at deprecation, not at removal.
- **Manufacturing doubt to avoid a verdict.** Imported "perhapses" are as undisciplined as imported facts. When the passage supplies everything a conclusion needs, deliver the conclusion — on tests, and in the meetings where your reading is the decision.

## Workplace job-specific situational judgement assessment

### About this assessment

A situational judgement assessment (SJT) presents realistic workplace scenarios and asks you to evaluate the effectiveness of possible responses — selecting the most effective, the least effective, ranking, or rating each independently. Scoring compares your judgements against those of experienced practitioners and validated competency frameworks; there are rarely perfect options, only better and worse resolutions of genuine tensions.

The typical format is 10 to 20 scenarios over 20 to 40 minutes. At managerial levels, the scenarios shift character: less "what should you do?" and more "what should you do *about what others are doing*?" — directing without micromanaging, holding standards without breaking people, escalating upward, deciding under authority gaps, and absorbing pressure without passing it on amplified. The response options are typically all plausible; discrimination happens at the level of second-order effects — what each response teaches the team, what it does to the record, what precedent it sets.

For an operational control manager, the SJT maps onto the core of the role with uncomfortable fidelity. You are accountable for day-to-day IT operations and act as the escalation point — meaning your working life *is* a situational judgement test, administered at speed, with consequences. The dilemmas below are drawn from your role's actual territory: leading incident investigations where seniors want answers faster than evidence arrives; holding change and release discipline against delivery pressure; managing runbooks and continuity when tests reveal inconvenient truths; being on call 24/7 with authority that sometimes exceeds your information and information that sometimes exceeds your authority; team dynamics surfaced by Agile health checks; and the user-focus calls where operational convenience and citizen outcomes pull apart. Practising these calmly, with full reasoning, is rehearsal for making them well at 03:00 — and for explaining them at 09:00.

A calibration note for your level: assessors consistently reward responses that keep accountability where it belongs (including with you), keep records truthful, convert pressure into structured action rather than transmitted stress, address behaviour directly before escalating, and protect users first when goods conflict. They consistently penalise heroics that bypass process, delegation that abandons, deference that falsifies, and any resolution of tension achieved by making the record say what reality doesn't.

### How this assessment maps to your role

- **Incident leadership dilemmas** map to **Incident management** and **Ownership and initiative**: leading investigations under pressure, owning outcomes you didn't personally cause, and being accountable for the calls made on your bridge.
- **Change and release pressure scenarios** map to **Change management**: holding release policies against urgency, seniority and plausible exceptions — and knowing when the emergency route is the discipline, not the exception to it.
- **Continuity and assurance dilemmas** map to **Continuity management** and **Asset and configuration management**: acting on inconvenient test results, refusing comfortable paper compliance, and keeping the estate's records true.
- **Team and feedback scenarios** map to **Community collaboration**: adapting feedback so it is effective and lasting, using health checks honestly, and repairing team dynamics you could more easily ignore.
- **Escalation and governance scenarios** map to your position as **escalation point** and your **service management framework knowledge**: managing upward honestly, deciding under authority gaps, and treating process as something you steward rather than merely obey.
- **User-outcome dilemmas** map to **User focus** and **Availability and capacity management**: championing user needs against operational convenience, and spending availability wisely when something must give.

### Practice questions

**Question 1 (easy) — The confident wrong answer on your bridge**

Ninety minutes into a SEV1, your most experienced engineer announces on the bridge: "It's the load balancer — I've seen this exact pattern before. I'm restarting it now." You have seen the evidence build differently: the database connection metrics point elsewhere, and a load balancer restart would drop all current sessions, worsening impact if wrong. The engineer is already typing. What is the most effective response?

- A) Let it proceed — they have twenty years' experience and challenging them publicly would undermine them.
- B) Intervene now, directly and without heat: "Hold the restart — connection metrics don't fit the load balancer pattern; walk me through what you're seeing first." Make the decision explicitly yours as incident lead, weigh their pattern against the metrics openly, and choose the next diagnostic step that discriminates between the two hypotheses.
- C) Overrule them silently by revoking their access to the load balancer mid-incident.
- D) Allow the restart but note your disagreement in the incident record for the review.

**Correct answer: B**

**Explanation:** Leading the investigation — your incident management skill's exact wording — means owning the decision layer: hypotheses are welcome from everyone; *actions with blast radius* go through the lead. Option B intervenes at the right altitude: it stops the irreversible action (session-dropping restart) before it fires, it does so by engaging the engineer's evidence rather than their status ("walk me through what you're seeing" treats twenty years' experience as data, not as noise), and it converts the disagreement into the professionally correct move — the next test that *discriminates* between hypotheses, rather than the next action that expresses one. Option A inverts the accountability structure: you, not the engineer, will own the worsened incident, and deference that spends user sessions to spare a colleague's feelings serves neither. Option D is accountability theatre — permitting an action you believe wrong while papering your dissent is the worst of both: the users get the harm, the record gets your alibi, and the engineer learns nothing until the review ambushes them. Option C solves a judgement disagreement with an authority weapon, humiliating a senior colleague mid-crisis and teaching the whole bridge that disagreement is dangerous. The second-order effects decide this, as they usually do at your level: option B teaches the team that the bridge runs on evidence, that seniority is heard but not obeyed, and that the lead will absorb the friction of stopping a confident colleague — which is exactly the culture that makes the *next* incident safer.

**Question 2 (easy) — Pressure from above during the incident**

Two hours into a citizen-facing outage, a director messages you directly: "The minister's office is asking. Tell me it's fixed in 30 minutes." Honest status: a fix is being tested; realistic restoration is 60–90 minutes; a rushed deployment of the untested fix could restore in 20 minutes or could corrupt data and double the outage. What is the most effective response?

- A) Commit to 30 minutes and push the untested fix — the pressure is real and the fix will probably work.
- B) Reply with the honest position, structured for their need: current state, the tested path (60–90 minutes), the rushed path and its data-corruption risk, your recommendation (tested path), and a committed update cadence — then hold the recommendation unless they explicitly direct otherwise at their accountability level.
- C) Stop answering the director until the incident is resolved; incident leads shouldn't be distracted.
- D) Tell the director 60–90 minutes but privately instruct the team to try the rushed fix in parallel, hedging both.

**Correct answer: B**

**Explanation:** The director's message is pressure, but inside it is a legitimate need: something true and useful to send upward. Option B meets the need without transmitting the pressure downward into engineering risk: it gives the director exactly what a minister's office conversation requires (state, options, risks, recommendation, next update), it keeps the risk decision at the right level — you recommend, and if a director knowingly directs the risky path, that is a decision made with accurate information at an accountability level entitled to make it — and the update cadence converts future chasing into scheduled communication, protecting the bridge. Option A makes you the author of a commitment you cannot keep and a risk you didn't need to take; when the rushed fix corrupts data, "the director was under pressure" will not be the finding — "the incident lead deployed an untested fix" will. Option D is the subtle trap at this level: it looks like sophistication, but "privately instruct... hedging both" means running the risky path *without* the director's informed authorisation while telling them you aren't — dishonesty upward plus unauthorised risk, wrapped in the appearance of prudence (and "in parallel" is operationally false comfort: the rushed fix's failure mode — data corruption — doesn't stay in its lane). Option C mistakes stonewalling for focus; unmanaged senior stakeholders escalate their interruptions. The template B models is the incident lead's core upward skill: absorb pressure, return structure. Directors amplify what you send them — send them decision-grade honesty.

**Question 3 (easy) — The health check surfaces something real**

Your team's Agile health check returns a sharp drop on "safe to raise problems", with anonymous comments: "mistakes get remembered here" and one specific: "when the monitoring gap was found last month, the first question was whose fault it was." You recall asking exactly that question, intending it as diagnosis, not blame. What is the most effective response?

- A) Announce that the health check shows a perception problem and that people should feel safer, effective immediately.
- B) Treat the data as accurate about impact regardless of intent: acknowledge to the team, specifically, that the "whose fault" question landed as blame and that you're changing how you ask ("what let this happen?" not "who"); change the visible behaviour in the next real incident; and re-check the measure next cycle rather than declaring it fixed.
- C) Investigate the anonymous comments to identify who wrote them so you can address their concerns individually.
- D) Quietly stop asking fault-related questions but say nothing, letting behaviour change speak for itself.

**Correct answer: B**

**Explanation:** Your community collaboration skill names this precisely: identify issues through Agile health checks and *help stimulate the right responses* — and the right response to psychological-safety data has a known shape. Option B does the three things that actually move the measure: it names the specific behaviour without defending the intent (intent is real but irrelevant to impact — "I meant it diagnostically" is true and repairs nothing), it makes the replacement behaviour public and specific (so the team can hold you to it, which is itself a safety signal), and it treats the next real incident — not the announcement — as the test, with the follow-up measurement honestly deferred until evidence exists. Option A is the classic inversion: instructing people to feel safe is itself unsafe-making, and it locates the problem in their perception rather than your behaviour. Option C is the catastrophic option dressed as diligence: de-anonymising a safety survey destroys the instrument permanently and confirms the comments' thesis in one stroke — no future health check in your team will contain a true sentence. Option D gets the behaviour right and wastes it: unannounced change reads as coincidence, forfeits the acknowledgement that does half the repair work, and leaves the team's model of you unchanged. The leadership point the scenario carries: at your level, feedback about your impact *is* operational data about the team's incident-reporting reliability — a team that hides mistakes from you is a team whose incidents you learn about late — so the health check drop is not an HR matter adjacent to operations; it is an early-warning system for your estate, and B is you repairing your own telemetry.

**Question 4 (easy) — The runbook test you'd rather not have seen**

Three weeks before a major planned migration that depends on the continuity runbook, your scheduled test fails: failover took 26 minutes against a 20-minute abort threshold (as in your cognitive section), and two runbook steps referenced infrastructure that no longer exists. The migration sponsor, hearing a "test issue", says: "We can't slip the date — just note it and we'll fix the runbook after migration." What is the most effective response?

- A) Agree — the runbook is only needed if something goes wrong, and slipping a major date over a test is disproportionate.
- B) Refuse to discuss the date and simply declare the migration blocked.
- C) Separate the findings from the date decision: fix the two stale steps now (days, not weeks), re-test the failover to determine whether 26 minutes is capacity drift or one-off, and bring the sponsor a quantified risk position — "migration with a runbook proven at X minutes" versus the date cost of fixing it — so the go/no-go is made on evidence at the sponsor's accountability level, with your recommendation attached.
- D) Fix the runbook quietly and re-date the test report so the migration paperwork shows a clean pass.

**Correct answer: C**

**Explanation:** The sponsor's framing — "note it and fix after" — treats the runbook as migration paperwork; your continuity management skill (manage the runbooks, *test* the runbooks to ensure availability is maintained) knows it as the migration's parachute: the artefact you need exactly and only if the migration goes wrong, which is why testing it *before* is the whole point. Option C converts the confrontation into a decision process: the cheap fixes proceed immediately (stale steps are days of work — much of the tension dissolves on inspection), the ambiguous finding gets the discriminating re-test (26 minutes might be a transient or might be data-growth drift — you don't know yet, and the difference decides everything), and the date question returns to the sponsor as a *quantified* choice with your recommendation — which respects that date-versus-risk trade-offs at migration scale belong to the sponsor, made on true information, while the truth of the information belongs non-negotiably to you. Option A accepts flying without the parachute because unpacking it is inconvenient. Option B may end in the right place but by the wrong route: "blocked" without the evidence path invites overrule and casts you as obstruction; C's version of the same firmness is overrule-resistant because it prices the options. Option D is the disqualifying answer: a re-dated test report is a falsified assurance record — if the migration then fails and the runbook fails with it, the record shows continuity was "proven" by a document you forged, and every future assurance from your centre becomes suspect. Note the general pattern for sponsor pressure: never argue adjectives ("risky" vs "fine"); bring the re-test, the number, and the priced options. Sponsors overrule adjectives; they rarely overrule arithmetic they must sign.

**Question 5 (moderate) — Emergency change authority, 02:00, imperfect information**

02:00, on call. A failing certificate will expire at 06:00, taking down the licensing portal's citizen login. The fix is a certificate replacement — routine in daylight, but the engineer available tonight has never performed it on this system; the specialist who has is unreachable. The emergency change route is available to you. Rollback is documented but untested for this path. If nothing is done, a guaranteed 4+ hour outage begins at 06:00, into the morning peak. What is the most effective response?

- A) Do nothing until the specialist surfaces — an unpractised change at night is worse than a predictable outage.
- B) Authorise the emergency change now: have the engineer walk the documented procedure with you on the call as second pair of eyes, checkpoint by checkpoint, with an explicit pre-agreed stop-and-revert rule at each stage, timed to leave a revert-and-retry window before 06:00; document the risk decision and your reasoning in the emergency record as you go.
- C) Authorise the engineer to proceed alone and quickly — process ceremony wastes the hours you have.
- D) Wake the head of operations to make the call, since the risk decision exceeds on-call authority.

**Correct answer: B**

**Explanation:** Frame it as the risk comparison it is. Path one (option A): a *certain* multi-hour citizen-facing outage starting at peak — the worst outcome on the table, chosen deliberately. Path two: a routine-in-daylight procedure, documented, performed by a competent-if-unfamiliar engineer, four hours before the deadline. The risk of path two is real but *shapeable*, and option B shapes it with exactly the controls a senior operational manager carries in their kit: paired execution (you on the call as checkpoint reader — not because you'll out-tech the engineer, but because read-along verification catches the skipped-step errors unfamiliarity produces), staged stop-and-revert rules agreed *before* stress arrives, timing that preserves a full revert-and-retry window before the hard deadline, and contemporaneous documentation of the risk decision — which is what "be on call 24/7 and be allowed to address issues across IT operations" means when it matters: the authority is yours, exercised visibly. Option A fails the comparison it claims to make: it prefers certain harm to managed risk, and "wait for the specialist" is a plan whose success condition you don't control. Option C takes the right path and strips its controls — speed is not what the four hours are for; the hours are the *budget for careful execution*, and an unfamiliar engineer alone at 02:00 is precisely how documented procedures produce undocumented outcomes. Option D deserves care: escalation is not wrong, but this decision — an emergency change, within the emergency route, within your delegated authority, with a clear risk asymmetry — is what your role *exists* to decide at 02:00; waking the head of operations to make it transfers nothing but the hour of the phone call, and a pattern of up-delegating decisions inside your authority teaches the organisation your authority is decorative. (Contrast Question 10 of the verbal section, where an added control genuinely removed the authority — the difference is exactly what you're paid to read.) Inform the head at 07:00 with the record; wake them only when the decision genuinely exceeds you.

**Question 6 (moderate) — The team lead gaming the change classification**

Reviewing change statistics (as in your numeric section), you find one delivery team classifies a suspiciously high share of its changes "low-impact", avoiding CAB review; two of last quarter's majors trace to that team's "low-impact" changes. The team lead, when you raise it, is candid: "The CAB adds a week. We're under delivery pressure you don't see, and honestly, most of our changes are fine." What is the most effective response?

- A) Report the team lead to their director for process circumvention with the incident evidence attached.
- B) Tighten enforcement: require your personal countersignature on all of that team's classifications until further notice.
- C) Engage both halves of what the lead just told you: the classification gaming stops — the two majors are the non-negotiable evidence, and you'll audit classifications against criteria for a period — and simultaneously take the "CAB adds a week" problem seriously as a process defect: examine whether standard changes, pre-approved patterns, or a faster CAB lane can give compliant changes a quicker path, and involve the lead in designing it.
- D) Accept the explanation — delivery pressure is real and most changes are indeed fine.

**Correct answer: C**

**Explanation:** The lead has handed you a diagnosis wrapped in a confession: the control is being evaded *because it is expensive*, and evasion will migrate to whatever route stays expensive. Option C runs both repairs the situation actually contains. The enforcement half is non-optional — two majors trace to the evasion, the classification criteria exist precisely so teams cannot self-certify away scrutiny, and the audit period makes the boundary concrete; your accountability for ensuring release policies "are applied" is not discharged by sympathy. But the process half is what makes the enforcement stick: if the CAB genuinely adds a week to changes that need two days of scrutiny, the *process* is generating the evasion pressure, and ITIL's own toolkit (standard change models, pre-approved patterns, differentiated lanes) exists for exactly this — service management framework knowledge as your summary means it: knowing the framework well enough to fix its application, not just enforce it. Involving the lead in the redesign converts your most sophisticated process-evader into a co-author of the compliant fast path — evaders know where the friction lives. Option B is enforcement-only: it works for a month, bottlenecks on you, teaches the team that compliance means surveillance, and leaves the week-long queue generating pressure that will find the next gap. Option A escalates before managing — the lead was candid with you; answering candour with a director report teaches every team lead to stop being candid, and it exports a problem that is squarely within your remit (you *are* the escalation point; this is the class of issue that stops with you). Option D accepts a control failure because its explanation was sympathetic — the two majors already refute "most of our changes are fine" as a governance standard. The pattern for control-evasion scenarios generally: enforce the boundary *and* fix the incentive, in that order, publicly linked — either half alone regenerates the problem.

**Question 7 (moderate) — What the user data says versus what operations wants**

A proposal from your own operations team would consolidate two overnight maintenance windows into one longer monthly window, 01:00–05:00 — operationally cleaner, fewer change collisions, easier staffing. User research data, which the user researcher flags to you directly, shows the affected service has a small but dependent overnight user population: shift workers and carers filing time-sensitive applications, disproportionately vulnerable users, for whom 01:00–05:00 is not dead time. The operations team's view: "It's 2% of traffic. You can't run operations around 2%." What is the most effective response?

- A) Approve the consolidation — 98% of users benefit from the improved stability, and 2% is a rounding error.
- B) Reject the consolidation — vulnerable users must never be affected by maintenance.
- C) Take the research seriously as design input rather than veto: work with the researcher to characterise the 2% (who they are, what they need mid-window, what fails hard versus degrades), then redesign the proposal against those needs — read-only mode during the window, deferred-submission queuing, a shorter hard-outage core inside a longer degraded window, or scheduling against observed overnight usage troughs — and bring the CAB a version whose user impact is designed, measured and honestly stated.
- D) Approve it but ask the communications team to notify overnight users in advance.

**Correct answer: C**

**Explanation:** Your user focus skill at this level is explicit and unusual: *collaborate with user researchers, represent users internally, explain the difference between user needs and user desires, champion research to focus on all users* — and "all users" is doing heavy lifting here, because the 2% case is exactly where user focus is either real or decorative. Option C is that skill operationalised. The move that matters is treating the research as *design input*: the operations team has framed a binary (consolidate vs don't) in which 2% loses to staffing convenience, but the researcher's data dissolves the binary — once you know *what* the overnight users need (submission that doesn't vanish; confirmation that queues; not necessarily full service), the engineering options multiply, and most of them (deferred-submission queuing, read-only plus queue, a 90-minute hard core in a 4-hour soft window) cost days of work, not the proposal. The percentage arithmetic deserves its own correction, and a manager who can make it lands the point without piety: 2% of traffic is not 2% of *harm* — a failed 03:00 application from a carer with a deadline is not offset by smoother maintenance for daytime users who never notice; impact-weighting is the same discipline your numeric section applied to availability aggregates, applied to people. Option A performs that error at decision level. Option B performs the opposite error — "never" is not a policy, and unpriced vetoes teach operations to stop showing you research. Option D is notification-as-absolution: telling vulnerable users in advance that the service they depend on will be down does not make it less down; communication is a component of C's design, not a substitute for it. Second-order effect, as ever: C teaches your centre that user research changes designs — which is the only thing that keeps researchers flagging data to the escalation point at all.

**Question 8 (moderate) — Your predecessor's paper compliance, discovered**

Newly confident in the role, you discover that the quarterly asset verification your centre has certified for the past two years was, under your predecessor, largely performative for one datacentre: records "confirmed" without physical or scan verification. Your first genuine verification finds 6% of that site's records wrong — including two decommissioned servers still listed as hosting a service's failover capacity. Nothing has yet failed. The certifications carry your centre's name; the predecessor is now a peer in another division. What is the most effective response?

- A) Fix the records quietly going forward; the past certifications are the predecessor's problem and raising them creates noise without benefit.
- B) Correct the records, then disclose the finding through your governance chain: the certifications were unreliable for that site and period, here is the verified current state, here is the control change preventing recurrence (verification method now recorded per item), and here is the risk assessment of the two failover-capacity errors — factually, without prosecuting the predecessor.
- C) Report the predecessor to their current division head for historical falsification before doing anything else.
- D) Re-certify the current quarter accurately but leave the historical record untouched and unmentioned, since amending history is complicated.

**Correct answer: B**

**Explanation:** Two questions hide inside this scenario; separating them is the judgement being tested. Question one — the estate: records are wrong *now*, and two of the errors are the dangerous kind (phantom failover capacity is a continuity failure that reveals itself only during an invocation — the worst possible discovery time; compare the failover question in your verbal section). Correction and verification are urgent and unambiguous. Question two — the certifications: documents bearing your centre's name assert verifications that didn't happen, and downstream consumers (audit, security, continuity planning) may have *relied* on them: the two-year unreliability is information those consumers currently lack, and only disclosure restores their decisions to an accurate footing. Option B handles both, and its manner is the senior part: disclosure *through the governance chain*, framed as finding-plus-fix-plus-control-change, without prosecuting the predecessor — because the organisational need is reliable records and a repaired control, not a villain, and because "factually, without prosecuting" is also what protects you if the history later surfaces another way (it usually does; the question "when did the current manager know?" then has a good answer). Option A makes the past *your* problem in the worst way: from the moment of discovery, silence converts the predecessor's performative compliance into your knowing concealment — every quarter you don't disclose, you re-certify the reliability of documents you know are unreliable. Option D is A with better paperwork. Option C inverts B's priorities: it leads with the person and defers the estate — the two phantom failover entries stay in the records while a personnel process spins up — and routing it to *their division head* rather than your governance chain converts a controls finding into an inter-divisional accusation, maximising heat and minimising repair. The durable principle, which this role meets repeatedly: when you inherit a falsified record, the falsification stopped being survivable-by-silence the day you found it; disclosure with a fix attached is the only version of this story that ages well.

**Question 9 (moderate) — The specialist bottleneck during a long-running problem**

A cross-service problem investigation (intermittent authentication timeouts, six weeks running) has stalled: the one identity specialist whose analysis it needs keeps deprioritising it for project work, his project manager protects his time fiercely, and your analysts' consultation requests get 15-minute fragments that restart from scratch each time. Meanwhile the timeouts continue at low frequency across three services. What is the most effective response?

- A) Instruct your analysts to keep requesting time and copy you into the requests for weight.
- B) Escalate to the specialist's project manager's director, citing the stalled problem record.
- C) Restructure the ask before escalating the priority: have your analysts package the investigation state into a one-page evidence brief with three specific technical questions, request a single 90-minute working session instead of fragments, and take the *priority* conflict — project delivery versus a cross-service problem affecting three estates — to the project manager as an explicit trade-off with the incident data attached; escalate jointly only if the trade-off can't be agreed at that level.
- D) Have your analysts work around the specialist and attempt the identity analysis themselves from documentation.

**Correct answer: C**

**Explanation:** Diagnose the stall before treating it: the pattern "15-minute fragments restarting from scratch" is not only a time-quantity problem — it is an *ask-structure* problem. Fragmented consultation without preserved state wastes whatever time is granted; the specialist experiences the requests as bottomless, which feeds the project manager's protection, which shrinks the fragments — a loop. Option C breaks the loop at both points. The evidence brief plus three specific questions plus one working session converts the ask from "lend us your specialist indefinitely" into "answer these, once, well" — cheaper for the lending side, dramatically higher-yield for yours, and it is exactly what your problem management skill's phrase "effectively consult specialists" means: consultation is a discipline of the *consumer's* preparation, not just the provider's availability. The priority half goes to the right level with the right shape: the project manager is not wrong to protect delivery — they are pricing one side of a trade-off whose other side (three services, six weeks, incident data) they haven't seen; showing them the full trade-off respects their role and usually resolves it, and the jointly-escalate fallback keeps the relationship intact if it doesn't. Option A adds weight without restructuring the ask — heavier fragments are still fragments. Option B escalates a conflict two levels before anyone at level one has seen both sides of it; you may win the specialist and lose the relationship economy that every future cross-team problem depends on. Option D has a defensible kernel — analysts stretching their understanding — attached to an operational error: six weeks of intermittent cross-service authentication timeouts is precisely the class of problem where documentation-taught improvisation produces confident wrong fixes; the specialist exists because the failure modes are non-obvious. Sequence C's two moves in order: restructure the ask first — a shocking fraction of "we can't get specialist time" dissolves when the ask becomes answerable — then price the priority conflict honestly at the level that owns it.

**Question 10 (hard) — Least effective: the morning after your own misjudgement**

Last night, on call, you declined to invoke the continuity runbook for a degraded storage array, judging the degradation self-limiting. It wasn't: the array failed at 05:00, and the delayed failover extended a citizen-facing outage by roughly 40 minutes into the morning peak. Your judgement was defensible on the information you had at 01:30 — but a precursor signature your own team documented two months ago (and which you signed off) was in the monitoring history, unlooked-at. The post-incident review is tomorrow; you will chair it, as you chair all of them. Which response is LEAST effective?

- A) Present your 01:30 decision and its information basis fully in the review, including the missed precursor check, and let the timeline show the 40-minute extension plainly; ask a peer to chair the session given your decision is in scope.
- B) Chair the review yourself as usual, but present your own decision with the same evidence standards you apply to others, inviting the team to probe it.
- C) Present the decision as sound risk management that simply encountered bad luck, keep the precursor signature out of the timeline as a distracting detail, and focus the review on the storage vendor's firmware defect as root cause.
- D) Before the review, tell your own manager directly: the decision, the missed precursor, the 40-minute cost, and the process change you propose (precursor check added to the on-call decision aid).

**Correct answer: C** (least effective)

**Explanation:** Rate all four. Option A is the strongest: full presentation including the miss, and — the subtle senior move — handing the chair to a peer, because a review whose chair's own judgement is in scope has a structural conflict no amount of personal integrity fully cures; participants probe the chair's decision less freely, and A removes the inhibition at source. Option D is also strong and complementary (upward candour with a fix attached, before the review rather than instead of it); its only weakness is that alone it doesn't address the review's structure. Option B is the interesting middle: self-chairing with genuine openness is common practice and far better than concealment — it loses to A only on the structural point, and an SJT rewards noticing that difference. Option C is least effective by a distance, and itemising why is the lesson. It commits three distinct integrity failures — reframing a misjudgement as "bad luck" (the precursor was knowable; your team documented it; luck is what remains *after* available information is used), suppressing evidence from a timeline ("distracting detail" is the concealment adjective — the precursor is the single most learning-dense fact the incident produced), and redirecting root cause onto the vendor (the firmware defect is real *and* the review's question includes why a documented precursor of that defect went unchecked) — and each failure compounds at your level specifically. You chair every review: the standard you apply to your own decision *is* the centre's evidence standard from now on; every engineer watching learns whether reviews here find truth or protect chairs. The 40-minute extension will surface anyway (timelines are checked against monitoring by exactly the analysts you trained to do so), converting C's soft concealment into hard discovery. And the suppressed fix — the precursor check that option D volunteers — is the one artefact that would make last night's cost purchase future benefit; C spends the tuition and skips the lesson. General rule for least-effective questions at leadership level: the worst option is rarely the laziest — it is the one that *uses the leader's process power to protect the leader*, because it corrupts the process for every future user. Note, finally, what A+D model together: accountability is not self-flagellation — it is full evidence, structural independence, upward candour, and a fix. Your role summary's phrase is exact: *take accountability for issues that occur*. Last night qualifies.

**Question 11 (hard) — Conflicting duties in the same hour**

09:00 Monday. Three items, one hour, no delegation available until 10:00: (i) the CAB sits at 09:30 to decide a high-impact change you have reviewed and have material concerns about (thin rollback evidence — your concerns are not yet in writing); without your input it likely passes on the proposing team's assurances; (ii) a director wants you on a 09:15 call about Friday's incident, which is politically hot but operationally closed; (iii) your senior analyst — the one from last month's health check concerns — has asked for twenty minutes "before the day starts, it's important", looking visibly strained. What do you do?

- A) Director call first (seniority), CAB second, analyst when the schedule clears.
- B) Send written CAB input now (ten minutes: your specific rollback concerns and a recommendation to defer pending evidence — written concerns cannot be talked past), take the analyst's twenty minutes at 09:15, and offer the director 10:00 with a written incident summary in the meantime — the closed incident's facts will keep; a strained person who asked for help "before the day starts" may not.
- C) Attend the CAB in person at 09:30 as the priority, asking the analyst to book time this afternoon and the director's office to reschedule.
- D) Take the analyst first for twenty minutes, then join the CAB late, then the director.

**Correct answer: B**

**Explanation:** The discriminating insight is that the three demands differ not just in importance but in *transformability*: one can be converted from synchronous to asynchronous without losing force, and spotting which one unlocks the hour. The CAB input converts best — and arguably *improves* in conversion: written, specific concerns ("rollback evidence consists of X; the untested path is Y; recommend deferral pending Z") enter the record, cannot be smoothed over in the room's social flow, and force the board to decide *against a documented objection* if it proceeds — which is governance working exactly as designed, and often more robust than your presence, since a written objection outlives the meeting. (Your change management accountability is discharged by the quality and timeliness of the concern, not by attendance.) The director's need also converts: the incident is closed; its facts are stable; a crisp written summary now plus a 10:00 call serves the political need almost undegraded — and "operationally closed, politically hot" is precisely the category where an hour's delay costs least. The analyst's request is the one that does *not* convert: a strained person who asked for time "before the day starts" has already rehearsed the conversation and timed the ask to their courage; deferral to the afternoon is not the same conversation later — it is frequently no conversation, and after last month's health check data (they are the safety signal made flesh), the twenty minutes is both a duty of care and, coldly, operational risk management: strained senior analysts on your on-call roster are a reliability issue. So B's sequencing — asynchronous artefacts for the convertible two, synchronous presence for the unconvertible one — serves all three demands at above 80% fidelity, where every other option serves one at 100% and drops another entirely: A defers the human indefinitely behind rank-ordered meetings (and note "when the schedule clears" — Monday schedules don't); C protects the CAB attendance that written input replaces while spending the analyst's courage window; D honours the analyst but arrives at the CAB after the decision — twenty minutes late to a 09:30 board that decides your item early is written input's inferior cousin, minus the record. The senior skill under examination: triage by *what each demand actually needs from you* — record, information, presence — rather than by the volume, rank, or order of the asking.

**Question 12 (hard) — Most and least: the estate-wide morning**

07:50. Overnight, three things happened across the estate you address issues for: (i) a security patch mandated centrally ("apply within 24 hours") failed on 2 of 14 servers, which are now running unpatched but stable; (ii) the overnight shift, misreading a runbook threshold, escalated a routine batch overrun to the duty engineer at 03:00 unnecessarily — the engineer is publicly irritated in the team channel and the overnight analyst, new, has gone quiet; (iii) monitoring shows the storage precursor signature (your old friend from earlier sections) firing again — controls are in place, the runbook is tested, the reset is scheduled within its threshold. Four candidate first hours:

(1) Personally drive the two failed patch installs to completion, as the central mandate has a deadline and security trumps everything.
(2) Sequence by residual risk: confirm the storage reset is proceeding under its tested control (five minutes — it is), assign the patch remediation to the day team with the 24-hour deadline and a check-in, then spend real time on (ii): a public word in the channel reframing the escalation as the runbook ambiguity it was, a private word with the engineer about the tone, a private word with the analyst confirming the escalation instinct was right even though the threshold reading was wrong — and a task to fix the ambiguous runbook wording.
(3) Spend the hour on the storage signature personally, since it has preceded a major outage before.
(4) Post a channel message that overnight escalation criteria will be reviewed, and schedule that review for next week.

Which is the MOST effective first hour, and which is the LEAST effective?

- A) Most: (2); Least: (3)
- B) Most: (1); Least: (4)
- C) Most: (2); Least: (4)
- D) Most: (3); Least: (1)

**Correct answer: A**

**Explanation:** Work the residual-risk ordering that option (2) itself models. The storage signature *sounds* most alarming — it has history — but it is precisely the item your earlier work has already de-risked: precursor alert firing as designed, tested runbook, reset scheduled inside threshold. Its residual risk is the lowest on the board, and the five-minute confirmation is the correct expenditure; an hour of personal attention (option 3) re-buys insurance you already own, which is why (3) is the *least* effective hour — not because it is careless, but because it spends the escalation manager's scarcest resource on the estate's best-controlled risk while both live items wait. (Least-effective is not always the negligent option; at senior level it is often the *redundant* one.) The patches (i) carry real but bounded risk — unpatched-but-stable, 22 hours of deadline remaining, and remediation is squarely delegable with a deadline and check-in; option (1)'s personal driving confuses the mandate's importance with a need for *your hands*, and spends the hour a team could spend. Which leaves (ii) — superficially the softest item, actually the most time-critical *and* least delegable: a new analyst is deciding, this morning, in the quiet after public irritation, what escalating will cost them next time — and the lesson they internalise by 09:00 propagates to every future 03:00 judgement call. Under-escalation cultures are built in exactly these mornings. The three-part repair in (2) is the full treatment: public reframe (the channel saw the irritation; the channel must see the correction — escalation instinct endorsed, ambiguity owned by the runbook), private tone conversation with the engineer (adapting feedback so it lands and lasts — your community collaboration skill verbatim), private confirmation to the analyst (the instinct was *right*; the threshold text was wrong), and the runbook wording fix that converts the whole episode into a system improvement. Option (4) is the bureaucratic mirage: it looks responsive, but a "criteria review next week" leaves the analyst silent for a week, the engineer's irritation as the channel's last word, and implicitly locates the fault in the *criteria* the analyst followed — the worst available message, delivered slowly. But note the ranking: (4) is weak, (3) is wasteful-plus-blind (an hour on the controlled risk while the culture wound sets), and the scoring key's discrimination between them — (3) as least effective — rewards seeing that redundant vigilance has an opportunity cost measured in the items it displaces. Hence A: most (2), least (3). The closing principle, which is very nearly the whole of operational leadership at your level: your value at 07:50 is not doing the most urgent-sounding thing — it is allocating yourself to the risk *only you* can retire this hour, and this morning that risk was cultural, not technical.

### Preparation tips

- **Audit your authority boundaries in advance.** List the decisions your role owns outright (emergency changes, incident leadership calls, prioritisation across the estate), those needing consultation, and those that are genuinely others' — with the governing document for each. Most senior SJT errors are altitude errors in one direction or the other, and the audit also improves your Tuesdays.
- **Rehearse the pressure-to-structure conversion.** For upward pressure (directors, sponsors, mandates), practise the template: current state, options with risks, recommendation, next update. Having it rehearsed is what keeps it available at 02:00.
- **Collect your own dilemmas.** After each genuinely hard call, write the scenario, the options you saw, and — a month later — what the second-order effects actually were. Your calibration against "what does this teach the team?" improves only with tracked outcomes.
- **Practise separating the two questions.** Most hard scenarios bundle an estate question (what does the risk need?) with a people question (what does the culture need?). Answer them separately, then sequence — the bundling is where wrong answers hide.
- **Pre-decide your integrity lines.** Records say what happened; concerns go in writing; discovered falsification gets disclosed with a fix. Deciding these in calm makes the pressured version a lookup, not a deliberation.
- **In most/least items, rate every option before ranking.** Score each against users, truth, authority-level, second-order teaching, and opportunity cost. The least-effective option at senior level is often redundant or self-protective rather than lazy — rating catches what ranking misses.

### Common pitfalls to avoid

- **Deference that spends what you're accountable for.** Letting seniority, experience or sponsor pressure override evidence you hold is not respect — the outcome stays yours. Engage the evidence, keep the decision at its right level.
- **Heroic personal execution of delegable work.** Driving the patches, doing the analysis, attending every meeting: activity that displaces the allocation judgement which is actually your job.
- **Escalating before managing — or absorbing what must rise.** The escalation point escalates too: the skill is exhausting the right lower step first (the direct conversation, the restructured ask, the priced trade-off), then rising with evidence.
- **Resolving tension through the record.** Re-dated tests, softened timelines, "bad luck" framings, quiet non-disclosure of inherited defects — every scenario containing a record has a trap version where the record bends. It is always the trap.
- **Treating culture wounds as soft items.** The quiet analyst, the health check dip, the public irritation — these are reliability infrastructure. Deferring them behind technical work is deferring the estate's future incident reporting.
- **Redundant vigilance on controlled risks.** Personal attention lavished where controls already stand is not diligence; it is the opportunity cost that starves the risk only you can retire. Confirm controls briefly, then allocate yourself where the residual is.

## Conclusion

You have reached the end of a demanding set of practice materials — well done for working through it with the honesty the questions asked of you.

Consider what you have exercised. In the cognitive section you diagnosed across shared dependencies, sequenced recoveries against binding deadlines, caught the collision hiding in an approved change calendar, and pushed problem investigations past mechanism to root cause. In the numeric section you ran burn rates against elapsed time, decomposed blended statistics to find the concentrated risk, priced preventative controls in expected value, reconciled measurements that answered different questions, and recomputed a supplier's headline with its exclusions restored. In the verbal section you held rule-plus-exception structures whole, kept "likely cause" from hardening into "cause", read floors as floors rather than schedules, narrowed a review's conclusions back to the scope of its evidence, and computed a declaration duty from modal verbs and timestamps under pressure. And in the situational judgement section you rehearsed the calls that define the level: stopping a confident senior's irreversible action, converting a director's pressure into decision-grade structure, repairing your own team telemetry after a health check, holding continuity truth against a sponsor's date, exercising 02:00 authority with its controls attached, and — hardest — putting your own misjudgement fully in evidence before a review you normally chair.

None of it was generic. Every question drew on the named skills your role summary holds you to — incident management, problem management, change management, continuity management, asset and configuration management, availability and capacity management, service focus, ownership and initiative, community collaboration, service management framework knowledge, and user focus — because at your level, assessment preparation and professional practice converge on the same disciplines: verify before trusting, quantify before deciding, read exactly, write unambiguously, keep the record true, and allocate yourself to the risk only you can retire.

If an assessment is ahead of you, revisit the preparation tips, rehearse once against your own estate's documents and data — the highest-fidelity practice available — and arrive rested. If certain sections resisted you, return to them after a few days and notice how much of the difficulty was technique rather than capability; technique consolidates. Consider also working one or two of the situational scenarios through with a trusted peer at your level — the calls are genuinely contestable, and hearing another manager's second-order reasoning is worth more than any answer key.

Finally, keep the larger frame. The judgement you have been sharpening here protects live public services and the people who depend on them — and it shapes the analysts and engineers who are watching how you decide, correct, disclose, and allocate. The standards you hold under pressure become your centre's standards. That is the real weight of the role, and the real value of practising for it deliberately. Take this preparation forward with confidence — you have done the work. Good luck.

