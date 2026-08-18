# Junior Accessibility Specialist - Psychometric Assessment Resources

## Introduction

Welcome! This guide has been written especially for you as a junior accessibility specialist working within the UK Government Digital and Data profession. You might be preparing for an internal assessment, applying for your next role, or simply wanting to understand how psychometric tests connect to the work you do every day. Whatever brought you here, this document will help you practise, build confidence, and feel ready.

First, a friendly reassurance: psychometric assessments are not designed to catch you out. They are structured, standardised exercises that measure the thinking skills and workplace judgement that predict success in a role. For a junior accessibility specialist, that means the tests are not abstract brain-teasers with no connection to your job. The best assessments use the materials you genuinely handle — automated accessibility scan results, WCAG success criteria, simple HTML snippets, test scripts, and messages from your team — and the decisions you genuinely make, such as spotting a missing alt attribute, following a test script carefully under supervision, or knowing when to ask your mentor for help.

Why do these assessments matter for your role in particular? As a junior accessibility specialist, you are learning on the job by assisting with accessibility testing. You work under supervision, you use different types of testing, and you are building your knowledge of standards, legislation, and basic HTML, CSS, and JavaScript. You also bring the voice of disabled users into your team's work, which is one of the most important things anyone in government digital services can do. Assessments of cognitive ability, numerical reasoning, verbal reasoning, and situational judgement map directly onto those demands. Practising them sharpens exactly the skills your role depends on: noticing patterns in scan results, checking a contrast ratio calculation, reading a WCAG success criterion carefully, and choosing the most sensible action when you find a serious issue during testing.

This document is organised into four main assessment sections. Each one follows the same friendly pattern:

- an overview of what the assessment measures and how it usually works
- a mapping of the assessment's dimensions to the specific skills in your role summary
- a set of practice questions with full worked explanations, starting easy and building up gently
- practical preparation tips
- common pitfalls and how to avoid them

Here is how to get the most from this guide. First, read each "About this assessment" section so the format holds no surprises. Second, try each practice question honestly — write down your answer before you peek at the explanation. Third, treat every explanation as a mini-lesson: even when you get a question right, the walkthrough will strengthen your technique. Fourth, do not rush. This is practice, not a race. If a question feels hard, that is completely normal — hard questions are included on purpose so the real test feels easier by comparison.

One last thing before we begin: nobody expects a junior specialist to know everything. Your role is about learning, asking good questions, and doing careful supervised work. The assessments respect that. Take your time, be kind to yourself, and enjoy the practice. Let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive ability assessment measures the exact mental processes your role demands, using practical workplace scenarios rather than abstract puzzles. Instead of asking you to rotate shapes or complete number squares with no context, it presents you with the everyday materials of your job — accessibility scan reports, snippets of HTML, WCAG checklists, test scripts, and simple page structures — and asks you to reason quickly and carefully about them.

The typical format is an online, timed test lasting 15 to 30 minutes, with somewhere between 15 and 30 questions. The questions cover pattern recognition, logical deduction, error checking, prioritisation, and applied problem solving. Scoring is objective: your answers are compared against a norm group of people at a similar level, so you are not being measured against senior experts. Many modern platforms are adaptive, which means the difficulty adjusts based on your previous answers — so if the questions feel like they are getting harder, that is usually a good sign, not a bad one. Employers often receive a breakdown of speed versus accuracy rather than a single number, so working both steadily and carefully matters more than racing through. You will normally be offered a few ungraded practice questions before the real test starts, so you can get comfortable with the screens without any pressure.

For a junior accessibility specialist, cognitive assessment is particularly relevant because your core daily work is careful, structured checking. When you perform basic automated and manual checks on websites and documents, you are doing pattern recognition and error checking in miniature, dozens of times a day: does this image have alt text, does this heading order make sense, does this form label match its input? A well-designed cognitive assessment simulates precisely those demands. Practising it will genuinely make you better at the job, not just better at the test.

### How this assessment maps to your role

The assessment dimensions map directly to the named skills in your role summary:

- **Pattern recognition** maps to your **Technical understanding (accessibility)** skill: performing basic automated and manual checks means spotting recurring accessibility issues — missing alt attributes, skipped heading levels, unlabelled form fields — across many pages, and noticing when something breaks the expected pattern.
- **Logical deduction** maps to **Technical understanding (accessibility)** and **Testing**: knowing some details of the standards and legislation, and knowing where to find more information, means reasoning correctly from a rule (such as a WCAG success criterion) to what it does and does not require in a specific case.
- **Error checking** maps to **Testing**: correctly executing test scripts under supervision depends on following each step exactly, noticing when an actual result differs from an expected result, and recording findings accurately so others can rely on them.
- **Prioritisation** maps to **Consultancy** and **Testing**: working under guidance to identify what advice or recommendations might be appropriate includes recognising which findings matter most — a blocker that stops a screen reader user completing a task matters more than a minor cosmetic issue.
- **Problem solving** maps to **Communicating information** and **User focus**: when you listen to the needs of design and business stakeholders, interpret information, and connect findings back to user needs and user stories, you are decomposing a problem and communicating the pieces clearly.

### Practice questions

**Question 1 (easy) — Pattern recognition in scan results**

You run an automated accessibility checker across five pages of a service. The tool reports the count of "images missing alternative text" per page:

- Home page: 0
- Start page: 0
- Question page: 0
- Check answers page: 7
- Confirmation page: 0

What is the most sensible first thought about this pattern?

- A) The checker is broken, because most pages report zero.
- B) The check answers page is worth a closer look — it may use a different template or a recent change may have introduced the issue.
- C) All five pages need to be rebuilt from scratch.
- D) Seven missing alt texts is normal and needs no action.

**Correct answer: B**

**Explanation:** Four pages cluster at zero and one page stands out with seven issues. That is an outlier, and an outlier is a prompt to investigate, not a conclusion. A likely explanation is that the check answers page uses a different template or component — perhaps a summary list with icon images — or that a recent change touched only that page. Option A jumps to blaming the tool without evidence; zeros are perfectly plausible for well-built pages. Option C is a massive over-reaction. Option D ignores a real accessibility barrier: an image without alternative text is invisible to a screen reader user. In your day-to-day checks, spotting the page that breaks the pattern, then investigating why, is exactly how you turn a scan report into a useful finding.

**Question 2 (easy) — Logical deduction from a WCAG rule**

Your mentor reminds you of this rule: "Every form input must have a visible label that is programmatically associated with the input." During a manual check, you find a search box that has a visible label next to it. Based only on this information, which conclusion is safe?

- A) The search box passes the rule.
- B) The search box fails the rule.
- C) You cannot tell yet — you still need to check whether the visible label is programmatically associated with the input.
- D) Search boxes are exempt from labelling rules.

**Correct answer: C**

**Explanation:** The rule has two parts joined by "and": the label must be visible, and it must be programmatically associated (for example, using a `label` element with a `for` attribute matching the input's `id`). You have confirmed the first part only. A label that sits next to a box visually but is not associated in the code will not be announced by a screen reader when the user focuses the input. So you cannot yet say pass or fail — you need to inspect the code or test with assistive technology. Option D invents an exemption that does not exist. This question rewards a habit that will serve you well in testing: check every part of a rule before recording a result, and never assume the invisible part is fine just because the visible part looks right.

**Question 3 (easy) — Error checking a test script step**

Your test script says: "Step 4: Using only the keyboard, press Tab until focus reaches the 'Continue' button, then press Enter. Expected result: the next page loads." You perform the step. Focus reaches the 'Continue' button, you press Enter, and nothing happens. What should you record?

- A) Pass, because focus reached the button.
- B) Fail, with a note of the actual result: focus reached the button but pressing Enter did not load the next page.
- C) Nothing — skip the step and move on.
- D) Fail, and rewrite the test script so the step is easier.

**Correct answer: B**

**Explanation:** The expected result was "the next page loads", and the actual result was that nothing happened. That is a fail, and it is an important one: a button that cannot be activated by keyboard blocks every user who cannot use a mouse. The correct record includes both the outcome and a clear note of what actually happened, because your supervisor and the developers will rely on your notes to reproduce and fix the issue. Option A confuses reaching the button with activating it — two different checks. Option C would hide a genuine barrier. Option D muddles roles: as a junior specialist you execute scripts under supervision and report problems with them, but you do not quietly rewrite the script mid-test, because that would make your results impossible to compare with anyone else's. Accurate, honest recording is the heart of the **Testing** skill.

**Question 4 (easy) — Prioritising findings**

At the end of a testing session you have four findings. Your supervisor asks which one you would raise first. Which is most urgent?

- A) A decorative border image has a slightly outdated colour.
- B) The main navigation cannot be reached using the keyboard at all.
- C) One paragraph uses a slightly informal tone.
- D) A page title could be a little more descriptive.

**Correct answer: B**

**Explanation:** The navigation issue is a blocker: a keyboard-only user — which includes many screen reader users, people with motor impairments, and people with some temporary injuries — cannot move around the service at all. That prevents task completion, which is the most serious category of accessibility issue. The other three findings are worth noting, but none of them stops anyone completing their task. When you prioritise, ask: "Who is blocked, and from doing what?" The bigger the block and the more people affected, the higher the priority. This mirrors the guidance you will see in your team's severity ratings, where issues that prevent task completion for assistive technology users sit at the top.

**Question 5 (moderate) — Pattern recognition in HTML headings**

You are checking the heading structure of a page. The headings, in order, are:

1. `<h1>` Apply for a Blue Badge
2. `<h2>` Before you start
3. `<h2>` What you will need
4. `<h4>` Proof of identity
5. `<h2>` How to apply

