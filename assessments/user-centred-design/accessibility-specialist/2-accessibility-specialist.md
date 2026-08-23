# Accessibility Specialist - Psychometric Assessment Resources

## Introduction

Welcome! This guide has been created especially for you as an accessibility specialist working within the UK Government Digital and Data profession. Whether you are preparing for an internal assessment, applying for a new post, benchmarking your own capability, or simply curious about how psychometric assessments relate to your day-to-day work, this document will help you practise, reflect, and build confidence.

Psychometric assessments are structured, standardised exercises that measure the mental capabilities and behavioural tendencies that predict success in a role. For an accessibility specialist, that means far more than abstract puzzles. The assessments described here are job-specific: they use the kinds of artefacts you genuinely handle — audit reports, WCAG success criteria, governance documents, training materials, test plans, and stakeholder communications — and the kinds of decisions you genuinely make, such as prioritising findings by user impact, advising a team on the right technical fix, assessing a project document against accessibility standards, and coaching a junior colleague through their first audit.

Why do these assessments matter for your role in particular? As an accessibility specialist, you support teams in creating accessible services. You perform accessibility audits and document findings clearly enough for others to work from. You provide advice, guidance, and recommendations based on specialist knowledge. You analyse governance and project documents against accessibility standards, resolve technical disputes between peers, coach and mentor junior colleagues, and bring the voice of disabled users into every conversation. Assessments of cognitive ability, numerical reasoning, verbal reasoning, and situational judgement map directly onto those demands. Practising them sharpens exactly the skills your role depends on: spotting the inconsistency in an audit table, interpreting assistive technology usage data accurately, extracting precise requirements from standards and legislation, and choosing the most effective course of action when a team pushes back on your findings.

This document is organised into four main assessment sections, each following the same pattern: an overview of what the assessment measures and why it matters for your role, a mapping of the assessment's dimensions to the specific skills in your role summary, a substantial set of practice questions with full worked explanations, practical preparation tips, and common pitfalls to avoid.

Here is how to get the most from it. First, read each "About this assessment" section so you understand the format before you meet it under time pressure. Second, attempt the practice questions honestly — commit to an answer before reading the explanation. Third, treat every explanation as a mini-lesson: even when you answer correctly, the reasoning walkthrough will deepen your technique, because the explanations tie each question back to the audits, advice, and advocacy you deliver in real life. Finally, use the preparation tips and pitfalls sections for self-reflection: they connect assessment performance back to your professional development as a specialist who is increasingly trusted to advise, audit, and coach.

Take your time, work steadily, and enjoy the practice. Let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive ability assessment measures the exact mental processes your role demands, using practical workplace scenarios rather than abstract puzzles. Instead of asking you to complete number sequences in a vacuum, it presents you with the everyday materials of your job — audit findings tables, WCAG conformance requirements, HTML and ARIA snippets, test conditions, governance checklists — and asks you to reason quickly and accurately about them.

The typical format is an online, timed test lasting 15 to 30 minutes, with questions covering pattern recognition, logical deduction, error checking, prioritisation, and applied problem solving. Scoring is objective, comparing your responses against a norm group at a similar level, and modern platforms often adapt question difficulty based on your previous answers — so a test that feels progressively harder is usually a test you are doing well on. Employers typically receive a breakdown of speed versus accuracy rather than a single score, so working both quickly and carefully matters. You will normally be offered short, ungraded practice questions before the real test begins.

For an accessibility specialist, cognitive assessment is particularly relevant because your professional value rests on structured, defensible thinking. When you perform a detailed audit, you hold a service's pages, components, states, and user journeys in mind simultaneously, checking each against dozens of success criteria without losing track. When you advise a team, you reason from a standard's requirements to a specific implementation's compliance. When you review a governance document, you detect what is missing as well as what is wrong. A well-designed cognitive assessment simulates precisely those demands in miniature — which means practising for it is also practising the craft itself.

### How this assessment maps to your role

The assessment dimensions map directly to the named skills in your role summary:

- **Pattern recognition** maps to your **Technical understanding (accessibility)** skill: performing detailed audits of websites, services, and documents means recognising recurring defect patterns — unlabelled controls, broken focus management, inconsistent landmark structure — across large, messy services, and noticing when a page deviates from an established pattern.
- **Logical deduction** maps to **Technical understanding (accessibility)** and **Consultancy**: advocating appropriate technical solutions requires reasoning validly from a success criterion's actual wording to what a given implementation must and must not do, and providing recommendations that follow from evidence rather than habit.
- **Error checking** maps to **Governance and assurance (accessibility)** and **Testing**: analysing project documents against a predefined framework, and analysing and reporting test activities and results, both depend on systematically detecting inconsistencies, omissions, and contradictions.
- **Prioritisation** maps to **Leadership and guidance** and **Testing**: making decisions characterised by managed levels of risk and complexity, and identifying issues and risks associated with work, requires rapidly ranking findings and tasks by user impact and urgency.
- **Problem solving** maps to **Consultancy** and **Communicating information**: framing problems so they can easily be understood, and troubleshooting to support the business in operating more effectively, is applied problem solving — decomposing a tangled situation into causes, options, and recommendations.

### Practice questions

**Question 1 (easy) — Pattern recognition in audit findings**

Auditing a six-page transaction, you record the count of "form field missing programmatically associated label" defects per page: Start 0, Personal details 4, Address 4, Contact 4, Review 0, Confirmation 0. The three affected pages all use the same recently rebuilt form component; the unaffected pages contain either no forms or forms built with the standard design system component. What is the most likely root cause?

- A) Three separate teams made three separate mistakes.
- B) The rebuilt form component omits label association, and every page using it inherits the defect.
- C) The audit tool produces false positives on alternate pages.
- D) The Review page is the source of the problem.

**Correct answer: B**

**Explanation:** The pattern is precise: defects appear exactly where the rebuilt component is used and nowhere else, with an identical count on each affected page. The most economical explanation is a single defect in the shared component, replicated wherever it is deployed. This matters practically: an audit that reports twelve separate findings sends developers to fix twelve symptoms, while an audit that reports one component-level root cause with twelve instances gets the whole problem fixed in one place — and your role summary asks you to document findings clearly for others to work from, which includes identifying root causes. Option A multiplies causes unnecessarily; option C invents tool failure despite a coherent pattern; option D confuses an unaffected page with a source. Component-level thinking is one of the marks of a maturing auditor.

**Question 2 (easy) — Logical deduction from a success criterion**

WCAG success criterion 2.1.1 (Keyboard) requires that all functionality be operable through a keyboard interface, with a narrow exception for functions that depend on the path of the user's movement (such as freehand drawing). A team tells you: "Our map's drag-to-pan cannot be done by keyboard, but we added keyboard buttons that pan the map in each direction." Based only on this, what is the most defensible assessment?

- A) Fail — drag-to-pan itself is not keyboard operable.
- B) Pass is plausible — the functionality (panning) is keyboard operable via the buttons; the criterion requires operable functionality, not identical interaction methods.
- C) Fail — maps are always exempt from WCAG.
- D) Pass — the path-dependent exception applies, so nothing keyboard-operable was needed at all.

**Correct answer: B**

**Explanation:** The criterion's object is functionality, not gesture. The functionality here is panning the map, and the buttons make panning operable by keyboard — a different mechanism achieving the same function, which is exactly the pattern the criterion permits. Option A misreads the requirement as "every input method must be replicated identically". Option C invents a blanket exemption that does not exist. Option D is subtler: even if drag-to-pan were argued to be path-dependent, the team did provide a keyboard alternative, so the exception is not what the pass rests on — and casually invoking exceptions when they are not needed is poor auditing discipline. Reading criteria precisely — what is the requirement's object, what exactly is excepted — is the deductive core of your **Technical understanding (accessibility)** skill, and the difference between advice teams trust and advice they learn to double-check.

