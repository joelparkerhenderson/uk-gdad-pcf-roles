# Analytics Engineer (Senior Analytics Engineer) - Psychometric Assessment Resources

## Introduction

Welcome. This document is a practical, role-specific preparation resource for psychometric assessments, written for you as a senior analytics engineer working within the UK Government Digital and Data (GDAD) profession. Whether you are preparing for an internal promotion board, a move to another department, a formal development review, or simply want to sharpen the mental toolkit you use every day, this guide is designed to help you practise, reflect, and improve with confidence.

Psychometric assessments are structured, standardised exercises that measure the underlying capabilities a role demands: how you process information, how you reason with numbers, how precisely you read and interpret written material, and how you judge complex workplace situations. Employers use them because they are objective and evidence-based, and because — when they are well designed — they mirror the genuine demands of the job. For a senior analytics engineer, those demands are distinctive. You oversee the development and testing of data models, direct and mentor other analytics engineers, translate organisational processes into structures optimised for analysis, ensure data quality and documentation standards are met, and communicate fluently between technical and non-technical stakeholders. The assessments in this guide are built around exactly those responsibilities.

This document is organised into four main assessment sections, each of roughly equal depth:

1. **Workplace job-specific cognitive assessment** — pattern recognition, logical deduction, error checking, and prioritisation using the artefacts you really handle: dimensional models, transformation pipelines, metadata repositories, and test results.
2. **Workplace job-specific numeric reasoning assessment** — interpretation of tables, percentages, ratios, capacity figures, and performance metrics drawn from data platform operations and team delivery.
3. **Workplace job-specific verbal reasoning assessment** — dense passages in the style of data standards, policies, stakeholder emails, and governance reports, followed by True / False / Cannot Say and comprehension questions.
4. **Workplace job-specific situational judgement assessment** — realistic dilemmas involving your stakeholders: less senior engineers you coach, subject matter experts, data users, governance boards, and multidisciplinary teams with sometimes difficult dynamics.

Each section explains what the assessment measures and why it matters for your role, maps its dimensions to the specific GDAD skills in your role profile, provides substantial worked practice questions at varied difficulty levels, and closes with preparation tips and common pitfalls.

How should you use it? Work through the practice questions under gentle time pressure first, then study the worked explanations carefully — the reasoning matters more than the answer. Use the self-reflection prompts in the situational judgement section to think honestly about your leadership habits. Revisit sections periodically; spaced practice is far more effective than a single cramming session. Above all, treat this as a development aid, not a verdict. You already operate at a senior level — this guide simply helps you demonstrate it under assessment conditions.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive ability assessment is a targeted psychometric test that measures the exact mental processes your role demands, using practical workplace scenarios rather than abstract puzzles. Unlike a generic IQ test, every question mimics the everyday tasks and data formats of the actual job — in your case, dimensional models, transformation dependency chains, data quality reports, metadata schemas, and test specifications. Assessments of this kind are usually delivered online in a timed format, typically 15 to 30 minutes, with objective scoring against a benchmark or norm group. Modern platforms may adapt question difficulty to your answers, and employers often receive a breakdown of speed versus accuracy rather than a single score.

For a senior analytics engineer, cognitive ability is not an academic nicety: it is the daily substance of the job. When you review a complex data model built by a less senior engineer, you are performing error checking and logical deduction. When you trace why a fact table's row count doubled overnight, you are diagnosing faults in a dependency graph. When you decide which of five competing requests to schedule first, you are prioritising under constraint. When you spot that a slowly changing dimension has been implemented as Type 1 where the requirement was Type 2, you are recognising a pattern deviation. This assessment measures how quickly and accurately you do all of that under time pressure.

### What it measures for your role

The cognitive dimensions map directly onto the GDAD skills in your role profile:

- **Data modelling, cleansing and enrichment** — building and reviewing complex data models against standards requires pattern recognition (spotting where a model deviates from Kimball or Inmon conventions), logical deduction (inferring the downstream effect of a grain change), and error checking (catching key violations, orphaned records, and broken conformance).
- **Testing** — reviewing requirements and defining test conditions is applied logic: deriving the complete set of conditions from a specification, and identifying issues and risks that the specification implies but does not state.
- **Problem management** — initiating and monitoring investigations into patterns and trends is fault diagnosis at scale: isolating the true cause among correlated symptoms, and determining preventative measures.
- **Programming and build (data engineering)** — designing, coding, testing and correcting moderate-to-complex scripts demands sequential logic and precise attention to transformation order.
- **Metadata management** — designing a metadata repository requires classification logic: recognising which attributes belong at which level of a hierarchy.
- **Data analysis and synthesis** — data profiling and source system analysis is systematic hypothesis testing against evidence.

As a senior, you are also assessed on prioritisation and oversight: not just solving the puzzle yourself, but judging which puzzle your team should solve first.

### Practice questions

**Question 1 (easy) — Pattern recognition in a naming standard.**
Your team's transformation standard requires staging models to be named `stg_<source>__<entity>`, intermediate models `int_<entity>__<verb>`, and mart models `fct_` or `dim_` prefixed. A less senior engineer submits a pull request containing these five models: `stg_hmrc__payments`, `int_payments__deduplicated`, `dim_customer`, `stg_payments`, `fct_payment_events`. Which model name violates the standard?

A) `stg_hmrc__payments`  B) `int_payments__deduplicated`  C) `dim_customer`  D) `stg_payments`  E) `fct_payment_events`

**Correct answer: D.**
**Explanation:** The staging pattern requires both a source and an entity separated by a double underscore: `stg_<source>__<entity>`. `stg_payments` names only an entity, with no source system and no double underscore, so it violates the standard. All the others match their required pattern exactly. In a real review you would flag this quickly — naming standards are the cheapest form of documentation, and enforcing them is part of ensuring adherence to standards across your team's models.

**Question 2 (easy) — Logical deduction from load dependencies.**
In your nightly pipeline, model B depends on model A, model C depends on model B, and model D depends on both A and C. This morning model A completed successfully but model B failed. Which statements must be true?

1. Model C did not build successfully from fresh data.
2. Model D did not build successfully from fresh data.
3. Model A contains bad data.

A) 1 only  B) 1 and 2 only  C) 2 and 3 only  D) 1, 2 and 3

**Correct answer: B.**
**Explanation:** C depends on B, so if B failed, C cannot have built from fresh data (statement 1 true). D depends on C (as well as A), so D also cannot have built fully fresh (statement 2 true). Statement 3 does not follow: B's failure could be caused by many things — a code error in B, a resource timeout, a schema change — and A completing successfully tells you nothing about A's data quality either way. Deducing only what the evidence supports, and no more, is exactly the discipline you apply when triaging pipeline incidents before directing an engineer to investigate.

**Question 3 (moderate) — Error checking a dimensional design.**
You are reviewing a Kimball-style star schema for a grants payment service. The design document states: "The grain of `fct_grant_payment` is one row per payment transaction. Dimensions: `dim_date`, `dim_grant_scheme`, `dim_applicant`, `dim_payment_status`. The fact table stores `payment_amount`, `application_count`, and `status_description`." Which two elements are inconsistent with the stated grain and good dimensional practice?

A) `payment_amount` and `dim_date`
B) `application_count` and `status_description`
C) `dim_payment_status` and `payment_amount`
D) `dim_applicant` and `application_count`

**Correct answer: B.**
**Explanation:** If the grain is one row per payment transaction, `application_count` is not a fact at that grain — a single payment does not have a "count of applications"; that is an aggregate belonging to a different grain or a separate summary table. `status_description` is a textual descriptive attribute, which belongs in `dim_payment_status`, not in the fact table; storing free text in a fact table bloats it and breaks the dimensional pattern. `payment_amount` is a proper additive measure, and the four dimensions are all reasonable. Grain violations are among the most damaging modelling errors because every downstream analysis silently inherits them — this is why your role profile emphasises reviewing complex models for adherence to standards.

**Question 4 (moderate) — Prioritisation under constraint.**
It is Monday morning. You have four items competing for your attention:

1. A data quality alert: the overnight reconciliation shows a 0.02% variance in a low-usage reference table, within tolerance but flagged for review.
2. A less senior engineer is blocked on a model review you promised; their sprint commitment is due Wednesday.
3. A director's office asks for a briefing note on your team's metadata repository by Thursday.
4. The finance data mart failed its freshness test; a monthly report used by ministers' offices is generated from it at 14:00 today.

What is the most defensible order to address them?

A) 4, 2, 3, 1  B) 2, 4, 1, 3  C) 4, 1, 2, 3  D) 3, 4, 2, 1

**Correct answer: A.**
**Explanation:** Item 4 combines high impact (ministerial reporting), hard deadline (14:00 today), and current failure — it comes first; as the senior you would either investigate or immediately delegate with oversight. Item 2 is next: unblocking your engineer protects a Wednesday commitment and honours your coaching responsibility, and reviews are usually quick relative to their unblocking value. Item 3 has a Thursday deadline and can be scheduled. Item 1 is within tolerance on a low-usage table — legitimate to review, but last. Option C wrongly elevates a within-tolerance alert above a blocked colleague; option B delays a same-day ministerial deliverable behind a Wednesday one. Senior-level prioritisation weighs impact, deadline proximity, and the multiplier effect of unblocking others.

**Question 5 (moderate) — Deduction from data profiling evidence.**
You profile a source system's `customer` table before modelling it. You find: 1,200,000 rows; `customer_id` has 1,200,000 distinct values; `national_insurance_no` has 1,140,000 distinct values and 45,000 nulls; `email` has 990,000 distinct values and no nulls. Which conclusion is safe?

A) `customer_id` is a reliable unique key for this table.
B) 45,000 customers share a national insurance number.
C) `email` uniquely identifies a customer.
D) The table contains 60,000 duplicate customer records.

**Correct answer: A.**
**Explanation:** Distinct count equals row count for `customer_id`, so within this extract it is unique — a safe (if provisional) conclusion, and exactly what you need for a surrogate key mapping. Option B miscounts: 1,200,000 minus 45,000 nulls leaves 1,155,000 populated values with 1,140,000 distinct, meaning at most 15,000 values are shared — and nulls are absences, not shared numbers. Option C is false: 990,000 distinct emails across 1,200,000 rows means substantial reuse (families, shared inboxes, placeholder addresses). Option D confuses non-unique attributes with duplicate records; duplication of an email does not make the whole record a duplicate. Careful profiling arithmetic prevents you baking a false uniqueness assumption into a model — one of the most expensive classes of modelling error to unwind.

**Question 6 (moderate) — Sequence logic in a transformation pipeline.**
A transformation script must perform these steps: (i) deduplicate source rows, (ii) apply currency conversion using a daily rates table, (iii) filter out test transactions, (iv) join to the conformed customer dimension, (v) aggregate to daily totals. The rates table joins on transaction date; test transactions are identified by a flag on the raw row; the customer dimension join requires the deduplicated natural key. Which ordering principle is most important for correctness?

A) Aggregation (v) must precede the dimension join (iv) to reduce data volume.
B) Filtering test transactions (iii) must occur before aggregation (v), and deduplication (i) before the dimension join (iv).
C) Currency conversion (ii) must be the final step so rates reflect the latest values.
D) The dimension join (iv) must precede deduplication (i) to enrich all rows.

