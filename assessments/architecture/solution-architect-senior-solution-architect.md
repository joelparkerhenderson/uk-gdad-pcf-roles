# Solution Architect (Senior Solution Architect) - Psychometric Assessment Resources

## Introduction

Welcome. This document is written for you as a senior solution architect working within the UK Government Digital and Data (GDAD) Profession Capability Framework. It is designed to help you understand, practise, and prepare for the four types of psychometric assessment most commonly used in recruitment, progression, and development for roles like yours: workplace job-specific cognitive ability, numeric reasoning, verbal reasoning, and situational judgement assessments.

Psychometric assessments are structured, standardised exercises that measure the mental processes and behavioural judgement that underpin effective performance in a specific role. For a senior solution architect, that means far more than abstract puzzle-solving. Your role demands that you frame problems of medium complexity so that solutions can be created, make and guide architectural design decisions characterised by medium risk, communicate complicated or risky architecture topics to senior stakeholders, weigh commercial sourcing options, and maintain the coherence of technical designs as circumstances change. Well-designed assessments for your role therefore use the artefacts you genuinely handle: architecture decision records, option appraisals, capacity and cost models, governance papers, technology roadmaps, spend approvals, and stakeholder correspondence.

These assessments matter for several reasons. First, they are widely used in Civil Service recruitment and in supplier and partner organisations, so familiarity reduces anxiety and lets your genuine ability show. Second, practising them sharpens the exact skills your role level requires: rapid pattern recognition across architectural options, precise reading of standards and policy text, sound arithmetic on budgets and capacity figures, and calibrated judgement in politically sensitive situations. Third, they are a valuable self-reflection tool. Working through the practice questions honestly will show you where your reasoning is strongest and where a little deliberate practice would pay off, which supports your own development and your coaching of other solution architects.

This document is organised into four main assessment sections. Each one explains what the assessment measures, maps its dimensions to the specific GDAD skills named in your role summary, then provides a substantial set of realistic practice questions with full answers and worked explanations, followed by preparation tips and common pitfalls. The scenarios are all drawn from your role: designing solutions for organisational problems, complying with standards and governance, managing risks and decisions transparently, and working with senior stakeholders across business and technical areas.

How to use this document: work through the questions under gentle time pressure first, then review the explanations carefully, including for the questions you answered correctly. The reasoning in the explanations is where most of the learning happens. Return to the sections periodically as part of your continuing professional development, and consider using selected questions as coaching material when you support other solution architects to follow best practice.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive ability assessment is a targeted psychometric test that measures the exact mental processes needed for your role, rather than abstract intelligence. Unlike a generic IQ test, it uses practical workplace scenarios and data drawn from the day-to-day work of a senior solution architect: architecture diagrams, decision logs, dependency maps, governance checklists, technology roadmaps, and integration sequences. The intent is to predict how effectively you will reason when confronted with real architectural material under realistic time pressure.

Typical format and timing: these tests are usually delivered online, timed at 15 to 30 minutes, and scored objectively against a benchmark or norm group. Some platforms are adaptive, adjusting question difficulty based on your previous answers, and most offer short ungraded practice questions before the scored section begins so you can get comfortable with the interface. Employers typically receive a breakdown of speed versus accuracy rather than a single raw score, so working both quickly and carefully matters.

For a senior solution architect, cognitive assessments concentrate on five mental operations: pattern recognition (spotting recurring structures across architectures, roadmaps, and incident histories), logical deduction (drawing valid conclusions from constraints, standards, and dependencies), error checking (finding inconsistencies in design documents, decision records, and configuration tables), prioritisation (sequencing work when everything appears urgent), and structured problem solving (decomposing an ill-defined organisational problem into a tractable shape). These are precisely the operations you perform when you ensure a problem and the desired outcomes are properly defined, when you design and document solutions so they can be implemented, and when you manage risks and decisions in a transparent way.

### What it measures for your role

Each cognitive dimension maps directly onto skills named in your role profile:

- Pattern recognition maps to **Architect for the whole context**: tracking emerging issues, strategies, roadmaps, patterns and technologies over time to assess opportunities and risks, and aligning your work with other architects and technical professionals. Test items ask you to detect trends and repeated structures across multiple artefacts.
- Logical deduction maps to **Making architectural decisions**: making and guiding design decisions characterised by medium risk and complexity, and using architectural governance and assurance to manage technical risks at the appropriate level. Test items present constraints and ask what must, might, or cannot follow.
- Error checking maps to **Technical design throughout the life cycle**: maintaining appropriate quality and architectural coherence of a technical design in response to change. Test items hide inconsistencies in tables, diagrams described in text, and decision records for you to find.
- Prioritisation maps to **Problem definition and shaping** and to your role-level duty to support multiple architecture projects simultaneously. Test items ask you to sequence competing demands rationally.
- Structured problem solving maps to **Strategy design** and **Problem definition and shaping**: framing a problem of medium complexity so that a solution can be created, and describing options so that appropriate delivery methods can be decided.

### Practice questions

**Question 1 (easy) - Pattern recognition in a technology roadmap**

Your department's technology roadmap shows the following pattern of platform migrations completed per quarter: Q1: 2 migrations, Q2: 3 migrations, Q3: 5 migrations, Q4: 8 migrations. A colleague asks you to estimate Q5 if the established pattern continues.

A) 10 migrations
B) 11 migrations
C) 12 migrations
D) 13 migrations

**Correct answer: C) 12 migrations.**

**Explanation:** Examine the differences between consecutive terms: 3 - 2 = 1, 5 - 3 = 2, 8 - 5 = 3. The increments themselves increase by one each quarter, so the next increment is 4, giving 8 + 4 = 12. In roadmap analysis this style of reasoning matters because delivery velocity rarely grows linearly; recognising an accelerating or decelerating pattern early lets you challenge whether supporting capabilities, such as environments and assurance capacity, will scale with it. Note that in real strategy work you would also question whether extrapolation is valid at all, which is exactly the kind of assumption-challenging your Strategy design skill calls for.

**Question 2 (easy) - Logical deduction from architecture standards**

Your organisation's technical standards state: "All citizen-facing services must use the central identity platform. All services using the central identity platform must complete a data protection impact assessment (DPIA). Service Alpha is citizen-facing. Service Beta has completed a DPIA."

Which conclusion is valid?

A) Service Beta uses the central identity platform.
B) Service Alpha must complete a DPIA.
C) Service Beta is citizen-facing.
D) Service Alpha has already completed a DPIA.

**Correct answer: B) Service Alpha must complete a DPIA.**

**Explanation:** Chain the rules forward: Alpha is citizen-facing, therefore Alpha must use the central identity platform, therefore Alpha must complete a DPIA. Options A and C commit the fallacy of affirming the consequent: completing a DPIA is required by identity platform use, but nothing says only identity platform users complete DPIAs, so Beta's DPIA tells us nothing about its architecture or audience. Option D confuses an obligation ("must complete") with a completed state. This distinction between what a standard obliges and what has actually happened is one you will apply constantly when you comply with standards and governance and when you review other architects' assurance evidence.

**Question 3 (moderate) - Error checking a decision record**

You are reviewing an architecture decision record (ADR) before it goes to the design authority. It contains these statements:

1. "We evaluated three options: extend the legacy case management system, buy a commercial off-the-shelf product, or build on the department's shared platform."
2. "Option 2 (COTS) was rejected because its licence cost of £480,000 per year exceeded the £450,000 annual budget ceiling."
3. "Option 3 (shared platform) was selected because it was the only option within budget."
4. "Option 1 (extend legacy) was estimated at £390,000 per year but rejected due to unsupported middleware."

Which pair of statements is logically inconsistent?

A) Statements 1 and 2
B) Statements 2 and 4
C) Statements 3 and 4
D) Statements 1 and 4

**Correct answer: C) Statements 3 and 4.**

**Explanation:** Statement 3 claims the shared platform was "the only option within budget", but statement 4 says the legacy extension was estimated at £390,000 per year, which is under the £450,000 ceiling. So at least two options were within budget, contradicting statement 3. The legacy option was rejected for a different and legitimate reason (unsupported middleware), but the ADR's stated rationale for selecting option 3 is factually wrong as written. Catching this matters: design authorities and audit teams rely on ADRs as the transparent record of how risks and decisions were managed, and a rationale that does not survive scrutiny undermines trust in the whole decision. Your duty to manage risks and decisions in a transparent way makes this precision non-negotiable.

**Question 4 (moderate) - Dependency deduction**

Five workstreams must be sequenced. The constraints are: the API gateway must be live before the payments integration starts. The payments integration and the notifications service can run in parallel, but both need the identity service live first. The identity service needs the API gateway live first. The reporting module can only start after the payments integration finishes.

Which workstream must be delivered first?

A) Identity service
B) API gateway
C) Notifications service
D) Payments integration

**Correct answer: B) API gateway.**

**Explanation:** Build the dependency chain: identity requires the gateway; payments requires both the gateway and identity; notifications requires identity; reporting requires payments to finish. Every other workstream has at least one predecessor, and the gateway has none, so it must come first. The full valid order is gateway, then identity, then payments and notifications in parallel, then reporting. This is the reasoning you use when you produce architectural representations that enable different teams to have a shared understanding of the delivery sequence, and when you identify architectural risks that affect multiple teams: a slip in the gateway cascades through everything downstream, so it deserves the strongest risk mitigation.

**Question 5 (moderate) - Prioritisation across multiple projects**

You support three architecture projects. On Monday morning you face four demands: (1) a design authority board meets at 14:00 today and your options paper for Project A has an unresolved reviewer comment; (2) Project B's delivery manager wants a two-hour whiteboard session this week to explore a new integration idea; (3) Project C reports a production incident in which a component you designed is suspected, with the incident manager requesting architectural input "as soon as possible"; (4) a junior solution architect you coach has asked for feedback on a draft ADR before their Wednesday review.

What is the most defensible order to address these?

A) 1, 2, 3, 4
B) 3, 1, 4, 2
C) 3, 4, 1, 2
D) 1, 3, 2, 4

**Correct answer: B) 3, 1, 4, 2.**

**Explanation:** The production incident (3) affects live service to users now and explicitly requests your input; live user harm outranks internal deadlines. The board paper (1) has a hard same-day deadline at 14:00, and design authority governance is a formal gate, so it comes next. The coaching feedback (4) has a Wednesday deadline, so it precedes the exploratory session (2), which is important but flexible within the week. Option C wrongly places coaching above a same-day governance deadline; options A and D let a formal meeting outrank a live incident. Assessors look for reasoning that weighs user impact first, then hard governance deadlines, then dated commitments, then flexible work. This mirrors your role-level duty to support multiple architecture projects while remaining responsive to operational risk.

**Question 6 (moderate) - Pattern recognition in incident data**

Reviewing twelve months of major incidents across the services you architect, you notice: incidents involving the legacy messaging middleware occurred in months 1, 4, 7 and 10; incidents involving the cloud file store occurred in months 4, 8 and 12. The two incident types co-occurred once, in month 4, and the joint incident took three times as long to resolve as either type alone.

