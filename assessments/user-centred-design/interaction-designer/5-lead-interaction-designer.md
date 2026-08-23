# Lead Interaction Designer - Psychometric Assessment Resources

## Introduction

Welcome. This guide is written for you as a lead interaction designer in the UK Government Digital and Data profession — an expert practitioner who influences and mentors others, works with service managers and programme directors to develop design concepts, sets direction and assures the quality of design delivery across teams, and leads multiple or highly complex services. Your role description is notably organisational: you gain support for design strategy from senior leaders, communicate it across organisational boundaries, coach others, measurably improve inclusive design practice across multiple teams, embed hypothesis-driven and iterative working, ensure insight reaches the wider organisation and across government, and create the conditions in which designers can do good work.

You may be facing a formal assessment as part of a selection process, or you may want to re-examine reasoning that has become fluent enough to be worth checking. Both are good reasons, and the second is the more interesting. At your level the risk is not that you lack technique but that technique has become automatic, automatic reasoning feels certain, and nobody in your organisation is positioned to catch you.

Three features of the role shape everything that follows. First, you are accountable for design quality you did not produce, frequently on services you have not seen, judged from outputs rather than from the work behind them — which makes diagnostic reasoning at a distance a core competence. Second, you work at the level of systems rather than screens: patterns, component libraries, design systems, assurance routines and the conditions of work. A decision at that level is paid for many times, in maintenance, in the expectations it sets, and in the accessibility characteristics it propagates. Third, your authority is largely informal. You do not line-manage most of the people whose practice you assure, you cannot compel a team, and you influence leaders who outrank you.

The document has four main sections:

1. A workplace job-specific cognitive assessment — evidence auditing at a distance, cross-service synthesis, systemic diagnosis, strategic prioritisation, and reasoning about organisational mechanisms.
2. A numeric reasoning assessment — weighted aggregation, funnel and cohort data, sampling adequacy, business case and vendor claims, and the interrogation of figures already embedded in decisions.
3. A verbal reasoning assessment — governance frameworks, audit reports, cross-government standards and technical specifications, with items pitched at real ambiguity.
4. A situational judgement assessment — ethics and inclusion at scale, assurance across boundaries, coaching and conditions, and the defence of design positions in senior forums.

Each section provides an overview, a mapping to your named skills, twelve practice questions with full explanations, preparation tips, and common pitfalls.

Several items have an attractive answer that is wrong for a reason worth understanding. Commit before reading, and attend particularly where you were quick and sure.

Let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive assessment measures the reasoning your role demands, presented through practical materials rather than abstract puzzles. At lead level the materials are organisational and the reasoning is diagnostic and strategic. You will meet evidence assembled by other people for other purposes, standards applied unevenly across teams, findings that appear to conflict until you establish what each measured, and prioritisation problems whose units are services and shared assets rather than screens.

The format is typically an online test of fifteen to thirty minutes covering pattern recognition, logical deduction, error checking, prioritisation and applied problem solving. Scoring is objective against a norm group of comparable seniority. Adaptive platforms raise difficulty after correct answers, and acuity reports distinguish speed from accuracy, both rewarding precision.

Three things characterise this section at your level.

The first is reasoning at a distance. You rarely see the work; you see an output, a component, a claim in a board paper, and must judge from visible traces whether the reasoning underneath holds.

The second is that the interesting questions concern mechanisms. When something goes wrong repeatedly, the informative feature is the distribution of the failures. Concentrated in one team under one condition among experienced people? That is a process telling you it cannot be complied with. Scattered? Something else.

The third is the multiplier. Because your decisions concern shared assets — patterns, components, standards, routines — several items ask you to weigh a decision by how many times it will be paid for. A component adopted by twelve services carries its defects twelve times and its virtues twelve times, and is far harder to change than to introduce.

You need to memorise nothing. What you need is the discipline not to let fluency substitute for examination.

### How this assessment maps to your role

The cognitive dimensions map onto the skills named in your role summary:

- **Auditing at a distance** maps to setting direction and assuring the quality of design delivery across teams.
- **Cross-service synthesis** maps to **Evidence-based design**, where you analyse, synthesise and use evidence to improve how the organisation works, and ensure insight is shared across the organisation and government.
- **Systemic diagnosis** maps to **Iterative design**, where you iterate delivery processes or team structures to help teams work effectively.
- **Strategic prioritisation** maps to **Designing strategically**, where you use risks, opportunities and constraints in technology, systems and policy to shape design.
- **Diagnosing structural exclusion** maps to **Designing for everyone**, where you measurably improve inclusive practice across multiple teams.
- **Reasoning about positions and incentives** maps to **Design communication**, where you gain support from senior leaders and communicate across organisational boundaries.

### Practice questions

**Question 1 (easy) — Auditing against a standard**

Your organisational standard requires every component entry to state: the problem it solves, when not to use it, its keyboard behaviour, its assistive technology behaviour, known limitations, and the date last reviewed. An entry states the problem, keyboard behaviour, and date; describes assistive technology behaviour as "tested and works"; and has no "when not to use" or known limitations. How many requirements are unmet?

- A) 1
- B) 2
- C) 3
- D) 4

**Correct answer: B**

**Explanation:** Work through all six. Problem, keyboard behaviour and date are present. "Tested and works" is a statement about assistive technology behaviour — thin, but it addresses the requirement, so it is met at a minimum level. "When not to use" is absent, so that fails. Known limitations are absent, so that fails. Two unmet, giving B. Option C typically comes from rejecting "tested and works" as insufficient, which is a defensible design judgement and the wrong assurance judgement — the discipline is to apply the standard as written. Note which two failed, because at your scale the pattern matters more than the instance: "when not to use" and "known limitations" are the two most commonly omitted fields in component documentation everywhere, and their absence is what produces components used in situations they were never designed for. That tells you to fix the template and the review prompt rather than this one entry.

**Question 2 (easy) — Deduction from a governance rule**

Your standard states: "A custom component may enter a live service only with design assurance sign-off, unless it replaces an existing custom component on a like-for-like basis and has been assessed as low risk." A programme reports: "We shipped a custom component last month without sign-off." Which must be true?

- A) The standard was breached.
- B) It was a low-risk like-for-like replacement.
- C) Either it was a low-risk like-for-like replacement, or the standard was breached.
- D) The component should be withdrawn.

**Correct answer: C**

**Explanation:** A conditional with a stated exception, plus facts silent on the exception, licenses only the disjunction. Options A and B each assume a branch. Option D prescribes an action rather than stating what must be true, and the question asks the latter — worth noticing, because at this level a sensible action is frequently offered as a distractor in a logic item and may well be what you would do. Only C holds. Note the compound exception: like-for-like *and* low risk. Partial satisfaction is not satisfaction, and it is the most common misreading in real governance conversations. As the person who owns this standard, your opening move is to establish which route was taken, framed as an enquiry — because an accusation you have to withdraw costs more than the fortnight it takes to ask.

**Question 3 (moderate) — Reading a study from its output**

An output states: "Users find the new autocomplete easy — all 22 participants completed the task without difficulty." It notes that the facilitator demonstrated the component first, participants came from the departmental panel, and all used a laptop with a mouse. What is the most important observation?

- A) Twenty-two participants is too small a base.
- B) The demonstration, the panel recruitment and the mouse-only conditions each remove a distinct source of the difficulty this kind of component characteristically produces — first encounter, unfamiliarity, and keyboard or assistive technology operation — so the result describes an unusually favourable case rather than the component's usability.
- C) "Easy" is not a measurable construct.
- D) A think-aloud protocol should have been used.

**Correct answer: B**

**Explanation:** Unanimity is the alarm, and the strongest observation explains it by identifying what the conditions removed. Demonstrating first eliminates the first-encounter difficulty autocompletes characteristically produce; a departmental panel is populated by people comfortable with government interfaces; and testing exclusively with a mouse skips the operation mode where custom autocompletes most often fail outright. Each removes a distinct source of difficulty, leaving a test that could hardly have produced another result. Option C is a fair secondary point about measurement. Option A misdiagnoses validity as size — 220 participants under identical conditions would produce the same finding. Option D is a technique fix leaving all three conditions in place. When this feeds back, name what each condition removed: a designer who adds think-aloud while keeping the demonstration gets the same answer and believes it more.

**Question 4 (moderate) — Strategic prioritisation**

You can direct substantial design capacity to one of four things this quarter:

1. A pattern for identity checks is being decided next month and will be reused across seven services.
2. A live service has a persistent 30% drop-off at one step, affecting 400,000 users a year.
3. A service launches in five weeks with designs signed off.
4. A programme is preparing a spending review submission due in eight months.

