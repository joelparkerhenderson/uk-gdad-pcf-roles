# Technical Architect (Principal Technical Architect) - Psychometric Assessment Resources

## Introduction

Welcome. This document is a practical, encouraging companion for you as a principal technical architect preparing for workplace psychometric assessments. Whether you are applying for a new post, preparing for an internal progression board, or simply investing in your own professional development, everything here is built around the realities of your role: leading at the highest level, making sure technical strategy is agreed and followed, networking with senior stakeholders across organisations, supporting multiple teams with best practice and emerging technologies, and taking responsibility for governance and for solving complex, high-risk issues.

Psychometric assessments are structured, standardised exercises that measure the mental processes and judgement a role genuinely requires. For a principal technical architect, that means far more than abstract puzzles. Well-designed assessments at your level probe how you reason about interdependent systems and strategies, how you interpret programme budgets, capacity figures, and supplier cost models, how precisely you read standards, policy, and stakeholder correspondence, and how you exercise judgement in politically sensitive, high-risk situations — mediating difficult architectural discussions, evolving governance, and inspiring other architects. Employers across the UK public sector use these assessments because they are evidence-based predictors of performance and because they make selection fairer and more consistent — values that align closely with the Government Digital and Data profession's commitment to openness and inclusion.

This document is organised into four main assessment sections, each following the same structure:

- **Workplace job-specific cognitive assessment** — pattern recognition, logical deduction, error checking, prioritisation, and problem solving using the artefacts you handle every day: architecture decision records, technology strategies, governance schedules, dependency maps, and risk registers.
- **Workplace job-specific numeric reasoning assessment** — programme budgets, supplier cost comparisons, cloud capacity planning, performance metrics, and transformation business cases, with the arithmetic worked through in full.
- **Workplace job-specific verbal reasoning assessment** — dense, role-relevant passages drawn from standards, strategies, governance terms of reference, and senior stakeholder correspondence, followed by True / False / Cannot Say and comprehension questions.
- **Workplace job-specific situational judgement assessment** — realistic dilemmas involving senior stakeholders across organisations, the architects you coach and inspire, delivery teams you support, suppliers, and governance boards, with detailed discussion of why each response option is stronger or weaker.

Each section explains what the assessment measures, maps it explicitly to the skills in your role profile — architect for the whole context, architecture communication, community collaboration, making architectural decisions, strategy design, and technical design throughout the life cycle — then provides substantial practice questions with worked explanations, and closes with preparation tips and common pitfalls.

How should you use this document? Three ways. First, as practice: attempt each question under light time pressure before reading the explanation. Second, as self-reflection: notice which question types feel effortful, because that tells you where to focus. Third, as preparation: in the days before a real assessment, revisit the tips and pitfalls so the formats hold no surprises. You already operate at the most senior technical level; treat this as a structured rehearsal of thinking you do every day, made explicit and measurable. Good luck — and enjoy the practice.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive assessment measures the exact mental processes your role demands, using practical scenarios and data rather than abstract puzzles. Unlike a generic intelligence test, every question mimics the everyday tasks and artefacts of the job: for you, that means architecture decision records, technology strategies and roadmaps, governance board papers, dependency diagrams, standards compliance matrices, risk registers, and the design documents produced by the multiple teams you support.

These assessments are typically delivered online, timed at around 15 to 30 minutes, and objectively scored against a benchmark or norm group. Some platforms use adaptive testing, adjusting question difficulty based on your previous answers, and most provide short, ungraded practice questions first so the interface holds no surprises. Employers usually receive a breakdown of speed versus accuracy rather than a single score, so working carefully and steadily matters as much as working fast.

For a principal technical architect, the cognitive assessment matters because your role is fundamentally about structured reasoning under constraint at organisational scale. You make and guide architectural design decisions characterised by high levels of risk and complexity. You are responsible for making sure the technical strategy is agreed and followed, which means detecting when a team's design quietly diverges from it. You track emerging internal and external issues over time that could affect the work of teams across the organisation, which requires spotting patterns early in incomplete signals. You lead and evolve architectural governance and assurance, which requires applying rules consistently and noticing when the rules themselves conflict. A well-designed cognitive assessment samples precisely these processes: deduction from governance rules, pattern recognition across programme data, error checking in high-stakes documents, and prioritisation across competing demands from multiple teams.

### What it measures for your role

The assessment dimensions map directly to the skills named in your role profile:

- **Logical deduction and inference** maps to **making architectural decisions**: reasoning from constraints, standards, and dependencies to a sound conclusion where risk and complexity are high, and identifying and addressing architectural risks across the organisation or wider government.
- **Pattern recognition** maps to **architect for the whole context**: tracking emerging internal and external issues over time that could affect the work of teams across the organisation, and recognising recurring structures and trends across programmes so you can act before problems crystallise.
- **Error checking** maps to **technical design throughout the life cycle**: reviewing technical designs characterised by high risk, impact, and complexity produced by the teams you lead and guide, and using feedback to optimise and refine standards — which requires spotting inconsistencies between a design document, its diagrams, and the standards it claims to meet.
- **Prioritisation and problem solving** map to **strategy design** and to your leadership duties: defining and connecting strategies across the organisation, deciding where your attention and advocacy will do the most good, removing blockers, and supporting multiple teams simultaneously.
- **Rule application** maps to your responsibility for **governance**: leading and evolving architectural governance and assurance, and representing architectural governance as part of wider governance, for example legal or commercial.

### Practice questions

Work through these under light time pressure — around two to three minutes per question — then read the explanation carefully, even where you answered correctly. The reasoning path is the real content.

**Question 1 (easy) — Logical deduction from governance rules**

Your organisation's architecture governance framework contains these rules:

- Rule 1: Any solution handling citizen personal data must complete a Data Protection Impact Assessment (DPIA) before technical design assurance.
- Rule 2: Any solution with projected annual running costs above £1 million must be approved by the Investment Board before technical design assurance.
- Rule 3: Technical design assurance must be completed before any solution enters public beta.

A programme in your portfolio proposes a citizen-facing benefits eligibility service with projected annual running costs of £1.3 million. Its DPIA is complete and the Investment Board has approved it, but technical design assurance is booked for next month. The delivery team wants to enter public beta this week.

Which statement is correct?

A) The service may enter public beta because both the DPIA and Investment Board approval are complete.
B) The service may not enter public beta because technical design assurance has not been completed.
C) The service may enter public beta if the DPIA is re-validated first.
D) The rules do not apply because the service is still in beta.

**Correct answer: B.**

**Explanation:** Rule 3 is unconditional: technical design assurance must be completed before any solution enters public beta. The DPIA (Rule 1) and Investment Board approval (Rule 2) are prerequisites for assurance, not substitutes for it. Option A confuses completing the prerequisites with completing assurance itself. Option C invents a re-validation mechanism that appears nowhere in the rules. Option D misreads the scope: "public beta" is exactly the phase Rule 3 governs. As the architect responsible for governance, your job in the real workplace would be the same as in this question — hold the line on the sequence while helping the team find the fastest legitimate route through it.

**Question 2 (easy) — Pattern recognition in operational signals**

You track monthly figures for four services on your organisation's shared platform. Unplanned outages over six months:

- Service A: 1, 1, 2, 1, 2, 1
- Service B: 0, 1, 1, 2, 3, 5
- Service C: 3, 2, 3, 2, 3, 2
- Service D: 2, 0, 2, 0, 2, 0

Which service shows the pattern most warranting proactive architectural investigation?

A) Service A
B) Service B
C) Service C
D) Service D

**Correct answer: B.**

**Explanation:** Service B shows accelerating growth: 0, 1, 1, 2, 3, 5, where each recent value roughly equals the sum of the two before it — the increments themselves are increasing. Services A, C, and D oscillate within a stable band, suggesting steady-state noise or a periodic cause. Your skill in architecting for the whole context is exactly this: tracking emerging issues over time across teams and acting before the trend becomes an incident. Extrapolating Service B's pattern suggests roughly eight outages next month if nothing changes — a strong case for you to influence colleagues now rather than after a major failure.

**Question 3 (moderate) — Deduction across a dependency chain**

Five workstreams in a legacy migration programme have these dependencies:

- The identity platform (W1) must be live before the case-working system (W2) can start migration.
- The case-working system (W2) and the document store (W3) must both complete before the citizen portal (W4) can switch over.
- The data warehouse feed (W5) depends only on the document store (W3).
- W1 is live. W3 completes in June. W2 starts migration in May and takes three months.

Which is the earliest month in which the citizen portal (W4) can switch over?

A) June
B) July
C) August
D) September

**Correct answer: C.**

**Explanation:** W2 starts in May and takes three months, so it completes at the end of July, meaning switch-over is possible in August at the earliest. W3 completes in June, which is earlier, so W2 is the binding constraint. W5 is irrelevant to W4 — a deliberate distractor testing whether you separate the dependency paths. Option A wrongly uses W3's completion alone; option B miscounts the three-month duration; option D adds unneeded slack. In real programme governance, this is critical-path reasoning: your architectural decisions about sequencing carry high risk precisely because a one-month error at this level cascades into procurement, comms, and legislative timetables.

**Question 4 (moderate) — Error checking a technology strategy summary**

A team submits a paper stating: "Our target architecture retires all four legacy systems by Q4. System Alpha's 12 integrations move to the API gateway in Q2. System Beta's 9 integrations move in Q3. System Gamma has no integrations and is switched off in Q2. System Delta's 6 integrations move in Q4. In total, the programme migrates 27 integrations to the gateway before the end of Q3."

Which statement identifies the error?

A) The total number of integrations is wrong: 12 + 9 + 6 = 27 is a miscalculation.
B) The claim about Q3 is wrong: only 21 integrations (12 + 9) migrate by end of Q3; Delta's 6 migrate in Q4.
C) System Gamma cannot be switched off in Q2 because its integrations have not moved.
D) There is no error; the paper is internally consistent.

**Correct answer: B.**

**Explanation:** The arithmetic 12 + 9 + 6 = 27 is correct, so option A fails. Gamma is stated to have no integrations, so switching it off in Q2 is consistent, eliminating option C. The error is temporal: the paper claims all 27 integrations migrate "before the end of Q3", but Delta's 6 are scheduled for Q4. Only 21 move by end of Q3. This is exactly the kind of subtle inconsistency you must catch when leading and guiding others in creating technical designs: the numbers add up, but the timeline claim contradicts the schedule. Assurance reviews live or die on this discipline.

**Question 5 (moderate) — Rule application with conflicting standards**

Your organisation mandates: (i) all new services must use the corporate single sign-on (SSO) service; (ii) services classified OFFICIAL-SENSITIVE must not depend on components hosted outside the UK; (iii) exceptions to any mandate require a decision record approved by the design authority you chair.

The corporate SSO service is currently hosted in an EU region, with UK hosting planned next year. A team is building an OFFICIAL-SENSITIVE case management service and asks how to proceed.

What is the correct governance position?

A) The team must use SSO; mandate (i) takes precedence because it is listed first.
B) The team must not use SSO and needs no exception, because mandate (ii) overrides mandate (i) automatically.
C) The mandates conflict for this service; whichever is not followed requires an approved exception via a decision record, and the design authority must choose which risk to accept.
D) The team should delay the service until the SSO service moves to UK hosting.

