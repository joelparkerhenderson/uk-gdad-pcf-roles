# Data Analyst (Associate Data Analyst) - Psychometric Assessment Resources

## Introduction

Welcome! This guide has been created especially for you as an associate data analyst working within the UK Government Digital and Data profession. Whether you are preparing for an upcoming assessment, exploring what assessments involve, or simply looking for a structured way to build your confidence, this document is here to help you succeed.

Psychometric assessments are structured exercises that measure how you think, reason, and make decisions at work. They are widely used across the UK public sector, both in recruitment and in professional development. They are not designed to catch you out. Instead, they give you and your organisation a fair, consistent picture of your strengths and the areas where you can grow. For an associate data analyst, they are especially useful because your day-to-day work involves exactly the kinds of thinking these assessments measure: spotting patterns in data, checking figures carefully, reading policies and reports accurately, and making sensible judgements when working with colleagues and stakeholders.

This document is organised into four main assessment sections, each matched to your role:

- **Workplace job-specific cognitive assessment** - measures your general problem-solving ability using the kinds of data files, quality checks, and analytical tasks you handle every day.
- **Workplace job-specific numeric reasoning assessment** - measures how well you work with tables, percentages, and performance figures like those you prepare and check under supervision.
- **Workplace job-specific verbal reasoning assessment** - measures how accurately you read and interpret written material such as data governance policies, emails from stakeholders, and project briefs.
- **Workplace job-specific situational judgement assessment** - measures how you respond to realistic workplace situations involving your team, your supervisor, and the people who rely on your analysis.

Each section explains what the assessment measures, how it connects to the specific skills in your role, and then gives you a generous set of practice questions with full worked answers. Every question is set in a realistic UK government digital and data context, so the practice you do here will feel close to the real thing.

Here is how to get the most from this guide. First, read each "About this assessment" section so you understand the format. Second, try the practice questions honestly, without peeking at the answers, and note your reasoning. Third, read the worked explanations carefully, even for questions you got right, because the explanations show you the thinking habits that assessors look for. Finally, use the preparation tips and common pitfalls to shape your revision.

You are at the start of an exciting career in data. Being an associate means you are learning, and nobody expects perfection. Take your time, be kind to yourself, and treat every practice question as a chance to grow. Good luck!

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive assessment is a targeted test that measures the exact mental processes you use in your role as an associate data analyst. Unlike a general intelligence test, it uses practical workplace scenarios and real-looking data, so every question feels like a small slice of your actual job. It typically covers pattern recognition, logical deduction, error checking, prioritisation, and problem solving.

The format is usually timed, most often 15 to 30 minutes online, with multiple-choice questions. Before the real test begins, you normally get a few short, ungraded practice questions so you can get used to the interface. Some modern platforms are adaptive, meaning the questions get slightly harder or easier depending on your previous answers - so do not panic if the questions seem to get tougher, because that can be a sign you are doing well! Scoring is objective: your results are compared against a benchmark group, and many employers look at both your speed and your accuracy rather than a single overall number.

Why does this matter for your role? As an associate data analyst, you support the development and delivery of data analysis and data projects. That means you spend much of your day spotting patterns in datasets, noticing when a value looks wrong, following logical steps in an analytical approach, and deciding what to work on first. A cognitive assessment measures precisely these habits of mind. Doing well shows that you can identify data quality issues, follow a data preparation process carefully, and reason clearly about problem statements - all things your role summary asks of you.

### What it measures for your role

Each cognitive dimension maps directly onto skills named in your role:

- **Pattern recognition** connects to your skill in **data preparation and linkage**: identifying data quality issues means noticing when values break an expected pattern, such as a date column that suddenly changes format halfway through a file.
- **Logical deduction** connects to **applying statistical and analytical tools and techniques** and **developing code for analysis**: designing an analytical approach, even simple code, means reasoning step by step from inputs to outputs.
- **Error checking** connects to **data preparation and linkage** and the quality assurance elements of **applying statistical and analytical tools and techniques**: you are expected to explain the value of quality assurance and to prepare and cleanse data under supervision, contributing to making it fit for purpose.
- **Prioritisation** connects to **managing a data project**: understanding a problem statement, explaining the intended outcome, and adapting your ways of working to deliver different project outcomes and requirements.
- **Problem solving** connects to **delivering business impact through data**: aligning data and analysis to meet business requirements means working out which analytical route actually answers the organisation's question.

### Practice questions

Work through these at your own pace first, then try them again under timed conditions (about 90 seconds per question is realistic).

#### Question 1 (easy) - Pattern recognition in a reference dataset

You are helping a senior analyst tidy a reference table of local authority codes. The first column follows a pattern:

E06000001, E06000002, E06000003, E06000005, E06000006

Which value appears to be missing from the sequence?

- A. E06000000
- B. E06000004
- C. E06000007
- D. E06000005

**Correct answer: B**

**Explanation:** The codes increase by one each time: 001, 002, 003, then the sequence jumps to 005. The value E06000004 is missing. This is exactly the kind of data quality issue your role asks you to identify: a gap in an expected sequence. In real work you would flag this to your supervisor and check whether the record was deleted deliberately (some codes are retired) or lost during a data move between systems. Notice that option D is a value already present in the list - a common distractor designed to catch people who skim.

#### Question 2 (easy) - Spotting a format inconsistency

You are preparing a dataset of service completion dates for cleansing, under supervision. A sample of the date column reads:

12/03/2026, 15/03/2026, 2026-03-18, 21/03/2026, 24/03/2026

What is the data quality issue?

- A. One date is in the future
- B. One date uses a different format from the others
- C. The dates are not in chronological order
- D. There are duplicate dates

**Correct answer: B**

**Explanation:** Four dates use the UK day/month/year format, but the third value (2026-03-18) uses the ISO year-month-day format. Mixed date formats are one of the most common data quality issues you will meet when you identify, collect and move data between a range of systems, because different systems store dates differently. The dates are actually in chronological order (12, 15, 18, 21, 24 March), there are no duplicates, and whether a date is "in the future" depends on today's date, which the question does not give you. A good cleansing step would be to standardise every date to a single agreed format before analysis.

#### Question 3 (moderate) - Logical deduction about a data pipeline

Your team moves survey data through three steps every week: Extract (from the survey platform), Transform (cleansing and recoding), and Load (into the reporting database). You know the following facts:

1. If Extract fails, Transform does not run.
2. If Transform does not run, the reporting database is not updated.
3. This week, the reporting database was updated.

Which conclusion must be true?

- A. Extract succeeded this week
- B. Transform found no data quality issues this week
- C. The survey platform had no downtime this week
- D. The reporting database contains no errors

**Correct answer: A**

**Explanation:** Work backwards through the chain. The database was updated (fact 3). Fact 2 says that if Transform does not run, the database is not updated - so Transform must have run. Fact 1 says that if Extract fails, Transform does not run - so Extract must have succeeded. That is option A. The other options go beyond the facts: Transform running does not mean it found zero issues (B); Extract succeeding does not rule out brief platform downtime (C); and an updated database can still contain errors (D). This step-by-step "if-then" reasoning is the same logic you use when designing an analytical approach or writing simple code with support.

#### Question 4 (moderate) - Error checking a summary table

A colleague asks you to double-check a summary before it goes to the service owner. The table shows the number of digital service applications processed by a casework team:

| Week | Applications received | Applications processed | Backlog change |
|------|----------------------|------------------------|----------------|
| 1    | 400                  | 380                    | +20            |
| 2    | 420                  | 430                    | -10            |
| 3    | 450                  | 425                    | +35            |
| 4    | 410                  | 415                    | -5             |

Backlog change should equal applications received minus applications processed. Which row contains an error?

- A. Week 1
- B. Week 2
- C. Week 3
- D. Week 4

**Correct answer: C**

**Explanation:** Check each row. Week 1: 400 - 380 = +20, correct. Week 2: 420 - 430 = -10, correct. Week 3: 450 - 425 = +25, but the table says +35, so this row is wrong. Week 4: 410 - 415 = -5, correct. Careful row-by-row checking like this is the heart of quality assurance in statistical and analytical outputs. In an assessment, resist the urge to guess after checking only one or two rows - the error is often placed in the third or fourth position precisely because people stop checking early.

#### Question 5 (moderate) - Prioritisation under a deadline

It is 14:00 on Thursday. Your supervisor is out at meetings until tomorrow. You have four tasks:

1. Refresh a chart for a briefing pack the deputy director needs by 16:00 today (about 30 minutes of work).
2. Investigate a data quality issue a colleague flagged this morning, needed for Monday (about 2 hours).
3. Respond to a stakeholder email asking when the quarterly report will be published (about 10 minutes).
4. Continue writing documentation for your analytical approach, due next Friday (ongoing).

What is the most sensible order to tackle them?

- A. 4, 2, 1, 3
- B. 1, 3, 2, 4
- C. 3, 1, 2, 4
- D. 2, 1, 3, 4

**Correct answer: C**

**Explanation:** Both C and B put the two urgent items first, which is right. The best answer is C because the stakeholder email takes only 10 minutes, and clearing it first means the stakeholder is not kept waiting while you do 30 minutes of chart work - and you still finish the chart well before 16:00 (10 + 30 = 40 minutes, done by about 14:40). This is a classic "quick win first when it does not endanger the deadline" pattern. The data quality investigation matters but is not due until Monday, and the documentation has the longest runway. Prioritising like this reflects your role's requirement to adapt your ways of working to deliver different project outcomes and requirements.

#### Question 6 (moderate) - Pattern recognition in code output

You run a simple script that counts records per month in a dataset covering a full year. The output is:

Jan: 1,021  Feb: 987  Mar: 1,044  Apr: 998  May: 1,033  Jun: 12  Jul: 1,019  Aug: 1,002  Sep: 976  Oct: 1,041  Nov: 1,008  Dec: 995

What is the most likely explanation you should investigate first?

- A. June genuinely had almost no activity
- B. Records for June may be missing or failed to load
- C. The script counted July twice
- D. The dataset covers only eleven months

**Correct answer: B**

