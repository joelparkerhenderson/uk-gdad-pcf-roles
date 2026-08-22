# Enterprise Architect - Psychometric Assessment Resources

## Introduction

Welcome! This document is designed especially for you as an enterprise architect working within the UK Government Digital and Data profession. Whether you are preparing for an internal assessment, applying for a new post, benchmarking your own capabilities, or simply investing in your professional development, this resource will help you understand, practise, and feel confident about the four most common types of workplace psychometric assessment you are likely to encounter.

Psychometric assessments are structured, standardised exercises that measure the mental processes and judgement you use every day in your role. For an enterprise architect, that means far more than abstract puzzles. Well-designed, job-specific assessments mirror the real work you do: translating business strategy into technical delivery, weighing architectural options against value for money, reading dense policy and standards documents, interpreting portfolio budgets and capacity figures, and navigating complex stakeholder relationships across an entire organisation. Because your role sits at the intersection of business, technology and data, assessments for enterprise architects tend to be broad, strategic, and scenario-rich — and that is exactly how this document approaches them.

This resource is organised into four main sections, one for each assessment type:

1. **Workplace job-specific cognitive assessment** — measuring pattern recognition, logical deduction, error checking, prioritisation and problem solving using the artefacts you genuinely handle: roadmaps, reference architectures, principles, standards and transition states.
2. **Workplace job-specific numeric reasoning assessment** — measuring your ability to interpret budgets, licensing costs, capacity figures, portfolio metrics and total cost of ownership comparisons.
3. **Workplace job-specific verbal reasoning assessment** — measuring precise comprehension of the written material you work with daily: architecture principles, government standards, strategy papers, governance minutes and stakeholder emails.
4. **Workplace job-specific situational judgement assessment** — measuring the quality of your professional judgement in realistic dilemmas involving senior stakeholders, delivery teams, governance boards and suppliers.

Each section explains what the assessment measures, maps it explicitly to the skills in your role profile — architecting for the whole context, architecture communication, commercial perspective, community collaboration, enterprise architecture, making architectural decisions, problem definition and shaping, and strategy design — and then gives you a substantial set of practice questions with full worked explanations, followed by preparation tips and common pitfalls.

How should you use this document? Work through it at your own pace. Try each practice question honestly before reading the answer. Use the explanations not just to check whether you were right, but to understand the reasoning pattern being tested. Reflect on where you felt confident and where you hesitated — those hesitations are your best guide to targeted preparation. Above all, remember that these assessments measure skills you already exercise every working day. This document simply helps you show them at their best.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive ability assessment is a targeted psychometric test that measures the exact mental processes needed for your role — not abstract intelligence, but applied thinking. Unlike a generic IQ test, it uses practical workplace scenarios and realistic artefacts to predict how effectively you will perform as an enterprise architect. Questions mimic the everyday tasks and data formats of your actual job: architecture roadmaps, dependency maps, principles catalogues, transition-state plans and governance decision logs.

Typical format and timing: these assessments are usually delivered online and timed, most commonly 15 to 30 minutes, with objective scoring against a benchmark or norm group. Many platforms offer short, ungraded practice questions first so you can get comfortable with the interface, and some use adaptive testing that adjusts question difficulty based on your previous answers. Employers typically receive a breakdown showing speed versus accuracy rather than a single score, so working carefully and steadily matters as much as working quickly.

For an enterprise architect, cognitive assessment matters because your role is fundamentally about structured thinking under complexity. You are expected to take a strategic view across all architectural domains, portfolios and programmes; to spot inconsistencies between 'as is', 'to be' and transitional states; to trace interdependencies through the organisation's ecosystem; and to prioritise changes that enable delivery at pace. Every one of those duties is, at its core, a cognitive operation: pattern recognition, logical deduction, error checking, prioritisation and problem solving. A well-designed cognitive assessment for your role simply isolates these operations and measures them directly.

### What it measures for your role

The dimensions of a cognitive assessment map closely onto the skills in your role profile:

- **Enterprise architecture**: turning an organisation's goals into clear objectives requires logical decomposition — breaking a broad ambition into ordered, testable steps. Cognitive questions test exactly this: given a goal and a set of constraints, can you deduce the valid sequence of actions?
- **Making architectural decisions**: identifying and addressing architectural risks across business, data and security domains depends on error checking and inference. Questions will present decision records, dependency tables or principle sets containing subtle contradictions for you to find.
- **Problem definition and shaping**: framing a problem so a solution can be created is pattern recognition applied to messy information. Expect questions that ask you to identify which problem statement correctly captures a scenario, or which option set is logically complete.
- **Architect for the whole context**: tracking emerging internal and external issues over time is trend and pattern detection. Questions may show sequences of events, incident logs or horizon-scanning summaries and ask what pattern they reveal.
- **Strategy design**: using architectural principles, patterns and constraints appropriately is rule application — a classic deductive reasoning task. Expect questions where you must apply a stated principle to a novel case and identify which conclusion validly follows.
- **Prioritisation for delivery at pace**: your duty to identify priorities for change is tested through ordering and scheduling puzzles built from roadmaps, dependencies and capacity constraints.

### Practice questions

Work through each question before reading the answer. Time yourself if you can — around 90 seconds to 3 minutes per question is realistic for this difficulty range.

#### Question 1 (easy) — Applying an architectural principle

Your organisation has established the architectural principle: "Reuse before buy, buy before build." A delivery team needs a document-management capability. The following options exist:

- Option A: An existing document-management platform already licensed and operated by another directorate, meeting 90% of the team's needs.
- Option B: A commercial off-the-shelf product, not currently licensed, meeting 100% of the team's needs.
- Option C: A bespoke build by the delivery team, estimated at nine months of effort.

According to the principle, which option should be evaluated first?

1. Option A
2. Option B
3. Option C
4. Options B and C jointly

**Correct answer: 1 (Option A).**

**Explanation:** The principle establishes a strict order of evaluation: reuse first, then buy, then build. Option A is the reuse candidate — an existing, already-licensed platform within the organisation. It must be evaluated first, regardless of the fact that Option B offers a higher functional fit. The principle does not say reuse must always win; it says reuse must be considered first. This distinction — between an order of evaluation and a guaranteed outcome — is exactly the kind of precise rule-reading that cognitive assessments reward, and that you apply whenever you recommend reuse, sustainability and scalability to achieve value for money.

#### Question 2 (easy) — Error checking a roadmap

An enterprise roadmap lists four transition states for retiring a legacy case-management system:

- T1 (Q1): New platform procured and hosting environment established.
- T2 (Q2): Data migration completed from legacy system to new platform.
- T3 (Q3): Legacy system decommissioned and contract terminated.
- T4 (Q4): Parallel running of legacy and new platform, with reconciliation checks.

Which statement identifies the logical error in this roadmap?

1. Procurement should never precede hosting decisions.
2. Parallel running (T4) is scheduled after the legacy system has already been decommissioned (T3), which is impossible.
3. Data migration should follow decommissioning.
4. There is no logical error; the roadmap is valid.

**Correct answer: 2.**

**Explanation:** Parallel running requires both systems to be operational at the same time so outputs can be reconciled. T3 decommissions the legacy system in Q3, yet T4 schedules parallel running of that same system in Q4 — after it no longer exists. The sequence is internally contradictory: T4 must come before T3. Option 1 is a plausible-sounding but unsupported generalisation, and option 3 reverses a sensible order. Spotting sequence contradictions in transition states is a core part of owning 'as is', 'to be' and transitional architectures — assessors use exactly this kind of artefact because you genuinely review such roadmaps.

#### Question 3 (moderate) — Dependency deduction

Five capability changes (V, W, X, Y, Z) must be scheduled. The dependency rules are:

- X cannot start until W is complete.
- Z cannot start until both X and Y are complete.
- Y cannot start until W is complete.
- V has no dependencies.

Only two changes can run in parallel at any time, and each change takes exactly one quarter. What is the minimum number of quarters needed to complete all five changes?

1. Three quarters
2. Four quarters
3. Five quarters
4. Two quarters

**Correct answer: 1 (three quarters).**

**Explanation:** Work through the dependency graph. Quarter 1: W and V can run together (V has no dependencies; W unlocks everything else). Quarter 2: with W complete, X and Y can now run in parallel — that fills both slots. Quarter 3: with X and Y complete, Z can run. Total: three quarters. The trap answers arise from scheduling V unnecessarily late (forcing a fourth quarter) or serialising X and Y. This is precisely the reasoning you use when sequencing cross-cutting capabilities on an enterprise roadmap under constrained delivery capacity: identify the critical path (W → X/Y → Z), then pack independent work (V) into spare capacity as early as possible.

#### Question 4 (moderate) — Pattern recognition in incident trends

Horizon scanning of your organisation's operational data shows the following pattern of integration-related incidents over six months, split by integration style:

- Point-to-point interfaces: 8, 11, 15, 20, 26, 33 incidents.
- API-gateway-managed interfaces: 6, 6, 7, 6, 7, 7 incidents.

The number of point-to-point interfaces grew by roughly 10% over the period, while API-gateway-managed interfaces grew by roughly 40%. Which conclusion is best supported?

1. API gateways cause fewer integrations to be built.
2. Incidents on point-to-point interfaces are growing much faster than the interface count itself, suggesting a scaling problem inherent to that style.
3. Point-to-point interfaces are cheaper to operate.
4. The organisation should stop building APIs.

**Correct answer: 2.**

**Explanation:** Point-to-point incidents roughly quadrupled (8 to 33) while the interface count grew only about 10% — incident growth is wildly out of proportion to estate growth, indicating the style itself scales badly (each new point-to-point connection multiplies interaction complexity). By contrast, gateway-managed incidents stayed flat (6–7) despite 40% estate growth, indicating that style absorbs growth well. Option 1 confuses incident data with build-rate causation; option 3 introduces cost data that was never given; option 4 contradicts the evidence. This question mirrors your horizon-scanning duty: identifying emerging trends, separating signal from noise, and drawing only the conclusion the data supports.

#### Question 5 (moderate) — Logical deduction from principles

Your principles catalogue contains three statements:

- P1: All citizen-facing services must meet the government accessibility standard.
- P2: Any service that meets the accessibility standard must have passed an accessibility audit.
- P3: Service Gamma has not passed an accessibility audit.

Which conclusion follows logically?

1. Service Gamma is not a citizen-facing service.
2. Service Gamma does not meet the accessibility standard, so if it is citizen-facing, it is non-compliant with P1.
3. Service Gamma must be decommissioned.
4. Service Gamma meets the accessibility standard but skipped the audit.

**Correct answer: 2.**

**Explanation:** This is a chained deduction using the contrapositive. P2 says meeting the standard requires a passed audit; Gamma has no passed audit (P3), so Gamma cannot meet the standard. P1 requires all citizen-facing services to meet the standard, so if Gamma is citizen-facing, it breaches P1. Note what we cannot conclude: we do not know whether Gamma is citizen-facing (so option 1 overreaches), no principle mandates decommissioning (option 3), and option 4 directly contradicts P2. Assessments frequently test whether you can hold the line between what follows necessarily and what merely might be true — the same discipline you apply when engaging with architectural governance and assurance, where overclaiming from evidence undermines decisions.

#### Question 6 (moderate) — Prioritisation for delivery at pace

You must recommend which one of four change initiatives to prioritise this quarter. Your organisation's stated prioritisation rule is: "Prioritise the change that unblocks the greatest number of dependent programmes, breaking ties by lowest delivery risk."

