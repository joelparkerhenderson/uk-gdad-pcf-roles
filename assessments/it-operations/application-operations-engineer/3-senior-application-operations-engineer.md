# Senior Application Operations Engineer - Psychometric Assessment Resources

## Introduction

Welcome! This guide has been created for you as a senior application operations engineer working within the UK Government Digital and Data profession. At your level, you deal with more complex issues: you are responsible for code deployment and for co-ordinating change-based activities such as taking services live, and depending on a project's complexity and business impact, you may manage and maintain significant aspects of an application in your own right. Whether you are preparing for an internal assessment, applying for a promotion or a move, benchmarking yourself against the capability framework, or simply keeping your professional edge sharp, this document will help you practise, reflect, and build confidence.

Psychometric assessments are structured, standardised exercises that measure the mental capabilities and professional judgement that predict success in a role. For a senior application operations engineer, that means far more than abstract puzzles. The assessments described here are job-specific: they use the artefacts you genuinely handle — change requests, configuration records, availability and capacity reports, deployment plans, test results, incident timelines, and performance statistics — and the decisions you genuinely make, such as assessing the impact of a change, sequencing a go-live, diagnosing an incident from partial evidence, and deciding when to consult a specialist.

Why do these assessments matter for your role in particular? Your work sits at the point where change meets stability. Every deployment you co-ordinate is a controlled risk; every incident you diagnose is reasoning under pressure; every capacity forecast is applied numeracy; every change request you document is an exercise in precise writing that others must act on safely. Assessments of cognitive ability, numerical reasoning, verbal reasoning, and situational judgement map directly onto those demands. Practising them sharpens exactly the skills your role depends on: spotting the inconsistency in a configuration record before it becomes an outage, interpreting a performance trend before it becomes a capacity crisis, extracting the operative condition from a change policy, and choosing the most effective course of action when a deployment goes wrong at the worst possible moment.

This document is organised into four main assessment sections, each following the same pattern: an overview of what the assessment measures and the format you can expect, a mapping of the assessment's dimensions to the specific skills in your role summary, a substantial set of practice questions with full worked explanations, practical preparation tips, and common pitfalls to avoid.

Here is how to get the most from it. First, read each "About this assessment" section so the format holds no surprises. Second, attempt every practice question honestly — commit to an answer before reading the explanation. Third, treat each explanation as a mini-lesson: even when you answer correctly, the worked reasoning will refine your technique and often connects the question back to a live aspect of your practice, from ITIL-style change control to capacity forecasting. Finally, use the preparation tips and pitfalls for self-reflection: they connect assessment performance back to your development as an engineer trusted with production systems and go-lives.

You already exercise these skills daily under real pressure; the practice here simply makes them visible, deliberate, and stronger. Take your time, and enjoy it. Let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive assessment measures the exact mental processes your role demands, using practical workplace scenarios rather than abstract puzzles. Instead of shapes and number sequences, it presents the everyday materials of application operations — change schedules, configuration baselines, deployment runbooks, monitoring output, dependency maps — and asks you to reason quickly and accurately about them: recognising patterns, deducing consequences from rules, checking artefacts for errors, prioritising competing demands, and solving multi-constraint problems.

The typical format is an online, timed test lasting 15 to 30 minutes, with 20 to 30 questions of graduated difficulty. Scoring is objective against a norm group, and many modern platforms are adaptive, adjusting question difficulty to your performance — so a test that feels progressively harder is often a test going well. Employers usually receive a profile of speed versus accuracy rather than a single number, which means disciplined pace matters: fast enough to finish, careful enough not to leak marks on questions you could do in your sleep.

For a senior application operations engineer, cognitive assessment is particularly relevant because your professional value is structured thinking under operational pressure. Diagnosing an incident is hypothesis elimination against evidence. Assessing a change's impact is tracing a dependency graph to its consequences. Reviewing a configuration record is error checking with an outage as the cost of a miss. Sequencing a go-live is constraint satisfaction with stakeholders attached. A well-designed cognitive assessment simulates precisely these demands in miniature — and because your decisions now carry deployment authority and change co-ordination responsibility, the accuracy the test measures is the accuracy your colleagues rely on.

### How this assessment maps to your role

The assessment's dimensions map directly onto the named skills in your role summary:

- **Pattern recognition** maps to **Problem management** and **Technical specialism**: initiating and monitoring actions to investigate patterns and trends, and using logical schemata to investigate problems and collect performance statistics, both begin with seeing the recurring structure inside noisy operational data.
- **Logical deduction** maps to **Change management** and **Incident management**: analysing and assessing the impact of change means reasoning from dependency rules to consequences; diagnosing incidents means eliminating hypotheses that the evidence contradicts until a cause remains.
- **Error checking** maps to **Asset and configuration management** and **Testing**: maintaining secure configuration and accurate information, verifying the location and state of IT assets, and reviewing requirements and specifications to define test conditions all depend on spotting the record that contradicts reality or the specification that contradicts itself.
- **Prioritisation** maps to **Incident management** and **Availability and capacity management**: diagnosing and prioritising incidents, and managing service components against business needs and KPIs, require rapid, defensible ranking of what matters most right now.
- **Applied problem solving** maps to **Ownership and topic** and **Service focus**: owning an issue until it is resolved, mitigated, or properly handed over means driving multi-step reasoning to a conclusion; taking inputs and establishing coherent frameworks that work is problem solving at the level of process design.

### Practice questions

**Question 1 (easy) — Pattern recognition in a deployment naming convention**

Your team tags releases using the pattern: application code (three letters), hyphen, environment (DEV, TST, or PRD), hyphen, version as major.minor.patch (for example, CMS-PRD-2.4.1). During an audit you review five tags:

1. CMS-PRD-2.4.1
2. CMS-TST-2.4.2
3. CMS-PRD-2.5
4. DOC-DEV-1.0.0
5. DOC-TST-1.0.1

Which tag breaks the convention?

- A) Tag 2
- B) Tag 3
- C) Tag 4
- D) Tag 5

**Correct answer: B**

**Explanation:** Check each element of the pattern in sequence: three-letter application code, environment from the permitted set, and a three-part version number. Tags 1, 2, 4 and 5 conform in every element. Tag 3 has a two-part version — "2.5" instead of major.minor.patch — so it breaks the convention. This is trivial to fix and expensive to miss: automated deployment tooling frequently parses tags, and a malformed version can cause a pipeline to select the wrong artefact or fail silently. As the engineer responsible for code deployment, you are the person whose eye is expected to catch this before the pipeline does — or does not. In the assessment, verify each component of a pattern rather than judging the string's overall shape; your visual system will happily normalise "2.5" into acceptability if you let it.

**Question 2 (easy) — Deduction from a change freeze rule**

Your department's change policy states: "No production changes may be deployed during the change freeze, except emergency changes approved by the duty service manager." It is currently the change freeze, and a production change was deployed this morning. Which conclusion must be true?

- A) The change was an emergency change approved by the duty service manager.
- B) The change policy was breached.
- C) Either the change was an approved emergency change, or the policy was breached.
- D) The duty service manager deployed the change personally.

**Correct answer: C**

**Explanation:** The rule is a prohibition with a single permitted exception. A production deployment during the freeze is therefore either within the exception (an emergency change with the required approval) or a breach — and the facts given do not tell you which. Option A assumes compliance; option B assumes violation; neither is guaranteed. Option D confuses approving a change with executing it — the policy assigns the duty service manager an approval role, nothing more. Only option C, the disjunction, must be true in every scenario consistent with the facts. This discipline has direct operational value: when you discover an unexpected production change, the professional first move is to check the emergency change record before concluding anything — an accusation of breach that turns out to be an approved emergency fix damages trust, while an assumption of approval that turns out to be a cowboy deployment misses a governance failure.

**Question 3 (easy) — Error checking a configuration record**

The configuration management database (CMDB) should record, for each server: hostname, environment, application, operating system version, and last patch date. You are verifying this record against reality:

- Hostname: app-prd-03
- Environment: Production
- Application: Licensing Service
- OS version: 22.04 LTS
- Last patch date: 2026-11-03

Today is 14 August 2026. What is wrong with the record?

- A) The hostname format is invalid.
- B) The last patch date is in the future.
- C) The environment contradicts the hostname.
- D) Nothing is wrong.

**Correct answer: B**

**Explanation:** Sweep every field. The hostname "app-prd-03" is well formed and its "prd" element agrees with the Production environment entry, so A and C fail. The application and OS entries are plausible. The last patch date, however, is 3 November 2026 — nearly three months after today's date of 14 August 2026. A patch cannot have been applied in the future, so the record contains a data error (plausibly a transposition of 2026-03-11, or a fat-fingered month). This matters beyond tidiness: your **Asset and configuration management** skill requires accurate information because patch dates drive security compliance reporting — a future-dated record could mask a server that is actually months overdue for patching. In assessments and audits alike, dates deserve explicit checking against "today", because they are the field where plausible-looking nonsense most often hides.

**Question 4 (moderate) — Impact analysis across a dependency map**

Your dependency documentation states: the Reporting application reads from the Data Warehouse; the Data Warehouse is loaded nightly from the Case System; the Notification service depends on the Case System's API; the Licensing service is fully independent. A change request proposes taking the Case System offline for four hours on Saturday night, spanning the nightly load window. Which services are affected, directly or indirectly?

- A) Case System only
- B) Case System and Notification service only
- C) Case System, Notification service, Data Warehouse load, and next-day Reporting freshness
- D) All services including Licensing

**Correct answer: C**

**Explanation:** Trace the dependency graph outward from the changed component. Direct dependents of the Case System: the Notification service (via the API — down for the outage window) and the nightly Data Warehouse load (which spans the outage and will fail or be incomplete). Then trace one more hop: Reporting reads from the Data Warehouse, so while Reporting itself stays up, its data will be stale the next day — an indirect but real business impact. Licensing is stated to be independent, so option D over-scopes. Options A and B stop tracing too early — the classic impact-analysis failure, because second-order effects (stale reports on Sunday morning) are precisely the ones that surprise stakeholders. This is your **Change management** skill in its purest form: analysing and assessing the impact of change means following every edge of the graph to quiescence, then documenting the full blast radius in the change request so approvers decide with complete information.

**Question 5 (moderate) — Pattern recognition in performance statistics**

You are reviewing weekly average response times (in milliseconds) for the case application over eight weeks: 210, 215, 208, 213, 260, 305, 352, 401. Which reading of this series is most accurate and most useful?

- A) Response times are stable — the average across all eight weeks is acceptable.
- B) The series shows a stable baseline around 210 ms for four weeks, then a sustained upward trend beginning in week 5, worsening by roughly 45-50 ms per week — an emerging degradation worth investigating now.
- C) Week 8 is a one-off outlier and can be ignored.
- D) The application is down.

**Correct answer: B**

**Explanation:** Partition the series before summarising it. Weeks 1-4 oscillate tightly around 210 ms — a healthy, stable baseline. From week 5 the values climb: 260, 305, 352, 401 — four consecutive increases of roughly 45-50 ms each, which is a trend, not noise. Option A commits the averaging fallacy: a single mean across a regime change (about 271 ms) describes neither the healthy period nor the degrading one, and "acceptable on average" is how services drift into breach. Option C mislabels a four-point trend as a one-point outlier. Option D overstates — slow is not down. The professional value of reading B correctly is timing: your **Availability and capacity management** skill means acting while the KPI is threatened rather than after it is breached, and your **Technical specialism** duty to collect performance statistics and forecast resource needs is exactly this — extrapolate the trend (week 9 at roughly 450 ms) and intervene before users feel it.

**Question 6 (moderate) — Prioritisation across competing demands**

It is 09:30. Four items compete for your attention:

1. A severity 2 incident: document uploads failing for one directorate; you are the assigned diagnostician.
2. A change request you must document by 16:00 today for tomorrow's Change Advisory Board (CAB), without which next week's go-live slips a fortnight.
3. A junior colleague asks for help interpreting an unfamiliar error message; they are blocked but their task is routine.
4. Monitoring shows disk usage on a production database server at 78%, trending up about 1% per day; the alert threshold is 90%.