Which heading breaks the expected pattern?

- A) Heading 2
- B) Heading 3
- C) Heading 4
- D) Heading 5

**Correct answer: C**

**Explanation:** Headings should form a logical outline without skipping levels downwards. The page moves from `h1` to `h2` correctly, but heading 4 jumps from `h2` straight to `h4`, skipping `h3`. "Proof of identity" is a sub-topic of "What you will need", so it should be an `h3`. Skipped heading levels confuse screen reader users who navigate by headings, because the structure implies a level of nesting that does not exist. Headings 2, 3, and 5 are all `h2` sections under the `h1`, which is fine — sibling sections at the same level are normal. Spotting sequence breaks like this is one of the most common manual checks you will perform, and it is pure pattern recognition: learn the rule, scan the sequence, find the break.

**Question 6 (moderate) — Logical deduction about testing types**

Your team uses this rule of thumb: "Automated checks can find roughly 30 to 40 per cent of accessibility issues; the rest need manual checks or assistive technology testing." A colleague says: "Our automated scan came back clean, so the page is accessible." Which response is most accurate?

- A) Agree — a clean automated scan means the page is accessible.
- B) Disagree — a clean scan is good news, but most issue types can only be found by manual and assistive technology testing, so more checks are needed.
- C) Disagree — automated scans are useless and should be abandoned.
- D) Agree — but only if the scan was run twice.

**Correct answer: B**

**Explanation:** The rule of thumb tells you automated tools catch only a minority of issue types. Things like whether alt text is actually meaningful, whether the focus order makes sense, whether error messages are helpful, and whether the page works with a screen reader all need human judgement. So a clean scan is a good start — it means the machine-detectable issues are absent — but it cannot support the conclusion "the page is accessible". Option A over-claims; option C throws away a genuinely useful tool (automated scans are fast, repeatable, and great at catching regressions); option D adds a condition that changes nothing. Understanding what each type of testing can and cannot tell you is central to your "understand and use different types of testing" responsibility, and this exact deduction — clean scan does not equal accessible — is one you will make many times.

**Question 7 (moderate) — Error checking a findings table**

You are tidying a findings table before sending it to your supervisor. The team's convention is: each row must have a unique ID in the format "A11Y-" plus a three-digit number, a WCAG reference, and a severity of High, Medium, or Low. The draft rows are:

| ID | WCAG reference | Severity |
|---|---|---|
| A11Y-001 | 1.1.1 | High |
| A11Y-002 | 2.4.6 | Medium |
| A11Y-02 | 1.4.3 | High |
| A11Y-004 | 3.3.2 | Urgent |

How many rows break the convention?

- A) 0
- B) 1
- C) 2
- D) 3

**Correct answer: C**

**Explanation:** Check each row against each part of the convention. Row 1: ID format correct, WCAG reference present, severity "High" is allowed — fine. Row 2: all parts fine. Row 3: the ID "A11Y-02" has only a two-digit number, breaking the three-digit format — one defect. Row 4: the ID and WCAG reference are fine, but "Urgent" is not one of the three allowed severity values — a second defect. So two rows break the convention. Conventions like this can feel fussy, but they matter: consistent IDs let developers, testers, and project managers refer to the same issue without confusion, and consistent severity values let issues be sorted and counted reliably. Careful, methodical checking of every field against every rule — without skimming — is exactly the discipline that makes your findings trustworthy.

**Question 8 (moderate) — Applied problem solving with alt text**

You are checking images on a news page. Four images have these alt attributes:

1. A photo of the minister opening a new office: `alt="Photo"`
2. A decorative swirl used as a section divider: `alt=""`
3. A chart showing complaint numbers falling from 400 to 150: `alt="Chart"`
4. The department's logo in the page header, which links to the home page: `alt="Department for Work and Pensions home"`

Which images have appropriate alternative text?

- A) 1 and 3
- B) 2 and 4
- C) 1, 2, and 4
- D) All four

**Correct answer: B**

**Explanation:** Work through each image against the purpose it serves. Image 1's alt text "Photo" tells a screen reader user nothing about the content; it should describe what matters, such as "The minister opening the new Leeds office". Image 2 is decorative, and empty alt text (`alt=""`) is exactly right for decorative images — it tells screen readers to skip the image silently. Image 3's "Chart" fails for the same reason as image 1, and worse: the chart carries real information, so the alt text should convey the key message, such as "Chart showing complaints fell from 400 to 150 over the year". Image 4 is a linked logo, and its alt text correctly describes the link's destination. So only 2 and 4 are appropriate. The underlying technique is to ask, for every image: what would a user miss if they could not see this? Good alt text supplies exactly that, no more and no less.

**Question 9 (moderate) — Prioritisation of your working day**

It is Tuesday morning and you have four things on your list:

1. Finish executing a test script your supervisor needs results from by the end of today, for a service going to an assessment on Thursday.
2. Reply to a friendly question in the cross-government accessibility community channel about a tool you have used.
3. Read a blog post about a proposed future WCAG version.
4. Re-run last week's automated scan, which is scheduled as a routine monthly task due next week.

Which order is most sensible?

- A) 2, 3, 4, 1 — quick tasks first
- B) 1, 2, 4, 3 — deadline-driven work first, then the community reply, then routine work, then reading
- C) 3, 1, 2, 4 — learning always comes first
- D) 4, 1, 2, 3 — scans before scripts

**Correct answer: B**

**Explanation:** Item 1 is both urgent (needed today) and high impact (it feeds a service assessment on Thursday), so it clearly comes first. Item 2 is quick, helps a colleague, and contributes to the cross-government community — a genuine part of your role — so it fits naturally next, perhaps in a short break from testing. Item 4 is routine and not due until next week. Item 3 is useful professional development with no deadline at all, so it comes last, perhaps at the end of the day. Option A falls into the trap of doing easy things first while a deadline burns; option C treats unscheduled learning as more urgent than a same-day commitment; option D promotes a task due next week above one due today. The pattern to remember: sequence by urgency and impact together, not by which task feels most comfortable.

**Question 10 (hard) — Deduction across multiple test results**

You test a form page three ways, with these results: (i) the automated scan reports zero issues; (ii) keyboard-only testing shows every field can be reached and completed; (iii) when you try the page with a screen reader, the error message "Enter your postcode" is displayed on screen after invalid input, but the screen reader announces nothing. Which statement must be true?

- A) The page has no accessibility issues, because the scan was clean.
- B) The page has at least one accessibility issue that only assistive technology testing revealed.
- C) The keyboard testing was performed incorrectly.
- D) The screen reader software is faulty.

**Correct answer: B**

**Explanation:** Result (iii) shows a real defect: an error message that appears visually but is not announced means a screen reader user has no idea their input was rejected — they may sit waiting, or submit again in confusion. Neither the clean scan (i) nor the successful keyboard test (ii) contradicts this, because each testing type detects different issue categories: the scan checks code patterns, keyboard testing checks focus and operation, and assistive technology testing checks the actual experience. So statement B must be true. Statement A is refuted by (iii). Statements C and D invent faults in the testing rather than the page — and while testers should always double-check surprising results, nothing in the evidence forces either conclusion. This question rehearses the single most important idea in your testing work: different types of testing find different problems, which is exactly why your role summary asks you to understand and use different types of testing.

**Question 11 (hard) — Multi-step reasoning about a fix**

A developer proposes fixing a "focus not visible" issue by adding this CSS: `*:focus { outline: none; }` and then adding a custom focus style only to buttons. The service also contains links, form inputs, and radio buttons. What is the logical consequence of this fix?

- A) The issue is fully fixed for all elements.
- B) Focus becomes visible on buttons but is now completely invisible on links, inputs, and radio buttons — making the overall situation worse for keyboard users.
- C) The fix has no effect at all.
- D) The fix only affects screen reader users.

**Correct answer: B**

**Explanation:** Reason through the CSS step by step. The rule `*:focus { outline: none; }` removes the browser's default focus indicator from every focusable element. The custom style then restores a visible indicator, but only for buttons. Links, text inputs, and radio buttons are focusable too, and they now have no indicator at all — the default was removed and nothing replaced it. So keyboard users can see where they are on buttons but are lost everywhere else, which is worse than the original single complaint. Option D confuses user groups: focus visibility mainly affects sighted keyboard users, not screen reader users, who follow the accessibility tree rather than visual outlines. The deeper lesson, which you will use when communicating findings and fixes, is to always ask of a proposed fix: what does it change for every affected element and every affected user, not just the one in the bug report?

**Question 12 (hard) — Combining rules to reach a verdict**

Your team's severity guide says: (i) an issue is "Critical" if it prevents task completion for any user group; (ii) an issue is "High" if it causes significant difficulty but a workaround exists; (iii) if in doubt between two levels, choose the higher and flag it for your supervisor's review. You find that a "Show password" toggle cannot be operated by keyboard. Users can still type their password without ever using the toggle, but they cannot check what they typed, which causes many failed login attempts for users with dexterity impairments. Which severity should you record?

- A) Critical, with no flag.
- B) High, flagged for supervisor review.
- C) Low, because passwords still work.
- D) No severity — it is not an accessibility issue.

**Correct answer: B**