- Initiative 1: Unblocks 3 programmes; delivery risk rated Medium.
- Initiative 2: Unblocks 5 programmes; delivery risk rated High.
- Initiative 3: Unblocks 5 programmes; delivery risk rated Low.
- Initiative 4: Unblocks 4 programmes; delivery risk rated Low.

Which initiative should you recommend?

1. Initiative 1
2. Initiative 2
3. Initiative 3
4. Initiative 4

**Correct answer: 3 (Initiative 3).**

**Explanation:** Apply the rule in strict order. First criterion: greatest number of dependent programmes unblocked. Initiatives 2 and 3 tie at five programmes each, ahead of Initiative 4 (four) and Initiative 1 (three). Second criterion, applied only to break the tie: lowest delivery risk. Initiative 3 (Low) beats Initiative 2 (High). Initiative 4 is the classic distractor — Low risk and a respectable four programmes — but the rule makes unblocking count first, and risk only functions as a tiebreak. Cognitive assessments often test whether you apply a stated decision rule faithfully rather than substituting your own intuition. In your role, this mirrors applying agreed prioritisation criteria consistently so that decisions are defensible at governance boards.

#### Question 7 (moderate) — Error checking a decision record

An architecture decision record (ADR) reads:

"Decision: Adopt the shared identity platform for all new services. Rationale: The shared platform reduces duplication, is already assured for OFFICIAL data, and all new services in scope process OFFICIAL data only. Consequence: Service teams handling SECRET data will onboard to the shared platform by Q3."

What is the logical flaw in this ADR?

1. The rationale mentions cost reduction but provides no figures.
2. The consequence introduces SECRET-data services, which the rationale explicitly excluded from scope, and extends them onto a platform assured only for OFFICIAL data.
3. Q3 is too soon for onboarding.
4. Shared platforms cannot reduce duplication.

**Correct answer: 2.**

**Explanation:** The rationale carefully scopes the decision: the platform is assured for OFFICIAL, and all in-scope services process OFFICIAL only. The consequence then contradicts that scope twice over — it brings SECRET-data services in, and it implies they will run on a platform not assured for their classification. Options 1 and 3 are judgement quibbles, not logical flaws in the record itself; option 4 is false. Detecting internal inconsistency between rationale, scope and consequence is a bread-and-butter skill for making architectural decisions with managed risk, and for the security-domain risk identification your role profile names explicitly.

#### Question 8 (challenging) — Whole-context inference

Three facts emerge from your ecosystem analysis:

- Fact 1: Every programme that consumes the payments capability also consumes the notifications capability.
- Fact 2: No programme that consumes the notifications capability is hosted in the legacy data centre.
- Fact 3: Programme Delta is hosted in the legacy data centre.

Which statement must be true?

1. Programme Delta consumes the payments capability.
2. Programme Delta consumes neither the payments nor the notifications capability.
3. Programme Delta consumes notifications but not payments.
4. Programme Delta will migrate out of the legacy data centre.

**Correct answer: 2.**

**Explanation:** Chain the deductions. From Fact 2's contrapositive: any programme in the legacy data centre does not consume notifications. Delta is in the legacy data centre (Fact 3), so Delta does not consume notifications. From Fact 1's contrapositive: any programme that does not consume notifications cannot consume payments (because consuming payments would force notifications consumption). Therefore Delta consumes neither. Option 4 may be desirable but is not entailed by the facts. This double-contrapositive structure appears frequently in higher-difficulty cognitive items, and it is a formalised version of the interdependency tracing you do when you map the organisation's ecosystem and reference architectures.

#### Question 9 (challenging) — Problem framing

A director tells you: "Our case-handling service is too slow. Buy a faster database." Investigation shows: database queries average 40ms; the service makes 300 sequential calls to a legacy API per case, each averaging 250ms; and caseworkers re-key data between two screens. Which problem framing best enables a solution?

1. "The database is too slow and needs replacement."
2. "Caseworkers type too slowly and need training."
3. "End-to-end case processing time is dominated by 300 sequential legacy API calls (roughly 75 seconds per case) and manual re-keying; the database contributes negligibly."
4. "The service needs a full rebuild on a modern platform."

**Correct answer: 3.**

**Explanation:** Do the arithmetic embedded in the evidence: 300 calls × 250ms = 75,000ms = 75 seconds per case from sequential API calls alone, versus a 40ms database query — the database is three orders of magnitude away from being the bottleneck. Option 3 is the only framing that locates the problem where the evidence puts it, quantifies it, and leaves solution options open (parallelise calls, batch the API, integrate the screens). Option 1 restates the director's assumption, which the data refutes; option 2 blames users for a system-imposed task; option 4 jumps to a solution without a defined problem. This is problem definition and shaping in miniature: challenge the presented assumption, frame the problem from evidence, and keep the option space open at an appropriate level of detail.

#### Question 10 (challenging) — Pattern completion in capability maturity

Your capability maturity reviews score capabilities from 1 to 5. Over four assessment cycles, three capabilities scored:

- Integration: 2, 3, 4, ?
- Data governance: 1, 2, 2, 3
- Identity: 3, 3, 4, 4

Each capability improves by one level per cycle whenever it received targeted investment that cycle, and stays flat otherwise. Integration received targeted investment in every cycle so far. If integration's investment continues, and no capability can exceed level 5, what is integration's most likely score in cycle 4, and in cycle 5?

1. 5, then 5
2. 4, then 5
3. 5, then 6
4. 4, then 4

**Correct answer: 1 (5, then 5).**

**Explanation:** Integration has risen one level per cycle (2→3→4) under continuous investment, so cycle 4 brings it to 5. In cycle 5, the stated ceiling applies: no capability can exceed level 5, so it remains at 5 even with continued investment. Option 3 ignores the explicit constraint; option 2 misreads the series (the "?" is cycle 4, which follows the third value of 4). The underlying skill is disciplined extrapolation: continue a pattern only as far as the stated rules allow, then let constraints override the trend. In practice, this is how you forecast capability roadmaps honestly rather than optimistically.

#### Question 11 (challenging) — Standards consistency check

Four statements appear across your organisation's standards library:

- S1: All new services must use the corporate API gateway.
- S2: Services classified as "internal analytics" are exempt from S1.
- S3: All services that handle citizen data must use the corporate API gateway, without exemption.
- S4: Service Epsilon is a new internal analytics service that handles citizen data.

What is Epsilon's correct obligation, and why?

1. Exempt from the gateway, because S2 exempts internal analytics.
2. Must use the gateway, because S3 removes the exemption for citizen-data services and S4 confirms Epsilon handles citizen data.
3. Exempt, because S2 was written after S1.
4. Cannot be determined.

**Correct answer: 2.**

**Explanation:** Epsilon triggers two rules that pull in opposite directions: S2 (exempt, as internal analytics) and S3 (must use the gateway, as a citizen-data service). The resolution is in S3's own wording: "without exemption" explicitly disables carve-outs such as S2 for the citizen-data case. So the specific, exemption-proof rule prevails and Epsilon must use the gateway. Option 3 invents a recency rule the question never states — a classic distractor that imports outside assumptions. Reconciling apparently conflicting standards, and finding the clause that resolves the conflict, is exactly what you do when you establish and maintain architectural principles, policies and standards across an enterprise.

#### Question 12 (challenging) — Multi-constraint problem solving

You are scoping a shared-hosting consolidation. Constraints:

- C1: Workloads A and B cannot share a platform (regulatory separation).
- C2: Workload C must co-locate with A (latency-critical integration).
- C3: Workload D must co-locate with B (shared data store).
- C4: You may operate at most two platforms.

Which allocation satisfies all constraints?

1. Platform 1: A, C. Platform 2: B, D.
2. Platform 1: A, B. Platform 2: C, D.
3. Platform 1: A, D. Platform 2: B, C.
4. No allocation is possible with two platforms.

**Correct answer: 1.**

**Explanation:** Test option 1 against each constraint: A and B are on different platforms (C1 satisfied); C sits with A (C2 satisfied); D sits with B (C3 satisfied); exactly two platforms are used (C4 satisfied). Option 2 violates C1 immediately. Option 3 violates both C2 (C is separated from A) and C3 (D is separated from B). Since option 1 works, option 4 is false. The efficient technique is constraint propagation: C1 forces A and B apart, which anchors the two platforms; C2 and C3 then place C and D deterministically. Constraint-driven placement like this is the cognitive core of designing target architectures under regulatory, technical and commercial constraints simultaneously.

#### Question 13 (moderate) — Sequence recognition in technology lifecycle

Your technology radar tracks each product through the lifecycle stages: Assess → Trial → Adopt → Contain → Retire. A product's history reads: Assess (2021), Trial (2022), Adopt (2023), Contain (2025). A colleague proposes moving it back to "Adopt" in 2026 because a new vendor version has been released. According to the lifecycle model as stated, which reasoning is soundest?

1. Reverting to Adopt is consistent with the lifecycle, because new versions reset the lifecycle.
2. The stated lifecycle is a forward sequence; a new vendor version is effectively a new candidate, which should enter at Assess rather than jumping straight back to Adopt.
3. The product should move directly to Retire.
4. The product should stay in Contain forever.

**Correct answer: 2.**

**Explanation:** The model as given is a one-directional sequence with no reset rule. Nothing in it permits backwards movement, so option 1 asserts a rule that does not exist. Option 3 skips a stage without justification, and option 4 turns the absence of a rule into an absolute prohibition on change. Option 2 respects the stated model while accommodating the genuinely new information: a materially new version can be treated as a new entrant, assessed on its merits. This tests a subtle cognitive skill — extending a rule system consistently when it meets a case it did not anticipate — which is exactly what you do when you maintain standards and horizon-scan emerging technologies whose novelty strains existing categories.

#### Question 14 (challenging) — Spotting the flawed inference in a business case

A business case argues: "Departments that adopted the shared platform reduced their running costs by an average of 20%. Therefore, if the remaining departments adopt it, total running costs across the organisation will fall by 20%."

What is the strongest criticism of this inference?

1. Twenty per cent is too small a saving to matter.
2. The early adopters may differ systematically from the remaining departments (for example, simpler estates or newer systems), so their average saving cannot simply be projected onto the rest — and a 20% saving in some departments does not equal a 20% fall in total organisational costs.
3. Shared platforms never save money.
4. The business case should have used median rather than mean.

**Correct answer: 2.**

**Explanation:** The inference commits two errors at once. First, selection bias: departments that adopted early are unlikely to be representative — early adopters often have the easiest migrations and thus the largest savings. Second, a scope error: even if every department saved 20% of its own running costs, total organisational costs would fall 20% only if the platform-relevant costs made up the whole cost base, which is not established. Option 4 raises a legitimate statistical preference but is far weaker than the structural flaws; options 1 and 3 are assertions, not criticisms of the reasoning. Assessing whether the evidence in a business case actually supports its conclusion is central to guiding the organisation towards decisions that genuinely achieve value for money.

### Preparation tips

