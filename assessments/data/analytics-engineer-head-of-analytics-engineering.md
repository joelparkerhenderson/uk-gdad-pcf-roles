# Analytics Engineer (Head of Analytics Engineering) - Psychometric Assessment Resources

## Introduction

Welcome. This document is a practical, self-directed resource to help you prepare for psychometric assessments relevant to your role as Head of Analytics Engineering in a UK government digital and data organisation. Whether you are preparing for an internal promotion board, an external application at an equivalent or higher grade, a development centre, or simply want to sharpen the mental skills your role demands every day, this guide is designed for you.

Psychometric assessments are structured, standardised exercises that measure how you think, reason, and decide. They are widely used across the Civil Service and the wider public sector because they are objective, evidence-based, and predictive of on-the-job performance. For a senior leader such as yourself, they are rarely about raw speed with abstract puzzles. Instead, they test whether you can extract the signal from a dense stakeholder briefing, interrogate a delivery dashboard, spot the flaw in a data quality report, and choose the wisest course of action when senior stakeholders pull in different directions. In other words, they test the very capabilities your role description sets out: building relationships with senior stakeholders, aligning your analytics engineering team with strategic priorities, upholding standards for data models and documentation, advocating for the profession, and growing capability across your community.

This document is organised into four assessment sections, each mirroring a type of psychometric test you are likely to encounter:

1. **Workplace job-specific cognitive assessment** - pattern recognition, logical deduction, error checking, prioritisation, and problem solving using artefacts a head of analytics engineering genuinely handles: data models, lineage diagrams, pipeline schedules, and standards documents.
2. **Workplace job-specific numeric reasoning assessment** - interpreting tables, percentages, ratios, budgets, capacity plans, and performance metrics drawn from analytics engineering leadership.
3. **Workplace job-specific verbal reasoning assessment** - reading dense, role-relevant passages (strategies, policies, emails, audit reports) and answering strictly on the evidence of the text.
4. **Workplace job-specific situational judgement assessment** - realistic leadership dilemmas involving your real stakeholders, judged against UK public sector values such as user needs, transparency, collaboration, accessibility, and inclusion.

Each section explains what the assessment measures, maps its dimensions to the specific skills in your capability framework, offers a substantial set of worked practice questions with full explanations, and finishes with preparation tips and common pitfalls.

How to use this guide: work through it actively rather than passively. Attempt each practice question before reading the answer. Time yourself where timing is suggested. Treat the explanations as coaching, not just marking. And use the questions as a mirror for self-reflection: each one is built from your actual duties, so a question you find difficult often points to a development area worth investing in. Take your time, be kind to yourself, and enjoy the practice.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive assessment measures the mental processes your role demands, using materials that look and feel like your day job rather than abstract puzzles. Unlike a generic IQ test, every question is built around the practical artefacts a head of analytics engineering actually handles: dimensional data models, transformation pipeline schedules, data quality dashboards, lineage diagrams, modelling standards documents, and metadata repository entries. The assessment predicts job performance by asking you to do, under mild time pressure, the same kinds of thinking your role requires: recognising patterns, deducing logical consequences, checking for errors, prioritising competing demands, and solving layered problems.

Typical formats present a scenario (a table, a diagram description, a set of rules, or a short case) followed by one or more multiple-choice questions. Assessments of this type are usually timed at 15 to 30 minutes for 20 to 30 questions, delivered online, and objectively scored against a norm group of comparable professionals. Some platforms adapt the difficulty as you go, and most give you a few ungraded practice items first so the interface never surprises you. Employers typically receive a breakdown of speed versus accuracy rather than a single score, so a careful, deliberate style is a legitimate strength as long as you keep moving.

At your level, the assessment is less about brute processing speed and more about quality of reasoning at altitude: can you see the systemic pattern behind three seemingly unrelated incidents, spot the contradiction between a standard and its implementation, and decide which of five urgent things genuinely matters most for the organisation's strategic priorities? These are exactly the judgements you make when you oversee a portfolio of data models serving analysis needs across the whole organisation.

### What it measures for your role

Each cognitive dimension maps directly onto the skills in your capability framework:

- **Pattern recognition** maps to your **Data analysis and synthesis** skill: understanding and helping teams apply data profiling techniques, analysing complex source systems, and bringing multiple data sources together in a conformed model. Recognising that three source systems share a hidden structural pattern is the essence of conformed dimensional design.
- **Logical deduction** maps to **Data modelling, cleansing and enrichment** and **Programming and build (data engineering)**: reasoning about what must be true of a data model given its grain, keys, and relationships, and about what a change to a pipeline or standard implies downstream.
- **Error checking** maps to **Testing** and **Metadata management**: reviewing requirements and specifications, defining test conditions, identifying issues and risks, and keeping repositories accurate through robust governance.
- **Prioritisation** maps to your role-level duty to **ensure the activities of the analytics engineering team align with strategic priorities**, and to your **Problem management** skill: anticipating problems, defending against them at the right time, and understanding how a problem fits into the larger picture.
- **Problem solving** maps to **Problem management** and **Data innovation**: identifying and describing problems, helping others describe them, building problem-solving capability in your community, and horizon-scanning for innovative ways of working.
- Several questions also exercise **Communicating between the technical and non-technical**, because at your level the correct answer often depends on reasoning about what a senior non-technical stakeholder has actually asked for versus what they said.

### Practice questions

Work through these in order if you can; they get progressively more demanding. Attempt each before reading the answer.

#### Question 1 (easy) - Pattern recognition in refresh schedules

Your team operates four data models with the following refresh completion times over five days:

- Finance model: 06:10, 06:12, 06:11, 06:14, 06:12
- Workforce model: 06:30, 06:45, 07:05, 07:30, 08:00
- Casework model: 05:50, 05:52, 05:49, 05:51, 05:50
- Performance model: 06:20, 06:22, 06:19, 06:21, 06:23

The organisation's daily analysis window opens at 08:30. Which model presents the most urgent risk, and why?

A) Finance, because it finishes latest on average
B) Workforce, because its completion time is drifting later by a consistent increment each day
C) Casework, because its times fluctuate
D) Performance, because it finishes after Finance

**Correct answer: B.**

**Explanation:** Three of the four models are stable, varying by only a few minutes around a fixed point. The Workforce model shows a monotonic drift: +15, +20, +25, +30 minutes day on day - the increments themselves are growing. Projecting forward, it will breach the 08:30 analysis window within roughly one more day. The pattern-recognition skill here is distinguishing random noise (Casework's one-to-two-minute wobble) from a systematic trend with acceleration. As a head of profession you would ask your team to profile the workforce pipeline now - anticipating the problem and defending against it at the right time - rather than waiting for the breach.

#### Question 2 (easy) - Logical deduction from modelling standards

Your published modelling standard states: "Every fact table must declare its grain in the metadata repository. Any fact table without a declared grain must not be promoted to the production analysis layer." A colleague tells you: "The grants fact table is in the production analysis layer."

Which one of the following must be true?

A) The grants fact table was built by your team
B) The grants fact table has a declared grain in the metadata repository, or the standard has been breached
C) The grants fact table has no data quality issues
D) The grants fact table uses Kimball dimensional modelling

**Correct answer: B.**

**Explanation:** This is a straightforward conditional deduction. The standard says: no declared grain implies no promotion to production. The grants table is in production. Therefore either it has a declared grain (satisfying the rule) or the rule was broken. Nothing in the premises tells you who built it (A), whether its data quality is good (C), or which modelling technique it uses (D) - the standard governs grain declaration, not methodology. Notice the disciplined habit this trains: as the person who ensures "standards for data models and documentation" are followed, you must reason from exactly what a standard says, not from what you assume it implies.

#### Question 3 (moderate) - Error checking a conformed dimension

You are reviewing a conformed "Organisation Unit" dimension that three data models share. The design note says: "Each row represents one organisational unit as at the current date. Historical restructures are tracked as Type 2 slowly changing dimension rows. The natural key is the unit code; the surrogate key is unique per row."

A profiling report on the dimension shows:

- 4,120 rows in total
- 3,890 distinct unit codes
- 3,890 rows flagged 'current'
- 4,120 distinct surrogate keys
- 12 rows where the 'valid from' date is later than the 'valid to' date

Which finding is an outright error, as opposed to expected behaviour?

A) More rows than distinct unit codes
B) Fewer current rows than total rows
C) Distinct surrogate keys equal to total rows
D) The 12 rows where 'valid from' is later than 'valid to'

**Correct answer: D.**

**Explanation:** In a Type 2 slowly changing dimension, history is kept as extra rows, so 4,120 rows against 3,890 unit codes simply means 230 units carry historical versions - expected (A). Exactly one row per unit is current, so 3,890 current rows is exactly right (B). Surrogate keys are unique per row by design, so 4,120 distinct keys is correct (C). But a validity window that ends before it starts is logically impossible: those 12 rows are defects, likely from a merge step that swapped the date columns or a restatement job that ran out of order. The error-checking discipline is to separate "looks odd but is by design" from "violates an invariant". Your Testing skill - defining test conditions from specifications - would turn this invariant into an automated test: valid_from must be less than or equal to valid_to on every row.

#### Question 4 (moderate) - Prioritisation across a portfolio

At Monday's triage you have five open items. The organisation's published strategic priorities are: (1) reduce casework backlog, (2) meet the accessibility commitments in the service standard, (3) improve financial forecasting.

- Item P: The casework model's queue-age measure has been silently under-counting for a week; the casework director's daily backlog report uses it.
- Item Q: A developer requests a review of a proposed naming convention change.
- Item R: The finance model refresh failed last night; a rerun is in progress and expected to succeed by noon.
- Item S: A dashboard consuming the workforce model fails screen-reader testing; the dashboard is owned by another team but built on your model's field descriptions, which are missing.
- Item T: A vendor invites you to a webinar on an emerging transformation tool.

Which two items should you act on first?

A) R and T
B) P and S
C) Q and R
D) P and Q

**Correct answer: B.**

**Explanation:** Prioritise by strategic alignment and by harm already occurring. Item P directly corrupts the evidence base for strategic priority 1, and the harm is active and invisible to its consumers - silent data corruption in a decision-making feed is the most dangerous failure class an analytics engineering leader faces. Item S engages strategic priority 2, and part of the root cause (missing field descriptions) sits in your team's documentation duty, so you owe the owning team a fast fix. Item R is self-healing - a rerun is already in progress with a credible ETA, so it needs monitoring, not leadership action. Items Q and T are legitimate but deferrable: Q is routine standards governance, T is horizon-scanning best batched into planned innovation time. The reasoning skill is mapping each item to organisational priorities and to whether harm is occurring now, rather than reacting to whatever arrived most recently or loudest.

#### Question 5 (moderate) - Pattern recognition across incident reports

Over six weeks, your team logs these incidents:

- Week 1: Duplicate rows in the grants model after a source system re-sent a batch file
- Week 2: Duplicate payments in the finance model traced to a re-sent interface file
- Week 3: No incidents
- Week 4: Inflated headcount in the workforce model after an HR extract was delivered twice
- Week 5: No incidents
- Week 6: Double-counted appointments in the casework model following a source retry

What is the most valuable conclusion for you, as head of analytics engineering, to draw?

A) Each source team should be told to stop re-sending files
B) The incidents share a common structural cause - the transformation layer is not idempotent with respect to repeated source deliveries - and a cross-cutting standard for deduplication or idempotent loading is needed
C) The four models should be merged into one to simplify support
D) Week 3 and week 5 show the problem is intermittent and can be tolerated

