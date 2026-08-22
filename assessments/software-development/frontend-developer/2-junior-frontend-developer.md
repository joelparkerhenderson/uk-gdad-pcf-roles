# Junior Frontend Developer - Psychometric Assessment Resources

## Introduction

Welcome! This guide has been written especially for you as a junior frontend developer in the UK Government Digital and Data profession. You might be preparing for an internal assessment, applying for a developer post at the next level, working towards the end of a development programme, or simply curious about how psychometric assessments connect to your day-to-day work. Whatever brought you here, this guide will help you practise, reflect, and build real confidence.

Let's start with the basics: what is a psychometric assessment? It is a structured, standardised exercise that measures the thinking skills and workplace behaviours that predict success in a role. "Standardised" means everyone answers the same kinds of questions under the same conditions, so results are comparable and fair. These are not trick tests, and they are not IQ contests. They measure practical, everyday thinking — the kind you already use when you review a pull request, read an analytics dashboard, interpret a user story, or decide whether to push on alone or ask a senior developer for guidance.

Why do these assessments matter for your role in particular? As a junior frontend developer, you learn on the job by delivering software components. You work independently, with guidance from more senior developers, to identify user issues and needs. You write clean code that follows web standards, build user interfaces that meet accessibility standards, and build your understanding of how static assets are compiled, delivered, and presented by browsers. That mix — real independence plus real learning — is exactly what these assessments sample. The questions in this guide use the genuine materials of your working week: HTML, CSS, and JavaScript conventions, build pipelines, browser support tables, accessibility audit results, sprint boards, performance budgets, user research summaries, and messages from designers, analysts, and stakeholders.

This document is organised into four main sections, one for each assessment type you are likely to meet:

1. A **cognitive assessment** — pattern recognition, logical deduction, error checking, prioritisation, and applied problem solving, all using frontend artefacts.
2. A **numeric reasoning assessment** — percentages, ratios, averages, rates, and table reading, using data such as page weights, test pass rates, device analytics, and audit counts.
3. A **verbal reasoning assessment** — precise comprehension of role-relevant passages, with true/false/cannot-say judgements, inference, and clear-writing questions.
4. A **situational judgement assessment** — realistic dilemmas for a junior developer, asking you to pick the most effective and least effective responses.

Each section follows the same pattern: an explanation of what the assessment measures and why employers use it for your role, a map from the assessment's dimensions to the named skills in your role summary, a substantial set of practice questions with full worked explanations, practical preparation tips, and common pitfalls to avoid.

Here is how to get the most from this guide. Work through one section at a time, and attempt every question honestly — write your answer down before reading the explanation. Then read every explanation, including the ones for questions you answered correctly: the explanations teach transferable technique, not just answers. When something catches you out, treat it as a gift — that is the exact spot where practice will improve you fastest. Come back after a week and try the tricky ones again.

One more thing before you begin: you belong here. You are already delivering components that real people use to access public services. These assessments are simply a mirror held up to skills you exercise every day. Take your time, trust your method, and let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive assessment measures the precise mental processes your role demands, using realistic workplace material rather than abstract puzzles. Instead of shape sequences, you get the artefacts of frontend delivery: code snippets, naming conventions, dependency rules, build pipelines, review checklists, and browser support policies. The questions ask you to reason about them quickly and accurately.

The typical format is an online, timed test lasting 15 to 30 minutes, with roughly 15 to 30 multiple-choice questions across five dimensions: pattern recognition, logical deduction, error checking, prioritisation, and applied problem solving. Scoring is objective, comparing your responses with a norm group of people at a similar level. Many platforms are adaptive — questions get harder as you answer correctly — so a rising difficulty curve is usually a good sign, not a bad one. Employers typically receive a speed-and-accuracy profile rather than a single number, which means steady, careful work is rewarded.

Why do employers use this assessment for junior frontend developers? Because frontend delivery is precision work performed under time pressure. A single-character difference in a class name silently breaks styling. A misread rule in a review checklist ships an inaccessible form. A wrongly ordered build step produces stale assets. As a junior developer you now catch many of these issues yourself, before a senior colleague does — that is what "working independently, with guidance" means in practice. The cognitive assessment samples exactly that catching ability: can you spot the broken pattern, follow the rule chain to its real conclusion, check every item on the list, and rank competing demands sensibly? These are learnable skills, and the questions below train them using scenarios from your actual working week.

### How this assessment maps to your role

Each dimension of the assessment corresponds directly to named skills in your role summary:

- **Pattern recognition** maps to **Programming and build (frontend developer)** and **Modern development standards**: writing clean code that follows web standards means recognising and preserving patterns — naming conventions, component structures, folder layouts — and noticing immediately when something deviates.
- **Logical deduction** maps to **Systems integration (frontend developer)** and **Modern development standards**: explaining how browsers use static assets, and how different versions of an interface reach different browsers and devices, requires "if this, then that" reasoning about pipelines, caching, and fallbacks — the logic of progressive enhancement.
- **Error checking** maps to **Accessibility** and **Programming and build (frontend developer)**: building user interfaces that meet accessibility standards, and fixing issues under the direction of others, begins with systematic checking — labels, heading orders, contrast, focus states — against a defined standard.
- **Prioritisation** maps to **Communicating information** and **Community collaboration**: managing differing perspectives, being an advocate for the team, and recognising and dealing with issues all depend on judging urgency and impact together, then sequencing your work defensibly.
- **Applied problem solving** maps to **User focus (frontend developer)**, **Prototyping**, and **Strategic thinking**: identifying user issues and needs, choosing when a prototype will answer a question, and explaining the strategic context of your work all require decomposing a fuzzy situation into checkable steps.

As you practise, notice that every question is a miniature of something you already do — the assessment simply times it.

### Practice questions

**Question 1 (easy) — Pattern recognition in component naming**

Your team's design system prefixes shared components with `govuk-` and service-specific components with `app-`. Modifier classes append `--` and the modifier name. You review this list in a template:

1. `govuk-button`
2. `govuk-button--secondary`
3. `app-task-list`
4. `app-task-list-completed`

The fourth class is meant to style a completed variant of the task list. Which change would make it follow the convention?

- A) Rename it `govuk-task-list--completed`
- B) Rename it `app-task-list--completed`
- C) Rename it `app--task-list-completed`
- D) No change needed — it already follows the convention

**Correct answer: B**

**Explanation:** Work through the convention's two parts. Prefix: the task list is service-specific, so `app-` is correct — that eliminates option A, which would wrongly claim the component belongs to the shared design system. Modifier: variants append a double dash plus the modifier name to the block name, so the completed variant of `app-task-list` must be `app-task-list--completed`. The original uses a single dash, which reads as part of the component name rather than a modifier — a subtle but real difference, because tooling, documentation, and teammates all rely on the double-dash signal to distinguish "a different component" from "a variant of this component". Option C puts the double dash in the wrong place, breaking the block name itself. Conventions like this are the backbone of clean, reusable code — one of your role's core responsibilities — and assessments test whether you apply them exactly, not approximately.

**Question 2 (easy) — Logical deduction from a support policy**

Your team's policy states: "JavaScript-dependent enhancements must degrade gracefully: if the script fails, the underlying HTML feature must still let the user complete their task. Enhancements that cannot degrade gracefully require sign-off from the technical lead." A colleague shows you an autocomplete enhancement on a text input and says: "If the script fails, the plain text input still works." Which conclusion must be true?

- A) The enhancement requires sign-off from the technical lead.
- B) The enhancement does not require sign-off from the technical lead.
- C) The enhancement complies with the graceful degradation requirement.
- D) The autocomplete will work in all browsers.

**Correct answer: C**

**Explanation:** Map the facts to the policy. The policy has two parts: a requirement (degrade gracefully) and a conditional escalation (sign-off needed only where graceful degradation is impossible). The colleague's statement establishes that the underlying HTML input still lets users complete the task when the script fails — which is precisely the definition of graceful degradation given. So option C must be true. Option B is tempting: since the enhancement does degrade gracefully, surely no sign-off is needed? That is a reasonable *inference about intent*, but the policy as quoted only says sign-off is required when degradation is impossible — it does not state sign-off is *never* needed otherwise (the team might have other sign-off rules not quoted). In deduction questions, choose the conclusion the text guarantees, not the one it merely suggests. Option D goes far beyond the facts. This discipline — distinguishing what a policy guarantees from what it implies — is exactly how you will read standards and definition-of-done documents throughout your career.

**Question 3 (easy) — Error checking against an accessibility checklist**

You are checking a form field against four items from your team's accessibility checklist: (i) the input has a visible label linked with matching `for`/`id`; (ii) error messages are prefixed with "Error:" for screen reader users; (iii) the input's purpose is identified with an `autocomplete` attribute where one exists; (iv) hint text is programmatically associated with the input via `aria-describedby`. You review:

```
<label for="email">Email address</label>
<div id="email-hint" class="hint">We'll only use this to send your licence</div>
<input id="email" type="email" autocomplete="email">
<span class="error">Error: Enter an email address</span>
```

Which checklist item fails?

- A) Item (i)
- B) Item (ii)
- C) Item (iii)
- D) Item (iv)

**Correct answer: D**

**Explanation:** Check each item methodically. Item (i): `for="email"` matches `id="email"`, and the label is visible — pass. Item (ii): the error text begins "Error:" — pass. Item (iii): `autocomplete="email"` is present and correct for an email field — pass. Item (iv): there is a hint with `id="email-hint"`, but the input has no `aria-describedby="email-hint"` attribute, so screen readers will not announce the hint when the user focuses the field — fail. The hint is visible on screen, which is exactly why this bug slips through visual review: sighted users see the hint, so nothing *looks* wrong. Programmatic association is the kind of issue that only systematic checking (or screen reader testing) catches, and it is central to your skill of building interfaces that meet accessibility standards. Assessment technique and job technique are identical here: run the checklist item by item, and never let three passes lull you into skipping the fourth.

**Question 4 (easy) — Prioritising a morning after stand-up**

It is 9:45 am. Four items compete for your attention:

1. The build on the main branch is failing after yesterday's merges, blocking everyone's deployments.
2. A designer asked you (yesterday) to review a prototype "when you get a chance this week".
3. Your own feature ticket is due at sprint end, three days away.
4. A senior developer offered to pair with you on testing at 2 pm today.

What should you do first?

- A) Start your feature ticket — deadlines come first.
- B) Investigate the failing build, or join whoever is already fixing it.
- C) Review the designer's prototype so it isn't hanging over you.
- D) Prepare for the 2 pm pairing session.

**Correct answer: B**

**Explanation:** Rank by impact and urgency together. A failing build on the main branch blocks the *whole team's* deployments — every hour it stays red multiplies across colleagues, and fixing it (or supporting the fix) is the highest-impact, most urgent item by a wide margin. As a junior developer you may not fix it alone, but checking whether it was your merge, and offering to help whoever is on it, is exactly "recognising and dealing with issues". Option A serves a three-day deadline ahead of a right-now blocker. Option C has an explicit "this week" window. Option D matters, but preparation can happen after the build is green — hours before 2 pm. The pattern to internalise: team-blocking issues beat personal deadlines; explicit deadlines beat vague windows; and "someone else is probably handling it" is worth verifying rather than assuming. Prioritisation questions reward reasoning about who is affected and when, not just what is yours.

