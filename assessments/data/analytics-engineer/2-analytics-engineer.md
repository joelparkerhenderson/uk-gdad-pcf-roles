# Analytics Engineer - Psychometric Assessment Resources

## Introduction

Welcome! This guide has been written especially for you as an analytics engineer working in the UK Government Digital and Data profession. Whether you are preparing for an internal development scheme, a promotion board, a new posting in another department, or you simply want to sharpen the mental skills you use every day, this document will help you practise and build confidence.

Psychometric assessments are structured, standardised exercises that measure the thinking skills a role genuinely requires. They are not tests of trivia or memory, and they are not designed to catch you out. Instead, they sample the kinds of reasoning you already use when you profile a source system, design a dimensional model, check a data quality report, or explain a data structure to a colleague who has never heard of a fact table. Because the questions are drawn from realistic workplace material, your day-to-day experience as an analytics engineer is a real advantage — and deliberate practice makes that advantage stronger.

This document is organised around the four assessment types you are most likely to meet:

1. **Workplace job-specific cognitive assessment** — pattern recognition, logical deduction, error checking, prioritisation, and problem solving using the artefacts you handle every day, such as data models, pipeline schedules, and metadata records.
2. **Workplace job-specific numeric reasoning assessment** — interpreting tables, percentages, ratios, and performance metrics of the kind you see in data quality dashboards, pipeline run logs, and capacity plans.
3. **Workplace job-specific verbal reasoning assessment** — reading dense written material such as data standards, documentation guidance, and stakeholder emails, then drawing strictly accurate conclusions from the text.
4. **Workplace job-specific situational judgement assessment** — choosing effective actions in realistic workplace dilemmas involving data users, subject matter experts, trainee colleagues, and senior analytics engineers.

Each section explains what the assessment measures, maps it to the specific skills in your role profile — from data modelling, cleansing and enrichment through to communicating between the technical and non-technical — and then gives you a generous set of practice questions with full worked answers. Every scenario is set in a UK government digital and data context, so the practice you do here transfers directly to both assessments and real work.

How should you use this guide? Work through it at your own pace. Try each question honestly before reading the answer, note the questions you find harder, and revisit them after a few days. Use the preparation tips and common pitfalls at the end of each section as a checklist before any real assessment. Most of all, treat this as friendly professional development rather than an exam: every question you attempt strengthens skills you use in your actual role.

Good luck — you may be surprised how much you already know.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive assessment measures the core mental processes your role depends on: recognising patterns, deducing conclusions from rules, spotting errors in detailed material, prioritising competing demands, and solving practical problems. Unlike a generic IQ test, every question is built from realistic workplace scenarios and data, so it predicts how you will perform on the job rather than how you perform on abstract puzzles.

For an analytics engineer, that means the questions look like your working week. You might be asked to spot the inconsistency in a set of metadata records, deduce which data model change caused a downstream report to break, work out the correct order to rebuild a set of dependent tables, or decide which of five support requests to handle first. The format is typically online and timed — usually 15 to 30 minutes — with objective scoring against a benchmark group. Many platforms give you a few ungraded practice questions first so you can get used to the interface, and some adapt the difficulty based on your previous answers. Employers usually receive a breakdown of speed versus accuracy rather than a single score, so working carefully matters just as much as working quickly.

The good news is that cognitive skills respond well to practice. Because you already exercise these skills whenever you profile a source system, trace a data lineage question through a metadata repository, or debug a transformation script, the practice questions below should feel familiar — they simply make the reasoning explicit and put it under gentle time pressure.

### What it measures for your role

Each cognitive dimension maps directly onto the skills in your role profile:

- **Pattern recognition** supports your **data modelling, cleansing and enrichment** skill: producing data models, comparing different types of models, and reverse-engineering a data model from a live system all depend on seeing structure — keys, hierarchies, grains, and relationships — in raw material.
- **Logical deduction** supports your **data analysis and synthesis** skill: data profiling and source system analysis are exercises in drawing sound conclusions from evidence, and presenting clear insights requires the chain of reasoning to be watertight.
- **Error checking** supports your **metadata management** and **testing** skills: maintaining a metadata repository so information remains accurate, drafting documentation that meets standards, and correctly executing test scripts all reward a sharp eye for small discrepancies.
- **Prioritisation** supports your **problem management** skill: investigating problems in systems, processes and services means understanding whether a problem is strategic, tactical or operational, and choosing what to tackle first.
- **Problem solving** supports your **programming and build (data engineering)** skill: designing, coding, testing and correcting scripts is applied problem solving, step by step.

### Practice questions

**Question 1 (easy) — Pattern recognition in table naming**

Your team's data warehouse uses a naming standard for transformed tables. You observe the following existing tables:

- `dim_citizen`, `dim_service_location`, `dim_case_type`
- `fct_application_submitted`, `fct_payment_processed`

A senior analytics engineer asks you to add a table holding one row per appointment booking event. Which name fits the established pattern?

A) `appointment_bookings`
B) `fct_appointment_booked`
C) `dim_appointment_booking`
D) `fact_appointments`

**Correct answer: B**

**Explanation:** The pattern shows dimension tables prefixed `dim_` with a singular noun describing an entity, and fact tables prefixed `fct_` with a singular noun plus a past-tense event verb (`application_submitted`, `payment_processed`). An appointment booking event is a fact (one row per event), so it takes the `fct_` prefix, and the event form is `appointment_booked`. Option D uses the wrong prefix spelling and a plural; option C wrongly treats an event as a dimension; option A ignores the standard entirely. Recognising and extending conventions like this is exactly what "understand industry-recognised data modelling patterns and standards" means in practice.

**Question 2 (easy) — Logical deduction from refresh rules**

Your department's data platform applies these rules:

1. If the source extract fails, the staging tables are not updated.
2. If the staging tables are not updated, the data models are rebuilt from yesterday's staging data.
3. If the data models are rebuilt from yesterday's staging data, dashboards display a "data may be out of date" banner.

This morning the dashboards display the "data may be out of date" banner. Which conclusion is definitely true?

A) The source extract failed last night.
B) The staging tables were not updated last night.
C) The data models were rebuilt from yesterday's staging data.
D) The dashboards are showing incorrect figures.

**Correct answer: C**

**Explanation:** The banner appears when models are rebuilt from yesterday's staging data, so C follows directly. But be careful about reasoning backwards up the chain: the rules say a failed extract *leads to* stale staging, and stale staging *leads to* a rebuild from old data — they do not say these are the *only* causes. The banner could, for instance, be triggered by some other condition not described, or the rebuild from old data could have another cause; from the information given, only C is guaranteed. D confuses "out of date" with "incorrect" — yesterday's figures may be perfectly accurate for yesterday. Assessments frequently test whether you affirm the consequent; resist it, just as you would when investigating a pipeline problem.

**Question 3 (moderate) — Error checking a metadata record**

You maintain the metadata repository. A colleague submits this entry for review:

> **Dataset:** Housing repairs — completed jobs
> **Owner:** Housing Operations Data Team
> **Update frequency:** Daily at 06:00
> **Grain:** One row per repair job per day
> **Primary key:** repair_job_id
> **Row count (last load):** 41,207
> **Sensitive fields:** tenant_name (removed at staging), property_postcode (retained)

Which pair of statements in the record is logically inconsistent?

A) Owner and update frequency
B) Grain and primary key
C) Row count and update frequency
D) Sensitive fields and owner

**Correct answer: B**

**Explanation:** If the grain is "one row per repair job **per day**", then `repair_job_id` alone cannot be the primary key — the same job would appear on multiple days, so the key must combine the job identifier with the date (for example `repair_job_id + snapshot_date`). Alternatively, if `repair_job_id` truly is unique, the grain statement is wrong and should read "one row per repair job". Either way, the two statements cannot both be true. This is precisely the kind of inconsistency you are expected to catch when you "maintain a metadata repository to ensure information remains accurate and up to date" — a wrong grain statement misleads every analyst who relies on the record.

**Question 4 (moderate) — Dependency ordering**

You must rebuild five objects after a schema change. The dependencies are:

- `stg_payments` depends on nothing.
- `stg_claims` depends on nothing.
- `int_claim_payments` depends on `stg_payments` and `stg_claims`.
- `dim_claimant` depends on `stg_claims`.
- `fct_claim_payment` depends on `int_claim_payments` and `dim_claimant`.

Which is a valid rebuild order?

A) `stg_claims`, `dim_claimant`, `stg_payments`, `int_claim_payments`, `fct_claim_payment`
B) `stg_payments`, `int_claim_payments`, `stg_claims`, `dim_claimant`, `fct_claim_payment`
C) `dim_claimant`, `stg_claims`, `stg_payments`, `int_claim_payments`, `fct_claim_payment`
D) `stg_payments`, `stg_claims`, `fct_claim_payment`, `int_claim_payments`, `dim_claimant`

**Correct answer: A**

**Explanation:** Work through each option checking that every object appears after all its dependencies. In A: `stg_claims` (no dependencies) ✓; `dim_claimant` (needs `stg_claims`, already built) ✓; `stg_payments` (no dependencies) ✓; `int_claim_payments` (needs `stg_payments` and `stg_claims`, both built) ✓; `fct_claim_payment` (needs `int_claim_payments` and `dim_claimant`, both built) ✓. In B, `int_claim_payments` is built before `stg_claims`, one of its dependencies — invalid. In C, `dim_claimant` is built before `stg_claims` — invalid. In D, `fct_claim_payment` is built before both of its dependencies — invalid. This mirrors reasoning about directed acyclic graphs of models, a daily reality when you develop and test data models assigned by senior colleagues.

**Question 5 (moderate) — Pattern recognition in data quality results**

Your nightly data quality checks on a citizen contact dataset produced these failure counts over ten runs:

Run 1: 12, Run 2: 14, Run 3: 11, Run 4: 13, Run 5: 12, Run 6: 45, Run 7: 44, Run 8: 47, Run 9: 46, Run 10: 45

Which interpretation best fits the pattern?

A) Data quality is deteriorating gradually and randomly.
B) A step change occurred between runs 5 and 6, suggesting a specific upstream change at that point.
C) The failures are seasonal and will return to normal without intervention.
D) The checks themselves are unreliable, since the numbers keep changing.

**Correct answer: B**

