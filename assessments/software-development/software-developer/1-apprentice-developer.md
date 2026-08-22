# Apprentice Developer - Psychometric Assessment Resources

## Introduction

Welcome! This guide has been written especially for you as an apprentice developer in the UK Government Digital and Data profession. You are at the very start of your journey as a software developer, and that is something to be proud of. You are learning on the job, attending certified training, shadowing more experienced developers, and pairing with colleagues to write code and tests. This guide will help you get ready for something you may not have met before: psychometric assessments.

So what is a psychometric assessment? It is a structured, standardised set of exercises that measures the thinking skills and workplace judgement that help people succeed in a role. Do not let the long word worry you. These assessments are not about trick questions or secret knowledge. They are about the everyday thinking you are already practising: spotting a pattern in code, following a rule step by step, checking a test result carefully, reading an email or a user story and understanding exactly what it says, and choosing a sensible next step when something goes wrong.

Why does this matter for you as an apprentice developer? Your role is built around learning. You spend a good portion of your time shadowing others, you work with other developers to write code and tests, you follow a test-driven approach, and you write code that is automatically tested. Employers use psychometric assessments to understand how you think and learn, because at your level, how you approach a problem matters more than how much you already know. Practising these assessments will also sharpen the exact skills your apprenticeship is building: careful reading, step-by-step reasoning, checking your work, and asking for help at the right time.

This document is organised into four main assessment sections:

1. A workplace job-specific cognitive assessment, which covers pattern recognition, logical thinking, error checking, prioritisation, and problem solving using developer materials like code naming rules, test results, and simple scripts.
2. A workplace job-specific numeric reasoning assessment, which uses the kinds of numbers you will genuinely meet: test pass rates, build times, story points, and simple service statistics.
3. A workplace job-specific verbal reasoning assessment, which checks how carefully you read things like coding standards, user stories, emails from your team, and short policy extracts.
4. A workplace job-specific situational judgement assessment, which presents realistic workplace situations for an apprentice — pairing, shadowing, making mistakes, asking questions — and asks what you would do.

Each section follows the same friendly pattern. First, you will read about what the assessment measures and how it is usually run. Next, you will see how the assessment maps to the named skills in your role, such as **Programming and build**, **User focus**, and **Service support**. Then come practice questions, starting easy and getting gradually harder, each with the correct answer and a full explanation. Finally, each section ends with preparation tips and common pitfalls to avoid.

Here is how to get the most from this guide. Take it slowly — one section at a time is plenty. Try each question honestly and write down your answer before you read the explanation. Read every explanation, even when you got the question right, because the explanations teach technique. And be kind to yourself: nobody expects an apprentice to get everything right first time. Every question you attempt is practice, and practice is exactly what your role is about.

Ready? Let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive assessment measures the thinking skills your job actually uses, through practical scenarios rather than abstract puzzles. Instead of asking you to rotate shapes in your head, it shows you the kinds of things an apprentice developer sees every day — naming conventions in code, sequences of test results, simple rules in a script, a list of tasks to sort — and asks you to reason about them quickly and carefully.

The typical format is an online, timed test lasting about 15 to 30 minutes. You will usually see somewhere between 15 and 30 questions covering pattern recognition, logical deduction, error checking, prioritisation, and applied problem solving. Scoring is objective: your answers are compared against a large group of other people who have taken the same test, called a norm group. Many modern platforms are adaptive, which means the questions get slightly harder when you answer correctly and slightly easier when you do not. Do not be alarmed if the test starts to feel difficult — that usually means you are doing well! Employers often see a breakdown of your speed and your accuracy, so it pays to work steadily and carefully rather than rushing. Almost every platform offers a few ungraded practice questions before the real test starts, so you can get used to the screen layout without any pressure.

Why do employers use this kind of assessment for an apprentice developer? Because your role is fundamentally about learning to think like a developer. Writing clean code that is automatically tested, following a test-driven approach, and helping to investigate service faults under direction all depend on the same core abilities: noticing patterns, following rules exactly, spotting small errors before they become big ones, and working out what to do first. A cognitive assessment simulates those demands in miniature, which makes it a fair and useful signal of how you will grow in the role.

### How this assessment maps to your role

Each dimension of the cognitive assessment connects directly to a named skill in your role summary:

- **Pattern recognition** maps to **Programming and build (software engineering)**. When you design, code, test, correct and document simple programs or scripts under the direction of others, you are constantly spotting patterns: how files are named, how functions are structured, how test cases repeat a shape. Recognising the pattern is how you learn to follow it.
- **Logical deduction** maps to **Modern development standards** and your duty to follow a test-driven approach. Standards and tests are rules. Deduction means working out correctly what a rule requires in a specific case — for example, what a failing test tells you, and what it does not tell you.
- **Error checking** maps to **Programming and build** and **Service support**. Correcting simple programs and helping with the investigation and fixing of service faults, completing defined activities under direction, both depend on spotting the small difference between what is written and what should be written.
- **Prioritisation** maps to your day-to-day working pattern of shadowing, pairing and building your knowledge. Even as an apprentice you must decide sensible orders for tasks: which item to raise with your pair first, which learning activity fits the time you have.
- **Problem solving** maps to **Prototyping** and **User focus**. Understanding why and when to prototype, and understanding the purpose of user stories, both involve breaking a fuzzy problem into steps — exactly what applied problem-solving questions practise.

### Practice questions

**Question 1 (easy) — Pattern recognition in file naming**

Your team's coding standard says test files are named after the file they test, with `_test` added before the file extension. You see these files in the repository:

1. `payments.py` and `payments_test.py`
2. `refunds.py` and `refunds_test.py`
3. `invoices.py` and `test_invoices.py`
4. `receipts.py` and `receipts_test.py`

Which pair breaks the naming pattern?

- A) Pair 1
- B) Pair 2
- C) Pair 3
- D) Pair 4

**Correct answer: C**

**Explanation:** The rule says `_test` is added before the extension, so the test file for `invoices.py` should be `invoices_test.py`. Pair 3 puts the word "test" at the front instead, which breaks the pattern even though it looks similar at a glance. Pairs 1, 2 and 4 all follow the rule exactly. This is a small thing, but it is exactly the kind of consistency your team relies on: automated tools often find test files by their names, so a wrongly named file might silently never run. As an apprentice, noticing naming patterns like this — and asking your pair when something looks different — is a genuinely valuable habit.

**Question 2 (easy) — Logical deduction from a test result**

You are pair programming. Your pair writes a test first, following your team's test-driven approach. The test checks that the function `add_vat` returns 120 when given 100. You run the test suite and the `add_vat` test fails. Which one of the following must be true?

- A) The function `add_vat` contains a bug.
- B) The test contains a bug.
- C) Either the function or the test does not currently behave as intended.
- D) The whole test suite is broken.

**Correct answer: C**

**Explanation:** A failing test tells you there is a mismatch between the test's expectation and the function's behaviour — but it does not tell you which side is wrong. Maybe the function has a bug (A), or maybe the test asserts the wrong value (B). Either is possible, so neither must be true on its own. D goes far beyond the evidence: one failing test says nothing about the rest of the suite. The only statement guaranteed by the facts is C. This careful thinking is the heart of the test-driven approach you follow: when a test fails, you investigate both sides before changing anything. Assessments reward the same discipline — conclude only what the information guarantees.

**Question 3 (easy) — Error checking a simple script**

Your mentor asks you to check a short script before it is committed. The team standard says every function must have a one-line comment above it describing what it does. The script contains four functions:

1. `load_data` — has a comment above it
2. `clean_data` — has a comment above it
3. `save_data` — has a comment two lines below it
4. `print_summary` — has a comment above it

How many functions breach the standard?

- A) 0
- B) 1
- C) 2
- D) 3

**Correct answer: B**

**Explanation:** Check each function against the rule, one at a time. Functions 1, 2 and 4 each have a comment above them, so they comply. Function 3 has a comment, but it is below the function, not above it — so it breaches the standard as written. That makes exactly one breach. The trap in questions like this is to think "well, it has a comment somewhere, that's probably fine". Assessments — and code reviews — reward reading the rule precisely and applying it exactly. When you document simple programs under the direction of others, following the documentation standard exactly is what makes your work easy for the next developer to read.

**Question 4 (easy) — Prioritisation of a morning's tasks**

It is 9:30 on Tuesday. You have four things on your list:

1. Your pairing session with a senior developer starts at 10:00 and you need to re-read yesterday's code beforehand.
2. Your apprenticeship training portfolio entry is due on Friday.
3. A teammate posted a message asking if anyone can help test a small fix "sometime today".
4. You want to read a tutorial about a testing library, with no deadline.

What is the most sensible order to deal with these?

- A) 2, 1, 3, 4
- B) 1, 3, 2, 4
- C) 4, 1, 2, 3
- D) 3, 4, 1, 2

**Correct answer: B**

**Explanation:** Item 1 is both urgent (the session starts in 30 minutes) and important (pairing is the core of how you learn and contribute), so it comes first. Item 3 has a same-day timeframe and helps a teammate, so it comes next. Item 2 matters but is due Friday, so it can be planned for later. Item 4 is valuable learning with no deadline, so it fits into remaining time. Option A puts a Friday deadline ahead of a 10:00 commitment; C starts with the only task that has no deadline at all; D leaves your pairing preparation until after two less urgent items. The pattern to remember: order tasks by urgency and importance together, not by whichever appeared first or sounds most interesting.

**Question 5 (moderate) — Pattern recognition in test output**

Your team's build runs the test suite every time code is pushed. Over the last six pushes, the number of failing tests was: 0, 0, 1, 0, 2, 4. All the new failures are in the payments module, which your team began changing three pushes ago. What is the most reasonable reading of this pattern?

- A) The test framework has stopped working properly.
- B) The recent changes to the payments module are probably introducing failures, and the trend is getting worse.
- C) Four failures out of a large suite is normal, so nothing needs attention.
- D) The failures are random and will probably go away on their own.

**Correct answer: B**

