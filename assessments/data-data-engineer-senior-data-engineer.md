# Data Engineer (Senior Data Engineer) - Psychometric Assessment Resources

## Introduction

Welcome. This document is a practical, self-paced resource to help you prepare for the psychometric assessments most commonly used for senior data engineering roles in the UK Government Digital and Data profession. It has been written specifically for you: someone who designs and leads the implementation of data flows that connect operational systems with analytics and business intelligence platforms, who leads the build of data streaming systems, optimises code for performance, and leads work on database management.

Psychometric assessments are structured, standardised exercises that measure how you think, reason, and make decisions. They are widely used across the Civil Service and the wider public sector, both in recruitment and in professional development, because they offer an objective, evidence-based view of capability that complements interviews and technical exercises. For a senior data engineer, they matter for a very practical reason: your day-to-day work depends on exactly the abilities these assessments measure. You diagnose faults in complex pipelines under time pressure, interpret throughput and capacity figures, read dense technical standards and policy documents with precision, and exercise judgement in situations where stakeholders disagree and there is no perfectly clean answer.

This document is organised into four main assessment sections, each mirroring a type of test you are likely to encounter:

1. **Workplace job-specific cognitive assessment** - pattern recognition, logical deduction, error checking, prioritisation, and problem solving using the artefacts you genuinely handle: pipeline DAGs, schema definitions, streaming configurations, and test results.
2. **Workplace job-specific numeric reasoning assessment** - interpretation of throughput tables, storage cost projections, capacity figures, performance metrics, and budgets.
3. **Workplace job-specific verbal reasoning assessment** - careful reading of standards, policies, technical reports, and stakeholder emails, answered strictly from the text.
4. **Workplace job-specific situational judgement assessment** - realistic dilemmas involving your real stakeholders: multidisciplinary teams, analysts, architects, service owners, and suppliers.

Each section explains what the assessment measures, maps it to the specific skills in your role profile, provides substantial practice questions with full worked explanations, and closes with preparation tips and common pitfalls.

How should you use it? Work through the practice questions honestly before reading the explanations. Treat each explanation as a short coaching session: the reasoning matters more than the answer. Use the questions for self-reflection too - many are drawn from genuine senior-level tensions, such as balancing reuse against delivery pressure, or advocating for your team while managing differing stakeholder perspectives. You already exercise these capabilities daily; this document simply helps you demonstrate them under assessment conditions, with confidence.

Take your time, enjoy the challenge, and remember: preparation is not about gaming a test. It is about removing surprise, so your genuine ability shows through.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive ability assessment is a targeted psychometric test designed to measure the exact mental processes needed for your role, rather than abstract intelligence. Instead of generic puzzles, it presents practical workplace scenarios and data formats drawn from senior data engineering: pipeline dependency graphs, schema definitions, streaming configurations, test result matrices, and metadata catalogues. Your task is to reason quickly and accurately about them.

Typical format: an online, timed test of 15 to 30 minutes, with questions that mimic the everyday tasks and artefacts of the job. Scoring is objective, with your results compared against a benchmark or norm group of professionals at a similar level. Modern platforms often adapt question difficulty based on your previous answers, and employers usually receive a breakdown of speed versus accuracy rather than a single headline score. Most platforms give you short, ungraded practice questions first so you can get comfortable with the interface - always take these.

For a senior data engineer, cognitive assessment matters because your role is fundamentally about reasoning under constraint. When a streaming pipeline degrades at 09:00 on a Monday, you must deduce the likely cause from partial evidence. When two data models disagree, you must spot the structural difference. When a release deadline approaches, you must prioritise faults by impact, not by noise. These are all cognitive operations, and this assessment measures how reliably you perform them under time pressure.

### What it measures for your role

The assessment dimensions map directly onto the skills named in your role profile:

- **Problem management**: logical deduction and fault diagnosis questions test your ability to investigate patterns and trends, isolate root causes, and determine appropriate resolutions and preventative measures.
- **Data integration design**: constraint-based reasoning questions test whether you can select the appropriate technologies to deliver resilient, scalable, future-proofed solutions when several options each satisfy some, but not all, requirements.
- **Data modelling**: pattern recognition and comparison questions test your ability to compare and align different data models, and to explain which models to use for which purpose.
- **Programming and build (data engineering)**: error-checking questions test the precision needed to design, code, test, correct and document moderate-to-complex programs and scripts.
- **Testing**: coverage-reasoning questions test how you review requirements and specifications, define test conditions, and identify issues and risks.
- **Metadata management**: consistency-checking questions test your eye for anomalies in metadata repositories.
- **Data analysis and synthesis**: data-profiling questions test how quickly you extract meaningful signal from source system information.

### Practice questions

**Question 1 (easy) - Pattern recognition in pipeline schedules**

A nightly batch pipeline has run with the following durations over eight consecutive nights (in minutes): 42, 44, 43, 58, 45, 44, 60, 46. The pipeline processes a daily extract, except that twice a week it also processes a weekly reconciliation file. Which nights most likely included the reconciliation file?

- A) Nights 1 and 5
- B) Nights 4 and 7
- C) Nights 2 and 6
- D) Nights 3 and 8

**Correct answer: B**

**Explanation:** The durations cluster tightly around 42-46 minutes, with two clear outliers: 58 minutes on night 4 and 60 minutes on night 7. A recurring extra workload, such as a weekly reconciliation file, would show up as a repeated step-change above the baseline rather than random noise. Nights 4 and 7 are the only two observations materially above the cluster, so they are the most likely candidates. This is exactly the kind of profiling instinct you use when investigating patterns and trends during problem management: separate the stable baseline from the recurring anomaly before hypothesising causes.

**Question 2 (easy) - Logical deduction on DAG dependencies**

In an orchestration DAG, task C depends on tasks A and B. Task D depends on task C. Task E depends on task B only. One morning, task B fails. Assuming the orchestrator only skips tasks whose upstream dependencies did not all succeed, which tasks will be skipped?

- A) C and D only
- B) C, D and E
- C) E only
- D) A, C, D and E

**Correct answer: B**

**Explanation:** Work through the dependency chain systematically. C requires both A and B; since B failed, C is skipped. D requires C; since C did not run, D is skipped. E requires B directly; since B failed, E is skipped. A has no dependency on B, so it runs normally. The tasks skipped are therefore C, D and E. Candidates commonly pick option A by forgetting the direct edge from B to E, or option D by wrongly assuming a failure propagates backwards to A. In real pipeline triage, tracing the blast radius of a single failure accurately is the first step in determining the appropriate resolution and in communicating impact to stakeholders.

**Question 3 (moderate) - Error checking across schema definitions**

You are reviewing a target table specification against the source system contract before a build. The source contract states:

- `case_id`: string, 12 characters, mandatory
- `opened_date`: date, ISO 8601, mandatory
- `priority`: integer, values 1-4, optional
- `assigned_team`: string, max 40 characters, optional

The target DDL your team drafted defines:

- `case_id`: VARCHAR(12) NOT NULL
- `opened_date`: DATE NOT NULL
- `priority`: SMALLINT NOT NULL
- `assigned_team`: VARCHAR(40) NULL

How many discrepancies exist between the contract and the draft DDL?

- A) None
- B) One
- C) Two
- D) Three

**Correct answer: B**

**Explanation:** Compare field by field. `case_id` matches: 12-character string, mandatory maps to NOT NULL. `opened_date` matches: date type, mandatory. `priority` is declared optional in the contract but NOT NULL in the DDL - that is a genuine discrepancy which would cause load failures whenever the source omits the value. `assigned_team` matches: 40-character string, optional maps to NULL. So there is exactly one discrepancy. Note that the DDL does not enforce the 1-4 value range on `priority`, but the contract describes permitted values rather than requiring a database constraint, so under strict error-checking discipline you flag only definite contradictions. This mirrors the precision required when you design, build and test data products from agreed specifications: the costliest defects are usually nullability and type mismatches that pass code review but fail in production.

**Question 4 (moderate) - Constraint-based technology selection**

Your department needs a data integration approach with these mandatory requirements: (1) handles late-arriving events without data loss, (2) scales horizontally to double current volume within a year, (3) supports replay of the last seven days of events, and (4) is supported by your existing platform team's skills. Four candidate approaches are summarised:

- Approach W: meets 1, 2 and 3; requires skills the team does not have.
- Approach X: meets 1, 2 and 4; no replay capability.
- Approach Y: meets 1, 3 and 4; scales vertically only.
- Approach Z: meets 2, 3 and 4; drops late-arriving events older than one hour.

If all four requirements are mandatory, what is the logically correct conclusion?

- A) Approach W is best because it meets the most technical requirements
- B) Approach Z is best because skills and scale matter most
- C) No approach currently satisfies the requirements, so the requirements or the options must be revisited
- D) Approach X is acceptable because replay is rarely used

**Correct answer: C**

**Explanation:** Each approach fails exactly one mandatory requirement, and the question states all four requirements are mandatory. Logically, none qualifies. Options A, B and D each smuggle in an unstated value judgement - that some mandatory requirement can be quietly waived. In a timed cognitive test, the discipline is to reason strictly from the stated constraints, not from what you would pragmatically do. Interestingly, this also reflects sound senior practice in data integration design: when no technology satisfies every stated constraint, the correct professional move is to surface the conflict explicitly - perhaps requirement 4 can be relaxed with training investment - rather than silently downgrading a requirement. Selecting resilient, scalable, future-proofed solutions starts with honest constraint analysis.

**Question 5 (moderate) - Fault diagnosis in a streaming system**

A streaming pipeline you lead ingests events from an operational case-management system into an analytics platform. At 10:15 you observe: consumer lag rising steadily since 09:30; producer publish rate unchanged from its normal profile; consumer CPU at 35% (normal); a schema registry change deployed at 09:25 adding a new optional field; error logs showing repeated deserialisation retries on one partition. What is the most probable root cause?

- A) A surge in event volume from the source system
- B) Consumer hardware exhaustion
- C) A message on one partition that the consumer cannot deserialise, blocking progress on that partition
- D) Network failure between producer and broker

**Correct answer: C**

**Explanation:** Evaluate each hypothesis against the evidence. A surge is contradicted by the unchanged producer rate. Hardware exhaustion is contradicted by 35% CPU. A network failure between producer and broker would reduce incoming messages, not create rising consumer lag with steady production. The remaining evidence - lag rising shortly after a schema change, and repeated deserialisation retries concentrated on one partition - points to a "poison pill" message: an event serialised under an incompatible expectation that the consumer cannot process, so it retries indefinitely and lag accumulates behind it. The timing correlation (deployment 09:25, lag from 09:30) strengthens the inference. This is classic problem management reasoning: correlate the onset of symptoms with recent changes, eliminate hypotheses contradicted by observations, and converge on the cause that explains all the evidence. The preventative measure - compatibility checks in the schema registry and a dead-letter queue - is the kind of follow-up a senior engineer would then determine.

**Question 6 (moderate) - Prioritisation under concurrent incidents**

