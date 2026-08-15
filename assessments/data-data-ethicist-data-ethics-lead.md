# Data Ethicist (Data Ethics Lead) - Psychometric Assessment Resources

## Introduction

Welcome. This document is a practical, encouraging companion for you as a data ethics lead preparing for psychometric assessments — whether for a new role, a promotion panel, an internal development programme, or simply as a way to sharpen the professional judgement you use every day.

Psychometric assessments are structured, standardised exercises that measure how you think, reason, and decide. They are widely used across the UK public sector because they offer a fair, evidence-based way to understand capability that goes beyond what a CV or interview alone can show. For a data ethics lead, they matter in a particular way: your role sits at the intersection of rigorous analysis and human judgement. You assess the societal effects of technology and data, produce recommendations for other data professionals, and enable colleagues across your organisation to understand data ethics and implement best practice. Every one of those responsibilities draws on the exact capabilities that psychometric assessments are designed to measure — analysing complex information quickly, reasoning accurately with numbers and text, and exercising sound judgement in ambiguous, high-stakes situations.

This document is organised around four workplace job-specific assessments:

1. **Cognitive ability** — pattern recognition, logical deduction, error checking, prioritisation, and problem solving using the artefacts you genuinely handle: ethics review registers, algorithmic impact assessments, training programmes, and policy documents.
2. **Numeric reasoning** — interpreting tables, percentages, ratios, budgets, and performance metrics of the kind that appear in bias audits, survey analyses, and ethics programme reporting.
3. **Verbal reasoning** — reading dense, role-relevant passages (policies, standards, guidance, stakeholder emails) and drawing strictly accurate conclusions from them.
4. **Situational judgement** — realistic workplace dilemmas involving the stakeholders you actually work with: data scientists, policy leads, senior officials, external researchers, and members of the public.

Each section explains what the assessment measures and why it matters for your role, maps the assessment dimensions to the specific skills in the Government Digital and Data Profession Capability Framework for your role, and then offers a substantial set of practice questions with full worked explanations. Each section closes with preparation tips and common pitfalls.

How to use this document: work through it actively rather than reading it passively. Attempt each practice question before reading the explanation. Use the explanations for self-reflection — notice not just whether you got the answer right, but how you reasoned. As a lead, you already coach others in structured thinking; treat this as an opportunity to apply that same discipline to yourself. Take your time, be honest with yourself about areas that feel less comfortable, and remember that performance on these assessments improves markedly with familiarity and practice. You bring deep, multidisciplinary expertise to this work — this document is simply here to help you show it.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive ability assessment is a targeted psychometric test that measures the exact mental processes your role demands. Unlike a generic intelligence test, it uses practical workplace scenarios and artefacts — in your case, ethics review registers, algorithmic impact assessments, research findings, training rosters, and policy frameworks — to predict how effectively you will perform on the job. Questions mimic the everyday tasks and data formats of real data ethics work in a UK government context.

The format is typically online and timed, usually 15 to 30 minutes, with objective scoring against a norm group of professionals at a comparable level. Many platforms are adaptive, adjusting question difficulty based on your previous answers, and most provide short ungraded practice questions first so you can get comfortable with the interface. Employers usually receive a breakdown of speed versus accuracy rather than a single score, so working both quickly and carefully matters.

For a data ethics lead, cognitive assessment matters because your role is fundamentally about structured thinking under complexity. You are asked to read and interpret complex documents from a range of sources and distil what is relevant, to spot flawed assumptions in data science projects, to sequence and prioritise competing ethical reviews, and to diagnose where a process or argument has gone wrong. A well-designed cognitive assessment samples precisely these operations: pattern recognition, logical deduction, error checking, prioritisation, and problem solving.

### What it measures for your role

The assessment dimensions map directly onto the skills in your role profile:

- **Analysis and synthesis (data ethics)**: the core of the test. Questions ask you to draw together and evaluate qualitative and quantitative information, quickly read complex material, and turn data into clear findings — exactly what this skill requires when you help teams define project outcomes and integrate ethical diagnostics.
- **Applied social sciences**: logical deduction questions test whether you can evaluate and challenge assumptions — the same discipline you use when critiquing the assumptions embedded in a data science project or applying social science theory to a policy question.
- **Data ethics and privacy**: error-checking and consistency questions mirror your work assessing and constructively challenging proposed data ethics policies, and spotting where a framework contradicts itself or the law.
- **Managing decisions and risks**: prioritisation questions test proportionate reasoning — applying different risk methodologies in proportion to the risk, and sequencing consequential decisions sensibly.
- **Problem management**: diagnostic questions test whether you can identify root causes, so the right actions are taken to investigate, resolve, and anticipate problems.
- **Product ownership (data ethics)**: several questions use the artefacts of ethics tooling — checklists, assessment templates, feedback data — testing whether you can translate theoretical principles into practical, coherent instruments.

### Practice questions

**Question 1 (easy) — Pattern recognition in an ethics review register**

Your team triages incoming ethics review requests. The register shows the reference codes assigned to the last five completed reviews, in order: ER-A1, ER-B2, ER-C4, ER-D8, ER-E16.

Which reference code comes next?

A) ER-F18
B) ER-F32
C) ER-G32
D) ER-F24

**Correct answer: B**

**Explanation:** Two independent patterns run in parallel. The letters advance one position in the alphabet each time (A, B, C, D, E, so F is next). The numbers double each time (1, 2, 4, 8, 16, so 32 is next). Only option B satisfies both patterns. This is the classic structure of cognitive pattern questions: check every element of the sequence, not just the most obvious one. In your work, the same habit — verifying that every dimension of a pattern holds — is what lets you spot when a dataset's apparent trend hides an inconsistent subgroup.

**Question 2 (easy) — Logical deduction from ethics policy rules**

Your organisation's data ethics policy contains these rules:

1. Every project that processes personal data must complete an ethics self-assessment.
2. Every project that completes an ethics self-assessment and is rated "high risk" must be reviewed by the data ethics team.
3. Project Kestrel processes personal data and is rated "high risk".

Which conclusion follows with certainty?

A) Project Kestrel has already been reviewed by the data ethics team.
B) Project Kestrel must complete an ethics self-assessment and, once completed, must be reviewed by the data ethics team.
C) Project Kestrel does not need an ethics self-assessment because it will be reviewed directly.
D) The data ethics team must review every project that processes personal data.

**Correct answer: B**

**Explanation:** Rule 1 obliges Kestrel to complete a self-assessment (it processes personal data). Rule 2 then obliges review, because Kestrel will have completed a self-assessment and is rated high risk. Option A confuses obligation with completion — the rules say what must happen, not what has happened. Option C invents an exemption that appears nowhere in the rules. Option D over-generalises: review is required only for high-risk projects that have completed self-assessments, not all personal-data projects. When you assess and constructively challenge proposed policies, this precision about what a rule does and does not entail is exactly the skill in play.

**Question 3 (moderate) — Error checking an algorithmic impact assessment summary**

A junior colleague drafts a summary table of four algorithmic impact assessments (AIAs) for your sign-off. The organisation's rule is: residual risk rating = inherent risk rating reduced by one level for each two mitigations implemented (levels: Critical > High > Medium > Low; a rating cannot fall below Low).

| Project | Inherent risk | Mitigations implemented | Residual risk (drafted) |
|---|---|---|---|
| Osprey | Critical | 4 | Medium |
| Merlin | High | 2 | Medium |
| Swift | Medium | 5 | Low |
| Heron | High | 3 | Low |

Which row contains an error?

A) Osprey
B) Merlin
C) Swift
D) Heron

**Correct answer: D**

**Explanation:** Apply the rule row by row. Osprey: 4 mitigations = 2 level reductions; Critical → High → Medium. Correct. Merlin: 2 mitigations = 1 reduction; High → Medium. Correct. Swift: 5 mitigations = 2 reductions (the odd mitigation earns nothing); Medium → Low, and Low is the floor. Correct. Heron: 3 mitigations = 1 reduction; High → Medium, not Low. The drafted "Low" overstates the risk reduction by a whole level — precisely the kind of quiet error that, if signed off, would let a genuinely medium-risk system escape appropriate scrutiny. Methodical row-by-row verification, rather than scanning for what "looks wrong", is the reliable strategy here and in real assurance work.

**Question 4 (moderate) — Prioritising the ethics team's review queue**

You lead the weekly triage of the ethics review queue. Four requests arrive simultaneously. Your triage framework says priority is determined first by potential harm to the public, then by imminence of deployment, then by request date.

- Request 1: A chatbot answering benefits queries; potential harm rated Medium; deploys in 6 weeks; requested Monday.
- Request 2: An automated triage model for social care referrals; potential harm rated High; deploys in 8 weeks; requested Wednesday.
- Request 3: An internal HR dashboard with aggregated, anonymised staff data; potential harm rated Low; deploys in 1 week; requested Monday.
- Request 4: A fraud-detection model flagging benefit claims for investigation; potential harm rated High; deploys in 3 weeks; requested Thursday.

What is the correct review order?

A) 4, 2, 1, 3
B) 2, 4, 1, 3
C) 4, 2, 3, 1
D) 3, 4, 2, 1

**Correct answer: A**

**Explanation:** Apply the criteria strictly in the stated order. Harm first: Requests 2 and 4 are both High, so they outrank 1 (Medium) and 3 (Low). To order 2 and 4, move to the second criterion, imminence: Request 4 deploys in 3 weeks versus 8 weeks for Request 2, so 4 comes first. Then Request 1 (Medium) precedes Request 3 (Low). The tempting error is to let imminence jump the queue — Request 3 deploys in only a week — but the framework subordinates imminence to harm. Distractor D reflects that error. In practice, this mirrors applying risk methodologies in proportion to the risk: an imminent low-harm launch does not outrank a slower high-harm one.

**Question 5 (moderate) — Spotting the flawed assumption**

A data science team presents this argument for a new model: "Our recidivism-risk model was trained on ten years of historical arrest data. Because the dataset is large and covers a long period, the model's predictions will be fair across demographic groups."

Which unstated assumption does the argument depend on?

A) That ten years is a long enough training period.
B) That the historical arrest data itself reflects unbiased treatment of demographic groups.
C) That the model uses the most modern algorithm available.
D) That the team has permission to use the data.

**Correct answer: B**

**Explanation:** The argument leaps from "large, long-period dataset" to "fair predictions". That leap only works if the underlying data is itself free of biased patterns — but arrest data famously encodes historical enforcement disparities, so size and duration can entrench bias rather than dilute it. Option A is discussed in the argument (it is stated, not unstated, and concerns accuracy rather than fairness). Options C and D raise real concerns but the argument's validity does not rest on them. Identifying the load-bearing hidden premise is the essence of evaluating and challenging assumptions made in data science projects — a named requirement of your applied social sciences skill.

**Question 6 (moderate) — Sequencing a training rollout**

You are rolling out data ethics training to four directorates. Constraints:

1. The Data Science directorate must be trained before the Policy directorate, because Policy's sessions use case studies drawn from Data Science's projects.
2. The Digital Delivery directorate cannot be trained in the same month as Data Science (shared staff).
3. Operations must be trained last, once all case studies are finalised.
4. Only one directorate can be trained per month, starting in April.