**Question 5 (moderate) — Pattern recognition in a build output**

Your build pipeline fingerprints assets: each compiled file is named `<name>.<8-character-hash>.<extension>`, for example `main.3f2a9c1b.css`. After a build, the output folder contains:

1. `main.3f2a9c1b.css`
2. `app.9d41e7aa.js`
3. `print.a1b2c3d.css`
4. `admin.77f0e2c4.js`

Which file breaks the naming pattern?

- A) File 1
- B) File 2
- C) File 3
- D) File 4

**Correct answer: C**

**Explanation:** The pattern requires exactly eight characters in the hash segment. Count each: file 1 has `3f2a9c1b` — eight. File 2 has `9d41e7aa` — eight. File 3 has `a1b2c3d` — seven. File 4 has `77f0e2c4` — eight. File 3 breaks the pattern. Counting characters feels tedious, and that is precisely the point: your eyes cannot judge seven versus eight characters at a glance, so the disciplined move is to count rather than eyeball. Why would this matter at work? Fingerprinted filenames drive cache-busting — browsers treat a changed hash as a new file and fetch it fresh. A malformed hash can indicate a misconfigured build step, and the symptom downstream is maddening: users see stale styles that "work on your machine". Recognising the malformed artefact in the build output is far cheaper than debugging the cache behaviour later — this is your systems integration skill (building static assets and testing the delivered result) in miniature.

**Question 6 (moderate) — Deduction about caching and delivery**

Your service's delivery rules are: (i) HTML pages are served with no caching, so browsers always fetch the latest page; (ii) CSS and JavaScript files are fingerprinted and cached for one year; (iii) a page only uses new styles when its HTML references a new fingerprinted filename. You deploy a change that edits only a CSS file. The build generates a new fingerprint, and the deployment updates both the CSS file and the HTML that references it. What will a returning user's browser do on their next visit?

- A) Use the old cached CSS, because CSS is cached for a year.
- B) Fetch the new HTML, see the new CSS filename, and fetch the new CSS.
- C) Fetch nothing, because everything is cached.
- D) Fetch the new CSS but keep the old HTML.

**Correct answer: B**

**Explanation:** Chain the rules. Rule (i): HTML is never cached, so the returning browser fetches the latest HTML — that eliminates options C and D immediately. The fresh HTML references the *new* fingerprinted CSS filename (the deployment updated it). Rule (ii) says CSS is cached by filename — but the browser has never seen this new filename, so there is nothing in cache for it, and the browser fetches the new CSS file. Result: the user gets the new styles on their next visit, which is option B. Option A describes the trap the fingerprinting system exists to avoid: the year-long cache applies to the *old* filename, which the new HTML simply no longer asks for. This mental model — uncached HTML as the always-fresh index, fingerprinted assets as immutable cached content — is one of the most useful pieces of systems-integration reasoning in frontend work, and assessment questions about rule chains reward exactly the step-by-step tracing you just did.

**Question 7 (moderate) — Error checking a pull request against the definition of done**

Your team's definition of done for a component: (i) unit tests cover the component's behaviour; (ii) the component is documented in the pattern library; (iii) accessibility checks (automated and keyboard) are recorded in the pull request; (iv) if the component introduces a new dependency, the dependency is approved and licence-checked. Your colleague's pull request for a new date-picker says: "Tests added (12 passing). Pattern library entry added. Automated accessibility check passing. Uses the `date-fns` library (already approved last quarter)." What is missing?

- A) Nothing — all four items are satisfied.
- B) The keyboard accessibility check.
- C) The dependency approval.
- D) The pattern library entry.

**Correct answer: B**

**Explanation:** Audit each item against the pull request's claims. Item (i): twelve passing tests — satisfied. Item (ii): pattern library entry added — satisfied. Item (iii): this item requires *two* checks, automated *and* keyboard, both recorded; the PR records only the automated check, so the keyboard check is missing — and for a date-picker, of all components, keyboard operation is where accessibility problems concentrate. Item (iv): `date-fns` was approved last quarter — satisfied. So option B is correct. The trap is the compound requirement: item (iii) bundles two obligations into one sentence, and a quick reader who sees "accessibility check ✓" mentally ticks the whole item. Compound requirements are everywhere in definitions of done, service standards, and acceptance criteria; the professional habit is to split every "and" into separate checkboxes. That habit — plus refusing to stop at the first plausible "all done" — is what this question, and real code review, both measure.

**Question 8 (moderate) — Ordering a release with dependencies**

You must complete five tasks to release a component: write the code (C), write the tests (T), get code review (R), update the pattern library documentation (D), and merge (M). Team rules: tests must be written before review is requested, because reviewers check them; review must be approved before merge; documentation must be finished before merge, but may be written any time after the code exists; code obviously precedes everything that examines it. Which sequence is valid?

- A) C, T, R, D, M
- B) C, R, T, D, M
- C) T, C, R, D, M
- D) C, T, D, M, R

**Correct answer: A**

**Explanation:** Extract the ordering constraints: C before T, R, D (they all examine the code — and note tests examine behaviour of written code in this team's flow); T before R; R before M; D before M (but D is flexible after C). Now test each option. Option A: C, T, R, D, M — C first ✓, T before R ✓, R before M ✓, D before M ✓. Valid. Option B places review before tests, violating "tests before review". Option C places tests before code exists. Option D merges before review is approved — the most dangerous violation of all, and one that real teams guard against with branch protection. Only option A satisfies every rule. Notice the efficient technique: you did not generate all possible orderings; you turned prose rules into short precedence facts and used each to eliminate options. This is the same reasoning you apply when sequencing real delivery work — and when you explain to a stakeholder why "just merge it now and review later" is not how the team works.

**Question 9 (moderate) — Applied problem solving: a bug that only some users see**

Users report that a "Save and continue" button does nothing — but only some users, and your team cannot reproduce it. You gather facts: the button's click behaviour is attached by JavaScript; analytics show the failing reports correlate with older browser versions; your bundle recently started using a newer JavaScript syntax feature; the build's compatibility (transpilation) step was recently changed. What is the most reasonable hypothesis to test first?

- A) Users are clicking the wrong button.
- B) The newer syntax is not being transpiled for older browsers, so the script fails there and the button's behaviour never attaches.
- C) The server is down intermittently.
- D) The analytics data is wrong.

**Correct answer: B**

**Explanation:** Good debugging aligns the hypothesis with *all* the evidence. Option B explains every fact at once: the failure is browser-version-correlated (older browsers reject syntax they don't understand), it affects only some users (those on older browsers), it makes the button inert rather than broken-looking (a script error stops the click handler ever attaching), and it coincides with two recent changes (new syntax, changed transpilation step). Options A, C, and D each explain at most one fact and contradict others — a server outage would not correlate with browser version; "users clicking wrong" would not correlate with your build changes. Testing B first is also cheap: open the site in an affected browser version and watch the console. There is a role lesson underneath: this is precisely why progressive enhancement matters — had the button been a real HTML form submission enhanced by JavaScript, those users would still have saved their work. Diagnosing with evidence, then reasoning back to the standard that would have prevented the bug, is the full arc of your problem-solving skill.

**Question 10 (challenging) — Multi-rule deduction about browser support tiers**

Your team's browser support policy defines two tiers: "compliant" browsers get the full experience; "functional" browsers must be able to complete every task, but may get simpler styling and no enhancements. Rules: (i) any browser above 2% usage is compliant; (ii) any browser between 0.5% and 2% is functional; (iii) below 0.5%, testing is not required, but progressive enhancement should mean tasks still work; (iv) assistive technologies are tested regardless of usage share. Your analytics: Browser P 45%, Browser Q 30%, Browser R 1.8%, Browser S 0.4%. A stakeholder asks: "So we don't need to care about R and S at all, right?" Which reply is accurate?

- A) "Correct — R and S are below our support threshold."
- B) "R must be able to complete every task with possibly simpler styling; S isn't tested, but our progressive enhancement approach means tasks should still work there too."
- C) "R gets the full experience; S must complete every task."
- D) "Both R and S get the full experience because we test assistive technologies regardless of usage."

**Correct answer: B**

**Explanation:** Apply the tier boundaries precisely. Browser R at 1.8% falls between 0.5% and 2%, so it is *functional*: every task must be completable, simpler styling allowed — not "full experience" (eliminating C) and certainly not "don't care" (eliminating A). Browser S at 0.4% falls below 0.5%: no testing required, but rule (iii) explicitly expects progressive enhancement to keep tasks working — so "don't care at all" misrepresents the policy for S too. Option D misapplies rule (iv), which concerns assistive technologies, not low-usage browsers. Option B states both cases accurately. Two skills are being tested at once here: threshold reading (1.8% and 0.4% sit close to boundaries on purpose) and faithful summarising for a stakeholder — your communicating information skill includes correcting a simplification without jargon or condescension. Note also the deeper point your reply carries: "unsupported" never means "broken" in a progressively enhanced service, and being able to explain that distinction clearly is a mark of a developer who understands why the standards exist.

**Question 11 (challenging) — Scheduling work with fixed constraints**

Next week you must fit four half-day activities around fixed commitments: implementing a component (needs two consecutive half-days), a design review of that component (must come after implementation is finished; the interaction designer is only available Wednesday afternoon or Friday morning), writing the pattern library documentation (one half-day, must come after the design review), and your team's community-of-practice session (fixed: Thursday afternoon). Sprint demo is Friday afternoon, and the documentation must be done before the demo. Mornings and afternoons Monday–Friday are otherwise free. What is the latest you can finish implementation?

- A) Tuesday afternoon
- B) Wednesday morning
- C) Thursday morning
- D) Friday morning

**Correct answer: B**

**Explanation:** Work backwards from the hardest deadline. Documentation must precede Friday afternoon's demo and must follow the design review. The design review has only two possible slots: Wednesday afternoon or Friday morning. Test Friday morning: documentation would then need a slot after Friday morning and before Friday afternoon's demo — none exists. So the review must be Wednesday afternoon. Implementation (two consecutive half-days) must finish before Wednesday afternoon; the latest consecutive pair ending by then is Tuesday afternoon + Wednesday morning, so implementation finishes Wednesday morning at the latest — option B. Documentation then fits anywhere from Thursday morning to Friday morning (Thursday afternoon is blocked by the community session). The technique: when a chain of dependencies meets fixed availability, anchor the least flexible item first (here, the review's two slots), eliminate the impossible slot by looking downstream, and let the survivors constrain everything upstream. This is assessment logic, but it is also exactly how you will plan real sprints around other people's calendars — and why experienced developers book scarce collaborators before writing a line of code.

**Question 12 (challenging) — Applied problem solving with a performance budget trade-off**

Your page must stay under a 300 KB JavaScript budget and load its main content within 2.5 seconds on the team's test connection. Current state: 280 KB of JavaScript, loading in 2.3 seconds. A new feature needs a mapping library: the full library is 90 KB; a lightweight alternative is 30 KB but lacks one nice-to-have gesture; writing your own minimal code is estimated at 4 days. Removing a now-unused analytics script would save 25 KB. Each 10 KB of JavaScript adds roughly 0.05 seconds on the test connection. The feature is due this sprint. Which option best meets all the constraints?

- A) Add the full library and remove the analytics script.
- B) Add the lightweight library and remove the analytics script.
- C) Write your own minimal mapping code.
- D) Add the full library and accept being slightly over budget temporarily.

