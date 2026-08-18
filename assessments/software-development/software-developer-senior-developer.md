# Senior Developer - Psychometric Assessment Resources

## Introduction

Welcome! This guide has been created especially for you as a senior developer working within the UK Government Digital and Data profession. Whether you are preparing for an internal assessment, applying for a new post, benchmarking your own capability against the framework, or simply curious about how psychometric assessments connect to the work you do every day, this document will help you practise, reflect, and build confidence.

Psychometric assessments are structured, standardised exercises that measure the mental capabilities and behavioural tendencies that predict success in a role. For a senior developer, that means far more than abstract puzzles. The assessments described here are job-specific: they use the kinds of artefacts you genuinely handle — pull requests, build pipelines, monitoring dashboards, incident timelines, capacity forecasts, integration plans, and technical design reviews — and the kinds of decisions you genuinely make, such as planning and leading development on sets of related stories, designing systems with security controls engineered in from the start, coordinating build activities across systems, and coaching more junior colleagues while operating the production services you build.

Why do these assessments matter for your role in particular? As a senior developer, you deliver and integrate software to form a complete service. That demands an unusual combination of capabilities: the analytical precision to spot a subtle defect in a diff or a flaw in a systems design, the numerical fluency to reason about error rates, capacity headroom, and delivery metrics, the verbal precision to read standards and specifications exactly and to write documentation others can reuse, and the judgement to handle the human situations that come with seniority — a mentee who is struggling, a production incident during a busy release week, a disagreement with another discipline about what needs to be built. Assessments of cognitive ability, numerical reasoning, verbal reasoning, and situational judgement map directly onto those demands. Practising them sharpens exactly the skills your role depends on.

This document is organised into four main assessment sections, each following the same pattern: an overview of what the assessment measures and why employers use it for roles like yours, a mapping of the assessment's dimensions to the specific named skills in the senior developer capability framework, a substantial set of practice questions with full worked explanations, practical preparation tips, and common pitfalls to avoid. Every question is grounded in the realities of building and running government digital services: test-driven development, code that is open by default, user needs rather than user desires, and production responsibility.

Here is how to get the most from the guide. First, read each "About this assessment" section so the format holds no surprises. Second, attempt every practice question honestly — commit to an answer before reading the explanation, exactly as you would commit to a hypothesis before checking the logs. Third, treat every explanation as a mini-lesson: even when you answer correctly, the worked reasoning will deepen your technique, and many explanations connect the question back to how you review code, run incidents, or mentor others. Finally, use the preparation tips and pitfalls as prompts for self-reflection: they connect assessment performance back to your growth as an engineer who takes responsibility for understanding the whole system and teaching it to others.

Take your time, be kind to yourself, and enjoy the practice. Let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive ability assessment measures the exact mental processes your role demands, using practical workplace scenarios rather than abstract puzzles. Unlike a generic intelligence test, it presents you with the everyday materials of your job — in your case, code and configuration fragments, dependency graphs, deployment pipelines, log extracts, systems designs, and integration schedules — and asks you to reason quickly and accurately about them.

Typical format: an online, timed test lasting 15 to 30 minutes, with somewhere between 15 and 30 questions covering pattern recognition, logical deduction, error checking, prioritisation, and applied problem solving. Scoring is objective, comparing your responses against a norm group of people at a similar level, and modern platforms often adapt question difficulty based on your previous answers — so a test that feels progressively harder is usually a sign you are doing well, not badly. Employers typically receive a breakdown of speed versus accuracy rather than a single number, which means working both quickly and carefully matters. You will normally be offered short, ungraded practice questions before the real test begins, so you can get comfortable with the interface without pressure.

For a senior developer, cognitive assessment is particularly relevant because your core professional value is structured technical thinking at the level of a whole service. You are expected to have an understanding of the whole system and to take responsibility for teaching it to others; that requires holding many moving parts in mind at once — which components depend on which, what a change in one service implies for its consumers, where a design contradicts an agreed standard, and what follows logically when a deployment step fails. You review the systems designs of others, coordinate build activities across systems, and identify, locate and fix service faults under time pressure. A well-designed cognitive assessment simulates precisely those demands in miniature: it rewards the person who reads carefully, deduces only what the evidence supports, and finds the minimal correction that restores consistency.

Employers in government digital settings use these assessments for senior technical roles because interview performance alone is a weak predictor of day-to-day reasoning quality. A candidate can talk fluently about architecture yet miss the off-by-one error in a pagination routine; another may be quiet in interviews yet consistently spot the flaw in an integration plan. Objective, job-realistic cognitive measurement helps level that field — and practising it helps you show your true capability on the day.

### How this assessment maps to your role

The assessment dimensions map directly to the named skills in your capability framework:

- **Pattern recognition** maps to **Programming and build (software engineering)** and **Modern development standards**: designing, coding, testing and documenting programs of medium-to-high complexity means recognising recurring structures — naming conventions, design patterns, repeated failure signatures in logs — and noticing when something breaks the pattern. It also maps to **Prototyping**, where you establish design patterns and iterate them.
- **Logical deduction** maps to **Systems design** and **Systems integration**: designing systems of medium risk and complexity, defining the integration build, and coordinating build activities across systems all require valid reasoning from constraints — dependency rules, environment availability, sequencing requirements — to their consequences.
- **Error checking** maps to **Programming and build (software engineering)**, **Information security**, and **Service support**: reviewing specifications and the systems designs of others, engineering security controls to mitigate specific threats, and identifying, locating and fixing service faults all depend on spotting the inconsistency others walked past.
- **Prioritisation** maps to your duty to plan and lead development on sets of related stories, to **Availability and capacity management** (managing service components to meet business needs and KPIs), and to **Service support**: when a fault, a review, a mentee, and a deadline compete, you must rank impact-weighted urgency rapidly and defensibly.
- **Applied problem solving** maps to **Development process optimisation** and your duty to find ways to improve system robustness, resilience and stability: given a messy situation — a flaky pipeline, an intermittent fault, a capacity ceiling — you decompose it, form hypotheses, and test them in a sensible order.

### Practice questions

**Question 1 (easy) — Pattern recognition in a naming convention**

Your team's coding standard requires environment configuration keys to follow the pattern `SERVICE_ENVIRONMENT_SETTING`, all upper case, separated by single underscores — for example `PAYMENTS_PROD_TIMEOUT`. While reviewing a pull request from a junior developer, you see these new keys:

1. `PAYMENTS_STAGING_RETRIES`
2. `PAYMENTS_PROD_MAX_CONNECTIONS`
3. `STAGING_PAYMENTS_TIMEOUT`
4. `PAYMENTS_DEV_LOGLEVEL`

Which key most clearly breaks the agreed pattern?

- A) Key 1
- B) Key 2
- C) Key 3
- D) Key 4

**Correct answer: C**

**Explanation:** The pattern fixes the order: service first, then environment, then setting. Key 3 inverts the first two elements — `STAGING` (an environment) appears where the service name belongs. Key 2 might look suspicious because the setting portion contains an underscore (`MAX_CONNECTIONS`), but the standard as stated constrains order and case, and a multi-word setting is the least-worst reading; the unambiguous violation is the inversion in key 3. This is exactly the consistency check you perform when you apply modern development standards and support others in applying them: conventions look trivial, but a config store where half the keys are inverted becomes unsearchable, and the reviewer who catches it in the pull request saves the on-call engineer an hour at 3am.

**Question 2 (easy) — Logical deduction from a deployment rule**

Your team's release policy states: "A change may be deployed to production only if the full test suite passes and the change has been reviewed by at least one other developer." A colleague tells you: "My change was deployed to production this morning." Which one of the following conclusions must be true?

- A) The full test suite passed and the change was reviewed by at least one other developer.
- B) The change was reviewed by you.
- C) The change contains no defects.
- D) The change was deployed using the automated pipeline.

**Correct answer: A**

**Explanation:** The policy makes passing tests and peer review necessary conditions for production deployment. If the deployment happened (and the policy was followed — which the question's framing assumes), both conditions must have held, so A must be true. B adds a detail the rule does not require — any other developer suffices. C confuses "tests passed" with "no defects": a passing suite only shows the absence of the failures it can detect, a distinction you rely on daily when you follow a test-driven approach. D introduces a mechanism the rule never mentions. Deduction questions reward exactly the discipline of a good code reviewer: conclude only what the stated rules guarantee, and treat everything else as merely possible.

**Question 3 (easy) — Error checking a log extract**

An API service logs each request as `timestamp | endpoint | status | duration_ms`. During fault investigation you scan this extract:

```
09:14:01 | /applications | 200 | 143
09:14:02 | /applications | 200 | 151
09:14:03 | /applications | 500 | 30012
09:14:04 | /applications | 200 | 139
09:14:05 | /applications | 200 | 30
```

The service's upstream dependency has a 30-second timeout. Which line most strongly suggests a dependency timeout rather than a fast application error?

- A) Line 2
- B) Line 3
- C) Line 4
- D) Line 5

**Correct answer: B**

**Explanation:** Line 3 pairs a 500 status with a duration of 30,012 milliseconds — almost exactly the 30-second upstream timeout plus a few milliseconds of handling. That signature (error status, duration pinned at the timeout ceiling) is the classic fingerprint of a dependency that never answered. Line 5's 30 milliseconds is fast and successful; a fast 500 would suggest an application-level failure such as an unhandled exception, but no such line appears. Reading durations against known timeout values is a core service support instinct: it tells you whether to look in your own code or at the dependency, which halves your search space before you open a single file. In an assessment, as in an incident, let the numbers point you to the layer at fault.

**Question 4 (moderate) — Deduction from integration constraints**

You are defining the integration build for three components: the case API (A), the document store adapter (D), and the notification service (N). Constraints: (i) D cannot be integrated before A, because D consumes A's contract; (ii) N must be integrated last; (iii) integration testing for each component takes one full day, one component per day; (iv) A's contract is frozen at the end of Monday, and no component may be integrated before its dependencies' contracts are frozen. Work begins Tuesday. What is the earliest day N's integration can complete?

- A) Wednesday
- B) Thursday
- C) Friday
- D) Tuesday

**Correct answer: B**

**Explanation:** Work the constraints forward. A's contract freezes end of Monday, so A can be integrated Tuesday. D depends on A, so D follows on Wednesday. N must be last, so N runs Thursday and completes that day. The tempting error is Friday, from assuming a buffer day between D and N that no constraint requires; another is Wednesday, from forgetting that D must precede N because N is last of three. This is the reasoning you use when you define the integration build and coordinate build activities across systems: the schedule falls out of the dependency rules, and the senior developer's job is to derive the tightest feasible sequence rather than pad every step "to be safe" — or promise a date the dependencies make impossible.

**Question 5 (moderate) — Pattern recognition in test failures**

Your continuous integration pipeline has run the same suite ten times against the same commit. The only failing test is `test_upload_large_file`, which failed on runs 2, 5, and 9 and passed on the others. The test uploads a 50 MB file to a shared staging object store and asserts completion within 20 seconds. Which explanation best fits the pattern?

