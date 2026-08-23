# Interaction Designer - Psychometric Assessment Resources

## Introduction

Welcome. This guide is written for you as an interaction designer in the UK Government Digital and Data profession — a confident, competent designer who develops designs from evidence of user needs and organisational outcomes, who is trusted to make good decisions, who recognises when to ask for further guidance, who contributes to design concepts, and who interprets evidence-based research and incorporates it into their work. That combination of trust and judgement shapes everything that follows.

You may be preparing for a formal assessment as part of a recruitment or promotion process, or you may simply want to sharpen the reasoning your job depends on. Either way, it is worth being precise about what psychometric assessment is at this level. It is not an intelligence test and it is not a knowledge quiz. It is a standardised sample of the thinking a role demands, and for a competent practitioner that thinking has a particular character: you are rarely choosing between a right answer and a wrong one, and usually choosing between defensible options under incomplete information, competing constraints and real consequences.

Three features of your role shape the questions here. First, you are trusted to make good decisions, which means the assessment will not reward escalating everything and will reward knowing which decisions genuinely belong to someone else. Second, you now design strategically: your role names identifying risks and using design to mitigate them, identifying opportunities and using design to take advantage of them, contributing to design patterns and components, and aligning your work to organisational objectives. That turns prioritisation from an administrative question into a design one. Third, you plan and run design sessions, engage the right people, and give and receive constructive feedback — so several items concern how you get good thinking out of a room rather than out of yourself.

There is a discipline-specific point worth naming. Interaction design operates at two scales at once — the flow and the element — and a great deal of senior-feeling judgement consists of noticing when a decision at one scale damages the other. Splitting a page helps comprehension and adds a round trip. Making a control cleverer helps confident users and breaks it for keyboard users. Reusing a pattern saves time and imports expectations that may be wrong. Several items below turn on exactly that trade-off, because it is where most real interaction design arguments actually live.

The document has four main sections:

1. A workplace job-specific cognitive assessment — evidence quality, methodological trade-offs, competing explanations, prioritisation, risk and opportunity, and the diagnosis of problems in a design.
2. A numeric reasoning assessment — rates, funnel data, device comparisons, weighted figures and the interrogation of quantitative claims made by others.
3. A verbal reasoning assessment — standards, accessibility criteria, review reports and stakeholder correspondence, with items pitched at genuine ambiguity.
4. A situational judgement assessment — realistic dilemmas at your level of independence, covering ethics, stakeholder consensus, design integrity and team dynamics.

Each section provides an overview, a mapping to your named skills, twelve practice questions with full explanations, preparation tips, and common pitfalls.

Commit to an answer before reading each explanation. At this level the reasoning transfers further than the answer, and the explanations spend most of their words on why the near-miss options fail. Pay particular attention where you were quick and certain.

Let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive assessment measures the reasoning your role genuinely uses, presented through practical materials rather than abstract puzzles. At your level the materials get messier and the reasoning less mechanical. You will meet evidence supporting two incompatible readings, design constraints that turn out to be negotiable and others that do not, components whose costs are not where they appear, and prioritisation problems with no dominant option.

The format is usually an online test of fifteen to thirty minutes covering pattern recognition, logical deduction, error checking, prioritisation and applied problem solving. Scoring is objective against a norm group at a comparable level. Many platforms are adaptive, so a test that feels hard is usually one you are doing well on, and acuity reports distinguishing speed from accuracy reward precision.

Two things distinguish this section at your level.

The first is that you are expected to reason about risk and opportunity rather than only about problems. Your role names identifying potential risks and using design to mitigate them, and identifying opportunities and using design to exploit them. That is forward-looking reasoning: given this evidence, what is likely to go wrong, and where is something available that nobody has taken? Several items turn on spotting a second-order consequence rather than an immediate one.

The second is comfort with irreducible uncertainty. A number of questions have no clean answer, only a best one, and the discriminating factor is whether you can identify the strongest reading of ambiguous evidence and state its limits rather than collapsing prematurely into confidence.

You need to memorise nothing. Everything you need appears in the question. What you need to bring is the discipline not to let familiarity substitute for examination.

### How this assessment maps to your role

The cognitive dimensions map onto the skills named in your role summary:

- **Pattern recognition** maps to **Evidence-based design**, where you analyse, synthesise and clearly explain evidence relevant to users or a service.
- **Logical deduction** maps to **Design communication**, where you clearly explain design decisions using appropriate tools and methods.
- **Error checking** maps to **Designing for everyone**, where you ensure a design meets appropriate standards such as accessibility regulations.
- **Prioritisation and risk reasoning** map to **Designing strategically**, where you identify risks and opportunities and use design to address them.
- **Applied problem solving** maps to **Iterative design**, where you prototype at different fidelities and use and iterate design patterns and components.
- **Reasoning about people and positions** maps to **Designing together**, where you identify and engage the right people throughout the design process.

### Practice questions

**Question 1 (easy) — Auditing a page against a standard**

Your standard requires every transactional page to: use words users would use, say what happens next, state how long it will take, avoid requesting information already held, offer a route to help, and work without JavaScript. A page uses internal terminology, says the case will be assessed, gives no timescale, re-requests a held reference number, has no contact route, and degrades gracefully without JavaScript. How many requirements are unmet?

- A) 3
- B) 4
- C) 5
- D) 6

**Correct answer: B**

**Explanation:** Work through all six. Internal terminology fails the first. "The case will be assessed" satisfies the second, minimally. No timescale fails the third. Re-requesting held information fails the fourth. No contact route fails the fifth. Graceful degradation satisfies the sixth. Four unmet, giving B. Option C typically comes from marking "what happens next" as unmet because the statement is thin — defensible as a design judgement, and the item is testing whether you apply the standard as written rather than as you would have written it, which is the discipline assurance requires. Note which two are easiest to miss: the absent help route and the JavaScript behaviour, both because they concern something that should be present rather than something present and wrong. Absences are the systematic blind spot in any audit.

**Question 2 (easy) — Deduction from a governance rule**

Your standard states: "A custom component may be used in a live service only with sign-off from the lead interaction designer, unless it replaces an existing custom component on a like-for-like basis and has been assessed as low risk." A developer says: "We shipped a custom component last sprint without sign-off." Which must be true?

- A) The standard was breached.
- B) It was a low-risk like-for-like replacement.
- C) Either it was a low-risk like-for-like replacement, or the standard was breached.
- D) The component is inaccessible.

**Correct answer: C**

**Explanation:** A conditional with a stated exception, plus facts silent on the exception, licenses only the disjunction. Options A and B each assume a branch. Option D imports a quality judgement the facts do not support. Only C holds. Note that the exception is compound: like-for-like *and* low risk. A replacement satisfying only one does not qualify, and partial satisfaction of a compound exception is among the most common misreadings in real governance conversations. As someone trusted to make good decisions, your opening move is to establish which route was taken — and framing it as an enquiry rather than a finding means you will not have to withdraw anything if the exception applied.

**Question 3 (moderate) — Competing explanations**

Completion of a form is 78% for users arriving from a guidance page and 49% for users arriving directly from a search result. A product manager proposes redesigning the form. What is the most rigorous analysis?

- A) Agree; the form is failing direct arrivals.
- B) The two groups differ in preparation rather than necessarily in what they encounter: users who came via guidance have generally learned what is required and gathered documents, while direct arrivals may be discovering requirements mid-form — so the highest-value intervention may be at the point of entry rather than inside the form.
- C) A 29 point gap is too large to be explained by anything but the form.
- D) Direct entry to the form should be blocked.

**Correct answer: B**

**Explanation:** Referral route is a marker for what the user has already done before arriving, and this is one of the most consequential confounds in service analytics. Someone who read guidance has typically established eligibility and assembled documents; someone landing from a search result may be doing both with the form open. That difference in preparation can account for much of the gap without the form being worse for anyone. Option B also draws the practical implication, which is what makes it rigorous rather than merely sceptical: a lightweight "what you'll need" step for direct arrivals may be cheaper and more effective than a redesign, and it is an interaction design intervention rather than a content one. Option A acts on an unexamined correlation. Option C mistakes effect size for causal certainty. Option D would harm users who arrive prepared.

