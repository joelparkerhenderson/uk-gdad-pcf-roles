# Associate Test Engineer - Psychometric Assessment Resources

## Introduction

Welcome! This guide has been written especially for you as an associate test engineer working within the UK Government Digital and Data profession. You are at the start of an exciting career in quality assurance testing, and this document is here to help you practise, build confidence, and feel prepared for any psychometric assessment you might face — whether that is part of an internal development scheme, an application for your next role, or simply a way to check your own progress.

Let's start with the basics. Psychometric assessments are structured, standardised exercises that measure the thinking skills and behaviours that predict success in a job. They are not trick tests, and they are not there to catch you out. For an associate test engineer, a good assessment will feel familiar, because it uses the kinds of materials you already work with every day: test scripts, defect reports, user stories, simple test plans, and messages between you and your teammates. The questions ask you to do the kinds of thinking you already do — spot a mistake in a script, follow a defect management process step by step, read a user story carefully, and decide what to do when something unexpected happens during testing.

Why do these assessments matter for your role in particular? As an associate test engineer, you work closely with test engineers and quality assurance test analysts to learn the activities and techniques required to establish the basis of testing. You develop test scripts under supervision, you raise awareness of defects and help manage them, and you build your domain and business knowledge day by day. Every one of those duties depends on careful attention, clear reading, sensible judgement, and simple accurate arithmetic — exactly the skills that psychometric assessments measure. Practising them here will help you in the assessment room and at your desk.

This document is organised into four main assessment sections:

1. A workplace job-specific cognitive assessment — pattern spotting, logical thinking, error checking, prioritisation, and problem solving using real testing artefacts.
2. A workplace job-specific numeric reasoning assessment — percentages, averages, ratios, and reading tables, using the sorts of numbers a tester genuinely handles, such as pass rates and defect counts.
3. A workplace job-specific verbal reasoning assessment — reading role-relevant passages carefully and answering true, false, or cannot-say questions.
4. A workplace job-specific situational judgement assessment — realistic workplace dilemmas for someone at your level, with guidance on the most effective and least effective responses.

Each section follows the same friendly pattern: an overview of what the assessment measures, a mapping of the assessment to the specific skills in your role, a set of practice questions with full worked explanations, practical preparation tips, and common pitfalls to avoid.

Here is how to get the most from this guide. First, read each "About this assessment" section so the format holds no surprises. Second, try every practice question honestly — write down your answer before you peek at the explanation. Third, treat each explanation as a mini-lesson: even when you get the question right, the walkthrough will strengthen your technique. Finally, be patient with yourself. You are at an associate level, and nobody expects you to know everything. What matters is steady, honest practice.

Take a deep breath, grab a notepad, and let's begin. You can do this.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive assessment measures the exact thinking skills your role demands, using practical workplace scenarios rather than abstract puzzles. Instead of asking you to rotate shapes or complete number sequences with no context, it presents you with the everyday materials of your job — test scripts, defect logs, user stories, checklists, and simple plans — and asks you to reason about them quickly and accurately.

The typical format is an online, timed test lasting 15 to 30 minutes, with somewhere between 15 and 30 questions. The questions cover pattern recognition, logical deduction, error checking, prioritisation, and applied problem solving. Scoring is objective: your answers are compared against a norm group of people at a similar career stage, so you are not being measured against senior engineers with twenty years of experience. Many modern platforms adapt the difficulty as you go, giving you slightly harder questions when you answer correctly and slightly easier ones when you slip. That is normal, so do not panic if the questions seem to get tougher — it usually means you are doing well. Employers typically receive a breakdown of speed and accuracy rather than a single score, so working carefully matters just as much as working quickly. You will almost always be offered a few ungraded practice questions before the real test starts, so you can get comfortable with the screen layout without any pressure.

Why do employers use this kind of assessment for an associate test engineer? Because your core professional value is careful, structured attention. Testing is the discipline of noticing: noticing when a script step is out of order, noticing when an actual result differs from an expected result, noticing when a defect report is missing a key detail. A well-designed cognitive assessment simulates those demands in miniature, and practising it genuinely makes you better at the day job.

### How this assessment maps to your role

The assessment dimensions map directly onto the named skills in your role summary:

- **Pattern recognition** maps to your **Designing and executing tests** skill. When you follow guidance to design, build and maintain simple tests that align to user needs and requirements, you must recognise recurring structures — consistent naming of test cases, repeated step sequences, and matching pairs of expected and actual results.
- **Logical deduction** maps to your **Test analysis** skill. Analysing information such as user stories, prototypes, processes and designs, even with support, requires you to reason from the given requirements to what must follow: if the story says a field is mandatory, then a test that leaves it blank must produce a validation message.
- **Error checking** maps to your **Managing, reporting and resolving defects** skill. Following a defect management process to report, communicate and maintain defects with appropriate information means spotting when something is wrong, incomplete, or inconsistent — the heart of error checking.
- **Prioritisation** maps to your **Test and quality planning** skill. Following quality testing approaches, plans and strategies with support means understanding which activities matter most right now, and raising your hand when two tasks compete for your time.
- **Applied problem solving** maps to your **Test engineering** skill and your duty to support the maintenance of automated tests and tools. When an automated check fails or an environment misbehaves, you work through the possibilities step by step to find the cause, with help from your team.

### Practice questions

**Question 1 (easy) — Pattern recognition in test case names**

Your team names manual test cases using the pattern `TC-<area>-<three-digit number>`, for example `TC-LOGIN-001`. While tidying the test case library under supervision, you see these five entries:

1. TC-LOGIN-001
2. TC-LOGIN-002
3. TC-SEARCH-01
4. TC-SEARCH-002
5. TC-PAYMENT-003

Which entry breaks the naming pattern?

- A) Entry 2
- B) Entry 3
- C) Entry 4
- D) Entry 5

**Correct answer: B**

**Explanation:** The pattern requires a three-digit number at the end. Entry 3, `TC-SEARCH-01`, has only two digits, so it breaks the rule. Entries 1, 2, 4 and 5 all follow the pattern exactly: the prefix `TC`, an area name in capitals, and a three-digit number. A helpful technique is to check each entry against each part of the rule in turn — prefix, area, number format — rather than glancing at the whole list and hoping the odd one out jumps at you. Naming conventions may feel small, but they are the foundation of a tidy test library: when hundreds of test cases exist, consistent names are what let your team find, filter, and report on them. Spotting this kind of inconsistency is exactly the attentive habit your role builds as you develop test scripts under supervision.

**Question 2 (easy) — Logical deduction from a user story**

A user story you are analysing with support says: "As a citizen, I want to reset my password by email, so that I can regain access to my account. Acceptance criterion: the reset link must expire after 24 hours." Your supervisor asks: "If a citizen clicks a reset link 30 hours after it was sent, what must happen?" Which one of the following must be true according to the story?

- A) The citizen's account is locked.
- B) The reset link no longer works.
- C) A new reset link is automatically sent.
- D) The citizen must call the helpdesk.

**Correct answer: B**

**Explanation:** The acceptance criterion says the link expires after 24 hours. Thirty hours is more than 24, so the link must have expired — meaning it no longer works. That is the only conclusion the story guarantees. Options A, C and D describe behaviours that some systems have, but nothing in this story mentions account locking, automatic resending, or helpdesk calls, so you cannot conclude any of them. Assessments reward this discipline: deduce only what the given information guarantees, and resist adding what you imagine the system might do. This is the same discipline you use in test analysis — a test should check what the requirement actually says, not what you assume it probably means. When you are unsure, the right move at your level is to ask the question, not to guess.

**Question 3 (easy) — Error checking a defect report**

Your team's defect management process says every defect report must contain: (i) a summary title, (ii) steps to reproduce, (iii) expected result, (iv) actual result, and (v) severity. You have drafted this report:

> **Title:** Search button unresponsive on results page
> **Steps:** 1. Log in. 2. Search for "passport". 3. On the results page, click Search again.
> **Expected result:** A new search is performed.
> **Severity:** Medium

What is missing from your report?

- A) The summary title
- B) The steps to reproduce
- C) The actual result
- D) The severity

**Correct answer: C**

**Explanation:** Check the report against the checklist item by item. The title is present, the steps are present, the expected result is present, and the severity is present — but the actual result (what really happened when you clicked Search) is missing. A developer reading this report would know what should happen but not what did happen: did the button do nothing, show an error, or crash the page? Working methodically through a checklist is the most reliable way to catch omissions, and it is far safer than re-reading the report as a whole and trusting your general impression. Following a defect management process to report defects with appropriate information is a named part of your role, and complete reports save your whole team time — a defect that must be sent back for more detail is a defect fixed later.

**Question 4 (easy) — Prioritisation of daily tasks**

It is 10:00 on a Tuesday. You have four tasks:

1. Retest a defect the developer fixed this morning; the release decision meeting is at 14:00 today and needs the result.
2. Continue writing a test script for a feature due to be tested next week.
3. Update your timesheet, due Friday.
4. Read a tutorial your mentor recommended, with no deadline.

Which task should you do first?

- A) Task 1
- B) Task 2
- C) Task 3
- D) Task 4

**Correct answer: A**

**Explanation:** Task 1 is both urgent (the meeting is at 14:00 today) and important (a release decision depends on the retest result). Retesting and escalating defects when needed is one of your named skills, and this is a clear example of it in action. Task 2 matters but is not due until next week; task 3 has a Friday deadline; task 4 has no deadline at all. The simple technique is to weigh urgency and importance together: something due today that other people are waiting on nearly always comes first. If you ever find that two tasks are both urgent and important, that is not a puzzle you must solve alone at your level — it is a signal to tell your supervisor promptly so the team can decide together. Assessments and real workplaces both reward that combination of sensible ordering and honest communication.

**Question 5 (moderate) — Pattern recognition in test results**

You run the same suite of five automated checks every morning and record pass (P) or fail (F). The results for the past four days are:

| Check | Mon | Tue | Wed | Thu |
|---|---|---|---|---|
| Login | P | P | P | P |
| Search | P | F | P | F |
| Upload | P | P | P | P |
| Payment | P | P | F | F |
| Logout | P | P | P | P |

Which statement best describes the pattern?

- A) Search fails every day; Payment fails on alternate days.
- B) Search fails on alternate days; Payment has failed on the two most recent days.
- C) All checks are becoming less reliable.
- D) Payment fails whenever Search fails.

**Correct answer: B**

**Explanation:** Read each row carefully. Search shows P, F, P, F — a fail every other day, which is an alternating pattern worth reporting because intermittent failures often point to timing or environment issues. Payment shows P, P, F, F — it passed early in the week and has failed on Wednesday and Thursday, the two most recent days, which suggests something changed midweek. Option A wrongly says Search fails every day. Option C is too sweeping: Login, Upload and Logout passed every day. Option D is contradicted by Wednesday, when Payment failed but Search passed. Reading tables row by row, and describing exactly what you see rather than a general impression, is a core habit for supporting the maintenance of automated tests — and when you spot patterns like these, raising awareness of them is precisely the defect-awareness duty your role describes.

**Question 6 (moderate) — Logical deduction about test coverage**

Your mentor tells you three facts about a small application: (i) every screen with a form has at least one validation test; (ii) the Contact screen has a form; (iii) the Home screen has no validation tests. Which conclusion must be true?

- A) The Home screen has a form.
- B) The Contact screen has at least one validation test.
- C) The Contact screen has exactly one validation test.
- D) The Home screen is untested.

**Correct answer: B**

**Explanation:** Chain the facts together. Fact (ii) says the Contact screen has a form, and fact (i) says every screen with a form has at least one validation test — so the Contact screen must have at least one validation test. That is option B. Option C overreaches: "at least one" is not "exactly one". Option A reverses the logic: fact (iii) tells us the Home screen has no validation tests, and combined with fact (i) that actually tells us the Home screen has no form (if it had one, it would need a validation test). Option D confuses "no validation tests" with "no tests at all" — the Home screen might have other kinds of tests. This step-by-step chaining, and the care not to say more than the facts allow, is exactly the reasoning you practise when you analyse user stories and designs with support.

**Question 7 (moderate) — Error checking expected versus actual results**

You are executing a simple test script with support. Step 4 says: "Enter date of birth 29/02/2023 and click Save. Expected result: the message 'Please enter a valid date' is shown." When you perform the step, the system shows the message "Please enter a valid date of birth". What should you record?

- A) Pass — the message is close enough.
- B) Fail — and raise a severity-critical defect immediately.
- C) The actual result exactly as seen, and query the small difference with your test engineer.
- D) Skip the step and move on.

**Correct answer: C**

**Explanation:** The actual message differs from the expected message by two words. That difference might be a genuine (minor) defect, or the script's expected result might simply be out of date — at your level, you are not expected to decide alone which it is. The professional habit is to record exactly what you observed, word for word, and then query the discrepancy with the test engineer supervising you. Option A is dangerous: "close enough" judgements made silently are how small inconsistencies slip into live services, and 29/02/2023 is a genuinely invalid date (2023 was not a leap year), so this validation matters. Option B overreacts: a wording difference is unlikely to be critical, and severity should follow your team's definitions, not your alarm level. Option D is never acceptable — skipped steps break the record of what was tested. Precise observation plus honest escalation is the core of executing simple tests with support.

**Question 8 (moderate) — Prioritisation using severity and process**

Your defect process defines severity levels: Critical (service unusable), High (major function broken, no workaround), Medium (function broken, workaround exists), Low (cosmetic). During one testing session you find four issues:

1. The service crashes on every login attempt.
2. A page heading reads "Aplication" instead of "Application".
3. The document upload fails, but users can email documents instead.
4. The print function is broken, and there is no other way to print.

Using the definitions, which issue should be reported with the highest severity?

- A) Issue 1
- B) Issue 2
- C) Issue 3
- D) Issue 4

**Correct answer: A**

**Explanation:** Match each issue to the definitions rather than to your gut feeling. Issue 1 makes the service unusable for everyone — nobody can get past login — so it is Critical, the highest level. Issue 4 is a major function broken with no workaround, which fits High. Issue 3 is a broken function with a workaround (email), which fits Medium. Issue 2 is a spelling mistake: cosmetic, therefore Low — worth reporting, but lowest priority. The discipline being tested is applying an agreed scale consistently instead of ranking by what annoys you personally. Explaining how to report and track defects, including using severity correctly, is a named part of your role, and consistent severity ratings are what allow your team to trust the defect list when deciding what to fix first.

**Question 9 (moderate) — Applied problem solving with an automated check**

An automated test that has passed for weeks fails this morning with the message "Element 'Continue button' not found". You have been asked to investigate with support. Which is the most sensible first step?

- A) Delete the test, since it is clearly unreliable.
- B) Rerun the test once, then open the application and look at the page to see whether the Continue button is still there and unchanged.
- C) Report a critical defect against the application.
- D) Rewrite the test in a different tool.

**Correct answer: B**

**Explanation:** "Element not found" has two common causes: the application changed (perhaps the button was renamed or moved, which the test correctly caught) or the test environment hiccuped (a slow page load, a temporary glitch). The cheapest way to distinguish them is to rerun once — which rules out a one-off glitch — and then look at the real page yourself. If the button has changed, the test needs updating and there may be a genuine change to discuss; if the button is unchanged and the rerun passes, you may have an intermittent timing issue to mention to your team. Option A destroys information: a failing test is telling you something. Option C reports a defect before establishing there is one. Option D is a large effort with no diagnosis. Supporting the maintenance of automated tests means exactly this kind of calm, step-by-step investigation — and explaining the value of automation includes understanding why a failing check is a prompt to look, not to panic.

**Question 10 (challenging) — Multi-step logical deduction about environments**

Your team has three environments: Dev, Test, and Staging. The rules are: (i) a build must pass all automated checks in Dev before it can be deployed to Test; (ii) a build must be manually tested in Test before it can be deployed to Staging; (iii) build B7 is currently deployed in Staging; (iv) build B8 has passed all automated checks in Dev but has not yet been manually tested. Which statement must be true?

- A) B8 is deployed in Staging.
- B) B7 passed all automated checks in Dev and was manually tested in Test.
- C) B8 failed its automated checks.
- D) B7 and B8 are the same build.

**Correct answer: B**

**Explanation:** Work backwards from what you know. B7 is in Staging (fact iii). Rule (ii) says nothing reaches Staging without manual testing in Test, so B7 was manually tested in Test. Rule (i) says nothing reaches Test without passing automated checks in Dev, so B7 also passed those checks. Chaining the two rules gives option B. Option A is impossible: B8 has not been manually tested (fact iv), so rule (ii) blocks it from Staging. Option C contradicts fact (iv), which says B8 passed its checks. Option D has no supporting evidence. The skill here is chaining conditional rules in sequence — the same reasoning you use when you explain why testing processes and environments are important: each environment gate exists so that only properly checked builds move forward, and understanding the chain lets you say with confidence what any deployed build must already have been through.

**Question 11 (challenging) — Error checking a test data table**

You are preparing test data for a form that accepts applicants aged 18 to 65 inclusive. Your supervisor asks you to prepare boundary test data: the youngest invalid age, the youngest valid age, the oldest valid age, and the oldest invalid age. A colleague drafts this table:

| Purpose | Age |
|---|---|
| Youngest invalid | 17 |
| Youngest valid | 18 |
| Oldest valid | 64 |
| Oldest invalid | 67 |

How many rows contain an error?

- A) 0
- B) 1
- C) 2
- D) 3

**Correct answer: C**

**Explanation:** "18 to 65 inclusive" means 18 and 65 are both valid ages. Check each row against that rule, one at a time. Row 1, youngest invalid: 17 is correct — it is the age immediately below the lower boundary. Row 2, youngest valid: 18 is correct — it is the lower boundary itself. Row 3, oldest valid: the table says 64, but 65 is valid too, so the oldest valid age is 65 — this row is wrong. Row 4, oldest invalid: boundary testing uses the value immediately outside the range, which is 66; the table says 67, so this row is wrong as well (67 is invalid, but it is not the boundary value, so it would let a defect at 66 slip through). Two rows are in error, so the answer is 2. Notice what the wrong table would have done in practice: the age 65 — the exact value where a lazy `< 65` check instead of a correct `<= 65` check would fail — is tested nowhere. Boundary values are where defects hide, which is why they deserve slow, deliberate checking. Analysing test data like this, with support, is exactly the kind of supported analysis your role describes, and querying a suspicious table with its author is always better than silently using it.

**Question 12 (challenging) — Applied problem solving under a checklist**

Your regression checklist has 12 items and must be completed before Friday's release. Each item takes about 30 minutes. It is Thursday 13:00, you finish at 17:00 today and work 09:00 to 17:00 on Friday, and the release cut-off is Friday 12:00. You also have a one-hour team meeting on Friday at 09:30. Assuming no breaks or interruptions, can you finish the checklist alone before the cut-off, and what should you do?

- A) Yes — there is exactly enough time, so say nothing and start work.
- B) No — you will be one hour short, so tell your test engineer now so the team can help or re-plan.
- C) No — so skip the four least interesting checklist items.
- D) Yes — if you skip Friday's team meeting without telling anyone.

**Correct answer: B**

