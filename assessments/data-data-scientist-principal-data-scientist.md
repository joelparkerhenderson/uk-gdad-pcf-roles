# Data Scientist (Principal Data Scientist) - Psychometric Assessment Resources

## Introduction

Welcome. This document is a practical preparation and self-development resource for you as a principal data scientist working within the UK Government Digital and Data (GDAD) profession. Whether you are preparing for an internal assessment, applying for a new post, benchmarking your own capability, or simply curious about how psychometric instruments relate to your day-to-day leadership of data science, this guide is written directly for you.

Psychometric assessments are structured, standardised measures of the mental capabilities and behavioural judgement that underpin performance in a specific role. They are widely used across the Civil Service and the broader public sector because they offer an objective, evidence-based complement to interviews and application sift. For a principal-level role such as yours, they are rarely about raw speed of mental arithmetic; instead they probe whether you can interpret complex evidence quickly, reason precisely from dense written material, weigh competing priorities, and exercise sound judgement in situations involving stakeholders, ethics, delivery pressure, and team leadership.

This document covers four assessment types, each in its own section:

1. **Workplace job-specific cognitive assessment** - your general problem-solving ability applied to data science artefacts: model outputs, pipelines, experimental designs, prioritisation trade-offs, and error checking.
2. **Workplace job-specific numeric reasoning assessment** - your ability to interpret tables, budgets, model performance metrics, capacity figures, and evaluation statistics of the kind you critique and present every week.
3. **Workplace job-specific verbal reasoning assessment** - your ability to draw strictly accurate conclusions from dense written material: data ethics policies, technical standards, delivery reports, and stakeholder correspondence.
4. **Workplace job-specific situational judgement assessment** - your behavioural judgement in realistic dilemmas involving team leadership, ethics and privacy, delivery priorities, and cross-organisational collaboration.

Each section explains what the assessment measures, maps it explicitly to the GDAD skills for your role, offers a substantial set of practice questions with full worked explanations, and closes with preparation tips and common pitfalls.

How to use this resource: work through the practice questions under gentle time pressure first, then review the explanations carefully - the reasoning matters more than the score. Use the questions as prompts for self-reflection: they are drawn from the genuine duties of a principal data scientist, so any area of discomfort is also a professional development signal. Revisit sections before real assessments, and consider using the scenarios as coaching material with the data scientists you manage - explaining reasoning to others is one of the best ways to sharpen your own.

You already operate at a senior level. Treat this document as a structured mirror: a way to see your own reasoning habits clearly, refine them, and walk into any assessment with calm confidence.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive assessment measures the core mental processes your role demands, using materials that mimic your actual work rather than abstract puzzles. Instead of rotating shapes or completing number sequences in isolation, you will reason about model evaluation tables, pipeline dependency diagrams, experimental designs, data quality checks, and delivery prioritisation problems - the artefacts a principal data scientist genuinely handles.

Typical format: an online, timed test of roughly 15 to 30 minutes, with objective scoring against a norm group of professionals at a comparable level. Many modern platforms are adaptive, adjusting difficulty as you answer, and employers usually receive a breakdown of speed versus accuracy rather than a single number. Questions are validated so that they predict job performance without bias, and you will normally get a few ungraded practice items to learn the interface before the clock starts.

Why it matters for your role: as a leader of data science you are the person others rely on to spot the flaw in an analysis, to see the dependency that will sink a delivery plan, to notice that a metric is being computed on the wrong denominator, and to decide - quickly and defensibly - what your team should do first. Cognitive assessments sample exactly these capabilities: pattern recognition, logical deduction, error checking, prioritisation, and structured problem solving under time pressure.

### What it measures for your role

The assessment dimensions map directly onto the GDAD skills for a principal data scientist:

- **Applied maths, statistics and scientific practices**: logical deduction about experimental designs, model outputs and statistical claims; spotting when a conclusion does not follow from the evidence; critiquing analyses at a glance.
- **Data engineering**: reasoning about pipeline dependencies, data cleansing sequences, reusable checks, and how failures propagate through architectures spanning cloud and on-premise components.
- **Programming and build (data science)**: error checking in code review situations, tracing logic through processing steps, evaluating whether an implementation matches a specification, and reasoning about efficiency and optimisation.
- **Understanding product delivery**: prioritisation under constraints, dependency ordering, defining the minimum viable product, and distinguishing critical-path work from noise.
- **Delivering business impact**: selecting which problem to solve first when several compete, and recognising which piece of evidence actually answers the organisational question.
- **Data science innovation**: pattern recognition across unfamiliar problem shapes - the mental agility that lets you match a new problem to a known technique.

### Practice questions

Work through these under light time pressure (aim for roughly two minutes per question, longer for the hard ones). Full explanations follow each question - read them even when you answer correctly, because the reasoning pattern is the thing being trained.

#### Question 1 (easy) - Error checking in a metrics table

Your team circulates a model card for a classifier that flags benefit claims for manual review. It reports: Precision 0.80, Recall 0.75, True Positives 480, False Negatives 320, False Positives 120.

Which reported metric is inconsistent with the raw counts?

- A) Precision
- B) Recall
- C) Both are consistent
- D) Both are inconsistent

**Correct answer: B) Recall.**

**Explanation:** Recalculate each metric from its definition using the raw counts. Precision = TP / (TP + FP) = 480 / (480 + 120) = 480 / 600 = 0.80, which matches the card. Recall = TP / (TP + FN) = 480 / (480 + 320) = 480 / 800 = 0.60, which does not match the reported 0.75. So precision is consistent and recall is overstated. The skill being tested is the verification habit: compute the definition from first principles rather than trusting the summary. Overstated recall on a manual-review classifier is not a cosmetic error - it means far more genuine cases are being missed than the card claims, which changes the operational risk picture you would present to stakeholders. When you meet a question like this in a live test, do the two divisions: they take fifteen seconds and are decisive. Senior candidates skip recalculation more often than junior ones - overconfidence is the principal-level failure mode, and critiquing statistical analyses is explicitly part of your skill set.

#### Question 2 (easy) - Pipeline dependency ordering

A new data science product requires these steps: (1) ingest raw case data from the operational system; (2) apply the personal-data minimisation transform; (3) train the model; (4) run the reusable data-quality checks; (5) generate features. Policy requires that no personal data reaches the feature store, and quality checks must run on cleansed data.

Which ordering is valid?

- A) 1, 4, 2, 5, 3
- B) 1, 2, 4, 5, 3
- C) 1, 5, 2, 4, 3
- D) 2, 1, 4, 5, 3

**Correct answer: B.**

**Explanation:** Constraint one: minimisation (step 2) must precede feature generation (step 5), because no personal data may reach the feature store. Constraint two: quality checks (step 4) must run on cleansed data, so 4 must come after 2. Ingestion (1) necessarily comes first - you cannot transform data you do not hold, which eliminates D. Option A runs quality checks before minimisation, violating constraint two. Option C generates features before minimisation, violating constraint one. Option B gives 1 → 2 → 4 → 5 → 3: ingest, minimise, check, build features, train. Both constraints hold. This is the data engineering reasoning you apply when designing pipelines with data engineers: express the policy and technical requirements as ordering constraints, then check candidate designs against them mechanically.

#### Question 3 (moderate) - Logical deduction from experimental results

Your team ran an A/B test on a triage recommendation model. You are told: "If the new model improves mean processing time, we will roll it out nationally. The test showed processing time improved in three regions and worsened in one. Overall mean processing time improved. However, the worsened region handles the most vulnerable users."

Which conclusion follows logically from the stated rollout rule?

- A) The model must not be rolled out because one region worsened
- B) The model will be rolled out nationally, per the stated rule
- C) The rule should be revised before any decision
- D) The model should be rolled out only in the three improved regions

**Correct answer: B.**

**Explanation:** This is pure conditional logic. The rule is "if overall mean processing time improves, then national rollout". The antecedent is satisfied - overall mean improved - so the stated rule commits the organisation to rollout. Options A and D contradict the rule as given; option C may be excellent professional judgement (and in a situational judgement test would likely be the strong answer, given the equity concern about vulnerable users), but the question asks what follows logically from the stated rule, not what you should do. Cognitive assessments frequently test exactly this discipline: separating what the premises entail from what your professional instincts recommend. As a principal you need both faculties - and the ability to know which one a question is asking for. Notice too the real-world echo: this is why you, in your actual role, challenge delivery rules that reduce a decision to a single averaged metric.

#### Question 4 (moderate) - Pattern recognition in data quality failures

Over five weekly runs, your reusable data-quality checks report the following failure counts on an upstream feed: Week 1: 12 failures, all missing-value. Week 2: 24 failures, all missing-value. Week 3: 48 failures, all missing-value. Week 4: 96 failures, all missing-value. Week 5 is about to run.

The upstream team says: "It is random noise; some weeks are worse than others." Which response best reflects the pattern?

- A) Agree - counts vary week to week and five points is too few to conclude anything
- B) The counts double each week, indicating a systematic, growing fault, so expect roughly 192 failures and escalate now
- C) The counts are seasonal and will fall back after month end
- D) The check itself is faulty because real-world failures never follow a clean pattern

**Correct answer: B.**

**Explanation:** The sequence 12, 24, 48, 96 is geometric with ratio 2 - each week exactly doubles the previous. Random noise produces irregular fluctuation, not four consecutive exact doublings; the probability of that pattern arising by chance is negligible. A clean multiplicative pattern suggests a systematic cause that compounds - classic examples include an unbounded retry loop duplicating bad records, a growing backlog being reprocessed each run, or a slowly expanding partition of malformed data. Option C invents an explanation with no support in the data. Option D gets the inference backwards: an overly regular pattern is a reason to investigate the generating process, and "the check is broken" is one hypothesis to test, not a conclusion. The principal-level move is B: name the pattern, project it forward (96 × 2 = 192), and escalate before week five doubles again. This mirrors your real duty to put reusable checks in place and act on what they reveal.

#### Question 5 (moderate) - Prioritisation under constraint

It is Monday morning. Your team of four data scientists has these demands this week:

- Task P: fix a fairness issue found in a live model affecting decisions about real users (2 person-days, must be done by Wednesday)
- Task Q: prepare a demonstration for the executive board on Friday (3 person-days)
- Task R: peer-review a partner team's statistical analysis, promised for Thursday (2 person-days)
- Task S: routine retraining pipeline maintenance (3 person-days, no fixed deadline)
- Task T: respond to an urgent ministerial data request due Tuesday (2 person-days)

Total capacity is 20 person-days but two team members are on training Thursday and Friday (losing 4 person-days), giving 16. Which task should be deprioritised if anything slips?

- A) Task P
- B) Task Q
- C) Task S
- D) Task T

**Correct answer: C) Task S.**

**Explanation:** Total demand is 2 + 3 + 2 + 3 + 2 = 12 person-days against 16 available, so nominally everything fits - but the constraint is not just volume, it is timing. Tuesday and Wednesday deadlines (T and P) consume early-week capacity; the Thursday/Friday training reduces late-week capacity exactly when Q (Friday) and R (Thursday) fall due, so slack is thinnest at the end of the week. Rank by consequence and deadline: T is externally committed and immovable (ministerial, Tuesday); P affects live decisions about real users - user harm outranks internal convenience; R is a promise to a partner team with a hard date; Q is high-visibility but a demonstration can be trimmed in scope rather than dropped. S is the only task with no fixed deadline and no immediate user impact: deferring it costs least and harms no commitment. The reasoning pattern - identify the binding constraint (late-week capacity), rank by user impact and external commitment, cut the task with the cheapest deferral cost - is exactly how you challenge delivery plans and priorities in your real role.