**Correct answer: C.**

**Explanation:** The two mandates genuinely conflict for this service: using SSO violates the UK-hosting rule; not using SSO violates the SSO rule. Nothing in the framework says list order confers precedence (option A) or that one mandate silently overrides another (option B) — mandate (iii) exists precisely for this case: an explicit, recorded, approved exception. Option D outsources the decision to the calendar, delaying a public service without any governance decision, which is weak leadership. As the architect who leads and evolves governance, you would convene the design authority, weigh the risks (data residency versus fragmented identity), record the decision with its rationale and expiry, and probably set a condition to converge once UK hosting arrives. The cognitive skill tested is recognising that a rule system can be locally inconsistent and knowing which meta-rule resolves it.

**Question 6 (moderate) — Prioritisation across multiple teams**

It is Monday morning. You support six delivery teams. Four items compete for your day:

1. Team A's go-live is Thursday; their security architect flagged an unresolved single point of failure in the payment flow on Friday evening.
2. Team B requests a routine design review for a feature shipping next quarter.
3. Your director asks for talking points on the technology strategy for a cross-government board meeting on Wednesday.
4. Team C's architect — someone you are coaching — asks for feedback on a decision record before their design authority session tomorrow.

What is the most defensible ordering of your attention today?

A) 1, 4, 3, 2
B) 3, 1, 4, 2
C) 1, 3, 4, 2
D) 4, 1, 2, 3

**Correct answer: A.**

**Explanation:** Item 1 is highest: a single point of failure in a payment flow going live Thursday is a complex, high-risk issue — exactly what you are responsible for solving — and the earlier it is examined, the more options remain. Item 4 is second because it is genuinely time-bound (the session is tomorrow), it is a coaching commitment, and a modest investment today multiplies through the architect you are developing. Item 3 matters but is due Wednesday; drafting talking points today after the urgent risk work still leaves margin. Item 2 has weeks of slack. Option B elevates the director's request above a live production risk — seniority of requester is not the same as urgency or impact. Option D puts coaching above a go-live risk affecting citizens. The pattern to internalise: order by (deadline proximity × consequence of missing it), not by who asked.

**Question 7 (moderate) — Pattern recognition in incident causes**

Across the organisation, post-incident reviews over the past year attribute major incidents as follows. Q1: 2 to configuration change errors, 1 to certificate expiry, 1 to capacity. Q2: 3 to configuration change errors, 1 to capacity. Q3: 4 to configuration change errors, 1 to certificate expiry. Q4: 5 to configuration change errors, 1 to capacity.

As the principal architect tracking issues across teams, which conclusion is best supported?

A) Certificate management is the fastest-growing systemic risk.
B) Configuration change errors show a steady upward trend and are the dominant, growing systemic cause warranting an organisation-wide architectural response.
C) Capacity incidents are declining and can be deprioritised entirely.
D) Incident volume is random; no pattern is present.

**Correct answer: B.**

**Explanation:** Configuration change errors rise monotonically: 2, 3, 4, 5 per quarter — both the largest and the only growing category. Certificate expiry (1, 0, 1, 0) and capacity (1, 1, 0, 1) oscillate at low level, so options A and C over-read noise; "deprioritised entirely" in option C should also trigger suspicion, as absolute claims rarely follow from four data points. Option D ignores a clean monotonic trend. The architectural response — perhaps mandating progressive delivery, automated configuration validation, or a standard change-safety pattern across teams — is exactly the "take action to solve or mitigate problems by influencing colleagues across the organisation" behaviour in your skill profile.

**Question 8 (hard) — Deduction with negative constraints**

You are evaluating hosting options for a new cross-government platform. The constraints agreed with stakeholders are:

- If the platform uses Region North, it cannot achieve latency targets for the devolved administrations' offices.
- If latency targets are not achieved, the Scottish Government partner will not sign the collaboration agreement.
- The programme cannot proceed without the collaboration agreement.
- Region South meets latency targets but currently lacks the required security accreditation, which takes four months.
- The programme must start hosting work within six months.

Which conclusion follows necessarily?

A) The programme cannot proceed at all.
B) The platform must use Region South, and the accreditation timeline fits within the six-month window.
C) The platform must use Region North because accreditation is a harder constraint than latency.
D) The platform can use either region if the Scottish Government partner is renegotiated.

**Correct answer: B.**

**Explanation:** Chain the conditionals: Region North → latency targets missed → no collaboration agreement → programme cannot proceed. So Region North is eliminated by pure deduction. Region South satisfies latency; its accreditation takes four months, inside the six-month start window, so no constraint is violated. Option A is too strong — a viable path exists. Option C inverts the logic: accreditation is time-limited and recoverable, whereas the North latency failure is terminal via the agreement chain. Option D speculates beyond the given constraints; the stated rules say the programme *cannot* proceed without the agreement, and nothing licenses renegotiation. At principal level you make exactly these eliminative arguments in front of senior stakeholders: showing not just that an option is preferred, but that the alternatives are logically foreclosed by agreed constraints.

**Question 9 (hard) — Error checking an architecture decision record**

An architecture decision record (ADR) submitted for your sign-off states:

"Decision: adopt an event-driven integration pattern for all inter-service communication on the platform. Rationale: synchronous REST calls between services created cascading failures in the March incident. Consequences: (1) all services must publish state changes to the event broker; (2) the reporting service, which requires strongly consistent reads at the moment of query, will consume events with eventual consistency; (3) no service will make synchronous calls to another service. Status: Accepted."

Which is the most significant internal problem in this ADR?

A) The rationale cites an incident, which is anecdotal and inadmissible.
B) Consequence (2) contradicts the reporting service's stated requirement: eventual consistency cannot satisfy a requirement for strongly consistent reads, so the decision as written breaks a known requirement without addressing it.
C) Consequence (1) and consequence (3) are contradictory.
D) The status should be "Proposed" because sign-off has not occurred.

**Correct answer: B.**

**Explanation:** Consequence (2) records that the reporting service "requires strongly consistent reads at the moment of query", then routes it through an eventually consistent event stream — a requirement violation stated in the ADR's own text with no mitigation (such as an exception for reporting, a read-model freshness bound, or a synchronous read path). Option A is wrong: incident evidence is legitimate rationale. Option C fails: publishing events and prohibiting synchronous calls are complementary, not contradictory. Option D notes a genuine process nicety but it is trivially fixable and far less significant than an unaddressed broken requirement. This is the core of technical design assurance at your level: the most dangerous flaws are the ones the document itself confesses to, one clause at a time, without ever putting the contradiction in a single sentence.

**Question 10 (hard) — Problem solving under resource constraints**

Three teams need specialist platform engineering support this quarter. You can fund 10 weeks of that specialist capacity in total.

- Team X needs 6 weeks to remove a critical single point of failure; without it, risk of a major outage is assessed as high.
- Team Y needs 5 weeks to meet an accessibility remediation deadline with regulatory consequences in this quarter.
- Team Z needs 4 weeks to enable a cost-saving migration worth £300,000 a year, with no deadline.

You cannot partially fund a team's need. Which allocation is most defensible?

A) X and Y (11 weeks) — exceed the budget slightly.
B) X and Z (10 weeks) — highest total weeks used within budget.
C) Y and Z (9 weeks) — meets the regulatory deadline and captures savings, deferring X with interim risk mitigation.
D) X only (6 weeks) — hold 4 weeks in reserve.

**Correct answer: C.**

**Explanation:** First, option A violates the hard constraint — 11 weeks is not available, and "slightly exceeding" a fixed capacity is not in your gift. The real choice is between funding X and Z, Y and Z, or X alone. Y carries a regulatory deadline *this quarter*: missing it has legal and reputational consequences that cannot be recovered later. Z is cheap (4 weeks) and yields recurring savings. X is serious but is a *risk*, not a certainty, and risks can be mitigated in the interim (monitoring, runbooks, temporary redundancy at the infrastructure level, or descoping traffic) and funded first thing next quarter. Option B leaves a statutory deadline to fail, which no outage-risk argument comfortably outweighs when mitigation exists. Option D strands capacity while both a deadline and savings go unmet. Note the deeper lesson, which assessors look for: "highest risk first" is a heuristic, not a law — recoverability, deadlines, and mitigation options change the calculus, and a principal architect is expected to reason about all three and to document the interim mitigation for X as part of the decision.

**Question 11 (hard) — Pattern recognition across strategy signals**

You are drafting the technology strategy refresh. Four signals arrive in the same month:

1. Two delivery teams independently request exceptions to use the same unsupported queueing technology.
2. The central platform's queueing service has a nine-week backlog of feature requests.
3. Exit interviews with two departing engineers cite "fighting the platform" as a frustration.
4. A supplier briefing forecasts price rises for the platform's underlying messaging product.

What is the most valuable strategic inference?

A) The two teams are colluding to bypass governance and should be reminded of the exception process.
B) The signals independently suggest the central queueing capability no longer meets demand; the strategy should treat messaging as an area for deliberate reinvestment or replacement, not case-by-case exception handling.
C) The supplier price rise is the root cause of all four signals.
D) The exit interviews are an HR matter and out of architectural scope.

**Correct answer: B.**

**Explanation:** The skill being tested is synthesis: four weak signals from different sources — governance requests, backlog data, people data, market data — converge on one underlying pattern: the central messaging capability is under-serving its consumers, and pressure is escaping through exceptions and attrition. Option A treats a systemic signal as a compliance problem, which is precisely the failure mode of governance-as-policing. Option C reverses causality — the price rise is future-dated and cannot have caused the backlog or the exits. Option D draws the boundary of "architectural" too narrowly; architecting for the whole context explicitly includes tracking internal issues affecting teams across the organisation, and engineer attrition attributable to platform friction is a first-class architectural signal. The strategic move is to name the pattern in the strategy and decide deliberately — reinvest, replace, or federate — rather than letting fifty exceptions decide by default.

**Question 12 (moderate) — Logical consistency in a stakeholder claim**

A senior director tells a board: "Every service that adopted the shared API platform reduced its integration costs. Our flagship service has not reduced its integration costs. Therefore the flagship service has not adopted the shared API platform."

Setting aside whether the premises are true, is the argument logically valid?

A) Yes — it is a valid application of the contrapositive.
B) No — it affirms the consequent.
C) No — reduced costs might have other causes, so the conclusion fails.
D) Yes — but only if most services adopted the platform.

**Correct answer: A.**

**Explanation:** Formally: adoption → reduced costs. The flagship shows not-reduced-costs, therefore not-adoption. Denying the consequent (modus tollens, the contrapositive) is valid: if adoption guaranteed reduction, a service without reduction cannot have adopted. Option B names the wrong fallacy — affirming the consequent would be "the flagship reduced costs, therefore it adopted the platform". Option C confuses validity with soundness: other causes of cost reduction are irrelevant because the argument runs on the *absence* of reduction; the premise "every adopter reduced costs" may be empirically dubious, but the question isolates the logic. Option D imports a quantifier the argument does not need. Why this matters for you: senior stakeholders constantly present arguments of exactly this shape, and your architecture communication skill includes hearing, in real time, whether the logic or the premises are the weak point — because you challenge each differently, and challenging the wrong one in a boardroom costs credibility.

