# DevOps Engineer - Psychometric Assessment Resources

## Introduction

Welcome! This guide has been created for you as a DevOps engineer working within the UK Government Digital and Data profession. Whether you are preparing for an internal assessment, applying for a new post, benchmarking your own capability, or simply curious about how psychometric assessments relate to your day-to-day work, this document will help you practise, reflect, and build confidence.

Psychometric assessments are structured, standardised exercises that measure the mental capabilities and behavioural tendencies that predict success in a role. For a DevOps engineer, that means far more than abstract puzzles. The assessments described here are job-specific: they use the kinds of artefacts you genuinely handle — pipeline configurations, monitoring dashboards, capacity forecasts, deployment strategies, incident timelines, interface specifications, and security threat models — and the kinds of decisions you genuinely make, such as transforming technical requirements into DevOps processes, managing live test environments, and identifying and resolving the issues that prevent delivery.

Why do these assessments matter for your role in particular? At your level, you deliver automated software components that form part of a development operations toolchain, and you do it without additional support. You build complex stories independently, you manage service components against business needs and key performance indicators, and you design solutions with security controls engineered to mitigate specific threats. That combination — independent technical delivery plus operational responsibility — is exactly what the four assessment types in this guide probe. Cognitive ability assessment tests whether you can reason precisely about pipelines, dependencies, and configurations under time pressure. Numeric reasoning tests whether you can handle the percentages, rates, and capacity arithmetic that KPIs and dashboards are made of. Verbal reasoning tests whether you extract exact meaning from standards, procedures, and incident reports — and whether you can judge writing quality, since your documentation is a deliverable too. Situational judgement tests the professional behaviours your level demands: balancing delivery pressure against operational safety, coordinating with other teams, escalating well, and keeping user needs in view while automating the machinery behind them.

This document is organised into four main assessment sections, each following the same pattern: an overview of what the assessment measures and its typical format, a mapping of the assessment dimensions to the specific named skills in your role summary, a substantial set of practice questions with full worked explanations, practical preparation tips, and common pitfalls to avoid.

Here is how to get the most from it. First, read each "About this assessment" section so the format holds no surprises. Second, attempt the practice questions honestly — commit to an answer before reading the explanation. Third, treat every explanation as a mini-lesson: even where you answer correctly, the worked reasoning will sharpen your technique, and many explanations connect the question back to genuine engineering practice — fair rate comparisons, boundary conditions, contract testing, blameless incident handling. Finally, use the preparation tips as prompts for self-reflection: assessment performance and professional capability draw on the same underlying habits, so time spent here repays you twice.

Take your time, enjoy the practice, and treat the whole exercise as what it is: structured reflection on a role you already know how to do. Let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive ability assessment measures the exact mental processes your role demands, using practical workplace scenarios rather than abstract puzzles. Instead of shape sequences, you reason about the everyday materials of DevOps engineering: pipeline stage graphs, deployment strategies, environment configurations, alerting rule sets, dependency chains, and automation scripts.

Typical format: an online, timed test lasting 15 to 30 minutes, with questions covering pattern recognition, logical deduction, error checking, prioritisation, and applied problem solving. Scoring is objective, comparing your responses against a norm group at a similar level, and modern platforms often adapt question difficulty to your performance — so a rising difficulty curve usually signals that you are doing well. Employers typically receive a speed-versus-accuracy breakdown rather than a single score, which rewards a working style that is both brisk and careful. Ungraded practice questions are normally offered before the timed section begins.

For a DevOps engineer, cognitive assessment is particularly relevant because your professional value is largely structured reasoning applied at speed. Transforming technical requirements into DevOps processes means decomposing a requirement into stages, dependencies, and failure modes. Managing live test environments means holding a mental model of what is deployed where, and spotting instantly when reality diverges from it. Identifying and resolving issues that prevent delivery — your role summary's phrase — is applied problem solving under pressure, usually against incomplete information. A well-designed cognitive test simulates those demands in miniature, and the techniques that earn marks (systematic elimination, boundary checking, tracing data through components) are the same techniques that make you effective at your desk.

### How this assessment maps to your role

The assessment dimensions map directly to the named skills in your role summary:

- **Pattern recognition** maps to **Service support** and **Development process optimisation**: identifying, locating, and fixing faults means recognising deviations from normal in logs, metrics, and configurations — and identifying "obvious deficiencies" in processes means seeing the recurring shapes of waste: rework loops, manual steps, queues.
- **Logical deduction** maps to **Systems integration** and **Availability and capacity management**: reasoning about what follows when one component of a toolchain changes, and tracing layered alerting and failover rules to their consequences, are deduction exercises with production stakes.
- **Error checking** maps to **Modern development standards** and **Systems design**: producing detailed designs and documenting work to required standards means auditing artefacts for internal consistency — a physical design that contradicts its logical design, a pipeline that violates the agreed conventions.
- **Prioritisation** maps to your duty to **identify and resolve issues that are preventing delivery**: with several problems live at once, you rank by impact on delivery and users, not by noise or recency.
- **Applied problem solving** maps to **Programming and build (software engineering)** and **Prototyping**: building medium-to-high complexity components, and choosing the prototyping method that answers a design question fastest, both rest on reasoning about cause, effect, and cost in the development process.

### Practice questions

**Question 1 (easy) — Pattern recognition in pipeline conventions**

Your organisation's pipeline convention requires every service pipeline to define stages in this order: `lint`, `build`, `test`, `scan`, `package`, `deploy`. Optional stages may be omitted but never reordered. You review four pipelines:

1. `lint`, `build`, `test`, `package`, `deploy`
2. `build`, `test`, `scan`, `package`, `deploy`
3. `lint`, `build`, `scan`, `test`, `package`, `deploy`
4. `lint`, `test`, `package`

Which pipeline violates the convention?

- A) Pipeline 1
- B) Pipeline 2
- C) Pipeline 3
- D) Pipeline 4

**Correct answer: C**

**Explanation:** The rule permits omission but forbids reordering, so check each pipeline for order only. Pipeline 1 omits `scan` — allowed. Pipeline 2 omits `lint` — allowed. Pipeline 4 omits three stages but keeps the survivors in canonical order — allowed. Pipeline 3 contains all six stages but swaps `scan` and `test`: a reordering, which is the one thing the convention forbids. The technique is to restate the rule precisely before scanning the data: "omission legal, inversion illegal" turns a fuzzy comparison into a crisp check for out-of-order pairs. Conventions like this exist because tooling and humans both key off stage order — a security scan that runs after packaging examines a different artefact than intended. Spotting order violations quickly is exactly the artefact-audit skill your modern development standards work depends on.

**Question 2 (easy) — Deduction from deployment gating rules**

Your deployment gates state: (i) a build may be promoted to staging only if all tests pass and the security scan reports no critical findings; (ii) a build may be promoted to production only from staging, and only after sign-off from the service owner. Build 417 is currently in staging. Which statement must be true?

- A) Build 417 has service owner sign-off.
- B) Build 417 passed all tests and had no critical security findings at promotion time.
- C) Build 417 will be promoted to production.
- D) Build 417 contains no defects.

**Correct answer: B**

**Explanation:** Reason backwards from the known state. Build 417 is in staging; rule (i) makes passing tests and a clean critical-finding scan preconditions for reaching staging, so both must have held when it was promoted — statement B is guaranteed. Statement A confuses the gates: sign-off belongs to the production promotion, which has not happened. Statement C converts eligibility into destiny — nothing says anyone will promote it. Statement D overreads what a green pipeline proves: tests passing means the checked behaviours behave; it never means "no defects". That last distinction is worth internalising beyond the test: knowing precisely what each gate does and does not certify is what makes your judgement reliable when production misbehaves despite an all-green history — the defect simply lived outside the certified area.

**Question 3 (easy) — Error checking an environment matrix**

You manage the test environments. The intended state, per the environment register, is: TST-1 runs release 3.2 with feature flags off; TST-2 runs release 3.3 with flags on; PERF-1 runs release 3.2 with flags on. Your tooling reports actual state: TST-1 — release 3.2, flags off; TST-2 — release 3.2, flags on; PERF-1 — release 3.2, flags on. How many environments diverge from the register?

- A) 0
- B) 1
- C) 2
- D) 3

**Correct answer: B**

**Explanation:** Compare each environment on both attributes. TST-1: release matches (3.2), flags match (off) — compliant. TST-2: flags match (on) but release is 3.2 against an intended 3.3 — divergent. PERF-1: release 3.2 ✓, flags on ✓ — compliant. Exactly one divergence. The disciplined method is a two-attribute checklist per row; the common error is pattern-skimming — seeing "3.2" three times in the actual state and letting the repetition read as consistency, when the register wanted variety. Environment drift detection is the daily reality of managing live test environments: a test team running against 3.2 while believing they are validating 3.3 produces confidently wrong results, which are far more expensive than obviously missing ones. The habit of reconciling intended against actual state — mechanically, attribute by attribute — is what your tooling automates and your judgement verifies.

**Question 4 (easy) — Prioritising delivery blockers**

It is 9:15am. Four issues compete for your attention: (1) the main pipeline is failing at the `package` stage, blocking every team's deployments; (2) a developer cannot access the artifact repository — their access request has sat unapproved for two days; (3) the nightly capacity report shows PERF-1 disk usage at 78%, with the alert threshold at 85%; (4) a teammate asks you to review their pull request before their 11:00 demo. What do you address first?

- A) Issue 2 — a colleague has waited longest
- B) Issue 1 — the broken pipeline blocks all delivery
- C) Issue 3 — capacity problems compound if ignored
- D) Issue 4 — the demo has the nearest fixed deadline

**Correct answer: B**

**Explanation:** Rank by impact on delivery, weighted by urgency — your role summary's phrase "identify and resolve issues that are preventing delivery" is almost a scoring rubric here. Issue 1 blocks every team's path to shipping right now: maximal impact, immediate. Issue 4 has a real deadline but a 30-minute task and a two-hour window — it fits after the pipeline triage begins or while a fix builds. Issue 2 is genuinely overdue and deserves an unblocking nudge today, but one developer's access is narrower than everyone's deployments. Issue 3 is a forecastable risk seven points below its threshold — monitor and schedule, not fire-fight. Option A prioritises by wait time (fairness), option D by deadline proximity alone; both are single-dimension rankings, and the reliable method is impact times urgency. Note the realistic nuance: "first" does not mean "only" — a good engineer triages issue 1, then interleaves the rest as the fix progresses.

**Question 5 (moderate) — Pattern recognition in a failure distribution**

Reviewing a month of pipeline failures, you tally the failing stage: `build` 4, `test` 31, `scan` 3, `package` 2, `deploy` 5. Digging into the 31 test-stage failures, 26 involve the same integration test suite, and reruns passed without code changes in 24 of those 26. What is the most reasonable interpretation?

- A) The codebase has widespread quality problems concentrated in integration.
- B) The failures cluster in one flaky integration suite — an environmental or timing instability, not primarily a code quality issue — and stabilising that suite would remove most pipeline failures.
- C) Failures are spread evenly, so no single intervention will help much.
- D) The test stage should be removed since it causes most failures.

**Correct answer: B**

**Explanation:** Read the distribution's structure layer by layer. First layer: failures concentrate overwhelmingly in one stage (31 of 45). Second layer: within that stage, they concentrate in one suite (26 of 31). Third layer — the diagnostic key: 24 of 26 pass on rerun with no code change, which is the signature of flakiness (timing races, environment contention, external dependencies), not of defective code, which fails consistently. So option B: one unstable suite generates most pipeline pain, and stabilising it is a high-leverage fix. Option A misreads flakiness as quality; option C is contradicted by the clustering; option D fires the messenger. This is your development process optimisation skill in action — "identify obvious deficiencies" means exactly this kind of Pareto reading of failure data, and the rerun-passes signal is one of the most useful diagnostic patterns in pipeline operations.

**Question 6 (moderate) — Deduction through a dependency chain**

Your toolchain has these dependencies: the deployment job requires the artifact repository; the artifact repository requires the authentication service; the monitoring stack requires the authentication service; the pipeline's `test` stage requires the test database, which does not depend on the authentication service. The authentication service goes down. Which capabilities are lost?

