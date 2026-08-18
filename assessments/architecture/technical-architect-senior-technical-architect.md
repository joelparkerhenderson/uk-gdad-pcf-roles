# Technical Architect (Senior Technical Architect) - Psychometric Assessment Resources

## Introduction

Welcome. This document is written for you: a senior technical architect working within the UK Government Digital and Data profession. You already operate at a level where you define strategy, assure services, collaborate with senior stakeholders, and mentor junior colleagues. This resource is designed to help you prepare for, practise, and reflect on the psychometric assessments that are increasingly used in recruitment, promotion, and professional development processes across the public sector.

Psychometric assessments are structured, standardised exercises that measure how you think, reason, and make judgements. They are not tests of memorised knowledge, and they are not attempts to catch you out. Used well, they offer an objective, evidence-based complement to interviews and application forms — and for a role like yours, where the consequences of architectural decisions ripple across large, complex, and risky pieces of work, employers want confidence that your reasoning is as strong as your track record suggests.

This document covers four assessment types, each tailored specifically to the duties and skills of a senior technical architect:

1. **Workplace job-specific cognitive assessment** — pattern recognition, logical deduction, error checking, and problem solving using the artefacts you genuinely handle: architecture decision records, dependency maps, technology roadmaps, and assurance findings.
2. **Workplace job-specific numeric reasoning assessment** — interpreting capacity figures, cloud cost models, migration budgets, performance metrics, and risk-weighted estimates.
3. **Workplace job-specific verbal reasoning assessment** — drawing precise conclusions from dense written material such as technology strategies, service standards, governance papers, and stakeholder correspondence.
4. **Workplace job-specific situational judgement assessment** — navigating realistic dilemmas involving senior stakeholders, delivery teams, governance boards, and the junior colleagues you mentor.

Each section explains what the assessment measures, maps it explicitly to the skills in your role profile — architecting for the whole context, architecture communication, community collaboration, making architectural decisions, strategy design, and technical design throughout the life cycle — and then gives you a substantial set of practice questions with worked answers. Each section closes with preparation tips and common pitfalls.

How should you use this resource? Three ways. First, as practice: work through the questions under light time pressure and check your reasoning against the explanations. Second, as self-reflection: notice where your reasoning diverges from the model answers and ask why — sometimes the divergence reveals a genuine development area, sometimes it reveals healthy professional scepticism worth articulating in an interview. Third, as preparation: the formats here mirror what you are likely to meet in real assessment platforms, so familiarity alone will reduce anxiety and free your working memory for the questions themselves.

Take your time, be honest with yourself, and enjoy the process. You have deep expertise; these assessments are simply another medium in which to demonstrate it.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive assessment measures the core mental processes your role demands: pattern recognition, logical deduction, error checking, prioritisation, and structured problem solving. Unlike a generic IQ test, it is role-targeted — the questions mimic the everyday tasks and data formats of the actual job. For you, that means reasoning over architecture decision records, dependency graphs, technology roadmaps, integration diagrams, assurance findings, and risk registers rather than abstract shapes and number sequences.

These assessments are typically delivered online, timed at around 15 to 30 minutes, and objectively scored against a norm group of comparable professionals. Some modern platforms adapt question difficulty based on your previous answers, and most provide short, ungraded practice questions first so you can get comfortable with the interface. Employers usually receive a breakdown showing speed versus accuracy rather than a single score, so a careful, deliberate style is not automatically penalised — but you should still keep moving.

Why does this matter for a senior technical architect? Because your role sits at the point where complexity concentrates. You work on large or multiple pieces of work that are complex or risky. You are expected to be proactive in identifying problems and translating them into non-technical descriptions that can be widely understood — which requires you to spot the problem in the first place, often buried in a dense artefact or an inconsistent set of claims. Cognitive assessments are among the strongest predictors of performance in exactly this kind of high-complexity work.

### What it measures for your role

Each cognitive dimension maps directly onto the skills in your role profile:

- **Pattern recognition → Architect for the whole context.** You track emerging issues, strategies, roadmaps, patterns and technologies over time to assess opportunities and risks. Assessment questions will ask you to spot trends, recurring anti-patterns, and anomalies across sequences of architectural events or technology adoption data.
- **Logical deduction → Making architectural decisions.** You make architectural design decisions characterised by managed levels of risk and complexity. Questions present rules, constraints, and dependencies — much like architectural principles and governance conditions — and ask what necessarily follows.
- **Error checking → Technical design throughout the life cycle.** You maintain appropriate quality and architectural coherence of a technical design in response to change. Questions ask you to find inconsistencies between two versions of a design artefact, or between a specification and its implementation summary.
- **Prioritisation → Strategy design.** You support the implementation of a strategy or vision using a roadmap or plan. Questions present competing work items with constraints and ask you to sequence them defensibly.
- **Problem decomposition → Architecture communication.** You lead the communication of complicated, complex or risky topics. Several questions test whether you can identify the essential structure of a messy problem — the precondition for explaining it simply to senior stakeholders.

### Practice questions

**Question 1 (easy) — Dependency deduction.**
Your programme has five services: Identity, Payments, Notifications, Case Management, and Reporting. The following constraints hold: Payments cannot go live before Identity. Notifications must go live before Case Management. Reporting must go live last. Case Management cannot go live before Payments. If Identity goes live second, which service goes live first?

A) Payments
B) Notifications
C) Case Management
D) Reporting

**Correct answer: B) Notifications.**

**Explanation:** Reporting is fixed last (position 5). Payments requires Identity first, so Payments cannot be first. Case Management requires both Notifications and Payments before it, so it cannot be first. Identity is second by the question's stipulation. The only remaining candidate for first is Notifications. A full valid order is: Notifications, Identity, Payments, Case Management, Reporting. This is the same reasoning you use when sequencing service migrations against hard dependencies — start by fixing what is pinned, then eliminate the impossible.

**Question 2 (easy) — Error checking an architecture decision record.**
An architecture decision record (ADR) states: "Decision: adopt the shared API gateway for all citizen-facing services. Context: three of our four citizen-facing services already route through the gateway. Consequence: after adoption, no citizen-facing service will route traffic directly to backend services." Later, the implementation summary states: "All five citizen-facing services now route through the shared gateway, except the legacy appeals service, which routes directly to its backend."

Which two inconsistencies exist between the ADR and the summary?

A) The count of citizen-facing services differs, and the "no direct routing" consequence is violated.
B) The gateway named differs, and the count of services differs.
C) The "no direct routing" consequence is violated, and the context is misstated.
D) There are no inconsistencies.

**Correct answer: A.**

**Explanation:** The ADR speaks of four citizen-facing services; the summary speaks of five — an inconsistency of count. The ADR's stated consequence is that no citizen-facing service routes directly to backend services; the summary admits the appeals service does exactly that — a violated consequence. The gateway is not named differently anywhere, so B fails; the context (three of four already routed) is not contradicted by the summary, so C fails. Spotting this kind of drift between decision and implementation is the essence of maintaining architectural coherence in response to change.

**Question 3 (moderate) — Pattern recognition in incident data.**
Over six releases, the number of post-release incidents attributed to integration failures is: Release 1: 2, Release 2: 3, Release 3: 5, Release 4: 8, Release 5: 12, Release 6: 17. Each release also doubled the number of new service-to-service integrations added. Which statement best characterises the pattern?

A) Incidents are growing linearly, so current assurance practices are scaling adequately.
B) The increase between consecutive releases grows by one extra incident each time, suggesting incident growth is accelerating and correlates with integration growth.
C) Incidents are random noise; no pattern can be inferred from six data points.
D) Incidents will certainly reach 23 next release.

**Correct answer: B.**

**Explanation:** The differences between consecutive values are 1, 2, 3, 4, 5 — the growth itself is growing, which is acceleration (a quadratic-like pattern), not linear growth, ruling out A. Six points is few, but a perfectly monotone accelerating series alongside a known causal driver (doubling integrations) is a legitimate signal, so C overstates the uncertainty. D converts an extrapolation into a certainty — the pattern suggests around 23 but cannot guarantee it; assessments frequently punish confusing "projected" with "certain". As a senior technical architect tracking emerging issues over time, the professionally useful conclusion is B: the trend and its plausible driver justify proactive intervention before the pattern continues.

**Question 4 (moderate) — Logical deduction from architectural principles.**
Your organisation's principles state: (1) All new services must be cloud-hosted. (2) Services handling SECRET data must not be cloud-hosted on the shared tenancy. (3) Any service that is not on the shared tenancy requires an approved exception. A team proposes a new service handling SECRET data. Which conclusion necessarily follows?

A) The service cannot be built.
B) The service must be cloud-hosted and must have an approved exception.
C) The service must be hosted on the shared tenancy.
D) The service does not need to be cloud-hosted because it handles SECRET data.

**Correct answer: B.**

**Explanation:** Principle 1 applies to all new services, so the service must be cloud-hosted — nothing in the principles exempts SECRET data from principle 1, which eliminates D. Principle 2 forbids the shared tenancy for this service, eliminating C. Being cloud-hosted but off the shared tenancy is permitted, so A is false. Principle 3 then bites: not on the shared tenancy means an approved exception is required. So the service must be cloud-hosted, off the shared tenancy, with an approved exception — exactly B. Note the discipline required: you deduce only what the stated rules entail, resisting the temptation to import real-world knowledge about classified hosting. This mirrors engaging with architectural governance, where the written principle — not your assumption about its intent — is what the review board will test your design against.

**Question 5 (moderate) — Prioritisation under constraint.**
You have one architecture review slot this week and four items requesting it: (1) a low-risk design refresh for an internal tool, due in six weeks; (2) a high-risk data-sharing design for a cross-department service, due at a governance board in eight days, where rework would take three weeks; (3) a medium-risk API versioning decision blocking one delivery team today; (4) a speculative technology evaluation with no deadline. A second review slot opens next week. Which item takes this week's slot, and why?

A) Item 3, because it is blocking a team right now.
B) Item 2, because its governance deadline combined with three weeks of potential rework means a review next week would leave no recovery time.
C) Item 1, because it was requested first.
D) Item 4, because horizon scanning is part of your role.

**Correct answer: B.**

**Explanation:** The key is to reason about lead time to consequence, not just urgency of noise. Item 2 has eight days to a governance board and a three-week rework tail: if the review happens next week and finds problems, the design fails governance with no time to recover — an irreversible slip on a high-risk, cross-department piece of work. Item 3 is genuinely blocking, but an API versioning decision for one team is a medium-risk, recoverable situation, and crucially it may be resolvable outside a formal review slot — a senior architect can unblock a team with a short conversation and a documented interim decision, then ratify it in next week's slot. Item 1 has ample slack; item 4 has none of the time-criticality that spends a scarce slot well. This is prioritisation as your role practises it: managed levels of risk, attention to what is reversible versus irreversible, and use of lightweight mechanisms where formal ones are not needed.

**Question 6 (moderate) — Spot the flawed inference.**
A discovery report concludes: "87% of surveyed caseworkers said the current system is slow. Therefore the database is the bottleneck and we should re-platform to a new database service." Which is the strongest criticism of this reasoning?

A) 87% is not a large enough majority to act on.
B) User-reported slowness establishes that a performance problem exists, but nothing in the evidence locates the bottleneck in the database rather than the network, application code, or client devices.
C) Caseworkers are not qualified to comment on performance.
D) Surveys should never be used in technical discovery.

**Correct answer: B.**

**Explanation:** The report makes a two-step leap: from "users perceive slowness" (well-evidenced) to "the database is the cause" (unevidenced) to "re-platform" (a costly remedy resting on the unevidenced step). B names the missing link precisely. A misdirects — 87% is ample evidence for the existence of a problem; the flaw is diagnostic, not statistical. C and D dismiss legitimate evidence rather than critiquing the inference. Being proactive in identifying problems means separating the observation from the diagnosis from the remedy — and challenging requirements and assumptions, as your strategy design skill demands, before a programme commits money to the wrong fix.

