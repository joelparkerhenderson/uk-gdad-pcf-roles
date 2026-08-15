# Senior DevOps Engineer (Management) - Psychometric Assessment Resources

## Introduction

Welcome! This guide has been created especially for you as a senior DevOps engineer on the management track within the UK Government Digital and Data profession. Whether you are preparing for an internal assessment, applying for a new post, benchmarking your own capability, or simply curious about how psychometric assessments relate to your day-to-day work, this document will help you practise, reflect, and build confidence.

Psychometric assessments are structured, standardised exercises that measure the mental capabilities and behavioural tendencies that predict success in a role. For a senior DevOps engineer with management responsibilities, that means far more than abstract puzzles. The assessments described here are job-specific: they use the kinds of artefacts you genuinely handle — pipeline configurations, deployment strategies, capacity dashboards, incident reports, security control designs, and sprint plans for large groups of stories — and the kinds of decisions you genuinely make, such as transforming technical requirements into an effective DevOps toolchain, ensuring deployment strategies are repeatable, scalable and highly available, and coaching and mentoring more junior colleagues while still solving complex technical problems yourself.

Why do these assessments matter for your role in particular? At senior level on the management track, you sit at the meeting point of deep technical delivery and people leadership. You plan and design large groups of stories, you provide support to delivery teams when they hit problems they cannot solve alone, and you develop the engineers around you. Assessments of cognitive ability, numerical reasoning, verbal reasoning, and situational judgement map directly onto those demands. Practising them sharpens exactly the skills your role depends on: spotting a logical flaw in a deployment sequence before it reaches production, interpreting a capacity trend table under time pressure, extracting precise meaning from a security policy or an incident report, and choosing the most effective course of action when a release deadline collides with a junior engineer's development needs.

This document is organised into four main assessment sections, each following the same pattern: an overview of what the assessment measures and why it matters for your role, a mapping of the assessment dimensions to the specific skills in the senior DevOps engineer capability framework, a substantial set of practice questions with full worked explanations, practical preparation tips, and common pitfalls to avoid.

Here is how to get the most from it. First, read each "About this assessment" section so you understand the format and timing you are likely to face. Second, attempt the practice questions honestly — write down your answer before reading the explanation, and note how long each one takes you. Third, treat every explanation as a mini-lesson: even when you answer correctly, the reasoning walkthrough will deepen your technique, and many explanations show how the same thinking pattern appears in your real work on toolchains, environments and teams. Finally, use the preparation tips and pitfalls for self-reflection: they connect assessment performance back to your professional development as an engineer who both delivers and leads.

Take your time, be kind to yourself, and enjoy the practice. Let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive ability assessment measures the exact mental processes your role demands, using practical workplace scenarios rather than abstract puzzles. Unlike a generic intelligence test, it presents you with the everyday materials of your job — in your case, CI/CD pipeline definitions, infrastructure-as-code templates, deployment runbooks, monitoring dashboards, environment naming schemes, and dependency maps — and asks you to reason quickly and accurately about them.

Typical format: an online, timed test lasting 15 to 30 minutes, with questions covering pattern recognition, logical deduction, error checking, prioritisation, and applied problem solving. Scoring is objective, comparing your responses against a norm group, and modern platforms often adapt question difficulty based on your previous answers: answer correctly and the next question gets harder, so do not be discouraged if the test feels increasingly demanding — that usually means you are doing well. Employers usually receive a breakdown of speed versus accuracy rather than a single score, so working both quickly and carefully matters. You will normally be offered short, ungraded practice questions before the real test begins, so you can get comfortable with the interface without pressure.

For a senior DevOps engineer, cognitive ability assessment is particularly relevant because your core professional value is structured thinking applied to complex, interconnected systems. You deliver and integrate software to form a complete DevOps toolchain, and that requires holding many moving parts in mind at once: which pipeline stages depend on which artefacts, which environments differ and why, where a proposed deployment strategy contradicts an availability requirement, and what follows logically when one element of the toolchain changes. On the management track you add a second layer: reasoning about people, priorities and coaching commitments alongside the technology. A well-designed cognitive assessment simulates precisely those demands in miniature.

### How this assessment maps to your role

The assessment dimensions map directly to the skills in your capability framework:

- **Pattern recognition** maps to your **Development process optimisation** skill: analysing current processes and identifying opportunities to optimise them means recognising recurring structures — duplicated pipeline stages, common failure signatures, repeated bottlenecks — across large and messy telemetry and configuration sets.
- **Logical deduction** maps to **Systems design** and **Systems integration**: designing systems of medium risk and complexity, defining the integration build, and co-ordinating build activities across systems all require you to reason validly from standards, dependency rules and constraints to their consequences.
- **Error checking** maps to **Modern development standards** and **Programming and build (software engineering)**: applying modern development standards and supporting others in applying them means spotting inconsistencies between artefacts — a pipeline that skips a mandated scan, a script that contradicts the agreed specification, a template that breaks the naming convention.
- **Prioritisation** maps to **Availability and capacity management** and **Service support**: identifying capacity issues, initiating remedial action, and identifying, locating and fixing service faults all depend on rapidly ranking what matters most when several things demand attention at once — a skill made harder, and more important, by your coaching and mentoring duties.
- **Problem solving** maps to **Information security** and your duty to provide deep technical support to delivery teams: teams bring you tangled build, deployment and security problems, and you must decompose them, form hypotheses, and recommend the change that fixes the cause rather than the symptom.

### Practice questions

**Question 1 (easy) — Pattern recognition in environment naming**

Your toolchain standard requires every environment to be named using the pattern `<service>-<environment>-<region>`, where environment is one of `dev`, `test`, `stg`, or `prod`, and region is a two-letter code. While reviewing environments created by a junior engineer, you see:

1. `payments-dev-ln`
2. `payments-stg-ln`
3. `payments-ln-prod`
4. `payments-test-mc`
5. `payments-prod-mc`

Which entry breaks the naming pattern?

- A) Entry 2
- B) Entry 3
- C) Entry 4
- D) Entry 5

**Correct answer: B**

**Explanation:** The pattern fixes the order: service first, then environment, then region. Entry 3 swaps the last two segments — `ln` (a region code) appears in the environment position and `prod` in the region position. Entries 1, 2, 4 and 5 all follow the rule. This looks trivial, but broken naming conventions are exactly what breaks automation: scripts that parse environment names, monitoring rules that route alerts by environment, and cost reports that group by region all silently misbehave when one entry inverts the pattern. When you support others in applying modern development standards, catching this in review — and explaining why it matters rather than just fixing it — is the coaching moment that stops it recurring.

**Question 2 (easy) — Logical deduction from a deployment policy**

Your deployment policy states: "Every deployment to production must pass the automated security scan, unless an emergency change has been formally approved by the service owner." A delivery team tells you: "Our release went to production this morning and did not pass the automated security scan." Which one of the following conclusions must be true?

- A) The team has breached the deployment policy.
- B) The service owner formally approved an emergency change.
- C) Either the service owner approved an emergency change, or the policy has been breached.
- D) The security scan tooling was unavailable this morning.

**Correct answer: C**

**Explanation:** The policy is a conditional rule with one permitted exception. From the facts given you cannot tell whether an emergency approval exists, so neither A nor B must be true on its own — each is merely possible. D introduces information not present at all. The only conclusion guaranteed in every case consistent with the facts is the disjunction in C. Assessments reward this discipline: deduce only what the given information guarantees. In your role the same discipline stops you accusing a team of bypassing controls before checking the change record — which protects your working relationships as well as your logic, and models exactly the fair-minded behaviour you want the engineers you mentor to copy.

**Question 3 (easy) — Error checking a pipeline stage order**

Your standard pipeline for a containerised service runs stages in this order: (1) lint, (2) unit tests, (3) build image, (4) scan image for vulnerabilities, (5) push image to registry, (6) deploy to staging, (7) integration tests, (8) deploy to production. A junior engineer proposes this order for a new service: lint, unit tests, build image, push image to registry, scan image for vulnerabilities, deploy to staging, integration tests, deploy to production. What is the most important problem with the proposal?

- A) Integration tests should run before deploying to staging.
- B) The image is pushed to the registry before it has been scanned, so an image with known vulnerabilities becomes available for deployment.
- C) Lint should run after unit tests.
- D) There is no problem; the order is equivalent.

**Correct answer: B**

**Explanation:** The proposal swaps stages 4 and 5. Pushing before scanning means a vulnerable image sits in the registry where any environment — or any other team consuming your registry — could pull and deploy it before the scan result arrives; the scan stops being a gate and becomes a report. Option A is wrong because integration tests need a deployed environment to test against. Option C is a stylistic non-issue. The habit being tested is reading an ordered process and asking, for each step, "what does this step assume has already happened, and what does it make possible?" That is the same reasoning you apply when you define the integration build and ensure security controls are engineered in rather than bolted on.

**Question 4 (moderate) — Prioritisation across delivery and people duties**

It is Monday morning. Four items compete for your attention:

1. A production payments service is degrading — error rates have doubled in the last hour and the on-call engineer has asked for your help diagnosing it.
2. The release train for another service closes at 15:00 today, and your review of the deployment plan is the last remaining gate.
3. A junior engineer you mentor has asked for feedback on their first infrastructure-as-code module, due to be demonstrated to the team on Thursday.
4. Your capacity forecast for the next quarter is due to the head of engineering at the end of the week.

Which sequencing is most defensible?

- A) 1, 2, 3, 4 — live degradation first, then the same-day gate, then coaching, then the forecast
- B) 2, 1, 3, 4 — deadlines always beat incidents
- C) 3, 1, 2, 4 — developing others always comes first
- D) 1, 4, 2, 3 — do the two pieces of analysis first

**Correct answer: A**