- A) The code under test has a logic error that always produces the wrong result.
- B) The test is flaky, most likely due to variable staging environment performance against a fixed time limit.
- C) The test only fails when the code is broken, so the code was broken on runs 2, 5 and 9.
- D) The object store rejects files over 50 MB.

**Correct answer: B**

**Explanation:** A deterministic logic error (A) would fail all ten runs of the same commit. The commit did not change between runs, so C is impossible — the code cannot have been broken on three runs and fine on seven. A hard size limit (D) would also fail every run. The observed pattern — intermittent failures of a test that races a shared environment against a fixed timeout — is the signature of flakiness caused by environmental variance. The professional consequence matters: a flaky test erodes trust in the pipeline, and finding ways to improve robustness and stability includes making tests deterministic (isolating the dependency, adjusting the assertion, or measuring the right thing). In assessments, "what varies between the passing and failing cases?" is the question that cracks intermittent-pattern items; nothing varied in the code, so the cause lives in the environment.

**Question 6 (moderate) — Prioritisation across competing demands**

It is 09:30 on Tuesday. Four items compete for your attention as the senior developer on your team:

1. A production alert fired ten minutes ago: error rates on the citizen-facing application service have risen from 0.1% to 4% and are climbing.
2. A pull request from a junior developer you are mentoring has been waiting for your review since yesterday; they are blocked on it.
3. Sprint planning starts at 11:00 and you have not yet broken down the set of related stories you are leading.
4. A security patch for a library you use is due to be applied by the end of the week.

Which sequencing is most defensible?

- A) 2, 1, 3, 4 — unblock people first, then look at the alert
- B) 1, 2, 3, 4 — production incident first, then unblock your mentee, then prepare planning, then schedule the patch
- C) 3, 1, 2, 4 — planning has the nearest fixed start time
- D) 1, 4, 2, 3 — security always comes immediately after incidents

**Correct answer: B**

**Explanation:** Item 1 is a live, worsening production impact on a citizen-facing service — you operate the production services you build, and a climbing error rate is both urgent and high impact, so it comes first. Item 2 is next: a blocked mentee is a person-hour leak and a coaching moment, and a review is usually quick once the incident is stable. Item 3 has a fixed start but is preparation you can compress or, in a genuine emergency, ask to reschedule; it outranks item 4 only on urgency. Item 4 is important but has days of slack — the right move is to schedule it, not do it now. Option A delays incident response for a review, inverting impact; C treats a meeting's clock as more important than citizens experiencing errors; D promotes slack-rich work over deadline-near work by slogan ("security always") rather than reasoning. Prioritisation items reward impact-weighted urgency, and so does your role.

**Question 7 (moderate) — Error checking a systems design review**

You are reviewing a junior colleague's design for a document upload feature. The design states: (i) "Files are scanned for malware after being stored in the public-access bucket"; (ii) "Uploads are limited to 10 MB, enforced in the browser's JavaScript"; (iii) "The upload endpoint requires an authenticated session"; (iv) "Antivirus signatures update daily." Which statement pair reveals the most serious security flaw?

- A) (i) and (ii) — unscanned files are publicly accessible, and the size limit can be bypassed by any client that skips the browser code
- B) (iii) and (iv) — authentication and signature updates conflict
- C) (ii) and (iv) — the size limit makes daily updates pointless
- D) (i) and (iii) — scanning after storage is fine because the session is authenticated

**Correct answer: A**

**Explanation:** Two independent flaws combine here. Statement (i) stores files where the public can reach them before scanning — a window in which malware is served to citizens. Statement (ii) enforces the size limit only client-side; anyone driving the API directly (a script, a modified client) bypasses it entirely, so the server can receive arbitrarily large — and, combined with (i), publicly served — files. Statements (iii) and (iv) are individually reasonable and do not conflict; authentication does not sanitise content, so D's reasoning is exactly the false comfort a reviewer must reject. The fix pattern is the one your information security skill describes — design solutions with security controls engineered against specific threats: scan in quarantine before promotion to public storage, and enforce limits server-side with the client-side check kept only for user experience. Design reviews reward the reader who asks, of each control, "where is this actually enforced, and what reaches the user before it runs?"

**Question 8 (moderate) — Deduction about fault localisation**

A service fault has this evidence: (i) requests through the load balancer to instance 1 fail; (ii) requests through the load balancer to instance 2 succeed; (iii) requests sent directly to instance 1, bypassing the load balancer, succeed; (iv) instances 1 and 2 run identical code and configuration. Which component is the most logical location of the fault?

- A) The application code
- B) Instance 1's server hardware
- C) The load balancer's routing or health-check configuration for instance 1
- D) Instance 2

**Correct answer: C**

**Explanation:** Isolate by differencing. Identical code on both instances, and instance 1 succeeds when reached directly, so the application code and instance 1 itself are exonerated — ruling out A and B. Instance 2 works in all observed paths, ruling out D. The only path that fails is load balancer → instance 1, so the fault lies in that specific hop: most plausibly the load balancer's per-instance configuration — a stale backend registration, a wrong port, or a health check marking instance 1 unhealthy and misrouting or rejecting its traffic. This elimination pattern — vary one element of the path at a time and see which variation flips the outcome — is the core discipline behind your service support skill of identifying and locating faults before fixing them, and it is precisely what multi-clue deduction items test: each clue removes a suspect, and the answer is whoever survives every clue.

**Question 9 (challenging) — Multi-constraint scheduling of related stories**

You are planning four stories — Schema migration (S), API change (P), Frontend change (F), and Load test (L) — across a five-day week, at most one story completing per day. Constraints: (i) S must complete before P, because P reads the new schema; (ii) P must complete before F, because F calls the new API; (iii) L must run on the day immediately after F completes; (iv) the database administrator is available to support S only on Monday and Thursday. On which day must the load test run if the team wants the earliest possible finish?

- A) Wednesday
- B) Thursday
- C) Friday
- D) The plan cannot fit in one week

**Correct answer: B**

**Explanation:** For the earliest finish, take the earliest permitted slot for the first dependency: S needs the database administrator, available Monday or Thursday, so choose Monday. P must follow S, so P completes Tuesday at the earliest. F follows P: Wednesday. L must run the day immediately after F: Thursday. Check every constraint: S<P (Mon<Tue), P<F (Tue<Wed), L = F+1 (Thu = Wed+1), DBA on Monday — all satisfied, so Thursday is achievable and nothing earlier is (L cannot precede three predecessors each taking a day). Choosing Thursday for S — the other DBA slot — would push P to Friday and the rest out of the week, which is why option D tempts anyone who anchors on the wrong DBA day. This is precisely your planning duty: when you plan and lead development on sets of related stories, the critical path falls out of the dependencies, and the leader's job is to spot which scarce resource (here, the DBA) anchors the whole sequence.

**Question 10 (challenging) — Applied problem solving on capacity**

Your service runs 4 application instances. Monitoring shows each instance handles at most 120 requests per second (rps) before response times breach the KPI. Current peak traffic is 380 rps, spread evenly by the load balancer. A marketing campaign is expected to add 40% to peak traffic. Instances can only be added in pairs. To keep peak per-instance load at or below 120 rps during the campaign, how many instances must be running?

- A) 4
- B) 5
- C) 6
- D) 8

**Correct answer: C**

**Explanation:** Compute the campaign peak first: 380 × 1.40 = 532 rps. Divide by the per-instance ceiling: 532 ÷ 120 = 4.43, so at least 5 instances are needed (4 instances give 480 rps of headroom — insufficient for 532). But instances are added in pairs, so from 4 you can go to 6, not 5; 6 instances provide 6 × 120 = 720 rps of capacity, and per-instance load becomes 532 ÷ 6 ≈ 89 rps, comfortably below the ceiling. Option B ignores the pairing constraint; option D over-provisions beyond what any constraint requires. Notice the two-step discipline — first the arithmetic minimum, then the operational constraint that rounds it — because that is exactly how availability and capacity management works in practice: KPIs give you the maths, infrastructure gives you the granularity, and the answer must satisfy both.

**Question 11 (challenging) — Deduction from monitoring rules**

Your alerting rules state: (i) if CPU exceeds 80% for 5 minutes, a warning fires; (ii) if a warning is active and memory exceeds 90%, a critical alert fires; (iii) a critical alert always pages the on-call engineer; (iv) no page was sent in the last hour. Assuming the rules operated correctly, which of the following must be true about the last hour?

- A) CPU never exceeded 80%.
- B) Memory never exceeded 90%.
- C) At no time was a warning active while memory exceeded 90%.
- D) The service was healthy.

**Correct answer: C**

**Explanation:** Reason backwards through the chain (contrapositive reasoning). No page (iv) means no critical alert, because a critical alert always pages (iii). No critical alert means the trigger in (ii) never occurred: there was never a moment when a warning was active and memory exceeded 90% — which is exactly option C. A is too strong: CPU could have exceeded 80% and even fired a warning, so long as memory stayed at or below 90% while the warning was active. B is likewise too strong: memory could have spiked while no warning was active. D ("healthy") is an informal judgement the rules cannot ground — an unpaged hour can still contain degraded performance. This is the same backward reasoning you use in service support when the absence of an alert is itself evidence: silence tells you precisely which conjunctions of conditions did not occur, and nothing more.

**Question 12 (challenging) — Error checking an intermittent defect report**

Users report that a "save draft" feature occasionally loses data. You gather these facts: (i) losses only occur for users with two browser tabs open on the same draft; (ii) the save endpoint writes the full draft, overwriting the stored version; (iii) each tab autosaves every 60 seconds, timed from when that tab loaded; (iv) the server processes saves strictly in arrival order. Which mechanism best explains the data loss?

- A) The server sometimes processes saves out of order, corrupting drafts.
- B) A stale tab's autosave overwrites the newer content saved by the other tab — a lost-update race between tabs.
- C) The 60-second timer is too infrequent, so unsaved work is lost on browser crashes.
- D) The database intermittently rejects large drafts.

**Correct answer: B**

**Explanation:** Test each candidate against every fact. A contradicts fact (iv) — order is strict. C would cause losses for single-tab users too, contradicting fact (i), and involves crashes the report never mentions. D likewise has no link to the two-tab condition. B fits all four: two tabs autosave on independent clocks (iii); each save overwrites the whole draft (ii); so a tab holding stale content can arrive after the tab holding fresh edits and, processed in arrival order, replace new data with old — classic lost update. Note the technique: the distinguishing fact is (i), the condition that separates affected from unaffected users, and the correct mechanism must use it. This is applied problem solving exactly as your role practises it — the fix (optimistic locking, per-field merging, or a version check on save) follows directly once the mechanism is named, which is why fault diagnosis questions reward mechanism-first thinking over plausible-sounding blame.

### Preparation tips

