# Data Scientist (Associate Data Scientist) - Psychometric Assessment Resources

## Introduction

Welcome! This guide has been created especially for you as an associate data scientist working within the UK Government Digital and Data profession. Whether you are preparing for an upcoming assessment, exploring what psychometric tests involve, or simply looking for a structured way to practise the thinking skills your role demands, you are in the right place.

Psychometric assessments are structured, standardised exercises that measure how you think, reason, and make decisions. They are widely used across the Civil Service and the wider public sector, both in recruitment and in professional development. For a data-focused role like yours, they matter for a very practical reason: your day-to-day work involves exploring and visualising data, building basic models, checking results carefully, and communicating findings clearly. Psychometric assessments measure exactly these kinds of abilities, so practising them helps you get better at the job itself, not just at the test.

This document is organised into four main assessment sections, each one tailored to your role and level:

1. **Workplace job-specific cognitive assessment** - how you spot patterns, check for errors, reason logically, and solve problems using the kinds of artefacts you handle every day, such as scripts, datasets, and model outputs.
2. **Workplace job-specific numeric reasoning assessment** - how you work with tables, percentages, ratios, model performance metrics, and capacity figures.
3. **Workplace job-specific verbal reasoning assessment** - how carefully you read and interpret written material such as data ethics guidance, project emails, standards documents, and analysis reports.
4. **Workplace job-specific situational judgement assessment** - how you handle realistic workplace dilemmas involving your team, your users, and your stakeholders.

Each section explains what the assessment measures, maps it to the specific skills in your role profile (such as applied maths and statistics, data engineering, data ethics and privacy, and programming and build), and then gives you a generous set of practice questions with full worked answers. Each section finishes with preparation tips and common pitfalls to avoid.

Here is how to get the most from this guide. First, read each "About this assessment" section so you understand the format. Then try the practice questions honestly, without peeking at the answers. Check your reasoning against the explanations, not just your final answer - the reasoning is where the learning happens. Finally, use the preparation tips for self-reflection: notice which question types feel comfortable and which feel harder, and focus your practice there.

Remember: as an associate, you are at the start of your data science journey, and nobody expects perfection. Curiosity, care, and steady practice are exactly the qualities your role profile asks for. Take your time, be kind to yourself, and enjoy the challenge. Let's begin!

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive ability assessment is a targeted psychometric test that measures the exact mental processes you need in your role. Unlike a general intelligence test, it uses practical workplace scenarios and data formats drawn from the real job - in your case, the datasets, scripts, model outputs, dashboards, and analytical artefacts that an associate data scientist handles every day in a UK government department.

These assessments are usually delivered online and timed, typically lasting 15 to 30 minutes. Questions mimic everyday tasks: spotting a pattern in a sequence of data quality checks, finding the logical flaw in an analytical conclusion, prioritising a set of competing tasks, or diagnosing why a data pipeline produced an odd result. Your answers are scored objectively and compared against a benchmark group, and modern platforms often report both your speed and your accuracy rather than a single number. Questions used in real recruitment are carefully validated so that they predict job performance fairly and without bias.

Why does this matter for you? Because data science is, at heart, structured thinking about messy information. Your role profile says you will "be inquisitive", "explore and visualise data", "find patterns in data and transform them into organisational insight", and "make recommendations to address complex problems". Every one of those duties depends on the mental skills this assessment measures: pattern recognition, logical deduction, careful error checking, sensible prioritisation, and step-by-step problem solving. Practising these skills makes you a stronger data scientist as well as a stronger test-taker - that is a genuinely good deal!

### What it measures for your role

Here is how the main cognitive dimensions map onto the specific skills named in your role profile:

- **Pattern recognition** maps to your skill in **Applied maths, statistics and scientific practices** - applying exploratory data analysis to a dataset means noticing trends, outliers, and structures, and to your duty to "find patterns in data and transform them into organisational insight".
- **Logical deduction** maps to **Applied maths, statistics and scientific practices** (statistical testing and reaching "accurate and reliable conclusions") and to **Data science innovation** - asking good questions requires reasoning about what follows from the evidence and what does not.
- **Error checking** maps to **Data engineering** - recognising "the processes and tools for cleansing and preparing data" and putting "reusable processes and checks in place" - and to **Programming and build (data science)**, where you "write and test scripts".
- **Prioritisation** maps to **Understanding product delivery** - managing "your contribution to tasks to fit in with the work of your wider team" and being aware of delivery methods such as Agile.
- **Problem solving** maps to **Delivering business impact** - collaborating "to help identify user needs and develop and deliver data science products" - and to **Developing data science capability**, using techniques such as machine learning to build reports, models, and dashboards.
- **Rule application** also touches your **Data ethics and privacy** skill, where you apply "fundamental principles of data ethics and privacy in your work under supervision".

### Practice questions

Work through these at your own pace first, then try them again under time pressure (about 90 seconds each). Full explanations follow each question.

#### Question 1 (easy) - Pattern recognition in data quality checks

You run a daily automated quality check on a benefits-application dataset. The check reports the number of records failing validation each day:

Monday: 12, Tuesday: 24, Wednesday: 48, Thursday: 96, Friday: ?

If the pattern continues, how many failing records would you expect on Friday?

- A) 120
- B) 144
- C) 192
- D) 240

**Correct answer: C) 192**

**Explanation:** Each day's count is double the previous day's: 12 → 24 → 48 → 96. Doubling 96 gives 192. In real work, a doubling pattern like this is a red flag - it suggests something systematic (perhaps a broken upstream feed) rather than random noise, and an inquisitive associate data scientist would investigate rather than just report the number. Recognising the type of growth (multiplicative, not additive) is the key skill here.

#### Question 2 (easy) - Logical deduction from analysis rules

Your team's analytical standards say: "Every model used to inform a ministerial decision must be peer reviewed. Every peer-reviewed model must have documented performance metrics."

Model X informed a ministerial decision last month. Which statement must be true?

- A) Model X has documented performance metrics.
- B) Model X was built using machine learning.
- C) Model X was reviewed by two people.
- D) Model X is still in use.

**Correct answer: A) Model X has documented performance metrics.**

**Explanation:** Follow the chain of rules step by step. Model X informed a ministerial decision, so by the first rule it must be peer reviewed. Because it is peer reviewed, by the second rule it must have documented performance metrics. Options B, C, and D introduce details the rules never mention - the rules say nothing about machine learning, the number of reviewers, or current use. Deduction means accepting only what the stated rules force to be true, which mirrors how you should read analytical governance standards in your department.

#### Question 3 (easy) - Error checking a script output

Your Python script should output one summary row per region, for nine English regions. A colleague runs it and gets this list of row labels:

North East, North West, Yorkshire and the Humber, East Midlands, West Midlands, East of England, London, South East, South West, London

What is wrong with the output?

- A) A region is missing.
- B) One region appears twice.
- C) The regions are in the wrong order.
- D) There are only eight rows.

**Correct answer: B) One region appears twice.**

**Explanation:** Count and scan carefully: there are ten labels, and "London" appears both seventh and tenth. All nine regions are present, so nothing is missing; order was never specified as a requirement. Duplicated grouping labels usually mean a join or concatenation bug in the script - exactly the kind of defect that your "write and test scripts" skill exists to catch. In an assessment, counting items before judging them takes five seconds and prevents careless mistakes.

#### Question 4 (moderate) - Sequence logic in model versioning

Your team names model versions using this pattern: v1.0, v1.1, v1.2, v2.0, v2.1, v2.2, v3.0, ...

A major retrain resets the minor number to zero and increases the major number; a small tweak increases the minor number. The current version is v4.1. The team plans one small tweak, then a major retrain, then another small tweak. What will the final version be?

- A) v4.3
- B) v5.0
- C) v5.1
- D) v6.1

**Correct answer: C) v5.1**

**Explanation:** Apply the rules one change at a time. Start at v4.1. A small tweak increases the minor number: v4.2. A major retrain increases the major number and resets the minor: v5.0. Another small tweak: v5.1. The most common error is doing the operations out of order or forgetting the reset. This mirrors real collaborative codebase work - your role profile expects you to "collaborate on shared codebases, using a variety of methodologies", and versioning discipline is part of that.

#### Question 5 (moderate) - Prioritisation under Agile delivery

It is Monday morning in your two-week sprint. You have four tasks:

1. Fix a data pipeline failure that is blocking a teammate's dashboard work today.
2. Prepare exploratory analysis for a show-and-tell on Friday.
3. Refactor an old script to improve readability (no deadline).
4. Respond to a data ethics query from your supervisor about a dataset you used (requested by Wednesday).

Which order of priority is most sensible?

- A) 2, 4, 1, 3
- B) 1, 4, 2, 3
- C) 3, 1, 2, 4
- D) 1, 2, 3, 4

**Correct answer: B) 1, 4, 2, 3**

**Explanation:** The pipeline failure blocks a colleague today, so unblocking others comes first - Agile teams prioritise flow of the whole team over individual tasks, and your role asks you to "manage your contribution to tasks to fit in with the work of your wider team". The ethics query has a firm Wednesday deadline and concerns responsible data use, a core professional obligation, so it comes second. The Friday show-and-tell is important but has more slack. The refactor has no deadline, so it comes last. Option D looks tidy but leaves the time-boxed ethics query dangerously late.

#### Question 6 (moderate) - Spotting a flawed conclusion

A colleague presents this finding: "Departments that adopted our new forecasting dashboard had 20% fewer budget overruns than departments that did not. Therefore the dashboard reduces budget overruns."

What is the strongest logical objection?

- A) 20% is too small a difference to matter.
- B) The comparison does not account for the possibility that better-managed departments were more likely to adopt the dashboard in the first place.
- C) Budget overruns are impossible to measure accurately.
- D) The dashboard should have been tested for longer.

**Correct answer: B)**

**Explanation:** This is a classic confound (selection effect): departments chose whether to adopt, so adopters may differ systematically from non-adopters - perhaps departments with stronger financial management adopted new tools sooner, and their stronger management, not the dashboard, explains the fewer overruns. Options A and D are judgement calls, not logical flaws; option C is an overstatement. Distinguishing correlation from causation is central to reaching the "accurate and reliable conclusions" your applied statistics skill demands, and assessments love this distinction.

#### Question 7 (moderate) - Error checking a data dictionary