If both patterns continue at the same regular intervals, in which upcoming month (13 to 18) should you plan for the elevated risk of both systems generating incidents in the same month?

A) Month 14
B) Month 15
C) Month 16
D) Month 18

**Correct answer: C) Month 16.**

**Explanation:** The middleware follows a three-month cycle (1, 4, 7, 10), so its next incidents fall in months 13 and 16. The file store follows a four-month cycle (4, 8, 12), so its next incidents fall in months 16 and 20. The first common month is 16. You can also reason via the lowest common multiple: cycles of 3 and 4 coincide every 12 months, and the last co-occurrence was month 4, so the next is month 16. Two further points make this realistic for your role. First, spotting compounding failure windows is exactly the kind of cross-system risk identification your Architect for the whole context skill describes: tracking emerging issues over time to assess risks to your work. Second, in real work you would treat the extrapolation itself as an assumption to challenge - four data points and three data points are thin evidence for a cycle - but you would still raise the month-16 window with service owners in advance, because the cost of preparing is low and the observed cost of a joint incident (three times the resolution time) is high. That is transparent, proportionate risk management.

**Question 7 (moderate) - Logical deduction about governance rules**

Your architecture governance framework states: "A design may proceed to build if and only if it has design authority approval. Designs with medium or high risk require a security review before design authority approval. Design X has a security review booked for next week. Design Y proceeded to build last week."

Which statement must be true?

A) Design X is medium or high risk.
B) Design Y had design authority approval.
C) Design Y was low risk.
D) Design X cannot receive design authority approval this week.

**Correct answer: B) Design Y had design authority approval.**

**Explanation:** The phrase "if and only if" makes design authority approval both necessary and sufficient for proceeding to build. Since Y proceeded to build, Y must have had approval - that is the only conclusion forced by the rules. Option A fails because a security review might be booked voluntarily or for other reasons; the rule says medium/high risk requires a review, not that a review implies medium/high risk. Option C fails because Y could have been medium or high risk and completed its security review before approval. Option D fails because "booked for next week" does not preclude the review being rescheduled or the design being low risk and not needing it at all. Reading governance rules with this precision is central to using architectural governance and assurance to make design decisions, and to contributing to the development of that governance yourself: rules with unintended logical gaps are ones you should spot and fix.


**Question 8 (moderate) - Error checking a capacity configuration table**

You are assuring a technical design before a go-live gate. The design document includes this environment configuration table:

| Environment | Instances | vCPU per instance | Total vCPU | RAM per instance (GB) | Total RAM (GB) |
|---|---|---|---|---|---|
| Development | 2 | 4 | 8 | 16 | 32 |
| Test | 4 | 4 | 16 | 16 | 64 |
| Staging | 6 | 8 | 48 | 32 | 192 |
| Production | 12 | 8 | 96 | 32 | 348 |

Which row contains an arithmetic error?

A) Development
B) Test
C) Staging
D) Production

**Correct answer: D) Production.**

**Explanation:** Verify each row: Development 2 x 4 = 8 vCPU and 2 x 16 = 32 GB, correct. Test 4 x 4 = 16 and 4 x 16 = 64, correct. Staging 6 x 8 = 48 and 6 x 32 = 192, correct. Production 12 x 8 = 96 vCPU is correct, but 12 x 32 = 384 GB, not 348 GB - the digits have been transposed. Transposition errors are among the most common defects in design documents, and this one matters: a 36 GB understatement in stated production RAM could mislead capacity planning, cost forecasting, and incident diagnosis. Maintaining appropriate quality of a technical design in response to change means routinely re-verifying derived figures whenever any source figure changes; an assured design with wrong numbers is worse than an unassured one, because people trust it.

**Question 9 (hard) - Structured problem solving with constraints**

A directorate asks you to "sort out the case-handling backlog with technology". Investigating, you establish four facts: (F1) 60% of backlog cases are stuck awaiting evidence from one external agency whose interface is a monthly paper exchange; (F2) caseworkers spend 30% of their time re-keying data between two internal systems; (F3) the oldest internal system exits vendor support in 14 months; (F4) the directorate has budget approval for exactly one major initiative this financial year.

Which initiative most directly addresses the largest defined component of the stated problem?

A) Replace the oldest internal system before support expires.
B) Build an automated data bridge between the two internal systems.
C) Establish a digital evidence exchange with the external agency.
D) Procure a workflow tool to track backlog cases more accurately.

**Correct answer: C) Establish a digital evidence exchange with the external agency.**

**Explanation:** The stated problem is the backlog. F1 tells you 60% of backlog cases are blocked on the paper-based external exchange, so the largest single cause of the defined problem is the evidence exchange, making C the most direct intervention. Option B addresses a real inefficiency (F2) but re-keying slows throughput generally rather than blocking the specific majority of stuck cases. Option A addresses a looming risk (F3) that is important but is a continuity concern, not a backlog cause; it belongs on the roadmap with a decision point well before month 14. Option D improves visibility of the problem without reducing it. This is problem definition and shaping in action: you ensured the problem and desired outcomes were properly defined before selecting a solution, decomposed it with evidence, and matched the single available initiative (F4) to the dominant cause. In a written options paper you would also record A as a time-bound risk and B as a candidate for a smaller continuous-improvement effort, showing stakeholders the whole picture transparently.

**Question 10 (hard) - Deduction across teams and domains**

Three teams consume your shared document service. Team 1's service must retain documents for 7 years. Team 2's service must delete documents within 90 days of case closure. Team 3's service must keep documents indefinitely pending litigation holds. The shared service currently applies one global retention policy to all stored documents.

Which conclusion is logically unavoidable?

A) The shared service must be split into three separate services.
B) No single global retention policy can satisfy all three teams' requirements.
C) Team 2's requirement should be relaxed to align with Team 1's.
D) The litigation hold requirement takes legal precedence over the others.

**Correct answer: B) No single global retention policy can satisfy all three teams' requirements.**

**Explanation:** The requirements are mutually exclusive under a single global rule: any one policy that deletes within 90 days violates the 7-year and indefinite requirements, and any policy retaining for 7 years or indefinitely violates the 90-day deletion requirement. Therefore B is forced by pure logic. Option A overreaches: per-tenant or per-document-class retention policies within one shared service would also resolve the conflict, so splitting the service is one design option, not a necessity. Options C and D are policy judgements that may or may not be right, but nothing in the given facts establishes them. This question rehearses a pattern you will meet constantly when you identify architectural risks that affect multiple teams or domains: distinguish what the constraints force (the conclusion) from what they merely suggest (candidate designs), and present the two separately so that stakeholders can see which parts of your recommendation are negotiable.

**Question 11 (hard) - Prioritising risks by expected impact**

Your risk log for a solution lists four architectural risks. Risk W: probability 0.5, impact if realised 20 days of delay. Risk X: probability 0.1, impact 120 days. Risk Y: probability 0.8, impact 10 days. Risk Z: probability 0.25, impact 48 days. Mitigation budget allows you to fully mitigate exactly two risks. Which pair maximises the expected delay avoided?

A) W and X
B) X and Z
C) W and Z
D) X and Y

**Correct answer: B) X and Z.**

**Explanation:** Compute expected delay for each: W = 0.5 x 20 = 10 days; X = 0.1 x 120 = 12 days; Y = 0.8 x 10 = 8 days; Z = 0.25 x 48 = 12 days. The two largest expected impacts are X (12) and Z (12), so mitigating both avoids an expected 24 days, more than any other pair (W+X = 22, W+Z = 22, X+Y = 20). Notice the cognitive trap: Y feels most urgent because it is most likely, and X feels scariest because its impact is largest, yet ranking requires the product of both. In practice you would layer further judgement on top - a 120-day tail risk may deserve mitigation regardless of expected value because it threatens the programme's viability, and that is a defensible position to argue at a risk board - but the assessment tests whether you can do the expected-value arithmetic first and depart from it deliberately rather than by instinct. Transparent risk management means showing this calculation in your papers so others can challenge your weighting.

**Question 12 (hard) - Pattern and rule integration on a technology roadmap**

Your organisation's roadmap principles state: "No service may depend on a component scheduled for decommissioning within 18 months. Components are decommissioned exactly 24 months after their replacement enters live service." The replacement for the current API gateway entered live service 9 months ago. A team proposes a new 12-month build that will, at go-live, depend on the current (old) API gateway.

Is the proposal compliant at its go-live date?

A) Yes, because the old gateway will still be running at go-live.
B) No, because at go-live the old gateway will be within 18 months of decommissioning.
C) Yes, because the 18-month rule applies only at proposal time, which is now.
D) No, because the old gateway has already been decommissioned.

**Correct answer: B) No, because at go-live the old gateway will be within 18 months of decommissioning.**

**Explanation:** Work the timeline. The replacement went live 9 months ago, so the old gateway decommissions at month +15 from today (24 - 9 = 15). The proposed build takes 12 months, so at go-live the old gateway has 15 - 12 = 3 months of life remaining - far inside the 18-month exclusion window. In fact, the proposal fails the rule even today, because 15 months is already within 18 months of decommissioning, which makes option C doubly wrong (and note the rule as written does not restrict itself to proposal time). Option A confuses "still running" with "compliant", and option D miscalculates the timeline. This is exactly the reasoning behind aligning your work with the work being done by other architects: roadmap rules encode cross-team commitments, and a senior solution architect is expected to run these date calculations before a dependency is baked into a design, then help the team find the compliant alternative - here, building against the new gateway from the start.

**Question 13 (hard) - Selecting the flawed inference in an options paper**

An options paper you are peer-reviewing argues: "Cloud provider P hosts 70% of our department's workloads. Our three most reliable services all run on provider P. Therefore, moving the remaining 30% of workloads to provider P will make them more reliable."

What is the strongest criticism of this inference?

A) It relies on figures that are probably out of date.
B) It confuses correlation with causation and ignores selection effects.
C) It fails to consider the cost of migration.
D) 70% is not a large enough majority to justify the conclusion.

**Correct answer: B) It confuses correlation with causation and ignores selection effects.**

**Explanation:** The paper observes that reliable services run on provider P and infers that provider P causes reliability. But with 70% of workloads on P, the most reliable services are statistically likely to be there regardless of any causal effect, and the reliable services may be reliable for other reasons: mature engineering teams, simpler architectures, older and well-hardened codebases. Selection effects could even run the other way - perhaps the most important services were deliberately placed on P and given the most operational investment. Options A and C raise legitimate practical questions but do not attack the logical structure of the argument, and option D misunderstands the flaw: the problem is not the size of the majority but the direction of inference. Spotting this pattern protects you when vendors, enthusiastic teams, or even your own preferences dress correlation up as evidence. Challenging requirements and assumptions is a named element of your Strategy design skill, and it applies to internal arguments as much as to external ones.

### Preparation tips

