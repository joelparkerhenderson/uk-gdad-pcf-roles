# Senior Interaction Designer - Psychometric Assessment Resources

## Introduction

Welcome. This guide is written for you as a senior interaction designer in the UK Government Digital and Data profession — an experienced designer who works with minimal support, influences and mentors others, works with service managers and programme directors to develop design concepts, potentially carries responsibility across complex services, helps set direction and embed good practice within teams, and makes important decisions based on research while understanding how that research affects others. That is a role defined as much by judgement and influence as by craft, and the assessments here are pitched accordingly.

You may be preparing for a formal assessment as part of a selection or promotion process, or you may be here because reasoning that has become fluent is worth periodically re-examining. Both are good reasons, and the second is the more interesting one. At your level the risk is not that you lack technique. It is that technique has become automatic, automatic reasoning feels certain, and certainty is where the expensive errors live.

Three features of your role shape everything that follows. First, you are accountable for more than your own work: you advise teams, critique others' approaches, identify and create new patterns and components, and embed good practice. That makes diagnostic reasoning — spotting the flaw in somebody else's evidence or design logic — a core competence rather than an occasional one. Second, you work with complexity: complex services, complex evidence such as large data sets, complex designs iterated across successive rounds, and prototyping complex ideas at appropriate fidelity. Complexity here means genuinely competing constraints and evidence supporting more than one reading. Third, you build consensus by asking difficult questions and challenging assumptions, and you work across profession boundaries with policy and technology colleagues. That is a negotiating role, and it rests on your evidence being unassailable.

There is a discipline-specific dimension worth naming. At your level you are creating patterns and components rather than only using them, which changes the nature of the reasoning. A pattern is a decision made once and paid for many times, in maintenance, in the expectations it sets, and in the accessibility characteristics it propagates. Getting one right multiplies; getting one wrong multiplies too, and is far harder to undo than a single screen. Several items below turn on that asymmetry.

The document has four main sections:

1. A workplace job-specific cognitive assessment — evidence auditing, competing hypotheses, systemic risk, strategic prioritisation, and the diagnosis of problems in designs and research done by other people.
2. A numeric reasoning assessment — rates, weighted comparisons, funnel and cohort data, sampling adequacy, and the interrogation of quantitative claims embedded in business cases and board papers.
3. A verbal reasoning assessment — dense standards, evaluation reports, technical specifications and stakeholder correspondence, with items pitched at real ambiguity.
4. A situational judgement assessment — dilemmas involving ethics, assurance, mentoring, organisational politics, and the defence of design positions under pressure.

Each section provides an overview, a mapping to your named skills, twelve practice questions with full explanations, preparation tips, and common pitfalls.

Several items have an attractive answer that is wrong for a reason worth understanding, and the explanations spend most of their words on the near misses. Commit before reading, and attend particularly where you were quick and sure.

Let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive assessment measures the reasoning your role demands, presented through practical materials rather than abstract puzzles. At senior level the materials are messier and the reasoning less mechanical. You will meet evidence supporting two incompatible readings, designs with a flaw that compromises some conclusions but not others, prioritisation problems with no dominant option, and claims made by other people that need diagnosing rather than accepting or rejecting.

The format is typically an online test of fifteen to thirty minutes covering pattern recognition, logical deduction, error checking, prioritisation and applied problem solving. Scoring is objective against a norm group of comparable seniority, so your comparison set is other experienced practitioners. Adaptive platforms raise difficulty after correct answers, and acuity reports distinguish speed from accuracy, both rewarding precision over pace.

Three things distinguish this section at your level.

The first is the shift from producing sound reasoning to auditing it. Your role names advising teams on inclusive design, helping teams use design hypotheses effectively, and building consensus by asking difficult questions and challenging assumptions. Each is a diagnostic act performed on somebody else's thinking, frequently under time pressure and often where saying "that does not follow" carries a social cost.

The second is systemic reasoning. When something goes wrong repeatedly, the informative feature is usually the distribution of the failures rather than any individual failure. Concentrated in one team, under one condition, among experienced people? That is a process telling you it cannot be complied with. Scattered? Something else. Reading distributions diagnostically separates senior practice from very competent practice.

The third is the multiplier effect of pattern-level decisions. Because you create patterns and components rather than only using them, several items ask you to weigh a decision by how many times it will be paid for rather than by its immediate cost.

You need to memorise nothing. What you need is the discipline not to let fluency substitute for examination.

### How this assessment maps to your role

The cognitive dimensions map onto the skills named in your role summary:

- **Auditing evidence and reasoning** maps to **Evidence-based design**, where you analyse, synthesise and clearly explain complex evidence such as large data sets, and help your team use design hypotheses effectively.
- **Challenging assumptions** maps to **Design communication**, where you build consensus by asking difficult questions and challenging assumptions.
- **Systemic and risk reasoning** map to **Designing strategically**, where you use risks, opportunities and constraints in technology, systems and policy to shape design.
- **Pattern-level judgement** maps to **Designing strategically**, where you identify and create new design patterns and components.
- **Diagnosing exclusion** maps to **Designing for everyone**, where you advise teams on inclusive design and deliver ethical services considering the personal and social context of users.
- **Reasoning about positions and incentives** maps to **Designing together**, where you work across team or profession boundaries, for example with policy teams.

### Practice questions

**Question 1 (easy) — Auditing against a standard**

Your standard requires every transactional page to: use words users would use, state what happens next, state how long it will take, avoid requesting held information, offer a route to help, and work without JavaScript. A page uses internal terminology, says the case will be assessed, gives no timescale, re-requests a held reference, has no contact route, and degrades gracefully without JavaScript. How many requirements are unmet?

- A) 3
- B) 4
- C) 5
- D) 6

**Correct answer: B**

**Explanation:** Work through all six. Internal terminology fails the first. "The case will be assessed" satisfies the second, minimally. No timescale fails the third. Re-requesting held information fails the fourth. No contact route fails the fifth. Graceful degradation satisfies the sixth. Four unmet, giving B. Option C typically comes from marking "what happens next" as unmet because the statement is thin — a defensible design judgement, and the item tests whether you apply the standard as written rather than as you would have written it, which is what assurance requires. Note which two are easiest to miss: the absent help route and the JavaScript behaviour, both because they concern something that should be present rather than something present and wrong. When auditing at scale, absences are the systematic blind spot, and it is worth building a checklist that leads with them.

**Question 2 (easy) — Deduction from a governance rule**

Your standard states: "A custom component may enter a live service only with sign-off from the head of interaction design, unless it replaces an existing custom component on a like-for-like basis and has been assessed as low risk." A team reports: "We shipped a custom component last month without sign-off." Which must be true?

- A) The standard was breached.
- B) It was a low-risk like-for-like replacement.
- C) Either it was a low-risk like-for-like replacement, or the standard was breached.
- D) The component should be withdrawn.

**Correct answer: C**

**Explanation:** A conditional with a stated exception, plus facts silent on the exception, licenses only the disjunction. Options A and B each assume a branch. Option D prescribes an action rather than stating what must be true, and the question asks the latter — worth noticing, because at this level a sensible action is frequently offered as a distractor in a logic item, and it may well be what you would do. Only C holds. Note the compound exception: like-for-like *and* low risk. A component satisfying only one does not qualify, and partial satisfaction of a compound exception is among the most common misreadings in governance conversations. As the person likely to be assuring this, your opening move is to establish which route was taken, framed as an enquiry — because if the exception applied, an accusation is something you then have to withdraw.

**Question 3 (moderate) — Diagnosing a colleague's conclusion**

A designer you advise reports: "Users find the new autocomplete easy — all 18 participants completed the task without difficulty." Sessions were moderated, the facilitator demonstrated the component first, participants were recruited from the departmental panel, and all used a laptop with a mouse. What is the most important observation?

- A) Eighteen participants is too small a sample.
- B) The demonstration, the panel recruitment and the mouse-only conditions all remove the difficulties the component is most likely to produce — first encounter, unfamiliarity, and keyboard or assistive technology operation — so the result describes an unusually favourable case rather than the component's usability.
- C) "Easy" is not a measurable construct.
- D) A think-aloud protocol should have been used.

**Correct answer: B**

**Explanation:** Unanimity is the alarm, and the strongest observation explains it by identifying what the conditions removed. Demonstrating a component first eliminates the first-encounter difficulty that autocomplete controls characteristically produce; a departmental panel is populated by people comfortable with government interfaces; and testing exclusively with a mouse skips the operation mode where custom autocompletes most often fail entirely. Each removes a distinct source of difficulty, and together they leave a test that could hardly have produced any other result. Option C is a fair secondary point about measurement. Option A misdiagnoses validity as size — 180 participants under identical conditions would produce the same finding. Option D is a technique fix leaving all three conditions in place. When you feed this back, name what each condition removed, because a designer who adds think-aloud while keeping the demonstration will get the same answer and believe it more.

