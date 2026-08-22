# Senior Developer (Management) - Psychometric Assessment Resources

## Introduction

Welcome! This guide has been written especially for you as a senior developer on the management track within the UK Government Digital and Data profession. Whether you are preparing for an internal assessment, applying for a promotion or a new post, benchmarking your own capability, or simply curious about how psychometric assessments connect to your day-to-day work, this document will help you practise, reflect, and build confidence.

Psychometric assessments are structured, standardised exercises that measure the mental capabilities and behavioural tendencies that predict success in a role. For a senior developer with management responsibilities, that means far more than abstract puzzles. The assessments described here are job-specific: they use the kinds of artefacts you genuinely handle — pull requests, CI/CD pipeline configurations, sprint boards, capacity dashboards, incident reports, test suites, integration plans, and design review notes — and the kinds of decisions you genuinely make, such as planning and leading development across sets of related stories, coaching and mentoring more junior colleagues, operating the production services your team builds, and finding ways to improve system robustness, resilience and stability.

Why do these assessments matter for your role in particular? As a senior developer on the management track, you sit at the point where hands-on engineering meets people leadership. You still write clean, secure code following a test-driven approach, and you still design systems of medium risk and complexity — but you also take responsibility for understanding the whole system and teaching it to others, for reviewing other people's designs, and for representing your team when working with other disciplines to understand what needs to be built. Assessments of cognitive ability, numerical reasoning, verbal reasoning, and situational judgement map directly onto those demands. Practising them sharpens exactly the skills your role depends on: spotting a logical flaw in a deployment plan, interpreting a capacity trend before it becomes an outage, extracting precise meaning from a security standard, and choosing the most effective response when a mentee is struggling or a release is at risk.

This document is organised into four main assessment sections, each following the same pattern: an overview of what the assessment measures and why employers use it for roles like yours, a mapping of the assessment's dimensions to the specific named skills in your role summary, a substantial set of practice questions with full worked explanations, practical preparation tips, and common pitfalls to avoid.

Here is how to get the most from it. First, read each "About this assessment" section so you understand the format before you meet it under time pressure. Second, attempt every practice question honestly — commit to an answer before reading the explanation. Third, treat each explanation as a mini-lesson: even when you answer correctly, the worked reasoning will deepen your technique, exactly the way a good code review deepens a pull request. Fourth, use the preparation tips and pitfalls for self-reflection: they connect assessment performance back to your professional development as an engineer who leads people as well as code.

You already do harder things than these questions every working week — you debug production systems, mediate design disagreements, and help junior developers grow. Treat this practice as another form of deliberate professional development. Take your time, be kind to yourself, and enjoy it. Let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive ability assessment measures the exact mental processes your role demands, using practical workplace scenarios rather than abstract shapes and number sequences. Unlike a generic intelligence test, it presents you with the everyday materials of your job — in your case, version-control histories, pipeline configurations, dependency graphs, release plans, monitoring dashboards, coding standards, and review comments — and asks you to reason quickly and accurately about them.

Typical format: an online, timed test lasting 15 to 30 minutes, with somewhere between 15 and 30 questions covering pattern recognition, logical deduction, error checking, prioritisation, and applied problem solving. Scoring is objective, comparing your responses against a norm group of people at a similar level, and modern platforms often adapt question difficulty based on your previous answers — so a test that feels progressively harder is usually a sign you are doing well, not badly. Employers typically receive a breakdown of speed versus accuracy rather than a single number, so working both quickly and carefully matters. You will normally be offered short, ungraded practice questions before the real test begins, so you can get comfortable with the interface without pressure.

For a senior developer on the management track, cognitive assessment is particularly relevant because your professional value increasingly comes from structured thinking applied at the level of the whole system rather than the single function. You plan and lead development on sets of related stories, which means holding many moving parts in mind at once: which stories depend on which, which services integrate with which, where a design decision contradicts an agreed standard, and what follows logically when one component of the system changes. You also review the work of others — code, designs, test plans — where the core skill is error checking: finding the inconsistency that everyone else has read past. A well-designed cognitive assessment simulates precisely those demands in miniature, which is why employers use it to identify people who can be trusted to lead delivery and teach the whole system to others.

### How this assessment maps to your role

The assessment dimensions map directly to the named skills in your role summary:

- **Pattern recognition** maps to **Availability and capacity management** and **Service support**: identifying capacity issues before they bite, and locating service faults quickly, both depend on spotting the anomaly in a wall of otherwise normal signals — a memory graph that creeps upward, a log pattern that repeats just before each failure.
- **Logical deduction** maps to **Systems design** and **Systems integration**: designing systems of medium risk and complexity, defining the integration build, and co-ordinating build activities across systems all require you to reason validly from constraints — dependency rules, environment availability, interface contracts — to their necessary consequences.
- **Error checking** maps to **Programming and build (software engineering)** and **Modern development standards**: reviewing specifications and code, applying agreed standards and supporting others in applying them, means spotting where an artefact quietly contradicts the rules it claims to follow.
- **Prioritisation** maps to your duties to **plan and lead development on sets of related stories** and to **operate the production services you build**: production incidents, sprint commitments, coaching conversations and governance requests all compete for the same hours, and ranking them well is a learned discipline.
- **Applied problem solving** maps to **Development process optimisation** and **Prototyping**: identifying process optimisation opportunities under guidance, and choosing the most appropriate prototyping method for a question, both start with decomposing a messy situation into a solvable structure.
- Throughout, **User focus** shapes what counts as the right answer: the best reasoning in this role always keeps sight of the users the service exists for.

### Practice questions

**Question 1 (easy) — Pattern recognition in release tags**

Your team tags releases using semantic versioning: MAJOR.MINOR.PATCH, where the patch number increments for fixes, the minor number increments (and patch resets to zero) for backwards-compatible features, and the major number increments (resetting the others) for breaking changes. Reviewing the release history a junior developer has prepared, you see:

1. 2.4.1
2. 2.4.2
3. 2.5.0
4. 2.5.1
5. 2.6.1

Assuming each tag was created in the order shown and each release was either a fix or a backwards-compatible feature, which tag breaks the versioning pattern?

- A) Tag 2
- B) Tag 3
- C) Tag 4
- D) Tag 5

**Correct answer: D**

**Explanation:** Walk the sequence forward against the rules. 2.4.1 to 2.4.2 is a patch increment — valid fix. 2.4.2 to 2.5.0 increments minor and resets patch to zero — valid feature. 2.5.0 to 2.5.1 is a valid fix. But 2.5.1 to 2.6.1 increments the minor version without resetting patch to zero: a feature release should have produced 2.6.0. Tag 5 is the anomaly. This is exactly the kind of consistency check you perform when supporting others in applying modern development standards: versioning conventions look trivial, but a broken convention misleads every downstream consumer about what changed — and spotting the structural break quickly, rather than re-deriving each rule from scratch, is what the assessment rewards.

**Question 2 (easy) — Logical deduction from a branch protection policy**

Your team's policy states: "Every pull request merged to main must have at least two approving reviews, unless it is a hotfix approved by the on-call lead." Looking at the audit log, you see that yesterday a pull request was merged to main with only one approving review. Which one of the following conclusions must be true?

- A) The team has breached its branch protection policy.
- B) The pull request was a hotfix approved by the on-call lead.
- C) Either the pull request was a hotfix approved by the on-call lead, or the policy was breached.
- D) The branch protection rules were misconfigured in the repository settings.

**Correct answer: C**

**Explanation:** The policy is a conditional rule with a single permitted exception. From the facts given, you cannot tell whether the exception applies: the merge might have been a legitimate on-call hotfix (making B true and A false) or an ordinary change pushed through with too little review (making A true and B false). Neither A nor B must hold on its own — each is merely possible. D introduces a mechanism the stem never mentions. The only conclusion guaranteed in every scenario consistent with the facts is the disjunction in C. This discipline — deducing only what the information guarantees — matters in your role too: challenging a colleague for "breaking the rules" before checking whether the exception applied damages trust, and as someone who coaches and mentors more junior colleagues, how you raise a suspected breach teaches the team as much as the rule itself.

**Question 3 (easy) — Error checking a CI pipeline definition**

Your team's agreed pipeline standard requires stages in this order: lint, unit tests, build, integration tests, security scan, deploy to staging. A colleague's proposed pipeline for a new microservice lists:

1. lint
2. unit tests
3. build
4. security scan
5. integration tests
6. deploy to staging

Which statement best describes the discrepancy?

- A) The pipeline is missing a required stage.
- B) Two adjacent stages are in the wrong order.
- C) The pipeline contains a stage the standard does not allow.
- D) The pipeline fully complies with the standard.

**Correct answer: B**

