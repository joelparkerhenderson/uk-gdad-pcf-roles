# Data Architect (Chief Data Architect) - Psychometric Assessment Resources

## Introduction

Welcome. This document is a practical, encouraging companion for you as a chief data architect preparing for workplace psychometric assessments. Whether you are preparing for a formal selection process, a development centre, a talent review, or simply want to sharpen the mental disciplines that underpin your work, this resource is written for you and calibrated to the seniority and breadth of your role.

Psychometric assessments are structured, standardised exercises that measure the mental capabilities and behavioural judgement that predict performance in a specific role. At your level, they are rarely about raw speed of calculation or trivia. Instead, they probe the capabilities that distinguish an effective chief data architect: the ability to see patterns across multiple data models and organisational domains, to reason rigorously about governance and risk, to interpret dense policy and standards documentation with precision, to work confidently with budgets, capacity figures, and assurance metrics, and to exercise sound judgement in politically sensitive, cross-government situations where the stakes are high and the audiences are senior.

This document covers four assessment types, each in its own section:

1. A workplace job-specific cognitive ability assessment, testing pattern recognition, logical deduction, error checking, prioritisation, and problem solving using the artefacts you genuinely handle - data models, metadata repositories, assurance reports, and architecture standards.
2. A workplace job-specific numeric reasoning assessment, testing your interpretation of tables, percentages, ratios, budgets, and performance metrics drawn from realistic data architecture and governance contexts.
3. A workplace job-specific verbal reasoning assessment, testing your precise comprehension of the dense written material your role lives in - data strategies, standards, governance policies, ministerial correspondence, and cross-government agreements.
4. A workplace job-specific situational judgement assessment, testing how you navigate the real dilemmas of senior data leadership - stakeholder conflict, assurance failures, innovation timing, and community leadership.

Each section explains what the assessment measures, maps it explicitly to the skills in your role profile, provides substantial practice questions with worked answers, and closes with preparation tips and common pitfalls.

How to use this resource: work through it actively rather than passively. Attempt each practice question before reading the answer. Time yourself where suggested. Use the explanations not just to check correctness but to notice your own reasoning habits - where you rushed, where you assumed, where you excelled. Treat the situational judgement scenarios as opportunities for genuine self-reflection about how you lead. You bring years of professional experience to this; these exercises are simply a way of making that experience visible, deliberate, and demonstrable. Good luck - you are better prepared than you think.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive ability assessment is a targeted psychometric test that measures the exact mental processes needed for your role, rather than abstract intelligence. Unlike a generic IQ test, it uses practical workplace scenarios, artefacts, and data formats that mirror what a chief data architect actually handles: enterprise data models, metadata repository extracts, assurance findings, standards documents, and architecture decision records.

The typical format is an online, timed test of 15 to 30 minutes, with objective scoring against a benchmark or norm group. Some platforms are adaptive, adjusting question difficulty based on your previous answers, and most provide short, ungraded practice questions first so you can get comfortable with the interface. Employers usually receive a breakdown showing speed versus accuracy rather than a single score, so a considered, accurate approach is often rewarded as much as a fast one.

Why does this matter for your role? As a chief data architect, you set the vision for the organisation's use of data as directed by the appropriate governance body. You oversee the design of multiple data models simultaneously, you are accountable for assuring data models at project and enterprise level, and you are responsible for ensuring the organisation's systems align with the enterprise data architecture. Every one of those accountabilities depends on high-order cognitive skills: spotting the inconsistency in a model that three review boards have missed, deducing the downstream consequence of a schema change, prioritising among competing architectural risks, and holding the "larger picture" in mind while diagnosing a specific fault. A cognitive assessment makes those capabilities visible and measurable.

### What it measures for your role

Mapped explicitly to the skills in your role profile:

- **Data modelling**: pattern recognition across entity-relationship structures, spotting where two models describe the same real-world concept differently, and recognising opportunities for reuse and alignment of data models across organisations. Questions will present model fragments and ask you to find inconsistencies, infer missing relationships, or classify models using a categorisation method.
- **Data analysis and synthesis**: logical deduction from data profiling results and source system analysis, drawing only the conclusions the evidence supports.
- **Data governance and data standards**: error checking against stated rules - given a standard, which artefacts comply and which do not? Given a governance control, which risk does it actually mitigate?
- **Metadata management**: reasoning about repository structures, lineage chains, and the logical consequences of stale or missing metadata.
- **Problem management**: anticipating problems, understanding how a problem fits into the larger picture, and structured fault diagnosis - the assessment's prioritisation and problem-solving items map directly to this skill.
- **Strategic thinking**: evaluating whether a chain of reasoning genuinely supports a strategic conclusion, and identifying the hidden assumption in a plausible-sounding argument.

### Practice questions

**Question 1 (easy) - Pattern recognition in model categorisation**

Your organisation categorises its data models using a three-part code: a letter for scope (E = enterprise, D = domain, P = project), a digit for maturity (1 = draft, 2 = reviewed, 3 = assured), and a letter for modelling level (C = conceptual, L = logical, Y = physical). You review this sequence of recently registered models: E1C, E2C, E3C, D1L, D2L, D3L, P1Y, P2Y, ...

Which code logically continues the sequence?

A) P3Y
B) E1L
C) P3C
D) D1Y

**Correct answer: A.**

**Explanation:** The sequence groups models in threes by scope (E, E, E, then D, D, D, then P, P, ...), advances maturity 1 to 3 within each group, and holds the modelling level constant within each group (C for enterprise, L for domain, Y for project). The third project model should therefore be maturity 3 with physical level: P3Y. This mirrors real work: when you design the method to categorise data models within an organisation, you must be able to verify instantly that registrations follow the scheme, and spot the one that does not.

**Question 2 (easy) - Error checking against a data standard**

Your organisation's data standard states: "Every master data entity must have exactly one designated authoritative source system, a named information asset owner, and a retention schedule. Reference data entities require an authoritative source and a review cycle, but not a retention schedule."

You review four register entries:

1. Entity "Citizen" (master data): authoritative source = CRM-1; owner = Head of Operations; retention schedule = 25 years.
2. Entity "Country Codes" (reference data): authoritative source = ISO feed; review cycle = annual.
3. Entity "Case" (master data): authoritative sources = CMS-2 and CMS-3; owner = Casework Director; retention schedule = 7 years.
4. Entity "Benefit Type" (reference data): authoritative source = Policy team spreadsheet; review cycle = none recorded; retention schedule = 3 years.

Which entries breach the standard?

A) 3 only
B) 4 only
C) 3 and 4
D) 2, 3 and 4

**Correct answer: C.**

**Explanation:** Entry 1 is fully compliant. Entry 2 is compliant: reference data needs a source and review cycle, both present. Entry 3 breaches the "exactly one authoritative source" rule because it lists two source systems - a classic real-world failure you would catch during enterprise assurance. Entry 4 breaches because a reference entity must have a review cycle and none is recorded; the presence of an unnecessary retention schedule is not itself a breach, but the missing review cycle is. So entries 3 and 4 breach. Careful reading of "exactly one" and "requires" is the whole game here - this is precisely the discipline you apply when you advocate for, and oversee compliance with, data policies and standards.

**Question 3 (moderate) - Logical deduction from profiling results**

Your team's data profiling of a legacy licensing system reports the following, all verified as true:

- Every record with a null "issue_date" also has status "pending".
- No record with status "pending" has a fee recorded.
- Some records with status "active" have a null "renewal_date".

Which one of the following conclusions must be true?

A) All records with status "pending" have a null issue_date.
B) No record with a null issue_date has a fee recorded.
C) Some records with a fee recorded have a null renewal_date.
D) Every record with an issue_date has a fee recorded.

**Correct answer: B.**

**Explanation:** From the first statement, null issue_date implies status pending. From the second, pending implies no fee. Chaining them: null issue_date implies no fee recorded - conclusion B follows necessarily. A reverses the first implication (pending records might still have issue dates). C is plausible but not compelled: we know some active records lack renewal dates, but nothing tells us any of those have fees. D is an unsupported universal claim. This is the syllogistic core of data analysis and synthesis: presenting clear insights to colleagues means never claiming more than the profiling evidence entails.

**Question 4 (moderate) - Prioritisation of assurance findings**

You are accountable for assuring data models at enterprise level. Your review backlog contains four findings, and you can commission only one deep-dive this week:

1. A project team has used a non-standard date format in a physical model for an internal reporting tool due to retire in six months.
2. Two flagship programmes have independently modelled "address" in incompatible ways, and both models are about to be baselined into contracts with different suppliers.
3. A domain model is missing three optional descriptive attributes recommended by the style guide.
4. The metadata repository shows one enterprise entity with an outdated definition, already queued for the next scheduled refresh.

Which finding should you prioritise, and why?

A) Finding 1, because date-format errors propagate quickly.
B) Finding 2, because incompatible baselined models will lock divergence into supplier contracts.
C) Finding 3, because style-guide compliance sets the tone for the community.
D) Finding 4, because enterprise entities matter more than project artefacts.

**Correct answer: B.**

**Explanation:** Prioritisation at chief level weighs impact, urgency, and reversibility. Finding 2 scores highest on all three: incompatibility in a core entity like "address" across two flagship programmes creates enduring integration cost; the models are "about to be baselined into contracts", making the window to act short; and once embedded in supplier contracts, the divergence becomes expensive and slow to reverse. Finding 1 is contained and time-limited (retirement in six months). Finding 3 concerns optional attributes - low impact. Finding 4 is already queued for remediation. This exercises problem management (anticipate problems and defend against them at the right time) and the accountability for reuse and alignment of data models across organisations.

**Question 5 (moderate) - Spotting the inconsistency between models**

Two domain models describe the same operational reality. Model A states: "A Grant is awarded to exactly one Applicant. An Applicant may hold many Grants." Model B, from a partner directorate, states: "An Award links one Application to one Funding Stream. An Application is submitted by one or more Organisations acting jointly."

A programme board asks whether the two models can be aligned so that Model B's "Award" records can populate Model A's "Grant" entity. What is the most significant structural obstacle?

A) The entity names differ, so alignment is impossible.
B) Model A assumes a single recipient per grant, while Model B permits jointly submitting organisations, so one Award may map to multiple recipients.
C) Model B includes Funding Stream, which Model A lacks.
D) Model A allows an applicant to hold many grants, which Model B forbids.

**Correct answer: B.**

**Explanation:** Naming differences (A) are superficial and resolved by mapping - exactly the reuse-and-alignment work your data modelling skill describes. An extra entity (C) is an extension, not an obstacle; Model A can simply not consume Funding Stream. Option D is false: Model B says nothing forbidding an organisation from having many applications. The genuine structural conflict is cardinality: Model A's "exactly one Applicant" cannot faithfully represent Model B's joint submissions by "one or more Organisations". Recognising cardinality conflicts - not cosmetic differences - is the heart of assessing whether models genuinely fulfil the needs of the organisation.

**Question 6 (moderate) - Metadata lineage deduction**

Your metadata repository records these lineage facts:

- Dashboard K reads only from Dataset P.
- Dataset P is produced by transformation T, whose only inputs are Datasets Q and R.
- Dataset Q is extracted nightly from System X.
- Dataset R is extracted weekly from System Y.

System Y suffered a silent corruption affecting all its extracts for the past three days. Yesterday's extract of Dataset Q completed cleanly. Today is the day after Dataset R's weekly extract ran. Which statement must be true?

A) Dashboard K is unaffected because Dataset Q is clean.
B) Dashboard K is potentially showing corrupted figures, because Dataset R's most recent weekly extract fell within the corruption window.
C) Dashboard K is unaffected because transformation T would reject corrupted input.
D) Dataset P is unaffected because only one of its two inputs is corrupted.

**Correct answer: B.**

**Explanation:** R's weekly extract ran yesterday, within the three-day corruption window, so R is suspect. T consumes both Q and R, so P inherits R's corruption risk, and K reads only P, so K is potentially compromised. A and D fail because one clean input does not cleanse a blended output. C invents a validation behaviour the facts never state - a classic trap of assuming controls exist. This is why you communicate the value of metadata repositories: only recorded lineage lets you trace impact this quickly, and only disciplined reasoning stops you over- or under-stating it.

**Question 7 (moderate) - Governance rule application**

Your data governance framework, which you aligned with wider governance including budget governance, includes this control: "Any change to an enterprise data model that affects more than one business domain must be approved by the Data Design Authority (DDA). Changes within a single domain may be approved by the domain data steward, unless the change alters an entity marked as critical, in which case DDA approval is required regardless of scope."

Which change requires DDA approval?

A) Renaming an attribute on a single-domain entity not marked critical.
B) Adding an optional attribute to the "Payment" entity, marked critical, used only within the finance domain.
C) A domain steward reordering attributes in a logical model diagram with no semantic change.
D) Correcting a typo in the description field of a non-critical, single-domain entity.

**Correct answer: B.**

**Explanation:** Work the rule as written. A: single domain, not critical - steward approval suffices. B: single domain, but the entity is marked critical, triggering the "regardless of scope" clause - DDA approval required. C and D are single-domain, non-critical, and arguably not even model changes in the semantic sense. The assessment skill here is applying nested conditional logic accurately under time pressure - the same skill you use daily when you decide where standards need to be set and how exceptions flow through assurance mechanisms.

**Question 8 (hard) - Problem diagnosis across the larger picture**

Three symptoms surface in the same fortnight:

- The customer insight team reports duplicate citizen records appearing in their analytical store.
- The operations directorate reports that address updates made in the case management system are not reflected in outbound correspondence.
- The metadata repository shows that the "golden record" matching service's configuration was last updated 14 months ago, despite two new source systems being onboarded since.

As chief data architect, which single underlying hypothesis best explains all three symptoms?

A) The analytical store's deduplication job has a defect.
B) The correspondence system is reading a stale address table.
C) The master data matching service has not been reconfigured for the new source systems, so records from those systems are neither matched nor propagated correctly.
D) The two new source systems have poor data quality.

**Correct answer: C.**

**Explanation:** Test each hypothesis against all three symptoms, not just one. A explains duplicates but not the address propagation failure. B explains the correspondence issue but not the duplicates. D might contribute to both but does not explain why the failures began recently while the matching configuration is 14 months stale. C explains everything: unmatched records from new sources appear as duplicates downstream, and updates entering via unconfigured paths never reach the golden record that correspondence relies on; the metadata evidence directly supports it. This is problem management as your profile defines it - understanding how a problem fits into the larger picture and describing it so others can act.

**Question 9 (hard) - Deductive reasoning about standards adoption**

You are deciding where standards need to be set across the organisation. Your analysis established these facts:

- If a standard is mandated without tooling support, compliance falls below 40%.
- Every standard with compliance below 40% is withdrawn within two years.
- The proposed address standard will be mandated next quarter.
- Tooling support for the address standard cannot be funded until the following financial year, which begins five months after the mandate.

Assuming the facts hold and no other factors intervene, which conclusion is best supported?

A) The address standard will certainly be withdrawn within two years.
B) If tooling support is not delivered, the address standard's compliance will fall below 40% and it will be withdrawn within two years.
C) The address standard will achieve compliance above 40% once tooling arrives.
D) Standards should never be mandated before tooling exists.

**Correct answer: B.**

**Explanation:** A overreaches: tooling arrives five months after mandate, and the facts do not state how quickly the sub-40% compliance effect takes hold or whether a five-month unsupported window is enough to trigger it - so certainty is not available. C asserts a converse the premises never state (tooling is necessary for compliance in the first rule's logic, not sufficient). D is a policy generalisation, not a deduction. B correctly chains the conditionals while preserving the conditional form: without tooling, compliance falls below 40%, and sub-40% compliance leads to withdrawal. Precision about what follows and what merely might follow is exactly what your advice to project teams and governance bodies must carry.

**Question 10 (hard) - Pattern recognition in assurance metrics**

Your quarterly enterprise assurance dashboard shows the count of models failing assurance, by quarter: Q1: 24, Q2: 12, Q3: 18, Q4: 9, Q5: 15, Q6: ?

The pattern alternates two operations. What is the expected Q6 value, and what is the pattern?

A) 21 - add 6 after each halving
B) 7.5 - halve every quarter
C) 12 - the series oscillates around 15
D) 22 - add 7 after each halving

**Correct answer: A.**

**Explanation:** Trace the operations: 24 halved is 12 (Q2); 12 plus 6 is 18 (Q3); 18 halved is 9 (Q4); 9 plus 6 is 15 (Q5). A purely mechanical continuation would halve again to get 7.5 - but a count of failing models cannot be fractional, which is your signal that the mechanical reading is wrong. The consistent whole-number reading is that the series alternates "halve" and "add 6" as paired operations, and the only offered answer that both fits the add-6-after-halving structure and respects the integer constraint is 15 + 6 = 21. Option B applies the pattern mechanically and produces an impossible count; C and D fit no operation in the series. This question deliberately rewards candidates who sanity-check answers against real-world constraints (you cannot fail half a model) rather than applying a pattern blindly - the same instinct you apply when a metric on a governance dashboard looks arithmetically plausible but operationally absurd.

**Question 11 (hard) - Innovation adoption logic**

You are evaluating when to adopt an emerging data catalogue technology, exercising your data innovation skill. Your criteria: adopt only when (i) at least two comparable government organisations have run it in production for a year, and (ii) it supports your metadata standard natively, or a funded adapter project exists. Current facts: three departments run it in production, one for 14 months, the others for 7 and 5 months; native support for your metadata standard is absent; an adapter project is scoped but its funding decision is pending next month.

What is the correct adoption decision now?

A) Adopt now - three departments use it in production.
B) Do not adopt yet - criterion (i) is unmet because only one organisation has a full year in production, and criterion (ii) is unmet because the adapter is not yet funded.
C) Do not adopt yet - criterion (i) is met but criterion (ii) is not.
D) Adopt now, conditional on the funding decision.

**Correct answer: B.**

**Explanation:** Criterion (i) requires at least two organisations with a year in production; only one qualifies (14 months), so (i) fails - option C's claim that (i) is met is wrong. Criterion (ii) requires native support (absent) or a funded adapter (pending is not funded), so (ii) also fails. Both criteria are unmet; B states this precisely. A counts deployments without checking duration; D converts a pending fact into an assumed one. Recognising the appropriate timing for adoption means holding your own criteria steady against enthusiasm - the discipline this question rehearses.

**Question 12 (very hard) - Multi-constraint scheduling and prioritisation**

You must sequence four assurance reviews with one senior reviewer available. Constraints:

- Review W (payments model) must complete before the DDA meets in 3 weeks.
- Review X (identity model) cannot start until an external security opinion arrives in 1 week.
- Review Y (reporting model) takes 2 weeks; W takes 1 week; X takes 2 weeks; Z (reference data) takes 1 week.
- Review Z's project team is only available in weeks 2 and 3.
- The reviewer handles one review at a time, starting now (week 1).

Which sequence satisfies every constraint?

A) W (week 1), Z (week 2), X (weeks 3-4), Y (weeks 5-6)
B) X (weeks 1-2), W (week 3), Z (week 4), Y (weeks 5-6)
C) Y (weeks 1-2), W (week 3), X (weeks 4-5), Z (week 6)
D) Z (week 1), W (week 2), X (weeks 3-4), Y (weeks 5-6)

**Correct answer: A.**

**Explanation:** Test A: W in week 1 completes before the week-3 DDA deadline; Z in week 2 falls inside the project team's weeks 2-3 availability; X starts week 3, after the security opinion arrives at end of week 1; Y follows without constraint. All constraints hold. B fails immediately because X cannot start until week 2 (opinion arrives after 1 week). C completes W in week 3 - arguably at the deadline, but Z runs in week 6, outside the team's weeks 2-3 window - fails. D schedules Z in week 1, outside the availability window - fails. Constraint-satisfaction under time pressure mirrors how you oversee the full data product life cycle across parallel projects: the right answer is rarely the obvious first ordering, and one overlooked constraint invalidates an otherwise elegant plan.

**Question 13 (very hard) - Identifying the flawed assumption in a strategic argument**

A director presents this argument to the governance body: "Our data strategy requires all analytical datasets to be catalogued by 2027. The catalogue currently grows by 200 datasets per quarter. We have 1,600 uncatalogued datasets and eight quarters remaining. Therefore we will meet the target without additional investment."

As chief data architect, which unstated assumption is the argument most critically dependent on?

A) That the catalogue tooling will remain available.
B) That no new uncatalogued datasets will be created during the eight quarters, and the cataloguing rate will not decline.
C) That the 2027 target is genuinely required by the strategy.
D) That 200 datasets per quarter is an impressive rate.

**Correct answer: B.**

**Explanation:** The arithmetic (200 x 8 = 1,600) works only if the backlog is static and the rate constant. In reality, organisations create datasets continuously, and cataloguing rates often slow as the easy datasets are done first - so B is the load-bearing assumption; if it fails, the conclusion collapses. A matters but is a background operational assumption, not the argument's critical dependency. C challenges the premise rather than finding the hidden assumption. D is irrelevant. Evaluating current strategies to ensure business requirements are being met - your strategic thinking skill - is largely the craft of surfacing exactly these silent assumptions before the governance body commits to them.

### Preparation tips

- Rehearse with your own artefacts. Take a real (suitably anonymised) data model, standards register, or lineage diagram and quiz yourself: what is inconsistent, what follows necessarily, what would break if X changed? The assessment formats are abstractions of this daily work.
- Practise the discipline of "must be true" versus "could be true". At your level, the trap is rarely inability - it is over-inference born of experience. You know what usually happens; the test asks what necessarily follows.
- Sanity-check answers against operational reality, as in Question 10. Whole numbers, plausible magnitudes, and real-world constraints are legitimate reasoning tools.
- Manage the clock strategically: bank the easy pattern and rule-checking items quickly to buy time for multi-constraint problems. Do not let a single scheduling puzzle consume a third of your time.
- Do a short warm-up on the day - two or three logic puzzles - so the first scored question is not your first cognitive effort of the morning.

