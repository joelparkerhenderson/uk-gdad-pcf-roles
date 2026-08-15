# Test Manager - Psychometric Assessment Resources

## Introduction

Welcome! This guide has been created especially for you as a test manager working within the UK Government Digital and Data profession. Whether you are preparing for an internal assessment, applying for a new post, benchmarking your own capability against the framework, or simply curious about how psychometric assessments relate to the work you already lead every day, this document will help you practise, reflect, and build confidence.

Psychometric assessments are structured, standardised exercises that measure the mental capabilities and behavioural tendencies that predict success in a role. For a test manager, that means far more than abstract puzzles. The assessments described here are job-specific: they use the kinds of artefacts you genuinely handle — test strategies, defect trend reports, release readiness dashboards, environment schedules, coverage matrices, supplier performance packs, and stakeholder communications — and the kinds of decisions you genuinely make, such as owning the quality assurance and testing strategy as part of a broader risk-based approach, leading its implementation across multiple teams, and making important decisions relating to test within the context of the delivery environment.

Why do these assessments matter for your role in particular? As a test manager, you take ownership of delivery. You create the strategy, lead others in adopting it, and are responsible for test improvement and optimisation. You mediate between technical testers and non-technical stakeholders, you use defect patterns and trends to make tactical and strategic recommendations, and you take responsibility for talent, succession planning and supplier management. Assessments of cognitive ability, numerical reasoning, verbal reasoning, and situational judgement map directly onto those demands. Practising them sharpens exactly the skills your role depends on: spotting a logical inconsistency in an exit-criteria decision, interpreting a defect density table under time pressure, extracting precise meaning from a policy extract or a supplier contract clause, and choosing the most effective course of action when a release deadline collides with an open severity-one defect.

This document is organised into four main assessment sections, each following the same pattern: an overview of what the assessment measures and why employers use it for test management roles, a mapping of the assessment dimensions to the specific named skills in the test manager capability framework, a substantial set of practice questions with full worked explanations, practical preparation tips, and common pitfalls to avoid. The questions progress from easy through moderate to hard within each section, so you can warm up before stretching yourself.

Here is how to get the most from it. First, read each "About this assessment" section so you understand the format you are likely to face. Second, attempt the practice questions honestly — commit to an answer before reading the explanation, exactly as you would ask a tester to record an expected result before executing a test. Third, treat every explanation as a mini-lesson: even when you answer correctly, the reasoning walkthrough will deepen your technique, and many explanations connect the technique back to your leadership duties. Finally, use the preparation tips and pitfalls for self-reflection: they connect assessment performance back to your professional development as a leader who coaches others, advocates for quality, and represents the testing community inside and outside your organisation.

Take your time, be kind to yourself, and enjoy the practice. Quality is your profession; bring the same structured, risk-based mindset to your own development that you bring to every release you assure. Let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive ability assessment measures the exact mental processes your role demands, using practical workplace scenarios rather than abstract puzzles. Unlike a generic intelligence test, it presents you with the everyday materials of your job — in your case, test strategies and plans, defect logs, environment booking schedules, traceability matrices, release readiness reports, and governance papers — and asks you to reason quickly and accurately about them.

Typical format: an online, timed test lasting 15 to 30 minutes, with questions covering pattern recognition, logical deduction, error checking, prioritisation, and applied problem solving. Scoring is objective, comparing your responses against a norm group, and modern platforms often adapt question difficulty based on your previous answers: answer correctly and the next item gets harder, answer incorrectly and it eases off, which allows the platform to locate your ability level precisely with fewer questions. Employers usually receive a breakdown of speed versus accuracy rather than a single score, so working both quickly and carefully matters. You will normally be offered short, ungraded practice questions before the real test begins, so you can get comfortable with the interface without pressure.

For a test manager, cognitive ability assessment is particularly relevant because structured thinking is the engine of everything you own. A quality testing strategy is, at heart, an exercise in logic: which risks matter, which test types and techniques mitigate them, in what sequence, with which environments and data, and against which entry and exit criteria. When you lead others in designing, building, maintaining and executing tests, you are constantly checking their reasoning as well as their artefacts — does this test actually exercise the requirement it claims to trace to? Does this defect trend genuinely support the tactical recommendation being made from it? When you make important decisions relating to test within the delivery environment, you often make them under time pressure with incomplete information, which is precisely the condition a timed cognitive assessment simulates. Employers use these assessments for test management roles because the cost of a reasoning failure at your level is high: a flawed exit-criteria judgement or a misread coverage matrix can let a defect escape into a live public service used by millions of citizens.

A note on fairness and reasonable adjustments: reputable assessment platforms used across the Civil Service comply with accessibility standards, and you are entitled to request reasonable adjustments — extra time, screen reader compatibility, alternative formats — if you need them. As someone who advocates for inclusive, user-centred quality practices, you should feel no hesitation in using these provisions yourself.

### How this assessment maps to your role

The assessment dimensions map directly to the named skills in your capability framework:

- **Pattern recognition** maps to your **Managing, reporting and resolving defects** skill: leading and coaching others in using defect patterns and trends to make tactical and strategic recommendations is pattern recognition applied at scale — clusters by component, spikes by sprint, recurring root causes across teams.
- **Logical deduction** maps to **Test analysis** and **Test and quality planning**: using multiple techniques to analyse complex information to identify risks, and determining if an approach needs to change based on effort and risk, requires you to reason validly from requirements, constraints, and criteria to their consequences.
- **Error checking** maps to **Designing and executing tests**: when you lead others in designing, building, maintaining and executing tests that align to user needs and requirements, and contribute to developing standards for test design, you must spot inconsistencies between artefacts — a test case that no longer traces to any requirement, an environment schedule that double-books a shared service, a dashboard whose RAG status contradicts its own underlying figures.
- **Prioritisation** maps to your responsibility to **make important decisions relating to test within the context of the delivery environment**: with fixed release dates, shared environments, and finite testers, ranking what matters most — by risk, not by noise — is a daily discipline, and it also underpins **Test and quality planning** when you guide teams in optimising approaches using appropriate data.
- **Applied problem solving** maps to your responsibility for **test improvement and optimisation** and to **Test engineering**: reasoning about why a testing process, environment or tool is underperforming, and working through constraints to a workable schedule or scope, is problem solving with real delivery consequences.

### Practice questions

**Question 1 (easy) — Pattern recognition in test case identifiers**

Your team's test management standard requires test case identifiers in the format `<Project code>-<Test level>-<Sequence number>`, where the project code is three capital letters, the test level is one of UT (unit), IT (integration), ST (system) or AT (acceptance), and the sequence number is three digits. Reviewing a regression pack submitted by one of your teams, you see:

1. PAY-ST-014
2. PAY-AT-131
3. PAY-141-ST
4. PAY-IT-006
5. PAY-UT-090

Which entry breaks the naming standard?

- A) Entry 2
- B) Entry 3
- C) Entry 4
- D) Entry 5

**Correct answer: B**

**Explanation:** The standard fixes the order: project code, then test level, then sequence number. Entry 3 transposes the last two elements, putting the sequence number "141" where the test level belongs and "ST" at the end. Entries 1, 2, 4 and 5 all conform. This looks trivial, but it is exactly the kind of consistency check you perform when you contribute to developing and implementing standards for designing and executing tests: broken identifier conventions quietly destroy traceability, break automated reporting that parses identifiers, and make defect-to-test cross-referencing unreliable. In an assessment, questions like this reward methodical element-by-element comparison rather than gestalt impressions — read each entry against the rule, one component at a time.

**Question 2 (easy) — Logical deduction from exit criteria**

Your system test exit criteria state: "System testing may close only when all severity 1 and severity 2 defects are resolved, unless the service owner grants a documented waiver for a specific severity 2 defect." A delivery manager tells you: "System testing has closed, and one severity 2 defect remains unresolved." Which one of the following conclusions must be true?

- A) The exit criteria were breached.
- B) The service owner granted a documented waiver for that defect.
- C) Either the service owner granted a documented waiver for that defect, or the exit criteria were breached.
- D) The defect was downgraded to severity 3 before closure.

**Correct answer: C**

**Explanation:** The criterion is a conditional rule with one permitted exception. From the facts given you cannot tell whether a waiver exists, so neither A nor B must be true on its own — each is merely possible. D invents an event not mentioned anywhere in the stem. The only conclusion guaranteed in every situation consistent with the facts is the disjunction in C: one of the two possibilities must hold. Assessments reward this discipline of concluding only what the information guarantees — and so does your job. Before you challenge a team for breaching exit criteria, you check the waiver record; deducing carefully protects your stakeholder relationships as well as your logic, which matters when you moderate difficult discussions about high risk topics.

**Question 3 (easy) — Error checking a traceability matrix**

You spot-check a requirements-to-test traceability matrix. The standard requires every requirement to be covered by at least one test case, and every test case to trace to at least one requirement. An extract reads:

| Requirement | Test cases |
|---|---|
| R-01 Submit application | TC-101, TC-102 |
| R-02 Save draft | TC-103 |
| R-03 Upload evidence | (none) |
| R-04 Receive confirmation email | TC-105 |

Separately, the test pack contains TC-106, which traces to no requirement. How many distinct breaches of the standard does this extract show?

- A) 0
- B) 1
- C) 2
- D) 3

**Correct answer: C**

**Explanation:** Work through both directions of the rule. Requirement-to-test: R-01, R-02 and R-04 are each covered by at least one test case, but R-03 has none — one breach. Test-to-requirement: TC-101, TC-102, TC-103 and TC-105 all trace correctly, but TC-106 traces to no requirement — a second breach. Total: two distinct breaches. A common error is to count only the visible gap in the table (answer B) and forget the orphaned test case mentioned in the prose, or to double-count R-03 as two problems. Bidirectional traceability checking is core to leading others in designing tests that align to user needs and requirements: an uncovered requirement is untested risk, and an orphaned test is wasted effort — both are quality signals you coach teams to catch themselves.

**Question 4 (moderate) — Prioritisation across a test portfolio**

It is Monday morning. Four items compete for your attention:

1. A go/no-go board meets on Wednesday and needs your release readiness assessment for a service entering public beta; without it, the board cannot decide.
2. A test analyst you line manage has asked for feedback on their first draft test approach, which they must present to their delivery team on Friday.
3. A supplier's monthly performance report, due to be discussed at the contract review in three weeks, has arrived and appears to show declining automated test reliability.
4. A programme director has emailed asking "how quickly could your team pick up testing for a new service?" with no deadline stated.

Which sequencing is most defensible?

- A) 4, 1, 2, 3 — directors outrank all other demands
- B) 1, 4, 2, 3 — board-blocking assessment first, then a brief scoping reply to the director, then coaching, then the supplier report
- C) 1, 2, 3, 4 — strict order of deadline proximity
- D) 2, 1, 4, 3 — developing your people always comes first

**Correct answer: B**

**Explanation:** Prioritisation questions test reasoning about impact and urgency together. Item 1 is both urgent (Wednesday) and high impact — it gates a public beta decision, and producing release readiness assessments is squarely your accountability for delivery. Item 4 has no deadline but is strategically significant and sponsored by a director; a short same-day scoping reply manages expectations without displacing deeper work, so it sensibly comes second. Item 2 matters — talent development is explicitly part of your role — but its Friday deadline allows it to follow. Item 3 is important evidence for supplier management, but the contract review is three weeks away; you should read it this week, not this morning. Option A over-weights seniority against a hard governance deadline; C confuses "no stated deadline" with "lowest priority"; D inverts impact ordering. The strong pattern: sequence by impact-weighted urgency, not by any single dimension such as seniority, deadline date, or personal preference.

**Question 5 (moderate) — Pattern recognition in defect trends**

Across the last four sprints, one of your teams recorded defects found in system testing, broken down by component:

| Component | Sprint 1 | Sprint 2 | Sprint 3 | Sprint 4 |
|---|---|---|---|---|
| Payments engine | 4 | 5 | 4 | 5 |
| Address lookup | 3 | 2 | 3 | 2 |
| Notifications | 2 | 6 | 11 | 19 |
| Reporting | 5 | 4 | 5 | 4 |

As the test manager coaching this team in using defect patterns, what is the most defensible first reading of this table?

- A) The team's testing is deteriorating, because total defect counts are rising.
- B) Notifications shows an accelerating defect trend that warrants targeted investigation; the other components are stable.
- C) Payments engine is the highest risk component because payments matter most to users.
- D) Nothing can be concluded until severity data is available.

**Correct answer: B**

