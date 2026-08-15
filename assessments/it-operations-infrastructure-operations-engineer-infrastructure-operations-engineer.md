# Infrastructure Operations Engineer - Psychometric Assessment Resources

## Introduction

Welcome! This guide has been created especially for you as an infrastructure operations engineer working within the UK Government Digital and Data profession. Whether you are preparing for an internal assessment, applying for your next role, benchmarking your own capability, or simply curious about how psychometric assessments connect to your daily work, this document will help you practise, reflect, and build confidence.

Psychometric assessments are structured, standardised exercises that measure the mental capabilities and behavioural tendencies that predict success in a role. For an infrastructure operations engineer, that means far more than abstract puzzles. The assessments described here are job-specific: they draw on the artefacts you genuinely handle — monitoring dashboards, incident tickets, change requests, asset and configuration records, capacity reports, test scripts, and operational documentation — and the decisions you genuinely make, such as deciding whether an alert warrants action, implementing a change request under change control, owning an issue until it is resolved or properly handed on, and keeping configuration information accurate and secure.

Why do these assessments matter for your role in particular? You are responsible for the preparation and support of IT operations solutions and services, physical or virtual, according to industry and organisational best practices, standards, service requirements and key performance indicators throughout the product life cycle. That responsibility rests on a distinctive combination of mental skills: the vigilance to monitor infrastructure and application services and spot the signal among the noise; the precision to perform routine tasks according to process and checklists without drift; the numeracy to reason about capacity, availability and KPIs; the reading discipline to apply change control procedures and follow documentation exactly; and the judgement to know when to act, when to escalate, and how to keep users informed. Cognitive, numeric, verbal, and situational assessments map directly onto those demands, which is why employers in operations roles use them.

This document is organised into four main assessment sections, each following the same pattern: an overview of what the assessment measures and why it matters for your role, a mapping of the assessment's dimensions to the specific skills in your role summary, a substantial set of practice questions with full worked explanations, practical preparation tips, and common pitfalls to avoid.

Here is how to get the most from it. First, read each "About this assessment" section so you understand the format before attempting questions. Second, attempt every practice question honestly — commit to an answer before reading the explanation. Third, treat each explanation as a mini-lesson: even when you answer correctly, the worked reasoning will sharpen your technique and often ties back to an operational habit worth keeping. Fourth, use the preparation tips and pitfalls sections for self-reflection — many of them double as good operational practice. Finally, revisit the material after a few weeks; spaced repetition is as effective for reasoning technique as it is for technical knowledge.

The questions progress from easy through moderate to hard within each section, so early success builds momentum and later challenge builds capability. Take your time, work honestly, and enjoy the practice. Let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive assessment measures the exact mental processes your role demands, using practical workplace scenarios rather than abstract puzzles. Instead of shapes and number sequences, you reason about monitoring output, configuration records, change schedules, log excerpts, and operational checklists — the daily material of infrastructure operations.

The typical format is an online, timed test lasting 15 to 30 minutes, with 20 to 30 questions covering pattern recognition, logical deduction, error checking, prioritisation, and applied problem solving. Scoring is objective, comparing your responses against a norm group, and many modern platforms adapt question difficulty to your performance as you go. Employers usually receive a breakdown of speed versus accuracy rather than a single score, so working both quickly and carefully matters. Most platforms offer short, ungraded practice questions before the real test begins, so you can settle into the interface without pressure.

For an infrastructure operations engineer, cognitive assessment is particularly relevant because operational reliability is largely a thinking discipline. Monitoring infrastructure and application services means continuously distinguishing normal variation from genuine anomaly. Alerting and taking appropriate action means reasoning quickly from symptoms to plausible causes and from causes to safe next steps. Performing routine tasks according to process and checklists means holding a procedure in mind while executing it faithfully — and noticing when reality diverges from what the procedure assumes. Maintaining accurate configuration information means constant cross-checking between records and the systems they describe. A well-designed cognitive assessment reproduces these demands in miniature: spot the inconsistency, follow the dependency chain, rank the queue, isolate the variable.

There is a practical payoff to practising, beyond any test: the techniques these questions reward — timeline reconstruction, systematic elimination, checking records field by field — are the same techniques that make incident investigation and configuration management faster and more reliable in real life.

### How this assessment maps to your role

The assessment dimensions map directly to the named skills in your role summary:

- **Pattern recognition** maps to your **Incident management** skill — identifying and registering incidents, gathering the required information and allocating them to the appropriate channel depends on recognising which alerts and symptoms belong together — and to monitoring infrastructure and applications services, where anomaly detection is pattern recognition performed continuously.
- **Logical deduction** maps to your **Problem management** skill: investigating problems in systems, processes and services, and understanding whether a problem is strategic, tactical or operational, requires valid reasoning from logs, timelines and symptoms to causes.
- **Error checking** maps to your **Asset and configuration management** skill — maintaining secure configuration and accurate information, and verifying the location and state of IT assets, is a sustained exercise in comparing records against reality — and to your **Testing** skill, where correctly executing test scripts under supervision means noticing every deviation from expected results.
- **Prioritisation** maps to your **Ownership and topic** skill (owning an issue until a new owner is found or the problem is mitigated or resolved requires ranking competing demands) and to your **Availability and capacity management** skill, where managing service components against business needs and KPIs means addressing the most service-critical risks first.
- **Applied problem solving** maps to your **Change management** skill (implementing change requests and applying change control procedures under supervision involves reasoning about sequence, dependency and rollback), your **Technical specialism** skill in support and maintenance activities, and your **Service focus** skill — taking inputs and establishing coherent frameworks that work is structured problem solving by definition.

### Practice questions

**Question 1 (easy) — Pattern recognition in monitoring output**

Your monitoring dashboard lists CPU utilisation for six production virtual machines, sampled every five minutes over the past half hour:

- VM-A: 34%, 36%, 33%, 35%, 34%, 35%
- VM-B: 41%, 40%, 42%, 41%, 43%, 41%
- VM-C: 28%, 29%, 27%, 61%, 88%, 97%
- VM-D: 55%, 54%, 56%, 55%, 54%, 55%
- VM-E: 12%, 13%, 11%, 12%, 14%, 12%
- VM-F: 47%, 46%, 48%, 47%, 45%, 47%

Which VM most warrants immediate attention, and why?

- A) VM-D, because it has the highest average utilisation.
- B) VM-C, because its utilisation is climbing steeply after a stable baseline.
- C) VM-E, because unusually low utilisation means the VM may have failed.
- D) VM-F, because 47% is close to half capacity.

**Correct answer: B**

**Explanation:** The question tests trend recognition, not level recognition. Five of the six VMs show stable readings with normal small variation. VM-C breaks pattern decisively: after a stable baseline around 28%, three successive samples show 61%, 88%, 97% — a steep, accelerating climb that will hit saturation imminently. VM-D's 55% is the highest steady level but is stable, giving no reason for urgency. VM-E's low, steady figure is consistent with a lightly loaded machine, and it is still varying normally — a failed VM would more likely report zero or stop reporting. Option D confuses an arbitrary landmark with a threshold. In monitoring work, the derivative often matters more than the value: a service at 55% forever is healthier than one that went from 28% to 97% in fifteen minutes. Alerting and taking appropriate action starts with reading trends this way.

**Question 2 (easy) — Logical deduction from a maintenance rule**

Your operational standard states: "A production server may only be rebooted during business hours if an approved emergency change exists." You learn that server APP-PRD-04 was rebooted at 14:20 on a Tuesday. Which conclusion must be true?

- A) An approved emergency change existed for the reboot.
- B) The standard was breached.
- C) Either an approved emergency change existed, or the standard was breached.
- D) The reboot was caused by a fault, not an engineer.

**Correct answer: C**

**Explanation:** The rule is conditional: a business-hours reboot is permitted only with an approved emergency change. The reboot occurred at 14:20 Tuesday — business hours — so one of exactly two situations holds: the required approval existed (rule followed) or it did not (rule breached). The facts given do not tell you which, so neither A nor B is guaranteed individually; each is merely possible. D introduces a cause the facts never mention — and note that if the reboot was a spontaneous fault rather than an action anyone took, that would complicate matters further, which is another reason not to assume it. The only conclusion true in every scenario consistent with the facts is the disjunction, C. This discipline — concluding no more than the evidence guarantees — is precisely what you exercise when investigating problems: an unexplained reboot in the logs prompts you to check the change record before writing "unauthorised reboot" in a ticket.

**Question 3 (easy) — Error checking a configuration record**

Your configuration management database (CMDB) requires each server record to contain: hostname, environment (PRD or TST), IP address, operating system with version, and assigned support team. You review this new record:

"Hostname: DB-PRD-03. Environment: PRD. IP: 10.20.31.7. OS: Linux. Support team: Database Operations."

What is wrong with the record?

- A) The IP address is in the wrong format.
- B) The operating system entry is missing its version.
- C) The environment code is invalid.
- D) Nothing — the record is complete.

**Correct answer: B**

**Explanation:** Audit the record against the requirement field by field. Hostname: present. Environment: PRD, which is one of the two valid codes. IP address: 10.20.31.7 is a validly formed address. Support team: present. Operating system: the requirement says "operating system with version", and "Linux" names the OS but omits any version. Option B is correct. This is exactly the habit that keeps a CMDB useful: "Linux" tells a patching coordinator almost nothing — whether the box needs a particular security update depends entirely on the distribution and version. Maintaining accurate information means treating each required field as a distinct check, not skimming the record for general plausibility. In assessments, resist the pull of option D whenever a record "looks fine" — completeness is verified, never assumed.

**Question 4 (easy) — Checklist logic under a changed condition**

Your nightly checklist for the application platform reads: (1) confirm the overnight batch completed; (2) if the batch completed, archive the batch logs; (3) if the batch failed, do not archive logs — raise an incident and attach the logs to it; (4) update the shift handover note. Tonight the batch failed. Which sequence of actions follows the checklist?

- A) Archive the logs, raise an incident, update the handover note.
- B) Raise an incident with the logs attached, update the handover note.
- C) Update the handover note only.
- D) Raise an incident, archive the logs, update the handover note.

**Correct answer: B**

**Explanation:** Trace the conditional branches. Step 1 establishes the batch failed. Step 2's condition ("if the batch completed") is not met, so archiving does not happen. Step 3's condition is met: raise an incident and attach the logs — and note it explicitly forbids archiving in this branch, which eliminates options A and D regardless of ordering. Step 4 is unconditional: update the handover note. That yields option B. The checklist's logic has an operational rationale worth internalising: archiving on failure would move the logs away from where the investigating engineer expects them, while attaching them to the incident keeps evidence with the investigation. Executing procedures correctly means executing their conditions, not just their verbs — the same skill as correctly executing test scripts, where the expected-result branch determines what you do next.

**Question 5 (moderate) — Deduction from a service dependency chain**

The intranet service depends on the web tier; the web tier depends on the application tier; the application tier depends on both the database tier and the authentication service. This morning: the database tier is confirmed healthy; users report the intranet is down; the authentication service's status is unknown; no other dependencies exist. Which of the following is a valid conclusion?

- A) The authentication service must be down.
- B) The fault must lie in the web tier.
- C) The fault lies in the web tier, the application tier, or the authentication service.
- D) The database tier is causing the outage.

**Correct answer: C**