**Correct answer: B.**
**Explanation:** Two hard constraints exist. Test transactions must be removed before aggregation, otherwise they contaminate the daily totals irrecoverably. Deduplication must precede the customer join because the join requires the deduplicated natural key — joining first would multiply duplicates through the enrichment. Option A is backwards: aggregating before joining the dimension would lose the ability to group by customer attributes (and is an optimisation question, not a correctness one). Option C is wrong because conversion must use the rate for the transaction date, not the latest rate. Option D violates the stated key constraint. Reasoning about operation order is the core of reviewing "moderate-to-complex programs and scripts from agreed specifications", as your programming and build skill requires.

**Question 7 (hard) — Fault isolation among correlated symptoms.**
At 09:10 you receive three alerts: (1) the `fct_case_events` build ran 4x longer than usual; (2) the duplicate-key test on `dim_caseworker` failed; (3) dashboard users report case counts roughly doubled. The overnight release notes show two changes: the caseworker HR feed migrated to a new extract, and a new index was added to the events staging table. What is the most probable single root cause, and the correct first verification?

A) The new index corrupted the events table; rebuild the index and re-run.
B) The HR feed migration introduced duplicate caseworker rows; verify by counting rows per natural key in the new extract.
C) Dashboard caching is stale; purge the cache and ask users to refresh.
D) Two independent faults occurred; investigate both changes in parallel with equal priority.

**Correct answer: B.**
**Explanation:** Work the dependency logic: duplicate rows in `dim_caseworker` would fan out every join from the fact table, roughly doubling case counts (symptom 3) and inflating the join workload, slowing the build (symptom 1). One cause explains all three symptoms, and it aligns with exactly one of the two changes — the migrated HR extract. The index change could plausibly slow a build but cannot double counts or create duplicate keys. Option C treats a downstream symptom as a cause. Option D abandons parsimony: when one hypothesis explains every symptom and maps to a known change, you verify it first — cheaply, by profiling the new extract for key duplication — before spending team effort elsewhere. This is the "investigate patterns and trends to resolve problems" discipline of your problem management skill, plus the preventative follow-up: add a duplicate test on the extract itself, not just the dimension.

**Question 8 (hard) — Test condition derivation.**
A specification states: "The model shall assign each application to exactly one processing band. Band A: value under £10,000. Band B: £10,000 to £50,000 inclusive. Band C: over £50,000. Applications with a null value shall be routed to a review queue and excluded from banding." Which set of test conditions provides the strongest minimal coverage?

A) Values £5,000, £30,000, £70,000.
B) Values £9,999.99, £10,000, £50,000, £50,000.01, null, and a check that no application appears in more than one band.
C) Values £10,000 and £50,000 only, since boundaries are where errors occur.
D) One null value and one non-null value.

**Correct answer: B.**
**Explanation:** Strong test design targets boundaries, the null path, and the exclusivity invariant. £9,999.99 and £10,000 exercise the A/B boundary; £50,000 and £50,000.01 exercise the B/C boundary (checking "inclusive" is honoured on both ends of Band B); null exercises the review-queue routing; and the mutual-exclusivity check verifies "exactly one band" — an invariant that per-value tests alone cannot confirm. Option A tests only mid-band happy paths. Option C tests boundaries but from one side only and ignores null and exclusivity. Option D ignores boundaries entirely. Deriving complete conditions from a specification — including the implied invariants — is precisely the "review requirements and specifications, and define test conditions" behaviour in your testing skill.

**Question 9 (hard) — Metadata classification logic.**
You are designing a metadata repository. You must classify these six items into the correct layer: business metadata (meaning and context), technical metadata (structure and lineage), or operational metadata (runtime behaviour). Items: (1) "Case value means the total awarded amount in GBP, excluding VAT"; (2) column data type `DECIMAL(12,2)`; (3) last successful load timestamp; (4) upstream-to-downstream lineage graph; (5) data owner: Head of Casework Operations; (6) average nightly build duration.

A) Business: 1, 5. Technical: 2, 4. Operational: 3, 6.
B) Business: 1, 4. Technical: 2, 5. Operational: 3, 6.
C) Business: 1, 5, 6. Technical: 2, 4. Operational: 3.
D) Business: 1. Technical: 2, 3, 4. Operational: 5, 6.

**Correct answer: A.**
**Explanation:** Definitions and ownership describe meaning and accountability — business metadata (items 1 and 5). Data types and lineage describe structure and derivation — technical metadata (items 2 and 4). Load timestamps and build durations describe how the system behaves at runtime — operational metadata (items 3 and 6). Option B misplaces lineage as business and ownership as technical; option C treats build duration as business context; option D confuses runtime facts with structural ones. Getting this taxonomy right matters because your role profile asks you to design an appropriate metadata repository and advise less experienced team members about metadata management — a muddled classification produces a repository nobody can navigate.

**Question 10 (hard) — Deductive reasoning about slowly changing dimensions.**
A requirement states: "Analysts must be able to report each case against the team that owned it at the time the case event occurred, and also against the team that owns the caseworker today." The current `dim_caseworker` is Type 1 (overwrite on change). What is the minimal correct change?

A) No change — Type 1 already supports both views.
B) Convert to Type 2 (row versioning with effective dates); join facts to the version current at event time for historical reporting, and expose a "current team" attribute for the as-of-today view.
C) Convert to Type 2 and drop the current-team view, as Type 2 cannot show current values.
D) Keep Type 1 and add a snapshot of the fact table taken daily.

**Correct answer: B.**
**Explanation:** The requirement demands both historical accuracy ("team at event time") and current-state reporting ("team today"). Type 1 destroys history on overwrite, so it cannot satisfy the first need — option A fails. Type 2 preserves each version with effective dates, satisfying historical reporting; adding a current-flag or a Type 1-style "current team" attribute on every row (a common Type 2/Type 6 hybrid) satisfies the second — so option C's claim is false. Option D is disproportionate and still loses the caseworker history embedded in the dimension. Recognising which SCD pattern a requirement implies, and challenging a design that cannot meet it, is core to overseeing model development and directing the work of other analytics engineers.

**Question 11 (moderate) — Error checking a data quality report.**
A weekly data quality summary produced by a junior colleague reads: "Completeness of `postcode` improved from 91.0% to 94.5%, an improvement of 3.5%. Uniqueness violations fell from 1,200 to 300, a fall of 300%. Overall, 5 of our 40 quality rules failed, meaning 92.5% passed." Which statements contain an error?

A) The completeness statement only
B) The uniqueness statement only
C) The uniqueness and pass-rate statements
D) All three statements

**Correct answer: C.**
**Explanation:** Check each number rather than skimming. The completeness claim is defensible: 94.5 minus 91.0 is a 3.5 percentage point improvement, and describing it as "an improvement of 3.5%" is the conventional shorthand — a precise writer would say "percentage points", but the arithmetic is right. The uniqueness claim is arithmetically impossible: nothing can fall by more than 100% and remain positive; a drop from 1,200 to 300 is a 75% fall, not 300%. The pass-rate claim also fails verification: 5 failures out of 40 rules means 35 passed, and 35/40 is 87.5%, not the stated 92.5% (which would require only 3 failures). Two genuine errors, so answer C. This question deliberately models the review experience: a plausible-looking report where independently recomputing each figure is the only safe approach. Ensuring documentation and reporting meet standards — one of your explicit senior responsibilities — means never letting "looks roughly right" substitute for arithmetic.

**Question 12 (hard) — Prioritising a team's review queue.**
Three pull requests await your review. PR-1: a one-line fix to a broken test blocking the whole team's merges, submitted by your most experienced engineer. PR-2: a 900-line new data mart from a junior engineer, their first major piece of work, due for a stakeholder demo in three days. PR-3: a refactor of the metadata loading script, no deadline, submitted a week ago and now growing stale. You have 90 minutes before back-to-back meetings. What is the most effective use of the time?

A) Review PR-2 thoroughly; it is the largest and the deadline is nearest.
B) Approve PR-1 in minutes to unblock everyone, then begin a first-pass review of PR-2 with written structural feedback the junior can act on today, and message the PR-3 author with a committed review slot tomorrow.
C) Review them strictly in age order: PR-3, then PR-1, then PR-2.
D) Delegate PR-2's review to the experienced engineer and spend the 90 minutes on PR-3.

**Correct answer: B.**
**Explanation:** PR-1 is minutes of effort with team-wide unblocking value — the highest return per minute available, so it goes first. PR-2 cannot be fully reviewed in the remaining time, but an early structural pass (grain, naming, test coverage) gives the junior engineer actionable feedback while there are still three days to respond — waiting until you have time for a "complete" review would compress their rework window to nothing. PR-3 needs a commitment, not silence: telling the author exactly when it will be reviewed maintains trust and stops the staleness compounding. Option A sacrifices the team-wide blocker; option C is process for its own sake; option D is a reasonable delegation instinct applied to the wrong PR — coaching a junior through their first major mart is senior-engineer work you should stay close to, though pairing the experienced engineer into the review alongside you would be a fine complement. This is the oversight dimension of your role: sequencing your attention for maximum team effect.

**Question 13 (moderate) — Pattern recognition in trend data.**
The nightly pipeline's total runtime over ten nights (minutes): 42, 43, 41, 44, 43, 58, 44, 43, 71, 43. Failures logged: none. The two slow nights were a Sunday and the following Sunday. Which hypothesis best fits the pattern and deserves first investigation?

A) The warehouse is undersized and runtimes are steadily degrading.
B) A weekly job — such as a full-refresh or a large weekly source extract — contends with the pipeline on Sundays, and its impact is growing.
C) The two slow nights are random noise and require no action.
D) The pipeline code was changed on both Sundays.

**Correct answer: B.**
**Explanation:** The baseline is stable (41-44 minutes) with no trend, ruling out option A's steady degradation. The anomalies recur on a weekly cadence — the signature of a scheduled weekly interaction, not noise; and the second spike (71) exceeding the first (58) suggests the contending workload is growing, which strengthens rather than weakens the case for investigating now, before a Sunday run breaches its delivery window. Option D is testable but less likely: releases on two consecutive Sundays that each slow the run yet leave weekdays untouched would be an odd coincidence. The senior-level habit here is your problem management skill's "initiate and monitor actions to investigate patterns and trends" — acting on the pattern before it becomes an incident, and determining preventative measures such as rescheduling the weekly job or isolating its compute.

### Preparation tips

- **Practise on your own artefacts.** Before the assessment, spend time consciously reviewing a model, a test suite, and a pipeline run log, narrating your reasoning aloud. The questions will feel familiar because they are drawn from exactly this material.
- **Rehearse deduction discipline.** For each practice question, write down what the evidence proves, what it merely suggests, and what it says nothing about. Senior assessments deliberately include tempting over-inferences.
- **Time-box ruthlessly.** With 15-30 minutes for the whole test, allocate a per-question budget and move on when it is spent. A flagged-and-skipped hard question costs you one mark; a five-minute rabbit hole costs you four.
- **Warm up your prioritisation criteria.** Impact, deadline, effort, and unblocking value — having these four words ready turns prioritisation questions from intuition into method.
- **Do the ungraded practice questions.** Most platforms offer them before the timer starts; use them to settle nerves and learn the interface.
- **Trust your seniority.** You resolve issues like these weekly. The assessment adds time pressure, not new material.