**Question 4 (moderate) — Strategic prioritisation**

You have responsibility across several services and can direct substantial design capacity to one this quarter:

1. A pattern for identity checks is being decided next month and will be reused across six services.
2. A live service has a persistent 30% drop-off at one step, affecting 250,000 users a year.
3. A service launches in six weeks with designs signed off.
4. A programme is preparing a business case due in nine months.

Which is strongest, and why?

- A) Item 2, because it affects the most users.
- B) Item 1, because the decision is imminent, will be reused six times, and design input is the only thing that could still shape it — and a pattern embeds its characteristics, good or bad, into every service that adopts it.
- C) Item 4, because business cases shape long-term investment.
- D) Item 3, because launching untested carries reputational risk.

**Correct answer: B**

**Explanation:** Value of information is the right frame, and item 1 has a multiplier the others lack. A pattern decided once and reused six times embeds either a good decision or a bad one six times over, and the cost of changing it rises with every service that adopts it — after a year, changing a widely used pattern is a coordination problem across six teams rather than a design problem. Item 2 affects more users today but has been stable for months and will remain so for three more, so deferral costs comparatively little. Item 3 is weakest despite sounding prudent: signed-off designs six weeks from launch means findings arrive with nowhere to go. Item 4 has nine months and, at your level, is where the profile trap lives — business cases attract attention, and attention is not decision leverage.

**Question 5 (moderate) — Systemic risk in a component decision**

A team proposes a custom component that will be used on eleven pages across three services. It is well designed, and it will be maintained by that team alone. What is the most complete risk analysis?

- A) The risk is that the component may have accessibility defects.
- B) The immediate risk is defects, but the structural risks matter as much: a component maintained by one team becomes a dependency for three, so its priorities will not match theirs; it will diverge as teams fork it for local needs; and its accessibility characteristics propagate to eleven pages, meaning one undetected defect is eleven defects — so the decision is really about ownership and maintenance, not about this component's quality.
- C) There is no significant risk if it is tested properly.
- D) Custom components should be avoided.

**Correct answer: B**

**Explanation:** The strongest analysis follows the consequences beyond the artefact, which is what your role means by using constraints in technology and systems to shape design. A well-made component is not the question; a shared dependency with a single owner is. The owning team will deprioritise a fix that matters urgently to another service, at which point the other teams fork it, and within a year there are three divergent versions with different defects and no shared testing. Meanwhile any accessibility characteristic — good or bad — is multiplied by eleven pages, which is what makes the initial quality so consequential and the maintenance arrangement so much more so. Option B names all of this and correctly reframes the decision as being about ownership. Option A stops at the first order. Option C treats testing as sufficient, which it is at launch and not thereafter. Option D states a rule without reasoning.

**Question 6 (moderate) — Feedback on a colleague's synthesis**

A designer presents a case for a new pattern drawing on nine studies. The central claim — "users expect to be able to save and return at any point" — is supported by material from three studies, all of services taking more than two weeks to complete. What is the most useful feedback?

- A) The claim is invalid and should be removed.
- B) Note that the supporting evidence comes exclusively from multi-week services, so the claim over-reaches as written; suggest narrowing it, or testing whether it holds in short services, before it becomes a pattern that every service is expected to implement.
- C) Suggest adding more studies.
- D) Approve it; three studies is a reasonable basis.

**Correct answer: B**

**Explanation:** The evidence is real and the sentence built on it reaches further than the evidence goes — the most common failure in synthesis, and one with unusual consequences here because the claim is destined to become a pattern. Multi-week services supply an obvious reason to expect saving and returning: you cannot finish in one sitting. That expectation may not transfer to a five-minute service, where a save-and-return control adds a decision, occupies visual space and creates an abandoned-session problem for nothing. Option B preserves the finding, corrects the scope, and offers two proportionate routes. Option A discards something real. Option D lets an over-generalised claim become an obligation on every team. Option C reaches for the expensive remedy before the free one — narrowing costs nothing.

**Question 7 (moderate) — Prototype fidelity for a complex idea**

You need to test whether a new multi-step interaction — a single control for entering a date range with optional open ends — is comprehensible before committing to build. You have three weeks. What is strongest?

- A) A high-fidelity interactive prototype with full validation.
- B) A low-to-mid fidelity prototype of the control in two or three variants, tested with keyboard and screen reader from the outset rather than only with a mouse — because comprehension is the question, but a novel control's viability depends on whether it can be operated at all, and discovering that late is what makes custom controls expensive.
- C) A written description discussed in interviews.
- D) A technical spike to establish feasibility.

**Correct answer: B**

**Explanation:** Match the artefact to the question, and then notice the second question hiding behind it. Comprehension can be tested at low fidelity, and low fidelity is faster and changeable between sessions, so you can test three variants rather than one. But a novel control carries a viability question that comprehension testing will not surface: whether it can be operated by keyboard and announced sensibly by a screen reader. Discovering at build that it cannot is what makes custom controls expensive, and it is entirely avoidable by including those modes from the first prototype rather than treating them as a later check. Option B combines both. Option A spends the three weeks building and still tests only the mouse path. Option C removes the concrete anchor a novel control needs. Option D answers a later question in the wrong order.

**Question 8 (harder) — Scoping a flaw**

A study you are assuring used a prototype whose "back" function was broken throughout. Four findings: (i) participants could not locate the eligibility criteria; (ii) participants abandoned after a wrong turn; (iii) sessions ran longer than expected; (iv) participants misread the declaration. Which are compromised?

- A) All four.
- B) None; the fault was incidental.
- C) Findings (ii) and (iii) are directly compromised, since inability to go back plausibly produced both, while (i) and (iv) concern comprehension of content and are largely unaffected.
- D) Only (ii).

**Correct answer: C**

**Explanation:** The skill is scoping precisely rather than treating a flaw as total or trivial. A broken back function prevents recovery from a wrong turn, directly manufacturing abandonment and inflating durations, so (ii) and (iii) cannot be separated from the artefact. Findings (i) and (iv) concern locating and understanding content, which the fault does not touch. Option A discards two sound findings and, when you are embedding good practice, does real damage: a senior designer who condemns wholesale teaches teams that any admitted prototype fault invalidates everything, which is a direct incentive to stop mentioning faults — and you will then be assuring studies whose faults have been quietly omitted. Option B leaves two artefactual findings circulating, where they will justify fixes to problems that do not exist. Option D catches the obvious compromise and misses the duration one.

**Question 9 (harder) — Reading a good number for the problem inside it**

Analytics show 40% of users who abandon at the upload step return within seven days and complete. The team treats this as a success. What is the strongest observation?

- A) Agree; the 60% is the real problem.
- B) The 40% are also evidence of a problem — two or more attempts at something that should take one — and they are a natural experiment: something enabled them to return and succeed, and identifying whether that was a saved session, an email, or simply remembering the URL tells you what to build for the 60%.
- C) The 40% should be excluded from the drop-off figure.
- D) Send reminders to everyone who abandons.

**Correct answer: B**

**Explanation:** This is opportunity reasoning. The team has read a number as a success because it ends well, and missed that a returning user is one who could not finish first time — almost always because a document was not to hand. That is an interaction design problem with an interaction design answer: set expectations before the journey starts, and make saving and resuming discoverable. The more valuable half of option B is the natural experiment, and note how specific it is: the three candidate mechanisms imply completely different builds. If people returned because a session persisted, the fix is making that visible; if they bookmarked, the fix is a resumable link; if they started again from scratch, the "return" is not a success at all but a second full attempt. Option A accepts the framing. Option C conceals the phenomenon. Option D leaps to one intervention without the cause.

**Question 10 (harder) — A local optimisation**

A team reports success because time on a form page fell from 90 to 55 seconds after content was removed. Contact centre calls about that step rose 25% over the same period, and completion was unchanged. What is the strongest analysis?

- A) The redesign succeeded on its metric; the calls need separate investigation.
- B) The pattern is consistent with content having been removed that users needed, pushing them to telephone for the explanation — an apparent efficiency that is probably a cost transfer, with unchanged completion suggesting no benefit at all; the right measure is end-to-end effort including contact.
- C) The call increase must have another cause.
- D) Report both metrics without interpretation.

**Correct answer: B**

