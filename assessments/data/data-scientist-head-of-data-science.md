# Data Scientist (Head of Data Science) - Psychometric Assessment Resources

## Introduction

Welcome. This document is a practical, encouraging companion for you as Head of Data Science — a leader with complete oversight of data science within your organisation. Whether you are preparing for an internal assessment, a promotion board, a cross-government move, or simply want to sharpen the mental skills your role demands, these resources are designed specifically for you and the work you do every day.

Psychometric assessments are structured, standardised exercises that measure how you think, reason, and decide. They are widely used across the UK Civil Service and the wider public sector because they are fair, evidence-based, and predictive of on-the-job performance. For a role at your level, they are less about testing whether you can do arithmetic or read a paragraph, and more about testing whether you can extract the signal from noisy information quickly, critique an analysis under time pressure, weigh competing priorities, and exercise sound judgement in situations where ministers, senior leaders, multidisciplinary teams, and the public all have a stake in the outcome.

This document covers four assessment types, each in its own section:

1. **Workplace job-specific cognitive assessment** — pattern recognition, logical deduction, error checking, prioritisation, and problem solving using the artefacts you genuinely handle: model outputs, pipelines, dashboards, capability plans, and ethics frameworks.
2. **Workplace job-specific numeric reasoning assessment** — budgets, capacity figures, model performance metrics, resourcing ratios, and the kind of tables that land on your desk before a spending review.
3. **Workplace job-specific verbal reasoning assessment** — dense passages drawn from data ethics policies, ministerial briefings, standards documents, and cross-government reports, followed by True / False / Cannot Say and comprehension questions.
4. **Workplace job-specific situational judgement assessment** — realistic leadership dilemmas involving your real stakeholders: ministers, senior leaders, data engineers, user researchers, delivery managers, and your own data science team.

Each section explains what the assessment measures, maps it to the specific skills in your role profile — from applied maths, statistics and scientific practices, through data ethics and privacy, to delivering business impact and developing data science capability — and then gives you a substantial set of practice questions with full worked explanations. Each section closes with preparation tips and common pitfalls tailored to your level.

How to use this document: work through it actively. Attempt each question before reading the answer. Time yourself where suggested. Treat the explanations as coaching, not just answer keys — they model the reasoning an assessor is looking for. And use the situational judgement scenarios for self-reflection: they are as valuable for thinking about how you lead as they are for assessment preparation.

You bring deep expertise to this role. These resources are here to help you demonstrate it with confidence. Let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive ability assessment measures the exact mental processes your role demands, using realistic workplace material rather than abstract puzzles. Unlike a generic IQ test, every item is built from artefacts a Head of Data Science genuinely handles: model evaluation tables, pipeline diagrams, ethics review findings, capability matrices, delivery plans, and dashboards. The assessment predicts how well you extract meaning from complex information, spot errors and inconsistencies, deduce what must follow from a set of facts, and prioritise under pressure.

Typical format: 15 to 30 minutes, delivered online, usually 20 to 30 questions. Some platforms are adaptive, raising the difficulty as you answer correctly, so do not be alarmed if the questions feel progressively harder — that usually means you are doing well. Scoring is objective and compared against a norm group of senior professionals, and modern platforms report speed and accuracy separately rather than as a single number. Most tests offer short ungraded practice items first so you can get comfortable with the interface; always take them.

Why it matters at your level: as Head of Data Science you set direction, oversee outputs and products, critique statistical analyses, and represent your department on data science matters. When a flawed model evaluation reaches you the day before a ministerial briefing, your ability to spot the logical hole in minutes — not hours — is precisely what this assessment simulates. Cognitive assessments at senior level are less about raw processing speed and more about disciplined reasoning: distinguishing what the evidence shows from what people claim it shows.

### What it measures for your role

Mapped to the skills in your role profile:

- **Applied maths, statistics and scientific practices** — logical deduction and error checking exercises mirror your duty to critique statistical analyses and to use model outputs to produce evidence for services and policies. Items test whether you can spot an invalid inference, a leaked variable, or a misapplied technique.
- **Data science innovation** — pattern recognition items reflect your practical knowledge of data science tools and techniques and your duty to identify opportunities where data science can improve data practices: seeing the structure in messy information is the core cognitive act of innovation.
- **Data ethics and privacy** — error checking and deduction items frequently embed compliance conditions, mirroring your oversight of ethics standards and legislation across the organisation. Can you deduce which project breaches the framework, given a set of rules and facts?
- **Data engineering and Understanding product delivery** — sequencing and prioritisation items reflect working with data engineers to design products, choosing between Agile and waterfall, defining an MVP, and supporting decisions about priorities across a portfolio.
- **Developing data science capability and Delivering business impact** — resource-allocation logic items simulate overseeing resourcing, budgeting, and building capability: given constraints, which allocation is feasible, and what must be true for the plan to work?

### Practice questions

**Question 1 (easy) — Pattern recognition in model performance**

Your team reports the weekly accuracy of a deployed classification model used to triage citizen correspondence:

Week 1: 94.2% — Week 2: 94.0% — Week 3: 93.5% — Week 4: 92.7% — Week 5: 91.6% — Week 6: ?

Which value best continues the pattern, and what does the pattern most likely indicate?

- A) 91.4% — random noise around a stable mean
- B) 90.2% — accelerating decline consistent with data drift
- C) 93.8% — seasonal recovery
- D) 91.6% — the model has stabilised at a new baseline

**Correct answer: B**

**Explanation:** Look at the successive drops: 0.2, 0.5, 0.8, 1.1 percentage points. The decline is not merely steady; the gap increases by 0.3 each week — an accelerating pattern. The next drop should be about 1.4 points, giving 91.6 − 1.4 = 90.2%. An accelerating decline in a production model is the classic signature of data drift: the live data distribution is moving progressively further from the training distribution. As Head of Data Science, recognising this pattern quickly matters because it dictates the intervention — retraining and drift monitoring — and because you are responsible for establishing maintenance support for scalable products, not just launching them.

**Question 2 (easy) — Logical deduction from an ethics framework**

Your organisation's data ethics framework contains these rules:

1. Any project using special category personal data must complete a Data Protection Impact Assessment (DPIA) before development begins.
2. Any project using machine learning to make or support decisions about individuals must be reviewed by the Ethics Board.
3. Projects that complete a DPIA are automatically logged in the transparency register.

Project Kestrel uses machine learning on special category personal data to support benefit-fraud triage decisions about individuals. Development began last month. The transparency register contains no entry for Kestrel.

Which conclusion must be true?

- A) The Ethics Board has not reviewed Project Kestrel.
- B) Project Kestrel has breached rule 1.
- C) Project Kestrel does not use personal data.
- D) The Ethics Board review is overdue but the DPIA was completed.

**Correct answer: B**

**Explanation:** Work through the chain. Kestrel uses special category data, so rule 1 requires a DPIA before development began. Rule 3 says every completed DPIA is automatically logged in the register. There is no register entry, so no DPIA was completed — yet development has begun. Therefore rule 1 has been breached; B must be true. A is tempting but not forced: the register tells us nothing about Ethics Board reviews, which are governed by rule 2 and are not stated to be logged anywhere. C contradicts the given facts. D asserts the DPIA was completed, which the register evidence refutes. This is exactly the disciplined "what must be true, not what might be true" reasoning you apply when overseeing compliance with ethics standards across the organisation.

**Question 3 (moderate) — Error checking a model evaluation write-up**

A junior data scientist sends you this summary for sign-off before it goes into a briefing for senior leaders:

"We trained a gradient boosting model to predict which of 40,000 planning applications will be appealed. The dataset contained 2,000 appealed cases (5%). We achieved 95% accuracy on the held-out test set, demonstrating the model is highly effective. We also included the appeal outcome date as a feature, which proved highly predictive. Precision on the appealed class was 22%."

Which is the most serious flaw you should flag first?

- A) The 95% accuracy claim, because a model predicting "no appeal" for everyone would also score 95%
- B) The use of gradient boosting rather than a neural network
- C) The inclusion of the appeal outcome date as a feature, which leaks the target
- D) The precision figure, which should never be reported for imbalanced data

**Correct answer: C**

**Explanation:** Two genuine flaws are present, and the question tests whether you can rank their severity. A is a real problem: with 5% prevalence, 95% accuracy is exactly what the trivial "always predict no appeal" model achieves, so the accuracy claim is uninformative. But C is fatal rather than misleading: the appeal outcome date can only exist for cases that were appealed, so including it leaks the target into the features. The model has effectively been told the answer, meaning every reported metric — including the accuracy — is invalid and the model will collapse in production where that field is empty at prediction time. B is a preference, not a flaw. D is wrong: precision is especially important for imbalanced data, and the low 22% figure is honest evidence the model is weak. Critiquing statistical analyses is a named element of your applied maths and statistics skill, and target leakage is the single most common fatal error you will catch when reviewing your teams' work.

**Question 4 (moderate) — Prioritisation across a portfolio**

Monday morning. Four items compete for your attention:

- A) The Ethics Board flags that a live recidivism-risk model may be producing disparate outcomes by ethnicity; the model continues to run.
- B) A minister's office requests talking points on your department's AI adoption for a speech on Thursday.
- C) Your data engineering lead reports the overnight pipeline failed, delaying the monthly performance dashboard by 24 hours.
- D) A promising candidate for your vacant lead data scientist post has a competing offer expiring Friday.

Which order of attention is most defensible?

- A) B, D, A, C
- B) A, B, D, C
- C) A, D, B, C
- D) C, A, B, D

**Correct answer: C**

**Explanation:** Item A is the clear first priority: a live model potentially causing discriminatory outcomes is an ongoing ethical and legal harm, and you lead on ethics — every hour it runs unexamined compounds the risk. The interesting discrimination in this question is the ordering of B and D. The ministerial deadline is Thursday; the candidate's offer expires Friday — but securing scarce senior talent is a build-capability responsibility where a short call today can prevent an irreversible loss, and drafting talking points can begin in parallel via delegation with your review later in the week. Both B, D and D, B orderings are defensible, but C is the option that puts the ethics incident first and the routine, already-mitigated pipeline delay (a 24-hour slip with a known cause and an owner) last. Option D fails by elevating an operational blip above an active ethical harm. At your level, prioritisation questions reward triaging by irreversibility and harm, not by who is shouting loudest.

**Question 5 (moderate) — Deductive reasoning about team capability**

You are planning capability development. The following statements are all true:

1. Every data scientist in your directorate who has completed the NLP specialism can be deployed to the correspondence-triage product.
2. No one who joined within the last six months has completed the NLP specialism.
3. Some data scientists on the forecasting team have completed the NLP specialism.
4. Priya joined within the last six months.

Which conclusion must be true?

- A) Priya cannot ever be deployed to the correspondence-triage product.
- B) Some members of the forecasting team can be deployed to the correspondence-triage product.
- C) Priya works on the forecasting team.
- D) Everyone on the forecasting team can be deployed to the correspondence-triage product.

**Correct answer: B**

**Explanation:** From statement 3, some forecasting-team members have completed the NLP specialism; from statement 1, everyone who has completed it can be deployed to the triage product. Therefore some forecasting-team members can be deployed — B follows necessarily. A overreaches: statements 2 and 4 tell us Priya has not completed the specialism *yet*, but nothing says she never can, and statement 1 only gives a sufficient condition for deployment, not a necessary one — there may be other routes in. C has no support. D generalises "some" to "all". The trap at senior level is A: it sounds like prudent workforce logic, but it confuses "not currently qualified via this route" with "permanently excluded". Precise reading of sufficient versus necessary conditions is the same skill you use when critiquing eligibility logic in policy models.

**Question 6 (moderate) — Sequencing a product delivery**

