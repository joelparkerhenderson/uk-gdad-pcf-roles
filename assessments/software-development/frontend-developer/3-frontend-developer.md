# Frontend Developer - Psychometric Assessment Resources

## Introduction

Welcome. This guide is written for you as a frontend developer in the UK Government Digital and Data profession — someone who builds software components, primarily user interfaces, collaborating closely with other disciplines to develop designs and working prototypes based on user needs. Your role level names writing clean, well-tested code that follows web standards, and coaching and mentoring more junior colleagues.

The wider role description adds three things worth holding onto, because they shape almost every question below. You write accessible code following a progressive enhancement approach. You create code that is open by default and easy for others to reuse. And you have a working understanding of the three fundamental frontend technologies — HTML, CSS and JavaScript — which in government means understanding them well enough to know when not to reach for the third one.

This is a role where the reasoning is genuinely distinctive. A frontend developer in government builds for a user base that includes people on old Android phones over intermittent mobile data, people using screen readers, people with motor impairments using switch access, and people who will use the service exactly once in their life at a difficult moment. That is not an edge case to accommodate; it is the population. A design that works beautifully on your laptop and fails on a five-year-old handset has failed for a meaningful share of the people it exists for.

You may be preparing for a formal assessment as part of a selection process, or you may want to sharpen judgement you already have. Either way, the questions here are built around the decisions this role actually contains: what to do when a design cannot be made accessible as drawn, how to tell whether a performance number means anything, what "it works on my machine" is worth, and how to raise a problem with a designer or a stakeholder so that it lands.

The document has four assessment sections — cognitive, numeric reasoning, verbal reasoning and situational judgement — each with an overview, a mapping to your named skills, twelve practice questions with full explanations, preparation tips and common pitfalls.

Try to commit to an answer before reading each explanation. The explanations are where most of the value is, particularly on the questions you found easy.

Let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive assessment measures the reasoning your role demands, using material that looks like your work rather than abstract puzzles. For a frontend developer that means accessibility requirements, browser and device behaviour, design specifications, performance data and interface logic.

The format is typically an online test of fifteen to thirty minutes covering logical deduction, pattern recognition, error checking, prioritisation and applied problem solving. Scoring is objective against a norm group of people at comparable levels. Some platforms adapt difficulty as you go, and many report speed and accuracy separately.

Three things distinguish this section at your level.

The first is that progressive enhancement is a reasoning discipline, not a style preference. The question "what happens if this JavaScript does not run" has a real answer for real users — on flaky connections, on locked-down corporate browsers, when a CDN fails — and building from a working baseline outward is what makes the answer acceptable.

The second is that accessibility problems are usually structural. An interface that is hard to make accessible is usually an interface built on the wrong element, and adding ARIA attributes to patch it is a symptom of a decision made earlier.

The third is that browser behaviour is discovered rather than deduced. Your mental model of what a browser does is an approximation, and the developers who get into trouble are the confident ones.

### How this assessment maps to your role

The cognitive dimensions map onto the skills named in your role summary:

- **Structural reasoning about markup** maps to **Accessibility**, where you build interfaces meeting a predefined set of standards.
- **Reasoning about failure modes** maps to progressive enhancement and to **Programming and build (frontend developer)**.
- **Performance diagnosis** maps to **Web performance optimisation**, where you help identify and resolve issues.
- **Prioritisation under constraint** maps to **Leadership and guidance**, where you make decisions of differing risk and complexity.
- **Integration reasoning** maps to **Systems integration (frontend developer)**.
- **Reading design intent** maps to **Prototyping** and **User focus**.

### Practice questions

**Question 1 (easy) — Deduction from a standard**

Your team's standard states: "All interactive components must be operable by keyboard, except components that duplicate functionality available elsewhere on the page in keyboard-operable form." A component is not keyboard-operable. Which must be true?

- A) The standard was breached.
- B) The functionality is duplicated elsewhere.
- C) Either the functionality is available elsewhere in keyboard-operable form, or the standard was breached.
- D) The component must be fixed.

**Correct answer: C**

**Explanation:** A rule with a stated exception, plus a fact silent on whether the exception applies, gives you only the disjunction. Options A and B each pick a branch without evidence. Option D prescribes an action rather than stating what must be true — and it is worth noticing that in practice you probably would fix it, which is exactly why the option is tempting. The logic and the action are different questions.

**Question 2 (easy) — Progressive enhancement**

A form submits via JavaScript to avoid a page reload. What is the most important question to ask about it?

- A) Whether the JavaScript is minified.
- B) What happens when the JavaScript does not run — whether the form still submits through a normal HTML form action and produces a working result, because if it does not, users on failed script loads, blocked CDNs or restricted browsers cannot complete the task at all.
- C) Whether it works in all supported browsers.
- D) Whether the response is accessible to screen readers.

**Correct answer: B**

**Explanation:** Progressive enhancement means the baseline works without JavaScript and the script improves it, and the test is whether the form has a real `action` and `method` that produce a valid result on their own. This matters because script failure is not rare at population scale — a dropped request, an aggressive corporate proxy, a browser extension — and in government the consequence is somebody unable to claim something. Option D is a genuinely important question and applies to the enhanced path; option B asks whether there is a path at all. Options A and C matter and are secondary to whether the task can be completed.

**Question 3 (moderate) — A structural accessibility problem**

A developer has built a dropdown menu using `<div>` elements with click handlers, and is now adding `role="button"`, `tabindex="0"` and keyboard event handlers to make it accessible. What is the strongest observation?

- A) The approach is fine as long as the ARIA is correct.
- B) The effort being spent reconstructing button behaviour is a signal that the wrong element was chosen — a native `<button>` provides focus handling, keyboard activation, and assistive technology semantics for free, and hand-built equivalents reliably miss something, most often the distinction between Enter and Space or the behaviour of a disabled state.
- C) They should add `aria-label` as well.
- D) The dropdown should be replaced with a `<select>`.

**Correct answer: B**

**Explanation:** The general rule — use the native element and only reach for ARIA when nothing native fits — exists because native elements carry a great deal of behaviour that is tedious and error-prone to reproduce. Option B names the specific things typically missed. Option D is a reasonable alternative for some patterns and is a different design decision rather than an observation about this one. Option A is the position that produces most inaccessible custom components, because the ARIA is usually correct and the behaviour is not. Option C adds an attribute to a component whose foundation is the problem.

**Question 4 (moderate) — Reading a bug report**

A user reports that a page "doesn't work on my phone". What is the strongest first step?

- A) Test on your own phone.
- B) Establish what "doesn't work" means and on what — which browser and version, what the user tried to do, and what happened instead — because "doesn't work" covers a layout problem, a script error, a timeout and an unreadable contrast, and these have nothing in common.
- C) Check the analytics for mobile errors.
- D) Reproduce it in the browser's device emulator.

