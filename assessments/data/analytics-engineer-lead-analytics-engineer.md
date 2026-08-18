# Analytics Engineer (Lead Analytics Engineer) - Psychometric Assessment Resources

## Introduction

Welcome. This document is a practical, role-specific preparation resource for you as a lead analytics engineer working within the UK Government Digital and Data (GDAD) Profession Capability Framework. It has been written for you personally — someone who leads the design and deployment of data models for analysis, who guides a team of analytics engineers, and who sits at the junction between organisational processes, stakeholder needs, and the technical craft of data modelling, transformation, and documentation.

Psychometric assessments are structured, standardised exercises that measure the mental capabilities and judgement you use every day: interpreting a dense specification, spotting an inconsistency in a data model, reasoning through pipeline metrics under time pressure, or choosing the wisest course of action when a senior stakeholder and your team pull in different directions. Employers — including government departments and their recruitment partners — use these assessments because they are strong, evidence-based predictors of on-the-job performance, and because they give every candidate the same fair, objective opportunity to demonstrate capability regardless of background.

For a role at your level, assessments are rarely about abstract puzzles. They are about whether you can do, quickly and accurately, the kinds of thinking your role genuinely demands: leading reviews of complex data models, defining data requirements with stakeholders across the organisation, setting standards for communication and documentation, coordinating problem investigations, and communicating fluently between the technical and the non-technical.

This document is organised into four assessment sections, each mirroring a widely used assessment type:

1. **Workplace job-specific cognitive assessment** — pattern recognition, logical deduction, error checking, prioritisation, and problem solving using the artefacts you really handle: data models, transformation pipelines, test suites, and metadata repositories.
2. **Workplace job-specific numeric reasoning assessment** — tables, percentages, ratios, budgets, capacity figures, and performance metrics drawn from analytics engineering work.
3. **Workplace job-specific verbal reasoning assessment** — dense role-relevant passages (standards documents, policies, emails, review reports) followed by True / False / Cannot Say and comprehension questions.
4. **Workplace job-specific situational judgement assessment** — realistic workplace dilemmas involving your stakeholders, your team, and the values of UK public sector delivery.

Each section explains what the assessment measures, maps it explicitly to the skills in your role profile, provides a substantial bank of worked practice questions at varied difficulty levels, and closes with preparation tips and common pitfalls.

How to use this document: work through it actively, not passively. Attempt each practice question under a self-imposed time limit before reading the answer. Then study the worked explanation, notice where your reasoning diverged, and reflect on how the same thinking shows up in your daily work. Used this way, the document serves three purposes at once — assessment practice, self-reflection on your professional strengths, and structured preparation for selection or development processes. Good luck — you already use these capabilities every day; this resource simply helps you demonstrate them at your best.

## Advisory

"This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff."

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive ability assessment is a targeted psychometric test designed to measure the exact mental processes needed for your role — not a generic IQ test, but a set of practical exercises built from the everyday tasks and data formats of analytics engineering leadership. Questions typically present artefacts you genuinely handle — dependency graphs of transformation models, star schema designs, data quality rule sets, review checklists, metadata records — and ask you to find the pattern, deduce the consequence, spot the error, or choose the priority.

The format is usually online and timed, most commonly 15 to 30 minutes, with objective scoring against a benchmark or norm group. Modern platforms often include short ungraded practice questions before the real test begins, and some adapt question difficulty based on your previous answers. Employers usually receive a breakdown of speed versus accuracy rather than a single score, so working both quickly and carefully matters. Questions used in real recruitment are validated to ensure they predict job success without bias — which is exactly why they focus on realistic work rather than abstract trivia.

For a lead analytics engineer, cognitive ability assessment matters because your role multiplies your thinking across a team. When you review another engineer's dimensional model, you are error checking. When you trace why a downstream dashboard broke after an upstream schema change, you are performing logical deduction across a dependency graph. When you decide which of five competing requests your team tackles first, you are prioritising under constraint. A strong cognitive assessment performance signals that you can do these things reliably and at pace.

### What it measures for your role

The assessment dimensions map directly onto the skills named in your role profile:

- **Data modelling, cleansing and enrichment** — pattern recognition and error checking within complex data models: spotting a fan trap in a star schema, a grain mismatch in a fact table, or a slowly changing dimension handled inconsistently against your standards.
- **Data analysis and synthesis** — logical deduction when profiling a complex source system or conforming multiple sources into one model: which join keys are safe, which records will drop, which anomaly explains the discrepancy.
- **Programming and build (data engineering)** — error checking of moderate-to-complex transformation code and scripts against agreed specifications, and reasoning about what a change will do before it runs.
- **Testing** — defining test conditions from requirements, identifying issues and risks, and deducing which failing test isolates a defect.
- **Problem management** — structured problem solving: coordinating an investigation, distinguishing symptoms from root causes, and choosing preventive measures that stop recurrence.
- **Metadata management** — consistency checking across a metadata repository: definitions, lineage, and ownership records that must agree with each other and with the physical models.
- **Communicating between the technical and non-technical** — prioritisation and framing: deciding what matters most and what to escalate, which is a cognitive act before it is a communication act.

### Practice questions

**Question 1 (easy) — Dependency deduction.**
Your team's transformation pipeline has these dependencies: model `stg_payments` feeds `int_payments_enriched`; `stg_customers` feeds `int_customer_profile`; both `int_payments_enriched` and `int_customer_profile` feed `fct_transactions`; `fct_transactions` feeds the `finance_dashboard` and the `fraud_report`. Overnight, `stg_customers` failed to build. Which downstream artefacts are affected?

A) Only `int_customer_profile`
B) `int_customer_profile`, `fct_transactions`, `finance_dashboard`, and `fraud_report`
C) `int_customer_profile` and `fct_transactions` only
D) Everything, including `stg_payments` and `int_payments_enriched`

**Correct answer: B.**

**Explanation:** Follow the directed dependency graph downstream from the failure. `stg_customers` feeds `int_customer_profile`, which feeds `fct_transactions`, which feeds both the dashboard and the report — so all four are affected. `stg_payments` and `int_payments_enriched` sit on a parallel branch upstream of the failure's influence and build independently, so D over-includes. C stops too early: anything consuming `fct_transactions` inherits the failure. This is exactly the deduction you perform when triaging an overnight build failure before your stakeholders start their day.

**Question 2 (easy) — Error checking a standard.**
Your team's naming standard states: staging models are prefixed `stg_`, intermediate models `int_`, fact tables `fct_`, and dimension tables `dim_`; all names are lower case with underscores. During a review you see this list of new models submitted by a team member: `stg_hmrc_receipts`, `int_ReceiptsEnriched`, `fct_receipts_daily`, `dim_taxpayer`, `stg_Case_Notes`. How many models violate the standard?

A) 1
B) 2
C) 3
D) 4

**Correct answer: B.**

**Explanation:** Check each name against both rules (prefix and lower-case-with-underscores). `stg_hmrc_receipts` passes. `int_ReceiptsEnriched` fails: correct prefix, but mixed case and no underscore separation. `fct_receipts_daily` passes. `dim_taxpayer` passes. `stg_Case_Notes` fails: correct prefix, but capital letters. Two violations. Systematic, rule-by-rule checking — rather than an impressionistic skim — is the habit that makes your model reviews reliable, and it is precisely what error-checking items measure.

**Question 3 (moderate) — Grain reasoning.**
A fact table `fct_appointments` is declared at the grain of "one row per appointment". A team member adds a column `total_appointments_per_clinic_per_month`. A dashboard built on this table starts double-counting monthly totals. What is the most likely cause?

A) The new column changed the table's grain
B) The new column repeats an aggregate value on every appointment row, and the dashboard is summing it
C) The dashboard is joining to a dimension table incorrectly
D) The fact table has duplicate appointment rows

**Correct answer: B.**

**Explanation:** Adding a column does not change a table's grain (rows are unchanged), so A is imprecise. The named column is a monthly aggregate stamped onto every appointment row; if a dashboard sums it across rows, each clinic-month's total is counted once per appointment in that month — a classic repeated-aggregate error, so B fits the symptom exactly. C and D could cause double counting in general but nothing in the scenario points to them, and the timing (the problem started when the column was added) points squarely at B. In Kimball terms, aggregates that do not match the declared grain do not belong on the fact table — this is the reasoning you apply when reviewing complex models for adherence to standards.

**Question 4 (moderate) — Conformed dimension logic.**
You are conforming two source systems into one model. Source A records citizens with a 9-character reference; Source B uses a 10-character reference that equals Source A's reference with a leading zero added. A team member proposes joining on the raw reference fields directly. What will happen, and what is the correct fix?

A) The join will work; no fix needed
B) The join will return zero matches; pad Source A's reference with a leading zero (or strip Source B's) before joining
C) The join will return duplicates; deduplicate Source B first
D) The join will work only for references beginning with zero

**Correct answer: B.**

**Explanation:** A 9-character string never equals a 10-character string, so a raw equality join matches nothing — the model would silently produce an empty or drastically reduced result. The fix is to standardise the key: pad one side or trim the other, ideally in a staging model so the conformed key is defined once and reused. C invents a duplication problem the scenario does not describe; D reverses the logic (references beginning with zero in Source B still differ in length from their Source A counterparts). Profiling both sources before designing the join — checking lengths, formats, and null rates — is core data analysis and synthesis, and this item tests whether you deduce the consequence before running the code.

**Question 5 (moderate) — Test condition selection.**
A specification says: "The `dim_school` table must contain exactly one current row per school URN; closed schools remain in the table flagged `is_open = false`." Which set of test conditions gives the best coverage of this requirement?

A) Test that the table is not empty
B) Test uniqueness of URN across all rows, and test that `is_open` is never null
C) Test uniqueness of URN among rows where the row is marked current, test that closed schools are present with `is_open = false`, and test that `is_open` is never null
D) Test that every school in the source appears in the table

**Correct answer: C.**

**Explanation:** Read the requirement precisely: uniqueness applies to *current* rows per URN, not all rows — a slowly changing dimension may legitimately hold multiple historical rows per URN, so B's blanket uniqueness test would fail correct data. The requirement also asserts retention of closed schools with a specific flag value, so a presence-plus-flag test is needed, and a not-null test on the flag guards the boundary. A is far too weak; D tests completeness, which is worthwhile but does not address the stated requirement. Translating requirements into precise test conditions — no stronger and no weaker than the specification — is exactly the Testing skill at your level, where you review requirements and define test conditions for the team.

**Question 6 (moderate) — Pattern recognition in run history.**
Your nightly pipeline's total run time over ten nights (in minutes) was: 42, 43, 44, 43, 58, 44, 45, 59, 45, 60. Which statement best characterises the pattern?

A) Run time is steadily increasing every night
B) Run time is stable around 43–45 minutes with a recurring spike roughly every third night, and the spikes themselves are growing
C) Run time is random with no pattern
D) Run time doubled halfway through the period

**Correct answer: B.**

