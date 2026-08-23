# Graphic Designer - Psychometric Assessment Resources

## Introduction

Welcome. This guide is written for you as a graphic designer in the UK Government Digital and Data profession — a confident, competent designer who develops designs based on evidence of user needs and organisational outcomes. Your role description says you are trusted to make good decisions, recognise when to ask for further guidance, contribute to the development of design concepts, and interpret evidence-based research and incorporate it into your work. It also defines the discipline functionally: you create the graphic elements underpinning interaction and service design, using layout, spacing, colour, type and iconography to ensure content is legible and readable and that users see and understand interactions.

That functional definition is worth holding on to, because it is what makes this a role with an evidence base rather than a matter of taste. A type size, a contrast ratio, a spacing value or an icon either lets somebody complete a task or prevents them, and the difference is measurable. A good deal of what these assessments test is whether you reason that way under pressure.

You may be preparing for a formal assessment as part of a recruitment or promotion process, or you may simply want to sharpen the reasoning your job depends on. Either way, psychometric assessment at this level is not an intelligence test and not a knowledge quiz. It is a standardised sample of the thinking a role demands, and for a competent practitioner that thinking has a particular character: you are rarely choosing between a right answer and a wrong one, and usually choosing between defensible options under incomplete information, competing constraints and real consequences.

Three features of your role shape the questions. First, you are trusted to make good decisions, so the assessment will not reward escalating everything and will reward knowing which decisions belong to someone else. Second, you design strategically: your role names identifying risks and using design to mitigate them, identifying opportunities, and contributing to design patterns and components. Third, you plan and run design sessions and give and receive constructive feedback — so several items concern getting good thinking out of a room, which is unusually hard in a visual discipline where everybody has an opinion.

The document has four main sections: a cognitive assessment, a numeric reasoning assessment, a verbal reasoning assessment, and a situational judgement assessment. Each provides an overview, a mapping to your named skills, twelve practice questions with full explanations, preparation tips, and common pitfalls.

Commit to an answer before reading each explanation. The explanations spend most of their words on why the near-miss options fail.

Let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive assessment measures the reasoning your role genuinely uses, presented through practical materials rather than abstract puzzles. At your level the materials get messier and the reasoning less mechanical. You will meet evidence supporting two readings, constraints that turn out to be negotiable and others that do not, and prioritisation problems with no dominant option.

The format is usually an online test of fifteen to thirty minutes covering pattern recognition, logical deduction, error checking, prioritisation and applied problem solving. Scoring is objective against a norm group at a comparable level. Many platforms are adaptive, so a test that feels hard is usually one you are doing well on, and acuity reports distinguishing speed from accuracy reward precision.

Two things distinguish this section at your level.

The first is that you are expected to reason about risk and opportunity rather than only about problems. Your role names identifying potential risks and using design to mitigate them, identifying opportunities and using design to exploit them, and contributing to patterns and components. Pattern-level decisions carry a multiplier: a colour token, a type scale or a component style is a decision made once and paid for everywhere, and its accessibility characteristics propagate to every place it is used.

The second is comfort with irreducible uncertainty. Several questions have no clean answer, only a best one, and the discriminating factor is whether you can identify the strongest reading of ambiguous evidence and state its limits.

You need to memorise nothing — every value you need appears in the question.

### How this assessment maps to your role

The cognitive dimensions map onto the skills named in your role summary:

- **Pattern recognition** maps to **Evidence-based design**, where you analyse, synthesise and clearly explain evidence relevant to users or a service.
- **Logical deduction** maps to **Design communication**, where you clearly explain design decisions using appropriate tools and methods.
- **Error checking** maps to **Designing for everyone**, where you ensure a design meets appropriate standards such as accessibility regulations.
- **Prioritisation and risk reasoning** map to **Designing strategically**, where you identify risks and opportunities and contribute to patterns and components.
- **Applied problem solving** maps to **Iterative design**, where you prototype at different fidelities and iterate patterns and components.
- **Reasoning about positions** maps to **Designing together**, where you identify and engage the right people throughout the design process.

### Practice questions

**Question 1 (easy) — Auditing against a standard**

Your standard requires every interface component to: meet 4.5:1 contrast for text under 24 pixels, have a visible focus indicator at 3:1, have touch targets of at least 24 by 24 pixels, use spacing from the system scale, and never convey meaning by colour alone. A component has 14-pixel text at 5.2:1, a focus indicator at 2.4:1, 44-pixel targets, spacing values of 12 and 20 pixels against a scale of multiples of 8, and distinguishes states by colour and icon. How many requirements are unmet?

- A) 1
- B) 2
- C) 3
- D) 4

**Correct answer: B**

**Explanation:** Work through all five. Text at 5.2:1 exceeds 4.5:1 — met. The focus indicator at 2.4:1 falls below 3:1 — unmet. Targets of 44 pixels exceed 24 — met. Spacing of 12 and 20 are not multiples of 8 — unmet, and note this counts as one failed requirement rather than two failed values. States distinguished by colour *and* icon means colour is not the sole carrier — met. Two unmet, giving B. Option C typically comes from counting the two off-scale spacing values separately, which is the standard confusion between counting values and counting requirements. Note also which requirement failed and how easy it is to miss: focus indicators are the least-inspected part of most components because they only appear when somebody uses a keyboard, and a 2.4:1 indicator is invisible to a designer reviewing with a mouse.

**Question 2 (easy) — Deduction from a governance rule**

Your standard states: "A custom colour value may be used only if no system token is suitable, unless the value has been approved by the lead graphic designer." A developer says: "We shipped a custom colour last sprint, and there is a suitable token." Which must be true?

- A) The standard was breached.
- B) The value was approved by the lead.
- C) Either the value was approved by the lead, or the standard was breached.
- D) The custom colour fails contrast.

**Correct answer: C**

**Explanation:** A conditional with a stated exception, plus facts silent on the exception, licenses only the disjunction. Options A and B each assume a branch. Option D imports a claim nothing supports — a custom value may be perfectly compliant, and sometimes is approved precisely because it solves a contrast problem the token does not. Only C holds. Note the "only if" construction, which makes the approval the sole route rather than one exception among several, so there are exactly two branches. As someone trusted to make good decisions, your opening move is to establish which route was taken — and framing it as an enquiry means you will not have to withdraw anything if the lead approved it.

**Question 3 (moderate) — Competing explanations**

A page's task completion is 88% on screens wider than 768 pixels and 54% on screens narrower than 400 pixels. A product manager proposes a mobile redesign. What is the most rigorous analysis?

- A) Agree; the mobile layout is failing.
- B) The gap is real and large, and narrow-screen users differ in more than screen size — connection speed, whether they are away from home, whether they have documents to hand — so before committing to a redesign the cheap step is to open the page at 375 pixels and at 400% zoom, which takes ten minutes and distinguishes a layout failure from a context effect.
- C) A 34 point gap can only be explained by the layout.
- D) Narrow screens should be unsupported.

**Correct answer: B**

**Explanation:** Screen width correlates with a good deal besides screen width, and treating the gap as self-explanatory risks a redesign that fixes nothing. Option B holds the finding seriously — the gap is real and large — while naming the confounds and, crucially, identifying the cheapest way to distinguish them. That last part is what makes it a graphic designer's answer rather than a generic sceptical one: unlike most confound questions, this one has a ten-minute empirical test available on your own machine. If a table forces horizontal scrolling at 375 pixels, or the primary action sits below the fold, you have your answer and can stop reasoning. Option A commits to a redesign on an unexamined correlation. Option C mistakes effect size for causal certainty. Option D would exclude the users already struggling most.

**Question 4 (moderate) — Prioritising by what can change**

You have capacity for one substantial piece of work this quarter:

1. A colour and type token set for a new service is being fixed next month and will be inherited by five services.
2. A live page has a known contrast failure on a secondary label.
3. A team wants exploratory visual concepts for next year.
4. The team wants to revisit a layout you produced six weeks ago after minor copy changes.