**Question 7 (challenging) — Multi-constraint scheduling.**
Three teams — Alpha, Beta, Gamma — must each complete a migration task in one of three consecutive fortnights (F1, F2, F3), one team per fortnight. Constraints: Alpha's task must precede Gamma's, because Gamma consumes Alpha's new API. Beta cannot migrate in F1 because its service freeze ends mid-F1. The shared platform team can support only one "high-support" migration, and both Beta's and Gamma's migrations are high-support — so Beta and Gamma cannot be in adjacent fortnights (the platform team needs a fortnight to recover between high-support migrations). Which schedule satisfies all constraints?

A) Alpha F1, Beta F2, Gamma F3
B) Alpha F1, Gamma F2, Beta F3
C) Beta F1, Alpha F2, Gamma F3
D) No schedule satisfies all constraints

**Correct answer: D.**

**Explanation:** Test each option. A: Alpha before Gamma holds; Beta avoids F1; but Beta (F2) and Gamma (F3) are adjacent — violates the platform constraint. B: Alpha (F1) precedes Gamma (F2) — fine; Beta is in F3, not F1 — fine; but Gamma (F2) and Beta (F3) are adjacent — violates the platform constraint again. C: Beta is in F1 — violates the freeze constraint immediately. Since only three orderings are offered and each fails, D is correct. More generally: with three consecutive slots, any assignment places Beta and Gamma at best one fortnight apart unless they occupy F1 and F3 — but Beta cannot take F1, so Beta must take F3 and Gamma F1, which then violates Alpha-before-Gamma. The constraint set is unsatisfiable, and the professional response is to say so and renegotiate a constraint (for example, extra platform support or a fourth fortnight) rather than to pick the least-bad illegal schedule. Assessments include "no valid option" questions precisely because senior roles require the confidence to report that the asked-for plan cannot work.

**Question 8 (challenging) — Pattern recognition across a technology radar.**
Your organisation's last four technology radar reviews show the following movements: containers moved from Trial to Adopt; the legacy ESB moved from Adopt to Hold; server-side rendering moved from Assess to Trial; a proprietary integration suite moved from Trial to Hold; event streaming moved from Assess to Trial to Adopt across the period. A team now proposes building a new integration layer on the proprietary integration suite. What is the most defensible architectural reading of the radar?

A) The proposal aligns with the radar because the suite was once in Trial.
B) The radar shows a sustained shift away from proprietary, centralised integration towards open, event-driven patterns, so the proposal runs against the organisation's observed direction of travel and needs strong justification.
C) The radar is advisory only, so it has no bearing on the proposal.
D) The proposal should be rejected without discussion.

**Correct answer: B.**

**Explanation:** Read the movements as a pattern, not as isolated facts: the ESB (centralised proprietary integration) moved to Hold; the proprietary suite moved to Hold; event streaming moved steadily to Adopt. Together they describe a consistent strategic direction — away from proprietary centralised integration, towards event-driven approaches. A cherry-picks a stale data point (the suite has since moved to Hold). C is too weak: radars are advisory, but "advisory" means they shift the burden of justification, not that they carry no weight. D is too strong: your role is to provide direction and challenge, and to find agreement with stakeholders — a Hold rating invites the team to justify an exception through governance, not to be dismissed. B captures both the pattern and the proportionate response, exactly as the "track emerging issues, strategies, roadmaps, patterns and technologies over time" element of architecting for the whole context intends.

**Question 9 (challenging) — Error checking a design under change.**
Version 1 of a technical design states: "The service stores citizen documents in the departmental object store, encrypted at rest with keys managed by the central key service. Retention: 7 years. The audit service receives a copy of every access event within 5 minutes." Version 2, after a change request, states: "The service stores citizen documents in the new cross-government object store, encrypted at rest. Retention: 7 years. The audit service receives a daily batch of access events." Which architecturally significant properties changed, possibly silently?

A) Only the storage location changed.
B) Storage location changed; key management ownership is no longer specified; audit latency degraded from 5 minutes to up to 24 hours.
C) Retention changed and encryption was removed.
D) Nothing significant changed; both versions encrypt at rest and retain for 7 years.

**Correct answer: B.**

**Explanation:** Compare clause by clause. Storage location: departmental store → cross-government store (explicit change). Encryption: both versions say "encrypted at rest", but version 1 specifies keys managed by the central key service and version 2 is silent — silence is not equivalence; key ownership may have changed, and an unspecified property in a security-relevant design is itself a defect. Audit: "within 5 minutes" → "daily batch" is a material degradation in detection latency for potential misuse of citizen data. Retention is unchanged, so C is wrong; A and D each miss at least one change. The craft here — noticing what a revision stops saying, not just what it says differently — is central to maintaining quality and architectural coherence of a technical design in response to change, and it is exactly what an assurance reviewer will expect a senior technical architect to catch.

**Question 10 (challenging) — Problem decomposition for communication.**
A delivery director asks you to explain, in one slide, why the case-management replacement is six weeks late. The true causes are: an upstream identity dependency slipped by four weeks; the team then discovered the legacy data model conflated two entity types, requiring a remodel; and two developers were reassigned mid-sprint. Which structure best decomposes the situation for a senior non-technical audience?

A) A chronological list of all 23 Jira tickets involved.
B) Three headlines — external dependency slip, discovered legacy complexity, resourcing change — each with impact in weeks and one mitigation, plus the single decision you need from the director.
C) A detailed entity-relationship diagram showing the conflated entities.
D) A statement that the delay is "due to technical debt" with no further detail.

**Correct answer: B.**

**Explanation:** Your role profile is explicit: translate problems into non-technical descriptions that can be widely understood, adapt your message to your audience, and manage stakeholder expectations. B does all three — it decomposes the messy reality into three causal threads, quantifies each in the audience's unit of concern (weeks), pairs each with a mitigation to show control, and ends with a decision request, which is what senior meetings exist to produce. A drowns the signal; C answers a question nobody asked at this altitude; D is technically honest but informationally empty, and it surrenders the trust that specific, quantified candour builds. Cognitive assessments increasingly include questions like this because decomposition-for-audience is a reasoning skill, not merely a presentation skill.

**Question 11 (hard) — Deduction with an exception hierarchy.**
Governance rules: (1) All externally facing services must pass a service assessment. (2) Services in private beta are exempt from rule 1 until public beta. (3) Any service processing payments must pass a security review regardless of phase. (4) A security review cannot begin until a design review is complete. A payments service is in private beta and its design review is scheduled to complete in three weeks. What can you deduce about its assessment obligations today?

A) It needs nothing until public beta.
B) It must pass a service assessment now.
C) It must pass a security review, which cannot begin for at least three weeks; the service assessment is deferred until public beta.
D) The design review is unnecessary because the service is exempt.

**Correct answer: C.**

**Explanation:** Work the rules in order of specificity. Rule 2 defers the service assessment (rule 1) until public beta — so B is wrong, and the first half of A is right. But rule 3 says "regardless of phase": the private beta exemption does not touch the security review obligation, so A as a whole is wrong. Rule 4 chains a precondition onto that obligation: no security review until the design review completes, which is three weeks away. D confuses exemptions — the exemption in rule 2 covers the service assessment only, not the design review, which is needed as a precondition for the mandatory security review. C is the complete, correct deduction. This layered-exemption structure is exactly how real assurance frameworks behave, and engaging with architectural governance means holding the whole rule hierarchy in mind rather than stopping at the first exemption that seems to help.

**Question 12 (hard) — Root-cause reasoning from mixed signals.**
After a new caching layer goes live, you observe: average API latency improved from 340ms to 90ms; the 99th-percentile latency worsened from 900ms to 4,200ms; error rates are unchanged; cache hit rate is 96%. Which hypothesis best explains all four observations?

A) The cache is misconfigured and serving stale data.
B) Cache hits are fast (improving the average), but the 4% of cache misses now traverse an extra network hop and a cold path, making misses far slower than the original direct calls (degrading the tail).
C) The backend database has failed.
D) The improvement in average latency proves the change is uniformly beneficial.

**Correct answer: B.**

**Explanation:** Test each hypothesis against all the evidence, not just some of it. A (stale data) would typically surface as correctness errors or complaints, but error rates are unchanged, and staleness does not explain a slower tail. C (database failure) would raise error rates and would not improve the average. D ignores the tail entirely — and in citizen-facing government services the tail is where real users live: the 1% of requests taking 4.2 seconds may be the accessibility-critical journeys. B explains everything: 96% of requests hit the cache and are fast, dragging the average down; the 4% that miss now pay cache-lookup-plus-origin cost on an unwarmed path, stretching the 99th percentile. The reasoning pattern — find the single hypothesis consistent with every observation — is core senior-architect problem solving, and the follow-up (instrument the miss path before rolling forward) is the kind of proactive problem identification your role level expects.

**Question 13 (hard) — Prioritising architectural risk.**
Your risk register for a multi-team programme shows four open architectural risks: (R1) a single shared database instance underpins three services, likelihood medium, impact severe, no mitigation started; (R2) a supplier's SDK licence changes in 12 months, likelihood high, impact moderate, mitigation planned; (R3) one team is using an unapproved framework, likelihood certain, impact minor, mitigation trivial; (R4) the disaster recovery plan is untested, likelihood low, impact severe, test scheduled next quarter. You can materially advance exactly one risk this sprint. Which, and why?

A) R3, because it is certain to occur.
B) R2, because its likelihood is high.
C) R1, because it combines severe impact with meaningful likelihood and — uniquely — has no mitigation underway, so marginal effort there buys the largest reduction in unmanaged exposure.
D) R4, because disaster recovery is always the top priority.

**Correct answer: C.**

**Explanation:** The discriminator is not raw severity or likelihood but unmanaged exposure and the marginal value of your effort. R2 and R4 already have mitigations planned or scheduled — your sprint adds least where work is already in motion. R3 is certain but minor and trivially fixed; delegate it (and note that "certain × minor" is how registers trick candidates who scan single columns). R1 is the classic architectural time bomb: a shared single point of failure across three services, severe impact, medium likelihood, and nothing being done — the only risk where this sprint's effort converts "unmanaged" into "managed". This is what "identify and address architectural risks relevant to your team or domain" looks like as a reasoning exercise: rank by where your action changes the risk position most, not by any single register column.

### Preparation tips

- **Practise with your own artefacts.** Take a real ADR, roadmap, or risk register from your work and quiz yourself: what necessarily follows from this? What changed between versions? What is the single decision this document should drive? You will be rehearsing the exact cognitive moves the assessment samples.
- **Rehearse constraint problems on paper.** Dependency-ordering and scheduling questions (like Questions 1 and 7) reward a quick notation habit: pin the fixed points, eliminate the impossible, then test what remains. Thirty seconds of structure beats three minutes of mental juggling.
- **Read every quantifier.** Words like "all", "only", "regardless of phase", and "no" carry the logical load in deduction questions, just as they do in governance frameworks. Senior candidates lose marks not through weak logic but through fast reading.
- **Manage the clock like a portfolio.** With 15 to 30 minutes for the whole test, no single question deserves more than its share. Flag, skip, and return — the same triage you apply to your review queue.
- **Trust deliberate over frantic.** Score reports separate speed from accuracy. At your level, employers care that your reasoning is reliable under mild pressure; a measured pace with high accuracy reads well.
- **Warm up beforehand.** Do two or three practice items immediately before the real assessment so the question formats cost you no novelty tax.

### Common pitfalls

