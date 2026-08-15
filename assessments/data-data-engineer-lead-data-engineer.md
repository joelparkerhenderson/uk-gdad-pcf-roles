# Data Engineer (Lead Data Engineer) - Psychometric Assessment Resources

## Introduction

Welcome. This document is a practical, role-specific preparation resource for psychometric assessments, written for you as a lead data engineer working within the UK Government Digital and Data (GDAD) Profession Capability Framework. Whether you are preparing for a promotion board, an internal capability review, a move to another department, or simply investing in your own professional development, this guide will help you understand what these assessments involve and how to perform at your best.

Psychometric assessments are structured, standardised exercises that measure the mental capabilities and behavioural judgement that underpin effective performance in a role. They are widely used across the Civil Service and the wider public sector because they are objective, evidence-based, and fair: every candidate faces the same questions, marked against the same criteria, which reduces the influence of unconscious bias in selection and development decisions. For a senior technical leadership role such as yours, they are less about abstract puzzles and more about the realistic demands of the job: interpreting pipeline metrics, reasoning through integration standards documents, weighing competing stakeholder needs, and making sound judgement calls under pressure.

This document covers four assessment types, each in its own section:

1. **Workplace job-specific cognitive assessment** — pattern recognition, logical deduction, error checking, prioritisation, and problem solving using the artefacts you genuinely handle: data flow diagrams, schema definitions, streaming configurations, and test results.
2. **Workplace job-specific numeric reasoning assessment** — interpreting tables, percentages, ratios, budgets, throughput figures, and performance metrics of the kind you see in capacity planning and service reporting.
3. **Workplace job-specific verbal reasoning assessment** — drawing accurate conclusions from dense written material such as data standards, integration policies, stakeholder emails, and governance reports.
4. **Workplace job-specific situational judgement assessment** — choosing effective responses to realistic dilemmas involving your teams, senior stakeholders, cross-government partners, and suppliers.

Each section explains what the assessment measures, maps it explicitly to the skills in your role profile — from data modelling and metadata management through to communicating between the technical and non-technical — and then gives you a substantial set of practice questions with full worked answers. Each section closes with preparation tips and common pitfalls.

How to use this guide: work through it actively rather than reading it passively. Attempt each practice question before reading the answer, time yourself where suggested, and treat the explanations as coaching rather than marking. Where you get a question wrong, resist the urge to move straight on; understanding *why* the correct answer is correct is where the real preparation value lies. You already operate at a senior level — this guide is about sharpening instincts you use every day and translating them into assessment performance.

Good luck, and enjoy the practice.

## Advisory

"This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff."

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive assessment measures the core mental processes you rely on as a lead data engineer: pattern recognition, logical deduction, error checking, prioritisation, and structured problem solving. Unlike a generic IQ test, every question is built around practical workplace scenarios and data formats drawn from the actual job — in your case, data flow diagrams, schema definitions, streaming system configurations, dependency graphs, test outputs, and integration runbooks.

Typical delivery is online and timed, usually 15 to 30 minutes, with objective scoring against a norm group of comparable professionals. Many modern platforms are adaptive, adjusting question difficulty based on your previous answers, and most provide a short, ungraded practice set beforehand so you can get comfortable with the interface. Employers generally receive a breakdown of speed versus accuracy rather than a single raw score, so working carefully and steadily matters as much as working fast.

Why does this matter for your role? At lead level you are responsible for the design and implementation of numerous complex data flows connecting operational systems, analytics platforms, and business intelligence systems. That work is fundamentally cognitive: you spot the recurring pattern across three teams' pipelines that could be replaced by one reusable flow; you deduce which upstream change broke a downstream dashboard; you check a colleague's transformation logic for subtle errors before it reaches production; and you prioritise a queue of incidents, feature requests, and standards work every week. A cognitive assessment is, in effect, a compressed simulation of that daily reasoning.

### What it measures for your role

The assessment dimensions map directly onto the skills in your role profile:

- **Pattern recognition → Data analysis and synthesis and Data modelling.** Recognising structural similarity across data sources is exactly what you do when you bring multiple sources together into a conformed model, or when you spot opportunities to reuse and align data models across organisations.
- **Logical deduction → Problem management and Systems integration.** Tracing cause and effect through connected systems — "if the reference data feed is stale, which downstream flows are affected?" — mirrors coordinating your team to investigate, resolve, and anticipate problems.
- **Error checking → Testing and Programming and build.** Spotting the mismatched data type, the off-by-one window boundary, or the inconsistent naming in a schema reflects your responsibility to review specifications, define test conditions, and ensure code quality across moderate-to-complex programs.
- **Prioritisation → Data development process and Problem management.** Deciding what your teams tackle first, under enterprise-scale integration procedures and finite resources, is a judgement the assessment probes through ranking and sequencing tasks.
- **Abstraction and rule induction → Data integration design and Metadata management.** Inferring the general rule from specific cases is how you establish standards, keep them current, and design metadata repositories that classify things consistently.

### Practice questions

Work through these without notes first, then study the explanations. Aim for two to three minutes per question.

**Question 1 (easy) — Pattern recognition in naming standards**

Your team's data integration standard requires dataset names in the form `domain_source_entity_frequency`. Four datasets have just been registered in the metadata repository:

1. `tax_hmrc_returns_daily`
2. `benefits_dwp_claims_weekly`
3. `daily_borders_hof_crossings`
4. `health_nhsd_prescriptions_monthly`

Which dataset violates the standard?

A) Dataset 1  B) Dataset 2  C) Dataset 3  D) Dataset 4

**Correct answer: C.**

**Explanation:** The standard fixes the order of the four segments: domain, source, entity, frequency. Datasets 1, 2, and 4 all follow that order (for example, `tax` domain, `hmrc` source, `returns` entity, `daily` frequency). Dataset 3 begins with the frequency (`daily`), then domain (`borders`), then source (`hof`), then entity (`crossings`) — the right components in the wrong order. This is the kind of consistency check you perform when you ensure teams adhere to standards you have established: the error is not a missing element, but a sequencing violation that automated tooling might miss if it only checks for four segments.

**Question 2 (easy) — Logical deduction from pipeline dependencies**

You maintain this dependency chain: the ingestion job A feeds staging table B; B feeds both the conformed model C and the audit log D; C feeds the BI dashboard E. This morning, E shows yesterday's data, but D is fully up to date.

Which single component is the most likely point of failure?

A) Job A  B) Table B  C) Model C  D) Dashboard E's refresh, or the B→C step

**Correct answer: D.**

**Explanation:** Deduce from what is working. D is up to date, and D is fed by B, so A and B must have run successfully — eliminating options A and B. The failure therefore lies downstream of B on the path to E: either the transformation from B into conformed model C, or C's feed into E, or E's own refresh. Option D is the only one consistent with the evidence. Option C alone is too narrow: with the information given you cannot distinguish a C failure from an E refresh failure, so the correct deduction identifies the failing *segment*, not a single unproven component. This mirrors real problem management: use healthy branches of the flow to bound where the fault can be.

**Question 3 (moderate) — Error checking a transformation specification**

A specification for a data flow states: "Records with a `status` of ACTIVE or PENDING are loaded into the conformed model. Records with a `status` of CLOSED are archived. Records with any other status are rejected to the quarantine queue." A junior engineer implements this as:

- If status = ACTIVE → load
- If status = PENDING → load
- If status = CLOSED → archive
- If status is NULL → reject to quarantine

What is wrong with the implementation?

A) Nothing — it matches the specification
B) CLOSED records should be rejected, not archived
C) The implementation only rejects NULL statuses, but the specification requires rejecting *any* status that is not ACTIVE, PENDING, or CLOSED
D) PENDING records should be archived

**Correct answer: C.**

**Explanation:** The specification's final rule is a catch-all: "any other status" includes NULL, but also SUSPENDED, unknown codes, typos, and future values nobody has thought of yet. The implementation narrows "any other" to "NULL", so a record with status = SUSPENDED would silently fall through all four rules and its fate would depend on undefined behaviour — perhaps dropped, perhaps crashing the job. This is a classic error-checking trap: each implemented rule is individually correct, so a line-by-line comparison passes, but the *coverage* is incomplete. When you review specifications and define test conditions, testing the unhappy path — values outside the enumerated set — is precisely what catches this class of defect before production.

**Question 4 (moderate) — Rule induction from metadata examples**

Your metadata repository classifies datasets by sensitivity. You observe these existing classifications:

- Payroll extracts: OFFICIAL-SENSITIVE
- Aggregated monthly service statistics: OFFICIAL
- Individual citizen case records: OFFICIAL-SENSITIVE
- Published open data on office locations: OFFICIAL
- Staff disciplinary records: OFFICIAL-SENSITIVE

A new dataset arrives: row-level records of individual benefit applications, including national insurance numbers. Applying the induced rule, how should it be classified?

A) OFFICIAL, because benefits data is routine government business
B) OFFICIAL-SENSITIVE, because the pattern shows person-identifiable, row-level data is classified as sensitive
C) It cannot be classified without a new rule
D) OFFICIAL, because it will eventually be aggregated

**Correct answer: B.**

**Explanation:** Inducing the rule from the examples: every OFFICIAL-SENSITIVE item contains information about identifiable individuals (payroll, case records, disciplinary records), while every OFFICIAL item is aggregated or non-personal (monthly statistics, office locations). The new dataset is row-level and person-identifiable — it includes national insurance numbers — so the induced rule places it in OFFICIAL-SENSITIVE. Option D is a distractor that confuses the dataset's *future* derived form with its current form; classification must reflect the data as it exists. This kind of rule induction is exactly what you exercise when you design the method to categorise data models and metadata within an organisation: the classification scheme must be learnable, consistent, and predictable for the teams applying it.

**Question 5 (moderate) — Prioritisation under constraint**

It is 09:00 Monday. Four items compete for your team's attention today:

1. A streaming pipeline feeding a ministerial dashboard has stopped; the dashboard is used at a 14:00 briefing.
2. A quarterly review of integration standards is due to the architecture board by Friday.
3. A junior engineer is blocked on a code review for a routine enhancement.
4. A partner department reports that last night's batch file arrived with 3% fewer records than usual; their next consuming job runs Wednesday.

What is the most defensible order of attention?

A) 1, 3, 4, 2  B) 2, 1, 3, 4  C) 1, 4, 3, 2  D) 4, 1, 2, 3

**Correct answer: A.**

**Explanation:** Rank by deadline proximity and impact. Item 1 has both the nearest hard deadline (14:00 today) and the highest visibility, so it comes first. Item 3 is a fifteen-minute unblocking action with an outsized effect — a blocked engineer loses a whole day while you do other things — so cheap, high-leverage unblocking comes next. Item 4 matters, but its consumer does not run until Wednesday, giving a full day of slack; it can be investigated after lunch. Item 2 has a Friday deadline and can be scheduled deliberately later in the week. Option C is the strongest distractor: it treats the 3% anomaly as more urgent than the blocked colleague, but the anomaly has slack while the colleague's idle time is being spent *right now*. Good prioritisation weighs deadlines, blast radius, and the cost of delay — not just how alarming an issue sounds.

**Question 6 (moderate) — Spotting the reusable pattern**

Three teams describe their pipelines to you:

- Team Alpha: pulls customer records nightly from System X, validates postcodes, standardises addresses, loads to their analytics store.
- Team Beta: pulls supplier records weekly from System Y, validates postcodes, standardises addresses, loads to a reporting database.
- Team Gamma: streams sensor readings from field devices, applies unit conversions, loads to a time-series store.