**Correct answer: B**

**Explanation:** Test each option against both budgets and the deadline, step by step. Option A: 280 + 90 − 25 = 345 KB — over the 300 KB budget; fails immediately. Option B: 280 + 30 − 25 = 285 KB — within budget. Load time: the net JavaScript change is +5 KB, adding roughly 0.05 × 0.5 = 0.025 seconds, so about 2.33 seconds — within 2.5 seconds. Deliverable this sprint, at the cost of one nice-to-have gesture: passes everything. Option C might produce the smallest code, but 4 days of estimated (and, for a junior developer, uncertain) work jeopardises the sprint deadline and creates unmaintained bespoke code where a maintained library exists — a reuse anti-pattern. Option D treats a hard budget as soft; performance budgets exist precisely to resist "temporarily" (temporary overruns have a way of becoming permanent, and users on slow connections pay the cost). Option B is the disciplined trade-off: it sacrifices the least important thing (a nice-to-have gesture) to protect users (performance), the team (deadline, maintainability), and the standard (the budget). Assessments and real engineering agree: the best option is rarely perfect — it is the one that satisfies every hard constraint and gives up only what is genuinely optional.

### Preparation tips

- **Practise in short, regular sessions.** Twenty minutes of focused question practice several times a week builds more skill than a single long cram. You are training habits — checking, counting, tracing — and habits grow through repetition.
- **Mine your own code reviews.** Every review comment you receive or read is a cognitive question in disguise: what pattern, rule, or check did the reviewer apply? Collect the recurring ones; they will reappear in tests and in your own reviewing.
- **Turn prose rules into lists.** When a question (or a policy) gives you several rules, number them and check each explicitly. The questions above repeatedly punished stopping one rule early — so never stop early.
- **Trace chains out loud.** For deduction questions about pipelines, caching, or fallbacks, narrate the chain: "HTML fetched fresh → new filename → cache miss → new CSS". Narration exposes the step you skipped.
- **Count, don't eyeball.** Hashes, thresholds, and near-identical names defeat visual skimming. When precision matters, count characters and compare digits deliberately.
- **Use the official practice questions.** Almost every assessment platform offers ungraded warm-up questions. Always take them — interface familiarity is free marks.
- **Simulate test conditions once or twice.** Do a timed set in a quiet space before the real thing. Time pressure changes how you read; practising under it removes the surprise.

### Common pitfalls to avoid

- **Reading what you expect instead of what is written.** Your fluency with code is a double-edged sword: experts skim. Near-matches (`app-task-list-completed` vs `--completed`, seven-character hashes) are designed to punish skimming. Slow down where precision pays.
- **Concluding more than the rules guarantee.** "The policy suggests no sign-off is needed" is not "the policy states it". Deduction questions want the guaranteed conclusion, and options that overreach are always on offer.
- **Ticking compound requirements half-done.** "Automated and keyboard checks recorded" is two obligations. Split every "and" before you tick anything.
- **Letting seniority of a document replace reading it.** Definitions of done, support policies, and checklists mean exactly what they say — including boundary values like "between 0.5% and 2%". Check which side of each threshold the numbers fall.
- **Choosing the heroic option in problem-solving questions.** Writing your own library, absorbing an over-budget "temporarily", or fixing everything alone often looks impressive and fails a hard constraint. Check every option against every constraint first.
- **Burning time on one hard question.** Eliminate what you can disprove, choose the best survivor, flag it if the platform allows, and move on. Consistent accuracy across the whole test beats perfection on a third of it.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A numeric reasoning assessment measures how accurately you extract, manipulate, and interpret numbers in workplace contexts. The mathematics itself stays modest — percentages, ratios, averages, rates, and percentage change — but the questions wrap it in realistic data: tables, charts, and short scenarios. What is really being tested is a chain of small skills: picking the right numbers out of the data, choosing the right operation, executing it accurately, and interpreting the result sensibly.

The typical format is an online, timed test of 20 to 30 minutes with 15 to 25 multiple-choice questions. A calculator and rough paper are normally allowed — use both. Questions often share a data set: one table feeding three or four questions. Scoring is objective and usually norm-referenced, and adaptive difficulty is common. The most reliable score-improver at this level is simply writing your working down: it converts avoidable slips into caught slips.

Why do employers use numeric reasoning tests for junior frontend developers? Because your role is surrounded by numbers that drive decisions. Performance budgets are set in kilobytes and milliseconds, and you are asked to keep pages inside them. Analytics dashboards report device splits and browser shares, which determine what you must test. Test suites report pass rates; accessibility audits report issue counts by severity; sprint boards report completed points and velocity. A junior developer who reads these numbers accurately — and who notices when a claimed percentage doesn't survive arithmetic — contributes to team decisions rather than just receiving them. Your role summary asks you to identify user issues and needs and to explain the strategic context of your work: both routinely arrive as data.

### How this assessment maps to your role

- **Percentages and percentage change** map to **Web performance optimisation**: page-weight budgets, compression savings, and load-time improvements are all expressed as percentages, and helping improve web performance under supervision means calculating them correctly.
- **Reading tables and charts** maps to **User focus (frontend developer)** and **Communicating information**: identifying user issues and needs frequently starts with analytics and research data, and shaping communications relevant to the audience includes reporting numbers faithfully.
- **Averages and rates** map to **Programming and build (frontend developer)** and **Systems integration (frontend developer)**: build durations, test pass rates, and deployment frequencies are the operational numbers of delivery, and you will quote them in stand-ups and retrospectives.
- **Ratios and thresholds** map to **Accessibility**: contrast ratios (such as 4.5:1) and audit severity counts are numeric artefacts of accessibility work, where threshold reading decides pass or fail.
- **Weighted combinations** map to **Strategic thinking** and **Community collaboration**: combining results from different-sized groups — devices, teams, sprints — without distortion is how you support planning honestly, and how you avoid being misled by a simple average.

### Practice questions

**Question 1 (easy) — Percentage of budget used**

Your page's JavaScript budget is 300 KB. The current bundle is 240 KB. What percentage of the budget is used?

- A) 60%
- B) 75%
- C) 80%
- D) 85%

**Correct answer: C**

**Explanation:** Percentage used = part ÷ whole × 100. Step 1: 240 ÷ 300 = 0.8. Step 2: 0.8 × 100 = 80%. So the bundle uses 80% of the budget, leaving 60 KB of headroom. Sense-check before you commit: 240 is clearly "most but not nearly all" of 300, so 60% is too small and 85% slightly too large — the check alone eliminates two options. In performance conversations this framing matters: "we're at 80% of budget" communicates urgency far better than "we have 60 KB left", because the percentage scales with the team's mental model of the limit. Getting fluent with part-whole percentages pays off every time you read a bundle-size report.

**Question 2 (easy) — Test pass rate after a change**

Before your change, the suite had 320 tests, all passing. Your change adds 30 new tests, and after it runs, 336 tests pass in total. What is the overall pass rate, to the nearest percent?

- A) 93%
- B) 96%
- C) 98%
- D) 100%

**Correct answer: B**

**Explanation:** Step 1: find the new total number of tests: 320 + 30 = 350. Step 2: pass rate = passes ÷ total = 336 ÷ 350 = 0.96. Step 3: 0.96 × 100 = 96%. So 14 tests are failing (350 − 336), and the pass rate is 96% — option B. The common slip is dividing 336 by the old total of 320 (which gives a nonsensical 105%) or forgetting to add the new tests at all. Always update the denominator before dividing. At work, the fluency matters for a subtler reason: a suite that was fully green and is now at 96% after your change means *your change* likely broke or introduced those failures — the numbers point directly at the next debugging step, and reading them correctly gets you there before anyone has to tell you.

**Question 3 (easy) — Device split from a table**

Last month's analytics for your service:

| Device | Sessions |
|---|---|
| Mobile | 90,000 |
| Desktop | 45,000 |
| Tablet | 15,000 |

What percentage of sessions were on mobile?

- A) 50%
- B) 60%
- C) 66%
- D) 75%

**Correct answer: B**

**Explanation:** Step 1: total sessions = 90,000 + 45,000 + 15,000 = 150,000. Step 2: mobile share = 90,000 ÷ 150,000 = 0.6 = 60%. Option B. A quick ratio view confirms it: the split is 90:45:15, which simplifies (dividing by 15) to 6:3:1 — six parts of ten are mobile. The professional takeaway sits behind the arithmetic: with 60% of sessions on mobile, mobile is not an edge case to check at the end — it is the majority experience, and testing mobile-first reflects where users actually are. When you advocate for the team externally or explain the strategic context of your work, numbers like "three in five sessions are mobile" are the kind of clear, accurate evidence that wins the argument.

**Question 4 (easy) — Average page load time**

You measure a page's load time five times on the test connection: 2.1 s, 2.4 s, 2.0 s, 2.6 s, and 2.4 s. What is the mean load time?

- A) 2.2 s
- B) 2.3 s
- C) 2.4 s
- D) 2.5 s

**Correct answer: B**

**Explanation:** The mean is the sum divided by the count. Step 1: 2.1 + 2.4 + 2.0 + 2.6 + 2.4 = 11.5 seconds. Step 2: 11.5 ÷ 5 = 2.3 seconds — option B. A practical habit from performance work: alongside the mean, glance at the spread. These runs range from 2.0 to 2.6 seconds — real measurements always vary, which is exactly why teams measure several runs rather than trusting one. If a single run had read 9.8 seconds, you would investigate before averaging it in (perhaps another process interfered), because one outlier can drag a mean far from typical experience. In tests, compute the mean exactly as asked; at work, remember that the mean is a summary, and summaries deserve a second look before they drive decisions.

**Question 5 (moderate) — Percentage change in bundle size**

After removing an unused library, your JavaScript bundle shrinks from 250 KB to 210 KB. What is the percentage reduction, and if the team's goal was "at least a 15% reduction", was it met?

- A) 16% reduction; goal met
- B) 16% reduction; goal not met
- C) 19% reduction; goal met
- D) 40% reduction; goal met

**Correct answer: A**

**Explanation:** Percentage change = (difference ÷ original) × 100. Step 1: difference = 250 − 210 = 40 KB. Step 2: 40 ÷ 250 = 0.16. Step 3: 0.16 × 100 = 16%. The goal was "at least 15%", and 16% ≥ 15%, so the goal is met — option A. Two traps guard this question. First, the denominator: dividing by the *new* size (40 ÷ 210 ≈ 19%) produces option C — percentage change always uses the original value. Second, the threshold: having computed 16%, you must still compare it correctly against "at least 15%" — a rushed reader who misremembers the goal as 20% picks option B. Compute, then compare, as two deliberate steps. This double discipline — right denominator, careful threshold — covers a remarkable share of all numeric-test errors, and it is exactly how you will verify claims like "we cut the bundle by a fifth" before repeating them in a sprint review.

