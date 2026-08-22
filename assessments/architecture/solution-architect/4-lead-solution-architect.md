# Solution Architect (Lead Solution Architect) - Psychometric Assessment Resources

## Introduction

Welcome. This document is a practical, role-specific preparation resource for psychometric assessments, written for you as a lead solution architect working within the UK Government Digital and Data (GDAD) Profession Capability Framework. Whether you are preparing for a formal assessment as part of a promotion, an internal development programme, or a move to a new department, this guide is designed to help you practise with confidence and to reflect on the mental skills your role genuinely demands.

Psychometric assessments are structured, standardised exercises that measure how you think, reason, and make decisions. They are widely used across the UK public sector because they are evidence-based, they reduce bias compared with unstructured judgements, and they predict on-the-job performance when they are properly targeted at the role. For a lead solution architect, that targeting matters a great deal: your daily work involves framing complex problems, weighing options under business and technical constraints, interpreting supplier costs and capacity figures, reading dense standards and governance documents, and navigating difficult conversations with senior stakeholders. Good assessments for your role therefore look very little like abstract puzzles and very much like a day in your working life, compressed and timed.

This document is organised around the four assessment types you are most likely to encounter:

1. A workplace job-specific cognitive ability assessment, measuring pattern recognition, logical deduction, error checking, and prioritisation using architectural artefacts.
2. A workplace job-specific numeric reasoning assessment, using budgets, licensing tables, capacity figures, and supplier comparisons of the kind you handle when giving commercial and technical advice.
3. A workplace job-specific verbal reasoning assessment, built on dense passages such as technology codes of practice, architecture governance terms of reference, and stakeholder correspondence.
4. A workplace job-specific situational judgement assessment, presenting realistic dilemmas involving senior stakeholders, junior architects you lead, suppliers, and delivery teams.

Each section explains what the assessment measures, maps it explicitly to the skills in your role profile, provides substantial practice questions with full worked explanations, and closes with preparation tips and common pitfalls.

How should you use this guide? First, work through the practice questions honestly, under light time pressure, before reading the explanations. Second, use the explanations as a self-reflection tool: they are written to show the reasoning a strong lead architect would apply, so compare your thinking with the model reasoning rather than just checking the answer letter. Third, return to the preparation tips shortly before any real assessment. You already exercise these capabilities every working day; this guide simply helps you demonstrate them deliberately, calmly, and at pace. Good luck, and enjoy the practice.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive ability assessment measures the exact mental processes your role demands, using practical workplace scenarios rather than abstract puzzles. Unlike a generic intelligence test, every question is built from the kinds of artefacts a lead solution architect really handles: architecture decision records, dependency diagrams, integration matrices, governance checklists, technology roadmaps, and risk registers. The assessment is typically delivered online, timed at around 15 to 30 minutes, and scored objectively against a benchmark or norm group of comparable professionals. Some modern platforms are adaptive, adjusting question difficulty based on your previous answers, and most provide short, ungraded practice questions first so you can get used to the interface before the clock starts.

For your role, this assessment matters because leading solution architecture is fundamentally a cognitive discipline. You are responsible for a group of solution architecture projects, or a single more complex area, and you may lead teams of more junior solution architects. That means you must hold multiple designs in your head at once, spot the inconsistency in a diagram that three other people have already reviewed, deduce the downstream consequence of a constraint change, and decide which of five competing demands genuinely needs your attention today. Employers use cognitive assessments at lead level to check that you can do this quickly and accurately under pressure, because at your level the cost of a missed logical flaw is measured in programme delays and public money.

Expect a mix of question styles: logical deduction from stated rules, error checking across paired documents, sequencing and dependency reasoning, pattern completion using technology lifecycle data, and prioritisation judgements. Speed matters, but so does accuracy: most report formats show employers your speed versus accuracy trade-off rather than a single score, so a rushed, careless run can look worse than a slightly slower, precise one.

### What it measures for your role

The dimensions of this assessment map directly onto the skills named in your role profile:

- **Problem definition and shaping.** Questions that ask you to identify what is actually being asked, spot hidden assumptions, and separate the stated problem from the real one test the same faculty you use when you lead the framing of a problem characterised by high complexity, complication, or risk, and when you help others challenge requirements and assumptions.
- **Making architectural decisions.** Logical deduction questions mirror the way you make and guide design decisions characterised by medium risk and complexity, and identify architectural risks that affect multiple teams or domains. Deducing that "if the payments service must be isolated, and isolation requires the new gateway, then the gateway is on the critical path" is exactly the reasoning tested.
- **Technical design throughout the life cycle.** Error-checking and consistency questions reflect your responsibility for creating and reviewing technical designs characterised by high risk, impact, and complexity, and for leading and guiding others in creating designs that achieve organisational objectives. Catching a contradiction between a design document and its interface specification is a daily lead-architect task.
- **Architect for the whole context.** Prioritisation questions test your ability to work to support wider organisational objectives beyond your immediate goals and to track emerging internal and external issues that could affect teams across the organisation.
- **Strategy design.** Sequencing and roadmap questions draw on your skill in directing the implementation of a strategy or vision, for example by creating roadmaps or plans, and defining architectural principles and patterns.

### Practice questions

**Question 1 (easy) — Logical deduction from architectural principles**

Your department's architecture principles state: (1) All citizen-facing services must use the shared identity platform. (2) Any service handling special category data must complete a Data Protection Impact Assessment (DPIA) before private beta. (3) Services using the shared identity platform must integrate with the central audit logging service.

A new benefits-eligibility checker is citizen-facing and handles health data (special category data). It is currently preparing for private beta.

Which of the following statements must be true?

- A) The service must complete a DPIA before private beta and must integrate with central audit logging.
- B) The service must complete a DPIA, but audit logging integration is optional at this stage.
- C) The service may defer the DPIA because the identity platform already provides assurance.
- D) The service must integrate with audit logging, but the DPIA is only required at public beta.

**Correct answer: A.**

**Explanation:** Work through the rules as a chain. The service is citizen-facing, so rule 1 applies: it must use the shared identity platform. Because it uses that platform, rule 3 applies: it must integrate with central audit logging. Separately, it handles special category data and is preparing for private beta, so rule 2 applies: the DPIA must be completed before private beta. Both obligations therefore hold, and nothing in the rules permits deferral or substitution. Options B, C, and D each quietly relax one rule that the principles state without qualification. In real governance reviews this is precisely how non-compliance slips through: someone assumes one control substitutes for another. The disciplined habit is to apply each rule independently unless an explicit exemption exists.

**Question 2 (easy) — Error checking across paired artefacts**

You are reviewing a junior architect's solution design pack before it goes to the design authority. The high-level design states: "The case management system will consume the address lookup API synchronously, with a 2-second timeout and a cached fallback." The accompanying interface catalogue lists the address lookup integration as: "Pattern: asynchronous message queue. Timeout: not applicable. Fallback: manual re-entry."

What is the most significant issue you should raise?

- A) The timeout of 2 seconds is too generous for a lookup API.
- B) The two documents describe contradictory integration patterns and fallback behaviours for the same interface.
- C) The interface catalogue should not mention fallback behaviour at all.
- D) Caching addresses may breach data minimisation rules.

**Correct answer: B.**

**Explanation:** The core cognitive skill here is consistency checking: the design says synchronous with a cached fallback; the catalogue says asynchronous with manual re-entry. These cannot both be implemented, and whichever team builds from the wrong document will produce an integration that fails testing or, worse, fails in production. Option A is a tuning opinion, not an error. Option C is false: interface catalogues routinely record failure behaviour. Option D raises a plausible-sounding concern, but the question gives no information about what is cached or for how long, so it is speculation rather than an identified defect. At lead level, your review value comes from spotting contradictions between artefacts, because authors rarely re-read their own pack side by side. The strongest answer is always the one that identifies an internal inconsistency with concrete delivery consequences.

**Question 3 (moderate) — Dependency sequencing**

You are planning a migration roadmap with five workstreams. The constraints are: the legacy database cannot be decommissioned until both the reporting service and the case service have migrated. The case service migration requires the new API gateway to be live. The reporting service migration requires the new data warehouse. The API gateway and the data warehouse can be built in parallel, but the same platform team must deploy both, and it can only deploy one per quarter.

If the platform team deploys the API gateway in Q1 and the data warehouse in Q2, and each migration takes one quarter after its dependency is live, what is the earliest quarter in which the legacy database can be decommissioned?

- A) Q2
- B) Q3
- C) Q4
- D) Q5

**Correct answer: C.**

**Explanation:** Trace each chain. API gateway live end of Q1, so the case service migrates during Q2 and is complete by the end of Q2. Data warehouse live end of Q2, so the reporting service migrates during Q3 and is complete by the end of Q3. Decommissioning requires both migrations to be complete, so the earliest the precondition is satisfied is the end of Q3, meaning the decommissioning itself happens in Q4. A common error is to answer Q3 by treating the reporting migration's completion and the decommissioning as the same event; another is to answer D by adding an unnecessary extra quarter of buffer. Assessments at this level deliberately test whether you distinguish "precondition satisfied" from "activity performed". In roadmap work this is the difference between telling a senior stakeholder a benefit lands this year or next, so precision matters commercially, not just logically.

**Question 4 (moderate) — Pattern recognition in technology lifecycle data**

Your technology radar tracks every platform component through the same lifecycle: Emerging, then Trial, then Adopt, then Contain, then Retire. At each annual review a component normally moves forward one stage. Two flags modify this: "accelerated" moves it forward two stages, and "hold" keeps it at its current stage. Retire is terminal: a component at Retire stays at Retire, and an accelerated move that would pass beyond Retire stops at Retire. Annual reviews took place in 2023, 2024, and 2025.

The 2022 positions were: Component P at Emerging, flagged accelerated in the 2023 review only. Component Q at Trial, flagged hold in the 2023 review only. Component R at Adopt, flagged accelerated in both the 2024 and 2025 reviews.

What are the statuses of P, Q, and R after the 2025 review?

- A) P: Retire; Q: Contain; R: Retire
- B) P: Contain; Q: Contain; R: Retire
- C) P: Retire; Q: Adopt; R: Contain
- D) P: Retire; Q: Retire; R: Retire

**Correct answer: A.**

**Explanation:** Step each component through the three reviews methodically. P starts at Emerging: the 2023 accelerated review moves it two stages, Emerging → Trial → Adopt; the 2024 review moves it Adopt → Contain; the 2025 review moves it Contain → Retire. P finishes at Retire. Q starts at Trial: the 2023 hold keeps it at Trial; the 2024 review moves it Trial → Adopt; the 2025 review moves it Adopt → Contain. Q finishes at Contain. R starts at Adopt: the 2023 review (no flag, so a normal single move) takes it Adopt → Contain; the 2024 accelerated review would move it two stages but caps at the terminal stage, so Contain → Retire; the 2025 review leaves it at Retire because Retire is terminal. R finishes at Retire. Only option A matches all three. The common errors are forgetting that R's unflagged 2023 review still moves it one stage (giving option C) and forgetting that the hold flag consumes a review cycle for Q (giving option D's overshoot on other components when applied inconsistently). This is exactly the discipline of tracking emerging technologies and approaches across a portfolio: apply the stated rules uniformly, one cycle at a time, and never let an exception flag on one item leak into your reasoning about another.

**Question 5 (moderate) — Prioritisation under competing demands**

It is Monday morning. Four items compete for your day: (1) A junior architect needs your review of a low-risk design going to governance on Thursday. (2) The programme director wants a same-day briefing on an emerging supplier insolvency risk that could affect three projects. (3) A delivery team is blocked right now on an integration decision you could make in 30 minutes. (4) Your quarterly architecture strategy paper is due to the design authority in two weeks.

Which ordering best reflects sound prioritisation?

- A) 3, 2, 1, 4
- B) 2, 3, 4, 1
- C) 1, 3, 2, 4
- D) 3, 1, 2, 4

**Correct answer: A.**

**Explanation:** Apply two lenses: urgency-impact and unblocking others. Item 3 is a live blocker on a whole team, resolvable in 30 minutes — the highest ratio of organisational benefit to your time, so do it first. Item 2 is same-day, senior, and affects multiple projects — a genuinely urgent, high-impact demand that follows immediately. Item 1 has a Thursday deadline; reviewing it today or tomorrow both work, so it comes third. Item 4 is important but has two weeks of runway; it is scheduled, not sacrificed. Option B fails because it leaves a team idle while you prepare a briefing. Options C and D elevate the routine review above the same-day senior risk briefing, misreading either urgency or impact. Notice the pattern in strong answers to prioritisation questions: quick unblocking actions first, then urgent-and-important, then deadline-driven, then important-but-distant — while ensuring nothing is dropped entirely. This mirrors the "architect for the whole context" skill: your calendar should serve the organisation's flow of work, not your personal task list.

