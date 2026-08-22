# Quality Assurance Test Analyst - Psychometric Assessment Resources

## Introduction

Welcome! This guide has been created especially for you as a quality assurance test analyst working within the UK Government Digital and Data profession. Whether you are preparing for an internal assessment, applying for your next role, benchmarking your own capability, or simply curious about how psychometric assessments connect to your daily work, this document will help you practise, reflect, and build confidence.

Psychometric assessments are structured, standardised exercises that measure the mental capabilities and professional judgement that predict success in a role. For a quality assurance test analyst, that means far more than abstract puzzles. The assessments described here are job-specific: they use the kinds of artefacts you genuinely handle — user stories, prototypes, risk registers, test coverage matrices, defect logs, automated run summaries, and stakeholder communications — and the kinds of decisions you genuinely make, such as selecting the most appropriate test approach based on risk, deciding what to test within an agreed approach, judging whether coverage aligns with business risk, and communicating the impact of defects clearly to stakeholders who need to act on them.

Why do these assessments matter for your role in particular? At your level, you design and execute both functional and non-functional tests, and you apply multiple testing techniques to inform an approach that mitigates risk. That work is intellectually demanding in exactly the ways psychometric assessments measure. Analysing artefacts to identify risks is applied logical reasoning. Ensuring test coverage aligns with business risk is prioritisation under constraint. Reading a defect trend table and deciding what it means for the release is numeric reasoning. Interpreting a standard, a policy extract, or a carefully worded stakeholder email is verbal reasoning. And navigating a multidisciplinary team with potentially difficult dynamics — hosting discussions, managing differing stakeholder perspectives, advocating for your team externally — is situational judgement, practised daily. Employers use these assessments for testing roles because the correlation is direct: the tester who reasons carefully, calculates accurately, reads precisely, and judges situations well is the tester whose work protects users and delivery alike.

This document is organised into four main assessment sections, each following the same pattern: an overview of what the assessment measures and why it matters for your role, a mapping of the assessment dimensions to the specific skills in your capability framework, a substantial set of practice questions with full worked explanations, practical preparation tips, and common pitfalls to avoid.

Here is how to get the most from it. First, read each "About this assessment" section so you understand the format and typical conditions. Second, attempt every practice question honestly — commit to an answer before reading the explanation, because the moment of commitment is where learning happens. Third, treat each explanation as a mini-lesson: even when you answer correctly, the worked reasoning will refine your technique and often connects the question back to a skill you use at work. Finally, use the preparation tips and pitfalls sections for self-reflection: they are as much about your professional craft as about test performance.

You already exercise these capabilities every day — this guide simply makes them visible, measurable, and improvable. Take your time, enjoy the practice, and let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive assessment measures the exact mental processes your role demands, using practical workplace scenarios rather than abstract puzzles. Instead of shape sequences and letter grids, it presents you with the everyday materials of your job — coverage matrices, acceptance criteria, environment configurations, defect logs, dependency maps — and asks you to reason quickly and accurately about them.

The typical format is an online, timed test lasting 15 to 30 minutes, with questions covering pattern recognition, logical deduction, error checking, prioritisation, and applied problem solving. Scoring is objective, comparing your responses against a norm group, and modern platforms often adapt question difficulty based on your previous answers — so a test that feels progressively harder is usually a sign you are performing well. Employers typically receive a breakdown of speed versus accuracy rather than a single score, meaning that working both quickly and carefully matters. Most platforms offer short, ungraded practice questions before the real test begins, so you can settle into the interface without pressure.

For a quality assurance test analyst, cognitive assessment is particularly relevant because structured thinking is your professional core. Determining what to test within an agreed approach requires you to decompose features into risks and risks into checks. Ensuring coverage aligns with business risk requires you to hold a many-to-many mapping in mind — which tests cover which requirements, which requirements carry which risks — and to spot the gaps. Exploratory testing, which your role explicitly includes, is applied hypothesis generation: noticing an anomaly, forming a theory, designing the next probe. And critically assessing dependencies, defects and risks means reasoning about chains of cause and consequence under incomplete information. A well-designed cognitive assessment simulates precisely these demands in miniature, which is why practising it improves not only your test score but your everyday analytical sharpness.

### How this assessment maps to your role

The assessment dimensions map directly to the named skills in your role summary:

- **Pattern recognition** maps to **Test analysis** and **Designing and executing tests**: analysing artefacts such as user stories, prototypes, processes and designs means recognising recurring structures and, more importantly, deviations from them — the field validated on one screen but not another, the defect cluster that keeps appearing in the same component, the anomaly that triggers a productive exploratory testing session.
- **Logical deduction** maps to **Test analysis** ("analyse information to identify risks") and **Designing and executing tests**: reasoning from requirements and business rules to their test consequences — including the boundary cases and negative paths the rules imply but do not state — is deduction in professional form.
- **Error checking** maps to **Managing, reporting and resolving defects** and **Test engineering**: critically assessing defects and dependencies, maintaining automated tests, and following engineering standards all depend on spotting inconsistencies between artefacts quickly and reliably.
- **Prioritisation** maps to **Test and quality planning** and your duty to ensure test coverage aligns with business risk: creating or adapting quality testing approaches based on risk is, at its heart, ranked decision-making about where limited testing effort buys the most protection.
- **Applied problem solving** maps to **Designing and executing tests** (exploratory testing, researching new techniques) and **Managing, reporting and resolving defects**: diagnosing why a test fails, isolating variables, and distinguishing system defects from environment or data problems is structured problem solving you perform daily.

### Practice questions

**Question 1 (easy) — Pattern recognition in a defect log**

Reviewing the defect log for a citizen-facing forms service, you notice the following recent defects: D-310 "Date field accepts 31/02", D-312 "Postcode field accepts 9-character entry", D-315 "Phone field accepts letters", D-318 "Confirmation page typo", D-321 "National Insurance field accepts lowercase without conversion". Which defect does not fit the dominant pattern?

- A) D-312
- B) D-315
- C) D-318
- D) D-321

**Correct answer: C**

**Explanation:** Four of the five defects share a pattern: input fields accepting values they should reject or normalise — an invalid date, an over-long postcode, letters in a phone number, unconverted lowercase in an NI number. D-318 is a content typo, unrelated to input validation. Recognising this cluster is more than a test-question skill: a run of validation defects strongly suggests a systemic weakness — perhaps the team lacks a shared validation library, or client-side validation is inconsistently applied — and that insight should shape your next move as an analyst: rather than testing fields one by one as defects arrive, you would design a validation-focused test set across all fields and raise the systemic pattern with the developers. Analysing information to identify risks means seeing the shape behind the instances, and defect clustering is one of the most reliable shapes there is.

**Question 2 (easy) — Logical deduction from a business rule**

A benefits calculator's rule states: "Applicants qualify for the higher rate if they are over state pension age AND live alone, OR if they receive the disability premium." An applicant lives alone, is under state pension age, and does not receive the disability premium. What does the rule imply?

- A) The applicant qualifies for the higher rate.
- B) The applicant does not qualify for the higher rate.
- C) The applicant qualifies only at state pension age.
- D) The rule does not cover this applicant.

**Correct answer: B**

**Explanation:** Parse the rule's logical structure carefully: (over pension age AND lives alone) OR (disability premium). Evaluate each branch for this applicant. First branch: lives alone is true, but over pension age is false — an AND fails if either part fails, so the first branch is false. Second branch: no disability premium, so false. False OR false is false: the applicant does not qualify. Option C smuggles in a prediction about the future the rule does not make (their living situation could change). Option D is wrong because the rule does cover this applicant — it evaluates to "no". This is exactly the reasoning you apply when designing tests for conditional logic: a rule with an AND inside an OR needs test cases for each branch and each failure mode, and a common defect is code that treats the AND as an OR. Decision-table thinking — enumerate the conditions, evaluate systematically — is a core technique for your **Designing and executing tests** skill.

**Question 3 (moderate) — Error checking a coverage matrix**

Your coverage matrix for a release maps requirements to test cases. The agreed approach requires: every "High" risk requirement to have at least two test cases, and every requirement to have at least one. An extract shows:

| Requirement | Risk | Test cases |
|---|---|---|
| R1: Submit application | High | TC-01, TC-02 |
| R2: Save draft | Medium | TC-03 |
| R3: Upload evidence | High | TC-04 |
| R4: Withdraw application | Low | — |
| R5: Payment calculation | High | TC-05, TC-06, TC-07 |

How many requirements currently breach the agreed approach?

- A) 1
- B) 2
- C) 3
- D) 4

**Correct answer: B**

**Explanation:** Apply both rules to each row. R1: High with two test cases — compliant. R2: Medium with one — compliant (the two-case rule applies only to High). R3: High with only one test case — breach of the High-risk rule. R4: no test cases at all — breach of the universal rule. R5: High with three — compliant. Two breaches: R3 and R4. The instructive detail is R3: it has a test case, so a quick visual scan ("every row filled except R4") would miss it — you must check the count against the risk rating, not just presence. This mirrors real coverage assurance: ensuring coverage aligns with business risk means the depth of testing must track the risk level, and shallow coverage of a high-risk requirement is the kind of gap that looks fine on a dashboard and fails in production. In the assessment as in the matrix: check each row against every applicable rule, not against a general impression.

**Question 4 (moderate) — Prioritisation across a testing day**

You return from leave to find four items. The release decision meeting is in three days. Which sequence is most defensible?

1. A developer's fix for a Severity 1 defect (payment reference corruption) has been awaiting retest since yesterday; the fix blocks two other defect fixes from being merged.
2. Your exploratory testing charter for the new upload feature is scheduled for today and the feature enters regression scope tomorrow.
3. A product manager has asked for your view on whether a proposed acceptance criteria change is testable — the story is planned for the next sprint.
4. The nightly automation run shows a new, consistent failure in a low-risk report screen.

- A) 1, 2, 4, 3 — unblock the fix chain, keep the charter on schedule, triage the new failure, then advise on next sprint
- B) 2, 1, 4, 3 — protect your scheduled charter first
- C) 4, 1, 2, 3 — newest failure first
- D) 3, 1, 2, 4 — stakeholder requests take precedence

**Correct answer: A**

**Explanation:** Weigh urgency, impact, and dependency together. Item 1 leads on all three: a Severity 1 retest is high impact in itself, it has already waited a day, and — decisively — it blocks two further fixes, so delay multiplies downstream. Item 2 is genuinely time-sensitive (the feature enters regression scope tomorrow, so today is the right day for exploratory discovery) and comes next. Item 4 needs triage — a consistent new failure deserves a prompt look — but it sits in a low-risk screen and triage can be brief; it slots after the charter. Item 3 is important collaboration, but the story is next sprint's; a considered reply later today or tomorrow loses nothing. Option B protects your own schedule over a blocking Severity 1, inverting the dependency logic. Option C confuses novelty with priority. Option D confuses stakeholder seniority with urgency — managing stakeholder expectations sometimes means a brief "I'll reply properly tomorrow", which is itself good communication. The pattern to internalise: dependencies first, then hard time windows, then triage, then advice — impact-weighted urgency rather than any single dimension.

**Question 5 (moderate) — Deduction about test environments**

Your team has three environments: DEV (refreshed nightly, unstable), TEST (refreshed weekly, mirrors production configuration), and STAGE (refreshed on demand, production data snapshot, access-controlled). The agreed standard says: performance tests must run against production-like data; functional regression must run on a stable environment with production configuration; new feature testing may run anywhere except STAGE. Where must performance testing run, and where should functional regression run?

- A) Performance on STAGE; regression on TEST
- B) Performance on TEST; regression on DEV
- C) Performance on STAGE; regression on DEV
- D) Performance on DEV; regression on TEST

**Correct answer: A**

**Explanation:** Match each activity's requirements to each environment's properties. Performance testing requires production-like data; only STAGE holds a production data snapshot, so performance must run on STAGE. Functional regression requires stability plus production configuration: DEV is explicitly unstable, so it fails the stability requirement; TEST mirrors production configuration and its weekly refresh cadence makes it stable within a testing cycle — TEST is the fit. Option B puts performance on TEST, whose weekly-refresh data is not stated to be production-like, and regression on unstable DEV. This mapping exercise is your **Designing and executing tests** skill ("set up suitable environments") and your **Test engineering** understanding in miniature: environments are not interchangeable, and much wasted testing effort — and many false defects — come from running the right tests in the wrong place. In assessments, tabulate mentally: requirements on one axis, properties on the other, and accept only complete matches.