Which schedule satisfies all constraints?

A) April: Data Science; May: Digital Delivery; June: Policy; July: Operations
B) April: Digital Delivery; May: Policy; June: Data Science; July: Operations
C) April: Policy; May: Data Science; June: Digital Delivery; July: Operations
D) April: Data Science; May: Policy; June: Operations; July: Digital Delivery

**Correct answer: A**

**Explanation:** Test each option against the constraints. Option A: Data Science (April) precedes Policy (June) — satisfies 1; Data Science and Digital Delivery are in different months — satisfies 2 (the constraint concerns simultaneity, and with one directorate per month it is automatically met, but check anyway); Operations is last — satisfies 3. All constraints hold. Option B trains Policy (May) before Data Science (June), violating constraint 1. Option C also puts Policy before Data Science. Option D puts Operations in June with Digital Delivery after it, violating constraint 3. Constraint-satisfaction questions reward systematic elimination — exactly the approach you would use scheduling real training around organisational dependencies.

**Question 7 (moderate) — Diagnosing a recurring problem**

Over three months, five separate project teams have each submitted ethics self-assessments that misclassify special category data as ordinary personal data. The five teams work in different directorates, use different data sources, and were trained by different trainers. All five, however, used version 3 of the self-assessment template, which was updated in the month before the errors began.

As the lead coordinating the problem investigation, what is the most defensible root-cause hypothesis to test first?

A) All five teams are careless and need disciplinary referral.
B) The version 3 template introduced wording that leads teams to misclassify special category data.
C) The trainers are inconsistent and need retraining.
D) Special category data is inherently too difficult for non-specialists to identify.

**Correct answer: B**

**Explanation:** The reasoning method is elimination of varying factors. Directorate, data source, and trainer all vary across the five cases, so none of them can straightforwardly explain a common failure. The template version is the single shared factor, and the timing (errors began after the update) strengthens the hypothesis. Option A attributes to individuals what the evidence pattern attributes to a system — and five independent teams failing identically is a systemic signature. Option C is contradicted by the fact the trainers differed. Option D is untestable pessimism that ignores the timing evidence. This is problem management in miniature: co-ordinate the investigation towards the factor common to all failures, and design the fix (template revision) as the preventive measure.

**Question 8 (moderate) — Consistency checking across policy documents**

You are reviewing three documents ahead of a governance board:

- The draft Data Ethics Policy states: "All automated decision systems affecting members of the public must undergo an ethics review before deployment and annually thereafter."
- The Model Deployment Standard states: "Automated decision systems must be reviewed by the ethics team before deployment; subsequent reviews occur only after material changes to the model."
- The board briefing states: "Our policies require ethics reviews of public-facing automated decision systems before deployment, after material changes, and annually."

Which statement best describes the relationship between the documents?

A) All three documents are consistent.
B) The policy and standard conflict on review frequency; the briefing papers over the conflict by merging both requirements.
C) The briefing contradicts both documents.
D) The standard is stricter than the policy.

**Correct answer: B**

**Explanation:** The policy requires annual reviews; the standard requires reviews only after material changes — a genuine conflict about post-deployment frequency. The briefing quietly combines the two ("after material changes, and annually") as though no conflict existed, which is how contradictions get laundered into governance papers. Option A misses the conflict. Option C is wrong because the briefing contradicts neither document individually — it contradicts the claim that the documents agree. Option D is backwards: the annual requirement is the stricter one, and it sits in the policy. Spotting cross-document inconsistency before a board does is a hallmark of the analysis and synthesis skill at lead level, and it is what makes your constructive challenge of proposed policies credible.

**Question 9 (challenging) — Deduction with incomplete information**

An external researcher tells you: "Every dataset in the ethics-approved catalogue has a completed privacy assessment. Dataset Q has a completed privacy assessment."

A colleague concludes: "Therefore Dataset Q is in the ethics-approved catalogue."

Which of the following is the best evaluation of the colleague's conclusion?

A) Valid — the conclusion follows from the premises.
B) Invalid — a completed privacy assessment is stated as necessary for catalogue membership, not sufficient.
C) Invalid — the premises contradict each other.
D) Valid — but only if Dataset Q contains personal data.

**Correct answer: B**

**Explanation:** The first premise says catalogue membership implies a privacy assessment (assessment is necessary). It does not say a privacy assessment implies membership (sufficient). The colleague has affirmed the consequent — one of the most common formal fallacies, and one you will meet constantly in assurance conversations: "We did the assessment, so we must be compliant." Options A and D endorse the fallacy; option C is wrong because the premises are perfectly compatible. Being able to name precisely why an inference fails — rather than just sensing it is wrong — is what lets you critique colleagues' findings to assure best practice without the conversation becoming adversarial.

**Question 10 (challenging) — Prioritisation under a resource constraint**

Your team of three reviewers has 12 reviewer-days available this month. Five reviews are pending. Your framework requires you to maximise harm-weighted coverage: each completed review earns its harm score; incomplete reviews earn nothing.

| Review | Harm score | Reviewer-days needed |
|---|---|---|
| V | 9 | 6 |
| W | 7 | 5 |
| X | 6 | 4 |
| Y | 5 | 3 |
| Z | 3 | 2 |

Which combination of completed reviews gives the highest total harm score within 12 reviewer-days?

A) V and W (16 points, 11 days)
B) V, Y and Z (17 points, 11 days)
C) W, X and Y (18 points, 12 days)
D) V and X (15 points, 10 days)

**Correct answer: C**

**Explanation:** Check each option's totals. A: 9+7 = 16 points in 11 days. B: 9+5+3 = 17 points in 11 days. C: 7+6+5 = 18 points in exactly 12 days. D: 9+6 = 15 points in 10 days. Option C wins with 18. The instructive point is that the single highest-harm review (V) does not appear in the best answer: its cost (6 days) crowds out combinations of cheaper reviews that jointly cover more harm. In real portfolio triage, the intuition "always do the biggest risk first" can be inferior to maximising total risk coverage — a proportionality judgement that sits at the centre of managing decisions and risks.

**Question 11 (challenging) — Evaluating an evaluation**

Your team piloted a data ethics training module. The product owner reports: "94% of attendees who completed the feedback form rated the training 'useful' or 'very useful'. We should roll it out unchanged organisation-wide."

Attendance records show 200 people attended; 50 completed the feedback form.

Which is the strongest reason to be cautious about the conclusion?

A) 94% is not a high enough satisfaction score.
B) The feedback form respondents are a self-selected 25% of attendees, so satisfied attendees may be over-represented.
C) The training should have been longer.
D) Feedback forms are never reliable.

**Correct answer: B**

**Explanation:** The evidential weak point is non-response bias: only 50 of 200 attendees responded, and people who volunteer feedback tend to differ systematically from those who do not — often being more engaged or more satisfied. The true satisfaction rate among all 200 could be markedly lower. Option A misreads the problem (the issue is representativeness, not the threshold). Options C and D are assertions with no basis in the evidence given. This question rehearses two of your skills at once: familiarity with feedback gathering and evaluation mechanisms (product ownership), and turning research data into clear findings that inform decisions rather than flatter them (analysis and synthesis).

**Question 12 (challenging) — Odd one out in ethical framing**

Four project descriptions cross your desk. Three share a common ethical failure mode; one does not. Which is the odd one out?

A) A model predicts which neighbourhoods need more housing inspections, trained on past inspection outcomes.
B) A model predicts which job applicants will succeed, trained on the performance ratings of past hires.
C) A model predicts which pupils need reading support, trained on a randomised screening assessment given to all pupils.
D) A model predicts which benefit claims are fraudulent, trained on past investigations that found fraud.

**Correct answer: C**

**Explanation:** A, B, and D all share the feedback-loop failure mode: they are trained on outcomes generated by prior human selection decisions (where inspectors chose to look, who was hired, which claims were investigated), so the training data reflects the historical targeting pattern, and the model risks recycling it. C is different in kind: the screening assessment was randomised and administered to all pupils, so the training data does not inherit a prior selection bias (other risks may exist, but not this one). Classifying problems by their underlying mechanism — rather than by surface subject matter — is what allows you to demonstrate how to apply ethical principles in practice through examples and case studies, and to teach teams to recognise a failure mode the next time it appears wearing different clothes.

**Question 13 (challenging) — Multi-step problem solving on a governance workflow**

Your ethics review workflow has four stages: Intake (1 day), Assessment (3 days), Panel (held only on Thursdays), and Decision letter (1 day after Panel). A project submits its request at Intake on a Monday. Stages run on consecutive working days, and a request can only go to the first Panel that falls after Assessment is complete.

On which day is the decision letter issued?

A) The first Friday after submission
B) The second Friday after submission
C) The first Thursday after submission
D) The second Thursday after submission

**Correct answer: B**

**Explanation:** Trace the workflow. Intake occupies Monday. Assessment takes Tuesday, Wednesday, and Thursday. The Panel must fall after Assessment completes — Assessment finishes on Thursday itself, so that same Thursday's panel is too early; the first available Panel is the following Thursday (the second Thursday after submission). The decision letter follows one working day later: the second Friday. Distractor A forgets the Panel-day constraint; C and D stop a stage short. Workflow-tracing questions reward drawing a quick timeline rather than reasoning in your head — a technique worth practising, since as a lead you routinely diagnose where governance processes silently add a week.

### Preparation tips

- **Practise with your own artefacts.** Take a real (suitably anonymised) ethics register, AIA summary, or training schedule and set yourself questions like those above: what is the pattern, where is the error, what should come first? Familiar material makes the cognitive operations transparent.
- **Rehearse timed conditions.** These tests give roughly a minute per question. Practise reading a rule set once, carefully, then answering fast — re-reading is the biggest time sink.
- **Verify systematically, not intuitively.** For error-checking and consistency questions, check every row or clause in order. Intuition tells you something is wrong; method tells you where.
- **Name the logic.** When you practise deduction questions, articulate why an inference fails (necessary versus sufficient, affirming the consequent, over-generalisation). At lead level you will meet these questions at the harder end, where the fallacies are dressed in plausible policy language.
- **Do the interface warm-up.** Always complete the ungraded practice questions offered before the timed section begins. Interface familiarity is free marks.
- **Trust your professional maturity.** You analyse arguments and evidence for a living. The test is a compressed, timed version of your daily work — approach it with the same calm rigour you bring to a review panel.

### Common pitfalls

- **Checking only the salient pattern.** Sequence and table questions often encode two rules at once (as in Question 1). Verify every element before answering.
- **Confusing "must" with "did".** Policy-logic questions punish sliding from obligation to fact (Question 2). Read modal verbs precisely.
- **Letting urgency trump the framework.** In prioritisation questions, apply the stated criteria in their stated order, even when an urgent-looking item tugs at you (Question 4).
- **Time sink questions.** Do not let one convoluted workflow-trace consume five minutes. Flag it, move on, return if time allows — accuracy on the questions you do answer matters more than heroics on one.
- **Bringing outside knowledge.** Answer from the rules and data given, not from what your own organisation's process happens to be. The test world is self-contained.
- **Second-guessing adaptive difficulty.** If questions feel harder as you go, that often means you are doing well. Do not let perceived difficulty rattle your confidence mid-test.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment evaluates your ability to analyse, interpret, and make sound decisions using numerical data. It deliberately mimics the data-handling demands of your role: rather than abstract formulae, you will meet tables, percentages, ratios, budgets, and performance metrics of the kind that appear in bias audits, survey results, training programme reports, and ethics programme budgets. The mathematics itself is rarely advanced — percentages, ratios, weighted averages, rates — but it is embedded in realistic data that must be read carefully.

