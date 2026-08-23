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

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment tests whether you can determine exactly what a piece of written material establishes. As a senior machine learning engineer the material is model documentation, evaluation reports, data sharing agreements, ethics and privacy guidance, and the research papers and vendor claims you assess when deciding what model is suitable.

The commonest format presents a passage followed by statements to be marked True, False or Cannot Say. True means the passage establishes it, False means it contradicts it, and Cannot Say means it settles neither — regardless of what you know.

Technical expertise is the principal hazard here, and it is a sharper hazard in machine learning than in most fields, because the discipline is full of claims that sound like results. You will read that a model "achieved" something and supply an experimental design the passage never described.

Three specifics matter particularly.

The first is that evaluation claims are scoped by dataset, metric and population. A figure established on one test set says nothing about another, and a metric that improved is not the same as an outcome that improved.

The second is that data sharing and privacy documents define permitted purposes narrowly. A permission to use data for one purpose does not extend to training a model on it, and this is precisely the kind of boundary your role requires you to respect.

The third is that "no evidence of X" combined with limited ability to detect X never establishes that X did not occur. This appears constantly in fairness and bias reporting, and reading it correctly is part of checking that live models stay safe.

### What it measures for your role

- **Reading evaluation reports precisely** maps to testing and assuring models to ensure they meet performance requirements.
- **Reading model documentation** maps to deciding what model is most suitable for use.
- **Reading data agreements** maps to **Data ethics and privacy**.
- **Reading integration documentation** maps to **Systems integration**.
- **Reading statistical claims** maps to **Applied maths, statistics and scientific practices**.
- **Communicating precisely** maps to **Communicating between the technical and non-technical**.

### Practice questions

*Passage A — for Questions 1 to 4*

"The model was evaluated on a held-out test set of 12,000 records drawn from the same collection period as the training data. Accuracy was 91.4%, and the area under the receiver operating characteristic curve was 0.88. Performance was reported separately for four age bands; the widest gap between bands was 6 percentage points in accuracy. The evaluation did not include records from the two regions onboarded after the collection period. No assessment of performance by ethnicity was carried out, as the field is not collected. The model is intended for use across all regions."

**Question 1 (easy)**

Statement: The model achieved 91.4% accuracy on the held-out test set.

- A) True
- B) False
- C) Cannot Say

**Correct answer: A**

**Explanation:** Stated directly and scoped precisely to the held-out test set. Note how much of the passage is devoted to qualifying what that figure covers — same collection period, four age bands, two regions excluded, no ethnicity data — which is what a well-written evaluation report does and what the next three questions test.

**Question 2 (moderate)**

Statement: The model will achieve approximately 91% accuracy in the two regions onboarded after the collection period.

- A) True
- B) False
- C) Cannot Say

**Correct answer: C**

**Explanation:** The passage states that the evaluation "did not include records from the two regions onboarded after the collection period", while the model "is intended for use across all regions". So performance in those regions is untested, and untested is not the same as equivalent or as worse. Both the test set and the training data come from the same collection period, which is a further reason to be cautious — but caution is not a finding, and the honest answer is that the passage establishes a gap rather than what is in it.

**Question 3 (moderate)**

Statement: The model performs equitably across ethnic groups.

- A) True
- B) False
- C) Cannot Say

**Correct answer: C**

**Explanation:** "No assessment of performance by ethnicity was carried out, as the field is not collected." That establishes the absence of an assessment, not the absence of a disparity. This is the single most consequential reading error in machine learning documentation, because an unassessed dimension is routinely reported and read as a clean one — and a model deployed in a public service with an unexamined equity dimension is a real problem regardless of how the sentence is phrased.

**Question 4 (harder)**

Statement: The evaluation shows the model performs consistently across age bands.

- A) True
- B) False
- C) Cannot Say

**Correct answer: C**

**Explanation:** The passage reports "the widest gap between bands was 6 percentage points in accuracy". Whether 6 points counts as consistent is a judgement the passage does not make, and it depends entirely on what the model is used for — 6 points is negligible for a content ranking task and serious for an eligibility decision. The passage supplies the number and not the interpretation. Marking True treats a small-sounding figure as a verdict; marking False treats it as a failure. Neither is established.

*Passage B — for Questions 5 to 8*