**Explanation:** Separate the sequence into its components. Nights 1–4, 6–7, and 9 cluster tightly at 42–45 minutes: a stable baseline. Nights 5, 8, and 10 show 58, 59, 60 — spikes at a roughly three-night cadence, each slightly higher than the last. A is wrong because most consecutive nights barely move; C ignores an obvious structure; D misdescribes isolated spikes as a level shift. Recognising this pattern would lead you, as the person coordinating problem investigation, to ask what runs every third night (perhaps a full-refresh model or a weekly-ish source extract) and why its cost is creeping upward — pattern recognition is the first step of anticipating problems before they become incidents.

**Question 7 (moderate) — Prioritisation under constraint.**
It is 08:30. Four items compete for your attention: (1) the overnight build failed, so the department's daily performance dashboard is stale — the data is from yesterday and clearly timestamped; (2) a team member's pull request implementing a new statutory reporting model is blocked awaiting your review, with a legally fixed submission deadline tomorrow; (3) a senior stakeholder has emailed asking for a meeting "sometime this week" about a new data requirement; (4) your metadata repository shows three model descriptions are out of date. What is the most defensible order of attention?

A) 1, 2, 3, 4
B) 2, 1, 3, 4
C) 3, 2, 1, 4
D) 1, 4, 2, 3

**Correct answer: B.**

**Explanation:** Prioritise by consequence and deadline, not by noise. Item 2 carries a legally fixed deadline tomorrow and is blocked *on you personally* — reviewing it (or delegating the review) unblocks another person and protects a statutory obligation. Item 1 matters, but the dashboard is clearly timestamped, so users are not being misled; also, as a lead you can direct a team member to investigate the failure in parallel rather than doing it yourself — leadership means allocating, not hoarding. Item 3 explicitly allows scheduling later in the week. Item 4 is routine maintenance. A is the instinctive "fix the breakage first" answer, but it ignores both the statutory deadline and your ability to delegate. This mirrors the judgement your role level demands: leading and supporting the team rather than personally firefighting everything.

**Question 8 (hard) — Root cause deduction.**
A data quality alert fires: 4% of rows in `fct_grants` have a null `local_authority_key`. You establish these facts: (i) the null rate was 0% until Tuesday; (ii) on Tuesday, the grants source system added a new grant type, "emergency support", administered nationally rather than by local authorities; (iii) the dimension `dim_local_authority` was last updated a month ago; (iv) the join in the transformation uses an inner join for standard grants and produces nulls only via a left join fallback. What is the most likely root cause?

A) `dim_local_authority` is stale and missing new authorities
B) The transformation code has a bug introduced on Tuesday
C) The new national grant type legitimately has no local authority, and the model design never anticipated grants without one
D) The source system is sending corrupted keys

**Correct answer: C.**

**Explanation:** Deduce from the conjunction of facts. The timing (fact i) coincides exactly with the source-side change (fact ii), and the new grant type is *nationally* administered — meaning there genuinely is no local authority to link. Fact (iii) makes A unlikely: no new authorities have been created, and stale dimensions would not suddenly matter on Tuesday. Fact (iv) shows the code is behaving as designed, not as broken, weakening B; nothing suggests corruption, ruling out D. The root cause is a modelling assumption invalidated by organisational change — every grant has a local authority — and the fix is a design decision (for example, a "National" member row in the dimension), not a code patch. Distinguishing "the code is wrong" from "the assumption is wrong" is the heart of problem management at lead level, and it is what your role means by refining requirements in response to changes in the organisation.

**Question 9 (hard) — Logical deduction from standards.**
Your team's standards state: (i) every fact table must declare its grain in the model documentation; (ii) every model with declared grain must have an automated uniqueness test on the grain's key combination; (iii) any model lacking a required test cannot be promoted to production. A colleague tells you: "Model X is in production." Which of the following must be true?

A) Model X is a fact table
B) If Model X is a fact table, it has an automated uniqueness test on its grain keys
C) Model X has a declared grain
D) Model X has no test failures

**Correct answer: B.**

**Explanation:** Chain the conditionals. If X is a fact table, then by (i) it declares its grain; by (ii) declared grain implies a required uniqueness test; by (iii) production status implies no required test is missing — so the test exists. That chain is airtight, making B necessarily true. A reverses the logic: production models need not be fact tables (dimensions and staging models may be promoted too). C fails for the same reason — only fact tables are obliged to declare grain. D overreaches: the standards govern the *existence* of tests for promotion, and say nothing about whether tests are currently passing after promotion. Assessments use this structure to test whether you apply rules exactly as written — the same discipline you use when your team's promotion checklist is challenged.

**Question 10 (hard) — Error checking transformation logic.**
A team member's script is meant to implement this specification: "Flag a payment as `late` if it was received more than 30 days after the invoice date, excluding invoices that were formally disputed." The code reads: flag `late` when `received_date - invoice_date >= 30 AND dispute_flag = false`. Which two errors should your review flag?

A) The comparison should be `> 30` not `>= 30`; and disputed invoices should be excluded from the population, not merely never flagged late
B) The comparison should be `> 30` not `>= 30`; and `dispute_flag = false` should be `dispute_flag = true`
C) The date subtraction is backwards; and the dispute condition is redundant
D) There are no errors; the code matches the specification

**Correct answer: A.**

**Explanation:** Two subtle mismatches. First, "more than 30 days" means strictly greater than 30, so `>= 30` wrongly flags payments received exactly 30 days after invoicing — an off-by-one boundary error that a good test condition (a payment at exactly 30 days) would catch. Second, the specification says disputed invoices are *excluded* — they should not be in the flagged-or-not population at all. The code instead keeps them in the population and marks them not-late, which silently distorts any "percentage late" metric built downstream: the denominator is inflated. B's second correction inverts the intended logic entirely; C invents errors that are not there. Spotting the difference between "never flag" and "exclude" is exactly the precision your role's review responsibilities demand, because downstream analysts will trust the metric without re-reading the code.

**Question 11 (hard) — Metadata consistency checking.**
Your metadata repository holds four records about the same model. Record 1: "`fct_road_maintenance` — owner: Highways Data Team; grain: one row per maintenance job; source: ROADWORKS system." Record 2 (lineage): "`fct_road_maintenance` is built from `stg_roadworks` and `stg_contractors`." Record 3 (column dictionary): "`contractor_sla_band` — derived from contractor contract terms in the CONTRACTS system." Record 4 (source register): "Sources feeding analytics models: ROADWORKS, CONTRACTORS." Which inconsistency should you raise?

A) Record 1 lists only ROADWORKS as source, but Records 2 and 3 indicate contractor data (and possibly the CONTRACTS system) also feed the model
B) Record 2 contradicts Record 4
C) The grain in Record 1 contradicts the lineage in Record 2
D) There is no inconsistency

**Correct answer: A.**

**Explanation:** Cross-check the records pairwise. Record 2's lineage shows `stg_contractors` feeding the model, and Record 3 says a column derives from the CONTRACTS system — yet Record 1 declares ROADWORKS as *the* source. Either Record 1 is incomplete, or Record 3 misattributes the derivation, and possibly the source register (Record 4, which lists CONTRACTORS but not CONTRACTS) needs reconciling too — but the direct, demonstrable inconsistency is Record 1's single-source claim versus the multi-source evidence, so A is the finding to raise. B is wrong because Records 2 and 4 are compatible (staging models plausibly map to registered sources). C confuses unrelated attributes: grain and lineage describe different things and cannot contradict each other here. Designing a repository where such contradictions surface automatically — and coaching less experienced team members to keep records consistent — is your metadata management skill in action.

**Question 12 (hard) — Problem solving with constraints.**
Two models must both be rebuilt before 07:00. Model P takes 50 minutes and must start after its source lands at 05:00. Model Q takes 80 minutes, must start after its source lands at 04:30, and cannot run at the same time as P because both saturate the warehouse. Can both finish by 07:00, and what schedule achieves it?

A) No — the combined runtime exceeds the available window
B) Yes — run Q at 04:30–05:50, then P at 05:50–06:40
C) Yes — run P at 05:00–05:50, then Q at 05:50–07:10
D) Yes — run both in parallel from 05:00

**Correct answer: B.**

**Explanation:** Test the orderings. Q first: starts at its earliest allowed time 04:30, runs 80 minutes, finishes 05:50; P starts 05:50 (after its own 05:00 source constraint is already satisfied), runs 50 minutes, finishes 06:40 — inside the deadline. P first (option C): P runs 05:00–05:50, Q then runs 05:50–07:10 and misses the deadline by ten minutes. D violates the no-parallelism constraint outright. A is wrong because 130 minutes of work fits the 04:30–07:00 window (150 minutes) provided the longer, earlier-available job goes first. The general principle — schedule the job with the earlier release time and longer duration first when resources are exclusive — is the same reasoning you apply when sequencing your team's builds, and assessments reward candidates who test each option against every constraint rather than the first plausible one.

**Question 13 (moderate) — Odd one out in modelling practice.**
Four design decisions were made across your team's models. Which one is inconsistent with dimensional modelling best practice as popularised by Kimball?

A) Storing the fact table at the most granular level available (one row per event)
B) Creating conformed dimensions shared across fact tables
C) Storing descriptive attributes (names, categories, bands) directly on the fact table as wide text columns
D) Using surrogate keys to link facts to dimensions

**Correct answer: C.**

**Explanation:** Kimball-style dimensional modelling puts descriptive, textual context into dimension tables and keeps fact tables lean: keys plus measures at a declared grain. A (atomic grain), B (conformed dimensions enabling cross-process analysis), and D (surrogate keys insulating the model from source-key changes) are all canonical practice. C bloats the fact table, duplicates text on millions of rows, prevents attribute reuse across facts, and makes slowly changing attribute handling impossible. Recognising which practice breaks the pattern is precisely the judgement you exercise when reviewing other analytics engineers' work against the standards you have created.

**Question 14 (moderate) — Sequencing a standards rollout.**
You are rolling out a new documentation standard across your team's models. The steps are: (i) publish the standard; (ii) run a workshop so the team understands it; (iii) update the model templates so new models comply automatically; (iv) retrofit the top twenty existing models; (v) add an automated check that blocks non-compliant changes. A team member proposes the order: v, iv, i, ii, iii. What is the main flaw in that proposal?

A) Retrofitting should always come last
B) Enabling the blocking check before the standard is published, understood, and supported by templates will block the team's work against rules they have not seen and cannot easily follow
C) Workshops are unnecessary if the standard is written well
D) Templates should be updated before the standard is agreed

**Correct answer: B.**

**Explanation:** Trace the consequences of the proposed order. Turning on enforcement (v) first means every change is judged against a standard nobody has read (i and ii come later) and that the tooling does not yet help them meet (iii is last) — the team is blocked, trust in the standard is damaged, and delivery stalls. A sensible order is i, ii, iii, iv, v: publish, build understanding, make compliance easy, clean up the estate, then enforce. A states a rigid rule that is not itself the flaw; C and D are simply poor practice. This item tests ordering logic — recognising which dependencies are real — and mirrors your responsibility for creating standards and defining ways of working in a manner the team can actually adopt.

### Preparation tips

