# Senior Accessibility Specialist - Psychometric Assessment Resources

## Introduction

Welcome. This guide is written for you as a senior accessibility specialist in the UK Government Digital and Data profession — someone who works with people at a range of levels to embed accessibility into the output of teams. Your role description says you coach and mentor more junior colleagues, input into accessibility strategy with business areas, create and deliver training, engage with teams across different levels and capabilities, potentially manage or lead individuals or sub-teams, and contribute to the cross-government accessibility community.

You may be preparing for a formal assessment as part of a recruitment or promotion process, or you may want to sharpen reasoning that your job depends on. Either way, it is worth being precise about what psychometric assessment is at this level. It is not an intelligence test and it is not a knowledge quiz — nobody will ask you to recite a success criterion. It is a standardised sample of the thinking a role demands, and for a senior specialist that thinking has a particular character: you are rarely choosing between compliant and non-compliant, and usually choosing between defensible positions where the standard is ambiguous, the constraint is real, and somebody has to decide what is proportionate.

Three features of your role shape everything that follows. First, most of what you do is advisory rather than executive: you audit work you did not build, recommend to people who may not take the recommendation, and depend entirely on your findings being unassailable. Second, you occupy an unusual position between a legal framework and a design conversation. Accessibility is one of the few areas of digital practice with statutory force behind it, which gives your findings weight and creates a specific risk — a specialist who overstates a requirement, or applies a criterion where it does not bite, spends credibility that the genuine requirements need. Third, your role names bringing the voice of disabled users, which means you carry a representative function alongside a technical one, and the two occasionally pull in different directions.

The document has four main sections: a cognitive assessment, a numeric reasoning assessment, a verbal reasoning assessment, and a situational judgement assessment. Each provides an overview, a mapping to your named skills, twelve practice questions with full explanations, preparation tips, and common pitfalls.

Commit to an answer before reading each explanation. The explanations spend most of their words on why the near-miss options fail.

Let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive assessment measures the reasoning your role genuinely uses, presented through practical materials rather than abstract puzzles. At your level the materials are audit findings, standards with edge cases, remediation plans, and claims made by teams and suppliers that need diagnosing rather than accepting or rejecting.

The format is typically an online test of fifteen to thirty minutes covering pattern recognition, logical deduction, error checking, prioritisation and applied problem solving. Scoring is objective against a norm group at a comparable level. Adaptive platforms raise difficulty after correct answers, and acuity reports distinguish speed from accuracy.

Three things distinguish this section at your level.

The first is that accessibility reasoning is unusually rule-shaped, which makes precision both easier and more consequential. Most criteria have defined thresholds, defined scopes and defined exceptions, so a question generally has a right answer — and getting it wrong in the direction of over-application is as damaging as under-application, because a team told to fix something that is not a failure learns to discount your next finding.

The second is that severity and compliance come apart. A technically conforming interface can be nearly unusable, and a technical failure can be trivial in practice. Your role names understanding the boundary between usability and accessibility, and several items turn on holding both judgements at once rather than collapsing into either.

The third is proportionality. You advise teams with finite capacity, and a list of forty findings with no ordering is a list nobody acts on. Deciding what must be fixed before release, what should be fixed next, and what can wait is a reasoning task, not an administrative one.

### How this assessment maps to your role

The cognitive dimensions map onto the skills named in your role summary:

- **Error checking and audit reasoning** map to **Technical understanding (accessibility)**, where you perform detailed audits, document findings clearly and provide solutions for others to work from.
- **Logical deduction** maps to **Technical understanding**, where excellent knowledge of standards and legislation *including edge cases* is named, and edge cases are precisely where deduction matters.
- **Severity and proportionality reasoning** map to **Governance and assurance (accessibility)**, where you reduce or remove risk associated with not meeting standards — which requires knowing which risks are which.
- **Prioritisation** maps to **Leadership and guidance**, where you make decisions characterised by medium risk and complexity.
- **Diagnosing systemic causes** maps to **Consultancy**, where you lead the definition of guidance and inform how the organisation approaches delivery.
- **Reasoning about positions** maps to **Communicating information**, where you manage stakeholder expectations and host difficult discussions.

### Practice questions

**Question 1 (easy) — Auditing against a criterion**

A criterion states: "Text smaller than 24 pixels must have a contrast ratio of at least 4.5:1. Text 24 pixels or larger, or 19 pixels or larger and bold, must have at least 3:1. Logotypes are exempt." You audit four items: 14px at 4.4:1; 19px bold at 3.2:1; 24px at 2.8:1; a logotype at 2.1:1. How many fail?

- A) 1
- B) 2
- C) 3
- D) 4

**Correct answer: B**

**Explanation:** Work through each. 14px needs 4.5:1 — 4.4 fails. 19px bold satisfies the second route, so needs 3:1 — 3.2 passes. 24px falls into the larger category, so needs 3:1 — 2.8 fails. The logotype is exempt. Two fail, giving B. Three readings decide this, and each is one specialists get wrong in practice: 4.4 fails despite rounding to 4; "19 or larger and bold" is an alternative route rather than an additional condition, so a bold 19px item at 3.2 passes; and the exemption is absolute rather than conditional on the ratio. Reporting the bold text or the logotype as failures would be an over-application, and at your level that costs more than the finding is worth — a team that fixes two things unnecessarily learns to check your findings rather than act on them.

**Question 2 (easy) — Deduction from a scope rule**

A regulation states: "Public sector websites must meet the standard, unless the content is a pre-recorded audio or video published before 23 September 2020, or the content is on an intranet not substantially revised after 23 September 2019." A team says: "This video is exempt; it was published in 2019." Which must be true?

- A) The video is exempt.
- B) The video is not exempt.
- C) The video is exempt if it is pre-recorded, and not otherwise on the basis given.
- D) The regulation does not cover video.

**Correct answer: C**

**Explanation:** The exemption for time-based media applies to *pre-recorded* audio or video published before the date. A live-streamed video published in 2019 would not qualify, since the exemption names pre-recorded content specifically. The team has given a date but not established that the content is pre-recorded, so the exemption depends on a fact not yet in evidence — making C the only statement guaranteed. Options A and B each assume a branch. Option D is wrong on the face of the regulation. This matters practically because exemption claims are almost always made on one criterion — usually the date — while the exemption has two, and a specialist who accepts or rejects on the date alone is doing the team's reasoning for them badly in either direction.

**Question 3 (moderate) — Severity against compliance**

You audit a service and find two issues: an image of a decorative flourish missing an empty alt attribute, and a form where the only error indication is a red border with no text. Both are failures. How should you present them?

- A) As two failures of equal standing, since both breach the standard.
- B) As two failures with clearly different severity: the missing empty alt causes a screen reader to announce a filename, which is a minor irritation, while error indication by colour alone means a user cannot tell what went wrong or where — one is a defect and the other is a blocker.
- C) Report only the error indication.
- D) Report the missing alt as a warning rather than a failure.

**Correct answer: B**

**Explanation:** Both are genuine failures and treating them as equivalent is the mistake that makes audit reports unusable. A decorative image without an empty alt attribute produces one unnecessary announcement; error indication by colour alone can leave somebody unable to complete a form at all, and unable even to establish why. Option B reports both and ranks them, which is what your role means by documenting findings clearly and providing solutions for others to work from — a team with limited capacity needs to know which finding to fix on Monday. Option A is technically accurate and practically useless, and it is how forty-item reports get filed. Option C suppresses a real failure. Option D downgrades a failure to a warning, which misrepresents the standard and will be noticed by whoever checks.

**Question 4 (moderate) — Prioritising a remediation plan**

An audit found: (i) a keyboard trap in a modal; (ii) fourteen images missing alt text; (iii) a heading structure that skips from h1 to h3; (iv) insufficient contrast on a decorative divider. The team can fix two before release. Which two, and why?

- A) (ii) and (iii), because there are more instances.
- B) (i) and (ii), because the keyboard trap prevents anyone using a keyboard from leaving the modal at all, and missing alt text on fourteen images removes information many users need — while the heading skip is a navigation inconvenience and the divider is decorative, so the requirement may not even apply.
- C) (i) and (iv).
- D) All four must be fixed before release.

**Correct answer: B**

