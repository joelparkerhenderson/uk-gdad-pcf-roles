# Junior Interaction Designer - Psychometric Assessment Resources

## Introduction

Welcome. This guide is written for you as a junior interaction designer in the UK Government Digital and Data profession — someone who explains design decisions, works collaboratively, has responsibility as part of a service, works independently after being given direction by more senior designers, and independently identifies user issues and important needs. That mix of independence and direction shapes everything that follows.

You might be preparing for a formal assessment, thinking about your next step, or simply curious how psychometric tests connect to the design work you do each week. All good reasons. Let us start by demystifying the assessments. They are not intelligence tests, they do not measure your worth, and they are not designed to catch you out. They are standardised exercises that sample the everyday thinking a job actually uses. In your case that means analysing evidence about a screen and explaining what it shows, working out whether a control excludes somebody, reading a specification and applying it correctly, interpreting analytics well enough to know where to look, and making sensible calls when a design decision has to be made before anyone senior is available.

Your role level raises the bar in three specific ways compared with a trainee, and the questions reflect them. You analyse and synthesise evidence yourself rather than only reading someone else's findings, so you will be asked to judge what evidence supports rather than merely spot patterns in it. You prototype at different fidelities and iterate across successive rounds of research, so there are questions about method choice and about what an iteration can and cannot establish. And you have responsibility as part of a service, so the prioritisation and judgement items assume you will act rather than only observe.

There is one thing worth naming about interaction design specifically. Your discipline works at two scales simultaneously — the flow, meaning what order things happen in and what happens when they go wrong, and the element, meaning the label, the control, the error, the focus behaviour. A great deal of skill consists of moving between those scales and noticing when a decision at one breaks something at the other. Splitting a page improves the flow and doubles the number of times a user must wait for a page to load. Making a control cleverer improves the element and breaks it for anyone not using a mouse. A surprising amount of what these assessments measure is that habit of checking both.

The document is organised into four main sections:

1. A workplace job-specific cognitive assessment — pattern recognition, logical deduction, error checking, prioritisation and applied problem solving, using components, flows, specifications and research evidence.
2. A numeric reasoning assessment — percentages, error rates, device comparisons, funnel data, averages and ratios, with an emphasis on interpreting figures rather than only calculating them.
3. A verbal reasoning assessment — reading design standards, accessibility criteria, review reports and stakeholder correspondence, then answering true/false/cannot-say and comprehension questions.
4. A situational judgement assessment — realistic dilemmas at your level of independence, with guidance on the most and least effective responses and on why.

Each section follows the same shape: what the assessment measures, how it maps to the named skills in your role, twelve practice questions with full explanations, preparation tips, and common pitfalls.

To get the most from this, commit to an answer before reading the explanation. An answer you have written down teaches you something; one you merely considered does not. Read the explanations even when you were right, because the reasoning transfers further than the answer. And pay attention where you were confident and wrong, because that is where a habit is hiding.

Let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive assessment measures the reasoning your role genuinely uses, presented through practical materials rather than abstract shapes. You will work with what a junior interaction designer actually handles: components and their specifications, a flow with branches, a set of error messages, analytics for a page, research observations, an extract from a design standard.

The format is normally an online test of fifteen to thirty minutes covering pattern recognition, logical deduction, error checking, prioritisation and applied problem solving. Scoring is objective against a norm group at a comparable level. Many platforms are adaptive, raising difficulty after correct answers, so a test that feels hard is usually one you are doing well on. Most employers receive an acuity report showing speed against accuracy, which rewards careful work.

For a junior interaction designer this section is closer to your daily work than it may appear, because the core of the craft is disciplined noticing at two scales. You notice that a page uses a pattern in a way the pattern was not built for. You notice that splitting a question across two pages doubles the number of times someone on a slow connection has to wait. You notice that a validation rule rejects a format most people type. You notice that the focus order jumps over the error summary. You notice that two screens in the same service handle the same choice differently. Each is an act of comparison, deduction or error detection.

What rises at your level, compared with a trainee's, is the expectation that you judge as well as notice. Several questions ask you to decide how strongly a finding can be stated, choose between reasonable approaches, or identify which of two plausible explanations the evidence supports. There is nothing to memorise — every rule and figure appears in the question — but you will need judgement rather than only rule-application.

A practical note about the options. Wrong answers are built from specific, predictable errors: counting mentions rather than people, stopping at the first rule breach, ignoring an exception clause, comparing raw counts across unequal groups, ranking by seniority rather than consequence. Learning the shape of those errors is most of the preparation.

### How this assessment maps to your role

The cognitive dimensions map onto the skills named in your role summary:

- **Pattern recognition** maps to **Evidence-based design**, where you analyse, synthesise and clearly explain evidence relevant to users or a service, such as web analytics data.
- **Logical deduction** maps to **Design communication**, where you clearly explain design decisions using appropriate tools and methods. A decision explained on an overreaching claim does not survive its first challenge.
- **Error checking** maps to **Designing for everyone**, where you ensure a design meets appropriate standards such as accessibility regulations, with support.
- **Prioritisation** maps to **Iterative design**, where you apply iterative design principles and agile methodologies to your work.
- **Applied problem solving** maps to **Iterative design** again, where you prototype at different fidelities and use and iterate design patterns and components.
- **Moving between flow and element** maps to **Designing strategically**, where you describe how your design work aligns to the wider goals and vision of your team.

### Practice questions

**Question 1 (easy) — Error checking a set of pages**

Your team's question page rules require each page to: ask one thing, use a question as the label, include a back link, have one primary action, and show errors both in a summary at the top and next to the field. You review three pages:

| Page | Things asked | Label | Back link | Primary actions | Error display |
|---|---|---|---|---|---|
| 1 | 1 | Question | Yes | 1 | Summary and inline |
| 2 | 1 | Statement | Yes | 1 | Inline only |
| 3 | 2 | Question | No | 1 | Summary and inline |

How many rule breaches are there in total?

- A) 2
- B) 3
- C) 4
- D) 5

**Correct answer: C**

**Explanation:** Count breaches, not pages, because the question asks for a total. Page 1 is compliant. Page 2 breaks two rules: a statement label, and inline-only errors. Page 3 breaks two: it asks two things, and it has no back link. Two plus two is four, giving C. Option A is the number of non-compliant pages, which is the classic confusion in this question type. Note which breaches are most consequential — inline-only errors on page 2 means a screen reader user may never encounter the message at all, which is a different order of problem from a statement label. Counting correctly is the first step; weighting by consequence is what makes the count useful when you hand it to a developer with limited time.

**Question 2 (easy) — Deduction from a component rule**

Your standard states: "A component may be used in a live service only if it is in the Design System, unless it has been reviewed and approved by the lead interaction designer." A developer says: "We shipped a component last sprint that is not in the Design System." Which must be true?

- A) The standard was breached.
- B) The component was reviewed and approved by the lead.
- C) Either the component was reviewed and approved, or the standard was breached.
- D) The component is inaccessible.

**Correct answer: C**

**Explanation:** A conditional with a stated exception, plus facts silent on the exception, licenses only the disjunction. Options A and B each assume a branch without evidence. Option D imports a quality judgement the question does not support — components outside the Design System are sometimes necessary and sometimes excellent. Only C holds in every case. This structure recurs constantly and is worth recognising instantly. It also has a workplace parallel that matters at your level, where you have responsibility as part of a service and may be the person asking: framing it as "which route did this go through?" rather than "this breaks the standard" gets you an answer instead of a defence.

**Question 3 (moderate) — Reconciling two evidence sources**

Research with ten participants found that seven could not tell which of two buttons was the primary action. Analytics show only 2% of users click the secondary button. What is the strongest interpretation?

- A) The research is unrepresentative; the analytics show almost nobody has a problem.
- B) The two measure different things — analytics record which button was eventually clicked, not how long it took or how confident the user was — so both can be true: most people work it out, and most people have to work it out, which is a cost in time and confidence that analytics cannot see.
- C) The sources contradict each other and cannot be reconciled.
- D) The secondary button should be removed.

**Correct answer: B**