#### Question 6 (moderate) - Code logic tracing

A junior analyst's script processes records as follows: "For each record: if the postcode field is empty, set region to 'Unknown'. Then, if region is 'Unknown', exclude the record from the model training set. Finally, count excluded records and report the exclusion rate against the total ingested."

The feed contains 10,000 records: 800 have empty postcodes, and separately 200 have postcodes that fail to match any region lookup (the script leaves their region blank, not 'Unknown'). What exclusion rate will the script report, and what is the true proportion of records without a usable region?

- A) Reported 8%, true 10%
- B) Reported 10%, true 10%
- C) Reported 8%, true 8%
- D) Reported 10%, true 8%

**Correct answer: A.**

**Explanation:** Trace the logic exactly as written. Only empty-postcode records are set to 'Unknown' (800 records), and only 'Unknown' records are excluded, so the script excludes 800 of 10,000 = 8% - that is what it reports. But 200 further records have unmatched postcodes whose region is left blank rather than 'Unknown'; they silently pass into the training set with no usable region. The true proportion lacking a usable region is (800 + 200) / 10,000 = 10%. So the report understates the problem: reported 8%, true 10%. This is the archetypal supervision catch when you review junior analysts' code: the branch condition ('Unknown') does not cover all the failure states (blank). It also shows why your team's coding standards should require exhaustive handling of lookup failures and why reusable checks should validate the output (every record has a valid region) rather than the mechanism.

#### Question 7 (moderate) - Matching technique to problem

Four problems land on your desk in one week. Match each to the most appropriate technique family, then answer the question below.

- Problem 1: A department wants to group 50,000 free-text complaints into themes with no predefined categories.
- Problem 2: A service team wants to predict which of next month's applications will need manual intervention, using three years of labelled history.
- Problem 3: A policy team wants to understand which factors are most associated with appeal success, with an emphasis on explainability for ministers.
- Problem 4: An operations team wants to detect, in near real time, transactions that look unlike anything seen before.

Which pairing is the LEAST appropriate?

- A) Problem 1 with unsupervised topic modelling / clustering
- B) Problem 2 with supervised classification
- C) Problem 3 with an uninterpretable deep ensemble chosen purely for accuracy
- D) Problem 4 with anomaly detection

**Correct answer: C.**

**Explanation:** Problems 1, 2 and 4 are textbook matches: unlabelled text with no predefined categories calls for unsupervised methods such as topic modelling (natural language processing territory); labelled history predicting a known outcome is supervised classification; "unlike anything seen before" is the definition of anomaly or novelty detection. Problem 3, however, states its binding requirement in the brief: explainability for ministers. Choosing a technique purely for accuracy when the stated user need is explanation fails the requirement - a regularised regression, decision tree, or a model paired with rigorous explanation methods would serve better. The cognitive skill is reading the whole problem statement, identifying the binding constraint, and refusing to let technical enthusiasm override the actual user need - central to both your innovation leadership and your duty to use model outputs to help design services and policies.

#### Question 8 (hard) - Deduction with multiple constraints

You are allocating three data scientists (Asha, Ben, Chloe) to three products (a fraud model, a demand forecast, a text-classification service), one person per product, given:

1. Asha cannot work on the fraud model because of a conflict of interest declared last month.
2. The text-classification service requires NLP experience; only Asha and Ben have it.
3. Ben has asked for a development opportunity away from forecasting, which you have agreed to honour.

Who works on the demand forecast?

- A) Asha
- B) Ben
- C) Chloe
- D) It cannot be determined

**Correct answer: D) It cannot be determined.**

**Explanation:** Work the constraints as eliminations. Constraint 3: Ben is not on the forecast. Constraint 1: Asha is not on the fraud model. Constraint 2: the text service must be Asha or Ben - so Chloe is not on the text service. Chloe is therefore on the fraud model or the forecast. Test both branches. Suppose Chloe takes the fraud model: Asha and Ben fill the forecast and text service; Ben cannot forecast, so Ben takes text and Asha forecasts - a valid assignment (Asha: forecast, Ben: text, Chloe: fraud). Now suppose Chloe takes the forecast: Asha and Ben fill fraud and text; Asha cannot take fraud, so Asha takes text and Ben takes fraud - also valid (Asha: text, Ben: fraud, Chloe: forecast). Two complete assignments satisfy every constraint, and they put different people on the forecast, so the forecast assignment cannot be determined from the information given. This question deliberately punishes premature closure: many strong candidates find the first valid assignment, answer A, and stop. The complete method is to enumerate all assignments consistent with the constraints and only conclude uniqueness when exactly one survives. In your real role this is the difference between "a plan that works" and "the only plan that works" - a distinction that matters when you challenge delivery plans, because a stakeholder who finds the second valid option will use it.

#### Question 9 (hard) - Error propagation reasoning

A daily pipeline has four stages in sequence: ingest → cleanse → feature-build → score. Historically each stage independently completes without error 95% of the time, and any stage failure halts the run. A stakeholder asserts: "Each stage is 95% reliable, so the pipeline is 95% reliable."

What is the approximate probability that a given daily run completes without error, and what is the flaw in the stakeholder's claim?

- A) About 95%; the claim is correct
- B) About 81%; reliability multiplies across sequential dependent stages
- C) About 81%; reliability multiplies across sequential independent stages: 0.95 × 0.95 × 0.95 × 0.95 ≈ 0.815
- D) About 99%; failures in different stages cancel out

**Correct answer: C.**

**Explanation:** For the run to complete, all four stages must succeed. With independent stages, the joint probability is the product: 0.95 to the fourth power = 0.95 × 0.95 = 0.9025; 0.9025 × 0.95 = 0.857375; 0.857375 × 0.95 ≈ 0.8145 - roughly 81%. So about one run in five fails somewhere. The stakeholder's flaw is treating the reliability of a component as the reliability of the chain. Option B gives the right number but the wrong reason - the multiplication rule as stated applies under independence (dependence would change the calculation). Option D is wishful thinking: sequential failures compound; they never cancel. This reasoning underlies your real conversations about delivering supported solutions at scale: a pipeline of individually decent components can be operationally poor, which is why monitoring, retries, and reusable checks exist - and why you can expect roughly one failed morning per working week without them.

#### Question 10 (hard) - Spotting the confound

Your team reports: "Users who received the new AI-assisted guidance completed their applications 30% faster than those who did not. Therefore the guidance causes faster completion, and we should scale it."

The guidance was offered as an opt-in feature, promoted primarily through the digital-confidence email newsletter. Which single observation most seriously undermines the causal claim?

- A) The sample size of the opt-in group is smaller than the comparison group
- B) Opt-in users, recruited via a digital-confidence newsletter, are likely more digitally confident and would complete faster regardless of the guidance
- C) Completion time is a noisy metric that varies day to day
- D) 30% is suspiciously round, suggesting the analysis was approximate

**Correct answer: B.**

**Explanation:** The design is self-selected, not randomised. The route to the treatment (a digital-confidence newsletter) recruits people who differ systematically in exactly the trait - digital confidence - that plausibly drives the outcome. That is a classic selection confound: the comparison is between different kinds of people, not between guidance and no guidance. Option A matters for precision but not validity - a small randomised group would still support causal inference. Option C would widen uncertainty but not bias the comparison in a particular direction. Option D is cosmetic. As the person who critiques statistical analyses before they reach decision makers, the confound is the first thing to name, and the constructive follow-up is a design fix: randomise the offer, or at minimum adjust for pre-existing completion speed and digital-engagement measures, then re-estimate. Scaling on the back of a confounded comparison is precisely the failure your role exists to prevent.

#### Question 11 (hard) - Minimum viable product reasoning

A commissioning director asks for a "complete forecasting platform" with: (a) automated data ingestion from six sources, (b) a forecasting model, (c) an interactive dashboard, (d) automated retraining, (e) role-based access for 200 users, and (f) an API for other departments. Delivery capacity allows roughly two components per quarter. The stated organisational objective is: "give operational managers a credible forecast to plan next quarter's staffing."

Which pair constitutes the strongest MVP for the stated objective?

- A) (a) full six-source ingestion and (d) automated retraining
- B) (b) a forecasting model on the one or two richest sources and (c) a simple way for managers to see and interrogate the forecast
- C) (e) role-based access and (f) the cross-department API
- D) (c) the interactive dashboard and (e) role-based access, with forecasts added later

**Correct answer: B.**

**Explanation:** An MVP is the smallest thing that delivers the stated value and tests the riskiest assumptions. The objective is a credible forecast that managers can use for staffing. That requires two things irreducibly: a forecast (b) and a way for the users to consume it (a minimal version of c). Option A builds plumbing and automation before proving the forecast is worth automating - infrastructure ahead of value. Option C serves secondary users before primary ones. Option D delivers a dashboard with nothing meaningful on it - presentation without substance. Note also what B tests: whether a model on limited sources is credible enough to act on, which is the riskiest assumption in the whole programme; if it fails, you have learned cheaply. This is the "define the MVP and support decisions about priorities" skill in its purest form, and it is also a communication task - you would need to explain to the director why "complete platform" is the destination, not the first step.

#### Question 12 (hard) - Integrated reasoning

Three statements about a live model are all true:

1. Overall accuracy has been stable at 91% for six months.
2. The volume of cases from one demographic group has quadrupled over the same period.
3. Accuracy within that group has always been 78%.

A dashboard tracking only overall accuracy shows no alert. What must be happening to the accuracy in the rest of the population, and what does this imply for your monitoring design?

- A) Rest-of-population accuracy is falling; the dashboard is correct to stay silent
- B) Rest-of-population accuracy must be rising for the overall figure to stay at 91% while a growing share of cases sits at 78%; the dashboard is masking two offsetting movements and needs per-group metrics
- C) Nothing can be inferred; overall accuracy is the only meaningful metric
- D) The group's accuracy must actually be improving, or the overall figure would fall

**Correct answer: B.**

**Explanation:** Overall accuracy is a weighted average of group accuracies. If the weight on a 78%-accuracy group is growing (its volume quadrupled) and the overall average is unchanged at 91%, the remaining population's accuracy must be drifting upwards to compensate - two real movements that exactly offset in the aggregate. This is a mixture effect (closely related to Simpson's paradox): a stable aggregate concealing divergent subpopulations. Option D has the logic backwards - the stated premises fix the group's accuracy at 78%. The monitoring implication is the operationally important part: an aggregate-only dashboard is blind to compositional change, so your team's reusable monitoring should track group-level performance and volume mix, particularly where the low-performing group may correspond to users with protected characteristics - at which point this stops being a statistics puzzle and becomes a data ethics obligation. This single question exercises three of your skills at once: statistical critique, delivering supported solutions at scale, and ethics-aware design.

### Preparation tips

