# Senior Business Analyst - Psychometric Assessment Resources

## Introduction

Welcome! This guide has been created especially for you as a senior business analyst working within the UK Government Digital and Data profession. Whether you are preparing for an internal assessment, applying for a new post, benchmarking your own capability, or simply curious about how psychometric assessments relate to your day-to-day work, this document will help you practise, reflect, and build confidence.

Psychometric assessments are structured, standardised exercises that measure the mental capabilities and behavioural tendencies that predict success in a role. For a senior business analyst, that means far more than abstract puzzles. The assessments described here are job-specific: they use the kinds of artefacts you genuinely handle — process models, requirements catalogues, options appraisals, acceptance criteria, stakeholder communications plans, and user research findings — and the kinds of decisions you genuinely make, such as leading the modelling of business processes across a programme, coordinating the prioritisation of requirements, advising on approaches to testing, and negotiating delivery priorities with stakeholders whose interests do not always align.

Why do these assessments matter for your role in particular? As a senior business analyst you lead large or complex projects, and you carry responsibilities beyond your own analysis: you mentor others, develop best practice, own stakeholder relationships, and manage community of practice activities within your business area. That combination places a premium on exactly the capabilities psychometric assessments measure. Cognitive ability underpins your work decomposing problems, spotting inconsistencies between artefacts, and reasoning about root causes. Numerical reasoning underpins your work with performance baselines, process metrics, benefits estimates, and prioritisation trade-offs. Verbal reasoning underpins your work reading policy constraints, standards, and dense stakeholder correspondence with precision — and writing requirements that cannot be misread. Situational judgement underpins the leadership dimension of your level: choosing the most effective course of action when a stakeholder pushes back, a mentee struggles, or a delivery deadline collides with analytical rigour.

This document is organised into four main assessment sections, each following the same pattern: an overview of what the assessment measures and why employers use it for your role, a mapping of the assessment's dimensions to the specific skills in the senior business analyst capability framework, a substantial set of practice questions with full worked explanations, practical preparation tips, and common pitfalls to avoid.

Here is how to get the most from it. First, read each "About this assessment" section so you understand the format before you meet it under timed conditions. Second, attempt every practice question honestly — commit to an answer before reading the explanation, because the act of committing is what builds judgement. Third, treat every explanation as a mini-lesson: even when you answer correctly, the worked reasoning will sharpen your technique and often connects the question back to a skill you use every week. Finally, use the preparation tips and pitfalls sections for self-reflection: they connect assessment performance back to your professional development as an analyst who leads complex work and develops others.

Take your time, be kind to yourself, and enjoy the practice. Let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive ability assessment measures the exact mental processes your role demands, using practical workplace scenarios rather than abstract puzzles. Unlike a generic intelligence test, it presents you with the everyday materials of your job — in your case, process maps, requirements traceability matrices, data models, options appraisals, test plans, and prioritisation frameworks — and asks you to reason quickly and accurately about them.

Typical format: an online, timed test lasting 15 to 30 minutes, with questions covering pattern recognition, logical deduction, error checking, prioritisation, and applied problem solving. Scoring is objective, comparing your responses against a norm group, and modern platforms often adapt question difficulty based on your previous answers — getting a question right tends to make the next one harder, so do not be alarmed if the test feels progressively more demanding. Employers usually receive a breakdown of speed versus accuracy rather than a single score, so working both quickly and carefully matters. You will normally be offered short, ungraded practice questions before the real test begins, so you can get comfortable with the interface without pressure.

For a senior business analyst, cognitive ability assessment is particularly relevant because structured thinking is the core of your professional value. You are the person a programme trusts to understand how a business area really works — its people, organisation, processes, information, data and technology — and to hold that understanding steady while everything around it changes. That requires keeping many moving parts in mind at once: which requirements trace to which business needs, which process changes affect which teams, where a proposed solution contradicts a policy constraint, and what follows logically when one assumption in an options appraisal turns out to be false. Because you lead complex projects and review the work of others, employers also want evidence that you can detect subtle errors in artefacts you did not create yourself. A well-designed cognitive assessment simulates precisely those demands in miniature.

### How this assessment maps to your role

The assessment dimensions map directly to the named skills in your role profile:

- **Pattern recognition** maps to **Business modelling** and **Systems analysis**: leading the modelling of processes, systems and data at varying levels of complexity means recognising recurring structures — duplicated process steps, common data flows, repeated hand-offs — across large and messy information sets, and spotting where a model deviates from its own conventions.
- **Logical deduction** maps to **Context, problem and option analysis**: leading the approach to understanding context, problems and root causes requires you to reason validly from evidence to conclusions, and to evaluate multiple options without deducing more than the evidence supports.
- **Error checking** maps to **Requirements definition and management** and **Testing (business analysis)**: ensuring requirements can be traced through design, build, test, tender and evaluation phases, and reviewing prototypes, test plans and test outcome reports, both depend on spotting inconsistencies between artefacts quickly and reliably.
- **Prioritisation** maps to **Adapting to delivery methodologies** and **Requirements definition and management**: negotiating and agreeing delivery priorities with the team and stakeholders, and coordinating the prioritisation of requirements, both require rapidly ranking what matters most under competing pressures.
- **Applied problem solving** maps to **Business process improvement** and **User experience analysis**: leading process analysis to define performance problems and opportunities, and analysing how user experience needs affect system design, both mean decomposing tangled situations into parts you can reason about and recombine into recommendations.

### Practice questions

**Question 1 (easy) — Pattern recognition in a requirements catalogue**

Your programme's requirements catalogue uses a fixed identifier convention: functional requirements are labelled FR-nnn, non-functional requirements NFR-nnn, and business rules BR-nnn, where nnn is a three-digit number allocated sequentially within each type. Reviewing a junior analyst's latest additions, you see:

1. FR-041: The caseworker can reassign a case to another team.
2. NFR-012: Case search results must return within 2 seconds.
3. FR-13: The applicant receives an email confirmation on submission.
4. BR-007: An application older than 12 months is archived.

Which entry breaks the catalogue's convention?

- A) Entry 1
- B) Entry 2
- C) Entry 3
- D) Entry 4

**Correct answer: C**

**Explanation:** The convention requires a three-digit number, so the thirteenth functional requirement must be written FR-013, not FR-13. Entries 1, 2 and 4 all follow the pattern for their type. This looks trivial, but identifier discipline is what makes traceability work: automated tools, test scripts and traceability matrices match on exact identifiers, and "FR-13" will silently fail to link to test cases referencing "FR-013". As the senior analyst who develops best practice and reviews others' work, you are the person expected to catch this before the catalogue is baselined — and to explain to the junior analyst why it matters, rather than just fixing it silently.

**Question 2 (easy) — Logical deduction from a policy constraint**

A policy constraint on your service states: "An application may be fast-tracked only if the applicant has provided verified identity evidence." A caseworker tells you: "This application has verified identity evidence." Which one of the following conclusions must be true?

- A) The application will be fast-tracked.
- B) The application is eligible to be considered for fast-tracking, so far as this constraint is concerned.
- C) The application meets all fast-track criteria.
- D) The application would have been rejected without the evidence.

**Correct answer: B**

**Explanation:** The constraint states a necessary condition, not a sufficient one: verified identity evidence is required for fast-tracking, but nothing says it guarantees fast-tracking, so A overreaches. C overreaches further — other criteria may exist that the constraint does not mention. D confuses fast-track eligibility with rejection of the whole application; an application without verified identity evidence simply cannot be fast-tracked, which is not the same as being rejected. Only B confines itself to what the constraint guarantees. This "necessary versus sufficient" distinction is one of the most common traps in cognitive testing, and one of the most common sources of defects in requirements: analysts who write "only if" when they mean "if" (or vice versa) create business rules that behave very differently from what policy intended. Understanding business and policy constraints, and assessing their implications precisely, is a core duty of your role.

**Question 3 (easy) — Error checking a process model**

A swim-lane process model for a grant application shows four steps: (1) Applicant submits form; (2) Caseworker validates form; (3) If invalid, caseworker returns form to applicant with reasons; (4) Finance officer schedules payment. A colleague asks you to review it before a stakeholder walkthrough. What is the most significant structural gap?

- A) The model does not name the software system used at each step.
- B) There is no path showing what happens when the form is valid, between validation and payment scheduling.
- C) The applicant lane should come after the caseworker lane.
- D) Step 3 should be worded in passive voice for consistency.

**Correct answer: B**

**Explanation:** Walk the happy path: the applicant submits, the caseworker validates, and then — as drawn — the only labelled outcome is the invalid case. The model jumps from validation to payment scheduling without any step showing approval or a decision outcome for a valid form, which means the most common path through the process is undocumented. Option A describes useful enrichment, not a structural gap; C is cosmetic (lane order is a presentation choice); D is a style preference, and active voice is generally clearer anyway. Reviewing models for logical completeness — does every decision point have all its outcomes? does the happy path actually reach the end? — is central to leading the modelling of business processes at varying levels of complexity, and catching the gap before the stakeholder walkthrough protects the credibility of the whole analysis.

**Question 4 (moderate) — Prioritisation across a senior analyst's week**

It is Monday morning. Four items compete for your attention:

1. The programme board meets Wednesday and needs your options appraisal for a critical build-versus-buy decision; without it, the decision slips a month to the next board.
2. A junior analyst you mentor has asked you to review their first process improvement proposal before they present it to their business unit on Friday.
3. A senior stakeholder has emailed overnight, unhappy that a requirement she considers vital has been deprioritised in the current release; no meeting is booked, but her tone is sharp.
4. Your business area's community of practice session is in two weeks and you have not yet drafted the agenda.

Which sequencing is most defensible?

- A) 3, 1, 2, 4 — an unhappy senior stakeholder always comes first
- B) 1, 3, 2, 4 — board-blocking appraisal first, then a same-day holding response to the stakeholder, then the mentee, then the agenda
- C) 1, 2, 3, 4 — strict deadline order
- D) 2, 1, 3, 4 — developing others always comes first

**Correct answer: B**

**Explanation:** Prioritisation questions reward reasoning about impact and urgency together, not applying a single rule. Item 1 is both urgent (Wednesday) and high impact: a slipped board decision delays the programme a full month. Item 3 is genuinely important — you own stakeholder relationships at this level, and an unaddressed grievance festers — but it does not require the full resolution today; a prompt, respectful holding reply acknowledging her concern and proposing a conversation costs twenty minutes and can happen alongside item 1. Item 2 matters and has a Friday deadline, leaving time after Wednesday. Item 4 is important but two weeks away. Option A over-weights seniority against a hard governance deadline; C treats the stakeholder email as third purely by deadline logic, ignoring the relationship cost of silence; D inverts impact ordering. Note the practical pattern in B: high-impact deadline work first, but with a cheap early gesture on the relationship issue — senior analysts rarely face pure either/or choices, and the best answers often sequence a small action inside a larger one.

**Question 5 (moderate) — Logical deduction about requirement dependencies**