**Correct answer: B**

**Explanation:** The report contains almost no information, and each of the possible meanings would send you somewhere different. Option B gets the three things that make the report actionable. Option D is the fastest thing to try and device emulation is not the same as a device — it emulates viewport and touch, not the actual browser engine, the CPU, the memory pressure or the network. Option A tests a modern handset on office wifi, which is the configuration least likely to reproduce anything. Option C is useful once you know what to look for.

**Question 5 (moderate) — Prioritising accessibility findings**

An audit returns four issues: a missing form label, a colour contrast ratio of 4.3:1 on body text, a decorative image with no `alt` attribute, and a modal that does not trap focus. Which is most urgent?

- A) The contrast ratio.
- B) The missing form label, because a form control with no accessible name is unusable by a screen reader user — they cannot tell what to enter — which blocks task completion entirely, whereas the others degrade the experience without preventing it.
- C) The modal focus trap.
- D) The decorative image.

**Correct answer: B**

**Explanation:** Prioritise by whether the issue blocks a task. An unlabelled form control is announced as "edit text, blank" and the user has no way to know what it wants, which stops them completing the form. The modal focus trap is the next most serious, since focus escaping a modal is disorienting and usually still recoverable. Contrast at 4.3:1 fails the 4.5:1 requirement for normal text and is a genuine failure that most users can still work through. A decorative image missing `alt=""` causes a screen reader to announce the filename, which is noise rather than a blocker. All four should be fixed; the question is order.

**Question 6 (moderate) — A performance symptom**

A page scores well on synthetic performance tests but users report it feeling slow. What is the strongest explanation to investigate first?

- A) The tests are wrong.
- B) Synthetic tests typically run on a fast connection from a nearby location on a capable machine, so the gap usually means real users differ on one of those axes — slower devices where JavaScript execution dominates, or higher latency where the number of round trips matters — and field data segmented by device and connection will show which.
- C) The users are exaggerating.
- D) The server is slow at peak.

**Correct answer: B**

**Explanation:** The discrepancy between lab and field data is one of the most common situations in web performance and it has a small number of usual causes. On a low-end Android device, JavaScript parse and execution can take several times longer than on a development machine, so a page that is fast in the lab can be unresponsive in the hand. Option B names the mechanism and the diagnostic. Option D is a real possibility and would usually show in synthetic tests too. Option A dismisses data; option C dismisses users, who in this case are reporting something true.

**Question 7 (moderate) — Design feedback before build**

A designer's specification includes a colour combination that fails contrast requirements. What is the strongest response?

- A) Build it as specified and raise it in testing.
- B) Raise it now with the specific numbers — the measured ratio, the required ratio, and one or two nearby colours that pass — because your role includes offering design feedback to mitigate the risk of failing accessibility testing, and a change to a colour value costs nothing before build and costs rework afterwards.
- C) Build it with a compliant colour and tell the designer.
- D) Ask the designer to check the contrast.

**Correct answer: B**

**Explanation:** Your role names this explicitly, and the timing is the whole value: a hex value changed in a design file costs a minute, and the same change after build means rework across components, screenshots and possibly a design system. Option B brings the measurement and a solution, which makes it collaborative rather than a rejection. Option C makes a design decision unilaterally, which is not yours and damages the working relationship. Option D asks them to do work you have already done. Option A defers a known failure to the point where it is most expensive.

**Question 8 (harder) — An intermittent layout problem**

A component's layout breaks occasionally on one page but never in local development. What is the strongest hypothesis to test first?

- A) A CSS specificity conflict.
- B) Something varying at runtime that does not vary locally — most likely content length, since real data includes names and addresses far longer than test fixtures, or a web font loading late and reflowing the layout — and the diagnostic is to try the longest real content and to simulate a slow font load.
- C) A browser bug.
- D) A race condition in JavaScript.

**Correct answer: B**

**Explanation:** "Never locally, occasionally in production" points at something that differs between the two environments, and the two candidates in option B are by far the most common in frontend work. Local development uses short, tidy fixture data; production contains a 60-character surname and a five-line address. Local development loads fonts from cache instantly; a real user gets a fallback font first and a reflow when the web font arrives. Both are easy to test deliberately. Option A would be consistent rather than occasional. Options C and D are possible and much rarer, and neither explains the environment difference.

**Question 9 (harder) — Reuse and openness**

You are building a component that another team will likely need. What most affects whether they can actually reuse it?

- A) Publishing it in a shared repository.
- B) Whether it can be used without adopting your assumptions — a component tightly coupled to your page's CSS, your data shape or your build setup is technically available and practically unusable, so the reusable version is the one with a clear interface, no dependency on ambient styles, and documented behaviour.
- C) Writing good documentation.
- D) Making it configurable.

**Correct answer: B**

**Explanation:** Availability and reusability are different properties, and the gap between them is where shared component libraries go to die. A component that inherits styles from a parent, expects a particular data structure, or requires a specific bundler configuration will be copied and modified rather than reused, which is the outcome sharing was meant to avoid. Option B names the three couplings that matter. Option C is necessary and does not help if the component cannot be dropped in. Option D can actively hurt, since a component with thirty options is harder to adopt than one that does one thing. Option A is the precondition.

**Question 10 (harder) — Distinguishing symptom from cause**

Screen reader users report that after submitting a form with errors, they do not realise anything has happened. The error messages are correctly marked up and associated with their fields. What is the strongest hypothesis?

- A) The error markup is wrong after all.
- B) The markup being correct is consistent with the problem: nothing has told the user that the submission failed or moved their attention to the errors, so focus probably remains where it was and there is no announcement — the usual fix is to move focus to an error summary at the top of the page, which both announces the failure and provides links to each field.
- C) The screen reader is not supported.
- D) The errors need `aria-live` regions.

**Correct answer: B**

**Explanation:** The scenario tells you the association markup is correct, which redirects attention to the question of attention itself. A sighted user sees the page change; a screen reader user, with focus unchanged and nothing announced, has no signal at all. Moving focus to a heading in an error summary is the established pattern in government services precisely because it solves both problems at once. Option D would announce something and is a weaker solution here, because a live region announcement interrupts without giving the user a way to navigate to the problems. Option A contradicts the premise. Option C blames the tool.

**Question 11 (harder) — A trade-off between two user groups**

An interaction that would be much clearer for most users relies on hover, which does not exist on touch devices. What is the strongest approach?

- A) Implement the hover interaction; most users are on desktop.
- B) Treat hover as an enhancement over an interaction that works without it — a pattern accessible by tap and by keyboard, with hover adding convenience where available — because hover-only interactions exclude touch users, keyboard users and many assistive technology users simultaneously, and the excluded groups overlap heavily with those who most need the service to work.
- C) Build separate mobile and desktop versions.
- D) Replace hover with click for everyone.

