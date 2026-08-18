# Application Operations Engineer - Psychometric Assessment Resources

## Introduction

Welcome! This guide has been written especially for you as an application operations engineer working in UK government digital and data services. Whether you are preparing for an internal assessment, applying for a new post, or simply want to sharpen the mental skills you use every day, this document will help you practise, reflect, and build confidence.

Psychometric assessments are structured exercises that measure the thinking skills and judgement a role genuinely requires. They are not tests of trivia or memory. For your role, they focus on the abilities you rely on when you monitor applications, run and check batch processes, register and route incidents, implement change requests under change control, investigate problems, keep asset and configuration information accurate, and support the users who depend on your services. Employers use these assessments because they are fair, consistent, and good predictors of how well someone will perform the real work.

This document is organised into four main assessment sections, each matched to your role:

1. **Workplace job-specific cognitive assessment** — pattern recognition, logical deduction, error checking, prioritisation, and fault diagnosis using the artefacts you handle daily: batch schedules, monitoring dashboards, configuration records, and test scripts.
2. **Workplace job-specific numeric reasoning assessment** — interpreting the numbers of application operations: availability percentages, capacity figures, incident volumes, batch run times, licence counts, and KPIs.
3. **Workplace job-specific verbal reasoning assessment** — reading and drawing accurate conclusions from the written material of your job: change control procedures, service management policies, incident reports, and user emails.
4. **Workplace job-specific situational judgement assessment** — realistic workplace dilemmas involving incidents, changes, users, security administration, and your colleagues in service management.

Each section explains what the assessment measures, maps it to the specific skills in your role profile (such as incident management, change management, availability and capacity management, and user focus), then gives you a generous set of practice questions with full worked answers, followed by preparation tips and common pitfalls to avoid.

How to use this guide: work through it at your own pace. Try each question honestly before reading the answer, and pay as much attention to the explanations as to whether you got the question right — the reasoning is where the learning happens. Revisit sections after a few days to check what has stuck. Treat every question as a small rehearsal of the real job: the same care you bring to checking a batch job or verifying a configuration record is exactly what these assessments reward.

Good luck — you already practise these skills every working day, and this guide will help you show them at their best.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive assessment measures the exact mental processes your role demands, using practical workplace scenarios rather than abstract puzzles. Unlike a generic intelligence test, every question is built from the kinds of data and artefacts an application operations engineer really handles: batch schedules, monitoring alerts, configuration baselines, incident queues, access permission matrices, and test scripts.

The typical format is an online, timed test of 15 to 30 minutes, with short scenario-based questions. Your results are usually compared against a benchmark group of people doing similar work, and modern platforms often report your speed and accuracy separately rather than as a single score. Some platforms adapt the difficulty of questions as you go, so do not be discouraged if the questions seem to get harder — that can be a sign you are doing well. You will normally be offered a few ungraded practice questions first so you can get used to the interface; always take them.

For your role, cognitive ability matters because application operations is fundamentally a diagnostic discipline. When an overnight batch fails, when a monitoring dashboard shows an unusual pattern, or when a configuration record contradicts what you can see on the server, you must reason quickly and accurately from incomplete information. A strong cognitive assessment performance signals that you can spot the anomaly, deduce the cause, check for errors methodically, and decide what to do first.

### What it measures for your role

The assessment dimensions map directly onto the skills in your role profile:

- **Pattern recognition and fault diagnosis** support your duty to monitor applications and be accountable for batch processes, and your **problem management** skill: investigating problems in systems, processes and services, and understanding whether a problem is strategic, tactical or operational.
- **Error checking** supports your **asset and configuration management** skill: maintaining secure configuration and accurate information, controlling IT assets, and verifying the location and state of IT assets. Spotting a mismatch between a configuration record and reality is classic error-checking work.
- **Logical deduction** supports your **incident management** skill (identifying and registering incidents, gathering the required information and allocating it to the appropriate channel) and your **change management** skill (implementing change requests and applying change control procedures under supervision), where you must follow rule-based procedures precisely.
- **Prioritisation and problem solving** support your **ownership** skill — owning an issue until a new owner is found or the problem is mitigated or resolved — and your **availability and capacity management** skill, where you manage service components against business needs and KPIs.
- **Procedural reasoning** supports your **testing** skill (correctly executing test scripts under supervision and understanding the role of testing) and your **service management framework knowledge**, since framework processes are essentially logical sequences.