- Practise with the artefacts of your trade. Reread a recent ADR, options paper, or capacity plan and actively hunt for logical gaps and arithmetic slips. Ten minutes of deliberate error-checking a day builds the exact muscle these tests measure.
- Rehearse dependency reasoning. Take any current programme plan and sketch its dependency graph from the text alone, then verify it with the delivery manager. Both the sketching and the verification are training.
- Under timed conditions, read the question stem before studying the data. Knowing what you are looking for typically halves the time you spend in a table or passage.
- Manage the clock like a portfolio, not a queue. As someone who supports multiple architecture projects, you already triage; apply the same discipline here. Bank the questions you can do quickly, flag the ones you cannot, and return if time allows.
- Trust structured methods over instinct for probability and sequence questions. Write the expected-value products or the timeline arithmetic down (or type them into the on-screen notepad if provided) rather than holding them in your head.
- Sleep, hydration, and a quiet environment genuinely move scores on speeded tests. Treat the assessment sitting with the same logistical seriousness you would give a design authority presentation.

### Common pitfalls

- Overthinking beyond the given information. Senior architects habitually add context ("but in reality the roadmap would slip..."). In the test, reason strictly from the facts provided; save the contextual critique for real work.
- Getting stuck on a single hard multi-stage question and losing four easier ones. Adaptive and speeded formats reward moving on; a flagged skip is a tactical decision, not a failure.
- Confusing "must be true" with "is probably true". Deduction questions ask what the constraints force. If you find yourself estimating likelihood, re-read the question stem.
- Misreading rule direction. "All X require Y" does not mean "all Y are X". Governance-rule questions are built to catch exactly this reversal.
- Skimming tables and missing units or scale qualifiers, such as per-instance versus total figures. The configuration-table question above fails people mainly through hurried reading, not weak arithmetic.
- Assuming your experience of "how it usually works" overrides the scenario. The test rewards fidelity to the stated rules, just as governance rewards fidelity to the written standard rather than folklore about it.


## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment evaluates your ability to analyse, interpret, and make sound decisions using numerical data of the kind your role genuinely produces and consumes. It is business mathematics, not abstract formulae: percentages, ratios, unit costs, capacity figures, budget variances, and cost-benefit estimations, presented in tables, charts, and short data narratives. For a senior solution architect, the source material is unmistakably yours: cloud consumption reports, licence and support cost schedules, total cost of ownership comparisons across sourcing options, performance and capacity metrics, migration burn-down figures, and benefit projections attached to business cases.

Typical format and timing: online delivery with a strict time limit, usually 20 to 30 minutes for 15 to 25 questions, so under 90 seconds per question on average. Most platforms allow or provide an on-screen calculator because the intent is to test interpretation and decision-making rather than mental arithmetic. Questions frequently share a dataset: one table may feed three or four questions, which rewards investing 20 seconds up front to understand the table's structure, units, and scale qualifiers (thousands, millions, per-month versus per-year).

Why it matters for your role: you work within business and technical constraints, and most constraints arrive as numbers. When you understand organisational objectives and external drivers such as financial constraints, you are being asked to reason about budget envelopes, spend controls, and unit economics. When you describe options for solving problems so that appropriate delivery methods can be decided, credible option appraisal means credible arithmetic: a senior stakeholder will forgive a cautious estimate but not a broken one. And when you weigh sourcing strategies from your commercial perspective, comparing a commercial off-the-shelf licence, a software-as-a-service subscription, and an in-house build is fundamentally a structured numerical comparison over time.

### What it measures for your role

- Budget and cost analysis maps to **Commercial perspective**: understanding commercial processes and different sourcing strategies means comparing licence models, support tiers, and multi-year cost profiles numerically before recommending one.
- Option appraisal arithmetic maps to **Problem definition and shaping** and **Making architectural decisions**: describing options so delivery methods can be decided, and making design decisions of medium risk, both rest on defensible cost, capacity, and risk numbers.
- Capacity and performance interpretation maps to **Technical design throughout the life cycle**: creating and refining technical designs requires reading throughput, utilisation, and growth figures correctly, and re-checking them as designs change.
- Trend and forecast reading maps to **Architect for the whole context** and **Strategy design**: tracking roadmaps and emerging issues over time, and supporting a strategy with a roadmap or plan, both involve projecting figures forward and knowing the limits of the projection.
- Presenting numbers to others maps to **Architecture communication**: the explanations in this section model how to show working transparently, which is the same discipline you use when you communicate risky architecture topics to senior stakeholders and need every figure to survive challenge.

### Practice questions

**Question 1 (easy) - Percentage change in cloud spend**

Your solution's monthly cloud hosting cost was £42,000 in January. By April it has risen to £52,500. What is the percentage increase from January to April?

A) 20%
B) 25%
C) 30%
D) 10.5%

**Correct answer: B) 25%.**

**Explanation:** Percentage increase = (new - old) / old x 100 = (52,500 - 42,000) / 42,000 x 100 = 10,500 / 42,000 x 100 = 25%. A common error is dividing by the new value (10,500 / 52,500 = 20%), which is option A and understates the growth. Getting the base right matters when you report cost trends to a programme board: a 25% quarterly rise in hosting spend is a material trend that should trigger investigation of whether the growth is traffic-driven (defensible) or waste-driven (actionable), and your transparent risk management duty means presenting the correct figure even when a smaller one would be more comfortable.

**Question 2 (easy) - Licence cost per user**

A commercial case management product costs £180,000 per year for an enterprise licence covering up to 1,200 users. Your service currently has 800 users. What is the effective annual cost per actual user?

A) £150
B) £180
C) £225
D) £240

**Correct answer: C) £225.**

**Explanation:** Effective cost per actual user = £180,000 / 800 = £225. The distractor £150 (option A) is the cost per licensed seat (180,000 / 1,200), which is the vendor's framing, not yours. This distinction is at the heart of a commercial perspective: vendors quote per-seat prices at full utilisation, but your organisation pays for the whole tier regardless of usage. If usage is expected to stay near 800, a lower tier or a per-user contract may be better value, and if growth to 1,200 is genuinely forecast, the enterprise tier amortises well. Either way, the number you take to a spend approval conversation is £225 today with a trajectory, not £150.

**Question 3 (easy) - Reading a utilisation table**

Your production platform report shows:

| Component | Capacity (requests/sec) | Peak load (requests/sec) |
|---|---|---|
| API gateway | 2,000 | 1,400 |
| Identity service | 1,500 | 1,200 |
| Case service | 900 | 675 |
| Document store | 1,200 | 600 |

Which component is running at the highest peak utilisation?

A) API gateway
B) Identity service
C) Case service
D) Document store

**Correct answer: B) Identity service.**

**Explanation:** Compute peak utilisation as peak load divided by capacity for every row: gateway 1,400 / 2,000 = 70%; identity 1,200 / 1,500 = 80%; case service 675 / 900 = 75%; document store 600 / 1,200 = 50%. The identity service is highest at 80%. The trap is eyeballing raw numbers: the gateway carries the largest absolute load (1,400 requests/sec) yet has the second-lowest utilisation, so option A tempts anyone who skips the division. Always calculate the ratio for each row rather than trusting visual size. In your technical design work this is the difference between "the gateway is our busiest component" (true but unhelpful) and "the identity service is our scaling bottleneck" (the design-relevant fact). An 80% peak utilisation figure on a shared identity dependency is also a cross-team risk of exactly the kind your Making architectural decisions skill expects you to identify and address, because every consuming service degrades together when it saturates.

**Question 4 (moderate) - Three-year total cost of ownership**

You are comparing two sourcing options for a document processing capability. Option 1 (SaaS): £15,000 per month subscription, £60,000 one-off onboarding. Option 2 (build on shared platform): £320,000 build cost in year 1, then £8,000 per month running costs from the start of year 2. What is the total cost of each option over three years, and which is cheaper?

A) SaaS £600,000; Build £512,000; Build is cheaper
B) SaaS £600,000; Build £416,000; Build is cheaper
C) SaaS £540,000; Build £512,000; Build is cheaper
D) SaaS £600,000; Build £512,000; SaaS is cheaper

**Correct answer: A) SaaS £600,000; Build £512,000; Build is cheaper.**

**Explanation:** SaaS: 36 months x £15,000 = £540,000, plus £60,000 onboarding = £600,000. Build: £320,000 in year 1, then running costs for years 2 and 3 only = 24 months x £8,000 = £192,000, total £512,000. Build is cheaper by £88,000 over three years. Option B forgets that running costs apply for two years, not one; option C forgets the onboarding fee; option D computes correctly then reads the comparison backwards. In a real options paper you would go further - the build option carries delivery risk, opportunity cost of team capacity, and a different exit profile, while SaaS carries lock-in and per-unit growth pricing - but the arithmetic backbone must be right first, because every stakeholder challenge starts by testing your numbers. This is the commercial perspective and option-description work of your role in its purest numerical form.

**Question 5 (moderate) - Budget variance**

Your architecture project has a delivery budget of £1.8 million for the financial year. At the end of month 8, spend to date is £1.35 million. Assuming spend continues at the same average monthly rate, by how much will the project overspend or underspend at year end?

A) Overspend by £225,000
B) Overspend by £112,500
C) Underspend by £150,000
D) Overspend by £450,000

**Correct answer: A) Overspend by £225,000.**

**Explanation:** Average monthly spend so far = £1,350,000 / 8 = £168,750. Projected annual spend = £168,750 x 12 = £2,025,000. Variance = £2,025,000 - £1,800,000 = £225,000 overspend. Option B halves the true variance, a decoy for anyone who projects only half the remaining months; option C is what you get if you compare spend to date against eight-twelfths of the budget the wrong way round (8/12 x 1,800,000 = 1,200,000, and 1,350,000 - 1,200,000 = 150,000 is actually an overspend against profile, not an underspend); option D doubles the variance. The most valuable habit here, in tests and in budget papers alike, is to recompute the flagged answer once, quickly, before you commit. In your role, run-rate projections like this are how financial constraints show up in architecture: an overspending delivery often pressures teams to cut scope in ways that threaten architectural coherence, so an architect who reads the burn rate early can propose deliberate descoping options before the crunch, which is far better than absorbing panic cuts later. That is what working within business and technical constraints looks like in practice.


**Question 6 (moderate) - Ratio reasoning on team allocation**

An architecture practice supports projects in the ratio 3:2:1 across three programmes (Casework, Payments, Data). The practice has 18 architect-days available per week. Following a reprioritisation, Payments' share must increase by 50% while total capacity stays fixed and Casework and Data keep their ratio to each other.

How many architect-days per week does Payments receive after the change?

A) 6
B) 9
C) 8
D) 7.5

**Correct answer: B) 9.**