**Explanation:** Prioritisation at this level ranks by consequence, not by count or by tidiness. A keyboard trap is absolute — a user cannot proceed or escape, and no workaround exists — so it goes first regardless of how many instances there are. Missing alt text on fourteen images removes content, which is serious though its severity depends on whether the images are informative. A heading skip is a real failure and a navigation inconvenience rather than a barrier. A decorative divider almost certainly falls outside the non-text contrast requirement, which applies to elements conveying information — so option B is also correcting a probable over-application in the audit itself. Option A ranks by instance count, which is the commonest error. Option D is technically ideal and unhelpful to a team that has told you what its capacity is.

**Question 5 (moderate) — A conforming interface that fails users**

A service passes every automated and manual check. Testing with screen reader users shows they complete tasks far more slowly and abandon more often. What is the strongest analysis?

- A) The testing must be flawed; the service conforms.
- B) Conformance and usability are different things: a service can meet every criterion and still be exhausting to use — for instance if the heading structure is technically correct but uninformative, if error messages are announced but not associated in a way that returns focus usefully, or if the reading order is valid but illogical — so the finding is real and points at issues the criteria do not capture.
- C) The criteria should be changed.
- D) The additional difficulty is acceptable since the service conforms.

**Correct answer: B**

**Explanation:** This is the boundary your role names explicitly, and it is where accessibility specialists earn most of their value. Conformance is a floor, not a description of a good experience, and a service can satisfy every success criterion while being far harder for a screen reader user than for anyone else — technically valid headings that describe nothing, focus that moves somewhere legal but unhelpful, a reading order that follows the markup rather than the meaning. Option B says this and names concrete mechanisms, which is what makes it actionable rather than a general observation. Option A dismisses the strongest evidence available, which is disabled users' actual experience, in favour of a checklist. Option D treats conformance as the goal, and your role's purpose is people using services rather than services passing audits.

**Question 6 (moderate) — A supplier's claim**

A supplier states their component library is "fully WCAG 2.2 AA conformant". Your audit of two services using it found defects in four components. What is the most important observation before treating these as contradictory?

- A) The supplier is wrong.
- B) Conformance claims are typically established for components in isolation under default configuration, while defects arise when components are composed, customised and given real content and focus management — so both statements can be accurate about different things, and the question is what was tested.
- C) The audit should be repeated.
- D) The library should not be used.

**Correct answer: B**

**Explanation:** Supplier claims and internal audits routinely disagree without either being wrong, and the reason is scope. A supplier tests a component in a demonstration harness with default settings and placeholder content; your teams compose several on a page, override styles, add validation and manage focus between them, and defects appear at the joins — a modal that traps focus only when it contains a date picker, an error summary that works until a second one is added. Option B names this and converts an apparent contradiction into an answerable question. Option A picks a fight you may lose and will certainly not need. Option C doubts your own finding first, which is the wrong order. Option D is disproportionate before establishing which components fail and whether they can be avoided or wrapped.

**Question 7 (moderate) — Advising under a constraint**

A team says a fully accessible version of a complex data visualisation cannot be delivered before a statutory deadline. What is the strongest advice?

- A) The visualisation must be accessible or must not launch.
- B) Establish what information the visualisation conveys, and advise that the same information be made available in an accessible form — a table, a summary of the key findings, a downloadable dataset — since the requirement is that the information is accessible rather than that every presentation of it is, and this route is usually deliverable within the timeline.
- C) Advise them to publish an accessibility statement noting the gap.
- D) Advise a delay.

**Correct answer: B**

**Explanation:** The strongest advice separates the information from its presentation, which is the move that resolves most visualisation problems. A complex chart that cannot be made directly navigable by assistive technology in three weeks can almost always be accompanied by a table of the underlying data and a plain-language summary of what it shows, and that satisfies the substance of the requirement — users get the information — while being deliverable. Option B also does something your role requires: it provides a solution rather than a verdict. Option A is a verdict, and a specialist who only issues verdicts stops being consulted early, which is when they are useful. Option C treats a statement as a way to launch with a known gap, which it is not — a statement discloses work in progress. Option D may be right if no alternative exists and is premature before exploring one.

**Question 8 (harder) — Scoping a finding**

An audit reports: "The service fails WCAG 1.3.1 Info and Relationships." What is wrong with this finding, and what should it say?

- A) Nothing; it identifies the criterion.
- B) It names a criterion without identifying what, where or why — a developer cannot act on it. A usable finding states the specific element and page, what is wrong in technical terms, what a user experiences as a result, and what the fix is: for example, that the address fields on the contact page are visually grouped but not associated in markup, so a screen reader user hears seven unrelated inputs, and a fieldset with a legend would fix it.
- C) It should cite the level and version.
- D) It should be rated for severity.

**Correct answer: B**

**Explanation:** Your role names documenting findings clearly and providing solutions for others to work from, and a criterion reference alone does none of that. The four elements in option B are what make a finding actionable: location, technical fault, user impact, and remedy. The user impact element is the one most often omitted and the most valuable — a developer who knows that a screen reader user hears seven unrelated inputs understands the problem in a way that "fails 1.3.1" does not, and is far more likely to fix it properly rather than doing the minimum that clears the criterion. Option D is a real improvement and secondary; a severity rating on an unactionable finding is still unactionable. Option C adds bibliographic precision to a finding nobody can use.

**Question 9 (harder) — Diagnosing a systemic cause**

Across six services you audit, the same three defects recur: missing form labels, non-descriptive link text, and unlabelled icon buttons. What is the strongest diagnosis?

- A) Six teams need training on those three issues.
- B) Three defects recurring across six teams suggests a shared cause — most likely a component library that permits or produces them, or a development framework whose defaults omit accessible names, or the absence of any check between writing code and merging it — and identifying which determines whether the remedy is a component fix, a linting rule, or a change to the workflow.
- C) Accessibility awareness is low across the organisation.
- D) Audits should be more frequent.

**Correct answer: B**

**Explanation:** Three specific defects recurring across six independent teams is not six coincidences, and the three named here have a common character worth noticing: all are missing accessible names, which is exactly what a linting rule or a component with a required label prop can prevent mechanically. Option B names the realistic causes and points out that they imply different remedies. Option A is the default response and the weakest: training six teams on issues that a linting rule would catch automatically spends everyone's time and relies on human memory for something a machine does reliably. Option C is a diagnosis so general it suggests no action. Option D increases detection without reducing occurrence, which raises your own workload permanently.

**Question 10 (harder) — A disagreement about severity**

A developer argues that a colour-only status indicator is a minor issue because the status is also in the page title. You believe it is significant. What is the strongest way to resolve this?

- A) Cite the criterion and require the fix.
- B) Establish whether the page title genuinely conveys the same information at the moment the user needs it — a title change may not be announced, may not be noticed by a sighted user with colour vision deficiency who is looking at the indicator, and may not distinguish between multiple items on one page — because if it does convey it, the developer may be right, and if it does not, the specific reason is the argument.
- C) Escalate to the developer's lead.
- D) Concede; there is redundancy.

**Correct answer: B**

**Explanation:** The developer has made a legitimate argument and it may be wrong for specific reasons rather than in principle. Redundant encoding genuinely can satisfy the requirement — that is the whole point of not relying on colour *alone* — so the question is whether this particular redundancy works. Three things would defeat it: a title change that is not announced to a screen reader user, a sighted user with colour vision deficiency who is looking at the indicator and not the title, and a page containing several items where one title cannot distinguish them. Option B establishes which apply, which either resolves the disagreement or produces a precise argument. Option A asserts the criterion without engaging, and since the developer's point is about whether the criterion is met, that is not a response. Option D concedes without checking. Option C escalates a technical question that has a technical answer.

**Question 11 (harder) — Proportionality and risk**

A service has forty-one audit findings: two blockers, eleven serious, twenty-eight minor. The team has capacity for the blockers and about half the serious issues before a legally significant deadline. What is the strongest advice?

- A) All findings must be fixed by the deadline.
- B) Advise fixing both blockers and prioritising the serious issues by the number of users affected and whether a workaround exists, publish an accessibility statement disclosing what remains with a dated plan, and set the remaining work against subsequent releases — since a disclosed, planned gap is a materially different position from an undisclosed one.
- C) Advise delaying the deadline.
- D) Advise fixing the twenty-eight minor issues, since they are quick.