Typical format: online, strictly timed (often around a minute to ninety seconds per question), with an on-screen calculator allowed or provided. The emphasis is on interpretation over mental arithmetic: extracting the right figures from a table, applying the right operation, and sanity-checking the result under time pressure.

For a data ethics lead, numeric fluency is not a nice-to-have. Your role profile asks you to draw together, analyse and evaluate qualitative *and quantitative* data, to hold meaningful conversations with data scientists about minimising bias in data, and to critique colleagues' findings to assure best practice. You cannot credibly challenge a data science team's fairness metrics, or spot that a headline percentage hides an unrepresentative denominator, unless you are comfortable doing the arithmetic yourself. Numeric reasoning is also central to proportionate risk management: deciding whether a disparity is material, whether a budget can absorb a programme extension, or whether a survey's response rate supports its conclusions.

### What it measures for your role

- **Analysis and synthesis (data ethics)**: every question requires drawing quantitative information together and turning it into a clear finding — the numeric half of this skill, exercised under time pressure.
- **Communication (data ethics)** and **Communicating between the technical and non-technical**: several questions rehearse the numbers behind conversations you host — bias rates, demographic representation, model error rates — because translating technical concepts credibly requires being able to compute them.
- **Data ethics and privacy**: questions use bias audit tables, consent rates, and data-quality figures, mirroring your work identifying and addressing ethical and privacy concerns with evidence rather than assertion.
- **Empathy and inclusivity**: representation and disparity calculations test the quantitative underpinning of incorporating views from underrepresented groups and understanding the consequences of data systems for diverse stakeholders.
- **Managing decisions and risks**: budget, capacity, and expected-impact questions test proportionate quantitative judgement.
- **Product ownership (data ethics)**: uptake, completion, and feedback metrics for ethics tools and training test your familiarity with evaluation mechanisms.

### Practice questions

**Question 1 (easy) — Training completion rates**

Your data ethics training programme has these completion figures for the quarter:

| Directorate | Staff enrolled | Staff completed |
|---|---|---|
| Data Science | 80 | 68 |
| Policy | 120 | 90 |
| Digital Delivery | 150 | 105 |
| Operations | 50 | 42 |

Which directorate has the highest completion rate?

A) Data Science
B) Policy
C) Digital Delivery
D) Operations

**Correct answer: A**

**Explanation:** Compute each rate: Data Science 68 ÷ 80 = 85%; Policy 90 ÷ 120 = 75%; Digital Delivery 105 ÷ 150 = 70%; Operations 42 ÷ 50 = 84%. Data Science's 85% narrowly beats Operations' 84%. The trap is judging by absolute numbers — Digital Delivery completed the most people (105) but has the lowest rate. Distinguishing counts from rates is the single most frequent numeric skill in ethics reporting: "105 people trained" and "70% completion" tell very different stories to a governance board.

**Question 2 (easy) — Percentage change in ethics review demand**

Last year your team received 240 ethics review requests. This year it received 312. What is the percentage increase?

A) 23%
B) 30%
C) 33%
D) 72%

**Correct answer: B**

**Explanation:** Increase = 312 − 240 = 72. Percentage increase = 72 ÷ 240 = 0.30 = 30%. Distractor D (72) is the raw increase mistaken for a percentage; distractor A comes from dividing by the new value (72 ÷ 312 ≈ 23%), a common error — percentage change is always measured against the *original* value. You will use this constantly when reporting demand growth to justify team resourcing.

**Question 3 (moderate) — Reading a bias audit table**

A data science team shares a bias audit of their fraud-flagging model:

| Group | Applications processed | Flagged for investigation | Investigations finding fraud |
|---|---|---|---|
| Group A | 10,000 | 800 | 200 |
| Group B | 5,000 | 600 | 150 |

Which statement is correct?

A) Group B's flag rate is 12%, which is 1.5 times Group A's flag rate of 8%.
B) Group A's flag rate is higher than Group B's.
C) Both groups have the same flag rate.
D) Group B's flag rate is 6%.

**Correct answer: A**

**Explanation:** Flag rate = flagged ÷ processed. Group A: 800 ÷ 10,000 = 8%. Group B: 600 ÷ 5,000 = 12%. And 12 ÷ 8 = 1.5, so Group B is flagged at 1.5 times the rate of Group A. The absolute counts point the other way (800 flags versus 600), which is why option B tempts anyone reading carelessly. Note what the question does *not* settle: whether the disparity is justified. The "hit rate" among investigations (200 ÷ 800 = 25% for A; 150 ÷ 600 = 25% for B) is identical, which means the model finds fraud at the same precision for both groups while subjecting Group B to proportionally more investigations — exactly the sort of nuance you would raise when supporting data scientists in implementing data ethics.

**Question 4 (moderate) — Survey representativeness**

You commission a public attitudes survey on data sharing. The population you serve is 20% from ethnic minority backgrounds. Your survey receives 1,500 responses, of which 180 are from ethnic minority respondents.

What percentage of survey responses came from ethnic minority respondents, and how does it compare with the population?

A) 12% — under-represented by 8 percentage points
B) 12% — over-represented by 8 percentage points
C) 18% — under-represented by 2 percentage points
D) 20% — representative

**Correct answer: A**

**Explanation:** 180 ÷ 1,500 = 0.12 = 12%. The population benchmark is 20%, so the survey under-represents ethnic minority respondents by 20 − 12 = 8 percentage points — meaning findings presented as "public attitudes" would be skewed towards majority-group views unless weighted or supplemented. This is the arithmetic behind your empathy and inclusivity skill: incorporating views from underrepresented groups starts with measuring whether they are in your evidence base at all. Note the phrase "percentage points" — the relative shortfall is 8 ÷ 20 = 40% fewer than expected, a distinction worth making precisely when you brief stakeholders.

**Question 5 (moderate) — Weighting a risk score**

Your ethics triage tool scores projects on three criteria, weighted as follows: potential harm (weight 3), scale of data (weight 2), novelty of technique (weight 1). Each criterion is scored 1–5. Project Osprey scores: harm 4, scale 3, novelty 5.

What is Osprey's weighted average score, to one decimal place?

A) 4.0
B) 3.8
C) 3.5
D) 4.2

**Correct answer: B**

**Explanation:** Weighted sum = (4 × 3) + (3 × 2) + (5 × 1) = 12 + 6 + 5 = 23. Total weight = 3 + 2 + 1 = 6. Weighted average = 23 ÷ 6 = 3.833… ≈ 3.8. Distractor A is the simple unweighted mean of 4, 3, 5 — forgetting the weights entirely. The design point matters as much as the arithmetic: the weighting means a project's novelty (score 5 here) contributes least, which is a deliberate proportionality choice. As the lead who develops data ethics tools and translates theoretical principles into practice, you should be able both to compute such scores and to defend or challenge the weights behind them.

**Question 6 (moderate) — Budgeting the ethics programme**

Your annual data ethics programme budget is £180,000, allocated: 45% staff training delivery, 30% research and expert advice, 15% tooling, 10% community engagement. Mid-year, you must find £13,500 for an unplanned bias audit by cutting the tooling line only.

What percentage of the original tooling budget remains after the cut?

A) 50%
B) 75%
C) 40%
D) 85%

**Correct answer: A**

**Explanation:** Tooling budget = 15% of £180,000 = £27,000. Cut = £13,500. Remaining = £27,000 − £13,500 = £13,500, which is 13,500 ÷ 27,000 = 50% of the original tooling line. Two-step percentage problems like this reward writing down the intermediate figure (£27,000) rather than chaining operations mentally. In programme terms, the calculation also frames the decision you would take to a sponsor: is halving the tooling line for one audit a proportionate trade-off, or should the cost be shared across lines?

**Question 7 (moderate) — Consent rates over time**

A service reports the proportion of users consenting to optional data sharing:

| Quarter | Users asked | Users consenting |
|---|---|---|
| Q1 | 40,000 | 26,000 |
| Q2 | 50,000 | 30,000 |

A colleague says: "Consent went up — 30,000 is more than 26,000, so users are more comfortable with sharing."

What does the consent *rate* show?

A) The rate rose from 60% to 65%.
B) The rate fell from 65% to 60%.
C) The rate is unchanged at 65%.
D) The rate fell from 65% to 52%.

**Correct answer: B**

**Explanation:** Q1 rate = 26,000 ÷ 40,000 = 65%. Q2 rate = 30,000 ÷ 50,000 = 60%. The rate *fell* by five percentage points even though the count rose, because the denominator grew faster than the numerator. Your colleague's conclusion reverses the true direction of travel — a mistake with real ethical consequences if it leads the organisation to believe user comfort is rising when it is declining. Challenging exactly this kind of numerically plausible but wrong claim is what "critique colleagues' findings to assure best practice" means in daily life.

**Question 8 (challenging) — Model error rates across groups**

A model supporting social care triage has these evaluation figures:

| Group | Cases | Cases needing urgent care | Urgent cases correctly identified |
|---|---|---|---|
| Group X | 2,000 | 400 | 340 |
| Group Y | 1,000 | 250 | 175 |

What are the false negative rates (urgent cases missed) for each group?

A) X: 15%; Y: 30%
B) X: 3%; Y: 7.5%
C) X: 85%; Y: 70%
D) X: 15%; Y: 25%

**Correct answer: A**

**Explanation:** Group X misses 400 − 340 = 60 urgent cases; false negative rate = 60 ÷ 400 = 15%. Group Y misses 250 − 175 = 75; rate = 75 ÷ 250 = 30%. So the model misses urgent cases in Group Y at twice the rate of Group X — a serious fairness finding, because a false negative here means a person needing urgent care is not identified. Distractor B divides by total cases rather than urgent cases (the wrong denominator); distractor C gives the *sensitivity* (the complement), a figure the team might prefer to quote. Knowing which denominator and which direction of error matters — and being able to say "your headline accuracy hides a doubled miss rate for Group Y" — is precisely the technical fluency your communication (data ethics) skill demands.

**Question 9 (challenging) — Cost per outcome for training options**

You are choosing between two delivery models for next year's ethics training:

- Option 1: E-learning licence at £24,000 per year, expected to reach 800 staff with a 60% completion rate.
- Option 2: Facilitated workshops costing £900 per session, 15 staff per session, 40 sessions planned, with a 95% completion rate.

What is the approximate cost per *completing* member of staff for each option?

A) Option 1: £50; Option 2: £63
B) Option 1: £30; Option 2: £60
C) Option 1: £50; Option 2: £60
D) Option 1: £40; Option 2: £63

**Correct answer: A**