### Common pitfalls

- **Assuming unstated controls exist.** Senior professionals instinctively assume validation, review gates, or rollback exist because they should. As in Question 6, reason only from what the scenario states.
- **Confusing plausibility with necessity.** Options that describe what usually happens in government data programmes are seductive; the correct answer is what the given facts entail.
- **Time sink questions.** Getting anchored on one hard constraint-satisfaction item and rushing everything after it. Skip, flag, return.
- **Mechanical pattern application.** Applying an arithmetic pattern without checking the result makes sense for the quantity being counted.
- **Skimming nested conditions.** Rules with "unless" and "regardless of scope" clauses (Question 7) punish fast readers. Slow down on conditional language; it is where the marks live.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment evaluates your ability to analyse, interpret, and make sound decisions using numerical data drawn from the real demands of your role. It is emphatically not an abstract mathematics exam: the questions focus on business arithmetic - percentages, ratios, cost-benefit estimations, budget allocations, and capacity figures - presented through tables, charts, and datasets of the kind that cross a chief data architect's desk every week.

Typical characteristics: the inputs are realistic artefacts such as programme budgets, storage capacity tables, data quality dashboards, licensing cost schedules, and assurance throughput metrics. An onscreen calculator is usually allowed or provided, because the test prioritises interpretation over mental arithmetic. Time limits are strict - often around a minute to ninety seconds per question - so quick, accurate data extraction matters as much as computation. Watch especially for scale qualifiers such as "in thousands" or "per quarter"; misreading them is the single most common cause of lost marks.

Why this matters for your role: you are accountable for supporting and aligning to the organisation's data strategy, and strategy at your level is argued in numbers - the cost of duplicated data platforms, the risk-weighted value of an assurance programme, the capacity headroom of shared services, the business case for a metadata repository. You align data governance with wider governance, explicitly including budget governance. When you communicate different options to a board, "taking into account risks and uncertainties" almost always means comparing quantified scenarios. A numeric reasoning assessment tests whether you can do that quickly, accurately, and without being misled by presentation.

### What it measures for your role

Mapped to the skills in your role profile:

- **Communicating data**: turning complex numerical data into clear, actionable conclusions - most questions are, at heart, "what do these figures actually tell you?"
- **Data governance (data architect)**: aligning data governance with budget governance; questions use funding tables, cost allocations, and assurance investment trade-offs.
- **Data analysis and synthesis**: extracting the relevant figures from profiling outputs and dashboards, and computing rates, proportions, and trends correctly.
- **Strategic thinking**: evaluating options quantitatively - projected savings, adoption curves, and whether a plan's arithmetic actually supports its conclusion.
- **Data standards and metadata management**: compliance percentages, repository coverage rates, and the cost of non-compliance.
- **Problem management**: spotting when a number is inconsistent with its context, and quantifying the size of a problem before proposing mitigation.

### Practice questions

**Question 1 (easy) - Percentage compliance**

Your data standards compliance dashboard shows that of 480 registered datasets, 312 fully comply with the organisation's metadata standard. What percentage do not fully comply?

A) 65%
B) 35%
C) 42%
D) 30%

**Correct answer: B.**

**Explanation:** Compliant proportion: 312 / 480 = 0.65, so 65% comply. Non-compliant: 100% - 65% = 35%, which is 168 datasets (480 - 312 = 168; 168 / 480 = 0.35). Option A is the trap for candidates who compute the compliant share but answer the question actually asked - always re-read whether the question wants compliance or non-compliance.

**Question 2 (easy) - Budget share**

The data architecture function's annual budget is £2.4 million, allocated as: staff 55%, tooling 25%, training and community 10%, contingency 10%. The governance body asks you to increase tooling by £120,000, funded entirely from contingency. What is the new contingency allocation in pounds?

A) £120,000
B) £240,000
C) £360,000
D) £96,000

**Correct answer: A.**

**Explanation:** Contingency starts at 10% of £2,400,000 = £240,000. Removing £120,000 leaves £240,000 - £120,000 = £120,000. Tooling rises from £600,000 (25%) to £720,000, and total remains £2.4 million. The arithmetic is simple; the skill is holding the "funded entirely from contingency" condition steady while the percentages try to distract you - exactly the discipline of aligning data governance with budget governance.

**Question 3 (moderate) - Data quality improvement rate**

A data profiling exercise on the citizen master dataset finds 18,400 records with address quality defects out of 920,000 records. After the matching service is reconfigured, a re-profile finds 11,960 defective records. By what percentage did the defect count fall, and what is the new defect rate?

A) 35% fall; new rate 1.3%
B) 65% fall; new rate 1.3%
C) 35% fall; new rate 2.0%
D) 30% fall; new rate 1.5%

**Correct answer: A.**

**Explanation:** Fall in defects: 18,400 - 11,960 = 6,440. Percentage fall: 6,440 / 18,400 = 0.35 = 35%. New defect rate: 11,960 / 920,000 = 0.013 = 1.3%. Option B confuses the remaining share (11,960 / 18,400 = 65%) with the fall. When you present clear insights to colleagues to support the end use of the data, the difference between "defects fell 35%" and "65% of defects remain" is the difference between a good headline and a wrong one.

**Question 4 (moderate) - Storage capacity and growth**

Your enterprise data platform currently holds 640 TB and grows at 5% per quarter (compounding). The platform's funded capacity ceiling is 780 TB. Will the platform breach its ceiling within four quarters, and roughly when?

A) No - four quarters of growth reaches approximately 778 TB, just under the ceiling.
B) Yes - it breaches in quarter 3.
C) Yes - it breaches in quarter 4 at approximately 795 TB.
D) No - growth is linear, reaching 768 TB.

**Correct answer: A.**

**Explanation:** Compound at 5%: Q1: 640 x 1.05 = 672 TB. Q2: 672 x 1.05 = 705.6 TB. Q3: 705.6 x 1.05 = 740.88 TB. Q4: 740.88 x 1.05 = 777.9 TB. That is just below 780 TB, so no breach within four quarters - but the headroom at the end of Q4 is only about 2 TB, meaning a breach is virtually certain early in quarter 5. Option D applies simple rather than compound growth (640 x 1.20 = 768). As chief data architect you would report both facts to the governance body: technically within ceiling this year, but the funding decision for expansion cannot wait - communicating options while taking account of risks and uncertainties.

**Question 5 (moderate) - Cost per model assured**

Your enterprise assurance team of 4 FTE costs £380,000 per year fully loaded and assured 95 data models last year. A proposal adds 1 FTE at £85,000, with an expected uplift to 130 models assured per year. What is the change in cost per model assured?

A) Falls from £4,000 to £3,577 - roughly an 11% reduction
B) Rises from £4,000 to £4,650
C) Falls from £4,000 to £3,577 - roughly a 22% reduction
D) Falls from £3,800 to £3,500

**Correct answer: A.**

**Explanation:** Current cost per model: £380,000 / 95 = £4,000. Proposed: (£380,000 + £85,000) / 130 = £465,000 / 130 = £3,576.92, approximately £3,577. Reduction: (£4,000 - £3,577) / £4,000 = £423 / £4,000 = 0.1058, roughly 11%. Option C pairs the right figures with a wrong percentage - a reminder to finish the calculation rather than pattern-match to the plausible-looking numbers. Unit-cost analysis like this is precisely how you justify assurance investment when aligning with budget governance.

**Question 6 (moderate) - Ratio of reuse**

Across government, your team surveys 240 data models in your domain cluster. They classify 96 as "aligned to a shared cross-government model", 84 as "locally bespoke but mappable", and the remainder as "incompatible". What is the ratio of aligned to mappable to incompatible models, in simplest form?

A) 8 : 7 : 5
B) 96 : 84 : 60
C) 4 : 3 : 2
D) 8 : 7 : 6

**Correct answer: A.**

**Explanation:** Incompatible: 240 - 96 - 84 = 60. Ratio 96 : 84 : 60. Divide by the greatest common divisor, 12: 96/12 = 8, 84/12 = 7, 60/12 = 5, giving 8 : 7 : 5. Option B is the unsimplified ratio; C and D each mis-simplify one term. Reuse-and-alignment metrics like these are the evidence base when you work across government recognising opportunities for the reuse and alignment of data models in different organisations.

**Question 7 (moderate) - Weighted risk scoring**

Your assurance mechanism scores each system's data risk as: (data sensitivity score x 0.5) + (volume score x 0.2) + (integration criticality score x 0.3), each component scored 1-10. Three systems are assessed:

| System | Sensitivity | Volume | Integration |
|---|---|---|---|
| Grants platform | 6 | 8 | 4 |
| Identity service | 9 | 5 | 9 |
| Reporting store | 4 | 9 | 6 |

Which system has the highest weighted risk score, and what is it?

A) Identity service, 8.2
B) Grants platform, 5.8
C) Identity service, 7.7
D) Reporting store, 6.4

**Correct answer: A.**

**Explanation:** Grants: (6 x 0.5) + (8 x 0.2) + (4 x 0.3) = 3.0 + 1.6 + 1.2 = 5.8. Identity: (9 x 0.5) + (5 x 0.2) + (9 x 0.3) = 4.5 + 1.0 + 2.7 = 8.2. Reporting: (4 x 0.5) + (9 x 0.2) + (6 x 0.3) = 2.0 + 1.8 + 1.8 = 5.6. Identity service leads at 8.2. Option D miscalculates the reporting store; option C is a near-miss arithmetic slip (forgetting one component's decimal). Weighted scoring is the arithmetic backbone of "assure corporate services by understanding important risks and providing mitigation through assurance mechanisms" - and the assessment checks you can execute it flawlessly under time pressure.

**Question 8 (hard) - Metadata repository business case**

A metadata repository licence costs £150,000 per year plus £60,000 annual support. Implementation is a one-off £220,000 in year 1. The repository is expected to save analysts 15 minutes per data discovery task; the organisation performs approximately 48,000 such tasks per year, and analyst time is costed at £52 per hour. Assuming the savings accrue in full in both years, what is the approximate net financial position over the first two years?

A) Net benefit of approximately £608,000
B) Net cost of approximately £150,000
C) Net benefit of approximately £624,000
D) Net benefit of approximately £828,000

**Correct answer: A.**

**Explanation:** Annual time saving: 48,000 tasks x 15 minutes = 720,000 minutes = 12,000 hours. Annual value: 12,000 hours x £52 = £624,000. Two-year benefit: 2 x £624,000 = £1,248,000. Two-year cost: implementation £220,000 + 2 x (£150,000 licence + £60,000 support) = £220,000 + £420,000 = £640,000. Net position: £1,248,000 - £640,000 = £608,000 net benefit. Option C is the single-year gross saving masquerading as a net figure; option D forgets the £220,000 implementation cost (£1,248,000 - £420,000 = £828,000); option B is what a sceptic gets by counting two years of costs against only one year of benefit - a scenario worth acknowledging when you present, because in reality benefits rarely start on day one. This is the arithmetic behind "communicate the value of metadata repositories": a governance body will probe exactly these terms - benefit start date, running costs, and the difference between gross and net - so build the habit of stating each assumption as you compute.