Which is strongest?

- A) Item 2, because it affects the most users.
- B) Item 1, because the decision is imminent, will be reused seven times, and design input is the only thing that could still shape it — and a pattern embeds its characteristics into every service that adopts it, becoming a coordination problem across seven teams rather than a design problem once adopted.
- C) Item 4, because spending review submissions shape long-term investment.
- D) Item 3, because launching untested carries reputational risk.

**Correct answer: B**

**Explanation:** Value of information is the right frame, and item 1 carries a multiplier the others lack. A pattern decided once and reused seven times embeds either a good decision or a bad one seven times over, and the cost of changing it rises with every adoption — after a year, changing a widely used pattern requires coordinating seven teams' release schedules, which is why patterns are so much easier to get right than to fix. Item 2 affects more users today but has been stable for months. Item 3 is weakest despite sounding prudent: signed-off designs five weeks from launch means findings arrive with nowhere to go. Item 4 has eight months, and at your level the profile trap takes exactly this form — spending review work attracts attention, and attention is not decision leverage.

**Question 5 (moderate) — Cross-service synthesis**

Three unrelated items reach you in a month. A team reports users struggling to prove identity without a passport or driving licence. Analytics in a second service show 45% drop-off at identity verification. The contact centre reports identity queries as its highest call driver across five services. What is the strongest synthesis?

- A) Three teams have found usability problems at their identity steps.
- B) The organisation has a cross-cutting identity assurance problem concentrated among people without common photographic documents — a strategic capability question rather than five separate interaction fixes, and one where five teams each building a workaround produces five partial solutions and five sets of excluded users.
- C) Identity verification is hard and should be simplified.
- D) The findings are unrelated.

**Correct answer: B**

**Explanation:** The synthesis that adds value identifies a shared mechanism and reframes the unit of the problem. Five services showing difficulty at the same step, with a discovery pointing at document availability and contact centre volume confirming scale, indicates something structural. Option B also draws the consequence, and the second clause is what makes it a lead's answer rather than an analyst's: five teams solving this locally is not merely wasteful but actively harmful, because each will build a partial workaround and the excluded population will remain excluded five times over, in five slightly different ways that nobody can then fix centrally. Option A describes without synthesising. Option C is true and strategically useless. Option D misses the pattern.

**Question 6 (moderate) — Scope of a claim heading for a pattern**

A designer proposes a new pattern, arguing that "users expect to save and return at any point", supported by four studies all of services taking more than two weeks to complete. What is the most useful intervention?

- A) Reject the pattern.
- B) Note that the evidence comes exclusively from multi-week services, so the claim over-reaches as written; narrow the pattern's stated applicability, or test whether the expectation holds in short services, before it becomes something every team is expected to implement.
- C) Commission more studies.
- D) Accept it; four studies is a reasonable base.

**Correct answer: B**

**Explanation:** The evidence is real and the sentence built on it reaches further than the evidence goes — the most common failure in synthesis, and one with unusual consequences here because the claim is destined to become a pattern with an implied obligation attached. Multi-week services supply an obvious reason to expect saving and returning: you cannot finish in one sitting. That expectation may not transfer to a five-minute service, where a save-and-return control adds a decision, occupies space, and creates an abandoned-session problem for no benefit. Option B preserves the finding and corrects the scope — and notice that the fix here is to the pattern's stated applicability, which is exactly the field that Question 1 identified as most commonly omitted. Option A discards something real. Option D imposes an obligation on every team on evidence from one service type. Option C reaches for the expensive remedy before the free one.

**Question 7 (moderate) — Diagnosing a systemic problem**

Six teams keep building custom components where Design System components would serve. Each has a plausible local reason. What is the strongest diagnosis and response?

- A) Review and challenge each proposal as it arises.
- B) Six teams doing the same thing for plausible local reasons is one systemic cause with six local rationalisations; establish which of the realistic candidates it is — the components are genuinely missing a needed variant, teams do not know what exists, or adopting is harder than building fresh — and address that, because the corresponding remedies are entirely different.
- C) Introduce a rule requiring approval for any custom component.
- D) Accept it; teams know their own needs.

**Correct answer: B**

**Explanation:** Six teams behaving identically for individually plausible reasons is the signature of a systemic cause, and the plausibility of each local reason is precisely what makes case-by-case challenge exhausting and ineffective — you win each argument and the behaviour continues. Option B names the three realistic candidates, and the point is that they imply completely different remedies: contributing the missing variant, improving discoverability, or reducing adoption friction, which is usually a tooling or documentation problem rather than a design one. Diagnosing wrongly wastes a quarter. Option A is sustainable only while you have capacity and stops the day you are busy. Option C adds a gate without addressing why teams route around the existing path, producing a queue and compliance theatre. Option D accepts six sets of accessibility defects and six maintenance burdens.

**Question 8 (harder) — Scoping a flaw**

A study you are assuring used a prototype whose "back" function was broken. Four findings: (i) participants could not locate the eligibility criteria; (ii) participants abandoned after a wrong turn; (iii) sessions ran long; (iv) participants misread the declaration. Which are compromised?

- A) All four.
- B) None; the fault was incidental.
- C) Findings (ii) and (iii) are directly compromised, since inability to go back plausibly produced both, while (i) and (iv) concern comprehension of content and are largely unaffected.
- D) Only (ii).

**Correct answer: C**

**Explanation:** The skill is scoping precisely rather than treating a flaw as total or trivial. A broken back function prevents recovery from a wrong turn, manufacturing abandonment and inflating durations, so (ii) and (iii) cannot be separated from the artefact. Findings (i) and (iv) concern locating and understanding content, which the fault does not touch. Option A discards two sound findings and, at organisational scale, does real damage: a leader who condemns wholesale teaches teams that any admitted prototype fault invalidates everything, which is a direct incentive to stop declaring faults — and you will then be assuring studies whose problems have been quietly omitted, which is worse than the original situation because you no longer know. Option B leaves two artefactual findings circulating. Option D misses the duration compromise.

**Question 9 (harder) — Apparent contradiction between teams**

Two teams reach opposite conclusions about the same control: one finds users prefer a single combined date field, the other that users prefer three separate inputs. Both studies appear sound. What is strongest?

- A) Commission a third study.
- B) Establish what differs between the contexts before treating it as a contradiction — the date being entered may differ, since a date of birth is recalled and typed while an appointment date is chosen from a known range, and the synthesis is that the right control depends on whether the user already knows the value.
- C) Report both and note the inconsistency.
- D) Treat the larger study as authoritative.

**Correct answer: B**

**Explanation:** Apparent contradictions between sound studies are usually context differences in disguise, and the diagnostic move is to ask what each participant was actually doing. Someone entering a remembered date of birth is transcribing a value they hold; someone selecting a future appointment is choosing among options. Those are different tasks and reward different controls, which is why both findings can be correct. Option B reaches the synthesis, and note that the synthesis is more valuable than either original finding: it gives every team in the organisation a rule for choosing, which neither study alone could, and that generalisable rule is precisely what your role exists to extract and propagate. Option A spends money on a question that dissolves. Option C abdicates the synthesis — "note the inconsistency" is how insight gets filed as a caveat. Option D picks a winner on an irrelevant criterion.

**Question 10 (harder) — Reading the distribution of failures**

Your standard requires accessibility assurance before public beta. Across the year, fifteen of nineteen services complied; the four that did not were all in one directorate, all under ministerial deadline pressure, all by experienced practitioners. What is the strongest response?

- A) Report the four and require remediation.
- B) Treat the concentration as diagnostic: four failures in one directorate under identical pressure by people who know the requirement indicates a process that cannot be complied with under deadline conditions — investigate what it demands and how long it takes, build a fast route, and remediate the four alongside.
- C) Remind all designers of the requirement.
- D) Introduce a mandatory pre-beta gate for every service.

**Correct answer: B**

**Explanation:** The distribution is the most informative feature. Scattered breaches would indicate conduct; four concentrated under identical pressure by experienced practitioners indicate a process that does not survive a deadline. Option B investigates the mechanism and fixes it, while the remediation clause preserves the point that a systemic diagnosis is not a reason to leave individual failures unaddressed — real users cannot use four services now. Option A treats the instances and guarantees recurrence. Option C is the weakest available response to any compliance failure. Option D imposes friction on fifteen compliant services to catch four, which is how organisational burden accumulates — and you are the person who will be asked in two years why design governance is so slow, defending a gate you introduced.

**Question 11 (harder) — Evidence for an investment decision**

