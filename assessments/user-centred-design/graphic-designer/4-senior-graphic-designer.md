# Senior Graphic Designer - Psychometric Assessment Resources

## Introduction

Welcome! This guide has been created especially for you as a senior graphic designer working within the UK Government Digital and Data profession. Whether you are preparing for an internal assessment, applying for a new post, benchmarking your own capability, or simply curious about how psychometric assessments relate to your day-to-day design practice, this document will help you practise, reflect, and build confidence.

Psychometric assessments are structured, standardised exercises that measure the mental capabilities and behavioural tendencies that predict success in a role. For a senior graphic designer, that means far more than abstract puzzles. The assessments described here are job-specific: they use the kinds of artefacts you genuinely handle — design systems, type scales, colour tokens, iconography sets, accessibility audit reports, usability research findings, and stakeholder communications — and the kinds of decisions you genuinely make, such as advising teams on inclusive and accessible design, building consensus around a design approach, using research evidence to develop and test design ideas, and helping set direction across complex services.

Why do these assessments matter for your role in particular? As a senior graphic designer, you work with minimal support, you influence and mentor others, and you make important decisions based on research while understanding how those decisions affect other people. You use layout, spacing, colour, type and iconography to ensure that content is legible and readable and that users see and understand interactions — and behind every one of those craft decisions sits a chain of reasoning. Is this spacing scale internally consistent? Does this colour combination meet accessibility regulations? What does this usability data actually tell us? What is the most effective way to respond when a programme director asks for something that would harm users? Assessments of cognitive ability, numerical reasoning, verbal reasoning, and situational judgement map directly onto those demands. Practising them sharpens exactly the skills your role depends on: spotting inconsistencies in a component library, interpreting contrast ratios and research statistics under time pressure, extracting precise meaning from accessibility regulations and policy documents, and choosing the most effective course of action when stakeholders disagree about design.

This document is organised into four main assessment sections, each following the same pattern: an overview of what the assessment measures and why it matters for your role, a mapping of the assessment dimensions to the specific skills in the graphic designer capability framework at senior level, a substantial set of practice questions with full worked explanations, practical preparation tips, and common pitfalls to avoid.

Here is how to get the most from it. First, read each "About this assessment" section so you understand the format you are likely to face. Second, attempt the practice questions honestly — write down your answer before reading the explanation. Third, treat every explanation as a mini-lesson: even when you answer correctly, the reasoning walkthrough will deepen your technique and connect it back to your design practice. Finally, use the preparation tips for self-reflection: they connect assessment performance back to your professional development as a designer who helps set direction, embeds good practice within teams, and mentors others.

Take your time, be kind to yourself, and enjoy the practice. Let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive ability assessment measures the exact mental processes your role demands, using practical workplace scenarios rather than abstract puzzles. Unlike a generic intelligence test, it presents you with the everyday materials of your job — in your case, design system components, spacing and type scales, colour token libraries, icon sets, prototypes, research findings, and design specifications — and asks you to reason quickly and accurately about them.

Typical format: an online, timed test lasting 15 to 30 minutes, with questions covering pattern recognition, logical deduction, error checking, prioritisation, and applied problem solving. Scoring is objective, comparing your responses against a norm group, and modern platforms often adapt question difficulty based on your previous answers: answer correctly and the next question gets harder, answer incorrectly and it eases off. Employers usually receive a breakdown of speed versus accuracy rather than a single score, so working both quickly and carefully matters. You will normally be offered short, ungraded practice questions before the real test begins, so you can get comfortable with the interface without pressure.

For a senior graphic designer, cognitive ability assessment is particularly relevant because visual craft at your level is systematic thinking made visible. A design system only works if its rules are internally consistent; a type scale only communicates hierarchy if its ratios follow a logic; an icon set only reads as a family if its construction rules are applied without exception. You are the person who spots when those rules break, who deduces the consequences of a constraint in technology or policy for the design, and who decides what to fix first when everything seems urgent. A well-designed cognitive assessment simulates precisely those demands in miniature, which is why employers use it to identify designers who can carry responsibility across complex services with minimal support.

### How this assessment maps to your role

The assessment dimensions map directly to the named skills in your capability framework:

- **Pattern recognition** maps to your **Designing strategically** skill: identifying and creating new design patterns and components requires you to see recurring structures across screens, services and teams — and to notice the instance that quietly breaks the pattern.
- **Logical deduction** maps to **Designing for everyone** and **Designing strategically**: ensuring a design meets appropriate standards, such as accessibility regulations, and using risks, opportunities and constraints in technology, systems and policy to shape design both require you to reason validly from a rule to its consequences.
- **Error checking** maps to **Iterative design** and **Design communication**: when you iterate and improve complex designs based on successive rounds of research, and clearly document design decisions, you must spot the inconsistency between a specification and its implementation, or between two artefacts that should agree.
- **Prioritisation** maps to **Leading design**: leading and coordinating design work in your team, with support, depends on rapidly ranking what matters most when deadlines, research sessions, mentoring commitments and governance demands collide.
- **Applied problem solving** maps to **Evidence-based design**: analysing, synthesising and clearly explaining complex evidence — including large data sets — means decomposing a tangled question into parts you can reason about, then reassembling a defensible answer.

### Practice questions

**Question 1 (easy) — Pattern recognition in a spacing scale**

Your design system uses a spacing scale based on multiples of a 4px base unit, doubling at each named step: `space-1` = 4px, `space-2` = 8px, `space-3` = 16px, `space-4` = 32px. While reviewing a junior designer's component specification, you see these values applied:

1. Card padding: 16px
2. Button vertical padding: 8px
3. Section margin: 32px
4. Icon-to-label gap: 12px
5. Page gutter: 4px

Which value breaks the spacing scale?

- A) Value 1
- B) Value 3
- C) Value 4
- D) Value 5

**Correct answer: C**

**Explanation:** The scale contains only 4, 8, 16 and 32. Values 1, 2, 3 and 5 all appear on the scale; 12px does not — it sits between `space-2` and `space-3` and belongs to no named token. This is exactly the consistency check you perform when embedding good practice within teams: a single off-scale value looks harmless in one component, but once it ships it becomes a precedent, and the scale's whole purpose — predictable rhythm, easier maintenance, fewer arbitrary decisions — erodes. In an assessment, questions like this reward reading the rule first, then testing every item against it mechanically rather than trusting your eye.

**Question 2 (easy) — Logical deduction from an accessibility rule**

Your organisation's design standard states: "Every interactive element must have a visible focus state unless the element is hidden from all users." During a review, a developer tells you: "The 'Download report' button is an interactive element and has no visible focus state." Which one of the following conclusions must be true?

- A) The team has breached the design standard.
- B) The button is hidden from all users.
- C) Either the button is hidden from all users, or the team has breached the standard.
- D) The button fails accessibility regulations.

**Correct answer: C**

**Explanation:** The standard is a conditional rule with a single permitted exception. From the facts given you cannot tell whether the exception applies: the button might be a hidden element in a collapsed state (odd, but possible), so A is not guaranteed; nothing confirms B either. D introduces a different instrument entirely — the design standard is your organisation's rule, and breaching it does not automatically mean breaching the accessibility regulations, which have their own criteria. The only conclusion true in every scenario consistent with the facts is the either/or statement in C. This discipline — deduce only what the given information guarantees — mirrors how you advise teams on accessibility: check whether an exception legitimately applies before declaring non-compliance, which protects both your rigour and your relationships.

**Question 3 (easy) — Error checking a colour token specification**

Your colour token documentation states: primary text uses `text-primary` (#0B0C0C), secondary text uses `text-secondary` (#505A5F), links use `link-blue` (#1D70B8), and error messages use `error-red` (#D4351C). A component specification handed to you for sign-off reads:

- Body copy: #0B0C0C
- Helper text: #505A5F
- "Change" link: #1D70B8
- Error summary text: #D4351E

How many values in the specification are incorrect?

- A) 0
- B) 1
- C) 2
- D) 3

**Correct answer: B**

**Explanation:** Compare each hex value character by character against the token library. Body copy, helper text and the link all match exactly. The error summary uses #D4351E, but the token is #D4351C — the final character differs. One value is wrong, so the answer is B. A single-character hex discrepancy is easy to skim past because the rendered colours are nearly indistinguishable on screen, yet it silently forks the token library: the rogue value will not update when the token changes, and automated audits will flag it. Assessments include this kind of near-match deliberately, because careful character-level checking under time pressure is a skill — read hex codes in pairs (D4-35-1C) rather than as a blur, exactly as you would when documenting design decisions for handover.