**Question 6 (moderate) — Pattern recognition in automated run history**

Your automated regression suite's pass rates over ten nightly runs: 98%, 97%, 98%, 84%, 98%, 97%, 83%, 98%, 85%, 97%. Investigation shows the low runs occurred on nights when the data refresh job overran into the test window. What is the most useful conclusion?

- A) The suite is unreliable and should be rewritten.
- B) The low pass rates reflect an environmental scheduling conflict, not product defects — the suite and the refresh job need sequencing, and low-run results should be treated as invalid rather than as quality signals.
- C) The product's quality fluctuates between 83% and 98%.
- D) Pass rates below 95% should trigger an automatic release block.

**Correct answer: B**

**Explanation:** The pattern is bimodal: runs cluster at 97-98% or 83-85%, with nothing between — and the low cluster correlates perfectly with the refresh job overrunning. That signature points to an environmental cause, not product regressions: when tests execute against an environment mid-refresh, they fail for reasons unrelated to code quality. The practical response is engineering, not rewriting: sequence the jobs so the refresh completes before the suite starts, and mark the affected runs invalid so they do not pollute trend data. Option A discards a suite that performs consistently when its environment is sound. Option C misreads infrastructure noise as product signal — a serious analytical error, because teams that believe it start distrusting their own quality data. Option D proposes a policy that would convert every scheduling clash into a release crisis. Distinguishing environmental failure from product failure is one of the most valuable diagnostic skills in test automation, central to supporting the maintenance of automated tests, and a direct application of analysing information to identify — and correctly classify — risks.

**Question 7 (moderate) — Logical deduction in defect triage**

Triage rules: (i) defects reproducible in production configuration are triaged within one working day; (ii) defects affecting payment amounts are always Severity 1; (iii) Severity 1 defects must have a named developer assigned before the daily stand-up. This morning you confirmed defect D-501 — incorrect rounding that understates payment amounts by pennies — reproduces in TEST, which mirrors production configuration. It is 09:00; stand-up is at 09:45. What do the rules require?

- A) D-501 must be triaged within one day, rated Severity 1, and have a named developer assigned before 09:45.
- B) D-501 can wait for tomorrow's triage because rounding errors are minor.
- C) D-501 is Severity 2 because the amounts are small.
- D) The rules conflict, so the test manager must decide.

**Correct answer: A**

**Explanation:** Apply each rule in turn and check for genuine conflict. Rule (i): TEST mirrors production configuration and the defect reproduces there, so the one-day triage clock applies. Rule (ii): the defect affects payment amounts — the rule says "always Severity 1" with no materiality threshold, so the penny size is irrelevant to classification: Severity 1. Rule (iii): as a Severity 1, it needs a named developer before stand-up — 09:45 today. All three obligations stack without conflict, so A follows and D is wrong. Options B and C both import a materiality judgement ("pennies are minor") that the rules deliberately exclude — and for good reason: rounding errors in payment systems scale across every transaction and can breach accuracy obligations regardless of individual size. The professional lesson sits alongside the logical one: when you critically assess defects, apply the agreed rules first, and if you believe a rule produces the wrong outcome, raise the rule for discussion — do not quietly waive it case by case.

**Question 8 (hard) — Multi-constraint test scheduling**

You must schedule four activities into a five-day window (Monday to Friday): smoke test the new build (S), run full regression (R), exploratory testing of the redesigned journey (E), and accessibility testing (A). Constraints: (i) S must complete before anything else starts; (ii) R takes two consecutive days; (iii) the accessibility specialist is available only Wednesday and Thursday; (iv) E must occur after R completes, because regression may change the build. S takes one day. On which days must R run?

- A) Monday and Tuesday
- B) Tuesday and Wednesday
- C) Wednesday and Thursday
- D) Thursday and Friday

**Correct answer: B**

**Explanation:** Chain the constraints. S occupies Monday (constraint i: everything else follows it). R needs two consecutive days starting Tuesday at the earliest. E must follow R's completion (constraint iv), so R cannot end on Friday — E would have no day. That eliminates Thursday–Friday (option D) and means R must end by Thursday, leaving R either Tuesday–Wednesday or Wednesday–Thursday. Now apply constraint (iii): accessibility testing needs Wednesday or Thursday. If R ran Wednesday–Thursday, then E must fall on Friday — but A also needs a slot, and its only available days (Wednesday, Thursday) would be consumed by R (note that A and R cannot sensibly share days if activities are exclusive, as the one-activity-per-day framing implies). With R on Tuesday–Wednesday, Thursday takes A (within the specialist's availability) and Friday takes E (after R completes). Every constraint is satisfied only by R on Tuesday and Wednesday. This is exactly the reasoning behind real test scheduling: specialist availability and dependency order interact, and the feasible plan often exists only if you sequence backwards from the tightest constraint — a discipline your **Test and quality planning** skill formalises when you create or adapt approaches within delivery timescales.

**Question 9 (hard) — Diagnosing an intermittent failure**

An automated checkout test fails roughly one run in five with "element not found: confirm-button". You gather: (i) the test always passes when run alone; (ii) failures occur only in the full suite run; (iii) the confirm button appears after a payment service call that takes 0.5 to 4 seconds; (iv) the test waits a fixed 2 seconds before clicking. What is the most likely cause?

- A) The confirm button is intermittently missing from the page — a product defect.
- B) The fixed 2-second wait is shorter than the payment call's worst-case response time, so the test intermittently looks for the button before it appears — a test design defect, likely worsened by system load during full suite runs.
- C) The test environment loses network connectivity one run in five.
- D) The element's identifier changes randomly.

**Correct answer: B**

**Explanation:** Reason from the evidence pattern. The button renders after a call taking 0.5 to 4 seconds (fact iii), but the test waits exactly 2 seconds (fact iv): whenever the call exceeds 2 seconds, the click fires too early and the element is genuinely absent at that moment. This explains the intermittency (response time varies), and facts (i) and (ii) explain the suite-only pattern: under full-suite load, the payment service responds more slowly, pushing more responses past the 2-second threshold; alone, it responds fast and the test passes. Options A, C and D each explain the failure but not the evidence pattern — a product defect or random identifier would also fail in isolated runs, and one-in-five connectivity loss would affect other tests too. The remedy is an explicit wait ("wait until element present, up to 10 seconds") rather than a fixed sleep — a cornerstone of reliable automation and exactly the kind of improvement your **Test engineering** skill supports. The transferable method: the best hypothesis explains every observation, including when the failure does not occur. Flaky tests erode a team's trust in its own safety net, so diagnosing them precisely is high-value work, not housekeeping.

**Question 10 (hard) — Risk-based coverage trade-off**

Two days of testing time remain before release; you cannot do everything. Remaining candidates: (1) regression of the payments module — no code changes this release, historically defect-prone, fully automated overnight; (2) manual testing of the new "change of circumstances" journey — new code, heavy business logic, used by 40% of service users; (3) cross-browser checks on the redesigned start page — cosmetic changes, high traffic, low harm if wrong; (4) retest of three fixed medium-severity defects in the documents section. Which allocation best aligns coverage with business risk?

- A) Trigger the automated payments regression overnight; spend the two manual days primarily on the new journey, with the defect retests fitted in; defer cross-browser checks or timebox them last.
- B) Spend both days on cross-browser checks — the start page has the highest traffic.
- C) Spend both days manually re-testing payments — it is historically defect-prone.
- D) Split the two days equally across all four items.

**Correct answer: A**

**Explanation:** Risk-based allocation weighs likelihood of defects, impact if wrong, and the cost profile of each option. Item 1 is high impact but low likelihood (no changes) and — decisively — nearly free: it is automated and runs overnight, consuming no manual days. Item 2 concentrates the release's risk: new code, complex logic, 40% of users — new, complex, heavily-used is the highest-likelihood, highest-impact combination, so it earns the bulk of scarce manual effort. Item 4 is obligatory in practice (unretested fixes are unverified changes) but small; it fits around item 2. Item 3 is low harm and cosmetic — a timebox at the end, or deferral with a noted risk, is proportionate. Option B chases traffic while ignoring harm and likelihood. Option C spends scarce manual effort duplicating free automated coverage of unchanged code. Option D — equal splitting — feels fair and is analytically indefensible: it allocates by item count rather than by risk, which is precisely what "ensure test coverage aligns with business risk" exists to prevent. Note the shape of the best answer: it uses cheap coverage everywhere it exists, concentrates expensive coverage where risk concentrates, and makes deferrals explicit rather than silent.

**Question 11 (hard) — Spotting the flawed inference in a quality report**

A draft report to stakeholders states: "Defect discovery has fallen for three consecutive sprints (28, 19, 11), demonstrating that product quality is steadily improving." Test execution data for the same sprints shows 410, 280, and 150 tests executed, as the team was progressively diverted to another programme. What is the strongest criticism of the report's claim?

- A) The defect counts are too small to mean anything.
- B) Falling defect discovery alongside sharply falling test execution may simply mean less testing was done, not that fewer defects exist — the discovery rate per test has actually stayed roughly constant, so the evidence for quality improvement is weak.
- C) The report should present percentages instead of counts.
- D) Three sprints is too short a period for any conclusion.

**Correct answer: B**

**Explanation:** Check the denominator before accepting a trend. Defects found per hundred tests executed: sprint one, 28 ÷ 410 ≈ 6.8; sprint two, 19 ÷ 280 ≈ 6.8; sprint three, 11 ÷ 150 ≈ 7.3. The discovery rate is flat — if anything, marginally rising. The falling raw counts are fully explained by falling test effort: the team looked less, so it found less. The report commits a classic denominator neglect error, and its conclusion — "quality is steadily improving" — could drive a premature release decision. Option B is the strongest criticism because it engages the actual data and shows the alternative explanation; options A and D gesture at rigour without analysis (three data points with a clear confound is a specific problem, not a generic small-sample complaint), and option C addresses presentation rather than validity. As the analyst on the team, this is your critique to make — clearly communicating risks to stakeholders includes protecting them from comforting but unsound readings of testing data, and doing it constructively: propose reporting defects per test executed alongside raw counts, so effort changes stay visible.

**Question 12 (hard) — Exploratory testing hypothesis selection**

During exploratory testing of a document upload feature, you observe: a 3MB PDF uploads successfully; a 6MB PDF fails with a timeout error rather than the expected "file too large" message (the stated limit is 5MB); a 3MB PNG fails with "unsupported format" although PNG is listed as supported. Which next test would be most informative?

- A) Upload the 3MB PDF again to confirm it still works.
- B) Upload a PNG of a different size and a PDF just under and just over 5MB, to separate the format problem from the size problem and locate the boundary behaviour precisely.
- C) Upload a 50MB video file to see what happens.
- D) Stop testing and raise a single defect titled "Upload broken".

**Correct answer: B**

**Explanation:** You have two distinct anomalies: size handling (over-limit files should get a clear rejection message, not a timeout) and format handling (a supported format is rejected). The most informative next tests are the ones that decouple the variables: a small PNG (say 1MB) tests format independent of size; PDFs at 4.9MB and 5.1MB test the boundary independent of format and reveal whether the limit is enforced at all, and how it fails. This is experimental design — vary one factor at a time — which is the analytical engine of good exploratory testing. Option A re-confirms what you already know, spending time to learn nothing. Option C jumps far past the boundary, where a failure would not tell you where behaviour changes. Option D abandons investigation and would produce exactly the kind of vague, unactionable defect report your defect management process exists to prevent: the eventual reports here should be two separate defects, each with precise reproduction conditions — separated causes, located boundaries. The transferable principle for assessments and for your craft: the best next test is the one whose outcome changes your understanding the most.

### Preparation tips

- **Practise on your own artefacts.** Ten minutes with a coverage matrix, a defect trend, or last night's automation summary — deliberately hunting for one inconsistency or one pattern — trains exactly what these assessments measure, and doubles as genuinely useful review of your project.
- **Name the technique as you use it.** When you answer a practice question, say to yourself "decision table", "boundary analysis", "vary one factor". Naming techniques builds the mental library that lets you select the right one quickly — the same selection skill your role applies when choosing test types and techniques.
- **Check every condition against every row.** Coverage and rule questions are lost to partial checking. Tick each rule off explicitly, especially rules with risk-dependent thresholds.
- **Train the "what changed?" reflex.** Most diagnostic questions — and most real test failures — yield to one question: what is different between the passing case and the failing case? Make it your first move.
- **Work the untimed practice items first, then simulate time pressure.** Accuracy first, pace second. When you do practise timed, use scrap paper and write intermediate conclusions down — working memory is the scarce resource.
- **Arrive rested and set up properly.** Quiet room, stable connection, scrap paper, water. Cognitive assessments measure your thinking at its best only if you let it operate at its best.
- **Ask about reasonable adjustments early** if you have a disability or condition affecting timed assessment — employers expect and welcome these conversations.

