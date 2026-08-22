# Apprentice Frontend Developer - Psychometric Assessment Resources

## Introduction

Welcome! This guide has been written especially for you as an apprentice frontend developer in the UK Government Digital and Data profession. You might be preparing for an assessment as part of your apprenticeship. You might be getting ready for an end-point assessment, an internal review, or an application for your first junior post. Or you might simply be curious about what psychometric assessments are and how they connect to your work. Whatever brought you here, this guide will help you practise, build confidence, and feel ready.

First, let's answer the big question: what is a psychometric assessment? It is a structured, standardised exercise that measures the thinking skills and workplace behaviours that predict success in a role. "Standardised" simply means everyone gets the same kind of questions under the same conditions, so the results are fair. There are no trick questions designed to catch you out. There is no pass mark based on being a genius. These assessments measure practical, everyday thinking — the kind you already use when you read an HTML file, follow a naming convention, or decide who to ask for help.

Why does this matter for your role in particular? As an apprentice, you spend a lot of your time learning: shadowing other developers, pairing on code and tests, writing simple user interfaces under direction, and building your understanding of accessibility, web standards, and web performance. The assessments in this guide use exactly those materials. You will check code snippets for errors, read a browser support table, work out percentages from a page-weight report, understand an email from your mentor, and decide what to do when you are stuck on a ticket. Nothing here assumes knowledge beyond your level. Everything here is grounded in the real day-to-day of an apprentice frontend developer: HTML, CSS, JavaScript, pairing, feedback, and users.

This document is organised into four main sections, one for each assessment type you are likely to meet:

1. A **cognitive assessment** — pattern spotting, logical thinking, error checking, and prioritising, all using frontend artefacts.
2. A **numeric reasoning assessment** — percentages, averages, and simple tables using data such as page weights, test results, and accessibility issue counts.
3. A **verbal reasoning assessment** — reading short workplace passages carefully and answering true, false, or cannot-say questions.
4. A **situational judgement assessment** — realistic apprentice dilemmas, where you choose the most effective and least effective responses.

Each section follows the same friendly pattern. First, a short explanation of what the assessment measures and why employers use it. Second, a map showing how the assessment connects to the named skills in your role. Third, a set of practice questions that start easy and get gradually harder, each with a full worked explanation. Fourth, preparation tips. Fifth, common pitfalls and how to avoid them.

Here is how to get the most from this guide. Take it one section at a time — there is no prize for rushing. Try each question honestly and write down your answer before you read the explanation. Then read every explanation, even for questions you got right, because the explanations teach technique, not just answers. If a question catches you out, that is good news: it means the practice is working. Come back in a week and try again.

You are at the start of your career, and that is a strength — everything you practise now becomes a habit that will serve you for years. Take your time, be kind to yourself, and let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive assessment measures the exact thinking skills your role uses every day. It is not an abstract intelligence test full of strange shapes. Instead, it shows you realistic workplace materials — in your case, HTML snippets, CSS class names, simple JavaScript, ticket boards, code review comments, and build steps — and asks you to reason about them quickly and carefully.

The typical format is an online, timed test lasting 15 to 30 minutes. You usually answer between 15 and 30 multiple-choice questions covering pattern recognition, logical deduction, error checking, prioritisation, and applied problem solving. Scoring is objective: your answers are compared with a large group of people who took the same test, called a norm group. Many modern platforms are adaptive, which means the questions get a little harder when you answer correctly and a little easier when you don't. That is normal, so don't panic if the questions feel like they are getting tougher — it often means you are doing well. Employers usually see a balance of speed and accuracy, so working steadily and carefully matters more than racing.

Why do employers use this for apprentice frontend developers? Because frontend work is detail work. A missing closing tag breaks a page. A class name that doesn't follow the team convention confuses the next developer. A test that checks the wrong thing gives false confidence. Employers want to know that you can spot patterns, follow rules exactly, notice small errors, and think step by step — because those are the habits that make code clean, accessible, and reliable. The good news is that these are learnable habits, and this section will help you practise them.

### How this assessment maps to your role

Each dimension of the cognitive assessment connects directly to named skills in your role summary:

- **Pattern recognition** maps to **Programming and build (frontend developer)** and **Modern development standards**. When you design, code, test, correct and document simple user interfaces under the direction of others, you constantly work with patterns: naming conventions, folder structures, component templates, and the repeated shapes of HTML. Spotting when something breaks the pattern is a core coding skill.
- **Logical deduction** maps to **Programming and build (frontend developer)** and **Web performance optimisation**. Working out what a rule implies — "if the browser does not support this feature, then the fallback must load" — is exactly the reasoning behind progressive enhancement, which your role asks you to follow.
- **Error checking** maps to **Accessibility** and **Programming and build (frontend developer)**. You help fix accessibility issues under the direction of others, and that starts with noticing them: a missing label, a skipped heading level, an image without alternative text.
- **Prioritisation** maps to **Leadership and guidance (frontend developer)** and **Community collaboration**. Following agreed good practice for the team includes knowing what to do first, when to keep going, and when to ask for help — a daily decision for every apprentice.
- **Applied problem solving** maps to **User focus (frontend developer)** and **Prototyping**. Understanding user stories and knowing why and when to prototype both require you to take a fuzzy situation, break it into steps, and reason towards a sensible next action.

As you work through the questions, notice how each one is really a miniature version of a task you already do — or will soon do — at work.

### Practice questions

**Question 1 (easy) — Pattern recognition in CSS class names**

Your team follows a naming convention for CSS classes: every class starts with the prefix `app-`, then the component name, then two underscores and the element name if needed. For example: `app-card`, `app-card__title`, `app-card__body`. While pairing with another developer, you see this list in a stylesheet:

1. `app-banner`
2. `app-banner__heading`
3. `app_banner__link`
4. `app-banner__icon`

Which class name breaks the team's convention?

- A) Class 1
- B) Class 2
- C) Class 3
- D) Class 4

**Correct answer: C**

**Explanation:** Work through the rule step by step. The prefix must be `app-` with a hyphen. Classes 1, 2 and 4 all start with `app-` and use two underscores before the element name, so they follow the pattern. Class 3 starts with `app_banner` — an underscore where the hyphen should be. It is a tiny difference, but in CSS a tiny difference means the style will not apply, because `app_banner__link` and `app-banner__link` are completely different names to the browser. This is exactly the kind of check you do when you follow agreed good practice for the team: conventions only help if everyone follows them exactly. In the real assessment, read patterns character by character — your eyes will try to "auto-correct" small errors, so slow down just enough to see what is really there.

**Question 2 (easy) — Logical deduction about progressive enhancement**

Your team's standard says: "Every interactive feature must work without JavaScript, unless the team has agreed a documented exception." You are shadowing a developer who shows you a new postcode lookup feature. They tell you: "This feature does not work without JavaScript." Which one of the following must be true?

- A) The team has broken its standard.
- B) The team has agreed a documented exception for this feature.
- C) Either the team has agreed a documented exception, or the standard has been broken.
- D) The feature should be rebuilt immediately.

**Correct answer: C**

**Explanation:** The standard is a rule with one allowed exception. From what you know, you cannot tell whether an exception exists for the postcode lookup. So option A might be true, and option B might be true, but neither one *must* be true. Option D jumps to an action before you know the facts. The only statement that must be true in every case is option C: one of the two possibilities holds. This careful "only conclude what you know for certain" thinking is a habit worth building early. At work, it stops you from assuming a colleague has made a mistake before you have checked — for example, by asking your mentor whether an exception was agreed. Deduce first, then ask; never accuse.

**Question 3 (easy) — Error checking heading levels**

You are helping fix accessibility issues under the direction of a senior developer. They remind you that heading levels should not skip: an `<h1>` can be followed by an `<h2>`, an `<h2>` by an `<h3>`, and so on, but a page should not jump from `<h1>` straight to `<h3>`. You review this page outline:

1. `<h1>` Apply for a fishing licence
2. `<h2>` Before you start
3. `<h3>` What you will need
4. `<h2>` How to apply
5. `<h4>` Apply online

Which heading breaks the rule?

- A) Heading 2
- B) Heading 3
- C) Heading 4
- D) Heading 5

**Correct answer: D**

**Explanation:** Check each step in order. Heading 1 to heading 2: `<h1>` to `<h2>` — fine. Heading 2 to heading 3: `<h2>` to `<h3>` — fine. Heading 3 to heading 4: `<h3>` back up to `<h2>` — that is allowed, because you can move back up to start a new section. Heading 4 to heading 5: `<h2>` down to `<h4>` — that skips `<h3>`, which breaks the rule. Skipped heading levels matter because people who use screen readers often navigate by headings; a skipped level makes the page structure confusing, like a book that jumps from chapter 2 to chapter 4. Noticing this kind of issue is one of the first accessibility skills you will build, and it needs no special tools — just careful, systematic checking, one step at a time.

**Question 4 (easy) — Prioritising your morning**

It is 9:30 am, just after stand-up. You have four things you could do:

1. Your pairing session with a senior developer starts at 10:00 am, and they asked you to read a short ticket description before you start.
2. A quiz for your apprenticeship training course is due on Friday (it is Tuesday today).
3. Yesterday you noticed a typo on a page your team owns; you have not told anyone yet.
4. Your inbox has some unread newsletters.

What is the best thing to do first?

- A) Start the training quiz, because apprenticeship study always comes first.
- B) Read the ticket description, so you are ready for the pairing session.
- C) Clear your inbox so you can concentrate later.
- D) Try to fix the typo yourself before anyone notices it.

**Correct answer: B**

**Explanation:** Think about urgency and impact together. The pairing session starts in 30 minutes, and your preparation directly affects someone else's time as well as your own — arriving unprepared wastes part of a senior developer's morning. That makes option B both urgent and high impact. The quiz matters, but Friday is three days away, so it can be scheduled later today or tomorrow. The typo should be raised — but the right move is to mention it to your team (perhaps at the next stand-up or in the team channel), not to fix it secretly, so option D is doubly wrong: it is neither urgent nor the agreed way of working. Newsletters are never the priority. In prioritisation questions, look for the item where a deadline and an effect on other people meet — that is almost always first.

**Question 5 (moderate) — Pattern recognition in a component library**