**Explanation:** Initial allocation: ratio 3:2:1 over 18 days gives Casework 9, Payments 6, Data 3. Payments increases by 50%: 6 x 1.5 = 9 days. The remaining 9 days are split between Casework and Data in their preserved 3:1 ratio, giving 6.75 and 2.25. The question only asks for Payments, so 9 is the answer, but computing the knock-on effects is the real skill: a 50% uplift to one programme halves nothing politely - Casework drops from 9 to 6.75 days, a 25% cut it will certainly notice. When you support multiple architecture projects and advocate on behalf of teams to other stakeholders, being able to state precisely what a reprioritisation costs each party turns an emotional negotiation into an evidence-based one, and managing stakeholder expectations effectively starts with numbers everyone can verify.

**Question 7 (moderate) - Performance percentile interpretation**

A performance report for your solution states: median API response time 240 ms; 95th percentile 900 ms; 99th percentile 2,100 ms. The service standard requires 95% of requests to complete within 1,000 ms. The service handles 400,000 requests per day. Approximately how many requests per day exceed 900 ms?

A) 4,000
B) 20,000
C) 40,000
D) 900

**Correct answer: B) 20,000.**

**Explanation:** By definition, the 95th percentile is the value below which 95% of requests fall, so 5% of requests exceed 900 ms. 5% of 400,000 = 20,000 requests per day. Option A (4,000) is 1%, confusing the 95th with the 99th percentile; option C (40,000) is 10%. Note what the report does and does not establish: the standard requires 95% within 1,000 ms, and the 95th percentile is 900 ms, so the standard is currently met with 100 ms of margin - but the 99th percentile at 2,100 ms means 4,000 requests a day take more than two seconds, a tail that harms real users even while the headline standard is green. Percentile fluency lets you challenge a "we meet the standard" claim with "and 4,000 users a day still wait over two seconds", which is the kind of user-focused, evidence-led challenge your Strategy design skill describes when it says to challenge requirements and assumptions.

**Question 8 (moderate) - Migration burn-down**

A migration must move 1,440 legacy interfaces to a new integration platform in 12 months. After 4 months, 360 interfaces are migrated. The delivery manager says the remaining work will accelerate by 25% per interface-throughput once tooling improvements land next month. If the improved rate applies from month 5 onward, will the migration finish on time, and with what margin?

A) Yes, finishing about 0.4 months early
B) No, finishing about 1.6 months late
C) Yes, finishing exactly on time
D) No, finishing about 3.2 months late

**Correct answer: B) No, finishing about 1.6 months late.**

**Explanation:** Current rate = 360 / 4 = 90 interfaces per month. Improved rate = 90 x 1.25 = 112.5 per month. Remaining work = 1,440 - 360 = 1,080 interfaces. Time at improved rate = 1,080 / 112.5 = 9.6 months. Total = 4 + 9.6 = 13.6 months against a 12-month target: about 1.6 months late. The optimistic framing ("will accelerate by 25%") invites you to assume the problem is solved; the arithmetic shows the uplift closes only part of the gap, and the honest options are more throughput, less scope, or more time. Presenting this calculation transparently - here is the rate, here is the gap, here are the levers - is precisely how you manage risks and decisions in a transparent way, and it converts a difficult message into a decision senior stakeholders can actually make.

**Question 9 (hard) - Weighted scoring in an options appraisal**

Your options appraisal scores three solutions against weighted criteria (weights in brackets): Fit to user needs (40%), Cost (30%), Delivery risk (20%), Strategic alignment (10%). Scores out of 10:

| Criterion | Option A | Option B | Option C |
|---|---|---|---|
| Fit to user needs (40%) | 8 | 6 | 9 |
| Cost (30%) | 5 | 9 | 4 |
| Delivery risk (20%) | 7 | 8 | 5 |
| Strategic alignment (10%) | 9 | 5 | 8 |

Which option has the highest weighted score?

A) Option A
B) Option B
C) Option C
D) Options A and B tie

**Correct answer: B) Option B.**

**Explanation:** Work each option fully. Option A: (8 x 0.4) + (5 x 0.3) + (7 x 0.2) + (9 x 0.1) = 3.2 + 1.5 + 1.4 + 0.9 = 7.0. Option B: (6 x 0.4) + (9 x 0.3) + (8 x 0.2) + (5 x 0.1) = 2.4 + 2.7 + 1.6 + 0.5 = 7.2. Option C: (9 x 0.4) + (4 x 0.3) + (5 x 0.2) + (8 x 0.1) = 3.6 + 1.2 + 1.0 + 0.8 = 6.6. Option B wins at 7.2. This result surprises many people because Option A "feels" strongest - it leads on strategic alignment and is second on the heavily weighted user-need criterion - and Option C tops the single biggest criterion outright. The intuition trap is anchoring on the most visible criterion rather than the weighted whole. There is a second, deeper lesson for your role: weighted scoring models are highly sensitive to their weights. If user-need fit rose from 40% to 50% at cost's expense, A would score 7.3, B 6.9, and C 7.1, flipping the recommendation entirely. A senior solution architect presenting a scoring table to a design authority should always run the weights personally rather than trusting the spreadsheet's author, and should show the sensitivity of the outcome to the weights, because that is where honest disagreement usually lives. Surfacing it is what managing decisions in a transparent way means in practice.

**Question 10 (hard) - Compound growth in storage costs**

Your solution's document store holds 40 TB and grows at 15% per quarter. Storage costs £22 per TB per month. Approximately what will the monthly storage bill be one year from now?

A) £880
B) £1,232
C) £1,540
D) £1,760

**Correct answer: C) £1,540.**

**Explanation:** Four quarters of 15% compound growth: 40 x 1.15^4. Compute stepwise: 1.15^2 = 1.3225; 1.3225^2 = 1.749. So 40 x 1.749 = 69.96, call it 70 TB. Monthly cost = 70 x £22 = £1,540. Option A is today's bill (40 x 22 = £880); option B applies simple rather than compound growth (40 x 1.6 = 64 TB gives £1,408, and 40 x 1.4 = 56 TB gives £1,232 - the 4 x 10% error); option D doubles today's bill. Compounding is the recurring blind spot in capacity and cost planning: 15% per quarter feels modest but is 75% per year compounded, and at that rate the store doubles roughly every 5 quarters. When you find and use emerging technologies and approaches, such as tiered or archival storage, this is the arithmetic that turns "storage is getting expensive" into a quantified business case with a payback date.

**Question 11 (hard) - Availability arithmetic across dependencies**

Your solution depends on three services in series: the identity platform (99.9% availability), the integration layer (99.5%), and the case database (99.8%). Assuming independent failures, what is the approximate end-to-end availability, and does it meet a 99.5% service commitment?

A) 99.9%; yes
B) 99.5%; yes, exactly
C) 99.2%; no
D) 98.9%; no

**Correct answer: C) 99.2%; no.**

**Explanation:** Series availability multiplies: 0.999 x 0.995 x 0.998. Stepwise: 0.999 x 0.995 = 0.994005; 0.994005 x 0.998 = 0.992017, so about 99.2%. That is below the 99.5% commitment, so the design as drawn cannot meet its service level even if every component meets its own. A quick approximation confirms it: summed unavailabilities are 0.1% + 0.5% + 0.2% = 0.8%, giving roughly 99.2%. The design insight is that a chain is always weaker than its weakest link when links are in series, and the integration layer at 99.5% consumes the entire error budget alone. Your options are redundancy around the weakest component, renegotiating the commitment, or removing the serial dependency. Spotting that a proposed design arithmetically cannot meet its stated commitment is exactly the kind of architectural risk affecting multiple teams that your role exists to catch before the design authority does.

**Question 12 (hard) - Benefit realisation with a one-off cost**

A proposed automation will cost £240,000 to build and £4,000 per month to run. It replaces manual processing that costs £18,000 per month. How many months after go-live does the automation break even, and what is the net saving over 36 months?

A) Break even at month 14; net saving £264,000
B) Break even at month 18; net saving £264,000
C) Break even at month 17.1; net saving £280,000
D) Break even at month 14; net saving £360,000

**Correct answer: B) Break even at month 18; net saving £264,000.**