At 08:50 you have four open issues and one hour before a cross-government publication deadline that depends on your pipelines:

1. The pipeline feeding today's statutory publication failed at 08:30; no output yet produced.
2. A development environment database is refusing new connections; two developers are blocked.
3. A data quality alert shows 0.2% of records in a non-publication dataset have malformed postcodes.
4. An analyst reports that yesterday's BI dashboard load appears to have duplicated one region's figures.

Which order of attention is most defensible?

- A) 1, 4, 2, 3
- B) 2, 1, 4, 3
- C) 1, 2, 3, 4
- D) 4, 1, 3, 2

**Correct answer: A**

**Explanation:** Rank by impact and urgency together. Issue 1 combines the highest impact (a statutory publication) with the hardest deadline (one hour), so it is unambiguously first. Issue 4 is next: duplicated published figures are a live data-integrity problem potentially misleading decision-makers right now, and correcting the record is time-sensitive even without a fixed deadline. Issue 2 blocks two developers - real cost, but recoverable and internal. Issue 3 is a low-severity quality signal (0.2%, non-publication) suitable for routine investigation. Option B over-weights developer convenience against public-facing integrity; option C sorts by ticket number, not impact; option D delays the statutory deadline behind a retrospective fix. Assessments at senior level frequently test whether you distinguish loud problems from important ones - exactly the judgement you apply when initiating and monitoring actions to resolve problems.

**Question 7 (moderate) - Matching data models to purpose**

You maintain three data models over the same case-management subject area:

- Model 1: highly normalised (third normal form), one table per entity, minimal redundancy.
- Model 2: a star schema with a central fact table of case events and dimensions for team, location, and time.
- Model 3: a denormalised wide table refreshed hourly, one row per case, optimised for a single dashboard.

Three requests arrive: (i) the BI team wants flexible slice-and-dice analysis of case volumes by team, month and region; (ii) the operational system team wants a reference structure that avoids update anomalies when a team is renamed; (iii) a service owner wants a fast-loading executive dashboard with fixed content. Which pairing is most appropriate?

- A) i-1, ii-2, iii-3
- B) i-2, ii-1, iii-3
- C) i-3, ii-2, iii-1
- D) i-2, ii-3, iii-1

**Correct answer: B**

**Explanation:** Slice-and-dice analysis across conformed dimensions is precisely what a star schema is designed for, so request i maps to Model 2. Avoiding update anomalies - a team rename should be a single-row change - is the defining benefit of normalisation, so request ii maps to Model 1. A fixed-content dashboard needing raw speed suits the pre-joined denormalised table, so request iii maps to Model 3. This question rehearses a named senior skill: explaining which models to use for which purpose, and recognising industry-standard patterns (normal forms, dimensional modelling, denormalised marts) and when to apply each. In an assessment, eliminate pairings quickly: any option pairing the operational anomaly concern with a denormalised structure can be discarded immediately, which removes options C and D and leaves a single check between A and B.

**Question 8 (moderate) - Consistency checking in a metadata repository**

Your metadata repository lists four datasets. An extract shows:

| Dataset | Owner | Update frequency | Retention | Last updated |
|---|---|---|---|---|
| Case events | Casework team | Daily | 7 years | Yesterday |
| Staff roster | HR data team | Weekly | 2 years | 12 days ago |
| Postcode lookup | Geography team | Quarterly | Indefinite | 40 days ago |
| Payments feed | Finance team | Daily | 7 years | 3 days ago |

Assuming the metadata is meant to be internally consistent, which entries warrant investigation?

- A) Staff roster and Payments feed
- B) Payments feed only
- C) Postcode lookup and Case events
- D) Staff roster only

**Correct answer: A**

**Explanation:** Test each row's "last updated" against its declared frequency. Case events: daily, updated yesterday - consistent. Staff roster: weekly, but last updated 12 days ago - at least one expected update has been missed, so investigate. Postcode lookup: quarterly, updated 40 days ago - well within a quarter, consistent. Payments feed: daily, but last updated 3 days ago - two expected updates missed, so investigate. Both the roster and the payments feed are anomalous, giving option A. Note the reasoning style: you did not need domain knowledge, only internal consistency between two metadata fields. As the person who designs metadata repositories and advises less experienced team members about metadata management, spotting where declared metadata and observed behaviour diverge is a core habit - stale metadata quietly destroys trust in a catalogue.

**Question 9 (challenging) - Test condition coverage**

A specification for a data transformation states: "Records with a valid case ID and an opened date in the current financial year are loaded to the main table. Records with a valid case ID but an opened date outside the current financial year are loaded to the archive table. Records with an invalid case ID are rejected to the error queue, regardless of date." Your junior colleague proposes three test conditions: (1) valid ID, current-year date, expect main table; (2) valid ID, prior-year date, expect archive; (3) invalid ID, current-year date, expect error queue. Which materially distinct condition is missing?

- A) Valid ID, current-year date, expect archive table
- B) Invalid ID, date outside the current financial year, expect error queue
- C) Valid ID, missing date, expected behaviour unspecified
- D) Invalid ID, current-year date, expect main table

**Correct answer: C**

**Explanation:** The specification partitions records along two dimensions: ID validity and date category. The three proposed tests cover valid/current, valid/non-current, and invalid/current. Option B (invalid/non-current) is technically untested, but the specification says invalid IDs are rejected "regardless of date", so it belongs to the same equivalence class as test 3 - useful as a cheap extra check, but not materially distinct. The genuinely missing case is a record with a valid ID and a missing or unparseable date: the specification is silent, meaning the behaviour is undefined. Identifying that gap is more valuable than adding another test, because it is a specification defect, not just a coverage hole. Options A and D describe expectations that contradict the specification, so they are not valid test conditions at all. This mirrors the senior testing skill: reviewing requirements and specifications, defining test conditions, and - crucially - identifying issues and risks in the specification itself before code is written.

**Question 10 (challenging) - Reuse versus rebuild deduction**

Your organisation has an existing data flow, Flow P, which extracts case records nightly, standardises addresses, and publishes to the analytics platform. A new requirement asks for case records with standardised addresses to be available to a fraud-detection service within 15 minutes of creation. Colleagues make four claims. Which claim is logically sound?

- A) "Flow P already produces exactly the required data, so reusing it fully satisfies the requirement."
- B) "The requirement is about latency, so none of Flow P can be reused."
- C) "Flow P's transformation logic could be reused, but its nightly batch trigger cannot meet the 15-minute latency, so the delivery mechanism must change."
- D) "Since the fraud service is a new consumer, we must build an entirely new pipeline to keep systems decoupled."

**Correct answer: C**

**Explanation:** Decompose the flow into what it produces (standardised case records - matching the requirement) and how it delivers (nightly batch - failing the 15-minute latency). Claim A ignores the delivery dimension: correct data delivered 24 hours late does not satisfy the requirement. Claim B commits the opposite error, treating one failed dimension as invalidating every component; transformation logic is latency-agnostic and reusable. Claim D asserts a conclusion ("entirely new pipeline") from a premise ("new consumer") that does not entail it - decoupling can be achieved while sharing transformation code. Claim C correctly separates the reusable component from the component that must change. This is the analytical core of a duty named in your role profile: recognising opportunities to reuse existing data flows. Genuine reuse analysis is component-level, not all-or-nothing.

**Question 11 (challenging) - Rule-based deduction with access policies**

Your platform enforces three rules. Rule 1: datasets classified OFFICIAL-SENSITIVE may only be accessed by named individuals with a current security check. Rule 2: any dataset joined with an OFFICIAL-SENSITIVE dataset inherits the OFFICIAL-SENSITIVE classification. Rule 3: dashboards may only be published organisation-wide if every underlying dataset is classified OFFICIAL (not SENSITIVE). An analyst builds a dashboard from Dataset J (OFFICIAL) joined with Dataset K (OFFICIAL-SENSITIVE). Which statement must be true?

- A) The dashboard may be published organisation-wide because Dataset J is OFFICIAL
- B) The joined dataset is OFFICIAL-SENSITIVE, so the dashboard may not be published organisation-wide
- C) The analyst may not access Dataset J
- D) The dashboard may be published if the analyst has a current security check

**Correct answer: B**

**Explanation:** Apply the rules mechanically. By Rule 2, the join of J and K inherits OFFICIAL-SENSITIVE from K. By Rule 3, organisation-wide publication requires every underlying dataset to be OFFICIAL, which the joined dataset is not; therefore publication is prohibited. Option A fails because Rule 3 quantifies over every dataset, not any dataset. Option C is unsupported: nothing restricts access to J itself. Option D confuses two separate rules - the analyst's personal clearance (Rule 1) governs access, not publication (Rule 3), and no rule allows a clearance to override the publication restriction. Assessments use this structure to measure whether you apply rules exactly as written rather than as you assume they were intended. The same discipline underpins your database management leadership: access and classification rules are enforced by their letter, and a senior engineer must reason about their composition precisely.

**Question 12 (challenging) - Code optimisation reasoning**

A transformation script processes 10 million records. Profiling shows: step 1 (parse input) takes 4 minutes; step 2 (look up each record's team against a reference table by calling the database once per record) takes 46 minutes; step 3 (write output) takes 5 minutes. Four optimisation proposals are made. Based on the profile, which will most reduce total runtime?

- A) Rewrite step 1 with a faster parsing library, expected to halve its time
- B) Replace step 2's per-record database calls with a single reference table load into an in-memory map at the start
- C) Compress the output in step 3 to reduce write volume by 30%
- D) Split step 1 across two threads

**Correct answer: B**

**Explanation:** Total runtime is 55 minutes, of which step 2 accounts for 46 minutes - roughly 84%. Amdahl's reasoning applies: the achievable saving from optimising any step is bounded by that step's share of total time. Option A saves at most 2 minutes; options C and D save fractions of 5 and 4 minutes respectively. Option B attacks the dominant cost, and it attacks it structurally: 10 million individual database round-trips replaced by one bulk load and in-memory lookups typically reduces that step from minutes to seconds, because per-call network latency, not computation, dominates. Recognising the "N+1 query" anti-pattern and reasoning proportionally from a profile is exactly the duty your role names: optimise the code to ensure processes perform optimally. In test conditions, do the arithmetic first - the biggest number in the profile almost always identifies the right answer - then sanity-check that the proposed fix plausibly removes most of that cost.

### Preparation tips

- **Rehearse with your own artefacts.** Sketch a DAG from one of your real pipelines and quiz yourself on failure propagation; compare two schemas from a recent build and time yourself finding the differences. Familiarity with the reasoning pattern transfers directly.
- **Practise proportional reasoning from profiles.** Many cognitive items at senior level reward finding the dominant term - the biggest cost, the largest anomaly - before doing any detailed work.
- **Answer strictly from the stated rules.** Where a question defines rules or constraints, suppress your instinct to apply pragmatic workplace judgement; apply the rules as written.
- **Manage the clock deliberately.** With 15 to 30 minutes total, allow roughly 60-90 seconds per question, bank the easy ones fast, and flag rather than wrestle any question that stalls you.
- **Use the ungraded practice items.** They exist to remove interface surprise. Treat them seriously, then start the timed section calm.