Your team's component library stores each component in its own folder. The pattern is: a folder named after the component, containing a template file, a style file, and a test file, all named after the component. For example, the `button` folder contains `button.html`, `button.scss`, and `button.test.js`. You list the files in four folders:

1. `checkbox/` → `checkbox.html`, `checkbox.scss`, `checkbox.test.js`
2. `radio/` → `radio.html`, `radio.scss`, `radios.test.js`
3. `select/` → `select.html`, `select.scss`, `select.test.js`
4. `textarea/` → `textarea.html`, `textarea.scss`, `textarea.test.js`

Which folder contains a file that breaks the pattern?

- A) Folder 1
- B) Folder 2
- C) Folder 3
- D) Folder 4

**Correct answer: B**

**Explanation:** Compare each file name with its folder name. Folder 2 is named `radio`, but its test file is named `radios.test.js` — with an extra "s". Every other file matches its folder name exactly. This matters in practice: many build tools and test runners find files by name pattern, so a mismatched name can mean a test silently never runs, and a component ships without its safety net. When you check patterns like this, be systematic: check folder against file, one pair at a time, rather than letting your eyes sweep the whole list at once. Assessments deliberately include near-matches like `radio`/`radios` because the human brain reads whole words, not letters — deliberate, slightly slower checking beats fast skimming.

**Question 6 (moderate) — Logical deduction from a browser support table**

Your team's browser support policy says: (i) features used on public pages must work in the two most recent versions of the major browsers; (ii) if a CSS feature is not supported in a required browser, you must provide a fallback; (iii) fallbacks must be tested before the change is merged. You want to use a CSS feature that is supported in all required browsers except one. Your fallback is written but not yet tested. Which statement must be true?

- A) You can merge the change now, because the fallback exists.
- B) You cannot merge the change yet.
- C) You should remove the CSS feature and use only the fallback.
- D) The browser support policy does not apply, because most browsers support the feature.

**Correct answer: B**

**Explanation:** Follow the chain of rules. The feature is unsupported in one required browser, so rule (ii) applies: a fallback is required. You have one — good. But rule (iii) says fallbacks must be tested *before* merging, and yours is not tested yet. So the conditions for merging are not yet met, and option B must be true. Option A ignores rule (iii). Option C goes further than the rules require — the policy allows modern features with tested fallbacks; that is the heart of progressive enhancement. Option D invents an exception that the policy does not contain. This is a very common shape of assessment question: a set of "if… then…" rules and a situation, where your job is to apply the rules exactly as written, without adding or removing anything. It mirrors real code review, where "almost meets the checklist" means "not yet ready".

**Question 7 (moderate) — Error checking a form snippet**

A senior developer asks you to check a form field against four team rules: (i) every input must have a `<label>` linked by matching `for` and `id` values; (ii) hint text goes in a separate element, not in the `placeholder`; (iii) inputs collecting names must have `autocomplete="name"`; (iv) the label text must use sentence case. You review:

```
<label for="full-name">Full Name</label>
<div class="hint">As shown on your passport</div>
<input id="full-name" autocomplete="name" type="text">
```

Which rule is broken?

- A) Rule (i) — the label is not linked correctly
- B) Rule (ii) — hint text is in the wrong place
- C) Rule (iii) — the autocomplete attribute is missing
- D) Rule (iv) — the label is not in sentence case

**Correct answer: D**

**Explanation:** Check each rule in turn, ticking them off. Rule (i): the label's `for="full-name"` matches the input's `id="full-name"` — correct. Rule (ii): the hint is in its own `<div class="hint">`, not in a placeholder — correct. Rule (iii): `autocomplete="name"` is present — correct. Rule (iv): the label reads "Full Name", but sentence case means only the first word is capitalised: "Full name". So rule (iv) is broken. This question rewards a checklist habit: instead of staring at the code hoping an error jumps out, walk the rules one by one and mark each pass or fail. That is exactly how you will do your first accessibility and code reviews under direction — and the habit of checking every rule, even after finding three passes, keeps you from stopping too early.

**Question 8 (moderate) — Ordering build steps**

Your team's project has four steps that run when building the site: (i) install dependencies; (ii) compile the Sass files into CSS; (iii) run the tests; (iv) deploy to the staging environment. The team rules are: dependencies must be installed before anything else can run; tests must run after the Sass compiles, because some tests check the compiled CSS; deployment must only happen if the tests pass. Which order is correct?

- A) Install, test, compile, deploy
- B) Install, compile, test, deploy
- C) Compile, install, test, deploy
- D) Install, compile, deploy, test

**Correct answer: B**

**Explanation:** Turn each rule into an ordering fact. "Dependencies first" puts install at the start — that removes option C. "Tests after Sass compiles" means compile comes before test — that removes option A. "Deploy only if tests pass" means test comes before deploy — that removes option D. The only order satisfying all three rules is install → compile → test → deploy, which is option B. Notice the technique: you did not need to imagine the whole pipeline at once; you used each rule to eliminate wrong answers. Dependency-ordering questions appear in many cognitive tests, and they map directly to your growing knowledge of how static assets are built from source code — understanding *why* the steps are ordered this way (each step needs the previous step's output) is more useful than memorising any single pipeline.

**Question 9 (moderate) — Applied problem solving on a broken page**

A page you helped build looks wrong on your screen: the footer styles are missing, but everything else looks fine. You know the following: the footer styles live in `footer.scss`; all `.scss` files must be listed in `main.scss` to be included in the compiled CSS; the compiled CSS loads correctly (other styles work). What is the most likely cause to check first?

- A) The user's internet connection is slow.
- B) `footer.scss` is not listed in `main.scss`.
- C) The whole CSS file failed to load.
- D) The browser does not support CSS.

**Correct answer: B**

**Explanation:** Reason from the evidence. Other styles work, so the compiled CSS file loaded — that rules out options C and D, and makes A irrelevant (a slow connection would not remove only the footer styles). The one fact that fits the evidence is that the footer's styles never made it into the compiled file, and the stated rule tells you how that happens: a `.scss` file must be listed in `main.scss`. So the first thing to check is whether `footer.scss` is missing from that list. This is the everyday logic of debugging: gather what works and what doesn't, eliminate causes the evidence contradicts, and check the most likely remaining cause first. As an apprentice you will do this with support, and it is fine to ask for help — but arriving with "here is what I checked and what I found" makes pairing on the problem far more productive.

**Question 10 (challenging) — Multi-rule deduction about a code review**

Your team's rules for merging a change are: (i) at least one approval from another developer; (ii) all automated tests passing; (iii) if the change touches a form, an accessibility check is also required; (iv) apprentice changes additionally need approval from the apprentice's mentor. Your change updates a form's error message. You have: one approval from a junior developer, all tests passing, and a completed accessibility check. What is still missing before you can merge?

- A) Nothing — you can merge now.
- B) A second developer approval.
- C) Your mentor's approval.
- D) An accessibility check.

**Correct answer: C**

**Explanation:** Match your situation to each rule. Rule (i): you have one developer approval — satisfied. Rule (ii): tests pass — satisfied. Rule (iii): the change touches a form (an error message is part of a form), and the accessibility check is done — satisfied. Rule (iv): you are an apprentice, so you also need your mentor's approval — and that is not in your list. So option C is the answer. The trap in this question is relief: after ticking three rules, it is tempting to choose "nothing missing". Assessments — and real checklists — punish stopping one rule early. Notice also that rule (iv) uses the word "additionally": special rules for your situation stack on top of the general rules, they do not replace them. Reading rule words like "additionally", "unless", and "only" with full attention is one of the most valuable habits this whole assessment type builds.

**Question 11 (challenging) — Scheduling with several constraints**

You need to book three activities next week, each taking one morning: a pairing session (P), an accessibility workshop (W), and your protected study time (S). The rules are: (i) your mentor is only free on Monday and Thursday mornings, and must attend the pairing session; (ii) the workshop is only offered on Tuesday and on Wednesday; (iii) the team's protected study morning is Wednesday only, and your study must come after your pairing session, because you will study the topic you paired on; (iv) at most one activity per morning. If you attend the workshop on Tuesday, on which day must the pairing session happen?

- A) Monday
- B) Tuesday
- C) Wednesday
- D) Thursday

**Correct answer: A**

**Explanation:** Place the fixed items first, then see what freedom remains. The workshop is fixed to Tuesday by the question. Study can only happen on Wednesday (rule iii), so study is Wednesday. Pairing must be Monday or Thursday, because those are the only mornings your mentor is free (rule i). Now apply the ordering rule: study must come *after* pairing. If pairing were Thursday, study on Wednesday would come *before* it — breaking rule (iii). So pairing must be Monday: pairing Monday, workshop Tuesday, study Wednesday satisfies every rule, and no clash occurs because each activity has its own morning (rule iv). The technique to remember: in scheduling questions, anchor the least flexible items first (here, study had only one possible day), and let the ordering rules eliminate the remaining options. This is exactly how sprint and diary planning works in real teams — fixed ceremonies and other people's availability go in first, and your flexible work fits around them.

**Question 12 (challenging) — Applied problem solving with a performance budget**

Your team has a performance rule: each page's total download size must stay under 500 KB. A page currently totals 480 KB. A designer asks to add a decorative image (90 KB) and a new font weight (60 KB). You know two possible savings: compressing an existing hero image would save 120 KB, and removing an unused script would save 35 KB. If the team adds *both* new items, what is the minimum you must also do to stay within the budget?

- A) Nothing — the additions fit within the budget.
- B) Apply the image compression only.
- C) Remove the unused script only.
- D) Apply both the compression and the script removal.

**Correct answer: D**

**Explanation:** Work the numbers step by step, exactly as you would with a real performance budget. New total after the additions: 480 + 90 + 60 = 630 KB. The budget is 500 KB, so you must save at least 630 − 500 = 130 KB. Now test each option precisely. Option A: 630 KB is over budget — fails. Option B: compression saves 120 KB, giving 630 − 120 = 510 KB — still 10 KB over, so it fails. Option C: the script removal saves 35 KB, giving 595 KB — well over, fails. Option D: both savings give 630 − 120 − 35 = 475 KB — under 500 KB, so it succeeds, and it is the *minimum* action that does. The trap here is option B: 120 KB "feels" close enough to 130 KB, and a rushed candidate accepts it. But performance budgets are hard limits — being 10 KB over is over. The habit to build: compute the exact new total, compute the exact required saving, and test each option with real arithmetic rather than gut feel. That is precisely the discipline you will use when you help improve web performance under supervision, and it turns a scary-looking question into simple addition and subtraction.