**Question 6 (moderate) — Accessibility audit across releases**

An accessibility audit is run before each release. The issue counts:

| Release | Critical | Serious | Minor |
|---|---|---|---|
| 1.0 | 6 | 10 | 24 |
| 1.1 | 3 | 8 | 30 |
| 1.2 | 1 | 4 | 33 |

A colleague says: "Total issues barely changed, so we've made no real progress." Is that a fair summary?

- A) Yes — totals went 40, 41, 38, which is roughly flat.
- B) No — critical issues fell from 6 to 1 and serious from 10 to 4; the mix improved sharply even though totals are flat.
- C) No — total issues actually rose.
- D) Yes — minor issues increased, cancelling out other progress.

**Correct answer: B**

**Explanation:** First verify the totals: release 1.0: 6 + 10 + 24 = 40; release 1.1: 3 + 8 + 30 = 41; release 1.2: 1 + 4 + 33 = 38. Totals are indeed roughly flat, so option C is factually wrong. But "no real progress" does not follow: severity matters. Critical issues — the ones that can block users outright — fell by 83% (6 to 1), and serious issues by 60% (10 to 4). Minor issues rose from 24 to 33, which deserves attention but does not "cancel" the severe-issue progress, because severities are not interchangeable: one critical issue harms users more than several minor ones. Option B reads the table at the right resolution. The lesson generalises to every dashboard you will ever present: totals across categories of different importance can hide the story, and your communicating information skill includes choosing the breakdown that tells it honestly — in both directions, celebrating real progress and flagging the creeping minor-issue count.

**Question 7 (moderate) — Sprint velocity and forecasting**

Your team completed 21, 24, 18, and 25 story points in its last four sprints. The remaining backlog for the current milestone is 66 points. Using the four-sprint average velocity, how many more full sprints will the milestone take?

- A) 2 sprints
- B) 3 sprints
- C) 4 sprints
- D) 5 sprints

**Correct answer: B**

**Explanation:** Step 1: average velocity = (21 + 24 + 18 + 25) ÷ 4 = 88 ÷ 4 = 22 points per sprint. Step 2: sprints needed = 66 ÷ 22 = 3.0 — exactly three sprints, option B. Had the division produced a fraction (say 3.2), the answer to "how many full sprints will it take" would round *up* to 4, because work remaining after three sprints still needs a fourth — a ceiling, not a nearest-integer rounding. Test writers love that distinction, so read forecast questions for whether partial sprints count. The real-world caveat belongs alongside the arithmetic: velocity is an average of variable numbers (your sprints ranged 18–25), so a forecast of "about three sprints" deserves the word "about" when you repeat it to a stakeholder. Supporting strategic planning in an administrative capacity — one of your named skills — means doing exactly this calculation and presenting it with exactly that honesty.

**Question 8 (moderate) — Image savings with mixed reductions**

A page's images total 800 KB: photographs 600 KB and icons 200 KB. Converting the photographs to a modern format reduces their size by 45%; optimising the icons reduces theirs by 25%. What is the total image weight after both optimisations?

- A) 380 KB
- B) 480 KB
- C) 520 KB
- D) 560 KB

**Correct answer: B**

**Explanation:** Handle each category separately — the reductions differ, so a single blended percentage will mislead. Photographs: a 45% reduction keeps 55%, so 600 × 0.55 = 330 KB. Icons: a 25% reduction keeps 75%, so 200 × 0.75 = 150 KB. Total: 330 + 150 = 480 KB — option B. Working with the "kept" fraction (0.55, 0.75) is faster and safer than computing each saving and subtracting. The main trap is applying one category's percentage to the whole 800 KB: 800 × 0.55 = 440 or 800 × 0.75 = 600 bracket the truth but match no option here; a sloppier test might include them. There is also a strategic reading: the photographs contributed 270 KB of savings versus the icons' 50 KB — when you help identify and resolve performance issues, the biggest files with the biggest reduction rates are where the effort pays, and this little calculation is how you prove it before spending the time.

**Question 9 (moderate) — Error rates from a form analytics table**

Analytics for a three-page application form last week:

| Page | Users entering | Users completing |
|---|---|---|
| Page 1: Details | 4,000 | 3,600 |
| Page 2: Evidence | 3,600 | 2,700 |
| Page 3: Review | 2,700 | 2,565 |

Which page has the highest drop-off *rate*, and what is that rate?

- A) Page 1; 10%
- B) Page 2; 25%
- C) Page 3; 5%
- D) Page 2; 900 users

**Correct answer: B**

**Explanation:** Compute each page's drop-off rate as (entering − completing) ÷ entering. Page 1: (4,000 − 3,600) ÷ 4,000 = 400 ÷ 4,000 = 10%. Page 2: (3,600 − 2,700) ÷ 3,600 = 900 ÷ 3,600 = 25%. Page 3: (2,700 − 2,565) ÷ 2,700 = 135 ÷ 2,700 = 5%. The highest rate is Page 2 at 25% — option B. Option D is a category error the question plants deliberately: 900 users is the largest *count*, but the question asks for a *rate*, and a rate is a percentage of those at risk. The distinction drives real decisions: a quarter of everyone who reaches the Evidence page gives up there — that is where user research and design effort should concentrate, and as the developer who identifies user issues and needs from data, you are exactly the person to bring this table to the team and say so. Rates find the broken step; raw counts often just find the busiest one.

**Question 10 (challenging) — Weighted completion rate across devices**

A usability study of your new form had 60 participants: 40 on mobile, 15 on desktop, and 5 using a screen reader (on either device). Completion rates: mobile 85%, desktop 80%, screen reader users 40%. What was the overall completion rate?

- A) 68.3%
- B) 78.3%
- C) 80.0%
- D) 81.7%

**Correct answer: C**

**Explanation:** Convert each group's rate into people, then recombine — never average the percentages directly. Mobile: 85% of 40 = 34 completions. Desktop: 80% of 15 = 12 completions. Screen reader users: 40% of 5 = 2 completions. Total completions: 34 + 12 + 2 = 48 out of 60 participants. Overall rate: 48 ÷ 60 = 0.8 = 80% — option C. The unweighted average of the three rates, (85 + 80 + 40) ÷ 3 ≈ 68.3%, is option A — wrong because the groups differ enormously in size (40 versus 5). Notice what the correct headline *hides*, though: an overall 80% looks healthy, yet only 2 of 5 screen reader users completed the form. Both facts are true; only reporting both is honest. This is the numeric heart of inclusive practice: overall rates weighted by group size are arithmetically correct and can still bury the users who struggled most. When you champion accessibility fixes, the sentence "overall completion is 80%, but screen reader completion is 40%" is the one that moves the backlog.

**Question 11 (challenging) — Load-time trend and a performance target**

Your page's median load time on the test connection has been tracked monthly: March 3.8 s, April 3.5 s, May 3.2 s, June 2.9 s. The team's target is at most 2.0 s. If the current fixed monthly improvement continues, in which month does the page first meet the target?

- A) August
- B) September
- C) October
- D) November

**Correct answer: B**

**Explanation:** First establish the trend: 3.8 → 3.5 → 3.2 → 2.9 falls by 0.3 seconds each month — a fixed decrement. Project forward, writing each value: July 2.6, August 2.3, September 2.0. The target is "at most 2.0 s", and September's 2.0 meets it exactly (2.0 ≤ 2.0). So September — option B. Two guard-rails produced that answer. First, listing the months one by one avoids the off-by-one slip in "need 0.9 more seconds, that's three months, June + 3 = September — or is it August?" (listing settles it). Second, the boundary: "at most 2.0" *includes* 2.0; a reader who treats the target as "below 2.0" continues to October and picks C. Boundary language decides the answer, exactly as it did in the browser-tier question. And carry the real-world caveat with you: fixed monthly improvements are a modelling assumption — genuine optimisation tends to get harder as the easy wins are spent, which is worth saying aloud when a stakeholder extrapolates your trend line for you.

**Question 12 (challenging) — Reconciling a stakeholder's claim with the data**

A stakeholder's slide claims: "Support tickets about the online form fell 60% after the redesign." The data: in the three months before the redesign, tickets were 180, 150, and 170 per month (form-related), while total service tickets averaged 1,000 per month. In the three months after: 90, 80, and 85 form-related tickets, with total service tickets averaging 500 per month. Is the 60% claim accurate for form-related tickets?

- A) Yes — form tickets fell by exactly 60%.
- B) No — form tickets fell by about 49%, though their share of all tickets actually rose.
- C) No — form tickets fell by about 30%.
- D) Yes — form tickets halved and their share fell too.

**Correct answer: B**

**Explanation:** Work the numbers before judging the claim. Before: 180 + 150 + 170 = 500 form tickets over three months (average 166.7/month). After: 90 + 80 + 85 = 255 (average 85/month). Reduction: (500 − 255) ÷ 500 = 245 ÷ 500 = 0.49 — about a 49% fall, not 60%. So the headline overstates. Now the subtler check: form tickets as a *share* of all tickets. Before: 166.7 ÷ 1,000 ≈ 17%. After: 85 ÷ 500 = 17% — the share held steady (call it "did not fall"; with rounding, 85/500 = 17.0% versus 16.7% before, a slight rise). The overall ticket volume halved for reasons that may have nothing to do with the form, and the form's fall roughly tracked the general fall. Option B is the only answer whose arithmetic survives checking. The professional moment this rehearses is delicate and real: when you spot that a stakeholder's number flatters, your communicating information skill is to correct it accurately and kindly — "the true fall is about 49%, and here's the working" — before the slide reaches an audience that will check. Teams that verify their own good news keep their credibility for when they need it.

### Preparation tips

- **Drill the four core operations.** Part-whole percentages, percentage change (difference over *original*), weighted combinations (counts before rates), and simple averages cover the large majority of questions. Make each automatic, then practise them mixed.
- **Write every step down.** The questions above repeatedly hinged on one intermediate number (a new total, a "kept" fraction, a per-group count). Paper holds those numbers reliably; working memory under time pressure does not.
- **Interrogate the denominator.** Before dividing, say what the whole is: original size? new total? those at risk? The wrong denominator is the most common error in this entire test type, and it is always among the answer options.
- **Watch boundary words.** "At least", "at most", "between", "more than" — each decides whether a boundary value passes. Circle them in the question before you compute.
- **Use your team's real data as practice.** Bundle-size reports, analytics dashboards, audit summaries, and velocity charts are free practice sets. Recompute one claimed percentage a day; you will be startled how often reality is a useful teacher.
- **Sense-check magnitude before selecting.** Is the answer roughly the right size? A 40 KB saving on 250 KB must be "a bit under a fifth" — that instinct catches calculator slips in two seconds.
- **Manage the clock deliberately.** Shared-data questions reward reading the table properly once, then answering several questions quickly. Invest the reading time up front; it repays itself.

### Common pitfalls to avoid