**Explanation:** The apparent contradiction dissolves once you name what each source measures. Analytics record an outcome — the click — while the research observed the process of arriving at it. A user who hesitates, reads both labels twice and then clicks correctly produces a perfectly clean analytics record and a poor experience. That is precisely the kind of cost interaction design exists to notice, and it accumulates: hesitation on every page of a fifteen-page journey is a service that feels exhausting for reasons no dashboard reports. Option A privileges scale over relevance. Option C gives up on an available reconciliation. Option D leaps to a solution before the diagnosis; the problem may be visual weight rather than the button's existence.

**Question 4 (moderate) — Prioritising a sprint**

You have capacity for one substantial piece of design work this sprint:

1. A new page goes into build in four days and nothing has been designed.
2. A live page has a 30% validation error rate on one field, unchanged for months.
3. A colleague wants help exploring a concept for next quarter.
4. The team wants to revisit a screen you designed six weeks ago after minor copy changes.

Which should you prioritise?

- A) Item 2, because it affects the most users.
- B) Item 1, because it is the only one where design work can still change what gets built inside the window, while item 2 remains valuable but is not time-boxed in the same way.
- C) Item 3, because early exploration has the highest leverage.
- D) Item 4, because unverified changes are a risk.

**Correct answer: B**

**Explanation:** The deciding factor in agile prioritisation is not importance in the abstract but whether work can still change a decision. Item 1 has a hard four-day window: design done now shapes what gets built, and design done afterwards becomes a critique of something already made. Item 2 matters and has persisted for months, so deferring it costs comparatively little — though it is worth noting that a 30% error rate on a single field is a serious problem and should be next. Item 3 has no deadline pressure. Item 4 is weakest, since minor copy changes rarely justify revisiting a screen. Option A ranks by scale rather than timing, the most common error in this question type and the one that leaves teams perpetually analysing problems they cannot yet act on.

**Question 5 (moderate) — Choosing a fidelity**

Your team needs to know whether users understand a new way of expressing a date range before committing to build. You have one week. Which approach fits best?

- A) A high-fidelity interactive prototype of the whole journey.
- B) A low-fidelity prototype of just the date range question, in two or three variants, because the question is about comprehension of an expression rather than about interaction detail — and low fidelity can be changed between sessions, letting you test several wordings in a week.
- C) A written description read to participants.
- D) A live A/B test of two versions.

**Correct answer: B**

**Explanation:** Match fidelity to the question. You need to know whether people understand an expression, which does not require working interactions, real data or polished visuals — and high fidelity actively works against you, because participants respond to the polish, comment on styling, and are more reluctant to criticise something that looks finished. Low fidelity is faster, cheaper and, crucially, changeable between sessions, so you can test three wordings rather than one. Option A spends most of the week building. Option C removes the visual presentation, which for a date range is a large part of the meaning — "from" and "to" fields side by side read differently from a single line. Option D cannot run without a build and would tell you which performed better without telling you why. Your role names prototyping at different fidelities to explore and test designs, and this judgement is the skill itself.

**Question 6 (moderate) — Strength of a finding**

Eight of twelve participants did not notice a "save and come back later" link. Which conclusion is best supported?

- A) 67% of users do not notice the link.
- B) The link's discoverability is a substantial problem, evidenced across most participants, warranting design work and a follow-up check on whether the change helps.
- C) The link should be moved to the top of the page.
- D) The link is invisible.

**Correct answer: B**

**Explanation:** Eight of twelve is a strong qualitative signal, strong enough to act on, and B states it at that strength while specifying what acting looks like. Option A converts twelve participants into a population rate, the commonest overreach in design reporting and the one most likely to be quoted back at you in a meeting you are not in. Option C prescribes one solution when the cause could be position, wording, visual weight, or a mental model in which people do not expect to be able to leave — and each implies a different fix. Option D overstates: participants did not notice the link, which is different from the link being invisible. Note that B builds in the follow-up check, which is what makes it iterative design rather than a one-off change.

**Question 7 (moderate) — Flow versus element**

A designer proposes splitting a page that currently asks for name, date of birth and national insurance number into three separate pages, following the one-thing-per-page pattern. The service is used heavily by people on slow mobile connections in areas with poor coverage. What is the strongest analysis?

- A) Split it; one thing per page is the pattern.
- B) Splitting generally helps comprehension and error recovery, but it triples the number of page loads for this section, which is a real cost on a poor connection — so the strongest move is to split it and check what the added page weight and load time actually are, rather than treating either the pattern or the connection concern as automatically decisive.
- C) Do not split it; the connection issue outweighs the pattern.
- D) Split it but combine name and date of birth.

**Correct answer: B**

**Explanation:** This is the flow-versus-element trade-off in its most common form. One thing per page is a well-evidenced pattern with a real basis: shorter pages are easier to understand, errors are easier to locate, and going back costs less. But every page is a round trip, and on a poor connection three round trips instead of one is a meaningful cost that pattern guidance does not weigh for you. Option B holds both truths and — this is what makes it the strongest — turns the disagreement into something measurable rather than a contest of principles. Often the added weight is trivial and the concern evaporates; occasionally it is not. Option A applies the pattern without checking it against the situation. Option C treats a real concern as decisive without measuring it. Option D picks an arbitrary middle without a reason.

**Question 8 (moderate) — Reading analytics to focus design work**

A journey shows: 24,000 users start, 20,400 pass eligibility, 12,240 reach the declaration, 11,628 submit. Where should design attention go first?

- A) The start, because 3,600 users are lost there.
- B) Between eligibility and the declaration, because 8,160 users are lost there — more than twice any other step.
- C) Submission, because it is closest to the outcome.
- D) All steps equally.

**Correct answer: B**

**Explanation:** Calculate each loss before choosing. Start to eligibility loses 3,600. Eligibility to declaration loses 20,400 − 12,240 = 8,160. Declaration to submission loses 612. The middle stretch is losing more than twice as many users as anywhere else, so it goes first. Expressing these as rates is often more informative: that stretch loses 40% of those who reach it, against 15% at the first step and 5% at submission. Option A identifies a real but smaller loss. Option C mistakes proximity to the outcome for size of problem. Option D sounds even-handed and is not a plan. This is a good example of quantitative data setting the agenda for design work: the analytics tell you where to look, and only research or a careful walkthrough will tell you why.

**Question 9 (harder) — Distinguishing signal from artefact**

Six participants tested a new form. The four who completed easily all used a desktop computer; the two who struggled both used a phone. A colleague concludes the form works on desktop and fails on mobile. What is the most rigorous response?

- A) Agree; the split is consistent.
- B) Note that device is a plausible explanation but rests on two phone users, who may differ in other relevant ways — digital confidence, whether they had documents to hand, whether they were at home — so it is a hypothesis to test rather than a finding, and the obvious next step is to recruit more phone users.
- C) Reject it; two participants show nothing.
- D) Recommend removing mobile access until the form is fixed.

**Correct answer: B**

**Explanation:** A perfect split like this should prompt investigation, and two phone users is a very thin base for a conclusion. Both are true, and holding them together is rigour. The two groups may also differ in ways that travel with device: people on a phone may be applying away from home, without documents, or may simply be less digitally confident, any of which could be doing the work that device appears to be doing. Option B says this and names the cheap next step. Option A promotes a hypothesis into a finding. Option C dismisses a genuine signal — small numbers justify caution, not blindness. Option D proposes a drastic action on thin evidence, and would remove access from users who may have no alternative.

**Question 10 (harder) — A component's second-order cost**

A designer proposes replacing a set of eight radio buttons with a searchable dropdown, arguing it takes less vertical space. What is the strongest analysis?

- A) Agree; vertical space matters on mobile.
- B) A searchable dropdown is a custom component that must work with keyboard alone, with screen readers, with voice input and at high zoom, and must be maintained; eight options gain almost nothing from search, and radio buttons let users see all options at once, which matters when they do not yet know what they are looking for — so the change adds accessibility risk and maintenance cost for a marginal space saving.
- C) It is fine if it is tested with screen reader users.
- D) Radio buttons should always be used for eight options or fewer.

**Correct answer: B**