- **Recalculate rather than recognise.** At principal level your pattern recognition is strong enough to be dangerous - you will "see" the answer early. The highest-scoring habit is to spend fifteen seconds verifying with the definition or the arithmetic before committing.
- **Read the question's frame, not just its content.** Several items above turn on whether you are asked what logically follows versus what you would recommend. Identify the frame first.
- **Practise constraint problems on paper.** Allocation, ordering and dependency questions yield instantly to a small grid or list of eliminations; they resist being held in your head under time pressure.
- **Rehearse with your own artefacts.** Take a recent model card, dashboard, or pipeline diagram from your work and ask: what is inconsistent, what would break first, what would I cut? You have an unlimited supply of realistic practice material.
- **Manage the clock like a portfolio.** Bank the easy questions fast, flag the multi-stage ones, and return. A principal who spends four minutes proving one hard item while three easy ones expire has misallocated - exactly the prioritisation instinct the test measures.
- **Sleep and pace beat cramming.** Cognitive throughput is physiological; you cannot revise your way to alertness, but you can protect it.

### Common pitfalls

- **Overconfidence on familiar-looking material.** The questions use your professional furniture - metrics, pipelines, experiments - which tempts you to answer from experience rather than from the stated premises. The test always rewards the premises.
- **Premature closure on constraint problems.** Finding one valid solution is not the same as proving uniqueness (see Question 8). Check whether alternatives survive.
- **Confusing professional judgement with logical entailment.** "The rule should be changed" can be excellent judgement and still the wrong answer to "what follows from the rule?"
- **Time-sink questions.** Multi-stage items like error propagation can consume five minutes if you let them; estimate, answer, flag, and move on.
- **Ignoring stated constraints in prioritisation items.** The binding constraint (a deadline, a policy, an explainability requirement) is usually stated in one quiet sentence. Train yourself to underline it.
- **Assuming aggregates tell the whole story.** As Question 12 shows, stable averages can conceal exactly the movements that matter most - in tests and in production.


## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment evaluates your ability to interpret, analyse, and make sound decisions from numerical data presented the way your job actually presents it: evaluation tables, budget spreadsheets, capacity plans, performance dashboards, and experiment readouts. It is business mathematics, not abstract formulae - percentages, ratios, weighted averages, rates, and cost-benefit estimation applied to realistic material.

Typical format: strictly timed online questions (often around a minute to ninety seconds each), usually calculator-friendly - the test prioritises interpretation and data extraction over mental arithmetic. Inputs are tables, charts and short numerical narratives; the challenge is extracting the right numbers, choosing the right operation, and respecting qualifiers like "in thousands" or "per quarter".

Why it matters for your role: a principal data scientist lives in numbers, but the assessment is not testing whether you can fit a model - it is testing the quick, reliable numerical judgement that surrounds your technical work. Can you sanity-check a budget line in a delivery plan you are challenging? Spot that a claimed percentage improvement uses a convenient baseline? Convert compute costs, team capacity and case volumes into a defensible recommendation in a meeting, without a notebook? At your level you also carry a second responsibility: the numbers you wave through are the numbers your organisation acts on, so your error-checking is the last line of defence before evidence reaches decision makers.

### What it measures for your role

- **Applied maths, statistics and scientific practices**: interpreting model performance metrics, confusion-matrix arithmetic, rates and proportions, weighted averages across segments, and critiquing numerical claims in others' analyses.
- **Delivering business impact**: cost-benefit reasoning about data science products - savings projections, return on investment, and translating model metrics into operational quantities (cases, hours, pounds).
- **Understanding product delivery**: capacity and velocity arithmetic - person-days, sprint maths, MVP scoping under resource constraints, and burn rate against budget.
- **Data engineering**: throughput, storage and compute cost calculations across cloud and on-premise architectures; pipeline volume reconciliation.
- **Developing data science capability**: training budgets, team growth planning, and quantifying capability-building programmes.
- **Data ethics and privacy**: proportion-based reasoning about group-level impacts - the arithmetic that turns an ethics concern into evidence.

### Practice questions

Use a calculator, as most real assessments allow one, but do the setup (which numbers, which operation) yourself before touching it. The arithmetic is shown in full in every explanation.

#### Question 1 (easy) - Percentage change in a performance metric

Your fraud-detection model reviewed 18,500 cases in March and 22,940 in April. What was the percentage increase in cases reviewed?

- A) 19.4%
- B) 24.0%
- C) 22.2%
- D) 4.4%

**Correct answer: B) 24.0%.**

**Explanation:** Percentage change = (new − old) / old × 100. Increase = 22,940 − 18,500 = 4,440. Then 4,440 / 18,500 = 0.24, so 24.0%. Option A (19.4%) is the classic reversed-baseline error: 4,440 / 22,940 = 0.1935, i.e. dividing by the new value instead of the old. Option D mistakes the absolute difference in thousands for a percentage. Baseline discipline - always divide by the starting value - is worth stating explicitly to yourself on every percentage question, because reversed baselines are also how misleading claims get into delivery reports you are asked to critique.

#### Question 2 (easy) - Reading a budget table

Your data science programme budget for the year (in £ thousands):

| Line | Q1 | Q2 | Q3 | Q4 |
|---|---|---|---|---|
| Staff | 210 | 210 | 225 | 225 |
| Cloud compute | 38 | 44 | 52 | 61 |
| Training and CPD | 12 | 8 | 15 | 10 |
| Software licences | 22 | 22 | 22 | 22 |

What percentage of the total annual budget is cloud compute? (Round to one decimal place.)

- A) 16.3%
- B) 19.5%
- C) 21.4%
- D) 13.2%

**Correct answer: A) 16.3%.**

**Explanation:** First sum each line. Staff: 210 + 210 + 225 + 225 = 870. Cloud: 38 + 44 + 52 + 61 = 195. Training: 12 + 8 + 15 + 10 = 45. Licences: 22 × 4 = 88. Total = 870 + 195 + 45 + 88 = 1,198 (£ thousands). Cloud share = 195 / 1,198 = 0.16277… ≈ 16.3%. Note the "in £ thousands" qualifier: the arithmetic is unaffected because it cancels in the ratio, but if a later question asked for the absolute cloud spend the answer would be £195,000, not £195 - scale qualifiers are the single most common source of careless errors in numeric tests. Also notice the trend within the cloud line (38 → 44 → 52 → 61, roughly 15% quarterly growth): the kind of pattern you would raise when challenging next year's delivery plan.

#### Question 3 (moderate) - Confusion matrix to operational workload

A model flags applications for manual review. On a monthly volume of 40,000 applications, 6% are genuinely problematic. The model has recall 0.85 and precision 0.30. How many applications will the manual review team receive per month?

- A) 2,040
- B) 6,800
- C) 2,400
- D) 5,100

**Correct answer: B) 6,800.**

**Explanation:** Work from definitions. Genuinely problematic cases: 40,000 × 0.06 = 2,400. True positives (problematic cases the model catches): 2,400 × 0.85 (recall) = 2,040. Precision = TP / (TP + FP) = 0.30, so total flagged = TP / 0.30 = 2,040 / 0.30 = 6,800. The review team therefore receives 6,800 cases, of which 2,040 are genuine and 6,800 − 2,040 = 4,760 are false positives - a 70% false-alarm rate, exactly as precision 0.30 implies. This translation from model metrics to staffing reality is the arithmetic behind "work with colleagues to implement scalable data science products": if a reviewer handles 25 cases a day, the model implies 6,800 / 25 = 272 reviewer-days per month, and that number - not the recall - is what the operations director needs from you.

#### Question 4 (moderate) - Weighted average across segments

Your text-classification service is used by three departments. Last month: Department A processed 120,000 documents at 94% accuracy; Department B processed 45,000 at 88%; Department C processed 15,000 at 71%. What is the overall accuracy across all documents? (Round to one decimal place.)

- A) 84.3%
- B) 91.6%
- C) 90.6%
- D) 92.4%

**Correct answer: C) 90.6%.**

**Explanation:** A weighted average, weighted by volume - never the simple mean of 94, 88 and 71 (that is 84.3%, option A, the classic trap). Correct documents: A: 120,000 × 0.94 = 112,800. B: 45,000 × 0.88 = 39,600. C: 15,000 × 0.71 = 10,650. Total correct = 112,800 + 39,600 + 10,650 = 163,050. Total documents = 180,000. Overall accuracy = 163,050 / 180,000 = 0.9058… ≈ 90.6%. Beyond the arithmetic, note the professional signal: Department C's 71% is buried by the healthy aggregate. If C's documents concern a vulnerable user group, the weighted average is not just a statistics answer but the start of an ethics conversation - your role's skills connect exactly here.

#### Question 5 (moderate) - Compute cost comparison

You are choosing where to run monthly model retraining. Option 1 (cloud): 140 hours of GPU time at £3.80 per hour, plus £310 fixed monthly storage. Option 2 (on-premise): the server costs £48,000 to buy, has an expected useful life of 4 years, and monthly running costs of £220. Comparing monthly costs (spreading the server purchase evenly over its life), which option is cheaper, and by how much per month?

- A) Option 2 is cheaper by £378
- B) Option 1 is cheaper by £378
- C) Option 1 is cheaper by £158
- D) They cost the same

**Correct answer: B) Option 1 is cheaper by £378.**

**Explanation:** Option 1 monthly: 140 × £3.80 = £532 of GPU time, plus £310 storage = £842. Option 2 monthly: the purchase spread over its life is £48,000 / (4 × 12 months) = £48,000 / 48 = £1,000 per month, plus £220 running costs = £1,220. Difference: £1,220 − £842 = £378 in favour of the cloud option. The commonest error is forgetting to convert years to months (dividing £48,000 by 4 gives an absurd £12,000 "monthly" figure) or ignoring the capital cost entirely, which makes on-premise look artificially cheap at £220. Note also what the arithmetic is sensitive to: if the server's life were 6 years, its monthly cost would fall to £48,000 / 72 + £220 = £886.67, narrowing the gap to £44.67; if two teams shared it equally, your share would be £610 and on-premise would win. Asset-life and cost-sharing assumptions swing these comparisons, which is why, when you challenge a delivery plan's hosting costs, your first questions should be "over what life, and shared with whom?" - exactly the cloud-versus-on-premise judgement your data engineering skill describes.

#### Question 6 (moderate) - Ratios in team planning

Your data science team maintains a ratio of 1 senior to 3 junior data scientists. You currently have 4 seniors and 12 juniors. The organisation asks you to grow the team to 24 people while keeping the same ratio. How many additional seniors and juniors must you recruit?

- A) 2 seniors and 6 juniors
- B) 6 seniors and 18 juniors
- C) 2 seniors and 4 juniors
- D) 4 seniors and 4 juniors

**Correct answer: A) 2 seniors and 6 juniors.**

**Explanation:** A 1:3 ratio means each group of 4 people contains 1 senior and 3 juniors, so seniors are 1/4 of the team and juniors 3/4. Target team of 24: seniors = 24 × 1/4 = 6; juniors = 24 × 3/4 = 18. You have 4 seniors and 12 juniors (16 people, ratio already correct), so recruit 6 − 4 = 2 seniors and 18 − 12 = 6 juniors - 8 hires in total, growing the team from 16 to 24. Option B ignores current staff; option C breaks the ratio (6:16 is not 1:3). This is the workforce arithmetic behind "supporting data science capability building across the team": growth plans, promotion pipelines, and the supervision load implied by every junior hire.

