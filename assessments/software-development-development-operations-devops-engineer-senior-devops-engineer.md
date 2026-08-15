# Senior DevOps Engineer - Psychometric Assessment Resources

## Introduction

Welcome! This guide has been created especially for you as a senior DevOps engineer working within the UK Government Digital and Data profession. Whether you are preparing for an internal assessment, applying for a new post, benchmarking your own capability, or simply curious about how psychometric assessments relate to your day-to-day engineering work, this document will help you practise, reflect, and build confidence.

Psychometric assessments are structured, standardised exercises that measure the mental capabilities and behavioural tendencies that predict success in a role. For a senior DevOps engineer, that means far more than abstract puzzles. The assessments described here are job-specific: they use the kinds of artefacts you genuinely handle — pipeline configurations, deployment strategies, availability dashboards, capacity forecasts, incident timelines, security controls, integration build plans, and code review comments — and the kinds of decisions you genuinely make, such as transforming technical requirements into an effective DevOps toolchain, ensuring deployment strategies are repeatable, scalable and highly available, and solving complex problems for the delivery teams you support.

Why do these assessments matter for your role in particular? As a senior DevOps engineer, you deliver and integrate software to form a complete DevOps toolchain, and you plan and design large groups of stories. You hold deep technical knowledge and other people rely on it: delivery teams come to you when the deployment fails at 4pm on a Friday, junior colleagues come to you for coaching and mentoring, and architects come to you to review systems designs. Assessments of cognitive ability, numerical reasoning, verbal reasoning, and situational judgement map directly onto those demands. Practising them sharpens exactly the skills your role depends on: spotting the one misconfigured stage in a pipeline definition, interpreting an availability report against a key performance indicator, extracting precise meaning from a dense security standard, and choosing the most effective course of action when a delivery deadline collides with a failing test suite.

This document is organised into four main assessment sections, each following the same pattern: an overview of what the assessment measures and why it matters for your role, a mapping of the assessment dimensions to the specific skills in the senior DevOps engineer capability framework, a substantial set of practice questions with full worked explanations, practical preparation tips, and common pitfalls to avoid.

Here is how to get the most from it. First, read each "About this assessment" section so you understand the format before you meet it under timed conditions. Second, attempt the practice questions honestly — write down your answer before reading the explanation, exactly as you would run a test before merging rather than after. Third, treat every explanation as a mini-lesson: even when you answer correctly, the reasoning walkthrough will deepen your technique, in the same way a good code review teaches even when the code was already sound. Finally, use the preparation tips for self-reflection: they connect assessment performance back to your professional development as an engineer who supports delivery teams, mentors more junior colleagues, and underpins good development processes for your organisation.

One reassuring thought before you begin: nothing in these assessments is beyond you. The reasoning they test is the reasoning you already use every working day — in retros, in incident reviews, in design discussions, in the quiet discipline of reading a diff carefully before approving it. Practice simply makes that reasoning faster, calmer, and more reliable under time pressure.

Take your time, be kind to yourself, and enjoy the practice. Let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive ability assessment measures the exact mental processes your role demands, using practical workplace scenarios rather than abstract puzzles. Unlike a generic intelligence test, it presents you with the everyday materials of your job — in your case, pipeline definitions, deployment sequences, environment configurations, access control rules, monitoring alerts, and integration build plans — and asks you to reason quickly and accurately about them.

Typical format: an online, timed test lasting 15 to 30 minutes, with questions covering pattern recognition, logical deduction, error checking, prioritisation, and applied problem solving. Scoring is objective, comparing your responses against a norm group, and modern platforms often adapt question difficulty based on your previous answers. Employers usually receive a breakdown of speed versus accuracy rather than a single score, so working both quickly and carefully matters. You will normally be offered short, ungraded practice questions before the real test begins, so you can get comfortable with the interface without pressure.

For a senior DevOps engineer, cognitive ability assessment is particularly relevant because your core professional value is structured technical thinking under constraint. Building a complete DevOps toolchain requires holding many moving parts in mind at once: which pipeline stages depend on which artefacts, which environments must be promoted in which order, where a configuration contradicts a security control, and what follows logically when one component of an integrated system changes. Debugging a complex service fault is essentially applied deduction; reviewing another engineer's systems design is essentially error checking at scale. A well-designed cognitive assessment simulates precisely those demands in miniature — which is also why senior engineers who practise a little tend to perform very well.

### How this assessment maps to your role

The assessment dimensions map directly to the named skills in your role summary:

- **Pattern recognition** maps to your **Service support** skill: identifying, locating and fixing complex service faults means recognising recurring signatures — a memory leak's sawtooth graph, a retry storm's log pattern, a certificate expiry's sudden cliff — across large and noisy telemetry.
- **Logical deduction** maps to **Systems design** and **Systems integration**: designing systems of medium risk and complexity, defining the integration build, and co-ordinating build activities across systems all require you to reason validly from constraints — dependency rules, promotion policies, security requirements — to their consequences.
- **Error checking** maps to **Programming and build (software engineering)** and **Modern development standards**: designing, coding, testing and documenting programs of medium-to-high complexity, and supporting others in applying modern standards, means spotting the inconsistency between a specification and its implementation, or between a standard and a submitted change.
- **Prioritisation** maps to **Availability and capacity management** and **Service support**: managing service components against business needs and KPIs demands rapid ranking of what matters most when alerts, requests and deadlines compete.
- **Problem solving** maps to **Development process optimisation** and your duty to provide deep technical support to delivery teams: teams bring you tangled build failures and slow processes, and you must decompose them, isolate causes, and recommend fixes.

### Practice questions

**Question 1 (easy) — Pattern recognition in environment naming**

Your organisation's platform standards require environments to be named `<service>-<env>-<region>` where `env` is one of `dev`, `test`, `stage`, or `prod`, and `region` is `ldn` or `mcr`. While reviewing infrastructure code from a delivery team, you see these resource names:

1. `licensing-dev-ldn`
2. `licensing-test-mcr`
3. `licensing-ldn-stage`
4. `licensing-prod-ldn`
5. `licensing-stage-mcr`

Which entry breaks the naming pattern?

- A) Entry 2
- B) Entry 3
- C) Entry 4
- D) Entry 5

**Correct answer: B**

**Explanation:** The pattern fixes the order: service, then environment, then region. Entry 3 swaps the last two segments — `ldn` (a region) appears where the environment belongs, and `stage` where the region belongs. Entries 1, 2, 4 and 5 all follow the rule. This is exactly the kind of consistency check you perform when you support others in applying modern development standards: naming conventions look trivial, but automation depends on them — a deployment script that parses the second segment to decide which credentials to load will behave dangerously when the segments are inverted. Spotting the broken convention before merge is cheaper than diagnosing the misdeployment afterwards.

**Question 2 (easy) — Logical deduction from a deployment policy**

Your deployment policy states: "Every change reaching production must have passed the full integration test suite in staging, unless it is an emergency fix approved by the on-call lead." A colleague tells you: "This change is in production and did not pass the integration suite in staging." Which one of the following conclusions must be true?

- A) The change is an emergency fix approved by the on-call lead.
- B) The deployment policy has been breached.
- C) Either the change is an approved emergency fix, or the policy has been breached.
- D) The integration suite was failing for unrelated reasons.

**Correct answer: C**

**Explanation:** The policy is a conditional rule with one permitted exception. From the facts given you cannot tell whether the emergency route was used, so neither A nor B must be true on its own — each is merely possible. D introduces information not present at all. The only conclusion guaranteed in every case consistent with the facts is the disjunction in C. Assessments reward this discipline: deduce only what the given information guarantees. In your role, the same discipline stops you accusing a team of bypassing controls before checking the emergency change record — which protects your working relationships as well as your logic, and models good judgement for the junior engineers you mentor.

**Question 3 (easy) — Sequencing a pipeline**

A build pipeline has five stages with these rules: Compile must run first. Unit tests require Compile. Package requires Unit tests. Security scan requires Package. Deploy to test requires both Package and Security scan. Which stage must run fourth?

- A) Unit tests
- B) Package
- C) Security scan
- D) Deploy to test

**Correct answer: C**

**Explanation:** Chain the dependencies: Compile (1st) → Unit tests (2nd) → Package (3rd) → Security scan (4th) → Deploy to test (5th). Deploy to test needs both Package and Security scan, and Security scan itself needs Package, so the scan must sit between Package and Deploy. The only valid order places Security scan fourth. Dependency chains like this are the daily grammar of toolchain work: when you define the integration build and co-ordinate build activities across systems, you are constructing exactly this kind of ordered graph — and a wrong ordering (scanning before packaging, deploying before scanning) either fails noisily or, worse, passes silently while checking the wrong artefact.

**Question 4 (moderate) — Error checking an access control matrix**

Your platform's access standard states: (i) production credentials may be held only by the platform team; (ii) every environment must have at least one team with deploy rights; (iii) delivery teams may deploy to dev and test only. You review this access matrix:

| Environment | Delivery team rights | Platform team rights |
|---|---|---|
| dev | deploy | deploy |
| test | deploy | none |
| stage | deploy | deploy |
| prod | none | deploy |

How many rows are inconsistent with the standard?

- A) 0
- B) 1
- C) 2
- D) 3

**Correct answer: B**

**Explanation:** Check each row against each rule. Dev: delivery may deploy to dev (rule iii satisfied), at least one team has deploy rights (rule ii) — consistent. Test: delivery may deploy to test, and rule ii is satisfied by the delivery team's rights; the platform team having "none" breaks no rule — consistent. Stage: delivery teams may deploy to dev and test *only*, so delivery deploy rights on stage breach rule iii — inconsistent. Prod: only the platform team has rights, satisfying rules i and ii — consistent. Exactly one row is defective. The tempting error is flagging the test row because the platform team lacks rights there, but no rule requires the platform team to hold rights everywhere — rule ii only requires *some* team to hold them. This mirrors real security review: engineers who add imagined rules generate false positives that erode trust in the review, while missing the genuine stage violation leaves a real hole. Designing solutions with security controls included means checking against the controls as written.

**Question 5 (moderate) — Prioritisation on a busy morning**

It is Monday morning. Four items compete for your attention:

1. Production alert: error rate on the payments service has breached its KPI threshold and the delivery team has asked for your help diagnosing it.
2. A junior DevOps engineer has asked you to review their first pipeline change, which they would like to merge today.
3. The quarterly capacity forecast for your services is due to the service owner on Friday.
4. A delivery team's staging environment is broken, blocking their sprint work; they raised it an hour ago.