**Explanation:** Search earns its complexity when a list is long enough that scanning is genuinely burdensome — hundreds of countries, for instance. With eight options everything is visible and search saves nobody meaningful effort, while a custom component must be built and maintained to work with keyboard navigation, assistive technology, voice control and zoom, any of which can break in ways that are hard to detect and easy to ship. Option B also names the less obvious cost: a dropdown hides options, which is fine when the user knows their answer and actively harmful when they are choosing between things they need to read. Option A weighs pixels against usability. Option C treats testing as a substitute for the design decision, and testing a complex custom control is expensive and does not remove maintenance burden. Option D states a rule without reasoning and would be wrong for a list of two hundred.

**Question 11 (harder) — Reconciling contradictory evidence**

A satisfaction survey of 1,500 users reports 79% positive. Your twelve sessions found substantial frustration, with nine participants describing significant difficulty. The contact centre reports the service as its third-highest call driver. How should you synthesise this?

- A) Trust the survey; 1,500 responses outweigh twelve sessions.
- B) The sources measure different populations and constructs: satisfaction surveys are typically served at the end of a journey, so people who abandoned rarely see them, and they often ask about outcome rather than process — while contact centre volume is behavioural evidence at scale corroborating the sessions. The picture is a service most people complete, many find hard, and a substantial minority need help with.
- C) The sources conflict irreconcilably.
- D) The service is performing well with minor issues.

**Correct answer: B**

**Explanation:** The conflict dissolves once you note who each source sees and what it measures. Completion-time satisfaction surveys reach only people who got to the end, and asking whether someone got what they needed is different from asking whether it was hard. Your sessions observed the process. The contact centre data is the pivot and the most useful element: high call volume is behavioural evidence, at scale, that people cannot complete unaided, and it corroborates your qualitative findings using exactly the kind of data sceptical colleagues find credible. Option A defers to scale over relevance. Option C abandons an available reconciliation. Option D is the comfortable reading and ignores the contact centre, which is the most telling figure in the set.

**Question 12 (harder) — A flaw in your own work**

You realise a flow diagram you shared a fortnight ago, which the team has been building from, omits the branch where a user answers "no" at the eligibility question. What is the strongest response?

- A) Update it and mention it at stand-up.
- B) Tell the team immediately, explain exactly what was missing, flag which stories may have been built without the branch, and note that an unhandled "no" path is likely a live defect rather than only a documentation gap.
- C) Update it quietly.
- D) Raise it in the retrospective.

**Correct answer: B**

**Explanation:** A fortnight of building against an incomplete diagram means the correction alone is insufficient — the important element is flagging the stories that may have been built without the branch, which is the part people skip because it is uncomfortable. Option B also does something distinctively interaction-design-shaped: it recognises that a missing branch in a flow is not merely an omission in a document but almost certainly an unhandled path in the built service, where a user who answers "no" reaches a dead end or an error. That is a defect with a user on the other side of it, and it needs finding today. Option C leaves both the documentation and the likely defect unexamined. Option A treats it as housekeeping. Option D defers to a meeting when the information is needed now.

### Preparation tips

- **Practise on your own service.** Check a real page against the rules it should follow; you exercise the tested skill and improve the page.
- **Ask what each source measures.** When analytics and research seem to disagree, the reconciliation is usually in the definitions.
- **Rehearse the strength-of-claim ladder.** Observation, pattern, supported finding, measured rate — and what each licenses.
- **Match fidelity to question.** Comprehension needs low fidelity; interaction detail needs higher; rates need analytics.
- **Check both scales.** Ask of any change: what does this do to the flow, and what does it do to the element?
- **Calculate every step's loss before choosing where to look.** The biggest gap is rarely the one people talk about.
- **Decide what you are counting.** Pages, breaches, participants, mentions — the question always specifies one.

### Common pitfalls to avoid

- **Converting participants into percentages.** "Eight of twelve participants" must never become "67% of users".
- **Declaring a winner between data sources.** A contradiction is usually a category error.
- **Treating a striking split as a finding.** Four versus two across six participants is a hypothesis.
- **Applying a pattern without checking the situation.** One thing per page is well evidenced and not free.
- **Prescribing the fix instead of establishing the problem.** It forecloses better options.
- **Ranking by scale rather than by timing.** Work that cannot change a decision has less value now.
- **Adding a custom component for a marginal gain.** Every one is an accessibility and maintenance liability.
- **Treating a missing branch as a documentation gap.** It is usually a live defect.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A numeric reasoning assessment measures how accurately you handle the numbers your job produces. It is not a maths exam. There are no equations and no formulae to memorise. Most platforms provide a calculator, and where they do not the arithmetic is deliberately simple. What is measured is whether you can read a table correctly, identify which figures matter, choose the right operation, and interpret the result without overstating it.

The format is typically a timed online test of fifteen to thirty minutes, each item presenting a small table, chart or paragraph of figures followed by a multiple-choice question. Time per item is tight, so the operative skill is locating the relevant numbers quickly and disregarding the deliberately irrelevant ones.

Your role names analysing, synthesising and clearly explaining evidence relevant to users or a service, and specifically mentions web analytics data. That makes this section directly job-relevant. A junior interaction designer reads error rates to find the field that is failing, compares device performance to spot exclusion, reads drop-off to decide which page to look at, checks whether an iteration made any difference, and translates all of it into something a team can act on.

What rises at your level is interpretation. Several items below have a correct calculation attached to a wrong conclusion, and telling them apart is the test. A designer who can compute a percentage but cannot say whether it means anything is not much use in a prioritisation meeting; a designer who can say "that rate is measured against the wrong group, so it overstates the problem" is genuinely valuable.

Four habits carry the load. Work out what the question asks before looking at the data. Identify the denominator before calculating. Estimate, calculate, compare. And sanity-check against the world.

One warning about the options. Distractors are constructed from specific errors: dividing by the wrong total, confusing a percentage with a percentage point, using the new value as the base in a percentage change. Finding your answer among the options is not evidence that you are right.

### How this assessment maps to your role

The numerical skills tested map onto your named skills:

- **Reading analytics accurately** maps to **Evidence-based design**, where you analyse and clearly explain evidence such as web analytics data.
- **Comparing rates between devices and groups** maps to **Designing for everyone**, where a gap is often the first numerical trace of exclusion.
- **Measuring whether an iteration worked** maps to **Iterative design**, where you iterate and improve a design based on successive rounds of research.
- **Understanding scale** maps to **Designing strategically**, where aligning to your team's goals means knowing how many people a decision affects.
- **Explaining figures honestly** maps to **Design communication**, where you clearly explain design decisions.
- **Working with analysts** maps to **Evidence-based design**, where you use evidence to inform, develop and test a design idea.

### Practice questions

**Question 1 (easy) — Error rate on a field**

Of 3,200 users who reached a page, 800 triggered a validation error on one field. What percentage triggered it?

- A) 20%
- B) 25%
- C) 30%
- D) 40%

**Correct answer: B**

**Explanation:** 800 ÷ 3,200 = 0.25, so 25%, and the answer is B. Estimate first: 800 of 3,200 is a quarter, since 1,600 would be half. Options A and C come from dividing by 4,000 and 2,667. Note how you would report it: a quarter of everyone reaching the page failing one field is substantial, and it almost always points at a format, label or hint problem rather than at users — people do not collectively become careless at one specific input.

**Question 2 (easy) — Drop-off measured correctly**

A page is reached by 4,500 users and passed by 3,600. What is the drop-off rate at that page?

- A) 20%
- B) 25%
- C) 80%
- D) 30%

**Correct answer: A**

**Explanation:** The drop-off is 4,500 − 3,600 = 900, measured against those who reached the page: 900 ÷ 4,500 = 0.2, or 20%, giving A. Option B is 900 ÷ 3,600, dividing by those who continued — the most common error in page analytics, and one that overstates every drop-off it touches. The rule: drop-off is measured against arrivals. This matters most when comparing pages, because two pages computed with different denominators produce a ranking of where to focus that can be simply wrong, and at your level you may be the person producing that ranking.

**Question 3 (easy) — Device comparison**

| Device | Users | Completed |
|---|---|---|
| Desktop | 7,000 | 5,950 |
| Mobile | 10,000 | 6,000 |
| Tablet | 1,000 | 850 |

Which device has the lowest completion rate, and how many users does it lose?