**Explanation:** Three facts fit together: the page got shorter, calls rose sharply, and completion did not move. The most economical explanation is that removed content is content users now obtain by telephone, so the saving has been transferred rather than realised — and the unchanged completion is the decisive detail, because a genuine improvement should have moved it. Option B names the mechanism and the measurement error beneath it: optimising one step while ignoring what happens around it is exactly the failure your discipline exists to catch, and it recurs as long as the metric is scoped to the page. Option A accepts a metric because it was agreed, which is how services get locally optimised into worse wholes. Option C asserts an alternative cause without evidence, which may be right and is not the first move. Option D abdicates the interpretation your role exists to supply.

**Question 11 (harder) — Reading the distribution of failures**

Reviewing a year across teams, you find accessibility defects reached live in four services. All four were in one directorate, all under ministerial deadline pressure, all designed by experienced practitioners. What is the strongest response?

- A) Report the four and require remediation.
- B) Treat the concentration as diagnostic: four failures in one directorate under identical pressure by experienced people indicates a process that cannot be complied with when time is short — investigate what accessibility assurance demands and how long it takes, propose a fast route, and remediate the four alongside.
- C) Remind all designers of the requirements.
- D) Introduce a mandatory accessibility gate for every service.

**Correct answer: B**

**Explanation:** The distribution is the most informative feature. Scattered failures would indicate individual capability; four concentrated under identical pressure by experienced practitioners indicate a process that does not survive a deadline. Option B investigates the mechanism and fixes it, while the closing clause preserves the point that a systemic diagnosis is not a reason to leave individual failures unremediated — real users cannot use four services now. Option A treats the instances and guarantees recurrence. Option C is the weakest available response to any compliance failure: people who knew the requirement and missed it under pressure will not change on being told again. Option D imposes friction on every compliant service to catch a localised failure, which is how organisational burden accumulates and how the next workaround gets invented.

**Question 12 (harder) — Working across a profession boundary**

A technology team has selected a third-party component library that does not meet your accessibility standard. They chose it for delivery speed and have already built two services with it. What is the strongest approach?

- A) Require them to stop using it.
- B) Establish specifically which components fail and how badly, since a library is not uniformly good or bad; propose a shortlist of components to avoid or wrap, and a route to remediate the two existing services — framing it as making their choice workable rather than reversing it.
- C) Escalate to the head of profession.
- D) Accept it and document the risk.

**Correct answer: B**

**Explanation:** "Does not meet the standard" is almost never true of a whole library — it is true of specific components, usually a handful of complex ones such as date pickers, modals and custom selects, while the buttons and inputs are fine. Option B establishes which, which converts an unwinnable argument about a decision already made into a tractable list of specific things to avoid or wrap. That reframe matters practically and politically: the team has built two services and cannot start again, so an answer requiring them to is an answer they will refuse, and you will have spent your standing to no effect. Option A asks for reversal without a route. Option C escalates a solvable disagreement across a boundary you will need repeatedly. Option D accepts an exclusion and calls it risk management, which is what documenting a risk becomes when nothing follows it.

### Preparation tips

- **Read outputs for the study behind them.** Practise inferring conditions, recruitment and mode of operation from what a report says and omits.
- **Scope flaws precisely.** Wholesale condemnation teaches teams to stop mentioning faults.
- **Follow consequences beyond first order.** A shared component is an ownership decision, not a design one.
- **Weight decisions by reuse.** A pattern used six times is worth six times the attention.
- **Read the distribution of failures.** Concentrated non-compliance diagnoses a process; scattered diagnoses conduct.
- **Test novel controls in the mode most likely to break them.** Keyboard and screen reader from the first prototype, not the last.
- **Look for metrics moving in opposite directions.** A local optimisation is usually a cost transfer.
- **Reframe unwinnable arguments into tractable lists.** "Which components, specifically?" beats "not compliant".

### Common pitfalls to avoid

- **Treating effect size as causal certainty.**
- **Missing absent requirements when auditing.** What is not there is systematically harder to see.
- **Applying a standard as you would have written it.** Assurance means applying it as written.
- **Reaching for reminders or training as the answer to a systemic problem.**
- **Adding friction for the compliant majority.** How burden accumulates and workarounds are born.
- **Accepting a metric because it is the agreed one.** Agreed metrics get optimised into worse services.
- **Reading a partially satisfied compound exception as satisfied.**
- **Documenting a risk and calling it management.** Nothing follows a documented risk unless someone makes it.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A numeric reasoning assessment measures how accurately you handle quantitative material. At senior level the emphasis shifts decisively from calculating to interrogating. You will still need to compute correctly, but the harder items ask whether a figure means what somebody claims — which is, not coincidentally, the question you are frequently the only person in the room positioned to ask.

The format is typically a timed online test of fifteen to thirty minutes, each item presenting a table, chart or paragraph of figures with a multiple-choice question. Calculators are usually provided and the arithmetic is deliberately tractable. Time per item is tight, so the operative skill is locating what matters and disregarding what does not.

The professional stake is substantial. Quantitative evidence carries unearned authority: a number in a board paper is treated as fact while a design argument is treated as a view, regardless of the rigour behind either. Your role names analysing complex evidence such as large data sets, and working with service managers and programme directors — people whose world is expressed in numbers. Senior designers who cannot interrogate a figure confidently lose arguments they should win, and occasionally win arguments they should lose.

Four habits carry most of the load. Establish what the question asks before looking at the data. Identify the denominator and the population it represents before calculating. Estimate, calculate, compare. And sanity-check against the world.

Distractors are constructed from a predictable catalogue: wrong denominator, percentage confused with percentage point, new value used as the base in a percentage change, rates averaged without weighting, vendor or benchmark metrics compared to internal ones without checking definitions.

### How this assessment maps to your role

The numerical skills tested map onto your named skills:

- **Analysing complex evidence** maps to **Evidence-based design**, where you analyse, synthesise and clearly explain complex evidence such as large data sets.
- **Comparing rates between groups** maps to **Designing for everyone**, where gaps between groups are the first numerical trace of exclusion.
- **Judging what a measurement can establish** maps to **Evidence-based design**, where you help teams use design hypotheses effectively.
- **Quantifying risk and reuse** maps to **Designing strategically**, where scale determines what matters.
- **Presenting figures at defensible strength** maps to **Design communication**, where you document and communicate decisions, risks and unresolved issues.
- **Interrogating others' claims** maps to **Design communication**, where you build consensus by asking difficult questions.

### Practice questions

**Question 1 (easy) — Rate from counts**

Of 6,400 users who reached a page, 1,600 triggered a validation error on one field. What percentage?

- A) 20%
- B) 25%
- C) 30%
- D) 40%

**Correct answer: B**

**Explanation:** 1,600 ÷ 6,400 = 0.25, so 25%, and the answer is B. Estimate first: 1,600 of 6,400 is a quarter. Options A and C come from dividing by 8,000 and 5,333. A quarter of arrivals failing one field is a serious signal and, at your level, the more interesting question is whether the field appears in a shared pattern — because if so, the same rate is being produced everywhere the pattern is used, and the fix is worth many times what it looks like from this page alone.

**Question 2 (easy) — Drop-off against the right base**

A page is reached by 8,000 users and passed by 6,000. What is the drop-off rate?

- A) 25%
- B) 33%
- C) 75%
- D) 30%

**Correct answer: A**

**Explanation:** The drop-off is 2,000, measured against arrivals: 2,000 ÷ 8,000 = 0.25, giving A. Option B divides by those who continued — the most common error in page analytics, overstating every drop-off it touches. The rule: drop-off is measured against arrivals. At your level the consequence is not one wrong figure but a wrong organisational picture: if teams compute pages with different denominators, the ranking of where design capacity should go is distorted, and you are frequently the person adjudicating that ranking. A short line in your team's standard specifying the denominator is one of the cheapest quality interventions available.

**Question 3 (easy) — Disaggregated rates**

| Group | Users | Completed |
|---|---|---|
| Mouse users | 9,000 | 8,100 |
| Keyboard-only users | 700 | 350 |
| Screen reader users | 300 | 75 |

What is the overall completion rate, and the gap between the highest and lowest group rates?

- A) 85% overall; 50 point gap
- B) 85% overall; 65 point gap
- C) 90% overall; 65 point gap
- D) 88% overall; 40 point gap

**Correct answer: B**

**Explanation:** Completions total 8,100 + 350 + 75 = 8,525, across 9,000 + 700 + 300 = 10,000 users, so 8,525 ÷ 10,000 = 85.25%, which rounds to 85%. Group rates are 8,100 ÷ 9,000 = 90%, 350 ÷ 700 = 50%, and 75 ÷ 300 = 25%, giving a gap of 90 − 25 = 65 percentage points. Hence B. Option C mistakes the largest group's rate for the overall rate, which is the characteristic error when one group dominates the sample — and it is worth noticing how nearly right it feels, since 90% of the users are mouse users. That is exactly the point. The overall figure of 85% describes no group in this table, and it conceals that screen reader users fail three times in four. An aggregate that can be disaggregated should be, and a standard that does not require disaggregation by mode of operation has a hole in it shaped precisely like the users least able to complain about it.