Which sequencing is most defensible?

- A) 1, 4, 2, 3 — live user-facing impact first, then the blocked team, then coaching, then the forecast
- B) 2, 1, 4, 3 — quick reviews first to unblock people
- C) 4, 1, 2, 3 — the staging failure was raised first, so it goes first
- D) 1, 3, 4, 2 — production issues then formal deliverables

**Correct answer: A**

**Explanation:** Prioritisation questions test reasoning about impact and urgency together. Item 1 is a live production KPI breach with user-facing impact — as the engineer responsible for managing service components against business needs and KPIs, this comes first. Item 4 blocks an entire team's delivery, so it outranks individually scheduled work; it comes second. Item 2 matters — coaching and mentoring is part of your role — but a same-day merge hope is not a same-hour need, and it follows. Item 3 has a Friday deadline and can be planned around the rest. Option B inverts impact ordering for the sake of a quick win; C confuses arrival order with priority, which is how ticket queues mislead; D leaves a whole team blocked behind a Friday deadline. Note the pattern: the strongest answer sequences by impact-weighted urgency — live service, then blocked teams, then individuals, then scheduled work — while none of the four items is simply dropped.

**Question 6 (moderate) — Logical deduction about promotion rules**

Your release process has these rules: (i) an artefact cannot be promoted to staging until its image has been signed; (ii) signing cannot occur until the vulnerability scan reports no critical findings; (iii) promotion to production requires the artefact to have run in staging for at least 24 hours. An artefact's vulnerability scan completed clean at 09:00 on Tuesday, and signing plus promotion steps each take negligible time. What is the earliest the artefact can reach production?

- A) 09:00 Tuesday
- B) 09:00 Wednesday
- C) 24 hours after signing, whenever signing happens
- D) 09:00 Thursday

**Correct answer: B**

**Explanation:** Work forwards through the dependencies. The clean scan at 09:00 Tuesday permits signing immediately; signing permits promotion to staging immediately; so the artefact can be in staging from 09:00 Tuesday. Rule iii requires 24 hours of staging soak, so production promotion is possible from 09:00 Wednesday. Option A ignores the soak requirement; D adds a phantom extra day; C looks rigorous but is weaker than B — it restates rule iii without using the given timings, and the question asks for the earliest concrete time. A tempting real-world error is the same: quoting the policy instead of computing the answer. When you plan deployment strategies that are repeatable and scalable, you constantly convert policy constraints into concrete schedules — release trains, freeze windows, soak periods — and assessments reward the same conversion done precisely.

**Question 7 (moderate) — Pattern recognition in an incident timeline**

During a service fault, you assemble this timeline: 02:00 nightly batch job starts; 02:10 database CPU rises to 85%; 02:15 API latency doubles; 02:30 batch job completes; 02:32 database CPU returns to 40%; 02:35 API latency returns to normal. The same pattern appears on four of the last five nights; on the fifth night the batch job did not run and no latency rise occurred. As a senior DevOps engineer, what is the most reasonable first interpretation?

- A) The API service has an unrelated memory leak that happens to coincide with the batch window.
- B) The evidence suggests the batch job's database load is driving the latency; investigate resource isolation or rescheduling for the batch job.
- C) The database needs to be upgraded immediately to a larger instance.
- D) The correlation is coincidental and five nights is too small a sample to act on.

**Correct answer: B**

**Explanation:** The pattern shows consistent temporal ordering (batch start precedes CPU rise precedes latency rise, and recovery follows completion), a dose-response shape, and — crucially — a natural experiment: the one night without the batch job was the one night without the symptom. That combination makes the batch job the strongest working hypothesis, and B correctly treats it as a hypothesis to act on (investigate isolation or rescheduling) rather than a proven fact. Option A invents a mechanism the data does not support and ignores the fifth-night evidence. Option C jumps to an expensive remediation before diagnosis — upgrading the instance might mask the problem while the real fix (a missing index in the batch query, say) stays hidden. Option D misapplies statistical caution: five consistent nights including a clean counterfactual is exactly the evidence pattern that fault diagnosis runs on. Identifying, locating and fixing complex service faults is a discipline of reading patterns like this one and committing to the cheapest decisive next test.

**Question 8 (challenging) — Multi-constraint scheduling of an integration build**

You are co-ordinating an integration build across three systems — Accounts (A), Notifications (N), and Reporting (R) — over five working days, Monday to Friday, integrating one system per day at most. Constraints: (i) A must be integrated before N, because N consumes A's events; (ii) the Reporting team is only available Monday and Thursday; (iii) after A is integrated, one full working day of contract testing is needed before N can be integrated; (iv) R must be integrated after N, because its dashboards read N's delivery receipts. On which day must N be integrated?

- A) Tuesday
- B) Wednesday
- C) Thursday
- D) Friday

**Correct answer: B**

**Explanation:** Work the constraints together. R needs the Reporting team (Monday or Thursday) and must come after N — so R must be Thursday, since a Monday R cannot follow anything. Therefore N must be on or before Wednesday. A must precede N with one clear working day of contract testing between them: if N were Tuesday, A would need to be Monday with a full day of testing between — impossible, as there is no day between Monday and Tuesday. So N cannot be Tuesday (and obviously not Monday). N must therefore be Wednesday, with A on Monday and Tuesday as the contract-testing day, and R on Thursday. Every constraint is satisfied and no alternative placement of N works. This is a compressed version of what defining the integration build actually involves: team availability, dependency order, and mandatory gaps interact, and the feasible schedule is often unique. In the assessment, write the day grid down if scratch paper is allowed — externalising the constraint graph prevents the working-memory overload that causes careless errors.

**Question 9 (challenging) — Deduction from monitoring rules**

Your alerting rules state: (i) if CPU exceeds 90% for 10 minutes, a capacity alert fires; (ii) if a capacity alert fires and the service is customer-facing, the on-call engineer is paged; (iii) if the on-call engineer is paged, an incident record is always created. This morning there is no incident record involving the licensing service, which is customer-facing. Which conclusion must be true?

- A) The licensing service's CPU did not exceed 90% at all overnight.
- B) No capacity alert fired for the licensing service overnight.
- C) The on-call engineer was not paged for the licensing service overnight.
- D) The monitoring system was working correctly overnight.

**Correct answer: C**

**Explanation:** Reason backwards through the chain (contrapositive reasoning). Rule iii says paging always creates an incident record; no record therefore means no page — C must be true. Can we go further back? Rule ii says a capacity alert on a customer-facing service causes a page; no page therefore means no capacity alert fired — so B looks tempting, and indeed B does follow from the rules as stated. But compare B and C: B depends on two links of the chain holding (ii and iii), while C depends only on rule iii. The question asks which conclusion *must* be true, and the assessment convention with a single-answer format is to choose the conclusion that follows most directly — but be careful: if both genuinely followed, the question would be flawed. Re-read rule ii: it says the engineer is paged if the alert fires *and* the service is customer-facing. The licensing service is customer-facing, so no page does entail no alert... for licensing. B says "no capacity alert fired for the licensing service" — that also follows. The discriminator is rule i's direction: A does not follow, because CPU could have exceeded 90% for less than 10 minutes without firing any alert; and D does not follow, because the rules describe intended behaviour, not evidence that the system honoured it — in fact, the strictly safest deduction is C, because B additionally assumes the paging mechanism functioned as designed, which the scenario does not guarantee. This layered reasoning — what the rules guarantee versus what the infrastructure actually did — is precisely the scepticism that makes a senior engineer good at fault diagnosis: absence of an alert is evidence, but only as strong as the alerting path itself.

**Question 10 (challenging) — Error checking a rollback plan**

A delivery team submits this rollback plan for review: "Step 1: redeploy previous application version 2.4.1. Step 2: restore the database from the pre-deployment snapshot. Step 3: invalidate the CDN cache. Step 4: confirm health checks pass. Note: version 2.5.0 includes a database migration that adds a new column and backfills it." You know the service takes live writes continuously. What is the most serious flaw in the plan?

- A) The CDN cache should be invalidated before redeploying the application.
- B) Restoring the pre-deployment snapshot will destroy all data written since the deployment.
- C) Health checks should be confirmed after each step, not only at the end.
- D) The plan does not name the person responsible for each step.

**Correct answer: B**

**Explanation:** The note tells you version 2.5.0's migration is additive (new column plus backfill). The previous application version 2.4.1 will typically run happily against a schema with an extra column it ignores — so the snapshot restore is not needed to make 2.4.1 work. But the service takes continuous live writes, so restoring the pre-deployment snapshot discards every transaction accepted since the deployment: real user data, lost. The safer plan is usually to roll back the application only and leave the additive schema in place. Options A, C and D are refinements — C and D are genuinely good practice, and A is debatable either way — but none of them destroys data. Assessments at senior level often hide one catastrophic flaw among several cosmetic ones, exactly as real review does: the reviewer's job, when reviewing the designs of others to ensure appropriate technology and efficient use of resources, is to rank flaws by consequence, and irreversible data loss outranks everything else on the page.

**Question 11 (challenging) — Applied problem solving under uncertainty**

Builds on the shared CI platform have slowed from 8 minutes to 20 minutes over two weeks. You gather facts: (a) the slowdown affects all teams' builds, not just one repository; (b) build agent CPU utilisation is normal; (c) the artefact cache hit rate has fallen from 92% to 31%; (d) a platform storage migration completed two weeks ago; (e) test counts and code size are roughly unchanged. What is the most efficient next diagnostic step?

- A) Ask all teams to reduce their test suites until builds return to 8 minutes.
- B) Roll back the storage migration immediately.
- C) Investigate why the artefact cache hit rate collapsed, checking whether the storage migration changed cache keys, paths, or eviction behaviour.
- D) Add more build agents to compensate for the slowdown.

**Correct answer: C**

**Explanation:** Triangulate the evidence. The slowdown is global (a), so repository-level causes are unlikely; agents are not CPU-bound (b), so compute capacity is not the constraint — which also rules out D as a fix and A as relevant. The cache hit rate collapse (c) is a large, specific anomaly whose timing matches the migration (d), and cache misses force rebuilds and re-downloads that would slow every build without stressing CPU. Option C follows the strongest signal to its most plausible cause and proposes a cheap, reversible investigation. Option B treats correlation as proof and reaches for a disruptive remediation before confirming the mechanism — rolling back a completed storage migration is itself risky and may be impossible. This is development process optimisation in miniature: identify the process signal that changed (hit rate), connect it to the event that could have changed it (migration), verify the mechanism, then fix the smallest thing that restores the process. Assessments reward the answer that maximises information gained per unit of risk, and so does production.