- **Practise on your own artefacts.** Before the assessment, spend time consciously reasoning about dependency graphs, review checklists, and test suites at work: articulate *why* a model passes or fails review. Verbalising your reasoning strengthens exactly the deduction pathways these tests measure.
- **Work the constraint, not the vibe.** At lead level, questions are built so the plausible-sounding answer and the correct answer differ by one constraint. Read every condition, then check each option against all of them, as you did in Questions 9 and 12.
- **Manage the clock like a pipeline.** With 15–30 minutes and objective scoring on both speed and accuracy, treat each question like a job in a schedule: if one exceeds its time budget, park it and return. You already do this when triaging incidents.
- **Do the ungraded practice items properly.** Use them to learn the interface — how to flag questions, how the timer displays — so no cognitive capacity is wasted on mechanics.
- **Rest and environment matter.** These assessments measure processing under time pressure; sleep, a quiet room, and a large screen for reading diagrams and tables are legitimate performance enhancers.

### Common pitfalls

- **Answering from experience instead of from the question.** You have deep knowledge of real systems; the test rewards reasoning strictly from the information given. If the question says the standard requires X, apply X even if your team does Y.
- **Impressionistic error checking.** Skimming a list of model names or a code snippet and "feeling" that it is fine. Check rule by rule, item by item — the test is calibrated to catch skimmers.
- **Getting anchored on the first plausible option.** Distractors are engineered to be almost right. Confirm your choice survives every stated fact before moving on.
- **Time sink questions.** Spending five minutes on one hard deduction while three easy questions go unanswered. Your speed-versus-accuracy profile is reported; a stranded hard question costs more than a skipped one.
- **Ignoring diagram and table labels.** Misreading which direction a dependency arrow points, or which column a test refers to, converts a solvable question into a guess. Slow down for ten seconds on the artefact before reading the options.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment evaluates your ability to analyse, interpret, and make sound decisions using numerical data of the kind your role really handles. It is business mathematics, not abstract algebra: percentages, ratios, rates of change, cost-benefit comparisons, and capacity calculations, presented through tables, charts, budgets, and performance dashboards. Most assessments allow or provide an on-screen calculator, because the skill being measured is interpretation — extracting the right figures, applying the right operation, and sanity-checking the result — rather than mental arithmetic. Time limits are strict, typically around a minute to ninety seconds per question, which simulates the reality of making defensible numerical judgements at working pace.

For a lead analytics engineer, numbers are the fabric of the job. You quantify data quality (null rates, match rates, duplication percentages), pipeline performance (run times, failure rates, cost per run), team capacity (review throughput, sprint allocation), and the business case for innovation (licence costs versus engineering hours saved). When you present to stakeholders across the organisation, your credibility rests on numerical claims that survive scrutiny. When you review a team member's analysis of a source system, you must spot the percentage that cannot be right. This assessment measures precisely that fluency.

Expect question inputs such as: a table of model run times and warehouse costs across environments; a data quality summary comparing sources before and after conforming; a team capacity plan; a budget for tooling and platform spend; or a dashboard of test pass rates over several releases. Each question asks for a specific derived figure or a comparison-based decision.

### What it measures for your role

Each numeric dimension corresponds to skills named in your role profile:

- **Data analysis and synthesis** — computing and comparing profiling metrics: null rates, distinct counts, match rates across sources being conformed into a single model.
- **Data modelling, cleansing and enrichment** — quantifying data quality against standards: what percentage of rows meet the interoperability rules, how a cleansing step changes record counts, whether a model's growth is sustainable.
- **Problem management** — trend and rate calculations on incidents and failures: is the failure rate improving, what is the mean time to resolve, which preventive measure gives the biggest reduction per unit effort.
- **Testing** — pass-rate arithmetic: coverage percentages, defect detection rates, and how results change between releases.
- **Data innovation** — cost-benefit reasoning: comparing tool licence costs against saved engineering hours, and judging when adoption pays back.
- **Communicating between the technical and non-technical** — turning raw figures into honest, proportionate statements ("a 40% reduction" versus "from 5 to 3 failures") that manage stakeholder expectations accurately.
- **Programming and build (data engineering)** — capacity and scheduling arithmetic: run durations, windows, and throughput of the kind you use when sequencing builds.

### Practice questions

**Question 1 (easy) — Null rate percentage.**
You profile a source table of 250,000 citizen records. The `postcode` column contains 12,500 nulls. What is the null rate, and what is the populated rate?

A) 5% null; 95% populated
B) 12.5% null; 87.5% populated
C) 4% null; 96% populated
D) 2.5% null; 97.5% populated

**Correct answer: A.**

**Explanation:** Null rate = 12,500 ÷ 250,000 = 0.05 = 5%. Populated rate = 100% − 5% = 95%. A quick sanity check: 10% of 250,000 would be 25,000, so 12,500 is exactly half of that — 5%. Profiling metrics like this are the first numbers you compute in source system analysis, and assessments begin with items like this to confirm you convert counts to percentages quickly and without error.

**Question 2 (easy) — Percentage change in run time.**
After your team refactors a transformation model, its nightly run time falls from 48 minutes to 36 minutes. What is the percentage reduction?

A) 12%
B) 20%
C) 25%
D) 33%

**Correct answer: C.**

**Explanation:** Reduction = 48 − 36 = 12 minutes. Percentage reduction = 12 ÷ 48 = 0.25 = 25%. The classic trap is D: 12 ÷ 36 = 33%, which divides by the *new* value instead of the original. Percentage change is always relative to the starting figure. When you report optimisation gains to stakeholders, this distinction is the difference between an accurate claim and an inflated one.

**Question 3 (moderate) — Match rate across conformed sources.**
You are conforming two sources into a single customer model. Source A has 180,000 records; Source B has 150,000 records. After standardising keys, 132,000 records match between the two sources. What percentage of Source B records remain unmatched?

A) 12%
B) 10%
C) 26.7%
D) 18%

**Correct answer: A.**

**Explanation:** Unmatched in Source B = 150,000 − 132,000 = 18,000. As a percentage of Source B: 18,000 ÷ 150,000 = 0.12 = 12%. Option C (48,000 ÷ 180,000) muddles populations by using Source A's unmatched count and denominator; option D mistakes the raw count (18,000) for a percentage. Reading *which population* the question asks about is half the skill — exactly as it is when you report match rates for a conformed model and must be precise about which source the percentage refers to.

**Question 4 (moderate) — Weighted data quality score.**
Your data quality standard scores each dataset on three dimensions: completeness (weight 50%), validity (weight 30%), and timeliness (weight 20%). A dataset scores 90 for completeness, 70 for validity, and 60 for timeliness. What is its weighted quality score?

A) 73.3
B) 78
C) 76
D) 80

**Correct answer: B.**

**Explanation:** Weighted score = (90 × 0.5) + (70 × 0.3) + (60 × 0.2) = 45 + 21 + 12 = 78. Option A is the unweighted mean (220 ÷ 3 = 73.3), the most common error when candidates ignore the weights. Weighted scoring appears constantly in your work — quality scorecards, prioritisation matrices, vendor comparisons — and the arithmetic habit is always the same: multiply each score by its weight, then sum.

**Question 5 (moderate) — Deduplication effect on record counts.**
A cleansing step removes duplicates from a 2,400,000-row staging table. Profiling shows 8% of rows are duplicates of another retained row and will be deleted. The deduplicated table then gains 60,000 new rows in the month after go-live. How many rows does it hold at the end of that month?

A) 2,268,000
B) 2,208,000
C) 2,148,000
D) 2,328,000

**Correct answer: A.**

**Explanation:** Duplicates removed = 2,400,000 × 0.08 = 192,000. After cleansing: 2,400,000 − 192,000 = 2,208,000. After a month of growth: 2,208,000 + 60,000 = 2,268,000. Option B forgets the growth; option C subtracts the growth instead of adding; option D applies 8% to the wrong base (subtracting only 132,000). Multi-step questions like this reward writing intermediate figures down — the same discipline as documenting each transformation step so the pipeline is auditable.

**Question 6 (moderate) — Test pass rates across releases.**
Your team's automated test suite results over three releases: Release 1 — 320 tests, 288 passed. Release 2 — 360 tests, 333 passed. Release 3 — 400 tests, 356 passed. Which release had the highest pass rate, and what was it?

A) Release 3, at 89%
B) Release 2, at 92.5%
C) Release 1, at 90%
D) Release 2, at 90.25%

**Correct answer: B.**

**Explanation:** Compute each rate: Release 1 = 288 ÷ 320 = 90%. Release 2 = 333 ÷ 360 = 92.5%. Release 3 = 356 ÷ 400 = 89%. Release 2 is highest at 92.5%. Note the trap in the question's surface: Release 3 has the most *passing tests* (356) but the lowest *rate*. Raw counts and rates diverge whenever denominators change — a distinction you draw whenever you analyse and report test activities and results for a growing test suite.

**Question 7 (moderate) — Warehouse cost per run.**
Your pipeline's monthly warehouse compute bill is £5,400. The pipeline runs nightly (30 runs in the month), plus 15 additional ad-hoc full refreshes that month, each costing twice as much compute as a nightly run. What does one nightly run cost?

A) £120
B) £180
C) £90
D) £135

**Correct answer: C.**

**Explanation:** Let a nightly run cost x. Ad-hoc refreshes cost 2x each. Total: 30x + 15(2x) = 30x + 30x = 60x = £5,400, so x = £90. Option A divides £5,400 by 45 runs, ignoring that ad-hoc runs cost double; option B divides by 30, ignoring the ad-hoc runs entirely. Setting up the equation before reaching for the calculator prevents both errors. This is exactly the unit-cost reasoning you use when someone proposes more frequent refreshes and you must quantify the platform cost of saying yes.

**Question 8 (hard) — Ratio reasoning for team capacity.**
Your team of analytics engineers spends time in the ratio 5 : 3 : 2 across building models, reviewing work, and supporting users. The team delivers 400 productive hours in a sprint. A new organisational commitment requires support hours to double, while total hours stay fixed and the build-to-review ratio stays 5 : 3. How many build hours does the team have after the change?

A) 200
B) 160
C) 150
D) 175

**Correct answer: C.**

**Explanation:** Currently: 5 + 3 + 2 = 10 parts across 400 hours, so one part = 40 hours — build 200, review 120, support 80. Support doubles to 160 hours, leaving 400 − 160 = 240 hours for build and review in the ratio 5 : 3 (8 parts, 30 hours per part): build = 5 × 30 = 150, review = 3 × 30 = 90. Option A is the pre-change figure; option B wrongly applies the doubling elsewhere; option D splits the remainder evenly-ish without honouring the ratio. Ratio reallocation under a fixed total is the arithmetic behind every capacity conversation you have when you define and improve your team's ways of working.


**Question 9 (hard) — Cost-benefit of tool adoption.**
You are evaluating a data transformation tool for the team. Licence cost: £18,000 per year. You estimate it saves each of your 6 analytics engineers 3 hours per week, and you cost an engineering hour at £45. Assuming 44 working weeks per year, what is the approximate annual net benefit of adoption?

A) £17,640
B) £35,640
C) £11,880
D) £53,640