### Preparation tips

- **Rehearse with your own artefacts.** Take a real ADR, dependency map, or governance paper (suitably anonymised) and interrogate it the way these questions do: what follows necessarily? What contradicts what? Which claim is temporal, which is logical? You do this instinctively; making it deliberate sharpens it under timed conditions.
- **Practise separating validity from truth.** Several question types at your level hinge on whether a conclusion follows from stated constraints, regardless of whether the constraints are realistic. Answer from the given rules only.
- **Manage the clock strategically.** With 15 to 30 minutes for a full test, treat any question consuming more than double its fair share as a candidate to flag and skip. As with a portfolio, sunk time is not a reason to spend more.
- **Read stem verbs precisely.** "Which follows necessarily", "which is most supported", and "which identifies the error" are different tasks. At principal level, distractors are usually plausible truths that fail the specific verb.
- **Warm up beforehand.** Ten minutes of practice questions immediately before the assessment measurably steadies early-question accuracy — and early questions matter more on adaptive platforms.

### Common pitfalls

- **Importing outside knowledge.** You know more about real government platforms than any test author. If the scenario says the accreditation takes four months, it takes four months — do not adjust for what you know of real accreditation bodies.
- **Seniority bias in prioritisation items.** A frequent error among senior candidates is ranking the most senior requester first. Assessments reward impact-and-deadline reasoning, not deference.
- **Over-engineering simple items.** Some questions really are one-step deductions. Hunting for a hidden trick in an easy question is a classic time sink identified in cognitive assessment research.
- **Confusing "no error" options.** When "there is no error" appears, check each claim methodically before selecting it — it is occasionally correct, and assuming every question hides a flaw is itself a bias.
- **Speed without verification.** Scoring reports separate speed from accuracy. A rushed wrong answer costs more than a checked slow one; aim for a steady cadence with a five-second verification pass per answer.


## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment evaluates your ability to analyse, interpret, and make sound decisions using numerical data drawn from the actual demands of your role. It is emphatically not an abstract mathematics exam: the emphasis is on business arithmetic — percentages, ratios, unit costs, growth rates, and cost-benefit comparisons — applied to the kinds of tables, budgets, and dashboards a principal technical architect actually handles. Most assessments allow or provide an on-screen calculator, because the point is interpretation and decision quality, not mental arithmetic. Time limits are typically strict, often around a minute to ninety seconds per question, so quick and accurate data extraction matters.

For your role, the numeric content will look like this: multi-year programme budgets and transformation business cases you must defend to investment boards; supplier and cloud cost models you compare when making high-risk architectural decisions; capacity and performance figures — requests per second, storage growth, availability percentages — that underpin technical designs; and portfolio-level metrics you track across the multiple teams you support. When you advocate for resources to enable a strategy, or argue that an emerging technology will pay back its adoption cost, you are making numeric arguments to senior stakeholders, and the credibility of your architecture communication rests on getting them right.

The assessment matters at principal level for a further reason: you check other people's numbers. Teams bring you business cases, capacity plans, and savings claims. Errors of scale ("in thousands" misread), baseline confusion (percentage of what?), and compounding mistakes (adding growth rates that should multiply) are among the commonest defects in the papers you assure. A strong numeric reasoning score signals that you can catch these quickly and confidently in governance settings.

### What it measures for your role

- **Budget and cost-model arithmetic** maps to **strategy design**: enabling implementation of strategies by advocating for resources means quantifying options, whole-life costs, and payback periods credibly.
- **Capacity, performance, and availability calculations** map to **technical design throughout the life cycle**: technical designs characterised by high risk and complexity stand or fall on whether throughput, storage, and resilience numbers hold together.
- **Comparative evaluation of options** maps to **making architectural decisions**: high-risk decisions typically reduce to structured numeric comparison — total cost of ownership, risk-weighted benefit, unit economics across suppliers.
- **Trend and portfolio metrics** map to **architect for the whole context**: tracking emerging issues over time means reading run-rate changes, growth curves, and cross-team indicators correctly.
- **Explaining numbers to others** maps to **architecture communication** and **community collaboration**: you coach architects and brief boards, so you must not only compute a figure but understand its construction well enough to defend it.

### Practice questions

Use a calculator freely, but write down intermediate figures — transcription errors are the leading cause of lost marks. Aim for ninety seconds per question before checking the worked answer.

**Question 1 (easy) — Percentage change in running costs**

A legacy case-working system costs £2.4 million a year to run. Your target architecture replaces it with a cloud-native service costing £1.8 million a year. What percentage reduction in annual running cost does the migration deliver?

A) 20%
B) 25%
C) 30%
D) 33%

**Correct answer: B.**

**Explanation:** Reduction = £2.4m − £1.8m = £0.6m. Percentage reduction = 0.6 ÷ 2.4 = 0.25 = **25%**. The classic distractor is option D: 0.6 ÷ 1.8 = 33%, which measures the saving against the *new* cost instead of the original baseline. Percentage change is always relative to the starting value unless stated otherwise. In an investment board paper, quoting 33% here would overstate your case and invite an uncomfortable correction — the kind of baseline discipline you also enforce when assuring other teams' savings claims.

**Question 2 (easy) — Reading a capacity table**

Your platform's four environments show the following monthly compute spend and utilisation:

| Environment | Monthly spend | Average utilisation |
|---|---|---|
| Production | £84,000 | 62% |
| Pre-production | £41,000 | 18% |
| Test | £22,000 | 11% |
| Development | £13,000 | 35% |

Which environment offers the largest absolute monthly saving if right-sizing could raise its utilisation to 60% at proportionally reduced spend?

A) Production
B) Pre-production
C) Test
D) Development

**Correct answer: B.**

**Explanation:** Right-sizing to 60% utilisation means you would need only (current utilisation ÷ 60%) of current spend. Pre-production: needed spend = 41,000 × (18 ÷ 60) = 41,000 × 0.3 = £12,300, saving £28,700. Test: 22,000 × (11 ÷ 60) = £4,033, saving £17,967. Development: 13,000 × (35 ÷ 60) = £7,583, saving £5,417. Production is already above 60%, so no saving. Pre-production's **£28,700** is the largest. The trap is choosing Test because it has the *lowest utilisation* — but absolute saving depends on spend as well as utilisation. Optimising for the worst percentage rather than the biggest opportunity is a real and common portfolio error.

**Question 3 (moderate) — Compound growth in storage**

A document store currently holds 40 TB and grows at 15% per year, compounding. The platform's economical ceiling is 70 TB, beyond which a re-architecture is needed. After how many complete years will storage first exceed 70 TB?

A) 3 years
B) 4 years
C) 5 years
D) 6 years

**Correct answer: C.**

**Explanation:** Compound year by year. Year 1: 40 × 1.15 = 46.0 TB. Year 2: 46 × 1.15 = 52.9 TB. Year 3: 52.9 × 1.15 = 60.8 TB. Year 4: 60.8 × 1.15 = 69.96 TB — fractionally *under* the ceiling. Year 5: 69.96 × 1.15 = 80.45 TB. So storage first exceeds 70 TB after **5 complete years**. This question rewards computing rather than estimating: rounding 69.96 "up to about 70" would hand you year 4, option B, and the wrong answer. Note also the linear-growth trap: 15% of the *original* 40 TB is 6 TB per year, giving 40 + 4 × 6 = 64 TB at year 4 and 70 TB at year 5 — the same final answer here purely by coincidence, but an indefensible method that fails on most datasets. Compounding applies the rate to each new balance. When a re-architecture takes months to plan and fund, the difference between year 4 and year 5 is your entire planning runway, so marginal cases like 69.96 versus 70 are exactly where assessors separate careful calculators from estimators.

**Question 4 (moderate) — Supplier cost comparison with usage tiers**

Two suppliers offer an API gateway service. Your platform handles 90 million calls per month.

- Supplier A: £8,000 per month flat, plus £0.10 per thousand calls.
- Supplier B: £20,000 per month flat, plus £0.04 per thousand calls above 30 million calls (first 30 million included).

Which supplier is cheaper at current volume, and by how much per month?

A) Supplier A, by £1,400
B) Supplier B, by £5,400
C) Supplier A, by £5,400
D) Supplier B, by £2,400

**Correct answer: C.**

**Explanation:** Convert units first: 90 million calls = 90,000 thousand-call units. Supplier A: usage charge = 90,000 × £0.10 = £9,000; total = 8,000 + 9,000 = **£17,000**. Supplier B: chargeable volume = 90m − 30m included = 60m = 60,000 thousand-call units × £0.04 = £2,400; total = 20,000 + 2,400 = **£22,400**. Supplier A is cheaper by 22,400 − 17,000 = **£5,400** per month. The two classic errors are both represented in the distractors: forgetting to subtract Supplier B's 30-million-call included tier before applying its rate (which inflates B's usage charge to £3,600 and shrinks the gap), and mixing up which supplier wins after a long calculation — always re-read the question's direction before answering. Worth noticing strategically: B's lower marginal rate means the ranking flips at high volume. Setting 8,000 + 0.10v = 20,000 + 0.04(v − 30,000) gives a break-even near 180,000 thousand-calls, i.e. 180 million calls per month — so if traffic is forecast to double twice, the "more expensive" supplier becomes the right long-term decision. Tiered pricing questions reward exactly this whole-life view, which is also how you should brief an investment board.

**Question 5 (moderate) — Availability percentages**

A citizen-facing service is composed of three sequential dependencies: an identity service with 99.9% availability, an application tier at 99.5%, and a payments provider at 99.8%. Assuming independent failures, what is the approximate end-to-end availability?

A) 99.9%
B) 99.5%
C) 99.2%
D) 98.7%

**Correct answer: C.**

**Explanation:** Serial availability multiplies: 0.999 × 0.995 × 0.998. Step by step: 0.999 × 0.995 = 0.994005. Then 0.994005 × 0.998 = 0.992017. That is **99.2%**. The tempting error is option B — taking the weakest link alone — but three imperfect components in series are always worse than the worst single one. 99.2% availability means roughly 0.8% downtime: about 5.8 hours in a 30-day month, versus 3.6 hours for 99.5% alone. At your level this arithmetic drives real design decisions: it is the quantitative argument for redundancy, graceful degradation, or renegotiating a dependency's service level — and it is exactly the calculation to run live in a design review when a team claims their service "inherits" the platform's headline availability.

**Question 6 (moderate) — Budget allocation ratios**

Your transformation programme's £5.4 million annual budget is split across strategy, platform engineering, and team enablement in the ratio 2 : 5 : 2. The board asks you to increase team enablement's share to 30% of the total budget, holding the total constant and taking the increase entirely from platform engineering. What is platform engineering's new annual allocation?

A) £3.00 million
B) £2.58 million
C) £2.40 million
D) £2.16 million

**Correct answer: B.**

