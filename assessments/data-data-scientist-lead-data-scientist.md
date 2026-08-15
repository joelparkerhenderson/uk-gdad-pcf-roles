# Data Scientist (Lead Data Scientist) - Psychometric Assessment Resources

## Introduction

Welcome. This resource has been prepared specifically for you as a lead data scientist working within the UK Government Digital and Data profession. Whether you are preparing for an internal progression board, applying for a lead data scientist post, benchmarking your own capability, or simply investing in your continued professional development, this document is designed to help you approach psychometric assessments with confidence and clarity.

Psychometric assessments are structured, standardised exercises that measure the mental capabilities and behavioural tendencies that predict success in a specific role. For a lead data scientist, they are not abstract puzzles: well-designed assessments mirror the real intellectual demands of your work — critiquing statistical analyses, interpreting model performance metrics, reading dense policy and standards documents, weighing ethical trade-offs, and making sound judgement calls about people, priorities, and delivery. Because you operate at a leadership level, the assessments you encounter will assume professional maturity: scenarios will involve directing teams, challenging delivery plans, navigating ministerial and departmental pressures, and championing data science across an organisation.

This document is organised into four substantial sections, each covering one assessment type commonly used for digital and data roles in the UK public sector:

1. **Workplace job-specific cognitive assessment** — pattern recognition, logical deduction, error checking, prioritisation, and problem solving using the artefacts you genuinely handle: model pipelines, code review findings, experiment designs, and data quality reports.
2. **Workplace job-specific numeric reasoning assessment** — interpreting tables, percentages, ratios, budgets, capacity figures, and model performance metrics under time pressure.
3. **Workplace job-specific verbal reasoning assessment** — drawing precise conclusions from dense written material such as data ethics frameworks, service standards, governance papers, and stakeholder correspondence.
4. **Workplace job-specific situational judgement assessment** — choosing effective courses of action in realistic leadership dilemmas involving your team, senior stakeholders, and the public interest.

Each section explains what the assessment measures, maps its dimensions to the specific skills in the lead data scientist role profile, provides a bank of realistic practice questions with fully worked answers, and closes with preparation tips and common pitfalls.

How to use this resource: work through the practice questions honestly before reading the explanations; time yourself where timings are suggested; and treat every explanation as a coaching conversation rather than a mark scheme. The goal is not to memorise answers but to sharpen the reasoning habits you already use daily — so that on assessment day, the format feels familiar and your genuine capability shows through. Take your time, be curious, and enjoy the process. You already do this work; this document simply helps you demonstrate it.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive assessment measures the core mental processes that underpin high performance in your role: pattern recognition, logical deduction, error checking, prioritisation, and structured problem solving. Unlike a generic IQ test, a job-specific version is built from the everyday materials of the role being assessed — for a lead data scientist, that means model evaluation outputs, data pipeline diagrams, code review notes, experiment designs, capability matrices, and delivery plans, all set in a UK government context.

Typical format: 15 to 30 minutes, delivered online, with multiple-choice questions of graded difficulty. Some platforms are adaptive, adjusting question difficulty based on your previous answers. Scoring is objective and usually benchmarked against a norm group of comparable professionals, and many employers receive a breakdown of speed versus accuracy rather than a single score. Questions used in formal recruitment are validated to ensure they predict job success without bias — which is precisely the standard you would expect, given your own responsibility for overseeing ethical, defensible use of data across your organisation.

For a lead-level role, cognitive assessments matter for a particular reason: your decisions have a multiplier effect. When you spot a flaw in an experiment design, an entire team avoids weeks of wasted effort. When you fail to notice a data leakage problem, a flawed model may inform a policy decision affecting millions of citizens. Cognitive assessments sample exactly this kind of thinking under mild time pressure.

### What it measures for your role

Mapped against the lead data scientist skill set:

- **Applied maths, statistics and scientific practices** — logical deduction questions test whether you can critique statistical analyses, spot invalid inferences, and reason correctly about model outputs across the whole data life cycle.
- **Data engineering** — pattern recognition and fault-diagnosis questions use pipeline dependencies, data cleansing rules, and transformation logic, reflecting your responsibility for identifying data engineering requirements and putting reusable checks in place.
- **Programming and build (data science)** — error-checking questions mirror code review: finding the inconsistency in a specification, a config table, or a set of coding standards you have set for your team.
- **Data ethics and privacy** — deduction questions test whether a proposed data use follows or breaches the rules of an ethical framework, reflecting your duty to oversee compliance with data ethics standards and legislation.
- **Understanding product delivery** and **Delivering business impact** — prioritisation questions present competing demands across the product delivery life cycle and ask you to sequence work rationally, mirroring your responsibility to challenge delivery plans and priorities.
- **Developing data science capability** and **Data science innovation** — several problems require matching techniques (machine learning, natural language processing, predictive analytics) to organisational opportunities, exactly as the role profile expects.

### Practice questions

**Question 1 (easy) — Pattern recognition in pipeline schedules.**
Your team's nightly pipeline runs four stages in strict sequence: Ingest, Cleanse, Feature-build, Score. Over five nights, the completion times for Cleanse were: 01:10, 01:25, 01:40, 01:55, and 02:10. Ingest always finishes at 00:45. If the pattern continues, on which night will Cleanse first finish after 03:00, counting the night after the last observation as night 6?

A) Night 8  B) Night 9  C) Night 10  D) Night 11

**Correct answer: B) Night 9.**
**Explanation:** Cleanse completion is drifting 15 minutes later each night: 01:10, 01:25, 01:40, 01:55, 02:10 across observed nights 1 to 5. Extend the arithmetic sequence one term at a time: night 6 = 02:25, night 7 = 02:40, night 8 = 02:55, night 9 = 03:10. Night 8's 02:55 is still before 03:00; night 9's 03:10 is the first completion after 03:00, so the answer is night 9. Two habits protect you here: extend the sequence term by term rather than jumping ahead with mental arithmetic (a common slip is to miscount which night the sequence resumes on), and re-read the threshold condition — "after 03:00", not "at or after" — before committing. In a real assessment, thirty seconds of deliberate recounting beats a fast guess. As a lead, this also mirrors a real operational signal: a stage drifting 15 minutes per night indicates growing data volume or degrading infrastructure, and needs intervention before it breaches its processing window — the kind of reusable check your data engineering skill expects you to put in place.

**Question 2 (easy) — Logical deduction from cleansing rules.**
Your team's reusable data-preparation standard states: "Every record must pass validation before enrichment. Any record failing validation is quarantined. Quarantined records are never scored." A stakeholder reports that record X was scored. Which conclusion follows logically?

A) Record X passed enrichment.
B) Record X was never quarantined.
C) Record X passed validation and was enriched.
D) Record X contained no errors.

**Correct answer: B) Record X was never quarantined.**
**Explanation:** The rules give a strict chain: quarantined records are never scored. Since X was scored, X cannot have been quarantined — that is the contrapositive, and it is watertight. Option C over-reaches: the rules require validation before enrichment, but nothing says a scored record must have been enriched — scoring might not require enrichment. Option A similarly assumes enrichment occurred. Option D confuses "passed validation" with "contained no errors": validation checks specific rules and may not catch every error. Lead-level statistical critique is largely the discipline of accepting only what the stated premises entail — the same discipline you apply when critiquing a colleague's causal claim from observational data.

**Question 3 (moderate) — Error checking a model card.**
You are reviewing a model card before a predictive model is deployed to help caseworkers prioritise benefit-fraud referrals. The card states: (i) training data covers April 2022 to March 2025; (ii) the model was evaluated on a random 20% holdout from the same period; (iii) precision at the operating threshold is 0.81; (iv) "the model has been tested for temporal robustness by evaluating performance on cases from April 2025 onward"; (v) the drift monitoring plan begins six months after deployment. Which pair of statements is in tension?

A) (i) and (iii)  B) (ii) and (iv)  C) (iii) and (v)  D) (i) and (v)

**Correct answer: B) (ii) and (iv).**
**Explanation:** Statement (ii) says evaluation used a random holdout from within the training window — a standard but purely in-period test. Statement (iv) claims temporal robustness was tested on post-period data. These are not strictly contradictory, but the card describes only one evaluation set in (ii); if a second, out-of-time evaluation existed, it should be documented with its own metrics. As written, (iv) asserts a test for which no evidence set is described, and (iii)'s precision figure is anchored to the in-period holdout only. A reviewing lead should flag this: either the out-of-time results are missing from the card, or the claim in (iv) is unsupported. Options A, C, and D pair statements that can comfortably coexist. This is exactly the critique-of-statistical-analysis skill your role profile names — and the kind of gap that matters enormously when model outputs will inform decisions about citizens.

**Question 4 (moderate) — Prioritisation across the delivery life cycle.**
It is Monday morning. Four items compete for your attention: (1) a junior analyst's pull request implementing a fix to a scoring bug that is currently sending incorrect prioritisation scores to a live operational team; (2) preparation for Thursday's show-and-tell to the programme board; (3) a request from the ethics committee for clarifications on a data sharing proposal, due Friday; (4) a promising but exploratory NLP prototype your team is excited about. What is the most defensible order of attention?

A) 1, 3, 2, 4  B) 2, 1, 3, 4  C) 1, 2, 3, 4  D) 4, 1, 2, 3

**Correct answer: A) 1, 3, 2, 4.**
**Explanation:** Item 1 is a live harm: incorrect scores are actively steering an operational team, so reviewing and shipping that fix is urgent and important — it comes first, and as the lead your review is the bottleneck. Between items 2 and 3, both have deadlines this week, but item 3 (ethics clarifications) has a hard external dependency: the committee needs time to consider your response before Friday, and ethics compliance is a lead-level accountability; starting it before the Thursday presentation preserves both deadlines. The show-and-tell (2) matters but its material largely exists. The prototype (4) is important for innovation but has no deadline; it is the classic "urgent crowds out important" trap in reverse — it should be scheduled, not dropped. Option C is close but delays the ethics response behind presentation-polishing, risking a rushed answer on the highest-stakes item. Cognitive assessments at lead level reward reasoning about dependencies and irreversibility, not just deadlines.

**Question 5 (moderate) — Deduction from experiment results.**
Your team ran an A/B test on a digital service: variant B's new recommendation model increased task completion from 62% to 66% (statistically significant). The product manager concludes: "The model improves completion for all user groups, so we should roll it out to everyone including assisted-digital users." Which single observation most directly undermines the conclusion?

A) The test ran for only three weeks.
B) Assisted-digital users were excluded from the experiment population.
C) Variant A's completion rate was measured on a Tuesday.
D) The model uses gradient boosting rather than a neural network.

**Correct answer: B) Assisted-digital users were excluded from the experiment population.**
**Explanation:** The conclusion generalises to "all user groups... including assisted-digital users". If that group never appeared in the experiment, no evidence exists about the model's effect on them — the inference simply does not extend to them, however significant the overall result. Option A raises a legitimate but weaker concern (duration affects seasonality and novelty effects, not group coverage). Option C is irrelevant as stated: both variants run concurrently in an A/B test. Option D is immaterial to validity. This mirrors your real accountability for inclusion: UK government services must work for everyone, and a lead data scientist is expected to catch exactly this leap before it reaches a rollout decision.

**Question 6 (moderate) — Pattern recognition in feature behaviour.**
A churn-style model for service drop-off uses four features. During monitoring you observe: when feature F1 rises, predictions rise; when F2 rises, predictions rise; when F3 rises, predictions fall; F4 shows no consistent relationship. This month, F1 fell sharply, F2 was stable, F3 fell sharply, F4 rose. Predictions overall were roughly unchanged. Which explanation is most consistent with the observations?