**Question 3 (easy) — Error checking a conformance claim**

A project document claims: "The service meets WCAG 2.2 AA. Evidence: automated scan passed with zero errors on all pages." Reviewing this against your governance framework, which requires evidence proportionate to the claim, what is the central defect in the document?

- A) WCAG 2.2 does not exist.
- B) The evidence cannot support the claim: automated scans detect only a minority of WCAG failures, so a clean scan cannot demonstrate AA conformance.
- C) Zero errors is impossible, so the scan must be fabricated.
- D) The document should claim AAA instead.

**Correct answer: B**

**Explanation:** The claim is full AA conformance; the evidence is a clean automated scan. Automated tools reliably detect only a subset of success criteria — broadly the machine-decidable ones such as missing alt attributes or some contrast failures — and cannot judge criteria requiring human evaluation: meaningful alt text, logical focus order, clear labels and instructions, or usable assistive technology experience. A clean scan is therefore necessary-ish but nowhere near sufficient, and the document's inference from scan to conformance is invalid. This is precisely the analysis your **Governance and assurance (accessibility)** skill describes: assessing documents against accessibility standards and providing feedback. Your feedback here would be constructive: retain the scan evidence, and add manual audit and assistive technology testing evidence before the claim can stand. Option C is unfounded — clean scans on well-built pages are common; options A and D are simply wrong.

**Question 4 (moderate) — Prioritising a mixed workload**

Monday morning, four items compete for your attention:

1. A service team goes to their beta assessment Thursday; your audit re-test of their fixed critical issues is the outstanding evidence, and re-testing takes about a day.
2. A junior specialist you mentor has sent their first draft audit report, asking for feedback before their Friday deadline; review takes about two hours.
3. A governance board meets Wednesday morning and has asked for your written feedback on a project's accessibility approach; the read and response take about half a day.
4. Your quarterly contribution to the team's training materials is due at the end of the month.

Which sequencing is most defensible?

- A) 1 today, 3 Tuesday, 2 Wednesday or Thursday, 4 later in the month
- B) 2, 4, 1, 3 — help people and long-term assets first
- C) 3, 1, 2, 4 — governance always outranks delivery
- D) 1, 2, 3, 4 — strict order of when each request arrived

**Correct answer: A**

**Explanation:** Sequence by deadline and dependency together. Item 1 needs a full day and must be complete before Thursday's assessment — an immovable, high-stakes gate — so it takes today. Item 3 is due Wednesday morning and takes half a day, so Tuesday fits exactly. Item 2 is due Friday and takes two hours, fitting comfortably Wednesday or Thursday — and still leaves the junior colleague time to act on your feedback, which is the point of mentoring. Item 4 has weeks of slack. Option B front-loads the two least deadline-critical items and risks both the assessment evidence and the governance response. Option C sends the governance feedback first even though it is due a day later than the re-test is needed and takes half the time — impact-weighted scheduling beats category-based rules like "governance first". Option D confuses arrival order with priority. The reasoning pattern — duration, deadline, and downstream dependency considered jointly — is exactly how you manage an audit-heavy diary in real life.

**Question 5 (moderate) — Pattern recognition across assistive technology results**

Testing a custom date picker, you record: NVDA with Firefox — announces correctly; JAWS with Chrome — announces correctly; VoiceOver with Safari — announces nothing when the picker opens; TalkBack with Chrome on Android — announces correctly. All tests used the current released versions. What is the most reasonable next step?

- A) Record a global failure: the date picker does not work with screen readers.
- B) Record a pass: three out of four combinations work.
- C) Investigate the VoiceOver/Safari behaviour specifically — the pattern suggests an implementation detail that this combination handles differently — and record the finding with its exact scope.
- D) Advise users to avoid Safari.

**Correct answer: C**

**Explanation:** The results are not noise; they form a pattern — one browser-and-screen-reader pairing diverges while three agree. That typically points to an implementation technique with uneven support (certain ARIA patterns and live-region behaviours are handled differently by VoiceOver/Safari than by other pairings). The professional response is scoped precision: investigate, then document the finding as exactly what it is — "picker opening is not announced in VoiceOver with Safari" — with reproduction details, because your role requires documenting findings clearly enough for others to work from, and a developer can only fix what is precisely described. Option A overstates and will be half-refuted by the team's own testing, costing credibility. Option B understates: VoiceOver/Safari is the dominant combination among blind and low-vision Mac and iOS users, so "three of four" may exclude a large user group. Option D shifts the burden onto users, which is the opposite of your advocacy duty. Scoped findings, exact conditions, no overclaim — that is audit craft.

**Question 6 (moderate) — Logical deduction about a proposed fix**

A team's modal dialog traps keyboard focus correctly while open but, on close, returns focus to the top of the page rather than to the button that opened it. The developer proposes: "We'll just remove the focus trap — then there's nothing to return." What necessarily follows from this proposal?

- A) The original defect (wrong focus return) is resolved, and no new defect is introduced.
- B) A worse defect is introduced: while the modal is open, keyboard users can tab into the obscured page behind it, losing their place and interacting with hidden content.
- C) The proposal has no effect on keyboard users.
- D) The proposal fixes the issue for screen reader users only.

**Correct answer: B**

**Explanation:** Deduce the consequences of the change itself. The focus trap exists to keep keyboard interaction inside the open dialog; removing it means Tab moves into content that is visually obscured and logically inactive — a well-known, serious failure of dialog behaviour. Meanwhile the original complaint (focus returning to the wrong place on close) is not even addressed by the change: focus on close still has to go somewhere, and nothing in the proposal sends it back to the triggering button. So the proposal adds a defect without removing one. The correct advice — which your **Consultancy** skill frames as proposing approaches to implementation — is to keep the trap and set focus explicitly to the triggering element on close. The transferable technique: when evaluating any proposed fix, trace its effect on each user group and each state, not just on the sentence describing the bug.

**Question 7 (moderate) — Error checking an audit summary table**

Your draft audit summary states: "Total findings: 24 — of which 6 critical, 9 high, 10 low." The detailed findings list contains 25 rows. The severity counts in the detail are: critical 6, high 9, medium 0, low 10. Which correction restores consistency with the least change, assuming the detailed rows are correct?

- A) Change the total to 25 and investigate the discrepancy — one detailed row is missing from the summary arithmetic.
- B) Delete a low finding to make the total 24.
- C) Change a low finding to medium.
- D) Leave it — one row's difference is immaterial.

**Correct answer: A**

**Explanation:** Check the arithmetic first: 6 + 9 + 10 = 25, not 24 — so the summary's own severity counts already contradict its own total, and they match the detailed list's 25 rows. Given the stem's instruction that the detailed rows are correct, the minimal correction is the total: 24 becomes 25. The "investigate" clause matters too: a mismatch like this often signals a late-added finding that was never rolled up, and checking prevents the same slip elsewhere in the report. Option B destroys a genuine finding to preserve a typo — exactly backwards, and in an assurance document, quietly deleting findings is a serious act. Option C changes severity data for cosmetic reasons. Option D misjudges materiality: an audit whose totals do not add up invites the reader to distrust everything else in it. Reports that others act on — the heart of your documentation duty — must be internally consistent to the last row.

**Question 8 (moderate) — Applied problem solving in a training context**

You are designing a two-hour introductory accessibility training session for thirty developers, most of whom have never used a screen reader. Your goals: attendees should leave able to run a basic check and motivated to care. You have: a lecture deck, a hands-on exercise using a screen reader on their own code, a video of a disabled user struggling with a government service, and a quiz. Time allows three of the four. Evidence from your previous sessions shows hands-on exercises produce the largest capability gains and user videos produce the largest attitude shifts. Which combination best fits the goals?

- A) Deck, quiz, video — measurable and moving
- B) Deck (shortened), video, hands-on exercise — motivation plus capability, framed by essential context
- C) Deck, quiz, hands-on — skip the emotional content
- D) Video, quiz, hands-on — skip all context-setting