### Common pitfalls

- **Answering from experience instead of the given scenario.** Your instinct might be "in my team we'd do X" — but cognitive questions are closed worlds; use only the stated facts, exactly as you would when triaging an unfamiliar system.
- **Missing scale and grain qualifiers.** Just as chart questions hide "in thousands" in a label, modelling questions hide the grain statement in one sentence. Read the setup line twice.
- **Over-calculating.** Where an estimate or an elimination settles the answer, use it; precision beyond what the options require is wasted time.
- **Time-sink questions.** The hardest deduction item may sit in the middle of the test. Skipping it and returning is a strategy, not a failure.
- **Assuming the longest, most technical option is right.** Assessment writers exploit this bias; several questions above have short correct answers.
- **Neglecting speed-accuracy balance.** Employers often see both measures. Wild guessing to finish fast is as visible as timid triple-checking.


## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment evaluates your ability to analyse, interpret, and make sound decisions using numerical data presented the way your role really presents it: tables of pipeline metrics, data quality percentages, warehouse cost figures, team capacity plans, and performance dashboards. It is business mathematics, not abstract formulae — percentages, ratios, rates, weighted averages, and cost-benefit estimation. Most assessments allow or provide an on-screen calculator, because the skill being measured is interpretation and decision-making, not mental arithmetic. Expect strict time limits, typically around a minute to ninety seconds per question, which reward quick and accurate data extraction and punish over-calculating.

For a senior analytics engineer, numeracy under pressure is a leadership tool as much as a technical one. You size warehouse costs when exploring new ways of working with data. You quantify data quality improvement so stakeholders can see progress. You estimate team capacity when overseeing tasks and committing to delivery. You interpret test pass rates and defect trends when reporting on quality. And crucially, you check other people's numbers — a junior engineer's row-count reconciliation, a vendor's performance claim, a dashboard's suspicious spike — because ensuring issues and risks are resolved starts with noticing that a figure cannot be right.

### What it measures for your role

The numeric dimensions align with your GDAD skills as follows:

- **Data analysis and synthesis** — profiling statistics (null rates, distinct counts, distribution shifts) are ratios and percentages; presenting clear insights means converting raw counts into meaningful comparisons.
- **Data modelling, cleansing and enrichment** — quality thresholds ("completeness must exceed 98%"), match rates in integration, and row-count reconciliation across model layers are all quantitative judgements.
- **Problem management** — trend analysis over time (runtimes, failure rates, incident volumes) requires computing and comparing rates of change.
- **Testing** — pass rates, coverage percentages, and defect density are the numbers by which you "analyse and report test activities and results".
- **Data innovation** — evaluating emerging tools means cost modelling: comparing licence, compute, and migration costs against quantified benefits.
- **Communicating between the technical and non-technical** — translating "0.7 percentage point improvement" into an honest, plain-English statement for stakeholders without overstating it.

As a senior you also handle team-level figures: capacity, velocity, review throughput, and training coverage for the users you support.

### Practice questions

**Question 1 (easy) — Completeness percentage.**
A source extract contains 250,000 customer records. Profiling shows 12,500 have a null postcode. What is the completeness rate for postcode?

A) 90%  B) 95%  C) 97.5%  D) 87.5%

**Correct answer: B.**
**Explanation:** Nulls as a fraction: 12,500 ÷ 250,000 = 0.05, i.e. 5% missing. Completeness = 100% − 5% = 95%. A fast route: 12,500 is 5% of 250,000 because 1% of 250,000 is 2,500 and 12,500 ÷ 2,500 = 5. In profiling work you compute this constantly; in the assessment, the trap options correspond to slips such as dividing by the wrong base or subtracting the wrong way.

**Question 2 (easy) — Row-count reconciliation.**
Your staging layer loads 1,840,000 rows. The deduplication step removes 4% of rows, and the test-transaction filter then removes 46,000 rows from what remains. How many rows should reach the mart layer?

A) 1,720,400  B) 1,766,400  C) 1,712,640  D) 1,794,000

**Correct answer: A.**
**Explanation:** Deduplication: 1,840,000 × 0.96 = 1,766,400 rows remain. Filter: 1,766,400 − 46,000 = 1,720,400. Note the order matters and the operations differ in kind: one is a percentage of the current total, the other a fixed count. Option B is the answer if you forget the filter; option D applies both as fixed counts. Reconciling expected against actual row counts through each transformation layer is one of the most reliable tests you will define, and this is its arithmetic.

**Question 3 (moderate) — Data quality improvement, percentage points versus percentages.**
Your quarterly report shows address-field accuracy rose from 88.0% to 92.4%. A stakeholder asks: "So quality improved by about 4 and a half percent?" Which statement is the most accurate correction?

A) Yes — 92.4 − 88.0 = 4.4, so quality improved 4.4%.
B) Quality improved by 4.4 percentage points, which is a 5.0% relative improvement on the previous accuracy level.
C) Quality improved by 4.4 percentage points, which is a 4.4% relative improvement.
D) The improvement cannot be quantified without the record counts.

**Correct answer: B.**
**Explanation:** The absolute change is 92.4 − 88.0 = 4.4 percentage points. The relative change is 4.4 ÷ 88.0 = 0.05 = 5.0%. These are different claims, and confusing them is one of the commonest errors in quality reporting. (An even stronger framing for stakeholders: the error rate fell from 12.0% to 7.6%, a 36.7% reduction in errors — same data, more meaningful.) Option D is a dodge: rates are comparable without counts, though counts add context. As the person who ensures documentation and reporting meet standards, and who communicates between the technical and non-technical, you are exactly the person expected to make this correction gracefully.

**Question 4 (moderate) — Warehouse cost comparison.**
You are evaluating two warehouse configurations for a new data mart. Option X: fixed cluster at £5.20 per hour, running 24 hours a day. Option Y: on-demand at £9.75 per hour, needed 11 hours per day. Over a 30-day month, what is the monthly saving of the cheaper option?

A) £529.50  B) £3,744.00  C) £3,217.50  D) £526.50

**Correct answer: D.**
**Explanation:** Option X: £5.20 × 24 × 30 = £5.20 × 720 = £3,744.00. Option Y: £9.75 × 11 × 30 = £9.75 × 330 = £3,217.50. Saving with Y: £3,744.00 − £3,217.50 = £526.50. Option A (£529.50) is a near-miss designed to catch arithmetic slips; options B and C are the raw totals rather than the difference — always re-read what the question asks for. Cost modelling like this underpins your data innovation responsibility: understanding the organisational impact of emerging tools means being able to defend figures like these to a spending review.

**Question 5 (moderate) — Team capacity for review workload.**
You oversee three analytics engineers. Each has 6 productive hours per day, 5 days per week. Next sprint (2 weeks), one engineer takes 3 days' leave and another is seconded 50% to an incident review for the whole sprint. Model reviews consume 20% of remaining team capacity. How many hours are left for development work?

A) 105.6 hours  B) 129.6 hours  C) 132.0 hours  D) 144.0 hours

**Correct answer: A.**
**Explanation:** Work stage by stage. Full capacity: 3 engineers × 6 hours × 10 working days = 180 hours. Subtract the leave: 3 days × 6 hours = 18 hours. Subtract the secondment: 50% of one engineer's 60 sprint hours = 30 hours. Remaining team capacity: 180 − 18 − 30 = 132 hours. Reviews take 20% of that: 0.20 × 132 = 26.4 hours. Development time: 132 − 26.4 = 105.6 hours. Option C is the trap for stopping one step early (forgetting the review deduction); option B applies the 20% to the wrong base (180 − 18 = 162, then subtracting 32.4 from 162); option D ignores the secondment. Multi-stage capacity sums like this are exactly what you compute when you oversee tasks and commit your team to a sprint — and the assessment lesson is to track which base each percentage applies to.

**Question 6 (moderate) — Ratio reasoning in integration match rates.**
You integrate two datasets. Automatic matching links 720,000 of 800,000 records. Of the unmatched remainder, a fuzzy-matching pass links 3 records for every 1 it leaves unmatched. How many records remain unmatched overall, and what is the final match rate?

A) 20,000 unmatched; 97.5% matched
B) 26,667 unmatched; 96.7% matched
C) 20,000 unmatched; 97.0% matched
D) 60,000 unmatched; 92.5% matched

**Correct answer: A.**
**Explanation:** Unmatched after the automatic pass: 800,000 − 720,000 = 80,000. A 3:1 linked-to-unlinked ratio means the fuzzy pass resolves 3/4 of them: 60,000 linked, 20,000 left. Final match rate: (800,000 − 20,000) ÷ 800,000 = 780,000 ÷ 800,000 = 97.5%. Ratio language ("3 for every 1") converts to fractions of the whole: 3:1 means quarters, not thirds — option B is the thirds error. Ensuring data "is interoperable with other data sets, enabling reuse" makes match-rate arithmetic a routine part of your quality reporting.

**Question 7 (hard) — Weighted average quality score.**
Your data quality dashboard scores four datasets: Payments 96% (2.4 million rows), Customers 91% (600,000 rows), Reference 99% (50,000 rows), Cases 84% (950,000 rows). A stakeholder wants one headline figure weighted by row count. What is it, to one decimal place?

A) 92.4%  B) 92.9%  C) 93.4%  D) 91.6%

**Correct answer: A.**
**Explanation:** Multiply each score by its row count, sum, and divide by total rows. Weighted sum: (0.96 × 2,400,000) + (0.91 × 600,000) + (0.99 × 50,000) + (0.84 × 950,000) = 2,304,000 + 546,000 + 49,500 + 798,000 = 3,697,500. Total rows: 4,000,000. Weighted average: 3,697,500 ÷ 4,000,000 = 0.9244, i.e. 92.4%. Note that the unweighted mean, (96 + 91 + 99 + 84) ÷ 4 = 92.5%, happens to sit very close here — but with different volumes the two can diverge widely, so always compute the one that was asked for. When you present clear insights to colleagues, state which average you used, and remember what a single headline hides: the weak Cases dataset (84%) is masked by the large, healthy Payments dataset, so pair any weighted headline with the worst-performer figure.

**Question 8 (hard) — Trend and projection in pipeline runtimes.**
A fact table build takes 40 minutes today. Data volume grows 8% per month, and runtime scales linearly with volume. Your delivery window allows a maximum build time of 55 minutes. After how many whole months will the build first exceed the window?

A) 3 months  B) 4 months  C) 5 months  D) 6 months

**Correct answer: C.**
**Explanation:** Runtime after n months: 40 × 1.08ⁿ. Month 1: 43.2. Month 2: 46.7. Month 3: 50.4. Month 4: 54.4. Month 5: 58.8. The build first exceeds 55 minutes at month 5. The tempting shortcut — "we need 37.5% growth; at 8% a month that's about 4.7 months, so 4" — fails because compounding accelerates growth but the threshold is crossed between months 4 and 5, and the question asks for the first whole month past the limit. Projections like this are how you turn a trend into a preventative measure (your problem management skill): armed with "we breach the window in five months", you can schedule optimisation work calmly instead of firefighting later.