#### Question 7 (hard) - Savings projection with adoption ramp

A business case claims your triage model will save £1.2 million per year, based on saving 15 minutes per case across 480,000 annual cases at a cashable staff cost of £10 per hour. First verify that the headline is internally consistent, then adjust it: in year one the model will only be adopted for 60% of cases, and your evaluation suggests the true time saving is 12 minutes per case, not 15. What is the defensible year-one saving?

- A) £1,200,000
- B) £720,000
- C) £576,000
- D) £480,000

**Correct answer: C) £576,000.**

**Explanation:** Step one, verify the headline: 480,000 cases × 15 minutes = 7,200,000 minutes; ÷ 60 = 120,000 hours; × £10 = £1,200,000. The headline is internally consistent, so the dispute is about the inputs, not the arithmetic. Step two, apply the corrections. Cases actually covered in year one = 480,000 × 0.60 = 288,000. Time saved = 288,000 × 12 minutes = 3,456,000 minutes = 57,600 hours. Value = 57,600 × £10 = £576,000 - option C, less than half the headline. Option B (£720,000) applies the adoption discount but keeps the unsupported 15-minute figure (£1.2m × 0.6); option D (£480,000) comes from over-discounting - treating the 3-minute reduction as if it were a further 1/3 cut rather than the correct factor of 12/15 = 0.8. The quick shortcut is multiplicative factors on the verified headline: £1.2m × 0.6 (adoption) × 0.8 (effect size) = £576,000. The method - verify the headline's own arithmetic, then apply adoption and effect-size corrections as multiplicative factors - is the core of honest benefits estimation, and benefits cases that survive your scrutiny are the ones that survive the Treasury's.

#### Question 8 (hard) - Pipeline volume reconciliation

Your daily pipeline reports: 250,000 records ingested; 4% rejected by cleansing rules; of the cleansed records, 1.5% dropped for failing the deduplication check; the remainder loaded to the feature store. The feature store team reports receiving 236,000 records. Is the pipeline leaking records, and roughly how many?

- A) No leak - the numbers reconcile
- B) Yes - about 400 records are unaccounted for
- C) Yes - about 2,400 records are unaccounted for
- D) Yes - about 10,000 records are unaccounted for

**Correct answer: B) about 400 records.**

**Explanation:** Work the expected flow. After cleansing: 250,000 × (1 − 0.04) = 250,000 × 0.96 = 240,000. After deduplication: 240,000 × (1 − 0.015) = 240,000 × 0.985 = 236,400. Expected at the feature store: 236,400. Reported received: 236,000. Discrepancy: 236,400 − 236,000 = 400 records unaccounted for - about 0.17% of expected volume. Small, but a genuine reconciliation gap: healthy pipelines reconcile exactly, so 400 silent losses per day (roughly 146,000 per year) is a defect to chase, not noise to accept. The common error is applying the 1.5% to the original 250,000 (giving 3,750 dropped and an expected 236,250) - percentage stages apply to the *surviving* volume, not the original. This compounding-of-survivors arithmetic is the same structure as the reliability question in the cognitive section, and it is the numerical backbone of the reusable checks your data engineering skill calls for.

#### Question 9 (hard) - Interpreting an evaluation table under drift

Quarterly evaluation of a live demand-forecast model (mean absolute percentage error, MAPE - lower is better):

| Quarter | Volume forecast MAPE | Data freshness (days lag) | Retraining performed? |
|---|---|---|---|
| Q1 | 6.2% | 2 | Yes |
| Q2 | 6.8% | 2 | No |
| Q3 | 8.9% | 9 | No |
| Q4 | 12.4% | 15 | No |

Error grew by what factor from Q1 to Q4, and which explanation does the table best support?

- A) Factor of 2.0; the model architecture has become obsolete
- B) Factor of 2.0; error growth tracks growing data lag and missed retraining, suggesting stale inputs rather than a broken model
- C) Factor of 6.2; seasonal demand explains everything
- D) Factor of 1.24; no action needed

**Correct answer: B.**

**Explanation:** The factor: 12.4 / 6.2 = 2.0 - error has doubled. (Option D misreads 12.4% as a factor of 1.24; option C confuses the Q1 level with a ratio.) Now the explanation: the table shows two things moving together with error - data lag rising from 2 to 15 days, and retraining stopping after Q1. That covariation supports the mundane operational explanation (stale data, missed maintenance) over the exotic one (architectural obsolescence), and nothing in the table speaks to seasonality at all - concluding seasonality would import outside knowledge, a habit numeric tests punish. The professional reading: before commissioning a redesign, restore freshness and retraining and re-measure. This is "appreciate and understand delivery methods, and how to deliver supported solutions at scale" in numeric form: most model degradation is operations, not science, and the cheapest experiment isolates the operational variable first.

#### Question 10 (hard) - Group-level impact proportions

An automated prioritisation system processes 60,000 applications: 45,000 from Group X (of which 9% are flagged for slower manual processing) and 15,000 from Group Y (of which 15% are flagged). Overall, what percentage of applications is flagged, and how much more likely is a Group Y application to be flagged than a Group X application?

- A) 10.5% overall; Group Y is 1.67 times as likely
- B) 12.0% overall; Group Y is 1.67 times as likely
- C) 10.5% overall; Group Y is 6 percentage points more likely, i.e. 2.5 times as likely
- D) 24.0% overall; Group Y is 1.5 times as likely

**Correct answer: A.**

**Explanation:** Flagged in Group X: 45,000 × 0.09 = 4,050. Flagged in Group Y: 15,000 × 0.15 = 2,250. Total flagged = 6,300 of 60,000 = 10.5%. Relative likelihood (risk ratio): 15% / 9% = 1.667 - a Group Y application is about 1.67 times as likely to be flagged. Option B averages 9 and 15 without weighting (12%); option C states the correct 6-percentage-point gap but converts it to "2.5 times" incorrectly (the ratio is of the rates, not derived from the gap). Distinguishing percentage-point differences from ratios is not pedantry: "6 points higher" and "67% more likely" describe the same data and land completely differently with stakeholders. In your data ethics and privacy work, this is exactly the arithmetic that turns "the system feels unfair to Group Y" into a precise, discussable, and fixable disparity - and choosing the honest framing of it is part of communicating how ethical issues fit the organisational context.

#### Question 11 (hard) - Capacity and burn rate

Your programme has £900,000 remaining budget and a monthly burn of £75,000 (staff) plus £13,000 (infrastructure). A stakeholder requests an additional discovery workstream costing £22,000 per month. If you accept it, in how many whole months does the budget run out, and how many months earlier is that than without the new workstream?

- A) 8 months; 2 months earlier
- B) 8 months; 3 months earlier
- C) 10 months; 1 month earlier
- D) 9 months; 1 month earlier

**Correct answer: A) 8 months; 2 months earlier.**

**Explanation:** Current burn: £75,000 + £13,000 = £88,000/month. Runway without the workstream: £900,000 / £88,000 = 10.23 months - the tenth full month is affordable (10 × 88,000 = £880,000 ≤ £900,000), the eleventh is not, so 10 whole months. With the workstream: burn = £88,000 + £22,000 = £110,000/month. Runway: £900,000 / £110,000 = 8.18 - eight whole months (8 × 110,000 = £880,000 ≤ £900,000; nine would need £990,000). Difference: 10 − 8 = 2 months earlier. The trap is rounding 10.23 to 10 but 8.18 to 8 inconsistently, or comparing the unrounded figures (10.23 − 8.18 = 2.05) and answering "2 months" for the wrong reason - whole-month framing must be applied consistently to both scenarios. This is the arithmetic behind "communicate effectively and challenge delivery plans and priorities": a crisp "that discovery costs us two months of runway" moves a governance board in a way a spreadsheet attachment never will.

#### Question 12 (hard) - Compound growth in demand

Requests to your team's inference API have grown 15% quarter on quarter for the past year, and this growth is expected to continue. The current volume is 2.0 million requests per quarter, and your infrastructure ceiling is 3.5 million per quarter. In which quarter from now does demand first exceed capacity?

- A) Quarter 3
- B) Quarter 4
- C) Quarter 5
- D) Quarter 6

**Correct answer: C) Quarter 5.**

**Explanation:** Compound at 15% per quarter: Q1: 2.0 × 1.15 = 2.30m. Q2: 2.30 × 1.15 = 2.645m. Q3: 2.645 × 1.15 = 3.042m. Q4: 2.0 × 1.15⁴ = 2.0 × 1.74900625 = 3.49801m - *below* the 3.5m ceiling by about 2,000 requests. Q5: 3.49801 × 1.15 = 4.02271m - clearly over. Demand first exceeds capacity in Quarter 5. This is the marginal case that separates careful candidates from quick ones: estimating 1.15⁴ ≈ 1.75 gives "3.5m in Q4, we breach" and the wrong answer B, because 1.15⁴ is actually 1.749 and the ceiling is exceeded only when demand is strictly greater than 3.5m. The operational lesson is double: compound growth reaches ceilings sooner than linear intuition suggests, so always compound rather than adding 0.3m per quarter; and capacity planning near a boundary deserves exact arithmetic, not estimation, because "we breach in Q4" versus "we breach in Q5" is the difference between an emergency procurement and a planned one. In a live test, whenever your estimate lands within a whisker of a threshold, spend the extra twenty seconds computing exactly.

### Preparation tips

- **Set up before you calculate.** Decide which numbers and which operation the question needs, say it to yourself ("weighted average, weighted by volume"), then compute. Most numeric-test errors are setup errors, not arithmetic errors.
- **Verify baselines on every percentage question.** Old value in the denominator for change; survivors in the denominator for staged pipelines; total volume for weighted averages. Three rules cover most of the test.
- **Rehearse metric-to-operations translation.** Practise converting precision/recall into caseloads, minutes saved into pounds, and burn rates into runway. These conversions are your daily work made explicit, and they appear constantly in role-specific numeric tests.
- **Respect qualifiers.** "In thousands", "per quarter", "of the cleansed records", "whole months" - underline them. Test writers put the difficulty in the qualifiers, not the arithmetic.
- **Use the calculator for arithmetic, never for thinking.** Typing faster does not fix a wrong setup. Estimate the order of magnitude first so a keying error announces itself.
- **Practise near boundaries.** Questions that land just above or below a threshold (Question 12) reward exact computation. When an answer sits within a few percent of a boundary, recompute precisely.
- **Bank easy marks first.** The test rewards total correct answers, not heroism on the hardest item. Flag multi-stage questions and return to them.

### Common pitfalls

- **Misreading chart and table labels** - confusing quarterly with annual figures, or ignoring scale qualifiers like "in thousands". At your level the embarrassment risk is real: these are the same misreadings you correct in others' business cases.
- **Unweighted averages of rates.** Averaging 94%, 88% and 71% without volume weights is the single most common error in professional numeric tests - and in real dashboards.
- **Reversed percentage baselines.** Dividing the change by the new value instead of the old understates growth and overstates decline.
- **Applying stage percentages to the wrong population.** Rejection and drop rates apply to survivors of the previous stage, not the original volume.
- **Over-calculating.** Some questions yield to estimation - if options are far apart, an order-of-magnitude check suffices. Save precision for boundary cases.
- **Time-sink questions.** A single multi-stage benefits calculation can eat five questions' worth of time. Estimate, flag, move on, return.
- **Forgetting that you are the audience's last check.** In real work, the numbers you pass through are acted on. Treat the test's verification habits as rehearsal for the genuine responsibility.


## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment measures how accurately you understand, analyse and draw conclusions from written material of the kind your role actually generates: data ethics policies, technical standards, governance board minutes, delivery reports, stakeholder emails, and draft publications. The defining discipline is fact-based logic - you answer strictly from the passage in front of you, setting aside everything you happen to know about the subject, however expert you are.

Typical format: a dense passage followed by statements you must classify as **True** (the passage supports it), **False** (the passage contradicts it), or **Cannot Say** (the passage neither supports nor contradicts it - insufficient information), plus some multiple-choice comprehension items. Timing is tight, often under a minute per question, deliberately simulating workplace reading under deadline.

Why it matters for your role: a principal data scientist is a professional reader and writer of consequential documents. You critique statistical analyses where a single word ("associated with" versus "causes") changes the claim; you assess and constructively challenge proposed data ethics policies, where obligations hide in modal verbs ("must" versus "should"); you communicate findings to stakeholders who will act on your precise wording. Verbal reasoning tests sample exactly this precision - and for experts, they carry a particular sting: the better you know the subject, the stronger the temptation to answer from knowledge rather than from the text. The test rewards the discipline of reading what is actually written.

### What it measures for your role

- **Data ethics and privacy**: extracting obligations, permissions and prohibitions from policy documents; spotting the difference between what a policy requires and what it merely encourages; constructively challenging proposed policies means first reading them exactly.
- **Applied maths, statistics and scientific practices**: distinguishing correlation language from causal language in analytical reports; identifying what a stated result does and does not support.
- **Delivering business impact**: reading stakeholder correspondence accurately - what was actually promised, requested, or conceded - and communicating compelling stories without overstating the evidence.
- **Understanding product delivery**: parsing delivery documentation, requirement statements, and definitions of done; the difference between "the MVP includes" and "the MVP may later include".
- **Developing data science capability**: reading CPD frameworks, standards, and job specifications precisely when building and assessing your team.
- **Programming and build (data science)**: specification reading - the skill of noticing that the requirements say "records that fail validation must be logged" but never say what happens to them next.

### Practice questions

For each passage, answer the statements strictly from the text. Resist your own expertise - if the passage does not say it, you cannot conclude it.

#### Passage A - Draft data ethics policy (Questions 1-4)

*"All new data science projects involving personal data must complete an ethics self-assessment before any data is accessed. Projects classified as high risk following the self-assessment must additionally be reviewed by the Data Ethics Committee, which meets monthly. The Committee may require modifications, impose conditions, or in exceptional cases recommend that a project does not proceed. Projects using only fully anonymised data are exempt from the self-assessment requirement, although teams are encouraged to complete one as good practice. The Committee's recommendations are advisory; accountability for proceeding rests with the Senior Responsible Owner."*

#### Question 1 (easy)

True, False, or Cannot Say: "A project using only fully anonymised data is required to complete an ethics self-assessment."

**Correct answer: False.**

**Explanation:** The passage states such projects "are exempt from the self-assessment requirement". Encouragement as good practice is not a requirement - the passage explicitly separates the two ("although teams are encouraged"). The statement claims a requirement, and the passage directly contradicts it. Note the precision demanded: if the statement had said "is expected to complete", the answer would arguably be Cannot Say, since "encouraged" and "expected" are not equivalent. Policy language earns its living in exactly these distinctions, which is why your skill of assessing and challenging proposed data ethics policies begins with reading them at this resolution.

#### Question 2 (easy)

True, False, or Cannot Say: "The Data Ethics Committee can prevent a high-risk project from proceeding."

**Correct answer: False.**

**Explanation:** The passage says the Committee "may... in exceptional cases recommend that a project does not proceed" and, decisively, that "the Committee's recommendations are advisory; accountability for proceeding rests with the Senior Responsible Owner." A body whose recommendations are advisory cannot itself prevent anything - the power to stop the project rests with the SRO. The statement attributes a power the passage explicitly withholds, so it is False rather than Cannot Say. Candidates who skim often mark this True because "recommend that a project does not proceed" pattern-matches to "can block". The governance distinction - who advises versus who decides - is one you navigate constantly when working with ethics stakeholders, and the passage draws it in a single semicolon.

#### Question 3 (moderate)

True, False, or Cannot Say: "A high-risk project could be delayed by up to a month waiting for Committee review."

**Correct answer: Cannot Say.**

**Explanation:** Tempting to mark True: the Committee "meets monthly", so a project that just missed a meeting might plausibly wait almost a month. But the passage says nothing about the review process's interaction with project timelines - whether reviews can happen between meetings, whether papers are considered out of committee, whether projects may proceed provisionally while awaiting review, or how scheduling works. "Meets monthly" makes the delay *plausible*; it does not make it *stated*. The inference requires assumptions the text does not supply, which is the precise definition of Cannot Say. This is the hardest discipline in verbal reasoning for senior professionals: your operational experience screams "of course it gets delayed - I have lived this", and the test asks you to silence that voice and report only what the passage supports.

#### Question 4 (moderate)

Multiple choice: According to the passage, which sequence correctly describes the obligations of a new project using personal data that is subsequently classified as high risk?

- A) Committee review, then self-assessment, then data access
- B) Self-assessment before data access; Committee review additionally required after the high-risk classification
- C) Self-assessment and Committee review may both happen after data access, provided the SRO approves
- D) The SRO may waive the self-assessment for urgent projects

**Correct answer: B.**

**Explanation:** The passage fixes two anchors: the self-assessment must complete "before any data is accessed", and high-risk classification follows the self-assessment ("classified as high risk following the self-assessment"), triggering the additional Committee review. Option A reverses the order - classification cannot precede the assessment that produces it. Option C contradicts "before any data is accessed". Option D invents a waiver power that appears nowhere in the text; the SRO's stated role is accountability for proceeding, not exemption-granting. Sequencing questions reward building a small mental timeline from the passage's temporal markers ("before", "following", "additionally") - exactly how you would trace obligations when challenging a proposed policy's workability.

#### Passage B - Delivery board minutes (Questions 5-8)

*"The Board noted that the forecasting product's private beta had met its primary success criterion - forecast accuracy within the agreed tolerance for three consecutive months - but that user adoption among operational managers remained below expectation, with 14 of 40 target users active in the final month of the beta. The user research lead attributed low adoption primarily to the product's requirement for manual data uploads, which several managers described as burdensome. The Board agreed that the public beta would not commence until the automated ingestion feature was delivered. The product manager estimated this feature would take one sprint; the principal data scientist advised that this estimate did not account for the data-sharing agreement required with the upstream system owner, which had historically taken between six weeks and four months to negotiate. The Board asked for a revised plan by the next meeting."*

#### Question 5 (easy)

True, False, or Cannot Say: "The private beta failed its primary success criterion."

**Correct answer: False.**

**Explanation:** The passage states the beta "had met its primary success criterion", directly contradicting the statement. Do not be misled by the adjacent negative material about adoption: adoption was "below expectation", but the passage does not designate adoption as the primary success criterion - accuracy is ("forecast accuracy within the agreed tolerance"). Verbal tests often place a true negative fact beside the claim being tested, inviting you to blend them. Reading at the clause level - which fact attaches to which subject - is the antidote, and it is the same skill you use when a delivery report interleaves good and bad news to soften the bad.

#### Question 6 (moderate)

True, False, or Cannot Say: "Fewer than half of the target users were active in the final month of the private beta."

**Correct answer: True.**

**Explanation:** The passage gives 14 of 40 target users active. Half of 40 is 20; 14 is fewer than 20, so fewer than half - the statement is a direct arithmetic restatement of the text, and verbal tests do expect this much numeracy. The care point: the statement must match the passage's own qualifiers - it concerns "target users", "active", "final month", all of which align with the text. If the statement had said "fewer than half of operational managers used the product during the beta", the answer would be Cannot Say: we know activity for the final month and for target users only; the wider population and period are not covered. Qualifier-matching of this kind is the mechanical core of True/False/Cannot Say questions.

#### Question 7 (moderate)

True, False, or Cannot Say: "The automated ingestion feature will take longer than one sprint to deliver."

**Correct answer: Cannot Say.**

**Explanation:** The passage records a disagreement: the product manager estimated one sprint; the principal data scientist advised that the estimate omitted the data-sharing agreement, which "had historically taken between six weeks and four months". Historical negotiation timescales make the one-sprint estimate *doubtful*, but the passage does not state what will happen - perhaps the agreement is negotiated in parallel with development, perhaps an existing agreement covers the ingestion, perhaps this negotiation bucks history. A recorded challenge to an estimate is not a recorded fact about the outcome. Marking this True is the expert's error: you have seen this movie and know how it ends, but the passage has not shown you the ending. Cannot Say. (Notice, incidentally, that the principal data scientist in the passage is modelling your own duty: communicate effectively and challenge delivery plans - the minute records the challenge, which is exactly what a well-run board should capture.)

#### Question 8 (moderate)

Multiple choice: Which statement best captures the Board's decision?

- A) The public beta is cancelled pending a review of user adoption
- B) The public beta will proceed once forecast accuracy is re-validated
- C) The public beta is conditional on delivery of automated ingestion, and a revised plan is due at the next meeting
- D) The public beta will proceed after one sprint

**Correct answer: C.**

**Explanation:** Two decisions are recorded: "the public beta would not commence until the automated ingestion feature was delivered" (a condition, not a cancellation - eliminating A) and "the Board asked for a revised plan by the next meeting". Option B invents a re-validation requirement; accuracy was met and no re-test is mentioned. Option D converts a contested estimate into a Board decision - the Board conditioned the beta on the *feature*, not on the *timeline*, and the one-sprint figure was immediately challenged in the same minute. Option C alone reflects both recorded decisions without addition or distortion. Summarising governance decisions faithfully - neither harder nor softer than minuted - is a skill you exercise every time you report a board's outcome to your team.

#### Passage C - Analytical report extract (Questions 9-11)

*"Analysis of 18 months of service data found that applications submitted with supporting documents attached at first submission were resolved 40% faster on average than those without. The association held after adjusting for application type and region. The analysis could not adjust for applicant circumstances, which the team notes may influence both the likelihood of attaching documents and the complexity of the case. The report recommends piloting a redesigned submission form that prompts for documents, with resolution time as the primary outcome measure, before any claim about the effect of the prompt is made. Machine learning feature analysis identified document presence as the strongest single predictor of resolution time in the current model."*

#### Question 9 (moderate)

True, False, or Cannot Say: "Attaching documents at first submission causes applications to be resolved faster."

**Correct answer: Cannot Say.**

**Explanation:** The passage reports an *association* ("were resolved 40% faster on average"), explicitly notes an unadjusted confounder ("could not adjust for applicant circumstances, which... may influence both"), and recommends a pilot "before any claim about the effect... is made". The text is scrupulously non-causal - it neither asserts the causal claim (so not True) nor denies it (so not False; the causal effect may well exist, which is why a pilot is proposed). This is the single most role-relevant verbal question in this document: as the critic of statistical analyses, the associated-versus-causal distinction is your daily bread, and the passage models exactly the careful language you should require of your own team's reports. If the statement had read "the analysis demonstrates an association between document attachment and faster resolution", the answer would be True.