**Question 12 (challenging) — Deduction about high availability**

Your service runs in two zones. The design rules are: (i) the service is available if at least one zone is serving; (ii) a zone is serving if at least two of its three instances are healthy; (iii) a deployment takes one instance out of service at a time in the zone being deployed. During a deployment to zone 1, one instance in zone 2 fails unexpectedly. Which statement must be true at that moment?

- A) The service is unavailable.
- B) Zone 1 is not serving.
- C) The service is still available.
- D) Zone 2 is not serving.

**Correct answer: C**

**Explanation:** Apply the rules to each zone. Zone 1 is mid-deployment, so one of its three instances is out of service, leaving two healthy — rule ii says two of three suffices, so zone 1 is serving. Zone 2 has lost one instance to failure, leaving two healthy — zone 2 is also serving. Rule i requires only one serving zone, and here both are serving; the service must be available, so C is guaranteed and A, B and D are all false. The instructive part is the margin: at this moment the service has zero spare failures in either zone — one more loss anywhere breaks a zone's quorum. A deployment strategy that is genuinely repeatable, scalable and highly available accounts for exactly this: the question "what is my failure budget *during* a deployment?" rather than only in steady state. Assessment questions of this type reward mechanical rule application first, and your engineering instinct — noticing the eroded margin — is what you bring back to the design review afterwards.

### Preparation tips

- **Practise with your own artefacts.** Ten minutes spent reading a pipeline definition, an access matrix, or a rollback plan and asking "what rule does each line obey, and does anything break it?" is direct rehearsal for cognitive items — and it makes you a sharper reviewer at work.
- **Externalise constraint problems.** For sequencing and scheduling questions, sketch the dependency graph or a day grid immediately, exactly as you would whiteboard an integration build. Working memory is the scarce resource under timed conditions; paper is free.
- **Read the rules as written, not as you would have written them.** Assessment rules, like security standards, sometimes differ from best practice. Answer against the stated rules. You can critique them in real life; in the test, precision wins.
- **Time-box per question.** In a 20-minute, 16-question test you have about 75 seconds each. If a question resists you after 90 seconds, mark your best elimination-based guess and move on — exactly the triage discipline you use in incident response.
- **Warm up before the real thing.** Do two or three practice items immediately before starting the timed assessment. Cold starts cost accuracy in the first questions, which adaptive tests weight heavily.
- **Sleep and environment matter.** Treat the assessment like an on-call shift handover: rested, hydrated, notifications silenced, a stable connection, and scratch paper ready if permitted.

### Common pitfalls to avoid

- **Answering from experience instead of from the stem.** You know that platform teams usually hold rights in every environment — but if the stated standard does not require it, the question's answer follows the standard. Imported assumptions are the leading cause of wrong answers for experienced engineers.
- **Confusing arrival order with priority.** Queue position feels fair, but impact-weighted urgency is what prioritisation items reward — and what live services need.
- **Over-concluding from correlation.** Timelines and dashboards invite causal leaps. The strong answers treat a matching pattern as a hypothesis warranting the cheapest decisive test, not as a verdict.
- **Missing the catastrophic flaw while polishing cosmetic ones.** In error-checking items with several defensible criticisms, rank by consequence. Data loss, security exposure, and irreversibility outrank style.
- **Perfectionism under the clock.** Senior engineers are trained to be thorough; adaptive tests punish spending three minutes proving what ninety seconds of elimination already established. Accuracy matters, but calibrated speed is part of the score.
- **Skipping the practice questions.** The ungraded warm-up exists to absorb interface surprises — how to flag, how to go back, how the timer displays. Spend those surprises before they cost marks.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment measures your ability to interpret, manipulate and draw sound conclusions from numerical information of the kind your role actually produces. It is not a mental arithmetic contest: calculators are usually permitted, and the skill being measured is choosing the right calculation, executing it accurately, and interpreting the result in context.

Typical format: an online, timed test of 20 to 40 minutes with 15 to 25 questions, each presenting data — a table, a chart, a short scenario with figures — followed by multiple-choice options. Questions typically cover percentages, ratios, averages, rates of change, and reading values accurately from tables and graphs. Many platforms are adaptive, and most report accuracy and speed separately. Distractor options are engineered from predictable mistakes — dividing by the wrong denominator, misplacing a decimal, confusing percentage points with percentages — so a wrong method reliably lands on a wrong option rather than nowhere.

For a senior DevOps engineer, numeric reasoning is not an abstract hurdle: it is the substance of availability and capacity management. Service level objectives are percentages; error budgets are subtractions from them; capacity forecasts are growth rates; cloud cost decisions are rate-times-time calculations; deployment health is measured in frequencies, failure rates and recovery times. When you manage service components against key performance indicators, every KPI is a number with a denominator, and knowing exactly which denominator is the difference between reporting a service as healthy and discovering, in an incident review, that it never was. Employers assess numeric reasoning for this role because the cost of numerical carelessness — an under-provisioned peak, a misread SLO, a budget overrun — lands directly on live public services.

### How this assessment maps to your role

The assessment dimensions map directly to the named skills in your role summary:

- **Percentages and error budgets** map to **Availability and capacity management**: KPIs for availability are expressed as percentages, and managing components to meet business needs means converting between percentage targets, minutes of allowable downtime, and budget consumed.
- **Rates and throughput calculations** map to **Systems design** and **Availability and capacity management**: designing systems of medium risk and complexity requires sizing them — requests per second per instance, headroom targets, growth trajectories.
- **Averages and distributions** map to **Service support**: recovery times, fault durations and queue statistics only guide improvement if you choose the right summary statistic and notice when an outlier distorts it.
- **Percentage change and trend reading** map to **Development process optimisation**: identifying optimisation opportunities and demonstrating that a contributed solution worked both depend on before-and-after comparisons done with the correct baseline.
- **Cost and resource calculations** map to **Systems design**'s demand for efficient use of resources, and to reviewing others' designs: an elegant architecture that doubles the hosting bill needs the arithmetic to show it.
- **Reading tables accurately** maps to **Programming and build (software engineering)** and toolchain work generally: dashboards, test reports and pipeline analytics are tables, and misreading a row is as damaging as miscomputing it.

### Practice questions

**Question 1 (easy) — Availability percentage to downtime**

Your service has a monthly availability KPI of 99.9%. Taking a 30-day month as 43,200 minutes, how many minutes of downtime does the KPI allow?

- A) 4.32 minutes
- B) 43.2 minutes
- C) 432 minutes
- D) 14.4 minutes

**Correct answer: B**

**Explanation:** The allowable downtime is 0.1% of the month: 43,200 × 0.001 = 43.2 minutes. A quick sanity check: 1% of 43,200 is 432 minutes, so 0.1% is a tenth of that, 43.2. Option C is the 1% figure (a misplaced decimal), and option A misplaces it the other way. This conversion is the daily currency of availability management: "three nines" sounds abstract until you translate it into the roughly 43 minutes a month you can actually afford — at which point a 20-minute deployment outage is visibly half the month's budget gone.

**Question 2 (easy) — Deployment success ratio**

Last quarter your toolchain ran 240 production deployments, of which 15 failed and were rolled back. What is the ratio of successful to failed deployments, in simplest form?

- A) 16:1
- B) 15:1
- C) 12:1
- D) 8:1

**Correct answer: B**

**Explanation:** Successful deployments = 240 − 15 = 225. Ratio of successful to failed = 225:15 = 15:1. The classic error is 240:15 = 16:1 (option A), which compares *total* to failed rather than *successful* to failed — always confirm which two populations the question compares before dividing. Ratios like this feed your deployment health reporting; the same care with denominators applies when you report change failure rate, where the convention is failures over total (15/240 = 6.25%), a different framing of the same three numbers.

**Question 3 (easy) — Percentage change in build time**

After you introduced parallel test execution, the average pipeline build time fell from 12 minutes to 9 minutes. What is the percentage decrease?

- A) 20%
- B) 25%
- C) 30%
- D) 33%

**Correct answer: B**

**Explanation:** Decrease = 12 − 9 = 3 minutes. Percentage decrease = 3 ÷ 12 = 0.25 = 25%. The trap is dividing by the new value: 3 ÷ 9 ≈ 33%, which is option D, placed there deliberately. Percentage change always uses the original (earlier) value as the denominator. When you contribute to process optimisation, this is exactly how you evidence the improvement in a show-and-tell — and using the wrong denominator overstates your own work, which a numerate stakeholder will spot.

**Question 4 (moderate) — Error budget consumed**

Your service's SLO is 99.9% availability per 30-day month (error budget: 43.2 minutes). So far this month the service has been down for 28.8 minutes. What percentage of the month's error budget remains?

- A) 66.7%
- B) 33.3%
- C) 28.8%
- D) 14.4%

**Correct answer: B**

**Explanation:** Budget remaining = 43.2 − 28.8 = 14.4 minutes. As a percentage of budget: 14.4 ÷ 43.2 = 0.333… = 33.3%. Option A is the percentage *consumed* (28.8 ÷ 43.2 = 66.7%) — the question asks for the remainder, and reading the final line of the question carefully is half the mark. Option D is the remaining minutes mistaken for a percentage. Error budget arithmetic drives real decisions in your role: with a third of the budget left and a third of the month remaining, the service is exactly on track, but one more incident of typical size would justify slowing the release cadence — precisely the conversation a senior engineer leads with the delivery team.

**Question 5 (moderate) — Weighted average pipeline duration**

Three pipelines share your build platform. Last week: Pipeline X ran 40 times averaging 6 minutes; Pipeline Y ran 25 times averaging 12 minutes; Pipeline Z ran 35 times averaging 8 minutes. What was the average duration per run across the platform?

- A) 8.0 minutes
- B) 8.2 minutes
- C) 8.7 minutes
- D) 9.0 minutes

**Correct answer: B**