**Explanation:** Look at the shape of the data before jumping to a cause. Failures were rare (0, 0, 1, 0), then rose to 2 and then 4 — an upward trend that began when the payments work started, and the failures are located in the payments module. That is a strong pattern linking the changes to the failures. Option A has no supporting evidence — the framework is running and reporting. Option C ignores the trend: it is not the number 4 that matters, it is the direction of travel. Option D is wishful thinking; test failures almost never fix themselves. In your role, you write code that is automatically tested precisely so that patterns like this appear early. Spotting the trend and mentioning it to your pair or mentor is exactly the right apprentice behaviour.

**Question 6 (moderate) — Logical deduction from a deployment rule**

Your team has a rule: "Code may be merged only if the build is green and at least one other developer has approved the review." Your change has one approval from a senior developer, and the build is currently red because of a failing test in your change. Which conclusion must be true?

- A) Your change may be merged, because it has an approval.
- B) Your change may not be merged at the moment.
- C) Your approval does not count because the build is red.
- D) You must find a second approver.

**Correct answer: B**

**Explanation:** The rule has two conditions joined by "and": green build AND at least one approval. You have the approval, but the build is red, so one condition fails — and when an "and" rule has any failed condition, the whole rule is not satisfied. So the change may not be merged right now, which is exactly what B says. A ignores the build condition. C invents a consequence the rule never states — the approval remains valid; it is simply not enough on its own. D also invents a requirement: the rule asks for at least one approver, and you have one. Rules in development standards are often written this way, with multiple conditions, and reading them precisely is part of your **Modern development standards** skill: understanding why the standard exists (protecting the main branch) helps you remember how it works.

**Question 7 (moderate) — Error checking data against a rule**

You are helping investigate a service fault under direction. Your mentor asks you to check a configuration list against the rule: "Every environment name must be lowercase, and test environments must end in `-test`." The list reads:

1. `production`
2. `staging`
3. `Payments-Test`
4. `integration-test`

Which entries breach the rule?

- A) Entry 3 only
- B) Entries 3 and 4
- C) Entry 4 only
- D) Entries 2 and 3

**Correct answer: A**

**Explanation:** Take each entry in turn. Entry 1, `production`, is lowercase and is not a test environment, so it is fine. Entry 2, `staging`, likewise. Entry 3, `Payments-Test`, contains capital letters, which breaches the lowercase rule — note that it does end in a form of `-test`, but the capitalisation alone is enough to make it a breach. Entry 4, `integration-test`, is lowercase and ends in `-test`, so it complies fully. So the answer is entry 3 only. Configuration checking like this is a real part of **Service support**: faults are often caused by a tiny mismatch, such as a capital letter, that a computer treats as completely different. When you complete defined checking activities under direction, being slow and exact beats being fast and approximate.

**Question 8 (moderate) — Problem solving with a step-by-step process**

Your team's process for fixing a bug is: (1) reproduce the bug with a failing test; (2) fix the code until the test passes; (3) run the whole suite; (4) ask for review. You have been given a simple bug to fix under supervision. You wrote a test, but it passes immediately, before you have changed any code. What is the most sensible next step?

- A) Move on to step 2 and start changing the code anyway.
- B) Delete the test and skip straight to fixing the code.
- C) Pause and check your test — it may not actually be reproducing the bug.
- D) Mark the bug as fixed, since the test passes.

**Correct answer: C**

**Explanation:** In a test-driven approach, the first test should fail, because it describes behaviour that is currently broken. A test that passes straight away has not captured the bug: perhaps it tests the wrong function, uses the wrong input, or asserts the wrong expectation. Option A means changing code without a safety net that proves the bug existed. Option B throws away the team's process. Option D confuses "my test passes" with "the bug is gone" — the bug was reported by someone who saw it, so a passing test more likely means the test is wrong. Option C follows the logic of the process: each step exists for a reason, and when a step gives a surprising result, you stop and understand it before continuing. Raising this with your supervisor is not failure — it is exactly how apprentices are expected to work.

**Question 9 (moderate) — Prioritisation during a service fault**

You are shadowing a developer during a live service incident. She is busy investigating and asks you to do three things: (1) note down the times of the error messages appearing in the log; (2) find the phone number of the on-call database administrator "in case we need it"; (3) fetch the runbook document for this service. She says the runbook is what she needs first. A minute later, a teammate messages you asking about lunch plans. What order do you act in?

- A) Runbook, error times, phone number; ignore lunch until later.
- B) Lunch reply, runbook, phone number, error times.
- C) Error times, phone number, runbook; quick lunch reply in between.
- D) Phone number, runbook, error times; ignore lunch until later.

**Correct answer: A**

**Explanation:** The developer told you directly what she needs first: the runbook. During an incident, the person leading the investigation sets the priorities, and your job under direction is to follow them. The error times come next because they are time-sensitive evidence for the ongoing investigation, and the phone number is a "just in case" item, useful but not blocking anyone. The lunch message is a genuine part of work life, but during a live incident it waits. Options B and C reorder the leader's stated priority, and D puts the contingency item first. This maps straight to your **Service support** skill — helping with the investigation of service faults by completing defined activities under direction — and shows that good prioritisation sometimes just means listening carefully to what you have been asked to do.

**Question 10 (hard) — Multi-step deduction about a build pipeline**

Your team's pipeline runs in strict order: unit tests, then integration tests, then deployment to the test environment. The rules are: (i) if unit tests fail, integration tests do not run; (ii) if integration tests fail, deployment does not happen; (iii) deployment always happens if integration tests pass. This morning, deployment to the test environment did not happen. Which one of the following must be true?

- A) The unit tests failed.
- B) The integration tests failed.
- C) The integration tests did not pass.
- D) The unit tests passed but the integration tests failed.

**Correct answer: C**

**Explanation:** Work backwards from what you know. Rule (iii) says deployment always follows passing integration tests. Deployment did not happen, so the integration tests cannot have passed — that is answer C. But be careful: "did not pass" is not the same as "failed". There are two ways integration tests can fail to pass: they ran and failed, or they never ran at all because the unit tests failed first (rule (i)). Option A might be true but is not guaranteed — the integration tests could have run and failed. Option B might be true but is not guaranteed either — they might never have run. Option D is just one of the possible stories. Only C covers every possibility. This kind of backwards reasoning is exactly how developers read a pipeline dashboard: the absence of a deployment tells you where to start looking, not precisely what went wrong.

**Question 11 (hard) — Applying several rules at once**

Your team's definition of done for a story says: (i) code is written and reviewed; (ii) automated tests are written and passing; (iii) documentation is updated if behaviour changed; (iv) the product owner has seen a demo. You and your pair finished a story that changed how error messages appear to users. The code is reviewed, all tests pass, and the product owner watched a demo yesterday. Your pair says the story is done. Is your pair right?

- A) Yes — everything on the list has been completed.
- B) No — the documentation must be checked, because user-facing behaviour changed.
- C) No — the demo happened yesterday, and demos must happen on the day of completion.
- D) Yes — documentation only matters for major changes.

**Correct answer: B**

**Explanation:** Go through the four conditions like a checklist. (i) Code written and reviewed — yes. (ii) Tests written and passing — yes. (iv) Product owner saw a demo — yes; the rule says nothing about when, so option C invents a condition that does not exist. That leaves (iii): documentation must be updated if behaviour changed. The story changed how error messages appear to users, which is a behaviour change, so the documentation condition is triggered — and nothing in the scenario says it was done. Option D invents a "major changes only" exception that the rule does not contain. So the story is not done yet, for exactly the reason B gives. This is applied rule-following, the everyday skill behind **Modern development standards**: neither adding conditions that are not there, nor skipping ones that are.

**Question 12 (hard) — Problem solving with incomplete information**

You are writing a simple script under direction that reads a list of user records and counts how many have no email address. Your first run reports 0 records with missing emails, but your mentor says she is certain some records have missing emails. You check and see the file has 5,000 records, your script read 5,000 records, and your script counts a record as missing an email when the email field equals the text "missing". What is the most likely explanation to investigate first?

- A) The file actually has no missing emails and your mentor is wrong.
- B) Records with missing emails may store something other than the word "missing" — for example an empty field — so your check never matches.
- C) The script is reading the wrong file.
- D) The counting logic can never work in this language.

**Correct answer: B**

**Explanation:** Line up the evidence. The script read all 5,000 records, so C is unlikely — the volume matches the expected file. D is not a real explanation; counting works in every mainstream language. A is possible but should not be your first assumption when an experienced colleague is certain and your script contains an obvious fragile assumption. That assumption is the definition of "missing": your script only counts records where the field literally says "missing", but real data usually represents absence as an empty field, a blank space, or a null value. So the first thing to investigate is what missing emails actually look like in this file — B. The general technique is powerful: when a program's answer conflicts with a trusted human's expectation, check the program's assumptions about the data before anything else. It will serve you throughout your career in **Programming and build**.

### Preparation tips

- **Practise little and often.** Ten or fifteen minutes of practice questions a few times a week builds skill far better than one long cramming session. This mirrors how your apprenticeship works: steady, repeated practice.
- **Read the rule twice, then answer.** Most cognitive questions at your level are about applying a stated rule exactly. Reading the rule a second time takes five seconds and prevents most wrong answers.
- **Say the reasoning in your head.** When you practise, explain to yourself why the answer is right, as if you were talking to your pair. If you cannot explain it, you have not fully understood it — and the explanation sections in this guide show you what a full reasoning walkthrough sounds like.
- **Use your everyday work as practice.** Every code review you shadow, every test failure you investigate, and every naming convention you follow is cognitive assessment practice in disguise. Notice patterns on purpose.
- **Get comfortable with timers.** Do some practice with a gentle time limit so the countdown on the real test feels familiar rather than frightening. Speed comes from calm familiarity, not rushing.
- **Sleep and setup matter.** Take the real assessment rested, in a quiet place, on a reliable connection, with any adjustments you are entitled to arranged in advance. Ask your employer or the test provider about adjustments early — this is normal and encouraged.

### Common pitfalls to avoid