**Explanation:** Option 1: completions = 800 × 0.60 = 480; cost per completion = £24,000 ÷ 480 = £50. Option 2: total cost = £900 × 40 = £36,000; attendees = 15 × 40 = 600; completions = 600 × 0.95 = 570; cost per completion = £36,000 ÷ 570 ≈ £63.16, which rounds to £63. So the correct pairing is £50 and £63 — option A. Options C and D each contain one correct figure paired with a wrong one, which is how rushed readers get caught: always compute *both* figures before choosing, rather than matching on the first one you calculate. The management insight survives the arithmetic: the workshops cost about 26% more per completion but deliver a far higher completion rate and, plausibly, deeper engagement — cost per outcome is where the numeric analysis ends and your product-ownership judgement begins.

**Question 10 (challenging) — Ratio reasoning on review capacity**

Ethics reviews come in two types: standard (taking 2 reviewer-days) and complex (taking 5 reviewer-days). Historically, standard and complex reviews arrive in the ratio 3:1. Your team has 220 reviewer-days available next quarter.

Assuming arrivals follow the historical ratio, how many complex reviews can the team complete if it handles every review that arrives, and demand exactly exhausts capacity?

A) 15
B) 20
C) 25
D) 30

**Correct answer: B**

**Explanation:** Take one "bundle" of arrivals in the 3:1 ratio: 3 standard + 1 complex = (3 × 2) + (1 × 5) = 11 reviewer-days per bundle. Bundles within capacity: 220 ÷ 11 = 20 bundles. Each bundle contains one complex review, so 20 complex reviews (and 60 standard). The bundle method — converting a ratio into a repeating unit of cost — is the fastest route through ratio-plus-capacity questions and is exactly how you would model whether a proposed intake policy is sustainable before agreeing it with stakeholders.

**Question 11 (challenging) — Interpreting a percentage-point disparity claim**

A briefing states: "After mitigation, the model's approval rate disparity between the two largest demographic groups narrowed from 12 percentage points (58% vs 46%) to 6 percentage points (52% vs 46%)."

Which of the following is a correct reading of the figures?

A) The disparity halved, achieved entirely by lowering the higher group's approval rate; the lower group saw no improvement.
B) Both groups' approval rates rose.
C) The lower group's approval rate rose by 6 percentage points.
D) The model now approves both groups at the same rate.

**Correct answer: A**

**Explanation:** Before: 58% vs 46%. After: 52% vs 46%. The gap fell from 12 to 6 percentage points — it halved — but look at *how*: the higher group's rate dropped 6 points while the lower group's rate is unchanged at 46%. This is "levelling down": equality improved without anyone becoming better off, and one group became worse off. Options B and C claim improvements the data does not show; option D overstates the convergence. The ethical significance of *how* a disparity narrows — not just that it narrows — is a classic discussion you would lead with a data science team, and it turns entirely on reading the underlying rates rather than the headline gap.

**Question 12 (challenging) — Compound growth in programme reach**

Your ethics champions network has 64 members. You plan growth of 25% per year. Approximately how many members will the network have after three years?

A) 112
B) 125
C) 120
D) 100

**Correct answer: B**

**Explanation:** Compound growth: 64 × 1.25 = 80 after year one; 80 × 1.25 = 100 after year two; 100 × 1.25 = 125 after year three. Distractor A comes from simple (non-compounding) growth: 64 + (3 × 16) = 112. The difference between simple and compound growth widens every year, so multi-year projections in business cases should be checked for which assumption they use — a quiet source of over- or under-promising in programme plans you sign off.

**Question 13 (moderate) — Sanity-checking a headline figure**

A press summary drafted by a comms colleague says: "Ethics reviews prevented harm in 45% of projects this year." The underlying data: 180 projects were reviewed; 27 reviews led to material changes that mitigated an identified harm.

What percentage of reviewed projects actually saw harm-mitigating changes?

A) 45%
B) 27%
C) 15%
D) 18%

**Correct answer: C**

**Explanation:** 27 ÷ 180 = 0.15 = 15%. The drafted 45% is unsupported — perhaps a transposition or a percentage taken of the wrong base (27 is 45% of 60, so someone may have used a subset as the denominator). Whatever its origin, publishing it would overstate the programme's effect threefold and expose the organisation to fair criticism. Verifying every published number back to its numerator and denominator is a discipline your role models for others: transparency about your own programme's performance is part of demonstrating how data ethical issues fit into the wider organisational context.

**Question 14 (challenging) — Opt-out rates and effective sample size**

A research team plans to reuse a service dataset of 60,000 users for an analysis, offering an opt-out. Early communications produce a 4% opt-out overall, but the rate differs by group: users aged over 65 (who make up 25% of the dataset) opt out at 10%, while all other users opt out at 2%.

After opt-outs, what proportion of the remaining dataset is aged over 65, to the nearest whole percentage point?

A) 25%
B) 22%
C) 23%
D) 27%

**Correct answer: C**

**Explanation:** Over-65s: 25% of 60,000 = 15,000; a 10% opt-out removes 1,500, leaving 13,500. Others: 45,000; a 2% opt-out removes 900, leaving 44,100. Remaining total = 13,500 + 44,100 = 57,600. Over-65 share = 13,500 ÷ 57,600 = 0.2344 ≈ 23%. (Check the overall opt-out: 2,400 ÷ 60,000 = 4%, consistent with the stem.) The ethical point is the arithmetic's shadow: a differential opt-out quietly shifts the dataset's composition, so analyses "of all users" now under-represent older users — a representativeness drift you would flag when advising the team, and a neat demonstration that respecting choice and maintaining representativeness are in genuine tension that must be measured, not assumed away.

**Question 15 (moderate) — Reading a stacked metric honestly**

Your quarterly dashboard reports "ethics engagement": the combined count of training completions, drop-in clinic attendances, and intranet guidance page views. This quarter's figure is 5,200, up from 4,000 last quarter (+30%). The breakdown:

| Component | Last quarter | This quarter |
|---|---|---|
| Training completions | 700 | 560 |
| Clinic attendances | 300 | 240 |
| Guidance page views | 3,000 | 4,400 |

Which statement most accurately characterises the quarter?

A) Engagement rose 30% across the board.
B) The headline rose 30%, but both high-effort engagement types fell by 20%; the rise is entirely from page views.
C) Training completions rose in line with the headline.
D) The figures are internally inconsistent.

**Correct answer: B**

**Explanation:** Check the components: training 560 ÷ 700 = 0.80 (a 20% fall); clinics 240 ÷ 300 = 0.80 (also −20%); page views 4,400 ÷ 3,000 ≈ 1.47 (+47%). Totals: 700+300+3,000 = 4,000 and 560+240+4,400 = 5,200, so the figures are consistent (ruling out D) and the headline +30% is genuine — but composed entirely of the lowest-effort, most ambiguous signal (page views can indicate confusion as easily as engagement) while both deeper engagement measures declined identically. A composite metric that mixes unlike components invites exactly this misreading, and the honest brief to your head of data ethics leads with the component trends, not the headline. Decomposing an aggregate before trusting it is bread-and-butter analysis and synthesis — and refusing to let a favourable headline pass unexamined, even one that flatters your own programme, is the integrity habit the role runs on.

### Preparation tips

- **Rebuild fluency with percentages, ratios, and rates.** Almost every question reduces to one of these. Practise percentage change (always against the original value), percentage points versus relative change, and weighted averages until they are automatic.
- **Always identify the denominator first.** Most ethics-relevant errors — and most test distractors — are denominator errors: wrong base for a percentage, counts confused with rates, subsets treated as wholes.
- **Write down intermediate figures.** Multi-step problems (budget lines, cost per completion) go wrong when steps are chained mentally. Use the on-screen calculator and note the interim result.
- **Practise reading tables under time pressure.** Give yourself 60–90 seconds per question. Scan the headers and units first, then extract only the cells the question needs.
- **Recheck against the options before committing.** As Question 9 shows, options are often built from mismatched or partially correct computations. Compute fully, then match.
- **Connect it to your practice.** After each practice question, ask: where does this calculation appear in my real work — a bias audit, a survey, a business case? That link makes the methods stick and reminds you why the fluency matters.

### Common pitfalls

- **Misreading labels and units.** Confusing quarterly with annual figures, or missing "in thousands" qualifiers, produces answers that are wrong by an order of magnitude. Read headers before numbers.
- **Counts versus rates.** The most common ethics-data error: a bigger count is not a higher rate (Questions 1, 3, and 7 all turn on this).
- **Wrong denominator for error rates.** False negative rates divide by actual positives, not by all cases (Question 8). Choose the denominator that matches the question asked.
- **Over-calculating.** When options are far apart, estimation and rounding will identify the answer faster than exact arithmetic. Save precision for when options are close.
- **Time sink questions.** A single multi-stage calculation can devour the time for three easier questions. Skip, flag, and return.
- **Percentage points versus percent.** A fall from 65% to 60% is five percentage points but about an 8% relative fall. Tests — and ministers' briefings — punish conflation of the two.

A final word of encouragement for this section: candidates at senior levels sometimes worry that their day-to-day arithmetic has gone rusty because analysts and data scientists now do the calculating. The questions above should reassure you that nothing here is beyond quick revision — every one reduces to a percentage, a ratio, a weighted average, or a careful choice of denominator. What the assessment really measures, and what your role really requires, is the judgement wrapped around the arithmetic: knowing which calculation exposes the truth of a table, noticing when a headline and its components tell different stories, and having the confidence to redo a number someone senior has already circulated. A few hours of deliberate practice will restore the fluency; the judgement you already have.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment evaluates how well you understand, analyse, and draw strictly correct conclusions from written material. It mirrors the exact reading demands of your role: dense policy documents, standards, legal-adjacent guidance, stakeholder emails, and research reports. Passages use relevant terminology, and questions typically require you to judge statements as **True**, **False**, or **Cannot Say** — based *only* on the text provided, ignoring everything you happen to know from outside it. Some questions are multiple-choice comprehension: identifying the best summary, the author's main claim, or what a clause does and does not require.

The format is time-pressured, often under a minute per question, simulating the reality of skimming a forty-page framework the morning before a governance board. Accuracy under that pressure — neither over-reading nor under-reading the text — is what the assessment scores.

For a data ethics lead, this may be the most job-relevant assessment of the four. Your role profile explicitly requires you to "quickly read and interpret complex documents from a range of sources and distil to what is relevant". You assess and constructively challenge proposed data ethics policies, which demands forensic attention to what a policy's words actually commit the organisation to, as opposed to what its authors intend or its readers assume. And because you mediate between technical and non-technical audiences, you constantly translate texts for others — a translation that is only trustworthy if your own reading is exact.

### What it measures for your role

- **Analysis and synthesis (data ethics)**: the entire test is this skill's reading component — interpreting complex documents quickly and distilling what is relevant, then converting text into defensible findings.
- **Data ethics and privacy**: passages are drawn from the genre you inhabit — ethics frameworks, privacy guidance, policy proposals — and the questions test whether you can extract precisely what a policy requires, permits, and stays silent about, which is the foundation of constructive challenge.
- **Communication (data ethics)** and **Communicating between the technical and non-technical**: comprehension questions test whether you can identify a text's core claim and tone — the first step in translating technical concepts so they are understood by all, and in interpreting the needs stakeholders express in writing.
- **Applied social sciences**: some passages present research findings and arguments; the questions test whether you can separate what a study found from what its authors speculate — the discipline of describing emerging theories accurately.
- **Stakeholder relationship management**: email and briefing passages test reading between formal lines without inventing content — understanding what a stakeholder has actually committed to or asked for.

