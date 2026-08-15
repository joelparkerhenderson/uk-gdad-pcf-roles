# Data architect - Psychometric Assessment Resources

## Introduction

Welcome! This document is a practical, friendly guide to the psychometric assessments you may encounter as a data architect working in the UK Government Digital and Data profession. Whether you are preparing for a formal assessment as part of a recruitment or progression process, or you simply want to sharpen the mental skills you use every day, this resource is designed to help you practise, reflect, and build confidence.

Psychometric assessments are structured, standardised exercises that measure how you think and how you make decisions. They are not tests of trivia or memory. Instead, they focus on the mental processes that genuinely predict success in a role: spotting patterns and errors, reasoning with numbers, drawing accurate conclusions from written material, and exercising sound judgement in realistic workplace situations. For a data architect, these skills map directly onto your day-to-day work. You design and maintain data models, you analyse source systems, you keep metadata repositories accurate, you check compliance with data standards, and you communicate insights to both technical and non-technical colleagues. Every one of those duties depends on clear, careful, structured thinking - which is exactly what psychometric assessments measure.

This document is organised into four main assessment sections, each of which follows the same shape:

- **Workplace job-specific cognitive assessment** - pattern recognition, logical deduction, error checking, prioritisation, and problem solving using the artefacts you really handle: data models, data dictionaries, metadata repositories, and integration mappings.
- **Workplace job-specific numeric reasoning assessment** - interpreting tables, percentages, ratios, budgets, capacity figures, and performance metrics drawn from data architecture work.
- **Workplace job-specific verbal reasoning assessment** - reading dense role-relevant passages such as data policies, standards, and stakeholder emails, then answering True / False / Cannot Say and comprehension questions.
- **Workplace job-specific situational judgement assessment** - realistic workplace dilemmas involving your real stakeholders, with most effective / least effective judgements and full discussion of the reasoning.

Each section explains what the assessment measures, maps it to the specific skills in your role profile, provides a generous set of practice questions with worked answers, and closes with preparation tips and common pitfalls.

How should you use this document? Three ways work well. First, as practice: attempt the questions under light time pressure, then study the explanations. Second, as self-reflection: notice which question types feel effortful, because those are your development areas. Third, as preparation: return to the tips and pitfalls shortly before any real assessment. Take your time, be kind to yourself when you get a question wrong, and remember that every explanation you read is building the same muscles you use in your professional practice.

Good luck - and enjoy the practice!

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive assessment is a targeted psychometric test that measures the exact mental processes needed for your role as a data architect. Unlike a generic IQ test, it uses practical workplace scenarios and the kinds of data artefacts you genuinely handle - entity-relationship models, data dictionaries, metadata repositories, integration mappings, archive schedules - to predict how effectively you will perform on the job.

Typical format and timing: these assessments are usually delivered online, are strictly timed (commonly 15 to 30 minutes), and score you objectively against a benchmark or norm group. You will normally receive a few short, ungraded practice questions first so you can get used to the interface. Some modern platforms are adaptive, adjusting question difficulty based on your previous answers, and employers often receive a breakdown of speed versus accuracy rather than a single score. Questions are carefully validated so that they predict job success without bias.

For a data architect, the assessment focuses on five overlapping capabilities: pattern recognition (spotting regularities and irregularities in models, naming conventions, and data flows), logical deduction (reasoning correctly from rules, constraints, and dependencies), error checking (finding inconsistencies between artefacts such as a model and its data dictionary), prioritisation (deciding what to tackle first when compliance, delivery, and stakeholder demands compete), and structured problem solving (working through multi-step technical puzzles methodically).

### What it measures for your role

The cognitive dimensions map directly to the skills in your role profile:

- **Data modelling**: logical deduction and pattern recognition are the core of producing, maintaining, and updating data models, and of reverse-engineering data models from a live system. Many questions present model fragments or schema clues and ask you to infer structure or spot flaws.
- **Metadata management**: error checking and cross-referencing mirror your duty to use metadata repositories for complex tasks such as data and systems integration impact analysis, and to keep repository information accurate and up to date.
- **Data standards** and **data governance**: rule-application questions test whether you can use data policies, processes, and standards effectively, monitor compliance, and analyse the impact if a standard is breached.
- **Data analysis and synthesis**: questions built on data profiling outputs and source system analysis test whether you can extract clear insight from messy evidence.
- **Problem management**: multi-step deduction and dependency questions reflect your duty to investigate patterns and trends to resolve problems, determine the appropriate resolution, and determine preventative measures.
- **Prioritisation** questions echo your duties to design, support, and provide guidance for the upgrade, management, decommission, and archive of data in compliance with data policy - work where sequencing and dependencies matter enormously.
- **Strategic thinking**: some harder questions ask you to reason about which option best serves the wider organisational context, not just the immediate technical fix.

### Practice questions

**Question 1 (easy) - Logical deduction from model rules**

Your organisation's conceptual data model contains these rules:

- Every Case is owned by exactly one Team.
- A Team may own many Cases.
- Every Document belongs to exactly one Case.
- A Case may have zero or more Documents.

Which one of the following statements must be true?

A. Every Team owns at least one Case.
B. A Document can be linked to two Cases if both Teams agree.
C. If a Document exists, there is exactly one Team that indirectly owns it.
D. Every Case has at least one Document.

**Correct answer: C.**

**Explanation:** Work strictly from the stated cardinalities. A Document belongs to exactly one Case, and that Case is owned by exactly one Team, so the chain Document → Case → Team resolves to exactly one Team: C must be true. A is false because "a Team may own many Cases" does not require it to own any (many includes zero unless stated otherwise, and nothing says every Team owns a Case). B directly contradicts "exactly one Case". D contradicts "zero or more Documents". In assessments, resist adding real-world assumptions - reason only from the rules given, exactly as you would when validating a model against its documented constraints.

**Question 2 (easy) - Error checking a data dictionary**

You are providing input into a data dictionary. Below are four entries. Which entry contains an internal inconsistency?

A. `citizen_id` - Data type: INTEGER - Nullable: No - Description: Unique identifier for a citizen record. Primary key.
B. `date_of_birth` - Data type: DATE - Nullable: Yes - Description: Citizen's date of birth in DD/MM/YYYY format; mandatory for all records.
C. `postcode` - Data type: VARCHAR(8) - Nullable: Yes - Description: UK postcode; optional where the citizen has no fixed address.
D. `record_created` - Data type: TIMESTAMP - Nullable: No - Description: System-generated timestamp set when the record is first inserted.

**Correct answer: B.**

**Explanation:** Entry B says the field is nullable ("Nullable: Yes") yet the description says it is "mandatory for all records". A mandatory field must be non-nullable, so the metadata contradicts itself. A, C, and D are internally consistent: A pairs a primary key with non-nullable, C pairs an optional field with a nullable flag and explains why, and D pairs a system-set field with non-nullable. This is exactly the cross-checking you perform when maintaining a metadata repository to ensure information remains accurate and up to date - the flag and the prose must tell the same story.

**Question 3 (moderate) - Pattern recognition in naming conventions**

Your team's physical naming standard generates table names as follows:

- `REF_COUNTRY`, `REF_CURRENCY`, `REF_LANGUAGE` (reference data)
- `TXN_PAYMENT`, `TXN_REFUND` (transactional data)
- `STG_PAYMENT_DAILY`, `STG_REFUND_DAILY` (staging loads)

A developer has created four new tables. Which one breaches the pattern?

A. `REF_REGION`
B. `TXN_INVOICE`
C. `STG_INVOICE_DAILY`
D. `INVOICE_ARCHIVE_TXN`

**Correct answer: D.**

**Explanation:** The observable pattern is prefix-first: a three-letter class prefix (`REF_`, `TXN_`, `STG_`) followed by the subject, with staging tables adding a frequency suffix. Options A, B, and C all follow this. Option D puts the subject first and the class code last, breaking the prefix convention - and it also introduces an `ARCHIVE` element that does not appear in the documented classes. Spotting convention drift early is a core part of monitoring compliance with standards in a team and taking action if needed: one wrongly named table quickly becomes ten.

**Question 4 (moderate) - Integration impact analysis**

Your metadata repository shows these data flows:

- System A feeds System B and System C.
- System B feeds System D.
- System C feeds System D and System E.
- System E feeds nothing.

The `customer_status` field originates in System A and flows along every feed listed. If System C is decommissioned next quarter with no replacement feeds, which downstream systems could lose at least one source of `customer_status`?

A. D only
B. E only
C. D and E
D. B, D, and E

**Correct answer: C.**

**Explanation:** Trace the graph carefully. System C currently feeds D and E, so removing C affects exactly those two. System D also receives from B (which receives from A), so D loses one of its two sources but not both - it still "loses at least one source", so it counts. System E's only feed is from C, so E loses its sole source entirely. System B is upstream of C and is unaffected. The answer is D and E. This is a miniature version of the data and systems integration impact analysis you perform with a metadata repository before any upgrade, decommission, or archive activity - the discipline is to follow the recorded lineage, not your memory of it.

**Question 5 (moderate) - Prioritisation under data policy**

It is Monday morning. Four items are in your queue:

1. A compliance report due Friday showing that an unsupported legacy database still holds personal data that data policy required to be archived last month.
2. A request from a delivery team for guidance on modelling a new entity, needed before their design review on Wednesday.
3. A routine metadata repository update reflecting last week's schema changes.
4. An invitation to explore a new data catalogue tool a vendor has offered to demonstrate "sometime soon".

Which is the most defensible order of attention?

A. 2, 1, 3, 4
B. 1, 2, 3, 4
C. 3, 1, 2, 4
D. 4, 1, 2, 3

**Correct answer: B.**

**Explanation:** Item 1 combines the highest risk (personal data held in breach of data policy - an existing compliance failure, not a hypothetical one) with a hard deadline, so it comes first: your role explicitly includes assurance of data solutions and recommendations to ensure compliance, and analysing the impact if a standard is breached. Item 2 has a real deadline (Wednesday) and blocks another team, so it comes second; starting it early in the week is prudent, but it neither carries regulatory risk nor is due before Wednesday. Item 3 matters - an out-of-date repository undermines future impact analysis - but it is routine and has no fixed deadline. Item 4 is genuinely valuable (data innovation is one of your skills) but is explicitly non-urgent. Option A wrongly puts a Wednesday deadline ahead of an active compliance breach; C and D promote routine or exploratory work above both deadlines.

**Question 6 (moderate) - Reverse-engineering a model from a live system**

You are reverse-engineering a data model from a live system with no documentation. Profiling reveals:

- Table `APPL` has columns `APPL_ID` (unique, never null), `CIT_ID` (never null, many duplicates), `SCHEME_CD` (12 distinct values across 2 million rows).
- Table `CIT` has `CIT_ID` (unique, never null).
- Every `APPL.CIT_ID` value exists in `CIT.CIT_ID`.