**Explanation:** Read each row as a series. Payments (4, 5, 4, 5), address lookup (3, 2, 3, 2) and reporting (5, 4, 5, 4) all oscillate within a narrow, stable band. Notifications runs 2, 6, 11, 19 — roughly doubling each sprint — a genuinely accelerating trend that dominates the total. Option A misattributes the rise: totals climb only because of one component, and rising defect *detection* may even reflect improved testing rather than worse quality. Option C imports an importance judgement not supported by the data in front of you — payments may matter, but its trend is flat. Option D overcorrects: severity data would enrich the analysis, but trend identification is legitimate and actionable now, and "wait for perfect data" is not how you lead. This is precisely your skill of using defect patterns and trends to make tactical recommendations: the pattern points you to where to look — recent changes to the notifications component, its test coverage, its team's workload — before defects escalate further.

**Question 6 (moderate) — Logical deduction about environment scheduling**

Your environment schedule has these rules: (i) performance testing cannot start until the production-like environment is refreshed with anonymised data; (ii) the data refresh cannot start until the current user acceptance testing (UAT) cycle finishes, because both use the same environment; (iii) security testing must run either in the same week as performance testing or the week immediately after it. UAT finishes at the end of week 2. The data refresh takes one full week. What is the earliest week in which security testing can run?

- A) Week 2
- B) Week 3
- C) Week 4
- D) Week 5

**Correct answer: C**

**Explanation:** Work forwards through the dependency chain. UAT finishes at the end of week 2, so the data refresh occupies week 3 at the earliest and completes at the end of week 3. Performance testing can therefore start in week 4 at the earliest. Security testing must run in the same week as performance testing (week 4) or the week immediately after (week 5); the earliest permissible week is week 4. A tempting error is week 5, from anchoring on "after performance testing" and forgetting the same-week option; another is week 3, from forgetting the refresh takes a full week. Dependency reasoning of exactly this kind underpins setting up suitable environments and creating and managing multiple test plans: environment contention is one of the most common causes of test schedule slippage, and a test manager who can reason cleanly about sequencing protects delivery dates without cutting scope.

**Question 7 (moderate) — Error checking a release readiness dashboard**

A release readiness dashboard prepared by a test lead reports:

- Test cases planned: 400; executed: 380; passed: 361
- Pass rate: "95% of planned"
- Severity 1 defects open: 0; severity 2 defects open: 2
- Overall status: GREEN, with the note "exit criteria met: pass rate ≥ 95% of executed, no open sev 1, no open sev 2"

Which single statement best describes the dashboard's problem?

- A) The pass rate is calculated on the wrong base, and the stated exit criteria are not met because two severity 2 defects are open.
- B) The pass rate is correct but the status should be AMBER, not GREEN.
- C) The dashboard is internally consistent; the status is defensible.
- D) The executed count must be wrong because 400 were planned.

**Correct answer: A**

**Explanation:** Check each figure against its own definitions. The pass rate label says "95% of planned", and 361 ÷ 400 = 90.25% of planned — but the exit criterion is defined against *executed*: 361 ÷ 380 = 95.0%, which does meet the threshold. So the pass rate as labelled is wrong (wrong base), even though the criterion it feeds happens to be satisfied. More seriously, the exit criteria as quoted require *no open severity 2 defects*, and the dashboard itself reports two — so "exit criteria met" is false on the dashboard's own numbers, and GREEN is unsupportable. Option A captures both defects. Option B concedes the label error but misses that the sev 2 count breaches the stated criteria outright. This is the error-checking discipline behind your accountability for making important release decisions: dashboards that contradict themselves are common, and boards will act on the RAG colour unless you catch the contradiction first. Always recompute headline percentages from the raw counts, and always test the status claim against the criteria as written.

**Question 8 (moderate) — Applied problem solving on flaky automation**

An automated regression suite of 500 tests has been failing intermittently. Investigation shows: 20 tests fail on every run (consistent failures); a further 45 tests each fail on roughly half of runs with no code changes between runs (intermittent); the remaining 435 pass consistently. The team proposes to "re-run the suite until everything passes and then sign off". As test manager, which reasoning is soundest?

- A) Agree — if every test has passed on at least one run, the software is demonstrated to work.
- B) Disagree — consistent failures indicate genuine defects or broken tests that need diagnosis, and intermittent failures make those 45 tests unreliable as evidence either way; re-running until green hides both problems.
- C) Disagree — the whole suite should be discarded and rewritten because 13% of it misbehaves.
- D) Agree, but only if the suite passes twice in a row.

**Correct answer: B**

**Explanation:** Reason about what each failure class tells you. Twenty consistent failures are a signal: either the software has defects or the tests are wrong — both demand diagnosis, not re-running. Forty-five intermittent failures mean those tests are not deterministic; a pass from a non-deterministic test is not evidence of correct behaviour, merely a lucky sample, so "re-run until green" is selection bias formalised — you keep sampling until you get the answer you want. Option A mistakes an eventual pass for demonstrated correctness. Option D is A with extra steps: two lucky runs are still luck. Option C overreacts — 87% of the suite is healthy and rewriting everything wastes that asset; the proportionate response is to quarantine and fix the flaky tests and diagnose the consistent failures. This is your test improvement and optimisation duty in miniature, and it also reflects the test engineering skill of understanding why reliable tooling matters: an automation suite is only as valuable as the trust you can place in its results, and coaching teams out of "re-run until green" is one of the highest-value interventions a test manager makes.

**Question 9 (challenging) — Multi-constraint test scheduling**

You must schedule three test activities — accessibility testing (X), performance testing (P), and a final regression cycle (G) — across five working days, Monday to Friday, at most one activity per day. Constraints: (i) G must run on the day immediately after P, so that configuration changes made during performance tuning are included in the regression build; (ii) the performance test environment is only available on Monday and Thursday; (iii) X must come before G, with at least one clear working day between X and G for accessibility fixes to be applied; (iv) X cannot be on Monday, because the assistive-technology specialist is unavailable then. On which day must G take place?

- A) Wednesday
- B) Thursday
- C) Friday
- D) It cannot be scheduled within the week

**Correct answer: C**

**Explanation:** Work the constraints as a system, testing each candidate placement of P. Case 1: P on Monday. Then G is Tuesday (i). X must precede G with a clear working day between them (iii), so X would have to be on Monday at the latest — but Monday is taken by P, and X cannot be on Monday anyway (iv). Case 1 is infeasible. Case 2: P on Thursday. Then G is Friday (i). X must be early enough to leave a clear day before Friday, so X can be Tuesday (Wednesday and Thursday clear) or Wednesday (Thursday clear); Tuesday and Wednesday are both open and both satisfy (iv). Feasible — for example X Tuesday, P Thursday, G Friday. Since Case 1 fails and Case 2 forces G to Friday, G must be on Friday. The efficient technique is exactly this case analysis: anchor on the most constrained activity (P has only two possible days), propagate each case through the dependent constraints, and eliminate. It is the same reasoning you apply when juggling shared environments across teams — and the same lesson holds in live planning: the most constrained resource, not the most important activity, is what actually determines your schedule, so identify it first and build outwards from it.

**Question 10 (challenging) — Risk-based scope reduction**

A delivery deadline has been brought forward, cutting your remaining system test window from ten days to six. Your plan had four remaining blocks: payments regression (3 days, mitigates the highest-rated risk, legally critical calculations), new-feature functional testing (3 days, moderate risk, feature can be dark-launched behind a flag), cross-browser compatibility (2 days, low risk, analytics show 96% of users on three browsers you can cover in 1 day), and exploratory testing of the amended user journey (2 days, high risk, recent defect cluster there). Which scope decision best reflects risk-based testing?

- A) Cut exploratory testing entirely and trim compatibility to 1 day: 3 + 3 + 1 = 7 — then trim functional testing by a day to fit 6.
- B) Keep payments regression (3) and exploratory testing (2) in full, trim compatibility to 1 day covering the three main browsers, and defer new-feature functional testing behind the feature flag for post-release testing.
- C) Run all four blocks but halve the depth of each to fit six days.
- D) Keep the plan unchanged and ask every tester to work weekends.

**Correct answer: B**

**Explanation:** Rank by risk, then spend the six days on the highest risks. Payments regression mitigates the top-rated, legally critical risk: non-negotiable, 3 days. Exploratory testing targets a recent defect cluster on a changed journey — high risk, 2 days. That leaves 1 day: compatibility trimmed to the three browsers covering 96% of users is an evidence-based reduction using appropriate data, exactly as your framework describes optimising approaches. New-feature functional testing is the block with a genuine mitigation outside testing — the feature flag allows dark launch and post-release verification without citizen exposure — so deferring it converts schedule risk into a controlled, reversible decision. Option A cuts the high-risk exploratory block while protecting a moderate-risk one, inverting the risk order. Option C spreads the cut evenly, which feels fair but is the opposite of risk-based: it thins coverage of the highest risks to preserve coverage of the lowest. Option D is not a scope decision at all; it trades staff wellbeing for schedule and typically degrades accuracy when you need it most. Determining if an approach needs to change based on effort and risk is your named test analysis skill — this question is that skill under exam conditions.

**Question 11 (challenging) — Deduction from a coverage matrix**

Your risk register lists four product risks: R1 (incorrect benefit calculation), R2 (personal data exposure), R3 (service unavailable under load), R4 (inaccessible to screen reader users). The test approach maps techniques to risks: payments regression covers R1; security testing covers R2; performance testing covers R3; accessibility testing covers R4; and exploratory testing covers R1 and R4. Status update: payments regression is complete; exploratory testing is complete; security testing is blocked; performance testing is cancelled this release; accessibility testing is 50% complete. Which risks currently have *no completed* test coverage at all?

- A) R2 only
- B) R2 and R3
- C) R3 only
- D) R2, R3 and R4

**Correct answer: B**

**Explanation:** Build the coverage picture risk by risk. R1: covered by payments regression (complete) and exploratory (complete) — covered. R2: covered only by security testing, which is blocked — no completed coverage. R3: covered only by performance testing, which is cancelled — no completed coverage. R4: covered by accessibility testing (50% complete — partial, not none) and exploratory testing (complete) — so R4 has completed coverage via the exploratory block. Therefore R2 and R3 are the uncovered risks. The trap is D, chosen by candidates who read "accessibility 50%" and forget that exploratory testing also maps to R4 — a reminder that coverage is a many-to-many mapping, and you must aggregate across all techniques before declaring a gap. In role terms, this is the analysis that turns a status report into a risk statement for a go/no-go board: "two of our four product risks currently have no completed mitigation — here is what that means and here are our options." Leading work with stakeholders to determine which quality characteristics add value, and reporting risk in those terms, is what distinguishes a test manager's report from a raw test dashboard.

**Question 12 (challenging) — Improvement logic and confounded evidence**

You introduced two changes simultaneously at the start of Q3: a new defect triage workflow and a rewritten smoke test suite. In Q3, escaped defects (found in live) fell from 24 to 15, and mean time to resolve defects fell from 9 days to 6. A board member asks: "Which change caused the improvement?" What is the most intellectually honest answer you can give, and what does it imply for how you should run improvements in future?

- A) The triage workflow caused the resolution-time improvement and the smoke suite caused the escaped-defect reduction; report both as proven.
- B) The changes are confounded: with both introduced together, the data cannot attribute either improvement to either change; the results justify keeping both, and future improvements should be introduced in a way that allows attribution, such as sequencing them or piloting in different teams.
- C) Neither change caused anything; the improvement is regression to the mean and should be ignored.
- D) Attribute both improvements to whichever change was cheaper, for the strongest efficiency narrative.

**Correct answer: B**

**Explanation:** Two interventions introduced at the same time on the same population cannot be separated by outcome data alone — the changes are confounded. Option A's mapping is plausible as a hypothesis (triage plausibly affects resolution speed; smoke tests plausibly catch escapes) but "plausible mechanism" is not "proven attribution", and reporting it as proven would misinform future investment decisions. Option C misuses a real statistical concept: regression to the mean is worth considering, but a 37% fall in escaped defects alongside a mechanism you deliberately introduced is not grounds to dismiss the result — it is grounds for cautious confidence. Option D is narrative-shopping and corrodes the evidential standards your role exists to uphold. Option B is honest about the limits of the evidence while still extracting value: the combined result supports retaining both changes, and the methodological lesson — sequence or pilot improvements so effects are attributable — is exactly what "improve test types and techniques through a structured process" means in your framework. Test managers who understand confounding run better improvement programmes and give boards advice they can trust.