Your traceability analysis establishes these facts: (i) requirement R1 (online payment) depends on R2 (identity verification); (ii) R2 depends on R3 (integration with the identity platform); (iii) R3 has been descoped from the current release. Assuming a requirement can only be delivered in this release if everything it depends on is delivered in this release, which conclusion must be true?

- A) R1 and R2 cannot be delivered in the current release.
- B) R1 will be delivered in a future release.
- C) R2 was descoped because R3 was descoped.
- D) The current release has no payment functionality.

**Correct answer: A**

**Explanation:** Follow the dependency chain. R3 is out of this release; R2 depends on R3, so R2 cannot be delivered in this release; R1 depends on R2, so R1 cannot either. That is exactly conclusion A. B goes beyond the evidence — nothing guarantees R1 will ever be delivered; descoping decisions in a future release are not determined by these facts. C invents a causal story: R2's infeasibility follows from the dependency, but no fact says R2 "was descoped" or why. D overgeneralises: R1 is one payment requirement; the release might contain other payment functionality not mentioned. The discipline here — deduce the full consequences of a dependency chain, but nothing more — mirrors your duty to co-ordinate and review the prioritisation of requirements: when a stakeholder descopes one item, the senior analyst is the person who traces what else silently falls out of scope and puts that consequence in front of the decision makers before they commit.

**Question 6 (moderate) — Pattern recognition in defect data**

During user acceptance testing, you review the defect log for a new casework service. Defects are tagged by screen. The counts are: Search screen 4, Case summary 5, Evidence upload 21, Payments 6, Letters 3. Test coverage (planned test cases executed) is roughly equal across screens. As the analyst who reviews test outcome reporting, what is the most reasonable first interpretation of the evidence upload figure?

- A) The evidence upload developers are underperforming and should be replaced.
- B) Evidence upload is a defect cluster warranting investigation — its requirements, design or technical complexity may differ from the other screens.
- C) The other screens were not tested properly, so their counts are artificially low.
- D) The defect counts are within normal variation and no action is needed.

**Correct answer: B**

**Explanation:** Four screens cluster between 3 and 6 defects; one shows 21 — roughly four times the cluster, with test coverage held approximately equal, so the difference is unlikely to be a testing artefact. That makes evidence upload a genuine cluster, and clusters are prompts for inquiry, not verdicts. Common explanations include ambiguous or volatile requirements for that screen, inherently higher technical complexity (file handling, virus scanning, format validation), or a late design change. Option A leaps from a symptom to a blame conclusion without evidence; C contradicts the stem, which says coverage was roughly equal; D ignores a four-fold outlier. The professional move — the one your Testing skill describes as reviewing test outcome reporting — is to ask what the cluster tells you about the quality of the requirements and acceptance criteria you and your team wrote for that screen, before asking what it says about anyone's code.

**Question 7 (moderate) — Error checking acceptance criteria against a requirement**

Requirement FR-022 states: "A caseworker must be able to place a case on hold for up to 28 calendar days, after which the case automatically returns to the active queue." A junior analyst drafts these acceptance criteria:

1. Given an active case, when the caseworker selects "hold" and enters a duration of 28 days or fewer, the case status becomes "On hold".
2. Given a case on hold, when the entered duration elapses, the case status becomes "Active" and it appears in the active queue.
3. Given an active case, when the caseworker selects "hold" and enters 30 days, the system saves the case with a 30-day hold.

Which criterion contradicts the requirement?

- A) Criterion 1
- B) Criterion 2
- C) Criterion 3
- D) None — all three are consistent with FR-022

**Correct answer: C**

**Explanation:** The requirement caps holds at 28 calendar days. Criterion 3 has the system accept and save a 30-day hold, which directly violates the cap — the correct behaviour for an over-limit entry would be rejection with a validation message, or capping at 28 days, depending on the agreed design. Criteria 1 and 2 restate the requirement's two halves faithfully: holds up to the limit, and automatic return when the duration elapses. Notice the shape of the error: criterion 3 reads like a plausible test of boundary behaviour, and a hurried reviewer might see "enters 30 days" and assume it tests rejection — but the "then" clause saves the hold rather than refusing it. Reading each criterion's outcome clause, not just its trigger, is the habit that makes your review of acceptance criteria genuinely protective. Advising on business scenarios and developing acceptance criteria so requirements can be traced into functionality is precisely your Testing (business analysis) skill in action.

**Question 8 (moderate) — Applied problem solving on root causes**

Call volumes to a benefits helpline rose 40% in March. You lead the root cause investigation and gather these facts: a new online claim form launched 1 March; the helpline's top March call reason, absent in February, is "confusion about question 7 on the new form"; average call handling time is unchanged; web analytics show 62% of users abandon the online form at question 7. What is the strongest analytical conclusion?

- A) The helpline needs 40% more staff.
- B) Question 7 of the new form is causing user confusion, driving both form abandonment and calls; redesigning it should be evaluated as the primary intervention.
- C) Users prefer telephone channels to online forms.
- D) The form should be withdrawn and the old process restored.

**Correct answer: B**

**Explanation:** Triangulate the evidence: the timing coincides with the form launch; the new top call reason names question 7 explicitly; and an independent data source — web analytics — shows abandonment concentrated at the same question. Three converging lines of evidence pointing at one specific cause is about as strong as root cause analysis gets. Option A treats the symptom and locks in the cost of the defect forever; C draws a general channel-preference conclusion that the evidence does not support (users are struggling at one question, not choosing the phone in general); D is disproportionate — one defective question does not justify abandoning the whole change, and the stem gives no evidence the old process performed better overall. The pattern to internalise: lead the approach to understanding root causes by seeking independent evidence sources that converge, then propose the smallest intervention aimed at the cause — a redesigned question 7, followed by measurement — with staffing relief at most as a short-term mitigation.

**Question 9 (challenging) — Multi-constraint scheduling of analysis activities**

You must schedule four activities in a discovery week, Monday to Friday, at most one per day: stakeholder interviews (S), process observation (O), a findings playback (P), and a prioritisation workshop (W). Constraints: (i) S and O must both be complete before P; (ii) P must occur the day immediately before W; (iii) the operations team can only host O on Tuesday or Wednesday; (iv) the sponsor, who must attend P, is unavailable Wednesday. On which day must the playback (P) take place?

- A) Tuesday
- B) Wednesday
- C) Thursday
- D) Friday

**Correct answer: C**

**Explanation:** Work through the constraints systematically. From (ii), P and W occupy consecutive days, so P can be at latest Thursday (with W on Friday). From (iv), P cannot be Wednesday. Could P be Tuesday? Then S and O would both need to precede it, on Monday — but only one activity is allowed per day, so S and O cannot both fit before Tuesday; P on Tuesday is impossible. Could P be Monday? Impossible for the same reason — nothing can precede it. That leaves Thursday as the only feasible day for P, with W on Friday. Check feasibility: O on Tuesday or Wednesday satisfies (iii), S on the remaining early day (Monday or Wednesday/Tuesday), both before Thursday — the schedule works, for example S Monday, O Tuesday, P Thursday, W Friday. Constraint-satisfaction reasoning of this kind is the hidden skeleton of real analysis planning: room availability, stakeholder diaries and dependency order interact, and the senior analyst who can rapidly deduce "the playback can only be Thursday" saves a week of email tennis.

**Question 10 (challenging) — Deduction from conflicting model versions**

Two versions of a data model exist for the same service. Version 1 states: every case has exactly one assigned caseworker; a caseworker may have many cases. Version 2 states: a case may have multiple assigned caseworkers during handover periods; at all other times it has exactly one. The operational reality is that handovers exist and last up to five working days. If the build team implements Version 1, which consequence must follow during handover periods?

- A) The system will crash during handovers.
- B) The system cannot represent the true state — either the outgoing or incoming caseworker's assignment must be omitted or the handover modelled some other way outside the case-caseworker relationship.
- C) Caseworkers will refuse to use the system.
- D) Handover periods will shorten to zero days.

**Correct answer: B**

**Explanation:** Version 1's cardinality — exactly one caseworker per case — makes it logically impossible for the database to record two simultaneous assignments. During a real handover, two people genuinely share responsibility, so the system as built cannot represent reality: teams will either record only one name (losing accountability information) or invent workarounds such as spreadsheets or notes fields. That is precisely conclusion B, and nothing stronger. A confuses a modelling gap with a technical failure — the system will run happily while misrepresenting the world; C predicts human behaviour the facts do not determine; D reverses cause and effect — a data model does not change operational practice by itself, and the stem says handovers genuinely last up to five days. This is the essence of your Systems analysis skill: using analysis of how processes and systems actually work to identify gaps between the model and the operation, and putting the discrepancy in front of the team before it is baked into the build, when a one-line cardinality change costs an hour rather than a migration.

**Question 11 (challenging) — Prioritisation with hidden dependencies**

Your backlog contains four analysis tasks for the next sprint, each estimated at one analyst-week, with two analyst-weeks available (you and one other analyst):

1. Define acceptance criteria for the release's committed features (needed by developers mid-sprint).
2. Analyse options for a policy change announced last week (minister interested; no committed date).
3. Update the process model library after last month's changes (overdue housekeeping).
4. Investigate a data quality issue that, if confirmed, would invalidate the benefits baseline used in task 2's options analysis.

Which pair should you schedule this sprint?

- A) Tasks 1 and 2
- B) Tasks 1 and 4
- C) Tasks 2 and 4
- D) Tasks 1 and 3

**Correct answer: B**

**Explanation:** Task 1 is anchored: developers need acceptance criteria mid-sprint, and failing to supply them blocks committed delivery — it must be in. The interesting reasoning is the second slot. Task 2 looks like the obvious choice (ministerial interest carries real weight), but task 4 is logically prior to it: if the data quality issue would invalidate the benefits baseline underpinning the options analysis, then doing task 2 first risks producing an appraisal built on bad data — work you may have to redo, and worse, advice a minister might act on before the flaw surfaces. Sequencing task 4 first protects the integrity of task 2 and typically delays it by only a week. Task 3 is genuine but has no deadline pressure and blocks nothing. Option A produces fast but potentially unsound strategic advice; C leaves developers blocked; D defers both strategic tasks for housekeeping. The senior-analyst insight: prioritisation is not just ranking by urgency and importance — it is ordering by logical dependency, and analysis that validates the foundations of other analysis often deserves to jump the queue. Making prioritisation decisions using analysis-led insights is exactly the duty this question exercises.

**Question 12 (challenging) — Applied problem solving under ambiguity**

A director asks you to "make the licensing process faster". Initial analysis shows: end-to-end elapsed time averages 40 working days; actual processing effort totals 6 hours per application; 25 of the 40 days are spent waiting for an external agency's check, which the agency completes in 3 days once started but only begins after a weekly batch transfer; internal quality checks account for 8 days, rework loops for 5 days, and the remainder is queue time. Which improvement hypothesis should you investigate first?