Which modelling conclusion is best supported by this evidence?

A. `APPL` and `CIT` are in a many-to-many relationship.
B. Each citizen may have many applications; each application belongs to one citizen; `SCHEME_CD` is likely a foreign key to a small reference table.
C. `SCHEME_CD` is the primary key of `APPL`.
D. `CIT` is a child of `APPL` because `CIT_ID` appears in both.

**Correct answer: B.**

**Explanation:** `APPL_ID` unique and non-null makes it the natural primary key of `APPL`, ruling out C (12 distinct values across 2 million rows cannot identify rows uniquely). `CIT_ID` unique in `CIT` and duplicated in `APPL`, with full referential containment, is the classic signature of a one-to-many relationship from `CIT` (parent) to `APPL` (child) - which rules out D, which has the direction backwards, and A, which would require a linking table or duplicated pairs in both directions. The low cardinality of `SCHEME_CD` (12 values) is the standard profile of a code referencing a reference/lookup table. This is exactly the evidence-led reasoning your skill profile describes: undertake data profiling and source system analysis, and reverse-engineer data models from a live system - let the observed data drive the model, not assumptions.

**Question 7 (moderate) - Metadata repository versus reality**

Your metadata repository records that view `V_CASE_SUMMARY` depends on tables `CASE`, `TEAM`, and `DOC`. A developer tells you the view was rewritten two months ago and now also reads `SLA_TARGET`. An impact analysis for changes to `SLA_TARGET`, run from the repository alone, would therefore:

A. Correctly include `V_CASE_SUMMARY`, because repositories update automatically.
B. Omit `V_CASE_SUMMARY`, creating a false negative in the impact analysis.
C. Include `V_CASE_SUMMARY` twice, creating a false positive.
D. Fail to run, because the repository will detect the inconsistency.

**Correct answer: B.**

**Explanation:** The repository does not know about the new dependency on `SLA_TARGET`, so an analysis of "what depends on `SLA_TARGET`?" will silently miss the view - a false negative, the most dangerous kind of impact-analysis error because nothing prompts you to look further. A is wrong because nothing in the scenario says the repository harvests dependencies automatically (and the two-month-old gap proves it did not). C confuses the failure mode: stale metadata here hides a dependency rather than duplicating one. D is wishful thinking - repositories cannot detect what they were never told. The professional lesson matches your skill statement precisely: maintain a metadata repository to ensure information remains accurate and up to date, because impact analysis is only as good as the metadata beneath it.

**Question 8 (hard) - Deduction with modelling constraints**

You must design a model satisfying all of these business rules:

- Rule 1: An Address is used by one or more Parties.
- Rule 2: A Party has zero or more Addresses.
- Rule 3: For each Party-Address pairing, the organisation must record the date the pairing started and the date it ended.
- Rule 4: A Party must never be recorded with two overlapping pairings for the same Address.

Which design satisfies Rules 1-3, and what does Rule 4 add?

A. A foreign key from Address to Party, with start and end dates on Address; Rule 4 is enforced automatically.
B. A foreign key from Party to Address, with start and end dates on Party; Rule 4 is enforced automatically.
C. An associative (link) entity between Party and Address carrying start and end dates; Rule 4 requires an additional constraint, because a composite key of Party, Address, and start date alone does not prevent overlaps.
D. An associative entity between Party and Address with no attributes; Rule 4 is impossible to enforce in any design.

**Correct answer: C.**

**Explanation:** Rules 1 and 2 describe a many-to-many relationship (an Address used by many Parties, a Party with many Addresses), which A and B cannot represent - a single foreign key on either side forces one end to "exactly one". Rule 3 attaches attributes (start and end dates) to the pairing itself, which is the textbook justification for an associative entity. Rule 4 is the subtle part: making Party + Address + start date the key prevents duplicate identical rows but does not prevent two rows whose date ranges overlap (for example, one pairing from January to June and another from March to December). Preventing overlaps needs an extra constraint - enforced in the database, the application, or a data quality control - and a good architect flags that explicitly rather than assuming the key handles it. D gives up too easily: the rule is enforceable, just not by entity structure alone. Explaining distinctions like this to colleagues is part of your skill to explain the concepts and principles of data modelling.

**Question 9 (hard) - Warehouse load sequencing**

Your data warehouse loads run under these dependency rules:

- Staging loads (S1, S2, S3) can run in parallel and must all finish before any dimension load starts.
- Dimension loads D1 and D2 can run in parallel after staging.
- Fact load F1 requires D1 and D2. Fact load F2 requires D2 only.
- The business intelligence extract E1 requires F1 and F2.

One morning, S2 fails and is rerun successfully, finishing after S1 and S3. Which statement about the remaining schedule is correct?

A. F2 can start as soon as S2 finishes, because it does not depend on D1.
B. D1 and D2 can start once S2 finishes, and F2 can start when D2 finishes even if D1 is still running.
C. E1 can start when F1 finishes, because F1 also covers F2's dependencies.
D. D2 must wait for D1 because dimensions load in numerical order.

**Correct answer: B.**

**Explanation:** Walk the dependency graph. All staging must finish before any dimension starts; once the rerun S2 completes, staging is complete, so D1 and D2 may both start (they are parallel). F2 depends only on D2, so it can begin the moment D2 finishes, regardless of D1's state - which makes B correct and shows why A is wrong (F2 still needs D2, so it cannot start straight after staging). C is wrong because E1 explicitly requires both F1 and F2; F1 finishing tells you nothing about F2. D invents a rule the scenario never states - a classic assessment trap and a classic real-world error when reasoning about batch schedules from habit rather than from the documented dependencies. Defining and maintaining the data technology architecture, including business intelligence and data warehouse architecture, means holding exactly this kind of dependency logic clearly in mind.

**Question 10 (moderate) - Applying archive rules**

Your data policy says: records in the case management system must be archived 2 years after case closure, retained in the archive for a further 5 years, then securely destroyed - unless the case is flagged "legal hold", in which case no archiving or destruction may occur until the flag is removed, at which point the normal clock resumes from where it paused.

A case closed exactly 6 years ago was placed on legal hold 1 year after closure, and the hold was removed 2 years later. What should its status be today?

A. Destroyed
B. In the archive, with about 1 year of retention remaining
C. In the archive, with about 3 years of retention remaining
D. Still in the live system, awaiting archive

**Correct answer: C.**

**Explanation:** Track the archive clock and the pause separately, then lay everything on one timeline. Call the closure date year 0. The archive clock needs 2 years of accumulated running time before the record is archived. It ran from year 0 to year 1 (1 year accumulated), then the legal hold paused it from year 1 to year 3, then it resumed and completed its second year from year 3 to year 4. So the case was archived at calendar year 4. The 5-year archive retention therefore runs from year 4 to year 9. Today is year 6, so the record is in the archive with 3 of its 5 retention years remaining - option C. A fails because destruction is not due until year 9. B miscounts by ignoring the pause and treating the archive date as year 2 (retention year 2 to year 7, leaving 1 year) - the classic error this question is designed to catch. D fails because the accumulated clock passed 2 years back at calendar year 4. The habit that earns the mark is to rebuild the timeline once, cleanly, before committing - exactly the error-checking discipline your role demands when you provide guidance for the management, decommission, and archive of data in compliance with data policy.

**Question 11 (hard) - Decommission dependency ordering**

You are planning the decommission of legacy system L. The constraints are:

- Consumers C1 and C2 currently receive nightly extracts from L.
- C1 can switch to the new platform N only after dataset D has been migrated to N.
- C2 can switch only after C1 has switched, because C2 validates its figures against C1's outputs during parallel running.
- Dataset D cannot be migrated until its metadata (ownership, definitions, lineage) has been completed in the repository.
- L can be switched off only when no consumers depend on it, and its data has been archived per policy.

Which is the earliest valid ordering?

A. Migrate D → complete metadata → switch C1 → switch C2 → archive L's data → switch off L
B. Complete metadata → migrate D → switch C1 → switch C2 → archive L's data → switch off L
C. Complete metadata → migrate D → switch C2 → switch C1 → archive L's data → switch off L
D. Archive L's data → switch off L → complete metadata → migrate D → switch C1 → switch C2

**Correct answer: B.**

**Explanation:** Convert each constraint into a precedence rule: metadata before migration of D; D's migration before C1's switch; C1 before C2; all consumers off L plus archive complete before switch-off. Option B honours every rule in sequence. A reverses the first dependency (migrating D before its metadata is complete). C reverses the C1/C2 order, breaking C2's validation requirement. D switches L off while both consumers still depend on it - the most severe violation. Notice the method: you do not need to imagine the systems, only to extract the partial order from the text and test each candidate sequence against it. This mirrors real decommission planning, where your role is to design, support, and provide guidance for decommission and archive in compliance with data policy, and where a single inverted dependency can interrupt a public service.

**Question 12 (moderate) - Spotting model/dictionary drift**

The logical model shows entity **Payment** with attributes: payment_id, case_id, amount, currency_code, paid_date. The data dictionary lists for the corresponding table: PAYMENT_ID, CASE_ID, AMOUNT, CURRENCY_CODE, PAID_DATE, REFUND_FLAG. The load specification for the finance feed maps six source fields to six target columns, including REFUND_FLAG.

What is the most accurate diagnosis?

A. The dictionary is wrong and REFUND_FLAG should be deleted from it.
B. The model is behind reality: an attribute exists in the implemented table and feed but was never added to the logical model, so the model should be reviewed and updated.
C. The load specification is wrong to map six fields.
D. Nothing is wrong; models never need to show every column.

**Correct answer: B.**

**Explanation:** Two independent artefacts (the dictionary and the load specification) agree that REFUND_FLAG exists and is populated; only the model omits it. When two sources corroborate each other against a third, the lone dissenter is most likely stale - so the model has drifted behind the implementation. A would destroy accurate metadata to match an outdated model, inverting the correction. C contradicts the corroborating dictionary. D is a half-truth used in the wrong place: while conceptual models legitimately omit detail, a logical model that claims to define an entity's attributes should reflect a real, business-meaningful attribute like a refund flag. The remedy in practice is your bread and butter: produce, maintain, and update relevant data models for the organisation's needs, and investigate how the drift happened so you can determine preventative measures - perhaps a change-control step that requires model sign-off before schema change.

### Preparation tips

- **Practise with your own artefacts.** Before an assessment, spend an hour reading one of your organisation's data models alongside its data dictionary, deliberately hunting for inconsistencies. This is the highest-fidelity rehearsal available for error-checking questions.
- **Externalise dependency graphs.** For sequencing and impact questions, sketch the arrows (even just A→B→C on scrap paper or in your head as a list). Working memory errors, not reasoning errors, cause most wrong answers on these items.
- **Reason only from what is given.** Assessments deliberately punish imported assumptions. Treat every question the way you treat a source system with no documentation: evidence first.
- **Manage the clock.** With 15-30 minutes for the whole test, allocate roughly a minute per question, flag anything that stalls you, and return to it. Accuracy on ten questions beats perfection on four.
- **Warm up.** Do two or three practice items immediately before the real assessment so your first scored question is not also your first question of the day.
- **Trust your professional instincts.** You perform integration impact analysis and standards compliance checks for a living. The test dresses those skills in compressed scenarios, but they are the same skills.