The organisation is deciding whether to adopt a third-party component library. Available: an internal audit finding accessibility defects in four of its components; a supplier claim of full WCAG conformance; two teams reporting faster delivery with it; and a maintenance cost model. What is your most rigorous contribution?

- A) Oppose adoption on the basis of the audit.
- B) Set out what each source establishes and its limits — including that "full conformance" claims typically cover components in isolation under default configuration rather than as integrated and customised, which is where defects arise — and name the one or two unknowns that would most change the decision.
- C) Support adoption on the delivery evidence.
- D) Recommend further audit before deciding.

**Correct answer: B**

**Explanation:** Your contribution at an adoption decision is neither advocacy nor delay; it is making the evidence base legible so the decision is taken knowingly. Option B does three things. It states what each source supports rather than letting a conformance claim and an audit finding be treated as a straight contradiction. It identifies the specific reason they can both be accurate — conformance claims are typically established for components in isolation with default settings, while defects appear once components are composed, customised and placed in a real page with real focus management. And it names the residual uncertainty, which tells decision-makers what their choice rests on. Option A opposes on partial evidence and forgoes real delivery benefits. Option C ignores the audit. Option D defers a decision the evidence may already support, and leads who reflexively call for more evidence find themselves excluded from decisions.

**Question 12 (harder) — A pattern across your own teams**

Reviewing a year of outputs, you find two teams consistently produce accessible components and five consistently do not. Both strong teams include a developer who previously worked in accessibility consultancy. What is the most useful inference and action?

- A) The five weaker teams need accessibility training.
- B) Something transferable is likely operating in the two strong teams — a routine, a check, a habit of testing in a particular mode — and the highest-value action is to find out what it actually is by watching how they work, then build it into the organisation's standards and tooling rather than attributing the difference to individual expertise.
- C) Recruit more people with accessibility backgrounds.
- D) Increase assurance scrutiny on the five weaker teams.

**Correct answer: B**

**Explanation:** The pattern is an opportunity to identify a practice, not to grade people. Teams producing consistently better components are almost always carrying a routine — testing every component with a keyboard before it leaves the branch, running an automated check in the pipeline, a rule that nothing merges without a screen reader pass — and routines transfer in a way that expertise does not. Option B goes and looks, which is the step almost everyone skips in favour of an assumption. Option A posits a knowledge deficit without diagnosing one, and accessibility training that does not attach to a routine is among the least effective interventions in the field. Option C is unusable as an inference from two people and misattributes a routine to a pedigree. Option D catches more defects and creates no capacity to prevent them. Your role names measurably improving inclusive practice across multiple teams — and a naturally occurring comparison telling you what good looks like in your own context is the best material that work will ever get.

### Preparation tips

- **Read outputs for the work behind them.** Infer conditions, recruitment and mode of operation from what an output says and omits.
- **Scope flaws precisely.** Wholesale condemnation teaches teams to stop declaring faults.
- **Weight decisions by reuse.** A pattern used seven times is worth seven times the attention and is far harder to change than to introduce.
- **Read the distribution of failures.** Concentrated non-compliance diagnoses a process; scattered diagnoses conduct.
- **Look for one cause behind several plausible local reasons.**
- **Ask what conformance claims actually cover.** Isolation and default configuration, usually — not composition and customisation.
- **Go and look before inferring a cause.** Especially when the inference flatters an assumption you hold.
- **Fix the template, not the entry.** A recurring documentation gap is a template problem.

### Common pitfalls to avoid

- **Applying a standard as you would have written it.** Assurance means applying it as written.
- **Reaching for training as the answer to a systemic problem.**
- **Reminding people of rules they knowingly missed.** The weakest available compliance response.
- **Adding friction for the compliant majority.** You will have to defend the gate later.
- **Challenging plausible local reasons case by case.** You win each argument and the behaviour continues.
- **Picking a winner between contradictory studies.** The insight lives in the difference between contexts.
- **Filing a contradiction as a caveat.** That is where organisational insight goes to die.
- **Letting fluency substitute for examination.** At your level the costly errors are the confident ones.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A numeric reasoning assessment measures how accurately you handle quantitative material. At lead level the emphasis is almost wholly on interrogation. You will need to compute correctly, but the questions that matter ask whether a figure means what somebody claims — and in most rooms you enter, you may be the only person who will ask.

The format is typically a timed online test of fifteen to thirty minutes, each item presenting a table, chart or paragraph of figures with a multiple-choice question. Calculators are usually provided and the arithmetic is deliberately tractable. Time per item is tight, so the operative skill is locating what matters and discarding what does not.

The professional stake is large. Quantitative evidence carries unearned authority: a number in a board paper is a fact, a design argument is a view, regardless of the rigour behind either. The figures you encounter are increasingly consequential and increasingly detached from anyone who could explain them — business cases, vendor conformance claims, benefits figures, performance metrics copied between documents for years without the definition being re-checked. Your role names gaining support for design strategy from senior leaders, and in practice that frequently reduces to whether you can engage credibly with the numbers those leaders work from.

Four habits carry most of the load. Establish what the question asks before looking at the data. Identify the denominator and the population it represents before calculating. Estimate, calculate, compare. And sanity-check against the world.

Distractors come from a predictable catalogue: wrong denominator, percentage confused with percentage point, new value as the base in a percentage change, rates averaged without weighting, vendor metrics compared with internal ones.

### How this assessment maps to your role

The numerical skills tested map onto your named skills:

- **Interrogating quantitative claims** maps to assuring the quality of design delivery across teams.
- **Aggregating across services** maps to **Evidence-based design**, where you analyse, synthesise and use evidence to improve how the organisation works.
- **Comparing rates between groups and modes** maps to **Designing for everyone**, where you measurably improve inclusive practice across teams.
- **Judging sampling adequacy** maps to **Evidence-based design**, where you embed hypothesis-driven design.
- **Presenting figures at defensible strength** maps to **Design communication**, where you gain support from senior leaders.
- **Detecting misleading metrics** maps to **Designing strategically**, where a wrong metric shapes design wrongly and does so across every team using it.

### Practice questions

**Question 1 (easy) — Rate from counts**

Of 8,000 users who reached a page, 2,000 triggered a validation error on one field. What percentage?

- A) 20%
- B) 25%
- C) 30%
- D) 40%

**Correct answer: B**

**Explanation:** 2,000 ÷ 8,000 = 0.25, so 25%, and the answer is B. Estimate first: 2,000 of 8,000 is a quarter. Options A and C come from dividing by 10,000 and 6,667. At your level the more consequential question is whether the field belongs to a shared pattern, because if so the same rate is being produced everywhere the pattern is used, and the value of fixing it is multiplied by the number of adopting services rather than confined to this page.

**Question 2 (easy) — Drop-off against the right base**

A page is reached by 10,000 users and passed by 7,500. What is the drop-off rate?

- A) 25%
- B) 33%
- C) 75%
- D) 30%

**Correct answer: A**

**Explanation:** The drop-off is 2,500, measured against arrivals: 2,500 ÷ 10,000 = 0.25, giving A. Option B divides by those who continued — the most common error in page analytics, overstating every drop-off it touches. At your level the consequence is not one wrong figure but a wrong organisational picture: if teams compute pages with different denominators, the ranking of where design capacity should go is distorted, and you adjudicate that ranking. A single line in your standard specifying the denominator is among the cheapest quality interventions available, and one of the few that fixes a whole class of error permanently.

**Question 3 (easy) — Disaggregated rates**

| Group | Users | Completed |
|---|---|---|
| Mouse users | 18,000 | 16,200 |
| Keyboard-only users | 1,400 | 700 |
| Screen reader users | 600 | 150 |

What is the overall completion rate, and the gap between highest and lowest group rates?

- A) 85% overall; 50 point gap
- B) 85% overall; 65 point gap
- C) 90% overall; 65 point gap
- D) 88% overall; 40 point gap

**Correct answer: B**

**Explanation:** Completions total 16,200 + 700 + 150 = 17,050, across 18,000 + 1,400 + 600 = 20,000 users, so 17,050 ÷ 20,000 = 85.25%, rounding to 85%. Group rates are 90%, 50% and 25%, giving a 65 point gap. Hence B. Option C mistakes the dominant group's rate for the overall rate, which is the characteristic error when one group makes up 90% of the sample — and it is worth noticing how nearly right it feels. That is the point. The overall figure of 85% describes no group here and conceals that screen reader users fail three times in four. A standard that does not require disaggregation by mode of operation has a hole in it shaped precisely like the users least able to complain, and writing that requirement into your standard is worth more than any individual finding.

**Question 4 (easy) — Centre and spread**