- **Importing outside knowledge.** The assessment world is closed: answer from the stated rules and data, not from what you know real platforms or policies do. Question 4 is deliberately built to punish imported assumptions.
- **Confusing projection with certainty.** Trends "suggest"; they do not "guarantee". Options containing "certainly" or "will definitely" attached to an extrapolation are usually wrong (see Question 3).
- **Stopping at the first exemption.** Layered rules often contain an overriding clause ("regardless of phase"). Read the full rule set before concluding anything is waived (see Question 11).
- **Missing what a document stops saying.** Error-checking questions hide changes as omissions, not just alterations (see Question 9). Compare artefacts clause by clause.
- **Time-sink questions.** Getting anchored on one hard multi-stage item instead of banking easier marks elsewhere is the most common cause of underperformance, at every seniority level.
- **Assuming there must be a valid answer.** Some questions, like some project plans, are unsatisfiable — and saying so is the mark of seniority (see Question 7).

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment evaluates your ability to analyse, interpret, and make sound decisions using numerical data drawn from the realities of your role. It is emphatically not an abstract mathematics exam: the arithmetic rarely goes beyond percentages, ratios, weighted averages, and rates. What it really tests is whether you can extract the right numbers from a realistic artefact — a cloud cost table, a capacity forecast, a migration budget, a performance dashboard — and reason with them quickly and accurately.

Typical characteristics: questions are built on real-world business data such as tables, budget spreadsheets, and utilisation charts; an on-screen calculator is usually allowed or provided, because the assessment prioritises interpretation over mental arithmetic; and there is a strict time limit, often around a minute to ninety seconds per question, which simulates the pace at which you are expected to sanity-check figures in governance papers and supplier proposals.

For a senior technical architect, numeric fluency is quietly load-bearing. You assure services — which means checking that a team's capacity claims, cost models, and performance targets actually add up. You provide direction and challenge to senior stakeholders — and the fastest way to earn the right to challenge is to find the arithmetic error in the business case before anyone else does. You make architectural decisions characterised by managed levels of risk — and risk management is substantially a numerical discipline: probabilities, impact ranges, and expected values. The scenarios below are drawn directly from these duties.

### What it measures for your role

- **Cost and budget interpretation → Strategy design.** Supporting a strategy's implementation through a roadmap means testing whether the roadmap is affordable. Questions use multi-year budget tables, cloud pricing comparisons, and total-cost-of-ownership calculations.
- **Capacity and performance arithmetic → Technical design throughout the life cycle.** Creating and refining technical designs requires throughput, latency, storage-growth, and headroom calculations. Questions use utilisation percentages, request rates, and growth projections.
- **Risk quantification → Making architectural decisions.** Managed risk means comparing options by expected cost or impact. Questions ask you to combine likelihoods and impacts, or to weigh a mitigation's cost against the exposure it removes.
- **Trend analysis → Architect for the whole context.** Tracking emerging issues over time means reading time-series data correctly: percentage change, compound growth, and the difference between levels and rates.
- **Evidence for communication → Architecture communication.** Managing stakeholder expectations often turns on presenting the right derived figure — cost per transaction, weeks of runway, percentage of demand served — so questions test whether you can compute the figure an audience actually needs.

### Practice questions

**Question 1 (easy) — Percentage change in hosting cost.**
Your platform's monthly hosting cost was £84,000 in April. After a rightsizing exercise you led, the May cost was £71,400. What was the percentage reduction?

A) 12.6%
B) 15%
C) 17.6%
D) 85%

**Correct answer: B) 15%.**

**Explanation:** Reduction = £84,000 − £71,400 = £12,600. Percentage reduction = 12,600 ÷ 84,000 = 0.15 = 15%. A common trap is dividing by the new value (12,600 ÷ 71,400 ≈ 17.6%, option C), which computes the increase you would need to get back to April, not the reduction achieved. Always divide the change by the original (baseline) value. When you report savings to a programme board, this distinction is exactly the kind of detail a sharp finance colleague will check.

**Question 2 (easy) — Capacity headroom.**
A case-management API handles a sustained 1,840 requests per second (rps) at peak. Load testing shows the current deployment saturates at 2,300 rps. What is the current peak headroom as a percentage of capacity?

A) 10%
B) 20%
C) 25%
D) 46%

**Correct answer: B) 20%.**

**Explanation:** Headroom = capacity − peak load = 2,300 − 1,840 = 460 rps. As a percentage of capacity: 460 ÷ 2,300 = 0.20 = 20%. Option C (25%) is the result of dividing headroom by the load instead of the capacity (460 ÷ 1,840 = 25%) — both framings exist in practice, so in the assessment (as in an assurance review) read carefully which denominator is asked for. "As a percentage of capacity" pins the denominator at 2,300.

**Question 3 (easy) — Reading a budget table.**
A programme budget shows, in thousands of pounds:

| Workstream | 2025-26 | 2026-27 |
|---|---|---|
| Platform build | 1,240 | 980 |
| Legacy migration | 760 | 1,410 |
| Assurance and security | 310 | 340 |
| Architecture and design | 450 | 380 |

By how much does total programme spend change from 2025-26 to 2026-27?

A) Increases by £350,000
B) Decreases by £350,000
C) Increases by £650,000
D) Increases by £350

**Correct answer: A) Increases by £350,000.**

**Explanation:** 2025-26 total = 1,240 + 760 + 310 + 450 = 2,760 (thousand). 2026-27 total = 980 + 1,410 + 340 + 380 = 3,110 (thousand). Change = 3,110 − 2,760 = +350 thousand = +£350,000. Option D is the classic scale-qualifier trap: the table is "in thousands of pounds", so 350 means £350,000. Misreading scale qualifiers ("in thousands", "in millions") is one of the most common errors in numeric assessments — and in real budget papers.

**Question 4 (moderate) — Cloud cost per transaction.**
Service A processes 2.4 million transactions per month at a monthly infrastructure cost of £36,000. Service B processes 900,000 transactions per month at £18,000. A director asks which service is more cost-efficient per transaction, and by how much. What do you tell them?

A) Service A at 1.5p per transaction, 33% cheaper per transaction than Service B at 2.0p.
B) Service B, because £18,000 is less than £36,000.
C) Service A at 15p per transaction versus Service B at 20p.
D) They are equally efficient.

**Correct answer: A.**

**Explanation:** Service A: £36,000 ÷ 2,400,000 = £0.015 = 1.5 pence per transaction. Service B: £18,000 ÷ 900,000 = £0.02 = 2.0 pence per transaction. Service A is cheaper per transaction by 0.5p, and 0.5 ÷ 2.0 = 25% cheaper relative to B — or, framing it as the question's option does, B is 33% more expensive than A (0.5 ÷ 1.5 ≈ 33%). Option B commits the absolute-versus-unit-cost error: total spend says nothing about efficiency without volume. Option C slips a decimal place — a reminder to sanity-check magnitudes (36,000 ÷ 2.4 million cannot be pence in double digits). Deriving the unit economics a senior audience needs is precisely the "evidence for communication" skill this assessment samples.

**Question 5 (moderate) — Storage growth projection.**
A document store currently holds 18 TB and is growing at 2.5 TB per quarter. The platform's contracted ceiling is 40 TB, and procurement of an uplift takes two quarters from initiation. After how many quarters from now must you initiate procurement, at the latest, to avoid breaching the ceiling?

A) 8 quarters
B) 6 quarters
C) 4 quarters
D) 2 quarters

**Correct answer: B) 6 quarters.**

**Explanation:** Ceiling headroom = 40 − 18 = 22 TB. At 2.5 TB per quarter, the ceiling is reached after 22 ÷ 2.5 = 8.8 quarters — so the store breaches during the 9th quarter. Procurement takes 2 quarters, so it must be initiated no later than 8.8 − 2 = 6.8 quarters from now; since decisions land on quarter boundaries in this question, the latest safe initiation point among the options is 6 quarters. Option A ignores procurement lead time entirely — the classic error of planning to the breach date rather than to the last responsible decision point. Thinking in lead times, not just end dates, is central to architecting for the whole context: the roadmap risk is created not when the ceiling is hit, but when the option to avoid it quietly expires.

**Question 6 (moderate) — Weighted option scoring.**
You are comparing two integration options against three weighted criteria. Scores are out of 10; weights sum to 1.

| Criterion | Weight | Option X | Option Y |
|---|---|---|---|
| Security posture | 0.5 | 6 | 8 |
| Delivery speed | 0.3 | 9 | 5 |
| Operating cost | 0.2 | 7 | 8 |

Which option wins on weighted score, and by how much?

A) Option X wins by 0.3
B) Option Y wins by 0.3
C) Option X wins by 1.0
D) They tie

**Correct answer: A) Option X wins by 0.3.**

**Explanation:** Option X: (0.5 × 6) + (0.3 × 9) + (0.2 × 7) = 3.0 + 2.7 + 1.4 = 7.1. Option Y: (0.5 × 8) + (0.3 × 5) + (0.2 × 8) = 4.0 + 1.5 + 1.6 = 6.8. So X scores 7.1, Y scores 6.8, and X wins by 0.3. Under time pressure, run each addition twice — in a different order the second time — because weighted-sum questions are where transposition slips cluster, and this is the cheapest error-check available. Note the architectural insight the numbers encode: Y wins the most heavily weighted criterion yet loses overall because X's advantage on speed (9 vs 5) outweighs it — weighted scoring can produce results that surprise stakeholders, which is why you should always show the table, not just the verdict, when communicating the decision.

**Question 7 (moderate) — Availability arithmetic.**
A citizen-facing journey chains three services in sequence: gateway (99.95% availability), application (99.9%), and legacy backend (99.5%). Assuming independent failures, what is the approximate end-to-end availability of the journey, and roughly how many minutes of unavailability per 30-day month does that imply?

A) About 99.35%, roughly 280 minutes per month
B) About 99.5%, roughly 220 minutes per month
C) About 99.95%, roughly 22 minutes per month
D) About 98%, roughly 880 minutes per month

**Correct answer: A.**

**Explanation:** Chained availability multiplies: 0.9995 × 0.999 × 0.995 ≈ 0.99351, i.e. about 99.35%. A quick approximation adds the unavailabilities: 0.05% + 0.1% + 0.5% = 0.65% unavailable, giving 99.35% — the approximation is excellent when unavailabilities are small. A 30-day month has 30 × 24 × 60 = 43,200 minutes; 0.65% of 43,200 = 0.0065 × 43,200 ≈ 281 minutes. Two professional lessons are embedded here. First, the chain is only as good as its weakest link times everything else — the legacy backend dominates the budget, which tells you where remediation spend belongs. Second, availability percentages hide their operational meaning until converted into minutes; senior stakeholders respond to "nearly five hours a month" very differently from "99.35%", and choosing the right representation is architecture communication in action.

**Question 8 (challenging) — Expected value of a mitigation.**
Your risk register estimates that, without mitigation, a shared-database failure has a 20% chance of occurring within the year, with an estimated impact of £600,000 (recovery, delay, and service disruption). A proposed mitigation — splitting the database — costs £90,000 and reduces the probability to 4% while halving the impact if it still occurs. On expected values over one year, what is the net benefit of the mitigation?

A) £108,000 net benefit
B) £18,000 net benefit
C) £96,000 net cost
D) £120,000 net benefit

**Correct answer: B) £18,000 net benefit.**

**Explanation:** Expected loss without mitigation = 0.20 × £600,000 = £120,000. Expected loss with mitigation = 0.04 × £300,000 (impact halved) = £12,000. Expected loss avoided = £120,000 − £12,000 = £108,000. Net benefit = £108,000 − £90,000 (mitigation cost) = £18,000. Option A forgets to subtract the mitigation's cost; option D forgets the residual risk; option C subtracts in the wrong direction. Two cautions worth voicing in a real governance discussion: expected value flattens a distribution into a single number, and a £600,000 tail event may deserve mitigation even at slightly negative expected value if the organisation is risk-averse about citizen-facing disruption. The assessment wants the arithmetic; the interview wants that second-order judgement too. This is "identify and address architectural risks" rendered numerically.