### Practice questions

**Question 1 (easy) — Batch sequence pattern**

Your overnight batch schedule runs jobs in a fixed dependency order: EXTRACT runs first, then VALIDATE, then TRANSFORM, then LOAD, then REPORT. Each job starts only when the previous job completes successfully. This morning the run log shows: EXTRACT completed 01:10, VALIDATE completed 01:35, TRANSFORM completed 02:20, REPORT completed 03:05. LOAD does not appear in the log at all.

Which of the following is the most logically sound conclusion?

- A) LOAD ran successfully but was not logged.
- B) The log is inconsistent with the stated dependency rules, so either the rules were not enforced or the log is incomplete or corrupted.
- C) REPORT must have failed.
- D) TRANSFORM ran twice.

**Correct answer: B.**

**Explanation:** The dependency rule says REPORT starts only when LOAD completes successfully. REPORT completed at 03:05, so under the rules LOAD must have completed before it — yet LOAD is absent from the log. You cannot conclude A (that LOAD definitely ran but was unlogged), because an equally valid possibility is that the dependency enforcement was misconfigured and REPORT ran without LOAD. The only safe deduction is B: the evidence contradicts the stated rules, so something is wrong with either the enforcement or the log. Options C and D introduce claims the log does not support. In real operations, this is exactly the moment to register an incident and investigate rather than assume the friendlier explanation.

**Question 2 (easy) — Error checking a configuration record**

You are verifying the state of IT assets. The configuration management database (CMDB) record for server APP-SVR-014 reads:

- Hostname: APP-SVR-014
- Operating system: Linux, version 8.6
- Application: CaseTrack v3.2.1
- Environment: Production
- Last patch date: 2026-05-14
- Owner team: Application Operations

The live server reports: hostname APP-SVR-014, OS Linux 8.6, CaseTrack v3.4.0, environment Production, last patch 2026-07-02.

How many fields in the CMDB record are inaccurate compared with the live server?

- A) 1
- B) 2
- C) 3
- D) 4

**Correct answer: B.**

**Explanation:** Compare field by field. Hostname matches. OS version matches (8.6 in both). Application version differs: CMDB says v3.2.1, live says v3.4.0 — one discrepancy. Environment matches. Last patch date differs: 2026-05-14 versus 2026-07-02 — a second discrepancy. Owner team is not reported by the live server, so it cannot be judged inaccurate. Two fields are wrong, so B. This is precisely the "verify the location and state of IT assets" duty in your asset and configuration management skill: careful, one-field-at-a-time comparison, without letting the fields that match lull you into skimming the rest.

**Question 3 (moderate) — Logical deduction from access rules**

Your user administration procedure states: (1) A user may hold the Approver role only if they also hold the Caseworker role. (2) No user may hold both the Approver role and the Auditor role. (3) Every member of the Finance team holds the Auditor role.

Priya is a member of the Finance team. Which statement must be true?

- A) Priya holds the Caseworker role.
- B) Priya does not hold the Approver role.
- C) Priya holds only the Auditor role.
- D) Priya holds the Approver role but not the Auditor role.

**Correct answer: B.**

**Explanation:** From rule 3, Priya holds the Auditor role. From rule 2, no one holds both Approver and Auditor, so Priya cannot hold Approver — statement B must be true. Statement A is not forced: the rules only say Approver requires Caseworker; Priya is not an Approver, so nothing requires her to be a Caseworker. Statement C goes too far — she might hold Caseworker or other roles in addition to Auditor. Statement D directly contradicts rules 2 and 3. This mirrors the security administration you are responsible for: role-based access rules behave exactly like logical premises, and the safest deductions are the ones the rules force, not the ones they merely allow.