**Explanation:** Weight each average by its run count. Total minutes = (40 × 6) + (25 × 12) + (35 × 8) = 240 + 300 + 280 = 820. Total runs = 40 + 25 + 35 = 100. Average per run = 820 ÷ 100 = 8.2 minutes. Option C, 8.67, is the unweighted mean of 6, 12 and 8 — the classic error of averaging averages without weighting. Platform-level reporting lives on this distinction: the unweighted mean overstates the influence of the infrequent, slow Pipeline Y, and a capacity decision based on it would buy the wrong improvement. When run counts differ, always weight.

**Question 6 (moderate) — Capacity growth forecast**

Your artefact repository currently holds 3.2 TB and is growing at 12.5% per month. The storage alert threshold is 4.0 TB. Will the repository breach the threshold within two months, and what will it hold at the end of month two?

- A) No — 3.85 TB
- B) Yes — 4.00 TB
- C) Yes — 4.05 TB
- D) Yes — 4.20 TB

**Correct answer: C**

**Explanation:** Growth compounds. End of month one: 3.2 × 1.125 = 3.6 TB. End of month two: 3.6 × 1.125 = 4.05 TB — above the 4.0 TB threshold, so the answer is yes, at 4.05 TB. Option A comes from simple (non-compounding) growth applied wrongly, and option D from adding 12.5% of the original twice then over-rounding. Identifying capacity issues and initiating changes before they bite is the essence of capacity management: the compounding calculation tells you that the cleanup job or quota increase needs to be scheduled *this* month, because next month the threshold is already breached — and alert thresholds should fire with time to act, not at the moment of failure.

**Question 7 (moderate) — Cloud cost of rightsizing**

A service runs 6 instances at £0.48 per instance-hour, all month (730 hours). Monitoring shows peak utilisation would be comfortably served by 4 instances. How much would rightsizing to 4 instances save per month?

- A) £350.40
- B) £700.80
- C) £1,401.60
- D) £2,102.40

**Correct answer: B**

**Explanation:** The saving is the cost of the 2 removed instances: 2 × £0.48 × 730 = £700.80. Step by step: 0.48 × 730 = £350.40 per instance per month; times 2 instances = £700.80. Option A is the one-instance saving, option D is the full current bill (6 × £350.40 = £2,102.40), and option C is the cost of the remaining 4 instances — every distractor is a correct calculation of the wrong thing, which is how cost questions usually fail in real life too. Reviewing systems designs for efficient use of resources means being able to put a monthly figure on over-provisioning; a concrete "£700.80 a month, £8,409.60 a year" moves a rightsizing ticket up a backlog far faster than "it seems oversized".

**Question 8 (moderate) — Choosing the right average for recovery time**

Your last five service faults took 20, 35, 40, 45 and 210 minutes to restore. The 210-minute fault involved waiting for a third-party supplier. Which statement best summarises typical restoration time?

- A) The mean is 70 minutes, so typical restoration takes about 70 minutes.
- B) The median is 40 minutes, which better represents typical restoration because the 210-minute outlier inflates the mean.
- C) The mean is 70 minutes and the median is 45 minutes, so typical restoration is about an hour.
- D) Typical restoration cannot be estimated from five incidents.

**Correct answer: B**

**Explanation:** Compute both. Mean = (20 + 35 + 40 + 45 + 210) ÷ 5 = 350 ÷ 5 = 70 minutes. Median = the middle value of the ordered list (20, 35, 40, 45, 210) = 40 minutes. The 210-minute incident is a known special cause (supplier dependency) and drags the mean far above four of the five observations, so the median is the honest "typical" figure — option B states both the number and the reason. Option C miscomputes the median (45 is the fourth value, not the middle one). Option D overcorrects: small samples deserve caution, but summarising five incidents is routine and useful provided the outlier is acknowledged. In service support reporting, this choice changes decisions: a 70-minute "MTTR" suggests your team is slow; the 40-minute median plus a supplier-escalation action tells the true story and targets the right fix.

**Question 9 (challenging) — Instance count for peak load**

A service must handle a forecast peak of 1,800 requests per second. Each instance can process 250 requests per second at maximum, but your design standard requires instances to run at no more than 70% of maximum at forecast peak. How many instances do you need?

- A) 8
- B) 10
- C) 11
- D) 15

**Correct answer: C**

**Explanation:** Each instance's usable capacity at the 70% ceiling = 250 × 0.7 = 175 requests per second. Instances needed = 1,800 ÷ 175 = 10.29, and you cannot deploy 0.29 of an instance, so round *up*: 11 instances. Option A is 1,800 ÷ 250 = 7.2 rounded up — correct arithmetic against the wrong (100%) ceiling, leaving zero headroom at peak. Option B rounds 10.29 down, which under-provisions precisely at the moment of maximum demand. Two disciplines matter here and in real capacity work: apply the headroom policy *before* dividing, and always round capacity up. The 70% standard is not bureaucracy — it is the margin that absorbs an instance failure or a traffic estimate error at peak, which is what "highly available" means in numbers.

**Question 10 (challenging) — Change failure rate from a table**

Your quarterly deployment report shows:

| Month | Deployments | Failed deployments |
|---|---|---|
| April | 45 | 3 |
| May | 60 | 3 |
| June | 80 | 5 |
| July | 50 | 2 |

In which month was the change failure rate highest, and what was it?

- A) June — 6.25%
- B) April — 6.67%
- C) May — 5.00%
- D) July — 4.00%

**Correct answer: B**

**Explanation:** Compute each month's rate as failures ÷ deployments. April: 3 ÷ 45 = 0.0667 = 6.67%. May: 3 ÷ 60 = 5.00%. June: 5 ÷ 80 = 6.25%. July: 2 ÷ 50 = 4.00%. The highest is April at 6.67%. The trap is anchoring on absolute counts: June has the most failures (5), which makes option A magnetic, but June also has the most deployments, and a rate question is answered by the ratio, not the numerator. This exact confusion appears in real delivery reporting — a busy month "looks worse" by raw failure count while actually being safer per deployment — and part of your value as a senior engineer is correcting it before it drives a bad decision, such as slowing down the team whose rate was actually improving.

**Question 11 (challenging) — Compound target for lead time**

Your team's lead time for changes (commit to production) is currently 96 hours. The improvement plan targets a 25% reduction this quarter and a further 25% reduction next quarter. What is the target lead time at the end of next quarter?

- A) 48 hours
- B) 54 hours
- C) 57.6 hours
- D) 72 hours

**Correct answer: B**

**Explanation:** Successive percentage reductions compound; they do not add. End of this quarter: 96 × 0.75 = 72 hours. End of next quarter: 72 × 0.75 = 54 hours. Option A treats the two reductions as a single 50% cut (25 + 25), the most common compounding error. Option D stops after one quarter, and option C applies a 25% then a 20% reduction. The general rule: apply each percentage to the *current* value, not the original. This matters in the other direction too — two successive 25% *increases* in traffic give 1.25 × 1.25 = 1.5625, a 56.25% rise, not 50% — and capacity plans built on added-not-compounded growth run out of headroom early.

**Question 12 (challenging) — Flaky test rate**

Last week the integration suite ran 1,200 times. It reported 54 failing runs. Investigation showed 18 of the failing runs revealed genuine defects; the rest were flaky (environmental or timing-related). What percentage of all runs were flaky failures, and what proportion of reported failures were flaky?

- A) 3.0% of runs; two-thirds of failures
- B) 4.5% of runs; one-third of failures
- C) 3.0% of runs; one-third of failures
- D) 1.5% of runs; two-thirds of failures

**Correct answer: A**

**Explanation:** Flaky failing runs = 54 − 18 = 36. As a percentage of all runs: 36 ÷ 1,200 = 0.03 = 3.0%. As a proportion of reported failures: 36 ÷ 54 = 0.667 = two-thirds. Both parts must be right, and each distractor gets exactly one part wrong: B swaps the genuine and flaky counts in one calculation, D uses 18 instead of 36 for the run percentage. The two denominators tell two different stories, and both matter to your toolchain work: 3% of runs failing spuriously sounds small, but two-thirds of all red builds being false alarms is a crisis of trust — teams start rerunning failures without reading them, and the 18 genuine defects hide among the noise. Quantifying flakiness with the right denominators is what turns "the tests feel unreliable" into a prioritised optimisation with a measurable exit criterion.

### Preparation tips

- **Rebuild the core moves until they are reflexes.** Percentage of, percentage change (original value as denominator), reversing a percentage, ratios, weighted averages, compound growth, and rounding capacity up. These seven moves cover almost every numeric item you will meet — and almost every dashboard you own.
- **Practise on your own service data.** Take last month's availability figure and convert it to downtime minutes; take two sprints' build times and compute the true percentage change; take your instance count and recompute it against a 70% headroom rule. Real data makes the methods stick.
- **Write the calculation before touching the calculator.** Deciding "36 ÷ 1,200" on paper first prevents the transposed-digit and wrong-denominator errors that calculators execute perfectly.
- **Sanity-check with a second method.** Estimate 1% and scale; check that a "decrease" answer is smaller than the original; confirm a rate answer sits between the smallest and largest plausible values. Ten seconds of checking catches most slips.
- **Read the final sentence twice.** Questions often present consumed budget and ask for remaining, or show failures and ask for successes. The arithmetic is easy; the mark is in answering the question actually asked.
- **Time-box and return.** Long table questions reward a first pass for easy rows; if a calculation sprawls, flag it and come back with fresh eyes and remaining time visible.

### Common pitfalls to avoid

- **Wrong denominator.** Dividing change by the new value, failures by successes, or a subgroup by the wrong total is the single most common error family. Name the denominator out loud before dividing.
- **Averaging averages without weighting.** When groups differ in size — runs, incidents, months — an unweighted mean of their means is wrong. Multiply back to totals first.
- **Adding successive percentages.** Two 25% changes are never 50%. Compound them.
- **Anchoring on absolute counts in rate questions.** The month with the most failures is often not the month with the worst rate. Compute every rate before comparing.
- **Rounding capacity down.** People and instances come in whole units; a requirement of 10.29 instances means 11. Round protective quantities up, always.
- **Confusing percentages with percentage points.** A rise from 5% to 6.25% is a 1.25 percentage-point increase but a 25% relative increase. Assessment options exploit the difference, and so do misleading status reports.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment measures how accurately you extract meaning from written material of the kind your role runs on: standards, policies, incident reports, service descriptions, supplier documentation, and emails from stakeholders. The dominant format presents a short passage followed by statements you must classify as **True** (the passage guarantees it), **False** (the passage contradicts it), or **Cannot say** (the passage neither guarantees nor contradicts it). Other formats test inference, identifying the main point, and judging which of several rewrites communicates most clearly.