Your team must deliver a new prescriptive analytics product for hospital discharge planning. The steps and their dependencies:

- Step 1: Agree user needs with the service team (no dependency)
- Step 2: Data sharing agreement signed (no dependency)
- Step 3: DPIA and ethics review (requires Step 2)
- Step 4: Build feature pipeline (requires Steps 2 and 3)
- Step 5: Train and validate model (requires Step 4)
- Step 6: Define MVP dashboard with users (requires Step 1)
- Step 7: Private beta with one hospital trust (requires Steps 5 and 6)

Steps 1 and 2 can run in parallel. Which statement about the critical path is correct?

- A) The critical path runs through Steps 1 and 6, because user needs drive everything.
- B) The critical path runs through Steps 2, 3, 4, 5, 7 — delays to the ethics review delay the beta.
- C) Steps 3 and 6 can be swapped to shorten delivery.
- D) The private beta can begin once Step 5 completes, regardless of Step 6.

**Correct answer: B**

**Explanation:** Trace the dependency chains to the beta. Chain one: 2 → 3 → 4 → 5 → 7 (five sequential stages). Chain two: 1 → 6 → 7 (three stages). Assuming broadly comparable durations, the longer chain — through the data sharing agreement, ethics review, pipeline, and model — is the critical path, so any delay to Step 3 delays the beta directly. A mistakes importance for criticality: user needs are vital, but that chain has slack. C is impossible: Steps 3 and 6 sit on different chains with different dependencies. D contradicts the stated dependency that Step 7 requires Step 6. Note the governance insight embedded here, which assessors at your level like to test: ethics review sits on the critical path, so as the leader who oversees both delivery and ethics you should resource the ethics review early rather than treat it as a late-stage gate. This mirrors your product delivery skill — supporting decisions about priorities and MVP definition — and your duty to ensure ethics is applied when implementing programmes.

**Question 7 (moderate) — Spotting the inconsistency in a dashboard**

A performance dashboard prepared for your monthly directorate review shows:

- Total models in production: 24
- Models with drift monitoring enabled: 19
- Models without drift monitoring: 3
- Models added this quarter: 4 (all with drift monitoring, included in the totals above)
- Models retired this quarter: 2 (removed from the totals above)

What should you challenge first?

- A) 19 + 3 = 22, not 24 — two production models are unaccounted for in the monitoring breakdown.
- B) Retired models should still appear in the totals.
- C) Four new models in a quarter is implausibly fast.
- D) Drift monitoring should be 100% before any dashboard is published.

**Correct answer: A**

**Explanation:** The monitored and unmonitored categories must partition the 24 production models, but 19 + 3 = 22. Two models are missing from the breakdown — perhaps their monitoring status is unknown, which is itself a governance concern. B is wrong: retired models are correctly excluded from a "in production" count. C is a judgement you cannot make from this data. D may be a worthy policy ambition but is not an internal inconsistency in the dashboard. Error checking of exactly this kind — do the categories sum, do the definitions partition — is a fast, high-value habit when you oversee outputs and products and must sign off figures before they travel upwards to senior leaders, where an inconsistency discovered later is far more costly.

**Question 8 (moderate) — Pattern recognition in recruitment data**

Your last five recruitment campaigns for data scientists produced these outcomes (applications → interviews → offers → acceptances):

- Campaign 1: 120 → 18 → 6 → 5
- Campaign 2: 95 → 14 → 5 → 4
- Campaign 3: 110 → 16 → 6 → 5
- Campaign 4: 130 → 20 → 7 → 3
- Campaign 5: 125 → 19 → 7 → 3

What is the most important pattern change for you, as the leader building capability, to investigate?

- A) Application volumes are falling.
- B) The interview-to-offer ratio has collapsed.
- C) Offer acceptance has dropped from roughly 80% to roughly 43% in the two most recent campaigns.
- D) There is no meaningful change; the numbers vary randomly.

**Correct answer: C**

**Explanation:** Compute the acceptance rates: Campaigns 1–3 run at 5/6, 4/5, 5/6 — about 80–83%. Campaigns 4–5 run at 3/7 and 3/7 — about 43%. Applications (A) are stable or rising; interview-to-offer ratios (B) are steady at roughly one offer per three interviews throughout. The step change is at the acceptance stage: candidates are receiving your offers and declining them. That points to a competitiveness problem — pay, competing offers, employer proposition — arising recently. For a Head of Data Science who oversees resourcing and builds capability, spotting *where in the funnel* the pattern broke is the difference between commissioning a useless advertising push and fixing the actual leak. The cognitive skill tested is identifying which stage of a multi-stage process changed, rather than reacting to the aggregate.

**Question 9 (hard) — Logical deduction across delivery methodologies**

Your portfolio office applies these rules when assigning delivery methods:

1. Products with fixed statutory deadlines are delivered by waterfall or hybrid, never pure Agile.
2. Products with evolving user needs must include iterative user research cycles.
3. Any product using hybrid delivery requires a trained delivery manager.
4. The correspondence-triage product has evolving user needs and a fixed statutory deadline.
5. No trained delivery manager is currently available.

Which conclusion must be true?

- A) The correspondence-triage product must be delivered by waterfall, and it must include iterative user research cycles.
- B) The correspondence-triage product cannot be delivered at all.
- C) The correspondence-triage product should use pure Agile because user needs are evolving.
- D) The statutory deadline must be renegotiated.

**Correct answer: A**

**Explanation:** From rule 4 and rule 1, the product must use waterfall or hybrid. From rule 3 and fact 5, hybrid is unavailable (it requires a trained delivery manager, and none exists). So waterfall is the only permitted method. Rule 2 independently requires iterative user research cycles because user needs are evolving — and note that nothing in the rules says waterfall delivery cannot contain user research cycles; the rules constrain the delivery method and the research activity separately. So A must be true. B overreaches — a valid configuration exists. C violates rule 1. D is a possible management response, not a logical necessity. This item rewards exactly the skill your role profile names: understanding the differences between delivery methods such as Agile and waterfall and choosing the most appropriate method — while resisting the intuitive but unsupported leap that "evolving needs" logically forces Agile.

**Question 10 (hard) — Problem solving under resource constraints**

You have three teams and four candidate projects for the next quarter. Each team can take exactly one project; one project will be deferred.

- Team Alpha: strong in NLP, no forecasting experience.
- Team Beta: strong in forecasting, moderate NLP.
- Team Gamma: strong in computer vision and forecasting.

Projects: P1 — ministerial correspondence NLP triage (requires strong NLP); P2 — A&E demand forecasting (requires strong forecasting); P3 — satellite imagery land-use classification (requires computer vision); P4 — long-term workforce forecasting (requires at least moderate forecasting).

Which assignment is feasible, and which project must be deferred?

- A) Alpha→P1, Beta→P2, Gamma→P3; defer P4
- B) Alpha→P1, Beta→P4, Gamma→P2; defer P3
- C) Alpha→P3, Beta→P2, Gamma→P1; defer P4
- D) Alpha→P1, Beta→P3, Gamma→P4; defer P2

**Correct answer: A**

**Explanation:** P3 requires computer vision, which only Gamma has — so Gamma must take P3 if P3 is to run at all. P1 requires strong NLP, which only Alpha has — Alpha must take P1. That leaves Beta for either P2 (strong forecasting required — Beta qualifies) or P4 (moderate forecasting — Beta also qualifies). Since only one project remains for Beta, one of P2/P4 is deferred. Option A satisfies every constraint: Alpha→P1 (strong NLP ✓), Beta→P2 (strong forecasting ✓), Gamma→P3 (computer vision ✓), defer P4. Check the others: B assigns Gamma to P2 and defers P3, feasible on skills but it defers the only project Gamma is uniquely required for while leaving Gamma on work Beta could not cover — still logically valid? No: B gives Beta→P4 and Gamma→P2, which is feasible, but then P3 is deferred even though the option set asks which assignment *is feasible*; B is feasible too, so discriminate further: the question asks which is feasible *and* correctly identifies the forced deferral. Only in A are all three uniquely-constrained matches (Alpha–P1, Gamma–P3) preserved; B needlessly abandons P3, which only Gamma can ever do, making the portfolio strictly worse under identical constraints. C fails immediately: Alpha lacks computer vision and Gamma is not stated to have strong NLP. D fails: Beta lacks computer vision. Constraint-satisfaction reasoning like this underpins your oversight of resourcing — start with the most constrained pairing, not the most attractive one.

**Question 11 (hard) — Error checking a causal claim**

An analysis unit sends you this conclusion for a policy evaluation: "Local authorities that adopted our predictive maintenance model spent 18% less on emergency housing repairs than those that did not. The model therefore reduces repair costs by 18%."

Which single challenge most undermines the causal claim?

- A) The percentage should be calculated on medians, not means.
- B) Adoption was voluntary, so authorities with better data maturity and lower baseline costs may have self-selected into adoption.
- C) 18% is too small an effect to matter.
- D) Emergency repairs are seasonal, so the comparison should use winter data only.

**Correct answer: B**

**Explanation:** The claim leaps from an observed difference between adopters and non-adopters to a causal effect of the model. The strongest challenge is selection bias: adoption was voluntary, and the kinds of authorities that adopt a predictive model early — data-mature, well-resourced, proactive — plausibly already had lower repair costs. The observed 18% gap could exist entirely without the model doing anything. A and D are methodological quibbles that adjust the estimate rather than invalidate the inference. C confuses effect size with validity. When you use model outputs to produce evidence and help design services and policies, distinguishing correlation from causation in evaluations is arguably the highest-stakes critique you perform: a spurious 18% saving, repeated in a business case, can misdirect millions of pounds of public money. The follow-up you would commission — matched comparisons, difference-in-differences, or a stepped-wedge rollout — flows directly from naming the right flaw.

**Question 12 (hard) — Multi-step deduction on data sharing**

Four datasets are candidates for a cross-government linkage project. The rules:

1. Any dataset containing personal data may only be linked inside the secure research environment (SRE).
2. Dataset W contains personal data. Dataset X is fully synthetic. Dataset Y is aggregate statistics at local-authority level. Dataset Z's contents are undocumented.
3. Undocumented datasets must be treated as containing personal data until an audit proves otherwise.
4. The SRE can host at most three datasets for any one project.

The project team insists all four datasets are essential and no audit can be completed in time. What follows?

- A) The project can proceed outside the SRE if dataset W is pseudonymised.
- B) The project as specified cannot proceed: W and Z must be in the SRE, X and Y may join them, but all four together exceed the SRE limit only if all four must be co-located — so the team must either drop a dataset or link in two stages.
- C) Dataset Z can be excluded from the personal-data rule because it might not contain personal data.
- D) The SRE limit does not apply because the project is cross-government.

**Correct answer: B**

**Explanation:** Apply the rules mechanically. W has personal data → SRE only (rule 1). Z is undocumented and unaudited → treated as personal data (rule 3) → SRE only. X and Y carry no SRE requirement but linkage means all four must be brought together — and rule 4 caps the SRE at three datasets per project. Four essential datasets, all needing to be co-located in an environment capped at three: the specification is infeasible as stated, so the team must drop a dataset, complete the audit after all (removing Z's constraint), or restructure into staged linkages. A fails because pseudonymised data is still personal data under UK data protection law and, more decisively, nothing in the rules offers pseudonymisation as an exemption. C inverts rule 3's precautionary logic. D invents an exemption. The cognitive skill is refusing to soften a rule because the conclusion is inconvenient — central to overseeing compliance with data ethics standards and legislation across the organisation.

**Question 13 (hard) — Prioritisation with incomplete information**

At 16:40 on a Friday you learn that a dashboard your directorate publishes externally has, since Tuesday, shown a hospital waiting-time figure that is wrong by an unknown amount due to a join error. Journalists have quoted the figure. Your dashboard lead has gone home; the analyst who found the error is unsure whether the error inflates or deflates the figure. What do you do first?

- A) Wait until Monday to investigate properly with the full team.
- B) Immediately take the dashboard offline, then notify your senior leadership and press office that a correction is in progress, before establishing the error's size.
- C) Publish an immediate correction with your best guess of the true figure.
- D) Ask the analyst to quietly fix the join over the weekend and update the figure without an announcement.

