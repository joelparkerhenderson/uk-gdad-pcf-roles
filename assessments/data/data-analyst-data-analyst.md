# Data Analyst - Psychometric Assessment Resources

## Introduction

Welcome! This guide has been created especially for you as a data analyst working within the UK Government Digital and Data profession. Whether you are preparing for an internal assessment, applying for a new post, or simply looking to sharpen the mental skills that underpin your day-to-day work, this document will help you practise, reflect, and build confidence.

Psychometric assessments are structured, standardised exercises that measure the thinking skills a role genuinely requires. They are widely used across the Civil Service and the wider public sector because they are fair, evidence-based, and focused on what you can do rather than where you came from. For a data analyst, that means assessments built around the things you actually handle every day: datasets that need cleansing, dashboards that need interpreting, stakeholder emails that need careful reading, quality assurance standards that need applying, and judgement calls about data ethics, privacy, and competing priorities.

This document is organised into four practice assessments, each tailored to your role:

1. **Workplace job-specific cognitive assessment** - pattern recognition, logical deduction, error checking, and prioritisation using the artefacts a data analyst really works with, such as data pipelines, lookup tables, and validation rules.
2. **Workplace job-specific numeric reasoning assessment** - percentages, ratios, rates, and performance metrics drawn from realistic public sector datasets, service dashboards, and project figures.
3. **Workplace job-specific verbal reasoning assessment** - dense passages based on data governance policies, accessibility standards, stakeholder emails, and analytical reports, followed by True / False / Cannot Say and comprehension questions.
4. **Workplace job-specific situational judgement assessment** - workplace dilemmas involving the stakeholders you really encounter: product managers, user researchers, policy colleagues, data engineers, and members of the public whose data you steward.

Each section explains what the assessment measures, maps it to the specific skills in your role profile, provides a substantial set of practice questions with full worked explanations, and finishes with preparation tips and common pitfalls to avoid.

How should you use this guide? Work through it at your own pace. Try each question honestly before reading the answer, and pay as much attention to the explanations as to whether you got the question right - the reasoning is where the learning happens. Revisit sections that feel harder; that is a signal of where practice will pay off most. Treat the whole document as a friendly training ground, not a judgement. Every analyst, at every level, can improve these skills with deliberate practice - and the fact that you are here, preparing thoughtfully, is already a great sign.

Good luck, and enjoy the practice!

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive assessment measures the core mental processes your role demands: spotting patterns in data, deducing logical conclusions from rules, checking for errors quickly and accurately, prioritising competing tasks, and solving practical problems. Unlike a generic IQ test, every question is built from the everyday artefacts of a data analyst's work - extracts, lookup tables, validation rules, pipeline schedules, and dashboard figures - so it predicts how you will perform on the job, not in the abstract.

These assessments are typically delivered online, timed at around 15 to 30 minutes, and scored objectively against a benchmark group. You will usually get a few ungraded practice questions first so you can get comfortable with the interface. Some modern platforms are adaptive, meaning the questions get harder or easier depending on how you are doing - so do not panic if the questions feel like they are getting tougher; that often means you are doing well. Employers generally receive a breakdown of speed versus accuracy rather than a single score, so working carefully matters as much as working quickly.

For a data analyst, cognitive ability is not an optional extra - it is the engine behind reliable analysis. Spotting a subtly wrong join, noticing that a monthly series has a suspicious gap, or deducing which of three data sources is authoritative are all cognitive tasks you perform daily, often under time pressure.

### What it measures for your role

Each cognitive dimension maps directly onto the skills in your role profile:

- **Pattern recognition** supports your skill in **Applying statistical and analytical tools and techniques** - contributing to statistical insights depends on noticing trends, seasonality, and anomalies before you formalise them.
- **Error checking** underpins **Data preparation and linkage** - identifying and resolving data quality issues, and preparing and cleansing data so it is fit for purpose, is fundamentally an error-detection discipline. It also supports your commitment to follow and apply quality assurance standards.
- **Logical deduction** supports **Developing code for analysis** - designing the analytical approach and code needed to address research questions requires you to reason precisely about conditions, dependencies, and edge cases, and to understand why testing code matters.
- **Prioritisation** maps to **Managing a data project** - contributing to project planning and adapting your ways of working to deliver different outcomes means constantly judging which task matters most right now.
- **Problem solving** connects to **Delivering business impact through data** - identifying the data needed to address business requirements is a problem-solving exercise: working out what is missing, what is possible, and what will genuinely enable decision making.
- Careful reasoning about rules also supports **Data management** and **Data ethics and privacy** - following organisational data governance policies on access, sharing, and protection requires you to apply written rules to concrete cases accurately.

### Practice questions

**Question 1 (easy) - Pattern recognition.** Your team assigns dataset reference codes in a fixed sequence. The last five codes issued were: DA-2041, DA-2044, DA-2047, DA-2050, DA-2053. A colleague asks you to reserve the next two codes for a new pipeline. Which codes should you reserve?

- A) DA-2054 and DA-2055
- B) DA-2056 and DA-2059
- C) DA-2055 and DA-2057
- D) DA-2056 and DA-2058

**Correct answer: B.** **Explanation:** The sequence increases by 3 each time (2041, 2044, 2047, 2050, 2053). The next code is 2053 + 3 = 2056, and the one after is 2056 + 3 = 2059. Option A assumes the codes increment by 1, which ignores the established pattern. Options C and D use the wrong step size. In real work, spotting the rule behind an identifier sequence stops you creating clashing references that break downstream joins.

**Question 2 (easy) - Error checking.** You are quality assuring a data extract against its source system. The source record reads: "Case 10482 | Opened 03/02/2026 | Region: North East | Status: Closed". The extract row reads: "Case 10482 | Opened 03/02/2026 | Region: North West | Status: Closed". Which field contains a transcription error?

- A) Case number
- B) Opened date
- C) Region
- D) Status

**Correct answer: C.** **Explanation:** The region has changed from "North East" in the source to "North West" in the extract; the other three fields match exactly. This is the classic error-checking format: comparing two versions of the same record character by character. In your role this mirrors validating that a pipeline has moved data between systems without corruption - one of your core duties of identifying, collecting and moving data between a range of systems. A single-letter or single-word slip like this can silently misallocate cases to the wrong regional team, so precision matters.

**Question 3 (moderate) - Logical deduction.** Your pipeline documentation states four rules: (1) The cleansing job must run after the ingestion job. (2) The linkage job must run after the cleansing job. (3) The publication job must run last. (4) The validation job must run immediately after the linkage job. In what order must the five jobs run?

- A) Ingestion, cleansing, linkage, validation, publication
- B) Ingestion, linkage, cleansing, validation, publication
- C) Cleansing, ingestion, linkage, validation, publication
- D) Ingestion, cleansing, validation, linkage, publication

**Correct answer: A.** **Explanation:** Rule 1 puts ingestion before cleansing; rule 2 puts cleansing before linkage; rule 4 places validation immediately after linkage; rule 3 places publication at the end. Chaining these gives ingestion → cleansing → linkage → validation → publication. Option B breaks rule 1 and 2's chain by running linkage before cleansing. Option C runs cleansing before ingestion, violating rule 1. Option D separates validation from its required position immediately after linkage. Reasoning through dependency chains like this is exactly what you do when you help ensure new and existing data models and pipelines can be reused or reproduced.

**Question 4 (moderate) - Logical deduction with validation rules.** Your team's data quality standard says: "A record is valid only if it has a non-blank NHS-style identifier AND a date of birth. If a record is valid, it enters the linkage stage. Records that enter the linkage stage are never deleted." A colleague tells you record R was deleted. What can you logically conclude?

- A) Record R had a blank identifier
- B) Record R was not valid
- C) Record R had no date of birth
- D) Record R entered the linkage stage

**Correct answer: B.** **Explanation:** Records entering linkage are never deleted, so a deleted record cannot have entered linkage. All valid records enter linkage, so record R cannot have been valid. That is all we can conclude. We cannot say *which* validity condition failed - it might have been the identifier, the date of birth, or both - so options A and C go beyond the evidence. Option D contradicts the rules. This is the discipline of deducing only what the rules strictly entail, which protects you from over-claiming when you respond to stakeholder questions about analytical techniques and data quality.

**Question 5 (moderate) - Prioritisation.** It is 09:15 on Monday. Four items are in front of you: (1) A dashboard used in a 10:00 ministerial briefing is showing yesterday's date stamp and may not have refreshed. (2) A user researcher has asked for a dataset by Thursday. (3) Your weekly data quality report is due at 17:00 today. (4) A colleague has asked you to review their analysis code "when you get a chance". What should you do first?

- A) Start the weekly data quality report because it is due today
- B) Check whether the ministerial briefing dashboard has refreshed correctly
- C) Send the user researcher the dataset
- D) Review your colleague's code since it will only take a few minutes

**Correct answer: B.** **Explanation:** Prioritisation combines urgency and impact. The dashboard feeds a 10:00 ministerial briefing - 45 minutes away - and may be showing stale data, which could lead to decisions based on wrong figures. That is both the most urgent and the highest-impact item. The quality report (option A) is due today but has hours of slack. The Thursday dataset (option C) has days of slack. The code review (option D) has no stated deadline at all. A quick diagnostic on the dashboard, followed by escalation if needed, protects the organisation's credibility - a direct expression of delivering business impact through data.

**Question 6 (moderate) - Pattern recognition in a data series.** A monthly count of completed applications reads: January 4,120; February 4,090; March 4,150; April 4,135; May 412; June 4,180. As the analyst preparing this data, what is the most likely explanation for the May figure?

- A) Demand genuinely collapsed in May
- B) A data entry or load error dropped a digit, and May should be around 4,120
- C) The June figure is wrong, not the May figure
- D) The series is seasonal and May is always low

**Correct answer: B.** **Explanation:** Every other month sits in a narrow band between 4,090 and 4,180, while May shows 412 - almost exactly one tenth of the neighbouring values. The most plausible pattern-based hypothesis is a dropped trailing digit (412 instead of, say, 4,12X) or a truncated load. Option A is possible in principle but a 90% collapse with instant recovery in June is far less likely than a data defect, and a good analyst investigates before believing it. Option C has no supporting evidence - June fits the band. Option D is unsupported: nothing in one year of data establishes seasonality, and a genuine seasonal dip would rarely be a factor of ten. The professional response is to flag and investigate the anomaly before publishing - identifying and resolving data quality issues is a named behaviour in your Data preparation and linkage skill.