**Correct answer: B.**

**Explanation:** Four incidents in four different models, four different source systems, one identical mechanism: a repeated delivery is ingested twice because the loading pattern assumes exactly-once delivery. Seeing "how a problem fits into the larger picture" is precisely your Problem management skill at this level: a team member sees four unrelated bugs; a head of profession sees one architectural weakness expressed four times. Option A treats the symptom and depends on the behaviour of teams you do not control - and retries are often legitimate. Option C is disproportionate and unsupported. Option D confuses absence of detection with absence of risk. The leadership move implied by B - setting a cross-team standard for idempotent loads and key-based deduplication - is exactly "develop standards for data transformation" applied at portfolio scale.

#### Question 6 (moderate) - Deduction about pipeline dependencies

Your overnight schedule has these dependency rules:

- The staging load must finish before any model build starts.
- The finance model build must finish before the performance model build starts, because performance consumes finance outputs.
- The workforce model build has no dependencies other than staging.
- The documentation harvest runs only after every model build has finished.

Last night the documentation harvest never ran, the workforce model built successfully, and staging finished on time. Which of the following can you validly conclude?

A) The finance model build failed
B) At least one of the finance or performance model builds did not finish
C) The performance model build started but crashed
D) The staging load produced bad data

**Correct answer: B.**

**Explanation:** The harvest runs only after every model build finishes. It did not run, so at least one build did not finish. Workforce finished, and staging completed on time, so the unfinished build must be among finance and performance - but you cannot tell which. Perhaps finance failed (so performance never started), or finance succeeded and performance failed, or performance is merely still running. Option A over-claims: finance failing is one possibility, not a certainty. Option C also over-claims - performance may never have started. Option D introduces a cause with no evidence. The disciplined habit is to deduce the weakest conclusion the facts force, and no more; when you take "technical responsibility for all stages" of a build, incident diagnosis starts with what is certain, then investigates the branches.

#### Question 7 (moderate) - Error checking a metadata repository entry

A metadata repository entry for the field "case_closed_date" reads:

1. Definition: "The date the case was closed by a caseworker."
2. Source: "CRM system, table CASES, column CLOSE_DT."
3. Transformation: "Converted from UTC timestamp to date using the Europe/London time zone."
4. Data quality rule: "Must be null for open cases; must be on or after case_opened_date for closed cases."
5. Last validated: "14 March" (this year), by the data governance analyst.

Users report that a small number of cases show case_closed_date one day earlier than the date the caseworker remembers closing the case, and all such cases were closed shortly after midnight during British Summer Time. Which entry line points to the likely defect?

A) Line 1 - the definition is wrong
B) Line 2 - the source column is wrong
C) Line 3 - the documented time zone conversion is probably not what the code actually does
D) Line 4 - the data quality rule is too strict

**Correct answer: C.**

**Explanation:** The symptom signature is diagnostic: errors of exactly one day, only near midnight, only during British Summer Time. That is the classic fingerprint of a UTC timestamp truncated to a date without applying the London offset - a case closed at 00:30 BST is 23:30 UTC the previous day, so truncating in UTC yields the prior date. The metadata says the conversion applies Europe/London, but the observed behaviour says the code does not; the documentation and the implementation have diverged. This is why your Metadata management skill emphasises "robust governance processes to keep repositories up to date": a repository entry that describes intended rather than actual behaviour is worse than no entry, because it sends investigators in the wrong direction. The corrective actions are to fix the conversion, add a test around the midnight boundary (your Testing skill), and re-validate the entry.

#### Question 8 (challenging) - Conformed model synthesis

Three source systems record training activity:

- System 1 (HR): one row per employee per completed course, keyed by payroll number and course code.
- System 2 (Learning platform): one row per enrolment attempt, keyed by email address and course identifier, including failed and abandoned attempts.
- System 3 (Professional body): one row per certification awarded, keyed by membership number, with no course-level detail.

A senior stakeholder wants a single "learning and capability" model answering: "How many staff completed each course, how many attempts did completions take, and how many hold certifications?" Which design consideration is most critical to get right first?

A) Choosing the colour scheme of the eventual dashboard
B) Establishing a conformed person dimension that reliably maps payroll number, email address, and membership number to a single individual
C) Deciding whether to schedule the refresh nightly or weekly
D) Selecting which cloud region hosts the model

**Correct answer: B.**

**Explanation:** Every question the stakeholder asks joins facts about the same person across three systems that identify people three different ways. Without a trustworthy person-matching spine - a conformed dimension with survivorship rules for identity resolution - counts of "staff who completed" versus "attempts per completion" versus "certification holders" cannot be combined; you would double-count people whose email changed or miss those whose membership record uses a maiden name. This is your Data analysis and synthesis skill verbatim: "bring multiple data sources together in a conformed model for analysis." Options A, C, and D are real decisions but all downstream: a beautiful, frequently refreshed, well-hosted model built on broken identity matching produces confidently wrong answers. Note too the different grains (completion, attempt, award) - each should become its own fact table sharing the conformed person and course dimensions, a textbook Kimball bus architecture judgement.

#### Question 9 (challenging) - Prioritising a standards roll-out

You are sequencing a programme to raise standards compliance across six teams. Facts:

- Teams vary in size: two large teams produce 70% of the organisation's data models between them; four small teams produce the rest.
- One small team is an enthusiastic early adopter that has volunteered to pilot.
- The two large teams are sceptical and busy with a legislative deadline for the next two months.
- Standards adopted without tooling support have historically decayed within a quarter.
- Your engineering effort can support either tooling development or intensive team onboarding this quarter, not both.

Which sequencing is most defensible?

A) Onboard the two large teams first, since they produce most models
B) Build the compliance tooling first while piloting the standard with the volunteer small team, then onboard the large teams after their legislative deadline
C) Onboard all four small teams first to build momentum
D) Delay everything until the large teams are free

**Correct answer: B.**

**Explanation:** Work through the constraints jointly rather than one at a time. The large teams matter most by volume, but they are unavailable for two months and sceptical - forcing onboarding now (A) spends your credibility at the worst moment and violates your duty to align activities with strategic priorities, since the legislative deadline is plainly one. History says standards without tooling decay, so tooling is a prerequisite for durable adoption, and your single quarter of engineering effort should go there. The volunteer team gives you a low-cost pilot that hardens the standard and generates an internal success story - useful for the advocacy part of your role - without consuming the engineering effort. Option C generates motion but only touches 30% of model production and leaves tooling unbuilt. Option D wastes the quarter entirely. B is the only option that satisfies every constraint simultaneously; this multi-constraint scheduling logic is what portfolio-level prioritisation actually is.

#### Question 10 (challenging) - Problem definition before problem solving

A programme director tells you: "Your data models are wrong - my dashboard says we processed 40,000 applications last month but my operations manager counted 43,000." Before proposing any fix, which single clarifying question most efficiently narrows the problem space?

A) "Which modelling technique do you think we should have used?"
B) "Are both figures counting the same thing over the same period - for example, does one count applications received and the other applications completed, and do both use the same month boundaries?"
C) "Would you like us to rebuild the model from scratch?"
D) "Have you tried refreshing the dashboard?"

**Correct answer: B.**

**Explanation:** Your Problem management skill includes "identify and describe problems, and help others to describe them" - and most reported data discrepancies dissolve under precise definition rather than requiring a technical fix. The two most common causes of a mismatch like this are definitional (received versus completed, first-touch versus final decision) and temporal (calendar month versus operational reporting period, time zone of the cut-off). Option B tests both in one question and, crucially, helps the stakeholder articulate what their number actually measures - communicating between the technical and the non-technical in its most practical form. Options A and C leap to solutions before the problem exists in any well-defined form. Option D is a support-desk reflex, not leadership diagnosis. Only after B fails to resolve the gap would you commission reconciliation work: profiling the source, tracing lineage, checking filters and joins.

#### Question 11 (challenging) - Deduction with an innovation claim

A vendor claims: "Organisations that adopted our automated transformation tool reduced pipeline failures by 60%." During horizon-scanning, you check the claim before recommending a trial. Which additional fact, if true, most seriously undermines the claim's relevance to a decision?

A) The vendor's customer base is mostly retail companies
B) The figure compares customers' failure rates before and after adoption, and adopting organisations simultaneously hired dedicated reliability engineers as part of the same improvement programme
C) The tool is priced per user
D) The vendor was founded four years ago

**Correct answer: B.**

**Explanation:** Option B describes a classic confounded comparison: two interventions (the tool and the new engineers) were applied together, so the 60% improvement cannot be attributed to the tool - some, most, or all of it may come from the staffing change. This is the sharpest logical flaw because it attacks the causal inference itself. Option A weakens generalisability to your sector but the underlying effect could still be real. Options C and D are commercially relevant but say nothing about whether the tool works. Your Data innovation skill asks you to "investigate emerging trends and introduce innovative ways of working" - and the investigation half of that duty is precisely this kind of critical reading of evidence before you spend public money or your team's attention.

#### Question 12 (challenging) - Multi-step fault isolation

Users report that yesterday's regional performance figures look implausibly low. You establish the following, in order:

1. The staging layer's row counts for yesterday match the source system exactly.
2. The transformation step's output row count is 8% lower than staging.
3. The transformation step applies two filters: exclude test records (normally removes about 0.5%) and exclude records with a null region code (normally removes about 0.3%).
4. The source system's release notes mention that a patch deployed two days ago changed the format of region codes from "R01" style to "REG-01" style.

What is the most probable fault chain?

A) The source is sending fewer rows than it should
B) The staging layer is dropping rows
C) The transformation's region-code validation no longer recognises the new "REG-01" format, so valid records are being treated as having invalid or unmapped region codes and excluded or misfiled, explaining the abnormal shrinkage after staging
D) Users are misreading the dashboard

**Correct answer: C.**

**Explanation:** Reason stepwise through the evidence. Fact 1 exonerates the source and the extract: staging matches source, so option A and option B are eliminated. Fact 2 localises the loss to the transformation step. Fact 3 says normal filter losses total roughly 0.8%, but observed loss is 8% - ten times normal, so a filter is misbehaving rather than merely active. Fact 4 supplies the mechanism and the timing: a region-code format change would make a validation or lookup built for "R01" fail to match "REG-01", swelling the "null or invalid region" exclusion exactly where the rows are vanishing. Option D is incompatible with the measured row loss. This is textbook fault isolation - bracket the failure between the last known-good checkpoint and the first bad one, then find the recent change that explains it. It is also a governance lesson your role exists to teach: upstream format changes must reach your team before deployment, which is why you build relationships with senior stakeholders across the organisation and set standards for communication.

#### Question 13 (challenging) - Reasoning about documentation coverage

Your documentation standard requires every production model to have: a purpose statement, an owner, a data dictionary, and a refresh schedule entry. An audit samples the portfolio and finds:

- 100% of models have an owner
- 92% have a purpose statement
- 74% have a complete data dictionary
- 96% have a refresh schedule entry
- Models built in the last year score above 95% on all four elements; older models account for almost all gaps

Which conclusion is best supported?

A) The documentation standard has failed and should be replaced
B) The standard is working for new builds; the gap is a legacy backfill problem, so the right response is a prioritised remediation plan for older models rather than a new standard
C) Data dictionaries are unnecessary since most models lack them
D) The audit sample must be wrong

**Correct answer: B.**