Which sequencing is most defensible?

- A) 1, 3, 2, 4 — resolve the incident, unblock the junior briefly, then document the change, then plan disk remediation
- B) 2, 1, 3, 4 — the go-live has the largest long-term impact
- C) 1, 2, 3, 4 — strict severity order, juniors wait
- D) 4, 1, 2, 3 — capacity risks always come first

**Correct answer: A**

**Explanation:** Rank by impact-weighted urgency and by cost-of-delay. Item 1 leads: a live severity 2 is degrading service for real users now, and you are the assigned owner — your **Incident management** and **Ownership and topic** skills both point here. Item 3 comes next, briefly: unblocking a colleague costs you minutes but recovers their whole morning, and a 10-minute assist barely delays the change documentation — pure cost-of-delay arithmetic, plus the collaborative behaviour senior engineers are expected to model. Item 2 follows with hours of margin against its 16:00 deadline; it is high-stakes but not yet time-critical, and incident diagnosis cannot be batch-scheduled while documentation can. Item 4 is genuinely important and genuinely not urgent: at roughly 1% per day, the 90% threshold is about twelve days away — schedule remediation this week, but it displaces nothing today. Option B lets a tomorrow deadline outrank a now impact; option C wastes a colleague's morning to save minutes; option D confuses a forecastable risk with an active one. The pattern assessors reward: sequence by impact and urgency jointly, and price in how cheaply each item can be deferred or delegated.

**Question 7 (moderate) — Deduction in incident diagnosis**

Users in Office A report that the case application is completely unavailable; users in Office B report it working normally. Monitoring shows the application servers healthy, response times normal, and error rates flat. Office A can reach other applications hosted in the same data centre without difficulty. Which hypothesis best fits all the evidence?

- A) The application servers have crashed.
- B) The data centre's internet connection is down.
- C) A network path or configuration issue specific to Office A's route to this application — such as a proxy rule, firewall change, or DNS issue affecting that office.
- D) The application's database is corrupted.

**Correct answer: C**

**Explanation:** Diagnose by elimination against every fact. Server crash (A): contradicted twice — monitoring shows healthy servers, and Office B is using the application right now. Data centre connectivity (B): contradicted — Office A reaches other applications in the same data centre. Database corruption (D): contradicted — corruption would affect both offices and would surface in error rates, which are flat. Hypothesis C is the only one consistent with the full evidence set: the fault lies on the specific path between Office A and this application — a scoped network, proxy, firewall, or name-resolution issue. Note the diagnostic power of the question "who is NOT affected?": Office B's normality eliminated more hypotheses than Office A's outage suggested. This is your **Incident management** skill as the assessment sees it — diagnosis is not pattern-matching to the most familiar cause; it is retaining only the hypotheses that survive every observed fact, then testing the survivor (for example, by comparing a traceroute from each office).

**Question 8 (moderate) — Error checking a test specification**

A test plan for a change to the payments application states: (i) "All test conditions must be traceable to a documented requirement." (ii) "Regression tests will cover requirements R1 to R6." (iii) "Test condition TC-9 verifies the new bulk-payment limit described in requirement R7." (iv) "Requirement R7 was descoped from this release at the March board." Assuming statements (i), (ii), and (iv) are correct, what is wrong with the plan?

- A) TC-9 is traceable to R7, so the plan is internally consistent.
- B) TC-9 tests a requirement that is no longer in the release, so either TC-9 should be removed or the plan must explain why a descoped requirement is being tested.
- C) The regression tests should cover R7 as well.
- D) Requirement R7 should be reinstated because a test exists for it.

**Correct answer: B**

**Explanation:** Reconcile the statements. TC-9 traces to R7, which satisfies rule (i) mechanically — but statement (iv) says R7 was descoped in March. A test condition verifying functionality that is not in the release is at best wasted effort and at worst dangerous: if TC-9 "passes", it implies the bulk-payment limit behaviour exists in a release that should not contain it, which would itself be a defect. Option A mistakes formal traceability for validity. Option C would extend regression coverage to descoped functionality, compounding the error. Option D inverts authority — test artefacts follow scope decisions, not the other way round; a board descope is not undone because a test document lagged behind it. The correct finding is B: flag the stale condition, remove or annotate it, and check whether other artefacts also predate the March descope. This is your **Testing** skill — reviewing requirements and specifications, defining test conditions, and identifying issues and risks — applied as document-set consistency checking, which is precisely how release-day surprises are prevented.

**Question 9 (hard) — Sequencing a go-live under constraints**

A go-live requires five activities: database migration (M, 2 hours), application deployment (D, 1 hour), smoke testing (S, 1 hour), DNS cutover (C, 30 minutes), and stakeholder notification of completion (N, immediate). Constraints: (i) D cannot start until M completes; (ii) S cannot start until D completes; (iii) C may only happen if S passes; (iv) the outage window is 22:00 to 03:00; (v) if at any point the remaining required activities cannot fit in the window, you must invoke rollback, which takes 90 minutes and must complete inside the window. M starts on time at 22:00 but completes at 00:15 instead of 00:00. What is the correct decision at 00:15?

- A) Continue: D, S and C need 2.5 hours, finishing at 02:45, inside the window — and rollback remains possible until 01:30 if needed.
- B) Invoke rollback immediately — the migration overran, so the plan has failed.
- C) Continue, but skip smoke testing to recover the lost 15 minutes.
- D) Extend the outage window unilaterally by 30 minutes to restore contingency.

**Correct answer: A**

**Explanation:** Do the arithmetic before the adrenaline. At 00:15, remaining required work is D (1 h) + S (1 h) + C (0.5 h) = 2.5 hours, completing at 02:45 — 15 minutes inside the 03:00 boundary, so constraint (v) does not trigger and continuing is legitimate. It is also worth computing the rollback horizon: rollback takes 90 minutes and must finish by 03:00, so the last safe moment to invoke it is 01:30 — which means the true decision point is the end of D (01:15): if deployment has gone badly, you can still roll back with margin; if smoke testing later fails at 02:15, rollback no longer fits, so option A's framing correctly identifies where the remaining risk sits. Option B abandons a still-viable plan — a 15-minute overrun is not a failure condition when the arithmetic still closes. Option C is the classic go-live sin: constraint (iii) makes smoke testing the gate that protects users from a bad cutover, and trading verification for schedule inverts the purpose of the window. Option D exceeds your authority and breaks faith with every stakeholder who agreed the window. Senior engineers co-ordinating go-lives are paid exactly for this: recompute feasibility at each milestone, know your last-safe-rollback time in advance, and change course on arithmetic, not emotion.

**Question 10 (hard) — Deducing a root cause from correlated events**

Over three weeks, the licensing application has crashed six times. You assemble the facts: crashes occur only on weekdays; all six occurred between 08:50 and 09:20; memory usage climbs steadily from 07:00 each weekday and the crashes coincide with its peak; a data import job runs at 07:00 on weekdays; weekend memory usage stays flat; the import job was upgraded to handle larger files three weeks ago. Which explanation best fits all the evidence?

- A) Users logging in at 09:00 overload the application.
- B) Since its upgrade three weeks ago, the weekday 07:00 import job consumes progressively more memory, and the application crashes when the morning login load arrives on top of the already-elevated memory — the upgrade is the likely root of the change in behaviour.
- C) The crashes are random and coincidentally cluster in the morning.
- D) Weekend batch processing corrupts the application state.

**Correct answer: B**

**Explanation:** Test each hypothesis against every fact, especially the discriminating ones. Pure login load (A) explains the 08:50-09:20 timing but not why the problem began three weeks ago — logins existed before — nor why memory climbs from 07:00, before users arrive. Randomness (C) is refuted by the tight temporal clustering and the clean weekday/weekend split. Weekend processing (D) is contradicted directly: weekend memory stays flat and crashes never occur then. Hypothesis B alone accounts for the full set: the upgraded import job (the change that matches the three-week onset) elevates memory from 07:00 on exactly the days crashes occur, and the morning login wave supplies the final increment that exceeds the limit — a two-factor cause, which is why neither "the import" nor "the logins" alone survived scrutiny before. Note the investigative principles the question rehearses: behavioural changes usually trace to system changes (ask "what changed three weeks ago?"), and absence of symptoms (quiet weekends) eliminates hypotheses as powerfully as their presence. This is your **Problem management** skill — investigating patterns and trends to resolve problems and determine preventative measures, which here might mean re-profiling the upgraded job's memory or rescheduling it away from the login peak.

**Question 11 (hard) — Multi-constraint change scheduling**

Three changes need scheduling next week: CH-1 (patch the database server, 2-hour outage of the case application), CH-2 (deploy new reporting features, requires the database patch to be in place first, 1-hour outage of reporting), CH-3 (network firmware upgrade, 1-hour outage of everything in the data centre). Constraints: (i) only one change per night; (ii) changes run in the 23:00-04:00 window; (iii) CH-3's network engineer is available only Tuesday and Thursday; (iv) the case application must not be disturbed on Wednesday night because month-end casework runs then; (v) CH-2 must complete before Friday, when the reporting features are announced. Which schedule satisfies all constraints?

- A) CH-1 Monday, CH-2 Wednesday, CH-3 Thursday
- B) CH-1 Tuesday, CH-2 Wednesday, CH-3 Thursday
- C) CH-3 Tuesday, CH-1 Wednesday, CH-2 Thursday
- D) CH-1 Monday, CH-3 Tuesday, CH-2 Thursday

**Correct answer: D**

**Explanation:** Encode the constraints, then test each option against all of them. The rules: CH-1 must precede CH-2 (CH-2 requires the database patch); CH-3 must fall on Tuesday or Thursday (iii); Wednesday night must not disturb the case application (iv), which certainly excludes CH-1 (a case-application outage) and CH-3 (an everything outage) from Wednesday, and prudently excludes CH-2 as well, since CH-2 deploys against and exercises the same database that month-end casework depends on; and CH-2 must complete before Friday (v). Now test. Option C fails immediately: it schedules CH-1 on Wednesday, putting a two-hour case-application outage in the middle of month-end casework — a direct breach of (iv). Options A and B both place CH-2 on Wednesday night: the reporting outage itself does not touch the case application, but deploying database-dependent features during the one night the business has asked you to protect creates exactly the interpretive risk a change advisory board exists to reject — if anything goes wrong with the shared database during month-end, "the constraint only said the case application" will not be a comfortable defence. Option D alone keeps Wednesday entirely change-free: CH-1 on Monday satisfies the dependency early; CH-3 on Tuesday matches the network engineer's availability; CH-2 on Thursday runs after CH-1 and completes before Friday's announcement. Every constraint is satisfied with margin and without interpretation. The professional lesson mirrors real CAB practice: when one schedule merely *probably* respects a business-protection constraint and another *certainly* does, the certain one is the defensible submission — you document the reasoning in the change request and let approvers see that the protected window was treated as genuinely protected.

**Question 12 (hard) — Establishing a coherent framework from messy inputs**

You inherit an application whose operational practices are inconsistent: some changes are logged in the ticketing system, some in a spreadsheet, some only in emails; three of nine servers are missing from the CMDB; monitoring alerts go to a mailbox nobody owns; and two undocumented "temporary" configuration workarounds have been live for over a year. You have limited time and cannot fix everything at once. Which first move creates the most coherent foundation for everything else?

- A) Delete the spreadsheet and emails, and declare the ticketing system the single source of truth from today.
- B) Establish an accurate baseline first: audit and register all nine servers and the two workarounds in the CMDB, then route all change recording through the ticketing system, then assign ownership of the alert mailbox — because every other control depends on knowing what actually exists.
- C) Fix the two workarounds first, since they are the oldest problems.
- D) Set up a new monitoring dashboard to get visibility of live issues.

**Correct answer: B**

