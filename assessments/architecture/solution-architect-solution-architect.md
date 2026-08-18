# Solution Architect - Psychometric Assessment Resources

## Introduction

Welcome! This document is written for you: a solution architect working within the UK Government Digital and Data (GDAD) Profession Capability Framework. Whether you are preparing for an internal assessment, applying for a new post, or simply want to sharpen the mental skills you use every day, this resource is designed to help you practise, reflect, and build confidence.

Psychometric assessments are structured, standardised exercises that measure the thinking skills and judgement a role genuinely requires. They are widely used across the Civil Service and the wider public sector because they are fair, evidence-based, and focused on capability rather than background. For a solution architect, they matter in a very practical way: your role asks you to define problems precisely, weigh options under constraint, interpret technical and commercial data, read dense standards and policy documents accurately, and make transparent decisions with stakeholders across the organisation. Those are exactly the capabilities that psychometric assessments are built to measure.

This document is organised around four assessment types, each in its own section:

1. **Workplace job-specific cognitive assessment** - measures how you recognise patterns, deduce conclusions, spot errors, and prioritise using the kinds of artefacts you handle every day: architecture diagrams, decision records, dependency maps, and governance checklists.
2. **Workplace job-specific numeric reasoning assessment** - measures how you interpret tables, percentages, ratios, budgets, capacity figures, and performance metrics of the kind that appear in options analyses, business cases, and cloud cost reports.
3. **Workplace job-specific verbal reasoning assessment** - measures how precisely you read and reason from written material such as technology standards, governance policies, stakeholder emails, and assurance reports.
4. **Workplace job-specific situational judgement assessment** - measures the quality of your professional judgement in realistic dilemmas involving delivery teams, senior stakeholders, governance boards, and suppliers.

Each section explains what the assessment measures, maps it to the specific skills in your role profile (such as making architectural decisions, problem definition and shaping, architecture communication, and strategy design), and then gives you a substantial set of practice questions with worked answers. Each section closes with preparation tips and common pitfalls.

How should you use this document? Three ways work well. First, as **practice**: attempt the questions under light time pressure, then study the explanations carefully, because the reasoning matters more than the answer. Second, as **self-reflection**: notice which question types feel effortful, and treat that as a signal for development. Third, as **preparation**: in the days before a real assessment, revisit the tips and pitfalls so the format holds no surprises.

Take your time, be kind to yourself when you get a question wrong, and remember: every question here is drawn from the real work of a solution architect. Practising them is practising your job. Let's begin.

## Advisory

"This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff."

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive assessment is a targeted psychometric test that measures the exact mental processes your role requires, using practical workplace scenarios rather than abstract puzzles. Unlike a generic IQ test, every item is built from the tasks and data formats of the actual job, which makes it a much better predictor of on-the-job performance.

For you as a solution architect, that means the questions will look like your working week: reading a dependency diagram and deducing what breaks if a component is removed; checking an architecture decision record for internal contradictions; spotting the error in a governance checklist; working out which of five competing tasks to do first when a design review, a security risk, and a stakeholder escalation all land on the same morning.

Typical format and timing: these assessments are usually delivered online, timed at around 15 to 30 minutes, and scored objectively against a benchmark or norm group. Many platforms give you short, ungraded practice questions first so you can get used to the interface, and some are adaptive, adjusting difficulty based on your previous answers. Employers typically receive a breakdown of speed versus accuracy rather than a single score, so working carefully and steadily is a genuinely good strategy - you do not need to rush recklessly.

Why does this matter for your role? A solution architect is responsible for a single solution, usually working independently where risk is low, and supporting more senior architects on larger work. That independence means your reasoning is often the first and only quality gate: if you misread a constraint, mis-order a migration sequence, or fail to notice that two requirements contradict each other, the error can travel a long way before anyone catches it. Cognitive assessments measure precisely that first-gate reliability.

### What it measures for your role

The assessment dimensions map directly onto the skills in your role profile:

- **Problem definition and shaping**: framing a problem of medium complexity so a solution can be created, and describing options clearly. Cognitive items test this through logical deduction and problem-structuring questions - given a messy set of facts, can you isolate what is actually true and what follows from it?
- **Making architectural decisions**: working with others to make design decisions with managed levels of risk and complexity, and identifying architectural risks across business, data, and security domains. Items test this through prioritisation and risk-ordering questions.
- **Technical design throughout the life cycle**: creating technical designs with managed risk, impact, and complexity, and adapting designs during delivery. Items test this through pattern recognition in system structures and sequencing questions about dependencies.
- **Architect for the whole context**: aligning your work with other architects and tracking emerging issues and patterns over time. Items test this through error-checking questions where a local detail contradicts the wider picture.
- **Architecture communication**: leading communication of complicated or risky topics. While communication itself is tested more directly in the verbal section, cognitive items test the underlying clarity of thought - can you identify the one statement that accurately summarises a complex situation?

### Practice questions

Work through these at a steady pace. Aim for about 90 seconds to 3 minutes per question depending on difficulty. Answers and full reasoning follow each question.

#### Question 1 (easy) - Dependency deduction

You are documenting a solution with five components. The design notes state:

- The Citizen Portal depends on the Identity Service.
- The Identity Service depends on the Audit Log.
- The Case Management API depends on the Identity Service and the Document Store.
- The Document Store has no dependencies.

The infrastructure team proposes taking the Audit Log offline for maintenance during working hours. Which components will be affected?

A. Only the Identity Service
B. The Identity Service, the Citizen Portal, and the Case Management API
C. The Identity Service and the Citizen Portal only
D. All five components

**Correct answer: B.**

**Explanation:** Trace the dependency chain. The Audit Log going offline directly affects the Identity Service (which depends on it). Anything depending on the Identity Service is then affected transitively: the Citizen Portal and the Case Management API both depend on it. The Document Store has no dependencies at all, so it is unaffected, which rules out D. Option C misses the Case Management API's dependency on the Identity Service. This is exactly the transitive reasoning you use when assessing the blast radius of a change - a core part of identifying architectural risks relevant to your team or domain.

#### Question 2 (easy) - Error checking in an architecture decision record

An architecture decision record (ADR) in your team's repository reads:

> "Decision: We will adopt the department's approved managed database service for the new licensing solution. Rationale: it reduces operational burden and is already assured by the security team. Consequence: the team must build and patch its own database servers, and must schedule quarterly security reviews of the operating system."

What is wrong with this ADR?

A. The decision is missing a date
B. The consequence contradicts the decision and rationale
C. The rationale does not mention cost
D. Nothing is wrong; it follows the standard ADR format

**Correct answer: B.**

**Explanation:** A managed database service means the provider handles server builds and operating system patching - that is the "reduced operational burden" the rationale cites. Yet the consequence says the team must build and patch its own database servers, which describes a self-managed approach. The record contradicts itself. Options A and C describe things that might improve the ADR but are not logical errors in it, and the question asks what is wrong, not what could be better. Spotting internal contradictions in design documents is bread-and-butter error checking for a solution architect: documents like this are implemented by delivery teams, so a contradiction left in place becomes a build-time dispute.

#### Question 3 (moderate) - Pattern recognition in integration styles

You review four recent solution designs from your architecture community, looking for the pattern your organisation is converging on:

- Design 1: services publish events to a message broker; consumers subscribe; no service calls another service directly.
- Design 2: services publish events to a message broker for state changes, but use direct synchronous calls for real-time queries.
- Design 3: services publish events for state changes; real-time queries go through direct synchronous calls; batch data moves via nightly file transfer.
- Design 4: state changes via events; real-time queries via synchronous calls; batch data via nightly file transfer; and all external partner integrations pass through a central API gateway.

A fifth design is being drafted for a solution with state changes, real-time queries, batch reporting, and one external partner. Following the established pattern trajectory, what should the fifth design include?

A. Events only, since Design 1 is the purest pattern
B. Events for state changes, synchronous calls for queries, file transfer for batch, and the API gateway for the external partner
C. Synchronous calls for everything, since they are simplest
D. A new integration style, since each design so far has been different

**Correct answer: B.**

**Explanation:** The four designs are not random variations - each one keeps everything from the previous design and adds one refinement for a new need: queries (Design 2), batch (Design 3), external partners (Design 4). The pattern is cumulative convention, not divergence, which rules out D. Option A ignores that later designs deliberately added synchronous queries because events alone did not serve real-time needs. Option C throws away the established event-driven convention. The fifth solution has all four needs, so it should apply all four conventions - option B. This mirrors the skill "architect for the whole context": tracking patterns across other architects' work over time and aligning your design with them, rather than inventing a local exception.

#### Question 4 (moderate) - Prioritisation under constraint

It is 09:00 on Monday. You have the following items competing for your day:

1. A delivery team is blocked: they need you to confirm whether the design permits caching personal data at the edge (they can do other work until 14:00, then they are idle).
2. The design assurance board meets Wednesday and requires your solution design pack two working days in advance - meaning it is due by end of today.
3. A senior architect asks you to review a strategy document by Friday.
4. A supplier email flags that a product in your design reaches end-of-support in 18 months.
5. A colleague asks you to present your problem-framing approach at the community of practice next month.

Which ordering best reflects sound prioritisation for today?

A. 2, 1, 4, 3, 5
B. 1, 2, 3, 4, 5
C. 2, 1, 3, 4, 5
D. 1, 2, 4, 3, 5

**Correct answer: C.**

**Explanation:** Two items are genuinely due today: the assurance pack (hard deadline, end of today, and missing it slips governance by a full board cycle) and the caching answer (the team is blocked from 14:00). The pack is the larger, less compressible piece of work with the earlier effective start requirement, so it leads; the caching question is important but answerable in a bounded conversation before 14:00 - so 2 then 1. Note that a strong real-world move is to timebox the caching answer mid-morning, which ordering C accommodates. Next comes item 3: it has a real deadline this week and serves a senior colleague's timeline, whereas item 4's end-of-support horizon is 18 months away - it needs logging on the risk register soon, but not before a Friday commitment. Item 5 is a month out. Options A and D promote the 18-month risk above a this-week deliverable, and B treats the soft-blocked team as more urgent than a hard end-of-day governance deadline. Prioritisation questions like this test whether you distinguish urgency (time criticality) from importance (impact) - central to managing risks and decisions in a transparent way.

#### Question 5 (moderate) - Logical deduction from constraints

Your solution must comply with these constraints from the technical design authority:

- If a service stores personal data, it must be hosted in the approved UK cloud regions.
- If a service is hosted in the approved UK cloud regions, it must use the central logging platform.
- The Notifications Service does not use the central logging platform.

What can you validly conclude about the Notifications Service?

A. It stores personal data but is hosted elsewhere
B. It does not store personal data
C. It is hosted in the approved UK cloud regions
D. Nothing can be concluded

**Correct answer: B.**