A data dictionary states: "Column `age_band` contains one of five values: 16-24, 25-34, 35-49, 50-64, 65+." You profile the live data and find these distinct values: 16-24, 25-34, 35-49, 50-64, 65+, Unknown, 25-34 (with a trailing space).

How many data quality issues does this reveal?

- A) None - the data matches the dictionary.
- B) One - an undocumented "Unknown" value.
- C) Two - an undocumented "Unknown" value, and a duplicate category caused by a trailing space.
- D) Three - the issues in C plus a missing category.

**Correct answer: C)**

**Explanation:** Compare the observed values against the documented set. "Unknown" is not in the dictionary: issue one. "25-34 " with a trailing space is technically a different string from "25-34", so grouping by this column would split one real category into two: issue two. All five documented values are present, so nothing is missing and option D overcounts. Trailing-space bugs are a staple of data cleansing - your data engineering skill of recognising "the processes and tools for cleansing and preparing data" is exactly about catching these before they poison an analysis.

#### Question 8 (moderate) - Logical deduction about pipeline dependencies

Your pipeline has four steps. Step B needs the output of Step A. Step C needs the output of Step B. Step D needs the outputs of both Step A and Step C. This morning Step B failed, but Steps A, C, and D all reported "success".

What should you conclude?

- A) Everything downstream is fine because C and D reported success.
- B) The success reports for C and D are suspicious: C cannot have run correctly on fresh data if B failed, so C and D probably used stale or incomplete inputs.
- C) Step A must also have failed.
- D) Step D failed silently.

**Correct answer: B)**

**Explanation:** Reason through the dependency chain. C depends on B; if B failed, C had no fresh input, so C's "success" most likely means it ran on yesterday's leftover output or on an empty file - a silent data integrity problem. D in turn consumed C's suspect output. Option A trusts status flags over logic; options C and D assert failures we have no evidence for. This is fault diagnosis applied to data engineering: the assessment skill is holding a small dependency graph in your head and asking "what does this failure imply downstream?"

#### Question 9 (moderate) - Rule application in data ethics

Your department's data ethics guidance includes these rules: (1) Personal data may only be used for the purpose for which it was collected. (2) Any new use of personal data requires a documented ethics review. (3) Aggregated, anonymised statistics are not personal data.

Your team collected postcode-level service usage data to improve appointment scheduling. A policy colleague now asks you to use the same individual-level records to profile which named users are "high demand". Which action best follows the rules?

- A) Do the profiling - the data already exists, so no review is needed.
- B) Refuse outright and delete the dataset.
- C) Flag that this is a new use of personal data, so it needs a documented ethics review before any work starts, and raise it through the appropriate channel.
- D) Anonymise the names afterwards, once the profiling is done.

**Correct answer: C)**

**Explanation:** Profiling named individuals for a new purpose is clearly a "new use" under rule 2, so a documented ethics review must happen first - not after the work (which rules out A and D; anonymising after profiling does not undo the misuse). Option B overreacts: the rules do not require deletion, and the original scheduling use remains legitimate. Your role profile says you should "apply fundamental principles of data ethics and privacy in your work under supervision" and "share data ethics and privacy risks through appropriate channels" - option C does both. Cognitive assessments often dress rule-application logic in ethics scenarios exactly like this.

#### Question 10 (hard) - Pattern recognition in model performance drift

You track a classification model's weekly accuracy on fresh data:

Week 1: 91%, Week 2: 90%, Week 3: 91%, Week 4: 90%, Week 5: 91%, Week 6: 86%, Week 7: 82%, Week 8: 78%

Which description best fits this pattern?

- A) Random noise around a stable level throughout.
- B) A stable level for five weeks, followed by a steady decline of roughly four percentage points per week.
- C) A gradual decline from week 1.
- D) A one-off dip in week 6 followed by recovery.

**Correct answer: B)**

**Explanation:** Weeks 1-5 oscillate tightly between 90% and 91% - that is stability with minor noise. From week 6, accuracy falls 86 → 82 → 78, a consistent drop of about 4 points per week with no recovery. Option C is wrong because the early weeks show no decline; option D is wrong because the decline continues after week 6. In practice this pattern suggests data drift or an upstream change around week 6 - your model validation skill ("understand and use different performance and accuracy metrics for model validation") includes noticing when a metric's behaviour changes character, not just its level.

#### Question 11 (hard) - Multi-step problem solving with constraints

You must schedule three pipeline jobs on a shared server tonight. Job P takes 2 hours and must finish before Job Q starts. Job Q takes 3 hours. Job R takes 4 hours and can run any time, but the server can only run one job at a time. The server window opens at 20:00 and closes at 06:00. The output of Q must be available by 04:00 for an overnight report.

Which schedule works?

- A) P 20:00-22:00, Q 22:00-01:00, R 01:00-05:00
- B) R 20:00-00:00, P 00:00-02:00, Q 02:00-05:00
- C) Q 20:00-23:00, P 23:00-01:00, R 01:00-05:00
- D) P 20:00-22:00, R 22:00-02:00, Q 02:00-05:00

**Correct answer: A)**

**Explanation:** Check each constraint methodically. Option A: P finishes 22:00 before Q starts - good; Q finishes 01:00, before the 04:00 deadline - good; R finishes 05:00, before 06:00 - good. All constraints satisfied. Option B: Q finishes at 05:00, missing the 04:00 deadline. Option C: Q runs before P, violating the ordering rule. Option D: Q finishes at 05:00, again missing 04:00. The skill is disciplined constraint-checking - the same habit you use when sequencing data preparation, model training, and reporting steps so your outputs "fit in with the work of your wider team".

#### Question 12 (hard) - Diagnosing an anomalous analytical result

Your exploratory analysis shows that average appointment waiting time dropped from 15 days to 3 days in March. Before reporting this as an improvement, you check four facts:

1. In March, the booking system migrated to a new platform.
2. The new platform records waiting time in weeks, not days, for some records.
3. Appointment volumes in March were similar to February.
4. No new staff were hired.

Which fact most plausibly explains the drop and should be investigated first?

- A) Fact 1 alone - migrations always improve performance.
- B) Fact 2 - if some March records store weeks in a field read as days, the computed average would fall dramatically without any real change.
- C) Fact 3 - stable volumes prove the improvement is real.
- D) Fact 4 - staffing is unrelated, so the drop must be genuine.

**Correct answer: B)**

**Explanation:** A five-fold improvement with no change in volume or staffing is extraordinary, and extraordinary results demand a data-definition check first. If a "3" in the new platform means 3 weeks (21 days) but your script reads it as 3 days, the average collapses artificially. Fact 1 provides the mechanism (the migration) and fact 2 the specific defect. Options C and D mistake "no obvious alternative cause" for confirmation. This is exploratory data analysis done properly: your applied statistics skill of reaching "accurate and reliable conclusions" starts with distrusting results that look too good to be true.

#### Question 13 (hard) - Logical consistency across statements

Three teammates describe the same dataset:

- Amir: "Every record has a valid National Insurance format in the NI field."
- Beth: "At least one record has a blank NI field."
- Chloe: "If a record has a blank NI field, it was created before 2020."

Which combination is possible?

- A) All three statements are true.
- B) Amir and Beth are both true.
- C) Beth and Chloe are both true.
- D) None - Beth always contradicts Chloe.

**Correct answer: C)**

**Explanation:** Amir says every record has a valid (therefore non-blank) NI value; Beth says at least one is blank. These directly contradict each other, so A and B are impossible. Beth and Chloe are compatible: there can be a blank record (satisfying Beth) that was created before 2020 (satisfying Chloe's conditional). Option D is wrong because Chloe's statement is an "if...then" claim - it does not deny that blanks exist; it only constrains when they were created. Reading conditionals precisely is essential when interpreting validation rules and data quality reports.

#### Question 14 (moderate) - Prioritising exploration questions

Your product manager asks you to explore a new dataset of digital service feedback and gives you one day. Which sequence of steps is the most effective use of the day?

- A) Build a machine learning model immediately to predict satisfaction.
- B) Profile the data (size, columns, missing values, duplicates), then explore distributions and simple relationships, then summarise the two or three most decision-relevant findings for the product manager.
- C) Write a full data cleaning pipeline with unit tests before looking at any values.
- D) Produce twenty visualisations covering every column and send them all without commentary.

**Correct answer: B)**

**Explanation:** Exploratory data analysis follows a sensible order: understand what you have (profiling), then look for structure (distributions, relationships), then communicate what matters, "tailored to your audience" as your Delivering business impact skill puts it. Option A models before understanding the data - a classic junior mistake. Option C invests in engineering before knowing whether the data merits it. Option D produces output without insight; twenty uncurated charts transfer the analytical burden to the reader. The assessment skill here is matching effort to purpose under a time constraint.

#### Question 15 (hard) - Deduction from tool behaviour

Your organisation provides two statistical tools. Tool S can read data only from the secure cloud store. Tool T can read from both the cloud store and the on-premise database, but cannot produce interactive dashboards. All interactive dashboards in your team are produced by Tool S. This morning you are handed an interactive dashboard built from on-premise data.

What must be true?

- A) The dashboard was built with Tool T.
- B) The on-premise data must have been copied or migrated to the secure cloud store before the dashboard was built.
- C) The dashboard breaches security policy.
- D) Tool S was upgraded to read on-premise data.

**Correct answer: B)**

**Explanation:** Work through the constraints. The artefact is an interactive dashboard, and all such dashboards come from Tool S, so Tool S built it (ruling out A, since Tool T cannot produce interactive dashboards anyway). Tool S reads only from the cloud store, yet the underlying data originated on-premise - so the data must have moved to the cloud store at some point. That is the only conclusion the given facts force. Option C assumes a policy breach nowhere stated - moving data to the cloud store may be entirely routine. Option D invents an upgrade the facts do not mention; the stated capabilities are the rules of the puzzle. This mirrors your data engineering skill of using "different architectures, including cloud and on-premise" and reasoning about how data flows between them.

### Preparation tips