- A) Train staff to reduce the 6 hours of processing effort.
- B) Replace the weekly batch transfer to the external agency with a daily or real-time transfer, attacking the largest single block of elapsed time.
- C) Eliminate internal quality checks to save 8 days.
- D) Hire more staff to reduce queue time.

**Correct answer: B**

**Explanation:** Decompose the 40 days: 25 days external agency (of which only 3 are the agency actually working — up to 22 days is waiting caused substantially by the weekly batching), 8 days quality checks, 5 days rework, and the remainder queueing. The largest improvement lever is the biggest block of dead time with an identifiable mechanical cause: applications wait for a weekly transfer before a 3-day check. Moving to daily transfer could remove several days for a typical application at low risk — likely the single biggest gain available. Option A optimises the smallest number in the problem: 6 hours of effort is under 2% of 40 days of elapsed time, a classic touch-time versus elapsed-time confusion. Option C saves 8 days but removes a control, trading speed for risk without any evidence the checks add no value — and the 5 days of rework suggests quality problems already exist. Option D treats queue time without knowing its cause. The analytical pattern — separate effort from elapsed time, find the largest wait, identify its mechanism, and intervene there first — is the heart of leading process analysis and evaluation to define business performance problems and opportunities.

### Preparation tips

- **Practise with your own artefacts.** Take a real process model, requirements catalogue or traceability matrix from a past project and deliberately hunt for inconsistencies: identifiers that break convention, decision points missing an outcome, criteria whose outcome clause contradicts the requirement. Ten minutes a day of artefact review builds exactly the error-checking speed these tests measure.
- **Learn the necessary/sufficient distinction cold.** A large share of deduction questions turn on "only if" versus "if", and so does a large share of requirements defects. Practise rewriting policy sentences both ways and noticing how the meaning changes.
- **Time-box your practice.** Cognitive tests reward calibrated pace. Practise answering questions in 60 to 90 seconds each; if you are stuck at the 90-second mark, choose your best elimination-based answer and move on. Accuracy under time pressure is a trainable skill.
- **Draw dependency chains.** For scheduling and dependency questions, sketch the chain (even mentally: R1 → R2 → R3) before reading the options. Working from your own reconstruction of the logic, rather than testing each option cold, is faster and less error-prone.
- **Read the outcome clause.** In any given/when/then structure — acceptance criteria, business rules, test steps — the trap is usually in the "then". Train yourself to read triggers and outcomes as separate claims.
- **Rest and environment matter.** Book your test for a time of day when you are sharp, use a quiet room, and have rough paper or a whiteboard ready. These are permitted in almost all cognitive assessments and dramatically help with multi-constraint questions.

### Common pitfalls to avoid

- **Deducing more than the evidence supports.** The most common error for experienced analysts is importing plausible context ("she probably meant...") into a deduction question. In the test, as in a requirements review, only what is stated counts.
- **Anchoring on the first inconsistency.** Having found one error in an artefact, people stop looking. Questions (and real reviews) often contain a second, subtler issue; finish your systematic pass before answering.
- **Confusing touch time with elapsed time.** In process questions, effort hours and elapsed days are different quantities with different improvement levers. Mixing them up leads to optimising the wrong thing.
- **Letting seniority override logic in prioritisation.** "The director asked" is a factor, not a trump card. Defensible sequencing weighs impact, urgency and dependency together — and assessors deliberately include a senior-stakeholder distractor to test this.
- **Rushing multi-constraint questions.** Constraint problems punish guessing and reward systematic elimination. Thirty seconds spent laying out the constraints saves ninety seconds of confused re-reading.
- **Treating adaptive difficulty as failure.** If the questions feel harder as you go, the adaptive engine is responding to your correct answers. Do not let perceived difficulty dent your confidence mid-test.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment measures your ability to interpret, manipulate and draw sound conclusions from quantitative information of the kind your role genuinely handles. It is not a mathematics exam: the arithmetic rarely goes beyond percentages, ratios, averages, rates and simple projections. What it tests is whether you can extract the right numbers from tables and charts, perform the right operations under time pressure, and — crucially for an analyst — recognise what a number does and does not show.

Typical format: an online, timed test of 20 to 40 minutes with 15 to 25 questions, each based on a table, chart or short data-rich passage. Most platforms allow a calculator and rough paper, and many are adaptive. Employers typically look at both accuracy and speed, and some report a "carefulness" indicator based on whether your errors cluster on questions with plausible-looking distractors. Question data is usually fictional but realistic — exactly as in the practice set below.

For a senior business analyst, numeric reasoning is not an adjacent skill; it is load-bearing. You define success measures and baselines, quantify the effects of change, appraise options with costs and benefits, review test outcome reports full of pass rates and defect counts, and challenge performance claims made by suppliers and stakeholders. When you lead analysis and evaluation to assess business process improvements, the assessment is numeric: cycle times, error rates, unit costs, uptake percentages. When you coordinate prioritisation, the trade-offs are numeric: value scores, effort estimates, capacity. And because you review others' work and develop best practice, employers want confidence that a wrong denominator or a misread chart will not get past you. A percentage error that survives your review can misdirect a programme board.

### How this assessment maps to your role

- **Percentages and percentage change** map to **Business process improvement**: defining performance problems and assessing improvements means computing and comparing error rates, completion rates, and before/after changes correctly — including the difference between percentage points and percentages.
- **Ratios and proportions** map to **Context, problem and option analysis**: options appraisals turn on cost per transaction, benefit-cost ratios, and proportional allocation of shared costs across options.
- **Averages and distributions** map to **Business modelling** and **Testing (business analysis)**: modelling how a process performs requires knowing when a mean misleads and a median informs, and test outcome reports demand correct aggregation of pass rates across unevenly sized test suites.
- **Rates and capacity arithmetic** map to **Adapting to delivery methodologies** and **Requirements definition and management**: negotiating delivery priorities honestly requires converting velocity, capacity and demand into feasible scope.
- **Reading tables and charts** maps to **User experience analysis** and **Stakeholder relationship management**: analytics funnels, survey results and dashboard extracts are how user experience evidence arrives, and communicating clearly and regularly with stakeholders means presenting numbers that survive scrutiny.

### Practice questions

**Question 1 (easy) — Percentage of a total**

A digital service received 12,400 applications last month. Of these, 3,100 were submitted through the assisted digital telephone channel and the rest online. What percentage were submitted online?

- A) 25%
- B) 66%
- C) 75%
- D) 79%

**Correct answer: C**

**Explanation:** Online applications = 12,400 − 3,100 = 9,300. Percentage online = 9,300 ÷ 12,400 = 0.75 = 75%. A common slip is computing the assisted digital share (3,100 ÷ 12,400 = 25%, option A) and forgetting the question asks for the complement. Always re-read which share the question wants before answering. Channel-share calculations like this appear constantly in your work analysing how a business area works and whether services meet user needs — for example, evidencing whether assisted digital provision is proportionate.

**Question 2 (easy) — Percentage change in a process metric**

After a process improvement you led, average end-to-end processing time for a licence application fell from 32 working days to 24 working days. What is the percentage reduction?

- A) 8%
- B) 25%
- C) 33%
- D) 75%

**Correct answer: B**

**Explanation:** Reduction = 32 − 24 = 8 days. Percentage reduction = change ÷ original = 8 ÷ 32 = 0.25 = 25%. The classic error is dividing by the new value: 8 ÷ 24 = 33% (option C), which overstates your improvement — an embarrassing mistake in a benefits report that a finance reviewer will catch. Always divide by the baseline (the "before" figure) for a reduction. When you lead the assessment of business process improvements, the credibility of your benefits claims rests on getting exactly this convention right.

**Question 3 (easy) — Reading a simple table**

Your sprint metrics for the last four sprints show completed story points: Sprint 1: 34; Sprint 2: 28; Sprint 3: 42; Sprint 4: 36. What is the mean velocity across the four sprints?

- A) 34
- B) 35
- C) 36
- D) 38

**Correct answer: B**

**Explanation:** Sum = 34 + 28 + 42 + 36 = 140. Mean = 140 ÷ 4 = 35 story points per sprint. A quick sanity check: the values range from 28 to 42, so the mean must sit comfortably inside that range, and 35 does. Velocity averages inform the conversations your Adapting to delivery methodologies skill describes — negotiating and agreeing delivery priorities with the team and stakeholders requires an honest, evidence-based view of what a sprint can actually absorb, not an optimistic one.

**Question 4 (moderate) — Percentage points versus percentages**

The first-time completion rate for an online form rose from 60% to 69% after your team redesigned the address lookup. A stakeholder drafts a press line saying the completion rate "rose by 9%". As the analyst reviewing the claim, what is the accurate characterisation?

- A) The rate rose by 9 percentage points, which is a 15% relative increase.
- B) The rate rose by 9%, exactly as drafted.
- C) The rate rose by 15 percentage points.
- D) The rate rose by 9 percentage points, which is a 9% relative increase.

**Correct answer: A**

**Explanation:** The difference between 69% and 60% is 9 percentage points. The relative increase is 9 ÷ 60 = 0.15 = 15%. So the draft understates the relative improvement and mislabels the unit: "rose by 9%" strictly means 60% × 1.09 = 65.4%. Option A states both figures correctly. This distinction is a favourite of numeric tests because it is a favourite source of real-world miscommunication: as the senior analyst who defines success measures and communicates them to stakeholders, you are the quality gate between the metric and the message, and correcting the wording before publication is exactly the kind of review your role exists to provide.

**Question 5 (moderate) — Weighted average across test suites**

You are reviewing a test outcome report. Suite A contains 120 test cases with a 90% pass rate; Suite B contains 40 test cases with a 70% pass rate. The report states the overall pass rate as "80% (average of the two suites)". What is the correct overall pass rate?

- A) 80%
- B) 82%
- C) 85%
- D) 87.5%

**Correct answer: C**

**Explanation:** Compute passes, not averages of averages. Suite A: 120 × 0.90 = 108 passes. Suite B: 40 × 0.70 = 28 passes. Total passes = 108 + 28 = 136 out of 160 cases. Overall rate = 136 ÷ 160 = 0.85 = 85%. The report's "80%" is the unweighted mean of 90% and 70%, which ignores the fact that Suite A is three times larger. Unweighted averaging of unevenly sized groups is one of the most common errors in test and performance reporting, and reviewing test outcome reporting is explicitly part of your Testing (business analysis) skill — this question is the exact check you should run whenever a report averages rates.

**Question 6 (moderate) — Capacity and demand arithmetic**

Your team of 4 analysts each has 6 productive hours per day, 5 days a week. Next sprint (2 weeks), the team must complete requirements workshops consuming a total of 130 hours and documentation consuming 80 hours. One analyst is on leave for the whole second week. How many hours of spare capacity, if any, does the team have?

- A) The team is 10 hours over capacity
- B) 0 hours — exactly at capacity
- C) 20 hours spare
- D) 30 hours spare

**Correct answer: B**