**Explanation:** Compare the lists position by position. Stages 1 to 3 match. The standard then requires integration tests followed by security scan; the proposal has security scan (position 4) before integration tests (position 5) — the same two stages, swapped. Nothing is missing and nothing extra has been added, so A and C are wrong, and D fails because order is part of the standard. The efficient technique is a positional walk-through rather than an impressionistic read: your eye is drawn to whether all six familiar names appear, and they do, which is exactly how ordering errors survive review. When you ensure design standards, methods and tools are applied effectively — part of your **Systems design** skill — this positional discipline is what catches the subtle deviation that a checklist mentality misses.

**Question 4 (moderate) — Prioritisation across delivery and people duties**

It is 9:15 on Monday morning. Four items compete for your attention:

1. The monitoring dashboard shows the payments service's error rate has risen from 0.1% to 2% over the past hour; no alert has fired yet and users may soon be affected.
2. Sprint planning starts at 10:00 and you are due to present the proposed breakdown of the next set of related stories.
3. A junior developer you mentor has asked for urgent feedback on a pull request they want to merge today.
4. Your delivery manager needs your input to the quarterly capacity report by Friday.

Which sequencing is most defensible?

- A) 2, 1, 3, 4 — the meeting is closest in time, so prepare for it first
- B) 1, 2, 3, 4 — investigate the production anomaly first, then planning, then the review, then the report
- C) 3, 1, 2, 4 — unblock your mentee first because coaching is a core duty
- D) 1, 3, 2, 4 — production first, then the mentee, and skip preparing for sprint planning

**Correct answer: B**

**Explanation:** Prioritisation questions reward reasoning about impact and urgency together. Item 1 is both urgent and high impact: a twenty-fold error-rate rise on a payments service signals a fault that may already be affecting users, and operating the production services you build is your responsibility — you triage first, even before an alert fires, because alerts confirm problems rather than define them. Item 2 comes next: it is time-anchored at 10:00 and the whole team's week depends on it; if the incident escalates, the defensible move is to send a colleague your breakdown and stay on the incident, but nothing in the stem says you cannot do both. Item 3 matters — coaching is genuinely part of your role — but "wants to merge today" is a preference, not a production deadline, and a same-day review after planning still meets it. Item 4 has days of slack. Option A confuses proximity with priority; C elevates a routine review above a live service risk; D abandons a leadership commitment that ten minutes of preparation would meet. The pattern to internalise: sequence by impact-weighted urgency, not by whichever stakeholder asked most recently or most loudly.

**Question 5 (moderate) — Logical deduction about integration sequencing**

You are defining the integration build for three services. The constraints are: (i) the notifications service cannot be integrated until the identity service is integrated; (ii) the reporting service must be integrated in the same phase as the notifications service or a later phase; (iii) each phase integrates exactly one service; (iv) there are exactly three phases. Which one of the following must be true?

- A) The identity service is integrated in phase 1.
- B) The reporting service is integrated in phase 3.
- C) The notifications service is integrated in phase 2.
- D) All of A, B and C must be true.

**Correct answer: D**

**Explanation:** Work through the constraints. With one service per phase and three phases, all three services are integrated in some order. Constraint (i) puts identity strictly before notifications. Constraint (ii) puts reporting at or after notifications, but "same phase" is impossible under one-service-per-phase, so reporting comes strictly after notifications. That forces the strict order identity → notifications → reporting, which pins identity to phase 1, notifications to phase 2 and reporting to phase 3 — so A, B and C are each individually necessary, and the answer is D. The trap is stopping at the first option that must be true and selecting A without noticing that the constraint set fully determines the schedule. When you define the integration build and co-ordinate build activities across systems, this is a daily reasoning pattern: partial orderings plus resource limits often determine far more of the plan than they appear to, and recognising a fully-determined schedule early saves the team from debating choices they do not actually have.

**Question 6 (moderate) — Pattern recognition in a capacity trend**

You review weekly peak memory usage for a production service over eight weeks, as a percentage of the container limit: 58, 61, 59, 63, 66, 65, 70, 73. The service is restarted during each fortnightly deployment. As the senior developer responsible for availability and capacity, what is the most reasonable first interpretation?

- A) Normal fluctuation — the figures move up and down, so no action is needed.
- B) An upward trend of roughly 2 percentage points per week that will approach the limit within weeks and warrants investigation now.
- C) A memory leak is confirmed, and the container limit should be doubled immediately.
- D) The monitoring data is unreliable because usage should be flat.

**Correct answer: B**

**Explanation:** Separate the signal from the noise. Week to week the figures wobble by a point or two, but the trend is unmistakably upward: from 58 to 73 is 15 percentage points over seven intervals, roughly 2 points per week, and the last three readings are the three highest. Extrapolating naively, the service approaches its limit in about three months — and trends like this often steepen. Option A pattern-matches on local wobble and misses the drift. Option C over-concludes: the growth is consistent with a leak, but it survives fortnightly restarts in aggregate terms, so it could equally be organic traffic growth or a data-volume effect; doubling the limit treats a symptom at real cost without a diagnosis. Option D mistakes an unwelcome pattern for a broken instrument. The professional move — and the assessment answer — is B: recognise the trend, and initiate investigation while there is still headroom. This is your **Availability and capacity management** skill in miniature: identify capacity issues and initiate remedial action before users ever notice.

**Question 7 (moderate) — Error checking a story dependency board**

Your sprint board for a set of related stories shows these dependencies: Story A ("Create consent API") must finish before Story B ("Consent UI") and before Story C ("Consent audit log"). Story D ("Migrate legacy consent records") must finish before Story C. The board also records: B is "In progress", A is "In progress", C is "Done", D is "Done". Which single status is impossible if the dependency rules were respected?

- A) A "In progress"
- B) B "In progress"
- C) C "Done"
- D) D "Done"

**Correct answer: C**

**Explanation:** Test each status against the rules. D "Done" violates nothing — it has no prerequisites. A "In progress" is fine in itself. B "In progress" is suspicious, because B requires A to be finished and A is not — but pause: teams often start UI work against a stubbed API, and more importantly the question asks which status is impossible, so compare the candidates. C "Done" requires both A and D to be finished; D is done but A is still in progress, so C cannot legitimately be complete. Between B and C, note the difference in severity: B in progress while A is unfinished breaches the rule for starting, but C done while A is unfinished breaches the rule for finishing — and on a strict reading of "must finish before", C's completion is flatly contradictory, whereas B's start would only be contradictory if the rule said B cannot start until A finishes. The precise reading of "finish before" language is the skill here. When you plan and lead development on sets of related stories, boards drift out of truth exactly like this, and the senior developer who reads statuses against dependencies — rather than trusting the columns — is the one who catches the audit log that "passed" without its API.

**Question 8 (moderate) — Deduction from a feature flag policy**

Your team's rollout policy says: (i) a feature flag may only be enabled in production after it has been enabled in staging for at least three days; (ii) any flag enabled in production must have a named owner; (iii) flags with no activity for 90 days must be removed. The new "instant-payout" flag was enabled in staging on Monday morning and has a named owner. Today is Wednesday afternoon of the same week. A product manager asks you to enable it in production now, saying "it has an owner, so we're compliant." Which response is logically correct?

- A) Enabling it now complies, because rule (ii) is satisfied.
- B) Enabling it now breaches rule (i), because staging exposure is roughly two and a half days, not at least three.
- C) Enabling it now breaches rule (iii).
- D) The rules conflict, so none of them can be applied.

**Correct answer: B**

**Explanation:** Each rule is independent, and compliance requires satisfying all applicable rules, not any one of them. Rule (ii) is indeed satisfied — there is a named owner — but that is necessary, not sufficient. Rule (i) requires at least three days in staging: Monday morning to Wednesday afternoon is about two and a half days, so the condition fails, and enabling now would breach it. Rule (iii) concerns stale flags and is irrelevant to a flag created this week. Nothing conflicts, so D fails. The product manager's argument is a classic partial-compliance fallacy: citing the rule you satisfy while omitting the one you do not. As a senior developer you will meet this reasoning often, usually in good faith and under delivery pressure; the cognitive skill is separating the rules, checking each, and the leadership skill — which the situational judgement section returns to — is explaining the gap without making the requester feel ambushed.

**Question 9 (challenging) — Multi-constraint release scheduling**

You must schedule three activities in one working week (Monday to Friday, one activity per day at most): the database migration (M), the API release (R), and the integration test run (T). Constraints: (i) M must happen on an earlier day than R; (ii) T must happen on the day immediately after R; (iii) the change advisory board only permits migrations on Tuesdays and Thursdays; (iv) Friday is a change-freeze day — no migrations, releases, or test runs may take place on Friday. On which day must the API release (R) take place?