### Preparation tips

- **Practise with your own artefacts.** Take a real traceability matrix, defect trend report, or release dashboard from your work and actively hunt for inconsistencies — a pass rate computed on the wrong base, a RAG status that contradicts its criteria, an orphaned test case. Ten minutes a day of deliberate error-checking builds exactly the muscle the assessment measures, and it will sharpen your artefact reviews too.
- **Verbalise your deductions.** When you conclude something from a set of rules — exit criteria, environment dependencies, coverage mappings — say the inference chain aloud or write it down. Assessments penalise plausible-sounding leaps, and so do go/no-go boards.
- **Time-box ruthlessly in practice.** Work at roughly one minute per question. If a question resists you for 90 seconds, flag it and move on — accuracy on ten questions beats perfection on four. You already apply time-boxing to exploratory test sessions; apply it to yourself.
- **Use elimination.** On multiple-choice items, discard options that introduce facts not present in the stem (a downgraded defect, an importance ranking, severity data that was never given). In this practice set, most wrong answers smuggled in outside information — real assessments do the same.
- **Recompute headline figures.** Whenever a stem quotes a percentage alongside raw counts, recompute it from the counts before trusting it. Wrong-base percentages are the single most common planted error in test-management-flavoured questions, because they are the most common real error in test reporting.
- **Prepare like it is a release.** Sleep, hydration, a distraction-free environment, and the interface practice questions taken seriously. You would never let a team enter a test cycle with an unverified environment; do not enter an assessment with an unverified setup, browser, or headset.

### Common pitfalls to avoid

- **Bringing outside knowledge into closed-world questions.** Cognitive items define a miniature world of rules. Your deep knowledge of how testing "usually" works is an asset at work but a liability here if it overrides the stated premises — answer from the stem, not from your last programme.
- **Confusing "consistent with" and "implied by".** Many candidates select an answer that could be true rather than the one that must be true. Train yourself to ask: does the given information guarantee this? It is the same discipline that separates a defect report's facts from its author's theory.
- **Time-sink questions.** Getting stuck on a single multi-constraint scheduling puzzle and sacrificing five easier questions is the most common score-killer. Skip and return — you triage defects; triage questions.
- **Misreading bases and denominators.** "95% of planned" versus "95% of executed", defects per sprint versus defects per release, availability of an environment versus availability of the specialist who uses it — assessments hide the trap in the qualifier, not the number. Read qualifiers with the care you give exit criteria.
- **Overconfidence at senior level.** Experienced test managers sometimes pattern-match to a familiar real-world situation and answer from memory rather than from the stem. The test rewards fresh reasoning every time — treat each stem as a new system under test, with its own specification.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numerical reasoning assessment evaluates your ability to analyse, interpret, and make sound decisions using numerical data drawn from the real demands of your role. It is emphatically not a mathematics exam: the arithmetic rarely goes beyond percentages, ratios, weighted averages, and rates of change. What it tests is whether you can extract the right numbers from realistic business material — test execution dashboards, defect density tables, automation coverage reports, supplier performance packs, environment utilisation schedules, and budget spreadsheets — and reason with them quickly and correctly.

Typical format: an online, strictly timed test, often 20 to 30 minutes for 15 to 25 questions, with an onscreen calculator allowed or provided. The priority is interpretation over mental arithmetic: the hard part is choosing what to calculate, reading scale qualifiers such as "per 1,000 test executions" or "defects per KLOC", and avoiding traps like mixing sprint-level and release-level figures or computing a percentage on the wrong base. Question inputs mimic the data formats of the target role, so for you they will look like the dashboards, burn-down charts and monthly supplier reports that cross a test manager's desk every week.

Numerical fluency is central to your role, not incidental to it. Your capability framework says you guide teams across an organisation in optimising quality testing approaches, plans and strategies *by using appropriate data* — and almost all of that data is quantitative: pass rates, defect find rates, escaped defect counts, automation coverage percentages, mean time to resolve, environment availability, test execution velocity, and cost per test cycle. When you take responsibility for supplier management, you must read a supplier's monthly report critically enough to notice that a headline "98% SLA achievement" is computed on a flattering base. When you make important decisions relating to test within the delivery environment, those decisions — extend the window, cut the scope, invest in automation, challenge the supplier — stand or fall on whether you have interpreted the numbers correctly. Delivery boards will act on the figures you present, so your numerical reasoning is a matter of professional credibility: one wrong percentage in a go/no-go paper can be more damaging than a dozen missed test cases.

Employers therefore use numerical reasoning assessments for test management roles to check three things: accuracy (can you compute correctly under time pressure), interpretation (do you choose the right calculation and the right base), and judgement (do you know what a number does and does not support). The practice questions below exercise all three, using the data your role genuinely handles.

### How this assessment maps to your role

- **Pass rates, defect densities and trend arithmetic** map to your **Managing, reporting and resolving defects** skill: leading and coaching others in using defect patterns and trends to make tactical and strategic recommendations means computing and comparing rates correctly — per component, per sprint, per thousand executions — and knowing when a base has shifted underneath a trend.
- **Coverage, effort and risk calculations** map to **Test analysis** and **Test and quality planning**: determining if an approach needs to change based on effort and risk, and optimising plans using appropriate data, requires you to quantify coverage gaps, estimate effort against capacity, and weigh cost against risk reduction.
- **Execution velocity and schedule arithmetic** map to **Designing and executing tests** and your ownership of delivery: leading others in executing tests to a deadline means burn-down arithmetic — executions per day against days remaining — done honestly.
- **Supplier and SLA percentages** map to your responsibility for **supplier management**: contract review meetings turn on availability percentages, defect turnaround times, and credit calculations, and you must be able to verify them from raw figures rather than accept the supplier's summary.
- **Budget and investment figures** map to your responsibility for **test improvement and optimisation** and for advocating test capabilities: business cases for automation tooling, environments and training are won or lost on payback arithmetic you must be able to defend line by line.
- **Communicating numbers to non-specialists** maps to **Communicating between the technical and non-technical**: choosing the honest, comprehensible figure — and explaining what it means — is how numerical skill becomes stakeholder trust.

### Practice questions

**Question 1 (easy) — Pass rate from raw counts**

In last night's regression run, 640 automated tests executed: 608 passed, 24 failed, and 8 errored before completing. Treating only passes as successes, what was the pass rate of executed tests, to one decimal place?

- A) 92.5%
- B) 95.0%
- C) 96.2%
- D) 97.4%

**Correct answer: B**

**Explanation:** Pass rate = passes ÷ executed = 608 ÷ 640. Compute: 608 ÷ 640 = 0.95, so 95.0%. A quick sanity check: 10% of 640 is 64, so 5% is 32, and 640 − 32 = 608 — confirming that 608 is exactly 95%. Option C (96.2%) is what you get if you wrongly exclude the 8 errored tests from the base (608 ÷ 632 = 0.962): errored tests still executed and still failed to pass, so removing them flatters the result. Option D excludes both errors and failures from the base, which is circular. The habit to build: fix the base first (what counts as the denominator?), then compute — and verify with a second method such as the 10%-then-5% scaling shown here. Wrong-base pass rates are among the most common defects in test reporting, and you are the person who catches them.

**Question 2 (easy) — Defects per thousand executions**

A team ran 4,000 test executions in a release cycle and raised 26 defects from them. What is the defect find rate per 1,000 executions?

- A) 5.2
- B) 6.5
- C) 7.2
- D) 9.6

**Correct answer: B**

**Explanation:** Rate per 1,000 = (26 ÷ 4,000) × 1,000 = 26 ÷ 4 = 6.5 defects per 1,000 executions. The shortcut: dividing by 4,000 and multiplying by 1,000 is simply dividing by 4. Normalised rates like this are the honest way to compare teams or releases of different sizes — 26 defects from 4,000 executions and 13 defects from 2,000 executions are the same find rate, not evidence that one team "found twice as many defects". When you coach teams in using defect data, insisting on normalised rates before comparisons is one of the simplest and most powerful standards you can set: raw counts reward big teams and long cycles, while rates reveal actual signal.

**Question 3 (easy) — Automation coverage percentage**

Your regression pack contains 900 test cases, of which 585 are automated. Your improvement plan targets 75% automation coverage of the pack. How many additional test cases must be automated to hit the target, assuming the pack size stays constant?

- A) 60
- B) 75
- C) 90
- D) 135

**Correct answer: C**

**Explanation:** Target count = 75% of 900 = 0.75 × 900 = 675 automated cases. Currently automated: 585. Additional needed = 675 − 585 = 90. Check the current position: 585 ÷ 900 = 65%, so you need to move 10 percentage points, and 10% of 900 is 90 — the same answer by a second route. Option D (135) is 15% of 900, a slip from subtracting 585 from 720 (80% target); option A comes from using 10% of 600. Two habits matter here: convert percentage targets into absolute counts before planning work, and note the assumption stated in the stem — "pack size stays constant". In real automation programmes the pack grows while you automate, so a static target count understates the work; assessments reward using the stated assumption, and your planning practice should reward making such assumptions explicit.

**Question 4 (moderate) — Percentage change in escaped defects**

Escaped defects — defects found in live rather than in testing — numbered 40 in the previous quarter and 26 in this quarter. What is the percentage change, and how should it be reported?

- A) A fall of 14%, reported as "escaped defects down 14%"
- B) A fall of 35%, reported as "escaped defects down 35%"
- C) A fall of 54%, reported as "escaped defects nearly halved"
- D) A fall of 65%, reported as "escaped defects down two-thirds"

**Correct answer: B**

**Explanation:** Percentage change = (change ÷ original) × 100 = ((40 − 26) ÷ 40) × 100 = (14 ÷ 40) × 100 = 35%. The original (earlier) quarter is always the base for a change over time. Option A reports the absolute fall (14 defects) as if it were a percentage — a category error that appears constantly in hurried reporting. Option C divides the change by the *new* value (14 ÷ 26 = 54%), inflating the improvement; option D divides the new value by the old and misreads the result. When you influence improvements to quality processes informed by defect trends, this is the exact calculation you will present to a board — and presenting 35% as "down 54%" would be the kind of error that, once spotted, undermines confidence in every other number in your pack. Compute change ÷ original, every time, and say the base aloud in your report: "down 35% on last quarter's 40".

**Question 5 (moderate) — Weighted average resolution time**

Defects resolved this month, by severity, with mean resolution times: severity 1: 4 defects at 1.5 days; severity 2: 16 defects at 3 days; severity 3: 30 defects at 6 days. What is the overall mean resolution time across all defects, to one decimal place?

- A) 3.5 days
- B) 4.2 days
- C) 4.7 days
- D) 5.0 days

**Correct answer: C**

**Explanation:** A weighted average multiplies each group's mean by its count, sums, and divides by the total count. Total defect-days = (4 × 1.5) + (16 × 3) + (30 × 6) = 6 + 48 + 180 = 234. Total defects = 4 + 16 + 30 = 50. Mean = 234 ÷ 50 = 4.68 ≈ 4.7 days. Option A is the unweighted average of the three means ((1.5 + 3 + 6) ÷ 3 = 3.5) — the classic mistake, which ignores that severity 3 defects dominate the volume. The gap between 3.5 and 4.7 is not academic: if your service-level target is "mean resolution within 4 days", the unweighted figure says you are comfortably meeting it and the weighted figure says you are missing it. When suppliers or teams present "average of averages" figures, recompute the weighted version before you accept the conclusion — that is what supporting others in assessing defects across the organisation looks like in numeric form.

**Question 6 (moderate) — Execution burn-down feasibility**

Ten working days remain in the system test window. The plan requires 1,080 test executions in that time. Your team of 6 testers currently averages 15 executions per tester per day. Environment maintenance will make the environment unavailable for 2 of the 10 days. Can the plan be completed, and what is the shortfall or surplus in executions?

- A) Yes, with a surplus of 120 executions
- B) No, with a shortfall of 180 executions
- C) No, with a shortfall of 360 executions
- D) Yes, exactly on target

**Correct answer: C**

**Explanation:** Available days = 10 − 2 = 8. Daily capacity = 6 testers × 15 executions = 90 executions per day. Total capacity = 8 × 90 = 720 executions. Required: 1,080. Shortfall = 1,080 − 720 = 360 executions. Option B is the trap for candidates who forget the environment outage: 10 days × 90 = 900 capacity gives a shortfall of only 180, half the true figure. Option A comes from misreading the execution rate as 20 per tester per day (10 × 6 × 20 = 1,200, a surplus of 120). The role-relevant reasoning starts where the arithmetic ends: a 360-execution shortfall is one-third of the plan, which no amount of exhortation will close. Your realistic options are the ones your framework names — change the approach based on effort and risk (prioritise the highest-risk third of the pack), add capacity, recover the maintenance days, or move the date — and the burn-down arithmetic is what lets you put those options to the delivery board with numbers rather than adjectives, early enough to act.