### Common pitfalls to avoid

- **Importing project knowledge into the question's world.** The question defines its own rules and environments. Reason only from what is stated — the same discipline as testing against the agreed requirement rather than your assumption of it.
- **Stopping at the first plausible answer.** Harder questions are built so that an early option survives a shallow check. Read all options; the correct one often differs only in a threshold, a scope, or a dependency.
- **Confusing correlation with cause.** Low pass rates on refresh nights, falling defect counts alongside falling effort — assessments and dashboards alike reward the reader who asks what else explains the pattern.
- **Prioritising by a single dimension.** Seniority, recency, or size alone are all traps; defensible sequences weigh impact, urgency, and dependency together. If your answer follows one simple rule, re-check it.
- **Losing minutes to a stubborn question.** Timed tests reward portfolio thinking: bank the answerable questions, return if time allows. This is coverage-versus-depth reasoning — you already practise it professionally.
- **Neglecting the denominator.** Any count offered as evidence — defects, failures, complaints — invites the question "out of how many?". Make it a reflex in tests, and in every quality report you read or write.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment measures how accurately and confidently you interpret and manipulate the kinds of numbers your role genuinely produces. It is not a mathematics exam: the operations rarely go beyond percentages, ratios, averages, rates, and reading tables and charts. What makes it demanding is context and precision — extracting the right figures from realistic data, choosing the right operation, and interpreting the result honestly.

The typical format is an online, timed test of 20 to 35 minutes with 15 to 20 questions, each presenting data — a results table, a trend chart, a defect summary — followed by a calculation or interpretation task. Calculators are usually permitted (confirm the instructions), rough paper is essential, and scoring reflects both accuracy and pace against a norm group. Some platforms adapt difficulty as you progress.

For a quality assurance test analyst, numeric fluency is a daily professional requirement, not an occasional extra. Testing produces a continuous stream of quantitative evidence: pass rates by suite and by sprint, defect discovery and closure rates, severity distributions, coverage percentages, automation run durations, environment availability figures. Your role turns that evidence into decisions and communications — you develop reports, you critically assess defects and risks, and you clearly communicate risks and the impact of defects to stakeholders. Every one of those duties has a numeric spine. When you tell a delivery manager "we're on track", that claim rests on execution rates versus remaining scope. When you argue that coverage aligns with business risk, you are implicitly comparing proportions. When you contribute to continuous improvement of testing approaches, the case for change is made with trend data — and undermined instantly if your arithmetic is wrong.

There is a second, subtler reason numeric reasoning matters at your level: you are often the person who protects the team from misleading numbers. Raw counts compared across different totals, trends quoted without denominators, averages distorted by outliers — these appear regularly in project reporting, and the analyst who can quietly recompute and gently correct them adds disproportionate value. The questions below therefore practise not only calculation but interpretation: what the numbers legitimately support, and what they do not. Work each one with pen and paper, show yourself every step, and sanity-check each result against the bounds the context implies.

### How this assessment maps to your role

The assessment dimensions map directly to the named skills in your role summary:

- **Percentages and rates** map to **Designing and executing tests** and your duty to execute tests, develop reports and record outcomes: pass rates, failure rates, coverage percentages and automation rates are the vocabulary of test reporting, and you must compute and verify them fluently.
- **Ratios and proportions** map to **Test and quality planning**: creating or adapting quality testing approaches based on risk involves proportional reasoning — how effort divides across risk levels, how defect find rates compare between test types, whether coverage depth tracks requirement criticality.
- **Averages, weighted calculations and rates over time** map to **Test engineering** and **Designing and executing tests**: suite durations, execution velocity, environment availability and automation throughput are the operational numbers behind setting up suitable environments and maintaining automated tests.
- **Trend interpretation** maps to **Managing, reporting and resolving defects**: critically assessing dependencies, defects and risks includes reading discovery and closure trends correctly, spotting denominators, and distinguishing genuine improvement from measurement artefacts.
- **Clear numeric communication** maps to **Communicating between the technical and non-technical**: managing differing stakeholder perspectives often comes down to presenting the same data honestly at the right level of detail — a skill that starts with getting the figures right.
- **Risk quantification** maps to **Test analysis**: analysing information to identify risks frequently means translating qualitative concerns into rough quantities — how many users affected, how often, at what cost — so they can be compared and prioritised.

### Practice questions

**Question 1 (easy) — Suite pass rate**

Last night's regression run executed 240 tests: 216 passed, 18 failed, and 6 were skipped due to a missing test data file. What was the pass rate of the executed tests (excluding skipped)?

- A) 90.0%
- B) 92.3%
- C) 91.5%
- D) 94.7%

**Correct answer: B**

**Explanation:** Read the definition carefully: the question asks for the pass rate of executed tests, excluding the skipped ones. Executed tests: 240 − 6 = 234. Pass rate: 216 ÷ 234 = 0.9231, so 92.3%. Option A (216 ÷ 240 = 90.0%) is the rate including skipped tests — a different, also legitimate metric, but not the one asked for. This distinction is not pedantic: skipped tests are neither passes nor failures, and how a team counts them changes its headline number by whole percentage points. When you develop reports, state which base you used ("92.3% of executed; 6 skipped due to data issue") so readers cannot misread the figure — and so the skipped tests, which represent a coverage gap, stay visible rather than vanishing into a denominator choice.

**Question 2 (easy) — Defect closure arithmetic**

At the start of the sprint, 34 defects were open. During the sprint, 21 new defects were raised, 27 were closed as fixed, and 4 were closed as duplicates or not-a-defect. How many defects remain open at sprint end?

- A) 24
- B) 28
- C) 31
- D) 20

**Correct answer: A**

**Explanation:** Track the flows into and out of the open pool. Opening balance: 34. Inflow: +21 raised. Outflow: −27 fixed and −4 closed for other reasons (duplicates and not-a-defect still leave the open pool). Calculation: 34 + 21 = 55; 55 − 27 = 28; 28 − 4 = 24. Option B forgets that duplicate/not-a-defect closures also reduce the open count — the most common slip, because "closed" gets mentally equated with "fixed". Option C subtracts only the 4, and option D double-counts an outflow. Balance arithmetic like this underpins every defect dashboard you will ever present; being able to reconcile the numbers ("do opening + raised − closed = closing?") is also how you catch tracking-tool hygiene problems, such as defects closed without a resolution category — a small data-quality habit that keeps your reporting trustworthy.

**Question 3 (easy) — Reading a severity distribution**

The open defect pool contains: Severity 1: 2 defects; Severity 2: 9; Severity 3: 24; Severity 4: 15. What percentage of open defects are Severity 1 or 2?

- A) 18%
- B) 22%
- C) 11%
- D) 26%

**Correct answer: B**

**Explanation:** Total open defects: 2 + 9 + 24 + 15 = 50. Severity 1 and 2 together: 2 + 9 = 11. Proportion: 11 ÷ 50 = 0.22 = 22%. Option C presents the raw count (11) as a percentage — always ask "out of what?". A quick mental verification: 50 is a convenient base, since every defect is worth 2 percentage points; 11 defects × 2 = 22%. Severity distribution percentages are a staple of release reporting because they compress the pool's risk profile into one line — "22% of our open defects are high severity" tells a stakeholder more than the raw list. But pair the percentage with the absolute numbers when you communicate: two Severity 1 defects can matter more than any percentage suggests, and clearly communicating the impact of defects means never letting a percentage hide a specific, serious problem.

**Question 4 (moderate) — Execution velocity and forecast**

Regression contains 360 test cases. After 3 days, your team of two testers has executed 135. A third tester of similar productivity joins from day 4. At the implied per-tester rate, how many more full days will the remaining tests take?

- A) 5 days
- B) 4 days
- C) 3.3 days, so 4 days in practice
- D) 3 days

**Correct answer: C**

**Explanation:** Find the per-tester daily rate first: 135 tests ÷ 3 days = 45 tests per day for two testers, so 45 ÷ 2 = 22.5 tests per tester per day. From day 4 there are three testers: 3 × 22.5 = 67.5 tests per day. Remaining work: 360 − 135 = 225 tests. Days required: 225 ÷ 67.5 = 3.33 days. Since the question asks for full days, that rounds up to 4 — you cannot report 3 days when a third of a day's work would remain. Option D takes the raw division and truncates it, promising an unachievable finish; option A ignores the third tester's arrival. Two professional notes travel with this calculation. First, always round effort forecasts up — schedules fail at the margins. Second, treat linear scaling as an approximation: a new joiner needs onboarding, some tests have dependencies, and defects interrupt execution, so a spoken forecast should be "about four days at current rates, assuming the new joiner ramps quickly". Forecasting execution honestly is a core input to the release conversations your reports feed.

**Question 5 (moderate) — Comparing defect find rates between test types**

This release, scripted regression consumed 12 tester-days and found 9 defects. Exploratory testing consumed 4 tester-days and found 11 defects. Which statement best compares their defect find rates?

- A) Scripted found 0.75 defects per tester-day; exploratory found 2.75 per tester-day — exploratory's find rate was over three and a half times higher this release.
- B) Scripted testing found fewer defects, so it should be abandoned.
- C) Exploratory found 2 more defects, a marginal difference.
- D) The comparison is impossible because the methods differ.

**Correct answer: A**

**Explanation:** Compute each rate: scripted, 9 ÷ 12 = 0.75 defects per tester-day; exploratory, 11 ÷ 4 = 2.75 defects per tester-day. Ratio: 2.75 ÷ 0.75 = 3.67 — exploratory found defects at over three and a half times the rate, per unit of effort. Option C compares raw counts and ignores the threefold difference in effort — denominator neglect again. Option D overcorrects: the methods do differ in purpose, which is why option B's conclusion is wrong (regression exists to protect existing behaviour, and its low find rate partly signifies success — stability), but effort-normalised find rates are still a legitimate, useful comparison. The mature reading, and the one worth offering when you contribute to continuous improvement of testing approaches: exploratory testing is earning its time richly this release, which supports allocating it more time or charter coverage — while regression's value is measured in confidence as well as defect counts. Numbers inform the judgement; they do not replace it.

**Question 6 (moderate) — Percentage change with direction**

Mean page response time in performance testing rose from 1.6 seconds in the last release to 2.0 seconds in this release candidate. The non-functional requirement states responses must stay under 2.5 seconds, and any release-on-release degradation above 20% must be escalated. What is the percentage change, and is escalation required?

- A) 20% increase — at the threshold, no escalation required
- B) 25% increase — escalation required
- C) 0.4% increase — no escalation
- D) 25% decrease — no escalation

**Correct answer: B**

**Explanation:** Percentage change = change ÷ original value × 100. Change: 2.0 − 1.6 = 0.4 seconds. Original: 1.6. So 0.4 ÷ 1.6 = 0.25 = a 25% increase. Since 25% exceeds the 20% degradation threshold, escalation is required — even though the absolute value (2.0s) still meets the 2.5s requirement. Option C mistakes the absolute change (0.4s) for a percentage; option A divides by the new value (0.4 ÷ 2.0 = 20%), the classic wrong-base error — percentage change always divides by the starting value. The two-threshold structure here is deliberately realistic: non-functional requirements often pair an absolute limit with a trend trigger, because a service can be inside its limit while degrading fast enough to breach it next release. Catching the trend breach now — and escalating per the agreed rule — is precisely the early risk mitigation your role level calls for: following appropriate standards to mitigate risk early.

**Question 7 (moderate) — Weighted average across suites**

Three automated suites ran last night: Suite A, 150 tests, 96% pass; Suite B, 50 tests, 88% pass; Suite C, 100 tests, 93% pass. What was the overall pass rate across all tests?

- A) 92.3%
- B) 93.7%
- C) 94.0%
- D) 95.0%

**Correct answer: B**

**Explanation:** You cannot average the three percentages directly (that gives (96 + 88 + 93) ÷ 3 = 92.3%, option A) because the suites differ in size — you must weight by test count. Convert each rate to passes: Suite A, 0.96 × 150 = 144; Suite B, 0.88 × 50 = 44; Suite C, 0.93 × 100 = 93. Total passes: 144 + 44 + 93 = 281. Total tests: 150 + 50 + 100 = 300. Overall rate: 281 ÷ 300 = 0.9367 = 93.7%. The unweighted average understates the true figure here because the weakest suite (B) is also the smallest — with different sizes the distortion can run either way, which is what makes the error dangerous: it is not conservatively biased. Weighted averages appear whenever you aggregate results across suites, sprints, or teams for a report; the reliable method is always the same — return to raw counts, sum, then divide once. If you remember one rule from this section: never average averages.