Which component is the strongest candidate for a shared, reusable data flow, and why?

A) The nightly scheduling logic, because Alpha and Beta both use schedules
B) The postcode validation and address standardisation step, because two teams implement identical business logic on different data
C) The loading step, because all three teams load data somewhere
D) Nothing — the teams work on different data so nothing is reusable

**Correct answer: B.**

**Explanation:** Reuse value is highest where the *logic* is identical even when the *data* differs. Alpha and Beta both validate postcodes and standardise addresses — the same non-trivial, maintenance-heavy business logic, currently duplicated, doubtless drifting apart with every bug fix one team applies and the other misses. Extracting it into a shared, well-tested service or library halves maintenance and guarantees consistent address handling. Option A fails because scheduling is commodity infrastructure, not duplicated business logic, and Alpha and Beta do not even share a schedule. Option C is superficial: "loading data" is not one component when the targets are an analytics store, a reporting database, and a time-series store. Recognising and sharing opportunities to reuse existing data flows between teams is a named responsibility at your level, and the skill being tested is seeing past surface differences (customers versus suppliers) to structural sameness.

**Question 7 (moderate) — Deduction across a streaming topology**

A streaming system has topics T1, T2, and T3. Consumer group G1 reads T1 and writes enriched events to T2. Consumer group G2 reads T2 and writes aggregates to T3. Monitoring shows: T1 receiving events normally; consumer lag on T2 growing steadily; T3 receiving no new aggregates for 40 minutes.

Which is the most consistent single explanation?

A) The producers into T1 have stopped
B) G1 has stopped consuming T1
C) G2 has stopped or stalled, so T2 messages accumulate unread and T3 receives nothing
D) T3's storage is full

**Correct answer: C.**

**Explanation:** Work through each claim against the evidence. T1 is receiving normally, so producers are fine — A is out. If G1 had stopped, T2 would receive *no new messages*; but lag on T2 is *growing*, which means messages are arriving at T2 faster than they are consumed — so G1 is alive and writing, ruling out B. Growing lag on T2 plus silence on T3 points to the consumer between them: G2 has stalled, leaving T2's messages unread and producing nothing into T3. Option D would produce write errors from G2 and possibly *shrinking* lag as G2 keeps reading, which contradicts the observations. As the person responsible for the build of data-streaming systems, this end-to-end causal tracing — using lag metrics as evidence about which stage is alive — is a core diagnostic pattern worth internalising until it is automatic.

**Question 8 (hard) — Error checking a conformed model mapping**

You are reviewing a mapping document that conforms three source systems into one `citizen_contact` model. The mapping states:

- Source A `phone` (format: `+44XXXXXXXXXX`) → target `phone_e164`
- Source B `telephone` (format: `0XXXXXXXXXX`) → target `phone_e164`, transformed by replacing leading `0` with `+44`
- Source C `contact_num` (format: `+44XXXXXXXXXX` or `0XXXXXXXXXX`, mixed) → target `phone_e164`, transformed by replacing leading `0` with `+44`

What defect will this mapping introduce?

A) Source A numbers will be double-prefixed
B) Source B numbers will lose a digit
C) Source C numbers already in `+44` format will pass through the `0`-replacement rule unchanged — which is correct — so there is no defect
D) Source C values starting with `+44` are fine, but the rule as written for C is a blind find-and-replace of leading `0`; nothing handles a C value that is malformed or empty, and more importantly a `+44` number whose *subscriber* portion legitimately starts after the prefix is untouched — the real defect is that C's mixed formats are handled by a rule specified only for one of the two formats, so behaviour for `+44`-format C records is unspecified in the document

**Correct answer: D.**

**Explanation:** The subtle issue is a *specification completeness* defect rather than an arithmetic one. For Source C the document declares two possible input formats but specifies a transformation for only one of them ("replacing leading `0` with `+44`"). What happens to a C record already in `+44` format? Probably the developer will pass it through — but the document does not *say* so, and an implementer could equally reject it, re-prefix it, or crash. Option C asserts the pass-through behaviour as fact; the document never states it, and reviews must flag what is unspecified rather than assume the friendly interpretation. Options A and B describe transformations the document does not contain. When you establish enterprise-scale integration procedures, this is the review discipline that matters: every declared input variant must have an explicitly specified outcome, because unspecified behaviour becomes inconsistent behaviour the moment two teams implement the same mapping.

**Question 9 (hard) — Prioritising a problem investigation**

Overnight, four alerts fired across your estate:

1. The metadata repository's nightly sync failed (it retries automatically each night).
2. A conformed model load succeeded but processed 40% more records than any previous run.
3. A streaming consumer restarted three times, recovering each time within seconds.
4. A test environment ran out of disk space.

Your team can deep-dive only one alert this morning. Which one deserves it?

A) Alert 1  B) Alert 2  C) Alert 3  D) Alert 4

**Correct answer: B.**

**Explanation:** Alert 2 is the only one where *success* may be hiding a serious defect. A 40% volume spike with a green tick could mean duplicate ingestion, an upstream re-send, a broken deduplication step, or a source system incident — and the bad data is now *inside* the conformed model, propagating to every consumer with each passing hour. Alerts 1, 3, and 4 are self-limiting: the sync retries tonight, the consumer self-healed, and a full test disk blocks only test work. The counter-intuitive lesson — and the reason this question is hard — is that failed jobs announce themselves, while anomalous successes do not. Effective problem management at your level means coordinating the team to investigate and *anticipate* problems, and volume anomalies on successful runs are the classic early signal of silent data corruption.

**Question 10 (hard) — Logical consistency of integration standards**

Your draft integration standard contains these rules:

1. All inter-departmental data transfers must use the approved API gateway.
2. Bulk historical migrations are exempt from rule 1 and may use secure file transfer.
3. Any transfer containing OFFICIAL-SENSITIVE data must be encrypted in transit and logged in the transfer register.
4. Transfers via the approved API gateway are logged automatically and need no manual register entry.

A team plans a bulk historical migration of OFFICIAL-SENSITIVE case records via secure file transfer. Which obligations apply?

A) None — bulk migrations are exempt from the standard
B) Encryption in transit and a manual entry in the transfer register
C) Encryption in transit only, because logging is automatic
D) They must use the API gateway because the data is OFFICIAL-SENSITIVE

**Correct answer: B.**

**Explanation:** Apply each rule precisely. Rule 2 exempts bulk migrations from *rule 1 only* — the exemption's scope is the gateway requirement, not the whole standard, so option A over-reads it. Rule 3 attaches to the data's sensitivity regardless of transfer mechanism: encryption in transit and a register entry are both required. Rule 4's automatic logging applies only to gateway transfers; this transfer uses secure file transfer, so the register entry must be made manually — eliminating option C. Nothing in the rules makes the gateway mandatory for sensitive data over and above rule 1, from which this transfer is exempt, so option D invents a rule. Assessments love this structure — nested exemptions with carefully scoped clauses — because it mirrors real standards documents. As the person who establishes standards and keeps them up to date, reading scope words ("exempt from rule 1", not "exempt from this standard") with precision is a daily necessity.

**Question 11 (moderate) — Sequence completion in capacity terms**

A streaming topic's daily peak throughput over six successive weeks was: 120, 132, 145, 160, 176, 194 (thousand events per hour). If the pattern continues, which week-seven figure should you plan for, and what is the pattern?

A) About 205 thousand — the series adds a constant ~12
B) About 213 thousand — the series grows by roughly 10% each week
C) About 226 thousand — the series grows by roughly 16% each week
D) About 194 thousand — throughput has plateaued

**Correct answer: B.**

**Explanation:** Test the additive hypothesis first: differences are 12, 13, 15, 16, 18 — not constant, and growing, so option A's model is wrong. Test the multiplicative hypothesis: 132/120 = 1.10, 145/132 ≈ 1.098, 160/145 ≈ 1.103, 176/160 = 1.10, 194/176 ≈ 1.102. The ratio is stable at about 1.10, so growth is roughly 10% per week, and week seven is approximately 194 × 1.10 ≈ 213 thousand events per hour. Option D contradicts the data outright. The job-relevant insight: growing *differences* with stable *ratios* means exponential growth, and exponential growth is what breaks streaming systems that were capacity-planned with straight-line thinking. Recognising which model fits — additive or multiplicative — is the difference between provisioning for 205 and provisioning for the 235 you will actually see two weeks later.

**Question 12 (hard) — Multi-constraint scheduling**

You must schedule four migration tasks — W, X, Y, Z — one per weekend, over four weekends, subject to:

- W must complete before Y (Y consumes W's outputs).
- Z cannot run on weekend 1 (its source system is frozen for year-end).
- Z must complete before X (X reuses the landing zone that Z's migration frees up).
- Y must run on weekend 3 or 4 (its downstream consumers are unavailable earlier).

Which schedule satisfies all constraints?

A) W, X, Y, Z  B) X, W, Y, Z  C) W, Z, Y, X  D) X, Z, Y, W

**Correct answer: C.**

**Explanation:** The efficient technique is elimination by the strictest constraint first. "Z before X" is highly restrictive, so test it across all options. Option A places X on weekend 2 and Z on weekend 4 — Z after X, violated. Option B places X on weekend 1 and Z on weekend 4 — violated again. Option D places X on weekend 1 and Z on weekend 2 — violated a third time (and D also fails "W before Y", since W sits on weekend 4 after Y on weekend 3). Only option C remains, and a full verification confirms it: W(1) before Y(3) ✓; Z(2) avoids weekend 1 ✓; Z(2) before X(4) ✓; Y on weekend 3 ✓. Note how much faster one well-chosen constraint eliminated three options than checking every constraint against every option would have been. This is exactly how you sequence real migration work when you coordinate teams: identify the binding constraint — usually a dependency or a frozen window — and let it collapse the schedule space before you fine-tune. In the assessment, a thirty-second written grid of options against constraints beats mental juggling every time.

**Question 13 (moderate) — Odd one out in data model concepts**

Which of these is *not* a property of a well-designed conformed dimension shared across government data models?

A) It has a single, agreed definition for each attribute
B) It is duplicated into each consuming team's model with local modifications allowed
C) It uses consistent keys so facts from different sources can be joined
D) It is version-controlled so consumers can track definitional change

**Correct answer: B.**

**Explanation:** A conformed dimension exists precisely so that different teams and organisations analyse against the *same* definitions and keys. Options A, C, and D describe that discipline: agreed attribute definitions, consistent keys enabling cross-source joins, and versioning so change is visible and managed. Option B describes the anti-pattern conformance eliminates — copy-and-diverge, where each team's "local modifications" quietly break comparability until two departments report different numbers for the same measure to the same minister. In your role you work across government and industry recognising opportunities for the reuse and alignment of data models in different organisations; the moment local modification is allowed on a shared dimension, alignment ends and reconciliation projects begin.

### Preparation tips

- **Rehearse with your own artefacts.** Take a real (suitably anonymised) data flow diagram or mapping document and quiz yourself: what breaks downstream if this node fails? What input value has no specified behaviour? This builds the exact muscles the assessment tests.
- **Practise bounded diagnosis.** For deduction questions, always ask "what does the *healthy* component tell me?" — evidence of what works eliminates hypotheses faster than staring at what is broken.
- **Time-box ruthlessly.** At 15–30 minutes total, a single stubborn question can consume a fifth of your test. Flag, skip, return. Adaptive tests reward steady accuracy over heroic struggles.
- **Verify options mechanically on logic puzzles.** As Question 12 demonstrated, plausible-looking options survive casual inspection; a quick written grid of constraints against options is faster than repeated mental re-checking, even under time pressure.
- **Read scope words like a reviewer.** "Any other", "exempt from rule 1", "at least" — the assessment hides answers in quantifiers and scopes, exactly as real standards documents do.
- **Do the ungraded warm-up.** Use the practice questions offered before the timed section to settle nerves and learn the interface — never skip them to "save energy".

