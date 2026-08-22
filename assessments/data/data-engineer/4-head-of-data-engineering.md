# Data Engineer (Head of Data Engineering) - Psychometric Assessment Resources

## Introduction

Welcome. This document is written for you: a head of data engineering working within the UK Government Digital and Data profession. You lead multi-functional delivery teams that build robust data services for your department, for other government departments, and for private sector partners. You inspire best practice, you build capability across a community of engineers, and you work alongside other senior leaders to identify, plan, develop and deliver data services at enterprise scale. Psychometric assessments are increasingly part of how senior digital and data appointments are made and developed, so it is well worth investing a little time to understand them and to practise.

Psychometric assessments are structured, standardised exercises that measure how you think, reason and decide. They are not tests of memory or trivia. For a senior role such as yours, they are designed to sample the genuine mental demands of the job: spotting the flaw in a pipeline design under time pressure, interpreting a budget table for a data platform migration, reading a dense cross-government data-sharing policy accurately, or choosing the wisest course of action when a stakeholder demands the impossible. Because the questions mirror real work, your everyday professional judgement is your greatest asset. Practice simply helps you show that judgement clearly, calmly and quickly under assessment conditions.

This document is organised into four main assessment sections, each of which follows the same pattern:

1. **Workplace job-specific cognitive assessment** - pattern recognition, logical deduction, error checking, prioritisation and problem solving using the artefacts you really handle: data models, integration standards, test reports and pipeline dependency maps.
2. **Workplace job-specific numeric reasoning assessment** - tables, percentages, ratios, budgets, capacity figures and performance metrics of the kind you review every week as a head of profession.
3. **Workplace job-specific verbal reasoning assessment** - dense passages drawn from policies, standards, emails and reports, followed by True / False / Cannot Say and comprehension questions.
4. **Workplace job-specific situational judgement assessment** - realistic leadership dilemmas involving your stakeholders, your engineering community and your delivery teams.

Each section explains what the assessment measures, maps it explicitly to the skills in your role profile, provides a substantial set of practice questions with fully worked explanations, and closes with preparation tips and common pitfalls. You can work through the document end to end, or dip into the section you find least familiar. Use the practice questions actively: attempt each one before reading the explanation, note where your reasoning diverged, and reflect on what the difference tells you. Approached this way, the material doubles as professional self-development, not merely exam preparation. Good luck - you bring years of hard-won engineering leadership to these assessments, and that experience will serve you well.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive ability assessment is a targeted psychometric test that measures the exact mental processes needed for your role, using practical workplace scenarios and data rather than abstract puzzles. Unlike a generic IQ test, every stimulus is drawn from the kind of material a head of data engineering genuinely handles: entity-relationship diagrams, pipeline dependency graphs, integration standards documents, test summaries, incident logs and metadata catalogues. The intent is to predict job performance by sampling the job itself.

Typical format and timing: the assessment is usually delivered online, timed at around 15 to 30 minutes, with objective scoring against a benchmark or norm group appropriate to senior digital and data roles. Many platforms are adaptive, adjusting difficulty as you answer, and most give you a few ungraded practice items first so you can get comfortable with the interface. Employers generally receive a breakdown of speed versus accuracy rather than a single raw score, so working carefully and steadily is rewarded - you do not need to rush recklessly to do well.

For a senior leader, the cognitive assessment matters for a particular reason: your decisions have a large blast radius. When you approve an integration design, set a programming standard, or triage a portfolio of problems across several delivery teams, an error in your reasoning propagates through everything your teams build. Assessors want evidence that you can hold complex structures in mind, detect inconsistencies quickly, deduce consequences rigorously, and prioritise soundly under time pressure - exactly what the following questions exercise.

### What it measures for your role

The dimensions of a cognitive assessment map directly onto the skills in your role profile:

- **Problem management**: logical deduction and root-cause analysis questions test your ability to anticipate problems, understand how a problem fits into the larger picture, and describe it precisely - the same faculties you use to build problem-solving capability in others.
- **Data modelling**: questions asking you to reverse-engineer a model from sample records, or to spot a violation of normalisation or referential integrity, test the skill of producing, maintaining and reverse-engineering data models from live systems.
- **Data integration design** and **data development process**: error-checking and consistency questions about integration standards, naming conventions and life cycle procedures test your ability to establish enterprise-scale standards and to notice when teams have drifted from them.
- **Data analysis and synthesis**: pattern-recognition questions about profiling outputs and conformed models test your ability to bring multiple data sources together and to help teams apply profiling techniques.
- **Testing**: questions about test conditions, coverage and risk test your ability to review requirements, define test conditions and identify issues and risks associated with work.
- **Programming and build (data engineering)**: sequence and dependency questions mirror your technical responsibility for all stages and iterations of a development project.
- **Metadata management**: catalogue-consistency questions test the same care for accuracy that robust metadata governance demands.

### Practice questions

**Question 1 (easy) - Pipeline dependency logic.**
Your platform team documents the following facts about a nightly batch estate: Pipeline A must complete before Pipeline B starts. Pipeline B and Pipeline C can run in parallel, but both must complete before Pipeline D starts. Pipeline C cannot start until Pipeline A completes. Pipeline E depends only on Pipeline D.

Which one of the following statements must be true?

- (a) Pipeline B must complete before Pipeline C starts.
- (b) Pipeline E cannot start until Pipeline A has completed.
- (c) Pipeline C must start before Pipeline B.
- (d) Pipeline D can start as soon as Pipeline B completes.

**Correct answer: (b).**
**Explanation:** Trace the dependency chain. E depends on D; D depends on both B and C; B and C each depend on A. Therefore nothing downstream of A - including E - can start until A completes, so (b) must be true. Option (a) is false because B and C are explicitly parallel. Option (c) states an ordering between B and C that is nowhere required. Option (d) is false because D needs C as well as B. In assessment conditions, sketch a quick directed graph; as a head of data engineering you read orchestration DAGs constantly, and putting the structure on paper prevents the classic error of confusing "can run in parallel" with "must run in a particular order".

**Question 2 (easy) - Error checking a metadata catalogue.**
Your metadata repository lists four dataset entries. Which entry contains an internal inconsistency?

- (a) Dataset: `benefit_claims_daily`; Classification: OFFICIAL; Refresh: daily at 02:00; Last refreshed: yesterday 02:04.
- (b) Dataset: `address_reference`; Classification: OFFICIAL; Refresh: monthly; Last refreshed: 11 days ago; Next refresh due: 19 days from today.
- (c) Dataset: `payments_ledger`; Classification: OFFICIAL-SENSITIVE; Refresh: weekly on Mondays; Last refreshed: last Wednesday.
- (d) Dataset: `staff_directory`; Classification: OFFICIAL; Refresh: quarterly; Last refreshed: 2 months ago.

**Correct answer: (c).**
**Explanation:** Entry (c) claims a weekly Monday refresh but records its last refresh on a Wednesday - the schedule and the history contradict each other, which is exactly the kind of drift a robust metadata governance process should surface. Entry (b) is consistent: 11 days elapsed plus 19 days remaining equals a 30-day cycle, which fits "monthly". Entries (a) and (d) contain no contradictions. This is a direct exercise of your metadata management skill: setting up governance processes that keep repositories up to date depends on being able to spot precisely this kind of inconsistency at a glance.

**Question 3 (moderate) - Reverse-engineering a data model.**
You are shown three sample rows from a live system table named `CASE_EVENTS`:

| case_id | event_type | event_date | officer_id | officer_name | officer_grade |
|---|---|---|---|---|---|
| 1041 | OPENED | 2026-03-01 | O-77 | J. Achebe | SEO |
| 1041 | REVIEWED | 2026-03-09 | O-82 | P. Singh | G7 |
| 1053 | OPENED | 2026-03-02 | O-77 | J. Achebe | SEO |

Based only on this evidence, which design weakness can you most confidently identify?

- (a) The table lacks a primary key entirely.
- (b) Officer attributes are repeated for each event, indicating the table is not normalised and officer details should live in a separate entity.
- (c) The event_date column stores dates in an inconsistent format.
- (d) case_id and officer_id should be combined into a single column.

**Correct answer: (b).**
**Explanation:** Officer O-77 appears twice with identical name and grade, showing that officer attributes depend on officer_id, not on the event - a transitive dependency that violates third normal form and creates update anomalies (if J. Achebe is promoted, multiple rows must change). This is exactly what you look for when reverse-engineering data models from a live system. Option (a) overreaches: a composite key such as (case_id, event_type, event_date) may exist; the sample cannot prove absence of a key. Option (c) is false - all dates shown share one format. Option (d) would destroy meaning rather than improve the design. Note the assessment discipline here: choose the conclusion the evidence supports most confidently, not the boldest claim.

**Question 4 (moderate) - Standards compliance deduction.**
Your published integration standard states: "All new inbound interfaces must (1) use the approved API gateway, (2) validate payloads against a registered schema, and (3) write rejected records to the quarantine store with a reason code." An audit of four interfaces built this quarter reports:

- Interface W: uses the gateway; validates against a registered schema; discards rejected records silently.
- Interface X: uses the gateway; validates against a schema held only in the developer's repository; quarantines rejects with reason codes.
- Interface Y: bypasses the gateway for performance reasons with a documented waiver; validates against a registered schema; quarantines rejects with reason codes.
- Interface Z: uses the gateway; validates against a registered schema; quarantines rejects with reason codes.

Assuming the waiver process is itself part of the standard, how many interfaces are fully compliant?

- (a) One
- (b) Two
- (c) Three
- (d) Four

**Correct answer: (b).**
**Explanation:** Z is compliant on all three clauses. Y is compliant because a documented waiver is a recognised route within the standard, and it meets clauses (2) and (3). W fails clause (3): silent discard is precisely what the quarantine requirement forbids. X fails clause (2): the schema must be *registered*, and a private repository copy does not satisfy that - the wording matters. So two interfaces are fully compliant. This question rehearses two of your core duties: ensuring adherence to the standards you establish, and reading compliance evidence with the precision needed to advise teams on the application of standards and methods.

**Question 5 (moderate) - Prioritisation under constraint.**
It is 08:30. Your four delivery teams each escalate one item, and you have time to intervene personally in only one before a 10:00 cross-government board:

- (a) Team 1: a conformed reporting model feeding a ministerial dashboard has shown stale data since 06:00; the dashboard is used in the board meeting you are attending.
- (b) Team 2: a developer requests a decision on which of two orchestration tools to adopt for a project starting next month.
- (c) Team 3: a partner department reports intermittent authentication failures on a data-sharing API, with a workaround in place.
- (d) Team 4: the weekly test report shows coverage has dropped from 82% to 78% on one service.

Which item should you address first?

**Correct answer: (a).**
**Explanation:** Apply impact and urgency jointly. Item (a) combines the highest impact (a ministerial-facing artefact is wrong) with hard urgency (the board meets at 10:00 and will rely on that dashboard); it is also the only item whose deadline precedes the meeting. Item (c) is significant but has a workaround, which reduces urgency; it belongs with the team's problem management process today, not necessarily with you personally in the next 90 minutes. Item (b) is important but has a month of runway. Item (d) is a trend worth a conversation this week, not an emergency. Strong senior prioritisation is not about doing everything; it is about correctly sequencing what only you can unblock - a core element of the problem management skill, anticipating problems and defending against them at the right time.