**Correct answer: B**

**Explanation:** Hover-dependent interactions fail for a larger and more varied group than the framing suggests: touch users, keyboard users, switch users, and anyone using a screen reader. Option B applies the progressive enhancement pattern to interaction rather than to script — build the version that works for everyone, then add the hover affordance on top. Option D is defensible and discards a genuine improvement for pointer users. Option C doubles the maintenance and the divergence, and device detection is unreliable. Option A weighs convenience for the majority against exclusion of a minority, which is the wrong comparison in a public service.

**Question 12 (harder) — Coaching judgement**

A junior colleague's pull request works correctly but uses a pattern your team has moved away from. What is the strongest response?

- A) Approve it; it works.
- B) Explain what the team moved to and why, in the review, and ask them to change it — because the reason is the transferable part, and a junior developer who understands why the pattern was abandoned will recognise the next instance, whereas one who is simply corrected will not.
- C) Change it yourself before merging.
- D) Approve it and mention the pattern separately.

**Correct answer: B**

**Explanation:** Your role names coaching and mentoring more junior colleagues, and code review is where most of that actually happens. The reason is the payload — "we moved away from this because it breaks when content wraps" teaches something reusable, while "please use X instead" teaches one substitution. Option C removes both the learning and their ownership of their own change. Option D is close and weaker, because feedback separated from the code it refers to is much harder to apply. Option A lets a deprecated pattern spread and, over time, makes the team's stated conventions meaningless.

### Preparation tips

- **Ask what happens when the JavaScript does not run.** Every time.
- **Reach for the native element first.** Effort spent rebuilding button behaviour is a signal.
- **Prioritise accessibility findings by whether they block a task.**
- **Treat "doesn't work" as a request for three more facts.**
- **Suspect content length and font loading for problems that never reproduce locally.**
- **Compare lab data against field data segmented by device and connection.**
- **Raise design accessibility issues with measurements and a proposed alternative.**
- **Give the reason, not the correction, when reviewing a junior colleague's code.**

### Common pitfalls to avoid

- **Patching a `<div>` with ARIA instead of using a `<button>`.**
- **Testing mobile problems in a desktop device emulator.**
- **Treating a synthetic performance score as a description of user experience.**
- **Building a design you know fails contrast, to raise later.**
- **Assuming a component is reusable because it is published.**
- **Adding a live region where moving focus is the correct fix.**
- **Making hover the only route to an interaction.**
- **Approving a deprecated pattern because the code works.**

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment tests whether you can draw a defensible conclusion from data under time pressure. For a frontend developer the data is performance metrics, analytics segmented by device and browser, accessibility audit results, bundle sizes and test coverage.

The format is typically fifteen to twenty-five minutes with a calculator permitted, presenting tables and charts followed by multiple-choice questions. Some items are computational; others ask what the data does and does not support.

Three habits matter particularly in frontend work.

The first is that averages hide the users you most need to know about. Mean page load time is dominated by fast connections and modern devices, and the users having a bad time are in the tail.

The second is that percentages of a large user base are people. A browser used by 0.4% of visitors to a service with two million annual users is eight thousand people, which is not a rounding error.

The third is that bytes are not time. A 200KB reduction in a bundle matters differently depending on whether it was images on a fast connection or JavaScript being parsed on a slow phone.

### How this assessment maps to your role

- **Performance metrics** map to **Web performance optimisation**, where you identify and resolve issues.
- **Segmented analytics** map to **User focus (frontend developer)**, where you champion research covering all users.
- **Accessibility audit data** maps to **Accessibility**.
- **Bundle and asset arithmetic** maps to **Systems integration (frontend developer)**, where you build static assets.
- **Coverage and defect figures** map to **Programming and build (frontend developer)**.
- **Presenting figures to stakeholders** maps to **Communicating information**.

### Practice questions

*Table 1 — Page load performance by device category, last 30 days*

| Device category | Sessions | Median LCP (s) | 75th percentile LCP (s) | 95th percentile LCP (s) |
|---|---|---|---|---|
| Desktop | 240,000 | 1.4 | 2.1 | 3.6 |
| High-end mobile | 180,000 | 1.9 | 3.0 | 5.2 |
| Mid-range mobile | 260,000 | 3.1 | 5.4 | 9.8 |
| Low-end mobile | 70,000 | 5.6 | 9.1 | 16.4 |

**Question 1 (easy) — Reading a table**

How many sessions were on mobile devices of any kind?

- A) 440,000
- B) 510,000
- C) 330,000
- D) 750,000

**Correct answer: B**

**Explanation:** 180,000 + 260,000 + 70,000 = 510,000. Total sessions across all categories are 750,000, so mobile is 68% of traffic — worth establishing early, because the table's most striking figures are all in the mobile rows and they describe most of the users.

**Question 2 (easy) — Comparing percentiles**

Approximately how many times slower is the 75th percentile LCP on low-end mobile than on desktop?

- A) About 2.5 times
- B) About 4.3 times
- C) About 6 times
- D) About 3 times

**Correct answer: B**

**Explanation:** 9.1 / 2.1 = 4.33. A quarter of low-end mobile sessions wait more than nine seconds for the main content to appear, against 2.1 seconds for the equivalent desktop user. The Core Web Vitals threshold for a "good" LCP is 2.5 seconds at the 75th percentile, which desktop passes and every mobile category fails.

**Question 3 (moderate) — Weighted median**

What is the approximate session-weighted median LCP across all four categories?

- A) About 2.5s
- B) About 2.8s
- C) About 3.0s
- D) About 1.9s

**Correct answer: A**

**Explanation:** Weight each median by sessions: (240,000 × 1.4) + (180,000 × 1.9) + (260,000 × 3.1) + (70,000 × 5.6) = 336,000 + 342,000 + 806,000 + 392,000 = 1,876,000 second-sessions. Divide by 750,000 sessions = 2.50s. The unweighted mean of the four medians is (1.4 + 1.9 + 3.1 + 5.6)/4 = 3.0s, which is option C and the standard trap — it treats the 70,000 low-end mobile sessions as equal in weight to the 260,000 mid-range ones. Note also that a weighted average of medians is not the true overall median; it is a comparison figure rather than a statistic to quote as the service's median.

**Question 4 (moderate) — Users behind a percentage**

The service has 750,000 sessions a month. A browser used by 0.6% of sessions has a rendering bug on your new component. How many sessions a month are affected, and does it warrant a fix?

- A) 450 sessions; not worth fixing.
- B) 4,500 sessions a month — around 54,000 a year — which is a small percentage and a large number of people, so whether it warrants a fix depends on what the bug does, not on the percentage.
- C) 45,000 sessions; must be fixed.
- D) 4,500 sessions; not worth fixing.

**Correct answer: B**