**Question 9 (hard) - Interpreting a data quality dashboard**

Your quarterly dashboard reports completeness of five critical entities (percentage of mandatory attributes populated):

| Entity | Q1 | Q2 | Q3 |
|---|---|---|---|
| Citizen | 91% | 93% | 94% |
| Address | 82% | 80% | 86% |
| Case | 77% | 79% | 78% |
| Payment | 96% | 96% | 95% |
| Organisation | 68% | 74% | 79% |

Which entity showed the largest percentage-point improvement from Q1 to Q3, and what was it?

A) Organisation, 11 percentage points
B) Address, 6 percentage points
C) Organisation, 16.2%
D) Citizen, 3 percentage points

**Correct answer: A.**

**Explanation:** Q1-to-Q3 changes: Citizen +3, Address +4, Case +1, Payment -1, Organisation +11. Organisation improves most, by 11 percentage points (68% to 79%). Option C is the relative change (11/68 = 16.2%) mislabelled as the answer - the question asked for percentage points. Option B misreads Address's dip-and-recover pattern (net +4, not +6). Distinguishing percentage points from percentage change is a signature trap in numeric tests and in real governance reporting alike; presenting one as the other in a board paper is exactly the kind of miscommunication your communicating data skill exists to prevent.

**Question 10 (hard) - Programme funding allocation**

The data strategy programme has £5.6 million to allocate across four workstreams in the ratio 4 : 3 : 2 : 5 (platform, governance, community, migration respectively). Mid-year, £700,000 is cut, applied proportionally. How much does the governance workstream lose, and what is its revised allocation?

A) Loses £150,000; revised £1,050,000
B) Loses £175,000; revised £1,225,000
C) Loses £150,000; revised £1,200,000
D) Loses £140,000; revised £1,060,000

**Correct answer: A.**

**Explanation:** Ratio total: 4 + 3 + 2 + 5 = 14 parts. Each part: £5,600,000 / 14 = £400,000. Governance (3 parts): £1,200,000. Proportional cut: governance share of £700,000 is (3/14) x £700,000 = £150,000. Revised: £1,200,000 - £150,000 = £1,050,000. Option C gives the original allocation as "revised". Option B misassigns 3.5 parts. Ratio-based allocation and proportional reduction is bread-and-butter arithmetic for a chief data architect defending workstreams through budget governance in a spending-review climate.

**Question 11 (hard) - Adoption curve versus target**

Your data standards adoption plan requires 90% of the organisation's 340 in-scope systems to comply within three years. Current compliance: 136 systems. The remediation pipeline upgrades systems at a steady 55 systems per year, but 10% of upgraded systems regress within the same year and must be redone the following year (counting against that year's 55). How many compliant systems will there be at the end of year 3, and is the target met?

A) 288 systems (about 85%) - target missed
B) 301 systems (about 89%) - target missed
C) 306 systems (90%) - target met exactly
D) 271 systems (about 80%) - target missed

**Correct answer: A.**

**Explanation:** Target: 90% of 340 = 306 systems. Effective net progress: each year 55 systems are upgraded but 10% (5.5, call it 5-6) regress and consume next year's capacity. Year 1: 136 + 55 = 191, minus 5.5 regressed = 185.5 net compliant entering year 2. Year 2: 55 upgrades, of which 5.5 slots effectively redo regressions; net new = 55 - 5.5 = 49.5 plus recovery of the 5.5 = net +55 gross but 10% of this year's upgrades (5.5) regress again: compliant approximately 185.5 + 55 - 5.5 = 235. Year 3: similarly +49.5 net plus the ongoing 5.5 redo churn: approximately 235 + 55 - 5.5 = 284.5, and adding back the final year's in-flight redos gives approximately 288. Compliance: 288 / 340 = 84.7%, short of 306. The precise modelling can vary by a few systems depending on assumptions, but every defensible reading lands well short of target - which is the strategic point. When you evaluate current strategies to ensure business requirements are being met, an adoption plan that looks sufficient on gross throughput (55 x 3 = 165 new; 136 + 165 = 301, already short) fails even faster once regression churn is modelled. Recognising that the gross plan misses before you even model churn is the fastest route to the right answer under exam conditions.

**Question 12 (very hard) - Cost of divergent models**

Two programmes built divergent "address" models. Integration between them requires a translation service costing £95,000 per year to operate, plus an average of 12 defects per year each costing £4,500 to resolve. Converging the models is a one-off project estimated at £310,000, after which translation and defect costs cease, but convergence adds £20,000 per year in shared model governance. Over a four-year horizon, what is the net saving from converging at the start of year 1?

A) £286,000
B) £306,000
C) £206,000
D) £366,000

**Correct answer: C.**

**Explanation:** Status quo annual cost: £95,000 translation + (12 x £4,500) defects = £95,000 + £54,000 = £149,000 per year. Over four years: 4 x £149,000 = £596,000 avoided if you converge at the start of year 1. Convergence cost over the same horizon: £310,000 one-off + (4 x £20,000) ongoing governance = £310,000 + £80,000 = £390,000. Net saving: £596,000 - £390,000 = £206,000. Option A (£286,000) is exactly £80,000 too high - it is what you get if you forget that the converged state carries £20,000 per year of governance cost; the distractors are deliberately spaced by that governance term because omitting the target state's running costs is the most common real-world business-case error. Option D nets only the one-off cost against gross savings. Always total both cost structures over the same horizon before differencing - and when you present the option to a board, say explicitly that the saving is net of new governance overheads, so the figure survives scrutiny.

**Question 13 (very hard) - Capacity, concurrency and the larger picture**

Your shared analytical platform serves 3 departments. Peak concurrent query load is 420 queries; the platform sustains 500. Department A plans a new service adding 15% to peak load; Department B plans one adding 60 queries; Department C will retire a service, removing 8% of the current peak. All changes land next quarter. What is the projected peak load, and what headroom remains?

A) 509.4 queries - the platform is over capacity by about 9 queries
B) 489 queries - headroom of 11 queries
C) 509 queries - headroom of 9 queries
D) 449 queries - headroom of 51 queries

**Correct answer: A.**

**Explanation:** Department A adds 15% of 420 = 63 queries. Department B adds 60. Department C removes 8% of 420 = 33.6 queries. Projected peak: 420 + 63 + 60 - 33.6 = 509.4. Capacity is 500, so the platform is over capacity by 9.4 queries - roughly 2% over. Option C computes the same figure but misreads it as headroom; option B subtracts A's addition incorrectly. The strategic insight matters more than the decimals: three individually reasonable changes, each approved in isolation by different governance routes, combine to breach shared capacity. This is the numeric face of problem management - anticipating problems and defending against them at the right time - and of your accountability for ensuring systems are designed in accordance with the enterprise data architecture rather than approved piecemeal.

**Question 14 (moderate) - Licensing consolidation savings**

Your organisation runs three separate data catalogue tools inherited from a machinery-of-government merger, costing £84,000, £126,000, and £57,000 per year respectively. Consolidating onto the mid-priced tool requires expanding its licence by 40% of its current cost, plus a one-off migration cost of £95,000. What is the payback period for consolidation, to the nearest quarter of a year?

A) About 1 year
B) About 0.75 years (three quarters)
C) About 1.25 years
D) About 2 years

**Correct answer: A.**

**Explanation:** Current total annual cost: £84,000 + £126,000 + £57,000 = £267,000. Consolidated annual cost: £126,000 x 1.40 = £176,400. Annual saving: £267,000 - £176,400 = £90,600. Payback: £95,000 one-off / £90,600 per year = 1.05 years - about 1 year to the nearest quarter. Option B tempts candidates who forget the 40% licence expansion and divide £95,000 by the larger, wrong saving of £141,000 (£95,000 / £141,000 = 0.67); option D doubles the migration cost or halves the saving. Payback arithmetic is the lingua franca of consolidation cases, and rationalising duplicated tooling after organisational change is a recurring chief data architect duty - being fluent in it lets you answer the finance director's first question before it is asked.

**Question 15 (hard) - Assurance throughput and utilisation**

Your assurance team has 5 reviewers. Each has 46 working weeks per year, of which 20% is consumed by community, training, and governance duties. A standard model review takes 1.5 reviewer-weeks; an enterprise-level review takes 4 reviewer-weeks. Next year's demand forecast is 96 standard reviews and 14 enterprise reviews. What is the approximate utilisation of the team's available review capacity?

A) About 109% - the team is over capacity
B) About 87% - comfortable headroom
C) About 100% - exactly at capacity
D) About 76% - substantial spare capacity

**Correct answer: A.**