**Question 6 (moderate) - Pattern recognition in data profiling output.**
Your team profiles a citizen contact dataset weekly. Null rates for the `postcode` field over six weeks are: 2.1%, 2.0%, 2.2%, 2.1%, 8.9%, 9.1%. The volume of records per week is stable. Which hypothesis best fits the pattern and should be investigated first?

- (a) Citizens have suddenly stopped providing postcodes.
- (b) A change deployed around week five - such as a form change or an upstream mapping error - is dropping postcode values.
- (c) The profiling tool is miscounting nulls in all six weeks.
- (d) Weeks one to four were measured incorrectly.

**Correct answer: (b).**
**Explanation:** The signature is a step change: four stable readings around 2%, then a jump to a new stable level around 9%. Step changes in data quality metrics almost always correspond to a discrete system event - a release, a schema change, a new source coming online - not to gradual behavioural drift, which would appear as a slope. Option (a) proposes an implausible behavioural cause for a discontinuity. Options (c) and (d) attack the measurement, but the internal consistency of each period (readings tightly clustered before and after) suggests the instrument is working. Helping teams apply profiling techniques and interpret them correctly is a named element of your data analysis and synthesis skill; recognising step change versus drift is one of its most practical applications.

**Question 7 (moderate) - Logical deduction about testing.**
A test manager tells you: "Every interface that passed schema validation testing also passed volume testing. Interface K failed volume testing. Interface L passed schema validation testing." Which of the following can you validly conclude?

- (a) Interface K failed schema validation testing.
- (b) Interface L passed volume testing.
- (c) Interface K passed schema validation testing.
- (d) Interface L failed volume testing at first attempt.

**Correct answer: both (a) and (b) are valid - the assessment answer is (b) if only one may be chosen; note carefully why (a) is also entailed.**
**Explanation:** The rule is: pass(schema) implies pass(volume). Its contrapositive is: fail(volume) implies fail(schema). Interface K failed volume testing, so by the contrapositive K must have failed schema validation - conclusion (a) follows. Interface L passed schema validation, so by the rule directly L passed volume testing - conclusion (b) follows. Option (c) contradicts the contrapositive. Option (d) adds "at first attempt", which the premises never mention - a classic distractor that smuggles in unstated detail. Real assessments usually offer only one entailed option; this question deliberately offers two so you practise both the direct inference and the contrapositive, the two moves that underpin rigorous review of requirements, specifications and test conditions.

**Question 8 (hard) - Root cause isolation.**
A conformed analytical model combines three sources: HR system (people), finance system (cost centres), and estates system (locations). Analysts report that 4% of people records fail to join to a cost centre. You establish these facts: (1) the HR extract row count matches the HR system exactly; (2) every cost centre code in the finance extract is present in the reference list; (3) 4% of HR records carry cost centre codes marked as "closed" in the reference list; (4) the join logic excludes closed cost centres.

What is the most precise statement of the root cause?

- (a) The finance extract is incomplete.
- (b) The HR system contains people assigned to cost centres that have since been closed, and the model's join rule excludes closed cost centres rather than handling them.
- (c) The reference list is out of date.
- (d) The join logic contains a coding defect.

**Correct answer: (b).**
**Explanation:** Work through the evidence eliminatively. Fact (1) clears the HR extract of data loss. Fact (2) clears the finance extract of invalid codes, ruling out (a). Fact (3) shows the failing 4% are exactly the records pointing at closed cost centres, and fact (4) shows the model excludes those by design - so the join is behaving as specified, ruling out (d); the defect is in the *rule*, not the code. Option (c) is the subtle distractor: the reference list correctly records the cost centres as closed; it is not stale. The precise root cause is a business-reality mismatch: people legitimately remain assigned to closed cost centres during reorganisations, and the model design failed to anticipate it. Identifying and describing problems precisely - and helping others describe them - is a named behaviour at your level, and the discipline of separating "code defect" from "design assumption defect" is what makes your problem descriptions actionable.

**Question 9 (hard) - Sequencing a programme of work.**
You must sequence five workstreams for an enterprise data integration programme. Constraints: the canonical data model (M) must be signed off before either the ingestion framework build (I) or the metadata repository setup (R) can complete. The quality rules engine (Q) requires the ingestion framework (I) to be complete. Analyst onboarding (O) requires both R and Q. Only two workstreams can run at once due to resourcing.

Which sequencing plan is feasible and finishes O earliest, assuming each workstream takes one quarter?

- (a) Q1: M alone; Q2: I and R; Q3: Q and O; Q4: nothing.
- (b) Q1: M and I; Q2: R and Q; Q3: O.
- (c) Q1: M alone; Q2: I and R; Q3: Q alone; Q4: O.
- (d) Q1: I and R; Q2: M and Q; Q3: O.

**Correct answer: (c).**
**Explanation:** First test feasibility. Plan (d) starts I and R before M is signed off - infeasible. Plan (b) runs I concurrently with M, but I cannot complete before M is signed off, so completing both in Q1 breaks the constraint (a subtle point: "must be signed off before I can complete" allows overlap of start but not completion in the same quarter if sign-off comes at quarter end; under assessment conventions treat it as infeasible). Plan (a) schedules O in Q3 alongside Q, but O requires Q to be *complete*, so O cannot run concurrently with Q - infeasible. Plan (c) respects every constraint: M finishes Q1; I and R finish Q2; Q (needing I) finishes Q3; O (needing R and Q) finishes Q4. When you manage resources so that data services work effectively at enterprise level, this is precisely the reasoning: distinguish "starts after" from "completes after", and test each plan against every constraint rather than accepting the first that looks tidy.

**Question 10 (hard) - Spotting the flawed inference in a horizon-scanning brief.**
A supplier's whitepaper argues: "Departments that adopted our real-time streaming platform reported a 40% reduction in data incident volumes within a year. Therefore, adopting streaming architectures reduces data incidents." As the leader responsible for horizon-scanning and introducing innovative ways of working, which is the strongest single criticism of this inference?

- (a) The sample may exclude departments whose adoption failed, and adopters may differ systematically from non-adopters, so the correlation cannot establish causation.
- (b) Streaming platforms are more expensive than batch platforms.
- (c) A 40% reduction is too small to matter.
- (d) Government departments should not use private sector case studies.

**Correct answer: (a).**
**Explanation:** The argument generalises from self-selected, possibly survivor-biased evidence to a causal claim. Departments that chose and successfully deployed the platform likely already had stronger engineering practices - a confound - and failed adoptions rarely appear in vendor whitepapers - survivorship bias. Option (a) names both defects and is the classic, decisive critique. Option (b) may be true but attacks cost, not the inference. Option (c) is factually weak (40% is material) and again does not address the logic. Option (d) is an irrelevant policy assertion. Your data innovation skill asks you to investigate emerging trends and horizon-scan for the organisation; the cognitive core of that duty is exactly this - separating genuine signal from persuasive but logically unsound vendor narrative before recommending change.

**Question 11 (moderate) - Test condition coverage.**
A specification for a new ingestion service states: "The service must accept files up to 2 GB; reject files with an invalid schema; and process a valid 2 GB file within 30 minutes." Your test manager proposes three test conditions: (1) submit a valid 1 GB file and confirm acceptance; (2) submit an invalid-schema file and confirm rejection; (3) submit a valid 2 GB file and confirm processing completes within 30 minutes.

Which requirement aspect remains untested?

- (a) Rejection of invalid schemas.
- (b) Behaviour at and just beyond the 2 GB boundary (e.g. that a file slightly over 2 GB is rejected or handled as specified).
- (c) Processing time of the 2 GB file.
- (d) Acceptance of valid files.

**Correct answer: (b).**
**Explanation:** Conditions (1)-(3) cover valid acceptance, invalid-schema rejection, and the performance clause. What no condition exercises is the *upper boundary itself from the other side*: what happens with a 2.1 GB file? Boundary value analysis says defects cluster at limits, so a complete condition set tests at the boundary and just beyond it. Reviewing requirements and specifications and defining test conditions is a named element of your testing skill; at head-of level your added value is rarely writing the tests yourself but asking precisely this question - "which boundary is unexercised?" - in a review, and coaching test managers to ask it too.

**Question 12 (hard) - Conformed model consistency.**
Two source systems feed a conformed customer model. System P holds 120,000 customer records; System F holds 95,000. Matching analysis shows 80,000 customers exist in both systems. The conformed model, built as a full union of distinct customers, contains 142,000 records. What does this indicate?

- (a) The model is correct.
- (b) The model contains about 7,000 duplicate or spurious records, because the expected distinct count is 120,000 + 95,000 - 80,000 = 135,000.
- (c) The model has lost about 7,000 records.
- (d) The matching analysis must be wrong because the numbers cannot be compared.

**Correct answer: (b).**
**Explanation:** Apply the inclusion-exclusion principle: distinct customers = |P| + |F| - |P ∩ F| = 120,000 + 95,000 - 80,000 = 135,000. The model holds 142,000, which is 7,000 *more* than expected - the signature of failed de-duplication, where some of the 80,000 overlapping customers were not matched and entered twice. Option (c) reverses the direction of the discrepancy. Option (d) surrenders too early; the figures are directly comparable. Bringing multiple data sources together in a conformed model for analysis is a named element of your data analysis and synthesis skill, and the inclusion-exclusion check is one of the fastest smoke tests you can teach your teams for validating any entity-resolution exercise.

**Question 13 (moderate) - Odd one out in standards.**
Your teams follow a naming standard: raw layer tables are prefixed `raw_`, curated layer tables `cur_`, and published data products `pub_`; all names are lower-case with underscores; source system code appears as a suffix on raw tables only. Which table name violates the standard?

- (a) `raw_payments_sap`
- (b) `cur_customer_addresses`
- (c) `pub_monthly_spend_sap`
- (d) `raw_hr_positions_wfm`

**Correct answer: (c).**
**Explanation:** The suffix `_sap` is a source system code, and the standard permits source codes on raw tables *only*. A published data product should be source-agnostic - that is much of the point of the published layer - so `pub_monthly_spend_sap` breaks the rule (and arguably the architecture). Options (a), (b) and (d) each conform. Trivial as it looks, this is the everyday texture of establishing standards, keeping them up to date and ensuring adherence: violations are rarely dramatic, and the leaders who catch them are the ones who have internalised the standard well enough to notice a suffix in the wrong layer within seconds.

### Preparation tips

- **Rehearse with your own artefacts.** Before the assessment, spend an evening reading a pipeline DAG, a data model and a test report from your own estate at speed, summarising each in one sentence. The stimuli in job-specific assessments will feel familiar, and recent fluency compounds that advantage.
- **Sketch structure immediately.** For dependency and deduction questions, draw the graph or write the rule (and its contrapositive) before looking at the options. Senior candidates lose marks by holding structure in their heads to save time - the sketch is faster overall.
- **Answer only from the evidence given.** Your experience will tempt you to fill gaps with what is usually true in real estates. Assessments reward the conclusion the stated facts support, no more.
- **Practise pace, not panic.** At 15-30 minutes total, budget roughly a minute per question, bank the easy ones fast, and mark hard ones to revisit. Accuracy-versus-speed reporting means a wrong rushed answer is worse than a skipped one on most platforms.
- **Trust your professional maturity.** You triage harder problems than these weekly. Treat each question as a small stand-up escalation: what do I know, what follows, what matters first?

### Common pitfalls