**Explanation:** Prioritisation questions test reasoning about impact and urgency together. Item 1 is both urgent and high impact: a degrading production service affects users now, and a colleague has explicitly asked for your deep technical support — the core of your service support duty. Item 2 has a hard same-day deadline and blocks another team's delivery, so it comes next. Item 3 matters — coaching and mentoring is part of your role, not an optional extra — but Thursday allows it to follow. Item 4 is important, routine, and due Friday. Option B ignores live user harm for an internal deadline; C treats mentoring as trumping an active incident, which no junior engineer would thank you for; D leaves both time-critical items waiting. Note the pattern: the strongest answer sequences by impact-weighted urgency, not by any single dimension such as seniority, deadline order, or personal preference.

**Question 5 (moderate) — Pattern recognition in monitoring data**

Four comparable microservices behind the same gateway report the following proportion of requests slower than one second over the past week: Service A 2%, Service B 3%, Service C 14%, Service D 2%. All four run the same instance size, similar traffic volumes and the same deployment baseline. As the senior engineer supporting these teams, what is the most reasonable first interpretation of Service C's figure?

- A) Service C's team is underperforming and should be told to fix their latency immediately.
- B) The figure is an outlier that warrants investigation — it may reflect a measurement difference, a workload difference, or a genuine performance problem.
- C) Services A, B and D are over-provisioned and should be scaled down to match C.
- D) The figures cannot be compared because every service is different.

**Correct answer: B**

**Explanation:** Recognising an outlier is pattern recognition; deciding what it means requires restraint. Three comparable services cluster at 2-3% and one sits at 14% — roughly five times the cluster. But an outlier is a prompt for inquiry, not a conclusion. Innocent explanations include a different measurement point (Service C may measure at the client rather than the server), a workload difference (perhaps C handles large file uploads), or a recent dependency change. Options A and C leap to action without evidence — and A, on the management track, would also damage trust with a team you are meant to support. Option D wrongly abandons comparison despite the stem stating the services are comparable. Identifying capacity and performance issues only leads to the right remedial action if you first validate that you are comparing like with like.

**Question 6 (moderate) — Logical deduction about release sequencing**

A cutover plan contains these dependency rules: (i) the new database schema must be migrated before the new application version can be deployed; (ii) the schema migration cannot start until the nightly backup completes; (iii) the traffic switch to the new version must happen in the same maintenance window as the application deployment or the window immediately after it. The nightly backup completes at 02:00. The schema migration takes one full maintenance window, and maintenance windows run 02:00–04:00 each night. What is the earliest window in which the traffic switch may occur?

- A) Tonight's window (the one starting at 02:00 immediately after the backup)
- B) The second window
- C) The third window
- D) The fourth window

**Correct answer: B**

**Explanation:** Work forwards through the dependencies. The backup completes at 02:00, so the migration can occupy tonight's window (window 1) and completes at 04:00. The application deployment therefore cannot happen before window 2. The traffic switch must fall in the deployment window (window 2) or the one immediately after it (window 3). The earliest permissible window for the switch is therefore window 2. A tempting error is window 3, by assuming the switch must follow the deployment window rather than share it; another is window 1, by forgetting the migration consumes a full window. Dependency reasoning of exactly this kind underpins your duty to make deployment strategies repeatable: a runbook that sequences steps incorrectly is not a strategy, it is an outage waiting for a date.

**Question 7 (moderate) — Error checking infrastructure code against standards**

Your platform standards state: (i) all storage buckets must have encryption at rest enabled; (ii) all production resources must carry a `cost-centre` tag; (iii) no security group may allow unrestricted inbound access on port 22. You review a template that defines: a production bucket with encryption enabled and a `cost-centre` tag; a staging bucket with encryption disabled and no tags; a production security group allowing inbound port 22 from the corporate address range only. How many of the three standards are breached?

- A) 0
- B) 1
- C) 2
- D) 3

**Correct answer: B**

**Explanation:** Check each rule against each resource, carefully separating what the standard covers from what it does not. Rule (i) applies to all buckets: the staging bucket has encryption disabled, so rule (i) is breached. Rule (ii) applies only to production resources: the production bucket is tagged, and the untagged staging bucket is out of scope, so rule (ii) is not breached. Rule (iii) forbids unrestricted access on port 22: the security group restricts access to the corporate range, so it is compliant. Exactly one standard is breached. The trap is over-flagging — counting the staging bucket's missing tag as a second breach even though the standard only covers production. In real reviews the same discipline matters in both directions: teams lose confidence in a reviewer who flags non-issues just as quickly as in one who misses real ones.

**Question 8 (moderate) — Applied problem solving on a flaky pipeline**

A delivery team reports that their integration test stage fails roughly one run in five, and re-running without any code change usually passes. You gather these facts: failures occur across many different tests rather than one; failures are more common during the mid-morning peak; the test environment shares a database with another team's load-testing activity; unit tests never show the same behaviour. Which hypothesis best fits all the evidence?

- A) The application code has a functional bug that the tests correctly detect.
- B) Contention on the shared test database causes intermittent timeouts under load.
- C) The test framework version is incompatible with the language runtime.
- D) The engineers are writing poor-quality tests.

**Correct answer: B**

**Explanation:** Test each hypothesis against every fact. A functional bug (A) would fail the same tests consistently, not a shifting set that passes on re-run. A framework incompatibility (C) would affect all runs regardless of time of day, and would likely affect unit tests too. Blaming test quality (D) explains flakiness in general but not the mid-morning pattern or the correlation with a shared, load-tested database. Hypothesis B explains everything: shared-resource contention produces intermittent, timing-dependent failures spread across many tests, worse at peak, absent from unit tests that do not touch the database. The technique — insist that the chosen explanation accounts for all the evidence, not just some of it — is the heart of fault diagnosis in your service support skill, and it is also what you should be teaching juniors to do instead of clicking "re-run" and hoping.

**Question 9 (challenging) — Multi-constraint scheduling of a toolchain migration**

You must schedule three activities — the artefact repository migration (M), the pipeline cutover (P), and the team training session (T) — across five working days, Monday to Friday, at most one activity per day. Constraints: (i) M must precede P, because the new pipelines pull from the new repository; (ii) the platform vendor's support engineer is available only Monday and Thursday, and must attend M; (iii) after M, two full working days are needed to replicate artefacts before P can run; (iv) T must be on the day immediately after P, so training uses the live setup. On which day must P take place?

- A) Tuesday
- B) Wednesday
- C) Thursday
- D) Friday

**Correct answer: C**

**Explanation:** Try each option for M. If M is Thursday, the two replication days push P to the following week and T later still — impossible within the week. So M must be Monday. Two full working days of replication (Tuesday and Wednesday) mean P can run no earlier than Thursday. If P is Thursday, T falls on Friday, satisfying every constraint. If P were Friday, T would fall outside the week. Therefore P must be Thursday. The method — anchor the most constrained element first (the vendor-dependent M), then propagate the consequences — is how you plan and design large groups of stories in real life: find the hardest constraint, place it, and let everything else arrange itself around it rather than the other way round.

**Question 10 (challenging) — Deduction across a dependency map**

Your dependency records show: services Alpha and Beta both call the authentication library directly; service Gamma calls Beta but never calls the authentication library directly; service Delta calls neither the library nor any of the other three services. A critical vulnerability is announced in the authentication library. Which services could be affected and therefore need assessment?

- A) Alpha and Beta only
- B) Alpha, Beta and Gamma
- C) Alpha, Beta, Gamma and Delta
- D) Beta and Gamma only

**Correct answer: B**

**Explanation:** Alpha and Beta are directly exposed. Gamma does not use the library itself, but it depends on Beta, and a vulnerability in Beta's authentication layer can propagate to consumers of Beta — for example if Beta's compromised sessions or responses are trusted by Gamma. So Gamma needs assessment even though a naive direct-dependency search would miss it. Delta has no path to the library, direct or transitive, so it is out of scope; including it (option C) wastes scarce assessment effort during an incident. The reasoning skill is transitive closure: follow dependency edges until they stop, then stop. This is precisely how you co-ordinate build activities across systems and how you scope the blast radius when designing solutions with security controls included — both the missed transitive dependency and the over-broad "assess everything" response are expensive mistakes.

**Question 11 (challenging) — Prioritising remedial capacity actions**

A capacity review shows four issues: (1) the build agent pool hits 100% utilisation for two hours every morning, queueing all teams' pipelines; (2) a staging environment will run out of disk space in roughly three weeks at current growth; (3) a production service is at 60% of its memory limit, trending upwards by two percentage points per month; (4) the artefact repository's storage costs have risen 40% year on year. You can commission immediate remedial work on exactly one issue this sprint. Applying availability and capacity management principles, which issue should you pick?

- A) Issue 1 — it is causing harm right now to every team's delivery
- B) Issue 2 — it will cause an outage soonest
- C) Issue 3 — production always outranks non-production
- D) Issue 4 — cost growth compounds and should be stopped early

**Correct answer: A**

**Explanation:** Separate current harm from future risk, and weigh both against time available. Issue 1 is a live, daily, organisation-wide impact: every team queues for two hours each morning, which is exactly the kind of process bottleneck your development process optimisation skill exists to remove. Issue 2 is serious but three weeks away — it must be scheduled, and it comfortably can be, before the deadline. Issue 3 is a slow trend: at two points per month, months remain before it threatens the limit, so monitoring with a planned fix is proportionate. Issue 4 is a cost-efficiency matter with no availability impact — real, but not urgent. Option C's rule of thumb ("production always outranks") fails here because the production issue is the least urgent of the four once you read the trend arithmetic. The assessment habit: extract the timescale from each item before ranking, rather than ranking by category labels.

**Question 12 (challenging) — Problem decomposition under ambiguity**

A delivery team asks you to "make deployments faster". Before proposing changes you gather data and find: the pipeline takes 45 minutes end to end; 30 of those minutes are a manual approval wait; the build and test stages take 12 minutes; the deployment itself takes 3 minutes. The team's real complaint, on questioning, is that urgent fixes take half a day to reach production. Which change addresses the actual problem most directly?

- A) Parallelise the build and test stages to cut 12 minutes to 6.
- B) Optimise the deployment scripts to cut 3 minutes to 1.
- C) Work with the service owner to introduce a pre-authorised expedited path for urgent fixes, reducing the approval wait.
- D) Buy faster build agents.

**Correct answer: C**