- **Practise with your real artefacts.** Open a dataset you worked on recently and quiz yourself: what patterns exist? What could be wrong with it? What would I check first? This builds the same mental muscles the test measures.
- **Do a little, often.** Two or three questions a day for a fortnight beats a single cramming session. Cognitive speed improves with regular light practice.
- **Verbalise your reasoning.** After each practice question, say out loud why the right answer is right. If you can explain it, you have truly learned it - and explaining analysis clearly is literally part of your job description.
- **Time yourself gradually.** Start untimed, then introduce a 90-second limit per question. Speed comes after accuracy, not before.
- **Rest properly before the real thing.** Cognitive tests are sensitive to tiredness. A good night's sleep is worth more than a late-night revision session, honestly!
- **Don't panic about hard questions.** As an associate, you are compared against a realistic benchmark, not perfection. Skipping one brutal question to answer three easier ones is smart strategy, not failure.

### Common pitfalls

- **Rushing the reading.** Most wrong answers come from misreading the setup, not from weak reasoning. Read the scenario once slowly before touching the options.
- **Bringing outside assumptions.** Answer using only the rules and data given, even when you know real-world exceptions. The test measures deduction from the material provided.
- **Getting stuck on one question.** A single time-sink question can cost you three easier marks. Flag it, move on, return if time allows.
- **Ignoring "counting" checks.** Before judging a list or table, count the items. Duplicates and omissions are deliberately hidden in plain sight.
- **Trusting status labels over logic.** As in the pipeline question, a "success" flag does not guarantee correct data. The test rewards candidates who reason about what must be true, not what is merely reported.
- **Confusing plausible with proven.** An answer that could be true is not the same as one that must be true. Reserve certainty for what the given rules force.


## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment evaluates your ability to analyse, interpret, and make sound decisions using numerical data. Rather than abstract formulas, it uses realistic business numbers: tables, percentages, ratios, budgets, capacity figures, and performance metrics - the same material that flows through an associate data scientist's day in a UK government department.

The format is friendly once you know what to expect. Questions present real-world data - a table of model performance metrics, a compute budget breakdown, a survey response summary - and ask you to extract the right figures and apply basic maths: percentages, ratios, rates, averages, and simple projections. Most assessments allow or provide an on-screen calculator, because they prioritise interpretation over mental arithmetic. There is usually a strict time limit, often around a minute to ninety seconds per question, which rewards quick, accurate data extraction rather than complicated calculation.

Why does this matter for your role? Numbers are your raw material. Your role profile expects you to "prepare and manipulate data, and perform analytics", to apply "exploratory data analysis and statistical testing", and to "understand and use different performance and accuracy metrics for model validation". Every model you validate, every dashboard you build, and every recommendation you make rests on getting percentages, rates, and comparisons right. A misplaced decimal in a briefing to a policy team is not just a test error - it can misdirect a real decision. The good news: the arithmetic itself is never harder than GCSE level. The skill being tested is care, method, and reading the data correctly under time pressure - all things that improve quickly with practice.

### What it measures for your role

- **Percentages and rates** map to **Applied maths, statistics and scientific practices**: accuracy, precision, recall, error rates, and response rates are all percentages, and "different performance and accuracy metrics for model validation" are the bread and butter of this section.
- **Tables and data extraction** map to your duty to "explore and visualise data" and to **Data engineering** - reading a data profile or capacity table correctly is step one of cleansing and preparing data.
- **Ratios and proportions** map to **Applied maths, statistics and scientific practices** - class balance in a training set, sampling fractions, and train/test splits are all ratios.
- **Budgets and costs** map to **Delivering business impact** - understanding "the organisation and the benefits of data science" includes knowing what compute, licences, and analyst time cost, and whether a data science product pays its way.
- **Capacity and throughput figures** map to **Data engineering** (pipeline volumes, storage) and **Understanding product delivery** (sprint capacity, fitting your contribution to the team's work).
- **Trend interpretation** maps to your duty to "find patterns in data and transform them into organisational insight".

### Practice questions

A calculator is allowed for all questions. Try to show your own working before checking the explanation - the working is where marks (and habits) are made.

#### Question 1 (easy) - Percentage of records cleaned

Your team receives 48,000 citizen feedback records. During cleansing you remove 2,880 records as duplicates or spam. What percentage of the original records remains?

- A) 92%
- B) 94%
- C) 95%
- D) 96%

**Correct answer: B) 94%**

**Explanation:** Removed fraction = 2,880 ÷ 48,000 = 0.06 = 6%. Remaining = 100% − 6% = 94%. A quick sanity check: 10% of 48,000 is 4,800, so 2,880 is clearly a bit more than half of that, i.e. around 6% - estimation catches slips before they cost you. Reporting how much data survived cleansing is a routine part of preparing and manipulating data.

#### Question 2 (easy) - Reading a simple metrics table

Your classification model produces these results on a test set of 1,000 cases:

| Outcome | Count |
|---|---|
| Correctly flagged (true positives) | 150 |
| Incorrectly flagged (false positives) | 50 |
| Correctly passed (true negatives) | 750 |
| Missed (false negatives) | 50 |

What is the model's overall accuracy?

- A) 75%
- B) 80%
- C) 90%
- D) 95%

**Correct answer: C) 90%**

**Explanation:** Accuracy = correct predictions ÷ all predictions = (150 + 750) ÷ 1,000 = 900 ÷ 1,000 = 90%. The wrong options come from common misreadings: 75% is just the true negatives; 80% mixes categories. Knowing exactly which cells of a confusion table feed which metric is core to your model validation skill - and assessments test precisely whether you pick the right cells under time pressure.

#### Question 3 (easy) - Ratio of a train/test split

You have 30,000 labelled records and use an 80:20 train/test split. How many records are in the test set?

- A) 4,000
- B) 5,000
- C) 6,000
- D) 8,000

**Correct answer: C) 6,000**

**Explanation:** The test share is 20% of 30,000 = 0.20 × 30,000 = 6,000. Equivalently, the ratio 80:20 means 4 parts train to 1 part test; 30,000 ÷ 5 parts = 6,000 per part, and the test set is one part. Ratios reappear constantly in data science - class balance, sampling, splits - so being able to switch between "percentage" and "parts" views is a small skill with big returns.

#### Question 4 (moderate) - Precision from a confusion table

Using the same table as Question 2 (150 true positives, 50 false positives, 750 true negatives, 50 false negatives): what is the model's precision (the proportion of flagged cases that were correctly flagged)?

- A) 60%
- B) 75%
- C) 80%
- D) 90%

**Correct answer: B) 75%**

**Explanation:** Precision = true positives ÷ all flagged = 150 ÷ (150 + 50) = 150 ÷ 200 = 0.75 = 75%. Notice how different this is from the 90% accuracy in Question 2 - same model, same data, different metric answering a different question. Your role profile explicitly asks you to "understand and use different performance and accuracy metrics", and this contrast is exactly why: a stakeholder told "the model is 90% accurate" might be shocked that a quarter of its alerts are wrong. Recall, for interest, is 150 ÷ (150 + 50 missed) = 75% too, in this balanced example.

#### Question 5 (moderate) - Percentage change in pipeline volume

Your nightly data pipeline processed 1.25 million records in June and 1.45 million in July. What is the percentage increase, to the nearest whole percent?

- A) 14%
- B) 16%
- C) 18%
- D) 20%

**Correct answer: B) 16%**

**Explanation:** Increase = 1.45m − 1.25m = 0.20m. Percentage increase = 0.20 ÷ 1.25 = 0.16 = 16%. The classic trap is dividing by the new value (0.20 ÷ 1.45 ≈ 13.8%, luring you to option A). Percentage change is always measured against the starting value. Monitoring volume growth like this feeds capacity planning - a data engineering conversation you will contribute numbers to.

#### Question 6 (moderate) - Compute budget allocation

Your team's quarterly cloud compute budget is £18,000, allocated as: model training 45%, data storage 25%, dashboards and reporting 20%, experimentation 10%. Mid-quarter, storage costs are already £4,200. By how much is storage over or under its full-quarter allocation?

- A) £300 under
- B) £300 over
- C) £700 under
- D) £750 over

**Correct answer: A) £300 under**

**Explanation:** Storage allocation = 25% of £18,000 = 0.25 × 18,000 = £4,500. Spend so far is £4,200, which is £4,500 − £4,200 = £300 below the full-quarter allocation. (Whether that is comfortable depends on it being mid-quarter - at the current pace storage would hit £8,400, well over budget, which is the kind of insight a good analyst adds!) The tested skill is a clean two-step: compute the allocation, then compare. Budget questions reward writing both numbers down before subtracting.

#### Question 7 (moderate) - Survey response rates across groups

A user research survey about a new digital service was sent to four groups:

| Group | Invitations sent | Responses received |
|---|---|---|
| Working-age adults | 5,000 | 1,100 |
| Pensioners | 2,000 | 560 |
| Students | 1,500 | 270 |
| Small business owners | 500 | 130 |

Which group had the highest response rate?

- A) Working-age adults
- B) Pensioners
- C) Students
- D) Small business owners

**Correct answer: B) Pensioners**

**Explanation:** Compute each rate in turn: working-age adults 1,100 ÷ 5,000 = 22%; pensioners 560 ÷ 2,000 = 28%; students 270 ÷ 1,500 = 18%; small business owners 130 ÷ 500 = 26%. Pensioners top the list at 28%. The trap is option A: working-age adults gave by far the most responses in absolute terms (1,100), but a count is not a rate. Rates and counts answer different questions, and confusing them is the single most common error when analysing survey and service-usage data. When you present response data to a user researcher or product manager, quoting both the rate and the base size ("28% of 2,000 invited") is good statistical practice - small bases make rates less reliable, a point your statistical testing skill should make you comfortable raising.

#### Question 8 (moderate) - Weighted average processing time

Your pipeline has three stages. Stage 1 handles 60% of records at 2 seconds each; Stage 2 handles 30% at 5 seconds each; Stage 3 handles 10% at 12 seconds each. What is the average processing time per record?

- A) 3.9 seconds
- B) 4.5 seconds
- C) 5.2 seconds
- D) 6.3 seconds

**Correct answer: A) 3.9 seconds**

**Explanation:** Weighted average = (0.60 × 2) + (0.30 × 5) + (0.10 × 12) = 1.2 + 1.5 + 1.2 = 3.9 seconds. The tempting error is the simple average (2 + 5 + 12) ÷ 3 = 6.3 seconds (option D), which ignores that most records take the fast path. Weighted averages appear everywhere in your work - blended error rates across data sources, average cost per prediction, mean satisfaction across user groups of different sizes - so make the weights-first habit automatic.