- **Practise with your own artefacts.** Take a real roadmap, ADR log or principles catalogue and interrogate it: what depends on what? Which statements could contradict each other? This builds the exact muscles the assessment measures, using material you already understand deeply.
- **Learn to spot the contrapositive.** Many of the hardest deduction items (like Questions 5 and 8) hinge on reasoning backwards from a rule. If "all X must Y", then anything that is not-Y cannot be X. Drill this until it is reflexive.
- **Apply stated rules, not your own experience.** As a seasoned architect you carry strong intuitions. In the assessment, the stated rule always wins (see Question 6). Read the decision criteria as carefully as you would read a contract clause.
- **Manage your time strategically.** Treat the test like a portfolio: invest first where return is certain. Answer the questions you can solve quickly, flag the multi-constraint puzzles, and return to them.
- **Rest and pace yourself.** These tests reward calm, systematic thinking. A rushed first read that misses one word ("without exemption", "sequential", "at most") costs more time than a careful read ever would.

### Common pitfalls

- **Overclaiming beyond the evidence.** Choosing a conclusion that is plausible in your professional experience but not entailed by the given facts. Assessors deliberately include "sensible but unsupported" options.
- **Substituting judgement for rule application.** When a prioritisation or decision rule is stated, applying your own weighting instead of the rule's strict order.
- **Missing scope words.** Qualifiers such as "all", "only", "new services", "without exemption" and "at most" carry the entire logical load of a question. Skimming past them is the single most common error.
- **Time-sink questions.** Getting anchored on one difficult multi-stage puzzle instead of banking the easier marks first — a pitfall the assessment literature flags for candidates at every level.
- **Assuming the artefact is correct.** Several question types (Questions 2 and 7) reward finding the flaw. Approach every roadmap, ADR and standard in the test the way you would in a governance review: sceptically.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment evaluates your ability to analyse, interpret, and make sound decisions using numerical data drawn from your actual role. It mimics the data-handling demands of enterprise architecture, focusing on practical business mathematics — percentages, ratios, cost comparisons and capacity figures — rather than abstract formulae. The question inputs are the tables and figures you already encounter: portfolio budgets, licensing schedules, total cost of ownership comparisons, hosting capacity plans, benefits projections and sustainability metrics.

Typical format and timing: numeric reasoning tests are usually online, strictly timed, and calculator-friendly — most platforms allow or provide an on-screen calculator, because the point is interpretation, not mental arithmetic. Expect a series of data sets (a table or chart) each followed by two to four questions, with roughly one to two minutes per question. Accuracy under time pressure is the game: quick, correct extraction of the right figures from a busy table matters more than mathematical sophistication.

Why does this matter for your role? As an enterprise architect you guide the organisation to make business, technology and data decisions that achieve value for money and reduce risk. That guidance is only credible when it is numerate. When you recommend reuse over rebuild, the recommendation rests on a cost comparison. When you advise on sustainability and scalability, you are reasoning about capacity growth curves and consumption figures. When you present a roadmap to an investment board, you must speak fluently about programme budgets, benefit profiles and run-cost trajectories. A numeric reasoning assessment for your role measures whether you can do this reliably, quickly, and without being misled by the way data is presented.

### What it measures for your role

The assessment dimensions map to your role profile skills like this:

- **Commercial perspective**: understanding sourcing strategies and commercial processes requires comparing contract costs, licence models (per-user versus consumption-based), and total cost of ownership across options. Expect questions built on supplier pricing tables and contract schedules.
- **Enterprise architecture** and **strategy design**: roadmaps and target states carry cost and capacity numbers. Questions will test whether you can project run costs across transition states, calculate cumulative savings, and check whether a benefits profile actually adds up.
- **Making architectural decisions**: decisions characterised by managed levels of risk need quantified trade-offs — for example, weighted scoring of options or expected-cost calculations that combine probability and impact.
- **Architect for the whole context**: tracking issues across the organisation means reading portfolio-level dashboards: percentages of programmes on track, aggregate spend against budget, and trend lines across quarters.
- **Guiding value for money**: the duty to recommend reuse, sustainability and scalability is tested through cost-per-unit comparisons, capacity utilisation ratios and energy or carbon figures.

### Practice questions

An on-screen calculator is normally allowed — use one here too. The explanations show the arithmetic in full so you can check your working.

#### Question 1 (easy) — Percentage of portfolio spend

Your architecture portfolio dashboard shows annual spend across four domains: business change £2.4m, technology £5.1m, data £1.8m, and security £0.7m. What percentage of total portfolio spend goes to the data domain, to the nearest whole per cent?

1. 15%
2. 18%
3. 21%
4. 24%

**Correct answer: 2 (18%).**

**Explanation:** Total spend = 2.4 + 5.1 + 1.8 + 0.7 = £10.0m. Data domain share = 1.8 ÷ 10.0 = 0.18 = 18%. The round total (£10.0m) is a gift — always add the whole column first, because percentage questions frequently hinge on a total that is easier than it looks. Misreading which row is "data" under time pressure is the main hazard here, which is why careful table navigation is worth a deliberate second glance.

#### Question 2 (easy) — Licence cost comparison

A shared platform offers two licence models for a service with 3,200 users:

- Model A: £18 per user per year.
- Model B: flat fee of £42,000 per year plus £4 per user per year.

Which model is cheaper for this service, and by how much per year?

1. Model A, by £2,800
2. Model B, by £2,800
3. Model B, by £12,800
4. Model A, by £12,800

**Correct answer: 2 (Model B, by £2,800).**

**Explanation:** Model A: 3,200 × £18 = £57,600. Model B: £42,000 + (3,200 × £4) = £42,000 + £12,800 = £54,800. Difference: £57,600 − £54,800 = £2,800 in favour of Model B. Distractor 3 (£12,800) is simply the per-user component of Model B — a figure you compute along the way and might grab in haste. This "intermediate value planted as an option" trick is extremely common in numeric tests. There is also a professional insight embedded here: flat-plus-per-user models beat pure per-user models above a break-even user count (here, £42,000 ÷ £14 = 3,000 users), so as the user base grows the case for Model B strengthens. Understanding pricing structures like this is exactly the commercial perspective your role profile asks for when evaluating sourcing strategies.

#### Question 3 (easy) — Capacity utilisation

Your hosting platform has 480 virtual server instances of capacity. Current utilisation is 65%. A programme migration will add 96 instances of demand. What will utilisation be after migration?

1. 78%
2. 82%
3. 85%
4. 88%

**Correct answer: 3 (85%).**

**Explanation:** Current usage = 480 × 0.65 = 312 instances. After migration: 312 + 96 = 408 instances. Utilisation = 408 ÷ 480 = 0.85 = 85%. A common error is adding 96 to 480 (treating new demand as new capacity) or computing 96 ÷ 480 = 20% and adding it to 65% to get 85% — which happens to give the right answer here by a valid alternative route (because 96/480 genuinely is 20 percentage points of the same capacity base). Recognising when a shortcut is legitimate (same denominator) and when it is not (changed denominator) is precisely the judgement that separates fast-and-right from fast-and-wrong. As the architect advising on scalability, you would also note 85% utilisation is above most headroom thresholds — expect a follow-on question about that.

#### Question 4 (moderate) — Total cost of ownership over five years

You are comparing two options for a case-management capability over five years:

- Option 1 (SaaS): £220,000 per year subscription, £150,000 one-off implementation.
- Option 2 (rebuild): £900,000 one-off build, then £75,000 per year running costs from year 1.

What is the five-year total cost of each option, and which is cheaper?

1. SaaS £1.25m, rebuild £1.275m; SaaS cheaper.
2. SaaS £1.25m, rebuild £1.20m; rebuild cheaper.
3. SaaS £1.1m, rebuild £1.275m; SaaS cheaper.
4. SaaS £1.35m, rebuild £1.275m; rebuild cheaper.

**Correct answer: 1.**

**Explanation:** Option 1: (£220,000 × 5) + £150,000 = £1,100,000 + £150,000 = £1,250,000. Option 2: £900,000 + (£75,000 × 5) = £900,000 + £375,000 = £1,275,000. SaaS is cheaper by £25,000 over five years. Note how close the totals are: a competent architect's real answer would be "materially equivalent on cost — decide on other criteria such as flexibility, exit costs, and sustainability". Assessment questions, though, ask exactly what was computed. Distractor 2 forgets rebuild running costs run for all five years; distractor 3 omits the SaaS implementation fee; distractor 4 double-counts a year of subscription. The discipline is exhaustively listing every cost line before summing — the same discipline you apply when assuring business cases.

#### Question 5 (moderate) — Percentage change in run costs across transition states

Your target-state roadmap projects annual run costs falling across three transition states: current state £8.0m; transition state 1, a 15% reduction on current; transition state 2, a further 10% reduction on transition state 1. What is the annual run cost at transition state 2?

1. £6.00m
2. £6.12m
3. £6.40m
4. £5.95m

**Correct answer: 2 (£6.12m).**

**Explanation:** Transition state 1: £8.0m × (1 − 0.15) = £8.0m × 0.85 = £6.8m. Transition state 2: £6.8m × (1 − 0.10) = £6.8m × 0.90 = £6.12m. The classic trap is adding the percentages (15% + 10% = 25%) and computing £8.0m × 0.75 = £6.0m — distractor 1. Sequential percentage changes compound; they do not add, because the second reduction applies to a smaller base. When you own roadmaps "from a business, technology and data perspective, including 'as is', 'to be' and transitional states", compounding savings correctly across states is the difference between a credible benefits case and one that unravels at the investment board.

#### Question 6 (moderate) — Weighted option scoring

Your options appraisal weights three criteria: strategic alignment 50%, cost 30%, delivery risk 20%. Two options score out of 10 on each criterion:

- Option A: alignment 8, cost 5, risk 6.
- Option B: alignment 6, cost 9, risk 7.

Which option wins, and with what weighted score?

1. Option A, with 6.7
2. Option B, with 7.1
3. Option A, with 7.1
4. Option B, with 6.7

**Correct answer: 2 (Option B, with 7.1).**

**Explanation:** Option A: (8 × 0.5) + (5 × 0.3) + (6 × 0.2) = 4.0 + 1.5 + 1.2 = 6.7. Option B: (6 × 0.5) + (9 × 0.3) + (7 × 0.2) = 3.0 + 2.7 + 1.4 = 7.1. Comparing: 7.1 > 6.7, so Option B wins under the stated weightings, despite Option A's stronger strategic alignment. This question is constructed to catch a specific error: computing both scores correctly and then selecting the option you intuitively prefer (the strategically aligned one) rather than the one the weighted model actually favours. In weighted scoring, the model's answer is the model's answer; if you believe strategic alignment deserves more weight, the professional move is to challenge the weightings openly at governance — not to misreport the calculation. Show the arithmetic, then have the argument about the weights.

#### Question 7 (moderate) — Ratio reasoning for team capacity

Your architecture community has 6 enterprise-level architects, 15 solution architects and 24 technical architects. Best practice in your organisation suggests a support ratio of no more than 1 enterprise-level architect to 8 other architects. Is the current ratio within tolerance, and what is it?

1. Yes; the ratio is 1 to 6.5
2. Yes; the ratio is 1 to 8
3. No; the ratio is 1 to 9.75
4. No; the ratio is 1 to 13

**Correct answer: 1 (yes; 1 to 6.5).**

**Explanation:** Other architects = 15 + 24 = 39. Ratio = 39 ÷ 6 = 6.5, i.e. 1 enterprise architect to 6.5 others — comfortably inside the 1-to-8 tolerance. Distractor 4 comes from dividing only the technical architects incorrectly or dividing 39 by 3; distractor 3 arises from including the enterprise architects themselves in the numerator (45 ÷ 6 = 7.5) or other slips. The care point is defining the ratio's terms precisely before dividing: "other architects" excludes the six themselves. Workforce ratios like this appear regularly when you develop the architecture community and advise on team makeup — and in tests, definitional precision is where marks are won.