**Explanation:** Disaggregate before concluding. The headline 74% dictionary coverage looks like standards failure, but the age split shows new models comply at over 95% across the board - the standard, and the culture around it, works where it has had the chance to operate. The deficit is concentrated in models predating the standard, which is a stock problem (backfill) not a flow problem (compliance). Option A throws away a working instrument; option C reverses the logic - 74% have dictionaries, and coverage below target is a gap, not evidence of uselessness; option D rejects data without grounds. The leadership follow-through for B is a risk-ranked backfill: dictionary-first for the models with the most consumers, folded into planned maintenance. This is "ensure the team works to standards for data models and documentation" done with judgement rather than blame.

### Preparation tips

- **Practise on your own artefacts.** For a fortnight, treat routine work as test preparation: when a pipeline fails, consciously bracket the fault between known-good and known-bad checkpoints; when an incident report lands, ask what larger pattern it belongs to. The assessment rewards habits, and habits are built on the job.
- **Rehearse the "weakest valid conclusion" discipline.** Senior candidates lose marks by over-concluding - choosing the answer that is plausible rather than the one the evidence forces. When two options both seem right, pick the one that claims less.
- **Do a few timed sets.** Even though your reasoning is strong, timed multiple-choice is its own format. Two or three 20-minute practice sessions will stop the clock feeling like an adversary.
- **Read every option before answering.** Distractors at senior level are crafted to be "true but not the point" - correct statements that do not answer the question asked.
- **Trust structure over recall.** Questions never require knowledge the scenario does not give you. If you find yourself relying on a fact from your own organisation, you have drifted off the page.
- **Manage energy, not just time.** At head-of level the questions are long. Skim the question stem first, then read the scenario knowing what you are looking for.

### Common pitfalls

- **Answering from experience instead of the scenario.** You have deep domain knowledge; the test wants reasoning from the given facts. If the scenario's world differs from yours, the scenario wins.
- **Getting stuck on a time-sink question.** One gnarly multi-step item can consume five easier ones' worth of time. Flag it, move on, return if time allows.
- **Confusing correlation with mechanism.** Several questions plant a plausible-sounding cause with no supporting mechanism; insist on evidence linking cause to effect.
- **Missing scale and unit qualifiers.** Row counts, percentages, and times are chosen so that a skim-reader picks the wrong distractor. Read numbers twice.
- **Treating stable noise as signal.** Small random fluctuations are normal in operational data; the tests reward distinguishing drift from wobble.
- **Rushing the error-checking items.** These reward meticulousness. A deliberate pace with high accuracy typically scores better than fast guessing, because reports separate speed from accuracy.


## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment evaluates your ability to analyse, interpret, and make sound decisions using numerical data presented the way your role presents it: budget tables, capacity plans, performance dashboards, data quality scorecards, and team utilisation figures. It is business mathematics, not abstract formulae - percentages, ratios, rates, weighted averages, and cost-benefit estimation applied to realistic figures. Most versions allow or provide an on-screen calculator, because the skill being measured is interpretation and decision-making, not mental arithmetic. Expect a strict time limit - often around a minute to ninety seconds per question - which rewards quick, accurate data extraction and sensible estimation.

For a head of analytics engineering, numeric reasoning is not an academic nicety. You size and defend budgets for people and technology, present pipeline reliability and adoption metrics to boards, weigh the cost of technical debt against delivery pressure, plan team capacity across a portfolio of models, and challenge vendor claims with arithmetic. When you advocate for the analytics engineering function to senior leadership, the strength of your case usually rests on numbers - cost per model maintained, hours returned to analysts, error rates driven down - and the credibility of your advocacy rests on those numbers surviving scrutiny. The assessment simulates exactly that: extracting the right figures from a table, combining them correctly, and noticing when a percentage is doing something sneaky.

Questions typically show a dataset (a table or described chart) followed by two to four questions of escalating difficulty. Every explanation below shows the arithmetic in full, because the working - not just the answer - is what you should be practising.

### What it measures for your role

- **Budget and cost reasoning** supports your role-level duty to **ensure appropriate technology is available for the community**: comparing licence models, projecting storage and compute costs, and making the value case for tooling.
- **Capacity and utilisation arithmetic** supports **building analytics engineering capability** and aligning **team activities with strategic priorities**: headcount planning, allocation across models, and the cost of support load versus development.
- **Data quality metrics** map to **support data quality improvement** and your **Testing** skill: pass rates, defect rates, error percentages, and the arithmetic of "analyse and report test activities and results".
- **Performance and adoption metrics** map to **Communicating between the technical and non-technical** and advocacy: usage growth, query volumes, and the honest presentation of percentage change to senior audiences.
- **Ratio and rate reasoning across sources** maps to **Data analysis and synthesis**: reconciling counts and rates when multiple systems measure the same thing differently.
- **Critical evaluation of claimed numbers** maps to **Data innovation**: horizon-scanning includes doing the vendor's arithmetic yourself.

### Practice questions

An on-screen calculator is assumed to be available. Work each answer before reading the explanation, and check the arithmetic line by line.

#### Question 1 (easy) - Team allocation percentage

Your analytics engineering team has 20 engineers. This quarter, 7 are building new models, 9 are maintaining and supporting existing models, and the rest are working on the standards and tooling programme. What percentage of the team is on standards and tooling?

A) 15%
B) 20%
C) 25%
D) 30%

**Correct answer: B.**

**Explanation:** Engineers on standards and tooling = 20 - 7 - 9 = 4. As a percentage: 4 / 20 = 0.20 = **20%**. A useful sanity check at speed: 10% of 20 is 2, so 4 people is 2 × 10% = 20%. Questions like this are about careful extraction - the number you need (4) is not printed anywhere and must be derived from the total first.

#### Question 2 (easy) - Data quality pass rate

Last month your automated test suite ran 12,500 data quality checks across the model portfolio, of which 275 failed. What was the pass rate?

A) 97.8%
B) 96.4%
C) 99.1%
D) 95.0%

**Correct answer: A.**

**Explanation:** Failures as a proportion: 275 / 12,500 = 0.022 = 2.2%. Pass rate = 100% - 2.2% = **97.8%**. Alternatively directly: passes = 12,500 - 275 = 12,225; 12,225 / 12,500 = 0.978. When you report test activities and results to a board, converting between failure counts and pass rates fluently - and knowing that "2.2% failure" and "97.8% pass" are the same fact wearing different clothes - is part of communicating between the technical and the non-technical.

#### Question 3 (easy) - Storage growth projection

The conformed warehouse layer currently holds 48 TB and has grown at a steady 5% per month. Approximately how much storage will it need in three months?

A) 50.4 TB
B) 52.9 TB
C) 55.6 TB
D) 60.0 TB

**Correct answer: C.**

**Explanation:** Compound the growth month by month: 48 × 1.05 = 50.4 TB after month one; 50.4 × 1.05 = 52.92 TB after month two; 52.92 × 1.05 = 55.566 TB after month three, so approximately **55.6 TB**. Equivalently 48 × 1.05³ = 48 × 1.157625 = 55.566. Distractor A is one month's growth; distractor B is two months'; a common trap is applying simple rather than compound growth (48 × 1.15 = 55.2 would be close here, but the gap widens over longer horizons, so build the compounding habit).

#### Question 4 (moderate) - Comparing licence models

You must recommend one of two transformation tool licence options for your 20-engineer team, over one year:

- Option A: £600 per user per year, all features included.
- Option B: £4,000 flat platform fee per year, plus £350 per user per year, plus a one-off £2,500 onboarding charge in year one.

Which option is cheaper in year one, and by how much?

A) Option A, by £1,500
B) Option B, by £1,500
C) Option B, by £500
D) Option A, by £500

**Correct answer: A.**

**Explanation:** Option A: 20 × £600 = £12,000. Option B: £4,000 + (20 × £350) + £2,500 = £4,000 + £7,000 + £2,500 = £13,500. Option A is cheaper in year one by £13,500 - £12,000 = **£1,500**. The common error is forgetting the one-off onboarding charge: a candidate who sums only B's recurring costs (£4,000 + £7,000 = £11,000) concludes B is cheaper by £1,000 and reaches for the nearest "Option B" distractor. Write every component down, sum once, compare once. Note also that in year two, with no onboarding charge, B costs £11,000 against A's £12,000 - so the multi-year recommendation may genuinely differ from the year-one arithmetic, which is exactly the nuance you would raise when ensuring appropriate technology is available for the community over a spending review period, not just a single year.

#### Question 5 (moderate) - Support load ratio

Your service desk data shows the four main data models generated the following support tickets last quarter, alongside each model's number of active users:

| Model | Tickets | Active users |
|---|---|---|
| Finance | 84 | 420 |
| Workforce | 66 | 220 |
| Casework | 90 | 600 |
| Performance | 40 | 160 |

Which model has the highest support burden per 100 active users?

A) Finance
B) Workforce
C) Casework
D) Performance

**Correct answer: B.**

**Explanation:** Compute tickets per 100 users for each model. Finance: 84 / 420 × 100 = 20.0. Workforce: 66 / 220 × 100 = 30.0. Casework: 90 / 600 × 100 = 15.0. Performance: 40 / 160 × 100 = 25.0. Workforce, at **30 tickets per 100 users**, carries the heaviest relative burden even though Casework has the most tickets in absolute terms. This normalisation habit - burden per user rather than raw counts - is fundamental when you decide where to direct improvement effort: raw ticket counts would send you to Casework, the healthiest model of the four per user. The follow-on leadership question, of course, is why Workforce users struggle: data quality, documentation, or training - each implying a different remedy from your duties list.

#### Question 6 (moderate) - Percentage change in adoption

Monthly queries against the conformed analysis layer were 180,000 in January. They fell 10% in February during a migration freeze, then rose 25% in March relative to February. What were March's query volumes, and what is the overall percentage change from January to March?

A) 202,500 queries; +12.5% overall
B) 207,000 queries; +15% overall
C) 202,500 queries; +15% overall
D) 198,000 queries; +10% overall

**Correct answer: A.**

**Explanation:** February: 180,000 × 0.90 = 162,000. March: 162,000 × 1.25 = 202,500. Overall change: (202,500 - 180,000) / 180,000 = 22,500 / 180,000 = 0.125 = **+12.5%**. The trap is adding the percentages (-10% + 25% = +15%) and choosing distractor B or C; sequential percentage changes multiply (0.90 × 1.25 = 1.125), they never add. When you present adoption trends to senior leadership as part of advocating for the function, this is precisely the arithmetic that must be right, because a finance director in the audience will do it in their head.

#### Question 7 (moderate) - Weighted average documentation coverage

Documentation coverage is measured per team as the percentage of models with complete data dictionaries:

| Team | Models owned | Coverage |
|---|---|---|
| Central platforms | 40 | 95% |
| Operations analytics | 25 | 80% |
| Corporate analytics | 15 | 60% |

What is the organisation-wide coverage across all 80 models?

A) 78.3%
B) 83.75%
C) 85.0%
D) 90.0%

**Correct answer: B.**

**Explanation:** Weight each team's coverage by its model count. Documented models: Central 40 × 0.95 = 38; Operations 25 × 0.80 = 20; Corporate 15 × 0.60 = 9. Total documented = 38 + 20 + 9 = 67 of 80 models. Coverage = 67 / 80 = 0.8375 = **83.75%**. Distractor A (78.3%) is the unweighted mean of the three percentages ((95 + 80 + 60) / 3), the single most common error with grouped percentages. As the leader who ensures the team works to documentation standards, you would also note the distribution: the headline 83.75% conceals a 60% team, and averages must never be allowed to hide the tail - a point worth making explicitly when you report the figure upwards.