**Explanation:** Ratio parts: 2 + 5 + 2 = 9 parts; each part = 5.4 ÷ 9 = £0.6m. Current: strategy £1.2m, platform £3.0m, enablement £1.2m. New enablement = 30% × 5.4 = £1.62m, an increase of £0.42m. Taken entirely from platform: 3.0 − 0.42 = **£2.58m**. Option A is the unchanged figure; option C wrongly recomputes platform as a fresh percentage; option D subtracts the whole new enablement growth from the wrong base. Ratio-to-percentage conversion under reallocation is bread-and-butter for resource advocacy: when you argue for enablement investment (coaching architects, communities of practice), you must state precisely what it costs the other lines.

**Question 7 (hard) — Payback period for a re-platforming decision**

A proposed migration from a licensed integration product to an open-source alternative costs £900,000 up front (engineering and parallel running). It removes £320,000 a year in licence fees but adds £80,000 a year in additional support engineering. Savings begin in year 1. What is the payback period, and what is the cumulative net position at the end of year 5?

A) Payback in year 3; net +£300,000 at end of year 5
B) Payback in year 4; net +£300,000 at end of year 5
C) Payback in year 3; net +£700,000 at end of year 5
D) Payback in year 4; net +£380,000 at end of year 5

**Correct answer: B.**

**Explanation:** Net annual saving = 320,000 − 80,000 = £240,000. Cumulative: end year 1: −900,000 + 240,000 = −£660,000. Year 2: −£420,000. Year 3: −£180,000. Year 4: **+£60,000** — payback occurs during year 4 (specifically at 900,000 ÷ 240,000 = 3.75 years). End of year 5: −900,000 + (5 × 240,000) = −900,000 + 1,200,000 = **+£300,000**. Option A/C err by using the gross £320,000 saving (payback 2.8 years, year-5 net +£700,000) — forgetting the added support cost, the single most common flaw in the open-source business cases you will assure. The paired figure matters strategically: "payback at 3.75 years, £300k positive by year 5" is a much more defensible statement to an investment board than a bare "it saves money".

**Question 8 (hard) — Weighted scoring of architectural options**

Your design authority scores three integration options against weighted criteria (scores out of 10):

| Criterion | Weight | Option 1 | Option 2 | Option 3 |
|---|---|---|---|---|
| Security | 40% | 8 | 6 | 9 |
| Cost | 30% | 5 | 9 | 4 |
| Delivery speed | 30% | 6 | 8 | 5 |

Which option wins, and would the winner change if security's weight rose to 60% (cost and delivery speed at 20% each)?

A) Option 2 wins; no change at 60% security weighting.
B) Option 2 wins; at 60% security weighting Option 3 wins.
C) Option 1 wins; at 60% security weighting Option 3 wins.
D) Option 3 wins; no change at 60% security weighting.

**Correct answer: B.**

**Explanation:** Original weights — Option 1: (8 × 0.4) + (5 × 0.3) + (6 × 0.3) = 3.2 + 1.5 + 1.8 = 6.5. Option 2: 2.4 + 2.7 + 2.4 = 7.5. Option 3: 3.6 + 1.2 + 1.5 = 6.3. Option 2 wins. Re-weighted — Option 1: (8 × 0.6) + (5 × 0.2) + (6 × 0.2) = 4.8 + 1.0 + 1.2 = 7.0. Option 2: 3.6 + 1.8 + 1.6 = 7.0. Option 3: 5.4 + 0.8 + 1.0 = 7.2. Option 3 now wins (and Options 1 and 2 tie). The deeper point for a principal architect: weighted scores are only as decisive as their weights, and a plausible reweighting can flip the recommendation. Running exactly this sensitivity analysis before a governance board — "the decision holds unless security is weighted above roughly 55%" — is what turns a scoring table from decoration into evidence, and it defuses the predictable challenge from whichever stakeholder favours the losing option.

**Question 9 (hard) — Performance headroom under growth**

A service handles a peak of 1,200 requests per second (rps). Load tests show the current architecture saturates at 3,000 rps. Traffic grows 25% a year, compounding. Policy requires at least 40% headroom above forecast peak at all times. In which year does the architecture first breach the headroom policy?

A) Year 2
B) Year 3
C) Year 4
D) Year 5

**Correct answer: B.**

**Explanation:** The policy requires capacity ≥ 1.4 × forecast peak, so the maximum policy-compliant peak is 3,000 ÷ 1.4 = 2,143 rps. Forecast peaks: year 1: 1,200 × 1.25 = 1,500. Year 2: 1,875. Year 3: 1,875 × 1.25 = 2,344 — **above 2,143**, so the policy is first breached in year 3. Note the two-step structure: many candidates compare growth directly against 3,000 (giving year 4, option C, since 2,930 < 3,000 < 3,662) and miss that the *headroom* requirement, not raw saturation, is the binding constraint. Policies of this kind exist precisely so that re-architecture starts while margin remains; as the architect responsible for governance you would treat year 3 minus procurement-and-build lead time as the real decision date, which likely means starting the work in year 1 — a conclusion the arithmetic makes unarguable.

**Question 10 (hard) — Interpreting a portfolio dashboard**

Your quarterly portfolio dashboard shows, for the six teams you support, the percentage of production changes that failed and required remediation:

- Q1: Team totals — 480 changes, 24 failed.
- Q2: Team totals — 620 changes, 25 failed.

A board member says: "Failed changes went up from 24 to 25 — reliability is getting worse." What is the correct reading?

A) The board member is right: failures rose.
B) The failure *rate* fell from 5.0% to about 4.0%, a material improvement, even though the absolute count rose by one.
C) The figures are contradictory and cannot both be true.
D) Reliability is unchanged because 24 ≈ 25.

**Correct answer: B.**

**Explanation:** Q1 rate: 24 ÷ 480 = 0.050 = 5.0%. Q2 rate: 25 ÷ 620 = 0.0403 ≈ 4.0%. The denominator grew 29% while failures grew 4%, so the rate — the meaningful reliability measure when change volume varies — improved by about a fifth. Option A commits the absolute-versus-rate error; option D wrongly treats similar numerators as similar performance; option C is baseless, since a rising count and falling rate coexist happily when volume grows. Correcting a senior stakeholder's misreading is a live architecture communication task: the effective move is to concede the true fact ("yes, one more failure") and then supply the denominator, ideally converting to a shared unit — "one failure per 25 changes, improved from one per 20". Rate literacy is also what keeps your own strategy metrics honest as delivery volume scales.

**Question 11 (moderate) — Cost per transaction across channels**

A service processes 2.5 million transactions a year. Channel costs: digital handles 80% of transactions at £0.90 each; telephone handles 15% at £7.40 each; post handles 5% at £12.60 each. What is the blended cost per transaction across all channels?

A) £1.83
B) £2.46
C) £2.10
D) £3.02

**Correct answer: B.**

**Explanation:** Weighted average = (0.80 × 0.90) + (0.15 × 7.40) + (0.05 × 12.60) = 0.72 + 1.11 + 0.63 = **£2.46**. The total volume (2.5 million) is a red herring for the per-transaction figure — percentages suffice — though it converts the answer into a budget: 2.5m × £2.46 = £6.15m a year. The strategic use of this arithmetic: every percentage point shifted from telephone to digital saves (7.40 − 0.90) × 25,000 = £162,500 a year, which is how a digital transformation business case turns channel-shift ambitions into money. Assessments frequently include an unused number; part of the skill is deciding what the question actually needs.

**Question 12 (hard) — Reconciling two versions of a savings claim**

A team's business case claims their re-platforming saves £1.5 million over three years. Their finance annexe shows: year 1 saving £200,000; year 2 saving £550,000; year 3 saving £600,000; one-off transition cost £400,000 incurred in year 1. Which statement most accurately assesses the £1.5 million claim?

A) The claim is correct: gross savings total £1,350,000, which rounds to £1.5 million.
B) The claim overstates the position: gross savings are £1,350,000 and net of transition costs the three-year benefit is £950,000.
C) The claim understates the position: net benefit is £1,750,000.
D) The claim is correct if year 3 savings continue into year 4.

**Correct answer: B.**

**Explanation:** Gross savings: 200,000 + 550,000 + 600,000 = £1,350,000. Net of the £400,000 transition cost: £950,000. The £1.5m headline exceeds even the *gross* figure, so it fails both tests: it cannot be defended as gross (£1.35m does not "round" to £1.5m — option A's rounding is a 11% inflation) and certainly not as net. Option C would require ignoring the cost and adding £400,000 rather than subtracting it — a sign error that genuinely appears in rushed business cases. Option D smuggles in a fourth year the claim did not state. This is verbatim the assurance skill your governance role demands: reconcile the headline to the annexe before the board meeting, because someone will, and it is far better that it is you. A useful habit: recompute every headline number from its own supporting table; where they disagree, the annexe is usually right and the summary was written last, in a hurry.

**Question 13 (moderate) — Cross-region replication costs**

A resilience design replicates 175 TB of data per month from a UK region to a second region, charged at £0.02 per GB transferred. A revised design replicates only changed records — estimated at 22% of the monthly volume — but requires a change-data-capture service costing £2,100 per month. Using 1 TB = 1,000 GB, which design has the lower total monthly replication cost, and by how much?

A) The original design, by £630
B) The revised design, by £630
C) The revised design, by £2,730
D) The costs are equal

**Correct answer: B.**

**Explanation:** Original design: 175 TB = 175,000 GB × £0.02 = **£3,500** per month. Revised design: replicated volume = 22% × 175,000 = 38,500 GB × £0.02 = £770, plus the £2,100 service = **£2,870** per month. The revised design is cheaper by 3,500 − 2,870 = **£630**. Option C is the trap for candidates who compute the transfer saving (3,500 − 770 = £2,730) and forget the fixed cost of the service that produces it — the exact omission that inflates optimisation business cases in real life. Option A tests whether you kept track of direction after a multi-step calculation. The strategically valuable move is to generalise: the service pays for itself only when 78% of the transfer bill exceeds £2,100, i.e. above 2,100 ÷ (0.78 × 0.02) ≈ 134,600 GB ≈ **135 TB per month**. Below that volume the "optimisation" loses money. Computing the break-even, rather than comparing single scenarios, is how a principal architect should frame every fixed-cost-versus-usage-cost decision — and it converts this answer from a number into a policy: adopt change-data-capture for datasets above roughly 135 TB per month at current prices, and revisit when either price moves. Percentage change from the correct baseline, weighted averages, compound growth, serial availability multiplication, and payback periods cover most of what a technical architecture assessment will throw at you. Ten minutes a day for a week is transformative.
- **Practise with your own programme's numbers.** Take a real budget line or capacity forecast and ask the question formats above of it. Familiar data lowers the cognitive load of the format, so test-day novelty is confined to the numbers themselves.
- **Write down intermediate values.** Even with an on-screen calculator, transcription is the top error source. Three neat intermediate figures beat one heroic chained calculation.
- **Estimate first, then compute.** A five-second order-of-magnitude estimate ("about £2.50, so options over £3 are out") catches calculator slips instantly and sometimes answers the question outright.
- **Know your calculator etiquette.** Confirm before starting whether a calculator is provided, permitted, or prohibited, and rehearse with the same tool you will use on the day.
- **Learn the break-even habit.** Many role-realistic questions — tiered supplier pricing, optimisation services with fixed costs, buy-versus-build — are secretly break-even problems. Setting the two cost expressions equal and solving for the crossover volume answers not just the question asked but the strategic question behind it, and it is often faster than evaluating each scenario separately.
- **Rehearse explaining an answer in one sentence.** After each practice question, say aloud what the number means for a decision ("payback at 3.75 years, so the case survives a one-year delay"). This deepens the arithmetic into judgement, which is what your role — and increasingly the assessment centre exercises that follow the test — actually rewards.

