# Data Analyst (Principal Data Analyst) - Psychometric Assessment Resources

## Introduction

Welcome. This document is a practical, self-contained preparation resource for psychometric assessments, written specifically for you as a principal data analyst working within the UK Government Digital and Data profession. Whether you are preparing for an internal promotion board, an external appointment, a development centre, or simply wish to benchmark your own capabilities, this guide gives you realistic, role-specific practice material calibrated to the seniority at which you operate.

Psychometric assessments are structured, standardised measures of the mental capabilities and behavioural judgement that underpin performance in a role. They matter for a principal-level position because the decisions you make ripple outward: you influence organisational decision making on data analysis, you oversee continuous improvement of data practices and management across your organisation, and you represent the data analyst community both inside and outside government. Assessors want evidence that you can interpret complex quantitative material accurately under time pressure, extract precise meaning from dense policy and standards documentation, reason logically about analytical pipelines and data quality problems, and exercise sound professional judgement in situations involving senior stakeholders, ethical tension, and competing priorities. These are exactly the capabilities psychometric instruments are designed to measure, and exactly what this guide helps you rehearse.

The document is organised into four substantial sections, each covering one assessment type you are likely to encounter:

1. **Workplace job-specific cognitive assessment** — pattern recognition, logical deduction, error checking, prioritisation, and problem solving using the artefacts you genuinely handle: data models, quality dashboards, analytical code, and governance registers.
2. **Workplace job-specific numeric reasoning assessment** — interpretation of tables, percentages, ratios, budgets, capacity figures, and performance metrics of the kind that cross your desk when you lead data teams and quality-assure statistical outputs.
3. **Workplace job-specific verbal reasoning assessment** — comprehension of dense role-relevant passages: data ethics policies, governance standards, ministerial briefings, and stakeholder correspondence, tested with True / False / Cannot Say and multiple-choice questions.
4. **Workplace job-specific situational judgement assessment** — realistic dilemmas involving your real stakeholders: directors, policy leads, junior analysts you mentor, and cross-government communities of practice.

Each section explains what the assessment measures, maps its dimensions to the specific skills in your role profile, provides a bank of worked practice questions of graded difficulty with full explanations, and closes with preparation tips and common pitfalls.

How to use this guide: work through the practice questions under gentle time pressure first, then review the explanations carefully — the reasoning is where the learning lives. Use the questions for self-reflection as much as for practice: at principal level, articulating *why* an answer is right is itself a leadership skill, because you will coach others through these same judgements. Take your time, revisit sections as needed, and treat every question as a rehearsal for the real analytical and interpersonal decisions your role demands.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive assessment is a targeted psychometric test that measures the exact mental processes your role demands, rather than abstract intelligence. Unlike a generic IQ test, it presents practical workplace scenarios and data artefacts drawn from the everyday reality of your job, and it is designed to predict on-the-job performance. For a principal data analyst, that means questions built around analytical data models, data quality dashboards, statistical outputs awaiting quality assurance, reproducible code pipelines, governance registers, and project plans for varied data projects.

The typical format is an online, timed test of 15 to 30 minutes, with objective scoring against a benchmark or norm group appropriate to senior analytical roles. Questions are validated to ensure they predict job success without bias, and modern platforms may adapt question difficulty based on your previous answers. You will usually receive short, ungraded practice questions first so you can get comfortable with the interface. Employers typically receive a breakdown showing your speed versus accuracy rather than a single number, so a considered, accurate approach is as valuable as a fast one.

At your level, the assessment is less about raw processing speed and more about the quality of reasoning under constraint: can you spot the flaw in a data model before it propagates into every downstream report? Can you deduce which stage of a pipeline introduced an anomaly? Can you prioritise correctly when several urgent analytical requests collide? These are the daily cognitive demands of leading significant areas of work in data analysis.

### What it measures for your role

The cognitive assessment maps directly onto the skills named in your role profile:

- **Applying statistical and analytical tools and techniques.** Logical deduction and error-checking items test the mental habits behind overseeing quality assurance of statistical techniques and analytical outputs. Spotting an inconsistency between a chart and its underlying table is quality assurance in miniature.
- **Data preparation and linkage.** Pattern-recognition items using entity relationships, join keys, and data lineage diagrams mirror your responsibility to develop analytical data models using a deep understanding of data sources, and to set data quality standards others follow.
- **Developing code for analysis.** Sequence and logic questions echo the reasoning you use when you oversee coding standards and ensure reproducibility of code and documentation across the organisation.
- **Data management.** Rule-application questions reflect your leadership of data management and governance processes — deducing what a retention schedule or access-control matrix implies for a specific dataset.
- **Managing a data project.** Prioritisation items test the trade-off reasoning you use when you oversee and advise on the planning and implementation of the project life cycle on varied data projects.
- **Delivering business impact through data.** Problem-solving items reward the ability to see which analytical intervention will actually move an organisational objective — the cognitive core of leading others to deliver scalable data products.

### Practice questions

**Question 1 (easy) — Pattern recognition in a data quality dashboard.**
Your team's data quality dashboard reports completeness scores for a citizen-contact dataset over six weekly snapshots: 98.2%, 98.0%, 97.9%, 95.1%, 97.8%, 97.7%. Which observation is the most defensible?

A. Completeness is in steady long-term decline and the pipeline should be rebuilt.
B. Week 4 is an outlier against an otherwise gently declining trend, and the week 4 ingestion should be investigated as a one-off incident.
C. The dashboard is faulty because completeness cannot fall then recover.
D. The dataset became 2.7% smaller in week 4.

**Correct answer: B.**
**Explanation:** Five of the six values form a slow, near-linear drift from 98.2% to 97.7% — a decline of about 0.1 percentage points per week. Week 4's 95.1% breaks that pattern by nearly three percentage points and then the series returns to trend, which is the classic signature of a transient ingestion failure rather than a structural problem. Option A over-reacts to a single anomaly; option C wrongly assumes completeness is monotonic; option D confuses completeness (proportion of populated fields) with dataset size. At principal level, distinguishing a one-off incident from a systemic trend determines whether you commission a fix or a redesign.

**Question 2 (easy) — Rule application in data governance.**
Your organisation's data management policy states: "Datasets containing personal data must have a named information asset owner, a completed data protection impact assessment (DPIA) where processing is high risk, and a retention schedule. Datasets that are fully anonymised require only a retention schedule." A new dataset contains pseudonymised case records — individuals are not directly identifiable, but re-identification is possible with a key held elsewhere. Which requirements apply?

A. Only a retention schedule, because the data is not directly identifying.
B. A named information asset owner and a retention schedule; a DPIA only if the processing is high risk.
C. All three requirements automatically, because pseudonymised data is always high risk.
D. None, because the policy does not mention pseudonymised data.

**Correct answer: B.**
**Explanation:** Pseudonymised data remains personal data because re-identification is possible, so the personal-data requirements apply: a named owner and a retention schedule unconditionally, and a DPIA conditionally "where processing is high risk". Option A wrongly treats pseudonymised as anonymised. Option C invents an automatic high-risk classification the policy does not state. Option D fails a basic deduction: the policy covers all datasets containing personal data, and pseudonymised data falls in that class. This is exactly the kind of careful rule-reading you model when you champion governance processes across your organisation.

**Question 3 (moderate) — Logical deduction across a pipeline.**
A nightly analytical pipeline runs four stages in order: (1) extract from three source systems, (2) standardise and link records, (3) apply the analytical data model, (4) publish to the reporting layer. This morning the reporting layer shows duplicate records for roughly 8% of citizens. You establish these facts: the extract row counts match the source systems exactly; the linkage stage logged a warning that one source system changed its unique identifier format last night; the model stage ran without errors; the publish stage copied exactly what the model stage produced. Where did the duplication most plausibly originate?

A. Stage 1, because three source systems always create duplicates.
B. Stage 2, because a changed identifier format would prevent records for the same person from being matched, leaving them as apparent distinct individuals.
C. Stage 3, because analytical models multiply rows.
D. Stage 4, because publishing is the last stage before the duplicates were seen.

**Correct answer: B.**
**Explanation:** Work the evidence stage by stage. Extract counts match sources, so stage 1 introduced nothing. Stage 2 logged a warning precisely about identifier format — and record linkage depends on identifiers to recognise that two rows describe the same person. If one system's identifiers changed format, its records would fail to match their counterparts and would survive as separate "people": duplication by *failed matching*, not by row multiplication. Stages 3 and 4 are exonerated by clean runs and exact copies. Option D commits the classic error of blaming the point of discovery rather than the point of origin. Diagnosing failures by reasoning over lineage evidence is core to overseeing continuous improvement of data practices.

**Question 4 (moderate) — Error checking a statistical output.**
A junior analyst you mentor submits a report stating: "Median processing time fell from 12 days to 9 days, a 33% improvement. The mean fell from 15 days to 14 days. Since both averages improved, performance improved uniformly across all cases." Which single criticism is the most important quality-assurance challenge?

A. The percentage is wrong: a fall from 12 to 9 is a 25% improvement, not 33%.
B. Medians should never be used for processing times.
C. The conclusion of uniform improvement does not follow: a falling median with a nearly static mean suggests the longest cases barely improved, so improvement was not uniform.
D. Means and medians can never both improve at once.

**Correct answer: C.**
**Explanation:** Option A is a genuine arithmetic error — (12 − 9) / 12 = 25% — and worth correcting, but it is a detail. The most important challenge is C, because the *inference* is unsafe: the median dropped 3 days while the mean dropped only 1, which mathematically requires that the upper tail (the slowest cases) improved far less than the middle. Claiming "uniform" improvement misleads decision makers about precisely the cases they most care about. Options B and D are simply false statements about statistics. Your role requires you to oversee the quality assurance of analytical outputs — and the highest-value QA catches invalid conclusions, not just wrong numbers.

**Question 5 (moderate) — Prioritisation under competing demands.**
It is 09:15 on Monday. Four items await you: (i) a director needs a one-page brief by 12:00 for a board discussion on the data strategy; (ii) a junior analyst is blocked on a data model question and cannot progress today's sprint work without your steer; (iii) a monthly statistical publication due Thursday has failed an automated quality check overnight; (iv) an external conference has emailed asking you to confirm a speaking slot by Friday. What is the most defensible ordering of your first three actions?

A. (iv), (i), (ii) — clear the quick email first.
B. (ii), (iii), (i) — unblock people, then fix quality, then write the brief.
C. (i), (ii), (iii) — hardest deadline first, then unblock your analyst, then start the quality investigation which has slack until Thursday.
D. (iii), (iv), (i) — quality is always first.

**Correct answer: C.**
**Explanation:** Prioritisation is deadline-and-dependency reasoning, not a fixed hierarchy of virtues. The board brief has the hardest, nearest deadline (12:00 today) and directly serves your accountability to influence organisational decision making. Unblocking the analyst comes next: a few minutes of your time restores a whole day of theirs — high leverage, and the cost of delay compounds hourly. The failed quality check matters greatly but has runway until Thursday; beginning it third still leaves ample time, and you might delegate the initial investigation when you unblock your analyst. The conference reply has four days of slack and belongs at the end of the day. Option B undervalues the immovable 12:00 deadline; options A and D order by habit ("quick wins first", "quality always first") rather than by reasoning.