- A) Mobile, 60% rate, 4,000 users lost
- B) Desktop, 85% rate, 1,050 users lost
- C) Mobile, 40% rate, 6,000 users lost
- D) Tablet, 85% rate, 150 users lost

**Correct answer: A**

**Explanation:** Rates are: desktop 5,950 ÷ 7,000 = 85%; mobile 6,000 ÷ 10,000 = 60%; tablet 850 ÷ 1,000 = 85%. Mobile is lowest and loses 10,000 − 6,000 = 4,000 users. So A. Option C inverts the rate and the loss. Note what the table tells you as a designer: desktop and tablet perform identically at 85%, which strongly suggests the problem is specific to small screens rather than to the content or the task — tablets have the same content and a large screen, and they behave like desktops. That is the kind of inference a table supports and a single overall figure would hide entirely.

**Question 4 (easy) — Average and its limits**

Six participants took 20, 25, 30, 30, 35 and 140 seconds to complete a step. What is the mean, and is it a good summary?

- A) 30 seconds; yes
- B) 47 seconds; yes
- C) 47 seconds; no, because one extreme value pulls it above five of the six observations
- D) 30 seconds; no

**Correct answer: C**

**Explanation:** The values sum to 280, and 280 ÷ 6 = 46.67, so about 47 seconds. But five of the six participants finished within 35 seconds, so the mean describes nobody: it sits above every observation except the outlier. The median, the average of the third and fourth values, is 30 seconds and represents the group well. Option C states both the arithmetic and the interpretation. Option B gets the number and misses the point, which is exactly the failure mode this item is testing. The 140-second session is the most interesting thing in the data — something on that step defeated one person entirely — and the right report gives the median, the range, and a description of the outlier.

**Question 5 (moderate) — Did the iteration work?**

Before a change to hint text, 960 of 1,600 users completed a field without error. After, 1,320 of 2,000 completed without error. Did it improve, and by how much in percentage points?

- A) Yes, by 360 users
- B) Yes, by 6 percentage points
- C) Yes, by 10 percentage points
- D) No, the rate fell

**Correct answer: B**

**Explanation:** Convert to rates, because the totals differ. Before: 960 ÷ 1,600 = 60%. After: 1,320 ÷ 2,000 = 66%. The improvement is 6 percentage points, giving B. Option A compares raw counts across different-sized groups, which is meaningless here — more users completed partly because more users arrived, and crediting the design with the whole increase would be wrong. This is exactly the comparison your role requires when iterating across successive rounds, and the trap is common in real reporting: "360 more people got it right" sounds like a win and could conceal a fall in the rate if traffic rose faster than successes.

**Question 6 (moderate) — Comparing groups fairly**

Of 600 users under 65, 510 completed a form online. Of 200 users over 65, 60 completed. What is the gap in percentage points?

- A) 30
- B) 45
- C) 55
- D) 85

**Correct answer: C**

**Explanation:** Under-65s: 510 ÷ 600 = 85%. Over-65s: 60 ÷ 200 = 30%. The gap is 85 − 30 = 55 percentage points, giving C. Options A and D are the two group rates offered as if they were the gap, a distractor pattern worth recognising — numbers from your working frequently appear among the options. A 55 point gap is enormous and would justify immediate investigation. For an interaction designer the likely suspects are specific and checkable: touch target size, contrast, whether the layout requires horizontal scrolling at high zoom, whether error messages appear above the fold, and whether the journey depends on a device capability the group is less likely to have.

**Question 7 (moderate) — Percentage change**

After a change, weekly validation errors on a field fell from 1,200 to 900. What is the percentage decrease?

- A) 20%
- B) 25%
- C) 33%
- D) 75%

**Correct answer: B**

**Explanation:** The difference is 1,200 − 900 = 300, and 300 ÷ 1,200 = 0.25, so a 25% decrease, giving B. Option C is 300 ÷ 900, dividing by the new figure — the most common error in this question type. Option D is the new figure as a proportion of the old, which tells you errors are now three quarters of what they were: a true statement answering a different question, and a distractor specifically designed to catch people who calculate correctly and then mismatch the answer to the stem. The rule: for percentage change, the denominator is always where you started.

**Question 8 (moderate) — Scale of a fix**

A service receives 480,000 submissions a year. A field currently produces a validation error for 4% of users, each of whom must correct it. How many corrections a year would eliminating the problem avoid?

- A) 1,920
- B) 19,200
- C) 20,000
- D) 192,000

**Correct answer: B**

**Explanation:** 4% of 480,000 is 0.04 × 480,000 = 19,200, giving B. Option A is 4% of 48,000; option D is 40%. This calculation earns its place because of what it does to a conversation. "A 4% error rate" sounds like an acceptable cost of doing business, and "19,200 people a year having to stop, read an error and re-enter something" does not. Converting a percentage into people takes five seconds and is the single most effective move available when arguing for a small fix nobody thinks is worth prioritising — and it sets up the next question, which is what each of those corrections costs in time, abandonment and support calls.

**Question 9 (moderate) — Choosing the denominator**

A journey shows 30,000 start, 24,000 pass eligibility, 14,400 reach the declaration, 12,960 submit. What percentage of those who reached the declaration went on to submit?

- A) 43%
- B) 54%
- C) 60%
- D) 90%

**Correct answer: D**

**Explanation:** The stem names users who reached the declaration, so the denominator is 14,400 and the part is 12,960: 12,960 ÷ 14,400 = 0.9, giving D. Option A uses 30,000, option B uses 24,000, option C is the eligibility-to-declaration rate. All four are true of this journey and one answers the question. Strategically, the numbers also tell you where to look: 6,000 lost at eligibility, 9,600 between eligibility and the declaration, and 1,440 at submission. A proposal to redesign the submission page would need a very good reason.

**Question 10 (harder) — A metric that hides a split**

Time on a page averages 45 seconds. Your sessions showed participants either glancing for a few seconds or reading carefully for two to three minutes. What is the most useful response?

- A) The average is wrong.
- B) The average is probably correct and uninformative: it sits between two clusters and describes neither, so ask for the distribution — which will show whether the page has two distinct audiences behaving differently.
- C) The participants were unrepresentative.
- D) The page should be shorter.

**Correct answer: B**

**Explanation:** When behaviour splits into two clusters, the mean lands in the gap and describes nobody. A 45-second average is entirely consistent with half the users spending five seconds and half spending two and a half minutes, and those are two different design problems: people glancing may be skipping content they need, while people reading carefully may be struggling with it. Option B asks for the distribution, which is the single most useful request you can make of an analytics colleague, and names what it would reveal. Option A disputes a figure that is probably calculated correctly. Option C blames the research. Option D leaps to a solution that could harm the careful readers by removing content they were relying on.

**Question 11 (harder) — Percentage points and relative change**

Error-free completion rose from 50% to 62% after a redesign. Which statement is accurate?

- A) It rose 12%.
- B) It rose 12 percentage points, a 24% relative increase.
- C) It rose 24 percentage points.
- D) It rose 19.4%.

**Correct answer: B**

**Explanation:** The arithmetic gap is 62 − 50 = 12 percentage points. The relative increase is 12 ÷ 50 = 0.24, or 24%. Option B labels both correctly. Option A is ambiguous and generally read as relative, making it wrong. Option C misapplies the percentage-point label. Option D divides by the new value. This matters beyond the test because both descriptions will be used to describe the same change, and one sounds twice as impressive. Being the person who quotes both, without making it an accusation, is a cheap way to be trusted with numbers.

**Question 12 (harder) — What a small comparison can establish**

Your team wants to know whether a redesign improved completion. Baseline is 62%, and a 5 percentage point improvement would be meaningful. A colleague suggests 20 moderated sessions before and 20 after. What is the strongest response?

- A) Agree; 40 sessions is reasonable.
- B) Explain that a 5 point difference on 20 per group is one participant and well inside ordinary variation, so the comparison cannot detect it — recommend measuring the rate with live analytics across all users, and spending the 40 sessions on understanding why users succeed or fail, which sessions do uniquely well.
- C) Increase to 40 per group.
- D) Run it and report the difference with caveats.

**Correct answer: B**