**Correct answer: A.**

**Explanation:** Hours saved per year = 6 engineers × 3 hours × 44 weeks = 792 hours. Value = 792 × £45 = £35,640. Net benefit = £35,640 − £18,000 = £17,640. Option B is the gross saving with the licence cost forgotten; option C uses 22 weeks or halves the saving; option D adds the licence cost instead of subtracting it. This is the core arithmetic of your data innovation skill — identifying areas of innovation is only half the job; recognising the appropriate timing for adoption means being able to show, in defensible numbers, when the benefit clears the cost.

**Question 10 (hard) — Incident rate trend.**
Your problem management log shows data pipeline incidents per quarter: Q1 — 24 incidents over 1,200 runs; Q2 — 21 incidents over 1,400 runs; Q3 — 18 incidents over 1,500 runs. A stakeholder says "incidents have fallen by a quarter, so reliability is up 25%." What is the more accurate statement about the incident *rate* from Q1 to Q3?

A) The rate fell from 2.0% to 1.2%, a 40% relative reduction
B) The rate fell from 2.0% to 1.2%, a 0.8 percentage point reduction — both framings are worth giving
C) The rate fell 25%, as the stakeholder said
D) The rate rose because runs increased

**Correct answer: B.**

**Explanation:** Q1 rate = 24 ÷ 1,200 = 2.0%. Q3 rate = 18 ÷ 1,500 = 1.2%. That is a fall of 0.8 percentage points, which is a relative reduction of 0.8 ÷ 2.0 = 40%. The stakeholder's "25%" describes the raw incident count (24 → 18), which understates the improvement because run volume grew. Option A's figures are correct but option B is the better answer for your role: presenting both the percentage-point change and the relative change is how you manage expectations honestly when communicating between the technical and the non-technical — a single dramatic-sounding figure without its companion framing can mislead in either direction. Option D confuses denominator growth with rate growth.

**Question 11 (hard) — Storage growth projection.**
A conformed data model currently occupies 1.6 TB and is growing at 5% per month, compounding. The platform team has allocated 2.0 TB. Approximately how many whole months from now will the model first exceed its allocation?

A) 3 months
B) 5 months
C) 8 months
D) 12 months

**Correct answer: B.**

**Explanation:** Apply compound growth month by month: 1.6 × 1.05 = 1.680 (month 1); × 1.05 = 1.764 (month 2); × 1.05 = 1.852 (month 3); × 1.05 = 1.945 (month 4); × 1.05 = 2.042 (month 5). The model first exceeds 2.0 TB during month 5. Option A comes from treating 5% as simple growth on a misread base; option C or D come from arithmetic slips or using 5% per quarter. A useful sanity check: the target requires 25% total growth (2.0 ÷ 1.6 = 1.25), and compounding at 5% reaches ~27.6% after five periods. Projections like this let you anticipate problems — a problem management responsibility — rather than discover them when the pipeline fails on a full disk.

**Question 12 (hard) — Multi-source table interpretation.**
You receive this data quality summary for three sources feeding your conformed citizen model:

| Source | Records | Valid postcode | Valid date of birth | Duplicate rate |
|---|---|---|---|---|
| Benefits system | 400,000 | 92% | 98% | 3% |
| Housing system | 250,000 | 88% | 96% | 6% |
| Council tax system | 350,000 | 96% | 99% | 2% |

Your interoperability standard requires each source to contribute at least 220,000 records that have BOTH a valid postcode AND a valid date of birth (assume validity of the two fields is independent, and ignore duplicates). Which sources meet the requirement?

A) All three
B) Benefits and council tax only
C) Council tax only
D) Benefits only

**Correct answer: B.**

**Explanation:** With independence assumed, multiply the rates. Benefits: 400,000 × 0.92 × 0.98 = 360,640 — meets it. Housing: 250,000 × 0.88 × 0.96 = 211,200 — falls short of 220,000. Council tax: 350,000 × 0.96 × 0.99 = 332,640 — meets it. So B. The common error is adding or averaging the two validity percentages instead of multiplying, or checking only one field. Note also the deliberate red herring: the duplicate rate column is irrelevant because the question says to ignore it — extracting only the columns the question needs, under time pressure, is a skill the assessment measures directly, and one you use whenever you read a profiling report.

**Question 13 (moderate) — Review throughput.**
You personally review your team's model changes. Reviews take 40 minutes each on average, and you protect 6 hours per week for review work. The team currently raises 8 changes per week, expected to rise by 50% next quarter. How many review hours per week will you be short next quarter if nothing changes?

A) 2 hours
B) 1 hour 20 minutes
C) 4 hours
D) You will not be short

**Correct answer: A.**

**Explanation:** Next quarter's demand = 8 × 1.5 = 12 changes per week × 40 minutes = 480 minutes = 8 hours. Your protected capacity is 6 hours, so the shortfall is 2 hours per week. Option B is the shortfall at current volume plus a miscalculation (current demand is 8 × 40 = 320 minutes = 5 hours 20 minutes, which actually fits inside 6 hours — so today you are fine, confirming why D is tempting but wrong for *next quarter*). The leadership insight the numbers point to: delegate reviews to senior team members or streamline the checklist — which is exactly the kind of ways-of-working improvement your role level exists to make. Assessments reward candidates who compute the future state asked for, not the present one.

**Question 14 (hard) — Budget allocation across a programme.**
Your directorate allocates a £240,000 annual data platform budget across three cost lines in the ratio 4 : 3 : 1 (compute : storage : tooling). Mid-year, a 10% budget cut is imposed, but tooling is protected at its original amount because licences are contractually committed. If compute and storage absorb the whole cut while keeping their ratio to each other, what is the new annual compute allocation?

A) £108,000
B) £106,286 (approximately)
C) £96,000
D) £120,000

**Correct answer: B.**

**Explanation:** Original allocations: 8 parts across £240,000, so one part = £30,000 — compute £120,000, storage £90,000, tooling £30,000. The cut is 10% of £240,000 = £24,000, all absorbed by compute plus storage, whose combined pot falls from £210,000 to £186,000. They keep their 4 : 3 ratio (7 parts), so one part = £186,000 ÷ 7 ≈ £26,571, and compute = 4 parts ≈ £106,286. Option A wrongly takes 10% off compute alone; option C takes the cut twice; option D is the original figure. Protected lines, ratios preserved among the unprotected remainder — this is precisely how real public sector budget adjustments cascade, and the arithmetic pattern (subtract the protected amount, re-divide the remainder by the surviving ratio) is worth rehearsing until fluent.

**Question 15 (moderate) — Mean time to resolve.**
Five data problems were resolved by your team last month, taking 4, 6, 3, 15, and 7 hours respectively. A stakeholder asks for the average resolution time. Which statement gives the most honest summary?

A) The mean is 7 hours, and that is the whole story
B) The mean is 7 hours, but it is inflated by one 15-hour outlier; the median of 6 hours better represents a typical resolution
C) The median is 7 hours
D) The mean is 5 hours once the outlier is discarded

**Correct answer: B.**

**Explanation:** Mean = (4 + 6 + 3 + 15 + 7) ÷ 5 = 35 ÷ 5 = 7 hours. Sorted values are 3, 4, 6, 7, 15, so the median is 6 hours. The 15-hour case pulls the mean above four of the five actual observations, so quoting the mean alone (A) overstates typical performance, while silently discarding the outlier (D) understates the true workload and hides the very case problem management should investigate. B does what your communication skill demands: give the figure, name the distortion, and offer the more representative statistic — managing stakeholder expectations with numbers that are both accurate and fairly framed.

**Question 16 (hard) — Freshness service level.**
Your data model's service level target is that data is refreshed within 24 hours for at least 98% of days in a quarter (assume 90 days). So far, 61 days have elapsed and the target was missed on 2 of them. What is the maximum number of misses the team can afford across the remaining 29 days while still meeting the quarterly target — and is the target still achievable?

A) 1 further miss; still achievable
B) 2 further misses; comfortably achievable
C) 0 further misses; achievable only with a perfect remainder
D) The target is already impossible to meet

**Correct answer: D.**

**Explanation:** Work out the whole-day threshold first: 98% of 90 days = 88.2 days, and since only whole days count, at least 89 of the 90 days must meet the refresh target. That permits at most 90 − 89 = 1 missed day in the entire quarter. Two misses have already occurred, so even a perfect remaining 29 days yields 88 successful days out of 90 = 97.78%, which falls short of "at least 98%". The target is already unachievable, so D. Options A and B misread the allowance as 2 or 3 days (forgetting that 1.8 must be interpreted through whole-day counting), and C assumes the budget is merely exhausted rather than exceeded. The arithmetic here is trivial; the marks are earned by handling the fractional-allowance-versus-whole-day convention precisely. Real service level reporting turns on exactly such conventions — when you define freshness targets for your own team's models, stating the counting and rounding rules up front prevents this ambiguity from ever reaching a stakeholder meeting, and in an assessment you should always compute the exact threshold before judging achievability.

**Question 17 (easy) — Documentation coverage.**
Your metadata repository shows that 68 of your team's 80 production models have complete documentation entries. Your standard requires 95% coverage. How many additional models must be documented to meet the standard?

A) 8
B) 12
C) 4
D) 10

**Correct answer: A.**

**Explanation:** Required coverage = 95% of 80 = 76 models. Currently documented: 68. Additional models needed = 76 − 68 = 8. Option B is the total undocumented count (80 − 68 = 12), which overshoots the question asked; option C misreads the target as 90%. The pattern — compute the required absolute number from the percentage target, then take the gap from the current position — recurs across coverage, quality, and test-pass metrics, and it is the calculation you present when you set the team an improvement goal with a concrete, finite backlog rather than a vague percentage aspiration.

### Preparation tips

- **Rehearse the core four.** Percentage change, weighted averages, ratios, and compound growth cover most role-relevant questions. Practise until the *setup* (what to divide by what) is automatic, leaving the calculator to do the rest.
- **Always identify the denominator first.** Most wrong answers in numeric tests are right numerators over wrong denominators. Before calculating, say to yourself: "percentage *of what*?"
- **Write intermediate results.** Multi-step questions (cleansing then growth; reallocating ratios) are engineered so that skipping a step lands you on a distractor. Jot each stage, exactly as you would document each transformation step.
- **Use estimation to pre-screen options.** In Question 11, knowing 5% compounding needs roughly five periods to reach 25% lets you pick B before doing precise arithmetic. Estimation first, precision second, is faster and self-checking.
- **Practise reading tables under time.** Give yourself 90 seconds with a profiling report or platform cost dashboard at work and extract three figures. Speed at locating the right cell is trainable and pays directly in the test.
- **Bring calm.** At your level you interpret numbers daily; the timed format is the only unfamiliar element. A short breathing pause before starting genuinely improves accuracy on the first questions, which set your rhythm.

### Common pitfalls