**Question 6 (moderate) — Pattern recognition in code review.**
Reviewing analytical code for reproducibility, you see four scripts. Script 1 reads data from a dated, versioned snapshot and sets a random seed. Script 2 reads from the live database "as of now" and sets a random seed. Script 3 reads from a dated snapshot and uses unseeded random sampling. Script 4 reads from the live database and uses unseeded random sampling. Ranked from most to least reproducible, the correct order is:

A. 1, 2, 3, 4
B. 1, 3, 2, 4
C. 2, 1, 4, 3
D. 4, 3, 2, 1

**Correct answer: B.**
**Explanation:** Reproducibility requires both fixed inputs and deterministic processing. Script 1 has both — fully reproducible. Between scripts 2 and 3, consider what actually varies: script 3's input is frozen (a dated snapshot) and only its sampling varies, so re-running it explores a stable dataset and its results can be bounded and re-created in distribution; script 2's *input itself* changes with every run because "as of now" is a moving target, so even its seeded logic operates on different data each time — and the input is the larger source of irreproducibility. Script 4 fixes nothing. Hence 1, 3, 2, 4. Ensuring reproducibility of code across the organisation is an explicit duty at your level, and it starts with recognising which sources of variation dominate.

**Question 7 (moderate) — Deduction from a data model.**
In your analytical data model: every Case links to exactly one Citizen; a Citizen may have many Cases; every Payment links to exactly one Case. An analyst reports that a query counting Payments per Citizen returns more Payments than exist in the Payment table. What is the most plausible cause?

A. Some Citizens have no Cases.
B. The join path from Payment to Case to Citizen was written with a join condition that matches on a non-unique field, fanning out rows.
C. Payments genuinely increased during the query.
D. The Payment table has too few rows.

**Correct answer: B.**
**Explanation:** Under the stated model, Payment→Case is many-to-one and Case→Citizen is many-to-one, so joining along those keys can never inflate the Payment count — each Payment reaches exactly one Citizen. If the count *grew*, the join must not be following the declared keys: joining on a non-unique field (say, a case reference that repeats across years) duplicates payment rows — the classic fan-out. Option A would reduce or leave counts unchanged, never inflate them. Options C and D do not explain inflation relative to the table itself. Reasoning from cardinalities to what is and is not possible is the deep understanding of data sources your role profile demands, and it is precisely what you teach when you mentor others in data quality and modelling.


**Question 8 (moderate) — Problem solving on training capability gaps.**
You have identified a data visualisation capability gap across four teams. A skills audit shows: Team A — strong charting skills, weak accessibility practice; Team B — weak charting, weak accessibility; Team C — strong in both; Team D — strong accessibility, weak charting. You can commission exactly two training modules this quarter: "Accessible visualisation" and "Charting fundamentals". Team C can coach one other team instead of attending training. Which allocation closes the most gaps?

A. Send A and B to Accessible visualisation; send D to Charting fundamentals; Team C coaches B on charting.
B. Send all four teams to both modules.
C. Send A to Charting fundamentals and D to Accessible visualisation.
D. Team C coaches everyone; commission no modules.

**Correct answer: A.**
**Explanation:** List the actual gaps: A needs accessibility; B needs both; D needs charting; C needs nothing. Option A covers A's accessibility gap, B's accessibility gap, and D's charting gap through the two modules, and closes B's remaining charting gap through C's coaching — all five gaps closed. Option B wastes training on teams already strong (and exceeds any sensible budget). Option C trains A and D in the skills they already have — it closes zero gaps. Option D closes at most one team's gaps, since C can coach only one team. Identifying capability gaps and implementing appropriate training is a named duty in your data visualisation skill; this question rehearses its logical core: match interventions to actual deficits.

**Question 9 (hard) — Logical deduction on conflicting quality reports.**
Three quality checks run on the same published dataset. Check X (schema validation) passes. Check Y (row-count reconciliation against source) fails, reporting 2,140 fewer rows than source. Check Z (aggregate-total reconciliation) passes, with published totals matching source totals exactly. All three checks are known to be individually reliable. Which conclusion follows most strongly?

A. Check Y is wrong because two checks passed and only one failed.
B. The missing 2,140 rows must all carry zero or null values in the aggregated fields, since their absence changes counts but not totals.
C. The dataset is fine because totals match.
D. The source system deleted rows after extraction.

**Correct answer: B.**
**Explanation:** Treat each check as evidence. Y failing means rows are genuinely missing (Y is reliable). Z passing means the aggregate totals are nonetheless identical. Both can be true simultaneously only if the missing rows contribute nothing to the aggregates — that is, they hold zeros or nulls in the summed fields. Option A resolves the conflict by majority vote, which is not how evidence works: the checks measure different things and are all reliable. Option C ignores that 2,140 records — perhaps representing real citizens — are absent, which could bias any non-total analysis such as counts by region. Option D is speculation with no supporting evidence and does not reconcile Z passing. This deduction pattern — holding multiple true facts together until only one explanation survives — is the reasoning behind overseeing quality assurance and continually improving practices.

**Question 10 (hard) — Prioritisation with strategic trade-offs.**
Your organisation's executive committee asks you to recommend one of three data products for immediate investment: (i) a real-time operational dashboard for one directorate, delivering value in 6 weeks to 40 users; (ii) a linked analytical dataset joining three departmental sources, delivering value in 6 months but enabling an estimated 12 future products across the whole organisation; (iii) an automated statistical publication saving 3 analyst-days a month starting in 4 weeks. The organisational data strategy names "building shared, reusable data foundations" as its top priority for the next two years. Which recommendation best serves your remit?

A. Product (i), because fastest visible value builds credibility for data.
B. Product (iii), because guaranteed efficiency savings are lowest risk.
C. Product (ii), because it is the only option that directly delivers the strategy's stated top priority and multiplies future delivery capacity, and you should communicate the longer payback openly.
D. Split investment three ways to avoid disappointing anyone.

**Correct answer: C.**
**Explanation:** At principal level you are expected to lead others in delivering scalable data products that align to organisational objectives — and the objective here is explicit: shared, reusable foundations. Product (ii) is the only candidate that is foundational and scalable (12 downstream products). Options A and B optimise for local, short-term wins against a strategy that has already made the trade-off the other way; choosing them substitutes your own preference for the organisation's stated priority without argument. Option D avoids the decision — spreading investment thinly typically means nothing reaches usable maturity, and executives asked for *one* recommendation. Note the honest caveat in C about payback: strategically communicating the business impact of data includes communicating its timeline truthfully.

**Question 11 (hard) — Error checking a visualisation against its data.**
A draft slide for the board shows a bar chart titled "Data quality incidents halved this year". The bars show 48 incidents last year and 31 this year. The vertical axis starts at 25 rather than zero. The underlying table also shows that this year has two months remaining. Identify the complete set of problems.

A. Only the axis truncation.
B. Only the incomplete year.
C. The claim "halved" is arithmetically wrong (31 is a 35% reduction, not 50%); the truncated axis visually exaggerates the fall; and the year-to-date figure is compared against a full year, biasing the comparison further in the claim's favour.
D. There are no problems; 31 is roughly half of 48.

**Correct answer: C.**
**Explanation:** Three independent flaws compound in the same direction. First, arithmetic: halving 48 gives 24, and (48 − 31) / 48 ≈ 35.4% — "halved" overstates the improvement. Second, visual integrity: starting the axis at 25 makes the 31 bar appear about a quarter of the height of the 48 bar, dramatising the difference; bar charts encode value by length, so their baseline must be zero. Third, denominator fairness: with two months still to run, this year's count will likely rise, so the comparison flatters the current year. Option D's "roughly half" is exactly the imprecision a principal must challenge before it reaches a board. Setting and advocating standards in data visualisation means catching all three classes of error — numerical, perceptual, and methodological — not just the most visible one.

**Question 12 (hard) — Problem solving across the project life cycle.**
A six-month data project you oversee is at the end of month two. The problem statement, agreed with the sponsoring director, was "identify which service channels drive avoidable contact". The delivery team now reports that the channel-identifier field needed for the analysis is reliably populated in only 30% of records, and backfilling it would take four months. Which option best reflects sound project reasoning?

A. Continue as planned; four months of backfill still fits within six months.
B. Pause and convene the sponsor: present the data limitation, and offer re-scoped options — for example, analysing the reliably-populated 30% with clearly stated caveats about representativeness, or answering a nearby question the data can support — and let the sponsor choose with full knowledge.
C. Quietly switch to analysing the 30% and present the results as if they covered all contact.
D. Cancel the project because the data is inadequate.

**Correct answer: B.**
**Explanation:** Test option A against the timeline: four months of backfill starting at month two consumes the entire remaining schedule, leaving zero time for the actual analysis — it does not fit. Option C is an integrity failure: results from a 30% subset may be systematically unrepresentative (perhaps one channel populates the field far more reliably), and concealing that misleads the decision it was meant to inform. Option D discards recoverable value without consulting the person accountable for it. Option B does what your role profile calls advising on problem statement development and leading stakeholder relationships: surface the constraint early, translate it into decision-ready options, and keep the sponsor in control of the trade-off. Bad news early with options attached is a hallmark of principal-level project judgement.

**Question 13 (hard) — Integrative reasoning on standards adoption.**
You propose a new organisation-wide standard requiring all analytical code to be version-controlled with peer review before publication. Evidence gathered: Team P adopted it voluntarily and cut published errors by 40%; Team Q says review adds two days to small jobs; Team R publishes daily statistics under statutory deadlines; Team S has no members trained in version control. Which implementation plan reasons correctly from all four facts?

A. Mandate the full standard immediately for all teams; the 40% figure proves it works everywhere.
B. Abandon the standard; Team Q's objection shows it is unworkable.
C. Phase the rollout: mandate it now for routine outputs, create a proportionate lightweight review path for small jobs (addressing Q), agree a pre-approved rapid procedure for statutory daily publications (addressing R), and fund version-control training for S before their compliance date.
D. Apply the standard only to Team P, since only they have proven it works.

**Correct answer: C.**
**Explanation:** Each fact constrains a good plan. P's result supports the standard's value but is one team's experience, not universal proof — so option A over-generalises. Q's two-day cost is a proportionality problem, solved by right-sizing review to job size, not by abandonment — so option B over-corrects from a single objection. R's statutory deadlines demand a designed-in rapid path, otherwise the standard forces a choice between compliance and legal duty. S's skills gap makes immediate mandating unfair and unachievable; training first makes compliance possible. Option D confines the benefit to where it is least needed. Option C is the only plan that answers all four constraints, and it mirrors your duties to contribute to coding standards across the organisation, implement training requirements, and share good practice in adapting teams' ways of working.

### Preparation tips