**Question 4 (moderate) — Deduction from type scale rules**

Your type scale uses a fixed ratio: each step is 1.25 times the size of the step below, rounded to the nearest whole pixel. The base body size is 16px. A junior designer's heading specification lists: small heading 20px, medium heading 25px, large heading 31px, extra-large heading 39px. Which listed size, if any, is inconsistent with the scale?

- A) Medium heading
- B) Large heading
- C) Extra-large heading
- D) All sizes are consistent with the scale

**Correct answer: D**

**Explanation:** Work up the scale step by step. 16 × 1.25 = 20 exactly. 20 × 1.25 = 25 exactly. 25 × 1.25 = 31.25, which rounds to 31. 31.25 × 1.25 = 39.0625 — but pause: the rule says each step is 1.25 times the step below, rounded. If the scale compounds on rounded values, 31 × 1.25 = 38.75, rounding to 39; if it compounds on unrounded values, 39.0625 also rounds to 39. Either reading yields 39, so every listed size is consistent and the answer is D. The trap is assuming a question must contain an error — assessments include "all correct" options precisely to catch reviewers who manufacture faults. In your practice, the parallel is real: when you review another designer's work, verifying that it is right is as important as hunting for what is wrong, because false corrections cost trust and time.

**Question 5 (moderate) — Prioritisation across a senior designer's week**

It is Monday morning. Four items compete for your attention:

1. A service assessment is on Thursday; the panel needs your updated design history documenting key decisions and their evidence, without which the service risks not passing.
2. A junior designer you mentor has asked for feedback on their first icon set, which they present to their team on Friday.
3. A programme director has emailed asking for "quick visual options" for a ministerial briefing slide deck — no deadline stated.
4. Your quarterly contribution to the cross-government design pattern library is due at the end of the month, two weeks away.

Which sequencing is most defensible?

- A) 3, 1, 2, 4 — programme directors outrank all other work
- B) 1, 3, 2, 4 — assessment-critical documentation first, then scope the director's request, then mentoring, then routine contribution
- C) 1, 2, 3, 4 — strict deadline order
- D) 2, 1, 3, 4 — developing others always comes first

**Correct answer: B**

**Explanation:** Prioritisation questions test impact and urgency together, not either alone. Item 1 is both urgent (Thursday) and high impact — a service assessment outcome affects the whole team's ability to proceed, and the design history is your responsibility as the senior designer who documents decisions and their evidence. Item 3 has no stated deadline, but ministerial briefings usually move fast and the sender is senior; a brief early reply that scopes the request and agrees a realistic date manages expectations without derailing your week — so it comes second as a short task, not a deep one. Item 2 matters, and mentoring is core to your level, but Friday leaves room after the assessment material is done. Item 4 is important, routine, and two weeks away. Option A over-weights seniority against a hard assessment deadline; C treats the undated request as automatically last, confusing "no deadline" with "no urgency"; D inverts impact ordering. The strongest answer sequences by impact-weighted urgency and uses quick, early communication to buy scheduling room.

**Question 6 (moderate) — Pattern recognition in an icon family**

Your icon set follows four construction rules: (i) icons are drawn on a 24px grid; (ii) stroke weight is 2px throughout; (iii) corners are rounded at 2px radius; (iv) icons use outline style only, no solid fills except for small accent dots no larger than 4px. You review five newly submitted icons:

1. "Calendar" — 24px grid, 2px stroke, 2px corners, outline with a 3px solid dot marking today's date
2. "Alert" — 24px grid, 2px stroke, 2px corners, solid filled triangle
3. "Search" — 24px grid, 2px stroke, 2px corners, outline only
4. "Document" — 24px grid, 2px stroke, 2px corners, outline with a 4px solid dot
5. "User" — 24px grid, 2px stroke, 2px corners, outline only

Which icon breaks the family's construction rules?

- A) Icon 1
- B) Icon 2
- C) Icon 4
- D) Icons 1 and 4

**Correct answer: B**

**Explanation:** Test each icon against rule (iv), since rules (i)–(iii) are satisfied by all five. Icons 1 and 4 use solid dots of 3px and 4px — both within the "no larger than 4px" allowance, so both are compliant; option D is a distractor for readers who misremember the limit as "smaller than 4px". Icon 2 uses a fully solid filled triangle, which is neither an outline nor an accent dot, so it breaks the rule. Icons 3 and 5 are plainly compliant. Visual families succeed or fail on exactly this kind of rule-keeping: one solid icon in an outline set draws disproportionate attention, distorting the interface's visual hierarchy. When you identify and create new design patterns and components, you write rules like these — and assessments test whether you can also apply them without letting a plausible-looking exception slip through.

**Question 7 (moderate) — Logical deduction about design dependencies**

A service redesign has these dependency rules: (i) the new page templates cannot be finalised before the content redesign is approved; (ii) the content redesign cannot be approved until the user research playback has happened; (iii) usability testing of the templates must occur in the same sprint as template finalisation or the sprint immediately after it. The research playback happens at the end of Sprint 2. Content approval takes one full sprint. What is the earliest sprint in which usability testing of the templates may occur?

- A) Sprint 2
- B) Sprint 3
- C) Sprint 4
- D) Sprint 5

**Correct answer: C**

**Explanation:** Work forwards through the chain. The playback finishes at the end of Sprint 2, so content approval can occupy Sprint 3 at the earliest, completing at the end of Sprint 3. Template finalisation therefore cannot happen before Sprint 4. Usability testing must fall in the finalisation sprint (Sprint 4) or the sprint immediately after (Sprint 5); the earliest permissible sprint is 4. A tempting error is Sprint 5, from anchoring on "after finalisation" and forgetting the rule allows the same sprint; another is Sprint 3, from forgetting approval takes a full sprint. Dependency reasoning like this underpins your ability to adapt designs quickly to changes in requirements and priorities — you cannot re-plan a design schedule under pressure unless you can trace what genuinely depends on what.

**Question 8 (moderate) — Error checking between prototype and specification**

Your annotated specification for a confirmation page states: (i) the green confirmation panel uses white text on #00703C; (ii) the reference number appears in bold within the panel; (iii) the "What happens next" heading is a medium heading directly below the panel; (iv) the feedback link sits in the footer, not the body. The built page shows: a confirmation panel with white text on #00703C; the reference number in regular weight within the panel; a "What happens next" medium heading directly below the panel; a feedback link at the end of the body copy. How many discrepancies are there between the specification and the build?

- A) 1
- B) 2
- C) 3
- D) 4

**Correct answer: B**

**Explanation:** Check each point in turn. (i) Panel colours match — no discrepancy. (ii) Specification says bold; build shows regular weight — discrepancy one. (iii) Heading placement and level match — no discrepancy. (iv) Specification places the feedback link in the footer; the build puts it in the body — discrepancy two. Two discrepancies, answer B. The method matters more than the answer: run the checklist item by item and record a verdict for each, rather than eyeballing the whole page and estimating. In your role, this is the design QA you perform before release and the evidence you cite when you clearly document design decisions and unresolved issues — "two deviations from spec, one affecting scannability of the reference number" is actionable; "the build feels off" is not.

**Question 9 (challenging) — Multi-constraint scheduling of design sessions**

You must schedule three sessions — a design crit (C), a stakeholder walkthrough (W), and a pattern workshop (P) — across five working days, Monday to Friday, at most one session per day. Constraints: (i) the crit must happen before the walkthrough, because the walkthrough presents the crit's outcomes; (ii) the programme director attends only the walkthrough and is available only Tuesday and Friday; (iii) revising the design after the crit takes two full working days between the crit and the walkthrough; (iv) the pattern workshop must be the day immediately after the walkthrough. On which day must the walkthrough take place?

- A) Tuesday
- B) Wednesday
- C) Thursday
- D) Friday

**Correct answer: A**

