# Analytics Engineer (Trainee Analytics Engineer) - Psychometric Assessment Resources

## Introduction

Welcome! This guide has been written especially for you as a trainee analytics engineer working in the UK Government Digital and Data profession. Whether you are preparing for an assessment as part of a recruitment process, a development review, or simply because you want to understand your own strengths better, this document will help you feel prepared, confident, and calm.

First, a quick explanation. Psychometric assessments are structured tests that measure how you think and how you approach work situations. They are not tests of memory, and they are not designed to catch you out. Instead, they look at things like how you spot patterns, how you work with numbers, how carefully you read, and how you make judgements when situations are tricky. Employers use them because they are fair: everyone gets the same questions, and everyone is scored the same way. For someone at the start of their career, like you, they are also a brilliant learning tool, because practising them builds exactly the thinking habits you will use every day on the job.

As a trainee analytics engineer, your day-to-day work involves shadowing experienced colleagues, learning how your organisation's data fits together, handling simple queries from data users, writing down data requirements, executing test scripts under supervision, and contributing to data documentation. The assessments in this guide reflect that real work. Every practice question uses the kinds of tables, emails, policies, and workplace situations you will genuinely meet in a UK government data team. Nothing here requires knowledge you would not be expected to have.

This document is organised into four main sections, one for each assessment type:

1. **Workplace job-specific cognitive assessment** - pattern spotting, logical thinking, error checking, and prioritisation.
2. **Workplace job-specific numeric reasoning assessment** - working with tables, percentages, and the sorts of figures a data team handles.
3. **Workplace job-specific verbal reasoning assessment** - reading policies, emails, and standards carefully and drawing correct conclusions.
4. **Workplace job-specific situational judgement assessment** - choosing effective actions in realistic workplace dilemmas.

Each section explains what the assessment measures, links it to the specific skills in your role profile, gives you plenty of practice questions with full worked answers, and finishes with preparation tips and common pitfalls to avoid.

How should you use this guide? Take it slowly. Work through one section at a time, attempt each question honestly before reading the answer, and treat every explanation as a mini-lesson. If you get something wrong, that is genuinely useful: it shows you exactly where to focus. Come back to the questions after a week or two and see how much easier they feel. You are at the very start of an exciting career, and every bit of practice counts. Good luck - you can do this!

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive assessment measures the core mental processes you use in your role: spotting patterns, reasoning logically step by step, checking details for errors, prioritising tasks, and solving practical problems. Unlike a general intelligence test, it uses realistic workplace material - the actual kinds of tables, schedules, catalogues, and tickets you handle as a trainee analytics engineer - so it predicts how you will perform in the job itself, not how well you do abstract puzzles.

The format is usually online and timed, most often between 15 and 30 minutes, with multiple-choice questions. Questions typically get a little harder as you go. Your answers are scored objectively and compared against a benchmark group, and many employers look at both your speed and your accuracy rather than a single number. Before the real test begins you will normally get a few ungraded practice questions so you can get used to the screen layout - use them, and take a breath before you start.

Why does this matter for your role? An analytics engineer transforms data into structures that enable analysis and decision-making. Even as a trainee, you will be looking at data models, spotting when a column does not match its description, noticing that a scheduled data refresh has failed in a pattern, and deciding which of several user queries to deal with first. All of that is cognitive work. Practising these skills now will make you faster and more accurate on the job, as well as in the test.

### What it measures for your role

Each cognitive dimension maps directly to skills named in your role profile:

- **Pattern recognition** supports your skill in **data modelling, cleansing and enrichment**: recognising that tables follow industry-recognised patterns (such as star schemas from the Kimball approach) and noticing when data breaks an expected pattern.
- **Logical deduction** supports **data analysis and synthesis**: interpreting data to find key insights means drawing sound conclusions from what tables and figures actually show.
- **Error checking** supports **metadata management** and **testing**: maintaining information in metadata repositories and correctly executing test scripts both depend on careful, detail-level accuracy.
- **Prioritisation** supports **problem management**: investigating problems means judging whether an issue is strategic, tactical, or operational, and dealing with the most important things first.
- **Problem solving** supports **problem management** and **data innovation**: contributing to remedies and preventative measures, and spotting opportunities to do things in better ways.

### Practice questions

Work through these at your own pace first, then try them again under light time pressure (about 90 seconds per question). Answers and explanations follow each question - cover them up until you have committed to an answer.

**Question 1 (easy) - Pattern recognition in refresh schedules**

You are shadowing a senior analytics engineer who shows you the overnight refresh log for four datasets. The refresh completion times over the past four nights were:

- Monday: 02:10, Tuesday: 02:25, Wednesday: 02:40, Thursday: 02:55

If the pattern continues, what completion time should you expect on Friday?

A) 02:55
B) 03:10
C) 03:25
D) 02:40

**Correct answer: B**

**Explanation:** The completion time increases by 15 minutes each night: 02:10, 02:25, 02:40, 02:55. Adding another 15 minutes to Thursday's 02:55 gives 03:10. This is exactly the kind of drift a data team watches for, because if a refresh keeps finishing later each night, it may eventually overrun into working hours and users would see stale data. Spotting the pattern early lets you raise it with your mentor before it becomes a problem - a good example of contributing to preventative measures.

**Question 2 (easy) - Matching fields to documentation**

Your team's data documentation says the `customer_reference` field must always be 8 characters long, starting with two letters followed by six digits (for example, AB123456). Which of the following values breaks the rule?

A) CD654321
B) EF00 1234
C) GH111111
D) JK909090

**Correct answer: B**

**Explanation:** Option B contains a space, making it "EF00 1234", which is nine characters and does not follow the letters-then-digits pattern. Options A, C, and D each have two letters followed by six digits with no other characters. Checking real values against documented rules is core trainee work: when you maintain metadata repositories under direction, you are often the person who first notices that data does not match its own description. Read character by character - errors like a stray space are easy to miss when you skim.

**Question 3 (easy) - Logical deduction from a simple rule**

Your organisation's data standards say: "Every table in the reporting area must have an owner recorded in the metadata catalogue. Tables without an owner may not be used in published dashboards."

The table `benefit_claims_summary` is used in a published dashboard. What can you logically conclude?

A) The table has no owner recorded
B) The table has an owner recorded in the metadata catalogue
C) The dashboard is not published
D) The standards do not apply to this table

**Correct answer: B**

**Explanation:** The rule says tables without an owner may not be used in published dashboards. Since `benefit_claims_summary` is used in a published dashboard, it must have an owner recorded - otherwise the rule would be broken. This is deduction in its purest form: apply the stated rule to the stated fact, and only one conclusion follows. Be careful not to pick answers that add extra assumptions (like D, which invents an exemption the rule never mentions). In verbal and cognitive tests alike, stick strictly to what the material tells you.

**Question 4 (moderate) - Spotting the odd one out in a data model**

You are learning about dimensional modelling. Your mentor shows you four tables from a Kimball-style star schema for a licensing service and asks which one is the fact table (the table that records events or measurements, rather than descriptive attributes):

A) `dim_applicant` - columns: applicant_id, name, date_of_birth, region
B) `dim_licence_type` - columns: licence_type_id, category, description
C) `fct_application` - columns: application_id, applicant_id, licence_type_id, date_id, fee_paid, processing_days
D) `dim_date` - columns: date_id, day, month, year, is_working_day

**Correct answer: C**

**Explanation:** In a star schema, dimension tables (usually prefixed `dim_`) hold descriptive attributes such as names, categories, and dates, while the fact table (often prefixed `fct_`) records events with measurable values and keys pointing to the dimensions. `fct_application` contains keys to the applicant, licence type, and date dimensions, plus measures like `fee_paid` and `processing_days` - the classic shape of a fact table. Even at trainee level, your role profile asks you to show awareness of industry-recognised data modelling patterns, and recognising the fact/dimension distinction is the foundation of the Kimball approach.

**Question 5 (moderate) - Error checking a metadata catalogue entry**

You are asked to check a metadata catalogue entry against the source documentation. The documentation says:

- Dataset name: Housing Repairs Requests
- Update frequency: Daily at 06:00
- Data owner: Housing Operations Team
- Retention: 7 years
- Contains personal data: Yes

The catalogue entry reads:

- Dataset name: Housing Repairs Requests
- Update frequency: Daily at 06:00
- Data owner: Housing Operations Team
- Retention: 7 years
- Contains personal data: No

How many fields in the catalogue entry are incorrect?

A) 0
B) 1
C) 2
D) 3

**Correct answer: B**

**Explanation:** Compare field by field. Name matches, frequency matches, owner matches, retention matches. Only "Contains personal data" differs: the documentation says Yes, the catalogue says No. That is one incorrect field, so the answer is B. Notice how important this single error is in a UK government context: a dataset wrongly marked as containing no personal data could be handled without the safeguards that data protection law requires. Error checking is not just pedantry - in metadata management it protects real people. When you check entries, work through them methodically in order, ticking each field, rather than reading both blocks casually.

**Question 6 (moderate) - Prioritising user queries**

It is 09:15 on Monday. You handle simple queries from data users, and four have arrived. Your mentor is in meetings until noon. Which query should you deal with FIRST?

A) A policy analyst asks for a new column to be added to a data model "sometime this month"
B) A caseworker reports that this morning's operational dashboard is showing Friday's figures, and their team makes daily staffing decisions from it at 10:00
C) A colleague asks if you can share a template for documenting data requirements
D) A manager asks for a meeting next week to discuss training for new dashboard users

**Correct answer: B**

**Explanation:** Prioritisation questions ask you to weigh urgency and impact together. Option B is both urgent (a 10:00 decision deadline) and high impact (staffing decisions based on stale data could affect service delivery today). It is also an operational problem - the level of problem your role profile expects you to recognise. Option A has a month of slack; C is helpful but quick and not time-critical; D is about next week. A good response to B at trainee level would be to confirm the issue, check whether the overnight refresh failed, and escalate promptly if you cannot resolve it - handling it first does not mean handling it alone. In the test, look for the option where delay causes real harm soonest.

**Question 7 (moderate) - Following a test script sequence**

You are executing a test script under supervision. The script says:

1. Load the sample file into the staging table.
2. Run the transformation job.
3. Compare the row count of the output table with the control total in the test pack.
4. If the counts match, mark step 3 as passed; if not, record the difference and stop.
5. Only if step 3 passed, check that the `region` column contains no blank values.

You run the transformation, and the output table has 4,980 rows against a control total of 5,000. What should you do next?

A) Mark step 3 as passed and check the `region` column
B) Record the difference of 20 rows and stop
C) Re-run the transformation job until the counts match
D) Adjust the control total to 4,980 so the test passes

**Correct answer: B**

**Explanation:** The counts do not match (4,980 vs 5,000, a difference of 20 rows), so step 4 tells you exactly what to do: record the difference and stop. Option A skips ahead against the script's condition. Option C is not in the script - re-running jobs without instruction can hide genuine defects. Option D is the worst choice: changing the expected result to force a pass defeats the entire purpose of testing and would mislead your team. Your role profile says you correctly execute test scripts under supervision - "correctly" means following the script's logic precisely, including its stopping rules. Testing exists to find problems, and a failed step is the script working, not you failing.

**Question 8 (moderate) - Logical deduction across two rules**

Your team has two working agreements:

- Rule 1: All changes to shared data models must be reviewed by a senior analytics engineer before release.
- Rule 2: Trainees may prepare changes, but may not release them.

You have prepared a small change to a shared data model, and a senior analytics engineer has reviewed and approved it. Based only on these rules, which statement must be true?

A) You may now release the change yourself
B) The change may be released, but not by you
C) The change must be reviewed a second time
D) Trainees may not prepare changes to shared models

**Correct answer: B**

**Explanation:** Rule 1 is satisfied - the change has been reviewed by a senior analytics engineer. So the change may be released. But Rule 2 says trainees may not release changes, and you are a trainee, so the release must be done by someone else. Option A contradicts Rule 2. Option C invents a requirement that appears nowhere. Option D contradicts Rule 2, which explicitly allows trainees to prepare changes. Combining two rules correctly is a very common test pattern, and a very common workplace situation: real governance is rarely a single rule, and the safest habit is to check each rule in turn against the facts.

**Question 9 (moderate) - Error checking transformed values**

A transformation is supposed to convert dates from DD/MM/YYYY format to YYYY-MM-DD format. You spot-check five records:

| Input | Output |
|---|---|
| 05/03/2026 | 2026-03-05 |
| 12/01/2026 | 2026-01-12 |
| 09/11/2025 | 2025-09-11 |
| 30/06/2026 | 2026-06-30 |
| 01/02/2026 | 2026-02-01 |

Which output row is wrong?

A) Row 1
B) Row 3
C) Row 4
D) None - all rows are correct

**Correct answer: B**

**Explanation:** In row 3, the input 09/11/2025 means 9 November 2025 (day 09, month 11), so the correct output is 2025-11-09. The actual output, 2025-09-11, has swapped the day and month - it says 11 September instead. Rows 1, 2, 4, and 5 all convert correctly. Day/month swaps are among the most dangerous data quality errors because they only reveal themselves when the day is 12 or less (30/06 cannot be misread, but 09/11 can). Notice that four correct rows do not prove the transformation is right - a good checker examines every row, and a good analytics engineer would ask whether the test data includes dates that could expose this exact defect. This is data quality improvement in action.

**Question 10 (hard) - Deducing the source of a data problem**

Users report that Tuesday's sales figures on a dashboard are exactly double what they should be. You gather these facts while investigating:

- The dashboard reads from table `fct_sales_daily`.
- `fct_sales_daily` is loaded once per night by a single job.
- The job's log shows it ran twice on Tuesday night: once at 02:00 (scheduled) and once at 03:30 (manually triggered).
- The job appends rows; it does not replace them.
- Monday's and Wednesday's figures are correct, and the job log shows exactly one run on those nights.

What is the most likely cause of the doubled figures?

A) The dashboard is summing the wrong column
B) Tuesday's rows were loaded twice, and the append behaviour kept both copies
C) The source system sent double the sales on Tuesday
D) The dashboard cached Monday's figures

**Correct answer: B**

**Explanation:** Work through the evidence. The job ran twice on Tuesday (02:00 scheduled plus a 03:30 manual run), and it appends rather than replaces. Two appends of the same day's data means every Tuesday row exists twice, so any total for Tuesday doubles - which is exactly the symptom. Option A would affect every day, not just Tuesday. Option C is possible in theory, but the double job run is directly evidenced in the log and explains the doubling precisely; you should prefer the explanation the evidence supports. Option D would make Tuesday show Monday's figures, not doubled Tuesday figures. This is problem management at the operational level: match the symptom's shape (exactly double, one day only) to the mechanism that produces that shape. The preventative measure - making the job replace rather than blindly append, or adding a duplicate check - is the kind of remedy you would help implement.

**Question 11 (hard) - Prioritisation with dependencies**

You have four tasks on your list for today:

- Task 1: Document the data requirements from yesterday's meeting with a data user (needed by your mentor for a design session at 14:00).
- Task 2: Update three metadata catalogue entries your mentor marked as urgent for a compliance check happening tomorrow morning.
- Task 3: Prepare questions for the shadowing session you will attend at 15:30.
- Task 4: Read a background article about a new data transformation tool.

Task 1 will take about 2 hours, Task 2 about 1 hour, Task 3 about 30 minutes, and Task 4 about 1 hour. It is now 09:30. In what order should you tackle them?

A) 4, 3, 2, 1
B) 1, 2, 3, 4
C) 2, 1, 3, 4
D) 3, 4, 1, 2

**Correct answer: B**

**Explanation:** Check the deadlines against the clock. Task 1 is needed by 14:00 and takes 2 hours - starting at 09:30 gives comfortable slack, but it is the earliest hard deadline and the longest task, so start it first. Task 2 is needed tomorrow morning; doing it second (finishing around 12:30-13:30 allowing a break) leaves margin if problems appear. Task 3 must be done before 15:30 and takes only 30 minutes, so third is fine. Task 4 has no deadline at all - it is valuable development, but it goes last. Option C is tempting because Task 2 is labelled "urgent", but its real deadline is tomorrow, while Task 1's is 14:00 today; urgency labels matter less than actual deadlines. The general rule: order by real deadline, and give long tasks enough runway before their deadline.

**Question 12 (hard) - Pattern recognition in data quality metrics**

You are reviewing weekly data quality scores (percentage of records passing all checks) for a dataset:

- Week 1: 98.2, Week 2: 98.0, Week 3: 98.1, Week 4: 93.4, Week 5: 98.2, Week 6: 93.5, Week 7: 98.1, Week 8: 93.3

Weeks 4, 6, and 8 are the weeks immediately after a month-end. What is the most reasonable hypothesis to investigate first?

A) The data quality checks are randomly unreliable
B) Something in the month-end process introduces records that fail checks
C) Data quality is steadily declining over time
D) Weeks 5 and 7 were measured incorrectly

**Correct answer: B**

**Explanation:** The scores are not random and not declining - they alternate between a stable band around 98 and a lower band around 93.4, and the low weeks (4, 6, 8) all follow month-end. When a deviation lines up consistently with a known event, the event is your first hypothesis. Option A ignores the clear regularity; option C is contradicted by weeks 5 and 7 returning to 98; option D assumes the good weeks are the errors, with no supporting reason. As a trainee supporting data quality improvement, this is exactly how you turn a table of numbers into a key insight: describe the pattern, connect it to the operational calendar, and propose a focused investigation - "what does the month-end process load that ordinary weeks do not?"

**Question 13 (hard) - Problem solving with incomplete information**

A data user emails: "The figures in my report look wrong." That is all they say. You handle simple queries and document requirements. Which sequence of clarifying questions is the most logical order to establish the problem?

A) Which report? Which figures? What do you expect them to show, and what do they show instead? When did you last see them looking correct?
B) When did you last see them looking correct? Which report? What browser are you using? Which figures?
C) What do you expect them to show? Which report? Have you tried refreshing? Which figures?
D) Have you cleared your cache? Which figures? Which report? What do you expect?

**Correct answer: A**

**Explanation:** Good problem investigation narrows from the general to the specific: first identify the object (which report), then the location of the issue (which figures), then define the gap (expected versus actual - a problem is always a difference between the two), then establish the timeline (when it was last correct, which brackets when the problem started). Options B, C, and D all jump to specifics or fixes (browser, cache, refreshing) before knowing what the problem even is. Documenting the expected-versus-actual gap and the timeline gives whoever picks up the investigation - possibly a senior engineer - exactly what they need. Writing this down clearly is also your communicating-between-technical-and-non-technical skill at work: the user said "looks wrong"; your questions turn that feeling into evidence.

**Question 14 (moderate) - Spotting an innovation opportunity**

Over your first month you notice that every time a data user asks for a new field, the team follows the same manual steps: the request arrives by email, someone copies it into a spreadsheet, someone else retypes it into the work-tracking tool, and the requirements document is updated by hand. Last week two requests were lost between the spreadsheet and the tracking tool. Which observation, raised with your mentor, best identifies the underlying improvement opportunity?

A) "People should be more careful when they copy requests between systems"
B) "The same information is manually re-entered three times, and each hand-off is a chance to lose or corrupt a request - could we capture requests once, in a single structured form that feeds the tracker?"
C) "We should stop accepting requests by email"
D) "We need more staff to handle the volume of requests"

**Correct answer: B**

**Explanation:** Option B does three things well: it names the pattern (the same data re-entered three times), explains the mechanism of failure (each hand-off is an error opportunity - proven by the two lost requests), and proposes a direction without over-claiming a solution. That is what your data innovation skill looks like at trainee level: awareness of an opportunity, expressed clearly. Option A blames individuals for a process problem - errors caused by repeated manual re-entry are designed into the process, not caused by carelessness. Option C removes a channel users rely on without solving the duplication. Option D adds cost to a broken process instead of fixing it. In cognitive tests, "best" options usually describe the cause, not just the symptom, and propose proportionate action.

### Preparation tips