**Explanation:** Decompose the 45 minutes: approval wait 30, build and test 12, deploy 3. Two-thirds of the elapsed time is a waiting state, not a computing state — and the stated pain ("urgent fixes take half a day") is dominated by process, not technology, since even several pipeline runs' worth of compute time cannot add up to half a day without queuing and approval delays. Options A, B and D optimise the minority of the time and would leave the complaint essentially intact; C attacks the dominant term while respecting governance by making the expedited path pre-authorised rather than uncontrolled. This is the essence of analysing current processes before optimising them: measure first, find the dominant term, and be willing to discover that the fix is a policy conversation rather than a technical task — a very common discovery on the management track.

### Preparation tips

- **Practise with your own artefacts.** Ten minutes spent reviewing a colleague's pipeline definition or infrastructure template, deliberately hunting for standard breaches and ordering errors, is directly transferable practice for error-checking questions — and it makes you a sharper reviewer at work.
- **Rehearse dependency reasoning on paper.** Take a real runbook or cutover plan and draw the dependency arrows. Questions like the scheduling and sequencing items above become mechanical once you habitually anchor the most constrained step first.
- **Time-box your practice.** Cognitive tests reward calibrated pace. Attempt questions in batches with a timer — roughly 60 to 90 seconds each — and learn what your instinct feels like when it is right versus when you are guessing.
- **Read stems twice, options once.** Most wrong answers on cognitive tests come from misreading the setup, not from faulty logic. Confirm what is actually being asked (which entry breaks the pattern? how many rows breach? what must be true?) before touching the options.
- **Use your coaching instincts.** When you explain a technique to a junior engineer, you decompose it into steps. Do the same for yourself: name the technique each question uses (transitive closure, dominant-term analysis, conditional with exception) and it becomes reusable.
- **Sleep and setup matter.** Take the real test rested, on a reliable connection, in a quiet slot in your calendar — treat it with the same environmental care you would give a production deployment.

### Common pitfalls to avoid

- **Answering from experience instead of from the stem.** You know real registries, real pipelines, real policies — but the question defines its own small world. If the stem says the services are comparable, they are. Import your expertise for technique, not for facts.
- **Concluding more than the logic allows.** "The team breached the policy" is tempting when the exception clause has not been checked. Assessments — and incident reviews — punish over-conclusion.
- **Flagging non-breaches.** In error-checking items, scope matters: a rule about production resources says nothing about staging. Over-flagging costs marks exactly as under-flagging does.
- **Ranking by category instead of by arithmetic.** "Production first", "directors first", "deadlines first" are heuristics that these questions are designed to break. Extract timescales and impacts before ordering anything.
- **Re-running instead of reasoning.** In flaky-failure questions, the pull towards "just try again" mirrors the workplace habit of clicking re-run. The assessment rewards the engineer who demands an explanation that fits all the evidence.
- **Losing marks to speed anxiety.** Adaptive tests get harder as you succeed. Interpret difficulty as progress, keep your pace steady, and never leave easy accuracy behind to chase the clock.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment measures your ability to interpret, manipulate and draw sound conclusions from numerical information of the kind your role genuinely produces. Rather than abstract arithmetic drills, it presents tables, charts and short data narratives — in your case, availability figures, pipeline duration statistics, deployment frequency trends, change failure rates, capacity utilisation curves, error budgets, and platform cost breakdowns — and asks questions that require calculation, comparison and inference.

Typical format: an online, timed test lasting 20 to 35 minutes, usually 15 to 20 questions, each based on a data table or chart. A basic on-screen calculator is normally permitted, and you should assume every question is answerable from the data given — no outside knowledge of "real" figures is required or wanted. Scoring compares accuracy and speed against a norm group. Some platforms present several questions per dataset, so time invested understanding a table pays back across multiple questions.

For a senior DevOps engineer on the management track, numeric reasoning is not a box-ticking exercise: it is the daily currency of your decisions. Availability targets are percentages; capacity headroom is a ratio; the case for optimising a process is a before-and-after comparison; the quarterly forecast you owe the head of engineering is a trend projection; and the coaching conversation about a team's flaky tests is far more persuasive when you can quantify the failure rate and its cost in lost engineer-hours. Employers assess numeric reasoning at this level because a senior engineer who misreads a utilisation table can commission the wrong remedial action, miss a looming outage, or misallocate a team's time.

### How this assessment maps to your role

The assessment dimensions map directly to the skills in your capability framework:

- **Percentages and rates** map to **Availability and capacity management**: availability targets ("three nines and a half"), utilisation percentages, growth rates and error rates are the raw material of ensuring correct implementation of availability and capacity standards and identifying capacity issues early.
- **Ratios and proportions** map to **Systems design** and **Systems integration**: sizing decisions — instances per service, agents per team, replicas per zone — are ratio judgements, and reviewing others' designs for efficient use of resources means checking their ratios, not just their diagrams.
- **Averages and distributions** map to **Development process optimisation**: mean and percentile pipeline durations, average queue times, and failure-rate distributions are how you demonstrate that a process change actually improved anything.
- **Trend reading and projection** map to your duty to plan and design large groups of stories and to initiate remedial action: forecasting when a disk fills, when a memory limit is reached, or when build demand outgrows the agent pool converts monitoring data into a plan.
- **Table and chart comprehension** map to **Service support** and **Information security**: incident dashboards, vulnerability counts by severity, and cost reports all arrive as tables; identifying and locating faults quickly depends on reading them accurately under pressure.

### Practice questions

**Question 1 (easy) — Availability percentage to downtime**

A service you support has a monthly availability target of 99.9%. The month in question has 30 days. To the nearest minute, what is the maximum downtime the service can incur this month while still meeting its target?

- A) 14 minutes
- B) 43 minutes
- C) 72 minutes
- D) 132 minutes

**Correct answer: B**

**Explanation:** Work step by step. Total minutes in the month: 30 days × 24 hours × 60 minutes = 43,200 minutes. The target permits 100% − 99.9% = 0.1% downtime. Downtime allowance: 43,200 × 0.001 = 43.2 minutes, which rounds to 43 minutes. Option A (14 minutes) is roughly the allowance for 99.97%; option C is close to the 99.83% level; option D would be about 99.7%. Knowing this conversion cold — 99.9% monthly is about 43 minutes, 99.99% is about 4.3 minutes — turns availability targets from slogans into engineering constraints, which is exactly what ensuring highly available deployment strategies requires.

**Question 2 (easy) — Change failure rate**

Last quarter your teams made 240 production deployments, of which 18 caused a degradation or outage requiring remediation. What was the change failure rate, as a percentage?

- A) 6%
- B) 7.5%
- C) 9%
- D) 13.3%

**Correct answer: B**

**Explanation:** Change failure rate = failed changes ÷ total changes × 100 = 18 ÷ 240 × 100. Compute: 18 ÷ 240 = 0.075, so 7.5%. Option A results from dividing by 300; option C from dividing 18 by 200; option D from inverting part of the calculation (240 ÷ 18 ≈ 13.3, which is the ratio of deployments per failure, a different and also useful number). Change failure rate is one of the four headline delivery metrics you will use when analysing current processes and demonstrating the effect of improvements, so being fluent in computing it — and in noticing when someone quotes its reciprocal — matters.

**Question 3 (easy) — Average pipeline duration**

Five runs of a pipeline this morning took 12, 15, 11, 14 and 18 minutes. What is the mean duration?

- A) 13 minutes
- B) 14 minutes
- C) 15 minutes
- D) 16 minutes

**Correct answer: B**

**Explanation:** Sum the durations: 12 + 15 + 11 + 14 + 18 = 70 minutes. Divide by the number of runs: 70 ÷ 5 = 14 minutes. A quick sanity check: the values range from 11 to 18, so the mean must sit inside that range, and 14 sits comfortably centrally. In practice you would also note the spread — the slowest run took 64% longer than the fastest — because when you optimise a process, tightening the variance often matters as much as lowering the mean: teams plan around the worst case, not the average.

**Question 4 (moderate) — Capacity headroom and growth**

A production service currently uses 480 GB of a 800 GB storage allocation. Usage is growing by 40 GB per month. Your standard requires remedial action to be initiated when utilisation reaches 80%. In how many months will the service reach the 80% threshold?

- A) 2 months
- B) 4 months
- C) 6 months
- D) 8 months

**Correct answer: B**

**Explanation:** First find the threshold in absolute terms: 80% of 800 GB = 640 GB. Current usage is 480 GB, so headroom to the threshold is 640 − 480 = 160 GB. At 40 GB per month, that is 160 ÷ 40 = 4 months. Option D (8 months) is the time to fill the allocation completely — the trap being to forget the 80% action threshold, which exists precisely so that remedial work happens before the crisis. This is the arithmetic behind your availability and capacity management skill: converting a policy percentage into a date on which you must have acted, then working backwards to when you must start.

**Question 5 (moderate) — Weighted mean time to restore**

Your incident log for the quarter shows: 6 priority-1 incidents with a mean time to restore of 90 minutes, and 18 priority-2 incidents with a mean time to restore of 40 minutes. What is the mean time to restore across all 24 incidents?

- A) 47.5 minutes
- B) 52.5 minutes
- C) 65 minutes
- D) 57.5 minutes

**Correct answer: B**

**Explanation:** A weighted average is needed — you cannot simply average 90 and 40 because there are three times as many P2s. Total restore time: (6 × 90) + (18 × 40) = 540 + 720 = 1,260 minutes. Divide by total incidents: 1,260 ÷ 24 = 52.5 minutes. Option C (65) is the unweighted average of 90 and 40 — the classic error. A useful instinct check: with P2s outnumbering P1s three to one, the overall mean must sit much closer to 40 than to 90, and 52.5 does. When you report service performance upwards or coach an on-call team using their own data, weighting correctly is the difference between an accurate picture and an accidentally flattering or alarming one.

**Question 6 (moderate) — Deployment frequency trend**

A team you support deployed 32 times in April, 40 times in May, and 50 times in June. What was the percentage increase in deployment frequency from April to June?