**Explanation:** Work the numbers step by step. Twelve items at 30 minutes each is 12 × 0.5 = 6 hours of work. Time available today: 13:00 to 17:00 is 4 hours. Time available Friday before the cut-off: 09:00 to 12:00 is 3 hours, minus the one-hour meeting (09:30–10:30) leaves 2 hours. Total available: 4 + 2 = 6 hours — which looks like exactly enough, but re-read the calculation: 4 + 2 = 6 and the work is 6 hours, so on paper it just fits with zero slack. A plan with zero slack fails the moment anything overruns, and at your level the professional move is to raise the risk now rather than gamble. Option B is best because it surfaces the problem while there is still time to get help — and honest early escalation is a named behaviour in your role (retest and escalate when needed). Option A hides a fragile plan. Option C silently cuts agreed coverage, which is never an associate's call to make alone. Option D solves the numbers by damaging team trust. When an assessment offers a "tell someone early" option in a tight-timing scenario, it is very often the strongest answer — just as it is in real delivery.

### Preparation tips

- **Practise with your own artefacts.** Spend ten minutes a day reading test scripts, defect reports, and user stories from your project (respecting any confidentiality rules). Ask yourself: is anything missing, inconsistent, or out of order? This is free cognitive training using exactly the materials assessments imitate.
- **Learn your team's checklists by heart.** The defect report fields, the severity definitions, the environment rules — knowing these cold makes checklist-style questions fast and calm.
- **Slow down on tables.** When a question shows a table, read it row by row and column by column before looking at the options. Most table mistakes come from skimming.
- **Say the logic out loud (or write it down).** For deduction questions, write the chain: "Fact 1 plus Rule 2 means X." If you cannot write the chain, you are guessing — go back to the facts.
- **Time yourself gently.** Try a few questions with a timer set to about 90 seconds each. The aim is familiarity with time pressure, not speed at any cost. Accuracy first, then pace.
- **Sleep and settle.** The night before a real assessment, prepare your space, test your login, and rest. A calm, rested associate outperforms an anxious one every time.

### Common pitfalls to avoid

- **Adding what the question never said.** The most common error at every level is concluding something the facts do not guarantee — assuming a system behaviour, a deadline, or an intention that is not in the text. Deduce only from what is given.
- **Marking "close enough" as a pass.** In error-checking questions, tiny differences (a word, a digit, a boundary value) are usually the whole point. Compare character by character when results should match.
- **Ranking by annoyance instead of by definition.** Severity and priority questions give you definitions — use them. Your personal irritation at a spelling mistake is not a severity level.
- **Rushing the first questions.** Adaptive tests often start easy. Careless slips early on cost more than slow care does — settle in, then build pace.
- **Freezing on hard questions.** If a question feels too hard, make your best reasoned choice and move on. One question is worth the same as any other; ten seconds of dithering across twenty questions is a whole question lost.
- **Forgetting that escalation is a valid answer.** At associate level, "record it precisely and ask" or "raise it early" is often the strongest option, in assessments as in real work. Choosing it is a sign of professionalism, not weakness.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment measures your ability to work accurately with the numbers your job genuinely produces. For an associate test engineer, that means test pass rates, defect counts, execution progress, simple time estimates, and small tables of results — not advanced mathematics. If you can add, subtract, multiply, divide, and handle percentages, fractions, ratios, and averages carefully, you have all the mathematical machinery you need. What the assessment really measures is whether you apply that machinery accurately, under gentle time pressure, to realistic workplace data.

The typical format is an online, timed test lasting 20 to 30 minutes with 15 to 20 questions. Each question presents a small data set — a table of test results, a chart of defect counts, a short statement of figures — followed by a multiple-choice question. Calculators are usually permitted (check the instructions for your specific test), and rough paper is your friend. Scoring compares your accuracy and speed against a norm group at a similar career stage. Some tests are adaptive, adjusting difficulty as you go.

Why do employers use numeric reasoning for your role? Because testing runs on numbers. Every day your team asks: how many test cases have we executed, how many passed, how many defects are open, are we on track to finish? When you raise awareness of defects or report progress, the numbers must be right — a pass rate reported as 90% when it is really 79% could send a broken feature to release. Estimation of test effort, which sits at the heart of the test engineer role you are growing into, is numeric reasoning in its everyday clothes. Practising here builds both assessment performance and daily accuracy.

### How this assessment maps to your role

- **Percentages and pass rates** map to your **Managing, reporting and resolving defects** skill: reporting defects and retest results with appropriate information often means expressing counts as percentages — pass rates, fix rates, and reopen rates.
- **Reading tables and charts** maps to your **Test analysis** skill: analysing information with support includes reading result tables, progress charts, and simple dashboards accurately before drawing any conclusion.
- **Averages and simple estimates** map to your **Test and quality planning** skill: following plans with support, and one day estimating test effort yourself, requires you to work with average execution times and totals.
- **Ratios and proportions** map to your **Designing and executing tests** skill: understanding how test cases are distributed across features, or how defects are spread across severity levels, is proportional reasoning.
- **Measuring effectiveness** maps directly to your duty to **explain how to measure the effectiveness of quality testing approaches** and why it is important: metrics such as defect detection percentage are exactly how teams measure whether testing is working.

### Practice questions

**Question 1 (easy) — Pass rate percentage**

You executed 40 test cases today. 34 passed and 6 failed. What is the pass rate?

- A) 75%
- B) 80%
- C) 85%
- D) 90%

**Correct answer: C**

**Explanation:** Pass rate = passed ÷ total × 100. Step by step: 34 ÷ 40 = 0.85. Then 0.85 × 100 = 85%. So the pass rate is 85%. A quick sense-check: 6 failures out of 40 is 6 ÷ 40 = 0.15 = 15% failed, and 100% − 15% = 85% passed — the two routes agree, which is a good habit whenever time allows. Reporting an accurate pass rate is a daily task when you communicate testing progress, and the sense-check habit (calculate the complement and confirm the two figures sum to 100%) catches most slips before they reach your team's stand-up.

**Question 2 (easy) — Counting from a defect table**

Your team's defect log shows:

| Severity | Open | Fixed |
|---|---|---|
| Critical | 1 | 2 |
| High | 3 | 5 |
| Medium | 6 | 9 |
| Low | 4 | 10 |

How many defects are open in total?

- A) 12
- B) 14
- C) 26
- D) 40

**Correct answer: B**

**Explanation:** Add down the Open column only: 1 + 3 + 6 + 4. Work in steps: 1 + 3 = 4; 4 + 6 = 10; 10 + 4 = 14. The answer is 14. Option C (26) is the total of the Fixed column, and option D (40) is the total of both columns — both are classic wrong-column traps. Before adding anything, put your finger (or cursor) on the column heading the question actually asks about. Reading tables precisely is part of analysing information with support, and the wrong-column error is the single most common table mistake in numeric tests — and in real status reports.

**Question 3 (easy) — Simple time estimate**

Each manual test case in your suite takes about 15 minutes to execute. You have 16 test cases left. About how many hours of execution time remain?

- A) 2 hours
- B) 3 hours
- C) 4 hours
- D) 6 hours

**Correct answer: C**

**Explanation:** Total minutes = 16 × 15. Step by step: 16 × 15 = 16 × 10 + 16 × 5 = 160 + 80 = 240 minutes. Convert to hours: 240 ÷ 60 = 4 hours. The answer is 4 hours. Estimation of test effort is the everyday arithmetic behind test planning — the role you are training in undertakes exactly this kind of estimating as part of a risk-based approach. Notice the multiplication shortcut: breaking 15 into 10 + 5 makes the mental arithmetic reliable without a calculator, and reliable beats fast.

**Question 4 (easy) — Percentage of testing complete**

Your test plan contains 120 test cases. So far, 90 have been executed. What percentage of the plan is complete?

- A) 60%
- B) 70%
- C) 75%
- D) 80%

**Correct answer: C**

**Explanation:** Completion = executed ÷ planned × 100. Step by step: 90 ÷ 120 = 0.75. Then 0.75 × 100 = 75%. You can also simplify the fraction first: 90/120 = 9/12 = 3/4 = 75%. Both routes give 75%. When you report progress at a stand-up, this is the exact calculation behind "we are three-quarters of the way through the plan". Beware the temptation to guess from the numbers' appearance: 90 out of 120 "looks like" 80% to many people because 90 is a big number, but the denominator matters — always divide, never eyeball.

**Question 5 (moderate) — Average execution time**

You timed five test cases at 12, 18, 9, 21, and 15 minutes. What is the average (mean) execution time?

- A) 12 minutes
- B) 14 minutes
- C) 15 minutes
- D) 16 minutes

**Correct answer: C**

**Explanation:** Mean = total ÷ count. Add step by step: 12 + 18 = 30; 30 + 9 = 39; 39 + 21 = 60; 60 + 15 = 75 minutes total. Divide by the count: 75 ÷ 5 = 15 minutes. The answer is 15. A sense-check: the values range from 9 to 21, so the mean must sit somewhere between them — 15 is comfortably in range, while an answer like 25 would be impossible. Averages like this feed directly into effort estimates: if your suite has 40 similar cases, an average of 15 minutes suggests roughly 40 × 15 = 600 minutes = 10 hours of execution — which is how test engineers turn small measurements into plans.

**Question 6 (moderate) — Defect ratio**

Your project's open defects are split between two features: Search has 18 open defects and Payments has 12. What is the ratio of Search defects to Payments defects, in simplest form?

- A) 18:12
- B) 6:4
- C) 3:2
- D) 2:3

**Correct answer: C**

**Explanation:** Start with 18:12. Simplify by dividing both sides by their highest common factor. Both are divisible by 6: 18 ÷ 6 = 3 and 12 ÷ 6 = 2, giving 3:2. Options A and B are the same ratio but not fully simplified — a ratio question asking for "simplest form" wants the smallest whole numbers. Option D reverses the order: the question asks Search to Payments, and order matters in ratios. In practice, a 3:2 split tells your team that Search carries proportionally more defect load, which might influence where retesting time is spent — proportional thinking like this supports the risk-based approach your discipline is built on.

**Question 7 (moderate) — Percentage change in open defects**

On Monday your project had 25 open defects. By Friday it had 18. By what percentage did open defects fall over the week (to the nearest whole percent)?

- A) 7%
- B) 25%
- C) 28%
- D) 38%