### Common pitfalls

- **Answering from experience instead of the given scenario.** You know how *your* streaming platform behaves; the question defines its own world. Reason only from what is stated — a discipline the specs call fact-based logic, and one senior engineers ironically fail more often than juniors because they know too much.
- **Treating anomalous success as safe.** Green ticks lull candidates into deprioritising the one alert that matters, as in Question 9. Assessors deliberately test whether you can rank a quiet anomaly above a noisy but harmless failure.
- **Over-calculating.** Some pattern questions yield to a ratio check in ten seconds; candidates who reach for elaborate modelling waste minutes. Estimate first, calculate only if options are close.
- **Losing accuracy to speed panic.** Score reports separate speed from accuracy; a rushed wrong answer hurts more than a considered pass. Maintain your review discipline — you would not merge unreviewed code under deadline pressure, so do not submit unreviewed answers either.
- **Ignoring the format instructions.** If a question asks for the *most defensible order*, it is testing ranking judgement, not whether every task gets done — answer the question actually asked.


## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment evaluates your ability to analyse, interpret, and make sound decisions using numerical data of the kind your role genuinely produces: pipeline throughput tables, storage growth figures, error-rate percentages, team capacity plans, cloud cost breakdowns, and service performance metrics. The emphasis is business arithmetic — percentages, ratios, rates, proportions, and cost-benefit estimation — not abstract formulae or advanced mathematics.

The typical format is online and strictly timed, often around 60 to 90 seconds per question across 15 to 25 questions. An onscreen calculator is usually allowed or provided, because the test prioritises *interpretation* over mental arithmetic: the challenge is extracting the right numbers from a table or chart, choosing the right operation, and sanity-checking the result, all at pace. Question inputs are realistic artefacts — a monthly cost report, a data quality dashboard, a capacity forecast — and several questions may share one dataset.

For a lead data engineer, numeric fluency is not a nice-to-have. You manage resources to ensure data services work effectively at an enterprise level, which means defending budgets, forecasting storage and compute, and evidencing performance improvements with numbers. You review test results and data-profiling outputs where a misread percentage means a defect ships. You size streaming systems where the difference between linear and compound growth determines whether the platform survives the next quarter. And you communicate figures to non-technical stakeholders, which demands that you have the arithmetic solidly right before you simplify it. This assessment rehearses all of that under time pressure.

### What it measures for your role

- **Rates, throughput, and capacity arithmetic → Programming and build (data engineering) and your responsibility for data-streaming systems.** Events per second, records per batch, lag accumulation, and headroom calculations.
- **Percentages and data quality metrics → Data analysis and synthesis and Testing.** Profiling results ("2.4% of rows fail postcode validation"), test pass rates, defect densities, and completeness measures.
- **Budgets and unit costs → Data development process.** Managing resources at enterprise level: cost per terabyte, per environment, per team, and the trade-offs between them.
- **Ratios and proportional reasoning → Data integration design and Data modelling.** Source-to-target record ratios, deduplication rates, and conformance coverage across systems.
- **Trend interpretation → Data innovation and Problem management.** Reading growth curves to time tool adoption and to anticipate problems before they become incidents.

### Practice questions

An onscreen calculator is assumed. Show your own working, then compare it with the explanation.

**Question 1 (easy) — Data quality percentage**

A profiling run over a source extract of 1,250,000 records reports 18,750 records failing address validation. What is the failure rate?

A) 0.15%  B) 1.5%  C) 15%  D) 6.7%

**Correct answer: B.**

**Explanation:** Failure rate = failures ÷ total = 18,750 ÷ 1,250,000 = 0.015 = 1.5%. A quick sanity check protects you from the decimal-place traps in options A and C: 1% of 1,250,000 is 12,500, and 18,750 is between 12,500 (1%) and 25,000 (2%), so the answer must sit between 1% and 2%. Option D comes from dividing the wrong way round with a slip. Anchoring percentages to an easy reference (1% of the total) is the fastest error-check available under time pressure, and it is the same habit you apply when a profiling report lands and you need to judge instantly whether a failure rate is routine or alarming.

**Question 2 (easy) — Throughput headroom**

A streaming cluster is provisioned to handle 40,000 events per second. Current peak load is 29,000 events per second. What percentage headroom remains at peak, relative to provisioned capacity?

A) 11%  B) 27.5%  C) 37.9%  D) 72.5%

**Correct answer: B.**

**Explanation:** Headroom = (capacity − peak) ÷ capacity = (40,000 − 29,000) ÷ 40,000 = 11,000 ÷ 40,000 = 0.275 = 27.5%. Option C is the classic trap: dividing the spare 11,000 by the *current load* (11,000 ÷ 29,000 ≈ 37.9%) instead of by capacity — a different, also-legitimate metric ("we could grow 37.9% before saturating"), but not what was asked. Option D is utilisation, the complement of the answer. Option A quotes the absolute difference in thousands as a percentage. The lesson: headroom questions always hinge on *which base* the percentage uses, so read the phrase "relative to provisioned capacity" as an instruction, not decoration. In capacity reviews, stating the base explicitly is equally vital, because a stakeholder who hears "37.9% headroom" when you meant 27.5% will approve the wrong deferral of scaling work.

**Question 3 (moderate) — Storage growth projection**

Your conformed data platform holds 84 TB today and has grown 6% per month for the past year. Contractually, your storage tier is capped at 100 TB. Approximately how many months until you hit the cap if growth continues?

A) 2 months  B) 3 months  C) 4 months  D) 6 months

**Correct answer: B.**

**Explanation:** Compound the growth month by month: 84 × 1.06 = 89.04 TB after one month; 89.04 × 1.06 ≈ 94.38 TB after two; 94.38 × 1.06 ≈ 100.04 TB after three. The cap is reached in approximately 3 months. The trap in option C (and beyond) is linear thinking: 6% of 84 is about 5 TB, and 16 TB of gap ÷ 5 TB per month suggests just over 3 months — close here, but the linear shortcut increasingly understates compound growth over longer horizons, which is why option D exists to catch anyone who discounts the compounding entirely. As the engineer responsible for enterprise-level resource management, this calculation is the difference between a planned, procured storage expansion and an emergency change request; always test whether growth in your estate is additive or compound before extrapolating.

**Question 4 (moderate) — Cost per terabyte comparison**

Two ingestion patterns are costed for a new data flow. Pattern A (batch): fixed platform cost £2,400 per month plus £35 per TB processed. Pattern B (streaming): fixed platform cost £4,100 per month plus £18 per TB processed. At what monthly volume do the two patterns cost the same?

A) 50 TB  B) 85 TB  C) 100 TB  D) 120 TB

**Correct answer: C.**

**Explanation:** Set the cost equations equal: 2,400 + 35V = 4,100 + 18V. Subtract 18V from both sides: 2,400 + 17V = 4,100. Subtract 2,400: 17V = 1,700, so V = 100 TB. Below 100 TB per month, batch (Pattern A) is cheaper; above it, streaming (Pattern B) wins on its lower marginal rate. A fast verification: at 100 TB, A costs 2,400 + 3,500 = £5,900 and B costs 4,100 + 1,800 = £5,900 — equal, confirmed. Break-even analysis like this is exactly the evidence base you need when championing data engineering choices to budget holders: not "streaming is more modern", but "streaming becomes cheaper than batch at 100 TB per month, and we are forecast to pass that volume in Q3". Numbers first, advocacy second.

**Question 5 (moderate) — Deduplication ratio**

Three source systems contribute citizen records to a conformed model: System 1 provides 2.6 million records, System 2 provides 1.9 million, and System 3 provides 1.5 million. After matching and deduplication, the conformed model contains 4.2 million unique records. What percentage of the total input records were duplicates?

A) 30%  B) 25%  C) 43%  D) satisfies none of these

**Correct answer: A.**

**Explanation:** Total input = 2.6 + 1.9 + 1.5 = 6.0 million records. Unique output = 4.2 million, so duplicates removed = 6.0 − 4.2 = 1.8 million. Duplicate percentage = 1.8 ÷ 6.0 = 0.30 = 30%. Option C (43%) comes from dividing the duplicates by the *output* (1.8 ÷ 4.2) rather than the input — again a base error, the single most common numeric-reasoning mistake. A 30% overlap across three government source systems is a realistic figure, and in your data analysis and synthesis work it is exactly the kind of headline number you would report when justifying the conformed model: "three sources, six million rows, but only 4.2 million real people — a third of the estate was duplication."

**Question 6 (moderate) — Test pass rates across iterations**

An integration test suite has 480 test conditions. In iteration 1, 408 passed. In iteration 2, after fixes, 456 passed. By how many percentage points did the pass rate improve, and what is the iteration 2 pass rate?

A) 10 percentage points; 95%  B) 12 percentage points; 95%  C) 10 percentage points; 90%  D) 48 percentage points; 95%

**Correct answer: A.**

**Explanation:** Iteration 1 pass rate = 408 ÷ 480 = 0.85 = 85%. Iteration 2 pass rate = 456 ÷ 480 = 0.95 = 95%. Improvement = 95 − 85 = 10 percentage points. Option D confuses the raw count of newly passing tests (48) with percentage points. Note also the language discipline the question enforces: the pass rate improved by 10 *percentage points*, but by 10 ÷ 85 ≈ 11.8 *percent* relative — the two phrasings describe different quantities, and assessments (like ministers' briefing packs) punish conflating them. When you analyse and report test activities and results, precise phrasing of improvement figures is part of the craft: "pass rate up ten points to 95%" is unambiguous; "tests improved 10%" is not.

**Question 7 (hard) — Streaming lag accumulation**

A consumer processes 5,400 events per minute. During a peak window, producers write 6,150 events per minute to the topic for 40 minutes, after which the rate drops to 4,900 events per minute. How long after the peak ends will the consumer clear the accumulated backlog?

A) 30 minutes  B) 45 minutes  C) 60 minutes  D) 75 minutes

**Correct answer: C.**

**Explanation:** During the 40-minute peak, backlog accumulates at 6,150 − 5,400 = 750 events per minute, so total backlog = 750 × 40 = 30,000 events. After the peak, the consumer drains the backlog at 5,400 − 4,900 = 500 events per minute (its spare capacity over the new inflow). Time to clear = 30,000 ÷ 500 = 60 minutes. The common error is dividing the backlog by the full consumption rate (30,000 ÷ 5,400 ≈ 5.6 minutes — suspiciously absent from the options, which is itself a hint) while forgetting that new events keep arriving and consume most of the throughput. This fill-and-drain pattern is the fundamental arithmetic of the data-streaming systems you are responsible for building: recovery time depends on *net* drain rate, and if the post-peak inflow had been 5,400 or more, the backlog would never clear — the calculation that justifies scaling decisions.

**Question 8 (hard) — Budget reallocation with constraints**

Your annual platform budget is £960,000, currently split: compute 45%, storage 25%, licences 20%, training 10%. Next year the total budget falls by 5%, and the licence cost is contractually fixed at its current pound value. If training must retain at least £80,000, what is the maximum combined budget available for compute and storage next year?

