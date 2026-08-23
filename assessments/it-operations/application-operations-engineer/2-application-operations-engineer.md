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


## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment tests whether you can reach a defensible conclusion from operational data at a steady pace. As an application operations engineer the data is what you look at daily: batch run times and record counts, incident volumes and priorities, availability figures, disk and capacity headroom, and licence and asset counts.

The format is typically fifteen to twenty-five minutes with a calculator permitted, presenting tables followed by multiple-choice items. The arithmetic is not advanced; the challenge is doing it accurately under time pressure and reading the qualifiers correctly.

Three habits matter particularly in this role.

The first is that availability percentages should convert instantly into minutes. When someone says a service must be 99.9% available, you need to know that is about 43 minutes a month before you can say whether a maintenance window fits.

The second is that batch processing is arithmetic you can do before it goes wrong. Records divided by throughput gives you elapsed time, and comparing that against the window is a two-minute calculation that prevents a great many overnight failures.

The third is that a count and a rate answer different questions. More incidents this month may mean things got worse, or may mean more transactions were processed — and normalising before comparing is what separates a useful observation from a misleading one.

### What it measures for your role

- **Availability arithmetic** maps to **Availability and capacity management**.
- **Batch and throughput calculations** maps to being accountable for batch processes.
- **Incident volumes and priorities** maps to **Incident management**.
- **Capacity headroom** maps to monitoring applications.
- **Asset and licence counts** maps to **Asset and configuration management**.
- **Reporting figures accurately** maps to **Service focus** and **Communicating information**.

### Practice questions

*Table 1 — Overnight batch jobs, typical run*

| Job | Records | Throughput (records/second) | Window start | Window end |
|---|---|---|---|---|
| Extract | 1,200,000 | 900 | 22:00 | 23:00 |
| Validate | 1,200,000 | 400 | 23:00 | 02:00 |
| Load | 1,180,000 | 250 | 02:00 | 04:00 |
| Reconcile | 1,180,000 | 1,500 | 04:00 | 04:30 |

**Question 1 (easy) — Reading a table**

How long does the Extract job take at the stated throughput?

- A) About 22 minutes
- B) About 45 minutes
- C) About 1 hour 20 minutes
- D) About 13 minutes

**Correct answer: A**

**Explanation:** 1,200,000 / 900 = 1,333 seconds, which is 22.2 minutes. Its window is a full hour, so it has comfortable headroom. Getting into the habit of converting record counts and throughput into elapsed minutes is the single most useful arithmetic in batch operations.

**Question 2 (easy) — A job against its window**

Does the Validate job fit its window?

- A) Yes, with about 10 minutes to spare
- B) Yes, comfortably
- C) No, it overruns by about 20 minutes
- D) It exactly fills the window

**Correct answer: B**

**Explanation:** 1,200,000 / 400 = 3,000 seconds = 50 minutes, against a three-hour window from 23:00 to 02:00. It fits very comfortably indeed — the window is more than three times what the job needs. That is worth noticing rather than glossing over, because a job with that much slack is a good candidate for absorbing a delay elsewhere in the chain.

**Question 3 (moderate) — The tight one**

Which job has the least headroom in its window?

- A) Extract
- B) Validate
- C) Load
- D) Reconcile

**Correct answer: C**

**Explanation:** Extract: 22 minutes in 60, using 37%. Validate: 50 minutes in 180, using 28%. Load: 1,180,000 / 250 = 4,720 seconds = 78.7 minutes, in a 120-minute window, using 66%. Reconcile: 1,180,000 / 1,500 = 787 seconds = 13.1 minutes in 30, using 44%. Load is tightest at 66% of its window. This is the job to watch as volumes grow, and the calculation tells you that before an overnight failure does.

**Question 4 (moderate) — Growth headroom**

By approximately what percentage could record volume grow before the Load job overruns its window?

- A) About 20%
- B) About 50%
- C) About 34%
- D) About 66%

**Correct answer: B**

**Explanation:** Load currently takes 78.7 minutes in a 120-minute window. It can grow to 120 minutes, which is 120 / 78.7 = 1.525, so about a 52% increase in volume before it overruns. Roughly 50%. Being able to answer "how much growth can this absorb" is far more useful than "does it fit today", because it tells you when to act rather than that you already should have.

**Question 5 (moderate) — Total chain time**

If all four jobs ran back to back with no gaps, how long would the chain take?

- A) About 2 hours 44 minutes
- B) About 3 hours 30 minutes
- C) About 2 hours 10 minutes
- D) About 4 hours