**Explanation:** This is a chain of contrapositives. From constraint 2: if a service does not use central logging, it is not hosted in the approved UK regions. The Notifications Service does not use central logging, so it is not in the approved regions. From constraint 1: if a service is not in the approved regions, it does not store personal data (contrapositive again). Therefore the Notifications Service does not store personal data - assuming, as the question requires, that the constraints are being complied with. Option A would describe a compliance breach, but the question asks what validly follows from the constraints as given. Working backwards through rule chains like this is exactly how you verify that a design complies with standards and governance before a review board does it for you.

#### Question 6 (moderate) - Sequencing a migration

You are designing the migration of a legacy licensing system to a new platform. The steps, with their prerequisites, are:

- Step P: Provision the new environment (no prerequisites).
- Step Q: Migrate reference data (requires P).
- Step R: Deploy the new application (requires P).
- Step S: Run parallel processing to compare outputs (requires Q and R).
- Step T: Switch users to the new system (requires S and sign-off at a governance gate, which takes five working days after S completes).
- Step U: Decommission the legacy system (requires T plus a 30-day rollback window).

The programme manager asks: "What is the earliest point we can start the governance gate paperwork to avoid the five-day wait?" What is the most accurate answer?

A. After Step T, since governance approves the switch after it happens
B. The gate clock starts when S completes, so prepare paperwork during S and submit the moment S finishes
C. Immediately, since governance is independent of delivery
D. After Step U, at the end of the programme

**Correct answer: B.**

**Explanation:** The constraint says sign-off takes five working days *after S completes* - so the clock cannot start earlier than S's completion, which rules out C in its strong form. But nothing prevents preparing the paperwork in parallel while S runs, so the wait is minimised by submitting immediately when S finishes. Option A reverses cause and effect: governance approval is a prerequisite for T, not a follow-up. Option D confuses the gate with programme closure. This is critical-path reasoning: identifying which dependencies are hard (the five-day clock after S) and which are soft (paperwork preparation), a routine part of providing guidance and support to teams using technical designs throughout the life cycle.

#### Question 7 (moderate) - Odd one out in non-functional requirements

Four non-functional requirements appear in your draft design for a public-facing service:

1. "The service must return search results within 2 seconds for 95% of requests at peak load of 500 concurrent users."
2. "The service must be available 99.5% of the time, measured monthly, excluding planned maintenance announced 5 days ahead."
3. "The service must be highly secure."
4. "The service must meet WCAG 2.2 AA accessibility criteria, verified by audit before public beta."

Which requirement is the odd one out, and why?

A. Requirement 1, because performance targets belong in a service level agreement, not a design
B. Requirement 3, because it is not measurable or testable as written
C. Requirement 4, because accessibility is a legal duty rather than a requirement
D. Requirement 2, because availability cannot exclude planned maintenance

**Correct answer: B.**

**Explanation:** Requirements 1, 2, and 4 each contain a measurable threshold and a verification condition: response time with percentile and load, availability percentage with measurement window, accessibility standard with audit gate. Requirement 3 states an aspiration with no threshold, no standard, and no test - you could neither design to it nor assure against it. Option A is wrong because performance targets absolutely belong in a solution design (they drive capacity and technology choices). Option C is confused: accessibility being a legal duty in the UK public sector makes it *more* important to state as a testable requirement, not less. Option D is factually wrong; availability targets commonly exclude announced maintenance. Recognising untestable requirements is part of challenging requirements and assumptions - a named behaviour in your strategy design skill.

#### Question 8 (hard) - Deduction with incomplete information

Three teams contribute to your solution. You know:

- Every component owned by Team Alpha has passed security review.
- Some components owned by Team Beta have not passed security review.
- The Payments Adapter has passed security review.
- The Reporting Module is owned by Team Beta.

Which one of the following statements must be true?

A. The Payments Adapter is owned by Team Alpha
B. The Reporting Module has not passed security review
C. If the Reporting Module has passed security review, it is not one of the Team Beta components that failed
D. Team Beta owns the Payments Adapter

**Correct answer: C.**

**Explanation:** Work through each option against the facts. A: passing security review is guaranteed for Alpha's components, but nothing says only Alpha's components pass - the Payments Adapter could belong to Beta or a third team and still have passed. Not forced. B: only *some* Beta components have failed; the Reporting Module might be among those that passed. Not forced. D: no ownership information links the Payments Adapter to Beta. Not forced. C is true almost by definition: a component that has passed cannot simultaneously be one that has not passed - it is the only statement that must hold in every scenario consistent with the facts. This question trains you to resist over-reading evidence, the same discipline you need when an assurance report says "some issues were found in the supplier's components" and a stakeholder asks you whether a specific component is affected. The transparent answer is often "the evidence does not tell us" - and recognising that is a skill.

#### Question 9 (hard) - Error checking a capacity plan

A delivery team sends you their capacity plan for review:

> "The service will support 10,000 registered users. We expect 20% of registered users to be active in any given hour at peak. Each active user generates on average 6 requests per minute. Therefore peak load is 10,000 × 0.20 × 6 = 12,000 requests per minute. Each application server handles 100 requests per second, so we need 12,000 ÷ 100 = 120 servers, plus one for resilience, totalling 121 servers."

There is a units error in this plan. What is the correct number of servers before the resilience addition?

A. 120
B. 12
C. 2
D. 20

**Correct answer: C.**

**Explanation:** The peak load arithmetic is right: 10,000 × 0.20 = 2,000 active users; 2,000 × 6 = 12,000 requests *per minute*. But server capacity is quoted *per second*. Convert: 12,000 requests per minute ÷ 60 = 200 requests per second. At 100 requests per second per server, you need 200 ÷ 100 = 2 servers, not 120. The team divided requests-per-minute by requests-per-second - a classic units mismatch that inflates the estimate sixty-fold, and with it the hosting budget. Catching mixed units in someone else's arithmetic is one of the highest-value error checks a solution architect performs: a design that provisions 121 servers where 3 would do fails the organisation's financial constraints just as surely as one that under-provisions fails its users.

#### Question 10 (hard) - Prioritising architectural risks

You maintain a risk register for your solution. Four risks are open:

- Risk W: A key open-source library used for document rendering has announced end-of-life in 24 months. Likelihood of impact: certain, eventually. Severity if unmitigated: high. Mitigation effort: moderate, can be scheduled.
- Risk X: The solution currently has no rate limiting on its public API. A similar service in another department suffered a denial-of-service incident last month. Likelihood: moderate to high. Severity: high, service outage. Mitigation effort: small.
- Risk Y: The design assumes a second data centre region that the hosting team has not yet confirmed. Likelihood of assumption failing: unknown. Severity: high, redesign required. Mitigation effort to resolve: trivial - a confirmation email.
- Risk Z: Two junior developers are unfamiliar with the chosen framework. Likelihood of some delay: high. Severity: low to moderate. Mitigation: training, small effort.

Which risk should you act on first, and why?

A. Risk W, because it is certain to occur
B. Risk X, because severity and likelihood are both high and the fix is small
C. Risk Y, because a trivial action removes a potentially design-breaking unknown
D. Risk Z, because it is the most likely to occur

**Correct answer: C.**

**Explanation:** This is a question about the *order of action*, not the ranking of raw severity. Risk Y is an unvalidated assumption underpinning the whole design: if the second region is not available, everything else - including your mitigation plans for W, X, and Z - may need rework. And the cost of finding out is a single email. Highest information value per unit effort, and it de-risks the foundation the other decisions stand on: act on it first, today. Risk X is the strongest competing answer and should be acted on immediately afterwards (small fix, high likelihood, high severity) - in practice you might send the Risk Y email and start the Risk X work the same morning, but the question asks what comes first. Risk W is certain but distant, with time to schedule. Risk Z is real but low-severity. Option A confuses certainty with urgency; option D confuses likelihood with impact. This judgement - resolve foundational unknowns cheaply and early, then attack high-exposure risks - reflects engaging with architectural governance and assurance to manage decisions and risks in a transparent way.

#### Question 11 (hard) - Pattern completion in environment promotion

Your organisation promotes code through environments using a strict pattern. Recent release records show:

- Release 1: Dev → Test → Staging → Production. Automated tests at each gate. Manual accessibility check at Staging.
- Release 2: Dev → Test → Staging → Production. Automated tests at each gate. Manual accessibility check at Staging. Rollback rehearsal at Staging.
- Release 3: Dev → Test → Staging → Production. Automated tests at each gate. Manual accessibility check at Staging. Rollback rehearsal at Staging. Security scan moved earlier, into Test.

A colleague drafts the plan for Release 4 as: "Dev → Staging → Production, automated tests at each gate, accessibility check at Staging, rollback rehearsal at Staging, security scan at Test." What is wrong with the draft?

A. It adds too many checks for a routine release
B. It references a security scan at Test but has removed the Test environment from the path
C. Rollback rehearsals should happen in Production
D. Nothing is wrong; environments can be skipped when teams are confident

**Correct answer: B.**

**Explanation:** The established pattern across all three releases keeps a four-stage path and *adds or shifts* controls - it never removes a stage. The draft removes Test from the promotion path yet still assigns the security scan to Test, an internal contradiction: the control now has no environment to run in. Option A is backwards - the trajectory has been adding controls, and the draft does not add any. Option C is unsafe practice and contradicts the observed pattern. Option D might be arguable in some organisations, but even then the draft would still be internally inconsistent, which is the detectable error. This combines two skills tested throughout this assessment: recognising the trajectory of a pattern over time, and checking a document against itself.

#### Question 12 (hard) - Problem framing

A programme director tells you: "The case management team says their system is too slow, the contact centre says citizens complain about waiting for decisions, and finance says overtime costs are up 30%. Fix the system performance."

Before accepting "system performance" as the problem, which single question is most valuable to ask first?

A. "What response time does the case management system currently deliver?"
B. "Do the citizen waiting times and overtime costs actually correlate with system response times, or with something else such as case volume or process steps?"
C. "Which database does the case management system use?"
D. "What budget is available for performance improvements?"

**Correct answer: B.**

**Explanation:** Three symptoms have been attributed to one cause, but the attribution is untested. Waiting for decisions and rising overtime could equally be driven by case volume growth, staffing gaps, or a process bottleneck - in which case even an infinitely fast system changes little. Option B tests the causal claim before committing to a solution direction, which is the essence of ensuring a problem and the desired outcomes are properly defined - the first duty in your role profile. Option A gathers a useful fact but assumes the frame; C jumps to implementation detail; D asks about means before the problem is defined. Frame first, solve second: the most expensive mistake a solution architect can make is efficiently solving the wrong problem.

### Preparation tips