**Question 7 (moderate) - Diagnosing a join.** You join a table of 5,000 unique service users to a table of local authority reference data using postcode. The result contains 5,430 rows. Which explanation is most consistent with this outcome?

- A) 430 service users were dropped because their postcodes did not match
- B) Some postcodes appear more than once in the reference table, duplicating matching users
- C) The join key was case-sensitive and failed for all rows
- D) The service user table contained blank rows that were removed by the join

**Correct answer: B.** **Explanation:** A one-to-many relationship on the join key is the classic cause of a row count *increasing* after a join: each service user whose postcode appears twice in the reference table generates two output rows. Option A describes rows being lost, which would produce *fewer* than 5,000 rows, not more. Option C would produce dramatically fewer matches, not extra rows. Option D would also reduce, not increase, the count. The practical habit here - compare row counts before and after every join, and investigate any change you cannot explain - is one of the highest-value quality assurance checks in data preparation and linkage, and it is exactly the kind of reasoning a cognitive assessment probes.

**Question 8 (moderate) - Error checking a lookup table.** You maintain a lookup table mapping region codes to region names. Review these five rows and identify the inconsistency: (1) NE → North East, (2) NW → North West, (3) YH → Yorkshire and The Humber, (4) EM → East Midlands, (5) WM → West Midland.

- A) Row 1
- B) Row 3
- C) Row 5
- D) There is no inconsistency

**Correct answer: C.** **Explanation:** Row 5 reads "West Midland" - missing the final "s" of the standard name "West Midlands". Rows 1 to 4 all follow the official region naming used in UK statistical geographies. A missing character in a lookup table is dangerous precisely because it looks almost right: any downstream join or filter on the exact string "West Midlands" will silently exclude those records. Cognitive error-checking questions test whether you slow down enough to verify each row rather than pattern-matching on the general shape. In your role this is the daily reality of using appropriate data management tools, procedures and methods, where reference data must be exactly right, not approximately right.

**Question 9 (moderate) - Deduction about access rules.** Your data governance policy states: "All analysts may access the anonymised dataset. Only analysts who have completed information governance training may access the identifiable dataset. No one may share the identifiable dataset outside the team." Priya is an analyst who has not completed information governance training. Which statement must be true?

- A) Priya may not access the anonymised dataset
- B) Priya may access the identifiable dataset once her manager approves
- C) Priya may access the anonymised dataset but not the identifiable dataset
- D) Priya may share the anonymised dataset outside the team

**Correct answer: C.** **Explanation:** The first rule grants all analysts - including Priya - access to the anonymised dataset. The second rule restricts the identifiable dataset to those who have completed training, which Priya has not, so she is excluded. Option A contradicts the first rule. Option B invents a manager-approval route that appears nowhere in the policy - a classic trap of importing outside assumptions. Option D goes beyond the text: the policy prohibits sharing the identifiable dataset externally but says nothing either way about sharing the anonymised one, so we cannot conclude she *may*. Applying access rules exactly as written, without adding or dropping conditions, is central to your Data management and Data ethics and privacy skills.

**Question 10 (hard) - Scheduling under constraints.** You must schedule three pipeline jobs on a shared server tonight. Job X takes 2 hours and must finish before 02:00. Job Y takes 3 hours and cannot start until Job X finishes. Job Z takes 1 hour, can run at any time, but cannot run at the same time as Job Y because both are memory-intensive. The server window opens at 22:00. Only one memory-intensive job can run at a time, but Job X can overlap with either. What is the earliest all three jobs can finish?

- A) 03:00
- B) 04:00
- C) 05:00
- D) 06:00

**Correct answer: A.** **Explanation:** Start Job X at 22:00; it finishes at 00:00, meeting its 02:00 deadline. Job Z can overlap with X, so run Z from 22:00 to 23:00. Job Y must wait for X, so it runs 00:00 to 03:00. Since Z finished at 23:00, the Y-Z conflict never arises. Everything completes by 03:00. Option B reflects running Z after Y unnecessarily, and options C and D reflect running all three jobs one after another. The insight is to exploit permitted parallelism: only the Y-Z pair conflicts, so schedule Z early alongside X. This mirrors real pipeline planning in your role, where understanding which processes can safely overlap is part of contributing to the planning of the data project life cycle.

**Question 11 (hard) - Deduction about code review.** Your team's development standard says: "Analysis code may be merged only if it has been peer reviewed. Code that includes automated tests is always approved by reviewers within one day. Code without automated tests is sometimes rejected." Your script was merged this morning. Which conclusion is logically safe?

- A) Your script included automated tests
- B) Your script was peer reviewed
- C) Your script was approved within one day
- D) Your script was never rejected in any earlier review round

**Correct answer: B.** **Explanation:** Merging requires peer review, so a merged script must have been reviewed - option B follows necessarily. Option A does not follow: code without tests is only *sometimes* rejected, which means it is sometimes approved, so a merged script might lack tests. Option C depends on the script having tests, which we cannot establish. Option D over-reaches: the rules say nothing about earlier rounds; a script could be rejected once, revised, and merged later. This question rewards the discipline of separating what *must* be true from what *might* be true - the same discipline you apply when you review and improve analytical approaches under supervision and explain the importance of testing code, both named behaviours in your Developing code for analysis skill.

**Question 12 (hard) - Problem solving a dashboard discrepancy.** Your published dashboard shows 12,400 completed transactions for July. The finance team's independent report shows 11,900 for the same month. You investigate and find: (i) your pipeline counts a transaction on the date it was *started*; (ii) finance counts it on the date payment *cleared*; (iii) payments typically clear 2 to 3 days after a transaction starts; (iv) July transaction volumes were rising week on week through the month. Which explanation best accounts for the 500-transaction gap?

- A) One of the two systems has lost 500 records and must be repaired
- B) Transactions started in late July cleared in early August, so finance's July count excludes them, and rising volumes make this end-of-month effect larger
- C) The finance team made an arithmetic error
- D) Duplicate transactions inflated your dashboard by exactly 500

**Correct answer: B.** **Explanation:** The two counts use different counting rules: start date versus cleared date. Transactions started in the final two or three days of July would clear in August, appearing in your July figure but not finance's. Because volumes were rising through the month, the final days of July carried more transactions than average, plausibly explaining a gap of around 500 without any data loss at all. Options A, C and D all assume a defect, but the evidence points to a definitional difference - the most common cause of "discrepancies" between well-run systems. The professional lesson: before declaring data wrong, check whether the two sources are measuring the same thing the same way. Explaining this distinction clearly to finance colleagues is a perfect example of communicating between the technical and non-technical.

**Question 13 (moderate) - Pattern recognition in file naming.** Your team's published extract files follow a naming convention. Recent files include: `svc_extract_2026Q1_v2_final.csv`, `svc_extract_2026Q2_v1_final.csv`, `svc_extract_2026Q3_v3_final.csv`. A colleague uploads `svc_extract_Q4_2026_v1_final.csv` for publication. What should you flag?

- A) Nothing - the file follows the convention
- B) The version number is wrong
- C) The quarter and year are in the wrong order compared with the established convention
- D) The file extension should be .xlsx

**Correct answer: C.** **Explanation:** The established pattern places the year before the quarter with no separator between them: `2026Q1`, `2026Q2`, `2026Q3`. The new file reverses this to `Q4_2026` and adds an underscore. Version numbers legitimately vary (v1, v2, v3 all appear in the history), so option B is wrong, and nothing suggests a format change (option D). This matters practically: automated pipelines and sorted directory listings depend on consistent naming, and a file that breaks the convention may be missed by a scheduled loader or sort out of chronological order. Enforcing conventions like this is a small but real part of ensuring pipelines can be reused and reproduced, and of following your team's data management procedures.

**Question 14 (hard) - Multi-condition filtering logic.** Your extract script applies these filters in order: (1) keep records where status is "Active" OR "Pending"; (2) then remove records where the last-updated date is more than 24 months old; (3) then keep only records with a valid postcode. You start with 10,000 records: 6,000 are Active, 2,500 are Pending, 1,500 are Closed. Of the 8,500 Active-or-Pending records, 500 are more than 24 months old. Of the records remaining after step 2, 5% have an invalid postcode. How many records survive all three filters?

- A) 8,500
- B) 8,000
- C) 7,600
- D) 7,225

**Correct answer: C.** **Explanation:** Step 1 keeps Active + Pending: 6,000 + 2,500 = 8,500 (the 1,500 Closed records drop). Step 2 removes the 500 stale records: 8,500 − 500 = 8,000. Step 3 removes the 5% with invalid postcodes: 8,000 × 0.05 = 400 removed, leaving 8,000 − 400 = 7,600. Options A and B are the intermediate counts after steps 1 and 2 - a reminder that multi-stage questions plant your own running totals as distractors. Option D applies the 5% to the wrong base. Tracing record counts through a filter chain, and being able to account for every excluded record, is precisely the reasoning you use when documenting an analytical approach and answering the inevitable stakeholder question: "why does your figure differ from the raw count?"

**Question 15 (moderate) - Prioritising a bug triage.** Overnight, four automated alerts arrived from your data pipelines: (1) the ingestion job for a decommissioned legacy feed failed - this feed was switched off last month and the alert was due for removal; (2) the nightly refresh of the team's internal exploratory sandbox failed; (3) row counts on the published statistics pipeline came in 40% below the seasonal norm, though the job itself reported success; (4) a disk usage warning shows the archive server at 82% capacity, rising about 1% per week. In what order should you investigate?

- A) 1, 2, 3, 4
- B) 3, 2, 4, 1
- C) 4, 3, 2, 1
- D) 3, 4, 2, 1

**Correct answer: B.** **Explanation:** Alert 3 is the standout priority: a "successful" run with a 40% row shortfall means the published statistics pipeline may silently be producing wrong outputs - silent partial failures are more dangerous than loud complete ones, because nothing else will stop the bad data reaching users. Alert 2 comes next: a genuine failure affecting colleagues' working environment today, though internal-only. Alert 4 is real but slow-moving - at 1% per week there are months of headroom, so it becomes a planned task, not an investigation. Alert 1 requires no investigation at all: the "failure" is expected because the feed no longer exists; the right action is tidying up the alert, last. Option D wrongly ranks the slow capacity issue above a same-day failure affecting colleagues. The general principle - triage by impact on users and by silence of the failure, not by how alarming the alert sounds - is core to keeping data products trustworthy.