### Common pitfalls

- **Misreading scale qualifiers.** "In thousands", "£m", and per-month versus per-year distinctions cause more lost marks than any arithmetic difficulty. Read the table header, then the units, then the numbers — in that order.
- **Baseline confusion.** Percentage change questions almost always offer the wrong-baseline answer as a distractor. Anchor to the original value unless told otherwise.
- **Adding growth rates that should compound.** Three years of 15% growth is ×1.15³ = ×1.52, not +45%. At small rates the difference is subtle; at portfolio scale it is a budget line.
- **Over-calculating.** If options are far apart, estimation and elimination are faster and safer than exact computation. Save precision for close options.
- **Time sinks.** One stubborn multi-stage question can cost you three easy ones. Flag, skip, and return — assessments reward total correct answers, not heroism on question 7.


## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment evaluates how well you understand, analyse, and draw correct conclusions from written material of exactly the kind your role demands. The passages mirror your real reading load: technology strategies, government service and technology standards, governance terms of reference, supplier correspondence, board papers, and emails from senior stakeholders. The defining rule is fact-based logic: you answer strictly from the text provided, ignoring everything you know from outside it. Most questions require a choice between True, False, or Cannot Say, supplemented by multiple-choice comprehension items, and time pressure is typically brisk — often less than a minute per question — to simulate workplace reading under deadline.

For a principal technical architect, verbal precision is not a soft skill; it is a control mechanism. The difference between "must" and "should" in a standard determines what your governance can enforce. The difference between what a supplier's letter states and what it merely implies determines your commercial position. The difference between a strategy that commits to an outcome and one that commits to an ambition determines what you can hold delivery teams to. You also draft much of this language yourself: when you define strategies, write decision records, and set standards for technical designs, the discipline of reading exactly what a text says — no more, no less — is the same discipline that makes your own documents unambiguous.

Assessments in this format also reward calibrated uncertainty. "Cannot Say" is not a weak answer; it is the correct verdict whenever the passage neither confirms nor contradicts the claim. Senior professionals often struggle with this more than junior ones, precisely because expertise supplies plausible answers the text never gave. Treat each passage as the entire universe of known facts.

### What it measures for your role

- **Precise comprehension of standards and policy** maps to your responsibility for **governance** and **making architectural decisions**: enforcing standards fairly requires reading exactly what they mandate, permit, and stay silent on.
- **Distinguishing stated fact from implication** maps to **architecture communication**: gaining support from stakeholders for high-risk topics requires representing documents accurately, and mediating difficult discussions often turns on what a text actually commits anyone to.
- **Reading strategy language critically** maps to **strategy design**: connecting strategies across an organisation demands detecting where a document promises an outcome, an intention, or merely an aspiration.
- **Synthesising stakeholder correspondence** maps to **architect for the whole context** and **community collaboration**: tracking emerging issues means extracting the real signal from long emails, minutes, and reports produced by teams across the organisation.
- **Spotting internal contradiction** maps to **technical design throughout the life cycle**: assurance reviews are, at bottom, an exercise in verbal consistency checking across a document set.

### Practice questions

For each passage, answer strictly from the text. Read the claim, then verify it word by word against the passage before answering.

**Passage A — extract from a departmental technology code of practice**

"All new digital services must be hosted on the department's approved cloud platforms unless a written exemption is granted by the Chief Technology Officer. Exemptions will normally be granted only where a service processes data classified above OFFICIAL, or where a statutory obligation requires on-premises processing. Services granted an exemption must be reviewed annually. Existing services are expected to migrate to approved platforms as part of their next major re-procurement, although the timing of re-procurement remains at the discretion of each service owner."

**Question 1 (easy).** True, False, or Cannot Say: "A new digital service may be hosted outside the approved cloud platforms if the Chief Technology Officer grants a written exemption."

**Correct answer: True.**

**Explanation:** The first sentence mandates approved platforms "unless a written exemption is granted by the Chief Technology Officer" — the exemption route is explicitly stated. Nothing more is needed; the second sentence's conditions describe when exemptions are "normally" granted but do not restrict the CTO's stated power. A careful reader resists the urge to add conditions the claim did not mention.

**Question 2 (moderate).** True, False, or Cannot Say: "Exemptions are granted only where data is classified above OFFICIAL or a statutory obligation requires on-premises processing."

**Correct answer: False.**

**Explanation:** The passage says exemptions "will normally be granted only" in those cases. "Normally" explicitly leaves room for abnormal cases, so the absolute claim "only" contradicts the qualified text. This single-word distinction — categorical claim versus qualified statement — is the most heavily tested pattern in verbal reasoning, and it mirrors real governance work: a standard that says "normally" cannot be enforced as if it said "always", and knowing which you are holding is the difference between firm assurance and overreach.

**Question 3 (moderate).** True, False, or Cannot Say: "Existing services must complete migration to approved platforms within three years."

**Correct answer: Cannot Say.**

**Explanation:** The passage sets an expectation ("expected to migrate... as part of their next major re-procurement") and explicitly leaves re-procurement timing to each service owner's discretion. No timeframe of any kind appears — three years is neither confirmed nor denied, and the obligation is an expectation tied to an event of uncertain date, not a deadline. Note the temptation for an experienced architect: you may know real codes of practice with hard deadlines. That knowledge is inadmissible; the passage is the whole universe.

**Question 4 (moderate).** True, False, or Cannot Say: "A service that received an exemption two years ago should have been reviewed at least once."

**Correct answer: True.**

**Explanation:** "Services granted an exemption must be reviewed annually." A service exempted two years ago falls under this mandate, and annual review over two years entails at least one review (in fact two). The reasoning is a small deduction, but it stays entirely inside the text: mandate plus elapsed time yields the conclusion. Deductions that combine two stated facts are legitimate; only *additions* of unstated facts are forbidden.

**Passage B — email from a supplier's account director to you as principal technical architect**

"Following our review of the platform roadmap, I can confirm that version 14 will reach end of standard support on 31 March next year. Extended support will be available for a further two years at an additional cost, details of which our commercial team will share separately. We recommend customers begin upgrade planning at least nine months before end of standard support. I should add that version 15 introduces a revised licensing model, which most customers on your usage profile have found cost-neutral or better. Our engineering team is happy to run a joint upgrade assessment at no charge, subject to scheduling."

**Question 5 (easy).** True, False, or Cannot Say: "Extended support for version 14 will be free of charge for two years."

**Correct answer: False.**

**Explanation:** The email states extended support is available "at an additional cost". The claim of "free of charge" directly contradicts this. Only the joint upgrade assessment is described as "at no charge" — a deliberate juxtaposition testing whether you attach the right cost statement to the right offering, exactly the reading error that creates budget surprises in real supplier negotiations.

**Question 6 (hard).** True, False, or Cannot Say: "Moving to version 15 will be cost-neutral or better for your organisation."

**Correct answer: Cannot Say.**

**Explanation:** The email says "most customers on your usage profile have found" the new licensing cost-neutral or better. "Most" is not "all", and other customers' experience — even similar ones — does not establish your outcome. The statement is evidence, arguably encouraging evidence, but the claim as worded asserts a fact about your organisation that the text cannot confirm or deny. This is precisely the kind of supplier sentence you must not transcribe into a board paper as an assurance: your architecture communication skill includes converting "most customers like you" into "the supplier reports that most similar customers..." — attribution intact, certainty not inflated.

**Question 7 (moderate).** According to the email, when should upgrade planning begin at the latest, following the supplier's recommendation?

A) 31 March next year
B) By the end of June this year — nine months before end of standard support
C) Two years after end of standard support
D) The email does not recommend a planning start point

**Correct answer: B.**

**Explanation:** End of standard support is 31 March next year; the supplier recommends beginning planning "at least nine months before", which lands at the end of June this year. Option A confuses the deadline with the planning start; option C confuses the extended support window with planning; option D ignores an explicit recommendation. Simple date arithmetic embedded in prose is a staple of verbal assessments because it mirrors real work: converting narrative supplier statements into calendar commitments for the teams you support.

**Passage C — extract from a draft cross-government technology strategy**

"Our vision is that by 2030, departments will share common platforms for identity, payments, and notifications, reducing duplication across government. This strategy commits us to three actions in the next two years: publishing interoperability standards for each platform domain; establishing a cross-government architecture forum with authority to endorse reference architectures; and funding two pathfinder integrations per year. The strategy does not mandate adoption of any specific platform. Departments retain accountability for their own technology choices, and we expect convergence to be driven by the demonstrated value of shared platforms rather than by central direction."

**Question 8 (moderate).** True, False, or Cannot Say: "The strategy requires departments to adopt the shared identity platform by 2030."

**Correct answer: False.**

**Explanation:** The passage states outright: "The strategy does not mandate adoption of any specific platform", and reinforces it — departments "retain accountability for their own technology choices", with convergence "driven by demonstrated value... rather than by central direction". The 2030 statement is labelled a *vision*, not a requirement. Distinguishing vision language from commitment language is a core strategy-design skill: this strategy commits to exactly three actions (standards, forum, pathfinders) and to nothing else, and reading it any more strongly would misrepresent it to your board.

**Question 9 (hard).** True, False, or Cannot Say: "The cross-government architecture forum will have authority to mandate reference architectures."

**Correct answer: False.**

**Explanation:** The forum's stated authority is "to endorse reference architectures". Endorsement and mandate are different powers, and the passage's closing sentences exclude central direction as the convergence mechanism, confirming the weaker reading. Answering "True" here is the over-reading error; answering "Cannot Say" is the under-reading error — tempting, but the text does settle the question, because a document that grants endorsement authority while explicitly disclaiming central direction has told you the mandate power is absent. Calibrating between False and Cannot Say is the hardest discrimination in this format: choose False when the text contradicts the claim (including by clear implication of its explicit statements), Cannot Say only when the text is genuinely silent.

**Question 10 (moderate).** Which statement best summarises the strategy's theory of change?

A) Central mandation of shared platforms, enforced through spending controls.
B) Voluntary convergence, encouraged by standards, endorsed reference architectures, and demonstration of value through funded pathfinders.
C) Immediate migration of all departments to common platforms.
D) Devolution of all technology decisions with no cross-government activity.

**Correct answer: B.**

**Explanation:** The strategy pairs enabling actions (standards, forum, pathfinder funding) with an explicit rejection of central direction, expecting "convergence... driven by the demonstrated value of shared platforms". Option A contradicts the no-mandate statements; C inflates a 2030 vision into an immediate obligation; D ignores the three funded central commitments. Summarisation questions test whether you can compress without distorting — the exact skill you use when a minister's office asks for the strategy "in one sentence" and every word you choose either preserves or betrays the document.