**Explanation:** This is your **Service focus** skill — taking inputs and establishing coherent frameworks that work — posed as a sequencing problem, and the key is dependency ordering among the controls themselves. Change control (option A's instinct) cannot work while the CMDB is missing a third of the estate and two live workarounds are invisible: you cannot assess the impact of a change to assets you do not know exist, so declaring a single source of truth *before* making it true merely centralises the fiction. Remediating the workarounds first (C) is action without assessment — undocumented year-old workarounds may be load-bearing, and touching them before registering and understanding them is how "temporary fix removed" becomes a severity 1. New dashboards (D) add observation without ownership — alerts already flow to an unowned mailbox; more signal into a void is not visibility. Option B sequences correctly: first make the configuration record match reality (**Asset and configuration management** — verify the location and state of IT assets), because an accurate baseline is the precondition for meaningful change control, impact assessment, and monitoring; then channel changes through one system; then give alerts an owner. Frameworks cohere when each control can rely on the one beneath it — and the bottom layer is always "an accurate picture of what exists".

### Preparation tips

- **Practise on live artefacts.** Spend ten minutes a day reading a change request, a CMDB extract, or a test plan with an auditor's eye: is every field consistent with every other field, and with reality? This is exactly the error-checking the assessment samples.
- **Rehearse dependency tracing.** Take any component you support and sketch its dependency graph from memory, then verify. Impact-analysis questions are graph traversal; fluency comes from repetition.
- **Do the arithmetic before the adrenaline.** For go-live and rollback questions — and real windows — practise computing "latest safe decision time" in advance. Assessors reward recomputation at milestones, not gut calls.
- **Use elimination on diagnosis questions.** List the facts, strike every hypothesis a fact contradicts, and attend closely to what is *not* affected — absence of symptoms is high-value evidence.
- **Time-box ruthlessly.** Bank the easy questions quickly and accurately; allocate the recovered time to the multi-constraint problems at the end.
- **Simulate mild pressure.** Do practice sets against a timer after a full workday, not just fresh on a Sunday morning. Assessments — like incidents — rarely arrive when you are at your best.

### Common pitfalls to avoid

- **Stopping impact analysis at first-order effects.** The dependency graph's second hop (stale data, delayed downstream jobs) is where unassessed impact hides. Trace to quiescence.
- **Averaging across a regime change.** A single mean over "four stable weeks plus four degrading weeks" describes nothing. Partition first, then summarise.
- **Letting formal consistency mask real inconsistency.** A test condition can trace perfectly to a requirement that was descoped months ago. Check artefacts against decisions, not just against each other.
- **Treating overruns as failures.** A slipped milestone triggers recomputation, not reflexive rollback — and equally, never let sunk progress carry you past your last safe rollback time.
- **Skipping verification to recover schedule.** Smoke tests and health checks are gates, not padding. Any option that trades verification for time is a trap, in tests and in production.
- **Trusting plausible-looking data.** Future-dated patches, two-part version numbers, subtly inverted hierarchies — assessments (and audits) hide errors inside well-formatted records. Verify content, not formatting.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment measures how accurately and confidently you work with the quantitative material your role genuinely produces: availability percentages, capacity utilisation figures, incident and change volumes, deployment success rates, performance statistics, and resource forecasts. You will read tables and charts, calculate percentages, ratios, weighted averages, and rates of change, and — the distinctly senior element — interpret what the numbers imply for decisions: when will this disk fill, is this KPI trending toward breach, did that remedy actually work?

The typical format is an online, timed test of 20 to 30 minutes with 15 to 20 questions, each presenting data and four options. Calculators are permitted; methodical rough work is expected. Platforms often adapt difficulty to performance, and scoring profiles both speed and accuracy against a norm group. The arithmetic itself is deliberately unexotic — the challenge is applying it precisely to operational data under time pressure, choosing the right numerator, the right denominator, and the right interpretation.

Why do employers use numeric assessments for this role? Because at senior level your numbers become commitments. When you forecast resource needs, procurement acts on the forecast. When you report availability against a KPI, service review meetings act on the figure. When you assess a change's capacity impact, the CAB approves on your arithmetic. Your role summary is explicit: you optimise performance and forecast resource needs, collect performance statistics and create reports, and manage service components against business needs and KPIs. Every one of those duties has a calculation at its core, and a senior engineer whose calculations are trusted saves the organisation from both outages (under-provisioning) and waste (over-provisioning).

The questions below use the data you actually handle — availability reports, capacity trends, incident statistics, deployment metrics, test results — and every explanation shows the arithmetic step by step, because in your role the working matters as much as the answer: it is what you will be asked to show when a stakeholder challenges the figure.

### How this assessment maps to your role

- **Percentages, availability and KPI arithmetic** map to **Availability and capacity management**: managing service components to meet business needs and KPIs means converting between availability percentages and downtime minutes, comparing performance against targets, and knowing exactly what "99.9%" commits you to.
- **Trends, rates and forecasting** map to **Technical specialism**: optimising performance and forecasting resource needs is extrapolation done honestly — identifying growth rates from performance statistics and projecting when thresholds will be crossed.
- **Before-and-after comparison** maps to **Problem management**: determining whether a resolution or preventative measure worked is a numerical question — did the error rate genuinely fall, and by how much relative to baseline?
- **Volume, ratio and workload analysis** maps to **Incident management** and **Change management**: prioritising incidents and assessing change impact both draw on volumes, proportions, and failure rates — including deployment success statistics from the releases you co-ordinate.
- **Test result analysis** maps to **Testing**: analysing and reporting test activities and results means pass rates, defect densities, and coverage percentages, reported without distortion.
- **User data interpretation** maps to **User focus**: using quantitative and qualitative data about users to turn user focus into outcomes starts with reading usage and satisfaction figures correctly.

### Practice questions

**Question 1 (easy) — Availability percentage**

The case application was unavailable for a total of 6 hours during a 30-day month. Assuming a 24-hour service, what was its availability for the month, to one decimal place?

- A) 99.2%
- B) 99.7%
- C) 98.8%
- D) 97.5%

**Correct answer: A**

**Explanation:** Step 1: total hours in the month = 30 × 24 = 720. Step 2: available hours = 720 − 6 = 714. Step 3: availability = 714 ÷ 720 = 0.99166…, which is 99.166…% — rounding to one decimal place gives 99.2%. A useful cross-check: 1% of 720 hours is 7.2 hours, so 6 hours of downtime must cost slightly less than one percentage point, landing just above 99% — consistent with 99.2%. This conversion fluency is foundational to your **Availability and capacity management** work: KPIs are set in percentages, but outages happen in hours, and you are the person who translates between them accurately in both directions.

**Question 2 (easy) — Change success rate**

Last quarter your team implemented 80 changes: 68 succeeded, 7 succeeded with minor issues, and 5 failed and were rolled back. What percentage of changes failed?

- A) 5%
- B) 6.25%
- C) 8.75%
- D) 15%

**Correct answer: B**

**Explanation:** Step 1: identify the part (5 failed changes) and the whole (80 total changes). Step 2: 5 ÷ 80 = 0.0625. Step 3: × 100 = 6.25%. Option A mistakes the raw count for a percentage. Option C is the "succeeded with minor issues" proportion (7 ÷ 80), and option D is those two categories combined (12 ÷ 80 = 15%) — worth noticing, because how your organisation classifies "succeeded with issues" changes the headline: a report claiming 85% clean success and one claiming 93.75% non-failure are both defensible from this data, and a senior engineer documenting change outcomes should state the definition alongside the figure. Precision about categories is as much a part of **Change management** reporting as the division itself.

**Question 3 (easy) — Reading a capacity table**

A storage report for your three production database servers shows:

| Server | Capacity (GB) | Used (GB) |
|---|---|---|
| db-prd-01 | 500 | 425 |
| db-prd-02 | 800 | 560 |
| db-prd-03 | 400 | 350 |

Which server has the highest percentage utilisation?

- A) db-prd-01
- B) db-prd-02
- C) db-prd-03
- D) They are equal

**Correct answer: C**

**Explanation:** Calculate each utilisation separately — the largest absolute usage is not necessarily the highest proportion. db-prd-01: 425 ÷ 500 = 0.85 = 85%. db-prd-02: 560 ÷ 800 = 0.70 = 70%. db-prd-03: 350 ÷ 400 = 0.875 = 87.5%. The highest is db-prd-03 at 87.5%, despite holding the least data in absolute terms. The trap is db-prd-02, whose 560 GB is the biggest raw number. In capacity management, percentage utilisation (with growth rate) determines urgency, not absolute usage — db-prd-03 is the server closest to its ceiling and the one your **Technical specialism** duty to forecast resource needs should flag first. Always compute the ratio; never rank by the raw column.

**Question 4 (moderate) — Downtime budget for a KPI**

Your service's availability KPI is 99.9% measured over a 365-day year, 24 hours a day. To the nearest quarter of an hour, how much total downtime per year does the KPI permit?

- A) About 4 hours 30 minutes
- B) About 8 hours 45 minutes
- C) About 17 hours 30 minutes
- D) About 43 hours 45 minutes

**Correct answer: B**

**Explanation:** Step 1: total hours per year = 365 × 24 = 8,760. Step 2: the KPI permits 100% − 99.9% = 0.1% downtime. Step 3: 0.1% of 8,760 = 8,760 × 0.001 = 8.76 hours. Step 4: convert the decimal: 0.76 × 60 ≈ 45.6 minutes, so approximately 8 hours 45 minutes. Option D is the 99.5% budget (0.5% = 43.8 hours) and option A is roughly the 99.95% budget — the wrong-decimal traps. This number should live in your head: a single mishandled four-hour outage consumes nearly half the annual budget of a 99.9% service, which is why your incident diagnosis speed and your change scheduling both connect directly to this KPI. When a stakeholder proposes "just a quick five-hour maintenance outage", the ability to reply "that is 57% of our annual downtime budget" changes the conversation.

**Question 5 (moderate) — Percentage change in incident volume after a fix**

A recurring defect generated 45 incidents in June. You implemented a preventative measure in early July, and July saw 27 incidents of the same type. By what percentage did the monthly incident count fall?

- A) 18%
- B) 27%
- C) 40%
- D) 60%

**Correct answer: C**

**Explanation:** Step 1: the fall = 45 − 27 = 18 incidents. Step 2: divide by the original (June) figure: 18 ÷ 45 = 0.4. Step 3: × 100 = 40%. Option A presents the raw difference as a percentage; option D is 27 ÷ 45 = 60%, which is the proportion remaining, not the fall — a subtle and common confusion: "fell by 40%" and "fell to 60%" describe the same data. This calculation is the heart of your **Problem management** duty to determine preventative measures and verify them: a 40% reduction is evidence of partial effectiveness, and the honest report says exactly that — the measure helped, but 27 incidents a month means the root cause is not fully addressed and investigation should continue. Numbers verify remedies; verified remedies close problems.

**Question 6 (moderate) — Weighted average resolution time**

Last month you resolved 30 severity 3 incidents averaging 3 hours each, 12 severity 2 incidents averaging 7 hours each, and 3 severity 1 incidents averaging 11 hours each. What was the overall average resolution time across all 45 incidents, to one decimal place?

- A) 7.0 hours
- B) 4.6 hours
- C) 4.1 hours
- D) 5.2 hours

**Correct answer: B**

**Explanation:** A simple average of 3, 7 and 11 gives 7.0 (option A) — wrong, because the groups differ greatly in size. Weight by volume. Step 1: severity 3 total = 30 × 3 = 90 hours. Step 2: severity 2 total = 12 × 7 = 84 hours. Step 3: severity 1 total = 3 × 11 = 33 hours. Step 4: grand total = 90 + 84 + 33 = 207 hours. Step 5: divide by 45 incidents: 207 ÷ 45 = 4.6 hours. Sense-check: two-thirds of incidents are the 3-hour kind, so the answer must sit much nearer 3 than 11 — 4.6 passes; 7.0 fails on inspection alone. Weighted thinking pervades senior reporting: whenever categories of different sizes are combined — resolution times, response times, test durations — combine the totals first. A report built on unweighted averages overstates the experience of the rare cases and misleads the service review.

**Question 7 (moderate) — Forecasting disk exhaustion**