**Question 9 (challenging) — Migration burn-down with a rate change.**
A legacy migration must move 3,600 workloads. In its first four months the team averaged 150 workloads per month. A tooling improvement you sponsored is expected to raise the rate by 40% from month five onwards. How many months in total will the migration take?

A) 24 months
B) 20 months
C) 18.3 months, so 19 months
D) 16 months

**Correct answer: C) 18.3 months, so 19 months.**

**Explanation:** Months 1-4: 4 × 150 = 600 workloads done, leaving 3,600 − 600 = 3,000. New rate from month five: 150 × 1.4 = 210 workloads per month. Remaining time = 3,000 ÷ 210 ≈ 14.29 months. Total = 4 + 14.29 = 18.29 months — and since you cannot finish partway through a reporting month, the honest roadmap answer is 19 months. Option A applies the old rate throughout; option D applies the new rate throughout, including retrospectively to the first four months, which is the subtler and more common modelling error. Piecewise rates — before and after an improvement, a hiring round, or a freeze — appear constantly in delivery forecasting, and assessments reward candidates who segment the timeline rather than averaging across it.

**Question 10 (challenging) — Comparing supplier pricing structures.**
Two suppliers quote for an API platform. Supplier P: £22,000 per month flat, unlimited calls. Supplier Q: £8,000 per month plus £0.004 per call. Your service currently makes 3.2 million calls per month, growing 25% year on year. At current volume, which supplier is cheaper, and at what monthly call volume do the costs break even?

A) Q is cheaper now; break-even at 3.5 million calls per month.
B) P is cheaper now; break-even at 5.5 million calls per month.
C) Q is cheaper now; break-even at 3.5 billion calls per month.
D) P is cheaper now; break-even at 3.5 million calls per month.

**Correct answer: A.**

**Explanation:** Supplier Q at current volume: £8,000 + (3,200,000 × £0.004) = £8,000 + £12,800 = £20,800, which is less than P's £22,000 — Q is cheaper today. Break-even: solve 8,000 + 0.004V = 22,000, so 0.004V = 14,000, giving V = 3,500,000 calls per month. With 25% annual growth, 3.2 million becomes 4.0 million within a year — crossing the break-even in roughly five to six months. The strategic point the arithmetic surfaces: the cheaper option today becomes the dearer one within the contract's first year, so the decision should be made on the volume trajectory, not the current snapshot. Challenging a procurement recommendation with exactly this calculation is a textbook example of the "challenge requirements and assumptions" element of strategy design.

**Question 11 (challenging) — Performance percentiles and user impact.**
A service handles 1.8 million requests per day. Monitoring shows the median response time is 220ms, the 95th percentile is 1.1s, and the 99th percentile is 6.2s. The service standard requires 95% of requests to complete within 1.2 seconds. Approximately how many requests per day exceed the 99th-percentile threshold of 6.2s, and is the service standard currently met?

A) About 18,000 requests exceed 6.2s; the standard is met.
B) About 90,000 requests exceed 6.2s; the standard is not met.
C) About 18,000 requests exceed 6.2s; the standard is not met.
D) About 1,800 requests exceed 6.2s; the standard is met.

**Correct answer: A.**

**Explanation:** By definition, 1% of requests exceed the 99th percentile: 1% of 1,800,000 = 18,000 requests per day. The standard requires 95% within 1.2s; the measured 95th percentile is 1.1s, meaning 95% of requests complete within 1.1s — comfortably inside 1.2s — so the standard is met. Option C pairs the right count with the wrong compliance reading; watch for options that are half right, because they are the ones a rushed candidate selects. The deeper lesson for assurance work: a service can meet its headline standard while 18,000 daily requests take over six seconds — a population large enough to contain, disproportionately, users on poor connections and assistive technologies. Reading percentile tables both ways — compliance and tail impact — is the numeric fluency your assurance duty demands.

**Question 12 (hard) — Multi-year total cost of ownership.**
You are comparing two strategies for a legacy system. Strategy R (re-platform): £1.6m one-off in year 1, then £280,000 per year running costs from year 1 onwards. Strategy M (maintain): no one-off cost, running costs of £520,000 in year 1, rising by 15% each subsequent year as skills scarcity bites. Over a five-year appraisal period, which strategy is cheaper, and by approximately how much? (Ignore discounting.)

A) M is cheaper by about £0.5m.
B) R is cheaper by about £0.5m.
C) R is cheaper by about £1.1m.
D) They are approximately equal.

**Correct answer: B.**

**Explanation:** Strategy R: £1,600,000 + (5 × £280,000) = £1,600,000 + £1,400,000 = £3,000,000. Strategy M: year 1 = £520,000; year 2 = £598,000; year 3 = £687,700; year 4 = £790,855; year 5 = £909,483. Sum ≈ £520,000 + £598,000 + £687,700 + £790,855 + £909,483 ≈ £3,506,038. Difference ≈ £3.51m − £3.00m ≈ £0.5m in favour of R. The compounding is the whole story: in year 1, M looks £1.36m cheaper (£520k versus £1.88m), and a stakeholder anchored on the first-year budget line will resist R. Your job — supporting the development of a strategy that aligns with organisational objectives — is to widen the frame to the appraisal period and show the crossover. Also note what "ignore discounting" flags: in a real HM Treasury Green Book appraisal you would discount future costs, which slightly narrows but does not reverse this gap. Assessments simplify; your commentary in a real business case should not.

**Question 13 (hard) — Reconciling conflicting utilisation figures.**
A supplier's report claims the platform "runs at 85% efficiency". Your monitoring shows: 40 provisioned virtual machines; average CPU utilisation 34%; 12 of the VMs sit idle outside business hours (an average of 128 of each week's 168 hours) yet are billed continuously. Which single calculation most directly challenges the supplier's claim?

A) 85% of 40 is 34, which matches the CPU figure, so the claim is consistent.
B) The 12 always-on but mostly idle VMs are unused for 128 ÷ 168 ≈ 76% of billed hours, so nearly a third of the estate (12 ÷ 40 = 30%) is paid for but idle three-quarters of the time — irreconcilable with "85% efficiency" on any utilisation-based definition.
C) 34% CPU utilisation proves the platform is 66% wasted.
D) Efficiency cannot be measured, so the claim is unfalsifiable.

**Correct answer: B.**

**Explanation:** Option A is numerology — 85% of 40 being 34 is a coincidence of digits, not a meaningful calculation (34% utilisation is a rate, not a count of machines). Option C overreaches: low average CPU can be legitimate where headroom is held for failover or spiky demand, so utilisation alone does not equal waste. Option D surrenders the challenge instead of making it. B does what a senior technical architect should: it takes the supplier's own billing model, quantifies the idle exposure precisely (12 of 40 VMs = 30% of the estate; idle 128 of 168 hours = 76% of the time), and shows that no reasonable definition of efficiency reconciles those facts with 85%. It also implicitly names the remedy — scheduling or rightsizing the 12 VMs. Providing challenge to stakeholders and suppliers is most effective when it arrives as one crisp, checkable calculation rather than a general accusation; this question rehearses exactly that move.

**Question 14 (moderate) — Ratio reasoning for team capacity.**
Your architecture community supports 18 delivery teams. Guidance says the sustainable ratio is one architect to no more than 3 teams for high-risk work and one to 6 for low-risk work. Currently 12 teams are doing high-risk work and 6 are doing low-risk work, and you have 5 architects including yourself. How many additional architects are needed to meet the guidance?

A) None — 5 is sufficient.
B) 1 additional architect.
C) 2 additional architects.
D) 4 additional architects.

**Correct answer: A) None — 5 is sufficient.**

**Explanation:** Required capacity: high-risk needs 12 ÷ 3 = 4 architects; low-risk needs 6 ÷ 6 = 1 architect. Total required = 4 + 1 = 5, and you have exactly 5 — the guidance is met with zero slack. The numerically correct answer and the professionally complete answer differ in an instructive way: zero headroom means one departure, one long absence, or one team switching from low-risk to high-risk work breaks the ratio immediately. In an assessment, answer A and move on; in a workforce planning discussion, the follow-up sentence — "we comply today with no resilience margin, and the trend in high-risk work will break the ratio within two quarters" — is what turns arithmetic into advice. Mentoring junior colleagues into architecture roles, as your role level expects, is one of the levers you would propose.

### Preparation tips

- **Rebuild your percentage reflexes.** Percentage change (always divide by the baseline), percentage points versus percentages, and reverse percentages ("the cost after a 15% rise is £46,000 — what was it before?") cover most of what these tests ask. Ten minutes of drilling pays back immediately.
- **Practise on artefacts you already read.** Cloud bills, capacity dashboards, and programme finance packs are ideal practice material — extract three numbers and derive a fourth (unit cost, headroom, run-rate) against the clock.
- **Write the calculation before computing it.** Under time pressure, setting up "8,000 + 0.004V = 22,000" on paper prevents the transposition errors that mental set-up invites. The calculator is allowed; the set-up is the skill.
- **Estimate first, then compute.** A rough order-of-magnitude estimate catches decimal-place slips (as in Question 4) before they cost you the mark. If the computed answer disagrees wildly with your estimate, recheck.
- **Convert percentages into operational units.** Practise turning availability and percentile figures into minutes and request counts (Questions 7 and 11) — assessments love these conversions, and so do the senior stakeholders you brief.
- **Know when to move on.** Multi-stage questions like the five-year TCO are worth the same as a one-step percentage. Bank the quick marks, then return.

### Common pitfalls