- **Answering from general knowledge instead of the question.** The question tells you the rule; use that rule, even if your team at work does things differently. Assessments test reading and reasoning, not memory of your own workplace.
- **Choosing the answer that goes beyond the evidence.** Options that say "must be true" require certainty. If you can imagine any situation where the option is false, it is not the answer. Question 10 above is a classic example.
- **Rushing the easy questions.** Easy questions are where careless mistakes cost you most, because you were capable of getting them right. Slow down for ten seconds; check the exact wording.
- **Panicking when questions get harder.** On adaptive tests, harder questions usually mean you are doing well. Treat difficulty as a good sign and keep working steadily.
- **Getting stuck on one question.** If a question is eating your time, make your best sensible choice and move on. One question rarely matters; running out of time always does.
- **Assuming a passing test means everything is fine.** Several questions above turn on this: a green result only means the check you wrote passed. Always ask what the check actually checks — in tests and in life.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment measures how confidently and accurately you work with numbers in the situations your job actually produces. This is not a maths exam. There is no algebra for its own sake, no formulae to memorise beyond everyday percentages, ratios, and averages. Instead, you are shown small tables and short descriptions of numbers — test results, build times, story counts, simple service statistics — and asked questions that check whether you can read them correctly and reason with them.

The typical format is an online, timed test of about 20 to 30 minutes, with somewhere between 15 and 25 questions. Most questions show you a small table or chart, then ask something specific: a percentage, a difference, an average, a rate, or a trend. Calculators are usually allowed — the test measures reasoning, not mental arithmetic speed — but check the instructions for your specific test. As with the cognitive assessment, scoring compares you with a norm group, and platforms may adapt the difficulty as you go. Accuracy generally matters more than raw speed: a steady, careful pace with correct answers scores better than a rush with mistakes.

Why do employers assess numeric reasoning for an apprentice developer? Because software development is quietly full of numbers. Test suites report pass rates. Builds have durations. Sprints have story counts. Services have availability percentages and error rates — and your **Availability and capacity management** skill asks you to explain exactly those processes. When you help investigate a service fault, someone will show you a graph and ask what you see. When your team talks about whether the sprint is on track, they are doing arithmetic out loud. Being comfortable with these small, practical calculations lets you follow those conversations, contribute to them, and check your own work.

One more reassurance: at apprentice level, the numbers in these tests are deliberately manageable. The skill being tested is care — reading the right row, using the right total, noticing the units — not speed-sums. Every question below shows its arithmetic step by step, so you can follow along and check your own method.

### How this assessment maps to your role

- **Percentages and rates** map to **Availability and capacity management**: explaining availability processes means understanding statements like "the service was available 99.5% of the time this month" and what that means in hours and minutes.
- **Reading tables** maps to **Programming and build (software engineering)** and **Service support**: test reports, build dashboards, and fault logs are all tables. Helping to investigate faults under direction often starts with reading numbers out of a monitoring screen correctly.
- **Averages and trends** map to your duty to build your knowledge and work with other developers: sprint reviews and retrospectives are full of averages (how many stories per sprint?) and trends (are builds getting slower?). Following those discussions is part of joining the team's conversation.
- **Simple proportions and ratios** map to **User focus**: user research findings often arrive as proportions — "6 out of 10 participants struggled with this screen" — and understanding user experience analysis means understanding what those figures do and do not tell you.
- **Checking calculations** maps to your test-driven approach: a test is just a calculation checked against an expectation. The habit of verifying "does this number make sense?" is the same habit as writing an assertion.

### Practice questions

**Question 1 (easy) — Percentage of passing tests**

Your team's test suite has 200 tests. This morning's run shows 190 tests passing and 10 failing. What percentage of the tests passed?

- A) 90%
- B) 95%
- C) 92.5%
- D) 98%

**Correct answer: B**

**Explanation:** Work step by step. The fraction of passing tests is the number passing divided by the total: 190 ÷ 200. To turn a fraction into a percentage, multiply by 100: (190 ÷ 200) × 100 = 0.95 × 100 = 95%. A quick sense-check: 10 failures out of 200 is 10 ÷ 200 = 5% failing, and 100% − 5% = 95% passing — the two routes agree, which is a good sign you are right. Option A (90%) would be the pass rate if 20 tests had failed; option C mixes up the arithmetic; option D would mean only 4 failures. Checking a result by a second route, as we did here, is a habit worth building — it is the numeric version of writing a test for your code.

**Question 2 (easy) — Reading a build dashboard table**

The build dashboard shows this week's builds:

| Day | Builds run | Builds failed |
|---|---|---|
| Monday | 8 | 1 |
| Tuesday | 10 | 0 |
| Wednesday | 12 | 3 |
| Thursday | 10 | 2 |

On which day did the largest number of builds succeed?

- A) Monday
- B) Tuesday
- C) Wednesday
- D) Thursday

**Correct answer: B**

**Explanation:** The table shows builds run and builds failed, but the question asks about builds that succeeded — so you need one small calculation per row: successes = runs − failures. Monday: 8 − 1 = 7. Tuesday: 10 − 0 = 10. Wednesday: 12 − 3 = 9. Thursday: 10 − 2 = 8. The largest is Tuesday with 10. The trap here is Wednesday: it has the most builds run (12), and if you answer from the "Builds run" column you will pick C. Table questions very often work like this: the answer is one step away from the columns shown. Always pause and ask, "which quantity is the question actually asking about?" — the same care you apply when reading a monitoring dashboard during service support.

**Question 3 (easy) — Simple average of story counts**

Over the last four sprints, your team completed 6, 8, 7, and 9 stories. What is the average (mean) number of stories completed per sprint?

- A) 7
- B) 7.5
- C) 8
- D) 30

**Correct answer: B**

**Explanation:** The mean is the total divided by the number of sprints. Step 1: add the values: 6 + 8 = 14; 14 + 7 = 21; 21 + 9 = 30. Step 2: divide by the number of sprints, which is 4: 30 ÷ 4 = 7.5. So the average is 7.5 stories per sprint — and yes, an average can be a "half story" even though no sprint delivered half a story; averages describe the group, not any single sprint. Option D (30) is the total, not the average — a very common slip when rushing. Sense-check: the average must sit between the smallest value (6) and the largest (9), and 7.5 does. Your team uses this exact number in sprint planning to predict how much work fits in the next sprint, so this little calculation is genuinely part of team life.

**Question 4 (easy) — Proportion in user research**

A user researcher tells your team that 12 of the 40 participants in a usability study could not complete the sign-in step. What proportion of participants is that?

- A) 25%
- B) 30%
- C) 33%
- D) 40%

**Correct answer: B**

**Explanation:** The proportion is 12 ÷ 40. Step 1: 12 ÷ 40 = 0.3. Step 2: multiply by 100 to get a percentage: 0.3 × 100 = 30%. A neat mental shortcut: 40 × 10% = 4 participants, so 12 participants is 12 ÷ 4 = 3 lots of 10%, which is 30%. Option A would be 10 of 40; option C is roughly a third (13.3 of 40); option D confuses the total (40) with the answer. Understanding figures like this supports your **User focus** skill: "30% of participants failed to sign in" is a strong signal about user needs, and when your team discusses the finding, you can follow exactly what the number means — nearly one in three real people hitting a wall.

**Question 5 (moderate) — Availability percentage to hours**

Your mentor is explaining availability. A service has a target of 99% availability over a 30-day month. Roughly how much downtime does that target allow in the month? (Use 30 days × 24 hours = 720 hours.)

- A) About 72 minutes
- B) About 7.2 hours
- C) About 1.4 hours
- D) About 14.4 hours

**Correct answer: B**

**Explanation:** Step 1: find the allowed downtime percentage: 100% − 99% = 1%. Step 2: find the total hours in the month: 30 × 24 = 720 hours. Step 3: take 1% of 720: 720 × 0.01 = 7.2 hours. So a 99% target allows about 7.2 hours of downtime a month — often a surprise to people, who expect 99% to mean "almost never down". Option A (72 minutes) is 1% of 5 days, or a factor-of-ten slip; option C would be roughly the allowance for a 99.8% target; option D is 2%. This is the core arithmetic of your **Availability and capacity management** skill: availability targets sound abstract until you convert them into hours, and being able to do that conversion is exactly what "explain availability management processes" looks like in practice.

**Question 6 (moderate) — Percentage change in build time**

Last month, the average build took 8 minutes. After the team added more tests, the average build now takes 10 minutes. What is the percentage increase in build time?

- A) 2%
- B) 20%
- C) 25%
- D) 80%

**Correct answer: C**

**Explanation:** Percentage change is always calculated relative to the original value. Step 1: find the change: 10 − 8 = 2 minutes. Step 2: divide the change by the original value: 2 ÷ 8 = 0.25. Step 3: multiply by 100: 25%. The most tempting wrong answer is B (20%), which you get if you divide the change by the new value (2 ÷ 10) — a very common error. Remember: "increase from" the old number means the old number is the base. Option A confuses the raw change (2 minutes) with a percentage; option D is 8 ÷ 10 and does not correspond to anything meaningful here. Teams watch build-time trends because slow builds slow everyone's feedback loop — a 25% increase is the kind of figure a team might discuss at a retrospective, and now you can calculate it yourself.

**Question 7 (moderate) — Error rate per thousand requests**

During a fault investigation you are asked to note error counts. In one hour, a service handled 24,000 requests and returned 60 errors. What is the error rate per 1,000 requests?

- A) 0.25 errors per 1,000
- B) 2.5 errors per 1,000
- C) 25 errors per 1,000
- D) 4 errors per 1,000

**Correct answer: B**