**Passage D — minutes of an architecture governance board**

"The board considered the case-working programme's request to defer its transition from the legacy messaging component. The programme argued that transition before the statutory year-end deadline would introduce unacceptable delivery risk. The security representative noted that the legacy component's vendor support expires in eight months and that no security patches will be issued thereafter. The board agreed to defer transition by six months, on condition that the programme deliver a compensating controls plan within four weeks and report monthly on implementation. Two members recorded reservations about the decision. The chair noted that a further deferral would require escalation to the executive risk committee."

**Question 11 (moderate).** True, False, or Cannot Say: "The deferred transition will complete before the legacy component's vendor support expires."

**Correct answer: Cannot Say.**

**Explanation:** The deferral is six months; vendor support expires in eight months. The comparison looks answerable — six is less than eight — but read carefully: the passage never states when the transition would have occurred without deferral, nor how long transition takes. "Defer transition by six months" shifts an unstated baseline; if the original transition date was three months away, the new date (nine months) falls *after* support expiry. The passage genuinely does not determine the ordering. This is a hard and instructive item: numbers in prose invite false confidence, and the assurance habit of asking "six months from *when*?" is exactly what the minutes fail to answer — as real minutes often do, which is why you would send them back for correction.

**Question 12 (easy).** True, False, or Cannot Say: "The board's decision was unanimous."

**Correct answer: False.**

**Explanation:** "Two members recorded reservations about the decision." Recorded reservations are incompatible with unanimity in any ordinary reading of board minutes — the board "agreed", but not unanimously and without dissent being invisible. The item tests whether you register the governance significance of small procedural sentences; in real assurance work, recorded reservations are a signal you follow up, because they often mark the risk that later materialises.

**Question 13 (moderate).** What must the programme deliver within four weeks?

A) The completed transition
B) A compensating controls plan
C) A monthly implementation report
D) An escalation to the executive risk committee

**Correct answer: B.**

**Explanation:** The condition reads: "deliver a compensating controls plan within four weeks and report monthly on implementation". The four-week deadline attaches to the plan; monthly reporting is a separate, ongoing condition; escalation applies only to a hypothetical *further* deferral; and the transition itself is deferred six months. Each distractor attaches a real element of the passage to the wrong obligation or timeline — the precise reading failure that turns governance conditions into disputes three months later.

**Question 14 (hard) — synthesis across Passage D.** Based on the minutes, which of the following would most plausibly trigger escalation to the executive risk committee?

A) The programme delivers its compensating controls plan a week early.
B) The programme requests a second deferral of the transition.
C) A board member withdraws their recorded reservation.
D) The vendor extends support for the legacy component.

**Correct answer: B.**

**Explanation:** The chair "noted that a further deferral would require escalation to the executive risk committee" — a second deferral request is precisely "a further deferral", so option B follows directly. Option A is compliance with a condition, not a trigger; option C reduces recorded dissent; option D would relieve the underlying security pressure rather than trip the escalation clause. Note the question's verb — "most plausibly trigger" — asks you to apply the stated rule to hypothetical events, a legitimate operation because the rule itself is in the text. This mirrors a real chairing skill: writing escalation clauses so that everyone can later agree, without argument, on whether an event tripped them. Vague escalation language ("significant further slippage") produces exactly the disputes that precise language ("a further deferral") prevents, and as the architect who leads governance you are usually the person who chooses those words.

**Passage E — extract from a technical standards consultation paper**

"This consultation proposes revising the organisation's API standard. Under the current standard, all externally consumed APIs must publish an OpenAPI specification and must version breaking changes; internally consumed APIs are encouraged, but not required, to do the same. The proposed revision extends both requirements to internally consumed APIs, with a twelve-month transition period from the date of publication of the revised standard. Respondents should note that the revision does not alter authentication requirements, which are governed by the separate security standard. Sixty-one teams responded to the previous consultation, of which forty-two supported extending the requirements, eleven opposed, and the remainder expressed no preference. The architecture forum will consider the consultation responses before a final decision is made."

**Question 15 (easy).** True, False, or Cannot Say: "Under the current standard, internally consumed APIs are required to publish an OpenAPI specification."

**Correct answer: False.**

**Explanation:** The passage states that internally consumed APIs "are encouraged, but not required" to publish a specification under the current standard. The claim asserts a requirement, which directly contradicts the text. The encouraged/required distinction is the modality pattern again, and it is one you police constantly in standards work: teams frequently treat encouragement as mandate (over-compliance that breeds resentment) or mandate as encouragement (under-compliance that breeds incidents), and the standard's author — often you — must keep the two legible.

**Question 16 (moderate).** True, False, or Cannot Say: "If the revision is adopted, internal APIs will need to version breaking changes within twelve months of the revised standard's publication."

**Correct answer: True.**

**Explanation:** The proposed revision "extends both requirements to internally consumed APIs" — both means the OpenAPI specification requirement *and* the breaking-change versioning requirement — "with a twelve-month transition period from the date of publication". Conditional claims ("if the revision is adopted") are evaluated by checking whether the text supports the consequence given the condition, and here it does explicitly. Note the claim does not assert the revision *will* be adopted — the passage leaves the decision with the architecture forum — so the conditional framing keeps the claim within what the text supports.

**Question 17 (hard).** True, False, or Cannot Say: "A majority of the teams consulted support extending the requirements."

**Correct answer: Cannot Say.**

**Explanation:** Read the denominators with care. Sixty-one teams *responded*; forty-two of them supported the extension. Forty-two of sixty-one is comfortably a majority of *respondents* — but the claim is about "the teams consulted", and the passage never states how many teams were consulted, only how many responded. If two hundred teams were consulted and sixty-one replied, the forty-two supporters would be a minority of the consulted population; if sixty-five were consulted, they would be a majority. The text cannot settle it, so Cannot Say is the verdict. This is the classic denominator-shift trap: the claim quietly swaps the passage's stated population (respondents) for a larger, unquantified one (consultees), and the plausible arithmetic on the wrong denominator lures you to True. Take the workplace lesson with you: consultation summaries that blur "responded" and "consulted" misrepresent their own evidence base, and it is exactly your job as the standards owner to catch that before the architecture forum treats forty-two out of sixty-one as the voice of the whole organisation.

**Question 18 (moderate).** Which of the following is explicitly out of scope for the proposed revision?

A) Versioning of breaking changes for internal APIs
B) Authentication requirements
C) The transition period's length
D) OpenAPI specifications for external APIs

**Correct answer: B.**

**Explanation:** "The revision does not alter authentication requirements, which are governed by the separate security standard" — an explicit scope exclusion. Option A is the substance of the revision, option C is a stated parameter of it, and option D is already required under the current standard and unchanged in force. Scope-exclusion sentences are among the most operationally important lines in any standards document: they tell you which governance regime an issue belongs to, and routing a question to the wrong standard's owner is a small error that costs weeks.

### Preparation tips

- **Train the three-verdict discipline.** For every claim, ask in order: does the text state or entail this (True)? Does the text state or entail its negation (False)? Otherwise Cannot Say. Senior candidates lose most marks by letting expertise convert Cannot Say into True.
- **Highlight modality words as you read.** Must, should, may, normally, expected, committed, vision, endorse, mandate — these words carry the whole logical weight of governance prose. Practising on real standards (the Technology Code of Practice, the Service Standard) builds the reflex on authentic material.
- **Read the claim first, then hunt.** Under a minute per question, reading the whole passage cold before seeing the claim wastes your budget. Skim the structure, read the claim, then verify against the specific sentences that bear on it.
- **Practise on your own document set.** Take a strategy or ADR you know well and generate True/False/Cannot Say claims for a colleague — writing the questions teaches the format faster than answering them, and it doubles as coaching material for the architects you develop.
- **Keep calm about ambiguity.** Some items are designed so that the difference between False and Cannot Say is genuinely fine. Apply the rule — contradiction (including clear implication) means False; silence means Cannot Say — and move on without relitigating.
- **Check denominators and populations.** Claims about "a majority", "most teams", or "all services" depend on which population the passage actually quantified. Respondents are not consultees; services reviewed are not services in total. Verifying the population takes five seconds and defeats one of the format's most reliable traps.
- **Watch for scope and exclusion sentences.** Lines such as "this does not alter authentication requirements" carry disproportionate weight in both assessments and real standards work. Note them as you skim; questions cluster around them because misreading scope is the highest-consequence comprehension error in governance documents.

### Common pitfalls

- **Importing professional knowledge.** You have read more technology strategies than most test authors. That is precisely your risk: the passage, not your experience, is the sole source of truth.
- **Treating likelihood as fact.** "Most customers found it cost-neutral" does not make it true for you; "we expect convergence" does not make convergence required. Confusing stated probability or expectation with established fact is the most common senior-level error.
- **Absolute-word blindness.** Claims containing "only", "always", "all", "never", or "must" are usually testing a qualifier in the passage ("normally", "expected", "should"). When you see an absolute claim, hunt for the hedge.
- **Baseline and reference ambiguity.** Durations and dates in prose ("defer by six months", "nine months before") depend on reference points the passage may not supply. Verify the anchor exists before comparing numbers.
- **Spending the time budget on reading.** Scanning for the claim's keywords beats sequential reading. The format rewards targeted verification, not literary appreciation — save that for the documents you write yourself.


## Workplace job-specific situational judgement assessment

### About this assessment

A workplace job-specific situational judgement assessment evaluates your decision-making, interpersonal skill, and professional conduct through realistic workplace dilemmas. Unlike the cognitive, numeric, and verbal formats, there is often no single objectively right answer: several responses may be reasonable, but one aligns best with the role's demands and the organisation's values. You are typically asked to select the Most Effective and Least Effective actions from a set, or to rank or rate all options from best to worst. Timing is usually generous or absent, because the format measures natural judgement rather than speed.

For a principal technical architect, the scenarios will be drawn from the situations that define your working life: a senior stakeholder pressing for a decision that undermines the agreed strategy; two teams in architectural conflict with a deadline looming; an architect you coach making a defensible but risky call; a governance process that is technically correct but strangling delivery; a supplier relationship drifting somewhere commercially uncomfortable. What is being assessed is not technical knowledge — the scenarios rarely have a technically determinate answer — but judgement: how you balance pace against risk, candour against diplomacy, empowerment against control, and your own authority against the collaborative culture the Government Digital and Data profession expects.

UK public sector values run through the scoring key: user needs first, openness and transparency, collaboration across boundaries, accessibility and inclusion, and evidence-based decision-making. Strong answers tend to address root causes rather than symptoms, keep decisions transparent and recorded, respect delegated authority while retaining accountability, and preserve relationships without abandoning the substance. Weak answers tend to be passive (wait and see), evasive (pass the problem along), autocratic (impose without engagement), or idealistic in ways that ignore practical constraints.

### What it measures for your role