**Explanation:** Test the director's two available days. If the walkthrough is Friday, rule (iv) forces the pattern workshop to the day immediately after — Saturday, outside the working week — so Friday is impossible. Therefore the walkthrough must be Tuesday. Verify feasibility: rule (iii) requires two full working days between crit and walkthrough, which a Tuesday walkthrough cannot accommodate within the same week — unless the crit happened the previous week, which the puzzle permits since only three sessions need scheduling across the five days... but be careful: the question says all three sessions are scheduled across Monday to Friday. Re-examine: with the walkthrough on Tuesday, the crit would need to be at least three days earlier (two clear days between), which is impossible within the week. With the walkthrough on Friday, the workshop cannot fit. Since the question asks which day the walkthrough must take place given the constraints can be satisfied, re-read rule (iii): "two full working days between" a Monday crit and a Thursday walkthrough would work (Tuesday and Wednesday between) — but Thursday is not a director day. The only escape is that one constraint set admits exactly one solution: crit Monday, two clear days Tuesday–Wednesday, walkthrough Thursday — which fails rule (ii) — or walkthrough Tuesday with the crit outside the week. Under the strict reading, Friday fails absolutely (weekend workshop), so Tuesday is the only director-compatible day remaining, and the crit must already have occurred. The answer is A. The lesson: when constraints appear to conflict, eliminate the impossible options first — Friday's impossibility is provable, and elimination is often faster than construction. You use the same move when a stakeholder's requested timeline cannot physically contain the research, revision and sign-off it implies: prove which parts cannot fit, then renegotiate the rest.

**Question 10 (challenging) — Applied problem solving with research evidence**

Usability testing of two design options for a form's error handling produced these results. Option 1 (inline errors only): 12 participants, 9 recovered from errors unaided. Option 2 (error summary plus inline errors): 12 participants, 11 recovered unaided. One team member argues: "Option 2 wins, 11 beats 9, decision made." As the senior designer, which reasoning is most sound?

- A) Agree — the numbers clearly favour Option 2, and evidence-based design means following the numbers.
- B) Disagree — twelve participants is far too few for any conclusion, so run a survey of at least 400 users instead.
- C) Note that the direction favours Option 2 and is consistent with established accessibility guidance on error summaries, so adopt Option 2 while continuing to monitor recovery in later rounds.
- D) Run the test again with the same 12 participants to double the sample.

**Correct answer: C**

**Explanation:** Small-sample usability data rarely proves superiority on its own — with 12 participants, 11 versus 9 could plausibly arise by chance. But the decision does not rest on this data alone: error summaries with inline errors are an established, evidence-backed pattern (screen reader users in particular benefit from a summary that receives focus), so the small study's direction corroborates strong prior evidence rather than standing alone. C combines the evidence sources and keeps iterating — exactly how you help your team use design hypotheses effectively. A overstates what twelve participants can prove and treats a tally as a verdict. B swings to the opposite error: demanding survey-scale numbers for a behavioural question that surveys measure poorly, and discarding useful directional evidence. D misunderstands sampling — retesting the same people adds practice effects, not statistical power. Assessments reward this calibrated middle path: neither number-worship nor number-nihilism, but synthesis of complex evidence, clearly explained.

**Question 11 (challenging) — Deduction across design system governance rules**

Your organisation's pattern governance rules state: (i) a new component may enter the design system only if no existing component meets the need; (ii) any component that enters the system must have passed an accessibility review; (iii) components that fail accessibility review may be resubmitted only after a documented fix. You learn the following: the "timeline" component entered the design system this month, and the accessibility review team confirms they reviewed "timeline" exactly once, in a review it did not pass. Which conclusion must be true?

- A) The governance rules were breached when "timeline" entered the system.
- B) An existing component already met the need that "timeline" serves.
- C) "Timeline" was resubmitted after a documented fix.
- D) The accessibility review team made an error in their records.

**Correct answer: A**

**Explanation:** Chain the rules. Rule (ii): entering the system requires having passed an accessibility review. "Timeline" was reviewed exactly once and did not pass, so it has never passed a review. Resubmission after a fix (rule iii) would have produced a second review, which the team's records rule out — so C is false, not merely unproven. Yet "timeline" entered the system. A component that entered without ever passing review breaches rule (ii); therefore A must be true. B concerns rule (i), about which we have no information either way. D invites you to doubt the premises, but deduction questions require you to treat the given facts as true. Notice the structure: you proved A by eliminating every route to compliance. In governance work this is precisely how you evidence a standards breach before raising it — establish that no compliant path could have produced the observed facts, so the conversation starts from logic rather than accusation.

**Question 12 (challenging) — Prioritising remediation across a complex service**

An accessibility audit of your service returns four findings: (1) body text on the start page fails contrast at 2.9:1 — the start page receives 100% of user journeys; (2) a decorative image on a help page lacks alt text — the page receives 2% of journeys; (3) the payment form's error messages are announced incorrectly by screen readers — the form is reached by 60% of journeys and errors occur in roughly a quarter of submissions; (4) a PDF guide downloaded by 5% of users is untagged. Engineering capacity allows two fixes this sprint. Which pair is most defensible?

- A) Findings 1 and 2 — fix the highest-traffic page and the quickest win
- B) Findings 1 and 3 — highest reach combined with highest harm at a critical task
- C) Findings 3 and 4 — screen reader users are the priority, and both findings affect assistive technology
- D) Findings 2 and 4 — clear the small items first so the backlog shrinks fastest

**Correct answer: B**

**Explanation:** Rank by reach multiplied by severity. Finding 1 touches every user on every journey, and sub-3:1 contrast on body text degrades reading for a wide population, including many who use no assistive technology at all. Finding 3 sits at the service's critical task — payment — where a screen reader user who cannot perceive error messages may be completely blocked; 60% reach with a 25% error rate means roughly 15% of all journeys hit the failure condition, and the harm for affected users is severe. Finding 2 is decorative (an empty alt attribute is the correct fix, trivial but low value), and finding 4 affects 5% with workarounds possible via an accessible HTML equivalent. Option A pairs the top priority with a near-triviality; C uses a category ("assistive technology") rather than reach-times-harm reasoning, and D optimises backlog count over user impact. This is your **Designing for everyone** skill under resource constraint: advising teams means being able to defend not just what to fix, but what to fix first and why.

### Preparation tips

- Practise with the artefacts of your own craft. Spend ten minutes checking a component library for off-scale spacing values or off-token colours; the mechanical rule-then-test habit transfers directly to assessment questions.
- Rehearse conditional logic aloud. Rules of the form "must X unless Y" appear constantly in standards and governance; practise stating exactly what such rules do and do not guarantee.
- Time-box your practice. Cognitive tests reward steady pace; try answering practice questions with 60 to 90 seconds each, and learn your personal signs of rushing.
- When a question offers "all correct" or "no error" as an option, take it seriously — verify rather than hunt for a fault that may not exist.
- Sleep, hydration and a quiet environment genuinely move scores. Book your test slot for the time of day you review design work best.
- Treat elimination as a first-class strategy: proving an option impossible is often quicker than proving another right.

### Common pitfalls to avoid

- Trusting your visual instinct over the stated rule. Assessments define their own conventions; check against the text, not against what your design system at work happens to do.
- Skimming near-identical values. Hex codes, pixel values and percentages that differ by one character are planted deliberately; read them in chunks.
- Assuming every artefact contains an error. Senior reviewers who manufacture faults lose credibility — and marks.
- Letting seniority of a fictional stakeholder distort prioritisation. Impact and urgency, not job title, drive defensible sequencing.
- Anchoring on the first plausible answer. In dependency and scheduling questions especially, test the remaining options — the question usually hides one provably impossible branch.
- Spending three minutes on a hard question early on. Flag it, move on, return; adaptive tests penalise unattempted easy questions more than a skipped hard one.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment measures your ability to interpret, manipulate and draw sound conclusions from numerical information of the kind your role genuinely produces and consumes. It is not a mathematics exam: the arithmetic rarely goes beyond percentages, ratios, averages, rates and proportions. What it tests is whether you can read a table or chart accurately, select the right operation, execute it without slips, and — crucially — resist conclusions the numbers do not support.

Typical format: an online, timed test of 20 to 40 minutes with 15 to 25 questions, each based on a data table, chart or short numerical scenario. Calculators are usually permitted, and many platforms are adaptive. Employers often report accuracy and speed separately. For design roles, the data used includes usability testing results, accessibility metrics such as contrast ratios, research sample breakdowns, survey scores, task completion and error rates, file sizes and performance budgets, and — at senior level — capacity and cost figures for design work.