### Common pitfalls

- **Bringing outside assumptions into rule-based questions.** As a senior engineer you know how systems "should" behave; the test asks how the described system does behave. Reason only from the given material.
- **Sinking time into one hard question.** The classic time-sink trap: a single multi-stage problem consumes five minutes while three easy questions go unanswered. Skip and return.
- **Speed without error checking.** Reports typically separate speed from accuracy. A rushed wrong answer costs more than a slightly slower right one; for error-checking items in particular, verify field by field.
- **Pattern-matching superficially.** Distractor options are engineered to look right at a glance (option A in Question 2, option B in Question 9). Trace the logic fully before committing.
- **Ignoring the question's exact ask.** "Which must be true" differs from "which is most likely"; "materially distinct" differs from "any missing case". Senior-level items turn on these qualifiers.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment evaluates your ability to analyse, interpret, and make sound decisions using numerical data. It deliberately mirrors the data-handling demands of your actual role: not abstract formulae, but the business mathematics of running data platforms - throughput figures, storage growth projections, cost tables, capacity calculations, availability targets, and performance metrics.

Typical format: a strictly timed online test, often allowing around one to two minutes per question, with an onscreen calculator provided or permitted. The emphasis is on interpretation over mental arithmetic: the challenge is extracting the right figures from tables, charts and multi-layered datasets quickly and accurately, then applying percentages, ratios, rates and cost-benefit reasoning. Question inputs look like the artefacts you already handle: platform billing summaries, ingestion dashboards, capacity plans, and quality reports. As with the cognitive test, results are usually benchmarked against a norm group, and both speed and accuracy are reported.

For a senior data engineer this assessment matters because quantitative judgement is embedded in your leadership duties. Leading the build of data streaming systems means sizing consumers against event rates. Optimising code means reading a profile and reasoning proportionally about where the time goes. Leading database management means projecting storage growth against budget. Selecting resilient, scalable, future-proofed technologies means comparing cost models honestly, including break-even points. Presenting clear insights to colleagues - a named skill in your profile - depends on getting the numbers right before you communicate them.

### What it measures for your role

The dimensions of this assessment map to the specific skills in your role profile:

- **Data analysis and synthesis**: extracting figures from profiling outputs and source system statistics, computing rates and proportions, and turning them into clear insights that support the end use of the data.
- **Data integration design**: cost and capacity comparisons between candidate technologies, including per-unit pricing, break-even analysis, and scaling projections that determine whether a solution is genuinely future-proofed.
- **Programming and build (data engineering)**: performance arithmetic - throughput, latency, and the proportional gains available from optimising the dominant cost, so processes perform optimally.
- **Problem management**: quantifying incident impact - backlog sizes, catch-up times, and error budgets - so investigations and resolutions are grounded in numbers rather than impressions.
- **Data development process**: effort and budget calculations for building complex or large-scale data products, and for resourcing the teams that complete data integration services.
- **Testing**: interpreting defect and rejection rates across sources, and weighting them correctly when reporting test activities and results.

### Practice questions

An onscreen calculator is assumed throughout. Work each answer yourself before reading the explanation.

**Question 1 (easy) - Daily event volume**

Your streaming platform ingests case events at an average rate of 1,250 events per second, sustained around the clock. Approximately how many events does it ingest per day?

- A) 10.8 million
- B) 108 million
- C) 1.08 million
- D) 1.8 million

**Correct answer: B**

**Explanation:** There are 86,400 seconds in a day (60 × 60 × 24). Multiply: 1,250 × 86,400 = 108,000,000, that is 108 million events per day. A quick estimation route: 1,250 × 86,400 is 1,250 × 86.4 thousand; 1,250 × 86.4 = 108,000, so 108,000 thousand = 108 million. Options A and C are magnitude errors - exactly the kind produced by mislaying a factor of ten under time pressure. When you lead the build of data streaming systems, this conversion between per-second rates and daily volumes is the first arithmetic of any capacity conversation, so make it automatic.

**Question 2 (easy) - Percentage improvement from optimisation**

You optimise a transformation job, reducing its runtime from 80 minutes to 62 minutes. What percentage reduction in runtime have you achieved?

- A) 18%
- B) 22.5%
- C) 29%
- D) 77.5%

**Correct answer: B**

**Explanation:** The reduction is 80 − 62 = 18 minutes. As a percentage of the original runtime: 18 ÷ 80 = 0.225 = 22.5%. Option A mistakes the absolute saving (18 minutes) for a percentage. Option D is the remaining proportion of the original runtime (62 ÷ 80 = 77.5%), a classic misread of what was asked. Option C divides by the new runtime instead of the original (18 ÷ 62 ≈ 29%). Percentage changes are always computed against the original value unless stated otherwise. When you report optimisation results to stakeholders, quoting the correct baseline is part of communicating between the technical and non-technical with credibility.

**Question 3 (moderate) - Compound storage growth**

Your analytics platform currently stores 40 TB. Volume is growing at 5% per month, compounding. Approximately how much storage will you need in six months?

- A) 52 TB
- B) 53.6 TB
- C) 50 TB
- D) 46 TB

**Correct answer: B**

**Explanation:** Compound growth multiplies: 40 × 1.05⁶. Step by step: 1.05² = 1.1025; 1.05³ ≈ 1.1576; 1.05⁶ = (1.05³)² ≈ 1.1576² ≈ 1.3401. Then 40 × 1.3401 ≈ 53.6 TB. Option A (52 TB) is the simple-interest shortcut: 40 × (1 + 6 × 0.05) = 40 × 1.30 = 52 TB, which understates compounding. Option D applies only three months of growth. The difference between 52 and 53.6 TB looks small at six months but widens dramatically over a multi-year horizon - at 5% monthly, storage nearly doubles every 14-15 months. Distinguishing linear from compound growth is essential when you assess whether a solution is genuinely scalable and future-proofed, and when you brief finance colleagues on where the storage budget is heading.

**Question 4 (moderate) - Cost break-even between two platforms**

You are comparing two managed database services for a new data product:

| Cost element | Service A | Service B |
|---|---|---|
| Storage (per TB per month) | £22 | £15 |
| Fixed compute (per month) | £3,400 | £4,800 |

At what stored volume do the two services cost the same per month?

- A) 150 TB
- B) 175 TB
- C) 200 TB
- D) 240 TB

**Correct answer: C**

**Explanation:** Set the monthly costs equal, with V as the volume in TB: 22V + 3,400 = 15V + 4,800. Subtract 15V from both sides: 7V + 3,400 = 4,800. Subtract 3,400: 7V = 1,400, so V = 200 TB. Below 200 TB, Service A's lower fixed compute makes it cheaper (for example at 180 TB: A costs 22 × 180 + 3,400 = £7,360 versus B at 15 × 180 + 4,800 = £7,500). Above 200 TB, Service B's cheaper storage wins. Break-even analysis like this is at the heart of selecting appropriate technologies for resilient, scalable solutions: the right answer depends on your projected volume, and - linking back to Question 3 - a platform growing 5% monthly will cross a 200 TB break-even sooner than a linear projection suggests.

**Question 5 (moderate) - Consumer capacity sizing**

A streaming topic must handle a peak load of 6,000 events per second. Each consumer instance can process at most 800 events per second. The topic has 12 partitions and each partition can be consumed by only one instance at a time. What is the minimum number of consumer instances that can handle peak load, and is it feasible?

- A) 7 instances; feasible
- B) 8 instances; feasible
- C) 8 instances; not feasible because of the partition limit
- D) 12 instances; feasible

**Correct answer: B**

**Explanation:** Divide peak load by per-instance capacity: 6,000 ÷ 800 = 7.5. You cannot run half an instance, so round up to 8. Then check the constraint: parallelism is capped by partition count, and 8 instances ≤ 12 partitions, so the configuration is feasible - option B. Option A forgets to round up: 7 instances give only 5,600 events per second of capacity, 400 short of peak, so lag would grow. Option C misapplies the partition constraint, which only bites when instances would exceed partitions. Option D wastes resources: 12 instances work but are not the minimum asked for. This two-step pattern - compute the raw requirement, then validate against a structural constraint - is exactly how you size the streaming systems you lead, and assessments reward candidates who remember the second step.

**Question 6 (moderate) - Weighted rejection rates across sources**

A nightly integration loads three sources. Last night's quality report shows:

| Source | Records received | Rejection rate |
|---|---|---|
| Case system | 2,000,000 | 0.5% |
| Staffing system | 500,000 | 2.0% |
| Payments system | 1,500,000 | 1.0% |

What was the overall rejection rate across all records received?

- A) 1.17%
- B) 0.875%
- C) 1.0%
- D) 3.5%

**Correct answer: B**

**Explanation:** Compute rejected records per source: case system 2,000,000 × 0.005 = 10,000; staffing 500,000 × 0.02 = 10,000; payments 1,500,000 × 0.01 = 15,000. Total rejections: 10,000 + 10,000 + 15,000 = 35,000. Total received: 4,000,000. Overall rate: 35,000 ÷ 4,000,000 = 0.00875 = 0.875%. Option A is the trap: averaging the three percentages ((0.5 + 2.0 + 1.0) ÷ 3 ≈ 1.17%) ignores that the sources differ enormously in size - the small staffing feed must not count equally with a feed four times larger. Option D simply adds the percentages. Weighted averages appear constantly in your work: when you undertake data profiling and source system analysis, and when you analyse and report test activities and results, the honest aggregate is always volume-weighted.

**Question 7 (moderate) - Compression savings**

A raw event archive holds 96 TB. Moving it to a columnar format achieves a 4:1 compression ratio. Storage costs £18 per TB per month. What monthly saving does the migration deliver?

- A) £432
- B) £1,296
- C) £1,728
- D) £324

**Correct answer: B**

**Explanation:** A 4:1 ratio means the compressed archive occupies 96 ÷ 4 = 24 TB. The saving in volume is 96 − 24 = 72 TB. At £18 per TB per month, the monthly saving is 72 × £18 = £1,296. Option C is the trap of costing the entire original archive (96 × £18 = £1,728) - that would be the saving only if the data vanished entirely. Option A prices the remaining 24 TB rather than the freed 72 TB. Watch the direction of ratios in questions like this: 4:1 compression divides the size by four, leaving a quarter, so the saving is three quarters of the original cost (0.75 × £1,728 = £1,296, confirming the answer by a second route). Cross-checking by an independent route is a habit worth building - it catches most arithmetic slips within seconds.

**Question 8 (moderate) - Migration budget tracking**

You lead a database migration with a budget of £120,000. Committed costs so far: two contractors at £650 per day each for 60 days; interim platform costs of £2,500 per month for 6 months; and £4,800 of training for the team. What percentage of the budget remains?

- A) 18.5%
- B) 22.2%
- C) 81.5%
- D) 15.0%

**Correct answer: A**