**Correct answer: B**

**Explanation:** Your role names reducing or removing risk associated with not meeting standards, and that is a proportionality judgement rather than an all-or-nothing one. Option B does four things: clears the blockers, gives a rational basis for choosing among the serious issues, uses the accessibility statement for its actual purpose — disclosing known gaps with a plan — and schedules the rest. The point about disclosure matters legally and practically: an organisation with a documented, dated remediation plan is in a defensible position, while one with the same defects and no statement is not. Option A is technically ideal and ignores the constraint you were told about. Option D is the trap that feels productive, clearing twenty-eight items while leaving serious barriers in place. Option C may be right occasionally and is rarely available.

**Question 12 (harder) — Representing users**

Your organisation is deciding between two designs. Automated and manual testing shows both conform. Testing with disabled users shows a clear preference for one. A stakeholder says conformance is what matters. What is the strongest response?

- A) Agree; conformance is the requirement.
- B) Agree that conformance is the requirement and point out that it is a floor rather than a goal — where two options both conform, the evidence from disabled users is the only thing distinguishing them, and disregarding it means choosing the worse option deliberately while meeting the letter of the standard.
- C) Argue that the preference testing overrides conformance.
- D) Escalate.

**Correct answer: B**

**Explanation:** The stakeholder is right about the requirement and wrong about the decision, and the strongest response concedes the first to win the second. Conformance is a legal floor; it is not a description of a good experience, and where two options both clear it the standard has stopped discriminating and the user evidence starts. Option B makes that argument in a form that does not require the stakeholder to have been wrong, which is what makes it likely to succeed. This is also where your role's representative function does real work: bringing the voice of disabled users is not a slogan when it is the only evidence distinguishing two compliant options. Option A abandons the position. Option C sets up a false conflict, since nobody is proposing to breach the standard. Option D escalates a conversation you can win.

### Preparation tips

- **Read criteria at their boundaries and their scopes.** Over-application costs credibility the real findings need.
- **Separate severity from compliance.** A conforming service can be unusable; a failure can be trivial.
- **Write findings with four parts.** Location, technical fault, user impact, remedy.
- **Rank by consequence, not instance count.**
- **Ask what a conformance claim actually covered.** Isolation and defaults, usually.
- **Separate the information from its presentation.** It resolves most "we cannot make this accessible" problems.
- **Look for the shared cause behind recurring defects.** Missing accessible names is usually a tooling problem.
- **Use the accessibility statement for disclosure, not for cover.**

### Common pitfalls to avoid

- **Reporting an over-application as a failure.** A team that fixes two unnecessary things starts checking your findings.
- **Treating all failures as equivalent.** It produces reports nobody acts on.
- **Naming a criterion without naming the fault.** A developer cannot act on "fails 1.3.1".
- **Dismissing user evidence because a service conforms.**
- **Treating a supplier's conformance claim and your audit as a straight contradiction.**
- **Prescribing training where a linting rule would do the work.**
- **Issuing verdicts rather than solutions.** It gets you consulted late.
- **Ranking findings by how quick they are to fix.**

## Workplace job-specific numeric reasoning assessment

### About this assessment

A numeric reasoning assessment measures how accurately you handle the quantitative material your role produces and consumes. Accessibility work is unusually full of numbers with thresholds attached: contrast ratios, target sizes, timing limits, reflow widths, text spacing multipliers. It is also full of numbers used in argument — prevalence figures, audit counts, remediation estimates, and the population sizes that determine whether a barrier affects a handful of people or a hundred thousand.

That second category is where this section earns its place. Accessibility arguments are frequently lost not because the technical case is weak but because it is presented as a technical case in a room making a resourcing decision. "This fails 1.4.3" competes with everything else in a backlog; "this affects an estimated 34,000 people a year, and the organisation has a statutory duty" does not. Being fluent with the arithmetic is what lets you make the second argument, and your role's requirement to manage stakeholder expectations and host difficult discussions with senior stakeholders assumes it.

The format is typically a timed online test of fifteen to thirty minutes, each item presenting a table, chart or paragraph of figures with a multiple-choice question. Calculators are usually provided.

Four habits carry the load. Establish what the question asks before looking at the data. Identify the denominator and the population it represents. Estimate, calculate, compare. And sanity-check against the world.

### How this assessment maps to your role

The numerical skills tested map onto your named skills:

- **Ratios and thresholds** map to **Technical understanding (accessibility)**, where knowing standards including edge cases is a numerical matter as much as a conceptual one.
- **Prevalence and population arithmetic** map to **Communicating information**, where managing stakeholder expectations depends on expressing impact in terms they weigh.
- **Comparing rates between groups** maps to **User focus**, where championing research to focus on all users means being able to show the gap.
- **Estimating remediation** maps to **Leadership and guidance**, where decisions of medium risk and complexity require a sense of cost.
- **Interpreting audit data** maps to **Governance and assurance (accessibility)**, where risk is a function of severity and scale.
- **Detecting misleading figures** maps to **Consultancy**, where advice built on a misread number is hard to withdraw.

### Practice questions

**Question 1 (easy) — Thresholds at the boundary**

A criterion requires 4.5:1 for text under 24 pixels and 3:1 for text 24 pixels or larger. Four items: 14px at 4.4:1; 18px at 4.5:1; 24px at 2.9:1; 28px at 3.0:1. How many conform?

- A) 1
- B) 2
- C) 3
- D) 4

**Correct answer: B**

**Explanation:** 14px needs 4.5:1 — 4.4 fails. 18px needs 4.5:1 — 4.5 meets it exactly, and "at least" is inclusive. 24px falls into the larger category because the wording is "24 or larger" rather than "over 24", so needs 3:1 — 2.9 fails. 28px needs 3:1 — 3.0 passes. Two conform, giving B. Each of the three boundary readings produces real errors in audit work: reporting 4.5 as a fail is an over-application, reporting 24px against 4.5:1 applies the wrong threshold, and rounding 4.4 up is a false pass. In a discipline where your findings carry statutory weight, being precisely right at the boundary is not pedantry — it is the whole basis on which teams take your reports seriously.

**Question 2 (easy) — Prevalence arithmetic**

A service has 850,000 users a year. If around 1 in 12 men and 1 in 200 women have red-green colour vision deficiency, and the user base is roughly evenly split by sex, roughly how many affected users a year?

- A) 3,500
- B) 37,500
- C) 70,000
- D) 106,000

**Correct answer: B**

**Explanation:** Take each group. Men: half of 850,000 is 425,000, and 1 in 12 is 425,000 ÷ 12 ≈ 35,400. Women: 425,000 ÷ 200 ≈ 2,100. Together about 37,500, giving B. Option C doubles the male figure by applying the male rate to everyone; option A applies the female rate to everyone. The reason this calculation belongs in your toolkit is what it does to a conversation: "colour blindness is rare" is an intuition that collapses instantly against 37,500 people a year, and the arithmetic takes twenty seconds. Note also the honest framing — "roughly" and "around" — because prevalence figures vary by source and population, and a specialist who presents an estimate as a precise count invites a challenge that distracts from the point.

**Question 3 (easy) — Audit counts and severity**

An audit found 2 blockers, 11 serious and 28 minor issues across a service. What proportion of findings are blockers or serious?

- A) 24%
- B) 32%
- C) 68%
- D) 76%

**Correct answer: B**

**Explanation:** The total is 2 + 11 + 28 = 41. Blockers and serious together are 13, and 13 ÷ 41 = 0.317, about 32%, giving B. Option C is the minor proportion. The figure is worth computing because it changes how a report reads: "forty-one findings" sounds overwhelming and unactionable, while "thirteen findings that matter before release, of which two are blockers" is a plan. At your level the presentation of an audit is part of the audit, and a report whose headline number is forty-one is one a team is more likely to file than act on.

**Question 4 (easy) — Reflow arithmetic**

A criterion requires content to reflow without horizontal scrolling at a viewport width equivalent to 320 CSS pixels. A page is designed at 1,280 pixels wide. What zoom level produces an equivalent effective width of 320 pixels?

- A) 200%
- B) 300%
- C) 400%
- D) 500%

**Correct answer: C**