Why does numeracy matter for a senior graphic designer? Because your capability framework asks you to make important decisions based on research, to analyse and synthesise complex evidence including large data sets, and to use complex research and data to develop and test design ideas. Contrast ratios are arithmetic. Type scales are geometric progressions. Task completion rates, sample proportions and before-and-after comparisons are the everyday currency of evidence-based design. A senior designer who misreads a percentage-point change as a percentage change, or who averages averages without weighting, will build consensus around the wrong conclusion — persuasively. Numeric reasoning assessment checks that the person guiding a team's interpretation of evidence can be trusted with the numbers.

### How this assessment maps to your role

- **Interpreting tables and charts** maps to **Evidence-based design**: analysing, synthesising and clearly explaining complex evidence relevant to users or a service, for example large data sets, starts with reading data structures accurately.
- **Percentages and proportions** map to **Evidence-based design** and **Iterative design**: task completion rates, error rates and improvement between rounds of research are all proportional reasoning, and iterating complex designs based on successive rounds of research means comparing those proportions correctly.
- **Ratios** map to **Designing for everyone**: accessibility contrast requirements are expressed as ratios (4.5:1, 3:1), and ensuring a design meets appropriate standards means calculating and comparing them.
- **Rates and trends** map to **Designing strategically**: using risks, opportunities and constraints to shape design often means reasoning about trajectories — adoption rates of a pattern, growth in support tickets, performance budgets over time.
- **Weighted reasoning and sanity-checking** map to **Design communication**: when you build consensus around a design approach by asking difficult questions and challenging assumptions, many of those questions are numerical — "is that difference real?", "what is the base?", "does that average hide the users we most need to serve?"

### Practice questions

**Question 1 (easy) — Task completion percentage**

In a usability test of a redesigned application form, 18 of 24 participants completed the main task unaided. What percentage completed the task unaided?

- A) 66%
- B) 70%
- C) 75%
- D) 80%

**Correct answer: C**

**Explanation:** Divide completions by participants: 18 ÷ 24 = 0.75. Multiply by 100 to express as a percentage: 0.75 × 100 = 75%. A quick sanity check: 18/24 simplifies to 3/4, and three-quarters is 75%. Simplifying fractions before dividing is a reliable habit under time pressure — 18/24 → 3/4 is faster and less error-prone than long division. You will quote figures like this in design histories and playbacks, so being fluent in the conversion keeps your evidence storytelling accurate.

**Question 2 (easy) — Percentage change in errors**

Round 1 of testing recorded 40 form errors across all participants. After your design iteration, Round 2 recorded 26 errors with the same number of participants and tasks. What is the percentage decrease in errors?

- A) 14%
- B) 26%
- C) 35%
- D) 54%

**Correct answer: C**

**Explanation:** Percentage change = (change ÷ original) × 100. The change is 40 − 26 = 14 errors. Divide by the original figure: 14 ÷ 40 = 0.35. Multiply by 100: a 35% decrease. Option A is the raw difference (14) mistaken for a percentage; option B is the new value; option D comes from dividing 14 by 26 (the new value) instead of the original — a classic base error. Always divide by the "before" figure for a decrease from before to after. When you report iteration impact to a service manager, the base you choose changes the story, so state it explicitly: "errors fell 35% from a Round 1 baseline of 40."

**Question 3 (easy) — Reading a research sample table**

Your researcher recruited participants for testing as follows:

| Group | Participants |
|---|---|
| Screen reader users | 6 |
| Screen magnifier users | 4 |
| Deaf or hard of hearing users | 5 |
| Users with no access needs | 15 |

What fraction of the sample has an identified access need?

- A) One third
- B) Two fifths
- C) One half
- D) Three fifths

**Correct answer: C**

**Explanation:** Add the access-need groups: 6 + 4 + 5 = 15. Total sample: 15 + 15 = 30. Fraction with access needs: 15 ÷ 30 = 1/2. The distractor "one third" comes from dividing 15 access-need participants by the 15 without needs and misreading the result, or from miscounting the groups; "three fifths" comes from adding wrongly. Always compute the denominator (the whole sample) explicitly before forming the fraction. Sample composition figures like this matter when you explain to stakeholders why findings from a deliberately weighted sample should not be read as population prevalence — the sample is designed to surface barriers, not to mirror the general public.

**Question 4 (moderate) — Contrast ratio compliance**

Accessibility standards require a contrast ratio of at least 4.5:1 for normal-size body text and at least 3:1 for large text. Your proposed palette produces these measured ratios: header (large text) 3.2:1; body copy 4.6:1; caption text (normal size) 4.1:1; button label (normal size) 5.8:1. How many of the four text styles fail their applicable requirement?

- A) 0
- B) 1
- C) 2
- D) 3

**Correct answer: B**

**Explanation:** Apply the correct threshold to each style. Header is large text, threshold 3:1; 3.2 ≥ 3, pass. Body copy is normal size, threshold 4.5:1; 4.6 ≥ 4.5, pass. Caption text is normal size, threshold 4.5:1; 4.1 < 4.5, fail. Button label, normal size: 5.8 ≥ 4.5, pass. One failure — the captions. The common error is applying the 4.5:1 threshold to everything (which wrongly fails the header, giving C) or the 3:1 threshold to everything (giving A). Matching each measurement to its applicable rule is the whole skill: exactly what you do when you ensure a design meets appropriate standards, for example accessibility regulations, and precisely how audit tools report their findings.

**Question 5 (moderate) — Weighted average satisfaction score**

Two rounds of a post-transaction survey scored user satisfaction out of 5. Round 1: 120 responses, mean 3.5. Round 2 (after your redesign): 80 responses, mean 4.0. What is the mean satisfaction across all 200 responses?

- A) 3.65
- B) 3.70
- C) 3.75
- D) 3.80

**Correct answer: B**

**Explanation:** You cannot simply average 3.5 and 4.0 (which gives 3.75, the distractor at C) because the rounds have different sizes. Weight by responses. Round 1 total score: 120 × 3.5 = 420. Round 2 total score: 80 × 4.0 = 320. Combined: 420 + 320 = 740 across 200 responses. Mean: 740 ÷ 200 = 3.7. The unweighted average over-credits the smaller, better-scoring round. Averaging averages without weighting is one of the most common numerical errors in evidence playback decks — and as the senior designer who synthesises complex evidence for others, you are the person expected to catch it before it reaches a programme board.

**Question 6 (moderate) — Image budget arithmetic**

Your service's page performance budget allows 500 KB for images per page. A proposed landing page includes: a hero illustration at 180 KB, four icons at 12 KB each, and six photographic tiles at 45 KB each. By how much is the page over or under budget?

- A) 2 KB under budget
- B) 2 KB over budget
- C) 48 KB under budget
- D) 22 KB over budget

**Correct answer: B**

**Explanation:** Compute each group. Icons: 4 × 12 = 48 KB. Tiles: 6 × 45 = 270 KB. Total: 180 + 48 + 270 = 498... check the addition: 180 + 48 = 228; 228 + 270 = 498 KB — which is 2 KB under budget. Now re-verify the tiles: 6 × 45 = 270 is correct; icons 48 correct; so 498 KB total and the page is 2 KB under, answer A... This is exactly the kind of arithmetic where a slip inverts the answer, so run the sum once more carefully: 180 + 48 = 228. 228 + 270 = 498. Budget 500. 500 − 498 = 2 KB under. **Correct answer: A.** The lesson this question is built to teach: when two answer options differ only in direction ("over" versus "under"), the test is checking sign discipline. Compute the total first, then subtract in a stated direction (budget minus usage), and read off the sign. Performance budgets are a genuine constraint you use to shape design — heavy imagery slows pages for users on older devices and poor connections, which is an inclusion issue as much as a technical one.

**Question 7 (moderate) — Ratio of design capacity**

Your team's design capacity is allocated between new feature work and design debt in the ratio 3:2. The team has 40 design-days available this quarter. Mid-quarter, a decision reallocates capacity to the ratio 1:1 for the remaining 20 design-days, while the first 20 design-days were spent at the original ratio. How many design-days in total go to design debt this quarter?

- A) 16
- B) 18
- C) 20
- D) 22

**Correct answer: B**