**Explanation:** Apply the rules in order. Does the issue prevent task completion? Not strictly — users can complete login without the toggle, so rule (i)'s "Critical" does not clearly apply. Does it cause significant difficulty with a workaround? Yes — typing blind and retrying is a workaround, but a poor one that causes many failures for a specific user group, so "High" fits rule (ii). Is there doubt? Reasonably, yes — you might argue that repeated failed logins effectively prevent completion for some users, which edges towards Critical. Rule (iii) says in doubt, choose the higher of the two you are torn between and flag it. Between High and Critical the cautious reading lands on High with a flag, because the workaround genuinely exists; the flag invites your supervisor to upgrade it if they judge the failure rate makes completion practically impossible. Options C and D dismiss a real barrier. This is a realistic piece of supervised judgement: apply the written rules faithfully, and use the escalation route the rules themselves provide when the case sits near a boundary.

### Preparation tips

- **Practise with real materials.** Spend ten minutes a day running an automated checker on a public government page, then manually checking one thing the tool cannot judge — alt text quality, heading order, or focus visibility. This builds exactly the pattern-recognition muscles the assessment measures.
- **Learn the shape of common issues.** Missing labels, skipped headings, missing alt text, invisible focus, unannounced errors: these few patterns cover a large share of real findings. Knowing them cold makes assessment questions feel familiar.
- **Slow down on "must be true" questions.** When a question asks what must follow, check each option against the given facts only. If you need extra assumptions, the option is not safe.
- **Read every part of a rule.** Many questions (and many real WCAG criteria) contain an "and" or an "unless". Train yourself to spot and check each clause separately.
- **Simulate test conditions once or twice.** Set a timer, sit somewhere quiet, and work through a batch of questions without interruptions, so the timed format feels normal on the day.
- **Sleep and settle.** Cognitive test scores genuinely improve with rest. The night before, close the laptop early; on the day, arrive settled, read the instructions fully, and use any ungraded practice questions offered.

### Common pitfalls to avoid

- **Racing.** Junior candidates often believe speed impresses. In fact, most scoring rewards accuracy heavily, and adaptive tests punish careless errors. Work at a steady pace you can sustain.
- **Answering from general knowledge instead of the given information.** If a question describes a team convention or a rule, use that rule — even if your own team does things differently. The test measures reasoning from given facts.
- **Confusing "looks right" with "is right".** A visible label is not necessarily an associated label; a clean scan is not an accessible page. Check the invisible part.
- **Flagging every symptom as a separate issue.** When one root cause produces several symptoms, the sharpest answer identifies the single correction, just as the sharpest audit finding names the root cause.
- **Letting one hard question derail you.** Mark it, make your best choice, and move on. One question is worth a tiny fraction of the total; your composure is worth far more.
- **Skipping the practice questions at the start of the real test.** They are free familiarisation. Use them to settle your nerves and learn the interface.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment measures how well you understand and work with the numbers your role genuinely produces: counts of issues from scans, pass rates from test scripts, contrast ratios, percentages of pages affected, and simple time estimates for testing tasks. It is not a maths exam. You will not need algebra, trigonometry, or anything you have not used since school beyond percentages, ratios, averages, and reading tables and charts. What the test measures is whether you can extract the right numbers from workplace data, do the right simple calculation, and interpret the result sensibly.

The typical format is an online, timed test lasting 20 to 30 minutes with 15 to 20 questions. Each question usually presents a small table, chart, or short description containing numbers, followed by a multiple-choice question. A basic on-screen calculator is usually allowed — check the instructions on the day. As with the cognitive test, scoring compares you with a norm group at your level, and accuracy matters more than raw speed.

Why does this matter for a junior accessibility specialist? Because your findings live in numbers. When you report that an automated scan found 24 issues across 6 pages, or that 3 of 20 test script steps failed, or that a colour pair has a contrast ratio of 3.2:1 against a required 4.5:1, you are handling exactly the kind of data this assessment uses. Getting these numbers right — and understanding what they do and do not mean — makes your findings credible and useful. Getting them wrong sends developers chasing the wrong problems. Practising numeric reasoning is therefore practising a core part of communicating findings and fixes well.

### How this assessment maps to your role

- **Percentages and proportions** map to your **Testing** skill: analysing simple test results means saying what share of steps passed, what share of pages had issues, and how results changed between test runs.
- **Ratios** map to **Technical understanding (accessibility)**: colour contrast is expressed as a ratio (such as 4.5:1), and comparing a measured ratio against a required threshold is one of the most common numeric checks you will perform.
- **Averages and rates** map to **Testing** and **Consultancy**: average issues per page, or issues fixed per sprint, help your team see progress and help you work under guidance to suggest where attention is needed.
- **Reading tables and charts** maps to **Communicating information** and **User focus**: scan reports, survey results, and analytics about assistive technology usage all arrive as tables and charts, and interpreting them accurately is how you listen to stakeholders and bring evidence about users into discussions.
- **Sense-checking** maps to everything: a junior specialist who notices that a claimed "50 per cent improvement" does not match the underlying counts is already showing the careful scepticism that makes a great tester.

### Practice questions

**Question 1 (easy) — Counting issues across pages**

An automated scan of a service reports issues on each page: Home 4, Start 2, Question 6, Review 8, Confirmation 0. How many issues were found in total?

- A) 18
- B) 20
- C) 22
- D) 24

**Correct answer: B**

**Explanation:** Add the counts step by step: 4 + 2 = 6; 6 + 6 = 12; 12 + 8 = 20; 20 + 0 = 20. The total is 20. Simple addition, carefully done, underpins every summary line you will ever write in a findings report — and a wrong total at the top of a report undermines trust in everything below it. When adding a list under time pressure, run the addition twice, ideally once top-to-bottom and once bottom-to-top; if the two totals agree, you can be confident.

**Question 2 (easy) — Pass rate as a percentage**

You execute a test script with 20 steps. 17 steps pass and 3 fail. What percentage of steps passed?

- A) 75%
- B) 80%
- C) 85%
- D) 90%

**Correct answer: C**

**Explanation:** Percentage passed = passes ÷ total × 100. Step by step: 17 ÷ 20 = 0.85; 0.85 × 100 = 85%. A quick sense-check: 10% of 20 is 2, so 3 fails is 15%, and 100% − 15% = 85% — the two routes agree. Reporting pass rates is a standard way to summarise a test run, but remember when you write reports that the 3 failures matter more than the 85% — one of them might be a blocker. The percentage gives the headline; the detail gives the meaning.

**Question 3 (easy) — Comparing a contrast ratio to a threshold**

WCAG requires normal-size body text to have a contrast ratio of at least 4.5:1 against its background. Your checking tool measures four text and background pairs:

- Pair 1: 3.9:1
- Pair 2: 4.5:1
- Pair 3: 7.2:1
- Pair 4: 4.4:1

How many pairs meet the requirement?

- A) 1
- B) 2
- C) 3
- D) 4

**Correct answer: B**

**Explanation:** The threshold is "at least 4.5:1", which means 4.5 exactly counts as a pass. Check each: Pair 1 at 3.9 is below 4.5 — fail. Pair 2 at exactly 4.5 — pass, because "at least" includes the boundary. Pair 3 at 7.2 — comfortably passes. Pair 4 at 4.4 — fails, even though it is close; there is no rounding up to the threshold. So 2 pairs pass. Two habits from this question will serve you daily: read whether a threshold is "at least" or "more than", and never round a failing measurement into a pass — 4.4:1 is a finding, however near the line it sits.

**Question 4 (easy) — Reading a simple table**

Your team logs how issues were found last month:

| Testing type | Issues found |
|---|---|
| Automated scan | 18 |
| Manual checks | 27 |
| Assistive technology testing | 15 |

What fraction of all issues was found by manual checks?

- A) 27/60
- B) 27/45
- C) 18/60
- D) 15/60

**Correct answer: A**

**Explanation:** First find the total: 18 + 27 + 15 = 60. Manual checks found 27, so the fraction is 27/60 (which simplifies to 9/20, or 45%). Option B uses the wrong denominator by leaving out one testing type; options C and D pick the wrong row. The practical lesson: always build the denominator from all the categories the question includes, and notice how the numbers support what your mentor tells you — automated scans found 18 of 60 issues here, or 30%, matching the rule of thumb that most issues need human testing to find.

**Question 5 (moderate) — Average issues per page**

You manually check 8 pages and record the number of issues on each: 3, 5, 2, 0, 6, 4, 2, 2. What is the average (mean) number of issues per page?

- A) 2.5
- B) 3
- C) 3.5
- D) 4

**Correct answer: B**

**Explanation:** Add the issues: 3 + 5 = 8; 8 + 2 = 10; 10 + 0 = 10; 10 + 6 = 16; 16 + 4 = 20; 20 + 2 = 22; 22 + 2 = 24. Then divide by the number of pages: 24 ÷ 8 = 3. The average is 3 issues per page. Note that the page with 0 issues still counts as a page — a common error is to divide by only the pages that had issues (24 ÷ 7 ≈ 3.4), which overstates the average. Averages like this help teams compare services or track improvement over time, but always remember what an average hides: here, one page had 6 issues and one had none, and the page with 6 deserves attention the average alone would never reveal.

**Question 6 (moderate) — Percentage change between scans**

Last month's scan found 40 issues. After a round of fixes, this month's scan finds 26. By what percentage did the issue count fall?

- A) 14%
- B) 26%
- C) 35%
- D) 65%

**Correct answer: C**

**Explanation:** Percentage change = (change ÷ original) × 100. Step by step: the change is 40 − 26 = 14 issues; divide by the original count, 14 ÷ 40 = 0.35; multiply by 100 to get 35%. So issues fell by 35%. Option A reports the raw change (14) as a percentage — a classic slip. Option B just repeats the new count. Option D is the share remaining (26 ÷ 40 = 65%), which answers a different question. Always divide the change by the original value, not the new one, and be ready to say clearly in reports whether you are describing the fall (35%) or the remainder (65%) — both are true, and mixing them up in a summary can mislead your whole team.