**Question 8 (moderate) — Test data volumes and ratios**

Your test data set must mirror production proportions. Production shows 3 standard applications for every 1 priority application. You need 240 application records in total for the performance test. How many should be priority applications, and how many standard?

- A) 60 priority, 180 standard
- B) 80 priority, 160 standard
- C) 40 priority, 200 standard
- D) 120 priority, 120 standard

**Correct answer: A**

**Explanation:** A ratio of 3 standard : 1 priority means 4 parts in total. Each part is 240 ÷ 4 = 60 records. Priority takes 1 part: 60. Standard takes 3 parts: 3 × 60 = 180. Verify: 60 + 180 = 240, and 180 ÷ 60 = 3 — the ratio holds. Option B misreads the ratio as 3:1 the other way after mis-dividing; option D ignores the ratio entirely. The professional context: representative test data matters because performance and behaviour often differ by record type — if priority applications trigger extra processing, a test set with the wrong mix will mislead on throughput and hide type-specific defects. Identifying and advocating for test needs, such as data, is an explicit part of your **Test analysis** skill, and being able to specify precisely — "we need 240 records at production's 3:1 mix: 180 standard, 60 priority" — turns a vague request into one an environment team can fulfil.

**Question 9 (hard) — Defect detection percentage across phases**

A release's defects were eventually counted as follows: 48 found in testing before release, and 12 found in production during the first month after release. What was the pre-release defect detection percentage? And if next release the team's stated goal is a detection percentage of at least 85% with production defects expected to stay at 12, how many defects would testing need to find?

- A) 80%; at least 68 defects
- B) 80%; at least 60 defects
- C) 75%; at least 51 defects
- D) 86%; goal already met

**Correct answer: A**

**Explanation:** Detection percentage = defects found before release ÷ total defects found × 100. Total: 48 + 12 = 60. Pre-release: 48 ÷ 60 = 0.80 = 80%. For the second part, let T be the number testing must find, with production defects at 12: the requirement is T ÷ (T + 12) ≥ 0.85. Solve step by step: T ≥ 0.85 × (T + 12); T ≥ 0.85T + 10.2; T − 0.85T ≥ 10.2; 0.15T ≥ 10.2; T ≥ 68. Testing would need to find at least 68 defects. Check: 68 ÷ (68 + 12) = 68 ÷ 80 = 85% exactly. Option B computes 85% of the old total (60), missing that finding more defects raises the total too — the moving-denominator subtlety that makes this question hard. A caveat worth carrying into real reporting: detection percentage is a lagging, imperfect metric (production defects surface over time, and finding more defects is not always possible if fewer exist), so treat targets like this as directional. Implementing ways to capture data that drives improvement of testing approaches is where your role meets metrics like this — use them with their caveats attached.

**Question 10 (hard) — Environment availability from downtime figures**

The TEST environment is scheduled for use 10 hours per working day, 5 days per week. Last week it suffered: one 3-hour outage during scheduled hours, one 90-minute deployment overrun during scheduled hours, and 4 hours of maintenance performed entirely outside scheduled hours. What was its availability as a percentage of scheduled hours?

- A) 83.0%
- B) 91.0%
- C) 87.0%
- D) 95.5%

**Correct answer: B**

**Explanation:** Scheduled hours: 10 × 5 = 50 hours. Downtime that counts is only downtime during scheduled hours: the 3-hour outage plus the 1.5-hour overrun = 4.5 hours. The 4 hours of out-of-hours maintenance does not reduce availability of scheduled time — including it (option A: (50 − 8.5) ÷ 50 = 83%) is the trap. Available time: 50 − 4.5 = 45.5 hours. Availability: 45.5 ÷ 50 = 0.91 = 91%. Environment availability is an operational number you will quote when advocating for test needs: if the environment is available only 91% of scheduled hours, roughly one hour in eleven of planned testing capacity is being lost, which compounds across a team — five testers lose about 22.5 tester-hours a week. Quantifying the loss like this is what converts a recurring frustration ("the environment keeps going down") into an evidenced case for investment — exactly how an analyst's numeric fluency turns into influence on **Test engineering** priorities.

**Question 11 (hard) — Reading a two-way table for risk analysis**

Defects from the last three releases, classified by component and by phase found:

| Component | Found in testing | Found in production |
|---|---|---|
| Applications | 30 | 2 |
| Payments | 18 | 6 |
| Documents | 24 | 2 |
| Notifications | 8 | 6 |

Which component shows the weakest pre-release detection, and therefore the strongest case for deeper test coverage?

- A) Payments — it has the most production defects
- B) Notifications — only 57% of its defects were caught before release, the lowest detection rate of any component
- C) Applications — it has the most defects overall
- D) Documents — its testing found many defects

**Correct answer: B**

**Explanation:** The question asks about detection weakness, which is a rate: found in testing ÷ total found, per component. Applications: 30 ÷ 32 = 94%. Payments: 18 ÷ 24 = 75%. Documents: 24 ÷ 26 = 92%. Notifications: 8 ÷ 14 = 57%. Notifications is the clear outlier: nearly half its defects escape to production, suggesting its test coverage misses the ways it really fails. Option A (Payments) ties on raw production count (6) but its stronger detection rate (75%) shows testing catches most Payments issues; note, though, that a fuller risk view would also weigh impact — payment failures may harm users more per defect, so Payments might still deserve attention on severity grounds even with a better rate. Options C and D misread high totals or high test finds as signals of weakness when they can equally signal thorough testing. The analytical habits here — compute rates per category, then layer impact on top — are exactly how you use defect patterns to ensure coverage aligns with business risk, and this two-way-table reading is among the most common hard-question formats in numeric assessments.

**Question 12 (hard) — Compound automation savings case**

Manual execution of the regression pack takes 40 tester-hours per release cycle, and the team runs 8 cycles per year. A proposal would automate 70% of the pack. Automated tests run unattended, but the automation requires an estimated 120 hours to build and 5 hours of maintenance per cycle. In the first year, how many tester-hours does the proposal save (or cost)?

- A) Saves 224 hours
- B) Saves 64 hours
- C) Costs 40 hours
- D) Saves 104 hours

**Correct answer: B**

**Explanation:** Build the year's ledger step by step. Current manual cost: 40 hours × 8 cycles = 320 hours per year. With 70% automated, manual execution drops to 30% of 40 = 12 hours per cycle, so 12 × 8 = 96 hours per year. Gross execution saving: 320 − 96 = 224 hours (option A stops here — the trap). Now subtract the automation's own costs in year one: build, 120 hours; maintenance, 5 × 8 = 40 hours; total 160 hours. Net first-year saving: 224 − 160 = 64 hours. Check option D: it forgets the maintenance (224 − 120 = 104). The shape of the answer matters as much as the number: year one nets +64 hours, but year two, with no build cost, nets 224 − 40 = 184 hours — automation investments typically pay back increasingly over time, provided maintenance stays controlled. Being able to construct this little business case is directly relevant to researching and trying new test types and techniques and to contributing to continuous improvement: proposals win support when their costs are counted as honestly as their savings.

### Preparation tips

- **Drill the four core operations until automatic.** Rate = part ÷ whole × 100; percentage change = change ÷ original × 100; weighted average = sum of raw counts ÷ total; ratio shares = total ÷ sum of parts. These four patterns cover the large majority of workplace numeric questions.
- **Always identify the denominator before calculating.** Executed or scheduled? Original or new value? Per suite or per test? Most wrong options in numeric tests are correct arithmetic on the wrong base.
- **Write the ledger.** For multi-step questions (savings cases, defect balances), list inflows and outflows on paper before computing. Structure prevents omissions — the same reason test scripts have numbered steps.
- **Verify by a second route.** Reconcile balances (opening + in − out = closing), recompute rates from raw counts, check ratio answers by dividing back. Agreement between routes is near-proof; disagreement is an early defect report on your own working.
- **Practise on live project data.** Recompute your team's dashboard figures occasionally — pass rates, closure rates, availability. It is the most realistic practice available, and now and then you will find a real reporting error, which is its own reward.
- **Mind the units.** Hours versus tester-hours, seconds versus milliseconds, per cycle versus per year. Convert once, at the end, and label every intermediate number as you write it.

### Common pitfalls to avoid

- **Averaging averages.** Percentages from different-sized groups cannot be averaged directly. Return to raw counts, always. This single error accounts for a remarkable share of wrong answers — and wrong dashboards.
- **Dividing by the wrong base in change calculations.** Percentage change divides by the original value. Rising 1.6 to 2.0 is +25%, not +20%. The wrong-base answer is nearly always among the options because it is nearly always the error people make.
- **Comparing counts when effort or size differs.** More defects found may mean more looking, not worse quality; fewer may mean less testing, not improvement. Normalise before comparing — per test, per tester-day, per component.
- **Stopping one step early.** Gross savings before costs, executed tests before the skip adjustment, 85% of the old total instead of the new one. Reread the question after calculating: which quantity was actually asked for?
- **Letting plausible numbers pass unchecked.** Availability above 100%, pass rates below 0%, forecasts shorter than the remaining work — impossible results mean a slipped step. Ten seconds of bounds-checking catches them.
- **Presenting percentages without absolutes (or vice versa).** In the test, answer what is asked; in your reports, give both — "91% availability (4.5 scheduled hours lost)" — so no reader is misled by either framing alone.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment measures how precisely you extract meaning, evaluate claims, and draw defensible conclusions from written material — using the document types your role genuinely handles: acceptance criteria, testing standards, policy extracts, release communications, defect discussions, and supplier documentation.

The typical format is an online, timed test of 15 to 25 minutes. You read a short passage and answer questions about it. The dominant format is **true / false / cannot say**: judged strictly against the passage, is each statement definitely true, definitely false, or undetermined? Supporting formats include best-summary questions, inference questions, and clear-writing judgement — choosing which phrasing communicates most effectively. Scoring is objective against a norm group and reflects accuracy and pace.

The discipline being measured is one you already exercise professionally: reading exactly. The golden rule — use only the passage, never outside knowledge — is the assessment version of testing against the agreed requirement rather than your recollection of it. A tester who reads "the system should respond within 2 seconds" and mentally files it as "the system responds fast" has already lost the boundary that testing needs; verbal reasoning tests punish exactly that softening, and practising them re-sharpens it.

For a quality assurance test analyst, the stakes of precise reading are concrete. Requirements and acceptance criteria are contracts written in natural language, and natural language leaks: qualifiers ("should", "must", "may"), scopes ("all", "each", "new users"), and conditions ("unless", "where applicable") carry the load-bearing meaning, and defects breed in the gaps between what a document says and what its readers assume. Your role analyses artefacts to determine what to test — a verbal task before it is a technical one. Equally, your role writes: defect reports that developers act on first time, risk communications that stakeholders correctly weigh, test summaries that survive being skimmed. The clear-writing questions in this section rehearse those judgements directly. And because you support and host discussions in a multidisciplinary team, and manage differing stakeholder perspectives, you regularly need to identify precisely what someone's written claim does and does not commit them to — a courtroom skill that verbal reasoning practice builds surprisingly well.

### How this assessment maps to your role

The assessment dimensions map directly to the named skills in your role summary:

- **Comprehension and extraction** map to **Test analysis**: determining what to test starts with extracting exactly what user stories, processes and designs state — including their conditions, scopes, and silences — and treating each as a distinct testable claim.
- **True / false / cannot say discipline** maps to **Designing and executing tests**: tests must verify stated requirements, not assumed ones; recognising "the document does not say" is the same act as spotting an acceptance criteria gap that needs a question raised before test design proceeds.
- **Inference judgement** maps to **Managing, reporting and resolving defects**: defect threads, developer replies and supplier responses require you to distinguish what has been stated, what is implied, and what remains open — misreading any of the three stalls resolution.
- **Argument evaluation** maps to **Test and quality planning** and **Test analysis** ("analyse information to identify risks"): proposals to change approaches, cut scope, or adopt tools arrive as written arguments; contributing to the development of strategy means testing the reasoning, not just the conclusion.
- **Clear-writing judgement** maps to **Communicating between the technical and non-technical**: communicating effectively with technical and non-technical stakeholders — and advocating for the team externally — depends on choosing phrasing that is specific, plain, and impossible to misread.