- **Misreading scale qualifiers.** Confusing thousands with millions, monthly with quarterly figures, or minutes with hours. Every table header and axis label deserves two seconds of deliberate attention.
- **Dividing by the new value in percentage change.** The reduction from 48 to 36 is 25%, not 33%. This single error accounts for a large share of lost marks.
- **Over-calculating.** Performing long exact arithmetic when rounding would identify the correct option faster. If options are far apart, estimate; if close together, calculate.
- **Ignoring stated assumptions.** When a question says "assume independence" or "ignore duplicates", it is telling you which mathematical route to take. Fighting the assumption wastes time and derails the method.
- **Time sink questions.** A multi-stage cost-benefit item can consume four minutes. If you are two minutes in without a clear path, flag it, move on, and return — the marks for two easy questions outweigh one hard one.
- **Answering the present when the question asks about the future.** As in Question 13, projections are a favourite trap: compute the state the question actually asks for.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment evaluates how well you understand, analyse, and draw correct conclusions from written business information of the kind your role deals with daily. It mirrors the exact reading demands of analytics engineering leadership: data standards documents, transformation specifications, governance policies, stakeholder emails, review reports, and metadata definitions. Passages use real professional terminology, and the questions demand fact-based logic — you must answer strictly from the text provided, deliberately setting aside your own professional knowledge, however deep it is.

The dominant question format is **True / False / Cannot Say**: given a statement about the passage, you decide whether the passage confirms it (True), contradicts it (False), or provides insufficient information either way (Cannot Say). Assessments also include multiple-choice comprehension items testing whether you can identify the core argument, the precise scope of a rule, or the best summary of a stance. Timing is tight — often less than a minute per question — simulating the pace at which you skim-then-verify documents in a working day.

Why does this matter for a lead analytics engineer? Because your role is unusually text-critical. You create standards for communication, data models, and documentation — texts other people must be able to apply unambiguously. You review specifications and define test conditions from their exact wording. You interpret the needs of technical and non-technical stakeholders from emails and meeting notes where precision varies wildly. A misreading at your level does not stay contained: it propagates through your team's models and into decisions made across the organisation. Verbal reasoning assessments measure the exact discipline — reading what the text says, no more and no less — that keeps this from happening.

### What it measures for your role

- **Communicating between the technical and non-technical** — interpreting stakeholder needs precisely from written requests, and recognising when a statement manages expectations accurately versus overpromises.
- **Data modelling, cleansing and enrichment** — reading standards documents with legal-level precision: what a rule requires, what it merely recommends, and what it is silent about.
- **Metadata management** — parsing definitions and repository policies where a single word ("must" versus "should", "dataset" versus "data model") changes the obligation.
- **Testing** — deriving exact test conditions from specification wording, and spotting where a specification is ambiguous or incomplete.
- **Problem management** — reading incident reports and post-incident reviews accurately: what was established as fact, what was hypothesised, and what remains unknown.
- **Data analysis and synthesis** — distinguishing what a written source-system description actually asserts from what a reader might assume.

### Practice questions

**Passage A — Data transformation standards (for Questions 1–4).**

*"All transformation code must be version controlled and peer reviewed before deployment to the production environment. Peer review must be performed by an analytics engineer who did not author the change. Reviews should normally be completed within two working days of the review request. Where a change affects a data model designated business-critical, the review must additionally be approved by the lead analytics engineer or a nominated deputy. Documentation must be updated in the same change where the change alters a model's grain, adds or removes columns, or changes a column's business definition. Changes made under the emergency process may be deployed before review, provided a retrospective review is completed within five working days."*

**Question 1 (easy).** True, False, or Cannot Say: "Every change to transformation code must be reviewed before it reaches production."

**Correct answer: False.**

**Explanation:** The final sentence explicitly permits emergency changes to be "deployed before review", subject to retrospective review within five working days. So the statement, with its "every ... before", is contradicted by the passage. This is the archetypal verbal reasoning trap: the first sentence sounds absolute ("must be ... peer reviewed before deployment"), and a candidate who stops reading there answers True. The passage as a whole defines an exception, and exceptions are exactly what you train your team to look for when applying standards.

**Question 2 (moderate).** True, False, or Cannot Say: "A review of a non-critical change that takes three working days breaches the standard."

**Correct answer: False.**

**Explanation:** The passage says reviews "should normally be completed within two working days". "Should normally" is guidance, not an absolute requirement — contrast it with the "must" used elsewhere in the same passage. A three-day review therefore departs from the norm but does not breach a mandatory rule, so the claim of a breach is contradicted. Discriminating between "must" and "should" is a precision skill assessments test relentlessly, and it is the same distinction you encode deliberately when you write standards for your own team.

**Question 3 (moderate).** True, False, or Cannot Say: "The lead analytics engineer must approve all changes to business-critical data models."

**Correct answer: False.**

**Explanation:** The passage says such reviews must be approved by "the lead analytics engineer *or a nominated deputy*". The word "or" makes the statement's "must approve all" too strong: a nominated deputy can approve instead. The claim is therefore contradicted as written. Notice the assessment skill here — the statement is nearly right, and the single overlooked disjunction flips the answer. As the person who nominates deputies and designs approval flows, you know operationally why that "or" exists; the test asks you to see it on the page.

**Question 4 (hard).** True, False, or Cannot Say: "A change that only improves the performance of a model's code, without altering grain, columns, or definitions, does not require any documentation update."

**Correct answer: Cannot Say.**

**Explanation:** The passage states when documentation *must* be updated in the same change (grain, columns, business definitions). It is silent about whether other changes require documentation updates through some other route or at some other time — it neither confirms nor denies a documentation obligation for performance-only changes. The tempting answer is True, by inverting the rule ("the listed cases require it, therefore unlisted cases do not") — but that inference imports an assumption the text does not license. "The passage doesn't say" is precisely what Cannot Say exists for, and recognising silence in a standard is the same skill as spotting a specification gap when you define test conditions.

**Passage B — Stakeholder email (for Questions 5–7).**

*"From: Head of Housing Performance. Subject: Quarterly returns model. Team — thank you for the new housing repairs model. Colleagues in operations tell me the repair-completion figures now match the source system for the first time, which has noticeably improved confidence. However, the finance team report that the cost-per-repair measure in the model differs from the figure in their quarterly return, and they are unwilling to sign off the return until this is explained. I understand the two figures may be calculated on different bases. Can your team provide a written explanation of the difference by Friday, and advise whether the model's basis should change? To be clear, I am not asking you to change the model at this stage. We remain committed to using the model as the single source for next year's returns provided outstanding issues are resolved."*

**Question 5 (easy).** True, False, or Cannot Say: "The finance team has refused to sign off the quarterly return until the difference in the cost-per-repair figures is explained."

**Correct answer: True.**

**Explanation:** The email states the finance team "are unwilling to sign off the return until this is explained" — where "this" refers to the differing cost-per-repair figures. "Unwilling to sign off until explained" directly supports the statement's "refused ... until ... explained". This is a straightforward retrieval item; the skill is confirming the referent of "this" and matching the paraphrase honestly rather than over- or under-reading it.

**Question 6 (moderate).** True, False, or Cannot Say: "The Head of Housing Performance has asked the team to change the basis of the model's cost-per-repair measure."

**Correct answer: False.**

**Explanation:** The email asks for two things: a written explanation of the difference by Friday, and *advice* on "whether the model's basis should change". It then states explicitly: "I am not asking you to change the model at this stage." The statement is therefore contradicted — a request for advice about a change is not a request to make the change. Reading requests at their exact strength is core to your skill of interpreting stakeholder needs and managing expectations: overreading this email as a change instruction could burn team capacity and undermine the very confidence the first paragraph celebrates.

**Question 7 (hard).** True, False, or Cannot Say: "The model's cost-per-repair measure is calculated on a different basis from the finance team's figure."

**Correct answer: Cannot Say.**

**Explanation:** The email says the writer "understand[s] the two figures *may* be calculated on different bases". "May" reports a possibility — a hypothesis the writer has picked up — not an established fact. The passage neither confirms the bases differ (the difference could yet prove to be a defect) nor denies it. Candidates who work in this field often answer True because differing calculation bases is the *likely* real-world explanation — but likelihood from professional experience is exactly what the test asks you to set aside. Treating hypotheses as hypotheses until verified is also, not coincidentally, the discipline of good problem management.

**Passage C — Metadata policy extract (for Questions 8–10).**

*"Each data model published to the analytical platform must have a corresponding entry in the metadata repository before publication. The entry must record the model's owner, refresh frequency, grain, and source systems. Column-level descriptions are required for all models designated business-critical and are recommended for all other models. Where a model is deprecated, its repository entry must be retained and marked as deprecated for a minimum of twelve months, after which it may be archived. The data governance board may grant exemptions to any provision of this policy; exemptions must be recorded in the exemptions register."*

**Question 8 (easy).** True, False, or Cannot Say: "A model may be published to the analytical platform before its metadata repository entry exists, if the data governance board has granted an exemption."

**Correct answer: True.**

**Explanation:** The final sentence says the board "may grant exemptions to *any* provision of this policy", and the before-publication entry requirement is a provision of the policy. So a granted exemption would permit exactly what the statement describes. The statement is conditional ("if the board has granted an exemption"), and the passage supports the condition's effect. Candidates sometimes answer False on the strength of the opening "must" alone — but a policy's exemption clause modifies everything before it, just as it does in the real governance frameworks you operate within.

**Question 9 (moderate).** True, False, or Cannot Say: "Column-level descriptions are mandatory for all models on the analytical platform."

**Correct answer: False.**

**Explanation:** The passage draws a two-tier distinction: column-level descriptions are "required" (mandatory) for business-critical models and "recommended" (not mandatory) for all others. The statement's "mandatory for all models" is therefore contradicted for the non-critical tier. Precision about which obligations attach to which tier is the daily grammar of metadata management — and when you advise less experienced team members, this required-versus-recommended distinction is often exactly what they need help reading correctly.

**Question 10 (hard).** True, False, or Cannot Say: "A deprecated model's repository entry must be archived after twelve months."

**Correct answer: False.**

**Explanation:** The passage says the entry must be retained and marked deprecated "for a minimum of twelve months, after which it *may* be archived". Two separate misreadings would produce True: turning the permission "may be archived" into the obligation "must be archived", and turning the "minimum of twelve months" floor into a fixed twelve-month trigger. The statement asserts an obligation where the passage grants only a permission, so it is contradicted — False, not Cannot Say, because the passage directly addresses archiving and speaks in "may". Modal verbs (must, may, should) carry the entire regulatory load of texts like this; assessments at your level test whether you weigh them exactly.

**Passage D — Post-incident review extract (for Questions 11–13).**

*"On 14 May, the overnight build failed, and the corporate performance dashboard displayed figures that were 24 hours out of date until 11:20. The failure was traced to an unannounced schema change in the licensing source system: a column relied upon by the staging model had been renamed. The investigation found that the schema-monitoring alert had been configured for the licensing system's test environment rather than its production environment, and consequently no alert fired. The review team concluded that the incident's impact was limited because the dashboard displays a data-refreshed timestamp. Two actions were agreed: first, repoint the schema-monitoring alert to the production environment; second, propose a data-sharing agreement with the licensing team that includes advance notice of schema changes. The review team noted, without reaching a conclusion, the suggestion that all staging models should select columns explicitly rather than using wildcard selection."*

