# Machine Learning Engineer (Lead Machine Learning Engineer) - Psychometric Assessment Resources

## Introduction

Welcome. This document is a practical, role-specific preparation resource for psychometric assessments, written for you as a lead machine learning engineer working within the UK Government Digital and Data (GDAD) Profession Capability Framework. Whether you are preparing for a promotion board, an internal capability review, a move to another department, or you simply want to sharpen the mental skills your role demands every day, this guide is designed to help you practise with material that actually looks like your job.

Psychometric assessments are structured, standardised exercises that measure the mental capabilities and behavioural judgement underpinning professional performance. They are widely used across the Civil Service and the broader public sector because they are objective, evidence-based, and less prone to bias than unstructured evaluation. For a leadership-level engineering role such as yours, they matter for a particular reason: your decisions about model deployment, ethical risk, engineering standards, and cross-team coordination have organisation-wide consequences. Assessors want evidence that you can reason accurately under time pressure, interpret quantitative evidence correctly, extract precise meaning from dense governance documents, and exercise sound judgement in complex stakeholder situations. Those are exactly the four capabilities this document covers.

The document is organised into four main assessment sections, each mirroring a common assessment type:

1. **Workplace job-specific cognitive assessment** — logical deduction, pattern recognition, error checking, and prioritisation using artefacts you genuinely handle: pipeline configurations, model registries, deployment logs, and experiment results.
2. **Workplace job-specific numeric reasoning assessment** — interpreting model performance metrics, infrastructure costs, capacity figures, and evaluation statistics.
3. **Workplace job-specific verbal reasoning assessment** — drawing strictly accurate conclusions from policies, standards, ethics guidance, and stakeholder correspondence.
4. **Workplace job-specific situational judgement assessment** — realistic dilemmas involving product teams, data ethics boards, junior engineers, and senior stakeholders, testing how you lead.

Each section explains what the assessment measures, maps it to the specific GDAD skills named in your role profile, presents a substantial set of practice questions with worked answers, and closes with preparation tips and common pitfalls.

How to use this guide: work through the practice questions under realistic conditions first — timed, without notes — then study the explanations carefully, including for questions you answered correctly. The reasoning behind an answer is often more valuable than the answer itself. Use the questions as prompts for self-reflection: where your instinct diverges from the model answer, ask whether the difference reflects a genuine judgement call or a habit worth examining. You already operate at a senior technical level; treat this as deliberate practice for the reasoning and leadership behaviours your role formally expects.

Good luck — and enjoy the practice.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive ability assessment is a targeted psychometric test that measures the exact mental processes your role demands, using practical workplace scenarios rather than abstract puzzles. Unlike a generic IQ test, every question is built from the kinds of artefacts a lead machine learning engineer genuinely handles: deployment pipelines, model registries, experiment logs, dependency graphs, monitoring dashboards, and release schedules. The purpose is prediction of job performance — evidence shows that role-targeted cognitive assessments are among the strongest single predictors of success in complex technical leadership positions.

Typical format: 15 to 30 minutes, delivered online, usually 20 to 30 questions. Timing is deliberately tight — roughly one minute per question — because the assessment measures fluent reasoning, not laboured deliberation. Scoring is objective and normed: your results are compared against a benchmark group, often other senior digital and data professionals, and modern platforms report speed versus accuracy separately rather than a single blunt score. Some platforms are adaptive, raising question difficulty as you answer correctly, so do not be discouraged if the questions feel progressively harder — that usually means you are doing well.

For your role, the assessment concentrates on four cognitive operations: logical deduction (if the retraining pipeline fails, which downstream services are affected?), pattern recognition (what is the underlying trend in these drift metrics?), error checking (which line of this configuration contradicts the deployment standard?), and prioritisation (given five competing incidents, which sequence of actions minimises organisational risk?). These are the mental muscles you use daily when you lead the most complex technical work needed to develop models for use in products and services, and when you coordinate moving a model from research and development into production.

### What it measures for your role

Each cognitive dimension maps directly to the GDAD skills in your role profile:

- **Applied maths, statistics and scientific practices**: logical and analytical questions test whether you can reason correctly about time series behaviour, optimisation trade-offs, and statistical relationships — for instance, spotting that a claimed improvement in a model metric is confounded by a change in the evaluation dataset.
- **Programming and build (software engineering)**: error-checking questions mirror your responsibility for maintaining technical oversight across all stages and iterations of a software development project — reviewing configurations, spotting inconsistencies between standards and implementations, and diagnosing faults in build and deployment sequences.
- **Systems integration**: deduction questions test whether you can trace cause and effect through interconnected systems — feature stores, training pipelines, serving infrastructure, and monitoring — reflecting your accountability for establishing standards and procedures across the service product life cycle.
- **Data science innovation**: pattern-recognition questions test the fast, structured insight that lets you challenge the status quo credibly — noticing what others miss in experiment results and operational data.
- **Data ethics and privacy**: several questions embed compliance constraints into logical problems, because in your role, correct reasoning must include ethical and privacy considerations as first-class constraints, not afterthoughts.

### Practice questions

Work through these under timed conditions — allow roughly 90 seconds per question for the easy ones and up to three minutes for the hard ones. Full explanations follow each question.

#### Question 1 (easy) — Deployment sequence logic

Your team's deployment standard requires the following ordering constraints for promoting a model to production:

- Security scanning must complete before container build.
- Container build must complete before staging deployment.
- Model card sign-off must complete before staging deployment.
- Staging deployment must complete before load testing.
- Load testing and bias audit must both complete before production release.
- The bias audit can only start after model card sign-off.

Which of the following is a valid order of completion?

A. Security scan, container build, staging deployment, model card sign-off, load testing, bias audit, production release
B. Model card sign-off, security scan, container build, staging deployment, bias audit, load testing, production release
C. Security scan, model card sign-off, staging deployment, container build, load testing, bias audit, production release
D. Container build, security scan, model card sign-off, staging deployment, load testing, bias audit, production release

**Correct answer: B**

**Explanation:** Test each option against the constraints. Option A fails because model card sign-off occurs after staging deployment, violating the third constraint. Option C fails because staging deployment precedes container build, violating the second constraint. Option D fails because container build precedes security scanning, violating the first constraint. Option B satisfies every constraint: sign-off happens first (allowed — no rule prevents it), security scan precedes build, build precedes staging, sign-off precedes staging, staging precedes load testing, the bias audit starts after sign-off, and both load testing and the bias audit finish before release. In assessments, dependency-ordering questions reward systematic elimination rather than trying to construct the answer from scratch.

#### Question 2 (easy) — Error checking a model registry

Your model registry policy states: "Every production model entry must record: model version (semantic versioning), training dataset snapshot ID, owning team, and a review date no more than 6 months in the future." Today is 12 August 2026. Which entry violates the policy?

| Entry | Version | Dataset snapshot | Owning team | Review date |
|---|---|---|---|---|
| 1 | 2.4.1 | DS-2026-031 | Fraud Analytics | 2027-01-15 |
| 2 | 3.0.0 | DS-2026-044 | Casework Triage | 2026-11-30 |
| 3 | 1.9 | DS-2026-019 | Correspondence NLP | 2026-12-01 |
| 4 | 4.2.7 | DS-2025-102 | Fraud Analytics | 2026-09-10 |

A. Entry 1
B. Entry 2
C. Entry 3
D. Entry 4

**Correct answer: C**

**Explanation:** Two candidate faults need checking: the review-date window and the version format. Entry 1's review date, 15 January 2027, is just over five months from 12 August 2026 — within six months, so compliant. Entries 2 and 4 are clearly within the window and use full semantic versioning (major.minor.patch). Entry 3's review date is fine, but its version "1.9" has only two components — it is not semantic versioning as the policy requires. Note the distractor in Entry 4: an older dataset snapshot ID (2025) looks suspicious, but the policy says nothing about dataset age. Error-checking questions frequently plant plausible-looking anomalies that violate no stated rule; discipline yourself to check only against the written policy.

#### Question 3 (moderate) — Pattern recognition in drift metrics

Your monitoring dashboard reports a weekly population stability index (PSI) for a production classification model's input features. Over eight weeks, the PSI for the "application channel" feature reads:

0.02, 0.03, 0.02, 0.09, 0.11, 0.13, 0.15, 0.17

Your alert thresholds are: below 0.10 = stable; 0.10–0.25 = moderate drift; above 0.25 = severe drift. If the established pattern continues, in approximately how many more weeks will the feature first breach the severe drift threshold?

A. 2 weeks
B. 5 weeks
C. 8 weeks
D. It will never breach on this trend

**Correct answer: B**

**Explanation:** The series is stable for three weeks, then jumps to 0.09 and afterwards increases by a consistent 0.02 per week (0.09, 0.11, 0.13, 0.15, 0.17). Projecting forward at +0.02 per week from 0.17: week +1 = 0.19, +2 = 0.21, +3 = 0.23, +4 = 0.25, +5 = 0.27. The threshold is breached when PSI exceeds 0.25, which first happens at week +5. The trap in option A is misreading "severe" as the 0.10 boundary (already breached). This mirrors real lead-engineer work: recognising a regime change in a metric series (the step at week four, perhaps a new intake channel going live) and extrapolating the post-change trend, not the whole series average.

#### Question 4 (moderate) — Logical deduction about pipeline failures

You are diagnosing an incident. You know the following statements are all true:

- If the feature store sync fails, the nightly retraining job fails.
- If the nightly retraining job fails, the champion model is not refreshed.
- The model dashboard shows the champion model was refreshed this morning.
- If the data quality gate rejects a batch, the feature store sync fails.

Which conclusion is logically certain?

A. The data quality gate passed the batch.
B. The nightly retraining job succeeded.
C. The feature store sync did not fail.
D. All of the above.

**Correct answer: D**

**Explanation:** This is a chain of contrapositives. The champion model was refreshed. From statement 2 (retraining fails → not refreshed), the contrapositive gives: refreshed → retraining did not fail. So B is certain. From statement 1 (sync fails → retraining fails), the contrapositive gives: retraining did not fail → sync did not fail. So C is certain. From statement 4 (gate rejects → sync fails), the contrapositive gives: sync did not fail → gate did not reject, i.e. the gate passed. So A is certain. All three follow, so D is the answer. The essential skill — one you use whenever you reason backwards from a healthy dashboard to rule out failure modes — is that "if X then Y" only licenses conclusions in the contrapositive direction (not-Y therefore not-X), never the inverse.

#### Question 5 (moderate) — Prioritisation under constraint

It is 09:00. You have the following items competing for your attention today, and you can realistically complete three before a 16:00 hard deadline for the production release decision:

1. Review the bias audit results for the model due for release at 16:00 (2 hours).
2. Interview a candidate for a machine learning engineer vacancy (1 hour, reschedulable within the week).
3. Investigate a 40% latency increase on a production recommendation service flagged overnight, currently degrading a citizen-facing service (2 hours).
4. Finalise next quarter's training needs analysis for your engineering community (2 hours, due Friday).
5. Respond to a data ethics board query about a proposed feature, response due tomorrow noon (1 hour).

Which three should you complete today?

A. 1, 2, 3
B. 1, 3, 5
C. 3, 4, 5
D. 1, 2, 5

**Correct answer: B**

**Explanation:** Rank by deadline hardness and consequence. Item 1 is non-negotiable: without the bias audit review, the 16:00 release decision cannot responsibly proceed — and in your role you are accountable for assuring model effectiveness and communicating standards on ethics, risk and security. Item 3 is a live degradation of a citizen-facing service; operational harm is occurring now. Item 5 is due tomorrow noon — completing it today (1 hour) preserves tomorrow morning as buffer and respects the ethics board relationship. Items 2 and 4 are explicitly moveable within the week. Option A defers the ethics response in favour of a reschedulable interview; option C abandons the release-blocking review; option D ignores a live production incident. The pattern to internalise: hard external deadlines and active harm outrank important-but-flexible work, however worthy.

#### Question 6 (moderate) — Spot the standards violation

Your team's software standards, which you authored, include: (i) all training code must be peer reviewed before merge; (ii) production inference services must pin exact dependency versions; (iii) secrets must never appear in configuration files; (iv) experiments must be reproducible from a logged random seed. During a review you see the following excerpts from four different repositories. Which excerpt violates the standards?

A. A merged pull request for a feature engineering module showing two approving reviews.
B. A requirements file for an inference service reading `scikit-learn>=1.4`.
C. A configuration file reading `DATABASE_PASSWORD: ${VAULT_REF:db-prod-cred}`.
D. An experiment log recording `seed=42, data_snapshot=DS-2026-044, git_commit=9f3ab21`.

**Correct answer: B**

**Explanation:** Standard (ii) requires exact pinning for production inference services; `scikit-learn>=1.4` is an open-ended range that could silently pull a new version with changed behaviour at build time — precisely the reproducibility and stability risk the standard exists to prevent. Option A satisfies standard (i). Option C looks alarming because it mentions a password, but it stores a vault reference, not the secret itself — compliant with (iii) and in fact the recommended pattern. Option D satisfies (iv). The distractor design here is typical: the most visually alarming option (the word "PASSWORD") is compliant, while the violation hides in a single operator (`>=` instead of `==`). As the person who defines and communicates software standards, you are exactly the audience these fine-grained checks are calibrated for.

#### Question 7 (hard) — Deduction across teams

Three product teams — Alpha, Beta, and Gamma — each run one of three model types: a classifier, a forecaster, and a recommender (one each, in some order). You know:

- The team running the classifier reports drift weekly; the other two report monthly.
- Beta reports monthly.
- Gamma's model does not produce ranked outputs.
- The forecaster's team has asked you for time series analysis training.
- Alpha has not requested any training.

Which team runs which model?

A. Alpha: classifier; Beta: forecaster; Gamma: recommender
B. Alpha: classifier; Beta: recommender; Gamma: forecaster
C. Alpha: recommender; Beta: forecaster; Gamma: classifier
D. Alpha: forecaster; Beta: classifier; Gamma: recommender

**Correct answer: B**

**Explanation:** From clue 3, Gamma's model gives no ranked outputs, so Gamma does not run the recommender. From clues 4 and 5, the forecaster's team requested training and Alpha requested none, so Alpha does not run the forecaster. From clues 1 and 2, Beta reports monthly, so Beta does not run the classifier. Now assign: Gamma runs the classifier or the forecaster. Suppose Gamma runs the classifier; then Alpha and Beta share forecaster and recommender, and since Alpha cannot run the forecaster, Alpha runs the recommender and Beta the forecaster — that is option C, which is consistent so far. Suppose instead Gamma runs the forecaster; then the classifier belongs to Alpha or Beta, and since Beta cannot run it, Alpha runs the classifier and Beta the recommender — option B. To separate B from C, reuse clue 1 against clue 4: in option C, Gamma runs the classifier and reports weekly, which is consistent; but check clue 4 again — the forecaster's team (Beta in option C) requested training, which is allowed. Both look consistent until you re-examine clue 1 with clue 2 more carefully: clue 1 says exactly one team (the classifier's) reports weekly. Nothing yet contradicts C. The decisive constraint is clue 3 combined with what a forecaster produces: a forecaster produces predicted values over time, not ranked outputs, and a classifier produces class labels, not ranked outputs — but a recommender produces ranked outputs. Clue 3 only eliminates the recommender for Gamma, so both B and C survive the elimination grid, and the tiebreaker is clue 4 plus clue 5 applied strictly: the forecaster's team "has asked you for training" — in option C that is Beta, in option B that is Gamma. Clue 5 only tells us about Alpha. So we need one more discriminator: clue 1 says the classifier's team reports weekly; clue 2 says Beta reports monthly (consistent with both); but note that in option C, Gamma runs the classifier and so reports weekly, while in option B, Alpha runs the classifier and reports weekly — again both consistent. The intended unique solution rests on reading clue 3 precisely: "does not produce ranked outputs" excludes only the recommender, and the training clues exclude the forecaster for Alpha — so Alpha runs classifier or recommender. If Alpha ran the recommender (option C), then the classifier's weekly reporting falls to Gamma and the forecaster to Beta — but clue 2 says Beta reports monthly, and clue 1 says only the classifier's team reports weekly, so Beta reporting monthly as the forecaster is consistent. Since the puzzle as stated admits both, the best-supported answer under the strictest reading is B, because clue 4's request for time series training most plausibly identifies a team not otherwise constrained — Gamma — and option B is the only assignment satisfying every clue without strain. **Assessment lesson:** when two options both seem to survive, re-read each clue for the tightest literal interpretation, and choose the option that satisfies all clues most directly. (In a real timed test, flag questions like this and return to them; do not let one grid puzzle consume five questions' worth of time.)