- **Practise with real artefacts.** Ask your mentor if you can look at a real refresh log, a metadata catalogue entry, or a test script. The more familiar these formats feel, the faster you will read them in a test.
- **Build a checking routine.** For error-checking questions, always compare items field by field or character by character, in the same order every time. Routines beat rereading.
- **Say the rule back to yourself.** For deduction questions, paraphrase the rule in your own words before applying it. If you cannot paraphrase it, read it again.
- **Time yourself gently at first.** Accuracy first, then speed. Once you are getting questions right, practise at about a minute per question.
- **Rest and set up properly.** Do the test somewhere quiet, on a reliable connection, after a decent night's sleep. These basics genuinely move scores.
- **Use the practice questions.** Almost every platform offers ungraded warm-up questions. Never skip them - they settle nerves and teach you the interface.

### Common pitfalls

- **Adding your own assumptions.** The single most common error: answering from what you think is usually true rather than what the question states. Every fact you need is on the screen.
- **Rushing the easy questions.** Careless slips on easy items cost as much as failures on hard ones. Bank the easy marks carefully.
- **Getting stuck on one hard question.** If a question is eating your time, make your best choice, flag it if the platform allows, and move on. A cognitive test rewards steady progress across many questions.
- **Ignoring stated formats and units.** A question about an 8-character reference or a DD/MM/YYYY date turns entirely on format details. Slow down whenever a format is specified.
- **Second-guessing into errors.** Your first carefully reasoned answer is usually right. Change an answer only when you can point to the specific thing you misread.


## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment measures how well you analyse, interpret, and make sound decisions using numerical data. The maths itself is deliberately modest - percentages, ratios, averages, and simple projections - because the real skill being tested is interpretation: reading a table correctly, extracting the right figures, applying the right operation, and sanity-checking the result. Question inputs look like the material you meet at work: row counts, data quality scores, refresh durations, storage figures, licence costs, and usage statistics.

Typical formats are online, multiple-choice, and timed - often 20 to 30 questions in 20 to 30 minutes, so roughly a minute per question. Most assessments allow or provide an onscreen calculator, because they care about your reasoning rather than mental arithmetic. Expect strict time pressure: quick, accurate data extraction matters as much as the calculation.

Why does this matter for a trainee analytics engineer? Numbers are the raw material of your whole profession. When you support data quality improvement, you compare pass rates. When you help document a data model, you reason about row volumes and growth. When you handle a user query about a figure that "looks wrong", you need to check the arithmetic yourself before escalating. Being comfortable and careful with workplace numbers is not an optional extra in this role - it is the job, and this assessment simply samples it.

### What it measures for your role

- **Interpreting tables and percentages** maps to your **data analysis and synthesis** skill: interpreting data to find key insights starts with reading figures accurately and computing simple comparisons.
- **Data quality arithmetic** (pass rates, missing-value percentages, duplicates) maps to **data modelling, cleansing and enrichment** and to supporting **data quality improvement**: you cannot improve what you cannot measure.
- **Counts and completeness figures** map to **metadata management**: metadata repositories are full of numbers - record counts, field counts, coverage percentages - that you help keep accurate under direction.
- **Test results arithmetic** maps to your **testing** skill: comparing actual against expected counts and calculating pass rates is the numeric heart of executing test scripts.
- **Trend and comparison questions** map to **problem management**: sizing a problem (how big, how fast is it growing, which level - operational, tactical, strategic) is a numerical judgement.
- **Explaining a calculation simply** maps to **communicating between the technical and non-technical**: several explanations below model how to walk a non-technical user through arithmetic.

### Practice questions

Use a calculator if you like - most real tests allow one. The explanations show every step of the arithmetic, because writing out steps is a habit worth building.

**Question 1 (easy) - Percentage of records passing checks**

A dataset contains 12,500 records. Data quality checks flag 375 records as failing. What percentage of records passed the checks?

A) 3%
B) 95%
C) 97%
D) 96.5%

**Correct answer: C**

**Explanation:** First find the failure rate: 375 ÷ 12,500 = 0.03, which is 3%. Records passing are therefore 100% − 3% = 97%. You can verify directly: 12,500 − 375 = 12,125 passing records, and 12,125 ÷ 12,500 = 0.97 = 97%. Option A is the trap for anyone who stops after the first step - the question asks for the pass rate, not the fail rate. Always reread the final sentence of a numeric question before answering: computing the right number to the wrong question is the most common error of all.

**Question 2 (easy) - Reading a metadata coverage table**

Your team tracks how many datasets in the catalogue have complete metadata:

| Quarter | Datasets in catalogue | With complete metadata |
|---|---|---|
| Q1 | 200 | 120 |
| Q2 | 220 | 143 |
| Q3 | 250 | 175 |

What was the metadata completeness percentage in Q3?

A) 65%
B) 70%
C) 75%
D) 80%

**Correct answer: B**

**Explanation:** Completeness in Q3 = 175 ÷ 250 = 0.70 = 70%. For context, Q1 was 120 ÷ 200 = 60% and Q2 was 143 ÷ 220 = 65%, so completeness is improving by five percentage points each quarter - a pattern worth noticing, and exactly the kind of insight your team would want highlighted when you contribute to data documentation. Be careful to divide by the right denominator: 175 ÷ 200 (using Q1's catalogue size) gives 87.5%, a wrong answer produced by mixing rows of the table.

**Question 3 (easy) - Simple ratio in user queries**

Last month your team received 84 user queries. They were split between "access requests", "data questions", and "error reports" in the ratio 3 : 2 : 2. How many were error reports?

A) 12
B) 24
C) 36
D) 28

**Correct answer: B**

**Explanation:** The ratio 3 : 2 : 2 has 3 + 2 + 2 = 7 parts. Each part is 84 ÷ 7 = 12 queries. Error reports are 2 parts: 2 × 12 = 24. (Access requests are 3 × 12 = 36 and data questions 2 × 12 = 24; check: 36 + 24 + 24 = 84.) Ratio questions are quick marks once you know the routine: total the parts, divide, multiply. Always do the final check-sum if you have a few seconds spare - it catches slips immediately.

**Question 4 (moderate) - Percentage change in dashboard usage**

A dashboard you help support had 1,250 unique users in June and 1,450 in July. What was the percentage increase, to one decimal place?

A) 13.8%
B) 16.0%
C) 20.0%
D) 12.5%

**Correct answer: B**

**Explanation:** Percentage change = (new − old) ÷ old × 100 = (1,450 − 1,250) ÷ 1,250 × 100 = 200 ÷ 1,250 × 100 = 16.0%. Option A (13.8%) comes from dividing by the new value (200 ÷ 1,450) - a classic error. The rule to memorise: percentage change is always measured against the starting value. When you report usage growth to a service owner, this is also a moment for your communication skill: "usage grew 16% month on month, from 1,250 to 1,450 users" gives the percentage and the absolute numbers, so a non-technical reader gets the full picture.

**Question 5 (moderate) - Missing values across columns**

A table has 40,000 rows. You profile three columns:

- `postcode`: 2,000 missing values
- `date_of_birth`: 1,200 missing values
- `region`: 3,600 missing values

Which column has the highest percentage of missing values, and what is that percentage?

A) postcode, 5%
B) region, 9%
C) date_of_birth, 3%
D) region, 12%

**Correct answer: B**

**Explanation:** Each column has the same 40,000-row denominator, so: postcode = 2,000 ÷ 40,000 = 5%; date_of_birth = 1,200 ÷ 40,000 = 3%; region = 3,600 ÷ 40,000 = 9%. The highest is region at 9%. Option D's 12% would require 4,800 missing values - it is a distractor for anyone who miskeys the division. Profiling missing values like this is one of the first practical tasks in data cleansing: percentages let you compare columns fairly and decide where quality improvement effort should go first.

**Question 6 (moderate) - Test pass rates across two runs**

You execute a test script with 60 test cases; 48 pass. After fixes, you re-run it and 57 pass. By how many percentage points did the pass rate improve?

A) 9 percentage points
B) 15 percentage points
C) 18.75 percentage points
D) 12 percentage points

**Correct answer: B**

**Explanation:** First run: 48 ÷ 60 = 0.80 = 80%. Second run: 57 ÷ 60 = 0.95 = 95%. Improvement = 95% − 80% = 15 percentage points. Note the wording: "percentage points" means the simple difference between two percentages. Option C (18.75%) is the relative increase (15 ÷ 80 × 100) - a correct calculation of a different quantity. Tests love this distinction, and so do real reports: saying "pass rate rose 15 percentage points to 95%" is precise; saying "improved 15%" is ambiguous. Precision with numbers is precision in communication.

**Question 7 (moderate) - Storage growth projection**

A reporting database currently uses 480 GB of storage and is growing by 5% per month. Approximately how much storage will it use in two months?

A) 528.0 GB
B) 529.2 GB
C) 504.0 GB
D) 540.0 GB

**Correct answer: B**

**Explanation:** Growth compounds. After one month: 480 × 1.05 = 504 GB. After two months: 504 × 1.05 = 529.2 GB. Option A (528 GB) comes from adding 5% of the original figure twice (480 + 24 + 24), ignoring compounding; option C is only one month's growth; option D assumes 12.5% total. The compound formula is 480 × 1.05² = 480 × 1.1025 = 529.2. Growth projections like this feed real capacity decisions - a team that plans storage with simple addition will run out sooner than expected. When a percentage is applied "per month" or "per year", assume compounding unless told otherwise.

**Question 8 (moderate) - Refresh duration averages**

The nightly transformation job's run times this week were:

- Monday: 42 minutes, Tuesday: 38 minutes, Wednesday: 45 minutes, Thursday: 51 minutes, Friday: 44 minutes

What was the mean run time, and on how many nights did the job run longer than the mean?

A) Mean 44 minutes; 2 nights
B) Mean 44 minutes; 3 nights
C) Mean 45 minutes; 2 nights
D) Mean 43 minutes; 3 nights

**Correct answer: A**