- **Practise on your own artefacts.** Ten minutes with yesterday's pull requests, pipeline runs, or alert history is job-realistic cognitive training: ask "what pattern holds here, and what breaks it?" The materials in the real assessment will feel familiar because they are modelled on materials like yours.
- **Rehearse constraint chains aloud.** Integration and scheduling questions are dependency graphs in prose. Practise translating "X cannot start until Y finishes" into a quick sketch — even in a timed test, five seconds of diagram saves thirty seconds of re-reading.
- **Separate "must be true" from "probably true".** Senior engineers live on plausible inference, but deduction items punish it. Before selecting an answer, ask: is there any scenario consistent with the facts where this is false? If yes, it is not a "must".
- **Time-box per question.** With 20 questions in 25 minutes, budget roughly 70 seconds each; bank time on easy pattern items to spend on multi-constraint ones. Flag and move on rather than sinking — exactly as you would time-box a spike.
- **Do a systems check before you start.** Quiet room, stable connection, browser updates done, notifications silenced. You would not deploy from a laptop mid-update; do not test from one either.
- **Sleep beats cramming.** Cognitive throughput is the thing being measured, and it is the thing sleep restores. The night before matters more than the hour before.

### Common pitfalls to avoid

- **Pattern-matching from experience instead of the stem.** You have seen a hundred flaky tests, so you may leap to the familiar diagnosis before checking it against the facts given. The question's world is the facts in the stem — answer that world, not your last incident.
- **Over-engineering easy questions.** Senior developers are trained to find edge cases, and some candidates talk themselves out of correct answers by inventing complications the question never states. If the simple reading satisfies every stated fact, take it.
- **Confusing "tests pass" with "correct".** Several items exploit the gap between evidence and proof. Keep the distinction sharp: a green pipeline, a silent pager, and an authenticated session each guarantee less than they imply.
- **Losing the thread in multi-constraint items.** Errors come from holding four constraints in your head at once. Externalise: jot the sequence, tick each constraint against your candidate answer before committing — the same habit as checking every acceptance criterion before merging.
- **Ignoring stated granularity.** Real-world constraints like "instances are added in pairs" or "one story per day" change the answer from the pure arithmetic one. Read the operational constraints as carefully as the numbers.
- **Rushing the last questions.** Adaptive tests put your hardest questions late, when fatigue peaks. Keep a steady cadence, and if you must guess, eliminate the options that contradict a stated fact first — that alone usually removes two.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment measures your ability to interpret, manipulate, and draw sound conclusions from numerical information of the kind your role genuinely produces and consumes. For a senior developer, that is not accountancy: it is service metrics. You will work with error rates and availability percentages, request throughput and capacity headroom, build durations and deployment frequencies, story estimates and velocity, defect counts and trends — presented in tables, charts, and short scenarios.

Typical format: an online, timed test of 20 to 35 minutes with 15 to 25 questions. Each question presents a small data set — a monitoring table, a sprint burndown, a cost breakdown — and asks for a specific computation or interpretation: a percentage change, a ratio, a weighted average, a rate, a projection. Calculators are usually permitted (and sometimes built into the platform), because the assessment targets reasoning rather than mental arithmetic: choosing the right operation, the right denominator, and the right level of scepticism. Questions are multiple choice, and wrong options are engineered from predictable mistakes — the inverted ratio, the percentage of the wrong base, the average of averages — so accuracy of method matters more than speed of keystrokes.

Why do employers use numeric assessment for senior developer roles? Because at your level, numbers are how the system talks to you and how you talk to the business. You manage service components to ensure they meet business needs and key performance indicators — KPIs are numbers. You find ways to improve robustness, resilience and stability — improvement is demonstrated numerically or not at all. You plan and lead development on sets of related stories — plans are estimates, and estimates are arithmetic under uncertainty. You operate production services — operating means reading dashboards correctly at 2am, when the difference between "errors doubled from 0.1% to 0.2%" and "errors doubled from 10% to 20%" determines whether anyone should be awake. A senior developer who misreads a denominator can page a team for nothing, under-provision a launch, or tell a service owner a fix worked when it did not. The assessment samples exactly these risks in miniature.

The test is also, quietly, a fairness device: it lets a candidate who is stronger at systems than at self-promotion demonstrate rigour objectively. Practising restores familiarity with computations you do implicitly every week but rarely on paper, so the format does not obscure ability you already have.

### How this assessment maps to your role

- **Percentages, rates, and availability arithmetic** map to **Availability and capacity management**: KPIs arrive as percentages (availability, error rate, cache hit ratio) and rates (requests per second, incidents per month). Managing service components against KPIs means converting between counts and rates without slipping a denominator.
- **Ratios and proportional scaling** map to **Systems design** and **Systems integration**: sizing components, splitting traffic between systems, and reasoning about efficient use of resources during design review all reduce to proportional reasoning.
- **Averages, trends, and projections** map to your duty to plan and lead development on sets of related stories and to **Development process optimisation**: velocity, cycle time, and build duration are averages over noisy data, and process improvement claims stand or fall on whether the trend is real.
- **Reading tables and charts under pressure** maps to **Service support**: identifying and locating faults usually begins with a dashboard, and the first skill is extracting the one number that matters from twelve that do not.
- **Cost and resource arithmetic** maps to **Information security** and robustness work: security and resilience improvements compete for budget, and the senior developer who can quantify "what does this mitigation cost against what expected loss?" wins the argument. It also supports **User focus** — for example, quantifying how many real users an accessibility defect affects turns advocacy into evidence.

### Practice questions

**Question 1 (easy) — Error rate as a percentage**

Yesterday your service handled 250,000 requests, of which 1,250 returned errors. What was the error rate?

- A) 0.05%
- B) 0.5%
- C) 5%
- D) 1.25%

**Correct answer: B**

**Explanation:** Error rate = errors ÷ total requests × 100. Step by step: 1,250 ÷ 250,000 = 0.005. Multiply by 100 to express as a percentage: 0.5%. Option A drops a factor of ten (0.05% would be 125 errors); option C multiplies wrongly by 1,000 (5% would be 12,500 errors); option D is the raw error count with a percent sign attached — a classic trap. A quick sanity check catches all three: 1% of 250,000 is 2,500, and 1,250 is half of that, so the answer must be half of 1%. Sanity-checking against an easy reference percentage is the single most useful habit in dashboard arithmetic, and it takes two seconds.

**Question 2 (easy) — Availability from downtime**

Your service's KPI is 99.5% monthly availability. In a 30-day month (720 hours), the service was down for a total of 5 hours. Did you meet the KPI, and what was the actual availability?

- A) Yes — availability was 99.31%
- B) No — availability was 99.31%
- C) Yes — availability was 99.5%
- D) No — availability was 98.6%

**Correct answer: B**

**Explanation:** Uptime = 720 − 5 = 715 hours. Availability = 715 ÷ 720 = 0.99306, i.e. 99.31% (to two decimal places). The KPI requires 99.5%, and 99.31% falls short, so the KPI was missed. Useful cross-check: 99.5% of 720 hours permits 0.5% × 720 = 3.6 hours of downtime; 5 hours exceeds the 3.6-hour budget, confirming the miss without computing the availability at all. Option A computes correctly but concludes wrongly; option D miscalculates (98.6% would imply about 10 hours down). Knowing your downtime budget in hours — 3.6 hours per month at 99.5%, about 22 minutes at 99.95% — is practical availability management: it converts an abstract KPI into an operational allowance you can track mid-month.

**Question 3 (easy) — Sprint velocity average**

Over the last four sprints your team completed 34, 28, 38, and 32 story points. Planning assumes velocity equals the four-sprint average. What velocity should you plan with?

- A) 30
- B) 32
- C) 33
- D) 34

**Correct answer: C**

**Explanation:** Sum the points: 34 + 28 = 62; 62 + 38 = 100; 100 + 32 = 132. Divide by the number of sprints: 132 ÷ 4 = 33. Option B is the median-looking middle value and also the most recent sprint — both tempting shortcuts; option D anchors on the first number. Two professional notes worth carrying into planning. First, the mean hides spread: a range of 28–38 means a plan of 33 will be under-delivered roughly half the time, so commit conservatively when the downside matters. Second, never average percentages or averages of unequal groups the same way — that error appears later in this section. Here the four sprints are equal periods, so the simple mean is legitimate.

**Question 4 (moderate) — Percentage change in build duration**

You optimised the continuous integration pipeline. Average build duration fell from 24 minutes to 18 minutes. Your team runs about 40 builds per working day. What was the percentage reduction in build duration, and roughly how much build time is saved per day?

- A) 25% reduction; 240 minutes saved per day
- B) 33% reduction; 240 minutes saved per day
- C) 25% reduction; 180 minutes saved per day
- D) 6% reduction; 40 minutes saved per day

**Correct answer: A**

**Explanation:** Percentage reduction uses the original value as the base: (24 − 18) ÷ 24 = 6 ÷ 24 = 0.25 = 25%. Option B commits the classic base error, dividing the change by the new value (6 ÷ 18 = 33%) — percentage change is always relative to where you started. Daily saving: 6 minutes saved per build × 40 builds = 240 minutes, i.e. 4 hours of pipeline time per day. Option C multiplies the new duration rather than the saving. This is exactly the arithmetic of development process optimisation: when you contribute to implementing a proposed improvement, quantifying the benefit ("four pipeline-hours a day") is what turns a nice-to-have into a funded piece of work — and using the wrong base would overstate your own improvement by a third, which an informed stakeholder will catch.

**Question 5 (moderate) — Capacity headroom ratio**

A service component currently processes a peak of 450 messages per second (mps) against a tested maximum of 600 mps. A new consumer is about to be integrated and is forecast to add 90 mps at peak. After integration, what percentage of tested maximum capacity will be in use at peak?

- A) 75%
- B) 82%
- C) 90%
- D) 96%

**Correct answer: C**

**Explanation:** New peak load = 450 + 90 = 540 mps. Utilisation = 540 ÷ 600 = 0.90 = 90%. Option A is the utilisation before integration (450 ÷ 600); option B misadds; option D divides by a misremembered maximum. The follow-on judgement is the real skill: 90% utilisation leaves 10% headroom, which most availability and capacity guidance treats as inadequate for a component with bursty traffic — a modest spike breaches the ceiling. The arithmetic answers "what will utilisation be?"; the senior developer then asks "is that acceptable against our KPIs, and if not, do we scale before or after integration?" In a real design review of this integration, computing 90% is the start of the conversation, not the end — and in the assessment, expect a paired question exactly like our next one.

**Question 6 (moderate) — Weighted average response time**

Your service has two endpoints. `/search` served 300,000 requests last week with a mean response time of 200 ms. `/submit` served 100,000 requests with a mean response time of 600 ms. What was the overall mean response time across both endpoints?

- A) 400 ms
- B) 300 ms
- C) 350 ms
- D) 250 ms

**Correct answer: B**