**Correct answer: B**

**Explanation:** The reasoning hierarchy: stop ongoing harm, inform those accountable, then fix carefully. Taking the dashboard down halts the spread of a known-wrong published statistic — you do not need to know the error's direction to know the figure is wrong. Alerting leadership and the press office respects transparency and prepares them for media questions, which have already begun. A allows a wrong public figure to stand for three more days. C replaces one unverified number with another — publishing a guess repeats the original failure. D is the most dangerous option at your level: a silent fix to an externally quoted statistic, if discovered, converts an honest error into an apparent cover-up, damaging the trustworthiness you are responsible for as the department's representative on data science matters. This item tests reasoning under uncertainty: identifying which actions are robust to what you do not yet know.

### Preparation tips

- **Practise on your own artefacts.** Take a recent model evaluation, dashboard, or delivery plan from your directorate and interrogate it: do the numbers sum, do the inferences follow, what would have to be true for the conclusion to hold? Ten minutes a day of this converts your daily assurance work into assessment fluency.
- **Rehearse sufficient versus necessary conditions.** Senior-level deduction items turn on this distinction constantly ("completing the specialism allows deployment" does not mean "deployment requires the specialism"). Slow down on quantifiers: all, some, none, only.
- **Triage ruthlessly.** With 20 to 30 questions in as many minutes, a stuck question costs you two easy ones. Flag, skip, return.
- **Use the practice items.** The ungraded warm-up questions exist to remove interface anxiety. Treat them seriously.
- **Trust your professional instincts, then verify them.** Your experience will often point to the right answer (target leakage, selection bias, drift) — but confirm against the text of the question, because assessments reward the reasoning given, not general wisdom.

### Common pitfalls

- **Answering from experience instead of the given rules.** You know how ethics review works in your organisation; the question defines how it works in this scenario. Use only the stated rules — assessors deliberately vary them.
- **Choosing "what might be true" over "what must be true".** Plausible conclusions are the classic distractor for senior candidates who are used to weighing likelihoods. Deduction items demand certainty.
- **Anchoring on the first flaw you spot.** In error-checking items there are often two genuine flaws; the mark goes to identifying the more severe one, as in the target-leakage question above.
- **Over-reading pattern items.** A five-point trend supports a simple pattern (steady, accelerating, cyclical), not an elaborate theory. Fit the simplest pattern consistent with the data.
- **Time sink on constraint puzzles.** Start from the most constrained element (the team only one project fits, the dataset only one environment accepts) — never enumerate every combination.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment evaluates how you analyse, interpret, and make sound decisions from numerical data presented the way it actually arrives in your working life: budget tables, capacity plans, model performance metrics, recruitment funnels, and evaluation results. It is business mathematics, not abstract formulae — percentages, ratios, rates of change, weighted averages, and cost–benefit estimation, applied to realistic figures.

Typical format: strictly timed, often 60 to 90 seconds per question, with an onscreen calculator allowed or provided. The time pressure is deliberate: the assessment prioritises quick, accurate data extraction and interpretation over mental arithmetic heroics. Questions typically present a table or chart followed by two to four items drawing on it, and the totals, units, and scale qualifiers ("in thousands", "FTE", "per quarter") are where most marks are won and lost.

Why it matters at your level: you oversee resourcing, budgeting, and outputs across the data science function. You present figures to ministers and senior leaders who will act on them. You critique cost models in business cases, challenge optimistic capacity plans, and decide where a limited budget buys the most capability. A Head of Data Science who cannot rapidly sanity-check a table under pressure signs off other people's errors. This assessment simulates precisely those moments: extract the right numbers, combine them correctly, and notice when a figure cannot possibly be right.

### What it measures for your role

Mapped to the skills in your role profile:

- **Applied maths, statistics and scientific practices** — the core of the assessment: percentages, rates, weighted averages, and interpreting model metrics such as precision, recall, and error rates, mirroring your duty to critique statistical analyses and use a variety of data analytics techniques across the data life cycle.
- **Delivering business impact** — cost–benefit items reflect building the case for data science products: computing return on investment, break-even points, and benefit projections that support organisational objectives.
- **Developing data science capability** — workforce arithmetic: FTE calculations, training budget allocation, recruitment funnel rates, and pay-band planning, matching your responsibility for capability, CPD direction, and resourcing.
- **Understanding product delivery** — capacity and scheduling items: sprint throughput, MVP scope trade-offs, and delivery-plan arithmetic that supports decisions about priorities.
- **Data engineering** — infrastructure figures: compute costs, pipeline volumes, and storage growth, reflecting your collaboration with data engineers to design and provide products.
- **Data ethics and privacy** — items on fairness metrics and disparity ratios, because overseeing ethics compliance increasingly means being able to read a bias audit table.

### Practice questions

**Question 1 (easy) — Percentage change in a directorate budget**

Your data science directorate budget was £4.8 million this financial year. Next year it will be £5.4 million. What is the percentage increase?

- A) 8.9%
- B) 11.1%
- C) 12.5%
- D) 15.0%

**Correct answer: C**

**Explanation:** Increase = £5.4m − £4.8m = £0.6m. Percentage increase = 0.6 ÷ 4.8 = 0.125 = 12.5%. The classic error is dividing by the new figure: 0.6 ÷ 5.4 = 11.1%, which is option B, deliberately included. Always divide the change by the *original* value. You will do this calculation constantly when presenting budget movements to senior leaders, and assessors know the wrong-denominator error is the most common slip.

**Question 2 (easy) — Team capacity in FTE**

Your machine learning team has 8 data scientists. Two work 0.6 FTE, one works 0.8 FTE, and the rest are full time. Corporate overhead (training, governance, leave cover) absorbs 15% of all available capacity. How many FTE are effectively available for project delivery?

- A) 5.95
- B) 6.12
- C) 6.80
- D) 7.00

**Correct answer: A**

**Explanation:** Count the headcount first: 8 people, of whom 2 + 1 = 3 are part time, leaving 5 full time. Raw FTE = (2 × 0.6) + (1 × 0.8) + (5 × 1.0) = 1.2 + 0.8 + 5.0 = 7.0 FTE. Deliverable capacity = 7.0 × (1 − 0.15) = 7.0 × 0.85 = 5.95 FTE. Option B (6.12) is what you get if you miscount one part-timer as full time and apply the overhead to 7.2 FTE (7.2 × 0.85 = 6.12); option D forgets the overhead entirely. This mirrors real capacity planning, where a single miscounted FTE compounds through every downstream projection. When you oversee resourcing, always reconcile the headcount before applying percentages.

**Question 3 (easy) — Reading a model metrics table**

A fraud-detection model produces the following confusion matrix on 10,000 test cases:

| | Predicted fraud | Predicted not fraud |
|---|---|---|
| Actual fraud | 300 | 200 |
| Actual not fraud | 700 | 8,800 |

What is the model's precision on the fraud class?

- A) 30%
- B) 60%
- C) 70%
- D) 8%

**Correct answer: A**

**Explanation:** Precision = true positives ÷ all positive predictions = 300 ÷ (300 + 700) = 300 ÷ 1,000 = 30%. Option B (60%) is the recall — 300 ÷ (300 + 200) — the proportion of actual fraud the model catches, a different question. When your teams bring you evaluation results and when you communicate model performance to senior leaders, keeping precision ("when it flags fraud, how often is it right?") and recall ("of all the fraud, how much does it catch?") distinct is fundamental: a minister told "the model is 60% accurate at finding fraud" will make a very different decision from one told "70% of the model's fraud alerts are false alarms" — and both describe this same model.

**Question 4 (moderate) — Compute cost projection**

Your cloud compute bill for model training is £22,000 per month. The data engineering lead proposes moving training jobs to spot instances, saving 55% on the affected workloads, but only 60% of your workload (by cost) is suitable. Migration costs a one-off £18,000. What is the monthly saving, and in how many months does the migration pay for itself?

- A) £7,260 per month; 2.5 months
- B) £12,100 per month; 1.5 months
- C) £7,260 per month; 3 months
- D) £13,200 per month; 1.4 months

**Correct answer: A**

**Explanation:** Affected workload = 60% of £22,000 = £13,200 per month. Saving = 55% of £13,200 = £7,260 per month. Payback = £18,000 ÷ £7,260 = 2.48 months ≈ 2.5 months. Option D is the trap for those who stop a step early (£13,200 is the affected cost, not the saving); option B applies 55% to the whole bill. Multi-stage percentage problems like this are the bread and butter of the infrastructure business cases you approve when working with data engineers to design and provide products — and of spotting when a vendor's "55% saving" claim quietly applies to only part of the estate.

**Question 5 (moderate) — Weighted average across teams**

Three teams report model deployment lead times: Team A averages 32 days across 5 deployments; Team B averages 18 days across 15 deployments; Team C averages 45 days across 4 deployments. What is the directorate's overall average lead time per deployment?

- A) 31.7 days
- B) 25.4 days
- C) 24.4 days
- D) 28.0 days

**Correct answer: B**

**Explanation:** Weight by deployments, not by teams. Total days = (32 × 5) + (18 × 15) + (45 × 4) = 160 + 270 + 180 = 610. Total deployments = 5 + 15 + 4 = 24. Overall average = 610 ÷ 24 = 25.42 ≈ 25.4 days. Option A (31.7) is the unweighted mean of the three team averages, (32 + 18 + 45) ÷ 3 — the single most common weighted-average error, giving small teams outsized influence on the headline figure. When you report a directorate-level KPI upwards, the simple mean of team means would overstate the true lead time here by more than six days; assessors set this trap because leaders aggregate team metrics constantly, and Team B's fifteen fast deployments should dominate the average precisely because they represent most of the actual work.

**Question 6 (moderate) — Training budget allocation**

Your CPD budget is £96,000. You decide to allocate it across 24 data scientists in the ratio 3:2:1 for senior : mid : junior bands, with 6 seniors, 10 mids, and 8 juniors. How much does each mid-level data scientist receive?

- A) £4,000
- B) £3,000
- C) £4,174
- D) £2,087

**Correct answer: C**

**Explanation:** The ratio applies per person: each senior gets 3 units, each mid 2 units, each junior 1 unit. Total units = (6 × 3) + (10 × 2) + (8 × 1) = 18 + 20 + 8 = 46 units. One unit = £96,000 ÷ 46 = £2,086.96. Each mid receives 2 units = £4,173.91 ≈ £4,174. Option A is £96,000 ÷ 24, the equal split; option D is one unit, a senior would get £6,261 (3 units) and that sanity check — do the parts sum? 18 × £2,086.96 + 20 × £2,086.96 + 8 × £2,086.96 = 46 × £2,086.96 = £96,000 ✓ — takes five seconds and catches most slips. Setting the direction of CPD within your team is a named element of your capability skill; ratio allocations of exactly this shape appear whenever budgets meet banding.

**Question 7 (moderate) — Fairness metrics in a bias audit**

An ethics audit of a triage model reports selection rates (the proportion of each group the model flags for fast-track): Group 1: 12.0% of 5,000 cases; Group 2: 8.4% of 3,000 cases. Your ethics framework requires the ratio of the lower selection rate to the higher (the disparate impact ratio) to be at least 0.80. What is the ratio, and does the model comply?