Which is strongest, and why?

- A) Item 2, because it affects users now.
- B) Item 1, because the decisions are imminent, will be inherited by five services, and a token set embeds its accessibility characteristics everywhere it is used — making it far harder to change later than to get right now.
- C) Item 3, because early work has the highest leverage.
- D) Item 4, because unverified changes are a risk.

**Correct answer: B**

**Explanation:** The right frame is what your input can still change and whether there is time, and item 1 carries a multiplier the others lack. A token set inherited by five services propagates every property it has — good and bad — and changing a colour token after adoption means coordinating five teams and revisiting every place the token appears, whereas setting it correctly costs nothing extra now. Item 2 matters and is a single label with a known fix that somebody can make in an hour, which is exactly why it does not need a quarter of your capacity. Item 3 has no deadline pressure. Item 4 is weakest. Option A ranks by immediacy and confuses urgency with the size of the work required.

**Question 5 (moderate) — Risk reasoning about a token**

A team proposes a new grey for secondary text, measuring 4.6:1 against white. It will be added to the token set. What is the most complete risk analysis?

- A) It passes 4.5:1, so it is fine.
- B) It passes against white by a margin of 0.1, which means it will fail against any of the tinted panel backgrounds already in the system, and tokens get used wherever they look right — so the real question is what backgrounds it will sit on, and a value with almost no headroom is a defect waiting to be discovered on a page nobody has audited.
- C) It should be darker.
- D) Secondary text should not exist.

**Correct answer: B**

**Explanation:** The strongest analysis names the mechanism rather than the measurement. A ratio of 4.6:1 passes against white and passes by almost nothing, and the moment that grey is placed on a light grey panel — which token sets invariably contain and designers invariably use — the effective ratio drops below the threshold. Because a token is available everywhere, nobody re-measures it in context; that is the entire convenience of tokens and also their risk. Option B identifies that and reframes the decision around the backgrounds the token will meet. Option C reaches the right conclusion without the reasoning, which means it cannot be defended when somebody asks why 4.6 is not enough. Option A treats a threshold as the whole question. Option D is disproportionate. Building headroom into a token is the practical lesson: values chosen at the boundary fail as soon as context changes.

**Question 6 (moderate) — Strength of a finding**

Nine of twelve participants failed to notice a secondary action. Which conclusion is best supported?

- A) 75% of users do not notice it.
- B) Its visual treatment is not signalling that it is available, evidenced across most participants, warranting a change to its prominence or position and a follow-up check on whether the change helps.
- C) It should be made a primary button.
- D) The page is badly designed.

**Correct answer: B**

**Explanation:** Nine of twelve is a strong qualitative signal, and B states it at that strength while naming the mechanism the evidence points at. Option A converts twelve participants into a population rate, the commonest overreach in design reporting. Option C jumps to one solution, and it is the wrong one for a specific reason worth knowing: making a secondary action look primary does not solve a discoverability problem, it creates a competing call to action, and the usual result is that both actions get weaker. The solution space is wider — position, spacing, giving it a heading, or asking whether the action needs to be on this page at all. Option D is unhelpful to whoever must act. Note that B includes the follow-up check, which is what turns a change into an improvement.

**Question 7 (moderate) — Designing under a constraint**

A communications team requires the brand's primary colour, which measures 3.4:1 against white, to be used for interface text. What is the strongest approach?

- A) Use it; the brand takes precedence.
- B) Establish what the brand requirement actually protects — recognisability — then propose using the primary at full strength where 3:1 applies, such as large headings and non-text elements, with a darker variant of the same hue for body text, so the palette reads as the brand while every element meets its threshold.
- C) Refuse and use black.
- D) Increase all text to 24 pixels so 3:1 applies.

**Correct answer: B**

**Explanation:** The strongest approach separates the brand's purpose from the specific instruction and finds a route satisfying both. Brands are recognisable through a palette, a typeface, a tone and a set of proportions, not through one value appearing in body text — and most brand palettes already contain a darker variant of the primary, precisely because the primary is optimised for impact rather than for reading. Option B proposes that and also identifies where the primary can appear at full strength, which is the concession that makes the argument acceptable rather than adversarial. Option A publishes text some people cannot read. Option C discards the brand unnecessarily and will be refused. Option D is the sophisticated-looking trap: enlarging all text to escape a threshold games the criterion rather than meeting its purpose, and produces a page that scans badly for everyone.

**Question 8 (harder) — Scoping a flaw**

A study you are relying on ran on a single high-quality external monitor at full brightness. Four findings: (i) participants could not find a secondary action; (ii) participants read the body text comfortably; (iii) participants misinterpreted an icon; (iv) participants found the colour-coded status labels easy to distinguish. Which findings are most compromised?

- A) All four.
- B) None; display conditions do not matter.
- C) Findings (ii) and (iv) are most compromised, because a bright high-quality display flatters legibility and colour discrimination in ways a phone in daylight or an older office monitor will not — while (i) and (iii) concern position and comprehension, which the display affects far less.
- D) Only (iv).

**Correct answer: C**

**Explanation:** The skill is scoping precisely rather than treating a condition as invalidating everything or nothing. A bright, high-quality display makes low-contrast text look fine and makes similar colours look distinct — which is exactly what findings (ii) and (iv) claim. Those same colours on a dimmed laptop, a cheap monitor with a blue cast, or a phone screen in sunlight may be indistinguishable. Findings (i) and (iii) concern where something is and what an icon means, which display quality barely touches. Option C says this. Option A discards two sound findings. Option B is wrong on the facts, and it is worth naming why this matters for graphic designers specifically: display conditions are the sampling frame problem of visual disciplines, and testing on the best screen in the building is the equivalent of recruiting only confident users.

**Question 9 (harder) — Spotting the opportunity**

Analytics show that a page's error rate on one field is 4%, but that 78% of users who make the error correct it successfully on the second attempt. The team treats the high recovery rate as evidence the page is fine. What is the strongest observation?

- A) Agree; users recover.
- B) A 78% recovery rate means 22% do not — and more usefully, everyone who makes the error pays a cost in time and confidence even when they recover, while the error itself is telling you the field's label, format hint or input type is producing a predictable mistake that could be prevented rather than recovered from.
- C) The error rate is acceptable.
- D) The error message should be improved.

**Correct answer: B**

**Explanation:** This is opportunity reasoning. The team has read a recovery rate as a success because it mostly ends well, and missed two things. The 22% who do not recover are the tail, and at 4% of a large user base that is a substantial number of people who abandon at a field. More importantly, a predictable error is a design problem rather than a user problem: if 4% of people enter a date in a format the field rejects, the field is asking for something people do not naturally supply, and the fix is upstream of the error message. Option B says both. Option D is a real improvement and treats the recovery rather than the cause, which is the second-best answer and the one most teams reach for. Options A and C accept the framing.

**Question 10 (harder) — Two things moving apart**

After a redesign that increased body text from 16 to 19 pixels, time on page rose 20% and completion was unchanged. A colleague concludes the larger text slowed people down. What is the strongest analysis?

- A) Agree; larger text means more scrolling.
- B) Time on page is an ambiguous measure — it rises both when people struggle and when they read more of the content — so unchanged completion with longer dwell is as consistent with users now reading text they previously skipped as with them being slowed down, and the way to distinguish them is whether errors or contact volume moved.
- C) The text should be reverted to 16 pixels.
- D) The redesign failed.

**Correct answer: B**

**Explanation:** Time on page is one of the most misused metrics in interface work, because it has no direction: a page people cannot read produces long dwell times, and so does a page people can finally read and are therefore reading. Unchanged completion tells you the outcome did not worsen, which rules out the most alarming interpretation. Option B names the ambiguity and identifies what would resolve it — errors and contact volume, both of which are directional in a way dwell time is not. If errors fell while dwell rose, people are reading; if errors held while dwell rose, something else is happening. Option A adopts one interpretation without evidence. Option C reverts a change on an ambiguous measure, which risks undoing an improvement. Option D declares failure on a metric that cannot support it.