**Question 7 (moderate) — Ratio of severities**

A findings report contains 8 high-severity, 12 medium-severity, and 20 low-severity issues. What is the ratio of high to medium to low severity issues, in simplest form?

- A) 8:12:20
- B) 4:6:10
- C) 2:3:5
- D) 1:2:3

**Correct answer: C**

**Explanation:** Start with 8:12:20 and divide every part by the largest common factor. All three numbers divide by 4: 8 ÷ 4 = 2; 12 ÷ 4 = 3; 20 ÷ 4 = 5. So the simplest form is 2:3:5. Option A is correct but not simplified; option B simplifies only by 2; option D looks neat but does not match the numbers (check: 1:2:3 scaled by 8 would give 8:16:24). Simplified ratios make severity mixes easy to communicate — "for every two high issues we have three medium and five low" — which is friendlier for stakeholders than raw counts, and communicating information in a form your audience can absorb is a named part of your role.

**Question 8 (moderate) — Time estimation for a testing task**

Your supervisor asks you to manually check 12 pages. From experience, each page takes you about 25 minutes to check, and you add a 30-minute buffer at the end for writing up notes. Roughly how long should you tell your supervisor the whole task will take?

- A) About 3 hours
- B) About 4 hours
- C) About 5 and a half hours
- D) About 7 hours

**Correct answer: C**

**Explanation:** Checking time = 12 pages × 25 minutes = 300 minutes. Convert to hours: 300 ÷ 60 = 5 hours. Add the 30-minute write-up buffer: 5 hours + 0.5 hours = 5.5 hours. So "about 5 and a half hours" — realistically, most of a working day once breaks and interruptions are included. Options A and B underestimate badly, which is the more dangerous direction: promising 3 hours and needing 5.5 lets your supervisor down and squeezes the quality of your checks. Honest estimates, built from a per-item rate times a count plus a buffer, are a small numeric habit that builds big trust — and it is fine, indeed expected, for a junior specialist to say "this is my estimate; shall I check in at the halfway point?"

**Question 9 (moderate) — Reading a bar chart description**

A slide shows a bar chart of screen reader usage from a survey of 1,200 assistive technology users. The bars read: JAWS 480 users, NVDA 360, VoiceOver 240, Other 120. What percentage of surveyed users used NVDA?

- A) 20%
- B) 25%
- C) 30%
- D) 36%

**Correct answer: C**

**Explanation:** First sense-check the total: 480 + 360 + 240 + 120 = 1,200 — matches the stated survey size, so the chart is internally consistent. NVDA share = 360 ÷ 1,200 = 0.30, so 30%. A quick mental route: 10% of 1,200 is 120, and 360 is three lots of 120, so 30%. Option D (36%) comes from misreading 360 as a percentage — always check whether a chart shows counts or percentages before you quote it. Data like this genuinely shapes your work: knowing which assistive technologies are most used helps your team decide what to test with, which supports your growing knowledge of assistive technology and keeps testing focused on real users.

**Question 10 (hard) — Combining percentages across two rounds**

A service had 60 accessibility issues. In sprint one, the team fixed 40% of them. In sprint two, the team fixed 50% of the issues that remained after sprint one. How many issues are still open after sprint two?

- A) 6
- B) 12
- C) 18
- D) 30

**Correct answer: C**

**Explanation:** Work in stages, and be careful that the second percentage applies to the remainder, not the original. Sprint one: 40% of 60 = 0.4 × 60 = 24 fixed, leaving 60 − 24 = 36. Sprint two: 50% of the remaining 36 = 18 fixed, leaving 36 − 18 = 18 open. The tempting wrong route is to add 40% + 50% = 90% and conclude only 6 issues remain (option A) — but percentages of different bases cannot be added. Option D stops after sprint one. When you report progress across multiple sprints, this distinction genuinely matters: "we fixed 40% then 50%" sounds like 90%, but the true clearance here is 42 of 60, which is 70%. Being the person who quietly gets this right is a real contribution to your team's credibility.

**Question 11 (hard) — Weighted effort across issue severities**

Your team estimates fixing effort as: each high-severity issue takes 4 hours, each medium takes 2 hours, and each low takes 1 hour. A report lists 5 high, 9 medium, and 12 low issues. The team has 40 hours available this sprint and fixes issues strictly in severity order (all high, then medium, then low). How many low-severity issues can be fixed this sprint?

- A) 0
- B) 2
- C) 4
- D) 12

**Correct answer: B**

**Explanation:** Calculate the effort tier by tier. High: 5 × 4 = 20 hours, leaving 40 − 20 = 20 hours. Medium: 9 × 2 = 18 hours, leaving 20 − 18 = 2 hours. Low: each takes 1 hour, so 2 hours covers 2 low-severity issues. The answer is 2. Option D assumes unlimited time; option A forgets the small remainder; option C mis-multiplies the medium tier. This layered calculation — multiply each category by its rate, subtract as you go — mirrors real sprint planning conversations you will sit in, and being able to follow the arithmetic lets you contribute when someone asks, "can we clear the lows this sprint?" (Answer: not this one — ten lows will carry over.)

**Question 12 (hard) — Spotting a misleading summary**

A dashboard claims: "Accessibility improving: issues per page down 50%!" The underlying data shows last quarter's scan covered 10 pages and found 30 issues; this quarter's scan covered 40 pages and found 60 issues. Is the claim's arithmetic correct, and what is the fuller picture?

- A) The claim is arithmetically correct — issues per page fell from 3.0 to 1.5 — but total issues doubled because coverage quadrupled, so the summary needs that context.
- B) The claim is wrong — issues went up from 30 to 60, so nothing improved.
- C) The claim is wrong — issues per page rose.
- D) The claim is correct and complete — no further context is needed.

**Correct answer: A**

**Explanation:** Compute both views. Issues per page last quarter: 30 ÷ 10 = 3.0. This quarter: 60 ÷ 40 = 1.5. The rate did fall by half — (3.0 − 1.5) ÷ 3.0 = 0.5 = 50% — so the claim's arithmetic holds, ruling out B and C. But the total issue count rose from 30 to 60 because the scan now covers four times as many pages; the new pages may include older, less accessible parts of the service. A summary that quotes only the rate invites a rosier reading than the data supports, and one that quotes only the total (as option B does) invites an unfairly gloomy one. The honest report gives both: "Coverage quadrupled; the issue rate per page halved; the total backlog doubled." Reading behind a headline number like this is exactly the sense-checking that makes stakeholders trust the figures you communicate.

### Preparation tips

- **Rebuild your percentage reflexes.** Practise the three core moves until they are automatic: X% of Y, X as a percentage of Y, and percentage change from X to Y. Nearly every workplace numeric question uses one of them.
- **Always identify the base.** Before calculating any percentage, ask "percentage of what?" Most wrong answers in numeric tests come from dividing by the wrong base.
- **Practise with your own data.** Take a real scan report and calculate totals, averages, pass rates, and changes since the last run. Familiar data makes the test format feel like a normal Tuesday.
- **Write the steps down.** Even with a calculator, jot each intermediate result. It prevents slips and lets you check your work in seconds.
- **Sense-check every answer.** Is the result plausible? A pass rate over 100%, an average bigger than the largest value, or a "fall" that produces a bigger number all signal an error worth thirty seconds to find.
- **Use the two-route check.** Where possible, reach the answer a second way (like checking 85% via the 15% fail rate). Agreement between routes is the fastest reliable verification.

### Common pitfalls to avoid

- **Adding percentages of different bases.** 40% fixed then 50% fixed is not 90% fixed. Work each stage on its own base.
- **Confusing counts with percentages.** A bar of 360 users is not 36%. Check axis labels and units before quoting any chart.
- **Rounding a failure into a pass.** 4.4:1 does not meet 4.5:1. Thresholds in accessibility are exact, and so are thresholds in test questions.
- **Dividing by the wrong number of items.** Pages with zero issues still count in an average. Include every item in the denominator.
- **Presenting a rate without its context.** "Issues per page halved" and "total issues doubled" can both be true. In tests, pick the option that captures the full picture; at work, report both numbers.
- **Calculator overconfidence.** The calculator does what you type, including your mistakes. The thinking — choosing the right operation and the right base — is always yours.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment measures how accurately you read, understand, and draw conclusions from written material of the kind your role handles every day: extracts from accessibility standards and regulations, guidance pages, emails from your team, audit findings, and user stories. The classic format presents a short passage followed by statements you must judge as True (the passage supports it), False (the passage contradicts it), or Cannot Say (the passage gives too little information either way). Other question types test inference — what follows from the passage — and clear-writing judgement, such as choosing the plainest way to express a finding.

The typical format is an online, timed test of 15 to 25 minutes with 15 to 25 questions, usually several statements per passage. The discipline it rewards is strict: you answer using only the passage, not your background knowledge. That can feel odd when you know the subject — you may know a fact is true in real life, but if the passage does not support it, the correct answer is Cannot Say.

For a junior accessibility specialist this assessment is highly relevant. Your role summary says you demonstrate knowledge of some details of the standards and legislation and know where to find more information — which in practice means reading dense normative text and extracting exactly what it requires, no more and no less. It also says you communicate findings and fixes: your written words travel to developers, designers, and your supervisor, and precision in reading and writing is what makes those words useful. Finally, you take part in discussions within a multidisciplinary team, where careful listening and accurate interpretation — verbal reasoning in spoken form — happen every day.

### How this assessment maps to your role

