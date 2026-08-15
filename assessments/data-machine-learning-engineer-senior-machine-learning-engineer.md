# Machine Learning Engineer (Senior Machine Learning Engineer) - Psychometric Assessment Resources

## Introduction

Welcome. This document is a practical, role-specific preparation resource for psychometric assessments, written for you as a senior machine learning engineer working within the UK Government Digital and Data (GDAD) profession. Whether you are preparing for a promotion board, an internal capability review, a move to a new department, or simply want to sharpen the reasoning skills that underpin your day-to-day work, this guide is designed to help you practise with material that actually looks like your job.

Psychometric assessments are structured, standardised exercises that measure the mental capabilities and behavioural judgement a role demands. They are widely used across the Civil Service and the wider public sector because they are objective, evidence-based, and fair: everyone answers the same style of questions and is scored against the same benchmark. For a senior machine learning engineer, the capabilities being measured are ones you already exercise constantly — deciding which model is most suitable for a service, interrogating evaluation metrics, reading dense technical and policy documents with precision, and making sound judgement calls when models in live services behave unexpectedly or stakeholders disagree.

This document is organised into four assessment sections, each mapped directly to your role's duties and skills:

1. **Workplace job-specific cognitive assessment** — pattern recognition, logical deduction, error checking, prioritisation, and problem solving using the artefacts you really handle: model pipelines, deployment configurations, evaluation matrices, and incident logs.
2. **Workplace job-specific numeric reasoning assessment** — interpreting performance metrics, capacity figures, budgets, latency tables, and drift statistics, with full worked arithmetic in every explanation.
3. **Workplace job-specific verbal reasoning assessment** — dense passages drawn from the kinds of standards, policies, service assessments, and stakeholder emails you read every week, followed by True / False / Cannot Say and comprehension questions.
4. **Workplace job-specific situational judgement assessment** — realistic dilemmas involving product managers, data scientists, security teams, and senior stakeholders, testing how you balance delivery pressure against safety, ethics, and public sector values.

Each section explains what the assessment measures, maps it explicitly to the skills in your role profile, provides ten or more substantial practice questions with correct answers and worked explanations, and closes with preparation tips and common pitfalls.

How to use this resource: work through the practice questions under light time pressure first, then review the explanations carefully — the reasoning matters more than the score. Treat wrong answers as diagnostic information, exactly as you would treat a failing evaluation metric. Revisit sections periodically rather than cramming. As a senior practitioner, you will find some questions straightforward; use those to build speed, and use the harder ones to stress-test your reasoning under ambiguity.

Good luck — and remember that these assessments measure skills you demonstrably already have. The goal here is familiarity and confidence.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive ability assessment measures the exact mental processes your role demands, using practical scenarios and data formats drawn from real work rather than abstract puzzles. Unlike a generic IQ test, every question mimics an artefact you genuinely handle: a model evaluation matrix, a deployment pipeline configuration, a set of retraining logs, or a prioritisation call across competing production incidents.

The typical format is an online, timed test of 15 to 30 minutes, with objective scoring against a benchmark or norm group. Modern platforms may adapt question difficulty based on your previous answers, and employers usually receive a breakdown showing speed versus accuracy rather than a single score. You will often be given short, ungraded practice questions first so you can get used to the interface — take them seriously, because they remove interface friction before the clock starts.

For a senior machine learning engineer, cognitive ability is not an abstract credential. Deciding what model is most suitable for a product, diagnosing why a retrained model regressed, spotting a subtle error in an integration build, and prioritising which of five simultaneous alerts actually threatens a live service are all cognitive tasks executed under time pressure. This assessment predicts performance on exactly that kind of work.

### What it measures for your role

The dimensions of this assessment map directly to the skills named in your role profile:

- **Pattern recognition and logical deduction** map to your skill in *applied maths, statistics and scientific practices*: recognising trends in time series, deducing which of several candidate models satisfies a set of constraints, and reasoning about optimisation trade-offs.
- **Error checking** maps to *programming and build (software engineering)*: reviewing specifications, spotting inconsistencies between a config file and its documented intent, and catching defects before they reach production.
- **Problem solving and fault diagnosis** map to *systems integration*: tracing a failure through an integration build, reasoning about dependencies between systems, and identifying which component in a pipeline is the true root cause.
- **Prioritisation under constraint** maps to your senior-level duty to check that models in live products and services stay safe, secure and effective — deciding what to fix first when several things are wrong at once.
- **Structured abstract reasoning** maps to *data science innovation*: seeing the general structure behind a specific problem, which is exactly what you do when you identify opportunities for data science to improve data practices.

### Practice questions

**Question 1 (easy) — Sequence recognition in retraining schedules**

Your team retrains a demand-forecasting model on a schedule driven by data volume. The last five retraining runs used training sets of the following sizes (in millions of rows): 2.0, 3.0, 4.5, 6.75, 10.125. If the pattern continues, what size will the next training set be?

A) 12.5 million rows
B) 13.5 million rows
C) 15.1875 million rows
D) 20.25 million rows

**Correct answer: C**

**Explanation:** Each term is 1.5 times the previous term: 2.0 × 1.5 = 3.0; 3.0 × 1.5 = 4.5; 4.5 × 1.5 = 6.75; 6.75 × 1.5 = 10.125. The next term is 10.125 × 1.5 = 15.1875 million rows. Geometric growth patterns like this appear constantly in capacity planning; the assessment is checking that you test a multiplicative hypothesis rather than assuming additive growth.