"The data sharing agreement permits the recipient to process the shared dataset for the purpose of evaluating eligibility for the named scheme. Processing for any other purpose requires the written agreement of the data controller. The recipient may retain the dataset for the duration of the scheme and for twelve months afterwards, after which it must be deleted and deletion confirmed in writing. The recipient may create derived datasets where those datasets do not permit re-identification of individuals. Derived datasets are subject to the same retention terms. The agreement does not permit onward sharing with third parties."

**Question 5 (easy)**

Statement: The recipient may process the dataset to evaluate eligibility for the named scheme.

- A) True
- B) False
- C) Cannot Say

**Correct answer: A**

**Explanation:** Stated directly as the permitted purpose. Note how tightly the permission is drawn — one named purpose, with anything else requiring written agreement — which is the structure of most data sharing agreements and the reason the next question matters.

**Question 6 (moderate)**

Statement: The recipient may train a machine learning model on the dataset without further permission.

- A) True
- B) False
- C) Cannot Say

**Correct answer: C**

**Explanation:** This turns on whether training a model *is* processing for the purpose of evaluating eligibility. If the model exists to evaluate eligibility for that scheme, a reasonable reading is that training it falls within the permitted purpose; if the model is for something else, it plainly does not. The passage does not say what the model is for, so it cannot be settled. This is exactly the ambiguity that should be resolved with the data controller in writing rather than by your own reading, and recognising that it is ambiguous is the professionally important part.

**Question 7 (moderate)**

Statement: A derived dataset that cannot be used to re-identify individuals may be retained indefinitely.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The passage contradicts this: "Derived datasets are subject to the same retention terms" — the scheme duration plus twelve months, then deletion. The non-re-identifiability condition governs whether a derived dataset may be created at all, not how long it may be kept. Reading a condition attached to creation as a release from a separate obligation is the error, and it is a common one in practice, where anonymised derivatives are often assumed to fall outside retention schedules.

**Question 8 (harder)**

Statement: The recipient may share a derived dataset with a supplier processing data on the recipient's behalf.

- A) True
- B) False
- C) Cannot Say

**Correct answer: C**

**Explanation:** The agreement "does not permit onward sharing with third parties", and whether a supplier processing on the recipient's behalf constitutes a third party in this sense is not addressed. In data protection terms a processor acting under the controller's instruction is often treated differently from an independent third party, and this passage does not adopt or reject that distinction. So the answer is genuinely unresolved — and, as with Question 6, the professional response is to get it in writing rather than to rely on the reading you prefer.

*Passage C — for Questions 9 to 12*

"A monitoring review of the deployed model covered the six months since launch. Predicted-versus-actual calibration remained within tolerance for the first four months and drifted in months five and six. The review found no evidence of degradation in performance for any monitored subgroup, noting that subgroup sample sizes in monthly monitoring are small. Input feature distributions shifted for two of eleven features. The review recommends retraining. The review did not examine whether the drift affected decisions made by the caseworkers who use the model's output."

**Question 9 (moderate)**

Statement: The model's performance did not degrade for any monitored subgroup.

- A) True
- B) False
- C) Cannot Say

**Correct answer: C**

**Explanation:** The review "found no evidence of degradation ... noting that subgroup sample sizes in monthly monitoring are small". No evidence of an effect, combined with limited power to detect it, does not establish absence. The passage is unusually helpful in flagging its own limitation, and the correct reading is that subgroup degradation is undetermined rather than ruled out. This is the standing trap in fairness monitoring, and the passage's own caveat is the clue.

**Question 10 (moderate)**

Statement: The distribution shift in two features caused the calibration drift.

- A) True
- B) False
- C) Cannot Say

**Correct answer: C**

**Explanation:** Both facts are reported; no causal link is asserted. The shift is a plausible and probably correct explanation, and the passage neither establishes it nor rules out other causes — a change in the underlying population, a change in how the data is recorded upstream, or a genuine change in the relationship being modelled. Professionally you would investigate the two shifted features first; that is a good prior, not a finding.

**Question 11 (moderate)**

Statement: The drift affected the decisions caseworkers made.

- A) True
- B) False
- C) Cannot Say

**Correct answer: C**