- A) 0.70 — non-compliant
- B) 0.80 — compliant at the boundary
- C) 0.70 — compliant because more Group 1 cases exist
- D) 1.43 — compliant

**Correct answer: A**

**Explanation:** Ratio = 8.4% ÷ 12.0% = 0.70. The threshold is 0.80, so 0.70 breaches the framework: non-compliant. The group sizes (5,000 and 3,000) are a distractor — the disparate impact ratio compares *rates*, which already normalise for group size, so option C's reasoning is spurious. Option D inverts the ratio (12 ÷ 8.4); frameworks specify lower-over-higher precisely so the ratio cannot exceed 1. As the leader who oversees compliance with data ethics standards and develops the ethical framework in your area, you will read tables like this in every bias audit that reaches you: the arithmetic is easy, and the mark is for knowing which numbers matter and which are noise.

**Question 8 (moderate) — Recruitment funnel arithmetic**

You need 6 new data scientists in post by Q4. Historic funnel rates: 15% of applicants reach interview, 33% of interviewees receive offers, 75% of offers are accepted. Approximately how many applicants must the campaign attract?

- A) 120
- B) 162
- C) 54
- D) 96

**Correct answer: B**

**Explanation:** Work backwards. Acceptances needed: 6. Offers needed = 6 ÷ 0.75 = 8. Interviews needed = 8 ÷ 0.33 ≈ 24.2, call it 24. Applicants needed = 24 ÷ 0.15 = 160, and with the rounding on the offer stage (8 ÷ 0.33 = 24.24; 24.24 ÷ 0.15 = 161.6) ≈ 162. Equivalently in one step: 6 ÷ (0.75 × 0.33 × 0.15) = 6 ÷ 0.0371 ≈ 162. Option A comes from multiplying only two of the three rates; option C from 6 ÷ 0.15 × ... partial chains. Chained-rate reversals like this are exactly how you size recruitment campaigns when overseeing resourcing and building capability — and the same backward arithmetic sizes user-research recruitment and beta-testing cohorts.

**Question 9 (moderate) — Storage growth projection**

A data platform currently holds 40 TB and grows 20% per quarter. The current contract caps storage at 80 TB. After how many quarters will the platform exceed the cap?

- A) 3 quarters
- B) 4 quarters
- C) 5 quarters
- D) 8 quarters

**Correct answer: B**

**Explanation:** Compound the growth: Q1: 40 × 1.2 = 48 TB. Q2: 48 × 1.2 = 57.6 TB. Q3: 57.6 × 1.2 = 69.1 TB. Q4: 69.1 × 1.2 = 82.9 TB — the cap is exceeded during the fourth quarter. Option D (8 quarters) is the linear-growth error: treating 20% of the original 40 TB (8 TB per quarter) as the constant increment gives 80 TB after 5 quarters, and misreading further stretches it. Exponential-versus-linear confusion is one of the most consequential errors in infrastructure planning; when you support and enable future IT developments, catching a linear projection of an exponential process in a supplier's capacity plan can save a contract renegotiation done in a panic.

**Question 10 (hard) — Cost–benefit of a data science product**

A proposed prescriptive analytics product for clinic scheduling costs £350,000 to build and £90,000 per year to run. It is projected to save 4,200 staff hours per year at an average loaded cost of £38 per hour, plus reduce missed appointments by 3,000 per year at £45 per missed appointment. What is the net annual benefit once live, and the payback period on the build cost?

- A) £204,600 per year; 1.7 years
- B) £294,600 per year; 1.2 years
- C) £159,600 per year; 2.2 years
- D) £204,600 per year; 1.2 years

**Correct answer: A**

**Explanation:** Gross annual benefit = (4,200 × £38) + (3,000 × £45) = £159,600 + £135,000 = £294,600. Net annual benefit = £294,600 − £90,000 running costs = £204,600. Payback on the £350,000 build = £350,000 ÷ £204,600 = 1.71 ≈ 1.7 years. Option B forgets the running costs; option C counts only the staff-hours benefit; option D mixes the correct net benefit with the payback computed against the gross figure. The discipline — gross benefit, minus running costs, then payback on capital — is the skeleton of every data science business case you take responsibility for when delivering scalable products into the organisation, and the item rewards keeping the three stages separate under time pressure.

**Question 11 (hard) — Interpreting an A/B evaluation table**

Your team A/B tested a new NLP triage model against the current one on live correspondence:

| Metric | Current model | New model |
|---|---|---|
| Volume processed | 12,000 | 12,000 |
| Correctly routed | 10,320 | 10,920 |
| Escalated to humans | 1,800 | 960 |
| Complaints traced to misrouting | 84 | 102 |

Which statement is numerically correct and most decision-relevant?

- A) The new model improves routing accuracy from 86% to 91% but complaints per misrouted case have risen, so accuracy alone should not decide deployment.
- B) The new model is worse: complaints rose from 84 to 102.
- C) The new model is better on every measure.
- D) Escalations fell 47%, so the new model saves the most money and should be deployed immediately.

**Correct answer: A**

**Explanation:** Routing accuracy: current 10,320 ÷ 12,000 = 86%; new 10,920 ÷ 12,000 = 91%. So accuracy improved — B's headline is misleading without denominators, but note the complaints detail: current misroutes = 12,000 − 10,320 = 1,680, complaints per misroute = 84 ÷ 1,680 = 5%; new misroutes = 1,080, complaints per misroute = 102 ÷ 1,080 = 9.4%. The new model misroutes less often, but its misroutes generate complaints at nearly twice the rate — plausibly it fails on more serious correspondence. C is false (complaints rose in absolute terms and per misroute). D computes the escalation drop correctly (840 ÷ 1,800 = 46.7%) but "deploy immediately" ignores the complaint signal and the human-in-the-loop implications of halving escalations. A is both numerically right and managerially wise. This is the level of table-reading expected of someone who critiques statistical analyses and decides what evidence goes to senior leaders: compute the rates, not just the counts, and ask what the residual errors are made of.

**Question 12 (hard) — Budget reprofiling under a spending cut**

Your directorate budget of £5.4m is split: staff 65%, cloud infrastructure 20%, training 5%, external partnerships 10%. A 7% cut to the total is imposed, but staff costs are contractually fixed for the year. If the cut must fall proportionately across the non-staff lines, what percentage cut does each non-staff line take?

- A) 7%
- B) 20%
- C) 10.8%
- D) 15.3%

**Correct answer: B**

**Explanation:** The cut = 7% of £5.4m = £378,000. Non-staff budget = 35% of £5.4m = £1.89m. Cut as a share of non-staff spend = £378,000 ÷ £1,890,000 = 0.20 = 20%. Because staff costs (65%) are protected, a 7% total cut concentrates into a 20% cut on everything else — cloud drops £75,600 ÷ ... to check one line: cloud = £1.08m, 20% cut = £216,000; training = £270,000, cut £54,000; partnerships = £540,000, cut £108,000; total £216,000 + £54,000 + £108,000 = £378,000 ✓. Option A misses the protection; option C divides the cut by half the budget. This "protected-line concentration" effect is one of the most important pieces of arithmetic a budget-holding leader can internalise: modest headline cuts become severe cuts to the flexible spend that funds training and innovation — precisely the lines that build capability.

**Question 13 (hard) — Model retraining economics**

A demand-forecasting model loses accuracy over time: each month without retraining, forecast error increases operational costs by an additional £6,000 per month relative to a freshly trained model (month 1 after training costs £6,000 extra, month 2 £12,000 extra, and so on). Retraining costs £30,000 and resets the error to zero. If you retrain every n months, total cost per cycle is the retraining cost plus accumulated error costs. Which retraining interval minimises average monthly cost?

- A) Every 2 months
- B) Every 3 months
- C) Every 4 months
- D) Every 6 months

**Correct answer: B**

**Explanation:** Accumulated error cost over n months = £6,000 × (1 + 2 + … + n) = £6,000 × n(n+1)/2. Cycle cost = £30,000 + £3,000n(n+1). Average monthly cost = £30,000/n + £3,000(n+1). Test each: n=2: 15,000 + 9,000 = £24,000. n=3: 10,000 + 12,000 = £22,000. n=4: 7,500 + 15,000 = £22,500. n=6: 5,000 + 21,000 = £26,000. Minimum at n=3: retrain quarterly. The structure — a fixed cost amortised over the interval versus a linearly growing degradation cost — recurs across maintenance scheduling, and the optimum balances the two. As the leader responsible for establishing maintenance support for scalable data science products, this is the arithmetic behind a sensible retraining policy, and the assessment version simply asks you to evaluate a short formula at four points rather than derive calculus.

**Question 14 (hard) — Percentage points versus percentages in a ministerial briefing**

A draft briefing states: "The new matching algorithm raised the successful-match rate from 8% to 12%, a 4% improvement." As you review, which correction is required, and what is the correct relative improvement?

- A) No correction; 4% is right.
- B) The rise is 4 percentage points, which is a 50% relative improvement.
- C) The rise is 4 percentage points, which is a 33% relative improvement.
- D) The rise should be reported as 1.5%, the ratio of the two rates.

**Correct answer: B**

**Explanation:** From 8% to 12% is a rise of 4 *percentage points*. The relative improvement = 4 ÷ 8 = 50%. Option C divides by the new rate (4 ÷ 12 = 33%) — the wrong denominator again. Conflating points and percent is the single most common numerical error in briefings for ministers and senior leaders, and it cuts both ways: "a 4% improvement" undersells a 50% gain here, while elsewhere the same confusion can wildly oversell a trivial change. Communicating and presenting data science effectively to ministers is a named duty at your level; assessments reward candidates who both spot the error and quantify the correction.

**Question 15 (moderate) — Sprint throughput and MVP scope**

The MVP for a new analytics product comprises 84 story points. The multidisciplinary team completes an average of 14 points per two-week sprint, but the first sprint of any new product historically delivers only half the average. The service team needs the MVP live for a policy deadline in 14 weeks. Does the plan fit, and with how much slack?

- A) Yes — the MVP needs 6 sprints (12 weeks), leaving 2 weeks of slack.
- B) No — the MVP needs 7 sprints (14 weeks), leaving no slack.
- C) Yes — the MVP needs 6.5 sprints (13 weeks), leaving 1 week of slack.
- D) No — the MVP needs 8 sprints (16 weeks).

**Correct answer: B**

