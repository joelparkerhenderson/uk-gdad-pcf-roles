# Data governance manager - Psychometric Assessment Resources

## Introduction

Welcome! This guide has been created especially for you as a data governance manager working within the UK Government Digital and Data profession. Whether you are preparing for an upcoming assessment as part of a recruitment or development process, or you simply want to sharpen the mental skills that underpin your day-to-day work, this document will help you practise, reflect, and build confidence.

Psychometric assessments are structured, standardised exercises that measure the abilities and judgement you use at work. They are widely used across the Civil Service and the wider public sector because they are fair, evidence-based, and focused on what actually predicts success in a role. For a data governance manager, that means the ability to reason clearly about frameworks, policies and standards; to interpret data quality metrics, risk figures and maturity scores; to read dense policy and legislative text with precision; and to make sound judgements when stakeholders disagree, risks emerge, or compliance is at stake.

This document is organised around four assessment types, each with its own dedicated section:

1. **Workplace job-specific cognitive assessment** – measuring pattern recognition, logical deduction, error checking, prioritisation and problem solving using the artefacts you really handle: data catalogues, RACI matrices, lineage diagrams, and governance workflows.
2. **Workplace job-specific numeric reasoning assessment** – measuring your ability to interpret tables, percentages, ratios, budgets and performance metrics such as data quality scores, training uptake figures and risk exposure calculations.
3. **Workplace job-specific verbal reasoning assessment** – measuring precise comprehension of the written material you work with every day: data policies, standards documents, stakeholder emails, and audit reports.
4. **Workplace job-specific situational judgement assessment** – measuring how you respond to realistic workplace dilemmas involving data owners, technical teams, senior leaders and the public interest.

Each section explains what the assessment measures, maps it to the specific skills in your role profile, provides a substantial set of practice questions with full worked answers, and finishes with preparation tips and common pitfalls.

How should you use this guide? Three ways work well. First, **practise**: attempt each question under gentle time pressure before reading the answer, so you experience realistic conditions. Second, **self-reflect**: when your answer differs from the suggested one, read the explanation carefully and ask yourself what reasoning step you missed — this is where the deepest learning happens. Third, **prepare**: revisit the preparation tips shortly before any real assessment, so the practical advice is fresh in your mind.

Take your time, be kind to yourself, and remember: these skills improve with practice. Let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive ability assessment is a targeted psychometric test designed to measure the exact mental processes needed for your role — not abstract puzzle-solving, but the practical reasoning you use when you plan, monitor and enforce the management of data assets. Unlike a generic IQ test, it uses realistic workplace scenarios and materials, so the questions look and feel like a working day: a data catalogue with inconsistencies to spot, a RACI matrix with a logical gap, a governance workflow with a missing step, or a set of competing priorities to sequence.

Typical format and timing: these assessments are usually delivered online and timed, most commonly 15 to 30 minutes. Questions are multiple choice, and scoring is objective — your results are compared against a benchmark or norm group rather than judged subjectively. Many platforms give you short, ungraded practice questions first so you can get used to the interface, and some adapt the difficulty of later questions based on your earlier answers. Employers typically receive a breakdown of speed versus accuracy rather than a single score, so working carefully matters as much as working quickly.

Why does this matter for a data governance manager? Your role sits at the intersection of detail and design. You must catalogue, monitor and identify essential data assets — which demands error checking and pattern recognition. You must develop end-to-end governance frameworks — which demands logical deduction about processes, policies and standards, and the ability to reason about what happens at each phase of the data life cycle. You must support risk processes around data — which demands sound prioritisation when several issues compete for attention. A cognitive assessment gives employers (and you) evidence of exactly these capacities.

### What it measures for your role

The assessment dimensions map directly onto the skills in your role profile:

- **Logical deduction** maps to your **Data governance** skill: developing an end-to-end framework means reasoning about which processes, operational policies and standards must exist, in what order, and what follows if one is missing. It also maps to **Data standards**: analysing the impact if a standard is breached is a deductive exercise — given the rule and the facts, what consequences follow?
- **Error checking** maps to **Data management** and **Data standards**: monitoring compliance with policies and standards in a team means spotting the record, the entry or the clause that does not match the rule.
- **Pattern recognition** maps to **Data maturity** and **Data quality** work: measuring data maturity and identifying opportunities to improve the quality and trustworthiness of data both depend on seeing trends and anomalies across assessments, audits and metrics.
- **Prioritisation** maps to **Enabling and informing risk-based decisions**: advising on risk impact and whether it is within risk tolerance requires weighing severity, likelihood and proportionality quickly and consistently.
- **Problem solving with workflows** maps to your duty to **incorporate governance of data into routine processes**: reasoning about process diagrams, approval chains and the data life cycle is central to designing practical governance solutions.
- **Sequencing and dependency reasoning** maps to **Data life cycle**: applying governance at each phase — creation, storage, use, sharing, archiving, disposal — means understanding what must happen before what.

### Practice questions

Work through these at your own pace first; then try again with a timer, allowing roughly 90 seconds to 2 minutes per question.

**Question 1 (easy) — Error checking in a data catalogue**

You are reviewing four new entries in your organisation's data catalogue. Your catalogue standard requires that every entry has: (a) a named data owner, (b) a security classification, (c) a retention period, and (d) a last-reviewed date no more than 12 months old. Today's date is 12 August 2026.

| Entry | Data owner | Classification | Retention | Last reviewed |
|---|---|---|---|---|
| Case Management Records | J. Okafor | OFFICIAL | 7 years | 03 Feb 2026 |
| Staff Survey Responses | (blank) | OFFICIAL | 2 years | 15 May 2026 |
| Grants Payment Ledger | P. Singh | OFFICIAL-SENSITIVE | 7 years | 30 Jun 2025 |
| Website Analytics Feed | L. Hart | OFFICIAL | 26 months | 01 Aug 2024 |

Which entries fail the standard?

A) Staff Survey Responses only
B) Staff Survey Responses and Website Analytics Feed
C) Staff Survey Responses, Grants Payment Ledger and Website Analytics Feed
D) All four entries

**Correct answer: C**

**Explanation:** Check each entry against all four rules, and start by computing the review cut-off once: 12 August 2026 minus 12 months is 12 August 2025, so any last-reviewed date before 12 August 2025 fails rule (d). Case Management Records passes everything. Staff Survey Responses has no named data owner, so it fails rule (a). Grants Payment Ledger was last reviewed on 30 June 2025 — before the 12 August 2025 cut-off, so it fails rule (d); this is the deliberate near-miss that tempts you towards option B, because at a glance "June 2025" feels recent enough. Website Analytics Feed (01 August 2024) is over two years old and clearly fails rule (d) too. So three entries fail: Staff Survey Responses (no owner), Grants Payment Ledger (review out of date), and Website Analytics Feed (review out of date). The lesson: compute the exact threshold first and compare every entry to it, rather than estimating month gaps in your head — near-miss values are placed precisely where estimation breaks down.

**Question 2 (easy) — RACI logic**

Your organisation's RACI matrix for the "approve new data sharing agreement" activity lists: Data Governance Manager — Responsible; Information Asset Owner — Accountable; Data Protection Officer — Consulted; Service Team — Informed. A colleague proposes adding a second Accountable role (the Chief Data Officer) "to be safe". Under standard RACI methodology, what is the flaw in this proposal?

A) The Chief Data Officer should be Responsible, not Accountable
B) A RACI activity should have exactly one Accountable role, because dual accountability creates ambiguity about final ownership
C) The Data Protection Officer must always be the Accountable party for data sharing
D) There is no flaw; RACI allows any number of Accountable roles

**Correct answer: B**

**Explanation:** The defining rule of RACI is one — and only one — Accountable role per activity. Accountability is the single point where the buck stops; splitting it means that when something goes wrong, each Accountable party can assume the other has it covered. Option A invents a placement without justification. Option C is wrong: the DPO advises and is typically Consulted, and independence considerations usually mean the DPO should not own operational decisions. Option D contradicts the method. This mirrors your real duty to "assign ownership of data, ensuring there is a clear RACI matrix in the organisation" — clarity of accountability is the entire point.

**Question 3 (moderate) — Logical deduction from policy rules**

Your data governance framework contains three rules:

1. If a dataset contains personal data, it must have a completed Data Protection Impact Assessment (DPIA) before it is shared externally.
2. If a dataset is classified OFFICIAL-SENSITIVE, external sharing requires senior information risk owner (SIRO) approval.
3. Any dataset without an assigned owner cannot be shared externally under any circumstances.

A service team wants to share Dataset Q externally. Dataset Q contains personal data, is classified OFFICIAL, and has an assigned owner. Its DPIA is in draft. Which statement is logically correct?

A) Dataset Q can be shared once SIRO approval is obtained
B) Dataset Q cannot currently be shared, because rule 1 is not satisfied
C) Dataset Q can be shared, because it is not OFFICIAL-SENSITIVE and has an owner
D) Dataset Q cannot ever be shared externally

**Correct answer: B**

**Explanation:** Apply each rule in turn. Rule 1 fires: the dataset contains personal data, so a *completed* DPIA is required — a draft does not satisfy the condition, so sharing is blocked. Rule 2 does not fire: the classification is OFFICIAL, not OFFICIAL-SENSITIVE, so SIRO approval is not triggered by this rule (option A wrongly adds a requirement that does not apply). Rule 3 does not fire: an owner is assigned. Option C ignores rule 1. Option D overstates: the block is conditional, not permanent — once the DPIA is completed, sharing may proceed. Assessments frequently test whether you can distinguish "blocked until a condition is met" from "prohibited outright"; in governance work that distinction is the difference between advising a team to pause and wrongly telling them the door is closed.

**Question 4 (moderate) — Pattern recognition in data quality trends**

You monitor a monthly completeness score (percentage of mandatory fields populated) for five key data assets. Over six months, the scores are:

- Asset A: 91, 92, 91, 93, 92, 93
- Asset B: 88, 85, 83, 80, 78, 75
- Asset C: 95, 96, 62, 95, 96, 95
- Asset D: 70, 74, 78, 82, 86, 90
- Asset E: 99, 99, 99, 99, 99, 99

Which asset most likely experienced a one-off data pipeline failure, and which shows a systemic, worsening problem?

A) Pipeline failure: C; systemic problem: B
B) Pipeline failure: B; systemic problem: C
C) Pipeline failure: C; systemic problem: D
D) Pipeline failure: E; systemic problem: B

**Correct answer: A**

**Explanation:** Asset C shows a stable pattern (95–96) with a single dramatic dip to 62 in month three, followed by immediate recovery — the signature of a one-off incident such as a failed load or schema change, not a behavioural or process issue. Asset B declines steadily by roughly 2–3 points every month — the signature of a systemic issue such as a process change, staff turnover, or growing backlog that will keep worsening without intervention. Asset D is *improving* steadily (perhaps following a remediation you led), and Asset E is stable and healthy. Distinguishing spike anomalies from trend deterioration is core to your duty to "identify opportunities and make recommendations to improve the quality and trustworthiness of data": the right response to C is a root-cause incident review; the right response to B is a process intervention.

**Question 5 (moderate) — Data life cycle sequencing**