**Explanation:** Contractors: 2 × £650 × 60 = £78,000. Platform: £2,500 × 6 = £15,000. Training: £4,800. Total committed: £78,000 + £15,000 + £4,800 = £97,800. Remaining: £120,000 − £97,800 = £22,200. As a percentage of budget: 22,200 ÷ 120,000 = 0.185 = 18.5%. Option C is the proportion spent, not remaining - always re-read which the question asks. Option B is what you get by misreading £22,200 as a percentage directly. Multi-component budget questions reward a methodical layout: list each component, total them, then perform the final comparison. As a senior engineer who builds teams to complete data integration services, you will present figures like these to service owners, so the discipline of computing them cleanly under time pressure is doubly valuable.

**Question 9 (challenging) - Availability targets and error budgets**

Your data service has a monthly availability target of 99.9%, measured over a 30-day month. This month the service has already been down for 28 minutes. How many more minutes of downtime can occur before the target is breached?

- A) 43.2 minutes
- B) 15.2 minutes
- C) 4.3 minutes
- D) 30.8 minutes

**Correct answer: B**

**Explanation:** First compute the total allowance. A 30-day month contains 30 × 24 × 60 = 43,200 minutes. The permitted downtime is the complement of the target: 100% − 99.9% = 0.1%, so 43,200 × 0.001 = 43.2 minutes for the month. Subtract downtime already consumed: 43.2 − 28 = 15.2 minutes remaining - option B. Option A is the whole monthly allowance, ignoring the 28 minutes already used. Option C mistakes 0.01% for 0.1%. Error-budget arithmetic like this shapes real engineering decisions: with only 15.2 minutes left, you might defer a risky deployment or invest in a safer rollout method - a quantitative version of determining preventative measures in problem management. It is also a powerful framing when you advocate for the team externally: "we have 15 minutes of error budget left this month" lands with non-technical stakeholders far better than raw percentages.

**Question 10 (challenging) - Weighted average latency**

Three pipelines feed a fraud-screening service. Pipeline X carries 60% of traffic with an average latency of 250 ms; Pipeline Y carries 30% at 400 ms; Pipeline Z carries 10% at 900 ms. What is the overall average latency experienced across all traffic?

- A) 517 ms
- B) 360 ms
- C) 325 ms
- D) 283 ms

**Correct answer: B**

**Explanation:** Weight each latency by its traffic share: (0.60 × 250) + (0.30 × 400) + (0.10 × 900) = 150 + 120 + 90 = 360 ms. Option A is the unweighted mean of the three latencies ((250 + 400 + 900) ÷ 3 ≈ 517 ms), which over-represents the small, slow Pipeline Z. Notice the insight hiding in the arithmetic: Z carries only a tenth of the traffic yet contributes a quarter of the weighted total (90 of 360 ms) - so if you want to optimise the overall figure, Z offers the largest per-event improvement, but halving X's latency (saving 75 ms of the weighted total) would actually help more users. Being able to decompose an aggregate metric into contributions is precisely how you present clear insights to colleagues to support the end use of the data, and assessments at senior level often hide a second-order insight like this inside a simple weighted average.

**Question 11 (challenging) - Backlog catch-up after an outage**

A consumer service fails for 45 minutes while producers continue publishing at 2,000 events per second. When the consumer restarts, it can process at a maximum of 3,500 events per second, while new events continue to arrive at 2,000 per second. How long will it take to clear the backlog?

- A) 26 minutes
- B) 45 minutes
- C) 60 minutes
- D) 90 minutes

**Correct answer: C**

**Explanation:** First size the backlog: 45 minutes × 60 seconds × 2,000 events per second = 5,400,000 events. On restart, the consumer's spare capacity - the rate at which the backlog actually shrinks - is processing rate minus arrival rate: 3,500 − 2,000 = 1,500 events per second. Time to clear: 5,400,000 ÷ 1,500 = 3,600 seconds = 60 minutes. Option A divides the backlog by the full 3,500 rate, forgetting that new events keep arriving and consuming most of the capacity. Option B assumes recovery time equals outage time, which is only true when spare capacity equals the arrival rate. This net-drain calculation is fundamental to leading streaming systems: it tells you, before you promise anything to stakeholders, that a 45-minute outage costs an hour of degraded freshness - and it quantifies the case for headroom, since a consumer that could do 6,000 events per second would clear the same backlog in 5,400,000 ÷ 4,000 = 1,350 seconds, about 22.5 minutes.

**Question 12 (challenging) - Reuse versus rebuild break-even**

You must deliver a new data flow. Option 1: adapt an existing flow - 15 engineer-days to deliver, then 2 engineer-days per month of ongoing maintenance (the old flow carries technical debt). Option 2: rebuild cleanly - 40 engineer-days to deliver, then 1 engineer-day per month of maintenance. After how many months of operation does the rebuild become the cheaper option in total engineer-days?

- A) 13 months
- B) 25 months
- C) 40 months
- D) The rebuild is never cheaper

**Correct answer: B**

**Explanation:** Write the total cost of each option after m months. Option 1: 15 + 2m. Option 2: 40 + 1m. The rebuild becomes cheaper when 40 + m < 15 + 2m. Subtract m from both sides: 40 < 15 + m, so m > 25. At exactly 25 months both options total 65 engineer-days; from month 26 onwards the rebuild is cheaper. Verify: at m = 26, Option 1 costs 15 + 52 = 67 days, Option 2 costs 40 + 26 = 66 days. Option A comes from setting the difference in build costs (25 days) against the combined maintenance rates rather than the difference in maintenance rates. The structure to remember: extra upfront investment ÷ monthly saving = break-even months, here 25 ÷ 1 = 25. This is the quantitative backbone of a duty named in your role profile - recognising opportunities to reuse existing data flows - and of honest conversations about technical debt: reuse genuinely wins for short-lived products, rebuilds win for long-lived ones, and the break-even point tells you which situation you are in.

**Question 13 (challenging) - Interpreting a performance metrics table**

Your team's quarterly platform report shows four pipelines:

| Pipeline | Runs per quarter | Failure rate | Mean minutes lost per failure |
|---|---|---|---|
| Ingest-A | 900 | 2.0% | 30 |
| Ingest-B | 450 | 4.0% | 25 |
| Transform-C | 1,800 | 0.5% | 120 |
| Publish-D | 90 | 10.0% | 40 |

Which pipeline costs the most total minutes lost per quarter?

- A) Ingest-A
- B) Ingest-B
- C) Transform-C
- D) Publish-D

**Correct answer: C**

**Explanation:** Total minutes lost = runs × failure rate × minutes per failure. Ingest-A: 900 × 0.02 × 30 = 18 failures × 30 = 540 minutes. Ingest-B: 450 × 0.04 × 25 = 18 × 25 = 450 minutes. Transform-C: 1,800 × 0.005 × 120 = 9 × 120 = 1,080 minutes. Publish-D: 90 × 0.10 × 40 = 9 × 40 = 360 minutes. Transform-C dominates at 1,080 minutes despite having by far the lowest failure rate, because it runs most often and each failure is expensive. Option D tempts candidates who anchor on the eye-catching 10% failure rate. The lesson generalises to problem management: to investigate patterns and trends usefully, rank problems by total impact (frequency × severity), never by a single alarming column. It also tells you where preventative measures buy the most - halving Transform-C's recovery time saves more minutes than eliminating Publish-D's failures entirely.

**Question 14 (challenging) - Ratio reasoning on infrastructure scaling**

A database cluster of 6 nodes currently sustains 15,000 queries per second at 60% average CPU utilisation. Assuming linear scaling and that you must keep average utilisation at or below 75% for resilience, what is the maximum queries per second the existing cluster can safely sustain, and how many nodes are needed to safely sustain 30,000 queries per second?

- A) 18,750 qps; 10 nodes
- B) 25,000 qps; 8 nodes
- C) 18,750 qps; 12 nodes
- D) 22,500 qps; 9 nodes

**Correct answer: A**

**Explanation:** First find capacity per unit of utilisation: 15,000 qps consumes 60% CPU, so each percentage point of average utilisation supports 15,000 ÷ 60 = 250 qps. At the 75% ceiling, the cluster safely sustains 250 × 75 = 18,750 qps. For 30,000 qps, compute the utilisation it would cause on the current cluster: 30,000 ÷ 250 = 120%, clearly beyond the ceiling. Nodes needed scale linearly: each node contributes 18,750 ÷ 6 = 3,125 safe qps, so 30,000 ÷ 3,125 = 9.6, rounding up to 10 nodes. Option A gives both figures correctly. Option C doubles the node count naively (6 × 2 = 12), ignoring that the current cluster runs below its safe ceiling and so has headroom already. Option D uses the 60% figure as the ceiling. Two-stage ratio problems like this reward writing down the intermediate quantity - safe qps per node - explicitly; it is the same arithmetic you present to platform architects when leading work on database management and making the case for scaling decisions before peak demand arrives.

### Preparation tips