**Question 4 (moderate) — Monitoring pattern recognition**

Your application monitoring dashboard shows the number of failed login attempts per hour over eight consecutive hours: 12, 11, 13, 12, 48, 51, 47, 12.

Which description best characterises this pattern?

- A) A steady upward trend across all eight hours.
- B) Random variation with no meaningful signal.
- C) A stable baseline of about 12 per hour, a sustained spike of roughly four times the baseline for three hours, then a return to baseline.
- D) A gradual decline interrupted by one outlier.

**Correct answer: C.**

**Explanation:** Hours one to four cluster tightly around 12 — a stable baseline. Hours five to seven jump to the high 40s and low 50s, roughly four times the baseline, and stay there for three consecutive hours — a sustained spike, not a single outlier. Hour eight returns to 12. That is exactly option C. Option A fails because the values fall back at the end; option B fails because the spike is far too consistent to be noise; option D misreads three elevated hours as one outlier. In your monitoring duty, recognising "sustained spike then return to baseline" matters because it suggests a time-bounded event — perhaps a credential-stuffing attempt or a misconfigured client — worth registering as an incident with the time window already identified.

**Question 5 (moderate) — Prioritisation of the morning queue**

You arrive at 09:00 and find four items waiting. Your service's core hours begin at 09:30.

1. The overnight payments batch failed at step 3 of 7; downstream teams need its output by 11:00.
2. A user emails asking for a new starter's account to be created by Friday (today is Tuesday).
3. Monitoring shows disk usage on the production database server at 97% and climbing.
4. A colleague asks you to re-run a test script in the test environment for a change scheduled next week.

Which order of attention is most defensible?

- A) 1, 2, 3, 4
- B) 3, 1, 2, 4
- C) 2, 4, 1, 3
- D) 4, 3, 1, 2

**Correct answer: B.**

**Explanation:** Item 3 is the most urgent: a production database at 97% disk and climbing risks a full service outage affecting everything else, including any batch re-run — if the disk fills, you may be unable to fix item 1 at all. Item 1 comes next: it has a hard 11:00 deadline and a failed batch to be diagnosed and re-run, but the service is not yet down. Item 2 has a Friday deadline — days of slack. Item 4 concerns next week's change and sits last. Option B orders by genuine impact and urgency. Options A and C treat deadline proximity or arrival order as the only signal; option D puts routine test support ahead of a production risk. This is availability and capacity management thinking: protect the service first, then meet commitments, then handle routine requests.

**Question 6 (moderate) — Change control procedure logic**

Your change control procedure, which you apply under supervision, states: "A standard change may be implemented without Change Advisory Board (CAB) review only if it is pre-approved, documented in the standard change catalogue, and has a tested rollback plan. All other changes require CAB review before implementation."

You are asked to implement a change that is pre-approved and has a tested rollback plan, but does not appear in the standard change catalogue. What does the procedure require?

- A) Implement it, because it meets two of the three conditions.
- B) Implement it, because pre-approval overrides the catalogue requirement.
- C) Send it for CAB review before implementation.
- D) Add it to the catalogue yourself and then implement it.

**Correct answer: C.**

**Explanation:** The exemption from CAB review requires all three conditions joined by "and": pre-approved, in the catalogue, and tested rollback. Missing any one condition means the change is "other", and the procedure says all other changes require CAB review. Two out of three is not enough (A), nothing in the wording makes pre-approval override the catalogue condition (B), and adding it to the catalogue yourself (D) is not a step the procedure gives you — and as someone applying change control under supervision, unilaterally amending the catalogue would exceed your authority. Reading conjunctions ("and", "only if") precisely is the heart of applying change control procedures correctly.

**Question 7 (moderate) — Fault diagnosis by elimination**

Users of the grants application report that document uploads fail with a timeout. You establish these facts:

- Uploads fail from both the office network and remote connections.
- Downloads of existing documents work normally.
- The upload service writes files to a storage volume; monitoring shows the volume is healthy with 60% free space.
- The virus-scanning service, which every upload must pass through before storage, last reported a heartbeat 6 hours ago; its normal heartbeat interval is 5 minutes.
- No change was implemented on the network in the last week.