### Practice questions

For questions 1 to 6, read the passage, then judge each statement as **True** (the passage states it or it follows necessarily), **False** (the passage contradicts it), or **Cannot say** (the passage provides insufficient information).

**Passage 1:**

> Release readiness policy, section 4: A release candidate may proceed to production only when all Severity 1 and Severity 2 defects are resolved or formally waived by the service owner. Severity 3 and 4 defects do not block release but must be logged with a target fix release. Regression testing must be completed on the final build; where only configuration has changed since the last full regression, a documented smoke test of affected areas may be substituted with the test manager's approval. Accessibility testing must be completed for any release that changes user-facing screens.

**Question 1 (easy) — True / false / cannot say**

Statement: "A release candidate with an unresolved, unwaived Severity 2 defect may not proceed to production."

- A) True
- B) False
- C) Cannot say
- D) True only if the defect is also Severity 1

**Correct answer: A**

**Explanation:** The policy states that release may proceed "only when all Severity 1 and Severity 2 defects are resolved or formally waived". An unresolved, unwaived Severity 2 defect means that condition is unmet, so the candidate may not proceed — the statement follows necessarily and is True. Note the logical form: "only when X" makes X a necessary condition, so not-X blocks the outcome. Option D misreads severity levels as cumulative. The professional parallel is exact: policies gate releases through necessary conditions, and part of your role in release conversations is holding the line on what the policy's words actually require — including knowing that the waiver route exists and who owns it (the service owner, not the test team), which is precisely the kind of governance detail that clear reading extracts and hallway summaries lose.

**Question 2 (easy) — True / false / cannot say**

Statement: "Severity 3 defects must be fixed before the next release."

- A) True
- B) False
- C) Cannot say
- D) True, if the service owner requires it

**Correct answer: B**

**Explanation:** The policy says Severity 3 and 4 defects "must be logged with a target fix release" — a target must be recorded, but nothing requires that target to be the next release, and nothing requires the fix to happen before it. The statement converts "logged with a target" into "fixed by next release", a strengthening the passage contradicts in substance: the policy's explicit design is that these defects do not block and are scheduled flexibly. This is False rather than Cannot say because the statement claims an obligation ("must be fixed before the next release") whereas the policy explicitly assigns these defects a different, weaker obligation — the passage's scheme is incompatible with the claimed rule. Watch this pattern: readers routinely inflate logging or tracking obligations into fixing obligations. In your defect management work, keeping those categories distinct is what makes commitments to stakeholders accurate — "it is logged with a target of release 2.6" is a different promise from "it will be fixed next release".

**Question 3 (moderate) — True / false / cannot say**

Statement: "A release that changes only backend configuration, with no user-facing screen changes, requires accessibility testing."

- A) True
- B) False
- C) Cannot say
- D) True, because accessibility always applies

**Correct answer: B**

**Explanation:** The policy requires accessibility testing "for any release that changes user-facing screens". A release changing only backend configuration, with no user-facing screen changes, falls outside that trigger, so the policy does not require accessibility testing for it — the statement contradicts the policy's scope and is False. Be precise about what is being judged: the question asks what this policy requires, not what good practice might recommend; option D appeals to a general principle the passage does not state, which is exactly the outside-knowledge reflex the assessment penalises. Notice also the scope word doing the work: "any release that changes user-facing screens" defines the trigger exhaustively for this obligation. Reading triggers and scopes precisely is how you determine, in real release planning, which standards apply to which release — misreading them in either direction wastes effort or leaks risk, and both failures start with a blurred reading of one sentence.

**Passage 2:**

> Email from the delivery manager: "Team — the supplier has confirmed that version 3.2 of the case management API will be deployed to our TEST environment on Tuesday 9 September. Version 3.2 changes the response format of the search endpoint; the supplier states that all other endpoints are unchanged. Our own regression pack currently includes 14 automated tests that call the search endpoint. Until those tests are updated, they will fail against 3.2 and the nightly run results for the affected suite should be read accordingly. Priya will update the 14 tests; she estimates completion by Friday 12 September. Please do not raise defects for search-endpoint failures between Tuesday and Priya's confirmation that updates are complete."

**Question 4 (moderate) — True / false / cannot say**

Statement: "Between 9 September and Priya's confirmation, any nightly failure in the 14 search-endpoint tests should be assumed to be a product defect."

- A) True
- B) False
- C) Cannot say
- D) True, once Friday has passed

**Correct answer: B**

**Explanation:** The email states the opposite: until the tests are updated, they will fail against 3.2 because of the response format change, results should be "read accordingly", and defects should not be raised for search-endpoint failures in that window. The statement inverts the instruction, so it is False. Option D is tempting but wrong on the passage's own terms: the window ends at "Priya's confirmation that updates are complete", not at Friday — Friday is an estimate, and the email deliberately anchors the boundary to confirmation, not the calendar. That distinction — estimate versus completion signal — is one experienced analysts read carefully, because acting on the estimate ("it's past Friday, failures must be real now") reintroduces exactly the false-defect noise the instruction was designed to prevent. The underlying practice here is one your **Test engineering** awareness recognises: known incompatibility windows require expected-failure handling, and disciplined teams document them precisely so the test record stays interpretable.

**Question 5 (moderate) — True / false / cannot say**

Statement: "Version 3.2 will change the response format of at least one endpoint other than search."

- A) True
- B) False
- C) Cannot say
- D) False, because the supplier guaranteed it

**Correct answer: C**

**Explanation:** Careful: the email says the supplier "states that all other endpoints are unchanged". If we accepted the supplier's statement as established fact, the statement would be False. But the passage does not assert the other endpoints are unchanged — it reports the supplier's claim ("the supplier states..."), which is attributed information, one step removed from fact. The delivery manager has told us what the supplier says, not vouched for its truth. Judged strictly, the passage leaves open whether the supplier's claim is accurate, so whether some other endpoint's format changes is undetermined: Cannot say. Option D shows the error explicitly — "guaranteed" appears nowhere. This attribution distinction ("X states that Y" versus "Y") is a genuinely important professional reading skill: supplier claims about unchanged behaviour are exactly the claims experienced testers verify rather than inherit — a light regression pass across "unchanged" endpoints is standard caution. The assessment version and the workplace version of this judgement are the same act: noticing who is asserting what, and how far the evidence actually extends.

**Question 6 (moderate) — True / false / cannot say**

Statement: "Priya estimated that the test updates would be complete by 12 September."

- A) True
- B) False
- C) Cannot say
- D) False — the delivery manager made the estimate

**Correct answer: A**

**Explanation:** The email says: "Priya will update the 14 tests; she estimates completion by Friday 12 September." The statement matches, with the estimate correctly attributed to Priya ("she estimates") and correctly framed as an estimate rather than a commitment. This is True on a direct reading. The value of an easy attribution question after the previous hard one is the contrast: here the passage does assign the estimate to Priya explicitly, so option D fails against the text. In assessments, resist momentum — having just answered a question where attribution created uncertainty, do not carry that suspicion into a sentence whose attribution is plain. Each statement is judged fresh against the passage. The workplace analogue is treating each document, and each claim within it, on its own words: pattern-based suspicion is a useful prompt for checking, never a substitute for it.

**Question 7 (moderate) — Best summary of a standards extract**

Read this extract from a testing standards document:

> Non-functional testing shall be planned with the same rigour as functional testing. Performance, security, and accessibility requirements shall be defined in measurable terms before build begins, and each shall have named test activities in the test plan. Where a non-functional requirement cannot be tested before release — for example, behaviour under full production load — the plan shall state how the risk will be monitored and controlled after release. The absence of measurable non-functional requirements shall be raised as a project risk, not resolved by omitting the testing.

Which option best summarises the extract?

- A) Non-functional testing is less important than functional testing but should still happen.
- B) Non-functional requirements must be measurable, planned, and tested with equal rigour; where pre-release testing is impossible, post-release monitoring must be planned; and missing measurable requirements are a risk to escalate, not a reason to skip testing.
- C) Performance testing should be done under full production load.
- D) Projects without measurable non-functional requirements should not proceed to build.

**Correct answer: B**

**Explanation:** Map the extract's four sentences: equal rigour; measurable requirements with named activities defined before build; a monitoring-and-control plan where pre-release testing is impossible; and missing requirements escalated as risk rather than answered with omission. Option B captures all four commitments at the right strength. Option A contradicts the first sentence's "same rigour". Option C inflates an example (production load as a case where pre-release testing may be impossible) into a requirement the extract never makes. Option D overshoots the fourth sentence: the extract says raise a risk, not halt the project — summary questions frequently hide the wrong answers in these strength miscalibrations, stronger or weaker than the text. The mapped skill is direct: working with stakeholders to determine which functional and non-functional quality characteristics add value requires you to know what standards actually oblige, at their actual strength — and to quote them accurately when advocating for non-functional test needs that schedules squeeze.

**Question 8 (moderate) — Inference from a defect thread**

A defect thread reads — Analyst: "Submitting the form with an apostrophe in the surname field (O'Brien) returns error 500." Developer, two hours later: "Confirmed, reproduced on TEST. This looks like it affects every free-text field, not just surname. Fix will need the shared input-handling library, which the platform team owns. I've raised it with them and linked their ticket." Which conclusion is best supported?

- A) The defect is fixed.
- B) The defect is confirmed, is broader than originally reported, and its fix depends on a team outside the immediate one — so resolution timing now involves a cross-team dependency.
- C) The platform team caused the defect deliberately.
- D) The analyst's report was wrong, since the problem is not really about surnames.

**Correct answer: B**

**Explanation:** Extract what the thread establishes: reproduction is confirmed; the developer's investigation suggests wider scope (every free-text field); the fix sits in a shared library owned by the platform team; a dependency ticket exists and is linked. Option B assembles exactly these facts and draws the one inference they support — resolution now runs through a cross-team dependency, with the timing implications that carries. Option A confuses "raised with the owning team" with "fixed". Option D misunderstands how good reports work: the analyst reported a precise, reproducible instance, and precise instances are what enable developers to generalise — the report was not wrong; it was the thread's foundation. Option C invents motive from nothing. Professionally, this is the moment your **Managing, reporting and resolving defects** skill turns to dependency management: critically assessing dependencies, updating the defect's severity assessment given the wider scope (every free-text field raises user impact), and communicating the revised risk and its cross-team timing to stakeholders — inference first, then action on exactly what the inference supports.

**Question 9 (hard) — Clear-writing judgement for a risk communication**

The release meeting needs one sentence summarising a testing risk for a mixed technical and non-technical audience. The situation: performance testing could not be completed because the STAGE environment was unavailable for four of five scheduled days; functional results are good; the service expects a seasonal peak in six weeks. Which sentence communicates the risk most effectively?

- A) "Owing to environmental non-availability, the non-functional validation baseline remains unestablished pending remediation of infrastructure constraints."
- B) "Testing went well overall, though we had some environment issues worth mentioning."
- C) "Functional testing passed, but performance testing could not be completed because the test environment was unavailable for four of the five scheduled days — so we cannot yet say whether the service will handle the seasonal peak expected in six weeks, and we recommend completing performance testing before then."
- D) "The environment team's failures have made proper testing impossible and the release is at risk."

**Correct answer: C**

**Explanation:** Judge each sentence against what a risk communication must do: state what is known, what is not known, why it matters, and what should happen next — in language every attendee can act on. Option C does all four: the good news is bounded ("functional testing passed"), the gap is specific and quantified (four of five days), the consequence is tied to a real business event (the seasonal peak), and a recommendation follows. Option A is jargon-dense and hides both the cause and the consequence — technical-sounding vagueness is the most common failure in risk reporting, and audiences correctly read it as evasion. Option B softens the risk into a pleasantry, transferring the interpretive burden ("worth mentioning") to listeners who lack the context to weigh it. Option D communicates blame, not risk: it assigns fault ("the environment team's failures"), inflames the cross-team relationship your role is supposed to manage, and still never says what the actual exposure is. Your skill in communicating between the technical and non-technical — and managing differing stakeholder perspectives — is largely built from sentences like option C: concrete, balanced, consequence-linked, and pointed at a decision.

**Question 10 (hard) — True / false / cannot say with layered conditions**

Read this extract from a data handling standard:

> Test environments must not contain unmasked production personal data. Masked production data may be used in TEST and STAGE where the masking method has been approved by the data protection team within the last twelve months. Synthetic data may be used in any environment without approval. Where a defect can only be reproduced with a specific production record, a time-limited exemption may be granted by the data protection team; such exemptions must be logged, must name the individuals with access, and expire after a maximum of ten working days.