You are designing governance checkpoints across the data life cycle for a new service. Place these five checkpoints in the correct life cycle order:

1. Confirm secure disposal certificate is logged
2. Approve the data collection notice and lawful basis
3. Review access controls for the live database
4. Apply the retention schedule and archive eligible records
5. Validate quality rules on first ingestion

A) 2, 5, 3, 4, 1
B) 5, 2, 3, 1, 4
C) 2, 3, 5, 4, 1
D) 2, 5, 4, 3, 1

**Correct answer: A**

**Explanation:** Map each checkpoint to a life cycle phase: (2) belongs to *creation/collection* — lawful basis and collection notices must be settled before any data exists; (5) belongs to *ingestion/processing* — quality validation happens as data first enters your systems; (3) belongs to *use/storage* — access controls govern the live, in-use phase; (4) belongs to *retention/archiving* — applying the schedule comes after active use; (1) belongs to *disposal* — the final phase, evidenced by a disposal certificate. Option C wrongly places access control review before first ingestion (there is nothing meaningful to control access to until data flows); option D archives before reviewing live access, inverting use and retention. This directly exercises your **Data life cycle** skill: "understand and apply data governance over a data life cycle, ensuring best practice at each phase."

**Question 6 (moderate) — Error checking a metadata standard**

Your metadata standard states: "Dataset identifiers must follow the pattern DEPT-DOMAIN-NNNN, where DEPT is a 3-letter department code, DOMAIN is a 4-letter domain code, and NNNN is a 4-digit number, all separated by hyphens." Which of the following identifiers is fully compliant?

A) DWP-CASE-27
B) HMRC-PAYE-0042
C) DFE-SKIL-0917
D) DVL-FLEET-1204

**Correct answer: C**

**Explanation:** Test each part against the pattern. Option A: "DWP" is 3 letters (pass), "CASE" is 4 letters (pass), but "27" is 2 digits, not 4 (fail). Option B: "HMRC" is 4 letters, but the standard demands a 3-letter department code (fail) — even though it looks the most "real", it breaks the rule, and assessments love to exploit real-world plausibility against literal compliance. Option D: "DVL" passes, but "FLEET" is 5 letters (fail). Option C: "DFE" (3 letters), "SKIL" (4 letters), "0917" (4 digits) — fully compliant. The workplace lesson: monitoring compliance with standards means checking against the written rule, not against what feels familiar. This is your **Data standards** skill in miniature.

**Question 7 (moderate) — Prioritisation under constraint**

At 09:00 you have four items in your queue. You can address only one before a 10:00 governance board meeting:

1. A team reports that last night's data quality dashboard shows a completeness drop from 94% to 91% on a medium-priority asset.
2. The DPO emails: a journalist has submitted an FOI request about data sharing agreements, response due in 15 working days.
3. A service manager reports that an unencrypted extract of OFFICIAL-SENSITIVE personal data may have been emailed to an external partner an hour ago.
4. A colleague asks you to review their draft data literacy training slides for next month.

Which item should you address first?

A) Item 1, because data quality is your core responsibility
B) Item 2, because FOI requests carry statutory deadlines
C) Item 3, because it is a potential data breach requiring immediate containment and assessment
D) Item 4, because it takes the least time and clears your queue

**Correct answer: C**

**Explanation:** Prioritisation questions test severity × urgency reasoning, not task preference. Item 3 is a potential personal data breach involving sensitive material: under UK GDPR, breaches likely to result in risk to individuals must be reported to the ICO within 72 hours of awareness, and the immediate window matters most for containment (recalling the email, alerting the partner, preserving evidence). Item 2 has a statutory deadline — but 15 working days of runway; urgent-seeming, not urgent. Item 1 is a 3-point dip on a medium-priority asset: worth investigating today, not this hour. Item 4 is important for your data literacy duties but has a month of lead time. The pattern to internalise: *irreversible harm in motion beats deadlines with runway, which beat monitoring signals, which beat routine reviews.* This mirrors your **Enabling and informing risk-based decisions** skill — advising on impact and proportionality.

**Question 8 (challenging) — Deduction across a governance workflow**

Your data access request workflow has five stages: Request → Owner Approval → DPO Review (only if personal data) → Security Check (only if classification is OFFICIAL-SENSITIVE or higher) → Provision. An internal audit samples four completed requests:

- Request W: personal data, OFFICIAL. Stages logged: Request, Owner Approval, DPO Review, Provision.
- Request X: no personal data, OFFICIAL-SENSITIVE. Stages logged: Request, Owner Approval, Provision.
- Request Y: personal data, OFFICIAL-SENSITIVE. Stages logged: Request, Owner Approval, DPO Review, Security Check, Provision.
- Request Z: no personal data, OFFICIAL. Stages logged: Request, DPO Review, Provision.

Which requests show workflow non-compliance?

A) X only
B) X and Z
C) W, X and Z
D) Y and Z

**Correct answer: B**

**Explanation:** Derive the required path for each request from its attributes, then compare with the log. W (personal, OFFICIAL) requires Request, Owner Approval, DPO Review, Provision — exactly what was logged: compliant. X (no personal data, OFFICIAL-SENSITIVE) requires Request, Owner Approval, *Security Check*, Provision — the Security Check is missing: non-compliant. Y (personal, OFFICIAL-SENSITIVE) requires all five stages — all logged: compliant. Z (no personal data, OFFICIAL) requires Request, Owner Approval, Provision — the log shows DPO Review instead of Owner Approval. The extra DPO Review is harmless, but *Owner Approval is missing*: non-compliant. Z is the subtle one: candidates often see an "extra" stage and assume over-compliance, missing the absent mandatory stage. When you monitor compliance in real life, check for missing required steps first, then worry about superfluous ones.

**Question 9 (challenging) — Data maturity model reasoning**

Your organisation uses a five-level data maturity model (1 = Initial, 2 = Repeatable, 3 = Defined, 4 = Managed, 5 = Optimising). The model requires that an organisation cannot be rated at a level unless it fully satisfies every lower level. Assessment findings for the "metadata management" dimension:

- Metadata processes are documented and standardised across all major services (a Level 3 criterion) — satisfied.
- Metadata quality is measured with agreed metrics and reviewed quarterly (a Level 4 criterion) — satisfied.
- Some individual teams still maintain ad-hoc, undocumented local glossaries in parallel, contrary to the Level 2 criterion that all metadata practice follows the repeatable organisational process — not satisfied.

What maturity level should you record for metadata management?

A) Level 4, because the highest satisfied criterion is Level 4
B) Level 3, averaging the results
C) Level 1, because the Level 2 criterion is not fully satisfied
D) Level 2, because partial compliance rounds down by one level

**Correct answer: C**

**Explanation:** The model's stated rule is cumulative: a level is only achieved when it and *all lower levels* are fully satisfied. Because a Level 2 criterion fails, the organisation cannot be rated 2, 3 or 4 on this dimension, regardless of impressive higher-level practices — so the rating is Level 1. Options A and B substitute intuitive heuristics ("highest achieved", "average") for the model's actual rule; option D invents a rounding rule that does not exist. This feels harsh, and in a real maturity conversation you would note the strong Level 3–4 practices as evidence that remediation will be quick — but the *recorded* level follows the model. This exercises your **Data maturity** skill ("explain the different data maturity models available; measure data maturity and implement best practices") and a broader assessment lesson: apply the rule as written, not as you wish it were.

**Question 10 (challenging) — Root cause isolation**

Duplicate customer records have risen sharply. You gather four facts:

1. The rise began the same week a new online self-service registration form launched.
2. The form does not check whether an applicant already exists before creating a record.
3. The nightly deduplication job has been running successfully all quarter.
4. Records created by phone agents (who search before creating) show no rise in duplicates.

What is the most logically supported root cause?

A) The deduplication job has silently stopped working
B) The new self-service form creates records without an existing-record check, generating duplicates faster than the nightly job's design anticipated
C) Phone agents have stopped searching before creating records
D) Customers are deliberately registering multiple times

**Correct answer: B**

**Explanation:** Fact 3 directly contradicts option A — the job runs successfully (note: "running successfully" means it executes; the volume may simply exceed what it was designed to catch, which is consistent with B, not A). Fact 4 directly contradicts option C — agent-created records show no rise. Option D is speculation with no supporting fact and is undermined by fact 2 providing a sufficient mechanical explanation. Option B is supported by the conjunction of facts 1 (timing), 2 (mechanism) and 4 (the differential: only the channel lacking the check shows the problem). The differential evidence in fact 4 is the clincher — when one channel with a control is clean and one channel without it is not, the control gap is implicated. This is the reasoning you use when you "support or manage risk processes around data": isolating cause before recommending remediation prevents fixing the wrong thing.

**Question 11 (challenging) — Conditional standards logic**

Your data standards manual says: "A dataset may be published as open data only if (i) it contains no personal data, and (ii) either it is already publicly available elsewhere or the information asset owner has approved publication. Additionally, any dataset containing location data at postcode level requires an aggregation review before publication."

Dataset R contains no personal data, is not available elsewhere, has owner approval, and includes postcode-level location data. Dataset S contains no personal data, is publicly available elsewhere, lacks owner approval, and has no location data. Which is true?

A) R may be published immediately; S may not
B) R requires an aggregation review before publication; S may be published
C) Both require owner approval before anything else
D) Neither may be published

**Correct answer: B**

**Explanation:** Work through R: no personal data (i satisfied); not available elsewhere but owner-approved, so (ii) is satisfied via the second branch of the "either/or". Both main conditions pass — but the additional postcode-level clause fires, so an aggregation review must occur before publication. Work through S: no personal data (i satisfied); publicly available elsewhere, so (ii) is satisfied via the *first* branch — owner approval is not needed when the disjunction is already satisfied. No location data, so no review needed: S may be published. Option A misses R's aggregation clause; option C misreads "either/or" as "and"; option D fails both analyses. The skill being tested — parsing conjunctions, disjunctions and conditional riders precisely — is exactly what you do when you "work with subject matter experts to develop standards, policies and guidance" and then apply them consistently.

**Question 12 (challenging) — Prioritising a remediation portfolio**

You have capacity to sponsor two remediation projects this quarter. The candidates:

- Project 1: Fix the master data feed that four downstream services depend on. Effort: medium. Risk reduced: high (breach of a critical standard affecting statutory reporting).
- Project 2: Refresh the data catalogue's visual design. Effort: low. Risk reduced: negligible.
- Project 3: Implement automated retention-schedule enforcement. Effort: medium. Risk reduced: high (currently manual, with two recent near-misses on over-retention of personal data).
- Project 4: Pilot an AI metadata-tagging tool. Effort: high. Risk reduced: low-moderate (innovation value, but unproven).

Applying risk-based prioritisation, which two projects should you sponsor?

A) Projects 1 and 2
B) Projects 2 and 4
C) Projects 1 and 3
D) Projects 3 and 4

**Correct answer: C**