**Explanation:** The values cluster tightly around 12-14 for five runs, then jump to a new tight cluster around 44-47 and stay there. That is a classic step change, not a gradual drift (which would show steadily rising values), not randomness (both clusters are stable), and not evidence of unreliable checks (small run-to-run variation is normal). A step change points to a discrete event between runs 5 and 6 — perhaps a source system release, a changed field format, or a new data entry process. Your next move as an analytics engineer would be source system analysis: find out what changed upstream on that date. Spotting step changes versus trends is a core profiling instinct.

**Question 6 (moderate) — Logical deduction about user access**

Your team's policy states:

- Every user of the analytical data platform must complete data protection training.
- Only users in the Analysis Directorate may access the unredacted case dataset.
- Some users who completed data protection training are in the Analysis Directorate.

Priya has access to the unredacted case dataset. What must be true?

A) Priya has completed data protection training and is in the Analysis Directorate.
B) Priya is in the Analysis Directorate, but she may not have completed data protection training.
C) Priya has completed data protection training, but she may not be in the Analysis Directorate.
D) Nothing can be concluded about Priya.

**Correct answer: A**

**Explanation:** Access to the unredacted dataset is restricted to the Analysis Directorate, so Priya must be in it. Having access also makes her a user of the platform, and every user must complete data protection training, so she must have completed it. Both conditions are therefore guaranteed, making A correct and B and C incomplete. Notice that the third policy statement ("some users who completed training are in the Analysis Directorate") is a distractor — it is not needed for the deduction. Assessments often include redundant premises to see whether you can identify which rules actually drive the conclusion, just as real access policies contain clauses irrelevant to the specific question at hand.

**Question 7 (moderate) — Prioritising support requests**

At 09:15 you have four items in your queue:

1. A trainee analytics engineer asks for help understanding a slowly changing dimension before their 14:00 walkthrough with a senior colleague.
2. A data user reports that this morning's benefits caseload dashboard shows zero rows — it is used at a 10:00 daily operations meeting.
3. A senior analytics engineer has asked you to draft documentation for a new dataset by the end of the week.
4. An automated alert says last night's metadata refresh completed with two non-blocking warnings.

Which order of attention is most defensible?

A) 3, 1, 2, 4
B) 2, 4, 1, 3
C) 2, 1, 4, 3
D) 1, 2, 3, 4

**Correct answer: C**

**Explanation:** Item 2 is operational and time-critical: a zero-row dashboard needed at 10:00 affects real decision-making within 45 minutes, so it comes first. Item 1 has a genuine same-day deadline (14:00) and supporting trainees is an explicit part of your role level, so it comes next once the incident is handled or escalated. Item 4 matters — non-blocking warnings can foreshadow tomorrow's failures — but it can wait until the afternoon. Item 3 has the longest deadline. Option B wrongly places routine warnings ahead of a colleague with a same-day need; options A and D leave a live operational incident waiting. Note the layered thinking: operational problems first, tactical (same-day commitments) second, then preventative and planned work — the strategic/tactical/operational lens from your problem management skill.

**Question 8 (moderate) — Problem solving in a transformation script**

A simple script you maintain applies these steps to a raw appointments file:

1. Remove rows where `appointment_date` is null.
2. Convert `appointment_date` from text (`DD/MM/YYYY`) to date type.
3. Filter to rows where `appointment_date` is within the last 365 days.
4. Count rows per clinic per month and load the results table.

Users report that the March total for one clinic is far lower than the clinic's own records. Investigation shows the source file for March contains many rows with `appointment_date` written as `2026-03-15` style (`YYYY-MM-DD`). What is the most likely mechanism for the undercount?

A) Step 1 removed the March rows because their dates were null.
B) Step 2 failed to parse `YYYY-MM-DD` values, so those rows were lost or rejected before the count.
C) Step 3 excluded the March rows because they are more than 365 days old.
D) Step 4 grouped the March rows into the wrong clinic.

**Correct answer: B**

**Explanation:** Trace the data through each step. The dates are present, so step 1 keeps them. Step 2 expects `DD/MM/YYYY`; a value like `2026-03-15` does not match that pattern, so the conversion fails and — depending on the platform — the rows error out, become null, or are rejected. Either way they never reach the count, producing exactly the observed undercount for the affected file. Step 3 cannot be the cause because the dates are recent, and step 4 concerns clinic grouping, not row loss. The general lesson is one you apply whenever you "design, code, test, correct and document simple programs or scripts": when output is wrong, walk the pipeline in order and ask at each step, "what would this step do to the problem rows?"

**Question 9 (hard) — Reverse-engineering a model from row counts**

You are reverse-engineering a data model from a live licensing system. You observe:

- Table P has 1,240 rows; its `licence_type_id` column contains 8 distinct values.
- Table Q has 8 rows and a unique `licence_type_id` for each row.
- Table R has 61,392 rows; every row contains a `licence_id` that appears in Table P and a `payment_date`.
- No `licence_id` appears more than once in Table P.

Which description of the model is best supported?

A) P is a fact table; Q and R are dimensions.
B) Q is a dimension of licence types; P is a dimension of licences referencing Q; R is a fact table of payment events referencing P.
C) R is a dimension; P is a fact table referencing R; Q is unrelated.
D) P, Q and R are all fact tables at different grains.

**Correct answer: B**

**Explanation:** Reason from cardinality and keys. Q has 8 rows with unique `licence_type_id` — a small reference table, i.e. a licence-type dimension. P has 1,240 rows with unique `licence_id` and a `licence_type_id` drawn from 8 values — one row per licence, referencing Q: a licence dimension. R has 61,392 rows, each referencing a licence and carrying a `payment_date` — many events per licence: a fact table of payments at the payment-event grain. This is the classic dimensional pattern (Kimball-style): high-volume event facts pointing at lower-volume descriptive dimensions. Options A and C invert the cardinality logic (facts are the many side), and D ignores the uniqueness evidence. When you "reverse-engineer a data model from a live system", distinct counts, uniqueness and foreign-key relationships are your primary clues.

**Question 10 (hard) — Error checking across documentation and reality**

Your data documentation states: "The `case_status` field contains exactly four values: OPEN, PAUSED, CLOSED, CANCELLED. CLOSED and CANCELLED cases are never reopened." Profiling the live table today shows: distinct values OPEN, PAUSED, CLOSED, CANCELLED, REOPENED; and 214 case IDs whose status history goes CLOSED then OPEN.

Which conclusion is soundest?

A) The profiling query must be wrong, because documentation is authoritative.
B) The documentation is out of date in at least two respects, and both the new value and the reopening behaviour need investigating with the source system team before the documentation is corrected.
C) The 214 cases are data quality errors and should be deleted.
D) The REOPENED value should be added to the documentation, and the 214 cases ignored.

**Correct answer: B**

**Explanation:** Live evidence contradicts the documentation twice: a fifth status value exists, and cases demonstrably move from CLOSED back to OPEN. Documentation is a description of reality, not a substitute for it, so A is wrong. But jumping to deletion (C) confuses "undocumented" with "invalid" — the reopening behaviour may be a legitimate business process introduced after the documentation was written; deleting real cases would corrupt the record. D fixes half the problem and ignores the other half. The professional response combines your skills: source system analysis to understand what changed, working with subject matter experts to confirm the business meaning, then updating the documentation and any affected models and tests. Documentation maintenance is not clerical — it is investigative.

**Question 11 (hard) — Deduction with multiple constraints**

Four models — Alpha, Bravo, Charlie, Delta — must be scheduled into two nightly batches (Batch 1 runs first, Batch 2 second). Constraints:

- Charlie depends on Alpha, so Charlie must run in a later batch than Alpha.
- Bravo and Delta cannot run in the same batch (they contend for the same source system).
- Delta must run in Batch 1 to meet a morning reporting deadline.

Which assignment satisfies all constraints?

A) Batch 1: Alpha, Delta. Batch 2: Bravo, Charlie.
B) Batch 1: Bravo, Delta. Batch 2: Alpha, Charlie.
C) Batch 1: Alpha, Bravo. Batch 2: Charlie, Delta.
D) Batch 1: Delta, Charlie. Batch 2: Alpha, Bravo.

**Correct answer: A**

**Explanation:** Apply the constraints in the most restrictive order. Delta must be in Batch 1. Bravo cannot share a batch with Delta, so Bravo must be in Batch 2. Charlie must run later than Alpha, and with only two batches that forces Alpha into Batch 1 and Charlie into Batch 2. Result: Batch 1 = Alpha, Delta; Batch 2 = Bravo, Charlie — option A. Check the others: B puts Bravo with Delta (violates contention rule); C puts Delta in Batch 2 (misses the deadline); D puts Charlie in Batch 1 with no earlier batch for Alpha (violates the dependency). Scheduling models around dependencies, contention and deadlines is everyday analytics engineering; the assessment version just compresses it into a neat logic puzzle.

**Question 12 (hard) — Choosing the right level of a problem**

Over the past quarter your team has fixed the same category of defect eleven times: reports built on your models break whenever the source HR system adds a new absence code, because each code is hard-coded into transformation logic in several places. A twelfth breakage has just been reported. Which response best reflects sound problem management?

A) Fix the twelfth breakage quickly and move on, because each fix takes under an hour.
B) Fix the twelfth breakage, then raise the recurring pattern with senior analytics engineers and propose a preventative remedy, such as driving the codes from a maintained reference table and adding a test that detects unmapped codes.
C) Refuse to fix the breakage until the source system team promises to stop adding codes.
D) Rebuild the entire HR data model from scratch to eliminate all hard-coding everywhere.

**Correct answer: B**

**Explanation:** This question distinguishes operational, tactical and strategic levels of a problem. The immediate breakage is operational — fix it, because users are affected now. But eleven recurrences reveal a tactical problem: the design pattern (hard-coded values scattered across logic) guarantees future failures. The proportionate remedy is a preventative measure — a reference table plus an automated test that flags unmapped codes — proposed through senior colleagues, since as an analytics engineer you develop models assigned by more senior engineers and contribute to remedies rather than unilaterally redesigning. A treats a chronic problem as a series of one-offs; C holds users hostage to an upstream negotiation; D is disproportionate and risky. B shows exactly what "contribute to the implementation of remedies and preventative measures" looks like.

**Question 13 (moderate) — Pattern completion in a test matrix**

You are executing a test script for a new data model. The script tests each combination of load type and dataset, and the results grid so far reads:

| | Full load | Incremental load |
|---|---|---|
| Payments dataset | Pass | Pass |
| Claims dataset | Pass | Fail |
| Appointments dataset | Pass | Not yet run |

The failure log for the claims incremental test says: "Rows updated in source after initial load were not reflected in the model." Following the pattern of what is being tested, what should you check most carefully when you run the final test?