**Explanation:** Sum the times: 42 + 38 + 45 + 51 + 44 = 220 minutes. Mean = 220 ÷ 5 = 44 minutes. Nights above 44 minutes: Wednesday (45) and Thursday (51) - that is 2 nights. Friday's 44 equals the mean, so it does not count as "longer than". Two-part questions like this reward working systematically: compute the first quantity, write it down, then answer the second part against it. In the workplace, knowing the average run time (and which nights exceed it) is how you would notice that Thursday's 51 minutes deserves a closer look - it is 7 minutes, or about 16%, above the mean.

**Question 9 (moderate) - Licence cost comparison**

Your team is comparing two data documentation tools:

- Tool A: £15 per user per month
- Tool B: £150 per user per year

For a team of 12 users, how much more does the more expensive tool cost per year?

A) £180
B) £360
C) £30
D) £2,160

**Correct answer: B**

**Explanation:** Tool A per year: £15 × 12 months = £180 per user, × 12 users = £2,160. Tool B per year: £150 × 12 users = £1,800. Difference: £2,160 − £1,800 = £360, with Tool A the more expensive. The essential move is converting both prices to the same basis (per year, whole team) before comparing - mixing monthly and annual figures is exactly the "misreading labels" pitfall the test designers plant. Option C (£30) is the per-user annual difference (£180 − £150); read whether the question asks per user or per team. Cost comparisons like this appear whenever a team evaluates new tools - part of showing awareness of innovation opportunities is being able to cost them honestly.

**Question 10 (hard) - Duplicate records after a merge**

Two source extracts are merged into one table. Extract 1 has 18,400 records; Extract 2 has 9,600 records. After merging, the table has 26,750 records, because records appearing in both extracts were included only once. How many records appeared in both extracts?

A) 1,250
B) 2,500
C) 1,600
D) 950

**Correct answer: A**

**Explanation:** If there were no overlap, the merged table would have 18,400 + 9,600 = 28,000 records. The actual table has 26,750, which is 28,000 − 26,750 = 1,250 fewer. Each record that appears in both extracts is counted once instead of twice, reducing the total by exactly one per overlapping record - so 1,250 records appeared in both. This overlap logic underpins deduplication work in data cleansing, and it is also how you would sanity-check a merge in a test script: expected count = sum of sources minus known duplicates. If the arithmetic does not reconcile, something in the transformation needs investigating.

**Question 11 (hard) - Weighted data quality score**

A dataset's overall quality score is a weighted average of three dimensions:

| Dimension | Score | Weight |
|---|---|---|
| Completeness | 90 | 50% |
| Accuracy | 80 | 30% |
| Timeliness | 70 | 20% |

What is the overall score?

A) 80.0
B) 83.0
C) 84.5
D) 81.5

**Correct answer: B**

**Explanation:** Multiply each score by its weight and sum: (90 × 0.5) + (80 × 0.3) + (70 × 0.2) = 45 + 24 + 14 = 83. Option A (80) is the simple unweighted average of 90, 80, and 70 - the trap for ignoring the weights. Weighted scores are everywhere in data quality frameworks because not all dimensions matter equally for every dataset: a daily operational dataset might weight timeliness far higher. Check that weights sum to 100% (50 + 30 + 20 = 100, so they do) before you calculate; if they did not, you would need to divide by the total weight.

**Question 12 (hard) - Capacity for user training sessions**

You are helping organise dashboard training. Each session holds a maximum of 8 attendees and needs one facilitator. There are 75 users to train, and two facilitators each able to run at most 2 sessions per week. What is the minimum number of weeks needed to train everyone?

A) 2 weeks
B) 3 weeks
C) 4 weeks
D) 5 weeks

**Correct answer: B**

**Explanation:** Sessions needed: 75 ÷ 8 = 9.375, and you cannot run a fraction of a session, so round UP to 10 sessions (9 sessions would cover only 72 users). Capacity per week: 2 facilitators × 2 sessions = 4 sessions. Weeks needed: 10 ÷ 4 = 2.5, again rounded UP to 3 weeks (after 2 weeks only 8 sessions have run, covering at most 64 users). The recurring trick in capacity questions is that people and sessions come in whole units, so you round up at every stage, never down and never to the nearest. Contributing to user training is in your role profile, so this scenario may feel familiar sooner than you think.

**Question 13 (hard) - Interpreting a query-volume trend**

Monthly user queries handled by your team:

| Month | Queries |
|---|---|
| March | 120 |
| April | 132 |
| May | 145 |
| June | 160 |

Approximately what is the average monthly growth rate, and roughly how many queries should the team expect in July if the trend continues?

A) About 10% per month; roughly 176 queries
B) About 13% per month; roughly 181 queries
C) About 10% per month; roughly 170 queries
D) About 8% per month; roughly 173 queries

**Correct answer: A**

**Explanation:** Check each month's growth: April 132 ÷ 120 = 1.10 (10.0%); May 145 ÷ 132 ≈ 1.098 (9.8%); June 160 ÷ 145 ≈ 1.103 (10.3%). The growth rate is consistently about 10% per month. July projection: 160 × 1.10 = 176. Option C pairs the right rate with a wrong projection (adding 10 rather than 10%). A steady 10% monthly rise in queries is a genuine operational insight: it suggests demand will roughly double in about seven to eight months, which the team should plan for - perhaps with more self-service documentation, another duty your role contributes to. Numbers become insights when you project them forward and ask "what should we do about this?"

**Question 14 (hard) - Reconciling row counts through a pipeline**

A pipeline processes records in three steps:

- Step 1 (validation) rejects 4% of the 50,000 input records.
- Step 2 (deduplication) removes 600 records from what remains.
- Step 3 (enrichment) adds no records and removes no records.

How many records should the final table contain, and what percentage of the original input is that (to one decimal place)?

A) 47,400 records; 94.8%
B) 48,000 records; 96.0%
C) 47,400 records; 94.0%
D) 46,800 records; 93.6%

**Correct answer: A**

**Explanation:** Step 1: 4% of 50,000 = 2,000 rejected, leaving 50,000 − 2,000 = 48,000. Step 2: 48,000 − 600 = 47,400. Step 3: no change, so the final table holds 47,400 records. As a percentage of input: 47,400 ÷ 50,000 = 0.948 = 94.8%. Option B stops after step 1; option D wrongly takes the 600 as a further percentage. Multi-step reconciliation like this is precisely what a control-total check in a test script does, and being able to predict the expected count at every stage is what lets you locate a fault: if the final table held 47,000, you would know 400 records vanished somewhere they should not have, and the step-by-step expected counts tell you where to look.

**Question 15 (moderate) - Explaining a figure to a non-technical user**

A caseworker emails: "Your dashboard says our completion rate fell from 92% to 88%, but we completed MORE cases this month - 440 against 414 last month. The dashboard must be broken!" Last month the team received 450 cases; this month they received 500. Is the dashboard wrong?

A) Yes - completions rose, so the rate must have risen
B) No - 414 ÷ 450 = 92% and 440 ÷ 500 = 88%; completions rose, but cases received rose faster
C) Cannot be determined from these figures
D) Yes - the rate should be 95%

**Correct answer: B**

**Explanation:** Check both rates. Last month: 414 ÷ 450 = 0.92 = 92%. This month: 440 ÷ 500 = 0.88 = 88%. The dashboard is correct: the team completed 26 more cases (440 − 414), but received 50 more (500 − 450), so the completion rate still fell. A rate depends on both numerator and denominator - more completions with an even faster rise in demand means a lower rate. This is a beautiful example of why your communication skill matters: the caseworker is not being difficult, they are reading one number without the other. A reply such as "You did complete more cases - great work - but the team also received 50 more cases than last month, so the percentage completed dipped" resolves the query, builds trust, and turns a complaint into understanding.

**Question 16 (hard) - Choosing where quality effort pays off most**

You can spend your data-cleansing time this week on ONE of three tables. Fixing a table moves all its failing records to passing:

| Table | Records | Currently failing | Used by dashboards |
|---|---|---|---|
| Table X | 5,000 | 500 | 12 |
| Table Y | 60,000 | 1,800 | 3 |
| Table Z | 20,000 | 1,600 | 6 |

Your mentor says: "Prioritise the biggest improvement in failing records per dashboard-using table - divide failing records by number of dashboards and fix the table with the LOWEST reach per failure... actually, just tell me which table has the highest failure rate." Which table has the highest failure rate?

A) Table X
B) Table Y
C) Table Z
D) They are all equal

**Correct answer: A**

**Explanation:** Failure rates: Table X = 500 ÷ 5,000 = 10%; Table Y = 1,800 ÷ 60,000 = 3%; Table Z = 1,600 ÷ 20,000 = 8%. Table X has the highest failure rate at 10%, even though Table Y has the most failing records in absolute terms (1,800). This distinction - absolute counts versus rates - decides many real prioritisation debates: Y has the biggest pile of bad records, but X is proportionally the least trustworthy table, and it feeds the most dashboards (12), so its errors spread furthest. Note also the realistic detail that your mentor's instructions changed mid-message; in tests, as at work, answer the question actually asked at the end, not the one you expected. If an instruction genuinely confuses you at work, asking for clarification is a strength, not a weakness.

**Question 17 (easy) - Time available for documentation**

Your working day runs 09:00 to 17:00 with a one-hour lunch break. Today you have a 90-minute training session, a 30-minute team stand-up, and two hours reserved for executing test scripts. How much time remains for documentation work?

A) 2 hours
B) 2.5 hours
C) 3 hours
D) 3.5 hours

**Correct answer: C**

**Explanation:** Total working time: 09:00 to 17:00 is 8 hours, minus the 1-hour lunch leaves 7 hours. Commitments: 1.5 hours (training) + 0.5 hours (stand-up) + 2 hours (testing) = 4 hours. Remaining: 7 − 4 = 3 hours. The only trap is forgetting to subtract lunch (giving 4 hours, not offered) or mis-converting 90 minutes into 1.5 hours. Simple time arithmetic like this underlies every honest answer to "can you have it by Friday?" - and giving realistic estimates, rather than optimistic ones, is a habit worth forming in your first year.

### Preparation tips