A) The model has silently failed and is outputting a constant.
B) The downward pressure from falling F1 was offset by falling F3.
C) F4 is now the dominant feature.
D) The monitoring system is reporting last month's data.

**Correct answer: B) The downward pressure from falling F1 was offset by falling F3.**
**Explanation:** Work through the directions: F1 falling should push predictions down (positive relationship). F3 falling should push predictions up (negative relationship — when F3 rises, predictions fall, so when F3 falls, predictions rise). Two opposing pressures of broadly similar magnitude produce roughly unchanged output — exactly what was observed, with F2 stable and F4 uninformative. Option A is contradicted because "roughly unchanged" aggregate output does not imply constant output, and nothing suggests failure. Option C contradicts the stated finding that F4 has no consistent relationship. Option D is possible in principle but explains nothing the simpler mechanism doesn't, and would usually show as an exact repeat, not "roughly unchanged". This is the day-to-day reasoning of model monitoring and maintenance — a responsibility your role profile assigns you explicitly under ensuring products are monitored, maintained and continually improved.

**Question 7 (moderate) — Error checking coding standards.**
You have set four coding standards for your team: (S1) all production code must have unit tests; (S2) any script touching personal data must log an audit record; (S3) open-sourcing requires that no credentials or personal data appear anywhere in the repository history; (S4) exploratory notebooks are exempt from S1 but not from S2. A junior analyst asks to open-source an exploratory notebook that reads pseudonymised case data from a live database using an embedded service password, has no unit tests, and writes audit records. Which standards block the request as things stand?

A) S1 only  B) S3 only  C) S1 and S3  D) S2 and S4

**Correct answer: B) S3 only.**
**Explanation:** Take each standard in turn. S1 does not apply: the artefact is an exploratory notebook, and S4 explicitly exempts notebooks from S1 — so the missing unit tests are not a blocker. S2 is satisfied: the notebook writes audit records. S4 itself imposes nothing beyond keeping S2 in force, which is met. S3 is the blocker, twice over: the notebook contains an embedded service password (credentials in the repository), and pseudonymised case data is still personal data under UK GDPR if re-identification is reasonably possible — so data extracts cached in the notebook's history would also violate S3. The disciplined move is to check every rule against every fact rather than pattern-matching on "no tests = fail". This reflects two of your named skills at once: setting coding standards for your team, and seeking to make code open source where appropriate — "appropriate" being exactly the judgement S3 encodes.

**Question 8 (hard) — Logical deduction in an ethics framework.**
Your organisation's ethical framework, which you maintain, contains these rules: (R1) Any automated decision with significant effects on an individual must have a human review route. (R2) Models trained on protected-characteristic data require sign-off from the ethics board. (R3) If a model requires ethics board sign-off, it cannot be deployed during the pre-election period. (R4) Dashboards that only aggregate data at national level are exempt from R1 and R2. A team proposes deploying, during the pre-election period, a model that recommends (but does not decide) individual case escalations and is trained without any protected-characteristic data. Which statement is correct?

A) Deployment is blocked by R3.
B) Deployment is blocked by R1.
C) Deployment is not blocked by any stated rule, but R1's applicability turns on whether a "recommendation" has significant effects.
D) Deployment is permitted because R4 exempts the model.

**Correct answer: C).**
**Explanation:** Trace each rule. R2 does not bite: no protected-characteristic data was used, so no ethics board sign-off is required. R3 therefore does not bite either, because R3 is conditional on R2-triggered sign-off. R4 is irrelevant: the artefact is a model recommending individual escalations, not a national-level aggregate dashboard — so option D fails. That leaves R1: it applies to "automated decisions with significant effects". The model recommends rather than decides, but if caseworkers follow recommendations by default, the recommendation may function as a de facto decision with significant effects — the rule's applicability genuinely turns on this judgement, which the stated facts do not settle. Option C captures precisely that: no stated rule clearly blocks deployment, but a lead should flag the R1 boundary question rather than wave it through. Options A and B assert certainty the premises do not support. This layered conditional reasoning — and the honesty to say "the rules do not settle this" — is the heart of overseeing compliance with data ethics standards and continuously improving an ethical framework.

**Question 9 (hard) — Problem solving: diagnosing a performance drop.**
A deployed classification model's precision fell from 0.84 to 0.61 over one month while recall stayed stable. During the same month: (i) an upstream team changed a source system, causing one input field to arrive with a new code list; (ii) case volumes rose 40% due to a policy change; (iii) a retraining job failed silently, so the model is three weeks older than intended; (iv) the operational team lowered the score threshold to handle the volume increase. Which change most directly explains stable recall with sharply lower precision?

A) (i) the new code list  B) (ii) the volume increase  C) (iii) the stale model  D) (iv) the lowered threshold

**Correct answer: D) the lowered threshold.**
**Explanation:** Reason from the mechanics of the metrics. Lowering the decision threshold flags more cases: recall typically rises or holds (you catch at least as many true positives) while precision falls (many additional flagged cases are false positives). That signature — stable recall, sharply lower precision — is the classic threshold-change fingerprint. The other options would show different signatures: a corrupted input field (i) or a stale model (iii) would usually degrade both precision and recall, because the model's ability to separate classes worsens overall; a pure volume increase (ii) with an unchanged class mix would leave both metrics roughly stable. In practice you would still investigate (i) and (iii) as contributing factors — silent retraining failure especially demands a pipeline alerting fix — but the question asks for the most direct explanation of the observed pattern. This is exactly the model-monitoring diagnosis your role's product delivery skill covers, and the "reason from the metric's definition" habit belongs to applied statistics.

**Question 10 (hard) — Prioritisation with dependencies and capability.**
You lead a team of five: two senior data scientists (one leaving in four weeks), two mid-level, and one apprentice. Four pieces of work exist: (W1) knowledge transfer of a bespoke forecasting model that only the departing senior understands; (W2) a ministerial commission for analysis due in six weeks that any senior could lead; (W3) a scheduled framework upgrade with a hard vendor deadline in eight weeks, well documented, suited to mid-level staff; (W4) apprentice coaching sessions you have already postponed twice. Which allocation best protects the organisation?

A) Departing senior on W2; remaining senior on W1 handover receiving; mid-levels on W3; postpone W4 again.
B) Departing senior on W1 knowledge transfer with a mid-level receiving; remaining senior on W2; other mid-level on W3; you protect W4 personally.
C) Both seniors on W2 to guarantee the ministerial deadline; mid-levels on W1 and W3; postpone W4.
D) Departing senior finishes W3 quickly; remaining senior on W2; mid-levels on W1; you take W4.

**Correct answer: B).**
**Explanation:** The controlling constraint is irreversibility: in four weeks the departing senior's knowledge of the bespoke model is gone forever, so W1 must involve them now — eliminating options C and D, which assign W1 to people who lack the knowledge to transfer it. Between A and B, the receiving end matters: option A has the remaining senior receive the handover, but that senior is the only person who can credibly lead the ministerial commission (W2, due in six weeks) — loading both onto them creates a single point of failure. Option B transfers knowledge to a mid-level (growing capability, consistent with your responsibility for developing data science capability), keeps the remaining senior focused on W2, covers W3's well-documented work with the other mid-level inside its eight-week window, and stops the repeated deprioritisation of apprentice coaching — postponing W4 a third time signals that development only matters when convenient, corroding the coaching culture your role profile expects you to build. Note the general principle: sequence by irreversibility first, deadlines second, convenience last.

**Question 11 (moderate) — Matching technique to opportunity.**
Four teams bring you problems in the same week: (P1) a policy team wants to understand common themes across 40,000 free-text consultation responses; (P2) an operations team wants next-quarter demand estimates for staffing; (P3) a finance team wants to know which invoice records deviate unusually from historical patterns; (P4) a service team wants to know which of two letter formats produces more responses. Which pairing of technique to problem is most appropriate?

A) P1 topic modelling/NLP; P2 time-series forecasting; P3 anomaly detection; P4 randomised controlled trial
B) P1 anomaly detection; P2 topic modelling; P3 forecasting; P4 clustering
C) P1 forecasting; P2 randomised trial; P3 NLP; P4 anomaly detection
D) P1 clustering of numeric features; P2 anomaly detection; P3 randomised trial; P4 forecasting

**Correct answer: A).**
**Explanation:** Free-text at scale (P1) is a natural language processing problem — topic modelling or modern embedding-based clustering surfaces themes humans cannot read at that volume. Forward demand estimation (P2) is classical time-series forecasting. "Deviates unusually from historical patterns" (P3) is the textbook definition of anomaly detection. Comparing two interventions for effect (P4) is best answered by a randomised controlled trial — an A/B test on letter format — because randomisation isolates the causal effect. The other options scramble these mappings. At lead level, the assessed skill is not knowing the techniques (all options name real ones) but the fluency of matching technique to organisational opportunity — precisely the "match new developments to opportunities in your organisation" behaviour in your capability-development skill, and the "select the most appropriate tools and technologies" expectation at your role level.

**Question 12 (hard) — Error checking a delivery plan.**
A delivery plan you are asked to challenge states: Sprint 1, "build features from the cleansed dataset"; Sprint 2, "data engineers deliver the cleansing pipeline"; Sprint 3, "train and validate the model, then agree the validation approach with the statistics lead"; Sprint 4, "private beta with 5% of caseworkers, and simultaneously begin national rollout communications". How many sequencing faults does the plan contain?

A) One  B) Two  C) Three  D) Four

**Correct answer: C) Three.**
**Explanation:** Fault one: Sprint 1 builds features from a cleansed dataset that does not exist until Sprint 2 delivers the cleansing pipeline — a hard dependency inversion. Fault two: Sprint 3 agrees the validation approach after training and validating; the validation approach must be agreed before validation is performed, or the exercise invites accusations of choosing the test that flatters the model — a scientific-practice failure a lead should catch instantly. Fault three: Sprint 4 begins national rollout communications simultaneously with a 5% private beta; the entire point of a beta phase is to learn whether to proceed and how to adjust, so committing to national rollout messaging before beta evidence exists pre-empts the decision the beta is meant to inform. There is no fourth fault: a 5% private beta with caseworkers is itself a reasonable step. Counting faults forces systematic checking rather than stopping at the first hit — the same behaviour as challenging delivery plans and priorities in the role profile.

**Question 13 (easy) — Deduction about team capability.**
Every member of your team who has completed the cloud certification can deploy models to the production environment. Amrit cannot deploy models to the production environment. What follows?

A) Amrit has not completed the cloud certification.
B) Amrit is not a member of your team.
C) Amrit will fail the cloud certification.
D) Nothing can be concluded.

**Correct answer: A) Amrit has not completed the cloud certification — provided Amrit is on your team; strictly, the safest full statement is that Amrit is not a certified member of your team.**
**Explanation:** The rule says: team member AND certified implies can-deploy. Amrit cannot deploy, so by contraposition Amrit is not (a team member AND certified). If the question context establishes Amrit as a team member — as "team capability" implies — then the certification must be the missing element, giving option A. Notice what does not follow: nothing about future performance (option C), and option B alone over-commits just as A would if Amrit's team membership were unknown. Assessments often include one question testing whether you notice a hidden premise; the strong habit is to state the contrapositive precisely, then apply the context. You use this same care when reasoning about skills matrices and deployment permissions across your team.

### Preparation tips