**Explanation:** Model the dependency chain: intranet → web → application → (database AND authentication). The intranet is down, so at least one link in its dependency chain has failed. The database tier is confirmed healthy, which eliminates one candidate — and directly rules out option D. That leaves three possible fault locations: the web tier, the application tier, or the authentication service (whose status is unknown — unknown means unknown, not down, so option A overreaches). Option B arbitrarily selects one of three live candidates. Option C states exactly the surviving possibility set, which is the valid conclusion. This is the elimination structure of real incident diagnosis: enumerate the dependency chain, strike out what monitoring confirms healthy, and focus investigation on what remains. Writing the remaining candidate list into the incident record — rather than a premature single suspect — is what good investigation notes look like.

**Question 6 (moderate) — Prioritising a morning queue**

You start your shift with four items in your queue:

1. A monitoring alert fired 10 minutes ago: certificate on the public-facing service portal expires in 48 hours; renewal takes about an hour and is documented.
2. An incident ticket: one user cannot print to their local office printer.
3. A scheduled task due today: monthly verification of asset records for your rack row, takes two hours, deadline 17:00.
4. An email from your team lead: please peer-review a colleague's change request before the change board meets at 14:00.

It is 09:00. Which order of attention is most defensible?

- A) 1, 4, 3, 2
- B) 2, 1, 4, 3
- C) 3, 4, 1, 2
- D) 1, 2, 4, 3

**Correct answer: A**

**Explanation:** Rank by impact-weighted urgency. Item 1 is the standout: an expiring certificate on a public-facing service is a guaranteed future outage with a known deadline — and the correct operational reflex is to remove such time bombs early, while there is still margin if renewal hits a snag; an hour spent at 09:00 costs nothing and eliminates the largest risk. Item 4 has a hard mid-day deadline (the 14:00 change board) and blocks a colleague, so it comes next. Item 3 has an end-of-day deadline and two hours of work — comfortably schedulable after the review. Item 2 affects one user's local printing: real, but lowest impact, and it slots in last or between tasks. Option B elevates a single-user inconvenience above a service-affecting deadline; option C leaves the certificate — the only item that can cause a public outage — until afternoon; option D is close but delays the deadline-bound review behind low-impact work. The scoring pattern in prioritisation questions rewards sequencing by impact and deadline jointly, not by ticket age, ease, or the order items arrived.

**Question 7 (moderate) — Error checking across two artefacts**

The change schedule says: "CH-3401: increase memory on VM cluster from 256 GB to 320 GB, Wednesday 21:00." The capacity report for the same cluster says: "Current memory 256 GB; approved uplift to 384 GB scheduled Wednesday 21:00 under CH-3401." Assuming exactly one document contains a typing error, what can you conclude, and what should you do?

- A) The schedule is definitely wrong; proceed with 384 GB.
- B) The report is definitely wrong; proceed with 320 GB.
- C) The two documents disagree on the target (320 vs 384 GB); you cannot tell from these documents alone which is correct, so verify against the approved change record before Wednesday.
- D) The difference is immaterial; either figure will do.

**Correct answer: C**

**Explanation:** Compare the artefacts field by field: change reference — match (CH-3401); current memory — match (256 GB); timing — match (Wednesday 21:00); target memory — mismatch (320 GB versus 384 GB). One document has an error, but nothing in the two documents tells you which: each is equally capable of containing the typo, and options A and B each assume an answer the evidence cannot support. Option D fails on operational grounds — implementing the wrong uplift either under-delivers approved capacity or applies an unapproved larger change, and both matter under change control. Option C is the disciplined conclusion: identify the discrepancy precisely, then resolve it against the authoritative source — the approved change record — before implementation. This mirrors your daily reality of applying change control procedures: when documents disagree, the approved record arbitrates, and the discrepancy itself is worth reporting so the erroneous document gets corrected.

**Question 8 (moderate) — Pattern recognition in recurring failures**

You pull the failure history for a file transfer job over four weeks:

- Week 1: failed Tuesday 02:10, succeeded all other nights
- Week 2: failed Tuesday 02:15, succeeded all other nights
- Week 3: succeeded every night
- Week 4: failed Tuesday 02:05, succeeded all other nights

You also learn that a database maintenance job runs every Tuesday from 02:00 to 02:30, except in week 3, when it was skipped for a bank holiday. What is the strongest hypothesis?

- A) The file transfer job fails randomly.
- B) The Tuesday database maintenance job contends with the file transfer job, causing the failures; week 3's success when maintenance was skipped supports this.
- C) Bank holidays cause the file transfer job to succeed.
- D) The file transfer job is misconfigured and should be rewritten.

**Correct answer: B**

**Explanation:** Line up the two schedules. The transfer job fails only on Tuesdays, only within the 02:00–02:30 window when the maintenance job runs — three co-occurrences. The natural experiment is week 3: the one week maintenance did not run is the one week the Tuesday transfer succeeded. Presence of the suspected cause coincides with failure; absence coincides with success. That is a strong correlation with a plausible mechanism (resource contention or a lock on shared data), making B the best hypothesis. Option A ignores an obvious pattern — three failures all in the same 15-minute weekly window is not random. Option C confuses the mediating variable: the bank holiday mattered only because it removed the maintenance job. Option D leaps to a remedy with no mechanism and maximum cost. Note the epistemics: B is framed as a hypothesis supported by evidence, which is exactly the right strength — the confirming step would be examining logs from the failure window or re-timing one job. Investigating patterns like this is the heart of contributing to problem management remedies and preventative measures.

**Question 9 (moderate) — Applied problem solving on a scripted task**

A colleague's handover note says: "Run the disk-cleanup script on the four web servers, one at a time, checking each server returns to normal service before starting the next. If any server fails to return to normal service within 10 minutes, stop — do not continue with remaining servers — and page the on-call engineer." You run the script on server 1: normal within 4 minutes. Server 2: normal within 6 minutes. Server 3: after 12 minutes, it has not returned to normal service. What do you do?

- A) Continue to server 4, then investigate server 3 afterwards.
- B) Re-run the script on server 3, since a second attempt may succeed.
- C) Stop — do not touch server 4 — and page the on-call engineer about server 3.
- D) Restore server 3 from backup.

**Correct answer: C**

**Explanation:** The instruction contains an explicit stop condition: any server not back to normal within 10 minutes halts the entire sequence and triggers a page. Server 3 has breached that condition (12 minutes and counting), so the procedure demands exactly option C: stop, do not proceed to server 4, page on-call. The rationale behind such stop conditions is worth absorbing: the one-at-a-time design exists to limit blast radius — if the script harms servers, you want one damaged web server with three healthy peers carrying the load, not four damaged servers. Option A violates the stop rule and risks widening the impact. Option B improvises an unauthorised retry on an already-degraded server, potentially compounding the fault and muddying the evidence. Option D is a drastic recovery action nobody has authorised. In both assessments and operations, an explicit stop condition in a procedure is the most important sentence in it: procedures encode not just what to do, but when to stop doing it.

**Question 10 (hard) — Timeline deduction across overlapping changes**

Overnight, four events occurred on the payments platform: (i) 22:00 — storage firmware updated; (ii) 23:00 — automated health check passed all tests; (iii) 23:30 — application patch applied; (iv) 00:15 — network switch port reconfigured. At 00:40, monitoring detected elevated error rates, which have continued since. A second health check at 01:00 failed. No other changes occurred. Which statement best ranks the suspects?

- A) The storage firmware update is the prime suspect because firmware is riskiest.
- B) The application patch and the switch reconfiguration are the live suspects, with the firmware update effectively cleared by the 23:00 health check; between the two, both remain credible and should be checked, starting with the one most easily verified or reverted.
- C) The switch reconfiguration alone is the suspect because it is closest in time to the errors.
- D) All four events are equally suspect.

**Correct answer: B**

**Explanation:** Apply last-known-good reasoning. The 23:00 health check passed after the firmware update, which substantially clears event (i) — the platform demonstrably worked post-firmware (with the caveat that latent faults can pass a health check, which is why "effectively cleared", not "impossible"). Errors appeared at 00:40; between the last known good state (23:00) and first known bad state (00:40), two changes occurred: the 23:30 application patch and the 00:15 switch reconfiguration. Both precede the errors and neither has been exonerated, so both are live suspects — option C's proximity-only reasoning is weaker, because a 23:30 patch can easily take an hour to misbehave (caches expiring, first overnight batch exercising a new code path). Option B captures the correct suspect set and adds sound triage practice: check the suspect that is cheapest to verify or safest to revert first. Option A substitutes a risk stereotype for the timeline; option D discards the information the passing health check provides. This layered reasoning — bound the window, list what changed inside it, order the checks by cost — is the professional core of incident investigation.

**Question 11 (hard) — Multi-constraint scheduling of operational work**

You must complete three tasks in tonight's maintenance window (20:00–00:00): a database backup (B) taking 90 minutes; an OS patch with reboot (P) taking 60 minutes; and a storage volume expansion (S) taking 45 minutes. Constraints: (i) the backup must complete before the patch begins, because you need a clean restore point; (ii) the storage expansion cannot run at the same time as the backup, because both saturate the storage network; (iii) the patch and storage expansion can run in parallel; (iv) all tasks must finish by 00:00. If you start the backup at 20:00, what is the latest time the storage expansion can start?

- A) 21:30
- B) 22:30
- C) 23:00
- D) 23:15

**Correct answer: D**

**Explanation:** Work the constraints step by step. The backup runs 20:00–21:30 (90 minutes). Constraint (ii) forbids the expansion during the backup, so the expansion cannot start before 21:30. Constraint (i) allows the patch from 21:30; running 21:30–22:30 satisfies (iv) easily. Constraint (iii) permits the expansion to overlap the patch, so the expansion is limited only by the backup's end (not before 21:30) and the window's end (must finish by 00:00). The expansion takes 45 minutes, so its latest start is 00:00 − 45 minutes = 23:15 — option D. Option A is the earliest start, not the latest. Option B assumes the expansion must wait for the patch to finish, which constraint (iii) explicitly does not require. Option C miscalculates the 45-minute duration as 60. The technique: separate "cannot start before" constraints from "must finish by" constraints, and compute the latest start as deadline minus duration. This is exactly the reasoning you apply when packing real work into real maintenance windows — including keeping slack for things going wrong, which is why, in practice, you would not actually start at 23:15.

**Question 12 (hard) — Isolating a variable with user reports**

Users report that the document management system is slow. You gather: (i) users connecting through the VPN report severe slowness; (ii) users on office networks report normal performance; (iii) the document system's server metrics — CPU, memory, disk, response time measured at the server — are all normal; (iv) the VPN concentrator's bandwidth graph shows it has been running at 98–100% capacity since Monday, when a new large team began working remotely. What is the most defensible conclusion?

- A) The document management system needs more server capacity.
- B) The evidence points to the saturated VPN concentrator, not the document system: the symptom tracks the connection path, the server itself measures healthy, and the saturation onset coincides with the new remote team's arrival.
- C) The new team is misusing the document system and should be told to stop.
- D) Users on the VPN are imagining the slowness, since server metrics are normal.

**Correct answer: B**