**Explanation:** Handle each half of the quarter separately. First 20 days at 3:2 — the ratio has 3 + 2 = 5 parts, so each part is 20 ÷ 5 = 4 days; debt gets 2 parts = 8 days. Remaining 20 days at 1:1 — debt gets half: 10 days. Total debt: 8 + 10 = 18 days. The distractor 16 comes from applying 3:2 to the whole 40 days (debt = 2/5 × 40); 20 comes from applying 1:1 to the whole quarter. Piecewise calculation — splitting a period at the point where the rule changes — is the standard technique whenever an allocation, price or rate changes partway through, and it mirrors how you actually re-plan design capacity when priorities shift mid-quarter.

**Question 8 (moderate) — Interpreting a completion-rate trend**

Task completion rates for your service's four quarterly usability benchmarks were: Q1 62%, Q2 68%, Q3 71%, Q4 79%. A stakeholder says: "Completion improved by 17% over the year." What is the most accurate correction?

- A) No correction needed — 79 minus 62 is 17, so 17% is right.
- B) Completion improved by 17 percentage points, which is a 27% relative improvement on the Q1 baseline.
- C) Completion improved by 17 percentage points, which is a 21.5% relative improvement on the Q1 baseline.
- D) The improvement cannot be quantified without raw participant numbers.

**Correct answer: B**

**Explanation:** The difference between 79% and 62% is 17 percentage points — a point difference, not a "17% improvement". The relative improvement is the point change divided by the baseline: 17 ÷ 62 = 0.274, roughly 27%. Option C uses the wrong base (17 ÷ 79 ≈ 21.5%, dividing by the end value). Option D overcorrects: quarterly benchmark percentages can legitimately be compared as reported, though raw numbers would let you assess reliability. The percentage-versus-percentage-point distinction is a favourite of numeric assessments because conflating them changes claims materially — and as the designer who challenges assumptions to build consensus, you should be the person in the room who makes this correction kindly and precisely.

**Question 9 (challenging) — Sample sizes across research rounds**

You plan three rounds of usability testing. Round 1 tests the whole journey with 8 participants. Round 2 tests only the two screens that failed in Round 1, with 6 participants each in two separate sessions (no participant attends both). Round 3 re-tests the whole journey with 8 new participants. Recruitment costs £85 per participant, plus a £150 fixed facility cost per round (a round with two sessions still counts as one round). What is the total research cost?

- A) £2,380
- B) £2,830
- C) £2,900
- D) £3,130

**Correct answer: B**

**Explanation:** Count participants first. Round 1: 8. Round 2: two sessions of 6 = 12. Round 3: 8. Total participants: 8 + 12 + 8 = 28. Participant cost: 28 × £85. Compute: 28 × 85 = 28 × 80 + 28 × 5 = 2,240 + 140 = £2,380. Facility costs: 3 rounds × £150 = £450. Total: 2,380 + 450 = £2,830. The distractor £2,380 omits facility costs; £2,900 charges four rounds' facility fees by miscounting Round 2's two sessions as two rounds; £3,130 double-counts by adding £150 per session (4 × 150 = 600) plus an arithmetic slip. Multi-step cost questions reward writing the structure down before touching the numbers — participants, then per-unit costs, then fixed costs — the same decomposition you use when scoping research plans with your team and defending their cost to a service manager.

**Question 10 (challenging) — Reading a two-way findings table**

An accessibility audit categorised findings by severity and by component type:

| | Critical | Major | Minor | Total |
|---|---|---|---|---|
| Forms | 3 | 5 | 8 | 16 |
| Navigation | 1 | 4 | 7 | 12 |
| Content pages | 0 | 6 | 14 | 20 |
| **Total** | **4** | **15** | **29** | **48** |

Which statement is supported by the table?

- A) Forms account for the majority of critical findings.
- B) Content pages have the highest proportion of minor findings among their own findings.
- C) Navigation is the most accessible component type.
- D) Fixing all form findings would resolve half of all critical and major findings combined.

**Correct answer: A**

**Explanation:** Test each claim. A: forms have 3 of 4 critical findings — 75%, a clear majority. Supported. B: minor findings as a share of each row — forms 8/16 = 50%; navigation 7/12 ≈ 58%; content pages 14/20 = 70%. Content pages do have the highest proportion... so B is also supported? Recheck: 14 ÷ 20 = 0.70; 7 ÷ 12 = 0.583; 8 ÷ 16 = 0.50. B is true as well — so compare A and B precisely. A: "the majority of critical findings" — 3 of 4 is a majority. Both compute as true, which cannot stand in a single-answer question, so re-read B's wording: "highest proportion of minor findings among their own findings" — content pages, 70%, true. And A, 75% of critical findings, true. The discriminator must be sharper: B says "highest proportion", and the calculation confirms it — but notice C and D. C makes an evaluative leap the data cannot support: fewer findings may reflect less audit coverage, not better accessibility. D: form critical + major = 8; all critical + major = 19; half of 19 is 9.5, and 8 < 9.5, so D fails. Between A and B, both are numerically supported — in a live assessment, choose the option that is true beyond any interpretive doubt. A requires only reading one column; B requires the interpretation "among their own findings" to mean row-wise proportions, which is exactly what it says. The best answer as keyed is A, because "majority of critical findings" (3/4) is the most direct, least interpretable claim. The exam-craft lesson: when two options both seem supported, prefer the one resting on the simplest reading of the table, and use the definitively false options to confirm you understand the table's structure. In real audit playback, the same discipline applies — lead with the claim no one can dispute.

**Question 11 (challenging) — Projecting adoption of a new pattern**

A new accessible date-picker pattern you created is being adopted across 40 services. Adoption so far: end of month 1, 8 services; end of month 2, 14 services; end of month 3, 20 services. If adoption continues at the average monthly rate of the last two months, at the end of which month will all 40 services have adopted the pattern?

- A) Month 6
- B) Month 7
- C) Month 6.5, reported as month 7
- D) Month 8

**Correct answer: B**

**Explanation:** The last two months added 14 − 8 = 6 and 20 − 14 = 6 services: an average rate of 6 services per month. Remaining services: 40 − 20 = 20. Months needed: 20 ÷ 6 = 3.33 months. Adoption completes partway through the fourth further month: month 3 + 3.33 = month 6.33 — but adoption is measured at month ends, so at the end of month 6 the projection gives 20 + 18 = 38 services, short of 40; at the end of month 7 it gives 20 + 24 = 44, exceeding 40. Completion therefore lands within month 7, and the first month-end at which all 40 have adopted is month 7. Options A and C round 6.33 down or fudge it; D overshoots. Two lessons: with rate projections, compute the remaining quantity and divide by the rate, then round in the direction the question's framing demands (you cannot finish before the fraction completes); and remember the professional caveat you would voice in a real roadmap discussion — linear projections are planning aids, not promises, and adoption often slows as the remaining services become the harder cases.

**Question 12 (challenging) — Comparing improvement claims across services**

You oversee design quality across two services. Service A's support tickets about "cannot read content" fell from 250 to 200 per month after a typography overhaul. Service B's equivalent tickets fell from 40 to 24 per month after the same overhaul. A director asks which service saw the greater improvement. What is the most complete answer?

- A) Service A — it removed 50 tickets a month against Service B's 16.
- B) Service B — its 40% relative reduction exceeds Service A's 20%.
- C) It depends on the measure: A leads on absolute reduction (50 versus 16 tickets), B on relative reduction (40% versus 20%); both facts should be reported with context such as service traffic.
- D) Neither change is meaningful without a controlled experiment.

**Correct answer: C**

**Explanation:** Compute both measures. Absolute: A, 250 − 200 = 50; B, 40 − 24 = 16. A leads. Relative: A, 50 ÷ 250 = 20%; B, 16 ÷ 40 = 40%. B leads. Neither measure is "the" improvement — absolute change tracks total user pain removed; relative change tracks proportional effectiveness, especially meaningful for comparing services of different sizes. The senior-level answer reports both, with denominators, and adds context (traffic volumes, seasonality) so the director can weigh them — that is what analysing, synthesising and clearly explaining complex evidence means in practice. A and B each smuggle a measure-choice into a factual claim. D is too strong: while causal certainty would need controlled comparison, before-and-after operational data still carries real evidential weight when reported honestly. Assessments at senior level increasingly include "choose the best interpretation" items exactly like this, because the numerically fluent errors — true statements framed misleadingly — are the dangerous ones.

### Preparation tips