**Explanation:** Net monthly saving = £18,000 - £4,000 = £14,000. Break-even = £240,000 / £14,000 = 17.14 months, so the build cost is fully recovered during month 18 - break-even is reached at month 18 in whole-month terms (option C's 17.1 is the exact division but assessments usually want the month in which cumulative savings first exceed cost: 17 x 14,000 = 238,000 < 240,000, and 18 x 14,000 = 252,000 > 240,000, confirming month 18). Net saving over 36 months = (36 x £14,000) - £240,000 = £504,000 - £240,000 = £264,000. Option A pairs the right saving with a wrong break-even month (240/18 = 13.3 misuses the gross saving); option D uses the gross £18,000 in one figure and not the other. When you understand organisational objectives and external drivers such as financial constraints, this payback arithmetic is the shared language between your architecture and the finance team's approval processes, and getting the whole-month convention right shows attention to how the audience will actually read the figure.

### Preparation tips

- Rebuild the arithmetic behind one real artefact each week: a cloud bill, a business case benefit table, or a capacity forecast. Recreating someone else's numbers from their sources is the highest-fidelity practice available and also makes you a sharper reviewer.
- Drill the four operations that dominate these tests: percentage change (with the correct base), ratios and re-allocations, compound growth, and weighted averages. Fluency here frees time for the genuinely hard questions.
- Read table headers, units, and scale qualifiers before touching any numbers. Per-month versus per-year and thousands versus millions cause more wrong answers than hard mathematics does.
- Use the on-screen calculator for arithmetic but do the setup on paper or in your head first: decide the formula, then compute. Typing exploratory calculations wastes the seconds the test is designed to price.
- Estimate before you compute. If a three-year SaaS cost is roughly 36 x 15k = 540k plus onboarding, you know any option far from 600k is wrong before dividing precisely - a senior architect's sanity-check reflex, applied under time pressure.
- Practise presenting one calculation aloud in two sentences, as if to a senior stakeholder. The discipline of stating base, operation, and result cleanly is the same discipline the test measures, and it doubles as preparation for board conversations.

### Common pitfalls

- Using the wrong base for percentage change, especially dividing by the new value instead of the original. Distractor options are built from exactly this error.
- Confusing per-unit vendor framings (cost per licensed seat) with your organisation's true unit cost (cost per actual user). The commercial perspective questions above show how different the two can be.
- Applying simple growth where compounding is stated. "15% per quarter" for a year is 1.15 to the fourth power, not 60%.
- Misreading scale qualifiers such as "in thousands", or mixing monthly and annual figures in one calculation - the most common defect in real business cases too.
- Over-calculating: computing every option's figure to three decimal places when estimation eliminates half the options immediately. The clock is part of the test.
- Sinking time into one multi-stage question. Flag it, bank the quick wins, return if time allows. Expected marks per minute is the metric, exactly as expected impact ranks your risk log.
- Accepting a stated conclusion without a single verification pass. As Question 9 demonstrates, intuition about which option "feels strongest" routinely disagrees with the weighted arithmetic; the recomputation habit is worth more than any formula.


### A note on numbers and seniority

At senior solution architect level, assessors are less interested in whether you can divide and more interested in whether you choose the right things to divide. Notice how many of the questions above turn on framing: the correct base for a percentage, the whole tier versus the used seats, the compound versus simple growth model, the expected value versus the scary headline figure. That framing judgement is what separates a number-literate architect from a calculator. It is also what your stakeholders are paying for: when a programme director asks "can we afford option two?", the valuable answer names the assumptions, states the arithmetic in one clean line, and identifies which assumption the answer is most sensitive to. Practising these questions with that standard in mind will improve both your test scores and your board papers, and it will give you concrete, worked examples to use when coaching other solution architects in commercial and numerical reasoning.


## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment evaluates how well you understand, analyse, and draw correct conclusions from written business information that mirrors the reading demands of your role. For a senior solution architect, that means dense, precise texts: technology standards and their exception clauses, governance terms of reference, security and data-protection policy extracts, supplier contract passages, design review feedback, and carefully worded emails from senior stakeholders. The core discipline is fact-based logic: you must answer strictly from the text provided, ignoring your outside knowledge - even where the passage's fictional policy differs from real government guidance you know well.

Typical format and timing: a passage of 100 to 300 words followed by two to five statements, each to be judged True (the passage logically supports it), False (the passage logically contradicts it), or Cannot Say (the passage provides insufficient information either way). Multiple-choice comprehension items are often mixed in, asking for the best summary, the author's main concern, or the correct application of a stated rule. Timing is tight, usually less than a minute per question, simulating the reality of absorbing a governance paper minutes before the meeting that discusses it.

Why it matters for your role: architecture is a writing-and-reading profession. You design and document solutions so they can be implemented by the organisation, which means others' ability to act depends on your precision with language. You comply with standards and governance, which means extracting exactly what a standard obliges, permits, and forbids - and noticing what it is silent about. You lead the communication of complicated, complex or risky architecture topics, which requires reading your audience's words as carefully as you choose your own. And when you challenge requirements and assumptions, the challenge usually starts by noticing that a document claims more than its evidence supports.

### What it measures for your role

- Precise extraction of obligations maps to **Making architectural decisions**: using architectural governance and assurance correctly depends on reading exactly what a governance rule requires, at what risk level, and with what exceptions.
- Distinguishing stated fact from inference maps to **Problem definition and shaping**: framing a problem properly requires separating what stakeholders have actually said from what everyone has assumed, and producing representations that create genuinely shared understanding.
- Reading tone, nuance, and position maps to **Architecture communication**: adapting your message to your audience, managing stakeholder expectations, and advocating on behalf of a team all begin with accurately reading what senior stakeholders have written, including what they carefully did not say.
- Spotting unsupported claims maps to **Strategy design**: challenging requirements and assumptions is, in textual form, the Cannot Say judgement - recognising when a strategy document asserts something its own evidence does not establish.
- Contract and policy comprehension maps to **Commercial perspective**: understanding commercial processes includes reading supplier terms, framework conditions, and internal spend-control policy with the precision the questions below rehearse.

### Practice questions

**Passage 1 (for Questions 1-4)**

"The department's Technology Standards Board (TSB) reviews all solution designs classified as medium or high risk. Designs classified as low risk may proceed without TSB review, provided the lead architect records the classification rationale in the decision log. The TSB meets fortnightly, and papers must be submitted at least five working days before a meeting. Where a design requires changes following review, the revised design must be re-submitted to the TSB unless the changes are confined to matters the Board has explicitly delegated to the lead architect. In the last financial year, the TSB reviewed 64 designs, of which 41 were approved without change."

**Question 1 (easy)**

True, False, or Cannot Say: "A low-risk design may proceed without TSB review if the classification rationale is recorded in the decision log."

**Correct answer: True.**

**Explanation:** The second sentence states this almost verbatim: low-risk designs "may proceed without TSB review, provided the lead architect records the classification rationale in the decision log." The statement accurately restates both the permission and its condition. Note the precision required: if the statement had said low-risk designs "must proceed without review" (removing choice) or "may proceed without any record" (removing the condition), it would be False. Verbal reasoning rewards matching the logical structure - permission plus condition - not just the keywords, which is the same care you apply when deciding whether your own design genuinely qualifies for a governance exemption.

**Question 2 (easy)**

True, False, or Cannot Say: "The TSB rejected 23 designs last financial year."

**Correct answer: Cannot Say.**

**Explanation:** The passage says 64 designs were reviewed and 41 were "approved without change". That leaves 23 designs that were not approved without change - but the passage also tells us that some designs require changes following review and are then re-submitted or handled under delegation. Those 23 could have been approved with changes, deferred, withdrawn, or rejected; the passage does not say. The tempting arithmetic (64 - 41 = 23) is correct as arithmetic but wrong as inference, because "not approved without change" is not the same category as "rejected". This is precisely the trap in real governance reporting: a design authority's statistics are often summarised in briefings as "23 designs failed review", and a senior architect who reads the source knows the claim outruns the data.

**Question 3 (moderate)**

True, False, or Cannot Say: "A design revised after TSB review must always return to the TSB before proceeding."

**Correct answer: False.**

**Explanation:** The passage states revised designs must be re-submitted "unless the changes are confined to matters the Board has explicitly delegated to the lead architect." The word "always" in the statement is defeated by this explicit exception: there exists a class of revisions that need not return to the Board. Watch for absolute quantifiers - always, never, all, only, must - in test statements; they are True only when the passage is equally absolute. In your governance work the same reading protects teams from unnecessary process: an architect who misreads this rule as "always re-submit" adds a fortnight's delay to changes the Board deliberately delegated, and part of supporting others to follow best practice is knowing where the rules genuinely leave discretion.

**Question 4 (moderate)**

Which of the following is the latest a paper can be submitted for a TSB meeting?

A) Five calendar days before the meeting
B) Five working days before the meeting
C) One fortnight before the meeting
D) The passage does not specify a deadline

**Correct answer: B) Five working days before the meeting.**

**Explanation:** The passage says "papers must be submitted at least five working days before a meeting." The phrase "at least" makes five working days the minimum notice, hence the latest permissible submission point. Option A substitutes calendar days for working days - a difference that, across a weekend, costs two days and a missed board slot. Option C confuses the meeting frequency (fortnightly) with the submission deadline. Reading "working days" versus "calendar days" precisely is a small skill with outsized consequences in governance timetables, procurement clock-stops, and contract notice periods; senior architects who plan design authority submissions build this arithmetic into their delivery plans so that governance never becomes the critical path by accident.

**Passage 2 (for Questions 5-8)**

"Email from the Programme Director: 'Thank you for the options paper on the citizen correspondence platform. I recognise the analysis behind the recommendation to build on the cross-government notification service, and the projected savings are compelling. However, the Permanent Secretary has asked all programmes to reduce dependencies on services outside our departmental control before the next spending review. I am not asking you to change your recommendation. I am asking you to add an assessment of what it would take to exit the cross-government service within six months if required, and to be explicit about which of the projected savings survive under that scenario. Please treat this as a priority ahead of Thursday's investment committee.'"

**Question 5 (moderate)**

True, False, or Cannot Say: "The Programme Director has rejected the recommendation to use the cross-government notification service."

**Correct answer: False.**

**Explanation:** The Director writes, "I am not asking you to change your recommendation" - an explicit statement that the recommendation stands, which directly contradicts "rejected". The email adds a requirement (an exit assessment and a savings re-statement) without reversing the recommendation. Misreading conditional concern as rejection is a common and costly error in stakeholder communication: an architect who returns on Thursday with a changed recommendation has answered a question nobody asked, and has surrendered a position the Director was prepared to support. Managing stakeholder expectations effectively begins with reading their actual words, especially when the overall tone is cautionary but the specific instruction is narrow.

**Question 6 (moderate)**

True, False, or Cannot Say: "The Permanent Secretary has instructed the programme to stop using cross-government services."

**Correct answer: False.**

**Explanation:** According to the email, the Permanent Secretary asked programmes "to reduce dependencies on services outside our departmental control before the next spending review". Reducing dependencies is materially weaker than stopping use: it is a direction of travel with a timeframe, not a prohibition. The statement claims an instruction to stop, which the passage's own words contradict in strength - so False is the better judgement than Cannot Say, because the passage does report what was asked and it is not this. Be careful, though: the distinction between False and Cannot Say here is subtle, and hinges on the statement being an overstatement of a reported instruction rather than an unreported matter. In real work this reading precision determines whether you architect for reduced coupling (correct) or premature migration off a working shared service (expensive overreaction) - a distinction worth a great deal of public money.

**Question 7 (hard)**

True, False, or Cannot Say: "The projected savings in the options paper depend at least partly on continued use of the cross-government notification service."

**Correct answer: Cannot Say - but examine the strongest contrary reading.**

**Explanation:** The Director asks you "to be explicit about which of the projected savings survive under that scenario" of exit. This phrasing strongly suggests the Director believes some savings may not survive an exit, which would mean they depend on continued use. But suggestion is not statement: the email does not assert that any savings would be lost; it asks for an assessment of which survive - and the answer could, in principle, be "all of them". Strictly, the passage does not establish the dependency, so Cannot Say is the defensible verdict. This is the hardest judgement type in verbal reasoning: an implication that is probably true in context but not logically forced by the text. The professional parallel is exact: when a senior stakeholder's question implies a concern, you address the concern - but in written analysis you must not convert their implication into an asserted fact, because transparent decision records distinguish what is known from what is suspected.

**Question 8 (hard)**

Which action best matches the Programme Director's request?

A) Revise the options paper to recommend a departmentally controlled alternative.
B) Add an exit assessment covering feasibility within six months and re-state which savings hold under exit, before Thursday.
C) Prepare a briefing defending the cross-government service against the Permanent Secretary's concerns.
D) Postpone the investment committee until the dependency question is resolved.

**Correct answer: B.**