Thirteen sessions produced task times in seconds: 12, 15, 18, 20, 22, 25, 28, 30, 35, 40, 45, 50 and 300. Which summary is most defensible?

- A) Mean 49.2 seconds
- B) Median 28 seconds, range 12 to 300, with the 300-second case described separately
- C) Median 28 seconds
- D) Mean 49.2 seconds, range 12 to 300

**Correct answer: B**

**Explanation:** The mean of about 49 exceeds eleven of the thirteen observations, so it represents almost nobody. The median is the seventh value, 28 seconds, which describes the group well. But the median alone conceals a session lasting more than ten times the typical duration, which is almost certainly the most informative observation in the set. Option B gives centre, spread and explicit treatment of the outlier. Option D pairs the range with a misleading centre. Option C buries the extreme case. The rule to write into your standard: a central figure never travels alone, and an outlier is a lead to investigate rather than noise to absorb — the person who took 300 seconds hit something the other twelve did not.

**Question 5 (moderate) — Weighted aggregation**

Four studies of a component: 15 participants at 40% success; 25 at 60%; 10 at 70%; 30 at 80%. What is the overall rate across all 80?

- A) 62%
- B) 65%
- C) 66%
- D) 68%

**Correct answer: B**

**Explanation:** Convert each rate to counts. Study 1: 40% of 15 = 6. Study 2: 60% of 25 = 15. Study 3: 70% of 10 = 7. Study 4: 80% of 30 = 24. Total 6 + 15 + 7 + 24 = 52, across 80 participants, so 52 ÷ 80 = 0.65, which is 65% and the answer is B. Option A is the unweighted mean of 40, 60, 70 and 80, which is 62.5 and over-weights the two smallest studies at the expense of the 30-participant study that should dominate. Always return to counts, and re-check the total before it leaves your hands — at your level a plausible-looking figure travels on your authority and nobody downstream will question it. Ask the prior question too: aggregating four studies of a component is meaningful only if the task and population were comparable.

**Question 6 (moderate) — Funnel denominators**

Funnel: 160,000 start, 120,000 pass identity, 72,000 upload evidence, 64,800 submit. What proportion of those who passed identity went on to submit?

- A) 40.5%
- B) 54%
- C) 60%
- D) 90%

**Correct answer: B**

**Explanation:** The stem names users who passed identity, so the denominator is 120,000 and the part is 64,800: 64,800 ÷ 120,000 = 0.54, giving B. Option A uses 160,000, option C is the identity-to-upload rate, option D is the upload-to-submit rate. All are true of this funnel; one answers the question. Strategically the funnel shows where capacity belongs: 40,000 lost at identity and 48,000 between identity and upload, against 7,200 at submission. A team proposing to redesign submission would need a strong reason, and being able to establish that in fifteen seconds is what lets you redirect a programme in the meeting rather than a month later.

**Question 7 (moderate) — A benefits claim**

A benefits paper states a change raised completion from 60% to 72%, describing it as "a 20% improvement". Is that accurate?

- A) No; it is a 12% improvement.
- B) Yes as arithmetic — 12 ÷ 60 = 20% relative increase — but the expression is ambiguous, and the paper should state either "20% relative increase" or "12 percentage points".
- C) No; it is 12 percentage points and calling it 20% is wrong.
- D) No; it should be 16.7%.

**Correct answer: B**

**Explanation:** The relative increase is 12 ÷ 60 = 0.2, so 20% is defensible arithmetic. The problem is labelling: "a 20% improvement" will be read by many as a rise from 60% to 80%. Option B captures both halves. Option C over-corrects into an error of its own. Option A confuses the units; option D divides by the new value. At your level this is governance rather than arithmetic: benefits papers routinely select the flattering framing, usually without intent to mislead, and an organisation where nobody asks for both numbers will eventually publish one it cannot defend. Requiring both as a standing convention costs no political capital, because it is a rule about documents rather than a challenge to a person.

**Question 8 (moderate) — A conformance claim**

A supplier states their component library is "fully WCAG 2.2 AA conformant". Your internal audit found defects in four components. What is the most important question before treating these as contradictory?

- A) Whether the audit was conducted competently.
- B) What the conformance claim actually covers — most such claims are established for components in isolation under default configuration, while defects typically arise once components are composed, customised and placed in a real page with real focus management, so both statements can be accurate about different things.
- C) Whether the claim is current.
- D) Whether the supplier has other government clients.

**Correct answer: B**

**Explanation:** Conformance claims and internal audits routinely disagree without either being wrong, and the reason is scope. A supplier tests a component in a demonstration harness with default settings; your teams compose several components on a page, override styles, add validation, and manage focus between them. Defects appear at the joins. Option B identifies this, which converts an apparent contradiction into a specific and answerable question about what was tested. Options A, C and D are reasonable due diligence that does not touch the discrepancy, and asking them instead produces the appearance of scrutiny without its substance — which is worse than asking nothing, because it satisfies the room. This is among the highest-value contributions available to you in a procurement discussion and one almost nobody else is positioned to make.

**Question 9 (moderate) — Reconstructing an implied value**

A business case claims a 5 percentage point completion improvement on 1.6 million annual starts is worth £9.6 million a year. What is the implied value per additional completed application?

- A) £6
- B) £60
- C) £120
- D) £240

**Correct answer: C**

**Explanation:** A 5 percentage point improvement on 1.6 million starts gives 0.05 × 1,600,000 = 80,000 additional completions. Dividing: £9,600,000 ÷ 80,000 = £120, so C. Option A divides by 1.6 million, valuing every start. This takes thirty seconds and immediately tells you whether a business case is plausible — £120 per additional completed application may be reasonable for a high-value transaction and implausible for a simple information service. The challenge it enables is far more effective than disputing a total: "so we are valuing each additional completion at £120 — is that the right order?" is specific, answerable, and requires accusing nobody, which matters when the author is a peer you need next month.

**Question 10 (harder) — A metric that conflates populations**

A board paper reports "average time to complete: 11 minutes" for a service your evidence shows most users taking over forty minutes across several sittings. What is the likely explanation and the right intervention?

- A) The board paper is wrong and should be corrected.
- B) The metric almost certainly measures single sessions rather than end-to-end journeys, so multi-sitting completions are excluded or counted only for their final short visit, and abandoned sessions may be included — ask for the definition and the distribution, and propose an end-to-end measure alongside it.
- C) The research sample was atypical.
- D) The figures cannot be reconciled.

**Correct answer: B**

**Explanation:** Session-based analytics and journey-based reality diverge systematically for any service completed over more than one sitting, and the divergence always flatters the service. Someone spending forty minutes across three visits typically appears as one short final session, and abandoned sessions drag the mean lower still. The figure is probably calculated correctly and defined in a way that cannot answer the question the board believes it answers. Option B names the mechanism and proposes a constructive intervention — asking for a definition is not an accusation, and offering an end-to-end measure gives the metric owner something to build rather than something to defend. Option A picks a fight over a number that is not wrong, which is how leads acquire a reputation for obstruction and then find themselves invited to fewer meetings. Option C blames the research. Option D forecloses a useful reconciliation.

**Question 11 (harder) — Sampling adequacy**

A directorate proposes measuring whether a redesign improved completion by running 50 moderated sessions before and 50 after. Baseline is 62%; a 5 percentage point improvement is meaningful. What is the strongest response?

- A) Agree; 100 sessions is substantial.
- B) Explain that a 5 point difference on 50 per group is two or three participants and well inside ordinary variation, so the comparison cannot detect it — recommend measuring the rate through live analytics across the full user base and spending the 100 sessions on mechanisms, which moderated research does uniquely well.
- C) Increase to 80 per group.
- D) Run it and report the difference with caveats.

**Correct answer: B**

**Explanation:** Fifty per group cannot distinguish a five point difference from chance; reliable detection needs several hundred per group. Option B says so and redirects rather than merely objecting: analytics measures rates across the whole population at negligible marginal cost, while moderated sessions are the only instrument that explains why a rate is what it is. Option A endorses a design that cannot answer its own question. Option C moves towards adequacy without reaching it. Option D is the most damaging at organisational level, because caveated findings from underpowered comparisons get cited without their caveats — and once your organisation establishes that fifty-session comparisons can measure rates, you will be arguing against that precedent for the rest of your tenure, usually against someone quoting a study you let through.

**Question 12 (harder) — A claim already in a board paper**

A board paper states: "Testing confirms 93% of users can complete the service independently." You trace it to a study of 43 participants, 40 of whom completed, all recruited through the departmental panel and all using a mouse. The board meets in four days. What is most important?