A) Whether the appointments full load completes faster than the payments full load.
B) Whether appointments rows updated in the source after the initial load are correctly reflected by the incremental load.
C) Whether the claims dataset contains sensitive fields.
D) Whether the payments tests should be re-run.

**Correct answer: B**

**Explanation:** The grid shows full loads passing everywhere, and the one observed failure is specific to incremental logic — updates made after the initial load being missed. The remaining untested cell is the appointments incremental load, and the sensible hypothesis is that whatever defect affects claims incremental handling (for example, an update-detection or merge condition) could also affect appointments. So the final test deserves particular attention on updated-row handling — option B. Options A, C and D drift away from both the pattern in the grid and the evidence in the log. This reflects your testing skill: "correctly execute test scripts under supervision" includes noticing what earlier results imply about where the remaining risk sits, and understanding the role of testing rather than executing it mechanically.

### Preparation tips

- **Practise with your own artefacts.** Before an assessment, spend an evening reading model dependency graphs, metadata records and data quality reports with a critical eye. Ask: what is the grain here, what would break this, which two statements could contradict each other? You are rehearsing the exact mental moves the test samples.
- **Verbalise your deductions.** For logic questions, get into the habit of saying (or writing) "the rule says X leads to Y; I observed Y; that does *not* prove X." One sentence of explicit reasoning prevents most deduction errors.
- **Time-box, don't rush.** In a 20-minute test with 20 questions, give each question a fair minute, flag anything that resists you, and return at the end. A flagged question answered calmly beats four questions answered in panic.
- **Do a short warm-up.** Ten minutes of puzzle-style questions immediately before the test gets you into gear, exactly as you would warm up by scanning yesterday's pipeline logs before a morning of debugging.
- **Trust your experience.** You already prioritise incidents, trace dependencies and check records for consistency at work. The assessment format is new; the thinking is not.

### Common pitfalls

- **Reasoning backwards along one-way rules.** "If extract fails then staging is stale" does not mean "staging is stale, so the extract failed." This is the single most common logical error in these tests — and in real incident investigations.
- **Answering from your own workplace instead of the question.** Your department may name tables differently or schedule loads differently; answer from the conventions and rules the question gives you, not from home habits.
- **Losing time to one hard question.** Assessments report speed and accuracy together. Skipping and returning is a strategy, not a failure.
- **Skimming detailed records.** Error-checking questions hide the inconsistency in the fourth or fifth field, because real metadata errors hide there too. Read every field once, deliberately.
- **Ignoring the difficulty label.** If a question marked "easy" seems to have a trap, you may be overthinking it; if a "hard" question seems obvious, re-read it — you have probably missed a constraint.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment evaluates how well you analyse, interpret, and make sound decisions using numerical data. It is deliberately built around business mathematics rather than abstract formulas: the inputs are tables, percentages, ratios, budgets, schedules, and performance metrics — the same shapes of number you meet in data quality dashboards, pipeline run logs, storage reports, and training registers.

For an analytics engineer, this is home territory. Your role is quantitative by nature: you profile source systems (row counts, null rates, distinct values), you monitor data quality (pass rates, failure trends), you reason about capacity (load durations, storage growth), and you report on user support (ticket volumes, training attendance). The assessment simply asks you to do the same interpretation quickly and accurately under a time limit.

Typical format: online, strictly timed (often around 45-90 seconds per question), multiple choice, and calculator friendly — most platforms allow or provide an onscreen calculator, because the test prioritises interpretation over mental arithmetic. The skill being measured is not whether you can multiply, but whether you can extract the right figures from a busy table, choose the right operation, and sanity-check the result before the clock moves on.

Every practice question below shows the full arithmetic in its explanation. Work each one with a calculator and rough paper, exactly as you would in a real test, and compare your working — not just your answer — with the explanation.

### What it measures for your role

- **Percentages, rates and proportions** underpin your **data analysis and synthesis** skill: data profiling is largely about proportions — what fraction of rows are null, duplicated, or out of range — and presenting clear insights means turning raw counts into rates colleagues can grasp.
- **Reading multi-column tables accurately** supports **data modelling, cleansing and enrichment** and **metadata management**: row counts, distinct counts and load statistics are the evidence base for modelling decisions and for keeping metadata records accurate.
- **Trend and comparison calculations** support your **problem management** skill: deciding whether a failure rate is drifting, stepping, or stable determines whether a problem is operational noise or a tactical issue needing a preventative remedy.
- **Budget, capacity and scheduling arithmetic** supports **programming and build (data engineering)** and your support duties: estimating run times, storage growth and training capacity is part of building and supporting data services.
- **Clear numerical communication** supports **communicating between the technical and non-technical**: you will often need to translate "0.7% of rows failed validation" into terms a policy colleague can act on — which starts with getting the 0.7% right.

### Practice questions

**Question 1 (easy) — Null rate in profiling**

You profile a source table of 250,000 citizen contact records. The `email_address` column contains 212,500 non-null values. What percentage of records have a null `email_address`?

A) 12%
B) 15%
C) 17.5%
D) 85%

**Correct answer: B**

**Explanation:** Null values = 250,000 − 212,500 = 37,500. Null rate = 37,500 ÷ 250,000 = 0.15 = **15%**. A quick sanity check: 10% of 250,000 is 25,000 and 20% is 50,000, so 37,500 sits exactly halfway — 15%. Option D (85%) is the *non-null* rate; under time pressure, the single most common numeric error is reporting the complement of the figure asked for. When you write profiling summaries for colleagues, this same care applies: always state whether a percentage refers to complete or missing values.

**Question 2 (easy) — Data quality pass rate change**

Last month your nightly quality checks on the payments model ran 30 times, with 27 fully passing runs. This month they ran 31 times, with 24 fully passing runs. By how many percentage points did the pass rate fall?

A) 3.0 percentage points
B) 9.6 percentage points
C) 12.6 percentage points
D) 22.6 percentage points

**Correct answer: C**

**Explanation:** Last month's pass rate = 27 ÷ 30 = 0.90 = 90.0%. This month's = 24 ÷ 31 ≈ 0.7742 = 77.4%. Fall = 90.0 − 77.4 = **12.6 percentage points**. Option A is the fall in the raw count of passing runs (27 − 24 = 3), not the rate; option B is roughly the fall if you mistakenly divide both months by 31. Note the phrase "percentage points": a fall *from* 90% *to* 77.4% is 12.6 points, but a *relative* fall of 12.6 ÷ 90 = 14%. Assessments — and quality reports to stakeholders — reward keeping those two ideas distinct.

**Question 3 (easy) — Training session capacity**

You provide training for users of a new reporting dataset. Each session holds 12 people. There are 87 registered users to train, and 15 have already been trained. How many sessions do you need for the remainder?

A) 5
B) 6
C) 7
D) 8

**Correct answer: B**

**Explanation:** Remaining users = 87 − 15 = 72. Sessions = 72 ÷ 12 = **6** exactly. If the division had not been exact — say 75 remaining — you would round *up* (75 ÷ 12 = 6.25 → 7 sessions), because a fraction of a session still requires a whole booking. Capacity questions almost always involve this "ceiling" logic; watch for it whenever the units are indivisible things like sessions, licences, or batch windows.

**Question 4 (moderate) — Interpreting a load statistics table**

The nightly load log for four models shows:

| Model | Rows loaded | Duration (minutes) | Failures this month |
|---|---|---|---|
| fct_claim_payment | 1,440,000 | 48 | 1 |
| dim_claimant | 96,000 | 8 | 0 |
| fct_appointment_booked | 720,000 | 30 | 3 |
| fct_repair_completed | 540,000 | 27 | 2 |

Which model loads rows at the fastest rate (rows per minute)?

A) fct_claim_payment
B) dim_claimant
C) fct_appointment_booked
D) fct_repair_completed

**Correct answer: A**

**Explanation:** Compute rows per minute for each: fct_claim_payment = 1,440,000 ÷ 48 = **30,000**; dim_claimant = 96,000 ÷ 8 = 12,000; fct_appointment_booked = 720,000 ÷ 30 = 24,000; fct_repair_completed = 540,000 ÷ 27 = 20,000. The largest is 30,000 rows/minute for fct_claim_payment. Two traps: the biggest table is not automatically the fastest *rate* (you must divide), and the failures column is a distractor — it is not part of this question. Real dashboards are full of columns you must deliberately ignore; so are numeric tests.

**Question 5 (moderate) — Duplicate reduction percentage**

A cleansing step you built removes duplicate citizen records. Before cleansing, a monthly file has 184,000 records; after cleansing, 161,000 remain. What percentage of the original records were removed as duplicates?

A) 8.75%
B) 12.5%
C) 14.3%
D) 23%

**Correct answer: B**

**Explanation:** Records removed = 184,000 − 161,000 = 23,000. Percentage of the *original* file = 23,000 ÷ 184,000 = 0.125 = **12.5%**. Option C (14.3%) comes from dividing by the *post-cleansing* count (23,000 ÷ 161,000); option D just restates the raw thousands as a percent. The denominator question — "percentage of what?" — decides the answer, and it matters in real reporting too: "12.5% of the source file was duplicated" and "duplicates equalled 14.3% of the clean file" are different claims, and your data quality documentation should say which you mean.

**Question 6 (moderate) — Storage growth projection**

Your fact table currently occupies 400 GB and grows by 5% per month, compounding. Approximately how much storage will it occupy in three months?

A) 460 GB
B) 463 GB
C) 469 GB
D) 500 GB

**Correct answer: B**

**Explanation:** Compound growth: 400 × 1.05 = 420 after month one; 420 × 1.05 = 441 after month two; 441 × 1.05 = 463.05 ≈ **463 GB** after month three. Equivalently, 400 × 1.05³ = 400 × 1.157625 = 463.05. Option A (460) is the *simple* growth answer (400 + 3 × 20), which ignores compounding — a small difference over three months but a large one over three years, which is why capacity plans use compound rates. In a timed test, if two options are close (460 vs 463), that is usually the compounding distinction being tested; compute the powers rather than estimating.

**Question 7 (moderate) — Ratio of records across sources**

A combined dataset you maintain draws records from three source systems in the ratio 5 : 3 : 2 (casework : payments : appointments). The combined dataset contains 640,000 records. How many come from the payments system?

A) 128,000
B) 192,000
C) 213,333
D) 320,000

**Correct answer: B**