**Question 6 (moderate) — Hidden assumption identification**

A programme board asks you to "select a cloud data platform so the analytics team can finally produce cross-departmental dashboards." During discovery you learn that the analytics team already has adequate tooling, but three source systems export inconsistent reference data, so every dashboard requires weeks of manual reconciliation.

What is the hidden assumption in the board's request, and what does sound problem shaping suggest?

- A) The assumption is that tooling is the constraint; the evidence points to a data standardisation problem, so reframe the problem before selecting any platform.
- B) The assumption is that dashboards are needed; you should challenge whether analytics adds value at all.
- C) The assumption is that the cloud is appropriate; an on-premises platform should be evaluated first.
- D) There is no hidden assumption; the board has stated a clear requirement that should be delivered as asked.

**Correct answer: A.**

**Explanation:** The board has embedded a solution ("select a cloud data platform") inside a problem statement ("we cannot produce dashboards"). Discovery evidence shows the real constraint is inconsistent reference data across source systems — a problem no new platform will fix, because the reconciliation burden would simply move onto the new platform. The lead-architect skill of problem definition and shaping is exactly this: ensuring a problem and the desired outcomes are properly defined before scoping a solution, and helping others challenge requirements and assumptions. Option B overcorrects into challenging the mission rather than the assumption. Option C swaps one premature solution debate for another. Option D is the compliant-but-costly path that leads organisations to buy platforms that disappoint. In the assessment, look for the option that separates the stated solution from the underlying problem and proposes validating the real constraint — that is nearly always the strongest answer, and it reflects how you coach junior architects to work.

**Question 7 (moderate) — Rule application with exception handling**

Your architecture governance framework states: designs with an estimated implementation cost under £100,000 and no new data sharing may be approved by a lead architect; designs involving new data sharing between departments must go to the design authority regardless of cost; designs over £1 million must additionally be notified to the central spend control team.

You receive three designs: Design X costs £80,000 and introduces a new data feed to another department. Design Y costs £950,000 with no new data sharing. Design Z costs £1.2 million and includes new cross-departmental data sharing.

Which routing is correct?

- A) X: design authority; Y: design authority; Z: design authority plus spend control notification.
- B) X: lead architect approval; Y: design authority; Z: spend control only.
- C) X: design authority; Y: lead architect approval; Z: design authority plus spend control notification.
- D) X: lead architect approval; Y: lead architect approval; Z: design authority plus spend control notification.

**Correct answer: A.**

**Explanation:** Apply each rule to each design. X is under £100,000, but it introduces new data sharing between departments, and the data sharing rule applies "regardless of cost", so X goes to the design authority — the cost threshold cannot rescue it. Y is £950,000: over the £100,000 lead-architect limit, so it exceeds delegated approval and must go to the design authority; it is under £1 million, so no spend control notification. Z is over £1 million with new data sharing, so it needs both the design authority and the spend control notification. Option C is the classic trap: it treats Y's lack of data sharing as sufficient for delegated approval while forgetting that the £100,000 cost ceiling independently rules it out. The cognitive skill is conjunction handling — delegated approval requires both conditions (under £100,000 and no new data sharing), while escalation triggers are disjunctive (any one condition suffices). This mirrors how you use architectural governance and assurance to make design decisions at the appropriate level: knowing precisely which forum owns which decision is a core part of contributing to the development of governance itself.

**Question 8 (hard) — Multi-constraint solution elimination**

You must recommend an integration approach for a new grants service connecting to a legacy finance system. Constraints: (1) The finance system supplier permits only file-based batch interfaces or its licensed API gateway. (2) The grants service must show payment status to caseworkers no more than 15 minutes after a change. (3) The licensed API gateway costs £250,000 per year, and the programme's residual integration budget is £150,000 per year. (4) Security policy prohibits direct database access between systems. (5) A batch interface can run at most every 10 minutes without breaching the finance system's overnight processing window, but each run only completes within 10 minutes if the file contains fewer than 50,000 records; daily change volume is around 30,000 records spread across the day.

Which approach satisfies all constraints?

- A) Direct read-only database replication from the finance system.
- B) The supplier's licensed API gateway, funded by reducing other integration work.
- C) File-based batch interface running every 10 minutes with incremental change files.
- D) A daily overnight batch file plus a caseworker warning banner about data staleness.

**Correct answer: C.**

**Explanation:** Eliminate options against constraints, one at a time. A breaches constraint 4 (no direct database access) and also constraint 1 (the supplier permits only two interface types). B satisfies the freshness requirement but breaches constraint 3: £250,000 exceeds the £150,000 budget, and the option's "reduce other work" wording changes the budget question rather than answering it — in an assessment, treat stated budgets as fixed unless the question says otherwise. D breaches constraint 2: overnight data can be almost 24 hours stale, and a warning banner mitigates but does not meet a stated 15-minute requirement. C works: incremental files every 10 minutes deliver changes well inside the 15-minute freshness bound; 30,000 changes per day spread across roughly 144 runs is on the order of a few hundred records per file, comfortably below the 50,000-record limit; file-based batch is supplier-permitted; and no gateway licence is needed. The strong habit demonstrated here is systematic elimination: check every option against every constraint rather than stopping at the first attractive candidate. This is exactly how you make architectural decisions within business and technical constraints, and how you document a decision record showing why rejected options were rejected.

**Question 9 (hard) — Logical consistency in a risk register**

A programme risk register contains these four entries: (R1) "If the identity supplier exits the market, all three citizen services lose their login capability." (R2) "Service A has a contingency login route that does not depend on any external supplier." (R3) "The identity supplier's exit would not affect Service B because Service B uses the in-house identity module." (R4) "All three citizen services (A, B, and C) depend solely on the external identity supplier for login."

Which pair of entries is directly contradictory?

- A) R1 and R2
- B) R2 and R4
- C) R1 and R3
- D) R3 and R4 only

**Correct answer: B.**

**Explanation:** Test each pair precisely. R2 states Service A has a supplier-independent contingency login; R4 states all three services, including A, depend solely on the external supplier. "Solely" and "has an independent contingency" cannot both be true of Service A, so R2 and R4 are directly contradictory. What about the others? R1 and R2 can coexist: R1 says services "lose their login capability" — arguably in tension with a contingency, but R1 could be read as describing the primary route, so the contradiction is not direct; more importantly, R1 does not use exclusive language. R1 and R3 are in tension (R1 says all three services are affected, R3 says B is not), and R3 and R4 likewise conflict — but note the question asks for the pair that is directly contradictory, and option D says "R3 and R4 only", which is falsified by the R2–R4 contradiction also existing. The sharpest single contradiction on exclusive wording is R2 versus R4. This is the kind of forensic reading you apply when you manage risks and decisions in a transparent way: registers accrete entries from different authors over months, and the lead architect is often the only person who reads them as a whole. Spotting that two entries cannot both be true is what turns a register from a filing exercise into a decision tool.

**Question 10 (hard) — Sequencing a strategy rollout with feedback loops**

You are directing the implementation of a new architecture strategy across four domains: Case Management, Payments, Data, and Channels. Your rollout rules: each domain requires a published target architecture before its teams can start aligned delivery; the Data domain's target architecture cannot be finalised until Payments has completed its data-flow mapping; Channels must not start aligned delivery until at least two other domains have delivered one aligned release each, so lessons can be incorporated; you have capacity to publish only one target architecture per month, and each domain delivers its first aligned release two months after its target architecture is published.

If you publish target architectures starting in January, which publication order allows Channels to start aligned delivery at the earliest date, and when is that?

- A) Payments (Jan), Case Management (Feb), Data (Mar), Channels (Apr); Channels starts in May.
- B) Case Management (Jan), Payments (Feb), Data (Mar), Channels (Apr); Channels starts in June.
- C) Payments (Jan), Case Management (Feb), Data (Mar), Channels (Apr); Channels starts in April.
- D) Data (Jan), Payments (Feb), Case Management (Mar), Channels (Apr); Channels starts in May.

**Correct answer: A.**

**Explanation:** Work the timeline. Publishing Payments in January means its first aligned release lands in March (two months later). Case Management published in February delivers its first aligned release in April. Those are the two aligned releases Channels needs, so the "two domains, one release each" condition is met at the end of April — but check the other conditions too. Data cannot be finalised until Payments completes data-flow mapping; publishing Data in March, after Payments has had January and February to progress, respects that dependency. Channels' own target architecture is published in April, and Channels can start aligned delivery once both its target architecture exists and two other domains have delivered — both true from end of April, so Channels starts in May. Option C claims April, but in April Case Management's release is only just landing and Channels' target architecture is only just published; starting the same month ignores the sequence of preconditions. Option B wastes a month by ordering Case Management before Payments, delaying the Data dependency chain and, on stricter readings, the second release. Option D publishes Data first, violating the Payments-before-Data dependency outright. The examined skill is exactly what strategy design means in practice: creating roadmaps where dependency logic, capacity limits, and feedback loops are all honoured simultaneously — and being able to defend the ordering to a programme board.

**Question 11 (hard) — Error checking in a capacity model**

A junior architect's capacity note for a document-processing service reads: "Each worker node processes 400 documents per hour. Peak demand is 12,000 documents per hour. We therefore need 30 worker nodes. Allowing for the standard resilience requirement that the service must tolerate the loss of any 2 nodes while still meeting peak demand, we will provision 32 nodes. Since each node costs £300 per month, the total compute cost is £9,000 per month."

Which single statement in the note is wrong?

- A) The calculation that 12,000 divided by 400 requires 30 nodes.
- B) The resilience adjustment from 30 to 32 nodes.
- C) The total cost figure of £9,000 per month.
- D) Nothing is wrong; the note is internally consistent.

**Correct answer: C.**

**Explanation:** Verify each claim independently. First, 12,000 ÷ 400 = 30, so 30 nodes meet peak demand — correct. Second, tolerating the loss of any 2 nodes while still meeting peak means 30 must remain after 2 fail, so provision 32 — correct reasoning. Third, the cost: 32 nodes at £300 per month is 32 × 300 = £9,600, not £9,000. The note has multiplied using the pre-resilience count of 30 nodes (30 × 300 = £9,000) — a classic stale-number error, where an earlier intermediate value survives into a later calculation after the input changed. This is one of the most common defects in real design packs: a figure is updated in one paragraph but not in the summary or the cost table. Assessments test it because catching it requires you to recompute rather than skim, and lead architects who recompute are the ones who catch the £600-per-month, £7,200-per-year discrepancies before finance does. When you review designs, make a habit of tracing every derived number back to its stated inputs; when a document has been revised, stale numbers cluster around whatever changed last.

**Question 12 (hard) — Prioritising architectural risks across domains**

Four risks sit on your portfolio radar: (1) A deprecated messaging library used by six teams reaches end of support in 14 months. (2) A single subject-matter expert holds all knowledge of the tax calculation engine and retires in 3 months. (3) A supplier's roadmap suggests, unconfirmed, that a product two teams use may be discontinued in 2 to 3 years. (4) An accessibility audit found that a shared component fails WCAG criteria, exposing every consuming service to compliance failure at its next service assessment; two services are assessed within 6 weeks.

Ranked by what needs action first, which ordering is most defensible?

- A) 4, 2, 1, 3
- B) 2, 4, 1, 3
- C) 1, 4, 2, 3
- D) 4, 1, 2, 3

**Correct answer: A.**

**Explanation:** Score each risk on proximity, impact breadth, and reversibility. Risk 4 combines the nearest hard deadline (assessments in 6 weeks), broad impact (every consuming service), and a public-sector legal and values dimension (accessibility is both a compliance requirement and a duty to users) — it acts first. Risk 2 is next: three months to retirement is close, and lost expert knowledge is effectively irreversible — once the expert leaves, recovery costs multiply; knowledge capture and succession must start immediately even though the deadline is slightly further out than risk 4's. Risk 1 has genuine breadth (six teams) but 14 months of runway; it needs a plan and a milestone now, and active work soon, but it follows the two nearer cliffs. Risk 3 is unconfirmed and 2 to 3 years out: the proportionate action is monitoring and supplier engagement, not immediate mobilisation. Option B is defensible-sounding but underweights the 6-week statutory-style deadline relative to the 3-month one; when two risks are both urgent, the one with the nearer immovable date and wider blast radius leads. This question exercises the "architect for the whole context" skill directly: tracking emerging internal and external issues over time, then converting them into a transparent, defensible ordering of action — and being able to explain that ordering to the teams whose priorities it changes.