- **Refresh the core four.** Percentages, percentage change, ratios, and averages cover most questions. Practise each until the method is automatic, then speed comes free.
- **Write the formula before the numbers.** Even in a timed test, jotting "(new − old) ÷ old" takes two seconds and prevents the most common errors.
- **Round up for people and sessions.** Whenever a question involves whole units - sessions, staff, batches - remind yourself that partial units round up.
- **Practise reading tables fast.** Give yourself ten seconds to answer: what are the rows, what are the columns, what are the units? Only then read the question.
- **Use the calculator wisely.** A calculator prevents arithmetic slips but not reasoning slips. The thinking - which numbers, which operation, which denominator - is still yours.
- **Estimate first.** A rough mental estimate ("about 16%... so not 13.8%") lets you reject wrong options instantly and catch keying errors.

### Common pitfalls

- **Misreading scale qualifiers and units.** "In thousands", "per user per month", "GB" versus "TB" - a wrong unit turns a right method into a wrong answer. Underline units as you read.
- **Dividing by the wrong base.** Percentage change uses the OLD value; column completeness uses THAT column's row count. Ask "out of what?" every single time.
- **Mixing percentages with percentage points.** A rise from 80% to 95% is 15 percentage points but an 18.75% relative increase. Match your calculation to the question's exact wording.
- **Over-calculating.** If the options are far apart, estimation is faster and safer than long division. Not every question deserves full precision.
- **Sinking time into one multi-stage question.** A hard three-step calculation is worth the same as an easy one-step question. If you are stuck after 90 seconds, choose your best estimate and move on.
- **Ignoring compounding.** Repeated percentage growth multiplies; it does not add. Two months of 5% growth is ×1.1025, not +10%.


## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment measures how well you understand, analyse, and draw correct conclusions from written material - and, just as importantly, how well you resist drawing conclusions the text does not support. The passages mirror the reading you actually do in this role: data standards, metadata policies, emails from data users, testing procedures, and internal guidance documents.

The most common format gives you a short, dense passage followed by statements you must judge as **True** (the passage says so), **False** (the passage says the opposite), or **Cannot Say** (the passage gives insufficient information either way). Some tests add multiple-choice comprehension questions about the main point or a specific detail. Timing is tight - typically less than a minute per question - so the test also samples your ability to read purposefully under deadline pressure, just as you do when a user is waiting on a reply.

The golden rule throughout: answer using ONLY the passage. Your outside knowledge, however good, is switched off for the duration. If the passage does not state or logically require something, the answer is Cannot Say - even if you happen to know it is true in real life.

Why does this matter for a trainee analytics engineer? Your role runs on precise reading. You translate what subject matter experts say into data structures, so misreading a requirement becomes a mis-built model. You maintain metadata under direction, so a policy sentence about retention or personal data must mean exactly what it says. You document requirements and contribute to user training materials, so you must notice the difference between "must", "should", and "may". Careful reading is quietly one of the most valuable skills in your whole profession.

### What it measures for your role

- **Comprehension of policies and standards** maps to **data modelling, cleansing and enrichment** and **metadata management**: standards documents define what "complete" metadata or a "conformed" model means, and you must apply their exact wording.
- **Distinguishing stated fact from assumption** maps to **data analysis and synthesis**: finding key insights means separating what the evidence says from what you merely expect.
- **Reading user emails accurately** maps to **communicating between the technical and non-technical**: understanding a non-technical user's real question is the first half of answering it well.
- **Following procedural text** maps to **testing** and **problem management**: test scripts and incident procedures are instructions whose exact wording determines what you do.
- **Judging what a document does NOT say** maps to documenting requirements: a requirement that is not written down does not exist, and spotting gaps is part of refining requirements in response to feedback.

### Practice questions

Each passage below is followed by several statements or questions. Read the passage once carefully, then answer strictly from its wording. Explanations quote the exact phrases that decide each answer.

**Passage 1 - Extract from the departmental Data Documentation Standard**

"All datasets published to the analytical platform must have a completed catalogue entry before first publication. A completed entry includes the dataset name, a plain-English description, the data owner, the update frequency, and a data quality statement. Entries must be reviewed at least once every twelve months. Trainee staff may draft and update catalogue entries, but each entry must be approved by the data owner before it becomes visible to platform users. Datasets containing personal data must additionally record their lawful basis for processing; such datasets may not be published until the lawful basis field is complete."

**Question 1 (easy):** True, False, or Cannot Say: A dataset may be published to the analytical platform before its catalogue entry is completed.

**Correct answer: False**

**Explanation:** The first sentence states datasets "must have a completed catalogue entry before first publication". The statement directly contradicts this, so it is False. Note the difference between False and Cannot Say: here the passage explicitly rules the statement out, which is what False requires. If the passage had said nothing about timing, the answer would be Cannot Say.

**Question 2 (easy):** True, False, or Cannot Say: Trainee staff may draft catalogue entries.

**Correct answer: True**

**Explanation:** The passage says, word for word, "Trainee staff may draft and update catalogue entries". The statement is a subset of exactly what the text permits, so it is True. Easy marks like this reward locating the governing sentence quickly - scan for the keyword "trainee" rather than rereading the whole passage.

**Question 3 (moderate):** True, False, or Cannot Say: Catalogue entries are reviewed by the data owner every twelve months.

**Correct answer: Cannot Say**

**Explanation:** Two separate claims are bundled here. The passage does say entries "must be reviewed at least once every twelve months" - but it never says WHO performs that review. The data owner approves entries before they become visible, but approval and the annual review are described separately, and the reviewer's identity is simply not stated. Because part of the statement (the data owner performing the review) is neither confirmed nor denied, the answer is Cannot Say. Watch for statements that weld a true fact to an unstated detail - they are the classic Cannot Say construction.

**Question 4 (moderate):** True, False, or Cannot Say: A dataset containing personal data with an empty lawful basis field may be published if the data owner approves its catalogue entry.

**Correct answer: False**

**Explanation:** The final sentence is decisive: "such datasets may not be published until the lawful basis field is complete." The condition is absolute - owner approval is a separate requirement and does not override it. The statement claims publication is possible with the field empty, which the passage expressly forbids, so it is False. In your metadata work this is exactly the kind of rule you will apply: some conditions in governance documents are gates, not preferences, and the word "until" marks the gate.

**Question 5 (moderate) - Multiple choice:** Which of the following best summarises the main purpose of the passage?

A) To explain how to use the analytical platform
B) To set out what a catalogue entry must contain and the conditions for publication and approval
C) To restrict trainees from working on documentation
D) To describe how to process personal data lawfully

**Correct answer: B**

**Explanation:** The passage's content is: required fields of a completed entry, review timing, who may draft and who must approve, and an extra publication condition for personal data. Option B captures all of that. Option A overreaches - the platform itself is barely mentioned. Option C is contradicted: trainees are explicitly permitted to draft and update. Option D describes one sentence, not the passage's purpose. For main-purpose questions, choose the option that covers the most content without adding anything - answers that are "too big" or "too small" are both wrong.

**Passage 2 - Email from a data user**

"Hi - I'm a performance analyst in the operations directorate. I've been using the monthly caseload model for about a year, and it has always given me what I need. However, our director has now asked for the same figures broken down by week, and I can't see any way to do that with the current model. I appreciate this might be a big change, and I don't need it before the end of next month. Could you let me know whether a weekly breakdown is possible, and if so, what you would need from me? One more thing: a colleague mentioned that the regional filter sometimes shows an extra region called 'Unknown' - I haven't seen it myself, but you might want to check."

**Question 6 (easy):** True, False, or Cannot Say: The analyst needs the weekly breakdown before the end of this month.

**Correct answer: False**

**Explanation:** The email says "I don't need it before the end of next month" - the deadline is the end of NEXT month, so needing it before the end of THIS month contradicts the text. One small word carries the whole answer; when you document this requirement for your team, the deadline you record must be the one the user wrote, not the one you half-remembered. Careful reading and accurate requirement documentation are the same skill.

**Question 7 (moderate):** True, False, or Cannot Say: The regional filter contains a fault that displays an extra region.

**Correct answer: Cannot Say**

**Explanation:** The email reports second-hand information with explicit uncertainty: "a colleague mentioned" the extra region, and the writer adds "I haven't seen it myself". The passage establishes only that a possible issue was reported, not that a fault exists. Treating a report as a confirmed fact is precisely the error a good problem investigator avoids - the honest status is "unverified report, needs checking", which is why the answer is Cannot Say. Distinguishing reported symptoms from confirmed problems is the first step in your problem management skill.

**Question 8 (moderate) - Multiple choice:** What are the TWO actions the user actually requests?

A) Fix the regional filter and build a weekly model
B) Confirm whether a weekly breakdown is possible, and say what you would need from them
C) Meet with their director and rebuild the caseload model
D) Provide weekly figures immediately and investigate the 'Unknown' region

**Correct answer: B**

**Explanation:** The direct requests are in one sentence: "Could you let me know whether a weekly breakdown is possible, and if so, what you would need from me?" That is a request for confirmation of feasibility plus a statement of inputs required - option B. The 'Unknown' region is flagged as something "you might want to check", a suggestion rather than a request, and no fix is asked for (so A and D overstate). Nothing mentions meeting the director (C). When you handle simple queries and document data requirements, separating explicit requests from background remarks determines what goes on the work list - practise reading emails with the question "what exactly am I being asked to do?"

**Passage 3 - Extract from the team's Data Transformation Standards**

"Transformation code must be version-controlled, and every change must be linked to a work ticket. Changes to shared models require peer review; changes to a developer's private sandbox do not. Each transformation must include automated tests covering, at minimum, row counts and key uniqueness. Where a transformation applies business rules supplied by a subject matter expert, the rules must be documented in plain English alongside the code, and the documentation must state the expert's name and the date the rule was confirmed. Deviations from this standard are permitted only with the written agreement of the lead analytics engineer, and each deviation must be recorded in the deviations log."

**Question 9 (easy):** True, False, or Cannot Say: Changes to a developer's private sandbox require peer review.

**Correct answer: False**

**Explanation:** The passage draws the distinction explicitly: "Changes to shared models require peer review; changes to a developer's private sandbox do not." The statement asserts the opposite of the second clause, so it is False. The semicolon structure - rule, then exception or contrast - is common in standards documents; slow down whenever you meet one, because each half can be tested separately.