### Preparation tips

- **Practise with your own artefacts.** Take a real (non-sensitive) extract from your work and set yourself mini-exercises: predict the row count after a join, scan a lookup table for inconsistencies, or trace a pipeline's dependency order. The assessment format will feel familiar because it *is* your job in miniature.
- **Build a checking rhythm.** For error-checking items, compare field by field in a fixed order rather than eyeballing the whole record. Consistency beats speed - and your speed will rise naturally with repetition.
- **Verbalise deductions.** For logic questions, say the chain out loud or jot it down: "X before Y, Y before Z, so X before Z." Externalising the chain prevents the mental slips that happen when you hold four rules in your head at once.
- **Time-box every question.** In a 20-minute test with 20 questions, no single item deserves more than about 90 seconds. Flag and move on; return if time allows.
- **Rest and set up properly.** Do the assessment somewhere quiet, on a reliable connection, with rough paper ready. A calm environment is worth several points.

### Common pitfalls

- **Pattern-matching on shape instead of substance.** Under time pressure it is tempting to see "West Midland" and read "West Midlands". Assessments deliberately include near-misses; slow down on verification items.
- **Importing outside knowledge into logic questions.** If the rules given do not mention manager approval, there is no manager approval - even if your real organisation has one. Answer strictly from the information provided.
- **Over-calculating when estimation suffices.** Some problems, like the dashboard discrepancy, are solved by reasoning about definitions, not arithmetic. Ask "what kind of problem is this?" before diving in.
- **Getting stuck on one hard question.** A single time-sink item can cost you three easier questions. Skipping strategically is a skill, not a failure.
- **Ignoring the speed-accuracy report.** Because employers often see accuracy and speed separately, a rushed, error-strewn attempt looks worse than a slightly slower, careful one. Aim for controlled pace.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment evaluates your ability to analyse, interpret, and make sound decisions using numerical data. It deliberately mimics the data-handling demands of your role: tables of service metrics, budget figures, capacity numbers, percentages, ratios, and performance dashboards - business maths, not abstract formulae. Most assessments allow or provide an onscreen calculator, because they prioritise interpretation over mental arithmetic, but they run to a strict time limit, so quick and accurate data extraction matters.

For a data analyst this assessment is close to a rehearsal of the day job. You already compute percentage changes for performance reports, check that published figures reconcile, size datasets against storage and processing capacity, and translate raw counts into rates that stakeholders can compare fairly. The assessment simply packages those tasks into timed questions. Expect question inputs in the form of small tables, charts described in text, and short scenarios, with four or five answer options each. Watch carefully for scale qualifiers such as "in thousands", for the difference between percentages and percentage points, and for questions where estimation gets you to the answer faster than exact calculation.

### What it measures for your role

- **Percentages, rates and ratios** map directly to **Applying statistical and analytical tools and techniques** - contributing to statistical insights and reports means being fluent in exactly these operations, and being able to explain them when you respond to stakeholder questions.
- **Table interpretation and cross-comparison** supports **Data visualisation** and **Delivering business impact through data** - choosing the most appropriate visualisation to tell a focused story starts with correctly reading the numbers yourself, and identifying the data needed to address business requirements means judging what the figures can and cannot support.
- **Data volume, capacity and throughput calculations** support **Data preparation and linkage** and **Data management** - planning pipelines and managing data across services requires you to reason about record counts, duplicate rates, load times, and storage growth.
- **Budget and cost questions** support **Managing a data project** - contributing to project planning includes understanding licence costs, day rates, and simple cost-benefit comparisons.
- **Reconciliation arithmetic** supports your quality assurance duties - following and applying quality assurance standards often comes down to checking that totals, subtotals, and percentages agree.

### Practice questions

**Question 1 (easy) - Percentage of missing data.** Your extract contains 24,000 records. During cleansing you find that 1,440 records have a missing date of birth. What percentage of records have a missing date of birth?

- A) 4%
- B) 6%
- C) 8%
- D) 14.4%

**Correct answer: B.** **Explanation:** Divide the missing count by the total and multiply by 100: 1,440 ÷ 24,000 = 0.06, and 0.06 × 100 = 6%. A quick sanity check: 10% of 24,000 is 2,400, so 1,440 must be less than 10%; and 5% would be 1,200, so the answer is a little above 5%. Option D is a distractor built from the digits of 1,440. Missing-value percentages like this are the bread and butter of your data quality reporting, so aim to do them almost automatically.

**Question 2 (easy) - Percentage change.** A digital service completed 18,500 applications in June and 20,350 in July. What was the percentage increase from June to July?

- A) 8.5%
- B) 9.1%
- C) 10%
- D) 11%

**Correct answer: C.** **Explanation:** The increase is 20,350 − 18,500 = 1,850. Divide by the *original* (June) figure: 1,850 ÷ 18,500 = 0.10, so 10%. The most common error is dividing by the new figure (1,850 ÷ 20,350 ≈ 9.1%, option B). Percentage change is always measured against the starting value unless the question says otherwise. You will make this calculation constantly when preparing month-on-month performance commentary for stakeholders.

**Question 3 (moderate) - Comparing rates across a table.** Four regional teams processed cases last quarter:

| Team | Cases received | Cases completed |
|---|---|---|
| North | 4,800 | 4,272 |
| South | 6,200 | 5,394 |
| East | 3,500 | 3,150 |
| West | 5,000 | 4,300 |

Which team had the highest completion rate?

- A) North
- B) South
- C) East
- D) West

**Correct answer: C.** **Explanation:** Compute each completion rate: North 4,272 ÷ 4,800 = 89%; South 5,394 ÷ 6,200 = 87%; East 3,150 ÷ 3,500 = 90%; West 4,300 ÷ 5,000 = 86%. East is highest at 90%, even though South completed the most cases in absolute terms. This is the crucial distinction between counts and rates: the biggest raw number is often not the best performance. When you develop visualisations that tell a focused story, choosing to display rates rather than raw counts (or both, clearly labelled) can completely change the message - so you must be able to compute them confidently first.

**Question 4 (moderate) - Pipeline throughput.** Your ingestion pipeline processes records at a steady 1,500 records per minute. Tonight's load contains 2.7 million records, and the pipeline must also complete a fixed 20-minute validation step after ingestion finishes. The processing window closes 31 hours after the load starts. Will the load complete in time, and with how much margin?

- A) Yes, with 40 minutes to spare
- B) Yes, with 10 minutes to spare
- C) No, it will overrun by 20 minutes
- D) No, it will overrun by 60 minutes

**Correct answer: A.** **Explanation:** Ingestion time is 2,700,000 ÷ 1,500 = 1,800 minutes, which is 1,800 ÷ 60 = 30 hours. Add the 20-minute validation step: total 30 hours 20 minutes. The window is 31 hours, so the margin is 31:00 − 30:20 = 40 minutes. The trap is unit conversion: keep everything in minutes (window = 1,860 minutes; job = 1,800 + 20 = 1,820 minutes; margin = 40 minutes) to avoid slips. Throughput-versus-window arithmetic like this is exactly what you do when planning overnight loads as part of managing and moving data between systems.

**Question 5 (moderate) - Licence budget.** Your team has a software budget of £48,000 for the year. An analytics platform costs £1,250 per user per year, and a visualisation tool costs £550 per user per year. The team needs 12 analytics licences and 20 visualisation licences. How much budget remains after both purchases?

- A) £22,000
- B) £26,000
- C) £15,000
- D) £11,000

**Correct answer: A.** **Explanation:** Analytics licences: 12 × £1,250 = £15,000. Visualisation licences: 20 × £550 = £11,000. Total spend: £15,000 + £11,000 = £26,000. Remaining budget: £48,000 − £26,000 = £22,000. Notice that options B, C and D are all intermediate values from the calculation (total spend, analytics subtotal, visualisation subtotal) - assessments frequently offer your own intermediate numbers as distractors, so always finish the final step before choosing. Simple budget arithmetic like this supports your contribution to project planning in Managing a data project.

**Question 6 (moderate) - Weighted average.** You are combining user satisfaction scores from three research rounds into one headline figure for a stakeholder report. Round 1: 120 respondents, average score 4.0. Round 2: 80 respondents, average score 3.5. Round 3: 200 respondents, average score 4.2. What is the overall average score across all respondents (to one decimal place)?

- A) 3.9
- B) 4.0
- C) 4.1
- D) 4.2

**Correct answer: B.** **Explanation:** Weight each average by its respondent count: (120 × 4.0) + (80 × 3.5) + (200 × 4.2) = 480 + 280 + 840 = 1,600. Total respondents: 120 + 80 + 200 = 400. Overall average: 1,600 ÷ 400 = 4.0. The naive approach - averaging the three averages, (4.0 + 3.5 + 4.2) ÷ 3 = 3.9 (option A) - is wrong because the rounds have different sizes. Weighted averages are essential whenever you aggregate metrics across groups of different sizes, and being able to explain *why* the simple average misleads is a lovely example of communicating between the technical and non-technical.

**Question 7 (moderate) - Storage growth projection.** Your team's database currently holds 3.2 terabytes and is growing by 5% per month. Approximately how much storage will it need in three months' time?

- A) 3.36 TB
- B) 3.52 TB
- C) 3.70 TB
- D) 3.85 TB

**Correct answer: C.** **Explanation:** Growth compounds monthly: 3.2 × 1.05 = 3.36 TB after month one; 3.36 × 1.05 = 3.528 TB after month two; 3.528 × 1.05 ≈ 3.70 TB after month three. Equivalently, 3.2 × 1.05³ = 3.2 × 1.157625 ≈ 3.70 TB. The distractor at option B is what you get from simple (non-compounding) growth of 5% × 3 = 15%: 3.2 × 1.10 would be wrong anyway, but 3.2 × 1.15 = 3.68 is close to the right answer, which is why the options are spaced to reward the exact method. Capacity forecasting supports your Data management skill - anticipating growth is part of delivering data management across services.

**Question 8 (moderate) - Percentages versus percentage points.** Last quarter, 12% of records failed validation. This quarter, 9% failed. A colleague drafts the line: "Validation failures fell by 3%." As the analyst quality assuring the report, which correction is right?