**Explanation:** The passage states explicitly that the review "did not examine" this. Nothing either way — and it is worth noticing that this is the question that actually matters. Calibration drift that caseworkers compensated for is a technical issue; drift that changed outcomes for people is something else entirely, and the review has left the important question unanswered while recommending a technical remedy.

**Question 12 (harder)**

Statement: Retraining the model will restore calibration.

- A) True
- B) False
- C) Cannot Say

**Correct answer: C**

**Explanation:** The review "recommends retraining", and a recommendation is not a prediction of its effect. Whether retraining restores calibration depends on why calibration drifted — retraining on recent data addresses a shifted input distribution and does not address a change in how the outcome is recorded upstream, or a feedback loop created by the model's own deployment. Treating a recommended action as an established remedy is a specific and common overreach, and here the passage has already told you that the cause was not determined.

### Preparation tips

- **Check the scope of an evaluation figure: which dataset, which population, which period.**
- **Read "no assessment was carried out" as absence of evidence.**
- **Read "no evidence of X" plus low power as undetermined, never as absence.**
- **Distinguish a reported number from an interpretation of it.**
- **Check whether a condition governs creation or retention.**
- **Notice when an agreement's key term is undefined for your case.**
- **Read a recommendation as a proposal, not as a predicted outcome.**
- **Notice which question a review did not ask.**

### Common pitfalls to avoid

- **Treating an unassessed dimension as a clean one.**
- **Generalising a test-set figure to an untested population.**
- **Assuming anonymised derivatives escape retention terms.**
- **Resolving an ambiguous data permission by your preferred reading.**
- **Reading a plausible cause as an established one.**
- **Treating a recommended remedy as a known fix.**
- **Answering from machine learning practice rather than from the passage.**

## Workplace job-specific situational judgement assessment

### About this assessment

A workplace job-specific situational judgement assessment presents realistic scenarios and asks you to identify effective and ineffective responses. As a senior machine learning engineer the scenarios involve deciding whether a model is fit to deploy, maintaining models already live, working with people who cannot evaluate what you tell them, and raising ethical and privacy concerns that are inconvenient.

The commonest formats ask for the most and least effective response, or for ratings. Scoring is against a key derived from experienced practitioners in comparable roles.

Three patterns run through the strong answers.

The first is that a model in production is a system rather than a result. The research question is answered once; the engineering questions — what happens when the input distribution shifts, who notices, what the fallback is, how it is rolled back — are answered continuously, and your role names checking that live models stay safe, secure and effective.

The second is that you are usually the only person in the room who can evaluate what you are saying. That creates an obligation to make your reasoning legible, including its uncertainty, because confident assertion from someone nobody can check is how organisations acquire expensive mistakes.

The third is that ethical and privacy concerns are cheapest to raise early and hardest to raise late, and you are frequently best placed to see them.

### What it measures for your role

- **Deployment judgement** maps to deploying, testing and assuring models against performance requirements.
- **Model maintenance** maps to checking that live models stay safe, secure and effective.
- **Model selection** maps to deciding what model is most suitable.
- **Communicating uncertainty** maps to **Communicating between the technical and non-technical**.
- **Ethical judgement** maps to **Data ethics and privacy**.
- **Integration** maps to **Systems integration** and working with others.

### Practice questions

**Question 1 (easy) — A model that evaluates well**

Your model performs strongly on the held-out test set and a product manager asks to deploy it. What is the most effective response?

- A) Deploy it; the evaluation is strong.
- B) Answer the questions the evaluation cannot — how live traffic will differ from the training data, what happens when it drifts, what the fallback is if the model is unavailable, and how a bad prediction gets noticed — because a strong test result shows the model can work, not that the system around it will.
- C) Run further offline evaluation.
- D) Deploy it behind a flag.

**Correct answer: B. Least effective: A**

**Explanation:** Offline evaluation answers one question and is silent on the four in option B, each of which has caused production failures in models that evaluated beautifully. Option D is a good mechanism and belongs after the questions rather than instead of them — a flag limits exposure without telling you what you are exposed to. Option C produces more of the evidence you already have. Option A is least effective because it treats a research result as a production decision, which is precisely the step your role exists to add rigour to.

**Question 2 (easy) — Explaining a model to a non-technical stakeholder**