**Correct answer: B**

**Explanation:** Work backwards from the stated goals. "Able to run a basic check" is a capability goal, and your own evidence says hands-on practice drives capability — so the exercise is non-negotiable. "Motivated to care" is an attitude goal, and the evidence says the user video drives attitude — so it stays. That leaves one slot for either the deck or the quiz: a shortened deck supplies the framing novices need (what accessibility is, what the exercise will show them), while a quiz measures learning but does not cause much of it in a single session. Option A drops the highest-impact capability element; option C drops the highest-impact motivational element for an audience that has never encountered the human stakes; option D drops orientation entirely, which novice audiences need. This is your "support in providing training materials and learning content" duty as a design problem: match each component to the outcome it demonstrably produces, and spend limited time on the components that move your actual goals.

**Question 9 (hard) — Deduction across governance rules**

Your organisation's assurance framework states: (i) any service handling citizen transactions must have a completed accessibility audit before public beta; (ii) an audit is "completed" only when all critical findings are fixed and re-tested; (iii) the accessibility statement must be published at public beta launch and must list any outstanding non-critical findings. A service launches into public beta with: an audit performed, two critical findings fixed and re-tested, one critical finding fixed but not re-tested, four high findings outstanding, and an accessibility statement listing the four high findings. How many of the three framework rules are breached?

- A) 0
- B) 1
- C) 2
- D) 3

**Correct answer: C**

**Explanation:** Test each rule against the facts. Rule (ii): "completed" requires all critical findings fixed and re-tested; one critical finding is fixed but not re-tested, so the audit is not completed — rule (ii)'s definition is unmet, and consequently rule (i) is breached, because the service entered public beta without a completed audit. That is two rules engaged: (ii) defines, (i) is breached — but count carefully: rule (ii) is a definition the service fails to satisfy, which is itself a breach of the framework's requirement for completion, and rule (i) is breached as a consequence. Rule (iii): the statement was published at launch and lists the outstanding non-critical (high) findings — compliant. So two rules are breached and one is met, giving C. The precise habit this rehearses: governance rules interlock through definitions, and an unmet definition cascades. When you analyse governance documents against a predefined framework, tracing definitional dependencies — not just reading each rule in isolation — is what makes your feedback authoritative. (And practically: the missing re-test is a small task with outsized compliance consequences — exactly the kind of advice teams thank you for.)

**Question 10 (hard) — Multi-constraint audit scheduling**

You must audit four services — Alpha, Beta, Gamma, Delta — over the next four weeks, one service per week. Constraints: (i) Alpha's team is unavailable in week 1; (ii) Gamma must be audited before Delta, because Delta reuses Gamma's component library and you want component findings first; (iii) Beta's audit must be in week 1 or week 2 to feed its assessment; (iv) you need the junior specialist to shadow the Alpha audit, and they are only available in weeks 2 and 3. Which schedule satisfies all constraints?

- A) Week 1 Beta, week 2 Alpha, week 3 Gamma, week 4 Delta
- B) Week 1 Gamma, week 2 Beta, week 3 Delta, week 4 Alpha
- C) Week 1 Beta, week 2 Gamma, week 3 Alpha, week 4 Delta
- D) Week 1 Delta, week 2 Alpha, week 3 Beta, week 4 Gamma

**Correct answer: A**

**Explanation:** Apply the constraints as filters. Constraint (i) removes any schedule with Alpha in week 1 — all four options pass. Constraint (iv) requires Alpha in week 2 or 3: option B places Alpha in week 4, eliminated. Constraint (iii) requires Beta in week 1 or 2: option D places Beta in week 3, eliminated. Constraint (ii) requires Gamma before Delta: both remaining options (A and C) satisfy it, so check all constraints again precisely. Option C: Beta week 1 (fine), Gamma week 2, Alpha week 3 (junior available — fine), Delta week 4 (after Gamma — fine). Option A: Beta week 1, Alpha week 2 (junior available), Gamma week 3, Delta week 4. Both appear to satisfy the letter of all four constraints — so return to constraint (ii)'s stated rationale: component findings from Gamma should precede Delta, which both give. The discriminator is subtle: in option C the junior shadows Alpha in week 3, and in option A in week 2 — both allowed. But option C places Gamma in week 2 and Alpha in week 3, leaving the junior's other available week (2) unused for shadowing while Alpha's team, unavailable only in week 1, is kept waiting an extra week with no constraint requiring it. Where two schedules both satisfy hard constraints, prefer the one that completes constrained work earliest, preserving slack for slippage — option A audits Alpha at its earliest permissible week. A is the best schedule. This layered elimination — hard constraints first, then slack preservation as the tie-breaker — is exactly how you should build real audit calendars, because in real life something always slips.

**Question 11 (hard) — Root-cause reasoning from mixed evidence**

A service's error summary component behaves as follows: (a) with NVDA, errors are announced on form submission; (b) with VoiceOver, errors are announced twice; (c) with the JavaScript console open, you see the summary is rendered, removed, and re-rendered on each submission; (d) the component uses an ARIA live region with `role="alert"`. Which hypothesis best explains all the evidence?

- A) VoiceOver has a bug and the component is correct.
- B) The remove-and-re-render cycle inserts the alert content twice in quick succession; screen readers differ in how they de-duplicate rapid live-region updates, so some announce once and others twice.
- C) The live region should be removed entirely.
- D) NVDA is failing to announce one of two genuine errors.

**Correct answer: B**

**Explanation:** A strong hypothesis must explain all four observations. Evidence (c) is the key: the component does not update the summary in place; it tears it down and rebuilds it, which with `role="alert"` (d) can fire the alert twice — once per insertion, or once for the insertion after removal, depending on timing. Screen readers handle rapid duplicate alerts differently: some coalesce them (a — NVDA announces once), others announce each (b — VoiceOver announces twice). Option B accounts for (a), (b), (c), and (d) together and points directly at the fix: render once and update content in place, or manage the live region deliberately. Option A explains (b) only by blaming the tool and ignores (c) entirely — and "the screen reader is buggy" should be a hypothesis of last resort reached after your own implementation is ruled out. Option C throws away the announcement behaviour users need. Option D invents a second error the evidence never mentions. This is the troubleshooting discipline your **Consultancy** skill names: gather evidence across conditions, form the hypothesis that explains all of it, and advocate the technical solution that addresses the cause — not the symptom, and not the tool.

**Question 12 (hard) — Prioritisation under a governance dilemma**

An hour before a governance board meets to approve a service's public beta, you discover your audit re-test evidence contains an error: one of the three "critical — fixed and verified" findings was verified on the staging environment, but the fix is not present in the production build the board is approving. Fixing your evidence pack takes minutes; re-verifying against production takes half a day; the board meets in an hour. Which action best balances accuracy, governance, and delivery?

- A) Say nothing now; correct the record after the board meeting so approval is not disrupted.
- B) Ask the board to reject the service outright.
- C) Notify the board (via the chair) before the meeting: two criticals verified in production, one verified only in staging; recommend conditional approval with production re-verification within a defined period, or a short deferral — the board's choice, made on accurate evidence.
- D) Quickly re-run the staging test again so you can honestly say it was double-checked.

**Correct answer: C**

**Explanation:** The governing principle: assurance evidence exists so decision-makers decide on accurate information; the moment you know the evidence is wrong, allowing a decision on it converts an honest error into something much worse. Option C corrects the record at the right level and in time, and — crucially for your level — it frames options rather than seizing the decision: conditional approval with a dated re-verification is a routine, proportionate governance device, and deferral is the board's alternative. This respects the board's authority while making full use of existing arrangements, and it is exactly the "managed levels of risk" decision-making your **Leadership and guidance** skill describes. Option A is the classic integrity trap — comfortable for an hour, corrosive forever after, and it converts your future corrections into confessions. Option B overcorrects: nothing in the evidence says the fix is absent from production, only that it is unverified there; recommending rejection overstates what you know. Option D is motion without meaning: re-testing staging again answers a question nobody is asking — the gap is production, and re-running the wrong test twice does not close it. Under pressure, the strongest professionals narrow to the exact question: what do we know, what do we not know, and who needs to know it before deciding?