- A) No correction needed; the sentence is accurate
- B) Failures fell by 3 percentage points, which is a 25% reduction in the failure rate
- C) Failures fell by 3 percentage points, which is a 33% reduction in the failure rate
- D) Failures fell by 9 percentage points

**Correct answer: B.** **Explanation:** The gap between 12% and 9% is 3 *percentage points*. As a relative change, the failure rate fell by 3 ÷ 12 = 0.25, i.e. 25%. Saying "fell by 3%" understates the improvement and confuses the two concepts; saying 33% (option C) wrongly divides 3 by 9, the *new* rate, instead of the original. This distinction trips up even experienced report writers, and catching it is precisely what following and applying quality assurance standards looks like in practice. When you brief non-technical stakeholders, spell it out: "the failure rate dropped from 12% to 9% - a quarter fewer failures."

**Question 9 (hard) - Multi-step projection with cost.** A casework service received 45,000 applications this year. Volumes are forecast to grow 8% next year. Each application currently costs £3.20 in data processing. A planned pipeline improvement would cut the per-application processing cost by 15% from the start of next year. What is the forecast total processing cost for next year with the improvement in place?

- A) £155,520
- B) £132,192
- C) £144,000
- D) £126,360

**Correct answer: B.** **Explanation:** Step 1 - next year's volume: 45,000 × 1.08 = 48,600 applications. Step 2 - improved unit cost: £3.20 × 0.85 = £2.72. Step 3 - total: 48,600 × £2.72 = £132,192. Option A applies the growth but forgets the saving (48,600 × £3.20 = £155,520). Option C is this year's cost (45,000 × £3.20). Option D applies the saving but not the growth (45,000 × £2.72 = £122,400 - close to but not equal to D, which also miscalculates). Multi-step questions reward writing each stage down; a single skipped step lands you on a distractor. Producing exactly this kind of costed forecast is how a data analyst delivers business impact through data and enables decision making.

**Question 10 (moderate) - Duplicates and cleansing yield.** You receive a file of 62,000 rows. De-duplication removes 4.5% of rows. Of the remainder, 2,368 rows fail validation and are quarantined. How many rows survive to the clean dataset?

- A) 59,210
- B) 56,842
- C) 57,632
- D) 55,922

**Correct answer: B.** **Explanation:** Step 1 - remove duplicates: 62,000 × 0.045 = 2,790 rows removed, leaving 62,000 − 2,790 = 59,210 rows. Step 2 - remove validation failures: 59,210 − 2,368 = 56,842 rows. Option A is the intermediate figure after de-duplication only. Option C wrongly subtracts both amounts from different bases, and option D applies the 4.5% *after* the validation removals - order and base matter. Tracking exactly how many records each cleansing stage removes, and being able to account for every row, is core to preparing and cleansing data so it is fit for purpose - and it is the first question a sharp stakeholder will ask about your numbers.

**Question 11 (hard) - Rates per 1,000 population.** Two local authority areas report referrals to a support service. Area A: 1,840 referrals, population 230,000. Area B: 2,250 referrals, population 375,000. A stakeholder claims "Area B has the bigger problem because it has more referrals." What do the rates per 1,000 population show?

- A) Area A: 8.0 per 1,000; Area B: 6.0 per 1,000 - Area A's rate is higher
- B) Area A: 6.0 per 1,000; Area B: 8.0 per 1,000 - Area B's rate is higher
- C) Both areas have the same rate of 7.0 per 1,000
- D) The rates cannot be compared because the populations differ

**Correct answer: A.** **Explanation:** Area A: 1,840 ÷ 230,000 × 1,000 = 8.0 per 1,000. Area B: 2,250 ÷ 375,000 × 1,000 = 6.0 per 1,000. Although Area B has more referrals in absolute terms, its much larger population means its *rate* is lower; relative to population, Area A has a third more referrals per person. Option D is exactly backwards - differing populations are the very reason rates exist. Converting counts to rates so that comparisons are fair is a foundational statistical technique in your Applying statistical and analytical tools and techniques skill, and gently correcting the stakeholder's interpretation is a classic communicating-between-the-technical-and-non-technical moment.

**Question 12 (hard) - Reading scale qualifiers.** A finance table reports data platform costs "in £ thousands": Q1: 210, Q2: 235, Q3: 260, Q4: 195. Your director asks: "What was the total annual cost, and which quarter was cheapest?" Which answer is correct?

- A) Total £900; Q4 cheapest
- B) Total £900,000; Q4 cheapest
- C) Total £900,000; Q1 cheapest
- D) Total £90,000; Q4 cheapest

**Correct answer: B.** **Explanation:** Sum the quarters: 210 + 235 + 260 + 195 = 900. But the table is "in £ thousands", so 900 means £900,000. Q4's 195 is the smallest figure, so Q4 was cheapest. Option A forgets the scale qualifier entirely; option D misapplies it by a factor of ten; option C misreads the minimum. Ignoring qualifiers like "in thousands" or "in millions" is one of the most common failure modes in numeric assessments and in real reporting. Building the habit of reading table headers, units, and footnotes *before* the numbers will serve both your test score and your professional credibility.

**Question 13 (hard) - Ratio reasoning for sampling.** For a quality audit you must check a stratified sample of 450 records, drawn from three sources in the ratio 4 : 3 : 2 (Source X : Source Y : Source Z). How many records must you check from Source Z?

- A) 200
- B) 150
- C) 100
- D) 90

**Correct answer: C.** **Explanation:** The ratio parts total 4 + 3 + 2 = 9. Each part is therefore 450 ÷ 9 = 50 records. Source Z has 2 parts: 2 × 50 = 100 records. (Source X gets 200, Source Y gets 150 - options A and B are the other strata, planted as distractors.) Check: 200 + 150 + 100 = 450. Ratio-share calculations appear whenever you design samples for quality assurance or allocate records across processing batches, supporting both your quality assurance duties and your contribution to planning analytical approaches.

**Question 14 (moderate) - Interpreting a performance dashboard.** Your service dashboard shows the following for last week: 9,600 visits; 7,200 users started the application; 5,760 users completed it. The service standard target is that at least 75% of users who start an application complete it. Did the service meet the target, and what was the start-to-completion rate?

- A) No - the rate was 60%
- B) Yes - the rate was exactly 75%
- C) Yes - the rate was 80%
- D) No - the rate was 66%

**Correct answer: C.** **Explanation:** The target measures completions against *starts*, not visits: 5,760 ÷ 7,200 = 0.80, so 80%, which exceeds the 75% target. Option A comes from dividing completions by visits (5,760 ÷ 9,600 = 60%) - the wrong denominator, since many visitors browse without starting. Option D divides starts into visits (7,200 ÷ 9,600 = 75%) and then mislabels it. Choosing the correct denominator is the whole game in funnel metrics: the same three numbers support several different rates, and only one matches the definition in the service standard. Being precise about which rate a stakeholder actually needs - and explaining why - is a core part of communicating analytical results without misleading.

**Question 15 (moderate) - Cost per record comparison.** Two options exist for an address-cleansing service. Option 1: a flat annual fee of £18,000 with unlimited records. Option 2: pay-as-you-go at £0.012 per record. Your team expects to cleanse 1.4 million records next year, though volumes could rise by up to 20%. Which option is cheaper at the expected volume, and does the answer change at the higher volume?

- A) Option 2 is cheaper at both volumes
- B) Option 1 is cheaper at both volumes
- C) Option 2 is cheaper at the expected volume, but Option 1 becomes cheaper at the higher volume
- D) Option 1 is cheaper at the expected volume, but Option 2 becomes cheaper at the higher volume

**Correct answer: C.** **Explanation:** At the expected volume: 1,400,000 × £0.012 = £16,800, which is less than £18,000, so Option 2 wins. At the higher volume: 1,400,000 × 1.20 = 1,680,000 records, and 1,680,000 × £0.012 = £20,160, which exceeds £18,000, so Option 1 wins. The break-even point is £18,000 ÷ £0.012 = 1,500,000 records - a useful figure to quote to your team: below 1.5 million records, pay-as-you-go is cheaper; above it, the flat fee is. Break-even reasoning like this turns a simple arithmetic exercise into genuine decision support - exactly what delivering business impact through data means in a spending decision.

**Question 16 (hard) - Sense-checking a headline figure.** A draft report states: "The backlog fell 30% in April (from 12,000 to 8,400 cases) and a further 25% in May, meaning the backlog has more than halved since March." As the analyst quality assuring this, what was the end-of-May backlog, and is the "more than halved" claim correct?

- A) 6,300 cases; the claim is correct
- B) 6,300 cases; the claim is wrong because 6,300 is more than half of 12,000
- C) 5,400 cases; the claim is correct
- D) 6,600 cases; the claim is wrong

**Correct answer: B.** **Explanation:** Work the figures first. April: 12,000 × 0.70 = 8,400 (matching the report). May: a further 25% fall means 8,400 × 0.75 = 6,300 cases at the end of May. Now test the claim: "more than halved since March" would require the backlog to be below half of 12,000, which is 6,000. Since 6,300 is above 6,000, the backlog has *not* halved - the total fall is (12,000 − 6,300) ÷ 12,000 = 5,700 ÷ 12,000 = 47.5%. So the end-of-May figure is 6,300 and the claim is wrong, which is option B. The underlying trap is one many report writers fall into: successive falls of 30% and 25% do not add to 55%, because the second percentage applies to a smaller base - they combine as 1 − (0.70 × 0.75) = 47.5%. Catching exactly this kind of over-claim in a draft before publication is what following and applying quality assurance standards means in practice, and explaining the compounding point tactfully to the report's author is a fine exercise in communicating between the technical and non-technical.

**Question 17 (easy) - Averages for a stakeholder summary.** Processing times (in days) for seven sampled cases were: 3, 4, 4, 5, 6, 7, 34. A stakeholder asks for "the typical processing time". Which figure best represents a typical case, and why?

- A) The mean of 9 days, because the mean uses all the data
- B) The median of 5 days, because the extreme 34-day case pulls the mean well above what most users experience
- C) The mode of 4 days, because it is the most common value
- D) The maximum of 34 days, to be safe