- A) Ask for the figure to be removed.
- B) Go to the author, explain that 43 panel-recruited mouse users cannot support a population rate — and that the mouse-only condition specifically excludes the modes where failure concentrates — propose the accurate statement, offer what the organisation does have if a rate is needed, and confirm the correction is made before the paper is tabled.
- C) Raise it at the board.
- D) Note it for the next assurance cycle.

**Correct answer: B**

**Explanation:** A qualitative sample from a self-selected panel has become a population statistic in a document informing a decision — a category error rather than a rounding one — and the mouse-only condition compounds it by excluding precisely the modes where completion failure concentrates, which is what makes 93% both unsupported and specifically flattering. Option B does the four things that matter: goes to the author first, names precisely what the evidence supports and why, offers an alternative source so the board is not left with a hole where a number was, and closes the loop by confirming the change lands. That last element is most often omitted, and the correction agreed but never made is a familiar organisational failure. Option A asks for removal without a replacement. Option C corrects the record in the most public and least recoverable setting. Option D allows a board decision to proceed on a claim you know to be unsupported.

### Preparation tips

- **Ask who could not have appeared in this data.** Mode of operation is the version of that question specific to your discipline.
- **Ask what a conformance claim actually covers.** Isolation and defaults, usually — not composition and customisation.
- **Reconstruct implied unit values.** Thirty seconds establishes plausibility.
- **Return to counts before combining rates, and re-check the total.**
- **Ask for the definition and the distribution.** Most misleading metrics are correctly calculated and wrongly defined.
- **Know what samples can detect.** Fifty per group cannot see five points.
- **Write the conventions into the standard.** Denominators, both framings, disaggregation by mode, spread with every central figure.
- **Trace three figures in current board papers back to source.**

### Common pitfalls to avoid

- **Averaging rates without weighting.**
- **Treating a conformance claim and an audit as a straight contradiction.** They usually measure different scopes.
- **Converting qualitative samples into population rates.** The error most likely to reach a board paper.
- **Measuring drop-off against those who continued.** It overstates every step and distorts the organisational ranking.
- **Reporting an aggregate that could be disaggregated.** A figure describing no group conceals the group that is failing.
- **Accepting a mean without a spread or a definition.**
- **Endorsing an underpowered comparison "with caveats".** Caveats do not travel; the number and the precedent do.
- **Correcting a board paper at the board.** Go to the author, and confirm the change lands.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A verbal reasoning assessment measures how accurately you read. At your level the documents that matter are governance frameworks, organisational standards, audit reports, cross-government guidance, technical specifications, board papers and contracts. A misread exception clause becomes a compliance failure across several teams; a misread audit finding becomes advice given confidently to a director general.

The classic format presents a short passage of dense workplace prose, typically three to six sentences, followed by statements to classify as True, False or Cannot Say. True means the statement follows necessarily. False means the passage contradicts it. Cannot Say means the passage neither establishes nor excludes it. Alongside these come comprehension items, main-point items, and questions asking which of four summaries is most accurate.

The governing rule is that you answer from the passage alone, and the part specific to your level is this: expertise actively costs marks. The more accessibility criteria and component specifications you have read, the more readily you supply the clause you expect and feel entirely confident doing it. Candidates at your level underperform on verbal reasoning at rates that surprise them, and this is nearly always the mechanism. The counter-habit must be mechanical: before marking anything True, put your finger on the words.

Cannot Say is the answer experienced leaders avoid most. Forming a view under incomplete information is what your job consists of, and the reflex is deeply worn in. Here it is a liability.

Small words carry the load. "All" is not "most". "May" is not "must". "Should" is not "will". "Consider whether" is not "recommend". "Solely", "entirely", "unless", "provided that" and "where practicable" govern everything around them.

There is a direct professional payoff. Your role names communicating design strategy across organisational boundaries, and much of what blocks that is a shared misreading of what some standard requires — in both directions, since teams over-comply with rules that do not reach them as often as they under-comply with rules that do.

### How this assessment maps to your role

The verbal skills tested map onto your named skills:

- **Reading precisely** maps to setting direction and assuring the quality of design delivery across teams.
- **Separating statement from inference** maps to **Evidence-based design**, where you guide the organisation in using evidence.
- **Identifying the main point** maps to **Design communication**, where you gain support from senior leaders and communicate across boundaries.
- **Handling qualified language** maps to **Designing strategically**, where constraints in technology, systems and policy shape design.
- **Reading for absence** maps to **Designing for everyone**, where noticing that a framework never mentions a mode of operation has consequences at scale.
- **Reading cross-government prose accurately** maps to ensuring insight is used across the organisation and across government.

### Practice questions

*Passage A — for Questions 1 to 4*

"Organisations must submit an annual design assurance return to the cross-government profession board, unless all design work within the organisation has been delivered under a centrally managed programme. Returns must confirm that accessibility assurance was completed where required, and must list any services where it was not. Where an organisation identifies a service released without required accessibility assurance, it must notify the board within ten working days of identifying it, separately from the annual return. Returns are published across government; notifications are not."

**Question 1 (easy)** — Statement: "Every organisation must submit an annual design assurance return." True, False or Cannot Say?

**Correct answer: False**

**Explanation:** The passage attaches an exception: organisations where all design work was delivered under a centrally managed programme are exempt. The statement's "every" contradicts that, so False. This is the most reliable pattern in the section. Note that the exception says "all design work", not "most", which narrows it substantially and supplies the material for Question 3.

**Question 2 (easy)** — Statement: "Notifications of missed accessibility assurance are published across government." True, False or Cannot Say?

**Correct answer: False**

**Explanation:** The final sentence states that returns are published across government and notifications are not. The statement contradicts this, so False. The item tests whether you read past the point where a sentence appeared to finish — the semicolon clause carries the operative distinction, and a reader who registered "returns are published across government" would generalise it. Governance prose places qualifications after semicolons with striking regularity, and slowing down there rather than speeding up is a habit worth building deliberately when you are reading at volume.

**Question 3 (moderate)** — Statement: "An organisation where nineteen of twenty services were delivered under a centrally managed programme must submit a return." True, False or Cannot Say?

**Correct answer: True**

**Explanation:** The exemption applies only where *all* design work was delivered centrally. Nineteen of twenty does not satisfy that, so the exemption does not apply and the requirement stands — the statement follows and is True. The item rewards carrying "all" from the first sentence to a scenario several lines later. It also reflects a recurring organisational error: partial satisfaction of an exception condition is non-compliance, and organisations routinely assume the reverse on the reasoning that they are substantially covered. Catching that before a return is due, rather than after it is late, is squarely your job.

**Question 4 (moderate)** — Statement: "A service released without required accessibility assurance must be notified within ten working days of release." True, False or Cannot Say?

**Correct answer: False**

**Explanation:** The passage requires notification within ten working days of *identifying* the service, not of its release. Those triggers can be many months apart — a service released in February and identified in a September assurance review must be notified in September, and would not be retrospectively late. The statement misstates the trigger, so False. Small distinction, large consequence: trigger events determine whether an organisation is compliant, and misreading one produces either unnecessary alarm or false comfort, both expensive when reported to a cross-government board on your signature. Whenever a passage specifies a deadline, establish what starts the clock first.

*Passage B — for Questions 5 to 8*

"The cross-government review of component libraries found considerable variation between departments. Five departments maintain a shared internal library; the remainder rely on team-level components. Departments with a shared library reported fewer accessibility defects reaching live, although the review did not examine whether their components were more accessible when tested independently. The review recommends that the profession board consider whether a common approach to component governance would be proportionate."

**Question 5 (easy)** — Statement: "Some departments do not maintain a shared internal component library." True, False or Cannot Say?

**Correct answer: True**

**Explanation:** The passage states that five departments maintain one and the remainder rely on team-level components, establishing directly that some do not. True. Answer quickly and bank the time. The only conceivable ambiguity — whether "the remainder" might be empty — is closed by the passage describing what the remainder does.

**Question 6 (moderate)** — Statement: "Shared component libraries produce more accessible components." True, False or Cannot Say?

**Correct answer: Cannot Say**

**Explanation:** The passage reports fewer defects reaching live and then states explicitly that whether the components were more accessible when tested independently was not examined. Those are different things, and the gap between them is instructive: a shared library might produce better components, or might simply concentrate review so that defects are caught before release rather than after, or might be maintained by departments that also happen to have stronger assurance for unrelated reasons. The passage flags its own silence, so Cannot Say. A candidate answering True has substituted professional intuition for what the text supports — and at your level that is exactly the substitution that produces a cross-government recommendation resting on a finding the review declined to make.

**Question 7 (moderate)** — Statement: "The review recommends introducing common component governance." True, False or Cannot Say?