- **Rehearse with your own artefacts.** Take a recent model card, pipeline diagram, or delivery plan and practise asking: what would contradict this? What depends on what? Which claim lacks evidence? You will find the assessment's puzzles are gentler versions of your Tuesday afternoons.
- **Practise the contrapositive.** A large share of deduction questions reduce to "if A then B; not-B; therefore not-A". Saying the contrapositive silently before looking at the options removes most wrong answers instantly.
- **Sequence by dependency and irreversibility.** For prioritisation items, ask which options destroy future choices (departing staff, live harms, external committees) and put those first, before deadline order.
- **Manage the clock like a triage queue.** With 15–30 minutes for the whole test, no single question deserves more than about 90 seconds. Flag, skip, return — exactly as you coach analysts to timebox investigations.
- **Trust structured reasoning over speed-reading.** Adaptive tests reward accuracy; a slightly slower, systematically correct approach usually outscores a fast, erratic one.

### Common pitfalls

- **Over-reading the question.** Bringing in professional knowledge the question did not state — for example, assuming a model must have been enriched, retrained, or biased when the premises say nothing of the kind. Answer only from what is given.
- **Stopping at the first plausible fault.** Error-checking questions often contain multiple issues or ask "which pair is in tension"; scan every element systematically before answering.
- **Deadline-only prioritisation.** Choosing the option that orders tasks purely by due date, ignoring dependencies, single points of failure, and irreversibility — the distinctions that separate lead-level judgement from list management.
- **Time-sink questions.** Losing five minutes to one hard logic chain and rushing six easy questions afterwards. The scoring almost never justifies this trade.
- **Second-guessing validated wording.** If a question says "recommends but does not decide", that distinction is deliberate. Assessment writers choose words the way you choose model features: nothing is decorative.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment evaluates your ability to analyse, interpret, and make sound decisions using numerical data presented the way it genuinely arrives in your role: performance dashboards, budget tables, capacity plans, model evaluation matrices, and programme metrics. The emphasis is on business-relevant mathematics — percentages, ratios, rates, weighted averages, and cost-benefit estimation — rather than abstract formulae. Most assessments allow or provide an on-screen calculator, because they prioritise interpretation over mental arithmetic, but they impose strict time limits: typically 20 to 60 seconds of thinking per data point extracted, with 15 to 25 minutes for the whole test.

You might reasonably ask why a lead data scientist — someone who builds predictive models and supervises complex statistical work — would face a numeric reasoning test at all. The answer is that the assessment measures something different from technical statistics: fast, accurate quantitative judgement under pressure, with unfamiliar data and no code. In your role this is the skill you use when a finance partner slides a budget table across the desk in a meeting, when a programme board challenges your team's throughput figures live, or when you must sanity-check a junior analyst's headline number before it reaches a minister. Leaders who can do arithmetic-with-meaning in real time earn trust for their profession — and championing the role of data science within the organisation is one of your named responsibilities.

Scores are typically normed against other senior digital and data professionals, so expect the questions at the harder end to involve multi-step calculations, distractor figures, and units that must be reconciled ("in thousands", per-quarter versus per-year, FTE versus headcount).

### What it measures for your role

- **Applied maths, statistics and scientific practices** — extracting correct conclusions from tables and charts, reasoning about rates and proportions, and critiquing numerical claims are directly assessed; several questions below mirror critiquing a statistical analysis someone else has summarised.
- **Delivering business impact** — budget, benefit and unit-cost questions reflect your accountability for identifying and delivering data science products that support organisational objectives, and for making the business case for them.
- **Understanding product delivery** — capacity, velocity and phasing calculations mirror challenging delivery plans and priorities with evidence.
- **Data engineering** — storage, throughput and pipeline-capacity arithmetic reflect your responsibility for designing scalable products with data engineers.
- **Developing data science capability** — training-budget and team-composition calculations reflect your responsibility for setting CPD direction and building organisational capability.
- **Programming and build (data science)** — compute-cost and optimisation trade-off questions reflect writing efficient, optimised code and supervising the team's engineering choices.

### Practice questions

**Question 1 (easy) — Percentage change in model workload.**
Your team's model scored 84,000 cases in Q1 and 105,000 cases in Q2. What was the percentage increase in cases scored?

A) 20%  B) 21%  C) 25%  D) 30%

**Correct answer: C) 25%.**
**Explanation:** Percentage increase = (new − old) ÷ old × 100 = (105,000 − 84,000) ÷ 84,000 × 100 = 21,000 ÷ 84,000 × 100 = 25%. The distractor 21% comes from misreading the absolute increase (21,000) as a percentage, and 20% comes from dividing by the new value (21,000 ÷ 105,000). Always divide by the baseline. This is the arithmetic behind every "demand grew by X%" line you sign off in a quarterly report.

**Question 2 (easy) — Team capacity in FTE.**
Your team has 6 data scientists. Two work 0.8 FTE, one is seconded out 50% of their time, and the remaining three are full time. One full-timer will spend 20% of their time on corporate duties this quarter. What delivery capacity, in FTE, does the team have this quarter?

A) 4.9  B) 5.3  C) 5.5  D) 5.7

**Correct answer: A) 4.9.**
**Explanation:** Two at 0.8 FTE = 1.6. One seconded 50% = 0.5. Three full-timers = 3.0, minus the 20% corporate loading on one of them (−0.2) = 2.8. Total = 1.6 + 0.5 + 2.8 = 4.9 FTE. The common slip is forgetting one deduction — 5.3 results from ignoring the seconded-out reduction beyond a half day, and 5.7 from ignoring the corporate duties. When you challenge delivery plans, this is precisely the arithmetic that turns "we have six people" into "we have 4.9 FTE", and it changes sprint commitments materially.

**Question 3 (moderate) — Budget allocation and unit cost.**
Your annual data science programme budget is £1.2 million: 55% staff costs, 25% cloud compute, 12% software licences, and the remainder training. Mid-year, cloud costs are forecast to overspend by 20% of the cloud allocation, to be funded by cutting the training budget. How much training budget remains, and what percentage of the original training budget is that?

A) £36,000 remaining; 37.5%  B) £36,000 remaining; 40%  C) £60,000 remaining; 62.5%  D) £24,000 remaining; 25%

**Correct answer: A) £36,000 remaining; 37.5%.**
**Explanation:** The remainder for training is 100% − 55% − 25% − 12% = 8%, so training = 0.08 × £1,200,000 = £96,000. Cloud allocation = 0.25 × £1,200,000 = £300,000; a 20% overspend on that is 0.20 × £300,000 = £60,000. Training remaining = £96,000 − £60,000 = £36,000. As a share of the original training budget: 36,000 ÷ 96,000 = 0.375 = 37.5%. Distractor B pairs the right amount with a wrong percentage (40% would be 38,400). Note what the numbers say strategically: a modest-sounding compute overspend consumes nearly two-thirds of the team's development budget — exactly the trade-off a lead who sets CPD direction must be able to quantify instantly and challenge.

**Question 4 (moderate) — Model performance metrics.**
Your fraud-referral model flagged 2,400 cases last quarter. Investigators confirmed 1,800 as genuine referrals. Across the whole caseload, there were 3,000 genuine referral-worthy cases in total. Calculate the model's precision and recall.

A) Precision 75%, recall 60%  B) Precision 60%, recall 75%  C) Precision 75%, recall 80%  D) Precision 80%, recall 75%

**Correct answer: A) Precision 75%, recall 60%.**
**Explanation:** Precision = true positives ÷ flagged = 1,800 ÷ 2,400 = 0.75 = 75%. Recall = true positives ÷ all genuine cases = 1,800 ÷ 3,000 = 0.60 = 60%. Option B simply swaps the two — the most common error under time pressure, and worth a deliberate ritual: "precision is out of what we flagged; recall is out of what was really there." As a lead you will present these figures to non-specialist boards, so being fluent in computing and narrating them from raw counts — not just reading them off a validation report — is part of communicating and presenting effectively at your role level.

**Question 5 (moderate) — Weighted average across services.**
Your team supports three services with monthly prediction volumes and error rates: Service A, 50,000 predictions at 4% error; Service B, 30,000 predictions at 6% error; Service C, 20,000 predictions at 9% error. What is the overall error rate across all predictions?

A) 5.6%  B) 6.3%  C) 5.0%  D) 6.0%

**Correct answer: A) 5.6%.**
**Explanation:** Total errors = (50,000 × 0.04) + (30,000 × 0.06) + (20,000 × 0.09) = 2,000 + 1,800 + 1,800 = 5,600. Total predictions = 100,000. Overall rate = 5,600 ÷ 100,000 = 5.6%. The trap answer is B, 6.3% — the simple average of 4%, 6% and 9% (19 ÷ 3) — which ignores that Service A dominates the volume. Weighted versus unweighted averages is one of the most frequent errors in real management reporting; a lead data scientist who catches an unweighted average in a board paper protects the organisation from a wrong headline. If asked to critique a statistical analysis in your assessment, check the weighting first.

**Question 6 (moderate) — Cloud compute cost comparison.**
Retraining your main model takes 40 hours on current infrastructure at £3.20 per hour. A data engineer proposes an optimised pipeline: 60% faster, on instances costing £5.00 per hour, plus a one-off engineering cost of £1,400. Retraining happens monthly. After how many months does the optimised pipeline break even?

A) 25 months  B) 29 months  C) 32 months  D) It never breaks even

**Correct answer: B) 29 months.**
**Explanation:** Current cost per retrain = 40 × £3.20 = £128. Optimised: 60% faster means 40% of the time = 16 hours; 16 × £5.00 = £80. Saving per retrain = £128 − £80 = £48 per month. Break-even = £1,400 ÷ £48 ≈ 29.2 months, so 29 is the closest option: after 29 monthly retrains the savings (£1,392) have essentially covered the one-off cost. Two traps to note: forgetting that "60% faster" leaves 40% of the runtime (not 60%), which wrecks the per-run saving; and comparing hourly rates alone (£5.00 versus £3.20 looks like a cost increase until multiplied by hours). The leadership insight is real, too: a two-and-a-half-year payback deserves scrutiny — if the model or platform will be replaced sooner, the £1,400 never pays back, so always ask over what horizon a saving is claimed. This mirrors your programming-and-build responsibility for efficient, optimised code and your role-level authority to select the most appropriate tools and technologies.

**Question 7 (hard) — Ratio reasoning on team composition.**
Departmental guidance recommends a ratio of at most 3 delivery data scientists per 1 senior reviewer to maintain code review standards. Your directorate currently has 14 delivery data scientists and 4 senior reviewers. A growth bid will add 10 more delivery data scientists over the next year. How many additional senior reviewers are needed to stay within the guidance after growth?

A) 2  B) 3  C) 4  D) 6

**Correct answer: C) 4.**
**Explanation:** After growth: 14 + 10 = 24 delivery data scientists. Guidance requires at least 24 ÷ 3 = 8 senior reviewers. Currently 4, so 8 − 4 = 4 additional reviewers are needed. Distractor A (2) comes from using the pre-growth headcount (14 ÷ 3 = 4.67 → 5, minus 4 = 1, or similar partial reasoning), and B (3) from arithmetic slips like 24 ÷ 3 = 7. Note the real-world reading: growth bids that fund only delivery posts quietly break quality ratios — a lead who supervises junior analysts and sets coding standards should cost the senior review capacity into every growth proposal.

**Question 8 (hard) — Interpreting a performance table.**
A quarterly dashboard for your directorate's three data science products shows:

| Product | Users (Q1) | Users (Q2) | Cost per quarter | Decisions supported (Q2) |
|---|---|---|---|---|
| Forecast tool | 1,200 | 1,500 | £90,000 | 4,500 |
| Triage model | 800 | 1,000 | £120,000 | 10,000 |
| Text classifier | 2,000 | 1,800 | £60,000 | 3,600 |

Which product had the lowest cost per decision supported in Q2, and which had the highest percentage user growth?