### Practice questions

**Passage A — Draft ethics framework clause (Questions 1–4)**

*"All projects developing or procuring automated decision-making systems must complete an Algorithmic Impact Assessment (AIA) before the system processes live data. Projects rated 'limited impact' in the AIA may proceed with annual self-certification thereafter. Projects rated 'significant impact' must obtain approval from the Data Ethics Board before deployment and after any material change to the system's purpose, data inputs, or model logic. The Board may, at its discretion, require an independent external audit for systems affecting access to public services. Nothing in this framework removes obligations arising under data protection legislation."*

**Question 1 (easy)** — True, False, or Cannot Say: "A project rated 'limited impact' must obtain Data Ethics Board approval before deployment."

**Correct answer: False**

**Explanation:** The passage assigns Board approval only to projects rated "significant impact". Limited-impact projects "may proceed with annual self-certification thereafter" — the text creates a different route for them, so the statement contradicts the passage. Note the discipline: you answer False because the text *establishes otherwise*, not because you know how your own organisation does it.

**Question 2 (moderate)** — True, False, or Cannot Say: "An external audit is mandatory for all systems affecting access to public services."

**Correct answer: False**

**Explanation:** The passage says the Board "may, at its discretion, require" an external audit for such systems. "May, at its discretion" is permissive, not mandatory — the Board can require an audit, but nothing obliges it to. The statement's "mandatory for all" directly contradicts the discretionary wording. Modal verbs — may, must, should — carry the legal and operational weight of a framework, and verbal reasoning tests (like policy review) turn on reading them exactly.

**Question 3 (moderate)** — True, False, or Cannot Say: "A significant-impact system that changes its data inputs materially requires fresh Board approval even if its purpose is unchanged."

**Correct answer: True**

**Explanation:** The clause requires approval "after any material change to the system's purpose, data inputs, or model logic". The list is disjunctive — the "or" means any one of the three triggers suffices. A material change to data inputs alone therefore triggers the requirement, regardless of purpose. Reading lists as disjunctive or conjunctive is a recurring test point and a recurring source of real-world compliance disputes.

**Question 4 (challenging)** — True, False, or Cannot Say: "Complying with this framework ensures a project also complies with data protection legislation."

**Correct answer: False**

**Explanation:** The final sentence states: "Nothing in this framework removes obligations arising under data protection legislation." The framework explicitly positions itself as *additional to*, not a substitute for, legal obligations — so it directly disclaims the idea that framework compliance ensures legal compliance. A careless reader might answer Cannot Say, reasoning that the passage doesn't discuss legal compliance in detail; but the disclaimer sentence is exactly a statement that the two are separate, which contradicts the claim. This mirrors a real advisory scenario: teams often assume an ethics sign-off is a legal sign-off, and your job is to point at the sentence that says it is not.

**Passage B — Email from a directorate head (Questions 5–7)**

*"Thanks for your team's review of our proposed analytics platform. We accept the recommendation to exclude the sensitive attributes from the model's inputs, and we will implement this before the pilot. However, we do not agree that the pilot should be delayed until the fairness metrics are re-run: the pilot is limited to 500 volunteer users who have given explicit consent, and we believe this contains any risk. We would welcome a follow-up session with your team during the pilot, and we will share the re-run metrics as soon as they are available. Could you confirm whether your team's concerns would prevent sign-off at the December gateway?"*

**Question 5 (easy)** — True, False, or Cannot Say: "The directorate has agreed to implement one of the review's recommendations before the pilot."

**Correct answer: True**

**Explanation:** "We accept the recommendation to exclude the sensitive attributes… and we will implement this before the pilot" — a direct match. The easy questions in a verbal test reward locating the sentence and checking it says what the statement says, no more.

**Question 6 (moderate)** — True, False, or Cannot Say: "The re-run fairness metrics will be available before the pilot begins."

**Correct answer: False**

**Explanation:** The email refuses to delay the pilot "until the fairness metrics are re-run" and promises to share the metrics "as soon as they are available" — with a follow-up session *during* the pilot. Taken together, the text establishes that the pilot will proceed without waiting for the re-run metrics; the writer's whole argument is that waiting is unnecessary. The statement contradicts the position the email stakes out. If you hesitated towards Cannot Say, notice that the refusal to delay *until* the metrics are re-run only makes sense if the metrics will not be ready first.

**Question 7 (challenging)** — Which of the following best describes what the directorate head is asking of the ethics team?

A) To withdraw the recommendation about sensitive attributes.
B) To state whether their outstanding concerns would block December gateway sign-off.
C) To approve the pilot's expansion beyond 500 users.
D) To re-run the fairness metrics themselves.

**Correct answer: B**

**Explanation:** The email's only question is: "Could you confirm whether your team's concerns would prevent sign-off at the December gateway?" Option A reverses what happened (the recommendation was accepted). Option C invents an expansion never mentioned. Option D misassigns the work — the directorate will share the metrics, implying they are re-running them. Identifying the actual "ask" buried at the end of a diplomatically worded email is a daily skill in stakeholder relationship management, and multiple-choice comprehension questions test it directly.

**Passage C — Research report extract (Questions 8–10)**

*"Our review of 42 public sector algorithmic transparency reports found that 31 disclosed the categories of data used, but only 9 described how the system's outputs were monitored after deployment. Interviewees from publishing bodies most frequently cited resource constraints as the reason for limited post-deployment reporting. The authors consider it plausible that mandatory reporting templates would increase disclosure consistency, though the study did not test this. No relationship was found between organisation size and disclosure completeness."*

**Question 8 (easy)** — True, False, or Cannot Say: "Fewer than a quarter of the reviewed reports described post-deployment monitoring of outputs."

**Correct answer: True**

**Explanation:** 9 of 42 reports described post-deployment monitoring. A quarter of 42 is 10.5, and 9 is fewer than 10.5, so the statement holds. Verbal tests frequently smuggle in small calculations; the discipline is to do the arithmetic rather than eyeball it, because "9 of 42" sits close enough to a quarter to tempt a guess either way.

**Question 9 (moderate)** — True, False, or Cannot Say: "Mandatory reporting templates increase disclosure consistency."

**Correct answer: Cannot Say**

**Explanation:** The authors "consider it plausible" that templates would help, and the passage explicitly notes "the study did not test this". A speculation flagged as untested can be neither confirmed (True) nor contradicted (False) by the text — the correct judgement is Cannot Say. This is the single most examined distinction in verbal reasoning: the difference between what a text *asserts as finding* and what it *offers as conjecture*. It is also the distinction your applied social sciences skill demands when you describe emerging theories to decision-makers without overstating the evidence.

**Question 10 (moderate)** — True, False, or Cannot Say: "Larger organisations produced more complete disclosures than smaller ones."

**Correct answer: False**

**Explanation:** The passage states: "No relationship was found between organisation size and disclosure completeness." The claim of a positive size–completeness relationship contradicts this reported finding, so within the world of the text the statement is False. Be careful with a subtle point: the text reports the *study found no relationship* — a reported negative finding is still a finding, and the statement contradicts it. Cannot Say would only be right if the passage had been silent on organisation size altogether.

**Passage D — Proposed policy wording (Questions 11–13)**

*"Staff may reuse datasets collected by other teams for new analytical purposes provided that: (a) the reuse is compatible with the purpose for which the data was originally collected; (b) a reuse record is logged in the data catalogue before analysis begins; and (c) where the dataset contains personal data, the data protection team confirms the lawful basis for reuse. The data ethics team should be consulted where the reuse may affect vulnerable groups, and must be consulted where the reuse involves automated decision-making. Consultation with the data ethics team does not substitute for condition (c)."*

**Question 11 (moderate)** — True, False, or Cannot Say: "A team reusing a dataset containing no personal data must obtain confirmation from the data protection team."

**Correct answer: False**

**Explanation:** Condition (c) is expressly conditional: "*where the dataset contains personal data*, the data protection team confirms the lawful basis". If no personal data is involved, condition (c)'s trigger is absent, so the confirmation requirement does not apply (conditions (a) and (b) still do). The statement asserts an unconditional requirement that the text makes conditional — False. Reading the scope of a qualifying clause ("where…") is precisely what you do when you assess whether a proposed policy is drafted tightly enough.

**Question 12 (challenging)** — True, False, or Cannot Say: "A reuse involving automated decision-making that affects vulnerable groups requires data ethics team consultation."

**Correct answer: True**

**Explanation:** Two overlapping clauses govern consultation: "should be consulted" where vulnerable groups may be affected (advisory), and "must be consulted" where automated decision-making is involved (mandatory). The scenario involves automated decision-making, so the mandatory "must" clause applies on its own; the vulnerable-groups element adds an advisory reason but is not needed to establish the requirement. The statement is True. The should/must distinction — one of the sharpest drafting conventions in government policy — is a favourite of test writers because sloppy readers treat the words as synonyms.

**Question 13 (challenging)** — Which of the following best summarises the *purpose* of the final sentence ("Consultation with the data ethics team does not substitute for condition (c)")?

A) To make ethics consultation optional in all cases.
B) To prevent teams treating an ethics conversation as if it satisfied the separate legal requirement for a lawful basis confirmation.
C) To subordinate the data protection team to the data ethics team.
D) To remove condition (c) for reuses that have had ethics consultation.

**Correct answer: B**

**Explanation:** The sentence anticipates a predictable failure mode: a team consults the ethics team, feels "cleared", and skips the data protection confirmation. The drafter forecloses that reading by stating the two are not interchangeable. Option A misreads it (the sentence does not alter when consultation is required); options C and D invert its effect. Recognising *why* a sentence exists — the misreading it is designed to block — is high-level comprehension, and it is exactly the perspective you bring when you strengthen a colleague's draft policy against future misinterpretation.

**Question 14 (moderate)** — Standalone comprehension

A minister's foreword to a data strategy states: *"We will be transparent by default about how we use the public's data, withholding details only where disclosure would enable fraud or compromise security."*

True, False, or Cannot Say: "The strategy commits to publishing all details of public data use."

**Correct answer: False**

**Explanation:** The commitment is transparency *by default*, with two stated exceptions (fraud enablement and security compromise). "All details" admits no exceptions, so the statement overstates the commitment and is contradicted by the qualifying clause. Watch for absolute words — all, never, only, every — inserted into statements about qualified text; they are the most common device for turning a True-looking statement into a False one.

**Passage E — Internal audit finding on ethics governance (Questions 15–18)**

*"The audit examined whether ethics review recommendations were implemented by project teams. Of the 60 recommendations sampled, 44 were implemented in full, 10 in part, and 6 not at all. In four of the six unimplemented cases, project documentation recorded a reasoned decision to accept the associated risk; in the remaining two, no record of any decision was found. The audit did not assess whether the recommendations themselves were proportionate. The ethics team's tracking spreadsheet was found to be accurate in all sampled cases. The audit rates the overall control environment as 'moderate', noting that the absence of a decision record in any unimplemented case is inconsistent with the organisation's governance manual, which requires all departures from ethics recommendations to be documented and approved at deputy director level."*