**Explanation:** A rate "per 1,000" asks: if we split the requests into groups of 1,000, how many errors happen in each group on average? Step 1: find how many groups of 1,000 there are: 24,000 ÷ 1,000 = 24 groups. Step 2: share the 60 errors across the 24 groups: 60 ÷ 24 = 2.5. So the rate is 2.5 errors per 1,000 requests. Options A and C are factor-of-ten slips on either side — always worth a sense-check: 2.5 per 1,000 across 24 thousand-groups gives 2.5 × 24 = 60 errors, matching the data. Option D comes from dividing the wrong way around. Rates like this matter in **Service support** because raw error counts are misleading: 60 errors is terrible in 100 requests but tiny in 24,000. Converting to a rate makes numbers comparable across busy and quiet hours.

**Question 8 (moderate) — Reading a two-way table**

Your team logs support tickets by type and priority:

| | High priority | Low priority | Total |
|---|---|---|---|
| Bug | 6 | 14 | 20 |
| Question | 2 | 18 | 20 |
| Total | 8 | 32 | 40 |

What percentage of high-priority tickets are bugs?

- A) 15%
- B) 30%
- C) 60%
- D) 75%

**Correct answer: D**

**Explanation:** The question asks about high-priority tickets only, so the base for the percentage is the high-priority column total: 8 tickets. Of those, 6 are bugs. Step 1: 6 ÷ 8 = 0.75. Step 2: × 100 = 75%. The classic mistake is using the wrong base. Option A (15%) is 6 ÷ 40 — bugs that are high priority as a share of all tickets. Option B (30%) is 6 ÷ 20 — high-priority tickets as a share of bugs, which answers a different question ("what percentage of bugs are high priority?"). Two-way tables are everywhere in service work, and the golden rule is: the words after "of" in the question tell you the base. "Percentage of high-priority tickets" means divide by the high-priority total. Read the question, find the base, then divide.

**Question 9 (moderate) — Time arithmetic for a maintenance window**

A planned maintenance task must run three scripts one after another. Script A takes 25 minutes, script B takes 40 minutes, and script C takes 55 minutes. The maintenance window starts at 22:00 and ends at 24:00 (midnight). Will the scripts finish inside the window, and with how much time to spare or overrun?

- A) Yes, with 20 minutes to spare
- B) Yes, with exactly 0 minutes to spare
- C) No, overrunning by 10 minutes
- D) No, overrunning by 20 minutes

**Correct answer: B**

**Explanation:** Step 1: total the script times: 25 + 40 = 65; 65 + 55 = 120 minutes. Step 2: find the window length: from 22:00 to 24:00 is 2 hours = 120 minutes. Step 3: compare: 120 minutes of work in a 120-minute window finishes exactly at midnight, with zero minutes to spare. So the answer is B — it fits, but only just. In real service support, "exactly fits" is a warning sign: any small delay causes an overrun, so a team would normally want buffer time and might trim the plan or extend the window. Options A, C and D all come from small addition or window-length slips, which is why writing the arithmetic down (rather than juggling it in your head) is the professional habit: during real maintenance tasks, checked arithmetic protects live services.

**Question 10 (hard) — Combining pass rates from two suites**

Your project has two test suites. The unit suite has 300 tests with a 96% pass rate. The integration suite has 100 tests with an 88% pass rate. What is the overall pass rate across all 400 tests?

- A) 92%
- B) 94%
- C) 95%
- D) 96%

**Correct answer: B**

**Explanation:** You cannot just average 96% and 88% to get 92%, because the suites are different sizes — the unit suite has three times as many tests, so it counts three times as much. Work with actual test counts. Step 1: passing unit tests: 300 × 0.96 = 288. Step 2: passing integration tests: 100 × 0.88 = 88. Step 3: total passing: 288 + 88 = 376. Step 4: overall rate: 376 ÷ 400 = 0.94 = 94%. Option A (92%) is the simple average trap — the most common wrong answer on questions like this. Sense-check: the overall rate must sit between 88% and 96%, and closer to 96% because the bigger suite pulls the average toward itself; 94% fits that perfectly. This "weighted average" idea appears whenever you combine groups of different sizes — pass rates, error rates, survey results — so it is well worth the practice.

**Question 11 (hard) — Trend and projection from a table**

The number of automated tests in your project has grown like this:

| Month | Tests |
|---|---|
| January | 120 |
| February | 150 |
| March | 180 |
| April | 210 |

If the trend continues at the same steady rate, how many tests will there be in July?

- A) 240
- B) 270
- C) 300
- D) 330

**Correct answer: C**

**Explanation:** Step 1: find the pattern. From January to February: 150 − 120 = 30. February to March: 180 − 150 = 30. March to April: 210 − 180 = 30. The suite grows by a steady 30 tests per month. Step 2: count the months from April to July: May, June, July — that is 3 more months. Step 3: project: 210 + (3 × 30) = 210 + 90 = 300. The classic slip is miscounting the months: April to July is 3 steps, not 4 (option D adds one step too many) and not 1 (option A). Writing the months out — May 240, June 270, July 300 — takes ten seconds and removes the doubt. Projections like this help teams plan: a suite growing by 30 tests a month will need more build capacity eventually, which is exactly the thinking behind **Availability and capacity management**.

**Question 12 (hard) — Ratio and sharing work fairly**

Your team is planning a bug-fixing day. There are 36 small bugs to share between three pairs of developers. Because of other commitments, the pairs agree to share the bugs in the ratio 2 : 3 : 4 (Pair X : Pair Y : Pair Z). How many bugs does Pair Y take?

- A) 8
- B) 12
- C) 16
- D) 18

**Correct answer: B**

**Explanation:** A ratio shares a total in proportion. Step 1: add the ratio parts: 2 + 3 + 4 = 9 parts in total. Step 2: find the size of one part: 36 ÷ 9 = 4 bugs per part. Step 3: Pair Y has 3 parts: 3 × 4 = 12 bugs. Check the whole distribution: Pair X gets 2 × 4 = 8, Pair Y gets 12, Pair Z gets 4 × 4 = 16; and 8 + 12 + 16 = 36, matching the total — a full check that costs seconds. Option A is Pair X's share, option C is Pair Z's share, and option D would be half the total, which no pair receives. Ratio-sharing appears in real planning whenever capacity differs between people or teams, and the method never changes: total the parts, size one part, multiply.

### Preparation tips

- **Slow down and write the steps.** Every explanation above shows the arithmetic in numbered steps. Copy that habit in practice and in the real test: write "change ÷ original × 100" before you touch the calculator. Method first, buttons second.
- **Learn the three big patterns.** Most workplace numeric questions are one of: a percentage (part ÷ whole × 100), a percentage change (change ÷ original × 100), or an average (total ÷ count). If you are secure on those three, you can handle most of any test.
- **Always find the base.** When a question says "percentage of X", the X is what you divide by. Underline it (mentally or on paper) before calculating.
- **Sense-check every answer.** Averages must sit between the smallest and largest values. Combined rates must sit between the two group rates. Downtime hours should feel roughly right. A ten-second sense-check catches most slips.
- **Practise with your team's real numbers.** Look at your build dashboard, test reports, or sprint board and ask yourself small questions: what is our pass rate? How has build time changed? This makes practice free and directly useful.
- **Check the calculator policy.** Most workplace tests allow calculators, but confirm it for yours, and practise the way you will be tested.

### Common pitfalls to avoid

- **Averaging percentages from different-sized groups.** As Question 10 showed, a 96% rate on 300 tests and an 88% rate on 100 tests do not average to 92%. Go back to real counts when groups differ in size.
- **Using the new value as the base for percentage change.** "Increased from 8 to 10" is measured against 8, not 10. This single habit fixes one of the most common errors in numeric tests.
- **Answering from the wrong column or row.** Question 2's trap — most builds run is not most builds succeeded — is typical. Match the question's exact words to the table before calculating.
- **Factor-of-ten slips.** Rates per 100, per 1,000, and percentages are easy to muddle. Write the units next to your answer ("2.5 errors per 1,000") and check they match what was asked.
- **Miscounting time steps.** April to July is three months of growth, not four. Listing the steps out is quicker than being wrong.
- **Rushing because it "looks easy".** Easy questions with small numbers are exactly where careless mistakes happen. Steady care beats speed, in tests and in maintenance windows alike.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment measures how accurately you read, understand, and reason about written material of the kind your job actually produces. For an apprentice developer, that means coding standards, user stories, team emails, short policy extracts, runbook instructions, and documentation. The test is not about vocabulary or literature; it is about careful, precise reading — the difference between what a text actually says and what you assume it says.

The typical format is an online, timed test of about 15 to 25 minutes. You are given short passages, each followed by one or more statements or questions. The most common question type asks you to judge a statement as **True** (the passage says or logically guarantees it), **False** (the passage contradicts it), or **Cannot say** (the passage gives too little information to decide either way). Other question types ask you to pick the best summary, identify what a writer is asking for, or choose the clearest rewrite of a sentence. Scoring is objective against a norm group, and — as with the other assessments — steady accuracy beats hurried speed.

Why does this matter for an apprentice developer? Because almost everything you learn arrives as text. Your certified training materials, your team's development standards, the user stories you help deliver, the pull request comments you read while shadowing, and the runbooks you follow during service support are all written documents. Misreading a single word — "must" versus "should", "before" versus "after", "any" versus "all" — can send a whole task in the wrong direction. The verbal reasoning assessment checks, and practising it strengthens, exactly this precision. It also builds a habit that will protect you for your whole career: when the text and your memory of the text disagree, trust the text, and re-read it.

A special note about "Cannot say": this option feels uncomfortable at first, because in everyday life we happily fill gaps with sensible guesses. In this test, sensible guessing is exactly what you must not do. If the passage does not state or guarantee the statement, the answer is "Cannot say" — even when the statement is probably true in real life.

### How this assessment maps to your role

- **Reading comprehension of standards** maps to **Modern development standards**: your skill outcome is literally to explain the importance of using modern development standards, and explaining something well starts with reading it precisely.
- **Understanding user stories** maps to **User focus**: you are asked to explain the purpose of user stories and the focus on user needs. Verbal reasoning questions about what a story does and does not commit the team to are direct practice for that.
- **Following written instructions** maps to **Service support** and **Programming and build**: completing defined activities under direction often means following a runbook or a task description exactly as written, including its conditions and exceptions.
- **Distinguishing stated facts from inference** maps to **Information security**: security guidance is full of precise conditions ("credentials must never be stored in the repository"), and explaining security controls accurately requires reporting what the guidance says, not a half-remembered version of it.
- **Clear-writing judgement** maps to your duty to document simple programs: choosing the clearest sentence in a test is the same skill as writing a commit message or comment that the next developer can understand first time.

