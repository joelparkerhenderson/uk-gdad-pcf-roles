# Service Readiness Analyst - Psychometric Assessment Resources

## Introduction

Welcome! This guide has been written especially for you as a service readiness analyst working within the UK Government Digital and Data profession. Whether you are preparing for an internal assessment, applying for your next role, benchmarking your own skills, or simply curious about how psychometric tests relate to your day-to-day work, this document will help you practise steadily, understand the techniques, and walk into any assessment feeling prepared rather than nervous.

Let's start with a reassurance: psychometric assessments are not trick exams, and they are not tests of whether you are "clever enough". They are structured, standardised exercises that measure the thinking skills and workplace behaviours that predict success in a specific role. For a service readiness analyst, that means the questions use the materials you genuinely work with — test results, security checklists, change requests, risk logs, KPI reports, and readiness criteria — and the decisions you genuinely make, such as checking whether an application meets its security criteria, assessing the impact of a change, spotting a risk that needs flagging, and escalating it clearly to your service transition manager.

Why do these assessments matter for your role in particular? As a service readiness analyst, you test the products and you are accountable for application acceptance and for checking whether security criteria have been met. You are also the person who flags potential risks upward. That is a role built on careful, honest, methodical thinking. Cognitive assessments measure whether you can spot the gap in a test report or follow a security rule to its correct conclusion. Numeric assessments measure whether you can read a KPI table, work out a pass rate, or notice a trend that signals trouble. Verbal assessments measure whether you can read a security standard or a supplier's email and understand exactly what it commits to — and what it quietly does not. Situational judgement assessments measure whether you choose sensible, professional responses when there is pressure to say "it's fine" and the evidence says "not yet".

This document is organised into four main assessment sections, one for each test type. Each section follows the same friendly pattern: an overview of what the assessment measures and why employers use it for your role, a mapping from the assessment's dimensions to the specific skills in your role summary, a substantial set of practice questions with full worked explanations, practical preparation tips, and common pitfalls to avoid.

Here is how to get the most out of it. First, read each "About this assessment" section so the format holds no surprises — familiarity is the cheapest confidence there is. Second, attempt every practice question honestly: commit to an answer before reading the explanation. Third, treat the explanations as mini-lessons; even where you answered correctly, the walkthrough will hand you a technique you can reuse. Fourth, spread your practice out. Short, regular sessions beat one long slog, and they suit a working week far better.

Finally, remember that flagging what you find difficult is your professional superpower, and it applies to practice too: noticing which question types feel hardest tells you exactly where to spend your next ten minutes. Take your time, be kind to yourself, and let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive assessment measures the exact mental processes your role demands, using realistic workplace scenarios rather than abstract puzzles. Instead of shape sequences and riddles, you will see the everyday materials of readiness work — security checklists, test completion reports, risk logs, change impact notes, and release checklists — and be asked to reason quickly and accurately about them.

The typical format is an online, timed test lasting 15 to 30 minutes, usually with 15 to 30 multiple-choice questions covering pattern recognition, logical deduction, error checking, prioritisation, and applied problem solving. Scoring is objective, comparing your responses against a norm group at a similar level. Many platforms are adaptive: the questions get slightly harder as you answer correctly, so a test that feels increasingly challenging is usually a test you are doing well on. Almost all platforms offer a few ungraded practice questions first, so you can learn the interface without pressure.

Employers use cognitive assessments for service readiness roles because your professional value is systematic verification. When you check whether security criteria have been met, you are doing rule-based deduction: this control is required, is it evidenced? When you test a product against readiness criteria, you are error checking: does what was delivered match what was specified? When you decide which of today's readiness tasks to do first, you are prioritising under constraints. And when you notice that a pattern of small test failures points at one underlying cause, you are doing applied problem solving. A well-designed cognitive test rehearses all of this in miniature, which is why role-specific practice — like the questions below — transfers so directly to both the test and the job.

One encouraging fact to hold on to: cognitive test performance is trainable. The techniques in this section — verbalise the rule, eliminate what the rules forbid, check numbers, rules, and timelines separately — are habits anyone can build with practice.

### How this assessment maps to your role

The assessment dimensions map directly to the named skills in your role summary:

- **Error checking** maps to your core duty of testing products and checking whether security criteria have been met: your value to the transition is finding the mismatch between what the criteria require and what the evidence shows.
- **Logical deduction** maps to your **Change management** skill: analysing and assessing the impact of change means reasoning correctly from "this component changes" to "these services, users and controls are affected".
- **Pattern recognition** maps to your **Asset and configuration management** and **Problem management** skills: tracking and correcting information, and investigating problems in systems and services, both begin with noticing the record or result that breaks the expected pattern.
- **Prioritisation** maps to your **Ownership and topic** and **Incident management** skills: owning an issue until it is resolved or properly handed over, and allocating incidents to the appropriate channel, both require ranking what matters most, quickly and defensibly.
- **Applied problem solving** maps to your **Availability and capacity management** skill — managing service components to meet business needs and KPIs — and to your **Service focus** skill of taking inputs and establishing coherent frameworks that work.
- **Structured thinking under pressure** supports your duty to flag risks and escalate them to your service transition manager: a well-structured flag (what, evidence, impact, suggestion) is a product of clear thinking, and it is what makes escalation useful rather than alarming.

### Practice questions

**Question 1 (easy) — Pattern recognition in test case IDs**

Your test cases are numbered by module and sequence: SEC-001 to SEC-020 for security tests, PERF-001 to PERF-010 for performance tests, and FUNC-001 to FUNC-050 for functional tests. A completion report claims "all tests executed" and lists the executed IDs. You spot-check the security range and see: SEC-001, SEC-002, SEC-003, SEC-005, SEC-006 ... SEC-020. What should you conclude?

- A) All security tests were executed — the report says so.
- B) SEC-004 does not appear in the executed list, so at least one security test seems unexecuted; the claim needs checking.
- C) SEC-004 was probably renamed, so there is no issue.
- D) The functional tests were not executed.

**Correct answer: B**

**Explanation:** The security range should run unbroken from 001 to 020. The list jumps from SEC-003 to SEC-005, so SEC-004 is missing from the evidence, which directly contradicts "all tests executed". Option A trusts the summary sentence over the detail beneath it — the exact habit your role exists to avoid. Option C invents a comforting explanation with no evidence; renaming is possible, but possible is not verified, and your next step is to ask, not assume. Option D concludes something about a range you have not checked. The technique — scan a numbered sequence for gaps — takes seconds and catches real problems, and it is precisely what "checking whether criteria have been met" looks like in practice: the summary claims, the detail proves.

**Question 2 (easy) — Deduction from a security criterion**

Your security criteria state: "An application may go live only if penetration testing has been completed AND all critical findings have been remediated." The supplier reports: "Penetration testing completed on 2 June; two critical findings raised." Based only on this, may the application go live?

- A) Yes — penetration testing is complete.
- B) No — critical findings were raised, so it can never go live.
- C) Not yet determinable — you need to know whether the two critical findings have been remediated.
- D) Yes — findings are normal in penetration tests.

**Correct answer: C**

**Explanation:** The criterion has two conditions joined by AND: testing completed, and critical findings remediated. The report confirms the first and tells you findings exist, but says nothing about remediation. If both findings have since been fixed and verified, the criterion could be met; if not, it is not. So the honest answer is "not yet determinable — ask about remediation". Option A stops at the first condition. Option B misreads the criterion: findings do not forbid go-live; unremediated critical findings do. Option D is true as a generalisation and irrelevant as evidence. This is the daily grammar of your role: security criteria are usually compound conditions, and your job is to check every clause, then ask precisely for what is missing.

**Question 3 (easy) — Error checking a release checklist**

A release checklist requires: (1) code deployed to staging, (2) smoke tests passed in staging, (3) security scan run against the staging build, (4) sign-off from the readiness analyst. The log reads:

- 09:10 — Code deployed to staging (build 4.2.1)
- 09:40 — Security scan run against build 4.2.0
- 10:15 — Smoke tests passed in staging (build 4.2.1)

What is the problem?

- A) The smoke tests ran after the security scan, which is the wrong order.
- B) The security scan was run against the previous build (4.2.0), not the build being released (4.2.1).
- C) Step 4 is missing, so nothing else matters.
- D) There is no problem.

**Correct answer: B**

**Explanation:** Compare each log line against its checklist item carefully — including the details in brackets. The deployment and smoke tests both reference build 4.2.1, but the security scan references build 4.2.0: the scan evidence belongs to the wrong build, so criterion (3) is not genuinely met for this release. Option A invents an ordering rule the checklist does not state. Option C is half-true — sign-off is indeed outstanding — but sign-off is your step, and it is not yet due until the first three are sound; the blocking defect is the scan. Option D misses the version mismatch. Version and identifier mismatches are among the most common — and most dangerous — findings in readiness work: evidence that is real, recent, and about the wrong thing. Train your eye to check not just "was it done?" but "was it done to this?"

**Question 4 (easy) — Prioritising a readiness morning**

It is 9:00. Four items await you:

1. A risk you flagged yesterday needs one supporting screenshot before your service transition manager presents it at a 10:00 meeting.
2. A supplier has emailed asking you to confirm receipt of their test report "when convenient".
3. Your weekly KPI figures are due by end of day.
4. A colleague wants help interpreting a security scan result; their work is paused until you respond.

Which order is most sensible?

- A) 1, 4, 3, 2
- B) 3, 1, 4, 2
- C) 2, 1, 4, 3
- D) 4, 1, 2, 3

**Correct answer: A**

**Explanation:** Item 1 has the hardest, nearest deadline (10:00) and feeds your manager's escalation — exactly the flag-and-escalate duty your role centres on — and it is quick, so do it first. Item 4 is next: a colleague is blocked, and unblocking people ranks above tasks with end-of-day or vague deadlines. Item 3 has a real deadline but a full day to meet it. Item 2 says "when convenient" and takes one line — last, or slotted into a spare moment. Option B lets a distant deadline outrank a 10:00 one; option C leads with the least urgent item; option D helps the colleague first but at the cost of your manager walking into a meeting under-armed at 10:00 — sequencing 1 before 4 costs the colleague minutes, while the reverse costs the escalation its evidence. Rule of thumb: hard near deadlines first, then unblocking others, then soft deadlines, then courtesies.