**Explanation:** Zooming reduces the effective viewport width proportionally: at 400% zoom, a 1,280-pixel viewport has an effective width of 1,280 ÷ 4 = 320 pixels. So C. Option A gives 640 and option D gives 256. The relationship is worth holding because it is how the reflow requirement is usually tested in practice — you do not resize a window to 320 pixels, you zoom a 1,280-pixel window to 400% — and a specialist who cannot do that conversion in their head cannot explain to a developer why 400% is the test rather than an arbitrary large number.

**Question 5 (moderate) — Comparing groups fairly**

Of 1,200 users on a service, 1,080 completed a task. Of 150 screen reader users, 45 completed. What is the gap in percentage points?

- A) 30
- B) 60
- C) 70
- D) 90

**Correct answer: B**

**Explanation:** General users: 1,080 ÷ 1,200 = 90%. Screen reader users: 45 ÷ 150 = 30%. The gap is 60 percentage points, giving B. Options A and D are the two group rates offered as if they were the gap — a distractor pattern worth recognising, since figures from your working frequently appear among the options. A 60 point gap is extreme, and the way to present it matters: the rates are the finding, and "screen reader users complete this task at one third the rate of other users" is the sentence that travels, because it converts two percentages into a single comparison anyone can hold.

**Question 6 (moderate) — Small-base caution**

An audit reports "only 3% of screen reader users completed the checkout", based on 1 of 33 participants. What is the strongest observation?

- A) The finding is clear.
- B) The arithmetic is right and the base is too small to support a percentage at that precision — one more success would make it 6% — so the honest statement is "1 of 33 participants completed", which is a devastating finding on its own and does not need a rate to carry it.
- C) More participants are needed before reporting.
- D) The figure should be rounded.

**Correct answer: B**

**Explanation:** The arithmetic is correct: 1 ÷ 33 is about 3%. The problem is that a percentage from a base of 33 with a single success implies a precision the data does not have, and a stakeholder who notices will use it to discount the whole report. Option B says this and makes the more important point: "1 of 33 participants completed" is a stronger sentence than "3%", because it is unarguable and because the raw form conveys the scale of the failure more vividly than a small percentage does. Option C would delay a finding that is already conclusive — 32 failures out of 33 does not need more participants to be believed. Option A invites the challenge. Option D adjusts presentation without addressing the issue.

**Question 7 (moderate) — Estimating remediation**

An audit found 14 instances of missing alt text across 6 templates. A developer estimates 20 minutes per instance. What is the most useful thing to establish before accepting the estimate?

- A) Whether 20 minutes is reasonable.
- B) Whether the 14 instances sit in 14 places or in 6 templates — because if the images are template-level, fixing 6 templates resolves all 14, and the estimate should be around 2 hours rather than nearly 5.
- C) Whether the developer has done this before.
- D) The total, which is 4 hours 40 minutes.

**Correct answer: B**

**Explanation:** The question hands you the key fact and the distractor together: 14 instances across 6 templates. If the images are in templates rather than in content, the unit of work is the template, and the estimate falls by more than half. Option B establishes that, and it matters beyond the arithmetic — a remediation estimate that treats instances as independent will consistently overstate template-level work and understate content-level work, and a specialist who accepts estimates without asking has no basis for advising on what is achievable before a deadline. Option D computes the total the estimate implies without questioning its basis. Option A asks about the rate rather than the count, which is the less consequential half. Option C is a management question rather than a technical one.

**Question 8 (moderate) — Scale of a shared defect**

A component with a keyboard trap is used across 9 services with combined annual sessions of 3.6 million. Around 3% of sessions involve keyboard-only navigation. How many sessions a year are affected?

- A) 10,800
- B) 108,000
- C) 1,080,000
- D) 36,000

**Correct answer: B**

**Explanation:** 3% of 3,600,000 is 0.03 × 3,600,000 = 108,000, giving B. Option A is 3% of 360,000; option D is 1%. This is the calculation that converts a component defect into an organisational priority. "A keyboard trap in the modal component" is a ticket; "108,000 sessions a year in which a keyboard user cannot leave a dialogue" is a decision. Note that the 3% figure covers keyboard-only navigation specifically and understates the affected population, since a keyboard trap also affects switch users, voice control users and people using a keyboard temporarily — which is worth saying when you present the number, because it makes the estimate conservative rather than contestable.

**Question 9 (moderate) — Percentage change**

Reported accessibility defects across an estate fell from 640 to 480 over a year, after a linting rule was added to the build pipeline. What is the change, and what should you check?

- A) 25% decrease, demonstrating the rule worked
- B) 25% decrease, and the check is whether the rule catches the defect types that fell — if the fall is concentrated in missing accessible names, which linting detects, that supports attribution; if it is spread evenly, something else is happening
- C) 33% decrease, demonstrating the rule worked
- D) 33% decrease, with the same caution

**Correct answer: B**

**Explanation:** The difference is 160, and 160 ÷ 640 = 0.25, a 25% decrease, so options C and D miscalculate by dividing by the new figure. Between A and B the analysis decides it, and B names the specific check that would establish attribution: linting catches a defined class of defect, mostly missing accessible names and invalid ARIA, so if the fall is concentrated there the causal story holds, and if it is distributed across defect types the rule probably is not responsible. That distinction matters because you will be asked whether the intervention worked, and a specialist who claims credit for a fall they have not attributed will be caught when the next year's figures move the other way.

**Question 10 (harder) — A conformance percentage**

A report states "the service is 94% conformant". What is the strongest observation?

- A) 94% is good.
- B) Conformance is not a percentage — a service either meets each success criterion or does not, and a single unmet criterion means the service does not conform at that level; "94%" probably means 94% of *checks* passed, which tells you nothing about severity, since one failed check can be a total barrier.
- C) The remaining 6% should be fixed.
- D) The figure should specify which criteria.

**Correct answer: B**

**Explanation:** This is a category error that appears constantly in supplier reports and internal dashboards, and recognising it is a core piece of professional literacy. Conformance is binary per criterion and per page: a service meets AA or it does not. A percentage is a count of passed checks, and it obscures exactly what matters, because a service failing one criterion — a keyboard trap, say — is unusable for a group of people while scoring 99%. Option B says this. Option C accepts the framing and treats the remaining 6% as a proportionate remainder rather than asking what is in it. Option D is a real improvement and stops short of the main point. At your level the useful move is to ask for the list of unmet criteria, because that is the only form in which the answer is meaningful.

**Question 11 (harder) — Weighted comparison across services**

Four services report defects per hundred components: 3 on 400 components, 9 on 100, 5 on 200, and 4 on 300. What is the overall rate per hundred?

- A) 4.3
- B) 4.6
- C) 5.25
- D) 6.0

**Correct answer: A**

**Explanation:** Convert to counts. 3 per hundred on 400 = 12 defects. 9 per hundred on 100 = 9. 5 per hundred on 200 = 10. 4 per hundred on 300 = 12. Total 43 defects across 1,000 components, so 4.3 per hundred, giving A. Option C is the unweighted mean of 3, 9, 5 and 4, which is 5.25 and over-weights the 100-component service against the 400-component one. Always return to counts. The organisational point matters more than the arithmetic: the unweighted figure describes the average *service*, while the weighted figure describes the average *component* — and only the second describes what users encounter, which is the figure that belongs in a report to a board.

**Question 12 (harder) — Presenting risk**

You need to advise a board on the risk of launching with eleven unresolved serious findings. Which framing is strongest?

- A) The service does not conform to WCAG 2.2 AA.
- B) Eleven serious findings remain, affecting an estimated number of users in specific ways — set out the two or three with the largest affected populations and no workaround, state the statutory position plainly, and present the disclosed-and-planned option against the undisclosed one, since those are materially different risk positions.
- C) The service has an 11-item backlog.
- D) The risk is legal and should go to the legal team.

**Correct answer: B**

**Explanation:** A board decides on consequence and exposure, and option B supplies both in a form it can act on. Naming the two or three findings with the largest affected populations and no workaround converts eleven abstractions into a decision, because a board cannot weigh eleven items but can weigh three. Stating the statutory position plainly is necessary and insufficient on its own, which is why option A fails — "does not conform" is true, familiar, and does not tell anyone what will happen or to whom. The final element is the one specialists most often omit: an organisation launching with disclosed, planned gaps is in a materially different position from one launching with the same gaps undisclosed, and making that distinction visible is frequently what turns a board towards the responsible option. Option C strips the risk out entirely. Option D outsources a judgement your role exists to make.