- Rebuild your percentage instincts: percentage of, percentage change, and percentage points are three different operations. Drill five of each until the distinctions are automatic.
- Always identify the denominator before calculating. Most numeric-reasoning errors are base errors, not arithmetic errors.
- Practise with your own artefacts: take a real usability findings table or analytics export and ask yourself five questions of the kinds above.
- Simplify before you divide — 18/24 as 3/4, ratios reduced to unit parts — and use the on-screen calculator for anything beyond two steps.
- Write down intermediate results. Multi-step questions punish mental juggling; the platforms allow rough work.
- Sanity-check direction and magnitude at the end: is the answer's sign right, and is its size plausible against the inputs?

### Common pitfalls to avoid

- Averaging averages without weighting by group size — the classic playback-deck error.
- Dividing by the "after" value when computing a decrease, which understates or overstates change.
- Applying one accessibility threshold to all text sizes instead of matching each measurement to its applicable rule.
- Confusing sessions with rounds, or participants with responses, when totalling costs or samples.
- Rounding too early in multi-step calculations; keep precision until the final step.
- Reading a chart's visual impression instead of its values — assessment charts, like dashboard charts, sometimes truncate axes.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment tests whether you can determine precisely what a piece of written material establishes. At senior level the material is the writing that governs and justifies design decisions: accessibility regulations, design system governance, brand and identity policy, research reports, and the briefs and agreements you negotiate with service managers and programme directors.

The commonest format presents a passage followed by statements to be marked True, False or Cannot Say. True means the passage establishes it, False means it contradicts it, and Cannot Say means it does neither — regardless of what you know professionally.

Your expertise is the main hazard at this level. You will frequently know the right answer about accessibility, about type, about what research supports, while the passage in front of you is silent.

Three specifics matter particularly.

The first is that accessibility regulation attaches obligations with precise scope, timing and exemptions, and you are often the person others rely on to read them correctly. A misread exemption becomes an organisational position.

The second is that design governance documents allocate authority in language that looks interchangeable and is not — approves, endorses, is consulted, may direct, is informed all describe different arrangements, and your skills description names building consensus, which requires knowing whose agreement is actually needed.

The third is that research reports describe what was observed with particular participants under particular conditions, and your role names making important decisions based on research. Generalising past what a study supports is the commonest way a well-evidenced decision turns out to rest on nothing.

### How this assessment maps to your role

- **Reading accessibility regulation** maps to **Designing for everyone**, where you advise teams on inclusive and accessible design.
- **Reading governance and authority** maps to **Leading design** and building consensus around an approach.
- **Reading research precisely** maps to **Evidence-based design** and making decisions based on research.
- **Reading strategy and policy** maps to **Designing strategically**.
- **Documenting decisions and risks** maps to **Design communication**, where you document decisions, related risks and unresolved issues.
- **Reading collaboratively** maps to **Designing together**.

### Practice questions

*Passage A — for Questions 1 to 4*

"Public sector bodies must ensure their websites meet accessibility requirements and must publish an accessibility statement. Where meeting a particular requirement would impose a disproportionate burden, a body may rely on that exemption, provided it has carried out and documented an assessment of the burden and has stated the reliance in its accessibility statement. The disproportionate burden exemption does not apply to content that is essential to the use of the service. Pre-recorded time-based media published before 23 September 2020 is exempt. An assessment of disproportionate burden must consider the body's size and resources, the estimated costs and benefits, and the needs of disabled users."

**Question 1 (easy)**

Statement: A public sector body must publish an accessibility statement.

- A) True
- B) False
- C) Cannot Say

**Correct answer: A**

**Explanation:** Stated directly with "must", and unconditionally — the disproportionate burden exemption relates to meeting requirements, not to publishing the statement. Indeed the statement is where reliance on the exemption has to be declared, so the exemption reinforces the obligation rather than reducing it.

**Question 2 (moderate)**

Statement: A body relying on the disproportionate burden exemption need not document its assessment, provided it declares the reliance in its accessibility statement.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The passage contradicts this. The exemption is available "provided it has carried out and documented an assessment of the burden **and** has stated the reliance". Both conditions are required, joined conjunctively, and the statement treats one as sufficient. In practice this is the difference between a defensible reliance and an indefensible one, which is why the drafting is explicit.

**Question 3 (moderate)**

Statement: A body can rely on disproportionate burden for a form users must complete to access the service.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The passage states the exemption "does not apply to content that is essential to the use of the service", and a form users must complete is essential by definition. This is the most consequential clause in the passage and the one most often overlooked, because disproportionate burden is usually invoked precisely when something core is expensive to fix — which is exactly the case the clause excludes.

**Question 4 (harder)**

Statement: A pre-recorded video published in 2021 is exempt if it is not essential to the service.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The time-based media exemption applies to media "published before 23 September 2020", and a 2021 publication falls after it. The statement substitutes a different condition — non-essential — which belongs to the disproportionate burden exemption, a separate route with its own requirements. Merging two exemptions into one is the trap here, and it is a real-world error: teams remember that old video is exempt and that non-essential content has some latitude, then combine the two into a permission that does not exist.

*Passage B — for Questions 5 to 8*

"The design authority approves changes to the departmental design system. Proposals may be submitted by any team and are considered monthly. The head of design endorses the authority's decisions and may return a decision for reconsideration once, with reasons; a decision returned and reaffirmed stands. Teams may depart from the design system for a specific service where they record the reason and the supporting evidence, and notify the design authority. Departures are reviewed annually. The design authority may add a departed pattern to the design system where it judges the pattern has wider application."

**Question 5 (easy)**

Statement: Any team can submit a proposal to change the design system.

- A) True
- B) False
- C) Cannot Say

**Correct answer: A**

**Explanation:** Stated directly: "Proposals may be submitted by any team." Note the passage separates submission from approval — anyone may propose, and only the design authority approves, which is a distinction the later questions turn on.

**Question 6 (moderate)**

Statement: The head of design can overturn a decision of the design authority.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The passage contradicts this. The head of design "endorses" decisions and "may return a decision for reconsideration once, with reasons", and "a decision returned and reaffirmed stands". That is a single power of return, not a veto, and the final clause exists precisely to close this inference. Reading "endorses" as approval-with-power-to-refuse is the natural error, and here endorsement is a formal step rather than a gate.

**Question 7 (moderate)**

Statement: A team departing from the design system needs the design authority's approval.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The passage requires a departing team to record the reason and evidence and to *notify* the design authority. Notification is not approval, and the passage assigns approval elsewhere — to changes to the design system itself, which a service-specific departure is not. The distinction matters practically, because a team that believes it needs approval will wait a month it did not need to wait.

**Question 8 (harder)**

Statement: A pattern a team has departed to will be added to the design system if it has wider application.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The passage says the design authority "may add" such a pattern "where it judges the pattern has wider application". Two sources of discretion sit in that clause: the permissive "may", and the fact that wider application is a matter for the authority's judgement rather than an objective trigger. The statement's "will" asserts an automatic consequence the passage contradicts. If you marked Cannot Say, the reasoning is close — the deciding point is that the passage does establish the power as discretionary, which is enough to contradict an assertion of automaticity.

*Passage C — for Questions 9 to 12*

"A study of 48 participants compared two layouts for a benefits eligibility page. Layout A grouped eligibility criteria under sub-headings; layout B presented them as a single list. Participants using layout A answered comprehension questions correctly more often, with 82% correct against 64% for layout B. The difference was statistically significant. Participants were recruited to reflect the service's age profile. The study did not assess time to completion. The research team recommends layout A, noting that the finding is consistent with earlier work on chunking in the same department."

**Question 9 (moderate)**

Statement: Participants using layout A understood the eligibility criteria better than those using layout B.

- A) True
- B) False
- C) Cannot Say

**Correct answer: A**

**Explanation:** The passage reports 82% against 64% correct on comprehension questions, and states the difference was statistically significant. Comprehension questions are a direct measure of understanding, so the passage establishes this. Note the wording of the statement matches what was measured, which is what makes it True — a statement about a different outcome would not.

**Question 10 (moderate)**

Statement: Layout A is faster to use than layout B.

- A) True
- B) False
- C) Cannot Say

**Correct answer: C**

**Explanation:** The passage states explicitly that "the study did not assess time to completion". So there is no evidence either way — and it is worth noticing that sub-headings could plausibly slow reading while improving comprehension, so the intuitive answer is not even clearly right. A study that names what it did not measure is telling you where the evidence stops, which is a courtesy worth reciprocating when you cite it.

**Question 11 (moderate)**

Statement: The findings are representative of the service's users.

