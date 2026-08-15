# Senior Frontend Developer - Psychometric Assessment Resources

## Introduction

Welcome! This guide has been created especially for you as a senior frontend developer working within the UK Government Digital and Data profession. Whether you are preparing for an internal assessment, applying for a new post, benchmarking your own capability against the framework, or simply curious about how psychometric assessments relate to the work you do every day, this document will help you practise, reflect, and build confidence.

Psychometric assessments are structured, standardised exercises that measure the mental capabilities and behavioural tendencies that predict success in a role. For a senior frontend developer, that means far more than abstract puzzles. The assessments described here are job-specific: they use the kinds of artefacts you genuinely handle — HTML, CSS and JavaScript, accessibility audit reports, web performance dashboards, build pipelines, design patterns, pull requests, sprint boards and stakeholder emails — and the kinds of decisions you genuinely make, such as planning and leading development on sets of related stories, making research-based decisions about tools and approaches, championing accessibility to internal stakeholders, and teaching and mentoring less experienced developers.

Why do these assessments matter for your role in particular? As a senior frontend developer you work with minimal support and you influence others. You help set direction and embed good practice within teams, you hold an understanding of the whole system rather than one corner of it, and you collaborate with user researchers, interaction designers and other disciplines to understand what needs to be built before a line of code is written. Assessments of cognitive ability, numerical reasoning, verbal reasoning and situational judgement map directly onto those demands. Practising them sharpens exactly the skills your role depends on: spotting the logical flaw in a progressive enhancement plan, interpreting a web performance monitoring table under time pressure, extracting precise meaning from an accessibility standard or a dense service assessment report, and choosing the most effective course of action when a stakeholder pushes for a feature that conflicts with user needs.

This document is organised into four main assessment sections, each following the same pattern: an overview of what the assessment measures and why employers use it for your role, a mapping of the assessment dimensions to the specific skills in the frontend developer capability framework at senior level, a substantial set of practice questions with full worked explanations, practical preparation tips, and common pitfalls to avoid.

Here is how to get the most from it. First, read each "About this assessment" section so you understand the format and the timing pressure you can expect. Second, attempt the practice questions honestly — write down your answer before reading the explanation, and note how confident you felt. Third, treat every explanation as a mini-lesson: even when you answer correctly, the worked reasoning will deepen your technique and often shows you a faster route than the one you took. Finally, use the preparation tips and pitfalls for self-reflection: they connect assessment performance back to your professional development as a developer who sets direction, embeds good practice, and mentors others.

You already reason about systems, standards and users every working day. These assessments simply ask you to do it in miniature, against the clock. Take your time with the practice, be kind to yourself when a question catches you out, and enjoy the process. Let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive ability assessment measures the exact mental processes your role demands, using practical workplace scenarios rather than abstract shapes and sequences. Unlike a generic intelligence test, it presents you with the everyday materials of your job — markup and stylesheets, component libraries, accessibility audit findings, build configurations, browser support matrices and sprint boards — and asks you to reason quickly and accurately about them.

Typical format: an online, timed test lasting 15 to 30 minutes, with somewhere between 15 and 30 questions covering pattern recognition, logical deduction, error checking, prioritisation and applied problem solving. Scoring is objective, comparing your responses against a norm group of people at a similar level, and modern platforms often adapt question difficulty based on your previous answers — so a test that feels progressively harder is usually a sign you are doing well, not badly. Employers typically receive a breakdown of speed versus accuracy rather than a single number, so working both quickly and carefully matters. You will normally be offered short, ungraded practice questions before the real test begins, so you can get comfortable with the interface without pressure.

For a senior frontend developer, cognitive assessment is particularly relevant because your core professional value is structured thinking about a whole system. You are expected to understand how the pieces fit together: how a change to a shared component ripples across services, how the static assets build feeds the deployment pipeline, how a CSS rule interacts with the cascade, and what follows logically when a browser lacks JavaScript support and your progressive enhancement strategy has to carry the experience. You also plan and lead development on sets of related stories, which means decomposing a feature into a dependency-ordered sequence of work and spotting the constraint that everyone else has missed. A well-designed cognitive assessment simulates precisely those demands in miniature.

Employers use these assessments at senior level for two reasons. First, cognitive ability is one of the strongest single predictors of performance in complex technical work, and seniors face the most complex work: high-complexity user interfaces, cross-team integration, and decisions with medium levels of risk. Second, at senior level your reasoning is amplified through others — you teach, mentor and review — so an error in your thinking propagates. The assessment gives an employer evidence that your reasoning is fast, accurate and disciplined.

### How this assessment maps to your role

The assessment dimensions map directly to the named skills in your capability framework at senior level:

- **Pattern recognition** maps to your **Prototyping** skill — you establish design patterns and iterate them, which means recognising when several superficially different interface problems share one underlying structure — and to **Programming and build (frontend developer)**, where reviewing specifications and building interfaces of medium to high complexity depends on seeing recurring structures in code and markup.
- **Logical deduction** maps to **Systems integration (frontend developer)**: when you define the static assets build, co-ordinate all aspects of the integration and configure the part of the system that uses the network, you must reason validly from configuration and dependency rules to their consequences. It also maps to **Strategic thinking**, because evaluating whether current strategies meet business requirements is an exercise in reasoning from principles to outcomes.
- **Error checking** maps to **Accessibility** — offering design feedback to mitigate the risk of failing accessibility testing is systematic error detection against a predefined set of standards — and to **Modern development standards**, because applying standards and supporting others in applying them means spotting where code departs from them.
- **Prioritisation** maps to **Leadership and guidance (frontend developer)**: you make decisions characterised by medium levels of risk and complexity, and you plan and lead development on sets of related stories, which requires rapidly ranking competing demands. It also draws on **User focus (frontend developer)**, because you effectively prioritise and define approaches to understand the user story.
- **Applied problem solving** maps to **Web performance optimisation** — identifying and resolving web performance issues is diagnostic reasoning under constraints — and to **Communicating information** and **Community collaboration**, because identifying issues through Agile health checks and working with others to address them starts with correctly diagnosing what is actually wrong.