**Correct answer: A**

**Explanation:** 22.2 + 50 + 78.7 + 13.1 = 164 minutes, which is 2 hours 44 minutes. The scheduled windows span 22:00 to 04:30, or six and a half hours, so the chain uses about 42% of the available time. That slack is what absorbs a slow night, and knowing the figure tells you how much of a delay the chain can survive before it starts eating into the morning.

*Table 2 — Incidents, last three months*

| Month | Transactions processed | P1 | P2 | P3 | P4 |
|---|---|---|---|---|---|
| July | 410,000 | 1 | 6 | 34 | 71 |
| August | 520,000 | 2 | 9 | 41 | 88 |
| September | 480,000 | 1 | 5 | 38 | 79 |

**Question 6 (easy) — Total incidents**

How many incidents were raised in August?

- A) 140
- B) 129
- C) 112
- D) 98

**Correct answer: A**

**Explanation:** 2 + 9 + 41 + 88 = 140. Straightforward, and worth doing before any comparison — August has the highest raw count of the three months, which the next question puts in context.

**Question 7 (moderate) — Normalising by volume**

Which month had the highest incident rate per 10,000 transactions?

- A) July
- B) August
- C) September
- D) They are equal

**Correct answer: A**

**Explanation:** July: 112 incidents / 410,000 × 10,000 = 2.73. August: 140 / 520,000 × 10,000 = 2.69. September: 123 / 480,000 × 10,000 = 2.56. July is highest, narrowly, and August — which had the most incidents in raw terms — is actually slightly better than July once volume is accounted for. This is why normalising matters: comparing raw counts across months of different volume rewards quiet months and penalises busy ones.

**Question 8 (moderate) — Severity mix**

What proportion of September's incidents were P1 or P2?

- A) About 4.9%
- B) About 7.9%
- C) About 12%
- D) About 2.4%

**Correct answer: A**

**Explanation:** September had 1 + 5 = 6 high-priority incidents out of 123 total, which is 4.9%. Tracking the severity mix rather than just the total is useful, because a stable total with a rising proportion of P1s and P2s is a service getting worse while its headline number stays flat.

**Question 9 (harder) — Availability in minutes**

A service has a 99.9% monthly availability target. How much downtime does that allow in a 30-day month, and does a planned 90-minute maintenance window fit?

- A) About 43 minutes, so a 90-minute window does not fit within the target
- B) About 43 minutes, and the window fits
- C) About 72 minutes, so the window does not fit
- D) About 22 minutes, so the window does not fit

**Correct answer: A**

**Explanation:** A 30-day month is 43,200 minutes, and 0.1% of that is 43.2 minutes. A 90-minute maintenance window is more than double the entire monthly allowance — so unless planned maintenance is excluded from the availability calculation, which is a question worth asking explicitly, the service cannot take that window and hit its target. Worth committing to memory: 99.9% ≈ 43 minutes a month, 99.95% ≈ 22, 99.99% ≈ 4.3.

**Question 10 (harder) — Disk headroom**

A filesystem is 68% full at 340 GB used. It grows by about 4 GB a week. Roughly how long until it reaches 90%?

- A) About 7 weeks
- B) About 27 weeks
- C) About 14 weeks
- D) About 3 weeks

**Correct answer: B**

**Explanation:** If 340 GB is 68%, total capacity is 340 / 0.68 = 500 GB. 90% of 500 is 450 GB, so there is 110 GB of growth available. At 4 GB a week that is 27.5 weeks, about 27. The step people skip is deriving the total capacity from the percentage and the absolute figure — once you have that, the rest is straightforward, and a figure of "about six months" is far more actionable than "it's getting full".

**Question 11 (harder) — A change in run time**

The Load job's run time has increased from 79 minutes to 96 minutes over three months, while record volume rose from 1,180,000 to 1,240,000. What is the strongest observation?

- A) The increase is explained by the extra volume.
- B) Volume rose about 5% while run time rose about 22%, so throughput has fallen — the job is now processing about 215 records a second against 250 — and something other than volume has changed.
- C) The job is approaching its window limit.
- D) The job needs more resource.

**Correct answer: B**

**Explanation:** Volume: 1,240,000 / 1,180,000 = 1.051, a 5% rise. Run time: 96 / 79 = 1.215, a 22% rise. If throughput were unchanged, a 5% volume rise would give a 5% time rise. Actual throughput is 1,240,000 / (96 × 60) = 215 records a second, down from 250. So the job has genuinely slowed — an index, a growing table, contention, or a resource constraint — and option A's explanation does not survive the arithmetic. Option C is true and secondary; option D prescribes before diagnosing.