#### Question 8 (moderate) — Reading a portfolio RAG table

Your quarterly portfolio report shows programme statuses across two quarters:

| Status | Q1 programmes | Q2 programmes |
|---|---|---|
| Green | 18 | 15 |
| Amber | 9 | 14 |
| Red | 3 | 4 |
| Total | 30 | 33 |

Which statement is accurate?

1. The proportion of Green programmes fell from 60% to about 45%.
2. The number of Green programmes fell by 20%, so portfolio health fell 20%.
3. Red programmes grew by 1 percentage point.
4. Amber programmes rose by 5 percentage points of the portfolio.

**Correct answer: 1.**

**Explanation:** Q1 Green proportion: 18 ÷ 30 = 60%. Q2 Green proportion: 15 ÷ 33 = 0.4545… ≈ 45%. Statement 1 is exactly right. Statement 2 mixes a count change (18 → 15 is a 16.7% fall, not 20%) with an unjustified leap to "portfolio health". Statement 3 confuses counts with percentage points: Red went from 3 ÷ 30 = 10% to 4 ÷ 33 ≈ 12.1%, a rise of about 2.1 percentage points, not 1. Statement 4: Amber went from 9 ÷ 30 = 30% to 14 ÷ 33 ≈ 42.4%, a rise of about 12.4 percentage points, not 5. The trap throughout is that the denominator changed (30 → 33). Whenever totals shift between periods, convert to proportions before comparing — a habit that will serve you every time you take a strategic view across portfolios and programmes.

#### Question 9 (challenging) — Expected cost of risk

Two architectural options carry different risk exposures:

- Option 1: 10% probability of a £1.2m integration failure; 20% probability of a £300,000 delay cost.
- Option 2: 45% probability of a £200,000 rework cost; 5% probability of a £2.0m contract penalty.

Using expected value, which option carries the lower expected risk cost, and what is it?

1. Option 1, at £180,000
2. Option 2, at £190,000
3. Option 1, at £150,000
4. Option 2, at £100,000

**Correct answer: 1 (Option 1, at £180,000).**

**Explanation:** Option 1 expected cost: (0.10 × £1,200,000) + (0.20 × £300,000) = £120,000 + £60,000 = £180,000. Option 2 expected cost: (0.45 × £200,000) + (0.05 × £2,000,000) = £90,000 + £100,000 = £190,000. Option 1 is lower by £10,000. Distractor 3 (£150,000) comes from taking 10% of £1.2m plus 10% of £300,000 — applying one probability to both impacts; distractor 4 counts only Option 2's penalty term and forgets the rework line. Notice how close the two expected values are, and how different the shapes of risk: Option 2's £2.0m worst case dwarfs Option 1's £1.2m. The lesson for making architectural decisions with managed risk is that expected value summarises risk but conceals tail exposure — two similar expected costs can hide very different worst cases, which is why governance boards rightly ask for both figures before endorsing a decision.

#### Question 10 (challenging) — Cloud consumption growth

A data platform's monthly cloud cost is £40,000 and is growing at 5% per month compound. If nothing changes, approximately what will the monthly cost be in 12 months, and what is the approximate percentage increase?

1. £64,000; about 60%
2. £72,000; about 80%
3. £66,000; about 66%
4. £62,000; about 55%

**Correct answer: 2 (about £72,000; about 80%).**

**Explanation:** Compound growth: £40,000 × (1.05)^12. Compute (1.05)^12 ≈ 1.796. So £40,000 × 1.796 ≈ £71,800 ≈ £72,000 — an increase of roughly 80%. The headline trap is linear thinking: 5% × 12 = 60%, giving distractor 1 (£64,000). Compounding at 5% monthly nearly doubles a cost in a year — this is why consumption-based commercial models need active architectural management, and why your sustainability and scalability recommendations must distinguish linear from compound growth. If you cannot compute powers quickly, use the doubling heuristic: at 5% per period, doubling takes about 14 periods (rule of 70: 70 ÷ 5 = 14), so 12 months lands just short of doubling — enough to select 80% over 60% with confidence.

#### Question 11 (challenging) — Benefits realisation check

A business case claims: "The consolidation programme costs £3.6m and delivers £1.1m per year of savings from year 2 onwards (no savings in year 1). Therefore the programme pays back within three years." Is the payback claim correct?

1. Yes — savings of £3.3m by end of year 3 exceed cost when rounded.
2. No — by end of year 3 cumulative savings are £2.2m, well short of £3.6m; payback actually occurs during year 5.
3. Yes — £1.1m × 3 = £3.3m plus interest covers it.
4. No — payback occurs in year 4 exactly.

**Correct answer: 2.**

**Explanation:** Savings start in year 2. Cumulative savings: end of year 1 = £0; end of year 2 = £1.1m; end of year 3 = £2.2m; end of year 4 = £3.3m; end of year 5 = £4.4m. The £3.6m cost is recovered during year 5 (between £3.3m and £4.4m cumulative — specifically after about 3.3 months of year 5, since £0.3m ÷ £1.1m ≈ 0.27 of a year). The claim's error is assuming savings flow from year 1. Distractor 1 makes exactly that mistake and then waves it through with "rounded". Checking whether a benefits profile supports its own payback claim — including when benefits actually start — is a routine assurance task when you guide the organisation towards value-for-money decisions, and assessments love it because the arithmetic is simple but the reading must be exact.

#### Question 12 (challenging) — Sustainability metrics

Your hosting estate consumes 1,600 MWh per year. A migration plan moves 45% of workloads to a cloud region whose effective energy per workload is 30% lower than your current estate. Assuming energy use scales with workload share, what is the estate's total annual consumption after migration?

1. 1,384 MWh
2. 1,120 MWh
3. 1,264 MWh
4. 1,456 MWh

**Correct answer: 1 (1,384 MWh).**

**Explanation:** Split the estate. Workloads staying put: 55% × 1,600 = 880 MWh, unchanged. Workloads migrating: 45% × 1,600 = 720 MWh of current consumption, reduced by 30%: 720 × 0.70 = 504 MWh. Total after migration: 880 + 504 = 1,384 MWh. Distractor 2 applies the 30% reduction to the whole estate (1,600 × 0.70 = 1,120). Distractor 3 subtracts 30% of the migrated share from the wrong base. The method — partition, transform the affected partition only, recombine — is the standard pattern for estate-level questions, and it is exactly how you would quantify a sustainability recommendation in a real roadmap: savings apply only to the workloads that actually move.

#### Question 13 (challenging) — Multi-step budget allocation

Your annual architecture budget is £2.5m. Governance rules require: at least 40% on strategic change initiatives; exactly 12% on community development and training; and no more than 20% on external consultancy. This year, consultancy is at its maximum and community development takes its exact allocation. What is the maximum remaining amount available for operational architecture work if strategic change takes its minimum?

1. £700,000
2. £600,000
3. £800,000
4. £550,000

**Correct answer: 1 (£700,000).**

**Explanation:** Work through each allocation: strategic change minimum = 40% × £2.5m = £1.0m. Community development = 12% × £2.5m = £300,000. Consultancy maximum = 20% × £2.5m = £500,000. Committed so far: £1.0m + £0.3m + £0.5m = £1.8m. Remaining for operational work: £2.5m − £1.8m = £700,000. The question demands careful tracking of "at least", "exactly" and "no more than": to maximise the remainder, the "at least" item is set to its floor, and the "no more than" item — stated as being at its maximum — is fixed at its ceiling. Constraint words are doing all the work, exactly as they do in real budget discussions with finance colleagues, where your commercial perspective and precision with allocation rules protect the operational capacity your teams depend on.

#### Question 14 (moderate) — Comparing sourcing day rates

You are advising on sourcing for an eighteen-month architecture workstream requiring the equivalent of 2 full-time architects. Options:

- Option 1 (contractors): day rate £750 per architect, working 220 days per architect per year.
- Option 2 (consultancy): fixed price £700,000 for the whole workstream.
- Option 3 (permanent hires): £95,000 per architect per year total employment cost, plus a one-off recruitment cost of £15,000 per architect.

What is the total cost of each option over the eighteen months, and which is cheapest?

1. Contractors £495,000; consultancy £700,000; permanent £315,000 — permanent cheapest.
2. Contractors £990,000; consultancy £700,000; permanent £315,000 — permanent cheapest.
3. Contractors £495,000; consultancy £700,000; permanent £285,000 — permanent cheapest.
4. Contractors £990,000; consultancy £700,000; permanent £600,000 — permanent cheapest.

**Correct answer: 1.**

**Explanation:** Work each option over 18 months (1.5 years) for 2 architects. Contractors: £750 × 220 days = £165,000 per architect per year; for 2 architects over 1.5 years: £165,000 × 2 × 1.5 = £495,000. Consultancy: £700,000 fixed, no scaling needed. Permanent: annual employment cost £95,000 × 2 × 1.5 = £285,000, plus recruitment £15,000 × 2 = £30,000, giving £315,000. Comparing: £315,000 < £495,000 < £700,000, so permanent hires are cheapest. Distractor 2 doubles the contractor figure by applying the 2-architect multiplier twice; distractor 3 forgets the recruitment cost; distractor 4 miscomputes the permanent salary line. The reliable method is a small grid — option by option, cost line by cost line, each multiplied by the correct headcount and duration exactly once. Note also what the numbers alone do not decide: an 18-month workstream may not justify permanent posts if the need then disappears, contractors carry engagement-rule and knowledge-retention considerations, and the consultancy price may include deliverable risk transfer. Understanding when each sourcing strategy applies — not just which is cheapest — is the commercial perspective your role profile names; the arithmetic is the entry ticket to that conversation.

### Preparation tips

- **Rebuild your fluency with percentages, ratios and compounding.** These three operations cover the vast majority of numeric questions at this level. Ten minutes a day recomputing percentage changes, reversing percentages, and compounding growth will pay off quickly.
- **Practise on real financial artefacts.** Take a genuine business case, licensing schedule or cloud billing report and quiz yourself: what is the five-year TCO? Where is the break-even point? What is the compound growth rate? Familiarity with your own domain's numbers makes test data feel routine.
- **Always identify the denominator.** Before computing any proportion, say to yourself: "out of what?" Changed denominators (Question 8) and partitioned bases (Question 12) are the two most reliable traps at senior level.
- **Use the answer options.** Options tell you the required precision and can reveal an extraction error: if your figure is not close to any option, re-read the table before recalculating.
- **Estimate first, then compute.** A ten-second estimate (rule of 70, rounding to friendly numbers) catches order-of-magnitude errors and helps you reject distractors instantly.
- **Keep calm about the calculator.** It is normally provided. The test is measuring interpretation, not arithmetic heroics — and as a senior professional you already interpret numbers like these weekly.

### Common pitfalls