- A) Deployments only
- B) Deployments and the artifact repository only
- C) Deployments, the artifact repository, and monitoring — but the `test` stage can still run
- D) Everything, including the `test` stage

**Correct answer: C**

**Explanation:** Propagate the failure along the stated edges, and only the stated edges. Authentication down → artifact repository down (direct dependency) → deployment job down (transitive, via the repository). Authentication down → monitoring stack down (direct). The test database is explicitly independent of authentication, so the `test` stage survives. That yields option C. Option B forgets that dependency loss propagates to monitoring's separate branch; option D over-propagates to a component the question explicitly exempted; option A stops one hop too early. Two disciplines matter: follow transitive chains all the way (a service two hops from the failure is just as down as one hop away), and resist assuming everything is connected — real architectures, like this puzzle, have deliberate independence. This is precisely the reasoning you perform in the first five minutes of an incident: from "auth is down", predict the blast radius, and know which capabilities you still have to work with.

**Question 7 (moderate) — Error checking a design against its requirements**

A technical requirement states: "The log-shipping component must batch entries and transmit at most once per 30 seconds; transmit immediately, regardless of the interval, when a batch contains any entry of severity ERROR or above; and never hold more than 10,000 entries in memory." The detailed design you are reviewing says: entries are batched; batches transmit every 30 seconds; a batch containing an ERROR entry transmits immediately; when the in-memory count reaches 10,000, new entries are dropped with a counter incremented. Which requirement is the design's handling most questionable against?

- A) The 30-second batching interval
- B) The immediate transmission on ERROR
- C) The 10,000-entry memory bound
- D) The design fully satisfies all three requirements

**Correct answer: C**

**Explanation:** Audit each requirement against the design's mechanism. Interval: batching with 30-second transmission matches "at most once per 30 seconds". ERROR fast-path: present and correct — though note "ERROR or above" includes severities like FATAL, and a careful reviewer would confirm the design's "an ERROR entry" means "ERROR or above"; the headline concern, however, is elsewhere. Memory bound: the requirement says never *hold* more than 10,000 entries, and the design honours the number — but by *dropping new entries silently* (a counter is not a transmission). Dropping is one legitimate strategy, but the requirement is silent on loss, and a design that discards log entries — potentially the ERROR entries the second requirement treats as urgent — merits a challenge: should it instead apply backpressure, flush early, or spill to disk? Option C is where the design makes an unstated, consequential choice. This is exactly what reviewing specifications collaboratively means in your programming and build skill: the gap between "satisfies the letter" and "satisfies the intent" is where review earns its keep — and translating logical designs into physical designs, per your systems design skill, is precisely the discipline of surfacing such choices explicitly.

**Question 8 (moderate) — Choosing a deployment strategy by constraint**

A service must be updated with zero downtime; the database schema change involved is backwards-compatible; the team wants the ability to shift a small percentage of real traffic to the new version before full cutover, and to revert quickly if error rates rise. Which deployment approach best fits all the constraints?

- A) Big-bang deployment in a maintenance window announced to users
- B) Blue-green deployment with instant full cutover
- C) Canary deployment: route a small share of traffic to the new version, observe error rates, then progressively shift the remainder — reverting the routing if metrics degrade
- D) Deploy to the test environment only and soak for a week

**Correct answer: C**

**Explanation:** Convert each stated constraint into a filter. Zero downtime eliminates A, whose maintenance window is downtime by appointment. "Shift a small percentage of real traffic first" is the defining feature of a canary and precisely what blue-green's instant full cutover does not provide — B gives fast revert but all-or-nothing exposure, so the partial-traffic constraint eliminates it. D never reaches real traffic at all, failing the requirement to observe the new version under production load. C satisfies every filter: no downtime (both versions serve throughout), graduated real-traffic exposure, metric-gated progression, and rapid rollback by re-routing. The backwards-compatible schema is the enabling detail — it is what lets two versions run side by side against one database. Requirement-to-mechanism matching of exactly this kind is "transforming technical requirements into DevOps processes", and the elimination technique — treat each constraint as a veto, see what survives — is both the fastest test approach and the most defensible way to justify the choice in a design review.

**Question 9 (moderate) — Applied problem solving: intermittent integration failure**

An interface your team built between the case-management system and the document store fails intermittently: roughly 2% of transfers error with a timeout, spread across all hours, all document sizes, and both data centres — but never occurring in the test environment, where the same code path runs clean under load tests. Which hypothesis best fits all the evidence?

- A) The interface code has a logic bug in size handling.
- B) A production-only environmental difference — such as a connection limit, network policy, or resource contention absent from test — intermittently delays requests past the timeout.
- C) The test environment load tests are not running.
- D) The document store is completely down 2% of the time.

**Correct answer: B**

**Explanation:** Score each hypothesis against every observation, not just one. A logic bug in size handling (A) predicts correlation with document size — explicitly absent — and would reproduce in test, which it does not. Option D predicts failure *clusters* during down periods, not an even 2% scatter across all hours; total outages also tend to produce connection errors, not clean timeouts. Option C is an aside that explains nothing about production's behaviour — and the stem says load tests run clean, not that they do not run. Option B fits everything: an environmental delta (production-scale connection pools, firewall idle policies, noisy neighbours) produces occasional latency spikes that breach the timeout, uncorrelated with size or time of day, and invisible in a differently configured test environment. The meta-skill is disciplined differential diagnosis: the hypothesis must explain the *whole* evidence pattern, including the dog that did not bark (no size correlation, no test reproduction). This is your systems integration skill's warning made concrete: interfaces behave differently across environments, and "works in test" bounds where the fault is not.

**Question 10 (hard) — Multi-constraint maintenance scheduling**

You must schedule four operations on the live test platform in one week (Monday–Friday, one operation per day): database upgrade (U), storage migration (M), certificate renewal (C), and monitoring agent rollout (R). Constraints: (i) M requires U to be complete first; (ii) C must happen before Thursday, when the current certificate expires; (iii) R must be the final operation, so the new agents observe the platform in its end state; (iv) the database team is unavailable Monday and Tuesday, and must attend U. Which schedule satisfies all constraints?

- A) U Mon, M Tue, C Wed, R Fri
- B) C Mon, U Wed, M Thu, R Fri
- C) C Wed, U Thu, M Fri, R Fri
- D) U Wed, C Thu, M Thu, R Fri

**Correct answer: B**

**Explanation:** Apply each constraint as an eliminator. Constraint (iv): U cannot be Monday or Tuesday — eliminating option A instantly (U on Monday). Option C schedules two operations on Friday (M and R), violating one-per-day, and R fails to be strictly final if M shares its day. Option D likewise doubles Thursday (C and M) — and places C on Thursday, the expiry day, when the constraint requires completion *before* Thursday. Option B survives every check: C on Monday (before Thursday ✓, no database team needed ✓), U on Wednesday (database team available ✓), M on Thursday (after U ✓), R on Friday (final ✓). Constraint-satisfaction puzzles reward mechanical elimination over holistic staring — check each option against each rule and cross out at the first violation. The scenario itself is your week: managing live test environments *is* sequencing interdependent operations around expiry dates, dependencies, and other teams' availability, and the puzzle's lesson — the schedule that works is often not the one that "looks" natural — holds in real planning too.

**Question 11 (hard) — Layered alerting logic under a change freeze**

Alerting rules: (i) response time above 800ms sustained for 5 minutes raises a WARNING; (ii) response time above 2,000ms at any point, or error rate above 5%, raises a CRITICAL immediately; (iii) during a declared change freeze, all WARNINGs are suppressed but CRITICALs page as normal; (iv) three or more WARNINGs (including suppressed ones) within one hour escalate to a CRITICAL. A change freeze is in force. Between 14:00 and 15:00: response time exceeded 800ms sustained from 14:05–14:12, 14:20–14:26, and 14:40–14:47; it peaked at 1,850ms; error rate peaked at 3%. What paging results?

- A) None — the freeze suppresses everything and no CRITICAL threshold was crossed directly.
- B) One page: the three WARNINGs within the hour escalate to a CRITICAL under rule (iv), and CRITICALs page despite the freeze.
- C) Three pages, one per WARNING.
- D) One page from rule (ii), because 1,850ms exceeded the sustained threshold.

**Correct answer: B**

**Explanation:** Evaluate each rule against the timeline, respecting each rule's exact trigger. Rule (i): three separate sustained breaches of 800ms → three WARNINGs (at ~14:10, ~14:25, ~14:45). Rule (ii): the 2,000ms instantaneous threshold was never crossed (peak 1,850ms) and error rate stayed below 5% — no direct CRITICAL; option D misapplies the instantaneous threshold to a lower peak. Rule (iii): the freeze suppresses those WARNINGs' pages — so option C fails. But rule (iv) counts WARNINGs *including suppressed ones*: three within the hour escalate to a CRITICAL, and rule (iii) explicitly lets CRITICALs page during freezes. Net result: exactly one page, from the escalation — option B. Option A misses that suppression governs paging, not counting; the parenthetical "(including suppressed ones)" is the load-bearing clause. Layered alert policies with suppression windows and escalation counters are precisely how mature monitoring works, and tracing them accurately is the availability management skill of *managing service components against KPIs* — knowing not just that the pager went off, but exactly which rule fired and why.

**Question 12 (hard) — Evaluating an optimisation trade-off**

Your pipeline's full run takes 42 minutes: `build` 6, `test` 25, `scan` 8, `package` 3 (stages run sequentially). You propose parallelising `test` and `scan`, and splitting `test` across four parallel shards averaging 7 minutes each. A colleague objects: "Parallel shards sometimes fail unevenly — one slow shard and we gain nothing." Assuming shards behave as stated, what is the best assessment of the new pipeline duration and the objection?

- A) New duration about 16 minutes; the objection identifies a real variance risk but does not change the expected large saving.
- B) New duration about 24 minutes; the objection is decisive.
- C) New duration about 16 minutes; the objection is meaningless because parallel jobs always finish together.
- D) New duration about 33 minutes; parallelisation saves only the scan time.

**Correct answer: A**

**Explanation:** Compute the critical path. After the change, `build` (6) runs first; then `test` and `scan` run in parallel — `test` now takes max(shard times) ≈ 7 minutes, `scan` 8 minutes, so the parallel block lasts the longer of the two: 8 minutes; then `package` (3). Total ≈ 6 + 8 + 3 = 17 minutes — closest to 16; the sequential 42 minutes falls to roughly the 16–17 range, a saving of about 25 minutes. Now weigh the objection honestly: shard-time variance is real — one 15-minute straggler would stretch the block — but the parallel block's floor is set by `scan` at 8 minutes anyway, so moderate shard variance is partially absorbed, and even a doubled worst shard leaves the pipeline far faster than 42 minutes. The objection names a genuine engineering concern (worth monitoring shard balance) without overturning the expected value — exactly option A's calibrated position. Option C's "always finish together" is false; B and D miscompute the critical path. Critical-path arithmetic plus fair treatment of objections is development process optimisation practised properly: quantify the gain, acknowledge the risk, and let the numbers — not the anecdote — carry the decision.

### Preparation tips

- **Practise on your own toolchain's artefacts.** Pipeline definitions, alerting rules, environment registers, and dependency maps are the exact genres these tests imitate. Ten minutes a day of deliberate reading — "what would violate this convention? what does this rule *not* cover?" — builds both test speed and professional sharpness.
- **Restate rules precisely before applying them.** Most cognitive questions turn on one clause: "at most", "including suppressed", "before Thursday", "or above". Paraphrase the rule crisply in your head, then scan the data.
- **Use elimination on constraint questions.** Checking each option against each constraint, crossing out at the first violation, is faster and more reliable than constructing schedules or configurations from scratch.
- **Trace propagation fully but not further.** For dependency questions, follow transitive chains to their ends — and stop where the stated topology stops. Both under- and over-propagation are marked wrong.
- **Compute critical paths, not stage sums.** For anything involving parallelism, the duration is the longest path, not the total work. Sketch the graph if rough paper is allowed.
- **Rehearse under time.** Once your accuracy is solid, practise at roughly 90 seconds per question. The goal is that your systematic habits survive the clock — the test measures precisely whether care persists at speed.