**Explanation:** Risk-based prioritisation weighs risk reduction against effort. Projects 1 and 3 each deliver high risk reduction for medium effort — the best ratio available — and both address live compliance exposure (statutory reporting; over-retention of personal data, which is itself a UK GDPR storage-limitation issue with recent near-misses signalling elevated likelihood). Project 2 is cheap but reduces essentially no risk: low cost is not a reason to spend capacity. Project 4 has genuine innovation value — and your **Data innovation** skill asks you to understand emerging tools — but "high effort, unproven, low-moderate risk reduction" cannot displace two high-reduction projects when capacity is the constraint; the right move is to keep it on the roadmap, perhaps as a smaller discovery. Note the classic distractor structure: one option pairs a strong project with a weak one (A), tempting you to accept a good-plus-bad bundle instead of comparing all pairings.

### Preparation tips

- **Practise with your own artefacts.** Spend ten minutes reviewing a real data catalogue entry, RACI matrix, or workflow diagram and ask yourself: what rule governs this, and does it comply? That habit is precisely what the test measures.
- **Anchor on thresholds.** Many error-checking questions hinge on exact cut-offs (dates, counts, formats). Compute the threshold once, write it down if you can, and compare every item to it.
- **Read the rule as written.** When a question quotes a policy or model, the answer follows the quoted rule — even when your professional instinct says the rule is imperfect. Assessments reward literal, consistent application.
- **Manage the clock.** With 15–30 minutes for the whole test, no single question deserves more than about two minutes. Flag and move on; accuracy on ten questions beats perfection on four.
- **Use the practice questions provided.** Untimed practice items before the real test exist to remove interface surprises — never skip them.
- **Rest and set-up matter.** Take the assessment somewhere quiet, on a reliable connection, with any permitted rough paper ready. Cognitive performance is measurably better when you are rested and uninterrupted.

### Common pitfalls

- **Plausibility over compliance.** Choosing the option that looks most like real life (e.g. "HMRC" as a department code) instead of the one that matches the stated rule. The rule as written always wins.
- **Missing the missing step.** When auditing a process log, checking only for wrong entries and overlooking absent mandatory ones — the hardest errors to see are the ones that are not there.
- **Estimating instead of calculating.** Eyeballing date gaps or counts under time pressure; near-miss values are placed deliberately to punish estimation.
- **Confusing "blocked" with "prohibited".** Governance rules often make actions conditional; assessments test whether you can tell a pausable block from a permanent bar.
- **Time-sink questions.** Spending five minutes on one multi-stage deduction while three easier questions go unanswered. Bank the accessible marks first.
- **Second-guessing validated questions.** These tests are strictly validated to predict job performance; arguing with the premise mid-test costs time. Answer the question that was asked.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment evaluates your ability to analyse, interpret and make sound decisions using numerical data. It deliberately mimics the data-handling demands of your actual role, focusing on practical business arithmetic — percentages, ratios, budgets, rates and trends — rather than abstract formulas or advanced mathematics. For a data governance manager, the inputs will look familiar: data quality scorecards, risk exposure tables, training uptake figures, remediation budgets, catalogue coverage statistics and maturity assessment results.

Typical format and timing: questions present a table, chart or short dataset followed by multiple-choice questions. Time limits are strict — commonly 20 to 30 minutes for 15 to 25 questions — so quick, accurate extraction of the right figures matters as much as the arithmetic itself. Most assessments allow or provide an onscreen calculator: the test prioritises interpretation over mental arithmetic, so the skill being measured is choosing the right calculation, not doing long division in your head. Results are compared against a norm group, and employers often see accuracy and speed separately.

Why does this matter for your role? Data governance is increasingly a numbers-driven discipline. When you identify opportunities to improve the quality and trustworthiness of data, you evidence them with completeness, accuracy and timeliness percentages. When you advise risk owners on whether an exposure is within risk tolerance, you work with likelihood scores, impact values and expected-loss arithmetic. When you advocate for better data management, your business cases stand on cost-benefit figures. When you measure data maturity or monitor compliance, you aggregate scores and track trends. An employer testing your numeric reasoning is testing whether the numbers in your recommendations can be trusted.

### What it measures for your role

- **Interpreting data quality metrics** (completeness, accuracy, duplication rates) maps to your **Data governance** and **Data management** skills — recommending improvements to the quality and trustworthiness of data requires fluency with the percentages that describe it.
- **Risk arithmetic** (likelihood × impact, expected loss, risk tolerance thresholds) maps to **Enabling and informing risk-based decisions** — "advise on risk impact and whether it's within risk tolerance" is a quantitative judgement.
- **Budget and cost-benefit calculations** map to your duty to **advocate for better use and management of data** — tactical recommendations, as your **Communicating analysis and insight** skill describes, must be backed by defensible figures.
- **Training and adoption statistics** map to **Data literacy improvement** — measuring uptake, completion rates and awareness scores is how you evidence that literacy is improving.
- **Maturity scoring and weighted averages** map to **Data maturity** — maturity models produce dimensional scores you must aggregate, compare and track over time.
- **Compliance rates and trend analysis** map to **Data standards** — monitoring compliance in a team means reading rates, spotting changes and quantifying breach impact.

### Practice questions

An onscreen calculator would normally be available; feel free to use one. Aim for about 90 seconds per question once you are practising under timed conditions. The arithmetic is shown in full in each explanation.

**Question 1 (easy) — Completeness percentage**

Your data catalogue lists 480 data assets. Of these, 384 have a named data owner. What percentage of assets currently lacks a named owner?

A) 15%
B) 20%
C) 25%
D) 80%

**Correct answer: B**

**Explanation:** Assets without an owner = 480 − 384 = 96. As a percentage: 96 ÷ 480 = 0.20 = 20%. A common slip is answering 80% — that is the percentage *with* an owner, and option D is there to catch anyone who computes 384 ÷ 480 and forgets what the question asked. Always re-read the final clause of the question ("lacks a named owner") before selecting.

**Question 2 (easy) — Percentage change in duplicates**

A deduplication initiative reduced duplicate citizen records from 12,500 to 9,875. What was the percentage reduction?

A) 18%
B) 21%
C) 26.25%
D) 2.1%

**Correct answer: B**

**Explanation:** Reduction = 12,500 − 9,875 = 2,625 records. Percentage reduction = 2,625 ÷ 12,500 = 0.21 = 21%. Note that the denominator is the *original* value (12,500), because percentage change is always measured against the starting point. Option C (26.25%) is what you get if you wrongly divide by the new value: 2,625 ÷ 9,875 ≈ 0.2658 — a classic denominator error. When you report quality improvements to stakeholders, this distinction changes the story you tell, so it is worth making the habit automatic.

**Question 3 (easy) — Training uptake**

You are supporting data literacy training. Of 640 eligible staff, 416 have completed the foundation module. Your target for the quarter is 75% completion. How many more staff must complete the module to hit the target?

A) 48
B) 64
C) 80
D) 224

**Correct answer: B**

**Explanation:** Target completions = 75% of 640 = 0.75 × 640 = 480 staff. Completed so far = 416. Shortfall = 480 − 416 = 64 staff. Option D (224) is the total not yet trained (640 − 416), which answers a different question; option A and C are near-misses for anyone who mis-multiplies. Two-step questions like this — compute the target, then the gap — are the most common structure in numeric tests, and in your real reporting on literacy programmes.

**Question 4 (moderate) — Data quality scorecard**

Your monthly quality scorecard for the Grants dataset shows four dimensions, each scored out of 100, with agreed weights:

| Dimension | Score | Weight |
|---|---|---|
| Completeness | 92 | 40% |
| Accuracy | 85 | 30% |
| Timeliness | 70 | 20% |
| Consistency | 60 | 10% |

What is the weighted overall quality score?

A) 76.75
B) 81.3
C) 82.3
D) 84.1

**Correct answer: C**

**Explanation:** Multiply each score by its weight and sum: Completeness 92 × 0.40 = 36.8; Accuracy 85 × 0.30 = 25.5; Timeliness 70 × 0.20 = 14.0; Consistency 60 × 0.10 = 6.0. Total = 36.8 + 25.5 + 14.0 + 6.0 = 82.3. Check the addition in stages: 36.8 + 25.5 = 62.3; 62.3 + 14.0 = 76.3; 76.3 + 6.0 = 82.3. Option A (76.75) is the simple unweighted average of the four scores ((92 + 85 + 70 + 60) ÷ 4 = 307 ÷ 4 = 76.75) — the classic error of ignoring weights. Options B and D are near-misses built from single mis-multiplications. Weighted scoring is exactly how composite quality and maturity indices are built, so practise until the "multiply-then-sum" pattern is second nature.

**Question 5 (moderate) — Risk exposure**

Your data risk register scores risks as expected annual loss = likelihood (probability) × impact (£). Three data risks are open:

| Risk | Likelihood | Impact if it occurs |
|---|---|---|
| R1: Over-retention of personal data leading to regulatory penalty | 10% | £180,000 |
| R2: Critical dataset unavailable during service outage | 25% | £60,000 |
| R3: Poor address quality causing failed citizen communications | 60% | £40,000 |

Which risk has the highest expected annual loss, and what is that figure?

A) R1, £18,000
B) R2, £15,000
C) R3, £24,000
D) R1, £180,000

**Correct answer: C**

**Explanation:** Compute each expected loss. R1: 0.10 × £180,000 = £18,000. R2: 0.25 × £60,000 = £15,000. R3: 0.60 × £40,000 = £24,000. The highest is R3 at £24,000. This question rewards the counter-intuitive insight at the heart of risk-based decision-making: the scariest headline impact (R1's £180,000) is not automatically the biggest expected exposure once likelihood is factored in. Option D quotes raw impact rather than expected loss. When you advise risk owners "on risk impact and whether it's within risk tolerance", showing both the raw impact and the expected value — and explaining the difference — is what makes your advice proportionate.

**Question 6 (moderate) — Risk tolerance threshold**

Continuing from Question 5: your organisation's stated risk tolerance for any single data risk is an expected annual loss of £20,000. A proposed control for R3 costs £7,500 per year and would reduce R3's likelihood from 60% to 25% (impact unchanged at £40,000). If implemented, would R3 fall within tolerance, and what would be the net annual benefit of the control?

A) Within tolerance; net benefit £6,500
B) Within tolerance; net benefit £14,000
C) Not within tolerance; net cost £7,500
D) Within tolerance; net benefit £10,000

**Correct answer: A**

**Explanation:** New expected loss for R3 = 0.25 × £40,000 = £10,000, which is below the £20,000 tolerance — so yes, within tolerance. Risk reduction achieved = £24,000 − £10,000 = £14,000 per year. Net benefit = reduction minus control cost = £14,000 − £7,500 = £6,500 per year. Option B forgets to subtract the control's cost; option D subtracts the wrong way (£24,000 − £14,000 = £10,000 confuses the reduction with the residual). Three-step chains like this — recompute, compare to threshold, net off the cost — mirror precisely how you would justify a control investment to a risk owner.

**Question 7 (moderate) — Compliance rate trend**

Quarterly spot-checks measure team compliance with your data handling standard:

| Quarter | Records checked | Compliant records |
|---|---|---|
| Q1 | 250 | 205 |
| Q2 | 300 | 252 |
| Q3 | 320 | 280 |

By how many percentage points did the compliance rate improve from Q1 to Q3?