**Correct answer: C**

**Explanation:** Percentage change = (change ÷ original) × 100. Step 1: the change is 25 − 18 = 7 defects. Step 2: divide by the original (Monday) figure: 7 ÷ 25 = 0.28. Step 3: multiply by 100 to get 28%. The answer is 28%. Option A (7%) confuses the raw change with the percentage. Option D (about 38%) comes from dividing by the new figure (7 ÷ 18 ≈ 0.389) — a very common error; percentage change always divides by the starting value. Reporting that "open defects fell 28% this week" is a much more informative message to stakeholders than raw counts alone, and getting the base right keeps the message honest.

**Question 8 (moderate) — Reading a two-way results table**

Your regression run results, split by area and outcome:

| Area | Passed | Failed | Blocked |
|---|---|---|---|
| Accounts | 22 | 3 | 0 |
| Search | 17 | 2 | 6 |
| Payments | 28 | 7 | 0 |

What percentage of the Search area's test cases were blocked (to the nearest whole percent)?

- A) 6%
- B) 24%
- C) 26%
- D) 35%

**Correct answer: B**

**Explanation:** First find the Search row total: 17 + 2 + 6 = 25 test cases. The blocked count is 6. Percentage blocked = 6 ÷ 25 × 100. Step by step: 6 ÷ 25 = 0.24, and 0.24 × 100 = 24%. The answer is 24%. Option A mistakes the raw count for a percentage. Option C uses the wrong denominator (6 ÷ 23, from adding only Passed and Blocked or a similar slip). The two-step discipline — build the correct denominator first, then divide — is the key to every table percentage. In real reporting, a 24% blocked rate in one area is a flag worth raising: blocked tests often mean an environment or data problem, and raising that awareness early is precisely your role's defect-awareness duty.

**Question 9 (moderate) — Retest arithmetic**

Of 30 defects fixed by developers this sprint, you retested all 30. 24 passed retest and were closed; the rest reopened. What percentage of fixes failed retest?

- A) 6%
- B) 20%
- C) 24%
- D) 80%

**Correct answer: B**

**Explanation:** Failed retests = 30 − 24 = 6. Percentage = 6 ÷ 30 × 100. Step by step: 6 ÷ 30 = 0.2, and 0.2 × 100 = 20%. The answer is 20%. Option A is the raw count dressed as a percentage; option D (80%) is the pass rate, answering the opposite question to the one asked. Read the final sentence of a numeric question twice — "failed retest", not "passed" — because the arithmetic is often easy while the reading is where marks are lost. A 20% reopen rate is also genuinely useful test intelligence: it suggests fixes are arriving under-checked, which your team might raise with developers — turning your careful retesting and escalation into better quality upstream.

**Question 10 (challenging) — Combining rates across suites**

Your automated suite has two parts. The smoke suite has 50 checks with a 96% pass rate this morning. The full regression suite has 150 checks with an 88% pass rate. What is the overall pass rate across all 200 checks?

- A) 88%
- B) 90%
- C) 92%
- D) 94%

**Correct answer: B**

**Explanation:** You cannot simply average 96% and 88% (that would give 92%) because the suites are different sizes — the bigger suite must count for more. Work with actual counts. Smoke passes: 96% of 50 = 0.96 × 50 = 48. Regression passes: 88% of 150 = 0.88 × 150 = 132. Total passes: 48 + 132 = 180. Overall rate: 180 ÷ 200 = 0.9 = 90%. The answer is 90%. Notice it sits closer to 88% than to 96% because the regression suite is three times larger — a weighted average always leans towards the bigger group. Option C is the trap for people who average the percentages directly. When you support the maintenance of automated tests and report suite health, weighting by suite size is the difference between an accurate picture and a flattering one.

**Question 11 (challenging) — Trend reading and projection**

Defects found per week over four weeks of testing: Week 1: 20, Week 2: 16, Week 3: 12, Week 4: 8. If the trend continues at the same rate, how many defects would you expect in Week 6?

- A) 0
- B) 2
- C) 4
- D) 6

**Correct answer: A**

**Explanation:** First identify the trend: 20 → 16 → 12 → 8 falls by 4 each week — a steady decrease of 4. Continue the pattern: Week 5 would be 8 − 4 = 4, and Week 6 would be 4 − 4 = 0. The answer is 0. Option C (4) is Week 5's figure — a classic off-by-one from stopping the projection a step early, so count the weeks on your fingers if you must. Falling defect discovery is a familiar late-testing pattern, and teams sometimes use it to judge readiness for release. But carry a tester's caution: a projection is an expectation, not a promise — defect discovery can also fall because testing slowed down or moved to well-worn areas. Explaining how to measure the effectiveness of testing includes understanding both what a metric suggests and what it cannot prove.

**Question 12 (challenging) — Multi-step effort calculation**

Your supervisor asks you to estimate a small test run. There are 24 test cases: three-quarters are simple (10 minutes each) and the rest are complex (25 minutes each). You also need 30 minutes to set up the environment before starting. What is the total estimated time?

- A) 5 hours 0 minutes
- B) 5 hours 30 minutes
- C) 6 hours 0 minutes
- D) 6 hours 30 minutes

**Correct answer: C**

**Explanation:** Break the problem into parts and keep the units straight. Step 1 — split the cases: three-quarters of 24 = 24 × 3 ÷ 4 = 18 simple cases, leaving 24 − 18 = 6 complex cases. Step 2 — simple time: 18 × 10 = 180 minutes. Step 3 — complex time: 6 × 25 = 150 minutes. Step 4 — add everything, including setup: 180 + 150 = 330, and 330 + 30 = 360 minutes. Step 5 — convert to hours: 360 ÷ 60 = 6 hours exactly. The answer is 6 hours 0 minutes. Option B (5 hours 30) is what you get if you forget the setup time — the most common slip in multi-part estimates, because setup is stated in a different sentence from the test cases. Option A comes from mis-splitting the cases (half and half instead of three-quarters and a quarter). The technique to remember: list every component before calculating any of them, then tick each one off as you add it. This is a miniature of real test effort estimation, which the test engineer role performs as part of a risk-based approach — and real estimates fail most often not through bad arithmetic but through forgotten components, exactly like that setup step.

### Preparation tips

- **Rebuild the basics until they are automatic.** Percentages (part ÷ whole × 100), percentage change (change ÷ original × 100), averages (total ÷ count), and ratios (divide both sides by the common factor). Ten minutes of drill a few times a week makes these reflexes.
- **Always identify the denominator first.** Before dividing anything, ask: "out of what?" Most numeric errors are correct arithmetic on the wrong base.
- **Use your own project's numbers.** At the end of each day, calculate your personal pass rate, your average execution time, and the percentage of the plan complete. Real numbers make practice meaningful and painless.
- **Write the steps down.** Even with a calculator, jot each intermediate result. It prevents slips and lets you re-verify quickly.
- **Sense-check every answer.** Is it between the smallest and largest plausible values? Does the complement add to 100%? Does a weighted average lean towards the bigger group? Three seconds of checking saves whole marks.
- **Practise reading questions twice.** The arithmetic in these tests is rarely the hard part; the question's final sentence is. "Failed", "passed", "open", "closed", "of the Search area" — every word narrows the calculation.

### Common pitfalls to avoid

- **Averaging percentages from different-sized groups.** A 96% rate on 50 checks and an 88% rate on 150 checks do not average to 92%. Convert to counts, add, then divide by the combined total.
- **Dividing by the new value in percentage change.** Percentage change always divides by the original (starting) figure. Dividing by the final figure is the single most common percentage-change error.
- **Wrong-column and wrong-row errors.** In a table question, physically locate the row and column named in the question before touching your calculator.
- **Answering the opposite question.** Pass rate when the question asked fail rate; open when it asked closed. Underline (mentally or on paper) the quantity actually requested.
- **Off-by-one in projections.** When projecting a trend to "Week 6", count each step explicitly. Stopping one step early is the standard trap.
- **Abandoning correct working under pressure.** If your twice-checked answer is not among the options, recheck once more — then trust your method, pick the closest option, and move on without spiralling. Confidence in verified working is a tester's asset in assessments and in defect triage alike.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment measures how accurately you read, understand, and reason about written material of the kind your job produces: user stories, test plans, defect descriptions, process guidance, emails from stakeholders, and extracts from standards such as the GOV.UK Service Standard. The classic format presents a short passage followed by statements, and for each statement you decide whether it is **true** (the passage supports it), **false** (the passage contradicts it), or **cannot say** (the passage gives too little information either way). Other question styles include picking the best summary of a passage, identifying what can properly be inferred, and judging which of several sentences communicates most clearly.

The typical format is an online, timed test of 15 to 25 minutes with 20 to 30 statements spread across several passages. The golden rule is that you must judge each statement using only the passage — not your background knowledge, however good it is. This feels strange at first and becomes natural with practice.

Why does verbal reasoning matter so much for an associate test engineer? Because reading precisely is the beginning of all testing. A test script is only as good as your reading of the user story behind it; a defect report is only as useful as the accuracy of its words; and a misread sentence in a plan can send hours of effort in the wrong direction. Your role also includes communicating between the technical and the non-technical — explaining why it is important to express technical concepts in plain language — and that starts with understanding, exactly, what a text does and does not say. Employers assess verbal reasoning for testing roles because testers are, in a real sense, professional careful readers.

### How this assessment maps to your role

- **Comprehension of requirements and stories** maps to your **Test analysis** skill: analysing information such as user stories, prototypes, processes and designs, with support, is applied reading comprehension — the passage is the story, and the statements are your candidate test conditions.
- **True/false/cannot-say discipline** maps to your **Designing and executing tests** skill: a test should verify what the requirement states, not what you assume; "cannot say" is the verbal twin of "this needs clarifying with the analyst before I script it".
- **Reading process documents accurately** maps to your **Managing, reporting and resolving defects** and **Test and quality planning** skills: following a defect management process, and following quality testing approaches and plans with support, both depend on reading procedural text and applying it faithfully.
- **Clear-writing judgement** maps to your **Communicating between the technical and non-technical** skill: explaining why technical concepts should be communicated in non-technical language — and recognising which sentence does that best — is exactly what clear-writing questions measure.
- **Understanding tools and standards text** maps to your **Test engineering** skill: following test engineering practices and standards, with support, starts with reading the standard correctly.