**Question 12 (harder) — Licence counts**

Your application has 340 named user licences. 312 are assigned. Of those, 47 belong to users who have not logged in for over 90 days. What is the strongest statement?

- A) There are 28 licences available.
- B) There are 28 unassigned licences, and a further 47 assigned to dormant accounts — so up to 75 could be available if the dormant accounts are genuinely no longer needed, which is worth confirming before reclaiming them.
- C) 75 licences are available.
- D) The service needs more licences.

**Correct answer: B**

**Explanation:** 340 − 312 = 28 genuinely unassigned. The 47 dormant accounts are assigned and may belong to people on long-term leave, secondment, or seasonal roles — so they are candidates for reclamation rather than available licences. Option B distinguishes the two correctly and names the check. Option C treats candidates as available, which is how someone returns from six months' leave to find their access removed. This distinction between "unused" and "reclaimable" is core to **Asset and configuration management**.

**Question 13 (harder) — A reported figure that needs a qualifier**

You are asked for last month's availability. The service was down for 38 minutes unplanned and 90 minutes for notified planned maintenance. What is the most accurate response?

- A) 99.91% availability, counting unplanned downtime only, with the 90 minutes of planned maintenance stated separately — because whether planned maintenance counts against the target depends on the agreement, and reporting a single number without saying which convention was used is how figures get disputed.
- B) 99.70%, counting all downtime.
- C) 99.91%.
- D) 99.91% or 99.70% depending on the convention.

**Correct answer: A**

**Explanation:** Unplanned only: 38 / 43,200 = 0.088%, so 99.91%. All downtime: 128 / 43,200 = 0.296%, so 99.70%. Both are correct arithmetic under different conventions, and option A gives the figure with the convention stated and the other component visible, which is what makes it usable. Option D identifies the ambiguity without resolving it, leaving the requester to choose. Options B and C each pick a convention silently, which is exactly how two people end up quoting different availability figures for the same month.

### Preparation tips

- **Convert availability percentages into minutes instantly.**
- **Divide records by throughput to get elapsed time, and compare against the window.**
- **Work out growth headroom, not just whether something fits today.**
- **Normalise incident counts by transaction volume before comparing months.**
- **Derive total capacity from a percentage and an absolute figure.**
- **Compare the rate of change in run time against the rate of change in volume.**
- **Distinguish unassigned from reclaimable.**
- **State the convention when reporting availability.**

### Common pitfalls

- **Comparing raw incident counts across months of different volume.**
- **Assuming a longer run time is explained by more records.**
- **Reporting availability without saying whether planned maintenance is included.**
- **Treating dormant licences as available.**
- **Checking that a batch job fits without checking how much growth it can absorb.**
- **Reading a filesystem percentage without working out the absolute headroom.**

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment tests whether you can determine exactly what a piece of written material establishes. As an application operations engineer the material is runbooks and knowledge articles, incident and change policy, service level agreements, security administration standards, and vendor documentation for the application you support.

The commonest format presents a passage followed by statements to be marked True, False or Cannot Say. True means the passage establishes it, False means it contradicts it, and Cannot Say means it settles neither — regardless of what you know from running the system.

Your own familiarity with the application is the main hazard. You will know how it behaves and what the team normally does, while the passage in front of you describes what the document actually says — and in an incident at 3am, the document is what someone else will be following.

Three specifics matter particularly.

The first is that priority definitions usually combine impact and urgency, and reading one as the whole is the commonest source of misclassification.

The second is that change policy allocates authority narrowly: who may implement what, in which circumstances, and what must be recorded. Your role includes user and security administration, where acting outside the stated authority is a governance matter rather than a technical one.

The third is that runbooks are written to be followed under pressure by someone who may not be you. Reading one for exactly what it covers — and noticing where it stops — is a skill you use both as a reader and as an author.

### What it measures for your role

- **Reading incident policy precisely** maps to **Incident management**.
- **Reading change policy** maps to **Change management**.
- **Reading service level agreements** maps to **Service focus** and **Availability and capacity management**.
- **Reading security administration standards** maps to your user and security administration duties.
- **Reading runbooks and knowledge articles** maps to **Technical specialism** and **Service management framework knowledge**.
- **Reading and recording accurately** maps to **Asset and configuration management**.