### Preparation tips

- **Practise little and often.** Ten minutes of pattern-spotting or rule-checking a day beats a two-hour cram. Your brain builds checking habits through repetition, just like it learns keyboard shortcuts.
- **Use your real work as practice.** Every code review you shadow is a cognitive workout. When a senior developer spots something, ask yourself: what pattern or rule did they check? Then try to spot the next one before they do.
- **Slow down on purpose for details.** Most apprentice-level mistakes in these tests come from reading too fast, not thinking too little. Train yourself to read class names, attribute values, and rule words ("unless", "only", "additionally") character by character.
- **Turn rules into checklists.** When a question gives you three or four rules, number them and tick each one off against the situation. Never stop at the first rule that passes or fails.
- **Do the official practice questions.** Real assessments almost always offer ungraded practice questions first. Always do them — they let you learn the interface without pressure.
- **Look after the basics.** Sleep well the night before, find a quiet spot, close your other tabs, and have water nearby. Simple, boring, and genuinely effective.
- **Remember your level.** Nobody expects an apprentice to score like a senior developer. Assessments compare you fairly, and your job is to show careful, honest thinking — which you practise every day at work.

### Common pitfalls to avoid

- **Skimming instead of reading.** Near-identical names (`radio` vs `radios`, `app-` vs `app_`) are the classic trap. If two options look the same, they almost certainly are not — look again, slowly.
- **Adding rules that aren't there.** If the question says "fallbacks must be tested", do not also assume "fallbacks must be approved". Apply exactly what is written, nothing more.
- **Stopping the checklist early.** Finding three rules satisfied does not mean the fourth is. Always check every rule, especially the last one — question setters know tired eyes stop early.
- **Choosing the action instead of the deduction.** When a question asks what *must be true*, resist options that describe what you *should do*. Logic questions want conclusions, not plans.
- **Panicking when questions get harder.** On adaptive tests, harder questions usually mean you are doing well. Take a breath and keep your method: read, list the rules, check each one.
- **Guessing wildly under time pressure.** If you must move on, eliminate the options you can disprove first, then choose from what remains. Even eliminating one option improves your odds meaningfully.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A numeric reasoning assessment measures how well you work with numbers in realistic workplace situations. Don't worry — this is not an advanced maths exam. The mathematics involved rarely goes beyond percentages, averages, ratios, and reading tables and charts. What the assessment really measures is whether you can pick the right numbers out of a table, do the right calculation with them, and interpret the result sensibly under a little time pressure.

The typical format is an online, timed test lasting 20 to 30 minutes, with 15 to 25 multiple-choice questions. Each question usually shows you some data — a table, a chart, or a short description with numbers in it — and asks a question about it. You can normally use a calculator and rough paper, and you should. Scoring is objective, and like cognitive tests, many numeric tests are adaptive. The single most important habit is to write down your working: it slows you down by seconds and saves you from errors that cost marks.

Why do employers use numeric reasoning tests for frontend developers, even apprentices? Because frontend work is quietly full of numbers. Page weights are measured in kilobytes and budgets are hard limits. Performance is measured in milliseconds and scores. Test suites report pass rates as percentages. Accessibility audits count issues by severity. Analytics report what percentage of users are on which browser or device, which drives what you must support. Sprint boards count tasks done and remaining. An apprentice who can read this data correctly — and spot when a number looks wrong — becomes useful to the team very quickly. This section gives you practice with exactly these kinds of numbers, starting gently.

### How this assessment maps to your role

The numeric skills in this assessment support several named skills from your role summary:

- **Percentages and proportions** map to **Web performance optimisation**: describing the basic principles of web performance means working with page-weight budgets, file-size savings from compression, and percentage changes in load time. You practised a taste of this in the cognitive section; here you go deeper.
- **Reading tables and charts** maps to **User focus (frontend developer)** and **Communicating information**: user experience analysis produces data — device usage, task completion rates, error counts — and interpreting information from design and business stakeholders often means reading their spreadsheets and dashboards correctly.
- **Averages and simple rates** map to **Programming and build (frontend developer)**: test suites, build times, and bug counts are all summarised as averages and rates, and you will meet them in every sprint review.
- **Ratios and comparisons** map to **Accessibility**: colour contrast is literally expressed as a ratio (such as 4.5:1), and audit results compare issue counts across pages — understanding that users have different accessibility needs includes understanding the numbers in an audit report.
- **Careful, step-by-step arithmetic** maps to **Modern development standards** and **Community collaboration**: checking your working before sharing it is the numeric version of testing your code before pushing it — a habit your whole team relies on.

None of these require maths beyond what you already know. They require care, method, and practice — which is what this section is for.

### Practice questions

**Question 1 (easy) — Percentage of a page-weight budget**

Your team's performance budget allows 500 KB per page. The page you are working on currently totals 400 KB. What percentage of the budget is currently used?

- A) 40%
- B) 75%
- C) 80%
- D) 90%

**Correct answer: C**

**Explanation:** A percentage is a part divided by a whole, multiplied by 100. The part is the current page weight (400 KB) and the whole is the budget (500 KB). Step 1: 400 ÷ 500 = 0.8. Step 2: 0.8 × 100 = 80%. So 80% of the budget is used, and the page has 20% (100 KB) of headroom left. A quick sense-check helps: 400 is clearly most of 500 but not nearly all of it, so answers like 40% (too small) and 90% (too big) can be rejected on sight. Building the habit of a rough sense-check before and after calculating is the single best defence against calculator slips — in tests and in real performance reviews alike.

**Question 2 (easy) — Counting test results**

Your team's test suite has 250 automated tests. After your latest change, 240 pass and the rest fail. How many tests fail, and what is the pass rate?

- A) 10 fail; 96% pass
- B) 10 fail; 94% pass
- C) 15 fail; 96% pass
- D) 40 fail; 84% pass

**Correct answer: A**

**Explanation:** Two small steps. Step 1: failures = total − passes = 250 − 240 = 10. Step 2: pass rate = passes ÷ total × 100 = 240 ÷ 250 = 0.96, and 0.96 × 100 = 96%. So 10 tests fail and 96% pass. Notice that the wrong options mix one correct number with one incorrect one — a very common trick. Always compute *both* parts of a two-part answer rather than choosing the option that matches the first number you found. At work, the same care applies when you report test results in stand-up: "240 of 250 passing, 10 failures, all in the date-picker component" is precise, useful, and exactly the kind of communication your team values from an apprentice.

**Question 3 (easy) — Reading a device usage table**

Your team shares this table of visits to your service last month:

| Device type | Visits |
|---|---|
| Mobile | 60,000 |
| Desktop | 30,000 |
| Tablet | 10,000 |

What fraction of all visits came from mobile devices?

- A) One half
- B) Three fifths
- C) Two thirds
- D) Three quarters

**Correct answer: B**

**Explanation:** First find the whole: 60,000 + 30,000 + 10,000 = 100,000 visits. Then form the fraction: mobile ÷ total = 60,000 ÷ 100,000 = 6/10, which simplifies to 3/5 — three fifths, or 60%. Working with a round total like 100,000 makes this easy, and test writers often choose friendly numbers at the easy end. The workplace point matters more than the arithmetic: if three fifths of your users are on mobile, then testing your interface on a mobile-sized screen is not optional — it is where most of your users live. Numbers like these are exactly why your role focuses on user needs: the data tells you which users you would let down if you only checked the page on your own laptop.

**Question 4 (easy) — Average build time**

You record how long the project build takes on five runs: 40 seconds, 45 seconds, 50 seconds, 55 seconds, and 60 seconds. What is the average (mean) build time?

- A) 45 seconds
- B) 48 seconds
- C) 50 seconds
- D) 52 seconds

**Correct answer: C**

**Explanation:** The mean is the sum divided by the count. Step 1: add the values: 40 + 45 + 50 + 55 + 60 = 250 seconds. Step 2: divide by the number of runs: 250 ÷ 5 = 50 seconds. A useful shortcut for evenly spaced numbers: when values rise in equal steps (here, steps of 5), the mean is simply the middle value — 50. Spotting that pattern saves time, but only use shortcuts you can verify. Why track build times at all? Because a build that slowly creeps from 50 seconds to 5 minutes quietly steals the team's day, and the first person to notice is often the one who measured. Bringing a small piece of evidence like this to your team is a great way for an apprentice to contribute.

**Question 5 (moderate) — Percentage change in load time**

You help improve a page's load time under supervision. Before the change, the page loaded in 4.0 seconds. After the change, it loads in 3.0 seconds. What is the percentage improvement in load time?

- A) 10%
- B) 25%
- C) 33%
- D) 75%

**Correct answer: B**

**Explanation:** Percentage change is (difference ÷ original) × 100 — and the word "original" is the key. Step 1: difference = 4.0 − 3.0 = 1.0 seconds. Step 2: divide by the *original* value: 1.0 ÷ 4.0 = 0.25. Step 3: 0.25 × 100 = 25%. The classic error is dividing by the new value instead: 1.0 ÷ 3.0 ≈ 33%, which is exactly why option C is there. Remember: improvement is measured against where you started. In performance work you will see this constantly — "we cut load time by 25%" — and being the person who calculates it correctly builds your credibility. If you ever forget which number to divide by, say the sentence out loud: "one second faster *than the original four*" — the sentence tells you the denominator.

**Question 6 (moderate) — Accessibility audit table**

An accessibility audit of four pages on your service reports these issue counts:

| Page | Critical issues | Minor issues |
|---|---|---|
| Start page | 0 | 4 |
| Form page | 3 | 5 |
| Confirmation page | 1 | 2 |
| Guidance page | 2 | 9 |

Your mentor asks: "Which page has the most issues in total, and how many critical issues are there across the whole service?" What is the correct answer?

- A) Guidance page; 6 critical issues
- B) Form page; 6 critical issues
- C) Guidance page; 5 critical issues
- D) Form page; 8 critical issues