**Explanation:** Available capacity: 5 reviewers x 46 weeks = 230 reviewer-weeks, minus 20% overhead = 230 x 0.80 = 184 reviewer-weeks for reviews. Demand: (96 x 1.5) + (14 x 4) = 144 + 56 = 200 reviewer-weeks. Utilisation: 200 / 184 = 1.087, about 109% - the team is roughly 16 reviewer-weeks over capacity. Option C is what you get by forgetting the 20% overhead (200 / 230 = 87% - which is option B's figure mislabelled); option D miscomputes demand. The managerial consequence matters more than the decimals: at 109% forecast utilisation you must either add capacity, reduce review scope, or triage demand - and this is exactly the quantified argument you would take to budget governance rather than letting the queue silently lengthen and assurance quality silently fall.

### Preparation tips

- Refresh the core toolkit: percentages, percentage points versus percentage change, ratios, weighted averages, compound growth, and unit costs. These six patterns cover the vast majority of questions at this level.
- Practise reading tables fast but reading questions slowly. Most errors at senior level are extraction errors (wrong row, wrong period, wrong unit), not calculation errors.
- Use the calculator for arithmetic but your head for estimation. Before computing, estimate the order of magnitude; if the calculator answer disagrees wildly, you mis-keyed or mis-extracted.
- Rehearse with your own artefacts: last quarter's assurance dashboard, the programme's budget spreadsheet, the platform capacity report. Convert them into questions - what changed, by what percentage, is the trend compound or linear?
- In business-case questions, always identify when benefits start and whether the new state has running costs. As Questions 8 and 12 show, those two assumptions move answers by six figures.
- Bank quick wins first. A ratio-simplification question is worth the same as a three-stage business case; do not spend them equally.
- Finally, practise under genuine time pressure at least twice before the real assessment. Accuracy that evaporates under a countdown clock is the most common gap between practice performance and test performance, and it is entirely trainable: two or three timed runs are usually enough to make the clock feel routine rather than threatening.

### Common pitfalls

- **Misreading chart and table labels**: confusing quarterly with annual figures, or ignoring scale qualifiers like "in thousands". At chief level the tables are dense on purpose.
- **Percentage points versus percentages**: reporting an 11 percentage-point rise as "16.2% improvement" (or vice versa) is both a test trap and a genuine governance-paper hazard.
- **Over-calculating**: performing full precision arithmetic when estimation would eliminate three options in seconds. Question 11 falls to estimation before modelling.
- **Time sink questions**: getting anchored on a multi-stage business case while easier ratio and percentage items go unanswered. Skip, flag, return.
- **Forgetting the new state's costs**: netting a one-off investment against gross savings without the ongoing running costs of the target state.
- **Answering the mirror question**: computing compliance when asked for non-compliance, headroom when asked for breach. Re-read the final sentence of every question before selecting.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment evaluates how well you understand, analyse, and draw correct conclusions from written business information. It mirrors the exact reading demands of your role: dense passages drawn from data strategies, governance policies, standards documents, assurance reports, cross-government agreements, and senior correspondence, followed by statements you must judge as True, False, or Cannot Say, plus multiple-choice comprehension items.

The defining rule is fact-based logic: you must answer based strictly on the text provided, setting aside your considerable outside knowledge. "True" means the passage states it or it follows necessarily from what is stated. "False" means the passage contradicts it. "Cannot Say" means the passage provides insufficient information either way - even if you know from experience that the statement is almost certainly correct in the real world. Tests are time-pressured, often allowing under a minute per question, to simulate the pace at which you triage a crowded inbox before a board meeting.

Why this matters for your role: a chief data architect lives in precise language. You create data standards for the organisation, where a single modal verb - "must" versus "should" - changes what compliance means. You are accountable for assuring data models, which requires reading design documentation exactly as written rather than as intended. You support or host difficult discussions with diverse senior stakeholders, where misquoting a policy by one clause can cost you the room. And you communicate between the technical and non-technical, which begins with extracting precisely what a text does and does not commit to. Verbal reasoning assessments measure that precision directly.

### What it measures for your role

Mapped to the skills in your role profile:

- **Communicating between the technical and non-technical**: interpreting the needs and commitments embedded in stakeholder correspondence, and distinguishing what was actually agreed from what was merely discussed.
- **Data standards**: parsing normative language - must, should, may, unless, except - exactly as written, because you both write standards and adjudicate compliance with them.
- **Data governance (data architect)**: reading governance frameworks and terms of reference closely enough to know precisely which body approves what, under which conditions.
- **Communicating data**: identifying the actual claim a report makes, including its caveats and uncertainties, before you re-communicate it to others.
- **Data analysis and synthesis**: separating evidence from interpretation in analytical write-ups.
- **Strategic thinking**: detecting the difference between a strategy's stated commitments, aspirations, and assumptions.

### Practice questions

**Passage A - Extract from a departmental data strategy**

"The department will establish a single enterprise data model for its priority domains by the end of the spending review period. Priority domains are those designated annually by the Data Governance Board. Systems procured after the strategy's publication date must demonstrate alignment to the enterprise data model before receiving approval to proceed to public beta. Legacy systems are expected to align at their next major upgrade, although the Board may grant time-limited exemptions where alignment costs are demonstrably disproportionate. Nothing in this strategy removes the obligations placed on the department by existing legislation concerning the handling of personal data."

**Question 1 (easy) - True / False / Cannot Say**

Statement: Systems procured after the strategy's publication must demonstrate alignment to the enterprise data model before approval to proceed to public beta.

A) True
B) False
C) Cannot Say

**Correct answer: A - True.**

**Explanation:** This is a near-verbatim restatement of the third sentence: "Systems procured after the strategy's publication date must demonstrate alignment to the enterprise data model before receiving approval to proceed to public beta." Easy items like this reward careful matching of the statement against the exact wording - note "must" in both. Bank these marks quickly and accurately.

**Question 2 (easy) - True / False / Cannot Say**

Statement: All legacy systems must align to the enterprise data model at their next major upgrade.

A) True
B) False
C) Cannot Say

**Correct answer: B - False.**

**Explanation:** The passage says legacy systems "are expected to align at their next major upgrade, although the Board may grant time-limited exemptions". The statement's "All ... must" contradicts the text twice over: "expected to" is weaker than "must", and the exemption clause means alignment is explicitly not universal. This is the must/should/expected distinction you police every day when you advocate for, and oversee compliance with, data policies and standards - the passage's normative language simply does not support the absolute claim.

**Question 3 (moderate) - True / False / Cannot Say**

Statement: The Data Governance Board designates priority domains every year.

A) True
B) False
C) Cannot Say

**Correct answer: A - True.**

**Explanation:** The passage states: "Priority domains are those designated annually by the Data Governance Board." "Designated annually by" directly supports "designates every year". Some candidates choose Cannot Say because the passage does not describe the Board actually doing it in any given year - but the passage's definitional sentence asserts the annual designation as how priority domains come to be, which is sufficient. Do not out-think plainly stated text.

**Question 4 (moderate) - True / False / Cannot Say**

Statement: The strategy reduces the department's obligations under data protection legislation.

A) True
B) False
C) Cannot Say

**Correct answer: B - False.**

**Explanation:** The final sentence states: "Nothing in this strategy removes the obligations placed on the department by existing legislation concerning the handling of personal data." A strategy that removes nothing cannot be said to reduce those obligations - the passage directly contradicts the statement. Note the precision required: if the statement had said "the strategy changes how the department documents its legislative obligations", the answer would be Cannot Say, because the passage is silent on documentation. The contradiction here is specific and textual.

**Question 5 (moderate) - True / False / Cannot Say**

Statement: The Board has granted at least one exemption to a legacy system.

A) True
B) False
C) Cannot Say

**Correct answer: C - Cannot Say.**

**Explanation:** The passage says the Board "may grant time-limited exemptions" - a power, not a record of use. Whether any exemption has actually been granted is simply not addressed. Your professional experience tells you exemption powers are always used eventually; the test asks you to suspend exactly that experience. "May" grants possibility; it reports no events. This is the single most common Cannot Say pattern: converting a stated power or possibility into an assumed fact.

**Passage B - Email from a director general**

"Thank you for the data architecture assurance report. I accept the finding that the casework programme's data model diverges from the enterprise standard in its handling of household relationships. However, I do not accept the recommendation to pause the programme's beta launch, given the Minister's public commitment to the launch date. I have asked the programme director to fund a remediation workstream, to report monthly to your Data Design Authority, beginning after launch. I would welcome your view on whether monthly reporting gives your team sufficient oversight, or whether the DDA requires an interim gate before the service scales nationally."

**Question 6 (moderate) - Multiple choice comprehension**

Which of the following best describes the director general's position?

A) They reject the assurance report and its recommendation.
B) They accept the finding but reject the recommendation to pause, proposing post-launch remediation with monthly reporting instead.
C) They accept both the finding and the recommendation, subject to ministerial approval.
D) They defer the entire decision to the Data Design Authority.

**Correct answer: B.**

**Explanation:** The email accepts "the finding that the casework programme's data model diverges" and explicitly does not accept "the recommendation to pause the programme's beta launch", proposing a funded remediation workstream reporting monthly. A overstates the rejection (the finding is accepted); C reverses the recommendation decision; D confuses an invitation for a view ("I would welcome your view") with a delegation of the decision. Reading senior correspondence at this resolution - what precisely is accepted, rejected, proposed, and asked - is the daily substance of communicating between the technical and non-technical at the most senior levels.

**Question 7 (moderate) - True / False / Cannot Say**

Statement: The Minister has publicly committed to the beta launch date.

A) True
B) False
C) Cannot Say

**Correct answer: A - True.**

**Explanation:** The director general writes "given the Minister's public commitment to the launch date". The email asserts this as fact, and in verbal reasoning you treat the passage's assertions as true for the purpose of the test. Some candidates hesitate because the claim is second-hand; but Cannot Say applies when the passage gives no information, not when the information arrives via the author's assertion. The passage explicitly states the commitment exists and is public.

**Question 8 (hard) - True / False / Cannot Say**

Statement: The remediation workstream will begin before the beta launch.

A) True
B) False
C) Cannot Say

**Correct answer: B - False.**

**Explanation:** The email states the workstream is "to report monthly to your Data Design Authority, beginning after launch". The most natural and grammatically supported reading is that the workstream's reporting - and the arrangement itself - begins after launch, which contradicts "will begin before the beta launch". Candidates who parse "beginning after launch" as attaching only to the reporting might argue Cannot Say about when work itself starts; the test rewards the direct reading, and the statement as worded ("will begin before") finds no support and direct contradiction in the only temporal anchor the text provides. When the only time reference in the passage places the activity after launch, a statement placing it before launch is false. In your assurance work, this is exactly the clause you would tighten before agreeing: "beginning after launch" should specify what begins - the work or merely the reporting.

**Passage C - Extract from a proposed cross-government data standard**

"This standard defines the exchange format for organisation identifiers across participating bodies. Participation is voluntary for arm's-length bodies but mandatory for ministerial departments from April next year. A participating body must publish a conformance statement within three months of adoption and must renew it annually thereafter. Where a participating body operates systems that cannot yet conform, it must publish a divergence register describing each non-conforming system and its remediation date. The standard does not apply to identifiers used solely within a single system that are never exchanged."

**Question 9 (hard) - True / False / Cannot Say**

Statement: An arm's-length body that chooses not to participate must publish a divergence register.

A) True
B) False
C) Cannot Say

**Correct answer: B - False.**

**Explanation:** The divergence register obligation attaches to "a participating body [that] operates systems that cannot yet conform". Participation is voluntary for arm's-length bodies; one that chooses not to participate is not a participating body, so no obligation in the passage reaches it. The statement asserts an obligation the text confines to participants - contradiction, hence False. This is scope-tracing: every "must" in a standard binds a defined subject, and your job as the author of organisational data standards is to know exactly who each obligation binds. The test compresses that craft into forty-five seconds.

**Question 10 (hard) - True / False / Cannot Say**

Statement: A ministerial department that adopts the standard in June must publish its first conformance statement by September of the same year.

A) True
B) False
C) Cannot Say

**Correct answer: A - True.**

**Explanation:** The passage: "A participating body must publish a conformance statement within three months of adoption." A ministerial department that adopts in June is a participating body; three months from June is September. The statement follows necessarily from the rule plus ordinary calendar arithmetic - the kind of small inferential step verbal tests do expect you to make. Note what would flip the answer: if the statement had said "by August", it would contradict the three-month window and be False; if it had concerned a body whose participation status was unstated, Cannot Say would enter the frame.

**Question 11 (hard) - True / False / Cannot Say**

Statement: Identifiers exchanged between two systems operated by the same participating body are outside the standard's scope.

A) True
B) False
C) Cannot Say

**Correct answer: B - False.**

**Explanation:** The exclusion is precise: "identifiers used solely within a single system that are never exchanged". Identifiers exchanged between two systems fail both limbs of the exclusion - they are not within a single system, and they are exchanged. Since the passage defines the standard as covering "the exchange format for organisation identifiers", an exchange between two systems falls inside scope even when one body operates both systems; nothing in the text limits "exchange" to exchanges between different bodies. The statement claims an exemption the text does not grant, and the definition contradicts it. Reading exclusion clauses at this precision is exactly how you decide where standards need to be set and how compliance questions get adjudicated - most real disputes live in exactly this kind of clause.

**Passage D - Extract from an assurance report to the governance body**