A) Triage model lowest cost per decision; forecast tool highest growth
B) Text classifier lowest cost per decision; triage model highest growth
C) Triage model lowest cost per decision; triage model highest growth
D) Forecast tool lowest cost per decision; text classifier highest growth

**Correct answer: C).**
**Explanation:** Cost per decision: forecast tool £90,000 ÷ 4,500 = £20; triage model £120,000 ÷ 10,000 = £12; text classifier £60,000 ÷ 3,600 = £16.67. Lowest is the triage model at £12, which immediately eliminates options B and D. User growth: forecast tool (1,500 − 1,200) ÷ 1,200 = 25%; triage model (1,000 − 800) ÷ 800 = 25%; text classifier declined by 10%. The two growing products are tied at 25%, so the triage model is jointly highest — making option C's growth claim true, while option A's claim that the forecast tool is *the* highest is no stronger and pairs with nothing new. C is the only option in which both claims hold. Real dashboards produce ties and near-ties constantly; the tested skill is computing all the figures before eliminating options, rather than stopping at the first plausible row. Showing this arithmetic is exactly how you would evidence a challenge to delivery priorities: the most expensive product per quarter is simultaneously the cheapest per decision supported — unit economics beat headline costs.

**Question 9 (hard) — Sampling and confidence reasoning.**
You plan user research for a new dashboard, aiming to establish user needs across 5,000 caseworkers. A colleague proposes surveying 50 caseworkers from the London office (which has 500 caseworkers) and scaling up the findings by multiplying by 100. Setting aside sampling error, what is the primary numerical flaw, and roughly what proportion of the workforce would actually be sampled?

A) The sample is 1% of the workforce and unrepresentative because it is drawn from one office containing 10% of caseworkers
B) The sample is 10% of the workforce and therefore adequate
C) The sample is 1% of the workforce, which is always too small for any survey
D) Multiplying by 100 is wrong because the multiplier should be 50

**Correct answer: A).**
**Explanation:** Sample proportion: 50 ÷ 5,000 = 1% of the workforce. The deeper flaw is representativeness: all 50 come from one office holding 500 ÷ 5,000 = 10% of caseworkers, so regional working patterns, caseload mixes, and demographics elsewhere are entirely unobserved — no multiplier fixes coverage bias. Option B miscalculates by dividing 50 by 500 (the office) instead of 5,000 (the population of interest). Option C overcorrects: 1% samples can be perfectly adequate if drawn representatively; sample size adequacy depends on variance and desired precision, not on percentage alone. Option D is arithmetic pedantry that misses the design flaw. This question mirrors your responsibility to champion user research and design processes to gather and establish user needs — and to critique statistical analyses before they mislead the organisation.

**Question 10 (moderate) — Pipeline throughput and scaling.**
Your scoring pipeline processes 1,500 records per minute. A new data-sharing agreement will add a source that increases daily volume from 1.8 million to 2.7 million records. The pipeline currently runs in a nightly window of 22:00 to 02:00. Will the new volume fit the window, and what is the minimum throughput needed if not?

A) Yes, it fits with about an hour to spare
B) No; minimum throughput needed is about 11,250 records per minute
C) No; minimum throughput needed is about 7,500 records per minute
D) Yes, it fits exactly

**Correct answer: B) No; minimum throughput needed is about 11,250 records per minute.**
**Explanation:** The window is 4 hours = 240 minutes. Required throughput for the new volume: 2,700,000 ÷ 240 = 11,250 records per minute — option B. Option C (7,500) is the throughput the *current* volume needs (1,800,000 ÷ 240), a classic distractor for anyone who divides the wrong volume. Notice also that the stated single-stream capacity of 1,500 records per minute yields only 1,500 × 240 = 360,000 records per night, well below even today's 1.8 million — so the pipeline must already run multiple parallel workers, and the real question for your data engineers is whether parallelism can scale 7.5 times (11,250 ÷ 1,500). A strong candidate does the required division first, then flags that the stated capacity cannot reproduce the status quo — exactly the sanity-checking you apply when working with data engineers to design and deliver scalable products.

**Question 11 (moderate) — Training investment per head.**
You have £42,000 CPD budget for a team of 12. Conference attendance costs £1,200 per person, a technical course £800 per person, and coaching accreditation £2,500 per person. You want every team member to attend one conference and one course, with the remainder funding coaching accreditations. How many accreditations can you fund?

A) 6  B) 7  C) 8  D) 9

**Correct answer: B) 7.**
**Explanation:** Universal provision: 12 × (£1,200 + £800) = 12 × £2,000 = £24,000. Remainder: £42,000 − £24,000 = £18,000. Accreditations: £18,000 ÷ £2,500 = 7.2, which funds 7 whole accreditations (you cannot fund 0.2 of one). The distractor 8 comes from rounding 7.2 up — a subtle but classic error when converting budget arithmetic into whole units of people. Directing CPD spend is literally in your role profile ("set the direction of CPD within your team"), and the divide-then-floor discipline applies to any per-person allocation you will ever present to a finance partner.

**Question 12 (hard) — Compound growth in demand.**
Requests for your team's analysis have grown 15% per quarter for the past year. This quarter the team received 320 requests. If growth continues at the same compound rate, roughly how many requests should you plan for in one year's time (four quarters), and what percentage increase does that represent over today?

A) About 512 requests; 60% increase  B) About 560 requests; 75% increase  C) About 512 requests; 75% increase  D) About 480 requests; 50% increase

**Correct answer: B) About 560 requests; 75% increase.**
**Explanation:** Compound growth: 320 × 1.15⁴. Compute stepwise: 1.15² = 1.3225; 1.3225² = 1.7490. So 320 × 1.749 ≈ 560 requests. The increase over today is 74.9% ≈ 75%. Distractor A uses simple (non-compound) growth: 4 × 15% = 60%, giving 320 × 1.6 = 512 — the single most common error with growth rates. The difference between 512 and 560 is roughly one additional analyst's quarterly workload, so compounding versus simple growth is not pedantry: it is the difference between a defensible workforce bid and an under-resourced team. When you challenge delivery plans and priorities, check whether growth assumptions are compounded correctly.

**Question 13 (hard) — Cost-benefit of a proposed product.**
A proposed anomaly-detection product would cost £250,000 to build and £80,000 per year to run. It is expected to flag errors currently costing the organisation £600,000 per year, catching 30% of that value in year one, and 50% per year thereafter. Using simple totals (no discounting), what is the cumulative net position at the end of year three?

A) −£40,000  B) +£290,000  C) +£540,000  D) +£110,000

**Correct answer: B) +£290,000.**
**Explanation:** Benefits: year 1 = 0.30 × £600,000 = £180,000; years 2 and 3 = 0.50 × £600,000 = £300,000 each. Total benefits = £180,000 + £300,000 + £300,000 = £780,000. Costs: £250,000 build + 3 × £80,000 running = £250,000 + £240,000 = £490,000. Net = £780,000 − £490,000 = +£290,000. The distractors punish incomplete accounting: +£540,000 forgets the running costs entirely (£780,000 − £250,000 + rounding of the build figure), +£110,000 applies the 30% catch rate to all three years (3 × £180,000 − £490,000 = £50,000, or nearby partial sums), and −£40,000 rewards stopping partway through the cost rows. The tested habit: lay out benefits and costs year by year in two rows, sum each row completely, then subtract once at the end. This is the arithmetic core of taking responsibility for delivering scalable data science products and establishing maintenance support — products carry running costs every year, not just a build cost, and business cases that omit them flatter themselves by exactly the margins these distractors represent.

**Question 14 (moderate) — Reading a confusion-adjacent claim.**
A board paper claims: "The model is 92% accurate, so only 8% of the fraud cases it clears are actually fraudulent." The underlying figures: 10,000 cases, of which 400 are genuinely fraudulent; the model flags 500 cases, including 320 of the genuine ones. What is the true rate of fraud among cases the model *clears* (does not flag)?

A) 8%  B) About 0.8%  C) About 3.4%  D) 20%

**Correct answer: B) About 0.8%.**
**Explanation:** Cases cleared = 10,000 − 500 = 9,500. Genuine fraud missed by the model = 400 − 320 = 80 cases, and all of these sit in the cleared pool. Fraud rate among cleared cases = 80 ÷ 9,500 ≈ 0.84%, so about 0.8%. The board paper's claim confuses overall accuracy (92%) with the miss rate among cleared cases — two unrelated quantities; "100% minus accuracy" is not the probability that a cleared case is fraudulent. Distractor D (20%) is a different, real quantity — the share of genuine fraud cases the model misses (80 ÷ 400) — which answers "how much fraud escapes?" rather than the question asked. Distractor C (3.4%) mixes flagged-pool arithmetic into the cleared pool, and A simply repeats the paper's error. Work from a two-by-two table of counts every time: flagged/cleared against fraud/not-fraud, then read the requested cell against the requested denominator. Base-rate confusions of exactly this kind reach real boards in real papers, and catching them — politely, with the corrected arithmetic — is one of the highest-value things a lead data scientist does when using model outputs to produce evidence for services and policies.

### Preparation tips

- **Rebuild the classics until they are reflexes.** Percentage change, weighted average, compound growth, unit cost, break-even, and FTE arithmetic cover most numeric questions at this level. Ten minutes daily with your own team's real figures for two weeks will make the test format feel routine.
- **Say the denominator out loud.** Most numeric errors at senior level are denominator errors: dividing by the new value instead of the baseline, by one office instead of the whole population, by flagged cases instead of genuine cases. Before dividing, name what the answer is "out of".
- **Watch units and qualifiers.** "In thousands", "per quarter", "FTE", "per worker" — misreading a scale qualifier is the most common cause of confidently wrong answers, according to the assessment literature and every reviewer's experience.
- **Estimate before you calculate.** A rough order-of-magnitude estimate catches keying errors instantly. If your estimate says "about 550" and your calculator says 5,596, you mistyped.
- **Use the calculator for arithmetic, not for thinking.** Set up the calculation completely on paper or in your head first; the calculator's only job is the final multiplication or division.
- **Practise under time pressure deliberately.** Give yourself 60–75 seconds per question in your final practice sessions. As a lead you already have the maths; the skill under test is composure and extraction speed.

### Common pitfalls

- **Misreading chart and table labels** — confusing quarterly with annual data, Q1 with Q2 columns, or ignoring "in thousands". Slow down for five seconds on every table header; it repays itself many times over.
- **Simple versus compound growth** — applying 15% × 4 instead of 1.15⁴. Any multi-period growth question should trigger the compound check.
- **Unweighted averages** — averaging percentages across groups of very different sizes. Always weight by volume.
- **Over-calculating** — computing exact figures when the options are far apart and an estimate settles it. If options are 25%, 40%, 62.5% and 80%, one rough division decides.
- **Time-sink questions** — a single multi-stage cost-benefit question can consume five minutes. Flag it, answer the quick percentage questions, and return.
- **Swapping precision and recall** — or any pair of directional metrics. Anchor each metric to its denominator before answering.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment evaluates how accurately you understand, analyse, and draw conclusions from written material of the kind your role genuinely demands. For a lead data scientist in UK government, that means data ethics frameworks, statistical governance guidance, data-sharing agreements, service standards, board papers, and carefully worded emails from stakeholders. The core discipline is answering based strictly on the text provided — setting aside your own expert knowledge, however extensive — and distinguishing what a passage states, what it implies, and what it simply does not address.

The dominant format presents a dense passage followed by statements you must classify as **True** (the passage supports it), **False** (the passage contradicts it), or **Cannot Say** (the passage provides insufficient information either way). Multiple-choice comprehension questions — "which statement best summarises...", "what does the author assume..." — are also common. Timing is tight by design: typically less than a minute per question, simulating the reality of reading a governance paper minutes before the meeting that discusses it.