**Question 5 (moderate) — Impact assessment logic**

Your change impact rules say: (i) any change to the authentication service affects all applications that use single sign-on; (ii) applications A, B and C use single sign-on; application D uses its own login; (iii) any application affected by a change must have its smoke tests re-run before the change is closed. A change to the authentication service was implemented last night. Which statement must be true?

- A) Application D's smoke tests must be re-run.
- B) Applications A, B and C must have their smoke tests re-run before the change is closed.
- C) All four applications must be re-tested.
- D) No re-testing is needed because the change was to a shared service, not to the applications.

**Correct answer: B**

**Explanation:** Chain the rules. Rule (i): the change affects every single sign-on application. Rule (ii): that means A, B and C — and not D, which has its own login. Rule (iii): affected applications need smoke tests re-run before closure. Therefore A, B and C must be re-tested; nothing requires D. Option C sweeps D in without support; option A picks exactly the unaffected application; option D misunderstands impact — changes to shared components affect their consumers, which is the entire reason impact assessment exists. This is your **Change management** skill ("analyse and assess the impact of change") as pure logic: follow the dependency, list the affected set precisely, and require exactly the right re-verification — no less (risk) and no more (waste).

**Question 6 (moderate) — Spotting the inconsistency in a readiness report**

A supplier's readiness report states: "User acceptance testing ran from 3 to 14 June with 25 testers. All 180 scenarios were completed. The defect log shows 42 defects raised during UAT, of which 39 are closed and 6 remain open." What is wrong?

- A) 25 testers is too few for 180 scenarios.
- B) 39 closed plus 6 open equals 45, which does not match the 42 defects raised.
- C) Twelve days is too short for user acceptance testing.
- D) Nothing is wrong.

**Correct answer: B**

**Explanation:** Check internal consistency before judging anything else: 39 + 6 = 45, but the report says 42 were raised. Three defects are unaccounted for — perhaps late additions, duplicates, or a typo, but the numbers as written cannot all be true, and your job is to query them. Options A and C criticise judgements (team size, duration) that the report's own facts neither support nor refute — you have no benchmark in the question, so they are opinions, not findings. The reconciliation habit — do the parts sum to the whole? — is one of the fastest checks in your toolkit and one of the most revealing: reports whose numbers do not reconcile often have process gaps behind them, which is exactly the kind of risk you are accountable for flagging before acceptance.

**Question 7 (moderate) — Deduction about environments**

Your standards say: (i) performance testing results are valid only if run in an environment matching production sizing; (ii) the staging environment matches production sizing; the development environment does not; (iii) results from invalid environments may be used for early indication but never for acceptance. The project offers you performance results run in the development environment, and they are excellent. What is the correct position?

- A) Accept them — excellent results are excellent results.
- B) Reject them entirely and instruct the project to delete them.
- C) Treat them as early indication only, and require a performance run in staging (or another production-sized environment) for acceptance.
- D) Accept them if the project manager confirms development is "close enough" to production.

**Correct answer: C**

**Explanation:** Apply the rules mechanically. The results come from development; rule (ii) says development does not match production sizing; rule (i) therefore makes them invalid for acceptance; rule (iii) tells you exactly what they are good for — early indication. Option C states precisely that, plus the constructive path to acceptance. Option A lets the quality of the numbers override the validity of their source — but a fast result in a small environment predicts little about production load. Option B overcorrects: the rules explicitly preserve a use for these results, and deleting data is never your call. Option D lets assertion replace the standard; "close enough" is what rule (ii) exists to settle. Notice the shape: good rules often anticipate the tempting shortcut and provide a legitimate half-way house. Knowing the rules well enough to offer that half-way house is what makes you firm and helpful at the same time.

**Question 8 (moderate) — Sequencing readiness activities**

Five readiness activities remain before go-live, with these rules: (i) security remediation verification must happen after the supplier deploys their fix, which lands Wednesday morning; (ii) the operations handover session requires the final runbook, which the project completes Tuesday; (iii) the go/no-go review is Friday and requires all other activities complete; (iv) the backup restoration test can run any day but occupies a full day of your time; (v) you can do at most one full-day activity per day, and the handover and verification are each half-day activities. Today is Monday. Which plan works?

- A) Monday: backup restoration test; Tuesday: handover; Wednesday: verification; Thursday: spare; Friday: go/no-go
- B) Monday: handover; Tuesday: backup restoration test; Wednesday: verification; Thursday: spare; Friday: go/no-go
- C) Monday: verification; Tuesday: backup restoration test; Wednesday: handover; Thursday: spare; Friday: go/no-go
- D) Monday: backup restoration test; Tuesday: verification; Wednesday: handover; Thursday: spare; Friday: go/no-go

**Correct answer: A**

**Explanation:** Test each plan against the rules. Plan A: the backup test (any day) fills Monday; the handover runs Tuesday, which works because the runbook completes that same day and the handover can follow its completion in the afternoon — the rules require the runbook to exist before the handover, and Tuesday-after-completion satisfies that. Verification runs Wednesday, after the fix lands Wednesday morning — allowed. Everything finishes before Friday's review. Plan B fails: Monday's handover precedes the runbook, which does not exist until Tuesday. Plan C fails: Monday's verification precedes Wednesday's fix. Plan D fails the same way as C — Tuesday's verification is before the Wednesday fix. Only A satisfies every dependency. In the test and at work, the method is identical: convert each rule into "X not before Y", then walk each candidate plan day by day. Scheduling by dependency, not by preference, is how transitions stay calm.

**Question 9 (moderate) — Choosing the appropriate channel**

During readiness testing you discover that a configuration file in staging contains what appears to be a live production database password. Which first action is most appropriate?

- A) Post a message in the project's open team channel asking "is this a real password?"
- B) Report it immediately through your organisation's security incident process and alert your service transition manager, so the credential can be changed and the exposure assessed.
- C) Try the password against the production database to check whether it is real.
- D) Remove the file from staging and carry on testing.

**Correct answer: B**

**Explanation:** A potentially exposed production credential is a security event, and security events have a proper channel — using it is not overreaction, it is the procedure working as designed. Option B also alerts your manager, which matches your role's escalation duty: you flag risks; the response is co-ordinated above you. Option A broadcasts the secret's existence (and location) to a wide audience — making exposure worse. Option C is the most seductive wrong answer: "verifying" by attempting access is itself unauthorised access, and readiness analysts never test live credentials against production. Option D hides the event without triggering the one action that actually reduces risk — changing the credential — and destroys evidence of what was exposed and for how long. The pattern for security discoveries: contain through the proper channel, inform the right people, never probe, never tidy up silently.

**Question 10 (hard) — Root-cause reasoning across test results**

Regression testing shows failures in four screens: case search, case summary, document upload, and audit history. You gather facts: (a) all four screens call the same shared records API; (b) the payments screen, which does not use that API, passes; (c) the records API was upgraded in this release; (d) each failing screen shows the same error: "field 'caseRef' not found". What is the best-supported conclusion and next step?

- A) Four separate screen defects; raise four unrelated bugs to four developers.
- B) The records API upgrade likely changed or removed the 'caseRef' field, breaking its consumers; raise one defect against the API with the four screens as evidence, and flag the impact to your service transition manager.
- C) The test environment is broken; re-run everything tomorrow.
- D) The payments screen is the anomaly and should be investigated first.

**Correct answer: B**

**Explanation:** Test the hypotheses against all four facts. Option B explains everything: the four failures share one dependency (a), the non-consumer passes (b), the dependency changed in this release (c), and the identical error message (d) points at a single missing field rather than four coincidental bugs. Option A ignores the shared structure and would send four teams chasing one defect. Option C explains none of the specifics — a broken environment would not produce one consistent, meaningful error only in API consumers. Option D inverts the logic: the passing screen is not the anomaly; it is the control case that strengthens the API hypothesis. The reasoning pattern — find what the failures share, find what the passes lack, connect to what changed — is classic problem investigation, matching your **Problem management** skill. And note the second half of B: one well-evidenced defect plus an upward flag about impact is exactly how a readiness analyst turns analysis into action.

**Question 11 (hard) — KPI logic with competing constraints**

A service component you manage has two KPIs: response time (95% of requests under 2 seconds) and cost (monthly infrastructure spend within budget). This month: response times meet target, but only because an engineer doubled the server count in an unrecorded change, pushing spend 40% over budget. Reversing the change would restore the budget but likely breach the response-time KPI at current demand. What is the most defensible immediate position for you to take?

- A) Keep the extra servers quietly — response time is what users feel.
- B) Reverse the change immediately — budget is budget.
- C) Flag the situation to your service transition manager: an unrecorded change is masking a genuine capacity shortfall, and the trade-off between cost and performance needs a proper decision, with the change retrospectively recorded either way.
- D) Split the difference by removing half the extra servers.

**Correct answer: C**

**Explanation:** Untangle the two problems. First, an unrecorded change exists — whatever else happens, that must be surfaced and recorded, because invisible changes corrupt every future diagnosis and audit. Second, there is a real trade-off: demand appears to have outgrown the budgeted capacity, so someone with authority over budget and service levels must choose (more budget, revised KPI, demand management, or optimisation). Options A and B each pick a side of that trade-off unilaterally and below the right level — and A additionally perpetuates concealment. Option D is engineering by compromise: without analysis, half the servers may satisfy neither KPI. Option C does what your role summary literally says: manage service components against business needs and KPIs, flag potential risks, and escalate to the service transition manager. Escalating a genuine trade-off is not indecision — it is routing a decision to where the authority lives, with the analysis attached.

**Question 12 (hard) — Building a coherent readiness framework**

You are asked to consolidate readiness checks from three sources into one checklist. Source 1 (security team): penetration test complete; critical findings remediated; credentials vaulted. Source 2 (operations): runbook delivered; monitoring configured; on-call rota agreed. Source 3 (previous project's lessons): monitoring configured; rollback tested; credentials vaulted. Requirements: include every distinct check once; group into "security", "operations", and "resilience" so that rollback testing sits under resilience; and order groups security → operations → resilience. How many distinct checks are there, and which check appears last?

- A) 9 checks; rollback tested last
- B) 7 checks; rollback tested last
- C) 7 checks; on-call rota agreed last
- D) 8 checks; credentials vaulted last