**Explanation:** 750,000 × 0.006 = 4,500 sessions a month. The arithmetic is the smaller half of the item. Percentages in the tenths sound negligible and describe substantial numbers of people at government service volumes, and the honest framing is that severity decides it: a cosmetic misalignment affecting 4,500 people is different from a component they cannot operate. Converting rates into counts before the conversation happens is the habit worth building, because everyone in the room hears "0.6%" as "nobody".

**Question 5 (moderate) — Contrast ratio**

A designer proposes body text at a contrast ratio of 4.2:1 and a heading at 24px bold with a ratio of 3.1:1. Which passes WCAG 2.2 AA?

- A) Both pass.
- B) Neither passes.
- C) The heading passes; the body text does not.
- D) The body text passes; the heading does not.

**Correct answer: C**

**Explanation:** WCAG AA requires 4.5:1 for normal text and 3:1 for large text, where large means at least 18pt (24px) regular or 14pt (18.66px) bold. The heading at 24px bold qualifies as large text and 3.1:1 clears the 3:1 threshold. The body text at 4.2:1 falls short of 4.5:1. The margin is small in both cases, which is worth flagging to a designer — a ratio of 3.1:1 leaves no room for a later tweak to either colour.

*Table 2 — Bundle composition before and after optimisation*

| Asset type | Before (KB) | After (KB) |
|---|---|---|
| JavaScript | 480 | 190 |
| CSS | 120 | 95 |
| Images | 1,340 | 410 |
| Fonts | 180 | 90 |

**Question 6 (moderate) — Total reduction**

What is the approximate percentage reduction in total transferred bytes?

- A) About 45%
- B) About 63%
- C) About 71%
- D) About 55%

**Correct answer: B**

**Explanation:** Before: 480 + 120 + 1,340 + 180 = 2,120KB. After: 190 + 95 + 410 + 90 = 785KB. Reduction: 1,335KB, which is 1,335/2,120 = 63.0%. A useful figure and, as the next question shows, not the one that best predicts the improvement users feel.

**Question 7 (harder) — Which reduction matters most**

Which change in Table 2 is likely to most improve experience on a low-end mobile device?

- A) The image reduction, since it is the largest in bytes.
- B) The JavaScript reduction, because JavaScript must be parsed, compiled and executed on the main thread as well as downloaded, and on a low-end device that processing cost is several times higher than on a development machine — so 290KB less JavaScript typically buys more responsiveness than 930KB less image data, which mostly costs download time and can be lazy-loaded.
- C) The font reduction, because fonts block text rendering.
- D) They are equivalent per byte saved.

**Correct answer: B**

**Explanation:** This is the central asymmetry in web performance: bytes of JavaScript are far more expensive than bytes of image data, because images decode off the main thread and can be deferred, while JavaScript blocks it. On a low-end Android device, parse and execute time for a few hundred kilobytes of script can run into seconds. Option A picks the largest number, which is the intuitive answer and the wrong one. Option C names a real effect — fonts can block text rendering — and 90KB is a small saving relative to the script. Option D asserts a per-byte equivalence that is precisely what does not hold.

**Question 8 (harder) — Accessibility audit arithmetic**

An audit of 40 pages found 96 issues: 12 critical, 31 serious, 38 moderate, 15 minor. Critical and serious issues take an average of 90 minutes each to fix; moderate and minor average 25 minutes. What is the approximate total effort?

- A) About 65 hours
- B) About 87 hours
- C) About 42 hours
- D) About 110 hours

**Correct answer: B**

**Explanation:** Critical and serious: 12 + 31 = 43 issues × 90 minutes = 3,870 minutes. Moderate and minor: 38 + 15 = 53 × 25 = 1,325 minutes. Total 5,195 minutes = 86.6 hours, so about 87. Roughly two and a half weeks of one person's time, which is the kind of figure that turns "we should fix the audit findings" into something that can be planned and prioritised. Note the concentration: the 43 higher-severity issues account for three-quarters of the effort.

**Question 9 (harder) — Interpreting a change**

After a release, bounce rate on a key page fell from 34% to 29% and average session duration fell from 4:10 to 3:20. What is the strongest interpretation?

- A) The release improved the page; bounce rate fell.
- B) Both metrics moved and they point in ambiguous directions — fewer people leaving immediately alongside shorter sessions is consistent with users finding what they need faster, which is good, and also with them giving up sooner, which is not — so a task completion measure is needed before calling it either way.
- C) The release made things worse; sessions are shorter.
- D) The two metrics are unrelated.

**Correct answer: B**

**Explanation:** Session duration is one of the most frequently misread metrics in web analytics, because longer can mean engaged or lost and shorter can mean efficient or abandoned. Here the two figures are individually ambiguous and jointly still ambiguous. Option B says so and names what would resolve it, which is whether people completed the task. Options A and C each pick the metric that supports a preferred story. Option D asserts independence between two measures of the same sessions.

**Question 10 (harder) — Sampling in performance data**

Your real user monitoring samples 5% of sessions. In the last week it recorded 42 sessions with an LCP above 20 seconds. Approximately how many such sessions occurred?

- A) 210
- B) 840
- C) 2,100
- D) 42

**Correct answer: B**

**Explanation:** A 5% sample means the recorded figure represents about 1/0.05 = 20 times as many actual sessions: 42 × 20 = 840. Roughly 840 people last week waited over twenty seconds for the main content. Forgetting to scale a sampled figure is a common and consequential error, because 42 sounds like an anomaly and 840 sounds like a defect. Option A divides by five rather than multiplying by twenty.

**Question 11 (harder) — Browser support decision**

A browser accounts for 1.2% of your 750,000 monthly sessions. Supporting a feature in it would take about three days of work and add ongoing maintenance. What is the strongest framing?

- A) 1.2% is too small to justify three days.
- B) 1.2% is 9,000 sessions a month, so the question is what those users cannot do without the work — if the feature is an enhancement and the baseline still works for them, three days is poor value; if they cannot complete the task, 9,000 people a month is a strong case regardless of the percentage.
- C) All browsers should be supported equally.
- D) 9,000 sessions justifies the work.

**Correct answer: B**

**Explanation:** The percentage alone cannot answer this and neither can the count. What decides it is whether the affected users can still complete their task through the baseline experience — which is precisely what progressive enhancement is for, and why a service built that way can make this decision calmly. Option B holds both facts and applies the right test. Option A treats the percentage as decisive. Option D treats the count as decisive. Option C ignores cost entirely, which is not a position that survives contact with a backlog.

**Question 12 (harder) — Presenting a figure to a stakeholder**

You need to make the case for performance work to a service owner. Which figure is most persuasive and most honest?