#### Question 8 (moderate) - Pipeline runtime capacity

Your overnight batch window runs from 01:00 to 07:00 (six hours). Current pipeline stages run sequentially: staging load 95 minutes, transformation 120 minutes, model builds 85 minutes, documentation harvest 25 minutes. A new legislative reporting model is forecast to add 40 minutes to transformation and 20 minutes to model builds. Will the window still hold?

A) Yes, with 35 minutes of slack
B) Yes, with 15 minutes of slack
C) No, it will overrun by 25 minutes
D) Yes, with 60 minutes of slack

**Correct answer: C.**

**Explanation:** Current total: 95 + 120 = 215; 215 + 85 = 300; 300 + 25 = 325 minutes. The window is 6 hours = 360 minutes, so today's slack is 360 - 325 = 35 minutes (distractor A is that current slack, offered to catch anyone who stops before applying the change). Additions: 40 + 20 = 60 minutes. New total: 325 + 60 = 385 minutes, which exceeds the 360-minute window by 385 - 360 = **25 minutes**. The demand (60 extra minutes) exceeds the available slack (35 minutes) by exactly the overrun. The leadership consequence matters as much as the arithmetic: as head of analytics engineering you would refuse to accept the new model into the sequential window as designed, and instead direct the team to parallelise independent stages (workforce and finance builds share no dependency, for instance) or negotiate a wider window with infrastructure stakeholders - a capacity conversation to have before onboarding the legislative model, not after it breaches. Anticipating the problem and defending against it at the right time is your Problem management skill applied to schedule arithmetic.

#### Question 9 (challenging) - Cost per model and marginal reasoning

Your function's annual budget is £2.4 million, covering 20 engineers and platform costs of £400,000. The team maintains 80 production models. A partner directorate asks you to take on 10 more models of similar complexity, offering £200,000 of annual funding. Assume engineer cost is the remaining budget divided equally per engineer, maintenance effort scales with model count, and each engineer can sustain 4 models alongside their other duties.

What is the approximate annual cost to maintain one model under the current budget, and is the £200,000 offer sufficient for 10 more?

A) £30,000 per model; the offer is sufficient
B) £25,000 per model; the offer falls short by £50,000
C) £30,000 per model; the offer falls short by £100,000
D) £20,000 per model; the offer is exactly sufficient

**Correct answer: C.**

**Explanation:** Step 1 - staff budget: £2,400,000 - £400,000 platform = £2,000,000 for 20 engineers, i.e. £100,000 per engineer. Step 2 - maintenance capacity: each engineer sustains 4 models, so one model consumes a quarter of an engineer: £100,000 / 4 = £25,000 of staff cost. Step 3 - platform cost per model: £400,000 / 80 = £5,000. Total: £25,000 + £5,000 = **£30,000 per model**. Step 4 - the ask: 10 models × £30,000 = £300,000 needed; £200,000 offered; shortfall = **£100,000**. Distractor B uses staff cost only, forgetting the platform share - the classic omission when costing marginal work. In role terms, this is the arithmetic behind a difficult stakeholder conversation: you can now say precisely why the offer funds two-thirds of the work, propose options (fund fully, descope, or accept degraded support standards explicitly), and keep the relationship strong while refusing an underfunded commitment - managing stakeholder expectations with evidence.

#### Question 10 (challenging) - Data quality improvement trajectory

A data quality improvement programme aims to cut the defect rate in the casework model from 4.8% of records to below 1.5% within three quarters. Each quarter, the planned remediation reduces the defect rate by 35% of its value at the start of that quarter. Will the programme hit its target, and what is the projected rate after three quarters?

A) Yes; approximately 1.32%
B) No; approximately 1.56%
C) Yes; approximately 1.02%
D) No; approximately 1.87%

**Correct answer: A.**

**Explanation:** A 35% reduction each quarter leaves 65% of the rate: after Q1: 4.8% × 0.65 = 3.12%. After Q2: 3.12% × 0.65 = 2.028%. After Q3: 2.028% × 0.65 = 1.3182% ≈ **1.32%**, which is below the 1.5% target - the programme succeeds with modest headroom. Equivalently 4.8 × 0.65³ = 4.8 × 0.274625 = 1.318. Distractor D applies 35% of the original rate each quarter (4.8 - 3 × 1.68 would actually go negative; 1.87 comes from other misapplications) and distractor B mixes simple and compound steps. Two leadership observations belong in your report of these results: first, compound percentage reductions get harder in absolute terms as the base shrinks (Q1 removes 1.68 points, Q3 removes only 0.71), so the same 35% relative effort yields visibly diminishing headline movement - set that expectation with stakeholders early; second, headroom of 0.18 points is thin, so a single bad source delivery could breach the target and the plan needs contingency.

#### Question 11 (challenging) - Reconciling counts across systems

Two systems report on the same grant applications. System X (operational) reports 26,450 applications received last month. Your conformed model reports 25,780. Investigation shows the model excludes test records (approximately 1.2% of System X volume) and applications withdrawn within 24 hours (approximately 1.3% of System X volume), and the two exclusions never overlap. After accounting for both exclusions, roughly how many applications remain unexplained by the documented differences?

A) About 10
B) About 320
C) About 660
D) Essentially zero

**Correct answer: A.**

**Explanation:** Expected exclusions: test records = 26,450 × 0.012 = 317.4; early withdrawals = 26,450 × 0.013 = 343.85. Combined (no overlap): 317.4 + 343.85 = 661.25, so the model should hold approximately 26,450 - 661 = 25,789. Observed model count: 25,780. Unexplained gap: 25,789 - 25,780 = **about 9-10 records**. Distractor C is the total exclusion volume mistaken for the residual; distractor B is one exclusion applied but not the other. The judgement layered on the arithmetic: a residual of ~10 in 26,000 (0.04%) is within the tolerance of two approximate exclusion rates, so the systems substantively reconcile - you would document the reconciliation and move on, rather than commissioning a forensic hunt. Knowing when a discrepancy is material is as much a numeric skill as computing it, and it is exactly what "analyse and report test activities and results" means at portfolio level.

#### Question 12 (challenging) - Capability investment trade-off

You have £120,000 of discretionary budget for capability building. Options:

- Option 1: External training for all 20 engineers at £3,500 each, historically lifting productivity 5%.
- Option 2: Hire one senior contractor for a year at £120,000 to deliver a mentoring programme, historically lifting the productivity of the 12 mid-level engineers by 10%, with no effect on the 8 senior engineers.

Assume every engineer currently delivers £150,000 of annual value. Which option yields the greater first-year value uplift, and by how much?

A) Option 1, by £30,000
B) Option 2, by £30,000
C) They are equal
D) Option 1, by £50,000

**Correct answer: B.**

**Explanation:** Option 1 cost check: 20 × £3,500 = £70,000 (within budget). Gross uplift: 20 engineers × £150,000 × 5% = 20 × £7,500 = **£150,000**. Option 2 cost: £120,000 (all of it). Gross uplift: 12 engineers × £150,000 × 10% = 12 × £15,000 = **£180,000**. The question asks for "first-year value uplift" - the gross figure - so Option 2 wins by £180,000 - £150,000 = **£30,000**. Now notice why distractor A is so tempting: if you instead compare uplift net of cost, Option 1 nets £150,000 - £70,000 = £80,000 while Option 2 nets £180,000 - £120,000 = £60,000, and Option 1 wins. Both computations are legitimate analyses; only one answers the question asked. This gross-versus-net distinction is where senior numeric reasoning lives: read the exact wording ("value uplift", not "net benefit"), answer what is asked, then bring the fuller trade-off - the £50,000 of unspent budget under Option 1, mentoring's lasting effect on career development (a duty of your role level), and single-contractor key-person risk - as the narrative you would wrap around the number in a real investment case.

#### Question 13 (challenging) - Interpreting a performance dashboard honestly

Your quarterly dashboard shows: model refresh success rate 99.2% (up from 98.8%); mean refresh duration 42 minutes (up from 35); 95th percentile refresh duration 118 minutes (up from 61); analyst-reported data issues 44 (down from 51). A colleague drafts the headline: "All key indicators improved this quarter." Which correction does the arithmetic demand?

A) No correction; all indicators improved
B) The success rate actually fell
C) Both duration measures worsened - the 95th percentile nearly doubled (61 to 118 minutes, a rise of about 93%) - so the headline is wrong for two of four indicators, and the tail deterioration is the most operationally significant fact on the page
D) Analyst-reported issues rose

**Correct answer: C.**

**Explanation:** Check each indicator's direction. Success rate: 98.8% to 99.2% = improved. Mean duration: 35 to 42 minutes = worsened by 20% (7/35 = 0.20). 95th percentile: 61 to 118 = worsened by (118 - 61) / 61 = 57/61 ≈ 93.4% - the slowest refreshes now take nearly twice as long, which is what analysts actually experience on bad days. Issues: 51 to 44 = improved (a fall of 13.7%). Two up, two down: the headline is false. The deeper point is the mean-versus-tail contrast: the mean rose 20% while the 95th percentile rose 93%, indicating the distribution has grown a long tail - a few very slow refreshes rather than uniform slowdown, typically one or two misbehaving models worth isolating. Presenting figures to senior leadership with this honesty is central to advocacy that survives scrutiny: a dashboard headline your audience later discovers to be spin costs the function more credibility than the slow pipelines did.

#### Question 14 (moderate) - Ratio reasoning for team shape

Your target operating model says the sustainable ratio of models in production to engineers is 4:1, and the sustainable ratio of engineers to team leads is 6:1. The portfolio is forecast to grow from 80 to 108 production models over two years. How many engineers and team leads will you need at the end of that period, and how many more engineers is that than today's 20?

A) 27 engineers and 5 team leads; 7 more engineers
B) 27 engineers and 4 team leads; 7 more engineers
C) 24 engineers and 4 team leads; 4 more engineers
D) 32 engineers and 6 team leads; 12 more engineers

**Correct answer: A.**

**Explanation:** Engineers needed: 108 models ÷ 4 models per engineer = 27 engineers. That is 27 - 20 = **7 more** than today. Team leads: 27 engineers ÷ 6 engineers per lead = 4.5 - and you cannot employ half a team lead, so you round **up** to 5; rounding down to 4 (distractor B) would put one lead over the sustainable ratio, which defeats the point of having one. Distractor C uses today's 80-model figure plus the growth applied to engineers only; distractor D applies the 4:1 ratio in the wrong direction. Two habits to take from this: ratios describing capacity are division problems whose direction you must fix before calculating (models per engineer, not engineers per model), and staffing arithmetic rounds up at every fractional step because people come in whole units. This is the quiet numeric spine of the workforce plan you would take into a spending review when building analytics engineering capability.

### Preparation tips

- **Rebuild fluency with the core four.** Percentages of a total, percentage change, weighted averages, and unit rates (cost per model, tickets per user) cover most senior numeric items. Ten minutes a day for two weeks restores speed.
- **Always write the components before summing.** The most common senior-level error is omission (a platform share, a one-off fee), not miscalculation.
- **Multiply sequential percentage changes; never add them.** Say it until it is a reflex: 0.90 × 1.25, not -10% + 25%.
- **Read what the question asks - gross or net, per user or absolute, one month or overall.** Senior distractors are correct answers to slightly different questions.
- **Practise with your own management information.** Recompute a figure from your last quarterly return by hand; the format familiarity transfers directly.
- **Use the calculator for arithmetic, your head for structure.** Decide the operations first, then compute; candidates who calculate before structuring produce plausible wrong numbers quickly.
- **Estimate before you compute.** A rough order-of-magnitude guess catches slips: if 4.8% compounding down by a third per quarter for three quarters must land somewhere near 1.3%, an answer of 0.13% or 13% is instantly suspect.