- **Dividing by the new value in change questions.** Percentage change compares against the original. The wrong-denominator answer (19% instead of 16%) is planted in the options every time.
- **Averaging percentages across different-sized groups.** Five screen reader users and forty mobile users do not contribute equally to an overall rate. Convert to counts, combine, then divide.
- **Confusing counts with rates.** The biggest drop-off *number* and the highest drop-off *rate* can be different pages. Check which one the question — or the stakeholder — actually asked about.
- **Forgetting to update the total.** Adding 30 tests changes the denominator to 350. Compute new wholes before computing new percentages.
- **Misreading severity-mixed tables.** Totals across categories of unequal importance (critical versus minor issues) can be flat while the picture transforms. Read tables at the resolution the question requires.
- **Treating boundary values carelessly.** 2.0 s meets "at most 2.0 s"; 5% usage meets "at least 5%". Boundary cases appear in these tests by design, never by accident.
- **Accepting round-number claims without checking.** "Fell 60%" took thirty seconds to disprove. In tests, verify against the data given; at work, verify before you repeat a number in front of an audience.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A verbal reasoning assessment measures how precisely you understand written information and how soundly you reason from it. Each question presents a short passage — in this guide, always drawn from your working world: coding standards, accessibility guidance, service manual extracts, tickets, emails from designers and analysts, and sprint or research notes. You then judge statements about the passage. The dominant format is **True** (the passage states or clearly implies it), **False** (the passage contradicts it), or **Cannot say** (the passage provides insufficient information either way). Some questions instead ask you to pick the best summary, the soundest inference, or the clearest piece of writing.

The typical format is an online, timed test of 15 to 25 minutes with 20 to 30 statements across several passages. The governing rule never changes: judge each statement using only the passage. Your professional knowledge — even when correct — must be set aside, because the test measures reading, not background. If the passage does not say it and does not clearly imply it, the answer is "cannot say", however plausible the statement sounds.

Why do employers test this for junior frontend developers? Because your work arrives and leaves as text. You receive user stories, acceptance criteria, standards, and review comments; you produce commit messages, pull request descriptions, documentation, and messages to designers and stakeholders. Your role explicitly includes interpreting information from stakeholders, shaping communications relevant to the audience, and advocating for the team externally — all of which fail if the reading underneath them is imprecise. A misread acceptance criterion becomes a rejected pull request; a misread policy becomes a compliance gap; an overclaimed summary becomes a credibility dent. Precise reading is a delivery skill, and this assessment measures it directly.

### How this assessment maps to your role

- **Comprehension of requirements** maps to **Programming and build (frontend developer)**: collaborating with others to understand and review software requirements starts with extracting exactly what a ticket or specification commits you to — no more, no less.
- **True/false/cannot-say discipline** maps to **User focus (frontend developer)** and **Strategic thinking**: user stories and strategy documents describe needs and context; distinguishing what they establish from what they leave open tells you which questions to ask before you build.
- **Modal and quantifier reading** maps to **Modern development standards** and **Accessibility**: standards use "must", "should", and "may" with legal precision, and applying modern development standards under guidance requires reading them at that precision.
- **Inference** maps to **Communicating information**: managing differing perspectives and advocating for the team depend on drawing sound conclusions from what stakeholders actually wrote — and resisting the conclusions they didn't support.
- **Clear-writing judgement** maps to **Community collaboration** and **Prototyping**: pull request descriptions, pattern library entries, and feedback all serve future readers; recognising clear, specific, actionable writing is the first step to producing it.

### Practice questions

For each true/false/cannot-say question, judge the statement using only the passage.

**Question 1 (easy) — A coding standard**

Passage: "All interactive components must be operable by keyboard alone. Components from the design system have keyboard support built in and may be used without additional keyboard testing. Custom interactive components must pass keyboard testing before release, and the test results must be linked in the pull request."

Statement: "A custom interactive component may be released before keyboard testing, provided the results are linked afterwards."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** The passage says custom interactive components "must pass keyboard testing *before release*". The statement proposes releasing first and testing after — a direct reversal of the stated order, so it is False. Notice how the statement borrows the passage's own vocabulary ("results", "linked") to sound compatible while inverting the sequence; timing inversions are among the most common manufactured contradictions in this test type. Note also the two-track structure of the passage: design system components are exempt from *additional* testing, custom components are not. Keeping parallel tracks separate — which rule applies to which category — is precisely how you read your team's real standards, where mixing up the tracks means either wasted testing or an inaccessible release.

**Question 2 (easy) — An email from a delivery manager**

Passage (email): "Hi both — the minister's office has moved the announcement to Tuesday, so the content changes must be live by Monday 5 pm. Dev work looks on track. Design sign-off is still outstanding: Amira is back from leave on Friday and has agreed to review first thing. If anything slips, tell me by Friday lunchtime, not Monday morning. Thanks, Sam."

Statement: "Sam wants to be told about any slippage no later than Friday lunchtime."

- A) True
- B) False
- C) Cannot say

**Correct answer: A**

**Explanation:** The email states it directly: "If anything slips, tell me by Friday lunchtime, not Monday morning." The statement is a faithful restatement, so it is True. Easy questions like this check that you don't overthink: "cannot say" is not a safe default, and hedging when the text is explicit costs marks just as surely as guessing when it is silent. There is also a workplace reading worth absorbing: Sam's email contains one hard deadline (Monday 5 pm), one dependency (Amira's Friday review), and one communication rule (escalate by Friday lunchtime). Emails from delivery managers routinely pack several commitments into few lines, and extracting all of them — not just the loudest — is the comprehension skill your role's "interpret information" bullet describes.

**Question 3 (easy) — A service manual extract**

Passage: "Services must work on the devices and browsers that users actually use, informed by analytics. Teams should test on a representative sample of devices. Emulators and simulators may be used for development, but final assurance testing should use real devices."

Statement: "Teams are forbidden from using emulators at any stage."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** The passage explicitly permits emulators: they "may be used for development". The restriction applies only to final assurance testing, and even there the language is "should use real devices" — a strong recommendation, not an absolute prohibition on everything else. The statement's "forbidden… at any stage" contradicts the explicit permission, so it is False. The skill on display is scope-reading: rules attach to stages ("for development", "final assurance"), and a statement that strips the stage qualifier and universalises the rule ("at any stage") manufactures a contradiction. Standards and policies in government digital work are full of stage-scoped and role-scoped rules; reading the scope as carefully as the rule is what keeps your team compliant without over-restricting itself.

**Question 4 (easy) — A user research summary**

Passage: "Round 3 testing (six participants) focused on the eligibility checker. Four participants completed all tasks without assistance. Two participants, both using screen magnification, missed the inline error messages and could not complete the final task. Participants generally described the language as clear. We recommend moving error messages above the input fields and re-testing in round 4."

Statement: "Most participants completed all tasks without assistance."

- A) True
- B) False
- C) Cannot say

**Correct answer: A**

**Explanation:** Four of six participants completed all tasks without assistance; four out of six is a clear majority, so "most" is accurate and the statement is True. Be careful not to let the passage's serious finding — two magnification users blocked by error placement — pull you toward False out of sympathy; the statement makes a narrow numerical claim, and the numbers support it. Both facts coexist: most participants succeeded, *and* the design has an accessibility problem worth fixing. Reading research summaries at work demands exactly this both-hands precision, because a team that hears only "most succeeded" ships the problem, and a team that hears only "users failed" loses calibration. The statement asked about one fact; answer that fact, and carry the whole picture into your day job.

**Question 5 (moderate) — Progressive enhancement guidance**

Passage: "Build the core user journey with HTML so it works regardless of scripting. Enhance with CSS and JavaScript where they improve the experience. An enhancement must never become a dependency: if removing the script would prevent task completion, the feature is not an enhancement but a requirement, and requires a documented exception. Exceptions are granted only where no HTML-based alternative exists."

Statement: "A feature whose script removal prevents task completion always requires a documented exception."

- A) True
- B) False
- C) Cannot say

**Correct answer: A**

**Explanation:** Trace the passage's definitions. If removing the script prevents task completion, the passage classifies the feature as "not an enhancement but a requirement, and requires a documented exception". The statement restates exactly that consequence, including its universality — the passage's rule contains no carve-outs at the classification step (the "only where" clause governs when exceptions are *granted*, not whether one is *required*). So the statement is True. The subtlety worth savouring: two different rules share one sentence-neighbourhood — "requires an exception" (always, for script-dependent features) and "exceptions are granted only where no HTML alternative exists" (a further hurdle). A hasty reader merges them and answers "cannot say" because they think granting conditions make the requirement conditional. Separating adjacent rules — what triggers a process versus what the process then decides — is a reading skill you will use on every governance and standards document in your career.

**Question 6 (moderate) — Cannot-say discipline with an incident note**

Passage (incident note): "14:20 — users report the document upload failing with a spinner that never resolves. 14:35 — deploys to the upload service paused. 14:50 — engineers identify a timeout between the upload service and the virus-scanning service introduced by this morning's configuration change. 15:10 — configuration rolled back. 15:25 — uploads confirmed working. Post-incident review scheduled."

Statement: "The frontend team's code caused the incident."

- A) True
- B) False
- C) Cannot say

**Correct answer: C**

**Explanation:** The note attributes the incident to "a timeout between the upload service and the virus-scanning service introduced by this morning's configuration change". Whose change was it? Which team owns that configuration? The note never says. It would be tempting to answer False — the cause sounds like backend configuration, not frontend code — but that is *outside knowledge and inference about team boundaries*, not the passage. The passage neither states nor denies frontend involvement (frontend engineers sometimes hold configuration too), so the disciplined answer is Cannot say. This distinction has a workplace shadow: incident writeups deliberately describe *what* failed before *who* changed it, because blameless analysis finds causes faster than blame finds scapegoats. Practising the restraint of "the text doesn't establish that" is practising exactly the habit that makes post-incident reviews work.

**Question 7 (moderate) — Inference from a design system announcement**

Passage: "From version 5.0, the design system's date input component validates day, month, and year ranges by default. Teams upgrading from 4.x should remove any duplicate validation they added themselves, as double validation can produce conflicting error messages. Version 4.x will receive security fixes, but no new features, until March, when support ends entirely."

Statement: "After March, teams still on version 4.x will not receive security fixes."

- A) True
- B) False
- C) Cannot say

**Correct answer: A**

**Explanation:** The passage says 4.x receives security fixes "until March, when support ends entirely". "Ends entirely" closes every support channel, including security fixes; combined with "until March", the clear meaning is that after March, no fixes of any kind arrive. The statement draws precisely that implication, so it is True. This is inference at the comfortable end: the conclusion is not stated verbatim but is guaranteed by the stated words — the standard for True. Compare a statement like "teams must upgrade before March": plausible advice, but the passage never issues that instruction, so it would be Cannot say. Reading deprecation notices with this care is a genuine junior-developer duty; upgrade planning, duplicate-validation removal, and security exposure all hang off exactly these sentences, and the developer who reads them precisely saves the team from both premature panic and quiet risk.

**Question 8 (moderate) — Judging a pull request description**