#### Question 9 (moderate) - Storage capacity projection

Your project's cloud storage currently holds 3.2 TB and grows by 0.4 TB per month. The allocated capacity is 6.0 TB. Assuming steady growth, in how many whole months will the storage exceed its allocated capacity?

- A) 6 months
- B) 7 months
- C) 8 months
- D) 9 months

**Correct answer: C) 8 months**

**Explanation:** Headroom = 6.0 − 3.2 = 2.8 TB. Months to fill = 2.8 ÷ 0.4 = 7 months, at which point storage is exactly 6.0 TB - at capacity but not yet over. It exceeds capacity in month 8 (6.4 TB). The subtlety is the word "exceed": reaching a limit and passing it are different events, and option B is the trap for solvers who stop at the division. Reading the question's exact requirement is half the mark. Projections like this are how you give early warning in capacity conversations with data engineering colleagues - your role includes using cloud architectures, and cloud bills reward foresight.

#### Question 10 (hard) - Cost per prediction comparison

Two model deployment options are costed for a service handling 200,000 predictions per month:

| Option | Fixed monthly cost | Cost per 1,000 predictions |
|---|---|---|
| Shared platform | £500 | £8 |
| Dedicated server | £1,600 | £2 |

Which option is cheaper at 200,000 predictions per month, and by how much?

- A) Shared platform, by £100
- B) Dedicated server, by £100
- C) Dedicated server, by £300
- D) Shared platform, by £300

**Correct answer: B) Dedicated server, by £100**

**Explanation:** Work in blocks of 1,000 predictions: 200,000 predictions = 200 blocks. Shared platform: £500 + (200 × £8) = £500 + £1,600 = £2,100. Dedicated server: £1,600 + (200 × £2) = £1,600 + £400 = £2,000. The dedicated server is cheaper by £2,100 − £2,000 = £100. Two transferable skills live in this question. First, fixed-plus-variable costing: total cost = fixed cost + (volume × unit cost), the structure behind most cloud pricing. Second, break-even thinking: setting 500 + 8v = 1,600 + 2v gives 6v = 1,100, so v ≈ 183.3 blocks - the options cost the same at roughly 183,000 predictions, and above that the dedicated server always wins because its marginal cost is lower. Mentioning the break-even point in a write-up turns a bare "cheaper" verdict into genuine decision support - exactly the cost-benefit framing your Delivering business impact skill calls for.

#### Question 11 (hard) - Interpreting A/B test results

An A/B test on a government service's new form design shows:

| Version | Users | Completed the form |
|---|---|---|
| A (current) | 12,000 | 8,400 |
| B (new) | 8,000 | 6,000 |

By how many percentage points does version B's completion rate exceed version A's?

- A) 3 percentage points
- B) 5 percentage points
- C) 7 percentage points
- D) B does not exceed A

**Correct answer: B) 5 percentage points**

**Explanation:** Rate A = 8,400 ÷ 12,000 = 70%. Rate B = 6,000 ÷ 8,000 = 75%. Difference = 75% − 70% = 5 percentage points. Two traps: first, comparing raw counts (8,400 > 6,000) suggests A is "better", but the groups are different sizes; second, the difference between percentages is expressed in percentage points, not percent - saying "5% better" would technically mean 70% × 1.05 = 73.5%. Precise language about percentages versus percentage points marks you out as someone who can "present and communicate effectively", as your role level requires. In real work you would also ask about statistical significance before recommending version B - good instinct to mention in any write-up.

#### Question 12 (hard) - Multi-step: sampling and error estimation

You need a quality-assurance sample from 250,000 processed records. The plan: sample 2% of records; you expect around 1.5% of sampled records to contain errors. Approximately how many erroneous records do you expect to find in the sample?

- A) 50
- B) 75
- C) 100
- D) 150

**Correct answer: B) 75**

**Explanation:** Step 1: sample size = 2% of 250,000 = 0.02 × 250,000 = 5,000 records. Step 2: expected errors = 1.5% of 5,000 = 0.015 × 5,000 = 75. The traps are taking 1.5% of the full 250,000 (= 3,750, not offered, but its "shape" lures people to larger options) or muddling which percentage applies to which base. Multi-step percentage problems are best handled by writing each intermediate result down with its units ("5,000 sampled records") before moving on - a habit that also makes your analysis scripts easier for teammates to review on your shared codebase.

#### Question 13 (hard) - Reading a two-way table of model errors

Your team audits a model's false positive rates across demographic groups to check fairness:

| Group | Cases processed | False positives |
|---|---|---|
| Group W | 40,000 | 800 |
| Group X | 25,000 | 625 |
| Group Y | 10,000 | 300 |
| Group Z | 5,000 | 100 |

Which group experiences the highest false positive rate, and what is it?

- A) Group W, 2.0%
- B) Group X, 2.5%
- C) Group Y, 3.0%
- D) Group Z, 2.0%

**Correct answer: C) Group Y, 3.0%**

**Explanation:** Rates: W = 800 ÷ 40,000 = 2.0%; X = 625 ÷ 25,000 = 2.5%; Y = 300 ÷ 10,000 = 3.0%; Z = 100 ÷ 5,000 = 2.0%. Group Y's rate is highest even though Group W has the most false positives in absolute terms (800). This is not just arithmetic - it is the numeric backbone of data ethics. A model that errs 50% more often for one group than another (3.0% versus 2.0%) raises a fairness risk that your Data ethics and privacy skill says you should "share through appropriate channels". Numeric fluency and ethical practice meet exactly here, which is why fairness auditing tables appear in role-specific numeric tests for data scientists.

#### Question 14 (hard) - Percentage of a percentage: pipeline success rates

Your data pipeline has two stages. Stage 1 (ingestion) succeeds for 96% of records; the failures are dropped. Stage 2 (transformation) succeeds for 92.5% of the records it receives. What percentage of the original records make it through both stages?

- A) 88.5%
- B) 88.8%
- C) 90.2%
- D) 94.25%

**Correct answer: B) 88.8%**

**Explanation:** Chained success = 96% × 92.5% = 0.96 × 0.925 = 0.888 = 88.8%. The classic error is subtracting the failure rates from 100 (100 − 4 − 7.5 = 88.5%, option A) - close enough to feel right, wrong enough to fail an audit. Multiplying survival rates, not subtracting failure rates, is correct because Stage 2's percentage applies only to what survived Stage 1. End-to-end yield calculations like this belong in the "reusable processes and checks" your data engineering skill expects you to put in place: a daily figure of records-in versus records-out catches silent data loss early.

#### Question 15 (moderate) - Averages and outliers in service data

Five local offices report their average call-handling times (in minutes): 4, 5, 5, 6, and 20. A stakeholder asks for "the typical handling time". Which figure and reasoning are most appropriate?

- A) 8 minutes - the mean of the five values, because the mean is always the best summary.
- B) 5 minutes - the median, because the value of 20 is an outlier that drags the mean well above what most offices experience.
- C) 20 minutes - the maximum, to be safe.
- D) 4 minutes - the minimum, to show the service at its best.

**Correct answer: B) 5 minutes**

**Explanation:** The mean is (4 + 5 + 5 + 6 + 20) ÷ 5 = 40 ÷ 5 = 8 minutes, but four of the five offices handle calls in 4-6 minutes; the single value of 20 pulls the mean up to a figure that describes no actual office. The median (middle value when sorted) is 5, which represents the typical experience far better. Options C and D answer different questions ("worst case" and "best case"), not "typical". Choosing summary statistics that honestly represent the data - and flagging the outlier office for investigation, since something interesting or broken is happening there - is exploratory data analysis in miniature, and precisely the judgement your applied statistics skill develops. In a briefing, the strongest answer reports both: "typically 5 minutes, but one office averages 20 and needs looking into."

#### Question 16 (hard) - Sprint capacity arithmetic

Your Agile team has a two-week sprint with 4 team members, each nominally available 8 days of the sprint after ceremonies and support duties. One member is on leave for 3 days, and you personally must reserve 25% of your own 8 days for CPD and mandatory training. How many person-days does the team actually have this sprint?

- A) 26 person-days
- B) 27 person-days
- C) 29 person-days
- D) 32 person-days

**Correct answer: B) 27 person-days**

**Explanation:** Start with the nominal total: 4 × 8 = 32 person-days. Subtract the leave: 32 − 3 = 29. Subtract your CPD reservation: 25% of your 8 days = 2 days, so 29 − 2 = 27 person-days. Option D forgets both deductions; option C forgets your CPD time; option A over-deducts by taking 25% of someone else's days too. Two role connections make this more than arithmetic: your Understanding product delivery skill expects you to "manage your contribution to tasks to fit in with the work of your wider team", which starts with honest capacity numbers, and your Developing data science capability skill expects you to "manage your CPD" - protecting learning time in the sprint plan is exactly how associates grow into data scientists.

### Preparation tips

- **Refresh the core four.** Percentages, ratios, averages (including weighted), and rates cover nearly every question. Fifteen minutes of practice a day on these beats hours of advanced maths.
- **Practise with your own metrics.** Take a model or dashboard you have worked on and compute things: accuracy versus precision, month-on-month change, cost per record. Familiar context makes the mechanics stick.
- **Write down intermediate values.** Even with a calculator, jot each step's result and its units. Most errors happen between steps, not within them.
- **Estimate before you calculate.** A rough answer ("about 6%") catches decimal slips instantly. This is a professional habit, not just a test trick.
- **Learn the percentage-point distinction.** Knowing when to say "percentage points" rather than "percent" prevents both test errors and awkward stakeholder corrections.
- **Time-box each question.** Give yourself 90 seconds; if you are stuck, guess, flag, and move on. As an associate you are not expected to finish every question - accuracy on the ones you attempt matters more.
- **Build a personal error log.** After each practice session, note which trap caught you: wrong base, wrong units, misread header, simple slip. Patterns emerge within a week, and targeting your top two error types is the fastest score improvement available.
- **Use your organisation's tools for practice.** Recreate a question's table in the statistical tools available to you - a notebook, a spreadsheet - and verify the answer computationally. Connecting test arithmetic to your working tools reinforces both, and it is a gentle way to sharpen the data manipulation skills your role level expects.