**Explanation:** Total ratio parts = 5 + 3 + 2 = 10. One part = 640,000 ÷ 10 = 64,000. Payments = 3 parts = 3 × 64,000 = **192,000**. Option A is 2 parts (the appointments share), option D is 5 parts (casework), and option C comes from dividing 640,000 by 3 — a common slip when ratios are misread as equal thirds. Ratio questions reward writing the parts down explicitly before touching the calculator; in source system analysis you use the same technique to check whether a combined load matches the expected contribution of each feed.

**Question 8 (moderate) — Support ticket workload**

Your team logged support tickets from data users over four weeks:

| Week | Tickets received | Tickets resolved |
|---|---|---|
| 1 | 34 | 30 |
| 2 | 41 | 38 |
| 3 | 29 | 33 |
| 4 | 36 | 31 |

The backlog at the start of week 1 was 12 tickets. What is the backlog at the end of week 4?

A) 8
B) 12
C) 20
D) 28

**Correct answer: C**

**Explanation:** Total received = 34 + 41 + 29 + 36 = 140. Total resolved = 30 + 38 + 33 + 31 = 132. Net change = 140 − 132 = +8. End backlog = starting backlog + net change = 12 + 8 = **20**. Notice week 3 resolved more than it received (33 vs 29) — backlogs can shrink in individual weeks while still growing overall. Option A is the net change alone (forgetting the starting backlog); option B assumes no change; option D double-counts. Running-total questions reward a simple discipline: write the opening balance first, then apply the flows. The same discipline keeps your support metrics honest when you report them to the team.

**Question 9 (hard) — Weighted data quality score**

Your department scores each dataset on three data quality dimensions, weighted as follows: completeness 50%, accuracy 30%, timeliness 20%. The benefits dataset scores 92 for completeness, 78 for accuracy, and 65 for timeliness. What is its weighted overall score?

A) 78.3
B) 78.4
C) 82.4
D) 83.5

**Correct answer: C**

**Explanation:** Weighted score = (92 × 0.50) + (78 × 0.30) + (65 × 0.20) = 46.0 + 23.4 + 13.0 = **82.4**. Option A/B are near the simple (unweighted) average, (92 + 78 + 65) ÷ 3 = 78.3 — the classic error of ignoring the weights. Check plausibility: completeness carries half the weight and is the highest score, so the weighted result should sit *above* the simple average, which 82.4 does. Weighted scores appear constantly in data quality reporting and prioritisation matrices, and assessments test whether you apply weights rather than default to the mean.

**Question 10 (hard) — Run window feasibility**

Your overnight batch window runs from 01:00 to 06:30. Three jobs must run *sequentially*: extract (75 minutes), transform (currently 140 minutes), and publish (55 minutes). A planned source system change will increase extract volume by 20%, and extract duration scales proportionally with volume. Will the batch still fit the window, and with how much slack?

A) Yes, with 45 minutes of slack.
B) Yes, with 30 minutes of slack.
C) Yes, with 15 minutes of slack.
D) No, it will overrun by 15 minutes.

**Correct answer: A**

**Explanation:** Window length = 01:00 to 06:30 = 5.5 hours = 330 minutes. New extract duration = 75 × 1.20 = 90 minutes. Total sequence = 90 + 140 + 55 = 285 minutes. Slack = 330 − 285 = **45 minutes**, so the batch fits comfortably — option A. The wrong options map to specific slips: if you selected D, you probably used 105 minutes for the extract (that would be a 40% increase, not 20%) and 300 minutes for the window (forgetting the half hour in 06:30); option C comes from making just one of those two errors. The reliable method is to convert all clock times to minutes first, apply a percentage increase as multiplication by 1.20 rather than mental adjustment, and add the job durations in a written line you can re-check. Capacity questions like this mirror real batch planning: a proposed upstream change lands on your desk, and you must say with confidence whether tonight's window still holds.

**Question 11 (hard) — Percentage of a percentage in cleansing**

A source file contains 480,000 records. Profiling shows 15% of records have at least one address field issue. Of those problem records, 40% can be fixed automatically by your standardisation script; the rest need referral to the data owner. How many records need referral?

A) 28,800
B) 43,200
C) 72,000
D) 192,000

**Correct answer: B**

**Explanation:** Problem records = 480,000 × 0.15 = 72,000. Automatically fixable = 72,000 × 0.40 = 28,800. Needing referral = 72,000 − 28,800 = 43,200 — or directly, 72,000 × 0.60 = **43,200**. Option A is the auto-fixable count (the complement again); option C is all problem records; option D applies 40% to the whole file. Chained percentages must each be applied to the correct base: 15% of the file, then 60% *of that subset*. Writing the intermediate figure (72,000) down before the second step prevents almost all errors here — the same habit that makes your data quality summaries auditable.

**Question 12 (hard) — Comparing model rebuild costs**

Two candidate designs for a reporting model differ in compute cost:

- Design X: full rebuild nightly, 42 minutes of compute per run, at £0.85 per compute-minute.
- Design Y: incremental build nightly, 9 minutes of compute per run at £0.85 per compute-minute, plus a full weekly consolidation of 65 minutes at the same rate.

Over a 28-day period (28 nightly runs; 4 weekly consolidations), how much cheaper is Design Y?

A) £564.40
B) Nothing — Design X is cheaper
C) £785.40
D) £435.20

**Correct answer: A**

**Explanation:** Design X: 28 runs × 42 minutes = 1,176 minutes; cost = 1,176 × £0.85 = £999.60 (check: 1,176 × 0.8 = 940.80; 1,176 × 0.05 = 58.80; total £999.60). Design Y: nightly = 28 × 9 = 252 minutes; weekly consolidations = 4 × 65 = 260 minutes; total = 512 minutes; cost = 512 × £0.85 = £435.20 (check: 512 × 0.8 = 409.60; 512 × 0.05 = 25.60). Saving = £999.60 − £435.20 = **£564.40**, option A. Option D is Design Y's total cost, not the saving — always re-read what quantity the question asks for. Option C is what you get if you forget the weekly consolidations entirely (£999.60 − 252 × £0.85 = £999.60 − £214.20 = £785.40), silently flattering the incremental design. The working method matters as much as the answer: lay out each design's minutes line by line, convert to pounds once at the end, then subtract. This is exactly the comparison you make in real life when weighing a full-rebuild pattern against an incremental pattern — and just as in the test, the commonest real-world error is leaving a whole cost component out of one side of the comparison.

**Question 13 (moderate) — Distinct values and coverage**

A reference table of local authority codes should contain 317 entries. Your loaded dimension contains 309 distinct codes, and the fact table references 302 distinct codes. What percentage of the official code list is missing from your dimension (to one decimal place)?

A) 2.5%
B) 4.7%
C) 8.0%
D) 97.5%

**Correct answer: A**

**Explanation:** Missing codes = 317 − 309 = 8. Missing percentage = 8 ÷ 317 = 0.02524 ≈ **2.5%**. The fact table's 302 is a distractor for this particular question — it tells you about usage, not completeness of the dimension. Option B (4.7%) comes from using 317 − 302 = 15 as the numerator, i.e. answering a different question ("what share of official codes never appear in the facts?"). Option D is the coverage rate, not the gap. Reference-data coverage checks like this are bread-and-butter analytics engineering; the assessment version tests whether you match the right numerator and denominator to the exact question asked.

**Question 14 (moderate) — Averages with a correction**

Five nightly runs of your transformation job took 38, 41, 44, 39 and 58 minutes. The 58-minute run is then confirmed to have included a one-off 20-minute manual pause that should be excluded from performance figures. What is the corrected average run time?

A) 38.0 minutes
B) 40.0 minutes
C) 44.0 minutes
D) 41.2 minutes

**Correct answer: B**

**Explanation:** Corrected fifth run = 58 − 20 = 38 minutes. Corrected total = 38 + 41 + 44 + 39 + 38 = 200 minutes. Average = 200 ÷ 5 = **40.0 minutes**. Option C (44.0) is the average with the uncorrected 58 included ((38+41+44+39+58) = 220 ÷ 5 = 44); option D comes from excluding the fifth run entirely and averaging four values (162 ÷ 4 = 40.5, or with a slip, 41.2). The question mirrors a real reporting judgement: when a measurement is contaminated by a known one-off, correct it explicitly and document why, rather than either leaving it in or silently dropping the data point.

**Question 15 (hard) — Index of change across two dimensions**

Your model's user base and query volume both grew this quarter. Registered users rose from 240 to 300, while total queries rose from 36,000 to 49,500. By how much did the average number of queries *per user* change?

A) It rose by 10%
B) It rose by 15 queries per user
C) It rose by 37.5%
D) It fell, because users grew faster than queries

**Correct answer: B**

**Explanation:** Last quarter: 36,000 ÷ 240 = 150 queries per user. This quarter: 49,500 ÷ 300 = 165 queries per user. Change = 165 − 150 = **15 queries per user** (a 10% relative rise, since 15 ÷ 150 = 0.10 — so option A describes the same movement in different units, but the question asks "by how much", and only B states the change in the quantity asked about; in a real test read the options' units as carefully as the numbers). Option C (37.5%) is the growth in *total* queries (13,500 ÷ 36,000), not queries per user; option D has the comparison backwards — queries grew 37.5% while users grew 25% (60 ÷ 240), so intensity per user rose. Per-unit rates are how you separate "more users" from "heavier use" when you report adoption of your data models to the team — two stories with very different support implications.

**Question 16 (moderate) — Estimating documentation effort**

You must document 45 datasets. A colleague's records show that documenting a *simple* dataset takes about 2.5 hours and a *complex* one about 6 hours. Of your 45 datasets, one third are complex and the rest are simple. You can spend 10 hours per week on documentation. Roughly how many whole weeks will the work take?

A) 12 weeks
B) 15 weeks
C) 17 weeks
D) 27 weeks

**Correct answer: C**

**Explanation:** Complex datasets = 45 ÷ 3 = 15; simple = 45 − 15 = 30. Hours = (15 × 6) + (30 × 2.5) = 90 + 75 = 165 hours. Weeks = 165 ÷ 10 = 16.5, which rounds *up* to **17 whole weeks** — you cannot finish mid-week capacity you do not have, so ceiling logic applies as in Question 3. Option B (15) comes from forgetting to round up and also miscounting the split; option A assumes all 45 are simple-ish at 2.5 hours plus rounding; option D treats all 45 as complex. Effort estimates like this are exactly what a senior analytics engineer will ask you for before committing your team to a documentation programme, and the same three steps — split by type, multiply, convert to calendar — keep the estimate defensible.

### Preparation tips