**Question 4 (moderate) — Prioritising by what can change**

You have capacity for one substantial piece of work this quarter:

1. A key interaction pattern for a new service is being decided next month, and will be reused across eight journeys.
2. A live page has a 32% validation error rate on one field, unchanged for months.
3. A team wants exploratory work on a concept for next year.
4. The team wants to revisit a screen you designed six weeks ago after minor copy changes.

Which is strongest, and why?

- A) Item 2, because it affects the most users now.
- B) Item 1, because the decision is imminent, will be reused across eight journeys, and design input is the only thing that could still shape it — giving it far the highest leverage.
- C) Item 3, because early exploration has the highest leverage.
- D) Item 4, because unverified changes are a risk.

**Correct answer: B**

**Explanation:** The right frame is how much a decision changes as a result of your input, and whether there is time. Item 1 scores highest on both, and it has a multiplier the others lack: a pattern decided once and reused eight times embeds either a good decision or a bad one eight times over, and the cost of changing it later rises with every journey that adopts it. Item 2 matters and has persisted for months, so deferring costs comparatively little, though a 32% error rate is serious and should be next. Item 3 has no deadline pressure. Item 4 is weakest, since minor copy changes rarely justify revisiting a screen. Option A ranks by current scale and misses the compounding effect of a reused pattern, which is precisely the strategic reasoning your role names.

**Question 5 (moderate) — Risk reasoning about a component**

A team proposes replacing a standard date input with a calendar picker, arguing it prevents invalid dates. The service asks for dates of birth, often decades in the past, and serves a wide public audience. What is the most complete analysis?

- A) Calendar pickers prevent invalid dates, so it is an improvement.
- B) A picker is well suited to choosing a near-future date and poorly suited to a date of birth, where a user must navigate back decades; it also adds a custom control that must work with keyboard, screen readers, voice and zoom — so the change increases effort for the common case and adds accessibility and maintenance risk, while the invalid-date problem it solves is better handled by accepting varied formats and validating clearly.
- C) It is fine if it is tested with screen reader users.
- D) Date pickers should never be used.

**Correct answer: B**

**Explanation:** The strongest analysis identifies why the control is mismatched to this specific task, not just that pickers carry risk. A calendar picker optimises for selecting a date near today, which is why it works for booking an appointment; entering 14 March 1957 through one means navigating back several hundred months. Meanwhile every custom picker must be built and maintained to work with keyboard, assistive technology, voice control and zoom, and the failure modes are easy to ship and hard to detect. Option B also names the better answer to the underlying concern: invalid dates are addressed by accepting the formats people type and validating with a clear, specific message. Option A accepts the stated benefit without weighing the cost. Option C treats testing as a substitute for a design decision. Option D states a rule without reasoning and would be wrong for a booking journey.

**Question 6 (moderate) — Strength of a finding**

Ten of fourteen participants failed to notice a "save and return" link. Which conclusion is best supported?

- A) 71% of users do not notice the link.
- B) Discoverability of the link is a substantial problem, evidenced across most participants, warranting design work and a follow-up measure of whether the change helps.
- C) The link should be moved to the top of the page.
- D) The link is invisible.

**Correct answer: B**

**Explanation:** Ten of fourteen is a strong qualitative signal, strong enough to act on, and B states it at that strength while specifying what acting looks like. Option A converts fourteen participants into a population rate, the commonest overreach in design reporting. Option C prescribes one solution when the cause could be position, wording, visual weight, or a mental model in which people do not expect to leave a form partway — and each implies a different fix, with different costs. Option D overstates: participants did not notice the link, which is different from the link being invisible, and the distinction matters because "not noticed" can be a hierarchy problem while "invisible" would be a contrast or rendering problem. Note that B builds in the follow-up measurement, which is what turns a finding into a change you can defend.

**Question 7 (moderate) — Designing under a constraint**

A service must let users provide a document. Users are predominantly over 75 and many are not confident online. The team proposes a smartphone-only photo upload because it is simplest to build. What is the strongest analysis?

- A) The team is right; most people have smartphones.
- B) Smartphone-only upload assumes a suitable phone, data, somewhere appropriate to photograph a document, and the confidence to do it — assumptions failing disproportionately in this group, so the design would exclude a substantial share of the service's core users; the useful next step is to establish how many, and to identify an alternative such as post or assisted digital.
- C) The team should add a postal route.
- D) The team should test the upload with older users first.

**Correct answer: B**

**Explanation:** The strongest analysis names the mechanism and its scale. A smartphone-only upload bundles four assumptions, each failing more often in this population than in the general one, and because the affected group is the core user base rather than an edge case, the exclusion is the main case. Option B also proposes the two things that move the conversation: quantifying the affected group, which turns a concern into something a plan can weigh, and naming an alternative. Option A treats a majority statistic as sufficient, which is the reasoning that produces inaccessible public services. Option C offers a good solution without the analysis that would justify it, and unsupported solutions get overruled. Option D is a sensible research step that does not address the current decision, which is to offer no alternative at all.

**Question 8 (harder) — Scoping a flaw**

A study you are relying on used a prototype whose "back" function was broken. Four findings: (i) participants could not locate the eligibility criteria; (ii) participants abandoned after a wrong turn; (iii) tasks took longer than expected; (iv) participants misread the declaration wording. Which findings are compromised?

- A) All four.
- B) None; it was a minor fault.
- C) Findings (ii) and (iii) are directly compromised, because inability to go back plausibly caused both, while (i) and (iv) concern comprehension of content and are largely unaffected.
- D) Only finding (ii).

**Correct answer: C**

**Explanation:** The skill is scoping a flaw precisely rather than treating it as total or trivial. A broken back function prevents recovery from a wrong turn, directly manufacturing both abandonment and inflated task times, so (ii) and (iii) cannot be separated from the artefact. Findings (i) and (iv) concern whether participants could find and understand content, which the fault does not touch. Option A discards two sound findings. Option B leaves two manufactured findings in circulation, where they will justify changes to problems that do not exist. Option D catches the obvious compromise and misses the duration one. Being able to say what a team can still rely on is more useful than either wholesale condemnation or wholesale acceptance — and, in a team, condemning everything teaches people to stop mentioning prototype faults.

**Question 9 (harder) — Spotting the opportunity**

Analytics show that 40% of users who abandon at the upload step return within seven days and complete. The team treats the 40% as a success and focuses on the 60% who do not. What is the strongest observation?

- A) Agree; the 60% is the real problem.
- B) The 40% are also evidence of a problem — they are making two or more attempts at something that should take one — and they are a natural experiment: something enabled them to come back and succeed, and identifying it is likely the fastest route to helping the 60% too.
- C) The 40% should be excluded from the drop-off figure.
- D) Send reminders to everyone who abandons.

**Correct answer: B**

**Explanation:** This is opportunity reasoning, which your role names explicitly. The team has read a number as a success because it ends well, and missed that a returning user is a user who could not finish first time — almost always because a document was not to hand. That is an interaction design problem with an interaction design answer: tell people what they will need before they start, and make saving and resuming genuinely easy and discoverable. The more valuable half of option B is the natural experiment: something let the returners come back, and whether it was a saved session, an email, or simply remembering the URL, knowing which tells you what to build. Option A accepts the framing. Option C would conceal the phenomenon. Option D leaps to one intervention without the cause.

**Question 10 (harder) — A local optimisation**

A team reports success because time on a form page fell from 90 to 55 seconds after content was removed. Over the same period, contact centre calls about that step rose 25% and completion was unchanged. What is the strongest analysis?

- A) The redesign succeeded on its metric; the calls need separate investigation.
- B) The pattern is consistent with content having been removed that users needed, pushing them to telephone for the explanation — an apparent efficiency that is probably a cost transfer, with unchanged completion suggesting no benefit to users at all; the right measure is end-to-end effort including contact.
- C) The call increase must have another cause.
- D) Report both metrics without interpretation.

**Correct answer: B**