### Common pitfalls

- **Misreading scale qualifiers.** "In thousands", "per 100 users", "per quarter" - confusing monthly with annual data, or absolute counts with normalised rates, is the single most frequent error the format is designed to catch.
- **Unweighted averages of grouped percentages.** Averaging 95%, 80% and 60% without weighting by group size gives a confidently wrong organisational figure.
- **Over-calculating.** Some items yield to estimation and elimination in fifteen seconds; performing full-precision arithmetic on every option is a time sink.
- **Time-sink questions.** One multi-stage budget item can cost you three easier questions. Flag, skip, return.
- **Stopping at the first plausible number.** Distractors are built from your intermediate results - the staff-only cost, the one-exclusion residual. If your number matches an option after step two of a four-step problem, keep going.
- **Ignoring materiality.** Not every discrepancy deserves pursuit; part of what is being measured is whether you can tell a 0.04% residual from a 4% one under time pressure.


## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment measures how accurately you understand, analyse, and draw conclusions from written material of the kind your role puts in front of you daily: data strategies, modelling standards, governance policies, stakeholder emails, audit findings, and vendor documentation. The dominant format presents a dense passage followed by statements you must classify as **True** (the passage logically supports it), **False** (the passage contradicts it), or **Cannot Say** (the passage provides insufficient information either way). Multiple-choice comprehension questions - "which statement best summarises", "what does the author imply" - round out most tests. Timing is brisk: typically under a minute per question, simulating the reality of reading a board paper minutes before the meeting.

The iron rule of the format is: **answer only from the text**. Your extensive professional knowledge is, for once, a liability - the test deliberately includes statements that are true in the real world but unsupported by the passage, and vice versa. "Cannot Say" is not an admission of defeat; it is frequently the correct, disciplined answer.

For a head of analytics engineering, this skill is far from academic. You interpret policy wording to decide what your standards must mandate; you read stakeholder emails for what they actually commit to versus what they appear to; you review audit reports where the difference between "the team did not evidence X" and "the team did not do X" determines your response; and you draft communications where a single ambiguous sentence can misdirect six teams. Precision reading is the quiet foundation of managing stakeholder expectations and moderating difficult discussions about high-risk topics.

### What it measures for your role

- **Comprehension of policy and standards language** maps to your duty to **ensure the team works to standards for communication, data models and documentation**, and to **develop standards for data transformation**: standards are texts, and enforcing them starts with reading them exactly.
- **Distinguishing stated fact from implication** maps to **Communicating between the technical and non-technical**: mediating between people and moderating difficult discussions about high-risk topics requires hearing precisely what was and was not said.
- **Extracting commitments and conditions from correspondence** maps to **building relationships with senior stakeholders** and **managing stakeholder expectations**: misreading a conditional promise as a firm one damages both.
- **Critical reading of claims and evidence** maps to **Data innovation** (horizon-scanning vendor and research material) and **Testing** (reviewing requirements and specifications, where ambiguity is a defect).
- **Reading data documentation precisely** maps to **Metadata management** and **create and maintain data documentation**: a repository definition means exactly what it says, and so must you.

### Practice questions

For each passage, answer every question strictly from the passage text. Options for True/False/Cannot Say items are exactly those three.

#### Passage A - Data transformation standard (Questions 1-4)

*"All transformation code deployed to the production environment must pass the automated test suite and be peer reviewed by an engineer who did not author the change. Emergency fixes may be deployed with retrospective review, provided the review occurs within two working days and the head of analytics engineering is notified before deployment. Transformation code that reads personal data must additionally be approved by the data protection team. This standard applies to all analytics engineering teams; teams in arm's-length bodies are encouraged, but not required, to adopt it."*

#### Question 1 (easy)

Statement: "Under the standard, an emergency fix may reach production before it has been peer reviewed."

**Correct answer: True.**

**Explanation:** The passage says emergency fixes "may be deployed with retrospective review" - review after deployment - subject to two conditions (review within two working days; the head of analytics engineering notified before deployment). Deployment preceding review is therefore explicitly permitted. Note the precision required: the conditions constrain the permission but do not negate it.

#### Question 2 (easy)

Statement: "Teams in arm's-length bodies must comply with the standard."

**Correct answer: False.**

**Explanation:** The final sentence states such teams are "encouraged, but not required, to adopt it". The statement says "must comply", which the passage directly contradicts. This distinction - mandatory for internal teams, voluntary for arm's-length bodies - is exactly the kind of scope clause a head of profession reads carefully before claiming organisation-wide compliance in a board paper.

#### Question 3 (moderate)

Statement: "A routine (non-emergency) change that passes the automated test suite may be deployed to production without peer review if the data protection team approves it."

**Correct answer: False.**

**Explanation:** For routine changes the passage imposes two cumulative conditions: passing the automated test suite **and** peer review by a non-author engineer. Data protection approval is an **additional** requirement for code reading personal data - the word "additionally" signals it stacks on top of, rather than substitutes for, the base requirements. No provision allows any approval to waive peer review for routine changes; only the emergency route defers it. The statement contradicts the standard, so it is False rather than Cannot Say.

#### Question 4 (moderate)

Statement: "The head of analytics engineering personally reviews emergency fixes."

**Correct answer: Cannot Say.**

**Explanation:** The passage requires that the head be **notified** before an emergency deployment and that a retrospective **review** occur within two working days - but it never says who performs that review. It might be the head; it might be any non-author engineer, consistent with the routine rule. The passage neither supports nor contradicts the statement, so the disciplined answer is Cannot Say. Candidates who know that in their organisation the head does review such fixes must leave that knowledge at the door: the test asks what this text establishes.

#### Passage B - Email from a director (Questions 5-7)

*"Thank you for the proposal to rebuild the workforce data model. I can see the case for improved grain and conformed dimensions. However, I am not able to release funding this quarter, as the directorate's discretionary budget is committed to the legislative programme. If the rebuild can be shown to reduce the manual reporting burden on my analysts by at least 20%, I would be willing to sponsor a bid in the next allocation round. In the meantime, my team will continue to rely on the current model, and I would ask that no breaking changes are made to it without consulting us."*

#### Question 5 (easy)

Statement: "The director has agreed to fund the rebuild in the next allocation round."

**Correct answer: False.**

**Explanation:** The director's commitment is doubly qualified: funding this quarter is refused outright, and the future offer is to "sponsor a bid" (not to fund), conditional on the rebuild being "shown to reduce the manual reporting burden... by at least 20%". A sponsored bid can still fail at allocation. The statement asserts an agreement to fund, which overstates the text on both counts - a misreading that, in real life, would surface painfully at the next allocation round. Reading commitments at their exact strength is core to managing stakeholder expectations.

#### Question 6 (moderate)

Statement: "The director's analysts currently spend some of their time on manual reporting."

**Correct answer: True.**

**Explanation:** The condition "reduce the manual reporting burden on my analysts by at least 20%" presupposes an existing manual reporting burden - you cannot reduce what does not exist. This is a supported inference, not an assumption: the passage's own wording entails it. Contrast this with facts the passage merely suggests (for example, that the current model causes the burden), which would be Cannot Say. Verbal reasoning at senior level frequently turns on this line between what wording entails and what it merely invites you to suppose.

#### Question 7 (moderate)

Statement: "The director has forbidden any changes to the current workforce model this quarter."

**Correct answer: False.**

**Explanation:** The request is narrower on both dimensions: it concerns **breaking** changes (not all changes) and asks that none be made **without consulting** the director's team (not that none be made at all). Non-breaking changes are unrestricted, and even breaking changes are permitted after consultation. The statement inflates a consultation condition on a subset of changes into a blanket prohibition. Spotting this kind of inflation matters when you brief your team: passing on the director's ask as "no changes allowed" would needlessly freeze legitimate work.

#### Passage C - Internal audit finding (Questions 8-10)

*"The audit examined ten data models selected from the production estate. Documentation for seven models met the organisation's published standard. For the remaining three, the data dictionary was incomplete, although in two cases the missing entries related to fields scheduled for deprecation. The audit found no evidence that incomplete documentation had caused analytical error. However, interviews indicated that analysts in two directorates were unaware of the metadata repository's existence. The audit recommends that the analytics engineering function strengthen its communication of the repository's role, and notes that responsibility for analyst training sits with directorate learning teams rather than with the analytics engineering function."*

#### Question 8 (moderate)

Statement: "Incomplete documentation caused analytical errors in three models."

**Correct answer: False.**

**Explanation:** The passage states the audit "found no evidence that incomplete documentation had caused analytical error". The statement asserts the opposite as fact. Be careful with a subtle temptation: "found no evidence that X" is not logically identical to "X did not happen" - but the statement here claims the audit's material **shows** errors occurred, which the text contradicts within its own scope. Against the passage, the assertion is False. If instead the statement had read "incomplete documentation has never caused analytical error anywhere in the organisation", the answer would be Cannot Say - absence of evidence in a ten-model sample does not establish organisation-wide absence. Holding that distinction steady under time pressure is precisely the precision this format measures, and precisely how you should read audit findings in the real job.

#### Question 9 (moderate)

Statement: "Fewer than half of the audited models failed the documentation standard."

**Correct answer: True.**

**Explanation:** Ten models were audited; seven met the standard; three did not. Three out of ten is fewer than half. The mitigating detail - that two of the three failures involved fields scheduled for deprecation - does not change the count of models falling short. Simple arithmetic embedded in prose is a staple of verbal tests: the trap is answering from impression ("mostly fine") rather than extracting and comparing the numbers.

#### Question 10 (challenging)

Statement: "The audit holds the analytics engineering function responsible for training analysts to use the metadata repository."

**Correct answer: False.**

**Explanation:** The final sentence explicitly "notes that responsibility for analyst training sits with directorate learning teams rather than with the analytics engineering function". The audit does recommend that the function "strengthen its communication of the repository's role" - communication, not training - and the passage carefully separates the two. A hurried reader merges the recommendation and the responsibility note into "we must train the analysts". Reading the division of responsibility exactly protects you from accepting accountability that the text assigns elsewhere - and equips you to respond to the audit with a communication plan (yours) while flagging the training gap to the learning teams (theirs). That is Metadata management's "communicate the value of metadata repositories" duty, correctly scoped.


#### Passage D - Vendor white paper extract (Questions 11-12)

*"Our metadata platform automatically harvests lineage from more than forty common transformation tools. Customers report that automated lineage reduces the time to diagnose data incidents. In a survey of 118 customers, 62% said incident diagnosis was 'faster' or 'much faster' after adoption. The platform requires read access to transformation code repositories. Where code is generated dynamically at runtime, lineage capture may be partial, and manual annotation is recommended to ensure completeness."*

#### Question 11 (moderate)

Statement: "A majority of surveyed customers reported faster incident diagnosis after adopting the platform."

**Correct answer: True.**

**Explanation:** 62% of the 118 surveyed customers chose "faster" or "much faster", and 62% is a majority. The statement stays carefully within the survey's scope ("surveyed customers", "reported") - it does not claim diagnosis actually was faster, or that the platform caused the improvement, either of which would exceed what a self-report survey establishes and push the answer towards Cannot Say. This is critical reading for horizon-scanning: your Data innovation duty means digesting vendor claims at exactly their evidential weight, no more and no less.

#### Question 12 (challenging)