**Question 4 (easy) — Centre and spread**

Eleven participants took these times in seconds: 12, 15, 18, 20, 22, 25, 28, 30, 35, 40 and 240. Which summary is most defensible?

- A) Mean 44.1 seconds
- B) Median 25 seconds, range 12 to 240, with the 240-second case described separately
- C) Median 25 seconds
- D) Mean 44.1 seconds, range 12 to 240

**Correct answer: B**

**Explanation:** The mean of about 44 exceeds ten of the eleven observations, so it represents almost nobody. The median is the sixth value, 25 seconds, which describes the group well. But the median alone conceals a session lasting six times the typical duration, almost certainly the most informative observation in the set. Option B gives centre, spread and explicit treatment of the outlier. Option D pairs the range with a misleading centre. Option C buries the extreme case. The rule to enforce in the work you assure: a central figure never travels alone, and an outlier is a lead rather than noise — the person who took 240 seconds encountered something the other ten did not, and finding out what is the point.

**Question 5 (moderate) — Weighted aggregation**

Four studies of the same component: 10 participants at 50% success; 20 at 65%; 10 at 70%; 20 at 80%. What is the overall rate across all 60?

- A) 66%
- B) 68%
- C) 69%
- D) 71%

**Correct answer: B**

**Explanation:** Convert each rate to counts. Study 1: 50% of 10 = 5. Study 2: 65% of 20 = 13. Study 3: 70% of 10 = 7. Study 4: 80% of 20 = 16. Total 5 + 13 + 7 + 16 = 41, across 60 participants, so 41 ÷ 60 = 0.683, about 68% and the answer is B. Option A is the unweighted mean of 50, 65, 70 and 80, which is 66.25 and over-weights the two smallest studies. Always return to counts. And ask the prior question, which matters more at your level: aggregating four studies of a component is meaningful only if the task and population were comparable. If one study tested the component in isolation and another within a full journey, the combined figure is arithmetically correct and referentially empty.

**Question 6 (moderate) — Funnel denominators**

Funnel: 100,000 start, 75,000 pass identity, 45,000 upload evidence, 40,500 submit. What proportion of those who passed identity went on to submit?

- A) 40.5%
- B) 54%
- C) 60%
- D) 90%

**Correct answer: B**

**Explanation:** The stem names users who passed identity, so the denominator is 75,000 and the part is 40,500: 40,500 ÷ 75,000 = 0.54, giving B. Option A uses 100,000, option C is the identity-to-upload rate, option D is the upload-to-submit rate. All are true of this funnel; one answers the question. Strategically the funnel also tells you where effort belongs: 25,000 lost at identity, 30,000 between identity and upload, and 4,500 at submission. A team proposing to redesign the submission step would need a strong reason, and being able to establish that in fifteen seconds is what lets you redirect a programme's plan in the meeting.

**Question 7 (moderate) — A benefits claim**

A benefits paper states that a change raised completion from 55% to 66%, describing it as "a 20% improvement". Is the description accurate?

- A) No; it is an 11% improvement.
- B) Yes as arithmetic — 11 ÷ 55 = 20% relative increase — but the expression is ambiguous, and the paper should say "20% relative increase" or "11 percentage points".
- C) No; it is 11 percentage points, and calling it 20% is wrong.
- D) No; it should be 16.7%.

**Correct answer: B**

**Explanation:** The relative increase is 11 ÷ 55 = 0.2, so 20% is defensible arithmetic. The problem is labelling: "a 20% improvement" will be read by many as a rise from 55% to 75%. Option B captures both halves. Option C over-corrects into an error of its own, since relative change is legitimate. Option A confuses the units; option D divides by the new value. At your level this is governance rather than arithmetic: benefits papers routinely select the flattering framing, usually without intent to mislead, and asking for both numbers as a standing convention rather than as a challenge to an individual is the cheapest control available and costs no political capital.

**Question 8 (moderate) — Quantifying a capability requirement**

A service receives 900,000 submissions a year. A proposed control requires JavaScript, and around 1.2% of sessions run without it. How many people a year would be affected?

- A) 1,080
- B) 10,800
- C) 11,000
- D) 108,000

**Correct answer: B**

**Explanation:** 1.2% of 900,000 is 0.012 × 900,000 = 10,800, giving B. Option A is 1.2% of 90,000; option D is 12%. The reason this belongs in a design guide is what it does to a conversation: "1.2% of sessions" sounds negligible, and "10,800 people a year unable to complete this" does not. It is also worth knowing what that population actually is, because it changes the argument: sessions without JavaScript are not a fixed group of ideological holdouts but largely people whose script failed to load on a poor connection, behind a corporate proxy, or on an older device. That makes the case about robustness rather than about accommodating a minority, which is a much stronger argument with a technology colleague.

**Question 9 (moderate) — Reconstructing an implied value**

A business case claims a 4 percentage point completion improvement on 1.2 million annual starts is worth £5.76 million a year. What is the implied value per additional completed application?

- A) £4.80
- B) £48
- C) £120
- D) £96

**Correct answer: C**

**Explanation:** A 4 percentage point improvement on 1.2 million starts gives 0.04 × 1,200,000 = 48,000 additional completions. Dividing: £5,760,000 ÷ 48,000 = £120, so C. Option A divides by 1.2 million, valuing every start; option B mistakes the completion count for pounds. The value of this calculation is that it takes thirty seconds and immediately tells you whether a business case is plausible — £120 per additional completed application may be reasonable for a high-value transaction and implausible for a simple information service. The challenge it enables is far more effective than disputing a total: "so we are valuing each additional completion at £120 — is that the right order?" is specific, answerable, and requires accusing nobody.

**Question 10 (harder) — A metric that conflates populations**

A dashboard reports "average time to complete: 12 minutes" for a service your evidence shows most users taking over forty minutes across several sittings. What is the likely explanation and the right intervention?

- A) The dashboard is wrong and should be corrected.
- B) The metric almost certainly measures single sessions rather than end-to-end journeys, so multi-sitting completions are excluded or counted only for their final short visit, and abandoned sessions may be included — ask for the definition and the distribution, and propose an end-to-end measure alongside it.
- C) The research sample was atypical.
- D) The figures cannot be reconciled.

**Correct answer: B**

**Explanation:** Session-based analytics and journey-based reality diverge systematically for any service completed over more than one sitting, and the divergence always flatters the service. Someone spending forty minutes across three visits typically appears as one short final session, and abandoned sessions may drag the mean lower. The figure is probably calculated correctly and defined in a way that cannot answer the question people think it answers. Option B names the mechanism and proposes a constructive intervention — asking for a definition is not an accusation, and offering an end-to-end measure gives the metric owner something to build rather than something to defend. Option A picks a fight over a number that is not wrong, which is how senior designers acquire a reputation for obstruction. Option C blames the research. Option D forecloses a useful reconciliation.

**Question 11 (harder) — Sampling adequacy**

A team proposes measuring whether a redesign improved completion by running 40 moderated sessions before and 40 after. Baseline is 58%; a 6 percentage point improvement is considered meaningful. What is the strongest response?

- A) Agree; 80 sessions is substantial.
- B) Explain that a 6 point difference on 40 per group is about two participants and well inside ordinary variation, so the comparison cannot detect it — recommend measuring the rate through live analytics across the full user base, and spending the 80 sessions on mechanisms, which moderated research does uniquely well.
- C) Increase to 60 per group.
- D) Run it and report the difference with caveats.

**Correct answer: B**

**Explanation:** Forty per group cannot distinguish a six point difference from chance; reliable detection needs several hundred per group. Option B says so and redirects rather than merely objecting, which is the substantive contribution: analytics measures rates across the whole population at negligible marginal cost, while moderated sessions are the only instrument that explains why a rate is what it is. Option A endorses a design that cannot answer its own question. Option C moves towards adequacy without reaching it while still misallocating scarce sessions. Option D is the most damaging at your level, because caveated findings from underpowered comparisons get cited without their caveats — and once your organisation establishes that forty-session comparisons can measure rates, you will be arguing against that precedent for years, usually against someone quoting a study you let through.

**Question 12 (harder) — Two metrics moving apart**

Time on a form page fell from 15 to 10 minutes after a redesign. Over the same period contact centre calls about the service rose 28% and completion was unchanged. What is the strongest analysis?

- A) The redesign succeeded on its metric; the calls need separate investigation.
- B) The pattern is consistent with content having been removed to shorten the page, pushing users to telephone for the explanation — an apparent efficiency that is probably a cost transfer, with unchanged completion suggesting no benefit to users; the right measure is end-to-end effort including contact.
- C) The call increase must have another cause.
- D) Report both without interpretation.