**Explanation:** Three facts fit together: the page got shorter, calls rose sharply, and completion did not move. The most economical explanation is that removed content is content users now obtain by telephone, so the time saving has been transferred rather than realised — and the unchanged completion is the decisive detail, because a genuine improvement should have moved it. Option B names the mechanism and the measurement error underneath: optimising one step while ignoring what happens around it is exactly the failure your discipline exists to catch, and it will recur as long as the metric is scoped to the page. Option A accepts a metric because it was agreed, which is how services get locally optimised into worse wholes. Option C asserts an alternative cause without evidence. Option D abdicates the interpretation your role exists to supply.

**Question 11 (harder) — A constraint that may not be one**

A developer states that a field cannot accept a value longer than 30 characters "because of the API". Research shows around 8% of users have addresses or names longer than this and are forced to truncate. What is the most productive line of enquiry?

- A) Accept the constraint and add a character counter.
- B) Ask where the 30-character limit comes from — the API, the database, or a form validation rule somebody wrote — and whether the underlying system genuinely rejects longer values or simply truncates them, since the answer determines whether this is a hard constraint, a data quality problem, or an assumption nobody has revisited.
- C) Insist the limit is removed.
- D) Ask users to abbreviate.

**Correct answer: B**

**Explanation:** "Because of the API" is a compressed claim that could mean several different things, and the productive move is to find out which. If the API genuinely rejects longer values, the constraint is real and the design problem becomes how to help people truncate gracefully and correctly. If it silently truncates, you have a data quality problem in which 8% of records are wrong and nobody knows. If the limit is a validation rule somebody added years ago, it can be changed. Option B distinguishes those cases, which is the whole question. Option A accepts the constraint and adds a counter, which tells users they are being cut off without helping them decide what to lose. Option C asserts without understanding, and a designer who treats every constraint as negotiable is not believed about the ones that are. Option D transfers the problem to users.

**Question 12 (harder) — A flaw in your own work**

Three weeks after a design decision you supported, you realise the research behind it recruited only users who had previously completed the service successfully. What should you do?

- A) Note it as a limitation in the next report.
- B) Tell the team and the decision-makers now, scope precisely which conclusions are affected and which still stand, and propose targeted follow-up with users who did not complete — since those are the people the study could not see and the ones the design most needs to serve.
- C) Quietly commission follow-up and correct the record if findings differ.
- D) Say nothing; the decision was reasonable anyway.

**Correct answer: B**

**Explanation:** A sample of successful completers cannot see the failures the design was meant to address, and a decision has already been made on it. Option B does the three things that matter: it tells the people who acted on the finding, it scopes the damage precisely rather than minimising or catastrophising, and it proposes the fix. The scoping matters — conclusions about how successful users navigate the journey may remain perfectly sound, and saying so is accuracy rather than defensiveness. Option A defers disclosure past usefulness. Option C conceals a known flaw while the team builds on it. Option D is least defensible: reasoning that the decision was probably fine substitutes your guess for the evidence you were relying on, and if it emerges later the concealment is what people will remember.

### Preparation tips

- **Follow consequences beyond the first order.** Removing content does not remove the need for it.
- **Ask who could not have appeared in this data.** Sampling frame exclusions are the highest-yield question against any evidence.
- **Scope flaws precisely.** Say which claims a fault compromises and which survive.
- **Ask what a control is optimised for.** A picker suits near dates; a dropdown suits long lists; neither suits everything.
- **Watch for metrics moving in opposite directions.** A local optimisation is usually a cost transfer.
- **Ask what a constraint actually is.** "Because of the API" has at least three distinct meanings.
- **Weight patterns by reuse.** A decision reused eight times is worth eight times the attention.
- **Read the stem's final sentence twice.** Items often ask something narrower than the scenario implies.

### Common pitfalls to avoid

- **Converting participants into percentages.** "Ten of fourteen participants" must never become "71% of users".
- **Treating effect size as causal certainty.** A 29 point gap can be entirely confounded.
- **Missing absent requirements when auditing.** What is not there is systematically harder to see.
- **Applying a standard as you would have written it.** Assurance means applying it as written.
- **Accepting a metric because it is the agreed one.** Agreed metrics get locally optimised into worse services.
- **Reading a partially satisfied compound exception as satisfied.** "Like-for-like and low risk" requires both.
- **Treating testing as a substitute for a design decision.** Testing tells you whether something works, not whether to choose the harder thing.
- **Prescribing the fix instead of establishing the problem.** It forecloses better options.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A numeric reasoning assessment measures how accurately you handle the quantitative material your role produces and consumes. At your level the emphasis shifts from calculating to interrogating. You will still need to compute rates correctly, but the harder items ask whether a figure means what somebody claims — which is, not coincidentally, the question you are often the only person in the room positioned to ask.

The format is typically a timed online test of fifteen to thirty minutes, each item presenting a table, chart or short paragraph of figures with a multiple-choice question. Calculators are usually provided and the arithmetic is deliberately tractable. Time per item is tight, so the operative skill is locating what matters and disregarding what does not.

There is a professional stake worth naming. Quantitative evidence carries unearned authority: a number in a slide is treated as fact and a design argument as a preference, regardless of the rigour behind either. Designers who cannot interrogate numbers confidently lose arguments they should win, and occasionally win arguments they should lose. Being the person who asks "what is the denominator, and who could not have appeared in this data?" is a substantial part of the value you add — and your role's requirement to align design work to organisational objectives frequently comes down to whether you can engage with the numbers those objectives are expressed in.

Four habits carry the load. Establish what the question asks before looking at the data. Identify the denominator and the population it represents before calculating. Estimate, calculate, compare. And sanity-check against the world.

Distractors are built from a predictable catalogue: wrong denominator, percentage confused with percentage point, new value used as the base in a percentage change, rates averaged without weighting, raw counts compared across unequal groups.

### How this assessment maps to your role

The numerical skills tested map onto your named skills:

- **Reading analytics accurately** maps to **Evidence-based design**, where you analyse, synthesise and clearly explain evidence such as web analytics data.
- **Comparing rates between groups and devices** maps to **Designing for everyone**, where a gap is often the first numerical trace of exclusion.
- **Measuring whether an iteration worked** maps to **Iterative design**.
- **Quantifying risk and opportunity** maps to **Designing strategically**, where identifying risks requires knowing how many people are involved.
- **Explaining figures at defensible strength** maps to **Design communication**.
- **Interrogating others' claims** maps to **Designing together**, where you give and receive constructive feedback — including on evidence.

### Practice questions

**Question 1 (easy) — Error rate**

Of 4,800 users who reached a page, 1,200 triggered a validation error on one field. What percentage?

- A) 20%
- B) 25%
- C) 30%
- D) 40%

**Correct answer: B**

**Explanation:** 1,200 ÷ 4,800 = 0.25, so 25%, and the answer is B. Estimate first: 1,200 of 4,800 is a quarter. Options A and C come from dividing by 6,000 and 4,000. A quarter of everyone reaching a page failing one field is a serious signal, and it points almost always at format, label or hint rather than at users — people do not collectively become careless at a single input, and if they appear to, the input is telling them something wrong.

**Question 2 (easy) — Drop-off against the right base**

A page is reached by 6,000 users and passed by 4,500. What is the drop-off rate?

- A) 25%
- B) 33%
- C) 75%
- D) 30%

**Correct answer: A**

**Explanation:** The drop-off is 6,000 − 4,500 = 1,500, measured against arrivals: 1,500 ÷ 6,000 = 0.25, giving A. Option B is 1,500 ÷ 4,500, dividing by those who continued — the most common error in page analytics and one that overstates every drop-off it touches. The rule: drop-off is measured against arrivals. This matters most when ranking pages by where to focus, because two pages computed with different denominators can invert the ranking, and at your level you are frequently the person producing that ranking for a team.

**Question 3 (easy) — Comparing devices**

| Device | Users | Completed |
|---|---|---|
| Desktop | 9,000 | 7,650 |
| Mobile | 15,000 | 9,000 |
| Tablet | 1,500 | 1,275 |

Which device has the lowest completion rate, and how many users does it lose?

- A) Mobile, 60% rate, 6,000 users lost
- B) Desktop, 85% rate, 1,350 users lost
- C) Mobile, 40% rate, 9,000 users lost
- D) Tablet, 85% rate, 225 users lost

**Correct answer: A**