**Correct answer: A**

**Explanation:** Two separate calculations — do them one at a time. Totals per page: Start 0 + 4 = 4; Form 3 + 5 = 8; Confirmation 1 + 2 = 3; Guidance 2 + 9 = 11. The Guidance page has the most in total (11). Critical issues across the service: 0 + 3 + 1 + 2 = 6. So the answer is Guidance page and 6 critical issues — option A. The trap is option B: the Form page has the most *critical* issues, and if you blur the two questions together you will pick it. Read exactly what is asked. There is a real-world lesson too: "most issues" and "most serious issues" are different facts, and both matter — the team might fix the Form page's critical issues first even though the Guidance page has more issues overall. Reading audit tables accurately is an early, valuable part of building your accessibility skill.

**Question 7 (moderate) — Sprint task ratio**

Your team's sprint board shows 24 tasks in total. So far, 15 are done, 6 are in progress, and the rest have not been started. What is the ratio of done tasks to not-started tasks, in its simplest form?

- A) 15:6
- B) 5:2
- C) 5:1
- D) 8:1

**Correct answer: C**

**Explanation:** First find the missing number: not-started = 24 − 15 − 6 = 3 tasks. The ratio of done to not-started is 15:3. To simplify a ratio, divide both sides by their largest common factor — here 3 — giving 5:1. Option A is the ratio of done to *in progress* (15:6, which simplifies to 5:2, option B); both are traps for anyone who grabs the wrong pair of numbers. The method to remember: identify exactly which two quantities the question asks about, compute any missing values from the total first, then simplify. Sprint numbers like these come up in every planning session and retrospective, and while the team's delivery lead usually presents them, understanding them lets you follow the conversation — and one day, lead it.

**Question 8 (moderate) — File size savings from compression**

You are helping optimise images under supervision. Three images on a page are 300 KB, 200 KB, and 100 KB. Compressing them reduces each image's size by 40%. What is the total size of the three images after compression?

- A) 240 KB
- B) 360 KB
- C) 400 KB
- D) 440 KB

**Correct answer: B**

**Explanation:** There are two safe routes — use whichever feels clearer, and check with the other if time allows. Route 1, image by image: a 40% reduction means each image keeps 60% of its size. 300 × 0.6 = 180; 200 × 0.6 = 120; 100 × 0.6 = 60. Total: 180 + 120 + 60 = 360 KB. Route 2, total first: the images currently total 300 + 200 + 100 = 600 KB; keeping 60% of 600 gives 600 × 0.6 = 360 KB. Both routes agree: 360 KB. The classic error is calculating the *saving* (600 × 0.4 = 240 KB, option A) and mistaking it for the remaining size — read the question's final line carefully to see which one is asked for. The "keep 60%" trick (working with what remains rather than what is removed) is faster and less error-prone than subtracting, and it is a technique you will reuse constantly in performance work.

**Question 9 (moderate) — Browser support percentages**

Analytics for your service show these browser shares: Browser A 55%, Browser B 25%, Browser C 12%, Browser D 5%, others 3%. Your team's policy is to fully support any browser used by at least 5% of visitors. Last month the service had 80,000 visitors. How many visitors used browsers that are *not* fully supported under the policy?

- A) 2,400
- B) 4,000
- C) 6,400
- D) 14,400

**Correct answer: A**

**Explanation:** Step 1: decide which browsers fall outside the policy. The threshold is "at least 5%", so Browsers A (55%), B (25%), C (12%) and D (exactly 5%) are all supported. Only "others" at 3% falls below the line. Step 2: convert that share into people: 3% of 80,000 = 0.03 × 80,000 = 2,400 visitors. The trap is option C: if you misread "at least 5%" as "more than 5%", you would exclude Browser D too, giving (5% + 3%) × 80,000 = 6,400. Threshold words — "at least", "more than", "up to" — decide which side of the line a boundary case sits on, in tests and in policies alike. And notice the human meaning: 2,400 real people used an unsupported browser last month. That is why progressive enhancement matters — even "unsupported" browsers should get a working, if simpler, experience.

**Question 10 (challenging) — Performance score trend**

Your page's performance score (out of 100) was measured monthly: April 60, May 66, June 72, July 78. If the score keeps improving by the same fixed amount each month, in which month would it first reach at least 95?

- A) September
- B) October
- C) November
- D) December

**Correct answer: B**

**Explanation:** First find the pattern: 66 − 60 = 6; 72 − 66 = 6; 78 − 72 = 6. The score rises by 6 points each month. Now project forward from July's 78, month by month, writing each step down: August 84, September 90, October 96. September's 90 is below 95, and October's 96 is the first value at or above 95 — so October, option B. The common slip is a fencepost error: counting "we need 17 more points, 17 ÷ 6 ≈ 3 months, July + 3 = October" happens to work here, but candidates often round down to 2 months and answer September. Listing the actual values is slower by ten seconds and almost impossible to get wrong. Real performance scores rarely improve in neat straight lines, of course — but recognising trends, projecting them cautiously, and checking against a target is exactly how teams track progress against a performance goal.

**Question 11 (challenging) — Combining percentages from a two-way table**

A usability test of your team's new form involved 40 participants: 25 on mobile and 15 on desktop. On mobile, 80% completed the form successfully. On desktop, 60% completed it. How many participants failed to complete the form, and what is the overall completion rate?

- A) 11 failed; 72.5% overall
- B) 11 failed; 70% overall
- C) 9 failed; 77.5% overall
- D) 14 failed; 65% overall

**Correct answer: A**

**Explanation:** Work group by group — never average the percentages directly. Mobile completions: 80% of 25 = 0.8 × 25 = 20, so 25 − 20 = 5 mobile participants failed. Desktop completions: 60% of 15 = 0.6 × 15 = 9, so 15 − 9 = 6 desktop participants failed. Total failures: 5 + 6 = 11. Total completions: 20 + 9 = 29 out of 40, and 29 ÷ 40 = 0.725 = 72.5% overall. The tempting shortcut — averaging 80% and 60% to get 70% (option B) — is wrong because the groups are different sizes: the mobile group is larger, so its higher rate pulls the overall figure above the midpoint. This "weighted average" idea is one of the most valuable numeric lessons in this whole guide. You will meet it whenever user research or analytics splits results by group, and interpreting such results correctly is part of representing user needs faithfully rather than accidentally distorting them.

**Question 12 (challenging) — Contrast ratio and audit arithmetic**

Accessibility guidance requires normal-size body text to have a colour contrast ratio of at least 4.5:1 against its background. A contrast-checking tool reports these ratios for four text styles on your page: body text 4.6:1, hint text 3.9:1, link text 4.5:1, button text 7.2:1. Fixing the failing style(s) will take 30 minutes each. Your mentor asks: "How many styles fail, and how long will the fixes take in total?" What do you tell them?

- A) 1 style fails; 30 minutes
- B) 2 styles fail; 60 minutes
- C) 2 styles fail; 30 minutes
- D) 3 styles fail; 90 minutes

**Correct answer: A**

**Explanation:** Apply the threshold to each style, watching the boundary carefully. The rule is "at least 4.5:1", so a ratio equal to 4.5:1 *passes*. Body text 4.6:1 — pass. Hint text 3.9:1 — fail. Link text 4.5:1 — exactly on the threshold, so it passes. Button text 7.2:1 — pass. Exactly one style fails, and one fix at 30 minutes gives a total of 30 minutes — option A. Option B is the trap for readers who treat 4.5:1 as a fail because it doesn't exceed the threshold; as in Question 9, "at least" includes the boundary value. This tiny reading decision changes your answer, your time estimate, and — at work — whether you tell a designer their colour choice must change. Contrast ratios are a lovely example of how accessibility work is partly numeric: the ratio is measurable, the threshold is defined, and careful reading of both gives you a clear, defensible answer to report back.

### Preparation tips

- **Refresh the four basics.** Percentages, averages, ratios, and reading tables cover almost everything at this level. Spend a little time on each until the methods feel automatic, then practise mixing them.
- **Always write your working.** Even for "easy" questions, jot the numbers down. Most lost marks come from mental-arithmetic slips, not misunderstanding. Paper is your friend.
- **Learn the "keep" trick for percentages.** A 40% reduction means you keep 60%; a 25% increase means you have 125%. Multiplying by what remains is faster and safer than subtracting.
- **Say the denominator out loud.** For any percentage change, ask "compared with what?" The original value is almost always the answer, and saying it prevents the most common error in this whole test type.
- **Sense-check every answer.** Before moving on, ask: is this number roughly the right size? If 400 of 500 KB is used, the answer must be "most but not all" — around 80%, not 40% or 98%.
- **Practise with your team's real numbers.** Ask to see the performance dashboard, the test report, or last month's analytics. Reading real tables with a friendly colleague beside you is the best practice there is — and it shows initiative.
- **Use the calculator wisely.** Calculators execute your plan; they do not make the plan. Decide the steps first, then compute them. And re-key any calculation whose result surprises you.

### Common pitfalls to avoid

- **Dividing by the wrong number.** Percentage change uses the *original* value as the denominator. Dividing by the new value is the single most common numeric-test error — and the wrong answer it produces is always among the options.
- **Averaging percentages from different-sized groups.** When groups differ in size, compute actual counts first, then combine. The simple average of the percentages will be one of the traps.
- **Confusing the saving with the remainder.** "How much is saved?" and "how much is left?" are different questions with different answers. Re-read the question's final sentence before answering.
- **Misreading threshold words.** "At least 5%" includes 5%; "more than 5%" does not. Boundary cases are placed in these questions on purpose — check which side of the line they sit.
- **Answering half of a two-part question.** If the question asks for a count *and* a rate, verify both parts against your chosen option. Options are built by pairing one right number with one wrong one.
- **Rushing the table read.** Picking a number from the wrong row or column wastes a correct calculation. Touch the row and column with your cursor or finger before you copy a number out.
- **Spending too long on one question.** If a question is eating your time, make your best elimination-based choice, flag it if the platform allows, and move on. Ten steady answers beat three perfect ones.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A verbal reasoning assessment measures how accurately you understand written information and how carefully you reason from it. In a typical question you read a short passage — in this guide, always a realistic workplace text such as a coding standard, an accessibility policy extract, an email from a mentor, or a sprint note — and then judge statements about it. The most common format asks whether a statement is **True** (the passage says or clearly implies it), **False** (the passage contradicts it), or **Cannot say** (the passage gives too little information to decide either way).