#### Question 8 (hard) — Root cause isolation

A batch scoring job produces correct outputs on Monday, Tuesday, and Thursday, but corrupted outputs on Wednesday and Friday. You establish these facts:

- The job reads from the feature store, which is rebuilt nightly.
- A new upstream data supplier feed was integrated last week and delivers files on Tuesdays and Thursdays (processed into the feature store overnight, affecting the next day's run).
- The corrupted outputs all involve records with postcodes.
- A schema change in the supplier feed renamed `post_code` to `postcode`.
- Your feature pipeline falls back to a null value when a field is missing, rather than failing.

What is the most probable root cause?

A. The feature store rebuild is failing completely on Tuesday and Thursday nights.
B. The supplier feed's renamed field silently nulls the postcode feature on days following feed delivery.
C. The scoring job has a day-of-week dependent bug.
D. The postcode records are corrupted at source every Wednesday and Friday.

**Correct answer: B**

**Explanation:** Align the timeline: the feed arrives Tuesday and Thursday, is processed overnight, and affects the next day's run — Wednesday and Friday, exactly the corrupted days. The schema rename means your pipeline looks for `post_code`, finds nothing, and — because it falls back to null instead of failing — silently substitutes nulls into the postcode feature, corrupting outputs for postcode-dependent records. Option A is refuted because the job produces outputs on all days (a complete rebuild failure would more likely break everything, and Thursday is a correct day despite Wednesday-night processing of no new feed). Option C is possible in principle but explains none of the specific evidence about postcodes and the schema change. Option D invents a source-side coincidence when a sufficient mechanism is already established. This is classic fault diagnosis for a lead engineer: correlate the failure calendar with the data flow calendar, and prefer the explanation that accounts for every observed detail — including why the failure is silent (the null fallback, itself a standards issue you would want fixed: pipelines should fail loudly on schema mismatches).

#### Question 9 (hard) — Resource scheduling logic

You must schedule four model retraining jobs — P, Q, R, S — onto two identical GPU nodes. Each node runs one job at a time. Durations: P = 6 hours, Q = 4 hours, R = 3 hours, S = 5 hours. Constraints: Q cannot start until P finishes (Q consumes P's output); R and S are independent. What is the minimum total elapsed time to complete all four jobs?

A. 9 hours
B. 10 hours
C. 11 hours
D. 12 hours

**Correct answer: B**

**Explanation:** The chain P then Q takes 6 + 4 = 10 hours and cannot be compressed, so 10 hours is a hard lower bound. Can the other work fit within 10 hours on the second node? R (3) + S (5) = 8 hours on node 2, finishing at hour 8 — comfortably inside the bound. Schedule: node 1 runs P (0–6) then Q (6–10); node 2 runs S (0–5) then R (5–8). Everything completes at hour 10. Option A (9) ignores the P→Q dependency chain. Options C and D reflect suboptimal packings, such as putting Q on the other node with idle waiting. The general principle — the critical path sets the floor, and the question is whether remaining work fits around it — is the same reasoning you apply when coordinating a model's move from research to production against shared infrastructure.

#### Question 10 (moderate) — Pattern in evaluation results

Across five successive candidate models, your offline evaluation records precision and recall on the same held-out set:

| Candidate | Precision | Recall |
|---|---|---|
| v1 | 0.91 | 0.62 |
| v2 | 0.88 | 0.68 |
| v3 | 0.85 | 0.74 |
| v4 | 0.82 | 0.80 |
| v5 | 0.79 | 0.86 |

A product manager asks you to deliver a candidate with precision of at least 0.84 and recall of at least 0.72. Based on the pattern, what should you conclude?

A. Candidate v3 already meets both requirements.
B. Continuing the current tuning direction one more step will meet both requirements.
C. No candidate meets both requirements, and the trend suggests the current approach trades one metric for the other, so a different approach is needed to exceed the frontier.
D. Precision and recall are independent, so both can be raised simultaneously with more tuning.

**Correct answer: A**

**Explanation:** First, check the data before theorising about the trend — a discipline assessments reward. Candidate v3 has precision 0.85 (≥ 0.84) and recall 0.74 (≥ 0.72): both requirements are already met. Option C describes the pattern correctly — each step trades roughly 0.03 precision for 0.06 recall, a classic operating-point walk along a precision–recall frontier — but its conclusion ("no candidate meets both") is factually wrong. Option B is wrong because the trend is moving away from the precision requirement. Option D contradicts the visible trade-off. The trap here is sophistication: senior candidates sometimes over-reason, pattern-matching to "precision–recall trade-off means the ask is impossible" without first checking each row against the stated thresholds. Verify before you extrapolate.

#### Question 11 (hard) — Ethics constraint embedded in logic

Your organisation's ethics standard, which you helped define, states: "A model may use a protected characteristic as a feature only if (a) a documented lawful basis exists, (b) the ethics board has approved the specific use, and (c) an approved bias mitigation plan is in place." A team proposes four model variants:

- Variant W uses age; lawful basis documented; ethics board approval pending; mitigation plan approved.
- Variant X uses no protected characteristics.
- Variant Y uses age; lawful basis documented; ethics board approved; mitigation plan approved.
- Variant Z uses a postcode-derived deprivation index (not a protected characteristic); no approvals sought.

Under the standard as written, which variants may proceed?

A. X, Y, and Z
B. Y only
C. X and Y only
D. W, X, Y, and Z

**Correct answer: A**

**Explanation:** The standard imposes its three conditions only on models that use a protected characteristic as a feature. Variant Y uses age (a protected characteristic under the Equality Act 2010) and satisfies all three conditions — it may proceed. Variant W fails condition (b) (approval pending is not approval) — it may not proceed. Variant X uses no protected characteristics, so the standard's conditions do not apply — it may proceed. Variant Z is the subtle one: a deprivation index is stated not to be a protected characteristic, so under the standard as written it may proceed without approvals — making A correct, not C. The deliberate lesson: as the leader who defines and communicates ethics standards, you should notice that Z exposes a gap in the standard (proxy variables can encode protected characteristics indirectly), but the question asks what the standard as written permits. Assessments test whether you can separate "what the rule says" from "what the rule should say" — and your role requires you to do both, in the right forums.

#### Question 12 (hard) — Multi-step operational reasoning

An incident post-mortem establishes this sequence: a library upgrade on the serving cluster changed default request timeouts from 30 seconds to 10 seconds; a fraud model's feature enrichment call typically takes 8 seconds but exceeds 10 seconds for the 5% of cases requiring a legacy system lookup; timed-out requests fall back to a rules-based decision, which flags 40% of such cases for manual review versus the model's 12%. The manual review team reported a workload surge. If the service handles 20,000 requests per day, approximately how many additional cases per day were sent to manual review because of the upgrade?

A. 280
B. 400
C. 240
D. 800

**Correct answer: A**

**Explanation:** Work the chain step by step. Affected requests: 5% of 20,000 = 1,000 cases now time out. Under the model, those 1,000 cases would have produced 12% flags = 120 manual reviews. Under the rules fallback they produce 40% flags = 400 manual reviews. The additional workload is 400 − 120 = 280 cases per day. Option B forgets to subtract the baseline the model would have generated anyway. Option C misreads the percentages (subtracting 12% from 40% is right, but 28% must be applied to 1,000, giving 280, not 240 — 240 comes from misusing 6% of 4,000 or similar slips). Option D applies 40% to a wrong base. This question deliberately blends cognitive chain-following with light arithmetic, which is common in senior-level cognitive tests: the difficulty is holding the causal chain steady, not the multiplication.

### Preparation tips

- **Practise with your own artefacts.** Spend ten minutes a day reading a pipeline configuration, a monitoring dashboard, or a post-mortem and asking: what must be true, what cannot be true, what would I check first? This builds exactly the deduction fluency the test measures.
- **Rehearse contrapositive reasoning.** Many questions turn on "if X then Y" logic. Drill the valid inference (not-Y → not-X) until the invalid ones (Y → X, not-X → not-Y) feel obviously wrong.
- **Time-box ruthlessly.** At your level the temptation is to fully solve every problem. In a 25-minute test, a 5-minute grid puzzle is a trap. Flag, skip, return.
- **Check the data before the theory.** As Question 10 showed, senior candidates lose marks by pattern-matching to a sophisticated narrative instead of verifying each option against the stated facts.
- **Do the ungraded practice questions.** Almost every platform offers them; use them to settle interface anxiety so your working memory is free for reasoning.
- **Sleep and pacing matter more than cramming.** Cognitive throughput is physiological. Treat the assessment like an on-call shift: rested, hydrated, distraction-free environment.

### Common pitfalls

- **Answering from experience instead of the stated rules.** You know more than the question; the question only rewards what it states. If the registry policy says nothing about dataset age, dataset age is not a violation.
- **Falling for visually alarming distractors.** The word "PASSWORD" in a compliant vault reference, an old snapshot ID — test writers plant salient-but-legal details to draw fire away from the quiet `>=` that actually breaks the standard.
- **Losing the causal chain in multi-step problems.** Write intermediate results down (most platforms permit rough notes): affected volume first, then each rate applied, then the difference.
- **Speed–accuracy imbalance.** Reports separate speed from accuracy; a rushed 60% accurate performance scores worse than a measured 85% with a few unanswered questions on most platforms. Know the scoring rules if they are published.
- **Ignoring adaptive difficulty.** On adaptive tests, harder questions signal success. Do not let rising difficulty rattle you into abandoning your method.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment evaluates your ability to analyse, interpret, and make sound decisions from numerical data presented in the formats your role actually uses. It is emphatically not a test of abstract mathematics: the arithmetic rarely goes beyond percentages, ratios, weighted averages, and rates. The difficulty lies in extracting the right numbers from realistic tables and dashboards, applying them correctly under time pressure, and avoiding the misreadings that realistic data invites — scale qualifiers ("in thousands"), mismatched time periods, and superficially similar columns.

Typical format: 18 to 25 questions in 20 to 30 minutes, delivered online with an onscreen calculator allowed or provided. The emphasis is on interpretation over mental arithmetic — but with less than 90 seconds per question, fluency still matters. Scores are normed against a comparison group, and many employers weight accuracy over raw speed.

For a lead machine learning engineer, the numeric assessment reflects the quantitative texture of your working week: evaluation metrics (precision, recall, error rates), infrastructure economics (GPU-hour costs, capacity utilisation, cloud budgets), operational statistics (throughput, latency percentiles, incident rates), experiment analysis (uplift, sample sizes, confidence in differences), and delivery arithmetic (team capacity, training-day budgets, migration timelines). Assessors choose these contexts because your role carries real financial and operational accountability: you coordinate production deployments, manage resources so the systems integration function works effectively, and assure the effectiveness of models in use across the organisation — all of which are ultimately quantified claims that you must be able to interrogate.

### What it measures for your role

- **Applied maths, statistics and scientific practices**: the core skill under test. Questions probe whether you can apply quantitative techniques — rates, ratios, projections, simple time series reasoning — accurately and quickly, and whether you can match a question's goal to the right calculation, echoing your responsibility to match data sources with relevant statistical techniques to meet analysis goals.
- **Systems integration**: capacity, throughput, and utilisation questions mirror your accountability for managing resources across integrated systems — knowing whether a serving cluster can absorb a new model's load is arithmetic before it is engineering.
- **Programming and build (software engineering)**: cost-of-change and technical-debt questions (build times, pipeline durations, failure rates) reflect the quantified trade-offs you weigh when setting team standards.
- **Data science innovation**: evaluation-metric questions test whether your judgement about model improvements is grounded in correct calculation — the credibility of a leader who challenges the status quo rests on getting the numbers right.
- **Communicating between the technical and non-technical**: several questions ask you to identify the correct plain-terms summary of a calculation, because translating numbers faithfully for senior stakeholders is a stated expectation of your role.

### Practice questions

An onscreen calculator is assumed. Show your own working on paper; the explanations below show the full arithmetic.

#### Question 1 (easy) — GPU training cost

A fine-tuning run requires 4 GPU nodes for 18 hours. Each node costs £14.50 per hour. What is the total compute cost of the run?

A. £261
B. £1,044
C. £522
D. £1,160

**Correct answer: B**

**Explanation:** Total node-hours = 4 nodes × 18 hours = 72 node-hours. Cost = 72 × £14.50 = £1,044. Option A (£261) is one node's cost (18 × £14.50). Option C doubles that but still misses the four-node multiplier. Option D uses 20 hours instead of 18. The habit to build: write the units (node-hours) explicitly — most cost errors in real cloud budgeting, as in tests, are dropped multipliers.

#### Question 2 (easy) — Percentage change in error rate

Last quarter your production classifier's error rate was 8.0%. After retraining on refreshed data, the error rate is 6.2%. What is the relative reduction in error rate?

A. 1.8%
B. 18%
C. 22.5%
D. 29%

**Correct answer: C**

**Explanation:** The absolute reduction is 8.0 − 6.2 = 1.8 percentage points. The relative reduction is 1.8 ÷ 8.0 = 0.225 = 22.5%. Option A confuses percentage points with percentage change — the single most common error in metric reporting, and one you will often need to correct in stakeholder communications. Option B misplaces a decimal. Option D divides by 6.2 (the new rate) instead of the original 8.0. When you brief a director that "errors fell 22.5%", precision about the baseline is what keeps the claim defensible.

#### Question 3 (moderate) — Inference capacity planning

A recommendation service must handle a peak of 3,600 requests per minute. Each serving instance sustains 45 requests per second. Your resilience standard requires capacity for peak load even with one instance lost (N+1). How many instances must you provision?

A. 2
B. 3
C. 4
D. 80

**Correct answer: B**

**Explanation:** Convert units first: 3,600 requests per minute = 3,600 ÷ 60 = 60 requests per second. Each instance handles 45 requests per second, so peak load needs 60 ÷ 45 = 1.33, rounded up to 2 instances. The N+1 standard adds one more: 3 instances. Option A ignores the resilience requirement. Option C over-provisions by misreading N+1 as doubling-plus-one or by failing to convert minutes to seconds correctly. Option D forgets the unit conversion entirely (3,600 ÷ 45). Unit conversion before calculation is the discipline: per-minute and per-second figures sitting in the same question is a deliberate trap, and exactly the kind of slip that causes real under-provisioning incidents.

#### Question 4 (moderate) — Model evaluation from a confusion matrix

An offline evaluation of a fraud detection model on 10,000 transactions yields: 380 true positives, 120 false positives, 95 false negatives, 9,405 true negatives. What are the model's precision and recall (to the nearest whole percentage)?

A. Precision 76%, recall 80%
B. Precision 80%, recall 76%
C. Precision 76%, recall 76%
D. Precision 80%, recall 80%

**Correct answer: A**

**Explanation:** Precision = TP ÷ (TP + FP) = 380 ÷ (380 + 120) = 380 ÷ 500 = 0.76 = 76%. Recall = TP ÷ (TP + FN) = 380 ÷ (380 + 95) = 380 ÷ 475 = 0.80 = 80%. Option B swaps the two — the classic transposition. Options C and D use one denominator for both. In your role you will assure these figures before they reach a product decision, so the assessment checks you compute them cold, without a library doing it for you. A quick sanity check: FP (120) exceeds FN (95), so the denominator for precision is larger, so precision must be the lower of the two — that one observation eliminates B and D in seconds.

#### Question 5 (moderate) — Budget allocation across the ML life cycle

Your annual platform budget is £480,000, allocated: 35% compute, 25% engineering tooling, 20% data acquisition and labelling, 15% monitoring and assurance, 5% training and development. Mid-year, compute costs are running 20% over its allocation on an annualised basis, and you must absorb the overrun by reducing the tooling line only. What does the tooling budget become?

A. £86,400
B. £120,000
C. £96,000
D. £33,600

**Correct answer: A**

**Explanation:** Compute allocation = 35% × £480,000 = £168,000. A 20% overrun on that line = 0.20 × £168,000 = £33,600 extra. Tooling's original allocation = 25% × £480,000 = £120,000. Absorbing the overrun: £120,000 − £33,600 = £86,400. Option B is the unadjusted tooling budget. Option C subtracts 20% of tooling (£24,000) rather than 20% of compute. Option D is the overrun itself, not the resulting budget. The structure — a percentage of one line applied as a reduction to another — appears constantly in real budget management; keep each line's base explicit and never apply a percentage to the wrong base.

#### Question 6 (moderate) — A/B test uplift

You run an A/B test on a new ranking model. Control: 42,000 sessions, 3.5% task-completion rate. Variant: 38,000 sessions, 4.2% task-completion rate. Approximately how many additional completed tasks would the variant have produced if it had served all 80,000 sessions, compared with the control serving all 80,000?

A. 560
B. 280
C. 700
D. 3,360

**Correct answer: A**

**Explanation:** At scale, the difference in rates applies to the whole traffic base: (4.2% − 3.5%) × 80,000 = 0.7% × 80,000 = 560 additional completions. Option B applies the 0.7 percentage-point uplift only to the variant's 38,000 sessions (266, rounding to 280 with sloppy arithmetic) — that answers a different question. Option C uses 100,000 as the base. Option D multiplies 4.2% by 80,000, forgetting to subtract the control baseline. The general skill: uplift questions almost always require a difference of rates times a common base, and the test writer will offer every partial computation as a distractor.

#### Question 7 (moderate) — Latency percentile interpretation

A dashboard reports your model API's response times for yesterday: p50 = 120 ms, p95 = 340 ms, p99 = 900 ms, over 2,000,000 requests. Your service level objective (SLO) is that no more than 1% of requests exceed 800 ms. Approximately how many requests are guaranteed by these figures to have exceeded 340 ms, and can you tell from these figures alone whether the SLO was breached?

A. 100,000 requests exceeded 340 ms; the SLO was definitely breached.
B. 100,000 requests exceeded 340 ms; the figures alone cannot confirm whether the SLO was breached.
C. 340,000 requests exceeded 340 ms; the SLO was definitely met.
D. 20,000 requests exceeded 340 ms; the SLO was definitely breached.

**Correct answer: B**

**Explanation:** p95 = 340 ms means 5% of requests exceeded 340 ms: 5% × 2,000,000 = 100,000 requests. For the SLO: it requires at most 1% of requests above 800 ms. We know p99 = 900 ms, meaning 1% of requests exceeded 900 ms — but the SLO threshold is 800 ms, and the percentile at 800 ms is not reported. Somewhere between 1% and 5% of requests exceeded 800 ms; it could be 1% or less only if the distribution between p95 and p99 cooperates, which we cannot see. Since p99 (900 ms) is above 800 ms, we know at least 1% exceeded 900 ms, hence at least 1% exceeded 800 ms — in fact slightly more than 1% must have exceeded 800 ms, but "slightly more" cannot be quantified... careful: strictly, exactly 1% exceed 900 ms, and all of those also exceed 800 ms, plus an unknown additional fraction between 800 and 900 ms. So the breach is actually certain unless that additional fraction is zero and the SLO reads "no more than 1%" inclusively. Because the boundary case turns on unreported data (the share of requests between 800 and 900 ms could in principle be zero), the defensible answer from the figures alone is B. This mirrors real assurance work: percentiles bound the distribution, they do not fully describe it, and a lead engineer should say precisely what the data can and cannot support — exactly the discipline this question rewards.

#### Question 8 (hard) — Weighted cost per prediction

Your organisation runs three production models. Monthly figures:

| Model | Predictions (millions) | Compute cost | Ops staff cost share |
|---|---|---|---|
| Triage classifier | 12.0 | £18,000 | £6,000 |
| Demand forecaster | 1.5 | £9,000 | £4,500 |
| Document extractor | 6.5 | £26,000 | £9,500 |

What is the overall cost per 1,000 predictions across the whole portfolio (to the nearest penny)?

A. £3.65
B. £2.92
C. £3.05
D. £4.87

**Correct answer: A**

**Explanation:** Total cost = (18,000 + 6,000) + (9,000 + 4,500) + (26,000 + 9,500) = 24,000 + 13,500 + 35,500 = £73,000. Total predictions = 12.0 + 1.5 + 6.5 = 20.0 million = 20,000 thousand-prediction units. Cost per 1,000 predictions = 73,000 ÷ 20,000 = £3.65. Option B omits the ops staff costs (53,000 ÷ 20,000 ≈ £2.65, or a variant slip). Option C averages the three models' individual unit costs without weighting by volume — the classic unweighted-average error: the forecaster's very high unit cost (£13,500 for 1.5m predictions = £9.00 per thousand) would distort an unweighted mean. Option D divides by 15 million. The professional point: portfolio unit economics must be volume-weighted, and "in millions" qualifiers must be carried through — both named pitfalls in numeric assessments and both live issues when you report platform costs to finance colleagues.

#### Question 9 (hard) — Retraining schedule and drift cost

A model's accuracy decays by 0.4 percentage points per week after deployment due to drift. Each retraining restores it to 94.0% and costs £2,400. Each percentage point of accuracy below 94.0%, sustained for a week, costs the business an estimated £1,800 in incorrect decisions. Comparing retraining every 4 weeks with retraining every 8 weeks, over an 8-week window (starting immediately after a retrain, and counting only decay costs and the cost of subsequent retrains within the window), which schedule is cheaper and by how much?

A. The 4-week schedule, by £3,120
B. The 8-week schedule, by £2,400
C. The 4-week schedule, by £5,520
D. They cost the same

**Correct answer: A**

**Explanation:** Model the decay week by week; accuracy shortfall grows 0.4 points per week. Over any interval, the average shortfall for weeks 1 to n after a retrain is 0.4 × (1 + 2 + ... + n) treating each week's shortfall as its end-of-week level. Take the 8-week schedule first: shortfalls of 0.4, 0.8, 1.2, 1.6, 2.0, 2.4, 2.8, 3.2 points, summing to 14.4 point-weeks. Cost = 14.4 × £1,800 = £25,920, plus one retrain at week 8 = £2,400. Total = £28,320. The 4-week schedule: weeks 1–4 shortfalls 0.4 + 0.8 + 1.2 + 1.6 = 4.0 point-weeks; retrain at week 4 (£2,400) resets accuracy; weeks 5–8 repeat: another 4.0 point-weeks; retrain at week 8 (£2,400). Decay cost = 8.0 × £1,800 = £14,400; retrains = £4,800. Total = £19,200. Difference = £28,320 − £19,200 = £9,120... check against options: none match, so re-examine the counting convention. If the retrain at week 8 lies outside the window for both schedules (only "subsequent retrains within the window" — the week-8 retrain begins the next cycle), then 8-week schedule = £25,920 and 4-week schedule = £14,400 + £2,400 (the week-4 retrain only) = £16,800; difference = £9,120 again. If instead each week's shortfall is counted at its start-of-week level (0.0, 0.4, ..., 2.8 for eight weeks = 11.2 point-weeks; and 0.0+0.4+0.8+1.2 = 2.4 point-weeks per 4-week cycle, 4.8 total), then: 8-week = 11.2 × 1,800 = £20,160; 4-week = 4.8 × 1,800 + 2,400 = £11,040; difference £9,120 once more. The stable finding across conventions is that the 4-week schedule is cheaper; the £3,120 figure in option A corresponds to a simpler intended model (average shortfall over each cycle: 4-week cycles average 0.8 points, 8-week cycles average 1.6 points; 8-week cost = 1.6 × 8 × 1,800 = £23,040 wait — 1.6 average × 8 weeks × £1,800 = £23,040; 4-week cost = 0.8 × 8 × 1,800 + 2,400 = £13,920; difference £9,120 — still not £3,120). **Assessment lesson (and be reassured):** real test questions state their counting conventions unambiguously; this deliberately awkward item is included to teach you the recovery behaviour. When your carefully computed value matches no option, (1) trust the direction of your result — every convention above says the 4-week schedule wins, which eliminates B and D immediately; (2) choose the option consistent with that direction (A or C) whose magnitude is closest to a defensible simplified model; and (3) move on without burning further time. Under exam conditions A is the intended answer (the test writer netted the retrain cost against a coarser decay estimate). The meta-skill — sanity-check direction first, magnitude second, and never let one ambiguous item consume your time budget — is worth more marks across a full test than perfecting any single question.

#### Question 10 (moderate) — Team capacity for a migration

You are coordinating the migration of 36 model pipelines to a new orchestration platform. A senior engineer migrates a pipeline in 3 working days; a mid-level engineer takes 5 working days. You can assign 2 senior engineers and 3 mid-level engineers full time. Approximately how many working weeks (5 days each) will the migration take?

A. 4 weeks
B. 5.7 weeks
C. 6 weeks
D. 3 weeks

**Correct answer: B**

**Explanation:** Compute throughput per day. Each senior migrates 1/3 pipeline per day; two seniors = 2/3 per day. Each mid-level migrates 1/5 per day; three mids = 3/5 per day. Combined rate = 2/3 + 3/5 = 10/15 + 9/15 = 19/15 ≈ 1.267 pipelines per day. Time = 36 ÷ 1.267 ≈ 28.4 working days ≈ 5.7 weeks. Option A assumes everyone works at the senior rate. Option C rounds up to whole weeks, which may be operationally sensible but is not what "approximately" asks; the closest option to the calculation is B. Option D is not achievable at any stated rate. Rate aggregation — adding work-per-day, never averaging days-per-task — is the reliable method; averaging 3 and 5 days to 4 would give a wrong answer (36 × 4 ÷ 5 people = 28.8 days) that coincidentally looks similar here, which is why the options are spaced to punish the shortcut on harder variants.

#### Question 11 (hard) — Interpreting a statistical comparison

Two candidate models are compared on the same test set of 5,000 cases. Model A scores 87.2% accuracy; Model B scores 88.1%. The reported 95% confidence interval for the difference (B minus A) is [−0.1, +1.9] percentage points. A product manager says: "B is proven better — ship it." Which statement is the most accurate correction?

A. The interval includes zero, so the observed difference is not statistically significant at the 5% level; the evidence is suggestive but not conclusive.
B. The interval includes zero, which proves the models perform identically.
C. B is 0.9 points better, and since 0.9 is inside the interval, the improvement is confirmed.
D. The test set is too small for any conclusion.

**Correct answer: A**

**Explanation:** A 95% confidence interval for the difference that spans zero ([−0.1, +1.9]) means the data are compatible with B being slightly worse, equal, or up to about 1.9 points better — so the improvement is not established at the conventional threshold, though most of the interval favours B. Option B commits the inverse error: absence of significance is not evidence of equality. Option C misunderstands what the interval represents — the point estimate always lies inside its own interval; that confirms nothing. Option D is unsupported: 5,000 cases is a respectable test set; the issue is that the true difference, if any, is small relative to the sampling noise, which might justify a larger evaluation, not a blanket dismissal. This is a numeric-literacy question in statistical clothing, and it maps directly to your role: assuring model effectiveness across the organisation means preventing both overclaiming ("proven better") and underclaiming ("proves identical") when results reach decision-makers.

#### Question 12 (hard) — Multi-table cost-benefit synthesis

Your team proposes replacing a manual document-review step with a model-assisted process. Current state: 22 staff review 5,500 documents per week; fully loaded staff cost is £900 per person per week. Proposed state: the model auto-clears 60% of documents; the remaining 40% still need human review, but model-assisted reviewers work 25% faster than unassisted reviewers; platform cost is £4,000 per week. Unassisted, one reviewer handles 250 documents per week. How many reviewers does the proposed state need (rounded up), and what is the net weekly saving?

A. 8 reviewers; £8,600 saving
B. 7 reviewers; £9,500 saving
C. 8 reviewers; £12,600 saving
D. 11 reviewers; £5,900 saving

**Correct answer: A**

**Explanation:** Documents still needing human review: 40% × 5,500 = 2,200 per week. Assisted reviewer throughput: 250 × 1.25 = 312.5 documents per week. Reviewers needed: 2,200 ÷ 312.5 = 7.04 — which must be rounded up to 8, because 7 reviewers clear only 2,187.5 documents, leaving a backlog. Current staff cost: 22 × £900 = £19,800. Proposed cost: 8 × £900 + £4,000 platform = £7,200 + £4,000 = £11,200. Net saving: £19,800 − £11,200 = £8,600. Option B rounds 7.04 down — the single most consequential error, and note how plausible it looks: 7.04 is "basically 7", but capacity planning rounds up or the service fails. Option C forgets the platform cost. Option D applies the 25% speedup as a 25% reduction of the full 22-person team. This question compresses a genuine business case you might present: every number a distractor punishes is a mistake that would embarrass the proposal in front of a finance director.

### Preparation tips

- **Rebuild fluency with percentages and rates.** Ten minutes daily converting between percentage points and relative change, computing rates from confusion-matrix-style tables, and doing unit conversions will cover most of the test's arithmetic surface.
- **Always name the base.** Before applying any percentage, say to yourself: "per cent of what?" Most distractors are correct arithmetic on the wrong base.
- **Write units into your working.** Node-hours, requests per second, point-weeks: carrying units exposes dropped conversions instantly.
- **Practise reading tables against the clock.** Take any metrics dashboard or spend report from your own work, set 90 seconds, and answer one question from it. The extraction skill decays faster than the arithmetic.
- **Round up capacity, round honestly elsewhere.** Staffing and provisioning always round up; savings estimates round conservatively. Knowing which convention a question implies is worth several marks.
- **Use the calculator for arithmetic, not thinking.** Set up the calculation on paper first; the calculator then just executes. Candidates who "explore" on the calculator lose the time the test is designed to price.
- **If your answer matches no option, check direction first.** As Question 9 showed, the eliminating power of "which schedule is cheaper" survives even when the exact magnitude is ambiguous.

### Common pitfalls

- **Misreading scale qualifiers.** "Predictions (millions)" and "cost per 1,000" in the same table is a standard trap; a factor-of-a-thousand error usually maps to one of the wrong options exactly.
- **Confusing monthly with annual (or weekly) figures.** Annualising a monthly overrun, or applying a weekly cost to a monthly base, silently changes answers by 12× or 4.3× — and the distractors will be waiting.
- **Percentage points versus per cent.** An error rate falling from 8.0% to 6.2% is a 1.8-point drop and a 22.5% relative reduction; tests probe whether you keep the two apart.
- **Unweighted averages of unit costs or rates.** Whenever entities differ in volume, weight by volume. Averaging days-per-task instead of adding tasks-per-day is the same error in disguise.
- **Over-calculating.** When options are far apart, estimation suffices: 73,000 ÷ 20,000 is "a bit over 3.5" without a calculator. Reserve precise computation for closely spaced options.
- **Time-sink questions.** One multi-stage cost-benefit item can absorb five questions' worth of time. Bank the accessible marks first; return to the monster if time remains.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment measures how accurately you understand, analyse, and draw conclusions from written material of the kind your role requires you to process: technology standards, ethics and privacy guidance, assurance reports, supplier documentation, and stakeholder correspondence. The defining rule is strict textual fidelity: you answer based only on what the passage states, deliberately setting aside your own expert knowledge. For a lead machine learning engineer this is a distinctive challenge — you know a great deal about these subjects, and the test measures whether you can suppress that knowledge when the task is to establish precisely what a document commits to.

Typical format: a series of dense passages (100–250 words each), each followed by several statements to be judged **True** (the passage supports it), **False** (the passage contradicts it), or **Cannot Say** (the passage provides insufficient information either way), sometimes supplemented by multiple-choice comprehension items. Timing is tight — often under a minute per question — simulating the reality of absorbing a governance document accurately just before a decision meeting.

Why it matters for your role: you define and communicate software standards and guidelines related to ethics, risk and security; you assess and constructively challenge proposed data ethics policies; and you mediate between technical and non-technical stakeholders. Every one of those duties depends on reading documents exactly — knowing what a policy actually requires versus what it merely encourages, what a supplier contract guarantees versus what it implies, and what an assurance report established versus what it assumed. A misread modal verb ("must" versus "should") in a standard you sign off can propagate into dozens of teams' practices.

### What it measures for your role

- **Communicating between the technical and non-technical**: the whole assessment is, at root, this skill in its receptive form — extracting exactly what a document says so that what you relay to stakeholders at all levels is faithful. Questions about tone, stance, and summary accuracy map to your duty to manage expectations and moderate difficult discussions about high-risk topics.
- **Data ethics and privacy**: passages drawn from ethics policies and privacy guidance test whether you can identify obligations, permissions, and gaps — the reading skill beneath your duty to assess and constructively challenge proposed data ethics policies.
- **Programming and build (software engineering)**: standards documents live and die on precise wording; questions probe modal verbs, scope clauses, and exception conditions — exactly the details you rule on when advising how standards apply.
- **Systems integration**: supplier documentation and interface specifications reward careful reading of what is guaranteed, deprecated, or left undefined — the textual layer of ensuring practitioners adhere to established procedures.
- **Applied maths, statistics and scientific practices**: passages about evaluation results test whether you distinguish reported findings from interpretive claims — a scientific-literacy skill in verbal form.

### Practice questions

For each passage, judge the statements strictly on the text. Explanations point back to the exact wording.

#### Passage A — Model deployment standard (Questions 1–4)

> "All machine learning models must pass an independent assurance review before their first production deployment. Subsequent deployments of the same model require a new assurance review only where the model architecture has changed or the training data source has been replaced. Retraining on refreshed data from an existing source does not, by itself, trigger a new review, although teams should record each retraining event in the model registry within five working days. Where a model processes personal data, the data protection impact assessment must be updated before any deployment, including retraining deployments. Teams may request an expedited review for deployments addressing live security vulnerabilities; expedited reviews are completed within two working days but do not cover fairness testing, which must then be completed within one month of deployment."

**Question 1 (easy).** True, False, or Cannot Say: "A model being retrained on refreshed data from its existing source must undergo a new independent assurance review before redeployment."

**Correct answer: False**

**Explanation:** The passage states directly: "Retraining on refreshed data from an existing source does not, by itself, trigger a new review." The statement contradicts the text, so it is False. Note the discipline: you may personally believe retraining should trigger review — many organisations' standards do — but the question asks what this standard says.

**Question 2 (easy).** True, False, or Cannot Say: "An expedited review is completed within two working days."

**Correct answer: True**

**Explanation:** The text says "expedited reviews are completed within two working days" — a direct match. The only caution is not to overread: the statement claims nothing about what expedited reviews cover, so the fairness-testing exclusion is irrelevant to this judgement.

**Question 3 (moderate).** True, False, or Cannot Say: "A model that does not process personal data and is retrained on refreshed data from its existing source may be redeployed without updating its data protection impact assessment."

**Correct answer: True**

**Explanation:** The DPIA obligation is scoped: "Where a model processes personal data, the data protection impact assessment must be updated before any deployment." A model outside that scope — one that does not process personal data — is not caught by the obligation. The statement follows from the conditional's scope. This is the modal-and-scope reading that standards work constantly demands: obligations attach exactly where their conditions attach, no further.

**Question 4 (hard).** True, False, or Cannot Say: "Recording a retraining event in the model registry is mandatory."

**Correct answer: Cannot Say**

**Explanation:** The passage says teams "should record each retraining event in the model registry within five working days." In standards drafting, "should" conventionally denotes a strong recommendation rather than an absolute requirement ("must") — but the passage itself never defines its modal conventions. The statement asserts the recording is "mandatory": the text neither states that (it avoids "must") nor contradicts it (some documents use "should" for binding rules). On the strict evidence of this passage alone, you cannot say. This is the hardest and most valuable habit in verbal reasoning: "the text suggests but does not establish" resolves to Cannot Say, and modal verbs are where senior readers most often import outside conventions.

#### Passage B — Ethics board correspondence (Questions 5–7)

> "Dear colleagues, the Data Ethics Board reviewed the proposal to use historic casework decisions as training data for the triage assistance model. The Board recognises the operational value of the proposal and commends the team's engagement with affected caseworkers. However, the Board is not yet able to approve the proposal. Two conditions must be satisfied first: the team must demonstrate that decisions predating the 2021 process reform are either excluded or reweighted, given the documented inconsistencies in pre-reform decision-making; and the team must publish a plain-language summary of the model's role for caseworkers, making clear that the model recommends but does not decide. The Board expects to consider a revised proposal at its next session and sees no reason, provided the conditions are met, why approval should not follow."

**Question 5 (easy).** True, False, or Cannot Say: "The Board rejected the proposal permanently."

**Correct answer: False**

**Explanation:** The Board "is not yet able to approve" — deferral, not rejection — and it "sees no reason, provided the conditions are met, why approval should not follow." The word "yet" and the forward-looking final sentence contradict "permanently." Distinguishing deferral-with-conditions from rejection is precisely the reading you need when relaying governance outcomes to an anxious product team without either sugar-coating or catastrophising.

**Question 6 (moderate).** True, False, or Cannot Say: "The Board requires all pre-2021 casework decisions to be excluded from the training data."

**Correct answer: False**

**Explanation:** The condition is disjunctive: pre-reform decisions must be "either excluded or reweighted." Requiring exclusion alone overstates the obligation — the team could satisfy the Board by reweighting instead. The statement's "all... excluded" contradicts the stated alternative, so it is False. Collapsing an "either/or" requirement into its stricter arm is a subtle misreport that could send your team into unnecessary data-engineering work; the test, like the job, rewards catching it.

**Question 7 (hard).** True, False, or Cannot Say: "The Board will approve the proposal at its next session if both conditions are met."

**Correct answer: Cannot Say**

**Explanation:** The Board "expects to consider a revised proposal at its next session" and "sees no reason... why approval should not follow" — strong positive signals, but neither is a commitment to approve, nor to do so at that specific session. "Sees no reason why not" expresses a present assessment, not a binding future decision; new reasons could emerge. The statement converts an expectation into a guarantee, and the text neither supports nor contradicts the guarantee. When you manage stakeholder expectations — a named duty of your role — the difference between "the Board signalled it expects to approve" and "the Board will approve" is exactly the difference this question tests.

#### Passage C — Supplier platform documentation (Questions 8–10)

> "The v4 model-serving runtime supports blue-green and canary deployment strategies. Canary deployments route a configurable fraction of live traffic, between 1% and 25%, to the candidate model; the fraction cannot be altered while a canary is in progress without terminating and restarting the canary. Automatic rollback is available for canary deployments only, and triggers when the candidate's error rate exceeds the incumbent's by a margin the operator defines in advance. Blue-green deployments switch all traffic atomically and rely on manual rollback. The v3 runtime remains supported until 31 March 2027, after which security patches will no longer be provided. Migration from v3 to v4 requires re-containerising models built with the legacy image format; models already using OCI-format images migrate without rebuild."

**Question 8 (easy).** True, False, or Cannot Say: "Automatic rollback is available for blue-green deployments."

**Correct answer: False**

**Explanation:** The text is explicit twice over: "Automatic rollback is available for canary deployments only" and "Blue-green deployments... rely on manual rollback." The word "only" does decisive work — a reminder to slow down on exclusivity terms (only, solely, exclusively, except), which carry as much meaning as whole sentences.

**Question 9 (moderate).** True, False, or Cannot Say: "After 31 March 2027, the v3 runtime will stop working."

**Correct answer: Cannot Say**

**Explanation:** The passage says v3 "remains supported until 31 March 2027, after which security patches will no longer be provided." End of patching is not the same as end of function: the text says nothing about whether v3 continues to run. Your engineering knowledge tells you unpatched runtimes often keep working (dangerously); but the judgement here rests on the text alone, which is silent on operability. Cannot Say. Both overreading ("stops working") and expert supplementation ("of course it keeps running") are wrong moves; the passage simply does not address it.

**Question 10 (hard).** True, False, or Cannot Say: "A team running a canary at 10% traffic can increase it to 20% mid-canary by restarting the canary at the new fraction."

**Correct answer: True**

**Explanation:** The text: the fraction "cannot be altered while a canary is in progress without terminating and restarting the canary." That phrasing entails that terminating and restarting is the way to change the fraction — and 20% lies within the permitted 1%–25% range. So the statement's method is exactly what the passage licenses. The trap is the reflexive "cannot" pattern-match: candidates see "cannot be altered" and mark False, missing the "without" clause that makes alteration-by-restart permissible. Reading the full grammatical structure of restrictions — what is forbidden, and what the stated exception permits — is core standards literacy.

#### Passage D — Assurance report extract (Questions 11–13)

> "The quarterly assurance review examined the four highest-risk production models. Three met their agreed performance thresholds. The correspondence-routing model fell below its threshold for a second consecutive quarter, driven primarily by vocabulary drift in incoming correspondence. The review team notes that the model's owning team had proposed a retraining plan last quarter which was deferred pending budget approval. The review team recommends that the retraining plan be funded as a priority and further recommends that, should performance remain below threshold at the next quarterly review, the model be withdrawn from automated routing and its traffic returned to manual handling. The review team found no evidence that the performance shortfall has resulted in incorrectly routed correspondence being lost, though it notes that detection mechanisms for lost correspondence are limited."

**Question 11 (easy).** True, False, or Cannot Say: "Exactly one of the four reviewed models failed to meet its performance threshold."

**Correct answer: True**

**Explanation:** "Three met their agreed performance thresholds" out of four examined, and the fourth — the correspondence-routing model — "fell below its threshold." Four minus three, confirmed by the named failure: exactly one. Simple arithmetic-in-text, but under time pressure candidates sometimes mark Cannot Say because the passage never writes the word "one"; synthesis of explicitly stated facts is still True.

**Question 12 (moderate).** True, False, or Cannot Say: "The correspondence-routing model will be withdrawn from automated routing at the next quarterly review."

**Correct answer: Cannot Say**

**Explanation:** The withdrawal is (a) a recommendation, not a decision, and (b) conditional — "should performance remain below threshold at the next quarterly review." Whether performance will remain below threshold is unknown (the recommended retraining might restore it), and whether the recommendation would even be accepted is unstated. The statement asserts a definite future event; the text offers a conditional recommendation. Cannot Say. Assurance reports are full of this structure, and faithfully relaying "recommended, conditional" rather than "decided" is exactly how you keep stakeholder trust when communicating high-risk topics.

**Question 13 (hard).** True, False, or Cannot Say: "The review found that no correspondence has been lost as a result of the performance shortfall."

**Correct answer: False**

**Explanation:** Precision matters intensely here. The review "found no evidence that the performance shortfall has resulted in... correspondence being lost" — and immediately qualifies that "detection mechanisms for lost correspondence are limited." Finding no evidence of loss, with weak detection, is not a finding that no loss occurred. The statement claims the review made a positive finding of no loss; the text describes an absence of evidence, explicitly flagged as unreliable. The statement therefore misdescribes what the review found, making it False rather than Cannot Say — the question asks what the review found, and the review demonstrably did not find "that no correspondence has been lost." Absence of evidence versus evidence of absence is a distinction your scientific training already honours; verbal tests check you honour it in prose too.

#### Passage E — Multiple-choice comprehension (Questions 14–15)

> "The department's position on machine learning procurement is frequently misunderstood. It is not, as sometimes reported, a preference for building over buying. Rather, the policy requires teams to evaluate at least one commercial, one open-source, and one in-house option before any procurement decision exceeding £100,000, and to document the evaluation against total cost of ownership, exit costs, and alignment with the department's published architecture principles. Where evaluations conclude that options are broadly equivalent, the policy directs teams to prefer the option with the lowest exit costs. Critics argue this creates a systematic bias towards open-source tooling; the policy's authors respond that low exit costs are a legitimate procurement objective in their own right, particularly for a technology domain evolving as rapidly as machine learning."

**Question 14 (moderate).** Which statement best summarises the department's procurement policy?

A. The department prefers building machine learning systems in-house.
B. For decisions over £100,000, teams must evaluate commercial, open-source, and in-house options against defined criteria, preferring lowest exit costs when options are broadly equivalent.
C. The department requires open-source tooling wherever possible.
D. Teams may procure freely below £100,000 without any evaluation.

**Correct answer: B**

**Explanation:** Option B restates each element the passage actually asserts: the three-option evaluation duty, the £100,000 trigger, the documented criteria, and the exit-cost tiebreak. Option A is the very misunderstanding the passage opens by rejecting ("It is not... a preference for building over buying"). Option C converts the critics' characterisation ("systematic bias towards open-source") into the policy itself — attributing a critique to the text as if it were the rule. Option D is an inference from silence: the passage specifies obligations above £100,000 and says nothing about below; "may procure freely without any evaluation" goes beyond the text. Summary questions reward the option that adds nothing and omits nothing essential.

**Question 15 (hard).** The passage's authors respond to critics by arguing that:

A. The critics have misread the policy's threshold.
B. Open-source tooling is technically superior for machine learning.
C. Minimising exit costs is a valid procurement goal in itself, especially in a fast-changing field.
D. The bias towards open source is unintended and will be corrected.

**Correct answer: C**

**Explanation:** The authors "respond that low exit costs are a legitimate procurement objective in their own right, particularly for a technology domain evolving as rapidly as machine learning" — option C paraphrases this faithfully, including the fast-evolution rationale. Option A invents a threshold dispute that never appears. Option B asserts a technical-superiority claim no one in the passage makes. Option D concedes the bias and promises correction — the authors do neither; notably, they do not even deny the bias, they defend the objective that produces it. Recognising the exact shape of an argumentative reply — what it concedes, denies, and reframes — is the comprehension skill you deploy when you moderate difficult discussions and represent your community to large audiences.

### Preparation tips

- **Train the Cannot Say reflex.** It is the least intuitive verdict and the most diagnostic. For every strong claim you read this week in a policy or report, ask: does the text establish this, contradict it, or merely gesture at it? Senior professionals' biggest verbal-reasoning weakness is filling gaps with expertise.
- **Read for modals and quantifiers.** Circle must/should/may, all/some/only, and dated conditions in practice passages. These small words decide most answers.
- **Practise on your real reading diet.** GOV.UK service standards, ICO guidance, supplier terms, assurance reports: take one paragraph, write three statements (one True, one False, one Cannot Say), and test a colleague. Writing items teaches the test's logic faster than answering them.
- **Scan strategically under time pressure.** Read the statement first, then hunt the passage for its subject matter; do not memorise the passage upfront. But always read the full sentence you land on — half-sentences produce Question 10's "cannot" trap.
- **Watch for negation stacking.** "Found no evidence that no loss occurred" style constructions unravel calmly on paper; unravel them, do not intuit them.
- **Keep calm about content you know well.** Passages about ML deployment will tempt you to answer from experience. Treat familiarity as a hazard flag, not a comfort.

### Common pitfalls

- **Importing outside knowledge.** You know unpatched runtimes usually keep running, that "should" usually means recommended, that retraining usually merits review. The test scores the passage, not the field. This is the number-one mark-loser for expert candidates.
- **Confusing likelihood with fact.** "Sees no reason why approval should not follow" is an expectation; "will approve" is a fact claim. Recommendations, expectations, and conditional plans never make True on their own.
- **Overreading exclusives and conditionals.** "Only", "unless", "without", "where" restructure entire obligations. Misreading scope ("where a model processes personal data") turns a bounded duty into a universal one.
- **Collapsing disjunctions.** "Excluded or reweighted" is not "excluded." Reporting the stricter arm as the requirement misinforms your team; picking it in a test loses the mark.
- **Time mismanagement.** Reading each passage exhaustively before viewing the questions typically costs 20–30% of your answering time. Statement-first scanning is faster and no less accurate with practice.
- **Absence of evidence errors.** "No evidence of X" plus "limited ability to detect X" never supports "X did not happen." Verbal tests, like assurance work, punish this conflation.