**Correct answer: B**

**Explanation:** De-duplicate first. The raw list has nine entries, but "monitoring configured" appears in sources 2 and 3, and "credentials vaulted" appears in sources 1 and 3. Distinct checks: penetration test complete, critical findings remediated, credentials vaulted, runbook delivered, monitoring configured, on-call rota agreed, rollback tested — seven (so A and D miscount). Now group and order: security (penetration test, findings remediated, credentials vaulted), then operations (runbook, monitoring, on-call rota), then resilience — which contains only rollback tested, making it the final item. Option C forgets that resilience comes after operations. This mirrors your **Service focus** skill — taking inputs and establishing coherent frameworks that work. Real readiness checklists are always merged from several teams' lists plus lessons learned, and the analyst who de-duplicates cleanly and groups logically produces the checklist people actually use.

### Preparation tips

- **Rehearse with real artefacts.** Take a recent test report or security checklist and consciously run the checks from this section: gaps in sequences, numbers that reconcile, evidence that matches the exact build and criterion. Ten deliberate minutes counts as training.
- **Verbalise rules before applying them.** "Both conditions, joined by AND." "Valid only if production-sized." Saying the rule in words anchors it before the options try to bend it.
- **Separate your three checks.** Numbers (do they add up?), rules (is it allowed?), timeline (is the order possible?). Running them one at a time catches what a single fused read misses.
- **Use elimination on hard questions.** Cross out options a rule forbids; what survives is your answer. This is faster and safer than arguing each option to a conclusion.
- **Practise accuracy first, then add the clock.** Untimed practice builds technique; timed practice builds pacing. In the final days before a test, do both.
- **Arrive rested and set up.** Quiet room, water, rough paper, calculator if allowed, notifications off. Cognitive scores are physiology as well as skill.

### Common pitfalls to avoid

- **Trusting the summary over the detail.** "All tests executed" is a claim; the ID list is the evidence. Your whole role — and many test questions — live in that gap.
- **Verifying evidence about the wrong thing.** A real scan of the wrong build, results from the wrong environment. Always check what the evidence is evidence of.
- **Letting excellence excuse invalidity.** Outstanding results from an invalid setup are still invalid for acceptance. Quality of numbers and validity of method are separate questions.
- **Inventing comforting explanations.** "It was probably renamed", "they probably fixed it". Possible is not verified. The correct move is a precise question, not a hopeful assumption.
- **Solving two tangled problems as one.** An unrecorded change masking a capacity gap is two issues: surface the concealment and escalate the trade-off. Untangle before you act.
- **Rushing easy questions to bank time.** Early careless errors cost more than late hard questions. Steady accuracy throughout beats a sprint-and-stumble pattern.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment measures how accurately and confidently you handle numbers in realistic work situations. It is emphatically not a maths exam: no algebra, no formulae to memorise beyond the everyday ones. The whole test is built from percentages, ratios, averages, rates, and the reading of tables and simple charts. What makes it job-specific is the data: for a service readiness analyst, that means test pass rates, defect counts, KPI figures, capacity utilisation, incident volumes, and availability percentages — the numbers that flow across your desk every week.

The typical format is an online, timed test of 20 to 30 minutes with 15 to 25 multiple-choice questions. Each question gives you a small data set — a table, a chart, or a short numeric statement — and asks for a calculation or comparison. Calculators are normally allowed, rough paper is invaluable, and some platforms adapt question difficulty to your performance. Scores compare your accuracy and pace against a norm group of people at a similar level.

Employers use numeric reasoning for readiness roles because acceptance decisions are numeric decisions wearing sentences. "Testing is essentially complete" means a specific pass percentage. "Performance is acceptable" means measured response times against a stated threshold. "The defect position is manageable" means counts, severities, and a closure rate. When you check whether criteria have been met, you routinely recompute a supplier's headline figure from their own raw numbers — and a meaningful fraction of the time, the two disagree. The organisation is safer when its readiness analyst finds that disagreement before go-live rather than after, and this assessment measures exactly that ability.

Take heart: nearly every question reduces to three moves — part-of-whole (percentages), comparison (ratios, differences, percentage change), and division-by-count (averages and rates). Master those three, sense-check every answer against the data's range, and you will handle anything this test format offers. The practice questions below build each move using your genuine working materials.

### How this assessment maps to your role

- **Percentages and pass rates** map to your core duty of testing products and checking criteria: acceptance thresholds are stated as percentages, and your job is to verify claimed figures from raw counts.
- **KPI arithmetic** maps to your **Availability and capacity management** skill: managing service components against business needs and KPIs means computing availability, utilisation, and headroom, and knowing when a trend will breach a target.
- **Defect and incident rates** map to your **Problem management** and **Incident management** skills: investigating problems starts with rates and trends — defects per release, incidents per week, closure velocity.
- **Impact quantification** maps to your **Change management** skill: analysing and assessing the impact of change often means counting affected users, systems, and transactions, and expressing risk in proportions.
- **Data reconciliation** maps to your **Asset and configuration management** skill: tracking and correcting information includes checking that counts reconcile across registers, audits, and reports.
- **Evidence-based flags** map to your escalation duty and your **User focus** skill: a risk flagged with clear numbers ("affects 60% of users", "trend breaches KPI in 5 weeks") is a flag your service transition manager can act on immediately.

### Practice questions

**Question 1 (easy) — Test pass rate**

A test completion report shows 168 of 175 executed test cases passed. What is the pass rate, to the nearest whole percentage?

- A) 92%
- B) 94%
- C) 96%
- D) 98%

**Correct answer: C**

**Explanation:** Pass rate = passed ÷ executed × 100. Here: 168 ÷ 175 = 0.96, so 96%. A tidy route: 7 tests failed, and 7 ÷ 175 = 0.04 = 4% failed, so 100% − 4% = 96% passed. Working from the smaller number (failures) is often quicker and less error-prone than dividing the big numbers. Verifying a supplier's claimed pass rate from their raw counts is one of the most common numeric acts in readiness work — and when your figure disagrees with their headline, you have found something worth a polite question.

**Question 2 (easy) — Average defects per release**

The last five releases introduced 6, 9, 4, 11 and 10 defects respectively. What is the mean number of defects per release?

- A) 7
- B) 8
- C) 9
- D) 40

**Correct answer: B**

**Explanation:** Add the values: 6 + 9 + 4 + 11 + 10 = 40. Divide by the number of releases: 40 ÷ 5 = 8. Option D is the total, not the average — re-read the question's final words before answering. Sense-check: the mean must lie between the minimum (4) and maximum (11); 8 does, 40 cannot. A defects-per-release average is a useful baseline in readiness work: when the next release lands with 19 defects against a baseline of 8, you have a numeric anomaly worth investigating and, quite possibly, flagging.

**Question 3 (easy) — Reading a KPI table**

| Component | Availability target | Availability actual |
|---|---|---|
| Web front end | 99.5% | 99.7% |
| Records API | 99.9% | 99.6% |
| Document store | 99.0% | 99.2% |

Which component missed its availability target?

- A) Web front end
- B) Records API
- C) Document store
- D) None of them

**Correct answer: B**

**Explanation:** Compare actual against target row by row. Web front end: 99.7% ≥ 99.5%, met. Records API: 99.6% < 99.9%, missed. Document store: 99.2% ≥ 99.0%, met. The trap in tables like this is visual: 99.6% looks like a "high" number, and a rushed eye sees all three actuals in the high nineties and concludes "all fine". But targets differ by component — the most critical component carries the strictest target, so the same actual figure can be a pass for one row and a fail for another. Always compare within the row, not against a general feeling of "high". This is exactly how you manage service components against their KPIs rather than against impressions.

**Question 4 (easy) — Percentage of users affected**

An impact assessment finds that a change affects the case-search feature, used by 1,350 of the service's 4,500 registered users. What percentage of users is affected?

- A) 25%
- B) 30%
- C) 33%
- D) 35%

**Correct answer: B**

**Explanation:** 1,350 ÷ 4,500 = 0.30 = 30%. A quick route: 10% of 4,500 is 450, and 1,350 is three of those (450 × 3), so 30%. Building answers from easy 10% blocks is one of the fastest mental techniques for workplace percentages and works beautifully under time pressure. Quantifying impact as a proportion is what turns your change analysis into a risk statement a manager can rank: "affects 30% of users" lands very differently from "affects some users", and your escalations become more useful the more precisely they are quantified.

**Question 5 (moderate) — Defect closure rate and projection**

Fourteen defects must be closed before go-live. Over the past four days the team closed 2, 3, 2 and 3 defects (10 in total). Go-live is 2 working days away. At the average closure rate of the past four days, how many of the 14 will remain open at go-live?

- A) 0
- B) 4
- C) 5
- D) 9

**Correct answer: A**

**Explanation:** Read the stem carefully: 14 defects must be closed in total, and 10 have already been closed over the four days described, leaving 14 − 10 = 4 open now. The average closure rate is 10 ÷ 4 = 2.5 defects per day. In the 2 remaining working days the team can close about 2.5 × 2 = 5 more — which exceeds the 4 remaining, so the projection says 0 remain open at go-live. Option B (4) forgets the coming two days entirely; option C (5) reports the projected closures rather than the remainder; option D (9) subtracts only one day's work. Two lessons travel with this question. First, always establish the current position (4 open) before projecting. Second, treat the result with professional care: a projection that lands exactly on "just enough" has zero margin, and in a real readiness report you would say so — "on current closure rates we clear the backlog with no contingency" is an honest flag, not a green light.

**Question 6 (moderate) — Ratio of severities**

The open defect log shows 6 critical, 18 major and 24 minor defects. What is the ratio of critical to major to minor, in simplest form?

- A) 6:18:24
- B) 1:3:4
- C) 3:1:4
- D) 1:2:4

**Correct answer: B**