**Question 2 (easy) — Error checking a deployment manifest**

A junior engineer submits a deployment manifest for review. The documented intent says: "The fraud-scoring model must run with 3 replicas in production, 1 replica in staging, autoscaling capped at 6 replicas, and a memory limit of 4 GiB per replica." The manifest contains: production replicas: 3; staging replicas: 1; autoscaling maximum: 8; memory limit: 4 GiB. Which single field contradicts the documented intent?

A) Production replicas
B) Staging replicas
C) Autoscaling maximum
D) Memory limit

**Correct answer: C**

**Explanation:** The intent caps autoscaling at 6 replicas; the manifest allows 8. All other fields match. This is a pure error-checking item: the skill is disciplined field-by-field comparison rather than pattern-matching on what "looks right". In your role, exactly this kind of mismatch is how a model quietly consumes double its budgeted compute.

**Question 3 (moderate) — Logical deduction in model selection**

You must choose one model for a citizen-facing eligibility checker. The constraints are: (1) if a model cannot produce explanations for individual predictions, it cannot be used for citizen-facing decisions; (2) any model used must score at least 0.85 macro F1 on the held-out test set; (3) if a model requires GPU inference, it must be deployed on the shared GPU cluster, which is unavailable until next quarter; (4) the service must launch this quarter.

- Model P: macro F1 0.91, no per-prediction explanations, CPU inference.
- Model Q: macro F1 0.87, per-prediction explanations, GPU inference required.
- Model R: macro F1 0.86, per-prediction explanations, CPU inference.
- Model S: macro F1 0.83, per-prediction explanations, CPU inference.

Which model can be used?

A) Model P
B) Model Q
C) Model R
D) Model S

**Correct answer: C**

**Explanation:** Apply each constraint as an elimination rule. Model P fails constraint 1 (no explanations for a citizen-facing decision). Model Q needs GPU inference, so constraint 3 forces deployment onto a cluster unavailable until next quarter, which violates constraint 4 (launch this quarter). Model S fails constraint 2 (0.83 < 0.85). Model R satisfies all four: F1 0.86 ≥ 0.85, explanations available, CPU inference so no GPU dependency, so it can launch this quarter. Note that the highest-accuracy model is not the answer — the assessment is testing constraint satisfaction, not metric maximisation, which mirrors your senior duty to decide what model is *most suitable*, not merely most accurate.

**Question 4 (moderate) — Pipeline dependency reasoning**

A nightly training pipeline has six stages with dependencies: Ingest must finish before Validate; Validate must finish before both Feature-Build and Schema-Report; Feature-Build must finish before Train; Train must finish before Evaluate; Schema-Report has no downstream dependencies. Tonight, Validate failed. Which stages definitely did not run to completion?

A) Feature-Build, Train, Evaluate, and Schema-Report
B) Feature-Build, Train, and Evaluate only
C) All six stages
D) Schema-Report only

**Correct answer: A**

**Explanation:** Everything downstream of the failed stage is blocked. Validate feeds both Feature-Build and Schema-Report; Feature-Build feeds Train, which feeds Evaluate. So Feature-Build, Schema-Report, Train, and Evaluate are all blocked. Ingest ran (it is upstream of the failure), and Validate itself started but failed. The distractor B tempts you to forget that Schema-Report also depends on Validate even though it sits on a side branch. Dependency tracing like this is the core cognitive act of coordinating build activities across systems in your systems integration skill.

**Question 5 (moderate) — Spotting the anomalous metric**

Four weekly monitoring snapshots for a live classification model show: Week 1 — precision 0.92, recall 0.88, daily volume 41,000; Week 2 — precision 0.91, recall 0.89, daily volume 43,500; Week 3 — precision 0.92, recall 0.88, daily volume 44,100; Week 4 — precision 0.91, recall 0.61, daily volume 43,900. Which conclusion is best supported?

A) The model's overall quality has been stable for four weeks.
B) A recall regression occurred in Week 4 while precision and volume stayed in their normal range.
C) Traffic growth caused the model to degrade.
D) Precision and recall both degraded gradually across the month.

**Correct answer: B**

**Explanation:** Precision stays within 0.91–0.92 all month and volume within roughly 41,000–44,100, but recall drops abruptly from a stable 0.88–0.89 band to 0.61 in Week 4. That is a step change in one metric, not gradual degradation (eliminating D), and it contradicts stability (eliminating A). Option C asserts causation from traffic, but volume in Week 4 is essentially the same as Weeks 2–3, so traffic cannot explain the drop. The discipline being tested — isolate which signal changed, and refuse causal stories the data does not support — is exactly what your monitoring duty requires when checking that live models continue to work effectively.

**Question 6 (moderate) — Prioritisation across simultaneous incidents**

At 09:00 you have four open items: (1) a live safeguarding-referral triage model is returning errors on 40% of requests; (2) a stakeholder wants a same-day answer about next quarter's model roadmap; (3) the nightly retraining job for an internal analytics model failed, meaning it will serve yesterday's model today; (4) a security patch for the model-serving platform is due within five working days. Which order of attention is most defensible?

A) 2, 1, 4, 3
B) 1, 3, 4, 2
C) 1, 4, 3, 2
D) 4, 1, 2, 3

**Correct answer: C**