### Preparation tips

- **Practise on your own artefacts.** Take a recent audit report and stress-test it: do the totals add up, are findings scoped to exact conditions, are root causes separated from symptoms? Ten minutes of this per week trains the exact muscles the assessment measures.
- **Rehearse criterion-precise reading.** Pick one WCAG success criterion a day and articulate: its object, its scope, its exceptions, and one implementation that passes for a non-obvious reason. Deduction questions become straightforward when this is habitual.
- **Trace fixes to consequences.** For any proposed fix you encounter, spend one minute asking what it changes for each user group and state. This habit answers an entire category of assessment questions and improves your real advice.
- **Time-box your reasoning.** Cognitive tests reward decisive accuracy. Practise giving yourself 60 to 90 seconds per question, committing, and moving on — then review at the end.
- **Interleave testing types in your head.** Many questions turn on knowing what automated scans, manual checks, and assistive technology testing can each detect. Keep a crisp mental map of the boundaries.
- **Arrive rested and settle in.** Use the ungraded practice questions to acclimatise to the interface. Composure is worth several points.

### Common pitfalls to avoid

- **Reporting symptoms instead of causes.** Twelve instances of one component defect is one finding with twelve occurrences. Assessments — and developers — reward the root-cause framing.
- **Overclaiming from partial evidence.** "Fails in VoiceOver with Safari" is defensible; "doesn't work with screen readers" is not. Scope every conclusion to the conditions actually tested.
- **Blaming the tool first.** "The screen reader is buggy" is occasionally true and usually a reasoning shortcut. Exhaust implementation hypotheses before reaching for it.
- **Letting category rules replace judgement.** "Governance always first" or "mentoring always first" feel principled but lose to impact-weighted scheduling. Reason from deadlines, durations, and dependencies.
- **Preserving summaries over data.** When a summary and its detail disagree, the instinct to make the tidy number win is exactly wrong. Trust the detail, fix the summary, and investigate the gap.
- **Speed-reading conditional rules.** Framework rules interlock through definitions ("completed", "verified", "critical"). Misreading one definition cascades through every dependent answer.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment tests whether you can draw a defensible conclusion from data under time pressure. For an accessibility specialist the data is audit results, contrast ratios and other measured thresholds, service volumes translated into affected users, remediation effort estimates, and the assistive technology usage figures people quote at you.

The format is typically fifteen to twenty-five minutes with a calculator permitted, presenting tables and charts followed by multiple-choice items. Some questions are computational; others ask what the data does and does not support.

Three habits matter particularly in this role.

The first is that percentages of a service's user base are people, and converting them is the single most persuasive thing you can do with a number. A screen reader user population of 0.5% sounds negligible until you say it is four thousand people a year who cannot complete the form.

The second is that WCAG thresholds are precise numbers and you need them instantly — 4.5:1 for normal text, 3:1 for large text and for interface components, with large text defined as 24px regular or 18.66px bold. Being fast and exact here is what lets you settle a design disagreement in one sentence.

The third is that audit findings need normalising before they are compared. A service with more pages audited will produce more findings at the same quality, and comparing raw counts across services rewards small audits.

### How this assessment maps to your role

- **Threshold arithmetic** maps to **Technical understanding (accessibility)** and performing audits.
- **Converting rates into people** maps to **User focus** and bringing the voice of disabled users.
- **Normalising audit findings** maps to **Governance and assurance (accessibility)**.
- **Effort estimation** maps to **Consultancy**, where you advise teams on remediation.
- **Interpreting research** maps to **Testing**.
- **Presenting figures** maps to **Communicating information**.

### Practice questions

*Table 1 — Accessibility audit results across five services*

| Service | Annual users | Pages audited | Critical | Serious | Moderate |
|---|---|---|---|---|---|
| Apply | 940,000 | 28 | 4 | 17 | 26 |
| Book | 210,000 | 11 | 1 | 5 | 9 |
| Check | 1,600,000 | 44 | 9 | 33 | 41 |
| Report | 85,000 | 16 | 5 | 12 | 14 |
| Update | 430,000 | 13 | 2 | 6 | 11 |

**Question 1 (easy) — Reading a table**

Which service has the most critical issues?

- A) Apply
- B) Check
- C) Report
- D) Update

**Correct answer: B**

**Explanation:** Check has 9 critical issues, ahead of Report's 5 and Apply's 4. Note before drawing conclusions that Check also has the largest audit — 44 pages — so a larger surface produced more findings, which the next questions address.

**Question 2 (easy) — Total exposure**

Approximately how many annual users are served by services with at least one critical issue?

- A) About 2.5 million
- B) About 3.3 million
- C) About 1.6 million
- D) About 2.0 million

**Correct answer: B**

**Explanation:** All five services have at least one critical issue: 940,000 + 210,000 + 1,600,000 + 85,000 + 430,000 = 3,265,000, so about 3.3 million. That sentence — three and a quarter million people using services with known critical accessibility barriers — is more useful in a governance meeting than any count of findings, because it is the number that makes the problem feel like a problem.

**Question 3 (moderate) — Normalising by audit size**

Which service has the highest rate of critical issues per page audited?

- A) Apply
- B) Check
- C) Report
- D) Update

**Correct answer: C**

**Explanation:** Apply 4/28 = 0.14; Book 1/11 = 0.09; Check 9/44 = 0.20; Report 5/16 = 0.31; Update 2/13 = 0.15. Report has the highest rate at 0.31 per page, ahead of Check's 0.20. Normalising by pages audited is the right correction, since a larger audit finds more at the same quality — and it changes the answer from Question 1, which is the point. Note the tension it creates: the service with the worst rate serves the fewest users.

**Question 4 (moderate) — Prioritising remediation**

Which service should be prioritised, and on what basis?

- A) Report, because it has the worst defect rate.
- B) Check, because it combines the second-highest defect rate with 1.6 million users — so far more people encounter a critical barrier there than anywhere else — although neither the counts nor the rates tell you which journeys are blocked, and one critical issue on a mandatory step matters more than five on a rarely-visited page.
- C) Apply, because it has the second-most users.
- D) All five equally.

**Correct answer: B**

**Explanation:** The right basis combines rate with exposure, and Check dominates on the combination: a defect rate close to the worst applied to a user base nineteen times larger than Report's. Option B reaches that and then names the limitation that should shape what you ask for next — a journey-level rather than page-level view. Option A picks the rate alone. Option C picks users alone. Option D declines to prioritise, which is what happens when nobody does this arithmetic.

**Question 5 (moderate) — Contrast thresholds**

A designer proposes body text at 4.4:1, a 24px bold heading at 3.2:1, and a button border at 2.8:1. Which fail WCAG 2.2 AA?

- A) All three.
- B) The body text and the button border.
- C) Only the body text.
- D) Only the button border.

**Correct answer: B**

**Explanation:** Body text needs 4.5:1 and 4.4 falls short. The heading at 24px bold is large text, needing 3:1, and 3.2 passes. Interface components need 3:1 against adjacent colours, and a button border at 2.8 fails. So two of the three fail. Knowing these numbers instantly is what lets you resolve a design question in one sentence — and note how close two of the three are to their thresholds, which is worth flagging to a designer, since a later tweak to either colour would push them over.

**Question 6 (moderate) — Remediation effort**

Across the five services there are 21 critical, 73 serious and 101 moderate issues. Critical and serious average 90 minutes each to fix; moderate average 25 minutes. What is the approximate total effort?