**Explanation:** Work step by step in writing. Full capacity = 4 analysts × 6 hours × 10 working days = 240 hours. The absent analyst loses 6 hours × 5 days = 30 hours, so available capacity = 240 − 30 = 210 hours. Total demand = 130 + 80 = 210 hours. Spare = 210 − 210 = 0 hours: the team is exactly at capacity. The tempting errors are forgetting the leave adjustment (240 − 210 = 30 spare, option D) or applying the leave to both weeks (60 hours lost, putting the team 10 hours over, option A) — each comes from rushing the capacity side of the equation. And note that exactly-at-capacity is itself a finding worth escalating when you negotiate delivery priorities: a plan with zero slack fails the first time anything slips, and the senior analyst's job is to say so before the sprint starts, not after.

**Question 7 (moderate) — Cost per transaction comparison**

An options appraisal compares two solutions for processing 60,000 applications per year. Option 1: annual running cost £480,000 plus £120,000 annual licence. Option 2: annual running cost £390,000 plus £150,000 annual licence, but it can only automate 80% of applications; the remaining 20% are handled manually at £15 per application. What is the cost per application for Option 2?

- A) £9.00
- B) £10.00
- C) £12.00
- D) £13.00

**Correct answer: C**

**Explanation:** Option 2's total annual cost = £390,000 + £150,000 = £540,000 for the automated capability, plus manual handling: 20% of 60,000 = 12,000 applications × £15 = £180,000. Total = £540,000 + £180,000 = £720,000. Cost per application = £720,000 ÷ 60,000 = £12.00. (For comparison, Option 1 costs £600,000 ÷ 60,000 = £10.00 per application — cheaper, despite its higher headline licence cost.) The trap is quoting £540,000 ÷ 60,000 = £9.00 (option A) by forgetting the manual tail. Hybrid solutions with a manual exception path are everywhere in government services, and pricing the exception path is precisely the kind of full-cost thinking your Context, problem and option analysis skill demands when you lead the evaluation of multiple options and advocate a recommendation.

**Question 8 (moderate) — Interpreting a funnel**

Web analytics for an application journey show: 20,000 users start the form; 16,000 complete section 1; 15,200 complete section 2; 9,120 complete section 3; 8,900 submit. Which section has the highest drop-off rate relative to the users entering it?

- A) Section 1
- B) Section 2
- C) Section 3
- D) Submission step

**Correct answer: C**

**Explanation:** Compute each step's drop-off as a proportion of those entering it. Section 1: (20,000 − 16,000) ÷ 20,000 = 4,000 ÷ 20,000 = 20%. Section 2: (16,000 − 15,200) ÷ 16,000 = 800 ÷ 16,000 = 5%. Section 3: (15,200 − 9,120) ÷ 15,200 = 6,080 ÷ 15,200 = 40%. Submission: (9,120 − 8,900) ÷ 9,120 = 220 ÷ 9,120 ≈ 2.4%. Section 3 loses 40% of its entrants — double section 1's rate and far above the rest. The trap is judging by absolute numbers alone or by cumulative completion, both of which can mask where the journey actually breaks. Funnel analysis with correct per-step denominators is core to your User experience analysis skill: recommending techniques to analyse the user experience means knowing that "9,120 completed section 3" is meaningless until you know how many tried.

**Question 9 (challenging) — Benefits projection with ramp-up**

A process change is forecast to save 5 minutes per case at a fully loaded staff cost of £30 per hour. Annual case volume is 240,000. The change goes live at the start of Q2 (the year has four equal quarters), and realises only 50% of the per-case saving in its first live quarter due to ramp-up, then 100% thereafter. What is the total saving in year 1?

- A) £600,000
- B) £375,000
- C) £450,000
- D) £300,000

**Correct answer: B**

**Explanation:** Step 1 — value of the full saving per case: 5 minutes at £30/hour = 5 ÷ 60 × £30 = £2.50 per case. Step 2 — quarterly volume: 240,000 ÷ 4 = 60,000 cases. Step 3 — quarter by quarter: Q1 is before go-live, saving £0. Q2 realises 50%: 60,000 × £2.50 × 0.5 = £75,000. Q3 and Q4 realise 100%: 60,000 × £2.50 = £150,000 each. Step 4 — total: £0 + £75,000 + £150,000 + £150,000 = £375,000. Option A (£600,000) is the naive full-year, full-rate figure (240,000 × £2.50) ignoring both the Q1 gap and ramp-up; C ignores ramp-up only; D ignores half the live period. Benefits cases that ignore go-live timing and ramp-up systematically overstate year 1 savings, and finance reviewers know it — building the quarterly profile explicitly, as here, is what makes your assessment of a business process improvement credible at approval and honest at benefits review.

**Question 10 (challenging) — Ratio reasoning in prioritisation scoring**

Your prioritisation framework scores each candidate feature as value points divided by effort points (higher is better). Feature X: value 60, effort 20. Feature Y: value 45, effort 12. Feature Z: value 90, effort 36. A stakeholder argues Z must come first "because it has by far the highest value". Ranked by the framework, what is the correct order?

- A) Z, X, Y
- B) X, Y, Z
- C) Y, X, Z
- D) Y, Z, X

**Correct answer: C**

**Explanation:** Compute each ratio. X: 60 ÷ 20 = 3.0. Y: 45 ÷ 12 = 3.75. Z: 90 ÷ 36 = 2.5. Order by ratio: Y (3.75), then X (3.0), then Z (2.5). The stakeholder's argument ranks by the numerator alone — the highest-value item is actually the least efficient use of capacity per point of effort. Note what the framework does and does not settle: value-per-effort maximises return on a constrained team, but a genuinely indivisible strategic commitment can still justify overriding the score — the analyst's job is to make the override explicit and evidenced rather than silent. Coordinating and reviewing the prioritisation of requirements, and negotiating solutions to meet programme objectives, means being able to do this arithmetic instantly in a meeting and explain it persuasively to the stakeholder whose favourite feature just ranked last.

**Question 11 (challenging) — Spotting a misleading average**

A supplier reports that average call-handling time in the service you are analysing is 8 minutes, evidencing "efficient operation". You obtain the underlying distribution for a sample of 1,000 calls: 700 routine calls averaging 4 minutes; 250 standard casework calls averaging 10 minutes; 50 complex calls averaging 54 minutes. Verify the average, and identify the most analytically important observation.

- A) The average is wrong; the true mean is 12 minutes.
- B) The average is approximately right (8.1 minutes), but the mean is inflated by a small number of very long calls; the median call is a 4-minute routine call, and complex calls consume about a third of total handling time.
- C) The average is approximately right, which confirms the operation is efficient.
- D) The average is wrong; the true mean is 6 minutes.

**Correct answer: B**

**Explanation:** Verify the mean: total minutes = 700 × 4 + 250 × 10 + 50 × 54 = 2,800 + 2,500 + 2,700 = 8,000 minutes across 1,000 calls = 8.0 minutes — the supplier's figure checks out arithmetically (8.1 in the option is within rounding of a real sample). But the mean conceals the structure: the median call (the 500th when sorted) sits among the 700 routine 4-minute calls, and the 50 complex calls — 5% of volume — consume 2,700 ÷ 8,000 ≈ 34% of all handling time. The analytical gold is that complex calls, not routine ones, are where a third of the resource goes: improving their handling (or diverting them to a better channel) is worth more than shaving seconds off routine calls. Options A and D are arithmetic errors; C accepts a true number with a false implication. When you lead process analysis and evaluation, distributions beat averages — a mean is a summary, not a diagnosis.

**Question 12 (challenging) — Reconciling two data sources**

A dashboard shows 5,200 applications received in June. The operational team's case management system shows 4,940 new cases created in June. Both systems are functioning correctly. Investigation shows 180 applications were withdrawn by applicants before a case was created, and duplicate submissions are merged before case creation. How many June applications were duplicates that were merged?

- A) 80
- B) 180
- C) 260
- D) 440

**Correct answer: A**

**Explanation:** Set up the reconciliation as an equation. Applications received = cases created + withdrawn before case creation + duplicates merged. So 5,200 = 4,940 + 180 + duplicates. Duplicates = 5,200 − 4,940 − 180 = 80. Option C (260) is the raw gap between the two systems, quoted without accounting for withdrawals — the classic partial reconciliation. Option B repeats the withdrawal figure; D combines numbers with no meaning. Reconciling counts across systems is bread-and-butter systems analysis: two "correct" systems routinely disagree because they count different events at different points in the process, and the analyst who can decompose the gap into named causes — withdrawal, merge, timing — turns a suspicious discrepancy into a documented data flow. This is exactly the deeper understanding of how processes and systems work that your Systems analysis skill describes, and it is how you stop a programme board wasting an hour arguing about whose number is "right".

### Preparation tips

- **Rebuild your percentage reflexes.** The four operations that dominate these tests are: share of total, percentage change (divide by the original), percentage points versus relative percentages, and reverse percentages (finding the original from a changed value). Drill each until automatic.
- **Always write the denominator first.** Before computing any rate or share, state to yourself what the denominator is — entrants to this step, the baseline year, the whole caseload. Most numeric errors are denominator errors.
- **Practise weighted averages.** Any time two groups of different sizes are averaged, weight by size. Practise on real test reports and performance packs from your own programme.
- **Do benefit-style calculations end to end.** Take a simple saving (minutes per case, cost per hour, annual volume) and build the year 1 figure with a go-live date and ramp-up, quarter by quarter. This single exercise rehearses multiplication chains, proportions and time-phasing together.
- **Use rough paper deliberately.** Write intermediate results down. Chained mental arithmetic under time pressure is where careful analysts make careless errors — as Question 6 dramatised.
- **Sanity-check every answer.** Is the mean inside the data range? Is the percentage between 0 and 100? Is the cost per unit plausible? A three-second sanity check catches most slips.

### Common pitfalls to avoid

- **Dividing by the wrong base.** Percentage change divides by the original value; per-step funnel drop-off divides by that step's entrants. Both are relentlessly tested because both are relentlessly fumbled in real reports.
- **Averaging averages.** Never average two rates from different-sized groups without weighting. If a report does it, the report is wrong — and if you do it in a test, the distractor is waiting.
- **Confusing percentage points with percentages.** A rise from 60% to 69% is 9 points and 15% relative. Choose language deliberately, in tests and in press lines alike.
- **Ignoring time-phasing.** Annualised benefits, mid-year go-lives and ramp-up periods interact. The full-year full-rate figure is almost always one of the wrong options.
- **Quoting the gap without decomposing it.** When two sources disagree, the difference is the start of the analysis, not the finding. Decompose before you conclude.
- **Speed-reading the question stem.** Numeric stems hide the operative words — "relative to users entering it", "in year 1", "per application". Read the final sentence of the stem twice; it usually defines the calculation.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment measures how accurately you extract meaning from written material of the kind your role handles daily — policy extracts, service standards, stakeholder emails, supplier proposals, research summaries and governance papers — and how soundly you reason from what a text actually says, as opposed to what you expect it to say.