**Question 11 (easy).** True, False, or Cannot Say: "No alert fired because the schema-monitoring alert was configured against the wrong environment."

**Correct answer: True.**

**Explanation:** The passage states the alert "had been configured for the licensing system's test environment rather than its production environment, and consequently no alert fired". The word "consequently" establishes precisely the causal link the statement asserts. A quick, clean retrieval item — but note how the question rewards reading the causal connective, not just the two facts on either side of it. Incident reports live or die on such connectives, and as the person coordinating investigations, you both read and write them.

**Question 12 (moderate).** True, False, or Cannot Say: "The review team concluded that all staging models should select columns explicitly rather than using wildcard selection."

**Correct answer: False.**

**Explanation:** The passage says the review team "noted, *without reaching a conclusion*, the suggestion" about explicit column selection. The statement claims a concluded position; the passage explicitly denies that a conclusion was reached. This is False rather than Cannot Say because the text directly addresses the matter and contradicts the claim. The distinction between "noted a suggestion" and "concluded" mirrors a real leadership discipline: when you write review summaries, separating agreed actions from open suggestions prevents your team from treating speculation as mandate.

**Question 13 (hard).** True, False, or Cannot Say: "A data-sharing agreement with advance notice of schema changes is now in place with the licensing team."

**Correct answer: Cannot Say.**

**Explanation:** The agreed action was to "*propose* a data-sharing agreement" — proposing is not concluding. The passage tells us the proposal was agreed as an action, but says nothing about whether the agreement was subsequently negotiated, accepted, or put in place. The statement describes a state of the world beyond the passage's horizon, so the answer is Cannot Say. The wrong answers each have a signature error: True extrapolates optimistically from an action item to its completion; False assumes the absence of mention means the agreement does not exist, which the passage cannot establish either. In your role you track exactly this gap — between actions agreed and actions delivered — whenever you coordinate preventive measures.

**Question 14 (moderate) — Multiple choice comprehension.**
Which of the following best summarises the Head of Housing Performance's overall position in Passage B?

A) The model has failed and the team should revert to the previous reporting process
B) The model is trusted for repair-completion figures, but an unexplained discrepancy in one measure must be resolved before finance signs off, and the commitment to the model's future remains conditional on resolving outstanding issues
C) The finance team's figure is wrong and the model's figure should be adopted in the quarterly return
D) The team must change the model's cost-per-repair basis by Friday

**Correct answer: B.**

**Explanation:** B captures all three movements of the email: the credit given ("noticeably improved confidence"), the specific unresolved issue (finance's discrepancy and sign-off), and the conditional forward commitment ("provided outstanding issues are resolved"). A contradicts the email's positive framing and forward commitment; C takes a side the writer conspicuously does not take (the email says the figures "may be calculated on different bases", assigning no fault); D repeats the misreading corrected in Question 6 — the Friday deadline attaches to the written explanation, not to any change. Summary items test proportionate reading: neither inflating criticism nor deflating it, which is the register you use when you relay stakeholder messages to your team.

**Question 15 (moderate) — Multiple choice comprehension.**
In Passage A, which of the following changes triggers a mandatory documentation update in the same change?

A) Improving a model's run time by rewriting a join
B) Renaming a column in a model
C) Adding a code comment
D) Moving a model to a different schedule

**Correct answer: B.**

**Explanation:** The passage mandates same-change documentation when a change "alters a model's grain, adds or removes columns, or changes a column's business definition". Renaming a column both removes a column name and adds another from the consumer's perspective — it falls squarely within "adds or removes columns" (and typically its business definition entry must move with it). Options A, C, and D touch none of the three listed triggers. The item rewards mapping a concrete scenario onto the exact enumerated list — the same act of classification you perform whenever your team asks, "does my change need a docs update under the standard?"

**Passage E — Draft proposal to the data governance board (for Questions 16–17).**

*"This paper proposes adopting a semantic layer tool to standardise metric definitions across the department. Currently, at least three teams calculate 'active caseload' differently, and reconciling the resulting figures consumes significant analyst time each quarter. Under the proposal, metric definitions would be maintained centrally by the analytics engineering team, reviewed quarterly with metric owners, and consumed by all reporting tools from a single source. The proposal does not remove teams' ability to create local metrics; it requires only that metrics used in cross-departmental reporting come from the central layer. A pilot with two teams is proposed for the first quarter, with a decision on wider rollout to follow the pilot evaluation. The cost of the tool is met from the existing platform budget for the pilot period; funding for wider rollout would require a separate business case."*

**Question 16 (moderate).** True, False, or Cannot Say: "Under the proposal, teams would no longer be able to define their own local metrics."

**Correct answer: False.**

**Explanation:** The passage states directly: "The proposal does not remove teams' ability to create local metrics." The constraint applies only to metrics used in cross-departmental reporting, which must come from the central layer. The statement is therefore contradicted. This distractor works on skim-readers who register "maintained centrally by the analytics engineering team" and stop there; the very next sentence carves out the local-metric freedom. It is also the sentence you, as the proposal's likely author, would have written deliberately to pre-empt stakeholder resistance — precise scoping of a mandate is how you build awareness and support for analytics engineering without triggering turf disputes.

**Question 17 (hard).** True, False, or Cannot Say: "If the pilot is successful, the wider rollout will be funded from the existing platform budget."

**Correct answer: False.**

**Explanation:** The passage states that the existing platform budget covers the cost "for the pilot period", and that "funding for wider rollout would require a separate business case". The statement claims the existing budget would fund the wider rollout, which the final sentence directly contradicts — regardless of the pilot's outcome. Note the two-layer trap: the conditional framing ("if the pilot is successful") invites a Cannot Say response because the passage does not say what happens after a successful pilot; but the *funding source* claim is addressed head-on and denied. When a compound statement contains one element the passage contradicts, the statement as a whole is False. Parsing compound claims into their separable parts is precisely the skill you use when reviewing requirement statements that bundle several obligations into one sentence.

### Preparation tips

- **Anchor every answer to quoted words.** Before selecting True or False, identify the exact phrase that confirms or contradicts the statement. If you cannot point to one, the answer is probably Cannot Say. This one habit fixes most verbal reasoning errors.
- **Train your modal-verb radar.** Must, may, should, normally, minimum, at least, or, and — circle them mentally as you read. Your own standards documents are perfect practice material: take a paragraph you wrote and generate three True/False/Cannot Say statements from it.
- **Suppress professional knowledge deliberately.** You know how metadata policies and incident reviews usually work; the test only cares what *this* passage says. Before answering, ask: "is my evidence in the text, or in my experience?"
- **Read the statement as precisely as the passage.** Half the traps are in the statement, not the passage — an added "all", a dropped "or", a completion claimed where only an intention was stated.
- **Manage the clock with a two-pass read.** Skim the passage for structure (what does each sentence govern?), answer retrieval questions fast, and reserve deeper re-reading for Cannot Say candidates. Under a minute per question, structure-first reading beats word-by-word reading.
- **Practise on live documents.** Ten minutes with a GOV.UK service standard page, a data-sharing agreement, or a governance policy — generating and answering your own statements — is the highest-fidelity rehearsal available to you, and it doubles as professional development.
- **Decompose compound statements.** When a statement bundles two claims (a condition and a funding source, an action and its completion), test each part separately against the passage. If the passage contradicts any part, the whole statement is False; if it confirms every part, True; if it confirms some and is silent on the rest, Cannot Say. Working this rule explicitly, rather than judging the statement as a single impression, converts the hardest items in the test into a mechanical and reliable procedure.

### Common pitfalls

- **Bringing in outside knowledge.** The most common failure for experienced professionals: answering from how things are in your organisation rather than from the passage. The test is calibrated to punish exactly this.
- **Confusing "likely" with "stated".** An email that says two figures "may" differ in basis has not stated that they do. Possibility words (may, might, expected, likely) can never support a True.
- **Treating silence as denial.** If the passage does not address a claim, the answer is Cannot Say — not False. False requires contradiction; silence contradicts nothing.
- **Inverting rules.** "Documentation is required when X" does not entail "documentation is not required when not-X". Unlicensed inversion is the classic hard-question trap (see Question 4).
- **Missing exception clauses.** Absolute-sounding opening sentences are routinely qualified later ("emergency process", "exemptions"). Read to the end of the passage before answering anything about "always" or "every".
- **Poor time allocation.** Reading every passage exhaustively before looking at the questions burns the clock. Skim for structure, then verify against the question — the same way you read a long specification when only one clause is in dispute.

## Workplace job-specific situational judgement assessment

### About this assessment

A workplace job-specific situational judgement assessment evaluates your decision-making, interpersonal skill, and professional conduct through realistic workplace dilemmas. Unlike the cognitive, numeric, and verbal assessments, there is no single objectively provable answer computed from data — instead, each scenario offers several plausible responses, and your task is to judge which are more and less effective given the role, the organisation's values, and the practical realities of delivery. Typical response formats ask you to select the **most effective** and **least effective** actions from a set, or to rank or rate every option from best to worst. Timing is usually generous or untimed, because the assessment measures your natural judgement rather than your speed.

For a lead analytics engineer in UK government, the scenarios draw on your real working world: a team of analytics engineers whose work you review and whose growth you support; stakeholders ranging from operational caseworkers to finance directors and governance boards; standards you have authored and must sometimes enforce against resistance; data quality problems with public-facing consequences; and the constant balancing of delivery pressure against doing things properly. Strong answers consistently reflect UK public sector values — meeting user needs, transparency and openness, collaboration across teams, accessibility and inclusion — alongside the leadership behaviours your role level demands: empowering rather than rescuing, addressing root causes rather than symptoms, and communicating honestly between the technical and the non-technical.

Situational judgement scores predict how you will actually behave under the routine pressures of the job, which is why they carry substantial weight in public sector selection. The good news: at your level, you have seen most of these dilemmas in real life. The assessment simply asks you to show, option by option, that you can tell wise handling from expedient handling.

### What it measures for your role

- **Communicating between the technical and non-technical** — scenarios test whether you manage expectations honestly, host difficult discussions rather than avoid them, and translate technical trade-offs for senior stakeholders without distortion.
- **Problem management** — dilemmas about incidents and recurring failures test whether you coordinate investigation, resist blame, fix root causes, and put preventive measures in place.
- **Data modelling, cleansing and enrichment** and **Testing** — scenarios about review findings, standards breaches, and quality shortcuts test whether you uphold standards proportionately, without either rigidity or laxity.
- **Metadata management** and documentation duties — dilemmas test whether you treat documentation and definitions as first-class delivery, even under time pressure.
- **Data innovation** — scenarios test judgement about when to adopt new tools and techniques, and when enthusiasm must yield to timing, evidence, and organisational readiness.
- **Leadership of the team** — throughout, options distinguish leaders who develop their people, delegate well, and improve ways of working from those who hoard work, bypass process, or manage by decree.

### Practice questions