- **Misreading scale qualifiers.** "In thousands" and "in millions" table headers are the most reliable trap in the genre (Question 3). Read the units before the numbers.
- **Wrong denominator.** Percentage-of-capacity versus percentage-of-load (Question 2), and change-over-original versus change-over-new (Question 1), are denominator choices, and the wrong one is always among the answer options.
- **Applying a rate change retrospectively.** When a rate improves partway through, segment the timeline (Question 9); averaging one rate across the whole period is the most common forecasting error.
- **Confusing totals with unit economics.** A cheaper total can hide a more expensive per-transaction cost (Question 4); volume context is everything.
- **Forgetting a cost term.** In net-benefit calculations, candidates routinely omit either the mitigation cost or the residual risk (Question 8). List every term before computing.
- **Over-calculating.** Where options are far apart, the additive approximation for availability (Question 7) or simple rounding will identify the answer faster than exact arithmetic; precision is a means, not an end.
- **Coincidence arithmetic.** Beware options that manufacture agreement from unrelated numbers (Question 13's "85% of 40 is 34"). Every calculation you accept should have a defensible meaning, in the test and in the boardroom.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment evaluates how well you understand, analyse, and draw correct conclusions from written material of the kind your role actually generates and consumes: technology strategies, service standards, governance papers, assurance reports, supplier correspondence, and policy documents. The defining discipline is fact-based logic — you answer strictly from the text provided, deliberately setting aside your own expert knowledge, however relevant it feels.

The dominant format is a passage followed by statements you must classify as **True** (the passage logically supports it), **False** (the passage contradicts it), or **Cannot Say** (the passage provides insufficient information either way). Multiple-choice comprehension questions — best summary, author's main claim, correct application of a stated rule — round out the set. Timing is tight, often under a minute per question, simulating the pace at which you triage a crowded inbox before a governance board.

For a senior technical architect, this is arguably the most job-realistic assessment of the four. You lead the communication of complicated, complex or risky architecture topics — which begins with reading such material with complete precision. You engage with architectural governance — where the difference between "must", "should", and "may" in a standard determines whether a design passes. You challenge requirements and assumptions — and the challenge only lands if your reading of the source document is unimpeachable. And you regularly collaborate and find agreement with senior stakeholders, whose positions arrive as carefully worded documents in which what is *not* said matters as much as what is.

### What it measures for your role

- **Precision reading of standards and policies → Making architectural decisions.** Governance documents encode obligations in modal verbs and scope clauses. Questions test whether you extract exactly what is mandated, permitted, and out of scope.
- **Inference discipline → Architect for the whole context.** Tracking emerging strategies means distinguishing what a document commits to from what it merely gestures at. Cannot Say questions train exactly this separation.
- **Argument analysis → Strategy design.** Challenging requirements and assumptions requires identifying a document's actual claim and its actual evidence, not the claim you expected. Main-argument questions sample this directly.
- **Stakeholder correspondence → Architecture communication.** Emails from senior stakeholders carry positions, conditions, and implicit expectations. Questions test whether you register precisely what has and has not been agreed — the raw material of managing stakeholder expectations.
- **Feedback and team texts → Community collaboration.** Retrospective write-ups and health-check reports need careful reading before you intervene in team dynamics; misreading them means misdiagnosing the team.

### Practice questions

**Passage A — Extract from a departmental hosting standard:**
"All new digital services must be deployed to one of the department's two approved cloud platforms. Services classified as OFFICIAL may use either platform. Services processing biometric data must use Platform One, which holds the enhanced accreditation, and must additionally complete a data protection impact assessment before public beta. Existing services are not required to migrate to an approved platform, but any existing service undergoing a major re-architecture must adopt an approved platform as part of that work. Exceptions to this standard may be granted only by the Technical Design Authority."

**Question 1 (easy).** True, False, or Cannot Say: A new digital service processing biometric data may be deployed to Platform Two.

**Correct answer: False.**

**Explanation:** The passage states directly: "Services processing biometric data must use Platform One". "Must use Platform One" excludes Platform Two, so the statement contradicts the text. Note that the general permission — "Services classified as OFFICIAL may use either platform" — does not rescue the statement, because the biometric clause is more specific and imposes an additional constraint. Reading specific clauses as overriding general ones is exactly how you read real standards in governance settings.

**Question 2 (easy).** True, False, or Cannot Say: An existing service that is not being re-architected must migrate to an approved platform within twelve months.

**Correct answer: False.**

**Explanation:** The passage says: "Existing services are not required to migrate to an approved platform". The statement asserts a migration obligation (with a deadline), and the passage explicitly negates that obligation — a direct contradiction, hence False rather than Cannot Say. The twelve-month detail is a distractor: once the core obligation is contradicted, added specifics cannot convert False into Cannot Say.

**Question 3 (moderate).** True, False, or Cannot Say: Platform Two does not hold the enhanced accreditation.

**Correct answer: Cannot Say.**

**Explanation:** The passage says Platform One "holds the enhanced accreditation". It says nothing about Platform Two's accreditation status. It is tempting to infer that if Platform Two also held the enhanced accreditation, biometric services would be allowed there — but the standard might restrict biometric processing to Platform One for other reasons (contractual, operational, or simply conservatism). The text neither confirms nor denies Platform Two's accreditation, so the disciplined answer is Cannot Say. This is the single most common trap in verbal reasoning: converting a plausible real-world inference into a textual fact.

**Question 4 (moderate).** True, False, or Cannot Say: A data protection impact assessment must be completed before a biometric service enters private beta.

**Correct answer: Cannot Say.**

**Explanation:** The passage requires the assessment "before public beta". Private beta precedes public beta in the usual service lifecycle — but the text does not say the assessment must precede private beta; a team could lawfully complete it during private beta and still satisfy the stated requirement. The statement imposes an earlier deadline than the passage does, and the passage is silent about that earlier point, so Cannot Say. If you answered True, you substituted a stricter rule you might personally prefer for the rule as written — a habit that, in real assurance work, generates avoidable disputes with delivery teams.

**Question 5 (moderate).** Which of the following most accurately states who can approve a deviation from this standard?

A) Any senior technical architect.
B) The Technical Design Authority only.
C) The platform team, with notification to the Technical Design Authority.
D) The passage does not address exceptions.

**Correct answer: B.**

**Explanation:** The final sentence is explicit: "Exceptions to this standard may be granted only by the Technical Design Authority." The word "only" does the decisive work, excluding A and C; D is contradicted by the sentence's existence. In assessments and in governance alike, exclusivity words — "only", "solely", "exclusively" — are load-bearing, and options that add plausible-sounding alternative routes ("with notification to...") test whether you noticed them.

**Passage B — Email from a programme director:**
"Thank you for the revised integration design. I can see the security concerns from the last review have been addressed, and I'm content for the team to proceed to build on that basis. However, I remain concerned about the dependency on the payments provider's roadmap: if their new API is delayed beyond March, our statutory deadline is at risk, and I have seen no contingency in the current plan. Before I can present this to the programme board with confidence, I need either a credible fallback option or evidence that the provider's March date is dependable. I'd also welcome your view on whether the caching approach affects our accessibility commitments, though this need not block the build starting."

**Question 6 (moderate).** True, False, or Cannot Say: The programme director has approved the design for presentation to the programme board.

**Correct answer: False.**

**Explanation:** The email separates two approvals that a hasty reader merges. The director is "content for the team to proceed to build" — build approval is given. But for the board: "Before I can present this to the programme board with confidence, I need either a credible fallback option or evidence that the provider's March date is dependable" — presentation is explicitly conditional on work not yet done. The statement claims board-presentation approval has been given; the text contradicts it. Managing stakeholder expectations depends on registering exactly this kind of split decision: partial green light, conditional amber.

**Question 7 (moderate).** True, False, or Cannot Say: The payments provider's new API will be delayed beyond March.

**Correct answer: Cannot Say.**

**Explanation:** The director's sentence is a conditional: "if their new API is delayed beyond March, our statutory deadline is at risk". A conditional asserts a consequence, not the occurrence of its trigger. The email expresses concern about the possibility of delay and notes the absence of contingency, but nowhere states that delay will happen or is likely. Neither confirmed nor contradicted: Cannot Say. Assessments repeatedly test whether candidates read "if X then Y" as "X is true" — a misreading with obvious costs when you relay stakeholder positions onward.

**Question 8 (challenging).** True, False, or Cannot Say: The accessibility question must be resolved before the build starts.

**Correct answer: False.**

**Explanation:** The email's final clause is precise: "I'd also welcome your view on whether the caching approach affects our accessibility commitments, though this need not block the build starting." The statement claims the accessibility question must be resolved pre-build; the text says it "need not block the build starting" — a direct contradiction. Notice the design of the trap: accessibility is genuinely important, both to the director (who raises it) and to UK public sector values, and a values-driven reader may promote it to a blocker. Verbal reasoning rewards reading what the stakeholder actually said; your professional judgement about what they *should* have said belongs in your reply, not in your comprehension.

**Question 9 (challenging).** Which single action would most directly satisfy the director's stated condition for board presentation?

A) Commissioning an accessibility audit of the caching approach.
B) Documenting a credible fallback for a delayed payments API.
C) Rerunning the security review.
D) Bringing the statutory deadline forward.

**Correct answer: B.**

**Explanation:** The stated condition is disjunctive: "either a credible fallback option or evidence that the provider's March date is dependable". Option B satisfies the first limb directly. A addresses the explicitly non-blocking question; C addresses a concern the email says is already resolved ("the security concerns from the last review have been addressed"); D is not within anyone's gift and is not requested. The question rehearses a core senior-architect skill: converting a stakeholder's prose into an actionable acceptance criterion, then doing the thing that meets it rather than the thing nearest to hand.

**Passage C — Extract from an internal assurance report:**
"The review team found that the service's technical design is broadly coherent and that the architecture decision records are of high quality. However, three of the eleven integration points lack documented failure modes, and the team was unable to demonstrate the disaster recovery procedure within the target recovery time during the observed exercise. The service team attributes the recovery overrun to an unusually configured test environment, an explanation the review team considers plausible but has not verified. The review team recommends conditional approval: the service may continue to public beta provided the failure-mode documentation is completed within eight weeks and the recovery exercise is repeated in a production-like environment before the next assessment."

**Question 10 (challenging).** True, False, or Cannot Say: The review team verified that the test environment's configuration caused the recovery overrun.

**Correct answer: False.**

**Explanation:** The passage states the review team "considers plausible but has not verified" the team's explanation. The statement claims verification occurred; the text explicitly says it has not — False. The subtlety is the two-part epistemic status: plausible (an assessment of credibility) and unverified (an assessment of evidence). Candidates who skim register only "plausible" and drift towards True or Cannot Say. Assurance work runs on exactly this distinction — what is believed versus what is evidenced — and so does this question.

**Question 11 (challenging).** True, False, or Cannot Say: The service will be permitted to enter public beta.

**Correct answer: Cannot Say.**

**Explanation:** The recommendation is conditional: "the service may continue to public beta provided the failure-mode documentation is completed within eight weeks and the recovery exercise is repeated". Two things stand between the text and the statement: first, a recommendation is not a decision — the passage does not say who accepts it or whether they have; second, even if accepted, permission depends on conditions whose fulfilment lies in the future. The passage therefore cannot confirm the statement, and nothing contradicts it either: Cannot Say. Distinguishing recommendations from decisions, and conditional permissions from permissions, is bread-and-butter reading for anyone who engages with architectural governance and assurance.

**Question 12 (challenging).** How many integration points have documented failure modes?

A) Three
B) Eight
C) Eleven
D) The passage does not say exactly.

**Correct answer: B) Eight.**

**Explanation:** "Three of the eleven integration points lack documented failure modes" — so 11 − 3 = 8 have them. The correct answer requires a small arithmetic step over precisely read figures, a hybrid the better assessments use because real documents rarely hand you the number you need directly. Option D tempts the over-cautious: the passage does say exactly, just not in the surface form of the question. Cannot-Say discipline means refusing unsupported inference — not refusing subtraction.

**Question 13 (hard).** Which statement best characterises the review team's overall position?

A) The design is fundamentally flawed and public beta should be blocked.
B) The design is sound in structure and documentation, with specific evidential gaps in failure modes and recovery, and progress should be permitted under explicit conditions addressing those gaps.
C) The design is fully approved, with minor suggestions for improvement.
D) The review team was unable to reach a conclusion.

**Correct answer: B.**

**Explanation:** Track each element back to the text: "broadly coherent" design and "high quality" decision records (sound structure and documentation); missing failure modes at three integration points and an undemonstrated recovery time (specific evidential gaps); "recommends conditional approval... provided..." (progress under explicit conditions targeting exactly those gaps). A overstates the negative findings; C erases the conditions — "conditional approval" is not approval with suggestions, because the conditions gate continuation; D contradicts the existence of a clear recommendation. Best-summary questions reward the option that preserves the document's actual weighting of positive and negative — the same fidelity you need when you brief a senior stakeholder on someone else's report and your summary becomes, in practice, the report.

**Question 14 (hard).** True, False, or Cannot Say: The failure-mode documentation must be completed before the recovery exercise is repeated.

**Correct answer: Cannot Say.**

**Explanation:** The passage sets two conditions with two different time references: documentation "within eight weeks", and the recovery exercise "before the next assessment". It never orders the two conditions relative to each other. Depending on when the next assessment falls, the exercise could precede, follow, or overlap the documentation work. The statement asserts an ordering the text does not contain, and nothing in the text contradicts the ordering either — Cannot Say. Parallel conditions with independent deadlines are common in assurance letters and contracts, and imposing an imagined sequence on them is a subtle, senior-level reading error the hardest questions are built to catch.