A) 5.5 percentage points
B) 7.5 percentage points
C) 6.0 percentage points
D) 75 percentage points

**Correct answer: A**

**Explanation:** Q1 rate = 205 ÷ 250 = 0.82 = 82%. Q3 rate = 280 ÷ 320 = 0.875 = 87.5%. Improvement = 87.5 − 82 = 5.5 percentage points. Two things matter here. First, you cannot compare raw counts (205 vs 280) because the sample sizes differ — rates are the honest comparison, which is why monitoring compliance requires this calculation. Second, note the phrase "percentage points": the difference between two percentages is measured in points, not in per cent. (The *relative* increase would be 5.5 ÷ 82 ≈ 6.7%.) Assessments and audit reports both punish sloppy language on this distinction.

**Question 8 (moderate) — Budget allocation**

Your data governance programme has an annual budget of £240,000, allocated: 45% staff, 25% tooling, 20% training, 10% contingency. Mid-year, the tooling line is overspent by £12,000, to be covered entirely from contingency. How much contingency remains for the rest of the year?

A) £24,000
B) £12,000
C) £36,000
D) £10,800

**Correct answer: B**

**Explanation:** Contingency allocation = 10% of £240,000 = £24,000. Covering the tooling overspend consumes £12,000, leaving £24,000 − £12,000 = £12,000. Option A is the original contingency (ignoring the overspend); option C is what you get if you wrongly add instead of subtracting; option D (£10,800) comes from misapplying a percentage to the wrong base. Straightforward, but under time pressure the discipline is the same as in your budget reviews: establish the base figure first (£24,000), then apply the movement.

**Question 9 (challenging) — Cost-benefit of a data quality initiative**

Poor address data currently causes 4,200 failed postal communications per year, each costing £6.50 to reissue. A proposed address-validation service costs £15,000 per year and is expected to prevent 80% of the failures. What is the expected net annual saving?

A) £27,300
B) £6,840
C) £21,840
D) £12,300

**Correct answer: B**

**Explanation:** Current annual failure cost = 4,200 × £6.50 = £27,300. Failures prevented = 80% of 4,200 = 3,360, saving 3,360 × £6.50 = £21,840 per year. Net saving = £21,840 − £15,000 = £6,840. Option A is the gross current cost (no control applied); option C is the gross saving (forgetting the service's own cost); option D (£27,300 − £15,000) wrongly assumes the service prevents 100% of failures. The four options correspond to four distinct reasoning errors, which is typical of well-built numeric items. This is also the skeleton of every data quality business case you will write: baseline cost, effectiveness rate, gross benefit, minus intervention cost.

**Question 10 (challenging) — Catalogue coverage projection**

Your catalogue currently documents 480 of an estimated 800 data assets (60% coverage). Your team documents new entries at a steady 30 assets per month, but discovery work also adds an estimated 10 previously unknown assets to the total each month. What will coverage be, to the nearest whole percentage, after 4 months?

A) 75%
B) 71%
C) 68%
D) 80%

**Correct answer: B**

**Explanation:** After 4 months, documented assets = 480 + (30 × 4) = 480 + 120 = 600. Total estimated assets = 800 + (10 × 4) = 800 + 40 = 840. Coverage = 600 ÷ 840 = 0.7142... ≈ 71%. Option A (75%) is 600 ÷ 800 — forgetting that the denominator grows as discovery finds new assets. This "moving denominator" pattern appears constantly in governance metrics: catalogue coverage, DPIA coverage, ownership coverage. When both the numerator and denominator change, recompute both before dividing; progress can look faster than it really is if the estate keeps growing beneath you.

**Question 11 (challenging) — Ratio reasoning on stewardship workload**

Best practice guidance you have adopted recommends no more than 25 data assets per data steward. You have 6 stewards and 480 catalogued assets, and expect the catalogue to reach 600 assets within a year. How many additional stewards must you recruit to comply with the guidance at 600 assets?

A) 6
B) 18
C) 24
D) 12

**Correct answer: B**

**Explanation:** Stewards needed at 600 assets = 600 ÷ 25 = 24 stewards. You have 6, so additional stewards required = 24 − 6 = 18. Option C (24) is the total needed, not the *additional* number — re-read the question's final clause. Option A (6) might tempt anyone who divides the 120 new assets by 25 and rounds oddly, or who anchors on the current steward count; the current 480 assets already exceed capacity (480 ÷ 25 = 19.2 stewards needed now), which is itself a finding you would flag. Ratio-to-headcount conversions like this are the arithmetic behind resourcing recommendations in your governance framework.

**Question 12 (challenging) — Maturity score movement**

Your organisation's data maturity is assessed across five dimensions, scored 1–5. Last year and this year:

| Dimension | Last year | This year |
|---|---|---|
| Governance & ownership | 2 | 3 |
| Data quality | 2 | 3 |
| Metadata management | 1 | 2 |
| Data literacy | 2 | 2 |
| Risk & compliance | 3 | 4 |

Your improvement plan targeted a mean score of 3.0 this year. By how much did the actual mean fall short of the target, and which single dimension, if raised by one level, would have exactly achieved the target mean?

A) Shortfall 0.2; raising any one dimension by one level would achieve it
B) Shortfall 0.4; no single dimension could achieve it
C) Shortfall 0.2; only Data literacy would achieve it
D) Shortfall 0.6; raising Metadata management by two levels would be needed

**Correct answer: A**

**Explanation:** This year's mean = (3 + 3 + 2 + 2 + 4) ÷ 5 = 14 ÷ 5 = 2.8. Shortfall = 3.0 − 2.8 = 0.2. Raising *any* single dimension by one level adds 1 to the total: 15 ÷ 5 = 3.0 exactly — so any one-level improvement on any dimension would have achieved the mean target. Option C is the trap: it feels intuitively right that only the laggard dimension "counts", but arithmetic on a mean is indifferent to *which* dimension contributes the extra point. (Strategically, of course, you might still prioritise Metadata management at level 2, or Data literacy which stagnated — the numbers tell you what achieves the target; your judgement decides what is most valuable. Noticing that distinction is what your **Communicating analysis and insight** skill calls giving "tactical recommendations based on your analysis".)

**Question 13 (challenging) — Interpreting a breach impact table**

A standard was breached when an extract was shared without the agreed field-level redactions. Remediation actions and costs:

| Action | Unit cost | Units |
|---|---|---|
| Recall and secure deletion confirmations | £45 per recipient | 38 recipients |
| Re-issue of corrected extract | £120 flat | 1 |
| Additional monitoring of affected records | £0.85 per record per month | 5,200 records for 3 months |

What is the total remediation cost?

A) £15,090
B) £6,090
C) £17,490
D) £14,970

**Correct answer: A**

**Explanation:** Take each line in turn. Recall costs = £45 × 38 = £1,710. Re-issue = £120. Monitoring = 5,200 records × 3 months = 15,600 record-months; 15,600 × £0.85 = £13,260. Total = £1,710 + £120 + £13,260 = £15,090; verify in stages: 1,710 + 120 = 1,830; 1,830 + 13,260 = 15,090. Option B is roughly what you get if you omit the three-month multiplier on monitoring; option C adds a spurious extra month of monitoring; option D drops the £120 re-issue. Multi-line cost totals reward a simple habit: write each line's subtotal, then sum once — exactly how you would "analyse the impact if a standard is breached" for a governance board.

**Question 14 (moderate) — Percentage of a percentage**

A survey finds 60% of staff have completed data literacy training. Of those trained, 85% pass a follow-up knowledge check. What percentage of all staff are both trained and passed?

A) 45%
B) 51%
C) 85%
D) 25%

**Correct answer: B**

**Explanation:** Multiply the two proportions: 0.60 × 0.85 = 0.51 = 51% of all staff. Option C confuses the pass rate among the trained with the rate among everyone. Chained percentages appear whenever a funnel is involved — trained → assessed → passed, or catalogued → owned → reviewed — and the rule is always multiply the stage rates. When you report literacy outcomes "to enable data consumers to understand what they can and cannot do with data", presenting both figures (85% of trained; 51% of all staff) is clearer and more honest than either alone.

**Question 15 (challenging) — Comparing improvement options per pound**

You must recommend one of two data quality interventions to the governance board. Both address the same failing dataset, which currently causes an estimated £48,000 of annual rework:

- Option 1: Automated validation at the point of entry. Annual cost £18,000; expected to eliminate 70% of the rework.
- Option 2: Quarterly manual cleansing sprints. Annual cost £9,000; expected to eliminate 40% of the rework.

Which option delivers the greater net annual benefit, and which delivers the greater benefit per pound spent?

A) Option 1 on both measures
B) Option 2 on both measures
C) Option 1 on net benefit; Option 2 on benefit per pound
D) Option 2 on net benefit; Option 1 on benefit per pound

**Correct answer: C**

**Explanation:** Option 1 gross benefit = 0.70 × £48,000 = £33,600; net = £33,600 − £18,000 = £15,600; benefit per pound = £33,600 ÷ £18,000 = £1.87. Option 2 gross benefit = 0.40 × £48,000 = £19,200; net = £19,200 − £9,000 = £10,200; benefit per pound = £19,200 ÷ £9,000 = £2.13. Option 1 wins on absolute net benefit (£15,600 vs £10,200); Option 2 wins on return per pound (£2.13 vs £1.87). Both statements are true simultaneously, which is why the correct answer is C — and why real recommendations must state *which* criterion the organisation cares about. If budget is unconstrained, maximise net benefit; if funds are scarce and could be spent elsewhere, efficiency per pound matters more. Presenting both figures, and saying which you recommend and why, is precisely the "tactical recommendations based on your analysis and insight" your role profile expects.

**Question 16 (moderate) — Reading a stacked figure correctly**

A report states: "Of the 1,200 data-related incidents logged this year, 55% were classified as data quality issues, 30% as access control issues, and the remainder as 'other'. Of the access control issues, one third involved personal data." How many access control incidents involved personal data?

A) 360
B) 120
C) 180
D) 132

**Correct answer: B**

**Explanation:** Access control incidents = 30% of 1,200 = 0.30 × 1,200 = 360. One third of those involved personal data: 360 ÷ 3 = 120. Option A stops one step early (all access control incidents); option C comes from taking 15% of 1,200 — muddling "one third of 30%" into "half of 30%"; option D takes 11% of 1,200, a keying slip. The question is easy arithmetic wrapped in prose — the skill is translating stacked percentage language ("of the..., one third...") into an ordered calculation. Incident summaries, DPIA registers and audit reports all describe subsets of subsets in exactly this style.

### Preparation tips

- **Rebuild the metrics you already use.** Take one real artefact from your work — a quality scorecard, the risk register, a training report — and recompute its headline figures by hand. Familiarity with your own numbers is the best rehearsal.
- **Master the five recurring patterns.** Percentage change (against the *original* value), weighted averages (multiply-then-sum), expected loss (likelihood × impact), net benefit (gross saving minus cost), and moving denominators (recompute both parts). Nearly every question above is one of these; so is nearly every real assessment item.
- **Read the final clause twice.** "How many *more*", "what percentage *lacks*", "*additional* stewards" — the arithmetic is often easy and the wording is where marks are lost.
- **Use the calculator, but write subtotals.** For multi-line totals, jot each line's result before summing. Keying one long chain into a calculator is where transposition errors breed.
- **Estimate to sanity-check, not to answer.** A quick rounding check (is 600 ÷ 840 roughly 70%?) catches gross errors, but select your answer from the exact calculation.
- **Practise light time pressure early.** Do a few questions at 90 seconds each so the pace feels normal before the real thing. Calm familiarity beats last-minute cramming.