**Correct answer: B**

**Explanation:** Three facts fit together: the page got shorter, calls rose sharply, and completion did not move. The most economical explanation is that content removed from the page is content users now obtain by telephone, so the saving has been transferred rather than realised — and the unchanged completion rate is decisive, because a genuine improvement should have moved it. Option B names the mechanism and the measurement error beneath it: optimising one step while ignoring what happens around it is exactly the failure your discipline exists to prevent, and it recurs as long as the metric is scoped to the page. Option A accepts the metric because it was agreed. Option C asserts an alternative cause without evidence. Option D abdicates the interpretation your role exists to supply.

### Preparation tips

- **Find the denominator and the population before calculating.**
- **Recompute when nothing matches.** A close option is not a right one.
- **Convert percentages into people, and know who those people are.** Sessions without JavaScript are mostly failed loads, not choices.
- **Return to counts before combining rates.**
- **Reconstruct implied unit values.** Thirty seconds establishes whether a business case is plausible.
- **Ask for the definition and the distribution.** Most misleading metrics are correctly calculated and wrongly defined.
- **Watch for metrics moving in opposite directions.**
- **Insist on disaggregation by mode of operation.** Mouse, keyboard and screen reader rates diverge, and a single figure hides it.

### Common pitfalls to avoid

- **Averaging rates without weighting.**
- **Measuring drop-off against those who continued.** It overstates every step and distorts the ranking.
- **Confusing percentages with percentage points.**
- **Accepting a metric because it is the agreed one.**
- **Accepting a mean without a spread or a definition.** Session metrics flatter multi-sitting services.
- **Endorsing an underpowered comparison "with caveats".** Caveats do not travel; the number and the precedent do.
- **Reporting an aggregate that could be disaggregated.**
- **Aggregating studies that are not comparable.** Arithmetically correct and referentially empty.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A verbal reasoning assessment measures how accurately you read. In a senior role that runs on documents — standards, accessibility regulations, component specifications, technical constraints, policy submissions, contracts — reading accuracy is the substrate everything else rests on. A misread criterion becomes a compliance failure across a programme; a misread finding in a colleague's report becomes advice given confidently to a programme director.

The classic format presents a short passage of dense workplace prose, typically three to six sentences, followed by statements to classify as True, False or Cannot Say. True means the statement follows necessarily. False means the passage contradicts it. Cannot Say means the passage neither establishes nor excludes it. Alongside these come comprehension items, main-point items, and questions asking which of four summaries is most accurate.

The governing rule is that you answer from the passage alone, and here is the part specific to your level: expertise actively costs you marks. The more accessibility criteria and component specifications you have read, the more readily you supply the clause you expect to be there and feel confident doing it. Senior candidates underperform on verbal reasoning at rates that surprise them, and this is nearly always the mechanism. The counter-habit must be mechanical: before marking anything True, put your finger on the words.

Cannot Say is the answer experienced practitioners avoid most. Forming a view under incomplete information is what your job consists of, and the reflex is deeply worn in. Here it is a liability.

Small words carry the load. "All" is not "most". "May" is not "must". "Should" is not "will". "Consider whether" is not "recommend". "Solely", "entirely", "unless", "provided that" and "where practicable" govern everything around them.

There is a direct professional payoff. Your role names building consensus by asking difficult questions and challenging assumptions, and a great many assumptions in delivery teams are about what a standard requires. Reading it precisely is how you find the room everyone believed was not there — and, equally often, how you establish that a rule people think is negotiable is not.

### How this assessment maps to your role

The verbal skills tested map onto your named skills:

- **Reading precisely** maps to **Designing for everyone**, where you ensure a design meets appropriate standards such as accessibility regulations.
- **Separating statement from inference** maps to **Evidence-based design**, where you analyse and clearly explain complex evidence.
- **Identifying the main point** maps to **Design communication**, where you clearly explain complex problems and ideas to teams or stakeholders outside design.
- **Handling qualified language** maps to **Designing strategically**, where you use constraints in technology, systems and policy to shape design.
- **Reading for absence** maps to **Designing for everyone**, where noticing that a specification never mentions keyboard operation has a consequence.
- **Documenting risks and unresolved issues accurately** maps to **Design communication**.

### Practice questions

*Passage A — for Questions 1 to 4*

"All new public-facing services must use components from the Design System where a suitable component exists, unless an exemption has been agreed in writing by the head of interaction design. Where no suitable component exists, teams may create a new one, provided it is documented and tested with assistive technology before use in a live service. Components created before this policy took effect must be reviewed within 12 months. Teams are encouraged, but not required, to contribute new components back to the Design System."

**Question 1 (easy)** — Statement: "Every new public-facing service must use Design System components where a suitable one exists." True, False or Cannot Say?

**Correct answer: False**

**Explanation:** The passage attaches an exception: a written exemption agreed by the head of interaction design. The statement's "every" contradicts that, so False. The pattern — absolute term in the statement, exception in the passage — is the most reliable in the section. Note that this passage carries two distinct mechanisms that are easy to conflate: an exemption, which removes the requirement, and the create-a-new-component route, which handles the case where no suitable component exists while the general obligation remains. They look similar and do different things, and Question 4 turns on the distinction.

**Question 2 (easy)** — Statement: "Teams must contribute new components back to the Design System." True, False or Cannot Say?

**Correct answer: False**

**Explanation:** The passage says teams are *encouraged, but not required*, to contribute back. The statement's "must" contradicts that explicitly, so False. Note that this soft aspiration sits directly alongside hard requirements — documentation, assistive technology testing, review within 12 months — which is why reading for general tone produces errors in both directions. In practice this is the sentence people quote at each other most often, usually to establish an obligation the passage explicitly declines to create.

**Question 3 (moderate)** — Statement: "A component created three years ago must have been reviewed by now." True, False or Cannot Say?

**Correct answer: Cannot Say**

**Explanation:** Components created before the policy took effect must be reviewed within 12 months, but the passage never says when the policy took effect. If it took effect three years ago a review would be overdue; if six months ago it would not. Because the fact you would need is absent, Cannot Say. Whenever a passage sets a deadline relative to a commencement, check whether the commencement date is given; its absence is deliberate and recurs throughout this section.

**Question 4 (harder)** — Statement: "A team that creates a new component because no suitable Design System component exists needs a written exemption." True, False or Cannot Say?

**Correct answer: False**

**Explanation:** Read the two mechanisms separately. The exemption applies to the requirement to use Design System components *where a suitable component exists*. Where none exists, that requirement is not engaged at all, and the passage provides a distinct route — create a new one, subject to documentation and testing. So no exemption is needed, and the statement is contradicted, making it False rather than Cannot Say. This is a genuinely important distinction beyond the test: teams frequently seek exemptions they do not need, which wastes their time and yours and creates a queue that makes the exemption process look like an obstacle. Reading the two routes apart is what lets you tell a team, accurately, that they can proceed.

*Passage B — for Questions 5 to 8*

"The evaluation of the new autocomplete component found that users completed address entry more quickly than with the previous free-text field, and made fewer formatting errors. The evaluation notes that participants were recruited through the departmental panel and all used a mouse. It did not assess performance with assistive technology or on touch devices. It recommends that the programme consider whether the component should be adopted more widely."

**Question 5 (easy)** — Statement: "Participants made fewer formatting errors with the autocomplete than with the free-text field." True, False or Cannot Say?

**Correct answer: True**

**Explanation:** The first sentence states this directly and the statement restates it without addition. True. Answer quickly and bank the time. The only care needed is to notice the comparison is against the previous free-text field specifically, not against some general standard — a statement claiming the component "produces few formatting errors" would be a different and unsupported claim.

**Question 6 (moderate)** — Statement: "The autocomplete component performs well with assistive technology." True, False or Cannot Say?

**Correct answer: Cannot Say**

**Explanation:** The passage says explicitly that the evaluation did not assess performance with assistive technology. Declared silence establishes nothing in either direction, so Cannot Say. This item is more consequential than it looks. Autocomplete components are among the most common sources of assistive technology failure, because announcing a dynamically filtered list of suggestions correctly is genuinely difficult and frequently done wrong. So the professional temptation runs towards False — you may well suspect it performs badly. The passage supports neither, and marking False would be substituting expertise for evidence in exactly the way this section penalises. In the workplace the right response is to commission the missing test, not to assume its result.

**Question 7 (moderate)** — Statement: "The component is suitable for wider adoption." True, False or Cannot Say?

**Correct answer: Cannot Say**