- **Misreading scale qualifiers.** Confusing "£ thousands" with "£ millions", or monthly with annual figures — the classic pitfall the assessment literature flags. Portfolio tables mix scales deliberately.
- **Adding sequential percentages.** Two successive reductions of 15% and 10% are not 25% (Question 5). Compounding errors are the most common senior-level mistake because the arithmetic looks beneath your dignity — until it isn't.
- **Grabbing intermediate values.** Distractors are frequently numbers you legitimately compute on the way to the answer (Question 2). Finish the question before choosing.
- **Over-calculating.** Performing an exact power calculation when the rule of 70 or a rounded estimate would identify the correct option in a fraction of the time.
- **Time-sink questions.** One brutal multi-stage question can consume five easier questions' worth of time. Bank the accessible marks first; return if time allows.
- **Forgetting the question's units or timeframe.** Computing an annual figure when the question asks monthly, or a total when it asks a difference. Re-read the final sentence of the stem before answering.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment evaluates how well you understand, analyse, and draw correct conclusions from written business information. It mirrors the exact reading demands of your role: dense strategy papers, architecture principles, government technology standards, governance board minutes, supplier correspondence and policy documents. The defining discipline is fact-based logic — you must answer based strictly on the text provided, setting aside your own considerable professional knowledge.

Typical format and timing: you are given a passage of role-relevant text followed by a series of statements. For each statement you choose **True** (the passage logically supports it), **False** (the passage logically contradicts it), or **Cannot Say** (the passage provides insufficient information either way). Some tests add multiple-choice comprehension questions about the passage's main argument or a specific clause. Timing is tight — often less than a minute per question — to simulate workplace reading under deadline pressure.

Why does this matter for an enterprise architect? Your role profile puts communication at its heart: you lead the communication of complicated, complex or risky architecture topics with technical and non-technical stakeholders, and you establish architectural principles, policies and standards — documents whose exact wording carries obligations. Misreading "should" as "must", or treating an implication as a statement, has real consequences: a governance decision built on a misread standard, a stakeholder commitment inferred from an email that never made it, a principle applied beyond its stated scope. Verbal reasoning assessments measure precisely this precision. They also measure the flip side: the restraint not to import outside knowledge. As an experienced architect you often know more than the passage says — the test rewards those who can quarantine that knowledge and reason only from the text, exactly as you must when assuring that a decision matches what a standard actually requires rather than what everyone assumes it requires.

### What it measures for your role

- **Architecture communication**: leading communication of complex topics starts with receiving text accurately. The True/False/Cannot Say format directly measures whether you extract what a document actually commits to — essential when you manage stakeholder expectations based on written positions.
- **Establishing principles, policies and standards**: these artefacts are legal-adjacent texts where "must", "should", "may", and "without exemption" each carry distinct force. Expect passages written in standards language, testing whether you track modal verbs and scope clauses.
- **Making architectural decisions** and **architectural governance**: decision records and board minutes must be read for what was decided versus what was discussed. Passages will mix decisions, options and opinions, and statements will probe whether you kept them separate.
- **Commercial perspective**: supplier letters and contract extracts test whether you can identify obligations, conditions and exclusions — the reading skill underlying sourcing strategy.
- **Architect for the whole context** and **horizon scanning**: analytical passages about industry trends test whether you distinguish the author's evidence from the author's speculation — the core skill of honest horizon scanning.

### Practice questions

For each passage, judge every statement strictly on the passage's wording. Your professional knowledge stays outside the room.

#### Passage A — Architecture principles extract

*"All new digital services must be designed in accordance with the organisation's published reference architectures. Where a reference architecture does not yet exist for a given domain, teams should consult the enterprise architecture function before selecting a design approach. Exemptions from published reference architectures may be granted only by the Design Authority, and each exemption must be recorded in the architecture decision log together with a remediation date. Exemptions are time-limited and lapse automatically at the remediation date unless renewed. The Design Authority meets fortnightly."*

#### Question 1 (easy)

Statement: Teams may grant themselves an exemption from a published reference architecture if they record it in the decision log.

1. True
2. False
3. Cannot Say

**Correct answer: 2 (False).**

**Explanation:** The passage states exemptions "may be granted only by the Design Authority". The word "only" excludes every other route, including self-granted exemptions — however well documented. Recording in the decision log is an additional requirement on granted exemptions, not an alternative granting mechanism. This is a direct contradiction of the passage, so the answer is False rather than Cannot Say. Notice how the distractor works: it takes a true fragment (exemptions must be recorded in the decision log) and welds it to a false one (teams granting themselves exemptions). Statements that are half-right are the workhorse of verbal reasoning tests — and of misread standards in real governance.

#### Question 2 (easy)

Statement: If no reference architecture exists for a domain, a team is required to consult the enterprise architecture function before selecting a design approach.

1. True
2. False
3. Cannot Say

**Correct answer: 3 (Cannot Say).**

**Explanation:** Look at the exact modal verb: teams "**should** consult" the enterprise architecture function. "Should" expresses a strong recommendation, not a requirement; the passage's mandatory language ("must") is used elsewhere, which shows the author distinguishes the two deliberately. The statement asserts a requirement ("is required to"), which the passage neither supports (it only recommends) nor flatly contradicts (it does not say consultation is optional in so many words). Under strict True/False/Cannot Say logic, a statement that overstates the modal force of the passage is generally treated as not supported — and because the passage does not directly contradict the existence of a requirement elsewhere, the safest strict answer is Cannot Say. In standards drafting, this must/should distinction is exactly the one you police when you establish architectural policies, and test writers exploit it constantly.

#### Question 3 (moderate)

Statement: An exemption that reaches its remediation date without renewal ceases to be valid.

1. True
2. False
3. Cannot Say

**Correct answer: 1 (True).**

**Explanation:** The passage says exemptions "are time-limited and lapse automatically at the remediation date unless renewed". "Lapse automatically" means the exemption ceases to have effect, and "unless renewed" is the only stated escape. The statement is a careful paraphrase — "ceases to be valid" for "lapse" — and paraphrase recognition is a core tested skill: True statements in these assessments rarely repeat the passage word for word. Verify each element: reaches remediation date (matches "at the remediation date"), without renewal (matches "unless renewed"), ceases to be valid (matches "lapse automatically"). All three map cleanly, so True.

#### Question 4 (moderate)

Statement: The Design Authority can grant an exemption within two weeks of a request.

1. True
2. False
3. Cannot Say

**Correct answer: 3 (Cannot Say).**

**Explanation:** The passage says the Design Authority "meets fortnightly", and it is tempting to compute: a fortnightly meeting cycle means a request waits at most two weeks for a meeting, so an exemption could be granted within two weeks. But the passage never says exemptions are granted at meetings, never says requests are decided at the first meeting after submission, and never mentions any service standard. The inference chain relies on assumptions imported from how governance boards usually work — your professional knowledge, not the text. The passage neither supports nor contradicts the statement, so Cannot Say. This is the single most important habit for verbal reasoning: identify where the passage's information ends and your own expertise begins, and answer only from the former.

#### Passage B — Governance board minutes extract

*"The board reviewed the options paper for the citizen identity capability. Option 2 (adopt the cross-government platform) was preferred by a majority of members on strategic alignment grounds, although the head of operations raised concerns about migration effort. The board agreed that a decision would be deferred until a revised cost model is presented at the next meeting. The chief data officer noted that, whichever option is chosen, the data migration approach must comply with the department's data residency policy. Action: architecture team to present the revised cost model within four weeks."*

#### Question 5 (moderate)

Statement: The board decided to adopt the cross-government platform.

1. True
2. False
3. Cannot Say

**Correct answer: 2 (False).**

**Explanation:** The passage explicitly says "the board agreed that a decision would be deferred until a revised cost model is presented". A deferral is a decision not to decide — which directly contradicts the claim that the board decided to adopt Option 2. The distractor's power comes from "Option 2 was preferred by a majority": preference expressed in discussion is not a decision minuted as such. Reading minutes for what was *decided* versus what was *discussed or preferred* is a precise skill you exercise in every governance and assurance engagement, and it is a favourite of test writers because the two are so easily conflated at speed.

#### Question 6 (moderate)

Statement: The head of operations opposed Option 2.

1. True
2. False
3. Cannot Say

**Correct answer: 3 (Cannot Say).**

**Explanation:** The head of operations "raised concerns about migration effort". Raising a concern is not opposition: one can prefer an option overall while flagging a risk within it, and the passage does not record how the head of operations voted or whether they were even in the majority that preferred Option 2. Equally, the passage does not say they supported it, so the statement cannot be marked False either. The information is simply insufficient — Cannot Say. Mapping stakeholders accurately ("concerned" is not "opposed"; "silent" is not "supportive") is central to managing stakeholder expectations effectively, and mislabelling a concerned stakeholder as an opponent is a real-world communication failure this question type deliberately probes.

#### Question 7 (challenging)

Statement: The data residency policy applies to the data migration approach only if Option 2 is chosen.

1. True
2. False
3. Cannot Say

**Correct answer: 2 (False).**

**Explanation:** The chief data officer's note is explicitly unconditional: "whichever option is chosen, the data migration approach must comply with the department's data residency policy". The statement tries to attach a condition ("only if Option 2 is chosen") to an obligation the passage states as applying in every case. "Whichever option is chosen" directly contradicts "only if Option 2" — so the answer is False, not Cannot Say. The technique for questions like this is to locate the scope phrase in the passage ("whichever option") and compare it against the scope phrase in the statement ("only if Option 2"); when they conflict head-on, the statement is False. Scope-narrowing distortions like this mirror a real risk in architectural work: a policy obligation quietly read down to apply only where convenient.

#### Passage C — Supplier letter extract

*"Further to our review of the hosting agreement, we confirm that the current per-instance pricing will be held until the end of the contract year. Thereafter, prices will be adjusted in line with our standard indexation clause. Please note that the enhanced support tier referenced in Schedule 4 is available only to customers who have completed migration to platform version 9. Customers who have not completed this migration by the end of the contract year will remain on the standard support tier, and we cannot guarantee extended maintenance windows for version 8 beyond that date."*

#### Question 8 (moderate)

Statement: Prices will increase at the end of the contract year.

1. True
2. False
3. Cannot Say

**Correct answer: 3 (Cannot Say).**

**Explanation:** The letter says prices "will be adjusted in line with our standard indexation clause". Adjustment under indexation is usually upward in practice — but the passage does not state the direction, and an indexation clause could in principle produce no change or even a decrease depending on the index. "Adjusted" is not "increased". Your commercial experience screams that supplier indexation means a rise; the test asks whether you can hold that knowledge apart from what the text commits to. This is exactly the discipline you need when summarising contractual positions for senior stakeholders: report what the supplier has actually committed to in writing, and flag your expectations separately as judgement.

#### Question 9 (moderate)

Statement: A customer still running platform version 8 at the end of the contract year will not receive the enhanced support tier at that point.

1. True
2. False
3. Cannot Say

**Correct answer: 1 (True).**

**Explanation:** Chain two stated facts. First: the enhanced tier "is available only to customers who have completed migration to platform version 9". Second: customers who have not completed migration by year end "will remain on the standard support tier". A customer still running version 8 at year end has, by definition, not completed migration to version 9, so both clauses independently place them outside the enhanced tier at that point. This is a supported deduction, not an assumption: every link uses the passage's own words. Contrast Question 8, where the deduction needed outside knowledge. Learning to feel that difference — a chain that closes inside the text versus one that needs an external link — is the highest-value verbal reasoning skill for anyone who reads contracts and standards professionally.

#### Question 10 (challenging)

Statement: The supplier guarantees extended maintenance windows for version 8 until the end of the contract year.

1. True
2. False
3. Cannot Say

**Correct answer: 3 (Cannot Say).**