**Explanation:** Adjust for the slow first sprint: sprint 1 delivers 14 × 0.5 = 7 points. Remaining work = 84 − 7 = 77 points at 14 points per sprint = 5.5 sprints, which in practice means 6 further sprints (you cannot deploy half a sprint's output mid-sprint under this plan). Total = 7 sprints × 2 weeks = 14 weeks: the plan lands exactly on the deadline with zero slack. Option A ignores the first-sprint effect (84 ÷ 14 = 6 sprints); option C wrongly treats the fractional sprint as schedulable. The managerial reading matters more than the arithmetic: a plan with zero slack against a policy deadline is a plan that misses it, so as the leader who defines the MVP and supports decisions about priorities, this calculation is your cue to descope, add capacity, or reset expectations now — not in week 12. Assessors reward candidates who both compute correctly and notice what the number means.

### Preparation tips

- **Rehearse the five core moves.** Percentage change (change ÷ original), weighted average (weight by volume), chained rates (multiply through, divide to reverse), compound growth (multiply repeatedly, never add), and points-versus-percent. These five patterns cover most senior-level numeric items.
- **Read the table before the question.** Spend ten seconds absorbing units, scale qualifiers ("£000s", "FTE", "per quarter"), and row/column totals. Most wrong answers come from extracting the wrong number, not computing badly.
- **Estimate first, compute second.** Before touching the calculator, bracket the answer ("about a third of 13,000, so roughly 4,000"). If your computed answer falls outside the bracket, you have mis-set the calculation.
- **Use the calculator for arithmetic, your head for structure.** The assessment tests whether you set up the right calculation; the calculator only executes it.
- **Practise on your own management information.** Recompute one figure from your directorate's monthly pack each day — budget variance, capacity, a model metric. It is the most role-faithful revision available, and it doubles as quality assurance.

### Common pitfalls

- **Misreading scale qualifiers.** Confusing monthly with annual data, or missing "in thousands", transforms every subsequent step. This is the most common failure mode in timed numeric tests.
- **Wrong denominator.** Dividing the change by the new value instead of the original, or a rate by the wrong population — several distractors above are built purely on this.
- **Unweighted means of team-level averages.** Aggregating averages without weighting by volume flatters small teams and misleads the board.
- **Linear thinking about exponential processes.** Storage growth, compound cost increases, and error accumulation compound; adding a fixed increment each period understates them badly.
- **Time sink questions.** A multi-stage item you cannot structure within 20 seconds should be flagged and skipped; return with remaining time. One stubborn question can cost three easy marks.
- **Over-calculating.** Some items yield to estimation: if options are far apart, rounding to clean numbers answers the question in a third of the time.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment evaluates how accurately you understand, analyse, and draw conclusions from written material of the kind your role generates and consumes: data ethics policies, cross-government standards, ministerial correspondence, evaluation reports, supplier documentation, and internal governance papers. The dominant format presents a dense passage followed by statements you must classify as **True** (the passage says or logically entails it), **False** (the passage contradicts it), or **Cannot Say** (the passage provides insufficient information either way). Multiple-choice comprehension items — best summary, author's main point, precise meaning of a clause — round out the set.

Two rules define the discipline. First, answer strictly from the passage: your extensive professional knowledge of data science, ethics, and government must be set aside, because the test measures reading, not expertise — and passages are sometimes written to differ deliberately from real-world practice. Second, respect the exact wording: "must", "may", "some", "all", "unless", and "intends to" each carry precise logical weight, and most wrong answers come from reading what you expected rather than what is written.

Typically you will face 20 to 30 items with under a minute each. For a Head of Data Science the relevance is direct: you oversee compliance with legislation and standards where a "may" misread as a "must" changes your obligations; you communicate to ministers whose words are drafted and parsed with exactly this precision; and you critique reports whose conclusions must be checked against what their own text actually establishes.

### What it measures for your role

Mapped to the skills in your role profile:

- **Data ethics and privacy** — passages drawn from ethics frameworks, DPIA guidance, and legislation test whether you can extract precise obligations, exemptions, and conditions: the core reading act in overseeing compliance across the organisation and continuously improving an ethical framework.
- **Applied maths, statistics and scientific practices** — passages from evaluation reports and statistical guidance test whether you can distinguish what a study claims from what it demonstrates — the verbal counterpart of critiquing statistical analyses.
- **Delivering business impact and Understanding product delivery** — passages from business cases, delivery frameworks, and user research summaries test whether you can identify commitments, dependencies, and scope boundaries before you champion a product or approve an MVP.
- **Developing data science capability** — passages about professional standards and CPD frameworks mirror your responsibility for setting development direction and talking confidently about data science to customers.
- **Communication to senior leaders** — best-summary and inference items reflect your duty to communicate and present data science and data ethics effectively to ministers and senior leaders, where compressing a dense document into a faithful sentence is a daily act.

### Practice questions

**Passage A — Data ethics framework extract (for Questions 1–4)**

"All new data science projects must complete an ethics self-assessment before development begins. Projects assessed as high risk must additionally be referred to the Data Ethics Committee, which meets monthly and may request modifications, impose conditions, or, in exceptional cases, recommend that a project does not proceed. The Committee's recommendations are advisory; final authority rests with the Senior Information Risk Owner (SIRO). Projects using only aggregate data published under the Open Government Licence are exempt from the self-assessment requirement, unless the project combines two or more such datasets in ways that could plausibly re-identify individuals. Departments must publish an annual summary of Committee referrals, excluding any detail that would compromise operational security."

**Question 1 (easy)**

True, False, or Cannot Say: "The Data Ethics Committee can stop a high-risk project from proceeding."

**Correct answer: False**

**Explanation:** The passage states the Committee "may... recommend that a project does not proceed" and immediately adds that its "recommendations are advisory; final authority rests with the SIRO". A body whose recommendations are advisory cannot itself stop a project — the power to stop lies with the SIRO. The statement attributes decisive power to the Committee, which the passage contradicts, so the answer is False, not Cannot Say. Watch how one clause ("recommendations are advisory") reverses the impression created by the preceding list of strong-sounding powers. In your governance work, the distinction between advise and decide determines accountability — and assessments place it exactly where a fast reader will miss it.

**Question 2 (easy)**

True, False, or Cannot Say: "A project using a single aggregate dataset published under the Open Government Licence must complete an ethics self-assessment."

**Correct answer: False**

**Explanation:** The exemption clause states that projects "using only aggregate data published under the Open Government Licence are exempt from the self-assessment requirement", with the exemption withdrawn only where the project "combines two or more such datasets" in potentially re-identifying ways. A single dataset cannot trigger the two-or-more condition, so the exemption stands and the statement — which asserts the assessment *must* be completed — contradicts the passage. The mark here is for tracking an exemption and its exception: exactly the structure of real data protection guidance, where obligations are defined, exempted, and then re-imposed by conditions, and where you, overseeing compliance, must know which layer applies.

**Question 3 (moderate)**

True, False, or Cannot Say: "The Data Ethics Committee has recommended that at least one project should not proceed."

**Correct answer: Cannot Say**

**Explanation:** The passage says the Committee "may... in exceptional cases, recommend that a project does not proceed". This defines a power, not an event. Nothing in the passage reports that the power has ever been exercised. The statement could be true in the world — but the passage neither confirms nor contradicts it, which is precisely what Cannot Say means. Senior candidates lose marks here by letting plausibility ("surely it has happened at least once") stand in for textual evidence. The discipline of separating "the rules permit X" from "X has occurred" is the same one you apply when reading audit reports and compliance summaries.

**Question 4 (moderate)**

True, False, or Cannot Say: "The annual published summary must include every referral made to the Committee during the year."

**Correct answer: False**

**Explanation:** The passage requires departments to publish "an annual summary of Committee referrals, *excluding* any detail that would compromise operational security". The published document is a *summary*, and it is explicitly required to omit security-sensitive material. The statement asserts an unconditional completeness obligation — the summary "must include every referral" — but the passage imposes no such obligation and, through the exclusion clause, expressly qualifies what the publication contains. An unconditional "must include every" cannot be reconciled with a mandated exclusion, so the statement contradicts the passage's qualified wording and the answer is False. The general lesson: when a statement strengthens the passage — replacing a qualified duty with an absolute one — it becomes False, not merely unproven. Transparency reporting with security carve-outs is a structure you will recognise from your own annual governance cycle, which is exactly why assessors expect you to read its qualifications precisely rather than from memory of how such regimes usually work.

**Passage B — Evaluation report extract (for Questions 5–8)**

"The pilot deployed a machine learning model to prioritise housing repair requests across three participating local authorities between January and June. Average time-to-repair for urgent cases fell by 22% compared with the same period last year. Participating authorities also reported higher tenant satisfaction, although response rates to the satisfaction survey were below 30%. The evaluation team cautions that two of the three authorities simultaneously increased their repairs budgets, and that the winter period covered by the baseline included an unusually severe cold spell. The team concludes that the model shows promise but that attribution of the improvement to the model alone is not yet supported. A randomised evaluation across ten authorities is proposed for next year."

**Question 5 (easy)**

True, False, or Cannot Say: "Average time-to-repair for urgent cases improved during the pilot compared with the baseline period."

**Correct answer: True**

**Explanation:** The passage states directly that "average time-to-repair for urgent cases fell by 22% compared with the same period last year". Falling time-to-repair is an improvement, and the comparison period is the stated baseline. This is a straightforward retrieval item — the kind you should bank quickly and confidently in the live assessment, spending your saved seconds on the harder inference items that follow. Note what it does *not* say: it does not attribute the improvement to the model. Keeping the fact and its explanation separate is where the next questions go.

**Question 6 (moderate)**

True, False, or Cannot Say: "The model caused the 22% reduction in time-to-repair."

**Correct answer: Cannot Say**

**Explanation:** The passage reports the reduction as fact but explicitly cautions that "attribution of the improvement to the model alone is not yet supported", citing the budget increases and the severe baseline winter as confounders. The passage neither asserts that the model caused the improvement nor asserts that it did not — it says the causal question is open. That makes the statement Cannot Say, not False: False would require the passage to contradict the claim, and cautioning that a claim is "not yet supported" is not the same as declaring it wrong. This True/False/Cannot Say boundary — unproven versus disproven — is the verbal-reasoning form of the correlation-causation critique you apply daily to evaluations, and assessors use it to separate careful readers from confident ones.

**Question 7 (moderate)**

True, False, or Cannot Say: "All three participating authorities increased their repairs budgets during the pilot."

**Correct answer: False**

**Explanation:** The passage states that "two of the three authorities simultaneously increased their repairs budgets". The statement claims all three did. Two-of-three directly contradicts all-three, so the answer is False. Quantifier precision — two, all, some, most — is among the most heavily tested reading skills because it is among the most consequential in governance documents: a control adopted by "some" services is a very different assurance position from one adopted by "all". Fast readers gliding over "two of the three" as "the authorities increased budgets" hand this mark away.

**Question 8 (hard) — Best summary**

Which statement best summarises the evaluation team's conclusion?

- A) The model reduced repair times by 22% and should be scaled to ten authorities.
- B) The pilot's results are encouraging, but confounding factors prevent attributing the improvement to the model, so a stronger evaluation design is proposed.
- C) The pilot failed because tenant satisfaction data was unreliable.
- D) Budget increases, not the model, caused the improvement in repair times.

**Correct answer: B**

**Explanation:** B captures all three elements of the conclusion: promise ("shows promise"), the attribution caveat ("not yet supported", with confounders named), and the proposed next step (a randomised evaluation). A overstates: the passage does not say the model *caused* the reduction, and the ten-authority study is proposed as an evaluation, not a scaling decision. C inverts the tone — a sub-30% survey response is flagged as a limitation, not a verdict of failure. D commits the opposite attribution error to A: the passage says causation is unresolved, not that the budgets explain everything. Best-summary items reward the option that preserves the passage's *calibration* — its hedges as well as its findings — which is exactly the fidelity you owe ministers and senior leaders when compressing an evaluation into a briefing line.

**Passage C — Ministerial briefing note extract (for Questions 9–11)**

"The Minister has asked for options to expand the use of natural language processing across citizen-facing services. Officials recommend a phased approach: an initial six-month discovery focused on correspondence handling, followed, subject to the discovery's findings, by private beta services in two further areas to be selected jointly with operational teams. Officials advise against announcing service-level commitments before the discovery concludes. Funding for the discovery phase can be met from existing budgets; any subsequent phase would require a new bid through the departmental investment board. The Minister's office has indicated that the Minister intends to reference the programme in a speech next month and has requested draft lines by Friday."

**Question 9 (moderate)**

True, False, or Cannot Say: "If the discovery's findings are unfavourable, the private beta services will not go ahead."

**Correct answer: Cannot Say**

**Explanation:** The passage makes the betas conditional — "subject to the discovery's findings" — but never states the decision rule. "Subject to" tells you the findings will be taken into account; it does not tell you what happens when findings are unfavourable (the department might narrow scope, delay, or proceed with modifications). The statement supplies a specific consequence the passage does not contain, so it is Cannot Say. Readers who paraphrase "subject to" as "dependent on success" are adding their own decision logic — a natural habit for someone who writes such briefings, and precisely the habit the assessment asks you to suspend.