### Common pitfalls

- **Misreading scale qualifiers.** Confusing "in thousands" with raw numbers, or monthly with annual figures, is the most common error in numeric tests. Read table headers and footnotes first.
- **Dividing by the wrong base.** Percentage change uses the original value; precision uses flagged cases; response rate uses invitations sent. Ask "out of what?" before dividing.
- **Comparing counts when the question asks about rates.** Bigger groups produce bigger counts; only rates make groups comparable.
- **Over-calculating.** If options are far apart, estimation answers the question in a third of the time. Save exact arithmetic for close options.
- **Time-sink questions.** One stubborn multi-step problem can cost you three easy marks. Skip and return.
- **Forgetting the exact wording.** "Exceed", "at least", "to the nearest whole percent" - these small words decide between adjacent options. Reread the question line before selecting your answer.
- **Neglecting units and periods.** Mixing seconds with minutes, records with blocks of a thousand, or a monthly figure with a quarterly budget quietly wrecks otherwise correct working. Write units beside every intermediate number - the ten seconds it costs repays itself many times over, in tests and in the analysis scripts your teammates will review.


## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment evaluates how well you understand, analyse, and draw correct conclusions from written workplace information. The passages mirror the exact reading demands of your role: data ethics guidance, analytical standards, project emails, technical documentation, and report extracts, all written in the style you meet in a UK government digital and data environment.

The rules of the game are strict and refreshingly fair. You answer based only on the text provided, ignoring anything you happen to know from outside. Most questions ask you to judge a statement as True (the passage supports it), False (the passage contradicts it), or Cannot Say (the passage gives insufficient information to decide). Some questions are multiple-choice comprehension instead, asking for the best summary or the correct application of a stated rule. Tests are time-pressured - often under a minute per question - which simulates the reality of reading a dense policy email between meetings.

Why does this matter for you? Because an associate data scientist reads for a living more than most people expect. Your role profile asks you to be "aware of ethical considerations" (usually communicated in written guidance), to collaborate on shared codebases (governed by written standards and pull-request comments), to be "aware of project delivery methods" (described in written playbooks), and above all to "present and communicate effectively" - which starts with reading others' words precisely before responding to them. Misreading a data-sharing agreement or an acceptance criterion does not just lose a test mark; it can send a week of analysis in the wrong direction. The happy flip side: careful reading is a completely learnable skill, and the True/False/Cannot Say discipline of "only what the text says" is the same discipline that makes your analytical conclusions reliable.

### What it measures for your role

- **Precise comprehension of rules and conditions** maps to **Data ethics and privacy** - applying "fundamental principles of data ethics and privacy in your work under supervision" means reading guidance documents exactly as written.
- **Distinguishing stated facts from assumptions** maps to **Applied maths, statistics and scientific practices** - reaching "accurate and reliable conclusions" requires knowing what the evidence (or the text) actually establishes.
- **Reading technical documentation** maps to **Data engineering** and **Programming and build (data science)** - tool documentation, pipeline runbooks, and codebase contribution guides are all dense text with consequences.
- **Understanding delivery language** maps to **Understanding product delivery** - sprint notes, acceptance criteria, and delivery-method descriptions must be parsed correctly to "manage your contribution to tasks".
- **Grasping audience and tone** maps to **Delivering business impact** - communicating analysis "tailored to your audience" begins with recognising what a stakeholder's message is really asking for.
- **Learning from written sources** maps to **Data science innovation** and **Developing data science capability** - researching "new data science techniques to support learning" means digesting articles and documentation accurately.

### Practice questions

For each passage, answer using only the information given. Resist your professional knowledge - if the passage does not say it, you cannot use it.

#### Passage A - Data ethics guidance extract

Read this extract from a departmental data ethics framework:

"All analytical projects using personal data must complete an ethics screening questionnaire before data access is granted. Projects assessed as high risk must additionally be reviewed by the Data Ethics Board, which meets monthly. Projects using only anonymised, aggregated data are exempt from the screening questionnaire, although project leads are encouraged to complete it voluntarily. Where a project's risk level changes during delivery, the project lead must notify the ethics team within five working days."

#### Question 1 (easy)

True, False, or Cannot Say: "A project using personal data can begin accessing that data before completing the ethics screening questionnaire."

**Correct answer: False**

**Explanation:** The passage states that such projects "must complete an ethics screening questionnaire before data access is granted". The word "before" makes the sequence mandatory, so the statement directly contradicts the text. Notice the technique: find the exact sentence, match the exact condition. Your answer should rest on the words "before data access is granted", nothing else.

#### Question 2 (easy)

True, False, or Cannot Say: "The Data Ethics Board meets every week."

**Correct answer: False**

**Explanation:** The passage says the Board "meets monthly". Weekly and monthly are directly contradictory, so this is False rather than Cannot Say. A common wobble is thinking "well, maybe they also meet weekly sometimes" - but that adds speculation to the text. The passage asserts a monthly meeting schedule; a claim of weekly meetings contradicts what is written.

#### Question 3 (moderate)

True, False, or Cannot Say: "A project using anonymised, aggregated data that is assessed as high risk must be reviewed by the Data Ethics Board."

**Correct answer: Cannot Say**

**Explanation:** This one is genuinely tricky, so take it slowly. The Board-review rule applies to "projects assessed as high risk", and the passage introduces that rule in the context of projects that complete the screening questionnaire. Anonymised, aggregated projects are exempt from the questionnaire - but the passage never states whether such projects can still be "assessed as high risk" through some other route, nor whether the Board-review rule covers them. The text neither confirms nor denies it, so Cannot Say is correct. This mirrors real governance reading: gaps and ambiguities in guidance are common, and spotting them - rather than papering over them with assumptions - is exactly the risk-sharing instinct your Data ethics and privacy skill asks you to develop.

#### Question 4 (moderate)

True, False, or Cannot Say: "If a medium-risk project becomes high risk halfway through delivery, the project lead must inform the ethics team within five working days."

**Correct answer: True**

**Explanation:** The final sentence covers exactly this: "Where a project's risk level changes during delivery, the project lead must notify the ethics team within five working days." A change from medium to high risk is a change in risk level during delivery, so the rule applies. The statement paraphrases "notify" as "inform" - assessments often reword, and your job is to match meaning, not exact vocabulary. All the load-bearing elements (risk change, during delivery, five working days, project lead's duty) align with the text.

#### Passage B - Email from a delivery manager

Read this email:

"Hi team - quick update ahead of sprint planning. The minister's office has asked for the service usage analysis two weeks earlier than planned, so we need to descope something. My suggestion is that we postpone the dashboard accessibility improvements to next sprint, but I want to hear your views before we decide anything. Also, a reminder that the new starters join on Monday, so please keep some capacity free for onboarding support. Priya has volunteered to lead the code walkthrough. Thanks, Sam."

#### Question 5 (easy)

True, False, or Cannot Say: "Sam has decided to postpone the dashboard accessibility improvements."

**Correct answer: False**

**Explanation:** Sam calls postponement "my suggestion" and explicitly says "I want to hear your views before we decide anything". A suggestion awaiting team input is not a decision, and the email says so in terms. The distinction between a proposal and a decision is one of the most tested nuances in verbal reasoning - and one of the most important in real Agile teamwork, where misreading a suggestion as an instruction can waste a sprint.

#### Question 6 (moderate)

True, False, or Cannot Say: "The service usage analysis deadline has moved because the original analysis contained errors."

**Correct answer: Cannot Say**

**Explanation:** The email gives a reason for the earlier deadline: "The minister's office has asked for the service usage analysis two weeks earlier than planned". It says nothing about errors in any original analysis. Be careful before jumping to False: does "the minister's office asked" actually contradict "because of errors"? No - both could be true at once, since the office might have asked precisely because of errors. The passage neither confirms nor denies the error claim, so Cannot Say is correct. This is the precision habit that protects you from reading motives into stakeholder emails - the text states what was requested, not why.

#### Question 7 (moderate)

Which of the following best summarises the main purpose of Sam's email?

- A) To announce a final decision about descoping the sprint.
- B) To update the team on a deadline change, propose a descoping option for discussion, and flag onboarding needs.
- C) To criticise the minister's office for moving the deadline.
- D) To ask Priya to lead a code walkthrough.

**Correct answer: B)**

**Explanation:** The email does three things: reports the earlier deadline, offers a suggestion explicitly open for discussion, and reminds the team about onboarding (noting Priya has already volunteered - so D describes something settled, not requested). A fails because nothing is decided; C invents a critical tone absent from the text, which is neutral and practical. Summary questions reward identifying all the main moves of a text and rejecting options that capture only a fragment or add emotional colouring. Reading a stakeholder's message for what it actually asks of you is step one of communicating "tailored to your audience".

#### Passage C - Analytical standards document extract

Read this extract from a government analytical standards document:

"Analytical outputs intended for publication must be quality assured by an analyst who was not involved in producing the output. Quality assurance must cover the data sources, the methodology, and the interpretation of results. For outputs produced under urgent timescales, a proportionate quality assurance approach may be agreed with the head of profession, provided the limitations are documented and communicated to users of the output. Machine learning models are considered analytical outputs for the purposes of this standard."

#### Question 8 (moderate)

True, False, or Cannot Say: "An analyst may quality assure a published output that they helped to produce, provided the head of profession agrees."

**Correct answer: False**

**Explanation:** The standard requires QA "by an analyst who was not involved in producing the output" - with no exception attached to that requirement. The head-of-profession provision relates to something different: agreeing "a proportionate quality assurance approach" under urgent timescales. It modifies the depth of QA, not who performs it. Assessments love this trap: an exception clause exists in the passage, so a careless reader assumes it covers everything. Match each exception to the exact rule it modifies - the same care you would use reading a data-sharing agreement.

#### Question 9 (moderate)

True, False, or Cannot Say: "A machine learning model built for publication must have its methodology quality assured."

**Correct answer: True**

**Explanation:** Chain two sentences: machine learning models "are considered analytical outputs for the purposes of this standard", and analytical outputs for publication "must be quality assured" with QA covering "the data sources, the methodology, and the interpretation of results". Together these force the conclusion: a model intended for publication needs methodology QA. Verbal tests at your level often require joining exactly two sentences; practise spotting the definitional sentence ("X counts as Y") that switches a rule on.