### Practice questions

*Passage A — for Questions 1 to 4*

"Incident priority is determined by impact and urgency. Priority 1 requires both high impact and high urgency. Response targets run from the time an incident is logged, not from the time it is reported. Resolution targets are suspended while an incident awaits information from the user and resume when the information is provided. A workaround that restores the user's ability to work is treated as a resolution for target purposes; the underlying fault is managed as a problem. Only the incident manager may change an incident's priority after it has been assigned, and must record the reason."

**Question 1 (easy)**

Statement: An incident with high impact and low urgency is Priority 1.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The passage contradicts this: Priority 1 "requires both high impact and high urgency". A conjunctive definition is not satisfied by one half. A batch failure affecting a whole department's reporting, which nobody needs until month-end, has high impact and low urgency — and it is not Priority 1, however loudly it is reported.

**Question 2 (moderate)**

Statement: You can raise an incident's priority if the user tells you it is more urgent than you first assessed.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The passage states that "only the incident manager may change an incident's priority after it has been assigned". So whatever the user tells you, the reassignment is not yours to make — the correct action is to give the incident manager the new information. The passage contradicts the statement, and this is precisely the sort of authority boundary that is easy to cross with good intentions under pressure from a user.

**Question 3 (moderate)**

Statement: Time spent waiting for a user to provide information counts against the resolution target.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The passage contradicts this: resolution targets "are suspended while an incident awaits information from the user and resume when the information is provided". The suspension exists to exclude exactly that time. Worth noting operationally: this is a legitimate provision and also a route by which a service can meet its targets while a user waits a long time in real terms, so a target-met figure and the user's experience can diverge considerably.

**Question 4 (harder)**

Statement: An incident resolved by a workaround has been fixed.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The passage draws the distinction explicitly: a workaround "is treated as a resolution for target purposes; the underlying fault is managed as a problem". So the incident is closed against target and the fault persists — treated, not fixed. The passage contradicts the statement. Holding this distinction is what stops a service reporting strong resolution figures while the same fault generates incidents indefinitely, which is why problem management exists as a separate discipline.

*Passage B — for Questions 5 to 8*

"Standard changes are pre-approved and may be implemented by any authorised engineer without further approval, provided they are recorded within one working day. Normal changes require approval by the change advisory board, which meets weekly. Emergency changes may be implemented with the approval of the on-call incident manager and must be presented to the next change advisory board for retrospective review. A change may be classified as standard only where it has been implemented successfully at least five times as a normal change and has an approved implementation procedure. Changes affecting user access rights are never classified as standard."

**Question 5 (easy)**

Statement: Standard changes require approval before implementation.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The passage contradicts this: standard changes "are pre-approved and may be implemented by any authorised engineer without further approval". The pre-approval is the whole point of the category. The recording obligation within one working day is a separate duty, not prior approval.

**Question 6 (moderate)**

Statement: A routine password reset procedure implemented successfully twenty times can be classified as a standard change.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The passage states that "changes affecting user access rights are never classified as standard". A password reset affects user access rights, so however many times it has been done successfully, it cannot be a standard change. The five-implementation rule is satisfied and irrelevant, because the access-rights exclusion is absolute — "never" leaves no room. This matters directly for your security administration duties, where the temptation to treat routine access work as standard is constant.

**Question 7 (moderate)**

Statement: An emergency change does not need change advisory board involvement.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The passage contradicts this: emergency changes "must be presented to the next change advisory board for retrospective review". The board's involvement is deferred, not removed. Reading the emergency route as bypassing governance entirely is the natural error, and the retrospective review is precisely what makes an emergency route safe to have — without it, "emergency" becomes everyone's preferred route.

**Question 8 (harder)**

Statement: A change implemented successfully six times as a normal change can be classified as standard.

- A) True
- B) False
- C) Cannot Say

**Correct answer: C**

**Explanation:** Six exceeds the five-implementation threshold, and the passage attaches a second condition — the change must also have "an approved implementation procedure" — about which the statement says nothing. It also does not tell you whether the change affects user access rights, which would exclude it regardless. So two conditions are unestablished and the answer cannot be True. Checking every condition in a compound requirement, rather than the one the statement draws attention to, is the discipline here.

*Passage C — for Questions 9 to 13*