**Question 7 (moderate) — Environment utilisation from a schedule**

A shared test environment is available 10 hours per working day, 5 days per week. Last week's bookings were: Team A 12 hours, Team B 9 hours, Team C 14 hours, and 5 hours of planned maintenance. Utilisation is defined as booked hours (including maintenance) as a percentage of available hours. What was last week's utilisation?

- A) 70%
- B) 75%
- C) 80%
- D) 87.5%

**Correct answer: C**

**Explanation:** Available hours = 10 × 5 = 50. Booked hours = 12 + 9 + 14 + 5 = 40. Utilisation = 40 ÷ 50 = 0.8 = 80%. Option A (70%) comes from excluding maintenance despite the definition explicitly including it — a reminder to compute against the definition as given, not the definition you might prefer. Option D (87.5%) uses a 40-hour week as the base for 35 booked hours, importing a standard working week that the stem contradicts. Two professional points follow. First, definitions drive numbers: when you set standards for environment reporting, write down what counts as "utilised", because teams will otherwise compute it three different ways. Second, interpretation: 80% utilisation of a shared environment is high — queuing theory and practical experience both say contention and schedule collisions climb steeply as you approach full utilisation, so this figure supports a capacity conversation, not congratulations.

**Question 8 (moderate) — Supplier SLA verification**

Your testing supplier's contract requires 95% of severity 2 defects to be turned around within 5 working days each month, with a service credit due if the level is missed. The supplier's monthly report states: "Severity 2 turnaround SLA: achieved — 96%." The raw data shows 80 severity 2 defects closed in the month. The supplier excluded 5 of them from its calculation as "awaiting customer information", leaving a base of 75, of which 72 were closed within 5 working days. Assuming the 5 excluded defects all breached the 5-day turnaround, what is the achievement percentage with the exclusions restored, and is the service credit due?

- A) 90.0%; a credit is automatically due
- B) 96.0%; no credit is due
- C) 94.7%; no credit is due because it rounds up to 95%
- D) 96.0% on the supplier's base but 90.0% with exclusions restored; whether a credit is due depends on whether the exclusions are contractually valid

**Correct answer: D**

**Explanation:** First the arithmetic. The supplier's figure: 72 ÷ 75 = 0.96 = 96%, correctly computed *on its chosen base*. With the 5 excluded defects restored, the base becomes 80 and, since all 5 breached, the numerator stays at 72: 72 ÷ 80 = 0.90 = 90%. So the same month's performance is either 96% (achieved) or 90% (missed by five points) depending entirely on whether those exclusions stand. That is why option D is correct: the decisive question is not arithmetic but contractual. Many contracts legitimately stop the SLA clock while a defect awaits customer information, and if such a clause exists and was correctly applied, the 96% stands; if not, the level was missed and the credit is due. Option A assumes the exclusions are invalid without checking; option B accepts the supplier's base without question; option C invents a rounding rule that no contract would contain. This is supplier management as your framework means it: verify the calculation from raw data, identify exactly what assumption the headline depends on, and take *that* — not a rival percentage — to the contract review. Boards respect a test manager who can say "the SLA claim rests on five exclusions; here is the clause that must justify them, and here is the 90% figure if it does not".

**Question 9 (challenging) — Automation business case payback**

A proposed automation investment costs £60,000 in year 1 (tooling and build effort), with automated running starting from the first cycle of year 2. The regression pack is currently executed manually 8 times per year, each manual cycle taking 30 tester-days at £400 per tester-day. Once automated, each cycle will need only 4 tester-days of triage and maintenance at the same rate. Ignoring other costs and benefits, what is the annual saving from year 2 onwards, and during which cycle of year 2 does the cumulative saving first exceed the initial investment?

- A) £83,200 per year; payback completes during the 6th cycle of year 2
- B) £83,200 per year; payback completes during the 5th cycle of year 2
- C) £96,000 per year; payback completes during the 5th cycle of year 2
- D) £41,600 per year; payback is not achieved until year 3

**Correct answer: A**

**Explanation:** Step by step. Manual cost per cycle = 30 tester-days × £400 = £12,000. Automated cost per cycle = 4 tester-days × £400 = £1,600. Saving per cycle = £12,000 − £1,600 = £10,400. Annual saving = 8 cycles × £10,400 = £83,200. For payback, accumulate cycle by cycle: after 5 cycles, 5 × £10,400 = £52,000 — still short of £60,000; after 6 cycles, 6 × £10,400 = £62,400 — the investment is exceeded. So payback completes during the 6th cycle of year 2. Option B is the near-miss trap for candidates who compute £60,000 ÷ £10,400 = 5.77 and then round *down* to "the 5th cycle": 5.77 cycles means you are still mid-way through the 6th cycle when cumulative saving crosses the line, so you must round up. Option C uses the manual cost alone (8 × £12,000 = £96,000) as the "saving", forgetting that automated cycles still cost money to triage and maintain — a flattering but false economy that real business cases commit constantly. Option D halves the true saving. In role terms, this is the payback arithmetic behind test improvement and optimisation: when you advocate for automation investment, a board will probe exactly these numbers, and a test manager who can walk through saving-per-cycle, annual saving, and honest payback timing — including the maintenance cost that enthusiasts omit — wins funding that a vaguer advocate loses.

**Question 10 (challenging) — Defect density with changed base**

Two releases are compared. Release 1: 120 defects found against 60,000 lines of changed code. Release 2: 90 defects found against 30,000 lines of changed code. A dashboard states: "Defects fell from 120 to 90 — quality improved 25%." Using defect density per 1,000 lines of changed code, what actually happened between releases?

- A) Density fell from 2.0 to 1.5 — quality improved, and the dashboard understates the improvement
- B) Density rose from 2.0 to 3.0 — a 50% increase in defect density, so the dashboard's conclusion is reversed
- C) Density was unchanged at 2.0 — the dashboard is meaningless either way
- D) Density rose from 1.5 to 2.0 — a 33% increase

**Correct answer: B**

**Explanation:** Release 1 density = 120 ÷ 60 = 2.0 defects per 1,000 lines (60,000 lines is 60 thousands). Release 2 density = 90 ÷ 30 = 3.0 per 1,000 lines. Change = (3.0 − 2.0) ÷ 2.0 = +50%. So although the raw count fell 25%, the code base being tested halved, and defect density — the like-for-like measure — rose by half. The dashboard's cheerful headline is exactly backwards. This is the "changed base" trap in its purest form: any comparison of raw counts across periods is only valid if the denominator held still, and in delivery it almost never does — code volume, test executions, team size and release cadence all move. As the leader who guides teams in using appropriate data, your standard should be that cross-release comparisons are reported as rates with the base stated, and your review question should always be "what happened to the denominator?" One caveat worth carrying into real life: density measured on *found* defects also depends on how hard you looked, so pair it with escaped-defect data before drawing strategic conclusions — a nuance that itself distinguishes tactical from strategic recommendations, as your framework does.

**Question 11 (challenging) — Capacity plan with mixed rates**

You are planning a 15-working-day test window. The scope is 1,500 executions: 900 are standard scripts averaging 20 executions per tester per day, and 600 are complex end-to-end scenarios averaging 8 executions per tester per day. You have 5 testers, all equally capable of both types. Assuming testers can split days between work types with no switching loss, how many tester-days does the scope require, and does the window suffice?

- A) 120 tester-days required; the window's 75 tester-days are insufficient — shortfall 45 tester-days
- B) 100 tester-days required; the window's 75 tester-days are insufficient — shortfall 25 tester-days
- C) 75 tester-days required; the window exactly suffices
- D) 120 tester-days required; the window's 90 tester-days are insufficient — shortfall 30 tester-days

**Correct answer: A**

**Explanation:** Compute each work type separately, because the rates differ. Standard scripts: 900 ÷ 20 = 45 tester-days. Complex scenarios: 600 ÷ 8 = 75 tester-days. Total requirement = 45 + 75 = 120 tester-days. Available capacity = 5 testers × 15 days = 75 tester-days. Shortfall = 120 − 75 = 45 tester-days. Option B comes from the blended-rate error: averaging the two rates ((20 + 8) ÷ 2 = 14) and dividing 1,500 by 14 ≈ 107, or similar — blending rates is only valid if work volumes are equal at each rate, which they are not; the slow work dominates. Note the planning insight the numbers surface: the complex 40% of the scope consumes 62.5% of the effort (75 of 120 tester-days). That asymmetry is where optimisation lives — could some end-to-end scenarios be decomposed, automated, or risk-assessed out of scope? Creating and managing multiple quality testing plans means doing this arithmetic per work type, per team, before committing dates — and a 45 tester-day shortfall found at planning time is a management decision, while the same shortfall found in week two is an incident.

**Question 12 (challenging) — Reading a percentage table with base sizes**

A quarterly quality survey asks delivery teams whether testing is engaged "early enough" in their delivery process. Results:

| Quarter | Teams responding | % answering "yes" |
|---|---|---|
| Q1 | 40 | 60% |
| Q2 | 20 | 70% |

A colleague concludes: "Positive sentiment rose from 60% to 70%, so early test involvement improved." Which statement is the strongest critique?

- A) The conclusion is sound; 70% is greater than 60%.
- B) The number of "yes" responses actually fell from 24 to 14, and the response rate halved — the Q2 sample may be unrepresentative (for example, if disengaged teams stopped responding), so the sentiment claim is unsafe without investigating who stopped responding.
- C) Percentages can never be compared across quarters.
- D) The survey should have used a 10-point scale, so the data is worthless.

**Correct answer: B**

**Explanation:** Convert percentages to counts before comparing: Q1 "yes" = 60% × 40 = 24 teams; Q2 "yes" = 70% × 20 = 14 teams. The percentage rose while the absolute number of satisfied teams fell — because the base halved. The critical risk is non-response bias: if the 20 teams who stopped responding are disproportionately the disengaged or dissatisfied ones, the survey now samples mostly the converted, and the "improvement" is an artefact of who answered. Option B captures both the arithmetic and the inferential problem, and — importantly — it prescribes investigation rather than the opposite conclusion: the data does not prove sentiment worsened either. Option C is too absolute (comparisons are fine when bases are comparable and stated); option D changes the subject. As a test manager advocating for early quality testing involvement in organisational delivery processes, survey data like this is your evidence base for change — which is precisely why you must handle its bases and biases with the same rigour you demand of defect statistics, or your advocacy will be dismantled by the first sceptical director who checks the counts.

### Preparation tips

- **Rehearse the core moves until they are automatic.** Percentage of a number, percentage change (change ÷ original), reverse percentage, weighted average, and rate normalisation (per day, per tester, per 1,000 executions) cover the overwhelming majority of questions. Ten minutes of daily drill for two weeks will make them reflexive, freeing your timed attention for interpretation.
- **Practise on your own dashboards.** Take this month's test report, cover the computed percentages, and recompute them from raw counts. Anything you cannot reproduce is either your calculation gap or the report's error — both are worth finding, and both build assessment fitness.
- **Say the base aloud.** For every percentage you compute, name its denominator: "of executed tests", "of the original quarter", "of available hours". Most planted traps are wrong bases, and naming the base defeats them almost mechanically.
- **Use the calculator for arithmetic, not for thinking.** Decide what to calculate before touching the calculator. Candidates who calculate first and think second run out of time; candidates who set up the calculation in words ("saving per cycle, times cycles, minus investment") rarely do.
- **Estimate before you compute.** A rough order-of-magnitude estimate ("about 90 per day for 8 days, so roughly 700 against a need of 1,100 — big shortfall") catches keying errors instantly, because a wrong answer will disagree with your estimate. This mirrors how you sanity-check a supplier report before diving into its detail.
- **Manage the clock like a test window.** Roughly a minute and a half per question; bank the easy ones fast, flag the long ones, return if time allows. You would never let one blocked test consume a cycle — do not let one question consume your sitting.

### Common pitfalls to avoid