**Question 10 (moderate)**

True, False, or Cannot Say: "Proceeding to a private beta phase would require funding beyond existing budgets to be approved."

**Correct answer: True**

**Explanation:** The passage separates the funding positions cleanly: the discovery "can be met from existing budgets", while "any subsequent phase would require a new bid through the departmental investment board". The private betas are a subsequent phase, so they fall under the new-bid requirement — funding beyond existing budgets would need approval through the board. The inference is short but real: you must connect "private beta" to "any subsequent phase". True/False/Cannot Say items reward such immediate entailments while punishing longer speculative chains; learning to feel the difference between a one-step entailment and an added assumption is the core skill.

**Question 11 (hard)**

True, False, or Cannot Say: "The Minister will announce service-level commitments in next month's speech."

**Correct answer: Cannot Say**

**Explanation:** Officials "advise against announcing service-level commitments before the discovery concludes", and the Minister "intends to reference the programme" in the speech. Neither fact settles what the Minister will do: advice can be accepted or rejected, and "reference the programme" does not specify content. The passage gives you an official recommendation and a stated intention — not the Minister's decision. Candidates often choose False here, reasoning that officials advised against it; but advice is not outcome, and intention to "reference" is not commitment-making or its absence. Cannot Say. At your level this mirrors a daily reality: you draft lines, officials advise, and the final words belong to the Minister — the passage's silence on the decision is the point.

**Passage D — Cross-government data standards extract (for Questions 12–14)**

"Departments should adopt the reference data architecture for all new analytical platforms. Existing platforms need not be migrated immediately, but any platform undergoing substantial re-procurement must be brought into conformance at that point. Conformance requires, at minimum: documented data lineage for all critical datasets; role-based access controls; and quarterly quality reporting against the published metrics. Departments may apply for a time-limited exemption where conformance would delay a service designated as critical national infrastructure, provided a remediation plan is agreed within three months of the exemption being granted. Exemptions are granted by the central standards authority, not by departments themselves."

**Question 12 (moderate)**

True, False, or Cannot Say: "A department may grant itself a time-limited exemption for a critical national infrastructure service."

**Correct answer: False**

**Explanation:** The final sentence is decisive: "Exemptions are granted by the central standards authority, not by departments themselves." The statement asserts self-granting, which the passage explicitly rules out. Everything else in the exemption clause — the CNI condition, the remediation plan — is a distractor: the statement fails not on eligibility but on authority. In standards governance, *who* may grant an exception is as important as *when*, and assessors test whether you track both. When you represent your department on data science matters, misremembering where authority sits is the kind of error that surfaces embarrassingly in cross-government meetings, which is why this pattern appears so often in role-specific verbal tests.

**Question 13 (hard)**

True, False, or Cannot Say: "An existing analytical platform that is not being re-procured is currently non-compliant with the standard."

**Correct answer: Cannot Say**

**Explanation:** The passage says existing platforms "need not be migrated immediately" and that substantial re-procurement triggers mandatory conformance. It does not state the compliance status of existing platforms in the meantime: "need not be migrated" suspends the obligation, and a platform without an obligation to conform is arguably neither compliant nor non-compliant — but more importantly, the passage simply never labels such platforms' status. Some existing platforms might already happen to meet all three conformance requirements. Since the passage neither asserts nor denies non-compliance for any particular existing platform, the answer is Cannot Say. The trap is inferring "not yet required to conform" implies "non-compliant" — a conflation of obligation with state. In your assurance work the same distinction separates "this platform has no current conformance duty" from "this platform fails the standard", and confusing them misstates risk to your board.

**Question 14 (hard) — Precise comprehension**

According to Passage D, which of the following is NOT a minimum requirement of conformance?

- A) Documented data lineage for all critical datasets
- B) Role-based access controls
- C) Quarterly quality reporting against published metrics
- D) A remediation plan agreed within three months

**Correct answer: D**

**Explanation:** The passage lists conformance's minimum requirements explicitly: lineage documentation, role-based access controls, and quarterly quality reporting — options A, B, and C. The remediation plan belongs to a different mechanism: it is the condition attached to a time-limited *exemption*, not a component of conformance. Negative items ("which is NOT...") reward slowing down for five seconds to check each option against the list's boundaries, because the distractor is always drawn from adjacent text performing a different function. Reading a standard means knowing not just what it says but which clause each requirement lives in — the difference between what conformance demands and what an exemption costs.

**Question 15 (hard) — Author's purpose**

The primary purpose of Passage B (the evaluation report extract) is to:

- A) Persuade authorities to adopt the housing repairs model immediately.
- B) Report pilot results with appropriate caveats and recommend a more rigorous next-stage evaluation.
- C) Criticise the participating authorities for confounding the pilot by raising budgets.
- D) Demonstrate that machine learning cannot be evaluated in operational settings.

**Correct answer: B**

**Explanation:** The passage's structure is: results (22% reduction, satisfaction signals), limitations (survey response rate, budget confounders, baseline weather), calibrated conclusion ("shows promise but... attribution... not yet supported"), and a proposed randomised evaluation. That is the anatomy of a balanced evaluation report, matching B. A ignores the explicit caution against attribution. C misreads a neutrally reported confounder as criticism — the passage assigns no blame. D generalises far beyond anything stated; indeed the proposal of a randomised evaluation presumes evaluation *is* possible. Purpose items ask you to stand back from individual sentences and name what the document is doing — a skill you exercise every time you decide whether a paper reaching your desk is informing, recommending, or advocating, and therefore how hard to interrogate it.

**Question 16 (moderate) — Word-in-context**

In Passage D, "Departments *should* adopt the reference data architecture for all new analytical platforms." Given the passage's later use of "must" and "may", the word "should" most precisely indicates that adoption is:

- A) Mandatory in all cases.
- B) Strongly expected, but not framed with the same mandatory force as the "must" obligations.
- C) Entirely optional, equivalent to "may".
- D) Required only for critical national infrastructure services.

**Correct answer: B**

**Explanation:** The passage deploys a graded vocabulary deliberately: "should adopt" for new platforms, "must be brought into conformance" at re-procurement, "may apply for a time-limited exemption". In standards drafting, this gradation is meaningful — "must" marks an absolute requirement, "may" a permission, and "should" a strong expectation or recommendation that sits between them. Reading "should" as "must" (option A) manufactures obligations the text does not impose; reading it as "may" (option C) erases an expectation the text clearly conveys; option D imports the CNI condition from the unrelated exemption clause. Standards bodies, legislation, and government guidance all rely on this must/should/may hierarchy, and as the person who oversees compliance with standards and legislation across your organisation, calibrating obligation strength from the exact modal verb is a skill you exercise — and are assessed on — sentence by sentence.

### Preparation tips

- **Train the three-way distinction daily.** Take one paragraph from a real policy, standard, or evaluation each day and write one True, one False, and one Cannot Say statement about it. Composing items teaches the boundaries faster than answering them.
- **Read the statement first, then hunt.** For True/False/Cannot Say items, read the statement before the passage, then scan for the governing clause. Reading the whole passage first is slower and encourages answering from overall impression.
- **Underline the operators.** Mentally flag must/may/should, all/some/none, unless/provided/subject to, intends/has agreed. Nearly every hard item above turns on one of these words.
- **Quarantine your expertise.** You know how ethics committees, spending controls, and standards regimes actually work. The passage may differ deliberately. Before answering, ask: is my evidence in the text, or in my experience?
- **Bank the easy retrieval items fast.** Direct-lookup questions should take twenty seconds; invest the surplus in Cannot Say boundary cases, which reward a second careful pass.
- **Practise on the documents your role already sends you.** Ethics framework updates, standards consultations, evaluation reports, and investment board papers are the exact genres these tests imitate. Once a week, take one such document and interrogate three of its sentences: what does this clause oblige, permit, or leave open? Ten minutes of this converts routine reading into assessment training, and it sharpens the compliance oversight and briefing work you do anyway.
- **Rehearse summarising with the caveats intact.** Best-summary items reward the option that keeps the passage's hedges. Practise compressing a page into one sentence that preserves both the finding and its qualification — the same craft as writing an honest line for a ministerial briefing.

### Common pitfalls

- **Importing outside knowledge.** The most common failure for expert candidates: answering from professional reality rather than the passage. If the text does not say it, it is not evidence — however true it is in your department.
- **Confusing "unproven" with "false".** A passage that says evidence is insufficient has not contradicted the claim; that is Cannot Say. Conversely, a statement that strengthens a qualified duty into an absolute one is False, not Cannot Say.
- **Gliding over quantifiers and modals.** "Two of the three", "may", "advise against" — misreading any of these flips the answer. Under time pressure, precision beats speed.
- **Treating likely outcomes as stated facts.** "Subject to findings" does not tell you what happens if the findings disappoint; supplying the consequence yourself converts Cannot Say into a wrong True or False.
- **Losing the clause structure.** Requirements, exemptions, and exceptions live in different clauses; attributing a remediation condition to conformance, or a Committee power to a decision-maker, are structural misreads that role-specific tests deliberately provoke.
- **Poor time discipline.** Under a minute per item means a stuck Cannot Say boundary case should be flagged and revisited, not agonised over while three retrieval items go unanswered.

## Workplace job-specific situational judgement assessment

### About this assessment

A workplace job-specific situational judgement assessment presents realistic dilemmas from your working life and asks you to evaluate possible responses. Unlike cognitive or numeric tests, there is rarely a single objectively correct answer; instead, some responses align better than others with the values and behaviours the role demands. Formats vary: choose the **most effective** and **least effective** actions from a set, rank all options from best to worst, or rate each option's effectiveness independently. Timing is usually generous or untimed — the assessment measures judgement, not speed.

For a Head of Data Science, scenarios revolve around your real stakeholders — ministers and their offices, senior leaders, the Ethics Board, data engineers, user researchers, delivery managers, arm's-length bodies, suppliers, and your own data scientists — and your real tensions: delivery pace versus ethical assurance, ministerial expectations versus evidential honesty, team advocacy versus organisational priorities, innovation versus stewardship of public money and public trust.

Strong answers at your level consistently reflect UK public sector values: put user needs first; be transparent, especially about uncertainty and error; collaborate across professions rather than defend silos; build accessibility and inclusion in from the start; act early on ethical risk; and develop your people. Weak answers tend to be passive (wait and see), evasive (pass the problem along), unilateral where collaboration is owed, or expedient at the cost of trust. Assessors also penalise idealistic answers that ignore practical constraints — the best option is usually both principled *and* workable.

### What it measures for your role

Mapped to the skills in your role profile:

- **Data ethics and privacy** — dilemmas where delivery pressure, ministerial interest, or commercial convenience collide with your duty to oversee ethics compliance, develop an ethical culture, and influence others to act on it.
- **Delivering business impact** — scenarios about championing data science, gathering genuine user needs, and taking responsibility for scalable products and their maintenance rather than chasing demos.
- **Developing data science capability** — situations testing how you grow people: CPD direction, technical leadership, retention, and giving colleagues guidance without doing their jobs for them.
- **Understanding product delivery and Data engineering** — dilemmas about MVP scope, method choice, and working with engineers and multidisciplinary teams to deliver smoothly.
- **Communication to ministers and senior leaders** — scenarios about presenting uncertainty honestly, correcting errors publicly, and championing data science credibly across professions and departments.

### Practice questions

For each scenario, identify the **most effective** and **least effective** responses before reading the answer.

**Question 1 (moderate) — The minister wants a stronger number**