- **Confusing "can" with "must".** In dependency and logic items, options that convert permission into obligation (or vice versa) are the most common trap for experienced engineers who pattern-match to familiar architectures.
- **Choosing the boldest diagnosis rather than the best-supported one.** As in Question 3, the correct answer is often the modest claim the evidence fully warrants, not the sweeping one it merely suggests.
- **Importing outside knowledge.** Knowing how your department's real metadata catalogue behaves is irrelevant; only the stated facts count.
- **Time-sink questions.** Multi-constraint sequencing items like Question 9 can absorb five minutes. If a question resists you after ninety seconds, flag it and move on - the marks are the same elsewhere.
- **Skimming compliance wording.** Words like "registered", "documented" and "only" carry the whole question, as in Questions 4 and 13. Read the standard's clauses as if you had written them - because in your role, you usually did.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment evaluates your ability to analyse, interpret and make sound decisions using numerical data of the kind your role genuinely generates. It mimics the data-handling demands of leading enterprise data services: platform budgets, cloud consumption tables, pipeline throughput and capacity figures, service level percentages, team resourcing plans and data quality metrics. The emphasis is business mathematics - percentages, ratios, rates, cost-benefit comparisons and projections - not abstract formulae or advanced statistics.

Typical format and timing: online, strictly timed (often around 60 to 90 seconds per question across 20-25 minutes), with an onscreen calculator usually allowed or provided. The test prioritises interpretation over mental arithmetic: the hard part is extracting the right numbers from a realistic table or chart quickly and combining them correctly, not the calculation itself. Questions frequently include scale qualifiers ("figures in thousands", "per month") that change the answer entirely if missed.

Why it matters for your role: as head of data engineering you are accountable for decisions with significant financial and operational consequences - whether a platform migration is affordable, whether a pipeline estate can absorb a new department's workload, whether a team's velocity justifies its cost, whether an SLA breach is a blip or a trend. Senior stakeholders will rarely check your arithmetic; they will act on your interpretation. The assessment samples exactly that: can you read operational and financial data accurately at speed, and draw the conclusion the numbers actually support?

### What it measures for your role

- **Data development process** - "manage resources to ensure that data services work effectively at an enterprise level": budget, resourcing and capacity questions test the quantitative core of this duty.
- **Data analysis and synthesis**: questions requiring you to combine figures from multiple tables mirror bringing multiple data sources together in a conformed model, and interpreting profiling metrics.
- **Problem management**: trend and threshold questions (error rates, SLA percentages) test your ability to anticipate problems and judge when a number signals a problem worth defending against.
- **Testing**: defect and coverage arithmetic tests your ability to analyse and report test activities and results.
- **Data innovation**: cost-benefit and projection questions mirror evaluating emerging approaches and building the numerical case for introducing new ways of working.
- **Communicating between the technical and non-technical**: every worked explanation below models the discipline of showing your arithmetic plainly - the same clarity you need when presenting figures to boards and non-technical stakeholders.

### Practice questions

**Question 1 (easy) - Percentage change in pipeline failures.**
Your monthly engineering report shows pipeline failure counts across the estate: January 140, February 119. What is the percentage change from January to February?

- (a) A decrease of 21%
- (b) A decrease of 15%
- (c) A decrease of 17.6%
- (d) An increase of 15%

**Correct answer: (b).**
**Explanation:** Percentage change = (new − old) ÷ old × 100 = (119 − 140) ÷ 140 × 100 = −21 ÷ 140 × 100 = −15%. So failures fell by 15%. Option (a) confuses the absolute change (21 failures) with the percentage. Option (c) is the result of dividing by the new value (21 ÷ 119 = 17.6%), a classic error - always divide by the *starting* value. Verify direction sanity: February is lower, so any "increase" option is instantly eliminable, halving your search space before you calculate.

**Question 2 (easy) - Storage capacity headroom.**
Your analytical platform has 480 TB of provisioned storage and currently holds 312 TB. A new data service is projected to add 9 TB per month. Assuming no other growth and no purge, in how many whole months will the platform exceed 90% of provisioned capacity?

- (a) 12 months
- (b) 13 months
- (c) 14 months
- (d) 18 months

**Correct answer: (c).**
**Explanation:** 90% of 480 TB = 432 TB. Headroom to that threshold = 432 − 312 = 120 TB. At 9 TB/month, 120 ÷ 9 = 13.33 months. After 13 whole months the platform holds 312 + 117 = 429 TB (still under 432); after 14 months it holds 312 + 126 = 438 TB, exceeding the threshold. So the answer is 14 - the question asks when the platform *exceeds* the threshold, so you must round up and check the boundary month. Capacity arithmetic like this underpins managing resources so data services work effectively at enterprise level; the rounding direction is where marks (and real-world procurement lead times) are won or lost.

**Question 3 (moderate) - Cloud cost comparison.**
Two ingestion architectures are costed for a new cross-government data service:

| Cost element | Option A (batch) | Option B (streaming) |
|---|---|---|
| Fixed platform cost per month | £18,000 | £26,000 |
| Cost per million records processed | £42 | £28 |

The service will process 400 million records per month. What is the monthly cost difference between the options?

- (a) Option B costs £2,400 less per month
- (b) Option B costs £8,000 more per month
- (c) Option A costs £2,400 less per month
- (d) The options cost the same

**Correct answer: (c).**
**Explanation:** Compute each total as fixed cost plus variable cost. Option A: £18,000 + (400 × £42) = £18,000 + £16,800 = £34,800. Option B: £26,000 + (400 × £28) = £26,000 + £11,200 = £37,200. Difference = £37,200 − £34,800 = £2,400, with Option A the cheaper - which is what option (c) states. Option (a) reverses the direction: B's lower unit rate does not overcome its higher fixed cost at this volume, and options that flip the direction of a correct figure are among the most common numeric-test distractors, so always re-read which architecture the option credits. Option (b) is the difference in fixed costs alone, ignoring the variable side. Fixed-plus-variable comparisons also carry a break-even insight worth extracting: the options cost the same where £18,000 + 42v = £26,000 + 28v, i.e. 14v = 8,000, so v ≈ 571 million records per month - above that volume, streaming becomes cheaper. When you horizon-scan and build the business case for an innovative architecture, presenting the break-even volume rather than a single-point comparison is one of the most persuasive numerical moves you can make with non-technical stakeholders, because it converts "which is cheaper?" into "under what conditions does each win?".

**Question 4 (moderate) - SLA availability.**
A data-sharing API you provide to another department has a 99.5% monthly availability SLA. In a 30-day month, what is the maximum downtime allowed, and did the service - which recorded 4 hours 20 minutes of downtime - breach its SLA?

- (a) Maximum 3.6 hours; the service breached the SLA
- (b) Maximum 3.6 hours; the service met the SLA
- (c) Maximum 7.2 hours; the service met the SLA
- (d) Maximum 7.2 hours; the service breached the SLA

**Correct answer: (a).**
**Explanation:** A 30-day month contains 30 × 24 = 720 hours. Allowed downtime = 0.5% of 720 = 0.005 × 720 = 3.6 hours = 3 hours 36 minutes. Recorded downtime was 4 hours 20 minutes, which exceeds 3 hours 36 minutes, so the SLA was breached. Option (c)/(d)'s 7.2 hours comes from using 1% instead of 0.5% - always convert "99.5% availability" to its complement (0.5% unavailability) explicitly before calculating. Note also the unit trap: 3.6 hours is 3:36, not 3:60. As the leader who negotiates and reports on these SLAs with partner departments, this conversion should become reflexive.

**Question 5 (moderate) - Team resourcing ratio.**
Your data engineering community comprises 48 engineers across four teams. The agreed operating model requires a ratio of one senior engineer to every three engineers at other grades. You currently have 10 senior engineers. How many more senior engineers do you need to meet the ratio, assuming total headcount stays at 48?

- (a) 2
- (b) 6
- (c) 12
- (d) 4

**Correct answer: (a).**
**Explanation:** A 1:3 ratio of senior to other grades means seniors are 1 part in 4 total parts, so required seniors = 48 ÷ 4 = 12. You have 10, so you need 12 − 10 = 2 more (promoted or recruited, with two non-senior posts converting). The common error is reading "1 to every 3" as 1/3 of the total (16 seniors, giving answer 6); a ratio of 1:3 makes the first term a quarter of the whole, not a third. Ratio-to-fraction conversion appears constantly in workforce planning - one of the least glamorous but most frequent numerical tasks in building data engineering capability and providing career development pathways for the community.

**Question 6 (moderate) - Data quality improvement.**
A profiling report on a conformed customer model shows 2.4 million records, of which 6.5% fail address validation. Your team deploys an improved standardisation rule that resolves 70% of the failing records. How many records still fail?

- (a) 46,800
- (b) 109,200
- (c) 156,000
- (d) 63,000

**Correct answer: (a).**
**Explanation:** Failing records = 6.5% × 2,400,000 = 0.065 × 2,400,000 = 156,000. The fix resolves 70% of these: 0.70 × 156,000 = 109,200 resolved. Remaining failures = 156,000 − 109,200 = 46,800. Option (c) is the original failure count (stopping too early); option (b) is the number *resolved* rather than remaining (answering the wrong question). Two-step percentage problems reward writing the intermediate figure down: under time pressure, the single biggest cause of error is holding 156,000 in your head while computing the second step. When you report this to a data governance board, the same three numbers - baseline, resolved, residual - are exactly the story to tell.

**Question 7 (moderate) - Throughput and deadline.**
An overnight batch window runs from 01:00 to 06:00. A new ingestion job must load 540 million records, and the pipeline sustains 45 million records per hour. Existing jobs already occupy the window until 02:30. Can the new job complete within the window, and with how much margin or shortfall?

- (a) Yes, with 30 minutes to spare
- (b) No, it overruns by 8.5 hours
- (c) No, it overruns by 8 hours 30 minutes minus the window - it needs 12 hours in total
- (d) No, it needs 12 hours of processing but only 3.5 hours are available, an 8.5-hour shortfall

**Correct answer: (d).**
**Explanation:** Processing time needed = 540 ÷ 45 = 12 hours. Available window = 02:30 to 06:00 = 3.5 hours. Shortfall = 12 − 3.5 = 8.5 hours. So the job cannot complete; it needs 12 hours but has 3.5, an 8.5-hour shortfall - option (d) states this precisely, while (b) and (c) garble the same numbers. The management insight matters more than the arithmetic: no amount of scheduling juggles 12 hours into 3.5, so the real options are parallelising the load (e.g. 4 parallel streams ≈ 3 hours), incremental loading, or challenging the requirement. Enterprise-scale integration procedures live or die on this kind of capacity arithmetic being done *before* go-live, not after the first breached morning deadline.

**Question 8 (hard) - Budget allocation with constraints.**
Your annual data platform budget is £2.4 million, allocated: 45% staff, 30% cloud infrastructure, 15% licences, 10% training and community development. Mid-year, cloud costs rise 20% for the second half of the year while all other categories stay on plan. If the total budget cannot increase, and the overrun must come entirely from the training allocation, what percentage of the original training budget remains for the second half of the year?

- (a) 70%
- (b) 40%
- (c) 55%
- (d) 25%

**Correct answer: (b).**
**Explanation:** Work in annual figures first. Cloud budget = 30% × £2.4m = £720,000, i.e. £360,000 per half-year. A 20% rise for the second half adds 0.20 × £360,000 = £72,000. Training budget = 10% × £2.4m = £240,000, i.e. £120,000 per half. The £72,000 overrun comes from the second-half training allocation: £120,000 − £72,000 = £48,000 remains. As a percentage of the original *half-year* training budget: 48,000 ÷ 120,000 = 40%. Option (a) subtracts £72k from the annual £240k (70%) - misreading the timeframe; option (d) divides £48k by an incorrect base. Note what the numbers imply for your leadership: sacrificing 60% of half-year community development to absorb a cloud overrun is exactly the trade-off a head of data engineering should surface to their director rather than absorb silently - the arithmetic is the easy part; deciding whether the trade is acceptable is the job.