A service manager asks how confident they can be in the model's predictions. What is the most effective response?

- A) Give the accuracy figure.
- B) Give the figure with what it means for their decisions — how often the model is wrong, in which direction, and what happens to a person when it is — because an accuracy percentage tells a non-specialist nothing actionable, and the errors are what they need to plan for.
- C) Explain that no model is perfect.
- D) Give the accuracy and the area under the curve.

**Correct answer: B. Least effective: C**

**Explanation:** Option B translates a technical figure into the terms the person actually decides in, and the direction of error is the part that matters most — a model that wrongly approves is a different operational problem from one that wrongly refuses. Option C is least effective: true, uninformative, and it reads as evasion when someone has asked a real question. Option D adds a second number the listener can interpret even less than the first. Option A gives a figure whose meaning depends on a base rate they do not know.

**Question 3 (moderate) — Drift in a live model**

Monitoring shows a live model's calibration has drifted over two months. Nobody has reported a problem. What is the most effective response?

- A) Retrain on recent data.
- B) Establish what is driving the drift and whether it is affecting decisions — a shifted input distribution, a change in upstream recording, or a feedback effect from the model's own deployment all look similar and need different responses, and "nobody has noticed" may mean no impact or a diffuse one.
- C) Alert the service team that the model is failing.
- D) Roll back to the previous model version.

**Correct answer: B. Least effective: D**

**Explanation:** Retraining is often the right answer and option A applies it before knowing the cause — if the drift comes from a change in how a field is recorded upstream, retraining bakes in the new error. Option B distinguishes the causes and asks the question that actually matters, which is whether decisions changed. Option D is least effective: rolling back to a model trained on older data responds to drift by moving further from the current distribution. Option C states a conclusion the evidence does not yet support.

**Question 4 (moderate) — A simpler model performs nearly as well**

A logistic regression achieves 89% accuracy where your gradient-boosted model achieves 91%. What is the most effective analysis?

- A) Use the more accurate model.
- B) Weigh the two points against what the simpler model buys — explainability to caseworkers and to people affected by decisions, faster inference, easier debugging when it behaves oddly, and a much lower maintenance burden — because in a public service those often outweigh two percentage points, and your role names deciding what model is most suitable rather than most accurate.
- C) Use the simpler model; explainability matters most.
- D) Ensemble the two.

**Correct answer: B. Least effective: D**

**Explanation:** Option B frames the decision as your role actually defines it — suitability rather than accuracy — and names the specific advantages that make simpler models frequently the right choice in government, where a decision affecting someone's benefits may need explaining to them. Option D is least effective: an ensemble adds the complexity of both models and the explainability of neither, for a marginal gain over the better one. Option C reaches a defensible conclusion by asserting a priority rather than weighing it. Option A optimises the metric rather than the decision.

**Question 5 (moderate) — An integration constraint**

The team integrating your model reports that its inference time is too slow for the transaction it sits in. What is the most effective response?

- A) Ask them to increase the timeout.
- B) Establish the actual budget available and work within it — through a smaller model, feature reduction, caching, or moving inference off the synchronous path — because an inference budget is a design constraint on model selection, not an obstacle to be negotiated away after the model is built.
- C) Optimise the model's implementation.
- D) Explain that the model needs the time it needs.

**Correct answer: B. Least effective: D**

**Explanation:** Option B treats latency as what it is — a requirement the model has to meet — and lists the routes, of which moving inference off the synchronous path is the one most often overlooked and frequently the best. Option D is least effective: it asserts an immovable constraint on the model's side of a boundary that is genuinely movable, and it puts the problem entirely on the other team. Option C is a good step within option B and may not close a large gap alone. Option A asks the transaction to absorb a cost users will feel.

**Question 6 (moderate) — A fairness concern raised late**

Days before deployment, a colleague suggests the model may perform worse for a particular group. What is the most effective response?

- A) Deploy and monitor for the issue.
- B) Test it before deploying, because the question is answerable with data you already have and the answer changes what you should do — and if the concern holds, deploying a model with known differential performance in a public service is a decision that must be made explicitly by someone accountable.
- C) Delay the deployment until it is resolved.
- D) Note the concern in the model documentation.

**Correct answer: B. Least effective: D**