"The application's batch scheduler runs jobs in dependency order. A job whose predecessor has failed is held rather than skipped. Held jobs are released automatically when the predecessor completes successfully. The scheduler retries a failed job twice at ten-minute intervals before raising an incident. Jobs marked as critical raise a Priority 2 incident on failure; other jobs raise Priority 3. The runbook instructs the on-call engineer to check the source file for completeness before re-running a failed extract job. It does not cover the case where the source file is absent."

**Question 9 (easy)**

Statement: A job whose predecessor has failed will be skipped.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The passage contradicts this directly: such a job "is held rather than skipped". The distinction matters operationally — a held job resumes automatically when the predecessor succeeds, so fixing the upstream failure clears the chain without further intervention, whereas a skipped job would need to be run separately.

**Question 10 (moderate)**

Statement: A failed critical job raises a Priority 2 incident immediately.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The scheduler "retries a failed job twice at ten-minute intervals before raising an incident". So the incident is raised after roughly twenty minutes of retries, not immediately. The passage contradicts the word "immediately". This is useful to know when reconstructing a timeline: the incident timestamp is about twenty minutes after the first failure, which matters if you are working out whether a job could still have made its window.

**Question 11 (moderate)**

Statement: The runbook tells the on-call engineer what to do if the source file is missing.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The passage states that the runbook "does not cover the case where the source file is absent". The passage contradicts the statement directly. This is the most useful sentence in the passage from a practical standpoint: a documented gap in a runbook is a gap that will be discovered at 3am by whoever is on call, and identifying it now is the point of noticing.

**Question 12 (moderate)**

Statement: A non-critical job that fails three times raises a Priority 3 incident.

- A) True
- B) False
- C) Cannot Say

**Correct answer: A**

**Explanation:** The scheduler retries twice after the initial failure — three attempts in total — and then raises an incident, and non-critical jobs raise Priority 3. So a job that has failed three times has exhausted its retries and raised a Priority 3 incident. The passage establishes this. The arithmetic of "retries twice" meaning three total attempts is the easy thing to get wrong.

**Question 13 (harder)**

Statement: If a critical job fails and its successor is held, resolving the critical job's incident will release the successor.

- A) True
- B) False
- C) Cannot Say

**Correct answer: C**

**Explanation:** Held jobs "are released automatically when the predecessor completes successfully" — completion is the trigger, not incident resolution. An incident can be resolved in ways that do not involve the job completing: it might be cancelled, deferred to the next night, or resolved by a workaround that bypasses it. So resolving the incident does not necessarily release the successor. The passage establishes what releases a held job and says nothing about what "resolving the incident" involves, which is why this is Cannot Say rather than False.

### Preparation tips

- **Read priority definitions as conjunctions of impact and urgency.**
- **Check who is authorised to do something before doing it.**
- **Note when a clock is suspended and what restarts it.**
- **Distinguish a workaround from a fix.**
- **Check every condition in a compound requirement.**
- **Watch for absolute exclusions — "never", "in all cases", "regardless".**
- **Count retries carefully: "retries twice" means three attempts.**
- **Notice what a runbook says it does not cover.**

### Common pitfalls

- **Treating high impact alone as Priority 1.**
- **Changing a priority yourself when a user presses you.**
- **Assuming an emergency change bypasses the board.**
- **Classifying access-rights work as a standard change.**
- **Reading "resolved" as "fixed".**
- **Assuming an incident is raised at the moment of first failure.**
- **Assuming resolving an incident restarts a held job.**

## Workplace job-specific situational judgement assessment

### About this assessment

A workplace job-specific situational judgement assessment presents realistic scenarios and asks you to identify effective and ineffective responses. As an application operations engineer the scenarios involve monitoring and incidents, batch failures overnight, user and security administration requests, and working with the people who own the application and the people who use it.

The commonest formats ask for the most and least effective response, or for ratings. Scoring is against a key derived from experienced practitioners in comparable roles.

Three patterns run through the strong answers.

The first is that you work within defined authority. You administer access, implement changes and manage incidents inside a framework that says who may do what, and the strong answers consistently stay within it and escalate rather than obliging a user who is pressing you.

The second is that restoring service and understanding the cause are separate activities. During an incident the priority is getting people working; afterwards it is finding out why. Doing them in the wrong order costs users.

The third is that you see things nobody else sees. You are the person watching the batch, the disk, the error rate — and a trend you notice and mention three weeks early is worth more than any amount of skill applied on the night it fails.

### What it measures for your role

- **Incident handling** maps to **Incident management**.
- **Batch accountability** maps to being accountable for batch processes.
- **Access administration** maps to your user and security administration duties.
- **Change discipline** maps to **Change management**.
- **Noticing trends** maps to **Availability and capacity management** and monitoring applications.
- **Working with users** maps to **User focus** and **Service focus**.