### Practice questions

**Question 1 (easy) — True/false/cannot-say on a process extract**

Passage: "All defects must be recorded in the tracking tool on the day they are found. Defects rated Critical must also be reported verbally to the test lead within one hour of discovery. Defects found after 16:00 may be recorded by 10:00 the following working day."

Statement: "A Medium defect found at 11:00 must be recorded in the tracking tool the same day."

- A) True
- B) False
- C) Cannot say

**Correct answer: A**

**Explanation:** The passage's first sentence sets the general rule: all defects are recorded the day they are found. The only exception is for defects found after 16:00, and 11:00 is well before that, so the exception does not apply. The verbal-reporting rule concerns Critical defects only and does not change the recording rule for a Medium defect. Everything needed is in the passage, and the statement matches it, so the answer is True. The technique: identify the general rule, then check whether any stated exception applies to the case in the statement. This mirrors how you follow a defect management process in real work — general rule first, exceptions second, and never an invented exception in between.

**Question 2 (easy) — True/false/cannot-say on the same passage**

Passage (as in Question 1): "All defects must be recorded in the tracking tool on the day they are found. Defects rated Critical must also be reported verbally to the test lead within one hour of discovery. Defects found after 16:00 may be recorded by 10:00 the following working day."

Statement: "High defects must be reported verbally to the test lead."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** The passage says defects rated Critical "must also be reported verbally". The word "also" marks verbal reporting as an additional duty attached specifically to Critical defects. For High defects, the passage imposes only the recording rule; it attaches no verbal-reporting duty to them. Because the passage explicitly reserves that duty for Critical defects, a claim that High defects "must" be reported verbally contradicts the passage's allocation of duties, so the statement is False rather than Cannot say. Be careful with this distinction: Cannot say is for matters the passage genuinely leaves open, while False is for statements the passage's wording rules out. Reading modal words — must, may, should — with precision is a tester's superpower: requirements hang entire behaviours on exactly these words.

**Question 3 (easy) — Comprehension of a user story**

Passage: "As a caseworker, I want to filter applications by submission date, so that I can process the oldest applications first. The filter must default to showing the oldest applications at the top. Caseworkers can reverse the order with one click."

Statement: "By default, the newest applications appear at the top of the list."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** The passage states the filter "must default to showing the oldest applications at the top". The statement claims the opposite — newest at the top by default — so it directly contradicts the passage and is False. This is the most straightforward kind of verbal question, but it rewards a habit worth naming: find the exact sentence in the passage that speaks to the statement, and compare the two word by word. In your day job this is the difference between a test script that checks the default order correctly and one that quietly enshrines the wrong behaviour as "expected". When you analyse user stories with support, defaults are among the first test conditions you extract — and among the most commonly misread.

**Question 4 (easy) — Choosing the clearest sentence**

Your test engineer asks you to draft one sentence for a non-technical product manager, explaining a failed check. Which version communicates most clearly?

- A) "The Selenium locator for the submit CTA threw a NoSuchElementException post-DOM-mutation."
- B) "The automated check could not find the Submit button on the page, so it failed — we are investigating whether the page changed or the check needs updating."
- C) "Test failure occurred consequent to element non-location within the object hierarchy."
- D) "It broke."

**Correct answer: B**

**Explanation:** Option B says what happened (the check could not find the Submit button), what the result was (the check failed), and what happens next (investigation of two possible causes) — in plain words a non-technical reader understands. Option A is accurate for an engineer but drowns a product manager in tool and code vocabulary. Option C uses formal-sounding abstract phrasing that communicates less than it appears to. Option D is plain but so vague it transfers no useful information. Your role explicitly includes explaining why it is important to communicate technical concepts in non-technical language, and this question shows the standard to aim for: plain words, concrete subject, cause and next step included, jargon translated or dropped. Clear writing is not "dumbing down" — it is doing the reader's decoding work for them.

**Question 5 (moderate) — Cannot-say discipline**

Passage: "The service team runs automated accessibility checks on every build. Last month, the checks found 14 issues, of which 11 were fixed within the month. The team also carries out manual accessibility testing before each major release."

Statement: "The three remaining accessibility issues were fixed at the start of this month."

- A) True
- B) False
- C) Cannot say

**Correct answer: C**

**Explanation:** The passage tells you 14 issues were found and 11 were fixed within the month, so three remained unfixed at month end. But it says nothing at all about what happened afterwards — the remaining three might have been fixed the next morning, scheduled for later, or reclassified. Because the passage neither supports nor contradicts the statement, the answer is Cannot say. Feel the difference from Question 3: there, the passage directly contradicted the statement (False); here, it is simply silent (Cannot say). Assessment writers rely on your urge to assume a tidy ending — teams usually fix things, so surely they were fixed? — but "usually" is background assumption, not passage content. The same discipline protects your testing: what a document does not say is a question to raise, never a fact to assume.

**Question 6 (moderate) — Inference from a standards extract**

Passage: "Point 5 of the Service Standard requires teams to make sure everyone can use the service, including people with disabilities and people with limited digital skills or access. Testing with assistive technologies, such as screen readers, is one way teams provide evidence of meeting this point."

Which one of the following can properly be inferred?

- A) Screen reader testing is the only way to evidence Point 5.
- B) Point 5 concerns only people with disabilities.
- C) Testing with assistive technologies can contribute evidence towards meeting Point 5.
- D) Every team must test with every available assistive technology.

**Correct answer: C**

**Explanation:** The passage says assistive-technology testing is "one way" to provide evidence — so it can contribute evidence, which is exactly option C and nothing more. Option A turns "one way" into "the only way", a quantifier distortion. Option B narrows the scope wrongly: the passage explicitly includes people with limited digital skills or access as well as people with disabilities. Option D inflates "such as screen readers" into a universal obligation the passage never states. Inference questions reward the smallest claim fully supported by the text. This maps directly to your work: quality characteristics such as accessibility are among those you describe and test for, and reading standards precisely — neither shrinking nor stretching them — is how testing stays aligned with what government services must actually achieve.

**Question 7 (moderate) — Reading an email chain accurately**

Passage: "From: Priya (developer), Monday 09:12 — 'The date validation fix is in build 42, deploying to the test environment at lunchtime.' From: Sam (test engineer), Monday 09:30 — 'Thanks. Ada, please retest defect D-118 once build 42 is in the test environment. Note the fix covers UK date formats only; international formats are out of scope for this sprint.'"

Statement: "Ada should retest D-118 using international date formats on Monday morning."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** Two parts of the statement fail. Timing: the build reaches the test environment "at lunchtime", and Sam says to retest "once build 42 is in the test environment" — so Monday morning is too early; the fix would not yet be there. Scope: Sam explicitly says international formats are out of scope this sprint, so retesting with them is contrary to the stated instruction. Either failure alone makes the statement contradict the passage, so it is False. Email-chain questions test whether you can assemble facts spread across multiple messages — exactly what you do daily when instructions arrive in fragments. Before retesting a defect, a careful associate assembles: which build contains the fix, where and when it will be deployed, and what the fix does and does not cover. Retesting the right thing at the wrong time, or the wrong thing at the right time, both waste effort.

**Question 8 (moderate) — Best summary of a passage**

Passage: "Exploratory testing is an approach in which the tester designs and executes tests in the moment, guided by what they learn as they go, rather than following pre-written scripts. It complements scripted testing: scripts confirm known expectations efficiently, while exploration can reveal unexpected problems scripts would never look for. Many teams timebox exploratory sessions and record findings in brief charter notes."

Which is the best summary?

- A) Exploratory testing replaces scripted testing because scripts cannot find unexpected problems.
- B) Exploratory testing is unstructured guesswork and should be avoided in government services.
- C) Exploratory testing means designing tests while executing them; it complements scripts by finding unexpected issues, and is often timeboxed with brief notes.
- D) Timeboxing is the most important part of testing.

**Correct answer: C**

**Explanation:** A good summary keeps every main claim and adds nothing. The passage makes three claims: what exploratory testing is (in-the-moment design), how it relates to scripting (complements, not replaces), and how teams manage it (timeboxed sessions, charter notes). Option C captures all three faithfully. Option A distorts "complements" into "replaces" — the passage explicitly says scripts remain valuable. Option B contradicts the passage's neutral-to-positive treatment and inserts an opinion found nowhere in the text. Option D promotes a supporting detail into the main point. Summary questions mirror a real skill: when you relay a testing concept to a stakeholder or a stand-up, you compress without distorting. As someone learning to contribute to decisions about test types and techniques, being able to state accurately what exploratory testing is — and is not — is a small but genuine professional asset.

**Question 9 (moderate) — Following procedural text**

Passage: "Before executing the payment test suite: (1) confirm the test environment shows build 57 or later; (2) load the anonymised test data pack TD-9; (3) if the data pack fails to load, do not proceed — notify the environment team and record a blocker; (4) after execution, export results and attach them to the test run record."

You confirm the environment shows build 58, but data pack TD-9 fails to load. What does the procedure require?

- A) Proceed with real customer data instead.
- B) Proceed without data, noting the problem afterwards.
- C) Stop, notify the environment team, and record a blocker.
- D) Reinstall the environment yourself.

**Correct answer: C**