Typical format: an online, timed test of 15 to 25 minutes. You are shown a short passage and asked a series of questions in one of several styles: True / False / Cannot say (does the statement follow from the passage alone?); inference questions (which conclusion is best supported?); and clear-writing judgement (which rewrite most faithfully and clearly conveys the meaning?). The cardinal rule, printed at the start of every such test, is that you must answer using only the information in the passage — outside knowledge, however expert, must be set aside. Scoring is objective, and adaptive versions raise passage complexity as you succeed.

For a senior business analyst, verbal precision is a professional instrument. Requirements are sentences: an ambiguous modal verb ("should" versus "must"), an unquantified adjective ("promptly", "significant"), or a misplaced qualifier can change what gets built. You read policy constraints and must assess their implications without over- or under-reading them. You own stakeholder relationships, which means reading between the lines of what stakeholders write while never confusing your inference with their statement — and writing your own communications so they cannot be misread. You review and quality-assure the documents of analysts you mentor. Employers assess verbal reasoning for this role because a senior analyst who misreads a policy sentence can misdirect an entire delivery team, and one who writes loosely can generate months of avoidable rework.

### How this assessment maps to your role

- **Precise comprehension** maps to **Requirements definition and management**: defining requirements that can be traced through design, build, test, tender and evaluation depends on reading source material — policy, legislation summaries, business rules — with exactness, and on knowing when a sentence is ambiguous.
- **True/False/Cannot-say discipline** maps to **Context, problem and option analysis**: leading the approach to understanding a problem means separating what the evidence states from what it merely suggests, and holding "we don't know yet" as a legitimate finding.
- **Inference judgement** maps to **Stakeholder relationship management**: identifying and resolving issues and influencing stakeholders requires reading correspondence for what it commits to, what it avoids committing to, and what can fairly be inferred — without putting words in anyone's mouth.
- **Clear-writing judgement** maps to **Business modelling** and **User experience analysis**: articulating how user experience needs affect design, and documenting models that others rely on, both demand plain, unambiguous prose — and the ability to spot and repair unclear prose in others' drafts, which is central to developing best practice and mentoring.
- **Reading standards and guidance** maps to **Adapting to delivery methodologies** and **Testing (business analysis)**: applying the Service Standard, test strategies and methodology guidance correctly starts with reading them correctly, including their qualifiers and exceptions.

### Practice questions

For questions 1 to 5, use this passage.

> **Extract from a departmental policy note on service eligibility**
>
> From 1 April, applicants who are resident in the United Kingdom and have held residency for at least 12 months are eligible for the standard grant. Applicants with less than 12 months' residency may be eligible for the transitional grant, subject to a caseworker assessment. The transitional grant is paid at 60% of the standard rate. Caseworker assessments must be completed within 15 working days of application. Where an assessment is not completed in time, the application is escalated to a senior caseworker; escalation does not change the eligibility criteria that apply. Applications made before 1 April continue under the previous scheme rules.

**Question 1 (easy) — True / False / Cannot say**

Statement: "An applicant with 8 months' UK residency who applies on 10 April will automatically receive the transitional grant."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** The passage says applicants with less than 12 months' residency *may be eligible* for the transitional grant, *subject to a caseworker assessment*. "May be eligible, subject to assessment" is the opposite of "automatically receive": the passage explicitly makes the outcome conditional on an assessment. So the statement is false on the passage's own terms — not "cannot say", because the passage directly contradicts the word "automatically". Watch for this pattern: a statement that matches the passage's topic but strengthens its modality ("may" becomes "will", "subject to" disappears) is false, not unverifiable. In requirements work, the identical discipline stops you turning a discretionary policy provision into a mandatory system rule.

**Question 2 (easy) — True / False / Cannot say**

Statement: "The transitional grant is paid at a lower rate than the standard grant."

- A) True
- B) False
- C) Cannot say

**Correct answer: A**

**Explanation:** The passage states the transitional grant is paid at 60% of the standard rate. Sixty per cent of a rate is lower than the full rate (for any positive rate), so the statement follows directly — this is a one-step arithmetic inference of the kind verbal tests treat as legitimately contained in the passage. Note the contrast with Question 1: here the statement's strength matches the passage's strength exactly. When you brief a delivery team on policy, being able to say "this is stated" versus "this is my interpretation" — and label which is which — is a hallmark of trustworthy analysis.

**Question 3 (moderate) — True / False / Cannot say**

Statement: "If a caseworker assessment takes 20 working days, the applicant becomes ineligible for the transitional grant."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** The passage specifies what happens when the 15-working-day limit is missed: the application is escalated to a senior caseworker, and — the key sentence — "escalation does not change the eligibility criteria that apply". A late assessment therefore triggers escalation, not ineligibility; the passage directly addresses the consequence and it is not the one the statement claims. The statement is false rather than "cannot say" because the passage does tell us the consequence of lateness. This mirrors a real analytical trap: conflating a service-level breach (process failure) with an eligibility change (policy outcome). Systems built by teams who confuse the two wrongly reject applicants — exactly the implication-checking your role performs when assessing business and policy constraints.

**Question 4 (moderate) — True / False / Cannot say**

Statement: "Most applicants for the transitional grant receive a decision within 15 working days."

- A) True
- B) False
- C) Cannot say

**Correct answer: C**

**Explanation:** The passage sets a requirement — assessments *must* be completed within 15 working days — but says nothing about actual performance against that requirement. A rule stating what must happen tells you nothing about how often it does happen; the existence of an escalation route even hints that breaches occur, but "hints" is not evidence of frequency, and "most" is a quantified empirical claim. So the correct answer is "cannot say". Distinguishing normative statements (what should happen) from empirical ones (what does happen) is fundamental to your work: a process model built from the policy alone describes the intended process, and only observation or data tells you the actual one. Senior analysts who conflate the two produce target operating models that describe a fiction.

**Question 5 (moderate) — Inference**

Which of the following is best supported by the passage?

- A) The department expects some assessments to exceed 15 working days.
- B) Senior caseworkers apply stricter eligibility criteria than caseworkers.
- C) Applications made on 31 March will be assessed under the new scheme rules.
- D) The standard grant requires no caseworker assessment.

**Correct answer: A**

**Explanation:** The passage builds an explicit escalation mechanism for late assessments. Designing a defined consequence for an event is good evidence the author anticipates the event occurring — you do not legislate for the impossible — so A is a fair, modest inference. B is contradicted: escalation "does not change the eligibility criteria". C is contradicted: applications before 1 April "continue under the previous scheme rules". D is tempting — the passage attaches assessment only to the transitional grant — but silence about assessment for the standard grant is not a statement that none is required; the passage may simply not cover it, so D overreaches from absence of evidence. The strongest inference is the one requiring the smallest step beyond the text. This calibrated-inference skill is what lets you read a supplier's carefully worded proposal and notice what it conspicuously does not promise.

For questions 6 to 8, use this passage.

> **Email from a programme director to the senior business analyst**
>
> Thanks for the options paper. I found the analysis of Options 1 and 2 thorough, and I accept the recommendation in principle. However, before I take this to the investment committee, I need the Option 3 costings validated by finance — the committee will not accept analyst estimates for a spend of this size. I also think the risks section understates the dependency on the identity platform team; their roadmap slipped twice last year. If validation is complete by Friday, I will circulate the paper for Tuesday's committee. Please also ensure the glossary is updated; two committee members are new to the programme.

**Question 6 (moderate) — Comprehension**

What has the programme director committed to doing?

- A) Presenting the paper at Tuesday's committee regardless of validation status.
- B) Circulating the paper for Tuesday's committee, if finance validation of Option 3 costings is complete by Friday.
- C) Accepting the recommendation and instructing delivery to begin.
- D) Rewriting the risks section personally.

**Correct answer: B**

**Explanation:** The director's commitment is explicitly conditional: "If validation is complete by Friday, I will circulate the paper for Tuesday's committee." Option A drops the condition; C overstates "I accept the recommendation in principle" — "in principle" is a hedged acceptance pending the committee process, not an instruction to proceed; D confuses a critique of the risks section with an offer to fix it (the fixing is implicitly your job). Mapping exactly what a stakeholder has and has not committed to — and what conditions attach — is the daily craft of owning stakeholder relationships: if you report to your team "the director will circulate on Tuesday" without the Friday condition, you have manufactured a commitment the director never made.

**Question 7 (moderate) — Inference**

What can be most safely inferred about the director's view of the risks section?

- A) The director believes the identity platform dependency is riskier than the paper currently conveys.
- B) The director believes the risks section should be deleted.
- C) The director believes the identity platform team is incompetent.
- D) The director believes all risks in the paper are understated.

**Correct answer: A**

**Explanation:** The director writes that the risks section "understates the dependency on the identity platform team" and evidences this with the team's roadmap slipping twice last year. That supports precisely A: the stated risk should be stronger. B has no basis. C converts an observation about roadmap slippage into a character judgement the email never makes — slippage has many causes, and the director attributes none. D generalises from one risk to all risks. The calibration here matters professionally: when you revise the paper, you should strengthen the specific dependency risk with the slippage evidence, not rewrite the whole risk section defensively. Reading feedback for its actual scope — no narrower, no wider — is how senior analysts respond to challenge efficiently and keep stakeholder trust.

**Question 8 (moderate) — Clear-writing judgement**

You need to reply confirming the plan. Which reply most clearly and faithfully reflects the email?

- A) "Thanks — I'll get finance to validate Option 3 costings by Friday, strengthen the identity platform dependency risk with the slippage history, and update the glossary for the new members. I'll confirm status Thursday so you have certainty before circulating."
- B) "Thanks — all agreed, the paper will be at committee Tuesday."
- C) "Thanks — I'll action your comments as soon as possible."
- D) "Thanks — noted on the costings. I don't agree the risks are understated, but I'll look at the glossary."

**Correct answer: A**

**Explanation:** Reply A restates each requested action specifically (validation, risk strengthening, glossary), reflects the Friday condition, and adds a sensible coordination step — a Thursday status confirmation — that protects the director's conditional commitment. B asserts an unconditional outcome the director never promised, propagating the exact misreading Question 6 warned against. C is courteous but contentless: it creates no shared understanding of what will happen by when, which is how Friday deadlines get missed. D picks a fight the email does not invite and ignores the costings deadline, the most time-critical item. In clear-writing questions, the best answer is usually the one that is specific, faithful to the source, and adds only coordination value — the same standard you apply when you communicate clearly and regularly with stakeholders.

For questions 9 to 12, use this passage.

> **Extract from an internal standard on requirements quality**
>
> Each requirement must be uniquely identified, testable, and traceable to a business need. A requirement is testable if an objective procedure can determine whether it is met. Requirements expressed as user needs should follow the format "As a [user], I need [capability], so that [outcome]". Non-functional requirements must specify measurable thresholds; the words "fast", "easy", "intuitive" and "secure" must not appear without an accompanying measure. Where a requirement derives from legislation, the requirement must cite the specific provision, and any simplification of legislative language must be verified by the legal team before the requirement is baselined. Draft requirements may be shared with delivery teams for early feedback, but only baselined requirements may be used for formal estimation.