### Common pitfalls

- **Misreading table labels and units.** Confusing quarterly with monthly figures, records with record-months, or ignoring qualifiers like "per recipient" or "in thousands". Read headers and units before touching the numbers.
- **The wrong denominator.** Percentage change divided by the new value instead of the original; coverage computed against last month's asset total. The denominator is the most commonly fumbled part of any percentage.
- **Answering the neighbouring question.** Reporting the total needed when asked for the additional amount; the share with owners when asked for the share without. The distractor options are built from exactly these slips.
- **Over-calculating.** Performing an elaborate multi-stage computation when a simple estimation would eliminate three options; conversely, trusting an estimate when options are close together. Match precision to the gap between options.
- **Time-sink questions.** One dense multi-step item can consume five questions' worth of time. Flag it, move on, return if time allows — the scoring rewards total correct answers, not heroics on hard ones.
- **Percentage points versus per cent.** A rise from 82% to 87.5% is 5.5 points but a 6.7% relative increase. Governance reporting — and test writers — care about the difference.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment evaluates how well you understand, analyse and draw correct conclusions from written material of the kind your role deals with every day. It mirrors the exact reading demands of data governance work: dense policy documents, data standards, sharing agreements, audit findings, stakeholder emails and strategy papers. The defining discipline of the format is *fact-based logic*: you must answer strictly from the text provided, setting aside everything you know professionally — even where your expert knowledge tells you what the policy "probably" means or "should" say.

Typical format and timing: you are shown a passage, then asked a series of statements to judge as **True** (the passage logically supports the statement), **False** (the passage logically contradicts it), or **Cannot Say** (the passage provides insufficient information either way). Some questions are multiple-choice comprehension instead — identifying the best summary, the correct application of a rule, or the author's position. Timing is tight: typically less than a minute per question, simulating the pace at which you skim-then-verify documents against a deadline.

Why does this matter for your role? Almost every artefact you produce or enforce is text. You develop "the processes, operational policies and standards needed to support data management" — and a policy that says something subtly different from what its author intended becomes a compliance problem you will have to untangle. You monitor compliance, which means reading what a team *actually did* against what the standard *actually says*. You manage differing stakeholder perspectives, which means extracting exactly what an email commits to, requests or concedes — no more, no less. And you communicate between the technical and the non-technical, which begins with reading both kinds of material precisely. Verbal reasoning is arguably the single most job-relevant assessment for a governance role, because governance *is* the disciplined reading and writing of rules.

### What it measures for your role

- **Precise rule extraction** maps to **Data standards** ("use data policies, processes and standards effectively") and **Data governance** — determining exactly what a policy requires, permits and prohibits.
- **Distinguishing stated fact from inference** maps to **Enabling and informing risk-based decisions** — advice to risk owners must separate what the evidence says from what you suspect.
- **Reading stakeholder correspondence accurately** maps to **Stakeholder relationship management** and **Communicating between the technical and non-technical** — consensus building starts from a correct understanding of each party's stated position.
- **Comprehending compliance and audit text** maps to **Data management** ("follow organisational data governance, including policies on data access, sharing, dissemination and protection") and to your duty to analyse the impact if a standard is breached.
- **Judging tone and emphasis in strategy documents** maps to **Strategic thinking** — communicating how activities meet strategic goals requires grasping what a strategy actually prioritises.
- **Ethics and privacy language** maps to **Data ethics and privacy** — recognising when a text does, or does not, establish a lawful basis, a consent condition or an ethical safeguard.

### Practice questions

For each True/False/Cannot Say item, use only the passage. "Cannot Say" is the correct answer whenever the passage neither supports nor contradicts the statement — however plausible the statement may seem.

**Passage 1 — Data retention policy extract**

*"All records containing personal data must be assigned a retention period from the corporate retention schedule at the point of creation. Records whose retention period has expired must be reviewed by the information asset owner before disposal; disposal without such review is permitted only where the record belongs to a category the schedule marks as 'routine', in which case automated deletion may proceed. Retention periods may be extended beyond the schedule only where a litigation hold or a public inquiry notice applies. Nothing in this policy overrides the statutory rights of data subjects, including the right to erasure where it applies."*

**Question 1 (easy) — True / False / Cannot Say**

Statement: "Under the policy, some records may be deleted automatically without review by the information asset owner."

A) True
B) False
C) Cannot Say

**Correct answer: A (True)**

**Explanation:** The passage states that disposal without owner review "is permitted only where the record belongs to a category the schedule marks as 'routine', in which case automated deletion may proceed." That sentence explicitly creates a class of records (routine ones) that may be automatically deleted without review. The statement is therefore directly supported by the text. Notice the reasoning style: point to the exact clause that supports the answer. In a real assessment — and a real compliance dispute — the winning move is always citation of specific wording.

**Question 2 (moderate) — True / False / Cannot Say**

Statement: "A team may extend a record's retention period beyond the schedule if a senior manager approves the extension."

A) True
B) False
C) Cannot Say

**Correct answer: B (False)**

**Explanation:** The passage says retention periods "may be extended beyond the schedule *only* where a litigation hold or a public inquiry notice applies." The word "only" makes the two listed grounds exhaustive: senior manager approval is not one of them, so an extension on that basis would contradict the policy. This is False rather than Cannot Say because the passage does not merely omit senior-manager approval — its "only" clause positively excludes every unlisted ground. Watch for restrictive words ("only", "must", "solely", "in all cases"): they convert silence about alternatives into prohibition of alternatives.

**Question 3 (moderate) — True / False / Cannot Say**

Statement: "The corporate retention schedule sets a seven-year retention period for financial records."

A) True
B) False
C) Cannot Say

**Correct answer: C (Cannot Say)**

**Explanation:** The passage tells us a corporate retention schedule exists and governs retention periods, but it says nothing about the specific periods it contains, for financial records or anything else. Your professional experience may make seven years feel very likely — many financial retention rules do run to six or seven years — but the passage neither supports nor contradicts the figure. This is the pitfall the format is built around: importing outside knowledge. If the words are not there, the answer is Cannot Say.

**Question 4 (challenging) — Multiple choice application**

A record containing personal data has passed its scheduled retention period. It is in a category the schedule marks as "routine". A public inquiry notice applies to the programme it belongs to. According to the passage, what should happen?

A) Automated deletion may proceed, because the record is routine
B) The record's retention is extended; it must not be disposed of while the inquiry notice applies
C) The information asset owner must review it, then dispose of it
D) The data subject's right to erasure requires immediate deletion

**Correct answer: B**

**Explanation:** Two clauses compete here, and the assessment is testing whether you can rank them. The "routine" clause would normally allow automated deletion — but the extension clause states that retention "may be extended beyond the schedule... where a litigation hold or a public inquiry notice applies", and an inquiry notice is in force. An active inquiry notice is precisely the circumstance in which disposal must not proceed; deleting evidence subject to an inquiry would defeat the clause's purpose. Option C applies the review route that the routine marking makes unnecessary, and ignores the inquiry. Option D misuses the final sentence: the passage preserves erasure rights "where it applies", but nothing in the scenario says a data subject has exercised that right. Layered rules with exceptions-to-exceptions are the daily texture of governance documents; practise reading them as: general rule → carve-out → override.

**Passage 2 — Email from a service manager**

*"Hi — following up on our conversation at the data owners' forum. My team is under real pressure to launch the new grants portal by the end of September. We've been told we can't go live until the data sharing agreement with the payments provider is signed off, and that sign-off is apparently waiting on your team's review of the data flows. I want to be clear that we value the governance process, and the last thing I want is another incident like March. But if the review can't be completed within two weeks, I'll have to escalate to the programme board, because the launch date is a ministerial commitment. Can we meet this week to agree a way forward?"*

**Question 5 (easy) — True / False / Cannot Say**

Statement: "The service manager states that the portal launch date is a ministerial commitment."

A) True
B) False
C) Cannot Say

**Correct answer: A (True)**

**Explanation:** The email says directly: "the launch date is a ministerial commitment." The statement simply reports what the author states, which is all True requires. Note the careful framing of the statement — "the service manager *states* that" — you are confirming the claim was made, not that it is accurate. Assessments (and careful stakeholder management) both distinguish between what someone says and what is independently true.

**Question 6 (moderate) — True / False / Cannot Say**

Statement: "The data governance team's review of the data flows is behind schedule."

A) True
B) False
C) Cannot Say

**Correct answer: C (Cannot Say)**

**Explanation:** The email says sign-off "is apparently waiting on your team's review" — a report, hedged with "apparently", that the review has not yet concluded. But nothing in the text establishes what the review's schedule was, or that any agreed date has been missed. "Not yet finished" is not the same as "behind schedule"; the review may be exactly on its planned timeline. The pressure in the email invites you to concede fault that the text never establishes. In both assessments and stakeholder negotiations, keep the distinction between "outstanding" and "late" firmly in view.

**Question 7 (moderate) — True / False / Cannot Say**

Statement: "There was a data-related incident in March."

A) True
B) False
C) Cannot Say

**Correct answer: A (True)**

**Explanation:** The author writes "the last thing I want is another incident like March." The word "another" presupposes that an incident occurred in March — the sentence makes no sense otherwise, and the passage offers this as shared background between writer and reader. This is a legitimate *textual* inference (from presupposition), not outside knowledge: the support is in the words themselves. Contrast this with Question 3, where the statement added a fact the text nowhere implied. The line to hold: inferences licensed by the wording are fair; facts imported from beyond the text are not. (Strictly, the text does not label the March incident "data-related" — but an incident invoked in a message about data governance sign-off, cited as a reason to value the governance process, is textually presented as a data incident. If you hesitated between A and C here, you are reading carefully; most published tests would accept the presupposition as textual support.)

**Question 8 (challenging) — Multiple choice comprehension**

Which of the following best characterises the service manager's position?

A) They reject the need for governance review and demand immediate sign-off
B) They accept the governance process but signal escalation if the review exceeds two weeks, and propose a meeting
C) They ask the governance team to accept accountability for the March incident
D) They request that the ministerial commitment be renegotiated

**Correct answer: B**

**Explanation:** The email explicitly affirms the process ("we value the governance process"), sets a conditional escalation ("if the review can't be completed within two weeks, I'll have to escalate"), and closes with a proposal to meet. Option B captures all three elements. Option A overstates: valuing the process and requesting pace is not rejecting review. Option C misreads the March reference, which is offered as shared motivation for good governance, not an accusation. Option D inverts the email's logic — the commitment is presented as fixed, which is *why* escalation is threatened. Summarising a stakeholder's position accurately — pressure, concession and proposal all together — is the reading skill beneath "manage differing stakeholder perspectives" and "build and reach consensus with stakeholders".

**Passage 3 — Internal audit finding**