**Explanation:** The passage reports favourable findings under specific conditions, flags two untested modes, and recommends only that the programme *consider whether* wider adoption is appropriate. Nothing establishes suitability, and the untested modes are precisely those that would matter for wide adoption. Cannot Say. Note the compounding: a component evaluated only with mouse users from a departmental panel, and never with assistive technology or touch, has been tested in the single most favourable condition available. That is not a reason to conclude it is bad; it is a reason to conclude the evaluation does not answer the adoption question.

**Question 8 (harder)** — Statement: "The evaluation recommends adopting the component more widely." True, False or Cannot Say?

**Correct answer: False**

**Explanation:** The evaluation recommends that the programme *consider whether* the component should be adopted more widely — a recommendation to evaluate an option, including the possibility of concluding it should not. The statement asserts a recommendation to adopt, which was not made, so it is False rather than Cannot Say: the passage tells you what was recommended and it was something different. This pervades real evaluation documents and produces a familiar sequence in which a recommendation to consider becomes a commitment to roll out, gets entered on a plan, and is delivered without anyone having decided it was right — which is especially costly for a component, because rolling one out widely is far easier than rolling it back.

*Passage C — for Questions 9 to 12*

"Interactive components must be operable using a keyboard alone. Where a component uses a non-standard interaction, the team must provide a documented keyboard alternative. Focus must be visible at all times and must move in an order consistent with the visual presentation. Where a component displays an error, the error must be programmatically associated with the field it relates to; a visual association alone is not sufficient. These requirements apply to public-facing services and to internal tools used by more than fifty staff."

**Question 9 (easy)** — Statement: "A visual association between an error and its field is sufficient." True, False or Cannot Say?

**Correct answer: False**

**Explanation:** The passage states that a visual association alone is not sufficient and that the error must be programmatically associated. The statement contradicts this directly, so False. The word doing the work is "programmatically", and skimming past it produces exactly the failure the requirement exists to prevent — a message beside a field is obvious to a sighted user and may be entirely absent for someone whose screen reader encounters fields and messages in markup order rather than visual order.

**Question 10 (moderate)** — Statement: "These requirements apply to an internal tool used by fifteen staff." True, False or Cannot Say?

**Correct answer: Cannot Say**

**Explanation:** The final sentence extends the requirements to internal tools used by more than fifty staff. A tool used by fifteen does not meet that threshold, so the extension does not apply — but the passage does not say the requirements are *excluded* for smaller tools, only where they do apply. Silence about the fifteen-user case leaves it undetermined, so Cannot Say rather than False. This is a fine and common distinction in scoping clauses: stating where a rule applies is not the same as stating where it does not, and a reader who converts the first into the second will confidently tell a team they are exempt when nobody has said so. It is also worth noting that the legal position for internal tools may be governed by something outside this passage entirely.

**Question 11 (harder)** — Statement: "A component whose focus order differs from its visual presentation breaches the requirements." True, False or Cannot Say?

**Correct answer: True**

**Explanation:** The passage requires that focus move in an order consistent with the visual presentation. A component whose focus order differs from its visual presentation fails that requirement directly, so the statement follows and is True. Note the contrast with Question 10: here the passage states a requirement without condition, so a departure from it is a breach; there the passage stated a scope without stating an exclusion, so silence left the case undetermined. Distinguishing an unconditional requirement from a scoping statement is one of the more consequential reading skills in governance prose, because the first supports a finding and the second does not.

**Question 12 (harder) — Main point**

Which best captures the main point of Passage C?

- A) Components must never use non-standard interactions.
- B) Components in public services and larger internal tools must remain operable and comprehensible for someone not using a mouse or not seeing the screen — through keyboard operation, visible focus in a consistent order, documented alternatives for unusual interactions, and errors associated in code rather than only visually.
- C) Focus must be visible at all times.
- D) Errors must be programmatically associated with their fields.

**Correct answer: B**

**Explanation:** The main point must span the passage while adding nothing. Option A overstates a conditional requirement into a prohibition the passage does not make. Options C and D are each accurate about one clause and silent on the rest. Option B captures all four requirements, the scope clause, and the logic joining them: every requirement exists so the component works for someone not using a mouse or not seeing the screen. Note that B is the only option mentioning scope, which matters because a summary omitting it would imply the requirements are universal — and a designer who tells a small internal team they are bound by a rule that does not reach them loses credibility for the rules that do. Main-point items reward the option broad enough to cover everything and disciplined enough to invent nothing.

### Preparation tips

- **Point at the words.** Before marking True, identify the phrase that makes it true. Experience makes this harder, not easier.
- **Treat Cannot Say as decisive.** Especially where you suspect the answer — suspicion is not evidence.
- **Circle every qualifier.** All, every, entirely, solely, may, must, should, encouraged, unless, provided that, more than, consider whether.
- **Separate an exemption route from an alternative route.** They look similar and do different things.
- **Distinguish an unconditional requirement from a scoping statement.** The first supports a finding; the second does not.
- **Look for the missing fact.** Some items are Cannot Say because a commencement date was never given.
- **Treat declared silence as silence.** An evaluation that did not test something has told you nothing about it.
- **Practise on real standards.** Take an accessibility criterion and write three statements — one True, one False, one Cannot Say.

### Common pitfalls to avoid

- **Answering from professional knowledge.** The dominant senior error, and it is worst where your expertise is strongest.
- **Marking False because you suspect the untested result.** Suspicion is not the passage.
- **Reading "encouraged" as "required".**
- **Conflating an exemption with an alternative route.** Teams seek exemptions they do not need.
- **Converting a scope statement into an exemption.** Silence about a case is not permission.
- **Skimming a load-bearing adverb.** "Programmatically" changes the whole requirement.
- **Reading "consider whether X" as "recommend X".** Especially costly for components, which roll out easily and roll back badly.
- **Responding to implied stance.** A favourable evaluation under favourable conditions has not established suitability.

## Workplace job-specific situational judgement assessment

### About this assessment

A situational judgement assessment presents realistic workplace scenarios and asks what you would do. There is no passage to parse and no arithmetic. You get a dilemma of the kind your role produces, four or five candidate responses, and a question asking which is most effective and often which is least.

This section measures whether your judgement matches what the profession considers good practice at your level. Your role places you as an experienced designer working with minimal support, who influences and mentors others, works with service managers and programme directors, may carry responsibility across complex services, helps set direction and embed good practice, and makes important decisions based on research while understanding how that research affects others. The strongest answers involve independent professional judgement, responsibility for other people's practice as well as your own, holding positions under genuine organisational pressure, and developing capability rather than solving everything personally.

That last point separates your level from a competent practitioner's more sharply than anything else. An interaction designer who fixes a colleague's flawed component has solved a problem. A senior interaction designer who fixes it without the colleague learning anything has done half the job. Several items below turn on that distinction.

Four principles carry most scenarios.

Users come first, and specifically the users who cannot get past something. An interaction that excludes one group is not slightly worse for them; it is unusable, and that asymmetry is why accessibility questions rarely lose to schedule questions on the merits.

Protect the integrity of the evidence and of the people whose job it is to protect it. You are increasingly the person a junior designer looks to when pressed to say something they should not, and options that leave them alone with that pressure are weak even when the design survives.

Develop capability while solving the problem. The best answers frequently teach, delegate with support, or change a process, because a senior designer who only produces outputs does not scale.

Escalate what genuinely requires authority you do not hold, and handle everything else.

### How this assessment maps to your role

The judgement dimensions map onto your named skills:

- **Building consensus and challenging assumptions** maps to **Design communication**, where you build consensus by asking difficult questions and challenging assumptions.
- **Advising on inclusive and ethical design** maps to **Designing for everyone**, where you advise teams and deliver ethical services considering users' personal and social context.
- **Running and adapting sessions, and coaching others** maps to **Designing together**, where you advise others how to plan and run sessions and adapt them to achieve a useful outcome.
- **Working across profession boundaries** maps to **Designing together**, where you work with policy and technology teams.
- **Embedding practice and mentoring** maps to **Leading design** and to **Iterative design**, where you help other designers apply iterative principles.
- **Documenting risk honestly** maps to **Design communication**, where you document decisions, related risks and unresolved issues.

### Practice questions

**Question 1 (easy) — A designer under pressure from a director**

A designer you mentor tells you a director has asked them to remove an accessibility finding from a board summary because it "muddies the message". They are unsure what to do. What is the most effective response?

- A) Tell them to leave it in and say you said so.
- B) Talk it through so they understand what is at stake, agree together how the finding should be presented — including a constructive framing with mitigation — offer to attend the meeting, and take the request itself up with the director yourself.
- C) Contact the director and instruct them not to make such requests.
- D) Escalate to the head of profession.

**Correct answer: B. Least effective: A**