#### Question 10 (moderate)

True, False, or Cannot Say: "The analysis adjusted for application type."

**Correct answer: True.**

**Explanation:** Directly stated: "The association held after adjusting for application type and region." The statement is a subset of the passage's claim, and subsetting is legitimate - the passage asserting "A and B" supports the statement "A". Contrast with Question 9: there the statement *exceeded* the text (adding causality); here it *stays within* it. Learning to feel the difference between a statement that stays inside the passage's claim and one that steps beyond it is the core calibration for True/False/Cannot Say formats, and it maps directly onto the discipline of not overstating findings when you present analysis to stakeholders.

#### Question 11 (hard)

Multiple choice: The report's recommendation of a pilot with resolution time as the primary outcome measure most directly reflects which analytical concern?

- A) The sample of 18 months was too small for statistical significance
- B) The observed association may be confounded by applicant circumstances, so an intervention study is needed before claiming the prompt has an effect
- C) The machine learning model was overfitted to document presence
- D) Regional variation invalidated the original analysis

**Correct answer: B.**

**Explanation:** Trace the report's own logic: association found → confounder acknowledged ("could not adjust for applicant circumstances") → therefore pilot before causal claims. The pilot is the standard remedy for confounding: intervene (redesign the form), measure the outcome, and let the design rather than statistical adjustment carry the causal weight. Option A invents a sample-size concern the passage never raises. Option C misreads the feature-analysis sentence - a strong predictor is not evidence of overfitting, and the passage draws no such link. Option D contradicts the text: region was adjusted for and the association held. The question rewards reconstructing an argument's internal structure - premise, limitation, remedy - which is precisely what you do when critiquing an analysis or challenging a policy: find what the author is worried about, and check whether their proposed remedy actually addresses it.

#### Passage D - Stakeholder email (Questions 12-14)

*"Thanks for the demonstration yesterday. The dashboard is impressive, and my team can see real potential for the weekly planning meeting. Before we commit, though, I need to be candid about two concerns. First, my analysts tell me the underlying model was trained on data that predates the service redesign in April; if that is right, I would want to understand the implications before we rely on the numbers. Second, our directorate cannot take on new tools that require training of more than half a day per user this quarter - our capacity is fully committed. If your team can address the first point in writing and confirm the training requirement, I am happy to put this to our management board in November. To be clear, this is not a commitment to adopt."*

#### Question 12 (easy)

True, False, or Cannot Say: "The stakeholder has committed to adopting the dashboard if both concerns are addressed."

**Correct answer: False.**

**Explanation:** The final sentence is explicit: "this is not a commitment to adopt." Even the conditional on offer is limited - if the concerns are addressed, the stakeholder is "happy to put this to our management board", i.e. to sponsor consideration, not to adopt. The statement claims a conditional commitment to adoption; the passage explicitly disclaims one. Misreading sponsorship as commitment is one of the costliest verbal errors in real delivery work - it becomes "the directorate is on board" in your planning documents, and unwinds months later. When you communicate stakeholder positions onward, this passage is the level of precision required.

#### Question 13 (moderate)

True, False, or Cannot Say: "The model was trained on data that predates the April service redesign."

**Correct answer: Cannot Say.**

**Explanation:** The email reports a second-hand claim, hedged twice: "my analysts tell me" and "if that is right". The stakeholder is not asserting the fact - they are asking you to confirm or refute it. The passage therefore contains a *reported claim*, not an *established fact*, and reported claims support neither True nor False about the underlying reality. This distinction - between what a document asserts and what it merely reports someone as saying - is essential in minutes, emails and news coverage alike, and verbal tests probe it constantly. In real life, of course, your next action would be to check the training-data provenance; if the analysts are right, a model trained on pre-redesign data may be systematically wrong about the redesigned service, which is a substantive drift concern, not a pedantic one.

#### Question 14 (moderate)

Multiple choice: What must happen, per the email, before the stakeholder will take the proposal to their management board?

- A) The training requirement must be reduced to under half a day
- B) The model must be retrained on post-April data
- C) The first concern must be addressed in writing, and the training requirement confirmed
- D) A second demonstration must be given to the analysts

**Correct answer: C.**

**Explanation:** The email's operative sentence: "If your team can address the first point in writing and confirm the training requirement, I am happy to put this to our management board in November." Two conditions: written response on the training-data question, and confirmation of the training requirement. Option A overshoots - the stakeholder needs the requirement *confirmed* as no more than half a day, but the email asks for confirmation, not reduction; if training already fits within half a day, nothing must change. Option B overshoots further: the stakeholder asks for an explanation of implications, not retraining. Option D invents a condition. Extracting exact conditions from stakeholder correspondence - no more, no less - is how you avoid both under-delivering (missing a stated condition) and over-committing your team (treating a question as a demand).

#### Question 15 (hard) - Cross-passage synthesis

Considering Passage B (board minutes) and Passage D (stakeholder email) together as documents from the same programme: True, False, or Cannot Say - "The stakeholder in Passage D is one of the 40 target users referred to in Passage B."

**Correct answer: Cannot Say.**

**Explanation:** Nothing in either passage links them. Passage B counts "target users" of a forecasting product's private beta among "operational managers"; Passage D's author manages a directorate considering a dashboard for "the weekly planning meeting". The products may be the same or different; the stakeholder may or may not be a target user; neither text identifies the other's cast. Plausibility ("it sounds like the same programme - the question even says so") is not textual support: even granting the same programme, the passages never place this individual among the 40. Synthesis questions test whether you demand an actual textual bridge before connecting documents - the same discipline that prevents you conflating two similarly named datasets, two versions of a policy, or two stakeholders with similar roles when assembling an evidence base across many documents.

### Preparation tips

- **Answer from the passage, ruthlessly.** Your expertise is the hazard here. Before marking True, find the supporting words; before marking False, find the contradicting words; if you can find neither, the answer is Cannot Say no matter what your experience insists.
- **Underline modal verbs and hedges.** Must, may, should, could, encouraged, recommended, "analysts tell me", "if that is right" - these small words carry the meaning in policies and correspondence, and nearly every hard question turns on one.
- **Watch for subset versus overreach.** A statement that claims *less* than the passage (Question 10) can be True; a statement that claims *more* (Question 9) cannot. Calibrate that boundary with practice.
- **Track who asserts what.** A minute recording a challenge, an email reporting a claim, a report noting a limitation - the document's assertion is not the same as the quoted person's assertion. Attribute before you classify.
- **Practise on your own inbox.** Take a real policy draft or board minute and write three statements about it: one True, one False, one Cannot Say. Designing the Cannot Say item teaches the distinction faster than answering does - and doubles as a coaching exercise for your team.
- **Manage reading time.** Skim the passage for structure (who, what obligations, what decisions), read the statement, then return to the relevant clause and read it exactly. Do not memorise the passage; interrogate it.

### Common pitfalls

- **Importing outside knowledge.** The expert's failure mode: you know how data-sharing negotiations go, how ethics committees behave, how adoption curves look - and none of it is admissible. Only the text counts.
- **Confusing likely with stated.** "The passage makes it plausible" earns Cannot Say, not True. Confusing a likely outcome with an asserted fact is the most common error in this format.
- **Blending adjacent facts.** Passages deliberately place true negative material next to the tested claim (Question 5). Attach each fact to its own subject.
- **Treating advisory as binding.** "Recommends", "encourages", "advises" create no obligation; "must" and "will" do. Marking encouraged behaviour as required (Question 1) is a classic error - in tests and in compliance work.
- **Missing explicit disclaimers.** When a text says "to be clear, this is not a commitment", believe it - however warm the surrounding language (Question 12).
- **Poor time allocation.** Reading every passage exhaustively before seeing the statements wastes the budget; most questions need one clause read precisely, not the whole text memorised.


## Workplace job-specific situational judgement assessment

### About this assessment

A workplace job-specific situational judgement assessment presents realistic dilemmas from your role and asks you to evaluate possible responses. Unlike the cognitive, numeric and verbal tests, there is no formula to apply: several options usually look reasonable, and the assessment measures whether your instincts align with the values and behaviours the organisation needs at your level - for the UK public sector, that means user needs first, transparency, collaboration, accessibility and inclusion, evidence-based decisions, and proportionate escalation.

Typical format: a short scenario followed by four or five possible actions. You either pick the **most effective** and **least effective** actions, or rank/rate all options. Timing is generous or absent - the test measures judgement, not speed. There is rarely a perfect option; the skill is recognising which imperfect action best serves users, the team, and the organisation, and which actively harms them.

Why it matters for your role: at principal level, judgement *is* the job. You lead and develop data scientists, arbitrate between delivery pressure and analytical rigour, own ethical calls that have no clean answer, challenge plans without breaking relationships, and represent data science to sceptical or over-enthusiastic stakeholders. A situational judgement test is the closest a psychometric instrument comes to sampling the actual texture of your week.

### What it measures for your role

- **Data science innovation** and leadership: coaching rather than rescuing, inspiring curiosity, challenging the status quo constructively, and creating opportunities for your team rather than hoarding the interesting work.
- **Data ethics and privacy**: identifying and addressing ethical and privacy concerns with stakeholders, communicating how ethical issues fit the wider organisational context, and constructively challenging proposed policies.
- **Delivering business impact**: balancing user needs, organisational objectives and technical purity; communicating compelling, honest stories about analysis; managing what happens when the evidence disappoints the sponsor.
- **Understanding product delivery**: MVP discipline, prioritisation calls, and working with multidisciplinary specialists when delivery and data science pull in different directions.
- **Developing data science capability**: handling underperformance, growth, credit, and CPD in the team you manage; building capability across the wider organisation.
- **Applied maths, statistics and scientific practices** and **Programming and build**: the professional-integrity dimensions - what you do when rigour, standards, or open-source principles collide with expedience.

### Practice questions

For each scenario, decide your answer before reading the analysis. The "most/least effective" designations reflect UK public sector values and principal-level expectations; if you disagree, articulating *why* is itself excellent preparation.

#### Question 1 (moderate) - The minister's deadline versus the unvalidated model

A policy team asks you to provide model-based estimates for a ministerial briefing due tomorrow morning. Your team's model produces the estimates, but the validation work you scheduled has not yet run - you have no current evidence on accuracy for this quarter, and the service context has changed since the last validation.

- Option A: Provide the estimates as requested, since the deadline is ministerial and validation can follow.
- Option B: Refuse to provide any figures until validation completes next week.
- Option C: Provide the estimates with a clear, prominent statement of the validation status and uncertainty, offer a range rather than a point estimate, and brief the policy lead directly on how the figures may safely be used.
- Option D: Provide the estimates informally by phone so nothing unvalidated appears in writing.
- Option E: Escalate to your director and ask them to decide whether the figures go forward.

**Most effective: C. Least effective: D.**