- **Rebuild fluency with the core four.** Percentages, ratios, averages (simple and weighted), and rates cover the great majority of questions. Ten minutes a day for a week — using your own team's run logs and quality dashboards as material — restores speed remarkably fast.
- **Always identify the denominator before calculating.** Most wrong options in numeric tests are correct calculations on the wrong base. Say to yourself: "percentage *of what*?"
- **Write intermediate figures down.** Chained calculations (percentage of a percentage, backlog running totals, cost comparisons) go wrong when held in your head. One scribbled line per step is faster than one redo.
- **Use the calculator for arithmetic, your brain for checking.** After every answer, do a one-second plausibility check: is the result the right order of magnitude? Should it be above or below the simple average? A weighted score dominated by a high-weight, high-value dimension should sit above the mean, for example.
- **Practise reading tables under time.** Give yourself 90 seconds per question when practising. Train your eye to find the right row and column *first*, and to notice scale qualifiers such as "in thousands", "GB", or "per minute".
- **Be kind to yourself about speed.** Accuracy under mild pressure is the goal; frantic speed produces the complement errors and wrong denominators the test is designed to detect.
- **Rehearse the unit conversions you actually meet.** Minutes to hours, GB per month to GB per year, rows per minute, pounds per compute-minute. Convert everything to one consistent unit at the start of a question — mixed units are where multi-step calculations quietly go wrong, in tests and in capacity plans alike.
- **Learn your calculator's memory functions.** Storing an intermediate result (72,000 problem records; 285 total minutes) and recalling it beats retyping, and eliminates transcription errors — the numeric equivalent of writing your working down.

### Common pitfalls

- **Misreading chart and table labels.** Confusing weekly with monthly figures, or missing qualifiers like "in thousands", changes every subsequent step. Read headers before numbers.
- **Reporting the complement.** Non-null rate instead of null rate, pass rate instead of failure rate, auto-fixed instead of referred. Re-read the final sentence of the question before you commit.
- **Percentage points versus percent.** A fall from 90% to 77.4% is 12.6 percentage points but a 14% relative fall. Both appear as options when the distinction matters.
- **Simple versus compound growth.** Storage and volume projections usually compound; adding a flat amount per period underestimates growth and the near-miss option will be waiting for you.
- **Over-calculating.** Sometimes estimation and elimination answer the question faster than full computation — if three options are wildly implausible, a rough check suffices.
- **Time sink questions.** One stubborn multi-stage calculation can consume five questions' worth of time. Flag it, move on, return with fresh eyes.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment measures how accurately you understand, analyse, and draw conclusions from written material. The passages mirror the reading demands of your actual role: data standards, documentation guidance, policy extracts, stakeholder emails, incident reports, and meeting notes. The questions then test whether you can separate what the text *actually says* from what you assume, expect, or already know.

The dominant format is **True / False / Cannot Say**. You read a passage, then judge a statement: **True** if the passage logically supports it, **False** if the passage contradicts it, and **Cannot Say** if the passage provides insufficient information either way. The golden rule is to answer based strictly on the text provided, ignoring outside knowledge — even accurate outside knowledge. Some tests add multiple-choice comprehension questions asking for the best summary, the author's main point, or the correct application of a rule to a case. Timing is usually tight, often less than a minute per question, to simulate workplace reading under deadline.

Why does this matter for an analytics engineer? Because your work is dense with authoritative text. You draft documentation that must meet standards, so you must read the standards precisely. You refine requirements in response to user feedback, so you must extract exactly what a user's email does and does not commit to. You maintain metadata that others rely on word by word. A misreading that survives into a data model or a documentation page misleads every downstream user — which is why employers test this skill directly.

### What it measures for your role

- **Precise comprehension of standards and policies** maps to your duty to **draft documentation of data that meets standards** and to **develop standards for data transformation**: you cannot meet a standard you have misread.
- **Distinguishing stated fact from inference** maps to **data analysis and synthesis**: presenting clear insights requires you to know which claims your evidence supports and which it merely suggests.
- **Reading stakeholder correspondence accurately** maps to **communicating between the technical and non-technical** and to **refining requirements in response to feedback**: user emails mix requests, assumptions and background, and you must separate them before acting.
- **Careful reading of procedural text** maps to your **testing** skill ("correctly execute test scripts under supervision") and **metadata management**: test steps and repository entries mean exactly what they say, no more.
- **Identifying what a report does and does not establish** maps to **problem management**: incident write-ups often invite conclusions the evidence does not support, and your remedies must rest on what is actually known.

### Practice questions

**Passage A — extract from a departmental data transformation standard**

> "All transformation code must be stored in the department's version control system. Each data model must have an accountable owner recorded in the metadata repository before the model is promoted to the production environment. Models that read personal data must, in addition, have a completed data protection impact screening. Documentation should be updated within five working days of any change to a model's structure; documentation updates for changes to descriptive text alone may be batched monthly. Where a model is decommissioned, its documentation must be archived, not deleted."

**Question 1 (easy) — True / False / Cannot Say**

Statement: "A data model can be promoted to production before an accountable owner is recorded in the metadata repository."

A) True
B) False
C) Cannot Say

**Correct answer: B (False)**

**Explanation:** The passage states each model "must have an accountable owner recorded in the metadata repository **before** the model is promoted to the production environment." The statement directly contradicts this sequencing requirement, so it is False. This is the easiest kind of verbal question — a direct contradiction — but under time pressure candidates sometimes select Cannot Say because the statement is phrased as a possibility ("can be"). When a passage says something must happen before X, a claim that X can happen without it is contradicted, not undetermined.

**Question 2 (moderate) — True / False / Cannot Say**

Statement: "A model that does not read personal data does not require a data protection impact screening before promotion."

A) True
B) False
C) Cannot Say

**Correct answer: C (Cannot Say)**

**Explanation:** The passage says models that read personal data must "in addition" have the screening. It tells us the screening is required *for* personal-data models; it does not say the screening is required *only* for them. Another clause of the standard, or another policy entirely, might require screenings more broadly — the passage is silent. Concluding "not mentioned as required, therefore not required" is the classic inference error this format exists to catch. Compare Question 1: there the passage contradicted the statement; here it simply does not settle it. Precision about what a standard does *not* say is a professional skill in itself — it tells you when to go and check rather than assume.

**Question 3 (moderate) — True / False / Cannot Say**

Statement: "If only a model's descriptive text changes, the documentation update may wait until a monthly batch."

A) True
B) False
C) Cannot Say

**Correct answer: A (True)**

**Explanation:** The passage distinguishes two cases: structural changes require documentation updates "within five working days", while "documentation updates for changes to descriptive text alone may be batched monthly." The statement restates the second case accurately, so it is True. Note the load-bearing word "alone" — if a change touched both structure and descriptive text, the five-day rule would apply because the change is not to descriptive text alone. Verbal tests reward spotting such qualifier words ("alone", "in addition", "before", "should" versus "must"); so does drafting documentation against a real standard.

**Question 4 (moderate) — Multiple choice**

According to the passage, what must happen to the documentation of a decommissioned model?

A) It must be deleted within five working days.
B) It must be archived rather than deleted.
C) It must be transferred to the accountable owner.
D) The passage does not address decommissioned models.

**Correct answer: B**

**Explanation:** The final sentence states: "Where a model is decommissioned, its documentation must be archived, not deleted." Option B paraphrases this exactly. Option A wrongly imports the five-day figure from the unrelated update rule — a favourite distractor technique, reusing a true number in a false context. Option C invents a rule, and D denies text that is plainly present. When you scan a passage for a specific rule, read the whole relevant sentence, not just the keyword: "archived, not deleted" is a two-part instruction whose second half is the point.

**Passage B — email from a data user in a casework team**

> "Hi — thanks for the new caseload model. It's mostly working well for us, but the regional breakdown doesn't match what our team publishes in the quarterly bulletin. I think this might be because our bulletin uses the region where the case was *opened*, while your model seems to use the claimant's current home region. If that's right, could we have both? The bulletin figures are signed off by the Head of Casework Statistics, so we can't change our method this side of the next quarterly release. There's no rush on the extra field itself, but we do need to understand the difference before our numbers go to the directorate board on the 14th."

**Question 5 (easy) — True / False / Cannot Say**

Statement: "The user has confirmed that the model uses the claimant's current home region."

A) True
B) False
C) Cannot Say

**Correct answer: B (False)**

**Explanation:** The user writes "I think this might be because…" and "your model *seems* to use" — explicitly tentative language — and then asks "If that's right…". The statement claims a confirmation, which misrepresents the hedged wording, so it is False. (If the statement had read "the user believes the model may use the claimant's current home region," that would be True.) Distinguishing what a stakeholder asserts from what they hypothesise is exactly the reading you do when refining requirements from feedback: acting on a guess as if it were a confirmed fact is how wrong fields get built.

**Question 6 (moderate) — True / False / Cannot Say**

Statement: "The casework team is unable to change its bulletin methodology before the next quarterly release."

A) True
B) False
C) Cannot Say

**Correct answer: A (True)**

**Explanation:** The email states: "we can't change our method this side of the next quarterly release," and gives the reason (the figures are signed off by the Head of Casework Statistics). The statement is a faithful paraphrase — "unable to change before the next quarterly release" matches "can't change this side of the next quarterly release" — so it is True. Be careful not to over-read the *reason* as a separate claim: the passage does not say the Head of Casework Statistics would refuse a change, only that sign-off is why the method is fixed for now. Answer the statement in front of you, not neighbouring statements you could imagine.

**Question 7 (hard) — True / False / Cannot Say**

Statement: "The user needs the additional regional field to be delivered before the 14th."

A) True
B) False
C) Cannot Say

**Correct answer: B (False)**

**Explanation:** Read the two deadlines apart. The user says "There's no rush on the extra field itself" — the field is explicitly *not* urgent — "but we do need to understand the difference before... the 14th." What is needed by the 14th is an *explanation of the discrepancy*, not the delivery of the field. The statement attaches the deadline to the wrong deliverable, contradicting the passage, so it is False. This is a highly realistic requirements-reading trap: a message contains one date and two requests, and the careless reader welds the date to the bigger request. When you triage user feedback, separating "what is wanted" from "when each part is wanted" is half the job.

**Question 8 (moderate) — Multiple choice**

Which of the following best summarises the user's overall message in Passage B?

A) The model is wrong and must be corrected before the 14th.
B) The model is broadly useful, but a definitional difference from the bulletin needs to be explained before the 14th, and an additional field would be welcome at some point.
C) The bulletin methodology is wrong and the user wants help changing it.
D) The user wants the model withdrawn until the figures match.