### Common pitfalls

- **Adding real-world assumptions.** The most common error is treating "may have many" as "must have at least one", or assuming systems behave like ones you know. Reason strictly from the stated rules, exactly as the strongest candidates do.
- **Reversing dependency direction.** In lineage and foreign-key questions, candidates frequently flip parent and child. Slow down for one beat and confirm which way the arrow points.
- **Time sink questions.** Spending five minutes on one hard multi-stage deduction while easier questions go unanswered is the classic self-inflicted wound. Skip and return.
- **Speed-accuracy imbalance.** Because employers often see speed and accuracy separately, a rushed, error-strewn performance looks worse than a slightly slower, careful one. Aim for controlled pace.
- **Second-guessing validated questions.** If an option seems ambiguous, choose the best-supported answer rather than agonising - these tests are professionally validated, and the intended answer follows from the text.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment evaluates your ability to analyse, interpret, and make sound decisions using numerical data of the kind your role genuinely produces. It is emphatically not an abstract mathematics exam: the questions focus on business arithmetic - percentages, ratios, growth rates, budgets, capacity figures, and cost comparisons - applied to realistic data architecture material such as data profiling outputs, storage forecasts, warehouse load statistics, archive schedules, and tooling budgets.

Typical format and timing: you will usually face a strict time limit (often around 45 to 75 seconds per question across a 20-30 minute test), with data presented in tables, charts, or short numeric narratives. Most assessments allow or provide an onscreen calculator, because the point is interpretation, not mental arithmetic heroics. The skill being measured is quick, accurate data extraction: finding the right numbers, applying the right operation, and sense-checking the result.

For a data architect in UK government, this matters because numbers permeate your work even though you are not a finance professional. You size storage for archives, estimate migration durations, read data quality percentages from profiling runs, compare tooling costs, and present capacity figures to non-technical stakeholders who will rely on your accuracy.

### What it measures for your role

- **Data analysis and synthesis**: the assessment's core - undertaking data profiling and source system analysis means reading tables of counts, null rates, and distinct values, then presenting clear insights to colleagues. Most questions here are profiling tables in miniature.
- **Communicating data**: creating basic visuals and presentations demands that the numbers behind them are right; several questions test whether a chart or summary faithfully represents underlying figures, reflecting your awareness that data needs to be aligned to the needs of the end user.
- **Data modelling** and **metadata management**: estimating row counts, growth rates, and integration volumes supports impact analysis and physical design decisions.
- **Data standards** and **data governance (data architect)**: compliance monitoring is often numeric - what percentage of tables meet the standard, how has the breach rate moved, what is the impact if a standard is breached expressed in affected records.
- **Problem management**: investigating patterns and trends to resolve problems frequently means comparing error rates across weeks or systems and quantifying whether a fix worked.
- **Strategic thinking**: cost projections and option comparisons support strategic planning; you should be able to explain the strategic context of a number, not just compute it.

### Practice questions

**Question 1 (easy) - Storage growth percentage**

The case management database held 3.2 TB of data at the start of the financial year and holds 4.0 TB at the end. What is the percentage growth over the year?

A. 20%
B. 25%
C. 30%
D. 80%

**Correct answer: B.**

**Explanation:** Percentage growth = (new − old) ÷ old × 100. Increase = 4.0 − 3.2 = 0.8 TB. Then 0.8 ÷ 3.2 = 0.25, so 25%. A common error is dividing by the new value: 0.8 ÷ 4.0 = 20% (option A, the trap). Always divide the change by the starting value. Growth rates like this feed directly into the capacity planning you do when defining and maintaining the data technology architecture.

**Question 2 (easy) - Null rate from a profiling run**

Your data profiling of the `ADDRESS` table shows 1,250,000 rows, of which the `postcode` column is null in 75,000 rows. What is the null rate for `postcode`?

A. 0.6%
B. 6%
C. 7.5%
D. 16.7%

**Correct answer: B.**

**Explanation:** Null rate = nulls ÷ total rows × 100 = 75,000 ÷ 1,250,000 = 0.06 = 6%. A quick sanity check: 10% of 1,250,000 would be 125,000, and 75,000 is a bit more than half of that, so the answer must be a bit more than 5% - confirming 6%. Option A misplaces the decimal; C confuses 75 with 7.5; D is 75,000 ÷ 450,000-ish, a made-up ratio. Reading null rates accurately is fundamental to undertaking data profiling and source system analysis and presenting clear insights to colleagues.

**Question 3 (moderate) - Deduplication ratio**

You are consolidating citizen records from three legacy systems into a single master data store:

| Source system | Records |
|---|---|
| System Alpha | 480,000 |
| System Beta | 360,000 |
| System Gamma | 240,000 |

After matching and deduplication, the master store contains 810,000 unique records. What percentage of the combined source records were duplicates?

A. 20%
B. 25%
C. 27%
D. 33%

**Correct answer: B.**

**Explanation:** Combined source records = 480,000 + 360,000 + 240,000 = 1,080,000. Duplicates removed = 1,080,000 − 810,000 = 270,000. Percentage = 270,000 ÷ 1,080,000 = 0.25 = 25%. Option C comes from dividing 270,000 by the wrong base; option D from dividing the unique count incorrectly. Note the assessment habit: total first, difference second, percentage last - and always ask "percentage of what?", because duplicates as a share of the master store (270,000 ÷ 810,000 = 33.3%, option D) is a different, wrong reading of the question. This is exactly the arithmetic behind the migration and integration analyses your role supports.

**Question 4 (moderate) - Data architecture budget shares**

Your data platform programme has an annual budget of £1,200,000 allocated as: warehouse infrastructure 45%, integration tooling 25%, metadata and catalogue tooling 15%, training and community 10%, contingency 5%. Mid-year, the metadata tooling allocation is increased by £30,000, funded entirely from contingency. What percentage of the total budget does contingency now represent?

A. 2.5%
B. 3.0%
C. 4.5%
D. 5.0%

**Correct answer: A.**

**Explanation:** Contingency starts at 5% of £1,200,000 = £60,000. It gives up £30,000, leaving £30,000. As a share of the (unchanged) total: 30,000 ÷ 1,200,000 = 0.025 = 2.5%. The total budget does not change because money moved between lines rather than being added, so the denominator stays £1,200,000 - the point option C misses by recomputing metadata's new share (£180,000 + £30,000 = £210,000, which is 17.5%, not asked). Budget questions reward slow reading of exactly which line and which denominator are wanted. Understanding money flows like this helps you support strategic planning in an administrative capacity with confidence.

**Question 5 (moderate) - Nightly load window capacity**

The warehouse's nightly batch window is 6 hours. Current loads process 90 million rows per night at a steady throughput. A new feed will add 36 million rows per night at the same throughput per row. How long will the total nightly load take?

A. 7.2 hours
B. 7.6 hours
C. 8.0 hours
D. 8.4 hours

**Correct answer: D.**

**Explanation:** Current throughput = 90 million rows ÷ 6 hours = 15 million rows per hour. New total volume = 90 + 36 = 126 million rows. Time = 126 ÷ 15 = 8.4 hours. Option A comes from adding 20% (36/180?) incorrectly; C from rounding 126/15 carelessly. The practical insight the question mimics: the new feed pushes the load 2.4 hours past the window, so as the architect defining the integration and data warehouse architecture, you would need to redesign the schedule, parallelise, or renegotiate the window. Show-your-working discipline (rate first, then total ÷ rate) keeps multi-step questions safe.

**Question 6 (moderate) - Archive savings**

Live storage costs £900 per TB per year; archive storage costs £150 per TB per year. Data policy allows you to move 12 TB from live to archive. The archive migration is a one-off project costing £5,400. What is the net saving in the first year?

A. £3,600
B. £5,400
C. £9,000
D. £10,800

**Correct answer: A.**

**Explanation:** Annual saving per TB moved = £900 − £150 = £750. For 12 TB: 12 × £750 = £9,000 per year. First-year net saving = £9,000 − £5,400 (one-off cost) = £3,600. Option C forgets the migration cost; D multiplies 12 × £900 as if archive storage were free. Note also the framing you would give stakeholders: from year two the full £9,000 recurs, so the project pays back well - a nice example of presenting clear insights to support decisions, and of quantifying the value of the archive work your role guides in compliance with data policy.

**Question 7 (moderate) - Metadata repository coverage**

Your metadata repository documents 320 of the estate's 500 datasets. After a focused documentation sprint, coverage rises to 80% of the estate. How many additional datasets were documented during the sprint?

A. 60
B. 80
C. 100
D. 180

**Correct answer: B.**

**Explanation:** Target coverage = 80% of 500 = 0.8 × 500 = 400 datasets. Already documented = 320. Additional = 400 − 320 = 80. Option A is 12% of 500 (a misread of the percentage-point gain: coverage went from 64% to 80%, i.e. 16 points, and 16% of 500 is 80 - consistent). D confuses the undocumented count (180 before the sprint) with the sprint output. Tracking coverage numerically like this is how you evidence that you maintain a metadata repository to ensure information remains accurate and up to date.

**Question 8 (hard) - Compound storage growth**

The analytics platform currently stores 8 TB. Data volume grows at 25% per year, compounding annually. The platform's economically sensible ceiling is 16 TB. Will three years of growth breach the ceiling, and what is the volume after three years (to one decimal place)?

A. No - 14.0 TB
B. No - 15.6 TB
C. Yes - 16.4 TB
D. Yes - 17.1 TB

**Correct answer: B.**

**Explanation:** Compound growth multiplies: 8 × 1.25 = 10.0 TB after year one; 10.0 × 1.25 = 12.5 TB after year two; 12.5 × 1.25 = 15.625 ≈ 15.6 TB after year three. That is below 16 TB, so the ceiling is not breached within three years - though only just, which is the strategic insight: the fourth year (15.625 × 1.25 = 19.5 TB) blows through it, so planning should start now. Option A uses simple (non-compounding) growth of 2 TB per year; C and D assume the breach without computing. Distinguishing simple from compound growth is one of the highest-value habits in capacity forecasting for the data technology architecture you define and maintain.

**Question 9 (moderate) - Tool licence cost comparison**

You are evaluating two data catalogue tools for a 40-user team:

| | Tool X | Tool Y |
|---|---|---|
| Licence per user per month | £22 | £30 |
| Annual platform fee | £6,000 | £1,200 |

Which tool is cheaper over one year, and by how much?

A. Tool X, by £2,640
B. Tool X, by £960
C. Tool Y, by £960
D. Tool Y, by £2,640