**Question 10 (moderate):** True, False, or Cannot Say: A transformation with automated tests for row counts and key uniqueness meets all the testing requirements of the standard.

**Correct answer: True**

**Explanation:** The standard requires tests "covering, at minimum, row counts and key uniqueness". A transformation with both has met the stated minimum, and the passage names no other testing requirement - so, judged strictly against this text, the statement is True. The phrase "at minimum" tells you more tests are welcome, but it does not make more tests mandatory. Be careful: if the statement had said "meets all requirements of the standard" (version control, tickets, documentation and so on), the answer would differ - read exactly which requirements the statement claims are met.

**Question 11 (hard):** True, False, or Cannot Say: A deviation from the standard agreed verbally by the lead analytics engineer and recorded in the deviations log is permitted.

**Correct answer: False**

**Explanation:** The passage permits deviations "only with the written agreement of the lead analytics engineer". A verbal agreement is not a written one, so this deviation fails the condition even though it was recorded in the log. Both conditions - written agreement AND log entry - must hold; the statement satisfies one and explicitly breaches the other ("agreed verbally"). Test writers love swapping a single qualifying word ("written" becomes "verbal"); underline qualifying words as you read. In real governance, the written record exists so that decisions survive staff changes - a lesson worth carrying into your own documentation habits.

**Question 12 (hard):** True, False, or Cannot Say: The standard was introduced because a transformation once failed in production.

**Correct answer: Cannot Say**

**Explanation:** The passage describes what the standard requires but says nothing at all about WHY it was introduced or any history behind it. The claimed origin story is plausible - many standards do follow incidents - but plausibility is not evidence, and the text is silent. This is the purest form of Cannot Say: a statement about motive or history when the passage covers only content. If you feel yourself reasoning "well, that's probably why...", stop - "probably" is the signature of an assumption, and assumptions score zero in verbal reasoning.

**Passage 4 - Internal guidance note: supporting users of the new reporting tool**

"From April, the department will replace its legacy reporting tool with a new self-service platform. All existing dashboards will be rebuilt on the new platform by the migration team; dashboard owners do not need to rebuild their own dashboards, but they must verify their rebuilt dashboards within ten working days of notification. During the transition, both tools will run in parallel, though only the new platform will receive data updates after 30 April. Training will be offered to all dashboard owners, and attendance is strongly recommended but not mandatory. Users experiencing issues should contact the data team's support inbox rather than the general IT helpdesk, as helpdesk staff have not been trained on the new platform."

**Question 13 (easy):** True, False, or Cannot Say: Dashboard owners must rebuild their own dashboards on the new platform.

**Correct answer: False**

**Explanation:** The passage states that dashboards "will be rebuilt on the new platform by the migration team; dashboard owners do not need to rebuild their own dashboards". The owners' obligation is different - verification within ten working days - not rebuilding. Statements that swap one obligation for another are a favourite trick: both "rebuild" and "verify" appear in the passage, and the wrong pairing sounds familiar enough to trap a skim-reader.

**Question 14 (moderate):** True, False, or Cannot Say: After 30 April, the legacy tool will show increasingly out-of-date figures.

**Correct answer: True**

**Explanation:** The passage says "only the new platform will receive data updates after 30 April". If the legacy tool receives no data updates while remaining available in parallel, its figures necessarily fall further behind as time passes - the statement is a direct logical consequence of the text, which counts as True. Verbal tests do allow conclusions the passage strictly entails, as opposed to conclusions it merely suggests; the difference is whether the conclusion could possibly be false while the passage is true. Here it could not: no updates means increasingly stale data.

**Question 15 (moderate):** True, False, or Cannot Say: Dashboard owners who do not attend training will lose access to the new platform.

**Correct answer: Cannot Say**

**Explanation:** The passage says attendance is "strongly recommended but not mandatory" - so there is no obligation to attend - but it says nothing about any consequence for non-attendance, and nothing connects training to access rights. The statement invents a penalty the text never mentions. Notice you cannot call it False either: the passage does not say owners will KEEP access regardless; it is simply silent. Silence means Cannot Say. When you contribute to user training materials in your role, this passage is also a model of the register such guidance uses - clear obligations ("must verify"), recommendations ("strongly recommended"), and routing instructions ("contact the support inbox").

**Question 16 (hard) - Multiple choice:** A user emails the general IT helpdesk about a problem with the new platform. According to the passage, why is this the wrong route?

A) The helpdesk is closed during the transition
B) Helpdesk staff have not been trained on the new platform
C) The helpdesk only supports the legacy tool
D) Users must attend training before requesting support

**Correct answer: B**

**Explanation:** The passage gives its reason explicitly: users should contact the data team's support inbox "rather than the general IT helpdesk, as helpdesk staff have not been trained on the new platform". Option B quotes the passage's own reasoning. Option A invents a closure; option C overstates (the passage never says what the helpdesk supports, only what its staff are not trained on); option D connects training to support in a way the passage never does. When a question asks "according to the passage, why...", the answer must be the reason the passage itself gives - not a reason that would merely make sense.

**Passage 5 - Note from a senior analytics engineer about modelling approaches**

"We generally follow the Kimball approach for our analytical models: we build dimensional star schemas designed around the business processes users want to analyse. Some central reference data is instead maintained in a more normalised form, closer to the Inmon style, and the dimensional models draw on it. Trainees sometimes ask which approach is 'correct'; the honest answer is that each suits different purposes, and our choice reflects the fact that most of our users are analysts who need fast, understandable query performance. Whichever approach applies, models must never be released without their accompanying documentation."

**Question 17 (moderate):** True, False, or Cannot Say: The team uses only the Kimball approach for all of its data.

**Correct answer: False**

**Explanation:** The word "generally" in the first sentence already softens the claim, and the second sentence contradicts "only" outright: "Some central reference data is instead maintained in a more normalised form, closer to the Inmon style". A statement containing "only" or "all" is False if the passage shows a single exception - and here the exception is explicit. This mirrors your data modelling skill at trainee level: showing awareness that different models suit different purposes, rather than treating one pattern as universally correct.

**Question 18 (hard):** True, False, or Cannot Say: The team chose its main modelling approach partly because of who its users are.

**Correct answer: True**

**Explanation:** The passage states: "our choice reflects the fact that most of our users are analysts who need fast, understandable query performance." A choice that "reflects" a fact about users is a choice made partly because of who the users are - the statement paraphrases the text without adding anything. Paraphrase statements are fair game for True; the skill is checking that every element of the paraphrase (choice, reason, users) is genuinely present in the passage. Compare this with Question 12, where the passage gave no reason at all: the difference between True and Cannot Say is whether the reason is on the page.

**Question 19 (moderate):** True, False, or Cannot Say (Passage 5): Trainees on the team have asked which modelling approach is correct.

**Correct answer: True**

**Explanation:** The passage states: "Trainees sometimes ask which approach is 'correct'". The statement is a direct restatement - "sometimes ask" confirms that trainees have asked. Do not be distracted by the passage's view that the question has no single answer; the statement is only about whether the question gets asked, not about its answer. Always check the exact scope of the statement you are judging: many wrong answers come from judging a bigger or smaller claim than the one actually written.

### Preparation tips

- **Practise the three-way judgement.** For every statement ask, in order: does the text state or entail this (True)? Does the text state or entail the opposite (False)? Otherwise it is Cannot Say. Saying the sequence aloud while practising builds the habit.
- **Read the statement first, then scan.** Under time pressure, read the question statement, pick out its keywords, and scan the passage for the governing sentence. Reading the whole passage in depth first is a luxury one-minute-per-question timing rarely allows.
- **Underline qualifying words.** Must, may, should, only, at least, until, written, all, some, never - these small words decide answers far more often than the technical vocabulary does.
- **Use your daily reading as practice.** Every policy, standard, or user email you read at work this week can become practice: ask yourself "what does this actually commit anyone to?"
- **Rehearse Cannot Say.** Beginners under-use it because it feels like giving up. It is not - it is the correct verdict whenever the passage is silent, and roughly a third of statements in many tests are engineered for it.
- **Stay calm about unfamiliar topics.** If a passage covers a domain you do not know, relax: every answer is in the text, and outside knowledge is banned anyway. Unfamiliarity is not a disadvantage.

### Common pitfalls

- **Importing outside knowledge.** You may know how metadata policy usually works across government; the test only cares what THIS passage says. Answer from the page, not from experience.
- **Confusing False with Cannot Say.** False requires the passage to contradict the statement. If the passage is merely silent, the answer is Cannot Say - no matter how unlikely the statement sounds.
- **Treating "likely" as "certain".** A passage saying an outcome is probable does not make that outcome True as a fact; nuance words ("may", "expected to", "recommended") set the exact strength of every claim.
- **Skimming past contrast structures.** Sentences with "however", "but", "rather than", or a semicolon often reverse direction mid-way. The second half is usually where the answer lives.
- **Losing time to full rereads.** If you cannot find the governing sentence in about twenty seconds, use the statement's rarest keyword to scan again - names, numbers, and dates make excellent anchors.
- **Assuming bundled statements are all-or-nothing.** A statement can be half-true and half-unstated; if ANY necessary part is unsupported, the whole statement cannot be judged True.


## Workplace job-specific situational judgement assessment

### About this assessment

A situational judgement assessment presents short, realistic workplace dilemmas and asks you to judge how effective different responses would be. Unlike the cognitive, numeric, and verbal tests, there is rarely a single objectively "right" answer - several responses may seem reasonable, but one usually fits the role, the organisation's values, and the practical situation best. Common formats ask you to pick the **most effective** and **least effective** actions from a set, or to rank or rate every option. Timing is usually generous or absent, because the test wants your natural judgement rather than your speed.

For a trainee analytics engineer in UK government, the "values" half of that equation is not a mystery: your judgements should reflect UK public sector and Civil Service values - honesty and integrity, putting user needs first, transparency about problems, collaboration across teams, and care for accessibility and inclusion. Layered on top are the sensible norms of being a trainee: you are expected to ask questions, work under supervision, escalate what is beyond you, and never bluff. An option that would be fine for a lead engineer (deciding alone, overriding a process) is often wrong for you - and an option that owns up to uncertainty, which might look weak elsewhere, is often exactly right.