**Passage D — Extract from a draft cross-government technology strategy:**
"Departments should adopt a cloud-first posture for new workloads, and are expected to publish exceptions with their rationale. This strategy does not mandate any particular vendor; departments remain responsible for their own commercial decisions. Interoperability is a priority: departments planning shared services must expose capabilities through open, documented interfaces, and legacy point-to-point integrations should be retired as opportunities arise. The strategy will be reviewed annually. Nothing in this strategy overrides existing statutory obligations, including accessibility regulations, which continue to apply to all services regardless of hosting model."

**Question 15 (moderate).** True, False, or Cannot Say: The strategy requires departments to use a specific approved cloud vendor.

**Correct answer: False.**

**Explanation:** The passage is explicit: "This strategy does not mandate any particular vendor; departments remain responsible for their own commercial decisions." The statement asserts a vendor mandate; the text directly denies one — False. A careless reader might reason from real-world knowledge of framework agreements and preferred suppliers towards True or Cannot Say, but the closed world of the passage settles it. When you communicate a strategy to senior stakeholders, being able to say crisply "the strategy is silent on vendor; that decision remains ours" is a small sentence that prevents a large misunderstanding.

**Question 16 (challenging).** True, False, or Cannot Say: A department planning a shared service must retire its legacy point-to-point integrations before launching the shared service.

**Correct answer: False.**

**Explanation:** Two different obligations sit side by side in the interoperability sentence, with two different strengths. Shared services "must expose capabilities through open, documented interfaces" — a hard obligation. Legacy point-to-point integrations "should be retired as opportunities arise" — a soft expectation with an explicitly opportunistic timeline. The statement welds them together into a hard precondition ("must retire... before launching"), which the text contradicts twice over: retirement is "should", not "must", and its timing is "as opportunities arise", not "before launch". Reading paired obligations at their stated strengths — and refusing to let the stronger one bleed into the weaker — is precisely the skill of using architectural principles and constraints "when appropriate" rather than maximally.

**Question 17 (challenging).** Which statement best captures the relationship between this strategy and accessibility regulations?

A) The strategy introduces new accessibility requirements for cloud-hosted services.
B) The strategy exempts cloud-hosted services from accessibility regulations.
C) The strategy leaves accessibility obligations exactly as they were: statutory, and applicable to all services whatever their hosting.
D) Accessibility is out of scope and unmentioned.

**Correct answer: C.**

**Explanation:** The final sentence states: "Nothing in this strategy overrides existing statutory obligations, including accessibility regulations, which continue to apply to all services regardless of hosting model." The strategy neither adds requirements (ruling out A) nor removes them (ruling out B); it explicitly preserves the status quo, and it does mention accessibility (ruling out D). Clauses like this — savings clauses, in drafting terminology — exist to prevent a new document from being misread as disturbing older obligations, and recognising them matters when stakeholders ask you, as they will, "does the new strategy change what we have to do about accessibility?" The correct professional answer, like the correct assessment answer, is C.

**Question 18 (moderate).** True, False, or Cannot Say: Departments adopting a cloud-first posture are relieved of the need to publish exceptions.

**Correct answer: False.**

**Explanation:** The first sentence joins two expectations with "and": departments "should adopt a cloud-first posture for new workloads, and are expected to publish exceptions with their rationale". Publishing exceptions is not an alternative to cloud-first adoption; it is the companion obligation that gives the posture its transparency. The statement claims adoption removes the publication expectation — the text presents them as coexisting, so the claim contradicts the passage's plain structure: False. There is also a values dimension worth noticing: publishing exceptions with rationale is how "cloud-first" stays an honest, accountable default rather than a slogan, which is why strategies in the UK public sector phrase it this way. But the assessment answer rests on the sentence structure alone.

**Question 19 (hard).** True, False, or Cannot Say: The strategy will be revised next year.

**Correct answer: Cannot Say.**

**Explanation:** The passage says "The strategy will be reviewed annually." Reviewed is not revised: a review is an examination that may conclude no change is needed, while a revision is a change. The statement asserts that a revision will occur; the passage guarantees only that a review will. The review makes revision possible — perhaps even likely, in your experience of how strategies age — but the text neither promises nor rules out a change next year: Cannot Say. This near-synonym substitution ("reviewed" → "revised", "recommended" → "required", "plausible" → "confirmed") is the signature move of hard verbal reasoning items, and of imprecise minute-taking in governance meetings. Senior architects who quote documents exactly, rather than paraphrasing them from memory, avoid both traps at once.

### Preparation tips

- **Drill the three-way distinction.** True requires textual support; False requires textual contradiction; everything else — however plausible, however consistent with your experience — is Cannot Say. Say the definitions to yourself before the test starts.
- **Underline modal verbs and scope words.** "Must", "may", "should", "only", "all", "any", "provided that", "need not" — these words decide most answers (see Questions 1, 5, and 8). Train your eye to snag on them.
- **Respect conditionals.** "If X then Y" tells you nothing about whether X holds (Question 7). Recommendations are not decisions, and conditional approvals are not approvals (Question 11).
- **Read the statement before rereading the passage.** With under a minute per question, scan the passage once for structure, then let each statement send you back to the specific clause it tests. Hunting keywords beats rereading.
- **Suspend your expertise deliberately.** You know how betas, accreditations, and DPIAs really work; the passage may not match your knowledge, and the passage wins. Treat each passage as a closed world — the same discipline you apply when the governance question is "what does the standard actually say?"
- **Practise on your real inbox.** Take a stakeholder email and write three statements about it: one True, one False, one Cannot Say. Composing the trap teaches you to see traps.

### Common pitfalls

- **Importing outside knowledge.** The most frequent error at senior level, precisely because your knowledge is extensive. Question 3 (accreditation) and Question 4 (DPIA timing) are built to punish it.
- **Confusing "unstated" with "false".** A passage's silence about Platform Two's accreditation does not make claims about it false — it makes them Cannot Say.
- **Confusing "contradicted" with "cannot say".** When the text explicitly negates an obligation ("not required to migrate"), a statement asserting the obligation is False, not Cannot Say (Question 2).
- **Merging split decisions.** Stakeholder texts often approve one thing and withhold another (Question 6). Summarising "content to proceed to build" as "approved" is how expectations get mismanaged.
- **Promoting values into text.** Accessibility and safety matter deeply, but the question asks what the document says (Question 8). Keep your comprehension and your advocacy in separate registers.
- **Imposing an order on parallel conditions.** Two obligations with separate deadlines are not sequenced unless the text sequences them (Question 14).
- **Poor time allocation.** Spending three minutes perfecting one Cannot Say while four easy questions expire unread costs more than any single wrong answer.

## Workplace job-specific situational judgement assessment

### About this assessment

A workplace job-specific situational judgement assessment evaluates your decision-making, interpersonal effectiveness, and professional conduct through realistic workplace dilemmas. Unlike the reasoning tests, it has no single objectively right answer: several responses may seem reasonable, and the scoring reflects how well your choices align with the values and behaviours the organisation needs from the role — in your case, the values of the UK public sector: user needs first, transparency, collaboration, accessibility, and inclusion.

Typical formats ask you either to select the **most effective** and **least effective** responses from a set, or to rank or rate every option from best to worst. Timing is usually untimed or generous, because the assessment targets your natural judgement rather than your speed. The scenarios are drawn from the genuine pressure points of the role — and for a senior technical architect, those pressure points are people-shaped: finding agreement with senior stakeholders while providing direction and challenge; being honest about problems early; protecting architectural coherence without becoming a bottleneck; mentoring junior colleagues; and keeping communities of practice healthy.

This assessment deserves your attention even if — especially if — the reasoning tests hold no fear for you. At senior levels, careers are rarely limited by cognitive horsepower; they are shaped by judgement under social and political pressure. The scenarios below rehearse the exact dilemmas your role profile implies: challenging a senior stakeholder's pet solution, surfacing a risk nobody wants to hear about, handling a mentee's mistake, and arbitrating between architectural purity and delivery reality.

### What it measures for your role

- **Stakeholder direction and challenge → Architecture communication.** You regularly collaborate and find agreement with senior stakeholders, providing direction and challenge. Scenarios test whether you can disagree without rupturing the relationship, and agree without abandoning the architecture.
- **Proactive problem identification → the role's core duty.** You are expected to be proactive in identifying problems and translating them into non-technical descriptions. Scenarios test whether you surface bad news early, clearly, and constructively.
- **Mentoring and coaching → the role's leadership duty.** You mentor and coach junior colleagues. Scenarios test how you respond to a mentee's errors, growth, and visibility.
- **Team and community health → Community collaboration.** You use Agile health checks to identify issues in team dynamics and help stimulate the right responses, and you adapt feedback so it is effective and lasting. Scenarios test facilitation, feedback, and inclusion.
- **Risk and governance judgement → Making architectural decisions.** You engage with governance and assurance to manage decisions and risks. Scenarios test escalation timing, exception handling, and the balance between autonomy and assurance.

### Practice questions

**Question 1 (moderate) — The director's pet technology.**
A programme director — senior to you, and influential over your programme's funding — announces in a steering meeting that the new case-management service "will be built on" a specific commercial platform they used successfully in a previous department. Your discovery work suggests the platform fits poorly with the department's data model and would create a costly integration burden. The director asks you, in front of the meeting, to confirm the platform is a good choice. Rate the options.

A) Confirm the choice in the meeting to preserve the relationship, then work quietly to limit the platform's footprint later.
B) Say that the platform has genuine strengths, that your discovery work has raised specific integration questions you want to resolve before the architecture is fixed, and offer to bring an evidence-based options comparison to the next steering meeting.
C) State plainly in the meeting that the platform is the wrong choice and that discovery evidence contradicts the director.
D) Say nothing in the meeting and raise your concerns with the director privately afterwards.

**Most effective: B. Least effective: A.**

**Explanation:** B does everything the role profile asks at once: it provides challenge ("specific integration questions") without ambush, keeps the decision open ("before the architecture is fixed"), commits to evidence over opinion (the options comparison), and manages expectations with a concrete next step. It is respectful, transparent, and it protects the decision-making process rather than winning the moment. A is least effective because it is the only option that involves saying something you believe to be untrue: it sacrifices transparency, sets the programme on a poor course, and converts a recoverable disagreement into a future crisis — quiet subversion afterwards compounds the dishonesty and erodes trust in architecture as a function. C is honest but poorly judged: public contradiction of a senior stakeholder invites entrenchment, and "the wrong choice" overstates what discovery evidence can show at this stage. D preserves the relationship but leaves a misleading impression standing in an official meeting and delays challenge that the meeting needed to hear in some form; it is a middling option — better than A, weaker than B because it spends the meeting's decision-making value.

**Question 2 (moderate) — The risk nobody wants on the register.**
During assurance work you identify that a critical service depends on a single subject-matter expert for its legacy integration layer; if that person leaves, the programme's timeline is unsafe. The delivery manager asks you not to add this to the risk register because "it will make the team look bad and the person might see it and feel singled out." Rate the options.

A) Agree to keep it off the register, but keep a personal note of it.
B) Add the risk to the register without telling the delivery manager.
C) Explain that unrecorded risks cannot attract mitigation or funding, work with the delivery manager to word the risk factually and without naming the individual (framing it as a resilience and knowledge-sharing need), and ensure the person is engaged positively — for example, through paired work and documentation time that develops others.
D) Escalate the delivery manager's request to their line manager as an attempt to suppress a risk.

**Most effective: C. Least effective: A.**

**Explanation:** C achieves the substantive goal — the risk is visible and mitigable — while genuinely addressing the delivery manager's concerns rather than overriding them: careful wording protects the individual, and the proposed mitigation (pairing, documentation) turns a personnel vulnerability into a development opportunity, which reflects the collaborative and inclusive values the assessment is scoring. A is least effective: an unrecorded risk on a critical service is unmanaged risk, and a private note satisfies neither transparency nor governance — if the expert resigns, the organisation discovers both the risk and the concealment. B gets the risk recorded but by circumventing a colleague, damaging the trust that community collaboration depends on and guaranteeing a harder conversation later. D is disproportionate as a first move: the delivery manager expressed a concern, however misdirected; escalation before dialogue treats a colleague as an adversary and spends senior attention on a problem you were equipped to solve. Escalation belongs in your toolkit — but after C fails, not instead of trying it.