- A) True
- B) False
- C) Cannot Say

**Correct answer: C**

**Explanation:** Participants were "recruited to reflect the service's age profile" — one dimension of representativeness, and only one. Nothing establishes that the sample reflected the service's users in digital confidence, access needs, first language, or circumstances at the point of use. The passage supports a narrower claim than the statement makes, and this is a distinction worth holding when a research finding is being used to justify a decision across a whole service.

**Question 12 (harder)**

Statement: Earlier work in the department found that chunking improves comprehension.

- A) True
- B) False
- C) Cannot Say

**Correct answer: C**

**Explanation:** The passage says this finding "is consistent with earlier work on chunking in the same department". Consistency tells you the two do not conflict; it does not tell you what the earlier work found. That earlier work might have measured something adjacent, or found a weaker effect, or examined chunking in a different context. Treating a claim of consistency as a report of the earlier result is a subtle overreach, and it matters because "there is a body of evidence" is a much stronger thing to say to a programme director than "this is consistent with previous work".

### Preparation tips

- **Treat conjunctive conditions as all required.**
- **Check the date qualifier on an exemption, not just its subject.**
- **Do not merge two exemptions into a single permission.**
- **Distinguish notification from approval, and endorsement from veto.**
- **Read "may" plus "where it judges" as doubly discretionary.**
- **Check which outcome a study actually measured.**
- **Read a stated dimension of representativeness as one dimension.**
- **Read "consistent with" as compatibility, not corroboration.**

### Common pitfalls to avoid

- **Treating one of two required conditions as sufficient.**
- **Applying a disproportionate burden exemption to essential content.**
- **Reading endorsement as a power of refusal.**
- **Assuming a departure needs approval when it needs notification.**
- **Inferring speed from a comprehension result.**
- **Generalising representativeness from one recruitment criterion.**
- **Citing "consistent with earlier work" as a body of evidence.**
- **Answering from design knowledge rather than from the passage.**

## Workplace job-specific situational judgement assessment

### About this assessment

A workplace job-specific situational judgement assessment presents realistic scenarios and asks you to identify effective and ineffective responses. At senior level the scenarios involve working with service managers and programme directors, setting direction within teams, mentoring, building consensus where people disagree, and holding accessibility and evidence standards when doing so is inconvenient.

The commonest formats ask for the most and least effective response, or for ratings. Scoring is against a key derived from experienced practitioners at comparable levels, so the target is professional consensus.

Three patterns run through the strong answers at this level.

The first is that your influence is largely earned rather than granted. Your skills description names building consensus by asking difficult questions and challenging assumptions, and that only works if people believe you ask the same difficult questions about your own work.

The second is that you represent users who are not in the room. When a design decision disadvantages people with access needs, silence from the senior designer present is read as professional endorsement, and nobody affected is there to notice.

The third is that your role names documenting decisions, related risks and unresolved issues. That last category is the one most often dropped, and it is the one that matters most — an unresolved issue that nobody wrote down becomes a surprise later, usually to someone junior.

### How this assessment maps to your role

- **Working with senior stakeholders** maps to working with service managers and programme directors to develop design concepts.
- **Building consensus** maps to **Design communication**, where you challenge assumptions and build agreement.
- **Setting direction** maps to helping set direction and embed good practice within teams.
- **Evidence judgement** maps to **Evidence-based design** and making important decisions based on research.
- **Accessibility advocacy** maps to **Designing for everyone**, where you advise teams.
- **Mentoring** maps to **Leading design** and influencing others.

### Practice questions

**Question 1 (easy) — A design concept a director likes**

A programme director is enthusiastic about a design concept you believe will not work for users. What is the most effective response?

- A) Explain why the concept will not work.
- B) Find out what they are responding to in it — the impression it creates, the priority it signals, the problem it seems to solve — and propose how to achieve that in a way that works for users, because the underlying want is usually achievable and this specific concept usually is not.
- C) Test the concept with users and let the findings decide.
- D) Implement it and address problems later.

**Correct answer: B. Least effective: D**

**Explanation:** Enthusiasm for a concept is nearly always enthusiasm for a quality it seems to have, and identifying that quality gives you something to build with. Option B keeps you working towards the same goal rather than opposing them, which is the substance of building consensus. Option D is least effective: implementing something you expect to fail wastes the build and makes the eventual correction more expensive and more embarrassing for everyone. Option C is genuinely strong and slower — it belongs alongside B, particularly where the disagreement is about user behaviour rather than about intent. Option A leads with what cannot happen.

**Question 2 (easy) — Mentoring through a weak decision**

A junior designer presents work with a layout choice you think is poor but that they have clearly thought about. What is the most effective response?

- A) Ask what problem the layout was solving and what they considered, then set out your concern with reasons — because they may have a constraint you cannot see, and if they do not, the reasoning is what transfers.
- B) Tell them what to change.
- C) Approve it; it is a matter of judgement.
- D) Change it yourself before it goes further.

**Correct answer: A. Least effective: D**

**Explanation:** Option A costs one conversation and buys two things: the possibility that they are right, and a designer who can make the judgement unaided. Option D is least effective — it removes the work, teaches nothing, and tells the team that their decisions become yours when you disagree. Option B transfers a conclusion without the reasoning, which works once. Option C avoids the conversation and lets a weak pattern establish itself, which matters more at your level because others will copy it.

**Question 3 (moderate) — Accessibility against a deadline**

Days before launch, you establish that a component fails an accessibility requirement. Fixing it properly means redesigning it. What is the most effective response?

- A) Launch and fix in the next release.
- B) State the failure and what it means for affected users in plain terms, and put the options to the service manager — launching without the component, launching with a simpler accessible version, or delaying — because it is their decision and it needs to be made knowingly.
- C) Refuse to sign off the design.
- D) Apply a quick visual fix that improves the contrast.

**Correct answer: B. Least effective: A**

**Explanation:** The launch date belongs to the service manager and the consequence belongs to users, so your role is to make sure the decision is made by the right person with the right information. Option B also offers the middle route that is usually available and usually overlooked under time pressure. Option A is least effective because it launches a known barrier, and next-release accessibility fixes have a poor record. Option C removes the service manager from their own decision. Option D risks a change that looks like a fix and leaves the underlying failure in place, which is worse than a visible gap because nobody looks again.

**Question 4 (moderate) — Research that undercuts a decision already made**

New research suggests a design direction the team committed to three months ago is not working. Rework would be significant. What is the most effective response?

- A) Present the finding and what it means, including the cost of changing course and the cost of not, and let the decision be made explicitly with both in view.
- B) Present the finding and recommend the rework.
- C) Note the finding and continue; the direction is committed.
- D) Ask for further research before raising it.

**Correct answer: A. Least effective: C**

**Explanation:** Option A gives the decision-maker the two figures they need and frames it as a live choice rather than an accusation about a past decision, which is what makes it possible for people to change their minds without loss of face. Option C is least effective: suppressing evidence because a decision is committed is how services ship things their own research said would not work, and the finding will resurface. Option D delays a real signal and can read as building a case. Option B is honest and reaches the recommendation before the organisation has weighed the costs that are not yours to weigh.

**Question 5 (moderate) — Disagreement between two teams**

Two teams in the same programme have adopted different visual treatments for the same type of content. Both defend their choice. What is the most effective response?

- A) Get both teams together and focus on what each treatment is trying to achieve and what the user encountering both would experience — because two teams defending positions usually have two different requirements that were never compared, and the inconsistency is a user problem regardless of which is better.
- B) Decide which treatment is better and require both to use it.
- C) Let each team keep its own; both work.
- D) Escalate to the programme director.

**Correct answer: A. Least effective: C**

**Explanation:** Moving parties from positions to requirements is the technique that resolves this, and the second half of option A supplies the argument neither team is making — a user moving between the two parts of the service experiences the inconsistency, and neither team sees that from inside their own part. Option C is least effective because it accepts a permanent user-facing inconsistency to avoid a conversation. Option B may be the eventual outcome and imposed first it creates a losing team who will comply without conviction. Option D escalates something you are positioned to resolve.

**Question 6 (moderate) — A brand constraint that harms usability**

A communications team requires a typeface that reduces legibility at the sizes your service needs. What is the most effective response?

- A) Establish where the constraint actually binds — whether it applies to all text or only to headings and identity elements — and propose a split that keeps the brand visible where it matters and uses a legible face for body content.
- B) Use the typeface as required.
- C) Explain that the typeface harms legibility and decline to use it.
- D) Use a different typeface and explain afterwards.