### Practice questions

**Question 1 (easy) — Pattern recognition in a component library**

Your team's design system names components with a BEM-style convention: a block name, then two underscores and an element, then two hyphens and a modifier where needed. Valid examples: `app-card`, `app-card__title`, `app-card__title--large`. While reviewing a junior developer's pull request you see these class names:

1. `app-banner`
2. `app-banner__heading`
3. `app-banner--warning`
4. `app-banner__heading--small`
5. `app-banner--warning__icon`

Which class name breaks the convention?

- A) Class 2
- B) Class 3
- C) Class 4
- D) Class 5

**Correct answer: D**

**Explanation:** The convention builds names in the order block, then element, then modifier. Class 5 attaches an element (`__icon`) to a modifier (`--warning`), inverting the order: the correct form would be `app-banner__icon--warning` if the icon itself has a warning variant, or the icon would simply inherit styling from the modified block. Classes 1 to 4 all follow the block, block-element, block-modifier and block-element-modifier forms exactly. This is the kind of consistency check you perform constantly when you establish design patterns and iterate them: naming conventions look trivial, but broken conventions quietly destroy the predictability that lets any developer on any team find, reuse and extend a component — and predictability is the whole point of a design system.

**Question 2 (easy) — Logical deduction about progressive enhancement**

Your team's standard states: "Every citizen-facing form must be fully usable without JavaScript, unless the service has a documented exemption agreed by the technical lead." During a review, a developer tells you: "The address lookup form on our service is citizen-facing and is not usable without JavaScript." Which one of the following conclusions must be true?

- A) The team has breached the standard.
- B) The service holds a documented exemption agreed by the technical lead.
- C) Either the service holds a documented exemption, or the team has breached the standard.
- D) The address lookup uses a third-party component that requires JavaScript.

**Correct answer: C**

**Explanation:** The standard is a conditional rule with one permitted exception. From the facts given you cannot tell whether an exemption exists, so neither A nor B must be true on its own — each is merely possible. D introduces information not present anywhere in the stem. The only conclusion guaranteed in every case consistent with the facts is the either/or statement in C. Assessments reward exactly this discipline: deduce only what the given information guarantees. In your role the same discipline has practical value — before flagging non-compliance in a review, you check whether an exemption was agreed, which protects both your logic and your working relationships. Writing clean, accessible code following a progressive enhancement approach is a duty of your role, but enforcing it well requires deducing carefully, not accusing quickly.

**Question 3 (easy) — Error checking a browser support table**

Your service's browser support policy requires "compliant" support for the two most recent versions of each major browser and "functional" support for the version before those. A junior developer drafts this support table for a new feature:

| Browser | Version N | Version N-1 | Version N-2 |
|---|---|---|---|
| Browser A | Compliant | Compliant | Functional |
| Browser B | Compliant | Functional | Functional |
| Browser C | Compliant | Compliant | Functional |
| Browser D | Compliant | Compliant | Compliant |

How many rows fail to meet the policy's minimum requirements?

- A) 0
- B) 1
- C) 2
- D) 3

**Correct answer: B**

**Explanation:** Translate the policy precisely: versions N and N-1 must be at least compliant; version N-2 must be at least functional. Row A meets it exactly. Row B fails because version N-1 is only functional where compliant is required. Row C meets it exactly. Row D exceeds it — compliant everywhere — and exceeding a minimum is not a failure. So exactly one row fails. Two traps are built in: counting row D as wrong because it differs from the pattern of the others (a minimum standard is a floor, not a template), and counting rows A and C as suspicious because N-2 is "only" functional (functional is precisely what the policy requires there). Reading a standard as stating minimums rather than exact targets is a habit that serves you in accessibility and support work alike.

**Question 4 (moderate) — Deduction from a build pipeline**

Your static assets build has these rules: (i) the CSS build cannot start until the design tokens package has been generated; (ii) the JavaScript bundle and the CSS build can run in parallel, but both must finish before the fingerprinting step; (iii) fingerprinting must finish before the assets are published to the CDN; (iv) the design tokens generation takes 2 minutes, the CSS build 4 minutes, the JavaScript bundle 5 minutes, fingerprinting 1 minute, and publishing 2 minutes. The JavaScript bundle starts at time zero, and the design tokens generation also starts at time zero. What is the earliest time, in minutes from the start, at which publishing can complete?

- A) 9
- B) 10
- C) 12
- D) 14

**Correct answer: A**

**Explanation:** Work forwards through the dependency graph. Design tokens: start 0, finish at minute 2. CSS build: can start at 2, takes 4, finishes at 6. JavaScript bundle: starts at 0, takes 5, finishes at 5. Fingerprinting needs both builds, so it starts at the later of 5 and 6 — that is, 6 — and finishes at 7. Publishing starts at 7, takes 2, and completes at minute 9. The critical path runs through the design tokens and CSS build: 2 + 4 + 1 + 2 = 9 minutes; the JavaScript bundle, finishing at 5, sits comfortably inside that path and adds nothing to it. The distractor 10 comes from wrongly serialising the tokens step before the JavaScript bundle as well; 12 comes from serialising the two builds after the tokens; 14 from serialising every step. Defining the static assets build is your named responsibility within **Systems integration**, and this is exactly the reasoning you use when a pipeline feels slow: you optimise the critical path, not the loudest step — a faster JavaScript bundler here would save nothing at all.