**Explanation:** With 20 per group a five point difference is a single participant, indistinguishable from chance; detecting a difference that small reliably needs hundreds per group. Option B says so and redirects rather than merely objecting: analytics can measure the rate across the whole user base at no recruitment cost, while moderated sessions are the only method that explains why the rate is what it is. That division of labour is the substantive recommendation. Option A endorses a design that cannot answer its own question. Option C moves towards adequacy without approaching it. Option D is the most damaging, because a reported difference from an underpowered comparison invites the team to act on noise, and caveats do not travel — the number does.

### Preparation tips

- **Find the denominator first.** Underline the group the question names.
- **Measure drop-off against the number who arrived.** Not the number who continued.
- **Convert percentages into people.** "4% of users" and "19,200 corrections a year" are the same fact; only one gets a fix prioritised.
- **Convert to rates before comparing anything.** Raw counts across unequal groups mislead every time.
- **Ask for the distribution.** It is the most useful request you can make of an analytics colleague.
- **Learn the percentage point sentence until it is automatic.**
- **Know roughly what samples can detect.** Twenty per group cannot see five points.
- **Practise on your own service's numbers.** Calculate the error rate on a real field and the loss at every page.

### Common pitfalls to avoid

- **Dividing by the wrong total.** Funnel items are built around this single error.
- **Comparing raw counts before and after a change.** Traffic changes too.
- **Confusing percentages with percentage points.** Both are correct labels for different things.
- **Accepting a mean without checking for clusters.** Bimodal behaviour hides entirely behind an average.
- **Reporting a number from your working as though it answered the question.** Distractors are built from exactly that.
- **Endorsing an underpowered comparison.** Acting on noise is worse than acting on nothing.
- **Rounding too early.** Carry a decimal and round at the end.
- **Leaving a percentage as a percentage.** People do not feel percentages.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A verbal reasoning assessment measures how accurately you read. It is one of the strongest predictors of performance in roles that run on documents, and interaction design is such a role. You read design standards, accessibility criteria, component specifications, content guidance, technical constraints and the words users say. Reading any of those slightly wrong changes what gets built.

The classic format presents a short passage of dense workplace prose, typically three to six sentences, followed by statements to classify as True, False or Cannot Say. True means the statement follows necessarily. False means the passage contradicts it. Cannot Say means the passage neither establishes nor excludes it. Alongside these come comprehension questions, main-point questions, and items asking which of four summaries is most accurate.

The governing rule is that you answer from the passage alone. Everything you know about the Design System, about WCAG, about what your team does — set it aside. If the passage contradicts what you believe, the passage still governs. This feels unnatural and it is the largest single source of lost marks: candidates recognise a statement as true of the world and mark it True even though the passage never said it. That is a Cannot Say.

Cannot Say deserves particular attention because people avoid it. It feels evasive, so candidates reach for True or False to appear decisive. In practice Cannot Say is frequently correct. The diagnostic: if you find yourself supplying a link the passage does not make, that is a Cannot Say.

Small words carry the meaning. "All" is not "most". "May" is not "must". "Should" is not "will". "Encouraged" is not "required". "Unless", "provided that" and "where practicable" flag conditions governing everything around them.

For an interaction designer there is a specific payoff. Accessibility criteria and component specifications are written with unusual precision, and a great deal of poor practice comes from remembering the gist rather than the wording. Reading them exactly is how you avoid both over-compliance, which wastes effort, and under-compliance, which excludes people.

### How this assessment maps to your role

The verbal skills tested map onto your named skills:

- **Reading precisely** maps to **Designing for everyone**, where you ensure a design meets appropriate standards such as accessibility regulations, with support.
- **Separating statement from inference** maps to **Evidence-based design**, where you analyse and clearly explain evidence.
- **Identifying the main point** maps to **Design communication**, where you clearly explain problems and design ideas to others.
- **Handling qualified language** maps to **Designing strategically**, where you explain the value of patterns and components — and where knowing whether one is mandatory or recommended tells you how much room you have.
- **Reading for absence** maps to **Designing for everyone**, where noticing that a specification never mentions keyboard operation has a direct consequence.
- **Understanding written direction** maps to **Designing together**, where feedback only works if understood as given.

### Practice questions

*Passage A — for Questions 1 to 4*

"All new public-facing services must use components from the Design System where a suitable component exists. Where no suitable component exists, teams may create a new one, provided it is documented and tested with assistive technology before use in a live service. Components created before this policy took effect must be reviewed within 12 months. Teams are encouraged, but not required, to contribute new components back to the Design System."

**Question 1 (easy)** — Statement: "Teams must contribute new components back to the Design System." True, False or Cannot Say?

**Correct answer: False**

**Explanation:** The passage says teams are *encouraged, but not required*, to contribute components back. The statement's "must" contradicts that explicitly, so False. This is the clearest form of the pattern — an explicit removal of an obligation. Note that the passage attaches hard requirements elsewhere in the same breath, to documentation and assistive technology testing, so a reader skimming for the general tone would get this wrong in either direction.

**Question 2 (moderate)** — Statement: "A team that creates a new component without testing it with assistive technology has breached the requirements." True, False or Cannot Say?

**Correct answer: True**

**Explanation:** The passage permits creating a new component *provided it is documented and tested with assistive technology before use in a live service*. Those are conditions on the permission, and failing one means the permission does not apply, so the requirement is breached. True. Note the contrast with Question 1: there the passage explicitly removed an obligation, giving False; here it attached conditions to a permission, and failing a condition is a breach. Distinguishing an explicit exemption from a conditional permission is one of the more useful habits this section builds, and it transfers directly to reading real standards.

**Question 3 (moderate)** — Statement: "A component created two years ago must have been reviewed by now." True, False or Cannot Say?

**Correct answer: Cannot Say**

**Explanation:** Components created before the policy took effect must be reviewed within 12 months — but the passage never says when the policy took effect. If it took effect two years ago, a review would be overdue; if six months ago, it would not. Because the fact you would need is absent, the answer is Cannot Say. Whenever a passage sets a deadline relative to a policy's commencement, check whether the commencement date is actually given. Its absence is deliberate and it appears in this section repeatedly.

**Question 4 (moderate)** — Statement: "A service may use a component that is not in the Design System." True, False or Cannot Say?

**Correct answer: True**

**Explanation:** The passage requires Design System components only *where a suitable component exists*, and expressly permits creating a new one where none does, subject to conditions. So a service may indeed use a non-Design-System component in the described circumstances, and the statement — which claims only that this is possible — is supported. True. Candidates sometimes mark this False by reading the first sentence in isolation as a blanket requirement, which is exactly the error the passage's structure is testing. Read to the end of a provision before concluding what it requires.

*Passage B — for Questions 5 to 8*

"The review of the application form found that users on mobile devices completed more slowly than desktop users and were more likely to abandon at the document upload step. The review notes that mobile users differed from desktop users in age and in whether they were completing the form at home. The review did not assess whether abandoned applications were later completed on another device. It recommends that the team consider whether a redesigned upload step would reduce mobile abandonment."

**Question 5 (easy)** — Statement: "Mobile users were more likely to abandon at the upload step." True, False or Cannot Say?

**Correct answer: True**

**Explanation:** The first sentence states this directly and the statement restates it without addition. True. Note the passage's careful "more likely to abandon" rather than "usually abandon", and the statement respects it. A statement claiming mobile users "usually abandon" would be far stronger than the passage supports.

**Question 6 (moderate)** — Statement: "The mobile interface causes abandonment at the upload step." True, False or Cannot Say?

**Correct answer: Cannot Say**

**Explanation:** The passage reports an association and explicitly names two ways the groups differed: age, and whether they were completing the form at home. Either could explain it — someone completing a form away from home is less likely to have their documents to hand, which produces upload abandonment regardless of interface quality. The passage neither asserts nor excludes an interface cause, so Cannot Say. The design consequence is direct: if the interface is the cause you redesign it; if the cause is that mobile users are not at home, the answer is saving and returning, or telling people what they will need before they start.

**Question 7 (moderate)** — Statement: "Users who abandoned on mobile did not complete the application at all." True, False or Cannot Say?

**Correct answer: Cannot Say**