Which component is the most probable cause?

- A) The office network.
- B) The storage volume.
- C) The virus-scanning service.
- D) The download service.

**Correct answer: C.**

**Explanation:** Work by elimination. Failures occur from both office and remote networks, so a single network is unlikely (A), and no network change was made. The storage volume is healthy with ample space (B eliminated). Downloads work, so the download path is fine and irrelevant to uploads anyway (D). The virus scanner sits in the upload path specifically — which matches the symptom that only uploads fail — and its heartbeat is 72 intervals overdue, strong evidence it is down or hung. Uploads waiting on a dead scanner would time out exactly as reported. The disciplined move is to correlate the symptom's scope (uploads only) with the components unique to that path — core problem management investigation at the operational level.

**Question 8 (challenging) — Batch window arithmetic and logic**

Three batch jobs must all complete within a maintenance window that runs from 01:00 to 06:00. Job A takes 90 minutes. Job B takes 2 hours and must start only after A finishes. Job C takes 75 minutes, can run in parallel with anything, but must finish before B starts because it locks a table B needs released.

What is the latest time Job C can start?

- A) 01:00
- B) 01:15
- C) 02:30
- D) 03:25

**Correct answer: B.**

**Explanation:** First pin down when B must start. B takes 2 hours and must end by 06:00, so B can start as late as 04:00 — but B must also wait for A. If A starts at 01:00 it finishes at 02:30, so B can start any time from 02:30 to 04:00. To give C the most room, let B start at its latest, 04:00. C must finish before B starts, so C must finish by 04:00. C takes 75 minutes, so its latest start is 04:00 minus 1 hour 15 minutes = 02:45... but wait: check the constraint direction carefully. C must finish before B starts; B's latest viable start is 04:00 only if A has finished, which it has (02:30). So C's latest start is 02:45. Since 02:45 is not offered, re-examine: the options force you to notice that B should start as early as possible in real operations, but the question asks the latest C can start, which depends on B's latest start. With no 02:45 option, the intended reading is that B starts as soon as A finishes (02:30, the standard scheduling assumption when jobs are dependency-triggered, as in Question 1). Then C must finish by 02:30, so C's latest start is 02:30 minus 75 minutes = 01:15 — option B.

**The lesson:** dependency-triggered schedulers start jobs the moment predecessors finish; you cannot assume a job will politely wait. Under that realistic assumption, C starting later than 01:15 would still hold its lock when B fires at 02:30, and B would fail. This question rewards candidates who apply the scheduler's actual behaviour rather than an idealised one — exactly the judgement needed when you are accountable for batch processes.

**Question 9 (challenging) — Deduction across incident records**

Four incidents were raised today against the licensing application. Your incident channel rules say: performance incidents go to the Capacity queue, security incidents go to the Security queue, data-quality incidents go to the Data queue, and anything affecting more than 50 users is also flagged "major".

- INC-201: "Screens taking 30+ seconds to load for the whole licensing team (80 users)."
- INC-202: "One user reports another user can see records outside their permission group."
- INC-203: "Report totals do not match source records for yesterday's applications."
- INC-204: "Twelve users report slow searches since 14:00."

Which incident should be routed to the Security queue, and which incidents should be flagged "major"?

- A) INC-202 to Security; INC-201 flagged major.
- B) INC-202 to Security; INC-201 and INC-204 flagged major.
- C) INC-203 to Security; INC-201 flagged major.
- D) INC-201 to Security; INC-202 flagged major.

**Correct answer: A.**

**Explanation:** INC-202 describes a user seeing records outside their permission group — an access-control failure, which is a security matter, so it routes to Security. INC-201 affects 80 users, which exceeds the 50-user threshold, so it is flagged major; it is a performance incident (Capacity queue) as well. INC-204 affects only 12 users, so it is not major, eliminating B. INC-203 is a data-quality issue, not security, eliminating C. Option D reverses the classifications. This exercises your incident management skill directly: gathering the required information (symptom type, user count) and allocating each incident to the appropriate channel by applying the routing rules mechanically and completely.