**Explanation:** Walk the steps in order. Step 1 is satisfied: build 58 is "57 or later". Step 2 fails: TD-9 will not load. Step 3 tells you exactly what to do in that situation: do not proceed, notify the environment team, record a blocker — which is option C, almost word for word. Option A is not only outside the procedure but seriously wrong in a government context: the procedure specifies anonymised data precisely because real citizen data must not be used in test environments without proper controls. Option B violates the explicit "do not proceed". Option D invents an action the procedure does not authorise and an associate would not perform alone. Procedural questions reward finding the branch that matches your situation and following it faithfully — the same skill as following test engineering practices and defect processes with support, where the process exists to protect the service and the people who use it.

**Question 10 (challenging) — True/false/cannot-say with subtle wording**

Passage: "The team's definition of done states that a story is complete only when its acceptance tests pass in the test environment and the code has been peer reviewed. Story S-204's acceptance tests passed in the test environment on Thursday. The peer review of S-204 is scheduled for Friday morning."

Statement: "Story S-204 was not complete on Thursday."

- A) True
- B) False
- C) Cannot say

**Correct answer: A**

**Explanation:** The definition of done sets two conditions, both required: passing acceptance tests and completed peer review. On Thursday, the first condition was met, but the peer review was still "scheduled for Friday morning" — meaning it had not yet happened on Thursday. With one required condition unmet, the story cannot have been complete on Thursday, so the statement is True. The subtlety is the negative phrasing: the statement asserts that the story was not complete, and many candidates misread negatives under time pressure, flipping their answer. Technique: rewrite the statement positively in your head ("the story was complete on Thursday"), judge that ("false — review not done"), then flip back ("so 'not complete' is true"). Definition-of-done logic is bread and butter in your team's quality planning: an "only when both" rule means every condition is a gate, and testers are often the people who politely point out that a gate is still open.

**Question 11 (challenging) — Identifying the unsupported claim in a report**

Passage: "Regression testing of release 3.2 is complete. Of 180 test cases, 171 passed and 9 failed. All 9 failures relate to the reporting module. The reporting module is scheduled for replacement in release 3.3."

A colleague drafts four statements for the test summary report. Which one is NOT supported by the passage?

- A) "95% of regression test cases passed."
- B) "All failures were confined to the reporting module."
- C) "The failures will not affect users, because the reporting module is being replaced."
- D) "Regression testing for release 3.2 has finished."

**Correct answer: C**

**Explanation:** Check each statement against the passage. A: 171 ÷ 180 = 0.95, so 95% is arithmetically supported. B: the passage says all nine failures relate to the reporting module — supported. D: the passage's first sentence says regression testing is complete — supported. C makes two moves the passage does not: it claims the failures "will not affect users" (the passage says nothing about user impact — a module can be both scheduled for replacement and harming users today), and it presents the replacement as a reason for that claim (a future replacement in 3.3 does nothing for users of 3.2). This is exactly the kind of comforting over-claim that slips into test reports and misleads decision makers. Your role includes clearly reporting and communicating defects with appropriate information; the discipline of separating "what we observed" from "what we hope" is what makes a test report trustworthy — and spotting the difference in others' drafts is a skill worth building early.

**Question 12 (challenging) — Reconciling two documents**

Passage: "Test plan extract: 'Smoke tests run on every deployment to any environment. Full regression runs before each production release.' Team wiki extract, updated later: 'To save pipeline time, smoke tests now run on deployments to the test and staging environments only. Full regression continues to run before each production release.'"

Statement: "According to the most recent guidance, smoke tests run on every deployment to any environment."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** Two documents conflict, and the question tells you which is more recent: the wiki was "updated later". The statement asks about "the most recent guidance", which is therefore the wiki — and the wiki restricts smoke tests to the test and staging environments only, not "any environment". The statement contradicts the most recent guidance, so it is False. The trap is anchoring on the first document you read: the test plan does say "every deployment to any environment", and a hurried reader pattern-matches the statement to it and answers True. Real testing work constantly involves documents that disagree — a plan, a wiki, a ticket, a conversation — and the professional habits are the ones this question rehearses: establish which source is current, read the current one precisely, and (in real life, beyond the assessment) flag the stale document so the next reader is not misled. That last step is your communication skill in action: raising a small documentation inconsistency is an easy, valuable contribution an associate can make from week one.

### Preparation tips

- **Read something procedural every day.** A defect process, a test plan section, a GOV.UK standard page. After reading, quiz yourself: what must happen, what may happen, what is forbidden, what is simply not covered?
- **Train the true/false/cannot-say reflex.** For every statement, ask two questions in order: "Does the passage support this?" (if yes — true), "Does the passage contradict this?" (if yes — false), and only then default to cannot say. The ordered check prevents the common blur between false and cannot say.
- **Watch the small words.** Must, may, only, all, some, unless, also, at least. Testers already know these words carry requirements on their backs — verbal tests simply measure how consistently you notice them.
- **Rewrite negatives.** When a statement contains "not", "never", or "no longer", rephrase it positively, judge it, then flip your judgement back. This one habit prevents a whole family of errors.
- **Practise summarising aloud.** After reading any work document, state its main points in two sentences to yourself. Summary questions — and stand-up updates — both become easy.
- **Use only the passage.** Your growing domain knowledge is an asset at work, but in the test it is a liability if it leaks into answers. Pretend each passage describes an unfamiliar system, and judge statements only against what is written.

### Common pitfalls to avoid

- **Importing outside knowledge.** You may know how defect tools or pipelines usually work; the passage may describe them differently. The passage always wins.
- **Confusing "false" with "cannot say".** False means the passage contradicts the statement; cannot say means the passage is silent. If you cannot point to the contradicting sentence, do not answer false.
- **Quantifier stretching.** "One way" is not "the only way"; "some" is not "all"; "may" is not "must". Most wrong inference options are quantifier stretches of true sentences.
- **Anchoring on the first document.** When a question includes two sources, check dates and precedence before judging any statement.
- **Misreading negatives under time pressure.** Statements with "not" flip more answers than hard vocabulary ever does. Slow down for one extra breath on every negative statement.
- **Choosing summaries that add comfort.** The "best summary" never contains reassurance, blame, or predictions absent from the passage. If a summary option sounds kinder or more confident than the text, it is probably wrong.

## Workplace job-specific situational judgement assessment

### About this assessment

A situational judgement assessment (often called an SJT) presents realistic workplace dilemmas and asks you to judge the effectiveness of different responses. There are usually no equations and no passages to parse — instead, each question describes a scenario you could plausibly face as an associate test engineer, followed by four possible actions. Common formats ask you to pick the most effective response, the least effective response, or both; some ask you to rate every option, or to rank them from best to worst.

The typical format is an online, untimed or generously timed test of 15 to 25 scenarios, taking 25 to 45 minutes. There is no adaptive difficulty; instead, your pattern of choices is compared with judgements made by experienced professionals and occupational psychologists who designed the scoring key. That means the "right" answers are not secret tricks — they reflect widely shared professional values: focus on users, honesty and ownership, collaboration, asking for help at the right moment, treating colleagues with respect, and protecting quality and safety.

Why do employers use SJTs for associate-level testing roles? Because at your career stage, behaviour matters at least as much as technique. Your role summary says you work closely with test engineers and quality assurance test analysts to learn, you develop test scripts under supervision, and you raise awareness of defects. Every one of those involves judgement calls: when to ask for help and when to try first, how to report a problem honestly without drama, how to respond when priorities clash, and how to treat a mistake — your own or someone else's. An SJT rehearses those calls safely, and thinking through the explanations here will genuinely prepare you for the situations themselves.

One reassuring note: SJTs are not personality tests, and they are not about being perfect. They reward the same instincts your team is already helping you build — honesty, care, user focus, and sensible escalation.

### How this assessment maps to your role

- **Escalation and ownership scenarios** map to your **Managing, reporting and resolving defects** skill: knowing when to retest, when to escalate, and how to communicate a defect calmly and factually.
- **Asking-for-help scenarios** map to your role level itself — working closely with test engineers and analysts **to learn** the activities and techniques of testing: an associate who asks well is doing the job right, not failing at it.
- **Stakeholder communication scenarios** map to your **Communicating between the technical and non-technical** skill: choosing what to say, to whom, in what language, and understanding the impact of different types of communication with internal and external stakeholders.
- **Priority-clash scenarios** map to your **Test and quality planning** skill: following agreed approaches and plans, and speaking up when reality stops matching the plan.
- **Quality-under-pressure scenarios** map to your **Test analysis** and **Designing and executing tests** skills: protecting alignment with user needs and honest coverage even when time is short — and explaining what might be a risk to achieving quality goals.

### Practice questions

**Question 1 (easy) — You find a defect just before a demo**

Thirty minutes before your team demonstrates a new feature to the service owner, you find a defect: the confirmation page shows the wrong reference number format. Your test engineer is in a meeting. What is the most effective response?

- A) Say nothing — you might be wrong, and you do not want to cause a fuss before a demo.
- B) Record the defect in the tracking tool with clear details, and send your test engineer and the developer a brief message now so the team can decide what to do before the demo.
- C) Interrupt the service owner directly to tell them their demo will be embarrassing.
- D) Try to fix the code yourself quickly.

**Correct answer: B**

**Explanation:** Option B does everything your role asks: it records the defect properly (following the defect management process with appropriate information), and it communicates promptly to the right people — the test engineer and developer — who can decide whether to mention it, work around it, or delay the demo. That is raising awareness of defects, exactly as your role describes, while leaving decisions above your level to the people who should make them. Option A is the least effective: hiding a known defect before a demo risks the team's credibility and the service owner's trust, and "I might be wrong" is a reason to describe what you saw, not to stay silent. Option C bypasses your team and communicates alarm rather than information to a senior stakeholder — the wrong channel and the wrong tone. Option D exceeds an associate's remit, and untested last-minute fixes are how one defect becomes two. The professional behaviours rewarded here are ownership, honest communication, and respect for team decision-making.

**Question 2 (easy) — You do not understand a task**

Your test engineer asks you to "knock together a quick boundary test for the age field" and hurries off to a meeting. You are not fully sure what boundary testing involves. The test is not needed until tomorrow. What is the most effective response?