**Question 5 (moderate) — Prioritisation across a sprint**

It is Monday morning of the final week of a sprint. Four items compete for your attention as the senior developer on the team:

1. A live accessibility defect: keyboard users cannot dismiss a cookie banner on the production service. The service is used daily by the public.
2. A pull request from a junior developer implementing a new component; they are blocked on your review to continue their next story, due Friday.
3. A request from the delivery manager to update the browser support documentation before a show-and-tell on Thursday.
4. An intermittent flaky test in the pipeline that fails roughly one build in ten, which the team re-runs when it happens.

Which sequencing is most defensible?

- A) 1, 2, 3, 4 — live user harm first, then unblocking a person, then a dated commitment, then an irritant
- B) 2, 1, 3, 4 — never leave a mentee blocked
- C) 1, 4, 2, 3 — fix all technical issues before process work
- D) 4, 1, 2, 3 — pipeline health underpins everything else

**Correct answer: A**

**Explanation:** Prioritisation questions test reasoning about impact and urgency together. Item 1 is both urgent and high impact: a production defect that blocks keyboard users from dismissing an overlay is live harm to users with access needs, on a public service, and championing accessibility is a named part of your role — it comes first. Item 2 is next: a blocked person compounds — every hour of your delay costs their progress too, and mentoring is part of your level. Item 3 has a real deadline (Thursday) but is documentation with modest impact, and item 4, while worth fixing, currently costs only occasional re-runs. Option B puts a convenience above live user harm; C and D treat "technical" as automatically more important than "human", which inverts how a senior weighs impact. Note the pattern in the strongest answer: impact-weighted urgency, with user harm at the top — precisely the ordering your **User focus** and **Leadership and guidance** skills describe.

**Question 6 (moderate) — Pattern recognition in defect reports**

Over the past month, your service's defect log shows these frontend issues: (1) a date field rejects valid dates when the user's device is set to a non-UK locale; (2) a currency input mis-parses amounts entered with a comma as the thousands separator; (3) a name field rejects surnames containing an apostrophe; (4) the postcode lookup fails for postcodes entered in lower case; (5) page titles are truncated on the service's welsh-language version. What single underlying theme most usefully connects the largest number of these defects?

- A) The team lacks automated tests.
- B) Input handling assumes one narrow format instead of accepting and normalising the variety real users produce.
- C) The service was not tested on mobile devices.
- D) The defects are unrelated and should be fixed individually.

**Correct answer: B**

**Explanation:** Defects 1 to 4 all share one structure: the code accepts a single canonical input format and rejects or mishandles legitimate variants — locale-formatted dates, comma-separated amounts, apostrophes in names, lower-case postcodes. Defect 5 is adjacent (an internationalisation gap) but the strongest common thread across the largest number is tolerant input handling: be liberal in what you accept, then normalise. Option A might be true but is not shown by the data — tests encoding the same narrow assumptions would pass while users still suffered. Option C is unsupported; nothing links these defects to device type. Option D surrenders the insight entirely. Spotting the shared root cause is what turns five tickets into one pattern, one team conversation and one lasting fix — exactly what your **Prototyping** skill means by establishing design patterns and iterating them, and what embedding good practice within teams looks like in defect triage.

**Question 7 (moderate) — Logical deduction about CSS cascade**

A stylesheet contains, in this order: (i) a rule `.button { background: blue; }`; (ii) a rule `#main .button { background: green; }`; (iii) a rule `.button--warning { background: red; }`. A button element inside `#main` has the classes `button button--warning`. No other rules or inline styles apply. What background colour does the button have, and why?

- A) Red — the last rule in the stylesheet wins
- B) Green — the ID-based selector has higher specificity than any single class
- C) Blue — the first matching rule wins
- D) Red — modifier classes always override base styles

**Correct answer: B**

**Explanation:** The cascade resolves competing declarations by origin, then specificity, then source order. All three rules are author rules, so specificity decides. Rule (ii) contains an ID selector plus a class, giving it specificity higher than any selector built from classes alone; rules (i) and (iii) are single classes. Source order only breaks ties, and there is no tie: green wins. Option A applies source order without checking specificity first — the single most common cascade error. Option D describes a convention (modifiers should override) rather than a mechanism; the convention only holds when specificity is kept deliberately flat, which is exactly why design systems avoid ID selectors. As a senior who contributes to best practice guidelines, you will recognise this question as the argument for those guidelines in miniature: a team that keeps specificity flat makes the cascade predictable, and predictable cascades make modifier classes behave the way rule D wrongly assumes they always do.

**Question 8 (moderate) — Error checking an accessibility audit response**

An external audit reports four findings against WCAG 2.2 AA: (1) images of text used in hero banners; (2) a colour contrast ratio of 3.8:1 on body text; (3) no visible focus indicator on custom dropdowns; (4) form errors announced only by colour change. The team's draft response says: "Finding 1: replaced images of text with styled real text. Finding 2: darkened the text to achieve 4.2:1. Finding 3: added a two-pixel focus outline. Finding 4: added an error icon beside the field." Which remediation is insufficient?

- A) Finding 1's remediation
- B) Finding 2's remediation
- C) Finding 3's remediation
- D) Finding 4's remediation