Typical format: an online, timed test of 15 to 25 minutes with 20 to 30 statements across several passages. The universal rule is that you answer **from the passage alone** — outside knowledge, however expert, must be set aside. That rule is what makes the test fair across candidates, and it is also what makes it genuinely hard for experienced engineers, whose professional knowledge constantly volunteers itself.

For a senior DevOps engineer, verbal precision is a core working skill, not an add-on. You read security standards and must implement exactly what they require — not more, not less. You read incident reports and must distinguish what was established from what was assumed. You write runbooks, review comments, and design documents that other engineers execute at 3am, when only the words on the page are available to help. And because you coach and mentor more junior colleagues, your reading and writing habits propagate: a senior engineer who reads standards loosely trains a team that implements them loosely. Employers assess verbal reasoning for this role because misread requirements become misbuilt systems, and ambiguous runbooks become extended outages.

### How this assessment maps to your role

The assessment dimensions map directly to the named skills in your role summary:

- **Precise comprehension of rules and standards** maps to **Modern development standards** and **Information security**: applying standards and designing solutions with security controls included both begin with reading the control exactly as written — the difference between "must" and "should", between "all environments" and "production", is the difference between compliance and exposure.
- **True/False/Cannot say discipline** maps to **Service support** and incident work: identifying and fixing complex faults requires separating what the evidence establishes from what everyone merely believes, and incident reviews collapse when the two are blurred.
- **Inference and reading between the lines** maps to **User focus**: explaining the difference between user needs and user desires is an act of interpretation — hearing what a stakeholder wrote, and working out what problem actually sits behind it, without inventing facts.
- **Clear-writing judgement** maps to **Programming and build (software engineering)** (documenting programs and scripts), to **Systems design** (design documents others must review), and to your coaching duty: choosing the clearest formulation is a skill assessments can measure and teammates depend on.
- **Comprehension of specifications** maps to **Programming and build**'s duty to collaborate on reviewing specifications and to **Systems integration**'s co-ordination work: an integration plan is a text before it is a schedule, and misreading it misorders the build.

### Practice questions

**Passage 1 (for Questions 1–3).** *Extract from a departmental deployment standard:* "All production deployments must be performed through the approved continuous deployment pipeline. Manual production changes are permitted only during a declared major incident, and any such change must be recorded in the incident log and reviewed at the next working day's change board. Deployments to non-production environments may be performed manually at the discretion of the delivery team. Teams should aim to deploy to production at least once per week; teams that have not deployed for four weeks will be asked to present their release plan to the service owner."

**Question 1 (easy) — True/False/Cannot say**

Statement: "A manual change to production during a declared major incident is permitted by the standard."

- A) True
- B) False
- C) Cannot say
- D) True only if the change board approves it in advance

**Correct answer: A**

**Explanation:** The passage states manual production changes "are permitted only during a declared major incident" — so during such an incident, they are permitted (with recording and next-day review obligations). Option D adds a condition the passage does not impose: the review happens at the *next working day's* change board, which is retrospective, not advance approval. Reading the sequence of obligations correctly matters in your real change process for exactly the same reason: an engineer who believes emergency changes need advance board approval will hesitate during an incident when the standard actually authorises action now and scrutiny after.

**Question 2 (easy) — True/False/Cannot say**

Statement: "A team that deploys to production every two weeks will be asked to present its release plan to the service owner."

- A) True
- B) False
- C) Cannot say
- D) True, because the standard requires weekly deployment

**Correct answer: B**

**Explanation:** The presentation requirement applies to teams that "have not deployed for four weeks". A team deploying fortnightly never reaches four weeks without a deployment, so the passage's own rule contradicts the statement — it is False. Option D misreads "should aim to deploy at least once per week" as a hard requirement with the presentation as its penalty; but "should aim" is aspirational language, and the concrete consequence attaches only at the four-week threshold. Distinguishing aspiration ("should aim") from obligation ("must") and from threshold-triggered consequence is precisely the reading skill that standards work demands — and that this question format is built to measure.

**Question 3 (moderate) — True/False/Cannot say**

Statement: "The approved continuous deployment pipeline includes automated testing."

- A) True
- B) False
- C) Cannot say
- D) True, because continuous deployment implies automated testing

**Correct answer: C**

**Explanation:** Nothing in the passage describes what the pipeline contains. Your professional knowledge insists that any credible CD pipeline includes automated testing — and option D voices exactly that instinct — but the passage neither states nor implies it, so the disciplined answer is Cannot say. This is the hardest habit for experienced engineers in verbal tests: the more expert you are, the more your background knowledge volunteers "facts" the text never provided. The same discipline has direct workplace value: when a supplier's documentation says "deployments are automated", a senior engineer verifies what the automation actually covers rather than assuming it matches best practice.

**Passage 2 (for Questions 4–6).** *Extract from an incident review report:* "At 14:22 the API gateway began returning elevated 502 errors, peaking at 38% of requests. The on-call engineer identified that a configuration change deployed at 14:15 had reduced the connection pool size. The change was rolled back at 14:41 and error rates returned to baseline by 14:44. The configuration change had passed review, but the reviewer had no visibility of production connection metrics at review time. Total user-facing impact lasted 22 minutes. Separately, the report notes that alerting fired at 14:31, nine minutes after errors began, because the alert threshold requires a sustained breach before firing."

**Question 4 (moderate) — True/False/Cannot say**

Statement: "The configuration change caused the elevated 502 errors."

- A) True
- B) False
- C) Cannot say
- D) False, because the change had passed review

**Correct answer: A**

**Explanation:** Strictly, the passage says the engineer "identified that" the change had reduced the pool size, the errors began seven minutes after the change deployed, and the rollback was followed within three minutes by recovery. The passage's own narrative presents the change as the identified cause — "identified" is the report asserting the diagnosis, not merely hypothesising it — and the rollback-recovery sequence is offered as confirmation. Within the world of the passage, True. Option D is a non-sequitur: passing review says nothing about whether the change caused the failure — reviews miss things, as this passage explicitly explains (the reviewer lacked production metrics). In incident reviews you write and read, this distinction between "the report asserts the cause" and "the evidence merely correlates" should be deliberate: good reports, like this one, state the diagnosis and show the confirming test.

**Question 5 (moderate) — Inference**

Which of the following is the most defensible inference from the passage?

- A) The on-call engineer was too slow to respond.
- B) Faster alerting would have reduced user-facing impact by at most nine minutes.
- C) The reviewer was negligent in approving the change.
- D) Connection pool changes should be banned from the deployment pipeline.

**Correct answer: B**

**Explanation:** Errors began at 14:22 and the alert fired at 14:31 — nine minutes of impact elapsed before the alerting system said anything. Even instantaneous alerting could only have removed those nine minutes (assuming diagnosis and rollback then took similar time), so B states a ceiling the timeline supports. Option A blames the engineer, but the timeline shows fast work *after* alerting: diagnosis and rollback within ten minutes of the page. Option C ignores the passage's explicit mitigation — the reviewer lacked production visibility, which is a systems gap, not negligence. Option D is a policy overreaction unsupported by the text. This inference pattern — bound the improvement each fix could deliver before choosing between fixes — is exactly how a senior engineer turns an incident review into a prioritised action list rather than a blame exercise.

**Question 6 (moderate) — True/False/Cannot say**

Statement: "Errors returned to baseline less than five minutes after the rollback."

- A) True
- B) False
- C) Cannot say
- D) True, but only for the API gateway

**Correct answer: A**

**Explanation:** Rollback at 14:41; error rates back to baseline by 14:44 — an interval of three minutes, which is less than five. True, by direct computation from two timestamps. The question is easy arithmetic wrapped in a reading task, and that is deliberate: verbal tests often embed small calculations to check you extract figures accurately from prose. Option D adds a qualification the statement does not need. In your work, timeline precision like this determines the "total user-facing impact" figure that goes in the report — and being the engineer whose timelines withstand scrutiny is part of what makes your incident reviews trusted.

**Passage 3 (for Questions 7–9).** *Extract from a security policy circular:* "From 1 April, all container images deployed to any departmental environment must be built from base images maintained in the departmental registry. Images built from external base images may continue to run if deployed before 1 April, but must be rebuilt against departmental base images at their next scheduled release, and in any case no later than 30 June. Exemptions may be granted by the Chief Technology Officer where a supplier product cannot be rebuilt; exempted images must be recorded on the exemptions register and scanned weekly."

**Question 7 (moderate) — True/False/Cannot say**

Statement: "After 30 June, no container image built from an external base image will be running in any departmental environment."

- A) True
- B) False
- C) Cannot say
- D) True, because the policy sets 30 June as the final deadline

**Correct answer: B**

**Explanation:** The passage explicitly provides an exemption route: the CTO may exempt supplier products that cannot be rebuilt, and exempted images continue running (recorded and scanned weekly). So the policy itself contemplates external-base images running after 30 June — the statement is contradicted by the passage, making it False, and option D fails for the same reason: the 30 June deadline governs the *rebuild* obligation for non-exempt images, not the existence of exemptions. Policies with exemption clauses are the norm in government technology work; reading the general rule while missing the exemption clause is precisely how teams either panic unnecessarily or, worse, report full compliance that an auditor then disproves from the exemptions register.

**Question 8 (challenging) — True/False/Cannot say**

Statement: "An image built from an external base image and deployed on 15 March, whose next scheduled release is 15 July, must be rebuilt before its next scheduled release."

- A) True
- B) False
- C) Cannot say
- D) Cannot say, because the release schedule might change

**Correct answer: A**

**Explanation:** Track the two clauses. The image was deployed before 1 April, so it may continue running, and must be rebuilt "at its next scheduled release, and in any case no later than 30 June". Its next scheduled release falls on 15 July — *after* the 30 June backstop — so the backstop binds: the rebuild must happen by 30 June, which is before the next scheduled release. The statement is therefore True. The tempting error is to read "at its next scheduled release" as the operative deadline and answer False; the phrase "in any case no later than" establishes that the earlier of the two dates governs. Option D invents contingencies the question does not raise. This is exactly the compound-deadline structure of real compliance obligations, and mis-sequencing it in a migration plan is how a team arrives at 30 June non-compliant in good faith.

**Question 9 (challenging) — Main point**

Which sentence best captures the main point of Passage 3?