The typical format is an online, timed test of 15 to 25 minutes with 20 to 30 statements spread across several passages. The golden rule is: judge the statement using *only* the passage. Your own knowledge — even correct knowledge — must be set aside. If the passage doesn't say it and doesn't clearly imply it, the answer is "cannot say", even if you happen to know it is true in real life. This feels strange at first and becomes natural with practice.

Why do employers test verbal reasoning for apprentice frontend developers? Because so much of your work arrives as text: tickets, user stories, code review comments, coding standards, service manuals, accessibility guidance, and messages from designers and stakeholders. Your role asks you to listen to the needs of design and business stakeholders and interpret information, and to take part in discussions in a multidisciplinary team. Misreading a ticket wastes a day; misreading a standard ships a defect; misreading a colleague's message strains a relationship. Reading precisely — noticing words like "must", "should", "may", "all", and "some" — is a professional skill, and this assessment measures it directly.

### How this assessment maps to your role

- **Reading comprehension** maps to **Communicating information**: interpreting information from design and business stakeholders starts with understanding exactly what their words do and do not say — no more, no less.
- **True/false/cannot-say discipline** maps to **Programming and build (frontend developer)**: implementing a user interface "using the right standards and tools under the direction of others" means treating written requirements precisely. If the ticket doesn't specify a behaviour, the professional response is to ask, not to assume — which is exactly the "cannot say" instinct.
- **Understanding rule language** maps to **Modern development standards** and **Accessibility**: standards documents use precise modal verbs — "must" (required), "should" (recommended), "may" (optional). Explaining the importance of standards includes reading them at that level of precision.
- **Inference** maps to **User focus (frontend developer)**: user stories describe needs, and you often have to work out what clearly follows from them — and, just as importantly, what does not follow and needs a question back to the researcher or designer.
- **Judging clear writing** maps to **Community collaboration** and **Prototyping**: working in the open, pairing, and giving feedback all depend on writing that others can understand. Recognising clear writing helps you produce it.

### Practice questions

For each question, read the passage, then decide whether the statement is True, False, or Cannot say — using only the passage.

**Question 1 (easy) — Reading a coding standard**

Passage: "All new pages must be built using the team's component library. Existing pages should be migrated to the component library when they are next updated. Custom components may be created where the library has no suitable component, and any custom component must be reviewed by a senior developer before use."

Statement: "A new page may be built without using the component library if the developer prefers their own approach."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** The passage says all new pages *must* use the component library. "Must" means required, with no exception for personal preference. The only flexibility mentioned is creating custom components *where the library has no suitable component* — and even then, a senior review is required. The statement claims a freedom the passage explicitly denies, so it is False. Notice the method: find the sentence that bears on the statement, and compare the strength of the language. "Must" in the passage versus "may… if the developer prefers" in the statement is a direct contradiction. Reading modal verbs precisely is a skill you will use every time you open your team's standards or the service manual.

**Question 2 (easy) — An email from your mentor**

Passage (email): "Hi — great work on the banner component this week. Before our session on Thursday, please read the accessibility guidance I linked, especially the section on focus states. We'll pair on adding keyboard support to the banner. Don't worry if the guidance feels dense — we'll go through it together. Thanks, Priya."

Statement: "Priya expects the apprentice to add keyboard support to the banner before Thursday."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** Look at what the email actually asks for before Thursday: *read the guidance*, especially the focus states section. The keyboard support work is described as something "we'll pair on" — that is, it will happen together, in the Thursday session, not before it. The statement therefore contradicts the email's plan, so it is False. This is a gentle example of a very common trap: the statement reuses the passage's own words ("keyboard support", "banner", "Thursday") but rearranges the timing. Matching words are not matching meaning. At work, misreading an instruction like this could mean spending an evening struggling alone with a task your mentor intended to teach you — so precise reading is also self-kindness.

**Question 3 (easy) — A sprint note**

Passage: "Sprint 14 goal: complete the question pages for the licence application. The team finished 18 of the 20 planned tasks. The two remaining tasks concern error message wording and will move to Sprint 15. User research on the completed pages is scheduled for the first week of Sprint 15."

Statement: "The team completed most of its planned tasks in Sprint 14."

- A) True
- B) False
- C) Cannot say

**Correct answer: A**

**Explanation:** The passage states the team finished 18 of 20 planned tasks. Eighteen out of twenty is clearly "most" — 90%, in fact. The statement is a fair summary of what the passage says, so it is True. Straightforward questions like this exist in every test, and their purpose is partly to check you don't overthink: "cannot say" is not the safe default for every statement, and choosing it when the passage clearly supports the statement is just as wrong as inventing information. The rhythm to build: locate the relevant sentence, check the statement against it, and commit. When the support is explicit and direct, answer True with confidence.

**Question 4 (easy) — An accessibility policy extract**

Passage: "Our service must meet the WCAG 2.2 AA standard. Automated accessibility checks run on every code change. Automated checks catch some, but not all, accessibility issues; manual testing is therefore carried out before each major release."

Statement: "Automated checks catch every accessibility issue before release."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** The passage says directly that automated checks "catch some, but not all, accessibility issues" — that is why manual testing exists. The statement claims the opposite, so it is False. The wider lesson sits in the phrase "some, but not all": quantity words (all, some, none, most) are load-bearing in verbal reasoning, and swapping one for another flips an answer. There is a practical lesson for your accessibility skill too, and it is worth remembering beyond any test: green automated checks are a floor, not a ceiling. Real users with real assistive technology, and manual checks with a keyboard and a screen reader, find what the robots miss. Knowing the limits of your tools is part of understanding accessibility.

**Question 5 (moderate) — A progressive enhancement explainer**

Passage: "Progressive enhancement means building the core of a service with HTML first, so it works for everyone, then adding CSS for presentation and JavaScript for enhanced behaviour. If the JavaScript fails to load or run, users can still complete their task using the HTML core. Some enhancements, such as an autocomplete suggestion list, improve convenience but are not required to complete the task."

Statement: "Under progressive enhancement, a user whose browser fails to run JavaScript will be unable to complete their task."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** The passage states the opposite: "If the JavaScript fails to load or run, users can still complete their task using the HTML core." That sentence directly contradicts the statement, so it is False. Take a moment to see how the wrong answer could tempt you: in many websites that do *not* follow progressive enhancement, broken JavaScript really does break the task — so your real-world experience might whisper "true". But the question is about what *this passage* says, and the passage describes the progressive enhancement approach your role explicitly follows. Setting aside outside knowledge is the discipline being tested. As a bonus, this passage is a genuinely accurate summary of why your role's "HTML first" responsibility exists — so this is one practice question where the test content doubles as revision.

**Question 6 (moderate) — Cannot-say discipline with a ticket**

Passage (ticket): "As a user applying for a parking permit, I need to see clear error messages when I miss a required field, so that I can fix mistakes and complete my application. Acceptance criteria: error messages appear next to the relevant field; error messages are announced to screen reader users; the error summary at the top of the page links to each field with an error."

Statement: "The parking permit form currently shows unclear error messages."

- A) True
- B) False
- C) Cannot say

**Correct answer: C**

**Explanation:** The ticket describes what the user *needs* and what the finished work must do. It never describes the current state of the form. Perhaps the current messages are unclear; perhaps there are no messages at all; perhaps the form is brand new. The passage simply does not say, so the answer is Cannot say. It is tempting to infer that a ticket asking for clear errors implies the current ones are unclear — plausible, but plausible is not stated, and "cannot say" exists precisely for plausible-but-unstated claims. This maps directly to reading user stories at work: a story tells you the need and the acceptance criteria, and anything else you want to know about the current behaviour, you check by looking at the service or asking the team — not by assuming.

**Question 7 (moderate) — Inference from a performance report**

Passage: "This month's performance report: the start page's load time improved after we compressed its images. The form page's load time did not change. The confirmation page was not measured this month because it was being rebuilt. All measurements were taken on a simulated slow mobile connection."

Statement: "The form page's images were compressed this month."

- A) True
- B) False
- C) Cannot say

**Correct answer: C**

**Explanation:** The passage says the *start page's* images were compressed and its load time improved. About the form page, it says only that its load time did not change. Did anyone compress the form page's images? The passage is silent. You might reason "if they had compressed them, the load time would have improved" — but that is an assumption (perhaps the form page has few images, or the change was too small to measure). Silence plus a plausible guess still equals Cannot say. Contrast this with the statement "The confirmation page's load time improved this month" — that would be False-flavoured but actually also Cannot say territory? No: the passage says the confirmation page was *not measured*, so no improvement could be reported — but whether its real-world load time improved is unknown, so that too would be Cannot say. Precision about what was measured versus what happened is a distinction real performance reports depend on.

**Question 8 (moderate) — Judging clear writing**

Passage: A colleague drafts four versions of the same code review comment. The team's guidance says feedback should be specific, kind, and actionable.

1. "This is wrong."
2. "Consider renaming `data2` to `filteredResults` so the variable's purpose is clear — happy to pair on it."
3. "I would never write it like this, but fine."
4. "There might be some naming issues somewhere in this file."

Which comment best follows the team's guidance?

- A) Comment 1
- B) Comment 2
- C) Comment 3
- D) Comment 4

**Correct answer: B**

**Explanation:** Test each comment against the three criteria. Comment 1 is neither specific (wrong how? where?), kind, nor actionable. Comment 3 is vaguely disapproving, mildly unkind, and offers no action. Comment 4 is at least gentle, but "might be… somewhere" is the opposite of specific, and it gives the author nothing concrete to do. Comment 2 names the exact variable, proposes a concrete improvement, explains the benefit ("purpose is clear"), and offers help — specific, kind, and actionable. This question style — judging which text best meets stated criteria — appears in many verbal assessments, and the skill transfers straight into your day: your role asks you to understand the importance of feedback, and soon you will both receive and give it. Comment 2 is the model: name the thing, suggest the change, share the reason, offer support.

**Question 9 (moderate) — A standards document with modal verbs**