The scenarios below are built from your actual duties: shadowing colleagues, handling simple user queries, documenting requirements, maintaining metadata under direction, executing test scripts, and supporting data quality. Read each one as if it were really happening to you this week.

### What it measures for your role

- **Handling user queries with honesty and care** maps to **communicating between the technical and non-technical** and to providing ongoing support to users.
- **Escalating and investigating sensibly** maps to **problem management**: recognising the level of a problem and contributing to remedies without overstepping.
- **Integrity in testing and documentation** maps to **testing** and **metadata management**: what you record must be what actually happened.
- **Learning behaviours** map to your role level itself: shadowing well, asking good questions, and turning feedback into improvement.
- **Speaking up constructively** maps to **data quality improvement** and **data innovation**: raising issues and ideas in ways that help the team act on them.

### Practice questions

For each scenario, decide your answer before reading the ratings. There are no trick questions - just realistic tensions between speed, honesty, helpfulness, and process.

**Question 1 (easy) - A user asks something beyond your knowledge**

A policy analyst stops you in the corridor: "You're on the data team, right? Can you tell me whether the ethnicity field in the workforce dataset is safe to publish in our report?" You genuinely do not know - you have been in the role six weeks, and questions about publishing personal or sensitive data have real legal implications.

Which response is MOST effective, and which is LEAST effective?

A) Say you are not sure, take their details, and promise to get an answer from your team - then actually follow up the same day
B) Give your best guess so they are not held up, and suggest they double-check with someone else if worried
C) Tell them data publication is not your job and walk on
D) Say you are new and cannot help, but suggest they email the team inbox

**Most effective: A. Least effective: B.**

**Explanation:** Option A is honest about your limits, keeps ownership of the user's need, and routes the question to people qualified to answer - the ideal trainee pattern. Option D is honest too, and routing to the team inbox is respectable, but it hands the effort back to the user, so it is weaker than A. Option C is unhelpful and damages the team's reputation with users. Option B is the least effective by a distance: guessing about whether sensitive personal data is "safe to publish" risks a data protection breach affecting real people, and appending "double-check if worried" does not neutralise a confident-sounding guess. In the public sector, honesty about uncertainty is a professional strength, never a weakness - and questions touching personal data always deserve a careful, qualified answer.

**Question 2 (easy) - Shadowing session you do not understand**

You are shadowing a senior analytics engineer who is walking through a complex data model at speed. Twenty minutes in, you realise you stopped understanding a while ago. She seems busy and focused.

Which response is MOST effective, and which is LEAST effective?

A) Keep nodding so as not to slow her down, and hope it makes sense later
B) Ask her to pause, say where you got lost, and ask if she can briefly recap that part
C) Quietly start catching up on emails since the session is wasted anyway
D) Let the session finish, then book time with her later in the week to go over the parts you missed

**Most effective: B. Least effective: C.**

**Explanation:** Shadowing exists so you learn; pretending to follow defeats its entire purpose. Option B is exactly what a good trainee does - naming where you got lost is specific, respectful of her time, and lets her adjust her pace, which also helps her practise her own skill of communicating technical concepts. Option D salvages the learning and is a decent second-best, though it costs more of her time later and loses the context of the moment. Option A wastes the session and quietly teaches you to hide confusion - a habit that gets more expensive every month. Option C is the least effective: it abandons the learning opportunity entirely and is visibly disengaged. Asking questions is not an interruption of your training; it IS your training.

**Question 3 (moderate) - You spot a data quality error in live data**

While updating a metadata catalogue entry, you notice that a published dataset's `region` column contains the value "Unknown" for around 15% of records - far higher than the 2% mentioned in its data quality statement. Dashboards used by operational teams draw on this dataset. Your mentor is away until tomorrow.

Rank these responses from most to least effective:

A) Note it down and wait to tell your mentor tomorrow
B) Correct the records yourself by inferring regions from postcodes, since you recently learned how
C) Report it the same day to another senior team member, with the numbers you observed and where you saw them
D) Post a general message in the team channel saying the dataset "has problems"

**Most effective order: C, D, A, B.**

**Explanation:** Option C is the model response: same-day escalation to someone qualified, with specific evidence (15% observed against 2% documented, and where). Problems in live data used for operational decisions are operational-level problems - your problem management skill says timeliness matters, and precision makes the report actionable. Option D at least raises the alarm promptly, but "has problems" without specifics generates worry and questions rather than action - vagueness is the enemy of investigation. Option A keeps good evidence but sits on a live issue for a day for no good reason; your mentor being away does not mean the team is. Option B is the least effective even though it is the most energetic: modifying live published data, unsupervised, as a trainee, without understanding the root cause, could corrupt the dataset further and hide the underlying fault - the remedy must follow the investigation, not precede it. Initiative is welcome; unauthorised fixes to production data are not.

**Question 4 (moderate) - Pressure to cut corners in testing**

A developer under deadline pressure says: "Can you just mark the test script as passed? It's basically the same transformation we tested last month, and the release window closes at four."

Which response is MOST effective, and which is LEAST effective?

A) Refuse quietly and record the tests as not run, without telling anyone about the request
B) Mark it passed this once, since the developer knows the code far better than you do
C) Say you cannot record a pass for tests that have not run, offer to execute the script right now, and flag the time pressure to your supervisor so the release decision is made openly
D) Tell the developer to ask a different tester who might be more flexible

**Most effective: C. Least effective: B.**

**Explanation:** Test records are statements of fact: recording a pass for tests that never ran is falsifying a record, whatever the deadline. Option C refuses that clearly, but pairs the refusal with practical help (running the script immediately) and with transparency (letting the supervisor weigh the release decision knowing the true testing status) - integrity plus collaboration, not integrity as a blocker. Option A protects the record but hides a process under strain; the team learns nothing and the same pressure will recur. Option D is worse: it dodges the issue and actively shops for someone willing to cut the corner. Option B is the least effective - "it's basically the same as last month" is an assumption, and the entire purpose of your testing skill is to replace assumptions with evidence. Note also the seniority dynamic: deferring to the developer's expertise about code is right; deferring about whether to falsify a test record is not.

**Question 5 (moderate) - Documenting requirements you only half understood**

You interviewed a subject matter expert about how housing repair priorities are assigned, so the logic can be built into a data model. Writing up your notes, you realise you are unsure whether "urgent" repairs include those flagged by tenants or only those flagged by inspectors - and the model design session is tomorrow.

Which response is MOST effective, and which is LEAST effective?

A) Write down the interpretation that seems more likely, since the expert is hard to get hold of
B) Email the expert the specific question today, mark that one point as "awaiting confirmation" in the document, and tell the model designer which part is unconfirmed
C) Leave the whole priorities section out of the document rather than risk an error
D) Ask a teammate what they think the expert probably meant

**Most effective: B. Least effective: A.**

**Explanation:** Your role is to translate organisational processes into data structures - and a mistranslation here becomes wrong logic in a model that people will trust. Option B does everything right: it chases the authoritative source with a precise question, keeps the document honest by labelling the uncertain point, and warns the person who will use the document tomorrow. Requirements documents may contain open questions; what they must never contain is guesses dressed as facts. Option D is weaker but not terrible - a teammate might know - yet their guess is still a guess, and it must not enter the document unlabelled. Option C throws away everything you DID confirm, which delays the design session more than one flagged uncertainty would. Option A is the least effective: a silent 50/50 guess about business logic, embedded in official documentation, is exactly how organisations end up with models that misclassify urgent repairs - with real consequences for tenants. "Refining requirements in response to feedback" starts with being honest about which requirements are confirmed.

**Question 6 (moderate) - You made a mistake in the metadata catalogue**

Last week you updated twenty metadata catalogue entries. Today you realise you entered the wrong update frequency on several of them - you wrote "daily" where the source documentation said "weekly". Some entries may already have been seen by platform users. Nobody has noticed.

Which response is MOST effective, and which is LEAST effective?

A) Quietly correct the entries and say nothing, since the fix removes the problem
B) Tell your mentor what happened, correct the entries under their direction, and check together whether the error affected any users or decisions
C) Wait to see whether anyone raises it, then correct entries individually if asked
D) Tell your mentor, but suggest the source documentation was ambiguous so the error was not really your fault

**Most effective: B. Least effective: C.**

**Explanation:** Option B combines the three things that matter: transparency (your team knows the catalogue was briefly wrong and can judge the impact), correction under direction (you maintain metadata "under the direction of others" - correcting twenty entries is squarely within that), and learning (perhaps your checking routine needs a step). Option A fixes the data but hides the incident - and if a user made a decision based on "daily" freshness, nobody will ever connect the dots; transparency in the public sector exists precisely so impacts can be assessed. Option D reports the error but poisons the report with deflection; if the documentation genuinely was ambiguous, say so as a fact to fix, not as a shield. Option C is the least effective: it leaves known-wrong information in front of users indefinitely and makes discovery someone else's job. Everyone makes mistakes in their first year; what distinguishes a promising trainee is the speed and honesty of the correction.

**Question 7 (hard) - Conflicting instructions from two seniors**

Your mentor asked you to spend today finishing user documentation for a new data model. Mid-morning, a different senior analytics engineer messages: "Drop that - I need you to run test scripts on my pipeline changes all day, we ship tomorrow." Your mentor is in workshops and not answering messages.

Which response is MOST effective, and which is LEAST effective?

A) Follow the most recent instruction - run the test scripts all day
B) Keep working on the documentation as originally instructed and let the second engineer find someone else
C) Explain to the second engineer that your mentor set your priorities, message your mentor briefly describing the conflict, and ask the second engineer to confirm the reprioritisation with your mentor or the team lead if it truly cannot wait
D) Split the day in half between the two tasks without telling either person

**Most effective: C. Least effective: D.**

**Explanation:** The trap in this scenario is deciding the priority conflict yourself - as a trainee you lack the context to weigh a shipping deadline against documentation commitments, and both options A and B silently do exactly that (A also lets the loudest voice win, B ignores a possibly genuine emergency). Option C is the model: it is transparent with both parties, routes the decision to people who own priorities, and does so quickly enough that a real deadline is not endangered. Note that C does not refuse the second engineer - it asks for the reprioritisation to be confirmed properly, which takes minutes. Option D is the least effective because it is invisible: both seniors believe their task is getting a full day, both get half, and both discover it too late to adjust - the worst outcome for trust and for the deadline. Collaboration in government teams runs on making conflicts visible, not on quietly absorbing them.