**Explanation:** The passage says the supplier "cannot guarantee extended maintenance windows for version 8 **beyond** that date". This tells you about the period after the contract year end — nothing about the period before it. The statement asks about "until the end of the contract year", a period on which the passage is silent: it neither promises extended windows now nor withholds them now. The tempting inference — "if they can't guarantee it later, they must be providing it now" — is an implicature, not a statement; suppliers often deny future guarantees about things they never provided. Boundary words like "beyond", "thereafter", "from", and "until" define exactly which period a sentence governs; matching the statement's period to the passage's period is the whole question.

#### Passage D — Horizon-scanning briefing extract

*"Industry analysts project that by 2028 a majority of large public sector organisations will operate formal AI-assurance functions. Early adopters report that establishing such a function typically requires between twelve and eighteen months. Our own department currently has no dedicated AI-assurance capability, although the data governance team performs some overlapping activities. If the analysts' projection is accurate and the department wishes to be within the majority, preparatory work would need to begin no later than mid-2026. It should be noted that analyst projections in this area have historically overestimated adoption speed."*

#### Question 11 (challenging)

Statement: The department will need to establish an AI-assurance function by 2028.

1. True
2. False
3. Cannot Say

**Correct answer: 3 (Cannot Say).**

**Explanation:** The passage is built almost entirely of conditionals and projections: analysts *project* majority adoption; *if* the projection is accurate *and* the department *wishes* to be in the majority, *then* work must start by mid-2026. Nowhere does the passage state that the department must, will, or has decided to establish the function — the "need" in the statement only exists inside an unfulfilled conditional. Moreover, the final sentence actively undermines the projection's reliability. The statement is not contradicted (the department might well decide to do it), so not False; it is not supported as a fact, so not True. Cannot Say. Honest horizon scanning — a duty named in your role profile — lives exactly here: presenting trends and their conditions without letting a projection harden into a commitment.

#### Question 12 (challenging) — Multiple choice comprehension

Which of the following best describes the briefing's overall treatment of the analysts' projection?

1. It endorses the projection and recommends immediate action.
2. It reports the projection, derives a conditional deadline from it, and explicitly flags the projection's historical unreliability.
3. It rejects the projection on the grounds of past overestimates.
4. It presents the projection as the department's official planning assumption.

**Correct answer: 2.**

**Explanation:** Walk the passage's moves: it reports what analysts project; it derives a timeline consequence ("preparatory work would need to begin no later than mid-2026") that is explicitly conditional ("if the analysts' projection is accurate and the department wishes..."); and it closes by noting the projections "have historically overestimated adoption speed". That is precisely option 2. Option 1 fails because nothing is endorsed and no recommendation is made — a conditional is not advice. Option 3 overreads the caveat: flagging unreliability is not rejection. Option 4 invents a status ("official planning assumption") the passage never assigns. Main-purpose questions reward mapping the passage's structure — claim, condition, caveat — rather than reacting to its most memorable sentence.

#### Question 13 (moderate)

Statement: The department currently performs no activities related to AI assurance.

1. True
2. False
3. Cannot Say

**Correct answer: 2 (False).**

**Explanation:** The passage concedes that "the data governance team performs some overlapping activities" even though there is "no dedicated AI-assurance capability". The statement's word "no activities" is an absolute, and the passage directly contradicts it with "some overlapping activities". Watch the two different claims: no *dedicated capability* (supported) versus no *activities at all* (contradicted). Absolutes — "no", "all", "none", "always" — make statements easy to falsify with a single counterexample from the text, and test writers rely on candidates blurring "no dedicated function" into "nothing happening". In your own communications, this is the same precision that stops a capability-gap message ("we lack a dedicated function") being heard as an unfair criticism ("the organisation is doing nothing").

#### Question 14 (challenging)

Statement: According to the passage, if the department starts preparatory work in early 2027, it cannot be among the majority of large public sector organisations operating formal AI-assurance functions by 2028.

1. True
2. False
3. Cannot Say

**Correct answer: 3 (Cannot Say).**

**Explanation:** Two pieces of the passage's own vagueness block any categorical conclusion. First, "typically requires between twelve and eighteen months" describes the usual case, not a hard bound — the passage does not exclude faster (or slower) establishment. Second, the passage never states which point in 2028 the projection refers to: an early-2027 start leaves up to 24 months before the end of 2028, comfortably longer than the typical maximum, yet the passage's own mid-2026 deadline implies its authors were measuring to some earlier, unstated point in 2028. Because the passage neither fixes the 2028 reference point nor makes twelve-to-eighteen months an absolute limit, the categorical "cannot" is neither supported nor contradicted — Cannot Say. Questions like this reward slowing down exactly when an arithmetic shortcut feels decisive: the missing fact (which point in 2028?) matters more than the calculation, just as the unstated assumption in a business case often matters more than its spreadsheet.

#### Question 15 (moderate) — Multiple choice comprehension on Passage A

Looking back at Passage A (the architecture principles extract), which of the following most accurately summarises the exemption regime it establishes?

1. Exemptions are granted by the Design Authority, recorded with a remediation date in the decision log, and expire at that date unless renewed.
2. Exemptions are granted by the enterprise architecture function after consultation, and reviewed fortnightly.
3. Exemptions are permanent once recorded in the architecture decision log.
4. Exemptions are available only for domains where no reference architecture exists.

**Correct answer: 1.**

**Explanation:** Option 1 assembles the three stated elements of the regime accurately: the sole granting body ("only by the Design Authority"), the recording requirement ("recorded in the architecture decision log together with a remediation date"), and the time limit ("lapse automatically at the remediation date unless renewed"). Option 2 misattributes the granting power to the enterprise architecture function — whose stated role is pre-design consultation where no reference architecture exists — and misapplies the fortnightly cadence, which describes meetings, not reviews of exemptions. Option 3 contradicts "time-limited" and "lapse automatically". Option 4 inverts the passage's logic: exemptions apply to *published* reference architectures; where none exists there is nothing to be exempt from, and a different rule (consultation) applies. Summary questions like this reward reassembling scattered clauses into a whole — the same synthesis you perform when you brief a board on what a standard actually requires, rather than reading it aloud clause by clause.

### Preparation tips

- **Train the Cannot Say reflex.** Most candidates — especially experienced professionals — err towards True or False because they know the subject matter. Practise asking one question: "Where in the passage is this stated or contradicted?" If you cannot point to the words, the answer is Cannot Say.
- **Read modal verbs like a standards author.** You already write principles and policies; bring that drafting eye to reading. Highlight (mentally) every "must", "should", "may", "only", "unless" and "beyond" — in this test they are the whole game.
- **Separate decisions from discussion.** When a passage is minutes or a decision record, note what was decided, what was preferred, what was raised, and what was actioned. Statements will probe the boundaries between them.
- **Match time periods and scopes exactly.** Before answering, check that the statement's timeframe, population and condition are the same as the passage's. "Beyond the contract year" is not "during the contract year"; "whichever option" is not "only Option 2".
- **Practise on your own documents.** Take a government technology standard, a supplier letter or a set of board minutes, write five True/False/Cannot Say statements about it, then defend each answer from the text alone. This doubles as excellent preparation for governance and assurance discussions.
- **Pace yourself with the statement, not the passage.** Skim the passage once for structure, then work statement by statement, returning to the exact sentence each statement touches. Reading the passage exhaustively first is the classic time-management error.

### Common pitfalls

- **Importing professional knowledge.** The most common failure for senior candidates: you know how indexation clauses, governance boards and analyst projections behave in real life, and that knowledge quietly fills the passage's gaps. Answer from the text alone.
- **Treating likely outcomes as facts.** A projection, preference or typical duration in the passage is not an absolute — confusing "likely" or "typically" with "will" turns Cannot Say answers into wrong True answers.
- **Half-right statements.** Distractors weld a true fragment to a false one (Question 1). Verify every clause of the statement, not just the recognisable part.
- **Absolutes and quantifiers.** "No activities", "all services", "always" — absolutes are falsified by a single textual counterexample, and supported only by equally absolute passage wording.
- **Boundary-word blindness.** "Beyond", "thereafter", "until", "from", "only", "unless" define the scope of every obligation. Misreading one boundary word flips an answer.
- **Poor time allocation.** Spending too long on a full first read of the passage instead of scanning for the sentence each statement targets — the pitfall the assessment literature flags most often for verbal tests.

## Workplace job-specific situational judgement assessment

### About this assessment

A workplace job-specific situational judgement assessment evaluates your decision-making, interpersonal skill and professional conduct through realistic workplace dilemmas. Unlike logic or numeric tests, there is often no single objectively right answer: several responses may seem reasonable, but one aligns best with the organisation's values and the demands of your role. For an enterprise architect in UK government, that alignment means the values of the public sector digital profession: user needs first, transparency, collaboration across boundaries, accessibility and inclusion, and stewardship of public money.

Typical format and timing: each item presents a short scenario — a conflict, an ethical dilemma, or an operational challenge — followed by three to five possible responses. You are usually asked to select the **most effective** and **least effective** actions, or to rank or rate every option from best to worst. Timing is generous or absent: the test measures your natural judgement, not your speed. Scoring compares your choices with those of experienced practitioners and with the organisation's competency framework.

Why does this matter for your role? Enterprise architecture is judged less by artefacts than by influence. Your role profile is explicit: you lead and influence cross-cutting change, consult and support collaboration across the business, communicate complicated and risky topics to senior stakeholders, develop the architecture community, and guide the organisation's decisions through governance rather than authority. Nearly every one of those duties is a judgement call about people, timing, escalation and candour. A situational judgement assessment simply compresses those calls into scenarios: a director bypassing governance, a supplier pressuring a decision, an architect community losing faith, a delivery team about to breach a principle for a deadline. How you choose to act — and what you choose never to do — reveals how you will actually operate in the role.

### What it measures for your role

- **Architecture communication**: scenarios test whether you adapt your message to your audience, manage expectations honestly, and advocate for teams to senior stakeholders without burning trust.
- **Community collaboration**: expect dilemmas about motivating architects, handling conflict within the community, contributing to others' work and creating the right team environment.
- **Making architectural decisions** and governance: scenarios probe whether you escalate through the right channels, keep decisions transparent, and balance pace against managed risk.
- **Architect for the whole context**: dilemmas will pit your immediate programme's interests against wider organisational objectives, testing whether you act on the bigger picture and influence colleagues across the organisation.
- **Commercial perspective**: supplier and sourcing scenarios test propriety, fairness and value for money under commercial pressure.
- **Strategy design** and **problem definition**: scenarios test whether you challenge requirements and assumptions constructively, and resist solutionising before the problem is framed.

### Practice questions

For each scenario, decide your answer before reading the commentary. The suggested "most effective / least effective" choices reflect UK public sector values — user needs, transparency, collaboration, accessibility and inclusion — and the collaborative, governance-based way enterprise architects exercise influence.

#### Question 1 (moderate) — The director who bypasses governance

A programme director tells you they intend to sign a contract for a new case-management platform next week. The option was never brought to the Design Authority, and it conflicts with the enterprise roadmap's commitment to the shared platform. The director says: "Governance is too slow, and my programme carries the delivery risk, not yours."

Possible actions:

- A: Escalate immediately to the director's superior, copying the governance board, stating the contract must not be signed.
- B: Meet the director promptly to understand their drivers and constraints, explain the specific risks and duplicated costs, and offer a fast-track Design Authority review before signature.
- C: Let the contract proceed — the director owns the delivery risk — but record your objection in the decision log.
- D: Ask a solution architect on the programme to quietly delay the procurement paperwork until the next Design Authority meeting.