**Explanation:** Divide all three numbers by their greatest common divisor. All divide by 6: 6 ÷ 6 = 1, 18 ÷ 6 = 3, 24 ÷ 6 = 4, giving 1:3:4. Option A is correct but unsimplified; option C scrambles the order (always keep the ratio in the order the question names the categories); option D divides inconsistently. Severity ratios describe the shape of a defect log at a glance: a log of mostly minors with few criticals (like this one) tells a go/no-go review a very different story from the same total count dominated by criticals — which is why readiness summaries often quote the ratio, and why you should be able to verify it in seconds.

**Question 7 (moderate) — Availability from downtime minutes**

A service ran for a 30-day month (43,200 minutes) with two outages: 54 minutes and 36 minutes. What availability percentage did it achieve, to two decimal places?

- A) 99.79%
- B) 99.90%
- C) 99.80%
- D) 99.98%

**Correct answer: A**

**Explanation:** Total downtime = 54 + 36 = 90 minutes. Downtime fraction = 90 ÷ 43,200. Simplify: 90 ÷ 43,200 = 1 ÷ 480 ≈ 0.002083, i.e. about 0.208%. Availability = 100% − 0.208% = 99.79% (to two decimal places). The efficient method computes the small downtime percentage and subtracts, rather than dividing 43,110 by 43,200 directly — less typing, fewer slips. Fluency with this conversion in both directions is genuinely useful: knowing that a 99.9% monthly target permits only about 43 minutes of downtime turns an abstract KPI into an operational reality you can test readiness against — if the rollback plan alone takes an hour to execute, a 99.9% target has already framed the stakes.

**Question 8 (moderate) — Percentage change in incident volume after go-live**

In the four weeks before a change went live, a service averaged 45 incidents per week. In the two weeks after go-live, it recorded 63 and 57 incidents. What is the percentage increase of the post-go-live average over the pre-go-live average?

- A) 15%
- B) 25%
- C) 33%
- D) 60%

**Correct answer: C**

**Explanation:** Post-go-live average = (63 + 57) ÷ 2 = 120 ÷ 2 = 60 incidents per week. Increase = 60 − 45 = 15. Percentage increase = 15 ÷ 45 = 0.333… ≈ 33%. Remember: divide by the value you started from (45), not the new value — 15 ÷ 60 = 25% is the classic wrong answer (option B), and option A confuses the raw difference (15 incidents) with a percentage. A one-third rise in weekly incidents after a release is a strong early-life-support signal: comparing before/after averages, correctly, is precisely how a readiness analyst evidences the sentence "this change appears to have degraded service stability" — a flag your service transition manager needs sooner, not later.

**Question 9 (moderate) — Weighted readiness score**

Your readiness scorecard weights areas as: security 40%, operations 35%, documentation 25%. A product scores 65 (out of 100) on security, 90 on operations, and 80 on documentation. What is its weighted score, and does it meet an acceptance threshold of 80?

- A) 78.3 — no
- B) 77.5 — no
- C) 80.5 — yes
- D) 78.5 — no

**Correct answer: B**

**Explanation:** Multiply each score by its weight and sum. Security: 65 × 0.40 = 26. Operations: 90 × 0.35 = 31.5. Documentation: 80 × 0.25 = 20. Total: 26 + 31.5 + 20 = 77.5. Against a threshold of 80, the product falls short. Option A is the unweighted mean ((65 + 90 + 80) ÷ 3 ≈ 78.3), which ignores the deliberate emphasis on security. Notice what the weighting does here: the strong operations score cannot compensate fully for weak security, because the framework was designed to make security count most — 40 weighting points. That design is the point: weighted scorecards encode priorities, and understanding the arithmetic lets you explain to a project team precisely why "brilliant ops, shaky security" fails while the reverse might pass.

**Question 10 (hard) — Capacity trend against a KPI**

A database server's storage stands at 3.30 TB used of 4.00 TB capacity. Usage grew from 3.06 TB three months ago — steady growth. Your standard requires flagging a capacity risk when usage is projected to exceed 90% of capacity within six months. Should you flag it, and why?

- A) No — usage is currently at 82.5%, below the 90% trigger.
- B) Yes — at 0.08 TB/month growth, usage reaches the 3.60 TB (90%) trigger in about 3.75 months, inside the six-month window.
- C) No — the server will not be completely full for about 8.75 months.
- D) Yes — any usage above 80% must always be flagged.

**Correct answer: B**

**Explanation:** Work in steps. Growth: (3.30 − 3.06) TB over 3 months = 0.24 TB ÷ 3 = 0.08 TB/month. Trigger level: 90% of 4.00 TB = 3.60 TB. Gap to trigger: 3.60 − 3.30 = 0.30 TB. Time to trigger: 0.30 ÷ 0.08 = 3.75 months — comfortably inside the six-month projection window, so the standard requires a flag. Option A answers a different question (current level) than the standard asks (projected level); option C computes time to 100% (0.70 ÷ 0.08 = 8.75 months), a threshold the standard does not use; option D invents a rule. This is your **Availability and capacity management** skill made numeric: identify capacity issues before they bite, by projecting the trend against the trigger — and note how the flag writes itself: "at current growth, storage breaches the 90% trigger in under 4 months".

**Question 11 (hard) — Reconciling test counts across sources**

The supplier's summary says 240 test cases were planned. Their detailed report lists: 205 executed and passed, 18 executed and failed, and 12 descoped with approval. Separately, the test tool export shows 223 executions. How many planned cases are unaccounted for in the detailed report, and does the execution count reconcile with the tool?

- A) 5 unaccounted; tool reconciles with the report
- B) 17 unaccounted; tool reconciles with the report
- C) 17 unaccounted; tool shows 6 fewer executions than the report
- D) 5 unaccounted; tool shows 12 fewer executions than the report

**Correct answer: A**

**Explanation:** Two reconciliations, done separately. First, planned versus reported: 205 + 18 + 12 = 235 accounted for, against 240 planned, so 240 − 235 = 5 cases are unaccounted for — neither executed nor descoped, simply absent (options B and C get 17 by wrongly excluding the 12 approved descopes from the accounting; a descoped case is accounted for, just not executed). Second, executions: the report implies 205 + 18 = 223 executed (descoped cases are not executed), and the tool export shows exactly 223 — the execution figures reconcile, eliminating options C and D. The working habit: reconcile each pair of sources on its own terms, and be precise about which categories count in each reconciliation (descoped counts toward "accounted for", never toward "executed"). Five silently missing test cases is a small number and a genuine finding — exactly the kind of quiet gap that turns up in production if nobody asks about it before acceptance.

**Question 12 (hard) — Combining pass rates across modules**

Security testing covered two modules. Module One: 40 tests, 90% passed. Module Two: 160 tests, 95% passed. What was the overall pass rate across all security tests?

- A) 92.5%
- B) 94%
- C) 93%
- D) 95%

**Correct answer: B**

**Explanation:** Convert percentages back to counts before combining — never average the percentages. Module One: 90% of 40 = 36 passed. Module Two: 95% of 160 = 152 passed. Combined: (36 + 152) ÷ (40 + 160) = 188 ÷ 200 = 0.94 = 94%. The tempting error is (90% + 95%) ÷ 2 = 92.5% (option A), which treats a 40-test module as equal in weight to a 160-test module. Because Module Two is four times larger, the true combined rate sits much nearer its 95%. Sense-check: the answer must lie between 90% and 95%, closer to the bigger module's figure — 94% fits perfectly. Suppliers' summary slides love averaged percentages; readiness analysts recompute from counts, and the difference between 92.5% and 94% (or in nastier cases, much more) can sit right on an acceptance threshold.

**Question 13 (hard) — Reading a trend table for a go/no-go input**

| Week | Incidents raised | Incidents resolved | Backlog at week end |
|---|---|---|---|
| 1 | 30 | 24 | 26 |
| 2 | 34 | 30 | 30 |
| 3 | 38 | 32 | 36 |
| 4 | 36 | 30 | 42 |

The backlog at the start of week 1 was 20. Which statement gives the most accurate go/no-go input?

- A) Resolution is keeping pace with demand — the backlog is stable.
- B) The backlog has more than doubled in four weeks (20 to 42) because resolutions have trailed arrivals every single week; at the current net rate (about +5.5 per week), it will pass 60 within four more weeks.
- C) Incidents raised are falling, so the situation is improving.
- D) The backlog figures must be wrong because they do not follow from the other columns.

**Correct answer: B**

**Explanation:** Verify the backlog column first: each week's backlog should equal the previous backlog + raised − resolved. Week 1: 20 + 30 − 24 = 26 ✓. Week 2: 26 + 34 − 30 = 30 ✓. Week 3: 30 + 38 − 32 = 36 ✓. Week 4: 36 + 36 − 30 = 42 ✓. The table is internally consistent, eliminating option D. Now the trend: arrivals exceeded resolutions every week (net +6, +4, +6, +6), the backlog grew from 20 to 42 — a 110% rise — and the average net growth is 22 ÷ 4 = 5.5 per week, so 42 + 4 × 5.5 = 64 in four more weeks. Option A is contradicted by every row; option C cherry-picks the single week-4 dip in arrivals (38 → 36) and ignores the backlog. Option B does what a readiness input should: states the verified trend, quantifies it, and projects it. Verify, quantify, project — that is the whole craft of numeric evidence for go/no-go decisions.

### Preparation tips

- **Drill the three moves.** Part-of-whole, comparison, division-by-count. Set yourself five of each from real work numbers this week; fluency in the moves is fluency in the test.
- **Recompute one real headline figure per week.** Take a supplier's or a dashboard's claimed percentage and derive it from the raw counts yourself. It is perfect practice and occasionally a genuine finding.
- **Write the formula fragment before computing.** "(new − old) ÷ old", "passed ÷ executed", "weight × score, then sum". Naming the method first prevents calculator autopilot.
- **Sense-check every answer against its range.** Averages sit between min and max; combined rates sit between the component rates, nearer the bigger group; availability sits just under 100%. Outside the range means a slip.
- **Learn the tidy conversions.** 1/480 of a month ≈ 0.21%; 43 minutes ≈ 0.1% of a month; 1/8 = 12.5%. Small stock of conversions, large saving of time.
- **Practise reconciliation as a habit.** Whenever a report offers parts and a total, add the parts. It takes seconds, and both tests and audits reward the reflex.

### Common pitfalls to avoid