**Explanation:** The concern is empirically checkable, usually within hours, and testing converts an uncomfortable question into a fact. Option B also names what happens if it holds — a risk decision belonging to an accountable person, not a judgement you make alone under deadline. Option D is least effective: recording a concern you could have resolved, and deploying anyway, is the version that looks worst in a subsequent review and helps nobody in the meantime. Option A monitors for something you could establish now. Option C may be the outcome and pre-empts the test that determines whether it is necessary.

**Question 7 (harder) — Pressure to over-claim**

A senior stakeholder wants to describe the model publicly as "95% accurate". The figure is from a balanced test set; the live class distribution is heavily skewed, making the number misleading. What is the most effective response?

- A) Allow it; the figure is technically correct.
- B) Explain concretely why it will mislead — on live data with this distribution a trivial baseline would score similarly, so the figure says nothing about the model's value — and offer a claim that is both true and stronger, such as what the model does better than the process it replaces.
- C) Refuse to allow the claim.
- D) Suggest adding a caveat about the test set.

**Correct answer: B. Least effective: A**

**Explanation:** Option B explains the problem in terms a non-specialist can act on and supplies a replacement claim, which is what stops the conversation becoming a refusal — a stakeholder wanting a strong public statement will accept a different strong statement far more readily than a subtraction. Option A is least effective: a misleading accuracy figure in public communication attracts scrutiny later, and you will be the person asked why it was allowed. Option D keeps the misleading headline behind a caveat nobody reads. Option C is right in substance and offers nothing.

**Question 8 (harder) — A model you inherited**

You take over a model in production with no documentation of how it was evaluated. What is the most effective response?

- A) Re-evaluate it from scratch on current data.
- B) Establish what it is being used for and what would happen if it were wrong, and let that determine how much assurance is needed — a model ranking internal search results needs far less than one contributing to a decision about a person — because "no documentation" is a risk whose size depends entirely on the use.
- C) Withdraw it until it can be assured.
- D) Document what you can reconstruct.

**Correct answer: B. Least effective: C**

**Explanation:** Option B proportions the response to the consequence, which is the judgement the situation actually requires — an undocumented model is not equally alarming everywhere. Option C is least effective as a first move: withdrawing a working production model on the basis of missing paperwork rather than a demonstrated fault may remove a service that is functioning, and the disruption is real. Option A is the right answer for a high-stakes use and disproportionate for a low-stakes one, which is what option B determines. Option D is useful and does not tell you whether the model is sound.

**Question 9 (harder) — A colleague's evaluation has a flaw**

Reviewing a colleague's work, you find their test set overlaps with their training data. They are more senior than you. What is the most effective response?

- A) Raise it directly, describing the overlap specifically and what it means for the reported figure.
- B) Approve it and mention the concern informally.
- C) Ask a third person to check whether you are right.
- D) Re-run the evaluation yourself and present the corrected figures.

**Correct answer: A. Least effective: B**

**Explanation:** Train-test contamination invalidates the reported performance entirely, which makes it a factual finding rather than a matter of opinion, and describing it specifically keeps the conversation technical regardless of seniority. Option B is least effective: letting an invalid evaluation stand while raising it informally means the figure circulates and gets used, and the informal mention provides no record. Option C is reasonable if you are genuinely unsure and, used to avoid the conversation, delays a clear finding. Option D is well-meant and takes over their work rather than telling them.

**Question 10 (harder) — Monitoring nobody asked for**

You want to add monitoring for subgroup performance on a live model. Nobody has requested it and there is no allocated time. What is the most effective response?

- A) Add it gradually alongside other work.
- B) Make the case with the specific risk — what could go undetected, for whom, and for how long — and put it to whoever owns the service as a prioritisation decision, because this competes for the same time as everything else and needs to be chosen rather than smuggled in.
- C) Raise it at a retrospective.
- D) Add a ticket to the backlog.

**Correct answer: B. Least effective: A**

**Explanation:** The risk is what makes this a decision rather than a preference, and naming who could be affected and for how long is what makes it land with a service owner. Option A is least effective: unsanctioned work alongside sanctioned work makes both slower, is invisible if it succeeds, and looks like a missed estimate if it does not. Option D puts an item in a queue nobody will prioritise without the argument. Option C surfaces it to the team rather than to the person who decides.