For your role, this assessment carries particular weight. You oversee compliance with data ethics standards and legislation — work that turns on the precise wording of frameworks and statute-adjacent guidance. You communicate and present effectively to non-specialists, which requires knowing exactly what a document licenses you to claim. And you critique statistical analyses, where the gap between "the data shows X" and "the data is consistent with X" is precisely the gap verbal reasoning tests probe. A lead who reads loosely signs off loosely.

One caution specific to experienced specialists: your subject knowledge is the main hazard here. You know how UK GDPR breach reporting works, what the Data Ethics Framework requires, and what retrieval-augmented systems can do — and the test will happily punish you for answering from that knowledge instead of from the passage. Treat every passage as a self-contained world whose rules may differ from the ones you know, and you will avoid the most common failure mode for senior candidates.

### What it measures for your role

- **Data ethics and privacy** — passages drawn from ethics frameworks and data-protection guidance test whether you can extract obligations, exemptions, and conditions exactly as written, reflecting your accountability for overseeing compliance and continuously improving an ethical framework.
- **Applied maths, statistics and scientific practices** — passages summarising statistical findings test whether you can separate supported conclusions from over-claims, the reading half of critiquing statistical analyses.
- **Delivering business impact** and **Understanding product delivery** — passages from business cases, delivery plans, and service assessments test whether you extract commitments, dependencies, and caveats accurately before challenging or endorsing them.
- **Data science innovation** and **Developing data science capability** — passages about emerging techniques test careful reading of claims about what a method can and cannot do, mirroring how you keep up to date with industry changes and match them honestly to organisational opportunities.
- **Programming and build (data science)** — passages from standards and open-source policies test rule extraction of the kind you perform when setting coding standards for your team.

### Practice questions

**Passage A (for Questions 1–4).**
"The department's data ethics framework requires that any new data science project completes an ethics self-assessment before development begins. Projects classified as high risk — defined as those processing special category data, those producing outputs that directly affect individuals, or those using novel techniques not previously deployed in the department — must additionally be reviewed by the Data Ethics Committee. The Committee meets monthly and aims to return decisions within ten working days of a meeting. Self-assessments are valid for twelve months, after which projects still in development must resubmit. The framework does not apply to projects that exclusively use synthetic data, although teams are encouraged to complete a self-assessment voluntarily in such cases."

**Question 1 (easy).** True, False, or Cannot Say: "A project using special category data must be reviewed by the Data Ethics Committee."

**Correct answer: True.**
**Explanation:** The passage defines high risk to include "those processing special category data", and states high-risk projects "must additionally be reviewed by the Data Ethics Committee". The chain is explicit: special category data → high risk → Committee review. No interpretation is needed; the answer follows from the two quoted clauses read together.

**Question 2 (moderate).** True, False, or Cannot Say: "The Data Ethics Committee returns its decisions within ten working days of a meeting."

**Correct answer: Cannot Say.**
**Explanation:** The passage says the Committee "aims to return decisions within ten working days". The statement as worded asserts that it *does* return decisions within ten working days — a claim of fact the passage neither confirms nor denies, because an aim is not an outcome. The passage gives no information about whether the aim is actually met, so the correct classification is Cannot Say rather than True (which would require evidence the aim is achieved) or False (which would require evidence it is missed). This distinction — aspiration versus achievement — is among the most frequently tested in verbal reasoning, and among the most important in your professional reading: a delivery plan that "aims to" retrain quarterly has promised nothing measurable. Whenever you see aims, seeks, intends, or expects in a passage, watch for a statement that quietly upgrades it to fact.

**Question 3 (moderate).** True, False, or Cannot Say: "A project using exclusively synthetic data is not required to complete an ethics self-assessment."

**Correct answer: True.**
**Explanation:** The passage states "The framework does not apply to projects that exclusively use synthetic data". Since the self-assessment requirement is part of the framework, a project outside the framework's scope is not required to complete one. The encouragement to do so "voluntarily" reinforces this: voluntary means not required. Note the precision trap in reverse — a hasty reader who remembers "teams are encouraged to complete a self-assessment" might answer False, converting encouragement into obligation. Obligation language (must, required) and encouragement language (should consider, encouraged) carry exactly the weight they state, in assessments as in the ethics frameworks you maintain.

**Question 4 (hard).** True, False, or Cannot Say: "A low-risk project that has been in development for fourteen months without resubmitting its self-assessment is in breach of the framework."

**Correct answer: True.**
**Explanation:** The passage states "Self-assessments are valid for twelve months, after which projects still in development must resubmit." This clause is not limited to high-risk projects — it applies to any project with a self-assessment, and all projects within the framework's scope must have one. Fourteen months exceeds twelve; the project is "still in development"; therefore resubmission was required and has not happened. The tempting answer is Cannot Say, on the theory that the passage does not use the word "breach" — but failing to do something the framework says you "must" do is what being in breach means, and assessments expect that much ordinary-language inference. The skill is calibrating inference: refuse to infer facts the passage doesn't state (Question 2), but do apply the plain meaning of the words it does state.

**Passage B (for Questions 5–8).**
"The evaluation compared the new triage model against the existing rules-based system across 12,000 historical cases. The model correctly prioritised 78% of urgent cases, compared with 71% for the rules-based system. However, performance varied by region: in two of the nine regions, the model performed worse than the existing system. The evaluation team noted that these two regions had the highest proportions of cases with missing occupation data. The report recommends phased deployment beginning in the seven regions where the model outperformed the baseline, alongside a data quality improvement programme, and states that a causal link between missing occupation data and reduced model performance has not been established."

**Question 5 (easy).** True, False, or Cannot Say: "The new model correctly prioritised a higher percentage of urgent cases than the rules-based system overall."

**Correct answer: True.**
**Explanation:** Directly stated: 78% versus 71% overall. The word "overall" in the statement matches the passage's headline comparison before the regional breakdown. This is a straightforward retrieval question — assessments include them early in a passage set to reward candidates who read the actual numbers rather than skimming.

**Question 6 (moderate).** True, False, or Cannot Say: "Missing occupation data caused the model's reduced performance in two regions."

**Correct answer: False.**
**Explanation:** The passage explicitly states "a causal link between missing occupation data and reduced model performance has not been established." The statement asserts causation; the passage says causation has not been established — a direct contradiction, making this False rather than Cannot Say. Notice the fine structure: the passage *does* report an association (the two underperforming regions had the highest proportions of missing data), and a careless reader converts association into causation — the exact error you correct in others' analyses. Where a passage explicitly disavows a causal claim, a statement asserting that cause is False; had the passage merely stayed silent on causation, the answer would have been Cannot Say. This question rewards the same discipline as your applied statistics skill: correlation language and causation language are different claims requiring different evidence.

**Question 7 (moderate).** True, False, or Cannot Say: "The evaluation team recommends deploying the model in all nine regions once the data quality programme is complete."

**Correct answer: Cannot Say.**
**Explanation:** The passage recommends "phased deployment beginning in the seven regions where the model outperformed the baseline, alongside a data quality improvement programme". It says nothing about what happens after the programme completes — full deployment in all nine regions is a plausible eventual intention, but the passage does not state it. "Beginning in" implies more phases may follow, but where and under what conditions is unstated. Plausibility is not textual support: this is the single most important discipline in verbal reasoning, and in reading delivery plans — the difference between what a paper actually commits to and what a sympathetic reader assumes it means.

**Question 8 (hard).** Which of the following best summarises the report's overall position?

A) The model is superior to the rules-based system and should replace it immediately everywhere.
B) The model shows overall promise but regional weaknesses justify a phased approach combined with data quality work.
C) The model is unreliable because it failed in two regions and should not be deployed.
D) Missing occupation data must be fixed before any deployment can begin.

**Correct answer: B).**
**Explanation:** Option B captures every load-bearing element: overall outperformance (78% versus 71%), regional variation (two of nine regions worse), the phased deployment recommendation, and the parallel data quality programme. Option A overstates — the report explicitly recommends phased, not immediate universal, deployment. Option C overweights the two regions against the overall gain and the recommendation to proceed. Option D inverts the report's sequencing: deployment begins alongside the data quality programme, not after it. Best-summary questions are won by elimination: strike every option containing a claim the passage contradicts or does not make, and one survivor remains. This mirrors drafting executive summaries of your team's evaluations — the summary must carry the caveats, not just the headline.

**Passage C (for Questions 9–11).**
"Under the memorandum of understanding, the partner agency will supply pseudonymised case records monthly, for the sole purpose of developing and evaluating the demand forecasting model. Records must be deleted within ninety days of receipt unless a written extension is agreed. Any output derived from the data may be published only in aggregate form, with cell counts below ten suppressed. The agreement permits linkage to the department's internal reference data, but expressly prohibits linkage to any commercially sourced dataset. Breaches must be reported to both parties' data protection officers within seventy-two hours of discovery. This agreement does not confer any right to use the data for operational decision making about individual cases."

**Question 9 (easy).** True, False, or Cannot Say: "The supplied records may be linked to commercially sourced datasets if the results are published only in aggregate."

**Correct answer: False.**
**Explanation:** The agreement "expressly prohibits linkage to any commercially sourced dataset". The prohibition is unconditional — aggregate publication is a separate rule governing outputs, not an exemption to the linkage prohibition. Statements like this test whether you let one clause (aggregate publication is allowed) soften another (linkage is prohibited); in legal-style documents, each clause binds independently unless one explicitly refers to the other. You apply this reading discipline every time you oversee a data sharing arrangement — and the assessment format simply compresses it.

**Question 10 (moderate).** True, False, or Cannot Say: "Using the forecasting model's data to inform a caseworker's decision on an individual case would fall outside what the agreement permits."

**Correct answer: True.**
**Explanation:** The final sentence states the agreement "does not confer any right to use the data for operational decision making about individual cases". Informing a caseworker's decision on an individual case is operational decision making about an individual case; the agreement grants no right to do it, and the stated sole purpose is "developing and evaluating the demand forecasting model". Both clauses point the same way, so the statement is supported by the text. The subtlety is that the passage says the agreement doesn't confer the right, rather than "is prohibited" — but the statement is carefully worded to match: "outside what the agreement permits" is exactly what "does not confer any right" means. Precision in both directions — neither over-reading nor under-reading — is the tested skill.

**Question 11 (hard).** True, False, or Cannot Say: "A breach discovered on a Friday afternoon must be reported by Monday afternoon."

**Correct answer: True.**
**Explanation:** The agreement requires breaches to be reported "within seventy-two hours of discovery". Seventy-two hours from Friday afternoon is Monday afternoon — the clock runs in hours, and nothing in the passage says working hours or business days. A reader who mentally substitutes "three working days" would answer Cannot Say or False, importing a convention the text does not contain; hour-based breach-reporting clocks (as in UK GDPR's seventy-two-hour standard) run through weekends precisely because the text says hours. The general lesson for both assessments and practice: take units literally. When a document you oversee means working days, it must say working days — and when you improve your organisation's ethical framework, this is the drafting precision you enforce.

**Passage D (for Questions 12–13).**
"Recent advances in large language models have prompted several departments to trial retrieval-augmented approaches for answering staff policy queries. Early evaluations suggest such systems can reduce simple query resolution times, though accuracy varies with the quality of the underlying document corpus. The Central Digital and Data Office guidance emphasises that generative systems should not be the sole basis for decisions affecting individuals, and that departments remain responsible for outputs regardless of the technology used. Several trials also report that maintenance effort was underestimated, with corpus curation demanding ongoing analyst time comparable to a small operational service."

**Question 12 (moderate).** True, False, or Cannot Say: "Retrieval-augmented systems reduce query resolution times."

**Correct answer: Cannot Say.**
**Explanation:** The passage says early evaluations "suggest such systems *can* reduce *simple* query resolution times". The statement strips three hedges at once: "suggest" (tentative evidence, not established fact), "can" (capability in some conditions, not a general effect), and "simple" (a subset of queries, not all queries). What remains is a stronger, more general claim than the passage supports — but the passage does not contradict it either, so the classification is Cannot Say rather than False. Counting the hedges is a practical technique: each one the statement drops moves it further from "True". As the leader who talks confidently about the benefits of data science approaches to existing and potential customers, you live on the right side of this line daily — the credible version of the claim keeps the hedges.

**Question 13 (moderate).** According to the passage, which of the following does the guidance from the Central Digital and Data Office state?

A) Generative systems must never be used for staff policy queries.
B) Departments are responsible for outputs regardless of the technology used.
C) Corpus curation requires a dedicated operational team.
D) Retrieval-augmented systems are more accurate than human advisers.

