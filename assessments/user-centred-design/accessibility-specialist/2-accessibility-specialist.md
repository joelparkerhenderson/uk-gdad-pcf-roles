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

<!-- APPEND -->