**Explanation:** Option C serves the real user need - the minister needs *decision-support*, not perfection - while preserving transparency and analytical honesty: caveats, ranges, and a direct conversation about safe use. This is "use model outputs to produce evidence" done properly under pressure. Option A is the classic pressure failure: unqualified figures acquire false authority the moment they enter a briefing, and retracting them later costs far more than caveating them now. Option B is rigid: refusing entirely fails the organisation when a caveated answer exists, and reads as the analyst who does not understand government tempo. Option E is not wrong but is weak as a first move at your level - you are the principal; providing the judgement (with your director informed) is the job, and escalating a decision you are equipped to frame simply relocates it without the analytical context you hold. Option D is the least effective by a distance: it evades accountability rather than exercising it, strips the caveats out of the record, and creates a figure that will be quoted with no provenance - the opposite of transparency. If the phone-only instinct ever feels attractive, treat it as a signal that the honest version of the message needs writing down.

#### Question 2 (moderate) - The enthusiastic senior stakeholder and the unsuitable technique

A director-general returns from a conference determined that your team should use a large generative model to draft responses to citizen correspondence. Your assessment is that the risk profile (hallucinated commitments, accessibility of tone, personal data in prompts) makes it unsuitable for direct citizen-facing use, though drafting *internal* summaries could work well.

- Option A: Implement what was asked; the DG outranks you and enthusiasm from the top is rare and valuable.
- Option B: Explain the risks in writing, decline to proceed, and copy the ethics board.
- Option C: Meet the DG, acknowledge the opportunity genuinely, present the risk assessment for the citizen-facing use, and propose the internal-summarisation pilot as the fastest safe route to demonstrable value.
- Option D: Quietly deprioritise the request and let it fade.
- Option E: Ask the DG's office to write a formal requirement so responsibility is documented before your team touches it.

**Most effective: C. Least effective: D.**

**Explanation:** Option C is stakeholder leadership: it honours the legitimate impulse (there *is* value in the technology), replaces a risky use case with a safe adjacent one, and keeps momentum - "challenge the status quo" cuts both ways, and a principal who can only say no is as limited as one who can only say yes. It also models "confidently talk about the benefits of data science approaches" while exercising the ethics skill of identifying and addressing concerns with stakeholders. Option A abdicates your professional duty - seniority does not transfer risk ownership, and you are the person in the room equipped to see the failure modes. Option B is procedurally defensible but relationally clumsy: leading with a written refusal and an ethics-board copy escalates before engaging, and squanders the rare asset of senior enthusiasm. Option E converts a leadership moment into bureaucracy - documentation matters, but as the *output* of engagement, not a substitute for it. Option D is least effective: passive resistance is a transparency failure, teaches your team that inconvenient requests are managed by neglect, and when the DG notices - they will - the trust cost lands on data science as a profession, not just on you.

#### Question 3 (hard) - The fairness finding a week before go-live

One week before a high-profile go-live, a junior data scientist on your team shows you evidence that the model's error rate is materially higher for applicants over 65 - a group not included in the fairness checks specified at design time. The programme board has announced the launch date publicly. The junior is visibly anxious about having found the problem so late.

- Option A: Thank the junior privately but hold the finding until after go-live, then fix it in the first patch release.
- Option B: Praise the finding openly, take it to the programme board immediately with a quantified impact assessment and options (delay, mitigate with manual review for the affected group, launch excluding the affected cohort from automated processing), and let the board make the risk decision with full information.
- Option C: Ask the junior to re-run the analysis three more ways to be certain before troubling the board.
- Option D: Fix the model quietly this week and go live on schedule without informing the board of the issue.
- Option E: Inform the board that launch must be delayed and instruct your team to begin remediation.

**Most effective: B. Least effective: A (with D a close second-worst).**

**Explanation:** Option B does four things a principal must do at once: protects the user group at risk (inclusion is not optional in public services), respects governance (the *board* owns the launch-risk decision, and it can only own it with full information), brings options rather than problems (quantified impact plus mitigation routes - the mark of senior advice), and publicly reinforces the behaviour you want from your team - the junior who found this should feel like a hero, not a problem, because psychological safety is what makes the *next* late finding surface at all. Option E gets the ethics right but the governance wrong: unilaterally declaring delay usurps the board's decision and squanders the mitigation options; boards accept hard news far better with choices attached. Option C, in moderation, is due diligence - but as posed ("three more ways before troubling the board") it is delay dressed as rigour, and a week is short; verify proportionately and fast, in parallel with alerting. Option D is a governance breach with a comforting surface: even if the quiet fix works, the board has certified a system whose risk profile it never saw, and if the fix fails you have compounded harm with concealment. Option A is worst: it knowingly launches a system that disadvantages older applicants - a protected characteristic - and converts your team's transparency into suppression. "Fix it in a patch" means real people receive worse decisions in the interim, with your signature on the silence. On age discrimination alone this is a legal exposure; on values it is disqualifying.

#### Question 4 (moderate) - The struggling senior and the team's delivery

A senior data scientist you manage - previously excellent - has missed two sprint commitments; their code review turnaround has become the team's bottleneck, and two juniors have privately mentioned waiting days for feedback. You suspect, but do not know, that something outside work is involved.

- Option A: Redistribute their code review duties to other seniors without discussion, to unblock the team quickly.
- Option B: Raise the missed commitments at the team retrospective so the whole team can problem-solve openly.
- Option C: Have a private, supportive one-to-one: describe the observed changes factually, ask open questions, listen, and agree a short-term plan (which may include temporarily rebalancing duties) with a review date.
- Option D: Begin documenting a formal performance-management case now, since the pattern is established across two sprints.
- Option E: Pair them with a junior to lighten the load and signal trust.

**Most effective: C. Least effective: B.**

**Explanation:** Option C is textbook people leadership: facts before interpretations, privacy for a personal matter, support before sanction, and a concrete plan with a review point so the team's needs are also met. It reflects "act as a coach" and the duty of care that comes with managing and developing teams. Option A treats the symptom while humiliating the person - discovering your duties reassigned without conversation tells a struggling colleague they are a problem to route around; the redistribution may well be *part* of the plan, but agreed, not imposed. Option D escalates to formal process before a single conversation, which is both procedurally premature and destructive of trust for someone with a strong record and a probable personal cause. Option E is well-meant misdirection: it neither addresses the cause nor reliably lightens senior-level load, and can add the burden of mentoring to someone already struggling. Option B is least effective: surfacing an individual's performance dip in a group retrospective makes a private difficulty public, breaches the trust of the two juniors who confided in you, and teaches everyone that struggling is punished with exposure - the exact opposite of the psychologically safe team your capability-building duty requires. Retrospectives examine the *system*; one-to-ones examine the *person*.

#### Question 5 (moderate) - The open-source request

Another government department asks whether they can reuse your team's entity-matching pipeline. Your coding standards say code should be open-sourced where appropriate. The pipeline works well, but the repository contains hard-coded internal server paths, sparse documentation, and one configuration file that references (though does not contain) a sensitive dataset's schema.

- Option A: Share the repository privately with the other department as-is, since they are also government.
- Option B: Decline: the code is not ready and your team has no capacity this quarter.
- Option C: Agree in principle, scope a short remediation (strip internal references, review the schema exposure with information assurance, write a minimal README), share with the requesting department first, and put open-sourcing properly on the team's backlog with a named owner.
- Option D: Open-source it immediately on the public repository to comply with the standard, and fix issues as external users raise them.
- Option E: Suggest the other department rebuild it themselves using your team's approach as inspiration, to avoid dependency risk.

**Most effective: C. Least effective: D.**

**Explanation:** Option C honours the open-source principle ("seek to make code open source where appropriate") while exercising the judgement the word "appropriate" demands: internal paths and a sensitive schema reference need review before any exposure, and information assurance owns part of that call. It also converts a one-off request into durable value - a backlog item with an owner - which is how principals turn favours into capability. Option A ignores that "government-to-government" does not neutralise the security review; internal server paths and schema references deserve the same scrutiny regardless of the recipient's lanyard. Option B wastes a cross-government collaboration opportunity that your role explicitly exists to cultivate, and "no capacity" is rarely true for a scoped, few-day remediation with this much return. Option E is the most expensive option dressed as prudence: duplicating a working pipeline across departments is precisely the waste that code sharing exists to eliminate. Option D is least effective: publishing known-unreviewed material containing internal infrastructure details and a sensitive schema reference converts a compliance instinct into a security incident. Open-source-by-default never means open-source-before-review; the standard says "where appropriate", and establishing appropriateness is your job, not the public's.

#### Question 6 (hard) - The analysis that contradicts the sponsor's policy

Your team completes a robust evaluation showing that a flagship intervention - publicly championed by your directorate's sponsor - has no measurable effect on its primary outcome. The sponsor's office asks you to "contextualise" the finding by leading the report with the positive secondary outcomes and moving the null primary result to an annex.

- Option A: Comply: emphasis is presentation, not falsification, and secondary outcomes are genuinely positive.
- Option B: Publish the report as drafted without discussing it further with the sponsor's office.
- Option C: Keep the null primary result prominent and honestly framed, present secondary outcomes fairly alongside it, and offer the sponsor's office a briefing on how to communicate the full picture - including what the evaluation does and does not show and what could be tested next.
- Option D: Ask the analyst who led the work to decide, since it is their analysis.
- Option E: Delay publication until after the sponsor's next public appearance to avoid embarrassment.

**Most effective: C. Least effective: A (with E close behind).**

**Explanation:** Option C holds the analytical line - the primary outcome was pre-specified precisely so that it could not be demoted when inconvenient - while treating the sponsor as a partner who needs help telling a difficult story, not an adversary to defy. Offering the "what next" framing (what could be tested, what the secondary outcomes justify) is what turns an unwelcome null into a constructive policy conversation; this is "communicate relevant and compelling stories effectively" in its hardest and most important case, where the compelling story must also be the true one. Option B gets the integrity right and the relationship wrong: publishing around your sponsor rather than through a conversation forfeits the chance to prepare them, and burns capital that honest analysis will need again next time. Option D outsources an organisational-pressure problem to the person least equipped to absorb it - shielding your team from exactly this pressure is what your seniority is for. Option E makes analytical timing serve political convenience, an arrangement that never survives disclosure. Option A is least effective despite its reasonable surface: relegating a pre-specified primary outcome to an annex *because it is null* is not presentation, it is spin - readers of the summary will conclude the intervention works, which is the falsehood the structure was designed to make impossible. The test of any "contextualisation" request: would you be comfortable explaining the re-ordering to a select committee? If not, decline it - kindly, with an alternative in hand.

#### Question 7 (moderate) - The multidisciplinary collision

Your data scientists and the service's delivery manager are in conflict. The delivery manager wants to descope model explainability features from the MVP to hit the release date; your scientists insist explainability is essential because caseworkers must justify decisions to applicants. The product manager asks for your view at tomorrow's planning session.

- Option A: Back your data scientists fully: explainability is non-negotiable and delivery pressure is not a reason to cut it.
- Option B: Back the delivery manager: MVP discipline means shipping the smallest thing and explainability can follow in the next release.
- Option C: Reframe the question around the user need: caseworkers must justify decisions to applicants from day one, so establish the *minimum* explainability that satisfies that need (e.g. top contributing factors in plain language, not a full explanation suite), propose that for the MVP, and defer the rest.
- Option D: Suggest the product manager decide, since prioritisation is their accountability.
- Option E: Propose delaying the release until the full explainability feature set is ready.