- A) 25%
- B) 36%
- C) 56.25%
- D) 62.5%

**Correct answer: C**

**Explanation:** Percentage increase = (new − old) ÷ old × 100 = (50 − 32) ÷ 32 × 100 = 18 ÷ 32 × 100 = 56.25%. Option A is the May-to-June increase (10 ÷ 40); option B is roughly the average of the two monthly increases (25% then 25%, compounding to 56.25% — note that two successive 25% rises do not add to 50%); option D uses 32 ÷ 50 upside down in the denominator. The compounding point is worth internalising: monthly growth rates multiply, they do not add — 1.25 × 1.25 = 1.5625. When you present a process optimisation's results, computing the end-to-end change correctly protects your credibility with numerate stakeholders.

**Question 7 (moderate) — Cost comparison for rightsizing**

A service runs 12 instances at £180 per instance per month. Monitoring shows average CPU utilisation of 20%. You propose consolidating to 5 larger instances at £310 per instance per month, which modelling suggests will run at about 55% utilisation. What is the monthly saving from the proposal?

- A) £310
- B) £610
- C) £520
- D) £1,550

**Correct answer: B**

**Explanation:** Current cost: 12 × £180 = £2,160 per month. Proposed cost: 5 × £310 = £1,550 per month. Saving: £2,160 − £1,550 = £610 per month. Option D is the new cost, not the saving; option A is one new instance's price; option C results from a slip in one multiplication. Beyond the arithmetic, the utilisation figures tell the qualitative story: 20% utilisation means you are paying for idle capacity, and the proposed 55% keeps sensible headroom — pushing towards, say, 90% would save more money but breach the availability principle that capacity must absorb spikes and instance failures. Reviewing others' designs for efficient use of resources is exactly this pairing of cost arithmetic with headroom judgement.

**Question 8 (moderate) — Error budget consumption**

A service has a 99.9% availability objective over a 30-day window, giving an error budget of 43.2 minutes of downtime. Fifteen days into the window, the service has already been down for 28.8 minutes. What percentage of the error budget has been consumed, and what is the most defensible operational response?

- A) 50% consumed — continue normal release cadence
- B) 66.7% consumed — slow or gate risky releases for the rest of the window
- C) 66.7% consumed — continue normal release cadence since the target is not yet breached
- D) 28.8% consumed — no action needed

**Correct answer: B**

**Explanation:** Budget consumed: 28.8 ÷ 43.2 = 0.667, i.e. 66.7%. But only half the window (15 of 30 days) has elapsed, so consumption is running at roughly 1.33 times the sustainable pace — if the burn rate continues, the budget exhausts around day 22, breaching the objective with over a week to spare. That is why B pairs the correct percentage with the correct response: error budgets exist to convert availability arithmetic into release decisions, and a budget burning faster than time elapses is the signal to slow down, add safeguards, or gate risky deployments. Option C computes correctly but ignores the burn-rate logic; options A and D miscompute. This question rehearses the exact reasoning you use to keep deployment strategies compatible with availability commitments.

**Question 9 (challenging) — Build agent queue arithmetic**

Your build agent pool has 10 agents. During the morning peak, teams submit 45 builds per hour, and each build occupies an agent for an average of 12 minutes. What is the average utilisation of the pool during the peak, and is the pool over or under capacity?

- A) 90% — under capacity, no queueing expected
- B) 90% — nominally under capacity, but queueing is likely because arrivals are uneven
- C) 75% — comfortably under capacity
- D) 108% — over capacity

**Correct answer: B**

**Explanation:** Work in agent-minutes. Demand per hour: 45 builds × 12 minutes = 540 agent-minutes. Supply per hour: 10 agents × 60 minutes = 600 agent-minutes. Utilisation: 540 ÷ 600 = 90%. So the pool is nominally under capacity — option D is wrong. But the second half of the judgement matters: build submissions cluster (stand-ups end, merges land together), and queueing theory's practical lesson is that waiting times grow sharply as utilisation approaches 100% with uneven arrivals. At 90% average utilisation, bursts will regularly exceed 10 concurrent builds and queues will form. Option A's "no queueing" conclusion misreads how averages hide peaks; option C miscalculates. This is precisely the reasoning behind identifying capacity issues before users complain: a resource can be simultaneously "under capacity" on average and painfully congested in practice.

**Question 10 (challenging) — Multi-service SLA table**

The quarterly report for four services you oversee shows:

| Service | Availability target | Achieved | Total requests (millions) | Error rate |
|---|---|---|---|---|
| Identity | 99.95% | 99.97% | 120 | 0.02% |
| Payments | 99.9% | 99.85% | 45 | 0.11% |
| Notifications | 99.5% | 99.6% | 300 | 0.35% |
| Reporting | 99.0% | 99.4% | 15 | 0.5% |

Which service failed its availability target, and approximately how many requests did Notifications serve with errors?

- A) Payments failed; Notifications served about 1.05 million error requests
- B) Payments failed; Notifications served about 105,000 error requests
- C) Reporting failed; Notifications served about 1.05 million error requests
- D) No service failed; Notifications served about 300,000 error requests

**Correct answer: A**

**Explanation:** Compare achieved against target row by row: Identity 99.97 ≥ 99.95 (met); Payments 99.85 < 99.9 (failed); Notifications 99.6 ≥ 99.5 (met); Reporting 99.4 ≥ 99.0 (met). Only Payments failed. For the error count: 0.35% of 300 million = 0.0035 × 300,000,000 = 1,050,000 — about 1.05 million error requests. Option B slips a decimal place (0.035% instead of 0.35%); option C misreads the Reporting row, where achieved exceeds target. Two habits protect you here: compare each achieved figure with its own row's target rather than a remembered "standard" target, and when taking a percentage of millions, write out the zeros. Reading a service report accurately is table stakes for the management conversation that follows it — especially the one with the Payments service owner.

**Question 11 (challenging) — Projecting compound growth**

A test environment's database currently holds 200 GB and is growing at 10% per month, compounding. The environment's storage limit is 300 GB. After how many whole months will the database first exceed the limit?

- A) 3 months
- B) 4 months
- C) 5 months
- D) 6 months

**Correct answer: C**

**Explanation:** Compound the growth month by month: month 1: 200 × 1.1 = 220 GB; month 2: 220 × 1.1 = 242 GB; month 3: 242 × 1.1 = 266.2 GB; month 4: 266.2 × 1.1 = 292.8 GB; month 5: 292.8 × 1.1 = 322.1 GB. The database first exceeds 300 GB after month 5. The linear-thinking trap is option A or B: "we need 100 GB more and we grow by 20 GB a month, so five months — no wait, 10% of 200 is 20, so 100 ÷ 20 = 5" happens to land on the right answer here only if you notice the growth base increases each month; with different numbers the linear shortcut fails badly, so always compound when the stem says compounding. Projections like this are how you initiate remedial action with a date attached — "we act by month 4" — rather than a vague warning.

**Question 12 (challenging) — Comparing before-and-after process metrics**

You led an optimisation of the release process. Before: 60 releases per quarter, mean lead time 5 days, 10% change failure rate. After: 90 releases per quarter, mean lead time 3 days, 8% change failure rate. Your head of engineering asks: "Did the absolute number of failed releases go up or down, and what happened to successful releases per quarter?"

- A) Failures fell from 6 to 5.4; successes rose from 54 to 82.8
- B) Failures rose from 6 to 7.2; successes rose from 54 to 82.8
- C) Failures rose from 6 to 7.2; successes fell from 54 to 48.6
- D) Failures fell from 6 to 5.4; successes rose from 54 to 84.6

**Correct answer: B**

**Explanation:** Before: failures = 10% of 60 = 6; successes = 60 − 6 = 54. After: failures = 8% of 90 = 7.2; successes = 90 − 7.2 = 82.8. So the failure rate fell but absolute failures rose slightly (6 → 7.2) because volume rose 50%, while successful releases rose dramatically (54 → 82.8, a 53% increase). Option A assumes a falling rate means falling absolute failures — the most common misreading of rate-versus-volume data. The honest summary for your head of engineering is that the change delivered many more successful releases at a lower failure rate, at the cost of about one extra failure per quarter in absolute terms — and being able to say that unprompted, before someone else spots it, is what makes your optimisation reporting trusted. Rates and absolutes answer different questions; senior engineers quote both.

### Preparation tips

- **Memorise the conversions you use anyway.** Minutes in a day (1,440), in a 30-day month (43,200); downtime allowances for 99.9% and 99.99%; the fact that successive percentage changes multiply. These are your professional times tables.
- **Practise on your own dashboards.** Take last month's monitoring or cost report and ask yourself assessment-style questions: what is the weighted average? when does this trend cross that threshold? Real data makes the techniques stick.
- **Write the formula before the numbers.** Under time pressure, jotting "CFR = failures ÷ total" before substituting prevents the inverted-ratio errors that distractors are built from.
- **Sanity-check every answer against the data's range.** A mean must lie within the values; a percentage of a subset cannot exceed the subset; a saving cannot exceed the original cost. Five seconds of checking catches most slips.
- **Watch for rate-versus-absolute traps.** Whenever a question mixes a percentage with a changing volume, expect the answer to hinge on the difference — because in capacity and delivery data, it usually does.
- **Use the calculator for arithmetic, not for thinking.** Decide the method mentally, then compute. Reaching for the calculator before you know what to calculate wastes the seconds the test is measuring.

### Common pitfalls to avoid

- **Averaging averages without weighting.** Unequal group sizes demand weighted means — in incident data, pipeline data and cost data alike.
- **Adding percentage changes.** Two 25% increases compound to 56.25%, not 50%. Distractors rely on the additive error.
- **Dropping the threshold.** Capacity questions often include an action threshold (80%, error budget pace). Computing time-to-full when the question asks time-to-threshold is a classic lost mark.
- **Decimal-place slips on large numbers.** 0.35% of 300 million invites a factor-of-ten error. Write the zeros out.
- **Linear projection of compound growth.** If the stem says compounding, compound. The linear shortcut understates growth more each month.
- **Answering the number but missing the judgement.** Some questions pair a calculation with an operational response. Compute correctly, then choose the response the number actually supports — the burn-rate question rewards exactly this pairing.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment measures how accurately you read, interpret and evaluate written material of the kind your role deals with every day. Rather than literary passages, it presents workplace texts — in your case, extracts from technology standards, security policies, incident reports, change advisory notes, supplier documentation, and emails from service owners and delivery managers — and asks you to determine what the text does and does not establish.