A) £640,000  B) £649,600  C) £540,000  D) £720,000

**Correct answer: A.**

**Explanation:** Work in pounds throughout, and label each figure as fixed or proportional before touching the calculator. Current licences = 20% × £960,000 = £192,000, and this pound value is contractually fixed. Next year's total = £960,000 × 0.95 = £912,000. Subtract the fixed licences: £912,000 − £192,000 = £720,000 available for compute, storage, and training combined. Training must retain *at least* £80,000, so the maximum for compute and storage occurs when training takes exactly its £80,000 floor: £720,000 − £80,000 = £640,000. Option B (£649,600) is the result of wrongly cutting the "fixed" licence figure by 5% along with everything else (£192,000 × 0.95 = £182,400; £912,000 − £182,400 − £80,000 = £649,600) — the single most tempting error, because applying the reduction uniformly *feels* consistent. Option D forgets training entirely; option C applies the 5% cut twice. The professional lesson mirrors real budget defence: the fixed-versus-proportional distinction is exactly what finance colleagues probe, and a lead engineer who cuts a contractually fixed cost in a forecast will present a plan that is £9,600 more optimistic than reality — small enough to slip through review, large enough to hurt in March. Multi-step budget questions reward laying out every step in pounds with its fixed/variable label, then re-reading the constraint direction ("at least" versus "at most") before selecting.

**Question 9 (moderate) — Reading a cost table**

Monthly cloud costs for your four environments (in £ thousands):

| Environment | April | May | June |
|---|---|---|---|
| Production | 42.0 | 44.1 | 46.3 |
| Pre-production | 18.0 | 18.0 | 21.6 |
| Test | 9.5 | 11.4 | 13.7 |
| Development | 6.5 | 6.5 | 6.4 |

Which environment had the largest *percentage* increase from April to June?

A) Production  B) Pre-production  C) Test  D) Development

**Correct answer: C.**

**Explanation:** Compute each percentage change from April to June. Production: (46.3 − 42.0) ÷ 42.0 = 4.3 ÷ 42.0 ≈ 10.2%. Pre-production: (21.6 − 18.0) ÷ 18.0 = 3.6 ÷ 18.0 = 20%. Test: (13.7 − 9.5) ÷ 9.5 = 4.2 ÷ 9.5 ≈ 44.2%. Development: essentially flat (−1.5%). Test wins by a wide margin despite having the *smallest absolute* increase among the growing environments in pounds-per-month terms comparable to production's £4,300. The trap is answering Production because its absolute rise (£4,300 a month) is largest, or Pre-production because its June jump is visually sharp. Percentage change always needs the base. In cost reviews this distinction drives entirely different conversations: production's 10% growth is capacity-driven and expected; test's 44% growth in three months is the anomaly worth investigating — probably an environment someone scaled up for a performance test and never scaled down.

**Question 10 (moderate) — Team capacity allocation**

Your data engineering group has 5 engineers, each with 8 productive days per fortnight. In the next fortnight you must allocate: 12 engineer-days to the streaming build, 8 to standards and documentation, 6 to problem investigations, and 20% of total capacity held for unplanned support. How many engineer-days remain for discretionary innovation work?

A) 4  B) 6  C) 8  D) 14

**Correct answer: B.**

**Explanation:** Total capacity = 5 engineers × 8 days = 40 engineer-days. Unplanned support reserve = 20% × 40 = 8 days. Committed work = 12 + 8 + 6 = 26 days. Remaining = 40 − 8 − 26 = 6 engineer-days. Option C is the reserve figure itself; option D forgets the reserve entirely (40 − 26 = 14); option A subtracts the reserve twice. The realistic detail is the 20% support reserve — mature teams running enterprise data services always hold capacity for the unplannable, and a lead who allocates 100% of nominal capacity has actually planned for zero incidents, zero sick days, and zero surprises. Six days for innovation is also the honest answer to "can we prototype that new ingestion framework this sprint?" — which connects directly to your data innovation skill: identifying the right *timing* for adoption includes knowing when the capacity genuinely exists.

**Question 11 (hard) — Weighted data quality score**

Your data quality framework scores datasets on three dimensions: completeness (weight 50%), validity (weight 30%), and timeliness (weight 20%). A critical dataset scores 92% completeness, 85% validity, and 70% timeliness. The service standard requires a weighted score of at least 85%. Does the dataset meet the standard, and what is its weighted score?

A) Yes — 85.5%  B) No — 84.5%  C) No — 82.3%  D) Yes — 86.2%

**Correct answer: A.**

**Explanation:** Weighted score = (92 × 0.50) + (85 × 0.30) + (70 × 0.20) = 46.0 + 25.5 + 14.0 = 85.5%. That clears the 85% threshold — just. Option B is the result of swapping the validity and timeliness weights (92 × 0.5 + 85 × 0.2 + 70 × 0.3 = 46 + 17 + 21 = 84.0, or nearby variants), which flips the pass into a fail; a reminder that weight-to-dimension pairing deserves a deliberate check, since transposition errors are invisible in a calculator history. The simple average (82.3%, option C) ignores the weights altogether. Two professional observations follow: first, a dataset passing at 85.5% with timeliness at 70% is fragile — one late feed drops it below standard, so the pass should trigger attention, not complacency; second, when you design quality frameworks (part of establishing data integration standards), the weights *are* policy — choosing 50/30/20 encodes a judgement that missing data hurts users more than late data, and you should be able to defend that judgement to stakeholders.

**Question 12 (moderate) — Ratio reasoning across sources**

A conformed reference dataset is assembled from two systems in the ratio 5:3 (System P : System Q). System Q contributes 240,000 records. How many records does the conformed dataset contain in total, assuming no overlap?

A) 400,000  B) 640,000  C) 384,000  D) 540,000

**Correct answer: B.**

**Explanation:** The ratio 5:3 means System Q's contribution represents 3 parts. One part = 240,000 ÷ 3 = 80,000 records. System P contributes 5 parts = 400,000 records. Total = 400,000 + 240,000 = 640,000 records (or 8 parts × 80,000). Option A stops at System P's contribution and forgets to add Q back in — the most common slip in ratio questions: answering an intermediate value because it appears among the options. Option C multiplies 240,000 by 8/5 instead of 8/3. The reliable technique is to convert the ratio into a concrete "size of one part" as the very first step, then scale — it turns every subsequent step into simple multiplication and gives you a built-in sanity check (all parts must sum to the total). Ratio fluency matters whenever you plan conformed models: contribution ratios drive matching workloads, storage sizing, and where your data-profiling effort should concentrate.

**Question 13 (hard) — Interpreting a performance improvement claim**

A supplier claims their new ingestion engine "reduces processing time by 60%". Your current nightly batch takes 7 hours 30 minutes. Separately, your own team's optimisation backlog is estimated to cut the current time by 90 minutes. If both claims are accurate and the supplier's percentage applies to the time *after* your team's optimisation, what would the final nightly runtime be?

A) 3 hours 00 minutes  B) 2 hours 24 minutes  C) 1 hour 48 minutes  D) 3 hours 36 minutes

**Correct answer: B.**

**Explanation:** Sequence matters. Current runtime = 7.5 hours. Your team's optimisation first: 7.5 hours − 1.5 hours = 6.0 hours. Then the supplier's 60% reduction applies to that 6.0 hours: reduction = 3.6 hours, leaving 6.0 × 0.40 = 2.4 hours = 2 hours 24 minutes. Option A applies the 60% to the original 7.5 hours (7.5 × 0.4 = 3.0) and ignores the sequencing instruction. Option C subtracts the 90 minutes *after* applying 60% to the original (3.0 − 1.5 + slippage variants). The general rule: percentage reductions are multiplicative and order-sensitive when mixed with absolute reductions — "60% off then 90 minutes off" differs from "90 minutes off then 60% off". Professionally, this is also a procurement-literacy question: supplier performance claims routinely leave the *base* ambiguous, and the lead engineer's job — part innovation appraisal, part communicating between technical and non-technical — is to pin down "60% of what, measured how, from which baseline?" before the figure reaches a business case.

**Question 14 (easy) — Unit conversion under time pressure**

A pipeline processes a steady 1,800 records per second. Approximately how many records does it process in a 6-hour overnight window?

A) 6.5 million  B) 10.8 million  C) 38.9 million  D) 64.8 million

**Correct answer: C.**

**Explanation:** Convert stepwise and keep the units visible: 1,800 records per second × 60 = 108,000 per minute; × 60 again = 6,480,000 per hour; × 6 hours = 38,880,000 ≈ 38.9 million records. Option A stops at roughly the per-hour figure with a decimal slip; option B multiplies by 60 once and then by 6 hours, silently treating minutes as hours — the classic missed conversion step; option D multiplies by an extra factor of 10/6. The defence is mechanical: write the unit next to every intermediate number ("6.48M *per hour*") so a skipped step announces itself. Throughput-over-window arithmetic is among the most common calculations in your working life — sizing batch windows, estimating backfill durations, checking whether a reprocessing job can finish before the morning load — and it is also among the most common places for an order-of-magnitude slip to survive into a capacity plan, precisely because every individual multiplication is trivial.

**Question 15 (moderate) — Percentage of a percentage**

Profiling shows that 12% of records in a source extract have at least one data quality issue. Of those flawed records, 25% have issues serious enough to reject; the rest can be auto-corrected. If the extract contains 3.4 million records, how many will be rejected?

A) 850,000  B) 408,000  C) 102,000  D) 306,000

**Correct answer: C.**

**Explanation:** Chain the percentages: flawed records = 12% × 3,400,000 = 408,000. Rejected records = 25% of the *flawed* records = 0.25 × 408,000 = 102,000. Equivalently, 12% × 25% = 3% of the whole extract, and 3% × 3.4 million = 102,000 — the one-step check that confirms the answer. Option A applies 25% to the whole extract; option B stops at the intermediate value (all flawed records); option D takes 9% (12% − 3%) of the extract. Nested percentages appear constantly in data quality reporting — "x% of records have issues, y% of those are critical" — and the reliable technique is to decide, for every percentage you meet, *of which population* it is a percentage before multiplying anything. It is the same base-discipline as earlier questions, applied twice in sequence, and it is exactly how you would brief a data quality summary to a non-technical stakeholder: "three in every hundred records will be rejected" is the version the meeting remembers.

### Preparation tips

- **Rebuild your reference fractions.** Knowing instantly that 1/8 = 12.5%, 1/3 ≈ 33%, 3/8 = 37.5% lets you sanity-check options before calculating. Ten minutes of revision pays for itself in the first five questions.
- **Anchor every percentage to its base.** Before computing, say silently "percent *of what*". The majority of wrong options in numeric tests are correct calculations on the wrong base — utilisation versus headroom, input versus output, original versus revised.
- **Practise with your own dashboards.** Take a real capacity report or cost export and ask: which environment grew fastest proportionally? When do we hit the cap at current compound growth? The formats you will see in the test are the ones you already own.
- **Write intermediate values down.** Multi-step questions (budget, then fixed costs, then reserve) collapse if you hold three numbers in your head. The onscreen calculator has no memory of your reasoning — your note paper is the audit trail.
- **Estimate before you calculate.** A rough order-of-magnitude guess catches decimal slips instantly, and sometimes the estimate alone eliminates three options.
- **Keep moving.** With roughly a minute per question, a stuck question costs you two easy ones. Flag it, bank the accessible marks, return if time allows.