- **Averaging percentages from unequal groups.** Always rebuild counts, combine, then divide. The bigger module drags the true figure toward itself; naive averaging hides that.
- **Dividing by the wrong base.** Percentage change divides by the starting value; pass rates divide by executed (not planned); missing items divide by the register. Ask "of what?" every time.
- **Answering the question you expected.** Time-to-90% is not time-to-full; the average is not the total; "projected to breach in six months" is not "currently breaching". Re-read the final sentence before committing.
- **Trusting a table without verifying its arithmetic.** Columns that should reconcile sometimes do not — and sometimes they do, which eliminates a tempting "the data is wrong" option. Check either way.
- **Confusing counts with rates.** A steady failure count over growing volume is an improving rate. Readiness claims blur this constantly; your arithmetic should not.
- **Skipping the sense-check under time pressure.** The two-second range check is the highest-value habit in numeric testing. Never trade it for pace.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment measures how precisely you read, understand, and draw conclusions from written material. For a service readiness analyst, the material is the paperwork of transitions: security standards, readiness criteria, supplier reports, service level agreements, incident procedures, and the emails in which project teams describe — sometimes optimistically — how ready their product really is.

The dominant question format is true / false / cannot say: after a short passage, you judge whether a statement is definitely true (the passage says it or it follows necessarily), definitely false (the passage contradicts it), or cannot be determined (the passage is silent). Other formats include choosing the best summary, identifying what follows logically, and judging which of several sentences communicates most clearly. A typical test runs 15 to 25 minutes with 20 to 30 questions spread across several passages, and is scored against a norm group.

The single most important rule: answer from the passage alone. Your ITIL knowledge, your experience of how suppliers behave, and your instincts about what "probably" happened must all be set aside. If the passage does not state it, and it does not follow necessarily, the answer is "cannot say" — even when your professional experience whispers otherwise. This discipline feels artificial for the first dozen questions and then becomes second nature, and it happens to be the same discipline that makes you excellent at your job.

Why do employers test this for readiness roles? Because your acceptance decisions rest on documents, and documents are written by people with incentives. A supplier report that says "testing is substantially complete" is doing something different from one that says "all planned tests have been executed". A security summary that says findings were "addressed" may or may not mean they were fixed. You are the reader whose precision protects the service — the person who notices what a sentence commits to, what it avoids committing to, and what evidence would settle the difference. Verbal reasoning scores predict exactly that kind of protective reading.

### How this assessment maps to your role

- **Precise comprehension** maps to your core accountability for application acceptance and security criteria: acceptance hangs on the exact meaning of words like "remediated", "reviewed", "planned" and "executed", and your reading must be exact enough to hold that line.
- **True / false / cannot say discipline** maps to your risk-flagging duty: a good flag distinguishes what is known (stated, evidenced), what is contradicted, and what is unknown — precisely the three verdicts the question format trains.
- **Inference control** maps to your **Change management** skill: assessing the impact of change from documents means deducing real consequences without inventing ones the documents do not support.
- **Reading procedures accurately** maps to your **Continuity management**, **Incident management** and **Asset and configuration management** skills: procedures are dense conditional texts, and acting on them starts with parsing them correctly.
- **Clear-writing judgement** maps to your duty to document change requests and to your **Community collaboration** skill: recognising and dealing with issues in a team often begins with writing them up so plainly that no one can misunderstand.
- **Reading user evidence carefully** maps to your **User focus** skill: collating user needs evidence without over-claiming is verbal precision applied to research data.

### Practice questions

For questions 1 to 5, read this extract from a departmental security standard:

> "Before any application handling official information is accepted into live service, a security assessment must be completed by an accredited assessor. Critical and high-severity findings must be remediated before go-live; medium-severity findings must either be remediated or have a risk acceptance signed by the Senior Information Risk Owner (SIRO). Low-severity findings may be carried into live service provided they are recorded in the risk register and reviewed within three months of go-live. Applications that do not handle official information follow the lightweight assurance route, which is documented separately."

**Question 1 (easy) — True / false / cannot say**

Statement: "Critical findings must be remediated before go-live."

- A) True
- B) False
- C) Cannot say

**Correct answer: A**

**Explanation:** The passage states it directly: "Critical and high-severity findings must be remediated before go-live." When a statement matches the passage almost word for word, confirm there is no flipped term (critical for medium, remediated for reviewed) and bank the mark. Easy verbal questions reward exactly the confirming glance you give a criterion before signing it off: not a re-read of everything, just a precise match of the claim against the text. That thirty-second habit is the foundation of both verbal test scores and trustworthy acceptance records.

**Question 2 (easy) — True / false / cannot say**

Statement: "Medium-severity findings must always be remediated before go-live."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** The passage offers two routes for medium-severity findings: remediation, or a signed risk acceptance from the SIRO. "Must always be remediated" denies the second route, so the statement contradicts the passage and is false. The pivotal word is "either... or" in the standard and "always" in the statement — absolute words (always, never, all, only) are the most common way a test statement diverges from a nuanced passage. Your working life is full of this exact structure: criteria with alternative routes to compliance. Knowing the alternatives is what lets you tell a project team "you don't have to fix this one before Friday — but you do need the SIRO's signature if you don't".

**Question 3 (moderate) — True / false / cannot say**

Statement: "The SIRO must sign risk acceptances for low-severity findings carried into live service."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** Check what the passage requires for low-severity findings: they "may be carried into live service provided they are recorded in the risk register and reviewed within three months". The conditions are recording and review — the passage attaches the SIRO's signature to medium-severity risk acceptances only. The statement transplants a requirement from one severity band to another, and the passage's own text contradicts it, making the answer false rather than cannot say. This "condition transplant" is a classic error in both tests and real reviews: requirements travel with their severity band, and a reader who blurs the bands will demand signatures that are not needed — or worse, miss ones that are. Read tiered rules tier by tier.

**Question 4 (moderate) — True / false / cannot say**

Statement: "A case-tracking application that handles official information must have its security assessment completed by an accredited assessor before acceptance into live service."

- A) True
- B) False
- C) Cannot say

**Correct answer: A**

**Explanation:** The passage's first sentence covers "any application handling official information" and requires a completed security assessment "by an accredited assessor" before acceptance into live service. A case-tracking application that handles official information is an instance of that category, so the requirement applies necessarily — this is a valid deduction from a general rule to a specific case, which the true/false/cannot say format does allow. "True" is not limited to word-for-word repetition; it includes what follows logically. Contrast this with invented details (an assessor's name, a timescale the passage never gives), which would be "cannot say". Applying general standards to specific products is your daily reasoning as a readiness analyst — this question is that reasoning in miniature.

**Question 5 (moderate) — Best summary**

Which sentence best summarises the passage?

- A) All findings must be fixed before any application goes live.
- B) Applications handling official information need an accredited security assessment, with remediation or governed acceptance requirements that scale with finding severity; other applications follow a separate lightweight route.
- C) The SIRO decides whether applications may go live.
- D) Low-severity findings can be ignored for three months.

**Correct answer: B**

**Explanation:** Sketch the passage's skeleton: (1) scope — applications handling official information; (2) requirement — accredited assessment; (3) a severity ladder with different obligations per rung; (4) a separate route for out-of-scope applications. Option B captures all four elements without contradicting any detail. Option A flattens the ladder into an absolute the passage explicitly avoids. Option C inflates one signature into general authority. Option D turns "recorded and reviewed within three months" into "ignored", which is nearly the opposite — recording in a risk register is active management, not neglect. Summary questions reward structure-first reading, and so does your job: when you brief your service transition manager on a standard, the severity-ladder summary in option B is exactly the shape of a useful briefing.

For questions 6 to 9, read this email from a supplier's delivery manager:

> "Following this week's testing, we're in good shape for the 28th. Performance testing is complete against the agreed profiles and all response-time thresholds were met. On security, the penetration test report arrived yesterday: no critical findings, three high-severity findings for which fixes are being developed, and some lower-severity items we'll talk through at the readiness review. Documentation is on track — the runbook draft is with your operations team for comment. One thing to note: the data migration dry run scheduled for Monday has been pushed back to Wednesday due to environment availability, which leaves it a little closer to the go-live date than we'd like, but we don't see this as a blocker."

**Question 6 (easy) — True / false / cannot say**

Statement: "All response-time thresholds were met in performance testing."

- A) True
- B) False
- C) Cannot say

**Correct answer: A**

**Explanation:** Directly stated: "all response-time thresholds were met". Locate the supporting sentence, confirm the wording matches, answer, move on. One refinement worth practising even on easy questions: notice the boundary of the claim. The email says thresholds were met "against the agreed profiles" — a scoped claim. The statement as written stays inside that scope, so it is true. Had the statement said "the application will perform well at any load", the scoping phrase would have made it "cannot say". Claims come with boundaries; precise readers track them.

**Question 7 (moderate) — True / false / cannot say**

Statement: "The three high-severity security findings have been fixed."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** The email says fixes "are being developed" — present continuous, work in progress. A fix being developed is by the email's own words not yet complete, so "have been fixed" contradicts the passage: false. Be careful not to slide to "cannot say" on the grounds that the fixes might be finished by now — the statement is judged against the situation the email describes, and the email is explicit about in-progress status. This tense-precision matters enormously in your role: "being developed", "being addressed", "in hand" all describe intention and activity, not completion, and a readiness analyst who reads them as "done" has accepted a promise as evidence. Your security criteria almost certainly require the fixes verified — a status this email does not claim.

**Question 8 (moderate) — True / false / cannot say**

Statement: "The delay to the data migration dry run was caused by problems with the migration scripts."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** The email gives a cause: "due to environment availability". The statement asserts a different cause — script problems — which the passage's stated reason contradicts. When a passage explicitly attributes a cause, an alternative cause is false, not cannot say. (Compare: if the email had given no reason at all, the script claim would be "cannot say".) The distinction rehearses a real readiness habit: recording the stated reason for every slip, precisely. Stated reasons can later be tested against evidence — "environment availability" invites the question "what is being done about environment contention before go-live?" — whereas vaguely remembered reasons can only breed speculation. Accurate cause-tracking is also what keeps your risk flags fair to suppliers.

**Question 9 (hard) — Reading what the email does not say**