### Preparation tips

- **Practise with your own artefacts.** Take a real (suitably anonymised) design pack, risk register, or roadmap and interrogate it: what contradicts what, which numbers do not recompute, which dependency is undeclared? This is the highest-fidelity practice available to you, because the assessment deliberately imitates these documents.
- **Rehearse elimination, not inspiration.** At lead level, hard questions are usually constraint-satisfaction problems. Train yourself to check every option against every stated constraint methodically. The right answer is often the last one standing, not the first one that appeals.
- **Read the logical connectives with a lawyer's eye.** Words like "solely", "regardless of cost", "at least two", "unless", and "only" carry the whole question. Underline them mentally; most wrong answers exist because a connective was skimmed.
- **Manage the clock strategically.** With 15 to 30 minutes for the whole test, no single question deserves more than a proportionate share. If a question resists you after 90 seconds, flag it, choose your best elimination-based candidate, and move on. Accuracy on ten questions beats perfection on four.
- **Warm up your working memory.** Dependency-chain questions reward holding three or four facts active at once. Doing two or three practice items immediately before the assessment measurably reduces early-question errors while you settle in.
- **Trust your professional maturity.** You review complex designs for a living. The assessment format is unfamiliar; the thinking is not. Treat each question as a miniature design review and your instincts will serve you well.

### Common pitfalls

- **Answering from experience instead of from the question.** You will recognise scenarios and be tempted to apply what your organisation actually does. Assessments score against the rules stated in the question; suppress your local conventions and reason only from the given text.
- **Stopping at the first plausible option.** Question writers place an attractive near-miss early in the option list. Verify your candidate against every constraint before committing — the near-miss usually violates exactly one.
- **Losing track of stale numbers.** When a scenario updates a figure mid-passage, earlier derived values become invalid. Recompute anything the update touches, as in the capacity-model question above.
- **Misreading conjunctions and disjunctions.** Delegation rules that require all conditions, and escalation rules that trigger on any condition, are systematically confused under time pressure. Slow down for exactly these sentences.
- **Spending your best minutes on the hardest question.** Speed-versus-accuracy reporting means an unanswered easy question costs more than an abandoned hard one. Bank the accessible marks first.
- **Ignoring the interface practice round.** The ungraded warm-up questions exist to absorb your interface mistakes. Use them deliberately — check how to flag, skip, and return to questions before the timer starts.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment evaluates your ability to analyse, interpret, and make sound decisions using numerical data drawn from your actual working context. It is emphatically not a mathematics exam: the arithmetic rarely goes beyond percentages, ratios, weighted comparisons, and cost projections. What it measures is whether you can extract the right numbers from a realistic table or chart, apply business logic to them, and reach a defensible conclusion quickly. Most assessments allow or provide an onscreen calculator, because the intent is to test interpretation rather than mental arithmetic, and questions are typically presented under a strict time limit — often around a minute to ninety seconds per question — to simulate the pace of real decision-making.

For a lead solution architect, the numerical content of the role is substantial and often underestimated. You evaluate supplier bids and licensing models when you identify, evaluate, and select appropriate suppliers. You sanity-check capacity models, transaction volumes, and performance figures in the technical designs you review. You compare the whole-life cost of build-versus-buy options within financial constraints. You translate a strategy into a roadmap with quantified benefits and phased costs. And because you manage risks and decisions in a transparent way, you must be able to show your working: a recommendation to a programme board that says "option B is cheaper" carries weight only when you can demonstrate by how much, over what period, and under which assumptions. The assessment compresses all of this into short, data-rich questions.

Expect data presented as licensing tables, budget breakdowns, capacity and utilisation figures, supplier comparison matrices, availability percentages, and migration cost profiles. The skill is always the same three steps: locate the relevant figures precisely (watch units and scale qualifiers such as "in thousands"), apply the correct operation, and check the answer against common sense before committing.

### What it measures for your role

- **Commercial perspective.** Questions on supplier pricing models, contract comparisons, and total cost of ownership map directly to your skill in identifying appropriate contractual frameworks and approaches, and identifying, evaluating, and selecting appropriate suppliers. Choosing between a per-user licence and a per-transaction licence is a numeric reasoning problem before it is a procurement one.
- **Making architectural decisions.** Cost-benefit and risk-weighted calculations underpin design decisions characterised by medium risk and complexity. When you address architectural risks that affect multiple teams, quantifying exposure — downtime cost, remediation effort, licence penalties — is how you make the risk tractable and the decision transparent.
- **Technical design throughout the life cycle.** Capacity arithmetic, throughput calculations, and availability figures are the numerical backbone of technical designs characterised by high risk, impact, and complexity. Reviewing a junior architect's sizing model means recomputing it.
- **Strategy design.** Roadmap phasing, cumulative benefit projections, and budget profiles across years are how you direct the implementation of a strategy or vision through plans that finance teams and programme boards will scrutinise.
- **Working within business and technical constraints.** Many questions present a fixed budget or capacity ceiling and ask what fits beneath it — the everyday numerical form of understanding organisational objectives and external drivers such as financial constraints.

### Practice questions

**Question 1 (easy) — Percentage change in licence costs**

Your department pays £480,000 per year for an integration platform licence. The supplier announces a 12.5% price increase at renewal. Your budget line for this licence next year is £550,000.

What will the new annual cost be, and does it fit the budget?

- A) £540,000; yes, it fits with £10,000 headroom.
- B) £540,000; no, it exceeds the budget.
- C) £552,500; no, it exceeds the budget by £2,500.
- D) £537,600; yes, it fits with £12,400 headroom.

**Correct answer: A.**

**Explanation:** Calculate 12.5% of £480,000: 480,000 × 0.125 = £60,000. The new cost is 480,000 + 60,000 = £540,000. Compare with the £550,000 budget: 550,000 − 540,000 = £10,000 headroom, so it fits. Option D comes from applying 12% instead of 12.5% (480,000 × 0.12 = £57,600), a misread of the percentage. Option C comes from applying the increase to the budget figure rather than the current cost — a surprisingly common slip when two similar-magnitude numbers sit side by side. The habit to build: label each number as you extract it ("current cost", "budget") before touching the calculator, so you never operate on the wrong one. In supplier negotiations this exact calculation is your opening position, so precision here is professionally familiar territory.

**Question 2 (easy) — Reading a capacity utilisation table**

A shared hosting platform reports the following for its four environments:

| Environment | Provisioned vCPUs | Average utilisation |
|---|---|---|
| Production | 640 | 65% |
| Pre-production | 320 | 35% |
| Test | 256 | 25% |
| Development | 128 | 55% |

Which environment has the largest number of idle (unused) vCPUs on average?

- A) Production
- B) Pre-production
- C) Test
- D) Development

**Correct answer: A.**

**Explanation:** Idle capacity is provisioned × (1 − utilisation), so compute it for each row. Production: 640 × 0.35 = 224 idle vCPUs. Pre-production: 320 × 0.65 = 208. Test: 256 × 0.75 = 192. Development: 128 × 0.45 = 57.6. Production has the most idle capacity at 224 vCPUs, even though its utilisation percentage is the highest in the table. That inversion is the whole point of the question: candidates who reason from percentages alone pick Test (lowest utilisation, option C) and never touch the absolute figures. The trap works because percentages feel like the finished analysis when they are only half of it — 35% waste of a large pool costs more than 75% waste of a small one. This is exactly the calculation you perform when reviewing a sizing model, challenging over-provisioning, or building the cost case for consolidating environments: convert every percentage into absolute headroom before drawing conclusions, and present both figures to stakeholders so the scale is visible. A secondary habit worth noting: idle capacity uses (1 − utilisation), so a careless reading that multiplies by the utilisation figure itself produces a plausible-looking but inverted ranking.

**Question 3 (moderate) — Comparing supplier licensing models**

You are evaluating two suppliers for a document generation service. Supplier Alpha charges £2.40 per 1,000 documents with a fixed platform fee of £36,000 per year. Supplier Beta charges £4.10 per 1,000 documents with no platform fee. Your service generates 30 million documents per year.

Which supplier is cheaper annually, and by how much?

- A) Alpha, by £15,000
- B) Alpha, by £51,000
- C) Beta, by £15,000
- D) Beta, by £36,000

**Correct answer: A.**

**Explanation:** Convert the volume first: 30 million documents is 30,000 units of 1,000 documents. Alpha: 30,000 × £2.40 = £72,000, plus £36,000 platform fee = £108,000. Beta: 30,000 × £4.10 = £123,000. Difference: 123,000 − 108,000 = £15,000 in Alpha's favour. Option B is the trap for those who forget to add Alpha's platform fee (£72,000 versus £123,000 gives £51,000). Option D anchors on the platform fee itself. The commercial insight embedded here is the break-even structure: Alpha's fixed fee is only worthwhile above a certain volume. That break-even sits where 36,000 = (4.10 − 2.40) × V, so V = 36,000 ÷ 1.70 ≈ 21,176 units, about 21.2 million documents. Below that volume Beta wins; above it Alpha wins. Assessments frequently reward candidates who recognise fixed-versus-variable cost structures, and in your role this is exactly the analysis behind identifying appropriate contractual frameworks: the right answer depends on volume assumptions, so a strong recommendation to a board states the break-even, not just the winner.

**Question 4 (moderate) — Availability percentages and downtime budgets**

Your target architecture specifies 99.5% availability for a citizen-facing service, measured monthly. A proposed design chains two components in series: an application tier with 99.8% availability and a legacy backend with 99.9% availability. (For components in series, multiply availabilities.)

Does the proposed design meet the target, and what is the approximate permitted downtime per 30-day month at the 99.5% target?

- A) Yes (99.7% combined); permitted downtime is about 3.6 hours.
- B) No (99.7% combined); permitted downtime is about 36 minutes.
- C) Yes (99.7% combined); permitted downtime is about 7.2 hours.
- D) No (99.85% combined); permitted downtime is about 3.6 hours.

**Correct answer: A.**

**Explanation:** Combined availability in series: 0.998 × 0.999 = 0.997002, i.e. approximately 99.7%, which exceeds the 99.5% target, so yes, the design meets it. Permitted downtime at 99.5%: unavailability is 0.5% of the month. A 30-day month has 30 × 24 = 720 hours, and 0.5% of 720 = 3.6 hours. So option A is right on both parts. Option B correctly multiplies but misjudges the comparison (99.7% is above, not below, 99.5%) and computes downtime for a 99.9%-style target. Option C doubles the downtime by using 1% instead of 0.5%. Two habits matter here: first, series availability multiplies, so chains degrade — a fact that surprises stakeholders and that you will often need to explain when reviewing integration-heavy designs; second, converting an availability percentage into concrete hours is how you make service-level commitments meaningful to non-technical stakeholders, turning "99.5%" into "up to three and a half hours down each month, and here is what that means for caseworkers".

**Question 5 (moderate) — Budget allocation across a programme**

Your architecture programme has a £2.4 million annual budget split across three portfolios in the ratio 5:4:3 (Modernisation : Integration : Data). Mid-year, £120,000 is transferred from Integration to Data to fund an urgent remediation.

After the transfer, what is Data's share of the total budget, to the nearest percent?

- A) 25%
- B) 30%
- C) 33%
- D) 36%

**Correct answer: B.**

**Explanation:** The ratio 5:4:3 has 12 parts, so each part is 2,400,000 ÷ 12 = £200,000. Initial allocations: Modernisation £1,000,000; Integration £800,000; Data £600,000. After transferring £120,000: Data holds 600,000 + 120,000 = £720,000, and Integration drops to £680,000. Crucially, the total remains £2.4 million, because the transfer is internal — nothing entered or left the programme. Data's share: 720,000 ÷ 2,400,000 = 0.30 = 30%. Option A is Data's original share (600,000 ÷ 2,400,000 = 25%), the answer you get if you forget to apply the transfer. Option C comes from dividing by the wrong base, such as miscounting the ratio as 11 parts. Option D arises from adding the transfer to Data while also subtracting it from the total, double-counting the movement. Two habits protect you here: first, always count ratio parts explicitly (5 + 4 + 3 = 12) before dividing; second, when money moves within a fixed envelope, restate the invariant — "the total is unchanged" — before computing shares. This is precisely the arithmetic behind roadmap re-planning and in-year budget adjustments, where you must show a programme board transparently who gained, who lost, and that the books still balance.