**Correct answer: B**

**Explanation:** The email opens positively ("mostly working well"), identifies a *suspected definitional* difference rather than an error ("I think this might be because…"), asks for both definitions to be available ("could we have both?"), fixes the bulletin method for now, and sets a deadline only for *understanding* the difference. Option B captures all of this. Option A converts a definitional difference into a defect and misplaces the deadline; C reverses who is willing to change; D invents an escalation. Summary questions reward weighing the whole passage rather than its most dramatic sentence — the same balance you need when you relay user feedback to senior analytics engineers accurately.

**Passage C — extract from a data quality incident report**

> "On 3 June, the morning refresh of the housing repairs model completed 47 minutes late. The delay followed a change to the source extract implemented by the supplier the previous evening. Because the refresh overran, the 08:00 automated quality checks ran against partially loaded data and reported 3,214 failures, of which the great majority were subsequently confirmed to be false positives caused by the incomplete load. Eleven failures related to genuinely malformed postcode values and were referred to the data owner. The team has asked the supplier for advance notice of future extract changes. A proposal to make the quality checks wait for load completion is under consideration."

**Question 9 (easy) — True / False / Cannot Say**

Statement: "The 08:00 quality checks ran before the data load had fully completed."

A) True
B) False
C) Cannot Say

**Correct answer: A (True)**

**Explanation:** The passage says the refresh "overran" and the checks "ran against partially loaded data" — a direct statement that the load was incomplete when the checks executed. The statement paraphrases this accurately. The supporting arithmetic (a refresh 47 minutes late against an 08:00 check time) is consistent, but you do not need to reconstruct the timeline: the phrase "partially loaded data" settles it. When the passage states a fact plainly, resist the urge to second-guess it with your own operational experience of how loads usually behave.

**Question 10 (hard) — True / False / Cannot Say**

Statement: "The supplier's change to the source extract caused the 47-minute delay."

A) True
B) False
C) Cannot Say

**Correct answer: C (Cannot Say)**

**Explanation:** Tempting, isn't it? The passage says the delay "followed" the supplier's change — a statement of sequence, not causation. The report's authors were careful (as good incident reports are) not to assert cause before investigation. Post hoc reasoning — "B came after A, so A caused B" — is precisely what both verbal tests and problem management discipline train you to resist. Had the passage said the delay "was caused by" or "resulted from" the change, the answer would be True. As written, causation is plausible but unestablished: Cannot Say. Note how this mirrors your problem management skill: remedies must rest on established causes, not on suggestive timelines.

**Question 11 (moderate) — True / False / Cannot Say**

Statement: "Most of the 3,214 reported failures were genuine data quality problems."

A) True
B) False
C) Cannot Say

**Correct answer: B (False)**

**Explanation:** The passage states "the great majority were subsequently confirmed to be false positives caused by the incomplete load," and separately that eleven failures were genuine (malformed postcodes). The statement claims the opposite of the stated majority, so it is False. Watch the two quantities: 3,214 reported, eleven genuine. A careless reading that anchors on the large number and the word "failures" invites the wrong answer. In your own quality reporting, this distinction — alerts raised versus defects confirmed — is one your non-technical stakeholders will rely on you to make clearly.

**Question 12 (moderate) — True / False / Cannot Say**

Statement: "The quality checks have been changed so that they now wait for the load to complete before running."

A) True
B) False
C) Cannot Say

**Correct answer: B (False)**

**Explanation:** The passage says this change is "a proposal… under consideration" — it has not been implemented. The statement asserts it as done, which contradicts the passage's explicit framing, so it is False. Some candidates argue for Cannot Say on the basis that the proposal might have been implemented since; but the passage describes the state of affairs as at the report, and within that text the change is explicitly not yet made. "Proposed" versus "implemented" is one of the most consequential word pairs in government reporting — status reports, board papers and audit responses all turn on it, and so does accurate metadata about your own controls.

**Question 13 (hard) — Multiple choice**

Which action does the passage state has *already been taken* (rather than proposed or considered)?

A) Making the quality checks wait for load completion.
B) Asking the supplier for advance notice of future extract changes.
C) Correcting the eleven malformed postcode values.
D) Rescheduling the morning refresh to an earlier time.

**Correct answer: B**

**Explanation:** The passage uses the perfect tense for exactly one action: "The team **has asked** the supplier for advance notice of future extract changes." Option A is explicitly a proposal under consideration. Option C is close but wrong: the eleven failures "were **referred to** the data owner" — referral happened, but the passage never says the values were *corrected*; correction may not even be the analytics team's job. Option D never appears. This question rewards reading verbs and their tenses with the same precision you apply to test scripts: "referred" is not "resolved", "proposed" is not "implemented", and documentation that blurs these differences misleads its readers.

**Passage D — extract from guidance on metadata repository entries**

> "Every dataset entry in the metadata repository must name a data owner and a technical contact; these may be the same person only where the dataset is used by a single team. Entries must state the dataset's update frequency and its retention period. Where retention is governed by legislation, the entry must cite the relevant provision. Entries for datasets containing personal data must additionally record the lawful basis for processing. Repository administrators review a sample of entries each quarter; entries found to be materially inaccurate are flagged to the owning team, which must correct them within ten working days of being notified."

**Question 14 (moderate) — True / False / Cannot Say**

Statement: "The data owner and the technical contact must always be different people."

A) True
B) False
C) Cannot Say

**Correct answer: B (False)**

**Explanation:** The passage says the two roles "may be the same person only where the dataset is used by a single team." So there is a defined circumstance in which one person can hold both roles — the statement's "always" is contradicted. Notice the double qualifier: "may… only where" permits the combination *and* restricts it. A statement claiming they can *never* be the same person is False; a statement claiming they can *always* be the same person would also be False; the passage occupies the precise middle ground. Reading permissions and restrictions as exact conditions is the same discipline you use when deciding whether a dataset entry you are drafting complies with the guidance.

**Question 15 (hard) — True / False / Cannot Say**

Statement: "A team notified of a materially inaccurate entry has ten working days to correct it, measured from the date the inaccuracy first arose."

A) True
B) False
C) Cannot Say

**Correct answer: B (False)**

**Explanation:** The deadline in the passage runs "within ten working days **of being notified**" — the clock starts at notification, not when the inaccuracy first arose (which might have been months earlier and may not even be known). The statement quietly moves the starting point, contradicting the text, so it is False. Deadline-anchoring tricks are a staple of verbal tests because they are a staple of real compliance misreadings: "within 10 days of X" questions always deserve a second look at what X actually is. If the statement had simply said "ten working days to correct it after being notified", it would have been True.

**Question 16 (moderate) — Multiple choice**

According to Passage D, which of the following entries would be non-compliant?

A) An entry for a single-team dataset naming one person as both owner and technical contact, with frequency, retention and (where applicable) lawful basis recorded.
B) An entry for a personal-data dataset that records owner, contact, frequency and retention, but no lawful basis for processing.
C) An entry citing a legislative provision for its retention period.
D) An entry corrected by the owning team eight working days after notification of an inaccuracy.

**Correct answer: B**

**Explanation:** The passage requires entries for datasets containing personal data to "additionally record the lawful basis for processing"; option B omits it, so that entry breaches a mandatory requirement. Option A is compliant because the single-team condition licenses combining the roles. Option C describes exactly what the guidance requires where legislation governs retention. Option D is within the ten-working-day correction window. Application questions like this one go a step beyond comprehension: you must hold several rules in mind and test a case against each. That is precisely the skill you use when reviewing a colleague's metadata entry — or your own — before it is published.

### Preparation tips

- **Drill the three-way distinction daily.** For one week, take a paragraph from any standard, policy or email you receive at work and write one statement of each kind against it: one the text supports, one it contradicts, one it cannot settle. Five minutes a day builds the exact reflex the test measures.
- **Hunt qualifier words.** "Must" versus "should", "alone", "in addition", "before", "may", "proposed", "seems", "followed". Circle them mentally as you read; they decide most answers.
- **Use only the passage.** You know a great deal about data platforms — set it aside. If the passage doesn't say it, you cannot use it, even if you are certain it is true in your department.
- **Read the statement before re-reading the passage.** Skim the passage once for structure, read the statement carefully, then return to the relevant sentence and read *that* closely. This is faster than mastering the whole passage up front, and mirrors how you check a clause in a standard at work.
- **Watch for tense and status.** Actions in reports are done, in progress, proposed, or considered — four different things. Match the statement's claimed status to the passage's verb.
- **Keep calm about Cannot Say.** Candidates under-use it because it feels like giving up. It is not — it is the correct professional answer whenever the text is silent, and roughly a third of well-built questions land there.
- **Practise on the documents your role actually produces.** Take one of your own metadata entries or documentation pages and read it as a hostile examiner would: which sentences state facts, which state intentions, and which could a reader legitimately answer "Cannot Say" about? This sharpens both your test performance and the documentation itself — ambiguity you find in practice is ambiguity your users would have hit in production.

### Common pitfalls

- **Bringing in outside knowledge.** The most common error for experienced professionals: you know how extracts, screenings, or sign-offs usually work, and you answer from experience rather than the text. The test deliberately punishes this.
- **Confusing sequence with causation.** "The delay followed the change" is not "the change caused the delay". Incident reports are written carefully; read them carefully.
- **Treating hedged claims as firm ones.** "Seems to", "I think", "might" mark hypotheses. A statement that upgrades them to fact is False (or Cannot Say), not True.
- **Welding a date to the wrong request.** When one message contains multiple asks and one deadline, check which ask the deadline governs.
- **Answering the passage's topic instead of the statement.** Each statement is a precise claim; a statement can be False even when it is "about the right thing".
- **Poor time allocation.** Scanning for the relevant sentence beats re-reading the entire passage for every question; with under a minute per item, reading strategy is part of the skill.

## Workplace job-specific situational judgement assessment

### About this assessment

A situational judgement assessment evaluates your decision-making, interpersonal skills, and professional conduct. Instead of testing what you can calculate or deduce, it presents short, realistic workplace dilemmas — conflicting priorities, awkward stakeholder conversations, ethical grey areas, operational surprises — and asks how you would respond. There is usually no single objectively right answer in the mathematical sense; rather, some responses fit the role, the organisation's values, and good professional practice better than others.

Common response formats include choosing the **most effective** and **least effective** actions from a set, or ranking or rating every option from best to worst. Timing is typically generous or untimed, because the point is your natural judgement, not your speed.