#### Question 10 (hard)

True, False, or Cannot Say: "Outputs produced under urgent timescales are exempt from quality assurance."

**Correct answer: False**

**Explanation:** The passage allows "a proportionate quality assurance approach" for urgent outputs - proportionate QA is still QA, and even that lighter approach carries conditions (agreement with the head of profession, documented and communicated limitations). "Proportionate" and "exempt" are very different words, and the statement contradicts the passage's clear intent that some QA always occurs. Reading "may be agreed" as "may be skipped" is the kind of misreading that causes real governance failures, so tests probe it deliberately.

#### Passage D - Technical documentation extract

Read this extract from your team's pipeline runbook:

"The ingestion job runs at 02:00 daily and writes to the staging area. If the source system is unavailable, the job retries every 30 minutes, up to four times, before raising an alert. Transformation jobs must not be started manually while an ingestion retry is in progress. Analysts wishing to rerun a transformation should first check the ingestion status page. Access to the production area requires a change request approved by the data engineering lead, except for read-only access, which is granted to all analysts by default."

#### Question 11 (moderate)

True, False, or Cannot Say: "If the source system is unavailable all night, the ingestion job will raise an alert at approximately 04:00."

**Correct answer: True**

**Explanation:** Walk the timeline: the job runs at 02:00; if the source is unavailable it retries every 30 minutes up to four times - at approximately 02:30, 03:00, 03:30, and 04:00 - and only then raises an alert. If the source stays unavailable throughout, the fourth retry at about 04:00 fails and the alert follows. The word "approximately" in the statement matches the reasonable reading of the schedule. This is verbal reasoning with a light numeric flavour - runbooks often need exactly this combined reading, which is why role-specific tests include it.

#### Question 12 (moderate)

True, False, or Cannot Say: "An analyst needs an approved change request to read data in the production area."

**Correct answer: False**

**Explanation:** The final sentence grants an explicit exception: "except for read-only access, which is granted to all analysts by default". Reading is read-only access, so no change request is needed. The trap is stopping at "Access to the production area requires a change request..." and answering True before reaching the exception. Always read to the end of the sentence - in tests and in runbooks alike, the second half of a sentence can reverse the first half's apparent meaning.

#### Question 13 (hard)

True, False, or Cannot Say: "The staging area is backed up every night."

**Correct answer: Cannot Say**

**Explanation:** The passage mentions the staging area only as the destination of the ingestion job. Backups are never mentioned - not affirmed, not denied. Your operational instinct might whisper "of course staging is backed up" (or "staging areas often aren't!"), but both whispers are outside knowledge, and the discipline of this test is to silence them. Cannot Say is the honest verdict whenever the text is simply silent. This mirrors reading documentation critically: noticing what a runbook does not say is often the most valuable observation an inquisitive associate can raise.

#### Question 14 (hard)

A teammate messages you: "Ingestion failed twice this morning but the third retry succeeded at 03:30. I want to rerun my transformation now." According to the runbook, what is the correct response?

- A) They must wait until tomorrow's 02:00 run before any transformation.
- B) They may rerun the transformation, but should first check the ingestion status page to confirm no retry is in progress.
- C) They need a change request approved by the data engineering lead before rerunning.
- D) They should raise an alert before proceeding.

**Correct answer: B)**

**Explanation:** The runbook's rule is that transformations "must not be started manually while an ingestion retry is in progress" and that analysts "should first check the ingestion status page". The teammate reports the retry succeeded, so no retry should be in progress - but the runbook still prescribes checking the status page before a manual rerun, which is what option B captures. Option A invents a waiting rule; option C misapplies the change-request rule, which governs production access, not transformation reruns; option D misuses alerts, which the passage assigns to the ingestion job itself. Applying written rules to a slightly new situation is precisely the skill of working from shared documentation on a collaborative codebase.

#### Passage E - Extract from an analysis report

Read this extract from a draft report your team is reviewing:

"Uptake of the online renewal service rose from 61% to 74% of all renewals during the pilot year. The largest increases were observed among users aged 35 to 54. Survey respondents most frequently cited 'saving a trip to the post office' as their reason for switching. However, uptake among users aged over 75 remained below 30%, and assisted digital support requests doubled during the same period. The team recommends continuing the phone and in-person channels alongside the online service, and conducting further research with older users before any channel changes are considered."

#### Question 15 (moderate)

True, False, or Cannot Say: "The majority of renewals were completed online by the end of the pilot year."

**Correct answer: True**

**Explanation:** The passage states uptake "rose from 61% to 74% of all renewals during the pilot year". At 74%, online renewals are comfortably a majority (more than 50%) of all renewals - in fact they were already a majority at 61% when the pilot began. The statement is a mathematical consequence of the stated figures, and verbal tests do expect you to make such small, safe inferences. What you may not do is go further than the numbers force - for example, inferring that older users prefer the online channel would be unsupported, as the passage suggests the opposite for the over-75s.

#### Question 16 (moderate)

True, False, or Cannot Say: "The doubling of assisted digital support requests was caused by the rise in online uptake."

**Correct answer: Cannot Say**

**Explanation:** The passage reports that the two things happened "during the same period" - a statement of timing, not causation. It never asserts that one caused the other. Your statistical training will recognise this instantly as "correlation is not causation", and here the verbal test rewards exactly the same discipline in prose form: co-occurrence in a sentence is not a causal claim. Since the text neither confirms nor denies the causal link, Cannot Say is correct. Noticing when a report implies causation without stating it is also a valuable quality-assurance comment you can offer when reviewing colleagues' drafts.

#### Question 17 (hard)

Which of the following best describes the report's recommendation?

- A) Close the phone and in-person channels, since most users now renew online.
- B) Keep non-digital channels running and research older users' needs before considering channel changes.
- C) Require users aged over 75 to receive assisted digital support.
- D) Extend the pilot for another year among users aged 35 to 54.

**Correct answer: B)**

**Explanation:** The recommendation sentence says precisely two things: continue "the phone and in-person channels alongside the online service", and conduct "further research with older users before any channel changes are considered". Option B restates both faithfully. Option A contradicts the recommendation outright - and notice how it tempts readers who anchored on the impressive 74% figure rather than the recommendation itself. Options C and D invent measures the passage never proposes. Recommendation questions reward finding the sentence where the authors state their position and treating everything else as context. This passage also models good public sector practice worth absorbing: digital uptake success did not lead the team to abandon users who need other channels - inclusion and accessibility considerations sit at the heart of government service delivery, and of the user needs your Delivering business impact skill asks you to help identify.

#### Question 18 (hard)

True, False, or Cannot Say: "Users aged 35 to 54 switched to the online service mainly because it saved them a trip to the post office."

**Correct answer: Cannot Say**

**Explanation:** This statement stitches together two separate findings from the passage, and the stitching is where it fails. The passage says the largest increases in uptake were among users aged 35 to 54, and - as a separate sentence - that survey respondents most frequently cited "saving a trip to the post office" as their reason for switching. But the passage never says who the survey respondents were, nor whether the most-cited reason among all respondents was also the main reason for the 35-54 group specifically. The 35-54 group's motives are simply not broken down. The text neither confirms nor contradicts the claim, so Cannot Say is correct. This trap - assuming a whole-population finding applies equally to a named subgroup - has a formal name in statistics (the ecological fallacy has a family resemblance), and it catches experienced analysts as well as test candidates. When you review or write reports, keep claims about subgroups tethered to evidence about those subgroups; when the breakdown does not exist, the honest phrasing is "respondents overall most frequently cited...". Precision of attribution is one of the quiet skills that makes analytical writing trustworthy, and verbal reasoning tests probe it because sloppy attribution is among the most common defects in real workplace reports.

### Preparation tips

- **Read the question before rereading the passage.** Skim the passage once for structure, read the statement, then hunt for the specific sentence that decides it. This is faster than memorising the whole text.
- **Learn the three verdicts cold.** True = the text supports it. False = the text contradicts it. Cannot Say = the text is silent or insufficient. When you feel torn between False and Cannot Say, ask: "does the text actively contradict this, or just not mention it?"
- **Practise on real work documents.** Take a paragraph from a data ethics framework, the Service Standard, or your team's runbook and write three statements about it - one True, one False, one Cannot Say. Designing questions teaches you more than answering them.
- **Watch for exception clauses.** "Except", "unless", "provided that", "may" versus "must" - circle these words mentally. They decide a large share of questions.
- **Silence your expertise.** Your data science knowledge is an asset everywhere except here. The test measures reading, not knowledge, so answer from the page alone.
- **Keep a steady pace.** Under a minute per question is normal. If a verdict will not come after two careful readings, choose your best answer and move on with a clear conscience.

### Common pitfalls

- **Bringing outside knowledge.** Knowing how ethics boards or pipelines usually work tempts you to answer from experience. The passage is the only universe that exists during the test.
- **Confusing "likely" with "stated".** A passage saying an outcome is expected or likely does not make the outcome a fact. Match the strength of the statement to the strength of the text.
- **Missing the scope of an exception.** Exceptions modify specific rules, not whole documents. Check exactly which requirement an "except" or "provided that" attaches to.
- **Answering False when the text is merely silent.** Absence of support is not contradiction. This single confusion causes more lost marks than any other in True/False/Cannot Say formats.
- **Reading only half the sentence.** Qualifiers at the end of sentences ("except for read-only access...") routinely reverse first impressions. Read to the full stop.
- **Poor time allocation.** Spending three minutes perfecting one verdict steals time from three straightforward ones. Accuracy per minute, not per question, wins these tests.


## Workplace job-specific situational judgement assessment

### About this assessment

A workplace job-specific situational judgement assessment evaluates your decision-making, interpersonal skills, and professional conduct. Instead of logic puzzles or arithmetic, it presents realistic workplace dilemmas - the awkward, ambiguous moments that actually happen in a data science team - and asks how you would respond. It measures how well your behavioural choices align with the values of your organisation and the demands of your role.

The format is distinctive. Each question describes a short scenario, then offers several plausible responses. Crucially, there is rarely one objectively "right" answer - several options may seem reasonable, but some fit the situation and your organisation's values better than others. You are usually asked to pick the Most Effective and Least Effective actions, or to rank or rate all the options from best to worst. Timing is generous or absent, because the test wants your natural judgement, not your speed.