- A) The median LCP improved from 3.1s to 2.2s.
- B) The proportion of sessions meeting the Core Web Vitals "good" threshold, broken down by device category — because it maps directly onto how many people had an acceptable experience, exposes that mid-range and low-end mobile users are the ones affected, and is harder to improve by helping users who were already fine.
- C) Total page weight fell by 63%.
- D) The Lighthouse score rose from 62 to 91.

**Correct answer: B**

**Explanation:** Option B is a count of people helped, segmented so the service owner can see who they were. That segmentation is what makes it honest — an aggregate improvement can be driven entirely by desktop users who were already fast, and a per-device breakdown shows whether the work reached the users who needed it. Option A is a real improvement and a single number that hides the distribution. Option C measures bytes, which the service owner has no way to interpret. Option D is a lab score on a simulated device, and a stakeholder who learns that the number does not describe real users will discount everything you present afterwards.

### Preparation tips

- **Weight averages by sessions.** The unweighted mean of medians is the standard distractor.
- **Convert percentages to counts before discussing them.**
- **Scale sampled figures by the inverse of the sampling rate.**
- **Know the WCAG thresholds.** 4.5:1 normal text, 3:1 large text, large being 24px regular or 18.66px bold.
- **Treat JavaScript bytes as more expensive than image bytes.**
- **Segment performance data by device category before drawing conclusions.**
- **Distrust session duration as a quality signal.**
- **Lead with the proportion of users having a good experience.**

### Common pitfalls to avoid

- **Averaging medians without weighting by traffic.**
- **Reading 0.6% as negligible at 750,000 sessions.**
- **Reporting a sampled count as an absolute count.**
- **Assuming the largest byte reduction is the largest improvement.**
- **Interpreting shorter sessions as either good or bad without a task measure.**
- **Presenting a Lighthouse score as evidence about real users.**
- **Deciding browser support on the percentage alone.**

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment tests whether you can determine precisely what a piece of written material establishes. For a frontend developer that material is accessibility standards, design system documentation, browser specifications, service standards and research findings.

The commonest format presents a passage followed by statements to be marked True, False or Cannot Say. True means the passage establishes it, False means the passage contradicts it, and Cannot Say means it does neither — regardless of what you happen to know. Your professional knowledge is the main hazard: you will frequently know the right answer about accessibility while the passage in front of you has not said it.

Three specifics matter in this domain.

The first is that accessibility standards are written with precise conditions — thresholds, exceptions for particular content types, and success criteria that apply only at certain conformance levels. Reading past a condition changes what the standard requires.

The second is that "must", "should" and "may" are terms of art in service standards and specifications, and treating them loosely leads to building the wrong thing or blocking the wrong thing.

The third is that user research findings describe what was observed with particular participants, and generalising past that is the commonest misuse of research in a design conversation.

### How this assessment maps to your role

- **Reading accessibility standards precisely** maps to **Accessibility**, where you build to a predefined set of standards.
- **Reading specifications** maps to **Programming and build (frontend developer)**, where you work from agreed specifications.
- **Reading research findings** maps to **User focus (frontend developer)**.
- **Reading design system documentation** maps to **Prototyping** and establishing design patterns.
- **Reading strategy and policy** maps to **Strategic thinking**.
- **Precise communication** maps to **Communicating information**.

### Practice questions

*Passage A — for Questions 1 to 4*

"Text and images of text must have a contrast ratio of at least 4.5:1 against their background. Large-scale text and images of large-scale text must have a ratio of at least 3:1. This requirement does not apply to text that is part of an inactive user interface component, that is pure decoration, that is not visible to anyone, or that is part of a picture containing significant other visual content. Logotypes are also exempt. User interface components and graphical objects required to understand content must have a contrast ratio of at least 3:1 against adjacent colours."

**Question 1 (easy)**

Statement: Body text must have a contrast ratio of at least 4.5:1.

- A) True
- B) False
- C) Cannot Say

**Correct answer: A**

**Explanation:** Stated directly in the first sentence, and body text is neither large-scale nor covered by any of the listed exemptions. The baseline item.

**Question 2 (moderate)**

Statement: The border of an input field must have a contrast ratio of at least 4.5:1 against the background.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The passage sets 3:1 for "user interface components and graphical objects required to understand content", and an input field border is a user interface component rather than text. The statement applies the text threshold to a non-text element, so the passage contradicts it — 4.5:1 would satisfy 3:1, but the statement asserts that 4.5:1 is required, which is not what the passage says. Reading the text ratio as universal is a common and expensive error, because it leads to rejecting compliant designs.

**Question 3 (moderate)**

Statement: Text appearing in a photograph of a street scene is exempt from the contrast requirement.

- A) True
- B) False
- C) Cannot Say

**Correct answer: A**

**Explanation:** The passage exempts text "that is part of a picture containing significant other visual content". A photograph of a street scene contains significant other visual content, so incidental text within it — a shop sign, a road marking — falls within the exemption. The passage establishes this. Note that the exemption is about the text being incidental to a picture, not about the text being unimportant, which is a distinction worth keeping if the picture is being used to convey information.

**Question 4 (harder)**

Statement: A disabled button's label is exempt from the contrast requirement.

- A) True
- B) False
- C) Cannot Say

**Correct answer: A**

**Explanation:** The passage exempts text "that is part of an inactive user interface component", and a disabled button is an inactive component. So its label is exempt. This is the item where professional judgement pulls against the text most strongly — low-contrast disabled states are a genuine usability problem and many teams choose to exceed the requirement — and the question asks what the standard requires, not what is good practice. Both things can be true: the exemption exists, and relying on it is often a poor choice.

*Passage B — for Questions 5 to 8*

"The design system component library provides a date input pattern consisting of three separate text fields for day, month and year. Research with 340 participants found that this pattern produced fewer errors than a single text field or a calendar picker for entering dates in the past, such as a date of birth. The guidance notes that a calendar picker may be more appropriate for selecting dates in the near future, such as an appointment, where the day of the week is relevant. Teams departing from the component library pattern should record the reason and the research supporting the alternative. The component library is updated quarterly; proposals for new patterns are reviewed by the design system working group."

**Question 5 (easy)**

Statement: The design system's date input pattern uses three separate fields.

- A) True
- B) False
- C) Cannot Say

**Correct answer: A**

**Explanation:** Stated directly: day, month and year as three separate text fields. Straightforward.

**Question 6 (moderate)**

Statement: The three-field pattern produces fewer errors than a calendar picker for booking an appointment.

- A) True
- B) False
- C) Cannot Say

**Correct answer: C**

**Explanation:** The research finding is scoped to "entering dates in the past, such as a date of birth". An appointment is a date in the near future, which the passage explicitly identifies as a case where a calendar picker "may be more appropriate". So the finding does not extend to the appointment case, and the passage does not establish the opposite either — "may be more appropriate" is not a research result. This is the characteristic misuse of a research finding: taking a result established in one context and applying it generally.