"Our profiling of the four source systems feeding the new analytical platform found that three provide organisation identifiers consistent with the enterprise model. The fourth, the grants legacy system, uses a locally minted identifier with no documented mapping. The programme team believes a mapping can be constructed from historical correspondence records, but this has not been tested. If no reliable mapping is achievable, grant records will be unlinkable to the organisation golden record, affecting an estimated 9% of analytical queries. We recommend that mapping feasibility be proven before the platform's assurance gate, and we note that the programme's own risk register does not currently include this risk."

**Question 12 (moderate) - Multiple choice comprehension**

Which statement most accurately reflects the report's assessment of the mapping?

A) A mapping has been constructed from correspondence records but not yet deployed.
B) The programme team believes a mapping can be constructed, but the belief is untested.
C) A reliable mapping is unachievable, so 9% of queries will fail.
D) The mapping risk is recorded on the programme's risk register.

**Correct answer: B.**

**Explanation:** The text: "The programme team believes a mapping can be constructed ... but this has not been tested." B reproduces both the belief and its untested status. A converts belief into completed construction. C converts a conditional ("If no reliable mapping is achievable ...") into a settled fact. D contradicts the report's explicit note that the risk register "does not currently include this risk". Every wrong option here upgrades tentative language into certainty - the precise failure mode your communicating data skill guards against when you carry analytical findings to a board: the caveats are part of the finding.

**Question 13 (hard) - True / False / Cannot Say**

Statement: If the mapping proves unreliable, more than 9% of analytical queries will be affected.

A) True
B) False
C) Cannot Say

**Correct answer: B - False.**

**Explanation:** The report says an unreliable mapping would affect "an estimated 9% of analytical queries". The statement claims more than 9% would be affected, which contradicts the estimate the passage gives - within the closed world of the passage, the estimate is the fact. Had the statement said "approximately 9% of queries would be affected", it would be True; had it said "9% of grant records would be unlinkable", it would be False for a different reason - the 9% attaches to queries, not records, and precision about what a percentage measures is a habit this role cannot do without. Candidates tempted by Cannot Say ("estimates can be wrong") are importing outside scepticism; the test's rule is that the passage's claims, including its estimates, are the evidence base.

**Question 14 (moderate) - True / False / Cannot Say**

Statement: The report recommends delaying the platform's assurance gate.

A) True
B) False
C) Cannot Say

**Correct answer: C - Cannot Say.**

**Explanation:** The recommendation is "that mapping feasibility be proven before the platform's assurance gate". That sequences the proof before the gate; it does not say the gate must move. If feasibility can be proven quickly, no delay follows; if not, a delay might - but the report itself neither recommends nor rules out moving the gate. The distinction between "X must happen before Y" and "Y must be delayed" is subtle and entirely real: in assurance practice these are different asks with different political costs, and conflating them in front of a governance body would misrepresent the report. Cannot Say is the disciplined answer.

**Passage E - Extract from the terms of reference of the Data Design Authority**

"The Data Design Authority (DDA) approves changes to enterprise data models and adjudicates disputes concerning data standards. The DDA meets monthly and is quorate when the chief data architect or their nominated deputy and at least three domain representatives are present. Decisions are made by consensus; where consensus cannot be reached, the chair holds a casting vote. Urgent decisions between meetings may be taken by the chair and ratified at the next meeting; any decision not ratified is void from the date of the meeting. The DDA reports quarterly to the Data Governance Board, which may overturn DDA decisions only on grounds of strategic misalignment or legal risk."

**Question 15 (moderate) - True / False / Cannot Say**

Statement: A DDA meeting attended by the chief data architect's nominated deputy and three domain representatives is quorate.

A) True
B) False
C) Cannot Say

**Correct answer: A - True.**

**Explanation:** The quorum rule requires "the chief data architect or their nominated deputy and at least three domain representatives". The described meeting has the nominated deputy (satisfying the first limb via "or") and exactly three domain representatives (satisfying "at least three"). Both limbs are met, so the meeting is quorate. Candidates sometimes stumble on "at least three" (three qualifies) or assume the chief must attend personally (the "or" says otherwise). Parsing conjunctions and disjunctions in governance documents - and versus or, at least versus more than - is a skill you exercise every time you check whether a decision of your own authority was validly made.

**Question 16 (hard) - True / False / Cannot Say**

Statement: An urgent decision taken by the chair between meetings has no effect until it is ratified.

A) True
B) False
C) Cannot Say

**Correct answer: B - False.**

**Explanation:** The passage says urgent decisions "may be taken by the chair and ratified at the next meeting; any decision not ratified is void from the date of the meeting". A decision that is void only "from the date of the meeting" if not ratified necessarily had effect between being taken and that meeting - otherwise there would be nothing to void from that date. The statement claims no effect until ratification, which the voiding rule's structure contradicts. This is the hardest kind of verbal item: the answer lives not in any single clause but in what a clause's wording implies about the interim period. It is also exactly the kind of drafting subtlety you would interrogate when setting up robust governance processes - does an unratified urgent decision unwind retrospectively or only prospectively? This text answers: prospectively.

**Question 17 (moderate) - True / False / Cannot Say**

Statement: The Data Governance Board may overturn a DDA decision because it disagrees with the technical design choice.

A) True
B) False
C) Cannot Say

**Correct answer: B - False.**

**Explanation:** The passage restricts the Board's power: it "may overturn DDA decisions only on grounds of strategic misalignment or legal risk". Technical disagreement is neither of the two permitted grounds, and the word "only" closes the list. The statement therefore asserts a power the text explicitly limits away - False. If the passage had lacked the word "only", the answer would arguably be Cannot Say, since an open list might admit other grounds; a single word carries the whole question. When you draft or negotiate terms of reference for the governance mechanisms you operate, "only" is one of the most consequential words you will place - this item rehearses reading it with the weight it deserves.

### Preparation tips

- Train the closed-world habit. For each practice passage, ask: what does this text state, what does it contradict, and what does it simply not address? Rehearse labelling statements with those three categories until it is reflexive.
- Read normative language forensically. Circle every must, should, may, expected, unless, except, and solely in practice passages. At your level the test-writers hide most of the marks inside these words - just as you do when you draft standards.
- Practise with your genuine reading diet: a page of a government data strategy, a standard's conformance clause, a director general's email. Write three statements about each - one True, one False, one Cannot Say - and check your own reasoning. Writing items is the fastest way to learn to answer them.
- Scan strategically under time pressure: read the question statement first, then hunt the passage for the governing sentence, then read that sentence slowly. Whole-passage deep reading first is a luxury the clock rarely affords.
- Resist your expertise. Your knowledge of how government data policy actually works is the very thing the Cannot Say option is calibrated to catch. Answer from the page, not from the career.
- When two answers feel close, re-read the statement one more time before the passage. In the majority of near-miss errors at senior level, the statement contains a quantifier, modal verb, or scope word ("all", "must", "only", "solely") that the candidate registered on first reading as weaker or broader than it actually is. Thirty seconds spent re-reading the statement is almost always better spent than thirty seconds re-reading the passage.

### Common pitfalls

- **Making assumptions**: importing personal knowledge of standards, governance, or how departments behave instead of relying only on the provided text. The strongest candidates for this trap are the most experienced ones - which means you.
- **Converting possibility into fact**: reading "may grant exemptions" as "has granted exemptions", or "believes a mapping can be constructed" as "a mapping exists".
- **Misinterpreting nuance**: confusing a likely outcome, an estimate, or an expectation stated in the text with an absolute fact - and equally, failing to treat the passage's own assertions as true within the test's closed world.
- **Scope slippage**: applying an obligation to a subject the text does not bind (Question 9), or reading an exclusion more broadly than its exact wording allows (Question 11).
- **Poor time management**: reading every passage exhaustively before looking at the questions. Statement-first scanning is faster and more accurate.
- **Answer symmetry bias**: expecting equal numbers of True, False, and Cannot Say. Real tests are not balanced; judge each item strictly on its own text, even if it gives you four consecutive answers of the same kind.

## Workplace job-specific situational judgement assessment

### About this assessment

A workplace job-specific situational judgement assessment evaluates your decision-making, interpersonal skill, and professional conduct through realistic workplace dilemmas. Unlike the logic and numeric tests, there is often no single objectively right answer: several responses may seem reasonable, and the task is to identify which behaviour best fits the role's responsibilities and the organisation's values. Response formats vary: you may be asked to pick the most effective and least effective actions from a set, or to rank or rate every option from best to worst. Timing is usually generous or untimed, because the assessment is interested in your natural judgement rather than your speed.

For a chief data architect, the scenarios are drawn from the genuine dilemmas of senior data leadership in the UK public sector: an assurance finding that collides with a ministerial commitment; two directors general with incompatible data models and equal seniority; an innovation you believe in but whose timing is wrong; a data architecture community losing faith in its standards; a governance body asking you to soften a risk. The values against which options are judged are the values of government digital and data work: user needs first, transparency and candour, collaboration across boundaries, accessibility and inclusion, evidence-based decisions, and responsible stewardship of public money and citizens' data.

Two calibration points before you begin. First, effective options at chief level usually act through the right mechanism - governance bodies, accountable owners, standards, and communities - rather than through personal heroics; but they also do not hide behind process when direct senior-to-senior conversation is what the moment requires. Second, least effective options tend to share a signature: they delay action without gaining information, pass a problem to someone who cannot own it, solve the visible symptom while entrenching the underlying divergence, or protect short-term comfort at the cost of transparency.

### What it measures for your role

Mapped to the skills in your role profile:

- **Communicating between the technical and non-technical**: managing expectations of diverse senior stakeholders, choosing when to host the difficult discussion yourself, and handling active and reactive communication under pressure.
- **Data governance (data architect)**: routing decisions through the right governance mechanisms, aligning data governance with wider governance, and providing risk mitigation through assurance rather than personal veto.
- **Data standards**: deciding where to hold the line on compliance, where exceptions serve the organisation, and how to keep standards credible while enforcing them.
- **Problem management**: anticipating problems, defending against them at the right time, and building problem-solving capabilities in others rather than solving everything personally.
- **Strategic thinking**: keeping decisions aligned to the data strategy and the larger picture, especially when local pressures argue for expedient divergence.
- **Data innovation**: judging the appropriate timing for adoption - neither chilling innovation nor gambling the enterprise on the unproven.
- **Communicating data**: presenting options with risks and uncertainties honestly, even when a simpler story would be easier to sell.

### Practice questions

**Question 1 (moderate) - The assurance finding and the ministerial deadline**

Your enterprise assurance review finds that a flagship programme's data model handles citizen consent in a way that diverges from the enterprise architecture and will make future cross-service consent management costly. The programme's public beta launches in six weeks, tied to a ministerial announcement. The programme director asks you to hold the finding back until after launch "to avoid destabilising the team".

Options:

A) Agree to hold the finding back; raise it at the first post-launch review.
B) Publish the finding through the normal assurance route now, and simultaneously offer the programme director a proportionate remediation path that does not require moving the launch date.
C) Escalate directly to the permanent secretary that the programme is non-compliant and should be paused.
D) Tell the programme director you will soften the wording of the finding so it reads as an observation rather than a divergence.