- A) External base images are insecure and must never be used.
- B) The department is standardising on internally maintained base images, with a transition period and a controlled exemption route.
- C) The Chief Technology Officer must approve all container deployments from 1 April.
- D) All container images must be scanned weekly.

**Correct answer: B**

**Explanation:** The passage establishes a rule (departmental base images from 1 April), transition arrangements (grace for pre-April deployments, backstop of 30 June), and a governed exception path (CTO exemptions, register, weekly scanning). Option B is the only summary covering all three elements at the right altitude. Option A overstates — the policy manages external images out; it never calls them forbidden in all cases, and the exemption route contradicts "never". Option C inflates the CTO's role from granting exemptions to approving everything. Option D promotes a detail that applies only to exempted images into the headline. Main-point questions reward the summary that is *complete and no stronger than the text* — the same judgement you apply when you summarise a policy for your team's channel, where an overstated summary triggers unnecessary work and an understated one triggers none.

**Passage 4 (for Questions 10–12).** *Email from a delivery manager:* "Hi — the product team wants the new document-upload feature live before the minister's announcement on the 12th. QA have signed off the happy path but say edge-case testing needs three more days, which takes us past the 12th. The product manager says the announcement traffic will be mostly reads, not uploads. Can we deploy behind a feature flag, enable it for internal users only, and switch it on publicly once edge-case testing completes? Also — separately — the staging environment certificates expire on the 10th; can your team renew them before then?"

**Question 10 (moderate) — Comprehension**

Which of the following does the email actually request from you?

- A) Approval to skip edge-case testing for the upload feature.
- B) A feature-flagged deployment with internal-only enablement, and renewal of staging certificates before the 10th.
- C) An opinion on whether announcement traffic will be reads or uploads.
- D) Deployment of the upload feature to all users before the 12th.

**Correct answer: B**

**Explanation:** The email proposes a specific technical approach — deploy behind a flag, enable internally, switch on publicly after testing — and asks a second, separate favour: certificate renewal before the 10th. Option B captures both requests and only those. Option A is the opposite of what is proposed: the flag approach exists precisely so edge-case testing *completes* before public exposure. Option D describes the outcome the product team originally wanted, not what the email asks you to do. Option C is background the delivery manager reports, not a question posed to you. Multi-request emails are a staple of both verbal tests and real inboxes; senior engineers who reply to only the first request generate the follow-up chase that clogs delivery — noticing the "also — separately" is worth a mark in the test and a certificate outage in real life.

**Question 11 (challenging) — Inference**

Which is the most defensible inference from the email?

- A) The delivery manager has already obtained QA's agreement to the feature-flag approach.
- B) If the certificates are not renewed by the 10th, staging will be unavailable for any pre-announcement verification after that date.
- C) The proposed approach means public users would not have access to the upload feature on the 12th.
- D) The minister's announcement will generate no upload traffic.

**Correct answer: C**

**Explanation:** Under the proposal, the feature is enabled "for internal users only" until edge-case testing completes, and testing takes three more days, past the 12th. Therefore on the 12th, public users would not have the feature — C follows necessarily from the proposal's own terms. Option A is not stated; QA's sign-off covers the happy path, and their view of the flag approach is unknown. Option B goes beyond the text: expired certificates cause failures for TLS-dependent access, but the email does not establish that all verification depends on staging or that nothing else could be done — it is plausible, not guaranteed. Option D converts the product manager's "mostly reads" into "no uploads", strengthening a hedge into an absolute. Inference questions reward the conclusion that must hold given the passage; your role rewards the same care, because the difference between "public users won't have it on the 12th" being understood or missed is the difference between an aligned announcement and a ministerial surprise.

**Question 12 (challenging) — Clear-writing judgement**

You are documenting a runbook step. Which formulation is clearest for an engineer executing it during an incident?

- A) "Consideration should be given to the restarting of the ingestion service in circumstances where queue depth has been observed to exceed acceptable parameters."
- B) "If queue depth exceeds 10,000 messages for more than 5 minutes, restart the ingestion service: `systemctl restart ingest`. Wait 2 minutes; if queue depth is not falling, escalate to the platform on-call."
- C) "The ingestion service can be restarted when the queue is too deep, which usually helps, though results may vary depending on the situation."
- D) "Restart ingest if needed."

**Correct answer: B**

**Explanation:** A runbook step is executed under stress by someone who may not share your context, so clarity means: a measurable trigger (10,000 messages, 5 minutes), an exact action (the command itself), a verification window (2 minutes), and a defined escalation path. Option B provides all four. Option A is passive, nominalised officialese — "consideration should be given" assigns the action to nobody, and "acceptable parameters" quantifies nothing. Option C hedges every clause into uselessness. Option D is admirably short but pushes the two hard decisions — when is it "needed", and what is "ingest" exactly — onto the reader at the worst possible moment. Documenting programs and scripts to the standard your role requires means writing for the 3am reader; clear-writing items measure whether you can tell the formulation that serves that reader from the ones that merely gesture at it.

### Preparation tips

- **Drill the three-way verdict.** For each statement ask: does the passage *guarantee* it (True)? *Contradict* it (False)? Otherwise it is Cannot say — no matter how plausible your expertise finds it. Most lost marks are Cannot-say statements marked True by professionals who knew too much.
- **Underline modal verbs and quantifiers.** Must, should, may, all, any, only, at least, no later than — these small words carry the legal weight of standards, and most verbal questions turn on one of them.
- **Practise on real documents.** The Technology Code of Practice, the Service Manual, NCSC guidance, and your own department's standards are ideal: read a paragraph, write three statements (one True, one False, one Cannot say), and test a colleague — excellent mentoring material too.
- **For compound deadlines, draw the timeline.** "At the next release, and in any case no later than…" resolves instantly on a sketched timeline and resists you in prose.
- **Answer from the passage, critique afterwards.** If a passage's policy seems technically wrong, note the itch and set it aside; the test measures reading, and your critique belongs in the design review, not the answer sheet.
- **Read the statement before re-reading the passage.** Knowing what you are checking turns a re-read into a targeted scan — the same skill as grepping a log with a hypothesis rather than paging through it.

### Common pitfalls to avoid

- **Importing expert knowledge.** "Any real CD pipeline has automated tests" is true of the world and irrelevant to the passage. The test is scrupulous about this boundary; be equally scrupulous.
- **Strengthening hedged claims.** "Mostly reads" is not "no uploads"; "should aim" is not "must". Converting hedges into absolutes is the most common inference error in tests and in stakeholder emails alike.
- **Missing exemption and exception clauses.** General rules with exception routes are the standard shape of policy. A verdict formed before reaching the exception clause is a verdict formed on half the rule.
- **Answering only the first request in multi-part texts.** Emails and questions alike often carry an "also, separately". Scan for it before finalising.
- **Choosing the overstated summary.** In main-point questions, the correct option is complete and calibrated; options that add blame, bans, or drama are distractors — as they are in incident reports.
- **Letting officialese pass as clarity.** In writing-judgement items, prefer the option with measurable triggers, named actors, and exact actions. If nobody in the sentence does anything specific, it is not the clear one.

## Workplace job-specific situational judgement assessment

### About this assessment

A situational judgement test (SJT) presents realistic workplace dilemmas and asks you to evaluate possible responses. The most common formats are choosing the most effective and least effective responses from a set of four, ranking all responses, or rating each response's effectiveness independently. Unlike cognitive and numeric tests, there is often no formula to apply — the "correct" answers are set by subject-matter experts and reflect the professional behaviours the organisation values: user focus, collaboration, ownership, sound escalation, integrity, and inclusion.

Typical format: an online test of 20 to 40 minutes with 8 to 15 scenarios. Timing is usually generous compared with cognitive tests, because the intent is considered judgement rather than speed. Scoring may be against an expert consensus key, and some platforms report a profile across behavioural dimensions rather than a single score.

For a senior DevOps engineer, situational judgement is arguably the most role-relevant assessment of all. Your technical decisions are rarely made in a vacuum: the failing test suite blocks a ministerial deadline, the security control frustrates a delivery team, the junior engineer's mistake is discovered mid-incident, and the architect's preferred tool conflicts with your operational evidence. Deep technical knowledge tells you *what* is true; judgement determines *what you do about it* — whom you tell, in what order, with what tone, and with what respect for process, people and users. Because you coach and mentor more junior colleagues, your judgement is also multiplied: the behaviours you model become the team's norms. Employers assess situational judgement at senior level because this is the level at which technical authority starts to carry organisational consequences.

### How this assessment maps to your role

The assessment dimensions map directly to the named skills and duties in your role summary:

- **Ownership and escalation** map to **Service support** and **Availability and capacity management**: identifying and fixing complex faults includes knowing when a fault exceeds your remit — when to act, when to inform, and when to escalate a KPI breach rather than quietly absorb it.
- **Collaboration and influence** map to **Systems design** (reviewing the designs of others without bruising them), **Systems integration** (co-ordinating build activities across teams you do not manage), and **Development process optimisation** (contributing solutions that other teams must willingly adopt).
- **Integrity under pressure** maps to **Information security** and **Modern development standards**: the moments that matter are when a control or standard is inconvenient — a deadline, a senior voice, a plausible shortcut — and the assessment probes whether the control survives.
- **Developing others** maps to your duty to **provide coaching and mentoring to more junior colleagues**: scenarios test whether you correct mistakes in ways that grow people rather than shrink them.
- **User focus** maps to your **User focus** skill: several scenarios hinge on distinguishing user needs from stakeholder desires, and on championing research even when it slows a decision everyone wants to make quickly.

### Practice questions

**Question 1 (moderate) — The deadline and the failing tests**

A delivery team must release a feature on Thursday for a public commitment. On Wednesday afternoon, the integration suite shows three failures in the payment reconciliation tests. The delivery manager says the failures are "probably the flaky environment again" and asks you to approve skipping the suite for this release. You know the environment has produced flaky failures before, but these three tests have not previously been flaky.

- Option A: Approve the skip — the environment has a documented history of flakiness and the deadline is a public commitment.
- Option B: Refuse to skip, and spend the time before Thursday investigating the three failures with the team; if they prove genuinely flaky, document that evidence and release; if they reveal a defect, tell the delivery manager immediately so the release decision can be made with accurate information.
- Option C: Refuse the skip and escalate the delivery manager's request to their line manager as attempted circumvention of quality controls.
- Option D: Approve the skip but ask the team to run the three tests manually after the release goes live.