A production database currently uses 620 GB of its 800 GB allocation. Usage has grown consistently by 30 GB per month. Procurement of additional storage takes two months from request to availability, and your team's standard practice is to keep at least one month of growth in reserve as a safety margin. If growth continues at the current rate, how many months from now will the disk reach capacity, and what should you do?

- A) 12 months — no action needed this year.
- B) 6 months — note it in the capacity plan and review again next quarter.
- C) 3 months — raise the request immediately.
- D) 6 months — raise the request within the next month or two, because the two-month lead time plus the one-month safety margin consumes half the runway.

**Correct answer: D**

**Explanation:** Step 1: remaining headroom = 800 − 620 = 180 GB. Step 2: months to exhaustion = 180 ÷ 30 = 6 months. Step 3: now work backwards from exhaustion to the decision date — this is the step that separates a calculation from a forecast. The new storage must be *available* one month of growth before exhaustion (the safety margin), i.e. by month 5. Procurement takes two months, so the request must be raised by month 3. Waiting until "next quarter's review" (option B) burns half of that decision window and leaves no slack if growth accelerates or procurement slips. Option A's 12 months would require 15 GB/month growth — half the observed rate; option C's 3 months confuses the request-by date with the exhaustion date. The professional output, as option D states, is both the forecast (6 months) and the timed recommendation (request within a month or two). This is your **Technical specialism** duty to forecast resource needs done properly: runway minus lead time minus safety margin equals your true decision window, and a senior engineer reports the decision window, not just the runway.

**Question 8 (moderate) — Test pass rates across cycles**

A regression suite of 240 tests was run in two cycles before a release. Cycle 1: 216 passed. Cycle 2 (after fixes): 234 passed. What were the pass rates for each cycle, and what was the percentage-point improvement?

- A) 90% then 97.5%; improvement 7.5 percentage points
- B) 90% then 97.5%; improvement 8.3 percentage points
- C) 92.5% then 99%; improvement 6.5 percentage points
- D) 90% then 95%; improvement 5 percentage points

**Correct answer: A**

**Explanation:** Cycle 1: 216 ÷ 240 = 0.90 = 90%. Cycle 2: 234 ÷ 240 = 0.975 = 97.5%. Improvement in percentage points = 97.5 − 90 = 7.5. Option B's "8.3" is the relative improvement (7.5 ÷ 90 = 8.33%) mislabelled as points — the distinction between percentage points (subtraction) and relative percentage change (division by the base) is a favourite assessment discriminator and a genuine reporting hazard. When you analyse and report test activities and results (**Testing**), say which you mean: "pass rate rose 7.5 points to 97.5%" is unambiguous. Note also what the numbers say operationally: 6 tests still fail (240 − 234), and a release decision needs to know *which* six — pass rates summarise, but go-live gates are about the content of the failures, not the percentage alone.

**Question 9 (hard) — Deployment window arithmetic**

A deployment consists of: pre-checks (15 minutes), database migration (75 minutes), application deployment (40 minutes), smoke tests (30 minutes), and DNS cutover (10 minutes), executed sequentially. Rollback, if needed, takes 50 minutes from the moment it is invoked. The change window is 23:00 to 03:00. What is the latest clock time at which rollback can be invoked and still complete within the window, and does the plan leave any slack if everything runs to time?

- A) Latest rollback 02:10; the plan has 70 minutes of slack.
- B) Latest rollback 02:10; the plan has 30 minutes of slack.
- C) Latest rollback 01:50; the plan has 30 minutes of slack.
- D) Latest rollback 02:30; the plan has no slack.

**Correct answer: B**

**Explanation:** Two separate calculations. Rollback horizon: rollback takes 50 minutes and must finish by 03:00, so the latest invocation is 03:00 − 50 minutes = 02:10. Plan duration: 15 + 75 + 40 + 30 + 10 = 170 minutes; the window is 4 hours = 240 minutes; slack = 240 − 170 = 70 minutes — so if everything runs to time, work finishes at 23:00 + 170 minutes = 01:50. Now reconcile with the options: A claims 70 minutes of slack, B claims 30. The plan's *schedule* slack is 70 minutes — but consider what slack is *for*: the ability to absorb overrun and still choose rollback. If the deployment consumes its full 70 minutes of slack, the critical smoke-test verdict arrives after 02:10 and rollback is no longer available. The *protected* slack — overrun you can absorb while keeping the rollback option alive through the end of smoke tests — is bounded by the 02:10 horizon: smoke tests nominally end at 01:40 (before cutover), leaving 02:10 − 01:40 = 30 minutes of slack that preserves the abort option. Option B captures both figures correctly: rollback by 02:10, and 30 minutes of genuinely usable contingency. This layered arithmetic — schedule slack versus decision-preserving slack — is exactly the calculation a senior engineer runs when co-ordinating a go-live, and the difference between the two numbers is the difference between "we finished inside the window" and "we kept our options open the whole way".

**Question 10 (hard) — Capacity headroom under growth and a step change**

An application server pool handles a peak of 1,200 requests per minute and has a tested capacity of 2,000 requests per minute. Organic traffic grows 5% per quarter (compounding). Next quarter, a departmental consolidation will also migrate a workload adding a one-off 300 requests per minute to the peak. If both occur, what will peak demand be at the end of next quarter, and how much headroom remains?

- A) 1,560 rpm; 440 rpm headroom (22% of capacity)
- B) 1,500 rpm; 500 rpm headroom (25% of capacity)
- C) 1,575 rpm; 425 rpm headroom
- D) 1,860 rpm; 140 rpm headroom (7% of capacity)

**Correct answer: A**

**Explanation:** Step 1: apply one quarter of organic growth to the current peak: 1,200 × 1.05 = 1,260 rpm. Step 2: add the migration's step change: 1,260 + 300 = 1,560 rpm. Step 3: headroom = 2,000 − 1,560 = 440 rpm. Step 4: as a proportion of capacity: 440 ÷ 2,000 = 22%. Option B forgets the organic growth (1,200 + 300); option C applies 5% *after* adding the step (1,500 × 1.05 = 1,575) — order matters, and the migration lands at quarter end after organic growth has accrued; option D erroneously compounds several quarters. The senior-level insight is the trajectory, not the snapshot: 22% headroom sounds tolerable, but with 5% compounding growth on a 1,560 base (~78 rpm next quarter, then more), the pool crosses a typical 80% utilisation planning threshold (1,600 rpm) almost immediately and exhausts within roughly five to six quarters — so the correct operational output of this arithmetic is a capacity plan and a procurement recommendation now, which is precisely what **Availability and capacity management** and forecasting resource needs mean in practice.

**Question 11 (hard) — Comparing incident profiles across two applications**

Two applications you support produced this quarter's figures: App X — 120 incidents, of which 18 were severity 1 or 2; App Y — 45 incidents, of which 9 were severity 1 or 2. A colleague says: "App X is the bigger problem — it produced nearly three times the incidents and twice the serious ones." What do the proportions show?

- A) The colleague is right: App X is worse on both measures.
- B) App X produces more incidents in total, but App Y has the higher *rate* of serious incidents: 20% of its incidents are severity 1-2 versus 15% for App X.
- C) The applications have identical serious-incident rates.
- D) App Y is worse on both measures.

**Correct answer: B**

**Explanation:** Compute the proportions the colleague skipped. App X: 18 ÷ 120 = 0.15 = 15% serious. App Y: 9 ÷ 45 = 0.20 = 20% serious. So the colleague's absolute claims are true (120 > 45; 18 > 9) but the *profile* claim is not: when an App Y incident occurs, it is more likely to be serious. Both views matter and they drive different actions: App X's volume argues for problem-management attention to its high-frequency defects (volume consumes team capacity); App Y's severity skew argues for investigating why its failures tend to be grave — perhaps missing resilience, so that when it fails, it fails hard. Option B is the only statement the arithmetic supports. This is your **Problem management** skill quantified: initiating investigations into patterns and trends starts with computing rates, not just counts, because counts follow size and usage while rates reveal character. In reports, publish both and let neither masquerade as the other.

**Question 12 (hard) — User research data and an outcome decision**

To assess a new self-service password reset feature, you gather data: in the four weeks before launch, the service desk averaged 190 password-reset tickets per week. In the four weeks after launch, the weekly numbers were 150, 130, 115, 105. A survey of 400 users who tried the feature found 340 rated it "easy" or "very easy". What weekly reduction (final week versus baseline) and satisfaction rate do the data show, and what is the soundest conclusion?

- A) 45% reduction; 85% satisfaction; the feature is succeeding and the trend suggests further improvement as adoption grows.
- B) 26% reduction; 85% satisfaction; the feature has plateaued.
- C) 45% reduction; 340% satisfaction; success.
- D) 45% reduction; 85% satisfaction; the feature has failed because 105 tickets still arrive weekly.

**Correct answer: A**

**Explanation:** Reduction: final week 105 versus baseline 190; fall = 190 − 105 = 85; 85 ÷ 190 = 0.447 ≈ 45%. Satisfaction: 340 ÷ 400 = 0.85 = 85%. Option B's 26% uses the *average* of the four post-launch weeks (125) — a defensible statistic, but the question asks final week versus baseline, and the week-on-week series (150 → 130 → 115 → 105) shows continuing decline, contradicting "plateaued". Option C's "340%" divides by nothing sensible — always sanity-check that a percentage of people cannot exceed 100. Option D demands perfection: some resets will always need human help (locked accounts, accessibility needs), and 105 weekly tickets against a falling trend is not failure. The soundest conclusion is A — and the reasoning pattern is your **User focus** skill exactly as your role summary states it: using quantitative data (ticket volumes, satisfaction rates) about users to turn user focus into outcomes. A senior engineer's report here would state both figures, note the still-declining trend, and recommend re-measuring after adoption stabilises — evidence-based, neither triumphalist nor defeatist.

### Preparation tips

- **Memorise your service's key conversions.** Know the downtime budgets for 99%, 99.5% and 99.9% at monthly and annual scales. Instant conversion frees working memory for the genuinely hard parts of a question.
- **Always name the base before dividing.** Percentage change divides by the original; utilisation divides by capacity; pass rate divides by tests run. Most numeric errors are base errors, in tests and in reports alike.
- **Weight everything combined.** Whenever categories of different sizes merge — incidents, tests, response times — total first, divide once. Practise until the unweighted average looks obviously wrong.
- **Separate points from percent.** Rehearse the sentence pattern: "up 7.5 points to 97.5%, a relative rise of 8.3%". If you can say it fluently, you will not confuse it under time pressure.
- **Forecast with both the line and the story.** For trend questions, compute the linear projection, then ask what could bend the line (migrations, retention changes, seasonality). Assessments increasingly reward the interpretive step, and your stakeholders always do.
- **Recompute before you rationalise.** When your answer is not among the options, redo the arithmetic before doubting the method. Transposition and decimal slips outnumber conceptual errors.

### Common pitfalls to avoid

- **Ranking by raw numbers when rates are asked.** The biggest server, busiest application, or largest count is not necessarily the closest to its limit or the worst per-incident. Compute the ratio.
- **Averaging away a regime change.** Post-fix weeks, post-launch weeks, and degradation periods must not be blended with baseline weeks into one mean. Partition, then compare.
- **Confusing "fell by 40%" with "fell to 40%".** The remaining proportion and the reduction are complements; misreading one as the other reverses your conclusion about whether a remedy worked.
- **Forgetting lead times in forecasts.** Runway to exhaustion minus procurement lead time is your true decision window. Twelve months of headroom with a two-month lead time is ten months of thinking time, not twelve.
- **Reporting percentages without definitions.** "Success rate" depends on how partial successes are classified. State the definition with the figure, or the figure will be challenged — rightly.
- **Spending five minutes to rescue one mark.** Flag the stubborn question, bank the rest, return if time allows. Assessments reward portfolio management of your minutes, just as operations rewards triage.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment measures how precisely you extract meaning, conditions, and implications from the written material your role runs on: change policies, service management standards, supplier notices, incident reports, test summaries, and stakeholder communications. The dominant format presents a short passage followed by statements to classify as **True** (the passage supports it), **False** (the passage contradicts it), or **Cannot say** (the passage provides insufficient information). Supporting formats include best-summary questions, inference questions, and clear-writing judgement — choosing the wording that communicates most accurately.