Typical format: an online, timed test lasting 15 to 25 minutes. The commonest question style presents a short passage followed by statements you must classify as True (the passage supports it), False (the passage contradicts it), or Cannot Say (the passage provides insufficient information either way). Other styles test inference, identifying the main point, and judging which rewrite of a sentence is clearest. The critical rule: answer only from the passage, not from your professional knowledge. A statement can be true in real life and still "Cannot Say" on the test.

For a senior DevOps engineer on the management track, verbal precision is a core professional skill, not an add-on. You read security requirements and must implement exactly what they mandate — neither less (a compliance gap) nor more (wasted effort). You read incident reports and must distinguish what is evidenced from what is assumed. You write runbooks, review documentation produced by the engineers you coach, and translate technical detail for service owners. Misreading a single conditional clause in a change freeze notice, or an "unless" in a security standard, has real operational consequences — and assessors know it, which is why verbal reasoning features so often in selection for senior technical management posts.

### How this assessment maps to your role

The assessment dimensions map directly to the skills in your capability framework:

- **Literal comprehension** maps to **Modern development standards** and **Information security**: applying standards and designing in security controls both begin with reading mandates precisely — what is required, what is recommended, what is exempted, and under which conditions.
- **True/False/Cannot Say discipline** maps to **Service support** and incident practice: an incident report tells you what was observed; treating a plausible cause as an established one is exactly the error that sends fault-finding down the wrong path.
- **Inference** maps to **Systems design** and **Systems integration**: supplier documentation and interface specifications rarely state everything explicitly; sound inference — and knowing where inference must stop and a clarifying question must be asked — keeps integration builds correct.
- **Clear-writing judgement** maps to your coaching and mentoring duty and to **User focus**: you review juniors' documentation and write for mixed audiences; recognising which formulation is clearest, and why, is a skill you both use and teach.
- **Identifying the main point** maps to **Development process optimisation**: process improvement proposals, retrospective write-ups and policy consultations are only actionable once you can extract the central claim from the surrounding detail.

### Practice questions

**Passage 1 (for Questions 1–3)**

"All services handling personal data must encrypt data in transit using the department's approved TLS configuration. Services that additionally handle special category data must also encrypt data at rest using keys managed by the central key management service. Development and test environments are exempt from the at-rest requirement provided they contain only synthetic data. Any exemption beyond this must be approved in writing by the Chief Information Security Officer."

**Question 1 (easy) — True/False/Cannot Say**

Statement: "A production service handling special category data must encrypt data both in transit and at rest."

- A) True
- B) False
- C) Cannot Say

**Correct answer: A**

**Explanation:** Trace the requirements. Special category data is personal data, so the in-transit requirement applies; the passage explicitly adds the at-rest requirement for special category data. The environment is production, so the development-and-test exemption is irrelevant. Both requirements therefore apply, and the statement is True. The technique is to layer the rules exactly as written — general rule, additional rule, exemption, exemption-to-the-exemption — the same way you would implement them in a compliance check. Notice how the passage's structure mirrors policy documents you genuinely implement: misreading the layering in real life produces either a data protection breach or unnecessary engineering work.

**Question 2 (easy) — True/False/Cannot Say**

Statement: "A test environment containing real customer records is exempt from the at-rest encryption requirement."

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The exemption for development and test environments is conditional: it applies "provided they contain only synthetic data". A test environment containing real customer records fails the condition, so the exemption does not apply, and the statement contradicts the passage — it is False, not Cannot Say. The trap is skimming "development and test environments are exempt" and stopping before the proviso. Conditional clauses — "provided", "unless", "subject to" — carry the operational meaning in standards documents, and assessors build questions on them because engineers who skim them build non-compliant environments. This is also a coaching point you will make repeatedly when juniors set up test data.

**Question 3 (moderate) — True/False/Cannot Say**

Statement: "The Chief Information Security Officer has approved at least one exemption."

- A) True
- B) False
- C) Cannot Say

**Correct answer: C**

**Explanation:** The passage establishes a mechanism — exemptions beyond the synthetic-data case require the CISO's written approval — but says nothing about whether any such exemption has ever been sought or granted. The statement is neither supported nor contradicted: Cannot Say. This distinction between a rule existing and a rule having been exercised is precisely the one you drew in the cognitive section's deployment-policy question, and it recurs throughout governance reading: "the process allows X" never entails "X has happened". Answering C when your instinct says "probably true in real life" is the core discipline of verbal reasoning tests.

**Passage 2 (for Questions 4–6)**

"Incident 4711 began at 09:14 when the payments service returned elevated error rates. The on-call engineer identified that a configuration change deployed at 09:02 had reduced the database connection pool size. The change was rolled back at 09:41 and error rates returned to normal by 09:45. The change had passed automated tests, which do not exercise the service under production-level load. A review of the change record shows peer review was completed, but the reviewer was not aware that the pool size parameter had been altered alongside the intended change."

**Question 4 (moderate) — True/False/Cannot Say**

Statement: "The incident lasted 27 minutes from onset to full recovery."

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** Anchor the interval on the exact events the statement names. Onset was 09:14. Full recovery — "error rates returned to normal" — was 09:45. The interval is therefore 31 minutes, not 27, so the statement contradicts the passage: False. The 27-minute figure comes from subtracting the onset time from the rollback time (09:41 − 09:14), but the rollback is the remedial action, not the recovery; the service remained degraded for four further minutes while the rollback took effect. Timeline questions are built on precisely this anchor trap, and it matters beyond the test: incident durations drive availability reporting and error budget accounting, and a report that quietly measures to the rollback rather than to recovery understates user impact. When you review your teams' incident write-ups, checking that every quoted duration is anchored on observed service state — not on operator actions — is one of the highest-value comments you can make.

**Question 5 (moderate) — True/False/Cannot Say**

Statement: "If the automated tests had exercised the service under production-level load, the incident would have been prevented."

- A) True
- B) False
- C) Cannot Say

**Correct answer: C**

**Explanation:** The passage states the tests do not exercise production-level load, and the fault was a reduced connection pool that presumably only bites under load. It is plausible that load-realistic tests would have caught it — but the passage does not establish that they would have: the pool might have been adequate for test-level load even at its reduced size, or the failure might have depended on production traffic patterns not reproducible in test. A counterfactual claim ("would have been prevented") needs stronger support than a plausible mechanism. Cannot Say. This is the discipline of good incident review: recommendations may cite plausible preventions, but a report — and a test answer — must not present a hypothesis as an established fact. Distinguishing evidenced findings from reasonable speculation is what makes your post-incident reviews trustworthy.

**Question 6 (moderate) — Inference**

Which of the following is the best-supported conclusion from Passage 2?

- A) The peer review process failed because the reviewer was careless.
- B) The change contained an alteration the reviewer did not know about, so the review could not assess it.
- C) Automated tests are not worth running since they missed this fault.
- D) The on-call engineer should have detected the problem before 09:14.

**Correct answer: B**

**Explanation:** The passage says peer review was completed but the reviewer "was not aware that the pool size parameter had been altered alongside the intended change". The direct conclusion is B: an unassessed alteration travelled with the reviewed change. Option A adds a judgement of carelessness the passage does not support — the alteration may have been buried in a large diff or generated by tooling; assigning blame goes beyond the evidence and, notably, beyond what a good blameless review culture would write. Option C is an overgeneralisation from one gap to worthlessness. Option D invents a duty the passage never mentions. The skill — accepting the conclusion the text supports and rejecting more attractive, more dramatic ones — mirrors how you should read your teams' incident reports before deciding on process changes.

**Passage 3 (for Questions 7–9)**

"The platform team proposes standardising all services on a single container orchestration platform. Currently, six services run on the strategic platform, three on a legacy scheduler, and one on a bespoke arrangement maintained by a single engineer. Migration of the legacy services is estimated at four sprints in total, while the bespoke service is estimated at six sprints alone due to undocumented dependencies. The proposal argues that standardisation will reduce the operational burden of maintaining three sets of tooling, monitoring and on-call knowledge, and will simplify recruitment and onboarding. The service owner of the bespoke service opposes the timing, citing a peak usage period in the next quarter."

**Question 7 (moderate) — True/False/Cannot Say**

Statement: "Migrating all four non-standard services is estimated to take ten sprints in total."

- A) True
- B) False
- C) Cannot Say

**Correct answer: A**

**Explanation:** The passage gives two estimates: the three legacy-scheduler services at four sprints "in total", and the bespoke service at six sprints "alone". Four plus six is ten sprints for all four non-standard services. The statement matches: True. The reading skill is attaching each number to its correct scope — "in total" covers the group of three; "alone" flags that the six sprints are for one service, not the whole programme. Misattaching scope words is how migration plans get misquoted in governance papers, and why your review of such papers — a routine senior-level duty — needs exactly this precision.

**Question 8 (challenging) — True/False/Cannot Say**

Statement: "Standardisation will reduce the operational burden of maintaining multiple sets of tooling."

- A) True
- B) False
- C) Cannot Say

**Correct answer: C**

**Explanation:** Careful: the passage reports that "the proposal argues" standardisation will reduce the burden. Reporting an argument is not endorsing it as fact — the passage tells us what the proposal claims, not what is true. Whether standardisation will actually deliver the reduction is not established by the text. Cannot Say. This "attribution shield" — the difference between "X is true" and "the document argues X" — is one of the most frequently tested distinctions in verbal reasoning, and one of the most operationally important in your role: when you summarise a supplier's whitepaper or a team's business case upwards, preserving the attribution ("the vendor claims", "the team estimates") keeps your own advice honest. Losing the attribution turns claims into facts and inflates confidence all the way up the management chain.