You are finalising a briefing for a ministerial speech. Your team's analysis estimates a new data-matching service will save "between £2 million and £6 million per year, with £3.5 million most likely". A private office official asks you to change the line to "will save £6 million per year" because "the range sounds weak".

- A) Agree to the change; £6 million is within your team's estimated range, so it is technically defensible.
- B) Refuse and escalate immediately to the Permanent Secretary that the private office is distorting analysis.
- C) Explain why quoting the top of the range as a central claim would misrepresent the evidence, and offer stronger wording that remains faithful — for example, "up to £6 million, with £3.5 million expected".
- D) Say nothing and quietly reinstate the original range in the final version, hoping no one notices.

**Most effective: C. Least effective: D.**

**Explanation:** C does what your role demands: it defends analytical integrity while solving the communicator's real problem — the official wants impact, and "up to £6 million, with £3.5 million expected" delivers impact honestly. Communicating data science effectively to ministers means finding language that is both faithful and usable, not just saying no. A fails your duty of evidential honesty: presenting a range's ceiling as the headline claim misleads, and when actual savings land near £3.5 million the credibility cost falls on the Minister and on your profession. B is disproportionate as a first move: escalating a routine drafting disagreement as "distortion" before attempting resolution damages the working relationship your role depends on — escalation is the right second step if pressure persists after C. D is the worst of all worlds: covert, likely to be discovered at the final check, and it converts an honest disagreement into apparent bad faith. It also solves nothing — the official will simply change it back. Transparency plus constructive alternatives beats both capitulation and confrontation.

**Question 2 (moderate) — The flagship model fails its bias audit**

Two weeks before a well-publicised launch, an internal audit finds your flagship eligibility-triage model recommends rejection significantly more often for one demographic group, unexplained by legitimate factors. The programme director, under delivery pressure, proposes launching on time and "fixing fairness in phase two". Rank these responses from most to least effective:

- A) Support the launch with a public commitment to address fairness in phase two.
- B) Recommend delaying launch until the disparity is understood, and bring the audit findings, options, and a revised timeline to the programme board with the Ethics Board's advice attached.
- C) Quietly ask your team to apply a statistical adjustment that equalises rejection rates before launch, without wider review.
- D) Tell the programme director the model cannot ever launch and withdraw your team from the programme.

**Most effective order: B, D, C, A.** (Most effective: B. Least effective: A.)

**Explanation:** B is the model answer: it acts on the ethical risk before harm occurs, uses governance rather than personal fiat, is transparent with decision-makers, and pairs the bad news with options and a path forward — leadership on ethics as your profile defines it. D, though heavy-handed and collaboration-damaging, at least prevents the harm; an over-cautious refusal ranks above options that let a discriminatory system reach citizens. C is seriously wrong despite its technical veneer: an unreviewed adjustment may mask rather than fix the problem, bypasses the ethics governance you yourself oversee, and creates a hidden intervention that will not survive scrutiny — but it does attempt to address the disparity. A is worst: it knowingly launches a system with unexplained discriminatory outcomes affecting real people, treats fairness as a deferrable feature, and stakes public trust on a promise. In UK public sector data ethics, preventing algorithmic harm to citizens outranks every delivery milestone; the ranking rewards those who see that C's secrecy is worse than D's bluntness, and that A's polished pragmatism is the most dangerous option on the list.

**Question 3 (moderate) — Two professions, one product**

Your data scientists have built a churn-prediction prototype for a citizen-facing service. The service's user researchers report that front-line staff do not trust the predictions and will not use them; your lead data scientist responds that "the model's AUC is excellent — the users need training". The product is stalling.

- A) Direct the service team to mandate use of the predictions, since the model is statistically sound.
- B) Bring the data scientists and user researchers together to observe front-line staff using the tool, and reframe the goal as improving decisions rather than defending the model.
- C) Accept the user researchers' verdict and shelve the prototype.
- D) Commission an independent statistical review to confirm the AUC figure.

**Most effective: B. Least effective: A.**

**Explanation:** B embodies two named elements of your role: championing user research (you "understand and champion user research, and can design and manage processes to gather and establish user needs") and collaborative working across professions. A statistically excellent model that users will not act on delivers no business impact; watching real usage typically reveals fixable causes — opaque outputs, poor timing in the workflow, missing explanations — that neither profession can see alone. A is least effective: mandating use of a distrusted tool poisons the service relationship, invites workarounds, and abandons user-centred practice; adoption by decree is how public sector tools die quietly. C capitulates without diagnosis — the researchers reported a trust problem, not a value problem — and wastes the investment. D answers a question nobody asked: the AUC is not in dispute; the human-model interface is. The scenario tests whether you locate the problem in the sociotechnical system rather than in one profession's artefact — the daily work of a leader who delivers data science products into organisations rather than into repositories.

**Question 4 (hard) — A capability walking out of the door**

Your only senior NLP specialist — the technical anchor of two live products — resigns, giving four weeks' notice, for a substantially higher private sector salary. Two of your data scientists could eventually grow into the specialism.

- A) Ask HR to explore a counter-offer while immediately starting structured knowledge transfer: the specialist pairs with the two developing data scientists for the notice period and documents the critical model pipelines.
- B) Focus the specialist's final four weeks on delivering as much product work as possible, since capability development can wait until after the deadline crunch.
- C) Ask the specialist to leave immediately to protect intellectual property.
- D) Accept the resignation and begin external recruitment for a like-for-like replacement.

**Most effective: A. Least effective: C.**

**Explanation:** A treats the notice period as what it is at your level: a four-week window to convert individual knowledge into organisational capability. Pairing plus documentation addresses the single-point-of-failure you should arguably never have allowed; the parallel counter-offer conversation is legitimate, though at that salary gap it may fail — which is why A does not depend on it. This is "building capability" and "helping colleagues to develop skills" under real conditions. B is short-sighted: it extracts product output while the transferable knowledge walks out permanently — trading four weeks of delivery for years of fragility. D is passive but not destructive: recruitment will take months in a competitive market and does nothing with the notice period, yet it eventually restores capability. C is least effective: it is needlessly adversarial toward a colleague leaving legitimately, forfeits the entire knowledge-transfer window, signals distrust to the whole team, and public sector employment practice provides no basis for treating an ordinary resignation as a security event. The ranking rewards leaders who respond to attrition by strengthening the system rather than punishing the person.

**Question 5 (hard) — The pilot the evidence doesn't support**

A director-general sponsor is enthusiastic about a supplier's proposal to pilot a generative AI tool for summarising case files, and asks you to endorse it at next week's investment board. Your team's technical review finds the supplier's accuracy claims are based on unrelated benchmark data, and no testing has been done on your department's document types, which include legally sensitive material.

- A) Endorse the pilot to maintain the sponsor's support for data science, and plan to raise concerns later if problems emerge.
- B) Present your technical review at the board, recommend a small structured evaluation on departmental documents with clear success criteria before any pilot involving live casework, and offer to design it.
- C) Decline to attend the board so you are not associated with the decision either way.
- D) Send the sponsor a strongly worded note stating the proposal is technically illiterate and should be rejected outright.

**Most effective: B. Least effective: C.**

**Explanation:** B is textbook senior judgement: it neither blocks innovation nor blesses unevidenced claims. Recommending a bounded evaluation with success criteria converts enthusiasm into a test the evidence can pass or fail, protects legally sensitive casework from an unvalidated tool, and keeps you in the role your profile describes — supporting and enabling future IT developments while leading on ethics. Offering to design the evaluation makes you the sponsor's ally, not obstacle. A repeats the oldest failure in technology governance: endorsing now and objecting later, by which point money, announcements, and reputations are committed — and your endorsement will be cited. D may be substantively right but is rhetorically ruinous: insulting a sponsor's judgement in writing forecloses the collaboration your role depends on, and "reject outright" overshoots what the evidence supports (the tool is untested, not proven bad). C is least effective because it is pure abdication: the department's most senior data science voice absenting themselves from a data science investment decision fails the role's core purpose — you exist to put expertise into exactly that room. Visible, constructive, evidence-anchored engagement beats absence, aggression, and acquiescence alike.

**Question 6 (moderate) — The data engineers' warning**

Your head of data engineering warns that the pipeline feeding your most-used forecasting dashboard is "held together with duct tape" and needs a two-sprint rebuild, during which the dashboard's daily updates would pause. Senior leaders check the dashboard every morning and a spending review is approaching. Your lead data scientist argues the rebuild can wait six months.

- A) Postpone the rebuild until after the spending review; the dashboard is too visible to interrupt.
- B) Agree the rebuild now, negotiate a reduced-frequency interim service (weekly snapshots with cached data), and tell senior leader users what is happening, why, and for how long.
- C) Order the rebuild done in parallel with daily operations, accepting the engineering team's overtime.
- D) Ask the data engineers to document the risks formally so responsibility is clear if the pipeline fails.

**Most effective: B. Least effective: D.**

**Explanation:** B takes the specialist warning seriously — you work with data engineers to design and provide products, and dismissing their assessment because a statistician outranks them politically would be a profession-collaboration failure — while managing the genuine visibility constraint with an interim service and honest stakeholder communication. Users who understand a brief, planned degradation stay confident; users surprised by an unplanned outage during a spending review do not. A gambles the department's most-used decision tool on six months of duct tape during the period of heaviest scrutiny: if it fails mid-review, the cost dwarfs two sprints. C sounds decisive but burns out the engineering team and, by running rebuild and operations off the same fragile system, raises the failure risk it is trying to avoid. D is least effective because it is pure liability management: documenting risk without mitigating it protects no user, fixes no pipeline, and signals that your leadership priority is blame allocation rather than service reliability — the inverse of taking responsibility for maintenance support of the products you deliver.

**Question 7 (hard) — A colleague's conference claim**

At a cross-government event, a fellow head of profession from another department presents your directorate's early experimental fraud-detection results as "proven at scale across government", crediting the collaboration. Delegates are visibly impressed; procurement colleagues begin asking you when they can adopt it.

- A) Correct the record publicly during the Q&A, making clear the results are experimental and not yet validated at scale.
- B) Let the claim stand to preserve the collaboration and the profession's growing reputation.
- C) Speak to the colleague privately straight after the session, agree a joint correction to circulate to attendees, and give the procurement colleagues an accurate written status when you respond to them.
- D) Report the misrepresentation to the colleague's permanent secretary.

**Most effective: C. Least effective: B.**

**Explanation:** C repairs the record — which must be repaired, because procurement decisions are already forming around a false claim — while preserving the relationship and the collaboration. A joint correction from both parties is more credible and less humiliating than a public contradiction, and the written status to procurement colleagues stops the concrete harm. A ranks second: the record does get corrected, and there are moments when immediate public correction is necessary (for instance if decisions were being taken in the room), but contradicting a peer from the floor inflicts avoidable damage on a relationship your role tells you to cultivate — you champion data science "in collaborative working across professions". D escalates before attempting resolution, treating a probably careless overstatement as misconduct; it is the move of last resort if the colleague refuses to correct. B is least effective: allowing a false capability claim to propagate through government trades long-term trust for short-term glow. When departments adopt an "proven" tool that then underperforms, the reputational damage lands on data science as a profession — the very thing you are trying to build. Honest representation of maturity is a form of championing, not a betrayal of it.

**Question 8 (moderate) — The junior analyst's discovery**

A junior data scientist emails you directly, bypassing two management layers, to say she believes a production matching algorithm has been silently mismatching around 2% of records for months, affecting benefit correspondence. She attaches a persuasive notebook and says her team lead told her the issue was "known and accepted".

- A) Forward the email to her team lead, asking them to handle it and reminding the analyst of the management chain.
- B) Thank her for raising it, commission an immediate technical verification of the finding, and separately establish with the team lead what "known and accepted" meant and whether the risk acceptance was ever properly made and recorded.
- C) Immediately halt the matching algorithm pending investigation.
- D) Ask her to present the finding at the next monthly quality meeting in three weeks.