**Correct answer: C.**

**Explanation:** Tool X: 40 users × £22 × 12 months = £10,560, plus £6,000 platform fee = £16,560. Tool Y: 40 × £30 × 12 = £14,400, plus £1,200 = £15,600. Difference = £16,560 − £15,600 = £960 in favour of Tool Y. The per-user price makes Tool X look cheaper (the intended trap), but the platform fee reverses the ranking at this team size. As an exercise in showing awareness of opportunities for innovation with new tools, note the breakeven thinking: X's £8 per-user-per-month saving equals £96 per user per year, so X wins only when (£6,000 − £1,200) ÷ £96 = 50 users or more. Numbers like these are how you turn tool evaluations into clear, defensible recommendations.

**Question 10 (hard) - Quantifying the impact of a standards breach**

A team breached the data standard by loading unvalidated postcodes for six weeks. Profiling shows the affected load inserted 42,000 records per week, of which 8.5% have invalid postcodes. Cleansing costs are estimated at £0.45 per invalid record, and re-validation of the remainder at £0.02 per valid record. What is the estimated total remediation cost (to the nearest £100)?

A. £9,600
B. £11,600
C. £14,300
D. £19,100

**Correct answer: C.**

**Explanation:** Total affected records = 42,000 × 6 = 252,000. Invalid = 8.5% of 252,000 = 0.085 × 252,000 = 21,420 records. Cleansing cost = 21,420 × £0.45 = £9,639. Valid remainder = 252,000 − 21,420 = 230,580 records. Re-validation cost = 230,580 × £0.02 = £4,611.60. Total = £9,639 + £4,611.60 = £14,250.60 ≈ £14,300. Option A stops after the cleansing cost; B applies £0.02 to all records rather than the valid remainder; D applies £0.45 too broadly. This is the arithmetic behind your skill to analyse the impact if a standard is breached - converting a governance failure into a concrete, credible cost that non-technical stakeholders can weigh.

**Question 11 (moderate) - Data quality trend**

Weekly failed-validation counts for the citizen data feed over five weeks: 1,840; 1,610; 1,725; 1,380; 1,150. Total records per week are steady at 115,000. By how many percentage points did the failure rate change from week 1 to week 5?

A. Fell by 0.6 percentage points
B. Fell by 0.9 percentage points
C. Fell by 1.6 percentage points
D. Fell by 37.5 percentage points

**Correct answer: A.**

**Explanation:** Week 1 rate = 1,840 ÷ 115,000 = 0.016 = 1.6%. Week 5 rate = 1,150 ÷ 115,000 = 0.01 = 1.0%. Change = 1.6 − 1.0 = 0.6 percentage points. Option D (37.5%) is the relative fall (690 ÷ 1,840), which is a percentage change, not percentage points - the most commonly confused pair of concepts in numeric assessments and in real reporting. Option C mistakes the week 1 rate itself for the change. When you present clear insights to colleagues about whether a fix is working, saying "failures fell 0.6 percentage points, a 37.5% relative improvement" shows mastery of both framings - a hallmark of communicating data well.

**Question 12 (hard) - Multi-step profiling table**

A source system analysis produces this profile of four candidate tables for migration:

| Table | Rows | Null key rate | Duplicate rate | Est. cleansing hours per 100k rows |
|---|---|---|---|---|
| CUST | 1,500,000 | 2% | 4% | 3.0 |
| ORDR | 4,000,000 | 0.5% | 1% | 1.5 |
| ADDR | 2,500,000 | 6% | 10% | 4.0 |
| PROD | 500,000 | 1% | 2% | 2.0 |

Cleansing effort applies to all rows. Which table needs the most total cleansing hours, and how many?

A. ORDR - 60 hours
B. ADDR - 100 hours
C. ADDR - 40 hours
D. CUST - 45 hours

**Correct answer: B.**

**Explanation:** Total hours = (rows ÷ 100,000) × hours per 100k. CUST: 15 × 3.0 = 45 hours. ORDR: 40 × 1.5 = 60 hours. ADDR: 25 × 4.0 = 100 hours. PROD: 5 × 2.0 = 10 hours. The maximum is ADDR at 100 hours. The null and duplicate rates are deliberate distractors for this particular question - they explain why ADDR's per-row effort is high, but the computation needs only rows and the rate column. Learning to ignore decorative columns under time pressure is a core assessment (and profiling) skill: real source system analysis always yields more numbers than the decision needs, and synthesis means selecting the ones that matter.

**Question 13 (moderate) - Integration volume ratio**

An interface transmits 3 message types nightly in the ratio 5 : 3 : 2 (case updates : document links : status changes). Last night the interface carried 84,000 messages in total. How many document-link messages were sent?

A. 16,800
B. 25,200
C. 28,000
D. 42,000

**Correct answer: B.**

**Explanation:** Ratio parts total 5 + 3 + 2 = 10. One part = 84,000 ÷ 10 = 8,400 messages. Document links are 3 parts = 3 × 8,400 = 25,200. Option A is 2 parts (status changes), D is 5 parts (case updates), and C is a miscount of parts. Ratio questions are quick marks if you always start by summing the parts. Message volumes in these proportions are the everyday material of the integration architecture you define, and knowing them cold helps when you host discussions with delivery teams about interface capacity.

**Question 14 (moderate) - Reading a summary for a stakeholder chart**

You are preparing a basic visual for a governance board showing warehouse query performance. Average query times: last quarter 12.5 seconds, this quarter 9.0 seconds. A colleague's draft slide says "query times improved by 39%". Is the slide right, and what is the correct figure?

A. Yes - 39% is correct
B. No - the improvement is 28%
C. No - the improvement is 35%
D. No - the improvement is 3.5%

**Correct answer: B.**

**Explanation:** Improvement = (12.5 − 9.0) ÷ 12.5 = 3.5 ÷ 12.5 = 0.28 = 28%. The colleague computed 3.5 ÷ 9.0 = 38.9% - dividing the change by the new value instead of the original, which overstates the gain. Option D confuses the absolute change (3.5 seconds) with a percentage. Catching this before the board sees it is precisely the value you add when communicating data: the awareness that data needs to be aligned to the needs of the end user includes making sure the headline number is computed correctly, because a board that later discovers an inflated claim will discount your next ten accurate ones.

**Question 15 (hard) - Migration timeline with contingency**

A data migration must move 18 million records. The tooling migrates 250,000 records per hour, but experience shows 4% of records fail first time and must be re-run once (re-runs succeed and run at the same rate). The programme adds 20% contingency to the computed duration. Migration can only run during a nightly 8-hour window. How many nights should you plan for?

A. 9 nights
B. 10 nights
C. 11 nights
D. 12 nights

**Correct answer: D.**

**Explanation:** Work stepwise. Base volume = 18,000,000 records. Re-runs add 4%: 18,000,000 × 0.04 = 720,000 additional record-passes, so total passes = 18,720,000. Raw duration = 18,720,000 ÷ 250,000 = 74.88 hours. Add 20% contingency: 74.88 × 1.2 = 89.856 hours. Divide by the 8-hour nightly window: 89.856 ÷ 8 = 11.232 nights - and you cannot book a fraction of a night, so round up to 12. Option A skips both the re-runs and the contingency (72 ÷ 8 = 9); B applies contingency but not re-runs (86.4 ÷ 8 = 10.8, then wrongly rounds down); C computes 11.232 and rounds down instead of up. Two disciplines earn the mark: apply every stated adjustment exactly once, and round in the direction reality demands - capacity plans round up. This mirrors the planning arithmetic behind the upgrade and migration guidance your role provides.

**Question 16 (moderate) - Weighted average data quality score**

Your quarterly assurance report scores three data domains on completeness. The domains differ in size, and the board wants a single estate-wide figure weighted by record volume:

| Domain | Records (millions) | Completeness |
|---|---|---|
| Citizen | 10 | 96% |
| Case | 6 | 88% |
| Finance | 4 | 93% |

What is the volume-weighted average completeness?

A. 92.3%
B. 92.9%
C. 93.0%
D. 95.0%

**Correct answer: C.**

**Explanation:** Weighted average = Σ(weight × value) ÷ Σ(weights). Numerator = (10 × 96) + (6 × 88) + (4 × 93) = 960 + 528 + 372 = 1,860. Denominator = 10 + 6 + 4 = 20. Weighted average = 1,860 ÷ 20 = 93.0%. The simple (unweighted) mean is (96 + 88 + 93) ÷ 3 = 92.3% (option A), the figure a careless report would publish; option B is a near-miss designed to catch rounding guesses, and D cherry-picks something between the two largest domains. The gap between 92.3% and 93.0% looks small, but on 20 million records it represents 140,000 records' worth of difference in the claim you are signing off - and taking responsibility for the assurance of data solutions means your published figures must survive scrutiny. When options sit close together like these, compute exactly; estimation is not enough.

**Question 17 (easy) - Decommission cost avoidance**

Running the legacy reporting database costs £4,500 per month in hosting plus £1,500 per month in support. Decommissioning it on schedule at the end of month 4 (of a 12-month financial year) avoids those costs for the remainder of the year. How much does the organisation avoid spending this financial year?

A. £24,000
B. £36,000
C. £48,000
D. £72,000

**Correct answer: C.**

**Explanation:** Combined monthly cost = £4,500 + £1,500 = £6,000. Months avoided = 12 − 4 = 8 (months 5 to 12 inclusive). Avoided spend = 8 × £6,000 = £48,000. Option A uses only the hosting element over the wrong period; B multiplies £6,000 by 6 months, miscounting the remainder of the year; D charges the full 12 months, forgetting the system ran (and cost money) for the first four. Two habits close out this section as they close out most numeric tests: combine cost components before multiplying, and count time periods carefully - "end of month 4" leaves eight billable months, not six and not twelve. Being able to quote a crisp, correct cost-avoidance figure is also one of the most persuasive tools you have when making the case for the decommission and archive work your role guides.

### Preparation tips

- **Rehearse the four core moves.** Percentage change, percentage-point change, ratios, and rate × volume cover the large majority of questions. Drill each until the setup is automatic and only the arithmetic needs the calculator.
- **Always identify the denominator before calculating.** "Percentage of what?" is the question that separates right from wrong answers far more often than the arithmetic does.
- **Use the calculator, but estimate first.** A rough order-of-magnitude estimate ("about a quarter, so around 25%") catches keying errors instantly.
- **Practise with your own profiling outputs.** Take a real profiling report or capacity spreadsheet from your work and quiz yourself: what is the null rate, the growth rate, the projected volume? Familiar material builds speed.
- **Bank the easy marks.** Ratio and single-step percentage questions take 30 seconds; multi-step cost questions take three minutes. Do the quick ones first if the platform allows navigation.
- **Write the units.** TB, rows, £, hours - carrying units through each step prevents the most embarrassing multi-step errors, exactly as it does in real capacity planning.