### Common pitfalls to avoid

- **Answering from your organisation instead of the stem.** Your team's real conventions, thresholds, and strategies are irrelevant; the scenario's stated rules are the whole universe. This trips experienced engineers more than juniors — expertise supplies confident wrong answers.
- **Reading gates as guarantees.** "Passed all tests" certifies the tested behaviours, nothing more; "in staging" implies the staging gate was met, not the production one. Deduce only what the rules force.
- **Single-dimension prioritisation.** Ranking by wait time, seniority, or deadline proximity alone is the classic error; the defensible ordering weighs impact and urgency together.
- **Mistaking clustering for spread and flakiness for quality.** Before interpreting failure data, ask where it concentrates and whether reruns pass. The rerun signal changes the diagnosis entirely.
- **Missing the load-bearing parenthesis.** Suppression versus counting, "or above", "including" — layered rule sets hide their answers in qualifying clauses. Slow down exactly there.
- **Perfectionism on hard questions.** A ten-option constraint check you cannot finish is still worth a best guess after partial elimination. One question is never worth three questions' time — in tests or in triage.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment measures how accurately and confidently you work with the quantitative material your role produces: percentages, ratios, averages, rates, and trends, presented in tables and charts drawn from operational life — availability figures, capacity forecasts, error budgets, pipeline durations, environment costs, and KPI dashboards.

Typical format: an online, timed test of 20 to 30 minutes with 15 to 25 questions, each presenting a compact data set and asking one precise thing about it. An on-screen calculator is usually available and rough paper permitted; confirm your test's rules. Scoring is objective against a norm group at your level, with accuracy and speed reported separately — so methodical work is rewarded, and the highest-scoring approach is a reliable method executed briskly, with a sense-check at the end.

For a DevOps engineer, numeric fluency is not an adjacent skill but a core one. Your role summary asks you to manage service components "to ensure they meet business needs and key performance indicators" — and KPIs are numbers with consequences: availability percentages against targets, error rates against budgets, capacity against growth curves. Managing live test environments means cost and utilisation arithmetic; development process optimisation means quantifying durations, failure rates, and the value of proposed improvements; even user focus at your level means handling quantitative data about users honestly — traffic distributions, completion rates, latency percentiles. The questions below rehearse exactly these calculations, and every explanation shows the arithmetic step by step, including the verification habits — second routes, sense checks, unit tracking — that distinguish numbers you can defend from numbers you merely produced.

### How this assessment maps to your role

The numeric skills in the test map directly to the named skills in your role summary:

- **Percentages, thresholds, and error budgets** map to **Availability and capacity management**: converting between availability targets, downtime allowances, and headroom is the arithmetic core of managing components against KPIs.
- **Rates and durations** map to **Development process optimisation**: identifying deficiencies and supporting improvement activities requires quantifying pipeline times, failure rates, and throughput — before and after each change.
- **Ratios and proportional allocation** map to **Systems design** and environment management: sizing instances across environments, splitting capacity between components, and costing configurations are ratio problems with budgets attached.
- **Weighted averages and fair comparisons** map to **Service support** and **Systems integration**: comparing fault rates across interfaces of different volumes, or response times across periods of different traffic, demands weighting — the difference between dashboards that inform and dashboards that mislead.
- **Trend reading and forecasting** maps to **User focus** and capacity planning: quantitative data about users — growth, peaks, seasonality — drives when capacity must be added and what "meeting business needs" numerically means.

### Practice questions

**Question 1 (easy) — Reading a KPI table**

The monthly KPI report for services you support shows incident counts: Service A: 7, Service B: 12, Service C: 4, Service D: 9, Service E: 8. What is the total number of incidents across the five services?

- A) 38
- B) 40
- C) 42
- D) 44

**Correct answer: B**

**Explanation:** Add stepwise: 7 + 12 = 19; 19 + 4 = 23; 23 + 9 = 32; 32 + 8 = 40. A regrouping check: 12 + 8 = 20, 7 + 9 = 16, 20 + 16 + 4 = 40 ✓. Two routes agreeing settles it. Fast, verified totals matter because summary figures propagate: the number you compute becomes the number quoted in the service review, so a slip here becomes an organisational "fact". Bank easy marks like this quickly and accurately — in the test, speed on simple questions funds care on hard ones, and the same economy applies to your working day.

**Question 2 (easy) — Error rate against an error budget**

A service handled 400,000 requests last week, of which 1,200 failed. The service's KPI allows a failure rate of up to 0.5%. What was the actual failure rate, and is it within budget?

- A) 0.3% — within budget
- B) 0.3% — over budget
- C) 3% — over budget
- D) 0.03% — within budget

**Correct answer: A**

**Explanation:** Failure rate = failures ÷ total × 100. Step 1: 1,200 ÷ 400,000 = 0.003. Step 2: 0.003 × 100 = 0.3%. Compare with the budget: 0.3% < 0.5% — within budget, with room to spare. A mental cross-check: 1% of 400,000 is 4,000, so 1,200 failures is well under 1%; specifically 1,200 is three-tenths of 4,000, hence 0.3% ✓. The distractors are decimal-place slips — 3% and 0.03% — which is faithful to real life: dashboard misreadings are usually order-of-magnitude errors, and the 1%-anchor check ("what would 1% be?") catches them in seconds. Framing the answer against the budget, not just as a bare number, is the KPI-management habit your role summary names: the question a service owner asks is never "what is the rate?" but "are we within it, and by how much?"

**Question 3 (easy) — Mean pipeline duration**

Six runs of the release pipeline today took: 14, 17, 13, 21, 16, 15 minutes. What is the mean duration?

- A) 15 minutes
- B) 16 minutes
- C) 17 minutes
- D) 18 minutes

**Correct answer: B**

**Explanation:** Mean = total ÷ count. Total: 14 + 17 = 31; 31 + 13 = 44; 44 + 21 = 65; 65 + 16 = 81; 81 + 15 = 96 minutes. Mean = 96 ÷ 6 = 16 minutes. Sense-check: the mean must sit between the minimum (13) and maximum (21), and 16 does ✓. Worth noticing operationally: five runs cluster at 13–17 and one took 21 — the mean smooths over that outlier, so for pipeline monitoring you would track the outliers separately (what made run four slow?). Assessments test the mean; dashboards deserve the distribution. Knowing both — computing the average cleanly, and knowing what it hides — is the numeric maturity your development process optimisation work draws on when you baseline a pipeline before improving it.

**Question 4 (easy) — Proportional allocation by ratio**

You are provisioning 45 compute instances across three test environments in the ratio 4:3:2 (integration : performance : exploratory). How many instances does the performance environment receive?

- A) 10
- B) 12
- C) 15
- D) 20

**Correct answer: C**

**Explanation:** Total parts = 4 + 3 + 2 = 9. One part = 45 ÷ 9 = 5 instances. Performance = 3 parts = 3 × 5 = 15. Check by completing the allocation: integration = 20, exploratory = 10; 20 + 15 + 10 = 45 ✓. The standard method — total the parts, size one part, multiply, then add back — is quick and self-verifying. Note the positional trap: the ratio names three environments in order, and the question asks for the *middle* one; option D (20) is the integration figure waiting for a misread. In real provisioning the same discipline applies with money attached: allocation ratios get quoted in planning meetings, and the engineer who recomputes the split before ordering instances catches the transposition that the meeting minutes introduced.

**Question 5 (moderate) — Availability target to downtime allowance**

A service you support has a 99.9% availability KPI, measured monthly. For a 30-day month, how much total downtime does the target allow, to the nearest minute?

- A) 14 minutes
- B) 43 minutes
- C) 72 minutes
- D) 144 minutes

**Correct answer: B**

**Explanation:** Step 1: total minutes in the month = 30 × 24 × 60 = 43,200. Step 2: the target permits 100% − 99.9% = 0.1% unavailability. Step 3: allowance = 43,200 × 0.001 = 43.2 minutes ≈ 43 minutes. A useful anchor to memorise: 0.1% of a 30-day month is about 43 minutes, so "three nines" monthly means roughly three-quarters of an hour of allowable downtime — and 99.99% ("four nines") means a tenth of that, about 4.3 minutes. Fluency in converting targets to time allowances in both directions is the working language of availability management: when an incident consumes 20 minutes, you can immediately say "we've spent nearly half the month's error budget", which turns an abstract KPI into an operational decision about how much risk the remaining weeks can absorb.

**Question 6 (moderate) — Percentage change in deployment frequency**

Your team's deployment count rose from 48 in the first quarter to 66 in the second quarter. What was the percentage increase?

- A) 27%
- B) 33.3%
- C) 37.5%
- D) 42%

**Correct answer: C**

**Explanation:** Percentage change = (new − old) ÷ old × 100. Step 1: increase = 66 − 48 = 18. Step 2: 18 ÷ 48 = 0.375. Step 3: × 100 = 37.5%. The perennial trap is dividing by the new value: 18 ÷ 66 ≈ 27% — option A, positioned to catch it. Change is always measured from the origin. Cross-check: 37.5% is three-eighths, and three-eighths of 48 is 18 ✓, landing on 66 ✓. Deployment frequency is a standard delivery health metric, and quoting its change correctly matters when the figure supports a case — for instance, evidencing that a process optimisation you supported actually accelerated delivery. A defensible "up 37.5% quarter on quarter" survives scrutiny; a hand-waved "up about a third" invites it.

**Question 7 (moderate) — Weighted average across environments**

Response-time monitoring for an API you manage shows yesterday's averages by environment tier: production 140 ms across 90,000 requests, staging 260 ms across 8,000 requests, and the demo instance 400 ms across 2,000 requests. What was the overall average response time across all 100,000 requests?

- A) 155 ms
- B) 160 ms
- C) 200 ms
- D) 267 ms

**Correct answer: A**

**Explanation:** Averages of averages mislead when group sizes differ — weight by request count. Step 1: total time = (90,000 × 140) + (8,000 × 260) + (2,000 × 400) = 12,600,000 + 2,080,000 + 800,000 = 15,480,000 ms. Step 2: divide by total requests: 15,480,000 ÷ 100,000 = 154.8 ms ≈ 155 ms. The unweighted average (140 + 260 + 400) ÷ 3 = 267 ms — option D — overstates reality by nearly 75%, because production's 90% share of traffic dominates the true figure. Sense-check: the answer must sit near the heavily weighted tier's 140 ms, nudged up slightly by the slower minorities ✓. This is among the most consequential habits in operational reporting: whenever you aggregate across groups of unequal size — environments, endpoints, time windows — multiply out totals first. Dashboards that average averages systematically misrepresent what users experience, and your user focus skill's "quantitative data about users" is only as honest as this arithmetic.

**Question 8 (moderate) — Capacity headroom forecast**

A message queue's storage volume is 800 GB, currently at 55% utilisation. Utilisation grows by 3 percentage points per week. Your KPI requires action before utilisation reaches 85%. Assuming steady growth, how many whole weeks from now can you wait, at most, before the threshold week arrives?

- A) 8 weeks
- B) 9 weeks
- C) 10 weeks
- D) 12 weeks

**Correct answer: C**

**Explanation:** Work in percentage points, since the growth rate is given that way. Gap to threshold = 85 − 55 = 30 percentage points. Weeks to consume the gap = 30 ÷ 3 = 10 weeks: utilisation hits exactly 85% ten weeks out, so the tenth week is when the threshold arrives — you can wait at most 10 weeks, and prudent action lands before then. Converting to gigabytes confirms: 30% of 800 GB = 240 GB of headroom, at 3% × 800 = 24 GB/week, and 240 ÷ 24 = 10 ✓. Two lessons transfer to real capacity work. First, match units to the given rate (percentage points here) and verify in absolute units — the double computation catches most slips. Second, a forecast is a planning input, not a snooze button: "10 weeks at current growth" should trigger the action your KPI names while options are cheap, because growth rates change and procurement takes time.

**Question 9 (moderate) — Cost comparison for environment scheduling**