**Explanation:** You cannot simply average 200 and 600 (that gives option A, 400 ms) because the endpoints served different volumes — the simple average of averages is the assessment's favourite trap. Weight each mean by its request count. Total time = (300,000 × 200) + (100,000 × 600) = 60,000,000 + 60,000,000 = 120,000,000 ms. Total requests = 400,000. Overall mean = 120,000,000 ÷ 400,000 = 300 ms. Intuition check: three-quarters of the traffic ran at 200 ms and one quarter at 600 ms, so the answer sits a quarter of the way from 200 towards 600 — exactly 300. This matters operationally: dashboards that average per-endpoint means mislead exactly this way, and a senior developer reviewing a "mean latency improved" claim should always ask whether the traffic mix changed rather than the endpoints themselves.

**Question 7 (moderate) — Defect trend interpretation**

Your team tracks defects found in production per month: January 12, February 9, March 15, April 6, May 8, June 4. A stakeholder says "defects fell every month." Which statement is the most accurate correction?

- A) Defects rose overall — June is higher than January.
- B) The claim is correct.
- C) Defects fell overall — June is a third of January — but not monotonically: March rose against February, and May rose against April.
- D) No trend can ever be inferred from six data points.

**Correct answer: C**

**Explanation:** Check the claim against each consecutive pair: 12→9 fell, 9→15 rose, 15→6 fell, 6→8 rose, 8→4 fell. Two months rose, so "fell every month" is false — but the overall movement, from 12 down to 4 (a 67% reduction: (12 − 4) ÷ 12 = 8 ÷ 12 ≈ 0.67), is clearly downward. Option C captures both truths. Option A misreads the endpoints; option D overcorrects into nihilism — six points cannot prove a trend statistically, but they can certainly falsify "every month", and describing the pattern accurately is not the same as claiming significance. This is the precision your role demands when robustness improvements are reviewed: report the genuine improvement, and correct the overclaim before someone else does, because a stakeholder who catches one exaggeration discounts your next three accurate claims.

**Question 8 (moderate) — Storage growth projection**

A database currently holds 1.2 TB and is growing by 75 GB per month. The storage volume is provisioned at 2.0 TB, and your team's standard is to expand storage before utilisation reaches 90%. Using 1 TB = 1,000 GB, in how many months must the expansion be completed?

- A) 6 months
- B) 8 months
- C) 10 months
- D) 12 months

**Correct answer: B**

**Explanation:** The 90% threshold on a 2.0 TB volume is 0.9 × 2,000 GB = 1,800 GB. Current usage is 1,200 GB, so the remaining allowance before the threshold is 1,800 − 1,200 = 600 GB. At 75 GB per month: 600 ÷ 75 = 8 months. Option C computes time to fill the whole volume (800 ÷ 75 ≈ 10.7, rounded optimistically); option A over-applies caution without arithmetic; option D misreads the threshold as 100% and rounds. The professional pattern: capacity planning always projects to the action threshold, not to the cliff edge — the 90% standard exists because expansion takes lead time and growth is not perfectly linear. In the assessment, read carefully whether the question asks time-to-threshold or time-to-full; both will be among the options.

**Question 9 (challenging) — Comparing failure rates fairly**

Two deployment pipelines are compared over a quarter. Pipeline Alpha ran 1,600 deployments with 48 failures. Pipeline Beta ran 250 deployments with 10 failures. A colleague argues Beta is more reliable "because it failed only 10 times against Alpha's 48." What are the failure rates, and is the colleague's reasoning sound?

- A) Alpha 3%, Beta 4% — the reasoning is unsound because it compares counts, not rates; Alpha is more reliable per deployment
- B) Alpha 3%, Beta 4% — the reasoning is sound because fewer failures is always better
- C) Alpha 4%, Beta 3% — the reasoning is sound
- D) Alpha 0.3%, Beta 0.4% — the reasoning is unsound

**Correct answer: A**

**Explanation:** Alpha: 48 ÷ 1,600 = 0.03 = 3%. Beta: 10 ÷ 250 = 0.04 = 4%. Beta fails more often per deployment despite fewer absolute failures, because it runs far less. Comparing raw counts across different denominators is the base-rate error, and it is endemic in engineering discussions — "that service pages us most" often just means "that service is biggest". Option D slips a decimal place (0.3% of 1,600 would be about 5 failures, not 48 — the sanity check catches it). Two further professional cautions: with only 250 runs, Beta's rate carries more statistical noise, so the gap may not be meaningful; and failure severity may differ. The assessment wants the rate comparison; the senior developer reviewing a process optimisation proposal should want all three considerations before declaring a winner.

**Question 10 (challenging) — Percentile versus mean latency**

A performance test returns these response times for ten requests, in milliseconds: 90, 95, 100, 100, 105, 110, 110, 115, 120, 1,955. Your KPI is "95th percentile response time under 500 ms" and a teammate reports "mean response time 290 ms — we pass." What is the mean, and does the service pass the KPI?

- A) Mean 290 ms; passes, because 290 < 500
- B) Mean 290 ms; fails, because the 95th percentile is driven by the 1,955 ms outlier, which exceeds 500 ms
- C) Mean 105 ms; passes comfortably
- D) Mean 290 ms; cannot be determined

**Correct answer: B**

**Explanation:** Mean: sum = 90+95+100+100+105+110+110+115+120+1,955 = 2,900; 2,900 ÷ 10 = 290 ms — the teammate's arithmetic is right. But the KPI is a percentile, not a mean. With ten ordered values, the 95th percentile sits at or beyond the 9.5th position — between 120 and 1,955, and on any standard method well above 500 ms once the outlier is included (the largest value alone represents the worst 10% of requests, so the worst 5% is at least 1,955 ms). The service fails. The mean of 290 ms is a textbook demonstration of why tail-sensitive KPIs exist: nine users had a fine experience and one waited two seconds, and the mean splits the difference into a number no user experienced. When you manage components against KPIs, always compute the statistic the KPI names — and when you review others' performance claims, the first question is "mean or percentile?"

**Question 11 (challenging) — Cost of resilience options**

To improve resilience you compare two options for a component that currently causes an estimated £4,000 of productivity loss per outage, with 6 outages expected per year. Option 1: active-passive failover costing £800 per month to run, expected to prevent 80% of outage impact. Option 2: re-architecture costing a one-off £18,000, expected to prevent 95% of outage impact, with no ongoing cost. Over a single year, which option has the better net saving?

- A) Option 1, saving £9,600 net
- B) Option 2, saving £4,800 net
- C) Option 1, saving £19,200 net
- D) Both save the same

**Correct answer: A**

**Explanation:** Annual outage impact without action: 6 × £4,000 = £24,000. Option 1: prevents 80% of £24,000 = £19,200; annual cost = £800 × 12 = £9,600; net saving = £19,200 − £9,600 = £9,600. Option 2: prevents 95% of £24,000 = £22,800; cost £18,000 in year one; net saving = £22,800 − £18,000 = £4,800. Over one year, Option 1's £9,600 beats Option 2's £4,800 — so A. Option C reports Option 1's gross benefit, forgetting its running cost — the most common error in benefits arithmetic. The horizon caveat is the senior insight: in year two, Option 2 costs nothing further and saves £22,800 against Option 1's recurring £9,600 net, so the ranking flips. State your time horizon before you state your recommendation; assessments (and finance colleagues) both test for it.

**Question 12 (challenging) — Reading a table of integration test results**

Integration testing across three systems produced this table of test outcomes:

| System pair | Tests run | Passed | Failed |
|---|---|---|---|
| API ↔ Database | 240 | 228 | 12 |
| API ↔ Frontend | 180 | 171 | 9 |
| API ↔ Notifications | 80 | 68 | 12 |

Which system pair has the highest failure rate, and what is the overall failure rate across all tests?

- A) API ↔ Notifications at 15%; overall 6.6%
- B) API ↔ Database at 5%; overall 6.6%
- C) API ↔ Notifications at 15%; overall 11.7%
- D) API ↔ Frontend at 5%; overall 5%

**Correct answer: A**

**Explanation:** Compute each pair's rate. Database: 12 ÷ 240 = 5%. Frontend: 9 ÷ 180 = 5%. Notifications: 12 ÷ 80 = 15% — the highest, despite failing the same absolute number as the Database pair (the base-rate lesson again). Overall: total failed = 12 + 9 + 12 = 33; total run = 240 + 180 + 80 = 500; 33 ÷ 500 = 0.066 = 6.6%. Option C wrongly averages the three rates ((5 + 5 + 15) ÷ 3 ≈ 8.3, and 11.7 miscomputes even that) instead of pooling counts — rates combine through their underlying totals, never by averaging, unless every group is the same size. For you, the numbers also carry the diagnostic: Notifications is the pair to investigate before coordinating further build activity, because a 15% failure rate on the smallest test suite suggests either an unstable integration or thin, brittle test coverage — both worth knowing before go-live.

### Preparation tips

- **Rebuild fluency with a few core moves.** Percentage change (always over the original base), weighted averages (weight by volume), rates (count ÷ denominator ÷ time), and projections to a threshold cover most questions. Drill these until choosing the operation is automatic and only the arithmetic remains.
- **Use your own dashboards as a practice set.** Take last month's monitoring data and ask: what was our real availability? Our weighted mean latency? Our failure rate per deployment? You will practise the exact computations and learn your service's numbers — doubly useful.
- **Estimate before you calculate.** A rough order-of-magnitude guess ("about half of one percent") catches slipped decimal places, the most common error under time pressure. Every worked example above includes a sanity check; make that your reflex.
- **Read the question's statistic precisely.** Mean or percentile? Rate or count? Time-to-threshold or time-to-full? Percentage of which base? Half the wrong options exist because a plausible misreading produces them.
- **Practise with the tools you'll have.** If the platform provides an on-screen calculator, practise with one; if you'll use your own, have it ready. Fumbling an unfamiliar interface costs more time than any calculation.
- **Keep units visible.** Write GB or ms or rps next to intermediate results. Unit discipline prevents the classic errors — mixing minutes with hours, TB with GB — and it is the same discipline that stops production capacity mistakes.

### Common pitfalls to avoid

- **Averaging averages.** The single most exploited error: combining per-group means or rates without weighting by group size. If groups differ in size, pool the underlying counts.
- **Wrong percentage base.** "Reduced from 24 to 18" is a 25% reduction, not 33%. Change ÷ original, always. Conversely, a 25% fall followed by a 25% rise does not return you to the start.
- **Counts versus rates.** "Fewer failures" means nothing without the denominator. Whenever two things are compared, your first question is whether the denominators match.
- **Ignoring stated operational constraints.** Instances in pairs, expansion before 90%, budgets per year — the realistic constraint moves the answer away from the naive calculation, and the naive calculation is always among the options.
- **Answering the computation you expected.** Under time pressure candidates compute the familiar statistic (mean, total) instead of the one asked (percentile, per-unit rate). Re-read the final sentence of the question before answering.
- **Abandoning scepticism.** Some questions embed a flawed claim from a colleague or stakeholder. Your job is the accurate correction — neither endorsing the error nor overcorrecting into "nothing can be known". Precision, not politeness or nihilism.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment measures how accurately you extract meaning from written material of the kind your role actually handles — and how disciplined you are about the difference between what a text says, what it implies, and what it simply does not address. For a senior developer, the passages are not literary: they are extracts from technical standards and service manuals, security policies, incident reports, API documentation, supplier emails, and specification documents. The questions come in familiar forms: true/false/cannot-say judgements against a passage, closest-meaning and inference items, and clear-writing questions that ask which sentence conveys a technical point most effectively.