### Common pitfalls

- **Misreading scale qualifiers.** Tables headed "£ thousands" or "events per minute" versus "per second" are the most reliable trap in the genre. Read units and captions before reading numbers — always.
- **Confusing percentage points with percent.** A pass rate rising from 85% to 95% is up ten points but 11.8 percent relative. Assessments test the distinction; so do finance colleagues.
- **Linear extrapolation of compound growth.** As in the storage question, straight-line thinking understates exponential trends — the same error that under-provisions streaming platforms.
- **Answering the intermediate value.** Test writers place your half-way result among the options (System P's 400,000; the 8-day reserve). Finishing the question means re-reading what was actually asked before selecting.
- **Over-calculating.** If two options differ by an order of magnitude, an estimate settles it; only calculate precisely when options are close.
- **Time-sink questions.** One stubborn multi-stage calculation can wreck an otherwise strong sitting. Senior candidates are especially prone to refusing to let a question win; in a timed test, strategic surrender is a skill.


## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment evaluates how well you understand, analyse, and draw correct conclusions from written material of the kind your role deals in daily: data integration standards, government data strategies, architecture decision records, supplier contracts, incident reports, and emails from stakeholders ranging from junior engineers to directors. Passages use genuine professional register and terminology; the questions test whether you can separate what a text *actually states* from what it merely implies, and both of those from what you happen to know or believe.

The classic format presents a dense passage followed by statements you must judge **True** (the passage states or logically entails it), **False** (the passage contradicts it), or **Cannot Say** (the passage provides insufficient information either way). Multiple-choice comprehension questions — best summary, author's main point, correct application of a stated rule — are usually mixed in. Timing is tight, often under a minute per question, deliberately simulating the pace at which you skim a policy paper before a meeting.

The cardinal rule is *fact-based logic*: answer strictly from the text provided, ignoring outside knowledge. For senior specialists this is genuinely harder than it sounds — you know how metadata repositories usually work, so when a passage describes one that works differently, your expertise becomes a liability unless you consciously set it aside.

Why it matters for your role: you establish standards and ensure adherence to them, which requires reading (and writing) documents whose precise wording carries obligations. You support or host difficult discussions with diverse senior stakeholders, where misreading a briefing or an email escalates rather than resolves. You keep abreast of best practice across industry and government, which means efficiently extracting the load-bearing claims from long publications. And you review specifications where the difference between "must", "should", and "may" determines what your teams build.

### What it measures for your role

- **Precise comprehension of standards and policies → Data integration design and Data development process.** Reading scope clauses, exemptions, and obligations exactly as written — the skill exercised every time you update a standard or audit adherence.
- **Interpreting stakeholder needs from text → Communicating between the technical and non-technical.** Emails and briefings rarely say precisely what stakeholders mean; the assessment tests whether you can identify what a text supports, and hold back from assuming the rest.
- **Reviewing specifications → Testing and Programming and build.** Deciding whether a statement about behaviour is entailed by a specification is literally the True/False/Cannot Say task in engineering costume.
- **Synthesising documentation → Metadata management and Data modelling.** Identifying the core claim of a passage mirrors writing definitions and repository descriptions that others must not misread.
- **Evaluating claims about tools → Data innovation.** Vendor whitepapers and blog posts mix fact, projection, and marketing; the assessment's discipline of separating stated fact from implication is your primary defence.

### Practice questions

For each passage, judge the statements strictly on the text. Resist expertise; trust wording.

**Passage 1 — Extract from a draft cross-government data sharing standard**

"Departments exchanging personal data must record each exchange in the departmental data sharing register within five working days. Where an exchange is repeated on a fixed schedule, a single register entry covering the schedule is sufficient, provided the entry is reviewed annually. Exchanges of fully anonymised data are exempt from registration but must still comply with departmental security classification policy. Pseudonymised data is treated as personal data for the purposes of this standard."

**Question 1 (easy).** True, False, or Cannot Say: "Under the draft standard, a weekly scheduled exchange of personal data requires a new register entry every week."

**Correct answer: False.**

**Explanation:** The passage directly addresses this case: "Where an exchange is repeated on a fixed schedule, a single register entry covering the schedule is sufficient, provided the entry is reviewed annually." A weekly exchange on a fixed schedule therefore requires one entry plus annual review, not a weekly entry. The statement contradicts the text, so it is False rather than Cannot Say. Notice the discipline: you are not asked whether weekly entries would be *good practice*, only what the standard requires — a distinction you apply whenever you audit teams' adherence to your integration procedures.

**Question 2 (moderate).** True, False, or Cannot Say: "Exchanging pseudonymised data on an ad hoc basis must be recorded in the register within five working days."

**Correct answer: True.**

**Explanation:** Chain two stated rules. First, "Pseudonymised data is treated as personal data for the purposes of this standard." Second, personal data exchanges "must record each exchange in the departmental data sharing register within five working days." An ad hoc (non-scheduled) pseudonymised exchange therefore inherits the five-day registration obligation. The scheduled-exchange concession does not apply because the exchange is ad hoc. This is entailment across two sentences — the passage never says the conclusion in one place, but the conclusion follows necessarily. Verbal tests at senior level lean heavily on such two-step chains, exactly as real standards do: obligations often attach through a definitional clause several paragraphs from the operative one.

**Question 3 (moderate).** True, False, or Cannot Say: "Fully anonymised data may be exchanged without any restrictions."

**Correct answer: False.**

**Explanation:** The passage exempts anonymised data from *registration* but immediately adds that it "must still comply with departmental security classification policy". "Without any restrictions" is therefore contradicted: at least one restriction (classification policy) survives. The trap is reading "exempt from registration" and generalising it to "exempt from everything" — the same over-extension of scope that Question 10 in the cognitive section punished. In your standards work, exemption scope is where most compliance disputes start; in verbal tests, it is where most False answers hide, dressed as True.

**Question 4 (hard).** True, False, or Cannot Say: "The five-working-day deadline was introduced because departments were recording exchanges too slowly."

**Correct answer: Cannot Say.**

**Explanation:** The passage states the deadline but gives no rationale whatsoever — nothing about why five days, what problem it addresses, or its history. The explanation you instinctively supplied ("presumably to stop slow recording") is plausible inference from professional experience, which is precisely what the test excludes. Cannot Say is correct whenever the passage neither states nor entails the claim, however reasonable it sounds. Senior candidates lose more marks to plausible-but-unstated rationales than to any other error, because supplying rationale is what experienced people do automatically when they read policy. In the test, notice the urge — then answer from the text alone.

**Passage 2 — Email from a director to the data engineering leadership group**

"Colleagues — the Spending Review outcome means our data platform programme will receive funding for two of the three planned workstreams next year. The analytics migration and the real-time integration workstreams both scored well in the prioritisation exercise; the metadata modernisation workstream will be paused rather than cancelled, and its business case should be refreshed for the following year. I would like the leadership group's view on sequencing by Friday. Please note that pausing metadata modernisation must not be communicated to suppliers before the commercial team completes the contract review."

**Question 5 (easy).** True, False, or Cannot Say: "The metadata modernisation workstream has been cancelled."

**Correct answer: False.**

**Explanation:** The email states it "will be paused rather than cancelled" — a direct contradiction of the statement. The phrase "rather than" is doing precise work: it explicitly rules out the stronger claim. Easy marks in verbal tests come from statements the passage addresses head-on; bank them quickly to buy time for the harder inferential items. There is also a professional echo here: when you cascade this kind of message to your teams, preserving exactly this distinction — paused, not cancelled — is what keeps morale and supplier relationships intact.

**Question 6 (moderate).** True, False, or Cannot Say: "The analytics migration workstream will receive funding next year."

**Correct answer: Cannot Say — but examine the reasoning carefully.**

**Explanation:** This one divides strong candidates, and working through it sharpens exactly the skill the test rewards. The email says funding covers "two of the three planned workstreams", that analytics migration and real-time integration "both scored well", and that metadata modernisation "will be paused". If exactly two are funded and metadata modernisation is the paused one, the remaining two — including analytics migration — are funded, making the statement look True by elimination. The hesitation: does "paused" *entail* "unfunded", and does "funding for two workstreams" *entail* those two are exactly the non-paused ones? The email strongly implies this mapping but never states it — strictly, the pause could be for non-funding reasons and the funded pair is never named. Under the strictest reading, Cannot Say; under ordinary entailment, True. Real assessments avoid publishing questions this borderline, but you will meet items near the line, and the practical guidance is: when a conclusion requires an unstated bridging assumption (however natural), the test expects Cannot Say. Where the chain uses only stated definitional links, as in Question 2, the answer is True. Learn to feel that difference — it is the whole game.

**Question 7 (moderate).** True, False, or Cannot Say: "Suppliers must not be told about the pause until the commercial team has finished reviewing the contracts."

**Correct answer: True.**

**Explanation:** The final sentence states: "pausing metadata modernisation must not be communicated to suppliers before the commercial team completes the contract review." The statement is a faithful paraphrase — "told about the pause" matches "communicated to suppliers", and "until the review is finished" matches "before the commercial team completes the contract review". Verbal tests routinely reword the text to check you are matching *meaning* rather than string-matching words; the skill is confirming that each element of the paraphrase maps onto an element of the original with no addition or loss. Nothing has been added (no reason for the embargo, no consequences) and nothing lost, so True. Handling embargoed information correctly is also, of course, a live professional obligation for anyone hosting difficult conversations across teams and suppliers.

**Passage 3 — Extract from an incident review report**

"On 14 May, the overnight conformed load completed with a record volume 38% above the trailing average. Investigation established that an upstream source system had re-sent a full historical extract following its own database restore, and the pipeline's deduplication step, which matches on a composite key of citizen identifier and event date, did not exclude the re-sent records because the restore had regenerated event timestamps. Downstream BI reports overstated activity for six hours until the load was rolled back. The review recommends extending the composite key to include the source transaction identifier, and adding an automated volume-anomaly gate that pauses loads deviating more than 15% from the trailing average pending engineer approval."

**Question 8 (easy).** True, False, or Cannot Say: "The deduplication step failed because the composite key did not include the source transaction identifier."

**Correct answer: Cannot Say — read closely; the passage supports a related but different claim.**

**Explanation:** Careful. The passage states the deduplication failed "because the restore had regenerated event timestamps", and separately *recommends* extending the key to include the transaction identifier. That recommendation implies the extended key would have prevented the failure, but the passage attributes the *cause* to regenerated timestamps interacting with the existing key — it does not state that the absence of the transaction identifier was the cause. The statement fuses a stated cause with a stated recommendation into a causal claim the text never quite makes. If your instinct said True, you performed a sensible engineering synthesis — and exceeded the text, which is the one thing this test format forbids. Strictly: Cannot Say.

**Question 9 (moderate).** True, False, or Cannot Say: "Under the recommended volume-anomaly gate, the 14 May load would have been paused for engineer approval."

**Correct answer: True.**

**Explanation:** The recommended gate "pauses loads deviating more than 15% from the trailing average pending engineer approval". The 14 May load was "38% above the trailing average", and 38% exceeds 15%. Applying the stated rule to the stated fact yields the conclusion by straightforward entailment — no bridging assumption required, unlike Question 8. This pairing is deliberate: two questions on one passage, one requiring you to *refuse* an inference and one requiring you to *make* one. The dividing line is whether every step of the chain is in the text. Rule application questions like this one also mirror your testing skill directly: given a specification (the gate) and a test input (the 38% deviation), determine the specified output (pause and await approval).

**Question 10 (moderate) — Multiple choice.** Which of the following best summarises the incident review passage?

A) A source system database restore caused a data breach that took six hours to contain
B) A re-sent historical extract evaded deduplication due to regenerated timestamps, briefly distorting BI reports, prompting recommendations to strengthen the matching key and add a volume-anomaly gate
C) The pipeline's deduplication step is fundamentally flawed and must be redesigned
D) BI reports overstated activity because the trailing average was calculated incorrectly