### Common pitfalls

- **Misreading table labels and scale qualifiers.** Confusing "per week" with "per month", or missing "in thousands", silently multiplies your answer by the wrong factor. Read the header row and units first, data second.
- **Confusing percentage change with percentage points.** As Question 11 showed, these differ hugely; assessments test the distinction deliberately.
- **Over-calculating.** If options are far apart, an estimate identifies the answer without full computation. Precision is only needed when options are close.
- **Time sink questions.** A single multi-stage cost question can consume five easier questions' worth of time. Flag, skip, return.
- **Dividing by the wrong base.** Change ÷ original for growth; the "new value" base is the single most common trap in these tests, appearing in Questions 1 and 14 above.
- **Ignoring distractor columns.** Real-feeling tables include numbers you do not need. Identify what the question asks before touching the data, just as you would in a genuine source system analysis.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment evaluates how well you understand, analyse, and draw correct conclusions from written material of the kind your role handles every day: data policies, standards documents, governance board minutes, technical guidance, and stakeholder emails. It mirrors the exact reading demands of your work - dense, precise, occasionally ambiguous prose from which you must extract exactly what is stated, no more and no less.

Typical format and timing: you read a short passage, then answer questions about it under time pressure - often less than a minute per question. The dominant format is **True / False / Cannot Say**: a statement is True if the passage supports it, False if the passage contradicts it, and Cannot Say if the passage provides insufficient information either way. Some assessments add multiple-choice comprehension questions asking for the best summary, the author's main point, or the correct application of a stated rule. The golden rule throughout: answer strictly from the text provided, ignoring your outside knowledge - even when (especially when) you know the subject well.

This discipline matters intensely for a data architect. Policies and standards are legal-adjacent documents where the difference between "must", "should", and "may" changes what teams are obliged to do; misreading them causes real compliance failures. Equally, the Cannot Say category trains the intellectual honesty your assurance work requires: recognising when a document simply does not answer the question being asked of it.

### What it measures for your role

- **Data standards**: using data policies, processes, and standards effectively begins with reading them precisely - and working with subject matter experts to develop standards means noticing where drafted wording fails to say what its authors intend. Most passages here are policy or standard excerpts.
- **Data governance (data architect)**: taking responsibility for the assurance of data solutions and making recommendations to ensure compliance requires distinguishing what a policy actually mandates from what people assume it does; analysing the impact if a standard is breached starts with establishing exactly what the standard says.
- **Communicating between the technical and non-technical**: managing differing stakeholder perspectives often turns on what an email or minute actually said versus what each party remembers. Several questions use stakeholder correspondence.
- **Communicating data** and **data analysis and synthesis**: presenting clear insights includes accurately representing written findings; comprehension questions test whether you can identify the main point of a dense report.
- **Metadata management**: definitions in data dictionaries and metadata repositories are prose artefacts; keeping information accurate and up to date means reading and writing definitions with exactness.
- **Strategic thinking**: explaining the strategic context of your work depends on correctly digesting strategy documents rather than skimming them.

### Practice questions

**Passage A - Data retention policy excerpt**

*"All datasets classified as containing personal data must be assigned a named information asset owner before they may be loaded to any shared analytical environment. Datasets without personal data should also be assigned an owner, although loading may proceed while ownership is being confirmed. Retention periods are set by the information asset owner in accordance with the departmental retention schedule; where no period has been set, a default of two years from date of load applies. The platform team must review unowned datasets quarterly and may suspend access to any dataset that has remained unowned for more than six months."*

**Question 1 (easy) - True / False / Cannot Say**

A dataset containing personal data may be loaded to a shared analytical environment while its owner is still being confirmed.

**Correct answer: False.**

**Explanation:** The passage says personal-data datasets "must be assigned a named information asset owner before they may be loaded". The allowance to load "while ownership is being confirmed" applies explicitly and only to "datasets without personal data". The statement directly contradicts the text, so it is False - not Cannot Say, because the passage does answer the question. Notice the structure of the trap: the true rule for one category is offered as if it applied to the other. Policies do this to readers constantly; the fix is to bind each rule to its subject clause.

**Question 2 (easy) - True / False / Cannot Say**

If no retention period has been set for a dataset, it must be deleted two years after the date of load.

**Correct answer: Cannot Say.**

**Explanation:** The passage says a default period "of two years from date of load applies" where none has been set - but it never states what happens when the period expires. Deletion, archiving, review, or renewal are all consistent with the text; the passage simply does not say. This is the essence of Cannot Say: the statement is plausible and may even match your organisation's real practice, but the passage provides insufficient information. Candidates who know retention regimes well are the most likely to wrongly answer True here - outside knowledge is the enemy in this format.

**Question 3 (moderate) - True / False / Cannot Say**

The platform team is required to suspend access to datasets that have been unowned for more than six months.

**Correct answer: False.**

**Explanation:** The passage says the platform team "may suspend access" - a permission, not an obligation. The statement's "is required to" converts may into must, which the text does not support; since the passage states the weaker rule explicitly, the stronger claim contradicts the text as written, making the statement False. Watch modal verbs relentlessly: must/shall (obligation), should (recommendation), may (permission) form the load-bearing skeleton of every standard you will ever draft or assure, and assessments test them because real compliance disputes turn on them.

**Question 4 (moderate) - Multiple choice**

Which of the following best summarises the passage's overall purpose?

A. To prohibit loading any dataset without an information asset owner.
B. To establish ownership and retention rules for datasets in shared analytical environments, with stricter requirements for personal data.
C. To set a universal two-year retention period for departmental data.
D. To require the platform team to review all datasets quarterly.

**Correct answer: B.**

**Explanation:** B captures the full shape: ownership rules (strict for personal data, looser otherwise), retention setting with a default, and a review mechanism. A overstates - only personal-data datasets are blocked from loading unowned. C mistakes the fallback default for a universal rule. D narrows the quarterly review to "all datasets" when the passage limits it to "unowned datasets", and makes a side mechanism the main purpose. Best-summary questions reward the option that is both accurate and complete; three of the four options here are accurate-but-partial or complete-but-inaccurate.

**Passage B - Metadata standard consultation draft**

*"This standard requires every data element in scope to carry, as a minimum: a business definition agreed with the relevant subject matter expert; a named data steward; and a recorded source system. Technical metadata, including data type and length, is mandatory for elements implemented in physical systems but not for purely conceptual elements. The standard applies to all new development from 1 April. Existing elements must be brought into conformance within eighteen months of that date, except where a system is scheduled for decommission within that window, in which case conformance work is not required. Departments were consulted on an earlier draft; a majority favoured a twelve-month conformance window, but the board extended it after impact analysis showed the shorter window was unachievable for two large legacy estates."*

**Question 5 (moderate) - True / False / Cannot Say**

Under the standard, a purely conceptual data element must record a data type.

**Correct answer: False.**

**Explanation:** The passage states technical metadata "including data type and length, is mandatory for elements implemented in physical systems but not for purely conceptual elements". The statement asserts the opposite of the stated exemption, so it is False. The question tests whether you track which subject each requirement attaches to - the same reading skill you use when you provide input into data dictionaries and must know which fields are compulsory for which class of element.

**Question 6 (moderate) - True / False / Cannot Say**

A legacy system scheduled for decommission nineteen months after 1 April is exempt from conformance work.

**Correct answer: False.**

**Explanation:** The exemption applies "where a system is scheduled for decommission within that window" - the window being eighteen months from 1 April. Nineteen months falls outside the window, so the exemption does not apply; the system must be brought into conformance. The statement contradicts the rule as written, so it is False. Careful: the intuitive reaction ("it's being decommissioned anyway, surely it's exempt") is a real-world judgement, not a textual one - and this format scores the text. In practice you might well recommend a pragmatic exception, but that is a governance decision, not what the standard says.

**Question 7 (hard) - True / False / Cannot Say**

The board considered departmental preferences when setting the conformance window.

**Correct answer: True.**

**Explanation:** The passage records that departments were consulted, that a majority favoured twelve months, and that "the board extended it after impact analysis". The sequence shows the board had the consultation result before it (it "extended" the very window the majority had favoured shorter), so departmental preferences were considered - even though the board decided against the majority view. This is a subtle True: considering preferences does not mean following them. Candidates often answer False because the board went against the majority, or Cannot Say because the word "considered" never appears; but the passage's narrative logically entails consideration. When the inference is this direct and unavoidable, True is safe; reserve Cannot Say for genuine gaps.

**Question 8 (moderate) - Multiple choice**

According to the passage, which combination is the minimum required for a conceptual data element?

A. Business definition, data steward, source system
B. Business definition, data steward, source system, data type
C. Business definition and data steward only
D. Data steward, source system, data type, and length

**Correct answer: A.**

**Explanation:** The universal minimum is the three items listed: agreed business definition, named data steward, recorded source system. Technical metadata (type and length) is additionally mandatory only for physically implemented elements, so a conceptual element needs just the three - option A. B adds a requirement the passage exempts; C drops one the passage requires; D swaps a required item for exempt ones. This is a pure extraction question: list what the text lists, resisting both addition and subtraction. It is also, not coincidentally, exactly how you would apply this standard when maintaining a metadata repository.

**Passage C - Email from a service manager**

*"Thanks for the draft target data model. I have to be honest: my team are worried. The proposal merges our local 'client' table into the corporate 'party' entity, and we've been told verbally that this means we lose the three status flags we depend on for daily triage. If that's true, it's a showstopper for us. I also gather the migration is pencilled in for the same quarter as our peak service period, which last year saw a 40% increase in caseload. We do support the single-view-of-the-citizen ambition - genuinely - but we need evidence that day-one operations are protected. Could you walk us through the mapping at Thursday's session? Our operations lead will attend, and she has final say on whether we sign off the design."*

**Question 9 (easy) - True / False / Cannot Say**

The service manager's team opposes the single-view-of-the-citizen ambition.

**Correct answer: False.**

**Explanation:** The email states plainly: "We do support the single-view-of-the-citizen ambition - genuinely". The statement contradicts this, so it is False. Simple - but important. In real stakeholder management, mistaking concern about implementation for opposition to strategy poisons relationships unnecessarily. The email carefully separates the two, and a careful reader (and assessment candidate) preserves that separation. Managing differing stakeholder perspectives starts with representing each perspective accurately.

**Question 10 (moderate) - True / False / Cannot Say**

The target data model removes the three status flags the team depends on.

**Correct answer: Cannot Say.**

**Explanation:** The email reports that the team have "been told verbally" that the merge "means we lose the three status flags", and the writer immediately conditions it: "If that's true...". The passage gives you a second-hand, unverified claim, explicitly flagged as unconfirmed by its own author. Whether the model actually removes the flags is not established either way - so Cannot Say. This distinction between what a document asserts and what it merely reports someone saying is one of the sharpest tools in verbal reasoning, and in your working life it is the difference between "the design drops the flags" and "the team believe the design drops the flags" - two very different problems.