Judged strictly against the email's content, which of the following is the strongest reason for caution about the 28th?

- A) Performance testing failed to cover the agreed profiles.
- B) The runbook has not been started.
- C) High-severity security findings exist without completed fixes, and the migration dry run has moved to within days of go-live — so two acceptance-critical items are unresolved.
- D) The supplier has admitted the date will be missed.

**Correct answer: C**

**Explanation:** Options A, B and D all misstate the email: performance testing did cover the agreed profiles; the runbook exists as a draft under review; and the supplier explicitly maintains the date. Option C sticks to what the email actually establishes — three high-severity findings with fixes merely in development, and a dry run now sitting "a little closer to go-live than we'd like" — and correctly identifies these as the unresolved acceptance-critical items. Notice the skill: the email's tone is confident ("good shape", "not a blocker"), but tone is not content. Strip the reassurance and list the objective statuses, and the caution writes itself. This is perhaps the most valuable verbal skill in readiness work: reading past an author's framing to inventory what is actually evidenced, actually pending, and actually at risk — then saying so, calmly, at the readiness review.

For questions 10 to 12, read this extract from an internal continuity procedure:

> "In the event of a complete failure of the primary data centre, services designated as priority one must be restored at the secondary site within four hours; priority two services within twenty-four hours. Restoration is performed in strict priority order. The continuity plan for each service must be tested at least annually, and any test that fails must be repeated within eight weeks. Service restoration times are measured from the formal declaration of a continuity incident, not from the initial failure."

**Question 10 (moderate) — True / false / cannot say**

Statement: "A priority two service could be restored more than twenty-four hours after the primary data centre initially fails, without breaching the procedure."

- A) True
- B) False
- C) Cannot say

**Correct answer: A**

**Explanation:** The procedure's last sentence is the key: restoration times run "from the formal declaration of a continuity incident, not from the initial failure". If declaration happens, say, three hours after the initial failure, a priority two service restored twenty-six hours after the failure is still within twenty-four hours of declaration — compliant. So the statement is true: the scenario it describes is possible without breach. This is a deduction question that hinges on measurement definitions, and it earns its "moderate-to-hard" label honestly: the untrained eye reads "twenty-four hours" and anchors it to the failure. Measurement clauses — from when, to when, measured how — are where SLAs and continuity targets are genuinely won and lost, and reading them precisely is a skill your **Continuity management** knowledge requirement expects you to explain to others.

**Question 11 (moderate) — True / false / cannot say**

Statement: "Continuity plan tests are carried out by the service readiness team."

- A) True
- B) False
- C) Cannot say

**Correct answer: C**

**Explanation:** The procedure requires testing "at least annually" and repeat testing after failures, but it never says who performs the tests. Your own role might well be involved in real life — and that knowledge is exactly what you must set aside. The passage is silent on the performer, so the answer is cannot say. Distinguish the three verdicts cleanly: the passage states testing frequency (true-territory), contradicts nothing about performers (not false-territory), and simply does not address who (cannot-say-territory). Recognising silence is a professional act, not a technicality: procedures that omit an owner for a required activity are procedures where the activity quietly stops happening — spotting the omission is precisely the kind of gap a readiness analyst flags when reviewing operational documentation.

**Question 12 (hard) — Clear-writing judgement**

You are writing a risk flag for your service transition manager about the supplier email in questions 6 to 9. Which version is most effective?

- A) "There are some concerns with the supplier's position that may warrant consideration ahead of the proposed implementation date."
- B) "Risk: three high-severity security findings are unfixed and the migration dry run has slipped to two days before go-live. Impact: security criteria cannot be evidenced, and a failed dry run would leave no time to respond. Suggested action: hold the go/no-go until fixes are verified and the dry run passes."
- C) "The supplier's optimism regarding the 28th appears potentially misplaced given various outstanding items of a security and migration-related nature."
- D) "As per my analysis of the aforementioned correspondence, several risk vectors have been identified for escalation purposes."

**Correct answer: B**

**Explanation:** Option B has the anatomy of a useful flag: the risk (specific, countable — three findings, a dated slip), the impact (what it means for criteria and response time), and a suggested action (what decision the reader could take). A manager can act on it in sixty seconds. Options A and C gesture at concern without naming anything — "some concerns", "various outstanding items" — forcing the reader to re-do your analysis; they are polite fog. Option D is jargon about the existence of analysis rather than the analysis itself. Since your role summary makes flagging and escalating risks your defining duty, this structure — risk, impact, suggested action — is worth memorising as a template. Clear flags travel up the organisation intact; vague ones either get ignored or get inflated, and both outcomes are failures of writing, not of analysis.

### Preparation tips

- **Practise the three verdicts on real documents.** From any supplier email, extract one thing it states, one thing it rules out, and one thing it leaves unsaid. This is the entire test format, rehearsed on your own material.
- **Track tenses and completion words.** "Being developed" versus "developed"; "planned" versus "executed"; "addressed" versus "remediated and verified". Completion status lives in the grammar.
- **Watch measurement clauses.** From when? To when? Against what scope? SLA and continuity passages hide their hardest questions in the definitions.
- **Locate the supporting sentence for every answer.** If you cannot point at the words, you are inferring — which is fine only when the inference is logically forced.
- **Summarise structure, not sentences.** Before judging summary options, sketch the passage's skeleton (scope, requirement, tiers, exceptions). The best summary matches the skeleton.
- **Read GOV.UK-style plain English regularly.** It calibrates your ear for the clear-writing questions and improves your own risk flags at the same time.

### Common pitfalls to avoid

- **Importing your professional knowledge.** You know how suppliers work; the passage may not say it. In this test, unstated experience is a source of errors, not marks.
- **Reading tone instead of content.** "We're in good shape" is mood music. List the objective statuses; judge those.
- **Blurring "false" and "cannot say".** Contradicted by the passage is false; unaddressed by the passage is cannot say. Spend the extra beat deciding which.
- **Transplanting conditions between tiers.** Requirements attach to their severity band, priority level, or service class. Do not carry the SIRO's signature where it does not belong.
- **Anchoring absolutes to the wrong reference point.** "Within twenty-four hours" of what? The measurement clause decides, not your assumption.
- **Choosing formal-sounding fog in writing questions.** The clearest option names the risk, the impact, and the action. Length and formality are not clarity — often they are its opposite.

## Workplace job-specific situational judgement assessment

### About this assessment

A situational judgement test (SJT) presents realistic workplace scenarios and asks you to judge the effectiveness of possible responses. It measures professional judgement rather than knowledge: given a messy, human, time-pressured situation, do you recognise which behaviours help and which harm?

Formats vary. The most common asks for the most effective response among four options; variants ask for the least effective, ask you to rank all options, or ask you to rate each on a scale. Timing is usually relaxed — 20 to 30 minutes for 15 to 20 scenarios — because the test measures judgement, not speed. Scoring compares your choices against a key built by experienced professionals and occupational psychologists, aligned to behaviour frameworks: for GDAD roles, expect user focus, collaboration, ownership, honesty about problems, appropriate escalation, and inclusion to underpin the key.

Employers use SJTs for readiness roles because your role concentrates a particular kind of pressure: you are the person whose findings can delay a go-live, and everyone with a stake in the date knows it. Suppliers frame their reports optimistically. Project managers ask whether items are "really" blockers. Colleagues hope a risk can wait until after the review. An SJT explores how you behave inside that pressure: whether you flag early or sit on concerns, whether you hold criteria firmly without hostility, whether you own an issue until it is genuinely handed over, and whether you keep the interests of end users — who are absent from every meeting — present in your judgements.

Reassurance about "right answers": SJT scenarios rarely contain a perfect option. They contain a most effective option, some defensible middles, and at least one genuinely poor choice. You are being tested on recognising the shape of good professional behaviour: establish the facts, be honest early, use the proper channel, involve the right people at the right level, and match the size of your response to the size of the problem. The explanations below name the behaviours behind each answer so you learn the pattern, not merely the letter.

### How this assessment maps to your role

- **Escalation quality** maps directly to your role summary: "flag any potential risks and escalate these to the service transition manager". Scenarios probe when you escalate, how you frame it, and what you do first.
- **Integrity under date pressure** maps to your accountability for application acceptance and security criteria: several scenarios test whether evidence standards bend when deadlines push.
- **Issue ownership** maps to your **Ownership and topic** skill: owning an issue until a new owner is found or the problem is mitigated or resolved — no silent drops, no hot-potato handoffs.
- **Team scenarios** map to your **Community collaboration** skill: contributing to others' work, motivating and empowering teams, creating the right environment, and recognising and dealing with issues in team dynamics.
- **Incident and security responses** map to your **Incident management** skill and your security-checking duty: gathering information calmly, using the appropriate channel, and never improvising with credentials or live systems.
- **User-centred judgement** maps to your **User focus** skill: engaging users and stakeholders, and letting quantitative and qualitative evidence — not convenience — shape readiness recommendations.

### Practice questions

**Question 1 (easy) — The optimistic status report**

At a readiness checkpoint, the project manager presents a slide saying "Security: GREEN". You know the penetration test report includes two high-severity findings whose fixes have not yet been verified. The meeting is moving quickly to the next slide. What is the most effective response?

- A) Stay silent — you can raise it privately later this week.
- B) Speak up now, briefly and factually: security has two high-severity findings awaiting verified fixes, so you would rate it amber until verification evidence lands.
- C) Interrupt to say the whole report is unreliable and should be withdrawn.
- D) Let the meeting finish, then email your objection to everyone who attended.

**Correct answer: B**

**Explanation:** Checkpoint meetings exist to establish a shared, accurate picture; letting a wrong "GREEN" stand — even briefly — means decisions may be taken on it. Option B corrects the record at the moment it matters, factually and proportionately: a status, a reason, and what would change it. That is your flagging duty performed in real time. Option A trades accuracy for comfort; "later this week" may be after the decision. Option C escalates one wrong status into an attack on the whole report and its author — disproportionate, and it damages the collaboration your role depends on. Option D creates a written dispute after the moment for a spoken correction has passed, which reads as politics rather than assurance. The behaviour pattern rewarded: timely, specific, proportionate honesty in the room where the record is being set.

**Question 2 (easy) — A blocked test and a waiting queue**