**Question 7 (moderate)**

Statement: A team may not use a calendar picker.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The passage contradicts this twice over. It says a calendar picker "may be more appropriate" for near-future dates, and it provides a route for departing from the library pattern — recording the reason and supporting research. Departure is permitted and conditioned, not prohibited. Note the obligation attached to departure is "should record", not "must", which is a further softening.

**Question 8 (harder)**

Statement: A new pattern proposed to the design system working group will be available in the component library within three months.

- A) True
- B) False
- C) Cannot Say

**Correct answer: C**

**Explanation:** The passage says the library is updated quarterly and that proposals are reviewed by the working group. It does not say that review takes place within one quarter, that review results in acceptance, or that an accepted pattern appears in the next release. Three separate unestablished steps sit between the proposal and the outcome the statement asserts. Chaining plausible inferences across a process the passage only partly describes is a reliable way to reach a Cannot Say item with a confident True.

*Passage C — for Questions 9 to 12*

"Services must work without JavaScript for all essential functions, unless the department's technical design authority has agreed an exemption. Where an exemption is agreed, the service must still work with assistive technologies and must degrade gracefully when JavaScript fails to load. Services should be tested on the browsers used by at least 95% of the service's users, and must be tested with at least one screen reader on at least one desktop and one mobile platform. Testing on a physical device is preferred to emulation. Where a service is used predominantly on mobile, mobile testing should be prioritised accordingly."

**Question 9 (moderate)**

Statement: A service with an agreed exemption need not work when JavaScript fails to load.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The passage contradicts this: even where an exemption is agreed, the service "must degrade gracefully when JavaScript fails to load". The exemption releases the service from working without JavaScript for essential functions; it does not release it from behaving acceptably when the script fails. The second sentence exists precisely to close this inference, and the distinction between "works without JavaScript" and "degrades gracefully when JavaScript fails" is a real one worth being able to articulate.

**Question 10 (moderate)**

Statement: A service must be tested on the browsers used by at least 95% of its users.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The passage uses "should" for the 95% browser coverage and "must" for screen reader testing in the very next clause. The contrast within a single sentence is deliberate, and the statement's "must" overstates the obligation. Reading the two clauses as carrying the same weight is the error, and it matters practically: browser coverage is negotiable under pressure and screen reader testing is not.

**Question 11 (moderate)**

Statement: Emulated device testing does not satisfy the mobile screen reader requirement.

- A) True
- B) False
- C) Cannot Say

**Correct answer: C**

**Explanation:** The passage says physical device testing "is preferred to emulation", which expresses a preference without establishing that emulation fails to satisfy the requirement. A preference ranks two acceptable options; a requirement excludes one. The statement asserts exclusion. Professionally you would be right that emulated screen reader testing is close to worthless, and the passage has not said so.

**Question 12 (harder)**

Statement: A service used predominantly on desktop must still be tested with a mobile screen reader.

- A) True
- B) False
- C) Cannot Say

**Correct answer: A**

**Explanation:** The screen reader requirement is unconditional: test "with at least one screen reader on at least one desktop and one mobile platform". The later sentence about prioritising mobile testing where usage is predominantly mobile adjusts emphasis, not the baseline obligation — and prioritisation between two required activities does not remove either. So a desktop-dominant service still owes mobile screen reader testing. Reading the prioritisation clause as creating an exemption is the trap, and it is the same shape as an exception that turns out to be a preference.

### Preparation tips

- **Check whether a threshold applies to text or to components.** They differ.
- **Read the exemption list before concluding a requirement applies.**
- **Note the scope of a research finding before generalising it.**
- **Distinguish "should" from "must" within the same sentence.**
- **Distinguish a preference from a requirement.**
- **Watch for a second sentence that closes the obvious inference.**
- **Count the unestablished steps before accepting a chained conclusion.**
- **Read a prioritisation clause as emphasis, not as an exemption.**

### Common pitfalls to avoid

- **Applying the 4.5:1 text ratio to user interface components.**
- **Extending a research finding past the context it was established in.**
- **Reading "may be more appropriate" as a research result.**
- **Treating an exemption from one obligation as an exemption from all.**
- **Reading "is preferred to" as prohibiting the alternative.**
- **Answering from accessibility knowledge rather than from the passage.**
- **Assuming a proposal reviewed quarterly is accepted quarterly.**

## Workplace job-specific situational judgement assessment

### About this assessment

A workplace job-specific situational judgement assessment presents realistic scenarios from your role and asks you to identify effective and ineffective responses. For a frontend developer the scenarios involve working across disciplines, defending accessibility under delivery pressure, giving and receiving design feedback, mentoring, and handling technical disputes.

The commonest formats ask you to select the most and least effective response, or to rate each. Scoring is against a key derived from experienced practitioners in comparable roles, so you are aiming at professional consensus rather than personal preference.

Three patterns run through the strong answers at this level.

The first is that accessibility is not a negotiation you win by refusing. It is a requirement, and the effective move is almost always to make the cost and consequence visible early enough that nobody has to choose under pressure.

The second is that you work with designers, content designers, user researchers and backend developers who each hold information you do not. Responses that gather their perspective before deciding are consistently stronger than ones that resolve alone.

The third is that your role names resolving technical disputes among peers, which means the way you disagree is part of the job rather than incidental to it.

### How this assessment maps to your role

- **Championing accessibility** maps to **Accessibility**, where you champion it to internal stakeholders.
- **Cross-discipline collaboration** maps to **Community collaboration** and **User focus**.
- **Managing stakeholder expectations** maps to **Communicating information**.
- **Resolving disputes** maps to **Leadership and guidance (frontend developer)**.
- **Coaching** maps to your role level's mentoring responsibility.
- **Performance advocacy** maps to **Web performance optimisation**.

### Practice questions

**Question 1 (easy) — Accessibility under deadline**

Two days before release, you find that a new component is not keyboard operable. Fixing it properly means restructuring it. What is the most effective response?

- A) Release it and fix it in the next sprint.
- B) Say clearly what it means — that keyboard and screen reader users cannot use this part of the service — and put the options to the service owner, including releasing without the component, releasing with a simpler accessible version, or delaying, because this is their decision and it needs to be made knowingly.
- C) Refuse to release.
- D) Add a keyboard handler as a quick patch.

**Correct answer: B. Least effective: A**

**Explanation:** The decision belongs to the service owner and your job is to make sure they make it with the consequence in front of them, in plain terms rather than as a technical finding. Option B also brings options, and the middle one — a simpler accessible version — is frequently available and frequently not considered under time pressure. Option A is least effective because it releases a known barrier and "next sprint" for accessibility fixes has a poor track record. Option C removes the owner from a decision that is theirs. Option D risks a patch that appears to work and fails for actual screen reader users, which is worse than a visible gap because nobody will look again.