- **Wrong-base percentages.** Computing pass rate on planned rather than executed tests, percentage change on the new value rather than the original, utilisation on the wrong definition of available hours. The base is where assessments hide the trap because it is where real reports hide their errors.
- **Averaging averages.** An unweighted mean of group means is only correct when group sizes are equal — and in defect data they never are. Weight by count, always.
- **Ignoring stated exclusions and assumptions.** When a stem says maintenance takes 2 days, defects were excluded from a calculation, or pack size stays constant, that clause is the question. Skimming past qualifiers is the numerical equivalent of not reading the test precondition.
- **Comparing raw counts across changed denominators.** Defect counts across releases of different sizes, survey percentages across collapsed response bases, executions across different team sizes — normalise before comparing, and ask what happened to the denominator.
- **Answer-shape traps.** Options are engineered from predictable errors: the unweighted average, the inverted ratio, the forgotten outage day. If your answer matches an option instantly but you skipped a step, be suspicious — recompute the one step you rushed.
- **Letting precision outrun validity.** A figure can be computed perfectly and still support nothing (a 70% from a halved sample; a density from found-defects only). The strongest candidates — and the strongest test managers — state what the number shows *and* what it cannot show.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment measures how accurately you understand, evaluate, and draw conclusions from written material of the kind your role requires you to process every day. Typical items present a short passage — a policy extract, a standard, a contract clause, an email chain, a report section — followed by statements you must classify as **true** (the passage guarantees it), **false** (the passage contradicts it), or **cannot say** (the passage neither guarantees nor contradicts it), together with inference questions and judgements about clear professional writing.

Typical format: an online, timed test of 15 to 25 minutes with 20 to 30 items, often adaptive, scored against a norm group. The discipline it enforces is strict: you answer from the passage alone, not from your professional knowledge. That constraint can feel artificial to an experienced practitioner, but it mirrors a real professional necessity — when you review a contract, a policy, or a defect report, what matters is what the document actually says, not what you assume it probably means.

For a test manager, verbal reasoning is a core operating skill wearing an exam costume. Consider what crosses your desk in a normal fortnight: a departmental testing policy whose exact wording determines whether your approach is compliant; a supplier contract whose clause about clock-stopping decides a service credit; defect reports whose precision (or vagueness) determines whether a developer can reproduce the issue; test strategies you must review for internal consistency before signing; emails from stakeholders that require you to distinguish what was actually promised from what was merely implied. You also produce high-stakes writing of your own — go/no-go recommendations, strategy documents, community communications — and you coach others whose reports must say exactly what the evidence supports and no more. Your framework's first-listed skill is communicating between the technical and non-technical: mediating between people, managing expectations, and moderating difficult discussions all begin with reading precisely and writing precisely.

Employers use verbal reasoning assessments for test management roles because imprecise reading at your level propagates: if you misread an exit criterion, every team following your strategy inherits the misreading. The practice questions below use passages drawn from the genres you genuinely handle.

### How this assessment maps to your role

- **True/false/cannot-say discipline** maps to **Managing, reporting and resolving defects**: a defect report must separate observed fact from hypothesis, and when you coach others in defect management you are teaching exactly the distinction between "the passage states it" and "the passage suggests it".
- **Comprehension of policy and standards extracts** maps to **Test and quality planning** and to **Designing and executing tests**: creating strategies that comply with departmental policy, and contributing to standards for test design, both require you to parse conditional, qualified, and exception-laden prose accurately.
- **Contract and SLA language** maps to your responsibility for **supplier management**: service credits, exclusions, and obligations all turn on precise wording — "shall" versus "should", "working days" versus "days", "notify" versus "agree".
- **Inference control** maps to **Test analysis**: using multiple techniques to analyse complex information to identify risks includes knowing when a conclusion is supported by the evidence and when it is merely consistent with it.
- **Clear-writing judgement** maps to **Communicating between the technical and non-technical**: choosing the clearest formulation of a technical message for a non-technical audience — without distorting it — is the writing half of your mediation skill, exercised every time you turn a defect trend into a board recommendation.

### Practice questions

**Passage 1 (for Questions 1–3).** Extract from a departmental testing policy:

"All digital services must complete accessibility testing against WCAG 2.2 AA before entering public beta. Accessibility testing must include testing with assistive technologies. Where a service uses a component from the departmental design system, that component's existing accessibility test evidence may be reused, provided the component is used without modification. Services that fail accessibility testing may enter private beta only if a remediation plan is agreed with the service owner and the accessibility lead."

**Question 1 (easy) — True, false, or cannot say**

Statement: "A service that has not completed accessibility testing against WCAG 2.2 AA is not permitted to enter public beta."

- A) True
- B) False
- C) Cannot say
- D) True only for services using the design system

**Correct answer: A**

**Explanation:** The passage states that all digital services "must complete accessibility testing against WCAG 2.2 AA before entering public beta". "Must … before" makes completion a precondition of public beta, so a service that has not completed it cannot (compliantly) enter public beta — the statement is a direct restatement of the rule in contrapositive form. Notice what makes this easy but instructive: the statement does not add anything to the rule, it only rephrases it. Distractor D invents a qualification found nowhere in the text — the design-system provision concerns *reuse of evidence*, not exemption from the rule. Reading conditionals accurately, including their contrapositives, is the same skill you use when checking whether a team's planned gate sequence complies with policy.

**Question 2 (easy) — True, false, or cannot say**

Statement: "A modified design system component's existing accessibility test evidence may be reused."

- A) True
- B) False
- C) Cannot say
- D) True, provided the modification is small

**Correct answer: B**

**Explanation:** The passage permits reuse "provided the component is used without modification". A modified component fails that condition, so the permission does not apply — the statement contradicts the passage as written, making it false. Option D is tempting because it reflects how such policies are often applied pragmatically in real life ("minor changes are fine"), but the passage contains no smallness threshold, and importing one is exactly the error verbal reasoning tests punish. The professional parallel is direct: when a team asks you whether their tweaked autocomplete component "still counts", the policy answer is no — reuse of evidence requires an unmodified component — and whatever flexibility exists must come from the policy owner, not from your generous reading. Test managers who read entitlements narrowly and escalate ambiguity protect their programmes from compliance surprises.

**Question 3 (moderate) — Inference within limits**

Statement: "A service that fails accessibility testing can never enter private beta."

- A) True
- B) False
- C) Cannot say
- D) True, unless the service owner objects

**Correct answer: B**

**Explanation:** The final sentence explicitly provides a route: a failing service "may enter private beta only if a remediation plan is agreed with the service owner and the accessibility lead". So entry to private beta after failure is possible — under a stated condition — and "can never" contradicts the passage. Read the logical shape carefully: "may … only if" states a *necessary* condition (no agreed plan, no private beta), not a guarantee that a plan secures entry; but the statement under test claims impossibility, and the passage's provision of any permitted route falsifies it. Candidates who conflate "only if" with "if" often wobble here; the question only requires you to see that a door exists, not that it always opens. Contract clauses, gate criteria and exit criteria constantly use "only if" constructions — parsing necessary versus sufficient conditions is a daily test-management skill.

**Passage 2 (for Questions 4–6).** Extract from a testing supplier's contract schedule:

"The Supplier shall provide a minimum of four test engineers for the duration of each agreed test cycle. Where the Authority postpones a scheduled test cycle with fewer than ten working days' notice, the Supplier may invoice fifty per cent of the cycle's agreed cost. The Supplier shall notify the Authority of any planned substitution of named personnel at least five working days in advance. Substitution of named personnel does not require the Authority's approval, but the Authority may raise an objection, which the parties shall discuss in good faith."

**Question 4 (moderate) — True, false, or cannot say**

Statement: "If the Authority postpones a test cycle with three working days' notice, the Supplier is entitled to invoice half of the cycle's agreed cost."

- A) True
- B) False
- C) Cannot say
- D) False, because three days is too short a period for any invoicing

**Correct answer: A**

**Explanation:** The clause grants the entitlement whenever postponement occurs "with fewer than ten working days' notice". Three working days is fewer than ten, so the condition is met and "the Supplier may invoice fifty per cent" — an entitlement, precisely as the statement says ("is entitled to"). Note the verb: "may invoice" creates a right, not an obligation; the statement correctly claims entitlement rather than claiming the supplier *will* invoice, so it is true. If the statement had said "the Supplier must invoice", the answer would be false. This is the level of granularity at which supplier management operates: as the person responsible for supplier relationships, the difference between "may", "shall" and "must" in a schedule is the difference between a negotiable position and a contractual fact — and between budgeting for a credit and being surprised by an invoice.

**Question 5 (moderate) — True, false, or cannot say**

Statement: "The Supplier must obtain the Authority's approval before substituting a named test engineer."

- A) True
- B) False
- C) Cannot say
- D) True, if the Authority objects

**Correct answer: B**

**Explanation:** The passage is explicit: "Substitution of named personnel does not require the Authority's approval". The supplier's obligations are notice (five working days) and good-faith discussion if an objection is raised — neither amounts to an approval requirement. The statement therefore contradicts the passage: false. Option D misreads the objection mechanism as a veto; the clause requires only discussion "in good faith", and the outcome of that discussion is not specified. This distinction bites in real supplier management: test managers sometimes believe they can block a substitution when their contract gives them only a right to be heard. Knowing exactly which lever you hold — approval, objection, or mere notification — determines how you play a staffing concern: with a veto you can refuse; with an objection right you must persuade, escalate commercially, or build the concern into the next contract renewal.

**Question 6 (moderate) — Inference from silence**

Statement: "If the Supplier provides only three test engineers for a cycle, the Authority is entitled to a service credit."

- A) True
- B) False
- C) Cannot say
- D) True, because breaching a 'shall' clause always triggers credits

**Correct answer: C**

**Explanation:** Providing three engineers would breach the "shall provide a minimum of four" obligation — the passage makes the breach clear. But the statement claims a specific *remedy*: a service credit. The extract mentions no credit regime at all; remedies for under-staffing are simply not covered in the quoted text. The breach is established; the consequence is not — so the correct classification is cannot say. Option D invents a general legal rule that does not exist ("shall" clauses have whatever remedies the contract specifies). This is the purest form of the cannot-say discipline: distinguish what the text establishes (breach) from what it is silent about (remedy), and resist completing the pattern from experience. In your work the same move protects you twice over — you neither promise stakeholders a credit your contract may not provide, nor let a supplier claim a protection their schedule does not contain. When the document is silent, the honest answer is "the document is silent", followed by a question to your commercial team.

**Passage 3 (for Questions 7–9).** Extract from a test lead's end-of-cycle report to you:

"System testing for release 4.2 closed on Thursday. Of the 312 planned tests, 298 were executed; the remaining 14, all relating to the document upload journey, were blocked throughout the cycle by an environment fault that the infrastructure team has now diagnosed. Of the executed tests, 291 passed. The seven failures raised six defects: one severity 2 (duplicate payment reference under concurrent submission) and five severity 3. The severity 2 defect has a fix in review. In my view the release can proceed, since the severity 2 fix will land before the release date and the upload journey has been stable in production for over a year."

**Question 7 (moderate) — True, false, or cannot say**

Statement: "Every planned test that went unexecuted in this cycle related to the document upload journey."

- A) True
- B) False
- C) Cannot say
- D) True, but only because the tests failed

**Correct answer: A**

**Explanation:** The report states that the remaining 14 tests — the planned-but-unexecuted ones, since 298 of 312 were executed — were "all relating to the document upload journey". The statement is a direct restatement of that sentence, so it is true. But pause on the direction of the claim, because this is where the trap lives: the passage guarantees that every *unexecuted* test was an upload test; it does not guarantee the converse, that every *upload* test went unexecuted. If the statement had read "every planned test relating to the upload journey went unexecuted", the correct answer would be cannot say — the passage never states how many upload tests were planned in total, and some may have executed successfully. Option D is false on the facts: the 14 were blocked by an environment fault, not failed. The reversal distinction is not pedantry; it changes the risk picture entirely. "All the gaps are in uploads" and "uploads are entirely untested" are different findings, and before accepting the lead's recommendation you would want to know which is true — which is exactly the question a careful reading tells you to ask. Coaching report writers to make such quantified claims unambiguous ("the 14 blocked tests were the whole of the upload coverage" or "12 further upload tests passed") is a small standard with a large payoff.

**Question 8 (moderate) — Fact versus judgement**

Which element of the report is a professional judgement rather than a reported fact?

- A) 298 of 312 planned tests were executed.
- B) The severity 2 defect has a fix in review.
- C) The release can proceed.
- D) The seven failures raised six defects.

**Correct answer: C**