- **Drill the core toolkit.** Percentages of and against the correct baseline, weighted averages, compound growth, break-even equations, and rate × time conversions cover the vast majority of senior data engineering numeric items. Ten minutes of daily practice for two weeks makes them reflexive.
- **Extract before you calculate.** Most errors in table-based questions happen at extraction, not arithmetic. Read the row and column headers, note the units, and only then reach for the calculator.
- **Estimate first, compute second.** A rough order-of-magnitude estimate (Question 1's "about 100 million") lets you discard implausible options instantly and catches slipped decimal points.
- **Verify by a second route when time allows.** As in Question 7, many quantities can be computed two ways; ten seconds of cross-checking prevents the most expensive errors.
- **Practise with your own dashboards.** Take a real ingestion dashboard or billing summary from your platform and invent questions: what is the weighted average? where is the break-even? This builds fluency with exactly the data formats the test mimics.

### Common pitfalls

- **Misreading scale qualifiers.** Confusing "per TB per month" with "per TB per year", or thousands with millions, silently invalidates an otherwise perfect calculation. Underline units as you read.
- **Averaging percentages without weights.** As Question 6 showed, the unweighted mean of rates from differently sized sources is almost always one of the distractor options.
- **Using the wrong baseline for percentage change.** Reductions are measured against the original value; option sets are built to punish dividing by the new value instead.
- **Over-calculating.** If options are far apart, estimation answers the question faster than exact arithmetic. Save precision for options that are close together.
- **Time-sink questions.** One multi-stage problem can consume the time of four simpler ones. If a question stalls you beyond about two minutes, flag it, move on, and return with fresh eyes.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment evaluates how well you understand, analyse, and draw correct conclusions from written business information. The passages mirror the exact reading demands of senior data engineering in government: data-sharing policies, technical standards, incident reports, supplier documentation, and stakeholder emails. The defining discipline is fact-based logic: you must answer based strictly on the text provided, deliberately setting aside your own professional knowledge, however expert it is.

Typical format: a series of dense passages, each followed by statements you must classify as **True** (the passage logically supports the statement), **False** (the passage logically contradicts it), or **Cannot Say** (the passage provides insufficient information either way), plus some multiple-choice comprehension questions. Timing is tight - usually less than a minute per question - to simulate workplace deadlines. Scores are benchmarked against a norm group.

For a senior data engineer, this assessment matters more than it might first appear. Your role profile puts communication at its head: communicating effectively with technical and non-technical stakeholders, hosting discussions in multidisciplinary teams with potentially difficult dynamics, and managing differing stakeholder perspectives. All of that rests on precise reading - of what a policy actually permits, what an architect actually committed to, what a specification actually requires. Misreading "should" as "must", or a proposal as a decision, causes real integration defects and real stakeholder friction. The Cannot Say category is especially relevant to your day job: recognising that a document does not answer your question - and saying so explicitly rather than assuming - is a mark of senior engineering judgement, and exactly what you do when you review requirements and specifications and identify issues and risks.

### What it measures for your role

- **Communicating between the technical and non-technical**: extracting the precise commitments, caveats and asks from stakeholder correspondence, so you can represent them faithfully when advocating for the team externally.
- **Data integration design and data modelling**: reading standards and design documents exactly - distinguishing mandatory requirements ("must") from recommendations ("should") and options ("may"), the vocabulary in which technical standards are written.
- **Testing**: detecting what a specification leaves unsaid - the gaps that become defects - which is the everyday form of Cannot Say.
- **Metadata management and data development process**: parsing governance documents that define ownership, retention and quality obligations, where a misread clause can mean non-compliance.
- **Data innovation**: reading analyst reports about emerging trends in data tools critically - separating what a report claims, what it predicts, and what it merely does not address.

### Practice questions

Answer strictly from each passage. Do not use your own technical knowledge.

**Passage A - Departmental data sharing policy (extract)**

"Personal data may only be transferred between departmental systems where a Data Sharing Agreement (DSA) is in place and has been countersigned by the Information Asset Owners of both the providing and receiving systems. Anonymised datasets are exempt from the DSA requirement, provided the anonymisation method has been approved by the Data Protection Team. Pseudonymised data is not considered anonymised for the purposes of this policy. Where a transfer is required urgently to prevent serious harm to an individual, the Head of Data may authorise a transfer in advance of a DSA being completed; in such cases a DSA must be completed retrospectively within ten working days. All transfers, however authorised, must be recorded in the departmental data transfer register within 24 hours."

**Question 1 (easy)**

True, False, or Cannot Say: "Pseudonymised data may be transferred between departmental systems without a Data Sharing Agreement, provided the pseudonymisation method has been approved by the Data Protection Team."

**Correct answer: False**

**Explanation:** The exemption in the passage applies to anonymised datasets: "Anonymised datasets are exempt from the DSA requirement, provided the anonymisation method has been approved". The passage then states explicitly: "Pseudonymised data is not considered anonymised for the purposes of this policy." Therefore pseudonymised data cannot use the anonymisation exemption, and the default rule applies: personal data "may only be transferred... where a Data Sharing Agreement (DSA) is in place". The statement directly contradicts the policy, so it is False - not Cannot Say. The distractor works by transplanting the exemption's wording ("method has been approved") onto a category the passage expressly excludes. In your data integration work, this pseudonymised/anonymised distinction is precisely the kind of clause that determines whether a proposed feed is lawful, so reading it exactly matters twice over.

**Question 2 (moderate)**

True, False, or Cannot Say: "A transfer authorised by the Head of Data to prevent serious harm does not need to be recorded in the data transfer register."

**Correct answer: False**

**Explanation:** The final sentence settles it: "All transfers, however authorised, must be recorded in the departmental data transfer register within 24 hours." The phrase "however authorised" explicitly sweeps in the urgent transfers authorised by the Head of Data, so the registration duty applies to them. The statement contradicts the passage and is False. Candidates sometimes answer Cannot Say here because the urgent-transfer sentence itself does not mention the register - the skill being tested is connecting two sentences within the same passage and noticing that a universal quantifier ("All transfers, however authorised") closes the apparent gap. Reading a policy as a whole document rather than sentence by sentence is exactly how you would brief a multidisciplinary team on what the policy requires of a new pipeline.

**Question 3 (moderate)**

True, False, or Cannot Say: "A retrospective DSA completed twelve working days after an urgent transfer would breach the policy."

**Correct answer: True**

**Explanation:** The passage states that in urgent cases "a DSA must be completed retrospectively within ten working days." Twelve working days exceeds ten; "must... within ten working days" is a mandatory deadline, so completion on day twelve fails the requirement, and the statement is True. Note what makes this a safe inference rather than an assumption: the passage supplies both the rule (a deadline) and the arithmetic fact (twelve is greater than ten); no outside knowledge is imported. Contrast a statement like "the Head of Data would face disciplinary action" - the passage says nothing about consequences, so that would be Cannot Say. Distinguishing what a document mandates from what it implies about consequences is a distinction you use whenever you translate governance requirements into pipeline controls.

**Passage B - Metadata standard for the analytics platform (extract)**

"Each dataset published to the analytics platform must have a catalogue entry containing, as a minimum: a plain-English description, a named data owner, an update frequency, and a retention period. Catalogue entries should also include field-level descriptions, and teams are encouraged to provide data lineage diagrams. Datasets lacking a complete minimum entry will not be discoverable in the catalogue search. The platform team reviews a sample of catalogue entries each quarter; entries found to be inaccurate will be flagged to the data owner, who must correct them within one reporting cycle. Field-level descriptions, where provided, must follow the departmental data dictionary style guide."

**Question 4 (easy)**

True, False, or Cannot Say: "A dataset with a plain-English description, a named data owner, an update frequency, and a retention period, but no field-level descriptions, can be discoverable in the catalogue search."

**Correct answer: True**

**Explanation:** The passage defines the minimum entry as exactly four items: "a plain-English description, a named data owner, an update frequency, and a retention period." Field-level descriptions sit in a separate sentence governed by "should also include" - the standard's vocabulary for a recommendation, not a requirement. The only stated barrier to discoverability is "Datasets lacking a complete minimum entry will not be discoverable", and this dataset's minimum entry is complete. So the statement is supported: True. The question turns entirely on the must/should distinction, which is load-bearing vocabulary in every technical standard you apply when designing metadata repositories - and precisely the distinction you teach when you advise less experienced members of the team about metadata management.

**Question 5 (moderate)**

True, False, or Cannot Say: "The platform team reviews every catalogue entry at least once a year."

**Correct answer: Cannot Say**

**Explanation:** The passage says the platform team "reviews a sample of catalogue entries each quarter." A sample, by definition, is a subset; the passage gives no information about sample size, selection method, or coverage over time. Four quarterly samples might cumulatively cover every entry in a year - or might repeatedly draw from the same subset. The passage neither supports nor contradicts the claim of complete annual coverage, so the answer is Cannot Say. This is the classic shape of a Cannot Say item: the statement is plausible, even likely in a well-run organisation, and that plausibility is the trap. Your own professional expectation of how sampling reviews ought to work must be set aside. The workplace parallel: when a specification says "records are validated", a senior engineer asks "which records, and when?" rather than assuming full coverage - the identical habit of mind.

**Question 6 (challenging)**

Which of the following best describes the consequence, according to the passage, of a catalogue entry being found inaccurate in a quarterly review?

- A) The dataset is removed from the catalogue search until corrected
- B) The entry is flagged to the data owner, who must correct it within one reporting cycle
- C) The data owner is required to add field-level descriptions
- D) The platform team corrects the entry and notifies the owner

**Correct answer: B**

**Explanation:** The passage states: "entries found to be inaccurate will be flagged to the data owner, who must correct them within one reporting cycle" - a direct match with option B. Option A borrows the discoverability sanction from a different rule, which applies to incomplete minimum entries, not inaccurate ones; the passage keeps the two consequences separate. Option C imports the recommended-but-optional field descriptions into the correction duty without textual basis. Option D reverses the responsibilities: the platform team flags, the owner corrects. Multiple-choice comprehension items are frequently built this way - each wrong option recombines genuine fragments of the passage into a false statement - so verify the whole option against the text, not just its familiar-sounding parts. The same care applies when you summarise a standard for your team: precision about who must do what, and when, prevents governance actions from falling between roles.

**Passage C - Email from a service owner (extract)**

"Thanks for the update on last week's streaming incident. I understand the backlog cleared by 14:00 and that no events were lost. However, the fraud team tell me they made decisions on Tuesday morning using data that was up to three hours stale, and they were not aware of the delay at the time. Before our board meeting on the 28th, I need two things from your team: a short note explaining what monitoring changes would let data consumers see freshness in real time, and an estimate of the cost of the extra capacity you mentioned. I should say that no decision has been made on funding; the capacity proposal will be considered alongside other bids in the autumn planning round. If the freshness monitoring can be delivered within your existing resources, please treat it as the priority of the two."

**Question 7 (easy)**

True, False, or Cannot Say: "The service owner states that events were lost during the incident."

**Correct answer: False**

**Explanation:** The email says the opposite: "I understand the backlog cleared by 14:00 and that no events were lost." The statement directly contradicts this, so it is False. Notice the precise attribution, though: the service owner reports their understanding ("I understand... that no events were lost"), which is a statement about what they were told. The question asks what the service owner states, and they state that no events were lost - so False is safe. Had the question asked "events were definitely not lost during the incident", the careful reader might weigh whether a stakeholder's second-hand understanding establishes the fact; assessments occasionally probe exactly that gap between what a writer asserts and what is independently true. Reading attribution accurately is essential when you manage differing stakeholder perspectives - much workplace conflict begins with "but you said" misquotations.

**Question 8 (moderate)**

True, False, or Cannot Say: "Funding for the extra capacity has been refused."

**Correct answer: False**

**Explanation:** The email says: "no decision has been made on funding; the capacity proposal will be considered alongside other bids in the autumn planning round." A refusal is a decision; the passage states explicitly that no decision has been made, and moreover that the proposal remains under live consideration. The statement therefore contradicts the passage and is False. This one catches candidates who reason "no decision means we cannot say whether it was refused" - but the passage does not leave the matter open; it affirmatively rules out any decision having occurred, which logically excludes refusal. Cannot Say is reserved for genuine silence, not for explicit statements of indeterminacy. The distinction has a direct workplace analogue: reporting to your team that "funding was not approved" after this email would be inaccurate and demoralising, when the truthful summary is "the decision comes in the autumn round" - faithful reading is part of being an advocate for the team externally.

**Question 9 (challenging)**

According to the email, which of the following is the service owner's priority request?

- A) The extra capacity, because the incident showed the platform is under-resourced
- B) The freshness monitoring note, unconditionally
- C) The freshness monitoring, if it can be delivered within existing resources
- D) A root-cause analysis before the board meeting on the 28th

**Correct answer: C**