**Explanation:** Two things must happen: the finding survives, and the designer emerges more capable and less exposed. Option B does both. Talking it through builds their judgement rather than substituting yours; agreeing the presentation gives them something constructive to bring rather than a refusal; offering to attend supplies backing without takeover. Most importantly, taking the request up with the director is your job — a power differential of that size is what a senior colleague exists to absorb, and leaving them to manage it alone is a failure of mentoring even if the finding survives. Option A is least effective: it leaves them defending a position by proxy, teaches nothing, and reframes integrity as hierarchy. Option C treats a conversation as an instruction you are not positioned to give. Option D escalates something within your remit, though informing your head of profession if it recurs is sensible.

**Question 2 (easy) — Embedding practice in a resistant team**

You are asked to embed good interaction design practice in a delivery team that has never worked with a designer and whose delivery manager says design is welcome "as long as it doesn't slow us down". What is the strongest first move?

- A) Present the service standard's design requirements.
- B) Find the team's nearest consequential decision, offer to answer that specific question inside their sprint, and get developers and the delivery manager observing a session — so the value is demonstrated in their terms before you ask for more.
- C) Ask the programme director to mandate design involvement.
- D) Run a full discovery first.

**Correct answer: B. Least effective: C**

**Explanation:** A team that has never worked with a designer has no reason to believe design repays its cost, and no explanation substitutes for watching a user fail at something you built. Option B is calibrated to that: it answers a question the team actually has, fits their cadence rather than demanding a change to it, and gets them into a session as observers — which for a delivery team is unusually effective, because developers who watch someone struggle with a control they wrote tend to become the strongest advocates you have. Option C is least effective: mandated involvement is performed rather than used, and it makes you the director's enforcement mechanism, which poisons the relationships you need. Option A wins compliance and loses goodwill. Option D is right in ambition and wrong in sequence.

**Question 3 (easy) — A session producing one voice**

You are running a session with senior stakeholders and frontline staff. Twenty minutes in, two stakeholders dominate and no frontline staff have spoken. What is the most effective response?

- A) Let it run; the stakeholders know the service.
- B) Change the structure — write first then round the table, or split into pairs — so quieter participants contribute without anyone being told to stop.
- C) Ask the stakeholders directly to let others speak.
- D) Follow up with the frontline staff separately.

**Correct answer: B. Least effective: A**

**Explanation:** The session is producing one perspective when you convened it for several, and structural solutions outperform confrontational ones. Writing before speaking gives quieter participants time to form a thought and gives you a legitimate reason to change who is talking. Your role names adapting a design session to ensure you achieve a useful outcome, and this is precisely that. Option A is least effective: it wastes the frontline staff's time and produces a design based on how senior people imagine the work is done — which for interaction design is particularly costly, because caseworkers know exactly which fields get entered wrongly, which errors they see hundreds of times a week, and which workarounds already exist. Option C may succeed and creates avoidable friction. Option D does not rescue this session.

**Question 4 (moderate) — Advising on work that is not good enough**

A designer in another team, who does not report to you, has shipped a custom component whose focus behaviour traps keyboard users. It is now in two services. What is most effective?

- A) Raise it with the services using it.
- B) Speak to the designer and their lead first, describe the defect precisely with a reproduction, agree how it will be fixed and communicated to the services already using it — with a clear next step if they decline.
- C) Escalate to the head of profession.
- D) Advise the two services to stop using the component.

**Correct answer: B. Least effective: A**

**Explanation:** The defect needs fixing and the designer needs to remain a functioning colleague, and option B achieves both. Going to them first is not merely courteous: they may know something you do not, and if they do not, the fix lands far better from them. The reproduction matters — a vague report gets triaged low while a precise one gets fixed. And the clause about communicating to services already using it is the element most often omitted, without which a fixed component sits alongside two services still running the broken version. Option A is least effective as a first move: it bypasses the person who can actually fix it and starts a conversation about their competence in rooms they are not in. Option C is premature. Option D is disproportionate before a fix has been requested, though it becomes reasonable if the fix is refused.

**Question 5 (moderate) — Pressure to predetermine a conclusion**

A programme director tells you, before work starts, that the design work "needs to show the new single-page form will work, because that decision is effectively made". What is the most effective response?

- A) Focus the work on the form's strengths.
- B) State plainly that the work will report what users experience, and reframe around what they actually need — if the decision is made, the useful questions become who will struggle with a single long page, what support they will need, and what would signal the change is failing.
- C) Agree, then report honestly and handle the fallout.
- D) Refuse and report the conversation.

**Correct answer: B. Least effective: A**

**Explanation:** The request as phrased asks you to predetermine a conclusion, which would make the work worthless to everyone including the director. Option B declines the premise without a confrontation and redirects to something genuinely useful: if the decision really is made, work aimed at relitigating it wastes everyone's time, while work identifying who will struggle — people using screen magnification who must scroll a long page, people whose session times out partway, people who cannot find an error thirty fields up — is honest and directly valuable. That reframe converts an integrity problem into a scoping conversation. Option A is least effective: designing to demonstrate a conclusion is a rigged exercise, and rigged exercises surface. Option C leaves the expectation uncorrected and guarantees a worse conflict. Option D may become necessary and is not the first move.

**Question 6 (moderate) — Developing someone whose practice is weak**

A designer you mentor repeatedly ships components that work with a mouse and fail with a keyboard. You have raised it twice in general terms and it continues. What is the most effective next step?

- A) Review every component they produce before it ships.
- B) Move from general feedback to something structured: sit with them and operate one of their own components using only a keyboard, so they experience the failure rather than being told about it; then agree they will do that check themselves before anything ships, and review the next one together.
- C) Raise it in their performance conversation.
- D) Reassign component work to someone else.

**Correct answer: B. Least effective: A**

**Explanation:** Twice-repeated general feedback has not worked, which usually means the person agrees in principle and cannot yet see the problem in their own work. Option B addresses that directly and uses the mechanism specific to this discipline: watching your own component fail under your own hands is a categorically different experience from being told it fails, and designers who have done it once rarely need telling again. Agreeing a check they will run themselves makes it portable, and reviewing the next one closes the loop. Option A is least effective because it removes the problem from view while guaranteeing it persists, makes you a permanent bottleneck, and signals that you do not think they can learn. Option C is a legitimate component eventually and premature before a structured intervention. Option D protects the outputs at the cost of the person's development.

**Question 7 (moderate) — A technology constraint**

A technology team has selected a component library whose date picker and modal fail your accessibility standard. Two services already use it. What is the strongest approach?

- A) Require them to stop using the library.
- B) Establish precisely which components fail and how, propose a shortlist to avoid or wrap with compliant alternatives, and a route to remediate the two existing services — framing it as making their choice workable rather than reversing it.
- C) Escalate to the head of profession.
- D) Accept it and document the risk.

**Correct answer: B. Least effective: D**

**Explanation:** A library is almost never uniformly good or bad — the complex interactive components fail while the buttons and inputs are fine. Option B establishes which, converting an unwinnable argument about a decision already made into a tractable list of specific things to avoid or wrap. That reframe matters practically and politically: the team has built two services and cannot start again, so an answer requiring them to is an answer they will refuse, and you will have spent your standing for nothing. Option D is least effective because documenting a risk with nothing following it is how an exclusion becomes permanent while everyone feels they have handled it. Option A asks for reversal without a route. Option C escalates a solvable disagreement across a boundary you will need repeatedly.

**Question 8 (harder) — An accessibility blocker close to launch**

Two weeks before launch you find a custom component cannot be operated with a keyboard. Fixing it delays launch. What is most effective?

- A) Launch and add it to the backlog.
- B) Raise it immediately with the delivery manager and service owner, describe precisely what cannot be done and by whom, ask for an explicit recorded decision, and check whether a standard component could replace the custom one within the fortnight.
- C) Attempt the fix yourself.
- D) Launch and publish an accessibility statement noting the gap.

**Correct answer: B. Least effective: A**

**Explanation:** A component that cannot be operated by keyboard means some people cannot use the service, and weighing a delay against an exclusion is a decision for people with authority. Raising it precisely and now is squarely yours, and "explicit recorded decision" is what makes option B senior rather than merely diligent: an unrecorded decision drifts into launch by default, and a recorded one makes the trade-off owned by someone who can own it. The final clause adds the step most often missed under pressure — a standard component may substitute in days. Option A is least effective: the backlog is where accessibility problems go to remain unfixed. Option D treats a statement as a way to launch with a known blocker, which it is not; a statement discloses a gap you are closing. Option C risks a fortnight with nobody aware.

**Question 9 (harder) — Evidence against a public commitment**

Your work shows that a publicly announced change will make a service substantially harder for users with motor impairments. Colleagues propose presenting this as "areas for future enhancement". What is most effective?