**Correct answer: B**

**Explanation:** WCAG 2.2 AA requires a contrast ratio of at least 4.5:1 for normal-size body text; 4.2:1 improves on 3.8:1 but still fails the standard — an improvement is not a pass. Finding 1's fix (real text instead of images of text) is the canonical remedy. Finding 3's visible focus outline addresses the failure. Finding 4's icon adds a non-colour cue, which addresses "colour alone"; pairing it with a text message would be stronger still, but the icon does cross the compliance line, whereas 4.2:1 does not. The assessment habit here is checking claimed fixes against the actual threshold rather than accepting the direction of travel — precisely what your **Accessibility** skill means by offering design feedback to mitigate the risk of failing accessibility testing. Teams fail audits twice when nobody checks the numbers in the remediation.

**Question 9 (challenging) — Multi-constraint story planning**

You are planning five related stories — API contract agreement (A), backend endpoint build (B), component build (C), integration (I) and accessibility testing (T) — across five sprints, at most one story starting per sprint. Constraints: (i) A must be completed before both B and C start; (ii) I cannot start until both B and C are complete; (iii) T must start in the sprint immediately after I; (iv) each story takes exactly one sprint; (v) B is delivered by another team who are only free from sprint 3 onwards. In which sprint must C start?

- A) Sprint 1
- B) Sprint 2
- C) Sprint 3
- D) Either sprint 2 or sprint 3

**Correct answer: B**

**Explanation:** Only one story can start per sprint and there are five stories and five sprints, so every sprint starts exactly one story — the schedule has no slack. A must precede B and C, so A is sprint 1. B cannot start before sprint 3. I needs B and C done, and T follows I immediately, so I and T must be the last two sprints in that order: I in sprint 4, T in sprint 5. That leaves sprints 2 and 3 for C and B. B cannot take sprint 2 (the other team is unavailable), so B is sprint 3 and C must be sprint 2. Option D is the trap for solvers who check C's own constraints but not the knock-on effect of B's availability window in a zero-slack plan. This is exactly the reasoning behind planning and leading development on sets of related stories: the binding constraint on your schedule is often another team's calendar, not your own team's velocity, and a senior spots that before the sprint starts rather than during it.

**Question 10 (challenging) — Applied problem solving in performance diagnosis**

Users report that a service page feels slow on mobile. You gather four facts: (i) the server responds to the HTML request in 120 milliseconds; (ii) the page's JavaScript bundle is 900 KB compressed and is loaded with a blocking script tag in the head; (iii) images are correctly sized and lazy-loaded; (iv) the CSS is 40 KB and inlined for the critical path. Which hypothesis best explains the reported slowness, and what is the strongest first fix?

- A) Slow server — add a CDN in front of the HTML
- B) The blocking 900 KB bundle delays rendering and interactivity — defer it, split it, and load only what the page needs
- C) Images — convert them to a newer format
- D) Inlined CSS — move it to an external cached file

**Correct answer: B**

**Explanation:** Reason from the evidence. The server answers in 120 ms, so A attacks a non-problem. Images are already sized and lazy-loaded, so C optimises what is optimised. The inlined critical CSS at 40 KB is a performance technique, not a defect, so D would likely make first render slower. That leaves the bundle: 900 KB compressed is very large, and a blocking script in the head halts parsing until it downloads and executes — on a mid-range mobile over a cellular connection, that alone can add many seconds to first render and interactivity. The fix sequence in B follows the standard playbook: defer or async the script so parsing continues, split the bundle so each page loads only its own code, and audit what fills 900 KB. Notice the method as much as the answer: three of the four options fail not because they are bad techniques but because the evidence rules them out. Identifying and resolving web performance issues — your **Web performance optimisation** skill — is precisely this discipline of letting measurements eliminate hypotheses before you spend effort.

**Question 11 (challenging) — Deduction across a whole system**

Your service renders a form server-side, enhances it with JavaScript, and submits to an API. Three statements are true: (i) if the JavaScript enhancement loads, client-side validation runs before submission; (ii) the API applies server-side validation to every submission it receives; (iii) last week, at least one submission reached the database containing an invalid postcode. Which conclusion follows necessarily?

- A) The JavaScript enhancement failed to load for that submission.
- B) The server-side validation contains a gap that permits that invalid postcode.
- C) Client-side and server-side validation use different postcode rules.
- D) A user bypassed the form and called the API directly.

**Correct answer: B**

**Explanation:** Follow the guarantees. Statement (ii) says every submission passes through server-side validation — with no exceptions stated — yet an invalid postcode reached the database. The only way both can be true is that the server-side validation checked the value and allowed it: its rules have a gap. Option A is possible but not necessary — even without client-side validation, the server-side check should have caught the value, and even with client-side validation the value might have been accepted there too. Options C and D are likewise merely possible routes to the outcome, not necessary ones. The deduction that survives every consistent scenario is B. This mirrors a principle you teach when mentoring: client-side validation is a courtesy to users; server-side validation is the guarantee, so when bad data lands, the guarantee is where you look first. Having an understanding of the whole system — a duty at your level — is exactly what lets you locate the one component whose promise was broken.

**Question 12 (challenging) — Prioritising a design pattern decision**

Three teams in your programme have each built their own autocomplete component. Team 1's is accessible but slow on long lists; Team 2's is fast but fails screen reader testing; Team 3's is accessible and fast but tightly coupled to their service's framework version. You have capacity to establish one shared pattern this quarter. What is the most defensible approach?