**Correct answer: False**

**Explanation:** The review recommends that the board *consider whether* a common approach would be proportionate, which includes concluding it would not be. The statement asserts a recommendation to introduce, which was not made, so False rather than Cannot Say: the passage tells you what was recommended and it was something different. This pervades review and audit prose and produces a familiar sequence in which a recommendation to consider becomes a commitment to deliver, is tracked, and is reported against for a year without anyone having decided it was right.

**Question 8 (harder)** — Statement: "Team-level components are a weaker approach than a shared library." True, False or Cannot Say?

**Correct answer: Cannot Say**

**Explanation:** The passage describes two approaches and reports one difference in outcome while explicitly declining to assess component quality. It makes no judgement about relative strength. A reader may reasonably infer that shared libraries are stronger, and the passage neither supports nor excludes that, so Cannot Say. What makes this harder than Question 6 is that the passage's structure leans towards shared libraries — mentioned first, associated with a favourable outcome — and structural lean is not content. Noticing when you are responding to a document's implied stance rather than its assertions is among the most transferable things this section trains, and it applies directly to audit reports, which routinely imply more than they will state so that readers draw the conclusion the authors lacked evidence to assert.

*Passage C — for Questions 9 to 12*

"Design decisions must not be altered to reflect the preferences of stakeholders where doing so would misrepresent the evidence. Presentation may be adapted to the audience provided the substance is unchanged. Where a designer is asked to alter a design rationale, the matter must be raised with the head of profession, who is accountable for the integrity of design outputs. Where design input cannot reach decision-makers before a decision is taken, the reason must be recorded; records are reviewed annually."

**Question 9 (easy)** — Statement: "Design rationale may be presented differently to different audiences." True, False or Cannot Say?

**Correct answer: True**

**Explanation:** The second sentence permits adapting presentation to the audience provided substance is unchanged, and the statement claims only that different presentation is permitted. It follows and is True. The statement is weaker than the passage's full provision, omitting the substance condition — but a weaker statement the passage supports is still True. Candidates occasionally mark such statements False for incompleteness, confusing "does not say everything" with "says something wrong".

**Question 10 (moderate)** — Statement: "A designer asked to alter a design rationale must refuse." True, False or Cannot Say?

**Correct answer: Cannot Say**

**Explanation:** The passage establishes that decisions must not be altered where doing so would misrepresent the evidence, and that a request must be raised with the head of profession. Neither states what the individual designer must personally do at the moment of the request. A duty to escalate is not a duty to refuse — arguably the escalation route exists so that an individual is not left to refuse alone, which is a substantive protection and, in a role adjacent to yours, the protection you are expected to provide. Note also that the first sentence's prohibition is itself conditional: alteration is prohibited *where doing so would misrepresent the evidence*, which is narrower than a blanket prohibition. Cannot Say.

**Question 11 (harder)** — Statement: "Altering a design rationale at a stakeholder's request always breaches the requirements." True, False or Cannot Say?

**Correct answer: False**

**Explanation:** The prohibition is conditional: alteration must not occur *where doing so would misrepresent the evidence*. An alteration that clarifies, reorders or reframes without misrepresenting anything is not caught, and the second sentence expressly permits adapting presentation provided substance is unchanged. The statement's "always" contradicts both, so False. This distinction is fine, consequential, and one you should expect to explain repeatedly. Read as absolute, the clause makes every stakeholder edit suspect and makes designers defensive about reasonable requests; read as written, it identifies precisely what is prohibited, which is misrepresentation. Standards read as absolutes lose their force, because people who know the absolute reading is unworkable begin ignoring the clause entirely.

**Question 12 (harder) — Main point**

Which best captures the main point of Passage C?

- A) Design rationales must never be changed.
- B) The substance of design reasoning must not be misrepresented to suit stakeholders, with adaptation permitted in form, escalation provided where independence is pressured, accountability located with the head of profession, and honesty required where timing fails.
- C) The head of profession is accountable for design integrity.
- D) Reasons must be recorded when design input arrives late.

**Correct answer: B**

**Explanation:** The main point must span the passage while adding nothing. Option A overstates: adaptation is expressly permitted and the prohibition is specifically on misrepresentation. Options C and D are each accurate about one clause and silent on the rest. Option B captures all four elements and the logic joining them — design input is useful only if it is both honest and timely, so the passage protects honesty with a conditional rule, an escalation route and an accountable owner, and handles timing with a requirement of disclosure rather than a prohibition. Main-point items reward the option broad enough to cover everything and disciplined enough to invent nothing.

### Preparation tips

- **Set expertise aside mechanically.** Before marking True, point at the words.
- **Treat Cannot Say as decisive.** The reflex to form a view is what costs marks here.
- **Circle every qualifier.** All, every, entirely, solely, may, must, should, unless, provided that, where practicable, consider whether.
- **Establish what starts the clock.** Deadlines hang on trigger events, and the trigger is often not the obvious one.
- **Notice conditional prohibitions.** "Must not, where X" is much narrower than "must not".
- **Separate "recommends considering X" from "recommends X".**
- **Notice structural lean.** Order of mention and favourable association are not assertions.
- **Practise on cross-government standards.** Write three statements about a page — one True, one False, one Cannot Say.

### Common pitfalls to avoid

- **Answering from professional knowledge.** The dominant error at your level.
- **Completing the clause you expected.** Governance prose has conventions; passages exploit them.
- **Missing "all", "entirely" and "solely".** Partial satisfaction of an exception is non-compliance.
- **Reading a conditional prohibition as absolute.** It makes the standard unworkable and then ignored.
- **Reading fewer defects reaching live as better components.** Passages distinguish outcome proxies from the thing itself.
- **Confusing a rule about outcomes with a rule about conduct.**
- **Responding to implied stance.** Audit reports imply far more than they will assert.
- **Rushing after a semicolon.** The operative qualification lives there disproportionately often.

## Workplace job-specific situational judgement assessment

### About this assessment

A situational judgement assessment presents realistic workplace scenarios and asks what you would do. There is no passage to parse and no arithmetic. You get a dilemma of the kind your role produces, four or five candidate responses, and a question asking which is most effective and often which is least.

This section measures whether your judgement matches what the profession considers good practice at your level. Your role places you as an expert practitioner who sets direction and assures design quality across teams, leads multiple or highly complex services, gains support for design strategy from senior leaders, coaches others, measurably improves inclusive practice across teams, and creates an inclusive, productive environment for designers. The strongest answers involve organisational rather than local action, capability building rather than problem solving, and holding positions in forums where the pressure is real.

Three features distinguish your level.

The first is that you are usually acting on systems rather than instances. A senior designer who fixes a flawed component has done their job. A lead who fixes it without asking why the assurance process did not catch it has done half of theirs.

The second is that your authority is largely informal. Options leading with instruction, mandate or escalation tend to score poorly — not because escalation is wrong, but because it is capital you spend rather than a tool you use freely.

The third is that you absorb pressure downwards. When a director leans on a designer, the designer should not be holding that line.

Four principles carry most scenarios. Users come first, including in work you did not commission. Protect the integrity of design reasoning, and the people whose job it is to protect it. Build capability and conditions while solving the problem. Calibrate escalation to severity.

### How this assessment maps to your role

The judgement dimensions map onto your named skills:

- **Assuring across boundaries** maps to setting direction and assuring design delivery quality across teams.
- **Coaching and capability** map to **Leading design**, where you mentor and coach other designers and create an inclusive, productive environment.
- **Influence with senior leaders** maps to **Design communication**, where you gain support for design decisions and strategy from senior leaders.
- **Organisational inclusion** maps to **Designing for everyone**, where you measurably improve inclusive practice across multiple teams.
- **Embedding practice** maps to **Iterative design**, where you embed iterative design and agile working and iterate delivery processes or team structures.
- **Working across boundaries** maps to **Designing together**, where you help teams connect and work across organisational boundaries.

### Practice questions

**Question 1 (easy) — A designer under pressure from a director**

A senior designer tells you a director has asked them to remove an accessibility finding from a board summary because it "muddies the message". What is the most effective response?

- A) Tell them to leave it in and cite your instruction.
- B) Agree with them how the finding should be presented, including mitigation; offer to attend; and take the request itself up with the director yourself, since a director asking for findings to be removed is a matter at your level.
- C) Contact the director and instruct them not to make such requests.
- D) Escalate to the director general.

**Correct answer: B. Least effective: A**