### Preparation tips

- **Read thresholds at the boundary.** Over-application costs credibility the real findings need.
- **Convert prevalence into people, and say "roughly".** An estimate presented as a count invites a distracting challenge.
- **Report small bases as counts, not percentages.** "1 of 33" is stronger than "3%".
- **Ask whether instances are template-level.** It changes a remediation estimate by more than half.
- **Convert shared-component defects into sessions.** It is what turns a ticket into a decision.
- **Return to counts before combining rates.**
- **Reject conformance percentages.** Ask for the list of unmet criteria.
- **Present risk as consequence, population and disclosure position.**

### Common pitfalls to avoid

- **Rounding a contrast ratio.**
- **Applying the wrong threshold at 24 pixels.**
- **Reporting a percentage from a base of 33.**
- **Accepting a remediation estimate without asking what the unit of work is.**
- **Claiming credit for a fall in defects you have not attributed.**
- **Accepting "94% conformant" as meaningful.**
- **Averaging service-level rates without weighting.**
- **Presenting risk as non-conformance alone.** It is true and tells a board nothing.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A verbal reasoning assessment measures how accurately you read. For most disciplines that is a useful proxy; for yours it is close to the job. Accessibility practice is built on documents written with unusual precision — success criteria, understanding documents, regulations, exemptions, procurement standards — and your authority rests on reading them exactly as written. A specialist who over-reads a criterion loses credibility; one who under-reads it lets a barrier through.

The classic format presents a short passage of dense workplace prose, typically three to six sentences, followed by statements to classify as True, False or Cannot Say. True means the statement follows necessarily. False means the passage contradicts it. Cannot Say means the passage neither establishes nor excludes it. Alongside these come comprehension items, main-point items, and questions asking which of four summaries is most accurate.

The governing rule is that you answer from the passage alone. Your professional knowledge must be set aside, and this is harder for you than for most candidates: you know these documents, and the more you know them, the more readily you supply the clause you expect rather than the one in front of you. That is the characteristic error at your level.

Cannot Say deserves particular attention. Specialists avoid it because forming a definite view is what the job consists of — a team asking whether something conforms wants an answer. In this section, and occasionally in practice, the honest answer is that the document does not determine it.

Small words carry the load. "All" is not "most". "May" is not "must". "Or" offers alternative routes and reading it as "and" produces over-application. "Substantially" and "pre-recorded" and "essential" are the load-bearing qualifiers in accessibility regulation, and each has decided real disputes.

### How this assessment maps to your role

The verbal skills tested map onto your named skills:

- **Reading precisely** maps to **Technical understanding (accessibility)**, where excellent knowledge of standards and legislation including edge cases is named.
- **Separating statement from inference** maps to **Consultancy**, where advice must be traceable to what a document actually says.
- **Identifying the main point** maps to **Communicating information**, where you communicate requirements to a range of stakeholders.
- **Handling qualified language** maps to **Governance and assurance (accessibility)**, where knowing exactly what a requirement bites on determines the risk position.
- **Reading for absence** maps to **Technical understanding**, where noticing that a specification never addresses a case is what stops you asserting one.
- **Reading exemptions accurately** maps to **Governance and assurance**, where a misread exemption is a compliance failure or an unnecessary cost.

### Practice questions

*Passage A — for Questions 1 to 4*

"Public sector bodies must ensure their websites meet the accessibility standard. This does not apply to pre-recorded time-based media published before 23 September 2020, to live time-based media, to online maps provided the essential information is available in an accessible alternative format, or to content on an intranet or extranet published before 23 September 2019 and not substantially revised since. Third-party content that the body neither funds, develops nor controls is also outside scope."

**Question 1 (easy)** — Statement: "All content on a public sector website must meet the standard." True, False or Cannot Say?

**Correct answer: False**

**Explanation:** The passage lists five categories outside scope. The statement's "all" contradicts them, so False. This is the pattern the section relies on, and it is worth noticing that the exemptions here are not marginal — pre-recorded media, live media, maps, older intranet content and third-party content between them cover a substantial amount of what a large organisation publishes. A specialist who carries "everything must conform" as a working assumption will spend effort on content outside scope and be corrected by somebody less expert, which is an avoidable way to lose standing.

**Question 2 (easy)** — Statement: "A live-streamed event published in 2018 is exempt." True, False or Cannot Say?

**Correct answer: True**

**Explanation:** The passage exempts live time-based media without any date condition — the date applies to the *pre-recorded* exemption, not the live one. A live stream is therefore exempt regardless of when it was published, and the statement follows. True. The item tests whether you attach the date qualifier to the right clause. A reader carrying "there's a 2020 date on media" as a general rule will check whether 2018 is before 2020, find that it is, and reach the right answer for the wrong reason — which will fail them the moment they meet a live stream from 2023.

**Question 3 (moderate)** — Statement: "An online map is exempt." True, False or Cannot Say?

**Correct answer: Cannot Say**

**Explanation:** The exemption for online maps is conditional: it applies *provided the essential information is available in an accessible alternative format*. Whether that condition is met is not stated, so the case is undetermined. Cannot Say. This is among the most commonly misapplied exemptions in practice, because the phrase "maps are exempt" circulates as though it were unconditional, and a specialist who repeats it lets teams publish a map with no alternative and believe they are compliant. Note also what the condition requires — essential information in an accessible form, not the map itself — which for a map showing office locations means an address list, and is usually straightforward once somebody asks.

**Question 4 (harder)** — Statement: "Intranet content published in 2018 and rewritten last month is exempt." True, False or Cannot Say?

**Correct answer: False**

**Explanation:** The intranet exemption has two conditions: published before 23 September 2019 *and* not substantially revised since. Content rewritten last month has been substantially revised, so the second condition fails and the exemption does not apply. False. The compound structure is what the item tests, and it is a live issue in practice: organisations frequently assume that old intranet content stays exempt indefinitely, when in fact the exemption lapses the moment somebody substantially updates it. That has a counter-intuitive implication worth knowing — improving old content brings it into scope, which is not a reason to avoid improving it but is a reason to plan for the accessibility work at the same time.

*Passage B — for Questions 5 to 8*

"The audit of the department's services found that teams with an accessibility specialist embedded reported fewer defects at launch than teams without. The audit notes that embedded specialists were assigned to services judged higher risk at the outset. The audit did not assess whether the services were more accessible in use. It recommends that the head of accessibility consider whether embedding should be extended."

**Question 5 (easy)** — Statement: "Teams with an embedded specialist reported fewer defects at launch." True, False or Cannot Say?

**Correct answer: True**

**Explanation:** The first sentence states this directly and the statement restates it without addition. True. Note the passage's careful "reported fewer defects" rather than "had fewer defects", and the statement respects it. Answer quickly and bank the time for harder items.

**Question 6 (moderate)** — Statement: "Embedding a specialist reduces defects." True, False or Cannot Say?

**Correct answer: Cannot Say**

**Explanation:** The passage reports an association and then flags that embedded specialists were assigned to services judged higher risk at the outset — which, if anything, works against the association, since higher-risk services would be expected to produce more defects rather than fewer. That makes the finding more interesting and no more conclusive: the assignment was not random, the risk judgement may have been wrong, and other differences may explain it. Cannot Say. This is the specific trap for someone in your position, because "embedding specialists reduces defects" is a claim you would like to be true and would certainly cite when arguing for more embedded posts. Citing it and being asked about the assignment is how a good proposal loses.

**Question 7 (moderate)** — Statement: "Services with embedded specialists are more accessible in use." True, False or Cannot Say?

**Correct answer: Cannot Say**

**Explanation:** The passage says explicitly that the audit did not assess accessibility in use. Declared silence establishes nothing, so Cannot Say. The distinction between defects reported at launch and accessibility in use is exactly the conformance-versus-experience boundary your role names, and it matters here: a team with an embedded specialist might produce fewer catalogued defects and a service that is still difficult to use, or might produce a genuinely better service that the defect count understates. The audit chose not to look, and treating its silence as evidence in either direction is the error.

**Question 8 (harder)** — Statement: "The audit recommends extending embedding." True, False or Cannot Say?

**Correct answer: False**