**Question 6 (moderate) — Migration cost and effort estimation**

A legacy system migration covers 84 interfaces. Historical data shows a team migrates simple interfaces at 3 per sprint and complex ones at 1 per sprint; 60 of the interfaces are simple and 24 are complex. Two teams are available, each running 2-week sprints, and each team can work on either category.

Assuming perfect load balancing between the two teams, roughly how many weeks will the migration take?

- A) 22 weeks
- B) 44 weeks
- C) 30 weeks
- D) 16 weeks

**Correct answer: B.**

**Explanation:** Convert everything to sprint-effort first. Simple interfaces: 60 ÷ 3 = 20 sprints of work. Complex interfaces: 24 ÷ 1 = 24 sprints of work. Total effort: 44 team-sprints. Two teams working in parallel: 44 ÷ 2 = 22 sprints of elapsed time. Each sprint lasts 2 weeks, so the elapsed duration is 22 × 2 = 44 weeks. Option A is the classic trap: it presents the intermediate value — 22 elapsed sprints — as if it were the number of weeks, stopping one conversion short. Option C comes from averaging the two migration rates (2 per sprint) across all 84 interfaces and mishandling the parallelism; option D from assuming both teams each complete the full simple-interface workload simultaneously. When an option list includes both an intermediate value and the properly converted final value, the test is checking whether you finish the unit conversion. Always carry units explicitly through the calculation — "team-sprints", "elapsed sprints", "weeks" — and state them in your answer. In real migration planning, presenting 22 sprints to a board that hears 22 weeks would understate the schedule by half a year, which is exactly the kind of transparency failure that your role's emphasis on managing risks and decisions openly exists to prevent.

**Question 7 (hard) — Weighted supplier evaluation matrix**

You are scoring three suppliers against four criteria with these weights: Technical fit 40%, Cost 30%, Security assurance 20%, Support model 10%. Scores out of 10:

| Criterion | Supplier X | Supplier Y | Supplier Z |
|---|---|---|---|
| Technical fit | 8 | 6 | 9 |
| Cost | 5 | 9 | 4 |
| Security assurance | 7 | 7 | 9 |
| Support model | 6 | 8 | 5 |

Which supplier has the highest weighted score?

- A) Supplier X
- B) Supplier Y
- C) Supplier Z
- D) X and Z tie

**Correct answer: B.**

**Explanation:** Compute each weighted total. Supplier X: (8 × 0.4) + (5 × 0.3) + (7 × 0.2) + (6 × 0.1) = 3.2 + 1.5 + 1.4 + 0.6 = 6.7. Supplier Y: (6 × 0.4) + (9 × 0.3) + (7 × 0.2) + (8 × 0.1) = 2.4 + 2.7 + 1.4 + 0.8 = 7.3. Supplier Z: (9 × 0.4) + (4 × 0.3) + (9 × 0.2) + (5 × 0.1) = 3.6 + 1.2 + 1.8 + 0.5 = 7.1. Y scores 7.3, Z scores 7.1, X scores 6.7 — so the highest weighted score belongs to Supplier Y. If you selected Z by eye because it dominates the headline criterion (technical fit) and security, you have just experienced the exact bias weighted matrices exist to correct: unweighted impressions overvalue the criteria we find most interesting, while Z's weak cost score (4 against a 30% weight) quietly drags its total below Y's. The arithmetic discipline — multiply every cell by its weight, add carefully, compare totals — is the same one you apply when you identify, evaluate, and select appropriate suppliers in a defensible, auditable way. Note also the sensitivity insight a lead architect should volunteer to a board: Y's win depends heavily on the cost weighting; if cost dropped from 30% to 20% and technical fit rose to 50%, Z would win (Z: 4.5 + 0.8 + 1.8 + 0.5 = 7.6 versus Y: 3.0 + 1.8 + 1.4 + 0.8 = 7.0). Stating where the ranking flips is what turns a scoring table into transparent decision-making.

**Question 8 (hard) — Total cost of ownership over multiple years**

You are comparing two options for a case management capability over a 5-year appraisal period. Option Build: £1.8 million development in year 1, then £280,000 per year running costs in years 2 to 5. Option Buy: £150,000 implementation in year 1, plus an annual licence of £520,000 in every year (years 1 to 5), with a contractual 5% licence increase applied once at the start of year 4 (affecting years 4 and 5).

Which option is cheaper over 5 years, and by approximately how much?

- A) Build, by about £118,000
- B) Buy, by about £118,000
- C) Build, by about £170,000
- D) Buy, by about £170,000

**Correct answer: B.**

**Explanation:** Total each option carefully. Build: 1,800,000 + (4 × 280,000) = 1,800,000 + 1,120,000 = £2,920,000. Buy: implementation 150,000; licence years 1 to 3 at 520,000 each = 1,560,000; the 5% increase makes years 4 and 5 cost 520,000 × 1.05 = 546,000 each, so 2 × 546,000 = 1,092,000. Buy total: 150,000 + 1,560,000 + 1,092,000 = £2,802,000. Compare: Build £2,920,000 versus Buy £2,802,000 — Buy is cheaper by £118,000. Option D's £170,000 figure comes from forgetting the licence indexation entirely (Buy would then total £2,750,000), and the Build-favouring options catch candidates who miscount the running-cost years — the question says years 2 to 5, which is four years, not five. The disciplines this trains are exactly those of a real options appraisal: enumerate every cost line for every year before comparing; apply contractual escalators from the correct start year (the increase bites at the start of year 4, affecting two of the five years); and never compare a fully loaded option against a partially loaded one. In board papers, small definitional differences — whether the year-1 licence applies during implementation, when an indexation clause bites — move totals by tens of thousands of pounds, so a lead architect states these assumptions explicitly alongside the totals. Transparency about the model is as important as the winner it produces.

**Question 9 (hard) — Transaction growth and capacity ceiling**

A payments API currently handles 2.0 million transactions per month, growing at a compound rate of 8% per quarter. The platform's tested capacity ceiling is 3.5 million transactions per month. Quarterly upgrade windows are the only opportunities to scale.

After how many complete quarters will monthly volume first exceed the capacity ceiling?

- A) 6 quarters
- B) 7 quarters
- C) 8 quarters
- D) 10 quarters

**Correct answer: C.**

**Explanation:** Track compound growth: volume after n quarters is 2.0 × 1.08ⁿ million. Compute stepwise: after 1 quarter 2.16; 2 quarters 2.33; 3 quarters 2.52; 4 quarters 2.72; 5 quarters 2.94; 6 quarters 3.17; 7 quarters 3.43; 8 quarters 3.70. The ceiling of 3.5 million is first exceeded after 8 complete quarters (3.70 million versus 3.43 million after 7). Option B is the near-miss for anyone who stops at "3.43 is close to 3.5" or who uses simple rather than compound growth: simple growth at 8% of the original 2.0 million adds 0.16 per quarter, reaching 3.44 after 9 quarters and 3.60 after 10 — which is where option D comes from. The practical lesson is twofold. First, compound growth accelerates: the gap between successive quarters widens (0.16, then 0.17, then 0.19...), so linear extrapolation systematically understates when ceilings arrive. Second, for planning purposes the answer "8 quarters" is not the deliverable — the deliverable is "we must complete a scaling upgrade at or before the quarter-7 window", because the breach happens during quarter 8. That translation from arithmetic result to roadmap action is precisely what distinguishes a lead architect's capacity note from a spreadsheet.

**Question 10 (hard) — Interpreting a performance metrics dashboard**

A service dashboard shows the following for two releases of a case-search feature:

| Metric | Release 1 | Release 2 |
|---|---|---|
| Median response time | 480 ms | 320 ms |
| 95th percentile response time | 1,900 ms | 2,600 ms |
| Requests per day | 40,000 | 55,000 |
| Error rate | 0.8% | 0.5% |

The service standard requires that no more than 5% of requests take longer than 2,000 ms. Which statement is best supported by the data?

- A) Release 2 improved typical performance but now breaches the service standard for slow requests.
- B) Release 2 is better on every measure and meets the service standard.
- C) Release 2 breaches the service standard because its error rate rose.
- D) Release 1 breached the service standard; Release 2 fixed it.

**Correct answer: A.**

**Explanation:** Interpret each metric against the standard. The standard says at most 5% of requests may exceed 2,000 ms — equivalently, the 95th percentile must be at or below 2,000 ms. Release 1: 95th percentile 1,900 ms, within the standard. Release 2: 95th percentile 2,600 ms, meaning more than 5% of requests exceed 2,000 ms — a breach. Meanwhile the median improved from 480 ms to 320 ms (typical requests got faster) and the error rate fell from 0.8% to 0.5% (option C misreads the direction). So Release 2 improved typical performance while degrading tail performance into breach — option A. Option B ignores the percentile breach; option D reverses which release complies. Also compute the human impact to make the finding concrete: at 55,000 requests per day, at least 5% — 2,750 requests daily — now take over 2,000 ms, and since the 95th percentile is 2,600 ms, the slowest 5% are substantially slow. This median-versus-tail divergence is a classic pattern in real systems (often caused by a cache that accelerates common queries while complex ones queue), and reading percentiles correctly is essential when you use feedback to optimise and refine standards for technical designs throughout the life cycle: a standard written only around averages would have scored Release 2 as a pure win.

**Question 11 (hard) — Risk-weighted cost exposure**

Your risk register quantifies three architectural risks. Risk A: probability 40%, impact £750,000. Risk B: probability 15%, impact £2,400,000. Risk C: probability 60%, impact £300,000. You have £250,000 of mitigation budget. Mitigation options: spending £150,000 halves Risk A's probability; spending £100,000 reduces Risk B's probability to 5%; spending £120,000 reduces Risk C's impact by two-thirds.

Which affordable combination of mitigations reduces total expected exposure the most?

- A) Mitigate A and B
- B) Mitigate A and C
- C) Mitigate B and C
- D) Mitigate A only, saving the rest

**Correct answer: A.**

**Explanation:** Compute expected exposure (probability × impact) before mitigation: A = 0.40 × 750,000 = £300,000; B = 0.15 × 2,400,000 = £360,000; C = 0.60 × 300,000 = £180,000. Total £840,000. Now value each mitigation. A's option halves probability to 20%: new exposure £150,000, a reduction of £150,000 for £150,000 spent. B's option cuts probability to 5%: new exposure 0.05 × 2,400,000 = £120,000, a reduction of £240,000 for £100,000 spent. C's option cuts impact to £100,000: new exposure 0.60 × 100,000 = £60,000, a reduction of £120,000 for £120,000 spent. Affordability: A+B costs £250,000 (exactly the budget) and reduces exposure by £390,000. B+C costs £220,000 and reduces exposure by £360,000. A+C costs £270,000 — over budget, so option B is infeasible regardless of its arithmetic. A alone reduces £150,000. The best affordable combination is A+B, option A. Notice that mitigation B is the standout bargain (£2.40 of exposure reduction per £1 spent), which is why every strong combination includes it; the real choice is between adding A or adding C, and A's £150,000 reduction beats C's £120,000. This is expected-value reasoning applied exactly as your role applies it: identifying and addressing architectural risks that affect multiple teams or domains, with a transparent, quantified case for why the mitigation budget went where it did.

**Question 12 (hard) — Roadmap benefits profile**

A three-phase strategy delivers annual savings once each phase completes: Phase 1 saves £200,000 per year, Phase 2 saves £350,000 per year, Phase 3 saves £500,000 per year. Phases complete at the end of year 1, year 2, and year 3 respectively, and each phase's savings begin the year after it completes and recur every year thereafter. Total investment is £1.6 million, all spent in year 1.

In which year do cumulative savings first exceed the total investment?

- A) Year 3
- B) Year 4
- C) Year 5
- D) Year 6

**Correct answer: B.**