- A) Adopt Team 2's — performance problems are harder to fix than accessibility problems
- B) Adopt Team 3's after investing the effort to decouple it, because it is the only candidate that already meets both user-facing requirements
- C) Adopt Team 1's — accessibility must always win, and speed is a nice-to-have
- D) Ask all three teams to keep their own components and publish guidance instead

**Correct answer: B**

**Explanation:** Rank the properties by how they affect users and how tractable they are. Accessibility failures and slowness both harm users directly; coupling harms only developers, and is the most mechanically fixable of the three — decoupling is refactoring work with a known endpoint, whereas retrofitting accessibility into Team 2's component or performance into Team 1's is open-ended. Team 3's component is the only one that already delivers both user-facing qualities, so investing engineering effort where the remaining problem is internal is the best value. Option A inverts the difficulty — accessibility retrofits on interactive widgets are notoriously hard. Option C accepts a known user harm (slowness) when a candidate without it exists. Option D avoids the decision and forfeits the point of a shared pattern: consistency, pooled maintenance and one accessibility sign-off instead of three. Establishing design patterns and iterating them is your named **Prototyping** responsibility, and this is what it looks like as a decision with medium risk and complexity — the kind your **Leadership and guidance** skill says you make.

### Preparation tips

- **Practise with your own artefacts.** Ten minutes reviewing a colleague's pull request for convention breaks, or tracing your build pipeline's critical path on a whiteboard, is cognitive assessment practice in disguise. The test's scenarios will feel familiar because they are your job.
- **Rehearse deduction discipline.** When you read a standard, a policy or a specification this week, ask: what does this guarantee, what does it permit, and what does it merely suggest? The distinction between "must be true" and "could be true" decides most deduction questions.
- **Time-box your practice.** Set a timer at roughly 60 to 90 seconds per question. Senior-level tests reward the ability to recognise when a question deserves 30 seconds and when it deserves two minutes.
- **Work the answer options.** On error-checking and deduction questions, elimination is often faster than derivation: three options usually contain a specific, findable flaw.
- **Recompute when in doubt.** If two lines of reasoning disagree, redo the calculation from the start rather than picking the answer you reached first. Fast, confident recomputation is a trainable skill.
- **Sleep and setup matter.** Take the real test rested, on a reliable connection, with paper and a pen for working. These mundane factors move scores more than last-minute cramming does.

### Common pitfalls to avoid

- **Pattern-matching past the details.** Seniors recognise question types quickly, then sometimes answer the type instead of the question. The stem's specific numbers, orderings and exceptions are where the marks live.
- **Treating minimum standards as templates.** A row that exceeds a minimum is compliant; a row that matches the pattern of its neighbours may still fail. Check against the rule, not against the crowd.
- **Applying source order before specificity, or urgency before impact.** Ordered decision procedures — the cascade, prioritisation frameworks — must be applied in order. Skipping the first criterion is the classic error in both.
- **Concluding more than the evidence guarantees.** "The team breached the standard" and "the enhancement failed to load" are plausible stories; assessments ask for necessary truths. Keep plausible and necessary in separate mental boxes.
- **Spending three minutes rescuing one hard question.** Adaptive tests in particular punish this: flag it, move on, and bank the questions you can answer. Your overall accuracy-speed profile matters more than any single item.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace numeric reasoning assessment measures your ability to interpret, manipulate and draw sound conclusions from numerical information of the kind your job actually produces. It is not a mathematics exam: the arithmetic rarely goes beyond percentages, ratios, averages, rates and proportional change. The difficulty lies in reading data accurately under time pressure, choosing the right operation, and resisting the plausible-looking wrong answer.

Typical format: an online, timed test of 20 to 30 minutes containing 15 to 25 questions, each based on a short table, chart or data statement. Calculators are usually permitted — the test measures reasoning, not mental arithmetic — and many platforms are adaptive, adjusting difficulty as you go. Employers receive accuracy and speed profiles benchmarked against a norm group. As with the cognitive assessment, you will usually get a couple of unscored warm-up questions to learn the interface.

For a senior frontend developer, numeric reasoning is a daily, practical skill dressed in test clothing. Your **Web performance optimisation** skill explicitly requires you to collect data to monitor and resolve web performance issues: bundle sizes in kilobytes, load times in milliseconds, Lighthouse scores, Core Web Vitals percentiles, cache hit rates. Your role at senior level requires you to make decisions based on research — which means reading analytics, A/B test results and usage statistics well enough to know when a difference is real and when it is noise. You plan and lead development on sets of related stories, which brings velocity, capacity and defect-rate arithmetic. And when you champion accessibility or performance to stakeholders, your case is far stronger when the numbers in it are unimpeachable — a senior who mis-states a percentage in a governance paper spends the next month rebuilding credibility.

Employers use numeric reasoning assessments for senior developers because the role sits at the point where measurements turn into decisions. A mid-level developer might report that "the bundle got smaller"; a senior is expected to say by how much, whether that is enough, what it will cost to go further, and whether the effort is worth it compared with the alternatives. That judgement is numerical at its core.

### How this assessment maps to your role