- A) Tuesday
- B) Wednesday
- C) Thursday
- D) It cannot be scheduled within these constraints.

**Correct answer: B**

**Explanation:** Anchor on the most constrained activity, the migration: rule (iii) allows only Tuesday or Thursday. Case 1: M on Thursday. Rule (i) then pushes R to Friday at the earliest, and rule (iv) bans Friday releases — the whole case fails. So M must be on Tuesday. Now place R: rule (i) allows Wednesday, Thursday, or Friday, and rule (iv) removes Friday, leaving Wednesday or Thursday. Test Thursday: rule (ii) forces T onto Friday, and rule (iv) bans Friday test runs too — so Thursday fails. That leaves exactly one placement: R on Wednesday, with T on Thursday, and the full schedule M-Tuesday, R-Wednesday, T-Thursday satisfies every rule. The answer is B, and A fails because Tuesday is taken by M under the one-activity-per-day limit while rule (i) requires R after M anyway. The method matters more than the puzzle: enumerate the options of the most constrained item, eliminate cases by propagating consequences, and confirm the survivor against every rule. This is exactly how you sequence real work around change freezes and board approvals when you define the integration build and co-ordinate build activities across systems — and writing the elimination down, rather than holding it in your head, is what makes your release plans reviewable by others.

**Question 10 (challenging) — Fault isolation by elimination**

A nightly batch job has failed three nights running. You establish these facts: (i) the job succeeds every night in the staging environment, which runs identical code; (ii) the failures began the night after a production-only configuration change to database connection pooling; (iii) the job fails at a different record each night; (iv) re-running the failed job manually each morning succeeds. Which hypothesis best fits all four facts?

- A) A bug introduced in the latest code release.
- B) A data quality problem with specific bad records.
- C) Resource contention in production during the nightly window, aggravated by the connection pool change.
- D) A hardware fault on the production database server.

**Correct answer: C**

**Explanation:** Test each hypothesis against every fact, not just some. A code bug (A) is undermined by fact (i) — identical code succeeds in staging — and by fact (iv), since the same code succeeds in the morning. Bad records (B) would fail deterministically at the same record each run, contradicting facts (iii) and (iv). A hardware fault (D) is possible but does not explain why failures began precisely after the pooling change (ii), nor why mornings always succeed (iv). Hypothesis C fits everything: production has nightly load that staging lacks (explaining i), the pooling change altered behaviour under that load (explaining ii and the timing), contention strikes non-deterministically (explaining iii), and the quiet morning window succeeds (explaining iv). This is the method behind your **Service support** skill — identify, locate and fix service faults — done properly: a fault hypothesis must explain *all* the evidence, and the facts that discriminate best are the ones that differ between environments and times. It is also a teachable moment: walking a junior colleague through this elimination table is exactly how you take responsibility for teaching the whole system to others.

**Question 11 (challenging) — Applied problem solving: on-call rota constraints**

You are constructing next month's on-call rota for four developers — Priya, Sam, Tomás, and you — covering four consecutive weeks, with each person taking exactly one week. Constraints: (i) you are attending a residential leadership course in weeks 3 and 4, so you can only take week 1 or week 2; (ii) Priya, the newest developer, must take the week immediately after yours so you can support her handover; (iii) Priya's on-call week must be one in which Sam is in the office to provide second-line cover on the legacy queue system, and Sam is on leave for the whole of week 2; (iv) Tomás took the final on-call week of last month, and the team rule against consecutive on-call weeks means he cannot take week 1. Who must take week 1?

- A) Priya
- B) Sam
- C) Tomás
- D) You

**Correct answer: B**

**Explanation:** Anchor on the most constrained person: you, restricted to week 1 or week 2 by constraint (i). Test week 1: constraint (ii) then puts Priya in week 2 — but constraint (iii) bars Priya from week 2, because Sam is on leave and cannot provide her second-line cover. The case collapses, so you must take week 2, and constraint (ii) places Priya in week 3. That leaves weeks 1 and 4 for Sam and Tomás. Constraint (iv) bars Tomás from week 1, so Sam takes week 1 and Tomás takes week 4 — and a final pass confirms every rule holds: you in week 2 (allowed), Priya in week 3 immediately after you, with Sam back in the office, and Tomás safely separated from his previous stint. Sam must take week 1: answer B. Notice the technique: case-split on the most constrained element, propagate each choice through the remaining rules, and let a contradiction eliminate the branch. Notice also what the puzzle encodes about your real job — the constraints are not arbitrary, they are supervision, cover, and workload fairness, and building rotas that respect all three is part of coaching and mentoring more junior colleagues while keeping the production service you operate safely staffed. Writing the constraints down explicitly before placing anyone, exactly as you did here, is what makes a real rota defensible when someone asks to swap.

**Question 12 (challenging) — Deduction across the whole system**

Your service comprises a frontend, an API, a queue, and a worker. You know: (i) if the queue is unhealthy, the worker cannot process jobs; (ii) if the worker cannot process jobs, user-facing exports are delayed; (iii) exports are currently delayed; (iv) the frontend and API dashboards are green. A stakeholder concludes: "Exports are delayed, so the queue must be unhealthy." Which statement about this reasoning is correct?

- A) The conclusion is valid: delayed exports imply an unhealthy queue.
- B) The conclusion is invalid: delayed exports are consistent with an unhealthy queue, but could have other causes, such as the worker failing while the queue is healthy.
- C) The conclusion is invalid because the green dashboards prove the queue is healthy.
- D) The conclusion is valid because rules (i) and (ii) chain together.

**Correct answer: B**

**Explanation:** Rules (i) and (ii) chain into "unhealthy queue → delayed exports". The stakeholder reasons in the reverse direction — from delayed exports back to an unhealthy queue — which is the classic fallacy of affirming the consequent. Delay is a *consequence* of queue failure, not a *signature* of it: the worker could be crashed, misconfigured, or starved of capacity while the queue itself is perfectly healthy, and (ii) fires just the same. Option C over-reads fact (iv): frontend and API dashboards say nothing about the queue either way. Option D correctly describes the chain but misapplies its direction. This pattern is at the heart of having an understanding of the whole system and teaching it to others: incident calls are full of confident reverse inferences ("users see errors, so it must be the database"), and the senior developer's job is to hold the causal graph the right way round, enumerate the candidate causes of the observed symptom, and design the check that discriminates between them. Practising this formally makes you faster and calmer when it happens at 2 a.m.

### Preparation tips

- **Practise on your own artefacts.** Take a real pipeline definition, dependency board, or release history from your work and actively hunt for inconsistencies for ten minutes a day. Deliberate error-checking builds exactly the muscle the assessment measures, and it makes your code reviews sharper too.
- **Anchor on the most constrained element.** In scheduling and sequencing questions, start with the item that has the fewest options — the migration that can only happen on two days, the person with leave booked. Real release planning works the same way.
- **Verbalise your deductions.** When you conclude something from a set of rules, say the inference chain aloud or write it down: "policy says X unless Y; Y is unknown; so either Y or breach." Assessments penalise plausible-sounding leaps — and so do incident reviews.
- **Watch the direction of implication.** "A causes B" plus "B is happening" does not give you A. Train yourself on this until it is reflexive; it is the single most common logical error in both cognitive tests and production incident calls.
- **Time-box ruthlessly.** Work at roughly one minute per question in practice. If a question resists you for 90 seconds, flag it and move on — accuracy on ten questions beats perfection on four, just as shipping the sprint beats gold-plating one story.
- **Use elimination.** Discard options that import facts not in the stem. Most wrong answers in this practice set smuggled in outside information; real assessments do the same.

### Common pitfalls to avoid

- **Bringing outside knowledge into closed-world questions.** Cognitive items define a miniature world of rules. Your deep knowledge of how Kubernetes or your department's change process *really* works is an asset at work but a liability here if it overrides the stated premises. Answer from the stem.
- **Confusing "could be true" with "must be true".** Many candidates select an answer that is consistent with the facts rather than the one the facts guarantee. Before choosing, ask: does the given information *force* this?
- **Reading statuses instead of rules.** As in the story-board question, errors hide in the relationship between artefacts and the rules they claim to follow, not in the artefacts alone. Check headers, orderings, and qualifiers — "finish before", "at least", "immediately after" — with the care you give a database migration script.
- **Time-sink questions.** Getting stuck on one multi-constraint puzzle and sacrificing five easier questions is the most common score-killer at every level. Skip and return.
- **Pattern-matching from experience.** Senior candidates sometimes recognise a scenario ("that's a memory leak") and answer from memory rather than from the evidence given. The test rewards fresh reasoning each time — and so does real fault-finding, where the familiar-looking incident with a different cause is the one that catches experienced engineers out.
- **Racing the adaptive difficulty.** If questions get harder, that means you are scoring well. Do not let a run of hard items rattle you into rushing.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment measures your ability to interpret, manipulate, and draw sound conclusions from numerical information of the kind your role genuinely produces. It is not a mental arithmetic contest: calculators are almost always permitted, and the numbers themselves are rarely difficult. What is being tested is whether you can select the right operation, keep track of units and denominators, read tables and charts accurately, and resist the numerically plausible but wrong conclusion.