**Explanation:** Isolate the discriminating variable. The user population splits cleanly by connection path: VPN users suffer, office users do not — so the cause plausibly lies on the VPN path, not in the shared destination. Fact (iii) corroborates: the server answers quickly as measured locally, so delay is being added in transit. Fact (iv) supplies mechanism and timing: a concentrator pinned at 98–100% since Monday, coinciding with a new remote workload, is a textbook bottleneck. Option B assembles all four facts into a coherent, testable conclusion. Option A proposes spending on a component the evidence exonerates. Option C moralises a capacity problem — the new team's traffic is legitimate demand, and this becomes an availability and capacity management action: the concentrator needs an uplift or traffic management. Option D commits the classic operations sin of preferring metrics over users: server-side metrics measure the server, not the user's experience, and the two diverge precisely when the network is the problem. This question rehearses your user focus skill in its most practical form — using quantitative data and user reports together to locate the truth.

### Preparation tips

- **Practise with your own dashboards and records.** The strongest preparation is deliberate use of the artefacts you already handle: read a CPU graph and name the trend; audit a CMDB record field by field; reconstruct last week's incident as a timeline. Every technique in this section has a daily-work twin.
- **Master last-known-good reasoning.** For any question (or incident) involving events in time, anchor the last moment things were verified working, list every change after it, and treat those as your suspect set. It converts confusion into a short checklist.
- **Check conditions before verbs.** Procedures and checklist questions hide their logic in "if", "unless", and "only if". Identify which branch reality has selected before deciding what actions follow.
- **Enumerate before eliminating.** For dependency and diagnosis questions, write out the full candidate set first, then strike out what the evidence clears. Answers chosen from a complete list are far more reliable than answers that spring to mind.
- **Rehearse under mild time pressure.** Once techniques feel comfortable, practise at roughly a minute per question. Speed in these tests comes from recognising question archetypes — trend versus level, must-be-true versus could-be-true, latest-start versus earliest-start — not from rushing arithmetic.
- **Use the platform's practice questions.** Real assessments almost always offer unscored warm-up questions. Use them to settle nerves, learn the interface, and calibrate your pace before the clock matters.

### Common pitfalls to avoid

- **Reasoning from stereotypes instead of evidence.** "Firmware is risky", "patches break things", "it's always the network" — assessments deliberately bait these reflexes. The correct answer follows the timeline and the facts, not the folklore.
- **Confusing "possible" with "must".** Deduction questions reward the conclusion guaranteed by the facts. If you can imagine a consistent scenario where an option is false, it is not a "must be true".
- **Treating unknown as known.** "Status unknown" means exactly that — it neither convicts nor clears a component. Keep unknowns in the suspect set until evidence removes them.
- **Ignoring stop conditions and exceptions.** The most heavily tested sentence in any procedure question is the exception clause. Read "unless", "do not continue", and "only if" twice.
- **Prioritising by ease or recency.** Queues are ranked by impact and deadline together. The tempting wrong options rank by what arrived last, what is easiest, or who asked loudest.
- **Trusting a record because it looks complete.** Field-by-field verification is the only reliable check, in tests and in configuration management alike. "Looks fine" is where errors live.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment measures how accurately and confidently you work with the quantitative material of your job: percentages, ratios, averages, rates, and data presented in tables and charts. For an infrastructure operations engineer, the data is drawn from the sources you use daily — capacity reports, availability figures, incident statistics, backup success rates, storage growth trends, and KPI dashboards.

The typical format is an online, timed test of 20 to 35 minutes with 15 to 25 questions. Each question presents data and asks you to calculate a value, compare quantities, or interpret a trend. An on-screen calculator is normally permitted, and rough working on paper is expected. Scoring compares accuracy and speed against a norm group; some platforms adapt difficulty as you progress. Unscored practice questions usually precede the real test.

Why does numeric reasoning matter so much for your role? Because the KPIs you work to are numbers, and misreading them has operational consequences. Availability targets are percentages with unforgiving arithmetic behind them — the difference between 99.5% and 99.9% is a factor of five in permitted downtime. Capacity management is applied trend arithmetic: a disk growing at a steady rate has a computable date on which it becomes an incident. Incident statistics drive decisions about staffing and problem investigations, and those decisions are only as good as the rates and averages they rest on. Your role summary makes this explicit: you manage service components to ensure they meet business needs and key performance indicators. That phrase quietly assumes you can read, compute, and challenge KPI figures — which is precisely what this assessment measures.

A reassurance: the mathematics involved never exceeds confident everyday arithmetic — the four operations, percentages, and averages. The difficulty in good numeric questions lies in choosing the right calculation and the right baseline, not in the calculation itself. Every explanation below shows the arithmetic step by step, so you can audit your own method against it. Work for accuracy first; speed follows from method.

### How this assessment maps to your role

- **Percentages and thresholds** map to your **Availability and capacity management** skill: availability targets, utilisation thresholds, and headroom calculations are the daily language of managing service components against KPIs.
- **Rates and trend projection** map to your **Problem management** skill — investigating patterns and trends in failures means computing rates over time — and to capacity forecasting, where growth per week converts directly into time-to-exhaustion.
- **Averages and distributions** map to your **Incident management** skill: mean resolution times, ticket volumes per day, and the difference between a typical day and an outlier day are statistical readings of the incident queue.
- **Reading tables and charts** maps to your **Asset and configuration management** skill (asset counts, licence reconciliations, and audit coverage are tabular data) and to your **Testing** skill, where analysing results means comparing pass counts and failure rates against expectations.
- **Applied cost and resource arithmetic** maps to your **Service focus** and **Change management** skills: coherent operational frameworks and well-planned changes rest on correctly computed durations, capacities, and margins.

### Practice questions

**Question 1 (easy) — Utilisation percentage**

A storage array has a total capacity of 80 TB, of which 52 TB is currently used. What is the utilisation percentage?

- A) 60%
- B) 65%
- C) 68%
- D) 72%

**Correct answer: B**

**Explanation:** Utilisation = (used ÷ total) × 100. Step 1: 52 ÷ 80 = 0.65. Step 2: 0.65 × 100 = 65%. Sense-check with landmarks: half of 80 is 40, so 52 is clearly above 50%; three-quarters of 80 is 60, so 52 is below 75%. The answer must sit between 50% and 75%, and 65% fits. Landmark checking takes two seconds and catches decimal slips — the same reflex that lets you glance at a capacity dashboard and notice a figure that cannot be right.

**Question 2 (easy) — Downtime from an availability figure**

A service achieved 99% availability over a 30-day month. A 30-day month contains 720 hours. For how many hours was the service unavailable?

- A) 0.72 hours
- B) 3.6 hours
- C) 7.2 hours
- D) 14.4 hours

**Correct answer: C**

**Explanation:** Unavailability = 100% − 99% = 1% of the period. Step 1: convert 1% to a decimal: 0.01. Step 2: 720 × 0.01 = 7.2 hours. So the service was down about 7 hours 12 minutes across the month. Option A is the decimal-place trap (0.1%), and option B corresponds to 0.5%. It is worth memorising the shape of this conversion: each "nine" you add divides permitted downtime by ten — 99% of a month is about 7.2 hours down, 99.9% is about 43 minutes. Fluency here lets you translate availability KPIs into concrete outage budgets, which is how capacity and availability conversations become practical.

**Question 3 (easy) — Average incident volume**

Your team logged the following incident counts over four weeks: 84, 91, 78, 95. What was the average (mean) weekly incident count?

- A) 85
- B) 87
- C) 88
- D) 90

**Correct answer: B**

**Explanation:** Mean = total ÷ number of weeks. Step 1: sum the counts: 84 + 91 = 175; 175 + 78 = 253; 253 + 95 = 348. Step 2: divide by 4: 348 ÷ 4 = 87. The mean weekly volume is 87 incidents. Note the spread: actual weeks ranged from 78 to 95, so a week of 95 is within normal variation around this mean, not automatically a crisis. When incident statistics feed problem investigations, distinguishing normal variation from genuine change is the first analytical step — and it starts with knowing the mean and the range.

**Question 4 (easy) — Patch compliance percentage**

Of 240 servers in your estate, 216 have received this month's security patch. What percentage of the estate is patched?

- A) 85%
- B) 88%
- C) 90%
- D) 92%

**Correct answer: C**

**Explanation:** Percentage patched = (patched ÷ total) × 100. Step 1: 216 ÷ 240 = 0.9. Step 2: 0.9 × 100 = 90%. Alternatively, work with the unpatched remainder: 240 − 216 = 24 unpatched; 24 ÷ 240 = 0.1 = 10% unpatched; 100% − 10% = 90% patched. Computing the small side and subtracting is often quicker and less error-prone. Operationally, the unpatched count is the actionable number — 24 named servers needing attention — which is why patch reports usually show both the percentage (for the KPI) and the count (for the work).

**Question 5 (moderate) — Storage growth projection**

A file share currently uses 3.0 TB of its 4.2 TB volume. Usage has grown steadily by 150 GB per month (1 TB = 1,000 GB). Your team's standard requires action when a volume reaches 90% utilisation. In how many months will the volume reach the 90% action threshold?

- A) 4 months
- B) 5.2 months
- C) 8 months
- D) 12 months

**Correct answer: B**

**Explanation:** Step 1: find the threshold in absolute terms: 90% of 4.2 TB = 0.9 × 4.2 = 3.78 TB. Step 2: find the growth headroom before the threshold: 3.78 − 3.0 = 0.78 TB = 780 GB. Step 3: divide by the monthly growth: 780 ÷ 150 = 5.2 months. The volume crosses the action threshold in about five months. Option C (8 months) is the trap for projecting to 100% full (1,200 GB remaining ÷ 150) — but the question asks about the 90% action point, not exhaustion. This distinction is the whole point of thresholds in capacity management: they convert "when will it be full?" into "when must we act?", building in time to procure and implement. Time-to-threshold = (threshold level − current level) ÷ growth rate is among the most used formulas in operations.

**Question 6 (moderate) — Reading a KPI table**

The monthly service report shows four KPIs:

| KPI | Target | Achieved |
|---|---|---|
| Availability | ≥ 99.5% | 99.7% |
| Incidents resolved within SLA | ≥ 90% | 87% |
| Change success rate | ≥ 95% | 96% |
| Backup success rate | ≥ 98% | 98% |

How many KPIs met or exceeded their target?

- A) 1
- B) 2
- C) 3
- D) 4

**Correct answer: C**

**Explanation:** Evaluate each row against its target, noting every target here is a "greater than or equal to" condition. Availability: 99.7 ≥ 99.5 — met. Incidents within SLA: 87 ≥ 90 is false — missed. Change success: 96 ≥ 95 — met. Backup success: 98 ≥ 98 — met, because "at least 98" includes exactly 98; equality satisfies a ≥ target. Three KPIs met, one missed: option C. Two traps live in this simple table: forgetting that meeting a target exactly counts as achieving it, and letting the "good" rows distract from identifying the one that missed — which, operationally, is the row that drives action: why did 13% of incidents breach SLA, and is there a pattern worth a problem record?

**Question 7 (moderate) — Percentage change in resolution time**

Last quarter, the mean incident resolution time was 8.0 hours. This quarter it is 6.0 hours. What is the percentage improvement (reduction) in mean resolution time?

- A) 20%
- B) 25%
- C) 30%
- D) 33%

**Correct answer: B**