The typical format is an online, timed test of 15 to 25 minutes covering 20 to 30 statements across several passages. The governing rule: answer from the passage alone, not from your professional knowledge. This is harder for experienced practitioners than for novices — you know how change management usually works, and the test deliberately includes passages that deviate from common practice to check whether you read what is written or what you expect. Treat that as the point, not a trick: in real operations, the supplier's actual notice, the department's actual policy, and this CAB's actual conditions are what bind you, however they compare with convention.

Why do employers use verbal reasoning assessments for this role? Because at senior level, misreading is an operational hazard with a blast radius. You are responsible for code deployment and for co-ordinating change activities: the difference between "changes must be approved before scheduling" and "changes must be scheduled before approval" is a governance breach; the difference between "the patch may be applied to clustered nodes sequentially" and "must be applied simultaneously" is an outage. You also write documents others act on — change requests, incident updates, handovers — so the assessment's clear-writing dimension measures the other half of the same skill: producing text that cannot be reasonably misread.

The passages below are drawn from your genuine document diet: a change management policy extract, a supplier security notice, and an incident report with stakeholder communications. Read them the way you would read a licence condition — because operationally, that is what they are.

### How this assessment maps to your role

- **Precise reading of conditions** maps to **Change management**: documenting change requests and actioning changes from change requests requires exact comprehension of approval conditions, freeze exceptions, and rollback triggers — the "unless", "only if", and "except" clauses where policies actually live.
- **Inference discipline** maps to **Incident management** and **Problem management**: diagnosing causes and investigating trends both demand the distinction between what the evidence states, what it implies, and what it merely fails to rule out — the true/false/cannot-say discipline is that distinction, formalised.
- **Standards comprehension** maps to **Service management framework knowledge**: a Level 3 service management qualification is substantially an exercise in reading framework definitions precisely — the difference between an incident and a problem, a change and a release, is definitional reading.
- **Reading user and stakeholder language** maps to **User focus**: collating user needs evidence and defining research that fits user needs begins with accurately understanding what users and stakeholders have actually said — including what their words do and do not support.
- **Clear-writing judgement** maps to **Ownership and topic** and **Testing**: owning an issue through to handover, and analysing and reporting test activities and results, both culminate in written artefacts whose value is exactly their clarity.

### Practice questions

**Passage 1 — Change management policy extract**

*"Standard changes are pre-approved, low-risk changes with an established procedure; they may be implemented without Change Advisory Board (CAB) review but must still be recorded before implementation. Normal changes require CAB approval before scheduling. Emergency changes may be implemented before approval is obtained, but only where delay would cause significant service impact, and retrospective approval must be sought at the next CAB meeting. Any change that fails must be reported to the CAB regardless of its category. The CAB meets every Wednesday. A change implemented under the emergency provision that is subsequently refused retrospective approval must be reversed within five working days of the refusal, unless reversal would itself cause greater service impact, in which case the service owner decides the way forward."*

**Question 1 (easy) — True, false, or cannot say**

Statement: "Standard changes do not need to be recorded."

- A) True
- B) False
- C) Cannot say
- D) True, provided the change succeeds

**Correct answer: B**

**Explanation:** The passage states that standard changes "may be implemented without Change Advisory Board (CAB) review but must still be recorded before implementation." The statement directly contradicts the recording requirement, so it is False. The design of this question mirrors a real comprehension hazard: "pre-approved" and "without CAB review" create a mental impression of informality that the reader's memory extends — incorrectly — to "no recording either". Policies frequently relax one control while retaining another, and the retained control is what audits check. Read each control's fate separately; never let one relaxation bleed into the neighbouring clause.

**Question 2 (easy) — True, false, or cannot say**

Statement: "Normal changes must be approved by the CAB before they are scheduled."

- A) True
- B) False
- C) Cannot say
- D) False, because approval follows scheduling

**Correct answer: A**

**Explanation:** The passage says: "Normal changes require CAB approval before scheduling." The statement restates this accurately — approval precedes scheduling — so it is True. Note the ordering language: "approval before scheduling" is a sequence constraint, and sequence constraints are where paraphrase most often goes wrong (option D asserts the reversed sequence). When you document change requests in real life, this is the clause that determines whether you may pencil a change into next week's window while approval is pending — under this policy, for a normal change, you may not. Verbal reasoning at senior level is substantially the accurate handling of before/after, may/must, and unless/only-if structures, because your operational calendar is built from them.

**Question 3 (moderate) — True, false, or cannot say**

Statement: "An emergency change implemented on a Thursday must receive retrospective approval within five working days."

- A) True
- B) False
- C) Cannot say
- D) True, because the CAB meets weekly

**Correct answer: B**

**Explanation:** Parse what the passage actually requires: retrospective approval for an emergency change "must be sought at the next CAB meeting". The CAB meets every Wednesday, so a Thursday emergency change goes to the following Wednesday's meeting — approval must be *sought* there, but the passage sets no deadline for approval to be *received*, and the five-working-day figure belongs to a different rule entirely: it is the reversal deadline after a *refusal* of retrospective approval. The statement therefore splices two provisions into a requirement the passage never makes, contradicting what is written — False. This splicing pattern is a premium assessment trap and a real documentation hazard: numbers migrate between clauses in the reader's memory. When a statement quotes a figure, return to the passage and confirm which rule the figure genuinely governs.

**Question 4 (moderate) — True, false, or cannot say**

Statement: "If an emergency change is refused retrospective approval, it will always be reversed."

- A) True
- B) False
- C) Cannot say
- D) True, within five working days

**Correct answer: B**

**Explanation:** The passage requires reversal within five working days of refusal — "unless reversal would itself cause greater service impact, in which case the service owner decides the way forward." The exception means reversal is not guaranteed in every case: where reversal is the more damaging option, the outcome rests with the service owner and might be to retain the change. "Always" is therefore contradicted by the explicit exception, making the statement False (and D fails with it, inheriting the same "always" through its unqualified phrasing). Absolute quantifiers — always, never, all, none — are the highest-value words in any statement you are asked to judge: a single documented exception defeats them. The operational parallel is exact: quoting a policy to a stakeholder as "we must reverse it" when the policy contains a service-impact exception misstates both your obligation and their options.

**Passage 2 — Supplier security notice**

*"Security bulletin SB-2044: A vulnerability has been identified in versions 8.0 through 8.6 of the platform. Version 8.7, released today, resolves the issue. Customers running affected versions should apply the 8.7 update within 14 days. For clustered deployments, nodes may be updated sequentially without a full outage, provided all nodes are updated within a single 24-hour period; mixed-version clusters operating beyond 24 hours are unsupported and may exhibit data synchronisation errors. Customers unable to update within 14 days should apply the interim mitigation described in appendix A, which reduces but does not eliminate exposure. Exploitation of this vulnerability has been observed in the wild. This bulletin will be updated if further information becomes available."*

**Question 5 (moderate) — True, false, or cannot say**

Statement: "A clustered deployment can be updated to 8.7 without any full outage, as long as every node is updated within 24 hours."

- A) True
- B) False
- C) Cannot say
- D) True, but only for version 8.6 clusters

**Correct answer: A**

**Explanation:** The passage states: "For clustered deployments, nodes may be updated sequentially without a full outage, provided all nodes are updated within a single 24-hour period." The statement reproduces both the permission (sequential update, no full outage) and its condition (all nodes within 24 hours), so it is True. Option D invents a version restriction the passage does not make — the sequential-update provision applies to clustered deployments generally, not to 8.6 alone. The skill being sampled is condition-complete reading: a permission and its proviso form a single unit of meaning, and the statement is only True because it carries both halves. In change planning, this clause is exactly what you would transcribe into the change request's implementation plan — and transcribing the permission without the 24-hour proviso is how a two-day rolling update becomes an unsupported mixed-version cluster with synchronisation errors.

**Question 6 (moderate) — Inference from the bulletin**

Which one of the following can properly be inferred from the bulletin?

- A) Version 7.9 is affected by the vulnerability.
- B) The supplier regards this vulnerability as carrying real, current risk, since exploitation has been observed in the wild and the mitigation only reduces exposure.
- C) Applying the appendix A mitigation makes updating to 8.7 unnecessary.
- D) All customers will be able to update within 14 days.

**Correct answer: B**

**Explanation:** Test each candidate. A: the affected range is "8.0 through 8.6"; the bulletin says nothing about 7.9 — you might privately suspect older versions, but the text does not support it (as an inference question, silence defeats the claim). C: the mitigation "reduces but does not eliminate exposure" and is explicitly for customers "unable to update within 14 days" — an interim measure, not a substitute; the bulletin's structure treats updating as the resolution. D: the existence of provisions for customers "unable to update within 14 days" points the other way. B synthesises two stated facts — observed in-the-wild exploitation and a mitigation that leaves residual exposure — into the conclusion they jointly compel: the risk is real and current. Sound inference combines stated facts into their necessary consequence; unsound inference imports facts from outside the text. In your role, B is also the sentence you would write in the change request's justification field to secure expedited approval.

**Question 7 (hard) — True, false, or cannot say**

Statement: "A customer who updates half their cluster's nodes on Monday morning and the remainder on Thursday will have an unsupported configuration in the interim."

- A) True
- B) False
- C) Cannot say
- D) True, but only if data synchronisation errors actually occur

**Correct answer: A**

**Explanation:** Apply the rule to the scenario's arithmetic. The bulletin permits sequential node updates "provided all nodes are updated within a single 24-hour period" and states that "mixed-version clusters operating beyond 24 hours are unsupported". Monday morning to Thursday is roughly three days — far beyond 24 hours — so between Tuesday morning (24 hours after the first updates) and Thursday, the cluster is a mixed-version deployment outside the supported window: unsupported, as the statement says. True. Option D confuses the *status* with its *symptoms*: the configuration is unsupported by rule, whether or not synchronisation errors "may" materialise — support status is defined by the condition breached, not by whether harm has yet occurred. This distinction is operationally sharp: an unsupported configuration that happens to be working is still a risk position you must report honestly in the change record, and "it seems fine" is not a supported state. Verbal questions that embed a small calculation inside a comprehension task are increasingly common — do the arithmetic, then apply the rule.

**Passage 3 — Incident report and stakeholder communication**

*"Incident INC-4471 summary (drafted by the resolving engineer): The document service failed at 10:42 on Tuesday following the morning's deployment of release 3.9. Initial diagnosis suspected the release; rollback was performed at 11:15 but the failure persisted. Further investigation identified the actual cause as expiry of the service's TLS certificate at 10:42, which the monitoring system was not configured to track. The certificate was renewed and service restored at 12:05. Release 3.9 was redeployed at 14:00 without incident. Total user-facing outage: 83 minutes. Actions proposed: add certificate expiry monitoring for all services in the estate; review the certificate inventory for other certificates expiring within 90 days; document the renewal procedure, which currently exists only as informal knowledge."*

*"Stakeholder update sent at 11:00 (before diagnosis completed): 'The document service is currently unavailable following this morning's software release. We have begun rolling back the release and expect service to be restored shortly.'"*

**Question 8 (moderate) — True, false, or cannot say**

Statement: "The rollback performed at 11:15 restored the service."

- A) True
- B) False
- C) Cannot say
- D) True, in combination with the certificate renewal

**Correct answer: B**

**Explanation:** The report states: "rollback was performed at 11:15 but the failure persisted", and restoration came at 12:05 from certificate renewal. The rollback restored nothing — the failure's cause was never the release, as confirmed by the clean redeployment of 3.9 at 14:00. The statement is contradicted: False. Option D tries to salvage the rollback with a contribution the report does not credit it with; the text attributes restoration to the renewal alone. Beyond the reading exercise, the timeline is a diagnostic parable your **Incident management** skill should savour: "the failure began at the same time as the deployment" was a correlation that consumed 33 minutes of rollback effort, while the true cause — certificate expiry at exactly 10:42 — was a coincidence of timing. When a plausible cause is disproved (failure persists after rollback), the disproof is itself high-grade evidence: it eliminated the release and forced the wider search that found the certificate.