**Correct answer: B.** **Explanation:** First compute both: the mean is (3 + 4 + 4 + 5 + 6 + 7 + 34) ÷ 7 = 63 ÷ 7 = 9 days; the median (middle value of the sorted list) is 5 days. Six of the seven cases took 7 days or fewer, so "typical" is far better represented by 5 than by 9 - the single 34-day outlier drags the mean upward. The mode (option C) is defensible but fragile with so few observations, and the maximum (option D) answers a different question about worst cases. The strongest professional answer often reports the median *and* mentions the outlier, since that 34-day case may itself be worth investigating. Choosing the right summary statistic for a skewed distribution - and explaining the choice in plain language - is a foundational part of applying statistical techniques and communicating them to non-technical stakeholders.

### Preparation tips

- **Rebuild fluency with the core four.** Percentage change, weighted averages, rates per 1,000, and ratio shares cover most questions in role-specific numeric tests. Practise each until the *method* is automatic, so test time goes on reading the data, not recalling the technique.
- **Write down intermediate steps.** Multi-step questions plant your own intermediate results as wrong options. A two-line jotting ("48,600 apps; £2.72 each") defends you against choosing your own half-finished answer.
- **Read units and qualifiers first.** Before touching any numbers, scan for "in thousands", "per month", "per 1,000 population", and date ranges. Ten seconds of reading prevents a whole question going wrong.
- **Use the calculator for arithmetic, your head for method.** The calculator cannot tell you whether to divide by the old or new figure - that judgement is what the test measures. Decide the method, then compute.
- **Estimate before you calculate.** A rough order-of-magnitude guess ("about 10%", "roughly £130k") lets you reject implausible options instantly and catch keying errors.
- **Practise under time pressure.** Set a timer for 90 seconds per question. The skill of moving on from a stubborn question is trainable - and valuable.

### Common pitfalls

- **Misreading chart and table labels.** Confusing monthly with quarterly data, or missing a "£ thousands" qualifier, produces confident wrong answers. This is the single most common error in numeric assessments.
- **Dividing by the wrong base.** Percentage change uses the original value; relative reduction uses the starting rate. When in doubt, write the fraction out before computing.
- **Confusing counts with rates.** The team with the most completions is not necessarily the best performer. Assessments love this trap because real dashboards do too.
- **Over-calculating.** If the options are far apart, estimation answers the question in a third of the time. Save precision for questions whose options are close together.
- **Time-sink questions.** One stubborn multi-stage problem can consume five minutes. Flag it, skip it, and bank the easier marks first - exactly the triage you apply when a delivery deadline looms.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment evaluates how well you understand, analyse, and draw correct conclusions from written business information. The passages mirror the reading demands of your role: data governance policies, quality assurance standards, stakeholder emails, accessibility guidance, and analytical reports. Most questions use a strict True / False / Cannot Say format - you must answer based *only* on the text provided, setting aside anything you happen to know from outside - and a smaller number are multiple-choice comprehension items that ask for the best summary or the author's main point.

The three options mean exactly this: **True** - the statement follows logically from the passage; **False** - the statement contradicts the passage; **Cannot Say** - the passage does not give enough information to decide either way. "Cannot Say" is not a hedge or a soft option; it is the *correct* answer whenever the passage is silent or ambiguous on the point, and disciplined use of it is what these tests reward most.

Timing is usually tight - often less than a minute per question - to simulate workplace reading under deadline. For a data analyst this is deeply realistic: you routinely need to extract the operative rule from a governance policy, spot the caveat buried in a methodology note, or work out exactly what a stakeholder's email is (and is not) asking for, all between meetings.

### What it measures for your role

- **Precise rule extraction** maps to **Data management** and **Data ethics and privacy** - following organisational data governance, including policies on data access, sharing, dissemination and protection, depends on reading policy text exactly as written, and sharing risks through appropriate channels requires you to recognise when a case falls outside what a policy permits.
- **Distinguishing fact from inference** maps to **Applying statistical and analytical tools and techniques** - quality assurance standards demand that published statements are supported by the data, so the True / False / Cannot Say discipline is the verbal twin of statistical rigour.
- **Reading stakeholder intent** maps to **Communicating between the technical and non-technical** - managing differing stakeholder perspectives starts with accurately understanding what each stakeholder has actually said, including tone and nuance.
- **Comprehending standards and documentation** maps to **Data visualisation** (accessibility guidance), **Developing code for analysis** (approach documentation), and **Data preparation and linkage** (pipeline and model documentation) - all of which require careful, literal reading.

### Practice questions

**Passage A - Data sharing policy extract.** *"Departmental data may be shared with another government organisation only where a data sharing agreement is in place and the request has been approved by the Information Asset Owner. Anonymised statistical outputs are exempt from the agreement requirement, provided that no individual can be identified either directly or through combination with other published data. Requests involving personal data must additionally be assessed against the UK GDPR by the Data Protection Team before any transfer occurs. Where a request is urgent, the Information Asset Owner may grant provisional approval, but the transfer itself must not take place until the Data Protection Team assessment, where required, is complete."*

**Question 1 (easy).** True, False, or Cannot Say: "Anonymised statistical outputs can be shared without a data sharing agreement."

**Correct answer: True.** **Explanation:** The passage states directly that "Anonymised statistical outputs are exempt from the agreement requirement" - with the condition that no individual can be identified. The statement as written matches the exemption the passage grants. Note that the exemption is conditional; a statement claiming anonymised outputs can *always* be shared *in all circumstances* without any conditions would be harder to support. Here, the claim mirrors the passage's own wording, so True is safe.

**Question 2 (moderate).** True, False, or Cannot Say: "Provisional approval from the Information Asset Owner allows an urgent transfer of personal data to proceed immediately."

**Correct answer: False.** **Explanation:** The final sentence explicitly separates provisional *approval* from the *transfer*: "the transfer itself must not take place until the Data Protection Team assessment, where required, is complete." Personal data requests are among those where the assessment is required ("Requests involving personal data must additionally be assessed"). So provisional approval does not permit an immediate transfer of personal data - the statement contradicts the passage. This is exactly the kind of subtle but crucial distinction you must catch when applying data governance policies in practice: approval to proceed with a *process* is not permission to move the *data*.

**Question 3 (moderate).** True, False, or Cannot Say: "The Data Protection Team can refuse a request that the Information Asset Owner has approved."

**Correct answer: Cannot Say.** **Explanation:** The passage says personal data requests "must additionally be assessed against the UK GDPR by the Data Protection Team", but it never states what powers the team has following that assessment - refusal, amendment, or mere comment. It is a plausible real-world inference that an assessment could block a transfer, but the text does not say so, and verbal reasoning demands you answer from the text alone. When the passage is silent on the specific claim, Cannot Say is the disciplined answer. This mirrors your professional duty not to over-interpret policy: if the text does not settle a question, you escalate and ask - sharing risks through appropriate channels - rather than assume.

**Passage B - Stakeholder email.** *"From: Head of Casework Policy. Subject: Regional dashboard. Thanks for the new dashboard - the team find it genuinely useful. Two things before Thursday's board. First, the completion-rate chart currently combines paper and digital applications; the board specifically asked to see digital separately, so please split it. Second, several colleagues using screen readers report that the chart labels are not being read out. I know accessibility fixes can take time, so if a full fix isn't possible by Thursday, a data table alongside the chart would be an acceptable interim step. I'd rather delay the dashboard than present figures we can't stand behind, but I don't currently see any accuracy problems - the issue is presentation."*

**Question 4 (easy).** True, False, or Cannot Say: "The Head of Casework Policy believes the dashboard currently contains inaccurate figures."

**Correct answer: False.** **Explanation:** The email states plainly: "I don't currently see any accuracy problems - the issue is presentation." The sender explicitly distinguishes between accuracy (fine) and presentation (needs work). The earlier sentence about preferring to "delay the dashboard than present figures we can't stand behind" expresses a general principle, not a claim that current figures are wrong - and the sender immediately clarifies this. Reading past the conditional framing to the sender's actual position is a core skill for managing stakeholder communications without manufacturing false alarms.

**Question 5 (moderate) - Multiple choice.** Which of the following best summarises what the sender is asking for by Thursday?

- A) A fully accessible dashboard with all accessibility defects resolved
- B) A split of the completion-rate chart into digital and paper, plus either fixed screen-reader labels or an interim data table
- C) A delay to the board presentation until accessibility is fixed
- D) A data table to replace the dashboard entirely

**Correct answer: B.** **Explanation:** The email makes two requests: split the combined chart ("please split it") and address the screen-reader issue, with an explicit fallback ("a data table alongside the chart would be an acceptable interim step"). Option A overstates the accessibility requirement - the sender accepts an interim step. Option C misreads the delay remark, which was conditional on accuracy problems that the sender says do not exist. Option D inflates "alongside the chart" into "replace the dashboard". Notice how each wrong option distorts the text slightly - overstating, understating, or shifting a condition. Developing inclusive, accessible data visualisations that recognise different user needs is a named behaviour in your Data visualisation skill, and this email is exactly how such requirements arrive in real life.

**Passage C - Accessibility standard for published statistics.** *"All charts published on the service's statistics pages must meet the following requirements. Colour must never be the only means of distinguishing data series; a difference in pattern, shape, or direct labelling must also be present. All charts must include alternative text that describes the main message of the chart, not merely its type and axes. Where a chart presents more than five data series, publishers should consider whether a table would communicate the data more clearly. Interactive charts must be fully operable by keyboard alone. These requirements apply to all new publications from 1 April; existing publications must be brought into compliance when they are next updated, rather than immediately."*

**Question 6 (easy).** True, False, or Cannot Say: "A chart that distinguishes its data series by colour alone meets the standard."

**Correct answer: False.** **Explanation:** The passage states: "Colour must never be the only means of distinguishing data series; a difference in pattern, shape, or direct labelling must also be present." A colour-only chart directly contradicts this requirement, so the statement is False. This rule exists because users with colour vision deficiency - roughly 1 in 12 men - cannot reliably separate series by hue alone. It is a requirement you apply every time you build a visualisation intended for a diverse audience.

**Question 7 (moderate).** True, False, or Cannot Say: "Charts with more than five data series are prohibited."

**Correct answer: False.** **Explanation:** The passage says publishers "should consider whether a table would communicate the data more clearly" when a chart has more than five series. "Should consider" is guidance to reflect, not a prohibition - the standard does not ban such charts. The statement contradicts the passage by converting a recommendation into a rule, which is precisely the kind of over-reading that verbal reasoning tests punish. Distinguishing "must" from "should" and "consider" is essential when you apply standards documents in your visualisation work; the difference determines what is mandatory versus advisory.