Passage: Your team's guidance says pull request descriptions should state what changed, why, and how it was tested. Four colleagues draft descriptions:

1. "Fixes the thing we discussed."
2. "Updated styles."
3. "Replaced the custom accordion with the design system version to fix keyboard navigation (issue #482). Tested with keyboard, NVDA screen reader, and the automated suite; all green."
4. "Massive refactor of everything accordion-related, works now, trust me — details in the commits if you really want them."

Which description best follows the guidance?

- A) Description 1
- B) Description 2
- C) Description 3
- D) Description 4

**Correct answer: C**

**Explanation:** Score each against the three required elements — what, why, how tested. Description 1: none of the three ("the thing we discussed" excludes every future reader who wasn't in the discussion). Description 2: a vague "what", no why, no testing. Description 4: an inflated "what", an asserted-not-evidenced outcome, and testing replaced by "trust me" — pushing the reviewer's work into the commit log is the opposite of communication. Description 3 nails all three: the change (custom accordion → design system version), the reason (keyboard navigation, with a traceable issue number), and the testing (keyboard, screen reader, automated suite). It is also short — clarity and brevity are allies, not rivals. This question format (best-match-to-criteria) rewards the same mechanical discipline as true/false questions: check each option against each stated criterion, and resist choosing by tone. At work, description 3 is the one that gets reviewed quickly, and writing its like is one of the cheapest reputation-builders available to a junior developer.

**Question 9 (moderate) — Modal verbs in a security standard**

Passage: "Dependencies must be sourced from the approved registry. New dependencies should be discussed with the team before adoption. Dependency updates may be automated, but major-version updates must be reviewed by a developer before merge. Lockfiles must be committed."

Statement: "A developer who adopts a new dependency without team discussion has violated a mandatory requirement of this standard."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** Locate the relevant rule and weigh its verb. "New dependencies *should* be discussed with the team" — "should" marks a strong recommendation, not a mandate. The mandatory requirements in this passage are the "must" clauses: approved registry, review of major-version updates, committed lockfiles. Skipping team discussion is therefore a lapse against a recommendation, not a violation of a *mandatory* requirement — the statement's word "mandatory" is what makes it False. Read how surgical that is: had the statement said "has acted against the standard's guidance", the answer would be True. Single words carry the verdict, in tests and in compliance conversations alike. Your role applies modern development standards under guidance; part of that is knowing exactly which lines of a standard are the hard floor ("must") and which are the strong default you deviate from only with reasons ("should") — and never blurring them in either direction when you explain the standard to someone else.

**Question 10 (challenging) — A dense accessibility regulation extract**

Passage: "Public sector bodies must make their websites accessible unless doing so would impose a disproportionate burden. Claiming disproportionate burden requires an assessment weighing the organisation's size and resources against the benefit to disabled users; cost alone is not sufficient grounds. The claim must be recorded in the accessibility statement and reviewed when circumstances change, and it does not exempt the body from providing accessible alternatives on request where reasonable."

Statement: "An organisation that records a disproportionate burden claim in its accessibility statement is thereby exempt from all accessibility obligations for the affected content."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** The final clause defeats the statement: a recorded claim "does not exempt the body from providing accessible alternatives on request where reasonable". So even a valid, recorded claim leaves obligations standing — the statement's "exempt from all accessibility obligations" contradicts the passage, making it False. This passage rewards a structured second read: rule (accessible unless disproportionate burden), threshold for the exception (assessment; cost alone insufficient), procedure (record; review on change), and residual duty (alternatives on request). Statements about dense regulatory text almost always target one of those layers — most often the residual duty, because tired readers stop at the exception. The professional stakes are real: accessibility regulations govern your actual services, and a junior developer who can say "the burden claim doesn't remove the alternatives duty" is reading at the level the public sector requires. Layered reading — rule, exception, procedure, residue — is the technique to take away.

**Question 11 (challenging) — Overclaimed summary of an analytics report**

Passage: "Following the header redesign, average session duration rose from 3 m 10 s to 3 m 40 s, and the search feature's usage doubled. Task completion for the top three user journeys was unchanged. The redesign coincided with a national deadline that historically increases traffic and engagement. We cannot yet separate the redesign's effect from the deadline effect; the next quarter's data should clarify."

Statement: "The report shows that the header redesign increased user engagement."

- A) True
- B) False
- C) Cannot say

**Correct answer: C**

**Explanation:** The engagement metrics rose — that much the report states. But the statement claims the *redesign caused* the rise, and the report explicitly declines that conclusion: the changes "coincided" with a deadline that historically increases engagement, and "we cannot yet separate the redesign's effect from the deadline effect". The passage neither affirms causation (so not True) nor denies it (the redesign may well have contributed — so not False). Cannot say is exact. This is the correlation-versus-causation trap in verbal-reasoning clothing, and it is beloved of test writers because the wrong answers split both ways: optimists answer True (the numbers went up!), sceptics answer False (it was the deadline!) — and both exceed the evidence. The report models the honest posture: state the observation, name the confound, wait for separating data. When you shape communications for stakeholders — a named part of your role — reproducing that honesty, rather than the flattering summary, is what keeps your team's numbers trusted.

**Question 12 (challenging) — Reading a strategy extract for what it commits to**

Passage: "Our digital strategy commits us to reducing legacy frontend frameworks from four to one within three years. Migration will be incremental: new features are built in the target framework; existing screens migrate when they are next substantially changed; rarely touched screens may remain on legacy frameworks beyond the three-year horizon if risk assessments justify it. Teams will receive migration training in the first year. No service downtime is expected as a result of migration."

Statement: "Under this strategy, some screens might still use a legacy framework after three years."

- A) True
- B) False
- C) Cannot say

**Correct answer: A**

**Explanation:** The passage grants the possibility explicitly: rarely touched screens "may remain on legacy frameworks beyond the three-year horizon if risk assessments justify it". The statement claims only that this *might* happen — a possibility claim — and the passage's "may remain… if" establishes exactly that possibility. True. The delicious tension is with the headline commitment ("four to one within three years"), which sounds absolute until the detail qualifies it; strategies routinely pair a crisp goal with hedged implementation clauses, and both are part of what the document says. Match the strength of the statement to the strength of the text: "some screens *will* remain" would be Cannot say (the condition might never be met); "all screens will be migrated within three years" would be False (it contradicts the express carve-out). Your role asks you to explain the strategic context of your work — and that means reading strategy documents at this resolution, so the context you pass on to teammates is the one the strategy actually contains, hedges and all.

### Preparation tips

- **Enforce the passage-only rule.** Before answering, point to the sentence that supports your choice. If you cannot point to it, you are answering from knowledge — the test's cardinal sin and the workplace's quiet one.
- **Build a word-watch list.** Modals (must, should, may), quantifiers (all, most, some), scopes ("for development", "on request"), and time markers ("before release", "until March") decide most answers. Note them on first read.
- **Give each verdict its own test.** True needs guaranteed support; False needs contradiction; Cannot say is the remainder. Run all three checks — the first plausible verdict is not always the survivor.
- **Read dense passages in layers.** Rule, exception, procedure, residual duty. One structured re-read beats three anxious skims, in tests and in real standards.
- **Practise on your team's actual documents.** Take a paragraph of the service manual or a definition of done, write three statements (one true, one false, one unsupported), and classify them. Ten minutes of this per week compounds fast.
- **Respect the statement's exact strength.** "Might", "always", "caused", "mandatory" — the verdict often lives in one word of the statement, not the passage. Read the statement as carefully as the text.
- **Separate observation from causation.** "X rose after Y" never proves "Y caused X" unless the passage says so. The confound sentence, when present, is the answer's home.

### Common pitfalls to avoid

- **Answering from professional experience.** You know how caching, frameworks, and incidents usually work — and the passage may describe a team that works differently. Inside the test, the passage is the only reality.
- **Universalising scoped rules.** "Emulators may be used for development" does not survive as "emulators are forbidden" or "emulators are always fine". Keep every rule attached to its stage, role, or category.
- **Merging adjacent rules.** "An exception is required" and "exceptions are granted only if…" are two rules. Statements exploit readers who blend neighbouring sentences into one.
- **Sympathy-driven verdicts.** A passage with a troubling finding (blocked screen magnification users) still supports cheerful narrow claims ("most completed"), and vice versa. Judge the statement, not the mood.
- **Treating "should" as "must".** A skipped recommendation is not a violated mandate. Match obligation strength precisely — especially when the statement inserts words like "mandatory" or "forbidden".
- **Rewarding confident, vague writing.** In clear-writing questions, "trust me, it works" energy loses to short, specific, evidenced description every time. Check options against the stated criteria, not their swagger.
- **Rushing the second half of long passages.** Test writers put the decisive clause — the residual duty, the confound, the carve-out — late in the passage, where tired eyes skim. Budget attention to the end.

## Workplace job-specific situational judgement assessment

### About this assessment

A situational judgement assessment (SJT) presents realistic workplace scenarios and asks you to evaluate possible responses — typically choosing the most effective, the least effective, or ranking or rating the full set. There is no arithmetic and no formal logic; what is being measured is professional judgement: how you balance users, colleagues, standards, deadlines, and your own level of authority when they pull in different directions.

The typical format is an online test of 20 to 40 minutes covering 10 to 20 scenarios. Scoring compares your judgements against those of experienced practitioners and against the organisation's declared values. For UK government digital roles, the value set is well documented: user needs first, working in the open, inclusion and accessibility, honest and early communication, collaboration across disciplines, and proportionate escalation — raise things at the right level, having tried the direct route first.

For a junior frontend developer, the SJT models the transition your role level is all about: you now work independently with guidance, which means dozens of small judgement calls each week are genuinely yours. When do you push through a blocker versus ask? How do you disagree with a designer, correct a stakeholder's misunderstanding, or handle a standard being bent under deadline pressure? How do you balance your own ticket against a teammate who needs help? None of these have a compiler to tell you you're wrong — which is exactly why employers assess them. The reassuring news: SJTs at your level do not demand heroics or politics. They reward the honest, user-focused, collaborative option, executed at the right level of independence — enough initiative to act, enough humility to involve others at the right moment.

### How this assessment maps to your role

- **Independent judgement with guidance** maps to **Programming and build (frontend developer)** and your level's core description — working independently, with guidance from more senior developers, to identify user issues and needs. Scenarios probe whether you calibrate autonomy well: neither helpless nor heedless.
- **Advocacy and expectation management** maps to **Communicating information**: being an advocate for the team externally, managing differing perspectives, and shaping communications for the audience all appear as scenario dilemmas with stakeholders.
- **Team contribution** maps to **Community collaboration** and **Leadership and guidance (frontend developer)**: contributing to the work of others, recognising and dealing with issues, and following agreed good practice are the behaviours the scoring keys reward.
- **Holding standards under pressure** maps to **Modern development standards** and **Accessibility**: several scenarios test whether accessibility and agreed practice survive contact with deadlines and seniority.
- **User-centred instincts** maps to **User focus (frontend developer)** and **Prototyping**: when evidence, opinion, and effort collide, the assessment rewards the option that keeps real users — including disabled users — at the centre.