**Explanation:** Options A, B and D are verifiable statements about what happened or what state things are in — counts and statuses that other evidence (the test management tool, the code review queue, the defect tracker) could confirm or refute. "The release can proceed" is a recommendation: a conclusion drawn from the facts using unstated risk judgements — that a fix "in review" will land in time, that a year of production stability substitutes for a cycle of absent coverage, that five severity 3 defects are tolerable. Separating fact from judgement is the central skill of consuming reports as a decision maker: you can accept every fact in this report and still reject its recommendation, because the judgements bridging fact to recommendation are yours to make, not the lead's. It is also the skill you coach into report writers — a good end-of-cycle report labels its recommendation as a recommendation, states the assumptions it rests on, and never launders judgement as fact. Your accountability for important release decisions means the judgement in option C is precisely the part you must interrogate rather than inherit.

**Question 9 (challenging) — Evaluating an argument**

The test lead's argument for proceeding rests on two supports: (i) the severity 2 fix "will land before the release date", and (ii) the upload journey "has been stable in production for over a year". Which is the strongest critique of this argument as stated?

- A) The argument is sound; both supports are facts.
- B) Support (i) states a future event as a certainty when the fix is only "in review", and support (ii) is evidence about the *unchanged* journey — it says nothing about whether release 4.2 changes the upload journey, which is the very thing the blocked tests would have checked.
- C) The argument fails because severity 3 defects should always block a release.
- D) The argument fails because production stability is never relevant evidence.

**Correct answer: B**

**Explanation:** Take the supports in turn. Support (i) converts a present state ("fix in review") into a future certainty ("will land") — reviews reject fixes, fixes fail verification, and dates slip, so the claim is a prediction dressed as a fact. Support (ii) is subtler: a year of production stability is genuine evidence, but only about the journey *as it currently runs*. The relevant risk is whether release 4.2 alters or interacts with the upload journey — and the 14 blocked tests existed precisely to check the journey under the new release. If 4.2 does not touch the journey, the historical evidence carries weight; if it does, the evidence is close to irrelevant. The report does not say which, so the argument has a hole exactly where the risk sits. Option C invents an absolute rule contrary to risk-based practice; option D throws away legitimately relevant evidence entirely. The pattern to carry into your work: when someone argues from historical stability, always ask whether the change under consideration disturbs the thing that was stable — that question is the whole difference between evidence-based confidence and comfortable extrapolation.

**Passage 4 (for Questions 10–12).** Draft message from a test analyst, intended for a non-technical service owner, which they have asked you to review:

"Hi — quick update. The regression suite flagged intermittent 500s on the payment callback endpoint under parallel execution; we think it's a race condition in the idempotency check but haven't isolated the repro steps. Net-net, payments might occasionally duplicate under load. We're timeboxing further investigation to two days. Shout if you want to jump on a call."

**Question 10 (moderate) — Audience-appropriate rewriting**

Which rewrite best serves the non-technical service owner while preserving the substance?

- A) "The system throws HTTP 500s on the callback under concurrency; suspected race in the idempotency layer; repro unconfirmed; timeboxed spike, two days."
- B) "We have found a possible fault: in busy periods, a small number of payments could be taken twice. We are still confirming exactly when it happens and will report within two working days. Until then we recommend not increasing traffic to the service. Happy to talk it through."
- C) "There is a minor technical issue under investigation. Nothing to worry about at this stage."
- D) "Testing has identified intermittent server errors. Root cause analysis is ongoing per our defect management process."

**Correct answer: B**

**Explanation:** The service owner needs three things: what the risk means in service terms, what is being done and by when, and what they should do meanwhile. Option B translates "intermittent 500s / race condition / idempotency" into the user-facing consequence — payments could be taken twice — keeps the honest uncertainty ("possible", "still confirming"), converts the timebox into a commitment with a date, and adds an interim recommendation the owner can act on. Option A is accurate but untranslated: it moves the jargon around without crossing the technical/non-technical boundary. Option C is soothing and information-free — and "nothing to worry about" is an assurance the evidence does not yet support, which will cost credibility if duplication occurs. Option D is process language that answers none of the owner's real questions. Note what B does *not* do: it does not exaggerate, and it does not hide the uncertainty. Adopting the appropriate communication method for stakeholders at all levels — your framework's phrase — means translating consequence, not simplifying by omission. The duplicate-payment detail is exactly the substance a service owner must have, because they own the decision about traffic, comms, and contingency.

**Question 11 (challenging) — True, false, or cannot say**

Based on the analyst's draft alone, classify: "The regression suite reproduces the fault reliably under parallel execution."

- A) True
- B) False
- C) Cannot say
- D) True, because the suite flagged the fault

**Correct answer: B**

**Explanation:** The draft says the suite "flagged *intermittent* 500s" and that the team "haven't isolated the repro steps". Intermittent means the fault does not appear on every run, and unisolated reproduction steps mean the team cannot yet trigger it at will — both directly contradict "reproduces the fault reliably". The statement is false, not cannot-say: the passage provides positive evidence against reliability, rather than mere silence. Option D commits the flag/reproduce conflation: detection on some runs is not reliable reproduction, and the difference matters operationally — a reliably reproducible fault is usually days from a fix, while an intermittent one may be weeks, which changes what you tell the service owner and how you plan the timebox. When you support others in assessing complex defects, insisting on this distinction early ("can we make it happen on demand?") is one of the highest-value coaching questions you can ask, because everything downstream — fix confidence, verification strategy, release advice — depends on it.

**Question 12 (challenging) — Identifying the load-bearing sentence**

You must compress the analyst's update into one sentence for a weekly delivery report read by senior stakeholders. Which sentence preserves the decision-relevant content?

- A) "The test team is investigating an intermittent technical issue found by the regression suite."
- B) "A suspected defect could cause duplicate payments under load; confirmation is expected within two days, and mitigation advice is in place meanwhile."
- C) "Regression testing continues to add value by finding defects before release."
- D) "A race condition in the idempotency check on the payment callback endpoint is being timeboxed."

**Correct answer: B**

**Explanation:** Decision-relevant content is the content a senior reader might act on: the consequence (duplicate payments — a financial and reputational risk), its status (suspected, being confirmed), the date certainty improves (two days), and the existence of interim mitigation. Option B carries all four in one sentence. Option A reports activity without consequence — a senior reader cannot tell whether to care, which is the most common failure of upward reporting. Option C is self-congratulation, not information. Option D preserves the technical mechanism (which senior readers cannot act on) while discarding the consequence and the date (which they can). The editing principle — keep consequence, status, date, and action; cut mechanism — is the essence of speaking on behalf of your community to large audiences: you win trust for testing not by showcasing its technical depth but by making its findings effortlessly actionable. It is also reversible: when writing for engineers, the mechanism in option D becomes the load-bearing content and the consequence is context. Great test managers switch between these registers deliberately.

### Preparation tips

- **Practise the three-way classification daily.** Take one paragraph from any policy, contract or report you handle, write three statements about it, and classify each as true, false, or cannot-say strictly from the text. The cannot-say category is the one senior professionals get wrong most, because experience keeps completing the pattern — practise until silence in the text reliably triggers "cannot say" rather than a confident guess.
- **Read conditionals aloud, both ways.** "Must X before Y", "may X only if Y", "unless" — restate each as "if… then…" and then state its contrapositive. Gate criteria, exit criteria and contract clauses are nearly all conditionals, and most misreadings are conditional misreadings.
- **Underline verbs of obligation.** Shall, must, may, should, will — in any passage, mark them and ask what each one binds and whom. This single habit resolves most contract-style questions and sharpens your own drafting.
- **Separate fact, judgement and prediction as you read.** For every sentence in a report, tag it: verifiable fact, professional judgement, or prediction. Assessments test the distinction directly, and your go/no-go decisions depend on it.
- **Time-box passages, not questions.** Read the passage once, carefully (about 45 seconds), then answer its questions from targeted re-reading. Re-reading the whole passage for every question is the main time sink in verbal tests.
- **Edit something every day.** Take one of your team's status updates and rewrite it for a different audience — technical to non-technical, or the reverse. The clear-writing questions reward exactly this practised versatility, and your stakeholders will notice the difference long before any assessment does.

### Common pitfalls to avoid

- **Importing professional knowledge.** You know how testing policies, SLAs and defect workflows usually work — and the passage may differ deliberately. Answer from the text alone; flag your outside knowledge and set it aside, exactly as you would when auditing an unfamiliar team's process against *their* documented standard rather than your habits.
- **Conflating "only if" with "if".** "May enter only if a plan is agreed" makes the plan necessary, not sufficient. This single conflation accounts for a large share of wrong answers on policy-style passages — and for a fair number of real-world gate disputes.
- **Treating vividness as truth.** A concrete, plausible detail in an option (a "small modification", a "usual credit") feels true precisely because it is easy to imagine. Verbal tests weaponise plausibility; check every appealing detail against the text.
- **Missing scope words.** All, some, every, never, may, must, at least — quantifiers and modals carry the meaning. "The 14 blocked tests were all upload tests" and "all upload tests were blocked" are different claims; assessments and defect reports both hinge on such reversals.
- **Answering the argument you would have made.** On critique questions, evaluate the argument *as stated*, not the better version you could construct. The same discipline applies when reviewing a test approach: review what is written, because what is written is what the next team will follow.
- **Over-softening or over-claiming in rewrite questions.** The best answer preserves substance and uncertainty while changing register. Options that reassure ("nothing to worry about") or that merely relocate jargon are both wrong — in tests and in service-owner emails alike.

## Workplace job-specific situational judgement assessment

### About this assessment

A situational judgement test (SJT) presents realistic workplace scenarios and asks you to evaluate possible responses — typically identifying the most effective and least effective actions, ranking all the options, or rating each option's effectiveness on a scale. Unlike the cognitive, numerical and verbal assessments, an SJT has no arithmetic and no passage to parse: it measures professional judgement — the ability to weigh competing pressures (delivery deadlines, quality risk, relationships, integrity, people development) and choose actions that serve users, teams and the organisation at once.

Typical format: 12 to 25 scenarios, often untimed or generously timed, sometimes accompanied by a personality-style questionnaire. Scoring is usually against a key agreed by subject-matter experts and calibrated to the target role's level — which matters for you, because at test manager level the scored behaviours are leadership behaviours: setting direction, coaching rather than rescuing, escalating with evidence, protecting integrity of quality information, managing suppliers commercially but fairly, and communicating hard messages early. An action that would score well for a test analyst ("raise it with your test manager") may score poorly for you, because you *are* the escalation point, and the assessment wants to see you exercise the authority and ownership your role carries.

For a test manager, the SJT is arguably the most job-relevant assessment of the four. Your framework describes a role that takes ownership of delivery, creates strategy and leads implementation, makes important decisions in the delivery environment, manages stakeholder expectations, moderates difficult discussions about high-risk topics under constrained timescales, takes responsibility for talent and succession, and manages suppliers. Every one of those is a judgement domain, not a technique domain. The scenarios below are built from the recurring dilemmas of the role: release pressure against open risk, supplier performance conversations, coaching struggling team members, defending evidence without becoming adversarial, and advocating for quality practices across an organisation that does not always want to hear it.

Two general principles will serve you throughout. First, strong answers usually address the substance, the system and the relationship together — fix the immediate risk, improve the process that allowed it, and preserve the working relationship, in that order of visibility. Second, weak answers usually share one of three shapes: avoidance (hoping the problem resolves itself), unilateral force (winning the point while losing the partnership), or integrity trades (adjusting evidence to ease a conversation). Watch for these shapes in the options — and in your own instincts.

### How this assessment maps to your role

- **Release-pressure scenarios** map to your accountability to **make important decisions relating to test within the context of the delivery environment**: go/no-go moments compress risk appetite, evidence, and stakeholder pressure into a single call, and the SJT tests whether you hold evidence steady while helping delivery find a safe path.
- **Difficult-conversation scenarios** map to **Communicating between the technical and non-technical**: managing stakeholder expectations and moderating difficult discussions about high-risk topics, even within constrained timescales, is tested through options that vary in candour, timing and empathy.
- **Coaching and delegation scenarios** map to **Test analysis**, **Designing and executing tests** and **Managing, reporting and resolving defects** — each of which, at your level, is expressed through *leading and coaching others* rather than doing the work yourself; the SJT probes whether you develop people or quietly replace them.
- **Supplier scenarios** map to your responsibility for **supplier management**: fair, evidence-based, commercially aware handling of underperformance, with relationships managed but never at the price of the service.
- **Talent and succession scenarios** map to your responsibility for **talent and succession planning**: single points of failure, growth opportunities, and honest performance conversations.
- **Advocacy and adoption scenarios** map to **Test and quality planning** — advocating for early quality testing involvement in organisational delivery processes and leading multiple teams in adopting strategy — and to your potential duty to **promote and advocate test capabilities internally and outside government**.