**Question 3 (moderate) — The mentee's public mistake.**
A junior architect you mentor presented a design to a cross-team forum yesterday. Today you discover the design contains a significant flaw: it assumes an API contract that the upstream team has already deprecated. Several teams are now planning against the flawed design. Rate the options.

A) Correct the design yourself and circulate the fixed version, without involving the mentee, to resolve the situation quickly.
B) Tell the mentee about the flaw, help them understand how to verify contract status in future, and support them to issue the correction to the forum themselves promptly — offering to join them if they want backing.
C) Wait until your next scheduled mentoring session in two weeks to raise it as a learning point.
D) Mention the flaw to the forum chair and suggest the design be quietly dropped from the agenda.

**Most effective: B. Least effective: C.**

**Explanation:** Two clocks are running: teams are planning against a flawed design now (an operational problem), and a mentee's development moment is available now (a coaching opportunity). B is the only option that serves both. The correction happens promptly and transparently; the mentee learns the underlying verification habit rather than just the fact of this error; and issuing the correction themselves — with backing available — builds the credibility and resilience that mentoring is for. Making feedback effective and lasting, as your community collaboration skill puts it, means exactly this: timely, specific, and delivered in a way that grows the person. C is least effective because it fails both clocks: teams continue building on a deprecated contract for two weeks, and the feedback arrives cold, detached from the moment it could teach. A fixes the artefact but disempowers the mentee — being publicly corrected by one's mentor without warning teaches fear, not verification — and it spends senior capacity on work a junior colleague could own with support. D is worse than A on transparency (problems are handled "quietly" rather than openly) while still abandoning the mentee, though it at least stops the flawed planning; it sits between A and C.

**Question 4 (challenging) — Architecture purity versus statutory deadline.**
A delivery team must meet a statutory deadline in ten weeks. Their proposed shortcut — writing case data directly into the reporting database, bypassing the event stream your target architecture mandates — would save four weeks but create exactly the kind of point-to-point coupling your organisation's strategy is retiring. The team asks for your support at the design authority. Rate the options.

A) Refuse: the target architecture exists precisely to prevent this, and exceptions erode it.
B) Support the shortcut unconditionally: statutory deadlines outrank architectural preferences.
C) Support a time-boxed, documented exception: the shortcut proceeds behind a clearly owned interface where feasible, an ADR records the decision, its rationale, and the remediation plan, and a funded work item to restore the event-stream pattern is agreed before you endorse it at the design authority.
D) Ask the design authority to decide without offering a recommendation, since both sides have merit.

**Most effective: C. Least effective: D.**

**Explanation:** This is the senior architect's signature dilemma, and the assessment is looking for managed risk rather than either absolutism. C treats the exception as what it is — a conscious, priced, reversible decision: time-boxed (so "temporary" has a definition), documented in an ADR (so the organisation learns and the debt is visible), and funded for remediation (so "we'll fix it later" is a plan, not a hope). This is "architectural design decisions characterised by managed levels of risk and complexity" made concrete, and it uses governance as a tool for managing the decision rather than a gate to be fought. A is principled but misses that architecture serves outcomes: a missed statutory deadline harms real users and, ironically, discredits the architecture function's judgement. B concedes everything and books none of the debt: unconditional support creates permanent coupling under temporary pressure. D is least effective because it is an abdication — you are the design authority's expert advisor on exactly this question; arriving without a recommendation withholds the analysis the forum exists to receive, providing neither direction nor challenge. Senior stakeholders can forgive a recommendation they overrule; they remember an advisor who would not advise.

**Question 5 (challenging) — The failing community of practice.**
You lead the architecture community of practice. Attendance has halved over four months. A quiet survey reveals: two vocal members dominate discussions; junior members feel their questions are "too basic" for the forum; and sessions have drifted into status reporting rather than problem-solving. Rate the options.

A) Cancel the community of practice; attendance shows it has run its course.
B) Email the two vocal members telling them to contribute less.
C) Redesign the format with the community: rotate facilitation, introduce structured formats that share airtime (such as lean coffee or lightning talks), create an explicit space where foundational questions are welcomed, and speak privately and appreciatively with the two dominant members about using their expertise to draw others out.
D) Keep the format but personally invite junior members and reassure them their questions are welcome.

**Most effective: C. Least effective: A.**

**Explanation:** The survey gives you three distinct causes; C is the only option that treats all three, and it does so with the community rather than to it — which matters, because a community of practice that has a format imposed on it is not a community. Rotating facilitation and structured formats fix the airtime problem systemically rather than personally; an explicit home for foundational questions addresses the inclusion failure (junior colleagues feeling unwelcome is an inclusion issue, not a curriculum issue); and the private conversations convert the dominant members from problem to asset, which is what "adapt feedback to ensure it's effective and lasting" looks like with senior peers. This is the community collaboration skill in full: identifying issues in group dynamics and helping to stimulate the right responses. A is least effective — it reads a symptom (falling attendance) as a verdict, destroying a mechanism your role depends on for aligning architects across the organisation, without trying a single remedy. B addresses one cause, bluntly and by email: feedback that is public-adjacent, unexplained, and framed as suppression tends to create resentment rather than change. D is warm but structural-blind: reassured juniors returning to an unchanged forum will have their reassurance disproved within two sessions.

**Question 6 (challenging) — Discovering the strategic misalignment late.**
Reviewing another programme's plans in your role as an assuring architect, you notice their flagship service is building a bespoke identity solution, while your department has committed publicly to adopting the cross-government identity platform within two years. The programme is six months into build. Their architect — a respected peer — tells you privately: "We know. Our director decided the shared platform's roadmap was too risky for our dates. Please don't make this a thing." Rate the options.

A) Respect the confidence and leave it out of your assurance findings; their director made a considered decision.
B) Record the divergence factually in your assurance findings, tell your peer beforehand exactly what you will write and why, and recommend the divergence be surfaced to the departmental design authority so the roadmap conflict is decided at the right level — noting the director's dates-versus-risk rationale fairly.
C) Immediately inform the departmental CTO that the programme is defying strategy.
D) Advise your peer to quietly add a migration layer so the divergence becomes less visible in future reviews.

**Most effective: B. Least effective: D.**

**Explanation:** The conflict here is between loyalty to a peer and integrity of assurance — and B shows they are reconcilable. The finding is recorded (assurance that omits known material divergences is not assurance); the peer is treated with respect (no surprises — they hear exactly what will be written and why); the director's rationale is represented fairly (the dates-versus-risk trade-off is a legitimate concern, not defiance); and the decision is routed to the level that owns it, because a two-year departmental commitment versus one programme's delivery dates is precisely what design authorities exist to arbitrate. This is aligning your work with other architects, engaging governance to manage risk, and identifying how other teams' work affects shared outcomes — three skills from your profile in one move. D is least effective: it uses your architectural knowledge to help conceal a divergence from future assurance — a corruption of the assuring role that damages the trust every future review depends on. A is a softer version of the same failure: a considered decision by a director can still be a decision the department needs to see. C is honest but skips the craft: escalating instantly, over your peer's head, without the factual write-up or the fair representation of rationale, maximises heat and minimises the chance of a good decision — and makes every future programme hide things from you earlier.

**Question 7 (challenging) — The roadmap collision.**
Your technology roadmap retires the department's ageing integration platform in 18 months. You learn that a neighbouring directorate has just signed a three-year support contract for the same platform and plans to onboard two new services to it, because nobody told them about the retirement. Their head of technology is defensive when you raise it: "We committed in good faith. Unpicking this now would embarrass us with the supplier." Rate the options.

A) Proceed with your retirement timeline as published; their contract is their problem.
B) Extend the platform's life by three years to match their contract, quietly amending your roadmap.
C) Acknowledge the process failure openly (the roadmap's communication clearly failed them), then convene a joint session to map the options — contract break clauses, a scoped carve-out for their two services with a defined migration date, or a negotiated retirement extension with shared costs — and take the recommendation to the body that owns the roadmap, with the communication gap logged as a lesson.
D) Ask your director to instruct their directorate to comply with the roadmap.

**Most effective: C. Least effective: A.**

**Explanation:** Notice what C does first: it concedes the legitimate half of the other side's position. The directorate did commit in good faith, and the roadmap's owners did fail to communicate — acknowledging this converts a defensive stakeholder into a partner, which is the practical meaning of "regularly collaborate and find agreement with senior stakeholders". C then does the architectural work: laying out real options with their costs, refusing to pretend the collision has a free resolution, and routing the decision to the roadmap's owning body rather than settling it bilaterally — because a three-year divergence affects everyone who plans against that roadmap. Logging the communication failure closes the loop for next time; tracking how change lands across other teams is architecting for the whole context. A is least effective: it is procedurally defensible and practically ruinous — two new services onboard to a dying platform, the eventual migration costs multiply, and the relationship is spent just when you need it. B avoids conflict by silently degrading the strategy: a roadmap amended "quietly" under pressure stops being a roadmap anyone can trust. D outsources a solvable disagreement upward at maximum interpersonal cost and before options exist for anyone to decide between; like all escalation-first options, it belongs later in the sequence, if C fails.

**Question 8 (challenging) — Accessibility versus launch pressure.**
Two weeks before a high-profile public beta, an accessibility audit finds that the service's document-upload journey is unusable with screen readers — traceable to a third-party component your technical design selected. The programme director proposes launching on schedule and fixing accessibility "in the first month of beta", noting the political cost of a delay. As the senior technical architect who owns the design, rate the options.

A) Support the on-time launch; accessibility can genuinely be fixed in beta, and beta exists to find issues.
B) State clearly that launching a journey unusable by screen-reader users excludes disabled users from a public service and creates legal exposure under accessibility regulations; propose the least-delay compliant path — such as launching with an accessible alternative route for document upload (an assisted-digital or alternative-format channel) while the component is replaced — and put the decision, with options and risks, to the director formally.
C) Say the launch decision is the director's to make and confine yourself to fixing the component.
D) Contact the audit team and ask whether the finding can be reclassified as medium severity so the launch can proceed.

**Most effective: B. Least effective: D.**

**Explanation:** B is what senior technical leadership looks like under political pressure. It names the issue in its true terms — exclusion of disabled users from a public service is a user-needs and legal matter, not a technical nicety — because translating problems into non-technical descriptions that can be widely understood is your explicit duty. It then does the constructive work: engineering the least-delay compliant option rather than presenting a binary of "launch inaccessibly or slip". And it locates the decision correctly — formally, with the director, on an honest risk picture. D is least effective and is the only option that corrupts evidence: pressuring auditors to reclassify a finding attacks the integrity of the assurance system itself, and a senior architect who does it once has taught every auditor to distrust them permanently. A misunderstands beta: beta exists to find unknown issues, not to ship known exclusions of a protected group; "fix it in beta" for a known accessibility failure inverts the public sector's inclusion commitment. C is technically industrious but abdicates leadership — the director's decision rights are real, but they are owed your professional assessment of the consequences, stated plainly; silence from the design's owner will be read, later, as assent.

**Question 9 (hard) — The stretched team's health check.**
An Agile health check you facilitate for a delivery team you architect for shows collapsing scores on "confidence in technical direction" and "sustainable pace", with comments blaming "constantly changing architectural guidance". You recognise some changes as your own: three revisions to the integration approach in four months, each responding to genuine external shifts. The delivery manager suggests skipping the readout session "since morale is already low". Rate the options.