**Explanation:** Item 1 is a live citizen-impacting failure in a high-stakes service — top priority without question. Item 4 is a security obligation with a hard deadline; although five days remain, security patching of the serving platform outranks an internal model serving a one-day-stale version (item 3), which has low real impact because yesterday's model still functions. Item 2 is important but is a same-day communication, not an operational risk, and can be handled with a brief holding reply. Option B is the main distractor: it ranks the failed retraining job above the security patch, but a stale internal model for one day carries less risk than delaying security work. The assessment rewards impact-and-risk ordering rather than order-of-arrival.

**Question 7 (hard) — Deductive fault isolation in an integration build**

An integrated service calls your model through this chain: API Gateway → Feature Service → Model Endpoint → Response Formatter. You observe: requests sent directly to the Model Endpoint with hand-built feature vectors return correct predictions; requests through the full chain return predictions that are systematically wrong for exactly one input field (applicant age is always treated as 0); the Response Formatter passes its unit tests and does not touch input features; the API Gateway logs show age arriving correctly from clients. Where is the fault most likely located?

A) API Gateway
B) Feature Service
C) Model Endpoint
D) Response Formatter

**Correct answer: B**

**Explanation:** Work by elimination with the evidence. The Model Endpoint is exonerated because direct calls with correct features produce correct predictions. The Gateway is exonerated because its logs show age arriving correctly. The Response Formatter operates after prediction and does not touch features, so it cannot zero out age before inference. The only remaining component between a correct age at the Gateway and a zeroed age at inference is the Feature Service — most plausibly a field-mapping or null-defaulting bug. This is classic differential diagnosis: each observation removes suspects. It mirrors the integration testing activities your role profile names explicitly.

**Question 8 (hard) — Rule-based deduction about retraining triggers**

Your team's retraining policy states: a model is retrained if population stability index (PSI) on any key feature exceeds 0.25, OR if weekly accuracy drops more than 3 percentage points below its rolling quarterly mean, provided in either case that the labelled feedback backlog contains at least 10,000 examples. Additionally, no retraining may occur during the two-week pre-election period. Current facts: PSI on "applicant income" is 0.31; weekly accuracy is 1.8 points below the quarterly mean; the feedback backlog holds 14,200 labelled examples; the pre-election period begins in three weeks. Should the model be retrained now?

A) No, because accuracy has not dropped more than 3 points.
B) No, because the pre-election period is approaching.
C) Yes, because the PSI condition and the backlog condition are both satisfied and the pre-election restriction is not yet in force.
D) Cannot be determined without knowing which features are "key" features.

**Correct answer: C**

**Explanation:** The trigger is a disjunction: PSI breach OR accuracy breach. PSI of 0.31 exceeds 0.25, so the first disjunct is satisfied regardless of accuracy. The conjunctive proviso — at least 10,000 labelled examples — is met (14,200). The prohibition applies only *during* the pre-election period, which starts in three weeks, so it does not block action now. Option D is a tempting overcaution, but the question states PSI is measured on "applicant income" as a key feature by presenting it as a PSI-monitored feature under the policy; the stem gives you everything needed. The cognitive skill is parsing nested logical structure (OR, AND, temporal condition) correctly — precisely what you do when you encode business rules into pipeline automation.

**Question 9 (hard) — Pattern recognition in error distributions**

A named-entity model deployed in a casework system shows the following error pattern over six weeks. Errors on documents scanned from paper: 4%, 4%, 5%, 9%, 15%, 22%. Errors on born-digital documents: 3%, 3%, 3%, 3%, 4%, 3%. Which hypothesis best fits the pattern and should be investigated first?

A) The model is degrading uniformly and needs immediate retraining on all data.
B) Something in the upstream scanning or OCR process changed around week 4, degrading inputs for scanned documents only.
C) Casework staff have started mislabelling errors.
D) Born-digital documents have become easier to process.

**Correct answer: B**

**Explanation:** The signature is a divergence: one input channel degrades sharply and progressively from week 4 while the other stays flat. Uniform model degradation (A) would affect both channels. Mislabelling (C) would most plausibly affect both channels too, and nothing in the data suggests it. Option D describes the stable channel as changing, which it is not. A channel-specific, time-localised degradation points upstream of the model — scanning hardware, OCR software version, or a new supplier of scanned input. The senior-level insight being tested: before retraining a model, check whether the model is even the thing that changed. This protects you from the classic failure of retraining on corrupted inputs and baking the fault into the model.

**Question 10 (moderate) — Specification consistency check**

A specification you are reviewing states: "The recommendation model shall return at most 5 results per query. Results shall be ordered by descending relevance score. Results with a relevance score below 0.2 shall be excluded. If fewer than 3 results remain after exclusion, the service shall display a 'no strong matches' banner alongside any remaining results." A test report claims all four behaviours pass, and includes this observed output for one query: 6 results returned, scores 0.91, 0.84, 0.77, 0.61, 0.44, 0.18, in that order, no banner shown. How many of the four specified behaviours does this observed output actually violate?

A) One
B) Two
C) Three
D) Four

**Correct answer: B**