**Question 2 (easy) — A designer's request you disagree with**

A designer asks you to build an animation you think will be distracting. What is the most effective response?

- A) Build it; design decisions are theirs.
- B) Ask what the animation is meant to do — draw attention to a change, signal progress, or provide continuity — and raise your concern in those terms, along with the practical point that it will need to respect reduced-motion preferences.
- C) Explain that animations harm performance.
- D) Build a subtler version.

**Correct answer: B. Least effective: D**

**Explanation:** Asking about intent turns a difference of taste into a discussion about whether the thing works, and it frequently reveals a purpose you can serve more simply. The reduced-motion point is concrete and non-negotiable, which is useful to raise early rather than as an objection. Option D is least effective: silently building something other than what was asked for is a decision made on the designer's behalf without telling them, and it damages the working relationship more than a direct disagreement would. Option A abandons the feedback role your skills name. Option C leads with an argument that may not be true and is not your actual concern.

**Question 3 (moderate) — A stakeholder wants a component from another site**

A senior stakeholder wants a component copied from a commercial website. It does not fit the design system and has accessibility problems. What is the most effective response?

- A) Explain that it does not meet the design system standards.
- B) Find out what they liked about it — usually a specific quality such as feeling faster, looking more modern, or making one action more prominent — and propose how to achieve that within the design system, because the underlying want is almost always achievable and the specific component almost never is.
- C) Build it with the accessibility problems fixed.
- D) Explain the accessibility problems and decline.

**Correct answer: B. Least effective: C**

**Explanation:** "Make it like that site" is a symptom rather than a request, and the useful move is finding the quality they are responding to. Option B does that and offers a route, which is what makes it a collaboration rather than a refusal. Option C is least effective because it delivers a component outside the design system and inconsistent with the rest of the service, and having complied once you will be asked again. Options A and D are both accurate and both lead with what cannot happen, which invites the stakeholder to treat standards as an obstacle rather than as something on their side.

**Question 4 (moderate) — Disagreement with a backend developer**

A backend developer proposes an API shape that would force awkward data handling in the frontend. They believe it is cleaner on their side. What is the most effective response?

- A) Accept it; the API is their decision.
- B) Set out concretely what it costs on the frontend — the specific transformations, the extra requests, or the state you would have to hold — and look for a shape that serves both, since "cleaner" on either side is a judgement and the total cost across both is the thing that matters.
- C) Escalate to a lead.
- D) Build the workarounds; it is not worth the argument.

**Correct answer: B. Least effective: C**

**Explanation:** Option B moves the conversation from two aesthetic preferences to a comparison of concrete costs, which is resolvable. Your role names resolving technical disputes taking all views into account, and the "serves both" framing is what makes that possible. Option C is least effective as a first move: escalating a routine technical disagreement between two developers signals that you cannot work it out, and it usually returns with a decision worse than either of you would have reached. Option D accepts a lasting cost to avoid a short conversation. Option A concedes a boundary that is genuinely shared.

**Question 5 (moderate) — Research findings you disagree with**

User research shows that people are not noticing a component you built and are confident works well. What is the most effective response?

- A) Accept the finding and change the component.
- B) Ask the researcher about the specifics — what people were trying to do, where their attention was, how many participants and in what context — because that will tell you whether the fix is the component, its placement, or the surrounding content, and the answer is frequently not the component at all.
- C) Question the research methodology.
- D) Ask for the research to be repeated.

**Correct answer: B. Least effective: C**

**Explanation:** The finding is that people did not notice it, which is a fact about attention rather than about the component, and the remedy depends on why. Option B gets the detail that distinguishes a component problem from a placement problem or a page problem. Option C is least effective, and it is what defensiveness sounds like — challenging methodology in response to an unwelcome finding, before understanding it, is the fastest way to stop being included in research. Option A over-corrects and may change the wrong thing. Option D is expensive and usually unnecessary.

**Question 6 (moderate) — Mentoring through a mistake**

A junior colleague you mentor has shipped a change that broke a page in one browser. They are visibly upset. What is the most effective response?

- A) Fix it quickly and reassure them.
- B) Get the fix done with them rather than for them, and separately treat it as a question about the process — a break that reached production means testing did not cover that browser, which is a team gap rather than their error.
- C) Tell them not to worry; everyone breaks things.
- D) Talk them through what they should have checked.

**Correct answer: B. Least effective: A**

**Explanation:** Two things need to happen and option B does both: the fix, done together so they learn the diagnosis, and the honest reframing that a change reaching production untested in a supported browser reflects a process gap rather than individual carelessness. That reframing is accurate and it is also what lets them stay confident. Option A is least effective — taking over the fix at the moment they feel worst confirms that they cannot be trusted with it. Option D puts the responsibility on them alone. Option C is kind and misses the chance to change anything.

**Question 7 (harder) — Pressure to drop progressive enhancement**

A delivery manager asks whether the team could move faster by dropping the no-JavaScript baseline, noting that "almost everyone has JavaScript". What is the most effective response?

- A) Explain that progressive enhancement is a government standard.
- B) Answer the actual question about speed honestly — for some components the baseline does cost time, and for many it costs almost nothing — and set against it the number of sessions where scripts fail for reasons unrelated to whether the user "has JavaScript", along with what those users would be unable to do.
- C) Explain that JavaScript fails more often than people think.
- D) Agree, provided the critical journeys keep a baseline.

**Correct answer: B. Least effective: A**

**Explanation:** The delivery manager has asked a reasonable question and deserves a real answer, including the part that concedes ground — the baseline genuinely does cost time on some components, and pretending otherwise is why these conversations go badly. Option B is honest in both directions and reframes the risk correctly: script failure is about networks, proxies and errors, not about users choosing to disable anything. Option A is least effective because citing a standard answers a cost question with an authority claim, which invites someone to seek an exemption. Option C is true and unquantified. Option D concedes the structure before the discussion.

**Question 8 (harder) — An accessibility problem in someone else's code**

Reviewing another team's component, you find it is unusable with a screen reader. It is already in production and used by three services. What is the most effective response?

- A) Report it through the accessibility reporting process.
- B) Contact the owning team directly with the specific problem and how you found it, offering to pair on the fix — and make sure the three consuming services know, because they are the ones with the accessibility obligation to their users and may need an interim mitigation.
- C) Fix it and raise a pull request.
- D) Advise the three services to stop using it.

**Correct answer: B. Least effective: D**

**Explanation:** Option B does the three necessary things: tells the people who can fix it, offers help, and informs the services that carry the legal and moral obligation to their own users. That last part is the one most often skipped and it matters, because a service unaware of a barrier cannot mitigate it. Option D is least effective as a first move — telling three services to remove a production component before its owners have had a chance to fix it creates a large amount of work and is likely to be ignored. Option C is generous and can land badly as an unsolicited rewrite of another team's component. Option A is appropriate and slow on its own.