- A) About 100 hours
- B) About 183 hours
- C) About 210 hours
- D) About 145 hours

**Correct answer: B**

**Explanation:** Critical and serious: 21 + 73 = 94 issues × 90 minutes = 8,460 minutes. Moderate: 101 × 25 = 2,525 minutes. Total 10,985 minutes = 183 hours, roughly five weeks of one person's time. That figure is what turns "we should fix the audit findings" into something that can be planned and funded — and note the concentration: the 94 higher-severity issues account for 77% of the effort.

**Question 7 (harder) — Users behind a percentage**

Roughly 2% of a service's users rely on screen magnification. The service has 940,000 annual users. A proposed change would make one journey difficult at high magnification. How should you frame this?

- A) 2% is a small proportion of users.
- B) About 18,800 people a year use magnification on this service, so the question is what "difficult" means for them — if the journey becomes unusable, that is 18,800 people a year unable to complete it, and the percentage is the least informative way to describe that.
- C) 18,800 users; the change must be rejected.
- D) The figure cannot be estimated.

**Correct answer: B**

**Explanation:** 940,000 × 0.02 = 18,800. The arithmetic is the smaller half of the item. What decides the response is the severity — difficult and unusable are very different — and option B holds both facts while making the count the headline. Option A uses the framing that makes the problem disappear. Option C converts a count into a verdict without establishing severity, which is the error that gets accessibility specialists characterised as obstructive.

**Question 8 (harder) — Interpreting an assistive technology statistic**

A stakeholder says "only 0.3% of our users use screen readers, so this is low priority". What is the strongest response?

- A) Accept it; 0.3% is small.
- B) Challenge what the figure measures: screen reader use is difficult to detect reliably, users who cannot complete a service leave and are undercounted, and the figure describes people who got far enough to be measured — so a low observed percentage is partly a consequence of the barriers, not a reason to leave them.
- C) Point out that 0.3% of 1.6 million is 4,800 people.
- D) Explain that accessibility is a legal requirement.

**Correct answer: B**

**Explanation:** The statistic is circular in a way that is easy to miss and important to name: a service that is hard to use with a screen reader will show few screen reader users, which then justifies not fixing it. Option B explains the mechanism. Option C is a genuinely good move and is stronger *combined* with B than alone, since a stakeholder who accepts the count may still believe the sample is representative. Option D is true and answers a prioritisation argument with an authority claim, which invites someone to look for the minimum compliance position.

**Question 9 (harder) — What the data supports**

An audit of a redesigned service finds 40% fewer issues than the previous audit. What is the strongest conclusion?

- A) The redesign improved accessibility by 40%.
- B) Fewer issues were found, which is consistent with improvement — but the comparison depends on both audits covering the same pages with the same method and auditor, and a smaller or differently-scoped audit produces fewer findings regardless.
- C) The redesign had no effect.
- D) Accessibility improved but not by 40%.

**Correct answer: B**

**Explanation:** Issue counts measure what was found, which is a function of what is there *and* how much was looked at and by whom. Option B states what the data supports and names the three things that would have to hold for the comparison to be valid. Option A treats a count difference as a measured improvement percentage, which is the version that appears in a slide deck. Option D asserts a smaller improvement with no more evidence than A had.

**Question 10 (harder) — Testing coverage**

An automated accessibility tool reports that a service passes all its checks. What proportion of WCAG success criteria can such tools typically verify, and what follows?

- A) Nearly all; the service is likely compliant.
- B) Automated tools reliably test only a minority of success criteria — commonly cited as around a third — because most criteria require judgement about whether something is meaningful, equivalent or in a logical order, so a clean automated result establishes the absence of one class of problem and says nothing about the rest.
- C) About half; further testing is optional.
- D) None; automated tools are unreliable.

**Correct answer: B**

**Explanation:** This is one of the most consequential facts in your role, because a clean automated report is routinely presented as evidence of compliance. Option B gives the proportion and, more importantly, the reason — criteria about meaningful alt text, logical focus order, and equivalent alternatives require a human judgement no tool can make. Option D overstates in the other direction; automated tools are genuinely valuable for the class of issue they catch. Option A is the belief you will spend a lot of your career correcting.

**Question 11 (harder) — Presenting to a governance board**

You have five minutes with a governance board to make the case for accessibility remediation. Which figure leads best?

- A) The number of outstanding critical and serious issues.
- B) The number of people using services with known critical barriers — around 3.3 million a year — alongside one concrete description of what a specific barrier means for one person trying to complete one task.
- C) The average audit score across services.
- D) The legal risk of non-compliance.

**Correct answer: B**

**Explanation:** Option B pairs the number that establishes scale with the example that establishes meaning, and boards need both — a count of people without an example is abstract, an example without a count is anecdote. Option A counts defects, which requires the board to know what a critical issue is. Option C averages away the finding. Option D is real and belongs later: leading with legal risk invites a compliance-minimising response, whereas leading with users invites a service-improving one, and you get the compliance benefit either way.

**Question 12 (harder) — Estimating from a small test**

Usability testing with 6 disabled participants found that 4 could not complete a task. What is the strongest statement?

- A) 67% of disabled users cannot complete the task.
- B) Four of six participants could not complete it, which is a strong signal that something is badly wrong — small qualitative samples are good at showing that a problem exists and poor at estimating how many people it affects, so the finding justifies investigation and fixing, not a percentage.
- C) The sample is too small to draw conclusions.
- D) About two-thirds of disabled users are affected.

**Correct answer: B**

**Explanation:** Six participants is a normal and appropriate size for this kind of testing, and it does a specific job: demonstrating that a barrier exists and showing you what it looks like. What it cannot do is support a population estimate, which is what options A and D attempt. Option C is least useful — it dismisses a finding that is actually very strong, since four failures out of six would be an extraordinary coincidence if the task were broadly usable. Knowing what a small qualitative sample proves and what it does not is central to using research credibly.

### Preparation tips

- **Convert percentages into annual user counts before discussing them.**
- **Know the WCAG thresholds cold.** 4.5:1 text, 3:1 large text and components.
- **Normalise audit findings by pages audited before comparing services.**
- **Combine rate and exposure when prioritising.**
- **Name the circularity in assistive technology usage statistics.**
- **Treat issue counts as a function of the audit as well as the service.**
- **Know what automated tools can and cannot verify.**
- **Use small qualitative samples to establish existence, not prevalence.**

### Common pitfalls to avoid

- **Comparing raw issue counts across audits of different sizes.**
- **Accepting a low assistive technology percentage at face value.**
- **Reading a clean automated report as compliance.**
- **Turning a six-participant finding into a population percentage.**
- **Reporting a 40% drop in findings as a 40% improvement.**
- **Leading a board conversation with legal risk.**
- **Describing thousands of affected people as a fraction of a percent.**

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment tests whether you can determine exactly what a piece of written material establishes. For an accessibility specialist this is unusually close to the work itself: reading WCAG success criteria, the accessibility regulations, procurement documentation and vendor conformance claims, and saying precisely what they require.

The commonest format presents a passage followed by statements to be marked True, False or Cannot Say. True means the passage establishes it, False means it contradicts it, and Cannot Say means it settles neither — regardless of what you know.

Your expertise is the principal hazard, and more so in this role than most, because you will frequently know the right professional answer while the passage is silent. It is worth noticing that this is also the discipline the job requires: the difference between what a standard requires and what is good practice is one you are asked to explain constantly.

Three specifics matter particularly.

The first is that success criteria have precise objects and narrow exceptions. A criterion about functionality is not a criterion about interaction method, and an exception that names one category does not stretch to a neighbouring one.

The second is that the regulations attach obligations with scope, timing and conditions — and your role includes governance and assurance, so a misread exemption becomes an organisational position rather than a personal error.