**Explanation:** Check each rule against the output. Rule 1 (at most 5 results): violated — 6 were returned. Rule 2 (descending order): satisfied — 0.91 down to 0.18 is monotonically decreasing. Rule 3 (exclude scores below 0.2): violated — 0.18 was included. Rule 4 (banner if fewer than 3 remain after exclusion): after correct exclusion, 5 results would remain, so no banner is required — the absence of a banner is consistent. Two violations. The trap is double-counting: the 0.18 result causes both the count breach and the threshold breach, and careless reviewers either count it once or count the banner as a third failure. Precise specification-versus-behaviour comparison is central to your programming and build skill, where you test against agreed specifications.

**Question 11 (hard) — Prioritising an investigation tree**

A model serving citizen benefit estimates suddenly shows a 12% increase in complaint escalations. You can investigate four hypotheses, each taking half a day: (H1) a feature pipeline schema change last Tuesday; (H2) seasonal change in applicant mix; (H3) a serving-infrastructure timeout causing fallback to a simpler model; (H4) a front-end change that displays estimates differently. Monitoring shows: model prediction distributions are unchanged; serving latency and fallback rates are normal; the complaint increase began the same day as a front-end release. Which hypothesis should you investigate first?

A) H1
B) H2
C) H3
D) H4

**Correct answer: D**

**Explanation:** Use the evidence to price each hypothesis. Unchanged prediction distributions argue against H1 and H2 (both would shift model outputs). Normal fallback rates argue against H3. The complaint increase is temporally aligned with a front-end release, and a display change can alter how citizens perceive identical estimates — consistent with unchanged model behaviour plus increased complaints. H4 is both the best supported and cheapest to confirm (compare complaint content before and after the release). The tested skill is Bayesian-style ordering of investigations by evidence fit, not by which hypothesis is closest to your own specialism — a senior habit that prevents ML engineers reflexively suspecting the model first.

**Question 12 (moderate) — Working-memory and rule application**

Your access-control policy for model artefacts states: production model weights may be downloaded only by engineers with role "ML-Prod" AND an active incident ticket, OR by the service owner with written approval from the security lead. Four requests arrive: (1) an ML-Prod engineer with an active incident ticket; (2) an ML-Prod engineer with no ticket; (3) the service owner with security-lead approval; (4) a data scientist with an active incident ticket. How many requests should be granted?

A) One
B) Two
C) Three
D) Four

**Correct answer: B**

**Explanation:** Request 1 satisfies the first clause (ML-Prod AND ticket) — grant. Request 2 has the role but no ticket — refuse. Request 3 satisfies the second clause (service owner AND approval) — grant. Request 4 has a ticket but not the ML-Prod role and is not the service owner — refuse. Two grants. The structure is (A AND B) OR (C AND D); the common error is treating the ticket alone as sufficient. Correctly applying compound access rules is part of keeping models secure in live services, a duty your role level names explicitly.

**Question 13 (hard) — Abstract reasoning about optimisation trade-offs**

You are tuning a model where each unit of additional training compute improves accuracy with diminishing returns, and each accuracy point above 90% halves the volume of cases needing manual review. Manual review capacity is fixed. Currently the model is at 92% accuracy and the review queue is at 80% of capacity, growing 5% per month due to rising demand. Training compute budget can buy you either: (X) one accuracy point now, or (Y) infrastructure that permanently reduces per-case review time by 10%. Which reasoning is soundest?

A) Choose X, because accuracy improvements compound while process improvements do not.
B) Choose Y, because accuracy gains at 92% are marginal while demand growth is a persistent pressure on a fixed-capacity process.
C) Choose X, because halving review volume (one point above 90% doubles the halving) immediately clears the queue for good.
D) Neither helps, because demand growth will exhaust any fixed gain.

**Correct answer: B**

**Explanation:** Work through the mechanics. Option X buys one accuracy point (92% → 93%), which by the stated rule halves review volume once — a large but one-off reduction, and diminishing returns mean the next point costs even more. Option Y reduces per-case review time by 10% permanently, effectively raising throughput capacity against a demand curve growing 5% per month. Option A's claim that accuracy "compounds" reverses the stated diminishing-returns structure. Option C overreads the halving rule and wrongly claims a permanent fix against growing demand. Option D is defeatist: both options help; the question is which helps more durably. B correctly matches a persistent pressure with a persistent remedy. This mirrors real senior decisions about whether to spend effort on the model or on the system around the model.

**Question 14 (moderate) — Deduction from monitoring alerts**

Three alerting rules protect a live model: Rule A fires if p95 latency exceeds 800 ms for 5 consecutive minutes; Rule B fires if the error rate exceeds 2% over any 10-minute window; Rule C fires if prediction volume falls below 50% of the same hour last week. This morning, Rule C fired but Rules A and B did not. Which situation is consistent with exactly this alert pattern?

A) The model endpoint crashed and is returning HTTP 500 errors to all callers.
B) An upstream service stopped sending requests to the model, while the requests that do arrive are served normally.
C) The model is timing out on most requests due to a memory leak.
D) A traffic surge has overloaded the endpoint.

**Correct answer: B**

**Explanation:** Test each scenario against all three rules. A crashed endpoint returning 500s (A) would drive the error rate far above 2%, firing Rule B — but Rule B did not fire. Widespread timeouts (C) would push p95 latency past 800 ms, firing Rule A — it did not. A traffic surge (D) would raise volume, not drop it below 50% of the weekly baseline, so Rule C would not fire. Only option B fits: requests dry up at the source (volume collapses, firing Rule C) while the surviving requests are healthy (latency and error rates normal, so Rules A and B stay quiet). The tested skill is reasoning about what each alert's *silence* tells you, not just what the firing alert says — an essential habit when you check that live models continue to work effectively, because the most dangerous production failures are often upstream of the model and invisible to model-centric metrics. Note also the operational lesson embedded here: volume-based alerts are your only defence against "silent" integration breakages, which is why senior engineers insist on them when defining the integration build.