Typical format: an online, timed test lasting 20 to 35 minutes, usually 15 to 25 questions, each presenting a small data set — a table, a chart, or a short scenario with figures — followed by multiple-choice options. Percentages, ratios, averages, rates of change, and simple projections dominate. Many platforms are adaptive, and most report accuracy and speed separately. As with all these assessments, you will usually get a short unscored warm-up.

For a senior developer on the management track, numeric reasoning is not an abstract hurdle — it is the daily language of the decisions you lead. Sprint capacity is arithmetic over person-days. Availability targets are percentages of elapsed time. Capacity planning is compound growth against a fixed limit. Error budgets, defect densities, test pass rates, build durations, and cloud costs are all numbers whose misreading has real consequences: a team that commits to 20% more than its capacity burns out; a service whose 99.5% target is confused with 99.9% promises eight times less downtime than the team has planned for. Employers use this assessment for senior developer roles because the people who plan and lead development on sets of related stories, and who operate production services, are precisely the people whose numerical judgement the organisation relies on when targets, budgets, and forecasts are set.

### How this assessment maps to your role

The assessment's dimensions map directly to the named skills in your role summary:

- **Percentages and proportions** map to **Availability and capacity management**: availability targets, utilisation percentages, and headroom calculations are the core arithmetic of ensuring the correct implementation of availability and capacity management standards, identifying capacity issues, and initiating remedial action before they become incidents.
- **Averages and weighted averages** map to **Programming and build (software engineering)** and your duty to **plan and lead development on sets of related stories**: velocity, defect density, and test pass rates are all averages, and knowing when a mean misleads (and a median or weighted figure serves better) is what makes your sprint commitments honest.
- **Rates and throughput** map to **Systems integration** and **Service support**: migration run-times, queue drain rates, and batch windows are rate problems, and co-ordinating build activities across systems means getting them right.
- **Trends and projections** map to your duty to **find ways to improve system robustness, resilience and stability**: reading an incident trend, projecting traffic growth against capacity, and quantifying the effect of an improvement are how you demonstrate that stability work is paying off.
- **Cost and efficiency figures** map to **Development process optimisation**: identifying process optimisation opportunities under guidance, and contributing to implementing solutions, almost always ends in a number — minutes saved per build, pounds saved per month — and you are the person expected to compute it correctly.
- **Interpreting data about users** maps to **User focus**: completion rates, error rates and response-time percentiles are how user needs show up in dashboards, and championing users means reading those figures with care.

### Practice questions

**Question 1 (easy) — Average sprint velocity**

Your team's completed story points over the last five sprints were: 42, 38, 45, 40, and 35. What is the team's mean velocity per sprint?

- A) 38 points
- B) 39 points
- C) 40 points
- D) 42 points

**Correct answer: C**

**Explanation:** Add the five values, then divide by the number of sprints. Step 1: 42 + 38 = 80. Step 2: 80 + 45 = 125. Step 3: 125 + 40 = 165. Step 4: 165 + 35 = 200. Step 5: 200 ÷ 5 = 40. The mean velocity is 40 points per sprint. A quick sanity check: the values range from 35 to 45, so the mean must sit inside that range, and 40 sits comfortably in the middle — a one-second check that catches most keying errors. When you present a proposed breakdown of the next set of related stories at sprint planning, this is the baseline figure you anchor the conversation on; quoting it accurately, and knowing it is a mean of a variable series rather than a guarantee, keeps the team's commitments realistic.

**Question 2 (easy) — Availability against an SLA**

Your service has a 99.5% monthly availability target. In a 30-day month, the service was down for a total of 190 minutes. First, how many minutes of downtime does the target permit, and second, did the service meet the target?

- A) 216 minutes permitted; target met with 26 minutes to spare
- B) 216 minutes permitted; target missed by 26 minutes
- C) 144 minutes permitted; target missed by 46 minutes
- D) 43.2 minutes permitted; target missed by 146.8 minutes

**Correct answer: A**

**Explanation:** Step 1: compute the minutes in a 30-day month: 30 × 24 = 720 hours; 720 × 60 = 43,200 minutes. Step 2: the target allows 100% − 99.5% = 0.5% downtime. Step 3: 0.5% of 43,200 = 0.005 × 43,200 = 216 minutes permitted. Step 4: compare with actual downtime: 190 minutes is less than 216, so the target was met, with 216 − 190 = 26 minutes of headroom. Option D is the permitted downtime for a 99.9% target (0.001 × 43,200 = 43.2 minutes) — a classic confusion, and an instructive one: each additional "nine" shrinks the allowance by a factor of five or ten, which is why agreeing the right number of nines matters so much when you ensure the correct implementation of availability standards. Knowing your service's real allowance in minutes, not just as a percentage, turns an abstract SLA into an operational budget you can manage.

**Question 3 (easy) — Defect density**

Over the last quarter, your team delivered 450 story points and the live service recorded 18 defects attributable to that work. What is the defect density per 100 story points?

- A) 2.5 defects per 100 points
- B) 4 defects per 100 points
- C) 18 defects per 100 points
- D) 25 defects per 100 points

**Correct answer: B**

**Explanation:** Step 1: compute defects per point: 18 ÷ 450 = 0.04. Step 2: scale to 100 points: 0.04 × 100 = 4. The density is 4 defects per 100 story points. Alternatively, notice that 450 points is 4.5 "hundreds", so 18 ÷ 4.5 = 4 — same answer by a different route, and having two routes is a useful self-check under time pressure. Density measures like this matter because raw defect counts mislead: a team that delivered twice as much work will usually log more defects, and only normalising by output lets you compare quarters fairly. When you find ways to improve system robustness, resilience and stability, defect density is one of the honest ways to show whether the improvement is real — and when you coach junior colleagues, explaining why we normalise is itself a small teaching moment about measurement.

**Question 4 (moderate) — Percentage improvement in build time**

Your team's average CI build time was 14 minutes. After you led a pipeline optimisation — caching dependencies and parallelising the test stages — the average dropped to 10.5 minutes. What is the percentage reduction in build time?

- A) 20%
- B) 25%
- C) 33%
- D) 35%

**Correct answer: B**

**Explanation:** Step 1: compute the absolute reduction: 14 − 10.5 = 3.5 minutes. Step 2: divide by the *original* value: 3.5 ÷ 14 = 0.25. Step 3: convert to a percentage: 0.25 × 100 = 25%. The denominator is the trap: dividing by the new value gives 3.5 ÷ 10.5 = 33.3%, which is option C — the percentage by which the new build would need to grow to return to the old time, not the reduction achieved. Percentage-change questions always hinge on "change divided by original". This calculation is the currency of your **Development process optimisation** skill: when you contribute to implementing a proposed solution, the benefit you report — "we cut build time by 25%, saving roughly 3.5 minutes × 40 builds a day ≈ 2.3 hours of waiting daily" — is what turns an engineering nicety into a case your delivery manager can defend.

**Question 5 (moderate) — Projecting traffic against capacity**

Your service's current peak load is 1,200 requests per second, and load testing shows it degrades beyond 2,000 requests per second. Peak traffic is growing at 15% per quarter. During which quarter from now will peak traffic first exceed capacity, if growth continues?

- A) The second quarter
- B) The third quarter
- C) The fourth quarter
- D) The sixth quarter

**Correct answer: C**

**Explanation:** Apply 15% compound growth step by step. After quarter 1: 1,200 × 1.15 = 1,380. After quarter 2: 1,380 × 1.15 = 1,587. After quarter 3: 1,587 × 1.15 = 1,825.05. After quarter 4: 1,825.05 × 1.15 = 2,098.8 — the first figure above 2,000. So capacity is first exceeded during the fourth quarter. Two important habits appear here. First, growth compounds: adding 15% of the *original* each time (1,200 + 4 × 180 = 1,920) would wrongly suggest the limit survives four quarters — the difference between simple and compound growth is exactly the margin that catches teams out. Second, translate the arithmetic into action: the answer is not "we have four quarters", it is "remedial work must land within three", because you want headroom before the breach, not a heroic scramble at it. This is your **Availability and capacity management** skill in its most literal form — identify capacity issues and initiate remedial action — with the initiative coming from a projection you ran months before any dashboard turned red.

**Question 6 (moderate) — Sprint capacity with absences**