Statement: "A tester who needs a specific production record to reproduce a defect may use it in TEST for up to ten working days, provided the exemption is logged and names those with access."

- A) True
- B) False
- C) Cannot say
- D) True, provided the record is masked

**Correct answer: B**

**Explanation:** Compare the statement's conditions with the standard's, clause by clause. The standard's exemption route requires: (1) the defect can only be reproduced with the specific record; (2) an exemption is granted by the data protection team; (3) it is logged; (4) it names individuals with access; (5) it expires within ten working days. The statement includes need (1), logging (3), naming (4), and the time limit (5) — but omits condition (2): the grant. As written, the statement says the tester "may use it... provided the exemption is logged and names those with access", presenting logging and naming as sufficient. The standard makes the data protection team's grant the gateway; logging and naming are obligations attached to a granted exemption, not substitutes for it. Because the statement asserts a permission under weaker conditions than the standard allows, the standard contradicts it: False. Option D confuses the two routes — masking is the separate, approval-based route for general use, while the exemption route exists precisely for unmasked specific records. Reading layered conditions without dropping one is exactly the skill that keeps your test data practices compliant — and it is the single most common way hard verbal questions are constructed: one omitted condition inside an otherwise faithful paraphrase.

**Question 11 (hard) — Evaluating a written proposal**

A tool vendor's written case states: "Teams using our AI test-generation platform report finding 40% more defects in their first quarter of use. Your regression coverage will therefore increase by 40%, and manual test design will no longer be needed. Leading government departments already rely on us." Which is the strongest critical reading?

- A) The claims chain together weakly: "defects found by new users" does not translate to "coverage increase" (different measures, and new-tool quarters involve unusual attention); "no longer needed" does not follow from any cited evidence; and "leading departments rely on us" is unverifiable social proof — so the case needs independent evaluation against your own baseline.
- B) The proposal is convincing because 40% is a large number.
- C) AI tools cannot generate tests, so the claims are false.
- D) The proposal should be rejected because it comes from a vendor.

**Correct answer: A**

**Explanation:** Take the argument apart claim by claim. First claim: users "report finding 40% more defects" — self-reported, first-quarter figures carry known distortions (novelty attention, backlog clearance, selection of successful customers). Second claim: the leap from "more defects found" to "coverage will increase 40%" changes the metric mid-argument — defect counts and coverage are different quantities, and the word "therefore" is doing illegitimate work. Third claim: "manual test design will no longer be needed" is supported by nothing cited. Fourth: named-free social proof cannot be checked. Option A catches all four moves and — importantly — ends at the professionally correct conclusion: not rejection, but independent evaluation against your own baseline, which is precisely what your role's "research and try new test types and techniques" means in practice: structured trials, your own metrics, defined success criteria. Options C and D are reverse errors — dismissing by category (technology or source) is as unanalytical as accepting by enthusiasm, and option D would also discard genuinely useful tools. Written cases like this cross your desk regularly; the analyst who can annotate exactly where an argument's chain slips — metric switches, unsupported leaps, unverifiable proof — contributes to tooling decisions far beyond their grade.

**Question 12 (hard) — Reconciling three documents**

Three artefacts describe the same journey. The user story: "Users can save a draft application and resume within 30 days; after 30 days, drafts are deleted and the user is notified by email before deletion." The API specification: "Draft retention: 30 days. Deletion job runs nightly. No notification endpoints defined in this version." The prototype's screen text: "We'll keep your draft for one month and email you a reminder a week before we delete it." As the analyst determining what to test, which is the most accurate assessment of the discrepancies?

- A) The artefacts agree in substance; "30 days" and "one month" are the same thing.
- B) There are two substantive discrepancies: the notification promised in the story and prototype has no supporting API capability in this version, and the prototype's specific "a week before" commitment appears nowhere else; additionally "one month" and "30 days" are not always equal, which matters for boundary testing.
- C) The API specification is wrong and should be corrected.
- D) Only the missing notification endpoint matters; the rest is cosmetic.

**Correct answer: B**

**Explanation:** Reconcile claim by claim. Retention: story and API say 30 days; the prototype says "one month" — usually intended as equivalent, but months run 28 to 31 days, so the copy and the system can diverge by up to a day; a genuine boundary-testing consideration and user-comprehension point, not mere pedantry. Notification: the story requires an email before deletion, the prototype promises one with a specific timing ("a week before"), yet the API version defines no notification endpoints — a substantive gap between promised behaviour and available capability; either the promise is undeliverable this version, or delivery depends on some mechanism outside this specification, which must be established before test design. Timing: "a week before" exists only in the prototype — an escalation of the story's unspecified "before deletion", needing a decision on which is authoritative. Option A waves through both the gap and the boundary. Option C decides unilaterally which artefact is wrong — analysis identifies conflicts; the product owner arbitrates authority. Option D dismisses commitments made to users as cosmetic; screen text is a promise, and testing whether the service keeps its promises is much of what quality means. This three-way reconciliation — enumerate claims, difference them, route each discrepancy to a decision — is your **Test analysis** skill performed at full fidelity, and precisely the work that ensures what you test is what was actually agreed.

### Preparation tips

- **Practise the three-way judgement on live documents.** Take a policy, standard or story from your project and write one statement it makes true, one it makes false, and one it leaves undetermined. Daily five-minute reps build the core discrimination faster than any question bank.
- **Underline the load-bearing words.** Qualifiers (must/should/may), scopes (all/each/only/new), conditions (unless/where/provided), and attributions (X states that...) carry the meaning. Train your eye to snag on them — in tests and in acceptance criteria alike.
- **Judge statements against the text, not against each other.** Each question is a fresh comparison with the passage. Momentum errors — carrying suspicion or confidence from the previous question — are a quiet mark-loser.
- **Count the conditions.** Hard questions omit one clause from an otherwise faithful paraphrase. When a statement paraphrases a rule, list the rule's conditions on scrap paper and tick them off against the statement.
- **Summarise structure, not sentences.** For best-summary questions, note what each sentence of the passage does (obliges, permits, excepts, escalates). The right summary preserves every move at its original strength.
- **Read your own reports as an assessor would.** Once a week, reread a defect report or risk summary you wrote and ask: could a reader honestly mark any claim in it "cannot say"? Rewriting to close those gaps trains both directions of the skill at once.

### Common pitfalls to avoid

- **Importing professional knowledge.** You know how releases usually work; the passage defines how this one works. The strongest candidates in verbal tests are conspicuously obedient to the text — the same obedience you owe the agreed requirement when designing tests.
- **Blurring "reported" with "asserted".** "The supplier states the endpoints are unchanged" is evidence about the supplier's claim, not about the endpoints. Attribution phrases are the most commonly missed signal in hard questions and in real supplier correspondence alike.
- **Inflating obligations.** "Logged with a target release" is not "will be fixed next release"; "raise as a risk" is not "halt the project". Match the strength of the verb, not the vibe of the sentence.
- **Confusing False with Cannot say.** False requires contradiction; silence yields Cannot say. Before answering False, point to the clause that actively conflicts with the statement.
- **Choosing confident-sounding writing over clear writing.** In clear-writing questions, jargon density and assertiveness are distractors; the correct option states facts, bounds, consequence and next step plainly. Apply the same test to your own release-meeting sentences.
- **Resolving discrepancies instead of reporting them.** When artefacts conflict, the analytical task is to enumerate the conflicts and route them for decision — options that quietly pick a winner ("the spec is wrong") are penalised in tests and cause rework in projects.

## Workplace job-specific situational judgement assessment

### About this assessment

A situational judgement assessment (SJT) presents realistic workplace scenarios and asks you to judge the effectiveness of different responses. Where the other assessments measure how you think about artefacts and data, this one measures how you act among people: how you balance honesty, user focus, collaboration, ownership, and escalation when the situation is awkward and more than one response looks defensible.

The typical format is an online assessment of 20 to 40 minutes containing 10 to 20 scenarios, each followed by four or five possible responses. Common question styles: choose the most effective response; choose the least effective; choose both; or rate every response on an effectiveness scale. Scoring compares your judgements against those of experienced professionals and against the behaviours the employer values — in UK government digital and data roles, that typically means user focus, honesty about problems, collaboration across disciplines, taking ownership, escalating appropriately, and treating colleagues inclusively.

For a quality assurance test analyst at your level, the scenarios concentrate on the genuinely hard parts of the job — which are rarely technical. You work at the centre of a multidisciplinary team, and your role explicitly includes supporting and hosting discussions with potentially difficult dynamics, managing differing stakeholder perspectives, and advocating for the team externally. Testing also occupies a structurally awkward position: you are the person whose job is to find problems in colleagues' work and to tell truths that complicate schedules. Handled poorly, that position breeds friction; handled well, it makes you one of the most trusted people on the team. SJTs probe exactly that handling: the defect that arrives at the worst possible moment, the developer who disagrees with your severity rating, the delivery pressure that leans on your independence, the junior colleague whose work needs correcting, the stakeholder who wants a cheerier summary than the evidence supports.

A useful orientation before you begin: SJT questions at mid level test independent judgement within your remit. You are expected to resolve peer-level friction directly and professionally, to keep decision-owners informed rather than deciding for them, and to escalate on substance, not on frustration. Responses that quietly absorb problems score poorly; so do responses that dramatically escalate what a direct conversation would fix. The consistently high-scoring pattern is: engage honestly, at the right level, with the right person, keeping users and evidence at the centre.

### How this assessment maps to your role

The assessment dimensions map directly to the named skills in your role summary:

- **Honest reporting under pressure** maps to **Managing, reporting and resolving defects**: clearly communicating risks and the impact of defects to stakeholders — especially when the message is unwelcome — is the behaviour SJTs most reliably reward, and the one your role most depends on.
- **Managing disagreement** maps to **Communicating between the technical and non-technical**: supporting and hosting discussions with difficult dynamics, and managing differing stakeholder perspectives, appear in scenario form as severity disputes, scope arguments, and cross-team friction.
- **Appropriate escalation** maps to **Managing, reporting and resolving defects** and **Test and quality planning**: contributing to mitigation and contingency plans means knowing which problems you resolve, which you raise, and which you hand to the decision-owner with clear options.
- **User focus** maps to **Test analysis**: working with stakeholders to determine which quality characteristics add value keeps the citizen at the centre; in SJT scenarios, the option that protects users usually outranks the option that protects the schedule or anyone's comfort.
- **Improving practice constructively** maps to **Test and quality planning** ("contribute to continuous improvement") and **Designing and executing tests** ("research and try new test types and techniques"): scenarios about flawed processes reward evidence-based suggestions through the team's own channels.
- **Supporting colleagues** maps to your role's collaborative core: helping others test well, correcting mistakes without humiliation, and advocating for the team externally are recurring scenario themes.

### Practice questions

**Question 1 (easy) — Severity disagreement with a developer**

You rated a defect Severity 2: the postcode lookup fails for around 5% of addresses, forcing those users to enter addresses manually. A developer changes it to Severity 4 with the comment "manual entry works fine — cosmetic". You believe the rating understates real user impact, particularly for users with low digital confidence. What is the most effective response?

- A) Change it back to Severity 2 without comment.
- B) Reply on the defect with your reasoning — the affected proportion, the user impact of forced manual entry, and the service's user demographics — and propose discussing it at triage if the developer still disagrees.
- C) Accept the change — developers understand the system better.
- D) Email the delivery manager that the developer is downgrading defects.

**Correct answer: B**

**Explanation:** Severity is a judgement about user impact, and disagreements about it are best settled with evidence in the open, at the forum that owns the decision. Option B does three things well: it puts your reasoning on the record where future readers of the defect will find it; it engages the developer's claim on its merits (manual entry "works", but forcing it on 5% of users is a real degradation, heaviest for the least confident users); and it routes persistent disagreement to triage — the team's mechanism — rather than into a private contest. Option A starts an edit war that settles nothing and sours the relationship. Option C defers on a question that is not primarily technical: developers know the system; user impact assessment is your professional ground. Option D escalates before attempting resolution and frames a legitimate disagreement as misconduct. The behaviours mapped here: managing differing perspectives with evidence, keeping the defect record honest, and using team decision structures — the exact texture of hosting difficult discussions well.

**Question 2 (easy) — Release pressure on your test summary**