### Practice questions

**Question 1 (easy) — True/False/Cannot say on a coding standard**

Passage: "All new code must be accompanied by automated tests. Code reviews are carried out by at least one other developer before merging. Documentation should be updated when behaviour visible to users changes."

Statement: "New code must be reviewed by at least one other developer before it is merged."

- A) True
- B) False
- C) Cannot say
- D) True, but only for user-visible changes

**Correct answer: A**

**Explanation:** Find the sentence that covers the statement. The passage says "Code reviews are carried out by at least one other developer before merging." The statement says the same thing in slightly different words: review by at least one other developer, before merging. Different wording, same meaning — so the statement is True. Option D invents a limitation from the documentation sentence, but that sentence is about documentation, not reviews; mixing up which sentence governs which rule is a common slip. The technique to practise: match the statement to the exact sentence in the passage that addresses it, then compare meanings word by word. As an apprentice, you will read standards like this in your first weeks — and being able to say precisely what they require is your **Modern development standards** skill in action.

**Question 2 (easy) — Understanding a user story**

Passage: "As a benefit claimant, I want to save my application part-way through, so that I can finish it later without starting again."

Statement: "This user story explains why the feature is wanted, from the user's point of view."

- A) True
- B) False
- C) Cannot say
- D) True, but user stories never mention users

**Correct answer: A**

**Explanation:** A user story has three parts: who ("As a benefit claimant"), what ("I want to save my application part-way through"), and why ("so that I can finish it later without starting again"). The statement claims the story explains why the feature is wanted from the user's point of view — and the "so that" clause does exactly that, and the whole story is written in the user's voice. So the statement is True. Option D contradicts itself: this story clearly names a user. This maps directly to your **User focus** skill outcome — explaining the purpose of user stories. The purpose is precisely this: keeping the team focused on a real person's need, not just a feature description. When you deliver work with your pair, re-reading the "so that" clause tells you what success actually means.

**Question 3 (easy) — Cannot-say discipline with an email**

Passage (email from your delivery manager): "Hi all — the show-and-tell moves from Thursday to Friday at 14:00 this week only. Same video link as usual. Please update your calendars."

Statement: "The show-and-tell will be held on Friday at 14:00 every week from now on."

- A) True
- B) False
- C) Cannot say
- D) True, because the time is stated clearly

**Correct answer: B**

**Explanation:** Read the email's exact words: the move to Friday applies "this week only". The statement claims the change is permanent ("every week from now on"), which directly contradicts "this week only" — so the statement is False, not merely unsupported. This is a useful contrast with Cannot say: if the email had not included "this week only", we would have had no information about future weeks and the answer would have been C. Because the email explicitly limits the change, we can positively say the statement is wrong. Option D confuses clarity about the time with truth about the frequency. Careful reading of small workplace messages avoids very real mistakes — like joining a meeting a day late — and the must-read-every-word habit is the same one that makes you good at reading error messages.

**Question 4 (easy) — What is being asked of you**

Passage (message from a senior developer): "When you get a chance today, could you run the linter on the reporting module and note any warnings in the ticket? Don't fix anything yet — we'll go through the warnings together tomorrow."

Which action matches the request?

- A) Fix all the linter warnings in the reporting module today.
- B) Run the linter, record the warnings in the ticket, and wait.
- C) Go through the warnings with the senior developer today.
- D) Run the linter on every module and fix the errors.

**Correct answer: B**

**Explanation:** Break the message into its instructions: (1) run the linter on the reporting module — today, when you get a chance; (2) note any warnings in the ticket; (3) explicitly do not fix anything yet; (4) the joint review happens tomorrow. Option B matches all four elements. Option A does the very thing the message forbids ("Don't fix anything yet"). Option C moves tomorrow's activity to today. Option D expands the scope from one module to every module and adds fixing. Instruction-following questions test whether you notice both the scope (which module) and the boundaries (don't fix yet) of a request. In real work, doing more than asked can cause as much trouble as doing less — especially under a supervision model, where your senior colleague has planned the next step deliberately.

**Question 5 (moderate) — Inference from a security policy extract**

Passage: "Passwords, API keys, and other credentials must never be committed to source code repositories. Where a service requires credentials, these must be stored in the approved secrets management tool. Any accidental commit of a credential must be reported to the security team immediately, and the credential must be rotated."

Statement: "If an API key is accidentally committed, reporting it to the security team is enough to resolve the incident."

- A) True
- B) False
- C) Cannot say
- D) True, provided the commit is deleted

**Correct answer: B**

**Explanation:** The passage sets out two required actions after an accidental commit: report it immediately, and rotate the credential. The statement claims reporting alone is enough — but the passage's "and" makes rotation equally required, so the statement contradicts the policy and is False. Option D introduces deletion, which the passage never mentions; in real life deleting a commit does not undo exposure, which is exactly why rotation is the required control. Notice the reading technique: when a policy lists actions joined by "and", every action is mandatory. This maps to your **Information security** skill — explaining the security controls available to protect solutions and services. You are not expected to run this process alone at apprentice level, but you are expected to understand it, and to speak up fast if you ever commit a secret by mistake. Speed of reporting is a virtue, never a source of blame.

**Question 6 (moderate) — Best summary of a passage**

Passage: "Pair programming means two developers working together at one workstation. One writes code while the other reviews each line as it is written, and the two swap roles frequently. Studies in government teams suggest pairing spreads knowledge across the team, reduces defects, and helps new joiners learn faster, though it can feel slower on simple tasks."

Which option best summarises the passage?

- A) Pair programming is slower than working alone and should be avoided on simple tasks.
- B) Pair programming is two developers sharing one workstation, swapping roles often; it spreads knowledge and reduces defects, though it can feel slower on simple tasks.
- C) New joiners must always pair with a senior developer at one workstation.
- D) Studies show pairing is the fastest way to write code in government teams.

**Correct answer: B**

**Explanation:** A good summary covers the main points without adding or exaggerating. The passage has three elements: the definition (two developers, one workstation, swapping roles), the benefits (knowledge sharing, fewer defects, faster learning for new joiners), and the caveat (can feel slower on simple tasks). Option B captures all three faithfully. Option A promotes the caveat into the main message and adds advice ("should be avoided") the passage never gives. Option C turns a described practice into a rule with "must always". Option D overstates: the passage says pairing can feel slower, and never claims it is fastest. Summary questions reward proportion — main points prominent, caveats included but not inflated. This matters for your working life because pairing is named in your role summary ("work with other developers to write code and tests"), and being able to explain it accurately is part of understanding how to work in an open and collaborative environment, from your **Prototyping** skill.

**Question 7 (moderate) — True/False/Cannot say on a standards passage**

Passage: "The service standard requires teams to make new source code open by default. Code should be published under an appropriate open licence unless there is a good reason not to, such as unreleased security fixes or keys and credentials. Publishing code allows other teams, in government and beyond, to reuse it."

Statement: "The majority of government teams currently publish their code openly."

- A) True
- B) False
- C) Cannot say
- D) True, because the standard requires it

**Correct answer: C**

**Explanation:** Search the passage for evidence about how many teams currently publish. There is none: the passage describes what the standard requires and why publishing is valuable, but says nothing about how many teams actually comply today. A rule existing does not tell you how widely it is followed — that is exactly the gap between "required" and "done" that Cannot say questions love to exploit, and option D falls straight into it. The statement is not contradicted either, so False is wrong too. The answer is Cannot say. This passage should feel familiar: your role summary says you create code that is open by default and easy for others to reuse, so the content is real. The reading discipline — never convert a requirement into a fact about behaviour — will serve you in every policy document you ever read.

**Question 8 (moderate) — Following a runbook precisely**

Passage (runbook extract): "If the queue length exceeds 500 messages for more than 10 minutes, restart the worker service. If a restart does not clear the queue within 15 minutes, escalate to the on-call engineer. Do not restart the worker service more than once per hour."

Situation: The queue has been at 620 messages for 12 minutes. The worker service was last restarted 20 minutes ago. What does the runbook direct you to do?

- A) Restart the worker service now.
- B) Escalate to the on-call engineer without restarting.
- C) Wait 40 minutes, then restart the worker service.
- D) Do nothing, because the queue may clear itself.

**Correct answer: C**

**Explanation:** Check each condition against the situation. The restart trigger is met: 620 exceeds 500, and 12 minutes exceeds 10. But there is a constraint: no more than one restart per hour, and the last restart was only 20 minutes ago — so restarting now (option A) is forbidden for another 40 minutes. Does the escalation rule apply? Not yet as written: escalation follows a restart that fails to clear the queue within 15 minutes; the passage describes a restart 20 minutes ago, and the queue is still long — but read carefully: we are not told that restart was for this incident or that 15 minutes were monitored; strictly, the direct instruction we can follow within the rules is to wait until a restart is permitted, then restart — option C. In a real incident you might also sensibly tell a senior colleague what is happening, but among the options given, C is the only one that follows every rule in the text. Runbook questions teach the key habit of **Service support**: apply all the conditions, including the "do not" ones, before acting.

**Question 9 (moderate) — Clear-writing judgement**

Your pair asks you to write a comment explaining a function that removes duplicate customer records. Which comment is clearest and most useful?

- A) "This function, which was written during the March sprint following the meeting about data quality, processes records."
- B) "Removes duplicate customer records, keeping the most recently updated copy of each."
- C) "Does deduplication utilising record-comparison methodology to actualise data-quality outcomes."
- D) "Removes duplicates. Do not change this function."

**Correct answer: B**