**Correct answer: B.**

**Explanation:** Option B captures every load-bearing element: cause (re-sent extract, regenerated timestamps defeating the composite key), impact (BI reports briefly overstated), and both recommendations (extended key, anomaly gate). Option A substitutes "data breach" — a security event the passage never describes; overstated reports are an accuracy incident, not a breach, and precision with such terms matters enormously in government reporting. Option C inflates a targeted recommendation ("extend the composite key") into "fundamentally flawed and must be redesigned", exaggerating tone as well as content. Option D invents a cause the passage contradicts — the trailing average was the *detection* reference, not the failure. Best-summary questions reward the option that is complete, proportionate, and adds nothing; the wrong options are usually distortions of emphasis rather than outright fabrications, so compare each candidate summary clause-by-clause against the text.

**Passage 4 — Extract from a vendor whitepaper being evaluated by your team**

"StreamForge 4 delivers up to 3x ingestion throughput compared with StreamForge 3 in vendor benchmark conditions. Early adopters in the financial services sector report material reductions in pipeline latency. StreamForge 4's schema registry is expected to achieve certification against the open interoperability profile in the next release. Organisations running StreamForge 3 should note that extended support ends in eighteen months."

**Question 11 (moderate).** True, False, or Cannot Say: "StreamForge 4's schema registry is certified against the open interoperability profile."

**Correct answer: False.**

**Explanation:** The passage says certification "is expected... in the next release" — that is, it has not happened. The statement asserts present certification, which the text's own framing contradicts: something expected in a future release is by implication not true of the current one. Vendor prose is engineered to leave exactly this impression, which is why the question matters beyond the test: "expected", "up to 3x", and "in vendor benchmark conditions" are all hedges that convert marketing claims into technically-true-but-weak statements. Your data innovation responsibility — identifying areas of innovation and the appropriate timing for adoption — depends on decoding such hedges: an uncertified registry with certification "expected" is a roadmap item, not a capability, and adoption timing should treat it as such.

**Question 12 (hard).** True, False, or Cannot Say: "Organisations migrating from StreamForge 3 to StreamForge 4 will experience a threefold increase in ingestion throughput."

**Correct answer: Cannot Say.**

**Explanation:** Three hedges separate the passage's claim from the statement. First, "up to 3x" is a ceiling, not a typical value — any improvement from 1.01x to 3x is consistent with it. Second, the figure was obtained "in vendor benchmark conditions", and the passage says nothing about performance in any real deployment. Third, the statement generalises to all migrating organisations ("will experience"), which even a strong benchmark could not support. The passage neither states the claim (so not True) nor contradicts it (a 3x improvement remains possible — so not False): Cannot Say. This is arguably the most professionally valuable question in this section, because translating "up to 3x in vendor benchmarks" into "unknown, to be validated in our environment" is precisely the discipline you apply — and teach your teams to apply — before any business case cites a supplier's number.

**Question 13 (moderate).** True, False, or Cannot Say: "Organisations currently running StreamForge 3 will lose extended support within two years."

**Correct answer: True.**

**Explanation:** The passage states extended support for StreamForge 3 "ends in eighteen months". Eighteen months is within two years, so the statement is entailed — a weaker claim implied by a stronger stated fact. Note the direction: a passage stating "eighteen months" makes a "within two years" claim True, but a "within one year" claim False, and a "within exactly eighteen months of the whitepaper's publication date" claim True only if you trust the document's own timeline, which the question format tells you to do. Entailment from stronger to weaker claims (eighteen months → within two years) is valid; the reverse (within two years → eighteen months) is not. Candidates who miss this question usually do so by overthinking — suspecting a trap where the arithmetic of entailment is genuinely simple.

**Passage 5 — Extract from a departmental architecture decision record**

"Decision: the citizen events integration will adopt the streaming pattern rather than nightly batch. Rationale: three consuming services require data freshness of under one hour, which batch cannot provide. Consequences: the team must acquire streaming operations skills before go-live; the existing batch flow will run in parallel for one quarter as a reconciliation reference, after which it will be decommissioned unless reconciliation reveals material discrepancies. This decision supersedes ADR-014. It does not apply to the archival extract, which remains batch."

**Question 14 (easy).** True, False, or Cannot Say: "The existing batch flow will be decommissioned at the end of the parallel-run quarter."

**Correct answer: Cannot Say.**

**Explanation:** The passage attaches a condition: decommissioning happens "unless reconciliation reveals material discrepancies". Whether it *will* be decommissioned therefore depends on an outcome the passage cannot know in advance. The statement asserts the unconditional version of a conditional plan — not contradicted (decommissioning is the expected path), but not entailed either, so Cannot Say. Conditional language ("unless", "provided that", "subject to") converts confident-sounding plans into contingent ones, and assessments — like architecture decision records themselves — reward readers who notice. If the statement had read "the batch flow is *planned* to be decommissioned after the parallel run", it would be True; the single word "will" is what moves it. That is the level of wording sensitivity this format demands, and it is the same sensitivity you apply when writing decision records your successors will read as commitments.

**Question 15 (moderate).** True, False, or Cannot Say: "All of the department's data flows must now use the streaming pattern."

**Correct answer: False.**

**Explanation:** Two elements of the passage contradict the statement's universal claim. First, the decision concerns "the citizen events integration" — one named flow, not the estate. Second, the passage explicitly carves out an exception: "It does not apply to the archival extract, which remains batch." A statement beginning "all" is False the moment the text names even one exception, and this passage does so in terms. The trap is momentum reading: a confident decision in favour of streaming, plus a rationale about freshness, *feels* like a general policy, and candidates who skim endorse the generalisation. Scope discipline — what exactly does this decision cover? — is the same skill you exercise when applying integration standards: a rule's authority extends precisely as far as its stated scope, in assessments, in ADRs, and in the standards you yourself establish and maintain.

**Question 16 (moderate) — Multiple choice.** According to the architecture decision record in Passage 5, why was the streaming pattern chosen?

A) Because the team wanted to develop streaming operations skills
B) Because three consuming services need data fresher than nightly batch can deliver
C) Because ADR-014 recommended it
D) Because the batch flow had revealed material discrepancies

**Correct answer: B.**

**Explanation:** The rationale is stated in one sentence: "three consuming services require data freshness of under one hour, which batch cannot provide." Option B paraphrases it faithfully. The other options each recycle genuine passage content in a false causal role — a favourite construction in comprehension questions. Option A inverts a *consequence* ("the team must acquire streaming operations skills") into a motive; the skills need is a cost of the decision, not its reason. Option C misreads "supersedes ADR-014": the new decision *replaces* the earlier record, which tells you nothing about what ADR-014 recommended. Option D borrows the reconciliation language from the decommissioning condition — a hypothetical future test, not a past finding. The technique for "why" questions: locate the passage's own rationale marker (here, literally the word "Rationale:") and match options against it, rejecting any option built from material that appears elsewhere in the text under a different logical role. Decision records separate rationale from consequences deliberately — reading them accurately is a prerequisite for writing them well, and you write them often.

### Preparation tips

- **Read the statement first, then hunt in the passage.** With under a minute per question, scanning for the relevant clause beats reading the whole passage cold. You already skim standards documents this way; make it deliberate.
- **Rehearse the three verdicts as tests.** True = "the text states or strictly entails this". False = "the text contradicts this". Cannot Say = "neither". Before answering, name which test the statement passes — verbalising the criterion suppresses instinct.
- **Watch modality and hedges.** "Must" versus "should", "is" versus "is expected to", "up to" versus "typically" — the answer usually lives inside these small words, in tests as in supplier contracts and standards.
- **Quarantine your expertise.** Before each passage, remind yourself: this describes its own world. Your knowledge of how streaming platforms or sharing agreements really work is inadmissible evidence.
- **Practise on your genuine reading diet.** Take a paragraph from a data strategy or an architecture decision record and write three statements — one True, one False, one Cannot Say. Composing items teaches the distinctions faster than answering them.
- **Bank direct-statement questions fast.** Items answered by one explicit sentence (like the "paused rather than cancelled" question) are your time reserve for the inference-heavy ones.

### Common pitfalls

- **Importing outside knowledge.** The senior specialist's signature error: filling gaps with what is *usually* true. Every "presumably" in your head is a Cannot Say the test will score as wrong if you answer True.
- **Confusing implication with entailment.** A recommendation implies a diagnosis; marketing "expected" implies progress; neither *states* it. If the conclusion needs a bridging assumption, however natural, the answer is Cannot Say.
- **Over-extending exemptions and scopes.** "Exempt from registration" is not "exempt from everything". Scope words are where False answers dress up as True.
- **Confusing a likely outcome with a stated fact.** "Early adopters report material reductions" does not mean you will see them; treating probable as certain is the pitfall the specs single out.
- **Reading the passage first, exhaustively.** Time evaporates. Statement first, targeted scan second, full read only if the item genuinely spans the passage.
- **Second-guessing simple entailments.** Eighteen months is within two years. Not every question is a trap; calibrated confidence beats defensive overthinking.


## Workplace job-specific situational judgement assessment

### About this assessment

A workplace job-specific situational judgement assessment evaluates your decision-making, interpersonal effectiveness, and professional conduct through realistic workplace dilemmas. Unlike the cognitive, numeric, and verbal assessments, there is no purely objective right answer: several responses to each scenario may seem reasonable, and the task is to identify which best fits the role's responsibilities and the organisation's values. For a UK government lead data engineer, those values are well documented: putting user needs first, transparency, collaboration across departmental boundaries, accessibility and inclusion, evidence-based decision-making, and the responsible stewardship of public money and citizens' data.

Formats vary. The most common asks you to pick the **most effective** and **least effective** of four or five possible actions; others ask you to rank all options from best to worst, or rate each on a scale. Timing is usually generous or absent — the test is interested in your natural judgement, not your speed. Scenarios at your level involve the stakeholders you really face: your engineering teams, peer leads in other departments, architects, delivery managers, information governance colleagues, suppliers, and senior civil servants who need technical reality translated into decision-ready language.

The scenarios are calibrated to leadership: they probe how you balance delivery pressure against engineering standards, how you handle conflict between teams you coordinate, when you escalate versus absorb, how you develop people rather than simply directing them, and how you champion good data engineering practice across government without alienating the people you need to persuade. Your role profile makes you responsible for coordinating teams, setting best practice and standards, managing expectations of technical and non-technical stakeholders, and supporting or hosting difficult discussions — the assessment is a rehearsal room for exactly those duties.

### What it measures for your role

- **Stakeholder communication and expectation management → Communicating between the technical and non-technical.** Scenarios where a senior stakeholder wants an impossible date, misunderstands a risk, or receives bad news late.
- **Team coordination and standards leadership → Data development process and Data integration design.** Dilemmas about teams cutting corners, standards being resisted, or best practice needing to spread without heavy-handedness.
- **Incident and problem leadership → Problem management and Testing.** Choices about escalation, communication during incidents, root-cause discipline versus quick fixes, and preventing recurrence.
- **Cross-government influence → your duty to champion data engineering and Data modelling reuse.** Situations involving other departments' teams, shared standards, and reuse opportunities where you have influence but no authority.
- **Judgement about innovation and risk → Data innovation.** Weighing a promising new tool against operational stability, procurement rules, and team capacity.