- **Rehearse with your own artefacts.** Before the assessment, spend an hour reviewing a real data model, a quality dashboard, and a recent code review from your own work, consciously narrating the reasoning: what would break this? what does this cardinality forbid? The test formats are abstractions of exactly these judgements.
- **Practise evidence-first deduction.** For pipeline and diagnosis questions, list the facts, then eliminate stages or causes the facts exonerate. Resist jumping to the most familiar culprit.
- **Time-box, don't rush.** With 15 to 30 minutes total, allocate roughly a minute or two per question and move on when stuck; flagged questions can often be answered quickly on a second pass once easier points are banked. Employers see speed *and* accuracy, so an unhurried, correct answer beats a fast guess.
- **Read every option before answering.** At senior level the distractors are plausible; the best answer often differs from a good answer only in completeness (as in Questions 11 and 13).
- **Use the practice items.** Ungraded warm-up questions exist to let you settle into the interface; treat them seriously so no marks are lost to unfamiliar controls.
- **Arrive rested and set up properly.** A quiet room, a stable connection, and a glass of water are worth several percentile points in sustained concentration. You already exercise this reasoning daily — the assessment simply asks you to do it in a distilled form.

### Common pitfalls

- **Blaming the point of discovery rather than the point of origin.** As in Question 3, errors surface downstream of where they are created. Trace lineage backwards before concluding.
- **Answering from habit rather than from the scenario.** "Quality first" or "quick wins first" are slogans, not reasoning; the correct prioritisation depends on the specific deadlines and dependencies given.
- **Stopping at the first flaw found.** Senior-level items often contain multiple compounding problems (Question 11). Check whether the question asks for the *complete* set.
- **Over-calculating when deduction suffices.** Many cognitive items yield to elimination — establishing what the stated rules make impossible — faster than to computation.
- **Getting stuck in a time sink.** One stubborn multi-stage problem can consume the time for three easier ones. Skip, bank the easy marks, return if time allows.
- **Assuming your real-world workaround is available.** In the test you cannot email a colleague or query the database; reason only from what the question provides, just as the scoring does.


## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment evaluates your ability to analyse, interpret, and make logical decisions using numerical data presented in the formats your role genuinely handles. It mimics the data-handling demands of the job, focusing on applied business mathematics — percentages, ratios, rates, budget allocations, and cost-benefit estimations — rather than abstract formulae. Question inputs are typically graphs, tables, budget statements, capacity plans, and performance dashboards.

For a principal data analyst this is home territory, but do not let familiarity breed complacency: the assessment tests careful extraction and manipulation of figures under a strict time limit, usually with less than ninety seconds per question. Most platforms allow or provide an on-screen calculator, because the intent is to measure interpretation and reasoning rather than mental arithmetic. Expect multi-step questions: read a value from a table, adjust it by a percentage, combine it with a second value, and compare the result against a threshold or a rival option.

At your level the numerical content will skew towards the figures you steward rather than produce: team budgets and day rates, publication performance metrics, data quality percentages, capacity and demand projections, weighted survey results, and the cost cases behind data products. The reasoning is the same reasoning you apply when you quality-assure a junior analyst's workings or challenge a benefits estimate in a business case — performed quickly, accurately, and without help.

### What it measures for your role

- **Applying statistical and analytical tools and techniques.** Percentage change, weighted averages, rates, and index numbers are the raw material of the statistical insights and reports you oversee; the assessment checks you manipulate them flawlessly at speed, which underpins credible quality assurance of others' outputs.
- **Delivering business impact through data.** Cost-benefit items — payback periods, savings projections, benefit-per-pound comparisons — test the numeracy behind strategically communicating the business impact of data and deciding when to pivot investment.
- **Managing a data project.** Budget burn rates, resource day calculations, and schedule arithmetic reflect your oversight of planning and implementation across the project life cycle on varied data projects.
- **Data preparation and linkage.** Reconciliation arithmetic — row counts, match rates, completeness percentages — mirrors the data quality standards you set and the linkage work you supervise.
- **Data visualisation.** Reading values accurately from charts and tables, including scale qualifiers such as "in thousands", is the quantitative bedrock of the visualisation standards you advocate.
- **Communicating between the technical and non-technical.** Several items ask you to select the correct plain-English statement of a numerical result — the translation task you perform for stakeholders at all levels.

### Practice questions

**Question 1 (easy) — Percentage change in a performance metric.**
Your team's monthly statistical publication was downloaded 12,400 times in April and 14,880 times in May. What was the percentage increase?

A. 15%  B. 20%  C. 24.8%  D. 25%

**Correct answer: B.**
**Explanation:** Increase = 14,880 − 12,400 = 2,480. Percentage increase = 2,480 ÷ 12,400 = 0.20 = 20%. A common error is dividing by the *new* figure: 2,480 ÷ 14,880 ≈ 16.7%, which is not offered but shows why the denominator matters — percentage change is always measured against the starting value. Distractor C comes from misreading 2,480 as a percentage of 10,000.

**Question 2 (easy) — Data quality match rate.**
A record linkage exercise attempts to match 68,000 hospital records to a population register. 61,200 match automatically, 4,080 match after clerical review, and the remainder fail to match. What proportion of records ultimately failed to match?

A. 4%  B. 6%  C. 10%  D. 2,720 records cannot be expressed as a proportion

**Correct answer: A.**
**Explanation:** Total matched = 61,200 + 4,080 = 65,280. Unmatched = 68,000 − 65,280 = 2,720. Proportion = 2,720 ÷ 68,000 = 0.04 = 4%. Distractor B is the clerical-review share (4,080 ÷ 68,000 = 6%); distractor C is the total non-automatic share (6,800 ÷ 68,000 = 10%). Read the question stem precisely: it asks about *ultimate* failures, after both matching passes. Setting data quality standards means knowing exactly which denominator and numerator each published rate uses.

**Question 3 (easy) — Team budget arithmetic.**
Your data analysis team has an annual staffing budget of £840,000. Contractor day rates average £600 and each contractor works 220 days per year. If you allocate 25% of the budget to contractors, how many full-time-equivalent contractors can you fund?

A. 1.4  B. 1.59  C. 2.1  D. 3.18

**Correct answer: B.**
**Explanation:** Contractor budget = 25% × £840,000 = £210,000. Annual cost per contractor = £600 × 220 = £132,000. Number fundable = £210,000 ÷ £132,000 ≈ 1.59 FTE. Distractor D doubles the answer by taking 50% of budget; distractor A uses a 200-day year. In practice you would round to a hiring decision, but the assessment wants the exact quotient — read whether the question asks for a whole number or a value.

**Question 4 (moderate) — Weighted average across teams.**
Three teams respond to a data maturity survey. Team A: 20 staff, average score 3.6. Team B: 35 staff, average score 2.8. Team C: 15 staff, average score 4.0. What is the organisation-wide average score, weighted by staff numbers?

A. 3.30  B. 3.47  C. 3.26  D. 3.13

**Correct answer: C.**
**Explanation:** Weighted sum = (20 × 3.6) + (35 × 2.8) + (15 × 4.0) = 72 + 98 + 60 = 230. Total staff = 20 + 35 + 15 = 70. Weighted average = 230 ÷ 70 ≈ 3.26. Distractor B is the unweighted mean of the three team scores ((3.6 + 2.8 + 4.0) ÷ 3 ≈ 3.47), the single most common weighting error and one you must catch instantly when quality-assuring analytical outputs: the largest team scored lowest, so the true average sits below the naive mean.

**Question 5 (moderate) — Reading a table with scale qualifiers.**
A capacity table shows monthly records processed (in thousands): January 310, February 288, March 342. Your pipeline's contracted capacity is 3.6 million records per quarter. By how many records did Q1 processing fall short of, or exceed, contracted capacity?

A. Exceeded by 340,000  B. Fell short of by 2,660,000  C. Fell short of by 340,000  D. Exceeded by 940 records

**Correct answer: B.**
**Explanation:** Q1 total = (310 + 288 + 342) thousand = 940 thousand = 940,000 records. Contracted capacity = 3,600,000. Shortfall = 3,600,000 − 940,000 = 2,660,000 records. The trap is the "in thousands" qualifier: reading 940 as raw records (distractor D) or mixing units between the table (thousands) and the contract (millions) produces distractors A and C. Always normalise all figures to the same unit before comparing — the classic chart-label pitfall named in assessment guidance.

**Question 6 (moderate) — Cost-benefit of automation.**
Automating a statistical publication costs £45,000 to build and £500 per month to run. It saves 3 analyst-days per month, and an analyst-day is costed at £350. Approximately how many months until cumulative savings equal cumulative costs?

A. 43 months  B. 82 months  C. 30 months  D. Never — running costs exceed savings

**Correct answer: B.**
**Explanation:** Monthly saving = 3 × £350 = £1,050. Net monthly benefit = £1,050 − £500 = £550. Payback = £45,000 ÷ £550 ≈ 81.8, so about 82 months. Distractor A ignores running costs (£45,000 ÷ £1,050 ≈ 43). Distractor C misreads analyst-days as analyst-weeks. This is the arithmetic behind deciding when to pivot: a seven-year payback on a tool with a plausible five-year life is a case you should challenge, however attractive "automation" sounds — exactly the constructive challenge your role applies to proposed investments.

**Question 7 (moderate) — Percentage points versus percentages.**
Completeness of a key dataset improved from 84% to 91%. Which statement is numerically correct?

A. Completeness improved by 7%.
B. Completeness improved by 7 percentage points, an 8.3% relative improvement.
C. Completeness improved by 8.3 percentage points.
D. Completeness improved by 91%.

**Correct answer: B.**
**Explanation:** The absolute change is 91 − 84 = 7 percentage points. The relative change is 7 ÷ 84 ≈ 0.083 = 8.3%. Option A commits the pervasive conflation of points with percent; option C swaps the two figures. As the person who oversees quality assurance of statistical outputs and communicates between the technical and non-technical, you must both compute and *phrase* this correctly — a minister told "7%" when the truth is "7 percentage points" has been misinformed, and the distinction routinely changes headlines.

**Question 8 (moderate) — Project burn rate.**
A 30-week data project has a budget of £360,000. At week 12, £168,000 has been spent and the project is 35% complete by earned value. If spending continues at the current weekly rate, and the remaining work proceeds at the current rate of completion, will the project finish within budget, and roughly when will the work complete?

A. Within budget, completing at week 30.
B. Over budget by about £120,000, completing around week 34.
C. Over budget by about £60,000, completing around week 32.
D. Under budget by £24,000, completing at week 28.

**Correct answer: B.**
**Explanation:** Current spend rate = £168,000 ÷ 12 = £14,000 per week. Completion rate = 35% ÷ 12 ≈ 2.917% per week, so 100% takes 100 ÷ 2.917 ≈ 34.3 weeks. Total forecast cost = 34.3 × £14,000 ≈ £480,000, which is about £120,000 over the £360,000 budget, finishing around week 34. Distractor A assumes plan equals reality; distractor C halves the overrun by projecting cost over 30 weeks but time over 34 — an inconsistent hybrid. Overseeing the project life cycle means running exactly this forecast the moment actuals diverge from plan, not at week 29.


**Question 9 (moderate) — Ratios in team composition.**
Best practice in your organisation recommends a ratio of one senior analyst to every four analysts, and one principal to every three seniors. Your growing directorate will have 48 analysts next year. How many seniors and principals does the recommended structure imply?

A. 12 seniors and 4 principals
B. 12 seniors and 3 principals
C. 16 seniors and 4 principals
D. 8 seniors and 2 principals