You are planning a two-week sprint for a team of six developers. Each developer normally contributes 8 productive days per sprint (after ceremonies and support duties). This sprint, Aisha is on leave for 5 days, and Ben is working half-time throughout for personal reasons. The team's historical delivery rate is 1.2 story points per person-day. What is the largest whole number of story points the sprint plan should commit to within capacity?

- A) 39 points
- B) 46 points
- C) 48 points
- D) 58 points

**Correct answer: B**

**Explanation:** Step 1: baseline person-days: 6 developers × 8 days = 48. Step 2: subtract Aisha's leave: 48 − 5 = 43. Step 3: subtract Ben's reduction: half-time across 8 days means he contributes 4, not 8, so subtract another 4: 43 − 4 = 39 person-days. Step 4: convert to points: 39 × 1.2 = 46.8 points. Step 5: the question asks for the largest whole number *within* capacity, so round down: 46 points, since committing to 47 would exceed 46.8. Option A stops at person-days without converting; option C forgets both absences' interaction with the rate; option D multiplies the baseline 48 × 1.2 = 57.6 and rounds up, ignoring the absences entirely. Note the rounding direction: capacity planning rounds down, because over-commitment is the error with the higher cost — a principle worth voicing at sprint planning, where optimism is the default. Planning honestly around real availability is also a management-track behaviour: it protects Aisha's leave and Ben's arrangement from becoming silent pressure, which is part of leading a team well.

**Question 7 (moderate) — Weighted average test pass rate**

Your service's test estate contains 1,200 unit tests with a 98% pass rate, 300 integration tests with a 92% pass rate, and 100 end-to-end tests with an 85% pass rate. What is the overall pass rate across the whole estate, to one decimal place?

- A) 91.7%
- B) 95.0%
- C) 96.1%
- D) 98.0%

**Correct answer: C**

**Explanation:** A simple average of the three rates — (98 + 92 + 85) ÷ 3 = 275 ÷ 3 = 91.7% — is option A and is wrong, because the suites are different sizes. Weight by test count. Step 1: unit passes: 1,200 × 0.98 = 1,176. Step 2: integration passes: 300 × 0.92 = 276. Step 3: end-to-end passes: 100 × 0.85 = 85. Step 4: total passes: 1,176 + 276 + 85 = 1,537. Step 5: total tests: 1,200 + 300 + 100 = 1,600. Step 6: 1,537 ÷ 1,600 = 0.960625 → 96.1%. The weighted figure is dominated by the large, healthy unit suite — which is precisely why an overall pass rate can mask a sick end-to-end suite. As the senior developer who applies modern development standards and supports others in applying them, the deeper lesson is to report both the headline and the breakdown: 96.1% overall *and* 15 failing end-to-end tests, because those 15 are the ones most likely to represent broken user journeys — a **User focus** point hiding inside the arithmetic.

**Question 8 (moderate) — Reading an incident trend table**

You led a resilience improvement programme that completed at the end of March. The monthly count of production incidents for your service was:

| Month | Jan | Feb | Mar | Apr | May | Jun |
|---|---|---|---|---|---|---|
| Incidents | 12 | 15 | 9 | 8 | 7 | 6 |

Comparing the mean monthly incident count for the quarter before the improvement (Jan–Mar) with the quarter after (Apr–Jun), what is the percentage reduction, to the nearest percentage point?

- A) 33%
- B) 42%
- C) 50%
- D) 58%

**Correct answer: B**

**Explanation:** Step 1: pre-improvement total: 12 + 15 + 9 = 36; mean = 36 ÷ 3 = 12 incidents per month. Step 2: post-improvement total: 8 + 7 + 6 = 21; mean = 21 ÷ 3 = 7 incidents per month. Step 3: reduction: 12 − 7 = 5. Step 4: percentage reduction relative to the original mean: 5 ÷ 12 = 0.4167 → 41.7% → 42% to the nearest point. Comparing quarterly means rather than cherry-picking single months (Mar's 9 against Jun's 6 gives a flattering-looking but noisy 33%) is what makes the claim robust — monthly incident counts are small and volatile, and averaging over the quarter smooths that noise. When you report the results of stability work to your delivery manager or at a service review, this is the defensible version of the story; and being ready to add the caveat "three months is early evidence, not proof" is what distinguishes measurement from advocacy.

**Question 9 (challenging) — Error budget consumption**

Your team runs a service with a 99.9% availability objective measured over a rolling 30-day window. This window, the service has had two outages: one of 18.4 minutes and one of 10.4 minutes. What percentage of the 30-day error budget remains?

- A) 66.7% remains
- B) 43.2% remains
- C) 33.3% remains
- D) 14.4% remains

**Correct answer: C**

**Explanation:** Step 1: minutes in the window: 30 × 24 × 60 = 43,200. Step 2: the error budget is the permitted downtime: 100% − 99.9% = 0.1%, so 0.001 × 43,200 = 43.2 minutes. Step 3: downtime consumed: 18.4 + 10.4 = 28.8 minutes. Step 4: proportion consumed: 28.8 ÷ 43.2 = 0.6667 = 66.7%. Step 5: proportion remaining: 100% − 66.7% = 33.3% (equivalently, 43.2 − 28.8 = 14.4 minutes remaining, and 14.4 ÷ 43.2 = 33.3%). Option A is the *consumed* fraction — read the question stem twice, because "remaining" and "consumed" answers usually both appear among the options. Option D confuses minutes with percentage. Operationally, two-thirds of the budget gone mid-window is a signal to change behaviour: slow the release cadence, prioritise reliability stories, tighten review on risky changes. Using the error budget as a shared, numeric decision rule — rather than arguing from anecdote about whether the service "feels stable" — is a practical way to exercise your duty to improve robustness, resilience and stability while keeping the conversation with your product manager objective.

**Question 10 (challenging) — Cloud cost comparison**

Your service currently runs on 4 instances at £0.32 per instance-hour. After profiling, you believe 3 instances of a newer type at £0.24 per instance-hour would handle the load. Using a 730-hour month, what is the monthly saving, and what percentage of the current cost does it represent?

- A) £408.80 saving; 43.75%
- B) £408.80 saving; 56.25%
- C) £233.60 saving; 25.0%
- D) £525.60 saving; 43.75%

**Correct answer: A**

**Explanation:** Step 1: current monthly cost: 4 × £0.32 = £1.28 per hour; £1.28 × 730 = £934.40. Step 2: proposed monthly cost: 3 × £0.24 = £0.72 per hour; £0.72 × 730 = £525.60. Step 3: saving: £934.40 − £525.60 = £408.80. Step 4: percentage of current cost: 408.80 ÷ 934.40 = 0.4375 = 43.75%. Option B pairs the right saving with the wrong percentage (the *new* cost as a share of the old, 525.60 ÷ 934.40 = 56.25% — the complement); option D reports the new cost as the "saving". Keeping "what we now pay", "what we would pay", and "the difference" as three distinct labelled numbers prevents exactly this slip. In role terms, this is efficient use of resources — a criterion your **Systems design** skill explicitly asks you to review others' designs against — and public money makes the discipline sharper: a rightsizing case you can defend line by line is the kind of evidence spend controls and service assessments respect. One caveat worth adding in real life: confirm the 3-instance configuration still meets your resilience requirements (losing one of three is a 33% capacity loss; one of four is 25%) before banking the saving.

**Question 11 (challenging) — Migration throughput**

You are co-ordinating a data migration of 90,000 records into a new service. Script A processes 400 records per minute. After the first 30 minutes, you are permitted to start Script B in parallel, which processes 200 records per minute. If both scripts then run together until the migration completes, what is the total elapsed time?

- A) 2 hours 30 minutes
- B) 2 hours 40 minutes
- C) 3 hours 0 minutes
- D) 3 hours 45 minutes

**Correct answer: B**

**Explanation:** Break the job into phases. Phase 1: Script A alone for 30 minutes at 400 records/minute processes 30 × 400 = 12,000 records, leaving 90,000 − 12,000 = 78,000. Phase 2: both scripts together process 400 + 200 = 600 records/minute, so the remainder takes 78,000 ÷ 600 = 130 minutes. Total elapsed: 30 + 130 = 160 minutes = 2 hours 40 minutes. Option D is the single-script time (90,000 ÷ 400 = 225 minutes) and option A likely comes from mis-adding the phases. Phase-based rate problems recur throughout **Systems integration** work — batch windows, queue drains after an outage, backfill jobs — and the practical value of computing them precisely is scheduling: if your change window closes in 2.5 hours, this migration does not fit, and knowing that *before* you start is the difference between a controlled postponement and an abandoned half-migration. It is also the arithmetic behind a useful leadership question: "what would we need to parallelise to fit the window?" (here, starting B at time zero gives 90,000 ÷ 600 = 150 minutes — inside 2.5 hours).