**Most effective: B. Least effective: A.**

**Explanation:** B does three things a head of profession must do at once: takes the substance seriously (verify first — a persuasive notebook is not yet a confirmed defect), takes the governance question seriously (a 2% silent mismatch affecting citizens' benefits may have been "accepted" by no one with authority to accept it, and if it was, where is the record?), and protects the person who spoke up. A is least effective — worse even than the delay of D — because it returns the concern to the very person who allegedly dismissed it, adds an implicit rebuke for escalating, and teaches your whole directorate that raising risk gets you sent back down the chain. A leader developing a data ethics culture, "influencing others to act on it", depends on exactly this kind of upward signal surviving. C is premature as a first move: halting a production service processing benefits correspondence has its own citizen impact and should follow, not precede, rapid verification — though it becomes right within days if the finding confirms. D treats a live citizen-affecting defect as an agenda item; three weeks of continued mismatching is three weeks of harm. Speed of verification, integrity of governance, and safety of the messenger — B is the only option that honours all three.

**Question 9 (hard) — The MVP that keeps growing**

A multidisciplinary team building a data science product for prison education planning has seen its MVP scope triple: the policy team wants extra cohort breakdowns, the supplier proposes a recommendation engine, and your own data scientists want to add a causal inference module. The delivery manager privately tells you the launch date is now impossible but no one will say so in the steering group.

- A) In the steering group, restate the user need the MVP exists to meet, ask each addition's sponsor to evidence its necessity for that need, and re-baseline the scope and date openly with the delivery manager's assessment on the table.
- B) Let the scope stand but move the launch date privately with the supplier, avoiding a confrontation in the steering group.
- C) Cut all three additions unilaterally and announce the original scope is restored.
- D) Ask the delivery manager to raise the timeline concern themselves at the next steering group, offering your support from the chair.

**Most effective: A. Least effective: B.**

**Explanation:** A performs the exact duty in your profile — "define the minimum viable product and support decisions about priorities" — using the discipline that makes MVPs work: every feature must trace to the validated user need, and trade-offs are made transparently by the governance forum, not in corridors. Putting the delivery manager's honest assessment "on the table" also breaks the collective silence, which is itself the deeper delivery risk. D is second best: empowering the delivery manager to speak respects their professional role and your support from the chair gives them cover — but it delegates the scope discipline that scope creep from three directions (including your own team) requires the senior owner to lead. C gets the scope right by the wrong means: unilateral reversal in a multidisciplinary partnership wins the baseline and loses the partners, and at least some additions might genuinely serve the user need. B is least effective: it changes the delivery commitment covertly, leaves the steering group governing a fiction, endorses unbounded scope, and when the private date slips too — as unmanaged scope guarantees — both the product and your candour will be questioned. Smooth delivery of data science products into organisations, as your profile puts it, is achieved in the open.

**Question 10 (hard) — The cross-government data request**

A policy director asks your team to link departmental service data with a dataset from another department to profile "households likely to need intervention". The policy aim is genuinely protective — early support for vulnerable families — but the request arrives with no legal basis identified, no DPIA, and a hoped-for turnaround of two weeks driven by a ministerial commitment.

- A) Decline until every governance artefact is complete, and inform the director that the timeline is impossible.
- B) Proceed with a rapid prototype on the full linked data, in parallel with the paperwork, given the protective intent.
- C) Convene the information governance, legal, and ethics leads within days; scope what *can* be done lawfully and quickly — such as methodology design and analysis on synthetic or existing lawfully-held data — while the legal basis and DPIA for linkage are established properly.
- D) Ask the other department to do the linkage instead, so the legal risk sits with them.

**Most effective: C. Least effective: B.**

**Explanation:** C refuses the false choice between blocking a protective policy and breaking data protection law. Convening governance colleagues fast honours the ministerial timescale as a constraint to engineer around, not a reason to cut corners; sequencing lawful preparatory work (methodology, synthetic-data development, analysis of data you already lawfully hold) in parallel with the DPIA and legal-basis work means the fortnight is not wasted even though full linkage waits. This is ethics leadership as your profile frames it — ensuring data ethics is applied "when formulating, implementing and evaluating" policy, not merely at the end. B is least effective: linking personal data across departments with no legal basis is unlawful regardless of intent, and "protective" profiling of families is precisely the class of activity where governance failures cause both citizen harm and programme-destroying scandal — the prototype would contaminate, not accelerate, the policy. A is principled but unhelpfully binary: it treats governance as a gate rather than a discipline, surrenders the chance to deliver anything useful in the window, and teaches policy colleagues to route around your profession next time. D is risk-shuffling dressed as delegation: the legal basis is absent wherever the linkage happens, and exporting a known compliance gap to a partner department is a collaboration and integrity failure. The scenario rewards leaders who make lawful the fastest available path.

**Question 11 (moderate) — The capability budget trade-off**

Mid-year pressures force you to surrender either your £120,000 external training and conference budget or an equivalent sum that funds protected "10% time" for your data scientists' development projects, which last year produced two tools now in production. Your directors will accept either.

- A) Surrender the external training budget, protect the 10% time, and rebuild external development through cheaper channels: cross-government communities, vendor-provided free training, and internal teach-backs.
- B) Surrender the 10% time; external training is more visible and easier to restore next year.
- C) Split the cut equally so neither is destroyed.
- D) Ask your data scientists to vote on which to keep.

**Most effective: A. Least effective: B.**

**Explanation:** A reflects evidence-based capability leadership: the 10% time has demonstrated production-grade return, and its value — protected practice, innovation culture, retention of people who could earn more elsewhere — is the hardest to rebuild once broken. External development genuinely matters ("keep up to date with new developments in data science" is in your profile), but it has cheap substitutes in the UK public sector: cross-government data science communities, free vendor training, and structured internal teach-backs preserve much of the benefit. B is least effective because it optimises for visibility over value — cutting the mechanism with proven organisational return to keep the line item that is easier to see — and because innovation time, once withdrawn, signals that development is a perk rather than a professional expectation; the retention damage lands with your strongest people first. C halves two budgets into two ineffective ones: a 5% time allocation is functionally none. D abdicates a leadership judgement that requires information the team lacks (the directors' constraints, the retention picture) — consultation is wise, delegation of the decision is not. Setting the direction of CPD within your team is your call to make, with evidence.

**Question 12 (moderate) — The accessibility afterthought**

At a show-and-tell four weeks before public launch, you notice the team's new statistics dashboard relies entirely on red-green colour coding, has no keyboard navigation, and offers no text alternatives for its charts. The product manager says accessibility fixes are scheduled "for the month after launch, once the main features are stable".

- A) Accept the plan; a month's delay to accessibility is minor compared with the value of launching.
- B) State that the service cannot launch to the public in this state, and work with the product manager to re-plan the four weeks so the core accessibility work is done first, descoping lower-value features if needed.
- C) Require the team to add an accessibility statement to the site acknowledging the limitations and committing to fixes.
- D) Escalate the product manager's decision to their line manager as a performance concern.

**Most effective: B. Least effective: A.**

**Explanation:** B treats accessibility as what UK public sector standards say it is: a legal requirement (public sector websites must meet accessibility regulations) and a core part of meeting user needs, not a feature to schedule after "the main features" — for users who cannot distinguish red from green or navigate without a keyboard, accessibility *is* the main feature. Re-planning with descoping keeps the launch realistic rather than punitive, and doing it *with* the product manager preserves the multidisciplinary relationship. C mistakes disclosure for compliance: an accessibility statement documents shortcomings, it does not license launching a public service that excludes users when the fixes are known and achievable pre-launch. D converts a fixable planning error into a personnel incident, skipping the collaborative correction that would fix the product faster and teach the team more. A is least effective: it accepts knowingly excluding disabled users from a public service at launch, normalises inclusion as an afterthought across every future product your directorate builds, and exposes the department legally and reputationally. Leaders set the floor: what you accept at show-and-tell becomes your organisation's standard.

### Preparation tips

- **Anchor on the role's values, not your instincts alone.** Before the assessment, re-read your role profile and the public sector values it encodes: user needs, transparency, ethics leadership, collaboration across professions, capability building. The strongest option almost always advances several of these at once.
- **Look for the option that is both principled and practical.** At senior level, purely principled options that ignore constraints (blanket refusals, immediate escalations) usually rank second, not first. The best answers solve the stakeholder's real problem while holding the line.
- **Check who owns the decision.** Many scenarios turn on governance: advising versus deciding, consulting versus delegating, correcting privately versus publicly. Ask "whose call is this, and what does my role owe the process?"
- **Rank the harms.** When options conflict, prioritise preventing irreversible harm to citizens and to public trust over internal inconvenience, visibility, or speed. That single heuristic resolves most hard rankings above.
- **Reflect, don't just rehearse.** These scenarios are close to your real work. After each practice question, ask when you last faced something similar and whether you acted like your own "most effective" option. That reflection improves both your score and your leadership.

### Common pitfalls

- **Choosing the idealistic answer over the effective one.** "Refuse anything imperfect" sounds virtuous but often abandons the outcome; assessors reward options that achieve the principled result in the real organisation.
- **Selecting passive or deflecting options.** Waiting, documenting risk without acting, sending the problem back down the chain, or absenting yourself from the decision are consistently rated least effective for leadership roles — as several scenarios above illustrate.
- **Escalating first.** Escalation is a legitimate second step and a poor first one. Options that skip the direct, constructive conversation usually rank below those that attempt it.
- **Protecting visibility over value.** Options that optimise for how things look (to boards, ministers, or peers) at the expense of users, evidence, or your team's trust are reliably penalised.
- **Forgetting the messenger.** In scenarios involving someone who raises a concern, how your chosen option treats that person is scored as heavily as how it treats the problem. Cultures of ethics and quality survive on protected messengers.
- **Answering as a technician rather than a leader.** At head-of-profession level, the winning options mobilise governance, relationships, and other professions; options where you personally redo the technical work, however satisfying, rarely rank first.

## Conclusion

Well done for working through this document. You have covered a great deal of ground: the logic of pattern recognition, deduction, and error checking applied to model evaluations, ethics frameworks, and delivery plans; the numeric discipline of budgets, capacity, fairness ratios, and business cases; the verbal precision of must and may, True and Cannot Say, across policies, evaluations, and briefings; and the leadership judgement demanded when ministers, ethics, delivery deadlines, and your own people pull in different directions.

Notice how consistently these four assessments echo the same underlying strengths — the strengths your role profile describes. Critiquing statistical analyses is pattern recognition plus scepticism about denominators. Overseeing ethics compliance is careful reading plus the courage to act on what you find. Building capability is arithmetic about people plus judgement about what to protect when budgets tighten. Communicating to senior leaders is verbal precision plus the integrity to keep the caveats attached. Preparing for these assessments is not a detour from your professional development; it is your professional development, concentrated.

Practical next steps: revisit the questions you found hardest in a week's time and see whether the reasoning now comes naturally. Build the small daily habits suggested in the preparation tips — one recomputed figure from your management pack, one paragraph turned into True/False/Cannot Say statements, one real dilemma reflected on against the values these assessments reward. If a live assessment is ahead of you, ask the organisers about format, timing, and adjustments early, and take every practice item offered. And consider sharing these materials with your own data scientists — coaching others is the fastest way to consolidate your own mastery, and developing your people is, after all, in the job description.

You lead a profession whose value to public services grows every year, and the skills tested here — clear reasoning, honest numbers, precise reading, principled judgement — are the ones that make that leadership trusted. Approach any assessment as an opportunity to demonstrate what you already practise daily. Good luck, and keep developing.