**Correct answer: B).**
**Explanation:** The passage attributes exactly two points to the guidance: generative systems "should not be the sole basis for decisions affecting individuals", and "departments remain responsible for outputs regardless of the technology used". Option B restates the second point. Option A distorts the first — "should not be the sole basis" is a constraint on reliance, not a ban. Option C garbles a different sentence: the maintenance observation comes from the trials, not the guidance, and says effort was "comparable to a small operational service", not that a dedicated team is required. Option D appears nowhere. Attribution questions test whether you track *who said what* — a skill you exercise whenever you brief upwards on what standards require versus what early evidence merely suggests.

**Passage E (for Questions 14–15).**
"Following the service assessment, the panel concluded that the forecasting product met the Service Standard at beta, subject to two conditions. First, the team must publish its model documentation, including known limitations, before public beta begins. Second, the team must demonstrate that assisted-digital users can access equivalent outcomes through the telephone channel. The panel commended the team's open-source publication of its codebase, noting that two other departments had already reused components. The panel expressed concern that the product's benefits case relied on staff-time savings that had not yet been independently verified, and recommended — but did not require — an independent benefits review within six months."

**Question 14 (moderate).** True, False, or Cannot Say: "The team is required to complete an independent benefits review within six months."

**Correct answer: False.**
**Explanation:** The passage draws the distinction itself: the panel "recommended — but did not require — an independent benefits review". The statement asserts a requirement; the passage explicitly states there is none, which contradicts the statement and makes it False rather than Cannot Say. Contrast the two genuine conditions, which use "must": publishing model documentation and demonstrating assisted-digital access. Assessments love documents that mix binding and non-binding language in one paragraph, because so do real governance papers — and as the person who leads teams through service assessments and delivery phases, tracking exactly which findings are conditions and which are advice determines your team's critical path.

**Question 15 (hard).** True, False, or Cannot Say: "The product's staff-time savings have been overstated."

**Correct answer: Cannot Say.**
**Explanation:** The passage says the savings "had not yet been independently verified" and that the panel "expressed concern" about the benefits case relying on them. Unverified is not the same as overstated: the savings could be accurate, understated, or overstated — verification would tell, and it has not happened. The panel's concern signals risk, not a finding. A reader pattern-matching "concern about benefits" to "benefits are inflated" imports a conclusion the text withholds; equally, the passage gives no evidence the savings are accurate, so True is unavailable too. This is the same epistemics you enforce when critiquing analyses: absence of verification is a statement about evidence, not about the underlying quantity. Holding that line under time pressure — in an assessment or a benefits board — is precisely what this format measures.

**Question 16 (moderate).** Based on Passage E, which of the following must happen before public beta begins?

A) An independent benefits review and publication of model documentation.
B) Publication of model documentation including known limitations.
C) Reuse of the codebase by at least two other departments.
D) Independent verification of staff-time savings.

**Correct answer: B).**
**Explanation:** The passage attaches an explicit timing requirement to exactly one item: the team "must publish its model documentation, including known limitations, before public beta begins". The second condition (assisted-digital access via telephone) is binding but carries no stated deadline relative to public beta — the passage requires the team to "demonstrate" it as a condition of the assessment outcome, without saying when. Option A smuggles in the benefits review, which was recommended, not required. Option C describes something that has already happened (two departments had already reused components) and was never a condition. Option D was the subject of concern, not a requirement. The tested skill is binding-plus-deadline extraction: in a single paragraph, separate what is mandatory from what is advisory, and then separate what is mandatory-by-a-date from what is merely mandatory. That is exactly the reading you perform on assessment reports before telling your team what their critical path actually is — and misreading it in either direction wastes a sprint or fails a gate.

### Preparation tips

- **Train the "text only" reflex.** Your expertise is an asset everywhere except here: the test rewards answering from the passage alone. In practice sessions, physically point at the sentence that justifies each answer; if you cannot point at one, the answer is probably Cannot Say.
- **Learn the hedge lexicon.** Aims, suggests, can, may, some, expects, is intended to — versus will, does, must, all, requires. Most True/False/Cannot Say questions turn on whether the statement preserves or upgrades the passage's hedging.
- **Read the statement before rereading the passage.** Skim the passage once for structure, then let each statement send you back to the specific clause it tests. Scanning for keywords beats rereading the whole text — you have less than a minute per question.
- **Practise on your own documents.** Take a data-sharing agreement, an ethics framework, or a service assessment report and write five True/False/Cannot Say statements about it. Composing the statements teaches you the traps faster than answering them.
- **Respect the difference between False and Cannot Say.** False requires the passage to contradict the statement; absence of support is Cannot Say. When unsure, ask: "could both the passage and this statement be true at once?" If yes, it is not False.

### Common pitfalls

- **Bringing outside knowledge.** You may know that UK GDPR mandates seventy-two-hour breach reporting or how the Data Ethics Framework works in your department; the question is only ever about the passage in front of you. Expertise-driven assumptions are the most common failure mode for senior specialists.
- **Converting association to causation.** Passages about analyses often report correlations; statements assert causes. Unless the passage asserts the cause, the answer is Cannot Say — or False where the passage explicitly disavows it.
- **Treating "likely" outcomes as facts.** A passage saying a phased rollout is "expected to complete by March" does not support "the rollout will complete by March".
- **Softening prohibitions with nearby permissions.** Clauses bind independently; an aggregate-publication permission does not dilute a linkage prohibition.
- **Poor time discipline.** Dense passages tempt full, careful reading of every word before any question. Structure-skim first, then verify clause by clause; spending three minutes mastering a passage you get one question about is a losing trade.
- **Second-guessing verbatim wording.** If a statement is nearly identical to a passage sentence but swaps "should" for "must" or drops "simple", the swap is the question. Assessment writers change one word at a time on purpose.

## Workplace job-specific situational judgement assessment

### About this assessment

A workplace job-specific situational judgement assessment evaluates decision-making, interpersonal skill, and professional conduct through realistic workplace dilemmas. Unlike the previous three assessments, there is usually no single objectively right answer: several responses may seem reasonable, and the test measures how well your behavioural choices align with the values of the organisation and the demands of the role. For UK public sector digital and data roles, those values are explicit: meeting user needs, transparency, collaboration, accessibility and inclusion, evidence-based decision making, and the Civil Service values of integrity, honesty, objectivity, and impartiality.

Typical formats present a scenario followed by four or five possible actions. You may be asked to pick the **most effective** and **least effective** actions, to **rank** all options from best to worst, or to **rate** each option's effectiveness independently. Timing is generous or absent — the test measures judgement, not speed.

For a lead data scientist, the scenarios will be leadership scenarios. Expect dilemmas about: pressure to overstate findings; ethical concerns raised mid-delivery; conflict within your team; coaching underperformers; competing stakeholder demands; deciding when to challenge and when to deliver; and balancing innovation against operational reliability. Your role profile is unusually rich in exactly the behaviours these tests probe — you are a "leader, coach, and champion of data science" who must "navigate ethical and data challenges", "challenge delivery plans and priorities", "influence others", and "act as a coach, inspiring curiosity and creativity in others". Situational judgement is arguably the assessment most aligned with what distinguishes a lead from a senior practitioner: the technical answer is rarely the hard part; the human and institutional path to it is.

### What it measures for your role

- **Data ethics and privacy** — dilemmas where delivery pressure, stakeholder enthusiasm, or ambiguity collide with your duty to oversee compliance and build a data ethics culture, influencing others to act on it.
- **Developing data science capability** — scenarios about coaching, delegation, underperformance, and growing others, reflecting your responsibility to help colleagues develop skills and set the direction of CPD.
- **Delivering business impact** — dilemmas about championing data science credibly: when to promise, when to caveat, and how to handle products after launch, including establishing maintenance support.
- **Understanding product delivery** — scenarios about phase gates, priorities, and working with product managers to influence the direction of work.
- **Data science innovation** — dilemmas balancing curiosity and improvement against delivery obligations and operational risk, reflecting "challenge the status quo and always look for ways to improve data science".
- **Applied maths, statistics and scientific practices** — scenarios where statistical integrity is under social pressure, testing whether you protect objectivity while maintaining relationships.

### Practice questions

**Question 1 (moderate) — Pressure to overstate results.**
Your team's evaluation shows the new prioritisation model improves outcomes by 4%, with meaningful uncertainty (the plausible range includes 1%). A senior stakeholder drafting the programme board paper writes that the model "delivers a 4% improvement, with further gains expected", and asks you to confirm the wording by 17:00 so the paper can go out. You believe the wording overstates the evidence. Rank these responses from most to least effective:

A) Confirm the wording; 4% is the central estimate and the board paper is not a statistical publication.
B) Reply proposing alternative wording that keeps the headline but adds the uncertainty range and removes "further gains expected", offering a call before 17:00 to agree it.
C) Refuse to confirm and escalate to the board chair that the paper misrepresents analysis.
D) Confirm the wording but note your concerns in an email to your own line manager for the record.

**Correct ranking: B, C, D, A.**
**Explanation:** B is the strongest because it solves the actual problem — inaccurate wording — while respecting the stakeholder's deadline and relationship: you offer a concrete alternative and a synchronous route to agreement, which is how influence works at lead level. It protects objectivity (a Civil Service value) and models the transparency your ethics responsibilities demand. C protects integrity but at unnecessary cost: escalation before attempting direct resolution damages the relationship and casts you as an obstacle rather than an adviser; it becomes appropriate only if B fails. D is worse than C on substance: the misleading wording still reaches the board, and the covering email protects you rather than the decision — a defensive move that fails your accountability for how model outputs are used as evidence. A is least effective: "not a statistical publication" is precisely the wrong instinct, because boards act on the words in front of them, and "further gains expected" is a claim with no evidential basis at all. Note the general pattern the strongest option shows: fix the problem at the source, offer alternatives rather than vetoes, and preserve both the evidence and the relationship.

**Question 2 (moderate) — Ethical concern raised mid-delivery.**
Two sprints before a planned private beta, a mid-level data scientist on your team tells you privately that they believe one input feature acts as a proxy for ethnicity, and that the fairness analysis planned for beta "feels like it's happening too late". The product manager wants no scope changes this close to the gate. Select the MOST effective and LEAST effective responses:

A) Thank them, and ask them to write up the concern; commission a rapid proxy analysis on the existing validation data before the gate, and tell the product manager the gate decision will include its results.
B) Reassure them that the beta fairness analysis will catch any real problem, and that beta is exactly the controlled environment for finding such issues.
C) Remove the feature immediately to be safe, absorbing the retraining cost and accepting the gate may slip.
D) Ask them to raise it at the next retrospective so the whole team can discuss the lesson for future projects.