**Explanation:** The email contains two explicit asks - an assessment of what a six-month exit would take, and explicitness about which savings survive that scenario - plus a deadline (ahead of Thursday's investment committee) and an explicit non-ask (do not change the recommendation). Option B captures all three elements. Option A does what the Director expressly said not to do. Option C misreads the task: the Director wants analysis to inform a decision, not advocacy against the Permanent Secretary's direction - and advocating against your Permanent Secretary's stated policy in a committee paper is a career-shortening genre error. Option D exceeds the architect's authority and contradicts the instruction to treat the work as a priority for Thursday. Questions like this test whether you can decompose a senior stakeholder's email into its actionable components - a core skill when you communicate with senior stakeholders across your organisation and need to respond to exactly what was asked, at the level it was asked.


**Passage 3 (for Questions 9-11)**

"Extract from a supplier framework agreement: 'The Supplier shall provide the Hosting Services at the service levels set out in Schedule 2. Where the Supplier fails to meet a service level in two consecutive months, the Customer may, at its discretion, require a remediation plan, and the Supplier shall deliver such plan within ten working days of the request. Service credits accrue automatically for each service level failure as set out in Schedule 3, and are the Customer's sole financial remedy for service level failures, save in cases of wilful default. Nothing in this clause limits the Customer's right to terminate for material breach under Clause 14.'"

**Question 9 (moderate)**

True, False, or Cannot Say: "If the Supplier misses a service level in two consecutive months, it must automatically provide a remediation plan."

**Correct answer: False.**

**Explanation:** The clause says the Customer "may, at its discretion, require a remediation plan" - the plan is triggered by the Customer's request, not automatically by the second failure. The Supplier's obligation (delivery within ten working days) arises only "of the request". Contrast this with the service credits, which the clause says "accrue automatically". The statement transplants the automaticity from the credits to the plan, a subtle swap that changes who must act first. Contract questions in verbal tests love this distinction between automatic consequences and discretionary rights, and so do real disputes: an architect advising a service owner who believes a remediation plan is "owed" automatically will give wrong advice about next steps, when the correct action is simply to make the request in writing and start the ten-day clock.

**Question 10 (hard)**

True, False, or Cannot Say: "The Customer cannot recover financial losses beyond service credits for any hosting service failure."

**Correct answer: False.**

**Explanation:** The clause makes service credits "the Customer's sole financial remedy for service level failures, save in cases of wilful default." The saving phrase creates an exception: where failure amounts to wilful default, remedies beyond service credits are available. The statement's "for any hosting service failure" ignores that exception, so the passage contradicts it. Additionally, the final sentence preserves termination rights for material breach, which is a further route (though termination is not itself a financial recovery, the wilful default exception alone settles the question). The lesson generalises: exclusive-remedy clauses almost always carry carve-outs, and the carve-outs are where commercial risk actually lives. When your commercial perspective work involves reading supplier terms alongside procurement colleagues, hunting for "save", "except", "subject to", and "without prejudice to" is how a technical reader adds value in a commercial review.

**Question 11 (hard)**

True, False, or Cannot Say: "Schedule 2 defines the amounts of service credits payable."

**Correct answer: False.**

**Explanation:** The passage assigns service levels to Schedule 2 and service credits to Schedule 3 ("Service credits accrue automatically ... as set out in Schedule 3"). The statement attributes the credits to the wrong schedule, so the passage contradicts it as written. This looks pedantic until you draft a contract change notice referencing the wrong schedule, or search Schedule 2 for credit rates during an incident review and conclude they do not exist. Precision about where obligations live is the reading-level equivalent of architectural traceability: every claim in your design documents should be attributable to its source, and every source cited correctly, because colleagues will act on your citations without re-checking them - that is what documentation that "can be implemented by the organisation" means.

**Passage 4 (for Questions 12-13)**

"Extract from a departmental strategy paper: 'Our legacy case management estate comprises eleven systems, of which six share no common data model. Independent analysis estimates that 40% of caseworker time is spent on activities that would be unnecessary under a unified platform. The strategy therefore commits to a single case management platform by 2030. Early adopter business units will migrate from 2027. International evidence shows that unified platforms reduce processing times; the Netherlands achieved a 30% reduction within three years of consolidation. We expect comparable results.'"

**Question 12 (hard)**

Which of the following is a fact stated in the passage, rather than an expectation, estimate, or inference?

A) A unified platform will make 40% of caseworker time unnecessary.
B) The department will achieve a 30% reduction in processing times.
C) Six of the eleven legacy systems share no common data model.
D) Unified platforms reduce processing times in all countries.

**Correct answer: C.**

**Explanation:** Sort each claim by its epistemic label in the text. Option C is presented as a plain description of the current estate: "six share no common data model" - a stated fact. Option A converts an estimate ("independent analysis estimates that 40% of caseworker time...") into a promised outcome, and also subtly shifts from "activities that would be unnecessary" to "will make unnecessary". Option B converts an expectation ("we expect comparable results") about someone else's 30% into the department's own guaranteed result. Option D generalises one country's evidence ("the Netherlands achieved") into a universal claim. Strategy papers habitually blur these categories, and the senior architect's job when supporting the development of a strategy is to keep them separate - because delivery plans built on estimates-treated-as-facts fail in predictable ways, and because challenging assumptions requires first identifying which statements are assumptions.

**Question 13 (hard)**

True, False, or Cannot Say: "Migrating the early adopter business units from 2027 will allow the department to meet its 2030 commitment."

**Correct answer: Cannot Say.**

**Explanation:** The passage states two dates - early adopters migrate from 2027, single platform by 2030 - but says nothing about whether the migration schedule is sufficient to hit the commitment: nothing about how many business units exist, migration duration per unit, or dependencies between them. The statement asserts a sufficiency relationship the passage never establishes. It is neither supported (no schedule analysis is given) nor contradicted (nothing says the plan is infeasible), so Cannot Say. This mirrors a live professional judgement: a strategy's dates are commitments, not evidence of achievability, and the architect's roadmap work is exactly the analysis that would convert "from 2027" and "by 2030" into a substantiated or challenged plan. Until that analysis exists, an honest reviewer marks the sufficiency claim as unknown - in test language, Cannot Say.

### Preparation tips

- Read one dense governance or policy document each week with a highlighter discipline: mark every obligation (must), permission (may), condition (provided that), and exception (unless, save). The four categories are the skeleton of nearly every verbal reasoning item at this level.
- Practise the Cannot Say judgement deliberately, because it is the hardest and most examined. After reading any passage, write one statement the text supports, one it contradicts, and one it merely suggests. The third category is where senior candidates lose marks by "knowing too much".
- Suppress outside knowledge consciously. You know how real design authorities and frameworks operate; the test's fictional ones will differ in details, and only the passage counts. Say to yourself: "in this passage's world..."
- Scan the question before deep-reading the passage. Locate the relevant sentences with keywords, then read those sentences with full attention. Under a minute per question, reading everything twice is a luxury you do not have.
- Watch quantifiers and modality like an editor: all, some, only, always, never, must, may, should, will, expects. Most False answers are absolute statements about qualified text; most Cannot Say answers are plausible inferences dressed as facts.
- Use your professional reading as training both ways: treat test passages with the rigour of a contract review, and treat real contract reviews as verbal reasoning practice. The transfer is direct, and it sharpens the precise reading you use to lead communication of complex architecture topics.

### Common pitfalls

- Bringing in personal or professional knowledge instead of relying only on the provided text. Experienced architects fail verbal items not from weak reading but from strong memory - answering from real standards rather than the passage's fictional ones.
- Confusing "the passage suggests" with "the passage states". A strongly implied dependency, like the savings question in Passage 2, is still Cannot Say if the text never asserts it.
- Treating arithmetic as inference. "64 reviewed, 41 approved without change, therefore 23 rejected" is the classic trap: the subtraction is valid, the categorisation is not.
- Missing exceptions attached to general rules: "unless", "save in cases of", "subject to". At this level the exception, not the rule, is usually what the question tests.
- Swapping who must act: discretionary rights ("the Customer may require") misread as automatic obligations ("the Supplier must provide"). Contract passages are chosen precisely because they punish this.
- Poor time allocation: spending three minutes mastering a passage before seeing that its questions target two sentences. Skim the questions first, then read with purpose.
- Second-guessing verified answers under time pressure. If you have located the controlling sentence and matched its logic, commit and move on; changed answers under panic are usually changed for the worse.


### A note on reading at senior level

Two habits distinguish senior performance on verbal assessments, and both come straight from your day job. The first is reading for logical structure rather than gist. A programme director skims for the headline; you are paid to notice that the headline says "sole financial remedy" while the footnote says "save in cases of wilful default". Test questions at this level are engineered around exactly those load-bearing phrases, so train your eye to snag on them. The second habit is separating the four voices every professional document mixes: what is asserted as fact, what is estimated, what is promised, and what is merely hoped. Passage 4 above is a miniature of every strategy paper you will ever review - a real fact about the estate, an analyst's estimate, a dated commitment, and an international comparison carrying an expectation. Your Strategy design skill asks you to challenge requirements and assumptions; verbal reasoning practice is that challenge rehearsed in laboratory conditions, one statement at a time. When you coach other solution architects, consider reviewing a passage together and asking them to classify each sentence into those four voices before any question is asked. Architects who can do that reliably write better decision records, brief senior stakeholders more accurately, and spot the unsupported claim in a vendor's whitepaper before it becomes an unsupported claim in your department's business case. Finally, remember that in the test itself the passage is the entire universe: however well you know the real standard, contract, or strategy the passage resembles, the marks are awarded for reading what is actually on the page - a discipline that, not coincidentally, is also the safest starting point for reviewing any document that crosses a senior architect's desk.


## Workplace job-specific situational judgement assessment

### About this assessment

A workplace job-specific situational judgement assessment evaluates your decision-making, interpersonal skill, and professional conduct by presenting realistic workplace dilemmas and asking how you would respond. Unlike the cognitive, numeric, and verbal assessments, there is usually no single objectively right answer computed from data; instead, several responses may seem reasonable, and the scoring reflects how well your choices align with the values and behaviours the organisation needs from someone in your role. Timing is generous or absent, because the test measures natural judgement rather than speed.

The common response formats are: choose the most effective and least effective actions from a set of four or five; rank all options from best to worst; or rate each option's effectiveness independently. In UK public sector settings, the scoring key is anchored in values you will recognise: meeting user needs, transparency, collaboration across boundaries, accessibility and inclusion, effective stewardship of public money, and the Civil Service values of integrity, honesty, objectivity, and impartiality.

For a senior solution architect, the dilemmas are about the human systems around the technical ones: a design authority under time pressure, a senior stakeholder who wants governance skipped, a delivery team that has quietly diverged from the agreed design, a supplier whose roadmap slips, a junior architect whose confidence is fragile, a peer architect whose solution conflicts with yours. Your role summary is explicit that you communicate and work effectively with stakeholders, manage risks and decisions in a transparent way, build relationships with senior stakeholders across different business and technical areas, and lead and coach other solution architects. Situational judgement is where those duties are tested in their natural habitat: ambiguity, competing pressures, and incomplete information.

### What it measures for your role

- Stakeholder handling under pressure maps to **Architecture communication**: leading communication of complicated or risky topics, adapting your message to your audience, advocating on behalf of a team, and managing stakeholder expectations.
- Governance courage maps to **Making architectural decisions**: using governance and assurance at the appropriate level, and addressing architectural risks affecting multiple teams, even when it is socially costly.
- Team and community behaviour maps to **Community collaboration**: working collaboratively, giving feedback that is effective and lasting, spotting problems in team dynamics, and helping to stimulate the right responses.
- Coaching judgement maps to your role level's expectation that you support others to follow best practice for solution architecture, and may lead and coach other solution architects.
- Commercial and organisational awareness maps to **Commercial perspective** and **Architect for the whole context**: knowing when a dilemma is really a sourcing question, and recognising how your choice lands across other teams and domains.