**Question 11 (harder) — A constraint that may not be one**

A developer says a component's touch targets cannot be enlarged "because of the layout". Research shows users are mis-tapping. What is the most productive line of enquiry?

- A) Accept it and make the icons smaller so they fit.
- B) Ask what specifically constrains the size — the visible control, the space between controls, or a container height — and raise the option that resolves most cases: extending the interactive area invisibly beyond the visible graphic, since a touch target does not have to match the size of what is drawn.
- C) Insist the layout changes.
- D) Add spacing between the controls only.

**Correct answer: B**

**Explanation:** "Because of the layout" is a compressed claim that could mean several things, and the productive move is to establish which. Option B does that and names the mechanism resolving most instances, which is genuinely useful knowledge to bring to a developer conversation: the interactive area of a control can extend beyond its visible bounds, so a 16-pixel icon can carry a 44-pixel target without changing the layout at all. Option A makes the visible element smaller to fit a constraint, worsening the original problem. Option C asserts without understanding, and a designer who treats every constraint as negotiable is not believed about the ones that are. Option D is a partial and sometimes sufficient fix — separating targets reduces mis-taps even when they stay small — and it does not address the size requirement itself, so it is second-best.

**Question 12 (harder) — A flaw in your own work**

Three weeks after you defined a token set now used in two services, you realise the secondary text token measures 4.4:1 rather than the 4.6:1 you recorded. What should you do?

- A) Note it for the next token review.
- B) Tell the teams and your lead now, state the measured value and where the token is used, correct it, and check whether any other tokens were measured against the wrong background — since the error suggests a method problem rather than a one-off slip.
- C) Correct the token quietly.
- D) Leave it; 4.4 is close.

**Correct answer: B**

**Explanation:** A token used in two services means the error is live in both, and 4.4:1 is a failure rather than a near miss — thresholds have no discretionary zone below them. Option B does the four things that matter: tells the people affected, states the measured value rather than describing the problem vaguely, corrects it, and asks the diagnostic question that distinguishes a lead-worthy response from a fix. A mis-measured token usually means the value was checked against the wrong background or with the wrong tool, and if so, other tokens defined in the same session are suspect. Option D is least defensible: "close" applied once to a threshold becomes the standard for every future judgement. Option C corrects the value and leaves both the published work and the method unexamined. Option A defers a live failure.

### Preparation tips

- **Count requirements, not values.** Two off-scale spacing values are one failed requirement.
- **Check the least-inspected properties.** Focus indicators only appear under keyboard use and are almost never reviewed.
- **Ask what background a value will meet.** A ratio with no headroom fails as soon as context changes.
- **Use the ten-minute empirical test.** Opening a page at 375 pixels and 400% zoom settles more arguments than reasoning does.
- **Weight decisions by reuse.** A token inherited by five services is worth five times the attention.
- **Ask what a constraint actually is.** "Because of the layout" has several meanings, and one of them has an easy fix.
- **Treat a predictable error as a design problem.** Recovery rates measure the cost, not the cause.
- **Distrust directionless metrics.** Time on page rises for opposite reasons.

### Common pitfalls to avoid

- **Converting participants into percentages.**
- **Treating a threshold as having a discretionary zone.** 4.4 is a fail.
- **Choosing values at the boundary.** Build headroom into anything reusable.
- **Testing on the best screen in the building.** It is the display equivalent of recruiting confident users.
- **Making a secondary action look primary to fix discoverability.** You get two weak calls to action.
- **Gaming a criterion rather than meeting its purpose.**
- **Reverting a change on an ambiguous measure.**
- **Prescribing the fix instead of naming the problem.** The solution space is usually wider than it looks.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A numeric reasoning assessment measures how accurately you handle the quantitative material your role produces and consumes. Graphic designers sometimes expect this to be the section furthest from their work, and it is not: the discipline is unusually full of values with thresholds attached. Contrast ratios, type scales, line lengths, spacing units, grid arithmetic, target sizes, viewport widths — almost every decision you make has a number, and a great many of them can be passed or failed rather than merely preferred.

At your level the emphasis shifts from calculating to interrogating. You will still need to compute correctly, but the harder items ask whether a figure means what somebody claims. That is a professionally consequential skill for you specifically, because visual decisions are the ones colleagues feel most entitled to have opinions about, and a measured value is the only thing that reliably converts a matter of taste into a matter of fact.

The format is typically a timed online test of fifteen to thirty minutes, each item presenting a table, chart or paragraph of figures with a multiple-choice question. Calculators are usually provided and the arithmetic is deliberately tractable.

Four habits carry the load. Establish what the question asks before looking at the data. Identify the denominator and the population it represents. Estimate, calculate, compare. And sanity-check against the world.

Distractors are built from a predictable catalogue: wrong denominator, percentage confused with percentage point, new value used as the base in a percentage change, off-by-one errors in grid arithmetic, and thresholds read as approximate.

### How this assessment maps to your role

The numerical skills tested map onto your named skills:

- **Working with ratios and thresholds** maps to **Designing for everyone**, where meeting a standard is a numerical question with a definite answer.
- **Reading analytics accurately** maps to **Evidence-based design**, where you analyse and clearly explain evidence relevant to users.
- **Comparing groups fairly** maps to **Designing for everyone**, where a gap between groups is the first numerical trace of exclusion.
- **Grid and scale arithmetic** maps to **Designing strategically**, where the value of patterns and components rests on internal consistency.
- **Quantifying impact** maps to **Design communication**, where a measured consequence is the most persuasive form a design argument takes.
- **Detecting misleading metrics** maps to **Evidence-based design**, where a wrong measure sends design effort to the wrong place.

### Practice questions

**Question 1 (easy) — Completion rate**

Of 4,800 users who reached a page, 3,600 completed it. What percentage?

- A) 70%
- B) 75%
- C) 80%
- D) 85%

**Correct answer: B**

**Explanation:** 3,600 ÷ 4,800 = 0.75, so 75%, and the answer is B. Estimate first: 3,600 of 4,800 is three quarters, since 2,400 would be half. Options A and C come from dividing by 5,143 and 4,500. The three-second estimate before every calculation is the cheapest error insurance available under a clock, and it costs nothing.

**Question 2 (easy) — Thresholds at the boundary**

A standard requires 4.5:1 for text under 24 pixels and 3:1 for text 24 pixels or larger. Four cases: 14px at 4.4:1; 16px at 4.5:1; 24px at 2.9:1; 30px at 3.0:1. How many meet the standard?

- A) 1
- B) 2
- C) 3
- D) 4

**Correct answer: B**

**Explanation:** Check each against the right threshold. 14px is under 24, so needs 4.5:1 — 4.4 fails. 16px is under 24, needs 4.5:1 — 4.5 meets it exactly, and "at least" includes the boundary, so it passes. 24px is "24 or larger", so needs 3:1 — 2.9 fails. 30px needs 3:1 — 3.0 meets it exactly, so it passes. Two pass, giving B. Three boundary readings decide this item: 4.4 fails though it rounds to 4, 4.5 passes because "at least" is inclusive, and 24px falls into the *larger* category because the wording is "24 or larger" rather than "over 24". Each of those is a real distinction that contrast checkers and standards handle precisely, and reading them loosely produces both false failures and false passes.

**Question 3 (easy) — Grid arithmetic**

A 12-column grid spans 1,152 pixels with 32-pixel gutters between columns and no outer margin. What is one column's width?

- A) 64 pixels
- B) 67 pixels
- C) 96 pixels
- D) 100 pixels

**Correct answer: B**