**Question 15 (easy)** — True, False, or Cannot Say: "More than 70% of sampled recommendations were implemented in full."

**Correct answer: True**

**Explanation:** 44 of 60 were implemented in full; 44 ÷ 60 = 73.3%, which exceeds 70%. As in Question 8, do the small calculation rather than estimating — 44/60 is close enough to the 70% threshold (42/60) that eyeballing is risky. The habit of computing rather than guessing marginal thresholds is precisely what separates a defensible audit summary from a challengeable one.

**Question 16 (moderate)** — True, False, or Cannot Say: "The two undocumented unimplemented recommendations breached the organisation's governance manual."

**Correct answer: True**

**Explanation:** Chain two pieces of the text. The governance manual "requires all departures from ethics recommendations to be documented and approved at deputy director level". The two cases in question are departures (recommendations "not at all" implemented) for which "no record of any decision was found". An undocumented departure fails the documentation requirement, and the audit itself says the absence of a decision record "is inconsistent with the organisation's governance manual". The inference requires assembling premises from different sentences — a step up from single-sentence matching, and exactly how you would read an audit report before deciding what to escalate. Note what you cannot conclude: nothing tells you *who* was at fault or whether approval was sought orally; the breach of the documentation requirement, though, is established by the text.

**Question 17 (challenging)** — True, False, or Cannot Say: "Some of the ethics team's recommendations were disproportionate."

**Correct answer: Cannot Say**

**Explanation:** The passage states: "The audit did not assess whether the recommendations themselves were proportionate." The text is explicitly silent on proportionality — it neither confirms that any recommendation was disproportionate nor asserts that all were proportionate. The statement can be neither verified nor contradicted from the passage, so Cannot Say. Contrast this with Question 10's structure: there, the study *reported a finding* of no relationship (decisive, so False); here, the question was *never examined* (silence, so Cannot Say). Distinguishing "investigated and found nothing" from "not investigated" is one of the sharpest reading distinctions in assurance work — and in test design.

**Question 18 (moderate)** — Which of the following best summarises the audit's overall message?

A) The ethics team's tracking is unreliable and its recommendations are widely ignored.
B) Implementation is largely good and tracking is accurate, but the failure to document risk-acceptance decisions in a minority of cases is a governance weakness.
C) The organisation's governance manual is too demanding for project teams to follow.
D) All departures from ethics recommendations were properly approved.

**Correct answer: B**

**Explanation:** Option B captures the balance of the finding: strong implementation (44 full, 10 partial, of 60), an accurate tracking spreadsheet, a "moderate" overall rating, and one identified control weakness (two undocumented departures). Option A contradicts the text twice — tracking was "accurate in all sampled cases", and 6 of 60 unimplemented is not "widely ignored". Option D is contradicted by the two cases with no decision record. Option C expresses an opinion the audit never offers. Best-summary questions reward weighing all the evidence in proportion — precisely the distillation skill your role profile describes as reading complex documents and distilling what is relevant, and the difference between briefing your board accurately and briefing it alarmingly.

**Question 19 (challenging)** — Standalone inference

A supplier's transparency statement reads: *"We never sell customer data. Aggregated, anonymised insights derived from customer data may be shared with commercial partners under licence."*

True, False, or Cannot Say: "The supplier provides commercial partners with material derived from customer data in exchange for payment."

**Correct answer: True**

**Explanation:** Parse the two sentences together. The first rules out selling *customer data* itself. The second confirms that *insights derived from customer data* "may be shared with commercial partners under licence" — and a licence to commercial partners is an exchange on commercial terms, i.e. for payment. So material derived from customer data does reach commercial partners commercially: True. The statement is carefully drafted to sound like a blanket denial while confirming the derived-data trade — the word "never" attaches only to raw data sales. Reading what a carefully lawyered sentence *does not* deny is a core professional skill for anyone who assesses vendor claims, and test writers love this structure because the reassuring first sentence primes an instinctive "False". If you hesitated at "under licence" implying payment, note that a licence to commercial partners is the standard textual signal of a commercial arrangement; the deliberately harder judgement here mirrors the real ambiguity you would probe in a supplier meeting — and in a live test, choose the best-supported reading rather than retreating to Cannot Say whenever any interpretive step is required.

### Preparation tips

- **Answer from the text alone.** Your subject-matter expertise is an asset everywhere except here: if the passage conflicts with what you know about UK data policy, the passage wins. Practise consciously suspending outside knowledge.
- **Master the Cannot Say discipline.** Cannot Say means the text neither confirms nor contradicts the statement. Before choosing it, check the passage genuinely says nothing decisive — reported negative findings (Question 10) and disclaimers (Question 4) are decisive.
- **Read modal verbs and qualifiers forensically.** May/must/should, "by default", "where", "at its discretion", "and/or" — underline them mentally. Most answers turn on one such word.
- **Scan the statement first, then hunt the passage.** Read the question statement, identify its key terms, and locate the governing sentence, rather than memorising the whole passage upfront. It is faster and more accurate under a one-minute-per-question budget.
- **Practise on your professional genre.** Take a real framework, standard, or consultation document and write your own True/False/Cannot Say items for a colleague — composing items teaches you exactly how the distinctions work.
- **Do the embedded arithmetic.** When statements involve fractions of counts ("fewer than a quarter"), calculate; do not estimate.

### Common pitfalls

- **Importing expert knowledge.** As a data ethics lead you know the UK GDPR, the Data Ethics Framework, and ICO guidance well — which makes you *more* likely than most candidates to answer from memory instead of the passage. This is the pitfall to guard hardest against.
- **Treating conjecture as finding.** "The authors consider it plausible" is not a result (Question 9). Confusing a likely outcome with a stated fact is the classic verbal reasoning error.
- **Missing the force of disclaimers.** Sentences like "nothing in this framework removes…" are decisive statements, not filler; they convert a tempting Cannot Say into a firm False (Question 4).
- **Absolute-word traps.** Statements adding "all", "always", "mandatory", or "every" to qualified text are usually False (Questions 2 and 14).
- **Reading the whole passage first.** Under time pressure, full read-throughs before seeing the questions waste your budget. Skim structure, then work statement by statement.
- **Should/must blindness.** In government drafting these words allocate obligation differently (Question 12); tests exploit readers who blur them.

One closing thought for this section: of the four assessments, verbal reasoning is the one where your daily practice gives you the strongest raw material and the strongest temptation at once. You read frameworks, audit findings, and lawyered vendor statements every week, so the genre holds no fear — but the very expertise that lets you anticipate what a policy *ought* to say is what the test punishes when the passage says something subtly different. Treat each passage as a new jurisdiction whose only law is its own text, and you will convert your professional reading habits into a genuine advantage rather than a liability.

## Workplace job-specific situational judgement assessment

### About this assessment

A workplace job-specific situational judgement assessment (SJT) evaluates your decision-making, interpersonal skill, and professional conduct through realistic workplace dilemmas. Unlike the cognitive, numeric, and verbal assessments, there is usually no single objectively right answer: several responses may seem reasonable, and the test measures how well your behavioural choices align with the values of the organisation and the demands of the role. Response formats vary — most commonly you will be asked to identify the **most effective** and **least effective** actions from a set, or to rank or rate every option from best to worst. Timing is generous or absent, because the test measures judgement, not speed.

For a data ethics lead, the SJT is where the role's essence is examined. Your work is almost entirely situational: mediating between parts of the organisation, hosting difficult discussions, helping people ask questions and express concerns, building consensus among independent stakeholders, and constructively challenging colleagues without losing their trust. The scenarios below are drawn directly from those duties, and the scoring logic reflects UK public sector values: serving user needs, transparency, honesty and objectivity, collaboration, accessibility, and inclusion. At lead level, assessors also look for judgement about *escalation* — knowing what to resolve yourself, what to take to the head of data ethics, and what must go to formal governance — and for the maturity to challenge without grandstanding and to compromise without capitulating.

### What it measures for your role

- **Communicating between the technical and non-technical**: scenarios test how you manage expectations, handle active and reactive communication, and support or host difficult discussions with diverse senior stakeholders.
- **Communication (data ethics)**: several dilemmas turn on translating a technical concern so a non-technical decision-maker grasps its weight — and on supporting data scientists and engineers rather than policing them.
- **Data ethics and privacy**: the dilemmas embed genuine ethical and privacy trade-offs, testing whether you identify the real concern and situate it in the wider organisational context.
- **Empathy and inclusivity**: scenarios involve underrepresented groups, community engagement, and bias; the effective options are those that widen participation and take lived experience seriously.
- **Managing decisions and risks**: options are differentiated by proportionality — the strongest responses match the intervention to the scale of the risk and build consensus rather than imposing outcomes.
- **Problem management**: some scenarios present recurring or systemic failures, testing whether you fix root causes and take preventive measures rather than treating symptoms.
- **Product ownership (data ethics)** and **Stakeholder relationship management**: scenarios about tools, training, feedback, and long-term relationships test whether you protect both the work and the relationships it depends on.

### Practice questions

**Question 1 (moderate) — The deadline-pressured data science team**

A data science team is due to deploy a model that prioritises housing repair requests. Two days before deployment, their own testing reveals the model performs noticeably worse for households where English is not the first language. The delivery manager tells you: "We've got a hard ministerial deadline. Can we deploy now and fix the disparity in the next sprint?"

Rate the options:

A) Agree to deployment, since the team has been transparent with you and has committed to a fix.
B) Refuse outright and inform the minister's office that the team attempted to deploy a biased model.
C) Convene the delivery manager and the head of data ethics the same day, quantify the disparity and its harm, and jointly agree either a mitigation that can ship with the model (for example, human review of affected cases) or a short, defensible delay with a clear communication to the senior owner of the deadline.
D) Tell the team it is their decision, since the ethics team is advisory.

**Most effective: C. Least effective: B.**

**Explanation:** Option C does everything the role demands: it acts at the speed of the problem, uses evidence rather than assertion (quantify the disparity), involves the right level of authority (the head of data ethics, matching your lead-level escalation duty), and searches for a proportionate path — mitigation-with-deployment or a short delay — rather than a binary fight between "ship it" and "stop everything". It also treats the deadline's owner as a stakeholder to be communicated with, not an obstacle. Option A converts transparency into a free pass; a known disparity affecting a vulnerable group, deployed knowingly, is a much worse position — ethically and reputationally — than a short delay, and "fix it next sprint" commitments are notoriously fragile once a system is live. Option D abdicates: advisory does not mean indifferent, and a lead who shrugs teaches the organisation that ethics review is optional. Option B is least effective because it detonates the relationship and the escalation ladder simultaneously: it mischaracterises the team (they disclosed the issue themselves — behaviour you want to reward, not punish), bypasses your own head of data ethics, and turns a solvable engineering-and-timing problem into a political incident. Public sector values at stake: user needs (the affected households), proportionality, collaboration, and honesty without theatrics.

**Question 2 (moderate) — The dismissive senior stakeholder**