- A) Guess what boundary testing means and hope for the best.
- B) Do nothing until the test engineer returns, then explain you were stuck all afternoon.
- C) Spend a short time researching boundary testing in your team's guidance and notes, draft the test, and ask the test engineer to check your draft when they return.
- D) Ask a different team's manager to explain it.

**Correct answer: C**

**Explanation:** Option C combines initiative with honesty about your learning stage — the exact blend your role level describes when it says you work closely with experienced colleagues to learn techniques. You use the time productively (researching and drafting), and you close the loop with a review request, so any misunderstanding is caught before it matters. Option A risks building the wrong test and, worse, silently normalising guesswork. Option B wastes an afternoon and reframes a normal learning moment as a blockage; associates are expected to ask and to try, not to wait passively. Option D leaps over your own team to an unrelated manager — inefficient and mildly disruptive when your own team's guidance and your own supervisor are the natural sources. Notice the general SJT pattern: options that combine trying, learning, and verifying usually beat options that only wait, only guess, or only escalate.

**Question 3 (easy) — A developer pushes back on your defect report**

A developer replies to your defect report: "This isn't a bug — it works fine on my machine. Closing it." You retest carefully in the test environment and the problem still occurs, exactly as you described. What is the most effective response?

- A) Reopen the defect with a note of your retest evidence — environment, build number, steps, and a screenshot — and ask the developer (politely, offering a quick screen-share) to look together.
- B) Accept the closure — developers know the code better than you do.
- C) Reply-all to the team channel saying the developer is wrong.
- D) Reopen the defect with the comment "It is definitely a bug."

**Correct answer: A**

**Explanation:** Your role includes retesting and escalating defects when needed, and following the process to maintain defects with appropriate information. Option A does both: it reopens with evidence (the environment and build details explain the "works on my machine" discrepancy — the two of you are probably looking at different builds or configurations), and it invites collaboration rather than confrontation. That respects the developer while standing firmly on facts. Option B abandons a verified observation out of deference; seniority in code does not outrank evidence from the test environment, and quietly dropping real defects harms users. Option C makes it public and personal — collaboration rarely survives a reply-all correction. Option D reopens without new information, which invites a second closure and a stalemate. The behaviours rewarded: evidence over assertion, courtesy over conflict, and persistence in service of quality.

**Question 4 (easy) — You made a mistake in yesterday's results**

Reviewing your work from yesterday, you realise you marked a test as passed that you now believe you executed against the wrong build. The results have already been included in the team's progress report. What is the most effective response?

- A) Quietly rerun the test today and change the record if it fails, saying nothing about yesterday.
- B) Tell your test engineer straight away what happened, correct the record, and rerun the test on the right build as soon as possible.
- C) Say nothing — one test out of many will not matter.
- D) Wait until someone notices, then explain.

**Correct answer: B**

**Explanation:** Option B is prompt, honest, and complete: the supervisor learns the report may need a footnote, the record is corrected, and the missing evidence is regenerated quickly. Everyone makes execution mistakes — what distinguishes professionals is the speed and openness of the correction. Option A fixes the record only conditionally and hides the report impact; if the rerun passes, the report's provenance is still wrong and nobody knows. Option C gambles the team's decisions on "probably fine" — but reports exist precisely so others can rely on them, and a single wrong "pass" can be the one covering the defect that matters. Option D outsources your integrity to chance. SJT scoring keys consistently reward early self-correction over concealment, and so do real teams: a tester whose records can be trusted, including trusted to be corrected loudly when wrong, is a tester whose word carries weight — the foundation of everything else in your career.

**Question 5 (moderate) — Pressure to cut testing short**

A delivery manager, under deadline pressure, says to you directly: "Can you just mark the remaining ten test cases as passed? They're low-risk screens and we need to ship today." Your test engineer is on leave. What is the most effective response?

- A) Do as asked — the delivery manager is senior to you.
- B) Refuse loudly and tell colleagues the delivery manager tried to corrupt the results.
- C) Explain politely that you cannot record tests as passed without running them, offer what you can honestly do (for example, run the highest-risk ones now), and escalate promptly to the test engineer's cover or your line manager.
- D) Mark them passed but keep a private note that you did not run them.

**Correct answer: C**

**Explanation:** Recording unexecuted tests as passed is falsifying quality evidence — it is never within anyone's gift to ask and never within yours to do, regardless of seniority. Option C handles it professionally in three moves: a polite, firm boundary ("I can't record what didn't run"); a constructive alternative that serves the deadline honestly (prioritised execution of the riskiest remaining cases — a genuinely risk-based response); and escalation to appropriate cover, because a request like this needs visibility beyond an associate. Option A follows an improper instruction; "they told me to" does not restore falsified records. Option B protects the records but torches the relationship and skips the constructive middle — the delivery manager is under pressure, not malicious, and deserves a professional response first. Option D is the worst of both worlds: the official record lies, and your private note proves you knew. The behaviours rewarded: integrity, user focus (those "low-risk" screens serve real people), constructive problem-solving, and proper escalation.

**Question 6 (moderate) — Conflicting instructions**

Your test engineer asked you this morning to spend today writing scripts for Feature A. At midday, a quality assurance test analyst from your team asks you to drop that and execute regression tests for Feature B this afternoon, saying it is urgent. What is the most effective response?

- A) Silently switch to Feature B — the most recent instruction wins.
- B) Silently continue with Feature A — the first instruction wins.
- C) Tell the analyst you have conflicting instructions, and quickly check with your test engineer (a short message will do) so the two of them can agree your priority.
- D) Try to do both by doing each half-heartedly.

**Correct answer: C**

**Explanation:** An associate should not privately adjudicate between two experienced colleagues' priorities — not because you lack judgement, but because you may lack context (the analyst's "urgent" may reflect a release decision you have not heard about, or the test engineer's plan may reflect a commitment the analyst has not heard about). Option C surfaces the conflict transparently and cheaply: one short message usually resolves it in minutes, and both colleagues keep an accurate picture of your work. Options A and B each gamble on a rule of thumb ("most recent wins" / "first wins") that has no standing; whichever you pick silently, one colleague's plan fails without warning. Option D guarantees both tasks are done badly — divided attention is where testing errors breed. This maps to your communication skill: understanding the types of communication used with stakeholders and their impact includes knowing that a quick clarifying message, sent early, is often the highest-value communication of the day.

**Question 7 (moderate) — You spot a possible risk nobody mentioned**

While analysing a user story about document upload, you notice it says nothing about what happens when a user uploads a file larger than the size limit. You are new to this service, and it is possible this is covered elsewhere. What is the most effective response?

- A) Assume it is covered elsewhere and script only what the story states.
- B) Raise it as a question with the test engineer or the story's business analyst: "The story doesn't say what happens for oversized files — is that defined somewhere, or is it a gap?"
- C) Invent an expected behaviour yourself (an error message you would consider sensible) and script a test against it.
- D) Raise a defect against the story.

**Correct answer: B**

**Explanation:** Your role says you analyse information such as user stories with support and explain what might be a risk in achieving quality goals — and an unspecified failure path is a textbook quality risk. Option B raises it in the right shape: as a question, aimed at the people who can answer, phrased neutrally so it lands as help rather than criticism. New team members often see gaps veterans have stopped noticing; asking is a contribution, not an interruption. Option A scripts around the gap, leaving the risk invisible until a citizen with a large file finds it in production. Option C is subtler but dangerous: inventing expected behaviour turns your assumption into the "standard" the system is checked against, without anyone agreeing to it. Option D uses a defect record for what is currently a question — defects are for observed misbehaviour or agreed requirement breaches; premature defects clutter the process your team relies on. The rewarded behaviours: curiosity, user focus, and routing questions to their owners.

**Question 8 (moderate) — A teammate is struggling**

Another associate on your team confides that they are falling behind on their assigned regression tests and are scared to tell the test engineer. The regression run feeds this Friday's release decision. What is the most effective response?

- A) Offer to help with some of their tests if your own workload allows, and encourage them warmly to tell the test engineer today — offering to sit with them while they do.
- B) Tell the test engineer yourself immediately, without telling your colleague you are doing so.
- C) Say nothing — it is their problem, not yours.
- D) Take over all their tests secretly so nobody finds out they fell behind.

**Correct answer: A**

**Explanation:** Two things need to happen: the release decision needs accurate information about regression progress, and your colleague needs support rather than exposure. Option A serves both — practical help within your capacity, plus encouragement (and companionship) towards the honest conversation that must happen today, because a Friday release decision built on an incomplete regression picture endangers users. Option B gets the information flowing but at the cost of your colleague's trust and their chance to own the disclosure; it might become necessary if they refuse, but it should not be the first move. Option C ignores both the team outcome and a struggling peer — testing is a team sport, and "not my problem" is corrosive in a discipline built on shared quality ownership. Option D compounds concealment: the team's picture of capacity stays wrong, your own work suffers silently, and the next sprint plans on a fiction. SJTs at associate level frequently probe this pattern: the strong answer pairs kindness with transparency, rather than choosing one against the other.

**Question 9 (moderate) — Boring but important work**

You have been asked to spend two days re-executing the same set of smoke tests after each of several deployment attempts, while the rest of the team works on more interesting exploratory testing. By the fourth run, you are confident nothing changes and are tempted to skim. What is the most effective response?

- A) Execute each run completely and carefully, using the repetition to also note any small ways the checklist could be improved or automated, and share those observations.
- B) Skim the later runs — check a few key screens and mark the rest passed from memory.
- C) Complain to the team that you always get the boring work.
- D) Ask a colleague to sign off runs you did not fully execute.

**Correct answer: A**