Your live test platform runs 15 instances at £0.60 per instance-hour, currently 24 hours a day. You propose running the full 15 instances only during a 12-hour working window on the 20 working days of a 30-day month, and keeping a 5-instance skeleton running at all other times. What is the monthly saving, to the nearest pound?

- A) £2,592
- B) £2,880
- C) £3,240
- D) £3,600

**Correct answer: B**

**Explanation:** Cost the current state first: hours in the month = 30 × 24 = 720; instance-hours = 15 × 720 = 10,800; cost = 10,800 × £0.60 = £6,480. Cost the proposal in two bands. Full-capacity band: 20 days × 12 hours = 240 hours, × 15 instances = 3,600 instance-hours. Skeleton band: "all other times" = 720 − 240 = 480 hours, × 5 instances = 2,400 instance-hours. Proposal total = (3,600 + 2,400) × £0.60 = 6,000 × £0.60 = £3,600. Saving = £6,480 − £3,600 = £2,880 — option B exactly. Verify by the instance-hour gap: 10,800 − 6,000 = 4,800 instance-hours saved, × £0.60 = £2,880 ✓. Two structural points repay attention. First, the two-band decomposition: mixed schedules (full fleet by day, skeleton by night and weekend) must be costed band by band — a single "hours × instances" line cannot represent them, and the most tempting distractor (£3,600, option D) is what you get by forgetting the skeleton band costs anything at all. Second, the check that "all other times" really is 480 hours guards the easiest slip: computing the skeleton over nights only and forgetting the ten non-working days. Cost models of exactly this shape justify real environment scheduling decisions, and the engineer who can walk a service owner from instance-hours to pounds — with the bands explicit — is the one whose proposal gets approved.

**Question 10 (hard) — Comparing interface failure rates fairly**

Two integrations you support ran for the same month. Interface Alpha processed 150,000 messages with 900 failures. Interface Beta processed 36,000 messages with 450 failures. Beta's owner argues Alpha needs attention first, having double the failures. Which analysis is correct?

- A) Alpha first: 900 failures exceed 450.
- B) Alpha's rate is 0.6% and Beta's is 1.25% — Beta fails more than twice as often per message, so Beta is the stronger candidate for attention on rate grounds.
- C) The rates are equal, so either order is fine.
- D) No comparison is possible without knowing message sizes.

**Correct answer: B**

**Explanation:** Volumes differ fourfold, so compare rates, not counts. Alpha: 900 ÷ 150,000 = 0.006 = 0.6%. (Anchor check: 1% of 150,000 = 1,500; 900 is six-tenths of that ✓.) Beta: 450 ÷ 36,000 = 0.0125 = 1.25%. (Anchor: 1% of 36,000 = 360; 450 is 1.25 × 360 ✓.) Beta fails roughly one message in 80; Alpha one in ~167 — Beta's reliability per message is materially worse, and option B states the comparison precisely. Option A is the raw-count fallacy. Option D confuses "another variable might matter" with "this comparison is impossible" — message size could inform a deeper diagnosis, but rates are computable and meaningful now. One professional nuance survives beyond the arithmetic: rate is the right *starting* metric, but prioritisation may still weigh impact per failure (what breaks downstream?) — which is why B is phrased "on rate grounds". Divide before comparing; then, and only then, layer on impact. That two-step is how fair operational triage actually works.

**Question 11 (hard) — Reading a trend table for capacity planning**

Weekly peak concurrent users on a service you support, over six weeks: 1,000; 1,100; 1,210; 1,331; 1,464; 1,610. The platform's tested capacity is 2,500 concurrent users. If the growth pattern continues, during which future week (counting from week 6) will peak concurrency first exceed tested capacity?

- A) 3rd week after week 6
- B) 5th week after week 6
- C) 7th week after week 6
- D) 10th week after week 6

**Correct answer: B**

**Explanation:** First characterise the trend — and check which kind of growth it is before projecting anything. The week-on-week *differences* are 100, 110, 121, 133, 146: not constant, so growth is not linear. The week-on-week *ratios* are constant: each week is its predecessor × 1.1 (1,000 → 1,100 → 1,210 → 1,331 → 1,464 → 1,610). This is 10% compound weekly growth. Now project forward from 1,610: week +1: 1,610 × 1.1 = 1,771; +2: 1,771 × 1.1 = 1,948; +3: 1,948 × 1.1 = 2,143; +4: 2,143 × 1.1 = 2,357; +5: 2,357 × 1.1 = 2,593. Week +4 stays below 2,500; week +5 reaches 2,593, the first value exceeding tested capacity — the 5th week after week 6, option B. The trap driving the later options is linear thinking: extrapolating the early ~110-per-week differences suggests the threshold is eight or more weeks away, but compound growth accelerates — its increments grow every week — and breaches thresholds far sooner than linear intuition expects. Two habits transfer directly to capacity planning: diagnose the growth pattern from ratios versus differences before forecasting, and give the answer as a specific week with the working shown, because "we have about five weeks" with the projection attached is what turns a monitoring chart into a procurement decision made in time.

**Question 12 (hard) — Error budget consumption mid-month**

A service has a 99.5% monthly availability KPI over a 30-day month. By day 12, it has accumulated 2 hours 24 minutes of downtime. What fraction of the month's total error budget has been consumed, and what does this imply for the remaining 18 days?

- A) 40% consumed — comfortable margin remains.
- B) 67% consumed — about 1 hour 12 minutes of budget remains for 18 days, so risk tolerance must tighten.
- C) 100% consumed — the KPI is already breached.
- D) 50% consumed — consumption is exactly on pace.

**Correct answer: B**

**Explanation:** Step 1: monthly error budget = 0.5% of 30 × 24 = 720 hours → 720 × 0.005 = 3.6 hours = 3 hours 36 minutes = 216 minutes. Step 2: consumed = 2 hours 24 minutes = 144 minutes. Step 3: fraction = 144 ÷ 216 = 0.6667 = 66.7% ≈ 67%. Remaining budget = 216 − 144 = 72 minutes = 1 hour 12 minutes for the remaining 18 days. Check the pace comparison: 12 of 30 days is 40% of the month elapsed, but 67% of the budget is gone — consumption is running well ahead of elapsed time, so option D's "on pace" is false, and A confuses elapsed time with consumed budget. C overstates: breached would need more than 216 minutes. Option B carries both the number and its operational meaning: with two-thirds of the budget spent at the 40% mark, the disciplined response is to tighten risk for the rest of the month — defer risky deployments, increase review rigour, watch the remaining 72 minutes like the scarce resource it now is. This is exactly what "managing service components to meet KPIs" means in practice: the arithmetic converts a target into a live decision about how much risk today can afford.

### Preparation tips

- **Drill the conversions your KPIs use.** Availability percentage ↔ downtime allowance (memorise: 0.1% of a 30-day month ≈ 43 minutes), error rate ↔ failure count, percentage points ↔ absolute units. Fluency in both directions halves your time on operational questions.
- **Weight everything aggregated across unequal groups.** Before averaging averages, ask whether group sizes differ; if they do, multiply out totals first. This single habit corrects the most consequential class of dashboard errors.
- **Divide before comparing.** Counts across different volumes are not comparable; rates are. Make "out of what?" a reflex for every figure you read or quote.
- **Distinguish linear from compound growth.** Equal *differences* mean linear; equal *ratios* mean compound. Check which pattern the data shows before projecting — compound trends breach thresholds far sooner than linear intuition suggests.
- **Verify by a second route.** For multi-step money and capacity questions, a different path to the same figure (instance-hour gap versus cost difference; percentage points versus gigabytes) is the strongest check that fits inside test timing.
- **Practise on live data.** Your own dashboards supply endless authentic questions: this month's budget consumption, the true weighted response time, the week the disk fills. The practice is simultaneously genuine KPI management.

### Common pitfalls to avoid

- **Averaging averages without weighting.** Unequal groups make the unweighted mean fiction. This is the most common error in real operational reporting, and tests target it deliberately.
- **Dividing by the new value for percentage change.** Change is measured from the original. The distractor built on the wrong base appears in nearly every test.
- **Confusing elapsed time with consumed budget.** Being 40% through the month says nothing about being 40% through the error budget. Compute both, compare explicitly.
- **Order-of-magnitude slips.** 0.3% versus 3% is a decimal point and an entirely different operational story. Anchor with "what would 1% be?" before committing.
- **Projecting compound trends linearly.** Ten per cent weekly growth doubles in under eight weeks; linear extrapolation of the early weeks misses thresholds by months.
- **Bending your arithmetic toward the options.** When your verified figure lands near but not on an option, re-verify once and choose the closest — do not distort a sound method to manufacture an exact match. In real work, show the working and stand by it.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment measures how precisely you read, interpret, and draw conclusions from the written material your role runs on: standards documents, operational procedures, incident reports, interface contracts, security guidance, service descriptions, and correspondence between teams.

The dominant question style presents a passage followed by statements to judge as **True** (supported by the passage), **False** (contradicted by it), or **Cannot say** (the passage provides insufficient information). Other styles include best-summary selection, identifying what a rule requires in a specific case, evaluating arguments (what would strengthen or weaken them), and judging which of several sentences communicates most effectively. Typical timing is 15 to 25 minutes for 20 to 30 questions, scored objectively against a norm group at your level.

The governing discipline throughout: **answer only from the passage.** Your operational experience will constantly offer plausible facts the text does not state; the test — deliberately — rewards holding those apart from what is actually written.

For a DevOps engineer, this is a job skill wearing test clothing. You transform written technical requirements into processes, which fails exactly where reading fails: a missed qualifier, an assumed default, a "should" treated as "must". You work with security guidance whose force depends on precise modal verbs, interface contracts whose guarantees live in exact wording, and incident reports whose causal chains reward — and punish — close reading. And you produce text others depend on: design documentation, runbooks, change records, incident writeups. Your role summary explicitly requires you to "effectively document all work using required standards, methods and tools", which is why the clear-writing judgement questions here are as role-relevant as the comprehension ones. Precision in, precision out.

### How this assessment maps to your role

The verbal skills in the test map directly to the named skills in your role summary:

- **Comprehension of requirements and procedures** maps to your duty to **transform technical requirements into DevOps processes**: the transformation is only as faithful as the reading — scope, conditions, exceptions, and modal force all carry design consequences.
- **True/false/cannot-say discipline** maps to **Information security**: designing solutions "with security controls included, specifically engineered to mitigate security threats" starts with representing guidance and threat information exactly — neither inflating nor diluting it.
- **Inference** maps to **Systems integration** and **Service support**: interface contracts and incident evidence rarely state every consequence; connecting stated facts into their guaranteed implications — and no further — is how faults get located and integrations get built correctly.
- **Argument evaluation** maps to **Development process optimisation** and **Prototyping**: proposals to change processes or to prototype arrive as arguments; weighing evidence, spotting unsupported bridges, and identifying what would genuinely strengthen or weaken a case is the skill that separates improvement from churn.
- **Clear-writing judgement** maps to **Systems design** and **User focus**: producing detailed designs and documenting to required standards means writing that survives a stressed 3am reader — and engaging stakeholders to collate user needs means summarising their words without distortion.

### Practice questions

**Question 1 (easy) — True/false/cannot say from an operational notice**

Passage: "The artifact repository will be upgraded on Saturday between 08:00 and 12:00. During the upgrade, existing artifacts remain downloadable, but new uploads are disabled. Pipelines that only consume artifacts will be unaffected; pipelines that publish artifacts will fail at the publish step and should be re-run after 12:00."

Statement: "During the upgrade window, a pipeline that only downloads artifacts will fail."

- A) True
- B) False
- C) Cannot say
- D) True, but only between 08:00 and 12:00

**Correct answer: B**

**Explanation:** The passage states directly that "pipelines that only consume artifacts will be unaffected" — and downloading is consuming, as the second sentence confirms ("existing artifacts remain downloadable"). The statement claims such a pipeline will fail; the passage contradicts it: False. Option D dresses the same wrong claim in a plausible time qualifier. The skill here is simply locating the deciding sentence and mapping the statement's terms onto the passage's terms (download = consume), a small translation step that many notices require. Operationally this is the exact reading you perform when a maintenance notice lands: which of *my* pipelines fall in the affected class? Answering from the notice's precise class definitions — rather than from a general sense that "upgrades break things" — is what lets you tell your teams accurately who needs to reschedule and who does not.