**Most effective: B. Least effective: A.**

**Explanation:** B honours transparency while managing expectations - the essence of communicating between the technical and non-technical. The finding enters governance unaltered, so the assurance mechanism keeps its integrity, while the remediation path shows you distinguish the finding (non-negotiable) from the response (negotiable, proportionate, launch-compatible). A is least effective: suppressing an assurance finding at a stakeholder's request corrodes the entire assurance mechanism you are accountable for - if findings can be timed for convenience, none of them can be trusted, and the divergence compounds silently during exactly the period when remediation is cheapest. C is disproportionate as a first move: it spends senior capital, bypasses the governance body that directs your work, and demands a pause the finding may not justify. D is worse than it looks: quietly recategorising a divergence is a falsification of the assurance record, more insidious than delay because it never surfaces at all.

**Question 2 (moderate) - Two directors, two models**

Two directorates have each built their own "organisation" data model, and both directors - your peers - insist theirs becomes the enterprise standard. Integration costs are mounting. Each director has hinted that they expect your support. The data strategy is silent on which model should win.

Options:

A) Back the technically superior model and announce your decision to both directors.
B) Convene a time-boxed, criteria-based evaluation under the Data Design Authority, with both directorates agreeing the criteria before either model is assessed, and commit publicly to adopting the outcome.
C) Propose both models coexist, with a translation layer maintained between them, revisiting the question next year.
D) Ask the governance body to choose, presenting both models without a recommendation to avoid the appearance of bias.

**Most effective: B. Least effective: C.**

**Explanation:** B does three senior things at once: it moves the contest from personality to criteria, it uses the legitimate mechanism (the DDA you lead) so the losing director can accept the outcome without losing face, and agreeing criteria before assessment is the classic device for making a contested decision procedurally fair - this is hosting the difficult discussion rather than avoiding it. A may pick the right model but by the wrong mechanism: an announced personal verdict between two peers converts a design question into a political grievance and undermines the standards-setting process you are supposed to champion. D is weak in a different way: the governance body directs you, but it relies on you for exactly this recommendation; arriving without one abdicates your role and usually produces a worse-informed decision. C is least effective because it institutionalises the divergence - a permanent translation layer is the mounting integration cost made policy, and "revisit next year" is delay without new information. Reuse and alignment of models is your accountability; C abandons it.

**Question 3 (hard) - The innovation your team loves**

Your data architecture community is enthusiastic about an open-source semantic-layer technology and several architects have begun using it in project work. Your own analysis, exercising your data innovation skill, is that the technology is promising but eighteen months from the maturity your enterprise needs, and unmanaged adoption is already creating unassured variation across projects.

Options:

A) Prohibit use of the technology until it reaches maturity, citing your analysis.
B) Establish a bounded pilot: two named projects, explicit evaluation criteria, a defined review date, and a community-visible write-up - while requiring all other projects to hold to current standards in the meantime.
C) Let adoption continue organically; the community's enthusiasm is evidence, and intervening would damage morale.
D) Adopt the technology as an enterprise standard now to get ahead of the divergence.

**Most effective: B. Least effective: D.**

**Explanation:** B is the textbook expression of "identify areas of innovation in data tools and techniques, and recognise appropriate timing for adoption": it converts scattered enthusiasm into a controlled experiment that generates the evidence a future adoption decision needs, keeps the enterprise assured meanwhile, and treats the community as partners - the pilot's visibility builds problem-solving capability in others rather than hoarding judgement at the top. A is defensible but heavy-handed: prohibition without a path to yes drives experimentation underground and spends your credibility with the community whose standards and ways of working you set. C confuses enthusiasm with evidence and lets unassured variation - the actual current harm - continue. D is least effective: standardising on technology you assess as eighteen months immature gambles the enterprise architecture to resolve a community-management problem, inverting the duty of care you owe as the accountable assurer.

**Question 4 (moderate) - The governance paper you are asked to soften**

You have drafted a paper for the data governance board stating that the organisation's metadata repository coverage has stalled at 60% and that two critical domains have no metadata stewardship at all. A senior colleague who reviews board papers suggests you "reframe the risks more positively" because the board "responds badly to red status reports".

Options:

A) Keep the risks stated plainly, but restructure the paper so each risk is paired with a costed, decision-ready mitigation option for the board.
B) Accept the reframing; a paper that lands well achieves more than a paper that is right.
C) Refuse to change anything and submit the original draft.
D) Withdraw the paper from this cycle and resubmit when the coverage figures improve.

**Most effective: A. Least effective: D.**

**Explanation:** A embodies communicating data at chief level: "understand and communicate different options, taking into account risks and uncertainties" - the risks stay honest, and pairing each with a decision-ready mitigation is what actually helps a board act rather than flinch; it also respects the legitimate kernel of your colleague's advice (boards need agency, not alarm) without the dishonest part. B trades the board's information quality for comfort - a governance body directed by softened data directs badly, and the eventual correction costs far more credibility than the red status would have. C keeps the content honest but wastes the genuine insight that presentation affects decisions; refusing all change is rigidity, not integrity. D is least effective: it deprives the board of material facts for a full cycle purely to manage optics, leaving critical domains unstewarded and unfunded precisely because the paper reporting the problem was withheld - transparency delayed into uselessness.

**Question 5 (hard) - The cross-government reuse opportunity**

At a cross-government architecture forum, you discover another department has a mature, well-documented data model for a domain your organisation is about to model from scratch, at an estimated cost of £400,000. Adopting theirs would save most of that, but it would mean accepting some modelling conventions that differ from your organisation's house style, and your own team is keen to build.

Options:

A) Commission your team to build in-house as planned; alignment with house conventions matters more than reuse.
B) Initiate a structured evaluation of the other department's model against your actual requirements, involve your team in running it, and if it fits, adopt with a documented mapping of convention differences.
C) Adopt the other department's model immediately by direction, cancelling the in-house work.
D) Ask your team to study the other department's model for ideas, then build your own version incorporating the best of it.

**Most effective: B. Least effective: A.**

**Explanation:** Your role profile is explicit: work across government, recognising opportunities for the reuse and alignment of data models in different organisations. B pursues that duty properly - evaluation against real requirements rather than either reflexive adoption or reflexive rejection, and involving the team converts a threat to their build ambitions into shared analytical work, managing internal expectations while you manage external alignment. C gets to the probable right answer by the wrong route: adoption by direction without evaluation risks a poor fit and buys team resentment that will surface as passive resistance during implementation. D sounds collaborative but is quietly the most expensive option - it spends most of the £400,000 anyway and yields a third variant model, adding to cross-government divergence in the name of learning from it. A is least effective: spending £400,000 of public money to preserve house style, without even evaluating the alternative, fails the reuse duty, the stewardship of public funds, and the strategic alignment your role exists to provide.

**Question 6 (moderate) - The problem nobody owns**

Duplicate citizen records are causing operational incidents. Investigation shows the root cause spans three teams: a source system, the matching service, and an analytics pipeline - each team insists the defect is elsewhere, and each has closed its ticket. The service desk keeps reopening incidents. This has run for six weeks.

Options:

A) Assemble the three teams, facilitate a joint diagnosis to build a shared description of the end-to-end problem, agree a single problem owner with a cross-team action plan, and take the systemic lesson into your governance processes.
B) Direct your own architecture team to diagnose the fault and hand each team its fix.
C) Escalate to the three teams' directors that their teams are failing to cooperate.
D) Add the issue to the enterprise risk register and review it at the next quarterly governance board.

**Most effective: A. Least effective: D.**

**Explanation:** This is your problem management skill made flesh: "identify and describe problems, and help others to describe them" and "build problem-solving capabilities in others". A treats the real defect - a problem that fits between organisational boundaries and therefore has no describer and no owner - and fixes both the instance and the pattern; facilitating the joint diagnosis rather than performing it yourself is what builds capability that outlasts the incident. B might resolve this incident faster but teaches the organisation that cross-boundary problems are the chief architect's personal job, guaranteeing you the next hundred of them. C escalates the blame dynamic rather than the problem: directors told their teams are "failing to cooperate" defend their teams, and the diagnosis you actually need becomes harder. D is least effective: after six weeks of live operational harm, routing the issue into a quarterly review cycle is delay dressed as governance - registers record risks; they do not resolve incidents.

**Question 7 (hard) - The standard nobody follows**

The address data standard you published eighteen months ago has 30% adoption. Project teams tell your architects, informally, that the standard is too rigid for their delivery timescales, but no formal exemption has ever been requested. Your community of practice has begun quietly advising teams on "pragmatic workarounds".

Options:

A) Enforce the standard: instruct assurance gates to fail any system that does not comply, with immediate effect.
B) Treat the adoption failure as evidence about the standard itself: commission a rapid review with the teams that avoided it, revise the standard or its exemption route where the criticism is fair, then re-launch with the community advocating for it and assurance gates enforcing it thereafter.
C) Withdraw the standard, since a standard with 30% adoption is doing more harm than good.
D) Ask the community of practice to stop advising workarounds and to report teams that use them.

**Most effective: B. Least effective: D.**

**Explanation:** Your role sets "the standards and ways of working for the data architecture community", and this scenario tests whether you understand that standards govern by consent as much as by mandate. B reads the situation correctly: 70% avoidance with zero exemption requests is diagnostic - the formal route is not credible, and the informal workaround economy is the community routing around a defect in your standard or its processes. Reviewing with the avoiders, fixing what is fairly criticised, then enforcing what survives gives you a standard that is both legitimate and enforced - deciding "how to set" standards, not just what they say. A enforces a possibly defective standard and will convert quiet workarounds into open conflict at every assurance gate, with you defending rigidity you have not re-examined. C overcorrects: withdrawal abandons the interoperability need the standard exists to serve. D is least effective: it turns your community of practice - your primary instrument for building capability and consent - into an informant network, destroying the trust that makes a community function, while doing nothing about why teams avoid the standard.

**Question 8 (moderate) - The non-technical audience**

You have twenty minutes with the departmental executive committee to secure £1.2 million for the metadata repository programme. Your slot follows a difficult finance discussion. The committee includes no technical members. Your draft deck has fourteen slides of architecture diagrams and repository coverage metrics.

Options:

A) Present the deck as drafted; the committee should see the technical evidence behind the request.
B) Rebuild around three things the committee governs: what the organisation cannot currently do (with two concrete service examples), what the £1.2 million buys in capability and risk-reduction terms, and what they are being asked to decide today - holding the technical detail in an annexe.
C) Ask a well-regarded operational director who benefits from the repository to co-present the case with you.
D) Reduce the request to £600,000 to make approval easier after the difficult finance discussion.

**Most effective: B. Least effective: D.**