Passage: "Developers must not commit secrets, such as passwords or API keys, to the code repository. Developers should write a descriptive message for every commit. Developers may squash related commits before merging. Branch names should follow the pattern `feature/short-description`."

Statement: "A developer who merges without squashing their related commits has broken this standard."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** The passage says developers *may* squash related commits — "may" grants permission, it does not impose a duty. Choosing not to squash is therefore entirely within the standard, and the statement's claim of a breach contradicts the passage's plain meaning, so it is False. Compare the verbs across the passage: "must not" (prohibition — committing secrets is always a breach), "should" (strong recommendation — a poor commit message is a lapse, though the word "broken" would be arguable), and "may" (pure option). Standards and guidance in government digital work use these words deliberately, and reading them correctly tells you what is mandatory, what is advised, and what is your call. When you explain the importance of modern development standards — one of your named skills — this vocabulary is the foundation.

**Question 10 (challenging) — A dense policy extract**

Passage: "Services must publish an accessibility statement. The statement must be reviewed at least annually, and additionally whenever a significant change is made to the service. A statement review need not result in changes to the statement, but the review itself must be recorded. Where a review identifies inaccuracies, the statement must be corrected within 14 days of the review."

Statement: "A service that reviewed its accessibility statement eleven months ago, and has made no significant changes since, is currently in breach of this policy."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** Walk the rules against the facts. The policy requires review "at least annually" — that is, at least once every twelve months. The last review was eleven months ago, which is within the twelve-month window, so the annual requirement is not yet breached. The additional trigger — a significant change to the service — has not occurred, so no extra review was required. Nothing in the facts suggests an uncorrected inaccuracy. On the facts given, the service complies, so the claim of breach is False. The trap is the closeness of "eleven months" to a year: urgency ("they should review soon!") is not the same as breach ("they have broken the rule"). Reading obligations with this precision — what is required, by when, triggered by what — is exactly the skill you will use with accessibility regulations, service standards, and your own team's definition of done.

**Question 11 (challenging) — Multiple statements about one passage**

Passage: "Open by default: our code is published in public repositories unless there is a specific reason not to, such as security-sensitive configuration. Publishing code helps other teams reuse our work and helps the public see how their services are built. Before code is made public, the team checks it for secrets and personal data. Code that cannot be published is documented internally, with the reason recorded."

Statement: "All of the team's code is published in public repositories."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** The passage's first sentence contains its own exception: code is public "*unless* there is a specific reason not to", and the final sentence confirms that some code "cannot be published" and is documented internally instead. So the word "All" in the statement overreaches: the passage describes a default with exceptions, not a universal rule. A default-plus-exceptions is one of the most common structures in policy writing — you met it in the cognitive section too ("must reuse… unless a formal exemption") — and the reliable technique is to scan for "unless", "except", and "where… not". When a statement converts a default into an absolute ("all", "always", "never"), the answer is very often False. This passage also happens to describe your real responsibility to create code that is open by default and easy for others to reuse — including the judgement about what cannot be open, and why recording that reason matters.

**Question 12 (challenging) — Inference and tone in a stakeholder message**

Passage (message from a service designer): "Thanks for the prototype changes. In tomorrow's research sessions we're testing whether users understand the new eligibility questions, so please don't change any wording tonight. Layout tweaks are fine if anything's broken on mobile. We have five participants booked, including two screen reader users, so could you double-check the focus order on the questions page before 9am?"

Statement: "The designer considers testing the wording with users more important tomorrow than having a polished layout."

- A) True
- B) False
- C) Cannot say

**Correct answer: A**

**Explanation:** This one requires inference — a conclusion the passage clearly implies without stating outright. The designer freezes the wording ("please don't change any wording tonight") explicitly *because* tomorrow's sessions test whether users understand the questions; layout changes, by contrast, are permitted only "if anything's broken". Protecting the wording while treating layout as fix-only-if-broken clearly implies wording is tomorrow's priority. That comfortably supports the statement, so it is True. Note where the line sits: a statement like "the designer thinks layout is unimportant" would go too far (they still want mobile working and focus order checked — details that matter to the two screen reader participants). Careful inference accepts what the text clearly implies and refuses what it merely might suggest. Reading stakeholder messages at this level — including the practical to-do hidden inside ("check focus order before 9am") — is precisely your Communicating information skill in action.

### Preparation tips

- **Use only the passage.** The single rule that governs everything: judge each statement against the text in front of you, not your knowledge or experience. Practise saying "where does the passage say that?" before every answer.
- **Learn the load-bearing words.** Modal verbs (must, should, may), quantifiers (all, some, none, most), and exception words (unless, except, only) decide most answers. Underline or note them as you read.
- **Give each option its own test.** True needs clear support; False needs clear contradiction; Cannot say means neither. Run all three tests rather than stopping at the first that feels right.
- **Practise on real documents.** The GOV.UK service manual, your team's coding standards, and accessibility guidance are perfect practice material — read a paragraph, invent a statement, and classify it. Ten minutes of this sharpens you quickly.
- **Read the statement twice.** Statements often reuse the passage's words with one crucial change — a swapped timing, an added "all", a reversed direction. The second read catches what the first missed.
- **Don't fear "cannot say" — or overuse it.** It is the right answer whenever the passage is silent, however plausible the statement. But when the passage clearly supports or contradicts, commit to True or False.
- **Build reading stamina gently.** If long passages tire you, practise with slightly longer texts each week. Stamina, like any skill, grows with steady use — and it will serve you in every ticket and standard you ever read.

### Common pitfalls to avoid

- **Importing outside knowledge.** Knowing frontend development well can hurt you here if you answer from experience rather than the passage. The test measures reading, not trivia — stay inside the text.
- **Treating plausible as true.** "The ticket asks for clear errors, so the current errors must be unclear" is a guess, not a fact. Plausible-but-unstated claims are Cannot say.
- **Missing the exception clause.** Defaults with exceptions ("public unless…") are not absolutes. When a statement says "all" or "always", hunt for the passage's "unless" before answering.
- **Confusing "should" with "must".** A broken recommendation is not the same as a broken requirement. Match the strength of the verb in the statement to the strength in the passage.
- **Confusing "not measured" with "did not happen".** Reports tell you what was observed. Absence of a measurement is not evidence of absence — a subtle distinction tests love and workplaces need.
- **Rushing dense passages.** Slowing down for 20 seconds on a hard passage saves three wrong answers. Dense text rewards a second, structured read: rules first, then facts, then the comparison.
- **Letting tone influence logic.** A friendly email and a stern policy get the same treatment: what exactly do the words say? Warmth or formality changes nothing about True, False, or Cannot say.

## Workplace job-specific situational judgement assessment

### About this assessment

A situational judgement assessment (often called an SJT) presents realistic workplace scenarios and asks you to judge how effective different responses would be. Unlike the other assessments, there is no arithmetic and no logic puzzle — the "right" answers are the ones that reflect good professional judgement for someone at your level, in your kind of organisation.

The typical format is an online test of 20 to 40 minutes with 10 to 20 scenarios. Each scenario describes a situation and offers four or five possible responses. You might be asked to pick the *most effective* response, the *least effective*, to rank all the responses, or to rate each one on a scale. Scoring compares your judgements with those of experienced professionals and the organisation's values. For UK government digital roles, that means the assessment rewards user focus, openness, collaboration, asking for help at the right time, honesty about mistakes, and care for accessibility and inclusion.

For an apprentice, SJTs are arguably the most important assessment of all, because your first year is full of judgement calls that have nothing to do with code: What do I do when I'm stuck? When do I ask for help, and how? What if I spot a mistake — mine or someone else's? How do I respond to feedback that stings? The scenarios in this section are drawn from exactly these moments. A reassuring truth up front: SJTs at apprentice level are not looking for heroics. They are looking for honesty, sensible escalation, willingness to learn, and respect for users and colleagues. If you aim for "honest, helpful, and asks at the right time", you will rarely go far wrong.

### How this assessment maps to your role

- **Asking for help and escalating well** maps to **Programming and build (frontend developer)** — your role says "under the direction of others" for a reason. Knowing when you have been stuck too long, and bringing what you tried to the conversation, is a core apprentice behaviour.
- **Responding to feedback** maps to **Leadership and guidance (frontend developer)** and **Community collaboration** — your role explicitly includes understanding the importance of feedback and of team dynamics. SJT scenarios test whether you treat feedback as a gift or a threat.
- **Honesty about mistakes** maps to **Modern development standards** and team good practice — teams that follow agreed practice fix mistakes fast and blamelessly, and that starts with people who speak up early.
- **User and accessibility awareness** maps to **Accessibility** and **User focus (frontend developer)** — many scenarios hinge on whether you remember the user, especially users with accessibility needs, when a deadline or a colleague pushes the other way.
- **Working with others** maps to **Communicating information**, **Community collaboration**, and **Prototyping** — pairing, discussing options in a multidisciplinary team, and working in the open are all behaviours the scoring key rewards.

### Practice questions

**Question 1 (easy) — Stuck on a ticket**

You have been working on a small CSS change for two hours. You expected it to take thirty minutes. You have tried several approaches and read the documentation, but the layout still breaks on small screens. Your mentor is at their desk. What is the most effective response?

- A) Keep trying on your own — asking for help after only two hours would look bad.
- B) Ask your mentor for help, showing them what you have tried so far.
- C) Move the ticket back to the backlog without telling anyone and pick up a different task.
- D) Post in the team channel that the ticket is impossible and should be redesigned.

**Correct answer: B**

**Explanation:** Option B is the textbook apprentice move, and it is worth understanding why each part matters. Asking after a genuine attempt (you tried approaches and read docs) is not weakness — it is exactly what "working under direction" means, and mentors expect it. Showing what you tried turns the conversation from "do it for me" into "teach me", makes the help faster, and shows respect for your mentor's time. Option A wastes hours protecting an image nobody is grading you on; most mentors would rather you asked at the one-hour mark. Option C hides a problem, which breaks the team's trust and its board. Option D escalates publicly, and with a conclusion ("impossible") you cannot support. The general rule this scenario teaches: struggle briefly, gather evidence of what you tried, then ask the nearest appropriate person. That pattern will serve you for your entire career — senior developers do it too, just with harder problems.

**Question 2 (easy) — You broke something**