### Practice questions

**Question 1 (moderate) — Release pressure against an open severity 2**

A programme board meets tomorrow to approve a public release. Exit criteria require no open severity 2 defects; one remains open — intermittent duplicate notifications affecting roughly 2% of users in test conditions. The delivery manager, under ministerial deadline pressure, says: "It's only notifications, nobody's harmed. Mark it severity 3 and we're compliant."

- Option A: Refuse to discuss reclassification and inform the board the exit criteria are failed, recommending the release be stopped.
- Option B: Keep the defect at severity 2 with the evidence documented, and bring the board a risk-based recommendation: the criteria are not met, here is the user impact, here are the options — release with a documented waiver, monitoring and a fix date; or delay; with your professional recommendation and the decision recorded at the right level.
- Option C: Agree to reclassify — the delivery manager owns delivery, and 2% of notifications is genuinely minor.
- Option D: Reclassify to severity 3, but note privately in the test records that you disagreed.

**Most effective: B. Least effective: D.**

**Explanation:** The severity classification is evidence: it records observed impact against agreed definitions, and it must not move because a deadline is near. But holding the evidence steady does not mean forcing a "no" — exit criteria commonly provide waiver routes precisely so that accountable owners can accept documented risk knowingly. Option B protects the integrity of the classification, translates the defect into user impact the board can weigh, and routes the decision to the accountable level with options rather than ultimatums — exactly what owning quality strategy within a risk-based approach means. Option A protects integrity but abandons your mediation role; boards deserve options and a recommendation, not a verdict from testing, and "testing stops releases" is a reputation that will cost your community influence for years. Option C trades evidence for comfort and teaches every future deadline that severity is negotiable. Option D is the least effective: it corrupts the official record while preserving a private conscience note — combining the harm of C with documented awareness that you knew better. If the reclassification later surfaces in an incident review, option D's paper trail shows the quality function falsifying its own data. The durable pattern: never trade the evidence; always help with the decision.

**Question 2 (moderate) — The underperforming supplier mid-cycle**

Halfway through a critical test cycle, your supplier's daily execution rate is 40% below the plan they committed to. Their on-site lead says the shortfall is due to "environment instability", but your own teams using the same environment are on plan. The contract review is six weeks away; the cycle ends in two.

- Option A: Wait for the contract review and present the shortfall data there, where commercial levers are available.
- Option B: Raise it informally with the on-site lead and accept the environment explanation — maintaining the relationship matters most mid-cycle.
- Option C: Meet the supplier's delivery manager now with the comparative data (their rate versus your teams' on the same environment), require a recovery plan within two days, agree what support they need, and put the episode formally on the contract review agenda.
- Option D: Redistribute the supplier's remaining scope to your own teams so the cycle recovers, and reduce the supplier's future allocations without discussing it.

**Most effective: C. Least effective: A.**

**Explanation:** Two clocks are running: the cycle ends in two weeks (a delivery problem now) and the contract review is in six (a commercial process later). Option C acts on the right clock: it confronts the performance gap immediately, with evidence that neutralises the offered excuse — the comparative rate on the same environment is precisely the data that turns an argument into a conversation — while remaining collaborative (what support do they need?) and preserving the commercial record for the review. That is supplier management as your framework intends: fair, evidence-led, and consequential. Option A is the least effective because it sacrifices the cycle to bureaucratic tidiness: six weeks of continued shortfall, a possibly failed cycle, and a review conversation about damage already done — escalation routes exist to serve delivery, not to replace timely management. Option B accepts an explanation your own data refutes, which is not relationship management but conflict avoidance, and it signals that under-delivery goes unchallenged. Option D fixes the cycle at your teams' expense and silently punishes the supplier — no recovery opportunity, no record, no learning — storing up both delivery dependence and a commercial dispute. Strong supplier handling pairs candour now with process later.

**Question 3 (moderate) — The struggling test lead's report**

A test lead you manage circulated an end-of-cycle report to a delivery board containing a pass rate computed on the wrong base and a GREEN status contradicted by their own defect table. A programme manager spotted it and emailed you, copying their director, calling the report "unreliable". The board meets again in four days, expecting a corrected report.

- Option A: Correct the report yourself tonight, send it out under your name, and tell the test lead to be more careful next time.
- Option B: Work through the errors with the test lead within a day, have *them* produce and present the corrected report, reply to the programme manager and director acknowledging the errors and the correction under way — and then introduce a peer-review step for board-bound reports across your teams.
- Option C: Reply defending the report — the underlying testing was sound and the errors are presentational.
- Option D: Ask the test lead to recheck the report and resend it, without discussing the wider criticism or informing the board of specifics.

**Most effective: B. Least effective: C.**

**Explanation:** Three things need repairing: the report (substance), the reporting process (system), and the board's confidence plus the test lead's development (relationships). Option B repairs all three: correcting *with* the lead — not for them — turns the failure into coaching, having them present the correction rebuilds their credibility rather than confirming their unreliability, the acknowledgment to the stakeholders is prompt and undefensive, and the peer-review step converts one team's error into an organisational improvement — your test improvement and optimisation duty in action. Option A feels responsible but develops nobody, signals to the board that the lead cannot be trusted, and makes you the single point of quality for every future report — an unsustainable leadership pattern. Option D is quiet remediation without learning: the same error class will recur, and the stakeholders' stated concern goes unaddressed, which reads as evasion. Option C is the least effective: defending erroneous quality data is self-disqualifying — your function's entire value rests on its numbers being trustworthy, and "the errors are only presentational" tells every stakeholder that your standards bend when your team is criticised. Nothing costs a quality leader more credibility than defending indefensible data.

**Question 4 (moderate) — Adoption resistance to the new strategy**

You have introduced a risk-based test strategy across six delivery teams. Five have adopted it. The sixth — the highest-performing team by delivery metrics — refuses, saying "our approach works; your strategy adds paperwork". Their delivery manager backs them. Your mandate from the QAT head is organisation-wide adoption.

- Option A: Instruct the team to comply, citing your mandate, and report them to the QAT head if they refuse.
- Option B: Exempt them — they are high-performing, and forcing the issue would cost goodwill.
- Option C: Spend time with the team to understand their approach in practice; identify what their method already achieves against the strategy's intent, adapt the strategy where their practice is genuinely better, and agree the minimum changes needed for the risks the strategy exists to control — bringing their delivery manager into the framing.
- Option D: Quietly arrange for the next audit cycle to focus on the team, so non-compliance is surfaced independently.

**Most effective: C. Least effective: D.**

**Explanation:** Leading and guiding multiple teams in adopting quality testing strategy — your framework's wording — is an influence task, not an enforcement task. Option C treats resistance as information: a high-performing team's objection may reveal that parts of your strategy genuinely are overhead, and a strategy improved by contact with strong practice gains credibility everywhere ("they adapted it with our best team" is the adoption story you want circulating). It also separates the negotiable (methods) from the non-negotiable (the risks that must be controlled), which is what strategy ownership actually requires — outcomes held firm, means held flexibly. Option A may achieve surface compliance but converts your best potential advocates into permanent opponents and spends the QAT head's authority on something influence could have won. Option B trades organisational consistency for comfort and creates a precedent every other team will cite — strategies with negotiable applicability stop being strategies. Option D is the least effective: engineering an audit ambush is manipulative, will be recognised as such (audit planning is rarely as confidential as people hope), and poisons both your relationship with the team and the audit function's independence. Influence that must be exercised through traps is not influence — and at your level, the assessment is measuring whether you know the difference.

**Question 5 (challenging) — The director who wants the dashboard "simplified"**

You produce a monthly quality dashboard for the digital directorate. Ahead of a spending review visit, a director asks you to remove the "escaped defects" panel for the next two months, saying: "It invites questions we don't have time to answer, and the trend is improving anyway."

- Option A: Remove the panel as asked — the director owns the audience, and the trend genuinely is improving.
- Option B: Keep the panel but change its presentation as a compromise: show a rolling average that smooths the recent spike.
- Option C: Keep the panel, and offer the director something better: a one-line context note under the panel explaining the improving trend and the actions driving it, plus a pre-briefed answer for likely questions — so the data stays whole and the director walks in prepared rather than exposed.
- Option D: Keep the panel and copy the QAT head into your refusal so the pressure is on record.

**Most effective: C. Least effective: A.**

**Explanation:** The director's underlying need is legitimate — not to be ambushed by questions during a high-stakes visit. The request's form — removing unwelcome data — is not. Option C separates the two: it solves the director's actual problem (preparedness) while keeping the quality record intact, and it reframes the escaped-defects panel from liability to evidence of a managed improvement — which, with an improving trend, it genuinely is. This is managing stakeholder expectations and moderating a difficult discussion in your framework's sense: you neither capitulate nor confront; you help. Option A is the least effective: selectively removing measures when senior visitors appear converts your dashboard from evidence into public relations, and once stakeholders learn panels vanish under pressure — and they do learn — every panel loses its evidential value permanently. Option B is subtler but still shading: choosing a smoothing method *because* it hides a spike is presentation engineered to mislead, and a numerate reviewer who spots the method change will ask why. Option D escalates before attempting resolution — if the director insists after your option-C offer, then involving the QAT head is right; leading with an on-record refusal turns a solvable conversation into a conflict and signals that you manage upwards by memo. Integrity plus helpfulness beats integrity alone.

**Question 6 (challenging) — Succession and the departing automation engineer**

Your strongest automation engineer — the only person who fully understands the framework underpinning nightly regression for four services — hands in their notice: four weeks remain. The same week, a delivery manager asks that they spend those weeks building automation for a new service "while we still have them".

- Option A: Agree — maximum value from a scarce skill while it lasts; the framework is stable and documentation can wait.
- Option B: Decline the new work; dedicate the four weeks to structured handover: pairing with two named successors on the existing framework, documenting its architecture and failure modes, prioritised by what would hurt most if it broke — and use the resignation as evidence in your case to fix the single-point-of-failure pattern across your teams.
- Option C: Split the time evenly between the new automation and handover.
- Option D: Ask the engineer to choose how to spend their notice period, since they know the systems best.

**Most effective: B. Least effective: A.**

**Explanation:** Taking responsibility for talent and succession planning — named in your role — means the scarce resource here is not four weeks of building; it is four weeks of *transferable understanding* that disappears on their last day. Option B spends the time on the only thing that cannot be bought later: knowledge transfer, prioritised by operational risk, into named people rather than into documents alone (pairing transfers the unwritten knowledge that documentation always misses). Its final move — converting the incident into a systemic case about key-person risk — is what distinguishes a leader from a scheduler. Option A is the least effective: it maximises short-term output while accepting that, from week five, four services' nightly regression depends on a framework nobody understands — the certain cost is deferred, invisible, and larger than the new automation's value; this is exactly the trade that produces 2 a.m. incidents months later. Option C halves an already insufficient handover for a task that any future engineer could do — the asymmetry (only the leaver can transfer their knowledge; many people can build new automation) makes even splits irrational. Option D abdicates a management judgement to someone with no stake in the aftermath; leavers, however excellent, optimise for interesting work and a graceful exit, not for your operational risk. Succession planning is precisely the duty not to discover key-person risk at resignation — but having discovered it, spend the notice period on nothing else.

**Question 7 (moderate) — Developers bypassing defect management**

You learn that developers on one team have been fixing defects found in system test directly with testers over chat, without records: "It's faster, and the defect process is admin." Cycle reports from that team show suspiciously low defect counts, which the delivery manager has been citing as evidence of high quality.

- Option A: Insist every past chat-fixed defect be retrospectively logged before any further testing proceeds.
- Option B: Say nothing — defects are being fixed quickly, which is the outcome that matters.
- Option C: Acknowledge to the team that fast collaboration is genuinely good, then fix the two real problems: agree a lightweight capture route (a one-line record per chat-fix, integrated with their workflow) so trends and reporting stay truthful, and correct the record with the delivery manager — the team's defect counts understate discovery, so the "high quality" narrative needs revising.
- Option D: Correct the delivery manager's narrative at the next programme board, using the chat logs as evidence, so the reporting distortion is exposed and deterred.

**Most effective: C. Least effective: D.**