**Explanation:** Build the savings timeline carefully. Phase 1 completes at the end of year 1, so its £200,000 annual saving begins in year 2. Phase 2 completes at the end of year 2, so its £350,000 begins in year 3. Phase 3 completes at the end of year 3, so its £500,000 begins in year 4. Annual savings are therefore: year 2 = £200,000; year 3 = 200,000 + 350,000 = £550,000; year 4 onward = 200,000 + 350,000 + 500,000 = £1,050,000 per year. Cumulative savings: end of year 2 = £200,000; end of year 3 = £750,000; end of year 4 = £1,800,000. The cumulative total first exceeds the £1.6 million investment during year 4 (entering the year at £750,000 and adding £1,050,000 crosses the threshold part-way through), so year 4 is the answer. Option A tempts those who forget the benefit lag and start each phase's savings in its completion year. Option C catches those who delay each phase's savings by an extra year, and option D those who compare against investment plus imagined running costs the question never mentioned. Two disciplines matter here: first, benefit lag — savings almost never start in the year the money is spent, and boards routinely misread this; second, keep annual and cumulative rows distinct in any benefits table you present. When you direct the implementation of a strategy through roadmaps and plans, the payback-year claim is often the single most scrutinised number in the pack, so derive it stepwise exactly as here.

### Preparation tips

- **Rehearse the three-step loop: locate, compute, sanity-check.** Under time pressure the failure mode is skipping step one (grabbing the wrong number) or step three (accepting an absurd result). Practise saying to yourself what each number is before using it, and asking "is this magnitude plausible?" after.
- **Refresh the handful of core operations.** Percentage change, reverse percentages, ratios and shares, weighted averages, compound growth, and expected value cover almost every question you will meet. Fifteen minutes a day with realistic figures (budgets in hundreds of thousands, volumes in millions) rebuilds fluency quickly.
- **Practise with the calculator you will use.** An onscreen calculator has different ergonomics from your phone or a spreadsheet. If the assessment provides one in its practice round, use the practice round to learn it.
- **Carry units through every calculation.** Team-sprints, elapsed weeks, transactions per month, vCPUs: writing (or subvocalising) the unit at each step prevents the intermediate-value traps that assessments love.
- **Estimate before you compute.** A rough order-of-magnitude estimate ("about 30,000 units at roughly £2.50 is about £75,000") catches keying errors instantly and often eliminates two options before you calculate at all.
- **Use your professional context as motivation, not interference.** The scenarios will feel familiar — supplier bids, capacity ceilings, benefit profiles. Let familiarity speed your reading, but compute from the question's numbers, not from what similar figures looked like in your organisation.

### Common pitfalls

- **Misreading scale qualifiers.** Confusing "£480k" with "£480,000 per quarter", or missing "in thousands" on a table header, silently corrupts every subsequent step. Read table headers and units before reading any data cell.
- **Anchoring on percentages instead of absolutes.** As the utilisation question showed, the biggest percentage is often not the biggest number. Decide which the question actually asks for.
- **Forgetting fixed costs in comparisons.** Per-unit prices are seductive; platform fees, implementation charges, and indexation clauses decide many comparisons. Total each option fully before comparing.
- **Over-calculating.** Some questions fall to estimation and elimination in twenty seconds; performing exact long-form arithmetic on every question is a time sink that costs you later marks. Match the precision to what the options require.
- **Getting stuck on a multi-stage question.** One hard compound-growth or TCO question can consume five minutes. Flag it, move on, and return if time allows — the scoring rewards total correct answers, not heroics on the hardest item.
- **Ignoring the time basis.** Monthly versus quarterly versus annual figures are mixed deliberately. Normalise everything to one time basis before comparing — it is the single most common source of error in real supplier evaluations too.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment evaluates how well you understand, analyse, and draw correct conclusions from written business information. The passages mirror the exact reading demands of your role: technology codes of practice, architecture governance terms of reference, supplier contract clauses, design authority minutes, and stakeholder correspondence. The dominant format asks you to judge statements against a passage as True (the passage states or logically entails it), False (the passage contradicts it), or Cannot Say (the passage provides insufficient information either way), usually supplemented by multiple-choice comprehension questions about main arguments, obligations, and implications. Timing is tight — typically less than a minute per question — because the test simulates reading under workplace deadlines.

The single most important rule is this: answer based strictly on the text provided, ignoring outside knowledge. This is harder for you than for most candidates, precisely because you are an expert. You know how spend controls usually work, what a typical exit clause says, and how design authorities normally operate — and the test will punish you for using any of it. "Cannot Say" is the correct answer whenever the passage neither states nor entails the claim, even if you know from experience that the claim is almost certainly true in the real world.

Why does this matter for a lead solution architect? Because your working life is a sequence of high-stakes readings. When you comply with standards and governance, you must know exactly what a standard mandates versus recommends. When you identify appropriate contractual frameworks, the difference between "the supplier shall" and "the supplier may" is the difference between an enforceable obligation and a hope. When you gain support from stakeholders for high-risk architectural topics, you must accurately represent what a policy or report actually says — misquoting a mandate to a programme board, even innocently, damages the credibility your influence depends on. And when you coach junior architects, you model the discipline of reading before opining. The assessment compresses this forensic reading into rapid-fire questions.

### What it measures for your role

- **Architecture communication.** Comprehension questions about tone, audience, and main argument reflect your skill in communicating with technical and non-technical stakeholders at all levels, and in mediating between people in difficult architectural discussions — mediation begins with accurately understanding each written position.
- **Making architectural decisions.** True/False/Cannot Say precision maps to reading governance documents correctly: knowing what a standard mandates, permits, and is silent on is the foundation of using architectural governance and assurance to make design decisions at the appropriate level.
- **Commercial perspective.** Contract-style passages test the exact skill you use when identifying appropriate contractual frameworks and evaluating suppliers: obligations, conditions, and carve-outs live in precise wording.
- **Problem definition and shaping.** Distinguishing what a document establishes from what it assumes mirrors how you help others challenge requirements and assumptions when defining problems.
- **Working within business and technical constraints.** Passages about legislation, financial rules, and organisational policy reflect your duty to understand organisational objectives and external drivers, such as legislation or financial constraints, from the primary texts that define them.

### Practice questions

**Passage 1 — Technology code of practice extract**

*"All new digital services must be assessed against the Technology Code of Practice at the discovery and beta phases. Services that cannot demonstrate use of open standards must document the reason in an exemption request approved by the chief technology officer. Cloud-first remains the default policy: departments should evaluate public cloud solutions before considering alternatives, although the policy does not mandate the selection of a public cloud solution where evaluation shows it to be unsuitable. Legacy systems undergoing significant change are treated as new services for the purposes of this code."*

**Question 1 (easy) — True / False / Cannot Say**

Statement: "A legacy system undergoing significant change must be assessed against the Technology Code of Practice at discovery and beta phases."

- A) True
- B) False
- C) Cannot Say

**Correct answer: A (True).**

**Explanation:** Chain two sentences: legacy systems undergoing significant change "are treated as new services for the purposes of this code", and "all new digital services must be assessed... at the discovery and beta phases." The entailment is direct: if the system is treated as a new service, the assessment obligation applies to it. Note the reasoning is textual, not worldly — you are not asked whether this is sensible policy or how your department applies it. This two-sentence chaining is the most common structure for "True" answers in well-set tests: no single sentence states the claim, but two sentences jointly entail it. Train yourself to look for the linking definition ("treated as new services") whenever a statement mentions a category the passage defines indirectly.

**Question 2 (easy) — True / False / Cannot Say**

Statement: "The cloud-first policy requires departments to select a public cloud solution."

- A) True
- B) False
- C) Cannot Say

**Correct answer: B (False).**

**Explanation:** The passage directly contradicts the statement: "the policy does not mandate the selection of a public cloud solution where evaluation shows it to be unsuitable." The policy requires evaluation of public cloud first ("departments should evaluate public cloud solutions before considering alternatives"), not selection. The statement collapses "must evaluate first" into "must select", which is precisely the kind of overreading that causes real-world governance disputes — a team believing it is forced onto public cloud, or conversely a board believing an architect who chose public cloud had no discretion. When a statement transforms a process obligation (evaluate, consider, document) into an outcome obligation (select, use, adopt), check the passage's verbs: verbs carry the compliance meaning, and the difference between them is the difference between False and True here.

**Question 3 (moderate) — True / False / Cannot Say**

Statement: "The chief technology officer has rejected at least one exemption request."

- A) True
- B) False
- C) Cannot Say

**Correct answer: C (Cannot Say).**

**Explanation:** The passage establishes a mechanism — exemption requests "approved by the chief technology officer" — but says nothing about how many requests have been made, approved, or rejected. Your professional experience insists that any real approval process produces rejections eventually; the text neither states nor entails it. This is the archetypal Cannot Say: the statement is plausible, consistent with the passage, and completely unsupported by it. The distinction matters in your role more than most: when you brief a board that "the standard requires X", you must know whether the document says X, implies X, or is merely consistent with X. A useful internal test: could the passage be true in a world where the statement is false? Here, yes — perhaps every request so far has been approved, or none has ever been submitted — so the answer is Cannot Say.

**Passage 2 — Supplier contract clause**

*"The Supplier shall provide the integration platform as a managed service with availability of no less than 99.7% measured monthly. Where availability falls below this level in any month, the Authority shall be entitled to service credits equal to 10% of the monthly charge for that month, rising to 25% where availability falls below 99.0%. Service credits shall be the Authority's sole financial remedy for availability failures, save where a failure persists for three consecutive months, in which case the Authority may terminate the agreement with 30 days' notice. The Supplier may propose replacement of any platform component provided that the replacement causes no degradation of the service and is approved in advance by the Authority's architecture function."*

**Question 4 (moderate) — True / False / Cannot Say**

Statement: "If availability is 99.5% in a given month, the Authority is entitled to service credits of 25% of that month's charge."

- A) True
- B) False
- C) Cannot Say

**Correct answer: B (False).**

**Explanation:** Track the thresholds precisely. Availability of 99.5% is below the 99.7% commitment, so credits apply — but the 25% rate applies only "where availability falls below 99.0%". At 99.5%, availability is below 99.7% but not below 99.0%, so the applicable credit is 10%, not 25%. The statement asserts the wrong tier, and the passage contradicts it, making the answer False rather than Cannot Say. Banded thresholds like this are a staple of both contracts and verbal reasoning tests because they reward careful boundary reading: the question deliberately picks a value inside the band where the lower credit applies. In supplier management this exact misreading — claiming the higher credit tier — is embarrassing in negotiation and expensive in goodwill; as the architect advising the commercial team, you are often the person expected to catch it.

**Question 5 (moderate) — True / False / Cannot Say**

Statement: "The Authority may terminate the agreement if availability falls below 99.7% for three consecutive months."

- A) True
- B) False
- C) Cannot Say

**Correct answer: A (True).**

**Explanation:** The clause states that service credits are the sole financial remedy "save where a failure persists for three consecutive months, in which case the Authority may terminate the agreement with 30 days' notice." A month with availability below 99.7% is an availability failure under the clause (it breaches the "no less than 99.7%" commitment), so three consecutive such months trigger the termination right. The statement mirrors the text's condition and consequence accurately, including the permissive "may" — the Authority is entitled to terminate, not obliged to. Had the statement said "must terminate" or "may terminate immediately", the answer would be False (the notice period is 30 days). At lead level you will often be asked, mid-incident, "can we exit this contract?" — and the credibility of your answer rests on exactly this style of clause-accurate reading, including its conditions (three consecutive months) and mechanics (30 days' notice).

**Question 6 (moderate) — Multiple choice comprehension**

According to the clause, which of the following is required before the Supplier replaces a platform component?

- A) Thirty days' notice to the Authority.
- B) Advance approval by the Authority's architecture function and no degradation of the service.
- C) A service credit payment covering the transition month.
- D) Evidence that the replacement improves availability above 99.7%.

**Correct answer: B.**

**Explanation:** The final sentence sets two conditions: the replacement "causes no degradation of the service" and "is approved in advance by the Authority's architecture function". Option B captures both. Option A borrows the 30-day notice period from the termination provision — a different mechanism entirely; distractors frequently transplant a genuine detail from elsewhere in the passage, counting on your memory of having "seen it". Option C invents a linkage between credits and component replacement that the clause never makes. Option D overstates the standard: the clause requires no degradation, not demonstrated improvement. Notice, too, the professional significance of the sentence: it writes your own function — architecture — into the supplier's change process. Recognising and using such clauses is part of the commercial perspective your role profile names: contractual frameworks are not just legal plumbing, they are where architectural control over a managed service is either secured or lost.