**Explanation:** Rates are desktop 7,650 ÷ 9,000 = 85%; mobile 9,000 ÷ 15,000 = 60%; tablet 1,275 ÷ 1,500 = 85%. Mobile is lowest and loses 15,000 − 9,000 = 6,000 users. So A. Option C inverts rate and loss. Note the design inference the table supports: desktop and tablet perform identically at 85%, and tablets have the same content on a large screen, which strongly suggests the problem is specific to small screens rather than to the content or the task. That is a much more useful conclusion than "mobile is worse", because it points at layout, touch targets, viewport behaviour and keyboard type rather than at wording.

**Question 4 (easy) — Centre and spread**

Nine participants took these times in seconds to complete a step: 15, 18, 20, 22, 25, 28, 30, 35 and 210. Which summary is most defensible?

- A) Mean 44.8 seconds
- B) Median 25 seconds, range 15 to 210, with the 210-second case described separately
- C) Median 25 seconds
- D) Mean 44.8 seconds, range 15 to 210

**Correct answer: B**

**Explanation:** The mean of about 44.8 exceeds eight of the nine observations, so it represents almost nobody. The median is the fifth value, 25 seconds, which describes the group well. But the median alone conceals a session lasting more than eight times the typical duration, which is almost certainly the most informative observation — something on that step defeated one participant entirely, and finding out what is the point of watching. Option B gives centre, spread and explicit treatment of the outlier. Option D pairs the range with a misleading centre. Option C buries the extreme case. The rule to enforce in your own reporting: a central figure never travels alone.

**Question 5 (moderate) — Did the change work?**

Before: 1,080 of 1,800 users completed a step without error. After: 1,470 of 2,100 completed without error. Did it improve, and by how much in percentage points?

- A) Yes, by 390 users
- B) Yes, by 10 percentage points
- C) Yes, by 14 percentage points
- D) No, the rate fell

**Correct answer: B**

**Explanation:** Convert to rates because the totals differ. Before: 1,080 ÷ 1,800 = 60%. After: 1,470 ÷ 2,100 = 70%. The improvement is 10 percentage points, giving B. Option A compares raw counts across different-sized groups, which is meaningless here — more users succeeded partly because more arrived, and crediting the design with the whole increase would be wrong. This is exactly the comparison your role requires when iterating across successive rounds, and the trap is common in real reporting: "390 more people got it right" sounds like a win and could conceal a fall in the rate if traffic rose faster than successes.

**Question 6 (moderate) — Comparing groups**

Of 1,200 users under 65, 1,020 completed online. Of 400 users over 65, 120 completed. What is the gap in percentage points?

- A) 30
- B) 45
- C) 55
- D) 85

**Correct answer: C**

**Explanation:** Under-65s: 1,020 ÷ 1,200 = 85%. Over-65s: 120 ÷ 400 = 30%. The gap is 55 percentage points, giving C. Options A and D are the two group rates offered as if they were the gap — a distractor pattern worth recognising, since numbers from your working frequently appear among the options. A gap this size would justify immediate investigation, and for an interaction designer the suspects are specific and checkable: touch target size, contrast, whether the layout requires horizontal scrolling at 200% zoom, whether error summaries appear above the fold, whether the journey depends on a capability the group is less likely to have.

**Question 7 (moderate) — Percentage change**

Weekly validation errors on a field fell from 1,500 to 1,125 after a change. What is the percentage decrease?

- A) 20%
- B) 25%
- C) 33%
- D) 75%

**Correct answer: B**

**Explanation:** The difference is 375, and 375 ÷ 1,500 = 0.25, so a 25% decrease, giving B. Option C is 375 ÷ 1,125, dividing by the new figure. Option D is the new figure as a proportion of the old, a true statement answering a different question and a distractor built to catch people who calculate correctly and mismatch the answer to the stem. The rule: for percentage change, the denominator is always where you started.

**Question 8 (moderate) — Quantifying an exclusion**

A service receives 720,000 submissions a year. A control you are considering would exclude users without JavaScript, currently around 1.5% of sessions. How many people a year would be affected?

- A) 1,080
- B) 10,800
- C) 11,000
- D) 108,000

**Correct answer: B**

**Explanation:** 1.5% of 720,000 is 0.015 × 720,000 = 10,800, giving B. Option A is 1.5% of 72,000 and option D is 15%. The reason this belongs in a design guide rather than a maths one is what it does to a conversation: "1.5% of sessions" sounds negligible, and "10,800 people a year unable to complete this" does not. Converting a percentage into people takes five seconds and is the most effective move available when arguing against a control that quietly requires a capability. It is also worth remembering that the 1.5% is not a fixed population — it includes people on flaky connections where a script failed to load, which is why the argument is about robustness rather than about a small identifiable group.

**Question 9 (moderate) — Choosing the denominator**

A journey shows 40,000 start, 32,000 pass eligibility, 19,200 reach the declaration, 17,280 submit. What proportion of those who reached the declaration went on to submit?

- A) 43%
- B) 54%
- C) 60%
- D) 90%

**Correct answer: D**

**Explanation:** The stem names users who reached the declaration, so the denominator is 19,200 and the part is 17,280: 17,280 ÷ 19,200 = 0.9, giving D. Option A uses 40,000, option B uses 32,000, option C is the eligibility-to-declaration rate. All four are true and one answers the question. Strategically the funnel also tells you where to look: 8,000 lost at eligibility, 12,800 between eligibility and declaration, and 1,920 at submission. A proposal to redesign the submission page would need a very strong reason, and being able to establish that in fifteen seconds is what lets you redirect a conversation in the meeting rather than a week later.

**Question 10 (harder) — A metric that hides a split**

Time on a page averages 50 seconds. Your sessions showed participants either glancing for a few seconds or reading carefully for two to three minutes. What is the most useful response?

- A) The average is wrong.
- B) The average is probably correct and uninformative: it sits between two clusters and describes neither, so ask for the distribution — which will show whether the page has two audiences behaving differently, and each would need a different design response.
- C) The participants were unrepresentative.
- D) The page should be shorter.

**Correct answer: B**

**Explanation:** When behaviour splits into two clusters the mean lands in the gap and describes nobody. Fifty seconds is entirely consistent with half the users spending five seconds and half spending two and a half minutes, and those are different design problems: people glancing may be skipping content they need, while people reading carefully may be struggling with it. Option B asks for the distribution — the most useful request you can make of an analytics colleague — and names why it matters, which is that the two groups need different responses and a single change may help one while harming the other. Option A disputes a figure that is probably correct. Option C blames the research. Option D leaps to a solution that could harm the careful readers.

**Question 11 (harder) — Percentage points and relative change**

Error-free completion rose from 45% to 54% after a redesign. Which statement is accurate?

- A) A 9% increase.
- B) A 9 percentage point increase, equivalent to a 20% relative increase.
- C) A 20 percentage point increase.
- D) A 16.7% increase.

**Correct answer: B**

**Explanation:** The arithmetic gap is 54 − 45 = 9 percentage points. The relative increase is 9 ÷ 45 = 0.2, or 20%. Option B labels both correctly. Option A is ambiguous and generally read as relative. Option C misapplies the percentage-point label. Option D divides by the new value. The professional stake is real: "error-free completion rose 20%" and "rose 9 percentage points" describe the same change, and one will appear in whichever document needs it to sound larger. Being the person who calmly asks for both is a cheap way to be trusted with numbers, and it costs nothing in goodwill if you make it a convention rather than a challenge.

**Question 12 (harder) — What a small comparison can establish**

Your team wants to know whether a redesign improved completion. Baseline is 60%, and a 6 percentage point improvement would be meaningful. A colleague proposes 25 moderated sessions before and 25 after. What is the strongest response?

- A) Agree; 50 sessions is substantial.
- B) Explain that a 6 point difference on 25 per group is between one and two participants and well inside ordinary variation, so the comparison cannot detect it — recommend measuring the rate with live analytics across all users, and spending the 50 sessions on understanding mechanisms, which moderated research does uniquely well.
- C) Increase to 40 per group.
- D) Run it and report the difference with caveats.

**Correct answer: B**