**Explanation:** The final sentence carries a condition: "If the freshness monitoring can be delivered within your existing resources, please treat it as the priority of the two." The prioritisation is expressly conditional on deliverability within existing resources, which option C preserves and option B erases. Option A reflects what a data engineer might infer should be the priority, but the passage never says it, and the funding caveat cuts against it. Option D invents a deliverable: the email asks for a monitoring note and a cost estimate before the 28th, not a root-cause analysis. Senior verbal reasoning items reward carrying conditions through to the answer rather than simplifying them away - just as, in real stakeholder management, relaying a conditional request as an unconditional one commits your team to work its sponsor never actually prioritised.

**Passage D - Analyst briefing on emerging data tools (extract)**

"Adoption of declarative pipeline frameworks grew markedly across surveyed public sector organisations this year, with 40% reporting production use, up from 25% last year. Respondents cited reduced maintenance effort as the primary benefit, although several noted that initial migration costs were higher than anticipated. The briefing predicts that within three years such frameworks will be the default choice for new data integration work in the sector. Streaming-first architectures, by contrast, showed flat adoption; the authors attribute this to skills shortages rather than to any weakness in the underlying technology. The briefing does not assess vendor lock-in risks, which the authors state are covered in a separate report."

**Question 10 (moderate)**

True, False, or Cannot Say: "More than a third of surveyed public sector organisations reported production use of declarative pipeline frameworks this year."

**Correct answer: True**

**Explanation:** The passage states that "40% reporting production use" of declarative pipeline frameworks this year. Since 40% is more than a third (33.3%), the statement is supported: True. The inference required is purely arithmetic comparison of stated figures, which is safe territory - no assumption about unsurveyed organisations or future behaviour is needed. Contrast a statement such as "most public sector organisations will adopt these frameworks within three years": the passage offers a prediction ("the briefing predicts... will be the default choice"), and a prediction reported in a document is evidence of what the document forecasts, not of what will happen - such a statement would need careful handling depending on its exact wording. When you assess the impact on your organisation of emerging trends in data tools, keeping reported fact, cited opinion, and forecast in separate mental boxes is precisely the skill this question rehearses.

**Question 11 (challenging)**

True, False, or Cannot Say: "The authors believe streaming-first architectures have technical weaknesses that explain their flat adoption."

**Correct answer: False**

**Explanation:** The passage attributes flat adoption "to skills shortages rather than to any weakness in the underlying technology." The construction "rather than" explicitly rejects technical weakness as the explanation, so a claim that the authors believe technical weaknesses explain flat adoption contradicts the text: False. A hasty reader pattern-matches "streaming-first... flat adoption... weakness" and answers True; a cautious but imprecise reader answers Cannot Say on the grounds that authors' private beliefs are unknowable. But the question asks what the authors' stated attribution is, and the passage records it directly. This mirrors a real senior duty: when you summarise an industry briefing for your team or your architecture board, faithfully preserving an author's "X rather than Y" reasoning - not flattening it into "problems with streaming" - is what makes your advice on emerging data trends trustworthy.

**Question 12 (moderate)**

True, False, or Cannot Say: "Vendor lock-in risks associated with declarative pipeline frameworks are negligible."

**Correct answer: Cannot Say**

**Explanation:** The passage says: "The briefing does not assess vendor lock-in risks, which the authors state are covered in a separate report." The document is explicitly silent on the substance of those risks - it tells you where the analysis lives, not what it concludes. Nothing in the passage supports the risks being negligible, and nothing contradicts it either, so the answer is Cannot Say. This is the purest form of the category: the passage itself declares its own gap. Candidates occasionally answer False, reasoning that "if there's a whole separate report, the risks must be significant" - but that is an inference about the world, not the text; report length implies nothing stated here about severity. The workplace parallel is exact: a specification that says "error handling is described in Appendix C" tells you nothing about whether the error handling is adequate, and flagging that unread dependency is part of identifying issues and risks in your testing skill.

**Passage E - Test strategy for a data migration (extract)**

"Reconciliation testing must compare record counts and financial totals between source and target for every migrated table. Field-level comparison is mandatory for tables classified as critical, and should be performed on a 10% sample for all other tables. Any variance in financial totals, of any size, must be investigated before go-live. Count variances below 0.01% in non-critical tables may be accepted by the migration board, provided the cause is documented. The migration board may not accept any variance in critical tables. Performance testing of the target platform is out of scope for this strategy and is addressed by the platform team's separate test plan."

**Question 13 (moderate)**

True, False, or Cannot Say: "A count variance of 0.005% in a non-critical table can go live without investigation, because it is below the 0.01% threshold."

**Correct answer: Cannot Say**

**Explanation:** Read the acceptance clause exactly: count variances below 0.01% in non-critical tables "may be accepted by the migration board, provided the cause is documented." Two conditions attach: board acceptance and documentation of the cause. Documenting a cause plainly requires some investigation, and acceptance is discretionary ("may"), not automatic. So the statement's claim of "without investigation" is not supported. Is it outright contradicted? The strategy requires investigation explicitly only for financial-total variances ("Any variance in financial totals... must be investigated"); for count variances it requires a documented cause, which implies inquiry but the passage never uses the word investigation for counts. The safest classification is Cannot Say: the passage neither licenses skipping investigation nor states in terms that investigation is required for counts. Items like this one reward candidates who track exactly which obligations attach to which variance type - the same clause-level precision you apply when you define test conditions from a specification.

**Question 14 (moderate)**

Which statement accurately reflects the strategy's treatment of critical tables?

- A) Field-level comparison on a 10% sample, and small variances acceptable if documented
- B) Field-level comparison mandatory, and no variance may be accepted by the migration board
- C) Field-level comparison mandatory, and variances below 0.01% acceptable with documentation
- D) Count and totals reconciliation only, with performance testing included

**Correct answer: B**

**Explanation:** Two sentences govern critical tables: "Field-level comparison is mandatory for tables classified as critical" and "The migration board may not accept any variance in critical tables." Option B reproduces both accurately. Option A assigns critical tables the sampling regime and the acceptance route that the passage reserves for "all other tables". Option C correctly keeps mandatory field-level comparison but wrongly imports the 0.01% acceptance clause, which the passage limits to non-critical tables. Option D contradicts the explicit scope exclusion: "Performance testing... is out of scope for this strategy." As in Question 6, the wrong options are stitched from genuine passage fragments attached to the wrong subject - so the verification habit is to check each clause of the chosen option against the sentence that actually governs it.

### Preparation tips

- **Practise the three-way discipline daily.** Take any policy or standard you work with and write three statements about it: one it supports, one it contradicts, one it does not address. Generating Cannot Say items yourself is the fastest way to stop confusing "plausible" with "stated".
- **Learn the signal words.** Must, may, should, all, some, unless, provided that, rather than: these small words decide answers. Slow down when you meet one; they are where senior-level questions hide their logic.
- **Suppress expertise deliberately.** You know how metadata catalogues and DSAs really work; the test rewards answering from this text alone. Before answering, ask: "where in the passage is that said?" If you cannot point to it, it is Cannot Say.
- **Scan, then verify.** Under one-minute-per-question timing, read the statement first, scan the passage for the governing sentence, then read that sentence and its neighbours carefully. Reading the whole passage deeply before seeing any question usually wastes time.
- **Track attribution.** Note who says what: the author states, a respondent cites, a briefing predicts, a stakeholder understands. Questions at senior level often turn on the difference.

### Common pitfalls

- **Importing outside knowledge.** The most common error for experienced professionals: your (correct) real-world knowledge overrides the passage. The test measures reading, not domain expertise - answer only from the text.
- **Confusing likely with stated.** A predicted or probable outcome in the text is not a fact; treating "the briefing predicts" as "it is true that" turns Cannot Say or nuanced items into wrong answers.
- **Treating explicit indeterminacy as Cannot Say.** When a passage states "no decision has been made", claims that a decision went one way are False, not Cannot Say. Reserve Cannot Say for genuine silence.
- **Answering from one sentence.** Universal clauses ("All transfers, however authorised...") elsewhere in the passage frequently close gaps that a single sentence appears to leave open. Check for a governing general rule before answering.
- **Poor time allocation.** Dense passages tempt complete, careful reading of every word before any question. Skim for structure, answer from targeted verification, and keep moving - unanswered easy questions cost more than an occasional hard one.

## Workplace job-specific situational judgement assessment

### About this assessment

A workplace job-specific situational judgement assessment evaluates your decision-making, interpersonal skills, and professional conduct. Unlike logic or numeric tests, it presents realistic workplace dilemmas - short scenarios involving conflict, competing priorities, ethical tension, or operational pressure - and asks how you would respond. There is usually no single objectively right answer; several responses may seem reasonable, but one aligns best with the values of the organisation and the demands of the role. For UK government digital and data work, those values are well documented: meeting user needs, transparency, collaboration across disciplines, accessibility and inclusion, and responsible stewardship of public money and public data.

Typical formats: you may be asked to pick the **most effective** and **least effective** responses from a set, to **rank** all options from best to worst, or to **rate** each option's effectiveness independently. Timing is usually generous or untimed - the test measures natural judgement, not speed.

For a senior data engineer, this is arguably the assessment closest to your daily reality. Your role profile is explicit that you support and host discussions within a multidisciplinary team "with potentially difficult dynamics", that you manage differing stakeholder perspectives, that you act as an advocate for the team externally, and that you build teams to complete data integration services. None of that is solved by arithmetic. The scenarios below are drawn directly from those duties: governance shortcuts under deadline pressure, disagreements between architects and delivery managers, junior engineers needing development rather than rescue, and incidents that test your commitment to transparency.

### What it measures for your role

- **Communicating between the technical and non-technical**: whether you translate rather than lecture, de-escalate rather than win, and keep non-specialist stakeholders genuinely informed.
- **Managing differing stakeholder perspectives and difficult team dynamics**: whether you surface disagreement productively, protect inclusion in discussions, and find resolutions that respect legitimate concerns on all sides.
- **Problem management**: whether you balance rapid restoration against root-cause discipline, escalate appropriately, consult specialists where required, and pursue preventative measures.
- **Data development process and testing**: whether you hold quality and assurance standards under delivery pressure, and how you handle requests to cut corners.
- **Metadata management and mentoring**: whether you develop less experienced colleagues rather than simply correcting them.
- **Data innovation and integration design**: whether you weigh emerging technologies with evidence and proportionality rather than enthusiasm or conservatism alone.

### Practice questions

For each scenario, decide your answer before reading the explanation. Where the format is most/least effective, choose one of each.

**Question 1 (moderate) - Governance shortcut under deadline pressure**

A policy team urgently needs case data joined with staffing data for a ministerial briefing due in three days. The data sharing agreement (DSA) covering this join has not been signed. The policy lead, senior to you, says: "Just run the join in your environment - nobody will mind, it's for the minister." Choose the MOST and LEAST effective responses.

- A) Run the join as asked; the ministerial deadline justifies it, and you can complete the paperwork afterwards.
- B) Refuse by email, copying the information governance team, stating that the request was improper.
- C) Explain that you cannot run the join without the DSA, and immediately offer routes that can work: contacting the Information Asset Owners for urgent countersignature, checking whether the urgent-authorisation route applies, or preparing an anonymised or aggregated version that answers the briefing question without personal data.
- D) Tell the policy lead you will look into it, then quietly let the deadline pass without acting.