**Question 8 (moderate).** True, False, or Cannot Say: "An existing publication that is never updated must still be brought into compliance by 1 April."

**Correct answer: False.** **Explanation:** The final sentence states that "existing publications must be brought into compliance when they are next updated, rather than immediately." Compliance for existing material is triggered by the next update, not by the 1 April date, which applies to *new* publications. A publication that is never updated has no trigger under this text - so the claim that it must comply by 1 April contradicts the stated rule. (Whether such a publication *should* be updated is a separate question the passage does not address.) Careful attention to which rule attaches to which category - new versus existing - is a hallmark of accurate policy reading.

**Passage D - Analytical report extract.** *"Completion rates for the digital service rose from 71% to 78% over the six months following the redesign. The largest gains were observed among users aged 65 and over, whose completion rate rose eleven percentage points. However, the analysis cannot attribute the improvement solely to the redesign: the assisted digital telephone support service was expanded during the same period, and seasonal application patterns differ between the two comparison windows. Survey responses suggest that satisfaction improved among users who completed the service, but the survey was offered only on the confirmation page, so users who abandoned the service are not represented. Further analysis using session-level data is planned for the next quarter."*

**Question 9 (moderate).** True, False, or Cannot Say: "The redesign caused the completion rate to rise by seven percentage points."

**Correct answer: Cannot Say.** **Explanation:** The rise from 71% to 78% - seven percentage points - is a fact in the passage, but *causation* is not: the report explicitly says "the analysis cannot attribute the improvement solely to the redesign" and lists two confounders (expanded telephone support and seasonal patterns). The passage neither confirms nor denies that the redesign caused the improvement; it says the question is unresolved. So the causal claim is Cannot Say - not False, because the passage does not rule out the redesign as the cause either. Separating correlation from attributed cause is the single most important habit in reading and writing analytical reports, and it sits at the heart of applying statistical techniques with integrity.

**Question 10 (moderate).** True, False, or Cannot Say: "The satisfaction survey results are representative of all users of the service."

**Correct answer: False.** **Explanation:** The passage states the survey "was offered only on the confirmation page, so users who abandoned the service are not represented." A survey that excludes abandoners cannot be representative of *all* users - the passage directly asserts this limitation. This is a textbook example of selection bias caveats in real government analysis, and spotting such caveats is part of following quality assurance standards: a headline like "satisfaction improved" must always carry its "among completers" qualifier when you communicate insights to stakeholders.

**Question 11 (easy).** True, False, or Cannot Say: "Users aged 65 and over showed the largest improvement in completion rate."

**Correct answer: True.** **Explanation:** The passage states: "The largest gains were observed among users aged 65 and over, whose completion rate rose eleven percentage points." The statement restates this directly, so it is True. Easy verification items like this reward reading the passage accurately rather than second-guessing; not every question hides a trap, and part of test discipline is answering the straightforward ones quickly to bank time for harder items - the same triage you use when reviewing a long report against a deadline.

**Passage E - Analytical code standard.** *"All analytical code that produces published figures must be stored in the team's version control repository. Each analysis must include documentation describing the approach taken, the data sources used, and any assumptions made. Code review is required before results are shared outside the team; the reviewer must not be the code's author. Automated tests are strongly recommended for any code that will be reused, and mandatory for code that runs on a schedule. Analysts remain responsible for the quality of their outputs even after review."*

**Question 12 (moderate).** True, False, or Cannot Say: "An analyst may review their own code if no other reviewer is available."

**Correct answer: False.** **Explanation:** The passage is unequivocal: "the reviewer must not be the code's author." No exception for reviewer availability is given, so self-review contradicts the standard regardless of circumstances. The temptation with this question is to import workplace pragmatism ("surely there's an exception when the team is short-staffed") - but the text admits none, and the test measures whether you can hold to the text. In practice, if you ever face this situation, the standard tells you the answer: results wait, or you escalate - they do not go out self-reviewed.

**Question 13 (hard).** True, False, or Cannot Say: "Automated tests are mandatory for reusable analysis code."

**Correct answer: False.** **Explanation:** Read the two categories precisely: tests are "strongly recommended for any code that will be reused, and mandatory for code that runs on a schedule." Reusable code attracts a strong recommendation, not a mandate; only *scheduled* code carries the mandatory requirement. The statement assigns the mandatory rule to the wrong category, so it contradicts the passage and is False. Reusable and scheduled code often overlap in real life, which is exactly why the test uses this structure - it checks whether you track which qualifier attaches to which noun. This literal precision is the same skill you use when producing analytical approach documentation and explaining the importance of testing code.

**Passage F - Data retention guidance.** *"Case management data must be retained for seven years from the date a case is closed, after which it must be deleted or fully anonymised. Analytical extracts derived from case management data inherit the retention period of the source records unless the extract has been fully anonymised, in which case it may be retained indefinitely. Analysts must record the creation date and source of every extract in the extract register. Where an extract combines records with different closure dates, the retention period is calculated from the most recent closure date among the included records. Requests to retain identifiable data beyond the standard period require approval from the Departmental Records Officer and must be justified by a continuing business need; convenience does not constitute a business need."*

**Question 14 (moderate).** True, False, or Cannot Say: "A fully anonymised analytical extract may be kept for longer than seven years."

**Correct answer: True.** **Explanation:** The passage states that an extract which "has been fully anonymised... may be retained indefinitely." Indefinite retention plainly permits keeping the extract beyond seven years, so the statement follows directly from the text. Note the precision required: the exemption applies to *fully anonymised* extracts only - an extract that is merely pseudonymised or partially anonymised would inherit the source retention period. When a question's claim uses a slightly weaker wording than the passage ("longer than seven years" versus "indefinitely"), the stronger text still supports the weaker claim, making it True.

**Question 15 (hard).** True, False, or Cannot Say: "An identifiable extract combining a case closed in 2020 and a case closed in 2024 must be deleted or anonymised in 2027."

**Correct answer: False.** **Explanation:** The passage says that for mixed extracts "the retention period is calculated from the most recent closure date among the included records." The most recent closure here is 2024, so the seven-year period runs to 2031, not 2027. The 2027 date comes from wrongly counting from the *earlier* closure (2020 + 7). Because the statement assigns a deletion deadline the rule contradicts, the answer is False rather than Cannot Say. Retention arithmetic like this is a genuine task in your Data management skill - following organisational policies on data protection includes knowing exactly when your extracts fall due for deletion, which is why the passage also requires an extract register.

**Question 16 (moderate).** True, False, or Cannot Say: "The Departmental Records Officer usually approves requests to retain identifiable data beyond the standard period."

**Correct answer: Cannot Say.** **Explanation:** The passage establishes the *process* - such requests "require approval from the Departmental Records Officer and must be justified by a continuing business need" - but says nothing about how often approval is granted. "Usually approves" is a claim about frequency that the text neither supports nor contradicts. The passage's firm tone ("convenience does not constitute a business need") might tempt you towards False, but tone is not evidence about outcomes: a strict-sounding rule could still see most well-founded requests approved. When a statement concerns something the passage simply does not measure, Cannot Say is the only defensible answer - the verbal equivalent of refusing to extrapolate beyond your data.

**Question 17 (moderate) - Multiple choice on Passage F.** Which of the following best states the main purpose of the extract register mentioned in Passage F?

- A) The passage does not state a purpose, but recording each extract's creation date and source is what makes its retention period calculable and enforceable
- B) To record which analysts are trained in data protection
- C) To list the business needs justifying long-term retention
- D) To log requests approved by the Departmental Records Officer

**Correct answer: A.** **Explanation:** The passage requires analysts to "record the creation date and source of every extract in the extract register" but never states the register's purpose explicitly - so the best answer is the one that acknowledges this while drawing the natural connection: retention periods depend on the source records and their closure dates, so a register of sources and dates is what allows anyone to work out when each extract falls due for deletion. Options B, C and D each attach the register to content the passage never mentions - training records, business-need justifications, and approval logs all appear nowhere in the text. In best-answer questions, unlike True/False/Cannot Say items, you choose the option *most* supported by the passage even when none is quoted verbatim - but the wrong options are still recognisable because they import material the text simply does not contain.

### Preparation tips

- **Train the "Cannot Say" muscle.** Most wrong answers on these tests come from choosing True or False when the passage is simply silent. Practise asking: "Does the text state or strictly entail this - or am I filling a gap with my own knowledge?" Your analyst's instinct for evidence is a genuine advantage here; trust it.
- **Read the question before re-reading the passage.** Skim the passage once for structure, then let each question direct you to the relevant sentence. Hunting for keywords beats re-reading whole paragraphs against the clock.
- **Mind the modal verbs.** "Must", "should", "may", "consider", "recommended", "mandatory" - policy passages turn on these words, and so do the questions. Underline them mentally as you read.
- **Watch for category-switching.** Many traps attach a rule from one category (new publications, scheduled code, personal data) to another (existing publications, reusable code, anonymised outputs). Check which noun the rule really modifies.
- **Practise on real documents.** The Government Digital Service standards, your department's data policies, and published statistical bulletins are perfect practice material: pick a paragraph, write three True/False/Cannot Say statements about it, and test yourself or a colleague.
- **Keep a steady pace.** At under a minute per question, aim to answer easy items in 30 seconds to buy time for the subtle ones.

### Common pitfalls

- **Bringing outside knowledge into the test.** You may know your organisation's real data sharing rules; the test only cares about the passage in front of you. Answer from the text alone, every time.
- **Confusing "likely" with "certain".** A passage saying an outcome is expected or suggested does not make a statement about that outcome True. Match the strength of the claim to the strength of the text.
- **Treating "Cannot Say" as a last resort.** It is a full-status answer, frequently correct by design. If the passage is silent, choose it with confidence.
- **Over-reading recommendations as rules.** "Should consider" is not "must". Converting advice into obligation is one of the most common ways to turn a False or Cannot Say into a wrong True.
- **Spending too long on the first read.** Scanning for the question's keywords is faster and more accurate than trying to memorise a dense policy paragraph up front - a habit that also serves you well with real 40-page governance documents.
- **Letting tone override text.** A passage written in strict, formal language can still leave a question open, and a friendly email can still contain a hard requirement. Judge each statement against what the words actually say, not the mood they create - the same discipline you apply when separating a stakeholder's frustration from their factual claims about your data.

## Workplace job-specific situational judgement assessment