**Question 11 (harder) — A request that pushes a data boundary**

A product team asks you to train a model on a dataset whose sharing agreement permits use for a different purpose. What is the most effective response?

- A) Say the agreement does not cover it and stop there.
- B) Say the position clearly and get it resolved properly — either written agreement from the data controller, or a different dataset — because the boundary is not yours to interpret away, and a written permission takes days while an unpermitted use discovered later is a serious matter for the department.
- C) Train the model; the purposes are related.
- D) Ask the product team to check with legal.

**Correct answer: B. Least effective: C**

**Explanation:** Option B holds the line and supplies the route through it, which is what makes it constructive rather than obstructive — most of these situations are resolved by an email to the controller. Option C is least effective: interpreting a purpose limitation generously on your own judgement is exactly the decision that is not yours, and "the purposes are related" is how unlawful processing happens with good intentions. Option D routes the question to people who need your technical account of what would actually be done with the data. Option A is correct and unhelpful.

**Question 12 (harder) — Your own model is underperforming**

A model you built and championed is performing worse in production than the rules-based process it replaced. What is the most effective response?

- A) Raise it yourself, with the comparison, and propose how to establish whether the model can be improved or should be withdrawn.
- B) Investigate quietly and act if it holds up.
- C) Note it alongside the model's other benefits.
- D) Retrain and see whether performance recovers.

**Correct answer: A. Least effective: C**

**Explanation:** Option A is honest, and the reason is practical rather than moral: you are the person best placed to see it, the least suspected of motivated reasoning if you raise it, and the most damaged if somebody else does. Framing it as a question with two possible answers — improvable or withdrawable — keeps it a technical matter. Option C is least effective: changing the subject to offsetting benefits is the move that, once noticed, discounts everything you say afterwards. Option B looks like concealment if discovered. Option D is a reasonable technical step taken without telling anyone the model is currently doing worse than what it replaced.

### Preparation tips

- **Ask what an offline evaluation cannot tell you.**
- **Translate accuracy into how often, in which direction, and what happens to a person.**
- **Find the cause of drift before retraining.**
- **Decide model suitability, not model accuracy.**
- **Treat inference latency as a requirement on model selection.**
- **Test a fairness concern rather than documenting it.**
- **Proportion assurance to the consequence of being wrong.**
- **Raise problems with your own models yourself.**

### Common pitfalls to avoid

- **Treating a strong test result as a deployment decision.**
- **Answering a confidence question with an accuracy figure.**
- **Retraining before diagnosing drift.**
- **Ensembling to avoid choosing.**
- **Allowing a technically correct but misleading public claim.**
- **Approving an evaluation with train-test contamination.**
- **Interpreting a data purpose limitation generously.**
- **Doing unsanctioned monitoring work alongside committed work.**

## Conclusion

You have worked through four assessments pitched at senior machine learning engineer, and the threads are worth drawing together.

The cognitive section was about reasoning under the particular uncertainty this role carries — models whose behaviour is learned rather than specified, evaluated on data that is never quite the data they will meet. The recurring discipline was asking what a result does not establish.

The numeric section was the arithmetic that separates a real effect from an artefact: base rates, class imbalance, the difference between a metric moving and a decision changing, and the scale qualifiers that quietly multiply an answer by a thousand.

The verbal section was an exercise in reading evaluation and governance prose exactly. An unassessed dimension is not a clean one. "No evidence of degradation" plus small samples is undetermined, not absence. A condition on creating a derived dataset is not a release from retention terms. And a recommendation is not a predicted outcome.

The situational judgement section circled what makes this role distinctive: you are usually the only person who can evaluate what you are saying, working on systems whose failures are quiet and whose consequences land on people who will never know a model was involved. The strong answers translated technical figures into terms that could be acted on, tested the uncomfortable question rather than recording it, held a data boundary while supplying the route through it, and raised a problem with the speaker's own model before anyone else could.

If one thing is worth carrying away, it is the pattern behind the fairness question and the accuracy claim: in both, the honest move cost something immediately and very little compared with what the alternative costs later. You are frequently the only person positioned to see these, which makes reliably raising them a large part of what senior means here.

Good luck. This is demanding work at the point where statistics meets consequence, and the care you have given this is exactly right.