### Preparation tips

- **Practise on your own artefacts.** Before the assessment, spend an hour reviewing a recent deployment config, an evaluation report, and an incident postmortem, and consciously articulate the reasoning chains in them. The test formats are abstractions of exactly these documents.
- **Rehearse elimination discipline.** Most cognitive items at senior level are solved fastest by eliminating options that violate a stated constraint. Train yourself to read constraints first, options second.
- **Time-box each question.** In a 20-minute, 20-question test you have roughly a minute per item. If an item resists you for 90 seconds, flag it and move on — exactly as you would time-box a debugging session.
- **Do the arithmetic on paper, not in your head, when stakes are high.** Careless slips, not lack of ability, are the main score-killer for experienced engineers.
- **Sleep and setup matter.** Take the test rested, on a reliable connection, with notepaper ready. Treat it like a production deployment: remove avoidable sources of failure in advance.
- **Use the ungraded practice items fully.** They exist to eliminate interface surprises. Never skip them to "save energy".

### Common pitfalls

- **Answering from experience instead of from the stem.** Senior engineers often "know" what usually causes a failure and pick it before checking the given evidence. The questions are constructed so the evidence, not the base rate, determines the answer.
- **Choosing the highest-performing option rather than the compliant one.** As in Question 3, the best metric does not win if a constraint is violated. Assessments deliberately punish metric tunnel vision.
- **Losing points to speed–accuracy imbalance.** Reports show speed versus accuracy separately; a rushed 60% accurate performance scores worse than a measured 85%. Calibrate during practice.
- **Forgetting side branches in dependency questions.** As in Question 4, components hanging off a failed node are easy to overlook when they are not on the "main path".
- **Getting anchored on one hypothesis.** In fault-diagnosis items, force yourself to state what evidence would exonerate each component before choosing.
- **Ignoring qualifiers.** Words like "definitely", "at most", "only", and "provided that" carry the logical weight of the question. Read them twice.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment evaluates your ability to analyse, interpret, and make sound decisions using numerical data presented in the formats your role really uses. It focuses on applied business mathematics — percentages, ratios, rates, cost comparisons, and capacity calculations — rather than abstract formulae. Question inputs are tables, dashboards, budgets, and schedules rather than equations.

Typical characteristics: a strict time limit (often around a minute per question), an onscreen calculator allowed or provided, and scoring that prioritises accurate interpretation over mental-arithmetic gymnastics. The pressure is deliberate: it simulates the reality of extracting the right figure quickly from a monitoring dashboard during an incident, or sanity-checking a compute budget in a planning meeting.

For a senior machine learning engineer, numbers are the medium of the job. You evaluate models with precision, recall, and F1; you plan GPU capacity and inference costs; you set drift thresholds; you compare latency percentiles; you justify infrastructure spend to product teams. This assessment measures whether you can move through such figures quickly and without error — a direct proxy for daily performance in your role.

### What it measures for your role

- **Statistical interpretation** maps to *applied maths, statistics and scientific practices*: reading confusion matrices, computing rates and proportions, interpreting time series changes, and reasoning about sampling.
- **Cost, capacity and optimisation arithmetic** maps to your duties to deploy and scale models and to help product teams evaluate and choose appropriate solutions: cloud cost comparisons, throughput calculations, and cost-benefit estimates between candidate models.
- **Performance-metric fluency** maps to your duty to test and assure models against performance requirements: percentage-point changes, ratios between error types, and threshold reasoning.
- **Data quality quantification** maps to *data ethics and privacy* and *data science innovation*: quantifying group-level disparities in model outcomes and measuring the numerical impact of data issues.
- **Translating numbers for stakeholders** maps to *communicating between the technical and non-technical*: several questions require choosing the correct plain-figure summary of a technical result.

### Practice questions

**Question 1 (easy) — Percentage change in inference cost**

Your model's monthly inference cost was £8,400 in June. In July, after you optimised the serving container, the cost fell to £6,720. What was the percentage reduction?

A) 15%
B) 20%
C) 25%
D) 30%

**Correct answer: B**

**Explanation:** Reduction = £8,400 − £6,720 = £1,680. Percentage reduction = 1,680 ÷ 8,400 = 0.20 = 20%. A quick sanity check: 10% of 8,400 is 840, so 1,680 is exactly 2 × 840 = 20%. Watch the direction of the base: percentage change is always measured against the *original* value (June), not the new one — dividing by 6,720 would give 25% and lead you to distractor C.

**Question 2 (easy) — Throughput and capacity**

A model endpoint handles 250 requests per second per replica. The service must support a peak of 4,200 requests per second, with at least 20% headroom above peak. What is the minimum number of replicas required?

A) 17
B) 20
C) 21
D) 24

**Correct answer: C**

**Explanation:** Required capacity = 4,200 × 1.20 = 5,040 requests per second. Replicas needed = 5,040 ÷ 250 = 20.16, and because replicas are whole units you must round *up* to 21. Distractor B comes from rounding down or from forgetting that 20 replicas provide exactly 5,000 requests per second, which is 40 short of the required 5,040. Capacity questions almost always test whether you remember to apply the headroom before dividing and to round up afterwards.