- **Practise with your own artefacts.** Take a real ADR, dependency diagram, or risk register from your work and quiz yourself: what follows if X changes? Where do these two documents disagree? The assessment format will feel familiar because it is your job in miniature.
- **Learn the contrapositive.** Many deduction questions hinge on reasoning of the form "if A then B; not B; therefore not A". Practise it until it is automatic - it is the logical backbone of compliance checking.
- **Check units and scales before arithmetic.** Per-second versus per-minute, thousands versus millions. Make it a reflex to state the units of every number before you calculate with it.
- **Distinguish "must be true" from "could be true".** When a question asks what must follow, actively try to construct a counterexample for each option. If you can imagine a consistent scenario where the option is false, it is not the answer.
- **Manage the clock kindly.** With 15 to 30 minutes for the whole test, no single question deserves five. Flag, skip, return. Accuracy on the questions you answer matters more than heroics on the hardest one.
- **Warm up beforehand.** Do two or three practice questions just before the real test so your first scored question is not also your first question of the day.

### Common pitfalls

- **Answering from experience instead of from the material.** You know how migrations usually go; the question describes how *this* one goes. Base every inference strictly on the stated facts - the same discipline governance boards expect of your design rationale.
- **Missing the internal contradiction.** Job-specific cognitive tests love documents that disagree with themselves, because real documents do. Read consequences against decisions, totals against line items, paths against controls.
- **Confusing severity with priority.** The biggest risk is not always the first action; sometimes a trivial step that resolves an unknown comes first. Test-writers know architects fall for the "biggest number wins" trap.
- **Time-sink questions.** Getting stuck on a single multi-stage problem instead of banking easier marks elsewhere is the most common cause of underperformance on timed cognitive tests.
- **Rushing the question stem.** "Which must be true?", "What is wrong?", and "What comes first?" are different questions with different answers about the same scenario. Read the ask twice.


## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment evaluates your ability to analyse, interpret, and make sound decisions using numerical data in the formats your role actually produces and consumes. It is business mathematics, not abstract formulae: percentages, ratios, cost comparisons, capacity figures, and trend reading, presented in tables, charts, and short briefs.

For you as a solution architect, the numbers in question are the numbers of your working life: options analyses comparing the total cost of build-versus-buy; cloud hosting estimates with compute, storage, and data-transfer components; licence and support costs across sourcing strategies; availability percentages and what they mean in minutes of downtime; capacity and throughput figures in performance requirements; and delivery metrics such as velocity and defect rates that tell you whether a technical design is surviving contact with reality.

Typical format and timing: most numeric reasoning assessments are online, strictly timed (often around 45 to 90 seconds per question across 20 to 30 minutes), and calculator-friendly - many provide an on-screen calculator, because the test prioritises interpretation over mental arithmetic. The data is usually presented in realistic exhibits: a table comparing options, a budget breakdown, a performance dashboard. The skill being measured is extracting the right numbers quickly and combining them correctly, not multiplying large numbers in your head.

Why it matters for your role: your role profile requires you to understand organisational objectives and external drivers, explicitly including financial constraints, to bring a commercial perspective including different sourcing strategies, and to describe options for solving problems so that delivery methods can be decided. Every one of those duties runs on numbers. An options paper with a broken percentage misleads a governance board; a capacity figure with mixed units misleads a delivery team; a misread licence table misleads a commercial colleague. Numeric reasoning is how your designs stay honest.

### What it measures for your role

- **Commercial perspective**: understanding commercial processes and sourcing strategies means comparing costs across suppliers, contract periods, and pricing models - tested here through cost tables, licence calculations, and total-cost-of-ownership questions.
- **Making architectural decisions**: decisions characterised by managed risk need quantified trade-offs. Tested through options-comparison questions where cost, capacity, and risk figures must be combined.
- **Problem definition and shaping**: describing options so delivery methods can be decided requires accurate baseline figures and projections. Tested through percentage change, trend, and estimation questions.
- **Technical design throughout the life cycle**: capacity planning, availability targets, and performance budgets are numeric artefacts of technical design. Tested through throughput, utilisation, and downtime arithmetic.
- **Strategy design and understanding financial constraints**: supporting strategy with a roadmap or plan means phased budgets and benefit projections. Tested through multi-year cost and benefits questions.

### Practice questions

An on-screen calculator is assumed to be available. Show yourself the working even when you use it - the discipline of writing the calculation is what prevents errors under time pressure.

#### Question 1 (easy) - Percentage of budget

Your solution has an approved budget of £480,000 for the year. The hosting component is forecast at £84,000. What percentage of the budget is hosting?

A. 14.5%
B. 17.5%
C. 21.0%
D. 8.4%

**Correct answer: B.**

**Explanation:** Percentage = part ÷ whole × 100 = 84,000 ÷ 480,000 × 100 = 0.175 × 100 = 17.5%. A quick sanity check: 10% of 480,000 is 48,000, and 20% is 96,000; since 84,000 sits between those, the answer must be between 10% and 20%, which eliminates C and D immediately. Estimation brackets like this are your fastest defence against slips.

#### Question 2 (easy) - Availability in minutes

A service level agreement commits your solution to 99.5% availability, measured monthly. Using a 30-day month (43,200 minutes), what is the maximum allowable downtime per month?

A. 43.2 minutes
B. 216 minutes
C. 21.6 minutes
D. 432 minutes

**Correct answer: B.**

**Explanation:** Allowable downtime = (100% − 99.5%) × total minutes = 0.5% × 43,200 = 0.005 × 43,200 = 216 minutes, or 3.6 hours. A common error is treating 0.5% as 0.05 (which gives 2,160) or as 0.0005 (which gives 21.6, option C). Translating availability percentages into real minutes is a conversation you will have with every service owner who asks "what does 99.5% actually mean for my users?" - and being fluent in it makes your designs concrete instead of abstract.

#### Question 3 (easy) - Ratio in team capacity

A delivery plan allocates developer effort across your solution in the ratio 5:3:2 for build, integration, and testing respectively. The team has 40 developer-days available this sprint. How many developer-days go to integration?

A. 12
B. 8
C. 20
D. 15

**Correct answer: A.**