**Explanation:** A good code comment says what the code does and captures the detail a reader cannot instantly see — here, which duplicate survives. Option B does both in one plain sentence: what (removes duplicate customer records) and the crucial rule (keeps the most recently updated copy). Option A gives history instead of behaviour; when the function changes, "written in March" helps nobody. Option C is jargon soup — "actualise data-quality outcomes" carries no information a maintainer can use. Option D gives an instruction without a reason, which readers rightly distrust, and omits the tie-breaking rule. Clear-writing questions reward plain words, active verbs, and the one detail the reader genuinely needs. This is your documentation duty from **Programming and build** in miniature: you document simple programs so that others can reuse them — and clarity is what makes reuse possible.

**Question 10 (hard) — Two statements about one passage**

Passage: "Availability management aims to make sure services meet agreed availability targets. Capacity management aims to make sure services have enough resources — such as processing power and storage — to meet current and future demand. The two processes are related: a service without enough capacity will often fail its availability target, but availability can also be lost for reasons unrelated to capacity, such as software defects or network failures."

Statement 1: "Capacity problems are the only cause of missed availability targets."
Statement 2: "A service can miss its availability target even when it has enough capacity."

- A) Statement 1: True; Statement 2: False
- B) Statement 1: False; Statement 2: True
- C) Both statements: Cannot say
- D) Statement 1: False; Statement 2: Cannot say

**Correct answer: B**

**Explanation:** Take the statements one at a time. Statement 1 claims capacity problems are the only cause of missed availability. The passage directly contradicts this: "availability can also be lost for reasons unrelated to capacity, such as software defects or network failures." So Statement 1 is False. Statement 2 claims a service can miss its target even with enough capacity — and that is exactly what the same sentence guarantees: defects and network failures can break availability regardless of capacity. So Statement 2 is True, and the answer is B. Notice that the two statements are close to logical opposites, so once you have solid evidence about one, you learn about the other. This passage is your **Availability and capacity management** skill in prose form — explaining these processes and how they relate is literally the skill outcome — so this question is double practice: verbal technique and role knowledge together.

**Question 11 (hard) — Inference about what a passage implies**

Passage (sprint retrospective notes): "The team completed 7 of the 9 stories planned. The two unfinished stories both depended on the payments API test environment, which was unavailable for three days. Team members said pairing on the search feature worked well, and suggested pairing on all complex stories next sprint. No one raised concerns about the build pipeline."

Statement: "The team would have completed all 9 stories if the payments API test environment had been available."

- A) True
- B) False
- C) Cannot say
- D) True, because the notes identify the environment as the cause

**Correct answer: C**

**Explanation:** The notes establish that the two unfinished stories depended on the unavailable environment. That makes the environment a plausible cause of the shortfall — but the statement goes further and claims the stories would certainly have been finished with the environment available. The notes cannot guarantee that: the stories might also have hit other problems, run out of time, or turned out larger than expected. Plausible is not proven, so the answer is Cannot say. Option D is the trap: it converts "the unfinished stories depended on X" into "X was the whole cause", which the text never states. This distinction — a stated dependency versus a guaranteed outcome — is precisely the reasoning discipline that keeps retrospectives honest and keeps your test conclusions honest too: a failing test depends on many things, and identifying one factor does not prove it is the only one.

**Question 12 (hard) — Precision with "must", "should", and "may"**

Passage (extract from a team's development standards): "Commit messages must describe what changed and why. Branches should be short-lived, ideally merged within two days. Developers may use the experimental linting rules, which are optional this quarter. Secrets must never appear in commit messages or code."

Statement: "A developer who keeps a branch open for a week has broken a mandatory rule."

- A) True
- B) False
- C) Cannot say
- D) True, because two days is the stated limit

**Correct answer: B**

**Explanation:** Standards documents use signal words with precise strengths: "must" marks a mandatory rule, "should" marks a strong recommendation that can be departed from with judgement, and "may" marks an option. The branch rule uses "should... ideally" — a recommendation, not a mandate. A week-long branch goes against the recommendation, but the statement claims a mandatory rule was broken, and the only "must" rules in the passage concern commit messages and secrets. So the statement is False: the developer has departed from guidance, not broken a mandate. Option D treats "should, ideally within two days" as a hard limit, which is exactly the misreading this question targets. Learning to weigh must/should/may accurately is a core part of your **Modern development standards** skill — it tells you which parts of a standard bend to circumstances and which never do, such as the absolute rule that secrets never appear in code.

### Preparation tips

- **Answer only from the passage.** The single biggest improvement for most people: pretend you know nothing about the topic except what the passage says. Your outside knowledge is for work; the passage is for the test.
- **Find the governing sentence.** For every statement, locate the exact sentence in the passage that addresses it, and compare wording carefully. If no sentence addresses it, lean towards Cannot say.
- **Learn the signal words.** Must/should/may, all/some/only, always/never/this week only, and/or — circle them mentally as you read. Most verbal questions turn on one of these small words.
- **Practise the three-way judgement.** True means guaranteed by the passage; False means contradicted by the passage; Cannot say means neither. Rehearse this definition until it is automatic.
- **Read workplace texts actively.** Your team's standards, user stories, and runbooks are free practice material. After reading one, quiz yourself: what is mandatory here? What is recommended? What is not actually stated?
- **Keep a steady pace.** Read the passage once carefully rather than three times anxiously. If a question wobbles you, choose your best answer and move on; accuracy across the whole test beats perfection on one item.

### Common pitfalls to avoid

- **Filling gaps with sensible guesses.** In everyday life, guessing is helpful; in this test, it turns Cannot say answers into wrong answers. If the passage does not say it, you cannot say it.
- **Converting requirements into facts.** "The standard requires open code" does not mean teams publish openly (Question 7). Rules describe what should happen; only evidence describes what does happen.
- **Missing limiting words.** "This week only", "under direction", "at least one", "unless" — small phrases that completely change meaning. Slowing down for them is the highest-value habit in verbal reasoning.
- **Treating "should" as "must".** Recommendations and mandates are different strengths of rule (Question 12). Confusing them causes wrong answers in tests and unnecessary alarm at work.
- **Choosing summaries that exaggerate.** The best summary keeps the passage's proportions. Be suspicious of options containing "always", "never", "only", or advice the passage never gave.
- **Letting one hard passage shake you.** Passages vary in difficulty by design. A confusing one is not a sign you are failing; take a breath, apply the technique, and carry on.

## Workplace job-specific situational judgement assessment

### About this assessment

A situational judgement assessment presents realistic workplace scenarios and asks you to judge possible responses. Unlike the other assessments in this guide, there is often no single "calculated" right answer; instead, each response option reflects better or worse professional judgement, and your choices are compared with the judgements of experienced people in the profession. Typical formats include: choose the most effective response; choose the most effective and the least effective; rank all the responses from best to worst; or rate each response on a scale. Tests usually contain 10 to 20 scenarios and take 20 to 40 minutes, often untimed or generously timed, because the point is judgement rather than speed.

For an apprentice developer, situational judgement matters enormously — arguably more than any other assessment type. Your technical skills are expected to be growing, not complete. What your team most needs from you right now is good judgement about how to learn: when to ask for help and when to persist, how to respond to feedback, what to do when you make a mistake, how to behave in pairing sessions, and when to speak up about something that seems wrong. These are exactly the situations a well-designed assessment presents.

The scenarios below are drawn from your real working pattern: shadowing developers, pairing on code and tests, following a test-driven approach, helping investigate service faults under direction, and building your knowledge through certified training. Each question explains not just which option is strongest, but why — referencing the professional behaviours that government digital teams value: user focus, collaboration, ownership, honesty about mistakes, appropriate escalation, and inclusion.

One important reassurance before you begin: in nearly every apprentice scenario, the strong answers share a family resemblance. They are honest, they are timely (problems surface early), they use the supervision around you rather than hiding from it, and they keep users and teammates in mind. If you remember nothing else, remember that pattern.

### How this assessment maps to your role

- **Asking and escalating well** maps to your working pattern of shadowing and working under direction: knowing when to try a little longer and when to ask is the core apprentice judgement, and it appears in scenarios about being stuck, finding faults, and receiving unclear instructions.
- **Collaboration behaviours** map to **Prototyping** — understanding how to work in an open and collaborative environment, by pair working for example — and to your duty to work with other developers to write code and tests. Scenarios test how you behave when pairing is uncomfortable, when you disagree, and when a teammate needs help.
- **Ownership and honesty** map to **Programming and build** and the test-driven approach: scenarios about breaking the build, making mistakes, and cutting corners test whether you protect quality even when it is embarrassing or slow.
- **Security instincts** map to **Information security**: scenarios test whether you treat credentials, personal data, and suspicious requests with appropriate caution and report concerns promptly.
- **User focus** maps to **User focus**: scenarios test whether you keep the end user's needs in view even in small technical decisions, reflecting your outcome of explaining the purpose of user stories and the focus on user needs.
- **Service care** maps to **Service support**: scenarios about live faults test calm, procedure-following behaviour and completing defined activities under direction.

### Practice questions

**Question 1 (easy) — Stuck on a task**

You are working on a small coding task your mentor set you. After 45 minutes you are stuck: the test you wrote will not pass, and you do not understand the error message. Your mentor is at her desk, working with headphones on. What is the most effective response?

- A) Keep trying on your own all afternoon — asking would show you are not good enough.
- B) Spend a few more minutes noting what you have tried, then ask your mentor for help, showing her your notes.
- C) Quietly delete the failing test so the problem goes away.
- D) Post the error message in the team channel with the comment "this codebase is broken".

**Correct answer: B**

**Explanation:** Option B shows exactly the judgement apprenticeships are designed to build. A short, bounded further attempt is healthy — struggling briefly is how learning happens — and preparing notes on what you tried turns the interruption into an efficient, respectful conversation. Mentors expect questions; that is what the role structure is for. Option A confuses asking with weakness; in reality, staying silently stuck for hours wastes your time and hides a learning need, and experienced colleagues consistently rate over-long silent struggling as a more serious problem than asking early. Option C is the worst response: deleting a failing test hides a real signal and breaks the test-driven approach your role explicitly follows. Option D escalates publicly with blame before understanding the problem, which damages collaboration. The general pattern for apprentice scenarios: try briefly, prepare, then ask openly.