**Question 12 (challenging) — Mean versus median lead time**

Your team's last five completed stories had cycle times, in days, of: 2, 3, 3, 4, and 21 (the last was blocked for two weeks awaiting an external dependency). Your delivery manager asks for "the typical cycle time" for a forecast. Which figure best answers the question, and what are the two candidate values?

- A) The mean, 6.6 days; the median is 3 days
- B) The median, 3 days; the mean is 6.6 days
- C) The mean, 4.4 days; the median is 3.5 days
- D) The median, 4 days; the mean is 8.25 days

**Correct answer: B**

**Explanation:** Compute both candidates. Mean: 2 + 3 + 3 + 4 + 21 = 33; 33 ÷ 5 = 6.6 days. Median: sort the values (already sorted) and take the middle of five: the third value, 3 days. The 21-day story is an outlier with a known special cause — an external blockage — and it drags the mean to 6.6, more than double what four of the five stories actually took. For "typical", the median (3 days) is the honest answer, so B is correct: right statistic, right values. The deeper practice is to report the median *and* mention the outlier and its cause, because the outlier is management information in its own right: external dependencies are a process risk worth escalating, which connects to identifying process optimisation opportunities. Assessments love mean-versus-median questions precisely because the mean is what a spreadsheet gives you by default and the median is what the question usually deserves; in your role, choosing knowingly between them — and saying which you chose — is part of making team data trustworthy for the people who plan around it.

### Preparation tips

- **Rebuild the classics until they are reflexes.** Percentage change (difference ÷ original), weighted averages (weight by size, never average the averages), compound growth (multiply repeatedly), and rate problems (work ÷ rate, in phases) cover most of any numeric test. Practise each with your own team's numbers — velocity, availability, build times — so the formats feel like home.
- **Name your numbers.** Under time pressure, jot a one-word label next to every intermediate figure: "allowed", "actual", "saving", "new cost". Most numeric errors are not arithmetic errors — they are grabbing the right number for the wrong role.
- **Read the question stem last as well as first.** "Remaining or consumed?" "Reduction or new value?" "Per sprint or per month?" Assessments deliberately include the answer to the neighbouring question among the options.
- **Sanity-check magnitudes.** A mean must lie within its data's range; a percentage of a total cannot exceed the total; five nines is minutes per year, not hours. A two-second plausibility check catches more errors than re-doing the calculation.
- **Use the calculator, keep the method.** Calculators remove arithmetic risk but not method risk. Write the expression before you key it.
- **Time-box.** Ninety seconds per question in practice; flag and return rather than sink. Your incident-triage instincts — stabilise, move on, come back — transfer directly.

### Common pitfalls to avoid

- **Dividing by the wrong base.** The single most common numeric error: percentage change computed against the new value instead of the original. If the options include both 25% and 33% for the same figures, this trap is present.
- **Averaging averages.** Whenever groups differ in size — test suites, teams, months of different traffic — the simple average of their rates is wrong. Weight by size, or work from raw totals.
- **Confusing simple and compound growth.** Adding 15% of the original each period understates real growth. If traffic, cost, or load "grows by X% per period", multiply period by period.
- **Ignoring units and time windows.** Minutes versus hours, per-sprint versus per-month, 30-day window versus calendar month: mismatched units are silent until the final answer is confidently wrong by a factor of 60.
- **Letting the outlier hide.** Before averaging anything, glance at the spread. One blocked story, one catastrophic month, one huge batch job can make a mean unrepresentative — and the assessment (like your delivery manager) will probe whether you noticed.
- **Rounding in the wrong direction.** Capacity commitments round down; risk allowances round conservatively. Rounding is a judgement about consequences, not a formatting choice — and questions that ask for "the largest value within" a limit are testing exactly this.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment measures how accurately you extract meaning from written material of the kind your role requires you to read — and, just as importantly, how well you resist reading in things that are not there. The classic format presents a short passage followed by statements you must judge as **True** (the passage guarantees it), **False** (the passage contradicts it), or **Cannot say** (the passage neither guarantees nor contradicts it). Variants include inference questions ("which conclusion follows?"), main-point questions, and clear-writing judgements ("which rewrite best conveys this to a non-specialist?").

Typical format: an online, timed test of 15 to 30 minutes with 20 to 40 short items. The passages in a job-specific version are drawn from your professional world: coding standards, security policies, service standards, incident reports, governance emails, and technical documentation. Scoring rewards disciplined literalism — answering from the text alone, at the exact strength the text licenses.

For a senior developer on the management track, this assessment mirrors a striking amount of your real work. You read specifications collaboratively and review them for gaps, which is verbal precision applied to requirements. You apply and teach modern development standards, which means reading normative documents — with their load-bearing distinctions between *must*, *should*, and *may* — exactly as written. You operate production services under change freezes, security advisories, and incident communications where misreading one qualifier can turn a permitted action into a breached control. And as a coach and mentor, you translate: turning a dense policy or a terse standard into something a junior developer or a non-technical stakeholder can act on, without losing the meaning in transit. Employers assess verbal reasoning at senior developer level because the cost of imprecise reading rises with seniority — your reading becomes the team's reading.

### How this assessment maps to your role

The assessment's dimensions map directly to the named skills in your role summary:

- **Literal comprehension** maps to **Modern development standards** and **Programming and build (software engineering)**: applying standards, and using agreed specifications to design, code, test and document programs, both begin with reading normative text at exactly its stated strength — a *should* is not a *must*, and "at least" is not "exactly".
- **True/False/Cannot-say discipline** maps to **Information security** and **Service support**: security policies and incident reports are documents where the difference between "the policy forbids this" and "the policy does not mention this" determines what you may do next, and where over-reading is as dangerous as under-reading.
- **Inference** maps to **Systems design** and your duty to **work with other disciplines to understand what needs to be built**: requirements documents rarely state everything explicitly, and drawing only the inferences the text supports — while flagging the gaps as questions — is how good designs start.
- **Clear-writing judgement** maps to your duties to **teach the whole system to others** and to **coach and mentor more junior colleagues**, and to **User focus**: choosing the version of a message that a mixed audience will actually understand is a daily leadership act, from incident updates to review comments.
- **Consistency checking across documents** maps to **Development process optimisation**: spotting that the team wiki contradicts the published policy is often the first step in identifying a process improvement.

### Practice questions

For each True/False/Cannot-say question, judge the statement strictly against the passage: **True** means the passage guarantees the statement; **False** means the passage contradicts it; **Cannot say** means the passage does neither.

**Question 1 (easy) — Reading a coding standard**

Passage: "All new services must be written with automated tests. Unit tests must run on every commit. Integration tests must run at least once per day. Teams should aim for unit test execution to complete within ten minutes; where this is not achievable, the team must record the reason in the service's technical documentation."

Statement: "Integration tests must run on every commit."

- A) True
- B) False
- C) Cannot say
- D) True, but only for new services

**Correct answer: C**

**Explanation:** The passage requires integration tests to run "at least once per day". Running them on every commit would *satisfy* that requirement (every commit almost certainly implies at least daily on active services), but the passage does not *require* it — and the statement claims a requirement ("must"). Does the passage contradict the statement? No: it sets a floor, not a ceiling, so per-commit integration tests are permitted but not mandated. Since the passage neither guarantees nor contradicts the statement, the answer is Cannot say. Option D is a distractor that adds a scope qualification the question never asked about. The discipline here — distinguishing "the standard permits X" from "the standard requires X" — is exactly what you exercise when you support others in applying modern development standards: juniors often read floors as ceilings or vice versa, and your correction has to be textually precise.

**Question 2 (easy) — Comprehension of an open-source policy**

Passage: "Departmental source code is open by default. Teams must publish new code in the open unless it relates to unreleased policy, security controls whose disclosure would create vulnerabilities, or algorithms used for fraud detection. Where code is withheld, the team must record the exemption and review it every twelve months, because exemptions are expected to be temporary."

Statement: "A team withholding fraud-detection code from publication is required to review that decision annually."

- A) True
- B) False
- C) Cannot say
- D) False — fraud-detection code must always be published

**Correct answer: A**

**Explanation:** Follow the chain in the text. Fraud-detection algorithms are one of the three listed grounds for withholding code, so such code may be withheld. The passage then states that *where code is withheld*, the team must record the exemption and review it every twelve months — which is a review "annually" in the statement's words. Both links are explicit, so the statement is guaranteed: True. Option D inverts the exemption. Notice that the statement paraphrases rather than quotes — "annually" for "every twelve months", "required" for "must" — and part of the skill is recognising faithful paraphrase as still True. This passage is close to the real ground of your role: you create code that is open by default and easy for others to reuse, and knowing precisely when the default can be set aside — and what process follows — is the difference between a defensible exemption and a quiet habit of secrecy.