**Explanation:** Twelve columns have eleven gutters between them, not twelve, because gutters sit between columns rather than after each one. The gutters take 11 × 32 = 352 pixels, leaving 1,152 − 352 = 800 pixels for the columns, and 800 ÷ 12 = 66.67, which rounds to 67. So B. Option A follows from assuming twelve gutters: 1,152 − 384 = 768, and 768 ÷ 12 = 64 — a suspiciously round number, which is part of why the error survives, since 64 looks more like a designed value than 66.67 does. Option C is 1,152 ÷ 12, ignoring gutters altogether, the commonest error of all. The off-by-one is worth fixing permanently: for n columns there are n − 1 internal gutters, and getting it wrong in a system definition produces numbers that never quite reconcile and that nobody can later explain.

**Question 4 (easy) — Line length**

A column is 720 pixels wide with 18-pixel type at an average character width of 9 pixels. How many characters fit on a line, and what does that suggest?

- A) 80 characters, comfortably within the usual range
- B) 80 characters, at or slightly above the upper end of the comfortable range for continuous reading
- C) 40 characters, uncomfortably short
- D) 60 characters, ideal

**Correct answer: B**

**Explanation:** 720 ÷ 9 = 80 characters. Comfortable measure for continuous reading is widely held to sit between about 45 and 75 characters, so 80 is at or just beyond the upper edge — making B correct and A wrong on the interpretation rather than the arithmetic. The distinction matters because the arithmetic alone does not produce a judgement; you need the range to know what 80 means. The two remedies are worth holding together: narrowing the measure, or increasing type size, since larger type at a fixed width reduces characters per line. Being able to do that calculation in your head is what lets you say something specific in a critique rather than that a column feels wide.

**Question 5 (moderate) — Comparing groups fairly**

Of 900 users on wide screens, 810 completed a task. Of 600 users on narrow screens, 300 completed. What is the gap in percentage points?

- A) 30
- B) 40
- C) 50
- D) 90

**Correct answer: B**

**Explanation:** Wide: 810 ÷ 900 = 90%. Narrow: 300 ÷ 600 = 50%. The gap is 90 − 50 = 40 percentage points, giving B. Options C and D are the narrow group's rate and the wide group's rate offered as if they were the gap — a distractor pattern worth recognising, since numbers from your working frequently appear among the options. A 40 point gap is enormous, and for a graphic designer the suspects are specific and checkable in ten minutes: text reflowing into unreadable line lengths, targets too close together, a fixed-width element forcing horizontal scrolling, or the primary action pushed below the fold at that width.

**Question 6 (moderate) — Percentage change**

After a type size increase, weekly completions rose from 640 to 800. What is the percentage increase?

- A) 20%
- B) 25%
- C) 80%
- D) 125%

**Correct answer: B**

**Explanation:** The difference is 160, and 160 ÷ 640 = 0.25, a 25% increase, giving B. Option A is 160 ÷ 800, dividing by the new figure — the most common error in this question type and one that under-reports every improvement you make, which matters when you are demonstrating that a change worked. Option D expresses the new figure as a proportion of the old, a true statement answering a different question. The rule: for percentage change, the denominator is always where you started.

**Question 7 (moderate) — Quantifying impact**

A service handles 800,000 sessions a year. An unreadable error message affects the 6% of sessions in which the error occurs. How many people a year are affected?

- A) 4,800
- B) 48,000
- C) 80,000
- D) 480,000

**Correct answer: B**

**Explanation:** 6% of 800,000 is 0.06 × 800,000 = 48,000, giving B. Option A is 6% of 80,000; option D is 60%. The reason this belongs in a design guide is what it does to a conversation: "the error message contrast is a bit low" is a matter of taste to whoever hears it, and "48,000 people a year hit an error message they may not be able to read" is not. Converting a defect into people takes ten seconds and is the single most effective move available to a designer arguing for a change nobody thinks is worth the effort — and it works precisely because visual arguments are otherwise so easy to discount.

**Question 8 (moderate) — Working back to a base**

A report says 12% of users abandon at a step, and that this is 3,600 people a month. How many reach the step?

- A) 4,032
- B) 15,000
- C) 30,000
- D) 43,200

**Correct answer: C**

**Explanation:** If 12% equals 3,600, the total is 3,600 ÷ 0.12 = 30,000, giving C. Stepwise: 12% is 3,600, so 1% is 300, and 100% is 30,000. Verify by reversing — 12% of 30,000 is 3,600. Option A adds 12%; option D is 3,600 × 12. This matters because colleagues quote percentages far more readily than bases, and 12% of 30,000 is a different problem from 12% of 300. Establishing the base in ten seconds lets you judge whether a figure deserves the weight it is being given.

**Question 9 (moderate) — Choosing the denominator**

A journey shows 40,000 start, 32,000 reach a form, 24,000 reach review, 22,800 submit. What proportion of those who reached review submitted?

- A) 57%
- B) 60%
- C) 71%
- D) 95%

**Correct answer: D**

**Explanation:** The stem names users who reached review, so the denominator is 24,000 and the part is 22,800: 22,800 ÷ 24,000 = 0.95, giving D. Option A uses 40,000, answering a whole-journey question nobody asked. This determines where design effort goes: 95% of those reaching review submit, so review is not the problem. The losses are 8,000 between start and form and 8,000 between form and review, which is where a legibility, hierarchy or target-size problem would be worth looking for.

**Question 10 (harder) — A ratio with no headroom**

A token measures 4.6:1 against white. The system contains panel backgrounds at various light tints. What is the most useful observation?

- A) It passes, so it is fine.
- B) It passes against white by 0.1 and will fail against any tinted panel, because contrast falls as the background darkens towards the text — and since tokens are used wherever they look right rather than re-measured in context, a value with no headroom becomes a defect discovered on a page nobody audited.
- C) It should be tested on each panel.
- D) Panels should be white.

**Correct answer: B**

**Explanation:** The strongest observation names the mechanism rather than the measurement. A ratio of 4.6:1 against white leaves 0.1 of margin, and any tint on the background reduces the luminance difference and therefore the ratio, so a grey passing on white will fail on a light grey panel. Because a token is available everywhere, nobody re-measures it in context — that is both the convenience of tokens and the risk. Option B identifies this and draws the practical conclusion, which is to build headroom into anything reusable. Option C is not wrong and is impractical as a standing requirement, since new panels appear faster than audits do. Option A treats the threshold as the whole question. Option D solves the problem by removing the design.

**Question 11 (harder) — Percentage points and relative change**

Completion on narrow screens rose from 50% to 62%. Which statement is accurate?

- A) A 12% increase.
- B) A 12 percentage point increase, equivalent to a 24% relative increase.
- C) A 24 percentage point increase.
- D) A 19.4% increase.

**Correct answer: B**

**Explanation:** The arithmetic gap is 62 − 50 = 12 percentage points. The relative increase is 12 ÷ 50 = 0.24, or 24%. Option B labels both correctly. Option A is ambiguous and generally read as relative. Option C misapplies the percentage-point label. Option D divides by the new value. The professional stake is real: "completion rose 24%" and "rose 12 percentage points" describe the same change, and one sounds twice as impressive. Being the person who gives both is a cheap way to be trusted with numbers — and for a designer it matters more than average, because a colleague who catches you choosing the flattering figure will treat your next visual argument as advocacy rather than evidence.

**Question 12 (harder) — A directionless metric**

After a type size increase, time on page rose 20% and completion was unchanged. A colleague concludes users were slowed down. What is the strongest analysis?

- A) Agree; longer text means more scrolling.
- B) Time on page has no direction — it rises both when people struggle and when they read more of the content — so unchanged completion with longer dwell is as consistent with people now reading text they previously skipped as with being slowed, and the way to distinguish them is whether errors or contact volume moved.
- C) Revert the change.
- D) The change failed.

**Correct answer: B**