**Question 9 (hard) — Cost-benefit of an emerging tool.**
You are assessing a new data transformation tool for your team of four engineers. Licence: £180 per engineer per month. Migration effort: 240 engineer-hours, at an internal cost of £45 per hour. The vendor claims a 15% productivity gain. Your team delivers roughly 560 productive engineering hours per month in total. Valuing productive hours at the same £45 rate, in which month after go-live does the cumulative benefit first exceed the cumulative cost (including migration)?

A) Month 3  B) Month 4  C) Month 5  D) Month 6

**Correct answer: B.**
**Explanation:** Monthly benefit: 15% × 560 hours × £45 = 84 × £45 = £3,780. Monthly licence cost: 4 × £180 = £720. Net monthly gain: £3,780 − £720 = £3,060. One-off migration cost: 240 × £45 = £10,800. Break-even when 3,060n > 10,800, i.e. n > 3.53, so the cumulative benefit first exceeds cost during month 4. This is the quantitative half of your data innovation skill — "understand the impact on the organisation of emerging trends in data tools" — and note the sensitivity: if the real productivity gain is 10% rather than the vendor's claimed 15%, the net monthly gain falls to £1,800 and break-even slips to month 6. Presenting the range, not just the vendor's best case, is what makes your advice trustworthy.

**Question 10 (moderate) — Interpreting a test results table.**
Your team's regression suite reports, by layer: staging — 340 tests, 334 passed; intermediate — 210 tests, 189 passed; marts — 150 tests, 144 passed. Which layer has the worst pass rate, and what is the overall pass rate across all tests?

A) Intermediate worst (90.0%); overall 95.3%
B) Marts worst (96.0%); overall 95.3%
C) Intermediate worst (90.0%); overall 94.6%
D) Staging worst (98.2%); overall 95.9%

**Correct answer: A.**
**Explanation:** Pass rates by layer: staging 334/340 = 98.2%; intermediate 189/210 = 90.0%; marts 144/150 = 96.0%. Intermediate is worst. Overall: total passed = 334 + 189 + 144 = 667; total tests = 340 + 210 + 150 = 700; 667/700 = 95.3%. Note the overall figure is not the average of the three rates ((98.2 + 90.0 + 96.0) ÷ 3 = 94.7%) because the layers differ in size — the same weighted-versus-unweighted principle as Question 7, appearing here in the form you meet when you "analyse and report test activities and results". The intermediate layer's 21 failures are also where you would direct investigative effort first.

**Question 11 (moderate) — Percentage change in problem trends.**
Incident tickets attributed to data quality problems over four months: March 48, April 60, May 45, June 27. Which statement correctly describes the June figure?

A) June fell 18% from May and 55% from April.
B) June fell 40% from May and 55% from March.
C) June fell 40% from April and 43.75% from March.
D) June fell 40% from May and 43.75% from March.

**Correct answer: D.**
**Explanation:** May to June: (45 − 27) ÷ 45 = 18 ÷ 45 = 0.40, a 40% fall. March to June: (48 − 27) ÷ 48 = 21 ÷ 48 = 0.4375, a 43.75% fall. Both parts of option D check out. Option A's "18%" is the absolute fall of 18 tickets misread as a percentage. Option B attaches the April comparison's figure (April to June is (60 − 27) ÷ 60 = 55%) to the wrong baseline month. Option C attributes the May comparison to April. The safest technique under time pressure is to compute each named comparison directly from the table rather than judging plausibility. The senior-level habit this drills is precision about baselines — "down 40%" means nothing until you state down from when, a discipline central to presenting problem trends honestly when you monitor investigations and report progress to stakeholders.

**Question 12 (hard) — Storage growth and retention policy.**
A fact table currently holds 3.2 TB. It grows by 120 GB per month. A proposed retention policy would archive all data older than 24 months, which today would remove 1.1 TB immediately, after which the net growth (new data in, old data archiving out) would be 25 GB per month. Storage costs £19 per TB per month. What is the approximate monthly cost saving 12 months from now, comparing the two futures? (Use 1 TB = 1,000 GB.)

A) About £43 per month  B) About £62 per month  C) About £26 per month  D) About £87 per month

**Correct answer: A.**
**Explanation:** Compare the two futures at the 12-month mark. Without the policy: 3.2 TB + 12 × 0.12 TB = 3.2 + 1.44 = 4.64 TB, costing 4.64 × £19 = £88.16 per month. With the policy: 3.2 − 1.1 + 12 × 0.025 = 2.1 + 0.3 = 2.4 TB, costing 2.4 × £19 = £45.60 per month. Monthly saving: £88.16 − £45.60 = £42.56, so about £43. Equivalently, the storage difference is 4.64 − 2.4 = 2.24 TB, and 2.24 × £19 = £42.56 — computing it both ways is a quick self-check. Option D is the without-policy cost mistaken for the saving; option C compares against today's size instead of the projected one. The broader point: small per-TB prices multiplied across many tables and many months are what justify retention and archiving standards — quantifying that saving is how you win the argument when you develop standards for data transformation and storage.

**Question 13 (easy) — Reading a capacity table with unit traps.**
A platform report states: "Daily ingest: 4.5 million rows. Average row size: 2 KB. Compression ratio 4:1 on storage." Approximately how much storage does one day's ingest consume after compression? (1 GB = 1,000,000 KB.)

A) 9.0 GB  B) 2.25 GB  C) 36 GB  D) 4.5 GB

**Correct answer: B.**
**Explanation:** Raw size: 4,500,000 rows × 2 KB = 9,000,000 KB = 9.0 GB. Compression at 4:1 divides by 4: 9.0 ÷ 4 = 2.25 GB. Option A forgets compression; option C multiplies by 4 instead of dividing; option D halves instead. The classic pitfall here is unit and ratio direction — precisely the "misreading scale qualifiers" error that numeric assessments are designed to catch, and precisely the kind of estimate you make when advising on storage best practice.

**Question 14 (moderate) — Training coverage for data users.**
You oversee training for users of your team's datasets. Of 220 registered users, 132 have completed the new data model training. Your target is 85% coverage by quarter end, and you can run sessions of up to 25 users each. What is the minimum number of further sessions needed to reach the target, assuming full sessions?

A) 2  B) 3  C) 4  D) 5

**Correct answer: B.**
**Explanation:** Target: 85% × 220 = 187 users trained. Already trained: 132. Shortfall: 187 − 132 = 55 users. Sessions of 25: 55 ÷ 25 = 2.2, which rounds up to 3 sessions (two sessions cover only 50). Remember that people arithmetic always rounds up — a fractional session cannot train the remaining five users. Overseeing "training and support for users of data sets" is a named responsibility at your level, and this is its planning arithmetic.

**Question 15 (hard) — Comparing two remediation options with combined rates.**
A cleansing exercise must fix 18,000 malformed address records. Option 1: a rules-based script fixes 70% of records automatically at negligible cost; the remainder go to a data steward team that clears 250 records per day at £310 per day. Option 2: an enhanced matching service fixes 92% automatically at a one-off cost of £4,300; the remainder go to the same steward team. Which option costs less in total, and by roughly how much?

A) Option 1, by about £1,200  B) Option 2, by about £990  C) Option 2, by about £2,400  D) They cost about the same

**Correct answer: B.**
**Explanation:** Option 1: automatic fixes 0.70 × 18,000 = 12,600, leaving 5,400 manual. Steward days: 5,400 ÷ 250 = 21.6 days; cost 21.6 × £310 = £6,696. Option 2: automatic fixes 0.92 × 18,000 = 16,560, leaving 1,440 manual. Steward days: 1,440 ÷ 250 = 5.76; cost 5.76 × £310 = £1,785.60; plus £4,300 one-off = £6,085.60. Difference: £6,696 − £6,085.60 = £610.40... check the steward arithmetic: 21.6 × 310 = 6,696 and 5.76 × 310 = 1,785.6 — confirmed, so Option 2 wins by about £610. If steward days must be whole (you pay for full days), Option 1 needs 22 days (£6,820) and Option 2 needs 6 days (£1,860 + £4,300 = £6,160), a gap of £660; either way Option 2 is cheaper by £600-£1,000, making B the only compatible option. Multi-stage cost comparisons with a rounding convention to notice are the realistic texture of "support data quality improvement" decisions — and noticing that the answer is robust to the convention is what lets you commit confidently under time pressure.

**Question 16 (moderate) — Defect density for a test report.**
Your quarterly test report covers two releases. Release 1: 34 defects found across 85 changed models. Release 2: 18 defects across 30 changed models. A colleague drafts the headline: "Defects fell from 34 to 18 — quality improved 47%." What should the headline say instead?

A) Defect density rose from 0.40 to 0.60 defects per changed model — a 50% increase — so quality worsened relative to change volume.
B) Quality improved 47%, as drafted; absolute defect counts are what stakeholders care about.
C) Defect density fell from 0.40 to 0.36 defects per model, a modest improvement.
D) The two releases cannot be compared because they differ in size.

**Correct answer: A.**
**Explanation:** Rates, not raw counts, make releases comparable. Release 1: 34 ÷ 85 = 0.40 defects per changed model. Release 2: 18 ÷ 30 = 0.60. Density rose by (0.60 − 0.40) ÷ 0.40 = 50%. The draft headline commits the classic denominator omission: fewer defects were found because far less changed, and per unit of change the defect rate worsened substantially. Option D overcorrects — differing sizes are precisely why you normalise rather than refuse to compare. Option C is a fabricated figure to catch candidates who expect "improvement" answers. When you "analyse and report test activities and results", this normalisation is the difference between a report that informs and one that soothes — and correcting the draft kindly is the communication half of the job.

### Preparation tips

- **Rebuild fluency with percentage points, relative change, and weighted averages.** These three concepts underpin more than half the questions above and the vast majority of real quality reporting. Ten minutes of deliberate practice a day for a week transforms your speed.
- **Use the on-screen calculator strategically.** Type full expressions where possible rather than chaining partial results — transcription between screen and calculator is where errors breed.
- **Estimate first, compute second.** A rough order-of-magnitude estimate ("about 2 GB, so options C and D are out") lets you catch calculator slips instantly and sometimes answers the question outright.
- **Practise with your own dashboards.** Take last month's pipeline metrics or quality scores and ask yourself assessment-style questions about them. Familiar data makes the mechanics automatic.
- **Track the base of every percentage.** Before computing, say to yourself: "per cent of what?" Most distractor options are built from correct arithmetic on the wrong base.
- **Keep momentum.** At roughly a minute per question, a stuck question costs you two others. Flag, skip, return.

### Common pitfalls

- **Misreading scale qualifiers.** "In thousands", "TB versus GB", "per month versus per year" — the numeric equivalent of a grain statement. Read units before touching the numbers.
- **Confusing percentage points with percentages.** A rise from 88% to 92.4% is 4.4 points but a 5% relative gain. Assessments — and stakeholders — will test whether you keep these straight.
- **Averaging rates without weights.** Overall pass rates, match rates, and quality scores must be computed from totals, not by averaging sub-rates of unequal size.
- **Over-calculating.** If two options differ by an order of magnitude, estimation settles it; exact long division is a time sink.
- **Answering the intermediate result.** Distractors are frequently your own correct partial computations (a raw total instead of a difference, a pre-filter count instead of a final one). Re-read what the question asks for before selecting.
- **Ratio direction errors.** "4:1 compression", "3 linked for every 1 unmatched" — decide explicitly which way the ratio operates before applying it.


## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment evaluates how well you understand, analyse, and draw correct conclusions from written business information — mirroring the exact reading demands of your role. The passages use the material you genuinely handle: data standards documents, modelling specifications, governance policies, stakeholder emails, incident reports, and documentation guidance. The defining rule is fact-based logic: you must answer strictly from the text provided, ignoring outside knowledge, however expert yours is. Most questions require a verdict of True (the passage logically supports the statement), False (the passage contradicts it), or Cannot Say (the passage provides insufficient information either way), with some multiple-choice comprehension items. These tests are time-pressured — often less than a minute per question — to simulate reading under workplace deadlines.

For a senior analytics engineer, this skill is deceptively central. You review specifications and requirements, where the difference between "must", "should", and "may" changes what you build and what you test. You ensure documentation of data meets standards, which means reading drafts with a precision most readers never apply. You manage differing stakeholder perspectives, which requires extracting what an email actually commits to versus what it merely gestures at. And you advocate for your team externally, where misquoting a policy — even slightly — damages credibility. The discipline this assessment trains, answering only from the text, is the same discipline that makes you a trustworthy reviewer: the specification says what it says, not what you assume it meant.

### What it measures for your role

- **Communicating between the technical and non-technical** — parsing stakeholder emails and papers accurately before you respond; representing others' positions faithfully when you host discussions in a multidisciplinary team with difficult dynamics.
- **Testing** — "review requirements and specifications" is verbal reasoning applied professionally: what conditions does this sentence actually impose, and what does it leave unstated?
- **Data modelling, cleansing and enrichment** — standards documents define what "adherence to standards" means; you cannot enforce wording you have misread.
- **Metadata management** — metadata is written meaning; definitions, ownership statements, and repository guidance demand precise reading, and you advise less experienced colleagues on exactly these texts.
- **Problem management** — incident reports and post-incident reviews must be read for what the evidence establishes versus what a hurried author asserted.
- **Data analysis and synthesis** — distinguishing what source system documentation states from what it implies is the first step of source system analysis.

### Practice questions

**Passage A — Data transformation standard (for Questions 1-4).**
"All transformation code must be version controlled and peer reviewed before deployment to the production environment. Peer review must be performed by an analytics engineer who did not author the change. Changes classified as minor — defined as documentation-only updates or formatting changes with no effect on query results — may be reviewed after deployment, provided the review occurs within five working days. Model owners are responsible for ensuring that every model has at least one uniqueness test and one referential integrity test where a foreign key exists. Exemptions from testing requirements may be granted by the data engineering standards board, and must be recorded in the exemptions register with a review date not more than twelve months ahead."

**Question 1 (easy).** True, False, or Cannot Say: "A documentation-only update may be deployed to production before it has been peer reviewed."

**Correct answer: True.**
**Explanation:** The passage classifies documentation-only updates as minor and states minor changes "may be reviewed after deployment, provided the review occurs within five working days." Review after deployment necessarily means deployment can precede review. The statement follows directly from the text — note that you are not being asked whether this is good practice, only what the standard permits.

**Question 2 (moderate).** True, False, or Cannot Say: "A model with no foreign keys is not required to have any tests."

**Correct answer: False.**
**Explanation:** The passage requires "at least one uniqueness test" for every model, unconditionally. Only the referential integrity test is conditional on a foreign key existing ("where a foreign key exists"). A model without foreign keys still requires the uniqueness test, so the statement contradicts the passage. This is a classic scope-of-qualifier item: the conditional clause attaches to the second requirement only, and misreading its reach is exactly the error that causes real review disputes.

**Question 3 (moderate).** True, False, or Cannot Say: "The data engineering standards board reviews all exemption requests within twelve months."

**Correct answer: Cannot Say.**
**Explanation:** The passage says exemptions "may be granted" by the board and must be recorded "with a review date not more than twelve months ahead." That constrains the recorded review date of granted exemptions; it says nothing about how quickly the board reviews requests, nor that the board reviews "all" requests on any timescale. The statement blends a real detail (twelve months) into a claim the text never makes — the signature construction of a Cannot Say item. Resist the pull of plausibility: plausible-and-unstated is Cannot Say, not True.

**Question 4 (hard).** True, False, or Cannot Say: "A formatting change that alters query results may be reviewed after deployment."

**Correct answer: False.**
**Explanation:** Read the definition clause precisely: minor changes are "documentation-only updates or formatting changes with no effect on query results." A formatting change that alters query results fails the definition, so it is not minor, and only minor changes qualify for post-deployment review; everything else "must be ... peer reviewed before deployment." The statement contradicts the standard. Definitional boundary-testing like this is precisely how you should read standards when you develop them for your team — every definition creates edge cases, and reviewers who spot them prevent loopholes.

**Passage B — Stakeholder email (for Questions 5-7).**
"From: Head of Operational Insight. Subject: Case dashboard discrepancies. Team — Our operations leads have flagged that the weekly case dashboard showed 4,860 open cases on Monday, while the operational system showed 4,912 at the same time. I appreciate the figures are drawn at different moments, but the leads' confidence in the dashboard is slipping, and two of them have started exporting their own figures directly from the operational system. Before we escalate anything, could your team confirm how the dashboard extract handles cases reopened over the weekend? If the extract logic is sound, we will need a short note we can share with the leads explaining the difference; if it is not, I would like a view on the fix effort by Thursday. I have not raised this with the data governance board and would prefer we understand it first."

**Question 5 (easy).** True, False, or Cannot Say: "The Head of Operational Insight has already escalated the discrepancy to the data governance board."

**Correct answer: False.**
**Explanation:** The email states plainly: "I have not raised this with the data governance board." The statement directly contradicts the text. Easy — but under time pressure, candidates who skim and remember only "escalate" from earlier in the email ("before we escalate anything") get this wrong. Anchor verdicts to the sentence, not the gist.

**Question 6 (moderate).** True, False, or Cannot Say: "The dashboard extract mishandles cases that were reopened over the weekend."

**Correct answer: Cannot Say.**
**Explanation:** The email asks the team to "confirm how the dashboard extract handles cases reopened over the weekend" — it raises this as a hypothesis to investigate, not a finding. The sender explicitly allows both possibilities ("if the extract logic is sound... if it is not..."). Concluding the extract is faulty imports an assumption the text does not make. This mirrors real triage discipline from your problem management skill: a stakeholder's suggested cause is a lead, not a diagnosis, and a senior engineer neither dismisses it nor adopts it before checking.

**Question 7 (hard).** Which of the following best describes what the sender is asking for by Thursday?

A) A note for the operations leads explaining the difference between the two figures.
B) Confirmation of how the extract handles reopened cases.
C) An estimate of the effort to fix the extract, if the extract logic turns out to be flawed.
D) A decision on whether to escalate to the data governance board.

**Correct answer: C.**
**Explanation:** Trace the conditional structure. The confirmation of extract behaviour (B) is requested, but with no stated deadline. The explanatory note (A) is required only "if the extract logic is sound", again without a date. The Thursday deadline attaches solely to "a view on the fix effort" in the branch where the logic "is not" sound. Escalation (D) is explicitly deferred. Assessments — and real inboxes — reward mapping each request to its own condition and deadline rather than attaching the one date you noticed to the most memorable request. Misreading this email would have you promising the wrong deliverable at Thursday's stand-up.

**Passage C — Metadata repository guidance (for Questions 8-10).**
"The metadata repository shall hold business definitions, ownership records, and lineage for all datasets classified as corporate data assets. Dataset owners must review business definitions at least annually; definitions unreviewed after fifteen months will be flagged as stale and excluded from the certified data catalogue until reviewed. Lineage must be captured automatically where tooling permits; manual lineage entries are permitted but must identify the recording engineer and the date of capture. The repository does not hold operational metadata, such as load timestamps, which remain in the platform monitoring system. Teams proposing changes to repository structure should submit a proposal to the metadata working group, which meets monthly."

**Question 8 (easy).** True, False, or Cannot Say: "Load timestamps are stored in the metadata repository."

**Correct answer: False.**
**Explanation:** The passage states the repository "does not hold operational metadata, such as load timestamps, which remain in the platform monitoring system." The statement contradicts this directly. Straightforward — the item tests whether you registered the exclusion clause, which in a real repository design conversation is precisely the boundary you would need to explain to less experienced team members asking where to look things up.

**Question 9 (moderate).** True, False, or Cannot Say: "A business definition reviewed fourteen months ago will be excluded from the certified data catalogue."

**Correct answer: False.**
**Explanation:** The exclusion trigger is "unreviewed after fifteen months". Fourteen months is within that threshold, so the definition is not yet flagged as stale, and the passage gives no other exclusion mechanism — so the claim, stated as a present fact, contradicts the rule. Note the layered thresholds: review is expected "at least annually" (twelve months), but the exclusion consequence bites only at fifteen. A definition at fourteen months is out of compliance with the review expectation yet still in the catalogue — standards frequently separate the obligation from the sanction, and precise readers keep the two apart.

**Question 10 (moderate).** True, False, or Cannot Say: "Manual lineage entries are prohibited where automatic capture tooling exists."

**Correct answer: Cannot Say.**
**Explanation:** The passage requires automatic capture "where tooling permits" and permits manual entries subject to attribution requirements. It does not state that the availability of tooling prohibits manual entries — perhaps manual additions supplement automatic capture; perhaps they are disallowed. The text simply does not resolve it. A natural operational reading leans towards "automatic replaces manual", but leaning is not licence: the verdict must rest on stated wording. When you advise on metadata management, this is exactly the ambiguity you would flag for clarification in the guidance rather than resolve by private assumption.

**Passage D — Extract from a post-incident review (for Questions 11-13).**
"On 14 May, the customer dimension build failed for three consecutive runs. The immediate cause was a schema change in the upstream HR system: the `team_code` column was renamed without notice to downstream consumers. The duty engineer applied a temporary column alias at 11:20, restoring the build by 11:45. Data consumers experienced stale dimension data for approximately 19 hours; no incorrect data was served. The review found that the data-sharing agreement with the HR system owner does not currently require advance notification of schema changes, although a notification clause was proposed in draft revisions circulated in March. The review recommends: (1) adopting the notification clause; (2) adding a schema drift test at the staging layer; (3) documenting the alias workaround and replacing it with a mapped rename within one sprint."

**Question 11 (easy).** True, False, or Cannot Say: "Consumers were served incorrect dimension data during the incident."

**Correct answer: False.**
**Explanation:** The passage states "no incorrect data was served" — consumers experienced stale data, which the text distinguishes from incorrect data. The item tests whether you preserve the author's distinction rather than merging "stale" and "wrong" into one impression. In incident communication this distinction is the difference between "reports were out of date" and "reports were misleading" — materially different messages to give stakeholders, and as the senior engineer you would insist the report keeps them separate.

**Question 12 (moderate).** True, False, or Cannot Say: "The data-sharing agreement requires the HR system owner to notify downstream consumers before schema changes."

**Correct answer: False.**
**Explanation:** The review "found that the data-sharing agreement ... does not currently require advance notification of schema changes." The statement asserts the opposite of the text. The distractor force here is the draft revision: a notification clause exists in draft and is recommended for adoption, and a skimming reader converts "proposed in draft" into "in force". Contract-versus-draft confusions cause real incidents to repeat; reading the governing document's current state accurately is part of ensuring issues and risks are genuinely resolved rather than assumed resolved.