**Explanation:** The passage says explicitly that the review did not assess whether abandoned applications were later completed on another device. Declared silence establishes nothing, so Cannot Say. This item is worth dwelling on because the intuitive reading is wrong in a specific and consequential way: abandonment on one device may be a user sensibly switching to a laptop where the documents are, which is a mild inconvenience rather than a service failure. Not knowing which of those it is changes how urgent the problem is, and the review flagged the gap rather than letting readers assume.

**Question 8 (harder)** — Statement: "The review recommends redesigning the upload step." True, False or Cannot Say?

**Correct answer: False**

**Explanation:** The review recommends that the team *consider whether* a redesigned upload step would reduce abandonment — a recommendation to evaluate an option, including the possibility of concluding it would not help. The statement asserts a recommendation to redesign, which was not made, so it is False rather than Cannot Say: the passage tells you what was recommended and it was something different. This distinction pervades real review documents and produces the familiar sequence in which a recommendation to consider becomes a commitment to deliver, gets tracked, and is reported against without anyone having decided it was right.

*Passage C — for Questions 9 to 12*

"Interactive components must be operable using a keyboard alone. Where a component uses a non-standard interaction, the team must provide a documented keyboard alternative. Focus must be visible at all times and must not be trapped within a component. Where a component displays an error, the error must be programmatically associated with the field it relates to; a visual association alone is not sufficient."

**Question 9 (easy)** — Statement: "A visual association between an error and its field is sufficient." True, False or Cannot Say?

**Correct answer: False**

**Explanation:** The final clause states that a visual association alone is not sufficient and that the error must be programmatically associated. The statement contradicts this directly, so False. The word doing the work is "programmatically", and skimming past it produces exactly the failure the requirement exists to prevent: a message placed next to a field is obvious to a sighted user and may be entirely absent for someone whose screen reader encounters fields and messages in whatever order the markup dictates.

**Question 10 (moderate)** — Statement: "A component with a non-standard interaction breaches the requirements." True, False or Cannot Say?

**Correct answer: False**

**Explanation:** The passage does not prohibit non-standard interactions; it requires that where one is used, a documented keyboard alternative is provided. So a non-standard interaction with such an alternative complies, and the statement — asserting a breach from the interaction alone — is contradicted. False. This is a standard setting a condition rather than a prohibition, and reading it as a prohibition produces two bad outcomes: teams avoid legitimate solutions unnecessarily, or conclude the rule is unrealistic and ignore it entirely.

**Question 11 (harder)** — Statement: "A component in which focus is briefly trapped while a dialogue is open complies with the passage." True, False or Cannot Say?

**Correct answer: False**

**Explanation:** The passage states that focus must not be trapped within a component, without qualification as to duration or context. The statement's "briefly" and "while a dialogue is open" introduce conditions the passage does not recognise, and the requirement as written is absolute. So the statement is contradicted and the answer is False. This item is deliberately uncomfortable, because in real practice a modal dialogue is normally expected to constrain focus within itself while open, and you may know that. The passage as written does not carve out that case — and the whole discipline of this section is answering the passage rather than the world. In a real workplace the right response would be to query the wording; in the test, the wording governs.

**Question 12 (harder) — Main point**

Which best captures the main point of Passage C?

- A) Components must never use non-standard interactions.
- B) Components must remain operable and comprehensible for someone not using a mouse or not seeing the screen — through keyboard operation, visible and unconstrained focus, documented alternatives where interactions are unusual, and errors associated in code rather than only visually.
- C) Focus must be visible at all times.
- D) Errors must be programmatically associated with their fields.

**Correct answer: B**

**Explanation:** The main point must span the passage while adding nothing. Option A overstates a conditional requirement into a prohibition. Options C and D are each true of one clause and silent on the rest, making them details rather than main points. Option B captures all four requirements and the logic joining them: every one exists so the component works for someone who is not using a mouse or not seeing the screen. Main-point items reward the option broad enough to cover everything and disciplined enough to invent nothing, and three of these four are true details promoted beyond their scope.

### Preparation tips

- **Point at the words.** Before marking True, identify the phrase that makes it true.
- **Trust Cannot Say.** If you are supplying a link, that is the diagnostic.
- **Circle every qualifier.** All, some, most, may, must, should, encouraged, unless, provided that, where practicable.
- **Distinguish an exemption from a conditional permission.** "Not required" gives False; "provided that" makes failure a breach.
- **Look for the missing fact.** Some items are Cannot Say because a commencement date was never given.
- **Answer the passage, not the world.** Even where you know the real standard is more nuanced.
- **Treat declared silence as silence.** A review that did not examine something has told you nothing.
- **Practise on real standards.** Take an accessibility criterion and write three statements — one True, one False, one Cannot Say.

### Common pitfalls to avoid

- **Answering from professional knowledge.** The commonest cause of lost marks, and it gets worse as you learn more.
- **Avoiding Cannot Say.** It converts good reading into wrong answers.
- **Reading "encouraged" as "required".** Standards put soft aspirations next to hard rules.
- **Reading a condition as a prohibition.** "Where X, do Y" permits X.
- **Skimming a load-bearing adverb.** "Programmatically" changes the whole requirement.
- **Treating association as causation.** A passage naming confounds is warning you off.
- **Reading "consider whether X" as "recommend X".** Review prose runs on this.
- **Inferring from what a review did not examine.** Declared silence is not evidence.

## Workplace job-specific situational judgement assessment

### About this assessment

A situational judgement assessment presents realistic workplace scenarios and asks what you would do. There is no passage to decode and no arithmetic. You get a dilemma of the kind your role produces, four or five candidate responses, and a question asking which is most effective and often which is least.

This section measures judgement rather than knowledge, and specifically whether your instincts match what the profession considers good practice at your level. Your role description places you as someone who explains design decisions, works collaboratively, has responsibility as part of a service, works independently after being given direction, and independently identifies user issues and important needs. So the strongest answers involve genuine independent action within your remit combined with prompt honesty about anything beyond it. Neither struggling in silence nor escalating everything scores well.

Four principles carry most scenarios.

Users come first, and in interaction design that specifically means the users who cannot get past something. When an option protects somebody who cannot operate a control, read an error or recover from a mistake, it almost always outranks one protecting a schedule, a budget or somebody's preference. An interaction that excludes one group is not slightly worse for them; it is unusable.

Act within your remit and be transparent at its edges. At your level you are expected to make design decisions, hold a position with a developer, and identify user needs yourself. You are not expected to overrule a technical constraint, commit the organisation, or absorb an accessibility blocker without telling anyone. The pattern is: do what you competently can, then tell the right person promptly.

Address problems directly, early, with the person involved. Private, specific, non-accusatory conversation beats public correction, silence, or routing around someone.

Check both scales. When one option fixes the control in front of you and another asks whether it should be there, or what happens to someone who gets it wrong, the second is usually stronger.

One trap: options that are pleasant, and options that are decisive, are both attractive for reasons unrelated to effectiveness.

### How this assessment maps to your role

The judgement dimensions map onto your named skills:

- **Explaining and defending design decisions** maps to **Design communication**, where you clearly explain problems, ideas and decisions using appropriate tools and methods.
- **Protecting inclusion** maps to **Designing for everyone**, where you work with others to deliver accessible services meeting the needs of all users and ensure designs meet appropriate standards.
- **Working with others' perspectives** maps to **Designing together**, where you explain techniques for bringing together multiple perspectives and the importance of constructive feedback.
- **Using evidence honestly** maps to **Evidence-based design**, where you analyse and clearly explain evidence and work with researchers and analysts.
- **Working in cycles and adapting** maps to **Iterative design**, where you apply iterative principles and improve designs across successive rounds.
- **Knowing where design sits** maps to **Designing strategically** and **Leading design**.

### Practice questions

**Question 1 (easy) — A developer proposes a shortcut**

A developer says the agreed error handling will take three extra days and proposes instead a single message at the top of the page saying "There is a problem with your answers". What is the most effective response?

- A) Agree; three days is a lot and the message tells users something.
- B) Explain what the generic message costs users — they must find the problem themselves, and someone using a screen reader may be unable to — and ask whether a middle option fits the time, such as specific messages for the two fields that fail most often.
- C) Insist on the full agreed behaviour.
- D) Escalate to your senior designer without talking to the developer.

**Correct answer: B. Least effective: A**