**Passage 3 — Design authority terms of reference**

*"The Design Authority meets fortnightly and is quorate when at least four voting members are present, of whom one must be the chief architect or their nominated deputy. Decisions are made by majority of voting members present; the chair holds a casting vote in the event of a tie. Designs classified as high risk require endorsement by the security architect in addition to the standard vote. Submissions must be circulated no later than five working days before the meeting. Where a submission is rejected, the submitting team may resubmit once revisions are complete, but no submission may be considered more than three times in any rolling twelve-month period. The Design Authority may delegate approval of low-risk designs to lead architects, subject to quarterly retrospective review of delegated decisions."*

**Question 7 (moderate) — True / False / Cannot Say**

Statement: "A meeting attended by four voting members, none of whom is the chief architect or their deputy, is quorate."

- A) True
- B) False
- C) Cannot Say

**Correct answer: B (False).**

**Explanation:** Quoracy has two conjunctive conditions: "at least four voting members are present" and "one must be the chief architect or their nominated deputy". The scenario satisfies the headcount but explicitly fails the composition requirement, so the meeting is not quorate — the passage contradicts the statement, making it False. The reading skill is recognising that "of whom one must be" attaches a mandatory composition condition to the numerical threshold rather than offering an example. In governance documents, embedded conditions like this are where organisations trip: a meeting proceeds, decisions are made, and weeks later someone notices the decisions were invalid. As a lead architect who contributes to the development of architectural governance, you will draft and review exactly these sentences — and precision in reading them is the prerequisite for precision in writing them.

**Question 8 (hard) — True / False / Cannot Say**

Statement: "A high-risk design supported by a majority of voting members present is approved."

- A) True
- B) False
- C) Cannot Say

**Correct answer: C (Cannot Say).**

**Explanation:** High-risk designs "require endorsement by the security architect in addition to the standard vote." A majority vote is therefore necessary but not sufficient; approval also depends on the security architect's endorsement, about which the statement says nothing. Is the statement False, then? Not quite — the design might also have the security architect's endorsement, in which case it is approved. The statement as written is sometimes true and sometimes false depending on a fact the statement omits and the passage cannot supply; the passage neither entails nor contradicts it, so Cannot Say. This is the subtlest of the three verdicts: a conditional gap rather than missing information about the world. Under time pressure, candidates rush to False because they spotted the extra requirement. Slow down for exactly this pattern: when a statement describes a situation compatible with both approval and non-approval under the passage's rules, the honest verdict is Cannot Say. The same discipline applies when you summarise governance outcomes for stakeholders — "the board voted in favour" and "the design is approved" are different claims, and conflating them in an email to a programme director is how misunderstandings escalate.

**Question 9 (hard) — Multiple choice comprehension**

A team's design has been rejected twice in the past eight months. Which statement best reflects the team's position under the terms of reference?

- A) The team may not resubmit, because designs may only be considered twice.
- B) The team may resubmit once revisions are complete, and that submission would be the third and final consideration possible within the rolling twelve-month period.
- C) The team may resubmit an unlimited number of times, provided each submission is circulated five working days in advance.
- D) The team must wait until twelve months have passed since the first rejection before resubmitting.

**Correct answer: B.**

**Explanation:** Combine the two relevant provisions. First, "where a submission is rejected, the submitting team may resubmit once revisions are complete" — so resubmission is permitted now, defeating options A and D. Second, "no submission may be considered more than three times in any rolling twelve-month period" — the design has been considered twice in eight months, so one further consideration is available within the current rolling window, making the next submission the third and final one for now; this defeats option C's "unlimited". Option B alone integrates both provisions accurately. The question models a genuinely common professional task: a delivery team asks you, their lead architect, "can we go back to the board, and what are our constraints?" The answer requires synthesising permission rules and frequency limits from different sentences — and noting the "rolling" qualifier, which means the team's position improves as earlier considerations age out of the window. Answering from one sentence alone, in either direction, gives the wrong advice.

**Passage 4 — Stakeholder email**

*"Following yesterday's programme board, I want to record my concerns about the proposed shared payments platform. The board was told that all four service teams support the approach. My team's position is more nuanced: we support consolidation in principle, but we cannot commit to the proposed migration window while our peak processing season runs from January to April. I am also aware — though this was not discussed at the board — that the supplier's reference implementation has only been deployed at half our transaction volume. I am not asking for the decision to be reopened; I am asking that the risks be recorded and that the migration schedule for my team be revisited before contracts are signed."*

**Question 10 (moderate) — True / False / Cannot Say**

Statement: "The author opposes consolidation onto a shared payments platform."

- A) True
- B) False
- C) Cannot Say

**Correct answer: B (False).**

**Explanation:** The author states: "we support consolidation in principle." The statement claims opposition to consolidation itself, which the text contradicts — the author's objection is to the proposed migration window and to unrecorded risks, not to the principle. This distinction between opposing a decision and opposing its implementation details is one of the most consequential in stakeholder management, and the passage is constructed exactly the way real stakeholder emails are: layered support ("in principle"), specific conditions (the January-to-April peak), and a carefully limited request ("I am not asking for the decision to be reopened"). Misreading this email as opposition — and reporting to the programme director that "team X is against the platform" — would inflame a manageable scheduling concern into a political dispute. Accurate reading is the foundation of the mediation your role profile describes: you cannot mediate between positions you have mischaracterised.

**Question 11 (hard) — True / False / Cannot Say**

Statement: "The programme board was given an inaccurate account of the service teams' support."

- A) True
- B) False
- C) Cannot Say

**Correct answer: A (True).**

**Explanation:** Reason from the two claims the author makes. The board "was told that all four service teams support the approach." The author, speaking for one of those teams, says "my team's position is more nuanced" and sets out a conditional position — support in principle, but no commitment to the migration window. Unqualified support was reported; the actual position is qualified. On the passage's own account, therefore, the description given to the board did not accurately represent this team's position, which makes the account inaccurate as stated. Careful candidates may hover over Cannot Say, reasoning that "support the approach" could loosely cover in-principle support with reservations — but the board statement was that all four teams support "the approach", and the author's team explicitly cannot commit to a core element of the approach as proposed (its migration window). The passage entails the mismatch, though note what it does not entail: any intent to mislead. "Inaccurate" is established; "dishonest" would be Cannot Say. Preserving that distinction — wrong versus wrongful — is precisely the discipline you need when recording risks and decisions transparently without accusing colleagues.

**Question 12 (hard) — Multiple choice: identifying the author's request**

Which option best summarises what the author is asking for?

- A) That the decision to adopt a shared payments platform be reversed.
- B) That the risks be formally recorded and the migration schedule for their team be revisited before contracts are signed.
- C) That the supplier's reference implementation be independently audited before any further steps.
- D) That the programme board be reconvened to hear the four teams' positions directly.

**Correct answer: B.**

**Explanation:** The author states the request in the final sentence: "I am asking that the risks be recorded and that the migration schedule for my team be revisited before contracts are signed" — and explicitly rules out option A ("I am not asking for the decision to be reopened"). Option C is a plausible inference from the volume concern, but the author raises the reference-implementation point as a risk to record, not as a demand for an audit; choosing C substitutes your solution for the author's request. Option D invents a procedural remedy nowhere in the text. This question tests a skill central to architecture communication: separating what a stakeholder says from what you would say in their position. When you draft the response to an email like this — or brief the programme director on it — fidelity to the actual request builds the trust that lets you gain support for architectural topics with high levels of risk and complexity later. Stakeholders forgive disagreement; they rarely forgive misrepresentation.

### Preparation tips

- **Drill the three verdicts until they are reflexes.** True means the passage states or logically entails the claim; False means the passage contradicts it; Cannot Say means neither. Write these definitions on a note while you practise. Most errors at senior level are experts answering True or False from professional knowledge when the text supports only Cannot Say.
- **Read the statement first, then hunt in the passage.** With under a minute per question, reading the full passage before every statement wastes time. Read the statement, identify its key terms (thresholds, actors, obligations), and scan the passage for the sentences that bear on them — then read those sentences slowly.
- **Interrogate the verbs and modals.** Shall, may, must, should, is entitled to, requires, does not mandate: these words decide most questions. Practise translating them — "may" grants discretion, "shall" imposes duty, "should" recommends — because the wrong translation flips the answer.
- **Watch for boundary values and conjunctions.** Banded thresholds (10% versus 25% credits), conjunctive conditions (four members AND the chief architect), and scope qualifiers ("for the purposes of this code") are the test-writer's favourite materials, just as they are the contract-drafter's.
- **Practise on your own governance documents.** Take a standard, a contract schedule, or terms of reference from your work and write five True/False/Cannot Say statements about it. Composing questions teaches you the traps faster than answering them, and doubles as coaching material for the junior architects you develop.
- **Keep calibrated confidence.** As a lead architect you read documents like these daily; trust that fluency. The only adjustment the test demands is strictness — the passage is the entire universe, and your considerable outside knowledge is, for thirty minutes, inadmissible.

### Common pitfalls

- **Importing expert knowledge.** The most common senior-level failure: you know how spend controls, cloud policy, or supplier contracts really work, and that knowledge contaminates a verdict the passage cannot support. If the passage does not say it, it is not evidence.
- **Confusing "consistent with" and "entailed by".** A statement that fits comfortably alongside the passage is not thereby True; it must follow from the passage. "Plausible" plus "unstated" equals Cannot Say.
- **Collapsing process obligations into outcome obligations.** "Must evaluate cloud first" is not "must choose cloud"; "may terminate" is not "must terminate". Transformation of verbs between passage and statement is the single most productive trap in the format.
- **Transplanted details.** Distractors reuse genuine numbers and phrases from elsewhere in the passage (a notice period, a threshold) in the wrong context. Verify not just that a detail appears, but that it attaches to the right mechanism.
- **Rushing the Cannot Say conditional.** When a statement's truth depends on a fact the passage does not settle (the security architect's endorsement), candidates under pressure choose False. Pause on any statement that could be true in one permitted scenario and false in another.
- **Reading the whole passage every time.** Time management fails when you re-read all of a dense passage for each of its four questions. Scan for the governing sentences, then read those with full attention.

## Workplace job-specific situational judgement assessment

### About this assessment

A workplace job-specific situational judgement assessment evaluates your decision-making, interpersonal skill, and professional conduct through realistic workplace dilemmas. Unlike the cognitive, numeric, and verbal assessments, there is usually no single objectively right answer: several responses may seem reasonable, and the scoring reflects how closely your choices align with the values and behaviours the organisation needs from someone in your role. Formats vary — you may be asked to pick the most effective and least effective actions from a set, to rank all the options from best to worst, or to rate each option's effectiveness independently. Timing is typically generous or untimed, because the assessment is interested in your natural judgement rather than your speed.

For a lead solution architect in UK government, the scenarios will draw on the situations your role profile describes: building relationships with senior stakeholders across multiple business and technical areas, leading and coaching junior architects, mediating difficult architectural discussions, managing supplier relationships commercially, handling governance and assurance honestly, and balancing delivery pressure against standards, security, and user needs. The scoring key is anchored in UK public sector values — meeting user needs, transparency in decisions and risks, collaboration across teams and organisations, accessibility and inclusion, and responsible stewardship of public money — alongside the leadership behaviours expected at your level: taking ownership rather than passing problems along, addressing root causes rather than symptoms, being candid with senior people even when it is uncomfortable, and developing the people you lead.

Two features of strong answers recur throughout. First, they act at the right altitude: a lead architect neither dives in to do a junior colleague's work for them habitually, nor escalates every difficulty upward; they resolve what is theirs to resolve, equip others to resolve what is theirs, and escalate transparently what genuinely requires it. Second, they preserve relationships while addressing substance: options that "win" an argument by ambush, or avoid conflict by silence, both score poorly. As you work through the scenarios below, compare your instincts against the explanations — the reasoning is more valuable than the answer key.

### What it measures for your role