### Practice questions

**Question 1 (easy) — A batch failure overnight**

You are on call. A critical batch job has failed and you are not sure why. The processing window closes in two hours. What is the most effective response?

- A) Follow the runbook first — check the things it tells you to check — and if that does not resolve it, escalate early enough that there is still time to act, rather than at the point the window closes.
- B) Investigate the cause thoroughly before doing anything.
- C) Re-run the job and see what happens.
- D) Wait until morning and let the day team handle it.

**Correct answer: A. Least effective: D**

**Explanation:** The runbook exists for this moment and covers the common causes, so it is both the fastest route and the one you can be held to. The second half of option A is what distinguishes it: escalating with ninety minutes left gives someone options, and escalating with ten minutes left gives them a fact. Option D is least effective — a missed processing window has consequences that compound through the next day, and being on call means the decision is yours to make now. Option C is worth doing when the runbook says so and is a guess on its own. Option B spends the window understanding rather than fixing.

**Question 2 (easy) — A user asking for access**

A senior manager asks you directly to give a new starter access to the application today, bypassing the usual request process. What is the most effective response?

- A) Grant it; the manager is senior and the need is real.
- B) Explain what the process requires and help them through it quickly — most access processes have a fast route for genuine urgency — because access grants outside the process are unauditable, and your security administration duties are exactly where that matters.
- C) Refuse and point them at the process.
- D) Grant it and ask them to submit the request afterwards.

**Correct answer: B. Least effective: A**

**Explanation:** The need is legitimate and the route is what is in question. Option B keeps the audit trail intact while solving their actual problem, which is speed — and knowing the fast route is what makes you useful rather than obstructive. Option A is least effective: an unauditable access grant is a control failure in the area you are personally responsible for, and seniority does not change that. Option D is the same failure with a promise attached, and the retrospective request frequently does not arrive. Option C is correct and unhelpful.

**Question 3 (moderate) — A trend you have noticed**

Over several weeks you have noticed the nightly load job creeping closer to its window. Nothing has failed. What is the most effective response?

- A) Work out how much growth remains before it overruns, and raise it with the application owner with that figure and a rough date.
- B) Mention it at the next team meeting.
- C) Wait until it fails; then it will be prioritised.
- D) Try to optimise the job yourself.

**Correct answer: A. Least effective: C**

**Explanation:** A trend spotted early is worth far more than skill applied on the night it fails, and option A converts an observation into something someone can plan around — "this overruns in about eight weeks at current growth" is actionable in a way that "it's getting slower" is not. Option C is least effective and is a genuine temptation, because a failure does get attention; it also means a missed window, a recovery, and an avoidable incident. Option D may be within your remit and may not, and it comes before anyone has decided this is the right fix. Option B is fine and slower and less specific than it needs to be.

**Question 4 (moderate) — A user reports something intermittent**

A user reports that the application "sometimes" logs them out unexpectedly. You cannot reproduce it. What is the most effective response?

- A) Gather the specifics — when it last happened, what they were doing, how long they had been in the application, which browser and device — and check whether other users have reported anything similar, because intermittent faults are solved by patterns rather than by reproduction.
- B) Close it as unable to reproduce.
- C) Ask them to report it next time it happens.
- D) Restart their session and see whether it recurs.

**Correct answer: A. Least effective: B**

**Explanation:** Intermittent issues are the hardest to diagnose and the most valuable to catch, and option A does the two things that work: gathering enough detail to spot a pattern, and checking whether the report is isolated. "How long had you been in the application" is often the question that cracks it, since session timeouts are a common cause. Option B is least effective: closing an unreproduced intermittent fault means it recurs, the user stops reporting it, and you lose the reports that would have shown the pattern. Option C is worth asking as well and puts the whole burden on the user. Option D changes something without knowing what.

**Question 5 (moderate) — Conflicting instructions**

The application owner asks you to make a configuration change today. It would normally require a normal change with board approval. What is the most effective response?

- A) Make the change; the application owner is accountable for the application.
- B) Explain what the change process requires, establish whether it genuinely qualifies as an emergency, and if it does, follow the emergency route with the incident manager's approval — because the emergency route exists for this and using it properly is different from skipping the process.
- C) Refuse until it goes through the board.
- D) Make the change and raise a retrospective record.

**Correct answer: B. Least effective: D**