**Explanation:** Twenty-five per group cannot distinguish a six point difference from chance; detecting a difference that small reliably needs hundreds per group. Option B says so and redirects rather than merely objecting: analytics can measure the rate across the whole user base at negligible marginal cost, while moderated sessions are the only instrument that explains why a rate is what it is. That division of labour is the substantive recommendation. Option A endorses a design that cannot answer its own question. Option C moves towards adequacy without approaching it. Option D is the most damaging, because a reported difference from an underpowered comparison invites the team to act on noise, and caveats do not travel — the number does, and it will be cited next year by someone who never saw the caveat.

### Preparation tips

- **Find the denominator and the population before calculating.**
- **Measure drop-off against the number who arrived.** Not the number who continued.
- **Convert percentages into people.** "1.5% of sessions" and "10,800 people a year" are the same fact; one wins arguments.
- **Convert to rates before comparing anything.**
- **Ask for the distribution.** Most misleading metrics are correctly calculated and wrongly interpreted.
- **Look for what two similar groups tell you.** Desktop and tablet behaving identically localises the problem to small screens.
- **Know what samples can detect.** Twenty-five per group cannot see six points.
- **Practise on your own service's numbers.** Calculate the error rate on a real field and the loss at every page.

### Common pitfalls to avoid

- **Dividing by the wrong total.** Funnel items are built around this.
- **Comparing raw counts before and after a change.** Traffic changes too.
- **Confusing percentages with percentage points.** Both are correct labels for different quantities.
- **Accepting a mean without checking for clusters.** Bimodal behaviour hides entirely behind an average.
- **Reporting a number from your working as though it answered the question.**
- **Endorsing an underpowered comparison.** Acting on noise is worse than acting on nothing.
- **Leaving a percentage as a percentage.** People do not feel percentages.
- **Treating a capability-dependent minority as fixed.** Users without JavaScript include people whose script failed to load.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A verbal reasoning assessment measures how accurately you read. In a role that runs on documents — standards, accessibility criteria, component specifications, technical constraints, content guidance — reading accuracy is the substrate everything else rests on. A misread criterion produces a design that fails an audit; a misread finding produces a design that fails a user.

The classic format presents a short passage of dense workplace prose, typically three to six sentences, followed by statements to classify as True, False or Cannot Say. True means the statement follows necessarily. False means the passage contradicts it. Cannot Say means the passage neither establishes nor excludes it. Alongside these come comprehension questions, main-point questions, and items asking which of four summaries is most accurate.

The governing rule is that you answer from the passage alone. Your professional knowledge must be set aside entirely — and this becomes harder, not easier, with experience. The more accessibility criteria you have read, the more readily you supply the clause you expect and feel confident doing it. That is the characteristic error at your level, and it needs a mechanical counter-habit: before marking anything True, put your finger on the words.

Cannot Say deserves particular attention because people avoid it. It feels evasive, so candidates reach for True or False to appear decisive. In practice Cannot Say is frequently correct. The diagnostic: if you are filling a gap with knowledge or inference, however reasonable, the answer is Cannot Say.

Small words carry the meaning. "All" is not "most". "May" is not "must". "Should" is not "will". "Encouraged" is not "required". "Consider whether" is not "recommend". "Unless", "provided that" and "solely" govern everything around them.

There is a specific payoff for an interaction designer. A great deal of poor practice comes from remembering the gist of a criterion rather than its wording, which produces both over-compliance that wastes effort and under-compliance that excludes people. Reading precisely is how you tell the two apart.

### How this assessment maps to your role

The verbal skills tested map onto your named skills:

- **Reading precisely** maps to **Designing for everyone**, where you ensure a design meets appropriate standards such as accessibility regulations.
- **Separating statement from inference** maps to **Evidence-based design**.
- **Identifying the main point** maps to **Design communication**, where you clearly explain problems and design ideas to others.
- **Handling qualified language** maps to **Designing strategically**, where constraints in technology and policy shape design and where knowing which are hard tells you where design can move.
- **Reading for absence** maps to **Designing for everyone**, where noticing that a specification never mentions keyboard operation has a direct consequence.
- **Reading feedback accurately** maps to **Designing together**, where you give and receive constructive design feedback.

### Practice questions

*Passage A — for Questions 1 to 4*

"All new public-facing services must use components from the Design System where a suitable component exists. Where no suitable component exists, teams may create a new one, provided it is documented and tested with assistive technology before live use. Components created before this policy took effect must be reviewed within 12 months. Teams are encouraged, but not required, to contribute new components back to the Design System."

**Question 1 (easy)** — Statement: "Teams must contribute new components back to the Design System." True, False or Cannot Say?

**Correct answer: False**

**Explanation:** The passage says teams are *encouraged, but not required*, to contribute back. The statement's "must" contradicts that explicitly, so False. This is the clearest form of the pattern — an explicit removal of an obligation sitting alongside hard requirements elsewhere in the same passage, which is why skimming for general tone produces errors in both directions.

**Question 2 (moderate)** — Statement: "A team that creates a new component without testing it with assistive technology has breached the requirements." True, False or Cannot Say?

**Correct answer: True**

**Explanation:** The passage permits creating a new component *provided it is documented and tested with assistive technology*. Those are conditions on the permission, and failing one means the permission does not apply, so the requirement is breached. True. Note the contrast with Question 1: there the passage explicitly removed an obligation; here it attached conditions to a permission, and failing a condition is a breach. Distinguishing an explicit exemption from a conditional permission transfers directly to reading real standards, where teams frequently assume the first when they are looking at the second.

**Question 3 (moderate)** — Statement: "A component created three years ago must have been reviewed by now." True, False or Cannot Say?

**Correct answer: Cannot Say**

**Explanation:** Components created before the policy took effect must be reviewed within 12 months, but the passage never says when the policy took effect. If it took effect three years ago a review would be overdue; if six months ago it would not. Because the fact you would need is absent, Cannot Say. Whenever a passage sets a deadline relative to a commencement, check whether the commencement date is given. Its absence is deliberate and recurs throughout this section.

**Question 4 (harder)** — Statement: "A team may use a custom component that has been documented but not yet tested with assistive technology, provided testing happens before the service goes live." True, False or Cannot Say?

**Correct answer: True**

**Explanation:** Read the condition precisely: the requirement is that the component is documented and tested with assistive technology *before use in a live service*. That wording locates the deadline at live use, not at creation, so a component that exists in a prototype but has not yet been tested is not in breach provided testing happens before launch. The statement describes exactly that, so it is True. Candidates who mark this False are reading the requirement as attaching to creation, which is a natural but incorrect reading of "may create a new one, provided...". This distinction matters practically: it is the difference between a rule that blocks exploration and one that blocks launch, and reading it the strict way would prevent teams from prototyping ideas they are entitled to explore.

*Passage B — for Questions 5 to 8*

"The review of the application form found that users on mobile devices completed more slowly than desktop users and were more likely to abandon at the document upload step. The review notes that mobile users differed from desktop users in age and in whether they were completing the form at home. The review did not assess whether abandoned applications were later completed on another device. It recommends that the team consider whether a redesigned upload step would reduce mobile abandonment."

**Question 5 (easy)** — Statement: "Mobile users were more likely to abandon at the upload step." True, False or Cannot Say?

**Correct answer: True**

**Explanation:** The first sentence states this directly and the statement restates it without addition. True. Note the passage's careful "more likely to abandon" rather than "usually abandon", and the statement respects it. Answer quickly and bank the time for harder items.

**Question 6 (moderate)** — Statement: "The mobile interface causes abandonment at the upload step." True, False or Cannot Say?

**Correct answer: Cannot Say**

**Explanation:** The passage reports an association and names two ways the groups differed: age, and whether they were at home. Either could explain it — someone away from home is less likely to have documents to hand, which produces upload abandonment regardless of interface quality. The passage neither asserts nor excludes an interface cause, so Cannot Say. The design consequence is direct and worth holding: if the interface is the cause you redesign it; if the cause is location, the answer is saving and returning, or setting expectations before the journey starts. Treating the association as a cause is how a team spends a quarter improving the wrong thing.

**Question 7 (moderate)** — Statement: "Users who abandoned on mobile did not complete the application." True, False or Cannot Say?