Yesterday you merged a small change, following all the team's checks. This morning a designer mentions that the service's footer links look wrong. You investigate and realise your change caused it. Nobody else knows yet. What is the most effective response?

- A) Quietly fix it and say nothing — no harm done if it's fixed quickly.
- B) Tell your mentor or the team straight away, explain what happened, and offer to fix it with support.
- C) Wait to see whether anyone else notices before deciding what to do.
- D) Explain to the designer that the checks passed, so it isn't really your fault.

**Correct answer: B**

**Explanation:** Speaking up immediately is the behaviour every healthy team wants and every SJT rewards. Option B does three things at once: it makes the problem visible so it gets fixed properly (perhaps your quiet fix would miss a second symptom), it shows honesty, and it invites support so the fix is done well. Option A might work out — but if the quiet fix is incomplete, the team later discovers both a bug and a cover-up, and the second is far more damaging to trust. Option C is passive and lets users see a broken footer for longer. Option D confuses blame with information: it is true the checks passed — that is a genuinely useful fact, because it means the team's checks have a gap worth fixing — but leading with self-defence rather than the fix puts your comfort above users and the team. The professional framing you are learning: mistakes are normal; hiding them is the real mistake. Teams that follow modern development practice treat every escaped bug as a chance to improve the checks, not to assign blame.

**Question 3 (easy) — Receiving tough feedback**

In a code review, a senior developer leaves several critical comments on your pull request, including "this duplicates a component we already have — please use `app-notification` instead". You feel embarrassed, because you spent two days building your version. What is the most effective response?

- A) Reply explaining why your version is better, to defend the two days you spent.
- B) Delete the pull request and start again without replying.
- C) Thank them, ask any questions you need to understand the existing component, and make the change.
- D) Ask your mentor to tell the senior developer to be less critical of apprentices.

**Correct answer: C**

**Explanation:** Feeling stung by review comments is universal — and what you do next is what the assessment measures. Option C treats the review as what it is: information that saves you from shipping duplication, plus a pointer to a component you now know exists. Thanking the reviewer keeps the relationship warm; asking questions turns the review into teaching; making the change delivers value. Option A defends sunk cost — the two days are spent whether or not you defend them, and reusing the existing component is genuinely better for the team ("easy for others to reuse" is part of your role's purpose). Option B over-corrects: silently discarding work loses the conversation and the learning. Option D escalates a normal, professionally worded review as if it were unkindness — save escalation for feedback that is actually disrespectful, which this is not. One practical tip from real teams: when a review stings, wait ten minutes before replying. The sting fades; the useful information remains.

**Question 4 (easy) — Pairing gone quiet**

You are pairing with a developer who types very fast and explains little. An hour in, you have mostly watched and are now lost. The session is scheduled for another hour. What is the most effective response?

- A) Keep watching and nod along — interrupting would be rude, and you can look things up later.
- B) Say you are lost, and ask if you can drive (type) for a while so you can learn by doing.
- C) Open your laptop and quietly work on your training course instead.
- D) End the session early, saying you have another meeting.

**Correct answer: B**

**Explanation:** Pairing exists so that both people engage — your role summary literally names pair working as part of an open, collaborative environment. Option B is honest about being lost (which the other developer probably has not noticed — fast typists rarely do) and proposes a concrete fix: swapping the driver role, which is standard pairing practice and forces a learning pace. Most colleagues respond warmly to exactly this request. Option A wastes the second hour and teaches the other developer nothing about pairing with apprentices; "I'll look it up later" rarely survives contact with the backlog. Options C and D are quiet withdrawals — one dishonest by omission, one dishonest outright — and both leave the real problem (a pairing style that isn't working) in place for next time. The transferable lesson: in collaborative settings, name the problem gently and offer a mechanic to fix it. "I'm lost — can I drive for a bit?" is eight words and solves everything.

**Question 5 (moderate) — Deadline pressure versus accessibility**

Your team is finishing a page for a ministerial announcement tomorrow. You notice the new page's images have no alternative text, which the team's standards require. The developer leading the work says: "No time — we'll add alt text next sprint. It's just decorative stuff anyway." You are not sure all the images are decorative; one seems to show important information. What is the most effective response?

- A) Say nothing — the lead developer has made the call, and they outrank you.
- B) Add the alt text yourself after hours without telling anyone.
- C) Point out the informative image specifically, and suggest at least that one needs alt text before release; offer to write it now.
- D) Report the lead developer to your line manager for planning to break accessibility standards.

**Correct answer: C**

**Explanation:** This scenario tests whether you can hold an accessibility line politely, proportionately, and at your level. Option C does exactly that: it narrows the disagreement to the specific image that matters (the informative one — a genuinely different case from decorative images, which can legitimately have empty alt text), it explains why, and it offers to do the work, which converts an objection into help and makes "no time" much weaker. That is championing users within your actual authority. Option A confuses hierarchy with correctness — apprentices are junior, but users with screen readers who miss key information on a ministerial announcement are the ones harmed, and your role asks you to build understanding of accessibility, which includes speaking up. Option B fixes one instance while hiding the disagreement, teaches the team nothing, and sets a lonely precedent. Option D leaps to formal escalation before trying the direct, friendly route — escalation is for when the direct route fails, and even then it would start with your mentor, not a report. Notice the SJT pattern: the best answer usually fixes the problem *and* preserves the relationship *and* stays at your level.

**Question 6 (moderate) — A confusing user story**

You pick up a ticket that says: "Update the date input so it works properly." There are no acceptance criteria, and you can think of at least three things "properly" might mean. The ticket was written by a business analyst who is in meetings all morning. Stand-up is finished. What is the most effective response?

- A) Guess the most likely meaning and build it — you can always redo it.
- B) Post a short, specific question to the analyst asynchronously (listing your three interpretations), and work on another ticket until they reply.
- C) Wait at the analyst's desk until they come out of meetings.
- D) Ask your mentor to rewrite the ticket, since apprentices shouldn't work from unclear tickets.

**Correct answer: B**

**Explanation:** Option B shows precisely the communication habits your role names: interpreting stakeholder needs, and asking rather than assuming. Listing your three interpretations is the crucial detail — it converts a vague "what does this mean?" (which the analyst must schedule time to unpack) into a thirty-second multiple-choice question, and it demonstrates you have already thought. Switching to another ticket keeps you productive while you wait, which respects the sprint. Option A risks building the wrong thing; "we can redo it" spends the team's time on your guess and may also confuse users if it ships. Option C spends your morning as a human notification and pressures the analyst the moment they emerge. Option D outsources a conversation you are entirely capable of having — asking clarifying questions *is* apprentice-level work, and doing it well builds exactly the stakeholder relationships you will rely on later. The reusable pattern: when a request is ambiguous, reply with named options, not open questions, and keep delivering meanwhile.

**Question 7 (moderate) — Credit for your work**

In a show-and-tell, a developer demonstrates a component you built most of during pairing sessions, and says "I put this together last week", without mentioning you. You feel invisible. What is the most effective response?

- A) Interrupt the demo to correct the record in front of everyone.
- B) Say nothing and quietly resent it — apprentices don't get credit anyway.
- C) Afterwards, mention to the developer privately that you'd appreciate being credited for shared work, assuming good intent.
- D) Email the head of the team explaining that your work was stolen.

**Correct answer: C**

**Explanation:** Team dynamics questions reward proportionate, direct, low-drama responses. Option C is exactly that: private (no public embarrassment), prompt (soon after the event), assumes good intent (the developer very likely spoke carelessly rather than maliciously — "I put this together" is often thoughtless shorthand), and states the need plainly. In most real cases the colleague apologises and corrects it at the next opportunity. Option A makes a small wrong into a public scene, damaging the demo, the colleague, and — fairly or not — how the room remembers you. Option B corrodes the relationship silently and teaches the colleague nothing; resentment is a poor substitute for a sentence. Option D escalates to the top with the most inflammatory framing ("stolen") before trying a two-minute conversation. The professional skill here — raising interpersonal issues early, privately, and kindly — is part of understanding team dynamics and feedback, and it is far easier to learn as an apprentice than to retrofit as a senior.

**Question 8 (moderate) — Asked to skip the tests**

A developer on your team is hurrying to finish a change before their holiday and asks you: "Can you merge my branch for me this afternoon? The tests keep failing on something unrelated — just skip them, it'll be fine." Merging without passing tests is against the team's agreed practice. What is the most effective response?

- A) Do it — they are more senior, and they said the failures are unrelated.
- B) Refuse and report them to the team lead for asking.
- C) Decline to skip the tests, and offer to help look at the failures or to ask your mentor how the team handles "unrelated" test failures.
- D) Say yes, but secretly not do it, so the problem goes away when they leave.

**Correct answer: C**

**Explanation:** This is a classic "agreed practice under social pressure" scenario, and the scoring key wants to see that you hold the practice *and* stay helpful. Option C declines the rule-break politely, then immediately offers two constructive paths: investigating the failures (perhaps they really are unrelated, in which case the team likely has a proper procedure — fixing or explicitly quarantining the flaky test — rather than skipping the whole suite) and involving your mentor, which is the right move whenever a senior colleague asks you to bypass agreed practice and you feel the pressure of the seniority gap. Option A follows seniority over standards; note that "the failures are unrelated" is exactly what the tests exist to verify, not assume. Option B jumps to reporting over a request that a conversation can resolve — escalate if the pressure continues, not as the first move. Option D is dishonest in both directions and leaves the change in limbo while its author is away. Rule of thumb: when asked to bypass practice, decline the bypass, offer real help, and involve your mentor early — that combination is respectful to everyone, including the person asking.

**Question 9 (moderate) — Spotting a struggling peer**

Another apprentice on a neighbouring team seems withdrawn lately. Today they tell you privately: "I'm completely lost on my project, my mentor is always busy, and I'm scared to say anything in case they end my apprenticeship." You are their peer, not their manager. What is the most effective response?

- A) Reassure them that everyone feels lost and it will pass.
- B) Listen, share that asking for help is normal and expected (perhaps with your own example), and encourage them to talk to their mentor or apprenticeship coordinator — offering to help them plan what to say.
- C) Tell their mentor yourself the next day so the problem gets fixed.
- D) Advise them to keep quiet and quietly search for a different job.