- **Percentages and proportional change** map to **Web performance optimisation**: page-weight budgets, compression savings, and regression thresholds are all expressed as percentages, and identifying and resolving web performance issues means computing them correctly and quickly.
- **Averages and weighted averages** map to your duty to make decisions based on research and to **User focus (frontend developer)**: real usage data must be weighted by traffic, device mix or user group before it supports a decision — an unweighted average across services of wildly different size misleads.
- **Ratios and rates** map to **Programming and build (frontend developer)** and to planning and leading development on sets of related stories: defect rates per story point, review turnaround per pull request, and build failure rates are the numbers you use to embed good practice within teams and to spot where practice is slipping.
- **Reading tables and charts** maps to **Communicating information** and **Strategic thinking**: when you manage stakeholder expectations or evaluate whether current strategies meet business requirements, the evidence usually arrives as a table, and the senior in the room is the person expected to read it correctly first time.
- **Threshold and budget arithmetic** maps to **Accessibility** and **Modern development standards**: contrast ratios, error budgets, support-matrix coverage and performance budgets are all pass/fail thresholds, and offering recommendations on the best tools and methods includes knowing exactly how far short of a threshold something falls.

### Practice questions

**Question 1 (easy) — Percentage reduction in bundle size**

Your service's main JavaScript bundle is 800 KB. After you remove an unused charting library and enable tree shaking, it is 620 KB. What percentage reduction have you achieved?

- A) 18%
- B) 22.5%
- C) 25%
- D) 29%

**Correct answer: B**

**Explanation:** Step 1: find the absolute reduction: 800 − 620 = 180 KB. Step 2: divide by the original size, because percentage change is always measured against the starting value: 180 ÷ 800 = 0.225. Step 3: convert to a percentage: 0.225 × 100 = 22.5%. The distractor 29% comes from dividing by the new size (180 ÷ 620 ≈ 0.29) — the single most common percentage-change error, and one worth naming when you mentor others: always ask "percentage of what?". When you report performance work to your team or a stakeholder, "a 22.5% reduction in bundle size" is the kind of precise, checkable claim that builds the credibility your **Web performance optimisation** guidance relies on.

**Question 2 (easy) — Average page load time**

You take five measurements of a page's load time on a mid-range mobile device: 2.1 s, 2.4 s, 1.9 s, 2.6 s and 2.5 s. What is the mean load time?

- A) 2.2 s
- B) 2.3 s
- C) 2.4 s
- D) 2.5 s

**Correct answer: B**

**Explanation:** Step 1: sum the measurements: 2.1 + 2.4 = 4.5; 4.5 + 1.9 = 6.4; 6.4 + 2.6 = 9.0; 9.0 + 2.5 = 11.5 s. Step 2: divide by the number of measurements: 11.5 ÷ 5 = 2.3 s. A quick sanity check protects you from slips: the values range from 1.9 to 2.6, so the mean must sit between them, which eliminates nothing here but would catch a mis-keyed total. In real performance work you would also note that a mean can hide what matters — a median and a 75th percentile tell you more about typical and poor experiences, which is why Core Web Vitals report percentiles. Assessments mostly ask for means because they are quick to compute; your professional habit of asking "is the mean the right summary?" is a separate and valuable layer on top.

**Question 3 (easy) — Ratio of accessibility findings**

An accessibility audit of your service raises 45 findings. Critical, major and minor findings are in the ratio 1 : 3 : 5. How many major findings are there?

- A) 5
- B) 9
- C) 15
- D) 25

**Correct answer: C**

**Explanation:** Step 1: add the ratio parts: 1 + 3 + 5 = 9 parts. Step 2: find the size of one part: 45 ÷ 9 = 5 findings per part. Step 3: majors are 3 parts: 3 × 5 = 15. As a check, criticals are 1 × 5 = 5 and minors are 5 × 5 = 25, and 5 + 15 + 25 = 45, which matches the total. The distractors are the other categories' counts — a reminder to re-read which quantity the question asks for before answering. Ratio splits like this appear constantly in your work: triaging audit findings by severity, splitting a performance budget across HTML, CSS and JavaScript, or dividing review capacity across teams. The three-step method — total the parts, size one part, scale — handles them all.

**Question 4 (moderate) — Percentage points versus percentages**

Your form's client-side error rate falls from 4.0% of submissions to 3.0% after you improve the field hint text. Which statement describes the improvement accurately?

- A) A 1% reduction in the error rate
- B) A 25% reduction in the error rate, equal to 1 percentage point
- C) A 33% reduction in the error rate
- D) A 1 percentage point reduction, equal to a 10% relative reduction

**Correct answer: B**

**Explanation:** Two different measures are in play and the question tests whether you keep them apart. Step 1: the absolute change is 4.0 − 3.0 = 1.0 percentage point. Step 2: the relative change is the absolute change divided by the starting rate: 1.0 ÷ 4.0 = 0.25 = 25%. So the error rate fell by one percentage point, which is a 25% relative reduction. Option A uses "%" for a percentage-point change, which is exactly the ambiguity that misleads stakeholders; option C computes 1 ÷ 3 against the final rate; option D invents a 10% figure. When you communicate results — a named part of your **Communicating information** skill — saying "we cut errors by a quarter" and "errors fell one percentage point" are both true and both clearer than "errors fell 1%", which is technically wrong and rhetorically weak. Seniors are expected to catch this distinction in others' reports as well as their own.

**Question 5 (moderate) — Weighted average Lighthouse score**

Three services in your programme have Lighthouse performance scores of 80, 60 and 90. They receive 60%, 30% and 10% of the programme's traffic respectively. What is the traffic-weighted average performance score experienced across the programme?

- A) 75
- B) 76.7
- C) 77
- D) 80

**Correct answer: A**