**Explanation:** Percentage change = (change ÷ original) × 100. Step 1: the change is 8.0 − 6.0 = 2.0 hours. Step 2: divide by the original value: 2.0 ÷ 8.0 = 0.25. Step 3: 0.25 × 100 = 25%. Resolution time fell by 25%. Option D is the classic reversed-baseline trap: 2.0 ÷ 6.0 ≈ 33% would be the answer only if the question asked by what percentage this quarter's time would need to rise to get back to last quarter's — percentage changes are not symmetric. Always anchor the denominator to the "from" value. When you quote improvements in service reports, this distinction determines whether your figures survive scrutiny.

**Question 8 (moderate) — Ratio allocation of virtual resources**

A physical host with 96 GB of allocatable memory is to be divided among three VMs in the ratio 3 : 2 : 1 (application : database : monitoring). How much memory does the database VM receive?

- A) 16 GB
- B) 24 GB
- C) 32 GB
- D) 48 GB

**Correct answer: C**

**Explanation:** Step 1: total the ratio parts: 3 + 2 + 1 = 6 parts. Step 2: size one part: 96 ÷ 6 = 16 GB. Step 3: the database VM gets 2 parts: 2 × 16 = 32 GB. Verify by summing all shares: application 3 × 16 = 48, database 32, monitoring 16; 48 + 32 + 16 = 96 — matches the total, confirming the split. Option D is the application share and option A the monitoring share — ratio questions punish grabbing the wrong position, so always label the parts before multiplying. This total-parts method applies unchanged to dividing CPU shares, bandwidth, licence counts, or budget across services.

**Question 9 (moderate) — Backup window arithmetic**

Your nightly backup copies 5.4 TB of data. The backup system sustains a throughput of 600 GB per hour (1 TB = 1,000 GB). The backup window runs from 22:00 to 07:00. How much spare time remains in the window after the backup completes?

- A) No spare time — the backup overruns the window.
- B) 1 hour
- C) 2 hours
- D) 3 hours

**Correct answer: A**

**Explanation:** Step 1: convert the data volume: 5.4 TB = 5,400 GB. Step 2: compute the backup duration: 5,400 ÷ 600 = 9 hours. Step 3: compute the window length: 22:00 to 07:00 is 9 hours... check that carefully: 22:00 to midnight is 2 hours, midnight to 07:00 is 7 hours, total 9 hours. Step 4: compare: the backup takes exactly 9 hours in a 9-hour window — zero spare time, and any slowdown, retry, or late start overruns. The strictly correct arithmetic answer to "spare time" is zero, and option A is the operationally correct reading: a job that exactly fills its window has no margin and will overrun in practice whenever throughput dips. The lesson doubles for real capacity planning: a plan that works only at nominal throughput is a plan that fails on bad nights. Windows need explicit headroom — and a growth trend on that 5.4 TB makes this backup a problem ticket waiting to be raised.

**Question 10 (hard) — Weighted average across teams**

Two teams handle incidents for a shared service. Team A resolved 60 incidents with a mean resolution time of 4.0 hours. Team B resolved 20 incidents with a mean resolution time of 8.0 hours. What is the overall mean resolution time across both teams?

- A) 5.0 hours
- B) 5.5 hours
- C) 6.0 hours
- D) 6.5 hours

**Correct answer: A**

**Explanation:** Averages combine through totals, weighted by volume — never by averaging the averages. Step 1: total hours for Team A: 60 × 4.0 = 240 hours. Step 2: total hours for Team B: 20 × 8.0 = 160 hours. Step 3: combined total: 240 + 160 = 400 hours across 60 + 20 = 80 incidents. Step 4: overall mean: 400 ÷ 80 = 5.0 hours. Option C (6.0) is the unweighted trap — (4 + 8) ÷ 2 — which would be correct only if both teams handled equal volumes; in fact Team A handled three times as many incidents, so the overall mean sits three times closer to A's figure. Weighted averaging matters whenever you consolidate KPIs across teams, services, or months of different sizes: the headline number in a service report is wrong if someone averaged the averages.

**Question 11 (hard) — Compound growth in capacity planning**

A database currently occupies 400 GB and grows by 10% per month (compound — each month's growth is 10% of the new, larger size). Approximately how large will it be after three months?

- A) 520 GB
- B) 528 GB
- C) 532 GB
- D) 540 GB

**Correct answer: C**

**Explanation:** Compound growth multiplies repeatedly rather than adding a fixed amount. Step 1: after month one: 400 × 1.10 = 440 GB. Step 2: after month two: 440 × 1.10 = 484 GB. Step 3: after month three: 484 × 1.10 = 532.4 GB ≈ 532 GB. Equivalently, 400 × 1.10³ = 400 × 1.331 = 532.4. Option A (520) is the simple-growth trap: adding 3 × 40 GB assumes each month grows by 10% of the original size, understating the true figure — and the understatement widens every month. Distinguishing linear from compound growth changes capacity forecasts dramatically over long horizons: at 10% compound, this database doubles in roughly seven to eight months, not the ten months linear thinking suggests. When you forecast resource needs, check whether the growth mechanism is a steady increment (log rotation, fixed daily loads) or proportional to size (usage that scales with an expanding user base) and model accordingly.

**Question 12 (hard) — Rates versus counts in a failure report**

The quarterly report for an automated job scheduler shows:

| Month | Failed jobs | Total jobs run |
|---|---|---|
| April | 40 | 8,000 |
| May | 66 | 12,000 |
| June | 78 | 15,600 |

A manager comments: "Failures have nearly doubled since April — the scheduler is deteriorating." What do the failure rates show?

- A) The rates confirm deterioration: failures per job are rising each month.
- B) The failure rate is constant at 0.5% across all three months; failure counts rose only because job volume nearly doubled, so per-job reliability is unchanged.
- C) The failure rate is falling, so reliability is improving.
- D) Rates cannot be computed from this table.

**Correct answer: B**

**Explanation:** Compute rate = failures ÷ total jobs for each month. April: 40 ÷ 8,000 = 0.005 = 0.5%. May: 66 ÷ 12,000 = 0.0055 = 0.55%. June: 78 ÷ 15,600 = 0.005 = 0.5%. The rate is essentially flat at 0.5% (May's 0.55% is a minor wobble, not a trend), while total job volume grew from 8,000 to 15,600 — which is why raw failures rose from 40 to 78. The manager's alarm rests on counts without denominators. Option B is the accurate reading: per-job reliability is stable; the growth in failures is a volume effect. That said, the finding is not "nothing to do": 78 failures a month still consume investigation effort, and a constant failure rate on a doubling workload doubles the absolute rework — a capacity observation worth making. The professional skill here is presenting both count and rate: the rate answers "is it getting worse?", the count answers "how much work is it causing?". Reports that show only one invite wrong decisions.

### Preparation tips

- **Drill the five core methods.** Percentage of a quantity; percentage change against the original baseline; time-to-threshold from a growth rate; weighted averages via totals; ratio splits via total parts. Between them, they cover the large majority of operations-flavoured numeric questions.
- **Write intermediate values down.** Even simple chains (convert units, subtract, divide) lose accuracy when held mentally under time pressure. One line of rough working per step keeps errors visible and recoverable.
- **Fix the units before calculating.** TB versus GB, hours versus minutes, per-week versus per-month. Convert everything to one unit at the start, and confirm the answer is in the unit the question requests.
- **Sense-check every answer against a landmark.** More or less than half? Above or below 10%? Roughly what magnitude? A two-second estimate catches the majority of calculator and decimal errors.
- **Practise on live operational data.** Compute the utilisation of a real volume, the time-to-threshold of a growing share, or last month's true weighted resolution time. Methods rehearsed on data you care about become automatic in tests.
- **Manage the clock deliberately.** Answer easy questions briskly and bank the marks; flag any question consuming more than double your average pace, choose the best-supported option, and move on.

### Common pitfalls to avoid

- **Averaging averages.** Combine group means through volumes and totals. Unweighted averages of unequal groups are the single most common professional-level numeric error, in tests and in service reports.
- **Wrong percentage baseline.** "Change from X" divides by X. Reversing the denominator turns 25% into 33% and hands you a plausible wrong answer that the test deliberately lists.
- **Projecting to the wrong endpoint.** Read whether the question asks for time to a threshold (90%, action point) or to exhaustion (100%). Both appear as options; only one is asked.
- **Confusing linear with compound growth.** Fixed increments add; proportional growth multiplies. Check the growth mechanism before projecting, and expect compound answers to exceed linear ones.
- **Reading counts without denominators.** Whenever a table offers both an event count and a volume, the examiner almost certainly wants the rate. Counts alone mislead when volumes change.
- **Missing the boundary condition.** "At least 98" is met by exactly 98; "more than 98" is not. Targets with ≥, >, ≤ and < are evaluated strictly by their operators — one symbol changes the verdict.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment measures how precisely you read, interpret, and draw conclusions from written material — using documents of the kinds your role genuinely handles: operational procedures, change control policies, service standards, incident reports, supplier notices, and correspondence with users and service desks.

The typical format is an online, timed test of 15 to 25 minutes. You read a short passage and answer questions about it. The dominant question type is true/false/cannot-say: deciding whether a statement is guaranteed by the passage, contradicted by it, or simply not determinable from it. Supporting types include best-summary questions, meaning-in-context questions, and clear-writing judgements. Scoring rewards accuracy under time pressure and — critically — rewards answering strictly from the passage rather than from background knowledge.

Why is verbal precision so central to infrastructure operations? Consider what your role summary asks of you: create and maintain documentation; perform all routine tasks according to process and checklists; apply change control procedures. Every one of those is a reading-and-writing discipline. A change procedure that says a change "must not proceed without CAB approval unless designated an emergency change" contains three load-bearing qualifiers, and misreading any of them produces either an unauthorised change or an unnecessarily blocked one. The documentation you create is executed by colleagues at 3 a.m. under pressure — ambiguity you leave in a procedure becomes someone else's outage. And your service management framework knowledge is, in large part, knowledge of precisely defined terms: the difference between an incident and a problem, a standard change and a normal change, is definitional, and definitions are read.

The golden rule for this section: answer from the passage alone. Your operational experience is an asset at work and a hazard in this test — the examiners deliberately write statements that are true in the real world but unsupported by the passage, and vice versa. If the passage does not state it, and it does not follow necessarily from what the passage states, the answer is "cannot say".

### How this assessment maps to your role

- **Comprehension of procedures and standards** maps to your **Change management** skill (implementing change requests and applying change control procedures under supervision is faithful reading in action) and your **Service management framework knowledge**, where a Level 3 qualification rests on precise understanding of defined terms and processes.
- **True/false/cannot-say discipline** maps to your **Problem management** skill: separating what the evidence states from what you are tempted to infer is the same restraint that keeps investigation notes factual, and your **Testing** skill applies it too — understanding the role of testing means reading expected results exactly as written.
- **Inference and summary** map to your **Incident management** and **Ownership and topic** skills: gathering required information, and owning an issue until a new owner is found, both depend on absorbing written reports accurately and handing them on without distortion.
- **Clear-writing judgement** maps to your duty to **create and maintain documentation** and to your **User focus** skill: collating user needs evidence and communicating with users requires writing that the intended reader — often non-technical — can act on. It also touches your **Coding and scripting** knowledge: describing scripting tools accurately for colleagues is a documentation task.

### Practice questions

**Question 1 (easy) — Reading a change control rule**

Read this extract from the change policy:

"Normal changes must be submitted to the Change Advisory Board (CAB) at least five working days before the proposed implementation date. Standard changes — pre-approved, low-risk, routine changes performed via a documented procedure — may be implemented without CAB submission. Emergency changes may be implemented before approval, but must be reviewed retrospectively at the next CAB meeting."

Statement: "All changes must be approved by the CAB before implementation."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** The passage describes two explicit exceptions to prior CAB approval: standard changes "may be implemented without CAB submission", and emergency changes "may be implemented before approval". A statement claiming all changes need prior CAB approval is therefore contradicted by the passage — false. The technique: universal claims ("all", "every", "always") are falsified by a single counterexample, and well-written policy passages usually contain the counterexample in plain sight. This maps directly to real change work: knowing which category a change falls into determines its approval path, and the categories are creatures of exact wording.

**Question 2 (easy) — What the notice does not say**

Read this supplier notice:

"From 1 October, version 4 of the backup agent will no longer receive security updates. Customers are advised to upgrade to version 5 before this date. Version 5 requires a minimum of 8 GB of memory on the host server."

Statement: "Version 4 of the backup agent will stop working on 1 October."

- A) True
- B) False
- C) Cannot say