Your security scan of a new build cannot start because your scanning account has been locked. Resetting it needs the identity team, whose queue says "responses within two working days". The scan is on the critical path for a review in three days. What is the most effective first action?

- A) Wait in the queue — two days still just fits.
- B) Raise the reset request immediately, note the critical-path dependency in the request, and tell your service transition manager the same day that the timeline now has no slack — so they can expedite if it slips.
- C) Borrow a colleague's credentials to run the scan today.
- D) Skip the scan this once — the previous build's scan was clean.

**Correct answer: B**

**Explanation:** Option B does three things in the right order: starts the clock on the fix (raise it now), improves the odds (a request that explains its urgency is easier to prioritise), and protects the timeline (your manager learns today that the plan has zero slack, while there is still time to act). That last step is the difference between an analyst who flags risk and one who reports history. Option A gambles the review on a best-case queue time and tells nobody. Option C is a serious security breach — sharing credentials is precisely the behaviour your scans exist to catch, and "for a good reason" is how every credential misuse story begins. Option D substitutes an old result for a required one: the previous build is not this build. Note the general shape: act through proper channels immediately, and escalate the risk in parallel — escalation and action are not alternatives.

**Question 3 (easy) — You broke it**

While testing in the shared staging environment, you accidentally corrupt a data set that another team is scheduled to use tomorrow morning. It is 16:30. What is the most effective response?

- A) Say nothing — they may not notice, and the environment team refreshes data weekly anyway.
- B) Tell the other team now, apologise, raise the refresh request with the environment team today, and follow it until the data is confirmed restored or a workaround is agreed.
- C) Send an anonymous note to the environment team asking for a refresh.
- D) Mention it to the other team tomorrow if their tests fail.

**Correct answer: B**

**Explanation:** This is an ownership scenario, and your **Ownership and topic** skill sets the standard: own an issue until it is mitigated, resolved, or properly handed over. Option B tells the affected team while they can still replan their morning, starts the fix immediately (a 16:30 request may still be actioned today), and — crucially — keeps following until restoration is confirmed. Ownership ends at confirmed resolution, not at "I sent an email". Option A converts an accident into a concealment, and tomorrow's failed test run will cost the other team hours of confused diagnosis. Option C fixes the data while hiding the cause, leaving the other team unable to assess what else might be affected. Option D makes them pay the diagnosis cost you could have spared them. Accidents in shared environments are routine; the score-separating behaviour is speed and completeness of honest follow-through.

**Question 4 (moderate) — Least effective: the supplier pushes back**

You reported that a supplier's evidence for the backup-restoration criterion is missing. Their delivery manager replies: "We've done dozens of these deployments — restoration always works. Requiring a test here is box-ticking." Which response is LEAST effective?

- A) Acknowledge their experience, restate the criterion and why it exists, and offer to observe a restoration test this week so the evidence burden is as light as possible.
- B) Agree to waive the test given their track record.
- C) Take the disagreement to your service transition manager with both positions fairly stated.
- D) Hold your position in writing and copy your service transition manager.

**Correct answer: B**

**Explanation:** In a least-effective question, hunt for the option that most damages the service and the framework. Option B is it: it substitutes the supplier's self-assessment for evidence, on the exact criterion — restoration — whose failure modes only appear when untested; and it teaches this supplier (and everyone they talk to) that your criteria yield to confident pushback. Option A is the most effective: it defuses the "box-ticking" framing by explaining purpose, and reduces friction by offering the cheapest sufficient evidence path. Options C and D are both reasonable escalation variants — C is collaborative, D is firmer — and either keeps the criterion intact while routing the disagreement appropriately. The professional behaviours at stake: evidence over assertion, criteria held with courtesy, and disagreement escalated rather than privately conceded. Track records are context; they are never evidence about this deployment.

**Question 5 (moderate) — A teammate wants to skip the boring part**

A fellow analyst, overloaded this week, asks you to countersign a readiness checklist section they say they have "basically finished — just the config checks left, and those never find anything". Countersigning confirms the section is complete. What is the most effective response?

- A) Countersign — team trust matters, and the checks are usually clean.
- B) Refuse and report them to your service transition manager for attempted misconduct.
- C) Decline to countersign until the checks are done, and offer practical help: split the remaining config checks between you now, or agree who does them tomorrow morning.
- D) Countersign now on their promise to finish the checks tomorrow.

**Correct answer: C**

**Explanation:** Your signature is an evidence artefact: it asserts that something happened. Options A and D both make the record say "complete" while reality says otherwise — D merely schedules the truth to catch up with the record, which inverts how records work, and if tomorrow goes wrong the record is false with your name on it. Option B treats an overloaded colleague's bad idea as malice; it damages the team over something a conversation can fix, and it skips the actually useful response. Option C protects the record and the colleague at once: the integrity line is held ("not until it's done"), and the workload problem — the real cause — gets a practical answer. This is your **Community collaboration** skill working with your integrity duty rather than against it: recognising and dealing with issues includes making it easy for a struggling teammate to do the right thing. "Config checks never find anything" is also worth a gentle challenge — checks that never find anything are either wasted or, more often, the ones that eventually find the big one.

**Question 6 (moderate) — Users versus the demo script**

Preparing for acceptance, you review the user research summary: assisted-digital users — about 15% of the service's users — struggle with the new document upload flow, and the research recommends a simplified alternative path that is built but switched off pending "post-launch evaluation". The acceptance demo next week will show only the standard flow. What is the most effective response?

- A) Note it privately and see whether complaints emerge after launch.
- B) Raise it before the demo: circulate the research finding, and propose that the review explicitly considers the assisted-digital path's status — on or off at launch — as an acceptance question.
- C) Switch the alternative path on yourself in staging so the demo includes it.
- D) Tell the researcher their finding has come too late to matter.

**Correct answer: B**

**Explanation:** Your **User focus** skill — using quantitative and qualitative user data to turn user focus into outcomes — is exactly what option B performs: the evidence (15% of users, a documented struggle, a built alternative) is put in front of the decision-makers, framed as a decision the review should own, before the moment of acceptance. Whether the path launches on or off is genuinely arguable; what is not arguable is that the decision should be made consciously, with the research visible, rather than by default because the demo script omitted it. Option A outsources user advocacy to future complaints — from the user group least likely to complain through digital channels. Option C exceeds your authority and confuses environments with decisions: toggling staging changes a demo, not a launch position. Option D shoots the messenger and buries the message. The rewarded pattern: bring user evidence to the decision point, in time, addressed to the people who own the decision.

**Question 7 (moderate) — The environment nobody owns**

Your readiness testing keeps failing because the staging environment drifts from production: patches and config changes appear in production without reaching staging. Each time, you fix the symptom and re-test. This is the fourth cycle. What is the most effective response?

- A) Keep fixing and re-testing — it works eventually each time.
- B) Refuse to conduct further testing until someone fixes staging permanently.
- C) Document the pattern (four cycles, the specific drifts, the time cost), identify that environment parity has no owner, and escalate to your service transition manager with a proposal: assign an owner and add a parity check to the release process.
- D) Quietly start testing in production instead, where the configuration is always current.

**Correct answer: C**

**Explanation:** This scenario tests whether you can convert recurring symptoms into a problem statement — your **Problem management** skill ("investigate problems in systems, processes and services... contribute to remedies and preventative measures") aimed at process rather than code. Option C carries all the ingredients of an effective escalation: evidence (four documented cycles), diagnosis (parity has no owner — a process gap, not a technical mystery), cost (your time, delayed readiness), and a proportionate proposal. Option A is diligence without learning; you will be fixing cycle nine while go-lives slip. Option B converts a legitimate grievance into a work stoppage that punishes projects for a process gap they did not create — escalation exists precisely so you do not have to choose between suffering and striking. Option D is the dangerous one: unauthorised testing in production trades a staging problem for potential live-service incidents and security violations. The rewarded shape, worth memorising: evidence, diagnosis, cost, proposal — routed to the level that can fix the system, not the symptom.

**Question 8 (moderate) — Least effective: the awkward stand-up**

In your team's stand-up, a quieter colleague is repeatedly talked over by two louder members; today she stopped contributing entirely, and you later learn she had spotted a genuine risk in the release plan that went unmentioned. Which response is LEAST effective?

- A) Talk to her afterwards, hear the risk, and encourage her to raise it — offering to back her at tomorrow's stand-up.
- B) Suggest to the team a round-robin format so every member speaks without interruption.
- C) Do nothing — stand-up dynamics are the team lead's business, not yours.
- D) Raise the general pattern with the team lead privately, without naming blame.

**Correct answer: C**

**Explanation:** The least effective option is C, and the reason is concrete, not just kind: a suppressed voice suppressed a risk, and the release plan is worse for it. Team dynamics are not somebody else's hygiene issue — your **Community collaboration** skill explicitly includes creating the right environment for teams and recognising and dealing with issues. Options A, B and D are all constructive at different levels: A recovers today's lost risk and supports the individual; B fixes the mechanism (format changes beat personality changes); D engages the person with formal authority while avoiding a blame frame. A strong real-world response might combine all three. The scenario's deeper lesson is the link SJTs repeatedly draw for readiness roles: inclusion is not separate from assurance quality — meetings where only the loud speak are meetings where risks go unlogged, and analysts who fix the room improve the release.

**Question 9 (hard) — Your manager is the bottleneck**

You flagged a significant security risk to your service transition manager eight days ago: a third-party component in the release has a published vulnerability, and the supplier's patch is unverified. Your manager said "leave it with me" — but the go/no-go review is in two days, nothing has visibly happened, and your follow-up message yesterday got no reply. What is the most effective response?

- A) You flagged it and it is with your manager — your responsibility has been discharged.
- B) Go around your manager directly to the programme director with the risk.
- C) Make one more direct, time-boxed attempt today — speak to your manager in person or by phone, state the two-day deadline, and ask explicitly whether they will take it forward or want you to; if you cannot reach them today, tell them in writing that the deadline requires you to raise it at the review, then do so.
- D) Say nothing, but if the review reaches go, mention the vulnerability afterwards so it is on record.

**Correct answer: C**