**Question 11 (moderate) - True / False / Cannot Say**

The operations lead has the authority to approve or reject the design on behalf of the service team.

**Correct answer: True.**

**Explanation:** The email says the operations lead "has final say on whether we sign off the design". "Final say" over sign-off is precisely the authority to approve or reject on the team's behalf, so the statement is supported by the text: True. Identifying the actual decision-maker from correspondence - which is not always the person writing - is a practical skill for anyone who must be an advocate for the team externally and host discussions where sign-off is at stake. Note what would make this Cannot Say: if the email had merely said the operations lead "will attend", her authority would be unstated.

**Question 12 (hard) - Multiple choice**

Which of the following would most directly address the concerns raised in the email?

A. A presentation on the strategic benefits of the single view of the citizen.
B. A written guarantee that the migration will be cancelled.
C. A walkthrough of the field-level mapping showing what happens to the three status flags, plus the proposed migration timing relative to the peak period.
D. An invitation to the operations lead to join the data governance board.

**Correct answer: C.**

**Explanation:** Anchor each option to the concerns the text actually raises: (1) the possible loss of three status flags, and (2) migration timing colliding with the peak quarter, wrapped in a request to "walk us through the mapping". Option C answers both concerns and the explicit request. A addresses a concern the team does not have - they already support the strategy. B overcorrects: the team asked for evidence and protection, not cancellation. D offers governance participation nobody requested and leaves both stated concerns untouched. In assessments and in stakeholder work alike, the strongest response maps one-to-one onto what was actually said - a reading-comprehension habit that doubles as a communication habit.

**Passage D - Data governance board minutes (extract)**

*"Item 4: Quarterly compliance report. The board noted that 14 of 17 in-scope systems now conform to the reference data standard, up from 11 last quarter. Of the three non-conforming systems, two have agreed remediation plans with dates inside the next quarter. The third, the grants platform, has no plan; its supplier contract ends in March and the service is under commercial review. The chair asked the data architecture function to prepare an impact analysis of continued non-conformance for the grants platform, covering downstream consumers of its reference data, and to present options - including read-only ring-fencing of its feeds - at the next meeting. The board agreed that no new consumers of grants platform reference data should be onboarded until the analysis is considered."*

**Question 13 (moderate) - True / False / Cannot Say**

Conformance with the reference data standard improved compared with the previous quarter.

**Correct answer: True.**

**Explanation:** The minutes state conformance is "up from 11 last quarter" to 14 of 17 systems. Fourteen exceeds eleven against the same denominator of in-scope systems, so the improvement is directly stated: True. Even in a True answer, verify the comparison is like-for-like - the passage keeps the scope at 17 in-scope systems, so the comparison holds. Reading compliance trends accurately is the raw material of your responsibility to monitor compliance with policies and standards and take action if needed.

**Question 14 (moderate) - True / False / Cannot Say**

The grants platform will be decommissioned when its supplier contract ends in March.

**Correct answer: Cannot Say.**

**Explanation:** The minutes say the contract "ends in March and the service is under commercial review". A review may end in decommission, renewal, re-procurement, or in-housing - the text does not say which. The statement is a plausible forecast, not a recorded fact, so Cannot Say. Minutes are a genre that rewards this precision: they record decisions actually taken (no new consumers to be onboarded) alongside contextual facts (contract end date) and open questions (the review) - and conflating the three categories is how organisations come to believe decisions were made that never were.

**Question 15 (hard) - Multiple choice**

Which action is the data architecture function required to complete before the next board meeting?

A. Ring-fence the grants platform's feeds as read-only.
B. Prepare an impact analysis of continued non-conformance, covering downstream consumers, and present options.
C. Onboard no new consumers of any reference data.
D. Agree a remediation plan with the grants platform supplier.

**Correct answer: B.**

**Explanation:** The chair "asked the data architecture function to prepare an impact analysis... and to present options... at the next meeting" - that is the function's required action, option B. A confuses an option to be presented ("including read-only ring-fencing") with a decision already taken; the board has not ordered ring-fencing. C misstates scope: the onboarding freeze applies to "grants platform reference data", not all reference data - and it is a board-wide decision, not an action assigned to the architecture function. D belongs to nobody in the text; the two remediation plans that exist were agreed by other systems' teams. Assessments love minutes because actions, options, and decisions sit one sentence apart; so does real governance, where taking responsibility for assurance means executing exactly the action you were assigned.

**Passage E - Guidance note on data warehouse layering**

*"The departmental warehouse architecture comprises three layers. The landing layer holds raw extracts exactly as received; no transformation is permitted here, and access is restricted to the platform team. The integration layer conforms data to the enterprise model; all business rules applied in this layer must be documented in the transformation register before deployment. The presentation layer exposes curated data marts to analytical users; marts may be created only from integration-layer objects, never directly from landing data. Exceptionally, a time-boxed tactical mart may be built from landing data with the written approval of the head of data architecture, provided it is registered on the exceptions log and reviewed within ninety days. Two tactical marts approved under the previous guidance remain in operation."*

**Question 16 (moderate) - True / False / Cannot Say**

Analytical users are permitted to query raw extracts in the landing layer.

**Correct answer: False.**

**Explanation:** The passage restricts landing-layer access "to the platform team", and analytical users are served by the presentation layer. A statement granting analytical users access to landing data contradicts the stated restriction, so it is False. Note that the tactical-mart exception does not rescue the statement: even a tactical mart built from landing data is still a mart that users query - the users still do not query the landing layer itself. Precision about which object carries the permission is the same precision your layered warehouse designs depend on.

**Question 17 (hard) - True / False / Cannot Say**

The two tactical marts currently in operation were reviewed within ninety days of creation.

**Correct answer: Cannot Say.**

**Explanation:** The ninety-day review requirement belongs to the current guidance's exception mechanism; the two operating marts were "approved under the previous guidance", whose terms the passage never describes. Whether they were reviewed, and on what schedule, is simply not stated. Candidates leap to True (assuming the same conditions applied before) or False (assuming the old regime was laxer) - both are speculation. The passage's careful phrase "under the previous guidance" is a scope boundary, and everything beyond it is Cannot Say territory. Legacy artefacts governed by superseded rules are a daily reality in warehouse estates, and this question rehearses precisely that disentangling.

**Question 18 (moderate) - Multiple choice**

A delivery team wants a new mart, built directly from landing data, to meet an urgent ministerial deadline. According to the passage, what would make this permissible?

A. Documenting the business rules in the transformation register.
B. Written approval from the head of data architecture, registration on the exceptions log, and a review within ninety days.
C. Restricting the mart's access to the platform team.
D. Nothing - marts may never be built from landing data.

**Correct answer: B.**

**Explanation:** The passage carves out exactly one route: "a time-boxed tactical mart may be built from landing data with the written approval of the head of data architecture, provided it is registered on the exceptions log and reviewed within ninety days" - option B reproduces all three conditions. A applies to integration-layer business rules, not the exception route. C garbles the landing-layer access restriction into a mart condition the passage never states. D quotes the general rule ("never directly from landing data") while ignoring the explicit exception that immediately follows - a reminder that in standards documents, as in this test, the sentence after the rule can matter as much as the rule. Reading exception clauses completely is a core habit for anyone who assures compliance and analyses the impact when standards are breached or bent.

### Preparation tips

- **Read the statement before re-reading the passage.** Identify the key claim, then hunt for the sentence that confirms, contradicts, or fails to address it. Scanning with a target is faster than absorbing everything first.
- **Master the modal verbs.** Must, shall, should, may, and might carry the legal weight in every policy and standard. Half of False answers in policy-based questions come from a modal being silently upgraded or downgraded.
- **Rehearse the Cannot Say discipline.** For each practice statement, ask: "Could I point to the exact words that settle this?" If not, Cannot Say - however plausible the claim. Your subject knowledge is a liability in this format; park it.
- **Distinguish assertion from report.** "The design drops the flags" versus "the team say the design drops the flags" are different facts. Passages built on emails and minutes test this constantly, and so does your inbox.
- **Practise on real documents.** Take a page of your organisation's data policy or a standard you helped draft, write five True/False/Cannot Say statements about it, and answer them a day later. This builds both assessment speed and drafting sharpness.
- **Keep pace.** At under a minute per question, if a statement resists resolution after two careful scans, choose your best-supported answer and move on. Verbal tests reward decisiveness anchored in text.

### Common pitfalls

- **Importing outside knowledge.** The most common failure mode for experienced professionals: you know how retention or metadata standards usually work, so you answer from experience rather than the passage. The test scores the passage.
- **Confusing "likely" with "stated".** A passage that says an outcome is expected or probable does not support a statement that it will happen. Match the certainty level of the statement to the certainty level of the text.
- **Treating Cannot Say as a weak answer.** Candidates under-use it, feeling it is a cop-out. It is not: it is frequently the designed correct answer, and choosing it on textual grounds demonstrates exactly the assurance mindset your role requires.
- **Missing scope-limiting phrases.** Words like "in-scope", "personal data", "unowned", and "new development" quietly restrict every rule they touch. Statements that widen the scope are False or Cannot Say, not True.
- **Reading the whole passage exhaustively first.** Under time pressure, targeted scanning for the statement's keywords beats full absorption. Save deep reading for the one sentence that decides the answer.
- **Letting sentiment colour judgement.** An email's frustrated tone does not change what it factually asserts. Score the propositions, not the emotion - in the test and in the meeting afterwards.

## Workplace job-specific situational judgement assessment

### About this assessment

A workplace job-specific situational judgement assessment evaluates your decision-making, interpersonal skill, and professional conduct through realistic workplace dilemmas. Unlike the cognitive, numeric, and verbal tests, there is often no single objectively right answer computed from data - instead, several responses may seem reasonable, and the assessment measures how well your choices align with the values and behaviours the role and organisation require. For your role, that means alignment with UK public sector values: meeting user needs, transparency, collaboration across disciplines, accessibility and inclusion, careful stewardship of public money and public data, and evidence-based decision-making.

Typical format and timing: each item presents a short scenario - a conflict, an ethical dilemma, an operational challenge - followed by several possible actions. You are usually asked to pick the **most effective** and **least effective** actions, or to rank or rate all the options. These assessments are generally untimed or generously timed, because they measure natural judgement rather than speed. Answer as the professional you are at work, not as an idealised hero or a cynical survivor; well-designed tests detect both.

The scenarios below are drawn directly from a data architect's real working life: design reviews with anxious service teams, standards breaches, governance pressure near go-live, difficult dynamics in multidisciplinary teams, and the constant balancing of strategic data ambitions against operational reality.

### What it measures for your role