**Question 1 (moderate) — The failing review.**
A newer analytics engineer on your team submits a data model for review. It works, but it breaches your team's standards in several ways: undeclared grain, no uniqueness tests, and cryptic column names. This is their third submission with similar problems. The model is needed by a stakeholder team next week. Rate the options.

Option A: Approve it this once given the deadline, and fix the issues yourself over the weekend.
Option B: Reject the review with a written list of the breaches and no further comment.
Option C: Pair with the engineer to fix the issues together, and agree a plan (for example, a pre-review checklist and some focused coaching) to address the recurring pattern.
Option D: Reassign future model work to a stronger engineer and give this person maintenance tasks.

**Most effective: C. Least effective: A.**

**Explanation:** Option C meets the deadline, upholds the standard, develops the engineer, and — crucially, given this is the third occurrence — treats the pattern as the real problem, exactly as your role's duties to review work, support the team, and improve ways of working require. Option A is the least effective: it hides the problem from the engineer (who learns nothing), erodes the standard silently, sets an unsustainable precedent of the lead absorbing rework, and models poor working practice. Option B upholds the standard but abdicates leadership — written rejection alone has already failed twice, and it does nothing for next week's deadline. Option D solves nothing and quietly writes a person off without ever having invested in their development, which is both poor leadership and poor inclusion practice.

**Question 2 (moderate) — The direct request from above.**
A director messages you directly: "I need a new dashboard measure of average processing time by Friday for a ministerial briefing. Just add it — no time for the usual process." You know the underlying data has a known quality issue: about 15% of cases have missing end dates, which would silently skew the measure. Rate the options.

Option A: Add the measure as asked; the director owns the risk.
Option B: Reply immediately explaining the data quality issue in plain terms, propose what *is* achievable by Friday (for example, the measure computed on complete cases, clearly caveated, with the missing-data rate stated), and flag what the full fix requires.
Option C: Refuse, citing the team's change process, and copy in your own manager.
Option D: Add the measure but privately tell the director's analyst about the skew so they can mention it if asked.

**Most effective: B. Least effective: A.**

**Explanation:** Option B is the model answer for communicating between the technical and the non-technical: it neither blocks nor blindly complies; it converts a technical caveat into decision-useful plain English, offers a deliverable that serves the user need honestly by Friday, and manages expectations about the full fix. Option A is least effective: a silently skewed figure in a ministerial briefing is a transparency failure with real public consequences, and "the director owns the risk" is untrue when you knew and did not say. Option C protects process over purpose — the director's need is legitimate and urgent; escalating defensively before offering options is neither collaborative nor user-focused. Option D is the quiet-corridor version of honesty: the caveat reaches the briefing only by luck, and it positions you as someone who knew of a defect and routed the warning informally rather than owning it.

**Question 3 (hard) — Conflicting definitions.**
You are conforming data from three business units into a single "active case" model. In workshops, each unit insists its own definition of "active" is correct, and the disagreement is becoming heated; two unit heads have separately emailed you asking you to adopt their definition. Your team is blocked pending a decision. Rate the options.

Option A: Adopt the definition of the unit that funds the largest share of the platform.
Option B: Model all three definitions as separate, clearly named measures, and pause any attempt at a single definition.
Option C: Facilitate a working session with the three units to map how each definition arises from their processes, identify what cross-unit decisions actually need, and propose a conformed definition (with unit-specific variants where genuinely justified) for governance sign-off.
Option D: Escalate to the data governance board to impose a definition, and tell your team to wait.

**Most effective: C. Least effective: A.**

**Explanation:** Option C is the essence of your role: working with stakeholders across the organisation to understand relationships between data and organisational processes, and using that understanding to define data requirements. It treats the disagreement as information — different definitions usually encode genuinely different processes — hosts the difficult discussion directly, and routes the outcome through legitimate governance. Option A is least effective: deciding semantics by funding power is arbitrary, corrodes trust in the platform's neutrality, and guarantees the losing units disengage from the conformed model. Option B is a reasonable interim tactic but as a final answer it abandons the purpose of conforming data — decision-making across units — and quietly institutionalises the confusion. Option D outsources a facilitation job that is yours to lead; boards impose definitions well only when someone has done Option C's groundwork first, and "tell the team to wait" leaves them blocked longer than necessary.

**Question 4 (moderate) — The overnight incident.**
Your pipeline failed overnight and the department's main performance dashboard is stale on the morning of a board meeting. A team member has found a quick manual workaround: re-running one model with a hand-edited parameter. You have not yet established the root cause. Rate the options.

Option A: Apply the workaround, note exactly what was done, tell the dashboard's owners about the staleness and the fix, and schedule a root-cause investigation for today with a named owner.
Option B: Refuse any workaround until the root cause is fully understood, whatever the delay.
Option C: Apply the workaround quietly and move on; the dashboard is fixed, and no one need know.
Option D: Ask the team member to keep re-running the manual fix each morning until someone has time to look at the underlying issue properly.

**Most effective: A. Least effective: D.**

**Explanation:** Option A balances service restoration with problem management discipline: users are informed transparently, the manual intervention is recorded (protecting auditability and the next investigator), and the root cause gets an owner and a date — restoring service and investigating properly are sequenced, not traded off. Option B mistakes rigidity for rigour; leaving decision-makers with stale data for hours when a recorded, reversible workaround exists serves no one, and root-cause analysis does not require the symptom to persist. Option C fails transparency twice — towards users who briefly saw stale figures, and towards your own team's record of what was changed by hand. Option D is least effective because it converts an incident into a permanent hidden process: unrecorded manual edits every morning are exactly how small failures compound into data integrity scandals, and it also silently taxes one team member with recurring toil — the opposite of taking "the right actions to investigate, resolve and anticipate problems".

**Question 5 (hard) — The innovation enthusiast.**
A talented senior engineer on your team is passionate about a new open-source transformation framework. They have begun quietly rebuilding part of the production pipeline in it "as a proof of concept", without agreement, and are encouraging two junior engineers to join in. The framework is genuinely promising, but it is immature, unsupported by your platform team, and outside your department's approved tooling. Rate the options.

Option A: Shut the work down and remind the engineer that tooling decisions are made through the proper channels.
Option B: Let the rebuild continue — innovation should not be stifled, and the framework may well be the future.
Option C: Stop the unauthorised production work, but redirect the enthusiasm: agree a bounded, non-production evaluation with success criteria, involve the platform team, and take the results to the appropriate forum as a considered adoption proposal.
Option D: Report the engineer to your manager for making unauthorised changes.

**Most effective: C. Least effective: B.**

**Explanation:** Option C exercises your data innovation skill exactly as the framework defines it: identifying areas of innovation *and recognising appropriate timing for adoption*. It removes the immediate risk (unauthorised, unsupported code heading for production), preserves and channels the engineer's initiative, brings the platform team in early — collaboration that any real adoption would need anyway — and creates an evidence-based decision route. Option B is least effective: unsanctioned rebuilds of production pipelines in unsupported tooling create operational risk, split the team's standards in two, and set juniors an example of bypassing agreed ways of working; enthusiasm is not a governance model. Option A manages the risk but wastes the energy and insight behind it — a purely suppressive response from a leader whose role includes promoting and building awareness of analytics engineering innovation. Option D escalates a leadership conversation you have not yet had; it damages trust and outsources people leadership that belongs with you.

**Question 6 (moderate) — The documentation shortfall.**
An internal audit finds that a third of your team's data models lack the documentation your own standards require. The team is under sustained delivery pressure, and one of your engineers says openly in a retrospective: "Documentation is what we cut when deadlines bite — everyone knows that." Rate the options.

Option A: Announce that no new model work will be accepted until every model is fully documented.
Option B: Acknowledge the reality the engineer has named, then change the system: make documentation part of the definition of done, budget for it in estimates, add automated checks where possible, and agree a prioritised backfill plan starting with the most-used models.
Option C: Accept that documentation slips under pressure and quietly lower the standard to match reality.
Option D: Remind the team that the standard exists and ask everyone to try harder.

**Most effective: B. Least effective: C.**

**Explanation:** Option B treats the audit finding as a ways-of-working problem, not a diligence problem — which the retrospective comment confirms it is. Building documentation into the definition of done and into estimates removes the structural incentive to cut it; automated checks make compliance cheap; a usage-prioritised backfill is proportionate rather than heroic. This is your role's duty to create and maintain data documentation and to define and improve ways of working, done at the system level where leads operate. Option C is least effective: silently lowering a standard because it is inconvenient tells the team that all standards are negotiable under pressure, and undocumented models directly undermine reuse, onboarding, and the metadata quality your stakeholders depend on. Option A punishes users of the platform for the team's process debt and creates a delivery cliff. Option D is the classic ineffective middle: restating a rule without changing any of the conditions that caused it to be cut.

**Question 7 (hard) — The difficult senior meeting.**
In a cross-directorate meeting, a senior stakeholder publicly blames your team for "wrong numbers" in a report, in front of your two most junior engineers. You are fairly sure the discrepancy comes from the stakeholder's own team using an outdated extract rather than your model, but you cannot prove it in the room. Rate the options.

Option A: Push back firmly in the meeting with your working theory, so the accusation does not stand unchallenged.
Option B: Say the discrepancy is being taken seriously, commit to a joint investigation with the stakeholder's team, and offer a specific date for shared findings; afterwards, check in with your junior engineers, and follow up with the stakeholder one-to-one about handling concerns before public forums.
Option C: Apologise on behalf of the team to defuse the moment and move the agenda on.
Option D: Stay silent in the meeting and send a detailed rebuttal email to all attendees that evening.

**Most effective: B. Least effective: C.**

**Explanation:** Option B does five things well: it stays composed and factual under public pressure; it converts an accusation into a *joint* investigation — collaborative rather than adversarial, and the fastest route to the truth whoever is right; it commits to specifics (a date, shared findings) that manage expectations; it protects and reassures the junior engineers who just watched their team attacked; and it addresses the behavioural issue privately, hosting the difficult conversation your skill profile explicitly includes. Option C is least effective: apologising for an error you do not believe occurred concedes a "fact" that will be repeated in future meetings, demoralises your team, and — if your theory is right — leaves the actual root cause (an outdated extract) uninvestigated so the error recurs. Option A risks an evidence-free public confrontation that becomes about personalities, and it may be wrong. Option D avoids the moment but then escalates in writing to a wide audience — the same public contest, minus the chance for dialogue.

**Question 8 (moderate) — The under-review backlog.**
You return from two weeks' leave to find eleven model changes awaiting your review, some blocking other teams. Your standards require lead approval for business-critical models (six of the eleven). Two senior engineers on your team are experienced reviewers. Rate the options.

Option A: Work through all eleven yourself in order of arrival, however long it takes.
Option B: Approve all eleven quickly on the senior engineers' assurance that they look fine.
Option C: Triage by impact; formally nominate the two senior engineers as deputies for business-critical approvals (as your standard allows), split the backlog, and then change the process so lead approval is never a single point of failure during absences.
Option D: Ask the requesting teams which changes are truly urgent and review only those this week.

**Most effective: C. Least effective: B.**