At a programme board, a senior director interrupts your presentation on ethical risks in a data-sharing initiative: "This ethics stuff is slowing us down. The public expects us to deliver. Can we take this offline?"

Rate the options:

A) Accept moving it offline, then follow up with a concise one-page brief linking each ethical risk to a delivery risk the director cares about, and request a short one-to-one before the next board.
B) Insist on finishing your slides, stating that ethics cannot be an afterthought.
C) Say nothing further at the board and quietly log the risks in the risk register.
D) Move it offline, and additionally ask the board chair to record a decision that the initiative proceeds with ethical risks unreviewed.

**Most effective: A. Least effective: C.**

**Explanation:** Option A reads the room without surrendering the substance. Accepting "offline" avoids a status contest you would likely lose in the moment, while the follow-up translates ethical risks into the director's own currency — delivery risk, legal exposure, public trust — which is the heart of communicating between the technical and non-technical and of managing expectations with senior stakeholders. The one-to-one builds the long-term strategic relationship your stakeholder management skill calls for. Option B may feel principled but hosting difficult discussions well means choosing the ground; forcing a confrontation at the board entrenches the "ethics = friction" narrative. Option D is interesting and not wholly wrong — making the risk acceptance explicit is good governance — but as the *most* combative-formal move available it should follow, not precede, an attempt at persuasion; deployed cold, it reads as weaponising the minutes. Option C is least effective: silent logging is passive, ensures the risks influence nothing, and fails the duty to raise awareness of data ethics issues. A register entry no one discusses protects only the author.

**Question 3 (challenging) — The colleague's flawed bias audit**

A well-respected data scientist, with whom your team has worked hard to build trust, circulates a bias audit concluding a recruitment-screening model is "fair across all groups". Reviewing it, you find the audit tested only gender, ignored ethnicity and disability, and used a sample too small to detect meaningful disparities for smaller groups.

Rate the options:

A) Reply-all to the circulation list correcting the audit's flaws so no one is misled.
B) Speak with the data scientist privately first, walk through the gaps, and offer to co-design an extended audit — then ensure the circulated conclusion is corrected to the same audience once agreed.
C) Say nothing, since criticising the audit could damage the relationship your team depends on.
D) Raise it at the next ethics board as an example of inadequate audit practice.

**Most effective: B. Least effective: C.**

**Explanation:** Option B is the textbook expression of "critique colleagues' findings to assure best practice" done in a way that preserves the collaboration it depends on: private first (protecting the colleague's standing), specific and technical (the missing protected characteristics, the statistical power problem — demonstrating the fluency your communication skill requires), constructive (co-design the fix), and — crucially — it does not stop at private diplomacy: the incorrect "fair across all groups" conclusion has already reached an audience and must be corrected for that same audience. Option A gets the correction right and the humans wrong: a public reply-all correction humiliates a trusted colleague, and the trust your team spent years building is itself an ethics asset — future teams disclose less to a team that embarrasses them. Option D uses a governance forum for what a conversation could fix, and does so identifiably at the colleague's expense. Option C is least effective and the most seductively rationalised: it privileges a comfortable relationship over people who could face discriminatory screening. Empathy and inclusivity here means empathy for affected applicants first; a lead who stays silent to stay liked has inverted the role.

**Question 4 (moderate) — The community consultation shortfall**

Your organisation is consulting on a new data-sharing scheme. Analysis of consultation responses shows almost no participation from disabled people and low-income households — two groups the scheme would affect most. The policy lead says: "We've met the statutory consultation requirement. Extending would cost six weeks we don't have."

Rate the options:

A) Accept the position; the statutory requirement is met and the timetable is fixed.
B) Propose targeted, faster engagement — working through disability organisations and community groups, offering accessible formats and small-group sessions — to gather the missing perspectives within the existing timetable, and note in the consultation report which voices remain under-heard.
C) Publicly state that the consultation is invalid.
D) Extend the consultation by six weeks regardless of the policy lead's objection.

**Most effective: B. Least effective: C.**

**Explanation:** Option B embodies the in-depth consulting and outreach strategies your empathy and inclusivity skill names: it distinguishes the *legal floor* (statutory requirement met) from the *ethical standard* (the affected groups' views genuinely inform the decision), then designs a proportionate way to close the gap within real constraints. Recording residual gaps in the report serves transparency — decision-makers should know whose voices are missing. Option A treats compliance as the ceiling; for a data ethics lead, "lawful" is where the analysis starts, not where it ends. Option D might occasionally be right, but you lack the authority to impose it, and bulldozing the policy lead sacrifices the consensus-building your managing decisions and risks skill requires — it also ignores that option B may capture most of the value at a fraction of the cost. Option C is least effective: it is not yours to declare, is probably wrong in law, and converts a fixable inclusion gap into a public credibility crisis for the whole consultation, harming the very policy outcome the missing groups need improved.

**Question 5 (challenging) — The anxious whistleblower**

A junior analyst asks to speak with you confidentially. They believe their team is linking datasets in a way that goes beyond what users consented to, but they are afraid: their line manager designed the approach, and they fear being seen as a troublemaker. They ask you not to tell anyone.

Rate the options:

A) Promise absolute confidentiality and investigate the linking quietly yourself, never revealing that anyone raised a concern.
B) Thank them, explain honestly what you can and cannot keep confidential, and agree a route that protects them — for example, the ethics team "routinely" reviewing the data-linking practice as part of its work programme so no individual is identifiable as the source — while making sure the concern is properly examined.
C) Tell them to raise it with their line manager first, since that is the proper channel.
D) Report the team to the data protection officer immediately, naming the analyst as the source so the concern is on the record.

**Most effective: B. Least effective: D.**

**Explanation:** Your role profile explicitly includes helping people "ask questions, express concerns and discuss ethical dilemmas" — which only works if raising a concern is safe. Option B does three hard things at once: it is honest about the limits of confidentiality (never promise what a serious finding might not let you keep), it engineers genuine protection (folding the review into routine programme activity de-identifies the source), and it ensures the substantive question — consent scope in data linking, a real privacy issue — is investigated rather than absorbed into reassurance. Option A's promise of absolute secrecy is a trap: if the review uncovers unlawful processing, you may be obliged to act in ways that strain the promise, and broken promises destroy the safe channel for everyone who comes after. Option C misreads power: sending a frightened junior back to the manager who designed the practice is procedurally tidy and humanly obtuse — it predictably ensures silence. Option D is least effective: it maximises the analyst's exposure against their express wishes, teaches the organisation that speaking to the ethics team gets you named, and poisons the well permanently. Note that escalation to the DPO may well be *right* — but option B reaches it with the source protected; D's failure is the naming, not the reporting.

**Question 6 (moderate) — The vendor's opaque algorithm**

A procurement team asks you to sign off a contract for a third-party fraud-analytics product. The vendor refuses to disclose how its risk scores are calculated, citing commercial confidentiality. The product performs well in trials, the price is good, and procurement wants to close this week.

Rate the options:

A) Sign off; trial performance is what matters, and vendors are entitled to protect their intellectual property.
B) Refuse sign-off and recommend the organisation build its own system instead.
C) Withhold sign-off for now and negotiate concrete transparency mechanisms into the contract — access to feature-level explanations for individual decisions, rights to audit for bias, documentation of training data provenance, and exit provisions if audits fail — accepting the deal only with enforceable safeguards.
D) Sign off but write a memo recording your concerns about opacity.

**Most effective: C. Least effective: D.**

**Explanation:** Option C treats the impasse as a design problem, not a yes/no gate. Commercial confidentiality and meaningful accountability can usually be reconciled through contract: audit rights, explanation interfaces, and exit clauses give the organisation what it ethically needs — the ability to detect and remedy unfair outcomes, and to explain decisions to affected citizens — without demanding the vendor's source code. This is translating theoretical principles (transparency, accountability) into practice, the defining move of your product ownership skill, and using contract negotiation as a risk methodology proportionate to the risk. Option A confuses trial accuracy with accountability: a system can perform well on average while failing specific groups, and with no audit rights you would never know. Option B is disproportionate — building in-house is a multi-year answer to a question the contract can solve — though it is at least a genuine safeguard, unlike option D. Option D is least effective because it is pure self-protection: the memo changes nothing for the citizens scored by an unaccountable system; it merely documents that you foresaw the harm you approved. An ethics function that signs off while filing objections has become ornamental.

**Question 7 (moderate) — The training programme nobody attends**

Your flagship data ethics training is mandatory for data practitioners, yet completion sits at 40%. Directors send apologies; teams cite delivery pressure. The head of data ethics asks you to fix uptake.

Rate the options:

A) Ask the executive committee to enforce completion, with non-compliance reported to directors quarterly.
B) Investigate why people are not attending — timing, length, format, perceived relevance — redesign the offer around what you learn (shorter, role-specific, embedded in existing team rituals), pilot the redesign with a sceptical directorate, and pair it with visible senior sponsorship.
C) Reduce the training requirement so the completion statistics improve.
D) Email all staff reminding them the training is mandatory.

**Most effective: B. Least effective: C.**

**Explanation:** Option B treats low uptake as a product problem and applies your product ownership skill: gather user feedback, capture needs, redesign the deliverable, pilot, iterate — while recognising that enforcement without a better product breeds resentful, box-ticking compliance that defeats the training's actual purpose (changed practice, not certificates). Piloting with a sceptical directorate is smart evaluation design and smart politics. Option A is not wrong as a *component* — mandatory training does need teeth, and senior sponsorship appears within option B — but leading with enforcement addresses the symptom (attendance) rather than the cause (a product people avoid). Option D is a weaker version of A: reminder emails about unpopular training are organisational wallpaper. Option C is least effective: it games the metric instead of improving the outcome — precisely the practice a data ethicist exists to challenge in others. Optimising a number at the expense of what it measures would be professionally self-undermining in the most literal sense.

**Question 8 (challenging) — Mediating between privacy and public benefit**

Two parts of your organisation are in deadlock. A health-analytics team wants access to linked administrative data to target support at families at risk of homelessness — evidence suggests earlier intervention could prevent serious harm. The privacy team objects: the linkage repurposes data collected for benefits administration, and affected families never consented to it. Both sides have escalated to the ethics team, and both regard you as their ally.

Rate the options:

A) Side with the privacy team; consent is fundamental and the linkage should not proceed.
B) Side with the analytics team; preventing homelessness clearly outweighs a technical consent objection.
C) Convene a structured deliberation: get both sides to agree the facts (what data, what linkage, what safeguards), map the harms of proceeding *and of not proceeding*, explore middle designs — minimised datasets, pseudonymisation, an opt-out with meaningful notice, external ethics scrutiny, a time-limited pilot with published evaluation — and take a documented recommendation weighing both duties to the appropriate decision-maker.
D) Decline to get involved, since the ethics team should stay neutral in interdepartmental disputes.

**Most effective: C. Least effective: D.**