**Most effective: A. Least effective: D.**
**Explanation:** A does four things at once: it validates the person who raised a concern (essential for the data ethics culture you are charged with building — people stop raising concerns that disappear into silence); it converts a feeling into evidence quickly and proportionately (a rapid proxy analysis on existing data costs days, not sprints); it keeps the product manager's gate intact while making it an informed gate; and it retains your options — remove the feature, mitigate, or proceed with documented justification, depending on what the analysis shows. B is weak: it defers an equalities risk to an environment where real users are affected — beta users are still citizens, and "we planned to check later" is not a defence the department could offer publicly. C has integrity but poor judgement: acting before evidence, it may remove a legitimate feature, harm model performance for the very groups you aim to protect, and teaches the team that concerns trigger panic rather than analysis. D is least effective because it reclassifies a live, potentially unlawful risk as a process-improvement topic weeks away: it neither investigates nor decides, and signals that ethics is retrospective paperwork. The public sector framing matters: transparency and inclusion are met by A's "gate decision includes the evidence", not by C's silent removal or B's hopeful deferral.

**Question 3 (hard) — Underperforming senior team member.**
A senior data scientist on your team — technically excellent, previously your peer — has for two months delivered late, skipped code reviews they were assigned, and been short with the apprentice in stand-ups. The apprentice has started staying silent. Other team members are quietly redistributing the senior's review load. Rank these responses from most to least effective:

A) Hold a private one-to-one this week: describe the specific behaviours and their impact on the team, ask what is going on, and agree expectations and support with a follow-up date.
B) Redistribute the review load formally so the team is protected, and monitor for another month before acting further.
C) Raise the pattern with HR to begin a formal performance process, given the duration and the impact on a junior colleague.
D) Address it obliquely at the team retrospective by discussing review-load fairness and stand-up behaviour as team-wide themes.

**Correct ranking: A, C, B, D.**
**Explanation:** A is the textbook and genuinely best first move: specific behaviours, described privately, with curiosity before consequences — two months of decline in a previously strong performer usually has a cause (health, workload, home, disengagement), and a leader's first duty is to find out while making expectations unambiguous. The follow-up date converts a chat into an agreement. C is second, not because it should happen first, but because it is a legitimate next step if A produces no change — and materially better than doing nothing, given a junior colleague is already being harmed; an assessment penalises leaders who let kindness to one person outweigh duty to the most vulnerable person in the room. B protects the team's throughput but is passive on the cause: it institutionalises the problem, rewards the silent redistribution, and delays the conversation another month while the apprentice's silence deepens. D is least effective and a classic trap option: oblique, whole-team messages about one person's behaviour are cowardice dressed as facilitation — the senior may not recognise themselves, the rest of the team resents the generalised criticism, and the apprentice learns that problems are managed by hints. Your role profile makes you a coach; coaching starts with honest, private, specific conversation.

**Question 4 (moderate) — Competing stakeholder demands.**
Two directors each believe their work is your team's top priority. Director P's programme needs a demand forecast refresh for a funding submission in three weeks. Director Q expects the promised discovery work for a new triage product to start Monday, with a user researcher already booked. Your team can fully staff only one. Select the MOST effective and LEAST effective responses:

A) Staff the forecast refresh, as funding submissions are hard deadlines, and quietly postpone the discovery start, telling Director Q's team the researcher booking fell through.
B) Assess both pieces of work against organisational priorities, then convene the two directors (or their delegates) with a recommendation and the capacity evidence, asking them to confirm or adjust the trade-off.
C) Split the team across both so each director sees progress.
D) Escalate to your own director to decide, providing a neutral summary of both demands.

**Most effective: B. Least effective: A.**
**Explanation:** B treats prioritisation as what it is at lead level: an evidence-based, transparent trade-off owned by the people accountable for the outcomes. Bringing a recommendation (not just a problem) with capacity arithmetic demonstrates the challenge-and-communicate behaviours in your role profile, and letting the directors confirm keeps the decision at the right altitude without dumping it upwards. D is defensible but weaker than B: it moves the decision up a level before testing whether the stakeholders can resolve it with evidence — escalation as a first resort spends your credibility and slows everyone. C is the classic weak option dressed as fairness: half-staffing both likely fails both, and discovery with a booked user researcher is particularly damaged by partial attention; assessments consistently punish split-the-difference options that avoid the underlying choice. A is least effective for one decisive reason: the lie. Whatever the prioritisation merits, telling Director Q's team a booking "fell through" is dishonest — it violates the Civil Service value of honesty outright, and when it surfaces (it will; the researcher knows the truth) it poisons your standing as a champion of the profession. In situational judgement tests, any option containing deception is almost always the least effective, regardless of how sensible its logistics are.

**Question 5 (hard) — Innovation versus operational reliability.**
Your team runs a stable, well-understood forecasting model that the operations centre relies on daily. A talented data scientist has built a prototype using a newer architecture that improves accuracy 9% in offline tests and is eager to swap it in, arguing "we're a data science team, not a museum". The operations centre lead is wary after a previous failed change. Rank these responses from most to least effective:

A) Approve a shadow deployment: run the new model in parallel on live data without affecting operations, define success criteria and a review date with the operations lead, and celebrate the prototype at the team show-and-tell.
B) Decline the swap for now: the operations centre's trust matters more than 9%, and revisit next year.
C) Approve the swap with a rollback plan, since offline results are strong and the team's innovation culture needs visible wins.
D) Ask the data scientist to write a business case and present it to the architecture board before anything runs anywhere.

**Correct ranking: A, D, C, B.**
**Explanation:** A is the strong answer because it refuses the false choice between innovation and reliability: a shadow deployment generates live evidence at zero operational risk, the jointly defined success criteria and review date rebuild the operations lead's trust by giving them control, and the public celebration protects the innovator's motivation — the coach-and-champion combination your role profile describes. D is second: governance is legitimate, and for some architectures mandatory, but as a first and only step it converts energy into paperwork and delays evidence that a shadow run would gather anyway; it is the right companion to A, not a substitute. C is third: a straight swap with rollback mistakes offline metrics for operational readiness — rollback plans restore systems, not confidence, and a second failed change could set data science back years with this stakeholder. B is last, though it sounds prudent: it teaches your most talented people that improvement is unwelcome, contradicts your responsibility to challenge the status quo, and confuses avoiding risk with managing it. Note the assessment pattern: the best options usually create information and preserve relationships simultaneously; the worst destroy one to protect the other.

**Question 6 (moderate) — A data breach discovered by your team.**
On Thursday evening, a junior analyst messages you: while debugging, they discovered that a shared analytical workspace has, for three weeks, been accessible to a wider group than the data sharing agreement for one dataset permits. There is no evidence anyone outside the permitted group accessed it, but access was possible. Select the MOST effective and LEAST effective responses:

A) Instruct the analyst to correct the permissions immediately, thank them, and note it in the next monthly risk report since no unauthorised access occurred.
B) Correct the permissions immediately, preserve the access logs, report the incident that evening to your data protection officer as a potential breach, and tell the analyst clearly they did the right thing by raising it.
C) Ask the analyst to establish definitively whether unauthorised access occurred before deciding whether to report anything.
D) Correct the permissions, then review at next week's team meeting how the misconfiguration happened.

**Most effective: B. Least effective: A.**
**Explanation:** B does everything the situation demands in the right order: stops the exposure, preserves the evidence an investigation needs, reports promptly to the people whose statutory job this is (breach-reporting clocks, typically seventy-two hours, run from discovery — Thursday evening counts), and reinforces the raising of bad news — the single most important cultural signal a leader can send, and central to the ethics culture your role requires you to build. C inverts the logic of breach handling: the reporting duty is triggered by the potential breach, and assessment of likelihood and severity belongs to the data protection officer, not to a junior analyst working alone; investigation and reporting run in parallel, not in sequence. D fixes the hole and learns the lesson but misses the legal duty entirely. A is least effective despite sounding proportionate: it makes the compliance call unilaterally ("no unauthorised access occurred" is an assumption, not a finding — access logs haven't been examined), buries a potential statutory notification in a monthly report, and quietly teaches the analyst that such discoveries are routine tidy-ups. Your accountability for overseeing compliance with data ethics standards and legislation means the least defensible move is deciding, without the designated experts, that the rules weren't engaged.

**Question 7 (moderate) — Coaching versus doing.**
A high-visibility ministerial request lands: a complex analysis needed in ten working days. You could do it yourself in four days to a standard you trust. Alternatively, a promising mid-level data scientist could lead it — developmentally ideal for them — but would need eight to nine days, your review time, and carries delivery risk. Rank these responses from most to least effective:

A) Do it yourself; ministerial requests are not training exercises, and the team can learn on lower-stakes work.
B) Give it to the mid-level data scientist with a structured safety net: agree a plan on day one, checkpoint reviews on days three and six, and your final review with two days' buffer.
C) Do the core analysis yourself but have the mid-level data scientist shadow you throughout, producing the annexes and attending your briefings.
D) Give it to the mid-level data scientist entirely, telling them you trust them and to shout if they need help — leaders must delegate outcomes, not tasks.

**Correct ranking: B, C, A, D.**
**Explanation:** B is delegation as your role profile means it — developing capability on real work while managing delivery risk explicitly: the day-one plan catches direction errors when they are cheap, the checkpoints replace hope with evidence, and the buffer makes the ministerial deadline safe even if the final review finds problems. C is a reasonable second: the deadline is very safe and some development occurs, but shadowing builds understanding, not capability — the mid-level scientist watches you lead rather than leading. A is third, not last, because it does deliver reliably; its cost is invisible and cumulative — a team whose lead absorbs all high-stakes work never develops, which your role profile treats as a core failure ("helping colleagues to develop skills", "building organisational capability"). D is least effective and deliberately tempting: it uses the vocabulary of empowerment to describe abdication. "Shout if you need help" transfers the burden of risk detection to the least experienced person in the arrangement, on a ministerial deadline, with no checkpoints; when juniors struggle, they characteristically go quiet rather than shout. Support structures are not distrust — they are what makes stretch assignments safe enough to give.

**Question 8 (hard) — Your model is being misused.**
Three months after your team delivered a demand-forecasting product with clear documentation that outputs are reliable only at regional level, you learn a service manager has been using it to set staffing for individual local offices — decisions affecting rosters and, downstream, service waiting times. The service manager is enthusiastic about the product and has praised your team publicly. Select the MOST effective and LEAST effective responses:

A) Contact the service manager directly: explain the local-level limitation and its consequences concretely, offer to explore whether a local-level version is feasible, and jointly review recent local decisions for material errors.
B) Ask the product manager to add a prominent warning to the product interface and update the documentation.
C) Say nothing for now; the manager is a crucial ally, the decisions are made anyway, and a local-level model is on your roadmap for next year.
D) Send a written notice to the manager's director stating the product is not approved for local-level use and that your team accepts no responsibility for decisions made on that basis.

**Most effective: A. Least effective: D.**
**Explanation:** A treats misuse as the shared problem it is: the direct conversation preserves an ally, the concrete explanation ("at local level, the forecast error exceeds the staffing differences you're acting on") converts a compliance message into a professional insight, the joint review addresses harm already done to service users, and the feasibility offer channels the manager's enthusiasm somewhere legitimate — user needs, transparency, and collaboration all at once. B is a genuinely good action but incomplete as the whole response: interface warnings prevent the next misuse; they neither engage the current decisions already made nor preserve the relationship — as a companion to A it is excellent, alone it is passive. C fails your core accountability: you know citizen-affecting decisions are resting on outputs the evidence does not support, and alliance-preservation is not a reason recognised by any value framework you operate under — post-launch, "ensuring products are monitored, maintained and continually improved" includes how they are used. D is least effective because it is liability management masquerading as governance: going over the manager's head first, in writing, converts an ally into an adversary, humiliates someone who publicly championed your work, and prioritises your team's protection over the service users affected — while doing nothing to review or correct the decisions already made. The strongest leaders run towards misuse of their products, because every misuse is unmet demand in disguise.