**Question 9 (hard) — True, false, or cannot say**

Statement: "The 11:00 stakeholder update contained information that later proved inaccurate."

- A) True
- B) False
- C) Cannot say
- D) False, because the update was reasonable given what was known at 11:00

**Correct answer: A**

**Explanation:** Compare the update's claims against the report's established facts. The update says the service is "unavailable following this morning's software release" — attributing the outage to the release — and that rollback should restore service "shortly". Both later proved wrong: the cause was the certificate, not the release, and the rollback did not restore service. So the update contained information that later proved inaccurate: True. Option D deserves careful dismantling because it is *also* a fair judgement — the update was indeed reasonable on the 11:00 evidence — but reasonableness and accuracy are different properties, and the statement asks only about accuracy. A statement can be True while the conduct it describes remains defensible. This distinction matters in real communications practice: the lesson from INC-4471 is not "never update stakeholders before diagnosis" but "phrase interim updates as hypotheses" — 'we believe the cause may be this morning's release and are rolling it back' would have been both reasonable *and* accurate. Assessments reward separating the question asked from the adjacent question you would rather answer.

**Question 10 (hard) — True, false, or cannot say**

Statement: "Certificate expiry monitoring was in place for some services in the estate before the incident."

- A) True
- B) False
- C) Cannot say
- D) False, because the monitoring system was not configured to track the expired certificate

**Correct answer: C**

**Explanation:** The report says the monitoring system "was not configured to track" the document service's certificate, and proposes to "add certificate expiry monitoring for all services in the estate". Does that proposal imply no service currently has it, or that coverage is merely incomplete? The text supports neither reading decisively: "add … for all services" is compatible with extending partial coverage to completeness and with introducing monitoring from zero. Since the passage neither confirms nor denies monitoring on *other* services, the answer is Cannot say. Option D generalises from one certificate to the whole estate — precisely the over-extension the Cannot say category exists to catch. The professional habit this trains is scope discipline in reading post-incident actions: "add X for all services" tells you the desired end state, not the current state, and a senior engineer reviewing the action would ask the scoping question rather than assume. In problem management terms: before initiating the estate-wide action, first verify the estate's actual baseline — which is your **Asset and configuration management** instinct applied to a sentence.

**Question 11 (hard) — Best summary of the incident**

Which option best summarises INC-4471 for a service review audience?

- A) "Release 3.9 caused an 83-minute outage of the document service; the release was rolled back and later redeployed."
- B) "The document service suffered an 83-minute outage caused by an untracked TLS certificate expiring; the coincident release 3.9 was initially suspected and rolled back, but was exonerated and redeployed successfully. Actions: certificate expiry monitoring across the estate, a 90-day certificate inventory review, and documentation of the renewal procedure."
- C) "A certificate expired but was quickly renewed; impact was minimal and the release proceeded as planned."
- D) "Monitoring failures caused a certificate to expire, resulting in an outage."

**Correct answer: B**

**Explanation:** Judge each against the record. A repeats the initial misdiagnosis as fact — the report explicitly exonerates the release — so it would propagate a falsehood into the governance record, where it might drive wrong actions (release-process scrutiny instead of certificate management). C minimises: 83 user-facing minutes is not "minimal", and "quickly" editorialises a two-diagnosis incident. D contains a causal error: monitoring did not cause the expiry — certificates expire by calendar; the monitoring gap caused the expiry to be *unanticipated* — and a summary that mistakes "failed to warn" for "caused" misdirects the fix. B preserves the true cause, the honest narrative of suspicion and exoneration (which itself justifies one of the actions), the accurate impact figure, and all three proposed actions, in four sentences. Summary questions are compression tests: the best answer loses bulk while preserving every causal link and every decision-relevant fact. Writing this summary well is your **Ownership and topic** skill's final act on any incident — the record you hand to the organisation is the incident, as far as the future is concerned.

**Question 12 (hard) — Clear-writing judgement in a change request**

You are documenting the change request for the estate-wide certificate monitoring work. Which implementation-summary wording is clearest and most complete for CAB approval?

- A) "Add cert monitoring to fix the INC-4471 thing so it doesn't happen again."
- B) "Configure certificate expiry monitoring (30-day and 7-day alerts) for all 23 production services; no service outage required; implementation via the standard monitoring pipeline over five working days; rollback is removal of the monitoring configuration; risk: alert noise during initial tuning, mitigated by routing first-week alerts to the operations channel only. Addresses the monitoring gap identified in INC-4471."
- C) "Certificate monitoring will be implemented in accordance with best practice at the earliest opportunity, leveraging synergies with the existing observability estate."
- D) "Monitoring for certificates. 23 services. See INC-4471."

**Correct answer: B**

**Explanation:** A CAB needs to approve a specific, bounded action, so the clearest wording answers the approver's questions in one pass: what exactly (expiry monitoring with defined alert thresholds), where (all 23 production services — a countable scope), impact (no outage), how and when (standard pipeline, five days), reversibility (removal of configuration), risk and mitigation (alert noise, contained routing), and why (the INC-4471 gap). Option B does all of this in five lines. Option A is informal and unbounded — "the INC-4471 thing" forces every reader back to the source record. Option C is the most instructive failure: it is grammatical, professional-sounding, and empty — "best practice", "earliest opportunity", and "leveraging synergies" convey no scope, schedule, impact, or reversibility, and a CAB approving it would not know what it had approved. Option D has fragments of the right content but transfers the assembly work to the reader. The assessment lesson generalises: clarity is measured by the questions a reader no longer needs to ask. Your **Change management** skill names this directly — documenting change requests — and option B is what that duty looks like when done so well that approval takes one reading.

### Preparation tips

- **Answer from the passage, especially when you know better.** Experienced engineers lose verbal reasoning marks by answering from professional convention when the passage deviates from it. The passage is the policy; read what is written.
- **Track figures to their owning clause.** When a number appears in a statement — five days, 24 hours, 14 days — return to the passage and confirm which rule it actually governs. Spliced provisions are the classic senior-level trap.
- **Interrogate absolutes.** Before marking a statement containing "always", "never", or "all" as True, hunt the passage for exceptions. One "unless" defeats an "always".
- **Separate status from symptoms, and accuracy from reasonableness.** "Unsupported" is true when the condition is breached, harm or no harm; "inaccurate" is true when facts later diverge, however defensible the original claim. Answer the property the statement actually asserts.
- **Practise compression on your own records.** Take a closed incident and write the four-sentence summary that preserves every causal link. Compare with the record a week later. This trains both the summary questions and your real reporting.
- **Read one framework definition daily.** Your Level 3 service management knowledge doubles as verbal training: definitions of incident, problem, change, and release are exercises in precise conditional reading.

### Common pitfalls to avoid

- **Letting one relaxed control relax its neighbours.** "No CAB review needed" does not imply "no recording needed". Track each requirement's fate separately through the passage.
- **Confusing "must be sought" with "must be received".** Obligations to attempt, to seek, or to request are not obligations to obtain. Verbal reasoning — and governance — turn on such verb distinctions.
- **Treating vivid correlation as stated causation.** An outage "following" a release is a sequence, not a verdict. Mark causal claims True only when the passage itself establishes the cause.
- **Rescuing a contradicted statement with outside charity.** If the text says the rollback did not restore service, no plausible-sounding "in combination with" option can make it True.
- **Under-using Cannot say on scope questions.** "Add X for all services" describes an end state, not the current state. When the passage is silent on the baseline, Cannot say is the strong answer, not the timid one.
- **Preferring polished vagueness in clear-writing questions.** The professional-sounding option stuffed with "best practice" and "synergies" is a deliberate decoy. Choose the option that leaves the fewest questions unanswered, however plain its style.

## Workplace job-specific situational judgement assessment

### About this assessment

A situational judgement assessment (SJT) presents realistic workplace dilemmas and asks you to evaluate possible responses — typically identifying the most effective, the least effective, or ranking all options. There is rarely a flawless option; the scenarios are engineered so that every response is something a real professional might plausibly do, and the discrimination is between good and slightly-less-good as often as between right and wrong. Scoring compares your judgements with those of experienced practitioners and with the behaviours the organisation values: user and service focus, ownership, collaboration, honest communication, proportionate escalation, and integrity under pressure.

The typical format is an online test of 12 to 20 scenarios, untimed or generously timed, with four responses each. For senior roles, scenarios shift characteristically: less "should I ask for help?" and more "I am the person others are asking" — pressure from stakeholders to compress testing, discretion over emergency changes, conflicts between a deadline and a freeze, a junior engineer's mistake happening on your watch, and the ever-present question of what to communicate, to whom, and when.

Why do employers use SJTs for senior operations roles? Because at your level, technical correctness is assumed and judgement is the differentiator. You hold deployment authority and change co-ordination responsibility: the organisation's exposure to your decisions is highest precisely in the ambiguous moments — the go-live that is 90% fine, the workaround that would save tonight but haunt the estate, the metric that could be reported two ways. Your role summary's **Ownership and topic** skill states the standard plainly: own an issue until a new owner has been found or the problem has been mitigated or resolved. SJTs measure whether your instincts implement that standard when it is costly.

As you work through the scenarios, notice the recurring anatomy of strong answers: they secure the service first, preserve truthful records and communications, use the change and incident processes rather than bypassing them, keep the user's outcome in view, and treat colleagues — junior, senior, and supplier — in ways that keep information flowing. Weak answers hide, gamble, bypass, or optimise a metric at the expense of the mission.

### How this assessment maps to your role

- **Deployment and go-live dilemmas** map to **Change management** and **Testing**: pressure to skip verification, ambiguous test results before a release, and freeze-period requests test whether you action changes as documented and let evidence gate releases.
- **Incident command scenarios** map to **Incident management** and **Ownership and topic**: diagnosing under pressure, communicating honestly mid-incident, and holding ownership until genuine handover are the core senior behaviours.
- **Escalation and consultation judgement** maps to **Problem management**: effectively consulting specialists where required means neither hoarding a problem beyond your expertise nor dumping it prematurely — a calibration SJTs probe repeatedly.
- **Configuration integrity scenarios** map to **Asset and configuration management**: undocumented workarounds, unrecorded changes, and tempting shortcuts test whether you keep records matching reality when nobody is checking.
- **Service performance dilemmas** map to **Availability and capacity management** and **Service focus**: choosing between a KPI's appearance and its meaning, and between a quick fix and a coherent framework, reveal what you actually optimise for.
- **Stakeholder and user scenarios** map to **User focus**: keeping user outcomes central when technical and political pressures point elsewhere.

### Practice questions

**Question 1 (easy) — Pressure to skip smoke tests**

A release has run late: the deployment finished 40 minutes behind schedule, and the 30-minute smoke test suite would take the window to its final minute. The delivery manager messages: "Everything deployed cleanly — can we skip the smoke tests and call it done? The team's exhausted." What is the most effective response?

- A) Agree — a clean deployment is strong evidence the release is fine.
- B) Run the smoke tests as planned, explaining that they are the evidence the service works for users, that the window still accommodates them, and that "deployed cleanly" and "working" are different claims.
- C) Skip the tests but monitor closely tomorrow morning and fix anything users report.
- D) Run a hand-picked 10-minute subset of the suite and declare the release verified.

**Correct answer: B**

**Explanation:** The window still fits the full suite — the pressure here is fatigue and optimism, not genuine constraint, and option B holds the evidence gate while explaining rather than merely refusing: deployment success means the artefacts arrived; smoke tests establish that the service functions, which is the claim stakeholders and users actually care about. Option A mistakes one for the other. Option C converts users into the test suite — tomorrow's incidents become your verification mechanism, which inverts **User focus** and typically costs more engineer-hours than the 30 minutes saved. Option D is the subtle trap for senior candidates: it sounds like proportionate pragmatism, but an improvised subset chosen at 02:00 by tired people has unknown coverage, and "declared verified" on partial evidence corrupts the release record — if a subset is ever to stand in for the suite, that decision belongs in the tested, pre-agreed release process, not in the final minutes of a window. Your **Testing** skill frames it exactly: test conditions are defined from requirements in advance, not negotiated against exhaustion at the finish line.