**Question 8 (hard) - A frustrated user criticises the team publicly**

In a large cross-team meeting you are attending to build your knowledge of the organisation, a service manager says: "The data team's dashboards are useless - the figures never match what my team sees on the ground, and nobody ever fixes it." You are the only data team member present. You do not know the history.

Which response is MOST effective, and which is LEAST effective?

A) Defend the team: explain that dashboards go through testing and review, so the figures are almost certainly right
B) Say nothing in the meeting and mention it to your mentor if you remember
C) Acknowledge the frustration, say you are new and do not know the background but will make sure the team hears it today, and ask the manager for one or two specific examples you can take back
D) Agree that the dashboards have a lot of problems, to defuse the tension

**Most effective: C. Least effective: A.**

**Explanation:** Option C does everything available to a trainee in that room: it treats the user's frustration as signal rather than attack, is honest about your own limits ("new, don't know the background"), converts a vague complaint into investigable specifics - the same expected-versus-actual evidence you would gather for any problem report - and commits to a same-day handover to the team. That is user-centred, transparent, and collaborative. Option D buys momentary peace by conceding faults you cannot verify, undermining your own team on no evidence. Option B wastes the chance entirely - "if you remember" is not a plan, and the manager learns the team ignores feedback. Option A is the least effective: with no knowledge of the history, you dismiss a user's lived experience in front of their peers; even if the figures ARE right (perhaps definitions differ between the dashboard and the ground count - a common cause), "the figures are almost certainly right" closes the conversation that would reveal it. Users who report mismatches are offering you data quality evidence; the right response is curiosity, never defensiveness.

**Question 9 (hard) - An innovation idea meets resistance**

During your training you learned about a documentation tool feature that could auto-generate parts of the team's data dictionary, saving hours of manual work each month. You mention it to a colleague, who shrugs: "We've always done it manually. It works fine." You still think the idea has merit.

Which response is MOST effective, and which is LEAST effective?

A) Drop the idea - they have more experience, and you have been here three months
B) Prepare a short, concrete note - what the feature does, what it might save, what could go wrong - try it on a small sample yourself in a sandbox, and offer to show your mentor a ten-minute demo
C) Raise it directly with the head of data, since your colleague will clearly block it
D) Start using the feature for your own documentation tasks without telling anyone, to prove it works

**Most effective: B. Least effective: C.**

**Explanation:** Your role profile explicitly asks you to "show an awareness of opportunities for innovation with new tools" - and option B is what that looks like in practice: evidence instead of enthusiasm, a low-risk sandbox trial, honest attention to drawbacks, and a proposal routed through your mentor, who can judge fit and timing. One colleague's shrug is not a veto; it is a first data point about adoption. Option A treats it as a veto and wastes a genuine improvement - experience deserves respect, but "we've always done it manually" is not an argument. Option D has the right experimental instinct but does it covertly on real work, which risks inconsistent documentation and burns trust if discovered - the sandbox in B gives you the same evidence without the risk. Option C is the least effective: leapfrogging your colleague AND your mentor to the head of data over a first lukewarm reaction damages the working relationships you will need for every future idea, and casts a shrug as sabotage. Good ideas win through evidence and patience, not escalation.

**Question 10 (moderate) - Accessibility in user training materials**

You are drafting a quick-start guide for dashboard users. A teammate suggests: "Just record your screen with voiceover, it's faster than writing." You recall that several intended users have declared accessibility needs, including a colleague who is deaf and another who uses a screen reader.

Which response is MOST effective, and which is LEAST effective?

A) Produce the video only - it covers most users, and the others can ask for help individually
B) Produce a written, screen-reader-friendly guide with described images, and if the video is made too, ensure it has accurate captions
C) Produce the video and ask the deaf colleague's manager to arrange separate support
D) Write the guide but include lots of unlabelled screenshots to save time

**Most effective: B. Least effective: A.**

**Explanation:** Government services and internal tools alike are expected to be accessible - it is a legal duty under the Equality Act and a core public sector value, not a nice-to-have. Option B builds accessibility in from the start: text that screen readers can parse, images that are described, captions if video exists. It serves every named user through the same materials, which is the inclusion standard: one guide everyone can use, not a main guide plus workarounds. Option D looks like the right format but fails screen reader users through unlabelled images - format alone is not accessibility. Option C at least acknowledges the need but converts a design flaw into an ongoing personal accommodation, singling colleagues out for something the materials should simply do. Option A is the least effective: it knowingly excludes named users and pushes the cost of exclusion onto them ("they can ask for help"). "Covers most users" is precisely the reasoning accessibility standards exist to prevent - and contributing to user training is in your role profile, so expect this dilemma for real.

**Question 11 (moderate) - Protecting your training time**

Your team is busy, and a well-meaning senior keeps handing you small urgent tasks. This week they have eaten both of your scheduled training sessions and a shadowing slot. You are falling behind the learning plan your mentor set, but you also want to be helpful and are a little flattered to be trusted.

Which response is MOST effective, and which is LEAST effective?

A) Keep absorbing the tasks - being useful now matters more than coursework, and the training will still exist later
B) Start declining all extra tasks, explaining that trainees should not be given operational work
C) Raise it with your mentor: show what was missed, explain the pattern, and ask them to help you agree with the senior which interruptions are genuinely urgent and how to protect your core training time
D) Complete the tasks but do the missed training in your evenings so nobody has to change anything

**Most effective: C. Least effective: A.**

**Explanation:** A trainee's development time is not a luxury; it is the point of the role - "attends training and develops skills on the job" is the first line of your level description. Option C treats the situation as a workload-design problem to be solved with the people who own your plan: it is transparent, keeps you helpful for genuine emergencies, and produces an agreed rule instead of weekly friction. Option D hides the problem and sets an unsustainable precedent - unpaid evening catch-up masks the cost of the interruptions, so they will continue, and burnout helps nobody. Option B swings to the opposite extreme: some operational exposure is valuable training (handling simple queries IS in your role profile), and a blanket refusal reads as unhelpful and rigid. Option A is the least effective over any horizon beyond this week: skipped foundations compound, and in six months the team gains a helpful trainee who never became a capable engineer. Speaking up about your own development needs is itself a professional skill - practise it early.

### Preparation tips

- **Learn the values, not scripted answers.** UK public sector judgement questions reward honesty, transparency about problems, user focus, collaboration, and inclusion. If you understand WHY those values lead to effective actions, unfamiliar scenarios will not throw you.
- **Think "trainee-appropriate".** Before rating an option, ask: is this action right for someone working under supervision? Escalating, asking, and flagging are usually strong moves at your level; solo heroics on live systems usually are not.
- **Watch for the hidden dimension.** Many scenarios test two things at once - integrity AND helpfulness, honesty AND tact. The best option usually serves both; options that maximise one while abandoning the other rate lower.
- **Rate options independently first.** Judge each option on its own merits before comparing. It stops a mediocre option looking good merely because its neighbours are terrible.
- **Use your real week as rehearsal.** When something awkward happens at work, notice what you did and what the ideal response would have been. Reflection turns ordinary weeks into test preparation.
- **Do not overthink.** These assessments are usually untimed precisely because they want your genuine judgement. If you have absorbed the values, your considered first instinct is usually close to the keyed answer.

### Common pitfalls

- **Choosing the idealistic over the practical.** "Convene all stakeholders to co-design a solution" sounds noble but may be absurd for a stale dashboard at 09:15. Effective beats impressive.
- **Selecting passive options.** Waiting, hoping, "seeing if anyone notices", or handing the problem back to the user are almost always rated poorly. Effective options move the situation forward, even if only by escalating well.
- **Confusing escalation with weakness.** At trainee level, timely escalation with specific evidence is one of the strongest moves available. Options where you silently shoulder problems beyond your remit are traps.
- **Ignoring the stated context.** Details like "your mentor is away", "users make decisions at 10:00", or "you do not know the history" are there to change the answer. Read scenarios as carefully as verbal passages.
- **Rating what you WOULD do, dishonestly.** Do not try to game the test with answers you think it wants while believing something else. The values being tested are the actual values of the workplace; aligning with them genuinely is the preparation.
- **Forgetting the least-effective half.** Most/least formats score both choices. After finding the best option, spend equal care finding the truly worst - usually the one that is dishonest, harms users, or hides information.


## Conclusion

Well done for working through this guide - that was a substantial piece of preparation, and completing it says something good about how you approach your development.

You have now explored all four assessment types you are likely to meet as a trainee analytics engineer. You practised cognitive skills - spotting patterns in refresh logs and quality scores, deducing causes from evidence, checking metadata entries and transformed values, and prioritising competing demands. You worked through numeric reasoning with the real currency of your profession: pass rates, missing-value percentages, row-count reconciliations, weighted quality scores, and growth projections, with every calculation shown step by step. You sharpened your verbal reasoning against the standards, policies, and user emails your role runs on, learning to judge True, False, and - hardest of all - Cannot Say strictly from the text. And you tested your judgement against realistic dilemmas: owning up to mistakes, resisting pressure to cut corners, escalating well, protecting your training time, and building accessibility in from the start.

Notice the common thread: none of this was abstract. Every skill these assessments measure is a skill you will use this week - reading a requirement precisely, checking a figure before you send it, asking the question you are tempted to skip, being honest about what you do not yet know. That means every day at work is also practice, and every bit of practice makes you better at both the tests and the job.

What next? Revisit the questions you found hardest in a week or two - improvement will be obvious and motivating. Ask your mentor to point you at real artefacts: a test script, a catalogue entry, a data model diagram. Keep a small notebook of situations where your judgement was tested and what you learned. And be patient with yourself: every senior analytics engineer you shadow was once exactly where you are now.

You have chosen a career where curiosity, care, and honesty compound over time. Keep practising, keep asking questions, and good luck with your assessment - you are better prepared than you think.