**Explanation:** Two things must happen: the finding survives, and the designer emerges more capable and less exposed. Option B does both. Agreeing the presentation builds their judgement rather than substituting yours; a constructive framing with mitigation gives them something to bring rather than a refusal; offering to attend supplies backing without takeover. Most importantly, taking the request up with the director is your job — a power differential of that size is what your role exists to absorb, and leaving a senior designer to manage it alone is a leadership failure even if the finding survives. Option A is least effective: it leaves them defending by proxy, teaches nothing, and reframes integrity as hierarchy. Option C treats a conversation as an instruction you are not positioned to give. Option D escalates far past the point and spends capital you will need.

**Question 2 (easy) — A standard nobody follows**

Your organisation has a component standard that is widely ignored. Designers describe it as unrealistic. What is the strongest approach?

- A) Reissue it with a message from you.
- B) Review recent components with designers to establish which requirements are genuinely unworkable and which are merely unclear, revise it with them, and pair it with a lightweight routine — such as a keyboard and screen reader pass before merge — that gives compliance a moment of application and produces something designers and developers want anyway.
- C) Introduce mandatory compliance checks.
- D) Run training on the standard.

**Correct answer: B. Least effective: A**

**Explanation:** A standard everybody ignores has already failed, and reissuing changes only the date. Option B treats the objection as data — some requirements probably are unworkable and the rest are usually unclear. Revising with designers produces authorship and therefore defenders, which is the only mechanism by which a standard becomes self-sustaining rather than dependent on your attention. Pairing it with a routine matters because a standard without a moment of application is an aspiration, and the specific routine named here is the right one for this discipline: a check performed before merge catches defects when they are cheap and turns compliance into a habit rather than an audit. Option A is least effective. Option C enforces a standard people have told you is unrealistic. Option D is useful and insufficient alone.

**Question 3 (easy) — Conditions for designers**

Designers across your teams report being pulled into delivery firefighting, having no time for critique, and rarely seeing each other. Three have left in eight months. What is the strongest response?

- A) Discuss workload with each designer's delivery manager.
- B) Treat it as structural: establish a protected routine bringing designers together regularly, negotiate with delivery leadership for the time by showing what the current pattern costs in rework and attrition, and change how designers are deployed if single embedding is the cause.
- C) Introduce a wellbeing initiative.
- D) Recruit replacements quickly.

**Correct answer: B. Least effective: D**

**Explanation:** Three departures in eight months alongside no critique and no professional contact is a structural pattern, not a series of individual circumstances, and your role explicitly names creating an inclusive, productive environment for designers. Option B addresses the structure on three fronts: a protected routine, the negotiation that makes it survive contact with delivery pressure, and a change to deployment if the cause is designers embedded singly with nobody to think alongside — which for interaction designers is particularly damaging, because component and pattern decisions made in isolation diverge and nobody notices for a year. The negotiation detail matters: protected time not paid for in delivery's currency gets cancelled by the third sprint. Option D is least effective, reproducing the attrition on a lag. Option A addresses symptoms individually. Option C treats a design-of-work problem as a morale problem.

**Question 4 (moderate) — Assuring across a boundary**

A directorate you do not manage has shipped a custom component whose focus behaviour traps keyboard users. It is now in three services. What is most effective?

- A) Advise the three services to stop using it.
- B) Speak to the designer and their lead first with a precise reproduction, agree how the fix will be made and communicated to the three services already using it, and set a clear next step if they decline.
- C) Raise it at the departmental board.
- D) Note it for the annual assurance return.

**Correct answer: B. Least effective: D**

**Explanation:** The defect needs fixing and the relationship needs to survive, since you will be assuring this directorate for years. Option B goes to the people responsible first — they may hold context you lack, and the fix lands better from them — with a reproduction, because a vague report gets triaged low while a precise one gets fixed. The clause about communicating to the three services is most often omitted, without which a fixed component sits alongside three services still running the broken version. Option A bypasses the person who can fix it and leaves the defect in the component itself. Option C is disproportionate as a first move. Option D is least effective by a distance: an annual return is a record, not an intervention, and keyboard users cannot use three services today.

**Question 5 (moderate) — Non-compliance concentrated in one place**

Accessibility assurance was missed on four services, all in one directorate, all under ministerial deadline pressure, all by experienced designers. What is the strongest response?

- A) Report the four and require remediation.
- B) Remediate the four, and separately investigate the assurance process — what it demands, how long it takes, whether a fast route exists — on the reasoning that experienced designers who know the requirement and miss it under pressure are telling you the process cannot be complied with when time is short.
- C) Remind all designers of the requirement.
- D) Introduce a mandatory pre-release gate for every service.

**Correct answer: B. Least effective: C**

**Explanation:** The concentration is the most informative feature. Scattered breaches would indicate conduct; four concentrated under identical pressure by experienced people indicate a process that does not survive a deadline. Option B handles both layers, and the remediation clause matters because a systemic diagnosis is not a reason to leave individual failures unfixed. Option A treats the instances and guarantees recurrence. Option C is least effective and is the weakest available response to any compliance failure. Option D imposes friction on every compliant service to catch a localised failure, which is how burden accumulates — and you will be defending that gate in two years when someone asks why design governance is slow.

**Question 6 (moderate) — Competing directorates**

Two directors want your design capacity in the same quarter. One has a failing live service; the other a ministerially visible new programme. Both have raised it with your director. What is most effective?

- A) Split capacity.
- B) Set out for each what design work would deliver, what decision it informs, and the cost of deferral; recommend a sequence with reasoning; and put that recommendation to both directors and your director together rather than negotiating separately.
- C) Prioritise the ministerial programme.
- D) Ask your director to decide.

**Correct answer: B. Least effective: A**

**Explanation:** A prioritisation problem is being conducted as a political one, and the way through is to make the trade-off explicit and simultaneously visible. Option B does the analytical work and handles the politics correctly: putting the recommendation to both at once prevents the parallel-negotiation dynamic in which each director hears something slightly different and trust collapses when they compare notes, which they will. Making a recommendation rather than presenting neutral options is essential; you are the expert on what design can deliver. Option A is least effective: splitting constrained capacity between two substantial needs reliably produces two efforts too thin to inform either decision. Option C ranks by visibility. Option D discards your judgement.

**Question 7 (moderate) — A technology decision already made**

A technology team has adopted a component library whose date picker, modal and custom select fail your standard. Four services already use it. What is strongest?

- A) Require them to stop using the library.
- B) Establish precisely which components fail and how, propose a shortlist to avoid or wrap with compliant alternatives, and a route to remediate the four existing services — framing it as making their choice workable rather than reversing it.
- C) Escalate to the head of profession.
- D) Accept it and document the risk.

**Correct answer: B. Least effective: D**

**Explanation:** A library is almost never uniformly good or bad — the complex interactive components fail while the buttons and inputs are fine. Option B establishes which, converting an unwinnable argument about a decision already made into a tractable list. That reframe matters practically and politically: four services cannot start again, so an answer requiring them to is an answer they will refuse, and you will have spent your standing for nothing. Option D is least effective because documenting a risk with nothing following it is how an exclusion becomes permanent while everyone feels they have handled it — and at your level you are the person whose name is on the risk register entry. Option A asks for reversal without a route. Option C escalates a solvable disagreement across a boundary you need repeatedly.

**Question 8 (harder) — Inclusion practice that is not improving**

Your role requires measurably improving inclusive design practice across teams. After a year of guidance, templates and talks, components still routinely ship with keyboard defects. What is the strongest response?

- A) Produce clearer guidance and repeat the training.
- B) Stop adding guidance and find out what is actually preventing it — most likely that nobody checks before merge, or that checking is manual and slow, or that defects are found only in an audit months later when fixing is expensive — then fix that specific blocker, most plausibly by putting a keyboard and screen reader pass into the routine where code is reviewed.
- C) Introduce a mandatory accessibility checklist.
- D) Report the failure to the head of profession.

**Correct answer: B. Least effective: A**

**Explanation:** A year of guidance that has not changed practice is evidence that the barrier is not knowledge, and continuing to supply knowledge is the characteristic failure of well-intentioned improvement programmes. Option B does the diagnostic work first and names the realistic blockers, all of which are about *when and how* checking happens rather than whether people know it should. The remedy it points at is specific and cheap: a check at code review catches defects when they cost minutes rather than months, and it converts an aspiration into a step in a workflow people already follow. Option A is least effective, repeating an intervention that demonstrably did not work and consuming the credibility of the next one. Option C adds a checklist to a system already full of guidance. Option D reports a failure you are accountable for solving.

**Question 9 (harder) — An unowned problem**

Synthesising across services, you conclude the organisation's largest interaction problem is inconsistency between services at the same moments — different controls, different error behaviour, different navigation — for users who move between them. No director owns cross-service consistency. What is most effective?