- **Stakeholder judgement** maps to **architecture communication**: gaining support from business and technical stakeholders for topics with high risk, impact, and complexity, and mediating between people in difficult architectural discussions.
- **Influence across boundaries** maps to **architect for the whole context**: taking action to solve or mitigate problems by influencing colleagues across the organisation, often without direct authority.
- **Developing others** maps to **community collaboration** and your duty to inspire other architects: adapting feedback so it is effective and lasting, and helping architects understand how to deliver the organisation's goals.
- **Decision discipline under pressure** maps to **making architectural decisions**: guiding decisions characterised by high risk and complexity, and leading architectural governance and assurance even when it is politically uncomfortable.
- **Strategic stewardship** maps to **strategy design**: making sure the strategy is agreed and followed — including when following it is inconvenient for someone powerful — and removing blockers so others can implement it.

### Practice questions

For each scenario, decide your answer before reading the discussion. Where the format is Most/Least Effective, commit to both choices.

**Question 1 (moderate) — The strategy-bypassing director**

A delivery director, senior to most of your stakeholders, tells you she intends to procure a proprietary low-code platform for her directorate's new casework services. The agreed technical strategy, which you are responsible for making sure is followed, commits new services to the department's standard stack precisely to avoid further platform sprawl. She says the strategy "wasn't written with her directorate's timescales in mind" and that she has budget cover. Options:

A) Escalate immediately to the CTO, copying the director, stating that the procurement breaches the technical strategy.
B) Meet the director to understand the delivery pressure behind her position, test whether the standard stack can meet her timescales, and agree to take her case through the strategy's exception process with your honest assessment attached.
C) Accept the procurement — she is senior, has budget, and the strategy allows local judgement.
D) Ask her team's architect to quietly delay the procurement paperwork while you build a coalition against it.

**Most effective: B. Least effective: D.**

**Explanation:** Option B does three things a principal architect must do at once: it treats a senior stakeholder's constraint as real rather than as defiance (architecture communication), it tests the strategy against a genuine hard case rather than assuming the strategy is always right, and it routes disagreement through the transparent exception mechanism you yourself govern — with your professional assessment on the record. That is "making sure the strategy is agreed and followed" in its mature form: followed *through* its processes, not enforced by ambush. Option A escalates before understanding; escalation may yet be needed, but leading with it burns the relationship, and boards reasonably ask "what did you do first?". Option C abandons your core accountability and misstates the strategy. Option D is the least effective by a distance: covert delay through a junior colleague is manipulative, puts the directorate's architect in an untenable position, and violates the openness the profession expects — when it surfaces, and it will, your governance loses the legitimacy that makes it work.

**Question 2 (moderate) — Two teams, one integration, no agreement**

Two delivery teams you support must integrate their services for a legislative deadline in ten weeks. Team One insists on an event-driven integration consistent with the target architecture; Team Two argues a direct point-to-point API is the only approach deliverable in time, and has data suggesting the event route needs fourteen weeks. The teams have stopped attending each other's design sessions. Options:

A) Direct both teams to implement the event-driven design because it matches the target architecture.
B) Let the teams resolve it themselves — intervening undermines their autonomy.
C) Convene a time-boxed joint session you facilitate: agree the deadline is fixed, examine the fourteen-week evidence together, and decide openly between a compliant route that fits and a documented, time-limited exception with a convergence plan.
D) Rule for the point-to-point API and move on — deadlines beat architecture.

**Most effective: C. Least effective: B.**

**Explanation:** This scenario tests mediation in difficult architectural discussions plus decision discipline. Option C restores the collaboration that has broken down (the teams have stopped talking — that dynamic, not the integration pattern, is the root problem), subjects the critical evidence to joint scrutiny, and frames the legitimate outcomes honestly: either the target-state route fits within the deadline or you record a conscious, expiring exception. A statutory deadline missed harms citizens; an undocumented architectural shortcut harms every future team; option C is the only route that avoids both silently. Option A imposes the target architecture without engaging the delivery evidence — if the fourteen-week estimate is right, you have just directed a team to miss a legislative deadline. Option D makes the mirror-image error and normalises strategy erosion with no convergence path. Option B is least effective: this is a deadlocked, deadline-critical conflict between teams that are no longer communicating — precisely the situation where a principal architect's facilitation is the job. Autonomy is for decisions teams can make; deadlock across team boundaries is yours.

**Question 3 (hard) — The coached architect's risky decision**

An architect you coach has taken a design decision for her programme: adopting a promising but immature open-source framework as the foundation of a high-profile service. Her decision record is well argued and was approved through her programme's local governance, which was entitled to decide. You believe the maturity risk is materially understated — two comparable projects elsewhere in government abandoned the framework this year. She is proud of the decision and has announced it to her programme board. Options:

A) Say nothing — the decision was properly made through legitimate governance, and undermining it would undermine her.
B) Share the two comparable cases with her privately, ask how her risk assessment would change if the same failure modes applied, and let her decide whether and how to reopen the decision — offering to support her either way.
C) Use your position to overturn the decision at the next design authority and select a mature alternative.
D) Raise your concerns at her programme board so the risk is transparently on record.

**Most effective: B. Least effective: C.**

**Explanation:** The tension is between respecting delegated, legitimate governance and your duty to identify architectural risks across the organisation — plus your coaching relationship. Option B resolves all three: the missing input is *information* (two abandonments she may not know about), and supplying it privately lets her own the reassessment, which is what "adapt feedback to ensure it's effective and lasting" means in practice. If she reopens the decision, it is her strengthened judgement, not your override; if she assesses the new evidence and stands by the choice, the risk is now genuinely considered rather than understated. Option A confuses respecting governance with withholding material evidence — silence here is a failure of your whole-context duty, not politeness. Option D puts the evidence on record but does it *to* her rather than *with* her, publicly, at her own board, damaging her standing and teaching every architect you coach that development conversations happen by ambush. Option C is least effective: overturning a legitimately made, well-argued decision by seniority substitutes your authority for the governance system you are supposed to be strengthening, and converts a coaching relationship into a compliance one. Principal architects who routinely overrule delegated decisions soon find no one brings them decisions at all — only finished announcements.

**Question 4 (moderate) — Governance strangling delivery**

Three delivery teams separately tell you that the architecture review process you inherited — a fortnightly board with a three-week paper deadline — is adding five to six weeks to every significant design decision. The board's members value the current format. One team admits it has started making decisions "informally" and regularising them afterwards. Options:

A) Remind the teams that the process is mandatory and that informal decision-making must stop immediately.
B) Treat the workaround as evidence the process is failing its users: redesign the governance with the teams and the board — for example, risk-tiered review, empowered team-level decisions within guardrails, and the board reserved for genuinely high-risk items — and pilot it openly.
C) Abolish the board — architecture governance should be fully delegated to teams.
D) Keep the process but ask teams to submit papers earlier so the delay is absorbed upstream.

**Most effective: B. Least effective: A.**

**Explanation:** Your role explicitly includes leading and *evolving* architectural governance and assurance. Option B reads the informal workaround correctly — as a signal, not a sin: when a control adds six weeks to every decision, evasion is the predictable system behaviour, and punishing it without fixing the cause guarantees it continues invisibly. Redesigning with both the teams and the board honours community collaboration, and risk-tiering is the recognised pattern: govern in proportion to risk, empower within guardrails, keep assurance for decisions that warrant it. Option D is superficially pragmatic but simply relocates the delay and increases teams' planning burden — the six weeks still exist. Option C over-corrects: your accountability for high-risk decisions and cross-organisation coherence cannot be wholly delegated, and abolition would abandon the board members rather than bring them along. Option A is least effective because it doubles down on a failing control, drives decision-making further underground, and frames teams as offenders when the process is the offender — the exact governance-as-policing posture that destroys the trust assurance depends on.

**Question 5 (hard) — The conference-corridor commitment**

At a cross-government event, your director general enthusiastically tells a counterpart from another department that your organisation will "definitely" adopt the counterpart's new shared platform next year, and asks you, in front of both delegations, to confirm. You assessed the platform three months ago: it is promising but currently fails two of your non-negotiable requirements — accessibility compliance and data residency. Options:

A) Confirm the commitment to avoid embarrassing your director general, and plan to surface the problems later.
B) Contradict the commitment on the spot, citing the two failed requirements, so no false expectation is created.
C) Respond that the platform is genuinely promising and you would welcome adoption, that your assessment found two specific issues to resolve first, and propose a joint working session with the counterpart's team to close them — then follow up with your director general privately.
D) Stay silent and let the moment pass, then send a corrective email to all parties afterwards.

**Most effective: C. Least effective: A.**

**Explanation:** This is architecture communication under its hardest conditions: senior stakeholders, cross-organisational audience, no preparation. Option C is truthful without being contradictory: it affirms the strategic direction (which is real), names the two issues as *conditions* rather than refusals, converts an awkward moment into a concrete collaborative next step, and preserves the director general's dignity while privately ensuring they understand the position — the "support from stakeholders for high-risk topics" behaviour, performed live. Option B is honest but needlessly public and framed as contradiction; the same facts delivered as "issues to resolve first" change the outcome entirely, and diplomacy in the moment is a skill your role demands. Option D creates a written correction that embarrasses everyone more than a spoken nuance would have, and reads as though you lacked the standing to speak. Option A is least effective: accessibility compliance and data residency are not negotiable garnish — one is an inclusion obligation, the other frequently a legal one — and confirming "definitely" creates a cross-departmental expectation whose later collapse costs far more, in trust and in delivery, than a moment's candour. Public commitments compound; so do public corrections.

**Question 6 (moderate) — The struggling community of practice**

You lead the organisation's architecture community of practice. Attendance has halved over six months. An informal Agile health check tells you why: sessions have become one senior architect presenting his programme's work at length; two experienced women in the community say privately that they no longer feel there is space to contribute; newer architects say the sessions feel "like a broadcast, not a community". The presenting architect is technically excellent and unaware of the effect he is having. Options:

A) Rotate the agenda mechanically — different presenter each session — without addressing anything directly.
B) Speak privately with the presenting architect about the pattern and its effect, redesign the format with the community (short talks, facilitated discussion, rotating ownership, explicit space for newer voices), and ask the two experienced architects what would make participation worthwhile — acting on what they say.
C) Replace the presenting architect as a session lead and announce that sessions will now be discussion-based.
D) Let the community find its own level; communities of practice are voluntary and attendance naturally fluctuates.

**Most effective: B. Least effective: D.**

**Explanation:** Your community collaboration skill is explicit: use health checks to identify problems in team dynamics and rectify them, and stimulate the right responses. Option B addresses all three layers of the problem — the individual (private, developmental feedback to someone acting in good faith; adapting feedback so it is effective and lasting), the structure (formats that create space rather than exhorting people to take it), and the excluded voices (asking, then *acting*, which is what makes consultation credible). The inclusion dimension matters doubly: an architecture community where experienced women conclude there is no space to contribute is losing exactly the perspectives and role models it exists to develop. Option A changes the rota but not the dynamic and gives the architect no chance to grow — pattern-blind fixes produce pattern-shaped recurrences. Option C fixes the symptom by public demotion, humiliating a well-intentioned colleague and teaching the community that feedback arrives as sanction. Option D is least effective: you have diagnostic data telling you participation is collapsing for identifiable, fixable reasons; "voluntary" describes attendance, not your responsibility for the dynamic. A halving community is not fluctuation — it is feedback.