**Explanation:** The audit recommends that the head of accessibility *consider whether* embedding should be extended — a recommendation to evaluate, including the possibility of concluding it should not be. The statement asserts a recommendation to extend, which was not made, so False rather than Cannot Say: the passage tells you what was recommended and it was something different. This pervades audit prose, and in your field it has a particular edge — recommendations about accessibility resourcing are quoted selectively by people on both sides of a resourcing argument, and being the person who reads them accurately is worth more than being the person who quotes them enthusiastically.

*Passage C — for Questions 9 to 12*

"A conformance claim must state the standard and level claimed, the date, the scope of the claim including the pages covered, and any technologies relied upon. Where a page contains third-party content outside the body's control, the claim may exclude that content provided the exclusion is stated. A claim may not be made for a level unless every applicable success criterion at that level and all lower levels is met. Partial conformance may be claimed for content produced by third parties only where the body has requested remediation."

**Question 9 (easy)** — Statement: "A conformance claim must state which pages it covers." True, False or Cannot Say?

**Correct answer: True**

**Explanation:** The first sentence requires the claim to state its scope including the pages covered. The statement restates that, so True. Answer quickly. It is worth noticing why the requirement exists: an unscoped conformance claim is unfalsifiable and therefore worthless, and a great many published claims are exactly that — which makes "which pages does this cover?" one of the most useful questions you can ask of a supplier's documentation.

**Question 10 (moderate)** — Statement: "A service meeting all AA criteria but failing one A criterion may claim AA conformance." True, False or Cannot Say?

**Correct answer: False**

**Explanation:** The third sentence requires every applicable criterion at the claimed level *and all lower levels* to be met. A failure at A means AA cannot be claimed, so the statement is contradicted. False. This is a genuinely common misunderstanding, because the levels look like a ladder on which you might stand on a higher rung while missing a lower one, and the structure is cumulative instead. The practical consequence is that a single unmet A criterion — a missing page title, say — invalidates an AA claim for the whole page, which is worth knowing before you accept a claim and before you make one.

**Question 11 (harder)** — Statement: "A body may exclude uncontrolled third-party content from a claim without saying so." True, False or Cannot Say?

**Correct answer: False**

**Explanation:** The second sentence permits excluding such content *provided the exclusion is stated*. Excluding it silently fails that condition, so the statement is contradicted. False. The condition is doing real work: an unstated exclusion makes a claim misleading rather than merely narrow, since a reader would reasonably assume the claim covers what is on the page. Note the contrast with Question 12's territory — the passage permits two different treatments of third-party content depending on control and on whether remediation was requested, and conflating them is easy.

**Question 12 (harder) — Main point**

Which best captures the main point of Passage C?

- A) Conformance claims must state the standard and level.
- B) A conformance claim must be scoped, dated and honest about its limits — stating what it covers and what it relies on, excluding uncontrolled third-party content only openly, and claiming a level only where every criterion at that level and below is met.
- C) Partial conformance may be claimed for third-party content.
- D) A claim may not be made unless all criteria are met.

**Correct answer: B**

**Explanation:** The main point must cover the whole passage while adding nothing. Option A is one element of the first sentence. Option C is one conditional clause. Option D is close and drops both the level structure — "at that level and all lower levels" — and everything about scoping and disclosure. Option B captures the four elements and the logic joining them: a claim is a public statement others rely on, so it must say what it covers, what it depends on, what it leaves out, and it must not overstate the level. Note that B preserves the conditions that the shorter options discard, which is the difference between a summary a colleague can act on and one that will mislead them.

### Preparation tips

- **Point at the words.** Before marking True, identify the phrase that makes it true. Your expertise makes this harder, not easier.
- **Attach qualifiers to the right clause.** The 2020 date applies to pre-recorded media, not to live.
- **Treat conditional exemptions as conditional.** "Maps are exempt" is a dangerous abbreviation.
- **Watch compound conditions.** The intranet exemption needs both a date and no substantial revision.
- **Trust Cannot Say, especially where the claim would support your case.**
- **Remember conformance levels are cumulative.** One A failure defeats an AA claim.
- **Ask what a claim covers.** An unscoped claim is unfalsifiable.
- **Separate "consider whether X" from "recommend X".**

### Common pitfalls to avoid

- **Answering from professional knowledge.** The dominant error for specialists.
- **Carrying "everything must conform" as a working assumption.**
- **Repeating an exemption without its condition.** It lets teams publish and believe they are compliant.
- **Assuming an exemption survives a substantial revision.**
- **Marking True on a claim that would support more resource for your function.**
- **Treating conformance levels as independent rungs.**
- **Accepting an unscoped conformance claim.**
- **Reading "or" as "and".** It produces over-application, which costs you credibility.

## Workplace job-specific situational judgement assessment

### About this assessment

A situational judgement assessment presents realistic workplace scenarios and asks what you would do. There is no passage to parse and no arithmetic. You get a dilemma of the kind your role produces, four or five candidate responses, and a question asking which is most effective and often which is least.

This section measures whether your judgement matches what the profession considers good practice at your level. Your role description places you as someone who embeds accessibility into the output of teams, coaches and mentors, inputs into strategy, delivers training, engages across levels and capabilities, and may lead individuals or sub-teams. The strongest answers involve advising rather than instructing, holding a position where the evidence warrants it, and building capability rather than becoming the person everything routes through.

Four principles carry most scenarios, and one of them is specific to your discipline.

Disabled users come first, and the asymmetry matters: a barrier is not a slightly worse experience, it is no experience, and that is why accessibility findings rarely lose to convenience arguments on the merits even when they lose on the day.

Be accurate before you are forceful. This is the distinctively accessibility-specialist principle and it runs through this section. Your findings carry statutory weight, which makes them powerful and makes over-application expensive: a specialist who reports something as a failure when it is not, or cites a requirement that does not bite, spends credibility that the genuine requirements need. Being scrupulously right is not caution, it is what makes you effective.

Advise with a route, not a verdict. A specialist who only says no is consulted late, when saying no is all that is left.

Build capability rather than dependency. Your role names coaching, mentoring and training, and a team that can catch its own defects is worth more than one that waits for your audit.

### How this assessment maps to your role

The judgement dimensions map onto your named skills:

- **Advising and recommending** maps to **Consultancy**, where you provide advice based on significant specialist knowledge.
- **Coaching and building capability** maps to **Leadership and guidance**, and to your role level's named coaching and training responsibilities.
- **Handling difficult conversations** maps to **Communicating information**, where you host or moderate difficult discussions with teams and senior stakeholders.
- **Managing risk proportionately** maps to **Governance and assurance (accessibility)**, where you challenge teams and reduce risk.
- **Representing disabled users** maps to **User focus**, where you champion research focused on all users.
- **Technical judgement** maps to **Technical understanding (accessibility)**, including edge cases and the boundary with usability.

### Practice questions

**Question 1 (easy) — A team disputes a finding**

A developer says your finding is wrong: the element you flagged has an ARIA label, so it is not missing an accessible name. You checked and the label is present but does not match the visible text. What is the most effective response?

- A) Restate the finding.
- B) Acknowledge that the label is present and explain the specific issue — that a visible label and an accessible name which differ break voice control, because a user saying the visible words does not activate the control — then correct your finding to name the actual fault rather than a missing name.
- C) Withdraw the finding.
- D) Escalate to their lead.

**Correct answer: B. Least effective: A**

**Explanation:** The developer is partly right, and the most effective response concedes that immediately and precisely. The element does have an accessible name, so the finding as written was inaccurate — and correcting it costs nothing while establishing that your findings are checked rather than asserted. The actual fault is different and worth explaining: where a visible label and an accessible name diverge, voice control users saying what they can see fail to activate the control, which is a specific and demonstrable barrier. Option B does both. Option A is least effective, restating a finding that has been shown to be inaccurately worded, which teaches the developer that your reports are not worth reading carefully. Option C over-corrects and drops a genuine issue. Option D escalates a technical disagreement with a technical answer.

**Question 2 (easy) — Training that does not land**

You have delivered accessibility training to six teams. Defect rates have not changed. What is the most effective response?

- A) Deliver the training again with clearer material.
- B) Find out what is preventing the behaviour rather than assuming the knowledge did not land — most likely that nothing in the workflow requires a check, or that checking is manual and skipped under pressure — then put a check where work already flows, ideally automated.
- C) Make the training mandatory.
- D) Increase audit frequency.