- A) Report it in your annual synthesis.
- B) Build the case with evidence from the affected services, quantify the affected population using contact centre and analytics data, identify who would need to own it, and take it to a forum with cross-service authority — accepting that securing an owner for an unowned problem is itself months of work.
- C) Raise it with each service owner separately.
- D) Propose research on cross-service journeys.

**Correct answer: B. Least effective: A**

**Explanation:** Unowned problems are the characteristic failure of service-shaped organisations, and surfacing them is what cross-service synthesis is for. Option B recognises that the hard part is ownership rather than insight: evidence from several services makes the problem undeniable, quantification makes it comparable to problems that do have owners and budgets, and a forum with cross-service authority is the only route by which anything unowned becomes owned. The closing clause is realistic — this is a campaign, not a communication, and treating it as a communication is why so many of these insights die. Option A is least effective: correct and filed, it will change nothing. Option C produces conversations in which each owner reasonably concludes it is mostly someone else's problem. Option D proposes more evidence when the evidence is sufficient.

**Question 10 (harder) — Cross-government collaboration**

Three departments are independently building the same component — a complex address-entry control — each solving it differently, and none is confident about its assistive technology behaviour. You have no authority over the other two. What is strongest?

- A) Focus on your own department's version.
- B) Convene the three departments' design leads, establish whether the requirement is genuinely common, and if so propose one properly tested shared component or a joint contribution to the Design System — accepting that you are building consensus rather than exercising authority, and noting that a single well-tested component is more achievable than three adequately tested ones.
- C) Ask the cross-government profession board to mandate a common component.
- D) Share your version with the other two for information.

**Correct answer: B. Least effective: A**

**Explanation:** Three departments building one complex component three ways, none confident about assistive technology, is precisely the waste that cross-government collaboration exists to prevent — and the accessibility argument is the strongest one available, because properly testing a complex control is expensive and doing it once is the only realistic route to doing it well. Option B is calibrated to the authority you have: convening is available, mandating is not, and establishing whether the requirement is genuinely common avoids the failure in which a shared component is agreed and then fits nobody. Option A is least effective, accepting solvable waste and leaving three inadequately tested components in public services. Option C reaches for a mandate before building the case; boards asked without evidence decline, spending the ask. Option D creates nothing.

**Question 11 (harder) — Assurance failure you signed off**

Nine months ago you approved a pattern now used in six services. You realise its error handling assumes errors appear on the same page as the field, which breaks in the two services using it across multiple pages. What should you do?

- A) Note it for the next pattern review.
- B) Notify all six services now, scope precisely which two are affected and which four are not, propose a fix to the pattern and an interim workaround for the two, and examine why the approval did not test the pattern against a multi-page case — then change the approval process.
- C) Amend the pattern documentation quietly.
- D) Advise the two services to stop using the pattern.

**Correct answer: B. Least effective: C**

**Explanation:** A pattern in six services means a flaw is potentially six defects, and the scoping matters as much as the disclosure — four services are fine, and telling them otherwise creates unnecessary work and erodes confidence in the pattern generally. Option B does all four necessary things: notifies, scopes precisely, fixes both immediately and durably, and — the element specific to your level — asks why the approval did not test against a multi-page case, which is the question that prevents the next one. Option C is least effective: amending documentation without telling the two affected services leaves live defects while creating a record suggesting they were addressed, which is worse than silence because it will be cited as evidence the issue was handled. Option A defers a live problem. Option D is disproportionate when a workaround exists.

**Question 12 (harder) — A standard that will be resisted**

You intend to require that every component entry document its keyboard and assistive technology behaviour and its known limitations. You anticipate resistance: teams will say they cannot fully test assistive technology behaviour. What is strongest?

- A) Introduce the requirement and handle objections as they arise.
- B) Engage the objection before introducing it, because it is partly correct: comprehensive assistive technology testing is genuinely beyond most teams. Frame the requirement as documenting what was tested, with what, and what was not — so a truthful "tested with one screen reader on one browser; not tested with voice control" satisfies it — and pair it with access to a shared testing capability for the cases teams cannot cover.
- C) Introduce it as guidance rather than a requirement.
- D) Require it only for components used by more than one service.

**Correct answer: B. Least effective: A**

**Explanation:** The anticipated objection is not obstruction; it is true, and a standard that ignores it will be resisted and technically unreasonable at once. Option B resolves the tension by changing what is required: documenting what was and was not tested is entirely feasible for any team, and it is arguably more useful than a claim of full conformance, because it tells the next team exactly where the risk sits. The paired testing capability is the other half, because requiring coverage without enabling it produces either non-compliance or a tick-box claim, and you will get whichever is easier to fake. Option A is least effective: introducing a requirement you know to be contestable and arguing it case by case spends enormous credibility for a worse outcome. Option C removes the force. Option D exempts single-service components, which are exactly where undocumented limitations are most likely and most invisible.

### Preparation tips

- **Ask what an option does to the system.** An intervention depending on your personal attention has not solved anything.
- **Absorb pressure downwards.** If a power differential is above the level of the person facing it, it is yours.
- **Read the distribution of a problem.** Concentrated failures diagnose a process; scattered diagnose conduct.
- **Stop adding knowledge when knowledge is not the barrier.** Ask when and how checking actually happens.
- **Put checks where work already flows.** A pass at code review beats an audit months later.
- **Engage the strongest objection before you launch.** A standard that has answered its critics survives without you.
- **Convene where you cannot mandate.**
- **Require honest documentation rather than unattainable coverage.** "What was tested and what was not" is feasible and more useful.

### Common pitfalls to avoid

- **Reissuing a standard nobody follows.**
- **Repeating an intervention that demonstrably did not work.**
- **Adding friction for the compliant majority.** You will have to defend the gate.
- **Solving personally rather than changing the mechanism.**
- **Leaving a colleague to hold a line you should be holding.**
- **Filing a strategic insight rather than finding it an owner.**
- **Documenting a risk and calling it management.** Nothing follows unless someone makes it.
- **Amending documentation instead of telling affected users.** It creates a record suggesting a fix that has not happened.

## Conclusion

You have reached the end, and it is worth registering the scale: forty-eight questions across four assessment types, with the reasoning worked through on each. That is a substantial piece of professional preparation and more than most people at your level undertake.

Look back at the ground. In the cognitive section you audited a component entry as written rather than as you would have written it, named what three favourable test conditions had removed, weighted a pattern decision by the seven services that would reuse it, diagnosed six teams' custom-component habit as one systemic cause with six rationalisations, resolved an apparent contradiction between two date-control studies by asking what task each participant was doing, and read a concentration of accessibility failures as a process diagnosis. In the numeric section you weighted rather than averaged, distinguished a conformance claim's scope from an audit's, converted a percentage into people, recognised a session metric masquerading as a journey measure, and declined to endorse a comparison that could not detect what it was built to find. In the verbal section you carried "all" across five lines, checked what started a deadline clock, noticed a conditional prohibition read as absolute, separated fewer defects reaching live from better components, and caught yourself responding to structural lean. And in the situational judgement section you absorbed a director's pressure, put an accessibility check where code review already happens, convened three departments you could not compel, campaigned for an owner for cross-service consistency, and designed a documentation standard around its strongest and truest objection.

Two threads run through it. The first is whether you know the limits of the evidence and will say so. The second is whether you act on mechanisms rather than instances. Between them those are most of what your role consists of. Teams can generate opinions without you and read dashboards without you. What you supply is design reasoning that holds when someone pulls at it, and a practice around you that keeps producing it when you are not looking.

A word about the particular difficulty of your level. The errors that cost you most are no longer the ones you would notice. They are made fluently, in areas where your experience runs deep enough that checking feels unnecessary, and nobody in your organisation is positioned to catch them. The verbal reasoning section is the clearest demonstration, and the pattern generalises to every judgement you make alone.

If you want to build on this, a few things repay effort more than rereading. Audit a pattern you approved and ask which service contexts it was never tested against. Complete a service you are responsible for using only a keyboard, then a screen reader, then at 400% zoom. Trace three figures in current board papers back to source. Go and find out what your strongest teams actually do differently rather than assuming. And the next time you are about to reissue something, ask instead why the first issue did not take.

Finally, for the day itself. An assessment samples your reasoning on one morning under artificial conditions. It is not a verdict on your judgement or your career. Read the stem twice, set expertise aside in the verbal section, find the denominator, trust Cannot Say, and remember that at your level the strongest answer is almost always the one honest about uncertainty and aimed at the mechanism rather than the symptom.

Good luck. The profession is stronger for leaders who prepare like this, and so are the people who depend on these services.