Typical format: an online, timed test of 15 to 25 minutes with 20 to 30 questions grouped under short passages. The central rule is strict: answer only from the passage. "True" means the passage states it or it follows necessarily; "False" means the passage contradicts it; "Cannot say" means the passage provides insufficient information either way — even if you, as a working engineer, happen to know the claim is correct in real life. This is harder for experts than novices, because your professional knowledge keeps volunteering answers the passage never gave. Scoring is objective, and adaptive platforms may raise passage complexity as you succeed.

Why does this matter for a senior developer? Because your role runs on precise reading and precise writing. You collaborate with others to review specifications, and a specification misread is a defect shipped. You use agreed specifications to design, code, test and document programs — "agreed" means the words on the page are the contract, and your test-driven approach turns those words directly into assertions. You apply modern development standards and support others in applying them, which means reading standards closely enough to know what they mandate, what they recommend, and what they leave open — the difference between "must", "should", and "may" is a verbal reasoning question you answer every week. You work with other disciplines to understand what needs to be built, translating between user researchers, designers, and product colleagues whose words carry different assumptions. And you write: documentation that must be easy for others to reuse, code review comments that must land without bruising, incident summaries that must be accurate under scrutiny. Employers assess verbal reasoning at senior level because the cost of imprecise reading scales with responsibility: a junior misreads a ticket and loses an afternoon; a senior misreads a security policy and the service fails an audit.

Practising this assessment type sharpens a skill you already exercise, and the transfer is direct: candidates routinely report that "cannot say" discipline improves their specification reviews within a week.

### How this assessment maps to your role

- **Comprehension of technical passages** maps to **Programming and build (software engineering)**: reviewing and implementing agreed specifications depends on extracting exactly what the specification commits to — data formats, error behaviour, boundary conditions — and nothing more.
- **True/false/cannot-say discipline** maps to **Systems design** and your review duty: when you review the systems designs of others, you must separate what the design document establishes from what its author assumes; unfounded "true" judgements in review become unfounded architecture in production.
- **Inference and modal-verb precision** maps to **Modern development standards** and **Information security**: standards and security policies are written in careful modal language — must, should, may, unless — and applying them (and supporting others to apply them) means reading that language exactly. Misreading "should" as "must" blocks teams needlessly; misreading "must" as "should" fails audits.
- **Comprehension of user-facing and cross-disciplinary language** maps to **User focus**: explaining the difference between user needs and user desires is a verbal act; representing users internally means reading research findings without projecting your own preferences onto them.
- **Clear-writing judgement** maps to your duties to document programs, create code that is open by default and easy for others to reuse, and teach the whole system to others: choosing the clearest sentence in an assessment mirrors choosing the clearest README, commit message, or incident update in your work. It also supports **Service support**, where an ambiguous status update during an incident multiplies confusion at the worst moment.

### Practice questions

**Passage 1 (for Questions 1–3).** From a departmental development standard: "All new services must expose health-check endpoints. Health-check endpoints should not require authentication, unless the endpoint reveals internal configuration details, in which case authentication is mandatory. Teams may additionally expose a detailed diagnostics endpoint; where provided, it must be authenticated. Existing services are expected to adopt this standard at their next major release."

**Question 1 (easy) — True/false/cannot-say**

Statement: "Under the standard, a new service without any health-check endpoint is non-compliant."

- A) True
- B) False
- C) Cannot say

**Correct answer: A**

**Explanation:** The passage states "All new services must expose health-check endpoints." "Must" is mandatory language, so a new service lacking one breaches the standard — the statement follows necessarily and is True. Note what makes this easy: the claim tracks a single "must" clause with no exceptions attached. The skill being rehearsed is the one you use when you support others in applying modern development standards — knowing which clauses are mandatory is the foundation for telling a team "this will block your release" versus "this is advice".

**Question 2 (moderate) — True/false/cannot-say with modal language**

Statement: "Under the standard, an unauthenticated health-check endpoint that reveals internal configuration details is non-compliant."

- A) True
- B) False
- C) Cannot say

**Correct answer: A**

**Explanation:** Track the conditional: health checks "should not require authentication, unless the endpoint reveals internal configuration details, in which case authentication is mandatory." The "unless... mandatory" clause converts the recommendation into a requirement precisely when configuration details are revealed. An endpoint that reveals such details and lacks authentication violates a mandatory clause, so the statement is True. The trap is the surrounding "should", which primes some candidates to answer Cannot say on the grounds that "should" is advisory — but the exception clause escalates to "mandatory" in exactly this case. Security policies are drafted in this layered way constantly, and your information security skill — designing controls that mitigate specific threats — begins with reading which controls are actually required, and when.

**Question 3 (moderate) — True/false/cannot-say on scope**

Statement: "An existing service that has not adopted the standard is currently in breach of it."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** The passage sets a different obligation for existing services: they "are expected to adopt this standard at their next major release." Until that release, non-adoption is anticipated by the standard itself — the compliance trigger is the next major release, which the statement's "currently" has not established has occurred. The passage therefore contradicts the claim that mere non-adoption today is a breach, making the statement False rather than Cannot say. This is the transition-clause reading you need whenever a new standard lands mid-flight: telling an existing team they are "in breach" when the standard grants them until their next major release both misreads the text and spends your credibility — the reviewer's equivalent of a false-positive alert.

**Passage 2 (for Questions 4–6).** From an incident report: "At 14:02 the payment provider began returning intermittent HTTP 503 responses. Our retry logic resubmitted failed payments up to three times. Because the idempotency key was regenerated on each retry rather than reused, some citizens were charged more than once. Duplicate charges affected 211 transactions before we disabled retries at 14:41. The provider restored normal service at 15:10. All duplicate charges were refunded within 24 hours."

**Question 4 (easy) — Comprehension**

According to the passage, what caused citizens to be charged more than once?

- A) The payment provider's 503 responses charged citizens directly.
- B) Retries were sent with a regenerated idempotency key instead of a reused one, so resubmissions were processed as new payments.
- C) Retries were disabled too early.
- D) The provider restored service too slowly.

**Correct answer: B**

**Explanation:** The causal sentence is explicit: "Because the idempotency key was regenerated on each retry rather than reused, some citizens were charged more than once." The 503s triggered the retries but did not themselves charge anyone — a 503 is a failure to respond successfully, and the passage attributes duplication to key regeneration, not to the provider's error responses. Options C and D describe response actions and provider recovery, neither offered as the cause. Comprehension items reward finding the passage's own causal claim rather than a plausible neighbour. In incident review — a core service support activity — this same precision determines the fix: reuse the key (correct) versus abandon retries entirely (overreaction to a misread cause).

**Question 5 (moderate) — True/false/cannot-say**

Statement: "The duplicate-charge defect was fully resolved by 15:10, when the provider restored normal service."

- A) True
- B) False
- C) Cannot say

**Correct answer: C**

**Explanation:** Separate the threads. The provider's outage ended at 15:10 — stated. Retries were disabled at 14:41 — stated, which stopped new duplicates. Refunds completed within 24 hours — stated. But the defect — regenerating idempotency keys on retry — is never said to have been fixed at all, let alone by 15:10; disabling retries suppresses the symptom without correcting the code. The passage neither confirms nor denies a code fix, so the statement is Cannot say. Candidates who answer True have merged three timelines into one comforting resolution; candidates who answer False have assumed the fix definitely had not happened by then, which the passage also does not establish. Holding parallel threads apart — outage, mitigation, remediation, refund — is exactly how a senior developer reads (and writes) a post-incident report.

**Question 6 (moderate) — Inference**

Which of the following can be validly inferred from the passage?

- A) The retry logic had never been tested.
- B) At most 211 transactions were retried.
- C) Correct reuse of idempotency keys would have made retries safe from duplicate charging.
- D) The provider breached its service-level agreement.

**Correct answer: C**

**Explanation:** The passage's causal structure supports C: duplication occurred because keys were regenerated "rather than reused" — the contrast identifies reuse as the safe behaviour, which is precisely what idempotency keys are for, and the inference stays within the passage's own logic. A is unsupported — a defect's existence does not establish absence of testing. B inverts the arithmetic: 211 transactions suffered duplicates, but more than 211 may have been retried without duplication (a retry could also simply fail again). D imports an SLA the passage never mentions. Inference questions reward the conclusion the text's own reasoning licenses, and reject conclusions that merely feel adjacent. The professional parallel is writing the "what would have prevented this" section of an incident review: the evidence must carry the counterfactual, or reviewers will pull it apart.

**Passage 3 (for Questions 7–9).** From an email sent by a supplier's account manager: "Following the upgrade, some API consumers may experience elevated latency for up to 48 hours while caches warm. We recommend consumers implement exponential backoff. Consumers who have already implemented backoff in line with our integration guide need take no further action. Please note that requests exceeding 10 per second per client will be throttled during this period; this limit may be revised without notice."

**Question 7 (easy) — Comprehension of obligations**

Your service already implements exponential backoff in line with the supplier's integration guide. According to the email, what must your team now do?

- A) Implement exponential backoff again.
- B) Nothing further is required by the email.
- C) Reduce all traffic below 10 requests per second permanently.
- D) Contact the supplier to confirm the upgrade.

**Correct answer: B**

**Explanation:** The email states that consumers who have already implemented backoff per the guide "need take no further action." Your team matches that description, so B follows directly. C over-reads the throttling note: the 10 rps limit applies "during this period" — the cache-warming window — not permanently, and the email imposes awareness of throttling rather than a duty to change traffic (though prudent engineering might). D invents an obligation nowhere stated. Reading supplier communications for the precise obligations they create is routine senior work during systems integration: teams waste real effort re-implementing what they already have, or miss genuine required actions, because someone skimmed an email like this one and reported it inaccurately at stand-up.

**Question 8 (moderate) — True/false/cannot-say**

Statement: "The 10 requests per second throttling limit will remain in force for exactly 48 hours."

- A) True
- B) False
- C) Cannot say

**Correct answer: C**

**Explanation:** Two durations are mentioned and they are not tied together as the statement requires. Elevated latency may last "up to 48 hours" — a maximum, not an exact duration. Throttling applies "during this period", most naturally the cache-warming window, but the email adds that the limit "may be revised without notice", explicitly unsettling any fixed duration. The passage therefore neither confirms an exact 48-hour term (so not True) nor states a different term that contradicts it (so not False): Cannot say. Words like "up to", "may", and "without notice" are load-bearing; treating "up to 48 hours" as "for 48 hours" is the same misreading that turns a supplier's hedge into a promise in your own status reports — and then into your problem when hour 30 arrives and the limit changes.