### Practice questions

**Question 1 (moderate) - The stakeholder who wants to skip governance**

A director sponsoring your project tells you privately: "The design authority will only slow us down, and the Minister has promised this service by March. I want you to take the design straight to build and we will square the governance afterwards." The design has a medium risk classification, which under your organisation's rules requires design authority review before build.

Options:

A) Agree, since the director carries the delivery accountability, and document their instruction in the decision log.
B) Explain the rule, propose an expedited review with the authority's chair this week, and tell the director you cannot take a medium-risk design to build unreviewed.
C) Refuse and immediately escalate the director's request to the chief architect as a governance breach attempt.
D) Agree to start build on low-risk components only, while quietly scheduling the review for the full design.

**Most effective: B. Least effective: A.**

**Explanation:** Option B holds the governance line while genuinely solving the director's problem, which is time, not review-avoidance. Expedited review paths exist in most governance frameworks precisely for ministerial commitments, and offering one converts a confrontation into a service. It is also transparent: the director hears the rule and the plan directly. Option A is least effective: it abandons a control designed for medium-risk decisions and treats documentation as a substitute for compliance - the decision log records the breach without preventing it, and "squaring governance afterwards" is how departments end up explaining avoidable failures publicly. Option C leaps to escalation before attempting resolution; escalation is right if the director insists after B, but leading with it damages a senior relationship unnecessarily and skips the influencing work your role exists to do. Option D is the subtle trap: it sounds pragmatic, but "quietly" is the tell - it manages the conflict by concealment rather than transparency, and starting any build implicitly commits architecture before review. The values at stake are transparency, stewardship, and honest communication with senior stakeholders - and note that B demonstrates managing stakeholder expectations effectively rather than merely resisting them.

**Question 2 (moderate) - The team that diverged from the design**

During a routine catch-up, a developer mentions that their team replaced the agreed message queue with a different technology three sprints ago because "the agreed one was painful". The change is live in production, works well so far, but was never reviewed, is inconsistent with the department's approved technology list, and duplicates a capability another team runs centrally.

Options:

A) Instruct the team to revert to the agreed technology in the next sprint, since the deviation was unauthorised.
B) Retrospectively assess the change: understand why the agreed option was painful, evaluate the replacement's risks, bring the decision to lightweight governance, and use the lesson to improve how teams raise design friction.
C) Let it stand silently since it works, and note it for the next architecture review cycle.
D) Report the team's deviation to their delivery manager and ask for process retraining.

**Most effective: B. Least effective: C.**

**Explanation:** Option B treats the event as both a risk to manage and a signal to learn from. The unreviewed change needs assessment now (production risk, duplication of a central capability, support implications), and the fact that a team found the agreed design "painful" and felt unable to say so is a failure of the architecture-team relationship that you can fix - your Community collaboration skill explicitly covers identifying issues in team dynamics and stimulating the right responses. Option C is least effective because silence converts an unmanaged risk into an invisible one: "works well so far" is not assurance, the duplication cost is real and compounding, and your silence teaches teams that divergence is fine if quiet. Option A may ultimately be the right technical outcome, but ordering reversion before understanding why the design was painful punishes honesty, risks a live service for procedural symmetry, and forfeits the learning. Option D outsources a relationship problem to hierarchy and frames a systemic issue as individual misconduct. Working effectively with delivery teams means being the kind of architect people tell about problems early - and every choice here either builds or erodes that.

**Question 3 (moderate) - Coaching a struggling junior architect**

You coach a junior solution architect whose ADR for a moderately complex integration is weak: options are thin, the recommendation is under-evidenced, and a security consideration is missing. Their design authority review is in three days. They are visibly anxious and have already had one paper rejected this quarter; a second rejection would be demoralising and would delay a team waiting on the decision.

Options:

A) Rewrite the ADR yourself tonight to guarantee the review passes, and walk them through your changes afterwards.
B) Give them written feedback identifying the three gaps, offer a working session tomorrow where they revise it with you questioning and steering, and agree together whether to proceed or ask to defer a week.
C) Tell them the paper is not ready and advise them to withdraw it to avoid a second rejection.
D) Let the review proceed as a learning experience; design authorities exist to catch these gaps.

**Most effective: B. Least effective: A.**

**Explanation:** Option B is coaching as your role level defines it: supporting others to follow best practice, with feedback that is effective and lasting. The junior architect does the revision, so the capability grows where it needs to; the working session bounds their anxiety with concrete help; and involving them in the proceed-or-defer decision teaches the meta-skill of judging readiness against governance - while keeping the waiting team's needs visible in the trade-off. Option A is least effective even though it maximises the paper's short-term quality: it teaches dependence, hides the junior's development need from them, misrepresents their work to the design authority (a transparency problem), and guarantees you will be rewriting their next paper too. Option C protects them from rejection but decides for them and treats deferral as the only lever, when three days of guided revision might genuinely close the gaps. Option D abdicates coaching to the governance process: authorities catch defects, but a predictable public failure you could have prevented is poor stewardship of both the individual's confidence and the authority's time. Adapting feedback so it lands and lasts is the named skill here; B is what that looks like under deadline pressure.

**Question 4 (hard) - Two senior stakeholders, two incompatible asks**

The operations director wants your solution hosted on the department's established platform because her teams can support it. The digital director wants it on the new strategic cloud platform to build momentum for the department's cloud strategy, of which your solution would be the first significant workload. Both have written to you expecting support, both will attend the investment committee, and your analysis shows the strategic platform is better long-term but carries a support capability gap for at least a year.

Options:

A) Recommend the established platform, since proven supportability outweighs strategic momentum for a live public service.
B) Present both options to the committee with your analysis of the trade-off, without a recommendation, and let the directors resolve it at the right level.
C) Meet both directors together before the committee, share your analysis including the support gap, explore whether a funded support uplift would close it, and take an agreed or explicitly disagreed position to committee with a recommendation.
D) Recommend the strategic platform with a documented risk acceptance for the support gap, since architecture should lead the strategy.

**Most effective: C. Least effective: B.**

**Explanation:** Option C does the senior-architect work before the governance moment: building relationships with senior stakeholders across different business and technical areas means getting the two directors and the evidence into one conversation, where the real question - can the support gap be closed with money and time? - can be explored rather than adjudicated. Committees decide better when the options have been jointly examined, and whichever way it lands, you arrive with a recommendation and a transparent record of who accepts which risk. Option B is least effective for a senior architect: presenting analysis without a recommendation looks neutral but is an abdication - the committee is paying for your judgement, and letting the directors resolve it in public, unprepared, invites a political rather than evidential decision. Options A and D are defensible recommendations reached prematurely: each takes a side before testing whether the trade-off is actually fixed (A treats the support gap as permanent; D treats it as acceptable without asking operations what would make it acceptable). Sometimes managing stakeholder expectations means advocating for the conversation that dissolves the conflict, not for one side of it.

**Question 5 (moderate) - The supplier roadmap slip**

A SaaS supplier central to your solution announces that a feature your design depends on will slip by nine months. Your programme has committed public milestones based on it. The supplier account manager asks you to keep the slip quiet until their press announcement in six weeks, hinting that early disclosure could affect the "partnership spirit" and future pricing conversations.

Options:

A) Honour the supplier's request; six weeks changes little, and the commercial relationship matters for future negotiations.
B) Tell the supplier you must inform your programme now, do so, and work with commercial colleagues on the contractual and re-planning consequences, while asking the supplier what mitigation they can offer.
C) Inform your programme director confidentially but delay wider communication until the supplier's announcement.
D) Escalate the supplier's request to your commercial team as attempted undue influence and pause the relationship pending review.

**Most effective: B. Least effective: A.**

**Explanation:** Option B is transparent risk management performed at the speed the risk requires: a nine-month slip against public milestones is a programme-level risk the moment you know it, and your duty runs to your organisation, not to a supplier's communications plan. Involving commercial colleagues respects the internal contacts and processes your Commercial perspective skill names, and asking the supplier for mitigation keeps the relationship professional and forward-looking - firmness and partnership are not opposites. Option A is least effective: it subordinates a public commitment to a hinted pricing benefit, which fails every values test (transparency, stewardship, integrity) and, practically, wastes six weeks of re-planning time your programme will bitterly miss. Option C is half-transparency: it protects you while leaving delivery teams and dependent projects planning against a fiction, and puts your programme director in the position of sitting on the same secret. Option D overreads the situation - the account manager's request is poor practice to decline clearly, and worth mentioning to commercial colleagues, but "pausing the relationship" with a supplier central to your solution injures your own programme to punish a hint. Proportionate firmness, promptly transparent: that is the scored behaviour.

**Question 6 (hard) - The accessibility corner-cut**

Two weeks before a public beta, testing shows the solution's document upload journey fails accessibility standards for screen reader users. Fixing it properly delays beta by three weeks. The service owner proposes launching on time with a workaround: an instruction page telling affected users to phone a helpline instead. The delivery manager supports launching; the user researcher objects strongly; everyone looks at you.

Options:

A) Support the launch with the helpline workaround, provided the fix is prioritised immediately after beta and the risk is recorded.
B) Advise delaying beta three weeks: the service excludes disabled users from a core journey, and a phone fallback is not equivalent access.
C) Propose descoping document upload from beta entirely, launching the rest on time, and adding upload when it passes accessibility testing.
D) Defer to the service owner's authority and record your concern in the decision log.

**Most effective: C (with B a close and defensible second). Least effective: D.**

**Explanation:** Option C reframes the problem the way your Problem definition and shaping skill teaches: the binary "launch versus delay" hides a scope option that protects both the launch date and the principle that no user group gets a second-class journey. A beta without upload treats all users equally and creates honest learning; a beta whose upload journey excludes screen reader users ships inequality as a feature. Option B is strong and may be right if upload is truly inseparable from the beta's purpose; ranking C above B rewards finding the option that dissolves the trade-off rather than picking a side of it. Option A normalises inequality of access under a risk-register fig leaf: UK public services are legally and ethically bound to accessibility, and "phone us instead" is a segregated journey, not a workaround. Option D is least effective: recording concern while deferring entirely is the passive option these tests consistently punish, because it treats the decision log as a substitute for advocacy. You are the senior technical voice in the room; advocating on behalf of users and the team is named in your communication skill, and silence spends that mandate on self-protection.


**Question 7 (moderate) - The peer architect conflict**

A peer solution architect on an adjacent programme circulates a design that duplicates an integration capability your programme built and offered for reuse. In a cross-programme forum, they describe your capability as "not fit for our purposes" without having discussed it with you. You believe reuse would save their programme roughly £200,000 and reduce long-term divergence.

Options:

A) Respond in the forum with a point-by-point rebuttal showing their claims about your capability are wrong.
B) Contact them directly, ask what requirements drove their assessment, offer a technical walkthrough, and if genuine gaps exist, explore whether closing them serves both programmes; bring the outcome back to the forum either way.
C) Raise the duplication with the head of architecture, recommending the reuse question be decided at portfolio level.
D) Accept their assessment; each programme understands its own needs best, and forced reuse creates resentment.