**Most effective: B. Least effective: D.**

**Explanation:** B does three things a strong enterprise architect does instinctively: it seeks the stakeholder's real drivers first (the director's pace concern is legitimate), it communicates the risk in terms the director cares about (cost duplication, delivery risk), and it removes the stated obstacle by offering a fast-track review — collaboration plus governance, at pace. A is premature: escalation is a legitimate tool, but as a first move it spends trust you will need for years and signals that architecture governs by force rather than influence; it becomes appropriate only if engagement fails. C abdicates: enterprise risks (roadmap conflict, duplicated spend) are not transferable to one programme's risk register, and a logged objection protects you, not the organisation. D is the least effective by a wide margin: covert manipulation through a junior colleague is a transparency failure, puts that colleague in an impossible position, and destroys the credibility on which all your future influence depends. In public sector values terms, D fails transparency and collaboration simultaneously.

#### Question 2 (moderate) — The deadline versus the accessibility standard

A flagship service is two weeks from a heavily publicised launch. The delivery team asks you to endorse deferring fixes for known accessibility failures until "a fast-follow release six weeks after launch", noting that ministers expect the launch date to hold.

Possible actions:

- A: Endorse the deferral — the political commitment to the date outweighs a six-week delay to fixes.
- B: Refuse to endorse, and state that accessibility is a legal and values-based obligation; work with the team to assess the failures' severity, explore what can be fixed pre-launch, and ensure any residual risk is escalated transparently to the service owner and senior responsible officer for an informed decision.
- C: Tell the team accessibility is not the architect's concern and direct them to the standards team.
- D: Publicly oppose the launch in the programme's all-hands meeting to force the issue.

**Most effective: B. Least effective: C.**

**Explanation:** B treats accessibility as what it is in UK government: a legal duty and a core inclusion value, not a nice-to-have — while still engaging with delivery reality. It distinguishes severity (some failures may genuinely be minor; others may exclude users outright), maximises what is fixed before launch, and routes the residual decision — with full information — to the accountable owners rather than taking or dodging it alone. That is transparency and managed risk in action. A rubber-stamps exclusion of users to protect a date, inverting user needs and inclusion values. D uses a public forum to win by embarrassment; it may even succeed once, but it poisons collaboration and treats colleagues as adversaries. C is least effective because it is both wrong on the role — an enterprise architect who owns standards cannot disown a standard's application — and wrong on behaviour: it abandons the team at the moment they asked for help, failing collaboration and community obligations at once.

#### Question 3 (challenging) — The strategically misaligned quick win

A senior stakeholder you have been cultivating for months finally offers enthusiastic sponsorship — for a data-platform initiative that duplicates a cross-government capability your roadmap commits to adopting next year. Accepting would deliver visible value quickly and cement the relationship; declining risks the stakeholder's disengagement.

Possible actions:

- A: Accept the sponsorship and quietly deprioritise the cross-government adoption.
- B: Decline outright, citing the roadmap, and copy the strategy board.
- C: Use the stakeholder's enthusiasm as an opening: propose shaping their initiative into an early-adopter pilot of the cross-government capability, giving them visible value and first-mover influence while keeping strategic alignment.
- D: Accept the sponsorship for now, intending to redirect the initiative later once the relationship is secure.

**Most effective: C. Least effective: D.**

**Explanation:** C is the distinctly senior move: it refuses the false choice between the relationship and the strategy. By redirecting the stakeholder's energy into an early-adopter role, it preserves value for money (no duplication), advances the roadmap ahead of schedule, and gives the stakeholder something better than what they asked for — influence and visibility. This is what "lead and influence the delivery of cross-cutting capabilities" looks like in practice. B protects the strategy but wastes the relationship and the energy behind it; copying the strategy board converts a conversation into a confrontation. A trades the enterprise position for a local win — the exact failure mode "architect for the whole context" warns against. D is least effective because it is A plus deception: accepting sponsorship while privately intending to redirect it later manages the stakeholder by misdirection, and when they discover it — they always do — the trust cost exceeds anything B would have incurred honestly.

#### Question 4 (moderate) — The struggling architecture community

Attendance at your architecture community of practice has halved over six months. A trusted colleague tells you privately: "People stopped coming because it became a broadcast channel — an hour of enterprise team slides, no discussion, nothing they can use."

Possible actions:

- A: Make attendance mandatory for all architects and track it.
- B: Redesign the community with its members: ask what they need, rotate ownership of sessions across domains and teams, shift the format towards working sessions on real problems, and keep any enterprise broadcast to a brief slot.
- C: Cancel the community of practice and replace it with a monthly newsletter.
- D: Continue as is, but improve the slide quality and invite more senior speakers.

**Most effective: B. Least effective: A.**

**Explanation:** Your role profile makes you responsible for developing the architecture community, and the skill definition is explicit about motivating and empowering teams and creating the right environment. B does exactly that: it treats community members as owners rather than audience, responds directly to the diagnosed problem (broadcast format, no practical value), and redistributes ownership — which is how communities generate energy. D treats the symptom as a production-values problem when the diagnosis says participation is the problem; better slides in a broadcast format is more of what killed attendance. C abandons the capability rather than fixing it, losing the collaboration and cross-pollination a community exists to create. A is least effective because compulsion is the opposite of motivation: mandated attendance fills the room while emptying it of engagement, signals that the community serves the enterprise team rather than its members, and converts a leadership failure into a compliance exercise. People can be required to attend; they cannot be required to collaborate.

#### Question 5 (challenging) — The supplier's exclusive briefing

A strategic supplier invites you to an exclusive executive briefing at their headquarters, with hospitality, shortly before your organisation begins a procurement in which the supplier will likely bid. The briefing content — their technology roadmap — would genuinely inform your horizon scanning.

Possible actions:

- A: Attend privately without telling anyone, since the content is professionally useful.
- B: Decline the exclusive event; instead, consult your commercial team about propriety rules, and request the roadmap content through a channel open on equal terms to other suppliers, with hospitality declined or declared per policy.
- C: Attend, but pay for your own travel so no hospitality is received.
- D: Decline and inform the supplier they should not contact architects during procurement periods.

**Most effective: B. Least effective: A.**

**Explanation:** This scenario tests commercial perspective — knowing the processes and the appropriate internal contacts — under a genuinely tempting professional justification. B gets every element right: it recognises the procurement context makes exclusive access a fairness and propriety risk; it uses the right internal contact (the commercial team) rather than improvising; and it still pursues the legitimate horizon-scanning value through an equal-access channel. C misunderstands the problem: self-funded travel addresses the hospitality rule but not the deeper issue of privileged access and perceived bias on the eve of procurement. D overcorrects into rudeness and overstates the rule — supplier engagement is not prohibited; unmanaged, exclusive, pre-procurement engagement is the risk — and it burns a relationship the organisation may need. A is least effective: attending covertly compounds the propriety risk with concealment, and in a subsequent procurement challenge, an undisclosed exclusive briefing with hospitality could taint the entire process. When a professional benefit tempts you towards an impropriety, the senior answer is to find the compliant route to the same benefit.

#### Question 6 (moderate) — The principle you no longer believe in

While preparing guidance, you conclude that one of the architectural principles you helped establish two years ago — mandating a specific integration pattern — is now outdated and is pushing teams towards worse designs. Three programmes are currently being held to it.

Possible actions:

- A: Keep enforcing the principle uniformly; changing it now would undermine the authority of all principles.
- B: Quietly stop enforcing it and let teams do what makes sense case by case.
- C: Bring an evidence-based revision proposal to the Design Authority promptly; meanwhile, be transparent with the three affected programmes that a revision is under consideration, and use the existing exemption process where the current principle demonstrably harms their design.
- D: Update the principle yourself immediately — you wrote it, and you own the principles catalogue.

**Most effective: C. Least effective: B.**

**Explanation:** Principles govern only while they are both authoritative and credible, and this scenario pits those qualities against each other. C preserves both: the revision goes through governance (authority intact), the change is argued from evidence (credibility intact), affected programmes get honesty about the direction of travel, and the existing exemption mechanism — not private discretion — handles urgent cases. This is "establish architectural principles, policies and standards" done as stewardship rather than possession. A mistakes rigidity for authority: enforcing a principle you know causes harm converts governance into dogma and quietly teaches teams that principles are obstacles, not aids. D bypasses the very governance that gives the catalogue its legitimacy; individual ownership of shared standards ends exactly where enterprise adoption begins. B is least effective because selective, unannounced non-enforcement is the worst of every world: the principle still officially binds anyone who reads it, enforcement becomes arbitrary and personal, and the decision log no longer reflects reality — a transparency failure that undermines every other principle too.

#### Question 7 (challenging) — Two domains, one budget

The data architecture and security architecture domains both submit compelling bids for the same limited capability-improvement budget. Each domain lead lobbies you separately, and both hint that losing the funding will be seen as a signal about how much the enterprise function values their domain.

Possible actions:

- A: Split the budget evenly to keep both leads onside.
- B: Fund the bid whose lead you judge more likely to escalate if refused.
- C: Assess both bids against the enterprise strategy's stated priorities and published investment criteria, decide transparently, share the reasoning with both leads together, and work with the unfunded lead on a realistic path for their bid in the next cycle.
- D: Defer the decision to the next quarter to avoid the conflict.

**Most effective: C. Least effective: B.**