**Question 9 (challenging) — Clear-writing judgement**

You must add a line to your service's operational notes summarising the supplier email for on-call engineers. Which version is best?

- A) "Supplier upgrade may cause elevated latency for up to 48 hours from [date/time]; clients exceeding 10 rps may be throttled during this window (limit subject to change). Our backoff already complies; no action needed unless latency persists beyond the window."
- B) "The supplier has upgraded and things might be slow for a bit. Should be fine."
- C) "URGENT: supplier outage in progress. All traffic will be throttled at 10 rps forever. Implement backoff immediately."
- D) "Following the recent supplier-side infrastructure upgrade activity, it is possible that certain API-consuming components could potentially experience some degree of elevated response-time characteristics for a period not exceeding approximately 48 hours."

**Correct answer: A**

**Explanation:** Judge each against what an on-call engineer at 2am needs: what changed, what they might observe, what to do, and when to worry. A delivers all four accurately and concisely, preserves the two crucial hedges ("up to", "subject to change"), and states the action position ("no action needed unless..."). B is accurate-ish but useless — no numbers, no window, no action guidance. C is actively wrong three times (no outage is in progress, the limit is not permanent, backoff is already implemented) — urgency without accuracy is the most dangerous style in operational writing. D is the passage's meaning buried in hedging noise ("possible... potentially... some degree of... approximately") and omits throttling and the action position entirely. Your documentation duty — code and notes that are easy for others to reuse — is tested exactly this way: the best answer is complete, correct, and shortest-after-those-two-conditions.

**Passage 4 (for Questions 10–12).** From a user research summary shared with your team: "In usability testing, 7 of 9 participants failed to find the 'save and return later' feature. Several described feeling anxious about losing entered data. Participants who found the feature praised it. Two participants asked for the ability to export their application as a PDF. The researcher notes that PDF export was requested by participants who had already successfully saved, and recommends prioritising discoverability of save-and-return over new export functionality."

**Question 10 (easy) — Comprehension**

According to the passage, what does the researcher recommend prioritising?

- A) Building PDF export, because users requested it explicitly.
- B) Making the save-and-return feature easier to find.
- C) Removing the save-and-return feature.
- D) Increasing the sample size before acting.

**Correct answer: B**

**Explanation:** The recommendation is verbatim: "prioritising discoverability of save-and-return over new export functionality." Option A is the notable distractor because it reflects a real request in the passage — two participants did ask for PDF export — but a request being present is not the same as it being the recommendation. The researcher explicitly ranks discoverability above export. This distinction is the daily substance of your user focus skill: the difference between user needs (evidenced by 7 of 9 failing to find a feature they need, with anxiety about data loss) and user desires (a nice-to-have export requested by users whose core need was already met). Representing users internally means carrying the researcher's evidence-based ranking into planning, even when the desire is more fun to build.

**Question 11 (moderate) — True/false/cannot-say**

Statement: "A majority of participants who found the save-and-return feature also requested PDF export."

- A) True
- B) False
- C) Cannot say

**Correct answer: C**

**Explanation:** Do the set arithmetic the passage supports. Nine participants; 7 failed to find the feature, so 2 found it. PDF export was requested by two participants "who had already successfully saved" — successful saving suggests they found the feature, so the export-requesters plausibly are the two finders. But "plausibly" is the trap: the passage never states that the two finders and the two requesters are the same people, nor how many finders requested export — and note "several" felt anxious without exact overlap given anywhere. A majority of 2 is 2; the passage would need to confirm both finders requested export, and it does not quite do so. Cannot say. This is deliberately close reading: assessments at senior level include items where the arithmetic nearly closes but the identity of the groups is asserted nowhere. Nearly-entailed is not entailed — in research summaries as in specifications.

**Question 12 (challenging) — Inference and clear thinking about evidence**

A product manager reads the same summary and says: "Only 2 of 9 wanted PDF export — 78% of users don't want it, so we should never build it." Which is the most accurate assessment of this reasoning?

- A) Correct — the maths and the conclusion both hold.
- B) Flawed — absence of a request is not evidence of absence of need; the sample is small; and the researcher ranked priorities rather than ruling export out permanently.
- C) Flawed only because 2 of 9 is 22%, not 78%.
- D) Correct in conclusion but the passage forbids building export.

**Correct answer: B**

**Explanation:** The arithmetic is technically defensible (7 of 9 ≈ 78% did not request export — though "did not request" is not "don't want", which is the first flaw). Participants were never asked about export; two volunteered it. Non-mention in a think-aloud test is weak evidence of non-need. Second, nine participants is a discoverability-testing sample, not an attitude survey — usability testing with small samples reliably finds task failures, but percentages from it do not generalise as demand statistics. Third, the researcher's recommendation was a priority ordering ("over"), not a permanent veto — the passage forbids nothing, so D overstates. C fixes a percentage that was not the main error while endorsing the broken inference. The professional skill here is championing research while protecting it from misuse: the same user focus that carries findings into planning also stops findings being stretched into claims they cannot bear.

### Preparation tips

- **Train the "cannot say" reflex.** For every statement, ask two separate questions: does the passage state or entail this? Does the passage contradict this? If both answers are no, the answer is Cannot say — regardless of what you know professionally. Practise on real standards documents: draft three statements per paragraph and classify them.
- **Highlight modal verbs as you read.** Must, should, may, unless, expected to, need not — these words carry the obligations. In the assessment, mentally underline them; in your work, you already know a "should" misread as "must" blocks a team and a "must" misread as "should" fails an audit.
- **Watch quantifiers and hedges.** "Up to", "some", "several", "at most", "may be revised" — each one limits what can be concluded. Distractor options are usually the passage with one hedge deleted.
- **Keep timelines and actors separate.** Incident-style passages interleave what the provider did, what your team did, and what the defect did. A ten-second mental table of actor → action → time prevents the merged-timeline errors.
- **For clear-writing items, judge by the reader's need.** The best sentence is the one that gives the stated audience what they need to act: complete, accurate, then concise — in that order. Style preferences come last.
- **Read the question before re-reading the passage.** Skim the passage once for structure, read the question, then return to the relevant lines. Passage-first-and-only reading wastes the timed minutes on detail the questions never touch.

### Common pitfalls to avoid

- **Importing professional knowledge.** The most common senior-level error: you know how idempotency keys work, so you "know" the fix was deployed. The passage is the entire universe; answer from it alone.
- **Treating plausible as proven.** Options that are consistent with the passage but not established by it are wrong for True and wrong for inference items. "Nearly entailed" is the test-writer's favourite trap for strong candidates.
- **Merging maximums into exacts.** "Up to 48 hours" becomes "48 hours" under time pressure. Hedged durations, limits "subject to change", and estimates "approximately" never support exact claims.
- **Confusing a mentioned view with the passage's conclusion.** Passages quote stakeholders, requests, and objections. The question asks what the passage states or recommends — not what someone within it wished.
- **Over-correcting into permanent scepticism.** "Cannot say" is not always the safe answer; when the passage does state or contradict something, choosing Cannot say is simply wrong. Roughly a third of such items resolve each way — judge each on the text.
- **Choosing the longest or most formal sentence in clear-writing items.** Formality is not clarity. The bloated option (hedges, nominalisations, "potentially... approximately") is a distractor precisely because it sounds official while informing nobody.

## Workplace job-specific situational judgement assessment

### About this assessment

A situational judgement test (SJT) presents realistic workplace dilemmas and asks you to judge the effectiveness of possible responses. Unlike the cognitive, numeric, and verbal assessments, there is often no single formally "correct" answer derived by calculation; instead, responses are scored against a key built from the judgements of experienced practitioners and the organisation's professional behaviours — in UK government digital contexts, behaviours like user focus, collaboration, ownership, appropriate escalation, inclusion, and openness.

Typical format: an online test of 20 to 40 minutes presenting 8 to 15 scenarios. Each scenario describes a situation you might genuinely face — a production incident colliding with a deadline, a mentee struggling, a disagreement in design review — followed by four to six possible responses. Question styles vary: pick the most effective response; pick the most and least effective; rank all responses; or rate each response's effectiveness independently. There is usually no time pressure per question, but the overall window rewards decisiveness. Scoring compares your judgements to the expert key, so the skill being measured is calibration: do you recognise which behaviours actually work in a professional setting like yours?

For a senior developer, the SJT is arguably the most role-relevant assessment of the four, because seniority in your framework is defined at least as much by judgement and behaviour as by technical skill. You coach and mentor more junior colleagues — mentoring is a stream of judgement calls about when to intervene, when to let someone struggle productively, and how to give feedback that lands. You work with other disciplines to understand what needs to be built — which means handling disagreement with researchers, designers, and product managers without either capitulating or bulldozing. You operate production services — incidents are judgement under pressure, including the judgement of when to escalate. You plan and lead development on related stories — leadership means balancing delivery pressure against quality, security, and the wellbeing of the team. And you take responsibility for teaching the whole system to others — which requires the humility to admit what you do not know and the openness to be corrected in public.

Employers use SJTs for senior technical roles because technical assessments alone systematically over-select for individual brilliance and under-select for the collaborative judgement that actually determines whether services ship and survive. Practising SJTs will not make you someone you are not — but it will make you conscious of the principles behind effective responses, so that on the day, and in the job, you choose deliberately rather than by mood.

### How this assessment maps to your role

- **Incident and pressure scenarios** map to **Service support** and **Availability and capacity management**: identifying, locating and fixing service faults while communicating honestly, prioritising citizen impact, and escalating at the right threshold.
- **Mentoring and feedback scenarios** map to your duties to coach and mentor more junior colleagues and to teach understanding of the whole system: choosing responses that grow people rather than merely fixing their output.
- **Cross-disciplinary disagreement scenarios** map to **User focus** and your duty to work with other disciplines: championing user research, distinguishing user needs from desires, and disagreeing constructively with product pressure.
- **Quality-versus-deadline scenarios** map to **Modern development standards**, **Programming and build (software engineering)** and **Information security**: holding the line on test-driven development, secure design, and review discipline when the schedule squeezes — and knowing when a pragmatic, transparent compromise is genuinely right.
- **Design review and technical influence scenarios** map to **Systems design** and **Systems integration**: reviewing others' designs candidly without humiliating them, and coordinating across teams where you have responsibility but not authority.
- **Process and improvement scenarios** map to **Development process optimisation** and **Prototyping**: raising improvement opportunities through the team rather than imposing them, and treating prototyping as a team activity rather than a solo demonstration.

### Practice questions

**Question 1 (easy) — Production incident during sprint planning**

You are in sprint planning when your phone shows a monitoring alert: the citizen-facing service your team operates is returning errors for roughly 5% of requests, and the rate is climbing. You are the most experienced engineer on the service. What is the most effective immediate response?