Statement: "The platform captures complete lineage for all transformation code."

**Correct answer: False.**

**Explanation:** The final sentence concedes that "where code is generated dynamically at runtime, lineage capture may be partial" and recommends manual annotation "to ensure completeness". Completeness is therefore not guaranteed for all code; the statement's "all" is contradicted by the disclosed exception. Vendor documents typically place such qualifications in the final sentences, after the headline claims - a reading pattern worth internalising before you recommend a procurement. Note also what would trip a knowledgeable reader: your own experience of lineage tools is irrelevant; the passage itself supplies the contradiction.

#### Passage E - Draft communication to be reviewed (Questions 13-14)

You are reviewing a draft message your deputy intends to send to all data model users:

*"From 1 October, the legacy finance data mart will be decommissioned. All reports must be migrated to the new conformed finance model before this date. The analytics engineering team will run migration surgeries every Tuesday in September. Users who have not migrated by 1 October will lose access to financial reporting data. Field-level mappings from the legacy mart to the new model are available in the metadata repository."*

#### Question 13 (moderate)

Which of the following is a factual claim made by the draft that you should verify before it is sent?

A) That migration is desirable
B) That users who have not migrated by 1 October will lose access to financial reporting data
C) That the team prefers Tuesdays
D) That conformed models are better than legacy marts

**Correct answer: B.**

**Explanation:** Option B is the draft's strongest verifiable claim - and it is very likely an overstatement. Users will lose access to the **legacy mart**; but "financial reporting data" will remain available through the new conformed model. As written, the sentence could cause unnecessary alarm - or, worse, be technically false, undermining trust in your team's communications. Options A, C and D are matters of judgement, preference, or opinion rather than factual claims requiring verification. Reviewing communications for exactly this kind of overshoot is the everyday form of your Communicating between the technical and non-technical skill: at your level you are accountable for what the team broadcasts, and a single imprecise sentence to all users generates a week of support tickets - the passage-level equivalent of a failed data quality check.

#### Question 14 (challenging)

Statement (True / False / Cannot Say, from the draft's text alone): "Migration surgeries will be available after 1 October."

**Correct answer: Cannot Say.**

**Explanation:** The draft commits to surgeries "every Tuesday in September". It says nothing about October: it neither promises surgeries will continue nor states they will stop. Absence of a commitment is not a commitment of absence. The disciplined answer is Cannot Say - and the editorial insight for your review is that users will wonder exactly this, so the final message should state the position explicitly. Verbal reasoning practice and communication leadership converge here: the gaps a Cannot Say answer exposes in a passage are the gaps your readers will fall into if you publish it unamended.

#### Question 15 (challenging) - Summary selection

Return to Passage C (the audit finding). Which single sentence best summarises the audit's overall position?

A) The documentation regime has comprehensively failed and analysts cannot use the models
B) Documentation is largely compliant with no evidenced analytical harm, but awareness of the metadata repository is inconsistent and its communication should be strengthened
C) The analytics engineering function must take over analyst training from the directorates
D) Three models must be withdrawn from production immediately

**Correct answer: B.**

**Explanation:** Option B captures every element at its correct weight: seven of ten models compliant ("largely compliant"), no evidence of analytical error ("no evidenced analytical harm"), analyst unawareness in two directorates ("awareness... inconsistent"), and the sole recommendation ("communication should be strengthened"). Option A exaggerates the failures and invents an incapacity the passage never states. Option C reverses the passage's explicit assignment of training responsibility. Option D invents a remedy the audit never proposes. Summary questions reward proportionality - the best answer neither dramatises nor minimises - which is the same judgement you exercise when you condense a forty-page audit into three lines for an executive committee.

#### Passage F - Cross-government community proposal (Questions 16-17)

*"The proposed cross-government analytics engineering community would meet quarterly, rotate its chair among member organisations annually, and maintain a shared library of modelling patterns. Membership is open to any public body employing at least one analytics engineering professional. The steering group has agreed that shared patterns must be published under an open licence unless they reveal security-sensitive infrastructure detail. Organisations contributing patterns retain responsibility for maintaining them for two years or until a maintainer is found, whichever is sooner. The community will not mandate any specific toolset, although an annual survey of tools in use will be published."*

#### Question 16 (moderate)

Statement: "An organisation that contributes a pattern is responsible for maintaining it for at least two years."

**Correct answer: False.**

**Explanation:** The passage sets the obligation at "two years **or until a maintainer is found, whichever is sooner**". If a maintainer is found after six months, the contributor's responsibility ends then - so the commitment can be much shorter than two years. The statement's "at least two years" turns a capped obligation into a floor, reversing its direction. "Whichever is sooner" versus "whichever is later" clauses are tiny hinges that swing entire obligations; you will meet them constantly in memoranda of understanding when you represent your community to other organisations, and misreading one in a real agreement commits your team to years of unplanned support.

#### Question 17 (challenging)

Statement: "All shared patterns will be published under an open licence."

**Correct answer: False.**

**Explanation:** The steering group's rule contains an explicit exception: patterns are published openly "unless they reveal security-sensitive infrastructure detail". The word "all" in the statement collides with that carve-out, making the statement contradicted rather than merely unproven - so False, not Cannot Say. A useful test-taking heuristic follows: when a statement contains a universal quantifier ("all", "every", "always", "never"), scan the passage for an exception clause before anything else, because test writers plant one more often than not. The same reading habit serves your advocacy role: when you describe the community's rules to senior leadership or to other organisations, reproducing the exception accurately is the difference between a correct briefing and a commitment you cannot honour.

#### Question 18 (challenging) - Inference from Passage F

Statement: "An organisation employing no analytics engineering professionals could not join the community as a member."

**Correct answer: True.**

**Explanation:** The passage states membership "is open to any public body employing at least one analytics engineering professional". The condition is stated as the criterion of openness: a body employing none fails it, so membership is not open to them - the statement follows. Notice what would flip this to Cannot Say: if the passage had said membership "is open to" such bodies without the framing making the condition exhaustive, one might argue other routes could exist; but as written, the eligibility clause defines who may join, and test convention treats a stated eligibility criterion as the operative rule. Contrast this with a genuinely unsupported inference from the same passage - for instance, "most member organisations use the same toolset" would be Cannot Say, since the passage explicitly refuses to mandate tools and says nothing about what members actually use. Holding stated criteria, their contrapositives, and unstated possibilities in three separate mental buckets is the whole discipline of this format, and it is the same discipline you apply when deciding whether a draft standard's wording actually excludes the case you intend it to exclude - reviewing requirements and specifications, in your Testing skill's words, where an ambiguity you fail to catch becomes a loophole someone will one day stand in.

#### Question 19 (moderate) - Comprehension across Passage D

Which of the following best describes the relationship between the platform's automated lineage capability and manual annotation, as presented in Passage D?

A) Manual annotation replaces automated lineage for all customers
B) Manual annotation is a recommended supplement where dynamic code generation makes automated capture potentially incomplete
C) Manual annotation is required by the platform before automated harvesting can begin
D) The passage does not mention manual annotation

**Correct answer: B.**

**Explanation:** The passage's final sentence sets the relationship precisely: automated capture "may be partial" where code is generated dynamically at runtime, "and manual annotation is recommended to ensure completeness". Supplement, not replacement (eliminating A); recommended in a specific circumstance, not required as a precondition (eliminating C); and plainly mentioned (eliminating D). Multiple-choice comprehension items like this reward reconstructing the logical role each element plays in the passage's argument - here, a mitigation attached to a disclosed limitation - rather than merely spotting that the words appear. It is the reading you would do before a procurement recommendation: the question "under what conditions does the headline capability degrade, and what does the vendor expect us to do about it?" is answered in exactly one sentence of the text, and finding that sentence fast is the skill.

### Preparation tips

- **Practise the three-way discipline daily.** Take one paragraph from a real policy, standard, or email each day and write one True, one False, and one Cannot Say statement about it. Composing the statements teaches the boundaries faster than answering them.
- **Treat "Cannot Say" as a positive finding.** Senior professionals dislike saying "the text does not tell us" - it feels like weakness. In this format it is frequently the right answer, and in your role it is often the most valuable thing a reviewer can say about a draft.
- **Watch the quantifiers and modals.** "All", "some", "only", "must", "may", "should", "encouraged", "required" - the answer usually turns on one of these small words. Underline them (mentally or literally) on first read.
- **Read the statement first, then hunt the passage.** With under a minute per item, scanning for the statement's keywords beats re-reading the whole passage each time.
- **Do not import your expertise.** You know more about analytics engineering than any passage will. The test rewards suppressing that knowledge; treat each passage as the complete universe.
- **Rehearse with your real material.** Board papers, audit reports, and supplier documents are ideal practice texts - and the practice doubles as sharper reading of documents you must engage with anyway.

### Common pitfalls

- **Making assumptions from professional knowledge.** The most common senior failure: marking True because the statement is true in your organisation, when the passage never says it.
- **Confusing "likely" with "certain".** A passage that says an outcome is expected, recommended, or probable does not support a statement that it will happen.
- **Missing scope restrictions.** "In the ten models audited", "of surveyed customers", "this quarter" - statements that generalise beyond the stated scope shift from True to Cannot Say.
- **Inflating requests into prohibitions.** "Please consult us before breaking changes" is not "no changes allowed"; conditions and subsets matter.
- **Treating "no evidence of X" as "X is impossible".** Evidence claims have exact strength; so should your answers.
- **Poor time allocation.** Reading every passage exhaustively before seeing the questions burns the clock; and lingering on one agonising Cannot Say judgement costs you two easier items. Answer, flag, move.


## Workplace job-specific situational judgement assessment

### About this assessment

A workplace job-specific situational judgement assessment evaluates your decision-making, interpersonal skill, and professional conduct through realistic dilemmas drawn from your role. Unlike cognitive or numeric tests, there is rarely a single objectively right answer: several options may be defensible, and the scoring reflects how closely your choices align with the values and behaviours the organisation prizes. For UK public sector digital and data roles, those values are well signposted: put user needs first, work in the open and be transparent, collaborate across boundaries, build accessible and inclusive services, act with integrity as a steward of public money, and grow the people around you.

The common formats are: choose the **most effective** and **least effective** responses from a set of four or five; rank all responses from best to worst; or rate each response's effectiveness independently. Timing is usually generous or absent - the test measures judgement, not speed. At head-of-profession level the scenarios are strategic: they involve directors and boards, cross-organisational politics, team leadership under pressure, resource conflicts, and the tension between delivery deadlines and doing things properly. There is a consistent grammar to strong answers: they address the root issue rather than the symptom, act at the right moment rather than deferring indefinitely, keep stakeholders informed rather than managing them in the dark, and use the incident to strengthen systems and people rather than to assign blame.

Every scenario below is built from your actual duties: senior stakeholder relationships, strategic alignment of the team, standards enforcement, advocacy for the function, capability building, technology provision, data quality, and problem management.

### What it measures for your role

- **Senior stakeholder handling** maps to **build relationships with senior stakeholders across the organisation** and to **manage stakeholder expectations and moderate difficult discussions about high risk and complex topics, even within constrained timescales**.
- **Strategic alignment judgement** maps to **ensure the activities of the analytics engineering team align with strategic priorities** - including saying no well.
- **Standards leadership** maps to **ensure the team works to standards for communication, data models and documentation** and **advise on the application of standards and methods and ensure compliance** - enforcing without alienating.
- **Advocacy and representation** maps to **advocate for the analytics engineering role to senior leadership and other organisations** and **speak on behalf of, and represent the community to, large audiences**.
- **Capability building** maps to **build analytics engineering capability by providing technical leadership and career development** and **build problem-solving capabilities in others**.
- **Problem anticipation and integrity under pressure** maps to **Problem management**: anticipating problems, defending against them at the right time, and understanding how each fits the larger picture.