The third is that conformance claims are claims. A vendor accessibility statement, a supplier's conformance report, an audit summary — each tells you what someone asserted, and what was actually tested is a separate question.

### How this assessment maps to your role

- **Reading success criteria precisely** maps to **Technical understanding (accessibility)**.
- **Reading the regulations** maps to **Governance and assurance (accessibility)**.
- **Reading conformance claims** maps to **Consultancy** and advising on procurement.
- **Reading audit and test reports** maps to **Testing**.
- **Reading research about users** maps to **User focus**.
- **Explaining precisely** maps to **Communicating information**.

### Practice questions

*Passage A — for Questions 1 to 4*

"Public sector bodies must ensure their websites meet accessibility requirements and must publish an accessibility statement. Where meeting a particular requirement would impose a disproportionate burden, a body may rely on that exemption, provided it has carried out and documented an assessment of the burden and has stated the reliance in its accessibility statement. The disproportionate burden exemption does not apply to content essential to the use of the service. Pre-recorded time-based media published before 23 September 2020 is exempt. An assessment of disproportionate burden must consider the body's size and resources, the estimated costs and benefits, and the needs of disabled users."

**Question 1 (easy)**

Statement: A body relying on the disproportionate burden exemption must say so in its accessibility statement.

- A) True
- B) False
- C) Cannot Say

**Correct answer: A**

**Explanation:** Stated directly as one of the two conditions attached to the exemption. Note the exemption reinforces the accessibility statement obligation rather than reducing it — the statement is where reliance has to be declared, which is what makes the exemption auditable.

**Question 2 (moderate)**

Statement: A body may rely on the exemption if it has documented an assessment, even without declaring it in the accessibility statement.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The passage contradicts this: the exemption is available "provided it has carried out and documented an assessment ... **and** has stated the reliance". Both conditions are required, joined conjunctively. The statement treats one as sufficient, and in practice this is exactly the difference between a defensible reliance and an indefensible one — an undeclared exemption is invisible to the disabled users it affects, which is why the declaration is mandatory.

**Question 3 (moderate)**

Statement: A body can rely on disproportionate burden for the payment step of a transactional service.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The exemption "does not apply to content essential to the use of the service", and the payment step of a transactional service is essential by definition — without it the service cannot be completed. This is the most consequential clause in the passage and the one most often overlooked, because disproportionate burden is invoked precisely when something core is expensive to fix, which is the case the clause excludes.

**Question 4 (harder)**

Statement: A pre-recorded video published in 2019 and re-published in 2022 is exempt.

- A) True
- B) False
- C) Cannot Say

**Correct answer: C**

**Explanation:** The exemption applies to media "published before 23 September 2020", and the passage does not say how re-publication is treated — whether the original publication date governs or the later one does. A reasonable reading is that re-publishing constitutes publishing, which would defeat the exemption; another is that the content was published in 2019 and remains so. The passage genuinely does not settle it, and this is the sort of ambiguity worth resolving with your legal or assurance colleagues rather than by your own preferred reading, since your answer becomes the organisation's position.

*Passage B — for Questions 5 to 8*

"Success criterion 1.3.1 requires that information, structure and relationships conveyed through presentation can be programmatically determined, or are available in text. Success criterion 1.4.3 requires a contrast ratio of at least 4.5:1 for text, with exceptions for large-scale text at 3:1, incidental text, and logotypes. Incidental text is text that is part of an inactive user interface component, that is pure decoration, that is not visible to anyone, or that is part of a picture containing significant other visual content. Criterion 1.4.11 requires a contrast ratio of at least 3:1 for user interface components and graphical objects required to understand content."

**Question 5 (easy)**

Statement: Text on a disabled button is exempt from the 4.5:1 contrast requirement.

- A) True
- B) False
- C) Cannot Say

**Correct answer: A**

**Explanation:** The passage defines incidental text as including "text that is part of an inactive user interface component", and incidental text is one of the stated exceptions to 1.4.3. A disabled button is inactive, so its label is exempt. The passage establishes it. This is the item where professional judgement pulls hardest against the text — low-contrast disabled states are a genuine usability problem and many teams deliberately exceed the requirement — and both things are true simultaneously: the exemption exists, and relying on it is often a poor choice. Being able to say exactly that is what the role requires.

**Question 6 (moderate)**

Statement: A visual grouping of related form fields satisfies criterion 1.3.1 if it is visually obvious.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The criterion requires that relationships conveyed through presentation "can be programmatically determined, or are available in text". Visual obviousness is presentation, which is the thing the criterion exists to supplement — a grouping conveyed only by proximity and a border is unavailable to someone who cannot see it. So visual obviousness does not satisfy it; a fieldset and legend, or equivalent, would. The passage contradicts the statement.

**Question 7 (moderate)**

Statement: An icon that conveys information must have a contrast ratio of at least 4.5:1.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** Criterion 1.4.11 sets 3:1 for "graphical objects required to understand content", and an informational icon is such an object rather than text. The statement applies the text threshold to a non-text element. Note that an icon *at* 4.5:1 would comfortably satisfy 3:1 — the statement fails because it asserts 4.5:1 is required, which is not what the passage says. Applying the text ratio universally is a common error and it leads to rejecting compliant designs, which costs you credibility with teams.

**Question 8 (harder)**

Statement: Text within a photograph of a street scene must meet 4.5:1.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** Incidental text includes text "that is part of a picture containing significant other visual content", and a street photograph plainly contains significant other visual content. So text within it is exempt from the contrast requirement. The passage contradicts the statement. Note the exemption is about the text being incidental to a picture, not about it being unimportant — if the picture is being used to convey information, that raises a different criterion entirely, which the passage does not address.

*Passage C — for Questions 9 to 12*

"The supplier's accessibility conformance report states that the product conforms to WCAG 2.1 AA, with three criteria marked 'partially supports'. The report covers the product's default configuration. Testing was carried out by the supplier's internal team using automated tools and manual keyboard testing. No testing with screen readers was carried out. The report is dated 14 months ago. The supplier states that subsequent releases have not reduced conformance. Two of the three partially supported criteria relate to the reporting module."

**Question 9 (moderate)**

Statement: The product conforms to WCAG 2.1 AA.

- A) True
- B) False
- C) Cannot Say

**Correct answer: C**

**Explanation:** The report *states* conformance and simultaneously marks three criteria as "partially supports", which is not conformance for those criteria — and the testing that produced the claim included no screen reader testing at all. So the passage establishes what was claimed, not that the claim is true, and gives you specific reasons for doubt. Reading a conformance report as evidence of conformance rather than as an assertion is the central skill in assessing procurement documentation.

**Question 10 (moderate)**

Statement: The product has accessibility problems with screen readers.

- A) True
- B) False
- C) Cannot Say

**Correct answer: C**

**Explanation:** No screen reader testing was carried out, which establishes the absence of evidence rather than the presence of problems. The product might work well with screen readers; nobody has looked. This is the mirror image of the mistake in Question 9 — a report that omits a test tells you nothing in either direction, and asserting problems on that basis is as unsupported as asserting conformance.

**Question 11 (moderate)**

Statement: Conformance has not been reduced by releases since the report.

- A) True
- B) False
- C) Cannot Say

**Correct answer: C**

**Explanation:** The passage says "the supplier states" this. That establishes the assertion, not its truth — and the supplier is not a neutral party on whether their own releases affected conformance, particularly given that the original testing was also carried out internally and omitted screen readers. Fourteen months is a long time in a product's life. The professional response is to ask for a current report or test the current version.

**Question 12 (harder)**

Statement: A deployment using a configuration other than the default is covered by the report.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The report "covers the product's default configuration", which by its own scope statement excludes other configurations. So a customised deployment — which is what almost every government implementation is — falls outside what was tested. The passage contradicts the statement. This is the scope limitation most often missed in procurement, and it matters practically: the conformance report you were given may describe a configuration your organisation will never run.

### Preparation tips