- **Reading comprehension** maps to **Technical understanding (accessibility)**: understanding what a WCAG success criterion or a regulation actually requires — including its scope and exceptions — is a reading task before it is a technical one.
- **True/False/Cannot Say discipline** maps to **Testing**: recording only what you observed, without adding assumptions, is the same mental move as answering only from the passage. Both protect the reliability of your findings.
- **Inference** maps to **Consultancy** and **Communicating information**: working under guidance to identify what advice might be appropriate means drawing sensible, supported conclusions from documents and previous work by others — and stopping before you over-claim.
- **Clear-writing judgement** maps to **Communicating information** and **User focus**: explaining an accessibility barrier so a busy developer understands it, or writing a user story that keeps the focus on user needs, both depend on choosing plain, direct wording.
- **Interpreting stakeholder needs** maps to **Communicating information**: listening to design and business stakeholders and interpreting information accurately is verbal reasoning applied in real time.

### Practice questions

Passage for Questions 1–4:

"Public sector bodies in the UK must meet the requirements of the Public Sector Bodies (Websites and Mobile Applications) Accessibility Regulations 2018. Under these regulations, public sector websites must be perceivable, operable, understandable, and robust. Each website must also publish an accessibility statement describing its level of compliance and listing any known accessibility issues. The regulations allow limited exemptions; for example, some third-party content that is neither funded nor developed by the public sector body is not required to comply. Meeting the Web Content Accessibility Guidelines (WCAG) at level AA is generally considered the way to demonstrate compliance."

**Question 1 (easy) — True/False/Cannot Say**

Statement: "Public sector websites must publish an accessibility statement."

- A) True
- B) False
- C) Cannot Say

**Correct answer: A**

**Explanation:** The passage states directly: "Each website must also publish an accessibility statement describing its level of compliance and listing any known accessibility issues." The statement is a plain restatement of this, so it is True. Easy verification questions like this reward one habit above all: go back to the passage and put your finger on the exact sentence. Never answer from memory of the passage, even when you feel sure — the thirty seconds spent confirming costs little and prevents careless errors.

**Question 2 (easy) — True/False/Cannot Say**

Statement: "All third-party content on public sector websites must comply with the regulations."

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The passage says the regulations "allow limited exemptions; for example, some third-party content that is neither funded nor developed by the public sector body is not required to comply." The statement claims all third-party content must comply, which the passage directly contradicts — some is exempt. So the answer is False. Watch the quantifier: "all" is a very strong word, and a single stated exception is enough to make an "all" statement false. Spotting absolute words — all, every, never, only — and checking them against the passage is one of the most reliable techniques in verbal reasoning, and in reading real regulations too.

**Question 3 (easy) — True/False/Cannot Say**

Statement: "Most public sector websites currently fail to meet WCAG level AA."

- A) True
- B) False
- C) Cannot Say

**Correct answer: C**

**Explanation:** The passage explains what the regulations require and how compliance is generally demonstrated, but it says nothing about how many websites actually meet the requirements today. Whatever you may believe or have read elsewhere about real-world compliance levels, the passage neither supports nor contradicts this statement, so the answer is Cannot Say. This is the discipline the format exists to test: separating "what the text tells me" from "what I happen to know or suspect". The same discipline protects your audit findings — you record what you tested and observed, not what you assume is probably true of pages you did not test.

**Question 4 (moderate) — Inference**

Which conclusion is best supported by the passage?

- A) A public sector website that meets WCAG level AA has definitely satisfied every legal requirement.
- B) Publishing an accessibility statement is optional good practice.
- C) A public sector body cannot rely solely on meeting WCAG AA, because it must also publish an accessibility statement.
- D) The regulations apply to private companies' websites.

**Correct answer: C**

**Explanation:** The passage sets out two distinct obligations: the website must meet the accessibility requirements (with WCAG AA as the general way to demonstrate this), and it must publish an accessibility statement. A body that achieved AA but published no statement would still be missing an obligation, so C follows from combining the two sentences. Option A over-reaches — the passage says WCAG AA is "generally considered the way to demonstrate compliance", which is hedged, and A also ignores the statement requirement. Option B contradicts "must". Option D contradicts "public sector bodies". Inference questions reward combining what is stated while respecting every hedge — a skill you will reuse whenever you summarise standards or guidance for your team.

Passage for Questions 5–7:

"From: Priya (Senior Accessibility Specialist)
To: Testing team
Subject: Changes to this sprint's testing

Hi all — two changes for this sprint. First, we're moving assistive technology testing of the renewals journey to next sprint, because the fix for the focus-order issue isn't merged yet and retesting before the fix would waste effort. Second, please add the new document downloads page to this sprint's manual checks; the content team published it on Tuesday and it hasn't been checked at all. Automated scans continue as scheduled. As always, log findings in the tracker by Friday midday so I can compile the report. Shout if anything is unclear. Thanks! Priya"

**Question 5 (moderate) — True/False/Cannot Say**

Statement: "Assistive technology testing of the renewals journey has been cancelled."

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** Priya says the testing is "moving... to next sprint" — postponed, not cancelled. The statement says cancelled, which contradicts the email, so it is False. The distinction between deferred and cancelled looks small but changes what the team does: a deferred test stays on the plan and must not be forgotten. In test questions and in real inboxes alike, verbs carry the meaning — moved, paused, cancelled, completed, and blocked are all different states, and reading them precisely keeps your testing records accurate.

**Question 6 (moderate) — Comprehension of instructions**

According to the email, what should happen to the document downloads page this sprint?

- A) It should receive assistive technology testing.
- B) It should be added to manual checks.
- C) It should be removed from automated scans.
- D) Nothing — it was already checked on Tuesday.

**Correct answer: B**

**Explanation:** Priya's second change is explicit: "please add the new document downloads page to this sprint's manual checks". Option A confuses the two changes — assistive technology testing was the renewals journey item, and it moved out of the sprint. Option C contradicts "Automated scans continue as scheduled". Option D misreads Tuesday: that is when the page was published, and Priya says it "hasn't been checked at all". When an email contains multiple instructions, a reliable technique is to list each action, its object, and its timing before acting: (1) renewals AT testing → next sprint; (2) downloads page → this sprint's manual checks; (3) findings → tracker by Friday midday. Misrouting instructions between items is one of the most common workplace reading errors — and one of the easiest to prevent.

**Question 7 (moderate) — True/False/Cannot Say**

Statement: "The focus-order fix will be merged before the end of this sprint."

- A) True
- B) False
- C) Cannot Say

**Correct answer: C**

**Explanation:** The email says the fix "isn't merged yet" and that retesting has moved to next sprint — which suggests Priya expects the fix to land in time for next sprint's testing, but she never states when it will merge. Expectation is not assertion: the email gives no commitment or date, so the statement can be neither confirmed nor denied. Cannot Say. Notice how naturally the mind fills this gap — "she moved the testing, so the fix must be coming soon" — and how the format trains you to notice the fill-in and withhold it. In your testing work, the same alertness stops you writing "fix scheduled for next sprint" in the tracker when all you actually know is "fix not yet merged".

Passage for Questions 8–10:

"Audit finding A11Y-014: The service's date-of-birth field rejects valid entries when users type spaces (for example '01 02 1990'). The error message reads: 'Invalid input detected. Constraint violation: pattern mismatch.' Screen reader testing confirmed the message is announced. However, the message does not explain what format is expected, and the field's hint text says only 'Enter your date of birth'. Recommendation: accept common formats including spaces, and rewrite the error message to say what to do, for example: 'Enter your date of birth in the format DD MM YYYY'. Severity: Medium. This finding does not block task completion because users who guess a format without spaces can proceed."

**Question 8 (moderate) — True/False/Cannot Say**

Statement: "The error message is not announced by screen readers."

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The finding states "Screen reader testing confirmed the message is announced." The statement claims the opposite, so it is False. It is worth pausing on why the finding still exists even though announcement works: the message's content is unhelpful — "Constraint violation: pattern mismatch" tells the user nothing about what to do. An announced but useless message is a different defect from an unannounced message, and the audit records precisely which one was observed. Precision of this kind is what your role summary means by communicating findings so others can act on them: the developer reading A11Y-014 knows exactly what works, what fails, and what to change.

**Question 9 (hard) — Inference from a finding**

Which statement is best supported by the finding?

- A) The severity is Medium partly because a workaround exists: users can proceed if they enter the date without spaces.
- B) The date field fails because of a screen reader defect.
- C) Accepting spaces in dates is legally required.
- D) The hint text 'Enter your date of birth' fully solves the problem.

**Correct answer: A**

**Explanation:** The finding's last sentence explains the severity: "This finding does not block task completion because users who guess a format without spaces can proceed." That is a workaround, and its existence is given as the reason the issue does not sit at a higher, blocking severity — supporting A. Option B contradicts the finding: the screen reader behaved correctly; the defect is in the validation and the message wording. Option C introduces a legal claim the finding never makes — the finding recommends accepting spaces, which is not the same as asserting a legal requirement. Option D is contradicted: the finding criticises the hint for not stating the expected format. The skill here is connecting a conclusion (Medium severity) to its stated justification (workaround exists) — exactly how you will learn to read, and eventually write, well-reasoned audit findings.

**Question 10 (hard) — Clear-writing judgement**

You need to explain finding A11Y-014's user impact in one sentence for a sprint review attended by non-specialists. Which sentence is best?

- A) "The DOB widget's regex constraint violation surfaces a non-actionable validation string."
- B) "If someone types their date of birth with spaces, the form rejects it with an error that doesn't tell them how to fix it."
- C) "There is a problem with dates and errors and formats that users might not like very much at all."
- D) "The service is completely unusable and must be taken offline immediately."