**Question 9 (challenging) — Identifying the strongest objection**

Based only on Passage 3, which of the following would be the most substantive point for you to raise when reviewing the proposal?

- A) The proposal should name the specific monitoring tools to be retired.
- B) The single-engineer dependency on the bespoke service is a risk that migration would reduce, but the same dependency plus undocumented dependencies make its six-sprint estimate the least reliable figure in the plan, and the migration is proposed to overlap the service's peak period.
- C) Six services already run on the strategic platform, so the proposal is unnecessary.
- D) The service owner's objection should be overruled because standardisation benefits recruitment.

**Correct answer: B**

**Explanation:** Option B synthesises the three facts the passage flags about the bespoke service — one maintaining engineer, undocumented dependencies, opposed timing over a peak period — into the observation that the riskiest and least estimable part of the plan is also the part scheduled against a business constraint. That is the review comment that changes the plan: perhaps migrate the three legacy services first while documenting the bespoke service's dependencies, then migrate it after the peak. Option A is a detail, not a substance issue. Option C misreads the proposal's purpose — the six compliant services are not its subject. Option D dismisses a stakeholder's stated business constraint, which is both poor reasoning (the passage gives no grounds to overrule) and poor management behaviour. Assessments at senior level reward answers that integrate the evidence rather than reacting to one fragment of it.

**Question 10 (moderate) — Clear-writing judgement**

You are reviewing a junior engineer's draft runbook. Which version of the rollback instruction is clearest and safest?

- A) "In the event of the observation of anomalous error rate elevation subsequent to deployment, consideration should be given to the initiation of rollback procedures."
- B) "If error rates rise above 2% within 15 minutes of deployment, run `deploy rollback` and notify the on-call lead."
- C) "Roll back if things look wrong."
- D) "Errors after deploying might mean you need to roll back, which can be done using the usual command, if appropriate."

**Correct answer: B**

**Explanation:** Option B gives a measurable trigger (error rate above 2%), a time bound (within 15 minutes), a concrete action (the exact command), and a communication step (notify the on-call lead). Option A buries the instruction under nominalisations ("initiation of rollback procedures") and passive constructions — no one reading it at 3 a.m. knows what to do or when. Option C is direct but replaces criteria with vibes, guaranteeing inconsistent decisions across the on-call rota. Option D hedges every clause ("might", "usual command", "if appropriate") and specifies nothing. Clear-writing questions test the editorial judgement you exercise whenever you review documentation: operational writing succeeds when a stressed reader with no context can act on it correctly. Teaching a junior engineer why B beats their draft — trigger, threshold, action, notification — is a better mentoring intervention than rewriting it for them.

**Question 11 (challenging) — Comprehension of a change freeze notice**

An email from the head of operations reads: "A change freeze applies to all citizen-facing services from 18 December to 2 January inclusive. Emergency fixes remain permitted under the expedited process. Internal-only services are out of scope of the freeze, except those on the shared payments infrastructure, which are in scope. Changes approved before 18 December but not yet deployed must be re-approved after the freeze ends."

Which of the following deployments would be permitted on 27 December without invoking the emergency process?

- A) A routine feature release to a citizen-facing service, approved on 15 December.
- B) A routine configuration change to an internal-only reporting service that does not use the shared payments infrastructure.
- C) A routine update to an internal-only service that runs on the shared payments infrastructure.
- D) No deployment of any kind is permitted during the freeze.

**Correct answer: B**

**Explanation:** Map each option to the rules. Option A: citizen-facing services are frozen 18 December to 2 January; prior approval does not help — indeed the notice explicitly says pre-freeze approvals need re-approval afterwards. Frozen. Option C: internal-only services are out of scope "except those on the shared payments infrastructure, which are in scope" — so this one is frozen. Option D overstates: the freeze never covered internal-only services off the payments infrastructure, and emergencies have a path. Option B is an internal-only service, not on the payments infrastructure, so the freeze does not apply and a routine change may proceed. Layered scope rules with exceptions-to-exceptions are the everyday grammar of operational notices; reading them accurately determines whether your teams deploy legitimately or breach a freeze — and as the senior engineer, you are the person your teams will ask.

**Question 12 (challenging) — Main point of a policy consultation extract**

"Departments are increasingly adopting continuous deployment, in which changes pass automatically to production once all quality gates succeed. This consultation does not propose prohibiting continuous deployment. It proposes that where continuous deployment is used for services above the significant-impact threshold, departments must be able to demonstrate that their automated quality gates provide assurance at least equivalent to the manual change approval they replace, and must retain the ability to suspend automatic promotion during major incidents. Responses are invited on the equivalence criteria in particular."

Which statement best captures the main point?

- A) The consultation proposes banning continuous deployment for significant services.
- B) The consultation proposes that automated gates for significant services must demonstrably match the assurance of the manual approvals they replace, with a suspension capability, and seeks views especially on the equivalence criteria.
- C) The consultation concludes that manual change approval is obsolete.
- D) The consultation requires all departments to adopt continuous deployment.

**Correct answer: B**

**Explanation:** The passage explicitly disclaims prohibition (eliminating A), proposes conditional requirements rather than mandating adoption (eliminating D), and treats manual approval as the assurance baseline to be matched, not as obsolete (eliminating C). B captures the two substantive requirements — demonstrable equivalence and a suspension capability — and the consultation's specific request for input on equivalence criteria. Extracting a main point means preserving the proposal's qualifiers: "where used", "above the threshold", "at least equivalent". As a senior engineer you will be asked to draft your team's response to consultations like this; a response that answers A's misreading instead of B's actual question wastes everyone's time and your department's voice.

### Preparation tips

- **Train the Cannot Say reflex.** After each practice passage, ask: is this statement supported, contradicted, or merely plausible? Your professional knowledge makes "plausible" feel like "true" — the test punishes exactly that.
- **Underline conditionals and scope words.** "Unless", "provided that", "except", "inclusive", "in total", "alone" — these small words carry the meaning in policies and notices. Practise spotting them on first read.
- **Watch for attribution.** "The proposal argues", "the vendor claims", "the team estimates" report a claim without endorsing it. Statements that drop the attribution are usually Cannot Say.
- **Practise on real documents.** Read a Technology Code of Practice point, a security standard, or a change freeze email and write three statements about it: one True, one False, one Cannot Say. Building the questions teaches the distinctions faster than answering them.
- **For clear-writing items, look for actionability.** The best operational sentence names a trigger, a threshold, an action and an owner. Rank options by how confidently a tired stranger could act on them.
- **Manage passage time.** Skim the passage once for structure, then read the statement, then return to the relevant lines. Re-reading whole passages for every statement is where time drains away.

### Common pitfalls to avoid

- **Importing your own knowledge.** You know how TLS, freezes and consultations really work; the passage defines its own world. Answer from the text alone.
- **Treating reported claims as facts.** The most common Cannot Say trap at senior level, because you read persuasive documents (business cases, vendor material) all day.
- **Skimming past provisos.** Exemptions are almost always conditional. An answer that ignores the "provided that" clause is usually the distractor.
- **Choosing dramatic inferences.** Blame, obsolescence and prohibition are attractive conclusions; the supported conclusion is usually quieter and more precise.
- **Wrong anchors in timelines.** When a statement quotes an interval, recompute it from the exact events named — rollback time and recovery time are different events.
- **Spending your empathy on the writer.** In clear-writing items, judge the text a stressed reader receives, not the effort the writer invested. That is also the kindest honest standard for reviewing your juniors' documentation.

## Workplace job-specific situational judgement assessment

### About this assessment

A situational judgement test (SJT) presents realistic workplace scenarios and asks you to judge the effectiveness of possible responses. Unlike cognitive or numeric tests, there is rarely a mathematically provable answer; instead, responses are scored against the judgement of experienced practitioners and the behaviours your organisation values — in the UK Government Digital and Data context, behaviours such as user focus, collaboration, taking ownership, appropriate escalation, developing others, and inclusion.

Typical format: an online test of 10 to 20 scenarios, often untimed or generously timed. Question styles include picking the most effective response, picking the most and least effective from four options, ranking all options, or rating each option independently on an effectiveness scale. Read the instructions carefully: "most effective" questions ask what works best, not what you would personally do, and rating formats allow several options to be rated highly.

For a senior DevOps engineer on the management track, the SJT is arguably the most role-relevant assessment of the four. Your scenarios are not hypothetical: a junior engineer's mistake reaching production, a security concern surfacing days before a deadline, a team resisting a new standard, a colleague struggling on the on-call rota, a delivery manager pressuring you to skip a gate. In each case the technically correct action and the humanly effective action must be found together, because at this level you deliver through other people as much as through your own keyboard. The SJT measures whether your instincts balance delivery, safety, honesty, and the development and wellbeing of your team — which is exactly the balance your coaching, mentoring and team leadership duties demand.

### How this assessment maps to your role

The assessment dimensions map directly to the skills in your capability framework:

- **Ownership and escalation judgement** maps to **Service support** and **Availability and capacity management**: knowing when to fix, when to escalate, and when to initiate remedial action on your own authority is the situational core of both skills.
- **Developing others** maps to your explicit duty to provide **coaching and mentoring to more junior colleagues**: SJT scenarios probe whether you turn mistakes into learning, delegate stretching work safely, and give feedback that changes behaviour without damaging confidence.
- **Collaboration and influence** map to **Development process optimisation** and **Systems design** review duties: leading a team of experts to deliver improvements, and reviewing others' designs, both fail if handled with technical correctness but interpersonal clumsiness.
- **Integrity under pressure** maps to **Information security** and **Modern development standards**: the scenarios where a deadline tempts someone to bypass a control are exactly where designing in security and upholding standards become behavioural rather than technical questions.
- **User focus** maps to your **User focus** skill: several scenarios test whether you keep the citizen or end user's interest visible when internal pressures — deadlines, politics, convenience — push it out of frame.

### Practice questions

**Question 1 (easy) — A junior engineer's mistake reaches production**