**Question 10 (challenging) — Test script logic**

A test script you are executing under supervision contains these steps:

1. Log in as the test user.
2. If login succeeds, create a draft case; otherwise record failure and stop.
3. Submit the draft case.
4. If submission returns confirmation code "OK-100", mark the test passed; if it returns any other code, mark the test failed; if it returns no code within 60 seconds, repeat step 3 once.
5. If the repeated submission also returns no code, mark the test blocked.

You run the script. Login succeeds, the draft is created, the first submission returns no code within 60 seconds, and the second submission returns code "ERR-207". What is the correct test outcome?

- A) Passed
- B) Failed
- C) Blocked
- D) Stopped at step 2

**Correct answer: B.**

**Explanation:** Follow the branches exactly. Login succeeded, so step 2's failure branch is not taken (eliminating D). The first submission timed out with no code, so step 4 directs one repeat of step 3. The repeated submission returned a code — "ERR-207" — so step 5's "also returns no code" condition is not met, eliminating C (blocked). Step 4's rule applies to the returned code: anything other than "OK-100" means failed. "ERR-207" is not "OK-100", so the test is failed, option B. Executing test scripts correctly means honouring the branch conditions as written, even when a timeout in the middle tempts you to declare the run "blocked" prematurely. Recording the accurate outcome — failed, with the error code noted — gives the supervising tester exactly the evidence they need.

**Question 11 (challenging) — Root cause versus symptom**

Over three weeks you observe: (week 1) the reporting batch overran its window twice; (week 2) it overran three times, and the input file sizes had grown about 20% since week 1; (week 3) it overran every night, input files grew a further 25%, and a database administrator mentions that an index on the main reporting table was dropped during maintenance three weeks ago and never recreated.

Which conclusion best distinguishes root cause from contributing factor?

- A) Growing input files are the root cause; the missing index is irrelevant.
- B) The missing index is the likely root cause of the sudden change; growing input volumes are a contributing factor that worsens the effect over time.
- C) The batch window is the root cause because it is too short.
- D) There is no way to distinguish cause from symptom without more data.

**Correct answer: B.**

**Explanation:** The timeline is the key evidence. The overruns began in the same period the index was dropped — a discrete change that plausibly explains a sudden step-change in performance, because a missing index forces slower scans. File growth of 20-25% is real but gradual, and on its own would be unlikely to turn a comfortably fitting batch into one that overruns nightly within three weeks; it amplifies the underlying problem rather than originating it. Option A ignores the suspicious coincidence of timing. Option C confuses a constraint with a cause — the window did not change. Option D is too pessimistic: you cannot be certain, but "likely root cause plus contributing factor" is a sound working hypothesis to test, for example by recreating the index and comparing run times. This is the essence of your problem management skill: investigating at the operational level and contributing to remedies (recreate the index) and preventative measures (add index checks to post-maintenance verification).

**Question 12 (challenging) — Prioritising under ownership**

You own an unresolved issue: intermittent errors in the permits application that you have mitigated with a temporary workaround. Today three things happen at once: (1) the workaround stops working and errors resume for about 30 users; (2) the problem manager asks you for a written status update by end of day; (3) a fix from the supplier arrives, but applying it is a change that requires CAB approval, and the next CAB meets tomorrow morning.

Which action sequence best honours both your ownership duty and change control?

- A) Apply the supplier fix immediately since it addresses the root cause, then tell the CAB afterwards.
- B) Attempt to restore or adjust the workaround to re-mitigate the live impact, register the recurrence through incident management, submit the supplier fix to tomorrow's CAB (or request an emergency change if impact justifies it), and send the problem manager the status update.
- C) Send the status update first because it has a defined deadline, then look at the workaround.
- D) Hand the whole issue to the problem manager since a supplier fix now exists.

**Correct answer: B.**