**Correct answer: B. Least effective: A**

**Explanation:** Training that has not changed behaviour is evidence that knowledge was not the barrier, and repeating it is the characteristic failure of well-intentioned improvement work. Option B does the diagnostic work first and names the realistic blockers, which concern *when and how* checking happens rather than whether people know it should. The remedy it points at is unusually strong in this discipline, because a meaningful class of accessibility defects — missing accessible names, invalid ARIA, missing language attributes — can be caught mechanically, which removes reliance on anyone remembering. Option A is least effective, repeating an intervention that demonstrably did not work and spending the credibility of the next one. Option C mandates attendance at something that has not changed behaviour. Option D increases detection without reducing occurrence, raising your own workload permanently.

**Question 3 (easy) — A junior colleague's audit**

A junior specialist's audit reports nineteen findings, of which you judge four to be over-applications — criteria cited where they do not bite. What is the most effective response?

- A) Correct the report before it goes out.
- B) Go through the four with them, explaining in each case why the criterion does not apply, and agree that they will re-issue it — because a report going out with four over-applications damages their standing with the team more than a day's delay does.
- C) Send it as it is and correct the record later.
- D) Ask them to remove the four without explanation.

**Correct answer: B. Least effective: C**

**Explanation:** Two things need to happen: the report goes out accurate, and the junior specialist learns why. Option B does both, and the reasoning it names is the one worth passing on — over-applications are not merely inaccurate, they are the specific way an accessibility specialist loses a team's trust, because a developer who fixes something unnecessary starts checking every subsequent finding. Having them re-issue it rather than doing it yourself is what makes it coaching rather than correction. Option C is least effective, letting inaccurate findings reach a team and then correcting them, which is the sequence most damaging to their credibility and yours. Option A protects the report and teaches nothing. Option D produces a corrected report and a colleague who does not know what they got wrong.

**Question 4 (moderate) — A team asks for a shortcut**

A team asks whether they can launch with a known keyboard trap and fix it in the first patch, two weeks later. What is the most effective response?

- A) Say no; a keyboard trap is a blocker.
- B) Explain what a keyboard trap means in practice — a keyboard user entering the dialogue cannot leave it, so their session ends there with no workaround — establish whether the trap can be removed by reverting to the standard component rather than fixing the custom one, and if it genuinely cannot, put the launch decision to whoever owns the risk with that description attached.
- C) Agree, provided an accessibility statement discloses it.
- D) Escalate immediately.

**Correct answer: B. Least effective: C**

**Explanation:** A keyboard trap is about as serious as accessibility defects get, and option B holds that while doing three useful things. Describing the consequence concretely is what makes the severity legible to people who cannot picture it. Checking whether reverting to a standard component removes the trap is the practical step that most often resolves this, and one nobody thinks of under launch pressure. And putting the decision to the risk owner rather than deciding yourself is correct — you advise, and a launch decision belongs to somebody accountable for it. Option C is least effective: an accessibility statement discloses gaps you are working on, and using it to authorise launching with a total barrier misuses the mechanism and sets a precedent that will be quoted at you. Option A is right in substance and offers no route, which is how specialists get consulted late.

**Question 5 (moderate) — Disagreement with a designer**

A designer argues that a status system using colour plus position is sufficient, since position is a second cue. You are unsure. What is the most effective response?

- A) Cite the criterion and require an icon or text.
- B) Establish whether position genuinely conveys the status independently — if the items are in a fixed order that means something, it may; if the order is arbitrary or changes, it does not — and test it by describing the interface to someone without seeing it, since that is close to what the requirement is asking.
- C) Concede; two cues are enough.
- D) Escalate.

**Correct answer: B. Least effective: A**

**Explanation:** The designer has made a legitimate argument that may be right, and the honest position is that it depends on facts you have not established. Redundant encoding is exactly what the requirement asks for, and position can be a genuine second cue — a fixed leftmost column meaning "overdue" carries information independently of colour. Whether it does here depends on whether the order is stable and meaningful. Option B establishes that and proposes a cheap test. Option A is least effective, asserting a criterion in circumstances where it may not be breached, which is the over-application that costs you the next argument. Option C concedes without checking, which is the mirror error. Option D escalates a question with a technical answer available in ten minutes.

**Question 6 (moderate) — A supplier's conformance claim**

Procurement asks whether a supplier's "fully WCAG 2.2 AA conformant" claim is sufficient assurance. What is the most effective response?

- A) Yes; the claim is explicit.
- B) Ask what the claim covers — which pages or components, tested in isolation or composed, with which assistive technologies, and at what date — because conformance claims are commonly established for components under default configuration, and defects appear when they are composed and customised; then advise procurement to require the claim's scope be stated in the contract.
- C) No; supplier claims cannot be trusted.
- D) Commission your own audit before contract.

**Correct answer: B. Least effective: A**

**Explanation:** A conformance claim without a stated scope is close to meaningless, and the questions in option B are the ones that make it assessable. The final clause is what makes this a senior response: requiring the scope in the contract converts a marketing statement into an obligation, which is far more valuable than any assessment you could make of the claim as it stands. Option A is least effective, treating an unscoped claim as assurance, which is precisely how organisations acquire inaccessible systems with paperwork saying otherwise. Option C is unhelpfully absolute and will get you excluded from procurement conversations. Option D is expensive, slow, and may be right for a major system — but asking the scoping questions costs nothing and frequently makes the audit unnecessary or much narrower.

**Question 7 (moderate) — Bringing the voice of disabled users**

A team is choosing between two designs. Both conform. Testing with disabled users shows a clear preference. A stakeholder says conformance is the requirement. What is the most effective response?

- A) Agree; conformance is the requirement.
- B) Agree that conformance is the requirement, and point out that it is a floor rather than a goal — where both options conform, the standard has stopped discriminating and the evidence from disabled users is the only thing distinguishing them, so disregarding it means deliberately choosing the worse option while meeting the letter of the rule.
- C) Argue that the preference evidence overrides conformance.
- D) Escalate.

**Correct answer: B. Least effective: C**

**Explanation:** The stakeholder is right about the requirement and wrong about the decision, and option B concedes the first to win the second — which is what makes it likely to succeed. Conformance is a legal floor and not a description of a good experience, and where two options both clear it the criteria have nothing further to say. This is also where your role's representative function does real work: bringing the voice of disabled users is not rhetoric when it is the only evidence distinguishing two compliant options. Option C is least effective, setting up a false conflict in which you appear to be arguing against the standard — nobody is proposing a breach, and framing it that way lets the stakeholder dismiss the evidence as a preference. Option A abandons the position.

**Question 8 (harder) — A finding nobody wants**

Two days before launch you find a barrier affecting screen reader users on the payment step. Fixing it delays launch. The delivery manager says the risk is small because few users use screen readers. What is the most effective response?

- A) Insist on the delay.
- B) Supply the arithmetic — even a conservative proportion of the service's user base runs to thousands of people a year, and a barrier at payment means they cannot complete a transaction at all — set out the statutory position plainly, check whether a temporary alternative route exists, and put the decision to whoever owns the risk with a recorded answer.
- C) Agree; the numbers are small.
- D) Escalate to the head of accessibility immediately.

**Correct answer: B. Least effective: C**

**Explanation:** The delivery manager's argument rests on an intuition about proportion, and intuitions about proportion collapse against a base number — which is why option B leads with arithmetic rather than principle. It then does three further things: states the statutory position, because a barrier at payment has a legal dimension that a barrier on a content page may not; looks for a temporary alternative, since a phone route or an assisted channel may make launching defensible; and puts the decision to the risk owner with a recorded answer, because an unrecorded decision drifts into launch by default. Option C is least effective, accepting an argument that would justify excluding any minority. Option A is right in substance and offers no route. Option D may be appropriate if the decision goes badly, and going there first bypasses the person who should decide.

**Question 9 (harder) — Capability rather than dependency**

Teams increasingly send you every design for accessibility review before build. Your queue is now three weeks long. What is the most effective response?

- A) Work through the queue faster.
- B) Recognise the queue as a signal that you have become a dependency rather than a capability: identify the checks teams could reliably do themselves, give them the means to do so, and reserve your review for genuinely complex or high-risk cases — then measure whether the queue shortens.
- C) Ask for another specialist.
- D) Introduce criteria for what qualifies for review.