**Correct answer: A.**
**Explanation:** Seniors = 48 ÷ 4 = 12. Principals = 12 ÷ 3 = 4. Distractor B rounds the principal calculation down incorrectly (12 ÷ 3 is exactly 4); distractor C inverts the first ratio as 1:3. Ratio chains like this appear whenever you advise on workforce plans or training requirements — set out each link explicitly and the arithmetic stays honest. Note the assessment habit worth forming: after computing, sanity-check the whole structure (48 + 12 + 4 = 64 staff, ratios 4:1 and 3:1 — consistent).

**Question 10 (hard) — Comparing options per unit of benefit.**
Two data products compete for funding. Product X costs £96,000 and is forecast to serve 1,600 users, saving each 45 minutes per month. Product Y costs £150,000 and is forecast to serve 3,000 users, saving each 30 minutes per month. Valuing staff time at £30 per hour, which product has the better first-year return per pound invested?

A. Product X, returning about £4.50 per £1.
B. Product Y, returning about £3.60 per £1.
C. Product X, returning about £2.70 per £1.
D. They are equal.

**Correct answer: A.**
**Explanation:** Work each product through the same four steps: value per user per month, total per month, total per year, return per pound. Product X: 45 minutes = 0.75 hours; 0.75 × £30 = £22.50 per user per month; × 1,600 users = £36,000 per month; × 12 = £432,000 per year; ÷ £96,000 cost = £4.50 returned per £1 invested. Product Y: 30 minutes = 0.5 hours; 0.5 × £30 = £15 per user per month; × 3,000 users = £45,000 per month; × 12 = £540,000 per year; ÷ £150,000 = £3.60 per £1. So X wins on return per pound even though Y delivers the larger absolute annual benefit (£540,000 versus £432,000) — the question asks for return *per pound invested*, and reading the required metric precisely is half the item. Distractor B is Y's genuine figure, tempting if you stop after noticing Y's bigger gross benefit; distractor C understates X by mishandling the minutes-to-hours conversion (using 0.45 hours instead of 0.75). When you strategically communicate the business impact of data, being able to say "Y saves more in total, but X returns 25% more per pound" is exactly the framing that helps executives decide — and in a funding round with limited capital, the per-pound view usually governs.

**Question 11 (hard) — Sampling and confidence in a quality audit.**
You audit a 250,000-record dataset by sampling 2,000 records; 96 contain errors. The business asks: "So about how many records in the full dataset are wrong?" Which reply is the most accurate and honest?

A. "Exactly 12,000 records are wrong."
B. "Around 4.8% — roughly 12,000 records — subject to sampling uncertainty of about plus or minus 1 percentage point, so plausibly between about 9,500 and 14,500."
C. "96 records are wrong."
D. "We cannot say anything without checking all 250,000."

**Correct answer: B.**
**Explanation:** Sample error rate = 96 ÷ 2,000 = 4.8%. Scaled to the population: 4.8% × 250,000 = 12,000. But a sample estimate carries uncertainty: the standard error of a 4.8% proportion on n = 2,000 is √(0.048 × 0.952 ÷ 2000) ≈ 0.48 percentage points, so a 95% interval spans roughly ±0.94 points — about 3.9% to 5.7%, or 9,650 to 14,350 records; option B's rounded range is a fair plain-English rendering. Option A presents an estimate as an exact count — the kind of false precision you exist to challenge. Option C confuses the sample with the population; option D wrongly claims sampling tells us nothing. Communicating between the technical and non-technical means giving decision makers the estimate *and* its uncertainty in words they can use.

**Question 12 (hard) — Index numbers and real-terms budgets.**
Your data team's budget was £500,000 in 2023-24 and is £530,000 in 2025-26. The relevant deflator index rose from 100 to 109 over the same period. In real (2023-24) terms, what has happened to the budget?

A. Increased by 6% in real terms.
B. Increased by £30,000 in real terms.
C. Decreased by about 2.8% in real terms.
D. Unchanged in real terms.

**Correct answer: C.**
**Explanation:** Deflate the later budget to 2023-24 prices: £530,000 × (100 ÷ 109) ≈ £486,239. Real change = (£486,239 − £500,000) ÷ £500,000 ≈ −2.75%, a real-terms cut of about 2.8% despite the £30,000 cash increase. Distractors A and B report the nominal change; D assumes the cash uplift exactly offsets inflation (it would need to be £545,000 to do so). When you influence organisational decision making on the use of data, distinguishing cash from real terms is essential — a "budget increase" headline can mask a genuine reduction in what your team can deliver.

**Question 13 (hard) — Multi-source reconciliation.**
Three source systems feed your linked analytical dataset. This month: System 1 supplied 142,000 records of which 3.5% failed validation; System 2 supplied 88,500 records of which 2.0% failed; System 3 supplied 66,000 records of which 6.5% failed. Records failing validation are excluded from linkage. How many records entered linkage, and what was the overall exclusion rate?

A. 285,470 records; 3.7% excluded
B. 296,500 records; 4.0% excluded
C. 284,640 records; 4.0% excluded
D. 285,470 records; 4.2% excluded

**Correct answer: A.**
**Explanation:** Compute each system's failures separately, because the failure rates differ. System 1: 142,000 × 0.035 = 4,970 (split it as 142,000 × 0.03 = 4,260 plus 142,000 × 0.005 = 710 if that is easier under pressure). System 2: 88,500 × 0.02 = 1,770. System 3: 66,000 × 0.065 = 4,290. Total failures = 4,970 + 1,770 + 4,290 = 11,030. Total supplied = 142,000 + 88,500 + 66,000 = 296,500. Records entering linkage = 296,500 − 11,030 = 285,470. Overall exclusion rate = 11,030 ÷ 296,500 ≈ 3.72%, which rounds to 3.7%. Distractor B pairs the *supplied* total with a rate built from the naive average of the three failure rates ((3.5 + 2.0 + 6.5) ÷ 3 = 4.0%) — wrong twice over, because the systems contribute very different volumes and the low-failure System 1 is the largest; this is the same unweighted-average error as Question 4 in different clothing. Distractor C applies that flawed 4.0% rate to compute the surviving records; distractor D has the right count but a rate using only Systems 1 and 3. The habit this item rehearses is the reconciliation arithmetic behind the data quality standards you set: totals, exclusions, and rates must all derive from the same weighted calculation, and any published rate should be re-derivable from its published numerator and denominator.

**Question 14 (hard) — Interpreting a performance dashboard for a decision.**
A dashboard shows your four data products' quarterly figures. Product P: 4,200 active users, up 5% on last quarter, cost £30,000 per quarter. Product Q: 1,100 users, up 40%, cost £22,000. Product R: 6,800 users, down 3%, cost £41,000. Product S: 300 users, up 2%, cost £28,000. The executive committee will retire one product. On cost per active user and trajectory combined, which product is the strongest candidate for retirement?

A. Product P (£7.14 per user, growing)
B. Product Q (£20.00 per user, growing fast)
C. Product R (£6.03 per user, declining slightly)
D. Product S (£93.33 per user, near-flat)

**Correct answer: D.**
**Explanation:** Compute cost per active user: P = £30,000 ÷ 4,200 ≈ £7.14; Q = £22,000 ÷ 1,100 = £20.00; R = £41,000 ÷ 6,800 ≈ £6.03; S = £28,000 ÷ 300 ≈ £93.33. S costs four to fifteen times more per user than the others and its 2% growth offers no realistic path to efficiency. Q's £20 looks high, but 40% quarterly growth means its cost per user is falling rapidly — next quarter at similar cost and 1,540 users it would be about £14.29. R's slight decline merits investigation, not retirement, at the portfolio's best unit cost. The principal-level lesson: unit economics and trajectory together, not either alone, drive portfolio decisions — this is how you strategically communicate the business impact of data and lead decisions about where to pivot.

**Question 15 (hard) — Compound growth in demand forecasting.**
Requests to your data team have grown 8% per quarter for the past year and stand at 1,250 this quarter. Each request takes an average of 0.6 analyst-days, and your team has 14 analysts each with 55 productive days per quarter. If growth continues at 8% per quarter, in roughly how many quarters will demand exceed team capacity?

A. Demand already exceeds capacity.
B. About 1 quarter.
C. About 4 quarters.
D. About 9 quarters.

**Correct answer: B.**
**Explanation:** Capacity = 14 × 55 = 770 analyst-days per quarter. Current demand = 1,250 × 0.6 = 750 analyst-days — just under capacity, so option A fails (although the 97% utilisation should already alarm you). Next quarter's demand = 750 × 1.08 = 810 analyst-days, which exceeds 770 — so capacity is breached in about one quarter. Distractor C comes from comparing request *counts* (1,250) against capacity in *days* (770) and growing the wrong quantity; distractor D assumes linear growth of 8% of the original value each quarter and a much larger buffer. Two habits matter here: convert demand and capacity into the same unit (analyst-days) before comparing, and respect compounding — 8% quarterly is roughly 36% a year, not 32%. This is precisely the forward look you need when you influence organisational decision making on resourcing data analysis: the team that looks 97% "fine" today is over capacity within twelve weeks.

### Preparation tips

- **Refresh the core operations until they are reflexes.** Percentage change (always divide by the starting value), weighted averages (weight before you average), percentage points versus percent, and real versus nominal values cover most senior-level items. Ten minutes of drill a day for a week is transformative.
- **Practise with the calculator you will use.** An on-screen calculator handles differently from your desktop habits; rehearse chained calculations (e.g. 142,000 × 0.035, memory-plus, next term) so the mechanics never steal reasoning time.
- **Normalise units first.** Before any comparison, convert everything to the same unit — thousands, millions, hours, days, quarters. Most wrong answers in table questions are unit errors, not arithmetic errors.
- **Estimate before you calculate.** A rough order-of-magnitude estimate ("about 4% of 250,000 is about 10,000") catches keying errors instantly and often eliminates two options before you compute at all.
- **Write the method mentally as steps.** For multi-stage items, articulate the pipeline — extract, adjust, combine, compare — exactly as you would sketch a data transformation. It prevents skipped steps under pressure.
- **Bank easy marks first.** Scan for the single-step items and secure them; return to multi-stage forecasting problems with the confidence of points already earned. You review numbers like these for a living — trust that experience.

### Common pitfalls

- **Misreading chart and table labels.** Confusing monthly with quarterly data, or ignoring scale qualifiers like "in thousands" or "in millions", is the most common failure mode — Question 5 is built on it.
- **Averaging rates without weighting.** Whenever groups differ in size, the naive mean of their rates is wrong (Questions 4 and 13). Ask "what is the denominator?" before averaging anything.
- **Confusing percentage points with percentages.** A change from 84% to 91% is 7 points but 8.3% — assessors deliberately offer both (Question 7).
- **Using the wrong base for percentage change.** Dividing the change by the new value instead of the original value flatters or understates every comparison.
- **Over-calculating.** Performing precise long division when estimation or elimination would reveal the answer faster costs time you need elsewhere; several options usually die on inspection.
- **Time-sink questions.** One five-step forecasting item can consume the time of three simpler ones. Skip and return — the marks are usually equal.
- **Presenting sample estimates as exact counts.** As in Question 11, false precision is a numerical *and* a communication error; the test rewards the honestly-hedged option.


## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment evaluates how well you understand, analyse, and draw correct conclusions from written business information. It mirrors the exact reading demands of your role: dense passages drawn from policy documents, governance standards, official reports, and stakeholder correspondence, followed by questions that test whether a given statement is **True** (definitely follows from the passage), **False** (definitely contradicts the passage), or **Cannot Say** (the passage provides insufficient information either way), plus some multiple-choice comprehension items.

Two rules define the format. First, fact-based logic: you must answer based strictly on the text provided, deliberately setting aside your own expertise — a discipline that feels counter-intuitive for a principal who knows the real policy landscape well. Second, time pressure: tests typically allow less than a minute per question, simulating the reality of absorbing a briefing minutes before a meeting.

For your role the passages will feel familiar: data ethics and privacy policies, data management standards, publication protocols, project governance documents, and emails from directors and external partners. The skill under test is the precise reading that underpins everything you do — assessing and constructively challenging proposed data ethics policies, mediating between stakeholders who have each read the same document differently, and representing your community's position accurately in high-stakes forums. A principal who misreads "should" as "must", or treats a proposal as a decision, propagates that error across an entire organisation.

### What it measures for your role

- **Data ethics and privacy.** Passages modelled on ethics frameworks and privacy policies test whether you can extract exactly what a policy requires, permits, and stays silent on — the foundation of working with stakeholders to identify and address ethical and privacy concerns, and of constructively challenging proposed policies.
- **Data management.** Standards and governance texts test the rule-precise reading behind championing and leading data management and governance processes, and defining data management responsibilities.
- **Communicating between the technical and non-technical.** Comprehension items about tone, audience, and main message test the translation instinct you use when mediating between people and moderating difficult discussions about high-risk topics.
- **Managing a data project.** Project documentation passages test your ability to spot what a problem statement actually commits to — central to advising on problem statement development and ensuring standards are met.
- **Applying statistical and analytical tools and techniques.** Passages about methodology and quality assurance test whether you can distinguish what a report claims, assumes, and merely suggests — the reading half of overseeing the quality assurance of analytical outputs.
- **Data visualisation.** Text about visualisation and accessibility standards tests the careful reading behind setting and advocating new standards in inclusive, accessible data visualisation.

### Practice questions

**Passage A — Data ethics policy extract (for Questions 1-4).**
"All new data projects must complete an ethics self-assessment before any personal data is processed. Where the self-assessment identifies a high ethical risk, the project must be referred to the Data Ethics Board, which meets monthly. The Board may approve the project, approve it with conditions, or reject it. Projects using only anonymised or synthetic data are exempt from the self-assessment requirement, although teams are encouraged to complete one as good practice. The Board's decisions are published internally, except where publication would itself create a privacy risk. This policy does not apply to projects that began before 1 April, which remain governed by the previous framework until their next major change."

**Question 1 (easy).** True, False, or Cannot Say: "A new project using only synthetic data is required to complete an ethics self-assessment."

**Correct answer: False.**
**Explanation:** The passage states that projects using only anonymised or synthetic data "are exempt from the self-assessment requirement". Encouragement as good practice is not a requirement — the passage explicitly separates the two ("although teams are encouraged"). The statement asserts a requirement that the passage directly contradicts, so it is False, not Cannot Say.

**Question 2 (easy).** True, False, or Cannot Say: "The Data Ethics Board meets every week."

**Correct answer: False.**
**Explanation:** The passage says the Board "meets monthly". "Every week" directly contradicts this stated frequency. A careless reader might mark Cannot Say on the grounds that extra meetings are conceivable, but the test convention is that a direct factual statement in the passage ("meets monthly") makes a contradictory statement False. Answer from the text as written.

**Question 3 (moderate).** True, False, or Cannot Say: "Most projects referred to the Data Ethics Board are approved with conditions."

**Correct answer: Cannot Say.**
**Explanation:** The passage lists the Board's three possible outcomes — approve, approve with conditions, reject — but gives no information whatsoever about how often each occurs. "Most" is a frequency claim the text neither supports nor contradicts. This is the archetypal Cannot Say: plausible in the real world, completely undetermined by the passage. Your professional experience of ethics boards must not fill the gap — that is precisely the discipline this format tests.

**Question 4 (moderate).** True, False, or Cannot Say: "A project that began in March and has not undergone a major change is not required to complete the ethics self-assessment described in this policy."

**Correct answer: True.**
**Explanation:** The final sentence states the policy "does not apply to projects that began before 1 April... until their next major change". A project that began in March began before 1 April; with no major change yet, it remains under the previous framework, so this policy's self-assessment requirement does not apply to it. Note the careful chain: the conclusion follows from two explicit conditions joined exactly as the statement joins them. Whether the *previous* framework demands something similar is irrelevant — the statement is limited to "described in this policy".

**Passage B — Data management standard (for Questions 5-7).**
"Each information asset must have a designated data steward responsible for data quality within that asset. Data stewards must review their asset's quality metrics at least quarterly and must report any metric falling below its agreed threshold to the Data Governance Committee within ten working days of discovery. The Committee may commission a remediation plan, which the relevant data steward is responsible for delivering. Where a steward is responsible for more than five assets, the Chief Data Officer should consider appointing an additional steward. Training in quality metrics is mandatory for new stewards and refresher training is recommended every two years thereafter."

**Question 5 (moderate).** True, False, or Cannot Say: "If a steward oversees seven information assets, the Chief Data Officer must appoint an additional steward."

**Correct answer: False.**
**Explanation:** The passage says the CDO "should consider appointing" an additional steward — an obligation to *consider*, not to *appoint*. The statement upgrades "should consider" to "must appoint", which contradicts the text's carefully weaker wording. Modal verbs — must, should, may, should consider — are the load-bearing words of standards documents, and this distinction is exactly what you police when you define data management responsibilities and lead governance processes.

**Question 6 (moderate).** True, False, or Cannot Say: "A data steward who discovers a below-threshold metric on 1 May and reports it to the Data Governance Committee on 20 May has complied with the reporting requirement, assuming no public holidays and a Monday 1 May."

**Correct answer: False.**
**Explanation:** The requirement is reporting "within ten working days of discovery". From Monday 1 May, counting working days (Mon-Fri), ten working days end on Friday 12 May; even counting generously from the day after discovery, the deadline is Monday 15 May. A report on 20 May falls outside ten working days on any reasonable counting, so compliance fails. The item tests whether you convert calendar spans to working-day spans — a small numeracy step embedded in verbal material, common in senior-level tests and in real governance casework alike.

**Question 7 (hard).** True, False, or Cannot Say: "Refresher training in quality metrics is mandatory for all data stewards every two years."

**Correct answer: False.**
**Explanation:** The passage draws a precise distinction: training is "mandatory for new stewards" while refresher training is "recommended every two years thereafter". The statement asserts that the refresher is mandatory, contradicting "recommended". If you skim, "mandatory... training... every two years" all appear in the sentence and can blur together — the classic trap of proximity reading. Slow down on any sentence containing two different obligation levels; document drafters put them together exactly because the distinction matters, and so do test writers.


**Passage C — Email from a policy director (for Questions 8-10).**
"Thanks for your team's analysis of appeal outcomes. The findings are striking, and I would like to include the headline figure in next month's white paper. However, my officials tell me the underlying dataset excludes appeals lodged online, which they believe may account for around a third of the total volume. Before we publish anything, I need your view on whether the headline conclusion would survive the inclusion of online appeals. I should say the Permanent Secretary is keen that the white paper is evidence-led, and the drafting deadline is the 14th. If your team cannot re-run the analysis by then, we will need to caveat the figure heavily or drop it."

**Question 8 (moderate).** True, False, or Cannot Say: "The director has decided to drop the headline figure from the white paper."

**Correct answer: False.**
**Explanation:** The email presents a conditional decision tree, not a decision: publish if the conclusion survives, or "caveat the figure heavily or drop it" if the re-run cannot be done by the 14th. Dropping the figure is one branch of a contingency, and even then one of two stated alternatives. Reading a conditional as a settled outcome is one of the most common — and most consequential — misreadings in stakeholder correspondence, and the kind of thing you correct when managing stakeholder expectations.

**Question 9 (moderate).** True, False, or Cannot Say: "Online appeals account for around a third of total appeal volume."

**Correct answer: Cannot Say.**
**Explanation:** The email reports what the director's officials "believe may account for around a third" — a hedged, second-hand estimate, not an established fact. The passage gives no data confirming or refuting it. Note the two layers of hedging: "they believe" and "may". A statement of fact about the true proportion is therefore undetermined by this text. Treating stakeholder beliefs as verified facts is exactly what your quality-assurance instincts should flag, in tests and in practice.

**Question 10 (hard) — Multiple choice.** Which of the following best characterises what the director is asking the analyst team to provide before the 14th?

A. A complete re-analysis including online appeals, with no alternative acceptable.
B. A professional judgement on whether the headline conclusion is robust to including online appeals, with a re-run of the analysis if feasible within the deadline.
C. Permission to publish the original figure unaltered.
D. A recommendation on whether the white paper should be published.

**Correct answer: B.**
**Explanation:** The direct request is "I need your view on whether the headline conclusion would survive the inclusion of online appeals" — a judgement — followed by a conditional about re-running the analysis by the 14th, with fallbacks (caveat or drop) if not. Option A overstates: the email explicitly contemplates not re-running ("If your team cannot re-run..."). Option C inverts the email's caution. Option D inflates scope from one figure to the whole white paper. Extracting the *actual ask* from senior correspondence — neither more nor less — is the essence of communicating between the technical and non-technical at your level.

**Passage D — Accessibility standard for data visualisation (for Questions 11-12).**
"Published visualisations must not rely on colour as the only means of conveying information. All charts must include alternative text describing the main message, and interactive dashboards must be fully operable by keyboard. Where a chart cannot be made accessible, the same information must be provided in an accessible table. Teams should test visualisations with users of assistive technology at least once per release cycle. These requirements apply to all external publications; for internal management information they are strongly encouraged but assessed case by case."

**Question 11 (moderate).** True, False, or Cannot Say: "An internal management dashboard that is not keyboard-operable necessarily breaches this standard."

**Correct answer: False.**
**Explanation:** The final sentence limits the mandatory requirements to "all external publications"; for internal management information they are "strongly encouraged but assessed case by case". So an internal dashboard failing keyboard operability does not *necessarily* breach the standard — it may or may not, depending on the case-by-case assessment. The word "necessarily" in the statement is what makes it False rather than Cannot Say: the passage explicitly establishes that internal cases are not automatic breaches. As the person who sets and advocates for standards in inclusive, accessible data visualisation, you must know exactly where a standard's hard edge lies.

**Question 12 (hard).** True, False, or Cannot Say: "A published external chart that relies solely on red and green colouring to distinguish two trend lines, but which includes alternative text, complies with the standard."

**Correct answer: False.**
**Explanation:** The standard imposes multiple independent requirements. The first — "must not rely on colour as the only means of conveying information" — is breached by a chart that distinguishes its two lines solely by colour, regardless of red-green colour blindness considerations you might add from professional knowledge. Alternative text satisfies a *different* requirement; compliance with one clause does not cure breach of another. The test convention: a statement claiming compliance is False if the passage establishes any requirement the described artefact violates. Requirements in standards are conjunctive unless stated otherwise — the same reading you apply when assessing proposed policies.