**Explanation:** The ratio parts total 5 + 3 + 2 = 10. Each part is therefore 40 ÷ 10 = 4 developer-days. Integration gets 3 parts: 3 × 4 = 12 developer-days. Build gets 20 (option C is build's figure, a classic distractor: the test-writer knows you might grab the wrong row) and testing gets 8 (option B). Always re-read which category the question asks about before answering.

#### Question 4 (moderate) - Comparing hosting options

You are preparing an options analysis for hosting a new service. The table shows monthly estimates:

| Option | Compute | Storage | Data transfer | Support |
|---|---|---|---|---|
| A: Current provider | £6,200 | £1,800 | £900 | £1,100 |
| B: Approved framework provider | £5,400 | £2,100 | £1,300 | £800 |
| C: Managed platform | £7,800 | £1,200 | £400 | £0 |

Which option has the lowest total monthly cost, and by how much compared with the next cheapest?

A. Option B, by £400
B. Option C, by £200
C. Option B, by £200
D. Option A, by £100

**Correct answer: B.**

**Explanation:** Total each row. Option A: 6,200 + 1,800 + 900 + 1,100 = £10,000. Option B: 5,400 + 2,100 + 1,300 + 800 = £9,600. Option C: 7,800 + 1,200 + 400 + 0 = £9,400. Hosting option C is cheapest at £9,400, and the next cheapest is hosting option B at £9,600, a difference of £200. So the correct *answer choice* is B: "Option C, by £200."

Notice the trap built into this question: the hosting options and the answer choices both use the letters A, B, and C, but they are two separate label sets. Having correctly calculated that hosting option C wins, many candidates reflexively select answer choice C - which pairs the wrong option with the right amount. Under time pressure, label-mapping errors like this are more common than arithmetic errors, in tests and in real options papers alike. Slow down at exactly the moment you transfer a result onto the answer sheet.

#### Question 5 (moderate) - Percentage change in performance metrics

After a design change you made to the caching layer, the service's average response time falls from 850 milliseconds to 510 milliseconds. What is the percentage improvement?

A. 34%
B. 40%
C. 66.7%
D. 60%

**Correct answer: B.**

**Explanation:** Percentage change = (old − new) ÷ old × 100 = (850 − 510) ÷ 850 × 100 = 340 ÷ 850 × 100 = 40%. The commonest error is dividing by the new value: 340 ÷ 510 = 66.7% (option C), which overstates your improvement - not a claim you want to defend at a design review. Percentage changes are always relative to the starting point unless explicitly stated otherwise. When you report performance improvements to stakeholders, quoting the baseline alongside the percentage ("40% faster, from 850ms to 510ms") is both transparent and audit-proof.

#### Question 6 (moderate) - Licence cost across sourcing strategies

A commercial colleague asks you to compare two sourcing strategies for a document management capability over 3 years:

- Strategy 1 (Commercial off-the-shelf): licence £45 per user per year, one-off implementation £60,000, annual support £18,000. User base: 800 users.
- Strategy 2 (Build on existing platform): no per-user licence, development cost £150,000 in year 1, annual maintenance £35,000 starting in year 1.

What is the 3-year total cost of each strategy?

A. Strategy 1: £222,000; Strategy 2: £255,000
B. Strategy 1: £168,000; Strategy 2: £220,000
C. Strategy 1: £222,000; Strategy 2: £220,000
D. Strategy 1: £180,000; Strategy 2: £255,000

**Correct answer: A.**

**Explanation:** Strategy 1: licences = £45 × 800 users = £36,000 per year × 3 years = £108,000; implementation = £60,000 once; support = £18,000 × 3 = £54,000. Total = 108,000 + 60,000 + 54,000 = £222,000. Strategy 2: development = £150,000; maintenance = £35,000 × 3 = £105,000 (it starts in year 1, so three payments). Total = 150,000 + 105,000 = £255,000. Option C's £220,000 comes from charging only two years of maintenance - the classic "does year 1 count?" error; the question says maintenance starts in year 1, so it does. Reading the payment schedule as carefully as the amounts is central to the commercial perspective your role requires: when to apply each sourcing strategy often turns on exactly this kind of multi-year comparison.

#### Question 7 (moderate) - Throughput and capacity headroom

Your technical design specifies that the message queue consumer must process 250 messages per second at peak. Load testing shows one consumer instance processes 40 messages per second. Governance requires 30% headroom above peak. How many consumer instances does the design need?

A. 7
B. 8
C. 9
D. 10

**Correct answer: C.**

**Explanation:** Required capacity with headroom = 250 × 1.30 = 325 messages per second. Instances needed = 325 ÷ 40 = 8.125. You cannot deploy 0.125 of an instance, and rounding down to 8 gives only 320 messages per second - below the 325 target - so round *up*: 9 instances. Option A (7) is peak without headroom rounded up (250 ÷ 40 = 6.25 → 7). Option B is the "round to nearest" trap. Capacity arithmetic almost always rounds up, because the consequence of rounding down is a breached requirement. State this rounding rule explicitly in your design documents so delivery teams do not silently round the other way.

#### Question 8 (moderate) - Reading a delivery dashboard

A delivery dashboard for your solution shows sprint data:

| Sprint | Planned story points | Completed story points | Defects raised | Defects fixed |
|---|---|---|---|---|
| 12 | 40 | 36 | 8 | 6 |
| 13 | 40 | 34 | 12 | 9 |
| 14 | 42 | 30 | 15 | 10 |
| 15 | 38 | 27 | 18 | 11 |

Which statement is best supported by the data?

A. The team's completion rate is stable and defects are under control
B. Completion rate is declining while the open defect backlog grows each sprint, suggesting the design or delivery approach needs attention
C. The team is planning too little work
D. Defect fixing has slowed down

**Correct answer: B.**

**Explanation:** Completion rate per sprint: 36/40 = 90%, 34/40 = 85%, 30/42 ≈ 71%, 27/38 ≈ 71%. That is a clear decline (rules out A). Net new open defects per sprint (raised minus fixed): +2, +3, +5, +7 - the backlog grows every sprint and at an accelerating rate. Option D is contradicted: fixes went 6, 9, 10, 11, so fixing has speeded up in absolute terms; it simply cannot keep pace with the rise in defects raised. Option C is not supported - planned points are roughly constant. The pattern of falling throughput plus compounding defect debt is exactly the signal that should prompt you, as the architect, to ask whether the technical design is proving harder to implement than expected and whether it needs adapting during delivery - a named behaviour in your technical design skill.

#### Question 9 (hard) - Cumulative cost crossover

Continuing from Question 6's two strategies (COTS: £36,000 per year licences + £60,000 one-off + £18,000 per year support; Build: £150,000 year 1 development + £35,000 per year maintenance from year 1), in which year does the Build strategy's cumulative cost first become cheaper than the COTS strategy's cumulative cost?

A. Year 3
B. Year 4
C. Year 5
D. Never within 10 years

**Correct answer: C.**

**Explanation:** Build a year-by-year cumulative table. COTS annual running cost = 36,000 + 18,000 = £54,000, plus £60,000 once in year 1, so cumulative COTS = 114,000; 168,000; 222,000; 276,000; 330,000. Build: year 1 = 150,000 + 35,000 = £185,000; then +£35,000 per year, so cumulative Build = 185,000; 220,000; 255,000; 290,000; 325,000. Compare year by year: year 3: 222,000 vs 255,000 (COTS cheaper); year 4: 276,000 vs 290,000 (COTS still cheaper, by £14,000); year 5: 330,000 vs 325,000 - Build is now cheaper by £5,000, for the first time. The crossover is year 5, option C. The trap in crossover questions is stopping at year 3 or 4, seeing COTS ahead, and concluding "never" (option D) - the gap was narrowing by roughly £19,000 per year (COTS costs £54,000 annually versus Build's £35,000), so the crossover was inevitable; the only question was when. Cumulative cost crossover is a standard exhibit in sourcing decisions, and being able to build this little table live in a meeting is a quiet superpower: it converts "build versus buy" arguments from opinion into arithmetic that everyone can inspect - transparency in decision-making, exactly as your role profile requires.

#### Question 10 (hard) - Weighted scoring in an options appraisal

Your options appraisal uses weighted scoring. Criteria and weights: Meets user needs (40%), Cost (30%), Delivery risk (20%), Strategic alignment (10%). Scores out of 10:

| Criterion | Option 1 | Option 2 | Option 3 |
|---|---|---|---|
| Meets user needs | 8 | 6 | 9 |
| Cost | 5 | 9 | 4 |
| Delivery risk | 7 | 8 | 5 |
| Strategic alignment | 9 | 5 | 8 |

Which option wins, and what is its weighted score out of 10?

A. Option 1, with 7.0
B. Option 2, with 7.2
C. Option 3, with 7.6
D. Option 2, with 6.9

**Correct answer: B.**

**Explanation:** Weighted score = Σ(score × weight). Option 1: (8 × 0.4) + (5 × 0.3) + (7 × 0.2) + (9 × 0.1) = 3.2 + 1.5 + 1.4 + 0.9 = 7.0. Option 2: (6 × 0.4) + (9 × 0.3) + (8 × 0.2) + (5 × 0.1) = 2.4 + 2.7 + 1.6 + 0.5 = 7.2. Option 3: (9 × 0.4) + (4 × 0.3) + (5 × 0.2) + (8 × 0.1) = 3.6 + 1.2 + 1.0 + 0.8 = 6.6. Option 2 scores highest at 7.2 - answer choice B. A quick glance can mislead here: Option 3 has the single highest score (9 on user needs) and Option 1 looks well balanced, but the weighted sum is the only figure that counts, and you must compute all three before choosing. Notice too what the weighted model has done: Option 2 is weakest on the highest-weighted criterion (user needs) yet still wins on the strength of cost and risk. When a scoring model produces a winner that under-serves user needs, a good architect does not silently accept the arithmetic - you present the result transparently and invite the board to examine whether the weights truly reflect organisational priorities. The numbers inform the decision; they are not the decision.

#### Question 11 (hard) - Data growth and storage forecasting

Your solution's document store currently holds 2.4 terabytes. Data volume grows at 15% per year, compounding. The current storage tier is cost-effective up to 4 terabytes, after which the design requires re-architecting to a tiered storage model. In which year of operation does the store first exceed 4 terabytes?

A. Year 3
B. Year 4
C. Year 5
D. Year 6

**Correct answer: B.**

**Explanation:** Compound growth: multiply by 1.15 each year. Year 1: 2.4 × 1.15 = 2.76 TB. Year 2: 2.76 × 1.15 = 3.174 TB. Year 3: 3.174 × 1.15 = 3.650 TB. Year 4: 3.650 × 1.15 = 4.198 TB - first breach of the 4 TB threshold. The common error is using simple (non-compounding) growth: 2.4 + (0.36 × n) reaches 4.0 when n ≈ 4.4, which happens to point at year 5 (option C) and understates real growth. Compounding matters: percentage growth applies to an ever-larger base. For your role, this calculation is the difference between scheduling the tiered-storage work calmly into a year-3 roadmap and discovering the cliff in year 4 - exactly the kind of foresight your "track emerging issues over time" skill behaviour describes.

#### Question 12 (hard) - Cost per transaction across a peak

A senior stakeholder challenges your design: "The managed platform costs £9,400 a month but the framework provider costs £9,600 - the saving is trivial. Convince me with better numbers." You gather transaction data: the service handles 400,000 transactions in a normal month, but during the annual renewal peak (2 months of the year) it handles 1,100,000 transactions per month. The managed platform's £9,400 is flat-rate; the framework provider's £9,600 covers up to 500,000 transactions, then charges £8 per additional 1,000 transactions.

What is the framework provider's cost in a peak month, and the resulting annual saving from choosing the managed platform?

A. £14,400 peak month; £12,000 annual saving
B. £14,400 peak month; £11,600 annual saving
C. £13,200 peak month; £9,600 annual saving
D. £9,600 peak month; £2,400 annual saving

**Correct answer: A.**

**Explanation:** Peak month excess = 1,100,000 − 500,000 = 600,000 transactions = 600 blocks of 1,000. Excess charge = 600 × £8 = £4,800. Peak month cost = 9,600 + 4,800 = £14,400. Annual comparison: framework provider = 10 normal months × £9,600 + 2 peak months × £14,400 = 96,000 + 28,800 = £124,800. Managed platform = 12 × £9,400 = £112,800 (12 × 9,000 = 108,000, plus 12 × 400 = 4,800). Annual saving = 124,800 − 112,800 = £12,000: option A. Options A and B differ only in the saving figure, which is exactly where the test-writer expects a slip: option B's £11,600 arises from accidentally counting 11 normal months alongside the 2 peak months, quietly modelling a 13-month year. When two options share the headline figure and differ in the second, recompute the second figure before committing. The deeper lesson is the one the stakeholder needed: flat-rate versus usage-based pricing cannot be compared on a single normal month - you must model the whole year including peaks. This is the commercial perspective skill in action: the sourcing recommendation reversed once the renewal peak was priced in, turning a "trivial £200" difference into £12,000 a year.

#### Question 13 (hard) - Estimation under uncertainty

You need a quick order-of-magnitude estimate in a meeting. The service will serve about 60% of the UK's 5.6 million small businesses, each interacting on average 4 times per year, and each interaction generates about 12 API calls. Roughly how many API calls per year should the design accommodate?

A. About 16 million
B. About 160 million
C. About 1.6 billion
D. About 1.6 million

**Correct answer: B.**

**Explanation:** Estimate in stages, rounding aggressively: users = 5.6M × 0.6 ≈ 3.4M. Interactions = 3.4M × 4 ≈ 13.4M per year. API calls = 13.4M × 12 ≈ 161M - about 160 million (option B). The options differ by factors of 10, so precision is irrelevant; what matters is keeping track of millions through three multiplications. Practise the habit of writing magnitudes ("3.4M × 4 = 13.6M, × 12 ≈ 160M") rather than long digit strings - dropped zeros are the dominant failure mode. Architects are asked for exactly this kind of estimate constantly, and a confident, transparent rough answer ("about 160 million a year, call it 5 per second sustained, more at peak") earns far more trust than false precision.

#### Question 14 (moderate) - Phased roadmap spend

Your solution's implementation roadmap phases the £480,000 annual budget across four quarters as 20%, 35%, 30%, 15%, reflecting a build peak in the middle of the year. At the end of Q2, actual spend to date is £287,000. How does actual spend compare with the planned spend to date?

A. £23,000 over plan
B. £23,000 under plan
C. £7,000 over plan
D. Exactly on plan

**Correct answer: A.**

**Explanation:** Planned spend to the end of Q2 = (20% + 35%) × £480,000 = 55% × 480,000 = £264,000. Actual = £287,000. Difference = 287,000 − 264,000 = £23,000 over plan (option A). The most common error is comparing against half the annual budget (£240,000, since two of four quarters have passed), which assumes even phasing and would suggest £47,000 over - not among the options, which is your cue to re-read the phasing percentages. Phased budgets are the numeric backbone of "support the implementation of a strategy or vision, for example, by using a roadmap or plan" (your strategy design skill): a variance is only meaningful against the *planned profile*, not against a flat average. When you report this to a programme board, the transparent framing is "£23,000 (about 8.7%) above the phased plan at the halfway point" - the percentage (23,000 ÷ 264,000 ≈ 8.7%) gives senior stakeholders the scale that the raw figure alone does not.

### Preparation tips

- **Rebuild your own spreadsheets by hand.** Take a real options analysis or hosting estimate from your work, cover the totals, and recompute them. Familiar data makes the mechanics stick.
- **Master the four workhorses.** Percentage of a whole, percentage change, ratios, and weighted averages cover most of what these tests ask. Drill them until each takes seconds.
- **Bracket before you calculate.** A ten-second estimate ("must be between 10% and 20%") catches most calculator slips and lets you eliminate options instantly.
- **Write units next to every number.** Per second, per minute, per month, per 1,000 transactions, in thousands. Most hard questions hide a unit conversion; most wrong answers are correct arithmetic on mismatched units.
- **Know your rounding direction.** Capacity rounds up; budgets round up for safety; percentages report as given. Decide the rule before the exam, not during it.
- **Use the on-screen calculator for arithmetic, not for thinking.** Set up the whole calculation on paper or in your head first, then key it in once. Repeated fragmentary keying is where transcription errors breed.

### Common pitfalls

- **Misreading chart and table labels.** Monthly versus annual data, "in thousands" qualifiers, and which row belongs to which option. The exhibit rewards thirty seconds of careful orientation before any calculation.
- **Dividing by the wrong base in percentage change.** Improvement is measured against the starting value. Dividing by the new value flatters the result - and test-writers always include that flattering figure among the options.
- **Over-calculating.** If the options are far apart, estimate; exact arithmetic on a question that only needs magnitude wastes minutes you will want later.
- **Time-sink questions.** A multi-stage cost model can consume five minutes. Bank the quick wins first, then return; an unanswered easy question is the most expensive kind of mistake.
- **Label-mapping slips.** When answer choices and scenario items share letters or names, transferring the right result to the wrong label is a silent killer. Point at the option and say it to yourself before you click.
- **Forgetting the peak.** Averages hide peaks, and usage-based pricing punishes anyone who models only the average month. Whenever a question mentions seasonal or peak behaviour, it is almost certainly the crux.


## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment evaluates how well you understand, analyse, and draw correct conclusions from written material of the kind your role deals in every day. The passages use the genuine vocabulary of your work - technology standards, governance policies, assurance reports, supplier notices, stakeholder emails - and the questions test whether your conclusions rest strictly on what the text says, not on what you expect it to say.

The dominant format is the True / False / Cannot Say question. You read a passage, then judge a statement: **True** means the passage logically supports it; **False** means the passage contradicts it; **Cannot Say** means the passage provides insufficient information either way. That third option is what makes these tests demanding - and what makes them so relevant to your work. Alongside these, expect multiple-choice comprehension questions asking for the best summary, the author's main point, or the correct application of a stated rule.

Typical format and timing: online, strictly timed, often less than a minute per question once the passage is read. Passages are typically 100 to 250 words, each followed by 3 to 5 questions. The discipline being measured is fact-based logic: answering from the text provided, ignoring outside knowledge, and resisting the temptation to fill gaps with plausible assumptions.

Why this matters for your role: as a solution architect you must comply with standards and governance - which first means reading standards exactly. You lead the communication of complicated, complex, or risky architecture topics with technical and non-technical stakeholders, which means your written summaries must say precisely what the evidence supports, no more. You challenge requirements and assumptions, which begins with noticing that a requirement does not actually say what everyone assumes it says. And you manage risks and decisions in a transparent way, which frequently comes down to the honest sentence: "the document does not tell us." Verbal reasoning is the psychometric mirror of all four duties.

### What it measures for your role

- **Architecture communication**: adapting your message to your audience starts with extracting the true content of source material. Tested through best-summary and main-point questions on dense technical passages.
- **Making architectural decisions**: engaging with governance and assurance means parsing policy wording precisely - "must" versus "should", "may" versus "will". Tested through rule-application questions.
- **Problem definition and shaping**: framing a problem requires separating what stakeholders have actually said from what has been inferred. Tested through True / False / Cannot Say discipline.
- **Strategy design**: challenging requirements and assumptions is, at root, close reading. Tested through statements that sound like the passage but subtly exceed it.
- **Architect for the whole context**: tracking emerging issues means reading supplier notices and roadmaps accurately, including their careful hedges. Tested through passages containing conditional and qualified language.

### Practice questions

Read each passage carefully, then answer strictly from the text. For True / False / Cannot Say items, remember: True = the passage supports it; False = the passage contradicts it; Cannot Say = not enough information in the passage.

**Passage 1 - Technology code of practice extract**

> "All new digital services must be assessed against the Technology Code of Practice before their beta phase. Services handling personal data must additionally complete a data protection impact assessment. Where a service intends to use technology that is not on the approved list, the design must be referred to the technical design authority, which meets fortnightly. The authority may grant an exemption for up to twelve months. Exemptions are not renewable; before an exemption expires, the service must either migrate to approved technology or demonstrate that the technology now meets the approval criteria."

#### Question 1 (easy) - True / False / Cannot Say

Statement: "A new digital service that handles personal data must complete a data protection impact assessment."

A. True
B. False
C. Cannot Say

**Correct answer: A. True.**

**Explanation:** The second sentence states this directly: "Services handling personal data must additionally complete a data protection impact assessment." The word "additionally" links it to the assessment regime for new digital services in sentence one. No inference beyond the text is required. Easy items like this exist to check you are anchoring answers in exact wording - build that habit here, because the harder items depend on it.

#### Question 2 (moderate) - True / False / Cannot Say

Statement: "The technical design authority must grant an exemption when a design is referred to it."

A. True
B. False
C. Cannot Say

**Correct answer: B. False.**

**Explanation:** The passage says the authority "may grant an exemption" - permissive, not obligatory. A statement converting "may" into "must" contradicts the text's plain meaning: the authority is described as having discretion, so a claim that it is required to grant exemptions is false rather than merely unsupported. This modal-verb precision ("must" versus "may" versus "should") is exactly what you check when confirming whether your design complies with a standard or merely aligns with its suggestions - and it is the single most tested distinction in policy-based verbal reasoning.

#### Question 3 (moderate) - True / False / Cannot Say

Statement: "A service can hold the same exemption for eighteen months if the authority agrees."

A. True
B. False
C. Cannot Say

**Correct answer: B. False.**

**Explanation:** Two parts of the passage combine to contradict this: exemptions run "for up to twelve months" and "are not renewable". The same exemption therefore cannot lawfully stretch to eighteen months under this policy, regardless of the authority's agreement, because the policy grants the authority no such power. Note the trap in "if the authority agrees" - it invites you to imagine discretion that the text explicitly bounds. When a statement smuggles in a permission the text does not grant, it is false, not Cannot Say.

#### Question 4 (moderate) - True / False / Cannot Say

Statement: "The technical design authority meets more often than once a month."

A. True
B. False
C. Cannot Say

**Correct answer: A. True.**

**Explanation:** The passage says the authority "meets fortnightly" - every two weeks, which is more often than once a month (roughly 26 times a year versus 12). This item tests whether you convert stated frequency into compared frequency accurately. It is a small calculation embedded in a verbal item, a common hybrid: read the fact, then reason one careful step. The step is licensed by the text, so this is True rather than Cannot Say - inference is allowed when it follows necessarily from what is written.

#### Question 5 (hard) - True / False / Cannot Say

Statement: "Most services that request exemptions eventually migrate to approved technology."

A. True
B. False
C. Cannot Say

**Correct answer: C. Cannot Say.**

**Explanation:** The passage describes what services *must* do before an exemption expires (migrate, or demonstrate the technology now meets approval criteria), but it says nothing about what proportion actually take each route, nor whether they comply at all. "Most" is a statistical claim, and the passage contains no statistics. This is the archetypal Cannot Say: the statement is plausible, consistent with the passage, and quite possibly true in the real world - but the text neither supports nor contradicts it. Answering "the evidence before us does not establish that" is the same professional muscle you use when an assurance report is silent on a point a stakeholder wants confirmed.

**Passage 2 - Email from a programme director**

> "Team - following yesterday's board, three decisions. First, the licensing solution's public beta moves from October to December; the board was clear this is a pause for the identity integration to mature, not a descoping. Second, budget for the current financial year is unchanged, though the board signalled that next year's settlement is likely to be tighter and asked all programmes to prepare options for a 10% reduction. Third, the board endorsed the architecture team's recommendation to reuse the department's existing payments platform rather than procure a new one, subject to the platform team confirming capacity by end of month. If capacity is not confirmed, the procurement route reopens. Please treat the beta date as confidential until the minister's office has been briefed."

#### Question 6 (easy) - Multiple choice comprehension

Which statement best summarises the payments decision?

A. The department will procure a new payments platform
B. Reuse of the existing payments platform is endorsed, conditional on a capacity confirmation due by end of month
C. The payments platform team has confirmed it has capacity
D. The board rejected the architecture team's recommendation

**Correct answer: B.**

**Explanation:** The email endorses reuse "subject to the platform team confirming capacity by end of month", with procurement reopening if confirmation fails. Option B captures both the endorsement and the condition. Option A describes the fallback as if it were the decision; option C converts a pending condition into a completed fact - the confirmation is due, not done; option D inverts the outcome. Summaries that preserve conditions intact are the heart of architecture communication: dropping the "subject to" clause when you relay this to your team would misinform them precisely where the risk lives.

#### Question 7 (moderate) - True / False / Cannot Say

Statement: "The programme's budget for the current financial year has been reduced by 10%."

A. True
B. False
C. Cannot Say

**Correct answer: B. False.**

**Explanation:** The email states the current year's budget "is unchanged". The 10% figure belongs to a different claim: programmes are asked to *prepare options* for a possible reduction in *next year's* settlement. The statement fuses two separate facts - current-year actuals and next-year contingency planning - into one false claim. Test-writers build these fusion traps deliberately, and so does real life: this is precisely how corridor summaries of board decisions become wrong. When you relay financial constraints to your team, keep timeframes and certainty levels attached to their numbers.

#### Question 8 (moderate) - True / False / Cannot Say

Statement: "The public beta has been delayed because features were removed from scope."

A. True
B. False
C. Cannot Say

**Correct answer: B. False.**

**Explanation:** The email pre-empts exactly this misreading: the move to December is "a pause for the identity integration to mature, not a descoping". The stated reason is integration maturity; the statement's reason (features removed) is explicitly denied. Notice that the delay itself is true - it is the attributed cause that makes the whole statement false. In True / False / Cannot Say items, a statement is judged as a whole: one contradicted element makes it False even if the rest is accurate.

#### Question 9 (hard) - True / False / Cannot Say

Statement: "The minister's office has not yet been briefed on the new beta date."

A. True
B. False
C. Cannot Say

**Correct answer: A. True.**

**Explanation:** The instruction "treat the beta date as confidential until the minister's office has been briefed" presupposes that the briefing has not yet happened at the time of writing - if it had, the instruction would be pointless and the "until" clause already satisfied. This is a presupposition question, the hardest kind: the fact is not asserted directly but is logically required for the sentence to make sense as an instruction. Strong candidates distinguish presuppositions the text commits to (answer: True) from mere plausible background (answer: Cannot Say). If you found yourself hesitating between True and Cannot Say here, that hesitation is healthy - resolve it by asking: could the passage be coherent if the statement were false? Here, it could not.

**Passage 3 - Supplier end-of-support notice**

> "From 31 March, version 4 of the integration platform will move to extended support. Extended support includes security patches but excludes functional fixes and new connector releases. Customers on extended support may continue to raise incidents, which will be triaged within existing service levels; however, incidents attributable to defects that would require a functional fix will be closed with the recommendation to upgrade. Version 5 offers full support and is available now. Migration from version 4 typically takes between six and sixteen weeks depending on the number of custom connectors deployed. Customers with more than ten custom connectors are strongly advised to begin migration planning immediately."

#### Question 10 (moderate) - True / False / Cannot Say

Statement: "After 31 March, version 4 customers will no longer receive security patches."

A. True
B. False
C. Cannot Say

**Correct answer: B. False.**

**Explanation:** The notice says extended support "includes security patches" - what it excludes is functional fixes and new connector releases. The statement contradicts the explicit inclusion, so it is False. This inclusion/exclusion structure is standard in supplier lifecycle notices, and misreading it in either direction is costly: assume too little support and you trigger an unnecessary emergency migration; assume too much and you carry an unpatched risk. Read lists of what is included and excluded with the same care you would read a contract - functionally, they are one.

#### Question 11 (hard) - True / False / Cannot Say

Statement: "An organisation with four custom connectors will complete its migration in less than ten weeks."

A. True
B. False
C. Cannot Say

**Correct answer: C. Cannot Say.**

**Explanation:** The notice gives a typical range (six to sixteen weeks) that "depends on the number of custom connectors deployed", and it singles out customers with more than ten connectors for urgent planning. It is tempting to reason: four connectors is few, so the migration will sit at the short end - under ten weeks. But the passage never states the relationship precisely enough: "typically" admits exceptions, the range is not mapped to connector counts, and other factors are not excluded. The statement is a plausible prediction, not a supported conclusion - Cannot Say. This is the assumption-trap at its most seductive, because the inference feels professional and reasonable. In your work the same discipline applies to supplier claims: "typically six to sixteen weeks" is planning input, not a commitment, and your migration plan should say so.

#### Question 12 (hard) - Multiple choice: applying a stated rule

Your service runs version 4 with twelve custom connectors. In April, the service raises an incident: a connector fails because of a defect whose remedy would require a functional fix. According to the notice, what will happen?

A. The incident will be rejected without triage
B. The incident will be triaged within existing service levels, then closed with a recommendation to upgrade
C. The supplier will issue a functional fix because twelve connectors qualifies for priority treatment
D. The supplier will extend full support because the defect is connector-related

**Correct answer: B.**

**Explanation:** Two rules chain together. First: customers on extended support "may continue to raise incidents, which will be triaged within existing service levels" - so triage happens, ruling out A. Second: "incidents attributable to defects that would require a functional fix will be closed with the recommendation to upgrade" - so after triage, closure with upgrade advice. Option B follows the chain exactly. Option C invents a priority rule the notice does not contain (the ten-connector threshold triggers *migration planning advice*, not fix entitlement); option D invents an exception with no textual basis. Applying stated rules to a specific case - without adding rules that seem fair - is exactly what you do when you assess your solution's position against a standard, and it is where wishful reading does the most damage.

#### Question 13 (moderate) - Multiple choice: best summary for a stakeholder

You must summarise Passage 3 in one sentence for a non-technical service owner. Which is best?

A. "The supplier is ending support, so we must migrate immediately or the service will fail."
B. "From 31 March our platform version gets security patches only; defects needing functional fixes won't be fixed, and with our twelve custom connectors we're advised to start migration planning now."
C. "The supplier has released version 5, which offers several interesting new capabilities."
D. "There is a support change coming but it mainly affects other customers."

**Correct answer: B.**

**Explanation:** Option B is accurate (security patches continue; functional fixes stop; the ten-plus connector advice applies to us), complete on the decision-relevant points, and calm. Option A overstates ("ending support" is false - extended support continues; "service will fail" is unsupported alarm). Option C is true but omits everything the service owner needs to act on. Option D understates: with twelve connectors, this organisation is squarely in the strongly-advised group. Notice the craft here: the best stakeholder summary is not the shortest or the most reassuring - it is the one that preserves the facts a decision depends on, tuned to the audience. That is the "adapt your message and communication techniques to your audience" behaviour from your architecture communication skill, in a single sentence.

#### Question 14 (hard) - True / False / Cannot Say

Statement: "Version 5 of the integration platform includes new connector releases."

A. True
B. False
C. Cannot Say

**Correct answer: C. Cannot Say.**

**Explanation:** The notice says version 5 "offers full support", and that extended support (for version 4) "excludes... new connector releases". It is natural to infer that full support includes new connector releases - but the notice never defines full support's contents. Perhaps it does include them; perhaps "full support" means only that functional fixes resume. The text is silent, so Cannot Say. Contrast with Question 10, where the text explicitly included security patches: the difference between "explicitly stated" and "reasonably assumed" is the entire game in these assessments, and in standards compliance too. When your design's assurance case depends on a vendor capability, cite the sentence that states it - if you cannot find the sentence, you have found an assumption to verify.

**Passage 4 - Extract from a design assurance report**

> "The review panel assessed the proposed solution design against the department's architecture principles. The design was found to align with the principles on reuse, openness, and accessibility. On resilience, the panel noted that the design's recovery time objective of four hours is consistent with the service's business impact assessment, but observed that the recovery plan has not yet been tested. The panel therefore grants approval to proceed to build, with one condition: a successful recovery test must be evidenced before the service enters public beta. The panel further recommends, though does not require, that the team document its caching strategy as a formal architecture decision record."

#### Question 15 (moderate) - True / False / Cannot Say

Statement: "The design failed to meet the department's accessibility principle."

A. True
B. False
C. Cannot Say

**Correct answer: B. False.**

**Explanation:** The report states the design "was found to align with the principles on reuse, openness, and accessibility". Alignment with the accessibility principle is directly asserted, so a claim of failure contradicts the text. Be careful not to let the report's overall conditional tone ("approval... with one condition") bleed into individual findings: the condition attaches to resilience testing, not accessibility. Attributing the right caveat to the right finding is exactly the precision governance boards expect when you report assurance outcomes onwards to your team and stakeholders.

#### Question 16 (hard) - True / False / Cannot Say

Statement: "The service cannot enter public beta unless a successful recovery test has been evidenced."

A. True
B. False
C. Cannot Say

**Correct answer: A. True.**

**Explanation:** The panel grants approval "with one condition: a successful recovery test must be evidenced before the service enters public beta". The statement is the contrapositive restatement of that condition - no evidenced test, no public beta - and restating a rule in equivalent logical form is licensed inference, not assumption. Compare the final sentence: documenting the caching strategy is "recommended, though not required", so an equivalent statement about the caching ADR blocking beta would be False. Conditions bind; recommendations advise. Reading which is which - and holding the line when a team hopes a condition was "really just a recommendation" - is central to complying with standards and governance.

#### Question 17 (moderate) - Multiple choice comprehension

Which of the following best describes the panel's overall decision?

A. Approval refused until the recovery plan is tested
B. Unconditional approval to proceed to build
C. Conditional approval: build may proceed, but public beta requires evidence of a successful recovery test
D. Approval deferred pending documentation of the caching strategy

**Correct answer: C.**

**Explanation:** The panel "grants approval to proceed to build" - so build is unblocked now, ruling out A and D - but attaches a condition gating *public beta* on recovery-test evidence, ruling out B. Option C is the only reading that keeps both the permission and the condition attached to their correct phases. Options A and C differ in exactly one respect: what the condition blocks (build versus beta). Mapping each governance condition to the specific life-cycle gate it constrains is how you turn an assurance letter into an actionable delivery plan - and how you avoid either over-blocking your team or sleepwalking past a genuine gate.

### Preparation tips

- **Practise on your organisation's real documents.** Take a technology standard, a board minute, or a supplier notice and write three statements about it: one True, one False, one Cannot Say. Constructing the items teaches you the traps faster than answering them.
- **Train the modal verbs.** "Must", "should", "may", "will", "typically" - each carries a precise level of obligation or certainty. When you read, mentally tag them; when you answer, check the statement's modal matches the passage's.
- **Ask the coherence question for presuppositions.** For hard True/Cannot Say boundaries, ask: could the passage make sense if this statement were false? If not, the passage commits to it - answer True.
- **Quarantine your expertise.** You know how supplier lifecycles and government assurance actually work; the passage may describe a world that differs. Answer from the text alone - examiners deliberately write passages that deviate from industry norms to catch experts relying on experience.
- **Read the statement more carefully than the passage.** Most wrong answers come from skimming the statement and missing a fused clause, a swapped timeframe, or a strengthened quantifier ("some" becoming "most").
- **Pace by passage, not by question.** Invest your reading time once per passage, keep the passage's structure in your head (what each sentence does), then answer its questions quickly by targeted re-reading.

### Common pitfalls

- **Making assumptions.** Bringing in outside knowledge or filling gaps with plausible inference is the number-one cause of lost marks - the plausible inference is precisely what "Cannot Say" is designed to catch.
- **Confusing "likely" with "fact".** A passage saying an outcome is expected, typical, or likely does not support a statement that it will happen. Certainty levels must match.
- **Judging half a statement.** A statement that is half true and half contradicted is False. A statement that is half true and half unaddressed is Cannot Say. Judge the whole claim.
- **Symmetric errors on Cannot Say.** Some candidates overuse Cannot Say (safe-feeling but wrong when the text does support or contradict); others underuse it (uncomfortable with uncertainty). Know your own bias and correct for it.
- **Poor time management.** Reading every passage exhaustively before looking at any question wastes time; skimming so fast you must re-read everything wastes more. Read once with structure in mind, then answer with targeted re-reads.
- **Forgetting the wording anchor.** Every explanation in this section pointed back to exact words - "may grant", "unchanged", "includes security patches". If you cannot point to the words, you have not earned the answer.


## Workplace job-specific situational judgement assessment

### About this assessment

A workplace job-specific situational judgement assessment evaluates your decision-making, interpersonal skill, and professional conduct through realistic workplace dilemmas. Unlike the cognitive, numeric, and verbal assessments, there is often no single objectively right answer: several responses may seem reasonable, and the test measures how well your instincts align with the values and behaviours the role and organisation require.

Each item presents a short scenario - a conflict, an ethical dilemma, an operational challenge - followed by a set of possible actions. The usual response formats are: choose the **most effective** and **least effective** actions; or **rank** all options from best to worst; or **rate** each option's effectiveness independently. Timing is typically generous or untimed, because the assessment measures natural judgement rather than speed.

For you as a solution architect, the scenarios will feature the stakeholders of your real working life: delivery teams who need decisions faster than governance moves; senior stakeholders with strong views and short attention; governance boards and assurance panels; suppliers with commercial agendas; fellow architects whose designs your work must align with; and the quiet, ever-present stakeholder of the UK public sector - the citizen whose needs, data, and money are at stake. The values that anchor "effective" in this context are the values of government digital work: user needs first, transparency in decisions and risks, collaboration across teams, accessibility and inclusion by default, and careful stewardship of public money.

Your role level shapes the calibration too. As a solution architect you are responsible for a single solution, usually working independently where risk is low, and supporting senior architects on riskier work. Effective responses therefore tend to combine three moves: act within your remit, make risks and decisions transparent rather than private, and escalate or consult at the right moment without offloading your own responsibility. Options that hide problems, bypass governance, delay without purpose, or hand your accountability to someone else usually score poorly.

### What it measures for your role

- **Architecture communication**: managing stakeholder expectations, adapting your message to your audience, advocating for a team, and communicating risky topics honestly - the heart of most scenarios below.
- **Community collaboration**: contributing to others' work, motivating and empowering teams, creating the right environment, and recognising and dealing with issues rather than letting them fester.
- **Making architectural decisions**: engaging governance and assurance properly, managing risk transparently, and knowing when a decision is yours and when it needs support.
- **Commercial perspective**: handling suppliers and sourcing questions with propriety, knowing the appropriate internal contacts, and protecting fair competition.
- **Problem definition and shaping**: resisting pressure to jump to solutions before the problem and outcomes are defined.
- **Strategy design and architect for the whole context**: balancing your solution's needs against organisational strategy and other teams' work.

### Practice questions

For each scenario, decide your answer before reading the commentary. Where the format asks for most and least effective, commit to both.

#### Question 1 (easy) - The team wants to skip governance

Your delivery team is under schedule pressure. The tech lead proposes: "The design assurance review will add two weeks. Our change is low-risk - let's just skip the review and note it in the backlog." You are the solution architect responsible for this design. Choose the MOST and LEAST effective responses.

A. Agree - the change is genuinely low-risk, and delivery speed matters most.
B. Check the assurance criteria: if the change qualifies for a lightweight or exempt route, use it; if not, book the earliest slot, tell the programme manager about the two-week impact, and look for work the team can progress in parallel.
C. Refuse and insist on the full review without further discussion, reminding the tech lead that process is process.
D. Say nothing and let the tech lead decide, since delivery timelines are their responsibility.

**Most effective: B. Least effective: A.**

**Explanation:** B does four things well: it takes the tech lead's underlying concern (schedule) seriously; it uses the governance system as designed - most assurance frameworks have proportionate routes for low-risk changes; it makes the schedule impact transparent to the person who owns the plan; and it mitigates the delay practically. This is "engage with architectural governance and assurance to effectively manage decisions and risks" combined with honest stakeholder communication. A is least effective because it privately waives a control that exists to catch exactly the risks a busy team underestimates - and "note it in the backlog" hides the decision rather than making it transparently. C reaches a defensible outcome badly: it dismisses a legitimate concern, damages the relationship, and misses the chance that a lightweight route genuinely exists. D abdicates: assurance of the design is your accountability, not the tech lead's. Between C and D, C at least protects the control; D fails both the control and the role.

#### Question 2 (easy) - A stakeholder asks for certainty you do not have

A senior business stakeholder emails: "I'm presenting to the director tomorrow. Confirm that the new system will handle the March peak with no issues." Load testing is scheduled but has not yet run. Choose the MOST and LEAST effective responses.

A. Reply confirming the system will handle the peak - the design targets were set with March in mind, so it should be fine.
B. Reply that you cannot comment until testing completes, and suggest they remove the topic from the presentation.
C. Reply with what is true: the design is sized for the March peak with 30% headroom, load testing runs next week and will verify it, and offer a form of words they can use with the director that is both confident and accurate.
D. Forward the email to the testing team and ask them to respond.

**Most effective: C. Least effective: A.**

**Explanation:** C manages stakeholder expectations honestly while actually helping - the offered form of words ("designed for the peak with headroom; verification completes next week") lets the stakeholder present confidently without overclaiming, which is precisely the "adapt your message and communication techniques to your audience" behaviour, applied under pressure. A is least effective because it converts a design intention into a verified fact; if testing finds a problem, the director has been misinformed and your credibility - the asset a solution architect trades on - is spent. B is honest but unhelpfully rigid: it treats communication as binary (silence or certainty) when your role is to communicate managed risk. D passes a relationship you own to a team that does not own it, and delays an answer the stakeholder needs today.

#### Question 3 (moderate) - Conflicting direction from two architects

A senior solution architect, whose programme your solution feeds into, tells you to use the department's event streaming platform for an integration. Your own analysis suggests a simple API call is sufficient and cheaper for the current volume, and the delivery team agrees with you. Choose the MOST and LEAST effective responses.

A. Implement the API approach - your analysis is sound and the solution is your responsibility.
B. Implement the event streaming approach without question - seniority settles it.
C. Take your analysis to the senior architect: present the volume data and cost comparison, ask what future context or programme-level pattern drives their direction, and agree the decision and its rationale together, recording it as an ADR either way.
D. Ask the delivery team to raise their concerns through their own management chain to avoid an architect-versus-architect dispute.

**Most effective: C. Least effective: D.**

**Explanation:** C embodies several behaviours from your role profile at once: "work with others to make architectural design decisions", "align your work with the work being done by other architects", and transparent recording of decisions. Crucially, it treats the disagreement as information: the senior architect may know something you do not (a programme-wide move to event-driven integration, a downstream consumer you cannot see), and your data may be something they lack. Either way the ADR captures the reasoning for whoever maintains this solution later. A is unilateral: locally optimal, possibly globally wrong, and it spends the relationship your solution depends on. B is obedience without understanding - if the direction is right, you should know why; if it is wrong, you have silently baked in cost. D is least effective because it manufactures an organisational conflict out of a technical conversation you are equipped to have directly - escalation through management chains turns colleagues into opponents and delays the decision. Disagreement between architects is normal; routing it through third parties is not collaboration, it is avoidance.

#### Question 4 (moderate) - The supplier demo

A supplier whose product is one of three candidates in your options analysis invites you to an exclusive demonstration event, including lunch and a gift bag, while the evaluation is live. Choose the MOST and LEAST effective responses.

A. Attend quietly - product knowledge improves your evaluation, and one lunch will not sway you.
B. Decline the exclusive event; ask your commercial team's advice on propriety, and request instead that the supplier provide the same demonstration available to all candidates through the formal evaluation process, declaring the invitation as your organisation's rules require.
C. Attend, but pay for your own lunch and refuse the gift bag.
D. Decline and also privately downgrade the supplier's scores for attempting to influence the evaluation.

**Most effective: B. Least effective: D.**

**Explanation:** B applies the commercial perspective skill exactly as written: "understand commercial processes and the appropriate internal contacts within a government department". During a live evaluation, even the appearance of preferential access can compromise a procurement's fairness and expose the organisation to challenge; the commercial team exists to advise on precisely this line, and channelling the demonstration through the formal process keeps information symmetrical across candidates. A underestimates how procurement fairness is judged - by appearance and access, not just by your inner certainty of impartiality. C shows instinct but still accepts asymmetric access, which is the substantive problem. D is least effective, and it is worth seeing why it beats out A for that spot: A is a propriety misjudgement, but D actively corrupts the evaluation in the opposite direction - scores must reflect the published criteria, and punishing a supplier off-the-books is exactly as improper as favouring one, while also being hidden. Two wrongs in one option: bias and opacity.

#### Question 5 (moderate) - A risk you spotted in someone else's solution

While reviewing integration points, you notice that a neighbouring team's service - not your responsibility - appears to store citizen data unencrypted in a cache. Your own solution merely reads from their API. Choose the MOST and LEAST effective responses.

A. Do nothing - it is not your solution, and teams resent outsiders auditing them.
B. Raise it directly and promptly with that team's architect or tech lead, factually and privately, offering your evidence and letting them verify and handle it; if it is confirmed and not addressed within a reasonable time, ensure it reaches the security team or appropriate governance route.
C. Report it immediately to the department's security incident process without speaking to the team.
D. Email a broad distribution list asking whether anyone else has noticed problems with that team's service.

**Most effective: B. Least effective: D.**

**Explanation:** B balances collegiality with duty. "Recognise and deal with issues" (community collaboration) and "identify and address architectural risks, for example, business, data, or security" (making architectural decisions) do not stop at your solution's boundary - and citizen data is everyone's duty of care. Going first to the owning team respects their ownership, allows for the real possibility that you have misread the design, and preserves the relationship; the escalation backstop ensures collegiality never becomes complicity. A fails the duty outright. C is the interesting distractor: for a confirmed active breach, the incident process would be right - but here you have an unverified observation about a design, and instant formal escalation over the team's heads, while defensible, costs trust that a five-minute conversation could preserve. If you chose C, you were wrong in a safe direction - worth half marks in life, if not in the test. D is least effective: it broadcasts an unverified security concern - potentially a real vulnerability - to a wide audience, simultaneously maximising reputational harm to the team and the risk that the vulnerability's existence spreads before it is fixed.

#### Question 6 (moderate) - The team is demoralised mid-delivery

Halfway through delivery, your solution's scope has changed twice due to legislation timing, and the delivery team is visibly demoralised. The delivery manager confides that two developers are talking about requesting moves to other teams. Choose the MOST and LEAST effective responses.

A. Focus on your own deliverables - team morale is the delivery manager's job, and role clarity matters.
B. Work with the delivery manager: explain the legislative drivers behind the scope changes directly to the team so the churn has meaning, involve the developers in reshaping the technical design to the new scope, and advocate upward for a stable scope window so the team can find its rhythm.
C. Give the team a motivational talk about the importance of public service and resilience in the face of change.
D. Suggest the delivery manager offer the two developers more interesting technical tasks to persuade them to stay.

**Most effective: B. Least effective: A.**

**Explanation:** B applies three community collaboration behaviours - "motivate and empower teams", "create the right environment for teams to work in", and advocacy on behalf of a team to other stakeholders (architecture communication). Its power is in the mechanism: people tolerate change they understand and help shape. Explaining the legislative "why" converts churn from arbitrary to meaningful; involving developers in the redesign converts them from victims of scope change to authors of the response; and advocating for a stable window attacks the root cause. A is least effective because it is false role clarity: the role profile explicitly makes team environment and motivation part of your job, and an architect who watches a team disintegrate while polishing diagrams has optimised the wrong thing. C is well-meant but hollow - motivation without agency or explanation rarely survives contact with the next scope change. D treats symptoms for two individuals while the cause keeps generating casualties.

#### Question 7 (hard) - Pressure to endorse a pre-chosen answer

A programme director has publicly favoured a particular platform and asks you to "get the options analysis done quickly - we all know where it's landing." Your genuine analysis suggests a different option is materially better on cost and accessibility. Rank ALL FOUR responses from most to least effective.

A. Produce the analysis honestly, present it to the director privately first - leading with the evidence on cost and accessibility, acknowledging the favoured platform's real strengths, and letting them adjust position without public embarrassment - then take it to the board.
B. Produce the analysis honestly and present it cold at the governance board, ensuring transparency through surprise.
C. Weight the analysis criteria so the favoured platform wins - the director has context you lack, and delivery relationships matter more than marginal differences.
D. Ask a senior architect colleague to review your draft analysis first, both to check your work and to gain a supportive voice, then proceed to present the honest findings to the director.

**Ranking: A, D, B, C (most to least effective).**

**Explanation:** The non-negotiable is the integrity of the analysis: options C fails it, everything else is sequencing. A ranks first because it combines honesty with stakeholder skill - "manage stakeholder expectations effectively" and "communicate with senior stakeholders" mean giving a senior person the evidence, the respect, and the room to change their mind; most people can walk back a position privately who cannot publicly. D ranks second and is nearly as good: peer review strengthens the work and "engage with architectural governance and assurance... with support" is exactly your level's behaviour - it loses to A only because it adds a step before the conversation that matters most, and could look like alliance-building. B is honest but tactically poor: ambushing a director at board converts a technical disagreement into a public loyalty contest, making it harder for them to accept the evidence. Still, B preserves the analysis's integrity, which is why it ranks clearly above C. C is the only option that corrupts the decision record itself: a weighted-to-order analysis misleads the board, wastes public money by design, and - once discovered, and these things are discovered - ends careers. No relationship is worth the rationale being false.

#### Question 8 (hard) - The design is failing in delivery

Three sprints into build, the delivery team reports that a core element of your technical design - the document processing pipeline - is proving far harder to implement than expected, and velocity has halved. The team has started quietly building a workaround that diverges from the design. Choose the MOST and LEAST effective responses.

A. Insist the team stop the workaround and implement the design as documented - divergence under pressure is how architectures rot.
B. Let the workaround continue - the team is closest to the code, and shipping matters.
C. Get into the detail with the team: understand precisely why the pipeline is harder than expected, assess the workaround on its merits, and either formally adapt the design to a version that works (updating the documentation and informing governance if the risk profile changes) or pair with the team to remove the specific blocker - deciding transparently rather than letting the divergence stay quiet.
D. Escalate to the senior architect that the team is not following the design.

**Most effective: C. Least effective: D.**

**Explanation:** C is almost a direct quotation of your role profile: "adapt a technical design if needed during delivery" and "provide guidance and support to teams using technical designs throughout the life cycle". The key insight is that the problem is not the workaround - it is the *quietness*. A design that survives contact with reality only by silent divergence is already dead as documentation; the fix is to bring the divergence into the open, evaluate it, and make the design true again, whichever way the decision goes. A defends the artefact instead of the outcome - sometimes the design is simply wrong, and three sprints of evidence is data, not disloyalty. B abandons the design's integrity in the other direction: undocumented divergence means the next team inherits a system that matches no known description, and any governance approvals now describe a fiction. D is least effective because it converts a solvable engineering problem into a trust rupture: escalating *about* the team before working *with* them tells every future team that honesty with you is dangerous - after which you will never again hear about a divergence while it is still small. Note the escalation contrast with Question 5: there, escalation was the backstop after direct engagement; here it is a first resort against your own team - same act, opposite judgement.

#### Question 9 (hard) - Accessibility versus deadline

Two weeks before public beta, accessibility testing finds that the document upload journey fails WCAG criteria for screen reader users. Fixing it properly needs four weeks. The service owner proposes launching on time and fixing accessibility "in the first post-launch sprint", noting that upload is used by only 8% of users. Rank ALL FOUR responses from most to least effective.

A. Support the launch with the accessibility defect - 8% usage makes it an edge case, and momentum matters.
B. Advise delaying the affected journey: launch the beta on time with the upload feature disabled and an accessible alternative route (for example, an assisted digital channel) in place, ship the fixed journey when it passes testing, and record the decision and its rationale transparently.
C. Insist the entire beta launch moves back four weeks - accessibility is non-negotiable, so the whole service waits.
D. Defer entirely to the service owner's judgement and record your concern privately in your own notes.

**Ranking: B, C, D, A (most to least effective).**

**Explanation:** Frame it as user needs plus legal duty, then look for the option that serves both without false trade-offs. B wins because it refuses the binary: the 92% get their beta on time, screen reader users are never presented with a journey that fails them, the alternative route keeps the capability available accessibly, and the decision is recorded transparently - challenge to a stakeholder's framing delivered as a better option, which is stakeholder management at its best. C ranks second: its values are right and its outcome is lawful and inclusive, but it pays four weeks of delay for the whole service when a scoped solution existed - rigid where B is creative. D ranks third rather than last only because it does not itself ship the failing journey - but it is professional failure in slow motion: your role exists to advise on exactly this, and a concern recorded privately protects you while protecting no user. A is least effective: it knowingly launches a public government service that excludes disabled users, treats a legal obligation (and more importantly, people) as a percentage, and gambles that "the first post-launch sprint" - the most oversubscribed sprint in software history - will honour the debt. In UK public service, accessibility is not a feature to trade; it is part of what "working" means.

#### Question 10 (hard) - The strategic reuse dilemma

Your problem analysis is complete, and a common platform already used by two other services in the department would meet about 85% of your solution's requirements. Building bespoke would meet 100% but cost roughly three times more and add months. The business lead is adamant: "Our process is unique - the platform version means the caseworkers change how they work, and I won't accept that." Choose the MOST and LEAST effective responses.

A. Design the bespoke solution - the business knows its process, and stakeholder acceptance is essential to delivery.
B. Design around the platform and let the business lead discover the process changes during user acceptance testing, when it is too late to change course.
C. Take the disagreement seriously as a problem-shaping question: work with the business lead to examine the 15% gap - which differences are genuine legal or operational constraints, and which are historical habit; quantify what the caseworker changes actually involve; bring evidence from the two services already on the platform; and take the resulting genuine options, with costs and trade-offs, to the appropriate decision-makers transparently.
D. Escalate immediately to the programme board that the business lead is blocking strategic reuse.

**Most effective: C. Least effective: B.**

**Explanation:** C treats the standoff as what it really is - an undefined problem. "Ensure a problem and the desired outcomes are properly defined" and "challenge requirements and assumptions" are your role's opening duties, and the 15% gap is exactly where they apply: some of it will be genuine constraint (legislation, safeguarding, court deadlines), some will be "how we've always done it". Evidence from the two existing platform services converts the argument from opinion to experience, and putting the genuine options to decision-makers honours both the organisation's financial constraints and the business's legitimate knowledge. A capitulates before the analysis: it may even be the right answer, but chosen now it is an unexamined answer costing three times more of public money. D escalates a conversation you have not yet had - the board will rightly ask what the 15% contains, and you will not know. B is least effective because it is deceit with a delivery plan: engineering a fait accompli spends the business lead's trust permanently, and discovering imposed process changes at acceptance testing is how services get rejected by the very caseworkers who must adopt them. You would win the argument and lose the solution.

### Preparation tips

- **Anchor on the values, not on cleverness.** UK public sector scenarios reward user needs, transparency, collaboration, accessibility, and care with public money. When torn between options, ask which one a citizen watching would respect.
- **Learn your level's escalation rhythm.** At your level, the strong pattern is: engage directly first, be transparent always, escalate as a backstop with the person's knowledge - and accept support from senior architects readily, because "with support" is written into your skill descriptions, not a weakness.
- **Look for the option that dissolves the dilemma.** The best answer often refuses a false binary - launch inaccessibly versus delay everything; obey the senior architect versus defy them. Test-writers plant a third way; find it.
- **Beware the plausible extreme.** Options that are pure process ("insist on the full review without discussion") or pure pragmatism ("shipping matters") each honour one real value while trampling another. Effective options usually integrate two values.
- **Read the question format twice.** Most/least, ranking, and rating are scored differently; on a most/least item, the least-effective choice carries as many marks as the most.
- **Practise out loud.** Explain to a colleague why an option is weaker - if your reason is "it just feels off", dig until you can name the value it violates. The naming is what transfers to unseen scenarios.

### Common pitfalls

- **Answering idealistically instead of effectively.** The perfect-sounding option (delay everything for principle, refuse all compromise) often ignores practical delivery reality; effectiveness means both the value and the outcome.
- **Selecting passive options.** Choices that delay action, defer entirely to others, note concerns privately, or pass the problem along score poorly almost everywhere - and doubly so for a role whose entire purpose is to advise and decide.
- **Ignoring the organisational culture.** These scenarios reward the collaborative, transparent culture of government digital work; imported instincts from aggressive commercial cultures (win the argument, protect your position, punish opponents) mis-calibrate your answers.
- **Escalating first.** Escalation is a vital backstop and a poor opening move. Watch for the pattern across scenarios above: direct engagement first, transparency throughout, escalation when engagement fails - except where formal routes exist precisely for first resort, such as genuine security incidents or safety risks.
- **Solving the wrong dilemma.** Under exam conditions it is easy to answer the scenario you expected rather than the one written. Check who owns what, what has been verified versus assumed, and what stage the decision is at before choosing.
- **Forgetting you have a remit.** Some options fail by overreach (unilaterally deciding another team's design) and some by underreach (treating team morale as not your job). Your role profile defines the boundary; the best options sit exactly on it.


## Conclusion

Well done for working through this resource - it represents a serious investment in your own development, and that investment compounds.

You have now practised the four kinds of thinking that psychometric assessments measure for your role, and that your role demands every day. In the **cognitive** section you traced dependencies, caught contradictions in decision records, sequenced migrations, and framed problems before solving them. In the **numeric** section you compared hosting and sourcing costs, converted availability percentages into real minutes, sized capacity with proper headroom, and modelled the peaks that averages hide. In the **verbal** section you held the line between what a standard, an email, or a supplier notice actually says and what it merely invites you to assume. And in the **situational judgement** section you navigated governance pressure, supplier propriety, accessibility trade-offs, and the delicate work of disagreeing well with senior colleagues - always returning to the values of public service: user needs, transparency, collaboration, and inclusion.

If some questions went wrong, be encouraged rather than discouraged: every worked explanation you studied is a pattern you now own, and the mistakes you make in practice are exactly the ones you will not make when it counts. Revisit the sections where you hesitated, build the small habits the tips describe - tag the modal verbs, write the units, bracket the estimate, engage before escalating - and let a little time pass before a second attempt; improvement between attempts is the most reliable evidence of growth.

Beyond any assessment, keep feeding the capabilities themselves: volunteer for an options analysis, offer to present at your architecture community of practice, ask a senior solution architect to walk you through a decision they found hard. Each of those is practice too - just unscored.

You chose a role that turns problems into working services for the public. The clear thinking you have practised here is how that happens. Good luck - you are better prepared than you were when you started reading.