A junior engineer you mentor accidentally applies a configuration change to production instead of staging. The change causes a brief, minor degradation, which they immediately notice and revert themselves. Visibly shaken, they come straight to you and admit what happened. What is the most effective first response?

- A) Thank them for their honesty and quick revert, check the service is stable, then arrange to review together how the mistake became possible — including whether guard rails are missing.
- B) Report the incident to their line manager so it can be recorded in their performance file.
- C) Tell them not to worry about it and move on — everyone makes mistakes.
- D) Remove their production access until they have completed additional training.

**Correct answer: A**

**Explanation:** Option A does four things in the right order: it reinforces the exact behaviour you want repeated (immediate honesty and remediation), it verifies current service state — ownership of the live service comes first — and it converts the mistake into learning at both the individual and the system level. The system question matters most: a change that can be applied to production by accident reveals missing guard rails (environment confirmation, restricted credentials, protected contexts), and fixing the system is your responsibility, not the junior's. Option B punishes disclosure, teaching your team to hide the next mistake — the most corrosive possible lesson for incident culture. Option C wastes the learning and leaves the systemic weakness in place. Option D is disproportionate to a self-caught, self-reverted minor error and signals that admitting mistakes costs you your job's substance. Blameless-but-thorough is the professional standard, and it is also what your coaching duty looks like under pressure.

**Question 2 (easy) — Deadline pressure to skip a quality gate**

A delivery manager asks you to let a release skip the automated security scan "just this once" because a ministerial announcement depends on the feature shipping today, and the scan queue is running three hours behind. What is the most effective response?

- A) Agree — the announcement is clearly the priority and the code is probably fine.
- B) Refuse and tell the delivery manager that process is process, ending the conversation.
- C) Explore options that protect both goals: expedite the scan for this release, check whether the deployment can proceed to a gated state pending the result, and if no compliant path exists in time, escalate jointly to the service owner with a clear statement of the risk.
- D) Quietly run the release through a reduced version of the scan you assemble yourself, without telling anyone.

**Correct answer: C**

**Explanation:** The scenario tests whether you treat a control as an obstacle, a weapon, or a risk-management tool. Option C treats it as the third: it looks for a legitimate fast path (queue prioritisation is usually possible and often sufficient), considers a technical compromise that keeps the gate meaningful, and — crucially — if the tension cannot be resolved, moves the decision to the accountable owner with the risk stated plainly, rather than making a concealed exception yourself. Option A abandons a security control under schedule pressure, precisely the behaviour "design in security" exists to prevent. Option B may be procedurally defensible but fails collaboratively: it leaves the delivery manager with a binary and an adversary rather than an ally, and senior engineers are expected to generate options. Option D is the worst of all: an undocumented, unofficial control substitution that no one approved and no one can audit. Note the general SJT pattern: the strongest option usually protects the substance of the control and the relationship and the transparency of the decision.

**Question 3 (moderate) — Coaching versus doing it yourself**

A junior engineer has spent two days stuck on a pipeline fault that you are fairly sure you could fix in twenty minutes. The team's sprint goal is not at risk yet, but it will be if the fault persists another two days. What is the most effective response?

- A) Fix it yourself immediately — the team's throughput comes first.
- B) Pair with them: ask them to walk you through what they have tried, guide them with questions towards the diagnosis, and let them implement the fix.
- C) Leave them to struggle — learning requires productive difficulty and they will figure it out eventually.
- D) Reassign the task to a mid-level engineer and give the junior something easier.

**Correct answer: B**

**Explanation:** This is the classic senior-level tension between delivery and development, and the scenario's details tell you the sprint can afford a coaching investment: the goal is not yet at risk. Option B resolves the tension rather than picking a side — pairing bounds the time cost (you steer the diagnosis, so it will not take two more days), transfers your diagnostic method (asking what they have tried honours their effort and surfaces their reasoning), and leaves the junior with the fix in their hands, which is what builds capability and confidence. Option A trades a twenty-minute win for a repeated dependency: the next fault lands on your desk too. Option C misapplies "productive struggle" — two days without progress is unproductive struggle, and unsupported struggle corrodes confidence. Option D solves the task but tells the junior they were not worth investing in. Your role explicitly includes coaching and mentoring; SJT scorers at this level look for options that deliver through developing people, using the slack the scenario says exists.

**Question 4 (moderate) — Discovering a colleague's shortcut**

While reviewing pipeline configurations, you discover that a respected mid-level engineer on a neighbouring team has disabled the failing accessibility test suite in their pipeline "temporarily" — the commit is three months old. The service is citizen-facing. What is the most effective response?

- A) Re-enable the suite yourself and say nothing — the configuration is wrong and you have access.
- B) Raise it directly with the engineer: ask what happened, explain the user impact of a citizen-facing service shipping unchecked accessibility regressions for three months, and agree a plan to fix the failures and re-enable the suite — offering help if the failures are the blocker.
- C) Report the engineer to their line manager for breaching standards.
- D) Note it for the next quarterly standards audit.

**Correct answer: B**

**Explanation:** Start with the user: a citizen-facing service has shipped for three months without accessibility checks, which risks excluding disabled users — the people accessibility standards exist to protect. That rules out D's leisurely timescale. Option A fixes the configuration but not the situation: re-enabling a suite with three months of accumulated failures will block the team's pipeline without warning, and acting silently in someone else's codebase corrodes trust. Option C escalates before conversation; the commit says "temporarily", which suggests an intention that decayed rather than defiance — the engineer most likely hit failing tests under deadline pressure and the disablement outlived its excuse. Option B addresses the user impact with urgency, treats a respected colleague as a professional, uncovers the real blocker, and — by offering help — turns a standards breach into a collaborative fix. It also models the behaviour publicly valued in your framework: champion user research and user needs "to focus on all users", which explicitly includes accessibility. Escalation remains available if the direct route fails; effective escalation is a next step, not a first resort, when no immediate harm requires otherwise.

**Question 5 (moderate) — An overloaded on-call colleague**

During a one-to-one, an engineer on your team mentions, half-jokingly, that they have been woken by pages four nights this week and their partner is "about ready to throw the laptop out of the window". The alerts mostly turn out to be false positives from a noisy threshold. Sprint commitments are tight. What is the most effective response?

- A) Sympathise, and suggest they use noise-cancelling settings on their phone so the pages disturb them less.
- B) Treat it as two linked problems and act on both: rebalance or relieve their on-call load now to protect their wellbeing, and prioritise tuning or fixing the noisy alert threshold this sprint as the root cause — even at some cost to sprint scope.
- C) Tell them on-call disruption is part of the role at their level and the rota is fixed for the quarter.
- D) Remove them from the on-call rota permanently.

**Correct answer: B**

**Explanation:** The half-joking disclosure in a one-to-one is exactly how real wellbeing problems surface; taking it seriously is a management-track fundamental. Option B recognises the two layers: an immediate human problem (four disturbed nights in a week is a health and safety issue, not a resilience test) and a technical root cause squarely inside your availability and capacity management remit — a noisy threshold paging humans for non-incidents is a defect in the alerting design, and every false positive also erodes the team's trust in real alerts. Trading some sprint scope for alert hygiene is a defensible engineering-management call, and being willing to make it visibly tells the team their sustainability is a first-class concern. Option A treats the symptom's symptom. Option C sacrifices a person to a rota artefact and will eventually cost you the engineer. Option D overcorrects, removing a capable responder and loading everyone else, without fixing the alerts that will wake them too. The scored behaviours: care for people, ownership of root causes, and honest re-prioritisation rather than pretending the sprint plan is sacred.

**Question 6 (moderate) — Most and least effective: conflicting review feedback**

You review a junior engineer's systems design and identify a scaling flaw. Separately, a senior engineer on another team has already reviewed it and commented "looks good to me". The junior is about to start building. Identify the most effective and least effective responses.

1. Explain the flaw to the junior directly, walk through the scenario where it fails, and loop in the other reviewer so all three of you converge on a revised design.
2. Tell the junior to go with the other reviewer's approval since seniors disagree and theirs came first.
3. Post a comment in the team channel that the design has a flaw the other reviewer missed.
4. Ask the junior questions in your review that lead them to discover the flaw themselves, then agree next steps.

- A) Most effective: 1; least effective: 3
- B) Most effective: 4; least effective: 2
- C) Most effective: 1; least effective: 2
- D) Most effective: 4; least effective: 3

**Correct answer: A**

**Explanation:** Both 1 and 4 are strong coaching behaviours, so the discriminator is the situational detail: build is about to start and a conflicting approval exists. Option 1 resolves the disagreement itself — bringing the other reviewer in converts "two seniors disagree" into "the reviewers converged", which unblocks the junior cleanly and maintains review integrity across teams; the Socratic route in 4, though excellent teaching, leaves the conflicting sign-off standing and delays a time-sensitive decision. For least effective: option 2 is poor (it privileges sequence over substance and ships a known flaw), but option 3 is worse — it broadcasts a colleague's oversight publicly before speaking to them, damaging trust with both the junior (whose work is publicly criticised) and the senior (who learns of the disagreement from an audience). Public correction before private conversation is the most reliably penalised behaviour in collaboration-focused SJTs, because its damage is social, lasting, and wholly avoidable. When reviewing others' designs — an explicit skill at your level — how you disagree is part of the competence.

**Question 7 (challenging) — Capacity warning versus roadmap pressure**

Your monitoring projects that a citizen-facing service will exhaust database connections within about six weeks at current growth. Fixing it properly requires two sprints of re-architecture. The product manager wants the next two sprints spent on a high-profile feature promised to the programme board, and suggests "we'll deal with capacity when it actually breaks". What is the most effective response?

- A) Accept the product manager's call — they own the backlog and the prioritisation.
- B) Quantify the risk and its timeline in business terms, present interim mitigations (connection pooling changes, load shedding) that narrow but do not remove the risk, and take the trade-off with your recommendation to the service owner for an informed decision — while recording the decision and its rationale.
- C) Instruct your engineers to work on the re-architecture anyway without telling the product manager, since availability is your accountability.
- D) Email the programme board directly warning that the feature will cause an outage.

**Correct answer: B**