**Passage E — Extract from a project problem statement (for Questions 13-15).**
"This project will identify the drivers of late submissions to the grant programme, quantify their relative contribution, and recommend interventions. It will use administrative data from the grants platform covering the last three complete financial years. The project will not evaluate the effectiveness of any interventions subsequently adopted, which would require a separate evaluation exercise. Success will be measured by the delivery of a prioritised, evidence-based list of interventions accepted by the programme board. The analysis phase is scheduled for eight weeks, subject to data access being granted by week two."

**Question 13 (easy).** True, False, or Cannot Say: "The project will evaluate whether the recommended interventions worked."

**Correct answer: False.**
**Explanation:** The passage states this explicitly and in terms: "The project will not evaluate the effectiveness of any interventions subsequently adopted". The statement directly contradicts a sentence of the passage. Scope exclusions are drafted precisely so that nobody later claims the work promised something it did not — when you advise on problem statement development, the "will not" sentences are as important as the "will" sentences.

**Question 14 (moderate).** True, False, or Cannot Say: "The analysis will use survey data collected from grant applicants."

**Correct answer: Cannot Say.**
**Explanation:** The passage says the project "will use administrative data from the grants platform". It does not say this is the *only* data source, nor does it mention surveys at all. The statement is neither confirmed (no survey is mentioned) nor contradicted (the passage never says "only administrative data"). This is a subtle Cannot Say: the temptation is to answer False because surveys are unmentioned, but absence of mention is not denial. Contrast with Question 13, where the passage contains an explicit negative.

**Question 15 (hard).** True, False, or Cannot Say: "If data access is granted in week three, the eight-week analysis schedule no longer applies as stated."

**Correct answer: True.**
**Explanation:** The schedule is "subject to data access being granted by week two". "Subject to" makes the eight-week commitment conditional on that event; access arriving in week three means the stated condition is unmet, so the schedule *as stated* — an unconditional eight weeks — no longer holds. Note what does not follow: the passage does not say the project fails or the schedule lengthens by any particular amount, only that the stated commitment was conditioned on week-two access. The statement is carefully worded to claim exactly what the condition implies, no more — which is why it is True rather than Cannot Say. Conditional commitments are the connective tissue of project governance documents, and reading them precisely is how you keep stakeholder expectations honest.

**Passage F — Methodology note from a statistical report (for Questions 16-18).**
"Estimates in this release are derived from a matched sample of administrative records. Records were matched using a deterministic algorithm; where deterministic matching failed, probabilistic matching was applied with a threshold chosen to keep the estimated false-match rate below 0.5%. Around 6% of records could not be matched by either method and are excluded from all estimates. Analysis of excluded records suggests they are disproportionately drawn from the youngest age groups, and users should exercise caution when interpreting estimates for those groups. Comparisons with the previous release are affected by an improvement to the matching algorithm; a consistent back series is provided in Table 7. All figures are provisional and subject to revision when the annual reconciliation is completed."

**Question 16 (moderate).** True, False, or Cannot Say: "The false-match rate of the probabilistic matching was 0.5%."

**Correct answer: False.**
**Explanation:** The passage says the threshold was "chosen to keep the estimated false-match rate below 0.5%". The statement asserts equality with 0.5%, but the text establishes the rate was *below* that bound — a bound is not a value. Additionally, the passage describes an *estimated* rate, while the statement asserts the rate itself. Either mismatch alone is enough to make the statement unsupported; the explicit "below" makes it contradicted, hence False. Thresholds, bounds, and point values are distinct objects — a distinction you enforce daily when quality-assuring statistical outputs.

**Question 17 (moderate).** True, False, or Cannot Say: "Estimates for the youngest age groups are less reliable than estimates for other age groups."

**Correct answer: Cannot Say.**
**Explanation:** The passage says excluded records are "disproportionately drawn from the youngest age groups" and that users "should exercise caution" with those estimates. That is a warning about potential bias, not a determination of relative reliability — the passage never compares reliability across groups directly, and caution-worthy is not the same as established-as-less-reliable. The statement goes one inferential step beyond the text. It is a tempting True for any statistician, which is precisely the point: the format tests whether you can hold your own valid professional inference apart from what the document actually asserts.

**Question 18 (hard) — Multiple choice.** A colleague wants to compare this release's headline figure directly with the figure published in the previous release. According to the passage, what should you advise?

A. The comparison is straightforward because both figures come from the same administrative source.
B. The comparison is affected by a matching-algorithm improvement, so they should use the consistent back series in Table 7 rather than comparing published headlines directly.
C. No comparison is possible until the annual reconciliation is completed.
D. The comparison is valid provided the 6% of unmatched records are added back in.

**Correct answer: B.**
**Explanation:** The passage states that "comparisons with the previous release are affected by an improvement to the matching algorithm" and immediately offers the remedy: "a consistent back series is provided in Table 7". Option B reproduces exactly this advice. Option A ignores the stated discontinuity. Option C over-reads "provisional and subject to revision" — provisionality qualifies the figures' finality, but the passage does not prohibit comparison, and it explicitly provides a tool for making one. Option D invents a remedy the passage never mentions and which is methodologically incoherent (unmatched records cannot simply be "added back"). Advising colleagues on exactly this kind of question — what a methodology note licenses and forbids — is part of representing good analytical practice across your organisation.

### Preparation tips

- **Practise the discipline of the text-only world.** Your greatest asset — deep domain knowledge — is the format's greatest trap. Before answering, ask: "Where in the passage is this stated?" If you cannot point to the words, the answer is likely Cannot Say, however confident your professional instinct.
- **Build a modal-verb radar.** Must, should, may, "should consider", "are encouraged", "is recommended" — rank them consciously as you read. Most senior-level items turn on obligation strength (Questions 5 and 7).
- **Distinguish the three verdicts sharply.** True needs positive support in the text; False needs contradiction by the text; Cannot Say covers everything else. "Plausible but unstated" is Cannot Say (Questions 3, 9, 14); "explicitly negated" is False (Question 13).
- **Scan, then verify.** With under a minute per question, read the statement first, then scan the passage for the relevant clause and read *that* clause slowly. Reading the whole passage deeply before seeing any question spends your time where the marks are not.
- **Watch quantifiers and absolutes.** "All", "only", "most", "necessarily", "always" transform a statement's truth conditions (Questions 3 and 11). One absolute word can flip True to Cannot Say.
- **Rehearse with real documents.** Take a data ethics policy or governance standard you know, write five True/False/Cannot Say statements about it, and justify each from the text alone. Ten minutes of this daily for a week sharpens exactly the muscle the test measures — and improves your policy-review practice as a bonus.

### Common pitfalls

- **Making assumptions from professional knowledge.** Bringing in what you know about GDPR, ethics boards, or accessibility law instead of relying only on the passage is the number-one failure mode for experienced candidates — the test deliberately rewards suspension of expertise.
- **Confusing "likely" with "certain".** A passage saying officials "believe" something "may" be true does not establish it as fact (Question 9); conversely, a statement hedged in the passage cannot support an absolute claim.
- **Treating absence of mention as denial.** Unmentioned is not contradicted: that is Cannot Say, not False (Question 14).
- **Proximity reading.** Letting words from neighbouring clauses blur together — "mandatory" from one clause attaching to "refresher training" from the next (Question 7). Slow down whenever one sentence contains two obligation levels.
- **Reading conditionals as decisions.** "If X, we will do Y" commits to nothing until X occurs (Questions 8 and 15).
- **Poor time management.** Spending too long reading each passage in full before scanning for the statement's keywords; at under a minute a question, targeted scanning is not a shortcut, it is the method.


## Workplace job-specific situational judgement assessment

### About this assessment

A workplace job-specific situational judgement assessment evaluates your decision-making, interpersonal skill, and professional conduct through realistic workplace dilemmas. Unlike logic or numerical tests, there is no formula to apply: each scenario presents a short, plausible conflict or challenge, and you evaluate a set of possible responses. There is deliberately no single objectively "right" answer — several options may seem reasonable — but one typically fits the role's responsibilities and the organisation's values best. Response formats usually ask you to select the **most effective** and **least effective** actions, or to rank or rate all options from best to worst. Timing is generous or absent, because the assessment measures natural judgement rather than speed.

For a principal data analyst in UK government, the scenarios will involve your real stakeholder landscape: directors wanting figures faster than quality allows, junior analysts you mentor making honest mistakes, policy teams proposing ethically questionable data uses, cross-government communities you represent, and delivery pressures that strain governance. Strong answers consistently express UK public sector values — evidence-led decision making, transparency, user needs, accessibility and inclusion, collaboration across professions, and proportionate, honest handling of risk. Strong answers at *principal* level additionally show leadership: addressing root causes rather than symptoms, developing people rather than bypassing them, and protecting long-term trust over short-term convenience.

### What it measures for your role

- **Communicating between the technical and non-technical.** Scenarios test whether you mediate between people, adopt the right communication method for each stakeholder, manage expectations, and moderate difficult discussions about high-risk topics within constrained timescales.
- **Data ethics and privacy.** Dilemmas probe whether you identify and address ethical and privacy concerns with stakeholders, and constructively challenge proposed uses of data rather than either rubber-stamping or obstructing them.
- **Data management.** Situations involving governance breaches and quality failures test how you champion data management processes while keeping delivery moving.
- **Managing a data project.** Scenarios about scope, risk, and stakeholder relationships test your oversight of the project life cycle and your development of stakeholder relationships for your team's projects.
- **Delivering business impact through data.** Options are often separated by whether they serve organisational objectives or merely local convenience — the judgement behind deciding when to pivot and championing the role of data.
- **Applying statistical and analytical tools and techniques.** Several dilemmas turn on defending analytical quality under pressure — the behavioural face of overseeing quality assurance.
- **Leadership duties of your level.** Influencing organisational decision making, overseeing continuous improvement, mentoring, and representing the data analyst community all appear as scenario material.

### Practice questions

**Question 1 (moderate) — The director wants the number today.**
A director calls you at 16:00. She needs a single headline figure — the percentage of service users affected by a proposed change — for a ministerial meeting at 09:30 tomorrow. Your team has a draft figure, but it has not completed your quality assurance process, and last month a similar unchecked figure had to be corrected after release. Rate the options.

A. Provide the draft figure now, without comment, to be helpful under deadline.
B. Refuse: explain that nothing leaves the team before full QA, and the QA queue means Thursday.
C. Explain the figure's status, run a rapid proportionate check on the single figure this evening, and provide it with a clear confidence statement and any necessary caveat in writing by 08:30.
D. Suggest the director use last year's published figure instead, since it is already assured.

**Most effective: C. Least effective: A.**
**Explanation:** Option C serves the real need (a defensible figure for a ministerial discussion) while managing risk proportionately: QA effort scales to a single number overnight, and the written caveat protects both the director and the evidence base — this is managing stakeholder expectations and moderating high-risk discussions within constrained timescales, exactly as your role profile describes. Option A is least effective: it repeats last month's known failure mode, transfers unquantified risk to a minister, and surrenders your quality assurance duty precisely when it matters most. Option B treats process as an end in itself and fails the organisation at its moment of need — governance exists to make evidence trustworthy, not unavailable. Option D is honest but may answer the wrong question; an out-of-date figure can mislead as surely as an unchecked one, though as a stopgap it is less damaging than A.