**Question 13 (hard).** True, False, or Cannot Say: "The temporary alias applied by the duty engineer remains in place at the time of the review."

**Correct answer: True.**
**Explanation:** Recommendation (3) is to document "the alias workaround and [replace] it with a mapped rename within one sprint." One can only recommend replacing something that has not yet been replaced; the recommendation's existence entails the alias is still in place when the review was written. This is a legitimate one-step inference from the text — unlike Cannot Say items, where the required inference goes beyond what the words entail. Distinguishing entailed inference (True) from invited assumption (Cannot Say) is the hardest judgement in verbal reasoning tests, and the professional analogue is reading a review and knowing which follow-up actions are genuinely still open.

**Question 14 (hard) — Comprehension across a dense governance passage.**
Read the following extract from a data quality policy: "Datasets feeding statutory returns are designated Tier 1 and must meet all applicable quality thresholds before publication. Where a Tier 1 dataset fails a threshold, publication may proceed only if the responsible deputy director approves a documented risk acceptance, and the failure and acceptance are disclosed in the return's quality annex. Tier 2 datasets, which feed internal management information, require thresholds to be monitored and breaches reported quarterly, but breaches do not block publication. Reclassification between tiers requires the data governance board's approval."

Which of the following situations is consistent with the policy?

A) A Tier 1 dataset fails a threshold and is published with the failure disclosed in the quality annex, without deputy director approval, because the failure was marginal.
B) A Tier 2 dataset breaches a threshold and continues to be published, with the breach reported in the next quarterly report.
C) A team reclassifies its dataset from Tier 1 to Tier 2 with its deputy director's approval to avoid a publication block.
D) A Tier 1 dataset fails a threshold and publication proceeds with the deputy director's verbal agreement, disclosed in the annex.

**Correct answer: B.**
**Explanation:** Option B matches the Tier 2 regime exactly: breaches monitored, reported quarterly, publication not blocked. Option A omits the deputy director's approval, which the policy makes a condition ("only if"), and offers a justification ("marginal") the policy nowhere recognises. Option C uses the wrong authority: reclassification requires the data governance board, not a deputy director. Option D fails the documentation requirement — the policy demands "a documented risk acceptance", and verbal agreement is not documented acceptance. Every wrong option is nearly right, differing in one condition — which is how policy misapplications happen in real organisations, and why your role of ensuring documentation and standards are met depends on condition-by-condition reading.

**Passage E — Briefing extract on emerging data tooling (for Questions 15-17).**
"The cross-government analytics engineering community's annual survey reports that 62% of responding teams now use a declarative transformation framework, up from 41% two years ago. Teams using such frameworks reported a median review turnaround of 1.5 working days, compared with 3 working days for teams using bespoke scripts, although the survey authors caution that teams adopting frameworks earlier also tended to have more mature review practices generally. Adoption was most common in larger teams: 78% of teams with more than five engineers used a framework, against 44% of smaller teams. The survey did not collect data on build performance or platform cost. The authors recommend that departments considering adoption pilot the framework on a single data mart before committing, and note that two departments have discontinued framework use, citing licensing changes."

**Question 15 (moderate).** True, False, or Cannot Say: "Using a declarative transformation framework causes faster review turnaround."

**Correct answer: Cannot Say.**
**Explanation:** The survey reports an association — framework users show a 1.5-day median against 3 days — but the authors explicitly caution that early adopters "also tended to have more mature review practices generally", flagging a confounder. An association with an acknowledged alternative explanation does not establish causation, and the passage never claims it does. This distinction is the working core of your data innovation skill: understanding the impact of emerging trends means reading vendor claims and community surveys with exactly this scepticism before advising your organisation.

**Question 16 (easy).** True, False, or Cannot Say: "More than three-quarters of teams with over five engineers use a declarative transformation framework."

**Correct answer: True.**
**Explanation:** The passage states 78% of teams with more than five engineers use a framework; 78% is more than three-quarters (75%). A pure extraction item — the only work is converting "three-quarters" to 75% and comparing. Under time pressure, bank these marks quickly and spend the saved seconds on inference-heavy items like Question 15.

**Question 17 (hard).** True, False, or Cannot Say: "Framework adoption reduces platform costs for most teams."

**Correct answer: Cannot Say.**
**Explanation:** The passage states the survey "did not collect data on build performance or platform cost", so the text contains no cost evidence in either direction. Two details might tempt a False verdict — the discontinuations "citing licensing changes" — but licensing is a reason two departments left, not evidence about platform costs across most teams. No evidence for, no evidence against: Cannot Say. When you brief a governance board on a new tool, this is the honest answer's shape too — "the evidence we have does not address cost" is a finding, and a senior engineer reports it rather than papering over it.

**Question 18 (moderate) — Comprehension: the survey's recommendation.**
Still using Passage E: which of the following best captures the survey authors' recommendation to departments considering adoption?

A) Adopt a declarative framework, since a majority of teams now use one.
B) Avoid frameworks, given that two departments have discontinued use.
C) Pilot the framework on a single data mart before making a wider commitment.
D) Adopt frameworks only in teams with more than five engineers.

**Correct answer: C.**
**Explanation:** The recommendation sentence is explicit: "pilot the framework on a single data mart before committing." Option A converts a descriptive statistic (62% adoption) into advice the authors never give — popularity is context in the passage, not counsel. Option B inflates a cautionary note (two discontinuations, attributed to licensing) into a recommendation against adoption. Option D manufactures a rule from the team-size adoption pattern, which the passage reports as an observation, not guidance. The skill here — separating what a document recommends from what it merely reports — is one you exercise every time you turn community evidence into advice for your own organisation, and every time you brief stakeholders on what a review "found" versus what it "suggested". Authors' descriptive statements and their normative ones deserve different weights, and precise readers never let the former masquerade as the latter.

### Preparation tips

- **Train the "text only" reflex.** Your expertise is the biggest hazard here: you know how transformation standards usually work, so you will be tempted to answer from experience. Practise saying "where does the passage say that?" before every verdict.
- **Learn the three verdicts as tests, not moods.** True: the passage entails it. False: the passage contradicts it. Cannot Say: neither. If you are weighing plausibility, you have already drifted — plausible-but-unstated is Cannot Say.
- **Read the statement first, then scan.** For True/False/Cannot Say items, reading the statement before the passage tells you which sentences matter. With under a minute per question, targeted scanning beats full reading.
- **Mark qualifiers as you read.** "Must", "may", "should", "only if", "at least", "where a foreign key exists" — the scope of these words decides most answers. This is the same skill you use reviewing specifications, so practise on real standards documents.
- **Watch for near-synonym swaps.** Stale versus incorrect, proposed versus adopted, review date versus review speed — assessments (like careless report authors) exchange neighbouring words and change the truth value.
- **Use your reviewer's stamina.** You already read dense material critically for a living. The assessment simply compresses it; a few timed practice passages will calibrate your pace.

### Common pitfalls

- **Making assumptions from professional knowledge.** The most experienced candidates lose the most marks this way — answering what the standard should say rather than what the passage says.
- **Confusing likelihood with fact.** A passage saying an outcome is expected, proposed, or under consideration does not make it true. Drafts are not policy; hypotheses are not findings.
- **Missing the scope of a conditional.** Deciding whether "where a foreign key exists" governs one requirement or both is the difference between True and False on Question 2 — and between passing and failing a real model review.
- **Overcorrecting into Cannot Say.** Cannot Say is not a refuge for hard questions. When the text entails a statement through a single valid inference step — as in Question 13 — the answer is True, and reflexively choosing Cannot Say costs marks.
- **Poor time management.** Reading every passage exhaustively before looking at the questions burns your budget. Scan with purpose.
- **Losing the thread across long sentences.** Governance prose stacks conditions. Mentally number them ("publication requires: threshold met, OR approval AND disclosure") before judging any option against them.


## Workplace job-specific situational judgement assessment

### About this assessment

A workplace job-specific situational judgement assessment evaluates your decision-making, interpersonal effectiveness, and professional conduct. Instead of logic puzzles or arithmetic, it presents realistic workplace dilemmas — conflicts, ethical tensions, operational pressure — and asks how you would respond. Typical formats ask you to select the Most Effective and Least Effective actions from a set, or to rank or rate all the options. There is rarely a single objectively right answer; several responses may look reasonable, but one aligns best with the values of the organisation and the demands of the role. These assessments are usually untimed or generously timed, because they measure natural judgement rather than speed.

For a senior analytics engineer in UK government, the values dimension is explicit. Your judgements are expected to reflect public sector principles: putting user needs first, working in the open with honesty and transparency, collaborating across disciplines, and building accessible, inclusive services and teams. Your role profile adds specific behavioural expectations: you coach and mentor less senior engineers rather than simply correcting them; you build relationships with stakeholders and manage differing perspectives; you host discussions in multidisciplinary teams with potentially difficult dynamics; you advocate for your team externally; and you ensure issues and risks are resolved rather than hidden. The scenarios below are built from those exact responsibilities. As you work through them, notice that the strongest options usually combine three things: addressing the root issue (not just the symptom), preserving relationships and trust, and acting at the right level of urgency — neither passive nor heavy-handed.

### What it measures for your role

- **Communicating between the technical and non-technical** — de-escalating stakeholder tension, translating technical trade-offs honestly, managing differing perspectives without taking sides prematurely.
- **Coaching and oversight (role level)** — developing less senior engineers through feedback and delegation; balancing delivery pressure against learning opportunities; directing work without micromanaging.
- **Problem management** — responding to incidents and risks with proportionate urgency, consulting specialists, and pursuing preventative measures over quick blame.
- **Data modelling, cleansing and enrichment / Testing** — holding the line on standards and quality when deadlines, seniority, or politics push against them.
- **Metadata management and documentation (role level)** — ensuring documentation standards survive real-world pressure to skip them.
- **Data innovation** — championing new ways of working responsibly, without chasing novelty or dismissing legitimate caution.

### Practice questions

**Question 1 (moderate) — The struggling junior and the slipping deadline.**
A junior analytics engineer you mentor is two days from delivering a data mart for a stakeholder demo. Reviewing their work informally, you see the model works but ignores the team's dimensional standards in several places, and reworking it properly would likely miss the demo. The junior looks stressed and has not asked for help.

A) Quietly rebuild the model to standard yourself tonight so the demo succeeds and the junior is spared embarrassment.
B) Let the demo proceed on the non-standard model without comment, and raise the standards issues in the next sprint retrospective.
C) Talk with the junior today: agree that the demo proceeds on the working model, jointly log the standards gaps as technical debt with a committed fix window, and plan pairing time so they learn the standards on the rework.
D) Tell the junior the model cannot be demonstrated until it meets standards, and inform the stakeholder the demo must move.

**Most effective: C. Least effective: A.**
**Explanation:** Option C separates the two real questions — "is the demo viable?" and "how does this engineer learn the standards?" — and answers both: the stakeholder keeps their demo on a working model, the debt is made visible and scheduled rather than hidden, and the rework becomes a coaching vehicle, which is your explicit role-level duty. Option A is the classic senior-engineer trap: it rescues the artefact while sabotaging the person — the junior learns nothing except that their work gets silently replaced, trust is damaged, and you have set a precedent of heroics that does not scale; it is the least effective. Option B avoids the difficult conversation and lets non-standard work reach stakeholders unexamined — passive on both fronts. Option D treats standards as absolute when the pragmatic path (demo now, documented debt, prompt fix) protects both the user-facing outcome and the standard; it also spends stakeholder goodwill needlessly.