**Question 2 (easy) — A mistake reaches the shared branch**

Pairing session over, you continue a small change alone, and you accidentally push code that breaks the team's build. You notice the red build ten minutes later. No one has said anything yet. What is the most effective response?

- A) Say nothing and hope someone else fixes it.
- B) Immediately tell your pair or mentor what happened, and offer to help fix it or revert your change.
- C) Wait until tomorrow's stand-up to mention it.
- D) Push more changes quickly, trying different fixes until something works.

**Correct answer: B**

**Explanation:** A broken build blocks the whole team, so time matters, and the person best placed to explain the breaking change is you. Option B combines honesty, speed, and ownership: you surface the problem, attach yourself to the fix, and learn from how your mentor handles it — often the fastest lesson of the week. Option A abandons ownership and lets teammates waste time diagnosing something you already understand. Option C delays the team for up to a day, converting a small mistake into a real cost. Option D — pushing speculative fixes to a shared branch — often makes things worse and shows the wrong instinct: under pressure, slow down and get help rather than thrash. Every developer breaks the build sometimes; assessors and mentors judge you on the ten minutes after, not the mistake itself. Teams that treat mistakes this way are safer and faster, and you contribute to that culture from day one.

**Question 3 (easy) — Uncomfortable pairing session**

You are pairing with a developer who types very fast, rarely explains what he is doing, and has not offered you the keyboard all morning. You are learning little. What is the most effective response?

- A) Say nothing — he is senior, so this must be how pairing works.
- B) Stop paying attention and quietly do your training modules instead.
- C) Politely say you would learn more if you could drive for a while, and ask him to talk through his thinking as you go.
- D) Complain to your mentor afterwards that the developer is bad at pairing.

**Correct answer: C**

**Explanation:** Pair programming, part of your **Prototyping** skill's open and collaborative working, works through role-swapping and running commentary — and your role summary says you work with other developers to write code and tests, not just watch them. Option C addresses the problem directly, respectfully, and in the moment, which gives the developer the chance to adjust immediately; most colleagues respond well, and many simply have not noticed. Option A mistakes seniority for correctness and costs you a morning's learning. Option B disengages, which wastes the session entirely and reads as disinterest. Option D raises the issue with the right kind of person but at the wrong time and in blaming terms — feedback after the fact has its place, but trying the direct, courteous route first is both fairer and more effective. Speaking up constructively in the moment is a professional behaviour worth practising early: it will serve you in design reviews, retrospectives, and stand-ups for your whole career.

**Question 4 (easy) — A user story you do not understand**

Your pair is away this afternoon, and you pick up a small story: "As a caseworker, I want the export button to include archived cases, so that my monthly report is complete." You realise you are not sure whether "archived cases" includes deleted cases. What is the most effective response?

- A) Guess — include deleted cases, since more data seems safer.
- B) Ask the product owner or a teammate to clarify what the caseworker needs before you build.
- C) Build both versions so someone can choose later.
- D) Skip the story and pick a different one without telling anyone.

**Correct answer: B**

**Explanation:** The story exists to express a user's need — that is the purpose of user stories, straight from your **User focus** skill — and the need here is ambiguous in a way that changes the code you would write. Option B resolves the ambiguity at its source, cheaply and quickly: a two-minute conversation with the product owner (or a teammate who knows the caseworkers) prevents hours of wrong work. Option A guesses on exactly the kind of detail — deleted data appearing in reports — that can have real consequences for accuracy and even data protection. Option C doubles the work and still defers the decision no one asked you to defer. Option D avoids the problem and hides the avoidance, leaving the story stranded. Asking clarifying questions about user needs is not a sign of inexperience; it is what your most senior colleagues do conspicuously and often, because building the wrong thing is the most expensive mistake in software.

**Question 5 (moderate) — Credentials in the open**

While reading code to build your knowledge, you notice a file in the team repository containing what looks like a real database password. You are not sure whether it matters — it might be a test password. What is the most effective response?

- A) Ignore it — you are an apprentice, and it is probably fine.
- B) Ask about it in a public team channel, quoting the password so people can check it.
- C) Delete the file yourself immediately.
- D) Tell your mentor or a senior developer privately, right away, without copying the password anywhere.

**Correct answer: D**

**Explanation:** Your **Information security** skill asks you to explain security controls, and the relevant control is clear: credentials must not live in repositories, and possible exposures should be raised immediately so they can be assessed and, if real, rotated. Option D does this promptly, through a private route, without spreading the secret further — copying a possibly real password into a chat channel (option B) widens the exposure and is itself a security mistake, even with good intentions. Option A gambles on "probably fine"; apprentices are not expected to judge whether an exposure is real, but they are absolutely expected to report what they notice — noticing is genuinely valuable, and no one will criticise a false alarm raised in good faith. Option C acts unilaterally and destroys evidence of what was exposed and for how long, which the security team needs; deletion also does not remove the password from the repository's history. Report fast, privately, and let experienced people drive: that is the pattern.

**Question 6 (moderate) — Pressure to skip the tests**

It is late afternoon before a demo. A developer on your team says: "Just push the change without tests — we'll write them after the demo, and no one will know." Your role and training say new code follows a test-driven approach. What is the most effective response?

- A) Push without tests — a more experienced developer told you to.
- B) Refuse loudly and say you will report him for breaking the rules.
- C) Say you are not comfortable skipping the team's approach, and suggest either writing a quick test together or asking your mentor how to handle the demo deadline.
- D) Secretly write the tests at home tonight and push everything at midnight.

**Correct answer: C**

**Explanation:** This scenario tests whether you can hold a standard under social pressure while staying collaborative. Option C does both: it states your position honestly ("not comfortable"), stays constructive (offering to pair on a quick test — often only minutes of work), and uses the supervision structure appropriately (bringing in your mentor when two views conflict is escalation done well, not telling tales). Option A treats seniority as overriding the team's agreed approach; instructions from colleagues do not transfer responsibility for your own work, and "someone told me to" is a weak place to stand. Option B protects the standard but torches the relationship — jumping straight to threats skips every reasonable step. Option D hides the problem, sets a precedent of unpaid, invisible work, and leaves the demo period unprotected anyway. Note the general shape of strong answers to pressure scenarios: honest, calm, constructive alternative, and a legitimate route to a decision-maker if disagreement remains.

**Question 7 (moderate) — Fault investigation beyond your brief**

You are helping investigate a service fault, with a defined task: gather the error logs from yesterday and attach them to the incident ticket. While doing this, you think you have spotted the actual cause — a configuration value that looks wrong. Fixing it would mean changing the live service's configuration. What is the most effective response?

- A) Change the configuration value yourself — it will save everyone time.
- B) Finish gathering the logs, and tell the incident lead what you found and why you think it matters.
- C) Say nothing about your theory — cause analysis is not your job.
- D) Stop gathering logs and investigate your theory fully first.

**Correct answer: B**

**Explanation:** Your **Service support** skill is precise: you help with investigation and fixing of service faults, completing defined activities under direction. Option B honours both halves of good apprentice judgement: complete the task you were directed to do (the logs are needed regardless of any theory), and surface your observation to the person coordinating (good incident practice welcomes hypotheses from anyone, clearly labelled as hypotheses). Option A is the serious error: changing live service configuration without authorisation, during an incident, as an apprentice, risks making the incident worse and bypasses every control the team relies on — even if your theory is right, the change needs the lead's decision, and possibly a proper change process. Option C wastes a potentially valuable observation; noticing things is precisely what you are for. Option D abandons your assigned task on your own initiative, leaving the lead without the logs they asked for. Contribute observations upward; leave live changes to those directed to make them.

**Question 8 (moderate) — Feedback that stings**

In a code review, a senior developer leaves twelve comments on your small change, including "this naming is confusing" and "this test doesn't actually test anything". The tone is blunt. You feel deflated. What is the most effective response?

- A) Work through each comment, ask about the ones you do not understand, and make the changes — treating the review as free teaching.
- B) Make the changes without reading the comments properly, to get it over with.
- C) Reply defensively to each comment explaining why your original code was fine.
- D) Ask your mentor to tell the senior developer to review your code more gently in future.

**Correct answer: A**

**Explanation:** Code review is one of the main channels through which apprentices learn, and twelve detailed comments represent a senior developer's time invested in your growth — blunt phrasing notwithstanding. Option A extracts the full value: understanding each point (asking about unclear ones is expected and welcomed), then applying them, which also directly improves your **Programming and build** skill of correcting and documenting programs. Option B "complies" without learning, which means the same comments will reappear on your next change. Option C treats review as a battle to win; occasionally pushing back on a specific point with reasons is healthy, but blanket defensiveness closes the learning channel and frays the relationship. Option D outsources your feelings prematurely: if tone is a persistent problem, raising it (with your mentor, or better, kindly and directly) is legitimate — but the first move on a single stinging review is to separate the useful content from the uncomfortable delivery and take the content. Resilience with feedback is among the most valued behaviours in early-career developers.

**Question 9 (moderate) — A quieter teammate in the mob**

Your team runs a group programming session with five people. You notice that the other apprentice, who joined last month, has not spoken for an hour, and was interrupted the one time she tried. You are fairly new yourself. What is the most effective response?

- A) Stay quiet — it is not your place to manage the session.
- B) At a natural pause, say "I'd be interested in what Priya was starting to say earlier" to make space for her.
- C) Message her privately afterwards saying the team is like this sometimes.
- D) Tell the session leader afterwards that he ran an exclusionary session.

**Correct answer: B**