- **Architecture communication.** Scenarios test whether you communicate with technical and non-technical stakeholders at the right level, mediate between people in difficult architectural discussions, and gain support for topics with high levels of risk, impact, and complexity — and whether you coach and support others in doing the same.
- **Community collaboration.** Dilemmas about team dynamics test how you work collaboratively, adapt feedback so it is effective and lasting, identify problems in team dynamics and rectify them, and use Agile health checks to stimulate the right responses.
- **Architect for the whole context.** Several scenarios pit your immediate project's interests against wider organisational objectives, testing whether you track and act on issues that affect teams beyond your own.
- **Making architectural decisions.** Governance dilemmas test whether you manage technical risk at the appropriate level, use assurance mechanisms honestly, and keep decision-making transparent.
- **Commercial perspective.** Supplier scenarios test propriety and value for money in evaluating and selecting suppliers, and judgement about contractual boundaries.
- **Problem definition and shaping and strategy design.** Scenarios about premature solutions and strategy resistance test whether you reframe problems, challenge assumptions constructively, and adapt strategy in response to feedback and findings.

### Practice questions

**Scenario 1 (moderate) — The premature solution from above**

A director you have a good relationship with announces at a programme board that the department will adopt a specific vendor's low-code platform to "fix the case management backlog", and asks you to produce the solution architecture within a month. Your discovery work so far suggests the backlog is driven by process bottlenecks and data quality, not by the technology. The director has already mentioned the platform to the minister's office.

Rate the options: which is the MOST effective and which is the LEAST effective response?

- A) Produce the requested solution architecture for the platform within the month, noting your reservations verbally to your own team.
- B) Request a short private meeting with the director, present the discovery evidence, and propose framing the board's commitment as "modernising case management", with the platform as one option to be validated against the actual bottlenecks.
- C) Raise your objections at the next programme board in open session, so the disagreement is on the record.
- D) Quietly commission a further three-month discovery to strengthen the evidence before saying anything to the director.

**Most effective: B. Least effective: A.**

**Explanation:** Option B does three things a lead architect must do at once: it protects the evidence-based framing of the problem (your problem definition and shaping duty), it protects the director from public embarrassment by working privately first, and it offers a face-saving reframe that keeps the political commitment intact while restoring architectural integrity — the essence of gaining support for high-risk topics from senior stakeholders. Option A is least effective because it converts a recoverable mistake into an owned one: you would be documenting an architecture you believe misdiagnoses the problem, with your dissent recorded nowhere that matters. Reservations shared only with your own team are not transparency; they are cover. Option C values transparency but chooses the worst venue — ambushing a director in front of peers after the minister's office is engaged makes the disagreement about status rather than evidence, and damages the relationship your influence depends on. Option D delays the necessary conversation and lets the commitment harden for three more months; it is diligence used as avoidance. The general pattern: challenge early, privately, with evidence, and always bring a reframe the senior person can adopt with dignity.

**Scenario 2 (moderate) — The struggling junior architect**

A junior solution architect you lead has produced a design for a medium-risk integration that contains significant flaws: an unsecured direct database connection and no consideration of failure modes. The design authority reviews it in five days. This is the second design from this architect with similar gaps. They are visibly anxious about the review and have worked hard on the pack.

Rank the options from most to least effective.

- A) Rewrite the problematic sections yourself this time, and schedule design training for them next quarter.
- B) Walk through the design together, use questions to help them find the flaws themselves, agree the corrections they will make, and set up a recurring design-review habit with them before future submissions.
- C) Tell them plainly the design is not ready, list the flaws in an email, and ask them to fix the items before the review.
- D) Let the design go to the design authority as it stands, so the formal review process gives them the feedback with appropriate weight.

**Most effective ranking: B, C, A, D.**

**Explanation:** Option B is the strongest because it fixes both the artefact and the architect: guided discovery ("what happens if this connection drops mid-transaction?") builds the reviewing instinct that emailed corrections never do, and the recurring pre-submission habit addresses the pattern — this is the second occurrence, so a systemic response is needed. This is your role profile's coaching duty in action: adapting feedback to ensure it is effective and lasting. Option C ranks second: it is honest, timely, and specific, and the design would be fixed — but a flaw list by email teaches compliance with your findings rather than the ability to find. Option A ranks third: the design authority sees a sound design, but the architect learns that failure means work is taken away from them, their anxiety is validated, and the third flawed design is now more likely, not less; deferred training three months away does not offset that. Option D is least effective and close to a breach of your own duties: knowingly sending a design with an unsecured database connection into governance wastes the authority's time, exposes the junior architect to a bruising experience you could have prevented, and misuses the assurance process as a teaching prop. Assurance exists to catch what leaders miss, not what they noticed and withheld.

**Scenario 3 (hard) — The supplier's generous offer**

You are leading the evaluation of suppliers for a major integration platform. One shortlisted supplier's account director, whom you know from a previous programme, invites you to their annual customer conference — flights and hotel covered — where, they mention, you could "see the roadmap nobody else gets to see". The evaluation closes in six weeks.

Which is the MOST effective and which is the LEAST effective response?

- A) Accept, since early roadmap insight would genuinely improve your evaluation of the supplier's capability.
- B) Decline the hospitality, record the offer in line with your organisation's gifts and hospitality process, and ask that any roadmap material relevant to the evaluation be submitted through the evaluation process so all bidders are treated equally.
- C) Decline politely but say nothing to anyone, to avoid causing awkwardness for a longstanding contact.
- D) Accept the conference invitation but pay for your own flights and hotel to remove the financial benefit.

**Most effective: B. Least effective: A.**

**Explanation:** Option B is the complete professional response: it removes the personal benefit, creates a transparent record (protecting you as much as the process — recorded declined offers are evidence of propriety if the procurement is later challenged), and converts the substantive value of the roadmap into a channel that preserves equal treatment of bidders, which is the legal and ethical backbone of public procurement. This is the commercial perspective skill exercised with integrity: evaluating suppliers includes managing how they seek to influence you. Option A is least effective: accepting covered travel from a shortlisted bidder during a live evaluation creates a conflict of interest that could void the procurement and end careers, and the "better evaluation" rationale is exactly the self-justification such hospitality is designed to invite. Option D removes the money but not the problem: private privileged access to one bidder's roadmap during an evaluation is an unfair advantage to that bidder regardless of who paid for the hotel. Option C avoids personal compromise but fails the transparency test — unrecorded approaches leave the next colleague they approach unprotected, and your organisation's process almost certainly requires recording. The instinct to protect a friendly contact from awkwardness is human; the discipline of your role is that propriety is procedural, not personal.

**Scenario 4 (hard) — Two teams, one architectural standoff**

Two delivery teams in your area are in escalating conflict over an integration contract. Team A insists on an event-driven interface, consistent with the target architecture you published. Team B, under a hard legislative deadline, wants a point-to-point interface it can build in half the time, and its delivery manager has accused Team A of "architectural purism that will make us break the law". The dispute has reached name-calling in a shared channel, and both teams have asked you to rule.

Rank the options from most to least effective.

- A) Rule in favour of Team A: the target architecture exists precisely to prevent expedient point-to-point proliferation.
- B) Rule in favour of Team B: legislative deadlines outrank architectural preferences, and the debt can be fixed later.
- C) Bring the teams together, reframe the question from "which interface" to "how do we meet the legal deadline without foreclosing the target architecture", and explore a time-boxed compromise such as a point-to-point interface behind a facade, with a funded, scheduled migration to events — recording the decision and debt transparently.
- D) Ask the programme director to decide, since the legislative risk makes this above your pay grade.

**Most effective ranking: C, A, B, D.**

**Explanation:** Option C is what mediation in difficult architectural discussions actually looks like: it de-escalates the interpersonal conflict by changing the question both teams have lost face over, honours the genuine constraint (the legislative deadline is real, and "comply with the law" is not negotiable), and protects the strategic direction by making the deviation explicit, contained, and funded rather than silent and permanent. The decision record and the named debt are what make this transparency rather than surrender. Option A ranks second because it defends a legitimate principle — but a ruling that ignores a legislative deadline will likely be overturned above you, and imposing it without addressing the conflict leaves the teams' relationship broken; you would win the interface and lose the community. Option B ranks third: it solves the deadline but teaches the whole organisation that deadline pressure defeats the target architecture every time, and "fix the debt later" without funding or schedule is how point-to-point spaghetti becomes permanent. Option D is least effective: this is precisely the decision a lead solution architect exists to make or broker — architectural risk affecting multiple teams — and escalating it wholesale signals that your governance role is decorative. Escalation is right when decisions exceed your authority; here the programme director would only ask you what to do anyway.

**Scenario 5 (moderate) — The accessibility shortcut**

Three weeks before a public beta assessment, a delivery team in your portfolio tells you they plan to defer fixing known accessibility failures in a shared component — keyboard navigation is broken for a significant journey — because "screen reader users are a tiny fraction of our traffic and we'll fix it in the next quarter". The service is used by people claiming a disability-related benefit.

Which is the MOST effective and which is the LEAST effective response?

- A) Agree to the deferral but ask the team to document it in the risk register.
- B) Explain that accessibility is a legal duty and a core standard, that this service's users are disproportionately likely to rely on assistive technology, and work with the team to reprioritise so the fixes land before the assessment — offering architectural help to reduce the cost of the fix.
- C) Report the team to the service assessment panel so the deferral is exposed.
- D) Suggest the team add a banner advising affected users to phone the helpline instead.

**Most effective: B. Least effective: D.**

**Explanation:** Option B combines the correct substance with the correct manner. Substantively, accessibility is a statutory obligation for public sector bodies and a condition of passing the service standard — and this scenario sharpens it: a disability-benefit service whose disabled users are treated as an edge case is a values failure, not just a compliance one. In manner, option B works with the team, brings help rather than only a demand, and uses your position to lower the cost of doing the right thing — collaboration in service of a non-negotiable. Option D is least effective because it converts a fixable defect into an institutionalised exclusion: routing disabled users to a phone line is a separate, lesser service, contradicts the equal-access principle at the heart of the standard, and would rightly fail the assessment anyway. Option A treats a legal duty as a schedulable risk; documentation does not discharge it, and the register entry would simply record a decision not to comply. Option C gets the substance right and the manner wrong: going straight to the panel without first working with the team burns trust you will need for years, and abandons your coaching role — escalation is the tool you reach for if the team refuses, not before. The pattern for values questions: user needs and legal duties are not trade-goods, but your first move is to make compliance achievable, not to punish.

**Scenario 6 (moderate) — The health check that found something**

You facilitate a quarterly architecture community health check across the six teams in your area. The anonymised results show one team scoring dramatically lower on "we can challenge technical decisions safely", with free-text comments describing their solution architect — one of your direct reports — as dismissive in design reviews. The architect is technically excellent, delivers reliably, and has just been praised by the programme director.

Rank the options from most to least effective.

- A) Share the anonymised results with the architect privately, ask for their perspective, agree specific behavioural changes for design reviews, and follow up by observing a review and re-checking the team's scores next quarter.
- B) Raise the pattern at your next team meeting of all six architects, without naming anyone, as a general reminder about review culture.
- C) Take no action this cycle: the evidence is anonymous survey data, and the architect's delivery record and the director's praise carry more weight.
- D) Move design review responsibilities for that team to another architect while you consider what to do.

**Most effective ranking: A, B, D, C.**

**Explanation:** Option A is the textbook use of a health check: the instrument exists to surface issues in team dynamics so they can be rectified, and your role profile explicitly includes identifying such problems and stimulating the right responses. The sequence matters — hear their perspective first (the data describes an experience, not a motive; there may be context), agree concrete observable changes rather than vague "be nicer" feedback, then verify through observation and the next cycle's data, which is what adapting feedback so it is effective and lasting means. Option B ranks second: it establishes norms and may prompt self-recognition, but broadcast feedback aimed at one person routinely misses its target — the architect in question often assumes it is about someone else, while conscientious colleagues wrongly self-accuse; it works as a supplement to A, not a substitute. Option D ranks third: it protects the team short-term but is a public, punitive-looking act taken without giving the architect the feedback or a chance to change — disproportionate as a first move, though reasonable if A fails. Option C is least effective: dismissing systematic signals because the person is technically strong is precisely how organisations teach their best people that behaviour does not matter, and psychological safety in design reviews is not a soft nicety — it is the mechanism by which flawed designs get challenged before they ship. Delivery excellence and dismissiveness compound: the better the architect, the fewer people dare to challenge, and the more expensive the eventual unchallenged mistake.

**Scenario 7 (hard) — The emerging technology and the board's scepticism**