**Explanation:** The developer has a real constraint and has proposed a solution that solves their problem by transferring the cost to users. Option B does three things: makes the user cost concrete rather than appealing to a standard, treats the time constraint as legitimate, and proposes a middle path, which is what usually gets agreed in practice. Naming the screen reader consequence matters specifically, because "there is a problem" with no indication of where is close to unusable without sight. Option A is least effective, accepting a change that will generate confusion and repeat submissions to save three days once. Option C may be right in the end and skips the collaborative step. Option D bypasses a colleague who has not had a chance to discuss it, though telling your senior afterwards is sensible.

**Question 2 (easy) — A defect you find in a live service**

Reviewing a live page, you find the error summary does not link to the fields it describes, so a keyboard user must tab through the page to reach the problem. What is the most effective response?

- A) Note it in your own list to fix eventually.
- B) Raise it with your senior designer and the team, describing precisely what a keyboard user has to do, and ask whether the same defect exists on other pages using the same template.
- C) Raise a bug ticket and move on.
- D) Fix it yourself in the prototype so the next build picks it up.

**Correct answer: B. Least effective: A**

**Explanation:** You have found a real accessibility defect, and describing the consequence rather than the rule is what makes it actionable. What lifts option B above the alternatives is the second clause: a defect in an error summary almost certainly comes from a shared template, so the same problem probably exists on every page using it. Asking that question turns one fix into a systemic one, and at your level noticing the pattern behind an instance is exactly the step up from trainee. Option A is least effective, deferring a live accessibility defect to a personal list. Option C is reasonable and incomplete, since a ticket without the pattern question fixes one page. Option D fixes a prototype rather than the live service, which helps future builds and leaves the current defect in place.

**Question 3 (easy) — Conflicting direction**

Your senior designer asked you to finish the interaction spec today. Your delivery manager then asks you to spend the day updating the prototype for tomorrow's show and tell, calling it urgent. What is the most effective response?

- A) Do the prototype; the delivery manager is more senior.
- B) Do the spec and tell the delivery manager you are unavailable.
- C) Tell the delivery manager about the existing task, offer a specific workable option, and ask them and your senior designer to confirm the priority.
- D) Attempt both and work late.

**Correct answer: C. Least effective: D**

**Explanation:** Two legitimate instructions have collided, and while resolving them is not yours to impose, surfacing the conflict promptly and helpfully is. What lifts option C above bare escalation is the offer of a specific option — "I could update the prototype this morning and have the spec by four" — which makes you part of the solution. Option A ranks by seniority; the delivery manager probably does not know about the spec. Option B is abrupt and leaves a real need unmet. Option D is least effective because working late hides the conflict, normalises over-commitment, and means the team never learns it is asking one person for two days.

**Question 4 (moderate) — Evidence that contradicts your design**

You designed a page, and in testing five of eight participants clicked a secondary link instead of the primary button. You believe the design is right. What is the most effective response?

- A) Note that the participants were unrepresentative and keep the design.
- B) Treat the result as a signal about the design, look at what drew people to the link — wording, position, visual weight, or whether it answers a question the page raised — and propose a change to test next round.
- C) Remove the secondary link.
- D) Ask for more participants before deciding.

**Correct answer: B. Least effective: A**

**Explanation:** Five of eight doing the same unexpected thing is a signal, not a coincidence, and the first move is to ask what in the design produced it rather than what was wrong with them. Option B does that and keeps it testable. Note the fourth possibility it lists, which designers often miss: people may click a link because the page raised a question it did not answer, in which case the fix is content rather than visual hierarchy. Option A is least effective — dismissing consistent behaviour as unrepresentative is the most reliable way for a designer to stop learning. Option C acts on a diagnosis you have not made; the link may be essential. Option D delays a cheap improvement, and eight participants converging is enough to justify trying something different.

**Question 5 (moderate) — Pressure to reuse a pattern badly**

A stakeholder asks you to use the "check your answers" pattern for a page listing documents the user must still obtain, arguing it will be quicker and look consistent. What should you do?

- A) Use it; consistency matters.
- B) Explain that the pattern sets an expectation — that everything shown is done and editable — which is wrong here and will mislead users, and propose a different pattern for "things you still need to do" while keeping the same visual style so the service stays consistent.
- C) Refuse and design from scratch.
- D) Use it but change the heading.

**Correct answer: B. Least effective: D**

**Explanation:** The stakeholder's goals — speed and consistency — are legitimate, and the proposal misunderstands what a pattern is. A pattern is not a layout; it is a set of expectations users have learned, and "check your answers" teaches people that what they see is complete and changeable. Applying it to outstanding tasks tells users the opposite of the truth. Option B holds the substance and addresses both goals directly, which is what makes it persuasive rather than obstructive. Option D is least effective: changing the heading while keeping a layout whose meaning is wrong is the worst combination, because users trust the visual language more than the words, and the layout will still say "done". Option A ships a misleading page. Option C discards the reuse that would genuinely help.

**Question 6 (moderate) — A constraint you doubt**

A developer says a postcode field cannot accept spaces "because of the database". Research shows many users type a space and then hit an error. What is the most effective response?

- A) Add a hint telling users not to type a space.
- B) Ask what the constraint actually is, and whether the space could be stripped when the value is saved rather than rejected when it is typed — since the requirement is presumably about what is stored, not about what the user types.
- C) Insist the field accepts spaces.
- D) Escalate without asking the developer.

**Correct answer: B. Least effective: A**

**Explanation:** "The database won't allow it" is sometimes exactly true, sometimes a summary of a storage requirement satisfiable another way, and sometimes an inherited assumption nobody has revisited. Option B asks the productive question and proposes the specific mechanism that resolves most versions of this: normalise input on save rather than validating on entry. That distinction between what a user types and what a system stores is one of the most useful things an interaction designer carries into conversations with developers. Option A is least effective — it makes users responsible for accommodating an internal constraint, and hint text telling people not to do the natural thing is reliably ignored, so the errors continue and the page is longer. Option C asserts without understanding. Option D bypasses a colleague.

**Question 7 (moderate) — Feedback that stings**

In a critique, a senior designer says your flow is "confusing and doesn't show what happens on a 'no' answer". You think it does. What is the most effective response?

- A) Point out where the branch appears.
- B) Ask them to show you where they got lost, since if an experienced designer cannot follow the branch the diagram is not communicating it — then fix that.
- C) Accept the criticism and redo it.
- D) Ask for the feedback in writing to consider later.

**Correct answer: B. Least effective: A**

**Explanation:** Both things can be true: the branch is there, and the diagram does not communicate it. Option B recognises that and converts feedback into information, which is more useful than establishing who was right and makes senior colleagues willing to review your work again. Option A is least effective because winning the argument leaves the flow as confusing as it was and teaches the room that giving you feedback is effortful. Option C accepts the verdict without extracting the detail, so you may reproduce the problem. Option D defers a two-minute conversation. Receiving feedback well is at least half of the constructive feedback skill your role names.

**Question 8 (moderate) — Something outside your service**

You notice the letter sent after submission uses completely different wording from the confirmation screen you designed, so users may think they are two different things. Letters belong to another team. What is most effective?

- A) Ignore it; letters are not your responsibility.
- B) Raise it with your senior designer, describing the mismatch and why it matters, and ask about a route to the team that owns the letter — while checking whether your own confirmation screen could reduce the confusion in the meantime.
- C) Contact the other team directly.
- D) Change your screen to match the letter.

**Correct answer: B. Least effective: A**

**Explanation:** A user does not experience your screen and their letter as two products; they experience one service saying two different things, which produces exactly the uncertainty that generates calls. Option B evidences the problem, seeks a legitimate route through someone with standing, and — this is the part that makes it your level rather than a trainee's — asks what the half you control can do meanwhile. Option A is least effective, because "not my responsibility" describes an org chart rather than an experience. Option C may be fine in some organisations and risks cutting across conversations you cannot see. Option D changes the half you control to match a half that may itself be wrong.

**Question 9 (harder) — An accessibility blocker close to launch**

Two weeks before launch you find a custom component cannot be operated with a keyboard. Fixing it delays launch. What is most effective?