**Question 2 (easy) — What does the standard require in this case?**

Passage (from deployment standards): "All production deployments must be performed through the pipeline. Production deployments must have a completed change record before they begin. Emergency fixes during a declared incident may skip the change record at deployment time, provided a retrospective change record is completed within 24 hours. Deployments to test environments require neither change records nor declarations."

During a declared incident, you deploy an emergency fix to production through the pipeline at 15:00 without a change record. What does the standard require?

- A) Nothing further — emergencies are exempt from change records.
- B) A retrospective change record completed by 15:00 the next day.
- C) The deployment was non-compliant and must be rolled back.
- D) A change record before the next deployment, whenever that is.

**Correct answer: B**

**Explanation:** Parse the exemption's exact shape. The emergency clause does not abolish the change record — it *defers* it: "may skip... at deployment time, provided a retrospective change record is completed within 24 hours". Your 15:00 deployment during a declared incident is therefore compliant so far, and becomes retrospectively non-compliant only if the record is missing after 15:00 tomorrow — option B states precisely this. Option A reads the exemption as total, dropping the proviso — the single most common misreading of conditional exemptions. Option C invents non-compliance where the standard explicitly authorises the path taken. Option D substitutes a vaguer deadline for the stated one. Conditional exemptions with provisos are the load-bearing joints of operational governance — they are how standards bend without breaking during incidents — and reading the proviso as part of the permission, not an optional footnote, is what compliance actually means.

**Question 3 (easy) — Best summary of a stakeholder email**

Email from a service manager: "Thanks for the new deployment dashboard. Two things. First, the release annotations are brilliant — the support team can now correlate user complaints with releases in seconds, so please keep those. Second, the raw pod-restart counts mean nothing to my team and clutter the view; could they move to an advanced tab? If that's hard, even just renaming the column to something meaningful would help. No urgency — next sprint is fine."

Which is the best one-sentence summary?

- A) The service manager dislikes the dashboard and wants it reworked urgently.
- B) The service manager values the release annotations, asks for pod-restart counts to be moved to an advanced tab or at least renamed, and is happy to wait until next sprint.
- C) The service manager wants the release annotations removed and the restart counts kept.
- D) The support team cannot use the dashboard.

**Correct answer: B**

**Explanation:** A faithful summary preserves every decision-relevant element: the positive to protect (annotations — explicitly "keep those"), the request with its stated fallback (move restarts, or rename), and the priority signal (next sprint). Option B carries all three. Option A inverts both sentiment and urgency; option C swaps the two features' fates — a reversal error that skim-reading produces surprisingly often; option D contradicts the email's report that the support team is actively succeeding with the annotations. This is user focus in its textual form: stakeholders hand you evidence about what serves them in exactly this mixed format — praise, friction, workaround, priority — and the engineer who relays it undistorted into the backlog ("keep annotations; move or rename restarts; next sprint") turns feedback into a correctly-shaped work item. Summaries that drop the fallback or the priority create either over-engineering or false urgency.

**Question 4 (easy) — Cannot-say discipline on a security bulletin**

Passage: "A vulnerability has been identified in versions 5.0 to 5.4 of the container runtime. Version 5.5, released this week, includes the fix. Systems running affected versions should be upgraded as soon as reasonably practicable. Exploitation requires local access to the host."

Statement: "The vulnerability has been exploited in production systems."

- A) True
- B) False
- C) Cannot say
- D) False, because exploitation requires local access

**Correct answer: C**

**Explanation:** The bulletin describes the vulnerability's existence, affected versions, the fix, the recommended action, and a precondition for exploitation. Whether anyone has actually exploited it — anywhere, let alone in production — is simply not addressed. Neither supported nor contradicted: Cannot say. Option D deserves attention because it *feels* rigorous: it cites a real detail from the passage. But "requires local access" constrains *how* exploitation could occur, not *whether* it has occurred — attackers do sometimes have local access. Citing a true detail in support of an unsupported conclusion is one of the most seductive wrong-answer patterns, in tests and in security discussions alike. The professional parallel is exact: when briefing your team on a bulletin, the trustworthy formulation distinguishes "affected versions exist in our estate" (checkable fact) from "we have been compromised" (unsupported) — threat communication that outruns its evidence causes either panic or, worse, cried-wolf immunity.

**Question 5 (moderate) — Tracing a rollback procedure's branches**

Passage (rollback procedure): "If a production deployment degrades the service, first check whether the deployment included a database migration. If it did not, roll back the application version immediately. If it did, do not roll back the application alone: assess whether the migration is reversible. If reversible, reverse the migration, then roll back the application. If not reversible, roll forward with a hotfix instead, and page the data engineering rota if data integrity is in question."

A deployment has degraded the service. It included a database migration, which is not reversible. Data integrity is not in question. What does the procedure require?

- A) Roll back the application immediately.
- B) Reverse the migration, then roll back the application.
- C) Roll forward with a hotfix; do not page data engineering.
- D) Roll forward with a hotfix and page the data engineering rota.

**Correct answer: C**

**Explanation:** Walk your facts through the branches. Migration included? Yes — so the "roll back immediately" branch (A) is closed, and the procedure explicitly forbids rolling back the application alone. Reversible? No — so branch B (reverse, then roll back) is closed too. The irreversible-migration branch prescribes: roll forward with a hotfix, and page data engineering *if data integrity is in question* — a conditional attached only to the paging, and your facts say integrity is not in question. So: hotfix, no page — option C. Option D over-applies the conditional, paging unconditionally; it is the "safer-looking" wrong answer, and worth a pause: in a real ambiguous situation you might well choose to consult data engineering anyway — but the question asks what the *procedure requires*, and precise reading must come before judgement about exceeding it. Nested conditionals with per-clause qualifiers are exactly how real rollback runbooks read, and the difference between branch C and branch D at 2am is the difference between a controlled recovery and a confused one.

**Question 6 (moderate) — Inference from an interface contract**

Passage (from an interface specification): "The reporting API guarantees that results are complete for any date range ending more than 48 hours in the past. Queries covering more recent periods may return partial results while ingestion completes, and the response includes a `complete` flag indicating whether the returned data is final. Consumers requiring finality must either query ranges older than 48 hours or check the flag."

A consuming service queries yesterday's data and receives a response with `complete: true`. Which conclusion is best supported?

- A) The response data is final, because the flag says so and the specification defines the flag as indicating finality.
- B) The response data cannot be trusted, because the range is within 48 hours.
- C) The query violated the specification.
- D) The consumer must re-query after 48 hours regardless of the flag.

**Correct answer: A**

**Explanation:** Map the query onto the contract's two regimes. Yesterday is within the 48-hour window, so the *automatic* completeness guarantee does not apply — but the specification provides exactly for this case: recent queries "may return partial results" and carry a `complete` flag "indicating whether the returned data is final". The flag returned true, and the contract defines that as finality — option A follows from the specification's own terms. Option B treats the 48-hour boundary as the only mechanism, ignoring the flag the contract created for precisely this situation. Option C is unsupported — recent queries are explicitly permitted, just differently guaranteed. Option D imposes a requirement the contract does not: "must either query ranges older than 48 hours *or* check the flag" is a disjunction, and the consumer satisfied its second arm. Reading contracts as systems of complementary guarantees — rather than collapsing them to their most conservative clause — is core systems integration literacy: over-conservative readings waste re-queries and engineering time just as surely as over-liberal readings corrupt reports.

**Question 7 (moderate) — True/false/cannot say with an exception clause**

Passage (from an environments policy): "Manual configuration changes are prohibited in all managed environments. During a declared major incident, the incident lead may authorise manual changes, which must be logged and reconciled through the pipeline within 48 hours of the incident closing. Unreconciled manual changes are treated as configuration drift and reverted automatically by the nightly enforcement job."

Statement: "A manual change authorised during a major incident will be automatically reverted if it is not reconciled within 48 hours of the incident closing."

- A) True
- B) False
- C) Cannot say
- D) False — authorised changes are never reverted

**Correct answer: A**

**Explanation:** Chain the clauses. Authorised manual changes carry a reconciliation obligation: pipeline reconciliation within 48 hours of incident close. The third sentence then classifies *unreconciled* manual changes — with no carve-out for previously authorised ones — as drift, and drift is "reverted automatically by the nightly enforcement job". So an authorised-but-unreconciled change becomes, after its 48 hours, drift, and drift gets reverted: the statement is supported — True. Option D asserts an exemption for authorised changes that the passage never grants; authorisation covered the *making* of the change, not permanent immunity from reconciliation. The precise reading skill is following a term ("unreconciled manual changes") as it picks up members from earlier clauses — the authorised change *enters* that class the moment its deadline lapses. This is also, not incidentally, how well-designed configuration governance actually works, and why post-incident reconciliation belongs on your incident close checklist: the enforcement job does not read incident reports.

**Question 8 (moderate) — Clear-writing judgement in an incident summary**

Your team's standard asks incident summaries to state impact, cause, resolution, and follow-up in language a service owner can act on. Which summary best meets the standard?

- A) "There was an issue with the deployment tooling which has now been resolved. Various improvements have been identified."
- B) "Between 09:40 and 10:25, deployments were blocked for all teams because the artifact repository rejected uploads after its disk filled. We freed space and deployments resumed; a fix to the repository's retention policy is scheduled this sprint to prevent recurrence."
- C) "The artifact repository experienced an anomalous condition impacting operational throughput. Remediation was effectuated and preventative measures are under consideration."
- D) "Disk full on artifact repo, fixed. See ticket OPS-2214 for details."

**Correct answer: B**

**Explanation:** Score each against the standard's four required elements in actionable language. Option B: impact (deployments blocked, all teams, 09:40–10:25 — bounded and quantified), cause (disk full → uploads rejected), resolution (space freed, service resumed), follow-up (retention policy fix, scheduled, with a prevention rationale). Every element present, every element concrete. Option A has no impact window, no cause, and "various improvements" names nothing anyone can track. Option C is the same emptiness in formal dress — "anomalous condition" and "effectuated" are vocabulary doing the work information should do; polish is not precision. Option D actually contains real facts and a pointer, making it the best of the wrong answers — but it states no impact scope or duration, and a summary whose reader must open a ticket to learn whether they were affected has not summarised. The standard's phrase "a service owner can act on" is the test: B alone lets its reader brief stakeholders and track the follow-up unaided. This is your documentation duty — "effectively document all work using required standards" — exercised on the genre that matters most when trust is lowest.

**Question 9 (moderate) — Evaluating a process-change argument**

Passage (from a team proposal): "We should require two approvals instead of one for changes to pipeline configuration. Last quarter, two of our three pipeline outages were caused by configuration changes approved by a single reviewer who missed the error. A second reviewer would have caught both. The cost is small — configuration changes average four per week — and the outages each cost roughly a day of team-wide delivery."

Which of the following, if true, would most strengthen the argument?

- A) Both single-reviewer misses involved subtle YAML indentation errors, and in a trial last month a second reviewer caught five of five seeded errors of the same type that first reviewers had missed.
- B) Other teams in the department also have pipeline outages.
- C) The team's pipeline configuration files are stored in version control.
- D) One of the proposal's authors is the team's most experienced engineer.

**Correct answer: A**

**Explanation:** Locate the argument's load-bearing bridge: "a second reviewer would have caught both" — asserted, but on what evidence? The claim is a counterfactual, and counterfactuals are the natural weak point of incident-driven arguments. Option A shores up exactly that plank with experimental evidence: for the specific error class that caused the outages, second reviewers demonstrably catch what first reviewers miss (five of five seeded errors). It converts the proposal's assumption into a measured result. Option B says the problem is widespread, not that this remedy works; option C is background plumbing; option D is an appeal to authority, which strengthens confidence in the proposer, not the argument. The evaluation skill — find the bridge, ask what evidence would bear its weight — runs in both directions: it tells you what to demand before adopting a process change, and what to measure before proposing one. That is development process optimisation practised as engineering rather than fashion: costs quantified (four changes weekly), benefits evidenced (trial results), decision earned.