For your role, the relevant values are those of the UK public sector and the Government Digital and Data profession: put user needs first, work in the open and be transparent, collaborate across disciplines, build accessible and inclusive services, and handle data ethically. Your role profile is full of judgement-shaped duties: "use data ethically and appropriately", "collaborate with others to develop data science solutions", "share data ethics and privacy risks through appropriate channels", "communicate effectively and present analysis and visualisations tailored to your audience", and "manage your contribution to tasks to fit in with the work of your wider team". A situational judgement test is simply these duties, dramatised.

One reassuring note for an associate: these scenarios do not expect heroics or seniority you do not have. In fact, options that overreach your level (making unilateral calls that belong to your supervisor) often score poorly, while options that combine honest action with appropriate escalation score well. Being new is not a weakness in this test - knowing how to act well while new is exactly what it measures.

### What it measures for your role

- **Ethical judgement** maps to **Data ethics and privacy** - applying principles "under supervision" and sharing "data ethics and privacy risks through appropriate channels".
- **Collaboration and teamwork** maps to **Delivering business impact** ("collaborate to help identify user needs") and **Programming and build (data science)** ("collaborate on shared codebases").
- **Communication judgement** maps to **Delivering business impact** - presenting "analysis and visualisations tailored to your audience", including when the audience will not like the message.
- **Handling uncertainty and mistakes** maps to **Applied maths, statistics and scientific practices** - the professional duty to reach "accurate and reliable conclusions" includes owning up when a conclusion turns out unreliable.
- **Learning behaviours** map to **Data science innovation** ("ask questions to improve your knowledge") and **Developing data science capability** ("manage your CPD").
- **Delivery awareness** maps to **Understanding product delivery** - fitting your work to the team's, flagging blockers early, and respecting agreed ways of working.

### Practice questions

For each scenario, decide your answer honestly before reading the ratings. The explanations matter more than the "score" - they show the reasoning patterns that strong colleagues use.

#### Question 1 (easy) - The suspicious data field

You are preparing a dataset for analysis and notice a column containing what look like full names and dates of birth, even though the data specification said the extract would be anonymised. Your supervisor is in meetings all morning.

- A) Continue your analysis but avoid using the suspicious columns.
- B) Stop working with the dataset, message your supervisor and the data owner flagging a possible personal data issue, and switch to another task until you hear back.
- C) Delete the suspicious columns yourself so the dataset is safe, then carry on.
- D) Carry on as normal - the specification said it was anonymised, so it must be fine.

**Most effective: B. Least effective: D.**

**Explanation:** Option B does everything your role asks: it applies data ethics principles under supervision, shares the risk "through appropriate channels" promptly, and avoids compounding any breach - while sensibly continuing to be productive elsewhere. Option D is worst because it privileges paperwork over evidence: the data in front of you contradicts the specification, and ignoring your own observation is the opposite of the inquisitive behaviour your role level prizes. Option A still processes a potentially unlawful extract; "avoiding" the columns does not remove the exposure and nobody is alerted. Option C means altering evidence and acting unilaterally beyond your level - well-intentioned, but it destroys the audit trail and may hide a systemic fault in the extraction process that will recur next month. Transparency plus escalation beats quiet fixes.

#### Question 2 (easy) - The confusing task

At sprint planning you are assigned a task to "productionise the churn model". You realise you do not actually understand what "productionise" involves in your team's setup, and everyone else seems busy.

- A) Spend the first two days researching on your own before telling anyone you are unsure.
- B) Ask in the team channel straight away: "Before I start, could someone point me at how we've productionised models before, or spare 15 minutes to walk me through what good looks like here?"
- C) Quietly do the parts you understand and hope the rest becomes clear.
- D) Ask to swap the task for one you already know how to do.

**Most effective: B. Least effective: C.**

**Explanation:** Option B is the textbook behaviour for your level: your role profile literally says you should "ask questions to improve your knowledge and learn about data science norms". Asking early, specifically, and with respect for others' time gets you productive fastest and signals professional maturity, not weakness. Option C is least effective because it delays the discovery of your uncertainty until the sprint is at risk - the delivery-method awareness your role expects includes surfacing blockers early. Option A wastes two days that a 15-minute conversation would save (some solo research is great; two silent days is not). Option D avoids growth entirely: associates develop precisely by taking on tasks at the edge of their ability, with support.

#### Question 3 (moderate) - The inconvenient result

Your analysis shows that a flagship digital service performs worse for users in rural areas. The service team's product manager, who commissioned the work, says: "Can we leave the rural breakdown out of the summary? It complicates the story and the main results are positive."

- A) Agree - the product manager commissioned the analysis and owns the report.
- B) Refuse and tell them omitting it would be dishonest, then escalate to their line manager immediately.
- C) Explain why the rural finding matters for user needs and inclusion, propose presenting it constructively alongside the positive results with recommendations, and if they still insist on omitting it, raise it with your own senior analyst before the report is finalised.
- D) Include the finding in the report anyway without telling the product manager.

**Most effective: C. Least effective: A.**

**Explanation:** This is a values collision: a stakeholder relationship versus analytical integrity and inclusion. Option C handles both. It communicates "tailored to your audience" - reframing the rural finding as actionable insight rather than embarrassment - and, if persuasion fails, escalates through your own professional line, which is the appropriate channel for an associate facing pressure on analytical integrity. Option A is least effective: government analysis exists to inform decisions honestly, and hiding a finding that a service underserves rural users fails user needs, transparency, and inclusion in one stroke. Option B reaches a defensible outcome by an unnecessarily combative route - escalating over someone's head before attempting a professional conversation damages collaboration. Option D protects the finding but by deception, poisoning the stakeholder relationship the team depends on. Notice the pattern: strong answers pair honesty with relationship care.

#### Question 4 (moderate) - The teammate's struggling code

Reviewing a pull request on your team's shared codebase, you find a teammate's script produces subtly wrong aggregations for records with missing values. The teammate is more experienced than you and slightly defensive about feedback.

- A) Approve the pull request to avoid friction - they probably know something you don't.
- B) Comment neutrally and specifically on the pull request: describe the behaviour you observed with a small reproducible example, and ask whether it is intended.
- C) Fix the bug yourself in a separate branch and merge it without discussing it.
- D) Mention it privately to your supervisor and let them handle it.

**Most effective: B. Least effective: A.**

**Explanation:** Option B models exactly how healthy collaboration on shared codebases works: evidence, specificity, and a genuinely open question ("is this intended?") that leaves room for the possibility you have missed context - respectful of experience without suppressing the observation. Option A is least effective because it knowingly lets a correctness bug into shared code; deference is not a substitute for accuracy, and "reaching accurate and reliable conclusions" is the profession's core promise. Option C bypasses the author entirely - even a correct fix, merged around a colleague, undermines the review process and trust. Option D is not terrible, but escalating a routine code observation before raising it with the author converts a normal engineering conversation into a personnel matter. Peer review exists precisely so juniors can question seniors' code on equal technical footing.

#### Question 5 (moderate) - The overloaded sprint

Mid-sprint, you realise your main task will take at least three days longer than estimated because the source data needs far more cleansing than anyone anticipated. The show-and-tell where results were promised is in four days.

- A) Work late every night to try to hit the original date, telling nobody about the problem.
- B) Tell your delivery manager and team at the next stand-up: explain the data quality discovery, give a revised estimate, and propose options - a reduced-scope interim result for the show-and-tell, or moving the item to next sprint.
- C) Show preliminary results at the show-and-tell without mentioning the data quality problems.
- D) Ask a teammate to secretly help you catch up.

**Most effective: B. Least effective: C.**

**Explanation:** Option B demonstrates delivery awareness: Agile teams depend on honest, early information about blockers, and offering options (interim scope versus re-planning) turns a problem report into a decision the team can make together - "managing your contribution to fit in with the work of your wider team" in action. Option C is least effective because it presents results you know rest on inadequately cleansed data; an audience will treat shown numbers as reliable, and walking back published-ish findings costs far more trust than a delayed demo. Option A hides the problem and gambles your wellbeing on an estimate already proven wrong - and if you fail, the team learns at the worst moment. Option D at least seeks help but the secrecy corrodes team transparency; help arranged openly at stand-up would be fine. Data quality surprises are utterly normal in this profession - what distinguishes professionals is how early and honestly they surface them.

#### Question 6 (moderate) - The tempting shortcut

A policy colleague urgently needs figures for a parliamentary question. The robust way to produce them takes a day; a quick approximation from an old cached dataset takes an hour but may be out of date. Your supervisor is on leave today.

- A) Provide the quick approximation without caveats - urgent means urgent.
- B) Refuse to provide anything until your supervisor returns tomorrow.
- C) Ask the colleague about the deadline and required precision, offer the one-hour approximation clearly labelled with its source, date, and limitations, and start the robust figures in parallel, checking whether another senior analyst can glance over the numbers before they go out.
- D) Provide the robust figures tomorrow, ignoring the stated urgency.

**Most effective: C. Least effective: A.**

**Explanation:** Option C shows the judgement the profession wants: it engages with the real user need (what deadline? what precision?), it is transparent about limitations - caveats transform a risky number into an honest one - and it seeks proportionate senior oversight rather than either freezing or freelancing. Options B and D both fail the user: parliamentary timescales are genuinely immovable, and an analyst who cannot distinguish "perfect" from "fit for purpose, honestly caveated" will frustrate every policy partner they serve. But option A is least effective because an unlabelled, possibly stale figure in a parliamentary answer is a small integrity failure with potentially public consequences - the accuracy of government numbers is a matter of public trust. The deep lesson: urgency changes the acceptable method, never the required honesty.

#### Question 7 (hard) - The biased training data

While building a prototype model to prioritise casework, you notice the historical training data reflects past practices that disadvantaged certain groups - the model will likely learn and repeat those patterns. The prototype demo to senior stakeholders is next week, and your team lead is excited about it.

- A) Present the demo as planned - it is only a prototype, and fairness can be fixed later.
- B) Quietly rebalance the training data using your own judgement about what is fair, without telling anyone.
- C) Raise the issue with your team lead before the demo: show what you found in the data, explain the risk of the model repeating past bias, and suggest the demo include this as a known limitation with a plan to address it.
- D) Email senior stakeholders directly to warn them the model is biased.