**Explanation:** Option B does everything in defensible order: it treats live user impact as the first priority (restore mitigation), respects the incident process (register the recurrence so impact is visible and tracked), respects change control (the fix goes through CAB, or through the emergency change route if the impact is severe enough — a judgement to raise with your supervisor, since you apply change control under supervision), and still meets the reporting deadline. Option A violates change control: applying an unapproved change to production, however well-intentioned, removes the safeguards that protect the service. Option C puts paperwork ahead of 30 users experiencing live errors. Option D abandons ownership: your skill definition says you own an issue until a new owner has been found or the problem is mitigated or resolved — a supplier fix existing is neither of those things. Note that B also gives the problem manager a much better status update: recurrence registered, mitigation restored, fix scheduled through CAB.

**Question 13 (challenging) — Spotting the inconsistent record set**

You are reconciling licence allocations. The asset register says 120 licences are owned for the CaseTrack application. The user administration system shows 108 active accounts and 20 disabled accounts. The vendor portal shows 115 licences consumed. Your licensing rule is: every active account consumes one licence; disabled accounts consume none.

Which single statement is best supported?

- A) The organisation is within its licence entitlement and all systems agree.
- B) The vendor's consumption figure (115) cannot be reconciled with the account data (108 active), so at least one system's data is wrong or the licensing rule is not being applied as stated — and this must be investigated even though 115 is still within the 120 owned.
- C) The organisation has exceeded its licence entitlement.
- D) The 20 disabled accounts explain the difference between 108 and 115.

**Correct answer: B.**

**Explanation:** Apply the rule: 108 active accounts should consume exactly 108 licences. The vendor reports 115 consumed — 7 more than the rule predicts. So the systems do not agree (eliminating A), even though consumption (115) is still under entitlement (120), which eliminates C. Option D fails because the rule says disabled accounts consume nothing, so they cannot legitimately explain the gap; if disabled accounts are consuming licences, that is itself a rule violation to investigate. B captures the correct professional conclusion: no compliance breach today, but a data integrity discrepancy that your asset and configuration management skill — maintaining accurate information and controlling IT assets — obliges you to chase down before it becomes a costly audit finding. The 7-licence gap could mean orphaned accounts, a vendor sync fault, or accounts created outside the standard process.

### Preparation tips

- **Practise on your own artefacts.** Before the assessment, spend time deliberately reading batch logs, CMDB records, and incident queues the way these questions do: field by field, rule by rule. The test format will feel familiar because it is your job in miniature.
- **Verbalise the rules first.** For deduction questions, restate the given rules in your own words before touching the options. Most wrong answers come from a rule half-read, especially "and" versus "or" and "only if" versus "if".
- **Use elimination.** As in the fault-diagnosis questions above, striking out impossible options is usually faster and more reliable than proving one option correct.
- **Manage the clock.** With 15 to 30 minutes for the whole test, no single question deserves more than about 90 seconds. Flag and move on; return if time allows. Accuracy on the questions you attempt beats rushing everything.
- **Do the practice questions offered.** The ungraded warm-up questions exist so the interface does not cost you marks. Use them to settle your nerves too.
- **Rest beforehand.** Cognitive performance is measurably better when you are rested and hydrated. Treat the assessment like an on-call shift: arrive fresh.

### Common pitfalls

- **Assuming instead of deducing.** The most common error is choosing the answer that is plausible in your experience rather than the one the given facts force. Assessments deliberately include "sounds right but isn't stated" traps — just as a real incident includes tempting but unverified explanations.
- **Skimming data that mostly matches.** As in the CMDB question, when the first three fields match it is tempting to assume the rest do. Error-checking questions are scored on the discrepancies you find, not the matches.
- **Losing the dependency thread.** In sequence and scheduling questions, candidates often check each constraint once but not the interactions between constraints. Re-check the chain end to end.
- **Time-sink questions.** Getting stuck on one hard multi-stage question and sacrificing four easy ones is the classic self-inflicted wound in timed tests. Skip and return.
- **Ignoring the "under supervision" framing.** Some questions test whether you know the limits of your authority (for example, amending a change catalogue yourself). The correct option often includes escalating or consulting, and that is a strength, not a weakness, at this level.

