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

<!-- APPEND -->