**Explanation:** This is the hardest escalation pattern: the escalation route itself has stalled. Option A mistakes process for purpose — your **Ownership and topic** skill says you own an issue until it is mitigated, resolved, or genuinely transferred, and a flag that vanished into silence has not been transferred; the risk still exists and you still know about it. Option D is worse: raising a known critical risk only after the decision is assurance theatre. Option B jumps two steps — going around your manager may eventually be right, but not before a direct, deadline-explicit attempt; managers juggling ten risks sometimes need exactly one clear sentence: "the review is in two days — are you taking this, or shall I?" Option C makes that attempt honestly, and — critically — includes a transparent fallback: your manager is told, in writing, that the deadline forces the issue into the review. Nothing is done behind anyone's back, and the risk reaches the decision on time. The rewarded behaviours: persistent ownership, respect for the escalation chain, transparency about what you will do, and an absolute refusal to let a known risk miss its decision point.

**Question 10 (hard) — The finding that embarrasses a friend**

Your readiness review of an application finds that the operations runbook — written by a good friend on the operations team — is significantly out of date: three procedures reference decommissioned systems, and the emergency contacts list is two reorganisations old. Your findings report goes to the readiness review, where your friend's team lead will see it. What is the most effective approach?

- A) Soften the finding to "minor documentation improvements suggested" to protect your friend.
- B) Tell your friend first so they can quietly fix it, and delay your report until they have.
- C) Report the finding accurately and neutrally (factual gaps, no blame framing), and give your friend a heads-up that it is coming so they are not ambushed — while making clear the report itself cannot change.
- D) Ask another analyst to review the runbook instead so you avoid the conflict.

**Correct answer: C**

**Explanation:** Two legitimate interests collide: the integrity of your findings and decency toward a colleague — and option C serves both without trading either. The report stays accurate (an out-of-date emergency contacts list is a genuine operational risk: in an incident at 3 a.m., someone calls a number that no longer answers), the framing stays factual rather than personal, and the heads-up converts an ambush into a professional courtesy. Option A falsifies severity — "minor improvements" describing broken emergency procedures is exactly the kind of softened finding that post-incident reviews later quote in bold. Option B subordinates the review's timeline to a private fix, and quietly conditions your report's content on personal relationships — the precedent is the poison, even if this fix would be harmless. Option D dodges rather than resolves: relationships in a team are permanent context, not recusal grounds for routine findings, and handing off the review signals that your findings are negotiable by friendship. The tested behaviours: report integrity, blame-free framing, and the professional kindness that operates alongside honesty instead of instead of it.

**Question 11 (hard) — Go-live day surprise**

It is go-live morning. During final checks you discover that last night someone applied an unapproved "quick fix" to the production configuration to resolve a performance issue found in the evening's rehearsal. The fix appears to work. The service goes live in three hours, stakeholders are assembled, and reversal would delay launch by at least a day. What is the most effective immediate action?

- A) Say nothing — the fix works, and launch pressure is enormous.
- B) Reverse the change immediately yourself, since it was unapproved.
- C) Immediately inform your service transition manager and the change authority: an unapproved production change exists, here is what it does, here are the options (retrospective emergency approval with expedited review, or reversal and delay) — so the go/no-go is made with full knowledge.
- D) Approve the change yourself retrospectively to regularise the paperwork before anyone asks.

**Correct answer: C**

**Explanation:** Strip the scenario to its structure: a decision (go/no-go) is about to be made on an inaccurate picture of production. Whatever the merits of the fix, the decision-makers do not know it exists — and restoring decision integrity is the immediate duty, ahead of either endorsing or reversing the change. Option C does exactly that, and does it well: facts, options, and consequences, routed to the people with authority, in time. This mirrors real change frameworks, which include retrospective emergency approval precisely for mornings like this — the fix may well survive review; concealment never should. Option A makes you a party to the concealment; "it works" is what everyone says until the first incident, at which point responders will be diagnosing a production system that does not match its documented configuration. Option B repeats the original sin in mirror image — another unilateral production change under pressure, this one guaranteeing the delay without any authority to accept it. Option D is worse than the original offence: the first change was unauthorised; falsifying its approval is a deliberate integrity breach. The rewarded pattern under maximum pressure: surface, inform, present options — and let authority decide with the truth in front of it.

**Question 12 (hard) — What the KPIs don't show**

Two weeks after a major release you supported, the service dashboard is green: availability, response times, and incident volumes all within target. But the service desk mentions in passing that "call handling times are up because callers seem confused by the new screens", and you notice task-completion feedback scores have dipped. Formal early-life-support exit is scheduled for Friday, based on the KPI dashboard. What is the most effective response?

- A) Support the Friday exit — the agreed KPIs are green, and the exit criteria are the exit criteria.
- B) Before Friday, gather the additional signals (call handling times, feedback scores, a quick word with the service desk lead), and bring them to your service transition manager with a recommendation: either extend early-life support or exit with a specific follow-up action on the usability signal.
- C) Declare early-life support failed and demand the release be rolled back.
- D) Log the observations in the service improvement backlog for consideration next quarter.

**Correct answer: B**

**Explanation:** This scenario separates analysts who monitor dashboards from analysts who monitor services. The KPIs are green — but KPIs are a sample of reality, not the whole of it, and two independent signals (longer calls, dipping completion scores) both point at the same thing: users are struggling with the new screens. Option B treats those signals with proportionate seriousness: gather quickly, corroborate with the humans nearest the users, and put an evidence-backed recommendation to the decision owner before the decision. Note that B does not prejudge the answer — exit-with-follow-up may be perfectly right; the point is that Friday's decision should see the whole picture. Option A hides behind criteria that were written before this evidence existed; "the criteria are the criteria" is how services exit support with known, unowned problems. Option C inflates a usability signal into a rollback demand — wildly disproportionate against green stability metrics. Option D correctly avoids overreaction and incorrectly avoids the deadline: next quarter is after the support structure that could act on the signal has been dismantled. The behaviours rewarded: user focus beyond the metrics, proportionate escalation, and respect for decision timing — evidence is worth most just before the decision it should inform.

### Preparation tips

- **Internalise your escalation template.** Risk, impact, options, suggested action — with a deadline attached. Most of this test's hardest scenarios are escalation scenarios in disguise, and the template turns panic into structure.
- **Rehearse holding a line kindly.** Practise sentences that pair firmness with help: "I can't sign that yet — here's the fastest route to evidence I can sign." Kind firmness is the single most rewarded behaviour pattern in assurance-role SJTs.
- **Study your behaviour framework before the test.** User focus, collaboration, ownership, honesty, escalation, inclusion. Scoring keys are built from these; reading them the week before is legitimate and effective preparation.
- **Name the behaviour after every practice question.** "That rewarded transparent fallback." "That punished unilateral production changes." Naming transfers the pattern to scenarios you have never seen.
- **Mine your own history.** Recall a time you softened a finding, sat on a flag, or watched a quiet colleague go unheard. What would the best version of you have done? SJT preparation done this way is straightforwardly professional development.
- **Answer consistently as your best professional self.** Do not model "what do they want me to say" — modern SJTs detect inconsistent personas. Considered honesty patterns best, in tests as in transitions.

### Common pitfalls to avoid

- **Discharging responsibility instead of ownership.** "I flagged it" is not the end of an issue you still know is live. Ownership ends at resolution, mitigation, or a confirmed handover — never at an unanswered message.
- **Confusing loyalty with kindness.** Softening findings for friends, countersigning for overloaded teammates, waiving tests for trusted suppliers — every one trades the service's safety for social comfort, and every one scores badly.
- **Unilateral action under pressure.** Reversing production changes alone, testing in production, toggling features, trying found credentials. The strong options route through authority and proper channels — at speed, but through them.
- **Silence in the room, objection afterwards.** Correcting the record after the meeting, mentioning the vulnerability after the decision. Timing is part of honesty; late truth loses most of its value.
- **Disproportion in both directions.** Demanding rollbacks over usability dips, or backlog-filing signals that a Friday decision needs. Match response size to problem size and decision timing.
- **Treating team dynamics as someone else's job.** The quiet colleague's unraised risk is your release's problem. Inclusion behaviours are assurance behaviours; SJT keys treat them that way.

## Conclusion

Well done — you have worked through a full programme of practice material built directly from your own role. That specificity is the point. Generic test practice makes you better at generic tests; practising with security criteria, test completion reports, KPI tables, supplier emails, and the genuine pressures of readiness work makes you better at both the assessments and the job they are modelled on.

Look back at what you have covered. In the cognitive section, you practised the verification disciplines at the centre of readiness work: finding the gap in a numbered sequence, chaining impact rules correctly, catching evidence that describes the wrong build or the wrong environment, and untangling two problems that arrive knotted together. In the numeric section, you rebuilt the three moves — part-of-whole, comparison, and division-by-count — and applied them to pass rates, availability, capacity projections, and the reconciliation checks that catch what summary slides smooth over. In the verbal section, you sharpened the reading that protects services: tenses that reveal completion status, measurement clauses that define what a target really means, tiered rules read tier by tier, and the discipline of "cannot say" when a document is silent. And in the situational judgement section, you rehearsed the professional shape of your role — flagging early and specifically, holding evidence standards with kindness, owning issues to genuine resolution, and keeping absent users present in every decision.

If a real assessment is coming, keep your preparation simple and steady. Practise in short sessions across at least two weeks. Return to the questions you got wrong and re-explain the correct reasoning in your own words — self-explanation is the strongest consolidation there is. Add light time pressure only in the final few days, once accuracy feels settled. On the day: rest well, set up a quiet space, and remember that the test is sampling skills you exercise every working week. You are arriving practised, not cold.

Beyond any single test, these are the capabilities your career is built from. The analyst who verifies precisely, quantifies honestly, reads exactly, and escalates well is the analyst trusted with bigger transitions — and, in time, with running them. Every technique in this guide — the reconciliation habit, the risk-impact-action flag, the "evidence, early, upward, proportionate" pattern — is usable at your desk tomorrow, and each use makes the next assessment easier.

Be patient with yourself, keep practising in small honest steps, and take pride in what your role protects: services going live safely because someone checked the evidence, someone flagged the risk, and someone told the truth at the review. That someone is you. Good luck — you are better prepared than you think.