**Explanation:** Time on page is among the most misused metrics in interface work precisely because it has no direction: a page people cannot read produces long dwell, and so does a page people can finally read and are therefore reading. Unchanged completion rules out the most alarming interpretation. Option B names the ambiguity and identifies what would resolve it — errors and contact volume, both of which are directional. If errors fell while dwell rose, people are reading; if errors held, something else is happening. Option A adopts one interpretation without evidence. Option C reverts on an ambiguous measure, risking the undoing of a genuine improvement, which is a specific hazard for legibility changes because their benefits show up in comprehension rather than speed. Option D declares failure on a metric that cannot support it.

### Preparation tips

- **Read thresholds at the boundary.** "At least 4.5:1" means 4.4 fails; "24 or larger" includes 24.
- **Remember n − 1 gutters for n columns.**
- **Pair an arithmetic result with the range that gives it meaning.** 80 characters is only informative if you know the comfortable range.
- **Find the denominator first.**
- **Convert defects into people.** It is the move that makes a visual argument land.
- **Build headroom into reusable values.** Anything at the boundary fails when context changes.
- **Distrust directionless metrics.** Time on page rises for opposite reasons.
- **Give both framings.** Percentage points and relative change, every time.

### Common pitfalls to avoid

- **Rounding a contrast ratio in your head.**
- **Ignoring gutters, or counting one too many.**
- **Dividing by the wrong total.**
- **Confusing percentages with percentage points.**
- **Choosing token values at the threshold.**
- **Reverting a change on an ambiguous measure.**
- **Reporting a number from your working as though it answered the question.**
- **Assuming a visual discipline is a non-numerical one.**

## Workplace job-specific verbal reasoning assessment

### About this assessment

A verbal reasoning assessment measures how accurately you read. It may feel further from your daily work than the other sections, and it is not: the documents constraining graphic design in government are unusually precise. Accessibility criteria specify ratios and thresholds. Brand guidelines specify permitted and prohibited uses. Design system documentation specifies when a component may and may not be used. Reading any of those slightly wrong produces either a design that fails an audit or a fight you did not need to have — and in this discipline the second is as costly as the first, because credibility spent on an unnecessary argument is not available for a necessary one.

The classic format presents a short passage of dense workplace prose, typically three to six sentences, followed by statements to classify as True, False or Cannot Say. True means the statement follows necessarily. False means the passage contradicts it. Cannot Say means the passage neither establishes nor excludes it. Alongside these come comprehension items, main-point items, and questions asking which of four summaries is most accurate.

The governing rule is that you answer from the passage alone. Your professional knowledge must be set aside — and this becomes harder with experience, because the more accessibility criteria you have applied, the more readily you supply the clause you expect.

Cannot Say deserves particular attention. It feels evasive, so candidates reach for True or False to appear decisive, and in practice it is frequently correct.

Small words carry the meaning, and one matters more in your discipline than in most: "or". Accessibility criteria routinely offer alternative routes to compliance separated by "or", and reading them as conjunctions produces unnecessary work, needlessly dark palettes, and arguments with whoever chose the brand.

### How this assessment maps to your role

The verbal skills tested map onto your named skills:

- **Reading precisely** maps to **Designing for everyone**, where you ensure a design meets appropriate standards such as accessibility regulations.
- **Separating statement from inference** maps to **Evidence-based design**.
- **Identifying the main point** maps to **Design communication**, where you clearly explain problems and design ideas to others.
- **Handling qualified language** maps to **Designing strategically**, where knowing whether a pattern is mandatory or recommended tells you how much room you have.
- **Reading for absence** maps to **Designing for everyone**, where noticing a specification never states a minimum has a consequence.
- **Reading feedback accurately** maps to **Designing together**, where you give and receive constructive design feedback.

### Practice questions

*Passage A — for Questions 1 to 4*

"Text smaller than 24 pixels must have a contrast ratio of at least 4.5:1 against its background. Text 24 pixels or larger, or 19 pixels or larger and bold, must have a contrast ratio of at least 3:1. Non-text elements that convey information, including icons and the boundaries of form fields, must have a contrast ratio of at least 3:1. Logotypes are exempt."

**Question 1 (easy)** — Statement: "All text must have a contrast ratio of at least 4.5:1." True, False or Cannot Say?

**Correct answer: False**

**Explanation:** The passage sets 3:1 for large and bold text and exempts logotypes. The statement's "all" contradicts both, so False. This is the most reliable pattern in the section, and it is also the most common real misquotation — "everything needs 4.5:1" is the version most people carry, and applying it to a large heading produces a needlessly dark palette and an avoidable argument.

**Question 2 (easy)** — Statement: "The boundary of a form field must meet a contrast requirement." True, False or Cannot Say?

**Correct answer: True**

**Explanation:** The third sentence names non-text elements that convey information, "including icons and the boundaries of form fields", and requires at least 3:1. The statement follows and is True. This provision is worth knowing precisely because it is the one designers most often overlook: a very light hairline around an input looks elegant, conveys the essential information that there is a field to type in, and frequently measures well below 3:1 against the page background. The passage's explicit mention of field boundaries exists because that is exactly where the requirement gets forgotten.

**Question 3 (moderate)** — Statement: "Bold text at 20 pixels needs 4.5:1." True, False or Cannot Say?

**Correct answer: False**

**Explanation:** The second sentence sets 3:1 for text "24 pixels or larger, **or** 19 pixels or larger and bold". Bold text at 20 pixels satisfies the second route, since 20 is 19 or larger and it is bold, so the applicable threshold is 3:1 and the statement is contradicted. False. This is the "or" trap, and it is the most consequential misreading in applying contrast criteria. Read as "and", the clause would require text to be both 24 pixels and bold, which would make it nearly useless and push designers towards unnecessarily dark palettes. Read as written, it recognises that size and weight each improve legibility, and either qualifies.

**Question 4 (harder)** — Statement: "A decorative icon must meet 3:1." True, False or Cannot Say?

**Correct answer: Cannot Say**

**Explanation:** The third sentence requires 3:1 for non-text elements *that convey information*, and names icons as an example of those. A decorative icon by definition conveys no information, so it falls outside the stated requirement — but the passage does not say decorative elements are exempt, only where the requirement applies. Silence about the decorative case leaves it undetermined, so Cannot Say rather than False. The distinction between stating where a rule applies and stating where it does not is a fine one and it recurs constantly in standards. In practice the useful move is to ask whether the icon is genuinely decorative, because designers describe icons as decorative far more often than users treat them that way.

*Passage B — for Questions 5 to 8*

"The review found that users on screens narrower than 400 pixels completed tasks less often than users on wider screens. The review notes that these users also differed in connection speed and in whether they were using the service away from home. The review did not assess whether the layout reflowed correctly at narrow widths. It recommends that the team consider whether a narrow-width review would be worthwhile."

**Question 5 (easy)** — Statement: "Narrow-screen users completed tasks less often." True, False or Cannot Say?

**Correct answer: True**

**Explanation:** The first sentence states this directly and the statement restates it without addition. True. Note the comparative framing — "less often than users on wider screens" — which the statement respects. Answer quickly and bank the time for harder items.

**Question 6 (moderate)** — Statement: "The narrow layout causes users to fail tasks." True, False or Cannot Say?

**Correct answer: Cannot Say**

**Explanation:** The passage reports an association and names two ways the groups differed: connection speed and whether they were away from home. Either could explain the difference — someone on a slow connection away from home may be interrupted, may lack documents, or may abandon before the page renders, all independently of layout. The passage neither asserts nor excludes a layout cause, so Cannot Say. The design consequence is direct: if the layout is at fault you fix the reflow, and if the cause is context you design for interruption and slow loading, which are different pieces of work with different costs.

**Question 7 (moderate)** — Statement: "The layout reflows correctly at narrow widths." True, False or Cannot Say?

**Correct answer: Cannot Say**

**Explanation:** The passage says explicitly that reflow was not assessed. Declared silence establishes nothing, so Cannot Say. The professional temptation here runs towards False — given a 34 point completion gap you may well suspect the reflow is broken, and you may be right — and marking False would substitute expertise for evidence, which is exactly what this section penalises. Note the asymmetry with real practice: in the workplace the right response is to open the page at 375 pixels, which costs ten minutes and settles it; in the test the check is unavailable and so is the conclusion.