**Correct answer: B**

**Explanation:** Option B states the trigger (typing with spaces), the behaviour (rejection), and the harm (no guidance on how to fix it) in plain words a product manager, content designer, or developer can all act on. Option A is jargon-dense — "regex", "non-actionable validation string" — and excludes non-specialists, defeating the purpose of a sprint review explanation. Option C is vague to the point of carrying no information. Option D is inaccurate escalation: the finding explicitly says the issue does not block task completion, and overstating severity spends your credibility, which is a junior specialist's most valuable asset. Government writing guidance favours short, concrete, active sentences, and so do assessment questions on clear writing: the best option is almost always specific, plain, and accurate all at once.

**Question 11 (hard) — Interpreting a user story**

A user story reads: "As a screen reader user, I need form errors to be announced when they appear, so that I know my application has a problem and can fix it before submitting again." Which of the following is a genuine acceptance test for this story, rather than an assumption smuggled in from outside it?

- A) Errors must be announced by the screen reader when they appear.
- B) Errors must be shown in red text.
- C) The form must never produce errors.
- D) The user must complete the form within five minutes.

**Correct answer: A**

**Explanation:** A user story defines who, what, and why: a screen reader user needs errors announced (what) so they can fix problems before resubmitting (why). Option A tests exactly the "what" — announcement on appearance — so it belongs. Option B concerns visual styling, which this story never mentions (and red-only signalling would itself be an accessibility issue for colour-blind users — a different story). Option C misreads the goal: the story asks for errors to be communicated, not eliminated; forms will always need validation. Option D invents a time constraint found nowhere in the text. Your role summary asks you to explain the purpose of user stories and the focus on user needs — and the heart of that is exactly this reading skill: the story's own words define its scope, and tests must trace to those words, not to what anyone assumes was probably meant.

**Question 12 (hard) — Reconciling two documents**

Document 1 (guidance page): "All videos published on the service must have captions." Document 2 (team email): "The welcome video is exempt from captioning because it has no dialogue or meaningful audio." A colleague asks you whether the welcome video needs captions. Based only on these two documents, what is the most accurate answer?

- A) Yes — Document 1 says all videos must have captions, and it outranks emails.
- B) No — Document 2 says it is exempt, and emails are more recent.
- C) The documents conflict: the guidance states a rule with no exceptions, while the email claims an exemption; the right step is to check the source of the claimed exemption before answering.
- D) Neither document mentions the welcome video.

**Correct answer: C**

**Explanation:** Read each document precisely. Document 1 states an unqualified rule: all videos, captions, no exceptions mentioned. Document 2 claims an exemption for a specific video, with a rationale. The two cannot both be applied as written — that is a conflict, and the honest answer reports it rather than silently picking a winner. Options A and B each invent a precedence rule ("guidance outranks emails", "newer wins") that appears in neither document; you may not resolve a conflict using rules the texts do not contain. Option D is simply false — Document 2 names the welcome video. In the real workplace, the email's rationale is plausible (captions convey audio content, and WCAG's captioning requirements concern audio information), but plausibility is not authority: the professional move, and the one your Consultancy skill describes as working under guidance by referring to previous work, is to trace the exemption to its source — the standard's actual text or your senior specialist — before advising your colleague. In the test, the option that accurately describes the texts and the sound next step beats every option that guesses.

### Preparation tips

- **Practise the three-way judgement daily.** Take any paragraph from a guidance page and write one statement it supports, one it contradicts, and one it does not address. This builds the True/False/Cannot Say reflex faster than passive reading.
- **Hunt the quantifiers and hedges.** Words like all, some, must, may, generally, and unless decide most answers. Circle them mentally as you read.
- **Answer from the passage only.** Your accessibility knowledge is an asset in your job and a trap in this test. If the passage does not say it, you Cannot Say it.
- **Read the statement as carefully as the passage.** Many wrong answers come from misreading the statement — a flipped negative, a swapped subject — rather than the passage itself.
- **Practise summarising in plain words.** After reading any finding or standard, try explaining it aloud in one sentence a non-specialist would understand. This trains the clear-writing judgement questions and improves your real reports.
- **Time-box gently.** Aim for a steady rhythm — roughly a minute per statement — and return to marked questions at the end rather than stalling.

### Common pitfalls to avoid

- **Importing outside knowledge.** The most common error for specialists: you know the real-world answer, so you stop checking the passage. Discipline beats knowledge here.
- **Treating "Cannot Say" as failure.** It is a correct, positive answer whenever the passage is silent. Expect a substantial minority of statements to land there.
- **Missing the difference between hedged and absolute claims.** "Generally considered the way to demonstrate compliance" does not support "always sufficient". Hedges limit what you may infer.
- **Confusing postponed with cancelled, published with checked, expected with promised.** Precise verbs carry workplace meaning; sloppy paraphrase loses it.
- **Choosing the fanciest-sounding rewrite.** In clear-writing questions, jargon-heavy options are traps. The best sentence is the plainest accurate one.
- **Rushing multi-instruction passages.** When an email contains several actions, map each action to its object and timing before answering anything about it.

## Workplace job-specific situational judgement assessment

### About this assessment

A situational judgement assessment presents realistic workplace scenarios and asks you to judge possible responses. Unlike the other assessments, there is often no single mathematically provable answer; instead, some responses are clearly more effective than others, and the test measures whether you can tell the difference. Common formats include: choose the most effective response; choose the most and least effective responses; rank all responses from best to worst; or rate each response's effectiveness on a scale. The scenarios are drawn from the real texture of the role — for you, that means supervised testing work, finding and reporting issues, asking for help, working in a multidisciplinary team, and advocating for users affected by accessibility barriers.

The typical format is untimed or generously timed (20 to 40 minutes for 10 to 20 scenarios), online, and scored against a key agreed by subject-matter experts and experienced managers. Employers use situational judgement tests for roles like yours because technical knowledge alone does not predict success: what matters equally is judgement — knowing when to ask, when to escalate, when to speak up for users, and how to work well with others while you are still learning.

A reassuring note for a junior specialist: these tests are calibrated for your level. Nobody expects you to resolve a dispute between directors. The scenarios test whether you do the junior role well — which includes asking questions, working under supervision honestly, and raising problems early. In situational judgement terms, "I checked with my supervisor" is very often part of the strongest answer at your level, not a sign of weakness. The behaviours that score well are the same ones that make you a trusted teammate: user focus, collaboration, ownership of your tasks, honest communication, appropriate escalation, and inclusion.

### How this assessment maps to your role

- **User focus scenarios** map to your **User focus** skill and your duty to be an advocate for people affected by accessibility barriers: the strongest responses keep disabled users' needs central even under delivery pressure.
- **Supervision and escalation scenarios** map to **Testing** ("correctly execute test scripts under supervision") and **Consultancy** ("work under guidance"): knowing what to handle yourself and what to raise, and raising it early and clearly, is the essence of working well at your level.
- **Team communication scenarios** map to **Communicating information**: taking part in discussions within a multidisciplinary team means contributing your findings clearly, listening to others' constraints, and interpreting what stakeholders need.
- **Learning and honesty scenarios** map to your level definition ("learns on the job"): responses that admit uncertainty, seek feedback, and follow through score higher than responses that bluff or hide mistakes.
- **Community scenarios** map to your duty to engage with and contribute to the cross-government accessibility community: sharing and asking within the community, appropriately, is part of the role.

### Practice questions

**Question 1 (easy) — You find a serious issue late on Friday**

It is 4:30pm on Friday. While finishing a test script, you find that the service's "Submit application" button cannot be activated using a keyboard. The service is due to go live on Monday morning. Your supervisor is still online. What is the most effective response?

- A) Log the issue in the tracker and go home — it will be seen on Monday.
- B) Message your supervisor now with a short, clear description of the issue and its impact, and log it in the tracker.
- C) Stay late and try to fix the code yourself.
- D) Post about the issue in the cross-government community channel to ask what to do.

**Correct answer: B**

**Explanation:** A keyboard-inoperable submit button blocks task completion for keyboard and many assistive technology users — on the final step of the journey — and the service goes live Monday. The combination of severity and timing makes this an escalation moment: your supervisor needs to know today, while there is still time to act, and the tracker entry preserves the details. Option A follows process but sits on time-critical information all weekend. Option C exceeds your role — you are not the developer, an unreviewed late-Friday code change is risky, and the delay in telling anyone makes things worse. Option D shares an internal, pre-launch problem outside your organisation before your own team knows — the community is for shared learning, not first-line escalation. The professional behaviours rewarded here are ownership (you saw it, you raised it), escalation done early and calmly, and user focus (recognising who would be blocked).

**Question 2 (easy) — You do not understand a test script step**

Halfway through executing a test script, you reach a step that says "verify the accessible name of the control". You are not sure what an accessible name is or how to check it. What is the most effective response?

- A) Skip the step and mark it as passed so the run looks complete.
- B) Guess what it means and record whatever seems plausible.
- C) Pause, look it up briefly in your team's guidance, and if still unsure, ask your supervisor before recording anything for that step.
- D) Abandon the whole test run.

**Correct answer: C**

**Explanation:** Your role is defined as learning on the job under supervision, and this scenario tests whether you do that honestly. Option C shows the ideal sequence: try to resolve it yourself quickly using available guidance (self-sufficiency), then ask rather than guess (honesty and accuracy), and crucially, record nothing you have not genuinely verified. Option A is falsification of results — the single most damaging thing a tester can do, because every downstream decision trusts your records. Option B is gentler but still pollutes the results with guesswork. Option D wastes the valid work already done; one unclear step does not invalidate a run. Notably, asking here is not a weakness signal: a junior specialist who asks precise questions at the right moments is demonstrating exactly the behaviour the level requires, and will learn "accessible name" properly — a concept they will use for years.