**Explanation:** C treats an emotionally loaded decision as what it should be: a transparent application of agreed criteria. Deciding against published priorities gives both leads something better than a win — a process they can trust and plan around — and handling the unfunded domain with a forward path turns a loss into a deferral with dignity. Sharing reasoning with both leads together kills the corridor-lobbying dynamic. A feels collaborative but often funds two half-capabilities instead of one whole one; if the criteria genuinely favour one bid, splitting is a values failure dressed as fairness (and if they don't, C would reveal that too). D converts a hard decision into a slow one; both domains stall and the lobbying intensifies. B is least effective because it replaces strategy with fear: rewarding anticipated escalation teaches every stakeholder that escalation works, institutionalising exactly the behaviour that makes enterprise prioritisation impossible. Value for money and transparency both demand that the loudest voice and the best bid be different questions.

#### Question 8 (moderate) — The junior architect's flawed proposal

A promising solution architect, presenting to the architecture community for the first time, shows a design that contains a significant flaw: it stores citizen data in a way that will breach the data residency policy. Several community members have noticed and are exchanging glances. The architect is visibly nervous.

Possible actions:

- A: Point out the breach immediately and thoroughly, so the community sees that standards are taken seriously.
- B: Say nothing in the session to spare them embarrassment, and email their line manager about the flaw afterwards.
- C: Ask an open question in the session that steers attention to the data residency aspect ("How does the design handle residency requirements for the citizen data store?"), let the architect engage with it, and follow up afterwards with supportive, specific guidance.
- D: Take over the presentation and explain how the design should be corrected.

**Most effective: C. Least effective: B.**

**Explanation:** This is community collaboration and communication in one scenario: a compliance issue that must be surfaced, inside a person and environment you are responsible for developing. C surfaces the flaw in the session — it cannot be left standing, since the community would otherwise learn that a policy breach passed review — but does so as a question the architect can engage with, preserving their standing and modelling how architects challenge each other. The private follow-up converts the moment into development. A gets the compliance right and the environment wrong: a thorough public correction of a nervous first-time presenter teaches the community that presenting is dangerous, and attendance problems follow. D rescues the design while erasing the designer — efficient, humiliating, and a lost learning opportunity. B is least effective because it fails on every axis: the flaw goes unchallenged in front of the community (compliance failure), the architect learns nothing in the moment, and the first they hear of it is via their line manager — which converts a technical correction into a reputational event. Kindness that routes bad news through hierarchy is not kindness.

#### Question 9 (challenging) — The minister's briefing and the inconvenient risk

You are contributing to a briefing for senior officials supporting a ministerial announcement about a major digital transformation. The draft states the legacy system replacement "is on track for completion next year". Your analysis shows a material risk: a critical data migration dependency is unresolved and could slip completion by up to a year. The programme director asks you to "keep the briefing positive — the risk is being managed."

Possible actions:

- A: Insist the briefing include your full risk analysis with all supporting detail, or your name comes off the work.
- B: Accept the director's framing — the risk is indeed being managed, and briefings are their call.
- C: Propose wording that is both accurate and proportionate — for example, "on track, subject to a known migration dependency that is being actively managed" — and if the director refuses any acknowledgement of the risk, escalate your concern through your professional line before the briefing is finalised.
- D: Send your risk analysis directly to the senior officials, bypassing the director.

**Most effective: C. Least effective: B.**

**Explanation:** Briefings that inform ministers sit at the sharp end of public sector transparency: officials advising ministers are entitled to an accurate picture. C does the professional work of finding language that is truthful without being alarmist — "positive" and "accurate" are usually reconcilable with careful drafting, which is precisely the architecture-communication skill of adapting the message to the audience — and it establishes a clear line: accuracy is not negotiable, and if it cannot be achieved collaboratively, the professional escalation route exists for exactly this. A confuses accuracy with completeness: a ministerial briefing does not need your full analysis, and making it an ultimatum about your name personalises what should be about the reader's need. D torpedoes trust and due process in one move; bypassing the director should be a last resort after C's escalation route, not a first response. B is least effective: "the risk is being managed" is the director's assertion, not your analysis, and acquiescing means senior officials brief a minister on a picture you know is materially incomplete. When transparency and hierarchy collide, the enterprise architect's obligation runs to the accuracy of the enterprise picture.

#### Question 10 (moderate) — The reuse recommendation nobody wants

Your analysis shows a sister department's grants platform could be reused for a new service at roughly 40% of the cost of the delivery team's preferred build. The delivery team resists: "Their platform is clunky, we didn't design it, and reuse makes us dependent on another department's roadmap."

Possible actions:

- A: Mandate reuse through the Design Authority and close the discussion.
- B: Accept the build option — team motivation matters more than a cost model.
- C: Take the team's objections seriously as requirements: test the "clunky" claim against user needs, get the dependency risk in the open by brokering a roadmap conversation with the sister department, and bring the enriched comparison — costs, risks, mitigations — back to a decision the team helps to shape.
- D: Ask the sister department to present their platform to the team and let the team decide alone.

**Most effective: C. Least effective: B.**

**Explanation:** The reuse duty in your role profile ("recommend reuse... to achieve value for money") is easy when everyone agrees; this scenario tests it against real resistance containing real information. C treats objections as data: "clunky" may encode genuine usability gaps that matter for user needs (test it), and dependency on another department's roadmap is a legitimate architectural risk that has a standard treatment — engagement, agreements, shared governance — rather than avoidance. Crucially, C keeps the team inside the decision, which is how recommendations survive contact with delivery. A wins the decision and loses the team: mandated reuse implemented by a resentful team fails slowly and expensively. D outsources an enterprise decision to the party with the strongest local interest; teams should shape decisions, not own trade-offs whose costs fall on the whole organisation. B is least effective because it converts a 60% cost premium into a morale payment without even testing the objections — value for money set aside not for evidence, but for comfort. The public purse deserves the analysis C insists on.

#### Question 11 (challenging) — The horizon-scanning disagreement

You believe an emerging technology (say, confidential computing) will materially change your organisation's data-sharing architecture within three years, and you want to start a small evaluation. Your peer enterprise architects disagree, calling it hype, and the architecture strategy group votes against including it in this year's radar.

Possible actions:

- A: Accept the group's decision, drop the topic entirely, and revisit only if the group raises it again.
- B: Run a small evaluation anyway using discretionary programme time, without telling the group.
- C: Accept the collective decision on the radar, while keeping the topic legitimately alive: track external evidence, build a stronger case with concrete departmental use cases, and bring it back to the group when material new evidence emerges.
- D: Escalate over the group's heads to the chief architect, arguing the group is complacent.

**Most effective: C. Least effective: B.**

**Explanation:** Horizon scanning is a named duty of your role, but so is working through collective governance — and this scenario tests what a senior professional does when the two collide. C holds both: the group's decision stands (collective governance means accepting outcomes you argued against), while your professional judgement continues to operate in the open — monitoring evidence, sharpening the case with organisation-specific use cases (the usual weakness of "hype" arguments in both directions), and returning through the front door when the facts warrant. That is how being right eventually becomes being effective. A confuses accepting a decision with abandoning professional judgement; if the technology matters, dropping surveillance entirely is a whole-context failure. D spends escalation capital on a disagreement about a radar entry, and "complacent" converts a technical disagreement into a personal one. B is least effective: a covert evaluation defies a collective decision in secret, and its findings are unusable — favourable results reveal the defiance; unfavourable ones were not worth the trust spent. Influence-based roles cannot afford secret work.

#### Question 12 (moderate) — The stakeholder who heard a promise

A director tells colleagues that you "committed" the enterprise architecture team to delivering an integration design for their programme by month end. What you actually said, in a corridor conversation, was that the timeline "sounded feasible, subject to checking the team's capacity". Your team cannot deliver it by month end without dropping higher-priority work.

Possible actions:

- A: Deliver it anyway by quietly deprioritising the other work — protecting the relationship matters most.
- B: Contact the director promptly and directly: clarify what was actually said, take your share of responsibility for the ambiguity, present the real capacity picture and options (later date, reduced scope, or a re-prioritisation decision made openly with the affected parties), and confirm the outcome in writing.
- C: Email the director's colleagues correcting the record, so the misstatement doesn't stand.
- D: Have your team lead tell the programme that no commitment exists.

**Most effective: B. Least effective: C.**

**Explanation:** This is expectation management — a named element of your architecture-communication skill — in its most common real form: a hedge heard as a promise. B contains every necessary move: it goes to the source rather than around them; it owns the communication failure ("subject to checking capacity" was said, but corridor conversations invite exactly this misunderstanding); it replaces the false commitment with real options rather than a bare refusal; and it closes the loop in writing, which is how corridor ambiguity is prevented from recurring. A rewards the misunderstanding by silently taxing higher-priority work — the whole-context failure of solving a local relationship problem with an enterprise resource; and D sends a subordinate to deliver your correction, which reads as both evasive and dismissive. C is least effective because correcting the record laterally — to the director's colleagues, without speaking to the director first — publicly contradicts a senior stakeholder and converts a fixable misunderstanding into a credibility contest. Expectations are managed with the person who holds them.

### Preparation tips

- **Anchor on the values, not the personalities.** Before the test, internalise the public sector digital values your answers should express: user needs first, transparency, collaboration, accessibility and inclusion, and value for public money. When two options both seem plausible, the one that better serves these values is usually the keyed answer.
- **Look for the option that engages before it escalates.** At your level, the strongest answers typically seek to understand stakeholders' drivers first, use governance channels as enablers rather than weapons, and hold escalation in reserve for when engagement fails. First-move escalation and first-move capitulation are both usually wrong.
- **Check each option for hidden transparency costs.** Covert action — quiet delays, secret evaluations, unannounced non-enforcement, undisclosed briefings — is almost always the least effective option, however practically appealing. If an option only works while nobody knows about it, it fails.
- **Read the question format carefully.** "Most effective" and "least effective" are judgements about outcomes, not intentions; a well-meant option can be least effective. In ranking formats, spend your effort on the extremes — the best and worst are usually clearer than the middle.
- **Rehearse with your own history.** Recall real dilemmas from your career: the bypassed governance, the deadline versus the standard, the community that stopped attending. For each, ask what worked, what you would do differently, and which value was really at stake. Experience becomes assessment performance when it is reflected on, not just accumulated.
- **Answer as the role, not as the hero.** The test wants an enterprise architect who strengthens institutions — governance, communities, decision processes — rather than one who personally saves every situation. Options where systems get stronger usually beat options where you win.

### Common pitfalls

- **Choosing idealistic over effective.** Options that sound noble but ignore practical reality — refusing all compromise, demanding perfection before any launch — are rarely keyed as most effective. The public sector values pragmatic delivery of user needs, not purity.
- **Selecting passive or deflecting options.** Deferring decisions, referring everything elsewhere, logging objections instead of acting, or letting others decide enterprise trade-offs — passivity is the most commonly keyed "least effective" pattern, and the assessment literature flags it explicitly.
- **First-resort escalation.** Jumping to a superior, a board, or a public forum before attempting direct engagement reads as influence failure. Escalation is a tool; as an opening move it is usually a mistake.
- **Ignoring the organisational culture.** UK government digital culture prizes openness, working in the open, and cross-department collaboration. Options that hoard information, protect territory or treat other departments as rivals score poorly even when commercially shrewd.
- **Solving the technical problem and missing the human one.** Several scenarios embed a correct technical answer inside a poor interpersonal move (taking over the junior architect's presentation, for instance). The keyed answer usually gets both right.
- **Answering as you suspect the organisation behaves, rather than as its values require.** Situational judgement tests are keyed to the espoused values and competency framework. Cynical answers — "escalation is what actually works here" — cost marks even where the cynicism is locally accurate.

## Conclusion

Well done — you have worked through a substantial and demanding set of materials. You have explored the four assessment types most relevant to your work as an enterprise architect: cognitive ability, where you practised logical deduction, error checking and prioritisation on roadmaps, decision records and standards; numeric reasoning, where you worked through budgets, licence models, total cost of ownership, risk exposure and capacity figures; verbal reasoning, where you sharpened the discipline of answering strictly from the text of principles, minutes, supplier letters and horizon-scanning briefings; and situational judgement, where you weighed realistic dilemmas involving directors, delivery teams, suppliers, governance boards and your own architecture community.

A few themes will have stood out. Precision with words and numbers is not pedantry in your role — it is the foundation of credible guidance. Rules and models should be applied faithfully and challenged openly, never quietly bent. Transparency beats cleverness in every dilemma. And influence, the true currency of enterprise architecture, is built through engagement first, governance always, and escalation rarely.

As next steps, consider revisiting the questions you found hardest and articulating, in your own words, why the keyed answer wins. Practise with your own artefacts — a real roadmap, a real business case, real board minutes — because familiarity with your domain's materials is the best preparation of all. If a formal assessment is ahead of you, take any official practice test the provider offers, arrive rested, and trust the professional judgement you exercise every day; these assessments measure what you already do.

Above all, treat this as one strand of continuous professional development. The skills tested here — architecting for the whole context, communicating with clarity, thinking commercially, collaborating generously, deciding transparently and shaping strategy — grow throughout a career. Keep practising, keep reflecting, and keep developing the community around you as you develop yourself. You are ready for this. Good luck!

---

Professional development tip: discuss your practice results with a mentor, a peer architect, or your line manager as part of your regular development conversations — turning individual practice into shared learning is itself an enterprise architecture habit worth modelling.