The delivery manager, preparing for the release board, says: "Your summary says 'two high-severity defects open, release not recommended'. Can you soften that? Maybe 'minor issues outstanding'? The board reacts badly to negative summaries." What is the most effective response?

- A) Soften the wording — the delivery manager owns the release message.
- B) Refuse and send your summary directly to the board yourself first.
- C) Keep the factual content accurate, and offer to reframe constructively: state the two defects and their user impact precisely, alongside what has passed, the mitigation options, and what would change your recommendation — but decline to describe high-severity defects as minor.
- D) Say nothing and quietly change the summary back after the meeting.

**Correct answer: C**

**Explanation:** Separate the legitimate request from the illegitimate one. Framing is negotiable: a summary can be constructive, balanced, and decision-focused — leading with what passed, presenting the defects with impact and options, and stating what would flip your recommendation. Accuracy is not negotiable: "minor issues outstanding" is a factual misdescription of high-severity defects, and a board that acts on it is making a decision on corrupted information — the precise failure your role exists to prevent. Option C gives the delivery manager real help with their genuine problem (how the message lands) while holding the line on truth. Option A abandons the line; if the defects surface in production, the record shows testing called them minor. Option B treats a framing request as an act of war — bypassing the delivery manager damages the relationship your advocacy depends on, and is rarely justified before a refusal to transmit accurate information has actually happened. Option D is passive deception in both directions. Clearly communicating risks to stakeholders sometimes means exactly this: help with the how, never with the what.

**Question 3 (easy) — A colleague's flawed test design**

A newer analyst on your team shares their test cases for a feature you know well. The cases cover happy paths thoroughly but omit negative testing and boundary values almost entirely. They seem proud of the work. What is the most effective response?

- A) Rewrite the test cases yourself tonight so the coverage is right.
- B) Approve them — pointing out gaps might discourage a newer colleague.
- C) Acknowledge the solid happy-path coverage, then walk through one or two concrete examples together ("what happens if the date field gets 31/02?"), helping them discover the gap and extend the cases themselves.
- D) Tell their line manager the work is not up to standard.

**Correct answer: C**

**Explanation:** The goal is three-fold: the coverage gets fixed, the colleague gets better, and the relationship gets stronger — and option C achieves all three. Leading with genuine acknowledgement keeps the conversation open; teaching through a concrete example ("what happens if...?") lets them find the gap themselves, which builds skill rather than dependence; and leaving the extension work with them preserves their ownership. Option A fixes today's coverage while teaching nothing and quietly signalling distrust — and it does not scale. Option B is the worst kind of kindness: the gaps ship, defects reach users, and the colleague eventually learns their early work was silently considered inadequate — discouragement deferred and compounded. Option D escalates a routine development conversation into a performance report; managers are for patterns, not first instances. This is the collaborative core of your role in miniature: quality is a team outcome, and the analyst who upgrades colleagues' testing multiplies their own impact. Peer feedback delivered as curiosity rather than verdict is the mechanism.

**Question 4 (moderate) — Discovering the automation has been silently failing**

Investigating an unrelated issue, you discover that a regression suite covering the payments module has been reporting "pass" for three weeks while actually executing zero tests — a configuration change made the suite exit early with a success code. Two releases have shipped in that window on the strength of green dashboards. What is the most effective response?

- A) Fix the configuration quietly — no need to alarm anyone about the past runs, since nothing bad seems to have happened.
- B) Fix the configuration, then immediately inform the team and delivery manager: the payments module has effectively been unregressed for three weeks across two releases, recommend a targeted regression pass on the current production version, and propose a run-validity check (minimum executed-test count) so silent failure cannot recur.
- C) Raise a defect against the person who made the configuration change.
- D) Report it at the retrospective in two weeks.

**Correct answer: B**

**Explanation:** Work through what the discovery actually means: the green dashboard was false evidence, so two releases shipped with less verification than everyone believed — the risk is live in production right now, not historical. Option B addresses all three time horizons: fix (stop the ongoing gap), disclose and remediate (the team must know its real position, and a targeted regression of production closes the open exposure), and prevent (a minimum-executed-count check turns this failure mode into a detectable one — a classic **Test engineering** improvement). Option A is the seductive trap: "nothing bad seems to have happened" is exactly what unverified systems look like — absence of evidence, not evidence of absence, and concealing a known verification gap makes you personally the owner of the next payments incident. Option C converts a systems failure into a blame exercise; the configuration slipped through because no validity check existed, and the person-focused response guarantees the next person hides their mistake. Option D sits on live risk for two weeks. The behaviours mapped: ownership of unwelcome truths, prompt risk communication to decision-owners, blameless systemic improvement — mitigation and contingency thinking under real pressure.

**Question 5 (moderate) — The product manager wants to skip exploratory testing**

Sprint planning is tight. The product manager proposes: "The new eligibility checker is well covered by the automated acceptance tests we wrote from the criteria — let's drop the exploratory session and bank the day." You know the checker encodes complex policy logic with many interacting conditions. What is the most effective response?

- A) Agree — acceptance tests derived from the criteria define done, and done is done.
- B) Explain the distinct value at stake: acceptance tests verify the behaviour we anticipated, while exploratory testing probes the interactions and edge conditions nobody wrote down — precisely where complex eligibility logic fails; propose a timeboxed session focused on condition interactions, and accept the team's informed decision.
- C) Insist that no feature ever ships without exploratory testing.
- D) Agree in the meeting, then do the exploratory session anyway without telling anyone.

**Correct answer: B**

**Explanation:** This scenario tests whether you can advocate for testing value without turning advocacy into veto. Option B makes the professional case in the product manager's own currency — risk: scripted acceptance tests are bounded by what the criteria anticipated, and eligibility logic with interacting conditions is the canonical home of unanticipated failure modes (condition combinations, boundary interactions, order effects). Offering a timebox converts an all-or-nothing argument into a cheap-insurance proposal, and accepting the team's informed decision keeps the decision where it belongs — informed is the part you own. Option A mistakes the definition of done for the definition of tested; criteria-derived tests inherit the criteria's blind spots. Option C converts a risk judgement into dogma, spending credibility you will need for battles that matter more. Option D is the most corrosive: it wins the argument by deception, breaks planning transparency, and if the session finds nothing, you have spent a hidden day proving the product manager right. Your role explicitly pairs exploratory testing with advocating within the team — this is what the pairing looks like when the room pushes back.

**Question 6 (moderate) — Least effective: cross-team environment conflict**

Your performance test window on STAGE, booked a week ago, has been taken by another team deploying a hotfix rehearsal; their lead says "we'll be done in two days, and our thing is urgent". Your window feeds a release decision on Friday. Which response is **least** effective?

- A) Talk to their lead directly: establish both teams' actual constraints, explore whether a partial window or off-hours slot could serve both, and jointly escalate to the environment owner only if no option works.
- B) Post in the shared channel that your window was booked first and the other team needs to leave.
- C) Reschedule your performance tests to the weekend without checking whether the results would still reach Friday's decision.
- D) Inform your delivery manager now that the Friday decision input is at risk, while you work the options with the other team.

**Correct answer: B**

**Explanation:** Rank the responses by what they accomplish. Option A is textbook: constraints on the table, options explored, escalation held in reserve for genuine deadlock — direct resolution attempted before any authority is invoked. Option D is not a rival to A but its complement: early warning to your decision-owner while resolution proceeds keeps Friday's risk visible without weaponising it. Option C is poor — it may silently deliver results after the decision they exist to inform, defeating the purpose — but it is at least an attempt at accommodation, and its flaw (not checking the timing) is an error of thoroughness. Option B is the least effective: it converts a solvable scheduling collision into a public territorial claim, invokes procedural right ("booked first") without engaging the other team's urgency claim at all, and forces their lead to either back down publicly or dig in — the classic difficult-dynamics failure. Public channels are for coordination, not confrontation; and "least effective" in SJTs is usually the option that makes the human problem bigger while leaving the practical problem unsolved. Note the underlying professional point: environment contention is chronic, and the analysts who handle it by relationship and option-generation, escalating jointly rather than against each other, are the ones whose test needs get met next time too.

**Question 7 (moderate) — An awkward finding in a senior colleague's area**

During exploratory testing you find that a data export feature — built and "fully tested" last quarter by a well-respected senior developer — silently truncates records containing certain special characters. The feature is in production. The developer is influential and known to be defensive about their work. What is the most effective response?

- A) Raise the defect with full reproduction detail, factually and without commentary on last quarter's testing; give the developer a heads-up before wider triage sees it, so they hear it from you first; and treat the production impact question (how many exports affected?) as the immediate priority.
- B) Quietly mention it to the developer and let them decide whether it becomes a defect.
- C) Raise the defect and add a note that the original testing clearly missed this.
- D) Leave it — it has been in production a quarter already, so it cannot be urgent.

**Correct answer: A**

**Explanation:** Untangle the three threads: a production defect with unknown blast radius, a defect record that must exist, and a relationship that determines how smoothly both get handled. Option A handles each precisely. The defect is raised formally — silent data truncation in production is exactly the kind of quiet, compounding harm that cannot live in a private conversation (option B leaves the record and the remediation hostage to the developer's comfort). The framing is factual and forward-looking: reproduction, impact, next steps — no archaeology about last quarter's testing, because option C's editorial note purchases nothing except defensiveness, and blame in defect records poisons the openness your team's future defect reporting depends on. And the personal heads-up is the difficult-dynamics move that costs five minutes and changes everything: people defend against ambush, not against colleagues who brought them the problem first. Option D reasons backwards — longevity in production means the impact question is bigger, not smaller: a quarter of exports may be quietly wrong. Behaviours mapped: courage in reporting regardless of the author's status, impact-first prioritisation, and the relational intelligence your communication skill names explicitly.

**Question 8 (moderate) — Your estimate is challenged in front of stakeholders**

In a planning session with external stakeholders present, the programme manager says: "Testing says three weeks for this scope, but frankly that feels padded — other teams do it in one. Can we just say one week?" Heads turn to you. What is the most effective response?

- A) Concede in the room and hope to claw the time back later.
- B) Calmly stand your ground with the reasoning: outline what the three weeks contain (risk areas, test types, environments), invite a scope conversation — "we can do one week's testing; here is what one week covers and what it leaves untested" — and offer to review the estimate against the other teams' comparison afterwards.
- C) Say "fine, one week" and privately plan to test for three.
- D) Tell the programme manager that other teams' quality is not your problem.

**Correct answer: B**

**Explanation:** An estimate challenged in public is a test of whether your numbers have reasoning behind them — and option B demonstrates that they do, without turning the exchange into a contest. Its centrepiece is the trade-off reframe: "one week buys this coverage and leaves these risks untested" converts an argument about whose number is right into a scope-and-risk decision the stakeholders can genuinely own — which is exactly what managing differing stakeholder perspectives means under pressure, and it treats the room as adults entitled to choose their risk with open eyes. Offering to examine the other-teams comparison afterwards takes the challenge seriously rather than dismissing it (perhaps their scope, automation coverage, or risk profile genuinely differs — worth knowing either way). Option A trades the service's protection for momentary comfort and teaches the room that testing estimates collapse under stares. Option C is deception with a built-in detonation date at week one's end. Option D is defensiveness wearing a professional costume — it answers a comparison with a dismissal and advocates for nobody. Advocating for the team externally is your named skill; this is its exam condition: firm on evidence, open on scope, calm in tone.

**Question 9 (hard) — Conflicting priorities from two legitimate authorities**

Your team's test approach — which you helped create and the team agreed — requires accessibility testing before any user-facing release. The service is due to release Thursday under a ministerial announcement deadline. Wednesday afternoon, the accessibility specialist is pulled away by a departmental emergency; they cannot return until Monday. The delivery manager says: "We release Thursday regardless — the announcement is fixed. Make the testing work." What is the most effective response?

- A) Run the accessibility checks yourself overnight using automated tools, and sign the release off as accessibility-tested.
- B) State the position precisely and route it as a risk decision: automated checks can cover a portion of accessibility risk tonight and you will run them, but they are not equivalent to specialist testing; the release would go out with a known, partially-mitigated accessibility gap, so the residual risk needs formal acceptance by the appropriate owner, alongside a committed specialist test on Monday with a rapid-fix path for findings.
- C) Refuse: the approach requires accessibility testing, so Thursday's release cannot happen.
- D) Escalate to the accessibility specialist's director demanding their return.

**Correct answer: B**