### Practice questions

**Question 1 (easy) — Blocked by a missing design**

You start a ticket to build a new confirmation page, but the ticket's linked design file is missing the error state. The interaction designer is on leave until Thursday; it is Tuesday. Your sprint ends Friday. What is the most effective response?

- A) Design the error state yourself and build it — you've seen plenty of error patterns.
- B) Pause the whole ticket until the designer returns.
- C) Build everything except the error state now, and message the designer (and their team channel) so the missing state is ready to discuss Thursday; check whether an existing design system error pattern is the intended one.
- D) Ask the delivery manager to extend the sprint.

**Correct answer: C**

**Explanation:** Option C shows exactly the independence-with-guidance calibration your level is about. It keeps delivery moving (most of the page needs no waiting), it surfaces the gap early through the right channels (the designer returns to a clear, answerable question rather than a surprise), and it does the intelligent homework — checking whether the design system already prescribes the error pattern, which may dissolve the blocker entirely. Option A overreaches: inventing UI without the designer bypasses the multidisciplinary collaboration your role names, and error states carry accessibility and content subtleties that are precisely the designer's craft. Option B surrenders three working days to a gap affecting one state of one page — under-independence. Option D escalates a normal, manageable gap into a process change before trying anything lighter. The SJT pattern to remember: the strong option usually *parallelises* — progress on what is unblocked, communication on what is blocked, and a check for existing patterns before anyone reinvents anything.

**Question 2 (easy) — Your bug in production**

A user support colleague forwards a complaint: dates entered in a form are displayed off by one day. You investigate and find the bug is in code you wrote and merged last week — a timezone handling mistake. It affects a small but real number of users. What is the most effective response?

- A) Fix it quietly in your next feature branch so it ships with other work.
- B) Tell the team now, raise a bug ticket with your diagnosis, propose a fix as the priority, and thank the support colleague with an update they can pass to users.
- C) Wait for the sprint retrospective to mention it, since that is where the team discusses problems.
- D) Explain to support that date handling is notoriously hard and the impact is minor.

**Correct answer: B**

**Explanation:** Option B strings together every behaviour healthy teams want: immediate transparency (the team can weigh the bug against other priorities only if it knows), a diagnosed ticket (you convert your investigation into shared knowledge — contributing to the work of others), proper prioritisation through the team rather than solo scheduling, and closing the loop with support — who face the users and deserve something accurate to tell them. Option A hides both the bug and its fix timeline inside unrelated work: users stay affected longer than necessary and the team learns nothing. Option C parks a live user-facing defect for a ceremony days away — retrospectives are for patterns and process, not for reporting active bugs. Option D spends effort on self-exculpation; "date handling is hard" is true and irrelevant to the user seeing the wrong date. Owning a mistake loudly, with a diagnosis attached, is one of the fastest trust-builders available at your level — and the scoring key knows it.

**Question 3 (easy) — A teammate needs help during your busy week**

You are deep in your own ticket, due Friday and on track but not comfortable. Another junior developer messages: they have been stuck for half a day on a build error you solved two weeks ago. What is the most effective response?

- A) Reply that you're busy this week and suggest they ask someone senior.
- B) Ignore the message until your ticket is done — your deadline comes first.
- C) Spend the whole afternoon pairing with them so they never feel unsupported.
- D) Send them the fix you used and the reason it works, offer twenty minutes on a call if it doesn't resolve, and return to your ticket.

**Correct answer: D**

**Explanation:** Option D is proportionate generosity — the collaboration sweet spot the assessment looks for. You hold knowledge that converts their half-day blockage into minutes; sharing it (with the *why*, so they learn rather than just paste) is high leverage at trivial cost to your deadline. The bounded offer of a short call handles the case where the fix doesn't transfer, without open-ending your afternoon. Option A refuses a near-zero-cost contribution — and "ask someone senior" for a problem *you* already solved wastes the senior's time too. Option B is the same refusal with worse communication: silence leaves a colleague stuck and unheard. Option C, though warm-hearted, overcorrects: donating an unbounded afternoon endangers your own commitment and does for them what a hint plus twenty minutes would teach better. Contributing to the work of others — a named part of your community collaboration skill — is rarely all-or-nothing; the strong options are almost always bounded, generous, and reason-sharing.

**Question 4 (easy) — Stakeholder asks you directly for a date**

A policy stakeholder catches you at the tea point: "You're on the payments page rebuild, right? When will it be live? I need a date for a newsletter." You genuinely don't know — the work depends on another team's API and the plan is the delivery manager's to communicate. What is the most effective response?

- A) Give your best guess — "probably a few weeks" — to be helpful.
- B) Say you don't deal with dates and walk on.
- C) Say the honest position — the date depends on a dependency and you don't want to guess wrongly for a newsletter — and connect them with the delivery manager today for the reliable answer.
- D) Promise to find out and get back to them, then let it slip given your workload.

**Correct answer: C**

**Explanation:** This scenario tests advocacy and expectation management — your communicating information skill in corridor form. Option C is honest about uncertainty (naming the dependency, without blaming the other team), respects the team's communication roles (dates for external publication are the delivery manager's to give), and still serves the stakeholder actively — a same-day connection rather than a brush-off. Option A feels helpful and is the most dangerous: a tea-point guess becomes a newsletter commitment, then a "missed deadline" the team never set. Casual numbers from developers have a way of becoming contractual in stakeholders' hands. Option B protects the team's process at the cost of the relationship — being an advocate for the team externally means representing it warmly, not tersely. Option D makes a commitment and breaks it, the worst of both. The reusable pattern: acknowledge, decline to guess, route to the owner, and do the routing yourself — helpfulness lives in the handover, not the guess.

**Question 5 (moderate) — Accessibility versus the sprint goal**

Mid-sprint, you discover the new file-upload component — built by a teammate, already merged — cannot be operated by keyboard. The sprint goal is a Thursday show-and-tell to senior stakeholders featuring this component. Fixing it properly looks like one to two days; your teammate is now on other work. What is the most effective response?

- A) Say nothing until after the show-and-tell — no point embarrassing the team in front of stakeholders.
- B) Raise it in the team channel today, tagging the teammate and lead: describe the issue, its severity for keyboard and assistive-tech users, and offer to pair on the fix or pick it up yourself before Thursday.
- C) Rebuild the component yourself tonight without telling the teammate, so it's fixed by morning.
- D) Post publicly that the component fails accessibility standards and shouldn't have passed review.

**Correct answer: B**

**Explanation:** Option B raises the issue at the speed its severity deserves (keyboard operability is fundamental — a component some users cannot operate at all is not demo-ready, it is not done), through the right channel (open to the team, so prioritisation is collective), with the right tone (factual severity, no blame), and with your own labour attached — offering to pair or fix converts criticism into contribution, and gives the sprint goal its best chance of being met *properly*. Option A knowingly showcases an inaccessible component to senior stakeholders; if they later learn the team knew, the credibility cost dwarfs any Thursday awkwardness — and users lose either way. Option C fixes the artefact while damaging the team: silent overnight rewrites deny your teammate the learning, imply distrust, and bypass review — the same practice failure in a different costume. Option D is public blame dressed as standards enforcement; review gaps are a team matter for the retrospective, not a channel spectacle. The pattern: severity honestly named, blame withheld, help attached — that trio is the scoring key for standards-under-pressure scenarios.

**Question 6 (moderate) — Disagreeing with a designer's choice**

An interaction designer hands you a design using light grey placeholder text as the only labelling for form fields. You believe this fails accessibility standards — placeholders vanish on input and the contrast looks insufficient — but the designer is experienced and the design is signed off. What is the most effective response?

- A) Build it as designed — sign-off means the decision is made, and design is their discipline.
- B) Build it your way with visible labels, and let them notice in review.
- C) Message the designer: share your specific concerns with references (standards guidance on placeholders and contrast), ask whether these were considered in sign-off, and offer to prototype a visible-label version for comparison.
- D) Raise the design at the next team meeting and ask the group to vote.

**Correct answer: C**

**Explanation:** Your role explicitly includes building interfaces that meet accessibility standards — which makes you a legitimate voice on this, sign-off or not — and equally explicitly values multidisciplinary collaboration, which rules out unilateral moves. Option C threads it: concerns made specific and evidenced (standards references shift the conversation from taste to requirement), genuine openness to the possibility that sign-off already weighed this (the question is asked, not assumed), and a prototype offer that plays to your strengths and gives the designer something concrete to evaluate — prototyping as a collaborative tool is a named skill at your level. Option A treats sign-off as infallible and outsources your professional responsibility; accessibility failures discovered in audit cost far more than a conversation now. Option B is the mirror error — right concern, wrong method: silently overriding a colleague's signed-off work ambushes them in review and corrodes exactly the relationship you need for the next hundred designs. Option D escalates socially before trying the direct conversation, and design quality is not settled by vote. Disagree early, specifically, kindly, and with something buildable in hand.

**Question 7 (moderate) — Flaky test under deadline**

Your pull request must merge today to make the release cut-off. The suite fails intermittently on one unrelated test — a known flaky test with an open ticket, failing roughly one run in five. Team practice: merges require a green build. Re-running usually produces green. What is the most effective response?

- A) Re-run until green, merge, and add a note to the flaky test's ticket that it cost you time today — nudging its priority.
- B) Comment out the flaky test in your branch so the build is deterministically green, then merge.
- C) Miss the release rather than merge anything that ever showed red.
- D) Ask a senior developer to override the green-build requirement just this once.

**Correct answer: A**

**Explanation:** This scenario rewards knowing the difference between working the process and gaming it. The team has already institutionalised this flake — known, ticketed, unrelated — so re-running to green is the accepted mechanism, not a dodge; the merge then happens with a genuinely green build, honouring the practice. The second half of option A is what elevates it: feeding today's cost into the ticket is how flaky tests eventually get fixed rather than tolerated forever — recognising and dealing with issues, not just personally surviving them. Option B silently weakens the suite: commenting out a test in a feature branch has a way of reaching main, and "deterministically green" achieved by deleting the check is the tester's equivalent of unplugging the smoke alarm. Option C treats a documented flake as if it were signal, sacrificing the release to a known false alarm — disproportionate. Option D asks seniority to waive a practice that doesn't need waiving; escalation should carry problems the normal path can't handle, and this one can. Strong answers here use the legitimate path *and* improve it.

**Question 8 (moderate) — Credit and visibility**

At a cross-team show-and-tell, your team lead presents the sprint's work, including the autocomplete component you built solo, described as "what the team built". Afterwards a developer from another team asks the lead technical questions about it, and the lead — not knowing the detail — answers vaguely. You are standing right there. What is the most effective response?

- A) Stay silent — correcting or supplementing the lead in public would undermine them.
- B) Step in helpfully: "I built that one — happy to go through the detail," answer the questions, and afterwards suggest to the lead that you'd love to co-present or demo your own pieces in future.
- C) Let the moment pass, then complain to teammates that the lead takes credit.
- D) Interrupt with "Actually, that's mine," and correct the vague answers point by point.

**Correct answer: B**