### About this assessment

A workplace job-specific situational judgement assessment evaluates your decision-making, interpersonal skills, and professional conduct through realistic workplace dilemmas. Unlike the cognitive, numeric, and verbal tests, there is often no single objectively "right" answer - several responses may seem reasonable, but one aligns best with the values and behaviours the organisation needs from someone in your role. For a data analyst in UK government, those values include putting user needs first, transparency and honesty about what data can and cannot show, collaboration in multidisciplinary teams, accessibility and inclusion, and careful stewardship of personal data.

The typical format presents a short scenario followed by three to five possible actions. You may be asked to pick the **most effective** and **least effective** actions, to rank all the options from best to worst, or to rate each option's effectiveness independently. These assessments are usually untimed or generously timed, because they measure your natural judgement rather than your speed. That means you can and should think each scenario through properly.

Two general principles will serve you well. First, effective options usually address the root issue directly, promptly, and honestly, while keeping the right people informed. Least effective options usually delay, conceal, pass the problem on without context, or prioritise convenience over users and integrity. Second, "escalate" is not automatically weak and "handle it yourself" is not automatically strong - the best action fits the seriousness of the issue and your level of responsibility as a practitioner who works to appropriate standards, sometimes with support.

### What it measures for your role

- **Integrity with data** maps to **Data ethics and privacy** - applying fundamental principles of data ethics and privacy in your work, and sharing risks through appropriate channels, is tested through dilemmas about data sharing, re-identification, and presentation pressure.
- **Stakeholder handling** maps to **Communicating between the technical and non-technical** - scenarios probe how you support and host discussions in a multidisciplinary team with potentially difficult dynamics, manage differing stakeholder perspectives, and advocate for your team externally.
- **Quality under pressure** maps to your quality assurance duties in **Applying statistical and analytical tools and techniques** and to **Data preparation and linkage** - dilemmas test whether you protect data quality when deadlines squeeze.
- **Delivery judgement** maps to **Managing a data project** and **Delivering business impact through data** - scenarios explore scope, requirements, prioritisation, and keeping work aligned to organisational priorities.
- **Team behaviour** maps to your role-level duty to ensure data is used to achieve the team's goals - collaboration, openness about mistakes, and supporting colleagues all feature.

### Practice questions

**Question 1 (easy) - An error in published figures.** Two days after your team's monthly statistics were published on GOV.UK, you discover that a filter error in your preparation code inflated one regional figure by around 8%. The figure has already been quoted in a local newspaper. What is the most effective and least effective response?

- A) Tell your line manager immediately, explain the error and its size, and propose issuing a correction following the team's revisions policy
- B) Quietly fix the code so next month's figures are right, avoiding embarrassment over a relatively small error
- C) Wait to see whether anyone else notices before deciding what to do
- D) Post an explanation from your own account on the newspaper's website comments section

**Most effective: A. Least effective: C.** **Explanation:** Option A is honest, prompt, proportionate, and uses the proper channel - published government statistics carry revision and correction policies precisely for this situation, and transparency is the foundation of public trust in official figures. Option B fixes the future but conceals the past: the public record stays wrong, and the concealment compounds the original error. Option D is well-intentioned but bypasses your organisation's communication channels and could create confusion. Option C is worst: it is pure delay, leaves a known error in the public domain, and gambles your team's credibility on nobody checking. Owning errors quickly is a strength, not a weakness - it is what following quality assurance standards means when things go wrong.

**Question 2 (moderate) - A request for identifiable data.** A policy colleague you like and trust emails asking you to send "the underlying dataset with names and addresses" for a briefing they are writing, adding "it's urgent, the deputy director needs it today." You know this dataset contains personal data and you are not aware of any data sharing agreement covering this use. What is the most effective and least effective response?

- A) Send the data - the deputy director's authority covers the request, and delay would harm the briefing
- B) Reply promptly explaining that personal data needs an approved sharing route, offer an anonymised or aggregated extract that may meet the actual need today, and flag the request to your data governance contact
- C) Ignore the email until the colleague follows the proper process
- D) Send the data but ask the colleague to delete it after use

**Most effective: B. Least effective: A (with D a close second-worst).** **Explanation:** Option B does three things well: it protects personal data in line with governance policy, it solves the colleague's real problem - briefings almost never need names and addresses, so an aggregated extract usually serves the genuine user need - and it routes the request through the appropriate channel, which is exactly how your role profile describes sharing data ethics and privacy risks. Option A treats seniority as authorisation, which it is not; urgency never suspends data protection law. Option D adds a fig leaf to the same breach - "delete after use" does not create a lawful sharing route. Option C protects the data but fails the colleague and the organisation: passive refusal without explanation damages relationships and delays legitimate work. The best public servants are firm on the rule and generous with the alternative.

**Question 3 (moderate) - Pressure to present data favourably.** A senior stakeholder reviewing your draft dashboard asks you to truncate the y-axis on a performance chart so a modest 3% improvement "looks like the step change we've promised the board." What is the most effective and least effective response?

- A) Make the change - axis choices are presentational, and the stakeholder owns the message
- B) Refuse and tell the stakeholder that manipulating charts is unethical
- C) Explain that the truncated axis would exaggerate the trend and risk the board's trust if noticed, and offer alternatives: an honest annotation of the 3% improvement, context from previous periods, or supplementary measures that show genuine progress
- D) Make the change but add a footnote in small text noting the axis does not start at zero

**Most effective: C. Least effective: A.** **Explanation:** Option C holds the line on honest presentation while treating the stakeholder as a partner with a legitimate communication need - the essence of managing differing stakeholder perspectives. It also demonstrates the visualisation skill of telling a *focused but truthful* story. Option B reaches the right ethical conclusion but with a delivery that damages the relationship and casts the stakeholder as a villain rather than someone under pressure; you can be firm without being accusatory. Option D knowingly ships a misleading chart with a disclaimer - the small print does not undo the visual impression, and visual integrity is the point. Option A is least effective: axis truncation chosen *specifically to exaggerate* is misrepresentation, and "the stakeholder owns the message" abdicates your professional responsibility for how data is communicated. Transparency is a core public sector value precisely because trust, once lost, is very hard to rebuild.

**Question 4 (moderate) - Difficult dynamics in a team discussion.** You are hosting a session to agree definitions for a new performance metric. Ten minutes in, a developer and a policy lead are talking over each other - the developer insists the policy lead's preferred definition is "impossible to compute from the data we actually have", while the policy lead says the developer is "blocking what ministers have asked for." Other attendees have gone quiet. What is the most effective and least effective response?

- A) Let the two of them argue it out - the strongest case will win, and it is their disagreement to resolve
- B) Pause the discussion, restate the shared goal, capture both concerns on the board - the ministerial requirement and the data constraint - and propose examining what data *could* support the policy intent, before inviting the quieter attendees' views
- C) Side with the developer, since you know the data constraint is real
- D) End the meeting and ask both parties to email you their positions separately

**Most effective: B. Least effective: A.** **Explanation:** Option B does what a good session host does: de-escalates, reframes the conflict as a shared problem (both concerns are legitimate), and widens participation - supporting and hosting discussions within a multidisciplinary team with potentially difficult dynamics is a named behaviour in your Communicating between the technical and non-technical skill. Note that B also reflects collaboration and inclusion: the quiet attendees may hold the missing insight. Option C may be factually right but prematurely picks a winner, entrenching the conflict and ignoring that the policy need is real too - often a proxy measure or a phased approach satisfies both. Option D postpones rather than resolves, and separating the parties prevents the joint problem-solving the metric needs. Option A is least effective: abandoning facilitation while dynamics deteriorate silences the wider team and lets the loudest voices decide - the opposite of hosting.

**Question 5 (moderate) - A colleague's code defect.** While reusing a colleague's analysis script, you notice a join that silently drops records with missing postcodes - and you realise the script produced figures that went into last quarter's published report. Your colleague is friendly but sensitive about criticism, and is currently on leave for a week. What is the most effective and least effective response?

- A) Wait until your colleague returns so they can check it themselves - it is their code and their reputation
- B) Quantify the impact of the dropped records now, and if the published figures are materially affected, alert your line manager the same day, framing it as a data quality issue rather than a personal failing; leave a kind note for your colleague explaining what you found
- C) Fix the script for your own use and move on - the published report is not your responsibility
- D) Email the whole team pointing out the error so everyone knows not to reuse the script

**Most effective: B. Least effective: A.** **Explanation:** Option B separates the two questions correctly: *is the public record wrong?* (urgent, cannot wait a week) and *how do I treat my colleague fairly?* (with kindness and no blame). Quantifying impact first means you escalate with facts, not alarm - identifying and resolving data quality issues is your job, and published figures affect real users and decisions. Option A privileges a colleague's comfort over the integrity of published statistics; a week's delay on a potentially material error fails the public. Option C is the narrowest possible reading of responsibility - quality assurance in a team is everyone's business, and you found the issue. Option D addresses the reuse risk but publicly exposes a colleague who has had no chance to respond, damaging trust and team culture; the same protection is achieved through the manager and a quiet note. Collaboration and candour can and should coexist.

**Question 6 (moderate) - Deadline versus data quality (ranking).** It is Wednesday afternoon. A product manager needs analysis of service drop-out points for a prioritisation meeting on Friday morning. Exploring the data, you find the event logs contain duplicate session records that you estimate would take two full days to cleanse properly - taking you past the deadline. Rank these four responses from most to least effective:

- A) Deliver on Friday using the uncleansed data without mentioning the duplicates
- B) Tell the product manager the analysis is impossible and decline the task
- C) Cleanse a representative subset (for example, the two highest-volume journeys), deliver findings for those on Friday with the limitation clearly stated, and complete the full analysis next week
- D) Ask the product manager today whether a caveated partial analysis on Friday or a complete analysis on Tuesday better serves the prioritisation decision

**Best ranking: D, C, B, A.** **Explanation:** Option D is strongest because it treats the deadline as a user need to be understood rather than an immovable fact: the product manager owns the trade-off between speed and completeness, and consulting them today - while options remain open - is textbook working with others to identify business requirements. Option C is a close second: it is a sensible plan you could propose within D, delivering genuine value on time with honest caveats. Ranked alone it is slightly weaker than D only because it decides the trade-off *for* the stakeholder. Option B at least avoids misleading anyone, but "impossible" is untrue - partial and delayed routes exist - and declining without alternatives fails the collaboration test. Option A is clearly worst: knowingly presenting duplicate-inflated figures to a prioritisation meeting, without caveats, could misdirect resources and breaches the transparency your role depends on. Notice the overall pattern: honest options that preserve the decision-maker's choice rank highest; concealment ranks lowest.