### Practice questions

For each scenario, decide your answer before reading the analysis. There is rarely a perfect option — the skill is comparative judgement.

**Question 1 (moderate) — The deadline versus the failing tests**

Your team is due to promote a new cross-departmental data flow to production on Friday, publicly committed to the programme board. On Wednesday, integration testing reveals that 3% of records fail referential integrity checks against the target conformed model. The delivery manager suggests going live anyway and fixing the failures "in flight", noting the failures affect only one downstream report. Choose the MOST effective and LEAST effective actions.

A) Agree to go live as planned; 97% success is acceptable and the board commitment matters most
B) Postpone the go-live unilaterally and inform the programme board that testing has failed
C) Quantify the impact of the 3% (which records, which users, which decisions rely on the affected report), define a remediation path, and present the board with a clear recommendation and options before Friday
D) Go live but quietly exclude the failing 3% of records from the load, planning to add them later without telling downstream consumers
E) Ask the test team to relax the referential integrity checks so the load passes

**Most effective: C. Least effective: E (with D a close second-worst).**

**Explanation:** Option C does what leadership at your level requires: turn a technical signal into decision-ready information, preserve the board's ability to make an informed choice, and bring options rather than problems. It is transparent, evidence-based, and keeps the user impact — not the milestone — at the centre. Option B has the right instinct (don't ship known-bad data) but exercises it poorly: unilateral postponement without analysis or options undermines the collaborative governance a programme board exists to provide, and "testing has failed" without quantification invites panic. Option A subordinates data integrity to reputation management and plants a known defect in a cross-departmental flow. Option D is worse: silently excluding records makes the report *silently* wrong and betrays downstream consumers' trust — transparency is a core public sector value precisely because others build decisions on your data. Option E is the least effective of all: it does not even accept the defect knowingly, it *destroys the instrument that detected it*, corrupting every future run's assurance. Weakening a control to pass a test is the data engineering equivalent of disconnecting a fire alarm. In "most/least" scoring, E-style options — those that damage systemic safeguards rather than merely making one bad call — are almost always the intended "least effective".

**Question 2 (moderate) — The resistant team and your new standard**

You have established a new metadata registration standard: every new dataset must be registered in the enterprise repository with defined ownership and sensitivity classification before first production load. One of the four teams you coordinate has ignored the standard for its last three datasets, and its team lead tells you privately: "The repository tooling doubles our lead time. We'll register things once the tooling improves." Choose the MOST effective and LEAST effective actions.

A) Escalate the non-compliance to the head of data engineering, recommending the team's releases be blocked until they comply
B) Sit down with the team to time their registration workflow end-to-end, fix or streamline the genuine tooling friction, agree a realistic compliance date, and make registration of the three missing datasets part of that plan
C) Grant the team a formal exemption from the standard until the tooling improves
D) Re-announce the standard to all four teams by email, emphasising it is mandatory
E) Quietly register the three datasets yourself so the repository is complete

**Most effective: B. Least effective: E.**

**Explanation:** Standards leadership at enterprise scale lives or dies on this scenario. Option B treats the resistance as information: the team has told you the standard's *cost* is too high, and the leader who investigates that claim — measuring the actual friction, fixing the tooling, agreeing a dated path back to compliance — gets both adherence and a better standard. This matches your role profile exactly: establish standards, keep them up to date, and ensure adherence — the middle clause is the one weak leaders skip. Option A may eventually be necessary, but as a first move it spends escalation capital and converts a solvable tooling problem into an interpersonal one; SJT scoring consistently penalises premature escalation. Option C rewards non-compliance with an exemption and signals to the other three teams that ignoring the standard is the cheapest route to relief. Option D is activity masquerading as action — the team already knows the standard is mandatory; repetition without addressing the friction changes nothing and slightly humiliates the compliant teams. Option E is least effective: it removes the symptom while entrenching the disease, teaches the team that non-compliance transfers work to you, does not scale across four teams, and leaves ownership and classification decisions — which genuinely require the owning team's knowledge — to someone one step removed from the data. Least-effective answers are often the *most helpful-looking* option that quietly destroys accountability.

**Question 3 (hard) — The minister's dashboard and the honest number**

A director asks you to confirm, by end of day, that the new benefits-processing dashboard can be described to the minister's office as "real-time". You know the underlying streaming pipeline delivers events with a median latency of 40 seconds, but a known failure mode — which occurred twice last month — can delay data by up to four hours until an engineer intervenes. Choose the MOST effective and LEAST effective actions.

A) Confirm "real-time", since 40 seconds median is real-time by any practical definition
B) Reply that the dashboard is "near-real-time under normal operation, typically under a minute, with a known failure mode that can delay data by up to four hours" and offer a one-paragraph plain-English description plus the remediation plan and timescale for the failure mode
C) Refuse to endorse any description until the failure mode is fixed
D) Confirm "real-time" but log your concerns about the failure mode in the risk register
E) Tell the director the question should be answered by the platform supplier

**Most effective: B. Least effective: A (with D close behind).**

**Explanation:** This scenario tests the heart of communicating between the technical and non-technical: giving decision-makers the *usable truth*. Option B translates engineering reality into plain language a minister's office can safely repeat, includes the caveat that matters (the four-hour tail, not the 40-second median), and pairs the bad news with a remediation plan — expectation management done properly. Option A is least effective because the omission is foreseeable and consequential: the description will be repeated publicly, the failure mode has occurred twice in a month, and when data next goes stale for four hours the minister's office will have made a false statement traceable to your confirmation. In government, the cost of an over-claim is measured in trust, and trust is the currency your championing of data engineering across government spends. Option D is barely better — logging a risk you simultaneously helped conceal is self-protection, not transparency, and assessors specifically look for candidates who avoid "cover yourself while enabling the harm" patterns. Option C mistakes perfectionism for integrity: services with known failure modes can be described honestly (that is what option B does); refusing all description leaves the director uninformed and invites someone less scrupulous to answer instead. Option E abdicates: the supplier neither knows the operational history nor owes the minister candour — you do.

**Question 4 (moderate) — The duplicate pipelines discovered mid-flight**

While reviewing another department's architecture as part of a cross-government working group, you realise their in-progress ingestion pipeline duplicates, almost feature for feature, a pipeline your team already runs and could share. Their build is three months in, with four months remaining, and their lead engineer is visibly proud of the design. Choose the MOST effective and LEAST effective actions.

A) Say nothing; their department funds its own work and reuse is not your call
B) Raise it in the working group meeting, presenting a comparison and proposing they abandon their build in favour of your pipeline
C) Speak privately with their lead engineer first: share your pipeline's documentation, explore honestly whether it meets their needs, and if it might, offer to bring a joint reuse assessment to the working group as a shared recommendation
D) Email both departments' directors recommending the duplicate project be stopped to avoid wasting public money
E) Suggest they finish their build, then converge the two pipelines "at some future point"

**Most effective: C. Least effective: D.**

**Explanation:** Your role profile explicitly includes recognising and sharing opportunities to reuse existing data flows between teams and championing data engineering across government — this scenario is that duty with realistic social friction attached. Option C sequences influence correctly: technical validation before public advocacy, respect for the other engineer's ownership, and a *joint* recommendation that lets them share credit for the saving rather than absorb blame for the duplication. Reuse across departments is as much a relationship problem as a technical one, and C is the only option that treats it as both. Option B may be right on the merits but ambushes a proud engineer in front of peers; proposals presented as fait accompli to the people who must implement them tend to be resisted on principle, and "abandon your build" without a joint gap analysis is premature. Option A fails the stewardship test — duplicated public spending is everyone's business in cross-government forums, which exist precisely for this. Option E is polite waste: convergence "at some future point" after doubling the investment rarely happens and defers the hard conversation indefinitely. Option D is least effective: leaping two levels of hierarchy with a stop-work recommendation, before any technical validation with the people who know the requirements, maximises embarrassment, weaponises the working group's access, and destroys the trust that makes future cross-government collaboration possible. You would win the battle and lose the profession's network.

**Question 5 (moderate) — The struggling junior engineer**

A junior engineer on one of your teams has, for the second sprint running, delivered pipeline code with test coverage well below the team's agreed standard, and a peer has privately complained to you about carrying the extra review burden. The junior engineer is enthusiastic and hard-working but was recruited into their first data engineering role five months ago. Choose the MOST effective and LEAST effective actions.

A) Move the junior engineer to less critical work until they improve
B) Raise the pattern with the junior engineer directly and kindly: review a recent piece of their code together, understand why the tests are thin (skill gap, time pressure, unclear standard), agree a development plan, and pair them with an experienced engineer for the next sprint
C) Tell the complaining peer that supporting juniors is part of everyone's job and they should continue reviewing patiently
D) Tighten the pipeline's merge controls so code below the coverage threshold cannot be merged at all
E) Raise the issue at the team retrospective as a general reminder about test coverage, without naming anyone

**Most effective: B. Least effective: C.**

**Explanation:** Your role profile includes advising less experienced team members and coordinating teams — this scenario tests whether you develop people or merely process them. Option B is direct, kind, and diagnostic: it distinguishes skill gaps from time pressure from unclear standards (three different problems with three different fixes), invests in the person, and relieves the overloaded peer through structured pairing rather than open-ended patience. Option D is a reasonable *supporting* control — automated coverage gates are good engineering — but as a complete response it is impersonal: the junior engineer's merges start failing with no explanation or support, converting a development need into a wall. Choosing D alone confuses tooling with leadership; the strongest real-world answer is B with D as follow-through. Option A protects delivery but quietly labels the engineer a problem, removes exactly the stretch experiences they need, and addresses nothing. Option E is conflict avoidance dressed as facilitation: everyone at the retrospective either knows who is meant (making it a public shaming by implication) or does not (making it useless). Option C is least effective because it dismisses a legitimate signal from a conscientious team member, converts their goodwill into resentment, and leaves the underlying development need wholly unaddressed — the burden continues, now with instructions to suffer silently. SJT scoring at leadership level consistently punishes options that silence feedback rather than act on it.

**Question 6 (hard) — The incident, the fix, and the root cause**

A critical data flow feeding several departmental BI systems failed at 06:00. Your team applied a manual workaround by 08:30, and consumers are unaffected. The engineer who fixed it says the underlying cause is "probably the upstream API change last week" and wants to move on to sprint work; the same flow failed with similar symptoms twice in the past quarter. Sprint commitments are already at risk. Choose the MOST effective and LEAST effective actions.

A) Accept the workaround, note "probable upstream API change" in the incident log, and return the team to sprint work
B) Commission a time-boxed root-cause investigation for the recurring failure, led by the fixing engineer with one other, present the findings to the team, and implement a permanent fix and detection — accepting a visible, communicated cost to this sprint's commitments
C) Ask the engineer to investigate the root cause "when they have spare time"
D) Escalate to the upstream system's team, asking them to stop changing their API without notice
E) Schedule the investigation for next quarter's planned maintenance window

**Most effective: B. Least effective: C.**