**Question 3 (moderate) — Confusion matrix arithmetic**

Your fraud-detection model was evaluated on 10,000 transactions, of which 400 were actually fraudulent. The model flagged 500 transactions as fraud. Of the flagged transactions, 320 were genuinely fraudulent. What are the model's precision and recall for the fraud class?

A) Precision 64%, recall 80%
B) Precision 80%, recall 64%
C) Precision 80%, recall 80%
D) Precision 64%, recall 64%

**Correct answer: A**

**Explanation:** Precision = true positives ÷ all flagged = 320 ÷ 500 = 0.64 = 64%. Recall = true positives ÷ all actual fraud = 320 ÷ 400 = 0.80 = 80%. The distractor B swaps the two denominators, which is the single most common error in metric arithmetic. A senior engineer must keep these straight instinctively: precision answers "when we flag, how often are we right?", recall answers "of the real fraud, how much do we catch?" — and each maps to a different operational cost (wasted investigations versus missed fraud).

**Question 4 (moderate) — Comparing model options on cost per correct prediction**

A product team asks you to compare two candidate models for a document-classification service processing 2,000,000 documents per month. Model A: accuracy 94%, inference cost £0.0008 per document. Model B: accuracy 97%, inference cost £0.0014 per document. What is the monthly cost per *correctly classified* document for each model, to four decimal places of a penny?

A) Model A £0.00085, Model B £0.00144
B) Model A £0.00080, Model B £0.00140
C) Model A £0.00094, Model B £0.00097
D) Model A £0.00085, Model B £0.00136

**Correct answer: A**

**Explanation:** Monthly cost: Model A = 2,000,000 × £0.0008 = £1,600; Model B = 2,000,000 × £0.0014 = £2,800. Correct classifications: Model A = 2,000,000 × 0.94 = 1,880,000; Model B = 2,000,000 × 0.97 = 1,940,000. Cost per correct prediction: A = 1,600 ÷ 1,880,000 ≈ £0.000851; B = 2,800 ÷ 1,940,000 ≈ £0.001443. So A ≈ £0.00085 and B ≈ £0.00144. Distractor B is the raw per-document cost without adjusting for accuracy. Note the decision insight this arithmetic supports: Model B's 3-point accuracy gain costs roughly 70% more per correct answer, so its suitability depends on the cost of an error — precisely the "help product teams evaluate and choose appropriate machine learning solutions" duty in your role profile.

**Question 5 (moderate) — Percentage points versus percentages**

At the last service review, your model's weekly accuracy was reported as falling "from 92% to 88%". A stakeholder writes that "accuracy fell by 4%". As part of managing expectations precisely, what is the accurate description?

A) Accuracy fell by 4 percentage points, which is a relative fall of about 4.3%.
B) Accuracy fell by 4 percentage points, which is a relative fall of exactly 4%.
C) Accuracy fell by 4.3 percentage points, which is a relative fall of 4%.
D) The stakeholder's statement is fully accurate.

**Correct answer: A**

**Explanation:** The absolute change is 92 − 88 = 4 percentage points. The relative change is 4 ÷ 92 = 0.0435 ≈ 4.3%. Percentage points and percentages are different units, and conflating them misleads non-technical audiences — a small but recurring hazard in your communicating-between-technical-and-non-technical skill. In formal reporting, quote the percentage-point change and, where useful, add the relative change explicitly.

**Question 6 (moderate) — GPU training budget**

Retraining your ranking model takes 18 hours on a node costing £4.20 per hour. You retrain weekly. The platform team offers a reserved-capacity deal: £220 per month flat for the same node, but retraining on it takes 20 hours due to shared contention. Assume 4.33 retraining runs per month on average. Which option is cheaper per month, and by roughly how much?

A) Pay-as-you-go, by about £55
B) Reserved capacity, by about £107
C) Reserved capacity, by about £55
D) They cost about the same

**Correct answer: B**

**Explanation:** Pay-as-you-go monthly cost = 18 hours × £4.20 × 4.33 runs = £75.60 × 4.33 ≈ £327.35. Reserved capacity = £220 flat (the longer 20-hour runtime does not change the flat price; it is a service consideration, not a cost). Saving ≈ £327 − £220 = £107. Distractor A reverses the comparison; distractor C halves the saving by mistakenly costing only part of the month. The extra two hours per run is worth flagging to the team as a schedule impact, but the arithmetic question asked only about cost — read what is asked.

**Question 7 (hard) — Drift threshold and sample proportions**

Your monitoring compares the proportion of high-risk predictions week over week. Last week: 1,840 high-risk out of 46,000 predictions. This week: 2,310 high-risk out of 42,000 predictions. Your alerting rule fires if the high-risk *rate* rises by more than 30% relative to the previous week. Does the alert fire?

A) No — the rate rose by 25.6%
B) No — the rate rose by 30% exactly
C) Yes — the rate rose by 37.5%
D) Yes — the rate rose by 47.0%

**Correct answer: C**