**Question 2 (moderate) — The stakeholder who wants "just a quick extract".**
A well-regarded operations manager emails you directly: "Your team's pipeline is too slow for what I need — can you just give me a direct extract of the underlying tables each week? I'll build my own figures." You know direct extracts bypass the quality tests and conformed definitions your team maintains, and that two versions of "open cases" already circulate in the organisation.

A) Decline, explaining that policy does not allow direct extracts, and copy your line manager.
B) Provide the extract — the manager is experienced, and refusing will damage an important relationship.
C) Meet the manager to understand what decision they are trying to support and by when; explain the risk of a second, untested version of the figures; and agree either a fast-tracked addition to the governed model or a clearly labelled interim extract with a retirement date.
D) Suggest they raise a formal request through the intake process so it can be prioritised against other work.

**Most effective: C. Least effective: B.**
**Explanation:** Option C treats the request as a symptom of an unmet user need — the manager does not want tables, they want timely figures for a decision. Meeting it with curiosity honours user needs; explaining the conformance risk is the honest technical translation your communication skill demands; and the agreed outcome keeps a single version of the truth while giving the user a route forward. Option B is least effective: it feels collaborative but quietly multiplies unquantified risk — untested figures, divergent definitions, and an invisible dependency your team will one day break without knowing anyone relied on it. Option A hides behind policy and escalation instead of engaging the need; the relationship damage it causes is avoidable. Option D is not wrong, but as a first and only response it is passive — process without partnership — and will likely drive the manager to build a workaround anyway.

**Question 3 (hard) — The defect found after sign-off.**
Your team's new financial reporting mart passed testing and has been signed off; the first monthly figures go to the department's board tomorrow. This evening, an engineer messages you: they have found a join condition that double-counts a small category of adjustment transactions — roughly 0.4% of total value, but concentrated in one directorate's figures, which it inflates by about 6%.

A) Say nothing tomorrow; fix the join in the next release and note the correction in the following month's figures if anyone asks.
B) Tonight, verify the finding with the engineer; inform the service owner and the report's business owner immediately with the quantified impact; recommend either correcting before issue or issuing with a disclosed caveat on the affected directorate; and schedule a fix and a regression test for the join pattern.
C) Pull the report entirely and tell the board secretariat it will be delayed until a full re-test of the mart is complete.
D) Fix the join quietly tonight and regenerate the figures, since the numbers will now be right and no one needs to be alarmed.

**Most effective: B. Least effective: A.**
**Explanation:** Option B does everything a senior engineer's duty requires: verify before alarming anyone, quantify the impact honestly, put the publication decision where it belongs (with the accountable owners, informed by your evidence), and convert the incident into prevention through a regression test — the problem management pattern of resolution plus preventative measures. Option A is least effective: knowingly letting a materially wrong figure (6% inflation of one directorate) reach a board breaches the transparency that public sector reporting depends on, and the deferred correction converts an honest defect into an apparent cover-up. Option D fixes the data but subverts governance — regenerating signed-off figures without telling the owners destroys the meaning of sign-off and, if discovered, trust in your team; good intent does not repair that. Option C is disproportionate: the defect is quantified and localised, so a full pull-and-retest sacrifices the board's visibility of every other directorate to avoid a caveat — heavy-handed urgency rather than calibrated urgency.

**Question 4 (moderate) — The difficult multidisciplinary meeting.**
You are hosting a session to agree the grain of a new events model. Ten minutes in, the discussion has turned tense: a performance analyst insists on event-level grain for flexibility; the platform engineer objects on cost grounds; a service owner interjects that "this is exactly why data work always takes forever here." Voices are rising and two attendees have gone silent.

A) Keep the debate running — strong disagreement now prevents weak compromise later, and the loudest concerns are clearly the most important.
B) Pause the discussion; restate the shared goal and the genuine trade-off (flexibility versus cost) neutrally; invite the two silent attendees for their view; and propose capturing the decision criteria and cost estimates as actions before reconvening.
C) Side with the performance analyst, since analytical flexibility is the model's purpose, and move the meeting on.
D) Close the meeting and escalate the disagreement to the heads of both professions to resolve.

**Most effective: B. Least effective: A.**
**Explanation:** Option B is textbook facilitation of "discussions within a multidisciplinary team, with potentially difficult dynamics" — your named skill. It lowers the temperature, reframes positions as a legitimate engineering trade-off rather than a contest, deliberately includes the silent voices (inclusion is not decoration; the quiet attendees may hold the missing constraint), and moves the group from assertion to evidence. Option A confuses heat with rigour: unmanaged escalation entrenches positions, silences more voices, and hands the service owner further proof that "data work always takes forever". It is least effective. Option C resolves the tension by fiat and tells the platform engineer their constraint does not matter — the decision may even be right, but the process damages the collaboration you will need for the next ten models. Option D escalates before the team has generated the evidence a decision needs; premature escalation is passivity dressed as governance.

**Question 5 (hard) — Credit and visibility.**
At a cross-department showcase, a senior stakeholder praises "the new data quality dashboard your team built — genuinely the best thing I've seen this year" and attributes it to you personally. In fact the dashboard was designed and built almost entirely by one of your less senior engineers, who is watching from the audience.

A) Accept the praise gracefully and privately thank the engineer afterwards, planning to credit them in the next team meeting.
B) Correct the record immediately and specifically: thank the stakeholder and name the engineer as the designer and builder, inviting them to take questions on it.
C) Deflect modestly — "it was a team effort" — and move the conversation on.
D) Say nothing in the moment, but ask the stakeholder afterwards to email the engineer's line manager with the feedback.

**Most effective: B. Least effective: A.**
**Explanation:** Option B is what "be an advocate for the team externally" means in practice: visible, specific, public credit that builds the engineer's reputation with exactly the audience that matters for their career, and it costs you nothing but a sentence — indeed it enhances your standing as a leader who grows people. Inviting them to take questions converts credit into visibility and development at once. Option A is least effective because the private thank-you does not repair the public misattribution the engineer just witnessed; what they learn is that their best work becomes your applause, which corrodes motivation and trust faster than almost any other leadership failure. Option C is better than silence but launders the individual's achievement into an anonymous collective — inclusion means named recognition, not diffusion. Option D produces a useful artefact (written feedback) but leaves the public record wrong and the moment wasted; it would be a good supplement to B, not a substitute.

**Question 6 (moderate) — The risky shortcut under delivery pressure.**
A programme manager asks your team to skip writing tests and documentation for a new set of models "just this once" to hit a ministerial deadline, promising time to backfill afterwards. Your experience is that backfill time rarely materialises. The deadline is real and the models are genuinely needed.

A) Refuse outright: standards are standards, and the programme must move its deadline.
B) Agree fully — ministerial deadlines outrank internal standards, and the team can backfill later.
C) Negotiate scope, not standards: identify with the programme manager which models are truly needed for the deadline, deliver that subset with tests and documentation intact, and schedule the remainder; if that still cannot fit, escalate the trade-off transparently with a written risk statement.
D) Agree to skip documentation but keep the tests, splitting the difference without telling the programme manager which corners are being cut.

**Most effective: C. Least effective: D.**
**Explanation:** Option C reframes the false choice. The pressure is on volume by a date, and the honest lever is scope: fewer models done properly beats all models done fragile, especially for ministerial work where an error is far more costly than a smaller first delivery. If the genuine minimum still does not fit, C escalates with a written, quantified risk — transparency that lets accountable people make the trade-off knowingly. Option D is least effective: it looks pragmatic but makes the corner-cutting invisible — the programme manager believes they got everything, nobody records the risk, and undocumented models become the next engineer's incident. A hidden compromise is worse than either honest answer. Option A defends the standard but abandons the user need without exploring options — rigidity, not rigour. Option B accepts a promise you have evidence is rarely kept and books the risk against your team's future; deadline pressure explains it but does not make it effective.

**Question 7 (hard) — Two engineers in conflict over standards.**
Two experienced engineers on your team are in escalating conflict over the team's data integration patterns. One wants to adopt a new incremental-loading pattern across all models; the other insists the current full-refresh standard stays until formally revised. Their code reviews of each other's work have turned pointed, and other team members are starting to pick sides.

A) Tell both engineers to keep disagreements out of code reviews and follow the current standard until told otherwise.
B) Convene the two engineers with a clear frame: acknowledge both are arguing for the team's good, separate the technical question (run a time-boxed comparison of the two patterns on a representative model, criteria agreed up front) from the behavioural one (review comments must critique code, not people — addressed with each privately), and commit to updating the written standard with whatever the evidence supports.
C) Adopt the incremental pattern — the engineer proposing it is technically stronger, and momentum matters more than process.
D) Rotate the two engineers onto separate workstreams so their paths cross less often.

**Most effective: B. Least effective: D.**
**Explanation:** Option B addresses both layers of the problem. Technically, it converts a status contest into an evidence question — the "explore and develop new ways of working with data" duty and the "work with other data professionals to improve integration patterns and standards" behaviour, done properly: time-boxed, criteria first, and the standard updated in writing so the team-wide answer is durable. Behaviourally, it names the review-tone problem and handles it privately with each engineer, protecting dignity while stopping the contagion. Option D is least effective: separation treats the symptom, leaves the standards question unresolved (so every future model reopens it), abandons the watching team to an unmodelled conflict, and wastes the energy in the disagreement — which, framed well, is exactly the fuel standards improvement runs on. Option A restores order but freezes improvement and tells your strongest people that initiative is unwelcome. Option C decides on personality rather than evidence, undermines the written standard's authority, and publicly ranks your engineers — a cost that outlives the technical decision.

**Question 8 (moderate) — The governance shortcut discovered.**
While reviewing lineage in the metadata repository, you discover that a neighbouring team has been loading a copy of your team's customer dimension into their own platform via an undeclared nightly extract, bypassing the data-sharing process. Their dashboards — used by their director — depend on it. The extract is eight months old and has silently missed two schema changes.

A) Cut off the extract immediately; undeclared access is a governance breach and the consequences are theirs.
B) Contact the neighbouring team's lead: share what you found without accusation, flag that their figures may be wrong after the missed schema changes, agree an immediate accuracy check for anything director-facing, and set a path to regularise the dependency through the proper data-sharing route — raising the pattern with governance so the process failure gets fixed too.
C) Report the breach to the data governance board and take no further action until they rule.
D) Leave it alone — their platform, their risk, and raising it will sour a neighbourly relationship.

**Most effective: B. Least effective: D.**
**Explanation:** Option B sequences the duties correctly: user protection first (a director may be consuming figures corrupted by two missed schema changes — that accuracy check cannot wait), relationship preserved through a no-blame opening (the shortcut likely signals an intake process that was too slow — a system problem worth surfacing, not just a rule broken), and the dependency made legitimate and visible so it can be maintained safely. Raising the pattern with governance addresses prevention without weaponising it. Option D is least effective: known bad data flowing to a director is not "their risk" in any sense that survives scrutiny — you now know, and silence makes your team complicit while the corruption compounds. Option A protects the letter of governance by knowingly breaking a director's dashboards without warning — maximum damage, no learning, and the neighbouring team's story becomes "their team broke us", not "we bypassed process". Option C is procedurally clean but slow where part of the risk is immediate; escalation and urgent verification are not alternatives, and choosing only the slow one is passivity.