**Correct answer: Cannot Say**

**Explanation:** The passage says explicitly that the review did not assess whether abandoned applications were later completed on another device. Declared silence establishes nothing, so Cannot Say. This item rewards noticing that the intuitive reading is wrong in a consequential way: abandonment on one device may be a user sensibly switching to a laptop where their documents are, which is a mild inconvenience rather than a service failure. Not knowing which changes how urgent the problem is, and the reviewers flagged the gap rather than letting readers assume.

**Question 8 (harder)** — Statement: "The review recommends redesigning the upload step." True, False or Cannot Say?

**Correct answer: False**

**Explanation:** The review recommends that the team *consider whether* a redesign would reduce abandonment — a recommendation to evaluate, including the possibility of concluding it would not help. The statement asserts a recommendation to redesign, which was not made, so it is False rather than Cannot Say: the passage tells you what was recommended and it was something different. This pervades real review documents and produces a familiar sequence in which a recommendation to consider becomes a commitment to deliver, is tracked, and is reported against without anyone having decided it was right.

*Passage C — for Questions 9 to 12*

"Interactive components must be operable using a keyboard alone. Where a component uses a non-standard interaction, the team must provide a documented keyboard alternative. Focus must be visible at all times. Where a component displays an error, the error must be programmatically associated with the field it relates to; a visual association alone is not sufficient. These requirements apply to components in public-facing services and to components in internal tools used by more than fifty staff."

**Question 9 (easy)** — Statement: "A visual association between an error and its field is sufficient." True, False or Cannot Say?

**Correct answer: False**

**Explanation:** The passage states that a visual association alone is not sufficient and that the error must be programmatically associated. The statement contradicts this directly, so False. The word doing the work is "programmatically", and skimming past it produces exactly the failure the requirement exists to prevent: a message next to a field is obvious to a sighted user and may be entirely absent for someone whose screen reader encounters fields and messages in markup order.

**Question 10 (moderate)** — Statement: "These requirements apply to an internal tool used by twelve staff." True, False or Cannot Say?

**Correct answer: Cannot Say**

**Explanation:** The final sentence extends the requirements to internal tools used by more than fifty staff. A tool used by twelve does not meet that threshold, so the extension does not apply — but the passage does not say the requirements are *excluded* for smaller tools, only that they apply to public services and to larger internal tools. Silence about the twelve-user case leaves it undetermined, so Cannot Say rather than False. This is a genuinely fine distinction and a common one in scoping clauses: stating where a rule applies is not the same as stating where it does not, and a reader who converts the first into the second will confidently tell a team they are exempt when nobody has said so.

**Question 11 (harder)** — Statement: "A component with a non-standard interaction breaches the requirements." True, False or Cannot Say?

**Correct answer: False**

**Explanation:** The passage does not prohibit non-standard interactions; it requires that where one is used, a documented keyboard alternative is provided. So a non-standard interaction with such an alternative complies, and the statement — asserting a breach from the interaction alone — is contradicted. False. This is a standard setting a condition rather than a prohibition, and reading it as a prohibition produces two bad outcomes: teams avoid legitimate solutions unnecessarily, or conclude the rule is unrealistic and ignore it. Both are worse than the accurate reading, which is that unusual interactions are permitted and carry an obligation.

**Question 12 (harder) — Main point**

Which best captures the main point of Passage C?

- A) Components must never use non-standard interactions.
- B) Components in public services and larger internal tools must remain operable and comprehensible for someone not using a mouse or not seeing the screen — through keyboard operation, visible focus, documented alternatives for unusual interactions, and errors associated in code rather than only visually.
- C) Focus must be visible at all times.
- D) Errors must be programmatically associated with their fields.

**Correct answer: B**

**Explanation:** The main point must span the passage while adding nothing. Option A overstates a conditional requirement into a prohibition. Options C and D are each true of one clause and silent on the rest. Option B captures all four requirements, the scope clause, and the logic joining them: each requirement exists so the component works for someone who is not using a mouse or not seeing the screen. Note that B is the only option that mentions scope at all, which matters because a summary omitting it would imply the requirements are universal. Main-point items reward the option broad enough to cover everything and disciplined enough to invent nothing.

### Preparation tips

- **Point at the words.** Before marking True, identify the phrase that makes it true. Experience makes this harder, not easier.
- **Trust Cannot Say.** If you are supplying a link, that is the diagnostic.
- **Circle every qualifier.** All, some, may, must, should, encouraged, unless, provided that, solely, more than.
- **Locate the deadline in a condition.** "Before live use" is not "before creation".
- **Distinguish stating where a rule applies from stating where it does not.** Scoping clauses invite that confusion deliberately.
- **Look for the missing fact.** Some items are Cannot Say because a commencement date was never given.
- **Treat declared silence as silence.**
- **Practise on real criteria.** Take an accessibility requirement and write three statements — one True, one False, one Cannot Say.

### Common pitfalls to avoid

- **Answering from professional knowledge.** The characteristic error at your level.
- **Avoiding Cannot Say.** It converts good reading into wrong answers.
- **Reading "encouraged" as "required".**
- **Reading a condition as a prohibition.** "Where X, do Y" permits X.
- **Skimming a load-bearing adverb.** "Programmatically" changes the whole requirement.
- **Converting a scope statement into an exemption.** Silence about a case is not permission.
- **Treating association as causation.** A passage naming confounds is warning you off.
- **Reading "consider whether X" as "recommend X".**

## Workplace job-specific situational judgement assessment

### About this assessment

A situational judgement assessment presents realistic workplace scenarios and asks what you would do. There is no passage to parse and no arithmetic. You get a dilemma of the kind your role produces, four or five candidate responses, and a question asking which is most effective and often which is least.

This section measures whether your judgement matches what the profession considers good practice at your level. Your role description places you as a confident, competent designer trusted to make good decisions, who recognises when to ask for further guidance, contributes to design concepts, plans and runs design sessions, engages the right people, and gives and receives constructive feedback. The strongest answers involve exercising real professional judgement, holding a position under pressure when the evidence warrants it, and knowing which decisions genuinely belong to someone else.

That last point distinguishes your level from a junior one. A junior designer escalates a technical constraint. You are expected to have the conversation, understand the constraint, and escalate only what genuinely needs authority you do not hold — accessibility blockers close to launch, decisions that commit the organisation, and anything where being too close to the work compromises your judgement.

Four principles carry most scenarios.

Users come first, and specifically the users who cannot get past something. An interaction that excludes one group is not slightly worse for them; it is unusable.

Protect the integrity of the design rationale. You are the person expected to say what the evidence supports, including when it is inconvenient. Options that inflate, soften or mislabel findings are close to automatically wrong, however reasonable the motive.

Address problems directly, early, with the person involved. Private, specific, non-accusatory conversation beats public correction, silence, or routing around someone.

Fix the instance, then the system. At your level, noticing that one broken error summary means a broken template — and doing something about the template — is a marker of the seniority you are working towards.

### How this assessment maps to your role

The judgement dimensions map onto your named skills:

- **Explaining and defending design decisions** maps to **Design communication**.
- **Protecting inclusion** maps to **Designing for everyone**, where you ensure designs meet appropriate standards and work for all users.
- **Running sessions and engaging the right people** maps to **Designing together**, where you effectively plan and run a design session and identify and engage the right people throughout.
- **Giving and receiving feedback** maps to **Designing together**, named in both directions.
- **Using evidence honestly** maps to **Evidence-based design**.
- **Risk, opportunity and alignment** map to **Designing strategically**, where you identify risks and opportunities and contribute to patterns and components.
- **Supporting colleagues** maps to **Leading design**, where you lead and coordinate design work with support and support other designers.

### Practice questions

**Question 1 (easy) — A design session producing one voice**

You are running a session. Twenty minutes in, two senior stakeholders dominate and the four caseworkers you invited have not spoken. What is the most effective response?

- A) Let it run; the stakeholders know the service.
- B) Change the structure — write first then round the table, or split into pairs — so quieter participants contribute without anyone being told to stop.
- C) Ask the stakeholders directly to let others speak.
- D) Follow up with the caseworkers separately.

**Correct answer: B. Least effective: A**