For an analytics engineer in UK government, the scenarios draw on your real working world: data users who depend on your models, subject matter experts whose knowledge you translate into data structures, trainee analytics engineers you support, senior analytics engineers who assign and review your work, and multidisciplinary teams with potentially difficult dynamics. Strong answers consistently reflect UK public sector values: meeting user needs, transparency and honesty (including about your own mistakes), collaboration across disciplines, accessibility and inclusion, and care with public data and public money.

A helpful framing: effective responses usually (1) address the immediate need, (2) are honest and proportionate, (3) keep the right people informed at the right level, and (4) fix causes as well as symptoms. Ineffective responses usually delay action, hide problems, bypass agreed ways of working, or treat people — users, trainees, experts — as obstacles.

### What it measures for your role

- **Communicating between the technical and non-technical**: several scenarios test how you handle stakeholders with different perspectives, host difficult discussions in a multidisciplinary team, and advocate for your team externally without becoming defensive.
- **Problem management**: dilemmas about incidents and recurring defects test whether you can judge a problem's level — operational, tactical, strategic — and act proportionately, contributing to remedies and preventative measures.
- **Data quality improvement and testing**: scenarios probe what you do when you find (or cause) a data quality problem, especially under deadline pressure — the moments when honesty and process discipline are tested.
- **Supporting users and trainees**: your role level explicitly includes providing training and support for users of data sets and supporting trainee analytics engineers; scenarios test patience, clarity and follow-through.
- **Working with senior colleagues**: as an analytics engineer you develop models assigned by more senior engineers and work with experienced colleagues to develop your skills; scenarios test when to act independently, when to consult, and how to disagree constructively.

### Practice questions

For each scenario, choose the **most effective** and **least effective** responses, then compare with the suggested answers and reasoning.

**Question 1 (moderate) — The dashboard is wrong on deadline day**

At 08:40 you discover that a figure in the housing performance model you built is double-counting one category of repairs. A dashboard using the model will be shown to the directorate board at 10:00 by the Head of Housing Analysis, who is not aware of the issue. Your senior analytics engineer is in a meeting until 09:30.

A) Say nothing for now; the error affects only one category, and you can fix it quietly this afternoon.
B) Immediately inform the Head of Housing Analysis and your senior engineer's team channel: explain which figure is affected, the likely direction and rough size of the error, and that you are working on the fix.
C) Rush a fix directly into production before 10:00 without testing, so the board sees correct figures.
D) Email your senior analytics engineer, wait for them to come out of their meeting at 09:30, and let them decide whether to tell anyone.

**Most effective: B. Least effective: A.**

**Explanation:** B acts on the two urgent needs — the presenter must not unknowingly show wrong figures to a board, and the team must know — while being transparent about uncertainty ("likely direction and rough size") and keeping the fix orderly. It reflects the public sector value of transparency and the practical truth that a forewarned presenter can caveat a number gracefully. A is the least effective: it knowingly lets a decision-making forum consume wrong data to protect your comfort — a direct breach of honesty and user-needs values, and the kind of silence that destroys trust when discovered. C swaps one risk for a worse one: an untested emergency change may introduce new errors minutes before a board meeting, bypassing the testing discipline your role is built on. D looks procedurally tidy but leaves the presenter uninformed during the 50 minutes that matter; escalation that arrives after the harm is not escalation. Note the general pattern: inform the affected user first, fix second, and never let hierarchy delay a time-critical warning.

**Question 2 (moderate) — The subject matter expert disagrees with your model**

You are designing a dimensional model for grant applications. A subject matter expert (SME) from the grants team insists that an application "belongs" to the caseworker who first logged it, while the data shows applications are routinely reassigned and your draft model tracks the *current* caseworker. In a design review, the SME says, with some irritation, that your model "doesn't reflect how the business works."

A) Defer entirely to the SME and change the model to record only the first caseworker.
B) Explain that the data supports your design, and that as the modelling specialist you should have the final say on structure.
C) Ask the SME to walk you through the business scenarios behind their view, then explore whether the model should capture *both* the originating and current caseworker — for example as a slowly changing relationship — and agree which reports need which.
D) Suggest the disagreement be escalated to the SME's head of profession to adjudicate.

**Most effective: C. Least effective: B.**

**Explanation:** C treats the disagreement as information: SMEs usually voice a real business need in structural terms, and "first caseworker versus current caseworker" is a classic case where the right model captures the history rather than choosing a side — exactly what your role means by working with subject matter experts to "translate organisational processes into data structures optimised for analysis". It also de-escalates a potentially difficult dynamic by giving the expert genuine attention. B is the least effective: pulling rank on specialism dismisses the expert, damages the relationship your model depends on, and — worse — may build the wrong model, since the data showing reassignments does not tell you which caseworker matters for the business questions. A capitulates without understanding, likely breaking current-workload reporting. D escalates prematurely: adjudication before exploration wastes senior time and signals you cannot host a difficult discussion — a skill explicitly in your profile. Collaboration first, structure second, escalation last.

**Question 3 (easy) — The trainee's repeated question**

A trainee analytics engineer asks you, for the third time in two weeks, how to tell whether a field belongs in a dimension or a fact table. You are busy preparing a data model for review tomorrow.

A) Tell them you are busy and to search the team wiki.
B) Give a quick answer now, and offer a short session later this week where you work through examples from the model you are currently building — then add the examples to the team's documentation so the next trainee benefits too.
C) Answer the question fully now, setting aside your review preparation for the afternoon.
D) Suggest they hold all their questions for the senior analytics engineer's weekly clinic.

**Most effective: B. Least effective: A.**

**Explanation:** B balances your genuine deadline with your explicit role-level duty to support trainee analytics engineers: an immediate short answer unblocks them, a scheduled worked-examples session addresses the *pattern* (a third repetition signals the concept has not landed, and concrete examples are how modelling concepts land), and capturing it in documentation converts a repeated interruption into a durable asset — a small preventative remedy, in problem management terms. A is least effective: it dismisses a junior colleague who has plainly already struggled, harms their confidence to ask again, and ignores that the wiki has evidently not answered this for them. C is generous but disproportionate — sacrificing tomorrow's review commitment when a brief answer plus a scheduled session serves everyone. D outsources your own responsibility and delays the trainee for days. Inclusion means junior colleagues can ask without being made to feel a burden.

**Question 4 (hard) — Pressure to skip testing**

A policy team urgently needs a new field added to your caseload model for a parliamentary question due tomorrow. Your team's standard requires model changes to pass the test suite and a peer review before production release. The policy lead asks you to "just add the field tonight — it's one line."

A) Refuse, explaining that the standard allows no exceptions, and tell them the field will arrive next week after the full process.
B) Add the field tonight directly in production, skipping tests and review, because parliamentary business overrides internal process.
C) Explain the risk, then run the change through the test suite tonight and ask a colleague or your senior engineer for an expedited peer review first thing tomorrow — while also offering the policy team a manually verified one-off extract this evening in case the full change cannot land in time.
D) Add the field tonight without review, but quietly run the tests afterwards and fix anything that breaks before anyone notices.

**Most effective: C. Least effective: D.**

**Explanation:** C serves the real user need (a parliamentary deadline is a genuine priority in government) without abandoning the controls that protect data quality: tests run tonight, review compressed but not skipped, and a manually verified extract as a safety valve that meets tomorrow's need even if the production change slips. This is what proportionate flexibility looks like — the process bends, the safeguards hold. D is the least effective and worth dwelling on: it carries all of B's risk *plus* concealment — "fix anything before anyone notices" means knowingly hiding an untested production change, corroding the transparency your role depends on. B at least acts openly but wrongly treats urgency as a licence to bypass safeguards; an error in a parliamentary answer is far more damaging than a slightly later field. A hides behind process without engaging with the need — "no exceptions, next week" fails the user when legitimate expedited options exist. Strong situational judgement finds the route that honours both the deadline and the discipline.

**Question 5 (moderate) — The recurring incident**

For the fourth month running, the monthly benefits extract arrives with a changed column layout, breaking your staging load. Each time, a team member has manually adjusted the load and moved on. It has just happened again, and you are on support duty.

A) Adjust the load manually as before, since the fix is known and quick.
B) Adjust the load to restore service, then log the recurrence formally, analyse the pattern (what changes, when, why), and propose a preventative remedy to your senior engineer — such as a layout-validation check that fails fast with a clear message, and a conversation with the supplying team about change notice.
C) Leave the load broken and email the supplying team that no data will be processed until they stabilise the layout.
D) Adjust the load, and add a note to the team wiki describing how to do the manual fix faster next time.

**Most effective: B. Least effective: C.**

**Explanation:** B is textbook problem management at your level: restore the operational service first (users need this month's data), then treat four recurrences as what they are — a tactical problem with a pattern — and contribute a preventative remedy through your senior engineer, addressing both the technical symptom (validation that fails fast) and the root cause (the supplier's unannounced changes). C is least effective: it holds users' data hostage to an inter-team dispute, punishing the people who depend on the extract for something they did not cause — the opposite of user-focused service. A keeps the team on a treadmill; a known quick fix repeated monthly is not a fix but a recurring cost and risk. D is better than A — documenting the workaround has value — but it optimises the symptom rather than preventing it, institutionalising the problem. The discriminating insight: "restore, then prevent" beats "restore and forget", "document the workaround", and "refuse to restore".

**Question 6 (hard) — Credit and visibility**

In a cross-government show-and-tell, a senior manager from another team praises the new data documentation portal and attributes it to their own team. In fact, your team — and particularly a quiet colleague of yours — designed the documentation standard behind it. You are attending; your senior analytics engineer is not.

A) Interrupt the senior manager to correct the record in front of the audience.
B) Say nothing; visibility politics are not your concern, and the work speaks for itself.
C) In the discussion afterwards, add a constructive comment along the lines of: "Really glad the portal is landing well — the documentation standard behind it was designed by our team, and my colleague led that piece; happy to connect anyone who wants to build on it." Then let your senior engineer know what happened.
D) Complain about the senior manager in your team channel after the meeting.

**Most effective: C. Least effective: D.**