**Explanation:** Eleven months cluster tightly around 1,000 records, and June shows only 12 - a value about 99% below the pattern. The most likely explanation for such an extreme outlier in operational data is a data loading or extraction problem, so B is the first thing to investigate. Option A is possible in principle, but a good analyst checks the data pipeline before concluding that reality changed dramatically. Option C is not supported (July's figure looks normal), and option D is contradicted by the output, which shows twelve months. The habit here - "check the data before trusting the surprise" - is central to identifying data quality issues and providing possible solutions.

#### Question 7 (moderate) - Logical deduction about joining datasets

You want to link a training-records dataset to a staff dataset. You know:

1. Every training record has a staff ID.
2. Some staff have no training records.
3. A few staff IDs in the training records belong to staff who have since left, and leavers are removed from the staff dataset.

If you join the two datasets keeping only rows that match in both, which statement must be true?

- A. Every staff member will appear in the result
- B. Training records for leavers will not appear in the result
- C. The result will contain more rows than the training dataset
- D. Staff with no training will appear with blank training fields

**Correct answer: B**

**Explanation:** A "keep only matches" join (an inner join) keeps rows only where the staff ID exists in both datasets. Leavers are absent from the staff dataset (fact 3), so their training records cannot match and will be dropped - that is option B. Option A fails because staff with no training records (fact 2) have nothing to match against. Option D describes a different kind of join (a left join from the staff side). Option C is wrong because an inner join cannot produce more rows than the smaller matching set here. Understanding what happens to unmatched records is a core part of data preparation and linkage, and questions like this test whether you can reason it through logically.

#### Question 8 (moderate) - Problem solving with incomplete information

A policy colleague asks: "Can you tell me how many users abandoned the online application form last month?" You look at the analytics data and find you can see: total form starts, total form completions, and total form errors. You cannot directly see abandonments. What is the most defensible first step?

- A. Report form errors as the abandonment figure, since errors cause abandonment
- B. Estimate abandonments as form starts minus form completions, and clearly state this assumption
- C. Tell the colleague the question cannot be answered
- D. Report total form starts, since that is the largest available number

**Correct answer: B**

**Explanation:** Starts minus completions is a reasonable proxy for abandonment, provided you state the assumption openly (for example, some users may complete the form in a later month, so the estimate is approximate). This shows problem solving: aligning the available data to the business requirement while being honest about limits. Option A confuses one possible cause with the outcome - not every error leads to abandonment and not every abandonment follows an error. Option C gives up too early, and option D answers a different question entirely. In your role, contributing to data products that deliver business impact often means constructing a careful, clearly-caveated answer from imperfect data - always with your supervisor's review.

#### Question 9 (challenging) - Deduction from data model rules

Your team's data model for a grants system has these rules:

1. Every application belongs to exactly one applicant.
2. An applicant may have many applications.
3. Every payment is linked to exactly one application.
4. An application may have zero, one, or many payments.

A report shows 5,000 applicants, 8,200 applications, and 7,900 payments. Which statement must be true?

- A. Some applicants have more than one application
- B. Some applications have no payments
- C. Every applicant has at least one application
- D. Some payments are not linked to an application

**Correct answer: A**

**Explanation:** There are 8,200 applications and only 5,000 applicants, and each application belongs to exactly one applicant (rule 1). If every applicant had at most one application, there could be at most 5,000 applications. Since there are more, at least some applicants must hold multiple applications - option A must be true. Option B is tempting because 7,900 payments is fewer than 8,200 applications, but rule 4 allows an application to have many payments, so 7,900 payments could in theory be concentrated on fewer applications; we cannot be certain some applications have none... and equally we cannot be certain they all have some - so B is possible but not guaranteed. Option C is not guaranteed either: the applicant table could contain applicants with zero applications. Option D contradicts rule 3. This question rewards understanding the importance of data models and their uses - exactly what your role asks you to explain.

#### Question 10 (challenging) - Multi-step problem solving

You are asked to check whether a dashboard figure is plausible. The dashboard says: "Average processing time in July: 3 days." You know:

1. The team processed 600 cases in July.
2. 500 cases took 2 days each.
3. 100 cases were complex and took much longer.

What is the minimum average time the 100 complex cases must have taken for the dashboard figure to be correct?

- A. 5 days
- B. 8 days
- C. 10 days
- D. 3 days

**Correct answer: B**

**Explanation:** If the overall average is 3 days across 600 cases, the total processing time is 600 × 3 = 1,800 case-days. The 500 straightforward cases account for 500 × 2 = 1,000 case-days. That leaves 1,800 - 1,000 = 800 case-days for the 100 complex cases, which is 800 ÷ 100 = 8 days each on average. This kind of sense-check - working backwards from a published average to see whether the underlying numbers hold together - is a valuable quality assurance habit for statistical outputs. If the complex cases were known to average, say, 15 days, you would know the dashboard figure was wrong and could raise it with your supervisor.

#### Question 11 (challenging) - Prioritising conflicting quality checks

You have one hour before a dataset must be handed to the analysis stage. You can run only some of these checks in the time available:

1. Duplicate check (10 minutes) - duplicates were found in each of the last three deliveries.
2. Column name check (5 minutes) - the supplier has never changed column names in two years.
3. Full manual review of all 200,000 rows (6 hours) - the most thorough option.
4. Missing values check on the five fields used in the analysis (15 minutes) - these fields drive the final report.
5. Spelling review of a free-text comments field not used in the analysis (45 minutes).

Which combination makes the best use of the hour?

- A. Checks 1, 2, and 4
- B. Check 3 only, delivered late
- C. Checks 2 and 5
- D. Checks 1 and 5

**Correct answer: A**

**Explanation:** Checks 1, 2, and 4 take 10 + 5 + 15 = 30 minutes, fit comfortably in the hour, and target the highest risks: duplicates have a strong recent history of occurring, and missing values in the five analysis-critical fields would directly damage the final report. The column check is cheap insurance even though the risk is low. Option B sacrifices the deadline for thoroughness that is not proportionate to the risk. Options C and D spend 45 minutes on a spelling review of a field the analysis does not even use - effort in the wrong place. Risk-based prioritisation of quality assurance is a mark of maturing analytical judgement, and it reflects your role's emphasis on adapting ways of working to project requirements.

#### Question 12 (challenging) - Diagnosing a broken analytical output

Last month your monthly script produced a report showing about 2,000 service users per region. This month the same script shows exactly double - about 4,000 per region - for every single region. Nothing about the service suggests usage doubled. Which explanation best fits the evidence?

- A. Each region genuinely grew by 100%
- B. The input data was accidentally loaded twice, duplicating every record
- C. One region's data was misallocated to another region
- D. The script's percentage calculation has a rounding error

**Correct answer: B**

**Explanation:** The clue is that every region doubled by the same factor. Genuine growth (A) almost never affects all regions identically and simultaneously. Misallocation between regions (C) would make some regions rise and others fall, not all double. A rounding error (D) would produce small distortions, not a clean doubling of counts. A double-load of the input file, duplicating every record, would exactly double every region's count - matching the evidence perfectly. The practical next step would be to run a duplicate check on a unique identifier and, if confirmed, reload the data. Reasoning from the shape of an anomaly to its most likely cause is a core cognitive skill for anyone who prepares and cleanses data.

#### Question 13 (moderate) - Following a documented analytical approach

Your team's documentation for the monthly performance analysis says the steps must run in this order: (1) remove test records, (2) remove duplicates, (3) calculate completion rates, (4) round rates to one decimal place. A new colleague ran the steps in the order 1, 3, 2, 4 and got a completion rate of 87.3% instead of the expected 84.1%. Why does the order matter here?

- A. Rounding before calculating always inflates results
- B. Calculating rates before removing duplicates lets duplicate records distort the rate
- C. Removing test records is optional so the order is irrelevant
- D. The documentation is wrong because the steps are independent

**Correct answer: B**

**Explanation:** The colleague calculated completion rates at step 3 while duplicates were still in the data, then removed duplicates afterwards - too late to fix the rate already computed. If completed cases are more likely to be duplicated (for example, because completion events are logged twice by the system), the rate is pushed upwards, which fits the inflated 87.3% figure. Option A describes a different mistake (and the colleague did not round early anyway). Options C and D dismiss the documentation, but the differing results prove the steps are not independent. This question shows why your role values maintaining analytical approach documentation: a written, ordered method means everyone gets the same, correct answer - and when results differ, the documentation helps you find out why.

### Preparation tips

- **Practise with the artefacts of your job.** Spend time looking closely at real (non-sensitive) datasets, spotting odd values, gaps, and format changes. The more familiar these patterns feel, the faster you will recognise them under timed conditions.
- **Talk your reasoning out loud when practising.** Explaining why an answer is right, as if to a non-technical colleague, strengthens the logical pathways you will rely on in the test - and it doubles as practice for your communication skill.
- **Time yourself gently at first.** Start untimed, then move to 2 minutes per question, then 90 seconds. Building speed gradually is kinder and more effective than diving straight into full exam pressure.
- **Learn the common distractor tricks.** Wrong options often repeat a number from the question, describe a different but related concept, or state something plausible that the facts do not support. Spotting these patterns is a learnable skill.
- **Rest well before the assessment.** Cognitive tests measure processing speed, and tiredness slows everyone down. A good night's sleep is worth more than a late-night cramming session.
- **Ask your supervisor or a senior analyst to set you mini-puzzles.** As an associate you work closely with other data professionals - use that! A weekly "spot the data issue" exercise with a mentor is excellent preparation.

### Common pitfalls

- **Rushing the reading.** Many errors come from answering the question you expected rather than the question asked. Slow down for the final sentence of each question - it tells you exactly what is wanted.
- **Stopping your checks too early.** As in Question 4, errors are often planted late in a table. Check every row unless time absolutely forbids it.
- **Getting stuck on one hard question.** A single question is worth the same as any other. If you are stuck after your time budget, make your best choice, flag it if the platform allows, and move on.
- **Assuming the dramatic explanation.** When data looks surprising, inexperienced analysts often assume reality changed; experienced analysts first suspect the pipeline. Check the mundane explanation before the exciting one.
- **Panicking when questions get harder.** On adaptive tests, harder questions usually mean you are performing well. Treat rising difficulty as encouragement.
- **Ignoring speed-versus-accuracy balance.** Employers often see both measures. Wild guessing to finish fast hurts your accuracy score; perfectionism hurts your completion rate. Aim for steady, deliberate progress.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment evaluates your ability to analyse, interpret, and make logical decisions using numerical data. It mimics the data-handling demands of your actual role, focusing on practical business maths rather than abstract formulas. The question inputs look like the material you handle every day: performance tables, budget figures, capacity numbers, survey results, and dashboard extracts.

The typical format is multiple choice with a strict time limit - often around 20 to 25 minutes for 15 to 20 questions, so roughly a minute to 90 seconds per question. Most assessments allow or provide an onscreen calculator, because the point is interpretation, not mental arithmetic gymnastics. The maths itself is deliberately accessible: percentages, ratios, averages, differences, and simple projections. What makes it challenging is extracting the right numbers quickly and knowing which calculation to perform.

For you as an associate data analyst, this assessment is arguably the most directly job-relevant of the four. Your role asks you to support the development of statistical and analytical insights and reports, to identify data quality issues, and to prepare and manage data. All of those tasks rest on numerical fluency: noticing that a percentage does not match its underlying counts, calculating a completion rate correctly, or sense-checking a monthly total. Assessors know this, so numeric reasoning results carry real weight for data roles. The encouraging news is that numeric reasoning is one of the most coachable assessment types - steady practice reliably improves scores.

### What it measures for your role

- **Percentages, rates and changes** map to **applying statistical and analytical tools and techniques**: supporting statistical insights and reports under supervision means calculating and checking rates, proportions, and period-on-period changes.
- **Reading tables and charts accurately** maps to **data visualisation** and **data preparation and linkage**: before you can develop a visualisation that tells a meaningful story, you must extract the right figures from the source data - and spot when a figure looks wrong.
- **Averages and distributions** map to quality assurance within **applying statistical and analytical tools and techniques**: sense-checking whether an average is plausible given the underlying data is a daily quality assurance habit.
- **Budgets, capacity and simple projections** map to **delivering business impact through data** and **managing a data project**: understanding a problem statement often means quantifying it - how many users, how much backlog, what capacity is needed.
- **Ratios and proportional reasoning** map to **data preparation and linkage**: sampling, weighting, and checking that linked datasets have sensible match rates all rely on ratio thinking.

### Practice questions

An onscreen calculator is normally allowed - use one here too. What matters is choosing the right calculation and reading the data carefully. The arithmetic is shown in full in every explanation.

#### Question 1 (easy) - Percentage of a total

Your team's user survey received 1,250 responses. Of these, 350 came from users of assisted digital channels (for example, telephone support). What percentage of responses came from assisted digital users?

- A. 22%
- B. 28%
- C. 32%
- D. 35%

**Correct answer: B**

**Explanation:** Divide the part by the whole and multiply by 100: 350 ÷ 1,250 = 0.28, and 0.28 × 100 = 28%. Option D (35%) is a classic trap: it simply reuses the "350" from the question as a percentage. Always do the division rather than pattern-matching digits. Reporting channel splits like this is exactly the kind of figure you would prepare for a survey insights report under supervision.

#### Question 2 (easy) - Reading a table correctly

The table shows digital service transactions (in thousands) by quarter:

| Service | Q1 | Q2 | Q3 | Q4 |
|---------|-----|-----|-----|-----|
| Licence renewals | 120 | 135 | 128 | 142 |
| Address updates | 95 | 88 | 102 | 99 |
| New registrations | 60 | 72 | 75 | 81 |

How many address update transactions were there in Q3?

- A. 102
- B. 102,000
- C. 75,000
- D. 128,000

**Correct answer: B**

**Explanation:** The cell for address updates in Q3 reads 102, but the table header says figures are in thousands, so the true count is 102,000. Option A ignores the scale qualifier - one of the most common numeric reasoning mistakes and one the assessment deliberately tests. Option C reads the wrong row (new registrations) and option D reads the wrong row and column. In your own work, scale qualifiers like "in thousands" or "£m" appear constantly in government management information, so make checking units a reflex.

#### Question 3 (easy) - Percentage change

A digital service handled 48,000 applications in June and 54,000 in July. What was the percentage increase from June to July?

- A. 6%
- B. 11.1%
- C. 12.5%
- D. 89%

**Correct answer: C**

**Explanation:** Percentage change = (new - old) ÷ old × 100. So (54,000 - 48,000) ÷ 48,000 = 6,000 ÷ 48,000 = 0.125 = 12.5%. Option A confuses the absolute difference (6 thousand) with a percentage. Option B divides by the new value instead of the old one (6,000 ÷ 54,000 ≈ 11.1%) - a very common error, so remember: divide by the starting value. Option D is the ratio of June to July expressed the wrong way round. Month-on-month change figures like this appear in almost every performance report you will help prepare.

#### Question 4 (moderate) - Completion rates

An online form was started 8,400 times last month. 6,090 of those starts ended in successful completion. Your service standard target is a completion rate of at least 75%. Which statement is correct?

- A. The completion rate is 72.5%, below target
- B. The completion rate is 72.5%, above target
- C. The completion rate is 76.1%, above target
- D. The completion rate is 27.5%, below target

**Correct answer: A**

**Explanation:** Completion rate = completions ÷ starts × 100 = 6,090 ÷ 8,400 = 0.725 = 72.5%. The target is 75%, and 72.5% is below 75%, so option A is right. Option C miscalculates. Option D gives the abandonment rate (100% - 72.5% = 27.5%) rather than the completion rate. This two-part structure - calculate, then compare with a target - mirrors real service performance reporting, where getting the comparison right matters as much as the arithmetic.

#### Question 5 (moderate) - Averages and sense-checking

Five caseworkers processed the following numbers of cases in a week: 42, 38, 45, 40, and 15 (the fifth caseworker was on leave for three days). What is the mean number of cases processed per caseworker, and what should you note when reporting it?

- A. Mean 36; note that one value is unusually low due to leave
- B. Mean 40; no notes needed
- C. Mean 41.25; note that one caseworker was excluded
- D. Mean 45; report the maximum for a fair picture

**Correct answer: A**

**Explanation:** The mean is (42 + 38 + 45 + 40 + 15) ÷ 5 = 180 ÷ 5 = 36. But a good analyst also notices that the mean is dragged down by one atypical value: four of the five caseworkers processed 38 or more, so 36 understates typical performance. Reporting the mean with a note about the leave - or also giving the mean of the four full-time weeks, (42 + 38 + 45 + 40) ÷ 4 = 165 ÷ 4 = 41.25 - gives a fairer picture. Option C's arithmetic is right for the four-person calculation but wrongly claims a caseworker was excluded from the official figure. This question tests both calculation and the quality assurance mindset your role asks you to develop: numbers need context to be honest.

#### Question 6 (moderate) - Ratios in data linkage

You link a dataset of 12,000 benefit applications to an address register. 10,200 records match automatically, 900 match after manual cleaning, and the rest do not match at all. What is the ratio of total matched records to unmatched records, in simplest form?

- A. 34 : 3
- B. 17 : 3
- C. 37 : 3
- D. 12 : 1

**Correct answer: C**

**Explanation:** Total matched = 10,200 + 900 = 11,100. Unmatched = 12,000 - 11,100 = 900. The ratio is 11,100 : 900. Divide both sides by 300: 11,100 ÷ 300 = 37 and 900 ÷ 300 = 3, giving 37 : 3. Option A uses only the automatic matches (10,200 : 900 = 34 : 3) and forgets the manual ones - a realistic mistake when a dataset has more than one match route. Match-rate reporting like this is bread and butter for data preparation and linkage work, and it directly affects how much confidence users can place in linked analysis.

#### Question 7 (moderate) - Budget proportions

Your data team's annual tooling budget is £48,000. It is allocated as: analysis software 35%, visualisation licences 25%, cloud compute 30%, and training 10%. How much more is spent on cloud compute than on visualisation licences?

- A. £2,400
- B. £4,800
- C. £14,400
- D. £12,000

**Correct answer: A**

**Explanation:** Cloud compute = 30% of £48,000 = 0.30 × 48,000 = £14,400. Visualisation licences = 25% of £48,000 = 0.25 × 48,000 = £12,000. The difference is £14,400 - £12,000 = £2,400. A faster route: the difference in percentages is 30% - 25% = 5%, and 5% of £48,000 = £2,400. Option C and option D are the individual amounts, not the difference - always reread what the question actually asks. The shortcut method (work with the percentage difference directly) is a great time-saver in timed tests.

#### Question 8 (moderate) - Data storage capacity

A reporting database currently holds 3.2 terabytes of data and grows by roughly 80 gigabytes per month. The infrastructure team plans an upgrade when the database reaches 4 terabytes. Assuming 1 terabyte = 1,000 gigabytes, in how many months will the database reach the upgrade threshold?

- A. 8 months
- B. 10 months
- C. 12 months
- D. 40 months

**Correct answer: B**

**Explanation:** The remaining headroom is 4 TB - 3.2 TB = 0.8 TB = 800 GB. At 80 GB per month, that takes 800 ÷ 80 = 10 months. Option A might come from misreading 0.8 TB as 640 GB or a rushed division; option D divides 3,200 by 80, which answers a different question ("how long did the current data take to accumulate at this rate?"). Unit conversion followed by a simple division is a very common two-step pattern in numeric tests - do the conversion first, and write it down so you do not lose track under time pressure.

#### Question 9 (moderate) - Weighted figures across regions

A national digital service reports user satisfaction by region:

| Region | Survey responses | Satisfaction |
|--------|------------------|--------------|
| North  | 2,000            | 80%          |
| Midlands | 1,000          | 74%          |
| South  | 3,000            | 70%          |

What is the overall satisfaction rate across all responses?

- A. 74.7%
- B. 74.0%
- C. 73.7%
- D. 76.0%

**Correct answer: B**

**Explanation:** You cannot simply average the three percentages, because the regions have different numbers of responses. Work out the satisfied users in each region: North 80% of 2,000 = 1,600; Midlands 74% of 1,000 = 740; South 70% of 3,000 = 2,100. Total satisfied = 1,600 + 740 + 2,100 = 4,440. Total responses = 2,000 + 1,000 + 3,000 = 6,000. Overall rate = 4,440 ÷ 6,000 = 0.74 = 74.0%. You can verify: 6,000 × 0.74 = 4,440. The unweighted average (80 + 74 + 70) ÷ 3 = 74.7% (option A) looks plausible but is wrong because it ignores the response volumes - the South, with the most responses and the lowest satisfaction, pulls the true figure down. Weighted averages are essential whenever you combine rates across groups of different sizes - a daily task when supporting statistical reports under supervision.

#### Question 10 (challenging) - Percentage points versus percentages

A service's digital take-up rose from 60% of all transactions in 2024 to 72% in 2025. Which two statements are both correct?

- A. Take-up rose by 12 percentage points, which is a 20% relative increase
- B. Take-up rose by 12%, which is 12 percentage points
- C. Take-up rose by 20 percentage points, which is a 12% relative increase
- D. Take-up rose by 72% overall

**Correct answer: A**

**Explanation:** The difference between 72% and 60% is 12 percentage points. As a relative change, 12 ÷ 60 = 0.20 = a 20% increase. Both parts of option A are correct. Option B muddles the two concepts: "rose by 12%" would mean 60% × 1.12 = 67.2%, not 72%. Confusing percentages with percentage points is one of the most common errors in government reporting, and analysts are often the last line of defence against it. If you can explain this distinction clearly to a non-technical colleague, you are demonstrating exactly the communication skill your role framework names.

#### Question 11 (challenging) - Projecting a backlog

A casework team has a backlog of 5,400 cases. Each week the team receives 1,200 new cases and can process 1,500 cases. If these rates stay constant, how many weeks will it take to clear the backlog completely?

- A. 3.6 weeks
- B. 4.5 weeks
- C. 18 weeks
- D. 27 weeks

**Correct answer: C**

**Explanation:** The backlog shrinks by the net difference each week: 1,500 processed - 1,200 received = 300 cases of net reduction per week. Time to clear = 5,400 ÷ 300 = 18 weeks. Option A divides the backlog by processing capacity alone (5,400 ÷ 1,500 = 3.6), forgetting that new cases keep arriving - the most tempting wrong answer. This "net rate" structure appears constantly in operational analysis: queues, backlogs, and storage all fill and drain at the same time, and the analysis must use the difference between the rates.

#### Question 12 (challenging) - Sampling for a quality check

You need to manually quality-check a sample from a dataset of 24,000 records. Your team's practice is to check 2.5% of records, sampled evenly across the dataset's four source systems, which contributed records in the ratio 3 : 3 : 4 : 2. How many records should you check from the largest source system?

- A. 600
- B. 200
- C. 150
- D. 250

**Correct answer: B**

**Explanation:** First find the total sample: 2.5% of 24,000 = 0.025 × 24,000 = 600 records. The ratio 3 : 3 : 4 : 2 has 3 + 3 + 4 + 2 = 12 parts, so each part is 600 ÷ 12 = 50 records. The largest system has 4 parts: 4 × 50 = 200 records. Option A stops after the first step (the whole sample, not the largest system's share). Option C is a 3-part share and option D has no basis. Multi-step questions like this reward writing down intermediate results - total sample, parts, per-part size - so each step stays simple.

#### Question 13 (challenging) - Interpreting a performance dashboard

A dashboard shows these metrics for an online licensing service in October:

- Transactions: 40,000 (September: 32,000)
- Failure rate: 2.5% (September: 3.0%)
- Average cost per transaction: £1.90 (September: £2.10)

Which statement is supported by the figures?

- A. The number of failed transactions fell from September to October
- B. The number of failed transactions rose from September to October
- C. Total transaction costs fell from September to October
- D. The service processed fewer transactions but more cheaply

**Correct answer: B**

**Explanation:** A falling failure rate does not guarantee fewer failures when volume rises. September failures: 3.0% of 32,000 = 960. October failures: 2.5% of 40,000 = 1,000. Failures actually rose from 960 to 1,000, so B is supported and A is contradicted. For option C, total costs were September: 32,000 × £2.10 = £67,200 and October: 40,000 × £1.90 = £76,000 - costs rose, so C is wrong. Option D is wrong because transactions increased. This is a superb example of why analysts must multiply rates by volumes before drawing conclusions - dashboards full of improving rates can still hide rising absolute numbers, and spotting that is the kind of insight that delivers real business impact.

#### Question 14 (challenging) - Reconciling two data sources

Two systems record completed applications for the same service. System A (the case management system) shows 18,240 completions for the quarter. System B (the payments system) shows 17,556 completions. Your supervisor asks: "What percentage of System A's figure is unaccounted for in System B?"

- A. 3.75%
- B. 3.9%
- C. 6.84%
- D. 96.25%

**Correct answer: A**

**Explanation:** The gap is 18,240 - 17,556 = 684 records. As a percentage of System A's figure: 684 ÷ 18,240 = 0.0375 = 3.75%. Option B divides by System B's figure instead (684 ÷ 17,556 ≈ 3.9%) - close enough to look right, which is why the question asks specifically "of System A's figure". Option D is the proportion accounted for, not unaccounted for. Reconciliation gaps like this one are a classic data quality issue: the follow-up in real work would be investigating whether the 684 records are timing differences (completions not yet paid), genuine errors, or duplicates in System A.

#### Question 15 (challenging) - Cost-benefit of automation

Your team spends 6 hours per week manually preparing a weekly report. A colleague proposes writing a script that would take 30 hours to build and reduce the manual work to 1 hour per week. Ignoring other costs, after how many weeks of use does the time invested in the script pay for itself?

- A. 5 weeks
- B. 6 weeks
- C. 30 weeks
- D. 4 weeks

**Correct answer: B**

**Explanation:** The script saves 6 - 1 = 5 hours per week. The build cost is 30 hours. Break-even = 30 ÷ 5 = 6 weeks. After six weeks the cumulative saving (6 × 5 = 30 hours) equals the build investment, and every week after that is pure gain. Option A divides by the original 6 hours; option C forgets that some manual work remains. This simple payback calculation is a persuasive way to explain the importance of coding for analysis to non-technical decision-makers - a skill your role framework explicitly names - because it turns a technical proposal into a business case.

#### Question 16 (moderate) - Checking a chart against its source data

You are quality-assuring a colleague's bar chart for a report. The chart shows complaint volumes of roughly 300, 450, and 600 for three service channels, and the caption says "Telephone complaints are three times webchat complaints." The source table reads: webchat 298, post 452, telephone 597. Which quality assurance conclusion is right?

- A. The chart and caption are both consistent with the source data
- B. The chart matches the data but the caption overstates the ratio, which is closer to two to one
- C. The caption is right but the chart bars are in the wrong order
- D. Both the chart and the caption are wrong

**Correct answer: B**

**Explanation:** Check the chart first: 298, 452, and 597 round naturally to roughly 300, 450, and 600, so the bars fairly represent the source. Now check the caption's claim: telephone (597) divided by webchat (298) = 597 ÷ 298 ≈ 2.0, so telephone complaints are about twice webchat complaints, not three times. The caption overstates the relationship, so option B is correct. Nothing in the question tells you the intended bar order, so option C has no basis. This two-part check - do the visuals match the data, and does the written claim match the arithmetic? - is precisely the quality assurance your role asks you to value in statistical and analytical outputs, and captions are where errors most often hide, because they are written last and checked least.

#### Question 17 (moderate) - Converting between reporting periods

A service reports 1,680 support tickets in a 28-day reporting period. A stakeholder asks: "Roughly how many tickets should we expect in a full 12-month year, assuming the rate stays constant?" Which estimate is best?

- A. About 20,160 tickets
- B. About 21,900 tickets
- C. About 61,320 tickets
- D. About 6,720 tickets

**Correct answer: B**

**Explanation:** First find the daily rate: 1,680 ÷ 28 = 60 tickets per day. A year has 365 days, so 60 × 365 = 21,900 tickets. Option A comes from multiplying the 28-day figure by 12 (1,680 × 12 = 20,160), treating a 28-day period as a month - but twelve 28-day periods cover only 336 days, so this undercounts by about a month. Option D multiplies by only 4, and option C has no sensible basis. Period conversions like this arise constantly in government reporting, where operational systems often use 28-day cycles but boards want monthly or annual views - and the 28-day-versus-calendar-month distinction is a genuine source of real-world reporting errors, not just a test trick. When rates are involved, always go down to a common unit (per day) before scaling up.

### Preparation tips

- **Master the core four: percentages, percentage change, averages, and ratios.** Almost every question is one of these or a two-step combination. Ten minutes of daily practice on these operations builds real speed.
- **Always check units and scale qualifiers.** Before calculating anything, glance at the table title and headers for "in thousands", "£m", or per-week versus per-month. Make it a ritual.
- **Write down intermediate results.** Multi-step questions are much easier when you note each stage (as in Question 12). Trying to hold three numbers in your head under time pressure invites errors.
- **Practise with your own team's reports.** Take a recent (non-sensitive) performance pack and recalculate its percentages and averages yourself. This doubles as quality assurance practice and assessment preparation.
- **Use the calculator wisely.** It removes arithmetic slips but cannot choose the calculation for you. Spend your thinking time on "what operation does this question need?" and let the calculator do the rest.
- **Estimate before you calculate.** A rough expectation ("the answer should be a bit above 70%") catches keying errors instantly. Estimation is a professional analyst's habit, not a shortcut.

### Common pitfalls

- **Misreading chart and table labels.** Confusing monthly data with annual data, or ignoring scale qualifiers like "in thousands", is the single most common cause of lost marks - and of embarrassing errors in real reports.
- **Dividing by the wrong base.** Percentage change uses the starting value; "percentage of A's figure" means divide by A. Questions 3 and 14 both test this deliberately.
- **Averaging percentages without weighting.** As Question 9 shows, rates from groups of different sizes must be weighted by group size. The unweighted average is almost always among the wrong options.
- **Over-calculating.** Sometimes a percentage-difference shortcut (Question 7) or an estimation gets you to the answer in seconds. Do not perform a five-step calculation when a one-step route exists.
- **Time-sink questions.** One stubborn multi-stage problem can swallow five minutes. Set a personal limit (say 2 minutes), then choose your best answer and move on - you can return if time remains.
- **Confusing rates with absolute numbers.** An improving failure rate can hide rising failures when volumes grow (Question 13). Always ask "rate or count?" before concluding anything.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment evaluates how well you understand, analyse, and draw correct conclusions from written workplace information. It mirrors the exact reading demands of your role: data governance policies, quality standards, project briefs, stakeholder emails, and analytical reports. The passages use real industry terminology, and the questions test whether you can work strictly from what the text says.

The most common format gives you a passage followed by statements you must judge as **True** (the passage says or logically guarantees this), **False** (the passage contradicts this), or **Cannot Say** (the passage gives insufficient information either way). Some tests add multiple-choice comprehension questions about the passage's meaning, tone, or main point. Timing is tight - often less than a minute per question - because the test simulates workplace reading under deadline pressure.

The single most important rule: answer only from the text provided, ignoring your outside knowledge. Even if you know from experience that something is usually true in government data work, if the passage does not say it, the answer may be Cannot Say. This feels strange at first, but it measures a genuinely important professional skill: reading precisely what a policy, standard, or specification actually commits to, rather than what you assume it means.

For an associate data analyst, this matters enormously. Your role asks you to explain the importance of data governance policies, follow appropriate standards and practices, understand problem statements, and communicate data and conclusions in appropriate formats. Every one of those duties starts with accurate reading. Misreading a retention policy, a data sharing agreement, or a project brief can cause real harm - so employers test this skill carefully, and building it will serve you throughout your career.

### What it measures for your role

- **Precise comprehension of policy text** maps to **data management** and **data ethics and privacy**: explaining the importance of data governance policies requires reading exactly what those policies do and do not require.
- **Distinguishing stated facts from assumptions** maps to **applying statistical and analytical tools and techniques**: quality-assured analysis reports claim only what the data supports - the same discipline True/False/Cannot Say questions train.
- **Understanding problem statements** maps to **managing a data project**: your role asks you to understand a problem statement and explain the intended outcome; verbal reasoning tests whether you extract requirements accurately from a brief.
- **Reading stakeholder communications** maps to **communicating between the technical and non-technical**: knowing the types of communication used with internal and external stakeholders starts with interpreting their messages correctly.
- **Identifying main points and tone** maps to **data visualisation** and storytelling: telling a meaningful story with data requires recognising what the key message of a document actually is.

### Practice questions

For each passage, judge the statements strictly on the text. Read the passage once for structure, then return to it to verify each statement against the exact wording.

#### Passage A - Data retention policy extract

*"Under this department's data retention policy, personal data collected for service improvement research must be deleted or fully anonymised within 24 months of collection, unless a documented exemption is approved by the Data Protection Officer. Pseudonymised data, where identifiers are replaced with codes but a key exists, is treated as personal data for the purposes of this policy. Teams must record all retention decisions in the departmental data catalogue. Aggregated statistics that cannot identify any individual fall outside the scope of this policy."*

#### Question 1 (easy)

True, False, or Cannot Say: Pseudonymised research data must be deleted or fully anonymised within 24 months unless an exemption is approved.

**Correct answer: True**

**Explanation:** The policy says pseudonymised data "is treated as personal data for the purposes of this policy", and personal data "must be deleted or fully anonymised within 24 months of collection, unless a documented exemption is approved". Chaining the two sentences gives the statement exactly. This kind of two-step reading - applying a definition from one sentence to a rule in another - is very common in policy documents, and in verbal tests.

#### Question 2 (easy)

True, False, or Cannot Say: Aggregated statistics that cannot identify any individual must be recorded in the departmental data catalogue.

**Correct answer: False**

**Explanation:** The final sentence says such aggregated statistics "fall outside the scope of this policy". The catalogue requirement is a rule of this policy, so it does not apply to out-of-scope data. Be careful: the passage says teams must record "all retention decisions", which sounds sweeping, but the scope sentence limits the whole policy. Reading a document's scope statement first is a professional habit worth building.

#### Question 3 (moderate)

True, False, or Cannot Say: The Data Protection Officer approves most exemption requests within one month.

**Correct answer: Cannot Say**

**Explanation:** The passage says exemptions must be "approved by the Data Protection Officer" but gives no information about how many requests are approved or how quickly. Your workplace experience might suggest a typical timescale, but the text is silent, so the only defensible answer is Cannot Say. Resisting the pull of plausible outside knowledge is the core skill this format measures.

#### Question 4 (moderate)

True, False, or Cannot Say: Personal data collected for purposes other than service improvement research may be kept for longer than 24 months.

**Correct answer: Cannot Say**

**Explanation:** The policy extract covers only "personal data collected for service improvement research". It says nothing about data collected for other purposes - other rules may exist, but they are not in this text. Notice the statement is not False: the passage does not contradict it; it simply does not address it. The False/Cannot Say boundary is exactly this: False needs a contradiction in the text, Cannot Say needs only silence.

#### Passage B - Email from a policy stakeholder

*"Hi team - thanks for the draft dashboard. The regional breakdown is useful, but the minister's office has asked that Thursday's pack focuses on national trends only. Please also note that the figures for the North East still look implausibly low; until the data supplier confirms the fix they promised us last week, we should not publish any regional figures externally. Internal circulation for quality assurance purposes is fine. Could you have a national-only version ready by Wednesday noon so we have time for sign-off?"*

#### Question 5 (easy)

True, False, or Cannot Say: The stakeholder wants a national-only version of the dashboard by Wednesday noon.

**Correct answer: True**

**Explanation:** The final sentence asks directly: "Could you have a national-only version ready by Wednesday noon". Although phrased politely as a question - very common in UK workplace emails - it is a clear request with a clear deadline. Learning to read polite phrasing as firm requirements is part of communicating with stakeholders.

#### Question 6 (moderate)

True, False, or Cannot Say: Regional figures must not be circulated internally.

**Correct answer: False**

**Explanation:** The email says "we should not publish any regional figures externally. Internal circulation for quality assurance purposes is fine." The statement contradicts the text's explicit permission for internal circulation, so it is False. Watch for the external/internal distinction: a rushed reader sees "should not publish any regional figures" and stops before the qualifier. In real data work, exactly this kind of misreading causes teams to either over-share or over-restrict data.

#### Question 7 (moderate)

True, False, or Cannot Say: The data supplier has fixed the North East data issue.

**Correct answer: Cannot Say**

**Explanation:** The email says the supplier "promised" a fix last week and that regional figures should be held back "until the data supplier confirms the fix". A promise of a fix is not confirmation that the fix has happened - the email treats it as pending. But equally the text does not say the fix has failed. The truthful position is that we do not know yet, so Cannot Say. Distinguishing a "likely or promised outcome" from a "stated fact" is one of the most heavily tested skills in verbal reasoning.

#### Question 8 (moderate) - Multiple choice

Which of the following best summarises the main request in the stakeholder's email?

- A. Investigate why the North East figures are implausibly low
- B. Produce a national-trends-only dashboard version by Wednesday noon for sign-off
- C. Stop all circulation of the dashboard until further notice
- D. Add more regional breakdowns to Thursday's pack

**Correct answer: B**

**Explanation:** The email's central, actionable request is the national-only version by Wednesday noon (option B). The North East issue (A) is context and a caution about publication, not a request for the analyst to investigate - the fix sits with the data supplier. Option C overstates the restriction (internal circulation is fine), and option D reverses the instruction. Identifying the main point among surrounding detail is precisely what you do when you understand a problem statement in a data project.

#### Passage C - Data quality standard extract

*"All datasets loaded to the corporate analytical platform must pass automated validation before use. Validation checks completeness of mandatory fields, conformity of formats to the published data dictionary, and referential integrity against master reference lists. A dataset failing any check is quarantined. Quarantined datasets may be released for analysis only when the data owner documents the failure's cause and either corrects the data or accepts the risk in writing. Analysts must not bypass quarantine, even for urgent requests. Where a reference list is itself out of date, the analyst should raise a reference data change request rather than amending the list directly."*

#### Question 9 (moderate)

True, False, or Cannot Say: A dataset that fails only the format conformity check will be quarantined.

**Correct answer: True**

**Explanation:** The standard says "a dataset failing any check is quarantined". Format conformity is one of the listed checks, and "any" means one failure is enough. The word "only" in the statement may make you hesitate, but it does not change the logic: failing one check triggers quarantine regardless of the others passing. Quantifier words - any, all, only, some - carry most of the logical weight in standards documents, and in these tests.

#### Question 10 (challenging)

True, False, or Cannot Say: An analyst may release a quarantined dataset for analysis if the request is urgent and the analyst documents the failure's cause.

**Correct answer: False**

**Explanation:** Two parts of the text defeat this statement. First, release requires the **data owner** - not the analyst - to document the cause and either correct the data or accept the risk in writing. Second, "analysts must not bypass quarantine, even for urgent requests". The statement swaps the responsible role and invokes urgency the standard explicitly rules out, so it contradicts the text and is False. Role-based rules ("who may do what") are a favourite trap: always check the actor, not just the action.

#### Question 11 (challenging)

True, False, or Cannot Say: Reference lists on the platform are updated every month.

**Correct answer: Cannot Say**

**Explanation:** The passage acknowledges that a reference list can be "out of date" and describes what an analyst should do about it (raise a change request), but it never states how often lists are updated. No schedule is given, so Cannot Say. Notice how a text can discuss a topic - here, reference data currency - without providing the specific fact a statement claims. Proximity of topic is not evidence.

#### Question 12 (challenging) - Multiple choice

According to the passage, what should an analyst do if they find the master reference list itself is out of date?

- A. Amend the reference list directly so validation passes
- B. Bypass the quarantine because the failure is not the dataset's fault
- C. Raise a reference data change request
- D. Ask the data owner to accept the risk in writing

**Correct answer: C**

**Explanation:** The final sentence addresses this exact situation: "the analyst should raise a reference data change request rather than amending the list directly". Option A is explicitly ruled out by that sentence, and option B is ruled out by the no-bypass rule. Option D is the release route for a quarantined dataset generally, but the passage prescribes a more specific action for the out-of-date reference list case. When a passage offers both a general rule and a specific rule, the specific rule answers the specific question.

#### Passage D - Extract from an analytical report

*"Digital applications rose 14% year on year, while paper applications fell 9%. The research team attributes most of the digital growth to the simplified sign-in process introduced in April, although the concurrent marketing campaign may also have contributed. Satisfaction among digital applicants averaged 4.2 out of 5, compared with 3.8 for paper applicants. However, respondents using assistive technology reported lower satisfaction (3.4), and the sample for this group was small, so this figure should be treated with caution. The team recommends further research with assistive technology users before drawing conclusions about accessibility barriers."*

#### Question 13 (moderate)

True, False, or Cannot Say: The simplified sign-in process caused the entire increase in digital applications.

**Correct answer: False**

**Explanation:** The report attributes "most" - not all - of the growth to the sign-in change, and explicitly says the marketing campaign "may also have contributed". Claiming the sign-in change caused the entire increase contradicts the report's carefully hedged wording. Analytical reports are written with precision about causation, and the test checks whether you read hedging words ("most", "may", "attributes") as carefully as they were written. This mirrors the quality assurance standard your own reports must meet.

#### Question 14 (moderate)

True, False, or Cannot Say: The satisfaction figure for assistive technology users is based on a small sample.

**Correct answer: True**

**Explanation:** The report states directly: "the sample for this group was small, so this figure should be treated with caution". The statement restates the text almost exactly. Not every question is a trap - some simply reward accurate reading. Answer confidently when the text is explicit; do not talk yourself into Cannot Say when the passage plainly says the thing.

#### Question 15 (challenging)

True, False, or Cannot Say: Paper applicants were less satisfied than digital applicants because the paper process is slower.

**Correct answer: Cannot Say**

**Explanation:** The satisfaction gap is stated (3.8 versus 4.2), so the comparison itself is true - but the statement goes further and asserts a *reason*: "because the paper process is slower". The passage never mentions processing speed at all. A statement that bundles a true fact with an unsupported explanation cannot be judged True; and since the text does not contradict the explanation either, the answer is Cannot Say. Read compound statements clause by clause - a single unsupported clause changes the answer.

#### Question 16 (challenging) - Multiple choice

What is the report's position on accessibility barriers in the digital service?

- A. It concludes that accessibility barriers exist and must be fixed urgently
- B. It concludes there are no accessibility barriers because overall satisfaction is high
- C. It notes a cautionary signal from a small sample and recommends further research before drawing conclusions
- D. It makes no reference to users with accessibility needs

**Correct answer: C**

**Explanation:** The report flags lower satisfaction (3.4) among assistive technology users, immediately cautions that the sample was small, and "recommends further research... before drawing conclusions about accessibility barriers". That is precisely option C: a signal, a caveat, and a next step. Options A and B both overstate - in opposite directions - what the evidence supports, and option D is contradicted by the passage. This measured position is a model for your own practice: your role asks you to develop inclusive, accessible outputs that recognise different user needs, and that starts with taking signals like this one seriously without exaggerating them.

#### Passage E - Project brief for a new data product

*"The Channel Insight project will build a monthly data product showing how users move between the department's contact channels: web, telephone, webchat, and post. Phase one covers web and telephone only; webchat and post will be added in phase two, subject to a data sharing agreement with the outsourced contact centre provider. The product's primary users are operational managers, who need channel volumes within five working days of month end. The project board has agreed that no individual-level data will be included in the product; all outputs will be aggregated to channel, region, and week. An associate data analyst will support the build under the direction of a senior data analyst, with responsibility for preparing and validating the monthly source extracts."*

#### Question 17 (moderate)

True, False, or Cannot Say: Phase one of the product will include webchat data.

**Correct answer: False**

**Explanation:** The brief states plainly: "Phase one covers web and telephone only; webchat and post will be added in phase two". The statement directly contradicts this, so it is False. Note the practical importance: if you were the associate analyst on this project and misread the phasing, you might spend days chasing webchat extracts that are not needed yet - and are not even covered by a data sharing agreement. Accurate reading of a brief's scope is the first act of understanding a problem statement.

#### Question 18 (challenging)

True, False, or Cannot Say: The data sharing agreement with the contact centre provider has been signed.

**Correct answer: Cannot Say**

**Explanation:** The brief says phase two is "subject to a data sharing agreement with the outsourced contact centre provider". "Subject to" tells you the agreement is a condition - but not whether it is signed, in negotiation, or not yet started. The text neither confirms nor denies its status, so Cannot Say. Compare this carefully with Question 7 in Passage B: conditional and pending language ("subject to", "promised", "planned") is one of the most reliable sources of Cannot Say answers, because it describes a dependency without reporting its outcome.

#### Question 19 (challenging) - Multiple choice

According to the brief, which of the following is part of the associate data analyst's stated responsibility?

- A. Directing the build of the data product
- B. Negotiating the data sharing agreement with the provider
- C. Preparing and validating the monthly source extracts
- D. Deciding which aggregation levels the outputs will use

**Correct answer: C**

**Explanation:** The final sentence assigns the associate "responsibility for preparing and validating the monthly source extracts", under the direction of a senior data analyst - so option C matches the text exactly. Option A inverts the reporting relationship: the senior analyst directs, the associate supports. Option B involves the provider agreement, which the brief attaches to phase two and to no named individual. Option D is settled already: the project board has agreed the aggregation (channel, region, and week), so it is not a decision left open for any analyst. This is the same actor-checking discipline as Question 10 - and it maps directly onto your real duty to understand roles within a multi-disciplinary team, including your own.

#### Question 20 (moderate)

True, False, or Cannot Say: Operational managers need channel volumes within five working days of month end.

**Correct answer: True**

**Explanation:** The brief states this requirement word for word: the primary users "need channel volumes within five working days of month end". When a statement matches the text this directly, answer True with confidence and bank the time for harder questions. In real work, this sentence would drive your whole monthly timetable as the analyst preparing the extracts - requirements about timing are among the most operationally important details to extract accurately from any brief.

#### Question 21 (challenging)

True, False, or Cannot Say: The data product will show which individual users switched from telephone to web.

**Correct answer: False**

**Explanation:** The board "has agreed that no individual-level data will be included in the product; all outputs will be aggregated to channel, region, and week". Showing which individual users switched channels would require exactly the individual-level data the brief rules out, so the statement contradicts the text and is False. This is a subtle one: the project's stated purpose is to show "how users move between... channels", which sounds individual - but the aggregation sentence tells you movement will be visible only in aggregate patterns, not per person. When two sentences seem to pull in different directions, the more specific and restrictive one usually governs, and here it also reflects the privacy-by-design thinking your data ethics and privacy skill asks you to value.


### Preparation tips

- **Read government writing every day.** GOV.UK service standards, data policies, and published statistical bulletins are free, realistic practice material. Read one short document daily and summarise its main rule in a sentence.
- **Practise the True/False/Cannot Say discipline.** After reading any policy paragraph, invent three statements about it - one True, one False, one Cannot Say - and check your reasoning. Teaching yourself to build the traps makes you far better at spotting them.
- **Learn the power words.** Quantifiers (all, any, some, only, most), modal verbs (must, may, should), and hedges (attributes, suggests, likely) decide most answers. Slow down whenever you meet one.
- **Check the actor as well as the action.** Standards assign duties to specific roles - data owner, analyst, Data Protection Officer. Question 10 shows how swapping the actor flips an answer.
- **Practise reading for structure first.** Skim to learn where the scope, the rules, and the exceptions live, then verify each statement against the exact sentence. This is faster than rereading the whole passage per question.
- **Be encouraged: this skill compounds.** Every hour you invest improves not just your test score but your daily work - clearer reading of briefs, policies, and stakeholder emails is visible to supervisors quickly.

### Common pitfalls

- **Bringing in outside knowledge.** You may know how retention policies usually work, but the test asks only about this passage. If the text is silent, the answer is Cannot Say - no matter what your experience says.
- **Confusing False with Cannot Say.** False requires the passage to contradict the statement; silence is not contradiction. Questions 4 and 11 both live on this boundary.
- **Misreading hedged language as fact.** "Promised a fix" is not "fixed" (Question 7); "attributes most" is not "caused all" (Question 13). Treat every hedge as deliberate.
- **Missing qualifiers.** External versus internal, personal versus aggregated, urgent versus routine - a single qualifying word can reverse the meaning of a sentence, as in Question 6.
- **Poor time management.** Spending too long absorbing the full passage before seeing the questions wastes time. Skim for structure, then hunt for the keywords each statement raises.
- **Overthinking explicit statements.** When the passage says the thing plainly (Question 14), answer True and move on. Second-guessing clear text costs time and marks.

## Workplace job-specific situational judgement assessment

### About this assessment

A workplace job-specific situational judgement assessment evaluates your decision-making, interpersonal skills, and professional conduct. Instead of testing logic or maths, it presents realistic workplace dilemmas - the kind you will genuinely meet as an associate data analyst in a UK government team - and asks how you would respond. It measures how well your choices align with the values and behaviours the organisation needs: user focus, transparency, collaboration, accessibility, inclusion, and integrity with data.

The format usually presents a short scenario followed by three to five possible responses. You are asked either to pick the **most effective** and **least effective** responses, or to rank or rate all the options. Timing is generous or absent, because the assessment cares about your natural judgement, not your speed. Importantly, there is often no perfectly right answer - several options may be reasonable - but there is usually a best answer for the role and culture, and usually one clearly weakest option.

For your level, scenarios typically explore: knowing when to work independently and when to seek supervision; handling data ethics and privacy concerns; communicating honestly about errors and uncertainty; working in a multi-disciplinary team; and balancing stakeholder pressure against quality standards. As an associate, the assessors are not expecting you to solve everything alone - in fact, options that show sensible use of supervision often score higher than heroic solo efforts. Equally, options that dodge responsibility, hide problems, or ignore user needs score poorly.

The public sector context matters. UK government organisations place strong weight on the Civil Service values of integrity, honesty, objectivity, and impartiality, alongside digital and data principles: meeting user needs, working in the open, protecting personal data, and making services accessible and inclusive. Keep these in mind as you judge each option.

### What it measures for your role

- **Escalation judgement** maps to **data ethics and privacy** ("identify appropriate channels to discuss ethical issues, with support") and to working "under supervision" across your skills: knowing when and how to involve others is a scored behaviour, not a weakness.
- **Honest communication about data** maps to **communicating between the technical and non-technical** and quality assurance in **applying statistical and analytical tools and techniques**: how you handle errors, caveats, and uncertainty under pressure.
- **Team collaboration** maps to your role-level duty to "work with others to understand roles within a multi-disciplinary team and how data analysts work with them".
- **User focus and inclusion** map to **data visualisation** ("develop inclusive, accessible data visualisations that recognise different user needs") and **delivering business impact through data**.
- **Adaptability** maps to **managing a data project**: "adapt your ways of working to deliver different project outcomes and requirements".

### Practice questions

For each scenario, decide which option is most effective and which is least effective before reading the explanation. There is real value in committing to an answer first - it reveals your instincts, which is exactly what the assessment measures.

#### Question 1 (easy) - A mistake in published figures

You notice that a chart you prepared last week, already circulated to the policy team, used the wrong month's data. The error makes performance look slightly better than it was. Nobody else has noticed. What do you do?

- A. Say nothing; the difference is small and the next report will use correct data anyway.
- B. Quietly correct the file in the shared folder so future viewers see the right version.
- C. Tell your supervisor promptly, explain the error and its size, and offer to send a correction to the policy team.
- D. Email the policy team directly with a correction before telling anyone in your own team.

**Most effective: C. Least effective: A.**

**Explanation:** Option C shows integrity, transparency, and appropriate use of supervision - the three things this scenario tests. You own the error, quantify it, and propose the fix, while letting your supervisor help judge the communication route: exactly right for an associate. Option A is the least effective because concealing a known error in circulated figures breaches honesty and objectivity, and small errors that surface later damage trust far more than prompt corrections do. Option B fixes the artefact but hides the fact that wrong figures informed readers - a silent correction is still concealment. Option D has honest intent but bypasses your team: your supervisor may know about downstream uses, and a correction sent without context can cause confusion. Promptness plus openness plus supervision is the pattern to remember.

#### Question 2 (easy) - An unclear request

A policy colleague asks you to "pull together some numbers on service usage for a meeting tomorrow". You are not sure which service, which time period, or what the meeting needs to decide. Your supervisor is available. What do you do?

- A. Ask the colleague two or three quick clarifying questions about the decision, service, and period before starting.
- B. Compile every usage statistic you can find so that whatever they need is somewhere in the pack.
- C. Guess the most likely interpretation and produce a focused summary based on it.
- D. Tell the colleague you cannot help without a properly written requirements document.

**Most effective: A. Least effective: D.**

**Explanation:** Option A treats the request as a problem statement to understand - which your role explicitly requires - and a few sharp questions ("What decision is the meeting making? Which service? Which months?") take minutes and prevent wasted hours. Option B produces an unfocused data dump that pushes the analytical work onto the reader; it feels safe but serves nobody, and it is the classic trap for new analysts. Option C at least produces something usable, but guessing when clarification was freely available is an unnecessary risk. Option D is the least effective: hiding behind process to refuse a reasonable colleague damages collaboration, and multi-disciplinary teamwork - a named duty at your level - means meeting people partway, not demanding paperwork for a simple query.

#### Question 3 (moderate) - Pressure to remove a caveat

A stakeholder reviewing your draft analysis asks you to delete the caveat noting that one region's data is incomplete, saying "it makes the report look weak and the gap is only small". Your supervisor is on leave today; the report is due tomorrow. What do you do?

- A. Remove the caveat; the stakeholder knows the audience better than you do.
- B. Keep the caveat, explain briefly why it protects the analysis and its readers, and offer to reword it more concisely if that helps.
- C. Refuse outright and escalate to the stakeholder's manager about pressure to alter analysis.
- D. Remove the caveat from the main page but leave the detail in a technical annex nobody reads.

**Most effective: B. Least effective: A.**

**Explanation:** Option B holds the professional line - honesty about data limitations is central to quality-assured statistical output - while staying collaborative: offering a tighter wording addresses the stakeholder's legitimate concern about presentation without sacrificing accuracy. Option A is least effective: silently dropping a known limitation misleads readers and, once discovered, undermines both your credibility and the team's. Option D is a subtler version of the same problem: burying a material caveat where readers will not see it is presentation-by-concealment. Option C jumps two steps too far - treating a first request as misconduct escalates conflict unnecessarily; escalation becomes right only if pressure continues after a reasoned refusal, and the natural first escalation would be to your own supervisor on their return, or a senior analyst today if the deadline forces the issue.

#### Question 4 (moderate) - A privacy concern in a shared dataset

While preparing a dataset for a colleague in another team, you notice it contains full names and dates of birth, although the analysis they described needs only age bands and regions. What do you do?

- A. Send the dataset as it is; the colleague works for the same department, so sharing is fine.
- B. Remove the identifying fields, send the minimised dataset with age bands and regions, and note what you removed and why.
- C. Decline to share anything until a full data protection impact assessment is completed.
- D. Send the full dataset but ask the colleague to delete the name and date of birth columns after receiving it.

**Most effective: B. Least effective: D.**

**Explanation:** Option B applies data minimisation - share only what the purpose needs - which is the heart of practical data ethics and privacy, a named skill for your role. Noting what you removed keeps the process transparent and invites correction if the colleague genuinely needs more (in which case the extra need can be justified properly). Option D is least effective because it transfers identifiable data unnecessarily and then relies on the recipient to fix the exposure after the fact - the risk has already happened by the time they delete anything. Option A wrongly assumes internal sharing needs no thought; purpose limitation applies inside organisations too. Option C is disproportionate for a straightforward minimisation case and blocks legitimate work; if you were unsure, the proportionate step would be a quick check with your supervisor or data protection contact - the "appropriate channels, with support" your skill description mentions.

#### Question 5 (moderate) - Disagreement in a multi-disciplinary team

In a sprint planning meeting, a user researcher says your proposed chart for the service dashboard "won't work for the people we interviewed - they found similar charts confusing". You spent significant time on the design and believe it is technically sound. What do you do?

- A. Defend your design firmly; the user researcher is not a data visualisation specialist.
- B. Ask the researcher what specifically confused users, and offer to test a revised version against those findings.
- C. Withdraw the chart entirely and let the researcher decide what replaces it.
- D. Agree in the meeting to keep the peace, but submit the original design unchanged.

**Most effective: B. Least effective: D.**

**Explanation:** Option B does what a strong multi-disciplinary team member does: treats user research as evidence, gets specific about the problem, and proposes an evidence-based iteration. It also directly serves your skill requirement to develop visualisations that recognise different user needs - the researcher is handing you exactly that insight. Option D is least effective because it is dishonest to the team and wastes the research: false agreement followed by unilateral action breaks trust in a way that is hard to repair. Option A treats specialism as territory; user evidence about confusion outranks technical elegance when the goal is a usable dashboard. Option C swings too far the other way - abandoning your expertise rather than combining it with the researcher's. Collaboration means both specialists contribute, and option B is the only choice where that happens.

#### Question 6 (moderate) - Struggling with an assigned task

You were asked to write a simple analysis script - a stretch task for you - and after a day and a half you are stuck. The script is due in three days. Your team includes a senior data analyst and a data engineer who both offered help when you started. What do you do?

- A. Keep working alone; asking for help now would show you were not ready for the task.
- B. Ask the senior analyst for a short pairing session, showing them what you have tried and where you are stuck.
- C. Ask the data engineer to write the script for you so the deadline is met.
- D. Tell your supervisor the task is impossible and ask for it to be reassigned.

**Most effective: B. Least effective: A.**

**Explanation:** Option B is exactly how your role level is designed to work: "develop analytical approaches... under supervision" and "work closely with other data professionals". Bringing what you have tried shows initiative and makes the help session efficient - you will finish the task, learn, and keep ownership. Option A is least effective because it risks the deadline to protect your image; struggling silently for days is one of the most common and most damaging habits in early-career analysts, and assessors specifically look for whether you avoid it. Option C meets the deadline but transfers the work and the learning - you would be no more capable next time. Option D declares defeat prematurely: the task was assigned as a stretch with support available, and escalating to reassignment before using that support wastes a development opportunity. Asking for help early and well is a strength at every level - especially yours.

#### Question 7 (challenging) - Conflicting priorities from two seniors

Your supervisor asked you to spend today finishing data cleansing for a project milestone. Mid-morning, a different senior manager messages you directly, asking you to produce urgent figures for a parliamentary question by 15:00. You cannot do both today. What do you do?

- A. Do the parliamentary question work; it sounds more senior and urgent, and explain to your supervisor tomorrow.
- B. Continue the cleansing as originally instructed; the senior manager should route requests through your supervisor.
- C. Tell your supervisor immediately about the new request, and let them agree the priority call with the senior manager.
- D. Try to do both by rushing the cleansing and cutting the quality checks.

**Most effective: C. Least effective: D.**

**Explanation:** Option C surfaces the conflict to the person accountable for your workload, quickly, so the two seniors can make an informed trade-off - which may well favour the parliamentary question, but that is their call to make with full information. This is textbook adaptability within managing a data project: priorities change, and the professional response is transparent re-planning, not silent guessing. Option D is least effective because it sacrifices quality assurance on milestone work while probably still rushing the urgent figures - the option that "does both" by degrading both is a recurring trap in situational tests. Option A makes a unilateral priority decision and leaves your supervisor exposed for a day; option B honours the original instruction but ignores a genuinely urgent organisational need and hides the conflict rather than raising it. When two legitimate demands collide, escalate the collision - immediately, not tomorrow.

#### Question 8 (challenging) - An accessibility shortcut under deadline

Your team is finalising a dashboard for launch tomorrow. You realise the colour scheme fails colour-contrast guidance and several charts rely on colour alone to distinguish categories - a barrier for colour-blind users. Fixing it properly needs about a day. The delivery manager wants to ship on time. What do you do?

- A. Ship as planned and add accessibility to the backlog for a future iteration.
- B. Raise the issue with the delivery manager and supervisor today, explain the user impact and the fix's size, and recommend either a one-day slip or shipping with the fixable elements corrected now.
- C. Stay silent and fix the charts quietly after launch when there is more time.
- D. Refuse to let the dashboard launch and tell the team accessibility law makes shipping illegal.

**Most effective: B. Least effective: C.**

**Explanation:** Option B treats accessibility as what it is in UK government digital work: a genuine user need and public sector obligation, not a nice-to-have - while respecting that the ship/slip decision belongs to the delivery manager and your supervisor once they have the facts. Recommending options (slip, or partial fix now) shows exactly the constructive, evidence-based behaviour your skill in inclusive, accessible data visualisation calls for. Option C is least effective: staying silent lets an avoidable barrier ship without the decision-makers ever knowing there was a choice - and quiet post-launch fixes may never happen. Option A at least is honest, but treating a known exclusion of users as backlog material undervalues inclusion; it might be the eventual team decision, but it should not be your opening recommendation. Option D raises a real concern in the worst way - as an ultimatum with a legal claim you are not placed to make; that damages your credibility even when your underlying point is sound.

#### Question 9 (challenging) - A tempting but doubtful finding

Exploring service data, you find a striking pattern: complaints appear to drop 40% in areas where a new process was piloted. Your team would love this to be true, and the programme board meets on Friday. But you notice the pilot areas also had a recording system change mid-period, which might explain some of the drop. What do you do?

- A. Present the 40% finding on Friday; it is what the data shows, and boards need good news.
- B. Present the finding alongside the recording-system caveat, and propose a quick check of the recording change's impact before firm conclusions are drawn.
- C. Withhold the finding entirely until a full evaluation is complete, telling the board nothing.
- D. Present the finding and mention the caveat only if someone asks about data quality.

**Most effective: B. Least effective: A.**

**Explanation:** Option B is honest, useful, and proportionate: the board hears the promising signal, understands the confounding factor, and gets a concrete plan to firm the evidence up. This is quality assurance in statistical insight - and it also serves business impact, because decisions made on inflated evidence eventually rebound on the service. Option A is least effective: presenting a figure you already doubt, without its known caveat, crosses from optimism into misleading analysis - the confound is not a technicality; it could explain much of the effect. Option D makes transparency conditional on being asked, which is concealment with a fig leaf. Option C errs in the opposite direction: boards can handle preliminary findings when they are labelled as such, and withholding everything delays learning. The professional pattern - show the signal, show the doubt, show the next step - is one of the most valuable habits you can build.

#### Question 10 (challenging) - Credit and visibility in a team

Your senior analyst presents your data preparation and visualisation work to the directorate, describing it as "the team's analysis" without mentioning you. A colleague urges you to complain to your supervisor about stolen credit. You had actually agreed the presentation content with the senior analyst beforehand. What do you do?

- A. Follow the colleague's advice and raise a formal concern about credit.
- B. Do nothing at all; visibility does not matter at your level.
- C. Reflect on whether "the team's analysis" was actually unfair, and if visibility matters to your development, ask the senior analyst or your supervisor how your contributions can be seen - for example, presenting a section next time.
- D. Add your name prominently to all future outputs before anyone reviews them.

**Most effective: C. Least effective: A.**

**Explanation:** Option C starts with perspective: team framing of collaborative work is normal and often right in government, and you had agreed the content in advance - so "stolen credit" is a strong reading of a routine event. But the option does not stop at acceptance: it channels the legitimate underlying need (development and visibility) into a constructive request, such as presenting next time - which also grows your communication skills. Option A is least effective because escalating a formal grievance over an agreed, conventional team presentation would damage your most important development relationship over a misreading - and taking a colleague's indignation as your evidence is not objective judgement. Option B swallows the feeling without addressing the development need; visibility does matter for growth, pursued the right way. Option D addresses the symptom unilaterally and slightly passive-aggressively. Situational tests often include a scenario like this to see whether you distinguish genuine mistreatment from ordinary teamwork - and whether you can advocate for yourself without conflict.

#### Question 11 (challenging) - Discovering a possible ethics issue

You are asked to link two datasets for an analysis of service uptake. During the work you realise the linkage would let analysts see individuals' benefit status alongside their health-related service use - a combination that feels more intrusive than the project described. You are not sure whether this was considered when the project was approved. What do you do?

- A. Complete the linkage as instructed; approval is someone else's responsibility.
- B. Pause that part of the work and raise your concern with your supervisor, asking whether the combination was covered by the project's approval.
- C. Anonymously report the project to the Information Commissioner's Office.
- D. Quietly leave the sensitive fields out of the linkage without telling anyone, so the issue disappears.

**Most effective: B. Least effective: C.**

**Explanation:** Option B is precisely what your data ethics and privacy skill describes: "identify appropriate channels to discuss ethical issues, with support". You are not expected to rule on the ethics yourself - you are expected to notice, pause proportionately, and ask the right person. Most likely the combination was considered and documented, and you will learn how such approvals work; if it was not, you have caught something important early. Option C is least effective: leaping to an external regulator before any internal question has been asked skips every appropriate channel, and would be seriously disproportionate for what may be a fully approved design. Option A ignores a legitimately noticed concern - "not my responsibility" is exactly the attitude ethics training tries to prevent. Option D unilaterally changes an approved analytical design in secret, which creates a different integrity problem: the analysis no longer matches its specification and nobody knows why. Notice and ask - with support - is the associate-level gold standard.

#### Question 12 (moderate) - Handling a repeated data quality problem

For the third month running, the extract you receive from a partner organisation arrives with the same formatting faults, and you spend half a day fixing them each time. Your fixes work, so nobody else is aware. What do you do?

- A. Keep fixing it each month; it works and it is only half a day.
- B. Document the recurring faults and your fixes, tell your supervisor, and suggest raising the issue with the partner so it is fixed at source.
- C. Email the partner organisation's team a complaint about their poor data quality.
- D. Stop fixing the faults so the problem becomes visible to everyone.

**Most effective: B. Least effective: D.**

**Explanation:** Option B turns silent heroics into system improvement: documentation captures the knowledge (a named value in your role - maintaining analytical approach documentation), your supervisor gains visibility of a recurring cost, and fixing at source could permanently recover half a day a month. This is "identify data quality issues and provide possible solutions" done properly. Option D is least effective: deliberately letting known-bad data flow onward to make a point harms the analysis and its users - manufacturing a failure is never the right way to gain attention for a problem. Option A is the quiet martyr option: it works today but hides a recurring cost and leaves the process fragile (what happens when you are on leave?). Option C addresses the right target with the wrong approach - cross-organisation data quality issues should go through agreed channels with your supervisor's knowledge, and a complaint framed without documentation invites defensiveness rather than a fix.

### Preparation tips

- **Learn your organisation's values, not just the framework.** Before an assessment, reread the Civil Service values (integrity, honesty, objectivity, impartiality) and the Government Digital Service standards on user needs and accessibility. Most scoring keys reward these directly.
- **Practise the "surface it early" instinct.** Across almost every scenario above, the strong option involves promptly telling the right person the true situation. If you notice you instinctively prefer waiting, practise reframing: early escalation is competence, not failure.
- **Use your real week as practice material.** When a small dilemma arises at work - an unclear request, a slipped deadline, a data doubt - pause and ask: what are my four options here, and which would an assessor score highest? Then discuss it with your mentor.
- **Answer as your best professional self, honestly.** Do not try to game the test with answers you would never carry out; inconsistency shows. The goal is genuine good judgement, which practice genuinely improves.
- **Remember your level.** Options involving supervision, pairing, and asking good questions are strengths for an associate. You are not being assessed on solving everything alone - you are being assessed on judgement about how to work.
- **Read every option fully before rating any.** Options are often designed in near-pairs (fix quietly versus fix openly). The differences between them are where the scoring lives.

### Common pitfalls

- **Choosing idealistic over practical.** "Refuse until a full impact assessment is complete" sounds principled but blocks legitimate work (Question 4). Effective options are proportionate to the actual risk.
- **Selecting passive options.** Saying nothing, waiting to be asked, adding it to the backlog, or hoping the next report fixes it - passive choices consistently score poorly because they leave the problem alive and hidden.
- **Confusing escalation with alarm.** Raising an issue with your supervisor is almost always strong; leaping to formal complaints, regulators, or ultimatums (Questions 3, 10, 11) is almost always weak as a first move.
- **Protecting image over outcomes.** Struggling alone rather than asking for help (Question 6) and silent corrections of your own errors (Question 1) both put how you look ahead of what users and colleagues need.
- **Ignoring the culture you are joining.** UK public sector scoring keys weight honesty, user needs, accessibility, and collaboration heavily. An option that hits a deadline by hiding a caveat or shipping a known barrier will rarely be the keyed answer.
- **Rushing the reading.** Scenario details - who offered help, what was already agreed, who is accountable - change which option is best. In Question 10, the fact that you had agreed the content beforehand transforms the scenario.

## Conclusion

Congratulations on working through this guide! You have covered a great deal of ground: what psychometric assessments are, how each of the four main types connects to your real work as an associate data analyst, and - most importantly - more than fifty practice questions grounded in the datasets, reports, policies, and workplace situations you genuinely encounter in UK government digital and data work.

A few messages are worth carrying with you. First, every one of these abilities is learnable. Numeric fluency grows with daily practice; precise reading becomes habit; pattern-spotting sharpens with every dataset you cleanse; and good judgement develops through reflection and honest conversations with the experienced professionals around you. The skills that make you score well are the same skills that make you good at your job - so preparation is never wasted, whatever the assessment outcome.

Second, remember your level and be proud of it. As an associate, you are supposed to be developing, supposed to ask questions, and supposed to work under supervision. The strongest candidates at your level are not the ones who know everything - they are the ones who read carefully, check their work, communicate honestly, and use the support around them well. That is what every section of this guide has really been about.

For next steps: revisit the sections where you found questions hardest, and space your practice out over days rather than cramming. Ask your supervisor or a senior analyst to talk through one or two of the situational scenarios with you - their war stories will teach you more than any answer key. Keep reading real government data policies and reports, keep recalculating figures in packs you receive, and keep a note of data quality issues you spot and how they were resolved.

You have chosen a career where curiosity, care, and clear thinking genuinely matter, and you are investing in exactly those qualities. Keep going - you are building the foundations of an excellent career in data. Good luck with your assessment!