**Most effective: C. Least effective: B.**

**Explanation:** Option C is textbook: it shares an ethics risk through the appropriate channel (your team lead), with evidence, before the moment of consequence (the demo), and it offers a constructive path - presenting the limitation openly, which in government data science builds credibility rather than undermining it. Option B is least effective, which surprises some people: isn't rebalancing the data at least doing something? The problem is that fairness interventions involve genuine value judgements that must be made transparently and with oversight, not silently by the most junior person on the team; an undocumented intervention makes the model's behaviour unexplainable and unauditable - a second ethics problem stacked on the first. Option A ships a known bias risk to stakeholders unmentioned; "prototype" status reduces polish expectations, not honesty expectations. Option D bypasses your team lead for no reason - escalation beyond your line is for when the appropriate channel has failed, not before it has been tried. Ethical practice at your level is mostly about noticing, evidencing, and raising - not unilaterally fixing.

#### Question 8 (hard) - Your own mistake, discovered late

A month ago you produced analysis that informed a published dashboard. Today, while reusing your script, you discover a filtering bug: the headline figure was overstated by around 8%. Nobody else has noticed.

- A) Fix the script for future use but say nothing about the published figure - 8% is within the noise.
- B) Tell your supervisor the same day: explain the bug, quantify the impact, propose corrected figures, and ask how the team should handle correcting the dashboard.
- C) Wait to see if anyone notices; if someone does, explain it then.
- D) Correct the dashboard yourself quietly, without telling anyone the history.

**Most effective: B. Least effective: C.**

**Explanation:** Option B is the professional gold standard and every element matters: same-day honesty, a clear account of cause and impact, corrected numbers ready (you fix as well as confess), and deference to your supervisor on the correction process - because published government figures may have formal correction procedures an associate cannot know fully. Option C is least effective because it converts an honest mistake into concealment; every day of silence makes discovery more damaging, and mistakes found by others cost trust that self-reported mistakes actually build. Option A rewrites "materiality" to suit yourself - an 8% error in a published headline is not yours to wave away. Option D fixes the public artefact but hides the history, leaving colleagues who used the wrong figure uninformed and the audit trail broken. Everyone in analysis ships a bug eventually; careers are shaped not by the bug but by the 24 hours after finding it. Owning errors fast is also how "accurate and reliable conclusions" stays true over time.

#### Question 9 (hard) - The enthusiastic new technique

You read about a new machine learning technique that could improve your team's forecasting model. You are keen to try it. Your team's current model is well-understood, documented, and trusted by stakeholders. Rank these actions from most to least effective:

- A) Propose a time-boxed spike in the next sprint to evaluate the technique against the current model on historical data, sharing results with the team either way.
- B) Rebuild the production forecasting model with the new technique over the weekend and present the improvement as a done deal.
- C) Add the paper to your CPD reading list, discuss it at the team's next technical session, and seek a colleague to pair on a small experiment.
- D) Dismiss the idea - the current model works, and new techniques are risky.

**Most effective ranking: A, C, B, D (A best, D worst).**

**Explanation:** A and C are both strong, and ranking them is a judgement about initiative versus process. A edges ahead because it channels innovation through the team's delivery method - a time-boxed spike is exactly how Agile teams explore safely, and "sharing results either way" treats a negative result as valuable learning, which is good science. C is also excellent (CPD management, collaboration, small experiments) but slower to generate evidence. B, despite its energy, is third: it bypasses the team, risks a trusted production asset, creates unreviewed code on a shared codebase, and frames a technical choice as a fait accompli - innovation without collaboration reads as recklessness in a government context. D is least effective because it abandons the "inquisitive and curious approach to data" and the duty to "seek out and research new data science techniques" that define your role level; a team that reflexively dismisses new methods slowly becomes unable to evaluate them. The ideal associate is visibly curious and visibly disciplined - at the same time.

#### Question 10 (moderate) - The inaccessible dashboard

You built a dashboard that a senior stakeholder loves. A colleague points out it fails accessibility standards: colour is the only way series are distinguished, and screen readers cannot access the underlying figures. Fixing it will take two days you had earmarked for a new feature the stakeholder requested.

- A) Fix the accessibility issues first and tell the stakeholder the new feature will follow two days later, explaining why.
- B) Build the new feature first - the stakeholder is senior, and nobody has complained about accessibility.
- C) Ask the colleague to log the issue in the backlog for consideration next quarter.
- D) Add a note to the dashboard advising users that a fully accessible version is planned eventually.

**Most effective: A. Least effective: B.**

**Explanation:** Accessibility in UK government services is not a nice-to-have; public sector digital services are legally required to be accessible, and "nobody has complained" usually means excluded users gave up silently rather than that no one is affected. Option A treats accessibility as the blocking defect it is, and communicates the trade-off to the stakeholder honestly - most senior stakeholders in government respond well to "we must meet accessibility standards first", and saying so is communicating "tailored to your audience" at its most useful. Option B is least effective: it privileges hierarchy over a legal and ethical obligation. Option C treats a live defect excluding users today as a someday-item. Option D documents the exclusion without ending it. There is also a craft lesson: building accessibly from the start (colour plus shape or labels, screen-reader-friendly tables behind every chart) is cheaper than retrofitting - a habit worth forming now, at the start of your career.

#### Question 11 (moderate) - The data request from another team

An analyst from another department emails you directly: "Could you send over the citizen-level dataset behind your published report? It would save us months." You have the file. Your team has a data sharing process, but it involves forms and takes about two weeks.

- A) Send the file - analysts helping analysts is collaboration, and the aggregate results are already public.
- B) Reply warmly, explain that citizen-level data can only be shared through the data sharing process, send them the link and offer to help them complete it - and share what you can immediately, such as the published aggregate tables and methodology notes.
- C) Ignore the email - it is not your job to handle data requests.
- D) Send the file but ask them to keep it within their team.

**Most effective: B. Least effective: D.**

**Explanation:** The published report being public does not make the underlying citizen-level data shareable - aggregates and record-level data have completely different privacy properties, a distinction at the heart of your data ethics skill. Option B is collaborative and compliant: it honours the process that exists precisely to check legal basis and security for personal data transfers, while genuinely helping - a warm no-but-here's-how beats a cold no. Option D is least effective, narrowly worse than A: it commits the same unauthorised disclosure as A but adds awareness of wrongdoing (the request for secrecy shows you know it should not spread), compounding a breach with concealment. Option A is a serious error made innocently - the "everything's basically public" rationalisation is exactly what ethics training exists to correct. Option C fails collaboration without protecting anything; unanswered requesters often try other routes, and a helpful redirect costs five minutes. Process is not the enemy of collaboration here - it is what makes collaboration with personal data possible at all.

### Preparation tips

- **Anchor on public sector values.** Before practising, write down the five you will be assessed against: user needs first, transparency, collaboration, accessibility and inclusion, ethical data handling. Most scenarios test two of these against each other.
- **Learn the escalation pattern.** For an associate, the strong move is almost always: act on what is yours to act on, raise what is not through the nearest appropriate channel (supervisor, team lead, data owner), and never sit on a risk. Practise spotting which parts of a scenario are yours.
- **Beware of extremes.** Options that do nothing, hide something, or act unilaterally beyond your level are usually the weak ones. Options combining honesty, initiative, and communication are usually strong.
- **Rehearse with real memories.** Think of three awkward moments from your own work or studies. What did you do? What would the best version of you have done? Personal rehearsal makes test scenarios feel familiar.
- **Answer as your professional self, not your ideal self.** Assessors can spot idealised answers that no busy human would execute. Choose what a conscientious, realistic associate would genuinely do.
- **Discuss scenarios with colleagues.** Ask a teammate or mentor how they would handle one of the dilemmas above. Their reasoning - especially where it differs from yours - is free calibration for your judgement.

### Common pitfalls

- **Answering idealistically.** Choosing the option that sounds noblest rather than the one that is practically effective. "Refuse and escalate immediately" often sounds principled but skips the professional conversation that solves most problems.
- **Ignoring organisational values.** Public sector scenarios reward transparency, user focus, and inclusion. Answering as if you were in a "results at any cost" culture will misfire.
- **Selecting passive options.** Waiting, ignoring, logging for someday, or hoping nobody notices - these delay action, pass problems along, or leave risks live. Assessors mark them harshly.
- **Overreaching your level.** Unilateral fixes, secret data interventions, and skipping your line to email senior people all ignore the "under supervision" reality of an associate role. Escalating well is a strength, not an admission of weakness.
- **Forgetting the least-effective answer matters.** Many candidates deliberate over "most effective" and rush "least effective". Both are scored; give the weakest option the same careful reasoning.
- **Treating caveats as optional.** In data roles, several scenarios hinge on whether information travels with its limitations attached. When in doubt, the option that labels uncertainty honestly usually beats the one that presents a cleaner story.


## Conclusion

Well done for working through this guide - that was a substantial piece of professional development, and finishing it says something good about the inquisitive, committed mindset your role level celebrates.

You have now explored the four assessment types most relevant to your work as an associate data scientist. You practised cognitive questions built from the patterns, pipelines, and prioritisation calls of real data work; numeric questions grounded in the model metrics, budgets, and capacity figures you handle; verbal questions demanding the precise reading that ethics guidance, runbooks, and stakeholder emails deserve; and situational judgements that dramatised the collaboration, honesty, and escalation habits that make early careers flourish in the public sector.

A few parting thoughts. First, remember that every skill in this guide is double-purpose: practising for assessments is practising the job itself. The discipline of "only what the text says", the habit of asking "out of what?" before dividing, the instinct to surface risks early - these will serve you in sprint planning and stakeholder meetings long after any test is behind you.

Second, treat your results - practice or real - as information, not verdicts. A wobbly area is simply your next CPD topic, and your role profile expects you to "manage your CPD and link your learning to objectives". Revisit the sections that stretched you, space your practice out over weeks, and notice how quickly the improvement comes.

Third, keep perspective on assessment day. Rest well, read slowly, skip and return, and let the hard questions go without regret. You are compared against realistic benchmarks for your level, not perfection - and the qualities that matter most in your role, curiosity and care and honesty, are ones you get to demonstrate every working day, not just in a timed window.

Your profession chose "inquisitive" as the first word of your role description. Stay that way, keep learning, and good luck - you are going to do well.