*"The audit examined 60 data sharing arrangements active during the financial year. Of these, 14 lacked a documented lawful basis at the time of inspection, although in 9 of the 14 cases a lawful basis was documented retrospectively before the audit concluded. The audit found no evidence that data was shared unlawfully; however, the absence of contemporaneous documentation prevents the organisation from demonstrating compliance, contrary to the accountability principle. We rate this finding as 'moderate' and recommend that the data governance team introduce a pre-sharing checklist, with completion monitored quarterly and reported to the Information Governance Board."*

**Question 9 (easy) — True / False / Cannot Say**

Statement: "At the time of inspection, fewer than a quarter of the examined arrangements lacked a documented lawful basis."

A) True
B) False
C) Cannot Say

**Correct answer: A (True)**

**Explanation:** 14 of 60 arrangements lacked documentation at inspection. A quarter of 60 is 15; since 14 < 15, "fewer than a quarter" is correct. The verbal test occasionally smuggles in light arithmetic like this — read the numbers as carefully as the words. Had the statement said "fewer than a fifth", the answer would be False (a fifth of 60 is 12, and 14 > 12): the cut-off is doing all the work, exactly as in the cognitive section's threshold questions.

**Question 10 (moderate) — True / False / Cannot Say**

Statement: "The audit found that data was shared unlawfully in five cases."

A) True
B) False
C) Cannot Say

**Correct answer: B (False)**

**Explanation:** The passage states: "The audit found no evidence that data was shared unlawfully." The statement attributes to the audit a finding of unlawful sharing in five cases (presumably tempting because 14 − 9 = 5 cases were never retrospectively documented). But lacking documentation is not the same as sharing unlawfully, and the audit's explicit "no evidence" statement contradicts the claim. This distinction — between a *demonstrability* failure (accountability) and a *substantive* failure (unlawful processing) — is one your role trades on constantly: the audit's point is precisely that the organisation could not *show* compliance, which is itself the breach of the accountability principle.

**Question 11 (challenging) — True / False / Cannot Say**

Statement: "The audit recommends that the data governance team report quarterly to the Information Governance Board on completion of a pre-sharing checklist."

A) True
B) False
C) Cannot Say

**Correct answer: A (True)**

**Explanation:** Unpack the recommendation clause: "introduce a pre-sharing checklist, with completion monitored quarterly and reported to the Information Governance Board." The recommendation is addressed to the data governance team; the checklist's completion is to be monitored quarterly and reported to the Board. The statement is a fair paraphrase. If you answered Cannot Say, you may have worried that the passage does not say the *reporting* is quarterly — only the monitoring. Read again: "monitored quarterly and reported" most naturally attaches the quarterly cadence to the monitoring-and-reporting pair describing the same cycle. Published tests avoid genuinely ambiguous attachments, but they do test whether you can track what each modifier modifies; where an attachment is truly undecidable, Cannot Say would be credited. Here the paraphrase stays within what the sentence supports.

**Question 12 (moderate) — Multiple choice comprehension**

What is the audit's central concern?

A) Data was shared with organisations that had no right to receive it
B) The organisation cannot demonstrate compliance because documentation was not created at the time of sharing
C) The Information Governance Board failed to monitor data sharing
D) Retrospective documentation is prohibited and the nine late cases must be reversed

**Correct answer: B**

**Explanation:** The pivot sentence is: "the absence of contemporaneous documentation prevents the organisation from demonstrating compliance, contrary to the accountability principle." That is option B almost verbatim. Option A contradicts the "no evidence" finding. Option C blames a body the passage merely names as the future recipient of reports. Option D invents a prohibition — the passage reports retrospective documentation neutrally, even mitigatingly ("in 9 of the 14 cases... before the audit concluded"). Identifying the load-bearing sentence in a finding is how you turn audit text into the right remediation — and how you brief it accurately to non-specialists, per your **Communicating analysis and insight** skill.

**Passage 4 — Data strategy extract**

*"Our data strategy rests on the principle that data is a shared organisational asset rather than the property of individual teams. Over the next three years we will prioritise improving the quality of our most critical data assets ahead of expanding our analytical tooling, on the grounds that better tools applied to unreliable data multiply cost without multiplying insight. Every directorate will nominate data stewards, and stewardship duties will be recognised in role descriptions and performance objectives. We recognise that this represents a cultural change, and that cultural change cannot be mandated by policy alone; it must be led, modelled and reinforced."*

**Question 13 (moderate) — True / False / Cannot Say**

Statement: "The strategy commits to expanding analytical tooling within three years."

A) True
B) False
C) Cannot Say

**Correct answer: C (Cannot Say)**

**Explanation:** The strategy says quality improvement will be prioritised "ahead of expanding our analytical tooling". This tells us the *relative ordering* of two priorities, not whether the second will be delivered within the three-year window — tooling expansion might follow within the period, or later, or be re-scoped. The passage neither promises nor rules out tooling expansion inside three years. Prioritisation language ("ahead of", "before", "first") is a favourite trap: it implies sequence, not commitment. Reading strategy documents at this level of precision is what lets you "communicate how activities meet strategic goals" without over-claiming on the strategy's behalf.

**Question 14 (challenging) — Multiple choice comprehension**

Which statement best captures the strategy's reasoning for sequencing quality before tooling?

A) Analytical tools are too expensive to procure in the current spending period
B) Applying better tools to unreliable data increases cost without a matching increase in insight
C) Directorates lack the data literacy to use advanced tools
D) The organisation's tooling is already best in class

**Correct answer: B**

**Explanation:** The passage gives its grounds explicitly: "better tools applied to unreliable data multiply cost without multiplying insight" — option B restates this. Options A, C and D each supply a plausible real-world rationale that the text never gives. This is the multiple-choice analogue of Cannot Say discipline: the right answer is the reason *the author states*, not the best reason *you* could construct. When you advocate for better use and management of data, quoting the strategy's own stated reasoning back to decision-makers is far more persuasive than substituting your own — and this question type trains exactly that habit.

**Passage 5 — Data ethics guidance extract**

*"Before any new use of existing data is approved, teams must complete an ethics screening questionnaire. Where the screening identifies a potential impact on individuals or groups, the proposal must be referred to the ethics advisory group, whose advice is not binding but must be recorded alongside the approval decision. Approvers may depart from the group's advice only with written reasons. The screening questionnaire is not required where the new use is limited to producing aggregate statistics from which no individual can be identified."*

**Question 15 (moderate) — True / False / Cannot Say**

Statement: "The ethics advisory group can veto a proposed new use of data."

A) True
B) False
C) Cannot Say

**Correct answer: B (False)**

**Explanation:** The passage states the group's "advice is not binding" — a veto is by definition binding, so the statement contradicts the text. Note what the passage *does* give the group: its advice must be recorded, and departures require written reasons. That is influence and accountability, not a veto. Candidates sometimes choose Cannot Say because "veto" is not mentioned; but "not binding" positively rules a veto out, which makes this False rather than unstated. Precision about advisory versus decision-making authority is a governance habit worth keeping sharp — it is the difference between a Consulted and an Accountable role in your own RACI matrices.

**Question 16 (moderate) — True / False / Cannot Say**

Statement: "A team producing anonymous aggregate statistics from existing data must still complete the ethics screening questionnaire."

A) True
B) False
C) Cannot Say

**Correct answer: B (False)**

**Explanation:** The final sentence creates an explicit exemption: the questionnaire "is not required where the new use is limited to producing aggregate statistics from which no individual can be identified." The statement asserts the opposite of that exemption for exactly the exempted case, so it is False. Read the exemption's conditions carefully, though — it applies only where the use is *limited to* such statistics and *no individual can be identified*. A statement about aggregate outputs from which individuals *could* be re-identified would fall outside the exemption. Exemption clauses reward the slowest, most literal reading you can afford — in tests and in the ethics screening processes you will design.

### Preparation tips

- **Practise the three-way discipline daily.** Take any policy paragraph you encounter this week and write one statement that is True, one that is False, and one that is Cannot Say against it. Five minutes of this is worth an hour of passive reading.
- **Hunt the operative words.** "Only", "must", "may", "unless", "all", "some", "apparently" — underline them mentally as you read. Almost every True/False/Cannot Say answer turns on one of these.
- **Suppress your expertise deliberately.** You know more about data protection than most passage writers. That knowledge is precisely what the test tempts you to import. Before answering, ask: "Which words in the passage support this?" If you cannot point to them, the answer is Cannot Say.
- **Read the statement before re-reading the passage.** Skim the passage once for structure, read the statement, then return to verify against the specific clause. Reading the whole passage exhaustively first is the classic time sink.
- **Practise on your own document types.** Retention schedules, sharing agreements, audit reports and strategy papers — the passages in your real assessment will resemble what you already read, which is an advantage most candidates do not have. Use it.
- **Keep calm about Cannot Say.** Candidates under pressure avoid it, feeling it is a "non-answer". It is a full answer — often the correct one — and selecting it confidently is a mark of disciplined reading.

### Common pitfalls

- **Making assumptions.** Bringing personal or professional knowledge into the answer instead of relying only on the provided text. For experienced practitioners this is the number-one cause of lost marks — you know too much, and the test knows it.
- **Confusing likelihood with fact.** A passage saying an outcome is "expected" or "likely" does not make a statement asserting the outcome True. Match the modality of the statement to the modality of the text.
- **Missing restrictive words.** Overlooking an "only" or "unless" converts a False into an apparent Cannot Say, or vice versa. These small words carry the legal weight — in the test and in your policies.
- **Treating silence as denial.** A passage that fails to mention senior-manager approval is not thereby saying approval is forbidden — unless a restrictive clause makes the listed grounds exhaustive. Distinguish "not stated" (Cannot Say) from "excluded" (False).
- **Poor time management.** Spending too long absorbing every passage in full before looking at the questions. Scan for structure, then verify clause by clause against each statement.
- **Answering the world instead of the text.** Especially on comprehension items: the best answer is the one the passage supports, not the one that would be wisest in reality. Save your professional judgement for the situational judgement section — it is wanted there.

## Workplace job-specific situational judgement assessment

### About this assessment

A workplace job-specific situational judgement assessment evaluates your decision-making, interpersonal skill and professional conduct by presenting realistic workplace dilemmas and asking how you would respond. Unlike the reasoning tests, there is usually no single objectively right answer computed by logic or arithmetic — several responses may seem reasonable, and the assessment measures how closely your choices align with the values and behaviours the role demands. For a data governance manager in UK government, those values are well documented: putting user needs first, transparency, collaboration across disciplines, accessibility and inclusion, proportionate risk management, and the Civil Service values of integrity, honesty, objectivity and impartiality.

Typical format and timing: each scenario describes a situation drawn from the role — a data owner resisting accountability, a delivery team wanting to bypass a review, an ethics concern in a new data use — followed by three to five possible actions. You are asked either to pick the **most effective** and **least effective** actions, or to rank or rate every option. Timing is usually generous or untimed: the test wants your natural judgement, not your speed.