**Question 3 (easy) — Main point of an incident email**

Email extract: "Team — following Tuesday's payments outage, the post-incident review identified that the alert for queue depth had been silenced during a previous maintenance window and never re-enabled. The fix took 18 minutes once the fault was located, but location took 74 minutes because we were blind to the queue. I have re-enabled the alert and added a weekly audit of silenced alerts to the run book. Please treat silenced alerts as changes that need an owner and an expiry, like feature flags."

What is the main point of this email?

- A) The payments outage lasted 92 minutes in total.
- B) Silenced alerts must be treated as owned, expiring changes, because an orphaned silence caused most of the outage's duration.
- C) The queue depth alert has been re-enabled.
- D) The fix for the outage took only 18 minutes.

**Correct answer: B**

**Explanation:** Every option is textually accurate or derivable (A: 18 + 74 = 92 minutes), so this is not a truth test — it is a weighting test. The email's structure gives the answer: the narrative (silenced alert → blindness → 74 of 92 minutes) exists to justify the closing instruction, "treat silenced alerts as changes that need an owner and an expiry". C and A are supporting details; D is a detail whose flattering tone might tempt a skim-reader. B captures both the instruction and its rationale, which is what "main point" means. This mirrors how you write as well as read: when you operate production services and share post-incident learning, the test of your own emails is whether a busy reader who retains one sentence retains the behavioural change — and when you review a mentee's incident write-up, "what should the reader do differently?" is the first question to ask of it.

**Question 4 (moderate) — Cannot-say discipline with a security policy**

Passage: "Critical security patches must be applied to internet-facing services within 5 working days of vendor release. For internal services, critical patches must be applied within 10 working days. High-severity patches must be applied within one month regardless of exposure. The security team may, on written request, extend any deadline where patching would disrupt a live service event, provided compensating controls are in place."

Statement: "A team that applied a critical patch to an internet-facing service 8 working days after release has breached the policy."

- A) True
- B) False
- C) Cannot say
- D) True, unless the patch was high-severity

**Correct answer: C**

**Explanation:** The default rule gives 5 working days for critical patches on internet-facing services, and 8 exceeds 5. But the passage's final sentence creates an exception: the security team may extend *any* deadline on written request with compensating controls. The statement gives no information about whether an extension was granted. If it was, there is no breach; if not, there is. The passage therefore neither guarantees nor contradicts the statement: Cannot say. Option D confuses the severity tiers — high-severity has a *longer* deadline (one month), so it is not the discriminating factor. This is the same logical shape as the branch-protection question in the cognitive section, and it recurs constantly in **Information security** work: policies are conditionals with exception clauses, and asserting "breach" before checking the exception is both a reasoning error and, in real life, a relationship error. As the person who designs solutions with security controls included, you read these documents as engineering constraints — precisely, exceptions and all.

**Question 5 (moderate) — Inference from a service standard extract**

Passage: "Teams must understand users and their needs, and should conduct research with participants who reflect the diversity of actual and intended users, including people with access needs and people with low digital confidence. Research findings must inform what the team builds. Where a team cannot recruit participants with particular access needs, it must state this limitation alongside its findings."

Which conclusion is best supported by the passage?

- A) Research that omits participants with access needs is prohibited.
- B) The standard treats research findings as binding decisions that teams must implement without change.
- C) The standard anticipates that recruiting participants with particular access needs will not always be possible, and requires transparency when it is not.
- D) Teams with experienced designers are exempt from user research.

**Correct answer: C**

**Explanation:** Work from the strength of the verbs. Conducting research with diverse participants is a *should* — strong encouragement, not an absolute — and the final sentence explicitly provides for the case where recruitment fails, requiring the limitation to be stated. That is precisely C: the standard anticipates the difficulty and mandates transparency. A over-reads: the passage requires disclosure of the gap, not prohibition of the research. B inflates "findings must inform what the team builds" into "findings are binding decisions" — informing is weaker than dictating. D has no textual basis at all. This inference discipline supports your **User focus** skill directly: you champion user research to focus on all users, and when you represent users internally you will often need to say exactly what the research does and does not establish — including its recruitment limitations — rather than the more rhetorically convenient version.

**Question 6 (moderate) — Clear-writing judgement for a mixed audience**

You are drafting a status update for a service review attended by policy colleagues and your delivery manager. Your first draft reads: "We remediated the N+1 query pathology in the eligibility microservice's ORM layer, yielding a p95 latency delta of −640ms." Which rewrite best serves this audience while staying accurate?

- A) "We fixed a database performance problem in the eligibility service. The slowest typical responses are now about two-thirds of a second faster."
- B) "We optimised the object-relational mapping layer to eliminate redundant query executions, reducing 95th-percentile latency by 640 milliseconds."
- C) "We made the eligibility service much better."
- D) "Following remediation activity, latency metrics have improved in line with expectations."

**Correct answer: A**

**Explanation:** Judge each rewrite against two criteria: can this audience understand it, and does it preserve the substance? Option A translates every technical element into plain terms — "N+1 query pathology in the ORM layer" becomes "a database performance problem"; "p95 latency delta of −640ms" becomes "the slowest typical responses are about two-thirds of a second faster" — and keeps the two facts that matter (what was fixed, how much users gain). Option B is accurate but merely re-states the jargon more grammatically; policy colleagues still cannot picture it. Option C is comprehensible but empty: it drops both the what and the how-much, so the audience cannot weigh it. Option D is worse than empty — passive, vague, and evasive-sounding, the register that makes review panels ask sharper questions. The underlying craft is one your role demands daily: you take responsibility for teaching the whole system to others, and you work with other disciplines to understand what needs to be built — both depend on translation that loses no truth. A useful test for your own writing: could a reader repeat the point accurately to someone else? A passes; B, C and D fail in three different ways.

**Question 7 (moderate) — True/False/Cannot-say on a testing policy**

Passage: "The department follows a test-driven approach. Developers write a failing test before writing the code that makes it pass, then refactor. Code reviews must confirm that tests exist and meaningfully exercise the change. Pair programming satisfies the review requirement, provided the pair records their session in the pull request description. Test coverage percentage is reported for information but no minimum threshold is mandated, because coverage figures can be gamed and high coverage does not guarantee meaningful tests."

Statement: "A change developed by a pair that recorded their session in the pull request description requires no further code review."

- A) True
- B) False
- C) Cannot say
- D) False — all changes require an independent reviewer

**Correct answer: A**

**Explanation:** The passage states that pair programming "satisfies the review requirement, provided the pair records their session in the pull request description". The statement's scenario meets exactly that proviso, so the review requirement is satisfied and no further review is required by this policy: True. Option D asserts a rule ("all changes require an independent reviewer") that the passage explicitly replaces for the pairing case — a plausible real-world norm imported from outside the text, which is precisely the reflex this question is testing. Note also what the passage says about coverage: reported, not mandated, with reasons. Being able to quote that distinction matters when you apply modern development standards and someone proposes "let's mandate 90% coverage" — the policy's own rationale (gameable metric, coverage ≠ meaningfulness) is the argument you would deploy, and reading it precisely now is what makes you persuasive later. Your responsibility for writing clean, secure code following a test-driven approach makes this passage's content, as well as its wording, part of your professional ground.

**Question 8 (moderate) — Modal verbs in a change-freeze notice**

Notice: "A change freeze applies from 17:00 Friday until 08:00 Monday. During the freeze, production deployments must not take place. Emergency fixes may be deployed only with the approval of the on-call service manager. Teams should complete their final deployments by 15:00 Friday to allow rollback time. Documentation changes are exempt from the freeze."

Which action would breach the notice?

- A) Deploying a routine feature at 16:30 Friday.
- B) Deploying an emergency fix at 22:00 Saturday with the on-call service manager's approval.
- C) Publishing updated API documentation at 10:00 Sunday.
- D) Deploying a routine feature at 18:00 Friday.

**Correct answer: D**

**Explanation:** Map each action to the notice's modal verbs. A: 16:30 Friday is before the 17:00 freeze; the 15:00 guidance is a *should* — advisory, so deploying at 16:30 is unwise but not a breach. B: emergency fixes during the freeze are a *may* with a condition — approval from the on-call service manager — and the condition is met, so no breach. C: documentation changes are explicitly exempt. D: a routine deployment at 18:00 Friday falls inside the freeze, where deployments *must not* take place, and no exemption applies — a clear breach. The question turns entirely on the normative hierarchy: *must not* (prohibition), *may … only with* (conditional permission), *should* (advice), *exempt* (out of scope). Reading these at their exact strength is a daily requirement when you operate production services under organisational controls — and when you teach the freeze rules to a junior developer, the distinction between "you'll get a breach recorded" (D) and "you'll get a raised eyebrow" (A) is exactly what they need you to articulate.