**Explanation:** The session is producing one perspective when you convened it for several, and structural solutions outperform confrontational ones. Writing before speaking gives quieter participants time to form a thought and gives you a legitimate reason to change who is talking, without anyone being corrected. Your role names planning and running design sessions and engaging the right people throughout — adapting the format when it is not working is the skill, not a workaround. Option A is least effective: it wastes the caseworkers' time and produces a design based on how senior people imagine the work is done, which for an interaction designer is particularly damaging because caseworkers know exactly which fields get entered wrongly and why. Option C may succeed and creates avoidable friction. Option D does not rescue this session.

**Question 2 (easy) — A shortcut proposed by a developer**

A developer says the agreed error handling will take three extra days and proposes a single generic message at the top of the page. What is the most effective response?

- A) Agree; three days is a lot.
- B) Explain what the generic message costs users — they must find the problem themselves, and someone using a screen reader may be unable to — and ask whether a middle option fits the time, such as specific messages for the two fields that fail most often.
- C) Insist on the full agreed behaviour.
- D) Escalate to your lead without talking to the developer.

**Correct answer: B. Least effective: A**

**Explanation:** The developer has a real constraint and has proposed a solution that solves their problem by transferring the cost to users. Option B makes the user cost concrete rather than appealing to a standard, treats the time constraint as legitimate, and proposes a middle path, which is usually what gets agreed. Naming the screen reader consequence matters, because "there is a problem" with no indication of where is close to unusable without sight. Option A is least effective, accepting a change that will generate confusion and repeat submissions to save three days once — and the error handling will then be inconsistent with the rest of the service, which is its own long-term cost. Option C may be right and skips the collaborative step. Option D bypasses a colleague who has not had a chance to discuss it.

**Question 3 (easy) — A defect with a template behind it**

You find that the error summary on a live page does not link to its fields. What is the most effective response?

- A) Raise a ticket for that page.
- B) Raise it with the team, describing what a keyboard user has to do, and ask whether the same defect exists on every page using the same template — since an error summary is almost certainly shared.
- C) Fix it in the prototype.
- D) Note it for the next accessibility audit.

**Correct answer: B. Least effective: D**

**Explanation:** What distinguishes a competent response here is recognising that an error summary is a shared component, so one broken instance almost certainly means every page using it is broken. Option B fixes the instance and the system in one move, and asking the question rather than asserting it leaves room for the possibility that this page is a one-off. Option A fixes one page and leaves twenty. Option C helps future builds and leaves the live defect. Option D is least effective: deferring a live accessibility defect to a scheduled audit means it persists for months, and audits are for finding things nobody noticed rather than for parking things somebody did.

**Question 4 (moderate) — Scope creep in a session**

Halfway through a session on a form journey, a stakeholder asks you to also cover a proposed new feature "since everyone's here". What is the most effective response?

- A) Cover it; it is efficient.
- B) Explain that adding an unrelated topic risks both the session's purpose and the quality of thinking on the new one, and propose a short separate session or adding it to the next with proper preparation.
- C) Refuse, since the agenda is agreed.
- D) Cover it briefly at the end if there is time.

**Correct answer: B. Least effective: D**

**Explanation:** The stakeholder's instinct is reasonable and their underlying need legitimate, so the answer is redirection rather than refusal. Adding a topic mid-session has two costs that are easy to underestimate: session time is finite, so something gets squeezed, and an unprepared topic gets thin, unstructured attention. Option B names both and offers two routes forward. Option A quietly degrades the session you convened. Option C treats an agenda as a wall rather than a reason. Option D is least effective — an unprepared topic discussed in the last ten minutes by a tired room produces conclusions too weak to use and just solid enough to be cited later as "we discussed that and agreed".

**Question 5 (moderate) — Evidence that contradicts your design**

In testing, six of nine participants clicked a secondary link instead of the primary button on a page you designed. What is the most effective response?

- A) Note the participants were unrepresentative and keep the design.
- B) Treat the result as a signal about the design, look at what drew people to the link — wording, position, visual weight, or whether it answers a question the page raised — and propose a change to test next round.
- C) Remove the secondary link.
- D) Ask for more participants before deciding.

**Correct answer: B. Least effective: A**

**Explanation:** Six of nine doing the same unexpected thing is a signal, not a coincidence, and the first move is to ask what in the design produced it. Option B does that and keeps it testable, and note the fourth possibility it lists, which designers often miss: people may click a link because the page raised a question it did not answer, in which case the fix is content and the visual hierarchy is innocent. Option A is least effective — dismissing consistent behaviour as unrepresentative participants is the most reliable way for a designer to stop learning, and it is precisely the reasoning "you are not your user" exists to prevent. Option C acts on a diagnosis you have not made. Option D delays a cheap improvement when nine participants converging is already enough to try something different.

**Question 6 (moderate) — A pattern used for the wrong purpose**

A stakeholder asks you to use the "check your answers" pattern for a page listing documents the user must still obtain, arguing it is quicker and looks consistent. What should you do?

- A) Use it; consistency matters.
- B) Explain that the pattern carries an expectation — that everything shown is done and editable — which is wrong here and will mislead users, and propose a pattern that fits "things you still need to do" while keeping the same visual style so the service stays consistent.
- C) Refuse and design from scratch.
- D) Use it but change the heading.

**Correct answer: B. Least effective: D**

**Explanation:** The stakeholder's goals of speed and consistency are legitimate, and the proposal misunderstands what a pattern is. A pattern is not a layout; it is a set of expectations users have learned, and "check your answers" teaches people that what they see is complete and changeable. Applying it to outstanding tasks tells users the opposite of the truth. Option B holds the substance and addresses both goals directly, which is what makes it persuasive rather than obstructive. Option D is least effective: changing the heading while keeping a layout whose meaning is wrong is the worst combination, because users read layout faster than words and will act on the wrong signal. Option A ships a misleading page. Option C discards the reuse that would genuinely help.

**Question 7 (moderate) — A constraint you doubt**

A developer says a field cannot accept values longer than 30 characters "because of the API", and research shows 8% of users must truncate their address. What is most effective?

- A) Accept it and add a character counter.
- B) Ask where the limit comes from — the API, the database, or a validation rule — and whether the underlying system rejects longer values or silently truncates them, since the answer determines whether this is a hard constraint, a data quality problem, or an assumption nobody has revisited.
- C) Insist the limit is removed.
- D) Ask users to abbreviate.

**Correct answer: B. Least effective: D**

**Explanation:** "Because of the API" is a compressed claim that could mean several things, and the productive move is to find out which. If the API genuinely rejects longer values, the constraint is real and the design problem becomes helping people truncate well. If it silently truncates, 8% of records are wrong and nobody knows, which is a bigger problem than the interaction. If the limit is an old validation rule, it can change. Option B distinguishes those cases. Option A adds a counter that tells users they are being cut off without helping them decide what to lose. Option C asserts without understanding, and a designer who treats every constraint as negotiable is not believed about the ones that are. Option D is least effective, transferring the problem to users and producing addresses that may not be deliverable.

**Question 8 (harder) — An accessibility blocker close to launch**

Two weeks before launch you find a custom component cannot be operated with a keyboard. Fixing it delays launch. What is most effective?

- A) Launch and add it to the backlog.
- B) Raise it immediately with the delivery manager and service owner, describe precisely what cannot be done and by whom, ask for an explicit recorded decision, and check whether a standard component could replace the custom one quickly.
- C) Attempt the fix yourself in the two weeks.
- D) Launch and publish an accessibility statement noting the gap.

**Correct answer: B. Least effective: A**

**Explanation:** A component that cannot be operated by keyboard means some people cannot use the service, and weighing a delay against an exclusion is a decision for people with authority. Raising it precisely and now is squarely yours, and the phrase "explicit recorded decision" is what makes option B a competent response rather than merely a diligent one: an unrecorded decision drifts into launch by default, and a recorded one makes the trade-off owned. The final clause adds the practical step that most often resolves this and that nobody thinks of under pressure — checking whether a standard component can substitute. Option A is least effective, because the backlog is where accessibility problems go to remain unfixed. Option D treats a statement as a way to launch with a known blocker, which it is not. Option C risks a fortnight with nobody aware.