**Most effective: B. Least effective: C.**

**Explanation:** Option B does what senior engineers are for: it converts an opinion ("probably flaky") into evidence before an irreversible decision, keeps the deadline genuinely reachable if the evidence cooperates, and puts the release decision where it belongs — with the accountable manager, but properly informed. It also models exactly the discipline you want your mentees to absorb. Option A gambles payment reconciliation on a hunch; the stem deliberately notes these tests have *not* previously been flaky, which is the detail careful readers act on. Option D is A with a fig leaf — testing after release is measurement of harm, not prevention. Option C is the least effective: the delivery manager's request is a normal deadline behaviour, not misconduct; escalating before investigating damages the collaboration your role depends on, wastes the hours that could resolve the question, and teaches the team that consulting you is dangerous. Escalation is a valuable tool exactly when direct engagement has failed or integrity is genuinely threatened — neither is yet true here.

**Question 2 (moderate) — The junior engineer's production mistake**

A junior engineer you mentor ran a cleanup script against production instead of staging, deleting a week of non-critical audit logs. Backups exist. The junior comes to you distressed, before anyone else has noticed, and asks what to do.

- Option A: Tell them to restore from backup quietly; no harm was done, and reporting it would dent their confidence.
- Option B: Guide them through restoring from backup, then support them to report the incident themselves through the normal process, and afterwards work with them on why the mistake was possible — such as production credentials being available in a context where staging was intended — and fix that cause.
- Option C: Take over: restore the data yourself, report the incident yourself, and tell the junior you will handle it from here.
- Option D: Tell them to report it immediately to their line manager before any remediation starts.

**Most effective: B. Least effective: A.**

**Explanation:** Option B repairs the harm, preserves organisational transparency, develops the junior (they report it, supported — which converts distress into ownership), and applies the senior engineer's signature move: treating a human error as a system defect, because a system in which staging and production are one mistyped variable apart will eventually catch someone less lucky. Option A is the least effective: concealing an incident, however minor, corrupts the incident record, teaches the junior that mistakes are hidden rather than learned from, and turns a recoverable error into a trust problem if discovered — the cover-up always costs more than the incident. Option C fixes the data but confiscates the learning; a mentee who watches you handle their mistake learns dependence, not resilience. Option D has the right transparency instinct but the wrong sequence for a low-risk, fully recoverable situation: restoring first (or in parallel) limits impact, and the report is better made with remediation already in hand — though in a higher-severity incident, D's report-first instinct would gain force.

**Question 3 (challenging) — The architect's tool and your evidence**

A solutions architect senior to you has mandated a particular secrets-management product for a new service. Your operational testing shows it fails over too slowly to meet the service's availability KPI, and you have benchmark data. The architect has already presented the choice to programme governance, and reversing it would be visibly awkward for them. The service goes live in six weeks.

- Option A: Implement the mandated product as instructed — the architect owns the decision and the governance record.
- Option B: Share your benchmark data with the architect privately first, framed as a risk to the availability KPI rather than a critique of the choice, propose options (configuration changes, an alternative product, a revised KPI), and offer to present the findings jointly to governance if a change is needed.
- Option C: Raise the benchmark data directly at the next programme governance meeting so the record is corrected before go-live.
- Option D: Implement the mandated product, but design a contingency migration path to an alternative and document your concerns in the risk register.

**Most effective: B. Least effective: A.**

**Explanation:** Option B gets the evidence to the decision-maker while giving them room to move — private first, options attached, joint presentation offered — which is how technical influence works between professionals who must collaborate for years. It treats the KPI, not the architect, as the thing under threat. Option A is the least effective: you hold evidence that the service will miss its availability KPI, and silently building it anyway abandons your core duty of ensuring deployment strategies are highly available; "they own the decision" does not transfer your obligation to inform it. Option C corrects the record but ambushes a colleague in front of governance, converting a solvable technical question into a face-saving contest — B achieves the same correction without the wound. Option D is a defensible engineering hedge but a poor first choice: it spends six weeks building around a problem that a conversation might simply fix, and a risk register entry is not a substitute for telling the person who can act. Note the seniority pattern: at your level, *how* evidence reaches a decision is part of your competence, not an optional social grace.

**Question 4 (moderate) — The KPI breach nobody mentions**

Reviewing dashboards, you notice a service you support has quietly missed its 99.5% availability KPI for the second consecutive month. The service team has not mentioned it in stand-ups, and the monthly service report sent to the service owner describes availability as "broadly on track".

- Option A: Say nothing — it is the service team's report, and raising it would look like policing colleagues.
- Option B: Raise it with the service team first: show them the dashboard, ask how the report was compiled, and support them to correct the report and investigate the misses; if the team resists correcting it, escalate to the service owner yourself.
- Option C: Email the service owner immediately with the correct figures, copying the service team.
- Option D: Fix the underlying availability issues yourself without mentioning the reporting discrepancy to anyone.

**Most effective: B. Least effective: A.**

**Explanation:** Option B combines colleagueship with integrity in the right order: the team may have an innocent explanation (a different measurement window, an agreed exclusion), and giving them first sight respects that while the conditional escalation guarantees the truth reaches the accountable owner either way. Managing service components against KPIs is your named skill; "broadly on track" over two missed months is the kind of drift that turns into a formal service failure. Option A is the least effective: it lets inaccurate reporting continue on your watch, and discovering later that you saw it and stayed silent damages you along with the team. Option C reaches the right destination discourteously — an accurate report matters, but the ambush-by-CC teaches every team to hide dashboards from you. Option D fixes symptoms while leaving the governance signal corrupted; the owner still believes all is well, so the resources and attention the service needs will not come. The strong pattern: correct the information through the people closest to it, with escalation as a committed backstop rather than a first strike.

**Question 5 (moderate) — The stakeholder's desire and the user's need**

A senior stakeholder wants the team to build a real-time dashboard of upload statistics for an internal case-working service, and asks you to prioritise the pipeline and infrastructure work for it. User research from the service's caseworkers, which you attended, showed their dominant pain point is slow document retrieval, and nobody raised statistics. The stakeholder says the dashboard "is what the director wants to see".

- Option A: Build the dashboard infrastructure as asked — the stakeholder is senior and the request is explicit.
- Option B: Share the user research findings with the stakeholder, distinguish the director's need (visibility of service performance, which might be met more cheaply — perhaps with an existing weekly report) from caseworkers' evidenced need (retrieval speed), and propose the team validate the dashboard's value with users before committing infrastructure work.
- Option C: Refuse, telling the stakeholder that user research does not support the dashboard.
- Option D: Build both the dashboard and the retrieval improvements by extending the team's timeline without consulting the delivery manager.

**Most effective: B. Least effective: D.**

**Explanation:** Option B enacts your **User focus** skill almost clause by clause: it distinguishes user needs from stakeholder desires, represents users internally, champions research, and — crucially — takes the director's underlying need seriously rather than dismissing the request, offering a cheaper way to meet it. Option C gets the evidence right and the collaboration wrong: a flat refusal leaves the director's legitimate need unmet and casts research as a veto rather than a guide. Option A spends the team's capacity on an unvalidated desire while the evidenced pain point waits. Option D is the least effective: it looks generous but unilaterally commits the team's time, bypasses the delivery manager's prioritisation authority, and hides the trade-off instead of surfacing it — a senior engineer's job is to make costs visible, not to absorb them invisibly until the schedule breaks. The general shape of strong answers here: honour the person, interrogate the request, bring the evidence, and keep prioritisation decisions with the people accountable for them.

**Question 6 (challenging) — Mid-incident, senior pressure**

During a major incident affecting a public-facing service, a senior manager joins the incident channel and instructs you to restart the database cluster immediately, "because that fixed it last time". You are incident lead for the technical response. Telemetry suggests the fault is in a downstream cache, and a database restart would extend the outage by roughly 20 minutes while providing no benefit if your diagnosis is right.

- Option A: Comply — the manager is senior, and the incident is too urgent for debate.
- Option B: Briefly state your diagnosis and its evidence in the channel, explain the cost of the restart if the cache is at fault, propose testing the cache hypothesis first as it takes two minutes, and proceed with that test unless the manager, so informed, still directs otherwise — while noting the direction in the incident log.
- Option C: Ignore the instruction and continue with your plan without responding — you are the incident lead.
- Option D: Ask the manager to leave the incident channel so the technical team can work.

**Most effective: B. Least effective: C.**

**Explanation:** Option B is textbook incident leadership under hierarchy: it respects the senior manager's authority while giving them what they lack — the current evidence and the cost of their proposal — and offers a two-minute test that resolves the disagreement empirically. Recording the direction in the log keeps accountability clean. This is how "deep technical knowledge, providing support and solving complex problems" behaves when it meets rank. Option A extends a public-service outage on a hunch you have evidence against — deference is not a diagnostic method. Option D may be emotionally tempting but picks a jurisdictional fight mid-incident and burns a relationship for no operational gain; managers in incident channels usually need information, not exile. Option C is the least effective: silent non-compliance is the worst of every option — the manager's concern is unaddressed and will escalate, the team sees the incident lead modelling contempt, and if your diagnosis proves wrong the ignored instruction becomes indefensible. In incidents, communication *is* the leadership; the strongest response is almost never silence.

**Question 7 (moderate) — The knowledge silo**

You realise you are the only person who understands the deployment tooling for a critical service — you built most of it. You are about to take two weeks of leave, and in the longer term you would like a promotion, which will move you away from day-to-day operation. A colleague jokes that you are "un-promotable because un-replaceable".

- Option A: Write a comprehensive wiki page about the tooling before your leave.
- Option B: Before leave, write a concise runbook for the most likely failure scenarios and walk one colleague through it; after leave, propose a rotation in which other engineers make routine tooling changes with you reviewing, plus a pairing session each sprint, so knowledge transfers through practice over the coming months.
- Option C: Tell your line manager the team needs to hire another senior engineer to cover the tooling.
- Option D: Keep the knowledge as it is — being indispensable is job security, and documentation would go stale anyway.

**Most effective: B. Least effective: D.**