**Question 9 (harder) — Performance work with no obvious sponsor**

You can see that the service is slow for mid-range mobile users, but no one has asked for performance work and the backlog is full. What is the most effective response?

- A) Do it gradually alongside other work.
- B) Make it visible with the numbers segmented by device — what proportion of users are affected and what they experience — and put it to the service owner as a prioritisation decision, because performance work competes for the same time as everything else and needs to be chosen rather than smuggled in.
- C) Raise it at a retrospective.
- D) Add performance tickets to the backlog.

**Correct answer: B. Least effective: A**

**Explanation:** The evidence is what makes this a decision rather than an opinion, and segmenting by device is what shows the service owner that a specific and identifiable group of their users is having a poor experience. Option A is least effective: doing unsanctioned work alongside sanctioned work makes both slower, is invisible if it succeeds, and looks like a missed estimate if it does not. Option D puts tickets in a queue that nobody will prioritise without the argument. Option C surfaces it to the team rather than to the person who decides.

**Question 10 (harder) — A dispute between two colleagues**

Two colleagues are in a stalled disagreement about a component's approach, and it is slowing the team. Neither has asked you to intervene. What is the most effective response?

- A) Stay out of it; it is not your dispute.
- B) Get them together and focus the discussion on what each approach optimises for and what the team's actual constraints are, because a stalled technical disagreement is usually two people optimising for different things without having said so — and your role includes resolving disputes among peers.
- C) Decide the question yourself.
- D) Suggest they escalate to a lead.

**Correct answer: B. Least effective: C**

**Explanation:** Most stalled technical disputes are not about the technical question; they are about unstated and differing priorities — one person optimising for readability, the other for performance, neither having said so. Naming that usually resolves it in minutes. Option B does this and is what your skills description means by resolving disputes taking all views into account. Option C is least effective — imposing your answer on a disagreement between peers who did not ask leaves both of them without ownership and does nothing about the underlying mismatch. Option A ignores a team problem you are positioned to fix. Option D escalates something resolvable.

**Question 11 (harder) — A design system constraint that does not fit**

The design system's pattern does not fit a genuine need in your service. What is the most effective response?

- A) Use the pattern anyway; consistency matters.
- B) Establish precisely where it fails for your users, look for a way to meet the need within the system, and if there genuinely is not one, depart from it deliberately — documenting the reason and the evidence, and feeding it back to the design system team, because a pattern that does not fit a real need is information they need.
- C) Build a custom component.
- D) Ask the design system team to change the pattern.

**Correct answer: B. Least effective: C**

**Explanation:** Option B follows the sequence that keeps both the service and the system healthy: establish the failure specifically, exhaust the in-system options, then depart with a record. The feedback loop is the part most often skipped, and it is how design systems improve — a documented mismatch is far more actionable to the system team than a general sense that the pattern is awkward. Option C is least effective as a first move because it forks the system silently and the next team hits the same problem. Option D asks for a change without the evidence that would justify it. Option A applies a pattern to users it does not serve.

**Question 12 (harder) — Being asked to certify accessibility**

A service owner asks you to confirm that the service is accessible before a launch. You have tested with one screen reader and fixed the audit findings. What is the most effective response?

- A) Confirm it; the audit findings are fixed and you have tested it.
- B) Say precisely what has been done and what has not — which standard was tested against, with what tools, on what platforms, and what has not been covered, particularly testing with actual disabled users — because "is it accessible" is a question no single person can answer yes to, and an unqualified confirmation is one you cannot support.
- C) Say it meets WCAG 2.2 AA.
- D) Decline to confirm.

**Correct answer: B. Least effective: A**

**Explanation:** Accessibility is not a binary state that one developer's testing establishes, and an unqualified yes will be quoted in an accessibility statement you cannot stand behind. Option B gives the service owner an accurate picture, which is what they need for the statement they are legally required to publish, and it names the largest gap — testing with disabled users, which no amount of automated or self-conducted testing substitutes for. Option A is least effective because it converts your partial testing into an organisational claim. Option C is a more specific version of the same overreach unless a full audit against that standard has been done. Option D withholds information you have.

### Preparation tips

- **Put accessibility decisions to the service owner in plain terms, with options.**
- **Ask what an animation or pattern is for before objecting to it.**
- **Find the quality behind "make it like that site".**
- **Compare concrete costs across both sides of an API boundary.**
- **Ask the researcher for specifics before accepting or disputing a finding.**
- **Treat a production break as a process gap.**
- **Segment performance evidence by device before asking for prioritisation.**
- **Say precisely what has and has not been tested.**

### Common pitfalls to avoid

- **Deferring a known accessibility barrier to the next sprint.**
- **Quietly building something other than what a designer asked for.**
- **Answering a cost question by citing a standard.**
- **Escalating a routine disagreement with another developer.**
- **Questioning research methodology in response to an unwelcome finding.**
- **Taking over a junior colleague's fix at the moment they feel worst.**
- **Forking the design system silently.**
- **Confirming that a service "is accessible".**

## Conclusion

You have worked through four assessments built around the reasoning a frontend developer in government actually uses, and it is worth drawing the threads together.

The cognitive section kept coming back to structure and failure. Effort spent rebuilding button behaviour with ARIA is a signal that the wrong element was chosen. A layout that never breaks locally and occasionally breaks in production is usually meeting real content lengths or a late-loading font. And the question "what happens when the JavaScript does not run" is not a philosophical commitment — it has a concrete answer for a measurable number of people, and progressive enhancement is what makes that answer acceptable.

The numeric section was about not being misled by your own metrics. Weight averages by traffic. Scale sampled counts. Know that 0.6% of a government service is thousands of people. And remember the asymmetry that decides most performance work: bytes of JavaScript cost far more than bytes of image data, because one blocks the main thread on a device far slower than yours and the other does not.

The verbal section was an exercise in reading standards exactly. The 4.5:1 ratio applies to text and 3:1 to user interface components. An exemption from working without JavaScript is not an exemption from degrading gracefully. A preference for physical devices does not prohibit emulation. And a research finding established for dates of birth says nothing about appointments.

The situational judgement section was mostly about working with other people whose expertise is not yours. The strong answers asked designers what an interaction was for, asked researchers what participants were actually doing, made accessibility decisions visible to the person who owns them, and — in the last question — declined to compress a complicated picture into a yes.

If one thing is worth carrying away, it is the pattern behind almost every accessibility question here: the effective move was never to refuse, and never to quietly comply. It was to make the consequence for real users visible, early, to the person who decides. That is what championing accessibility means in practice, and it is a skill that gets easier every time you use it.

Good luck. The work you do sits between a service and the people who have no choice but to use it, and care at this level genuinely shows.