**Explanation:** Last week's rate = 1,840 ÷ 46,000 = 0.04 = 4.0%. This week's rate = 2,310 ÷ 42,000 = 0.055 = 5.5%. Relative increase = (5.5 − 4.0) ÷ 4.0 = 1.5 ÷ 4.0 = 0.375 = 37.5%, which exceeds the 30% threshold, so the alert fires. The trap is comparing raw counts: 2,310 versus 1,840 is a 25.6% increase in count (distractor A), but total volume fell from 46,000 to 42,000, so the *rate* rose much more sharply. Rate-versus-count confusion is exactly the kind of subtle numerical error that causes teams to miss genuine drift in live services.

**Question 8 (hard) — Latency percentiles and SLA compliance**

Your service-level agreement requires p95 latency under 500 ms. This week's latency samples for the recommendation endpoint were distributed as follows: 88% of requests under 300 ms; 7% between 300 and 500 ms; 4% between 500 and 900 ms; 1% above 900 ms. Is the SLA met, and what is the strongest correct statement?

A) Yes — 95% of requests complete under 500 ms, so p95 is at most 500 ms.
B) No — 5% of requests exceed 500 ms, so p95 is above 500 ms.
C) Yes — average latency is clearly under 500 ms.
D) Cannot be determined from percentile bands.

**Correct answer: A**

**Explanation:** Cumulate the bands: 88% + 7% = 95% of requests complete in under 500 ms. The 95th percentile is the value below which 95% of observations fall; since 95% of requests fall below 500 ms, p95 ≤ 500 ms and the SLA (p95 under 500 ms) is met — strictly, met at the boundary, with 95% *under* 500 ms satisfying it. Distractor B misreads "5% exceed 500 ms" — in fact 5% are *at or above* 500 ms, which places p95 right at the 500 ms boundary, not above it. Distractor C is irrelevant: an SLA on p95 says nothing about the mean, and averages are notoriously misleading for latency. Understanding exactly what a percentile asserts is essential when you test and assure models against performance requirements.

**Question 9 (hard) — Fairness disparity arithmetic**

An eligibility-triage model's monthly audit shows approval rates by age band: under-35 applicants — 6,300 approvals from 9,000 applications; over-35 applicants — 4,560 approvals from 7,600 applications. Your data ethics review uses the "four-fifths" screening rule: the lower group rate should be at least 80% of the higher group rate. What is the ratio of the lower rate to the higher rate, and does it pass the screen?

A) 0.86 — passes
B) 0.79 — fails
C) 0.83 — passes
D) 0.75 — fails

**Correct answer: A**

**Explanation:** Under-35 rate = 6,300 ÷ 9,000 = 0.70 = 70%. Over-35 rate = 4,560 ÷ 7,600 = 0.60 = 60%. The lower rate is 60%; ratio = 0.60 ÷ 0.70 = 0.857 ≈ 0.86, which is at least 0.80, so the screen passes. Common errors: dividing the smaller *count* by the larger count (4,560 ÷ 6,300 = 0.72, near distractor D), or inverting which group is the denominator. Passing a screening ratio is not the end of an ethics review — your role profile expects you to work with stakeholders to identify and address ethical concerns, and a 10-percentage-point gap may still warrant investigation of causes — but the arithmetic itself must be exact before any such conversation.

**Question 10 (moderate) — Weighted evaluation score**

Your team scores candidate models on three criteria with fixed weights: accuracy (weight 0.5), latency (weight 0.3), and maintainability (weight 0.2), each scored out of 100. Model X scores accuracy 90, latency 60, maintainability 80. Model Y scores accuracy 82, latency 85, maintainability 85. Which model wins, and by how many weighted points?

A) Model X wins by 2.5
B) Model Y wins by 4.5
C) Model Y wins by 2.5
D) Model X wins by 4.5

**Correct answer: B**

**Explanation:** Model X: (90 × 0.5) + (60 × 0.3) + (80 × 0.2) = 45 + 18 + 16 = 79. Model Y: (82 × 0.5) + (85 × 0.3) + (85 × 0.2) = 41 + 25.5 + 17 = 83.5. Model Y wins by 83.5 − 79 = 4.5 weighted points. The distractors are built from predictable slips: forgetting the 25.5 (writing 85 × 0.3 as 25) narrows the margin towards 2.5, and mis-assigning the weights (0.5 on latency instead of accuracy) flips the winner to Model X. Two habits protect you: write the weight beside each score before multiplying, and verify the weights sum to 1.0. Weighted scoring matrices are a standard tool when you help product teams evaluate and choose appropriate machine learning solutions, so this arithmetic should feel like home ground — note also the real-world caveat that a weighted total is only as defensible as the weights themselves, which stakeholders should agree before the scores are known.

**Question 11 (moderate) — Sampling for a labelling budget**

You need a stratified evaluation set of 2,400 labelled cases, matching the live traffic mix: 55% English-language documents, 30% Welsh-language, 15% other languages. Labelling costs £0.85 per English document, £1.40 per Welsh document, and £2.10 per other-language document. What is the total labelling cost?

A) £2,886
B) £2,880
C) £2,517
D) £3,024

**Correct answer: A**