**Correct answer: B. Least effective: A**

**Explanation:** A three-week queue means teams are waiting on you to do things many of them could do themselves, and the queue will grow as your reputation does. Option B reframes the problem correctly — this is a capability problem wearing the costume of a capacity problem — and does the two things that resolve it: transferring the routine checks and reserving yourself for the cases that genuinely need specialist judgement. Your role names coaching, mentoring and training precisely so that this is possible. Option A is least effective, treating a structural problem as an effort problem and guaranteeing that you remain the bottleneck permanently. Option D is a reasonable component and, without the capability transfer, simply turns people away. Option C may be justified and is a much easier ask once you can show that routine work has been devolved.

**Question 10 (harder) — Inputting into strategy**

You are asked to contribute to a business area's accessibility strategy. The draft consists of a commitment to WCAG 2.2 AA and an annual audit. What is the most effective contribution?

- A) Endorse it; those are the right commitments.
- B) Point out that an annual audit detects rather than prevents, so the strategy commits to finding defects once a year after they have shipped — and propose the additions that change the outcome: an automated check in the build, an accessibility acceptance criterion on stories, procurement requirements, and named capability development, since a strategy without a prevention mechanism produces the same defects annually.
- C) Suggest quarterly audits.
- D) Suggest adding a training commitment.

**Correct answer: B. Least effective: A**

**Explanation:** The draft is not wrong, it is incomplete in a specific and consequential way: everything in it operates after the fact. An annual audit tells you what shipped inaccessibly twelve months ago, which is useful for reporting and useless for prevention, and a strategy consisting of a standard and an audit will produce the same defect profile every year. Option B names that and proposes mechanisms at the points where defects are created rather than discovered — the build, the definition of done, procurement and capability. Option A endorses a strategy that will not change anything. Option C increases detection frequency without touching creation, and quadruples your own workload. Option D is a real addition and, on the evidence of most training programmes, insufficient alone.

**Question 11 (harder) — A difficult discussion with a senior stakeholder**

A director dismisses an audit finding as "gold-plating" and says the service is good enough. What is the most effective response?

- A) Restate the finding and the criterion.
- B) Establish what "good enough" is being measured against — if the concern is proportionality on minor findings, that is a conversation you can have and may partly agree with; if it is dismissal of blockers, name the specific barrier, who it affects and the statutory exposure, and ask for the decision to be recorded.
- C) Escalate to the head of accessibility.
- D) Accept the judgement; it is theirs to make.

**Correct answer: B. Least effective: D**

**Explanation:** "Gold-plating" is a word that covers two very different objections, and the response depends entirely on which is meant. If the director is objecting to twenty-eight minor findings being presented as equally urgent, they may have a point and conceding it costs you nothing while establishing that you distinguish severity. If they are dismissing blockers, that is a different conversation requiring specifics, population and statutory exposure — and a recorded decision, because an unrecorded dismissal leaves the organisation exposed and leaves you having flagged something nobody can find later. Option B establishes which. Option D is least effective: the decision is theirs to make, and making it without the information is not the same thing, and accepting silently means the risk is neither owned nor documented. Option A repeats a finding already dismissed. Option C escalates before establishing the disagreement.

**Question 12 (harder) — A colleague's practice concerns you**

A specialist in another team routinely reports issues as failures that you judge to be usability problems rather than conformance failures. Teams have started disputing accessibility findings generally. What is the most effective response?

- A) Correct the specific reports.
- B) Speak to them directly and privately about the pattern, using two or three specific examples, and explain the consequence you are both experiencing — that conflating usability findings with conformance failures gives teams grounds to dispute everything, including the genuine failures — then agree how to report usability issues in a way that keeps them visible without miscategorising them.
- C) Raise it with their manager.
- D) Raise it at the accessibility community.

**Correct answer: B. Least effective: D**

**Explanation:** The problem is real and its consequence is shared, which is what makes the direct conversation the right route and gives it something to be about beyond correctness. Option B uses specific examples, which makes the pattern discussable rather than a characterisation, and names the consequence you are both experiencing — teams disputing findings generally — which is a far better basis for agreement than being told you are wrong. The final clause matters too: usability findings are valuable and should be reported, just not as conformance failures, so the answer is a reporting convention rather than suppression. Option D is least effective, raising a colleague's practice in a public forum before speaking to them, which will be experienced as an attack and will harden the position. Option C escalates before the direct route. Option A corrects instances and leaves the pattern.

### Preparation tips

- **Be accurate before you are forceful.** Over-application is the specific way accessibility specialists lose standing.
- **Concede the correct half of an objection immediately.** It costs nothing and wins the rest.
- **Describe consequences, not criteria.** "A keyboard user cannot leave the dialogue" lands where "fails 2.1.2" does not.
- **Lead with arithmetic against arguments from rarity.**
- **Advise with a route, not a verdict.** Specialists who only say no are consulted late.
- **Check whether reverting to a standard component fixes it.** It frequently does, and nobody thinks of it under pressure.
- **Ask for decisions to be recorded.** An unrecorded dismissal is a risk nobody owns.
- **Treat a growing review queue as a capability problem.**

### Common pitfalls to avoid

- **Reporting an over-application as a failure.**
- **Restating a finding that has been shown to be inaccurately worded.**
- **Using an accessibility statement to authorise launching with a blocker.**
- **Asserting a criterion where the facts have not been established.**
- **Accepting an unscoped conformance claim as assurance.**
- **Arguing against conformance when nobody has proposed breaching it.**
- **Repeating training that has not changed behaviour.**
- **Conflating usability findings with conformance failures.** It gives teams grounds to dispute everything.

## Conclusion

You have reached the end, and it is worth pausing over what that involved: forty-eight questions across four assessment types, with the reasoning worked through on each. That is a substantial piece of professional preparation and rather more than most people do.

Look back at the ground. In the cognitive section you distinguished a failure from an over-application, separated severity from compliance, ranked a remediation plan by consequence rather than count, wrote a finding with location, fault, impact and remedy, and traced three recurring defects to a tooling gap rather than six training needs. In the numeric section you read thresholds at their boundaries, converted a prevalence figure into 37,500 people a year, reported a small base as a count rather than a percentage, asked whether fourteen instances sat in six templates, and rejected "94% conformant" as a category error. In the verbal section you attached a date qualifier to the right clause, treated a conditional exemption as conditional, noticed that a substantial revision ends an exemption, and declined to mark True on a claim that would have supported more resource for your own function. And in the situational judgement section you conceded a developer's correct point and corrected your own finding, described a keyboard trap by its consequence, required a conformance claim's scope in a contract, and treated a three-week review queue as a capability problem.

Two threads run through all of it, and they are in productive tension. The first is that your findings carry statutory weight, which makes precision non-negotiable — being scrupulously right at the boundary is what makes teams act on your reports rather than check them. The second is that precision is not the point; people using services is. A specialist who is technically impeccable and consulted late has less effect than one who is equally precise and consulted early, and the difference is almost always whether they bring routes rather than verdicts.

A word about your level. Working across teams at a range of capabilities means most of your effect is indirect, and the temptation is to do more yourself — more audits, more reviews, more findings. That path ends in a three-week queue and an organisation whose accessibility depends entirely on your availability. Your role names coaching, mentoring and training for a reason: the teams that catch their own defects are worth more than any audit you will ever write.

If you want to build on this, a few things repay effort more than rereading. Sit with somebody using a screen reader for an hour on a service you have audited, and notice how much of their difficulty your report did not capture. Take an audit you wrote six months ago and check whether the findings were acted on, and if not, why not. Ask a developer what would have to be true for an accessibility check to run automatically in their pipeline. Read one exemption in the regulations properly, all the way through, including the conditions. And practise writing findings with all four parts until the shorter version stops feeling adequate.

Finally, for the day itself. An assessment samples your reasoning on one morning under artificial conditions. It is not a verdict on your judgement or your career. Read the stem twice, read thresholds at the boundary, trust Cannot Say, describe consequences rather than criteria, and remember that the strongest answer is usually the one that is precisely right and offers a way forward.

Good luck. Go carefully, be exact, and keep bringing the route as well as the finding.