**Question 9 (moderate) — Capability gap in your own plan.**
Mid-way through planning next year's roadmap, you realise it depends heavily on natural language processing work, but your team's NLP experience is thin: one person has moderate experience, and your own is dated. The roadmap is due to your director in two weeks and is otherwise strong. Rank these responses from most to least effective:

A) Submit the roadmap as drafted; capability will develop through doing the work, which is how teams grow.
B) Submit the roadmap with the capability gap named, alongside a costed development plan: training, a targeted hire or secondment, delivery phasing that starts with the least NLP-intensive products, and a partnership with another department's established NLP team.
C) Reshape the roadmap around the team's current strengths, moving the NLP-dependent work to the following year.
D) Keep the roadmap but privately begin recruiting an NLP specialist so the gap is closing by the time delivery starts.

**Correct ranking: B, D, C, A.**
**Explanation:** B is what setting the direction of CPD and building organisational capability look like in practice: the gap is disclosed (transparency with your director, who is entitled to see the risk), and the plan converts it into a funded, phased, multi-route response — training plus hiring plus partnership is far more robust than any single route, and sequencing delivery from least to most NLP-intensive turns the roadmap itself into a development vehicle. D shows initiative but hides the risk from the person accountable for accepting it; a director who later discovers the roadmap was submitted with a known, unnamed capability gap has learned something about your candour that no successful hire repairs. C is honest but timid: it optimises for comfort over organisational need — if the NLP work matters, deferring it a full year cedes the opportunity, and matching new developments in data science to opportunities in your organisation is precisely your role's innovation remit. A is least effective: "we'll learn by doing" without any named risk, plan, or support is optimism substituting for leadership, and the failure mode — an overcommitted team learning a hard discipline on deadline — lands on the same junior staff you are meant to be developing.

**Question 10 (hard) — Open-sourcing under pressure.**
Your department has committed publicly to "coding in the open". A central transparency team asks you to open-source your team's fraud-detection scoring code within a month. You support open source in principle — you have set team standards for it — but this codebase includes feature logic that could help sophisticated actors game the detection system, and parts were written under old standards with hard-coded configuration you have not fully audited. Select the MOST effective and LEAST effective responses:

A) Decline: fraud detection is inherently sensitive, and open-sourcing any of it creates gaming risk that outweighs a transparency commitment.
B) Agree a scoped release with the transparency team: publish the pipeline, data preparation, and evaluation code after a security and credentials audit, withhold the specific detection features on documented gaming-risk grounds, and publish the reasoning for the partial release.
C) Comply in full within the month; the public commitment was made at departmental level and it is not your place to relitigate it.
D) Ask for a six-month delay so the code can be fully rewritten to current standards before any release.

**Most effective: B. Least effective: C.**
**Explanation:** B is the mature reading of "open where appropriate" — the standard your own role profile sets ("seek to make code open source where appropriate"). It honours the transparency commitment substantively (most of the codebase, plus published reasoning for what is withheld, which is itself transparency), manages the genuine gaming risk with a documented, reviewable justification rather than a blanket refusal, and deals with the credential/configuration audit before anything ships — the non-negotiable step. A is too blunt: "inherently sensitive" proves too much, would exempt entire classes of government code from a public commitment, and ignores that pipeline and evaluation code carries little gaming risk while offering real reuse value to other departments. D substitutes engineering perfectionism for judgement: the risk requiring delay is the audit, which takes weeks, not a rewrite taking six months; delay without a differentiated plan reads as resistance. C is least effective despite its apparent deference: releasing unaudited code with hard-coded configuration within a month risks exposing credentials and exploitable logic — an operational and security harm no transparency commitment intends — and "it is not my place" abandons exactly the judgement the organisation employs a lead data scientist to exercise. Public commitments are implemented by professionals who scope them safely, not by compliance that creates the next incident.

**Question 11 (moderate) — The uncomfortable evaluation result.**
Your team evaluated a flagship programme's pilot at the programme director's request. The results are disappointing: the pilot shows no measurable improvement, and the programme's expansion case assumed one. The director, who commissioned you precisely because your team is respected, asks whether the analysis could be "framed more constructively" for the investment committee. Rank these responses from most to least effective:

A) Present the results exactly as they are, and separately offer the director help developing options: what the data suggests about why the pilot underperformed and what could be tested next.
B) Reframe the summary to emphasise the pilot's operational learning and describe the outcome data as "early and evolving".
C) Tell the director the results cannot change and suggest they present the analysis to the committee themselves.
D) Agree to include the director's contextual narrative alongside your unchanged analysis, provided the summary states plainly that no measurable improvement was found.

**Correct ranking: A, D, C, B.**
**Explanation:** A pairs unshakeable objectivity with genuine partnership — the analysis stands, and the director gets what they actually need, which is not a kinder number but a credible path forward; "no measurable improvement" plus "here is what to test next" is a constructive framing that requires no distortion. D is a close second and in many real cases the practical settlement: decision-makers may legitimately add programme context around an analysis, and D's condition — the unambiguous headline finding — protects the committee's ability to decide on accurate evidence. C protects integrity but abandons the field: refusing to engage with presentation at all, and stepping away from the committee, leaves your unambiguous analysis to be summarised by someone with an incentive to soften it — objectivity without stewardship. B is least effective: "early and evolving" is wording chosen to make a null result sound like a positive trajectory, which is precisely the misrepresentation your role exists to prevent; an investment committee that later discovers the reframing will discount every analysis your team produces thereafter. The lead-level insight the ranking rewards: integrity and helpfulness are not in tension — the most effective option is almost always the one that keeps the evidence intact while solving the stakeholder's underlying problem.

**Question 12 (moderate) — Building capability across the organisation.**
A policy director tells you their analysts keep commissioning external consultants for basic predictive modelling because "your team is always booked". They ask you to fix it. Your team genuinely has no spare delivery capacity this quarter. Select the MOST effective and LEAST effective responses:

A) Offer a capability partnership: your team runs a monthly clinic and code-review surgery for their analysts, provides templates and standards, and takes on one joint project per quarter where their analysts deliver with your team's coaching.
B) Explain the capacity position and suggest they continue with consultants, but offer to review the consultants' outputs for quality.
C) Request funding for two more posts in your team so future commissions can be brought in-house.
D) Agree to take on their modelling work next quarter by deprioritising your existing roadmap, since duplicate external spend is worse than internal delay.

**Most effective: A. Least effective: B.**
**Explanation:** A is the only option that solves the actual problem, which is capability, not capacity: clinics, standards, templates, and coached joint delivery grow the policy team's own ability — turning "your team is always booked" from a bottleneck complaint into a distributed capability model. This is your role profile almost verbatim: "act as a leader or technical specialist... helping colleagues to develop skills", "talk confidently about the benefits of data science approaches to existing and potential customers", "building organisational capability". C addresses supply but slowly and fragilely — funding cycles take months, and centralising all modelling in one team recreates the bottleneck at a larger scale. D is generous but undisciplined: silently deprioritising a roadmap your director has agreed breaks commitments to other stakeholders and hides a resourcing problem instead of surfacing it. B is least effective because it institutionalises the failure: permanent consultant dependency for basic modelling, with your team as unpaid quality assurance — the costliest possible arrangement for the organisation, no capability growth, and a quiet abdication of your championing role. Note that B's reviewing offer makes it feel responsible; assessments frequently make the least effective option the politest one.

### Preparation tips

- **Anchor on the published values.** UK public sector situational judgement scenarios reward user needs, honesty, transparency, inclusion, evidence, and collaboration. When torn between options, ask which one you would be comfortable explaining publicly — to the National Audit Office, a select committee, or the person affected.
- **Look for the option that creates information.** At lead level, the strongest options usually generate evidence (a rapid analysis, a shadow deployment, a joint review) rather than forcing a premature yes/no. If an option converts a dispute into data, look hard at it.
- **Separate first moves from escalations.** Escalation, formal processes, and written notices are legitimate — as second steps after direct engagement fails. Options that skip the direct conversation usually rank below those that start with it.
- **Beware the deceptively kind option.** Reassurance without action, delay dressed as diligence, and politeness that entrenches a problem are classic "least effective" answers. Ask what each option actually changes.
- **Answer as the role, not as your current constraints.** Respond as a well-supported lead data scientist should, not as workarounds in your current organisation might force. The test measures your judgement, not your scar tissue.
- **Be consistent.** Rating formats reward a stable value hierarchy across scenarios: integrity above convenience, users above stakeholders' comfort, capability-building above heroics. Decide your hierarchy before the test; apply it evenly.

### Common pitfalls

- **Answering idealistically rather than effectively.** "Commission a full independent ethics review" sounds principled but may be wildly disproportionate to a permissions misconfiguration. Effective options are proportionate to the actual risk.
- **Selecting passive options.** Choices that delay action, hand the problem to someone else untouched, or address symptoms (redistributing review load) rather than causes (the conversation) consistently score poorly.
- **Ignoring the least-effective half.** In most/least formats, the least-effective choice carries equal marks. Options containing deception, unilateral compliance decisions, or harm to junior colleagues are usually the intended "least" — even when other options are also imperfect.
- **Choosing conflict avoidance dressed as diplomacy.** Oblique team-wide messages about one person, silence to preserve an alliance, and softened findings are recurring traps for senior candidates who have learned to value smooth relationships.
- **Forgetting your specific accountabilities.** As lead, you own ethics oversight, capability development, and the credibility of evidence. Options that would be acceptable for a mid-level data scientist ("flag it to my manager") can be weak for you, because you are the person things get flagged to.
- **Overcorrecting into harshness.** The strongest options pair standards with support: honest conversations with follow-up dates, declined requests with alternatives, withheld code with published reasoning. Firmness without a constructive offer usually ranks mid-table, not top.

## Conclusion

You have now worked through four substantial assessment types — cognitive, numeric reasoning, verbal reasoning, and situational judgement — every one of them grounded in the real work of a lead data scientist in UK government: critiquing model cards and delivery plans, computing precision and break-even points under time pressure, reading ethics frameworks and data-sharing agreements with exactness, and navigating the leadership dilemmas where evidence, people, and public values meet.

A few themes will have become clear along the way. First, these assessments measure disciplines you already practise: the contrapositive reasoning of the cognitive section is your statistical critique; the denominator vigilance of the numeric section is your evaluation work; the hedge-spotting of the verbal section is how you read governance papers; and the situational judgement rankings reward the coach-champion-challenger blend your role profile describes. Preparation is therefore less about acquiring new skills than about translating your daily craft into assessment formats — and a modest amount of deliberate, timed practice does that translation remarkably quickly.

Second, the habits that score well are the habits that lead well: answer from the evidence in front of you, name your uncertainty honestly, prefer options that create information and preserve relationships, and be the person who reads the document all the way to the clause that matters.

As next steps, consider spacing your practice over a few weeks rather than cramming; revisiting the questions you found hardest and articulating out loud why the strong answer is strong; and writing a few questions of your own from your team's real artefacts — there is no faster way to internalise a format than to construct it. If a live assessment is ahead of you, ask the organisers about format, timing, calculator policy, and adjustments — knowing the shape of the day removes most of its stress.

Above all, take encouragement: you lead a discipline built on curiosity, rigour, and honest evidence, and those are precisely the qualities these assessments exist to find. Prepare steadily, trust your reasoning, and let the capability you exercise every day show. Good luck — and keep investing in your own development as generously as you invest in your team's.