**Question 8 (harder)** — Statement: "The review recommends a narrow-width review." True, False or Cannot Say?

**Correct answer: False**

**Explanation:** The review recommends that the team *consider whether* a narrow-width review would be worthwhile — a recommendation to evaluate, including concluding it would not be. The statement asserts a recommendation to conduct one, which was not made, so False rather than Cannot Say: the passage tells you what was recommended and it was something different. This pervades review documents and produces the familiar sequence in which a recommendation to consider becomes a commitment on a plan that somebody then reports against.

*Passage C — for Questions 9 to 12*

"Interactive elements must have a visible focus indicator with a contrast ratio of at least 3:1 against adjacent colours. Touch targets must be at least 24 by 24 pixels, unless an equivalent target of at least 24 by 24 pixels is available elsewhere on the same screen. Meaning must not be conveyed by colour alone. Where a component is provided in the design system, services must use it unless an exemption has been agreed with the lead graphic designer."

**Question 9 (easy)** — Statement: "Meaning may be conveyed by colour alone if the contrast is high." True, False or Cannot Say?

**Correct answer: False**

**Explanation:** The passage states without qualification that meaning must not be conveyed by colour alone. The statement introduces a condition the passage does not recognise, and high contrast does not address the requirement's purpose, which concerns people who cannot distinguish the hues rather than people who cannot see them clearly. False. Being precise about that purpose matters, because "make it a stronger red" is a common and useless response — a stronger red is still only red.

**Question 10 (moderate)** — Statement: "Every touch target must be at least 24 by 24 pixels." True, False or Cannot Say?

**Correct answer: False**

**Explanation:** The requirement carries an exception: a smaller target is permitted where an equivalent target of at least 24 by 24 pixels is available elsewhere on the same screen. The statement's "every" drops that, so False. The exception exists for a practical reason: an inline link inside a paragraph cannot always be enlarged without breaking the text, and the requirement accepts that provided the same action is reachable from a properly sized control nearby. Reading the exception is what lets you keep an inline link rather than fighting to enlarge it, which is an argument you would probably lose and should not be having.

**Question 11 (harder)** — Statement: "A service using a custom component instead of a design system component has breached the requirements." True, False or Cannot Say?

**Correct answer: Cannot Say**

**Explanation:** The final sentence requires services to use the system component *unless an exemption has been agreed with the lead graphic designer*. Whether an exemption was agreed is not stated, so the case is undetermined: with an exemption the service complies, without one it does not. Cannot Say. This is the same rule-plus-exception structure as the logic items in the cognitive section, appearing here in reading form, and it rewards the same discipline — resisting the conclusion that feels obvious from the general rule when the facts are silent on the exception.

**Question 12 (harder) — Main point**

Which best captures the main point of Passage C?

- A) Services must use design system components.
- B) Interactive elements must be perceivable and operable regardless of how a user perceives colour or how precisely they can point, and services should draw on shared components unless an exemption is agreed — with visible focus, adequately sized targets or equivalents, and meaning carried in more than colour.
- C) Touch targets must be at least 24 by 24 pixels.
- D) Meaning must not be conveyed by colour alone.

**Correct answer: B**

**Explanation:** The main point must cover the whole passage without adding anything. Option A is one clause and drops its exemption. Options C and D are each true of one sentence and silent on the rest, and C also drops the equivalence exception. Option B captures all four requirements and the logic joining them: three concern making elements work for people who cannot see colour differences, cannot point precisely, or cannot see the screen, and the fourth ensures those properties are inherited rather than reinvented. Note that B preserves both the equivalence exception and the exemption, which the shorter options discard — and a summary dropping an exception is how a standard acquires a reputation for being unreasonable.

### Preparation tips

- **Answer only from the passage.** Before marking True, point at the words.
- **Read "or" as "or".** In accessibility criteria it offers alternative routes; reading it as "and" costs effort and arguments.
- **Trust Cannot Say.** Especially where you suspect the answer.
- **Notice which non-text elements are named.** Field boundaries and icons are where the 3:1 requirement gets forgotten.
- **Distinguish stating where a rule applies from stating where it does not.**
- **Keep exceptions in summaries.** A summary dropping one makes a standard look unreasonable.
- **Separate "consider whether X" from "recommend X".**
- **Practise on real criteria.** Write three statements about a requirement — one True, one False, one Cannot Say.

### Common pitfalls to avoid

- **Answering from professional knowledge.**
- **Reading "or" as "and".** The most costly misreading in your discipline.
- **Carrying "everything needs 4.5:1" in your head.**
- **Marking False because you suspect the untested result.**
- **Converting a scope statement into an exemption.**
- **Treating association as causation.**
- **Forgetting the rule-plus-exception structure.** Silence on the exception gives Cannot Say.
- **Dropping an exception when summarising.**

## Workplace job-specific situational judgement assessment

### About this assessment

A situational judgement assessment presents realistic workplace scenarios and asks what you would do. There is no passage to parse and no arithmetic. You get a dilemma of the kind your role produces, four or five candidate responses, and a question asking which is most effective and often which is least.

This section measures whether your judgement matches what the profession considers good practice at your level. Your role description places you as a confident, competent designer trusted to make good decisions, who recognises when to ask for guidance, contributes to design concepts, plans and runs design sessions, and gives and receives constructive feedback. The strongest answers involve exercising real professional judgement, holding a position under pressure when the evidence warrants it, and knowing which decisions belong to someone else.

Four principles carry most scenarios.

Users come first, and specifically the users who cannot see, read or operate something. A design that excludes one group is not slightly worse for them; it is unusable.

Bring the value, not the opinion. This is the distinctively graphic-design signature of a strong answer, and it recurs throughout this section. Visual decisions are the ones colleagues feel most entitled to have opinions about, and the most effective response is almost never "that looks wrong" but "that measures 3.1:1 and the requirement for that size is 4.5:1". A number ends an argument that taste cannot, and it converts you from someone with preferences into someone with findings.

Address problems directly, early, with the person involved. Private, specific, non-accusatory conversation beats public correction, silence, or routing around someone.

Fix the token, not the instance. At your level, noticing that one off-system colour means the token was unavailable — and doing something about that — is a marker of the seniority you are working towards.

### How this assessment maps to your role

The judgement dimensions map onto your named skills:

- **Explaining and defending design decisions** maps to **Design communication**.
- **Protecting legibility and access** maps to **Designing for everyone**, where you ensure designs meet appropriate standards and work for all users.
- **Running sessions and engaging the right people** maps to **Designing together**, where you effectively plan and run a design session and identify and engage the right people.
- **Giving and receiving feedback** maps to **Designing together**, named in both directions.
- **Using evidence** maps to **Evidence-based design**.
- **Risk, opportunity and contribution to patterns** map to **Designing strategically**.
- **Supporting colleagues** maps to **Leading design**.

### Practice questions

**Question 1 (easy) — A session where everyone has an opinion**

You are running a design session on a page's visual hierarchy. Twenty minutes in, four people are debating a colour and nobody has mentioned the heading structure you convened the session to resolve. What is the most effective response?

- A) Let it run; the colour matters too.
- B) Note the colour question for later, restate the decision the session needs to reach, and change the format — for instance asking everyone to mark on a printout the order in which they would read the page, which produces evidence rather than preferences.
- C) Tell the group the colour debate is off-topic.
- D) End the session and reschedule.

**Correct answer: B. Least effective: D**

**Explanation:** Colour is the most opinion-attracting element in any design conversation, and a session left to itself will spend all its time there. Option B does three things: parks the colour question so nobody feels dismissed, restates the purpose, and — the part that makes it work — changes the format to one producing evidence. Asking people to mark reading order converts a discussion about preference into data about perception, and it is very hard to argue with the resulting marks. Your role names planning and running design sessions and identifying and engaging the right people, and adapting a format that is not working is the skill rather than a workaround. Option D is least effective, discarding twenty minutes and everyone's availability over a recoverable problem. Option A lets the session fail. Option C may work and spends goodwill unnecessarily.