**Correct answer: C**

**Explanation:** The notice says version 4 stops receiving security updates — it says nothing about the software ceasing to function. Unsupported software commonly continues running (that is precisely why unsupported software is a risk: it runs, unpatched). But be careful of the reverse over-reach too: the passage does not state that version 4 will keep working either. Since the passage neither guarantees nor contradicts the statement, the answer is "cannot say". Distinguishing "unsupported" from "non-functional" is not pedantry — it is the difference between an urgent outage-prevention task and a security risk-management task, with different priorities, communications, and timelines. Precise reading of supplier notices is a routine part of maintaining services through their life cycle.

**Question 3 (easy) — Identifying the required action**

Read this extract from the incident process:

"On receiving a monitoring alert for a production service, the engineer must first check whether an incident already exists for the affected service. If one exists, the alert details must be added to the existing incident. If none exists, a new incident must be raised and categorised. Duplicate incidents for the same underlying event must not be created."

A production alert arrives for the payroll service. You check and find an open incident for the payroll service covering the same event. According to the passage, what do you do?

- A) Raise a new incident and link it to the old one.
- B) Add the alert details to the existing incident.
- C) Close the existing incident and raise a fresh one.
- D) Ignore the alert, since an incident already exists.

**Correct answer: B**

**Explanation:** The passage prescribes a two-branch procedure, and your check has determined which branch applies: an incident exists, so "the alert details must be added to the existing incident" — option B verbatim. Option A creates precisely the duplicate the final sentence forbids. Option C destroys the incident history for no stated reason. Option D fails the first branch's requirement: adding the alert details is mandatory, not optional — the new alert may carry diagnostic information the investigation needs. Note the question's structure: it did the condition-checking for you and asked only for faithful execution. Real alert handling is the same discipline with the checking included, which is why "identify and register incidents, allocating to the appropriate channel" is a reading skill as much as a technical one.

**Question 4 (easy) — Meaning in context**

Read this line from a colleague's handover note:

"The disk replacement on FIL-PRD-02 is done, but the array is still rebuilding — expect degraded performance until it completes; don't schedule the backup verification until then."

In this note, "until it completes" refers to the completion of:

- A) The disk replacement.
- B) The array rebuild.
- C) The backup verification.
- D) The handover.

**Correct answer: B**

**Explanation:** Resolve the pronoun by proximity and sense. The disk replacement is described as already "done", so it cannot be the thing still awaited — eliminating A. The backup verification has not started (it must not be scheduled yet), so "completes" cannot refer to it — eliminating C. The one process described as ongoing is the array rebuild ("still rebuilding"), and both consequences in the sentence — degraded performance, delayed verification — hang on its completion. Pronoun resolution sounds like a grammar exercise, but in operational handovers it determines what you wait for and when you act; a misread "it" in this note could trigger a backup verification against a degraded array, producing misleading results. When you create and maintain documentation, the fix is to repeat the noun: "until the rebuild completes" costs three words and removes the ambiguity.

**Question 5 (moderate) — Combining two rules**

Read this extract from the access policy:

"Administrative access to production servers must be requested through the access management system and approved by the service owner. All administrative sessions on production servers are logged, and the logs are reviewed weekly by the security team. Access not used for 90 days is automatically revoked."

Statement: "An engineer whose approved administrative access was granted 100 days ago, and who has never used it, no longer has that access."

- A) True
- B) False
- C) Cannot say

**Correct answer: A**

**Explanation:** Chain the relevant rule to the case. The policy states access not used for 90 days is automatically revoked. The engineer's access is 100 days old and has never been used — so it has been unused for 100 days, exceeding 90. The automatic revocation applies; the access is gone. The statement follows necessarily from the passage: true. Notice what makes this "true" rather than "cannot say": the passage's rule is automatic ("is automatically revoked"), not discretionary ("may be revoked") — had the wording been "may", the answer would flip to "cannot say", because discretion leaves the outcome undetermined. One modal verb changes the verdict. Reading policies at this resolution is exactly the skill that maintaining secure configuration and managing access-related assets demands.

**Question 6 (moderate) — Choosing the accurate summary**

Read this incident report extract:

"At 09:12 the load balancer began returning errors for approximately 30% of requests to the licensing service. The on-call engineer failed over to the standby load balancer at 09:31, restoring full service. The failed unit was found to have a corrupted configuration following an automatic firmware update at 03:00. The supplier has been asked to confirm whether the firmware version is faulty. Pending their response, automatic firmware updates have been disabled on both units."

Which is the most accurate summary?

- A) "A faulty firmware version corrupted the load balancer configuration; the supplier has confirmed the fault and updates are disabled."
- B) "Partial errors from 09:12 were resolved by failover at 09:31; the failed unit had a corrupted configuration after an automatic firmware update; supplier confirmation of a firmware fault is awaited, and automatic updates are disabled meanwhile."
- C) "The licensing service was completely down for 19 minutes due to a supplier error."
- D) "The standby load balancer corrupted its configuration at 03:00 and was replaced at 09:31."

**Correct answer: B**

**Explanation:** Test each summary's claims against the report. Option A upgrades two things: it asserts the firmware version was faulty (the report only says confirmation has been requested) and says the supplier "has confirmed" (explicitly still pending). Option C converts 30% errors into "completely down" and asserts supplier fault as established. Option D misassigns the corruption to the standby unit — it was the active unit that failed; the standby restored service — and invents a replacement. Option B preserves every fact at its stated strength: the partial impact, the timeline, the found condition (corrupted configuration — a fact), the suspected cause (firmware — a hypothesis awaiting confirmation), and the interim mitigation. Summarising without altering claim strength is the difference between a handover colleagues can trust and one that spreads misinformation — and it is the precise skill best-summary questions are built to measure.

**Question 7 (moderate) — Inference from a service desk email**

Read this email:

"Since the office move completed on Friday, we have logged 26 tickets from Building C users unable to reach the print service, versus none from Buildings A and B. The print server itself shows no errors and users in A and B are printing normally. Building C was recabled during the move. Could your team check the network path from Building C before we escalate to the cabling contractor?"

Which conclusion is best supported?

- A) The cabling contractor made an error in Building C.
- B) The print server is faulty.
- C) The fault pattern — confined to Building C, beginning after the move, with the server and other buildings unaffected — makes the Building C network path the right place to investigate first.
- D) The 26 users have misconfigured their laptops.

**Correct answer: C**

**Explanation:** The email establishes a differential: one building affected, two unaffected, onset coinciding with a recabling event in the affected building, destination server healthy and reachable from elsewhere. That pattern localises the likely fault to the path between Building C and the print service — which is exactly what the email requests be checked. Option C states this at the correct strength: "the right place to investigate first", not "proven". Option A may eventually prove true, but the email itself is explicitly one step short of blaming the contractor — that is why it asks for a check "before we escalate". Option B is contradicted (no server errors; A and B print normally). Option D asks you to believe 26 independent identical misconfigurations arose simultaneously — vanishingly unlikely and unsupported. The reading skill here mirrors the diagnostic skill: locate what the evidence localises, and hold conclusions at the evidence's strength.

**Question 8 (moderate) — Conditional instructions with an exception**

Read this extract from the patching runbook:

"Apply patches to servers in the order listed in Appendix A. After each server, run the verification script. If verification passes, continue to the next server. If verification fails, revert the patch on that server and continue to the next server — unless the failed server is a domain controller, in which case stop all patching and notify the infrastructure lead before proceeding."

You patch the fifth server on the list — a file server — and its verification fails. According to the runbook, what do you do?

- A) Stop all patching and notify the infrastructure lead.
- B) Revert the patch on the file server and continue to the sixth server.
- C) Retry the patch on the file server before deciding.
- D) Continue to the sixth server without reverting, and log the failure.

**Correct answer: B**

**Explanation:** Walk the conditional tree. Verification failed, so the failure branch applies: revert and continue — unless the server is a domain controller. The failed server is a file server, so the exception does not trigger, and the default failure action stands: revert the patch, move to the next server — option B. Option A applies the exception to a case outside its scope; the stop-everything response is reserved for domain controllers, presumably because a domain controller failure has estate-wide implications. Option C invents a retry the runbook does not offer, and option D skips the mandatory revert, leaving a server in a failed, patched state. The pattern to internalise: locate the default rule, locate the exception, check whether the exception's condition is met, and only then act. Exception clauses are where runbook questions — and real 2 a.m. patching decisions — are won and lost.

**Question 9 (moderate) — Clear-writing judgement for documentation**

You are writing the first line of a procedure that colleagues will follow during incidents. Which opening line is best?

- A) "In the event that circumstances should arise wherein the service becomes unresponsive, it may be considered appropriate for remediation activities to be initiated by the responsible party."
- B) "If the service stops responding, the on-call engineer must restart it using the steps below."
- C) "Service unresponsiveness remediation initiation procedure follows."
- D) "As everyone knows, the usual thing to do when it breaks is the standard restart."

**Correct answer: B**

**Explanation:** Judge each line as an instruction to be executed under pressure. Option B is direct, active, and complete: a clear trigger condition ("if the service stops responding"), a named actor ("the on-call engineer"), a mandatory verb ("must restart"), and a pointer to the method ("the steps below"). Option A buries the same content in passive, hedged officialese — "may be considered appropriate" fails to say whether action is required, and "the responsible party" names no one. Option C is a noun pile-up that gives no instruction at all. Option D assumes shared knowledge ("as everyone knows", "the usual thing") — precisely what documentation exists to eliminate, since the reader at 3 a.m. may be a new starter. Government guidance on writing favours short sentences, active voice, named actors, and unambiguous obligation ("must" versus "may") — and operational documentation needs those qualities most of all, because its readers act on it immediately. Creating and maintaining documentation is in your role summary; this judgement is that duty in miniature.

**Question 10 (hard) — Scope tracking across a standard**

Read this extract from the logging standard:

"All production servers must forward system logs to the central platform in near real time. Application logs must also be forwarded where the application supports remote logging; where it does not, application logs must be retained locally for 90 days. Test servers are outside the scope of this standard."