Why does this matter for your role? Governance succeeds or fails on judgement calls made in the room. Your role profile is explicit that you will "work within the organisation to minimise data risks", "advocate for better use and management of data", "manage differing stakeholder perspectives" and "support and host discussions within a multidisciplinary team, with potentially difficult dynamics". None of those duties can be performed by policy documents alone — they are performed by a person choosing, under pressure, between escalating and absorbing, between blocking and enabling, between the letter of a standard and its purpose. The situational judgement test simulates precisely those choices.

### What it measures for your role

- **Balancing enablement against control** maps to **Data governance** — implementing a framework "and making recommendations to ensure compliance" while remaining a partner to delivery teams, not an obstacle.
- **Escalation judgement** maps to **Enabling and informing risk-based decisions** — knowing when a risk is within tolerance to be managed locally, and when it must go up.
- **Stakeholder handling** maps to **Stakeholder relationship management** and **Communicating between the technical and non-technical** — building consensus, managing difficult dynamics, tailoring the message to the audience.
- **Ethical reasoning** maps to **Data ethics and privacy** — recognising ethics and privacy risks and sharing them "through appropriate channels".
- **Championing literacy and culture** maps to **Data literacy improvement** and your duty to **advocate for better use and management of data** — choosing responses that build capability rather than dependency.
- **Strategic patience** maps to **Strategic thinking** — weighing the quick fix against the framework, and communicating how today's decision serves the longer goal.

### Practice questions

For each scenario, decide your answer before reading the commentary. Where the format asks for most and least effective, choose one of each.

**Question 1 (easy) — The unowned critical dataset**

While cataloguing data assets, you identify a dataset used in statutory reporting that has no assigned owner. Two directorates each insist the other should own it, and the disagreement has lasted three weeks. Choose the MOST and LEAST effective actions.

A) Assign ownership to the directorate that uses the dataset most, notify both, and record the decision in the RACI matrix as final
B) Convene a short meeting with both directorates, present the risks of continued non-ownership, propose ownership criteria (creation, primary use, ability to maintain quality), and seek agreement — escalating with a recommendation if no agreement is reached by a set date
C) Leave the dataset unowned but add it to the risk register so the exposure is at least visible
D) Take ownership of the dataset yourself within the governance team, since you understand it best

**Most effective: B. Least effective: D.**

**Explanation:** Option B does what your role profile literally asks — "assign ownership of data, ensuring there is a clear RACI matrix" — but does it *through* stakeholders rather than *to* them: criteria-based, time-boxed, with a defined escalation path. That combination of collaboration and decisiveness is the pattern strong SJT answers share. Option A is decisive but unilateral; imposed ownership without agreement tends to produce owners who ignore their duties, and it spends relationship capital you will need again. Option C converts an unresolved problem into a documented unresolved problem — visibility without action is the classic passive distractor. Option D is least effective because it structurally undermines the framework you exist to build: the governance team owning operational data confuses second-line assurance with first-line accountability, does not scale, and teaches directorates that resistance transfers work to you. In UK public sector terms, B also models transparency (documented criteria) and collaboration.

**Question 2 (easy) — The literacy request**

A service team repeatedly sends you basic questions about what their own data means. You are busy, and answering has become a significant drain. Choose the MOST and LEAST effective actions.

A) Continue answering promptly — being helpful builds goodwill for the governance programme
B) Stop responding, so the team learns to find answers themselves
C) Answer the current question, then work with the team to create a business glossary and data dictionary for their service, offering a short training session so they can self-serve in future
D) Forward the questions to the team's line manager and ask them to address the capability gap

**Most effective: C. Least effective: B.**

**Explanation:** Option C resolves the immediate need (leaving no one blocked) and then converts a recurring dependency into capability — exactly your **Data literacy improvement** skill: "support data literacy training and development by enabling data consumers to understand what they can and cannot do with data." It also creates reusable metadata assets, advancing your framework. Option A is kind but builds permanent dependency and hides the capability gap; helpfulness that prevents learning is not help. Option D is not unreasonable in a persistent case, but as a first move it escalates a solvable teaching moment into a management issue and can damage the relationship. Option B is least effective: it abandons colleagues without notice, damages trust, and the team may guess at meanings and embed data errors — the outcome your role exists to prevent. Note the SJT scoring pattern: options that *both* solve today's problem *and* prevent tomorrow's recurrence outrank options that do only one.

**Question 3 (moderate) — The two-week ultimatum**

(Recall the email from the verbal section.) A service manager needs your team's data-flow review completed within two weeks or a ministerial launch commitment is at risk; they have signalled escalation to the programme board. Your standard review takes four weeks, and your team is at capacity. Choose the MOST and LEAST effective actions.

A) Hold the four-week standard: quality reviews cannot be compressed, and the programme should have engaged earlier
B) Meet the service manager this week; triage the review to prioritise the highest-risk flows (personal data and external sharing) for completion within two weeks, with the remainder completed post-launch under documented conditions and a named owner for residual risk
C) Skip the review this once, given the ministerial commitment, and rely on the payments provider's own assurance processes
D) Ask the service manager to escalate to the programme board now, so the board can decide whether the review is needed

**Most effective: B. Least effective: C.**

**Explanation:** Option B is risk-based governance in action: it protects what matters most (personal data, external flows) inside the deadline, makes the residual risk explicit, assigns it an owner, and keeps the relationship collaborative — "work with them to build relationships while meeting user needs", as your **Stakeholder relationship management** skill puts it. It treats governance as a service to delivery, not a gate. Option A defends quality but is rigid: it invites the escalation, positions governance as a blocker, and ignores that a proportionate two-week review of the riskiest flows may address most of the exposure. Option D is the passive distractor — outsourcing your own professional judgement to a board that will only ask *you* what should be done. Option C is least effective: it abandons the control entirely at the moment of maximum risk, sets a precedent that ministerial pressure dissolves governance, and if the March incident taught the organisation anything, this is how it repeats. Proportionality is a two-way street: it means lighter-touch review under pressure, never no review.

**Question 4 (moderate) — The quiet breach**

During a routine compliance check you discover that, three weeks ago, an analyst emailed an extract containing 2,000 citizens' personal data to their own personal email account "to work on at home over the weekend". The data appears not to have gone further, and the analyst is cooperative and apologetic. Choose the MOST and LEAST effective actions.

A) Since no harm appears to have resulted, remind the analyst of the policy, note it informally, and move on
B) Report the incident through the organisation's data incident process immediately so it can be assessed against breach-notification requirements; support containment (verified deletion from the personal account); treat the analyst without blame while being clear the process must run; and examine whether a control or training gap made the workaround attractive
C) Report the analyst to their line manager and recommend disciplinary proceedings to deter others
D) Instruct the analyst to delete the email and confirm in writing that they have done so, closing the matter with an audit trail

**Most effective: B. Least effective: A.**

**Explanation:** Option B follows the incident process — which exists precisely so that individual managers do not privately adjudicate breaches. Personal data leaving organisational control *is* an incident regardless of apparent harm; assessment against the 72-hour ICO notification test is the incident process's job, not yours to pre-empt (and note the clock ran from *awareness*, which is now). B also pairs accountability with a just-culture response — cooperative staff who self-explain are an asset to incident learning, and the question "why was working from home easier via personal email?" often reveals the real control gap. Option D contains but conceals: closing the matter without reporting deprives the organisation of its legal assessment and its learning, however tidy the audit trail. Option C leaps to punishment, which teaches the workforce to hide the next incident — the opposite of the reporting culture your **Data ethics and privacy** skill ("share data ethics and privacy risks through appropriate channels") depends on. Option A is least effective because it makes you personally complicit in non-reporting: an undocumented, unassessed personal-data breach known to the governance manager is a governance failure squared.

**Question 5 (moderate) — The vanity metric**

A senior leader asks you to present the data governance programme to the executive board and suggests you "lead with the 95% catalogue completion figure — it tells a great story". You know the 95% covers only one directorate; organisation-wide completion is 61%. Choose the MOST and LEAST effective actions.

A) Present the 95% figure as suggested — the senior leader knows the audience and sponsorship matters
B) Present both figures with clear labels: the 95% as evidence the approach works in the pilot directorate, and the 61% as the honest organisation-wide baseline with a trajectory for improvement, agreeing this framing with the senior leader beforehand
C) Refuse to present rather than risk misleading the board
D) Present the 61% only, since the organisation-wide figure is the only honest number

**Most effective: B. Least effective: A.**

**Explanation:** Option B is honest *and* persuasive — the 95% is genuinely good news when labelled truthfully as pilot-scope, and pre-agreeing the framing preserves the sponsor relationship while protecting your integrity: "shape and share communications relevant to the audience" (your **Communicating analysis and insight** skill) never licenses shaping the truth. Option D is honest but tactically clumsy: discarding legitimate good news buries the evidence that investment works and blindsides your sponsor. Option C abandons the field over a solvable framing problem — passive, and it forfeits the board's attention that the programme needs. Option A is least effective: presenting a directorate figure as if it were the organisational picture misleads the accountable board, breaches the objectivity and honesty values, and when the true figure surfaces (it always does), both your credibility and the programme's are spent. Public sector transparency is not decoration here; boards govern on the numbers you give them.

**Question 6 (moderate) — The enthusiastic AI pilot**

A team excitedly tells you they have begun uploading citizen correspondence into a commercial generative AI tool to draft summaries, and invite you to see the productivity gains. No assessment of the tool has been done; the correspondence includes personal data. Choose the MOST and LEAST effective actions.

A) Ask them to pause use for citizen data immediately while you fast-track an assessment (data flows, provider terms, DPIA screening); acknowledge the genuine value they have demonstrated; and work with them to find a compliant route — an approved tool, anonymised inputs, or an internal alternative
B) Report the team for unauthorised processing and require them to certify the practice has stopped
C) Allow the pilot to continue while the assessment proceeds, since interrupting it would discourage exactly the innovation the data strategy wants
D) Advise them informally to be careful about what they upload, and revisit when the organisation publishes AI guidance

**Most effective: A. Least effective: C.**

**Explanation:** Option A pairs the necessary stop (personal data flowing to an unassessed external processor is a live, continuing exposure) with the posture your **Data innovation** skill requires — understanding "the impact on the organisation of emerging trends in data tools" means engaging with them, not banning them. The acknowledgement and the search for a compliant route determine whether this team ever comes to you early again. Option B achieves the stop at maximum relational cost and teaches the organisation to hide pilots from governance. Option D is the passive distractor: "be careful" is not a control, and waiting for guidance leaves personal data flowing in the meantime. Option C is least effective because it inverts the risk logic — the exposure is current and compounding with every upload, while the innovation value can be preserved through a short pause; permitting known unlawful-risk processing to continue in the name of innovation is the judgement failure the scenario is probing. Enable the innovation, stop the data flow: the two are separable, and separating them is the skill.

**Question 7 (challenging) — The resistant data owner**

A director formally holds the Information Asset Owner role for a critical dataset but delegates everything, skips governance boards, and has not completed owner training. Data quality issues in their asset are now affecting two other services. Your programme's credibility is publicly linked to owners performing their duties. Choose the MOST and LEAST effective actions.