**Explanation:** Read the moment: a technical peer wants detail, the lead lacks it, the builder is present. Option B serves everyone — the asker gets accurate answers, the lead is rescued (not exposed) by a natural, collegial hand-off, and you gain deserved visibility. "The team built it" is normal presenting shorthand, so treating it as benign while quietly attaching your name through *usefulness* is both accurate and graceful. The follow-up conversation converts a one-off into a pattern: asking to demo your own work is legitimate career development, and most leads welcome it — presenting is work they're often glad to share. Option A leaves the asker with vague answers — the team's reputation for engineering depth suffers to preserve a face nobody was threatening. Option C is corridor resentment: it changes nothing, spreads negativity, and denies the lead the feedback that would fix the pattern — the opposite of understanding the importance of feedback. Option D gets the facts right and the frame wrong: "that's mine" contests credit rather than adding help, and point-by-point public correction diminishes the lead. Same information, delivered as contribution versus contest — the scoring key can tell.

**Question 9 (moderate) — Scope creep from a friendly stakeholder**

A content designer you work well with asks directly: "While you're in the confirmation page code, could you also add a print stylesheet? Tiny job, users keep asking." It probably *is* small — an hour or two — but it's not in the ticket, the sprint is tight, and unticketed work has burned the team before. What is the most effective response?

- A) Just do it — it's small, users want it, and goodwill matters.
- B) Refuse: "Not in the ticket. Raise it through the product manager."
- C) Say it sounds genuinely useful and quick, and that you want it visible rather than smuggled: offer to write the ticket with them now and flag it to the product manager for a priority call — noting you could likely take it next sprint, or this one if something moves.
- D) Do it secretly but don't mention it in stand-up, to avoid a scope discussion.

**Correct answer: C**

**Explanation:** The tension is real: user value and goodwill versus planning integrity. Option C honours both. It validates the request (users asking for print support is genuine user-needs evidence — the very thing you're meant to spot), routes it through prioritisation in the lightest possible way (writing the ticket *with* the requester, immediately, is service rather than bureaucracy), and stays honest about capacity instead of quietly absorbing it. Crucially, it keeps the product manager's picture of the sprint true — which is what protects the team the next time something must be cut. Option A trades planning integrity for goodwill: each "tiny" favour is invisible work, and invisible work is why sprints mysteriously overrun and why the *next* stakeholder's bigger favour is harder to decline. Option D is option A plus concealment — strictly worse. Option B protects the process and pointlessly spends the relationship; the same boundary delivered with help ("let's write it up now") costs nothing extra. Managing differing perspectives — the stakeholder's urgency, the team's plan — by making work visible and shared is precisely the communicating skill your role names.

**Question 10 (challenging) — Research contradicts your prototype**

You prototyped a clever inline-editing pattern for updating application details, and you're proud of it. In usability testing, two of six participants — including one screen reader user — didn't realise their changes had saved, and another accidentally edited a field. The user researcher recommends replacing it with a conventional edit-page pattern. The interaction designer agrees. You believe minor tweaks could rescue the inline pattern. What is the most effective response?

- A) Accept the recommendation immediately and delete the prototype branch.
- B) Argue the sample is too small to justify abandoning a better interaction.
- C) Accept that the evidenced default is now the conventional pattern, ask the researcher to help you understand the failures — and ask whether a tweaked version could earn a slot in a future testing round, while the team builds the conventional pattern now.
- D) Build the conventional pattern, but keep quietly refining the inline version in work hours for a future surprise reveal.

**Correct answer: C**

**Explanation:** Option C gets three things in the right order: evidence governs current decisions (the conventional pattern ships — users failing to notice saves, and accidental edits, are serious failures for a government service, and the screen reader failure especially so); curiosity replaces defensiveness (understanding *why* — missing announcements? unclear affordances? — turns a rejection into transferable interaction knowledge); and the door stays open through the legitimate channel — future research rounds exist precisely to test iterations, and researchers generally welcome a developer who wants their idea *tested* rather than *believed*. That is prototyping as your role describes it: a team activity, tested with others, iterated on evidence. Option A overcorrects — discarding the learning and the branch wholesale loses salvageable knowledge, and swallowing disagreement isn't collaboration either. Option B relitigates the method: small-sample usability testing reliably surfaces real problems (three of six participants failing is a pattern, not noise), and "better interaction" is precisely what the evidence just contested. Option D splits the team's reality — a shadow workstream consuming work hours against an agreed decision, with a "reveal" that ambushes colleagues. Hold ideas firmly enough to iterate them and lightly enough to let evidence steer; that balance is the mark the assessment is looking for.

**Question 11 (challenging) — A senior developer's questionable instruction**

A senior developer, rushing before a demo, tells you: "Strip out the focus outline styles globally — the blue rings look messy in the demo. We'll put them back after." Removing focus indicators would make the service unusable for keyboard users, and the change would go through the normal deploy pipeline to production. What is the most effective response?

- A) Do it — they're senior, it's temporary, and it's their responsibility.
- B) Say you're not comfortable removing focus indicators even temporarily since it ships to production and breaks keyboard use — and offer a demo-safe alternative: a local flag, a demo environment tweak, or restyled (but visible) focus indicators; if they insist, say you'd want the tech lead's view first.
- C) Say yes, then simply not do it and hope the demo goes fine.
- D) Refuse and immediately report the request to the head of profession as an accessibility violation.

**Correct answer: B**

**Explanation:** This is the assessment's classic seniority-versus-standards test, and option B demonstrates the full professional sequence. First, a clear, reasoned decline — naming the actual harm (production keyboard users, not "the rules say"), because reasons persuade where refusals grate. Second — and this is what separates strong answers — *alternatives that solve the senior's real problem*: their need is a clean-looking demo, not the absence of accessibility, and a demo-environment tweak or nicely restyled focus indicators (entirely legitimate — visible ≠ ugly) gives them a yes to something. Third, proportionate escalation *announced, not sprung*: "I'd want the tech lead's view" keeps it transparent and routes deadlock to the right level — not silence, not the head of profession. Option A executes a change you know harms users; "temporary" removals have a way of surviving demos, and seniority doesn't transfer accountability for what you personally push. Option C avoids the conflict by deceit — the worst of all worlds, since the senior discovers mid-demo that their instruction was silently ignored. Option D leaps past every intermediate step to maximal escalation, converting a rushed bad idea into a formal incident; that's not courage, it's poor calibration. Decline with reasons, offer a better path, escalate transparently if needed — that pattern serves you at every level of your career.

**Question 12 (challenging) — Least effective: the abandoned improvement**

Your team's retrospective agreed the pattern library documentation is badly out of date, and you volunteered to update it "as capacity allows". Three sprints later you've done none of it — features always felt more urgent, and nobody has chased you. The stale docs have now misled a new developer into rebuilding an existing component. Which response would be the *least* effective?

- A) Acknowledge in the retro that you took this on and it hasn't moved, propose either timeboxing it into next sprint as a real ticket or handing it to someone with capacity, and pair with the new developer to merge their duplicate with the existing component.
- B) Quietly delete the outdated pages so they can't mislead anyone else, without telling the team.
- C) Apologise to the new developer, explain what happened, and ask the delivery manager to make the documentation work visible on the board.
- D) Raise the pattern in the retro: "as capacity allows" tasks never get capacity, so the team should stop creating them and ticket improvement work properly.

**Correct answer: B**

**Explanation:** In least-effective questions, hunt for the option combining concealment, information loss, and unilateral action — option B has all three. Deleting the outdated pages secretly removes *wrong* information by removing *all* information: the next developer finds nothing instead of something stale, and nobody knows why the docs vanished or that a gap now exists. It also disguises the real problem (unowned, invisible improvement work) instead of surfacing it, guaranteeing recurrence — and it does all this without the team's knowledge, eroding the openness the working culture depends on. The other three options are all creditable, each attacking a different layer: A owns the lapse and fixes both the immediate harm (the duplicate component) and the commitment structure; C repairs the relationship and makes the work visible; D fixes the systemic cause — vague "capacity allows" commitments — which is a genuinely mature retrospective contribution. Notice, as exam technique, that you need not rank A, C, and D against each other; least-effective questions only require identifying the option that damages most. And absorb the honest lesson inside the scenario: volunteering and then silently not delivering is common, human, and recoverable — *if* it's surfaced. The unrecoverable version is the cover-up.

### Preparation tips

- **Anchor on the public value set.** Users first (especially disabled users), openness, early honesty, collaboration, proportionate escalation. When torn between options, ask which one a team living those values would applaud — that is almost always the key.
- **Calibrate to your level.** The junior sweet spot is act-then-inform for normal work, consult-first for cross-discipline or standards territory, and escalate-transparently for deadlock. Options that are fully solo or fully dependent usually score poorly.
- **Look for the three-part option.** Strong responses tend to fix the immediate problem, protect the relationship, and improve the system (a ticket, a retro item, a fed-back lesson). Count the parts when comparing candidates.
- **Learn the weak-option clusters.** Concealment, guessing dates, silent workarounds, public blame, sunk-cost defence, over-escalation, and "wait and hope" recur across every SJT. Spotting the cluster is faster than reasoning each time.
- **Attach help to every objection.** Notice how many strong answers pair a "no" with an offer — a prototype, a pairing session, a demo-safe alternative, a co-written ticket. Practise that reflex in real life; it will surface naturally in the test.
- **Rehearse real memories.** Before assessment day, recall five actual moments: a mistake you owned, a disagreement you raised well, a boundary you held, help you gave, help you asked for. Concrete memories calibrate judgement better than principles alone.
- **Read scenarios forensically.** Details like "already merged", "signed off", "ships to production", or "known flaky test with a ticket" change the correct answer. SJTs reward careful reading as much as good values — the two skills are one skill.

### Common pitfalls to avoid

- **Deference dressed as respect.** "They're senior / experienced / signed off" never by itself justifies shipping harm or staying silent. The strong options respect people *and* hold the standard — usually by offering alternatives.
- **Kindness dressed as avoidance.** Not telling the team about a bug, a missed commitment, or an inaccessible component to spare feelings always scores badly. The genuinely kind option is early, factual, and blame-free.
- **Initiative dressed as unilateralism.** Redesigning the designer's work, rewriting a teammate's component overnight, deleting docs — energy applied without consent damages more than it fixes. Channel initiative through offers, prototypes, and tickets.
- **Process dressed as obstruction.** Flat "raise it through the proper channel" refusals protect the letter of the process while burning the relationship. Walk the requester through the channel instead — same boundary, opposite effect.
- **Honesty applied selectively.** Giving stakeholders guessed dates, staying quiet in demos, or "yes then don't" moves all trade long-term trust for short-term comfort. The scoring key prices trust correctly; price it the same way.
- **Over-escalation as virtue.** Skipping the direct conversation to reach a lead, a vote, or a head of profession reads as poor judgement, not high standards. Escalate after the direct route, transparently, to the nearest appropriate level.
- **Polishing "most effective" and guessing "least".** The least-effective half of questions is quick once you look for concealment, irreversibility, information loss, and user harm. Answer it with the same care — it carries the same marks.

<!-- APPEND -->