**Question 2 (easy) — An undocumented workaround discovered**

While investigating slow performance, you discover that a previous engineer (who has left) applied a manual configuration change to a production server that does not appear in the CMDB or in any change record. The change appears deliberate and is possibly load-bearing. What is the most effective response?

- A) Remove it immediately — undocumented changes have no place in production.
- B) Leave it alone and say nothing; it seems to be working and it is not your mess.
- C) Document it now as found (server, setting, apparent purpose), raise a record to investigate its function and dependencies, and only then decide — through change management — whether to formalise or remove it.
- D) Quietly replicate it to the other servers in the pool for consistency.

**Correct answer: C**

**Explanation:** Two wrongs are available here and option C avoids both. Removing on principle (A) treats documentation status as evidence about function: an undocumented change may still be load-bearing, and deleting it untested is how a performance investigation becomes a severity 1 — principle is not a diagnostic. Ignoring it (B) fails **Asset and configuration management** at its core — maintain accurate information — and fails **Ownership and topic**: you found the issue; it is yours until properly handed over or resolved, and "not my mess" is precisely the attitude the skill exists to exclude. Option D is the worst of all: propagating an ununderstood change multiplies unknown risk and adds three more undocumented deltas to the estate. Option C sequences correctly: first make the record match reality (document as found), then understand (investigate function and dependencies, consulting specialists if needed), then decide through the proper mechanism (a change request to formalise or remove). The order — record, understand, decide — is the configuration-integrity pattern that recurs across senior operations work, and assessors look for it explicitly.

**Question 3 (moderate) — Emergency change temptation**

It is Friday at 17:30. A director calls you directly: a report needed for Monday's ministerial briefing is failing to generate, and she asks you to "just put a fix in tonight — I'll take responsibility." Your department's process allows emergency changes only where delay would cause significant service impact, with duty manager approval. You have diagnosed the fault and have a fix ready. What is the most effective response?

- A) Deploy the fix immediately — a director has authorised it.
- B) Refuse: no changes outside the CAB cycle, ministerial briefing or not.
- C) Tell the director the fix exists and can plausibly qualify as an emergency change given the briefing impact, contact the duty manager for the required approval, and deploy tonight through the emergency process with full documentation if approved.
- D) Deploy the fix tonight but record it on Monday as a normal change to avoid weekend paperwork.

**Correct answer: C**

**Explanation:** The emergency change process exists for exactly this shape of situation — genuine business impact, delay costly, fix ready — so the senior move is neither to bypass governance nor to hide behind it. Option C runs the process at pace: the impact case (a ministerial briefing) is articulated to the actual approval authority, the deployment happens tonight if approved, and the record is complete. Option A substitutes seniority for process: a director's "I'll take responsibility" is not the duty manager approval the process names, and verbal responsibility evaporates when an unapproved Friday-night change breaks something Saturday. Option B is the rigidity failure — quoting the change cycle at a legitimate emergency mistakes the process's letter for its purpose, and it teaches stakeholders that the process is an obstacle rather than a route, encouraging future bypasses. Option D is the integrity failure: deploying under emergency conditions while falsifying the category on Monday corrupts the change record and, once discovered, taxes every future claim you make. The discriminating insight: governance at senior level is a thing you *operate skilfully under pressure*, not a thing you either worship or evade.

**Question 4 (moderate) — Junior engineer's production mistake**

A junior engineer you are supervising ran a cleanup script against production instead of the test environment. Data has been deleted; the application is erroring; users are affected. The junior is visibly distressed and offers to "fix it quietly before anyone notices". What is the most effective response?

- A) Let them attempt the quiet fix — it will build their confidence and protect them from embarrassment.
- B) Declare the incident through the normal process, take charge of restoration (backups, impact assessment), keep the junior involved in the recovery so they learn, and make clear — publicly if needed — that the systemic gap (production access safeguards) matters more than individual blame.
- C) Take over completely, send the junior home, and handle everything yourself.
- D) Report the junior to their line manager as a first step and let the manager decide the incident response.

**Correct answer: B**

**Explanation:** Sequence the duties: service first, people second, lessons third — option B honours all three in order. Declaring the incident is non-negotiable: users are affected now, and an undeclared incident with quiet fixing (A) compounds a mistake into a concealment, delays restoration expertise, and teaches the junior that hiding is how professionals respond — the exact inversion of the culture that prevents repeat events. Keeping the junior inside the recovery converts the worst day of their year into their most durable learning, while your visible framing — "the interesting question is why production was reachable by that script at all" — models blameless post-incident practice and surfaces the systemic fix (access controls, confirmation prompts) that actually prevents recurrence. Option C protects the service but discards the person and the learning; it also leaves you without a second pair of hands mid-incident. Option D outsources incident command at precisely the moment your **Incident management** and **Ownership and topic** skills make it yours — personnel conversations have their place, later, and led with empathy. Assessors read this scenario as a culture probe: the senior engineer's response to a junior's mistake sets the team's honesty economics for years.

**Question 5 (moderate) — Mid-incident stakeholder communication**

Ninety minutes into a major incident, the cause remains unknown. The service owner asks for an update to send to directors, adding: "Can we say we've identified the cause and are fixing it? It sounds better than 'still investigating'." What is the most effective response?

- A) Agree — confidence reassures stakeholders and you will probably find the cause soon anyway.
- B) Provide an update that is honest and still substantive: confirmed impact and scope, what has been ruled out, current diagnostic focus, mitigation in place, and the time of the next update — declining to claim a cause you do not have.
- C) Refuse to send any update until the cause is found, to avoid saying anything wrong.
- D) Send the honest version to the service owner but let them alter it as they see fit.

**Correct answer: B**

**Explanation:** The service owner's request is common and human — and granting it creates a specific, predictable failure: when the claimed cause proves wrong (as INC-style incidents regularly do), the follow-up must retract a fabrication, at which point stakeholders re-read every prior update with suspicion and demand direct involvement, which slows the actual diagnosis. Option B demonstrates the senior communicator's craft: honesty is not emptiness — "we have ruled out the release and the network path, current focus is the database layer, read-only access is restored, next update at 14:30" is more reassuring than false certainty, because it exhibits control of the *process* even without control of the *cause*. Option C confuses accuracy with silence; stakeholders abhor a vacuum and will fill it with worse. Option D is the subtle abdication: you know the alteration being contemplated is a falsehood about your incident; handing over the pen with that knowledge is participation by omission — the better move is to give the service owner honest language good enough that they do not want to alter it. This is **Ownership and topic** applied to information: you own the truthfulness of what the organisation knows about your incident.

**Question 6 (moderate) — Consult or continue?**

You have spent six hours investigating intermittent database deadlocks. You have solid evidence and two hypotheses, but confirming either requires deep database internals expertise at the edge of yours. The organisation has a database specialist team with a two-day response queue; the problem is causing a handful of failed transactions daily — annoying, not critical. A part of you wants to crack it yourself. What is the most effective response?

- A) Continue solo — six hours of context would be wasted in a handover, and you are close.
- B) Package the investigation now (timeline, evidence, eliminated causes, both hypotheses, reproduction steps) and engage the specialist team, continuing lower-risk investigation strands and mitigation in parallel while the request is queued.
- C) Drop the problem entirely into the specialists' queue and move on — it is their domain.
- D) Apply both candidate fixes to production and see which stops the deadlocks.

**Correct answer: B**

**Explanation:** Your **Problem management** skill names this judgement precisely: "effectively consult specialists where required" — and the craft is in both halves of option B. *Engaging now* respects the two-day queue arithmetic: at moderate severity, the cheapest schedule starts the clock today rather than after two more days of solo effort at your expertise boundary. *Packaging well* is what makes consultation effective rather than expensive: a specialist receiving a timeline, eliminated hypotheses, and reproduction steps starts at hour six, not hour zero — the handover quality converts your sunk investigation into their head start, answering option A's real concern without option A's gamble. Option A also misprices "close": at the edge of your expertise, confidence about proximity is exactly the signal to distrust. Option C throws away the packaging value and abandons mitigation — dumping is not consulting, and **Ownership and topic** keeps the problem yours until the specialists genuinely take it. Option D experiments on production with concurrent variables: even if the deadlocks stop, you will not know which fix worked or what else changed — untested changes applied speculatively violate both change management and the scientific discipline that makes problem management converge.

**Question 7 (moderate) — Least effective: capacity warning before a big event**

Your capacity monitoring shows the case application will likely exceed safe utilisation during next month's legislative deadline, when submission volumes triple. Additional capacity takes three weeks to provision. It is four and a half weeks before the deadline. Which response is LEAST effective?

- A) Raise the forecast formally now with the evidence, request the capacity, and identify interim levers (caching, deferring batch jobs) in case provisioning slips.
- B) Wait two weeks to see whether the growth trend continues before requesting anything — the forecast might be pessimistic.
- C) Brief the service owner on the risk and the decision deadline, so the cost of inaction is owned at the right level.
- D) Begin load-testing the interim levers now so their effect is quantified before they are needed.

**Correct answer: B**

**Explanation:** Read the stem's polarity first — this asks for the LEAST effective option. Then do the arithmetic that damns option B: provisioning takes three weeks; the deadline is 4.5 weeks away; the decision window is therefore about 1.5 weeks. Waiting two weeks consumes the entire window and then some — the option converts a manageable risk into a fait accompli, and "the forecast might be pessimistic" is an argument for *refining* the forecast in parallel, never for burning the decision window to find out. Options A, C and D compose exactly the senior playbook: A acts within the window with evidence and a fallback; C places the risk-acceptance decision with the accountable owner while there is still a decision to make — an underrated move that assessors reward, because engineers who silently absorb capacity risk deny the organisation its chance to choose; D turns the fallback from hope into measured capability. This is **Availability and capacity management** as the skill statement means it — managing components against business needs — where the business need has a statutory date and the engineering calendar must be run backwards from it.

**Question 8 (hard) — The KPI that can be reported two ways**

Preparing the monthly service report, you find availability can be honestly calculated as 99.6% (counting a 3-hour degradation where the service was up but unusably slow for most users as downtime) or 99.92% (counting only full outages, as the report has historically done). The KPI target is 99.9%. The historical method says "met"; the user-experience method says "missed". What is the most effective response?

- A) Report 99.92% — consistency with the historical method is what makes trends meaningful.
- B) Report 99.6% without comment — the users' experience is the truth.
- C) Report both figures with the definitions, note that the historical method counts the degradation as available while users could not work, and propose that the service review agree the definition going forward.
- D) Report 99.92% this month but quietly switch methods next month.

**Correct answer: C**

**Explanation:** This scenario tests whether you understand what reporting is *for*. Option A's consistency argument is genuinely weighty — trend comparability matters — but consistency in a definition that calls an unusable service "available" preserves comparability of a number that no longer measures the thing the KPI exists to protect. Option B corrects the meaning but breaks the trend silently, inviting the accusation of moving goalposts and losing the audience for the better method. Option D combines A's problem with a concealed methodology change — the worst of both, and a small integrity failure that compounds. Option C is the senior answer because it refuses the false choice: both figures, both definitions, the gap explained in user terms ("during those three hours, caseworkers could not process submissions"), and the *decision about the definition* routed to the governance forum that owns the KPI. That last step matters most: a definition change adopted unilaterally — in either direction — is a report shaped by the reporter; a definition agreed at service review is a measurement the organisation owns. This is **Service focus** (coherent frameworks that work) meeting **User focus** (data about users turned into outcomes) in the place they most often collide: a metric.

**Question 9 (hard) — Freeze-period pressure with a twist**