**Question 9 (hard) - Interpreting a multi-team delivery table.**
Quarterly figures for your four delivery teams (story points delivered, and defects escaping to production):

| Team | Q1 points | Q2 points | Q1 defects | Q2 defects |
|---|---|---|---|---|
| Ingest | 240 | 276 | 12 | 12 |
| Platform | 180 | 171 | 9 | 6 |
| Products | 300 | 330 | 10 | 22 |
| Integration | 210 | 231 | 7 | 7 |

Which team's defect rate per 100 story points worsened the most from Q1 to Q2?

- (a) Ingest
- (b) Platform
- (c) Products
- (d) Integration

**Correct answer: (c).**
**Explanation:** Compute defects per 100 points each quarter. Ingest: Q1 = 12/240 × 100 = 5.0; Q2 = 12/276 × 100 ≈ 4.3 - improved. Platform: Q1 = 9/180 × 100 = 5.0; Q2 = 6/171 × 100 ≈ 3.5 - improved. Products: Q1 = 10/300 × 100 ≈ 3.3; Q2 = 22/330 × 100 ≈ 6.7 - roughly doubled, a worsening of about 3.3 points. Integration: Q1 = 7/210 × 100 ≈ 3.3; Q2 = 7/231 × 100 ≈ 3.0 - improved. Products worsened most. The trap is judging by raw defect counts (Ingest and Integration look "flat", Products merely "up a bit against higher delivery") - rates, not counts, are comparable across teams of different sizes and velocities. As the leader analysing and reporting test activities and results across an estate, normalising to a rate before comparing is the single most important habit this question rehearses.