**Question 3 (easy) — A developer dismisses your finding**

You report that a form field has no programmatically associated label. The developer replies in the ticket: "Looks fine to me on my screen. Closing." What is the most effective response?

- A) Reopen the ticket with a note explaining that the label is visible but not associated in the code, describe the impact on screen reader users, and offer to demonstrate it.
- B) Let it go — the developer knows the code better than you.
- C) Reply: "Reopening. This is a WCAG violation and closing it is unprofessional."
- D) Complain to the developer's line manager about the closure.

**Correct answer: A**

**Explanation:** The developer's comment reveals the misunderstanding: they checked visually, but the defect is programmatic. Option A resolves exactly that gap — it explains the difference between visible and associated, makes the user impact concrete (a screen reader announces nothing when the field gains focus), and offers a demonstration, which is often the moment accessibility "clicks" for a developer. It is polite, persistent, and educational — advocacy for affected users done well. Option B abandons a genuine barrier; deference to seniority does not extend to letting real defects ship, and your role explicitly makes you an advocate for people affected by barriers. Option C may be technically right but its tone turns a colleague into an opponent; collaboration matters. Option D leaps two escalation levels over a first misunderstanding — escalation is for when direct, respectful engagement fails, not before it is tried.

**Question 4 (easy) — Invitation beyond your experience**

A service team invites you to run a full accessibility audit of their service by yourself, with your name as the sole auditor. You have assisted with audits but never led one, and your role level says audits are performed by more senior specialists while you assist with testing. What is the most effective response?

- A) Accept — it is a great opportunity and you will figure it out.
- B) Decline without telling anyone, to avoid embarrassment.
- C) Thank them for thinking of you, explain that audits at your level are done with senior oversight, and bring the request to your supervisor so it can be resourced properly — asking to assist on it as a development opportunity.
- D) Accept, but secretly ask a friend in another department to do the hard parts.

**Correct answer: C**

**Explanation:** This scenario tests self-awareness about scope and the difference between ambition and overreach. An audit issued under your name alone becomes an assurance artefact others rely on; performing one without the experience or the mandate risks missed barriers shipping with apparent sign-off — a risk to users, the team, and you. Option C handles it ideally: it keeps the relationship warm, is honest about level, routes the work to proper resourcing, and converts the moment into supervised development — assisting on the audit is exactly how your level's "learns on the job by assisting with accessibility testing" is designed to work. Option A confuses confidence with capability where the cost of error falls on users. Option B loses both the work and the development opportunity, and hides a resourcing need from your team. Option D adds concealment and an accountability fiction to overreach. Strong situational judgement at junior level often looks like this: enthusiastic, honest about limits, and quick to bring opportunities to the team.

**Question 5 (moderate) — Most and least effective**

During sprint planning, the product manager proposes skipping accessibility checks this sprint to hit a deadline: "We'll catch up next sprint." You are the only accessibility person in the room. Consider these responses:

1. Say nothing — you are the most junior person present.
2. Calmly note what the checks cover, the risk of shipping unchecked changes to disabled users, and suggest discussing options — such as checking only the highest-risk changes — then follow up with your supervisor afterwards.
3. Tell the product manager that skipping checks is illegal and the meeting should be stopped.
4. Agree enthusiastically to build goodwill with the team.

Which is the MOST effective and which is the LEAST effective response?

- A) Most: 2; Least: 4
- B) Most: 2; Least: 1
- C) Most: 3; Least: 1
- D) Most: 1; Least: 3

**Correct answer: A**

**Explanation:** Response 2 is clearly strongest: it raises the user impact and the risk (advocacy and user focus), proposes a proportionate middle path (collaboration — risk-based checking is a genuine practice), respects the product manager's authority to decide, and loops in your supervisor, which is exactly right at your level for a decision with this much consequence. Choosing the least effective response is where this question sharpens judgement: response 1 is weak — silence lets users' interests go unrepresented — but response 4 is worse, because it actively endorses the removal of the safeguard and spends your professional voice to do it; an enthusiastic agreement from "the accessibility person" will be remembered as expert blessing. Response 3 is flawed too — an unqualified legal claim delivered as a meeting-stopper overstates your standing and hardens positions — but it at least attempts to protect users. The ranking logic worth remembering: actively harmful endorsement < silence < clumsy advocacy < skilled advocacy.

**Question 6 (moderate) — Your mistake is discovered**

Compiling results, you realise that yesterday you recorded a step as "pass" but you now doubt you actually performed it — you may have confused it with a similar step on another page. The report goes to the service team tomorrow. What is the most effective response?

- A) Leave it — it was probably fine.
- B) Change it to "fail" to be safe.
- C) Re-run the step now if you can; if you cannot, tell your supervisor today that the result is unreliable and needs re-testing before the report goes out.
- D) Delete the step from the report so the question never arises.

**Correct answer: C**

**Explanation:** The core value under test is the integrity of results, with a deadline adding pressure. Option C repairs the problem at its root: the best fix is simply to perform the test properly (often minutes of work), and where that is impossible, honest disclosure lets your supervisor decide — perhaps re-testing, perhaps annotating the report. Raising it today respects the deadline; raising it after publication would turn a small correction into a credibility problem. Option A ships data you know may be wrong — "probably fine" is not a test result. Option B corrupts the data in the opposite direction; guessing "fail" is no more honest than guessing "pass", and false failures waste developer time and erode trust in your findings. Option D conceals, which is worse than either guess. Everyone records something imperfectly eventually; what distinguishes professionals is that they correct quickly and openly. Supervisors consistently rate "tells me the same day" among the most valuable behaviours a junior colleague can show.

**Question 7 (moderate) — Balancing community and deadlines**

You have a testing task due tomorrow that will take the rest of today. A member of the cross-government accessibility community posts a question you could answer well, and answering properly would take about an hour. What is the most effective response?

- A) Spend the hour now — community always comes first.
- B) Ignore the post entirely — community is not real work.
- C) Post a brief note that you can help and will reply fully tomorrow after a deadline, then finish your testing task.
- D) Ask your supervisor to do your testing task so you can answer the post.

**Correct answer: C**

**Explanation:** Your role genuinely includes engaging with and contributing to the cross-government community — option B's dismissal is wrong on the role definition itself, and communities wither when everyone leaves answering to someone else. But contribution does not outrank a committed deadline: option A trades tomorrow's promised delivery for an unscheduled hour, and option D inverts the supervision relationship in a way that would rightly raise eyebrows. Option C honours both: the deadline is met, the community member gets a fast acknowledgement (often the most reassuring part), and the full answer arrives a day later — entirely acceptable in an asynchronous community. The general skill is sequencing commitments rather than treating every good activity as equally urgent — the same impact-and-urgency reasoning as the cognitive test's prioritisation questions, now expressed as workplace behaviour.

**Question 8 (moderate) — A colleague uses outdated guidance**

A content designer on your team shares a draft "accessibility checklist" for the team wiki. You notice it recommends a technique your recent training identified as outdated and potentially harmful for screen reader users. The designer is senior to you and proud of the work. What is the most effective response?

- A) Say nothing — correcting a senior colleague is not your place.
- B) Post a public comment on the wiki: "This is wrong and shouldn't be used."
- C) Message the designer privately: thank them for the initiative, mention that one technique may have been superseded, share the source from your training, and offer to check it together with your supervisor or a senior specialist.
- D) Quietly edit the wiki page yourself without telling the designer.

**Correct answer: C**

**Explanation:** The scenario tests whether you can advocate for users across a seniority gap without damaging a relationship. Option C succeeds on every axis: it protects users (the flawed technique gets challenged before the checklist spreads), it protects the relationship (private, appreciative, evidence-based), it respects your level (you cite a source and propose verification with a senior specialist rather than positioning yourself as the final authority — wise, since training can be misremembered), and it keeps the designer as an accessibility ally, which matters enormously long-term. Option A lets a harmful technique be institutionalised in team guidance. Option B may be factually right but the public bluntness embarrasses a proud senior colleague and teaches the team that engaging with accessibility invites humiliation. Option D fixes the page but breaks trust when discovered, and skips the verification your level calls for. Inclusion and collaboration are the behaviours scored here: the best advocates make allies, not opponents.

**Question 9 (moderate) — Conflicting instructions**

Your supervisor asked you to spend today re-testing fixed issues on Service A. Mid-morning, a delivery manager from Service B messages you directly: "Need you to check our new pages today please — urgent." Your supervisor is in workshops and slow to respond. What is the most effective response?

- A) Switch to Service B — the request said urgent.
- B) Refuse Service B outright: "I don't work for you."
- C) Tell the delivery manager you are committed to another task today and are checking with your supervisor about priorities; send your supervisor a short message stating both demands and asking which comes first; continue Service A until told otherwise.
- D) Try to do both by doing each half-heartedly.

**Correct answer: C**

**Explanation:** Junior staff frequently face competing demands from people who each feel their need is most urgent — and the key insight is that re-prioritising your supervisor-assigned work is your supervisor's call, not yours or the delivery manager's. Option C gets every element right: the delivery manager receives an immediate, honest status (not silence), the supervisor receives a crisp decision request with both facts, and productive work continues on the last agreed priority in the meantime. Option A lets whoever says "urgent" loudest reorder your team's plan — "urgent" is a claim, not a verdict, and Service A's re-testing may feed something more critical. Option B protects the plan but damages a stakeholder relationship your team depends on; courtesy costs nothing. Option D delivers two unreliable half-jobs — and unreliable testing is worse than no testing, because people trust it. Ownership, honest communication, and correct escalation are the behaviours being scored.