A) Raise the pattern at the next governance board, naming the directorate's non-engagement in the minutes so accountability is transparent
B) Request a one-to-one with the director; bring evidence of the cross-service impact framed in terms of their objectives and risks; ask what makes the duties hard to discharge and agree a workable model (a trained deputy with real authority, tailored briefing instead of standard training); and set a review point, being candid that continued non-engagement would have to be escalated to the SIRO
C) Work around the director by dealing with their delegate for all practical purposes and quietly updating the RACI to match reality
D) Escalate directly to the SIRO now, since the director has had ample opportunity to engage

**Most effective: B. Least effective: C.**

**Explanation:** Option B is the mature stakeholder play: evidence-led ("work to improve stakeholder relationships using evidence to explain decisions"), framed in the director's interests, genuinely curious about the blockers (senior non-engagement usually has causes — time, unclear value, fear of exposure), flexible about the *how* while firm about the *what*, and honest about the escalation consequence — which makes any later escalation fair rather than ambush. Option D is premature as a first substantive move and burns the relationship a one-to-one might save; but it is defensible soon after, which is why it is not the worst. Option A performs accountability theatre — public naming before private engagement hardens resistance and makes the board a tribunal rather than a governance forum. Option C is least effective despite feeling pragmatic: it formally rewrites accountability downward to whoever is willing, exactly inverting the ownership model, and when a serious incident hits the dataset the accountability gap becomes indefensible — an unauthorised RACI "fix" is a governance manager dismantling their own framework. Difficult dynamics are named in your role profile for a reason; the test is whether you engage them or route around them.

**Question 8 (challenging) — The conflicting stakeholder demands**

Legal advises that a dataset must be minimised aggressively to reduce privacy risk. The analytics team argues the same fields are essential for a fraud-detection model with proven public value. Both cite your governance framework. They have reached deadlock, and each asks you to rule in their favour. Choose the MOST and LEAST effective actions.

A) Rule in favour of legal — privacy risk carries regulatory consequences, and fraud analytics can proceed on reduced data
B) Rule in favour of analytics — fraud detection protects public money, which is the stronger public interest
C) Convene both parties; reframe from positions to interests (what privacy risk is legal actually managing; which fields drive model performance); explore middle-ground designs — pseudonymisation, field-level retention limits, aggregation, access controls; and if genuine residual conflict remains, take a worked options paper with your recommendation to the appropriate risk owner for a documented decision
D) Ask each side to submit written positions and pass both to the SIRO to decide

**Most effective: C. Least effective: D.**

**Explanation:** Option C recognises that most minimisation-versus-utility deadlocks are false binaries: pseudonymisation, tighter access, shorter retention on sensitive fields, or aggregated features frequently satisfy the legal *interest* (reducing identifiability and exposure) while preserving the analytical *interest* (signal in the data). "Support and host discussions within a multidisciplinary team, with potentially difficult dynamics" is nearly a description of this meeting, and the endgame — a documented, risk-owned decision if conflict genuinely remains — respects that some trade-offs are properly made by risk owners, informed by you ("work with risk owners to advise and give feedback"). Options A and B each ratify one side's framing without testing it; both spend your neutrality, which is the asset that makes governance arbitration possible at all. Option D is least effective: it forwards the deadlock upward without analysis, options or recommendation — the SIRO receives a dispute instead of a decision-ready paper. Escalation is not wrong here; *unprocessed* escalation is. The governance manager's value is turning conflict into structured choice.

**Question 9 (challenging) — The maturity assessment nobody wants to hear**

Your first organisation-wide data maturity assessment scores the organisation lower than its peers, and lower than senior leadership publicly claimed last year. Your head of profession hints that the report "could be socialised more gently" — perhaps the peer comparison could be dropped. Choose the MOST and LEAST effective actions.

A) Publish the report as drafted to all staff simultaneously, so no one can accuse the programme of softening findings
B) Drop the peer comparison as hinted; the absolute scores still show the position and the improvement plan is unchanged
C) Keep the findings intact — including the comparison — but work with your head of profession on sequencing and framing: brief affected leaders before wide release, pair every low score with its improvement action and the benefits of closing the gap, and position the baseline as the foundation the strategy builds on
D) Share the report only with the leaders whose areas scored lowest, avoiding wider embarrassment

**Most effective: C. Least effective: B.**

**Explanation:** The distinction the scenario tests is between softening the *message* (legitimate communication craft) and softening the *findings* (integrity failure). Option C keeps every finding — the peer comparison is often the single most decision-forcing element for executives — while exercising real communication skill: pre-briefing prevents ambush, pairing scores with actions converts embarrassment into agency ("describe the benefits of potential improvements", as your **Data maturity** skill puts it), and framing the baseline honestly protects the credibility of every future assessment against it. Option A confuses integrity with insensitivity; unsequenced wide release maximises defensiveness and minimises the executive engagement the findings need. Option D fragments the evidence base and looks like concealment when it surfaces. Option B is least effective because it is the quiet corruption the hint invited: removing the analytically legitimate comparison *because it is uncomfortable* subordinates evidence to reputation, and once leadership learns that unwelcome analysis can be negotiated away, your measurement programme is decorative. Objectivity is a Civil Service value precisely for moments when the evidence disappoints.

**Question 10 (challenging) — The retention purge under pressure**

A cost-reduction programme demands rapid deletion of legacy data to cut storage spend, with a target date four weeks away. Reviewing the plan, you find the deletion list includes datasets with unexpired statutory retention periods, and one dataset subject to an active subject access request. The programme director says the target "has already been announced". Choose the MOST and LEAST effective actions.

A) Support the programme's goal explicitly, then supply a corrected deletion list: proceed at pace on the (large) compliant portion, hold back the statutory-retention and SAR-affected datasets with the legal grounds documented, and give the director a defensible line for the announcement variance — offering alternatives such as cheaper archive tiers for the held-back data
B) Object to the entire programme until a full retention review of every dataset is complete
C) Allow the deletion to proceed as announced — storage costs are real, the announcement is made, and retention rules have flexibility in practice
D) Email your concerns to the programme director so they are on record, and take no further action unless asked

**Most effective: A. Least effective: C.**

**Explanation:** Option A is "apply data governance to optimise the safety and value of data throughout the data life cycle" under commercial pressure: it protects the two legally immovable categories (deleting data under an active subject access request may amount to an offence under UK data protection law, and unexpired statutory retention is not negotiable), while actively helping the programme succeed — most of the savings, on time, plus cheaper-storage alternatives for the remainder. Governance that arrives with solutions gets invited back. Option B is the over-blocking mirror image: gold-plating a proportionate check into a programme-stopping review makes governance the enemy of a legitimate objective. Option D is the covering-yourself distractor — a concerns email that changes nothing protects you and abandons the data subjects and the organisation. Option C is least effective: "retention rules have flexibility" is not a legal theory, an announcement is not a lawful basis for deletion, and destroying SAR-relevant data converts a storage project into a regulatory incident. The strongest SJT responses, here as throughout, share one shape: protect the non-negotiable, enable everything else, and document the line between them.

### Preparation tips

- **Anchor on the values, not on cleverness.** UK public sector SJTs reward user focus, transparency, collaboration, proportionality and integrity. When torn between options, ask which one a fair-minded observer would say served the public and the organisation — not which is most ingenious.
- **Look for the "both/and" option.** The most effective answer usually solves the immediate problem *and* addresses the underlying cause *and* preserves the relationship. Options that achieve only one of the three are rarely the best available.
- **Rehearse your escalation logic.** Before the test, articulate for yourself when you would escalate a data risk: continuing exposure, exceeded tolerance, failed local engagement, or a decision that properly belongs to a risk owner. Options that escalate too early (avoiding your own responsibility) or too late (sitting on a live risk) are both marked down.
- **Beware the sympathetic shortcut.** Scenarios are engineered so that helping a pressured colleague by waiving a control feels kind. Practise noticing whose interests are absent from the room — usually the data subjects' — and weight them deliberately.
- **Answer as the role, not as a hero or a bystander.** You are a manager with a framework, stakeholders and escalation routes. Options where you personally absorb others' duties, or where you merely record concerns, both misplace the role's centre of gravity.
- **Reflect on your real incidents.** Recall two or three genuine dilemmas from your own governance work and honestly appraise what worked. Self-knowledge calibrates judgement better than any bank of practice questions.

### Common pitfalls

- **Answering idealistically rather than effectively.** Choosing the option that sounds most virtuous ("refuse to present", "object until everything is reviewed") over the one that is practically effective in a real organisation. Assessors score workplace effectiveness, not moral display.
- **Selecting passive options.** Options that record, forward, monitor or await guidance while a risk continues are consistently among the lowest-scoring. Visibility is not mitigation; an email is not a control.
- **Ignoring the organisational culture and values.** UK government SJTs presume collaboration, transparency and user focus. Unilateral rulings, public naming-and-shaming and workarounds may be scored well in other cultures; not here.
- **Solving today at tomorrow's expense.** Waiving a review, absorbing a task or accepting a vanity figure relieves immediate pressure while planting the next incident. Strong answers price in the precedent being set.
- **Over-escalating and under-escalating.** Passing an unprocessed dispute upward is as weak as sitting on a breach. The role adds value by preparing decisions, not by relaying problems — and by acting immediately on the genuinely non-negotiable.
- **Forgetting the absent stakeholder.** In data dilemmas, the people the data is about are never in the meeting. Options that protect their rights and interests almost always outrank options that only balance the interests present in the room.

## Conclusion

Well done for working through this guide — it represents a substantial investment in yourself, and that investment pays off twice: once in any formal assessment you sit, and again every working day, because the abilities these four assessments measure are the abilities your role runs on.

You have practised the cognitive skills of a data governance manager: checking catalogue entries against exact thresholds, reasoning through RACI logic and layered policy rules, spotting the difference between a one-off anomaly and a systemic decline, and prioritising when a potential breach, a statutory deadline and a quality dip all land at once. You have worked the numbers that underpin credible governance advice: quality scorecards, expected-loss risk arithmetic, cost-benefit cases, coverage projections with moving denominators, and the ever-treacherous distinction between percentage points and per cent. You have exercised the disciplined reading that policies, audit findings, stakeholder emails and strategy papers demand — holding the line at "Cannot Say" when the words are not there, and catching the "only" that turns silence into prohibition. And you have rehearsed judgement in the situations that define the job: unowned datasets, two-week ultimatums, quiet breaches, vanity metrics, resistant owners and deletion programmes in a hurry.

If some questions caught you out, be encouraged rather than discouraged — every explanation you paused over is a reasoning pattern now available to you that was not there before. Consider revisiting the sections after a few weeks; spaced repetition consolidates these skills remarkably well. You might also practise generating your own questions from the documents you handle at work, which deepens the skill further and often improves the documents too.

Keep going with your professional development. Your role profile points the way: deepen your data governance and maturity expertise, stay curious about data innovation, and keep building the communication and stakeholder skills that turn frameworks into culture. Talk to your line manager about development opportunities, connect with the data community across government, and be generous in sharing what you learn — raising data literacy in others is, after all, part of your role.

You bring judgement, rigour and advocacy to how your organisation cares for its data. That work matters — to services, to colleagues, and to the citizens whose data it ultimately is. Good luck with your assessment: you are better prepared than you were when you started reading.