**Question 10 (hard) - Migration projection with compound growth.**
A legacy warehouse holds 200 TB and grows at 5% per quarter (compound). Your migration plan moves 40 TB per quarter to the new platform, starting now. After two quarters, approximately how much data remains on the legacy platform? (Assume growth applies to the remaining legacy data at the end of each quarter, after that quarter's migration.)

- (a) 120.0 TB
- (b) 138.5 TB
- (c) 134.4 TB
- (d) 128.0 TB

**Correct answer: (c).**
**Explanation:** Follow the stated order of operations strictly - migration first, then growth, in each quarter. Quarter 1: 200 − 40 = 160 TB remaining, then growth: 160 × 1.05 = 168 TB. Quarter 2: 168 − 40 = 128 TB remaining, then growth: 128 × 1.05 = 134.4 TB. The answer is 134.4 TB. Option (d), 128.0 TB, is the balance *before* the second quarter's growth is applied - stopping one step early. Option (b), 138.5 TB, is what you get if you apply growth *before* migration each quarter (200 × 1.05 = 210, − 40 = 170; 170 × 1.05 = 178.5, − 40 = 138.5) - the reversed convention. Option (a) ignores growth entirely (200 − 80 = 120). The lesson: compound-growth-with-drawdown questions hinge entirely on operation ordering, and good assessments state it in the stem, as this one does in its bracketed assumption - compute strictly in the stated order and write each quarter's balance down rather than chaining it mentally. The same issue is live in your real migration planning: whether growth is booked before or after each migration tranche can move a decommissioning business case by whole quarters, which is why finance colleagues will (rightly) ask you to state the convention explicitly, and why a migration that removes 40 TB per quarter against 5% compound growth is barely outrunning the growth at all - a point worth making to any board that believes the legacy estate is "shrinking fast".

**Question 11 (moderate) - Defect detection percentage.**
In user acceptance testing for a new data service, your teams raised 180 defects. Post go-live, a further 20 defects were found in the first month that existed before release. What was the defect detection percentage of testing (defects found in testing as a percentage of all pre-release defects)?

- (a) 90%
- (b) 88.9%
- (c) 11.1%
- (d) 111%

**Correct answer: (a).**
**Explanation:** Total pre-release defects = 180 + 20 = 200. Detection percentage = 180 ÷ 200 × 100 = 90%. Option (b) divides 180 by an incorrect base; 180/200 is exactly 90%, whereas 160/180 or similar slips produce 88.9%. Option (c) is the escape rate (20/180 misused) and option (d) is arithmetically impossible for a detection measure. Defect detection percentage is a standard measure you should expect in any mature test report, and it directly serves your testing skill - analysing and reporting test activities and results - as well as your problem management duty to quantify how well the estate defends against problems before they reach users.

**Question 12 (moderate) - Weighted average for a conformed model.**
You conform three sources into a single citizen contact model. Source volumes and duplicate rates are: Source 1 - 1.2 million records, 4% duplicates; Source 2 - 0.6 million records, 9% duplicates; Source 3 - 0.2 million records, 15% duplicates. What is the overall duplicate rate across all records?

- (a) 9.3%
- (b) 6.6%
- (c) 5.4%
- (d) 7.0%

**Correct answer: (b).**
**Explanation:** Weight each rate by volume. Duplicates: Source 1 = 0.04 × 1,200,000 = 48,000; Source 2 = 0.09 × 600,000 = 54,000; Source 3 = 0.15 × 200,000 = 30,000. Total duplicates = 132,000. Total records = 2,000,000. Overall rate = 132,000 ÷ 2,000,000 = 6.6%. Option (a) is the simple (unweighted) mean of 4%, 9% and 15% - the classic error this question exists to punish. Unweighted averaging of rates is wrong whenever the underlying populations differ in size, which in data engineering is essentially always. When you help teams apply data profiling techniques across sources of very different scales, insisting on volume-weighted quality metrics is one of the simplest ways you raise the analytical standard of the whole community.

**Question 13 (hard) - Cost per outcome for an innovation pilot.**
You pilot two approaches to automated metadata capture. Approach P costs £84,000 and correctly catalogued 5,600 data assets. Approach Q costs £59,500 and correctly catalogued 3,500 data assets. Your director asks: "Which gives better value, and by how much per asset?"

- (a) P at £15 per asset, Q at £17 per asset; P is £2 per asset better
- (b) P at £15 per asset, Q at £17 per asset; Q is £2 per asset better
- (c) P at £6.67 per asset, Q at £5.88 per asset; Q is better
- (d) Q is better because it costs £24,500 less overall

**Correct answer: (a).**
**Explanation:** Unit cost P = £84,000 ÷ 5,600 = £15 per asset. Unit cost Q = £59,500 ÷ 3,500 = £17 per asset. P achieves the outcome £2 per asset more cheaply, so P offers better value per asset - option (a). Option (d) commits the total-cost fallacy: Q spends less but achieves proportionally less still; value questions require a unit rate, not a total. Option (c) inverts the divisions (assets ÷ cost, mangled). Note the leadership layer: unit cost is necessary but not sufficient - coverage, quality of the catalogue entries and scalability matter too - and saying so, after giving the crisp £15 versus £17 answer, is exactly how you communicate between the technical and the non-technical: lead with the number the director asked for, then add the caveat that keeps the decision sound.

**Question 14 (moderate) - Percentage points versus percentages.**
Your quarterly performance pack states: "Pipeline first-time success rate improved from 92% to 95% this quarter." A board member asks whether that is "a 3% improvement". Which statement is numerically correct?

- (a) Yes - the rate improved by exactly 3%.
- (b) The rate improved by 3 percentage points, which is a relative improvement of about 3.3%; and the failure rate fell from 8% to 5%, a relative reduction of 37.5%.
- (c) The failure rate fell by 3%, so the two statements are equivalent.
- (d) The improvement cannot be quantified without volume figures.

**Correct answer: (b).**
**Explanation:** Distinguish percentage *points* from percentages. The success rate rose by 95 − 92 = 3 percentage points. As a relative change that is 3 ÷ 92 × 100 ≈ 3.3%. Meanwhile the failure rate fell from 8% to 5%, a fall of 3 percentage points but a relative reduction of 3 ÷ 8 × 100 = 37.5% - a far more striking (and equally honest) way to state the same improvement. Option (a) conflates points with percent; option (c) repeats the conflation on the failure side; option (d) is wrong because rates can be compared without volumes (volumes would matter only for absolute counts). This distinction is not pedantry: when you represent your community's performance to large audiences inside and outside the organisation, "we cut failures by 37.5%" and "we improved success by 3%" describe the same quarter, and choosing the framing - while being ready to show both calculations - is a core skill of communicating between the technical and the non-technical with integrity.

### Preparation tips

- **Rebuild fluency with the core four.** Percentage change, ratios, weighted averages and unit rates cover most questions at this level. Thirty minutes of practice on each, with your own platform's real figures, restores speed that day-to-day delegation may have dulled.
- **Read the units and qualifiers first.** Before touching any numbers, scan for "per month", "in thousands", "TB", "per 100 points". Most wrong answers at senior level are unit errors, not arithmetic errors.
- **Write intermediate results down.** Two-step problems (find the subtotal, then operate on it) are where held-in-head figures go wrong. The onscreen calculator handles the arithmetic; your notepad handles the structure.
- **Sanity-check direction and magnitude.** Is the answer supposed to be an increase or a decrease? Bigger or smaller than the starting figure? A two-second sanity check eliminates half the options before you calculate, as in Question 1.
- **Practise the executive summary.** After each practice question, say the answer aloud in one sentence as if briefing your director. This cements interpretation - the skill actually being tested - and doubles as rehearsal for the stakeholder communication your role demands daily.

### Common pitfalls

- **Misreading chart and table labels** - confusing monthly with quarterly data, or missing scale qualifiers like "in thousands". At your level the tables resemble ones you sign off weekly, which breeds dangerous over-familiarity: read the stimulus as if it were a supplier's invoice.
- **Dividing by the wrong base** - percentage change uses the original value; detection rates use the *total* defect population; weighted averages use total volume. Questions 1, 11 and 12 each turn on the base.
- **Over-calculating** - performing exact multi-decimal work when estimation identifies the only plausible option. If options are far apart, round aggressively and move on.
- **Total-cost fallacy** - judging value by the smaller invoice rather than the unit rate, as in Question 13. Assessors include this trap because real procurement decisions fail this way.
- **Time-sink questions** - a single compound-growth item like Question 10 can consume four questions' worth of time. Bank the accessible marks first; return if time allows.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment evaluates how well you understand, analyse and draw correct conclusions from written business information that mirrors the exact reading demands of your role. For a head of data engineering, that means dense material: cross-government data-sharing agreements, technology standards, governance board papers, escalation emails from partner departments, supplier proposals and test summary reports. The questions typically require a strict choice between **True** (the passage logically entails the statement), **False** (the passage contradicts it), or **Cannot Say** (the passage provides insufficient information either way), plus some multiple-choice comprehension items about main arguments and implications.

Two rules define the format. First, fact-based logic: you must answer based strictly on the text provided, deliberately setting aside your considerable outside knowledge - what is true in your department is irrelevant if the passage does not say it. Second, time pressure: tests usually allow less than a minute per question, simulating the reality of absorbing a board paper minutes before the meeting starts.

Why it matters for your role: your role profile puts communication at its centre - mediating between people, managing stakeholder expectations, moderating difficult discussions about high-risk and complex topics within constrained timescales, and speaking on behalf of the community to large audiences. Every one of those duties rests on a prior skill: reading precisely. A head of data engineering who misreads a data-sharing clause, or asserts something a policy does not actually say, damages trust at senior levels where it is hardest to rebuild. Verbal reasoning assessments sample exactly this precision.

### What it measures for your role

- **Communicating between the technical and non-technical**: comprehension items test whether you extract the core argument from dense text - the prerequisite for translating it faithfully for ministers, boards and citizens.
- **Data integration design** - "establish standards, keep them up to date and ensure adherence": True/False/Cannot Say items on standards documents test whether you read normative language ("must", "should", "may") with the precision that writing and enforcing standards demands.
- **Metadata management** - "communicate the value of metadata repositories": passages about governance test your grasp of exactly what a policy commits the organisation to.
- **Problem management** - "identify and describe problems, and help others to describe them": distinguishing what a report states, implies and omits is the reading half of precise problem description.
- **Data innovation** - "investigate emerging trends... perform horizon-scanning": critical-reading items about supplier and industry claims test your defence against persuasive overstatement.
- **Testing** - "analyse and report test activities and results": comprehension of test reports depends on separating recorded fact from inference.

### Practice questions

**Passage A - Cross-government data-sharing agreement (for Questions 1-4).**
"Under this agreement, the Provider department will make the Address Reference Extract available to the Recipient department each calendar month, no later than the fifth working day. The Extract must be transferred exclusively through the approved secure transfer service; transfer by any other mechanism, including departmental email, constitutes a reportable incident. The Recipient may use the Extract solely for the validation of citizen correspondence addresses and must not link it to any other dataset without the prior written consent of the Provider's Data Governance Board. Consent decisions will normally be issued within twenty working days of a complete application. The Recipient must delete each monthly Extract within forty working days of receipt, except where a linking consent is in force, in which case retention terms will be specified in the consent instrument."

**Question 1 (easy).** True, False, or Cannot Say: "The Recipient may link the Extract to other datasets if the Provider's Data Governance Board has given prior written consent."

**Correct answer: True.**
**Explanation:** The passage states the Recipient "must not link it to any other dataset *without* the prior written consent" of the Board. The contrapositive reading is that linking with such consent is permitted - the prohibition is expressly conditional. Notice the reasoning move: converting "must not X without Y" into "may X with Y" is a valid reading of conditional prohibition. This mirrors how you must read data-sharing clauses daily when establishing enterprise-scale integration procedures involving other departments.

**Question 2 (moderate).** True, False, or Cannot Say: "Consent decisions are always issued within twenty working days of a complete application."

**Correct answer: False.**
**Explanation:** The passage says decisions "will *normally* be issued within twenty working days". "Normally" explicitly allows exceptions, so the claim that they are *always* issued within that period contradicts the qualified wording. This is the single most tested distinction in verbal reasoning at senior level: qualified commitments ("normally", "typically", "in most cases") versus absolute ones ("always", "must", "in all cases"). When you manage stakeholder expectations about turnaround times, the difference between "normally twenty days" and "twenty days" is precisely the gap in which expectation management lives.

**Question 3 (moderate).** True, False, or Cannot Say: "Transferring the Extract via a commercial file-sharing website would constitute a reportable incident."

**Correct answer: True.**
**Explanation:** The agreement requires transfer "exclusively through the approved secure transfer service" and states that "transfer by any other mechanism, including departmental email, constitutes a reportable incident". A commercial file-sharing website is a mechanism other than the approved service, so it falls within "any other mechanism". The phrase "including departmental email" gives an example; it does not limit the rule to email - "including" signals a non-exhaustive list. Reading "including" as exhaustive is a common error that this question is designed to catch.

**Question 4 (hard).** True, False, or Cannot Say: "If no linking consent is in force, the Recipient must delete each monthly Extract within forty working days of the fifth working day of the month."

**Correct answer: False.**
**Explanation:** The deletion clock runs from *receipt* ("within forty working days of receipt"), not from the fifth working day. The fifth working day is merely the latest permitted delivery date; the Extract could arrive earlier, in which case the deletion deadline would be earlier too. The statement substitutes the delivery deadline for the receipt date, so it misstates the rule and is False rather than Cannot Say - the passage gives enough information to identify the contradiction. Anchoring obligations to the correct trigger event is exactly the precision your teams need when you set retention rules in integration procedures, and it is the kind of subtle substitution that dense agreements hide.

**Passage B - Draft engineering standard (for Questions 5-7).**
"All data pipelines deployed to the production environment must emit structured run-telemetry to the central observability service. Pipelines classified as business-critical must, in addition, define automated alerting with a named on-call rota. Teams should adopt the shared ingestion framework for new pipelines; teams choosing an alternative framework must record the decision and its rationale in the architecture decision log before the first production deployment. This standard applies to pipelines built or substantially modified after 1 April; pipelines predating that date are expected to achieve compliance at their next substantial modification."

**Question 5 (easy).** True, False, or Cannot Say: "A team may build a new pipeline on an alternative framework provided it records the decision and rationale in the architecture decision log before first production deployment."

**Correct answer: True.**
**Explanation:** The standard says teams "should" adopt the shared framework - a recommendation, not an obligation - and then explicitly provides the route for alternatives: record the decision and rationale in the log before first production deployment. The statement matches this permission and its condition exactly. The must/should distinction is the load-bearing vocabulary of standards documents (deliberately echoing RFC-style normative language); as the leader who establishes standards and keeps them up to date, you read and write these verbs for a living, and the assessment rewards that fluency.

**Question 6 (moderate).** True, False, or Cannot Say: "A business-critical pipeline that emits run-telemetry but has no automated alerting is compliant with the standard."

**Correct answer: False.**
**Explanation:** Business-critical pipelines "must, in addition, define automated alerting with a named on-call rota". A business-critical pipeline lacking automated alerting therefore fails a mandatory clause, so it cannot be compliant. The trap is the word "emits run-telemetry" - satisfying one mandatory requirement can create an impression of compliance, but conjunctive requirements ("must, in addition") demand all clauses. Audit findings in real estates frequently turn on exactly this: partial compliance presented as compliance.

**Question 7 (hard).** True, False, or Cannot Say: "A pipeline built in January and not modified since must emit run-telemetry to the central observability service."

**Correct answer: False.**
**Explanation:** The standard "applies to pipelines built or substantially modified after 1 April"; older, unmodified pipelines are only "expected to achieve compliance at their next substantial modification". A January-built, unmodified pipeline is therefore not yet under the mandatory obligation - the "must" does not attach to it, so the statement as phrased ("must emit") is contradicted by the transition provision. Careful: "expected to achieve compliance" at a future trigger is not a present obligation. Transition and grandfathering clauses are where standards adherence disputes actually happen in large estates, and reading them precisely is part of ensuring adherence fairly - teams rightly lose confidence in a head of profession who enforces obligations the standard does not yet impose.

**Passage C - Escalation email from a partner department (for Questions 8-10).**
"Dear colleague, I am writing to escalate our concerns about the reliability of the citizen address validation API. Since the start of last month we have logged eleven authentication failures, three of which caused our overnight correspondence run to be postponed to the following evening. Your service desk has been responsive, and we recognise that the workaround your team supplied has prevented further postponements since it was applied two weeks ago. However, our director has asked me to seek assurance on two points before we extend the service into our benefits correspondence programme: first, a root cause and remediation date for the authentication failures; second, confirmation that the API can sustain a doubling of our current call volume. We would welcome a joint session with your engineers in the next two weeks. Please treat this as a formal escalation under section 6 of our service agreement."

**Question 8 (easy).** True, False, or Cannot Say: "The workaround has prevented further postponements of the correspondence run since it was applied."

**Correct answer: True.**
**Explanation:** The email states directly that "the workaround your team supplied has prevented further postponements since it was applied two weeks ago". The statement is a near-verbatim restatement. Easy marks like this reward scanning the passage for the keyword ("workaround") rather than re-reading the whole text - a legitimate and intended technique under one-minute-per-question timing.

**Question 9 (moderate).** True, False, or Cannot Say: "All eleven authentication failures caused the partner department's overnight correspondence run to be postponed."

**Correct answer: False.**
**Explanation:** The email says eleven failures were logged, "three of which caused our overnight correspondence run to be postponed". Three out of eleven contradicts "all eleven". The quantifier substitution - "some" becoming "all" - is among the most frequent verbal reasoning traps, and it matters operationally: a leader who reports "every failure postponed their correspondence" to their own board has just overstated an incident's impact in writing, the sort of imprecision that difficult stakeholder discussions then have to unwind.

**Question 10 (hard).** True, False, or Cannot Say: "The partner department will not extend the service into its benefits correspondence programme unless both assurances are provided."

**Correct answer: Cannot Say.**
**Explanation:** The email says the director "has asked me to seek assurance on two points *before* we extend the service". Seeking assurance before extending is not the same as committing to refuse extension if assurance is not provided - the email describes a sequencing request, not an explicit condition of refusal. It is plausible, even likely, that the extension depends on the assurances, but the text does not state it, so the strict answer is Cannot Say. This is the hardest discipline of the format: resisting a highly plausible inference because the passage stops short of asserting it. In your stakeholder work the same discipline appears in reverse - if you intend a condition, write it as a condition, because precise readers will not infer it for you.

**Passage D - Supplier proposal excerpt (for Questions 11-12).**
"Our lakehouse platform is the market-leading choice for public sector data engineering. Departments using our platform have reported reductions in pipeline development time of up to 60%. The platform's built-in metadata catalogue automatically harvests technical metadata from every connected source, eliminating manual cataloguing effort. Migration from legacy warehouse estates is typically completed within two quarters. Our proposal includes a dedicated public sector success team and assumes your engineers will complete our certification programme during the first quarter of the engagement."

**Question 11 (moderate).** Which of the following is a claim of *fact* in the passage, as opposed to a qualified or promotional claim?

- (a) The platform reduces pipeline development time by 60%.
- (b) The proposal assumes the department's engineers will complete the supplier's certification programme during the first quarter.
- (c) Migration from legacy estates always completes within two quarters.
- (d) The platform is objectively the best choice for public sector data engineering.

**Correct answer: (b).**
**Explanation:** Option (b) restates an unqualified, verifiable statement about the proposal's own content - what it assumes. Option (a) inflates "up to 60%" (a ceiling on self-reported outcomes) into a general effect. Option (c) hardens "typically completed within two quarters" into "always". Option (d) converts the promotional "market-leading choice" into an objective superlative. Horizon-scanning for the organisation, as your data innovation skill requires, is substantially this exercise: sorting a supplier document into verifiable commitments, qualified evidence and marketing language before any of it reaches a business case. Note too the buried cost in the factual claim: the certification assumption transfers a quarter of your engineers' capacity to the supplier's onboarding - the kind of detail a precise reader surfaces at negotiation.

**Question 12 (moderate).** True, False, or Cannot Say: "The platform's metadata catalogue harvests business definitions and data ownership information from connected sources."

**Correct answer: Cannot Say.**
**Explanation:** The passage says the catalogue "automatically harvests *technical* metadata". Business definitions and ownership are business metadata - a different category - and the passage is silent about them. It neither asserts nor denies the capability, so Cannot Say. (Your professional knowledge that automated harvesting of business metadata is rare must be set aside; the test asks only what the text supports.) The distinction is one you communicate constantly when explaining the value of metadata repositories: technical harvesting is the easy part, and stewardship processes must supply the business layer - but here the only question is what the supplier actually claimed, and they carefully claimed less than a hasty reader would remember.

**Passage E - Test summary report (for Questions 13-14).**
"Performance testing of the conformed reporting model completed on schedule. Of the forty-two test conditions defined from the requirements, forty were executed; two conditions relating to year-end volume peaks could not be executed because representative data was unavailable and are deferred to the next cycle. Thirty-seven executed conditions passed. The three failures all concern incremental refresh under concurrent user load; a fix is in development and will require regression testing. The test manager assesses the residual risk of the deferred conditions as medium, on the basis that year-end volumes are approximately 2.4 times the tested peak."

**Question 13 (easy).** True, False, or Cannot Say: "More than 90% of the executed test conditions passed."

**Correct answer: True.**
**Explanation:** Executed conditions: 40 (the two deferred conditions were never executed, so they leave the denominator). Passed: 37. Pass rate = 37 ÷ 40 = 92.5%, which is more than 90%, so the statement is True. The trap is the denominator: dividing by the 42 *defined* conditions gives 37 ÷ 42 ≈ 88.1%, which would flip the answer to False - but the statement says "executed", and the passage distinguishes defined from executed conditions explicitly. A verbal item that embeds a simple calculation must be computed, not judged by impression: read which population the statement names, take five seconds to do the division, and only then choose. This is the same denominator discipline that Question 11 of the numeric section drilled, now hidden inside prose - which is exactly where test summary reports hide it in real life.

**Question 14 (hard).** True, False, or Cannot Say: "The conformed reporting model has been shown to perform acceptably at year-end volumes."

**Correct answer: False.**
**Explanation:** The report states the two conditions "relating to year-end volume peaks could not be executed" and were deferred, and that year-end volumes are about 2.4 times the tested peak. So far from being shown acceptable at year-end volumes, the model has explicitly *not* been tested at them - the passage contradicts the claim of demonstrated acceptability, making this False rather than Cannot Say. Be careful with the boundary: if the statement had said "the model performs acceptably at year-end volumes", the answer would be Cannot Say (untested is not the same as failing); but "has been *shown* to perform" is a claim about the evidence, and the passage directly establishes that no such showing occurred. Parsing exactly what a report demonstrates versus what remains unknown is the essence of analysing and reporting test activities and results - and of the risk judgement you will be asked to defend when someone proposes going live before year-end testing.

**Passage F - Data governance board paper (for Questions 15-16).**
"The board is asked to note progress on the metadata repository programme and to approve the next phase. Since the last meeting, 62% of the department's priority datasets have complete catalogue entries, up from 41%. Entries are considered complete when they include a named data owner, a business description, a retention classification and lineage to at least the immediate upstream source. The programme team attributes the improvement principally to the appointment of data stewards in three directorates; the two directorates without stewards account for the majority of the remaining incomplete entries. The next phase proposes extending stewardship to the remaining directorates and integrating the repository with the pipeline deployment process, so that a production deployment cannot proceed unless the affected datasets' catalogue entries are complete. The board should note that this integration would introduce a new dependency between the repository's availability and the release process, and that mitigation options are set out in Annex B."

**Question 15 (moderate).** True, False, or Cannot Say: "A catalogue entry that includes a named data owner, a business description and a retention classification is considered complete."

**Correct answer: False.**
**Explanation:** The passage defines completeness as four elements: owner, business description, retention classification *and* lineage to at least the immediate upstream source. The statement lists only three, omitting lineage, so an entry with just those three would not meet the stated definition - the statement contradicts the passage's definition of "complete". Definitional questions reward checking every conjunct: when a text defines a term with an enumerated list, a statement that silently drops one element is False, not Cannot Say, because the definition itself supplies the missing information. As the leader who sets up robust governance processes to keep repositories up to date, you will write definitions exactly like this one - and defend them when someone argues that three out of four is close enough.

**Question 16 (hard).** Which of the following is the most accurate summary of the risk the paper asks the board to note?

- (a) The metadata repository may contain incomplete entries after the next phase.
- (b) Making deployment conditional on catalogue completeness couples the release process to the repository's availability, so a repository outage could block production deployments.
- (c) Data stewards may not be appointed in the remaining directorates.
- (d) The repository integration will slow down all production deployments.

**Correct answer: (b).**
**Explanation:** The paper says the integration "would introduce a new dependency between the repository's availability and the release process", with mitigations in an annex - that is precisely option (b): if deployments cannot proceed without complete catalogue entries, and the repository is unavailable, releases stall. Option (a) describes the current state, not the flagged risk. Option (c) invents a risk the paper never raises. Option (d) overstates: a dependency is a conditional exposure, not a claim that all deployments will be slower. Summarising the *actual* stated risk - neither diluting it nor inflating it - is the comprehension skill your role exercises when you brief boards: the value of a metadata repository is easiest to sell when you are also candid and precise about the operational coupling it introduces, and this passage models how a well-written paper does both in three sentences.

### Preparation tips

- **Train the three-way distinction daily.** For one week, when reading any policy or report, classify a few claims as entailed, contradicted, or unsupported. The True/False/Cannot Say discipline is a habit, and senior professionals - accustomed to reading for gist and action - often need to deliberately re-sharpen reading-for-entailment.
- **Learn the trigger words.** "Normally", "typically", "up to", "including", "should" versus "must", "expected to" - each one changes the logical force of a sentence. You write these words into standards yourself; the assessment simply tests whether you notice them at reading speed.
- **Scan, then verify.** Read the question first, scan the passage for its keywords, then read that sentence and its neighbours closely. Whole-passage reading before seeing the questions is the classic time-management failure in this format.
- **Suppress expertise deliberately.** Your knowledge of real data-sharing agreements, standards and supplier behaviour is the main source of Cannot Say errors for experienced candidates. Say to yourself: "only the text".
- **Practise with your own inbox.** Take a real escalation email and write three statements about it: one entailed, one contradicted, one plausible-but-unstated. Designing items teaches the format faster than answering them.

### Common pitfalls

- **Bringing in outside knowledge** - answering from how government data sharing actually works rather than from the passage. The more senior you are, the stronger this pull.
- **Confusing "likely" with "stated"** - as in Question 10: a highly plausible business inference is still Cannot Say if the text stops short of asserting it.
- **Quantifier and qualifier slips** - "three of eleven" read as "all", "normally" read as "always", "up to 60%" read as "60%". These distinctions decide most items.
- **Reading "including" as exhaustive** - example lists signal breadth, not limits, as in Question 3.
- **Poor time management** - spending the first ninety seconds reading a passage end to end instead of locating what the question actually asks. With less than a minute per item, targeted scanning is not a shortcut; it is the intended method.
- **Missing the difference between "untested" and "failed"** - as Question 14 showed, a claim about what the evidence *demonstrates* can be False even when the underlying capability is merely unknown. Match the statement's verb ("has been shown", "performs", "will") to what the passage can actually support before choosing between False and Cannot Say.

## Workplace job-specific situational judgement assessment

### About this assessment

A workplace job-specific situational judgement assessment evaluates your decision-making, interpersonal skill and professional conduct by presenting realistic workplace dilemmas and asking how you would respond. Unlike the reasoning tests, there is no single objective calculation: several responses may look reasonable, but one best fits the values of the organisation and the demands of the role. For senior UK public sector digital roles, the anchoring values are well established: putting user needs first, transparency and candour, collaboration across boundaries, accessibility and inclusion, evidence-based decisions, and the responsible stewardship of public money and public data.

Typical format and timing: you are given a short scenario and four or five possible actions, and asked either to select the **most effective** and **least effective** actions, or to rank or rate every option. Timing is usually generous or untimed - the test measures natural judgement, not speed. Scoring compares your choices with those of an expert panel of experienced leaders.

Why it matters for your role: at head-of level, judgement *is* the job. Your role profile is dense with situations that have no formula: mediating between people and strengthening relationships, managing stakeholder expectations, moderating difficult discussions about high-risk and complex topics within constrained timescales, providing technical leadership and career development to a community, and deciding when an emerging trend deserves investment. Assessors use situational judgement tests at this level because technical excellence is assumed; what distinguishes candidates is how they balance delivery pressure against engineering integrity, candour against diplomacy, and short-term fixes against long-term capability.

### What it measures for your role

- **Communicating between the technical and non-technical**: scenarios test whether you mediate rather than inflame, match the communication method to the audience, and moderate difficult discussions about high-risk topics under time pressure.
- **Problem management**: scenarios test whether you anticipate problems, address root causes rather than symptoms, see how a problem fits the larger picture, and build problem-solving capability in others instead of solving everything yourself.
- **Data development process** and **data integration design**: scenarios test how you uphold enterprise-scale procedures and standards when adherence is inconvenient - the moment standards actually matter.
- **Programming and build**: scenarios test how you exercise technical responsibility and advise on standards without micromanaging experienced teams.
- **Data innovation**: scenarios test how you respond to emerging technology pressure - neither reflexive adoption nor reflexive dismissal.
- **Metadata management** and **testing**: scenarios test whether you protect unglamorous but essential disciplines when delivery pressure squeezes them.
- **Building capability**: several scenarios test the leadership behaviours named in your role - inspiring best practice and providing career development for the community.

### Practice questions

For each scenario, identify the **most effective** and **least effective** responses before reading the discussion.

**Question 1 (moderate) - The deadline versus the standard.**
A delivery team building a new data service for a ministerial commitment tells you they can hit the launch date only by skipping the agreed integration standard's quarantine-and-reason-code requirement for rejected records, promising to retrofit it "in the next sprint". The service will process citizen benefit data from day one. The programme director supports the team: "Ship it; it's a technicality."

- (a) Approve the exception verbally to keep the launch on track, and rely on the team's promise to retrofit.
- (b) Refuse the launch outright and inform the programme director that the standard is non-negotiable in all circumstances.
- (c) Convene the team and programme director briefly; assess the concrete risk of silent record loss in citizen benefit data; if the launch proceeds, grant a time-boxed, documented waiver with a named owner, a retrofit date, and interim manual monitoring of rejects; escalate to your director if the risk is unacceptable.
- (d) Tell the team to launch but privately instruct one engineer to build the quarantine feature over the weekend without telling the programme director.
- (e) Email the programme director restating the standard and copy the departmental risk register team.

**Most effective: (c). Least effective: (d).**
**Explanation:** Option (c) does what your role profile actually describes: it moderates a difficult discussion about a high-risk topic within a constrained timescale, converts an informal "technicality" argument into a concrete risk assessment (silent loss of citizen benefit records is a serious harm, not a technicality), and uses the standard's own governed flexibility - a documented, time-boxed waiver with ownership and monitoring - rather than either rigidity or capitulation. It also keeps escalation available, showing you know when a decision exceeds your risk appetite. Option (d) is worst: it launches non-compliantly *and* adds a concealed, unresourced weekend workaround, deceiving the programme director, burning out an engineer, and creating an unreviewed change path - it fails transparency, collaboration and engineering integrity simultaneously. Option (a) is weak: verbal exceptions with unenforced promises are how standards die and how "temporary" gaps become permanent. Option (b) is stronger than (a) but brittle - "non-negotiable in all circumstances" refuses the risk conversation your level exists to have, and standards with governed waiver routes are more resilient than absolutist ones. Option (e) is passive-defensive: it protects your paper trail without engaging the decision, the classic "pass the problem sideways" pattern that situational judgement scoring penalises.

**Question 2 (moderate) - The struggling team lead.**
One of your four team leads, promoted eight months ago, is visibly struggling: their team's delivery has slowed, two engineers have privately told you they are considering leaving because sprint planning is chaotic, and the lead has started declining your one-to-ones, citing workload. The team is mid-way through a critical integration for another department.

- (a) Move the strongest engineer from another team in to "shadow" the lead without explaining why to either of them.
- (b) Reinstate the one-to-ones as non-optional, share the specific observations candidly and supportively, ask for the lead's own diagnosis, and agree a support plan - such as a delivery manager pairing, coaching, or temporarily narrowing their scope - with a review point in four to six weeks.
- (c) Demote the lead back to engineer immediately to protect the critical integration.
- (d) Wait until the integration ships, then address the performance issues in the next formal review cycle.
- (e) Ask the two unhappy engineers to give the lead direct feedback themselves, since the issue is between them.

**Most effective: (b). Least effective: (d).**
**Explanation:** Option (b) reflects the capability-building core of your role: providing technical leadership and career development for the community means treating a struggling recent promotee as a development situation with structure - candid observations, the lead's own diagnosis first (they may know exactly what is wrong), concrete support, and a bounded review point. It also quietly re-establishes the management relationship the lead has been avoiding. Option (d) is least effective, though it looks prudent: months of further chaos risk losing two engineers (a real capability loss), harming the cross-department integration, and letting the lead fail longer - deferring known people-problems to review cycles is the passive option the format penalises, and the delivery it claims to protect is exactly what the dysfunction is degrading. Option (c) is disproportionate and destroys psychological safety for every future promotee: no support was offered before the sanction. Option (a) is manipulative - unexplained shadowing will be discovered, read as surveillance, and poison trust. Option (e) abdicates: peer feedback has value, but the engineers escalated to you because the issue exceeds what peer feedback fixes; redirecting them back down converts your leadership responsibility into their interpersonal risk.

**Question 3 (hard) - The vendor announcement and the excited minister's office.**
A major cloud vendor announces an "autonomous data engineering" AI service, claiming it eliminates most pipeline development. The minister's office, having read press coverage, asks your director whether the department can cut its data engineering headcount next year. Your director asks you for a same-week briefing. Your community is anxious; two engineers have already asked you whether their jobs are safe.

- (a) Write a briefing dismissing the technology as hype and recommending no change, to reassure your community.
- (b) Write a balanced briefing: summarise what the service verifiably does today versus vendor claims, propose a small time-boxed evaluation against one real use case, set out realistic capability implications (skills shifting toward oversight, integration design and assurance rather than disappearing), and address your community openly about what you have advised and why.
- (c) Delay the briefing until you can run a full three-month evaluation, since advising without evidence would be irresponsible.
- (d) Write the briefing recommending early adoption and voluntary redundancy planning, aligning with the direction the minister's office seems to want.
- (e) Send your director links to independent analyst coverage and offer to discuss it when the anxiety has died down.

**Most effective: (b). Least effective: (d).**
**Explanation:** This scenario tests three of your named skills at once. Data innovation: horizon-scanning means neither dismissal (a) nor credulity (d) - it means separating verifiable current capability from claims (as the verbal section's supplier passage drilled) and generating evidence cheaply via a time-boxed pilot. Communicating between the technical and non-technical: option (b) gives the director something a minister's office can absorb - what is true now, what we will test, what it means for people - within the constrained timescale, where (c) misses the political moment entirely and cedes the narrative to press coverage for a quarter. Representing the community: (b) speaks on behalf of your engineers honestly, addressing job-security anxiety with candour about how roles will evolve rather than hollow reassurance. Option (d) is least effective because it converts marketing into workforce policy: recommending redundancy planning on unverified vendor claims fails evidence-based decision-making, stewardship of public money and your duty to the community - and if the technology underdelivers, the department will have traded real capability for a press release. Option (a) fails in the mirror-image way: protective dismissal sacrifices your credibility as an honest broker, which is the asset that lets you defend your community effectively. Option (e) is abdication dressed as delegation - your director asked for your professional judgement, not a reading list.

**Question 4 (moderate) - The cross-department data quality dispute.**
Your team provides a conformed dataset to another government department. Their head of analysis emails your director claiming your "poor data quality" caused errors in their published statistics, and demands a formal apology and compensation from your budget. Your team's investigation shows the receiving department misapplied a field that your published data dictionary defines clearly - but also that your dictionary's distribution list was out of date, so they never received the last two updates.

- (a) Reply with the evidence that their analysts misused the field, and decline further discussion until the accusation is withdrawn.
- (b) Accept fault fully and offer compensation to preserve the relationship.
- (c) Contact their head of analysis directly to propose a joint technical review; present the field-definition evidence factually and without blame; acknowledge your side's distribution-list failure and fix it; propose a shared change-notification process so both organisations get earlier warning of definition changes.
- (d) Escalate to your director with a rebuttal pack and let the directors resolve it between themselves.
- (e) Quietly fix the distribution list and wait to see whether the complaint is pursued.

**Most effective: (c). Least effective: (e).**
**Explanation:** Option (c) is the textbook exercise of mediating between people and strengthening relationships while managing a difficult, reputationally loaded discussion: it separates fact from blame, is transparent about your own contributory failure (the stale distribution list) rather than hiding behind the stronger evidence, and converts the dispute into a durable process improvement - a shared notification mechanism that protects both departments' published statistics in future. That combination of candour and system-fixing is what UK public sector values look like in practice. Option (e) is least effective: it conceals a known contributory failure while a formal accusation stands, which is a transparency failure that will look far worse when discovered - and the complaint will not simply evaporate. Option (a) wins the battle and loses the relationship; being right about the field definition does not excuse the distribution failure, and conditioning dialogue on withdrawal escalates conflict. Option (b) overcorrects: accepting full fault misstates the facts, sets a compensation precedent public budgets cannot sustain, and does nothing to fix the actual root causes. Option (d) has situational uses but here it outsources a technical dispute you are best placed to resolve, delaying resolution and signalling to both communities that heads of profession cannot settle professional disagreements.

**Question 5 (moderate) - The metadata governance decay.**
Six months after a successful launch, your metadata repository is decaying: stewards in two directorates have stopped updating entries, and a spot check shows 30% of "complete" entries are now stale. Delivery teams say cataloguing "adds no value to sprints". Meanwhile, a data protection review has asked for evidence of your data inventory within eight weeks.

- (a) Issue a directive that all teams must update their catalogue entries within two weeks, with non-compliance reported to directors.
- (b) Pay a contractor team to bulk-update the entries before the review deadline.
- (c) Use the review deadline as the catalyst: brief directorate leaders on the concrete consequence (a failed data protection review), re-establish stewardship with named owners and time in plans, automate harvesting of the technical fields so stewards maintain only business context, and integrate entry updates into the deployment workflow so currency becomes a by-product of delivery rather than an extra chore.
- (d) Report to the review that the repository is materially complete, since most entries were accurate at launch.
- (e) Accept that metadata repositories always decay and scope the review response around other evidence sources.

**Most effective: (c). Least effective: (d).**
**Explanation:** Your role includes communicating the value of metadata repositories and setting up robust governance processes to keep them up to date - and this scenario is precisely the moment that skill exists for. Option (c) works at every level: it converts an abstract governance duty into a concrete stake leaders understand (the review), fixes the incentive problem the teams named (automating what can be harvested, embedding the rest in existing workflow so the "no value to sprints" objection dissolves), and rebuilds the human stewardship layer with ownership and time - the design insight being that governance which relies on voluntary extra work always decays, while governance embedded in the pipeline persists. Option (d) is least effective and the only ethically disqualifying one: describing 30%-stale data as "materially complete" to a data protection review is a misrepresentation with legal and reputational consequences far exceeding the original problem. Option (a) may produce a one-time compliance spike but attacks none of the causes and spends leadership capital on coercion; entries will be stale again in six months. Option (b) buys a snapshot with public money while teaching the organisation that neglect gets bailed out. Option (e) treats a solvable design problem as fate and leaves the department without a working inventory - the passive option again.

**Question 6 (hard) - The incident during the board meeting.**
You are presenting your data strategy to the departmental board when your phone buzzes: your deputy reports that the overnight conformed load feeding several departments' morning statistics has partially failed, and teams are split on whether to re-run (statistics available two hours late) or publish from the partial load (on time, but roughly 8% of records missing, concentrated in one region). Publication is due in 90 minutes. Your deputy asks for a decision.

- (a) Step out briefly; direct the re-run (late but complete), on the basis that regionally skewed statistics are worse than late statistics; ask your deputy to notify affected departments' contacts immediately with the revised time; return to the board and briefly inform them.
- (b) Reply by message: "Publish from the partial load; we'll correct later" - on time delivery protects the department's reputation.
- (c) Tell your deputy to make the call themselves; you are with the board.
- (d) Leave the board meeting entirely to personally supervise the re-run.
- (e) Step out and convene a 30-minute call with all affected departments to reach consensus before deciding.

**Most effective: (a). Least effective: (b).**
**Explanation:** The substantive judgement: publishing statistics with an 8% gap *concentrated in one region* is not a minor completeness issue - it is a skewed picture that downstream departments would treat as true, and regionally biased official figures carry equity and trust harms that a two-hour delay does not. Complete-but-late beats wrong-but-punctual for public data; that is what putting users of the statistics first means. So (b) is least effective - and note that "we'll correct later" makes it worse, knowingly publishing skewed figures with a correction planned. On the leadership mechanics: (a) shows proportionate presence - a brief, decisive intervention with clear delegation of the communication task, then candour with the board (who are, after all, being told the strategy is "robust data services"; telling them about the incident and your handling of it is a live demonstration). Option (c) looks like empowerment but is abdication at the wrong moment: your deputy explicitly asked for a decision on a cross-department judgement call that exceeds their risk authority - building problem-solving capability in others happens in the review afterwards, not by refusing a requested decision under deadline. Option (d) over-corrects: supervising a re-run personally adds nothing your teams cannot do and visibly signals to the board that your services cannot run without you. Option (e) mistakes consultation for decision-making: 30 of the 90 minutes spent seeking consensus that may not come, when what partners actually need is a prompt decision and early notification - which (a) provides.

**Question 7 (moderate) - The standards rebel with a point.**
Your most technically respected principal engineer publicly refuses to follow the new team-based programming standard you sponsored, arguing in the community channel that its mandated orchestration pattern is "outdated for streaming workloads" - and their technical argument, on inspection, has merit for a subset of cases. Other engineers are watching how you respond; two teams have quietly paused adopting the standard.

- (a) Enforce the standard uniformly: credibility requires that no one is exempt, whatever the technical merits.
- (b) Acknowledge publicly that the concern has technical merit; invite the principal engineer to lead a working group to define a streaming-workload profile or exception within the standard, with a deadline; restate that the current standard applies until formally amended; and privately discuss why public defiance was the wrong route and what the right one is.
- (c) Grant the principal engineer's teams an informal exemption to keep the peace.
- (d) Remove the engineer from the community channel for undermining agreed standards.
- (e) Withdraw the standard until full consensus is achieved.

**Most effective: (b). Least effective: (d).**
**Explanation:** Your role profile contains both halves of this dilemma: establish standards and ensure adherence, *and* keep abreast of best practice - which means standards must be able to metabolise legitimate technical challenge. Option (b) does both: it honours the valid engineering point (streaming workloads genuinely strain batch-era orchestration patterns), channels the challenger's expertise and status into improving the standard through the governed route, keeps the standard authoritative in the meantime (so the two hesitating teams have a clear answer), and deals with the behavioural issue - public defiance by a senior figure - privately and developmentally, separating the message ("your argument is good") from the method ("the channel broadside was not"). Option (d) is least effective: punishing your most respected engineer for a technically meritorious challenge would chill honest dissent across the community, likely trigger a resignation, and signal that standards are about authority rather than engineering - the opposite of inspiring best practice. Option (a) is rigid: enforcing a partially wrong standard "whatever the merits" converts a fixable design gap into a legitimacy crisis. Option (c) is corrosive in the quiet way: informal exemptions for the influential teach everyone that standards bind only the compliant. Option (e) abandons the estate to fragmentation and teaches that public resistance repeals standards - consensus is desirable, but standards governance exists precisely because full consensus is rare.

**Question 8 (hard) - The capability budget under pressure.**
Mid-year savings are demanded across the department. Your director proposes cancelling the data engineering community's training and conference budget and pausing the apprenticeship intake, noting these are "the least operationally disruptive" cuts. You know your retention already trails the market, two teams depend on skills (streaming, IaC) that the training programme was building, and the apprenticeship scheme is your main pipeline for diversifying the profession's intake.

- (a) Accept the proposal; delivery must come first in a savings year, and development can resume next year.
- (b) Refuse to offer any savings from your area, arguing data engineering is too critical to cut.
- (c) Counter-propose within 48 hours: offer alternative savings you can better absorb (e.g. deferring a tooling renewal, reducing contractor reliance by converting one role), quantify the true cost of the proposed cuts - attrition replacement costs against training costs, the delayed capability the two teams need, and the diversity pipeline impact - and propose protecting the apprenticeships and a reduced, prioritised training programme.
- (d) Accept the cuts publicly but privately tell your leads to disguise training as project costs.
- (e) Email your community that the director is cutting their development, encouraging them to raise concerns through staff networks.

**Most effective: (c). Least effective: (d).**
**Explanation:** Building data engineering capability - technical leadership, career development, and a diverse pipeline into the profession - is not a perk you administer; it is a named duty of your role, so defending it with evidence is doing your job, not special pleading. Option (c) is effective because it engages the savings requirement seriously (offering real alternatives, which earns the right to be heard), converts capability from a soft plea into hard numbers (replacing a departing engineer typically costs far more than training one; contractor conversion often saves more than a conference budget), and prioritises rather than protecting everything - protecting apprenticeships hardest because a paused intake breaks a multi-year, diversity-critical pipeline that cannot simply resume. Option (d) is least effective and integrity-breaking: mislabelling training as project costs is financial misreporting of public money - it exposes your leads to serious consequences for a decision you made, and it is disqualifying conduct in any values-based scoring. Option (b) refuses collective responsibility and will likely see the original cut imposed anyway, now without goodwill. Option (a) is the quiet failure: "least operationally disruptive" is true only on a one-year horizon, and accepting it silently means the attrition and skills gaps arrive on your watch with your consent on record. Option (e) weaponises your community against your director - it breaches the trust that lets you represent engineers effectively and converts a negotiable budget question into an industrial-relations problem.

**Question 9 (moderate) - The conformed model shortcut.**
A programme board wants a "quick win": joining your conformed citizen dataset with a legacy departmental dataset to produce a new cross-cutting analysis for a spending review submission, in three weeks. Your data modelling lead reports that the legacy dataset's person-matching keys are unreliable - trial matching produced a 12% false-match rate - and recommends eight weeks to build proper resolution logic. The board chair says: "It's for internal analysis, not publication; 88% right is good enough."

- (a) Deliver the three-week join as asked, since the chair has accepted the accuracy trade-off.
- (b) Deliver the three-week join, but attach a caveat page describing the false-match rate.
- (c) Explain the specific consequence in the board's terms - at 12% false matches, the spending review figures could be materially wrong in either direction, and "internal" analyses have a way of anchoring real allocation decisions; offer a middle path such as three-week delivery restricted to the record subset with reliable keys (quantifying its coverage), with the full resolution logic to follow; let the board choose between honestly framed options.
- (d) Refuse until the eight-week work is complete, since your modelling lead's professional judgement must be final.
- (e) Ask the modelling lead to lower the matching threshold so the false-match rate looks smaller in reporting.

**Most effective: (c). Least effective: (e).**
**Explanation:** This is the data modelling and analysis-synthesis judgement call your profile describes - explaining the concepts and principles of matching to non-specialists, and bringing sources together honestly. Option (c) succeeds because it translates a technical metric into decision consequences (a 12% false-match rate is not "88% right" in effect - false matches distort aggregates unpredictably, and spending review numbers drive real allocations), respects the board's authority to accept risk while ensuring the risk is genuinely understood, and offers an engineered middle path that gives a fast, defensible partial answer - which is usually what "quick win" boards actually need. Option (e) is least effective and the only dishonest one: tuning a threshold to make a quality metric *look* better without making matching better is manipulating evidence that feeds a spending review - a straightforward integrity violation. Option (b) is the subtle trap: caveat pages detach from headline numbers within one forwarding, and attaching a disclaimer to figures you believe are unfit for purpose is transferring risk on paper, not managing it. Option (a) abdicates professional responsibility for making the trade-off legible before it was accepted. Option (d) overcorrects: engineering advice deserves great weight, but "must be final" makes specialists into vetoes over governance, and refuses the creative option (c) that satisfies both the deadline and the integrity constraint.

**Question 10 (moderate) - Representing the profession under fire.**
At a cross-government conference, during your talk on your department's data engineering practice, a senior figure from another department interrupts from the floor: "Frankly, departmental data engineering teams like yours are why nothing interoperates - you all build bespoke empires." There is laughter, and the room waits for your response. You have 200 people watching, including several of your own engineers.

- (a) Respond in kind with a barbed joke about the questioner's department's well-known integration failures.
- (b) Acknowledge the legitimate frustration behind the point, briefly evidence where cross-government standards are working and where your own department has fallen short and is fixing it, and offer to continue the exchange in the panel or afterwards - modelling for the room and your engineers how the profession debates.
- (c) Decline to engage: "I'll take questions at the end", and continue the prepared talk.
- (d) Concede the criticism entirely to defuse the moment.
- (e) Invite the questioner to co-present a session next year on interoperability, without addressing the substance now.

**Most effective: (b). Least effective: (a).**
**Explanation:** Speaking on behalf of, and representing the community to, large audiences inside and outside the organisation is verbatim in your role profile - and this scenario tests it under mild hostility. Option (b) works because it does four things at once: it treats the interruption as a real argument rather than an attack (there *is* a genuine cross-government interoperability critique, and acknowledging it shows confidence, not weakness); it responds with brief evidence and balanced candour, including where your department has fallen short - which UK public sector transparency values reward far more than defensiveness; it manages the room's format so the talk survives; and it consciously models professional conduct for the engineers watching, which is capability-building in public. Option (a) is least effective: a barbed retort might win the laugh but converts a professional exchange into an inter-departmental feud in front of 200 witnesses, damages the collaboration your data-sharing work depends on, and shows your engineers exactly the behaviour you would discipline. Option (c) is a lesser failure - it avoids harm but reads as unable to engage, and the unanswered charge hangs over the rest of the talk. Option (d) overcorrects: wholesale concession is untrue (some things do interoperate), demoralises your watching community, and teaches the room that heckling extracts confessions. Option (e) is charming but empty on its own - deferral without substance; combined with a brief substantive reply it would strengthen (b), which is the pattern top-scoring candidates often add.

### Preparation tips

- **Anchor on public sector values, not corporate instinct.** Where a commercial test might reward competitive aggression, senior civil service scoring rewards user needs, transparency, candour about failure, collaboration across boundaries, inclusion, and stewardship of public money. Re-read the Civil Service values and your organisation's leadership statement the week before the assessment.
- **Look for the option that fixes the system, not just the incident.** At head-of level, the strongest answers usually combine an immediate decision with a durable improvement - a waiver process, a shared notification mechanism, workflow-embedded governance. Symptom-only options score as mid-range.
- **Watch for the integrity tripwires.** Most senior SJTs include one option per scenario that involves concealment, misreporting or manipulation (Questions 5(d), 8(d), 9(e)). These are almost always the least effective. Identify them first; it simplifies the remaining ranking.
- **Balance decisiveness with proportionality.** Both abdication ("let someone else decide") and over-control ("I will personally supervise") are penalised. The scored behaviour is usually a brief, clear decision with genuine delegation of execution.
- **Rehearse with real dilemmas.** Take three difficult situations from your own leadership history, write four plausible responses to each including the one you took, and rank them against the values above. Honest reflection on where your instinct diverges from the scoring frame is the highest-value preparation available - and useful far beyond the test.

### Common pitfalls

- **Answering idealistically rather than effectively.** "Convene all stakeholders for consensus" sounds collaborative but is often the passive or slow option, as in Question 6(e). Effectiveness under real constraints is what is scored.
- **Selecting passive options.** Waiting for review cycles, quietly fixing and hoping, sending links instead of judgement - options that delay action, pass the problem along, or ignore the root cause consistently score poorly, and appeared throughout this section.
- **Ignoring the values context.** These scenarios are scored against UK public sector culture: candour about your own side's failures (Question 4), honest data over punctual data (Question 6), evidence over vendor narrative (Question 3). Answering from a purely commercial playbook misfires.
- **Protecting your position instead of the outcome.** Paper-trail options - restating the standard in an email, attaching caveats to figures you distrust - protect you while leaving users exposed; assessors read them as risk transfer, not risk management.
- **Over-indexing on being right.** Several scenarios (4, 7, 10) contain a party who is partly wrong and partly right. Options that press your correctness while ignoring your own contribution, or the relationship, score below options that hold both.

## Conclusion

You have now worked through four substantial assessment areas - cognitive ability, numeric reasoning, verbal reasoning and situational judgement - each built from the genuine substance of your role: pipeline dependencies and data models, platform budgets and capacity arithmetic, data-sharing agreements and governance papers, and the leadership dilemmas of running an enterprise data engineering profession. If you attempted the questions before reading the explanations, you have done real practice, not just reading; that difference is what shows up on assessment day.

A few closing encouragements. First, trust your experience. Every question type in this document samples something you already do: you triage problems, read standards precisely, interrogate supplier claims, weigh delivery against integrity, and represent your community under pressure. The assessments are unfamiliar packaging around familiar judgement, and packaging yields quickly to practice. Second, treat your error patterns as information. If Cannot Say items caught you, sharpen reading-for-entailment; if denominators tripped you, slow down on rates; if your situational instincts diverged from the scoring frame, reflect on whether that reveals a coaching point or simply a context difference worth being conscious of. Senior professionals improve fastest at exactly this kind of targeted correction. Third, keep perspective: psychometric results are one input among many - your track record, interviews and technical assessments all speak too - so approach the test as an opportunity to demonstrate strengths rather than a hazard to survive.

Finally, let this material serve your wider development. The skills these assessments measure - precise reading, honest numbers, structured problem description, values-anchored judgement - are the same ones that make you effective in the role itself, and the same ones you are building in others as you develop your community of engineers. Consider sharing practice material like this with the leads you are growing toward head-of-profession roles; working through scenarios together is capability-building of exactly the kind your role profile describes. Prepare steadily, arrive rested, read every question as carefully as you would read a data-sharing clause, and go and show them what an experienced head of data engineering brings. You are better prepared than you think.