**Question 9 (moderate) — True / False / Cannot say**

Statement: "A requirement stating 'The service must be easy to use' complies with the standard if user research supports it."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** The standard prohibits "easy" appearing "without an accompanying measure". Research support is not a measure: the requirement as stated specifies no measurable threshold (such as a task completion rate or a usability benchmark), so it breaches the standard regardless of what evidence sits behind it. The statement is false, not "cannot say", because the standard's rule is categorical about the wording itself. The professional point: evidence and expressibility are different quality dimensions — a requirement can be well-evidenced and still untestable as written. Turning "easy to use" into "a first-time user completes the application without assistance in under 10 minutes, achieved by at least 80% of usability test participants" is precisely the craft your Requirements definition and management skill names as making requirements traceable into test.

**Question 10 (moderate) — True / False / Cannot say**

Statement: "Delivery teams are prohibited from seeing requirements before they are baselined."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** The final sentence expressly permits sharing draft requirements with delivery teams for early feedback; the restriction applies only to using them for formal estimation. The statement inverts the standard's carefully drawn distinction between *seeing* (allowed, encouraged for feedback) and *formally estimating against* (baselined only). Standards frequently draw exactly this kind of distinction, and collapsing it in either direction causes real harm: prohibiting early sharing kills collaboration; allowing formal estimation on drafts bakes volatility into commitments. Reading a rule's precise scope — what activity it governs, and what it deliberately leaves free — is a core verbal skill for anyone who, like you, advises on the approach to requirements management across a programme.

**Question 11 (challenging) — Applying multiple rules**

A junior analyst drafts: "REQ-104: As a caseworker, I need to see an applicant's document history, so that I can make evidence-based decisions. (Derives from the Data Handling Act, summarised: records must be reviewable.)" The requirement has not been to the legal team. Under the standard, which single statement is most accurate?

- A) The requirement is fully compliant and may be baselined.
- B) The requirement follows the user-need format, but it cannot be baselined until the legal team verifies the simplified legislative language, and it must cite the specific provision rather than the Act generally.
- C) The requirement is non-compliant because caseworkers are not users.
- D) The requirement is non-compliant because it lacks a measurable threshold.

**Correct answer: B**

**Explanation:** Test the draft against each rule in turn. Format: it follows "As a / I need / so that" — compliant. Legislative derivation: the standard imposes two duties — cite the *specific provision* (the draft cites only "the Data Handling Act" with no provision) and have any *simplification* of legislative language ("summarised: records must be reviewable" is exactly that) verified by legal before baselining, which has not happened. So B captures both defects and the correct consequence: not baseline-able yet, though not irredeemable. C invents a rule — the standard nowhere restricts who counts as a user, and caseworkers are internal users. D misapplies the measurable-threshold rule, which the standard attaches to non-functional requirements; REQ-104 is functional. Multi-rule application questions reward exactly the systematic clause-by-clause checking you use when you review analysts' work against best practice you have developed — and the answer models good mentoring, too: name what is right, what is missing, and the path to compliance.

**Question 12 (challenging) — Clear-writing judgement on a requirement rewrite**

The draft requirement reads: "NFR-020: Search must be fast." Which rewrite best satisfies the standard while remaining faithful to the intent?

- A) "NFR-020: Search must be fast and intuitive for all users."
- B) "NFR-020: Search results must be returned quickly enough that users are satisfied."
- C) "NFR-020: Search results must be displayed within 2 seconds for 95% of queries under normal load, measured monthly from server logs."
- D) "NFR-020: The search infrastructure must be scalable."

**Correct answer: C**

**Explanation:** The standard requires non-functional requirements to specify measurable thresholds. Rewrite C supplies a threshold (2 seconds), a coverage level (95% of queries), a condition (normal load) and a measurement method (monthly, from server logs) — an objective procedure can determine compliance, which is the standard's own definition of testable. A adds a second banned word ("intuitive") and still measures nothing. B replaces one unmeasurable word with an unmeasurable clause — "quickly enough that users are satisfied" cannot be objectively verified as written. D changes the subject from response time to scalability, failing the faithfulness test: a rewrite must preserve intent, not substitute a different requirement. When you mentor analysts on requirement quality, this is the pattern to teach: quantity, coverage, conditions, measurement source. It converts an aspiration into an acceptance criterion.

### Preparation tips

- **Practise the three-way verdict.** For True/False/Cannot-say questions, rehearse the discipline: True means the passage guarantees it; False means the passage contradicts it; Cannot say means the passage neither guarantees nor contradicts. Most errors are False/Cannot-say confusions — ask "does the passage actually address this?" before choosing.
- **Underline modal verbs and qualifiers.** "Must", "may", "should", "only", "unless", "in principle", "subject to" — these small words carry the meaning. Reading with a deliberate eye for them transfers directly from tests to policy documents and stakeholder emails.
- **Set aside expertise.** You know how government grants and assessments really work; the test passage may describe a world that works differently. Answer from the passage alone — the same discipline you apply when a new policy overrides your assumptions from the last one.
- **Practise on real material.** GOV.UK service standards, published policy notes and your own programme's papers are ideal practice passages. Write three statements per passage — one true, one false, one unverifiable — and check your reasoning.
- **For clear-writing questions, apply a checklist.** Faithful to the source? Specific about actions, owners and dates? Free of new ambiguity? The best option usually wins on all three; distractors typically win on tone but lose on content.
- **Pace yourself by passage, not by question.** Read the passage once carefully (a minute is rarely wasted), then answer its cluster of questions quickly. Re-reading the passage from scratch for every question is the main cause of running out of time.

### Common pitfalls to avoid

- **Strengthened modality.** Distractors quietly turn "may" into "will" and "subject to assessment" into "automatically". If the statement is stronger than the passage, it is not true.
- **Answering from the world instead of the passage.** Your professional knowledge is an asset everywhere except inside a verbal reasoning test — and inside any task where the source document, not custom and practice, is authoritative.
- **Treating silence as denial.** A passage that does not mention something neither confirms nor denies it. "The passage doesn't say X is required" does not license "X is not required".
- **Scope creep in feedback reading.** When a stakeholder criticises one thing, do not read it as criticising everything — or as criticising nothing. Match your response to the feedback's actual scope.
- **Choosing polite over precise.** In clear-writing questions, warm but vague replies ("I'll action your comments") are traps. Specificity is what makes writing genuinely clear.
- **Conflating normative and empirical claims.** "Assessments must be completed in 15 days" does not mean they are. Keep rules and reality in separate mental columns — in tests, and in every process you model.

## Workplace job-specific situational judgement assessment

### About this assessment

A situational judgement assessment (SJT) presents realistic workplace dilemmas and asks you to judge the effectiveness of possible responses. Unlike cognitive or numeric tests, there is often no single objectively "right" action; instead, responses are scored against a framework of professional behaviours agreed with subject matter experts — for a role like yours, behaviours such as user focus, collaboration, ownership, appropriate escalation, developing others, and inclusion.

Typical format: an online assessment of 25 to 45 minutes presenting 8 to 15 scenarios. Common response formats include: choose the *most effective* response; choose the most effective *and* the least effective; rank all responses from most to least effective; or rate each response independently on an effectiveness scale. There is usually no strict time pressure per question, but the overall test is timed. Scoring compares your judgements to a key derived from experienced practitioners and the employing organisation's values — in government digital roles, that means the Service Standard's user-centred ethos and Civil Service behaviours strongly inform the key.

For a senior business analyst, the SJT is arguably the assessment closest to your real job. Your level is defined not by analysis alone but by leadership of analysis: you mentor others, develop best practice, own stakeholder relationships, and manage a community of practice. The hardest moments in your week are rarely analytical — they are judgement calls. What do you do when a stakeholder pressures you to soften a finding? When a mentee's work is not good enough two days before a deadline? When delivery pace and analytical rigour collide? When your recommendation is overruled? SJTs sample exactly these moments, and practising them builds a vocabulary for reasoning about them deliberately rather than instinctively.

### How this assessment maps to your role

- **Ownership and delivery focus** map to **Adapting to delivery methodologies** and your duty to negotiate delivery priorities: scenarios test whether you keep outcomes moving while being honest about trade-offs, and whether you communicate the value of iterative delivery instead of defending waterfall comfort zones.
- **Stakeholder influence and escalation** map to **Stakeholder relationship management**: identifying and resolving issues, influencing stakeholders, and building long-term strategic relationships — including judging when to persist, when to compromise, and when to escalate without burning trust.
- **Evidence integrity** maps to **Context, problem and option analysis** and **Business process improvement**: scenarios probe whether you protect the honesty of findings, baselines and options appraisals under political or commercial pressure.
- **Developing others** maps to your level's mentoring and best-practice duties and your **Testing (business analysis)** review responsibilities: SJTs for senior roles reliably include a struggling-colleague scenario, testing whether you balance support, standards and deadlines.
- **User focus and inclusion** map to **User experience analysis**: ensuring services meet business *and user* needs, including users who are digitally excluded or have accessibility needs, even when they are the least represented voice in the room.

### Practice questions

**Question 1 (easy) — Stakeholder pressure on a finding**

Your process analysis shows that a business unit's cherished workaround adds four days to case processing. The unit head, a key stakeholder whose cooperation you need for the next phase, asks you to remove the finding from your report because "it makes my team look bad". What is the most effective response?

- A) Remove the finding to preserve the relationship; you can raise it informally later.
- B) Keep the finding, but meet the unit head first to share the evidence, understand the workaround's origins, and agree how the report can present the finding fairly — including any genuine mitigations the unit has.
- C) Keep the finding unchanged and copy the unit head's director when you circulate the report.
- D) Offer to soften the wording so the four-day impact is no longer quantified.

**Correct answer: B**

**Explanation:** The tension is between evidence integrity and relationship management, and the best responses refuse to sacrifice either. Option B keeps the finding (integrity), engages the stakeholder before publication (respect and collaboration), seeks the workaround's context — workarounds usually exist for a reason, and that reason may itself be a finding — and offers fair framing rather than suppression. A sacrifices integrity and teaches the stakeholder that pressure works. C weaponises escalation before attempting resolution, damaging a relationship you own and need. D corrupts the evidence by removing the quantification that makes the finding actionable. The professional behaviours rewarded here are ownership of the analysis, collaboration before escalation, and honesty with respect — the combination your Stakeholder relationship management skill describes as resolving issues and influencing stakeholders while building long-term relationships.

**Question 2 (easy) — Mentee's work below standard**

A junior analyst you mentor submits a requirements catalogue for a workstream you oversee. It is due to the delivery team in three days, and your review finds pervasive problems: untestable requirements, missing identifiers, no traceability to business needs. The junior analyst has clearly worked hard. What is the most effective response?

- A) Rewrite it yourself tonight; the deadline is what matters.
- B) Return it with a note listing everything wrong and ask them to fix it by tomorrow.
- C) Sit down with them promptly, explain the main quality gaps with examples, work through fixing one section together so they see the standard, then agree a plan for them to complete the rest with a checkpoint before the deadline — while you decide whether to flag a possible short delay to the delivery team.
- D) Send it to the delivery team as-is; they can raise defects if it causes problems.