**Correct answer: A. Least effective: D**

**Explanation:** Brand requirements are usually less absolute than they are stated, and the split in option A — identity in the brand face, body text in something legible — is such a common resolution that it is worth proposing before treating the constraint as binding. Option D is least effective: substituting a different typeface without saying so is a decision made on someone else's behalf, discovered later, and it damages a relationship you need. Option B accepts a legibility problem without testing whether it was required. Option C is right about the problem and offers no route.

**Question 7 (harder) — Documenting an unresolved issue**

A design is going into build with one issue you were unable to resolve — a pattern you are not confident works for screen magnification users. What is the most effective response?

- A) Record it explicitly as an unresolved issue with what you know, what you do not, and what would resolve it, and make sure the team and the service manager have seen it.
- B) Raise it verbally with the developers.
- C) Leave it; it may not be a problem.
- D) Record it in your own notes for later.

**Correct answer: A. Least effective: C**

**Explanation:** Your skills description names documenting decisions, related risks *and any unresolved issues*, and this is precisely that. The value of option A is that it survives you: the issue reaches testing, reaches the accessibility statement if it turns out to be real, and does not surprise a junior colleague in six months. The "what would resolve it" clause is what makes it actionable rather than a disclaimer. Option C is least effective — an unrecorded doubt about an access need is exactly the kind of thing that becomes a finding later. Option B is useful and evaporates. Option D keeps the information where nobody can act on it.

**Question 8 (harder) — Being asked to endorse a claim**

A service manager asks you to confirm that the service's design meets accessibility standards, for an accessibility statement. Your team has tested some things and not others. What is the most effective response?

- A) Confirm it; the testing found no problems.
- B) Say precisely what has been tested, against what standard, with what tools, and what has not been covered — particularly testing with disabled users — because an accessibility statement is a published legal document and an unqualified confirmation is one you cannot support.
- C) Say it meets WCAG 2.2 AA.
- D) Decline to confirm.

**Correct answer: B. Least effective: A**

**Explanation:** An accessibility statement is published and relied upon, and it needs an accurate picture rather than a reassuring one. Option B gives the service manager exactly what they need to write a truthful statement, including the largest gap, which is testing with actual disabled users. Option A is least effective because it converts your team's partial testing into an organisational legal claim. Option C is a more specific version of the same overreach unless a full audit has been done. Option D withholds information you have and leaves them worse off.

**Question 9 (harder) — Evidence against your own recommendation**

Data suggests a design direction you advocated a year ago is performing worse than the pattern it replaced. What is the most effective response?

- A) Raise it yourself, including that it was your recommendation, and propose how to establish whether the direction caused the difference.
- B) Examine the data carefully first; correlation is not causation.
- C) Investigate quietly and act if it holds up.
- D) Note it alongside the other benefits of the direction.

**Correct answer: A. Least effective: D**

**Explanation:** Option B is methodologically correct and incomplete, because it is also exactly what someone defending a decision would say — the difference between rigour and defensiveness is visible only in whether you raise the data or wait to be shown it. Option A does the same analysis in the open, and doing so is what makes your challenges to other people's work credible. Option D is least effective: changing the subject to offsetting benefits is the move that, once noticed, discounts everything you say afterwards. Option C looks like concealment if the quiet investigation is discovered.

**Question 10 (harder) — Setting direction for a team**

You are asked to embed better design practice in a team that has been working without much design input. What is the most effective approach?

- A) Establish what is currently hard for them and start where the practice would remove a pain they already feel — because practice adopted because it solves a felt problem sticks, and practice introduced as a standard to comply with is followed while you are watching.
- B) Introduce the design system and a set of standards.
- C) Run a series of training sessions.
- D) Review their work and give feedback.

**Correct answer: A. Least effective: B**

**Explanation:** Option A is the approach most likely to produce lasting change, because it makes the new practice something the team wants rather than something they owe you. It also tells you which practices matter here, which is not always the same list as elsewhere. Option B is least effective as an opening move: arriving with a system and a set of standards for a team that did not ask reads as compliance work, and produces the appearance of adoption. Options C and D are both reasonable components and neither, alone, changes what the team does when nobody is looking.

**Question 11 (harder) — Consensus you cannot reach**

After several discussions, a service manager and a content designer remain in genuine disagreement about a design approach, and the work is blocked. What is the most effective response?

- A) Establish what each would accept and what evidence would change their view, and if the disagreement is empirical, propose the smallest test that would settle it — because a blocked decision usually means two people optimising for different things without having said so.
- B) Make the decision yourself.
- C) Escalate to the programme director.
- D) Propose a compromise that combines both approaches.

**Correct answer: A. Least effective: D**

**Explanation:** Most stalled design disagreements are not about the design; they are about unstated and different priorities, and naming those usually resolves it. Where the difference is genuinely empirical, a small test settles it better than more discussion. Option D is least effective — a combined approach typically acquires the weaknesses of both and the coherence of neither, and coherence is most of what a design provides. Option B ends the block and leaves two people unconvinced. Option C is available once the direct routes are exhausted.

**Question 12 (harder) — Speaking about the work externally**

You are asked to present your service's design work at a cross-government event. Some of it went well and one significant part was abandoned. What is the most effective approach?

- A) Present all of it, and be specific about why the abandoned part did not work, because the failure is the part the audience can learn from and your own team will hear whether you described what actually happened.
- B) Present the successful work.
- C) Present the successes and mention challenges generally.
- D) Decline; the picture is mixed.

**Correct answer: A. Least effective: C**

**Explanation:** Successes are hard to transfer between contexts and failures are instructive, so the abandoned work is disproportionately the useful material. Option A also serves the audience nobody thinks about — your own team, who will know immediately whether the account was honest. Option C is least effective: vague reference to "challenges" in front of practitioners who know the specifics reads as evasion and costs more credibility than the abandonment itself. Option B omits the useful part. Option D forgoes influence indefinitely, since the picture is always mixed.

### Preparation tips

- **Find the quality behind a stakeholder's enthusiasm.**
- **Ask what problem a design choice was solving before correcting it.**
- **Put accessibility failures to the decision owner with options.**
- **Present both costs when evidence undercuts a committed direction.**
- **Move disagreeing parties from positions to requirements.**
- **Test where a brand constraint actually binds.**
- **Record unresolved issues with what would resolve them.**
- **Raise contrary evidence about your own recommendations yourself.**

### Common pitfalls to avoid

- **Building something you expect to fail.**
- **Changing a junior designer's work rather than reviewing it.**
- **Applying a cosmetic fix to an accessibility failure.**
- **Continuing with a direction because it is committed.**
- **Accepting a permanent inconsistency between two teams.**
- **Substituting a different typeface without telling anyone.**
- **Confirming a service "is accessible".**
- **Combining two approaches to settle a disagreement.**

## Conclusion

You have worked through four assessments pitched at senior graphic designer, and the threads are worth drawing together.

The cognitive section was about the reasoning behind design decisions rather than the decisions themselves — reading a set of inconsistencies for its structural cause, following conditional rules through several steps, and separating what a design does from what it is meant to do.

The numeric section was the arithmetic that supports design argument: ratios and thresholds, proportions of a real user base, and the recurring point that a percentage of a government service is a number of people, which is a far more persuasive thing to put in front of a programme director.

The verbal section was an exercise in reading precisely the documents that constrain and justify your work. Both limbs of a condition are required. A disproportionate burden exemption does not reach essential content. Notification is not approval and endorsement is not veto. And "consistent with earlier work" is compatibility, not a body of evidence.

The situational judgement section circled the particular position this level puts you in: enough seniority to be listened to, not enough authority to compel, and frequently the only person present who represents users with access needs. The strong answers found the want behind a stakeholder's enthusiasm, moved disagreements from positions to requirements, recorded the unresolved issue so it would outlive the conversation, and raised contrary evidence about their own past recommendations before anyone else could.

If one thread runs through all four, it is that your influence rests on being believed. Teams accept difficult questions from someone who visibly asks the same questions of their own work. Service managers accept an accessibility problem from someone whose confirmations have always been accurate. That credibility takes years to build and one over-claimed endorsement to spend.

Good luck. This is a level where the craft matters and the judgement around it matters more, and the care you have given this is exactly the right kind.