**Question 9 (moderate) — Mentoring versus delivering.**
Sprint capacity is tight. A complex source-system integration needs doing; you could complete it yourself in two days, or pair with a mid-level engineer who is keen to learn source analysis, which would take four to five days and require your intermittent attention. The sprint also holds other commitments that depend on you. There is no immovable external deadline on the integration.

A) Do it yourself; the team's throughput this sprint matters most, and teaching can happen in quieter periods.
B) Hand it to the engineer solo — stretch assignments are how people grow, and they can figure it out.
C) Pair on it: structure the work so the engineer leads with defined checkpoints, treat the extra two-to-three days as a deliberate investment, and adjust the sprint plan openly so the cost is visible and agreed.
D) Split it: do the difficult profiling yourself and give the engineer the routine mapping work.

**Most effective: C. Least effective: A.**
**Explanation:** With no immovable deadline, this is close to a pure investment decision, and option C invests correctly: the engineer leads (so the learning is real), checkpoints bound the risk (so oversight is real), and the sprint plan is adjusted transparently (so the cost is a team decision, not a private virtue). One integration done in five days that leaves a second person capable of source analysis outperforms two days of your time every quarter thereafter — "coach and mentor less senior analytics engineers" and "oversee tasks" done simultaneously. Option A is least effective in this scenario precisely because the deadline pressure that would justify it is absent; "quieter periods" for teaching are a well-documented mirage, and doing it yourself keeps your team permanently dependent on you — the opposite of senior leverage. Option B confuses stretch with abandonment; source analysis has real failure modes, and unsupported struggle on an unfamiliar system teaches mostly frustration. Option D protects delivery but hoards exactly the skill the engineer wanted to learn, leaving them with work they already know how to do.

**Question 10 (hard) — The innovation proposal meeting resistance.**
You believe a semantic-layer approach would let analysts self-serve consistent metrics, cutting your team's ad-hoc request load substantially. You propose a pilot. The head of analysis responds sceptically in a leadership meeting: "We tried something like this three years ago and it failed. Our analysts don't have capacity to learn another tool."

A) Press the case harder with more slides next meeting: the technology has moved on and the objection is out of date.
B) Drop the proposal; without the head of analysis onside a pilot cannot succeed, and the relationship matters more.
C) Ask to understand the earlier failure properly — what was tried, what broke, who was burned; then reshape the pilot to answer those specific risks (small scope, two willing analysts, success criteria agreed with the head of analysis, explicit training-time budget) and invite them to co-own the evaluation.
D) Run the pilot quietly within your own team's remit and present the results once they are undeniable.

**Most effective: C. Least effective: D.**
**Explanation:** Option C treats the scepticism as data — which it is: a three-year-old failure is exactly the organisational evidence your data innovation skill says you should understand before pushing a trend. Asking about the failure respects the head of analysis's experience, surfaces the real risks (perhaps tooling, perhaps training, perhaps sponsorship), and rebuilding the pilot around their concerns with co-owned success criteria converts your chief sceptic into your chief validator — the strongest possible position for a scale-up decision. Option D is least effective: a covert pilot on a capability whose entire value is cross-team adoption cannot generate the evidence that matters (analyst self-service), and its discovery reads as going around a senior stakeholder — the trust cost lands precisely on the relationship the change depends on. "Undeniable results" obtained this way get denied. Option A escalates volume, not evidence, and answers an experience-based objection with slides. Option B mistakes the first objection for the final answer; abandoning a well-founded improvement at the first "no" fails the advocacy your role demands — the skill is in metabolising the objection, not obeying or overriding it.

**Question 11 (moderate) — The user who stopped trusting the numbers.**
An operations lead tells you their team has "gone back to counting manually" because the case dashboard "was wrong once too often". Your logs show the dashboard has been accurate for four months since a defect was fixed, but the manual counts now circulate in parallel and occasionally contradict the dashboard in meetings.

A) Show the operations lead the four months of accuracy metrics and ask them to stand the manual counts down.
B) Treat it as a trust-repair problem: acknowledge the history without defensiveness, run a joint reconciliation of the manual count against the dashboard for two or three cycles with their team, explain any differences found (timing, definitions), and agree the conditions under which they would retire the manual count — then keep publishing the accuracy metrics they said they needed.
C) Escalate to the operations director that duplicate reporting is wasting staff time and creating contradictory figures.
D) Add a banner to the dashboard stating it is the single authoritative source of case figures.

**Most effective: B. Least effective: D.**
**Explanation:** Trust lost through experience is rebuilt through experience, not assertion — option B supplies exactly that: shared evidence gathered with the sceptical users, honest accounting of the residual differences (which usually turn out to be timing and definition, the explainable kind), and a dignified exit ramp for the manual process defined by the users themselves. This is "provide ongoing support to users" and "manage differing stakeholder perspectives" in their hardest form. Option D is least effective: a banner asserting authority at users who concluded from experience that the authority was misplaced does not move a single mind — it is declaration substituting for repair, and it invites quiet ridicule. Option A leads with your evidence but skips their experience; being told your scepticism is obsolete rarely retires it, though the metrics belong inside option B's approach. Option C converts a repairable trust problem into a political one and burns the relationship in the process; it might eventually stop the manual counts while guaranteeing the distrust survives underground.

**Question 12 (moderate) — Rating exercise: documentation debt surfaced by an audit.**
An internal audit of your area finds that a third of your team's data models lack the required documentation, concentrated in models built during last year's urgent programme. The audit report is due to your director in two weeks. Rate each response independently on a scale from highly counterproductive to highly effective.

A) Draft a response committing to a realistic remediation plan: triage the undocumented models by usage and risk, set a documentation standard-and-template refresh so the gap does not recur, schedule the backfill across coming sprints, and give the director an honest completion date with progress checkpoints.
B) Direct the team to backfill all missing documentation before the report lands, pausing current sprint commitments without telling stakeholders why.
C) Challenge the audit's scope, noting the models in question predate the current documentation standard.
D) Accept the finding and note that the gap traces to a period when delivery was prioritised over documentation — then use that fact to argue for explicit documentation time in future programme plans.

**Ratings: A — highly effective. D — effective. C — counterproductive. B — highly counterproductive.**
**Explanation:** A is the complete senior response: it accepts the finding, sequences remediation by risk rather than alphabetically, fixes the system (template and standard refresh) so the debt does not regrow, and treats the director as an adult with an honest date — "ensure documentation of data meets standards" pursued as a plan rather than a scramble. D is effective as far as it goes — the causal honesty is valuable and converting the finding into future programme-planning leverage is genuinely senior thinking — but alone it explains the debt without retiring it; paired with A it would be ideal. C is counterproductive: even where technically arguable, contesting scope reads as defensiveness, spends credibility on avoiding a finding rather than fixing a real gap (users still cannot understand those models), and audits challenged on technicalities tend to return wider. B is highly counterproductive twice over: it deceives the audit's timeline (documentation authored in a fortnight's panic misrepresents the state the audit measured), and it silently breaks commitments to stakeholders — compounding a documentation failure with a transparency failure, the one kind of failure a public sector data team can least afford.

### Preparation tips

- **Anchor on the role's values, not your instincts alone.** Before the assessment, re-read your role profile and the public sector principles it sits within: user needs, honesty and transparency, collaboration, accessibility and inclusion. The strongest options serve those; the weakest sacrifice them for speed, comfort, or appearances.
- **Look for the option that addresses the root issue.** Across every scenario above, the winning option treats the cause (unmet need, missing process, broken trust) while managing the symptom. Options that only suppress the symptom rate poorly.
- **Check each option for hidden costs.** Rescue-the-artefact options cost development; quiet-fix options cost trust; escalate-first options cost relationships; do-nothing options cost users. Rating options means pricing these.
- **Practise the "most and least" discipline.** Identifying the least effective option is often easier and worth equal marks: look for deception, passivity, disproportion, or knowingly leaving users exposed.
- **Rehearse with a peer.** Talk through two or three scenarios with another senior engineer and argue the ratings. Divergence in your answers is exactly where your judgement will sharpen fastest.
- **Answer as the role, at your level.** The question is not "what would a heroic individual contributor do?" but "what does the senior engineer who oversees, coaches, and advocates do?" Your added value is usually in sequencing, transparency, and growing others.

### Common pitfalls

- **Answering idealistically instead of effectively.** "Consult everyone about everything" sounds virtuous but rates poorly when the scenario needs calibrated urgency. Effectiveness is context-fit, not maximal virtue.
- **Selecting passive options.** Deferring, escalating without acting, or waiting for a board to rule are recurring least-effective patterns — especially where users are currently exposed to wrong or stale data.
- **Ignoring the culture you are being assessed for.** UK government digital culture prizes working in the open, user needs, and multidisciplinary collaboration. Options that hoard information, bypass users, or win by seniority run against the grain.
- **Protecting artefacts at the expense of people.** Rebuilding a junior's work overnight, absorbing credit, or hoarding interesting work all "solve" the immediate problem while corroding the team — assessments at senior level test whether you notice.
- **Choosing deception-shaped shortcuts.** Any option in which someone who reasonably expects to know is kept unknowing — a stakeholder, an auditor, a report's owner — is almost always the least effective, however efficient it looks.
- **Over-escalating.** Escalation is a tool, not a reflex. The senior judgement being tested is usually: act proportionately now, escalate transparently when the trade-off exceeds your authority.


## Conclusion

You have now worked through four complete, role-specific assessment resources: cognitive ability exercises built from the models, pipelines, and review queues you oversee; numeric reasoning drawn from the quality scores, capacity plans, and cost cases you present; verbal reasoning grounded in the standards, emails, and governance texts you read critically every week; and situational judgement scenarios that test the leadership behaviours — coaching, facilitation, transparency, advocacy — that define the senior analytics engineer role.

If one message carries across all four sections, it is this: these assessments measure things you already do. Reviewing a star schema for grain violations is pattern recognition. Reconciling row counts through a pipeline is numeric reasoning. Parsing whether a clause governs one requirement or two is verbal reasoning. Deciding how to handle a defect found after sign-off is situational judgement. The assessment setting adds time pressure and unfamiliar formats — both of which respond well to exactly the kind of deliberate practice you have just done.

For your next steps: revisit the questions you found hardest after a few days' gap, and re-attempt them cold before re-reading the explanations. Practise little and often rather than in single long sittings. Where a section exposed a genuine soft spot — perhaps weighted averages, or the Cannot Say discipline, or your instincts around escalation — fold it into your development plan and, better still, into your coaching conversations: teaching these skills to the engineers you mentor is the most reliable way to deepen your own command of them.

Finally, keep perspective. Psychometric results are one input among many; they sit alongside your delivery record, your stakeholder relationships, and the engineers you have developed — evidence no timed test can capture. Prepare well, rest properly before any real assessment, read every question as carefully as you would read a specification, and trust the professional judgement you exercise every day. You are well equipped for this. Good luck — and keep building.