- **Communicating between the technical and non-technical**: several scenarios test whether you can communicate effectively with technical and non-technical stakeholders, support and host discussions within a multidisciplinary team with potentially difficult dynamics, advocate for the team externally, and manage differing stakeholder perspectives.
- **Data governance (data architect)** and **data standards**: dilemmas about compliance, assurance, and standards breaches test whether you take responsibility for the assurance of data solutions, make recommendations to ensure compliance, monitor compliance in a team and take action if needed, and analyse the impact if a standard is breached.
- **Problem management**: scenarios about recurring incidents test whether you investigate patterns and trends, consult specialists effectively, determine the appropriate resolution, and determine preventative measures rather than settling for quick fixes.
- **Data innovation**: judgement about when and how to pursue new tools and uses of data - with enthusiasm and with due diligence.
- **Communicating data**: dilemmas about visuals and reported figures test your commitment to aligning data honestly to the needs of the end user.
- **Strategic thinking**: choices that weigh immediate convenience against the organisation's strategic data direction, as defined by chief data architects.

### Practice questions

**Question 1 (easy) - The baffled service manager**

In a design review, a service manager stares at your entity-relationship diagram and says, "I'll be honest, this means nothing to me - I just need to know my caseworkers can still see client history on one screen." Several other non-technical attendees look relieved that someone said it.

A. Continue the walkthrough as planned; the technical audience members still need the detail, and the slides were circulated in advance.
B. Switch mode: put the diagram aside, walk through a day-in-the-life example of a caseworker viewing client history in the new design, and offer a separate technical session for those who want the detail.
C. Apologise and end the session early, promising to send a simplified written summary.
D. Ask a business analyst to translate for the service manager while you continue presenting the model.

**Most effective: B. Least effective: A.**