**Explanation:** Step 1: multiply each score by its traffic share: 80 × 0.60 = 48; 60 × 0.30 = 18; 90 × 0.10 = 9. Step 2: sum the weighted contributions: 48 + 18 + 9 = 75. The distractor 76.7 is the unweighted mean (80 + 60 + 90 = 230; 230 ÷ 3 ≈ 76.7), which overstates the typical experience because the best-scoring service carries the least traffic. This is precisely why weighting matters when you make decisions based on research: if you had one quarter of improvement capacity, the weighted view points you at the 60-score service with 30% of traffic, whereas the unweighted view makes the programme look healthier than most users find it. Whenever services, pages or device classes differ in volume, weight before you average — and when you guide others on monitoring, make sure the dashboards they build do the same.

**Question 6 (moderate) — Image optimisation savings**

A page weighs 3.2 MB, of which 75% is images. You convert the images to a modern format, reducing total image weight by 40%. What is the new total page weight?

- A) 1.92 MB
- B) 2.24 MB
- C) 2.40 MB
- D) 2.72 MB

**Correct answer: B**

**Explanation:** Step 1: find the image weight: 3.2 × 0.75 = 2.4 MB. Step 2: find the saving: 2.4 × 0.40 = 0.96 MB. Step 3: subtract the saving from the original total: 3.2 − 0.96 = 2.24 MB. The distractor 1.92 MB applies the 40% cut to the whole page rather than just the images (3.2 × 0.60 = 1.92); 2.72 MB applies a 40% cut to the non-image weight instead; 2.40 MB is simply the image weight, left over from step 1. Multi-step percentage problems are where most marks are lost, and the defence is labelling each intermediate result as you go — "images 2.4, saving 0.96, new total 2.24" — rather than chaining operations in your head. This mirrors your real optimisation workflow: you estimate savings per asset class before doing the work, so you can tell a stakeholder what an afternoon of image work will buy compared with, say, a script audit.

**Question 7 (moderate) — Reading a sprint quality table**

Your team's last four sprints show:

| Sprint | Story points completed | Defects raised |
|---|---|---|
| 21 | 40 | 6 |
| 22 | 30 | 6 |
| 23 | 50 | 8 |
| 24 | 25 | 6 |

Measured as defects per 10 story points, which sprint had the worst quality rate?

- A) Sprint 21
- B) Sprint 22
- C) Sprint 23
- D) Sprint 24

**Correct answer: D**

**Explanation:** Compute the rate for each sprint. Sprint 21: 6 ÷ 40 = 0.15 defects per point, or 1.5 per 10 points. Sprint 22: 6 ÷ 30 = 0.20, or 2.0 per 10 points. Sprint 23: 8 ÷ 50 = 0.16, or 1.6 per 10 points. Sprint 24: 6 ÷ 25 = 0.24, or 2.4 per 10 points. The worst rate is sprint 24. The trap is answering sprint 23 because it has the highest raw defect count — but it also delivered the most work, and quality comparisons need a rate, not a count. This is exactly the arithmetic behind Agile health checks in your **Community collaboration** skill: a team that "raised more defects" may simply have delivered more, while a small sprint with the same defect count is the real signal. Normalising before comparing is what turns a retrospective from blame into insight — and note that sprints 22 and 24 both hint that smaller sprints are going worse, which is a pattern worth a conversation.

**Question 8 (moderate) — Compound growth in traffic**

A service you support receives 200,000 visits in January. Traffic grows 20% in February and then a further 25% in March (each increase applying to the previous month). What is the March traffic, and what is the overall percentage growth from January to March?

- A) 290,000 visits; 45% growth
- B) 300,000 visits; 50% growth
- C) 300,000 visits; 45% growth
- D) 290,000 visits; 50% growth

**Correct answer: B**

**Explanation:** Step 1: February = 200,000 × 1.20 = 240,000. Step 2: March = 240,000 × 1.25 = 300,000. Step 3: overall growth = (300,000 − 200,000) ÷ 200,000 = 0.50 = 50%. Alternatively multiply the growth factors: 1.20 × 1.25 = 1.50, a 50% overall rise — the factor method is faster and less error-prone, and worth adopting as your default. The 45% distractors come from adding the percentages (20 + 25), which is wrong whenever the second change applies to an already-changed base; the 290,000 figures follow from that same error. Compound change matters in your work in both directions: two successive "small" regressions of 20% and 25% in a performance metric compound to 50%, which is why performance budgets are checked per change rather than per quarter — a point worth making, with this arithmetic, when you guide teams on monitoring.

**Question 9 (challenging) — Uptime and error budget**

Your service has a 99.9% monthly availability target. Assume a 30-day month. The service has already been down for 30 minutes this month. How many more minutes of downtime can it sustain before breaching the target?

- A) 13.2 minutes
- B) 43.2 minutes
- C) 3.2 minutes
- D) 30 minutes

**Correct answer: A**

**Explanation:** Step 1: total minutes in a 30-day month: 30 × 24 × 60 = 43,200 minutes. Step 2: the allowed downtime is 0.1% of that (100% − 99.9%): 43,200 × 0.001 = 43.2 minutes. Step 3: subtract the downtime already used: 43.2 − 30 = 13.2 minutes remaining. The distractor 43.2 is the full budget with the subtraction forgotten; 3.2 comes from a slip in step 3; 30 anchors on the downtime already consumed. This "error budget" framing — a fixed allowance you spend down — is the standard way availability targets are managed, and it applies to frontend concerns directly: when you co-ordinate integration and take responsibility for the tests around the user interface, a flaky deployment that takes the service down for ten minutes has spent a quarter of a 99.9% monthly budget. Being able to do this sum in a meeting, from memory of the 43.2-minute figure, is a genuinely useful senior party trick.

**Question 10 (challenging) — Valuing a performance improvement**