A) Hold the readout; open it by acknowledging your own contribution to the churn, explain briefly the external drivers behind each revision, and facilitate the team towards concrete stabilising actions — such as a commitment period during which the integration approach is frozen barring defined triggers, and a lightweight change note whenever guidance shifts.
B) Skip the readout as suggested and simply stop revising the guidance for a while.
C) Hold the readout but present the survey data without comment on the architecture guidance, steering discussion towards pace and workload topics.
D) Hold the readout and explain to the team why each architectural revision was necessary and correct, so they understand the changes were justified.

**Most effective: A. Least effective: B.**

**Explanation:** Your community collaboration skill names this exact situation: identify issues through Agile health checks and help stimulate the right responses. A models everything the moment requires. Owning your contribution first makes it safe for everyone else to be honest — psychological safety is created by example, and a senior figure self-assessing candidly is the strongest signal available. Explaining the external drivers briefly gives the team the context that turns "chaotic architect" into "volatile environment", without becoming a defence. Most importantly, A converts feedback into structure: a freeze period with defined triggers and change notes addresses both failing scores — direction confidence and pace — with mechanisms, not reassurance. B is least effective twice over: cancelling a readout because the results are bad teaches the team that the health check is theatre (destroying the instrument), and silently stopping revisions addresses churn by accident, without the team ever seeing cause and effect. C holds the meeting but dodges its subject; teams notice steering, and unaddressed elephants grow. D attends to the right topic in the wrong register — a justification session treats the team's experience as a misunderstanding to be corrected, when the feedback ("effective and lasting", as your skill puts it) needed to flow towards you first.

**Question 10 (hard) — The strategy you inherit and doubt.**
You join a programme as its senior technical architect. Its published technical strategy — authored by your predecessor and endorsed by the CTO — commits to decomposing the monolithic case system into twelve microservices. After a month, your assessment is that the team's size and operational maturity can realistically support four services, and that pursuing twelve will fail slowly and expensively. The team is already three services into the decomposition. Rate the options.

A) Implement the strategy as endorsed; re-litigating a CTO-endorsed decision in your first months would undermine confidence.
B) Announce that the strategy is wrong and halt further decomposition while you write a replacement.
C) Continue the in-flight work while you assemble the evidence — operational metrics from the three delivered services, team cognitive-load and on-call data, comparable case studies — then take a revised proposal ("consolidate at four to six services, with defined criteria for further splitting") through the strategy's own governance route, engaging the CTO with the reasoning before the formal session.
D) Quietly steer the team to slow-walk the remaining decomposition so the strategy fails softly without a confrontation.

**Most effective: C. Least effective: D.**

**Explanation:** Your strategy design skill is explicit that you "challenge requirements and assumptions, and identify opportunities to develop strategy" — a published strategy is not exempt from that duty just because it is endorsed and inherited. C challenges it the way strategies deserve to be challenged: with evidence rather than opinion (the three delivered services are now data), through the governance route that gives a revision legitimacy, and with the CTO engaged early enough that the formal session confirms understanding rather than springing surprise — that is finding agreement with senior stakeholders, done properly. The proposal itself is good strategy design: a target with criteria ("four to six, with defined splitting triggers") rather than a new dogma to replace the old one. A confuses deference with alignment: implementing a plan you believe will fail, without voicing that belief, serves nobody — least of all the CTO whose endorsement was made on older information. B has the right conviction and the wrong method: an announcement-and-halt in your first months, before evidence is assembled, spends credibility you have not yet earned and disrespects the governance that endorsed the strategy. D is least effective because it is the only dishonest option: engineering quiet failure avoids the confrontation by deceiving everyone — the team, the CTO, and the strategy's governance — and when discovered (slow-walking always is), it ends trust in you specifically. Strategies are revised in the open or they rot.

**Question 11 (hard) — Credit and visibility for the mentee.**
Your mentee co-designed, with you, an elegant approach to a difficult data-migration problem — the core insight was theirs. A deputy director, impressed, asks you to present the approach at a cross-department architecture forum, a visible career moment. The forum's convention is a single senior presenter. Rate the options.

A) Present it yourself, crediting the mentee verbally during the talk.
B) Reply proposing the mentee co-present or present with you introducing them, explaining that the core insight was theirs and that the forum benefits from hearing the designer directly; prepare them thoroughly for the session.
C) Decline the invitation and tell the deputy director to invite the mentee instead.
D) Present it yourself without dwelling on attribution; team output is collective.

**Most effective: B. Least effective: D.**

**Explanation:** Mentoring and coaching junior colleagues is in your role profile at this level, and sponsorship — spending your visibility to create theirs — is mentoring's most valuable and least practised form. B does it well: it corrects the attribution to the person who controls the platform (the deputy director), negotiates the forum's convention rather than merely obeying or defying it, keeps you present as introducer and safety net (appropriate for a cross-department stage the mentee has not stood on before), and invests in preparation so the opportunity lands as a success rather than an exposure. A is the comfortable middle: verbal credit is genuinely better than nothing, but the career-visible act — being the presenter — stays with you, and "credited in someone else's talk" builds no platform. C has generous intent but overshoots: declining outright may read as slighting the deputy director's invitation, removes the support structure a first big presentation benefits from, and — notice — hands the mentee an outcome without asking what they want or preparing them for it. D is least effective: "team output is collective" is, in this use, a rationalisation for taking individual credit for a junior colleague's insight — the exact inversion of the mentoring duty, and corrosive to the trust on which your future influence with every junior architect depends. Inclusion values are scored here too: whose voices get platforms is an inclusion question.

**Question 12 (hard) — Most and least, under time pressure.**
A security review of a partner department's connected service reveals a vulnerability that also affects your service through a shared component — details are embargoed by the partner until their fix ships in three weeks. Meanwhile your own service's public beta launches in one week, and your launch assessment requires you to declare known security risks. The embargo agreement was made at director level. Select the MOST and LEAST effective actions.

A) Declare nothing at the launch assessment; the embargo binds you, and the risk originates elsewhere.
B) Break the embargo and give the launch assessment full technical details, since transparency is a public sector value.
C) Immediately engage your security lead and the director who agreed the embargo: establish what can be disclosed to the assessment under confidentiality (for example, the existence, severity, and mitigation status of a vulnerability in a shared component, without exploitable detail), assess interim mitigations for your service, and if risk to citizens is material, seek an accelerated coordinated disclosure or a launch delay.
D) Postpone your launch by a month without explanation, to be safe.

**Most effective: C. Least effective: A.**

**Explanation:** The question stages a collision between two legitimate obligations — coordinated vulnerability disclosure (embargoes protect users of the vulnerable component everywhere) and honest assurance (a launch assessment that does not hear about a known material risk is a false assurance). C refuses to accept the collision as binary. Nearly every real embargo permits controlled disclosure to those with a need to know under confidentiality; severity-without-detail is the standard mechanism, and the security lead and embargo-owning director are exactly the people who can authorise it inside the agreement rather than around it. C also does the architect's substantive work — interim mitigations for the shared component — and holds open the honest last resort: if citizens would be materially exposed, the launch moves, not the truth. A is least effective: it converts an embargo on technical detail into a licence to mislead your own governance, and "the risk originates elsewhere" is untrue in the way that matters — your service carries the vulnerable component, so your users carry the risk. B honours one value by destroying another: breaking a director-level embargo unilaterally harms the partner's users (the fix is not out), your department's trustworthiness in future disclosures, and was unnecessary given C's existence. D reaches a possibly-right outcome (delay) by an indefensible route: unexplained, unilateral, and leaving the assessment none the wiser — decisions this large are made with governance, not for it.

### Preparation tips

- **Anchor on the role's values, not your instincts alone.** Before practising, write down the five commitments that recur in every strong answer above: users first, transparency over comfort, evidence over opinion, decisions at the level that owns them, and people developed rather than protected. Scenario options that sacrifice one of these are rarely "most effective".
- **Look for the option that does two jobs.** The best answers typically resolve the operational problem and the relationship or development problem in one move (Questions 3, 5, 9). If an option fixes the artefact but damages the person, keep looking.
- **Sequence before escalating.** Escalation is legitimate — but options that escalate before dialogue, or decide before assembling options, are consistently scored below those that try the direct, evidenced route first (Questions 2, 6, 7).
- **Beware the dishonest shortcut in senior clothing.** The least effective option is often not the lazy one but the politically smooth one: confirming what you do not believe, reclassifying a finding, slow-walking a strategy. Name the deception and the option eliminates itself (Questions 1, 8, 10).
- **Read the question's format carefully.** "Most and least effective" is not a ranking of all options; spend your effort on the two poles. Where full ranking is required, the middle positions usually separate "honest but clumsy" from "kind but structurally blind".
- **Rehearse out loud.** For each scenario, say your reasoning in two sentences as if to a colleague. Judgement that cannot be articulated tends to drift under pressure; articulated judgement stabilises.

### Common pitfalls

- **Answering idealistically rather than effectively.** "Refuse all compromise on architecture" and "always be maximally transparent immediately" both sound principled and both fail real dilemmas (Questions 4, 12). The assessment rewards workable integrity, not slogans.
- **Selecting passive or deferring options.** Waiting for the scheduled mentoring session, offering no recommendation to the design authority, skipping the difficult readout — options that delay action or pass the problem onward score poorly at every level, and worse at yours (Questions 3, 4, 9).
- **Ignoring the values context.** These scenarios are set in the UK public sector: user needs, accessibility, and inclusion are scoring criteria, not scenery (Questions 8, 11). An option that is commercially astute but excludes users will not be "most effective".
- **Over-escalating.** Senior candidates sometimes treat escalation as decisiveness. Options that go over a colleague's head before speaking with them read as political, and are placed below dialogue-first options (Questions 2, 6, 7).
- **Protecting people from information.** Keeping risks off registers, softening audit findings, skipping bad-news meetings — the protective instinct is human and consistently scored least effective, because unshared information cannot be managed (Questions 2, 8, 9).
- **Forgetting you are the expert in the room.** At this level, withholding your recommendation is not humility; it is the withdrawal of the service you exist to provide (Question 4).

## Conclusion

You have now worked through four full assessment types, each grounded in the real substance of your role: cognitive reasoning over decision records, dependency chains, and risk registers; numeric reasoning over budgets, capacity figures, availability targets, and supplier pricing; verbal reasoning over standards, stakeholder correspondence, assurance reports, and strategy documents; and situational judgement across the stakeholder, mentoring, governance, and community dilemmas that define senior architectural work.

Notice what the four sections have in common. Every strong answer came from the same small set of habits: read exactly what is written, deduce only what follows, quantify before you conclude, surface problems early and honestly, route decisions to the level that owns them, and develop the people around you as deliberately as you develop the architecture. These are not test-taking tricks — they are the working habits of an effective senior technical architect, which is precisely why well-designed assessments sample them.

If some questions caught you out, treat that as useful information rather than a verdict. A missed Cannot Say suggests tightening how you quote documents in governance settings; a missed expected-value calculation suggests rehearsing the arithmetic of risk before your next board paper; a situational judgement disagreement is worth discussing with a trusted peer — sometimes the model answer is teaching you, and sometimes your dissent is the beginning of a genuinely better option worth articulating.

For continued development: revisit this material in a month and note which errors have disappeared; practise under stricter timing once accuracy is stable; and consider using these formats in your own mentoring — writing a good situational judgement scenario for a junior architect will sharpen your judgement as much as theirs. Your role profile expects you to mentor and coach, and assessment literacy is a gift worth passing on.

Whether you are preparing for a specific selection process, a promotion board, or simply keeping your professional edge sharp, you now have a realistic, role-specific practice resource — and, more importantly, a mirror for the reasoning habits your work runs on. Approach the real thing rested, unhurried, and confident. You reason about complex, risky systems for a living; an assessment is a small one. Good luck — you are better prepared than most.