- A) Accept the framing; the commitment is public.
- B) Report the findings accurately and do the constructive work alongside — quantify who is affected, specify what mitigation would look like, and present finding and mitigation together so the organisation has a route that is neither reversal nor denial.
- C) Report starkly and let the organisation respond.
- D) Escalate before acting.

**Correct answer: B. Least effective: A**

**Explanation:** The proposed framing protects the organisation from discomfort and produces the worst available outcome: the difficulty occurs anyway, nobody owns it, and evidence that could have driven mitigation has been defused. Option B keeps the finding intact and makes it actionable. Quantifying who is affected converts an abstract concern into something a delivery plan can address, and arriving with mitigation means the finding is not a problem dropped on people who cannot reverse an announcement. Option A is least effective — softening findings to accommodate a commitment is the precise failure your standards exist to prevent, and it falls hardest on the users least able to absorb it. Option C is accurate and unhelpful; at your level a finding without a route forward gets managed around. Option D is worth doing in parallel and is not a substitute.

**Question 10 (harder) — Consensus that would harm users**

A team you advise has converged on a control everyone likes, which your evidence indicates will fail users on small screens and users with motor impairments. Reopening it reverses a decision people are relieved to have made. What is most effective?

- A) Let it go; the team has decided.
- B) Raise it once, clearly and specifically, showing what the evidence indicates will happen to those users and what mitigation might look like — then if the team proceeds, ensure the risk is documented and propose measuring the outcome after release.
- C) Escalate to the service owner over the team's head.
- D) Keep raising it until the team changes course.

**Correct answer: B. Least effective: A**

**Explanation:** You have a professional obligation to say the thing and you also have to keep advising these people. Option B threads that: raise it once and properly, with evidence and a constructive mitigation rather than a veto; then if the decision stands, do the two things that protect users and your position — document the risk so the decision is knowing rather than accidental, and set up a measurement so reality gets a vote later. Documenting risks and unresolved issues is a named part of your role, and this is what it is for. Option A is least effective because consensus harming users who already have fewer options is not a value. Option C escalates before using the direct route and costs the team's trust. Option D substitutes persistence for persuasion, and an adviser who relitigates every decision stops being heard on any of them.

**Question 11 (harder) — A flaw in something you approved**

Three months ago you approved a pattern that is now used in five services. You realise its error handling assumes errors appear on the same page as the field, which breaks in the two services that use it across multiple pages. What should you do?

- A) Note it for the next pattern review.
- B) Tell the pattern's users now, scope precisely which services are affected and which are not, propose a fix to the pattern and an interim workaround for the two broken services, and review why the approval did not catch a multi-page case.
- C) Quietly amend the pattern documentation.
- D) Advise the two services to stop using the pattern.

**Correct answer: B. Least effective: C**

**Explanation:** A pattern used in five services means a flaw is potentially five defects, and the scoping matters as much as the disclosure — three services are fine, and telling them otherwise creates unnecessary work and erodes confidence in the pattern generally. Option B does all four necessary things: notifies, scopes precisely, fixes both immediately and durably, and — the element specific to your level — asks why the approval process did not test the pattern against a multi-page case, which is the question that prevents the next one. Option C is least effective: amending documentation without telling the two affected services leaves live defects in place while creating a record suggesting they were addressed. Option A defers a live problem. Option D is disproportionate when a workaround exists and would leave two services without a pattern at all.

**Question 12 (harder) — A recurring problem across teams**

Across three teams you advise, custom components keep being built where Design System components would serve. Each team has a plausible local reason. What is most effective?

- A) Review and challenge each proposal as it arises.
- B) Look for the common cause — most likely that the Design System components are genuinely missing something, or that teams do not know they exist, or that adopting them is harder than building fresh — then address whichever it is, and propose the corresponding change: contributing the missing variant, improving discoverability, or reducing adoption friction.
- C) Introduce a rule requiring approval for any custom component.
- D) Accept it; teams know their own needs.

**Correct answer: B. Least effective: D**

**Explanation:** Three teams doing the same thing for plausible local reasons is a pattern, and the plausibility of each local reason is precisely what makes case-by-case challenge exhausting and ineffective. Option B looks for the common cause and names the three realistic candidates, each of which implies a completely different remedy: if the Design System is genuinely missing a variant, the answer is to contribute it; if teams do not know what exists, the answer is discoverability; if adoption is harder than building fresh, the answer is reducing that friction, which is usually a tooling problem. Option A is sustainable only while you have capacity and stops the day you are busy. Option C adds a gate without addressing why teams are choosing this route, which produces either compliance theatre or a queue. Option D is least effective: accepting three teams independently rebuilding components is accepting three sets of accessibility defects and three maintenance burdens.

### Preparation tips

- **Answer as a senior practitioner.** Independent judgement, responsibility for others' practice, capability building alongside problem solving.
- **Check whether the option develops anyone.** Solving it yourself is frequently the second-best answer.
- **Absorb pressure downwards.** If a power differential is above the level of the person facing it, it is yours.
- **Let people experience the failure.** Operating their own component by keyboard teaches what feedback cannot.
- **Reframe unwinnable arguments into tractable lists.** "Which components, specifically?" beats "not compliant".
- **Look for the common cause behind three plausible local reasons.**
- **Ask for an explicit recorded decision.** Unrecorded decisions drift into launches.
- **Document the risk when you lose the argument.** It makes the decision knowing rather than accidental.

### Common pitfalls to avoid

- **Solving without developing.** The characteristic senior failure.
- **Becoming the permanent review bottleneck.** It hides the problem and guarantees it persists.
- **Softening findings to accommodate a commitment.**
- **Correcting a colleague's component by going to its users first.** Speak to the person, with a reproduction and a next step.
- **Documenting a risk and calling it management.** Nothing follows unless someone makes it.
- **Adding a gate instead of diagnosing why teams route around the existing path.**
- **Treating an accessibility statement as a way to launch with a blocker.**
- **Amending documentation instead of telling affected users.** It creates a record suggesting a fix that has not happened.

## Conclusion

You have reached the end, and it is worth registering what that involved: forty-eight questions across four assessment types, with the reasoning worked through on each. That is a serious piece of professional preparation and rather more than most senior candidates undertake.

Look back at the ground. In the cognitive section you audited a page as written rather than as you would have written it, named what three favourable test conditions had removed, weighted a pattern decision by the six services that would reuse it, reframed a shared component as an ownership decision rather than a design one, read a 40% return rate as a natural experiment with three distinct mechanisms, and read a concentration of accessibility failures as a process diagnosis. In the numeric section you recomputed when nothing matched, converted 1.2% into 10,800 people and knew who those people actually were, weighted rather than averaged, reconstructed an implied unit value, and declined to endorse a comparison that could not detect what it was built to find. In the verbal section you separated an exemption route from an alternative route, refused to mark False on a component you suspected would fail, distinguished an unconditional requirement from a scoping statement, and caught "consider whether" pretending to be a recommendation. And in the situational judgement section you absorbed a director's pressure on a designer's behalf, had someone operate their own component by keyboard instead of telling them a third time, converted "the library is not compliant" into a shortlist, and looked for the common cause behind three plausible local reasons.

A thread runs through all of it. Almost every item was asking two things at once: do you know the limits of what you have, and can you act on the mechanism rather than the instance? Those two capabilities are most of what your role consists of. Teams can generate opinions without you and read dashboards without you. What you supply is a design rationale that holds when someone pulls at it, and a practice around you that keeps producing them.

A word about the particular difficulty of your level. The errors that cost you most are no longer the ones you would notice. They are made fluently, in areas where your experience runs deep enough that checking feels unnecessary — and the verbal reasoning section is the clearest demonstration, because expertise measurably costs marks there. The senior designers whose judgement holds up across a career kept a habit of deliberate scepticism about their own reasoning long after it stopped feeling required.

If you want to build on this, a few things repay effort more than rereading. Audit a pattern you approved and ask which service contexts it was never tested against. Complete a service you are responsible for using only a keyboard, then with a screen reader, then at 400% zoom — three passes, three classes of defect. Trace three figures in a live business case back to source. Take a technology constraint you have accepted for months and ask precisely what it is. And the next time you give a designer feedback that has not landed twice already, have them experience the failure rather than saying it a third time.

Finally, for the day itself. An assessment samples your reasoning on one morning under artificial conditions. It is not a verdict on your judgement or your career. Read the stem twice, set expertise aside in the verbal section, find the denominator, trust Cannot Say, and remember that at your level the strongest answer is usually the one honest about uncertainty and aimed at the mechanism rather than the symptom.

Good luck. Go carefully, ask what things are for, and keep unplugging the mouse.