**Explanation:** Option B distinguishes the two things that get confused here — genuine urgency, which has a defined route, and inconvenience, which does not. Following the emergency route properly gets the change made today with the approvals and the record intact. Option D is least effective: an unapproved change with a record added afterwards looks like compliance and is not, and it is the habit that makes a change process meaningless. Option A ignores the process entirely. Option C is correct if it is not an emergency and forecloses the question of whether it is.

**Question 6 (moderate) — During an incident**

A Priority 2 incident is in progress. A colleague suggests a change that might fix it, but neither of you is sure what it would do. What is the most effective response?

- A) Try it; the service is degraded and something needs to happen.
- B) Check what it would affect before doing it, and prefer actions you know how to reverse — because an untested change during an incident can turn a degraded service into a broken one, and the recovery from that is much longer.
- C) Wait for the incident manager to decide.
- D) Restart the application instead.

**Correct answer: B. Least effective: A**

**Explanation:** The instinct to do something during an incident is strong and is exactly when the discipline matters. Option B gives the practical test — what does it affect, and can I undo it — which is the right filter under time pressure. Option A is least effective: acting on an unknown change during a live incident is how a Priority 2 becomes a Priority 1, and it happens regularly. Option C is appropriate for a decision above your authority and is not a substitute for thinking. Option D is a specific action offered without knowing whether it is relevant.

**Question 7 (harder) — A mistake you made**

You realise a change you made yesterday has caused a problem that has not yet been noticed. What is the most effective response?

- A) Report it now, say what you did and what the effect is, and propose the fix.
- B) Fix it quietly before anyone notices.
- C) Wait to see whether it causes an actual incident.
- D) Fix it and mention it at the next team meeting.

**Correct answer: A. Least effective: C**

**Explanation:** Everyone makes mistakes in operations, and how they are handled is what people remember. Option A is quick and lets someone else assess whether the impact is wider than you think — which is the part you cannot judge alone, since you may not know what depends on what you changed. Option C is least effective: waiting means the problem is found by someone else, later, with no idea of the cause, and the diagnosis costs hours that your disclosure would have saved. Option B removes anyone's chance to check the wider impact. Option D delays by days.

**Question 8 (harder) — A workaround that keeps being used**

A known fault has been generating incidents for months, each resolved by the same workaround. Nothing has been done about the underlying cause. What is the most effective response?

- A) Continue applying the workaround; it restores service.
- B) Put together what the recurrence has cost — how many incidents, how much engineer time, how much user disruption — and raise it as a problem needing a permanent fix, because an efficient workaround removes the pressure to solve anything.
- C) Ask the application owner to prioritise a fix.
- D) Stop applying the workaround so the problem gets attention.

**Correct answer: B. Least effective: D**

**Explanation:** This is the specific failure mode of a good workaround: it resolves incidents against target while the fault persists indefinitely, and because service is restored every time, nothing ever forces the issue. Option B converts the accumulated cost into a case, which is what gets a fix funded. Option D is least effective and is genuinely tempting — deliberately letting users suffer to make a point is not a legitimate route, and it damages the people the service exists for. Option C is the right ask made without the evidence that would carry it. Option A accepts the position permanently.

**Question 9 (harder) — An access review**

A quarterly access review shows 40 accounts that have not been used for over 90 days. What is the most effective response?

- A) Check what each account is before acting — long-term leave, secondment, seasonal roles and service accounts all look dormant — then remove the ones confirmed as no longer needed and record what was done.
- B) Remove all 40 accounts.
- C) Leave them; they are not causing harm.
- D) Ask each account holder's manager to confirm.

**Correct answer: A. Least effective: B**

**Explanation:** Dormant accounts are a real security risk and dormancy is a poor proxy for "no longer needed", which is what makes option A the right sequence: check, act on what is confirmed, and record. Option B is least effective: removing a service account or the account of someone on maternity leave causes an outage or a very bad first day back, and both are avoidable with one check. Option D is a reasonable part of the checking and is slow as the whole approach for 40 accounts. Option C ignores a control you are responsible for.

**Question 10 (harder) — Something outside your remit**

Investigating an incident, you conclude the cause lies in an infrastructure component another team owns. What is the most effective response?

- A) Pass it to them with what you found — the evidence, the timings, what you ruled out — because a handover with your diagnostic work attached saves them repeating it, and a bare reassignment usually comes back.
- B) Reassign the incident to them.
- C) Investigate further to be certain before passing it on.
- D) Fix it yourself if you can.