- A) Stay in planning — the on-call process exists for exactly this, and interrupting planning sets a bad precedent.
- B) Excuse yourself, confirm the on-call engineer is responding, join the incident channel, and support the response; ask the team to continue planning without you.
- C) Silently leave the meeting and start debugging alone, since you know the system best.
- D) Announce that planning is cancelled and everyone should join the incident call.

**Correct answer: B**

**Explanation:** B balances every duty in play: citizen impact comes first (a climbing 5% error rate on a public service outranks a ceremony), but responding through the incident process — confirming on-call is engaged rather than displacing them — respects the team's operating model and keeps the response coordinated. Telling the team to continue models proportionate response. A hides behind process while the person best able to help sits in a meeting; on-call structures assign first response, not exclusive response. C helps technically but sabotages coordination — an incident with an invisible senior engineer working alone produces conflicting changes and a confused timeline. D over-escalates, burning six people's afternoon on an incident that currently needs two, and signals panic. The scored behaviours are ownership, user focus, and proportionate escalation — being available without taking over.

**Question 2 (easy) — A mentee's struggling pull request**

A junior developer you mentor has opened their third pull request for the same story. Their previous two attempts missed the point of your review comments, and this one still contains the same design problem. They seem increasingly discouraged. What is the most effective response?

- A) Approve it — it works, more or less, and their confidence matters more than design purity.
- B) Rewrite the code yourself tonight and push it to their branch so the story can close.
- C) Book a half-hour pairing session, work through the design problem together at the whiteboard or in the editor, and let them make the changes themselves.
- D) Write a longer, more detailed review comment explaining the problem a third time.

**Correct answer: C**

**Explanation:** Three written attempts have failed, which is strong evidence the medium is wrong, not the mentee. Pairing changes the channel: you can discover what they are actually misunderstanding (often something small and unstated), model your reasoning aloud, and — crucially — let them implement the fix so the learning and the credit stay theirs. A abandons the standard and teaches that persistence in misunderstanding gets rewarded; it also quietly tells them their growth is not worth your time. B closes the story but humiliates: code appearing overnight in your branch is a verdict. D repeats a failed strategy with more words — comment three did not fail for being too short. Your framework makes coaching and mentoring an explicit duty at this level; the scored behaviours are developing others, patience, and choosing effectiveness over convenience. Notice the general SJT pattern: when repetition has failed, the effective option changes approach rather than intensity.

**Question 3 (easy) — Credit in a show-and-tell**

At a cross-team show-and-tell, your delivery manager credits you personally for an integration approach that was substantially designed by a developer on another team during a joint spike. Colleagues from that team are present. What is the most effective response?

- A) Accept the praise and thank them — correcting details in public is awkward, and your team did do the work of implementing it.
- B) Briefly and warmly correct the record in the moment: name the colleague's contribution, then continue.
- C) Say nothing publicly but email the colleague afterwards to apologise.
- D) Interrupt to insist you deserve no credit at all and the other team did everything.

**Correct answer: B**

**Explanation:** Credit accuracy is a collaboration currency, and the situation is public: the colleague and their teammates are watching whether you will absorb their work into your reputation. A costs you their future collaboration — and cross-team goodwill is the medium in which systems integration work happens; you coordinate build activities across systems, and you will need that team. C rights the wrong in private while the public record stays false; the apology even confirms you knew. D overcorrects into theatrical self-effacement, which reads as performance and erases your team's genuine implementation work. B is proportionate: a one-sentence correction ("the elegant part of this came from Priya's design in our joint spike — we built on it") costs ten seconds, is remembered for years, and models the openness your level is expected to teach. Scored behaviours: integrity, collaboration, and giving credit — a named behaviour of effective technical leaders everywhere.

**Question 4 (moderate) — Deadline pressure against test-driven discipline**

Your team has committed to a ministerial deadline for a new feature, ten days away. A product manager suggests: "Skip the automated tests for now and write them after launch — we'll save three days." Your team follows a test-driven approach as standard. What is the most effective response?

- A) Agree — deadlines from ministers outrank engineering preferences, and tests can genuinely be added later.
- B) Refuse outright and state that the team will miss the deadline rather than compromise on any practice.
- C) Explain the actual trade-off: tests written test-first are part of how the code gets designed and how you know it works before launch; then explore real scope options — cutting a lower-value story, simplifying the feature — to meet the date without silently raising defect risk on a citizen-facing launch.
- D) Agree publicly but privately instruct the team to write tests anyway and absorb the schedule slip without telling the product manager.

**Correct answer: C**

**Explanation:** The effective move reframes a false trade (quality versus deadline) into the true one (scope versus deadline) — the negotiation that actually works in delivery. C treats the product manager as a partner: it explains why "tests afterwards" is not the same work moved later (test-first shapes design and provides pre-launch evidence; post-launch test-writing famously does not happen under the next deadline), then offers options a product owner can actually decide between. A silently converts a schedule risk into a defect risk on a public service and abandons a standard you are meant to uphold and teach. B is principled but rigid: it treats the practice as sacred rather than explaining its function, and surrenders the chance to solve the real problem. D is the worst kind of harmony — a lie that destroys the trust that working with other disciplines depends on, and leaves the product manager planning on false information. Scored behaviours: transparency, collaborative problem solving, and holding standards through explanation rather than authority.

**Question 5 (moderate) — Discovering a security flaw in an adjacent team's service**

While integrating with another team's API, you notice it returns full records — including data your service should not see — when queried with a malformed filter. This looks like an access-control flaw affecting real citizen data. The other team's tech lead is on leave this week. What is the most effective response?

- A) Report it immediately through your organisation's security incident route and notify the team's remaining developers directly, sharing exactly how to reproduce it; offer help; do not exploit the flaw further than the accidental discovery.
- B) Wait for the tech lead to return — it is their service, and going around them could damage the relationship.
- C) Post the reproduction steps in the open cross-team channel so everyone is aware and someone fixes it fast.
- D) Quietly code your own service to avoid triggering the flaw, since your integration works fine without malformed filters.

**Correct answer: A**

**Explanation:** A potential exposure of citizen data is a security incident now, not a code review comment next week. A does everything the moment requires: uses the incident route (which exists precisely so that individual absence cannot delay response), tells the people who can fix it with actionable detail, offers collaboration rather than blame, and respects the ethical line on probing further. B prioritises a relationship over citizens' data for a week — a clear mis-ranking, and most tech leads would themselves say so. C compounds the exposure: broadcasting reproduction steps for a live access-control flaw in an open channel is disclosure without containment. D is the quiet failure of ownership — engineering around a known data exposure makes you complicit in it; your information security skill is about mitigating threats, not personally avoiding them. Scored behaviours: escalation at the right threshold, ownership beyond your own service's boundary, and responsible disclosure. Note the SJT pattern: for security and data-protection scenarios, speed-through-proper-channels almost always outranks both waiting and broadcasting.

**Question 6 (moderate) — Design review disagreement with a peer**

In design review, a peer senior developer proposes an event-driven architecture for a new integration. You believe a simpler synchronous design meets the requirements with substantially less operational complexity, and you have reviewed the requirements carefully. The peer is invested in their proposal and the meeting is becoming tense. What is the most effective response?

- A) Defer — they will operate the thing, and vetoing a peer's design damages the relationship.
- B) State your position firmly and refuse to approve the design until it is changed.
- C) Anchor the discussion in shared criteria: walk through the requirements the design must meet — including operational load, failure modes, and who supports it at 2am — and propose evaluating both options against them, offering to timebox a spike if the group cannot decide on paper.
- D) Let the meeting end without resolution and email the architecture lead afterwards recommending your design.

**Correct answer: C**

**Explanation:** Your review duty — reviewing others' designs to ensure appropriate technology and efficient use of resources — is precisely this conversation done well. C depersonalises the disagreement by moving it from proposal-versus-proposal to options-versus-criteria: complexity, failure modes, and operability become shared measures rather than debating points, and the spike offer replaces opinion escalation with evidence. This is also how prototyping works as a team activity in your framework — testing options with others rather than winning arguments. A abandons your honest technical judgement to preserve comfort; unneeded event-driven complexity will tax the team for years, and review exists to catch exactly that. B substitutes authority for reasoning and entrenches the tension. D is the relationship-damaging move A feared, done covertly: the peer learns you went around them, and every future review with you becomes adversarial. Scored behaviours: constructive challenge, evidence over ego, and keeping technical conflict inside the room where it can be resolved.

**Question 7 (moderate) — A researcher's findings against your own preference**

You personally designed a navigation pattern for an internal caseworker tool. User research now shows caseworkers consistently fail to find a key function under your pattern, though two vocal caseworkers say they love the design. The user researcher recommends changing it. You genuinely believe the design is elegant and that users would adapt with time. What is the most effective response?

- A) Support the change: the failure data reflects user needs; the praise and your own attachment reflect desires and aesthetics. Ask the researcher what success would look like so the fix can be tested the same way.
- B) Argue for keeping the design for another quarter to give users time to adapt, since some users clearly like it.
- C) Accept the change but register formally that you disagree, so the record shows your design was overruled.
- D) Propose a compromise keeping your pattern but adding a tutorial explaining where the function lives.

**Correct answer: A**

**Explanation:** Your framework is unusually explicit here: you champion user research, represent users internally, and can explain the difference between user needs and the desires of the user — and this scenario tests whether that holds when the desire is your own. Consistent task failure is need-level evidence; the two enthusiasts and your sense of elegance are preference-level evidence. A acts on the stronger evidence and — the senior move — closes the loop by defining a measurable success test for the replacement. B bets caseworkers' daily productivity on adaptation, privileging the vocal minority over the failing majority. C complies while spending goodwill on blame-proofing; a formal register of dissent over a usability fix reads as ego, not rigour. D is seductive — everyone likes a compromise — but a tutorial that explains an unfindable function is a patch on the symptom: if users need instructions to find a key function, the finding stands. Scored behaviours: user focus over personal attachment, championing research, and gracefully losing an argument to evidence.

**Question 8 (moderate) — Least effective: intermittent fault before a bank holiday**

It is Thursday afternoon before a bank holiday weekend. A colleague mentions the payments reconciliation job "failed once overnight but worked on retry — probably nothing." The job runs nightly, unattended, and feeds a report finance uses each morning. Which response is LEAST effective?

- A) Spend thirty minutes now checking the logs from the failure to understand what happened before deciding anything.
- B) Note it as "probably transient" and pick it up after the long weekend, since the retry succeeded.
- C) Check whether alerting would catch a full failure over the weekend, and add a basic alert if not.
- D) Brief the on-call engineer that the job showed instability, with a pointer to the runbook and last night's logs.

**Correct answer: B**