**Question 7 (hard) — Emerging technology pressure**

Your organisation's board has asked every directorate to show progress on generative AI adoption this year. A delivery team you support proposes embedding an AI assistant into a benefits-adjudication workflow to draft decision letters. The team is capable and the supplier demo is impressive. Your assessment: the use case touches decisions with statutory consequences for vulnerable people, no assurance framework for AI-drafted decisions exists in the organisation yet, and two lower-risk, high-value AI use cases (internal knowledge search, correspondence triage) are available. Options:

A) Support the adjudication proposal — the board wants visible progress and this is the most visible option.
B) Block all AI work until a complete organisational assurance framework exists.
C) Steer the portfolio: advocate the two lower-risk use cases as this year's visible progress, and channel the adjudication idea into building the assurance framework it would need — human review, bias evaluation, auditability — with the team as co-designers.
D) Let the team proceed with a pilot, on the basis that pilots are exempt from assurance expectations.

**Most effective: C. Least effective: D.**

**Explanation:** Your duties include proactively seeking digital transformation opportunities *and* using emerging technologies with best practice — the pairing is the point. Option C says yes to the transformation demand and no to the specific risk, which is the mature form of both: the board gets real progress, the organisation gets an assurance framework built against a concrete use case, and the team's energy is redirected rather than rejected — co-designing the framework keeps them invested. Option A optimises for visibility over consequence: AI-drafted statutory decisions affecting vulnerable people, with no assurance framework, is a high-risk architectural decision made for presentational reasons — the profile of failure that ends up in front of committees. Option B is the classic governance over-correction: it protects nothing that option C does not, while forfeiting genuine value and teaching the organisation that architecture is where ideas go to die. Option D is least effective because it is option A wearing a lab coat: "pilot" describes scale, not risk — a pilot that drafts real decision letters for real citizens carries the same per-case consequences with an added implication that assurance is a formality to be waived. Pilots earn exemptions from *scale* commitments, never from safety ones.

**Question 8 (moderate) — The supplier bearing gifts**

A strategic supplier's account director invites you to present your organisation's technology strategy at their international customer conference — flights, accommodation, and a speaking fee covered. The same supplier is expected to bid in a major platform procurement your architecture team will help evaluate next quarter. Options:

A) Accept — presenting the strategy publicly is good for the organisation and the profession.
B) Decline the invitation and, from now on, avoid all contact with this supplier until the procurement concludes.
C) Consult your commercial and propriety colleagues before responding; if speaking is judged appropriate, do it without personal benefits (no fee, expenses via your organisation) and record the interaction in line with procurement conduct rules.
D) Accept the invitation but decline the speaking fee, judging that this removes any conflict.

**Most effective: C. Least effective: A.**

**Explanation:** This tests your representation of architectural governance within *wider* governance — here, commercial and propriety. The live issue is not whether you would be influenced; it is whether a reasonable observer, or an unsuccessful bidder's lawyer, could perceive influence: paid hospitality from an imminent bidder, accepted by an evaluator, is textbook challenge material against a procurement. Option C treats that risk properly — take advice from the people whose job it is, strip out personal benefit, create a record. That is transparency doing its work: the interaction may well be fine, but the *process* that says so cannot be you alone. Option D shows partial awareness but self-certifies: flights and accommodation are also benefits, and "I judged it fine myself" is exactly the sentence that fails review. Option B over-corrects — suppliers with live relationships still need architectural engagement, and monastic avoidance harms delivery without adding protection beyond what disclosure achieves. Option A is least effective: it takes the full package, fee included, from an imminent bidder without consultation or record — each element defensible to yourself, the combination indefensible to anyone else.

**Question 9 (moderate) — The design review you cannot staff**

Four significant design reviews land in the same fortnight, all from teams you support. You can personally lead at most two. The other principal-level architect is on leave. Three senior architects in your community are capable but have never led a high-stakes review; one of them, given the chance, would be reviewing a programme whose lead architect openly doubts her experience. Options:

A) Postpone two reviews until you can lead them personally — quality cannot be compromised.
B) Lead the two highest-risk reviews yourself; delegate the other two to senior architects with a clear brief, your review of their findings before issue, and a pre-emptive message to the sceptical programme lead expressing your confidence in the reviewer and the process.
C) Delegate all four to create maximal development opportunity, making yourself available for questions.
D) Run all four yourself as shortened, one-hour reviews.

**Most effective: B. Least effective: D.**

**Explanation:** The scenario tests whether you scale yourself through others — the essence of supporting multiple teams and inspiring other architects — or remain the bottleneck. Option B triages by risk (your personal attention goes where risk is highest), creates genuine development with genuine safety nets (clear brief, findings reviewed before issue — support without secret re-doing), and handles the credibility threat *before* it undermines the reviewer: your public confidence transfers your authority to her, which is what sponsorship means and how architects come to "understand how to deliver the goals of the organisation" by doing, not watching. Option A protects a standard by missing the moment it exists for — a review after decisions are baked is theatre — and tells your seniors you do not trust them, twice over. Option C mistakes abandonment for empowerment: development needs stretch *and* support, and putting a first-time reviewer in front of a hostile programme lead without backing is how development opportunities become career injuries. Option D is least effective: four token reviews assure nothing while appearing to assure everything — a one-hour skim that stamps a high-risk design is worse than no review, because it converts your assurance signature from information into noise.

**Question 10 (hard) — The blocked strategy**

Eighteen months ago the organisation agreed the technical strategy you authored, including consolidation from three case-management platforms to one. Consolidation has stalled: the two directorates due to migrate cite funding pressure each budget cycle, and their directors privately admit they are waiting each other out — neither wants to fund the shared migration tooling first. Meanwhile both directorates keep extending their legacy platforms. The strategy is now quietly being unwound by inaction. Options:

A) Accept reality and revise the strategy to a three-platform model — a strategy nobody follows is worse than none.
B) Take the pattern to the executive: quantify the cost of the stalemate (duplicate run costs, mounting extension spend, lost benefits), propose breaking the deadlock by centrally funding the shared tooling or sequencing the migrations by executive decision, and ask for the strategy to be explicitly recommitted or explicitly revised.
C) Keep raising consolidation at each directorate's governance boards until one of them moves.
D) Announce that no further legacy platform extensions will receive architectural approval, forcing the migrations.

**Most effective: B. Least effective: C.**

**Explanation:** "Enable the implementation of strategies... by advocating for resources and removing blockers" is nearly a description of option B. The blocker is a first-mover funding stalemate — a structural problem no amount of directorate-level persuasion resolves, because each director's position is locally rational. Structural deadlocks need a decision from the level that spans both parties, and your job is to force that decision honestly: quantified costs, concrete deadlock-breaking options, and — crucially — the demand that the organisation either recommit or *explicitly* revise. A strategy dying by silent inaction is the worst outcome, because everyone still plans against a fiction; option B makes the choice conscious either way, which is what "making sure the strategy is agreed and followed" means when following has stopped. Option A capitulates without ever putting the real choice to the people who own it — revision may be the answer, but it is the executive's call to make with the costs in view, not your pre-emptive surrender. Option D uses governance as a weapon: blocking extensions punishes the delivery teams and their users for their directors' stalemate, and creates operational risk (unsupported platforms) to win a budget argument. Option C is least effective because it is the *status quo* — you have been raising it for eighteen months at the level where the deadlock lives; repetition at the same level with the same audiences is activity impersonating action, and eighteen more months of it is how strategies die politely.

### Preparation tips

- **Anchor on the role, not on yourself.** Answer as the strongest principal architect would act in that organisation, which sometimes differs from your personal instinct. The question is "what is most effective for the organisation and its users", not "what would I prefer".
- **Look for root cause and relationship together.** The best options usually fix the underlying system (a process, a deadlock, an information gap) while preserving or strengthening relationships. If an option does one at the expense of the other, a better option is probably on the list.
- **Beware passive and covert options.** Waiting, staying silent, quiet workarounds, and letting problems find their own level score poorly at every level — and especially at yours, where inaction by the accountable person is itself a decision.
- **Use the profession's values as a tiebreaker.** When two options both seem strong, prefer the one with more transparency, more collaboration, more inclusion, and better outcomes for users. That is genuinely how scoring keys for public sector roles are built.
- **Rehearse aloud.** Talk through two or three dilemmas from your own recent history — what you did, what the option set really was, why. Making your judgement explicit is the best preparation this format allows, and it is interview preparation at the same time.

### Common pitfalls

- **Answering idealistically.** Options that sound noble but ignore practical constraints — "block everything until perfect assurance exists" — score poorly. Effectiveness, not purity, is the criterion.
- **Deference disguised as judgement.** At senior levels the tempting error flips: not passivity toward problems but passivity toward power — confirming the director general, accepting the delivery director's fait accompli. Rank does not change the risk profile of a bad decision.
- **Overusing escalation.** Escalation is a legitimate tool that weak answers reach for first. Strong answers usually show what you did with your own influence before spending anyone else's.
- **Solving the presenting problem only.** Reassigning the dominant presenter, forbidding the workaround, postponing the reviews — symptom fixes leave the generating pattern intact and are marked accordingly.
- **Forgetting you are being assessed on values.** Accessibility, inclusion, transparency, and user needs are not decorative in UK public sector scoring keys; options that trade them away for speed or comfort are reliably the "least effective" answers.

## Conclusion

You have worked through four substantial assessment formats — cognitive, numeric reasoning, verbal reasoning, and situational judgement — every part of it grounded in the real substance of your role as a principal technical architect: the strategies you design and steward, the high-risk decisions you make and guide, the governance you lead and evolve, the teams you support, and the architects you coach and inspire.

If you take away one idea, let it be this: these assessments are not alien hurdles but structured mirrors of thinking you already do daily. Deducing what follows from governance rules, checking a business case against its own annexe, reading the exact force of a "normally" in a standard, choosing the response that fixes the system while strengthening the relationship — this is your ordinary work, made explicit and timed. Preparation is therefore less about learning new material than about making your existing judgement fast, precise, and consistent under assessment conditions.

Between now and any real assessment: revisit the sections where the explanations surprised you, because surprise marks the highest-value practice; rehearse the core numeric moves until they are automatic; practise the True / False / Cannot Say discipline on documents you handle anyway; and talk through a few of your own hardest judgement calls with a trusted peer. Fifteen focused minutes a day for two weeks outperforms a single long session the night before — and arrive rested, because at your level the margin between good and excellent performance is mostly composure.

Finally, remember that this material serves your development beyond any single assessment. The same skills that earn strong scores — rigorous reading, honest numbers, transparent decisions, judgement that balances pace with risk and authority with collaboration — are the skills that make technical strategy real across an organisation. Investing in them is investing in the leader you are becoming for the profession, and in the architects who are watching how you work and learning from it. You operate at the highest technical level of your profession; walk into the assessment the way you walk into a difficult governance board — prepared, calm, and genuinely curious. Good luck.