**Explanation:** Stratum sizes: English = 2,400 × 0.55 = 1,320; Welsh = 2,400 × 0.30 = 720; other = 2,400 × 0.15 = 360. Costs: English = 1,320 × £0.85 — split it as 1,320 × 0.8 = 1,056 plus 1,320 × 0.05 = 66, giving £1,122; Welsh = 720 × £1.40 = £1,008; other = 360 × £2.10 = £756. Total = 1,122 + 1,008 + 756 = £2,886. Distractor B (£2,880) sits deliberately close to the true value to punish rounding mid-calculation; C counts only two strata; D applies the Welsh price to the English stratum. Verify sums by re-adding in a different order (756 + 1,008 = 1,764; 1,764 + 1,122 = 2,886) — addition-order variation catches transposition errors that a same-order re-read never will. Stratified sampling against a labelling budget is bread-and-butter work when you build evaluation sets that reflect live traffic, part of assuring models against real usage rather than convenient data.

**Question 12 (hard) — Compound growth in request volume**

A newly launched service currently sends your model 120,000 requests per month, and volume is growing at 15% per month compound. Your current infrastructure can serve 200,000 requests per month. After how many complete months will demand first exceed capacity?

A) 3 months
B) 4 months
C) 5 months
D) 6 months

**Correct answer: B**

**Explanation:** Apply compound growth month by month: after 1 month 120,000 × 1.15 = 138,000; after 2 months 138,000 × 1.15 = 158,700; after 3 months 158,700 × 1.15 = 182,505; after 4 months 182,505 × 1.15 = 209,881. Demand first exceeds 200,000 after 4 complete months. The trap is linear thinking: 15% of 120,000 is 18,000, and (200,000 − 120,000) ÷ 18,000 ≈ 4.4, which coincidentally also suggests month 5 to those who round up (distractor C). Compound growth accelerates, so it crosses the threshold earlier than the linear estimate. Planning deployment capacity ahead of demand is a core part of your duty to deploy and scale machine learning models.

**Question 13 (moderate) — Interpreting an A/B test summary for stakeholders**

An A/B test compares the current model (control) with a retrained model (variant) on task-completion rate: control 68.0% (n = 24,000), variant 70.4% (n = 24,000), reported as statistically significant. A product manager asks: "So the new model helps roughly how many more people per 100,000 sessions?" What is the best plain-figure answer?

A) About 240 more completions per 100,000 sessions
B) About 2,400 more completions per 100,000 sessions
C) About 24,000 more completions per 100,000 sessions
D) About 3.5% more completions per 100,000 sessions

**Correct answer: B**

**Explanation:** The absolute uplift is 70.4% − 68.0% = 2.4 percentage points. Per 100,000 sessions, that is 100,000 × 0.024 = 2,400 additional completions. Distractor A drops a factor of ten; distractor D gives the *relative* uplift (2.4 ÷ 68 ≈ 3.5%) in a format that does not answer the "how many people" question. Converting rates into human-scale counts is one of the most valuable translation moves in your communicating-between-technical-and-non-technical skill: stakeholders decide on people, not percentage points.

**Question 14 (hard) — Storage and retention arithmetic**

Your feature store writes 3.2 GB of feature data per day. Privacy rules require raw features to be deleted after 90 days, but aggregated features (which take 5% of the raw size) are kept for 3 years. What is the approximate steady-state storage requirement?

A) 288 GB
B) 463 GB
C) 175 GB
D) 512 GB

**Correct answer: B**

**Explanation:** Raw features at steady state: 3.2 GB × 90 days = 288 GB (a rolling window — each day one day's data is added and one deleted). Aggregated features: 5% of 3.2 GB = 0.16 GB per day, retained for 3 years ≈ 1,095 days, giving 0.16 × 1,095 = 175.2 GB. Total ≈ 288 + 175 = 463 GB. Distractor A counts only the raw window; distractor C counts only the aggregates. Notice how the privacy retention rule directly drives the arithmetic — an everyday intersection of your data ethics and privacy skill with infrastructure planning, and a nice example of why retention schedules should be checked with real numbers before you promise storage budgets.

### Preparation tips

- **Rebuild fluency with rates, not just formulas.** Practise converting between counts, rates, percentage points, and relative percentages until it is automatic — Questions 5, 7 and 13 all turn on those conversions.
- **Use the onscreen calculator strategically.** Type full expressions rather than chaining intermediate results by memory; transcription is where errors creep in.
- **Estimate first, compute second.** A ten-second order-of-magnitude estimate ("about £2,900", "roughly 21 replicas") catches most gross errors before you commit.
- **Practise with your own dashboards.** Take a real monitoring dashboard or cost report from your service and quiz yourself: what changed, by how much, relative to what base?
- **Round up for capacity, keep precision for money.** Physical resources round up; financial comparisons keep pennies until the final step.
- **Manage the clock.** Numeric tests punish time-sink questions. If a multi-stage calculation is fighting you, flag it, bank the easier marks, and return.

### Common pitfalls

- **Misreading scale qualifiers.** "In thousands", "per replica", "per month" — the spec-level detail of chart labels is where most marks are lost. Confusing monthly with annual figures is the classic case.
- **Comparing counts when the question is about rates.** As in Question 7, counts can rise while rates fall, or vice versa, when denominators change.
- **Using the wrong base for percentage change.** Change is always measured against the original value unless stated otherwise.
- **Over-calculating.** Some questions yield to estimation and elimination in a quarter of the time a full calculation takes; look at the spread of the options before diving in.
- **Forgetting to round in the correct direction.** Replicas, staff, and labelled examples are whole units and round up for requirements; averages and costs are not.
- **Trusting your first pass of arithmetic.** Recompute subtotals in a different order, as demonstrated in Question 11 — transposition and slip errors are invisible on a same-order re-read.