**Correct answer: B**

**Explanation:** Peer-support scenarios test empathy plus respect for boundaries. Option B does the three right things in order: listen first (being heard reduces the fear itself), normalise help-seeking (your own "I asked my mentor after two hours on a CSS bug" story is powerful, because it converts an abstract reassurance into evidence), and guide them toward the proper channels — mentor or apprenticeship coordinator — while leaving the choice and the telling to them. Offering to help plan the conversation is practical support that keeps their agency intact. Option A is kind but empty: it neither reduces the isolation nor moves them toward help. Option C, though well-intentioned, breaks a confidence they explicitly shared privately; except where someone's safety is at risk, the information is theirs to share, and going around them may confirm their fear that speaking up is dangerous. Option D is corrosive advice that abandons every support system designed for exactly this situation. Collaboration skills include caring for the people around you — and doing it in a way that empowers rather than overrides them.

**Question 10 (challenging) — Research findings you didn't want**

You spent two weeks building an animated progress indicator you are proud of. In usability testing, several participants — including one screen reader user and one participant with a vestibular condition who found the motion uncomfortable — struggled with it. The user researcher recommends removing the animation and simplifying the component. What is the most effective response?

- A) Argue that two weeks of work shouldn't be thrown away for a small sample of participants.
- B) Accept the findings, ask the researcher questions to understand the problems fully, and work with the interaction designer on a simpler, accessible version — salvaging anything from your work that still fits.
- C) Suggest keeping the animation but adding a setting so users can turn it off if they complain.
- D) Accept the change but privately decide research sessions are unfair to developers.

**Correct answer: B**

**Explanation:** This scenario sits at the heart of user-centred development: what happens when evidence contradicts effort. Option B is the professional response chain — accept, understand, collaborate, salvage. Asking questions ("what exactly confused the screen reader user? was it the announcements or the structure?") turns a painful verdict into precise learning you will apply to every future component. Working with the designer honours the multidisciplinary approach your role names, and salvage is often real: the underlying logic or markup may survive in the simpler version. Option A weighs your two weeks against users' actual struggle — and small usability samples finding *consistent* problems are exactly how research works; three of five participants struggling is a signal, not noise. Option C keeps the harm as the default and pushes the burden onto affected users to find a setting; accessible-by-default is the standard in government services (and respecting reduced-motion preferences would be a floor, not a fix, when the component confused screen reader users too). Option D complies outwardly while quietly rejecting the principle — and SJTs, like careers, are shaped by what you actually believe about users. The mindset to take away: research findings about your work are findings about the *work*, never about your worth.

**Question 11 (challenging) — An impossible estimate**

In sprint planning, the delivery manager asks how long a small component will take you. You genuinely don't know — you have never built anything like it — but the room is waiting and a senior developer whispers "just say two days". What is the most effective response?

- A) Say "two days" — the senior developer knows best, and you can apologise later if it takes longer.
- B) Say you don't know, and stop there.
- C) Say you haven't built one before, give a range with your best reasoning, and offer to timebox a half-day investigation to firm the estimate up.
- D) Ask the delivery manager to assign the component to someone more experienced instead.

**Correct answer: C**

**Explanation:** Estimation under uncertainty is a judgement skill, and the assessment looks for honesty *with* usefulness. Option C is honest about inexperience (which calibrates everyone's expectations), still offers something the planner can use (a reasoned range — "somewhere between two and five days, because the styling looks simple but I've not done the keyboard interactions before"), and proposes a standard, genuinely professional technique: a timeboxed spike to convert unknowns into knowledge. Delivery managers consistently prefer this to confident guesses. Option A borrows someone else's number without their context; when it takes six days, the plan and your credibility both suffer — and "the senior said so" will not comfort anyone. Option B is honest but leaves the planner with nothing; honesty plus effort beats honesty alone. Option D retreats from a growth opportunity that is entirely appropriate for an apprentice with support — and sprint planning is exactly where you can ask for that support ("could I pair with someone on the keyboard part?"). The wider lesson: "I don't know, and here is how I'll find out" is one of the most trusted sentences in software delivery, at every level of seniority.

**Question 12 (challenging) — Least effective: the open-source shortcut**

Your team's standard says code must be open by default and reusable, and dependencies must be checked before adoption. You find an unmaintained third-party script (last updated years ago, no licence file) that solves your ticket instantly. Rank aside — which of these responses would be the *least* effective?

- A) Ask your mentor whether the team has an approved way to solve this problem, mentioning the script you found.
- B) Copy the script's code into the project without attribution, since it is only a small file.
- C) Look for an equivalent in the team's existing component library or a well-maintained library the team already uses.
- D) Post in the team channel asking if anyone has solved this problem before.

**Correct answer: B**

**Explanation:** Least-effective questions flip your usual thinking: you are hunting for the option that most damages users, the team, or trust. Option B is that option, and on several counts at once. Copying code with no licence file means the team has no legal right to use it — a genuine compliance risk for a government service. Copying without attribution hides the code's origin, so nobody can check it for security issues or track upstream fixes; and an unmaintained script is precisely where such issues live. It also bypasses the team's stated dependency checks — an agreed practice, not a suggestion. Options A, C, and D are all effective, and notice they share a shape: they use the team's collective knowledge before adopting outside code. C is arguably the strongest first move (reuse is your role's explicit value), A brings judgement to your mentor with evidence, and D taps the wider team — but the question only asks for the least effective, so do not agonise over ranking the good ones. Exam technique for least-effective questions: look for irreversibility, hidden information, broken rules, and harm to users — the option collecting the most of those is your answer.

### Preparation tips

- **Anchor on the values.** For every scenario ask: what would an honest, user-focused, collaborative person do here? UK government digital values — users first, working in the open, inclusion, asking for help early — are the scoring key's backbone.
- **Remember your level.** The best apprentice answers involve support: asking with evidence, offering to help, involving a mentor at the right moment. Answers where you act entirely alone — or push everything upward instantly — usually score poorly.
- **Look for the option that does three things.** Strong responses tend to fix the immediate problem, protect the relationship, and improve things for next time. Options that manage only one of the three are rarely "most effective".
- **Practise the least-effective flip.** Weak options cluster around hiding, guessing, public confrontation, and rule-breaking under pressure. Learn those clusters and the least-effective half of each question becomes quick.
- **Rehearse your real repertoire.** Before an assessment, recall times you actually asked for help, owned a mistake, or raised a concern kindly. Fresh memories calibrate judgement better than abstract rules — and they double as interview stories.
- **Read the whole scenario.** Details like "you are not sure all the images are decorative" or "no licence file" are placed deliberately and often decide the answer. SJTs reward careful reading as much as good values.
- **Don't answer as a hero or a robot.** The scoring key wants a realistic, decent colleague — not someone who fixes everything alone at midnight, and not someone who quotes rules without helping anyone.

### Common pitfalls to avoid

- **Choosing silence to be polite.** Saying nothing about a problem — a bug, a missing credit, an accessibility gap — almost always scores badly. Politeness and speaking up are compatible; the strong options do both.
- **Confusing seniority with correctness.** "They outrank me" is never, by itself, a reason to skip tests, drop accessibility, or stay quiet. The strong options respect seniors *and* hold the standard, usually by offering help.
- **Escalating first, talking never.** Reporting a colleague before trying a direct, kind conversation reads as relationship-destroying. Escalation is the right second step, rarely the right first one.
- **Fixing things secretly.** After-hours stealth fixes and quiet cover-ups solve today's symptom while hiding the problem from the team. Openness is the value being tested — including openness about your own mistakes.
- **Defending sunk cost.** Two days or two weeks of your effort never outweigh user evidence or existing reusable components. The assessment — and your team — rewards letting go gracefully and salvaging what fits.
- **Guessing instead of asking.** Building on top of an assumption, or echoing someone else's estimate, feels productive and scores poorly. "Here are my three interpretations — which did you mean?" is the apprentice power move.
- **Forgetting the user in the room.** When a scenario mentions a screen reader user, a deadline, and a senior opinion, the user detail is rarely decoration. Options that quietly sacrifice users for convenience are reliably wrong.

## Conclusion

Well done — you have worked through a full set of practice materials covering all four assessment types you are likely to meet as an apprentice frontend developer: cognitive ability, numeric reasoning, verbal reasoning, and situational judgement. That is a genuine achievement, and it deserves a moment of recognition before you close this guide.

Along the way, you practised far more than test technique. You checked CSS class names and heading levels character by character. You applied browser support rules and merge checklists exactly as written. You calculated page-weight budgets, pass rates, weighted completion rates, and contrast thresholds, step by step. You read coding standards, tickets, emails, and policy extracts with precision, learning to respect the difference between "must", "should", and "may" — and between what a passage says and what it merely suggests. And you weighed realistic judgement calls: when to ask for help, how to own a mistake, how to hold an accessibility line kindly, and how to receive feedback that stings. Every one of those exercises maps directly onto the skills your apprenticeship is building: accessibility, communicating information, community collaboration, leadership and guidance, modern development standards, programming and build, prototyping, user focus, and web performance optimisation.

A few encouragements as you move forward. First, remember that assessment performance is itself a skill, and skills grow with practice. If some questions caught you out today, that is the practice doing its job — revisit the explanations, notice the recurring patterns (denominators, threshold words, checklists, the ask-with-evidence habit), and try similar questions again in a week. You will be surprised how much sticks. Second, treat the preparation tips as professional development, not just exam tactics: the habits these assessments reward — careful reading, honest estimates, early questions, user focus — are exactly the habits that will turn you into a junior developer, and eventually a senior one. Third, be confident in what you already bring. Every day at work you pair, you check, you learn, and you build things real people use. Assessments simply sample, in miniature, what you are already learning to do.

If a real assessment is coming up, find out the provider, format, and timing in advance, complete any official practice questions offered, and look after the basics: sleep, a quiet space, water, and a steady pace. During the test, use the methods you practised here — read slowly where it matters, write your working, check every rule, and choose the honest, helpful option.

And whatever the outcome, keep going. Ask questions generously, volunteer for the tasks that stretch you, keep building your understanding of accessibility and performance, and be kind to yourself on the hard days — every developer you admire once sat exactly where you are sitting now. Good luck — you are better prepared than when you started reading.