Statement: "A production server running an application that does not support remote logging is in breach of the standard if its application logs are only retained locally."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** Track which rule governs the case. The server is production, so the standard applies (test servers are excluded, but this is not one). Its application does not support remote logging, so the applicable rule is the fallback: "application logs must be retained locally for 90 days." Local-only retention is therefore not a breach — it is exactly what the standard prescribes for this case, provided the 90-day retention is met. The statement claims local-only retention constitutes a breach; the passage contradicts this, so the statement is false. The subtlety: the statement says "only retained locally" as if local retention were a deficiency, inviting you to import the headline rule ("must forward") while missing that the passage itself carves out this case. One caution — if the server also failed the 90-day requirement, there would be a breach, but the statement does not say retention fell short, and adding that assumption would be your addition, not the passage's. Standards are systems of scoped rules; compliance judgements attach cases to the right rule first.

**Question 11 (hard) — Reconciling documents by recency and authority**

Read these two extracts.

Extract 1, from the published service catalogue: "The reporting service is available 24/7, with support hours 08:00–18:00 Monday to Friday."

Extract 2, from a service notice emailed yesterday by the service owner: "From next Monday, the reporting service moves to an overnight maintenance model: the service will be unavailable 02:00–04:00 daily. The catalogue entry will be updated to reflect this at the end of the month."

Today is Wednesday. A user asks whether the reporting service will be available at 03:00 this coming Saturday. Based on both extracts, what is the correct answer?

- A) No — the overnight maintenance window applies every day from now on.
- B) Yes — the change takes effect next Monday, so this Saturday at 03:00 the service is still on the 24/7 model.
- C) No — the catalogue is out of date, so the service should be assumed unavailable overnight.
- D) The documents contradict each other, so no answer can be given.

**Correct answer: B**

**Explanation:** Sequence the information carefully — twice. First, recency and authority: the service owner's notice is newer and explicitly supersedes the catalogue, even flagging that the catalogue will lag until month end. So the notice governs. Second — the step this question really tests — read the notice's effective date: the new model starts "from next Monday". Today is Wednesday; this coming Saturday precedes next Monday; therefore the old 24/7 model still applies on Saturday at 03:00, and the service will be available. Option B is correct. Option A applies the new rule before its commencement date; option C treats "the catalogue will become outdated" as "everything in it is already void"; option D declares a contradiction where there is only an orderly transition with a stated switchover. Real operational reading constantly involves documents in mid-transition — policies with commencement dates, catalogues awaiting update — and the skill is holding both the supersession and the effective date in view at once. Getting this wrong in real life means giving users wrong availability information, a direct user-focus failure.

**Question 12 (hard) — Inference about user needs from research notes**

Read this extract from user research notes shared with your team:

"We interviewed 14 caseworkers about the case system's overnight batch window (currently 23:00–01:00). Twelve reported no impact. Two — both in the international team — reported regular disruption: they work UK evening hours to overlap with partners in Asia-Pacific time zones, and the batch window falls in the middle of their working peak. The international team is expected to triple in size next year. Caseworkers also asked, unprompted, for advance notice when the batch overruns, as overruns currently surface only when the system 'goes quiet'."

Which conclusion is best supported by the notes?

- A) The batch window suits almost everyone, so no action is needed.
- B) The window disrupts a small but growing user group whose working pattern differs from the majority, and users need proactive communication about overruns — two distinct needs the current arrangement does not meet.
- C) The batch window must be moved immediately to daytime.
- D) The two international caseworkers should change their working hours.

**Correct answer: B**

**Explanation:** The notes contain two separable findings. First, a minority-impact finding with a trend attached: 2 of 14 users are disrupted, but they are disrupted regularly, the cause is structural (time-zone overlap work, not preference), and their team "is expected to triple" — so today's marginal issue is on a path to becoming a significant one. Second, an unprompted communication need: users want notice of overruns rather than discovering them by silence — a need independent of when the window sits. Option B captures both findings at accurate strength. Option A reads the 12/14 majority and stops, discarding both the trend and the unprompted request — a classic misuse of averages over segments. Option C converts evidence into a specific remedy the notes do not evaluate (a daytime window might disrupt the majority far more). Option D solves the system's problem by redesigning the users — inverting user focus, and ignoring that the evening pattern exists to serve the organisation's international partners. This is your user focus skill as your role defines it: using qualitative and quantitative data about users to turn user focus into outcomes — which starts with reading research notes for every distinct need they contain.

### Preparation tips

- **Anchor the three verdicts.** True: the passage guarantees it (possibly by combining stated rules). False: the passage contradicts it. Cannot say: neither. Before answering, name which verdict you are claiming and why.
- **Circle the operators.** "Must", "may", "all", "some", "unless", "where", "at least", "from next Monday" — modal verbs, quantifiers, exceptions, and effective dates decide most questions. Read them as precisely as you would read a config file.
- **Match cases to rules by scope.** When a passage contains several rules, first determine which rule governs the case in the statement. Most hard errors are correct reasoning applied to the wrong rule.
- **Keep claim strength constant.** In summary and inference questions, eliminate options that promote hypotheses to facts ("suspected" → "confirmed") or shrink stated impacts ("30% of requests" → "completely down").
- **Practise on the documents you live with.** Take a real change policy or runbook paragraph and write one true, one false, and one cannot-say statement about it. Ten minutes of this per week builds exactly the tested muscle — and improves your documentation as a side effect.
- **Read the question before re-reading the passage.** On timed tests, skim the passage once for structure, read the statement, then return to the specific sentences that bear on it. Targeted re-reading beats repeated full reads.

### Common pitfalls to avoid

- **Importing operational knowledge.** You know how patching, logging, and suppliers behave in real life. The test scores only what the passage supports — real-world truths that the passage does not state are "cannot say".
- **Treating "unsupported" as "non-functional", or vice versa.** More generally: watch for statements that quietly substitute a related concept (stops being updated → stops working; will be updated → already void). Substitution of neighbours is the test-writer's favourite trick.
- **Missing effective dates and transitions.** A newer document supersedes an older one — but only from its commencement date. Check both which document governs and when.
- **Applying exceptions outside their scope.** The stop-everything clause for domain controllers does not cover file servers. Exceptions have conditions; verify the condition before invoking the exception.
- **Choosing the summary that "sounds professional".** Wrong summaries often sound crisper and more confident than the passage warrants — that confidence is precisely the distortion. The best summary is the faithful one, not the most decisive one.
- **Forgetting the reader in writing questions.** The best-written option is defined by its audience: executable by a stressed on-call engineer, or understandable by a non-technical user. Elegance and completeness lose to actionability.

## Workplace job-specific situational judgement assessment

### About this assessment

A situational judgement assessment presents realistic workplace scenarios and asks you to judge the effectiveness of possible responses. Question formats vary: choose the most effective response; choose the most and least effective from a set; or rate every response on a scale. The scenarios have no arithmetic and no passage-parsing — they test professional judgement: what you do when an alert fires mid-change, when a colleague pressures you to shortcut process, when your fix works but you are not sure why, or when a user's complaint contradicts your dashboard.

The typical format is an online test of 25 to 40 minutes with 12 to 20 scenarios, usually generously timed because it measures judgement rather than speed. Scoring compares your choices against the consensus of experienced practitioners and against the behaviours the organisation values: user focus, ownership, collaboration, appropriate escalation, honesty, and inclusion. There are no trick questions, but the wrong options are engineered to be attractive — decisive-sounding responses that bypass change control, or diplomatic-sounding responses that abandon ownership.

Why does this assessment matter for your role? Because at your level, judgement is the difference between an engineer who executes tasks and one who can be trusted with a production estate. You own issues until a new owner is found or the problem is resolved — which requires judging when to persist and when to hand over. You implement change requests and apply change control under supervision — which requires judging what to do when reality departs from the change plan mid-implementation. You monitor services and take "appropriate action" — and appropriateness is precisely what situational judgement measures. Employers assess this because operations is where good judgement quietly prevents incidents and poor judgement audibly causes them.

Approach these scenarios as your best professional self: the engineer who is honest about mistakes, keeps users informed, respects process while using its emergency provisions when genuinely warranted, and treats colleagues — including service desk staff and suppliers — as partners. If you hold those values in view, most scenarios resolve themselves.

### How this assessment maps to your role

- **Ownership judgement** maps to your **Ownership and topic** skill: owning an issue until a new owner is found or the problem is mitigated or resolved is a series of judgement calls about persistence, handover quality, and follow-through.
- **Process integrity under pressure** maps to your **Change management** skill (applying change control procedures when others push for shortcuts) and your **Asset and configuration management** skill (keeping records accurate even when updating them is inconvenient).
- **Escalation and alerting judgement** maps to your **Incident management** skill and your duty to monitor, alert and take appropriate action: choosing the right action, channel, and urgency for what monitoring reveals.
- **Investigation discipline** maps to your **Problem management** and **Testing** skills: contributing to remedies without guessing, preserving evidence, and being honest about what is verified versus assumed.
- **Service and user orientation** maps to your **Service focus** and **User focus** skills: remembering that behind every component KPI is a service, and behind every service are users whose needs are the point of the work.

### Practice questions

**Question 1 (easy) — Alert during a routine task**

You are mid-way through a routine, interruptible documentation task when monitoring raises a critical alert: the customer-facing booking service is returning errors for all requests. The incident process requires immediate logging and notification of the on-call lead for customer-facing outages. What is the most effective response?

- A) Finish the documentation section first so you do not lose your train of thought, then handle the alert.
- B) Pause the documentation, log the incident, notify the on-call lead per the process, and begin initial diagnostics while awaiting their response.
- C) Attempt a full solo fix first, notifying the on-call lead only if you cannot resolve it within an hour.
- D) Forward the alert email to the whole team and resume documentation.

**Correct answer: B**

**Explanation:** A total outage on a customer-facing service outranks any interruptible task, so option A fails on prioritisation — twenty minutes of documentation flow is not worth twenty minutes of users unable to book. Option B follows the process precisely and adds appropriate initiative: logging creates the record, notifying the on-call lead engages the accountable responder, and starting initial diagnostics (gathering symptoms, checking recent changes) uses the waiting time productively without exceeding your remit. Option C inverts the process: an hour of silent solo effort on a full outage delays the coordinated response the process exists to provide, and deprives the incident of the timeline record that later diagnosis needs. Option D broadcasts without acting — notification is not ownership. The behaviours assessed: prioritisation by user impact, faithful process execution, and initiative within role boundaries.

**Question 2 (easy) — A discrepancy you could ignore**

While completing an unrelated task, you notice the CMDB lists a decommissioned server as live, in a rack where you can see it no longer exists. Updating the record is not your task today, and nobody has noticed. What is the most effective response?

- A) Leave it — it is not your task, and touching other records creates risk.
- B) Correct or flag the record through your team's configuration process now (or log it as a data-quality task if immediate correction is not permitted), so the CMDB reflects reality.
- C) Mention it verbally to a colleague and move on.
- D) Delete the server record entirely to tidy the database.

**Correct answer: B**

**Explanation:** Accurate configuration information is a standing duty, not a task-scoped one — your role includes maintaining accurate information and verifying the location and state of IT assets, and you have just verified a state mismatch. Option B closes the gap through the proper route: correct it if your process permits, or raise it formally so it cannot evaporate. Stale CMDB records have real costs — engineers plan patching, capacity, and incident response against them, and a ghost server wastes someone's 2 a.m. attention during the next crisis. Option A treats data quality as someone else's job; option C almost guarantees the fix is forgotten, since verbal mentions leave no record; option D exceeds the finding — decommissioned assets usually require a status change with history preserved, not deletion, and destroying the record may breach asset-tracking requirements. The behaviours assessed: proactive ownership, respect for process, and understanding that records are shared infrastructure.