- **Treat conjunctive conditions as all required.**
- **Read "essential to the use of the service" as a hard limit on burden exemptions.**
- **Check whether a threshold applies to text, large text, or components.**
- **Read the incidental text definition before deciding a contrast rule applies.**
- **Read a conformance report as an assertion, with a scope and a date.**
- **Note what a report says it did not test.**
- **Distinguish absence of evidence from evidence of a problem.**
- **Check whether a scope statement excludes the configuration you will run.**

### Common pitfalls to avoid

- **Applying the 4.5:1 text ratio to icons, borders and components.**
- **Treating a conformance report as conformance.**
- **Reading "no screen reader testing" as evidence of screen reader problems.**
- **Accepting a supplier's statement about their own subsequent releases.**
- **Assuming a default-configuration report covers your deployment.**
- **Applying a burden exemption to an essential step.**
- **Answering from good practice rather than from what the criterion requires.**

## Workplace job-specific situational judgement assessment

### About this assessment

A workplace job-specific situational judgement assessment presents realistic scenarios and asks you to identify effective and ineffective responses. For an accessibility specialist the scenarios involve advising teams who did not ask for advice, delivering audit findings people find inconvenient, coaching colleagues, and representing users who are never in the room.

The commonest formats ask for the most and least effective response, or for ratings. Scoring is against a key derived from experienced practitioners in comparable roles.

Three patterns run through the strong answers.

The first is that you work almost entirely by influence. You audit, advise and coach; you rarely decide. That makes how you deliver a finding as consequential as the finding, because a team that experiences accessibility as an obstacle will route around you, and a team that experiences it as help will bring you problems early.

The second is that accessibility failures are facts, not opinions. A contrast ratio either meets the threshold or it does not, and grounding a conversation in the measurement takes it out of the realm of taste — which protects both you and the team.

The third is that you represent people who are not present. Silence from you in a meeting is read as professional endorsement, and nobody affected is there to notice.

### How this assessment maps to your role

- **Advising teams** maps to **Consultancy** and providing support, advice and guidance.
- **Delivering audit findings** maps to performing accessibility audits and **Governance and assurance (accessibility)**.
- **Coaching** maps to coaching and mentoring more junior colleagues and **Leadership and guidance**.
- **Representing users** maps to **User focus** and bringing the voice of disabled users.
- **Working in multidisciplinary teams** maps to **Communicating information**.
- **Community contribution** maps to engaging with the cross-government accessibility community.

### Practice questions

**Question 1 (easy) — Delivering an audit finding**

Your audit of a team's service found twelve issues, several serious. How should you present them?

- A) Send the report with all twelve listed by severity.
- B) Send the report and talk it through — grouping issues by root cause where several share one, explaining what each means for a user trying to do something, and being clear which block a task and which degrade it.
- C) Send the report and offer to answer questions.
- D) Present only the serious issues to avoid overwhelming the team.

**Correct answer: B. Least effective: D**

**Explanation:** A list of twelve findings sends a team to fix twelve symptoms; grouping by root cause frequently reduces it to three or four actual changes, which is both more efficient and much less demoralising. Explaining the user impact is what makes a finding feel worth fixing rather than a rule being enforced. Option D is least effective: withholding findings means the team cannot plan remediation and will discover the rest later, which damages trust in the audit. Options A and C are reasonable and leave the interpretation to people less equipped to do it.

**Question 2 (easy) — A design that fails contrast**

You notice a designer's proposed palette fails contrast for body text. What is the most effective response?

- A) Raise it with the measured ratio, the required ratio, and one or two nearby colours that pass.
- B) Say the contrast looks too low.
- C) Raise it at the next design review.
- D) Note it for the audit.

**Correct answer: A. Least effective: D**

**Explanation:** Option A turns an observation into something immediately actionable and takes the conversation out of the realm of preference — a ratio either meets 4.5:1 or it does not. Bringing passing alternatives makes it collaborative rather than critical. Option D is least effective: saving a fixable problem for a formal audit means it gets built, costs far more to change, and makes the audit feel adversarial. Option C delays something that takes two minutes now. Option B is the right instinct expressed too vaguely to act on.

**Question 3 (moderate) — A team that did not ask for you**

You are assigned to advise a team who clearly regard accessibility work as an imposition. What is the most effective approach?

- A) Find something that makes their life easier early — a component that fixes several issues at once, a testing shortcut, an answer to a question they have been stuck on — because a team that experiences you as useful will bring you things, and one that experiences you as an inspection will hide them.
- B) Explain the legal obligations and the standards they must meet.
- C) Audit their service and present the findings.
- D) Ask their delivery manager to make attendance mandatory.

**Correct answer: A. Least effective: D**

**Explanation:** The relationship determines everything you can achieve, and option A invests in it deliberately — early usefulness buys the standing to raise difficult things later. Option D is least effective: mandating engagement produces attendance without cooperation and confirms exactly the framing you are trying to change. Option B leads with obligation, which is heard as a threat. Option C is your job and, as an opening move with a hostile team, arrives before you have any credit to spend.

**Question 4 (moderate) — Pressure to sign off**

A team asks you to confirm their service is accessible before launch. You have audited some journeys and not others, and no testing with disabled users has been done. What is the most effective response?

- A) Confirm it; your audit found the issues and they were fixed.
- B) Say precisely what was tested, against what standard, by what method, and what has not been covered — particularly testing with disabled users — because "is it accessible" is a question no single audit answers, and the team needs an accurate picture for their accessibility statement.
- C) Say it meets WCAG 2.2 AA.
- D) Decline to give any assurance.

**Correct answer: B. Least effective: A**

**Explanation:** An accessibility statement is a published document the organisation is legally required to get right, and it needs an accurate picture rather than a reassuring one. Option B gives them exactly that, including the largest gap. Option A is least effective because it converts your partial audit into an organisational claim you cannot support, and you will be the person asked about it. Option C is a more specific version of the same overreach unless a full audit against that standard was done. Option D withholds information you have and leaves them worse off.

**Question 5 (moderate) — A finding a team disputes**

A developer disputes one of your findings, arguing that the pattern is widely used and works fine. What is the most effective response?

- A) Ask them to show you it working in the assistive technology in question, and test it together — because either they are right and you have learned something, or the demonstration will show the problem more convincingly than any amount of citation.
- B) Cite the relevant success criterion.
- C) Accept their view; they know the codebase.
- D) Escalate to their lead.

**Correct answer: A. Least effective: D**

**Explanation:** A shared demonstration resolves this faster and better than argument, and it genuinely leaves room for you to be wrong — widely-used patterns are sometimes fine, and sometimes widely-used and broken. Option A also teaches the developer to test in the same way. Option D is least effective: escalating a technical disagreement turns a colleague into an opponent and gets a ruling from someone less able to judge it. Option B is correct and can become a citation exchange. Option C concedes a finding without testing it.

**Question 6 (moderate) — Coaching a junior colleague**

A junior colleague you mentor has written an audit report that lists issues accurately but reads as a series of rule violations. What is the most effective response?

- A) Show them how to reframe findings in terms of what a user cannot do, and explain why that lands better and gets more fixed — then let them rewrite it.
- B) Rewrite the report yourself.
- C) Tell them to make it friendlier.
- D) Send it as it is; the findings are accurate.

**Correct answer: A. Least effective: B**

**Explanation:** Option A transfers the reasoning, which is the part that generalises to every future report — a finding expressed as "a screen reader user cannot tell what this field wants" gets fixed more often than one expressed as "fails 3.3.2". Option B is least effective: it produces a good report once, teaches nothing, and signals that their work becomes yours when you disagree. Option C gives a direction without the means. Option D lets an accurate but ineffective report go out, and accuracy that does not lead to fixes has not achieved much.

**Question 7 (harder) — An inaccessible product being procured**

A product your organisation is procuring has significant accessibility problems. The procurement is well advanced. What is the most effective response?