**Explanation:** Two distinct things are happening: a genuinely healthy behaviour (developers and testers collaborating to fix fast) and a genuinely harmful one (quality data silently losing its meaning — the trend analysis you use for tactical and strategic recommendations is being starved, and a false quality narrative is reaching decision makers). Option C keeps the health and fixes the harm: leading and coaching others in improving defect management processes, in your framework's words, means adapting the process to the team's flow — a one-line capture that costs seconds — rather than defending process weight for its own sake, and it means correcting the record with the delivery manager directly, privately, and promptly. Option A punishes the collaboration, buries the team in retrospective admin of limited value, and teaches everyone to hide workarounds from you rather than surface them. Option B accepts the speed and ignores that escaped-trend data, coverage judgements and the delivery manager's citations are all now built on false counts — the damage is invisible until a strategic recommendation fails. Option D is the least effective: a public ambush at a board, with chat logs as exhibits, humiliates the delivery manager and the team, converts a fixable process gap into a political incident, and makes you the person who surveils rather than the person who improves. Correct records, yes — public prosecution, no.

**Question 8 (moderate) — The conference invitation during a delivery crunch**

You are invited to speak at a cross-government QAT community event in three weeks about your department's risk-based testing approach — a genuine opportunity to advocate test capabilities beyond your organisation, which your role encourages. But your teams are mid-way through the most difficult release of the year, and preparation would take about two days.

- Option A: Decline — delivery always outranks community activity, and the timing is bad.
- Option B: Accept without adjusting anything, and prepare during evenings so neither commitment is visibly affected.
- Option C: Assess honestly whether two days can be made safe: if yes, accept, delegate a named deputy for the release period with clear escalation triggers, and treat the deputising itself as a development opportunity; if no, decline this instance but propose a colleague or a later slot so the community relationship is kept warm.
- Option D: Accept, and have a member of your team write the talk and handle the preparation, since the release needs your attention.

**Most effective: C. Least effective: B.**

**Explanation:** This scenario tests whether you treat competing goods as a judgement to be made rather than a rule to be applied. Option C does the actual work of the decision: it weighs the release's real (not assumed) need for you across two specific days, uses delegation as both a coverage mechanism and a succession-planning investment — a deputy who runs a hard release fortnight with clear escalation triggers grows more in two weeks than in a year of shadowing — and, if the answer is no, declines in a way that preserves the advocacy channel. Both branches of C are defensible; what scores is the deliberate assessment and the protected relationships. Option A applies a rule instead of judging: "delivery always outranks" would rationalise never doing the advocacy your role explicitly names, and community influence compounds — seats not taken are eventually not offered. Option D mistakes advocacy for content production: representing the community to external audiences is a relationship and credibility act performed by you, not a deliverable to outsource to someone who will neither present it nor own its questions (though *co-presenting* with a rising team member would have been a strong variant). Option B is the least effective because it is the abdication dressed as heroism: unexamined acceptance funded by unsustainable hours, with no deputy, no escalation plan, and degraded judgement mid-release — the failure mode where both commitments suffer and nobody was told a trade-off existed. Leaders make trade-offs visible; they do not absorb them silently.

**Question 9 (challenging) — The escaped defect and the blame meeting**

A defect has reached live: benefit award letters sent to roughly 3,000 citizens contain a miscalculated repayment date. At the incident review, the service owner opens with: "Testing signed this release off — I want to understand how your team missed it." You know the defect arose in a code path changed after the regression pack was last updated, and that your team's request for two extra days to extend the pack was declined by the programme at planning.

- Option A: Present the timeline factually: the code path changed after the pack was updated, the extension request was declined — so the miss traces to the programme's decision, not testing's execution.
- Option B: Accept accountability for the gap on behalf of the quality function, then move the review to mechanism and prevention: how the change-to-coverage gap opened, the full timeline including the declined extension presented as learning rather than blame, the citizen-facing fix and comms as first priority, and a proposed control (coverage impact assessment for late changes) so the class of miss is closed.
- Option C: Note that no test approach guarantees zero escapes, and that a 99.98% accuracy rate across letters is within any reasonable quality tolerance.
- Option D: Say the team will review internally and report back, avoiding any positions in the meeting itself.

**Most effective: B. Least effective: C.**

**Explanation:** Incident reviews are where a quality leader's character is most visible. Option B does the hard things in the right order: it absorbs the accountability that comes with having signed off (ownership first — you cannot lead quality while deflecting quality failures), returns the room to mechanism rather than fault, surfaces the declined-extension fact as system learning — it *is* relevant, and suppressing it would be as distorting as weaponising it — keeps the harmed citizens at the top of the agenda, and leaves the review with a control that closes the gap class. That combination — own, explain, fix, prevent — is what moderating a difficult, high-risk discussion means in practice. Option A contains the same facts as B but deploys them as a counter-accusation; it may be forensically accurate and it will still read as "testing blames the programme", entrenching the adversarial frame the service owner opened with and burying the prevention conversation. The facts belong in the room; the framing decides whether they teach or convict. Option D defers what the room needs now — someone taking ownership — and reads as evasion under fire. Option C is the least effective: statistically framing away 3,000 citizens receiving wrong financial information is tone-deaf to user harm (the framework's user focus is not a percentage), insults the service owner's legitimate concern, and hands anyone who wants one a quotation proving the quality function does not take quality seriously. Never minimise citizen impact to win a meeting.

**Question 10 (challenging) — Late-engaged testing and the fixed deadline**

A programme approaches you eight weeks before a legally mandated go-live date, asking you to "arrange testing" for a service that has been in build for five months with no test involvement: no testability review, no test environments, no requirements traceability. Your rapid assessment says a responsible test approach needs twelve weeks. The legal deadline cannot move.

- Option A: Take the engagement and compress the twelve weeks into eight by running everything in parallel and asking teams for overtime; flag the compression informally to the programme manager.
- Option B: Decline the engagement as set up: testing cannot assure the service in the time available, and taking it on would make the quality function complicit in the outcome.
- Option C: Accept the reality and reshape the ask: agree with the programme's SRO a risk-based scope for eight weeks — the legally critical journeys and highest-harm risks first — with an explicit, written statement of what will not be covered by go-live and the residual risk this leaves, a post-go-live completion plan for the remainder, and a lessons-learned commitment that future programmes engage testing at discovery, which you then pursue through the delivery assurance process.
- Option D: Escalate to the QAT head to negotiate with the programme's director, and hold engagement until the governance question of late involvement is resolved.

**Most effective: C. Least effective: B.**

**Explanation:** The deadline is legally fixed, the past is unrecoverable, and the citizens who will use this service on day one are the stakeholders with the most at stake and no voice in the room. Option C serves them: risk-based scoping under genuine constraint is your test analysis skill at full stretch — determining what adds most value, ensuring the highest harms are mitigated first — while the written residual-risk statement keeps the accountability honest: the SRO accepts known, documented risk instead of enjoying imagined assurance. The forward-looking move — turning this programme into the case study that drives earlier engagement — is advocating for early quality testing involvement in organisational delivery processes, your framework's exact phrase, pursued through governance rather than grievance. Option B is the least effective: refusal maximises the harm to users (the service launches with *no* professional testing rather than eight risk-based weeks) while protecting only the quality function's reputation — quality leadership that walks away from constrained situations is decorative, and "complicity" is avoided by documenting residual risk, not by absence. Option A accepts the ask without reshaping it: a silent compression with informal flagging produces the imagined assurance that option C's written statement exists to prevent — when escapes occur, "testing had eight weeks and signed off" will be the record. Option D has a place — the QAT head should know — but *holding engagement* while governance deliberates spends the scarcest resource, the eight weeks, on a process question that can run in parallel. Escalate and engage are not alternatives; sequencing them as alternatives is the error.

### Preparation tips

- **Answer as the role, not as yourself on a bad day.** SJTs measure your grasp of what the role's best version does. Before the test, re-read your role description — ownership of delivery, coaching, supplier management, advocacy — and let those duties frame every scenario: "what does the owner of quality strategy do here?"
- **Look for the option that fixes substance, system and relationship.** Strong options usually address the immediate risk, improve the process that produced it, and keep the working relationship intact. Options that achieve only one of the three are usually distractors.
- **Identify the least effective option by its shape.** Avoidance, unilateral force, integrity trades, public ambushes, and silent heroics are the recurring shapes of least-effective answers. Name the shape and the option identifies itself.
- **Respect the level.** At test manager level, "escalate to your manager" is rarely the strong first move — you are the manager. Equally, options where you do a struggling team member's work yourself usually score poorly: your level's verbs are coach, lead, guide, influence.
- **Rehearse your real dilemmas.** Take three difficult situations from your own last year, write four plausible responses to each, and rank them cold a week later. Discuss them with a peer test manager — calibration against another professional's judgement is the closest available rehearsal for an expert-keyed test.
- **Do not overthink toward cynicism.** Candidates sometimes reject the constructive option as "too idealistic" and choose a worldly-wise compromise. Expert keys reward the constructive option; professional standards are the scoring rubric, not office politics.

### Common pitfalls to avoid

- **Trading evidence for harmony.** Any option that adjusts severity, removes a dashboard panel, softens a score, or smooths a trend to ease a stakeholder conversation is an integrity trade, and it is nearly always the least effective or close to it. The moment quality data becomes negotiable, it stops being data.
- **Confusing escalation with action.** Escalation is a tool, not a deed. Options that escalate *instead of* acting (waiting for contract reviews, holding engagement pending governance) usually lose to options that act *and* keep governance informed.
- **Rescuing instead of coaching.** Redoing a team member's flawed work yourself protects this week's output and mortgages every future week. The scored behaviour at your level is developing the person while safeguarding the outcome.
- **Winning the room, losing the relationship.** Public corrections, audit ambushes, and evidence deployed as accusation may be factually impeccable and are still judgement failures. Ask of every option: after this action, will the other party work with me better or worse?
- **Forgetting the user.** In release-pressure and incident scenarios, options are ultimately keyed to citizen impact. Any option that reframes user harm as a percentage, a technicality, or someone else's problem is signalling itself as a wrong answer.
- **Choosing the heroic silent option.** Absorbing impossible workloads without surfacing the trade-off looks dutiful and scores badly: leadership behaviour is making constraints visible and deciding them deliberately, not hiding them in your evenings.

## Conclusion

Well done for working through this guide. You have covered a great deal of ground: the mental disciplines of a cognitive assessment — pattern recognition in defect trends, deduction from exit criteria and environment dependencies, error checking of dashboards and traceability matrices; the numerical fluency that turns pass rates, defect densities, supplier SLAs and automation business cases into trustworthy decisions; the verbal precision that parses policies, contracts and reports for exactly what they say; and the professional judgement that navigates release pressure, supplier underperformance, coaching moments, incident reviews and late-engaged programmes with integrity intact.

If one theme runs through all four sections, it is this: the assessments and your job reward the same habits. Fix the base before computing the percentage. Conclude only what the evidence guarantees. Read the qualifier, the quantifier, and the "only if". Hold the data steady and help with the decision. Address the substance, the system, and the relationship together. None of these is an exam trick — each is a behaviour you already practise as the owner of a quality testing strategy, and deliberate practice here compounds directly into sharper artefact reviews, more credible board papers, and better coaching conversations with your teams.

Be encouraged by how much of this you found familiar. As a test manager you have spent years training exactly the capabilities these assessments measure: risk-based thinking, evidence discipline, precise communication between technical and non-technical worlds, and calm judgement under delivery pressure. An assessment is simply those capabilities performed in miniature, under a clock, without your usual context. Preparation closes the gap between what you can do and what you can show — and you have now done that preparation.

A few suggestions for where to go next. Revisit the questions you got wrong in a week's time; the second attempt, after the explanation has settled, is where the learning consolidates. Practise little and often rather than in single long sessions — ten minutes of percentage drills or one true/false/cannot-say passage a day beats a weekend cram. Use your own working materials as a practice library: every dashboard, contract schedule and end-of-cycle report that crosses your desk is a potential assessment item, and treating them that way improves both your test scores and your professional output. And consider sharing this practice with your teams and the wider QAT community — coaching others through these questions is succession planning, capability building, and advocacy all at once, which is to say: it is your job, done well.

Approach any real assessment rested, unhurried, and confident in your preparation. You measure quality for a living; trust your own. Good luck — and keep practising.

---

*Professional development tip: revisit this guide periodically as your role evolves. The scenarios that feel hardest today are often the ones that map to the capabilities you are currently growing into.*