**Question 10 (hard) — Inference across an incident report**

Passage (from an incident report): "At 11:03, error rates on the payments interface rose to 12%. The on-call engineer rolled back the 10:45 payments-service release at 11:15, but error rates did not improve. At 11:32, investigation found that a dependency — the currency-rates service — had begun returning malformed responses at 11:01 following its own automated certificate renewal, which had loaded a misconfigured certificate bundle. The payments service's retry logic masked the failures in its own logs by classifying them as transient. Rates service certificates were corrected at 11:41 and error rates returned to baseline by 11:44. The 10:45 release was re-deployed at 14:00 without incident."

Which statement is best supported by the report?

- A) The 10:45 release caused the incident, and the rollback was the correct fix.
- B) The incident was caused by the currency-rates service's certificate renewal; the 10:45 release was coincidental in timing, as shown by the rollback's failure to help and the release's later clean re-deployment.
- C) The payments service's retry logic caused the malformed responses.
- D) The on-call engineer's rollback prolonged the outage.

**Correct answer: B**

**Explanation:** Assemble the causal case the report makes. The rates service began failing at 11:01 — before symptoms at 11:03 — following its certificate renewal; the rollback of the 10:45 release changed nothing (the classic exculpatory test: removing a suspected cause without effect); the correction of the certificates coincided with recovery within minutes; and the release later re-deployed cleanly. Four independent strands, all pointing at option B, which also correctly names the release's timing "coincidental" — the trap the on-call engineer reasonably fell into at 11:15, since recent releases are the right *first* suspect. Option A survives none of the evidence. Option C inverts a relationship: the retry logic masked failures in logs, obscuring diagnosis — an aggravating factor, not the cause of the malformed responses. Option D overreaches: the rollback consumed some minutes, but the report neither quantifies an alternative timeline nor criticises the action, and rolling back the newest change was defensible practice. This layered attribution — cause, trigger, masking factor, red herring — is precisely the reading your service support skill performs on real incidents, where the first plausible suspect and the actual cause differ more often than post-hoc summaries admit.

**Question 11 (hard) — Modal force across a standards extract**

Passage (from API design standards): "Services must expose a health endpoint. The health endpoint must not require authentication. Services should expose a readiness endpoint distinct from the health endpoint; where a combined endpoint is used instead, it must document which checks gate readiness. New services must not use combined endpoints after Q3. Existing services are encouraged, but not required, to migrate."

Statement: "After Q3, an existing service using a documented combined endpoint breaches the standard."

- A) True
- B) False
- C) Cannot say
- D) True, unless the service migrates

**Correct answer: B**

**Explanation:** Attach each modal to its subject with care. The post-Q3 prohibition on combined endpoints binds *new* services ("new services must not..."). For *existing* services, the final sentence sets the force explicitly: migration is "encouraged, but not required" — the strongest possible signal that non-migration is not a breach. An existing service with a combined endpoint must still meet the documentation requirement ("must document which checks gate readiness"), and the statement's service is documented. So: no requirement is violated — the statement is contradicted by the passage: False. Option D smuggles the new-service rule onto existing services via an "unless" that the standard never writes. The skill is resisting *scope creep between clauses* — each "must", "should", and "encouraged" governs exactly the population its sentence names, and standards documents rely on that precision to phase changes in without retroactive breaches. This is the reading that lets you transform requirements into processes correctly: grandfathering clauses, phase-in dates, and per-population obligations are the standard machinery of platform migrations, and misreading them generates either false compliance panics or genuine missed deadlines.

**Question 12 (hard) — Which conclusion does the research summary support?**

Passage (from a user research summary you commissioned): "We interviewed nine caseworkers and observed six using the deployment status page. All six who were observed checked the page only after a deployment had already failed, using it to answer 'what broke and when'. Interviewees consistently said they would value proactive notification of failures. Two interviewees suggested a browser extension; none mentioned email. Observed participants found the current page's timestamp column confusing, with four of six misreading UTC times as local."

Which conclusion is best supported for the team's next step?

- A) Build a browser extension, since users requested it.
- B) The evidence supports prioritising proactive failure notification and fixing the timestamp display; the notification *channel* needs further investigation, since the extension suggestion came from only two participants and alternatives went unexplored.
- C) Email notifications should be ruled out, since no interviewee mentioned email.
- D) The research is invalid because only six users were observed.

**Correct answer: B**

**Explanation:** Weigh each finding by the evidence behind it. The reactive-use pattern (six of six observed) and the desire for proactive notification ("consistently said") are the summary's strongest strands; the timestamp confusion (four of six misreading UTC) is a concrete, observed usability defect — both belong in "next steps", and option B takes them. Where B earns its keep is the channel question: two of nine suggesting an extension is a signal about *one* option, gathered without exploring alternatives — a preference glimpsed, not a design decision made. Option A converts two voices into a roadmap, the classic error of treating any user suggestion as a requirement. Option C misreads absence of mention as rejection — nobody was asked about email; silence is not data against it. Option D confuses "small sample" with "invalid": six observed users producing a unanimous behavioural pattern and a four-of-six usability failure is exactly the kind of small-n qualitative evidence that reliably identifies problems (while remaining weak for choosing between solutions — which is B's point). This is your user focus skill in written form: using qualitative and quantitative data about users honestly means matching the strength of each conclusion to the strength of its evidence, and defining the follow-up research that fits the remaining uncertainty.

### Preparation tips

- **Attach every modal verb to its exact subject.** "Must", "should", "may", "encouraged but not required" — and crucially, *which population* each one governs. Phase-ins, grandfathering, and per-environment rules are where careless reading manufactures false breaches.
- **Walk procedures with your actual facts.** For branch-heavy passages, resolve each condition explicitly (migration? reversible? integrity in question?) before looking at options — the distractors are built from adjacent branches.
- **Interrogate the flag details.** Contracts and bulletins hide their answers in mechanisms ("the `complete` flag", "including suppressed ones", "provided that..."). When a detail seems decorative, assume it is load-bearing.
- **Practise the strengthen/weaken move.** For any proposal you read this week, name its load-bearing bridge and ask what evidence would bear or break its weight. Argument evaluation is a muscle, and your process-optimisation work exercises it for real.
- **Hold "absence of mention" apart from "denial".** A passage silent on exploitation, email, or staging is silent — not negative. This single distinction resolves most cannot-say errors.
- **Read your own writing as a stressed stranger.** The clear-writing questions reward the impact-cause-resolution-follow-up shape; audit your last incident summary against it. Test preparation and documentation improvement are the same exercise here.

### Common pitfalls to avoid

- **Importing operational experience into the passage.** Your estate's real configurations and conventions are the most dangerous source of confident wrong answers — expertise fills gaps the test deliberately leaves open. The passage is the whole world.
- **Reading exemptions as unconditional.** "May skip X, provided Y" keeps Y as a live obligation. Dropping the proviso is the most common misreading of governance text, in tests and in audits.
- **Letting a true detail launder a false conclusion.** "Requires local access" is true and does not establish "never exploited". Verify that the cited detail actually supports the claimed conclusion.
- **Over-applying conditionals.** A qualifier attached to one clause ("page data engineering *if* integrity is in question") governs that clause only. The cautious-looking over-application is still marked wrong.
- **Treating user suggestions as requirements, or silence as rejection.** Research summaries reward evidence-weighted reading: behavioural patterns are strong, unprompted suggestions are weak, unexplored options are open.
- **Choosing polish over content in writing questions.** Formal vocabulary ("remediation was effectuated") is a camouflage the tests use deliberately. Judge sentences by what a reader can *do* after reading them.

## Workplace job-specific situational judgement assessment

### About this assessment

A situational judgement assessment (SJT) presents realistic workplace dilemmas and asks you to judge the effectiveness of possible responses — most effective, least effective, or a full ranking. There is no arithmetic and no passage-parsing; the material is professional judgement itself, exercised on scenarios a DevOps engineer at your level genuinely meets.

Typical format: 15 to 25 scenarios, untimed or generously timed (30 to 45 minutes), online. Your judgements are scored against those of experienced practitioners and against the behaviours UK government digital organisations value: user focus, collaboration across teams, ownership and honesty, proportionate escalation, and inclusion. SJTs are not personality tests and contain no tricks — they measure whether you recognise effective professional behaviour in context, at your level.

Your level gives the scenarios their particular shape. A mid-level DevOps engineer delivers independently — "builds complex stories without additional support" — but operates inside a web of dependencies: other teams consume your toolchain, your live test environments serve many masters, and the issues you resolve are often blocking someone else's delivery. Strong responses at your level therefore typically involve: acting decisively within your own remit while communicating proactively across its edges; balancing delivery pressure against operational and security safety with explicit, stated reasoning; escalating with evidence and options rather than problems alone; making your automation and environments serve their users, not their maintainer; and treating process rules as things you follow *and* help improve through the proper channels. Weak responses typically involve: acting beyond your remit into other teams' territory; deferring decisions that are yours to make; quiet workarounds that trade tomorrow's integrity for today's convenience; and escalation that arrives too late, too vague, or not at all. Employers use SJTs precisely because this calibration — decisive where you own, collaborative where you border, honest everywhere — predicts effectiveness better than technical skill alone.

### How this assessment maps to your role

The behaviours the SJT measures map directly to your role summary:

- **Balancing delivery against operational safety** maps to your duty to **identify and resolve issues that are preventing delivery** while you **manage live test environments**: scenarios probe when to unblock fast, when to hold a gate, and how to state the trade-off.
- **Security judgement under pressure** maps to **Information security**: designing controls "specifically engineered to mitigate security threats" is tested socially — what you do when a control is inconvenient, bypassed, or challenged by someone senior.
- **Cross-team collaboration** maps to **Systems integration** and **Programming and build**: working "on more complex integration as part of a wider team" and collaborating "to review specifications" become scenarios about boundaries, handoffs, and disagreement between teams.
- **Improving rather than circumventing process** maps to **Development process optimisation**: identifying deficiencies is rewarded; quietly routing around them is not — scenarios distinguish the two sharply.
- **Serving toolchain users** maps to **User focus** and **Prototyping**: your users include developers, testers, and ultimately citizens; scenarios test whether their needs — evidenced, not assumed — drive your choices, and whether you use prototypes to settle questions teams would otherwise argue about.
- **Documentation and handover integrity** maps to **Systems design**: effectively documenting all work is tested at exactly the moments documentation is tempting to skip.

### Practice questions

**Question 1 (easy) — A blocked release and a failing gate**

Friday, 15:30. A delivery team's release is blocked: the security scan stage is failing the build over a critical-severity finding in a third-party library the release newly introduces. The delivery manager messages you: "This is the third delay this month. Can you just disable the scan stage for this one release? We'll deal with the finding next week." What is the most effective response?

- A) Disable the stage for this release — three delays is excessive, and they have committed to a fix next week.
- B) Keep the gate; explain that a critical finding on a newly introduced library is exactly what the gate exists to catch; offer immediate help — checking for a patched library version or an alternative — and if the team believes the risk is acceptable, point them to the documented risk-acceptance route with the security team, which can be fast-tracked.
- C) Refuse and end the conversation — the gate is the gate.
- D) Disable the stage but log a ticket noting that you did so.

**Correct answer: B**

**Explanation:** The question beneath the question: who owns the decision to accept a critical security risk? Not you, and not a delivery manager under schedule pressure — which is why option B redirects to the legitimate route (documented risk acceptance by the security owner) while doing everything in your actual power: keeping the control intact, explaining its purpose without condescension, and offering the practical unblocking help (a patched version often exists) that addresses the manager's real problem. That last element matters: gates survive politically because their keepers help people through them. Option A converts schedule pressure directly into unreviewed risk, on your personal authority; "next week" commitments made at 15:30 on Friday have a documented survival rate. Option D adds an audit trail to the same failure — a logged bypass is still a bypass nobody authorised. Option C holds the line but abandons the person: no help, no route, and a delivery manager who will next time route around you rather than through you. The durable pattern: hold controls, help people, route risk decisions to their owners — kindly and fast.