**Question 2 (easy) — A brand constraint that reduces legibility**

A communications colleague requires the brand's light grey for body text. It measures 3.2:1 against white; the requirement for that size is 4.5:1. What is the most effective response?

- A) Use it; the brand matters.
- B) State the measured value and the threshold, and offer the brand's darker grey — or a darkened variant of the same hue — which keeps the palette recognisable while meeting the requirement.
- C) Refuse and use black.
- D) Use the light grey and enlarge the text so a lower threshold applies.

**Correct answer: B. Least effective: D**

**Explanation:** The colleague's concern is legitimate and the specific instruction is unworkable, so the answer is substitution rather than refusal. Option B does the two things that make a visual argument land: it supplies the measured value, converting a matter of taste into a matter of fact, and it offers an alternative from within the brand, which addresses what the colleague actually wants. Most brand palettes already contain a darker variant of the primary, because the primary is optimised for impact rather than reading. Option D is least effective and is the sophisticated-looking trap: enlarging body text purely to escape a threshold games the criterion rather than meeting its purpose, and produces oversized text that scans badly for everyone including the people the rule protects. Option A publishes text some people cannot read. Option C discards the brand unnecessarily.

**Question 3 (easy) — An off-system value**

You find a spacing value of 20 pixels in a component, against a system scale of multiples of 8. What is the most effective response?

- A) Change it to 24.
- B) Find out what the 20 was solving before changing it — an off-scale nudge usually indicates a real layout problem somebody fixed by eye — then either resolve that properly or, if the scale genuinely cannot accommodate the case, raise it as a gap in the system.
- C) Leave it; 20 is close to 24.
- D) Raise a ticket.

**Correct answer: B. Least effective: C**

**Explanation:** An off-scale value is a symptom, and changing it without understanding it will reintroduce whatever problem prompted it — most likely a component that does not sit correctly at 16 or 24. Option B investigates first and names the second possibility, which is the one that matters at your level: if the scale genuinely lacks a step the design needs, that is a finding about the system rather than a mistake by a designer, and it is your role's contribution to patterns and components to raise it. Option C is least effective, normalising a value that breaks the property making a scale useful, which is that every value is predictable. Option A fixes the symptom and loses the information. Option D defers without diagnosing.

**Question 4 (moderate) — Feedback that stings**

In a critique, a senior colleague says your layout is "cluttered and the hierarchy doesn't work". You think it is clear. What is the most effective response?

- A) Explain the hierarchy you intended.
- B) Ask what order they read the page in, since if an experienced designer read it in a different order from the one you designed, the hierarchy is not working regardless of intention — then fix that specific thing.
- C) Accept it and start again.
- D) Ask for the feedback in writing.

**Correct answer: B. Least effective: A**

**Explanation:** Both things can be true: you designed a hierarchy, and the page does not communicate it. Option B converts feedback into information, and the specific question matters — asking what order somebody read in produces a concrete, checkable answer, while asking what they disliked produces opinion. If they read the caption before the heading, you know the caption is too heavy or the heading too light, and you have a measurable fix. Option A is least effective because explaining your intention does not change what a reader experiences, and it teaches the room that giving you feedback means hearing a defence, which is how designers stop receiving useful critique. Option C discards work without extracting the lesson. Option D defers a two-minute conversation.

**Question 5 (moderate) — A developer's constraint**

A developer says touch targets cannot be enlarged "because of the layout", and research shows users mis-tapping. What is the most effective response?

- A) Make the icons smaller so more fit.
- B) Ask what specifically constrains the size, and raise the option that resolves most cases: extending the interactive area invisibly beyond the visible graphic, since a touch target need not match the size of what is drawn.
- C) Insist the layout changes.
- D) Add a note asking users to tap carefully.

**Correct answer: B. Least effective: D**

**Explanation:** "Because of the layout" is a compressed claim covering several possibilities, and the productive move is to establish which. Option B does that and names the mechanism resolving most instances, which is genuinely useful knowledge to bring to a developer: a 16-pixel icon can carry a 44-pixel target without changing anything visible. Option D is least effective, asking users to compensate for a defect — futile, and the clearest possible statement that the problem was noticed and not fixed. Option A makes the visible element smaller, worsening the original problem. Option C asserts without understanding, and a designer who treats every constraint as negotiable is not believed about the ones that are.

**Question 6 (moderate) — Evidence that contradicts your design**

In testing, seven of ten participants missed a secondary action you positioned deliberately. What is the most effective response?

- A) Note that the participants were rushed and keep the design.
- B) Treat it as a signal about the design, look at what drew attention away — position, contrast, competing weight, or whether the action answers a question the page has not yet raised — and propose a change to test next round.
- C) Make it a primary button.
- D) Ask for more participants.

**Correct answer: B. Least effective: A**

**Explanation:** Seven of ten missing the same element is a signal, not a coincidence. Option B treats it as one and lists the realistic mechanisms, including the fourth that designers often miss: an action can be perfectly visible and still be ignored if the user has no reason to want it yet, which is a sequencing problem rather than a visual one and would not be fixed by making it louder. Option A is least effective — dismissing consistent behaviour as participant error is the most reliable way for a designer to stop learning. Option C jumps to a solution that creates a competing call to action and usually weakens both. Option D delays a cheap improvement when ten participants converging is already sufficient to try something different.

**Question 7 (moderate) — Contributing to the system**

You have solved a recurring layout problem with a component variant that works well in your service. What is the most effective next step?

- A) Keep using it locally.
- B) Document it with the reasoning and the evidence, including what you tested and what you did not, and propose it to whoever maintains the system — accepting that it may be changed or rejected, which is preferable to five services each inventing their own version.
- C) Add it to the system yourself.
- D) Share a screenshot in the design channel.

**Correct answer: B. Least effective: A**

**Explanation:** Your role names contributing to the development of design patterns and components, and this is the case where that obligation is concrete: a recurring problem solved once and shared is worth more than five separate solutions, all slightly different and none properly tested. Option B does it well, and the honest note about what was not tested is what prevents the variant acquiring more authority than it earned — a component adopted widely on the strength of one service's testing is a risk rather than a gift. Option A is least effective, keeping a solution while others repeat the work and diverge. Option C bypasses the maintainers and the review that makes a system trustworthy. Option D shares an image without the reasoning, which is how variants get copied badly.

**Question 8 (harder) — An accessibility problem found late**

Two weeks before launch you find the focus indicator across every component measures 1.6:1 against its background, well below the 3:1 requirement. What is the most effective response?

- A) Launch and add it to the backlog.
- B) Raise it immediately with the delivery manager and service owner, describe precisely what a keyboard user experiences — no visible indication of where they are — ask for an explicit recorded decision, and check whether the system's default focus style can simply be reinstated.
- C) Change the focus style yourself across the components.
- D) Launch and publish an accessibility statement noting the gap.

**Correct answer: B. Least effective: A**

**Explanation:** A focus indicator below the threshold makes the service effectively unusable without a mouse, and weighing that against a launch date is a decision for people with authority — though raising it precisely and now is entirely yours. Two details make option B strong: asking for a recorded decision prevents the matter drifting into launch by default, and checking the system default is the practical step nobody thinks of under pressure, since a failing custom focus style has usually replaced a compliant default and reinstating it may fix everything in an afternoon. Option A is least effective, because the backlog is where accessibility problems remain. Option D treats a statement as a way to launch with a known blocker, which it is not. Option C risks a fortnight with nobody aware.

**Question 9 (harder) — Consensus that would exclude people**

The team has converged on a status system using colour alone, which everyone likes and which your evidence indicates will fail users with colour vision deficiency. Reopening it reverses a decision people are relieved to have made. What is most effective?