**Most effective: C. Least effective: D.**

**Explanation:** Option C holds the governance line while treating the user need as real - the essence of senior data engineering in government. It neither blocks nor capitulates: it converts an improper request into a proper one by offering legitimate fast paths, including the data-minimising option of aggregation, which often serves a briefing better anyway. This demonstrates managing differing stakeholder perspectives and communicating between the technical and non-technical. Option A is seriously weak - it processes personal data without a lawful basis and normalises pressure-driven exceptions - but option D is the least effective: it combines the governance failure of unresolved risk with dishonesty ("I will look into it") and guarantees the stakeholder is let down at the worst moment, damaging trust in the whole team. Passive avoidance is consistently rated worst in situational judgement tests because it resolves nothing and adds deception. Option B gets the compliance substance right but chooses escalation-by-ambush over collaboration; copying governance may eventually be necessary, but as a first move it burns a relationship the team needs.

**Question 2 (moderate) - Architect versus delivery manager**

You are designing a new integration. The technical architect insists on rebuilding the flow on the strategic platform, adding roughly six weeks. The delivery manager insists on reusing the legacy flow to hit the quarter's commitment, and both have begun lobbying your engineers separately, creating tension in stand-ups. Choose the MOST and LEAST effective responses.

- A) Convene a short options session with both, present a component-level analysis - what can be reused, what the rebuild buys, costs and risks of each, including a phased option - and drive to a documented decision with the service owner as arbiter if needed.
- B) Side with the delivery manager; commitments to users come first, and the strategic platform will still be there next quarter.
- C) Side with the architect; strategic alignment prevents technical debt, and the delivery manager will have to manage expectations.
- D) Tell your engineers to ignore both until the two of them sort out their disagreement.

**Most effective: A. Least effective: D.**

**Explanation:** This scenario tests the duties at the top of your role profile: hosting discussions in a multidisciplinary team with difficult dynamics and managing differing stakeholder perspectives. Option A does the senior engineer's real job - replacing positional lobbying with evidence. A component-level reuse analysis (as in the cognitive section's Question 10) frequently dissolves the binary: reuse the transformation logic now, migrate the delivery mechanism next quarter. Crucially, A also names an arbiter, so the decision is made transparently and recorded, not re-litigated in stand-ups. Options B and C are mirror-image weaknesses: each may be the right outcome, but choosing a side without analysis rewards lobbying, alienates the other stakeholder, and leaves your engineers watching decisions made by force of personality. Option D is least effective: it abandons your team to the crossfire, lets the tension fester in stand-ups you are responsible for protecting, and outsources a decision that sits naturally with you. Collaboration in government digital work means engineering the decision process, not just the pipeline.

**Question 3 (easy) - Junior engineer's code before a release**

Reviewing a junior engineer's pull request the day before a scheduled release, you find their transformation handles the happy path well but will silently drop records with missing dates - a scenario the specification does not address. The junior engineer has worked hard and is visibly proud of the work. Choose the MOST and LEAST effective responses.

- A) Approve the release to protect their confidence, and fix the code quietly next sprint.
- B) Flag the missing-date gap in review as a specification question, work through the fix with them pairing so they own it, and agree with the delivery manager whether the release holds or ships with the gap documented and monitored.
- C) Rewrite the code yourself tonight so the release is safe and the deadline holds.
- D) Reject the pull request with a comment listing the defects, and remind the team that silent data loss is unacceptable.

**Most effective: B. Least effective: A.**

**Explanation:** Option B does three senior things at once. It treats the defect accurately - the specification is silent, so this is an issues-and-risks finding from your testing skill, not just a coding error. It develops the junior engineer through pairing, so the learning and the ownership stay with them - how you build teams to complete data integration services. And it makes the ship/hold decision transparently with the delivery manager, rather than unilaterally. Option A is least effective despite its kind intention: silent data loss is among the worst defect classes in data engineering because downstream users cannot see what is missing; shipping it knowingly, undocumented, subordinates data integrity and user needs to one person's feelings - and quietly fixing it later denies the engineer the chance to learn. Option C rescues the release but teaches nothing, burns you out, and signals that hard problems get taken away from juniors. Option D is technically defensible but developmentally poor - public, list-form criticism of a proud junior colleague damages the psychological safety that inclusion in a multidisciplinary team depends on. The strongest answers separate the standard (non-negotiable) from the person (supported).

**Question 4 (challenging) - Incident transparency with a service owner**

A streaming pipeline your team owns delivered stale data to a fraud-screening service for three hours yesterday because of a configuration change your team deployed without adequate testing. The fraud team has not noticed. Your service owner has a board meeting tomorrow. Choose the MOST and LEAST effective responses.

- A) Say nothing; the impact window has passed, no events were lost, and raising it now would create noise before the board.
- B) Tell the service owner and the fraud team today: what happened, the window affected, what decisions might have used stale data, and the specific testing and monitoring changes you are making so it cannot recur silently.
- C) Mention it to the service owner informally as a minor blip, without specifics, so they are covered if asked.
- D) Fix the testing gap first, then disclose next week once you can show the fix is in place.

**Most effective: B. Least effective: A.**

**Explanation:** Option B is uncomfortable and correct. Transparency is a core public sector value, and it is also operationally necessary here: the fraud team made real decisions on stale data (recall Passage C in the verbal section) and only they can assess whether any decision needs revisiting - concealment forecloses that. Disclosing with the impact window, the affected decisions, and the preventative measures attached is textbook problem management: resolution plus prevention, communicated to the people affected. It also protects the service owner from the worst boardroom position - learning of an incident from someone else. Option A is least effective: it converts an honest engineering failure into a concealment, which in government is far more damaging than the original incident, and it leaves potentially flawed fraud decisions standing. Option C performs disclosure without its substance; vagueness that is designed to cover rather than inform fails the transparency test while creating the illusion it was met. Option D reverses the right order - affected users' need to know is immediate, while the fix has its own timeline; delaying disclosure to improve the story is a subtler form of option A. Senior credibility is built in exactly these moments.

**Question 5 (moderate) - The enthusiastic technology proposal**

A capable engineer on your team proposes migrating your batch integrations to a new open-source streaming framework they have been exploring. They are enthusiastic, technically persuasive, and have prepared a demo. The framework is genuinely promising but young: small community, no managed offering on your platform, and no one else in the department uses it. Choose the MOST and LEAST effective responses.

- A) Approve a migration of one significant pipeline; enthusiasm like this should be rewarded and the technology probably is the future.
- B) Decline; the department's standard tools exist for a reason, and the team should focus on delivery.
- C) Channel the enthusiasm into a bounded evaluation: a time-boxed spike on a non-critical flow, with explicit criteria - operability, skills demands, support model, exit cost - and a short write-up to share with the architecture community.
- D) Ask the engineer to keep exploring it in their own time and report back if the community grows.

**Most effective: C. Least effective: A.**

**Explanation:** Your role profile includes understanding the impact on the organisation of emerging trends in data tools - which means neither reflexive adoption nor reflexive refusal, but structured evaluation. Option C converts enthusiasm into evidence: time-boxed, criteria-led, on a flow where failure is cheap, with findings shared beyond the team so the organisation learns once rather than five times. The criteria named are the ones that kill young frameworks in government settings - operability, skills, support, exit cost - exactly the resilient, scalable, future-proofed test from your integration design skill. Option A is least effective: committing a significant pipeline to an unproven framework with no support model gambles a production service on enthusiasm, and "probably the future" is not an engineering argument; if it fails, the cost lands on users and on the engineer you meant to encourage. Option B is safer but wasteful - it teaches your best people that initiative is unwelcome, which is corrosive to the team you are supposed to be building. Option D outsources evaluation to unpaid personal time, which is poor inclusion practice and signals the idea is not taken seriously. Reward the behaviour, bound the risk.

**Question 6 (moderate) - Analyst misreading the data**

An analyst in another team publishes an internal dashboard using your case dataset, showing a sharp regional rise in case volumes. You know the rise is an artefact: a source system migration you led means one region's historical records were backfilled last month. The analyst's finding is already being discussed by policy colleagues. Choose the MOST and LEAST effective responses.

- A) Contact the analyst directly, explain the backfill and its effect on their chart, offer to help them correct and annotate the dashboard, and improve the dataset's catalogue entry so the backfill is documented for all future users.
- B) Email the policy colleagues to tell them the dashboard is wrong before any decisions are made.
- C) Post a correction in the departmental data community channel so everyone learns about the artefact.
- D) Note it for the next data quality forum in three weeks; the analyst owns their dashboard and its corrections.

**Most effective: A. Least effective: D.**

**Explanation:** Option A fixes the immediate error through the person responsible for it, preserves the analyst's standing by helping rather than exposing them, and - the distinctly senior move - fixes the systemic cause: the backfill was known to you but invisible in the metadata, so the catalogue entry gets improved. That last step is your metadata management skill doing its real job: supporting the end use of the data by people you will never meet. Option B corrects the record but routes around the analyst, embarrassing them before their stakeholders and teaching them nothing; it should be the follow-up only if the analyst will not act and decisions are imminent. Option C spreads awareness but publicises an individual's error before giving them the chance to correct it - poor collaboration hygiene. Option D is least effective: a known-wrong finding is actively influencing policy discussion now, and waiting three weeks on procedural grounds lets misinformation compound daily. "Not my dashboard" is technically true and professionally wrong; presenting clear insights to support the end use of the data includes stopping your data being misread when you are the only person who knows why.

**Question 7 (challenging) - Ranking under incident pressure**

At 07:40, the overnight load feeding a statutory 09:30 publication has failed. Initial logs suggest an upstream schema change. Your two platform specialists are both on leave today. Rank ALL FOUR actions from most to least effective as your FIRST move.

- A) Start debugging the failure yourself immediately; you are the strongest engineer available and time is short.
- B) Spend five minutes establishing facts - failure point, error, scope, feasibility of a rerun - then alert the publication team and your service owner with an honest early assessment and a next-update time, while the best available engineer starts diagnosis in parallel.
- C) Call one of the specialists on leave; the statutory deadline justifies the intrusion.
- D) Wait until you fully understand the problem before telling anyone, so you do not cause unnecessary alarm.

**Correct ranking: B, A, C, D.**

**Explanation:** B ranks first because it does the two things that matter in the first minutes of an incident: establish enough facts to speak accurately, and give affected stakeholders early, honest notice with a committed next update - transparency that lets the publication team activate their own contingencies (delay notices, fallback figures) which are theirs to invoke, not yours. Diagnosis proceeding in parallel loses almost nothing. A ranks second: energetic and personally competent, it fixes the technical problem while leaving the publication team blind; as a first move it also puts the senior leader heads-down where coordination should be. C ranks third: it might work, but as a first move it disrespects leave boundaries before establishing whether the on-shift team can cope - consulting specialists where required is your problem management skill, but it follows fact-finding, not fear. D ranks last: silence until full understanding is the classic incident anti-pattern; stakeholders lose their reaction time, and the eventual conversation is worse ("you knew at 07:40?"). Notice the general principle assessments reward: communicate early with what you know and when you will know more - never wait for certainty that may arrive after the deadline.