**Question 2 (easy) — Your automation broke someone else's morning**

Overnight, a change you made to the shared pipeline template — tested against your own team's repositories — has broken builds for two other teams whose repositories use an older layout you did not account for. Their channels are filling with confusion. What is the most effective response?

- A) Post in the affected channels immediately: your change caused it, a revert is underway, here is the workaround meanwhile — then revert, then fix properly with the older layout accounted for, and add both layouts to the template's test matrix.
- B) Revert quietly and let the builds recover; no need to add noise to their channels.
- C) Fix forward as fast as possible — a revert would delay your own team's improvement.
- D) Explain in the channels that the older repository layout is deprecated and the teams should migrate.

**Correct answer: A**

**Explanation:** Shared infrastructure inverts the usual privacy of mistakes: your template change is other teams' outage, and they are currently spending engineer-hours investigating a mystery you can dissolve with one message. Option A does the full sequence — attribute fast (ending their wasted investigation), restore fast (revert now, improve later: the two teams' delivery outranks your enhancement's schedule), and fix the system (test matrix covering both layouts) so the class of error dies, not just the instance. Option B restores service but leaves two teams having burned a morning on a ghost, and when the cause surfaces later — it always surfaces — the quietness reads as concealment. Option C holds other teams hostage to your fix-forward confidence; reverts exist because that confidence is frequently wrong. Option D may even be right about the deprecation — but announcing it *as the explanation for breakage you caused* converts a valid roadmap conversation into blame-shifting, and the migration discussion deserves its own channel and timeline. Toolchain engineering's first law: whoever changes the shared thing owns the blast radius, loudly and immediately.

**Question 3 (easy) — Credentials in a handover script**

Taking over maintenance of an environment-provisioning script from an engineer who left last month, you find a service account password hard-coded in it — and the git history shows it has been there for two years. The script runs daily and many things may depend on that account. What is the most effective response?

- A) Replace the hard-coded password with a secrets-manager reference, and consider the matter closed.
- B) Report the exposure to the security team now; coordinate rotation of the credential with an inventory of what uses the account, so rotation does not cause an outage; move the script to the secrets manager; and check history for other secrets while you are there.
- C) Rotate the password immediately yourself — security first, dependencies later.
- D) Leave it — it has been fine for two years, and the account may be too entangled to touch.

**Correct answer: B**

**Explanation:** Two years in version control means the credential must be treated as compromised — every clone, fork, and backup of that repository carries it — so remediation is mandatory; the judgement lies in *sequencing* it safely. Option B runs the full professional chain: security team informed (exposure assessment is their remit, and there may be monitoring to check), rotation *coordinated with a dependency inventory* — because rotating a two-year-old service account blindly is how a security fix becomes a production incident — and the systemic sweep (other secrets in history) that a two-year miss makes prudent. Option A fixes the future while ignoring the past: the secret stays in history, unrotated, exposed. Option C has the right urgency and the wrong physics — "security first, dependencies later" means discovering the dependencies as outages, and the resulting chaos teaches the organisation that security fixes break things. Option D is risk acceptance by inertia, decided by the one person who just found the problem — the decision belongs to the security owner, informed. Your information security skill in one sentence: treat exposure honestly, remediate completely, sequence like an engineer.

**Question 4 (easy) — The test environment turf conflict**

You manage the live test environments. The performance testing team has PERF-1 booked all week for load tests ahead of a major release. Wednesday morning, a delivery team lead — blocked on reproducing a production bug that only manifests at realistic scale — asks you to "borrow" PERF-1 for the afternoon, arguing their production bug outranks rehearsal testing. What is the most effective response?

- A) Agree — production bugs outrank pre-release rehearsal.
- B) Refuse — the booking system exists precisely to prevent this conversation.
- C) Broker it: put the two leads in direct contact with your read on options — whether the load test schedule has slack, whether an afternoon slot can be swapped, and whether another environment could be temporarily scaled up to realistic size for the bug work — and apply whichever agreement they reach.
- D) Let the delivery team use PERF-1 without telling the performance team, restoring it before tomorrow's tests.

**Correct answer: C**

**Explanation:** The trap is accepting the framing that this is *your* adjudication to make. You own the environments; you do not own the two teams' priorities — the relative weight of a production bug against release-readiness testing is a delivery question for the people accountable for both outcomes. Option C plays the environment manager's actual role: convener and options-broker, contributing what only you know (schedule slack, swap feasibility, the scale-up alternative — which might dissolve the conflict entirely) and then executing the owners' decision. Option A and option B both adjudicate unilaterally — A by overruling a booking on one side's argument, B by hiding behind process when a ten-minute conversation might satisfy everyone; the booking system is a coordination tool, not a conversation-prevention tool. Option D is the seriously penalised one: covert use of a booked performance environment can corrupt the week's baselines (warm caches, residual data, shifted metrics) — invisible interference with another team's work product, discovered later, costs trust that environment managers run on. Pattern: own the resource, broker the priorities, never act covertly on shared ground.

**Question 5 (moderate) — Pressure from above to skip the soak**

Your deployment process includes a 24-hour soak in staging for releases touching the payment path. A senior manager — two levels up — messages you directly: "The minister's office is asking about the fee-change release. Push it to production today; the soak is overkill for a config-level change." You believe the soak has caught two payment-path regressions this year. What is the most effective response?

- A) Comply — the seniority and the ministerial context make this their call.
- B) Reply with the trade-off made concrete: the soak's catch record on this exact path, what a payment regression would mean publicly, and what an expedited-but-not-skipped option looks like (e.g. a shortened soak with targeted payment-path checks); state that you will proceed with the expedited option unless they confirm they are directing a full skip — and if they do so direct, ensure the direction and your stated concern are recorded, then comply.
- C) Refuse outright — process is process, whatever the minister's office wants.
- D) Comply, but quietly run extra manual checks yourself after the production deployment.

**Correct answer: B**

**Explanation:** Seniority can legitimately overrule a process — that is what accountability means — but it must do so *informed*, and your professional duty is to make the risk concrete before the decision, not after the incident. Option B does each piece: evidence (two catches this year, on this path — not "the process says", but "the process has caught"), consequence framing (payment errors under ministerial attention are their own news story), a constructive middle option that respects the genuine urgency, a clear default, and — if overruled — a recorded direction. Recording is not defensive theatre; it is how organisations learn which pressures produced which risks. Option A treats seniority as a substitute for the information only you hold. Option C treats process as self-justifying and offers a binary where a better option exists — refusal without alternatives reads as obstruction and usually loses. Option D is compliance plus conscience-laundering: post-deployment manual checks catch problems *after* citizens are paying wrong fees, which is the outcome the soak existed to prevent. Pattern for pressure from above: make the risk legible, offer the middle path, state your default, record the override.

**Question 6 (moderate) — A deficiency you keep working around**

For months, provisioning a new service in the toolchain has required a manual step: someone with your access must hand-edit a routing entry, taking you ten minutes and typically blocking a team for half a day until you get to it. You know it; you are quick at it; teams know to ping you. This week, while you were on leave for two days, four teams stalled. What is the most effective response?

- A) Apologise and commit to handling pings faster, including checking messages on leave.
- B) Document the manual step so any platform engineer can do it, then propose and build its automation as a prioritised piece of toolchain work, using this week's four-team stall as the evidence for prioritisation.
- C) Train one colleague as backup and continue otherwise as now.
- D) Tell teams to batch their provisioning requests for efficiency.

**Correct answer: B**

**Explanation:** This scenario tests whether you recognise yourself as the single point of failure — and whether your response fixes the system or your throughput. The situation is a textbook process deficiency of exactly the kind your development process optimisation skill exists to identify: a manual step, a queue behind one person, and now a measured cost (four teams, two days). Option B is the full engineering response: immediate resilience through documentation (anyone can execute), followed by elimination through automation — which is, precisely, your role summary's "writing software that automates systems" — with the stall as the prioritisation evidence that turns a chronic annoyance into a fundable work item. Option A doubles down on the anti-pattern: faster heroics deepen the dependency, and normalising leave-time work is a team-health cost of its own. Option C is the partial answer — a backup halves the fragility but keeps the manual toil and the queue; it is a reasonable *first week* action inside option B, not a destination. Option D optimises the queue for the bottleneck's convenience, inverting user focus: the toolchain serves the teams, not its maintainer. The identity shift being tested: from "I am quick at this step" to "this step should not exist".

**Question 7 (moderate) — Integration disagreement between teams**

You are building your team's side of an interface with another team's service. Their published contract says events arrive at most once per entity per minute; your design depends on that ceiling. In integration testing, you observe bursts of five events per entity per second. Their engineer shrugs it off in chat: "The doc's aspirational. Just handle the bursts — everyone else does." Your design would need significant rework to absorb them. What is the most effective response?

- A) Silently rework your side to handle bursts — their advice reflects reality, and arguing wastes time.
- B) Raise it as a contract question between the teams: present your test evidence, ask whether the documented ceiling or the observed behaviour is the intended contract, and route the answer to whoever owns the interface agreement — because the answer determines whether they fix the burst, you absorb it, or the contract changes for every consumer.
- C) Insist they fix their service to honour the published ceiling.
- D) Escalate to your delivery manager that the other team is unreliable.

**Correct answer: B**

**Explanation:** The engineering question — who absorbs the bursts — is answerable only after the *contract* question: what is the interface's actual promise? Option B treats it that way: evidence on the table, the discrepancy named without blame, and the decision routed to the interface's owner — because a contract that "everyone" quietly patches around is not a contract, and the next consumer will hit the same rock. Note what B does not assume: perhaps the bursts are a bug they will fix (your design stands); perhaps the doc is stale (it should change, visibly, for all consumers — and your rework becomes a planned, justified cost). Option A privately absorbs the cost and, worse, entrenches the divergence between documentation and behaviour — "everyone handles it" is how integration landscapes rot. Option C asserts your preferred answer to a question you do not own; the published doc supports you, but "insist" skips the possibility that the doc is simply wrong. Option D escalates a technical discrepancy as a relationship complaint, poisoning a well you will drink from for years. This is "working on more complex integration as part of a wider team" in miniature: contracts are shared property, and discrepancies between promise and behaviour are raised, decided, and documented — never quietly absorbed.

**Question 8 (moderate) — The prototype that would settle it**

Your team has spent two sprint-planning sessions arguing about the new deployment dashboard: one faction wants deployment status grouped by team, the other by service. Both argue from conviction about what "users obviously want"; no one has asked the users — delivery teams and service owners. A third planning session is scheduled. What is the most effective contribution?

- A) Side with the more senior faction to end the deadlock.
- B) Propose a compromise: a toggle offering both groupings.
- C) Propose replacing the third debate with evidence: two clickable mock-ups, an hour with three or four actual users watching them attempt real tasks ("is anything blocking your team's release right now?"), and a decision at the session from what is observed.
- D) Suggest the team defer the dashboard until consensus forms naturally.

**Correct answer: C**

**Explanation:** Two sessions of conviction-based argument about user preference is a research question wearing a debate costume, and your role summary arms you for exactly this: "approach prototyping as a team activity, actively soliciting prototypes and testing with others", plus user focus's "identify and engage with users to collate user needs evidence". Option C converts the argument's currency from seniority and rhetoric to observed behaviour — cheap mock-ups, real users, real tasks — and the task framing matters: watching a service owner *hunt* for blocked releases reveals the right grouping faster than asking their opinion of two designs. It also, quietly, is inclusive: evidence flattens hierarchies that debate amplifies. Option A resolves the deadlock socially while leaving the design question to luck. Option B is the seductive one: the toggle feels like listening to everyone, but it doubles maintenance surface, defers the information-architecture question to every future feature ("which grouping does this new filter apply to?"), and is frequently a decision-avoidance artefact — compromises should be chosen from evidence too, not instead of it. Option D hopes consensus will emerge from the same inputs that failed twice. Pattern: when teams argue about users, stop arguing and go watch some.

**Question 9 (moderate) — Mid-incident, out of your lane**