**Explanation:** Option C resolves today's backlog and tomorrow's: triage handles urgency, formal nomination keeps the approvals legitimate under your own standard rather than bypassing it, delegation develops your senior engineers, and the process change removes the structural single point of failure — leads who bottleneck reviews are a well-known anti-pattern, and defining better ways of working is your job. Option B is least effective because "they look fine" is not a review: it launders eleven unexamined changes — six of them business-critical — through your authority, defeating the purpose of the control while pretending to honour it. Option A is diligent but slow, keeps other teams blocked, misses the leadership lesson entirely, and guarantees a repeat after your next leave. Option D usefully gathers priority information but, alone, leaves non-"urgent" teams blocked indefinitely and still fixes nothing structural.

**Question 9 (moderate) — The accessibility gap.**
A well-regarded analyst in a stakeholder team tells you privately that the documentation site your team maintains is difficult for them to use with a screen reader — tables render poorly and diagrams have no text alternatives. Your team is mid-sprint on a stakeholder-facing deliverable. Rate the options.

Option A: Thank them, log it in the backlog, and pick it up when the current delivery pressure eases.
Option B: Thank them, make the quick fixes now (text alternatives, heading structure), schedule the structural fixes visibly in the next sprint, ask whether they would be willing to sanity-check the improvements, and update your documentation standards so new content is accessible by default.
Option C: Suggest they request the information they need by email, as a workaround, until the team has capacity.
Option D: Forward the issue to the department's central accessibility team, as documentation platforms are really their responsibility.

**Most effective: B. Least effective: C.**

**Explanation:** Accessibility is a legal and values-level obligation in UK public services, not a nice-to-have — public sector websites and documentation are covered by accessibility regulations, and inclusion is a core public sector value. Option B responds proportionately: immediate low-cost fixes now, structural work scheduled transparently, the affected user involved respectfully (and voluntarily) in verification, and — the lead-level move — the *standard* updated so the problem stops being recreated in every new page your team writes. Option C is least effective: it converts a systemic defect into a recurring personal burden on the person affected, which is the opposite of inclusion, and it signals that access for disabled colleagues is a workaround rather than a requirement. Option A treats a live exclusion as ordinary backlog — better than C, but it leaves a colleague unable to use your documentation for an indefinite period. Option D may be a useful *additional* step for platform-level issues, but as a complete response it deflects ownership of content your own team authors and maintains.

**Question 10 (hard) — The quality issue in yesterday's answer.**
While improving a model, one of your engineers discovers that a figure your team supplied three weeks ago — since quoted in a published departmental report — was overstated by roughly 8% because of a duplicate-join defect that has now been fixed. No one outside the team knows. Rate the options.

Option A: Say nothing; the defect is fixed, the error is historical, and reopening it would damage the team's reputation.
Option B: Quietly correct the model going forward, and mention the historical discrepancy only if someone asks.
Option C: Verify the size and scope of the error, inform the report's owner promptly with a clear plain-English explanation and a corrected figure, support any correction process the department requires, and run a review to catch similar defects earlier.
Option D: Inform the report's owner but frame the discrepancy as a "data source revision" rather than a defect, to protect the team.

**Most effective: C. Least effective: A.**

**Explanation:** Option C is the transparency answer, and in a public sector context it is not optional: a published figure informs public accountability, and knowingly leaving it uncorrected makes the error a choice rather than an accident. C also does it professionally — verify first so you report accurately; communicate in plain English to a non-technical owner; support the correction process rather than dictating it; and close the loop with a preventive review, which is problem management applied to quality. Option A is least effective for the same reason C is best: concealment converts an honest defect into an integrity failure, and discovery later (defects of this kind are usually discoverable) would do far more reputational damage than the correction. Option B is concealment with a conscience clause — the public record stays wrong. Option D crosses a line from framing into misrepresentation: describing a join defect as a "source revision" to the report's owner deprives them of accurate information they are entitled to, and asks your team to maintain a fiction.

**Question 11 (moderate) — The struggling adopter.**
You have introduced a new standard requiring all transformation code to include automated tests. Most of the team has adapted well, but one long-serving engineer — technically strong, and respected — has not written a single test in two months, and their untested changes have twice caused small regressions. In one-to-ones they say: "I've written reliable code for fifteen years without this overhead." Rate the options.

Option A: Exempt them informally; their code is mostly reliable, and the conflict is not worth it.
Option B: Enforce the standard mechanically: reject all their unreviewed, untested changes until they comply.
Option C: Have a direct, respectful conversation linking the standard to the two regressions and to the team's collective responsibility; listen to their objections in case some have merit; offer support (pairing, examples); and be clear the standard applies to everyone, following through consistently in review.
Option D: Raise their non-compliance in the team retrospective so the group can address it together.

**Most effective: C. Least effective: D.**

**Explanation:** Option C combines the two things leadership requires here: genuine listening — long-serving engineers' objections sometimes surface real flaws in a new standard, and refining standards in response to feedback is your role — and unambiguous consistency, because an informally exempted senior engineer teaches the whole team that standards are optional for the sufficiently confident. The two regressions give the conversation concrete, non-personal evidence. Option D is least effective: naming an individual's compliance failure before the group is public shaming by process — it poisons the retrospective's psychological safety, humiliates a respected colleague, and makes future honest discussion less likely. Option A trades short-term peace for the standard's credibility. Option B may eventually be necessary as a follow-through, but as an opening move it skips the conversation, the listening, and the support — enforcement without engagement reads as hostility and squanders a respected engineer's goodwill.

**Question 12 (hard) — The tempting shortcut at scale.**
A programme director offers your team significant new funding to build conformed data models for four additional business areas — but requires all four in six months, a pace your experience says will force the team to skip profiling, testing, and documentation. Declining outright risks the programme building its own shadow data team instead. Rate the options.

Option A: Accept the funding and the deadline; the team will find a way, and the alternative is worse.
Option B: Decline; the timeline is undeliverable to standard, and the team's quality reputation matters more than growth.
Option C: Engage the director on outcomes: present a transparent, evidence-based counter-proposal (for example, two areas delivered properly in six months with the others phased, or a scoped thin-slice across all four), explain in business terms what the compressed timeline sacrifices and what that costs later, and seek agreement on a plan the team can actually deliver.
Option D: Accept the deadline publicly but privately plan for the team to deliver what it can and renegotiate when the shortfall becomes undeniable.

**Most effective: C. Least effective: D.**

**Explanation:** Option C is expectation management at programme scale: it takes the director's need seriously, converts your delivery-quality concerns into consequences a non-technical leader can weigh (rework, unreliable figures, support burden), and offers credible alternatives rather than a bare no — the behaviour your communication skill describes as supporting difficult discussions with diverse senior stakeholders. Evidence-based counter-proposals also usually beat shadow-team threats, because the director's real interest is delivered outcomes, not organisational rivalry. Option D is least effective: it is a commitment you already believe to be false, and planned failure discovered late costs the director options they would have had in month one — it is the least transparent choice on the list, and it makes the eventual difficult conversation happen at the worst possible time. Option A gambles the team's health and the models' integrity on hope, and quietly plans to breach the very standards that make the team worth funding. Option B may be where you end up if negotiation fails, but leading with refusal — no options, no engagement — abandons a legitimate organisational need and invites exactly the shadow-team outcome it fears.

### Preparation tips

- **Anchor on values, then on effectiveness.** For each option ask two questions in order: does this reflect public sector values (user needs, transparency, collaboration, accessibility, inclusion)? And does it actually solve the problem, including its root cause? The best options score on both; the worst usually fail both.
- **Think like the leader you are, not the engineer you were.** At lead level, options that involve doing the work yourself, quietly absorbing problems, or bypassing your own team usually rank lower than options that develop people, fix systems, and communicate openly — even when the hands-on option feels generous.
- **Watch for the "quietly" word.** Options containing quiet fixes, private workarounds, or selective disclosure almost always rank poorly in public sector scenarios, where transparency is a first-order value.
- **Distinguish interim tactics from complete answers.** Many weaker options are fine first steps (escalate, log it, ask for priorities) that fail because they are offered as the whole response. The strongest options tend to pair immediate action with a structural follow-through.
- **Use your real experience as calibration, not as a script.** Recall how similar situations actually unfolded for you — what worked, what backfired — but answer the scenario on the page, including its stated constraints.
- **Read every option fully before rating any.** Most/least formats are comparative; an option that seems strong alone may be dominated by a better-constructed neighbour.

### Common pitfalls

- **Answering idealistically rather than practically.** "Refuse anything imperfect" options sound principled but fail the effectiveness test — rigidity that leaves users without data or teams blocked rarely scores well.
- **Selecting passive or deflecting options.** Logging, waiting, forwarding to another team, or escalating without any action of your own are classic low-scoring choices: they delay action, pass the problem on, or ignore the root issue.
- **Choosing conflict avoidance dressed as diplomacy.** Apologising for errors you have not verified, conceding definitions to the loudest stakeholder, or exempting difficult colleagues all buy short-term calm at long-term cost — and assessors know it.
- **Forgetting the people in the scenario.** Options that fix the technical problem but humiliate a colleague, burden the person who raised an issue, or ignore junior staff who witnessed a conflict lose marks on the interpersonal dimension the assessment is explicitly measuring.
- **Ignoring the public sector context.** In government scenarios, transparency about errors, accessibility obligations, and stewardship of public money are weighted heavily; judgement calibrated purely to private sector commercial norms will misrank options.
- **Overthinking towards the exotic option.** The most effective option is usually the one that acts promptly, communicates honestly, involves the right people, and prevents recurrence. If an option does all four, trust it.

## Conclusion

You have now worked through four complete, role-specific assessment resources: a cognitive assessment built from the dependency graphs, standards, models, and problem investigations you lead every day; a numeric reasoning assessment grounded in the quality metrics, capacity plans, budgets, and cost-benefit cases you present to stakeholders; a verbal reasoning assessment drawn from the standards documents, stakeholder emails, policies, and incident reviews you read and write; and a situational judgement assessment reflecting the genuine leadership dilemmas of running an analytics engineering team in the UK public sector.

If one message ties the four together, it is this: these assessments measure capabilities you already exercise. Leading the design and deployment of data models has made you a careful reader, a disciplined checker, a fluent interpreter of numbers, and a considered decision-maker. Preparation is not about becoming someone else for a test — it is about practising the format, sharpening the habits (anchor to the text, identify the denominator, check every constraint, pair action with prevention), and arriving calm enough to show your real ability.

As next steps: revisit the questions you found hardest and re-derive the answers a few days from now; generate your own practice items from documents and dashboards in your daily work, which is the highest-fidelity practice available; and time yourself, because familiarity with pace is half of test-day confidence. Consider working through a question or two with your own team — explaining the reasoning aloud is powerful preparation for you and genuinely useful development for them.

Whether you are preparing for a selection process, benchmarking yourself for development, or simply curious about how your role's skills translate into assessable capabilities, treat this document as a resource to return to rather than a one-time read. Your role sits at a valuable and growing intersection of data, engineering, and leadership in government — and the same qualities these assessments measure are the ones that will carry your career forward. Good luck: prepare well, trust your experience, and let your everyday excellence show.