**Question 2 (moderate) — A junior analyst's public mistake.**
A junior analyst on your team discovers they made a coding error in a statistical release published three weeks ago: a filter excluded one region, understating the national total by about 2%. They come to you anxious, having told no one else. Rate the options.

A. Thank them for coming forward, initiate your organisation's published-error correction process immediately, inform the release's owner and users transparently, and afterwards review with the team how the error escaped QA — treating it as a process failure, not a personal one.
B. Quietly fix the code so future releases are correct, but leave the published release alone since 2% is within normal revision ranges.
C. Correct the release but avoid naming any cause publicly, and privately note the analyst's error in their next performance review.
D. Escalate to your director first and take no other action until instructed.

**Most effective: A. Least effective: B.**
**Explanation:** Option A does everything the situation requires: correction, transparency to users (a core public sector value — people may have made decisions on the wrong number), protection of the person who spoke up, and continuous improvement of the process — your duty to oversee quality assurance and improve practices. Option B is least effective: it knowingly leaves a wrong statistic in the public domain, corrodes trust if discovered, and teaches your team that concealment is acceptable — the opposite of the culture a principal must build. Option C corrects the number but punishes the messenger, guaranteeing the next error stays hidden; blame-centred responses destroy the psychological safety that quality depends on. Option D is not wrong to involve the director, but making it the *only* action delays a correction you already have authority and duty to begin; a principal informs upwards while acting, not instead of acting.

**Question 3 (hard) — The ethically questionable data request.**
A policy team asks your team to link benefits data with library-membership data to identify individuals "unlikely to be engaging with services", so the individuals can be contacted proactively. The policy intent is genuinely supportive, but the request troubles you: the purposes seem incompatible with what citizens were told when their data was collected, and no ethics assessment has been done. The policy lead says the deadline is tight and asks you to start the linkage while the paperwork catches up. Rate the options.

A. Start the linkage as asked; the intent is benign and the paperwork is a formality.
B. Decline to start, explain specifically why — purpose compatibility and the missing ethics assessment — and offer to help the policy team complete the ethics self-assessment rapidly and explore designs that could achieve the policy aim with less intrusion, such as aggregate-level targeting.
C. Refuse outright and report the policy team to the information governance team for attempting to bypass process.
D. Start preparing the datasets separately (without linking) so no time is lost, while the ethics assessment is completed.

**Most effective: B. Least effective: A.**
**Explanation:** Option B embodies your data ethics and privacy skill at principal level: identify and address the concern with the stakeholder, explain how the ethical issue fits the wider organisational context, and constructively challenge — while staying in partnership with the policy aim and offering a route to yes. Note that B also demonstrates the professional maturity to distinguish the *aim* (legitimate) from the *method* (premature). Option A is least effective: "start now, paperwork later" inverts the entire purpose of ethical assessment, and benign intent does not cure incompatible purpose — if the assessment later finds the linkage unjustifiable, the intrusion has already happened. Option C treats a collaborative stakeholder as an adversary; escalation may become appropriate, but as a first move it destroys the relationship your role depends on and teaches policy teams to avoid consulting data professionals. Option D sounds like a pragmatic middle path but pre-commits resources and momentum to an approach that may be rejected, and "preparing" datasets for an unapproved purpose already processes personal data for that purpose — a subtler version of A.

**Question 4 (moderate) — Two teams, one truth.**
Two directorates publish dashboards showing "active users" of the same service, using different definitions: one counts monthly logins, the other counts completed transactions. A board member has noticed the figures differ by 40% and asks you, as the senior data professional, "which number is right?". Rate the options.

A. Explain that both are right by their own definitions, and leave the directorates to continue as they are since each definition suits its own purpose.
B. Recommend the board adopt whichever figure is larger, since it better demonstrates the service's reach.
C. Explain why the figures differ, then lead the two directorates to an agreed shared definition (or an agreed pair of clearly-labelled measures) recorded in a common data dictionary, so the organisation reports consistently from now on.
D. Ask the two directorates to reconcile the numbers themselves and report back to the board.

**Most effective: C. Least effective: B.**
**Explanation:** Option C answers the immediate question honestly *and* fixes the systemic cause: undefined shared language. Leading the organisation to common definitions is data management leadership — championing governance processes and enabling continuous improvement — and it converts a moment of board-level embarrassment into a durable asset (the data dictionary). Option B is least effective and fails integrity outright: choosing figures for advocacy value rather than accuracy is precisely what a principal exists to prevent, and a board that later discovers the choice will discount everything your profession publishes. Option A is analytically correct but abdicates leadership; "both are right" without convergence guarantees the same confusion at the next board. Option D delegates a coordination problem that has already failed to self-resolve — the directorates produced the divergence; resolving it needs the neutral authority you carry.

**Question 5 (hard) — The struggling high-performer you mentor.**
A talented senior analyst you mentor has led the data modelling on a high-profile project. In review, you find their new analytical data model contains a design flaw: it hard-codes assumptions that will break when a key source system migrates next year. The analyst has already presented the model to stakeholders as finished, and correcting it means visibly reopening "completed" work. The analyst asks you to let it stand, promising to fix it quietly during the migration. Rate the options.

A. Agree — the flaw is not currently causing errors, the analyst is trusted, and morale matters.
B. Overrule them and assign the redesign to a different analyst to ensure objectivity.
C. Require the correction now, but coach the analyst through leading it themselves: help them frame the change to stakeholders as a strengthening found in review, and use the episode to teach how models are designed for known future change.
D. Let the model stand but document your objection in writing so responsibility is clear.

**Most effective: C. Least effective: D.**
**Explanation:** Option C fixes the artefact, develops the person, and models the standard: your role profile makes you responsible for ensuring data models align with modelling standards *and* for mentoring others in data quality and modelling — C is the only option that does both. Reframing review findings as strengthening (which they are) also teaches the analyst that revisiting work is professional, not shameful. Option A knowingly ships a model that will break on a foreseeable event; "fix it quietly later" defers the cost to the moment of maximum disruption (mid-migration) and normalises concealment. Option B fixes the model but at the price of publicly stripping the analyst of their work — a mentoring failure that teaches your best people that honesty about flaws means losing ownership. Option D is least effective because it is self-protection dressed as governance: the organisation still gets the broken model, the analyst still learns evasion works, and the written objection helps no one but its author. A principal's job is to prevent foreseeable failures, not to be provably blameless when they occur.

**Question 6 (moderate) — Representing the profession under fire.**
At a cross-government event, a senior official from another department states in open session that "data analysts slow everything down with quality theatre — policy teams should just use the numbers they have". You are on the panel representing the data analyst community. Rate the options.

A. Respond with a concrete, brief story of a decision improved (or a costly error prevented) by proportionate quality assurance, acknowledge that assurance must be proportionate to the decision at hand, and offer to continue the conversation with their department afterwards.
B. Rebut firmly with a list of the official's department's recent data errors to demonstrate why assurance is needed.
C. Let the comment pass to keep the panel collegial, and raise it privately later.
D. Agree that assurance is often disproportionate and commit publicly to lighter-touch processes across government.

**Most effective: A. Least effective: B.**
**Explanation:** Option A does what representing the community to large audiences requires: it defends the profession's value with evidence rather than assertion, concedes the legitimate kernel in the criticism (proportionality — a real principle of good assurance), and converts a public challenge into a working relationship. Option B is least effective: publicly humiliating another department wins the exchange and loses the relationship, confirms the "adversarial analyst" stereotype, and will follow you into every future cross-government negotiation. Option C leaves a false characterisation standing before an audience of exactly the people whose cooperation your community needs — silence reads as concession when you hold the community's brief. Option D capitulates: it trades away standards you are appointed to uphold for momentary approval, and commits the whole profession without mandate. The panel format is the point: at principal level you are tested on judgement *in public*, where both aggression and appeasement carry lasting costs.


**Question 7 (hard) — Pivot or persevere.**
Four months into a six-month project to build a predictive model for service demand, interim results show the model performs only marginally better than the simple baseline already in use, though it is far more complex to maintain. The team is invested and believes two more months could improve it. The sponsoring director has been enthusiastically telling colleagues about "the AI project". Meanwhile, the same team's exploratory work has revealed a data quality problem whose fix would demonstrably improve operational decisions within weeks. Rank the options from most to least effective.

A. Continue the model build as planned; changing course now would embarrass the sponsor.
B. Present the sponsor with the interim evidence, the honest probability that two more months yields marginal gains, and the alternative of redirecting effort to the data quality fix — with a recommendation to pivot and a plan for communicating the change constructively.
C. Pivot the team to the data quality work immediately and inform the sponsor at the next scheduled monthly meeting.
D. Split the team in half to pursue both workstreams simultaneously.

**Most effective ranking: B, D, C, A.**
**Explanation:** Option B is the textbook expression of partnering with others to decide when to pivot for business impact: evidence first, sponsor engaged as a partner in the decision, and the reputational dimension managed openly rather than driving the decision covertly. Option D is second — it hedges and dilutes, and two half-teams often deliver less than one focused team, but it is at least honest and keeps both options alive pending a fuller decision. Option C ranks third: the pivot itself may well be right, but executing it before telling the sponsor converts a defensible evidence-led decision into a trust breach — sponsors forgive changed plans far more readily than surprises, and "influence organisational decision making" means bringing decision makers with you, not presenting them with faits accomplis. Option A is least effective: it knowingly spends two months of public money on work the evidence says is marginal, to protect a narrative — the exact inversion of evidence-led government. Sunk cost plus sponsor embarrassment is the most common real-world reason bad projects continue; assessors include this option to see whether you recognise it as a reason to communicate carefully, not a reason to continue.

**Question 8 (moderate) — The inaccessible flagship dashboard.**
Your organisation's flagship performance dashboard, built by a contractor and championed by your directorate, wins internal praise. A colleague who uses a screen reader tells you privately that it is unusable with assistive technology, and they have stopped raising it "because nobody acts". External publication is planned next month. Rate the options.

A. Thank the colleague, verify the issues, and require an accessibility remediation plan (and interim accessible alternative, such as a structured data table) as a condition of external publication — using your standards-setting role to make assistive-technology testing a standing requirement for all future releases.
B. Log the issue in the backlog for the contractor's next development cycle after publication, since the deadline is fixed.
C. Advise the colleague to raise a formal complaint through the proper channel so the issue is officially recorded.
D. Delay publication indefinitely until the dashboard is fully rebuilt to be accessible.

**Most effective: A. Least effective: B.**
**Explanation:** Option A treats accessibility as what it is — a requirement, not a preference — while remaining proportionate: an interim accessible alternative can make publication viable, the remediation plan fixes the product, and the standing testing requirement addresses the systemic failure your colleague described ("nobody acts"). This is your data visualisation duty in action: setting and advocating for standards in inclusive, accessible visualisation. Option B is least effective: publishing externally a product known to exclude disabled users is a legal risk (public sector accessibility regulations), a values failure, and a personal signal to your colleague that raising issues is indeed pointless. Option C outsources to the person with least power what you have most power to fix, and formalises a relationship problem you could resolve by acting. Option D over-corrects: it treats the issue as binary when interim alternatives exist, and indefinite delay punishes the organisation without a plan — proportionate remediation with a firm condition beats both extremes.