**Explanation:** This scenario compresses the hardest structural truth of the role: you own the evidence and the risk statement; you do not own the release decision — and the highest-scoring response honours both halves. Option B does the professional maximum within that boundary: it extracts every drop of legitimate mitigation available tonight (automated checks genuinely catch a meaningful subset of accessibility failures), refuses the false equivalence (automated coverage is not specialist testing — and for government services, accessibility is a legal obligation under which unfound failures exclude real users), converts the remainder into a formally-owned residual risk with a named acceptance decision, and pre-builds the remediation path (Monday's test plus rapid fixes) so acceptance is bounded, not open-ended. Option A is the trap for the diligent: heroic effort culminating in a false attestation — "signed off as accessibility-tested" claims a verification that did not occur, and the signature is yours. Option C overplays your authority: the approach is the team's agreement, and deadline-versus-approach conflicts are decided by decision-owners informed of consequences, not vetoed by any single role; option C also surrenders the chance to shape a mitigated path. Option D spends escalation on commandeering a person managing a genuine emergency — disproportionate and almost certainly futile. Contributing to mitigation and contingency plans is your named skill; option B is that skill executed in real time: mitigate what you can, quantify what you cannot, and put the residual where residuals belong — with the accountable owner, in writing.

**Question 10 (hard) — Most and least effective: the retrospective revelation**

At a retrospective, a developer mentions offhandedly: "Half the unit tests in the notifications service have been commented out since March — they kept failing the build and we were under deadline." The team laughs uneasily and the facilitator starts to move on. You are the test analyst. Consider these responses:

1. Let it pass in the meeting, then raise a quiet defect about the commented-out tests tomorrow.
2. Intervene now, constructively: ask the facilitator to hold the topic, establish the facts briefly (which tests, what they covered, what has shipped since March), and propose the team treat it as a joint quality risk — reinstating coverage becomes a tracked action with an owner, and the deadline pressure that caused it becomes a retrospective theme rather than a punchline.
3. Ask, in the meeting, who commented them out and why they thought that was acceptable.
4. Say nothing in the meeting or after — unit tests belong to the developers, not to QA.

Which is the most effective response, and which is the least effective?

- A) Most: 2; Least: 4
- B) Most: 2; Least: 3
- C) Most: 1; Least: 4
- D) Most: 3; Least: 1

**Correct answer: A**

**Explanation:** Evaluate each. Response 2 is clearly strongest: the retrospective is precisely the forum for this — the team is assembled, the norm being tested ("we disable safety nets under pressure and laugh about it") is a team norm, and letting the moment pass ratifies it. The intervention is constructive rather than prosecutorial: facts first, joint framing ("our quality risk", not "your shortcut"), a tracked action, and — crucially — attention to the cause (deadline pressure) rather than only the symptom. Response 1 gets the artefact fixed but misses the norm: a quiet defect tomorrow addresses coverage while leaving the team's laughter as the last word on whether this is acceptable — half the value, and the harder half lost. Response 3 raises it in the room but as an interrogation — "who did this?" converts a systems conversation into a blame hunt on the spot, which is both the least effective way to change behaviour and toxic to the psychological safety retrospectives run on; note, though, that it at least surfaces the issue. Response 4 is the least effective of all: it wraps abdication in a demarcation myth. Unit tests are part of the team's quality position — six months of shipped changes with half a safety net down is squarely material to any risk assessment you have signed in that window — and "not my tests" is the reasoning of a role that has forgotten what it is for. Advocating for full team ownership of quality is the spirit of your planning skill; response 2 enacts it, response 4 renounces it. Comparing 3 and 4 for the bottom slot: clumsy engagement beats principled absence — silence loses.

**Question 11 (hard) — The improvement that threatens a colleague**

You have trialled a new test data generation tool in your own work: it reduces test data preparation from two days to two hours per cycle, with better coverage of edge cases. Preparing test data manually is a large part of a long-serving teammate's role, and they have twice deflected your suggestions to look at the tool, once saying "we've always done it this way and it works". You believe adopting it would significantly improve the team's capability. What is the most effective response?

- A) Deploy the tool into the team's pipeline yourself — results will speak for themselves.
- B) Drop it — team harmony is worth more than a tool.
- C) Bring the trial results to the team as a shared decision, framed around what the change enables rather than what it replaces; talk with your teammate beforehand, acknowledging their expertise directly and exploring what their deeper knowledge could do with the freed time — data strategy, the complex cases automation can't reach — so the proposal reaches the team with them, not against them.
- D) Send the productivity comparison to the test manager and let them handle the people side.

**Correct answer: C**

**Explanation:** The technical case is already made; the entire remaining problem is human, and SJTs at this level probe whether you can tell the difference. Your teammate's deflection is almost certainly not about the tool — it is about what the tool implies for the value of their accumulated expertise, and any response that ignores that subtext fails regardless of its logic. Option C works because it converts the threatened party into a co-author: the pre-conversation acknowledges their expertise as an asset the change needs (someone must define what good data looks like, own the strategy, handle what generation cannot), the framing is expansion rather than replacement, and the decision routes through the team, where it belongs — improvement by consent is the only kind that sticks. Option A wins the pipeline and loses the person — unilateral deployment into shared infrastructure breaches team ownership and confirms the teammate's worst reading of your intentions. Option B abandons a genuine capability improvement to avoid one uncomfortable conversation — harmony purchased by stagnation, and your role explicitly includes researching and introducing new techniques. Option D outsources the human difficulty upward, arriving at the manager as a productivity case against a colleague — which is how the teammate will experience it, whatever you intended. Contributing to continuous improvement is a named part of your planning skill; this question is the reminder that in mature teams, how an improvement lands is inseparable from whether it lands.

**Question 12 (hard) — Discovering your own earlier mistake has consequences**

Preparing evidence for Friday's release board, you discover that a defect you retested and closed three weeks ago — a fix for incorrect eligibility date calculations — was retested against the wrong build. The fix may or may not actually work; your closure note says "verified". The feature has been live for two weeks. Eligibility decisions affect citizens' payments. What is the most effective response?

- A) Retest correctly now, quietly; if it passes, update nothing — the record ends up true either way.
- B) Retest correctly now, and regardless of the result, tell your test manager and the team today: the closure was recorded against the wrong build, the production behaviour has been unverified for two weeks in a payments-affecting feature, and if the retest fails, impact analysis on two weeks of live eligibility decisions starts immediately.
- C) Wait until after Friday's board — no point complicating the release with a three-week-old issue.
- D) Reopen the defect and assign it back to the developer without explanation.

**Correct answer: B**

**Explanation:** Strip it to what is actually true right now: a payments-affecting calculation has been running in production for two weeks with no valid verification, the record claims otherwise, and the person who knows this is you. Option B is the only response that treats all three facts with the seriousness they carry. Disclosure is immediate and unconditional — not contingent on the retest failing — because the verification gap itself is material information: your team has been operating on a false "verified", and Friday's board is about to inherit it; timing the truth around the board (option C) converts an honest mistake into deliberate concealment from the exact forum that exists to weigh such information. The retest happens at once because it collapses the uncertainty cheaply. And the failure branch is pre-planned — two weeks of live eligibility decisions means citizens may have been mispaid, so impact analysis cannot wait for anyone's comfort. Option A is the deep trap, and it deserves slow examination: if the retest passes, the outcome was fine but the record's "verified" was still false when written, your process failure stays invisible (so nothing prevents its recurrence — perhaps by someone whose defect does fail), and you have practised concealing near-misses — which is how organisations teach themselves to conceal hits. Option D leaks the problem into the workflow stripped of the context — wrong build, live exposure, urgency — that makes it actionable, and hands a developer your mistake unexplained. The behaviours mapped: ownership without self-protection, honest records as non-negotiable, user impact first, and the mark of a mature professional — reporting your own error with the same rigour you would report the system's.

### Preparation tips

- **Anchor on the behaviours, not on cleverness.** UK government digital teams assess against user focus, honesty, collaboration, ownership, and appropriate escalation. Before choosing, ask which option best serves the citizen and the truth — that single filter resolves most scenarios.
- **Locate the decision-owner in every scenario.** Many hard questions turn on the boundary between informing a decision and making it. Your role owns evidence, risk statements, and recommendations; releases, waivers, and scope belong to their owners. Options that respect that boundary while maximising the quality of the decision usually score highest.
- **Watch the order of operations.** Direct conversation before escalation; facts before framing; disclosure before (or alongside) remediation — but risk-stopping actions immediately. Many options contain the right elements in the wrong sequence.
- **Rehearse with real memories.** After each practice question, recall your nearest real equivalent and compare what you actually did with the highest-scoring option. The gap, examined honestly, is the training.
- **Distinguish "uncomfortable" from "ineffective".** High-scoring options are frequently the awkward ones: correcting a respected colleague, disclosing your own error, holding an estimate under public challenge. If an option's only drawback is discomfort, that is often the answer.
- **Read "least effective" questions with full attention.** Rank the harm: options that hide information, ratify bad norms, or abandon the role's purpose sit below options that are merely clumsy or confrontational. Silence is usually worse than imperfect engagement.

### Common pitfalls to avoid

- **Softening the record to manage the mood.** Any option that trades factual accuracy in defect ratings, summaries, or closure notes for stakeholder comfort is the most reliably penalised choice in testing SJTs — because it is the most damaging behaviour in testing practice.
- **Escalating past the conversation.** Managers, directors, and public channels before a direct, professional exchange with the person involved — SJTs read this as conflict avoidance wearing an assertive mask. Escalate on substance, after engagement, ideally jointly.
- **Unilateralism in shared territory.** Deploying tools into team pipelines, rewriting colleagues' work, vetoing releases, signing off what wasn't verified: options where you act alone in space the team or a decision-owner shares are consistently marked down, even when your technical judgement is right.
- **Confusing role boundaries with indifference.** "Not my tests", "their module", "the developer's call" — demarcation reasoning scores badly because quality is a whole-team property. The counterpart error — doing everyone's job for them — scores no better. The high road is engagement through influence.
- **Timing truth for convenience.** Holding disclosures until after boards, demos, or releases converts honest problems into concealment. In scenario after scenario, the option that tells the right person today beats the option that tells everyone eventually.
- **Solving the technical layer and missing the human one.** Hard scenarios hide a person inside the problem — the defensive developer, the threatened teammate, the laughing retrospective. Options that are logically impeccable but relationally blind rarely top the scoring; read for who is affected, not only what is broken.

## Conclusion

Well done — you have worked through a substantial and demanding set of practice material, and every section of it has exercised capabilities you use in earnest every working day.

Look back at what you have covered. In the **cognitive assessment** section, you practised recognising defect clusters and bimodal automation patterns, deducing outcomes from layered business rules and triage policies, checking coverage matrices against risk-dependent standards, sequencing constrained test schedules, diagnosing flaky tests from evidence patterns, and allocating scarce testing effort where risk concentrates. In the **numeric reasoning** section, you worked step by step through pass rates with honest denominators, defect flow arithmetic, weighted averages, ratio-true test data, detection percentages with moving denominators, environment availability, and a complete automation business case — the quantitative spine of the reports and risk communications your role produces. In the **verbal reasoning** section, you sharpened the true/false/cannot-say discipline against release policies, supplier emails, and data handling standards; practised catching attribution shifts, inflated obligations, and omitted conditions; evaluated a vendor's argument; and reconciled three conflicting artefacts the way analysis genuinely requires. And in the **situational judgement** section, you navigated the human terrain — severity disputes, softening pressure, silent automation failure, public estimate challenges, colleagues' mistakes and your own — and saw the consistent shape of the most effective responses: honest, direct, user-centred, and respectful of who owns which decision.

The through-line is worth stating plainly: these assessments are not adjacent to your profession — they are your profession, distilled. The analyst who checks every condition of a rule, normalises before comparing, reads the qualifier rather than the vibe, and tells the accountable owner the truth today is simultaneously the candidate who scores well and the professional whose judgement teams learn to trust. Practising one strengthens the other, in both directions.

At your level, that trust is the asset under construction. You design and execute tests independently, you assess risk and communicate it, and you are increasingly the person a team turns to when the evidence is ambiguous or the conversation is difficult. The habits rehearsed here — precision, honest denominators, exact reading, and judgement that keeps the citizen at the centre — are what that reputation is made of.

Before any real assessment, return to the preparation tips and work a handful of questions from each section to warm up the specific muscles. Between now and then, use your daily artefacts as a free practice library: every coverage matrix, defect trend, policy extract and awkward stakeholder moment is a question from this guide wearing work clothes.

Keep practising, keep asking "out of how many?", keep reading the small words, and keep telling the truth early. Good luck — you are well prepared, and getting better.