Your horizon scanning suggests that a maturing technology could remove a whole category of manual reconciliation work across three departments, but it would cut across the current strategy you yourself published eighteen months ago, and two influential board members are known sceptics who recall a previous failed pilot of an earlier version. You have moderate but not conclusive evidence of the benefit.

Which is the MOST effective and which is the LEAST effective response?

- A) Leave it out of your strategy refresh until the evidence is conclusive, to protect your credibility with the sceptics.
- B) Propose a small, time-boxed, criteria-defined proof of concept in one department, present it to the board as a cheap way to settle the question either way, acknowledge the previous pilot's failure directly and explain what has changed since.
- C) Include full adoption of the technology in the strategy refresh, using your architectural authority to overcome the sceptics.
- D) Share the research informally with the three departments' architects and let them decide independently whether to trial it.

**Most effective: B. Least effective: C.**

**Explanation:** Option B is how a lead architect handles emerging technology under uncertainty: it right-sizes the commitment to the evidence (a proof of concept, not adoption), converts a political argument into an empirical one with pre-agreed success criteria — sceptics can support an experiment designed to be capable of failing — and deals with the previous pilot's ghost by naming it, since unaddressed history resurfaces at the worst moment. It also demonstrates the role behaviours of finding and using emerging technologies and developing or maintaining strategy in response to findings: a strategy you cannot revise in the face of evidence is dogma, and revising your own published strategy models intellectual honesty for your community. Option C is least effective: committing three departments on moderate evidence, over known board scepticism, by authority rather than persuasion, repeats the failure mode of the earlier pilot with higher stakes — and if it fails, it takes your strategy's credibility down with it. Option A is safe but is a dereliction of the horizon-scanning duty: opportunities to improve the organisation are part of your remit precisely because someone must be proactive about them, and "wait for conclusive evidence" often means "wait until a competitor department proves it first". Option D scatters the decision: three independent, uncoordinated trials duplicate cost, produce incomparable results, and abdicate the cross-cutting leadership that distinguishes your level.

**Scenario 8 (hard) — The governance shortcut under deadline**

A programme director asks you to give architectural sign-off for a solution "in principle" so that a funding gate can be passed this week, with the detailed design review to follow afterwards. The design pack is 60% complete; what exists looks reasonable, but the integration and security sections — historically where problems hide — are missing. Missing the gate delays the programme by a quarter and the director has been direct: "I need your signature, not your caveats."

Rank the options from most to least effective.

- A) Sign as asked, and rely on the detailed review to catch problems later.
- B) Refuse to sign and inform the director that the request itself was inappropriate, copying the head of architecture governance.
- C) Offer a conditional endorsement in writing: state precisely what has been reviewed and looks sound, what has not been reviewed, and the specific conditions and dates for completing the outstanding sections — and tell the director this is what you can honestly give the gate.
- D) Ask a peer lead architect to review the pack instead, since the director's pressure has compromised your independence.

**Most effective ranking: C, B, D, A.**

**Explanation:** Option C is the strongest because it refuses the dishonesty while solving the director's actual problem. Funding gates run on accurate information; a precisely scoped conditional endorsement gives the gate the truth in a usable form — many gates can and do proceed on conditions — and it puts the unreviewed integration and security sections on the record with dates, which is exactly what managing risks and decisions in a transparent way means. It treats "I need your signature, not your caveats" as an opening position, not an instruction: senior stakeholders routinely accept honest conditions when you make them concrete and workable, and respect is built rather than spent in the exchange. Option B ranks second: its substance is right — an unconditional signature would be wrong — but it maximises confrontation and skips the constructive step; escalation to governance is the right second move if the director rejects honest conditions and demands the clean signature anyway, not the right first move. Option D misdiagnoses the situation: pressure is not compromise, deflecting the decision wastes days the programme does not have, and a peer would face the identical incomplete pack — this is your call to make. Option A is least effective and the most dangerous option in this entire assessment: an unconditional sign-off on an unreviewed security section is your professional assurance given to something you have not assured, and when the retrospective review finds the problem, the record will show your signature and no caveats. The lesson generalises: your signature is the currency of architectural governance, and its value to everyone — including directors under deadline — depends on it never being available under pressure.

**Scenario 9 (moderate) — The cross-department dependency nobody owns**

While supporting one of your programmes, you notice that a reference-data service owned by another department is due for decommissioning in nine months — and that at least four services across your organisation, two outside your own area, silently depend on it. No one appears to be tracking this. Your own programmes would survive with modest rework; the worst-exposed service belongs to a different directorate you have no relationship with.

Which is the MOST effective and which is the LEAST effective response?

- A) Handle the rework in your own programmes and leave the other directorates to discover the issue through their own processes.
- B) Verify the dependency picture, alert the affected teams and the owning department directly, and raise the issue at the cross-organisation architecture forum with a proposed coordination approach — offering to broker the conversation with the service owner about timelines.
- C) Send a one-line note to the enterprise architecture mailbox flagging the decommissioning date, and consider the duty discharged.
- D) Ask the owning department to delay decommissioning by a year, buying everyone time.

**Most effective: B. Least effective: A.**

**Explanation:** Option B is "architect for the whole context" made concrete: tracking issues that could affect the work of teams across the organisation and taking action by influencing colleagues beyond your own patch is a named behaviour of your role, not a nice-to-have. The sequence in B is deliberate — verify first (false alarms spend credibility), notify the affected and the owner directly (mailing lists are not notification), then use the cross-organisation forum to create ownership and coordination rather than four uncoordinated bilateral scrambles. Offering to broker reflects the reality that you currently hold the most complete picture. Option A is least effective because it optimises your patch while knowingly letting colleagues walk into a nine-month cliff — a failure of exactly the whole-context duty, and organisationally self-defeating: the eventual emergency will land on shared infrastructure, shared suppliers, and possibly shared headlines. Option C performs notification without achieving it; a mailbox note discharges nothing if nobody reads it, and you know the stakes. Option D is premature and presumptuous as a first move: the owning department has its own reasons and budget for decommissioning, a delay may be impossible or costly, and requesting one before the affected services have even assessed their options asks for the wrong favour with information you have not yet gathered. Delay may emerge as the right answer — from the coordinated conversation B creates.

**Scenario 10 (moderate) — Feedback that did not land**

Six weeks ago you gave one of your solution architects feedback that their design documents were too technology-centred for business stakeholders — packed with component diagrams, silent on outcomes, costs, and user impact. They agreed enthusiastically. The latest document is unchanged. A business sponsor has now emailed you saying they "cannot engage with what the architecture team sends".

Rank the options from most to least effective.

- A) Rewrite the latest document yourself and send your version to the sponsor, copying the architect so they can see the difference.
- B) Revisit the feedback with the architect: acknowledge it did not stick, explore why (do they know what good looks like? do they have an example? do they believe it matters?), then work a real document together — pairing on restructuring the latest one for the sponsor — and agree a checkpoint on the next two documents.
- C) Repeat the original feedback more firmly, adding that the sponsor has now complained, and ask them to redo the document by Friday.
- D) Create a mandatory template for business-facing architecture documents across your whole team, so the standard no longer depends on individual judgement.

**Most effective ranking: B, D, C, A.**

**Explanation:** Option B applies the core insight of your role profile's phrase "adapt feedback to ensure it's effective and lasting": when feedback is accepted but not acted on, repetition is rarely the answer — diagnosis is. Enthusiastic agreement followed by no change usually means a capability gap (they cannot picture the target) rather than a motivation gap, and pairing on a real document converts abstract advice into demonstrated skill while directly repairing the sponsor relationship with a better artefact. The checkpoint makes the change verifiable. Option D ranks second and pairs well with B: templates institutionalise the standard, help the whole team, and reflect your duty to develop best practice for solution architecture — but alone, a template fixes the form and not the writer; component-centred thinking will leak through the mandated headings. Option C ranks third: firmness and the sponsor's complaint add urgency, but it repeats a treatment that has already failed once and adds deadline pressure to a person who likely does not know how to do what you are asking. Option A is least effective: it meets the sponsor's immediate need at the cost of humiliating the architect (the copied comparison is a public lesson in inadequacy), teaches them that failure transfers their work to you, and leaves the underlying skill exactly where it was. Rewriting is occasionally right in a genuine emergency — but silently, followed by B, never as the visible lesson.

### Preparation tips

- **Anchor yourself in the values before you start.** Re-read the service standard's spirit: user needs first, transparency, collaboration, accessibility, and stewardship of public money. When two options both seem sensible, the one that better embodies these values almost always scores higher in a public sector assessment.
- **Think altitude.** Before rating options, ask: what does the organisation need from a lead architect here — as opposed to a junior architect, a delivery manager, or a director? Options that do a junior's work, or push a lead's decision upward, are usually distractors. The strongest options resolve, equip, or escalate deliberately — in that order of preference.
- **Look for the option that addresses the pattern, not just the instance.** At your level, scenarios frequently contain a repeat problem (the second flawed design, the feedback that did not stick). Strong answers fix the artefact and the cause; answers that fix only today score mid-table.
- **Be suspicious of passive and postponing options.** "Wait for more evidence", "let the formal process handle it", "say nothing to avoid awkwardness" — passivity dressed as prudence is the most common least-effective option across the format.
- **Watch for manner as well as substance.** Many option sets include one choice with the right substance delivered destructively (public ambush, immediate escalation, punitive first moves). These rank above passivity but below the option that pairs the same substance with private, constructive delivery.
- **Practise explaining your rankings aloud.** The reasoning habit — "B beats C because it addresses the root cause and preserves the relationship" — sharpens your judgement faster than silent answering, and it doubles as preparation for the interviews and boards where you will defend real decisions.

### Common pitfalls

- **Answering idealistically rather than effectively.** Choosing what sounds noble ("always escalate wrongdoing immediately") over what works (give the person or team the chance to fix it first, then escalate) misreads how effective public sector leaders actually operate.
- **Ignoring the stated context.** Details like "the minister's office has been told", "this is the second occurrence", or "the evaluation closes in six weeks" are not scenery — they are what makes one option better than its neighbours. Rushing past them flattens the dilemma.
- **Selecting passive options.** Options that delay action, pass the problem to someone else, or ignore the root issue are systematically scored as weak. If your instinct under uncertainty is to wait, interrogate it.
- **Over-escalating or under-escalating.** Escalation as a first resort signals you cannot operate at your level; refusal to escalate genuinely out-of-authority matters (legal breaches, refused governance) signals poor judgement. Calibrate to what the scenario says about authority and risk.
- **Solving the technical problem and ignoring the people.** Lead-architect scenarios almost always contain both an architectural question and a relationship under strain. Options that win the argument while breaking the relationship rarely top the key.
- **Forgetting you are being assessed as a leader.** Every scenario involving a junior colleague is partly asking: does this person develop others? Answers where you absorb, redo, or bypass your team's work may look efficient and score poorly.

## Conclusion

You have now worked through four complete, role-specific assessment resources: cognitive ability exercises built from the design packs, governance rules, and dependency chains you handle every week; numeric reasoning drawn from the supplier comparisons, capacity models, and benefit profiles that underpin your recommendations; verbal reasoning grounded in the codes of practice, contract clauses, and stakeholder correspondence you read forensically; and situational judgement dilemmas that mirror the leadership, coaching, and integrity decisions that define the lead solution architect role.

If one theme runs through all four sections, it is this: the assessments are not testing something foreign to you. They are testing, under time pressure and in compressed form, the same disciplines you practise daily — reading exactly what a document says, recomputing the numbers before trusting them, checking every option against every constraint, and choosing responses that are transparent, collaborative, and anchored in user needs and public value. That should give you genuine confidence. Preparation for you is less about learning new material and more about sharpening familiar instincts into fast, deliberate technique.

As next steps, consider spacing your practice rather than cramming it: two or three short sessions a week, alternating question types, will do more for your speed and accuracy than a single long sitting. Revisit the questions you got wrong after a fortnight — if you get them right for the right reasons, the learning has stuck. And use this material twice over: once for yourself, and once for the junior architects you lead. Walking a mentee through why one situational judgement option beats another, or how a Cannot Say verdict is reached, is coaching of exactly the kind your role profile asks of you — and nothing consolidates your own judgement like teaching it.

Finally, keep perspective. An assessment is a snapshot; your professional development is the film. Whether you are preparing for a specific selection process or simply investing in your own growth, the habits rehearsed here — evidence before opinion, transparency in decisions, and bringing others with you — are the ones that will carry you well beyond any test. Good luck. You are better prepared than you think.