- A) Let it go; the team has decided.
- B) Raise it once, clearly, with the arithmetic — that across this service's user base the affected group runs into tens of thousands a year — and propose the minimal mitigation of adding an icon or text label, then if the team proceeds ensure the risk is documented and propose measuring the outcome.
- C) Escalate to the service owner.
- D) Keep raising it until the team changes course.

**Correct answer: B. Least effective: A**

**Explanation:** You have an obligation to say the thing and you also have to work with these people. Option B threads that: raise it once with evidence rather than principle, and propose the minimal change rather than a redesign, because "add an icon" is a far easier thing to accept than "rethink the status system" and achieves the necessary result. If the decision stands, documenting the risk makes it knowing rather than accidental, and measuring gives reality a vote. Option A is least effective, because a consensus excluding people who already have fewer options is not a value, and silence makes you complicit in a decision you had the evidence to inform. Option C escalates before the direct route. Option D substitutes persistence for persuasion, and a designer who relitigates everything stops being heard on anything.

**Question 10 (harder) — A token you defined**

You realise a colour token you defined, now used in two services, measures 4.4:1 rather than the 4.6:1 you recorded. What should you do?

- A) Correct it quietly.
- B) Tell both teams and your lead now, state the measured value and where the token is used, correct it, and check whether other tokens defined in the same session were measured the same way — since the error suggests a method problem rather than a slip.
- C) Correct it and mention it at stand-up.
- D) Leave it; 4.4 is close.

**Correct answer: B. Least effective: D**

**Explanation:** A token is used everywhere it is available, which is what makes a small error consequential: 4.4:1 is a failure across every element using it in two services. Option B does four things — tells the affected teams, states the value rather than describing the problem, corrects it, and asks the diagnostic question that makes it more than a fix. A mis-measured token usually means it was checked against the wrong background or with the wrong tool, and if so, everything defined alongside it is suspect. Option D is least defensible: "close" applied once to a threshold becomes the standard for every future judgement, and thresholds work precisely because they have no discretionary zone. Option A leaves published work unexamined. Option C delays disclosure of something live.

**Question 11 (harder) — An assumption in the room**

In a session someone says "colour blindness is rare, we don't need to design for it". The service has around 700,000 users a year. What is most effective?

- A) Let it go.
- B) Bring the arithmetic — around one in twelve men and one in two hundred women have red-green colour vision deficiency, which across a user base this size means tens of thousands of people a year — and ask what should happen to them, so the decision is made knowingly.
- C) Argue that all designs must be accessible.
- D) Raise it privately afterwards.

**Correct answer: B. Least effective: A**

**Explanation:** The comment rests on an intuition about rarity, and intuitions about rarity collapse against a base number. Option B supplies the arithmetic and then asks a question, keeping the conversation about the design rather than about who is right and leaving room for the team to have an answer. It is also more effective than a principle, because a principle invites a debate about principles while a number invites a decision. Option A is least effective: a decision made on an assumption that is numerically wrong will exclude real people and you had the number. Option C states something true in the least persuasive available form. Option D misses the moment when the decision is being made.

**Question 12 (harder) — A flaw in your own work**

Three weeks after a design decision you supported, you realise the evidence behind it came from testing on a single high-quality monitor at full brightness. What should you do?

- A) Note it as a limitation next time.
- B) Tell the team now, scope precisely which conclusions are affected — legibility and colour discrimination findings, rather than findings about position or comprehension — and propose a quick re-check on a phone in daylight and a dimmed laptop, which costs an hour.
- C) Quietly re-check and correct the record if findings differ.
- D) Say nothing; the decision was probably fine.

**Correct answer: B. Least effective: D**

**Explanation:** Testing on the best screen available is the display equivalent of recruiting only confident users, and it flatters exactly the properties a graphic designer is responsible for. Option B does the three things that matter: tells the people who acted on the finding, scopes the damage precisely rather than minimising or catastrophising, and proposes a fix proportionate to the problem — an hour with a phone outdoors and a dimmed laptop will settle it. The scoping is important, because findings about where things are and what icons mean remain sound, and overstating the damage is as unhelpful as understating it. Option D is least defensible: reasoning that the decision was probably fine substitutes your guess for the evidence you relied on. Option C conceals a known flaw while the design stands.

### Preparation tips

- **Bring the value, not the opinion.** A measured ratio ends an argument that taste cannot.
- **Offer an alternative from inside the constraint.** A darker variant of the brand hue beats refusing the brand.
- **Change the format when a session produces preferences.** Marking reading order produces evidence.
- **Ask what order somebody read in.** It converts hierarchy feedback into something checkable.
- **Ask what an off-system value was solving.** It is usually a real problem, and sometimes a gap in the system.
- **Extend the target beyond the graphic.** It resolves most touch-size constraints without touching the layout.
- **Propose the minimal mitigation.** "Add an icon" is accepted where "rethink the system" is not.
- **Scope your own errors precisely.** Some findings survive a flawed condition.

### Common pitfalls to avoid

- **Explaining your intention in response to hierarchy feedback.**
- **Dismissing consistent behaviour as participant error.**
- **Making a secondary action primary to fix discoverability.**
- **Gaming a criterion rather than meeting its purpose.**
- **Asking users to compensate for a defect.**
- **Normalising an off-scale value because it is close.**
- **Treating "close enough" as a threshold.** 4.4 is a fail.
- **Keeping a solved problem locally while other services reinvent it.**

## Conclusion

You have reached the end, and it is worth pausing over what that involved: forty-eight questions across four assessment types, with the reasoning worked through on each. That is a substantial piece of professional preparation and rather more than most people do.

Look back at the ground. In the cognitive section you counted requirements rather than values, spotted that a token passing at 4.6:1 has no headroom against a tinted panel, named the ten-minute empirical test that distinguishes a layout failure from a context effect, scoped a display-condition flaw precisely enough to say which findings survived, and recognised that time on page has no direction. In the numeric section you read thresholds at their boundaries, remembered that twelve columns have eleven gutters, paired a line-length calculation with the range that gives it meaning, and converted a defect into forty-eight thousand people a year. In the verbal section you read "or" as offering alternative routes, noticed that field boundaries are named because that is where the requirement gets forgotten, declined to mark False on something you suspected but the passage had not tested, and kept exceptions in a summary. And in the situational judgement section you changed a session's format to produce evidence instead of preferences, offered a darker brand variant rather than a refusal, asked what an off-scale spacing value was solving, and proposed adding an icon rather than rethinking a status system.

Notice what unites almost all of it. Every section, in its own idiom, was training you to attach values to visual decisions — because in this context a design decision either lets somebody complete a task or prevents them, and the difference is measurable. That is what makes you trusted to make good decisions, which is the phrase your role description uses, and it is what turns a discipline everybody feels entitled to have opinions about into one whose judgements can be checked.

A word about your level. Being trusted is a real threshold. Nobody reviews your reasoning before it reaches a build, and the standard you hold yourself to becomes the standard the service gets. It also means the errors that matter most are the ones you are confident about — and in a visual discipline that is particularly true, because a design you have looked at for three days stops being something you can see.

If you want to build on this, a few things repay effort more than rereading. Measure every colour pairing in a service you know, including text on coloured panels rather than only on white. Complete a service using only a keyboard and watch the focus indicator. View a page at 400% zoom, at 375 pixels, and on a phone outdoors. Print it and read it at arm's length. Ask a developer how a spacing token actually reaches the browser. And practise stating findings with their values attached until the precise version is the one that comes naturally.

Finally, for the day itself. An assessment samples your reasoning on one morning under artificial conditions. It is not a verdict on your judgement or your career. Read the stem twice, read thresholds at the boundary, find the denominator, trust Cannot Say, and remember that the strongest answer is usually the one honest about uncertainty rather than the one that sounds most decisive.

Good luck. Go carefully, measure things, and keep looking at the edges.