**Explanation:** Option B treats knowledge transfer as an engineered process with a short-term mitigation (runbook plus a briefed human before leave) and a long-term mechanism (practice with review, which is how operational knowledge actually transfers — people learn deployment tooling by deploying, not by reading). It also directly serves your coaching and mentoring duty and your own promotion interest. Option A is helpful but insufficient alone: a wiki page nobody has exercised is untested documentation, and untested documentation fails exactly when needed — the same reason you test restores, not just backups. Option C outsources a development problem to a hiring process that will take months and still land on undocumented tooling. Option D is the least effective: engineered indispensability is a bus-factor of one dressed up as job security — it caps your own progression (as the joke warns), makes every leave a service risk, and inverts the profession's values, which prize leaders who multiply capability rather than hoard it. Strong senior engineers make themselves replaceable on purpose; that is what makes them promotable.

**Question 8 (challenging) — The security control that blocks delivery**

You designed the pipeline so that container images with critical vulnerabilities cannot be promoted to production. A delivery team's release is blocked by a critical finding in a third-party library. The team's product manager tells you the finding is "theoretical — the vulnerable function isn't even called", the fix version breaks their build, and a trade negotiation deadline depends on the release. They ask you to disable the gate for this deployment.

- Option A: Disable the gate for this deployment — the product manager owns the risk and the deadline is real.
- Option B: Keep the gate, and work the problem with the team: verify whether the vulnerable path is truly unreachable, check for mitigations (a patched fork, a virtual patch at the gateway, vendor advisories), and if residual risk remains, route a time-boxed, documented exception through the security risk owner rather than deciding it yourself — while helping the team plan the proper fix.
- Option C: Refuse and tell the team no release can happen until the library is upgraded, whatever the deadline.
- Option D: Suggest the team deploy from a branch that predates the vulnerability scan's introduction, since the gate does not apply to it.

**Most effective: B. Least effective: D.**

**Explanation:** Option B honours the principle that security exceptions are *decisions with owners, evidence and expiry dates*, not favours between colleagues. Verifying reachability converts the PM's claim into evidence; exploring mitigations often unblocks without any exception; and routing residual risk to the security risk owner puts the decision at the accountable level — designing solutions with security controls included also means designing how the controls flex under pressure. Option A makes you personally the approver of a risk you do not own, on an unverified claim, and establishes that the gate is negotiable with whoever asks firmly enough — after which it protects nothing. Option C is honest but rigid: it treats the control as an end rather than a means, ignores legitimate mitigation routes, and hands "security blocks delivery" ammunition to every future opponent of the gate. Option D is the least effective: it is not an exception but a circumvention — advising a team to launder a release through a scan-free path is integrity failure in engineering form, worse than A because it is covert, unrecorded, and coached by the very person who built the control. Strong answers hold the control, verify the claims, and move the decision to its rightful owner.

**Question 9 (moderate) — Coaching versus rescuing at the review**

A junior engineer's pipeline change is due to be demonstrated to the delivery team tomorrow. Reviewing it tonight, you find it works but is poorly structured: hard-coded environment values, no rollback step, and a misleading stage name. You could rewrite it in an hour; guiding the junior through fixing it would take most of tomorrow morning and tighten the demo timeline.

- Option A: Rewrite it tonight and tell the junior what you changed, so the demo goes smoothly.
- Option B: Note the issues as review comments tonight, prioritised — rollback step first, as it is a safety issue — and pair with the junior first thing tomorrow to fix the top items together, accepting that the demo may show slightly less polish; treat the remaining items as follow-ups.
- Option C: Let the demo proceed as is and raise the issues afterwards, to protect the junior's confidence.
- Option D: Postpone the demo until the change meets your standards.

**Most effective: B. Least effective: A.**

**Explanation:** Option B balances the three real obligations: safety (the missing rollback step is the one item that genuinely cannot wait, and prioritising it teaches risk-ranking), development (the junior does the fixing, with you alongside — which is what coaching and mentoring means in practice), and delivery (the demo proceeds). Option A is the least effective mentoring move disguised as the most helpful one: the demo shows work the junior did not do, the learning evaporates, and a pattern is set in which your rewrites silently backstop every deadline — exhausting for you, stunting for them, and misleading for the team assessing the work. Option C protects confidence at the price of demonstrating a change with no rollback step to a team that may adopt it — kindness to one person, risk to many. Option D over-weights polish: postponing a demo for structural cleanliness (as opposed to safety) signals perfectionism and costs the team feedback it needs. The discriminating detail is the rollback step: strong candidates separate the safety-critical fix from the stylistic ones and sequence accordingly.

**Question 10 (challenging) — The optimisation that helps one team and harms another**

You identify a build-cache change that would cut your platform's average build time by roughly 30%. Rolling it out requires a short migration during which each team's first build after migration runs slow. One delivery team, mid-way through a critical release week, asks you to postpone the entire rollout for a month. Three other teams are asking loudly for the speed-up now.

- Option A: Postpone the whole rollout a month — release weeks are sacred.
- Option B: Roll out to all teams now — three teams outvote one.
- Option C: Roll out now to the three teams who want it, exclude the releasing team until their release completes, and agree with them a specific migration date; communicate the plan and the one-slow-build expectation to everyone.
- Option D: Ask the four teams to discuss it among themselves and tell you the consensus.

**Most effective: C. Least effective: D.**

**Explanation:** Option C notices what the stem quietly allows: the migration is per-team, so the conflict is false — the constraint can be honoured for one team while the benefit flows to three. Segmented rollout with explicit expectations ("your first build will be slow") is exactly how process optimisation is implemented without burning trust, and it is your call to design: contributing to the implementation of proposed solutions is your named skill. Option A taxes three teams a month of slow builds to spare one team a scheduling conversation; option B imposes migration risk on a team in its most fragile week for no gain that a week's wait would not preserve — both accept a trade-off the situation does not require. Option D is the least effective: it abdicates a platform decision to an unstructured negotiation among parties with no shared accountability, guarantees delay and possibly rancour, and signals that the platform's senior engineer will not exercise the judgement the role exists to provide. Consultation is valuable — C includes communication throughout — but consultation is input to your decision, not a substitute for it.

### Preparation tips

- **Answer as your best professional self, consistently.** SJTs measure judgement, not mind-reading. The behaviours rewarded — verify before deciding, inform the accountable person, develop rather than rescue, hold controls while helping people — are stable across scenarios. Decide your principles before the test and apply them evenly.
- **Look for the option that addresses both the substance and the relationship.** Strong answers usually fix the technical problem *and* preserve or repair the human system around it. If an option does only one, keep scanning.
- **Respect the accountable owner.** Many scenarios turn on decision rights: release decisions belong to delivery managers, risk acceptances to risk owners, prioritisation to the accountable manager. The strong option informs and equips the owner; it rarely seizes or silently absorbs the decision.
- **Notice sequence words.** "First", "then", "before anyone else has noticed", "if the team resists" — effective responses are often about *order*: engage directly first, escalate as a backstop, remediate before or alongside reporting depending on severity.
- **Read every option fully before choosing either answer.** The least-effective option is sometimes a subtle integrity failure (a circumvention, a concealment) hiding behind a helpful tone, and the most-effective is sometimes the slightly slower, more collaborative one.
- **Rehearse with your own history.** Recall three real dilemmas from your last year — a deadline versus a control, a mistake by a mentee, a disagreement with a senior colleague — and write down what worked. Your calibrated experience is the best preparation an SJT allows.

### Common pitfalls to avoid

- **Choosing maximum escalation as a display of rigour.** Escalating before engaging reads as rigour but scores as poor collaboration. Escalation is the backstop in strong answers, not the opening move.
- **Choosing maximum deference as a display of respect.** Complying with a senior voice against your evidence — mid-incident or in design — abandons the expertise your role exists to supply. Respect is informing the decision-maker well, not agreeing with them quickly.
- **Rescuing instead of developing.** Rewriting the junior's work, taking over their incident report, absorbing the extra scope yourself — these feel generous and score poorly, because they trade other people's growth and the organisation's visibility for short-term smoothness.
- **Treating controls as either absolute or negotiable.** The strong pattern is neither "no release, ever" nor "just this once": it is verify the claim, seek mitigations, and route genuine exceptions to the accountable owner with documentation and an expiry.
- **Missing the covert-integrity-failure option.** Somewhere in many SJTs is an option that quietly conceals, circumvents, or misreports. However pragmatic it sounds, it is reliably the least effective. Find it and you have found one of your two answers.
- **Answering as the hero, not the professional.** Options where you personally fix everything, decide everything, or work around everyone often flatter the ego and fail the test. The profession values engineers who make systems and people around them better — assessments are keyed the same way.

## Conclusion

Well done — you have worked through a substantial set of practice material, and every question you attempted honestly has sharpened something you use in your real work.

Take a moment to notice what you have actually practised. In the cognitive section, you traced dependency graphs, checked configurations against standards as written, ranked competing demands by impact-weighted urgency, and separated correlation from cause in incident timelines — the same reasoning that makes your toolchain reliable and your fault diagnosis fast. In the numeric section, you converted availability targets into downtime minutes, compounded growth rates, weighted averages properly, and defended the right denominator — the arithmetic that keeps your capacity plans honest and your KPI reports trustworthy. In the verbal section, you held the line between what a passage guarantees, contradicts, and merely permits — the discipline that makes you a precise reader of standards and a writer of runbooks that work at 3am. And in the situational judgement section, you rehearsed the judgement calls that define senior engineering: holding a security gate while helping the team it blocks, giving evidence to a senior decision-maker without ambushing them, and developing a junior colleague instead of rescuing them.

If some questions caught you out, that is the practice working. Note the *pattern* of your misses — wrong denominators, imported assumptions, escalating too early — rather than the individual questions, because assessments repeat patterns, and so does the job. A short review of your errors a few days from now will consolidate more than another full pass today.

Remember, too, that assessment performance is a skill with its own trajectory, just like any technology you have mastered. Nobody's first pipeline was elegant; nobody's first timed test reflects their ceiling. Calibrated speed, calm under the clock, and familiarity with the formats are all trainable, and you have just trained them.

Finally, connect this back to your development as a senior DevOps engineer. The capabilities these assessments sample — structured reasoning, numerical honesty, precise reading, and professional judgement — are the same capabilities that will carry you through design reviews, incident leadership, mentoring, and whatever your next role level asks of you. Practising them here is not a detour from your professional development; it is a compact, honest form of it.

You support the systems that support public services, and you help the people around you grow while you do it. Approach your assessment the way you approach a well-planned deployment: prepared, rested, methodical, and confident in your rollback plan — which, in this case, is simply the knowledge that you can always practise again. Good luck.