**Question 8 (moderate) - Pressure to skip reconciliation**

A migration you lead has completed its final dress rehearsal. Reconciliation shows a small unexplained variance in financial totals for one table. The service owner, under pressure to hit a publicly announced go-live date, says: "It is 0.003% - accept it and let's go." Your test strategy states any variance in financial totals must be investigated before go-live. Choose the MOST and LEAST effective responses.

- A) Accept the variance; 0.003% is immaterial by any reasonable standard, and the strategy was written before the date was announced.
- B) Explain that unexplained financial variances are categorically different from small count variances - the size of an unexplained error says nothing about the size of its cause - give a time-boxed estimate for root-causing it, and present the service owner with explicit options and risks, escalating to the migration board if they still wish to accept it.
- C) Refuse to sign off and state that go-live cannot happen, full stop.
- D) Sign off as instructed but record in the log that you disagreed.

**Most effective: B. Least effective: D.**

**Explanation:** The technical insight at the centre of option B is the one that separates senior engineers: an unexplained variance is not a small problem, it is an unmeasured one. 0.003% could be a rounding difference - or the visible edge of a truncation bug that nets to nearly zero. Investigation converts unknown risk into known risk; only then can anyone accept it honestly. B also respects governance: the decision to accept a documented risk belongs to the migration board per the strategy, and giving the service owner options, timings and an escalation route treats them as the accountable adult they are. Option A abandons the strategy's explicit "any variance... must be investigated" rule under pressure and reasons from the error's size, which is precisely the fallacy. Option C holds the right line the wrong way - blanket refusal without options or time-box gives the stakeholder nothing to work with and casts assurance as obstruction. Option D is least effective: it knowingly enacts what you believe is wrong while constructing a paper trail to protect yourself - the log entry proves you understood the risk and proceeded anyway. Accountability without candour is the worst combination in public service.

**Question 9 (easy) - The quiet voice in the design review**

In your fortnightly design review, a confident senior developer from a partner team repeatedly talks over a less experienced data engineer from your team, who eventually stops contributing - though her earlier half-finished point about metadata dependencies sounded important. Choose the MOST and LEAST effective responses.

- A) Let the discussion flow; interrupting the senior developer would create exactly the awkwardness you want to avoid, and your engineer can raise her point afterwards.
- B) As chair, steer back explicitly: "Before we move on, I want to hear the rest of the point about metadata dependencies" - and afterwards, privately check in with your engineer and have a quiet word with the senior developer about interruptions.
- C) Publicly tell the senior developer to stop interrupting people.
- D) Follow up with your engineer by email after the meeting to get her point, and add it to the notes.

**Most effective: B. Least effective: A.**

**Explanation:** Your role profile makes you the host of discussions in teams with potentially difficult dynamics, and hosting is an active verb. Option B fixes the moment (the point is heard while the design can still absorb it), the person (a check-in that says her contribution matters), and the pattern (a private, low-drama word about interruptions) - inclusion enacted as chairing craft rather than confrontation. Option A is least effective: it treats the chair's discomfort as weightier than the engineer's exclusion, likely loses a materially important design input, and teaches both parties the meeting's real rules - interrupters win, quieter voices stop trying. Junior colleagues rarely "raise it afterwards"; they conclude their input is unwelcome. Option C protects the engineer but publicly, trading one person's face for another's, and often makes the room warier rather than safer. Option D recovers the content but not the culture: the design gets the point, but everyone watching learned that being talked over goes unaddressed. Accessibility and inclusion in government digital work are not abstractions - they are what the chair does in minute forty of a design review.

**Question 10 (challenging) - Advocating for the team externally**

At a cross-programme meeting, a delivery director states that "the data engineering team has become the bottleneck" and proposes moving two of your engineers to a supplier-led workstream. You know the real story: your team absorbed unplanned work from a failed supplier deliverable last quarter, and your throughput is actually up 20%. Your engineers have heard the bottleneck comment and morale has dipped. Choose the MOST and LEAST effective responses.

- A) In the meeting, acknowledge the delivery pressure is real, offer to bring a short evidence pack - workload sources, throughput trend, the absorbed supplier work - to the next planning session, and ask that the resourcing proposal wait for that evidence; afterwards, brief your team honestly on what was said and how you are responding.
- B) Accept the criticism diplomatically and absorb the resourcing change; senior directors have visibility you lack, and pushing back looks defensive.
- C) Rebut the director on the spot with the throughput figures from memory and point out that their supplier caused the backlog.
- D) Say nothing in the meeting, then raise your concerns informally with your own line manager afterwards.

**Most effective: A. Least effective: B.**

**Explanation:** Being an advocate for the team externally - a named behaviour in your role profile - means correcting the record with evidence, through a process that lets decision-makers change course without losing face. Option A does this precisely: it validates the director's underlying concern (delivery pressure is real), replaces anecdote with data on a short timescale, and asks only that an irreversible decision wait for evidence - a request no reasonable forum refuses. The closing move matters most for your team: they heard the criticism, so they must hear the defence, or morale damage compounds. Option B is least effective: it accepts a false narrative into the programme's record, loses two engineers on the strength of it, and - worse - shows your team that no one defends them, which is how good engineers start leaving. Option C has the right facts and the wrong forum: a from-memory rebuttal that blames the director's supplier turns a resourcing discussion into a public contest the relationship may not survive, and any misremembered figure destroys your credibility. Option D preserves harmony you do not need at the cost of influence you do - your line manager was not in the room and cannot un-say what was said there. Evidence, delivered calmly, in a process: that is senior advocacy.

**Question 11 (moderate) - The metadata shortcut**

Mid-sprint, you discover the team has been publishing new datasets without catalogue entries for six weeks - "we'll backfill the metadata when the delivery pressure eases", says your most senior engineer, who took the decision while you were focused on the migration. Downstream analysts have begun asking what the new fields mean. Choose the MOST and LEAST effective responses.

- A) Publicly reverse the decision at stand-up and assign the backlog of catalogue entries to the engineer who made the call.
- B) Talk privately with the engineer to understand the pressure that drove the call, agree that undocumented datasets stop at the next publication, make catalogue entries part of the definition of done, and schedule the backfill as visible, planned work - starting with the datasets analysts are actually asking about.
- C) Let it continue until the delivery pressure genuinely eases; the engineer made a reasonable triage call and overriding it undermines them.
- D) Backfill the catalogue entries yourself over the next few evenings to avoid burdening the team.

**Most effective: B. Least effective: D.**

**Explanation:** Option B repairs all three broken things. The standard: metadata is not deferrable decoration - undocumented fields are already costing analysts time, which is the end use of the data your role exists to support - so the definition of done changes, and the leak stops at source. The person: the engineer made a defensible-feeling triage call under pressure you did not see; understanding it privately preserves their standing and probably surfaces a real resourcing problem. The backlog: prioritised by user demand, planned and visible, not squeezed into gaps. This is metadata management as your profile means it - designing the repository and advising the team about it. Option A gets the standard right and the people wrong: public reversal plus punitive assignment humiliates your strongest engineer for a judgement call. Option C mistakes loyalty for leadership - the analysts' unanswered questions are the evidence that "when pressure eases" means never. Option D is least effective, though it looks generous: it hides the true cost of the shortcut from the team and the planning process, fixes nothing systemic (next quarter's datasets will be undocumented too), sets an unsustainable personal precedent, and denies the team the learning. Senior engineers fix systems, not just symptoms - even when the symptom is quicker to fix.

### Preparation tips

- **Anchor on the values, not the politics.** UK public sector situational judgement scenarios consistently reward user needs, transparency, collaboration, inclusion, and evidence-based decisions. When torn between options, ask which one a well-run public organisation would want on the record.
- **Look for the option that fixes the system.** At senior level, the strongest responses usually address the immediate issue and its recurrence - the preventative measure, the definition-of-done change, the improved catalogue entry.
- **Check who owns the decision.** Many scenarios hinge on governance: variances belong to migration boards, contingency choices to publication teams, funding to planning rounds. Options where you quietly take or dodge someone else's decision are usually weak.
- **Practise the "most and least" separately.** The least effective option is often easier to identify - look for passivity, concealment, or self-protection - and eliminating it sharpens your choice of the best.
- **Reflect on your real incidents.** Before the assessment, recall two or three genuine dilemmas from your own leadership - what you did, what worked. The test measures judgement you already exercise; recent, honest reflection calibrates it.

### Common pitfalls

- **Choosing the idealistic over the effective.** "Refuse and stand firm" options sound principled but often give stakeholders nothing to work with; the effective option usually holds the line and offers a workable route.
- **Selecting passive options.** Waiting, deferring to forums weeks away, handing the problem back, or fixing things quietly yourself - these consistently rate poorly because they delay action, dodge ownership, or hide problems.
- **Ignoring the people in people problems.** Options that are technically correct but publicly humiliate a colleague, or bypass the person responsible, lose marks on collaboration and inclusion - both core public sector values.
- **Solving only the visible instance.** Correcting one dashboard, one dataset, or one release while leaving the cause untouched is a mid-level answer to a senior-level question.
- **Forgetting your dual audience.** As a senior engineer you answer upwards (service owners, boards) and downwards (your team) simultaneously; the best options usually communicate honestly in both directions, as in the incident and advocacy scenarios above.

## Conclusion

Well done for working through this resource. You have covered substantial ground: the cognitive assessment's pattern recognition, fault diagnosis and constraint-based reasoning; the numeric assessment's throughput, capacity, cost and break-even arithmetic; the verbal assessment's disciplined reading of policies, standards and stakeholder correspondence; and the situational judgement assessment's dilemmas of governance, transparency, team dynamics and advocacy. Every question was built from the real substance of your role - the data flows you design, the streaming systems you lead, the code you optimise, the databases you manage, and the multidisciplinary relationships you navigate.

If one message stays with you, let it be this: these assessments do not measure something foreign to you. They measure, under structured conditions, the judgement you already exercise every working day. A senior data engineer who traces failure propagation through a DAG, weights rejection rates by volume, reads "may" differently from "must", and discloses an incident honestly is already practising every skill these tests reward. Preparation simply removes surprise, so that your genuine capability - not your unfamiliarity with a question format - determines your result.

For next steps, consider three habits. First, little and often: ten minutes of practice several times a week builds more fluency than a single long session. Second, review your errors more carefully than your successes: each wrong answer is a precise pointer to a reasoning habit worth adjusting. Third, connect practice back to work: the weighted average you compute in a test tomorrow is the platform report you present next month, and the situational scenarios are rehearsals for conversations you will genuinely have.

Beyond assessments, this material doubles as professional development for the role itself - and for wherever you are heading next, whether deeper technical mastery or leadership at principal level. Approach the real assessment rested, unhurried, and confident that you have prepared properly. You bring years of genuine engineering judgement with you into that room. Trust it, and good luck.