During the pre-Christmas change freeze, a programme manager asks you to deploy "one tiny config change" to enable a feature demo for the minister's visit on 20 December. The change genuinely is small; you have made similar ones dozens of times. The freeze policy allows exemptions via the design authority, which meets tomorrow. The programme manager says: "The exemption route is for real changes. This is nothing — no one will ever know." What is the most effective response?

- A) Make the change — it genuinely is trivial, and ministerial visits matter.
- B) Decline to bypass the freeze, and — because the demo matters — offer the legitimate fast path: help the programme manager draft the exemption request tonight for tomorrow's design authority, including your technical assessment that the change is low-risk.
- C) Refuse and report the programme manager's request to their director.
- D) Make the change in the demo environment only, telling the programme manager it is production.

**Correct answer: B**

**Explanation:** Strip the scenario to its logic: an exemption process exists, its timeline fits (the authority meets tomorrow, the visit is later), and the requester's argument is not "the process will refuse" but "the process is beneath this change" — which, examined closely, is the argument for *every* freeze breach ever made, since no one proposes risky changes as "tiny". Option B wins on both integrity and service: the freeze holds, and the programme manager gets what they actually need — a route to yes — with your low-risk assessment strengthening their case, which is collaboration rather than obstruction. "No one will ever know" deserves particular attention: change records mean someone can always know, and a senior engineer's willingness to act on that phrase is precisely what SJTs are calibrated to detect (option A). Option C escalates a resolvable request into a conflict before trying resolution — proportionality matters; report patterns, resolve moments. Option D is disqualifying on honesty grounds: deceiving a colleague about what environment they are demonstrating — to a minister — manufactures a future incident with your name in it. The senior pattern: when someone asks you to bypass a process, the strongest response is usually to *run the process better than they thought possible*.

**Question 10 (hard) — Ranking: the failed change you co-ordinated**

A change you co-ordinated last night partially failed: the deployment succeeded, but this morning an integration with a partner department's system is erroring, affecting cross-departmental case referrals. Rank these responses from most to least effective:

1. Declare an incident, notify the partner department's operations team with symptoms and timeline, begin diagnosis with rollback explicitly on the table, and record the change as "failed" pending investigation.
2. Begin diagnosing quietly first: if you can fix it within the hour, the change record can stay "successful" and the partner never needs to be troubled.
3. Roll back immediately without diagnosis, then investigate at leisure in the test environment.
4. Declare an incident and diagnose, but describe the change as "successful with unrelated integration issues" in the record, since the deployment itself worked.

- A) 1, 3, 2, 4
- B) 1, 3, 4, 2
- C) 3, 1, 2, 4
- D) 1, 2, 3, 4

**Correct answer: A**

**Explanation:** Response 1 is clearly first: the incident is declared (users of cross-departmental referrals are affected now), the partner is informed — critical, because their operations team may be fielding the same symptoms without your context, and inter-departmental trust is spent or earned in exactly these moments — and the change record reflects reality. Response 3 is second: immediate rollback is a defensible, sometimes optimal choice — it restores service fast at the cost of diagnostic evidence and the change's benefits — but done *without any diagnosis or partner notification* it is a blunt version of the right instinct; ranked below 1 because 1 preserves both the rollback option and the information flows. The genuinely discriminating judgement is ranking 2 versus 4, the two concealments. Response 2 hides the event for up to an hour — bad: the partner diagnoses blind and the record is provisionally wrong — but its concealment is *temporal* and collapses honestly if the fix fails. Response 4 declares the incident (better operationally) yet engineers a *permanent* falsehood into the change record: "successful with unrelated issues" is a characterisation crafted to survive scrutiny, corrupting the failure statistics your organisation uses to judge change risk, and — unlike 2's deferral — it never self-corrects. A durable, deliberate misrecord outweighs a short honest-by-default delay: 1, 3, 2, 4 — option A. The underlying principle: in operations, records are load-bearing; a lie that enters the record does damage long after the incident is forgotten.

**Question 11 (hard) — User needs versus stakeholder assumption**

Budget exists to improve the case application, and the deputy director has directed it toward a dashboard "because caseworkers keep complaining about the system". You review the evidence: 68% of recent tickets concern save failures and slow document loading; your informal conversations with caseworkers confirm stability is their overwhelming pain point; nobody has mentioned dashboards. The deputy director's programme announcement is next week. What is the most effective response?

- A) Build the dashboard as directed — the deputy director presumably has context you lack.
- B) Build the dashboard but quietly divert some capacity to fixing the save failures.
- C) Before the announcement, present the evidence: the ticket analysis, the user conversations, and a proposal to fix the stability issues that the complaints actually concern — offering to run a brief structured validation with caseworkers if the deputy director wants firmer ground.
- D) Survey caseworkers over the next month to build an unimpeachable evidence base, then present findings after the announcement.

**Correct answer: C**

**Explanation:** The deputy director and the evidence agree on the problem (caseworkers are unhappy) and diverge on the cause — and the divergence is checkable *now*, before public commitment makes correction expensive. Option C is your **User focus** skill executed at senior level, almost clause by clause: quantitative data (the 68% ticket analysis) and qualitative data (caseworker conversations) collated as user needs evidence, offered *before* the decision point, with a proposal to strengthen the evidence through defined research if needed — "understand and define research that fits user needs". Crucially, C challenges the direction while respecting the authority: the deputy director still decides, but decides informed, and the timing (before the announcement) is what makes the challenge a service rather than an embarrassment. Option A launders an assumption through deference — "presumably has context" is checkable, so check it. Option B is the quiet-diversion trap: it misuses delegated capacity, delivers a diluted version of both priorities, and denies the deputy director the information that would let them redirect properly — undermining rather than influencing. Option D gathers excellent evidence for a decision that will already have been announced; evidence is worth most *before* commitment, and a month of surveying to confirm what tickets and conversations already show is rigour misapplied. Senior influence is evidence, timed well, offered respectfully.

**Question 12 (hard) — Holding ownership across a boundary**

An intermittent fault in the licensing application traces to a supplier-hosted component. You have raised it with the supplier, who responded: "No fault found our side; closing our ticket." The fault continues — roughly a dozen users affected each day. Your own service desk has begun telling users "it's a supplier issue" and closing tickets. What is the most effective response?

- A) Accept the supplier's finding — they know their component best — and monitor in case it worsens.
- B) Keep the problem record open and owned; assemble evidence the supplier cannot dismiss (timestamps, correlation IDs, traffic captures showing the fault at the boundary); re-engage the supplier through the contract's escalation route; brief the service desk to keep linking user tickets to the problem record; and give affected users a workaround and honest status meanwhile.
- C) Tell the service desk to keep closing tickets as "third party" — the fault is genuinely not in your code.
- D) Escalate immediately to commercial colleagues to invoke contractual penalties against the supplier.

**Correct answer: B**

**Explanation:** This is the scenario for which your **Ownership and topic** skill statement might have been written: own an issue *until a new owner has been found or the problem has been mitigated or resolved* — and the supplier closing their ticket is neither of those things. The users are yours; the service is yours; "it's a supplier issue" describes the fault's location, not its ownership. Option B works every live front: evidentially (a supplier's "no fault found" usually means "not reproducible from what we received" — boundary-level evidence with correlation IDs changes that conversation), procedurally (contracts contain escalation routes precisely for disputed findings — using them is firm, not hostile), organisationally (the service desk closing tickets is quietly destroying your evidence base — every closed-unlinked ticket weakens the pattern your **Problem management** investigation needs), and humanly (a dozen users a day deserve a workaround and the truth). Option A abandons users on the strength of a first-pass denial. Option C makes the evidence destruction official. Option D reaches for the contractual weapon before exhausting the collaborative-with-evidence route — penalties may eventually be right, but as an opening move they convert a solvable technical dispute into a relationship dispute, and you still need this supplier's engineers to fix the component. Boundary problems are the purest test of senior ownership: anyone can own what is clearly theirs.

### Preparation tips

- **Rehearse the anatomy of strong answers.** Secure the service, keep records and communications truthful, run processes rather than bypassing them, keep users in view, keep information flowing. Score each option against all five before choosing.
- **Check the stem's polarity every time.** Most-effective and least-effective questions interleave; the classic lost mark is a perfect judgement applied to the inverted question.
- **Distinguish the process's letter from its purpose.** Senior scenarios repeatedly offer rigid rule-quoting as a decoy. The strong answer usually *operates* the process skilfully — emergency routes, exemptions, escalation clauses — rather than either worshipping or evading it.
- **Watch for permanent versus temporary concealment.** When ranking flawed options, a durable falsehood in a record generally outweighs a short delay in disclosure. Records are load-bearing.
- **Practise on your own history.** Recall three genuinely difficult judgement calls from your last year. For each, name the options you had, the one you chose, and the one you would choose now. SJT fluency is largely honest retrospection, systematised.
- **Calibrate escalation.** Before the test, articulate your personal thresholds: what you resolve, what you inform upward, what you hand to specialists, what goes to governance. Scenarios reward proportionate escalation, and knowing your thresholds keeps you consistent.

### Common pitfalls to avoid

- **The heroic solo fix.** Continuing alone past your expertise boundary, or fixing quietly to spare embarrassment, reads as ownership but scores as risk. Consultation and disclosure are senior strengths.
- **Deference dressed as respect.** "The director authorised it" and "the deputy director presumably knows" are traps: authority does not substitute for the named approval, and assumptions are checkable. Respect authority by informing it.
- **Metric optimisation over mission.** Any option that improves a number — availability, change success rate, ticket closures — by degrading its meaning is a designed trap, however defensible it sounds.
- **Punitive first moves.** Reporting a colleague, invoking penalties, or escalating to directors *before* attempting evidence-based resolution scores poorly. Escalate patterns and impasses, not first requests.
- **Abandoning users at organisational boundaries.** "Supplier issue", "other team's system", "descoped" — none of these ends your ownership while your users remain affected.
- **Treating exhausted-but-possible verification as skippable.** Fatigue is the test's favourite disguise for risk appetite. If the window fits the checks, the checks run.

## Conclusion

You have now worked through a complete set of practice materials for the four assessment types most relevant to a senior application operations engineer: cognitive, numeric reasoning, verbal reasoning, and situational judgement. That is a substantial investment in your own capability, and it deserves acknowledgement — not least because you made it at a level where practice often gets crowded out by delivery.

Consider what you have actually rehearsed. In the cognitive section, you traced dependency graphs to their second-order impacts, recomputed go-live feasibility at milestones, diagnosed faults by eliminating hypotheses against evidence, and sequenced changes under overlapping constraints — the structured thinking behind your **Change management**, **Incident management**, and **Problem management** skills. In the numeric section, you converted availability targets into downtime budgets, weighted averages honestly, forecast capacity exhaustion with lead times and safety margins, and verified remedies with before-and-after arithmetic — the quantitative backbone of **Availability and capacity management** and your **Technical specialism** duty to forecast resource needs. In the verbal section, you read change policies, supplier bulletins, and incident records with clause-level precision, and judged writing by the questions it leaves unanswered — the comprehension and clarity your change requests and reports depend on. And in the situational judgement section, you rehearsed the moments that define senior credibility: holding the evidence gate when everyone is tired, running governance at pace instead of bypassing it, communicating honestly mid-incident, developing a junior through their worst day, and owning a problem across a supplier boundary until your users are genuinely served.

A theme ran through all four sections, and it is worth naming: at your level, accuracy is a form of trustworthiness. The correct percentage, the complete change record, the honest status update, the properly scoped conclusion — each is a small act of reliability, and your organisation's willingness to hand you production systems and go-lives is built from thousands of them. Assessment practice sharpens the same edge your daily work depends on.

Keep the habit going lightly: recalculate one dashboard figure a week, summarise one closed incident in four sentences, sketch one dependency graph from memory and check it. Ten minutes at a time is enough — the compounding does the rest.

Whether your next assessment is part of a promotion, a move, or a development programme, approach it the way you approach a well-planned deployment: prepared, paced, verified as you go, and with your options understood in advance. You manage complexity for a living, and you are demonstrably good at it — this guide has simply made that capability visible to you in a new way.

Good luck — and enjoy the quiet confidence that thorough preparation brings.