Your service receives 100,000 sessions per month, and 62% of sessions currently complete the main transaction. Research from a comparable service suggests that making the page one second faster increases completion by 3 percentage points. If that holds, how many additional completed transactions per month would the speed improvement generate?

- A) 1,860
- B) 3,000
- C) 6,200
- D) 65,000

**Correct answer: B**

**Explanation:** Step 1: the new completion rate would be 62% + 3 percentage points = 65%. Step 2: current completions: 100,000 × 0.62 = 62,000. Step 3: projected completions: 100,000 × 0.65 = 65,000. Step 4: the difference: 65,000 − 62,000 = 3,000 additional completions. A faster route: 3 percentage points of 100,000 sessions is 3,000 directly. The distractor 1,860 treats the 3-point uplift as a 3% relative increase on 62,000 (62,000 × 0.03 = 1,860) — percentage points versus percentages again, now with money-shaped consequences; 65,000 is the new total rather than the increase; 6,200 is 10% of sessions, a plausible-looking but meaningless number. This is the arithmetic of a business case: when you champion performance work to a stakeholder, "3,000 more completed transactions a month" is language that wins a place in the sprint, and your **Strategic thinking** skill — evaluating whether strategies meet business requirements — expects you to translate technical improvements into exactly these terms.

**Question 11 (challenging) — Reverse percentage on a bundle budget**

After a 15% reduction, your CSS bundle now weighs 391 KB. What did it weigh before the reduction?

- A) 449.65 KB
- B) 455 KB
- C) 460 KB
- D) 470 KB

**Correct answer: C**

**Explanation:** The reduced size is 85% of the original (100% − 15%). Step 1: set up the relationship: original × 0.85 = 391. Step 2: solve: original = 391 ÷ 0.85 = 460 KB. Step 3: check by going forwards: 460 × 0.15 = 69; 460 − 69 = 391, which matches. The distractor 449.65 comes from the classic reverse-percentage error of adding 15% to the reduced figure (391 × 1.15 = 449.65) — wrong because the 15% was taken from the larger original, not from the smaller result. Reverse percentages appear whenever you know an "after" and a rate but need the "before": reconstructing a pre-regression metric from a dashboard that only kept the bad week, or working out what a page weighed before a compression change from the saving percentage in the release notes. The forwards check in step 3 takes ten seconds and catches nearly every error of this type — make it a habit in tests and in code review alike.

**Question 12 (challenging) — Comparing A/B test results**

An A/B test on a start-page redesign shows: variant A, 4,800 completions from 60,000 sessions; variant B, 4,620 completions from 55,000 sessions. Which variant has the higher completion rate, and what is the difference in percentage points?

- A) Variant A, by 0.4 percentage points
- B) Variant B, by 0.4 percentage points
- C) Variant A, by 4.0 percentage points
- D) They are exactly equal

**Correct answer: B**

**Explanation:** Step 1: variant A's rate: 4,800 ÷ 60,000 = 0.08 = 8.0%. Step 2: variant B's rate: 4,620 ÷ 55,000 = 0.084 = 8.4%. Step 3: the difference: 8.4 − 8.0 = 0.4 percentage points, in variant B's favour. The trap is comparing raw counts: variant A has more completions (4,800 versus 4,620), but it also had more sessions, and rates are what make unequal groups comparable — the same normalisation principle as the defect-rate question, now applied to research data. Option C's 4.0 points comes from misplacing a decimal, which a sanity check catches (both rates are near 8%, so their gap cannot be 4 points). In practice, before acting on a 0.4-point difference you would also ask whether the sample is large enough for the gap to be reliable — with tens of thousands of sessions per arm it likely is, but asking the question is part of making decisions based on research rather than on whichever number is nearest. Champion that habit when you review research findings with your team.

### Preparation tips

- **Rebuild fluency with the core four.** Percentage change, reverse percentage, weighted average and rate-per-unit cover most workplace numeric tests. Ten minutes a day for a week with a calculator and made-up bundle sizes will restore speed you last used in an exam hall.
- **Always ask "percentage of what?"** Before dividing, name the base out loud. Most percentage errors are base errors, and the discipline costs two seconds.
- **Use growth factors for chained changes.** Convert +20% to ×1.2 and −15% to ×0.85, then multiply. It is faster than stepwise addition and immune to the add-the-percentages trap.
- **Check forwards after solving backwards.** Every reverse-percentage answer can be verified in one multiplication. Do it every time.
- **Practise on your own dashboards.** Take this week's real performance or analytics data and compute a weighted average, a rate and a month-on-month change. Test questions will feel like Tuesday.
- **Keep units and labels on intermediate results.** Writing "images: 2.4 MB" instead of "2.4" prevents the most common multi-step slips under time pressure.

### Common pitfalls to avoid

- **Comparing counts when the groups differ in size.** Defects, completions, errors: if the denominators differ, compute rates first. Every table-based question is checking whether you will.
- **Confusing percentage points with percentages.** A fall from 4% to 3% is one point and 25% at once. State both when you communicate, and read carefully which one a question asks for.
- **Adding successive percentage changes.** Sequential changes multiply. 20% then 25% is 50%, never 45%.
- **Dividing by the new value in percentage change.** Change is measured against the original. The wrong base usually appears among the answer options, waiting.
- **Ignoring the sanity check.** Means must lie inside the data's range; two rates near 8% cannot differ by 4 points; a part cannot exceed its whole. Five seconds of plausibility checking catches more errors than five minutes of rework.
- **Rushing table questions.** Most table errors are reading errors — wrong row, wrong column — not arithmetic errors. Put your finger (or cursor) on the cell before you compute.

<!-- APPEND -->