**Question 3 (easy) — A user disputes your dashboard**

A user phones: the HR system has been "unusably slow all morning" for their whole team. Your monitoring dashboard shows the HR system healthy, with normal response times. What is the most effective response?

- A) Tell the user the system is fine because the dashboard proves it, and close the call.
- B) Take the report seriously: gather specifics (who is affected, since when, from where, doing what), log the incident, and investigate the gap between the users' experience and the dashboard — the path between them may be the problem.
- C) Advise the whole team to restart their computers and call back tomorrow.
- D) Escalate straight to the network team, telling them their network is broken.

**Correct answer: B**

**Explanation:** A green dashboard and a suffering user are not contradictory — dashboards measure what they are instrumented to measure, typically the server side, while users experience the whole chain: client, network path, authentication, and load patterns your synthetic checks may miss. Option B treats the user report as data (which it is — your user focus skill explicitly includes using qualitative data about users) and investigates the discrepancy, which is often where the most instructive faults live. Option A elevates instrumentation over experience and abandons users who remain unable to work; note also that "my dashboard says you're wrong" is corrosive to the trust that makes users report faults early. Option C is a generic deflection without diagnosis. Option D escalates on a guess, exporting blame before evidence — poor collaboration and often wrong. The assessed behaviours: user focus, investigative honesty, and gathering required information before concluding.

**Question 4 (moderate) — Pressure to skip change control**

A project manager, under deadline pressure, asks you to apply a firewall rule change this afternoon: "The change board doesn't meet until Thursday and we go live Wednesday. It's a tiny change — just do it, I'll take responsibility." The change is not in any approved category you can self-serve, and your process has an expedited/emergency route requiring your team lead's approval. What is the most effective response?

- A) Apply the change — the project manager has accepted responsibility, and go-live matters.
- B) Refuse flatly and tell the project manager to plan better next time.
- C) Explain you cannot apply an unapproved change, and immediately offer the legitimate fast path: contact your team lead about the expedited route so the change can be properly approved before Wednesday.
- D) Apply the change but keep the project manager's message as evidence it was their decision.

**Correct answer: C**

**Explanation:** This scenario tests whether you hold process under social pressure while staying genuinely helpful. Option C does both: it declines the improper request clearly, and it actively solves the project manager's real problem — the process itself provides an expedited route, and engaging it today comfortably beats Wednesday. This is the collaborative shape of integrity: "not that way, but here is the right way, and I will help you take it." Option A fails on a point worth internalising: a project manager cannot "take responsibility" for your bypassing of change control — accountability for applying unauthorised changes stays with the person who applies them, and unrecorded firewall changes are precisely how outages and security gaps become undiagnosable. Option D knows this — collecting evidence is preparing for the consequences of a decision you know is wrong. Option B protects process but fails collaboration; the rebuke helps no one and the go-live problem remains. The behaviours assessed: integrity under pressure, constructive collaboration, and knowing your process well enough to offer its legitimate exceptions.

**Question 5 (moderate) — Mid-change deviation**

You are implementing an approved change to upgrade a monitoring agent across twenty servers, following the change plan. On server twelve, the installer fails with an error the plan does not mention, though the server appears to keep functioning normally. The plan has no explicit instruction for this situation. What is the most effective response?

- A) Continue with the remaining eight servers and investigate server twelve later.
- B) Pause the rollout, record the error exactly, verify server twelve's monitoring is still working, and check with the change owner (or your supervisor) whether to proceed, fix, or invoke the rollback plan.
- C) Improvise a manual installation on server twelve using a workaround you found online.
- D) Roll back all twelve servers immediately and abandon the change.

**Correct answer: B**

**Explanation:** An unplanned deviation during an approved change converts execution mode into judgement mode, and the effective judgement is to stop and consult, not to improvise or barrel on. Option B contains the four correct elements: pause (bounding the deviation at one server), record (the exact error is evidence the fix and the change review will need), verify impact (an unmonitored production server is a real risk — check whether the old agent still functions), and consult the accountable person before proceeding. This is "applying change control procedures under supervision" behaving exactly as designed — supervision exists for precisely this moment. Option A gambles that an ununderstood failure is isolated; if the installer is corrupting something subtle, you are about to have nine mysteries instead of one. Option C introduces an unauthorised, untested variation inside an approved change — the workaround may "work" while leaving server twelve permanently different from its nineteen siblings, a configuration drift that surfaces months later. Option D overreacts: a working estate with one anomaly does not warrant destroying eleven successful installations before anyone has looked at the error. The assessed behaviours: composure, evidence preservation, proportionality, and using supervision properly.

**Question 6 (moderate) — Your fix works but you do not know why**

An application service was failing intermittently. You restarted one of its components on a hunch, and the failures stopped. The incident can now be closed, users are happy, and it is nearly end of shift. What is the most effective response?

- A) Close the incident as resolved with the note "restarted component, issue resolved".
- B) Close the incident but record what you observed, what you did, and that the root cause is unknown — and raise or link a problem record so the underlying cause is investigated before it recurs.
- C) Keep the incident open indefinitely until root cause is found, regardless of user impact being over.
- D) Say nothing about the restart, in case it was the wrong thing to do.

**Correct answer: B**

**Explanation:** This scenario separates incident management from problem management — a distinction at the heart of your service management framework knowledge. The incident (user impact) is genuinely resolved; restoring service was the right goal, and closing the incident is correct. But a fix that works for unknown reasons is a debt: the intermittent fault will likely return, and the next engineer will start from zero unless your observations survive. Option B pays the debt properly: honest closure notes ("root cause unknown" is a professional statement, not an admission of failure), plus a problem record so investigation happens on its own track. That is your problem management skill — contributing to remedies and preventative measures — operating exactly as designed. Option A closes the loop with a note that quietly implies understanding you do not have, burying the recurrence risk. Option C misuses the incident record: incidents track user impact, which has ended; keeping it open blurs the queue's meaning and helps nobody. Option D is concealment — the restart was a reasonable action, and hiding actions from the record corrupts the timeline any future investigation depends on. Behaviours assessed: honesty about uncertainty, framework fluency, and ownership that extends past the visible symptom.

**Question 7 (moderate) — Handover of an owned issue**

You have spent two days investigating a recurring storage fault and built up detailed notes. Your rota moves you to a different duty tomorrow, and the fault is not yet resolved. A colleague will take over. What is the most effective response?

- A) Tell your colleague "it's all in the ticket" and move on — they can read your notes.
- B) Update the ticket fully, then give your colleague a structured handover: what is confirmed, what is suspected, what has been ruled out, what the next planned step is — and remain available for questions until they confirm they have what they need.
- C) Take the fault with you unofficially and keep working on it alongside your new duties.
- D) Suggest the investigation restart from scratch so your colleague forms their own view.

**Correct answer: B**

**Explanation:** Your ownership skill is explicit: own an issue until a new owner has been found — and "found" means genuinely equipped, not merely named. Option B transfers the investigation's real asset, which is not just the notes but the structure of the reasoning: confirmed facts versus hypotheses versus eliminated causes, plus the intended next step. That structure is exactly what two days of work bought, and it is what a written ticket alone often fails to convey — hence the conversation and the availability for follow-up questions. Option A performs a handover without ensuring one has happened; tickets written for yourself routinely lack context a newcomer needs. Option C means the issue has two half-owners and no accountable one — and your new duties suffer too. Option D discards two days of evidence for a ritual of independence; fresh eyes are valuable when an investigation is stuck, but this one has momentum and a planned next step. The behaviours assessed: complete ownership through transition, knowledge transfer as an active duty, and respect for both your colleague's time and the organisation's investment in your investigation.

**Question 8 (moderate) — A colleague's unsafe habit**

You notice an experienced colleague routinely makes small production configuration tweaks without change records — "twenty-second jobs, not worth the paperwork". This week, one such tweak coincided with a brief outage on another team's service, and nobody connected the two because nothing was recorded. What is the most effective response?

- A) Say nothing — the colleague is senior to you, and the habit is common.
- B) Speak with the colleague directly and without accusation: point out that this week's outage could not be traced because the tweak was unrecorded, suggest using the standard-change route for small jobs, and raise it with your team lead if the practice continues.
- C) Report the colleague to senior management immediately, citing this week's outage.
- D) Start keeping your own private log of the colleague's tweaks so you can prove the connection next time.

**Correct answer: B**

**Explanation:** The scenario has moved past the hypothetical: unrecorded change activity has already produced an untraceable outage. Doing nothing (option A) is no longer neutral — it accepts a demonstrated ongoing risk to service, and "senior and common" describes exactly the habits that only peer-level candour ever corrects. Option B is proportionate and constructive: the direct conversation is specific (this week's outage, not a character judgement), offers the legitimate lightweight path (most change frameworks provide standard changes precisely so twenty-second jobs are not burdened with full paperwork — a fluent use of your service management framework knowledge), and sets an escalation boundary if the risk persists. Option C leaps past the collegial step to the most severe channel on a first conversation-worthy issue — proportionality matters, and would-be reporters who skip the direct word usually inherit a poisoned team dynamic. Option D is surveillance in place of candour: it plans for the next failure instead of preventing it, and a private log helps no one diagnose anything in real time. The behaviours assessed: courage, proportionate escalation, process fluency (knowing the standard-change route exists), and treating a colleague as a partner to influence rather than a case to build.

**Question 9 (hard) — Competing demands on a degraded service**

At 14:00 a disk array degrades: the finance service it backs is running but slow, and the array's remaining redundancy means a second disk failure would cause data loss. The documented fix is a disk replacement plus rebuild, requiring the service to run even slower for about three hours. Finance's quarter-end deadline is 17:00 today, and the finance manager begs you to delay the rebuild until tomorrow. Your team lead is in a meeting, reachable by message. What is the most effective response?

- A) Delay the rebuild until tomorrow — the finance deadline is real, and the array will probably hold.
- B) Start the rebuild immediately — data integrity always beats deadlines; the finance manager will have to cope.
- C) Message your team lead now with a crisp summary — degraded array, data-loss exposure until rebuilt, rebuild slows finance through their 17:00 quarter-end — and your recommendation, so the risk trade-off is decided at the right level quickly; meanwhile prepare the replacement so no time is lost.
- D) Ask the finance manager to email you accepting the risk, then delay until tomorrow.

**Correct answer: C**

**Explanation:** This is a genuine risk trade-off, and the mark of good judgement is recognising that it is not yours to settle alone — but that engaging the decision-maker fast and well is yours. The exposure is asymmetric and hard to price: delaying risks unrecoverable data loss for the very finance data the deadline concerns (a second failure during quarter-end processing would be the worst of all outcomes), while proceeding risks a missed statutory or management deadline with costs you cannot fully see. Option C does everything within your remit at once: it escalates immediately with a decision-ready summary (facts, exposure, options, recommendation — the format that gets fast answers from busy leads), and it uses the waiting minutes to prepare, preserving both options. Option A and option B each amputate the trade-off — A gambles data on "probably", B disregards a legitimate business need without letting anyone weigh it; either might be the eventual decision, but taken solo at 14:00 they are both overreach. Option D is the subtle trap: the finance manager cannot own infrastructure risk — they are neither accountable for the data platform nor equipped to price a rebuild-window failure, and an email "accepting risk" from the wrong owner is governance theatre. The behaviours assessed: escalation quality (not just escalation), risk articulation, preparation under uncertainty, and knowing which decisions belong at which level.