**Question 9 (harder) — A component that is not your team's**

A shared component maintained by another team has a focus behaviour that traps keyboard users. Your service uses it. What is most effective?

- A) Work around it in your service.
- B) Report it to the owning team with a precise description and a reproduction, ask about their timeline, and meanwhile decide with your team whether to apply a local mitigation — while flagging that every service using the component is affected.
- C) Stop using the component.
- D) Fix it locally and move on.

**Correct answer: B. Least effective: A**

**Explanation:** A defect in a shared component is a defect in every service using it, which makes reporting it upstream the highest-value action available — and the precision matters, because a vague report gets triaged low while a reproduction gets fixed. Option B also handles the immediate question honestly: your users are affected now, so a local mitigation may be justified while the upstream fix is made. Option A is least effective, working around a defect silently and leaving every other service broken. Option D is better than A and still leaves the shared component wrong, and local forks of shared components are how organisations end up with six divergent versions. Option C is disproportionate unless the component is unusable and no mitigation exists.

**Question 10 (harder) — Findings the team does not want**

Research shows a component the team built over two months causes problems for nine of twelve participants. You have five minutes at the show and tell. What is most effective?

- A) Lead with the positives and mention difficulties briefly.
- B) Present what happened clearly and without blame — what participants tried, where they got stuck, what they said — and frame the next step as understanding why, inviting the team into the diagnosis.
- C) Present the failure rate starkly.
- D) Ask your lead to present it.

**Correct answer: B. Least effective: A**

**Explanation:** Difficult findings are the most valuable, and delivery determines whether they get acted on or defended against. Option B keeps the focus on observed behaviour rather than on the quality of anyone's work, and ending on a question brings the people who built it into the analysis — where a developer may know immediately why focus behaves oddly, or a content designer may recognise the wording problem. Option A is least effective: softening a nine-in-twelve failure means two months of effort continues down the same path. Option C is accurate and adversarial, and a defensive room learns nothing. Option D is understandable and deprives you of the experience and the standing.

**Question 11 (harder) — Consensus that would harm users**

The team has converged on a control everyone likes, which your evidence indicates will fail users on small screens and users with motor impairments. Reopening it reverses a decision people are relieved to have made. What is most effective?

- A) Let it go; consensus has value.
- B) Raise it once, clearly and specifically, showing what the evidence indicates will happen to those users and what a mitigation might look like — then if the team proceeds, ensure the risk is documented and propose measuring the outcome after release.
- C) Escalate to the service owner over the team's head.
- D) Keep raising it until the team changes course.

**Correct answer: B. Least effective: A**

**Explanation:** You have a professional obligation to say the thing and you also have to work with these people next week. Option B threads that: raise it once and properly, with evidence and a constructive mitigation rather than a veto; then if the decision stands, do the two things that protect users and your position — document the risk so the decision is knowing rather than accidental, and set up a measurement so reality gets a vote later. Option A is least effective, because consensus that harms users who already have fewer options is not a value, and silence makes you complicit in a decision you had the evidence to inform. Option C escalates before using the direct route and costs the team's trust. Option D substitutes persistence for persuasion, and a designer who relitigates every decision stops being heard on any of them.

**Question 12 (harder) — A flaw in your own work**

You realise that research you relied on for a design decision recruited only users who had previously completed the service. The decision is in build. What should you do?

- A) Note it as a limitation next time.
- B) Tell the team and decision-makers now, scope precisely which conclusions are affected and which still stand, and propose targeted follow-up with users who did not complete.
- C) Quietly commission follow-up and correct the record if findings differ.
- D) Say nothing; the decision was reasonable anyway.

**Correct answer: B. Least effective: D**

**Explanation:** A sample of successful completers cannot see the failures the design was meant to address, and something is being built on it. Option B does the three things that matter: tells the people who acted on the finding, scopes the damage precisely rather than minimising or catastrophising, and proposes the fix. The scoping is important — conclusions about how successful users navigate may remain sound, and saying so is accuracy rather than defensiveness. Option A defers past usefulness. Option C conceals a known flaw while the build proceeds. Option D is least effective: reasoning that the decision was probably fine substitutes your guess for the evidence you relied on, and if it emerges later the concealment is what will be remembered.

### Preparation tips

- **Answer as a trusted practitioner.** Exercise judgement, hold positions the evidence supports, escalate only what needs authority you lack.
- **Put the excluded user first.** When an option protects someone who cannot operate a control, assume it is strongest.
- **Prefer structural fixes to confrontational ones.** Changing a session's format beats telling someone to stop talking.
- **Ask whether an instance is a template.** One broken shared component means every service using it.
- **Redirect rather than refuse.** "Not that, but here is what would work" outperforms "no".
- **Ask for an explicit recorded decision.** Unrecorded decisions drift into launches.
- **Raise it once, properly.** One well-evidenced challenge plus a documented risk beats repeated objection.
- **Report shared defects upstream with a reproduction.** Vague reports get triaged low.

### Common pitfalls to avoid

- **Dismissing consistent behaviour as unrepresentative participants.**
- **Accepting a shortcut that transfers cost to users.**
- **Keeping a pattern whose meaning is wrong.** Users read layout faster than words.
- **Forking a shared component locally.** It leaves every other service broken and creates divergence.
- **Treating an accessibility statement as a way to launch with a blocker.**
- **Softening difficult findings.** It lets wasted effort continue.
- **Treating consensus as a terminal value.**
- **Delaying disclosure of your own error.** Speed and precise scoping turn a mistake into evidence of integrity.

## Conclusion

You have reached the end, and it is worth pausing over what that involved: forty-eight questions across four assessment types, with the reasoning worked through on each. That is a substantial piece of professional preparation, and rather more than most people do.

Look back at the ground. In the cognitive section you audited a page and caught the requirements that were absent rather than wrong, separated preparation from interface as explanations for a 29 point gap, worked out why a calendar picker suits a booking and not a date of birth, weighted a pattern decision by the eight journeys that would reuse it, read a 40% return rate as both a failure and a natural experiment, and connected a shorter page to a rise in phone calls. In the numeric section you measured drop-off against the right base, converted 1.5% into 10,800 people, noticed that desktop and tablet behaving identically localised a problem to small screens, distinguished percentage points from relative change, and declined to endorse a comparison too small to detect what it was built to find. In the verbal section you located a deadline inside a condition, refused to convert a scope statement into an exemption, noticed "programmatically" carrying a whole requirement, and read a condition as a condition rather than a prohibition. And in the situational judgement section you fixed a lopsided session structurally, asked whether one broken error summary meant a broken template, reported a shared defect upstream with a reproduction, and documented a risk after losing an argument.

Notice what unites almost all of it. Every section, in its own idiom, was testing whether you know the limits of what you have and will say so — the limits of a sample, of a metric, of a constraint somebody has asserted, of a decision made on comfortable evidence. That is what makes a designer trusted to make good decisions, which is the phrase your own role description uses. Teams can generate opinions without you and read dashboards without you. What you bring is a design rationale that holds up when someone pulls at it.

A word about your level. Being trusted is a real threshold. Nobody proofreads your reasoning before it reaches a build, and the standard you hold yourself to becomes the standard the service gets. It also means the errors that matter most are no longer the ones you would notice — they are the ones you are confident about. That is the honest case for practising this kind of reasoning deliberately rather than trusting experience: experience makes you fluent, and fluency makes overreach feel like insight.

If you want to build on this, a few things repay effort more than rereading. Complete your own service using only a keyboard, then again with a screen reader, then again at 400% zoom; each pass finds a different class of defect. Read the "when not to use this" section of every component you rely on. Ask a developer what actually happens to a value between the keyboard and the database. Take a constraint you have accepted for months and ask where it comes from. And the next time a number sounds decisive, convert it into people before you respond to it.

Finally, for the day itself. An assessment samples your reasoning on one morning under artificial conditions. It is not a verdict on your judgement or your career. Read the stem twice, find the denominator, trust Cannot Say, check both scales, and remember that the strongest answer is usually the one honest about uncertainty rather than the one that sounds most decisive.

Good luck. Go carefully, ask what things are for, and keep unplugging the mouse.