**Most effective: C. Least effective: B.**

**Explanation:** Option C does what a principal uniquely can: dissolve a false binary with domain knowledge. The genuine user need is not "explainability features" (a solution) but "caseworkers can justify decisions to applicants" (a need) - and needs can usually be met minimally. Proposing top-factors-in-plain-language as MVP explainability honours both MVP discipline ("define the minimum viable product and support decisions about priorities") and the user requirement, showing an understanding of user research's role in arbitrating exactly these disputes. Option A wins the battle and damages the multidisciplinary relationship - "non-negotiable" is a stance, not an argument, and it teaches delivery colleagues that data science is inflexible. Option E is Option A with a schedule cost added. Option D is half-right - the product manager does own prioritisation - but abdicates your input at the moment your expertise is the missing ingredient; being *asked* for a view and returning the question is not humility, it is absence. Option B is least effective because it descopes the wrong thing: an automated decision that caseworkers cannot explain to applicants fails transparency obligations from the first case processed - some capabilities are load-bearing for lawful, fair operation and do not defer. Knowing *which* capabilities those are is precisely the judgement your role adds to MVP conversations.

#### Question 8 (hard) - The privacy concern in someone else's product

In a cross-government working group, a peer team proudly demonstrates a prototype that links several datasets to profile service users. You notice the linkage almost certainly exceeds the purposes for which one dataset was collected, and no data protection assessment is mentioned. It is not your product, not your department, and the room is enthusiastic.

- Option A: Say nothing: it is another department's risk, and their data protection officer will presumably catch it.
- Option B: Publicly challenge the legality of the prototype in front of the working group.
- Option C: Raise a constructive question in the session ("what did your data protection assessment conclude about purpose compatibility for dataset X?"), then follow up privately with the team lead, offering your team's experience of navigating the same issue.
- Option D: Report the team to the Information Commissioner's Office.
- Option E: Email the working group chair afterwards suggesting data protection be a standing agenda item.

**Most effective: C. Least effective: A (with D as the most disproportionate).**

**Explanation:** Option C is proportionate professional courage. The in-session question is framed as curiosity, not accusation - it gives the team the chance to reveal an assessment you have not seen (you may be wrong), while ensuring the issue is on the record before enthusiasm hardens into commitment. The private follow-up converts challenge into collaboration - "our team hit the same purpose-limitation question; here is how we approached it" - which is how cross-government capability actually builds, and exactly what "work with stakeholders to identify and address ethical and privacy concerns" looks like beyond your own walls. Option B may be justified if the response to C is dismissive, but as an opening move it humiliates a peer team publicly on an inference you have not verified. Option D skips every internal step: regulators exist for unaddressed risk, not for first resort against colleagues who have not yet been asked a single question. Option E is a reasonable *supplement* but feeble as the whole response - a process suggestion that lets the specific prototype sail on. Option A is least effective: at principal level, data ethics leadership does not stop at your organisational chart's edge. You are among the few people in that room equipped to see the problem; silence is a choice, and "someone will presumably catch it" is how citizen-affecting failures ship. The working group *is* the mechanism for cross-government professional standards - use it.

#### Question 9 (hard) - The retraction decision

Three weeks after your team's analysis informed a published policy decision, a data engineer discovers that an upstream extract had silently dropped records with missing postcodes - about 8% of cases, skewed towards urban areas. Your team re-runs the analysis: the headline conclusion still holds directionally, but a supporting figure quoted publicly (a regional comparison) is materially wrong.

- Option A: Since the headline conclusion holds, log the issue internally and correct the figure at the next scheduled publication.
- Option B: Immediately notify the policy team and your head of profession, issue a correction to the published figure with a plain-language explanation, add the extract check to your reusable data-quality pipeline, and review which other analyses consumed the same feed.
- Option C: Notify the policy team but advise against public correction, as the conclusion is unchanged and a correction would invite disproportionate criticism.
- Option D: Publicly correct the figure but attribute the error to the upstream data provider's extract process.
- Option E: Quietly replace the figure in the online version of the publication without an errata note.

**Most effective: B. Least effective: E.**

**Explanation:** Option B is the complete professional response, in the right order: the decision-owners hear first (they must judge whether the wrong figure changes anything downstream), the public record is corrected transparently, the *system* is fixed so the class of error cannot recur (this is exactly why your data engineering skill emphasises reusable checks), and the blast radius is mapped - the same silent drop may sit under other work. Option A misjudges what "materially wrong" means for a published figure: corrections delayed for convenience become concealment the moment anyone else spots the error, and urban-skewed missingness is the kind of detail that a journalist or committee *will* spot. Option C makes reputational comfort the arbiter of the public record - and the criticism from a discovered-uncorrected error is always worse than from a self-declared one. Option D corrects the figure but poisons the well: publicly blaming the upstream provider shreds the collaborative relationship your data products depend on, and the accountability for validating inputs to *your* analysis was yours - the silent drop is their bug, but the unchecked consumption is your gap, which is why Option B fixes your pipeline rather than pointing fingers. Option E is least effective: a stealth edit of a public document is the one action here that converts an honest error into a trust catastrophe, because it demonstrates intent to conceal. Analytical organisations survive being wrong; they do not survive being caught hiding it.

#### Question 10 (hard) - The coaching moment in a crisis

During a live incident - the overnight scoring pipeline has failed and caseworkers have no prioritisation lists this morning - your mid-level scientist on support duty proposes a fix you can see is wrong (rerunning with a manual override that would silently score yesterday's cases twice). You could take over and fix it yourself in twenty minutes. Operations are calling every few minutes.

- Option A: Take over, fix it, and walk through what you did at the next team meeting.
- Option B: Tell them their fix is wrong and instruct them step-by-step through the correct one.
- Option C: Ask one sharp question that exposes the flaw ("what happens to yesterday's cases under that override?"), let them find the correct fix with you present, and handle the operations calls yourself while they work.
- Option D: Let them apply their fix and learn from the consequences, staying close to help clean up.
- Option E: Convene a quick call with the whole team to decide the fix collectively.

**Most effective: C. Least effective: D.**

**Explanation:** Option C threads the needle the scenario is built on: the flaw gets caught (users are protected), the scientist does the thinking (capability grows precisely when stakes are real), and you absorb the stakeholder pressure so they can work - which is what senior air cover *is*. The sharp question is the coaching move: it transfers the diagnostic pattern ("always ask what a rerun does to already-processed cases"), not just today's answer. This is "act as a coach, inspiring curiosity" exercised under the conditions where it counts most. Option A is sometimes right - there are incidents where twenty minutes matters that much - but as a default it buys twenty minutes today at the price of the same phone call every future incident, because nobody else ever becomes the person who can fix it. Option B protects the outcome but does the thinking for them; instruction produces followers of steps, questions produce owners of problems. Option E misapplies collaborative ritual to an emergency with a known-diagnosable fault - a whole-team call adds latency, not insight, when one person plus one coach suffice. Option D is least effective and the scenario says why: the flawed fix *silently double-scores real cases* - caseworkers would work mis-prioritised lists and citizens would feel the consequences. "Learning from consequences" is a legitimate technique for consequences a team can safely own; it is never legitimate when the consequences land on users. The line between growth-by-failure and negligence is exactly there, and knowing where it sits is principal-level judgement.

### Preparation tips

- **Anchor on users, then transparency, then relationships.** When options conflict, UK public sector values order themselves reliably: protect the people the service affects, keep the record honest, and preserve working relationships in that priority order. Most "most effective" answers fall out of that hierarchy.
- **Look for the option that adds information before adding action.** Strong principal-level responses quantify, verify proportionately, or ask one sharp question first - without letting verification become delay (Question 3's trap in both directions).
- **Distinguish owning a decision from hoarding it.** Governance bodies own launch risk; product managers own prioritisation; sponsors own their communications. The best options usually *inform those owners fully* rather than deciding for them - but never use "not my decision" to withhold your expertise.
- **Rehearse the trust question.** For any tempting option, ask: how does this read when discovered? Stealth edits, phone-only figures, quiet deprioritisation and delayed corrections all fail that test instantly.
- **Practise with your own past dilemmas.** Write up three hard calls from your career as SJT items with four options each. Designing the "plausible but wrong" options teaches you the format's grammar - and makes excellent coaching material for your team.
- **Answer as the role, not as the hero.** The test wants the judgement of a principal data scientist operating within an organisation - escalating proportionately, coaching rather than rescuing - not the lone expert who fixes everything personally.

### Common pitfalls

- **Choosing the idealistic option over the effective one.** "Refuse until validation completes" and "delay launch until perfect" read as principled but fail the organisation; the strong options deliver honesty *and* usefulness simultaneously.
- **Selecting passive options.** Waiting for someone else to notice, letting requests fade, deferring decisions that are yours - assessments consistently punish delay-and-deflect patterns, and Questions 2 and 8 both contain one.
- **Over-escalation as a reflex.** Escalating can look safe, but at principal level the test expects you to *be* the escalation point for most matters, going upward with options and analysis, not with unprocessed problems.
- **Under-weighting the people dimension.** Options that solve the technical or delivery problem while humiliating a colleague (public retrospectives, silent reassignment, blame-shifting corrections) are reliably rated poorly - relationships are infrastructure in multidisciplinary work.
- **Ignoring who legitimately owns the decision.** Both usurping governance (unilateral delay) and abdicating expertise ("you decide") lose marks; the pattern that scores is full information plus clear recommendation to the accountable owner.
- **Forgetting the coaching lens.** In any scenario involving your team, ask whether the option grows capability or merely consumes yours. The role is leader of data science; the assessment scores you as one.


## Conclusion

You have now worked through the four assessment types most relevant to your role: cognitive reasoning with the artefacts of data science leadership, numeric reasoning across the budgets, metrics and capacity figures you handle weekly, verbal reasoning over the policies, minutes and correspondence you read and write, and situational judgement across the genuine dilemmas of leading data science in the public sector - ethics under deadline pressure, coaching in a crisis, honesty when the evidence disappoints, and stewardship of the public record.

A few themes will have surfaced repeatedly, because they are the connective tissue of your role. Verify before you trust - recalculate the metric, reconcile the pipeline, re-read the clause. Answer the question actually asked - what follows logically, what the passage states, what the accountable owner needs. Protect users first, then the record, then the relationships - and notice how rarely those genuinely conflict once the options are laid out honestly. And in every people scenario, grow capability rather than merely consuming your own.

If some questions felt uncomfortable, treat that precisely as a development signal rather than a verdict. A wobble on weighted averages is an afternoon's practice; hesitation over the fairness-finding scenario is a prompt to rehearse your escalation routes before you need them. Consider revisiting the sections a few weeks apart, and use the scenarios with your own team - they make ready-made coaching conversations, and articulating why an option is weaker is a deeper test than choosing the stronger one.

Assessments, in the end, sample what you already do. The preparation that counts is the daily practice of your craft: critiquing analyses kindly and precisely, keeping your reading exact, making your numbers honest, and exercising judgement you would be content to explain in public. Keep linking your learning to your objectives as your CPD habit already demands, keep coaching curiosity into the people around you, and walk into any assessment - or any Monday morning - knowing that the capabilities being measured are ones you strengthen every working day. Good luck: you are better prepared than you think.