- A) Set out the specific failures, what they mean for affected staff or users, and what obligations they create — then work the routes available at this stage: contractual remediation commitments with dates, an accessibility statement reflecting reality, and a documented decision by whoever accepts the risk.
- B) Recommend the procurement be stopped.
- C) Accept it; the decision is made.
- D) Raise it with the procurement team.

**Correct answer: A. Least effective: C**

**Explanation:** Late procurements are rarely stopped by an accessibility objection alone, and option A works the levers that do exist — supplier remediation commitments written into a contract are the most effective, because a supplier facing signature is far more responsive than one holding it. The named risk acceptance ensures the decision is made by someone accountable rather than absorbed silently. Option C is least effective: accepting an unmet legal obligation without recording it leaves nobody accountable and nothing improved. Option B is likely to fail and to be the last time you are consulted early. Option D is a step within A rather than a response.

**Question 8 (harder) — Silence in a meeting**

In a meeting running late, a decision is being taken quickly that will make a journey harder for screen reader users. Nobody else has raised it. What is the most effective response?

- A) Raise it now with the specific consequence and a rough sense of what addressing it would cost — because silence from you is read as professional endorsement, the people affected have no other representative in the room, and a decision is far cheaper to influence now than to revisit.
- B) Raise it now, briefly.
- C) Raise it with the decision owner afterwards.
- D) Note it and address it during implementation.

**Correct answer: A. Least effective: D**

**Explanation:** Option B is right and option A is stronger for one reason: adding a cost estimate turns an objection into something the meeting can actually decide in the time available, whereas an unquantified concern in a late-running meeting gets deferred. Option D is least effective: addressing during implementation a decision that creates the barrier means designing around it at much greater cost, and frequently means not addressing it at all. Option C loses the moment and requires reopening a settled decision.

**Question 9 (harder) — A team asking for a shortcut**

A team asks whether they can launch with a known accessibility issue and fix it in the next release. What is the most effective response?

- A) Say what the issue means for affected users, whether it blocks a task or degrades it, what the organisation's obligations are, and what would need to be in the accessibility statement — then let the accountable person decide, and offer an interim mitigation if one exists.
- B) Say no; known issues should not launch.
- C) Say yes if it is documented.
- D) Say it is their decision.

**Correct answer: A. Least effective: D**

**Explanation:** The decision belongs to whoever is accountable for the service, and your job is to ensure it is made knowingly. Option A supplies everything they need — including the accessibility statement consequence, which is often what makes the trade-off real — and offers the mitigation that frequently resolves it. Option D is least effective: it is technically true and abandons the advisory role entirely, leaving a decision to be made without the expertise you were brought in for. Option B removes the decision-maker. Option C treats documentation as sufficient regardless of severity.

**Question 10 (harder) — Findings that recur across teams**

Auditing across several services, you keep finding the same three issue types. What is the most effective response?

- A) Report them to each team as you find them.
- B) Treat the recurrence as a supply problem — the shared components or design tooling most teams use are probably producing these — and work on fixing them at source, since that removes the issues across every service at once.
- C) Produce guidance covering the three issue types.
- D) Propose accessibility training for developers.

**Correct answer: B. Least effective: A**

**Explanation:** The same three issues across independent teams is a signal about what they are all building with, not about their individual knowledge. Option B fixes the cause: a form component that requires a label to render, a palette without failing colours, a modal that manages focus correctly. Option A is least effective as the whole response — it fixes instances forever while the source keeps producing them, and it is the single most common way accessibility specialists exhaust themselves. Options C and D address knowledge, which is worth doing and does not stop a component that does the wrong thing.

**Question 11 (harder) — A statistic used to deprioritise**

A product manager says the analytics show almost no screen reader users, so the issues are low priority. What is the most effective response?

- A) Explain why the figure is unreliable — screen reader use is hard to detect, and users who cannot complete a service leave and are undercounted, so a low observed number is partly a consequence of the barriers — and convert what is measurable into people, then offer to include disabled participants in the next round of research.
- B) Explain that accessibility is a legal requirement.
- C) Point out that the percentage still represents thousands of people.
- D) Accept the prioritisation.

**Correct answer: A. Least effective: D**

**Explanation:** The statistic is circular in a way that is easy to miss and important to name — a service that is hard to use with a screen reader shows few screen reader users, which then justifies leaving it hard to use. Option A explains the mechanism, converts what can be converted, and offers the thing that actually settles it, which is research with disabled participants. Option C is a good move and stronger combined with A. Option B answers a prioritisation argument with an authority claim. Option D is least effective: accepting it leaves both the barrier and the reasoning intact for next time.

**Question 12 (harder) — Contributing to the community**

You have developed a testing approach that solved a problem several other departments are likely facing. What is the most effective response?

- A) Write it up and take it to the cross-government accessibility community, including the approaches that did not work, because the dead ends save other people more time than the solution does.
- B) Mention it to colleagues who ask.
- C) Keep the notes for your own use.
- D) Add it to your team's internal documentation.

**Correct answer: A. Least effective: C**

**Explanation:** Your role names engaging with and contributing to the cross-government accessibility community, and option A is the version that produces value — with the specific detail that failed approaches are frequently the most useful part, since they are what other people are about to spend a week on. Option C is least effective: it converts a solved shared problem into a solved private one, and everyone else solves it again. Option D helps your own team and nobody beyond it. Option B relies on other people knowing to ask, which they cannot.

### Preparation tips

- **Group audit findings by root cause and explain them as user impact.**
- **Bring the measurement and a passing alternative when raising a contrast issue.**
- **Invest in being useful before you need to be difficult.**
- **Say precisely what was tested and what was not.**
- **Resolve a disputed finding by testing together.**
- **Fix recurring issues at their source, not in each service.**
- **Name the circularity in assistive technology statistics.**
- **Attach a cost estimate when raising a concern in a late-running meeting.**

### Common pitfalls to avoid

- **Sending a list of twelve findings with no root-cause grouping.**
- **Saving a fixable design issue for a formal audit.**
- **Confirming that a service "is accessible".**
- **Escalating a disputed finding instead of demonstrating it.**
- **Rewriting a junior colleague's report yourself.**
- **Accepting a low assistive technology percentage as a prioritisation argument.**
- **Reporting the same issue to team after team.**
- **Staying silent in a meeting where a barrier is being created.**

## Conclusion

You have worked through four assessments built around the reasoning an accessibility specialist actually uses, and it is worth drawing them together.

The cognitive section was about reading patterns and rules precisely — recognising that twelve findings across three pages are one component defect, and that a success criterion's object is functionality rather than gesture.

The numeric section was about turning accessibility into numbers people act on. Convert percentages into annual users. Normalise findings by pages audited. Know the thresholds cold. And understand what a six-participant test proves — that a barrier exists, vividly — and what it does not, which is how many people it affects.

The verbal section was an exercise in reading the documents that define your professional territory. Both limbs of the disproportionate burden condition are required. The exemption does not reach essential content. A disabled button's label is exempt, and relying on that is often a poor choice. And a supplier conformance report is an assertion with a scope, a date, and — here — no screen reader testing behind it.

The situational judgement section was about working entirely through influence. The strong answers grouped findings by root cause and explained them as user impact, invested in being useful before being difficult, resolved a disputed finding by testing together rather than escalating, and fixed recurring issues at source instead of reporting them to team after team.

If one thread runs through all four, it is that your effectiveness is decided by how teams experience you. The same finding delivered as a rule violation and as "a screen reader user cannot tell what this field wants" gets very different responses, and the second one gets fixed. That is not about being agreeable — the standards are not negotiable and the measurements are facts — but about the fact that you cannot decide anything, so everything depends on people wanting to hear from you.

Good luck. You are in a role where the people who most depend on your judgement are never in the room, and the care you have given this is exactly the right kind.