**Explanation:** Your skill profile includes being "an advocate for the team externally", and C does precisely that: it corrects the record factually and warmly, credits the specific colleague (who, being quiet, is least likely to claim credit themselves — an inclusion point), offers collaboration rather than grievance, and keeps your senior engineer informed. A pursues a fair goal in a damaging way: a public interruption embarrasses a senior colleague, creates the "difficult dynamics" your role asks you to manage rather than cause, and makes your team look territorial. B abandons your colleague's recognition and your team's standing; unattributed work does *not* reliably speak for itself, and quiet contributors are the first to lose out when others stay silent. D is least effective: venting in a channel corrects nothing externally, spreads negativity internally, and creates a written record of grievance instead of a professional remedy. Advocacy is done in the room, constructively — not over the manager's head, and not behind their back.

**Question 7 (moderate) — The tempting shortcut on data quality**

While preparing training data for a user session tomorrow, you notice that around 2% of records in the live model have malformed National Insurance number formats — an issue nobody has reported. Fixing it properly requires source analysis; you could also just exclude those rows from your training materials so the session looks clean.

A) Exclude the rows from the training materials and mention nothing; the session is about how to use the model, not its flaws.
B) Postpone tomorrow's training until the data is fixed.
C) Keep the session as planned, but include the finding honestly — show users how to recognise the malformed records and what to do about them — and separately log the issue with details for proper investigation and support of a fix.
D) Spend tonight attempting your own fix in the live model so the data is clean by morning.

**Most effective: C. Least effective: A.**

**Explanation:** C turns a flaw into good training and good process. Users of data sets are better served by honest material — real data has quality issues, and "how to recognise and handle them" is among the most useful things you can teach. Logging the issue with your profiling details feeds the data quality improvement duty in your role, routed properly rather than heroically. A is least effective because it curates reality: users will meet these records in the live model the day after training, unequipped, and will rightly wonder why the training hid them; concealing a newly discovered quality issue also means nobody investigates it. B overreacts — a 2% format issue does not invalidate training on an otherwise working model, and postponement fails scheduled users for little gain. D is well-meant but risky: unreviewed overnight changes to a live model, made unassigned and untested, violate the working practices of your role level, where model changes flow through senior assignment and testing. Honesty plus proper routing beats both concealment and heroics.

**Question 8 (moderate) — Conflicting instructions**

Your senior analytics engineer asked you to spend this week building a new dimension for the claims model. Mid-week, a different senior colleague from the analysis team asks you to drop that and build them a set of one-off extracts, saying their work is "higher priority for the directorate."

A) Continue with the dimension work and do not mention the request, since your assignment came first.
B) Switch immediately to the extracts, since the analysis colleague sounds senior and urgent.
C) Tell the analysis colleague you cannot help and that they should raise a formal request through the intake process.
D) Explain your current assignment, then promptly connect the two seniors (or raise it with your senior engineer) so the priority call is made by those who own it — offering what you can see of the trade-off, such as the dimension slipping by two days.

**Most effective: D. Least effective: B.**

**Explanation:** D recognises the real issue: this is a prioritisation conflict between two owners, and at your role level — where work is assigned by more senior analytics engineers — the call belongs to them, not to whoever asked last or loudest. Supplying the trade-off information ("the dimension would slip by two days") is your distinctive contribution: you are closest to the facts. B is least effective: silently switching means your actual assignment slips without its owner's knowledge, breaking the trust your assignment model relies on, and it rewards pressure over process — next time everyone will push directly. A is the mirror error: ignoring a possibly genuine directorate priority and hiding the request denies your senior engineer the chance to make an informed call. C is not unreasonable in bureaucratic form but is cold in substance: process signposting without engagement fails a colleague who may have a legitimate urgent need; D achieves the same governance with collaboration intact. When two instructions collide, surface the collision — don't privately resolve it.

**Question 9 (hard) — The accessibility objection**

You demonstrate a new data model's documentation site to users. Afterwards, a user with a visual impairment tells you privately that the entity-relationship diagrams — the core of the documentation — are unreadable with a screen reader, and the colour-coding of fact versus dimension tables is indistinguishable to them.

A) Thank them, explain that diagrams are inherently visual, and suggest they ask a colleague to talk them through the diagrams when needed.
B) Thank them, treat it as a defect in the documentation standard rather than a personal accommodation: add structured text equivalents (each table's grain, keys and relationships in list form) alongside every diagram, fix the colour-coding with patterns or labels, propose these as requirements in the team's documentation standard, and follow up with the user to confirm the changes work for them.
C) Apologise and offer to produce a special separate document just for them whenever they need one.
D) Note it in the backlog as a low-priority enhancement, since only one user has raised it.

**Most effective: B. Least effective: A.**

**Explanation:** B does three things strong answers to accessibility scenarios always do. It fixes the artefact, not the person — text equivalents of a data model (grain, keys, relationships) are fully expressible in accessible form, so "diagrams are inherently visual" (option A) is simply false for this content, which is why A is least effective: it converts a fixable defect into a permanent dependency on colleagues' goodwill, excluding the user from independent work. B also fixes the *standard*, not just the instance — your role explicitly includes creating and maintaining data documentation and developing standards, so embedding accessibility requirements prevents every future recurrence; that is problem management thinking applied to inclusion. And it closes the loop with the user who raised it, which both verifies the fix and signals that raising issues is welcomed. C is kindly meant but creates a segregated, always-stale parallel document — accommodation, not accessibility. D misjudges severity: in UK government, accessibility is a legal and values-based obligation, not a feature request whose priority scales with the number of complainants. One report means every affected user you haven't heard from is silently excluded.

**Question 10 (moderate) — The innovation suggestion**

You have been experimenting, in your own development area, with an open-source data transformation tool that could automate much of your team's hand-written documentation and lineage tracking. Your team's current toolset does not include it, and adopting it would affect everyone's workflow.

A) Start building your assigned production models with the new tool so its benefits become undeniable.
B) Keep it to yourself until you are more senior; tool choices are not made at your level.
C) Prepare a short demonstration using a realistic but non-production example — showing concretely what it would automate, what it would change, and what risks or costs you can see — and share it with your senior analytics engineers as a proposal to evaluate.
D) Circulate an email to the whole multidisciplinary team recommending everyone switch to the tool.

**Most effective: C. Least effective: A.**

**Explanation:** Your skill profile asks you to "show an awareness of opportunities for innovation with new tools and uses of data" — awareness and advocacy, exercised through the right channel. C does this well: a concrete demonstration on non-production data is evidence, not opinion; naming the risks and costs yourself shows judgement and makes evaluation easy; and routing it to senior engineers respects that adoption decisions affecting everyone's workflow are theirs to make. A is least effective: unilaterally introducing an unapproved tool into production models creates unmanaged risk (support, security review, maintainability, key-person dependency) and presents colleagues with a fait accompli — innovation by ambush, which typically kills both the idea and trust. B wastes a genuinely valuable idea and misreads the role: suggesting is precisely at your level, deciding is not. D bypasses your own team's owners, asks non-technical colleagues to adjudicate a technical choice, and creates noise a demonstration would have converted into signal. Good innovation practice at your level: experiment safely, demonstrate honestly, propose through those accountable.

### Preparation tips

- **Anchor on the values, not the vibe.** Before an assessment, write down the handful of values these scenarios reward — user needs first, honesty especially about your own errors, restore service then prevent recurrence, respect for both expertise and process, inclusion by default — and test each option against them. Options that "feel strong" often fail the honesty or proportionality test.
- **Look for the option that does two things.** The most effective answer usually pairs an immediate action with a systemic one: inform *and* fix, restore *and* prevent, answer *and* document. Single-action options are usually incomplete.
- **Read the role level into the scenario.** At your level, models are assigned by senior engineers, and remedies are contributed to rather than imposed. Options where you unilaterally redesign systems, adjudicate priorities, or change production without review are usually wrong — not because initiative is bad, but because judgement includes knowing the channel.
- **Least effective deserves as much care as most effective.** The least effective option is typically the one that conceals, delays while harm accrues, or punishes the wrong people — not merely the least impressive one.
- **Rehearse with real memories.** For each skill in your profile, recall one real situation you handled — a difficult stakeholder, a found defect, a struggling trainee — and ask what the strongest version of your response would have been. Assessments sample judgement; reflection is how judgement improves.

### Common pitfalls

- **Answering idealistically rather than practically.** "Postpone everything until it's perfect" sounds principled but fails users with real deadlines; the effective option usually serves the need *and* keeps safeguards.
- **Selecting passive options.** Waiting for a meeting to end, filing a ticket while a presenter walks unwarned into a board room, or leaving problems for someone senior — options that delay action or pass the problem along are consistently rated weak.
- **Confusing escalation with abdication.** Escalating a genuine priority conflict is strong; escalating a design disagreement you haven't yet explored is weak. The difference is whether you have done your part first.
- **Protecting yourself instead of the user.** Options built around not being blamed — silence, quiet fixes, "before anyone notices" — are reliably among the least effective, whatever their surface efficiency.
- **Ignoring the organisation's culture.** UK public sector scenarios reward collaboration, transparency, accessibility and care with public data. An option that might pass as decisive in a sales culture ("just ship it tonight") reads as reckless here.
- **Over-punishing other people's mistakes.** Options that hold users hostage to inter-team disputes, or publicly embarrass a colleague to correct a record, mistake retaliation for accountability.

## Conclusion

Well done — you have worked through a substantial set of practice material covering all four assessment types you are likely to meet as an analytics engineer: cognitive ability, numeric reasoning, verbal reasoning, and situational judgement.

Along the way, you have practised the thinking that defines your role. You traced dependencies and spotted step changes in quality metrics. You calculated null rates, weighted quality scores, batch windows and documentation estimates — and saw how most numeric errors come from the denominator, the complement, or a skipped intermediate step. You read standards, emails and incident reports with the precision that separates "proposed" from "implemented" and sequence from causation. And you weighed realistic dilemmas about honesty under deadline pressure, supporting trainees, disagreeing with experts, and making documentation accessible to everyone.

Three suggestions for what to do next. First, revisit: return to the questions you found hardest in a few days and try them cold; the second attempt is where the learning consolidates. Second, transfer: bring these habits into your daily work — profile with explicit denominators, read standards for their qualifier words, and when incidents recur, reach for the preventative remedy. Your everyday work is the best assessment preparation there is, and the preparation makes your everyday work better. Third, share: if you support trainee analytics engineers or train users of your data sets, work through a few of these questions with them — explaining reasoning to someone else is the fastest way to deepen your own.

Remember that psychometric assessments are a snapshot, not a verdict. They measure skills that grow with practice, and you have just practised them deliberately. Approach any real assessment rested, unhurried, and confident that the reasoning it samples is reasoning you use every working day.

Keep learning, keep asking good questions of your data and your colleagues, and good luck — you are better prepared than you think.