**Explanation:** Inclusion is a professional behaviour, not a management task, and option B performs it in the lightest possible way: a small, natural intervention that opens the door without putting anyone on the spot or criticising anyone. This is collaborative working — your open, pair-and-group working environment from **Prototyping** — functioning as intended, and it is entirely "your place": anyone in a session can make space for a colleague. Option A mistakes hierarchy for permission. Option C offers sympathy but normalises the problem ("the team is like this") and changes nothing about the session where her contribution was lost. Option D leaps to an accusation; the leader may simply not have noticed, and feedback framed as "exclusionary" invites defensiveness — if the pattern continued, a gentler observation to the leader would be a reasonable later step. Small acts of inclusion also make teams measurably better at finding defects and ideas: the quietest person in the room frequently holds the observation everyone else missed.

**Question 10 (hard) — Most and least effective: the tempting shortcut**

You are finishing your first solo-written feature (with review to come). You discover a copy of very similar code elsewhere in the codebase — you could copy-paste it and be done in ten minutes, though you do not fully understand what two of its lines do. Alternatively you could write your own version, which will take the rest of the day, or ask your mentor to talk through the existing code with you, which will take half an hour of her time. Identify the MOST effective and LEAST effective responses.

1. Copy the existing code, including the lines you do not understand, and submit it for review.
2. Ask your mentor for half an hour to understand the existing code, then reuse it knowingly.
3. Write your own version from scratch without looking further at the existing code.
4. Copy the existing code but delete the two lines you do not understand, since they are probably unnecessary.

- A) Most effective: 1; Least effective: 3
- B) Most effective: 2; Least effective: 4
- C) Most effective: 3; Least effective: 1
- D) Most effective: 2; Least effective: 1

**Correct answer: B**

**Explanation:** Reuse is genuinely good — your role summary says you create code that is easy for others to reuse, and using well-tested existing code avoids duplicating bugs. But reusing code you do not understand imports risk you cannot see. Response 2 gets the best of everything: the reuse benefit, the understanding, and a high-value use of mentor time — exactly what mentors are for — so it is most effective. For least effective, compare 1 and 4. Response 1 submits code containing lines its author (now you) cannot explain; review may catch problems, and at least the code is intact. Response 4 mutilates working code precisely at the point of your own ignorance: "I don't understand it, so it's probably unnecessary" is the reasoning that deletes the error handling or the security check, and it may pass review because it looks deliberate. That makes 4 worst, so B is correct (and D wrongly names 1 as worst). Response 3 is honest but wasteful — a full day to avoid a conversation. The deep pattern: never let "I don't understand it" quietly become "it doesn't matter".

**Question 11 (hard) — Conflicting instructions**

Your mentor set you a task for this week: finish the validation component, with tests, by Friday. On Wednesday, a delivery manager asks you to spend the next two days manually re-testing an unrelated feature because "we're short of people". Your mentor is on leave until Friday. What is the most effective response?

- A) Do what the delivery manager asks — they are more senior than you.
- B) Refuse — your mentor's instructions always win, and the delivery manager should know that.
- C) Explain your existing Friday commitment, then contact your mentor's nominated cover (or ask the delivery manager to) so the priority call is made by someone with the authority to make it.
- D) Try to do both tasks by working late both evenings without telling anyone.

**Correct answer: C**

**Explanation:** This is an escalation-shaped problem: two legitimate authorities want the same two days, and the person who set your original priority is away. Apprentices are not expected to arbitrate between a mentor and a delivery manager — but they are expected to make the conflict visible and route it to someone who can decide, which is exactly what option C does. It is transparent (the delivery manager learns of your commitment immediately), respectful to both parties, and uses the cover arrangements that exist for precisely this situation; if no cover was nominated, a senior developer on the team is the natural stand-in. Option A silently abandons a commitment; your mentor returns Friday to find the week's plan gone without a word. Option B invents a rule (mentor always wins) and applies it abrasively; the delivery manager's need might genuinely be the priority — you do not know, which is the point. Option D hides the conflict and pays for it with unsustainable hours, setting a precedent that helps no one. Surfacing conflicts early and routing decisions to the right level is professional behaviour at every grade; at yours, it is the whole skill.

**Question 12 (hard) — Ranking responses: accessibility concern near a deadline**

Your pair is finishing a form component due tomorrow. You notice the error messages only appear as a colour change from grey to red, and you remember from training that colour alone is not accessible to everyone — but you are not certain of the rule, and your pair says "it looks fine to me, let's ship it". Rank these responses from most to least effective:

1. Quickly check the accessibility guidance together now, and raise it with the team today if the concern is confirmed.
2. Say nothing — you are not sure, and the deadline is tomorrow.
3. Log a ticket suggesting the error styling be reviewed "at some point" after shipping.
4. Refuse to continue pairing until the component is rebuilt.

- A) 1, 3, 2, 4
- B) 1, 2, 3, 4
- C) 3, 1, 4, 2
- D) 1, 4, 3, 2

**Correct answer: A**

**Explanation:** Work through the ranking. Response 1 is clearly best: it converts an uncertain memory into a checked fact within minutes (accessibility guidance is easy to consult), it keeps your pair involved rather than going around him, and it gives the team the information while there is still time to act — genuine **User focus**, because accessible services are the whole point of user-centred government services, and users with colour-blindness or low vision are users. Next best is 3: it at least records the concern, though "at some point after shipping" risks a known barrier reaching real users and never being fixed — a weak second, but better than silence. Response 2 ships a possible barrier and wastes the one advantage you had: noticing. Worst is 4: refusing to work is wildly disproportionate before the concern is even verified, and damages the pairing relationship that your learning depends on. So the order is 1, 3, 2, 4 — option A. The transferable pattern: verify quickly, raise early, keep collaborating, and remember that "shipped inaccessible" is a cost paid by users, not by the team.

### Preparation tips

- **Learn the behaviour families.** Strong responses across almost all apprentice scenarios share features: surface problems early, be honest about mistakes and uncertainty, use your mentor and team rather than struggling or acting alone, keep users in mind, and stay respectful under pressure. When unsure, ask which option best fits that family.
- **Answer as you should act, not as you fear you might.** Situational judgement tests measure your understanding of effective behaviour. Choose the response that reflects good professional judgement, even if in a nervous moment real life might tempt you otherwise — practising the judgement is how it becomes real behaviour.
- **Watch for "acting alone" options.** At apprentice level, options involving unilateral changes to live services, deleting things, or secretly working extra hours are almost always weak. The supervision around you is a feature of your role; strong answers use it.
- **Distinguish escalation from telling tales.** Bringing in a mentor to resolve a conflict or verify a concern is professional; bypassing colleagues to complain about them usually is not. Notice which one an option describes.
- **Read the whole scenario, including feelings.** Details like "you are not certain" or "your mentor is on leave" are placed deliberately and change which response is best.
- **Reflect on real situations.** After a tricky day at work, ask yourself what the "most effective response" options would have been. Your own week is the best practice bank you have.

### Common pitfalls to avoid

- **Choosing deference over judgement.** "A senior person told me to" is not automatically the most effective path — several questions above turn on exactly this. Seniority deserves respect, not blind obedience, especially where standards, security, or users are at stake.
- **Choosing heroics over teamwork.** Secretly working late, fixing live systems solo, and building two versions "to be safe" all look industrious but score poorly, because they hide information and bypass the team.
- **Confusing honesty with harshness.** Options that tell the truth aggressively ("refuse loudly", "tell him he ran an exclusionary session") mix a good behaviour with a damaging delivery. The strong options are honest and constructive.
- **Delaying disclosure.** Waiting until tomorrow's stand-up, mentioning it after the demo, logging it "for later" — delay is the quiet weakener of otherwise reasonable options. Timeliness is a scoring dimension in itself.
- **Ignoring the least-effective half.** In most/least formats, half the marks are for spotting the worst option. Practise articulating why an option is harmful, not just why another is good.
- **Overthinking edge cases.** These scenarios reward mainstream good judgement, not exotic exceptions. If you find yourself inventing elaborate circumstances where a weak option becomes strong, come back to the scenario as written.

## Conclusion

Well done — you have worked through a complete set of psychometric assessment resources built specifically for your role as an apprentice developer. That is a real achievement, and it is worth pausing to notice what you have practised.

In the cognitive section, you exercised pattern recognition on naming conventions and test output, logical deduction on build rules and pipelines, error checking on scripts and configuration, and prioritisation of a realistic apprentice workload. In the numeric section, you worked step by step through pass rates, averages, availability hours, error rates, weighted combinations, and projections — the everyday arithmetic of a development team. In the verbal section, you practised precise reading of standards, user stories, emails, runbooks, and policy extracts, including the discipline of "Cannot say" and the crucial differences between must, should, and may. And in the situational judgement section, you rehearsed the moments that define an apprenticeship: being stuck, making mistakes, pairing well, protecting standards under pressure, handling security concerns, and including quieter teammates.

Here is the encouraging truth that ties it all together: none of this was separate from your job. Every technique in this guide — read the rule twice, check the base of a percentage, trust the text over your memory, surface problems early, use your mentor — is simultaneously an assessment technique and a professional habit. When you practise for the test, you are practising the role. When you do the role well, you are preparing for the test. Your daily work of shadowing, pairing, writing automatically tested code, and helping investigate faults under direction is quietly building exactly the capabilities these assessments measure.

If you take the real assessment soon, remember the practical basics: rest well, set up a quiet space, confirm any adjustments you are entitled to in advance, use the ungraded practice questions to settle in, and work steadily rather than fast. If a question rattles you, give your best answer and move on — a single question almost never decides an outcome.

And whatever the result, keep perspective. Psychometric assessments are one snapshot of a growing person, taken on one day. You are at the beginning of a career in a profession that builds services used by millions of people, and the skills in your framework — from **Programming and build** to **User focus** — grow through exactly the kind of steady, honest, curious practice you have just done. Revisit this guide when you like, quiz yourself on your own team's real standards and dashboards, and be as encouraging to yourself as a good mentor would be.

You are learning the craft the right way: carefully, collaboratively, and with users in mind. Keep going — you are doing better than you think.

---

*Professional development tip: consider keeping a short learning log. After each practice session or real work task, write one sentence about a technique you used and one about something you want to try next time. Over a few months, the log becomes evidence of growth for your apprenticeship portfolio — and a genuine confidence boost on harder days.*