A production incident is running: the case-management service is degraded, and the incident lead — from the application team — has the response in hand. Monitoring dashboards you built are in heavy use. Watching the metrics, you notice something the responders have not mentioned: the degradation began exactly when a platform-level autoscaling change you know about rolled out, and the connection-pool graph shape matches that mechanism, not the database-index theory the team is pursuing. You are not on the incident roster. What is the most effective response?

- A) Stay out of it — the incident has a lead, a roster, and a working theory, and interruptions cost focus.
- B) Post your observation in the incident channel, concisely: the timing correlation, the graph pattern, the autoscaling change reference — offered as a hypothesis for the lead to triage, and make yourself available if they want to pull the thread.
- C) Directly message individual responders that their database theory is wrong.
- D) Start investigating the autoscaling theory yourself and post results when you have proof.

**Correct answer: B**

**Explanation:** Incident structure exists to concentrate decision-making, not to filter out information — and you hold information with a mechanism, a timing correlation, and provenance the responders lack (you know the autoscaling change happened; they may not). Option B delivers it in the form incident leads can actually use: one concise post, in the channel of record (not private side-conversations), framed as hypothesis rather than verdict, with the decision about pursuing it left where it belongs — the lead's triage. That framing discipline matters: confident-sounding alternative theories can hijack an incident as easily as help it, and "for the lead to triage" is what keeps your contribution additive. Option A confuses respecting structure with withholding evidence; the roster governs who *decides*, not who may *observe*. Option C fragments the response into private channels and frames help as correction — the surest way to have a right idea rejected. Option D delays shareable information in pursuit of private certainty: during incidents, a falsifiable hypothesis now outvalues proof in an hour, because the team can check the connection-pool theory in minutes with hands you do not have. Pattern: contribute evidence through the structure, promptly, labelled with its confidence — then let the structure work.

**Question 10 (hard) — What the metrics say versus what gets reported**

Preparing the quarterly service review, your manager drafts a slide claiming the deployment pipeline "now delivers 99% success". Your data says: 99% includes automatic retries; first-attempt success is 91%, and the retry storms are themselves degrading pipeline throughput at peak times — a problem you are trying to get prioritised. The 99% is technically defensible. The review decides next quarter's platform investment. What is the most effective response?

- A) Let the slide stand — 99% is technically true, and it reflects well on the team's work.
- B) Before the review, show your manager both numbers and the retry-storm data; propose the slide present first-attempt success alongside effective success, framed as "reliability is high, but retry load is the next problem worth investment" — which is both more honest and a stronger case for the prioritisation you need.
- C) Say nothing beforehand, but correct the figure from the floor if the review discusses it.
- D) Raise the discrepancy with the review board directly, bypassing your manager.

**Correct answer: B**

**Explanation:** Two duties collide: honest measurement, and effective advocacy for platform investment — and option B notices they point the same way. A 99%-with-retries figure that buries first-attempt truth does not just shade honesty; it *destroys the evidence for your own priority* — a board told "99% success" will not fund retry-storm work, and when throughput degradation surfaces later, the slide becomes the reason nobody acted. Presenting both figures with the storms as "the next problem" converts an awkward correction into a stronger narrative: high reliability, clear-eyed team, fundable next step. The private-first route respects your manager — most inflated slides are enthusiasm, not deception, and correcting them pre-review preserves both accuracy and relationship. Option A trades a quarter's investment decision for a quarter's comfort. Option C ambushes your manager publicly with information you chose to withhold — maximally corrosive, and it makes the correction about the two of you rather than the pipeline. Option D escalates past a person who has not yet declined to fix anything; bypass is for after the direct route fails, not before it is tried. Pattern: metrics that flatter by omission are challenged privately, early, and constructively — and the honest number is usually the more useful one.

**Question 11 (hard) — The convenient exception becoming precedent**

Last month, under time pressure and with your agreement, a delivery team deployed to the test environment through a temporary manual route while the pipeline's provisioning bug was being fixed. The bug has been fixed for two weeks. Today you notice the team is still using the manual route — it is faster for them — and a second team, having seen it work, has started doing the same. Environment state has begun drifting from the configuration records. What is the most effective response?

- A) Shut off the manual route immediately without discussion — the exception has expired.
- B) Say nothing — the teams are delivering, and the drift is manageable so far.
- C) Contact both teams: the exception existed for a bug now fixed, the drift it causes is already measurable, and the route closes on a stated date days away — paired with asking what makes the manual route faster, because that speed gap is pipeline feedback worth fixing so the sanctioned route becomes the attractive one.
- D) Report both teams' non-compliance to their delivery managers.

**Correct answer: C**

**Explanation:** This scenario is about how exceptions die — and what their afterlife teaches. A temporary bypass that outlives its justification, then spreads by observation, is a norm being born; wait longer and there will be three teams and an incident traceable to drifted state. Option C closes it properly: rationale restated (the *why* of the closure, not just the closure), a firm near date (notice respects the teams' in-flight work; open-endedness would just continue the drift), and — the element that distinguishes good platform engineering — genuine curiosity about *why the workaround wins*. "The manual route is faster" is user feedback about your pipeline from users voting with their feet; fix that gap and enforcement becomes unnecessary, which is the only kind of enforcement that scales. Option A is within your rights and needlessly expensive: a surprise shutoff mid-sprint converts two collaborating teams into opponents of the next control. Option B is how organisations acquire unauditable environments — "manageable so far" is drift's marketing slogan. Option D escalates before conversing, spending relationship capital on a problem a message would fix, and skips your own share of the story: you agreed to the exception and let it outlive its reason. Pattern: close exceptions with dates and reasons, and treat every popular workaround as a requirements document.

**Question 12 (hard) — Least effective: the post-incident actions list**

An incident review has produced five agreed actions after a bad outage: one is yours (add an alert on the failure mode), two belong to the application team, one to the database team, and one — updating the shared runbook — is unassigned. Three weeks later, checking before the follow-up meeting: your alert is done; the application team has done one of two; the database action is not started; the runbook is untouched, and a near-miss last week would have been caught by the missing database action. Which response would be **least effective**?

- A) Bring the status picture to the follow-up meeting, including the near-miss as evidence of live risk, and propose the unassigned runbook action get an owner and date.
- B) Since your own action is complete, report your part done at the meeting and leave the other teams' actions to their own management chains.
- C) Before the meeting, message the database team's lead: flag the near-miss connection to their unstarted action and ask whether help, context, or re-prioritisation would move it.
- D) Update the runbook yourself where you have the knowledge, noting the sections needing application-team input, and bring the remainder to the meeting.

**Correct answer: B**

**Explanation:** The stem asks for *least* effective — the format that punishes skimming — and option B is the weakest despite being procedurally spotless. Its flaw is the boundary it draws: "my action, my report" treats incident follow-up as a set of private chores rather than a shared defence against recurrence — and the near-miss means recurrence is actively knocking. At your level, having noticed that the risk is live, that an action is unowned, and that another is stalled, *the noticing creates a duty*: not to do other teams' work, but to make the system-level status visible and moving. The other options all express that duty proportionately: A is the meeting-level version (status, evidence, ownership proposal — classic good practice); C is the collegial pre-meeting version, offering help before spotlight, which often unsticks things fastest; D directly executes the unowned work where you are competent, honestly bounded where you are not. None of them oversteps into others' remits; all of them treat "the outage should not happen again" as everyone's deliverable. The theme, which recurs across senior-leaning SJTs: completed-my-bit compliance scores below system-level ownership — because incidents do not respect team boundaries, and neither can follow-up.

### Preparation tips

- **Name the behaviour patterns until they are reflexes.** At your level: act decisively inside your remit, broker rather than adjudicate at its edges, make risk legible before decisions, close exceptions with dates and reasons, route risk acceptance to its owners, and treat workarounds as requirements feedback. Recognising the pattern makes the options sort themselves.
- **Check whose decision it is before choosing an action.** Many scenarios hinge on ownership: risk acceptance belongs to security owners, priority conflicts to delivery leads, contract questions to interface owners. Options that decide someone else's question — even correctly — score below options that route it with evidence.
- **Read the stem's question twice.** "Most effective", "least effective", and ranking formats coexist in one test; a large fraction of lost marks are inverted answers to misread stems.
- **Trace each option a month downstream.** The tempting wrong answers optimise the moment (speed, comfort, deference) at costs that appear later: precedent, drift, trust, unfunded priorities. The scoring rewards the month view.
- **Mine your own week for scenarios.** Every gate challenge, environment conflict, and stalled action item you handle is SJT practice with real feedback. Notice what worked, name why, and you are studying for the test and the job simultaneously.
- **Answer as the professional you are at work, not an idealised hero or a cautious minimum.** SJT norms come from experienced practitioners; your genuine best judgement, applied consistently, is the calibration the test measures.

### Common pitfalls to avoid

- **Deciding questions you do not own.** Accepting security risk to be helpful, adjudicating other teams' priorities, declaring contracts by preference — decisiveness misapplied across ownership lines is the most common mid-level error, precisely because decisiveness is your strength.
- **Quiet fixes on shared ground.** Silent reverts, covert environment use, privately absorbed contract divergences, unannounced workarounds — anything that leaves colleagues' mental model of shared systems false scores badly, however technically sound the fix.
- **Compliance theatre.** Logged bypasses, post-hoc manual checks, completed-my-bit reporting while the system risk lives on — the tests distinguish the appearance of diligence from its substance, and so do incident reviews.
- **Escalation at the wrong time or altitude.** Too late (after the pattern set), too early (before the direct conversation), too high (bypassing people who have not yet declined to act), or as relationship complaint rather than evidence. Match the escalation to what the situation has actually demonstrated.
- **Treating process as self-justifying — or as optional.** "The gate is the gate" without help loses the argument that keeps gates alive; skipping the gate under pressure loses the protection. The scored behaviour is holding controls *while* helping people through them and improving them through legitimate channels.
- **Forgetting your users when you are the platform.** Developers, testers, and delivery teams are your users; options that optimise the toolchain for its maintainer — batched requests, maintainer-convenient defaults, dashboards nobody validated — fail the user-focus behaviours the framework names.

## Conclusion

Well done for working through the whole guide — four assessment disciplines, nearly fifty scenarios, and a great deal of deliberate reasoning about the work you do every day.

Look at what you have practised. In the cognitive section, you audited pipelines and environment registers against their intended state, propagated failures through dependency chains exactly as far as the topology allowed, matched deployment strategies to constraints by elimination, and computed critical paths instead of stage sums. In the numeric section, you converted availability targets into downtime allowances, tracked error-budget consumption against elapsed time, weighted averages by traffic, compared failure rates fairly across unequal volumes, and recognised compound growth before it embarrassed a linear forecast. In the verbal section, you held exemptions to their provisos, attached each modal verb to exactly the population it governs, traced rollback branches with per-clause conditionals, and weighed research conclusions by the strength of their evidence. And in the situational judgement section, you rehearsed the judgement calls that define mid-level operational careers: holding a security gate while helping people through it, owning the blast radius of a shared-template change, making risk legible to seniority before a decision, closing a workaround with a date and a lesson, and contributing evidence to an incident without hijacking its structure.

None of it was generic. Every question was constructed from the named skills in your role summary — availability and capacity management, development process optimisation, information security, modern development standards, programming and build, prototyping, service support, systems design, systems integration, and user focus — and from your level's defining duties: transforming requirements into processes, building complex stories without support, managing live test environments, and resolving whatever is preventing delivery. Time spent here was therefore double-counted in your favour: assessment preparation and professional sharpening in the same hours.

Keep both compounding. The habits that earn test marks — restating rules precisely, weighting before averaging, checking whose decision a question is, tracing options a month downstream — are the same habits that make your dashboards honest, your designs reviewable, and your escalations effective. Practise them on live material: your own pipelines, your own KPI reports, your own next awkward conversation about a gate.

On assessment day: read every stem twice, keep bases and units explicit, answer from the passage rather than from your estate, and bring the same calibrated judgement you bring to a Tuesday incident — decisive where you own, collaborative at the edges, honest everywhere. That combination is what these assessments are built to detect, and you exercise it professionally already.

Good luck — and enjoy noticing, next time you reconcile an environment register or challenge a flattering metric, that you are practising still.