- A) Launch and add it to the backlog.
- B) Raise it immediately with your senior designer and delivery manager, describe precisely what cannot be done and by whom, ask for an explicit decision, and check whether a standard component could replace the custom one quickly.
- C) Attempt the fix yourself in the two weeks.
- D) Launch and publish an accessibility statement noting the gap.

**Correct answer: B. Least effective: A**

**Explanation:** A component that cannot be operated by keyboard means some people cannot use the service at all, and weighing a delay against an exclusion is a decision for people with the authority to make it — though raising it is entirely yours. Option B does everything in your remit and adds the practical step that most often resolves this: checking whether a standard component can replace the custom one, which is frequently the fastest fix available and which nobody thinks of under pressure. Asking for an explicit decision matters too, because an unrecorded decision drifts into a launch by default. Option A is least effective — the backlog is where accessibility problems go to remain unfixed. Option D treats an accessibility statement as a way to launch with a known blocker, which it is not. Option C risks a fortnight and leaves nobody with authority aware.

**Question 10 (harder) — Findings the team does not want**

Research shows a component the team built over a month causes problems for eight of ten participants. You have five minutes at the show and tell. What is most effective?

- A) Lead with the positives and mention difficulties briefly.
- B) Present what happened clearly and without blame — what participants tried, where they got stuck, what they said — and frame the next step as understanding why, inviting the team into the diagnosis.
- C) Present the failure rate starkly so the team takes it seriously.
- D) Ask your senior designer to present it.

**Correct answer: B. Least effective: A**

**Explanation:** Difficult findings are the most valuable, and delivery determines whether they get acted on or defended against. Option B keeps the focus on observed behaviour rather than on the quality of anyone's work, which lets the team engage with the problem instead of their feelings about it, and ending on a question brings the people who built it into the analysis, where they will often see causes you cannot — a developer may know immediately why focus behaves oddly. Option A is least effective: softening an eight-in-ten failure means a month of effort continues down the same path, which serves nobody. Option C is accurate and adversarial, and a defensive room learns nothing. Option D is understandable and deprives you of the experience.

**Question 11 (harder) — A mistake of your own**

You realise a prototype you shared a fortnight ago, which the team has been building from, omits the branch for users who answer "no" at eligibility. What should you do?

- A) Update it and mention it at stand-up.
- B) Tell the team immediately, explain what was missing, flag which stories may have been built without the branch, and check whether the live or in-progress build leaves those users at a dead end.
- C) Update it quietly.
- D) Raise it in the retrospective.

**Correct answer: B. Least effective: C**

**Explanation:** Two weeks of building against an incomplete prototype means the correction alone is insufficient — the important elements are flagging affected stories and, distinctively for interaction design, checking whether the omission has produced an actual dead end for real users. A missing branch in a prototype is usually an unhandled path in the build, where someone answering "no" reaches an error or nothing at all. That is a defect with a person on the other side of it. Option C is least effective, leaving both the documentation and the likely defect unexamined and risking discovery by someone else. Option A treats it as housekeeping. Option D defers to a meeting when the information is needed now.

**Question 12 (harder) — An assumption in the room**

In a session someone says "we don't need to worry about screen reader users here — hardly anyone uses one". The service has around 900,000 users a year. What is most effective?

- A) Let it go; the team has decided.
- B) Bring the arithmetic into the room — even one per cent of 900,000 is 9,000 people a year, and the real figure is higher once magnification, voice control and keyboard-only use are included — and ask what should happen to them, so the decision is made knowingly.
- C) Argue that all services must be accessible to everyone.
- D) Raise it privately with your senior designer afterwards.

**Correct answer: B. Least effective: A**

**Explanation:** The comment rests on an intuition about proportion, and intuitions about proportion collapse against a base number. Even one per cent of 900,000 is 9,000 people a year, and the population is larger than "screen reader users" suggests once you include people using magnification, voice control, or a keyboard because of a temporary injury or a broken trackpad. Option B supplies the arithmetic and then asks a question, which is the most effective form of challenge available and genuinely the right thing to do, since the team may have an answer. Option A is least effective, because a decision made on an assumption that is numerically wrong will exclude real people and you had the number. Option C states a true principle in a way that invites a debate about principles. Option D is a reasonable backup and misses the moment.

### Preparation tips

- **Answer as a junior with real responsibility.** Competent independent action, plus prompt honesty beyond your remit.
- **Put the excluded user first.** When an option protects someone who cannot operate a control, assume it is strongest.
- **Ask whether an instance is a pattern.** One broken error summary usually means a broken template.
- **Bring the number, not the principle.** Converting a percentage into people changes rooms.
- **Ask what a constraint actually is.** "The database won't allow it" is a question, not an answer.
- **Offer a middle option.** When a colleague proposes a shortcut, find a cheaper way to protect the user.
- **Ask for an explicit decision.** Unrecorded decisions drift into launches.
- **Read the least-effective question separately.** The worst option usually conceals something or transfers cost to users.

### Common pitfalls to avoid

- **Dismissing consistent behaviour as unrepresentative participants.** Five of eight is a signal about your design.
- **Accepting a shortcut that transfers cost to users.** Three saved days against months of confusion is a bad trade.
- **Keeping a pattern whose meaning is wrong.** Users trust the layout more than the words.
- **Making users accommodate an internal constraint.** Normalise on save rather than rejecting on entry.
- **Fixing an instance and missing the template.** One page fixed, twenty still broken.
- **Winning the argument about feedback.** If an experienced designer got lost, the artefact is unclear.
- **Treating an accessibility statement as a way to launch with a blocker.** It is for gaps you are closing.
- **Treating a missing branch as a documentation gap.** It is usually a live dead end.

## Conclusion

You have reached the end, and it is worth pausing over what that involved: forty-eight questions across four assessment types, with the reasoning worked through on each. That is a substantial piece of preparation and rather more than most people do.

Look back at the ground. In the cognitive section you counted rule breaches rather than pages, reconciled analytics that appeared to contradict research, chose a prototype fidelity from the question rather than the habit, weighed one-thing-per-page against page loads on a poor connection, and found a searchable dropdown wanting against eight radio buttons. In the numeric section you measured drop-off against the right denominator, compared devices fairly, converted 4% into 19,200 corrections a year, distinguished a percentage from a percentage point, spotted a mean sitting between two clusters, and declined to endorse a comparison too small to detect what it was built to find. In the verbal section you told an explicit exemption from a conditional permission, spotted a missing commencement date, noticed "programmatically" carrying an entire requirement, and answered a passage rather than the world even where you knew the real standard was more nuanced. And in the situational judgement section you found a middle path with a developer under time pressure, asked whether one broken error summary meant a broken template, asked what a database constraint actually was, and brought arithmetic to an assumption nobody had examined.

Notice how little of that was really about tests. Every one is a working skill. A designer who calculates against the right denominator, reads the specification as written, checks both the element and the flow, brings the number rather than the principle, and says so within ten minutes of finding their own mistake — that is simply a good designer. Preparing for these assessments and getting better at the job turn out to be nearly the same activity.

A word about where you sit. Junior interaction designer is a genuinely good stage. You are past needing someone beside you for everything, and not yet expected to have an answer for everything. Your role captures it well: you explain design decisions, work collaboratively, have responsibility as part of a service, and work independently after being given direction. Use that direction deliberately. The designers who progress fastest are not the ones who ask for the least help; they are the ones who ask precise questions, act on the answers, and gradually need to ask less.

If you want to build on this, a few things repay effort more than rereading. Unplug your mouse for an afternoon and complete your own service using only the keyboard — you will find things no review surfaces. Turn on a screen reader and listen to one of your pages until you understand what an error summary is actually for. Read the "when not to use this" section of a component you use often. Sit with a developer and ask how a validation rule is actually implemented, and what happens to the value between the keyboard and the database. And practise stating findings out loud at the right strength — "eight of twelve participants", not "most users" — until the accurate version is the one that comes naturally.

Finally, for the day itself. An assessment is a snapshot taken on one morning under artificial conditions. It is not a verdict on your ability or your future in this profession. Read the stem twice, find the denominator, trust Cannot Say, check both scales, and remember that careful beats fast.

Good luck. Go carefully, ask what things are for, and keep unplugging the mouse.