### Practice questions

For each scenario, decide your answer before reading the commentary. Where the format is most/least effective, commit to both choices.

#### Question 1 (moderate) - The director who wants it yesterday

A director you have been cultivating as an ally corners you after a board meeting: "I need a new performance data model for my area in three weeks - the minister has asked for a dashboard. Your team's roadmap says twelve weeks. Make it happen." Your team is fully committed to work aligned with published strategic priorities, and a rushed model would bypass your modelling and testing standards.

Options:

A) Agree to the three-week deadline; the ministerial connection makes it a de facto strategic priority, and you can quietly relax the standards this once.
B) Refuse, citing the roadmap, and suggest the director raise it at the next quarterly prioritisation board.
C) Explore what the minister actually needs: propose a rapid, clearly-labelled interim product (for example, a curated extract with documented caveats) inside three weeks, while scoping the proper model through the prioritisation route - and be explicit about what the interim product cannot support.
D) Accept the work but tell your team privately to deprioritise another directorate's committed work without informing that directorate.
E) Escalate immediately to your own director that you are being pressured inappropriately.

**Most effective: C. Least effective: D.**

**Explanation:** Option C does what strong senior judgement almost always does in these tests: it decomposes the demand (what does the minister actually need, by when, at what fidelity?), offers a safe partial yes, protects standards by labelling the interim product's limits honestly, and routes the full work through legitimate prioritisation - transparency, user focus, and stakeholder care all at once. It is also the answer that treats the three-week figure as a proxy for an underlying need rather than a specification, which is how skilled mediators between the technical and non-technical operate. Option D is the worst on every axis: it makes a secret commitment, breaks faith with another directorate, corrodes your team's trust, and hides a prioritisation decision that should be visible - the opposite of working in the open. Option A sacrifices standards invisibly, creating a precedent that every future deadline will invoke. Option B is procedurally correct but relationally clumsy: it treats a senior ally's urgent problem as someone else's queue ticket and spends the relationship capital you have built. Option E escalates before attempting resolution - escalation is a legitimate tool, but as a first move it signals you cannot handle senior stakeholders, which is precisely what your role exists to do.

#### Question 2 (moderate) - The silent data corruption

Your team discovers that for the past three weeks, the casework model has been under-counting queue ages due to a transformation defect your team introduced. The casework director has been reporting the flawed figures to the executive committee. The fix is ready. Nobody outside your team knows.

Options:

A) Deploy the fix quietly; the numbers will correct themselves and no one need know.
B) Inform the casework director immediately and personally: explain what was wrong, the period affected, the direction and rough size of the error, the fix, and what you are changing to prevent recurrence - and offer to help correct the record with the executive committee.
C) Send a broadcast email to all users noting a "minor data revision" without specifics.
D) Ask your engineers to check whether anyone actually made a decision based on the wrong figures before deciding whether to disclose.
E) Report it to the executive committee yourself before telling the casework director, to demonstrate transparency.

**Most effective: B. Least effective: A.**

**Explanation:** Option B is the integrity answer and the relationship answer simultaneously: the director has been unknowingly misinforming the executive committee, and they deserve to hear it from you, first, with everything they need to correct the record on their own terms. Adding the prevention story turns a failure into evidence of a well-run function - which, counterintuitively, is how advocacy credibility is actually built. Option A is concealment: public sector data feeds ministerial and executive decisions, and quiet correction leaves the director exposed to discovering the discrepancy later, from someone else - the worst outcome for trust. Option C is transparency theatre: technically disclosed, practically hidden. Option D inverts the ethics - whether harm resulted affects the remediation, not whether you disclose; and the check can proceed in parallel with disclosure. Option E gets transparency right but the route wrong: going over the director's head to their own committee ambushes the very stakeholder you owe the duty of candour to, and burns the relationship your role depends on. Sequence matters in stakeholder ethics: disclose to the person affected, then support wider correction.

#### Question 3 (moderate) - The standards rebel who delivers

Your most productive team lead consistently ships excellent, heavily-used data models - and consistently skips the documentation standard, arguing "the models speak for themselves and users want features, not paperwork". Two junior engineers have started copying this behaviour. An internal audit is six months away.

Options:

A) Publicly reprimand the team lead at the next community meeting so everyone sees the standard is serious.
B) Quietly document the models yourself after hours to keep the audit clean.
C) Meet the team lead privately: acknowledge their delivery record, make the case for why documentation is a user need too (future maintainers, analysts, and auditors are users), be explicit that the standard is not optional and that they are modelling behaviour for juniors - then agree a realistic remediation plan and check whether the standard itself needs streamlining given their feedback.
D) Remove the team lead from model development until they comply.
E) Wait for the audit to make the case for you.

**Most effective: C. Least effective: B.**

**Explanation:** Option C holds both truths at once: the person is valuable and the behaviour is unacceptable - and it treats the team lead as a professional by engaging their stated objection on its merits. Framing documentation as serving users (the analyst who must trust the model, the engineer who inherits it) recruits the team lead's own "users want features" logic rather than fighting it. Naming the influence on juniors addresses the real systemic risk - culture is set by what your best people are seen to get away with. Inviting critique of the standard keeps the door open to the possibility that compliance is low partly because the standard is heavier than it needs to be: standards leaders who never revise their standards breed rebels. Option B is the least effective despite feeling virtuous: it hides the problem, exhausts you, teaches the team lead nothing, leaves the juniors copying unchecked behaviour, and presents a false picture to audit. Option A humiliates a high performer in public - discipline in private, praise in public remains sound leadership. Option D is disproportionate as a first move and punishes delivery the organisation needs. Option E outsources your leadership to auditors and wastes six months of culture drift.


#### Question 4 (moderate) - The tool your engineers want

Your engineers are enthusiastic about a new open-source transformation framework and have started using it informally on one model, outside your approved toolset. It genuinely looks promising - your own horizon-scanning had flagged it. But nothing in your standards covers it, the security team has not assessed it, and one informal adopter has already hit an incident that took days to debug because nobody else knew the tool.

Options:

A) Ban it until further notice and require the informal work to be rebuilt with approved tools.
B) Legitimise the energy while containing the risk: set up a time-boxed, bounded evaluation - one non-critical model, security assessment initiated, evaluation criteria agreed, findings shared with the whole community - and make clear that production adoption follows the evaluation, not the other way round.
C) Approve it organisation-wide immediately; the engineers know best and innovation should not be slowed by process.
D) Allow the informal use to continue while you observe how it develops.
E) Ask the enthusiasts to write a paper on it for you to consider next quarter.

**Most effective: B. Least effective: D.**

**Explanation:** Option B is the textbook shape of governed innovation, and it maps directly onto two of your duties at once: "investigate emerging trends... and introduce innovative ways of working" and "ensure appropriate technology is available for the community" - available meaning assessed, supported, and standardised, not merely present. It converts unsanctioned energy into a structured pilot, brings security in early, and promises the community a shared answer rather than private knowledge - fixing exactly the failure mode the debugging incident exposed. Option D is the least effective because it is a decision to not decide while risk accumulates: the incident has already demonstrated the cost of unshared, unassessed tooling, and passive observation leaves production exposure growing with zero of the compensating structure B provides. Option A is defensible governance but wastes genuine promise your own horizon-scanning validated, and teaches engineers that initiative is punished - expect the next experiment to be better hidden. Option C abdicates the risk-owning half of your role. Option E performs diligence while actually deferring it: a quarter's delay with no security assessment started and informal use presumably continuing is slower and no safer than B.

#### Question 5 (challenging) - The conference platform and the criticism

You are representing the analytics engineering community at a cross-government conference. During your talk's question session, a well-known figure from another department states, publicly and with some heat, that your organisation's much-cited data model programme is "overhyped", claiming their team saw poor documentation and unreliable refreshes when they reused one of your published patterns.

Options:

A) Firmly rebut the criticism point by point, defending your team's reputation in front of the audience.
B) Acknowledge the specific experience without becoming defensive: thank them for the direct feedback, note that refresh reliability and documentation are exactly the areas your standards programme targets, offer to follow up bilaterally on the specific pattern - and do so, feeding what you learn back to your team and, where fair, publicly closing the loop.
C) Deflect with humour and move quickly to the next question.
D) Concede everything on stage and apologise on behalf of your organisation.
E) After the session, complain to the other department's leadership about their representative's unprofessional tone.

**Most effective: B. Least effective: E.**

**Explanation:** When you "speak on behalf of, and represent the community to, large audiences", the audience is scoring your composure and candour, not the debate points. Option B models exactly the culture you advocate: openness to challenge, seriousness about quality, and follow-through - and the bilateral follow-up frequently converts a public critic into a collaborator, which is what cross-government community building means in practice. Closing the loop publicly, where the facts allow, completes the transparency story. Option E is the least effective: it answers professional criticism with a political complaint, escalates a quality conversation into an inter-organisational grievance, and - if it becomes known, and such things become known - confirms the critic's narrative more damagingly than the original comment did. Option A wins the exchange and loses the room: heat against heat reads as fragility at senior level. Option C signals evasion on a substantive quality claim. Option D over-corrects: apologising for everything, before establishing facts, is neither honest nor fair to your team - the criticism might be partly wrong, and your team deserves a leader who finds out before conceding on a stage.

#### Question 6 (challenging) - Two directors, one team

The casework director and the finance director both demand your team's next available capacity: casework for backlog analytics (a published strategic priority), finance for a forecasting model the finance director says "the permanent secretary is interested in". You have capacity for one. Both directors are senior to you, both are copying escalating emails to your boss, and the finance director hints that future funding for your platform "depends on being seen to deliver for finance".

Options:

A) Split the team's capacity evenly between both, delivering both slowly.
B) Choose finance; platform funding is existential for the whole function.
C) Take the decision out of the bilateral crossfire: convene both directors (or take a short paper to the prioritisation forum) with a transparent options analysis - strategic alignment, urgency, delivery risk, and consequences of each sequencing - recommend the casework-first sequencing given the published priority, with a firm scheduled start for finance, and name the funding linkage openly as something to resolve on its own merits rather than through work allocation.
D) Choose casework and inform the finance director by email that their request is declined.
E) Ask your boss to decide.

**Most effective: C. Least effective: A.**

**Explanation:** Option C does the three things this situation demands. First, it moves a two-front lobbying war into a transparent forum where trade-offs are visible - the strongest defence against being personally squeezed, and the behaviour that keeps both relationships intact because the losing party can see the reasoning and has a firm start date rather than an open-ended no. Second, it anchors the recommendation to published strategic priorities, which is your role-level duty in one line. Third, it surfaces the funding hint - naming a lever neutralises it far more safely than either yielding to it (B) or pretending it was not said; resource decisions bought under funding pressure are exactly what transparency norms exist to prevent. Option A is the least effective: halving capacity across two urgent demands is the classic failure of splitting the baby - both deliverables arrive late, both directors stay dissatisfied, and your team context-switches its productivity away. It feels even-handed; it is actually the only option guaranteed to fail both stakeholders. Option D makes the defensible call indefensibly - a bare email refusal to a senior stakeholder manufactures an enemy. Option E delegates upward a judgement your role exists to make; your boss should receive your recommendation, not your dilemma.

#### Question 7 (challenging) - The struggling senior hire