**Question 10 (hard) — Pressure to soften findings**

You assisted a senior colleague with testing, and your part found 14 issues. Before the report goes out, a delivery manager approaches you informally: "Fourteen looks terrible for us at the service assessment. Some are tiny — could you drop the trivial ones from your list? It would really help the team." Your senior colleague is away today. What is the most effective response?

- A) Drop the five smallest issues — being helpful builds relationships.
- B) Explain politely that findings can't be removed, but that the report can present severity clearly so small issues are visibly small; say you'll flag the conversation to the senior colleague leading the report.
- C) Tell the delivery manager you will report them for attempted fraud.
- D) Say nothing to anyone and let the senior colleague find out whenever.

**Correct answer: B**

**Explanation:** This is an integrity-under-pressure scenario dressed in friendliness — the request is to make evidence disappear because it is inconvenient. Option B refuses the substance while treating the person and their underlying worry seriously: the manager's real problem is how the findings will look, and accurate severity presentation is the legitimate solution — an assessment panel reading "2 high, 3 medium, 9 low" draws a fair conclusion, whereas discovering removed findings later would be far more damaging to the team than any count. Flagging the conversation to the report's lead is essential, not optional tale-telling: they own the report, may face the same request, and the approach targeted the most junior person involved — a pattern seniors need to know about. Option A quietly falsifies an assurance record and teaches stakeholders that pressure on juniors works. Option C treats a misguided request as a crime, incinerating a working relationship where firm politeness would do. Option D avoids the falsification but withholds material information from the report's owner. Ownership, integrity, and upward transparency are the scored behaviours — with marks too for solving the stakeholder's legitimate problem legitimately.

**Question 11 (hard) — A user's complaint reaches you**

Your team receives a complaint forwarded from the department's contact centre: a blind user spent 40 minutes failing to complete a form your team tested and passed last month. Your supervisor asks you to look into it. You re-test with the same script and everything passes. What is the most effective response?

- A) Report back: "Re-tested, all passes — the user must have been mistaken."
- B) Report the passing results, but also note the limits of the script: ask whether the user's assistive technology, browser, or journey might differ from the tested setup, and suggest the team try to reproduce the user's actual conditions — treating the complaint as evidence, not error.
- C) Mark the complaint as resolved since the script passes.
- D) Rewrite the test script so it would have caught whatever the problem was.

**Correct answer: B**

**Explanation:** A passing script and a failing user are both facts, and the junior mistake is letting the tidy fact overrule the messy one. Scripts sample reality: they fix a browser, an assistive technology, a version, and a path, while real users bring different screen readers, voice control, magnification, older versions, and unexpected journeys. A user who persisted for 40 minutes is a rich signal — most people give up silently — and your role exists to bring exactly this voice into the team. Option B reports honestly (the script does pass), reasons about why the mismatch might exist, and proposes the investigative next step, all while staying within your level: you suggest and ask rather than unilaterally redesign the testing approach. Options A and C share the same flaw — treating the script as the definition of accessibility rather than a partial check of it — and A adds a dismissiveness toward a disabled user that is the opposite of advocacy. Option D acts before understanding: you cannot write the catching test until you know what to catch, and reproducing the user's conditions comes first. User focus, humility about tools, and honest reporting are the behaviours scored.

**Question 12 (hard) — Ranking responses under launch pressure**

Two days before a high-profile launch, you find that the service's PDF guidance document is an untagged scan — completely unreadable by screen readers. The HTML pages of the service itself all pass. The content team says a proper accessible version needs a week. Rank these responses from most to least effective:

1. Raise it to your supervisor today with the facts, and suggest discussing interim options — such as publishing an accessible HTML version of the key content, or publishing the PDF with a prominent note, a contact route for alternative formats, and a dated commitment to replace it.
2. Insist the launch be delayed a week until the PDF is fixed.
3. Say nothing until after the launch to avoid being seen as a blocker.
4. Fix the PDF yourself tonight using a tagging tool you have never used before, and tell no one.

- A) 1, 2, 4, 3
- B) 1, 2, 3, 4
- C) 2, 1, 3, 4
- D) 1, 4, 2, 3

**Correct answer: A**

**Explanation:** Response 1 leads clearly: it surfaces the problem at the right level immediately, and brings options rather than only a problem — and the options are the realistic ones services actually use, since the essential content can often go up as accessible HTML quickly while the PDF is remediated, paired with an alternative-format route. Response 2 comes second: it is honest advocacy in the right direction, but it prescribes the most drastic remedy while ignoring workable interim paths, and launch decisions are far above your level — recommend and inform, rather than insist. Ranking 4 above 3 is the subtle judgement: response 4 is misguided — unsupervised, unreviewed remediation with an unfamiliar tool, concealed from the team, could produce a PDF that seems fixed but is not, which is arguably worse than one that is obviously broken — but it at least attempts to help users and its flaws are of competence and process. Response 3 is a failure of the role's core duty: deliberately concealing a known barrier so launch messaging stays comfortable abandons the users you exist to represent, and discovery of the concealment would damage trust more than the barrier itself. Silence in the face of known harm ranks below even clumsy action.

### Preparation tips

- **Learn the behaviours, not the answers.** Strong responses at your level almost always combine user focus, honesty, early escalation, and respect for colleagues. When torn between options, ask which one best serves users and keeps your team informed.
- **Notice the "junior-shaped" right answer.** At your level, checking with a supervisor, asking a clarifying question, or offering to assist rather than lead is usually a strength. Options where you act far beyond your role — fixing code, making launch decisions, issuing legal rulings — are usually distractors.
- **Separate the person from the problem.** Many scenarios involve someone senior being wrong or applying pressure. The best responses stay warm toward the person and firm about the issue.
- **Practise "most and least" thinking.** For any workplace dilemma you hear about, identify not just the best response but the worst, and articulate why. Least-effective judgements are where many candidates lose marks.
- **Reflect on real moments.** After each week, note one situation where you escalated, asked, or advocated — and what you would do differently. Situational judgement improves through reflection, and interviews love these examples too.
- **Read each scenario's constraints carefully.** Deadlines, who is available, and what has already been tried all change the best answer. The details are there on purpose.

### Common pitfalls to avoid

- **Choosing heroics.** Staying all night, fixing things secretly, or single-handedly saving the launch feels impressive but scores poorly. Teams run on communication, not lone heroes.
- **Confusing escalation with weakness.** Sitting on a serious problem to seem self-sufficient is one of the most heavily penalised behaviours. Early, calm escalation is a strength at every level, and especially yours.
- **Over-escalating.** The mirror-image error: going to a line manager or making formal accusations before trying a direct, polite conversation. Match the response to the situation's stage.
- **Endorsing bad decisions to be liked.** Agreement under pressure reads as expert blessing when it comes from "the accessibility person" — even a junior one. You can be collegiate without surrendering the user's interest.
- **Absolutism.** Responses built on "never", "illegal", or "must stop everything" usually overstate your standing and the situation. Proportionate options — interim fixes, risk-based approaches, dated commitments — usually score best.
- **Forgetting the user.** Under deadline scenarios, it is easy to pick the option that smooths delivery. Re-read the options asking, "where did the disabled user's interest go?" The best answer never loses track of it.

## Conclusion

Well done for working through this guide — that took real commitment, and it is exactly the kind of steady, careful effort that makes a good accessibility specialist.

Let's recap what you have covered. In the cognitive section, you practised the pattern recognition, deduction, error checking, and prioritisation that power your daily testing work — from spotting the page that breaks the pattern in a scan report, to reasoning correctly about what a WCAG rule does and does not require. In the numeric section, you worked with the numbers your role genuinely produces: issue counts, pass rates, contrast ratios, averages, and percentage changes — and you practised the sense-checking that stops a misleading headline number slipping into a report. In the verbal section, you sharpened the reading discipline that standards, regulations, findings, and team emails all demand: answering from the text, respecting hedges and quantifiers, and writing plainly. And in the situational judgement section, you rehearsed the workplace moments that define a junior specialist's reputation: raising serious issues early, asking rather than guessing, keeping results honest under pressure, and always, always keeping disabled users at the centre of the conversation.

Notice something encouraging that runs through all four sections: the skills that help you score well on these assessments are the same skills that make you better at your actual job. Practising percentage change makes your reports more trustworthy. Practising True/False/Cannot Say makes your reading of standards more precise. Practising situational judgement makes you the kind of colleague supervisors trust with more responsibility. None of this practice is wasted, whatever the outcome of any particular test.

If a test is coming up soon, be practical: revisit the preparation tips, do a timed practice run or two, and get a good night's sleep beforehand. On the day, read instructions fully, use any ungraded practice questions, and keep a steady rhythm — accuracy first, speed second. If one question goes badly, let it go; the next one is a fresh start.

Looking further ahead, keep growing the way your role is designed to grow: assist with testing and audits, ask precise questions, learn one assistive technology deeply and others broadly, and keep contributing to the cross-government accessibility community — it is one of the friendliest and most generous professional communities in government. Every check you perform carefully, every finding you communicate clearly, and every time you bring the voice of disabled users into a room, you make public services work better for everyone.

You are at the start of a career that genuinely matters. Keep practising, keep asking, and be proud of the work you do. Good luck — you are better prepared than you think.