**Explanation:** Least-effective questions invert your reading: find the response that ignores the risk everyone else is managing. B walks past a warning sign at the worst possible moment — an intermittent failure in an unattended nightly job, immediately before three unattended nights, with a business consumer depending on the output each morning. "Worked on retry" is how systemic issues introduce themselves; your duty to improve robustness, resilience and stability is built on treating intermittence as signal. A, C, and D are all reasonable and complementary: A investigates while the evidence is fresh, C ensures a weekend failure would at least be seen, D arms the person who will be holding the pager. Notice that none of the effective options is heroic — nobody cancels their weekend; they spend well under an hour converting an unknown risk into a monitored one. Scored behaviours: ownership, foresight, and proportionate risk management — and the classic least-effective cluster: dismissal of a warning because dismissal is convenient.

**Question 9 (challenging) — Capacity concern versus a launch commitment**

A cross-government campaign will drive traffic to your service on the 1st of next month. Your load estimates suggest peak demand could exceed your tested capacity by around 30%, but the estimate is uncertain. The service owner has publicly committed to the date, and moving it would be embarrassing. You raised capacity informally two weeks ago and nothing happened. What is the most effective response now?

- A) Raise it formally: write a short note quantifying the risk (forecast versus tested capacity, uncertainty range, expected failure mode and citizen impact), propose concrete mitigations — load testing this week, scaling ahead of the date, graceful degradation, a queue-based fallback — and ask the service owner for a decision, offering to talk it through.
- B) Say nothing further — you raised it once, the decision is above your pay grade, and you have an email trail proving you flagged it.
- C) Escalate directly to the service owner's boss, since the service owner ignored the first warning.
- D) Quietly scale the infrastructure yourself to triple capacity, absorbing the cost into the team's budget without approvals.

**Correct answer: A**

**Explanation:** An informal mention that produced nothing has not discharged your responsibility — availability and capacity management against business needs is your named skill, and the citizen impact of a launch-day failure is the highest stake in the scenario. A does what effective escalation looks like: it converts a vague worry into a decision-ready document (numbers, uncertainty, impact, options), routes it to the accountable person, and preserves the relationship by helping them succeed rather than proving them wrong. The mitigations matter — offering paths that protect the date (scale, degrade gracefully, queue) shows you understand the political constraint rather than dismissing it. B optimises for blamelessness: the email trail will comfort you at the post-incident review while citizens see error pages. C skips a step — the service owner has not yet refused a clear, formal, quantified request; leapfrogging them on the basis of an informal mention burns the relationship unnecessarily (though C becomes right if A is genuinely ignored). D exceeds your authority, hides a material cost, and — worse — silently removes the organisation's chance to consider the better mitigations. Scored behaviours: active escalation with options, quantification, ownership, and respecting accountability without abandoning responsibility.

**Question 10 (challenging) — A teammate's shortcut with citizen data**

Reviewing a colleague's pull request, you notice they have added debug logging that writes full citizen records — including personal details — to the application log to help diagnose a production issue. The logs are retained for 90 days and accessible to the whole team. The colleague is respected and was trying to fix a real problem quickly. What is the most effective response?

- A) Approve it with a comment suggesting they remove the logging "when convenient", since the production issue is real and urgent.
- B) Request changes on the pull request, explaining the data protection problem specifically; suggest a compliant alternative (logging record identifiers, or redacted fields); and check whether similar logging already reached production — because if it did, that needs reporting as a potential data incident, and you should say so to them directly and kindly.
- C) Reject the pull request with a one-line comment quoting the security policy.
- D) Approve the pull request but raise the pattern anonymously at the next retrospective so nobody is singled out.

**Correct answer: B**

**Explanation:** Two problems hide here, and the effective answer handles both. The prospective one — the pull request — is straightforward: request changes, explain the specific harm (personal data spread into a 90-day, team-readable store multiplies exposure and breaches minimisation principles), and offer a working alternative so the real production issue still gets diagnosed; that last part is what separates a colleague from a compliance gate. The retrospective one is the senior catch: if this pattern was already deployed, citizen data may already sit in logs, and that is a potential data incident with reporting obligations — noticing the possibility and saying so is exactly the whole-system thinking your level is responsible for teaching. A treats live personal data exposure as a style nit with a courtesy deadline. C may technically stop the change but teaches nothing, offers no alternative, and leaves the maybe-already-deployed question unasked. D approves the actual harm in front of you to preserve comfort, then discusses it abstractly later — backwards on both counts, and anonymity in a small team protects no one anyway. Scored behaviours: information security as engineering (specific threat, specific mitigation), kindness with candour, and ownership of the system beyond the diff.

**Question 11 (challenging) — Most and least effective: knowledge silo risk**

You realise you are the only person who understands the overnight batch subsystem — its design, its failure modes, its recovery procedures. You are about to take three weeks of leave, and a major integration touching that subsystem is scheduled during your absence. Rank matters: which is the MOST effective and which the LEAST effective response?

1. Postpone your leave — the integration is too important.
2. Spend the remaining time before leave running two working sessions with the team on the subsystem, writing up the recovery runbook, and pairing with one developer on the integration's riskiest touchpoint; agree with your delivery manager what should wait for your return.
3. Write a long document alone covering everything you know and email it to the team on your last day.
4. Tell the delivery manager the integration must be delayed until you return, since nobody else can do it safely.

- A) Most: 2; Least: 4
- B) Most: 1; Least: 3
- C) Most: 2; Least: 3
- D) Most: 3; Least: 1

**Correct answer: A**

**Explanation:** Option 2 is the model answer for the bus-factor scenario because it converts private knowledge into team capability through the channels that actually transfer it — working sessions and pairing move tacit knowledge, the runbook captures the procedural core, and the scoping conversation with the delivery manager makes residual risk a managed decision rather than a surprise. This is your framework duty verbatim: take responsibility for teaching the whole system to others. For least effective, compare 3 and 4. Option 3 is weak — documents written alone on the last day transfer far less than their authors believe, and nobody can ask the absent author questions — but it attempts mitigation and leaves the team better than nothing. Option 4 is worse: it blocks the programme, entrenches the silo as leverage ("nobody else can") rather than treating it as the problem to fix, and converts your leave into organisational fragility on the record. Option 1 sacrifices your own sustainability to avoid fixing the underlying fragility, which will still exist at your next holiday — martyrdom is not mitigation, but it is not the least effective. Scored behaviours: teaching, sustainability, planning ahead, and treating yourself as a single point of failure to be engineered away.

**Question 12 (challenging) — Improvement idea meeting team resistance**

You have identified that the team's manual release checklist could be largely automated, cutting release time from half a day to under an hour and removing a recurring class of human error. When you raise it, two long-tenured developers push back hard: "the manual checks catch things automation can't" and "we've been burned by automation before." The team room goes quiet. What is the most effective response?

- A) Drop it — team harmony on release practices matters more than efficiency, and they know history you don't.
- B) Build the automation over a weekend and demonstrate it as a fait accompli at Monday's stand-up.
- C) Get curious about their objection: ask which specific checks have caught real problems and what the previous automation failure was; propose a reversible first step — automating only the mechanical checks while keeping human judgement checks manual, run in parallel with the checklist for three releases and reviewed against evidence.
- D) Ask the delivery manager to mandate the automation, since the data clearly supports it.

**Correct answer: C**

**Explanation:** Your development process optimisation skill is explicitly collaborative at this level — identify opportunities and contribute to implementing solutions, with the team, not to them. C treats the resistance as data: long-tenured objections usually encode real history ("burned before" has a story), and asking for specifics either surfaces genuine constraints your design must honour or lets the objectors discover the concerns are addressable. The proposal is then engineered for trust — reversible, partial (automate the mechanical, keep the judgement), run in parallel, and judged on evidence after three releases. That structure converts an argument about opinions into an experiment with agreed success criteria — the same instinct as your prototyping skill: test options with others, iterate patterns. A abandons a meaningful improvement (and the error class keeps recurring) at the first friction. B wins the argument and loses the team: fait-accompli engineering tells colleagues their concerns are obstacles, and they will remember at your next proposal — besides which, their specific catches may be real and your weekend build may miss them. D borrows authority to skip persuasion; mandated practices get complied with minimally and abandoned quietly. Scored behaviours: curiosity before advocacy, incremental change, evidence over assertion, and bringing people along — the difference between having influence and merely being right.

### Preparation tips

- **Learn your organisation's behaviour language.** SJT keys are built from the professional behaviours your organisation publishes — user focus, collaboration, ownership, inclusion, openness. Re-read them before the test; effective options are usually those behaviours in scenario clothing.
- **Answer as your best professional self, consistently.** Do not try to game what "they" want with an invented persona — inconsistency across scenarios is detectable and self-defeating. The test rewards the judgement you actually use on your good days; practise noticing what your good days have in common.
- **Rehearse the recurring shapes.** Most senior-developer SJT scenarios reduce to a handful of shapes: live risk versus ceremony, quality versus deadline, mentee versus schedule, peer disagreement, security versus speed, silo versus team. For each, know your principle in advance (citizen impact first; scope not quality; change the medium when repetition fails; criteria not egos; proper channels fast; teach the system).
- **In "most effective" items, look for the option that solves the problem and the system.** The strongest responses fix the immediate issue and address why it arose — the alert that gets added, the runbook that gets written, the success test that gets defined.
- **For "least effective", find the passive or self-protective option.** Least-effective answers cluster around dismissing warnings, waiting for someone else, documenting concerns instead of acting on them, and covert moves that protect the responder rather than the outcome.
- **Practise ranking, not just picking.** If the format ranks all options, the middle rankings matter. After choosing best and worst, ask of the remainder: which does more good with less harm? Practising full rankings sharpens the calibration the test scores.

### Common pitfalls to avoid

- **Answering idealistically rather than effectively.** "Simply persuade everyone" is not an available move in a real organisation with deadlines and history. Choose what would actually work with real colleagues under real constraints.
- **Confusing decisiveness with unilateralism.** Senior candidates over-select bold solo action — rewriting the mentee's code, scaling infrastructure without approval, building the automation over the weekend. Boldness that bypasses people scores as relationship and governance damage, because that is what it causes.
- **Over-escalating and under-escalating.** Both fail. Skipping a level before the accountable person has refused a clear, quantified request burns trust; staying silent after a real warning has been ignored abandons the outcome. The pattern that scores: escalate actively, with evidence and options, one level at a time — faster for security and citizen data.
- **Protecting yourself instead of the outcome.** Options built around email trails, formal records of disagreement, and "I flagged it" optimise for blamelessness. Assessment keys — and post-incident reviews — can tell the difference between covering the risk and covering yourself.
- **Sacrificing standards silently to be agreeable.** Quietly dropping tests, approving the risky pull request, deferring to the louder peer — harmony purchased with hidden risk scores poorly, because the risk lands on users. The effective versions of "yes" are transparent trade-offs.
- **Forgetting the people in technical scenarios.** Every scenario with a mentee, a peer, or another discipline is scoring how you treat them, not just what gets built. Responses that humiliate, bypass, or manipulate people lose points even when their technical content is impeccable.

<!-- APPEND -->