**Explanation:** Problem management at your level means ensuring the right actions are taken to investigate, resolve, and *anticipate* problems — and a third similar failure in a quarter is a pattern announcing a fourth. Option B is textbook: time-boxed (so it cannot swallow the sprint), staffed with the person holding the freshest context plus a second pair of eyes (spreading knowledge, checking assumptions), transparent about the delivery trade-off, and finished only when both permanent fix *and* detection exist — because a problem you can detect early is half-solved. Option A embeds a guess ("probably") as an explanation; unverified causes in incident logs are how organisations convince themselves recurring problems are a series of coincidences. Option D acts on that same unverified guess and spends cross-team escalation capital on it; if investigation later shows the cause was your own pipeline's timeout handling, the apology costs more than the escalation gained — verify first, escalate second. Option E treats a recurring live failure as scheduled maintenance; the failure has not agreed to wait for next quarter. Option C is least effective because "when you have spare time" is a decision disguised as a deferral — spare time does not exist in a team with at-risk sprint commitments, so C silently chooses never, while allowing everyone to believe the investigation is happening. Of all the options, it is the only one that is dishonest with the team itself. Least-effective options in incident scenarios are typically the ones that neither fix nor honestly decline to fix.

**Question 7 (moderate) — The exciting tool and the procurement reality**

Two of your strongest engineers champion adopting a genuinely promising open-source data orchestration framework they have prototyped successfully. Adopting it would mean migrating twelve production pipelines, retraining four teams, and it falls outside the department's currently supported technology list. The engineers are ready to start migrating "quietly, one pipeline at a time" and warn that the profession will leave the department behind if it always waits. Choose the MOST effective and LEAST effective actions.

A) Authorise the quiet gradual migration; innovation requires bending rules and the tool is clearly better
B) Decline: the supported-technology list exists for good reasons and the current orchestrator works
C) Channel the prototype into a formal evaluation: define success criteria with the engineers, run a bounded pilot on a non-critical flow with the platform and architecture teams' knowledge, and take the results to the technology governance forum as a proposal to amend the supported list
D) Tell the engineers to raise it with the architecture team themselves and continue with current tooling meanwhile
E) Adopt the framework for all new pipelines only, leaving the twelve existing ones alone, without updating the supported-technology list

**Most effective: C. Least effective: A (with E close behind).**

**Explanation:** Your data innovation skill is defined with unusual precision in the framework: identify areas of innovation *and recognise appropriate timing for adoption* — timing being the discipline this scenario probes. Option C honours both halves. It keeps the engineers' energy (they define the success criteria), makes the evaluation legitimate (governance forums exist to update technology lists — using them *is* how the list stays good), bounds the risk (non-critical flow, known to platform teams), and creates the evidence an adoption decision deserves. Option A is least effective: "quietly" is the tell. Unsanctioned divergence across production pipelines creates shadow infrastructure that the wider organisation cannot support, secures no training or security review, and — when discovered — sets back not just this tool but the credibility of every future innovation proposal from your teams. Championing data engineering across government requires being the person governance forums trust, not the person they audit. Option E commits the department to *two* orchestration stacks indefinitely — doubling the skills burden and operational surface — while still bypassing governance; it is option A with better manners. Option B wastes the prototype, the enthusiasm, and possibly a real opportunity: flat refusal teaches strong engineers to stop proposing (or to stop asking). Option D is half-hearted delegation of your own leadership duty — sending engineers without positional influence to argue an architectural case you believe has merit is how good proposals die politely. The leadership pattern the assessors seek: convert unsanctioned enthusiasm into sanctioned evidence.

**Question 8 (hard) — The difficult discussion you must host**

You are hosting a meeting to resolve a dispute: the information governance lead insists a new cross-departmental analytics flow must exclude a set of sensitive fields until a data protection assessment completes (six weeks away), while the consuming department's deputy director says the analysis is needed for a fiscal event in three weeks and accuses governance of "blocking the whole point of the project". Tempers are short. As the technical chair, choose the MOST effective and LEAST effective actions.

A) Side with governance: the assessment is mandatory and the deputy director must wait
B) Side with the deputy director: the fiscal event is a national priority and governance can assess retrospectively
C) Reframe the dispute around options: ask governance which specific fields drive the assessment requirement, ask the deputy director which analyses the fiscal event actually needs, and explore technical middle paths — a flow excluding the sensitive fields now, pseudonymisation, or aggregated outputs — with a clear decision-owner and date for each
D) Pause the meeting and ask both parties to escalate to their respective directors for a decision
E) Commit your team to accelerating the flow's build so that whichever way the decision goes, delivery is not the bottleneck

**Most effective: C. Least effective: B.**

**Explanation:** Supporting or hosting difficult discussions with diverse senior stakeholders is a named skill at your level, and option C demonstrates its core move: converting a positional standoff ("must wait" versus "cannot wait") into a joint examination of the underlying needs, where technical expertise genuinely adds options neither party could see alone. Perhaps only two of thirty fields trigger the assessment; perhaps the fiscal analysis needs aggregates that carry no personal data at all. The chair who asks those questions usually dissolves the dispute rather than adjudicating it — and note that C keeps governance requirements fully intact while serving the deadline: it looks for what is possible *inside* the rules. Option A is defensible (compliance is not optional) but prematurely adversarial: it accepts the framing that the only choices are total delay or total delivery, when the technical middle ground has not been explored — a data engineering leader who defaults to "wait" wastes the specific value they bring to the room. Option B is least effective: "assess retrospectively" means processing sensitive personal data before assessing whether it is lawful to do so — a potential legal breach, a betrayal of citizen trust, and precisely the outcome governance colleagues exist to prevent. No fiscal deadline converts an unlawful processing decision into a good one, and a technical chair endorsing it lends engineering credibility to a compliance failure. Option D escalates before the room has done its work; escalation is for genuine impasses, not for chairs avoiding hard facilitation. Option E is generous but answers a question nobody asked — build speed was not the blocker, and committing your team's capacity as a gesture erodes it for the problems that are yours.

**Question 9 (moderate) — Ranking: the morning the numbers disagreed**

At 09:15 you learn that two departmental dashboards — both fed by flows your teams operate — are showing different totals for the same headline measure, and a permanent secretary's office has noticed. Rank these four actions from FIRST to LAST as your immediate sequence.

1. Establish which (if either) figure is correct, and the scope and cause of the divergence
2. Send a brief holding message to the permanent secretary's office and both dashboards' owners: divergence confirmed, under investigation, which figure (if either) to trust meanwhile, update by a stated time
3. Convene the two responsible engineers to trace the divergence to its source
4. Draft the root-cause report and the prevention plan (reconciliation checks between the two flows)

**Correct ranking: 2, 3, 1, 4 — with 2 and 3 defensibly simultaneous.**

**Explanation:** The instinct of most engineers is to investigate first and communicate when there is something solid to say (order 1 or 3 first). Leadership inverts this: when a permanent secretary's office has already noticed a discrepancy, silence is itself a message — it says "they do not know either", and it invites decisions to proceed on whichever wrong number is convenient. The holding message (2) costs five minutes, tells consumers what to trust in the interim, and buys the investigation room to be thorough; stating an update time converts anxiety into schedule. Convening the engineers (3) starts the technical work — realistically you send the message *while* assembling them, which is why 2 and 3 are near-simultaneous, but if forced to sequence, communication leads because its value decays fastest. Establishing the correct figure and cause (1) is the investigation those engineers perform, so it follows 3. The report and prevention plan (4) come last — not because prevention matters least, but because reconciliation checks designed before the cause is known are guesswork. The deeper lesson for ranking questions: they test *sequencing under pressure*, and the discriminator is almost always where communication sits. Candidates who bury stakeholder communication at position three or four have answered as engineers; the role being assessed is a leader of engineers.

### Preparation tips

- **Answer as the leader the role profile describes, not as your most cautious self.** Before the test, re-read your role's duties: coordinate teams, set standards, manage expectations, champion the profession. The "most effective" option usually acts where those duties point — directly, transparently, and with others rather than around them.
- **Rehearse the values explicitly.** User needs first, transparency, collaboration, accessibility and inclusion, stewardship of public money and citizens' data. When torn between two plausible options, ask which one a permanent secretary could comfortably describe in public afterwards.
- **Look for the option that gathers information before acting** — but distinguish genuine diagnosis (time-boxed, purposeful) from procrastination dressed as diligence. Assessors reward the former and punish the latter.
- **Practise "least effective" separately.** It is usually not the most aggressive option but the one that silences feedback, destroys a safeguard, hides information, or transfers a problem without solving it. Train yourself to spot those four signatures.
- **Draw on real memories.** For each practice scenario, recall a time you faced something similar and what actually worked. Your genuine leadership experience is the best calibration available — the test is trying to measure it.
- **Do not overthink cultural second-guessing.** UK public sector SJTs consistently reward transparency, early communication, proportionate escalation, and developing people. You do not need to guess a hidden culture; it is published.

### Common pitfalls

- **Choosing the idealistic option over the effective one.** "Refuse until it is perfect" feels principled but often abandons stakeholders (see the real-time dashboard scenario). The strongest options are honest *and* useful.
- **Selecting passive or deferring options.** "Mention it at the retrospective", "when they have spare time", "at some future point" — options that delay action, pass the problem along, or ignore root causes are systematically scored down, and the specs call this out directly.
- **Premature escalation.** Escalating above someone's head before speaking to them, or before any analysis, wastes trust and reads as conflict avoidance by other means. Escalate genuinely stuck or genuinely serious issues — after doing your part.
- **Protecting yourself instead of the outcome.** Logging a risk while enabling the harm, staying silent to preserve a relationship, quietly excluding failing records — assessors specifically watch for self-protective patterns.
- **Answering as an individual contributor.** At lead level, options where you personally absorb the work (registering datasets yourself, taking over the code) score poorly against options that build capability and accountability in others.
- **Ignoring stated constraints in the scenario.** If the scenario says the failure recurred twice or the office has already noticed, those details exist to change the correct answer. Read scenarios with the same precision you give verbal reasoning passages.

## Conclusion

You have now worked through all four assessment types a lead data engineer is most likely to meet: cognitive, numeric reasoning, verbal reasoning, and situational judgement. Along the way you have practised the specific mental disciplines each one rewards — bounding a fault from healthy evidence, anchoring every percentage to its base, refusing inferences a text does not support, and sequencing communication ahead of investigation when stakeholders are watching.

A few threads run through everything you have read. First, these assessments are not alien rituals: they are compressed, standardised versions of judgements you already make every week across data flows, standards, budgets, and difficult meetings. Preparing for them is professional development in disguise — the same precision that earns marks on a Cannot Say question makes you a sharper reviewer of specifications, and the same values that identify a "most effective" option make you a better chair of contested discussions. Second, technique matters and is learnable: reading scope words deliberately, estimating before calculating, time-boxing stubborn questions, and naming the criterion before answering are habits that reliably add marks within a week or two of practice. Third, calibrated confidence beats both arrogance and anxiety: you operate at a senior level in a demanding profession, and the evidence of that capability is exactly what these instruments are designed to surface.

For next steps, keep the practice light but regular — a handful of questions a few times a week beats a single marathon session. Build your own practice items from the documents and dashboards you genuinely use, because authoring questions teaches faster than answering them. If a formal assessment is coming, ask the organisers what format and platform will be used, do every ungraded practice item offered, and treat the logistics (rest, environment, timing) with the same care you would give a production go-live. And whatever the outcome, mine the feedback: an assessment report is data, and working effectively with data is rather your speciality.

Good luck — prepare well, trust your experience, and let the assessments show what you can do.