Eight months ago you hired a senior engineer to lead the metadata repository programme - a cornerstone of your governance plans. They interview brilliantly and their technical knowledge is real, but delivery has stalled: milestones slip, the two engineers assigned to them seem disengaged, and one has quietly asked to move teams. The individual is from a group underrepresented in your profession, and you are conscious both of the additional scrutiny they may face and of your duty to build an inclusive community.

Options:

A) Reassign the programme to your strongest team lead and move the senior hire to lower-stakes work without discussion, avoiding a difficult conversation.
B) Hold a direct, private, supportive conversation: share the specific delivery and team-health observations, ask genuinely for their reading of the situation (there may be blockers you cannot see), jointly agree a support plan with clear expectations and check-ins - and separately make sure the assigned engineers are heard and supported.
C) Give it another six months; senior roles take time to bed in, and intervening now risks appearing discriminatory.
D) Ask the two assigned engineers to report on the senior hire's performance weekly.
E) Raise a formal capability procedure immediately to protect the programme.

**Most effective: B. Least effective: D.**

**Explanation:** Option B is what "providing technical leadership and career development" looks like when it is hard. Inclusion means giving every professional the same honest feedback, genuine curiosity about causes, and structured support you would give anyone - withholding candour from someone because of their background (option C's logic) is itself an inequity, and it lets a career problem compound while a cornerstone programme and two junior careers suffer. The two-sided structure of B matters: the senior hire gets specifics and agency; the assigned engineers get acknowledgement that their experience counts. Option D is the least effective: it converts the hire's own team into covert monitors, guaranteeing the trust needed to lead them can never form, poisoning three working relationships at once, and gathering data you already have - you know delivery has stalled; what you need is understanding and a plan. Option A avoids the conversation the person is owed and quietly writes off a senior hire without due process or dignity. Option E leaps to formal procedure before any informal support has been attempted - process as a substitute for leadership, and premature by any reasonable standard.

#### Question 8 (challenging) - The inherited estate and the new broom

You have just become head of analytics engineering. You discover that a well-loved, heavily-used dashboard maintained by a predecessor's favourite project is fed by an undocumented pipeline that breaches several current standards, runs on one engineer's personal scheduling scripts, and that engineer retires in four months.

Options:

A) Decommission the dashboard now; it is non-compliant and represents unacceptable key-person risk.
B) Commission the retiring engineer to spend a substantial part of their remaining time on structured knowledge transfer: pairing with two younger engineers to document the pipeline, migrate the scheduling to team-standard tooling, and bring the model under normal support - treating the four months as a closing window for capability transfer, and telling users what is happening and why.
C) Ask the retiring engineer to write documentation in their final week.
D) Do nothing until the retirement forces the issue; the dashboard works and you have bigger priorities.
E) Outsource the pipeline's support to a contractor after the engineer leaves.

**Most effective: B. Least effective: D.**

**Explanation:** This scenario is problem management in its purest form: "anticipate problems and defend against them at the right time" - and the right time is now, while the knowledge is still in the building. Option B converts a ticking key-person risk into a capability-building exercise (pairing spreads the knowledge to two people, not one document), a standards win (migration to team tooling), and a transparency win (users informed). It also honours the retiring engineer's craft rather than condemning it - the pipeline predates your standards, and a new head who leads with respect for inherited work builds more compliance than one who leads with condemnation. Option D is the least effective: the risk has a known, dated fuse, and choosing to wait is choosing the 3 a.m. failure after the only person who understands it has gone - with users who were never warned. Option A destroys user value that could be preserved and reads as new-broom zealotry - spending your first months' credibility on a demolition. Option C misunderstands knowledge transfer: a week of solo writing captures a fraction of four months of paired working, and untested documentation fails exactly when needed. Option E replaces key-person risk with more expensive key-contractor risk and forfeits the learning your own team could have gained.

#### Question 9 (challenging) - The data quality bad news before the big announcement

The organisation announces tomorrow a widely-trailed "single view of performance" built on your conformed models. Tonight, a routine profiling run surfaces that one source system has been sending stale data for five days: roughly 8% of tomorrow's headline figures are affected, most only marginally. The communications team says the announcement "cannot move". Your analysis suggests corrected data will be available in three days.

Options:

A) Say nothing; 8% marginally affected is within tolerance and the announcement is not your call.
B) Tell the senior owner of the announcement tonight, with a one-page factual summary: what is stale, the likely magnitude and direction of error in the headline figures, the three-day path to corrected data, and options (delay, annotate the affected figures, publish with a dated caveat and scheduled correction) - and let the accountable owner decide with full information.
C) Unilaterally pull your models from the product tonight to protect your team from association with bad data.
D) Tell the communications team to fix the wording but not trouble the senior owner.
E) Email a broad distribution list flagging "possible data issues" without quantification.

**Most effective: B. Least effective: C.**

**Explanation:** The principle is single-sentence simple: the accountable decision-maker must decide with full information, and your job is to make that possible tonight, in decision-ready form. Option B's shape is worth memorising for real life - what is wrong, how big, in which direction, when it will be fixed, and what the options are - because senior owners do not need your alarm, they need your analysis. Providing options rather than a single demand respects that publish-with-caveat may genuinely be the right call for marginal errors; transparency does not always mean delay, but it always means informed. Option C is the least effective: it takes a decision far above your authority, detonates the announcement without consultation, and prioritises your team's reputational shelter over the organisation's interests - the inverted priority order for a public servant. Option A gambles the organisation's credibility on your private tolerance judgement; discovery later ("they knew the night before") is a trust catastrophe. Option D fixes words, not the decision, and hides information from the accountable owner. Option E spreads unquantified alarm - noise without decision value, and the panic it causes is likely worse than the 8% marginal error it describes.

#### Question 10 (challenging) - Ranking: building the community's future

Budget season. You can fund exactly one of four proposals this year. The organisation's data strategy emphasises self-service analytics and reducing dependency on scarce specialist teams. Rank the four proposals from most to least aligned choice, given that strategy.

- Proposal W: A semantic layer and documentation overhaul making the twenty most-used models genuinely self-service for analysts, with training materials.
- Proposal X: A specialist rapid-response squad within your team to build bespoke datasets on demand for directorates.
- Proposal Y: Migration of all pipelines to a newer orchestration tool, delivering engineer-facing improvements with no user-visible change.
- Proposal Z: A prestigious annual analytics engineering conference hosted by your organisation.

**Most aligned ranking: W, Y, X, Z.**

**Explanation:** Work from the strategy's own words: self-service and reduced dependency on specialists. Proposal W is the strategy made concrete - it directly converts specialist-dependent models into self-service assets, multiplies the value of the estate you already own, and its training component builds capability outside your team, which is dependency reduction at the root. Proposal Y comes second: invisible infrastructure work is easy to undervalue, but reliability and maintainability are preconditions for self-service trust - an unreliable self-service layer teaches analysts to go back to asking specialists. It serves the strategy indirectly but genuinely. Proposal X comes third, and the reasoning is the important part: a bespoke-datasets-on-demand squad is attractive, popular with directorates, and precisely counter-strategic - it deepens dependency on your specialists and teaches the organisation that the path to data is a ticket to your team. In a ranking format, spotting the seductive counter-strategic option is usually where the marks are. Proposal Z is last, not because advocacy is worthless - it is one of your duties - but because as the single funded item it delivers profile without capability; it is the garnish, not the meal. Note the meta-skill: every ranking justification above argues from the stated strategy, not from personal preference - exactly how you should defend prioritisation decisions to your board.

### Preparation tips

- **Anchor on public sector values, not corporate instinct.** Where a private-sector answer might prize decisive unilateral action, UK public sector scoring rewards transparency, informed accountable decision-making, collaboration across boundaries, and user focus. Re-read the Civil Service values and the government service standard the week before your assessment.
- **Look for the root-cause option.** In almost every scenario, one option treats the symptom, one defers, one over-escalates, and one addresses the underlying issue while preserving relationships. Train yourself to spot that fourth shape quickly.
- **"Least effective" deserves equal care.** Candidates lose marks by finding the best option and guessing the worst. The least effective option is usually the one that is secretive, passive in the face of accumulating risk, or destructive of a key relationship - not merely the clumsiest.
- **Beware the seductive wrong answer.** Test writers include options that feel strong - decisive bans, dramatic escalations, self-sacrificing quiet fixes. Ask of each option: what does this teach people, and what does it look like when it becomes known?
- **Practise narrating your reasoning.** After each practice question, explain your choice aloud in two sentences referencing a value or duty. If you cannot, your choice was instinct, not judgement - fine until the interview panel asks you to justify it.
- **Draw on your real incidents.** You have lived versions of most of these dilemmas. For each, recall what you did, what happened, and what you would repeat or change - the assessment rewards the judgement that reflection builds.

### Common pitfalls

- **Answering idealistically instead of effectively.** "Convene a working group to co-design a solution" sounds collaborative but scores poorly when the scenario demands action tonight. Effectiveness includes timeliness.
- **Selecting passive options.** Waiting, observing, deferring to the next quarterly board, or asking someone else to decide are consistently among the lowest-scoring choices when risk is live and the decision sits in your role.
- **Over-escalating.** Escalation as a first resort signals inability to operate at your level; escalation with a recommendation, after attempting resolution, is the senior pattern.
- **Protecting your team's image over the organisation's interests.** Options that hide, spin, or unilaterally withdraw to avoid association with a problem score badly against transparency and stewardship values.
- **Ignoring what options teach observers.** At head-of level every visible decision is a lesson to your community - about standards, initiative, candour, and fairness. Options that resolve today's problem while teaching tomorrow's bad lesson are traps.
- **Forgetting the relationship after the decision.** The best options routinely include informing the affected party, offering a path forward, or closing the loop. A right call delivered as a bare refusal is scored as a weaker answer - and works out that way in real life too.

## Conclusion

You have now worked through four substantial assessment types - cognitive, numeric, verbal, and situational judgement - every one of them grounded in the real work of leading analytics engineering in a UK public sector organisation: the models and pipelines your team runs, the standards you steward, the budgets you defend, the audits you answer, and the directors, engineers, and cross-government communities whose trust you hold.

A few closing thoughts. First, be encouraged: nothing in these assessments is alien to you. Pattern recognition across incidents, weighted averages in a coverage report, the exact force of "encouraged but not required", the right way to deliver bad news before a big announcement - these are things you already do. Psychometric preparation, at your level, is mostly about translating lived competence into the compressed, timed, multiple-choice grammar of a test. Familiarity with the format is the cheapest performance gain available, and you have just bought a good deal of it.

Second, let the practice double as professional development. Where a cognitive question felt slippery, there may be a diagnostic habit worth sharpening. Where a numeric item slowed you, ten minutes a day with your own management information will pay off in board meetings as well as tests. Where a situational judgement commentary surprised you, that is worth a reflective conversation with a mentor or a peer head of profession. The questions were built from your duties precisely so that every weakness they expose is a development area your role rewards you for closing.

Third, prepare kindly and practically: sleep, a quiet room, a working calculator, a glass of water, and the discipline of flagging hard questions and moving on. Under time pressure, calm process beats brilliance.

Finally, remember why organisations assess: to make fair, evidence-based decisions about capability. That is the same principle you champion every day when you insist decisions be made on well-modelled, well-documented, trustworthy data. Walk into the assessment as what you are - a senior professional who builds the evidence base for good decisions - and let the preparation you have done here speak. Good luck, and keep investing in yourself; your community is watching how its leaders grow, and learning from it.