**Correct answer: C**

**Explanation:** Senior-level SJTs almost always include this scenario because it tests whether you can hold three commitments simultaneously: the person's development, the quality standard, and the delivery date. Option C does all three — teaching through worked example (the fastest way to transfer a standard), keeping the work with its owner (preserving their growth and confidence), inserting a checkpoint (managing delivery risk), and honestly assessing whether the deadline needs a conversation (transparency beats a heroic secret rescue). A meets the deadline but develops nobody and hides the capability gap; it also silently signals that your standard is "I'll fix it". B upholds the standard but delegates learning to a list — feedback without demonstration rarely lands, and an ultimatum deadline sets the mentee up to fail. D abandons both quality and the delivery team. Mentoring others and developing best practice are explicit duties of your level; this is what they look like on a Tuesday.

**Question 3 (easy) — User needs versus internal convenience**

In a prioritisation workshop, the operations manager argues for building an internal bulk-edit feature next sprint, while user research shows applicants are abandoning the journey because the eligibility checker gives confusing results. Both cannot fit. The operations manager is persistent and senior. What is the most effective response?

- A) Agree to the bulk-edit feature; operations keep the service running and their goodwill matters.
- B) Present the evidence for both items side by side — abandonment data and support costs for the checker, time saved for the bulk edit — recommend the checker fix on impact, and propose a committed slot for the bulk edit in the following sprint.
- C) Tell the operations manager that user needs always beat internal needs, as the Service Standard requires.
- D) Escalate the disagreement to the service owner without attempting to resolve it in the workshop.

**Correct answer: B**

**Explanation:** Option B does what analysis-led prioritisation is for: it converts an opinion contest into an evidence comparison, makes a clear recommendation (senior analysts recommend; they do not just facilitate), and treats the losing item respectfully with a concrete commitment rather than an indefinite deferral — which is what actually preserves the operations relationship. A trades user outcomes for comfort and teaches stakeholders that persistence beats evidence. C reaches a defensible conclusion through an alienating method: internal users are users too, and slogans invite resistance where evidence invites agreement. D escalates prematurely — escalation is the right tool when resolution genuinely fails at your level, not a substitute for attempting it. The behaviours scored: user focus, evidence-based decision making, and influencing through data — the heart of making prioritisation and minimum viable product decisions using analysis-led insights.

**Question 4 (moderate) — Discovering an inconvenient constraint late**

Two weeks before a planned public beta, your analysis of a policy document reveals a constraint nobody had spotted: a subset of applicants must receive a paper notification by law, and the service as built is digital-only for notifications. Raising it now will likely delay the beta; staying silent means launching non-compliant. What is the most effective response?

- A) Raise it immediately with the service owner and delivery manager, bring your analysis of which applicants are affected and rough options (delay; launch with a manual paper workaround for the affected subset; phased eligibility), and recommend one.
- B) Say nothing until after launch, then raise it as a fast-follow improvement.
- C) Email the policy team asking them to confirm your interpretation, and wait for their reply before telling anyone on the delivery side.
- D) Tell the delivery manager informally but ask them not to tell the service owner until you are certain.

**Correct answer: A**

**Explanation:** Legal non-compliance affecting citizens is a bright-line issue: the effectiveness key rewards immediate, open escalation with analysis attached. Option A does three senior things at once — surfaces the problem to the accountable people without delay, quantifies who is affected (turning a scare into a sized problem), and arrives with options and a recommendation rather than a bare alarm, which is the difference between escalating a problem and dumping one. B knowingly launches an unlawful service — indefensible regardless of delivery pressure. C confuses verification with delay: seeking policy confirmation is right, but it can run in parallel with alerting the team, and "waiting for certainty" is how two weeks becomes two days. D creates a concealment pact and inverts accountability — the service owner is precisely the person who must know. Understanding business and policy constraints and assessing their implications is a core duty of your role; this scenario tests whether you act on it when the implication is expensive.

**Question 5 (moderate) — Your recommendation is overruled**

After a rigorous options appraisal, you recommended Option A. The programme board, weighing factors including ministerial preference, chooses Option B — which your analysis shows carries materially higher delivery risk. The decision is made. What is the most effective response?

- A) Ask for your dissent to be minuted, then support the implementation of Option B fully — including reshaping your analysis to identify and mitigate Option B's specific risks.
- B) Continue arguing for Option A at each subsequent board until the decision is reversed.
- C) Support Option B publicly but privately tell your team the board got it wrong and the programme will probably fail.
- D) Ask to be moved to a different programme, since your professional advice was ignored.

**Correct answer: A**

**Explanation:** Boards are entitled to weigh factors beyond the analysis — that is what governance is for — and analysts are entitled, indeed obliged, to have their advice recorded. Option A gets both halves right: the minuted dissent preserves professional integrity and the audit trail, and full-hearted implementation support redirects your expertise to where it now adds most value — making the chosen option succeed by attacking its known risks. That last move is the mark of seniority: your risk analysis of Option B is suddenly the most valuable document in the programme. B relitigates a made decision, spending influence you will need later and stalling delivery. C is corrosive: public/private inconsistency destroys the team's confidence in both the board and you. D treats disagreement as grounds for exit, which no sustainable career or programme can support. The scored behaviours: ownership, resilience, honest record-keeping, and commitment to collective decisions — all central to working within governance while owning stakeholder relationships.

**Question 6 (moderate) — Community of practice under delivery pressure**

You run the business analysis community of practice for your business area. Your delivery manager asks you to cancel the next three monthly sessions because "the programme needs every hour". Attendance has been growing, and two junior analysts have told you the sessions are the main way they learn. What is the most effective response?

- A) Cancel the sessions; the programme's delivery needs are the priority.
- B) Refuse; professional development is protected time and the delivery manager has no authority over it.
- C) Explore the pressure with the delivery manager, then propose a proportionate adjustment — for example shorter sessions, or one session focused on a skill the programme immediately needs — and share evidence of what the community contributes to delivery quality.
- D) Keep running the sessions but stop advertising them, so attendance quietly falls and the conflict disappears.

**Correct answer: C**

**Explanation:** Managing community of practice activities is an explicit duty at your level, so the SJT is testing whether you defend it intelligently — neither capitulating nor entrenching. Option C treats the delivery manager's pressure as real (it usually is), then negotiates a solution that preserves the community's continuity while visibly serving delivery — turning a session toward a skill the programme needs is the classic win-win, and evidencing the community's contribution (fewer requirement defects, faster onboarding) reframes it from cost to investment. A abandons a leadership responsibility at the first challenge and tells junior analysts their development is expendable. B may be technically defensible but treats a negotiation as a jurisdiction dispute, damaging the relationship. D is passive avoidance dressed as compliance — the worst of both. Scored behaviours: developing others, collaboration, negotiation, and the long-term view that best practice needs a community to carry it.

**Question 7 (moderate) — Supplier resists analysis**

An external supplier building part of the service tells you their delivery is "requirements complete" and pushes back on your request to review their acceptance test coverage, saying the contract does not oblige them to share internal test artefacts. Your own traceability check suggests three requirements have no visible test coverage. What is the most effective response?

- A) Accept their position; contractual boundaries must be respected and challenging them risks the relationship.
- B) Share your traceability analysis with the supplier, naming the three requirements, and ask them to evidence how each will be verified — while checking with your commercial colleague what the contract actually says about acceptance evidence, and keeping your delivery manager informed.
- C) Publicly declare at the next programme meeting that the supplier is hiding test failures.
- D) Quietly write your own tests for the three requirements and say nothing.

**Correct answer: B**

**Explanation:** Option B applies pressure precisely where the evidence is: naming the three requirements converts a general demand ("show me everything") the supplier can lawyer against into a specific, reasonable question ("how will these be verified?") that is hard to refuse. Running the contractual check in parallel — through the commercial function, which owns that expertise — establishes your actual entitlements, and keeping the delivery manager informed means no one is ambushed later. A confuses respecting a contract with declining to verify acceptance — your Testing (business analysis) skill exists exactly for reviewing test plans and outcome reporting, and unverified requirements become production incidents. C makes an accusation ahead of evidence, poisoning a relationship the programme depends on. D hides a gap instead of closing it and lets the supplier's coverage stay unknown. Scored behaviours: constructive challenge, evidence-first influence, appropriate use of specialist colleagues, and transparency with your own side.

**Question 8 (moderate) — Inclusion in research and requirements**

Reviewing the user experience analysis for a new service, you notice all research participants so far are confident digital users recruited online, while operational data shows about 20% of the service's users currently come through assisted digital routes. The researcher says the deadline makes further recruitment impossible and "we can pick up edge cases in beta". What is the most effective response?

- A) Accept the researcher's plan; beta exists precisely to catch what alpha misses.
- B) Raise the gap with the researcher and service owner: 20% of users are not an edge case, the requirements and design will be skewed without them, and propose practical fast options — recruiting through the assisted digital support line, existing charity panels, or reviewing the deadline itself — while recording the risk if the gap stays.
- C) Insist the alpha is halted until a fully representative sample is achieved.
- D) Add your own assumptions about assisted digital users to the requirements, based on your experience of similar services.

**Correct answer: B**

**Explanation:** One in five users is a population, not an edge case, and requirements built only on confident digital users will systematically encode exclusion — the analysis you validate now is the service someone struggles with later. Option B challenges the framing with data, offers realistic recruitment routes (speed and inclusion are not always opposed; assisted digital users are reachable through the channels that serve them), engages the service owner who owns the deadline trade-off, and — critically — records the risk if the decision is still to proceed, so the gap is a managed choice rather than an invisible one. A rubber-stamps deferral of the users most likely to be harmed by a bad service. C may be disproportionate — halting everything is an option of last resort, and the scenario offers cheaper remedies first. D replaces missing research with unvalidated assumption, which is worse than a documented gap because it looks like evidence. Scored behaviours: inclusion, user focus, evidence integrity, and proportionate escalation — advising on the analysis, prioritisation and validation of user experience needs is your named skill, and validation is the word this scenario tests.

**Question 9 (challenging) — Most and least effective: conflicting stakeholder demands**

Two senior stakeholders give you contradictory steers in the same week. The finance director insists the options appraisal must recommend the lowest-cost option; the operations director insists anything that reduces headcount flexibility is unacceptable, whatever the saving. Your analysis genuinely supports a middle option that partially satisfies both. Identify the MOST effective and LEAST effective responses.

- A) Present the analysis to both stakeholders together, showing transparently how each option performs against cost, flexibility and other criteria, and recommend the middle option with the trade-offs explicit.
- B) Produce two versions of the appraisal, each emphasising what its recipient wants to see.
- C) Recommend the lowest-cost option, since finance ultimately controls the budget.
- D) Delay the appraisal until the two directors resolve their disagreement between themselves.

**Correct answer: Most effective A; least effective B**