**Question 9 (moderate) — Conflicting demands on your team's roadmap.**
Three stakeholders each insist their need tops your team's next quarter: the finance director wants automated monthly reporting (moderate value, low effort); an operations head wants a demand-forecasting analysis (high value, high effort); a policy team wants exploratory analysis for a bill in parliament next quarter (uncertain value, hard deadline, modest effort). Your team can deliver at most two. Rate the options.

A. Take all three and ask the team to stretch; disappointing a stakeholder damages relationships.
B. Choose the two with clearest value — finance and operations — and tell the policy team their timing is unfortunate.
C. Assess the three against organisational priorities and deadline rigidity; propose delivering the parliamentary analysis (immovable deadline, modest effort) and the finance automation (quick, frees future capacity), while scheduling the forecasting work next quarter with the operations head involved in that decision — then communicate the rationale to all three together.
D. Ask your director to choose, since stakeholder prioritisation is above your team's remit.

**Most effective: C. Least effective: A.**
**Explanation:** Option C reasons rather than reacts: the parliamentary deadline is genuinely immovable (parliament does not reschedule for analytical capacity) and the effort is modest; the finance automation is cheap and *creates* capacity; the high-effort forecasting work is valuable but schedulable — and involving the deferred stakeholder in the scheduling preserves the relationship. Communicating one rationale to all three treats them as adults and demonstrates the transparent prioritisation your role models. Option A is least effective: over-commitment is the dishonest option that feels polite — it converts one difficult conversation now into three broken promises later, and burns out the team you lead. Option B applies a defensible value lens but ignores deadline rigidity (the policy window closes permanently) and delivers the news without partnership. Option D delegates upwards a judgement squarely within a principal's remit — advising on prioritisation of data work *is* influencing organisational decision making; escalation is for genuine ties on organisational priority, after your analysis, with your recommendation attached.

**Question 10 (hard) — The community you represent disagrees with you.**
You are leading the adoption of a new organisation-wide standard for reproducible analytical pipelines. In the data analyst community of practice — which you chair and represent — a vocal group of experienced analysts argues the standard is bureaucratic overreach and is quietly encouraging teams to ignore it. You believe the standard is right, and its adoption is part of your objectives. Rate the options.

A. Use your position to instruct teams to comply, and remove the dissenting analysts from community leadership roles.
B. Host a structured session where the dissenters present their objections concretely; adjust the standard where their criticisms identify genuine disproportion, publish what changed and what did not with reasons, and ask the community's respected sceptics to co-own the revised rollout.
C. Bypass the community and secure a mandate from the executive committee making the standard compulsory.
D. Pause the standard indefinitely until the community reaches consensus.

**Most effective: B. Least effective: A.**
**Explanation:** Option B reflects how standards actually take hold: through legitimacy. Experienced dissenters usually hold real information — about disproportionate burden on small jobs, missing tooling, unrealistic timelines — and harvesting it improves the standard (continuous improvement of practices is literally your duty); publishing what changed *and what did not, with reasons* shows challenge is heard without pretending it always wins; converting credible sceptics into co-owners is the oldest and best adoption strategy. Option A is least effective: it uses positional power to suppress professional dissent inside the very community you exist to represent — compliance will be performative, the community's trust in its representative collapses, and your best analysts disengage or leave. Option C wins the mandate and loses the profession: an executive edict against the community's visible opposition makes the standard "management's rule", ensuring minimum compliance forever; it also advertises that you could not carry your own community. Option D mistakes consensus for legitimacy — full consensus among strong-minded experts may never come, and indefinite pause abandons an improvement you believe in; leadership sometimes means deciding after genuine consultation, not instead of it.

**Question 11 (moderate) — The overheard shortcut.**
You learn that a team elsewhere in the organisation is regularly emailing spreadsheets of case-level personal data to an external evaluation partner, because "the secure transfer system is too slow". The team does not report to you, and their head of profession is a peer of yours. Rate the options.

A. Since the team is outside your line, note it and take no action — their management chain owns their risks.
B. Contact your peer directly and promptly: describe what you have learned without accusation, ensure the transfers stop immediately, ensure the incident is assessed under the organisation's data-incident process (which may involve mandatory reporting), and jointly sponsor a fix for the underlying cause — the unusable secure transfer route.
C. Report the team anonymously to the data protection officer and let the formal process run its course.
D. Email the team directly instructing them to stop, copying their entire management chain.

**Most effective: B. Least effective: A.**
**Explanation:** Option B does the three things the situation demands, in the right order: stops ongoing harm fast (peer-to-peer contact is the quickest credible route), ensures proper incident handling (personal data sent insecurely and repeatedly may meet reporting thresholds — that assessment is not optional and not yours to waive), and fixes the root cause, because a security control that is too slow to use is a defect that will breed workarounds forever — champion data management and governance across your organisation means across, not just within, your line. Option A is least effective: data protection failures do not respect organisational charts, you now know about ongoing risk to citizens' data, and "not my team" is indefensible for the organisation's senior data professional — knowledge creates responsibility at this level. Option C ensures the issue is eventually handled but chooses the slowest honest route while transfers continue, and anonymity spends none of your standing to accelerate the fix. Option D stops the practice but by publicly humiliating a peer team you do not manage — creating a profession-level rift and teaching teams to hide workarounds from you, when workarounds surfacing early is exactly what good governance culture produces.

**Question 12 (hard) — Quality versus the legislative clock.**
Analysis your team produced will underpin a regulatory impact assessment laid before parliament next week. At the final check, you find the central estimate is sound but a supporting sensitivity analysis contains an error: fixing it will likely move one secondary figure by an unknown amount, and the fix needs four days you barely have. The policy team suggests publishing as-is and correcting quietly in a future version "if anyone asks". Rate the options.

A. Publish as-is; the central estimate is sound and the error is secondary.
B. Fix the error before laying, informing the policy team and, through them, the responsible senior owner of the timing risk, so the choice between a short delay and a corrected-on-time document is made explicitly at the right level with full information.
C. Publish as-is but proactively disclose the known error and its expected correction in the document itself.
D. Publish as-is and adopt the policy team's plan to correct it quietly later if raised.

**Most effective: B. Least effective: D.**
**Explanation:** Work through what each option does with the four days. Option B uses them to fix the error while ensuring the schedule-versus-accuracy trade-off is decided by those accountable for the parliamentary timetable — with full information. It may still end in publishing with disclosure, but that becomes an informed decision, not a default. Option D is least effective — note it is materially worse than C, which looks similar: D's "quietly, if anyone asks" is concealment of a *known* error in evidence before parliament, the most serious transparency failure available here; discovery would damage not just this assessment but the credibility of your organisation's evidence generally. Option C at least meets the transparency standard — a known limitation, disclosed — and in genuine immovable-deadline cases disclosure is the honest fallback; it ranks second or third depending on whether four days truly exist. Option A publishes a known error silently through negligence framing ("secondary") rather than active concealment, barely better than D. The principal-level discrimination assessors seek: B versus C turns on using available time; C versus D turns on disclosure — and disclosure is never optional once an error is known.

### Preparation tips

- **Anchor in the values, not in cleverness.** UK public sector scenarios reward transparency, user focus, evidence-led decisions, accessibility, and collaboration. When torn between options, ask which one you could explain comfortably to a select committee, a service user, and your own team — the option that survives all three audiences is usually the credited one.
- **Look for the option that fixes the system, not just the incident.** At principal level, credited answers typically pair the immediate remedy with the process improvement (Questions 2, 4, 8, 11). An option that only firefights is usually ranked below one that also prevents recurrence.
- **Respect the people in the scenario.** Options that develop, protect, or partner with colleagues generally outrank options that bypass, expose, or punish them — even when the bypass is faster (Questions 5, 10, 11).
- **Neither rubber-stamp nor obstruct.** For ethics and governance dilemmas, the credited option is almost always constructive challenge with a route to yes (Question 3): pure refusal and pure compliance both usually rank poorly.
- **Read the response format carefully.** "Most and least effective" questions score two judgements; ranking questions score the full ordering. In rating formats, judge each option on its own merits rather than relative to your favourite.
- **Rehearse honestly, not aspirationally.** Answer as you would genuinely act; assessors and validity studies detect impression management, and coached "perfect" answers often misjudge which option is credited. Your years of real stakeholder judgement are the preparation — these scenarios are your working week in miniature.

### Common pitfalls

- **Answering idealistically rather than effectively.** "Stop everything until it is perfect" options (Questions 1B, 8D) sound principled but fail the organisation practically; credited options are principled *and* workable.
- **Selecting passive options.** Choices that delay action, defer wholly to others, or merely document concerns (Questions 2D, 5D, 9D) consistently rank low — principals are scored on acting with judgement, not on being provably blameless.
- **Protecting relationships by avoiding truth.** Over-commitment (Question 9A), letting false statements stand (Question 6C), and quiet non-correction (Question 2B) all trade long-term trust for short-term comfort; assessors rank them harshly.
- **Escalating as a first resort.** Involving seniors is often right, but options where escalation *replaces* your own available action (Questions 2D, 9D) score poorly; inform upwards while acting within your authority.
- **Punishing honesty.** Any option that penalises a person for surfacing a problem (Questions 2C, 5B) damages the reporting culture your role depends on and is almost never credited.
- **Ignoring the public sector context.** Options acceptable in a commercial setting — choosing the flattering figure (Question 4B), quiet corrections (Question 12D) — are disqualifying where parliament, ministers, and citizens rely on the numbers.


## Conclusion

You have now worked through a complete set of psychometric preparation materials built around your role: a cognitive assessment testing the pattern recognition, deduction, error checking, and prioritisation you apply to data models, pipelines, and portfolios; a numeric reasoning assessment covering the percentages, weighted averages, budgets, forecasts, and unit economics you steward; a verbal reasoning assessment grounded in the ethics policies, governance standards, and stakeholder correspondence you read with a professional's precision; and a situational judgement assessment drawn from the genuine dilemmas of leading data analysis in UK government — quality under deadline pressure, ethical challenge, mentoring, standards adoption, and representing your profession in public.

If one theme runs through all four sections, it is this: the assessments are not testing something foreign to you. They are distilled versions of your working week. Every explanation in this document has pointed back to the same skills your role profile names — quality-assuring statistical outputs, communicating between the technical and non-technical, championing data ethics and governance, modelling and preparing data well, delivering business impact, and managing projects and people with honesty and judgement. Preparation, therefore, is less about learning new material and more about practising your existing judgement in a distilled, timed, text-only format.

For next steps: revisit the questions you found hardest and re-derive the answers aloud — articulating the reasoning is what converts practice into durable skill, and it doubles as coaching material for the analysts you mentor. Keep the daily habits small and steady: ten minutes of percentage and weighted-average drills, one policy passage read with True / False / Cannot Say discipline, one real dilemma from your week examined against the values that decide situational judgement scoring. If you can, practise one full section under realistic timing before any real assessment.

However your next assessment goes, treat it as a snapshot, not a verdict. You lead significant areas of work in a profession that grows through exactly the reflective practice you have just done. Keep investing in it, keep sharing it with your community, and go into the assessment confident that the capabilities being measured are ones you exercise, at scale, every day. Good luck — you are better prepared than you think.