**Explanation:** This is your role profile in a single scenario: "listen to, convene, advise and mediate between various parts of the organisation." Option C's strength is procedural before it is substantive: deadlocks like this usually rest on contested facts and unexamined all-or-nothing framings. Insisting that the harms of *inaction* be mapped alongside the harms of action is the mark of mature ethical analysis — privacy harms are real, and so are preventable homelessness harms; neither side's value automatically trumps. Exploring middle designs (data minimisation, opt-outs, external scrutiny, pilot-with-evaluation) frequently dissolves the dilemma, and routing the final recommendation to an accountable decision-maker respects governance: you advise, convene, and structure; you do not seize the decision. Options A and B share the same flaw in mirror image: they pick a winner before doing the work, reducing a genuine values conflict to a slogan ("consent is fundamental" / "benefit outweighs"). Either might be where the analysis *lands*, but as opening moves they are prejudgement. Option D is least effective: neutrality between positions does not mean absence from the process — convening this exact conversation is what the organisation employs a data ethics lead to do. Declining is not neutrality; it is vacancy.

**Question 9 (moderate) — The AI-generated briefing error**

Preparing for a conference where you represent the organisation, you discover that a widely circulated internal briefing about your ethics programme — drafted by a colleague using a generative AI tool — contains a fabricated statistic: it claims "external research shows our framework reduced data incidents by 60%". No such research exists.

Rate the options:

A) Quietly correct your own conference materials; the internal briefing is the author's responsibility.
B) Alert the colleague, help them issue a correction to everyone who received the briefing, and propose a light-weight verification step for AI-assisted drafting so it does not recur.
C) Email the colleague's director to report misuse of AI tools.
D) Raise the incident at the all-staff meeting as a cautionary tale, without naming the colleague.

**Most effective: B. Least effective: A.**

**Explanation:** Option B pairs the immediate fix (correction to the actual audience of the error — fabricated evidence about an *ethics* programme is reputationally radioactive precisely because your function trades on accuracy) with the systemic fix (a verification step), which is problem management done properly: resolve, then prevent. It also treats the colleague as a partner in the correction rather than a defendant. Option C escalates a good-faith error into a disciplinary matter before giving the colleague any chance to fix it — disproportionate, and corrosive to the culture of safe disclosure you exist to build. Option D fixes nothing (the briefing's recipients still hold the false statistic) and, in a real organisation, "without naming" rarely conceals identity for long. Option A is least effective because it is knowing complicity: you would present accurate figures at the conference while a falsehood circulates internally under your programme's name. An ethics lead who corrects only their own copy of a known fabrication has adopted exactly the compartmentalised responsibility their role exists to challenge.

**Question 10 (challenging) — The head of data ethics is away**

Your head of data ethics is on leave and unreachable for two weeks. A newspaper contacts your organisation's press office with detailed, partially accurate claims that a pilot algorithm disadvantaged single parents, and asks for comment within 48 hours. The press office asks you, as the senior ethics person available, what the organisation should say.

Rate the options:

A) Advise the press office to deny the claims, since they are partially inaccurate.
B) Advise saying nothing until the head of data ethics returns.
C) Rapidly verify what the pilot's records actually show, brief the press office and the relevant senior owner on what is accurate and what is not, and support a response that acknowledges what is true, corrects what is false, and states what the organisation is doing about the genuine issue — flagging the matter for the head of data ethics on their return.
D) Speak to the journalist yourself to explain the technical detail, since you understand it best.

**Most effective: C. Least effective: A.**

**Explanation:** Option C is lead-level deputising: you step up in the head's absence (the role profile says you support the head of data ethics, which includes covering their function), you ground the response in verified fact rather than instinct, you work *through* the proper channels — the press office owns media handling; the senior owner owns the decision — and you ensure continuity by briefing your head on return. The substance reflects public sector transparency values: acknowledge the true part, correct the false part, and show remediation; partial denials of partially true claims are how organisations convert a one-day story into a month-long scandal. Option B mistakes absence for paralysis — a 48-hour media deadline will not wait two weeks, and "no comment" plus a later correction is far more damaging than a same-week accurate response. Option D violates channel discipline: technical understanding does not make you the spokesperson, and freelancing with journalists undermines the press office and creates a second, unmanaged story. Option A is least effective: advising a denial you know to be partially false is the one option that is not merely unwise but dishonest — the single fastest way for an ethics function to forfeit its authority, internally and publicly.

**Question 11 (moderate) — The external academic's request**

An academic you collaborate with asks for access to internal ethics review case files "to advance the field", offering co-authorship on the resulting paper. The files contain candid, sometimes unflattering details about internal projects and the concerns teams raised in confidence.

Rate the options:

A) Share the files; the research benefit is real, academic collaboration is in your role profile, and the academic promises to anonymise everything.
B) Decline all engagement to avoid any risk.
C) Explore a governed route: agree the research value, then work through what could be shared under what safeguards — formally anonymised or synthesised case summaries, an information-sharing agreement, internal review of the material before release, and consent from teams whose cases would feature — declining the raw files.
D) Share the files but ask the academic to keep their use discreet.

**Most effective: C. Least effective: D.**

**Explanation:** Your applied social sciences skill explicitly includes working with academics and external researchers, so option B's blanket refusal wastes genuine value — advancing the field is part of how data ethics practice improves everywhere, including in your organisation. But the case files exist because teams spoke candidly on an understanding of internal confidence; releasing them raw (option A) would breach that trust and chill every future disclosure, and "the academic promises to anonymise" outsources your duty of care at the moment it matters most. Option C threads it: preserve the collaboration, protect the confidence, and use the governance instruments — agreements, review-before-release, consent of featured teams — that make sharing defensible. It applies your own data ethics standards to your own data, which is the credibility test every ethics function eventually faces. Option D is least effective because it adds concealment to the breach: sharing sensitive material *and* asking for discretion signals that you know it is wrong. The least defensible position in ethics is the one you would not want examined.

**Question 12 (moderate) — Ranking under a live incident**

It emerges that a dashboard your organisation published three days ago inadvertently allows small groups of identifiable individuals to be singled out when filters are combined (a re-identification risk). It is being discussed on social media. Rank these four actions in the order you would take them:

1. Get the dashboard's publishing team to remove or fix the affected feature immediately.
2. Establish exactly which data combinations create the risk and who could be affected.
3. Notify the data protection officer so breach-assessment obligations are met.
4. Commission a review of pre-publication checks so the failure mode is caught in future.

**Most defensible order: 1, 3, 2, 4** (with 1 and 3 effectively simultaneous).

**Explanation:** In a live exposure, stopping ongoing harm dominates: every hour the feature stays up, more combinations can be tried, so takedown or feature-disable comes first — you do not need the full analysis to justify making people safer. Notifying the DPO comes essentially in parallel: a re-identification risk in published data plausibly engages statutory breach-assessment clocks, and the DPO cannot start their assessment until told; delaying notification to "understand it fully first" is a recognised failure pattern in incident handling. The detailed analysis of affected combinations (2) then proceeds properly — it informs the DPO's assessment, any notification of affected individuals, and the fix's completeness. The preventive review (4) is essential but last: problem management's "anticipate problems" duty is about sequencing, not skipping — root-cause work done during firefighting is done badly. Candidates commonly over-rank 2 (analysis before action feels rigorous, but leaves the public exposed meanwhile) or under-rank 3 (treating the DPO as bureaucracy rather than as a legal clock already ticking).

### Preparation tips

- **Anchor in public sector values.** Before the test, re-read the Civil Service values (integrity, honesty, objectivity, impartiality) and the service standard's emphasis on user needs, accessibility, and inclusion. Effective options almost always serve affected people first, are honest even when uncomfortable, and work through legitimate channels.
- **Look for the option that pairs action with relationship.** At lead level, the best responses usually fix the substance *and* protect the human infrastructure — the trust, the escalation route, the safe channel. Options that achieve one at the cost of the other are rarely "most effective".
- **Check for root cause.** Where a scenario hints at recurrence (the fifth flawed self-assessment, the chronically avoided training), the strongest option treats causes, and the weakest treats symptoms or games the measure.
- **Calibrate escalation.** Ask of each option: is this the right level, the right channel, and the right moment? Premature escalation and non-escalation are both marked down; well-sequenced escalation — try influence, then formalise — is marked up.
- **Answer as the role, honestly.** Do not choose what you imagine a saint would do; choose what an effective, values-driven data ethics lead would actually do on a Tuesday. Idealised answers that ignore constraints score poorly, and so does cynicism.
- **Practise articulating why.** For each practice scenario, say aloud why the weakest option fails. The habit of articulating trade-offs is also, conveniently, your day job.

### Common pitfalls

- **Choosing the idealistic over the effective.** "Refuse and report to the minister" feels righteous but ignores channels, proportionality, and relationships. SJTs reward practical wisdom, not moral display.
- **Selecting passive options.** Quietly logging risks, writing memos-to-file, waiting for someone senior to return — options that delay action, pass the problem on, or protect only you are systematically scored as least effective.
- **Purity about your own function.** Beware options where the ethics team wins the argument and loses the mission — public corrections that humiliate allies, sign-off refusals where negotiation would deliver safeguards. Your influence is the instrument; options that spend it cheaply are weak.
- **Ignoring the stated culture.** UK public sector SJTs reward collaboration, transparency, inclusion, and user focus. An option that is decisive but unilateral usually loses to one that is decisive and consensual.
- **Missing whose interests are primary.** In every scenario, locate the affected citizens or users; options ordered around institutional or personal comfort rather than their interests are the classic least-effective picks.
- **Over-consulting.** The mirror-image trap: options that convene a working group for something needing action today. Match the deliberation to the clock — a live re-identification risk and a training redesign run on different timescales.

## Conclusion

You have now worked through four substantial, job-specific assessments — cognitive ability, numeric reasoning, verbal reasoning, and situational judgement — every one of them built from the real material of your role: ethics review triage, bias audits, policy frameworks, consultation gaps, deadlocked stakeholders, and the daily craft of challenging colleagues while keeping their trust.

A few themes are worth carrying forward. First, the assessments are not a distraction from your professional practice; they are a compressed mirror of it. The denominator discipline that catches a test distractor is the same discipline that catches a misleading fairness statistic. The Cannot Say judgement that separates finding from conjecture is the same judgement you apply to an academic claim or a vendor's promise. The situational instinct to pair decisive action with protected relationships is the essence of leading a data ethics function. Preparing for these tests is, quietly, professional development.

Second, familiarity compounds. If any section felt uncomfortable — perhaps the speed of numeric extraction, or resisting your own expertise in verbal reasoning — that is useful information, not a verdict. Return to those sections, practise little and often, and time yourself as the real assessments will. Performance on every one of these formats improves substantially with practice, and you have the analytical habits to improve quickly.

Third, on the day: rest properly, do the untimed warm-up questions, read precisely, manage the clock, and let go of any single hard question. You are not being asked to be perfect; you are being asked to demonstrate, under structured conditions, the judgement you already exercise.

Finally, keep growing. Talk to your head of data ethics about the capabilities you want to stretch; seek feedback from the data scientists, policy leads, and researchers you serve; keep reading across the social sciences that ground your practice. The GDAD capability framework you work within is a map for that growth, and documents like this one are simply waypoints. You do demanding, genuinely important work — helping an organisation use data in ways worthy of the public's trust. Approach your assessments with the same care, curiosity, and integrity you bring to that work, and you will represent yourself well. Good luck — you are better prepared than you think.