**Explanation:** A is the disciplined play: one version of the truth, both stakeholders in the room (contradictory steers usually persist precisely because the principals never hear each other's constraints), evaluation criteria made explicit so the disagreement becomes a weighting discussion rather than a power struggle, and a clear recommendation — which is what your Context, problem and option analysis skill means by advocating recommendations to gain support. B is the least effective by a distance: two tailored versions of an appraisal is not diplomacy but a breach of analytical integrity that will be discovered the first time the directors compare papers, destroying your credibility with both — and credibility is the only currency an analyst's influence runs on. C capitulates to the loudest budget-holder without analytical justification; it is poor, but it is at least one honest document. D abdicates: the analysis exists precisely to give the directors a shared basis for resolving their disagreement, and waiting for consensus to precede evidence gets the sequence backwards. Scored behaviours: integrity, courage in influencing upward, transparency, and facilitation of collective decisions.

**Question 10 (challenging) — Methodology conflict in a multidisciplinary team**

You join a programme whose delivery teams work in two-week sprints, but the programme office requires a fully signed-off requirements specification before development starts — a hangover from the previous methodology. The teams are frustrated; the programme office cites audit obligations. As the senior business analyst, what is the most effective response?

- A) Side with the teams and advise them to start building from the backlog; documentation can catch up later.
- B) Side with the programme office; their audit obligation trumps team preference, so enforce full up-front specification.
- C) Design and propose a requirements approach that satisfies both needs — for example, a baselined set of high-level requirements and constraints for audit and traceability, elaborated just-in-time into detailed stories and acceptance criteria each sprint — and agree it with the programme office and the teams, iterating the standard as evidence accumulates.
- D) Ask the programme director to rule on which methodology wins.

**Correct answer: C**

**Explanation:** This scenario tests the skill your framework names directly: determining the approach for your role within the team's delivery methodology and advising on the requirements management approach within a programme. Option C recognises that the conflict is between two legitimate needs — iterative elaboration and audit traceability — not between right and wrong, and that a layered requirements model (stable baseline above, just-in-time detail below, with traceability between the layers) genuinely satisfies both. Crucially, C also agrees the approach *with* both parties and iterates it, modelling the "define and agree the scope of delivery" behaviour rather than imposing cleverness. A creates an audit exposure and teaches teams that governance is optional; B imposes waterfall documentation on iterative delivery, guaranteeing stale specifications and change-request churn — and misses your duty to clearly communicate the value of iterative delivery to those who have not yet seen it work. D escalates a design problem as if it were a dispute: rulings produce losers, designs produce adopters. Escalation remains available if your proposal is rejected — but it is the second move, not the first.

**Question 11 (challenging) — Evidence integrity versus programme optimism**

Drafting the quarterly benefits report, you find that the flagship process improvement is delivering roughly half its forecast saving, largely because uptake of the new digital channel is slower than the business case assumed. The programme manager, under pressure, suggests reporting the original forecast "since uptake will catch up" and notes that the benefits methodology "allows for judgement". What is the most effective response?

- A) Report the original forecast as suggested; forecasts are judgements and the programme manager owns the report.
- B) Report the actual measured benefit alongside a revised, evidenced forecast; include an uptake-recovery analysis showing what would need to be true for catch-up, and proposed actions to drive uptake — then discuss the draft with the programme manager before submission.
- C) Report the actual figure and add a note stating that the programme manager attempted to inflate the benefits.
- D) Ask to be removed from benefits reporting to avoid the conflict.

**Correct answer: B**

**Explanation:** The senior move separates three things the pressure is trying to merge: what has happened (measured benefit — non-negotiable fact), what may happen (a forecast — legitimately a judgement, but one that must now be re-evidenced against actual uptake), and what should happen (actions to close the gap). Option B reports all three, which is both honest and genuinely more useful to decision makers than either the stale forecast or the bare shortfall: the uptake-recovery analysis converts "we are behind" into "here is what catch-up requires and how we would drive it" — analysis in service of delivery, not just audit. Discussing the draft with the programme manager first is respect, not weakness: they may have context, and they deserve no surprises, but the numbers are not theirs to change. A launders hope as measurement; when actuals surface — and benefits actuals always surface — both your credibility and the programme's go with them. C turns a resolvable professional disagreement into an accusation of misconduct, skipping every intermediate step. D avoids the conflict by abandoning the exact duty — leading analysis and evaluation to assess business process improvements — that your role exists to perform under pressure, not just in fair weather. Scored behaviours: integrity, ownership, constructive challenge, and stakeholder respect.

**Question 12 (challenging) — Most and least effective: capability gap in the team**

A reorganisation gives you functional oversight of four business analysts across two teams. Within a month you observe that requirements quality varies wildly: one team's artefacts are exemplary, the other's regularly cause rework. The weaker team's analysts are open about it: "no one ever showed us a standard". Delivery pressure is constant. Identify the MOST effective and LEAST effective responses.

- A) Publish the exemplary team's artefacts as the standard, pair analysts across teams on live work, run a short community of practice series on the weakest areas, and track rework as the improvement measure.
- B) Report the weaker team's analysts to their line managers as a performance concern requiring formal management.
- C) Personally review and correct every artefact the weaker team produces before it is released.
- D) Wait two more months to gather more evidence before acting.

**Correct answer: Most effective A; least effective B**

**Explanation:** The analysts have told you the cause: absence of a standard, not absence of effort — and the scenario is testing whether you respond to the cause you were given. Option A is a complete senior-level intervention: it creates the missing standard from proven local practice (cheaper and more credible than importing one), transfers capability through pairing on live work (the fastest mechanism, and it builds relationships across the two teams), uses your community of practice machinery for exactly its purpose, and defines a delivery-relevant success measure — rework — so the investment justifies itself to the delivery managers. B is least effective: escalating a systemic gap as individual performance failure punishes people for a standard no one gave them, teaches the whole function that honesty about gaps is dangerous, and would poison your new functional relationship in its first month. C fixes artefacts but caps quality at your personal capacity, builds dependency rather than capability, and burns the hours you owe to senior-level work. D delays action on a cause you already understand — more evidence is a virtue when the diagnosis is uncertain, and a delay tactic when it is not. Scored behaviours: developing others, best-practice leadership, systemic rather than blame-first thinking, and measurement. This is your level's mandate — mentor others, develop best practice — executed as a system rather than a series of favours.

### Preparation tips

- **Learn the behaviour framework, not the answers.** SJT keys are built from professional behaviours: user focus, collaboration, ownership, honest escalation, inclusion, developing others. Before the test, write down how each behaviour shows up in your own role — the scenarios will feel familiar because they are.
- **Look for the response that holds two goods at once.** The best options rarely sacrifice integrity for relationships or delivery for quality; they find the move that serves both — evidence plus empathy, escalation plus options, standards plus support. Train yourself to spot the "and" answer among the "or" distractors.
- **Watch the escalation gradient.** Effective responses usually attempt resolution at the lowest sensible level first, escalate with analysis and options attached, and never escalate as a first resort or conceal as a last one. Bright-line issues — legal compliance, safety, evidence falsification — are the exception: escalate those immediately.
- **Rank by damage when unsure.** For most/least questions, the least effective option is usually the one that destroys trust or integrity irreversibly (tailored truths, concealment, public accusation), not merely the suboptimal one.
- **Rehearse with your own history.** Recall three genuinely difficult judgement calls from your career; write down what you did, what worked, and what the textbook response would have been. This reflection is the highest-value SJT preparation there is — and it doubles as interview preparation.
- **Answer as the role, at the level.** The key is calibrated to a senior analyst who mentors, owns relationships and leads practice. Responses that would suit a junior analyst (do the work yourself, wait to be told, escalate everything) score poorly at your level.

### Common pitfalls to avoid

- **Choosing conflict-avoidance dressed as diplomacy.** Removing findings, tailoring reports to audiences, and quiet workarounds all feel relationship-friendly and all score badly — because they trade long-term trust for short-term comfort.
- **Escalating too early or too late.** Bouncing every disagreement upward signals inability to influence; sitting on legal or ethical issues signals worse. Practise placing scenarios on the escalation gradient.
- **Heroic self-sacrifice.** Rewriting a mentee's work overnight or personally reviewing everything forever feels responsible but scores as poor delegation and failure to develop others. Senior roles are judged on building capability, not absorbing work.
- **Slogan-based reasoning.** "Users always come first" and "the contract is the contract" are half-truths; the key rewards applying principles through evidence and negotiation, not reciting them.
- **Ignoring the quiet stakeholder.** Scenarios often include an absent constituency — assisted digital users, junior staff, the supplier's delivery team. Responses that account for people not in the room score well because that is what inclusion means in practice.
- **Answering as your organisation actually behaves rather than as good practice requires.** If your current environment tolerates practices the framework would score poorly, answer to the framework. The test measures your judgement, not your habitat.

## Conclusion

Well done — you have worked through a substantial set of practice materials covering all four assessment types you are likely to meet as a senior business analyst: cognitive ability, numerical reasoning, verbal reasoning, and situational judgement.

Along the way, you have practised far more than test technique. You have checked requirements catalogues and process models for structural errors, traced dependency chains to their real consequences, recomputed pass rates, benefits projections and cost-per-transaction comparisons the way a careful reviewer must, read policy extracts and stakeholder emails with forensic attention to modality and scope, and weighed difficult judgement calls involving pressured stakeholders, struggling mentees, resistant suppliers, and users who were not in the room. Every one of those exercises maps directly to the named skills of your role: adapting to delivery methodologies, business modelling, business process improvement, context, problem and option analysis, requirements definition and management, stakeholder relationship management, systems analysis, testing, and user experience analysis.

A few encouragements as you move forward. First, remember that assessment performance is a skill in itself, and skills respond to practice: if some questions caught you out today, that is the practice doing its job. Revisit the explanations, notice the recurring patterns — denominators, necessary-versus-sufficient conditions, strengthened modality, the hold-two-goods-at-once heuristic in judgement scenarios — and try similar questions again in a week. Spaced repetition beats cramming for every assessment type here.

Second, treat the preparation tips as professional development, not just test preparation. The habits these assessments reward — reading the outcome clause, writing the denominator first, matching your response to feedback's actual scope, escalating with options attached — are the habits that make you a better analyst and a better mentor every day. Several of them are worth teaching directly in your community of practice sessions; explaining a technique to others is also the strongest way to consolidate it yourself.

Third, be confident in what you already bring. You lead complex analysis, own consequential stakeholder relationships, and develop the analysts around you; assessments simply sample, in miniature and under a clock, what you already do at scale. If you are preparing for a real assessment, find out the format, timing and provider in advance, complete any official practice tests offered, and look after the basics — rest, a quiet environment, rough paper, and a steady pace.

And whatever the outcome, keep investing in your development: seek feedback on your influence as well as your analysis, take on the ambiguous problems that stretch you, and keep sharing what you learn with the community you lead.

Good luck — you are better prepared than you were when you started reading. Keep going.