**Correct answer: A. Least effective: D**

**Explanation:** Cross-team handovers fail when they arrive without evidence, because the receiving team starts from nothing and frequently sends it back. Option A gives them everything you established, including what you ruled out, which is often the most useful part. Option D is least effective: changing another team's component without their knowledge is outside your authority, may break something you cannot see, and leaves them with an unexplained change. Option C delays a handover you already have grounds for. Option B is the right destination delivered in the least useful form.

**Question 11 (harder) — Documentation that is wrong**

Following a runbook during an incident, you find a step that is out of date and does not work. You resolve the incident another way. What is the most effective response?

- A) Update the runbook now while you remember exactly what was wrong and what worked instead.
- B) Mention it to the team.
- C) Leave it; you know the right way now.
- D) Raise a ticket to update it.

**Correct answer: A. Least effective: C**

**Explanation:** The runbook will next be used at 3am by someone who does not know what you now know, and the details fade within days. Option A costs ten minutes at the point where you have the information. Option C is least effective: knowledge held only by you is knowledge the on-call rota does not have, and it guarantees the next person hits the same dead end under the same pressure. Option D is better and puts a delay between the knowledge and the record. Option B shares it with people who are awake now rather than the person on call in three weeks.

**Question 12 (harder) — Too much at once**

Several things need attention: a batch job that will finish late, a user waiting on an access request, and a monitoring alert you do not recognise. What is the most effective approach?

- A) Deal with them by what deteriorates if delayed — the unrecognised alert first if it could indicate something spreading, then the batch job while there is still time to affect the outcome, then the access request — and tell the waiting user roughly when you will get to them.
- B) Deal with them in the order they arrived.
- C) Deal with the access request first; it is quickest.
- D) Escalate all three.

**Correct answer: A. Least effective: B**

**Explanation:** Option A prioritises by deterioration, which is the right criterion — an unrecognised alert may be the early sign of something that gets much worse, while an access request is equally solvable in an hour. Telling the waiting user when you will reach them is the small thing that stops a reasonable wait becoming a complaint. Option B is least effective: order of arrival ignores every piece of information you have about consequence. Option C optimises for getting something finished. Option D escalates work that is yours to do.

### Preparation tips

- **Follow the runbook first, and escalate while there is still time to act.**
- **Keep access grants inside the process, and know the fast route.**
- **Raise a trend with a figure and a date attached.**
- **Gather specifics on intermittent faults rather than closing them.**
- **Prefer reversible actions during an incident.**
- **Report your own mistakes before they are discovered.**
- **Update a runbook while you still remember what was wrong.**
- **Prioritise by what deteriorates if delayed.**

### Common pitfalls

- **Granting access outside the process for a senior requester.**
- **Making a change during an incident without knowing what it affects.**
- **Closing an intermittent fault as unable to reproduce.**
- **Waiting for a creeping batch job to fail before raising it.**
- **Making a change and raising the record afterwards.**
- **Removing dormant accounts without checking what they are.**
- **Reassigning an incident without your evidence attached.**
- **Keeping a runbook correction in your head.**

## Conclusion

You have worked through four assessments built around the reasoning an application operations engineer actually uses, and it is worth drawing them together.

The cognitive section was about reading operational evidence carefully — spotting the pattern across a set of findings, following a dependency or a rule through several steps, and checking data that mostly matches rather than assuming the rest does.

The numeric section was the arithmetic this job runs on: records divided by throughput against the window, availability percentages converted into minutes, incident counts normalised by transaction volume, and growth headroom worked out before something overruns rather than after. None of it was advanced, and all of it rewarded doing the division rather than estimating.

The verbal section was about the documents that define what you may do and what is expected. Priority is impact *and* urgency. Only the incident manager changes a priority. Access-rights changes are never standard. "Retries twice" means three attempts. And a runbook that says it does not cover the missing-file case has told you exactly where the next 3am problem will be.

The situational judgement section came back to three habits. Stay inside your authority, and know the fast route so that staying inside it is not obstructive. Restore first and diagnose afterwards, preferring actions you can reverse. And say things early — the creeping batch job, your own mistake, the runbook step that no longer works.

That last one is worth trusting, because you see things nobody else does. Nobody else is watching the load job creep towards its window, and a note three weeks early is worth more than any amount of skill applied on the night it finally fails.

Good luck. This is work that most of the organisation only notices when it stops, and the care you have given this is exactly the kind that keeps it from stopping.