**Explanation:** "Deal with it when it breaks" for a citizen-facing service is not a legitimate plan — it converts a manageable engineering task into a future major incident with user harm. But the response must work through, not around, the people who own the trade-off. Option B does what a senior engineer on the management track is for: translate a technical projection into business terms ("in about six weeks, citizens will see failures during peak hours"), generate options that partially de-risk the preferred plan, make a clear recommendation, and route the residual decision to the accountable service owner with the rationale recorded. That is initiating remedial action and escalating properly, simultaneously. Option A abdicates your professional duty to make risk visible — prioritisation authority does not extinguish your advisory responsibility. Option C is shadow work: it breaks trust, hides a material trade-off, and if discovered destroys your influence on every future prioritisation. Option D leaps two escalation levels, weaponises the risk, and burns the product relationship — escalation should follow the shortest path to the accountable decision-maker, with the people involved aware of it. The pattern to internalise: make the risk undeniable, make the options real, make the decision owned, make the record permanent.

**Question 8 (challenging) — A standard you disagree with**

The department mandates a new deployment tool across all teams. You believe, with evidence from a proof of concept, that it will slow your teams' pipelines significantly. Your engineers are frustrated and some suggest quietly keeping the old tool "until someone notices". What is the most effective response?

- A) Allow your teams to keep the old tool quietly — the mandate was made without understanding your context.
- B) Adopt the mandated tool as required, and separately submit your proof-of-concept evidence through the standards governance route, requesting either an exemption or a change to the standard — while telling your teams openly that this is how the disagreement will be pursued.
- C) Adopt the tool and tell your teams that mandates are not up for discussion.
- D) Delay adoption indefinitely by citing "integration complexities" in status reports.

**Correct answer: B**

**Explanation:** This scenario tests the difference between disagreement and defiance. Option B disagrees professionally: it complies with the legitimate authority of the standard (standards deliver their value — shared tooling, transferable knowledge, consolidated support — precisely because compliance is not optional per team), while pursuing the disagreement transparently through the route that can actually change the outcome, armed with the proof-of-concept evidence that makes the case credible. Telling your teams how the challenge is being pursued matters as much as pursuing it: it models constructive dissent and prevents the corrosive "quiet non-compliance" culture that option A would endorse. Option A also sets your teams up for a painful forced migration later, without support, when the divergence is discovered. Option C complies but wastes both the evidence and a teaching moment about how professionals disagree with organisations. Option D is dishonesty in slow motion — misrepresenting status reports is an integrity breach that outlasts any tooling question. Your framework's expectation that you help "evaluate and establish requirements for the implementation of changes by setting policy and standards" cuts both ways: you uphold standards, and you improve them through the front door.

**Question 9 (challenging) — Production incident during a team ceremony**

You are facilitating a retrospective your team has needed for weeks — morale is low after a difficult quarter. Fifteen minutes in, a monitoring alert fires for a citizen-facing service: error rates are elevated but the service is degraded, not down. The on-call engineer is in the retrospective. What is the most effective response?

- A) Continue the retrospective — the service is only degraded and the retrospective is important for the team.
- B) End the retrospective and have the whole team join the incident response.
- C) Release the on-call engineer to investigate immediately, ask a second engineer to support them if needed, and continue the retrospective with the rest of the team — checking in on the incident at a natural break and being ready to stop if it escalates.
- D) Investigate the alert yourself while the team continues the retrospective without you.

**Correct answer: C**

**Explanation:** The judgement being tested is proportionate response. A degraded citizen-facing service requires immediate attention — user focus rules out option A, which gambles user experience against a meeting. But degraded-not-down does not require ten people; option B swings to the opposite disproportion, teaching the team that any alert vaporises any commitment, and sacrificing a morale-critical session that the scenario tells you the team needs. Option C matches response to severity: the designated on-call engineer responds (respecting the rota system you have built), a support buddy is pre-arranged (removing the lone-responder risk), and you preserve the team investment while keeping an explicit escalation trigger. Option D is subtly wrong for a management-track senior: it bypasses the on-call system you own, makes you the single point of response, and abandons your facilitation role — doing the junior job instead of the senior one. The strongest SJT answers at this level delegate the response, protect the system that makes response reliable, and keep strategic activities alive under tactical pressure.

**Question 10 (challenging) — Inclusion in technical discussions**

In your team's design discussions, you notice the same two confident engineers do most of the talking. A quieter engineer — recently returned from a career break — made a suggestion last week that was talked over, yet closely resembles the design the team eventually reached two days later; no one acknowledged the connection. What is the most effective response?

- A) Do nothing — technical discussions are meritocratic and the best ideas won in the end.
- B) Publicly credit the quieter engineer's earlier suggestion at the next design discussion, and change the format to give ideas a fairer hearing — for example, written proposals before discussion, structured turn-taking, and you actively inviting contributions — while privately encouraging the engineer.
- C) Privately tell the two confident engineers to talk less.
- D) Move the quieter engineer to a team with a gentler culture.

**Correct answer: B**

**Explanation:** The scenario contains a measurable failure: the team reached the right design two days late because it could not hear the person who already had it — inclusion here is a delivery issue as well as a fairness issue. Option B acts on all three levels. Public credit corrects the record, signals that contributions are tracked to their source, and costs nothing. Format changes attack the mechanism rather than the personalities: written proposals and structured turn-taking are standard techniques for making design discussion favour idea quality over vocal confidence — a direct expression of your duty to guide how the team works and to establish design patterns as a team activity. Private encouragement supports the individual without making them the problem. Option A mistakes outcome for process: the idea won eventually, anonymously, and slowly — that is not meritocracy working, it is meritocracy failing with a lucky ending. Option C treats colleagues as the defect and, done clumsily, creates resentment without changing the structure that rewards interrupting. Option D removes the signal and keeps the noise: the team culture remains exclusionary for the next quiet joiner. Assessors look for responses that fix systems, credit fairly, and develop everyone — the quieter engineer's confidence and the louder engineers' collaboration alike.

**Question 11 (challenging) — Most and least effective: inherited fragile automation**

You inherit responsibility for a deployment automation script, written by an engineer who has left, that the whole department depends on. It is undocumented, has no tests, and last month failed twice, requiring manual intervention at 2 a.m. Your backlog is full. Identify the most effective and least effective responses.

1. Schedule incremental hardening: characterise current behaviour with tests first, add documentation as you learn it, and refactor in small safe steps alongside backlog work — with the risk logged so the investment is visible.
2. Rewrite the whole script from scratch immediately, since it is clearly not fit for purpose.
3. Leave it alone — it mostly works, and touching undocumented code risks breaking it.
4. Raise the risk with your head of engineering and propose pausing one backlog item to fund the initial characterisation work.

- A) Most effective: 1; least effective: 3
- B) Most effective: 4; least effective: 2
- C) Most effective: 1; least effective: 2
- D) Most effective: 4; least effective: 3

**Correct answer: A**

**Explanation:** Options 1 and 4 are both professional; the discriminator is completeness. Option 1 is a full senior-level response: it applies the established engineering discipline for hazardous inherited code (characterisation tests before change, small reversible steps), it converts tribal knowledge into documentation as a by-product, and — critically — it logs the risk so the effort is visible and defensible. Option 4 is a good escalation but only funds the first step; on its own it outsources a judgement you are equipped to make and schedule. Note that 1 effectively contains 4's virtue (visibility via the risk log) while 4 does not contain 1's plan. For least effective: option 2 feels decisive but is the classic trap — a from-scratch rewrite of an undocumented, untested, department-critical script maximises risk exactly where you have least knowledge, and history's failed rewrites are littered with behaviours nobody knew were load-bearing. Yet option 3 is worse: it is a decision to keep waking engineers at 2 a.m., accepts unbounded operational risk on a department-wide dependency, and abdicates the ownership your service support and process optimisation skills exist to express. Between reckless action and negligent inaction, SJT scoring — and good engineering management — condemns negligent inaction hardest when the harm is already occurring twice a month.

### Preparation tips

- **Answer as the role, not as the hero.** Management-track scenarios reward delegating through systems (on-call rotas, governance routes, review processes) rather than personally swooping in. If your instinctive answer has you doing a junior's job, look again.
- **Look for the option that protects both.** The strongest responses usually protect the delivery and the relationship, the control and the deadline, the person and the root cause. Options that sacrifice one entirely are rarely scored highest.
- **Check the escalation path length.** Effective escalation goes to the nearest accountable decision-maker, with the people involved aware. Options that skip levels or escalate behind someone's back are reliably penalised.
- **Use the scenario's stated slack.** Details like "the sprint goal is not at risk yet" or "degraded, not down" are calibration signals telling you how much room you have for coaching, ceremony, or deliberation. Read them as deliberately placed.
- **Rehearse your values before the test.** Spend ten minutes recalling the behaviours your organisation publishes — user focus, honesty, developing others, inclusion. SJTs are scored against those, and having them consciously loaded improves consistency.
- **In most/least formats, find the least first.** Dishonesty, concealment, public blame and negligent inaction are usually easy to spot; eliminating the worst option often clarifies the choice among the good ones.

### Common pitfalls to avoid

- **Punishing honesty.** Any option that makes disclosure more costly for the discloser — formal reports for self-caught minor errors — teaches concealment and scores badly.
- **Quiet workarounds.** Secretly keeping old tools, secretly doing unapproved work, secretly substituting controls: concealment converts a defensible judgement into an integrity failure every time.
- **Binary refusals.** "No, process is process" without generating options fails the collaboration dimension even when the refusal itself is right. Senior engineers create paths, not just verdicts.
- **Over-escalation and under-escalation.** Emailing the programme board about a solvable risk is as wrong as sitting on an unsolvable one. Match the escalation to the decision that needs making.
- **Fixing the person instead of the system.** Telling confident engineers to talk less, removing juniors' access, or moving quiet people to other teams treats structural problems as personality problems.
- **Sacrificing long-term capability for short-term throughput.** Doing the twenty-minute fix yourself, every time, builds a team that always needs you. The management track is scored on the team you build, not the tickets you close.

<!-- APPEND -->