**Explanation:** Option B is the heart of communicating between the technical and non-technical: the diagram is your artefact, not the stakeholder's need, and re-anchoring the discussion in the user's real scenario (a caseworker's screen) serves everyone in the room - including the quiet majority who were also lost. Splitting the technical detail into its own session respects both audiences. Option A is least effective because it prioritises your plan over your audience's stated needs; you would finish the meeting having communicated nothing to the people whose sign-off you need. C abandons a live opportunity - the stakeholders are present and engaged - and a written summary rarely answers the questions a conversation surfaces. D outsources your own core skill mid-meeting and subtly tells the service manager their question was a distraction. Public sector design culture starts from user needs; so should your meeting.

**Question 2 (moderate) - The repeat standards breach**

Monitoring shows a delivery team has, for the third sprint running, created database objects that breach the naming and modelling standards. Their tech lead is capable and busy, and previously promised to fix things "when the pressure eases". The breaches are starting to propagate into the warehouse integration layer.

A. Escalate immediately to the head of delivery, attaching the three sprints of evidence.
B. Fix the objects yourself over the weekend and mention it casually to the tech lead.
C. Meet the tech lead, share the evidence and the downstream impact analysis, agree a remediation plan with dates, and be clear that continued drift will need escalating - then follow up as agreed.
D. Add stricter automated checks to the deployment pipeline so non-conforming objects cannot be deployed, without discussing it with the team first.

**Most effective: C. Least effective: B.**

**Explanation:** Your skill profile is explicit: monitor compliance with policies and standards in a team and take action if needed, and analyse the impact if a standard is breached. Option C does all of it - evidence, impact, a concrete plan, a transparent warning about escalation, and follow-through - while preserving the collaborative relationship a multidisciplinary environment depends on. Option B is least effective: it hides the problem, sets a precedent that the architect will silently clean up after delivery teams, fixes symptoms rather than behaviour, and burns your weekend as a subsidy for non-compliance. A is premature - escalation is a legitimate later step, but leaping there first without giving a capable colleague a structured chance to remediate damages trust and wastes senior attention. D has real merit as a preventative measure (and might follow from C's plan), but imposing pipeline controls without discussion invites workarounds and resentment; transparency about controls is part of good governance.

**Question 3 (moderate) - Go-live pressure versus assurance**

A high-profile service is due to go live in nine days. Your data assurance review finds that the solution stores citizens' contact history unencrypted in a shared schema, contrary to data policy. The programme manager says: "We can't slip the date. Log it as a known issue and we'll fix it in the next release - the Minister has announced this."

A. Agree to log it as a known issue; the announcement makes the date immovable and the fix is coming anyway.
B. Set out the breach, its impact, and remediation options in writing to the programme manager and the senior responsible owner, recommending either a pre-go-live fix or a formal, documented risk acceptance at the right level - and offer to help scope the quickest compliant fix.
C. Refuse to sign off the assurance and inform the programme board that go-live cannot proceed under any circumstances.
D. Quietly raise it with a friend on the security team so it becomes their problem rather than yours.

**Most effective: B. Least effective: D.**

**Explanation:** Option B does what taking responsibility for the assurance of data solutions and making recommendations to ensure compliance actually means in government: the breach is documented transparently, the decision is escalated to the accountable owner with options rather than ultimatums, and you contribute to solving the problem (scoping the quick fix) rather than just certifying it. Crucially, risk acceptance is a legitimate outcome - but only when made knowingly, at the right level, in writing. Option D is least effective: it is opaque, evades your own accountability, converts a governance issue into corridor politics, and delays action on citizens' data - the opposite of transparency. A silently absorbs a policy breach on a programme manager's say-so, leaving no accountable decision trail; if the data leaks, "we logged it" protects no one, least of all citizens. C overplays the architect's authority - blanket refusal without options ignores the possibility of a properly governed risk decision and positions you as an obstacle rather than an adviser.

**Question 4 (moderate) - The clashing seniors**

You are hosting a data model working session. Ten minutes in, a senior developer and a senior analyst begin talking over each other about whether "customer" and "citizen" are one entity or two. The exchange grows sharp; other attendees have gone quiet, and two junior members look uncomfortable.

A. Let the two seniors argue it out - they have the deepest knowledge, and the answer matters.
B. Pause the debate, acknowledge both positions have substance, capture the disagreement as a named decision point with the evidence each side would need, park it, and move the session on - then convene the two seniors separately with the relevant subject matter expert.
C. Side with the senior developer, whose view matches your own instinct, and move on.
D. Adjourn the meeting and ask both to send you their positions in writing.

**Most effective: B. Least effective: A.**

**Explanation:** This is the "support and host discussions within a multidisciplinary team, with potentially difficult dynamics" skill in its purest form. Option B protects the session's purpose, dignifies both experts, converts heat into a structured decision with evidence criteria (very much how entity questions should be settled), and - importantly for inclusion - restores a room in which quieter and junior colleagues can contribute. Option A is least effective: unmanaged conflict between seniors silences everyone else, models poor behaviour, and rarely converges; the facilitator's passivity is itself a decision. C settles a modelling question by hierarchy and instinct rather than evidence, and publicly picks a winner - both bad modelling practice and bad facilitation. D is not terrible, but it sacrifices the assembled group's time and momentum for a problem B can contain in two minutes, and written position papers tend to harden positions rather than reconcile them.

**Question 5 (hard) - The stale repository discovery**

Preparing an integration impact analysis for a major upgrade, you discover the metadata repository is significantly out of date: dozens of dependencies added in the last year were never recorded. The analysis is due at the architecture board in three days, and the upgrade decision depends on it.

A. Run the analysis on the repository as it stands and present it without comment - the repository is the official source.
B. Delay the board paper indefinitely until the repository is fully remediated.
C. Rapidly triage: verify the dependencies for the systems actually in the upgrade's blast radius (consulting the delivery teams who know them), present the analysis with an explicit statement of confidence and coverage, and propose a funded remediation plan for the repository as a follow-up action.
D. Present the analysis but verbally mention that the repository "may have some gaps" if anyone asks.

**Most effective: C. Least effective: A.**

**Explanation:** Option C combines the practical and the principled: it focuses verification effort where the decision needs it (the upgrade's blast radius), consults specialists effectively - a named behaviour in your problem management skill - is transparent about confidence and coverage, and converts the discovery into a preventative measure (the remediation plan), which is exactly how problem management should end. Option A is least effective because it knowingly presents materially flawed analysis to a decision-making board as though it were sound - a transparency failure that could cause a service-affecting outage and, when the gaps surface later, will undermine trust in the architecture function itself. B fails the organisation in the other direction: indefinite delay leaves the board deciding with no analysis at all, and "wait for perfect data" is rarely a public-service option. D's difference from A is cosmetic; material caveats belong in the paper, stated precisely, not held back for a lucky question.

**Question 6 (moderate) - Strategy versus the local shortcut**

The chief data architect's target architecture mandates that new services consume citizen reference data from the corporate master data service. A delivery team you support asks you to endorse a local copy instead: "The master service's API is slower and we'd own our data. We can sync it later. You know our deadline."

A. Endorse the local copy - the team knows its needs best, and the strategy can catch up later.
B. Decline to endorse it, explain the strategic rationale (divergent copies are how the citizen-view problem arose), quantify the API performance gap with the master data team, and jointly pursue either a fix, a caching pattern consistent with the target architecture, or a time-boxed, documented exception with a convergence date.
C. Tell the team to raise it with the chief data architect and step away from the question.
D. Endorse the copy but ask the team to keep it quiet until after go-live.

**Most effective: B. Least effective: D.**

**Explanation:** Your role exists to fulfil the strategic data needs of the organisation as defined by chief data architects, and to explain the strategic context of your work - option B does both while genuinely engaging with the team's legitimate performance concern. Note its shape: hold the line on the destination, be flexible and evidence-led about the route (caching patterns and governed exceptions are real architecture tools, not defeats). Option D is least effective by a distance: it is the strategic failure of A plus deliberate concealment - a straightforward breach of the transparency that public sector working demands, and it makes you complicit in undermining the governance you are meant to uphold. A capitulates without analysis and "sync it later" is the origin story of most data quality problems. C is an abdication: escalation routes matter, but the architect on the ground is precisely the person who should shape the options before anything reaches the chief data architect.

**Question 7 (moderate) - The tempting new tool**

At a conference, a vendor demonstrates an impressive AI-assisted data catalogue that could transform your metadata management. The vendor offers a free three-month trial: "Just point it at a copy of your databases and it does the rest." Your organisation has procurement rules and a data protection assessment process, and your current catalogue contract runs for another year.

A. Decline to think about it further - the current contract makes it pointless.
B. Accept the trial and point the tool at a copy of production databases; it is only a trial, and innovation requires moving fast.
C. Capture the capability gap the demo revealed, arrange a deeper demonstration using vendor-supplied or synthetic data, and raise a proper evaluation - including data protection assessment and procurement advice - timed to inform the contract renewal.
D. Recommend immediate procurement of the new tool to replace the incumbent.

**Most effective: C. Least effective: B.**

**Explanation:** Showing awareness of opportunities for innovation with new tools is one of your named skills, and option C exercises it responsibly: the innovation signal is captured and pursued, but evaluation uses safe data, follows the data protection and procurement processes that safeguard public money and citizens' data, and lands at the moment (contract renewal) when it can actually change something. Option B is least effective: pointing an unassessed external tool at copies of production databases - which will contain real citizen data - is a serious data protection failure dressed up as agility; "it is only a trial" protects nobody. A mistakes patience for pointlessness and would discard a year of preparation time an evaluation could use well. D leaps from demonstration to procurement with no evaluation, no due diligence, and no regard for existing commitments - enthusiasm without evidence, which is not innovation but gambling.

**Question 8 (hard) - The recurring data quality incident**

For the fourth time in two months, the overnight citizen data load has failed reconciliation, and each time the operations team has patched the affected records manually. The service desk treats each failure as a closed incident. You notice the failures cluster around end-of-month processing.

A. Praise the operations team's fast patching and leave the arrangement in place - the service has never actually gone down.
B. Open a problem record, analyse the pattern (including the end-of-month clustering you spotted), consult the source system's specialists on month-end behaviours, identify the root cause, implement a fix, and add a reconciliation alert to catch any recurrence early.
C. Instruct the operations team to stop patching records so the failures become visible enough to force investment in a fix.
D. Ask the service desk to merge future occurrences into a single ticket to reduce noise.

**Most effective: B. Least effective: C.**

**Explanation:** This is your problem management skill rendered as a scenario: initiate and monitor actions to investigate patterns and trends to resolve problems, effectively consult specialists where required, determine the appropriate resolution, and determine preventative measures. Option B performs the full cycle - pattern analysis (the month-end clustering is the analytical thread), specialist consultation, root cause, fix, and a preventative alert. Option C is least effective because it deliberately degrades citizens' data quality to manufacture pressure - harming users as a negotiating tactic is indefensible in public service, whatever the tactical logic. A confuses the absence of outage with the absence of a problem: manual patching is unsustainable, error-prone, and hides a defect that will eventually strike somewhere less patchable. D is administrative tidying that actively reduces the visibility of a pattern that needs investigating - the opposite of problem management.

**Question 9 (moderate) - The flattering dashboard**

A programme director reviewing your draft data quality dashboard asks you to change the completeness chart's vertical axis to start at 90% rather than zero, "so the improvement is actually visible", ahead of a board meeting where the programme's funding is discussed.

A. Make the change - axis choices are presentational, and the underlying numbers are unchanged.
B. Refuse and report the request to the board as attempted manipulation.
C. Explain that a truncated axis on its own can mislead; offer an honest alternative that makes the genuine improvement visible - for example, a supplementary trend chart of the change itself, clearly labelled axes, or annotated percentage-point gains - and agree the final visual with the director.
D. Keep the zero-based chart but present the truncated version separately to the board yourself, with a caveat.

**Most effective: C. Least effective: B.**

**Explanation:** Communicating data honestly is a named part of your role: awareness that data needs to be aligned to the needs of the end user - here, a board that needs an accurate picture of progress. Option C treats the director's request as containing a legitimate need (real improvement is invisible at full scale) wrapped in a problematic method, and solves the need honestly: annotation, change-focused charts, and clear labelling are the honest craft of visualisation. Option B is least effective: it escalates a routine, probably innocent presentational request into an accusation of misconduct, destroying a working relationship and your reputation for proportionality - the director asked a question, not committed a fraud. Option A is genuinely poor (truncated axes without clear signalling do mislead, and the funding context raises the stakes) but it at least lacks B's relationship damage; in a most/least format, B's disproportion makes it the standout failure. D is muddled - presenting two competing charts with a mumbled caveat serves neither honesty nor clarity.

**Question 10 (moderate) - The informal data request**

An analyst from another department emails you directly: "You have the citizen contact dataset in your warehouse, right? Can you extract me a copy with postcodes and dates of birth? It's for a genuinely good piece of cross-government analysis and our deadline is Friday." No data sharing agreement exists between the organisations for this dataset.

A. Send the extract - cross-government collaboration is a public sector value, and the purpose sounds worthwhile.
B. Ignore the email; if it matters, they will follow a proper channel eventually.
C. Reply promptly and warmly: explain that this dataset needs a data sharing agreement and the data owner's approval, copy in the information asset owner, and offer practical help - the fastest route to a lawful share, whether anonymised or aggregated data might meet the need, and what is realistic by Friday.
D. Send an anonymised version of the extract without approval, since anonymisation removes the risk.

**Most effective: C. Least effective: A.**

**Explanation:** Option C is collaborative and compliant at once - which is the actual public sector standard: transparency and lawfulness are not obstacles to collaboration but the terms on which it earns public trust. It moves fast (prompt reply, practical routes, realistic framing of the deadline), engages the accountable people, and explores whether a lesser dataset serves the need - often it does. Option A is least effective: postcodes plus dates of birth are highly identifying personal data, and sharing them with no agreement and no owner approval is a serious breach regardless of how good the analysis is; good intentions are precisely how most data incidents begin. B fails the collaboration value and helps nobody - the analyst deserves a signposted route, not silence. D substitutes your private judgement for the governance process: whether anonymisation is adequate is itself an assessed decision (postcode and date of birth combinations are notoriously re-identifiable), and making it unilaterally repeats A's error with extra confidence.

**Question 11 (hard) - The unready consumer**

You are guiding the decommission of a legacy reporting database, scheduled for switch-off in six weeks and already twice delayed. Five of six consuming teams have migrated. The sixth - a small team producing statutory accessibility reports - says their replacement feed is blocked by a defect in the new platform and they cannot migrate in time. The platform team says the defect fix is "eight to ten weeks away". Running the legacy database costs money and carries security risk.

A. Hold the switch-off date; the sixth team has had two extensions already, and statutory reports are their problem to solve.
B. Delay the entire decommission by ten weeks until the defect is fixed.
C. Investigate a narrow bridge for the sixth team - for example, keeping a minimal read-only extract or interim feed for exactly the statutory data they need, with a documented end date tied to the defect fix - while switching off the rest on schedule, and put the trade-off with its costs and risks to the decommission board transparently.
D. Ask the sixth team to produce their statutory reports manually until the defect is fixed.

**Most effective: C. Least effective: A.**

**Explanation:** Decommission guidance is a named duty of your role, and option C shows the architect's craft: decompose the dependency (one team, one dataset, one statutory purpose) rather than treating switch-off as all-or-nothing; contain cost and security exposure by shrinking the legacy footprint to a minimal, read-only, time-boxed remnant; and put the decision transparently to the accountable board. It protects a statutory duty - and accessibility reporting carries inclusion weight beyond its size - without surrendering the programme. Option A is least effective: forcing a failure of statutory accessibility reporting to enforce a project date inverts public sector priorities; the two previous delays explain the frustration but do not change the duty. B pays ten weeks of full cost and risk for a problem one small bridge could isolate, and rewards the defect with programme-wide delay. D quietly converts a platform defect into sustained manual burden on a small team - operationally fragile exactly where accuracy is legally required, though at least it attempts continuity, which is why A remains the clearest failure.

### Preparation tips

- **Answer as your professional self on a good day.** Situational judgement tests reward your realistic best practice, not fantasy heroics or weary cynicism. If you would gather evidence, consult, and escalate transparently at work, choose those options here.
- **Look for the option that solves the need, not just the demand.** In several scenarios above, the strongest option digs beneath a stakeholder's stated request (a truncated axis, a local data copy) to the legitimate need underneath, and meets that instead.
- **Check each option against public sector values.** User needs, transparency, collaboration, accessibility, inclusion, lawful data handling, and stewardship of public money. An option that quietly sacrifices one of these - especially transparency - is rarely the intended "most effective".
- **Watch for the passive and the covert.** Ignoring emails, hiding caveats, fixing things secretly, keeping decisions quiet: options built on avoidance or concealment are classic "least effective" designs.
- **Escalate in the right order.** The strong pattern is: engage directly with evidence, agree a plan, be transparent that escalation follows if the plan fails - then escalate. Leaping straight to senior escalation, or never escalating at all, both score poorly.
- **Rehearse with colleagues.** Talk through a scenario from this section with a peer or mentor and compare instincts. Where you disagree is where your judgement will grow - and it is excellent preparation for hosting difficult discussions for real.

### Common pitfalls

- **Answering idealistically rather than effectively.** "Convene a workshop with all stakeholders" sounds virtuous, but if the scenario needs a decision by Friday, the practical-and-principled option beats the ceremonially perfect one.
- **Selecting passive options.** Choices that delay action, pass the problem wholesale to someone else, or wait for perfect information consistently score as weak - assessments are designed to catch them, as Question 5's "delay indefinitely" shows.
- **Ignoring the organisation's culture and values.** In UK government digital work, transparency, user needs, and lawful data handling outrank speed and hierarchy. An option that hits the deadline by hiding a breach fits a different culture, not this one.
- **Overcorrecting into aggression.** The mirror image of passivity: instant escalation, blanket refusal, public accusation. Question 9's "report the director to the board" shows how disproportion can make an otherwise principled instinct the worst option on the card.
- **Choosing what protects you rather than the service.** Options built around covering yourself ("mention it verbally if asked") score poorly against options that put accountability and evidence in the open.
- **Forgetting your actual authority.** The data architect advises, assures, recommends, and escalates; options where you unilaterally block programmes or approve data shares overstate the role, and options where you silently comply understate it. The strong options exercise exactly the authority the role really has.

## Conclusion

Well done for working through this resource - it represents a serious investment in your own development, and that investment pays off twice: once in any formal assessment you sit, and again every day in the quality of your professional judgement.

You have practised the four families of thinking that define excellent data architecture work. In the cognitive section, you reasoned from model rules, hunted inconsistencies between dictionaries and schemas, traced dependencies through lineage graphs, and sequenced decommissions safely. In the numeric section, you computed growth rates, deduplication percentages, load windows, archive savings, breach costs, and weighted quality scores - always with an eye on the right denominator. In the verbal section, you held policies, standards, emails, and minutes to their exact wording, giving must, should, and may their full weight and letting Cannot Say do its honest work. And in the situational judgement section, you weighed realistic dilemmas - standards breaches, go-live pressure, difficult meetings, tempting shortcuts - against the values that underpin public service: user needs, transparency, collaboration, accessibility, inclusion, and careful stewardship of citizens' data.

If some questions caught you out, be encouraged rather than discouraged: every trap you have now seen in practice is one you will recognise in a live assessment - and, more importantly, in live work. Revisit the sections where you felt stretched, redo the questions after a week or two, and notice how much faster the reasoning comes.

Keep building from here. Practise on your organisation's real artefacts - models, profiles, policies, board papers. Ask a mentor or your chief data architect to talk through how they would have handled the situational scenarios. Volunteer for the work that stretches these muscles: an assurance review, a difficult stakeholder session, an impact analysis. Continued professional development is not a separate activity from your role; it is the role, compounding quietly.

You have everything you need to walk into an assessment - or a design review - prepared, calm, and confident. Good luck!