**Question 10 (hard) — Most and least effective**

During patching, you notice the patch you are about to apply to a production application server was reported this morning (in a supplier bulletin your team circulated) as causing service crashes on a configuration matching yours. The change is approved and scheduled for tonight; the vulnerability it fixes is rated serious. Rank the responses: which is MOST effective and which is LEAST effective?

1. Proceed as approved — the change went through CAB, and the schedule is the schedule.
2. Halt the patch for this server, take the bulletin to the change owner today, and ask for a decision: defer, apply with enhanced rollback readiness, or await a fixed patch version — documenting whichever is chosen.
3. Quietly skip that server, mark the change complete, and wait for a corrected patch.
4. Apply the patch to a matching test server first, if one exists, and share the result with the change owner before the production window.

- A) Most effective: 2; least effective: 3
- B) Most effective: 4; least effective: 1
- C) Most effective: 2; least effective: 1
- D) Most effective: 4; least effective: 3

**Correct answer: A**

**Explanation:** Work the four responses against the behaviours. Response 2 is the strongest: new material information (a credible crash report matching your configuration) invalidates the risk assessment the approval rested on, and the correct move is to surface it to the change owner today with the realistic options framed — that is ownership, evidence-based challenge, and proper use of change governance. Response 4 is genuinely good — testing on a matching server generates local evidence — but it is second-best here because it acts on the risk unilaterally before engaging the accountable owner, and "if one exists" leaves it contingent; ideally testing happens as part of the owner's decision, which response 2's conversation would likely produce. Response 1 is poor: approval is not a suicide pact — CAB approved a risk picture that has since changed, and proceeding into a known crash condition because "the schedule is the schedule" abandons professional judgement. But response 3 is the worst: it combines the unmanaged vulnerability (server unpatched), a falsified record ("complete" when it is not), and concealment — the security team now believes a serious vulnerability is closed on a server where it is open. Falsification of change records is the one response that damages every future decision made from those records. So: most effective 2, least effective 3 — option A. The ranking principle: surfacing new risk through the accountable owner beats solo mitigation, which beats blind compliance, which beats deceptive non-compliance — honesty of the record is the floor beneath everything.

**Question 11 (hard) — An inclusion moment under pressure**

During a tense major incident bridge call, a service desk analyst — new, and audibly nervous — offers an observation: several affected users mentioned a VPN prompt just before the failures. A senior engineer talks over them: "Desk folks, please keep the line clear for engineering." The observation matches something you noticed in the logs but had not yet connected. What is the most effective response?

- A) Stay silent — challenging a senior engineer mid-incident undermines command.
- B) Say briefly: "Actually, the desk's VPN observation matches authentication errors I'm seeing in the logs — worth checking," crediting the analyst and putting the lead onto the connection.
- C) Message the analyst privately afterwards to say their input was good, but say nothing on the call.
- D) Wait until the post-incident review to raise both the VPN lead and the senior engineer's behaviour.

**Correct answer: B**

**Explanation:** Two things are at stake simultaneously: a live diagnostic lead and the collaborative climate that produces such leads. Option B serves both in one move, and does so proportionately for the moment — it is brief (respecting the bridge's discipline), substantive (log evidence, not etiquette), and it explicitly credits the analyst, which repairs the dismissal in front of the same audience that heard it and signals that frontline observations are wanted. This is your user focus skill in its operational form — service desk analysts carry user-experience evidence engineers cannot see — and incident effectiveness depends on that channel staying open; a nervous new analyst who is talked over and undefended learns to stay silent, and the next incident is diagnosed with less information. Option A confuses hierarchy with incident command: command benefits from evidence, and B challenges nobody — it adds data. Option C consoles the person but abandons both the live lead (the VPN connection waits while the incident runs) and the public correction; private kindness does not repair public dismissal. Option D delays a diagnostic lead for hours in service of a process moment — the review is the right place for the behavioural pattern if it recurs, but the lead is needed now. The behaviours assessed: inclusion as an operational capability, courage with proportion, evidence over status, and keeping user-side information flowing into technical response.

**Question 12 (hard) — End of shift, untested assumption**

It is 17:40; your shift ends at 18:00. You have just finished implementing a change to log rotation on four production servers. The change plan's verification step says "confirm logs rotate correctly at the next scheduled rotation" — which happens at 02:00 tonight. The overnight shift is short-staffed, and nothing in the plan assigns the 02:00 verification to anyone. What is the most effective response?

- A) Leave at 18:00 — the implementation went cleanly, and rotation will almost certainly work.
- B) Before leaving: hand the verification explicitly to the overnight shift with exact instructions (what to check at 02:00, what "correct" looks like, what to do and who to contact if it fails), record this in the change ticket, and if the overnight shift cannot take it, agree an alternative with your lead — do not let the step silently own no one.
- C) Stay until 02:00 yourself to do the verification.
- D) Set a personal reminder to check the logs when you start tomorrow at 09:00.

**Correct answer: B**

**Explanation:** The scenario's trap is the orphaned step: a verification that everyone assumes will happen and no one owns — the exact gap through which clean-looking changes become morning incidents. Option B closes it with a genuine handover: explicit assignment, executable instructions (what to check, what good looks like, failure action, contact), a record in the change ticket so accountability is visible, and an escalation path if the overnight shift genuinely cannot absorb it. That is your ownership skill applied to a task rather than an incident — owning it until a new owner has truly been found. It is also your documentation duty in miniature: instructions that a short-staffed overnight shift can execute without you. Option A converts "almost certainly" into nobody checking; if rotation fails, four production servers fill their disks by morning — a foreseeable, preventable outage. Option C over-serves the step at unsustainable personal cost, and a tired engineer at 02:00 is itself a risk; occasional genuine emergencies may warrant staying, but an assignable verification does not. Option D leaves a seven-hour window in which failed rotation runs unobserved — 09:00 may be too late, and a personal reminder is invisible to the organisation if you are ill tomorrow. The behaviours assessed: foresight, complete ownership through handover, realistic self-management, and making accountability visible in shared records.

### Preparation tips

- **Know your processes before the test — and use the test to know them better.** The strongest answers repeatedly involve the legitimate fast paths and exception routes real frameworks provide: expedited changes, standard changes, problem records, handover protocols. Fluency in your organisation's versions of these is both assessment preparation and professional development.
- **Judge options against the behaviour set.** For each response ask: is it honest (including honest records)? Does it serve users? Does it keep the right people informed? Is it proportionate? Does ownership land somewhere visible? Most-effective options score well across all five; least-effective options usually fail honesty or ownership.
- **Watch for the orphaned responsibility.** Many scenarios hide a task, risk, or verification that no option explicitly owns. The best response is usually the one that makes ownership explicit and recorded.
- **Distinguish escalating a decision from abandoning it.** Senior-level trade-offs (risk versus deadline) belong with accountable owners — but the strong option escalates with a decision-ready summary and keeps preparing meanwhile. "Told my lead" is not the whole answer; "equipped my lead to decide fast, and stayed useful" is.
- **Rehearse with colleagues.** Talk through scenarios like these with your team lead or an experienced peer — "what would you have wanted me to do?" calibrates your judgement against your actual organisation, which is what the real assessments approximate.
- **Answer as your considered self, consistently.** Rating-scale formats detect inconsistency. Anchor the clearly strong and clearly weak responses first, then place the middle ones relative to those anchors.

### Common pitfalls to avoid

- **The hero reflex.** Solo fixes, solo risk decisions, and staying until 02:00 all feel committed and score poorly. Effective operations is coordinated: the strong options engage processes and people at the right moments.
- **The compliance reflex.** The mirror-image trap: "it was approved / scheduled / ordered" does not justify proceeding into newly known danger. Approvals encode a risk picture; when the picture changes, strong options resurface the decision.
- **Any falsified or silent record.** Marking incomplete work complete, closing incidents with implied understanding, tweaking production without records, keeping private logs — every scenario containing a record offers a response that corrupts it. That response is reliably among the worst on offer.
- **Dismissing user-side evidence.** Green dashboards, senior voices, and engineering confidence all tempt you to discount what users and service desk colleagues report. User experience is data; options that honour it score well.
- **Disproportionate escalation — in both directions.** Under-escalation (handling risk trade-offs solo) and over-escalation (senior management for a first conversation-worthy issue) both fail. The strong options match the channel to the stakes and try the direct, collegial step first when stakes allow.
- **Ownership that ends at the visible symptom.** Users happy, incident closed, shift over — and the root cause, the verification step, or the handover quietly unowned. Assessments repeatedly reward the response that carries ownership through to the unglamorous last step.

## Conclusion

Congratulations on working through a complete set of psychometric assessment practice materials built around your role as an infrastructure operations engineer. Take a moment to recognise what that represents — not just test preparation, but a structured tour of the thinking your profession runs on.

You have practised cognitive reasoning with the artefacts of your daily work: monitoring trends, dependency chains, configuration records, change timelines, and maintenance-window scheduling. You have worked numeric questions on the quantities your KPIs are made of — availability percentages and their downtime budgets, capacity thresholds and time-to-exhaustion, weighted resolution times, failure rates versus failure counts — with every calculation laid out step by step. You have sharpened verbal precision on change policies, supplier notices, runbooks, and user research notes, applying the true/false/cannot-say discipline that keeps investigation notes factual and handovers trustworthy. And you have exercised situational judgement across the dilemmas that define operational professionalism: process integrity under pressure, mid-change deviations, honest closure of half-understood fixes, risk trade-offs escalated well, and ownership carried through to the last unglamorous verification step.

Notice how consistently the same principles resolved questions across all four sections. Anchor to the last known good state and reason forwards. Verify field by field rather than by general impression. Hold conclusions at exactly the strength the evidence supports. Match cases to the rules that actually govern them. Keep records honest, keep users informed, and make sure every risk and task has a visible owner. These are not test tricks — they are the operating principles of reliable infrastructure work, which is precisely why job-specific assessments measure them.

That alignment is worth taking seriously as a development opportunity. Every technique this guide rehearses has a daily-work twin: timeline reasoning is incident diagnosis; weighted averages are honest service reporting; scope-tracking is compliance judgement; escalation quality is what your team lead experiences when you bring them a decision. Practising for assessments and getting better at your job are, for once, the same activity. Use that. Revisit these questions in a few weeks and notice how much faster the methods come. Time yourself on the second pass. Take the situational scenarios to a team discussion — the conversations they provoke are worth more than the answers.

If a real assessment is ahead of you, go in confident: you now know the formats, the question archetypes, the standard traps, and — more importantly — the reasoning habits that dissolve them. Read precisely, calculate with the right baseline, conclude only what the evidence guarantees, and answer as the engineer you are at your best.

The infrastructure you support underpins public services that people depend on every day. The care you bring to a trend line, a change record, or a handover note is part of what keeps those services running. Keep building that care into habit — your assessments, your team, and the public you ultimately serve all benefit from it.

Good luck, and keep up the excellent work.