**Most effective: B. Least effective: A.**

**Explanation:** Option B is community collaboration as your skill defines it: working collaboratively, actively networking, and rectifying issues in team dynamics. The direct conversation assumes good faith - "not fit for our purposes" may rest on a real requirement you have not heard, an outdated understanding of your capability, or pressure you cannot see - and the walkthrough replaces claim with evidence. Crucially, B closes the loop publicly ("bring the outcome back to the forum"), which repairs the record without a fight. Option A is least effective: winning a public rebuttal loses the relationship, hardens their position, and teaches the forum that architectural disagreement is combat - the opposite of the collaborative culture a senior architect is supposed to model. Option C is a legitimate second step if B fails or the duplication proves strategic, but leading with escalation skips the cheapest resolution path. Option D dresses conflict-avoidance as respect: £200,000 of duplication and permanent divergence is precisely the cross-team outcome your Architect for the whole context skill exists to catch, and silence serves nobody.

**Question 8 (hard) - The emerging technology enthusiasm**

Your chief technology officer returns from a conference enthusiastic about an emerging integration technology and asks you to "find a place for it" in your current solution, which is mid-delivery with a proven, boring design. The technology is genuinely promising but immature: sparse production evidence, one dominant vendor, and skills your organisation lacks. Declining outright could cost you influence with a stakeholder whose support your programme needs.

Options:

A) Introduce the technology in a peripheral, low-risk component of the current solution to satisfy the CTO while limiting exposure.
B) Propose a bounded evaluation: a time-boxed spike or pilot outside the critical path, with defined success criteria, a skills assessment, and a decision point on the roadmap for wider adoption if it proves itself.
C) Explain that changing a mid-delivery design for an immature technology is unjustifiable, and recommend revisiting it in a couple of years.
D) Ask the CTO to sponsor the change formally through the design authority so the decision and its risks are owned at the right level.

**Most effective: B. Least effective: C.**

**Explanation:** Option B honours both truths in the scenario: the technology may matter (your role level explicitly expects you to find and use emerging technologies and approaches) and the current delivery must not carry an immature dependency. A time-boxed, criteria-driven evaluation off the critical path converts enthusiasm into evidence, gives the CTO a genuine yes, protects the solution, and creates a transparent roadmap decision point - strategy design by pilot rather than by argument. Option A is the quiet compromise that satisfies nobody safely: even a "peripheral" production component creates support, security, and skills obligations, and choosing architecture to manage a stakeholder's mood rather than user or organisational need is a values failure that scoring keys detect reliably. Option C is least effective not because its risk assessment is wrong but because it slams a door on a senior relationship and on your own duty to track emerging technology: "revisit in a couple of years" gives the CTO's strategic instinct no legitimate outlet and forfeits influence your programme needs. Option D routes an informal ask straight into formal machinery, which reads as deflection - the design authority cannot evaluate what nobody has yet evidenced. Offer B; keep D's discipline for whatever the pilot recommends.

**Question 9 (hard) - The strategy you disagree with**

Your department adopts a strategy mandating a specific vendor's platform for all new casework solutions. Your analysis for your current problem shows the mandated platform fits poorly: it would cost roughly 40% more and constrain two important user needs, while a compliant alternative pattern exists within the strategy's stated objectives if interpreted flexibly. The strategy team, stung by earlier resistance from other programmes, has signalled that exception requests are unwelcome this quarter.

Options:

A) Comply fully with the mandate and record the cost and user-need impacts in the decision log.
B) Design using the alternative pattern and describe it in governance papers using the strategy's language, avoiding the word "exception".
C) Prepare a concise, evidence-based exception case - costs, user needs, and how the alternative still meets the strategy's objectives - share it with the strategy team privately first for their input, then take it through the formal route with their concerns addressed.
D) Delay the design decision this quarter and raise the platform's poor fit through the architecture community's feedback channels, hoping the strategy softens.

**Most effective: C. Least effective: B.**

**Explanation:** Option C is what supporting the development of a strategy actually means: strategies improve through evidenced challenge, and your Strategy design skill explicitly includes challenging requirements and assumptions and identifying opportunities to develop strategy. The sequencing matters - sharing the case privately first respects the strategy team's position, converts likely opponents into contributors, and means the formal submission arrives pre-socialised rather than as an ambush; this is how senior architects spend relationship capital deliberately. Option B is least effective because it is camouflage: engineering the language so that an exception does not look like one is a transparency failure that, when discovered, damages your credibility and the legitimacy of every future genuine exception, and denies the strategy team the very evidence that might improve the strategy. Option A is honest but supine: complying while recording a 40% cost premium and constrained user needs treats the decision log as a conscience rather than acting on what you know - stewardship of public money argues against silent compliance at that price. Option D avoids the hard conversation, delays a team that needs a decision, and outsources your professional judgement to community sentiment. The scored behaviours are transparency, evidence over positioning, user needs, and constructive challenge through legitimate routes - C carries all four.

**Question 10 (hard) - Ranking under procurement pressure**

Your programme is three weeks from a procurement decision between two suppliers. You realise the requirements you contributed months ago over-specify one integration constraint in a way that materially favours Supplier A, whose solution matches your department's incumbent patterns. Loosening the constraint would let Supplier B's architecture qualify and would likely intensify price competition, but reopening requirements now will delay the procurement by up to six weeks and irritate the commercial team.

Rank these options from most to least effective:

A) Say nothing; the requirement reflected genuine preferences at the time, and procurement timelines have their own integrity.
B) Raise the issue immediately with the commercial lead and programme director, explain the technical rationale and its competitive effect, and let the procurement professionals decide how to handle it within the rules.
C) Quietly tell Supplier B's bid team the constraint may be interpreted flexibly, evening the playing field without delaying the process.
D) Raise it in your next scheduled architecture forum for peer input before troubling the commercial team.

**Correct ranking: B, D, A, C.**

**Explanation:** Option B is first because it takes the knowledge to the people with the authority and expertise to act on it, immediately, through legitimate channels - understanding commercial processes and the appropriate internal contacts is a named element of your Commercial perspective skill, and a possibly distorted competition is a commercial-legal question, not an architectural judgement call. Note what B does not do: it does not decide unilaterally whether to reopen requirements; it surfaces the facts transparently and respects professional boundaries. Option D is second but clearly weaker: a scheduled forum adds days or weeks of delay to a time-critical disclosure, and peers cannot resolve what is fundamentally a procurement-integrity question. Option A is third: silence knowingly leaves a materially unfair specification in place - a stewardship and transparency failure that grows more expensive the later it surfaces, including after contract award, when it can void the procurement entirely. Option C is decisively last: privately advantaging one bidder, however equalising the intent, is a serious procurement breach that could disqualify the process and expose the department legally. Transparency through proper channels is not the cautious option here; it is the only survivable one.

### Preparation tips

- Before the assessment, write down the values you would want your decisions measured against: user needs, transparency, collaboration, accessibility and inclusion, stewardship of public money, and honest communication. Most scoring keys for UK public sector roles are recognisable restatements of these, and consciously naming them beforehand anchors your choices under pressure.
- Rehearse the shape of strong answers: address the problem directly, at the lowest effective level, through legitimate channels, transparently, while preserving relationships. Weak answers avoid, conceal, delay, escalate prematurely, or fix the mood instead of the problem.
- Distinguish "what I might do on a bad day" from "what the most effective response is". The test asks for your judgement of effectiveness, and your judgement is sound even when your energy is not.
- Use your real experience as a question bank: recall five difficult moments from your career and, for each, write the option you took plus three you did not, then decide which was most and least effective and why. This is nearly perfect practice and doubles as coaching material for the architects you develop.
- Read every option fully before rating any. Options are often engineered in near-pairs - the transparent version and the quiet version of the same action - and the difference lives in a single clause, exactly as it does in governance papers.
- Do not overcorrect into idealism. "Escalate everything to be safe" and "always delay for more analysis" score as poorly as recklessness; senior roles are scored for calibrated, proportionate action at the right level.

### Common pitfalls

- Choosing the passive option: recording concerns instead of voicing them, deferring to authority instead of advising, waiting for reviews instead of acting. Situational judgement scoring is consistently harsh on decision-log-as-conscience behaviour, as Questions 6 and 9 illustrate.
- Answering idealistically rather than practically: picking the response that sounds noble ("refuse and escalate immediately") over the one that actually resolves the situation at the lowest effective level.
- Ignoring the organisation's values: in UK public sector contexts, options that trade away accessibility, transparency, or fair competition for delivery speed or relationship comfort are scored failures however pragmatic they feel.
- Solving the mood instead of the problem: the quiet workaround, the private assurance, the reworded exception. Concealment options are seeded through these tests precisely because they tempt experienced, socially skilled professionals.
- Escalating too early or too late: leaping to the chief architect before attempting resolution wastes hierarchy; staying silent past the point where the risk outgrows you hoards it. The scored skill is choosing the level, not avoiding or embracing escalation as a policy.
- Forgetting your seniority: at your level, "someone should do something" usually means you. Options that outsource your judgement to committees, forums, or the passage of time read very differently for you than for a junior colleague.
- Treating the least-effective choice casually: many formats score your "least effective" selection equally. Apply the same care to identifying the worst option - usually the concealing or passive one, not the merely imperfect one - as you do to the best.

## Conclusion

You have now worked through a substantial set of practice materials built specifically for your role: cognitive questions drawn from the decision records, dependency maps, and governance rules you handle daily; numeric questions built on the budgets, capacity figures, and sourcing comparisons that shape your options papers; verbal passages with exactly the load-bearing clauses your standards and contracts contain; and situational dilemmas featuring the directors, delivery teams, suppliers, and junior architects who populate your real working week.

A few things are worth carrying forward. First, the skills these assessments measure are the same ones your role profile names - making architectural decisions, problem definition and shaping, architecture communication, commercial perspective, community collaboration, strategy design, technical design throughout the life cycle, and architecting for the whole context - so every hour of practice is also professional development, and every day of real architecture work is also assessment preparation. The transfer runs both ways. Second, the habits that raise scores are the habits that make senior architects trusted: verify the arithmetic once, read the exception clause, separate fact from estimate from hope, act transparently at the lowest effective level. Third, your role includes leading and coaching other solution architects; the worked explanations in this document were written to be reusable, and talking a less experienced colleague through why an option is weaker is one of the fastest ways to deepen your own judgement.

If some questions caught you out, that is the document doing its job - each explanation shows the reasoning so you can close the gap deliberately, and returning to a section after a few weeks is an excellent way to check the gap stayed closed. Approach any real assessment rested, unhurried, and curious, and treat it as what it is at your level: a structured mirror held up to capabilities you exercise every day. You design solutions for problems that affect your organisation, you manage risk in the open, and you help others do the same. Keep practising, keep coaching, and good luck.