**Question 7 (hard) - A misquoted statistic.** In a live cross-team meeting, a communications colleague states that "our analysis shows the new service has cut processing times by 40%." Your analysis actually showed a 40% reduction *in one pilot office*, with an average reduction of 12% across all offices - a distinction your report stated clearly. The claim is about to be included in a press notice being finalised this afternoon. What is the most effective and least effective response?

- A) Say nothing in the meeting and correct the record later by email
- B) Interrupt aggressively to say the figure is wrong and the report has clearly been misread
- C) Intervene politely in the meeting: "Can I add some context? The 40% was our pilot office; the average across all offices is 12% - happy to help get the exact wording right for the press notice"
- D) Let the press notice go out - 40% is technically one of your findings, and the publicity helps the programme

**Most effective: C. Least effective: D.** **Explanation:** Option C corrects the error at the moment it matters - before the press notice is finalised - and does so collaboratively, offering help rather than blame; this is advocating for accurate use of your team's work, a behaviour named in your communication skill. Option A risks the correction arriving after the press notice is drafted or issued; with an external publication hours away, "later" may be too late, though it beats never. Option B achieves accuracy at the cost of a public put-down that damages the relationship and makes colleagues warier of engaging with analysts. Option D is least effective: allowing a knowingly misleading figure into a government press notice trades public trust for programme publicity - the moment the 12% average emerges, the damage to credibility will far exceed any short-term gain. Being technically-true-but-misleading fails the transparency standard just as surely as being false.

**Question 8 (moderate) - Accessibility raised late.** Your interactive dashboard ships to the whole directorate on Monday. On Thursday, a colleague who uses keyboard-only navigation tells you they cannot operate the filter controls. Fixing the interaction properly will take an estimated week. What is the most effective and least effective response?

- A) Ship on Monday as planned and add the fix to the backlog for a future release
- B) Thank the colleague, verify the issue, and raise it with the team immediately: propose shipping with an accessible alternative in place (such as a keyboard-operable data table view of the same figures) and a committed date for the full fix, or delaying if no alternative is viable
- C) Delay the launch by a week without discussion - accessibility always trumps deadlines
- D) Suggest the colleague ask a teammate to operate the filters for them when they need the dashboard

**Most effective: B. Least effective: D.** **Explanation:** Option B treats accessibility as a genuine requirement rather than a nice-to-have, while engaging the team in an informed decision - developing inclusive, accessible visualisations that recognise different user needs is a named behaviour in your Data visualisation skill, and public sector services are for everyone, including your colleagues. The interim-alternative approach mirrors accepted practice: equivalent access now, full fix soon, transparently communicated. Option C gets the value right but acts unilaterally: a one-week delay affects many stakeholders, and the team - not you alone - should choose between a compliant interim and a delay. Option A ships a product you know excludes users, making them wait indefinitely on a backlog. Option D is least effective because it converts a product defect into the excluded person's ongoing burden, undermining their independence and dignity - the antithesis of inclusion.

**Question 9 (hard) - Urgent request for unvalidated figures.** At 16:30, a private office contact asks for "tonight's best figure" on application backlogs for a ministerial answer due tomorrow morning. Your new backlog pipeline produced its first output today, but it has not yet passed your team's validation checks; the previous validated figure is nine days old. What is the most effective and least effective response?

- A) Send the new unvalidated figure - it is the most current, and the minister needs the latest
- B) Send the nine-day-old validated figure without comment
- C) Consult your senior analyst or line manager now, then respond offering the validated figure with its date clearly stated, noting that a more recent figure exists but has not yet passed quality assurance - and agree what, if anything, can be validated by the morning
- D) Reply that no reliable figure is available until validation completes next week

**Most effective: C. Least effective: A.** **Explanation:** Option C balances every duty in play: honesty about what is and is not assured, service to an urgent legitimate need, and appropriate use of support - your role level explicitly works "under supervision" on statistical outputs, and a ministerial answer is exactly when to involve a senior colleague. Crucially, C also explores whether targeted overnight validation could unlock the newer figure - problem-solving rather than gatekeeping. Option B supplies quality-assured data but conceals its age and the existence of newer data, leaving the minister's office to discover later that "the latest figure" was not; transparency includes being honest about limitations. Option D overstates the constraint and abandons the user. Option A is least effective: an unvalidated first output from a brand-new pipeline is precisely the figure most likely to be wrong, and a wrong number in a ministerial answer - correctable only by written parliamentary correction - is among the most damaging outcomes an analyst can cause. Speed never outranks assurance when the public record is involved.

**Question 10 (hard) - A re-identification risk.** While linking a health-related dataset to local area statistics for publication, you notice that in three small rural areas, the combination of age band, area code, and condition category could plausibly identify individuals. Your project plan assumed the output was safely anonymised, and flagging this now may delay a publication your team has committed to. What is the most effective and least effective response?

- A) Proceed as planned - the fields are technically anonymised because no names are present, and the plan was already approved
- B) Quietly suppress the three problematic areas from the output without telling anyone, so the publication stays on schedule
- C) Raise the risk today with your line manager and data governance or disclosure control colleagues, bring your evidence, and recommend options such as wider age bands, merged geographies, or suppression - accepting a delay if that is what safe publication requires
- D) Ask a trusted peer analyst whether they think it is really a problem, and drop it if they are relaxed about it

**Most effective: C. Least effective: A.** **Explanation:** Option C is the model response and maps word-for-word onto your Data ethics and privacy skill: applying fundamental principles under supervision and *sharing risks through appropriate channels*. Re-identification through combination is a real disclosure risk - "no names" does not equal anonymous, and the passage of approved plans does not immunise new evidence. Bringing options, not just problems, keeps the publication viable. Option B reaches a defensible technical outcome through an indefensible route: silent, unrecorded changes to a statistical output undermine reproducibility and deprive disclosure control experts of the chance to check your fix - and the same risk may lurk in areas you did not spot. Option D delegates a governance question to an unaccountable channel. Option A is least effective: proceeding with a known identification risk in health-related data could cause genuine harm to real people, and "the plan was approved" is no defence when the approver did not know what you now know. Protecting the public's data is the deepest trust your role carries.

### Preparation tips

- **Anchor yourself in the values, not the politics.** Before the assessment, re-read the Civil Service values and your framework's emphasis on user needs, transparency, collaboration, accessibility, and inclusion. When two options both seem plausible, the one that better serves users and honesty is almost always rated higher.
- **Look for the option that addresses the root issue promptly.** Strong answers act on the real problem, at the right time, through the right channel. Weak answers delay, conceal, act unilaterally on team-level decisions, or hand the problem to someone else without context.
- **Calibrate escalation to your level.** As a data analyst you are expected to handle routine analytical judgement yourself, and to involve senior colleagues on matters of public record, personal data, and cross-team conflict. Escalating a ministerial figure is strength; escalating a formatting choice is not.
- **Read every option before rating any.** Options are often designed in near-pairs - the same action done transparently versus quietly, or promptly versus later. The differences only show when you compare the full set.
- **Practise with colleagues.** Talk through scenarios like these at a team huddle - real situational judgement is built by discussing why one response beats another, and hearing perspectives from user researchers, engineers, and policy colleagues will genuinely broaden your judgement.
- **Be yourself, thoughtfully.** These assessments work best - for you and the employer - when your answers reflect your genuine professional judgement, considered carefully, rather than a guess at what sounds impressive.

### Common pitfalls

- **Answering idealistically rather than practically.** "Convene a workshop with all stakeholders" sounds splendid but is a weak response to a figure going wrong in a press notice this afternoon. Effective beats elaborate.
- **Selecting passive options.** Waiting to see if anyone notices, leaving it for a colleague's return, or adding a known defect to a backlog - options that delay or transfer the problem are consistently rated least effective, and assessments include them deliberately.
- **Ignoring the values context.** In UK public sector assessments, options that compromise transparency, data protection, accessibility, or inclusion rate poorly even when they are fast and convenient. If an option trades public trust for speed, rate it down.
- **Over-escalating or under-escalating.** Passing every difficulty upwards suggests you cannot operate independently; handling personal data breaches or public record errors entirely alone suggests you do not know your limits. Match the response to the stakes.
- **Rating the person instead of the action.** A scenario may involve a sympathetic colleague or an intimidating senior stakeholder; the question is whether the *action* is effective, not whether you like or fear the people involved.

## Conclusion

Well done for working through this guide - that is a genuine investment in your professional development, and it will pay off both in assessments and in your everyday work as a data analyst.

You have now practised the four kinds of thinking your role draws on most. In the cognitive assessment you exercised pattern recognition, logical deduction, error checking, and prioritisation on the artefacts you really handle - pipelines, lookup tables, validation rules, and dashboards. In the numeric reasoning assessment you worked with the percentages, rates, ratios, budgets, and capacity figures that fill a data analyst's week, and practised showing your arithmetic step by step. In the verbal reasoning assessment you read governance policies, stakeholder emails, accessibility standards, and analytical reports with the precision they demand, and strengthened your discipline around True, False, and Cannot Say. And in the situational judgement assessment you weighed realistic dilemmas about data quality, privacy, honest presentation, difficult meetings, and urgent requests - always returning to the public sector values of user needs, transparency, collaboration, accessibility, and inclusion.

A few encouragements as you move forward. First, remember that every one of these skills is trainable: the analysts who score well are rarely the ones with special talent, and usually the ones who practised deliberately, reviewed their mistakes kindly, and tried again. Second, let this practice flow back into your day job - check your joins, caveat your findings, read the modal verbs in policies, and speak up early when something looks wrong. The assessment and the job are, in the end, the same craft. Third, keep growing across your skill set: your framework skills, from applying statistical techniques to managing a data project, each have a next level, and the habits you have practised here - precision, honesty, curiosity, and care for users - are exactly what carries you there.

If an assessment is coming up soon: prepare steadily rather than cramming, sleep well the night before, set up a quiet space, and trust your preparation. You know this work - these assessments simply give you a structured chance to show it.

Good luck. Your analysis makes government decisions better, and the care you bring to data is a genuine public service.