**Explanation:** Repetitive checks exist precisely because deployments can fail in quiet ways; the fourth run is as capable of catching a regression as the first, but only if it is genuinely executed. Option A does the assigned work with integrity and turns the repetition into value: noticing that a manual check is stable, tedious, and frequently repeated is exactly the observation that justifies automation — and your role explicitly includes explaining the value of automation within testing and supporting the maintenance of automated tests. Bringing that observation to your team is an associate-level contribution to continuous improvement. Option B is the silent corrosion of test evidence — "passed from memory" is not a test result. Option D is option B with a witness. Option C raises a fair development conversation in an unfair way; if the distribution of work concerns you, a calm one-to-one with your test engineer about your learning goals is the channel — and teams respond far better to "could I pair on exploratory testing next sprint?" than to complaints. The rewarded behaviours: conscientiousness, improvement-mindedness, and honest records.

**Question 10 (challenging) — Sensitive data in a test environment**

While executing tests, you notice that a test environment screen is displaying what appear to be real citizens' names and addresses, not the anonymised test data your team normally uses. Nobody else has mentioned it. What is the most effective response?

- A) Carry on testing — the data is probably fine, and it is not your area.
- B) Stop using that data, immediately tell your test engineer (or, if unavailable, your line manager) what you observed, and follow their direction — do not copy, share, or screenshot the records.
- C) Post a screenshot in the team channel asking "is this real data?"
- D) Delete the suspicious records yourself so nobody's data is exposed.

**Correct answer: B**

**Explanation:** Real personal data appearing in a test environment is a potential data protection incident, and in government it can affect real citizens' privacy. The right associate-level response has three parts, all in option B: stop interacting with the data (limiting further exposure), report immediately through your line (test engineer or manager — they know the incident process and who must be informed, potentially including a data protection officer), and avoid making copies — which is why the screenshot in option C, though well-intentioned, is exactly wrong: it duplicates personal data into a chat tool where it does not belong. Option A normalises a serious risk because raising it feels awkward; "not my area" does not apply to safeguarding citizens' data — noticing is everyone's area. Option D destroys evidence and possibly live records; deletion decisions belong to data owners following an assessed process, not to an individual tester acting alone. The rewarded behaviours: protecting the public, immediate escalation, and disciplined restraint about what you do not do. Questions like this also echo your real duty to explain why testing processes and environments are important — controlled, anonymised environments are not bureaucracy; they are how testing stays safe.

**Question 11 (challenging) — Least effective: demo day priorities**

Your team's stand-up reveals that today's priorities are: finish the regression run (needed tomorrow), and support a mid-morning bug triage. Mid-morning, a friendly developer asks if you can spend "an hour or two" helping them manually verify a pet refactoring change that is not on the sprint board. You would learn something interesting. Which response is LEAST effective?

- A) Explain you are committed to regression and triage today, and suggest they raise the verification work with the test engineer for proper prioritisation.
- B) Agree immediately and quietly spend two hours on it, leaving the regression run at risk.
- C) Offer to look at it after the regression run finishes, if time allows and your test engineer agrees.
- D) Ask the developer whether the change carries user-facing risk, so the team can judge its urgency properly.

**Correct answer: B**

**Explanation:** This question flips the format: you are asked for the least effective response, and careless reading is the biggest hazard — always check whether an SJT question asks for most or least. Option B is the weakest because it silently sacrifices a committed, deadline-bearing team priority (the regression run feeds tomorrow's decisions) for unplanned work, and does so invisibly, so nobody can manage the risk it creates. The other three are all reasonable professional moves: A protects the plan while routing the new work into proper prioritisation; C sequences generosity behind commitments and keeps your supervisor informed; D gathers the one fact (user-facing risk) that would legitimately change the priority conversation. Note that the least effective option is not the rudest-sounding one — it is the one that most damages outcomes and transparency. In real teams, helping colleagues is a virtue precisely when it is visible and prioritised; unplanned favours that quietly displace planned quality work are how regression runs get abandoned half-finished, and how trust in the plan erodes.

**Question 12 (challenging) — Automation results you do not trust**

You have been maintaining a small automated suite with support. This morning it reports all 60 checks passed in a surprisingly short runtime — about a tenth of the usual duration. Your team is about to quote the green run in the daily report. What is the most effective response?

- A) Let the report go out — green is green.
- B) Say you think automation is unreliable and the team should return to manual testing.
- C) Quickly investigate before the report goes out — check the run logs and one or two known behaviours by hand — and tell the team the green run needs verifying, because the runtime suggests the checks may not have actually executed.
- D) Rerun the suite repeatedly until the runtime looks normal, then report that run.

**Correct answer: C**

**Explanation:** A tenfold drop in runtime with a perfect pass rate is a classic signature of a suite that failed to run — checks skipped, an environment stubbed out, or a misconfiguration reporting vacuous success. Option C treats the suspicious result as untrusted until verified, and — crucially — says so before the team relies on it: log inspection plus a quick manual probe of known behaviour is a proportionate, associate-appropriate investigation, done with support if needed. This is your automation duty and your defect-awareness duty combined: supporting the maintenance of automated tests includes noticing when their results cannot be trusted, and raising awareness includes preventing a false green from reaching stakeholders. Option A forwards potentially false assurance — the most dangerous kind of test result, because it ends scrutiny. Option B overcorrects from one suspicious run to abandoning automation, contradicting the value of automation your role asks you to explain. Option D is quietly alarming: rerunning until output "looks right" is curve-fitting, not verification — if the environment is broken, a normal-looking runtime does not restore trust, and if it is not, you have learned nothing about this morning's anomaly. Rewarded behaviours: healthy scepticism, timely transparency, proportionate investigation, and protecting stakeholders from false confidence.

### Preparation tips

- **Learn the values, not the answers.** SJT keys reward user focus, honesty, collaboration, sensible escalation, and ownership. Before choosing, ask: "Which option best serves the user, the truth, and the team, in that order of my responsibility to act?"
- **Notice the escalation sweet spot.** At associate level, strong answers usually involve trying what is within your remit and informing or asking the right person at the right moment. Options that never escalate, or escalate everything instantly to senior people, are usually weaker.
- **Read whether it asks most or least effective.** Half the avoidable SJT errors are format misreads. Underline the word in your mind before judging options.
- **Rehearse with real memories.** Think of moments from your own weeks — a confusing instruction, a defect pushback, a deadline squeeze. Decide what the best response would have been. This turns the SJT into a review of your actual professional habits.
- **Talk scenarios through with your mentor.** Your test engineer or analyst colleagues have faced every one of these situations. Their reasoning — not just their answer — is the training data you want.
- **Stay calm about grey areas.** Some options are close together deliberately. Choose the one with the best combination of honesty, timeliness, and respect, and move on without agonising.

### Common pitfalls to avoid

- **Choosing deference over evidence.** "A senior person said so" never justifies recording false results or dropping a verified observation. Politeness and firmness are compatible.
- **Choosing silence over awkwardness.** Many weak options are quiet ones: not mentioning the defect, the mistake, the gap, the conflict. In testing, silence is rarely neutral — someone downstream inherits what you did not say.
- **Fixing things outside your remit.** Editing code, deleting data, or overriding priorities single-handedly usually scores poorly at associate level, even with good intentions. The strong pattern is act within remit, inform beyond it.
- **Public corrections and reply-all justice.** Options that embarrass a colleague in front of others almost never score well, even when you are factually right. Evidence goes in the record; conversations go to the person.
- **All-or-nothing reactions.** One flaky run does not condemn automation; one pushy request does not make a stakeholder an enemy. Measured, specific responses beat sweeping ones.
- **Forgetting the user.** Behind every scenario is a citizen trying to use a government service. When two options seem close, the one that better protects users — their data, their access, the honesty of what the team knows about quality — is nearly always the keyed answer.

## Conclusion

Well done — you have worked through a complete set of psychometric assessment practice materials built specifically around your role as an associate test engineer in the UK Government Digital and Data profession. That is no small thing, and you should feel genuinely encouraged by what you have just done.

Along the way, you have practised the four families of thinking that assessments — and your daily work — draw on. In the cognitive section, you spotted broken naming patterns, chained deployment rules, checked defect reports against checklists, and prioritised tasks the way a careful tester does. In the numeric section, you calculated pass rates, weighted averages, percentage changes, and effort estimates, always with the denominator-first, sense-check-last discipline that keeps reported numbers honest. In the verbal section, you held the line between true, false, and cannot say, read modal words like "must" and "may" with a tester's precision, and judged which sentences genuinely communicate to non-technical readers. And in the situational judgement section, you rehearsed the moments that shape a testing career: reporting defects promptly, correcting your own mistakes openly, declining improper requests politely, protecting citizens' data, and distrusting a green run that looked too good to be true.

Notice the thread running through all four sections: none of this was abstract. Every question used the artefacts and dilemmas of your real role — the test scripts you develop under supervision, the defects you raise awareness of and manage, the user stories you analyse with support, and the automated checks you help maintain. That is the point of job-specific assessment practice: the same habits that raise your scores raise the quality of your work. Careful reading makes better test analysis. Denominator discipline makes truthful progress reports. Escalation judgement makes you a teammate people trust.

Here is how to carry this forward. Revisit the sections where you hesitated most — a second pass a week later cements more than a single long session. Bring one or two questions to your test engineer or mentor and talk through the reasoning together; their perspective will deepen yours, and the conversation itself practises your communication skill. Keep using your own project's numbers and documents as free practice material. And when a real assessment arrives, remember what you know now: read the question twice, deduce only what is given, check the denominator, and when in doubt, choose honesty and timely escalation — in the test and in the job.

If you are preparing for a real assessment, find out the format, timing, and provider in advance, complete any official practice tests offered, and look after the basics — rest, a quiet space, and a steady pace on the day. And whatever the outcome, remember that no single test defines you: it is one snapshot of skills that you are actively growing every week.

You are at the beginning of a profession that government services genuinely depend on. Every carefully executed test, every precise defect report, and every good question you ask makes public services better for the people who use them. Keep practising, keep asking, and keep going — you are doing well, and you are on your way.