**Explanation:** This is the purest test of communicating between the technical and non-technical and communicating data: "turn complex data into clear and well understood solutions, which can be acted upon". B translates architecture into the committee's own decision language - capability, risk, money, and a specific ask - which is what "acted upon" means; the annexe respects scrutiny without forcing it. C is genuinely strong and in real life often combines with B: a benefiting operational voice is powerful advocacy; it ranks second only because co-presentation without B's restructuring still delivers the wrong deck. A mistakes evidence for communication - fourteen technical slides to a non-technical committee after a bruising finance item is how good programmes lose fundable arguments. D is least effective: halving the request because of the meeting's mood, rather than because the programme needs less, guarantees an underfunded programme and teaches the committee that your numbers are negotiable ambience rather than costed need - undermining every future ask.

**Question 9 (hard) - The strategy drifting out of date**

The organisation's data strategy, which you are accountable for supporting and aligning to, predates a machinery-of-government change that transferred a major service into your department. Programmes are now making architecture decisions the strategy does not cover, each inventing its own direction. Refreshing the strategy formally would take the governance body six months.

Options:

A) Instruct programmes to pause architecture decisions in uncovered areas until the strategy refresh completes.
B) Issue interim architecture positions for the uncovered areas under your own authority now, explicitly labelled as interim, while initiating the formal strategy refresh through the governance body and feeding the interim positions into it as evidence.
C) Allow programmes to proceed on their own judgement and reconcile the divergence during the strategy refresh.
D) Draft the refreshed strategy yourself and circulate it as final, bypassing the six-month governance cycle given the urgency.

**Most effective: B. Least effective: D.**

**Explanation:** Strategic thinking at this level means "define strategies and policies, providing guidance to others on working in the strategic context" - including when the context has a hole in it. B fills the vacuum with legitimate, clearly-labelled interim guidance (a recognised device precisely because it separates speed from permanence), keeps programmes moving, and strengthens rather than bypasses the governance body by feeding it evidence. A stops delivery for six months to protect strategic tidiness - the cost lands on services and users, and the pause is rarely enforceable anyway. C is the quiet failure mode: six months of uncoordinated decisions creates exactly the divergence that costs millions to unwind, and "reconcile later" is problem deferral, not problem management. D is least effective: your role sets the vision "as directed by the appropriate governance body"; a self-issued final strategy is a constitutional overreach that, once noticed, undermines both the strategy's legitimacy and yours - and at the most senior levels, legitimacy is the currency everything else is bought with.

**Question 10 (hard) - Ranking: the data-sharing request**

A policy director urgently requests that citizen data from your systems be shared with another department for a cross-government initiative the Minister supports. Your metadata repository shows the receiving purpose was not among those notified for this data. The director says legal can "catch up with the paperwork" after sharing begins.

Rank all four options from most to least effective:

A) Share the data now on the director's assurance, and ask legal to regularise it afterwards.
B) Decline to share until the lawful basis is established; immediately convene data protection, legal, and the receiving department to establish it at pace, and give the director a dated plan within 48 hours.
C) Share a fully anonymised or aggregated extract now if one can satisfy the initiative's immediate need, while the lawful basis for record-level sharing is established in parallel.
D) Refuse the request and report the director's suggestion to the permanent secretary as a data protection incident.

**Most effective ranking: B, C, D, A.**

**Explanation:** B leads because it is a "no, and here is how we get to yes fast" - it protects citizens' data and the department's lawfulness while treating the Minister's initiative as the legitimate priority it is; the dated plan is what makes the refusal constructive rather than obstructive, and it exercises your governance skill of providing mitigation through assurance mechanisms. C is a close second and in practice often accompanies B: a privacy-preserving extract may genuinely unblock the initiative - it ranks below B only because offered alone it risks being treated as the permanent answer, quietly deferring the lawful-basis work. D protects the data but torches the relationship and misreads the situation: a director pushing for speed is a stakeholder to be managed and educated, not reported - your role hosts the difficult discussion before escalating it; escalation is the tool you hold in reserve if pressure continues after refusal. A is last and decisively so: sharing citizens' data without an established lawful basis, on a promise of retrospective paperwork, is the one option that converts a manageable governance problem into an actual breach - unlawful, corrosive of public trust, and precisely what your accountability for data governance exists to prevent. Note the general lesson of the ranking: options that find a fast, lawful path to the stakeholder's goal outrank both capitulation and confrontation.

**Question 11 (moderate) - Building capability versus doing the work**

A talented but inexperienced domain architect brings you a draft data model for a politically visible service. It has a significant flaw in its handling of temporal data that will cause reporting errors. The assurance gate is in two weeks. You could correct the model yourself in an afternoon.

Options:

A) Correct the model yourself and send it back with the changes marked, given the deadline.
B) Book a working session where you help the architect discover the flaw through questions, let them redesign it with your review before the gate, and add temporal modelling to the community's development curriculum.
C) Send the model back marked "not ready for assurance" with a note to review the temporal design.
D) Ask a more senior architect on your team to take over the model.

**Most effective: B. Least effective: D.**

**Explanation:** Your problem management skill includes "build problem-solving capabilities in others", and at chief level developing the community is not a nice-to-have - it is how the organisation scales beyond your personal capacity. B achieves everything at once: the flaw is fixed ahead of the gate, the architect learns temporal modelling at the deepest level (guided discovery), their confidence and ownership survive, and the curriculum addition converts one person's gap into community capability - the systemic move that distinguishes a chief architect from a senior reviewer. A fixes the model but teaches nothing except that the chief will catch and correct your errors; it also quietly tells a talented architect their work is taken from them when it matters. C provides the least help of the developmental options: a bare "not ready" with a hint leaves an inexperienced architect to struggle against a deadline, risking both the gate and their morale. D is least effective: removing the architect from a visible piece of work signals - to them and to everyone watching - that visibility is reserved for the already-senior, which is precisely how organisations fail to grow the next generation and how communities learn that stretch work is dangerous to accept.

**Question 12 (hard) - The vendor briefing and the governance body**

A major supplier briefs your governance body directly, claiming their platform "eliminates the need for enterprise data modelling" and proposing a proof of concept using live citizen data. Two board members are enthusiastic and ask why your team's modelling programme is still necessary. You are given ten minutes at the next board to respond.

Options:

A) Use the ten minutes to rebut the supplier's claims point by point, demonstrating the technical inaccuracies in their briefing.
B) Acknowledge what is genuinely promising in the technology, explain in the board's own terms what enterprise modelling protects (interoperability, lawful data use, exit costs), propose evaluating the platform through the organisation's standard innovation route using synthetic data, and offer criteria by which the board can judge any such claim in future.
C) Advise the board that supplier briefings should be routed through your team in future to prevent misinformation.
D) Support the proof of concept as proposed, since the board's enthusiasm makes resistance politically costly.

**Most effective: B. Least effective: D.**

**Explanation:** B is senior stakeholder communication under adversarial conditions: it refuses the trap of a defensive technical rebuttal, gives the board decision-language rather than architecture-language, converts the supplier's momentum into your governed innovation route (with synthetic rather than live citizen data - a non-negotiable you install without drama), and - the genuinely strategic move - equips the board with evaluation criteria, building their capability to resist the next overclaiming briefing without you in the room. A wins the argument and loses the audience: ten minutes of point-by-point rebuttal to enthusiastic non-technical board members reads as territorial defensiveness, however accurate. C may even be sensible policy, but as your ten-minute response it sounds like gatekeeping to a board already wondering if you are the bottleneck. D is least effective: it waves live citizen data into an unevaluated supplier proof of concept - a governance and data protection failure - and concedes the premise that your modelling programme needs no defence, purely to avoid discomfort. Political cost deferred at that price compounds.

### Preparation tips

- Before the assessment, write down the five values you believe should govern your decisions in role - for example: citizens' data protected, governance bodies honestly informed, standards credible and consented to, capability built in others, public money stewarded. Most scenario options can be sorted quickly against a list like this.
- Rehearse the "no, and here is the path to yes" pattern. At chief level, the most effective option is very often the one that holds the line and offers a fast, legitimate route to the stakeholder's underlying goal.
- Watch for the mechanism, not just the outcome. Options that reach a good outcome by overreach (deciding what a governance body should decide, personally fixing what a team should learn to fix) usually rank below options that reach it legitimately.
- Read every option before rating any. SJT distractors are written to sound strong in isolation; their weakness appears only in comparison.
- Answer as the role, not as your most cautious self. Assessors calibrate against effective chief-level behaviour, which is candid, proportionate, and decisive - not maximally defensive.
- Reflect afterwards. These scenarios are close enough to your real work that your answers are information about your leadership habits, not just your test technique.

### Common pitfalls

- **Answering idealistically**: choosing the option that sounds noble rather than the one that is practically effective - refusing all compromise, escalating every conflict, or demanding pauses the organisation cannot afford.
- **Selecting passive options**: quarterly reviews, risk-register entries, and "revisit next year" appear responsible but are usually delay without information gain - the classic least-effective signature.
- **Solving it all personally**: at chief level, options where you do the work yourself (fix the model, diagnose the fault, write the strategy alone) usually score below options that work through governance, ownership, and capability-building.
- **Ignoring the values context**: UK public sector scenarios reward transparency with governance bodies, protection of citizens' data, cross-government collaboration, and stewardship of public money - an option can be commercially astute and still wrong against these values.
- **Punishing stakeholders for pressure**: reporting, rebuking, or bypassing a stakeholder who pushes back is rarely most effective as a first move; hosting the difficult discussion is your job before escalation is.
- **Over-reading the scenario**: answer the dilemma as written, without inventing facts ("perhaps the deadline could move") that the scenario does not offer.

## Conclusion

You have now worked through four substantial assessment domains, each grounded in the real substance of your role as chief data architect: a cognitive assessment built from the data models, standards registers, lineage chains, and assurance findings you handle daily; a numeric assessment drawn from the budgets, capacity figures, compliance rates, and business cases through which your strategy is argued and funded; a verbal assessment built from the strategies, standards, governance papers, and senior correspondence in which your profession lives; and a situational judgement assessment reflecting the genuine dilemmas of senior data leadership - assurance under political pressure, contested models, innovation timing, community trust, and the stewardship of citizens' data.

If you attempted the questions actively, you have done more than prepare for a test. You have rehearsed the disciplines the role itself demands: reasoning from evidence rather than assumption, distinguishing what follows necessarily from what is merely plausible, checking arithmetic against operational reality, reading normative language forensically, and choosing actions that work through legitimate mechanisms while keeping stakeholders moving. Notice which sections felt effortless and which required care - that contrast is useful professional self-knowledge, whatever any formal assessment says.

Some encouragement for next steps. First, revisit the questions you got wrong in a week's time; the reasoning patterns consolidate on the second pass. Second, keep converting your own work artefacts into practice material - each governance paper, dashboard, and assurance report you handle is a free rehearsal. Third, share this practice with your data architecture community: setting standards and ways of working includes modelling how senior professionals keep their own capabilities sharp, and working through scenarios together builds exactly the shared judgement your community needs. Finally, hold the assessments in perspective. They measure important capabilities, but they sample them; your track record of models assured, standards adopted, and difficult discussions well hosted is evidence too.

You operate at the most senior level of a demanding profession, and the fact that you have worked through this document carefully is itself evidence of the professional seriousness the role requires. Prepare well, trust your preparation, and go and do yourself justice.