**Question 9 (challenging) — Identifying the unstated assumption**

A design review comment reads: "We should build the notification component in-house rather than adopt the cross-government notification platform, because our department's messages include appointment reminders, and missed-appointment costs are high, so we need delivery guarantees we fully control."

Which unstated assumption does this argument depend on?

- A) Missed appointments are costly to the department.
- B) The cross-government notification platform cannot provide, or cannot be relied upon to provide, the delivery guarantees the service needs.
- C) The department sends appointment reminders.
- D) Building in-house is always cheaper than adopting a platform.

**Correct answer: B**

**Explanation:** Separate what the argument states from what it needs. A and C are stated premises, not assumptions — they appear explicitly in the comment. D is an assumption the argument does not need: the comment argues from delivery guarantees, not cost, and would survive even if in-house were more expensive. The load-bearing gap is B: the conclusion "build in-house to get guarantees we control" only follows if the existing platform's guarantees are inadequate or untrustworthy — otherwise adopting it would achieve the stated need with less effort. Test it by negation: if the platform *does* reliably provide the needed guarantees, the argument collapses, which is the signature of a necessary assumption. This skill is central to reviewing the systems designs of others: most flawed build-versus-reuse arguments are internally coherent but rest on an unexamined claim about the alternative, and the reviewer's highest-value contribution is naming that claim and asking for evidence — "what did we actually establish about the platform's delivery guarantees?" — rather than debating the stated premises. It also models, for the junior developers watching the review, how to challenge an idea without attacking its author.

**Question 10 (challenging) — Consistency across two documents**

Document 1 (departmental policy): "Secrets, including API keys and database credentials, must never be stored in source code repositories, including private repositories. Secrets must be stored in the approved secrets management service and injected at deployment time."

Document 2 (your team's wiki): "For local development convenience, developers may keep a .env file with real service credentials in the repository, provided the repository is private and the file is listed in the deployment ignore list."

Which statement best describes the relationship between the documents?

- A) They are consistent, because the wiki only covers private repositories.
- B) They are consistent, because the wiki concerns local development, which the policy does not mention.
- C) The wiki contradicts the policy: the policy prohibits real credentials in any repository, private ones included, and the wiki permits exactly that.
- D) Cannot say without knowing whether the secrets management service supports local development.

**Correct answer: C**

**Explanation:** Put the two rules side by side at their stated scope. The policy's prohibition is explicitly universal over repository types: "must never … including private repositories". The wiki permits "real service credentials in the repository" when the repository is private — the precise case the policy names and forbids. The wiki's conditions (private repo, deployment ignore list) narrow the practice but cannot license it, because the policy admits no exceptions; so C is correct. A fails because privacy is the very case the policy anticipates; B fails because the policy governs what is *stored in repositories*, and a committed .env file is stored in the repository regardless of its purpose; D confuses a practical question (how to do local development well) with the textual question asked (do the documents conflict?). Finding and fixing exactly this kind of drift is where your skills compound: **Information security** (the credential exposure is real — private repositories get cloned, forked, and breached), **Modern development standards** (the wiki is teaching new joiners a non-compliant habit), and **Development process optimisation** (the right fix is not just deleting the wiki page but providing the compliant path — for example, documented use of the secrets service for local injection — because convenience gaps are why shadow practices grow).

**Question 11 (challenging) — Precise reading of accessibility requirements**

Passage: "Public sector websites and mobile applications must meet the WCAG 2.2 AA standard and must publish an accessibility statement. The statement must list any parts of the service that are not accessible, explain the reason, and describe planned remediation with dates, unless remediation would be a disproportionate burden, in which case the statement must explain the assessment behind that claim. Publishing an accessibility statement does not by itself make a service compliant."

Statement: "A service that publishes a complete and honest accessibility statement thereby meets its accessibility obligations."

- A) True
- B) False
- C) Cannot say
- D) True, provided the statement includes remediation dates

**Correct answer: B**

**Explanation:** The passage sets out two distinct obligations — meeting WCAG 2.2 AA, and publishing a compliant statement — and then closes off exactly the conflation the statement attempts: "Publishing an accessibility statement does not by itself make a service compliant." The statement claims that publication alone ("thereby") discharges the obligations; the passage directly contradicts this, so the answer is False, not Cannot say. Option D decorates the same error with a detail from the middle of the passage. The reasoning trap is subtle: everything the statement describes (complete, honest publication) is genuinely required, which creates a feeling of compliance — but required is not the same as sufficient, and the passage says so in terms. In role terms, accessibility is where your **User focus** skill carries legal weight: when you review designs or plan sets of related stories, "we've documented the inaccessible bits" is a statement about transparency, not a substitute for building accessible components — and as a mentor you will want your team to hear that distinction from you before they hear it from an auditor.

**Question 12 (challenging) — Choosing the best summary**

You want a junior developer to read this paragraph from a post-incident review and take away the right lesson: "The deployment tooling permitted a release while the database migration from the previous release was still running. The new code assumed the migrated schema, and requests that touched unmigrated rows failed. The rollback restored the old code but the half-completed migration left the table in a mixed state, extending recovery. We will add a deployment gate that verifies migration completion, and we will require all migrations to be backwards-compatible for at least one release cycle."

Which summary best captures the lesson?

- A) "Rollbacks don't work, so we should avoid them."
- B) "The outage happened because a release ran before its predecessor's migration finished; the fixes make that impossible (a completion gate) and make it survivable if it recurs (backwards-compatible migrations)."
- C) "Database migrations are risky and should be avoided where possible."
- D) "The deployment tooling was at fault, and it has now been fixed."

**Correct answer: B**

**Explanation:** A good summary preserves the causal chain and the reasoning behind both remedies. B does exactly that — and, crucially, it captures the *defence-in-depth* logic: the gate prevents the triggering condition, while backwards-compatible migrations remove the fragile assumption so that even a gate failure would not strand the service in a mixed state. A over-generalises from one hard rollback to a false rule; rollback difficulty was a consequence, not the cause. C draws a lesson of avoidance where the review's own remedy is *safer practice*, not abstinence. D is partially true but keeps only one of the two fixes and frames the incident as a tooling story, missing the code's schema assumption — the half of the lesson most relevant to developers. Summarisation under fidelity constraints is a leadership skill you use whenever you take responsibility for teaching the whole system to others: the version of an incident that your team remembers is the version you tell, and B is the telling that changes future behaviour in the right two ways.

### Preparation tips

- **Train the three-way judgement.** Most verbal errors are two-way thinking: "it sounds right, so True; it sounds wrong, so False." Practise until "the passage doesn't address this" is a fast, comfortable third verdict. Cannot-say is not a failure to decide — it is the correct description of the text's silence.
- **Underline the modals.** In every passage — practice or real — mark *must*, *must not*, *should*, *may*, *unless*, *at least*, *only*. These small words carry the rules. Your daily reading of standards and policies is free practice if you read them this actively.
- **Answer from the text, not the world.** You know how deployment freezes and secrets management really work in your department. The passage may differ. The test measures your reading, not your experience — and the discipline transfers back: reading the *actual* policy rather than the remembered one prevents real compliance mistakes.
- **For main-point and summary questions, look for the "so what".** The main point is usually the sentence that would change the reader's behaviour, not the most detailed sentence.
- **Test assumptions by negation.** For "which assumption" questions, negate each candidate and ask whether the argument still stands. The one whose negation collapses the argument is the answer.
- **Read the statement as precisely as the passage.** Half the traps are in the statement's wording — "thereby", "always", "requires", "by itself". Give both texts the same forensic attention.

### Common pitfalls to avoid

- **Importing professional knowledge.** The strongest developers are the most at risk: you know what good practice is, and you answer from that knowledge instead of the passage. If an option matches your experience but not the text, the text wins.
- **Treating "permitted" as "required" (and floors as ceilings).** "At least daily" does not mean "daily and no more"; "may deploy with approval" does not mean "must deploy". Match the modal strength exactly.
- **Missing exception clauses.** Policies are conditionals with escape hatches — "unless", "provided that", "on written request". A breach verdict that ignores an exception clause is a wrong verdict, in tests and in team disputes alike.
- **Choosing the accurate-but-minor option.** In main-point questions, several options are usually true; only one is the point. Ask what the author wants the reader to do or believe.
- **Being seduced by confident vagueness.** Options like "metrics have improved in line with expectations" sound professional and say nothing. In clear-writing questions, prefer the option a reader could accurately repeat.
- **Rushing dense passages.** Verbal tests are usually generous enough for one careful read plus targeted re-reads. One accurate pass beats three skims — the same economics as code review.

<!-- APPEND -->
