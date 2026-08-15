# Technical Architect (Lead Technical Architect) - Psychometric Assessment Resources

## Introduction

Welcome. This document is written for you as a lead technical architect working within the UK Government Digital and Data profession. As someone who leads the technical design of systems and services across multiple projects and teams, you already know that your role demands broad architectural thinking, sound judgement under uncertainty, and the ability to communicate complex decisions to stakeholders at every level. Psychometric assessments are one way that organisations measure exactly those capabilities, and this resource will help you understand, practise, and prepare for them with confidence.

Psychometric assessments are structured, standardised tests that measure how you think, reason, and make decisions. They are widely used across the Civil Service and the wider public sector for recruitment, promotion, and professional development. For a role at your level, they are rarely about raw speed with trivia; instead, they probe the mental processes you use every day: interpreting dense technical and policy documents, reasoning about capacity figures and budgets, spotting logical flaws in a proposed design, and judging the most effective course of action when architectural discussions become difficult or political.

This document covers four assessment types, each in its own section:

1. **Workplace job-specific cognitive assessment** - measuring pattern recognition, logical deduction, error checking, prioritisation, and problem solving using the artefacts you genuinely handle, such as architecture decision records, dependency maps, and assurance findings.
2. **Workplace job-specific numeric reasoning assessment** - measuring your ability to interpret tables, percentages, ratios, budgets, capacity figures, and performance metrics of the kind that inform real architectural decisions.
3. **Workplace job-specific verbal reasoning assessment** - measuring precise comprehension of policies, standards, emails, and reports, answered strictly from the text provided.
4. **Workplace job-specific situational judgement assessment** - measuring your professional judgement in realistic dilemmas involving delivery teams, senior stakeholders, suppliers, and cross-government partners.

Each section explains what the assessment measures, maps it explicitly to the skills in your role profile - architecting for the whole context, architecture communication, community collaboration, making architectural decisions, strategy design, and technical design throughout the life cycle - and then gives you a substantial set of practice questions with full worked explanations. Each section closes with preparation tips and common pitfalls.

How should you use this resource? First, read each "About this assessment" subsection so you know the format and timing to expect. Second, attempt the practice questions honestly, under light time pressure, before reading the explanations. Third, treat the explanations as self-reflection prompts: they are written to connect the reasoning back to your day-to-day leadership work, so even where you answered correctly, the discussion may sharpen how you justify and communicate decisions. Approached this way, the document doubles as preparation for assessments and as professional development for the role itself.

Take your time, be curious, and enjoy the practice. You bring years of experience to this; these pages simply help you show it.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive ability assessment is a targeted psychometric test designed to measure the exact mental processes needed for a specific role. Unlike a generic IQ test, it uses practical workplace scenarios and data drawn from the job itself to predict performance. For a lead technical architect, that means the questions mimic the everyday artefacts you actually handle: architecture decision records, service dependency maps, technology roadmaps, assurance review findings, incident timelines, and cross-government standards.

Typical delivery is online and timed, usually 15 to 30 minutes, with objective scoring against a norm group of comparable professionals. Modern platforms often include short, ungraded practice questions so you can learn the interface before the clock starts, and some use adaptive testing, adjusting question difficulty based on your previous answers. Employers generally receive a breakdown of speed versus accuracy rather than a single number, so a careful, deliberate approach that gets questions right is genuinely valued, not just raw pace.

At your level, cognitive items lean towards logical deduction across interacting systems, spotting inconsistencies between documents, sequencing and prioritising work under constraints, and diagnosing faults from partial evidence. These are precisely the habits of mind that let you assure the quality of other services, justify design decisions, and keep technical work aligned with broader government strategy.

### What it measures for your role

The assessment dimensions map directly onto the skills named in your role profile:

- **Making architectural decisions**: logical deduction and consistency-checking questions test whether you can make and guide design decisions characterised by medium risk and complexity, and identify architectural risks that affect multiple teams or domains. A question asking you to find the contradiction between two architecture decision records is a compressed version of governance work you do weekly.
- **Architect for the whole context**: pattern recognition and systems-thinking items test whether you can track emerging internal and external issues over time and reason about knock-on effects across the organisation, not just your immediate goals.
- **Technical design throughout the life cycle**: fault-diagnosis and error-checking items test the precision you need to create and review technical designs characterised by high risk, impact, and complexity, and to refine standards based on feedback.
- **Strategy design**: prioritisation and sequencing items test whether you can direct the implementation of a strategy or vision, for example by ordering roadmap activities when dependencies and constraints conflict.
- **Architecture communication**: several items ask you to identify which conclusion a set of facts does and does not support - the same discipline you use when justifying and communicating design decisions to technical and non-technical stakeholders without overclaiming.

### Practice questions

Work through these under light time pressure - aim for about two to three minutes per question - then read the explanations carefully.

#### Question 1 (easy) - Dependency deduction

Your programme has four services. Service A depends on Service B. Service B depends on Service C. Service D depends on Service A. Service C depends on nothing. A breaking change is planned to Service C's API.

Which services could be affected by the change?

- (a) B only
- (b) B and A only
- (c) B, A, and D
- (d) A and D only

**Answer: (c) B, A, and D.**

**Explanation:** Dependencies propagate transitively. B calls C directly, so B is affected. A depends on B, so a change in B's behaviour can reach A. D depends on A, so D can be reached too. This is the exact reasoning behind blast-radius analysis when you assure a change across multiple teams: you trace the full dependency chain, not just the first hop. A common error is stopping at direct consumers, which is answer (a); at lead level you are expected to reason about second- and third-order effects across domains.

#### Question 2 (easy) - Odd one out in architectural principles

Four draft principles are proposed for your organisation's architecture principles catalogue. Three share a common characteristic; one does not. Which is the odd one out?

- (a) "Reuse before buy, buy before build."
- (b) "Expose business capabilities as well-defined APIs."
- (c) "The payments team should adopt PostgreSQL 16 by Q3."
- (d) "Design services to degrade gracefully under partial failure."

**Answer: (c).**

**Explanation:** Options (a), (b), and (d) are genuine principles: durable, technology-agnostic statements of intent that guide many decisions over time. Option (c) is a specific, dated, team-level implementation decision - roadmap content, not a principle. Your skill in strategy design includes defining architectural principles and patterns, and a frequent real-world review task is separating principles from decisions so that governance artefacts stay at the right altitude.

#### Question 3 (moderate) - Contradiction between decision records

You are assuring a service and read two architecture decision records (ADRs).

- ADR-014 (approved in March): "All citizen-facing services in this programme must authenticate users via the department's single sign-on platform. Exceptions require Design Authority approval."
- ADR-031 (approved in July): "The appeals service will use its own bespoke username-and-password store to reduce dependency on shared platforms."

ADR-031 contains no reference to the Design Authority. Which statement is the most defensible conclusion?

- (a) ADR-031 supersedes ADR-014, so no action is needed.
- (b) ADR-031 conflicts with ADR-014 and there is no evidence the required exception was granted, so it needs investigation.
- (c) ADR-014 was clearly wrong and should be retired.
- (d) The appeals service is not citizen facing, so ADR-014 does not apply.

**Answer: (b).**

**Explanation:** The two records conflict on their face: ADR-014 mandates single sign-on for citizen-facing services with a defined exception route; ADR-031 departs from that mandate and shows no evidence of the exception being granted. You cannot conclude supersession (a) - later does not automatically mean overriding, especially where an explicit exception process exists. Option (d) invents a fact not in evidence: an appeals service used by citizens gives no indication of being exempt. Option (c) leaps to a judgement with no supporting information. The disciplined move - and the one your architectural governance and assurance skill demands - is to flag the inconsistency and investigate before approving anything downstream.

#### Question 4 (moderate) - Sequencing a migration

A legacy case-management system must be decomposed. The teams agree on five activities:

1. Build the new case API.
2. Put a strangler-fig facade in front of the legacy system.
3. Migrate historical case data.
4. Switch write traffic to the new API.
5. Decommission the legacy system.

Constraints: the facade must exist before any traffic can be routed anywhere new; write traffic cannot switch until the new API exists and historical data is migrated; decommissioning requires all traffic to have switched.

Which ordering is valid?

- (a) 1, 3, 4, 2, 5
- (b) 2, 1, 3, 4, 5
- (c) 3, 4, 1, 2, 5
- (d) 2, 4, 1, 3, 5

**Answer: (b).**

**Explanation:** Test each constraint. Option (b): facade first (2), then build the API (1), migrate data (3), switch writes (4) - which is legal because the API exists and data is migrated - then decommission (5). All constraints hold. Option (a) switches traffic (4) before the facade exists (2), violating the routing constraint. Option (c) migrates data and switches writes before the API is even built. Option (d) switches writes (4) before the API exists (1) and before data migration (3). This is the sequencing logic you apply when directing the implementation of a strategy through roadmaps: identify hard dependencies first, then order everything else around them.

#### Question 5 (moderate) - Error checking an options appraisal

A team's options appraisal contains this passage: "Option 1 (rehost) has the lowest one-off cost. Option 2 (re-platform) has a higher one-off cost than Option 1 but lower annual running cost than both other options. Option 3 (rebuild) has the highest one-off cost and its annual running cost is lower than Option 2's."

What is wrong with this passage?

- (a) Nothing; it is internally consistent.
- (b) It contradicts itself about which option has the lowest annual running cost.
- (c) It contradicts itself about which option has the highest one-off cost.
- (d) It omits Option 1's annual running cost, making it unreadable.

**Answer: (b).**

**Explanation:** The second sentence says Option 2's annual running cost is lower than both other options - so Option 2 is the cheapest to run. The third sentence says Option 3's annual running cost is lower than Option 2's - so Option 3 is cheaper to run than Option 2. Both cannot be true; that is a direct contradiction. The one-off cost statements are consistent (Option 1 lowest, Option 3 highest, Option 2 between), so (c) is wrong. Option (d) points at an omission, but omission is not the contradiction the question exposes. Catching exactly this kind of inconsistency before an options paper reaches a spend control board is core assurance work at your level: a governance decision made on self-contradictory evidence is a risk that affects multiple teams.

#### Question 6 (moderate) - Pattern recognition in incident data

Over six releases, the number of post-release incidents attributed to integration defects was: 2, 3, 5, 8, 12, 17. If the underlying pattern continues, how many such incidents should you expect after the next release, and what kind of growth does the series show?

- (a) 21; linear growth
- (b) 23; growth with a linearly increasing difference
- (c) 24; doubling
- (d) 22; random variation

**Answer: (b) 23.**

**Explanation:** Look at the differences between terms: +1, +2, +3, +4, +5. The differences themselves increase by one each time, so the next difference is +6, giving 17 + 6 = 23. That is not linear growth (differences would be constant) and not doubling (each term would be twice the previous). Recognising that a defect trend is accelerating rather than steady changes the architectural conversation entirely: an accelerating integration-defect curve suggests a structural cause - perhaps eroding contract testing or growing coupling - that you should raise as an emerging issue affecting teams across the organisation, one of the explicit behaviours in your architect-for-the-whole-context skill.

#### Question 7 (moderate) - Which conclusion follows?

Facts established at an assurance review: every service that passed its service assessment has an up-to-date threat model. The licensing service has an up-to-date threat model. The grants service does not have an up-to-date threat model.

Which conclusion follows logically?

- (a) The licensing service passed its service assessment.
- (b) The grants service did not pass its service assessment.
- (c) Both (a) and (b).
- (d) Neither (a) nor (b).

**Answer: (b).**

**Explanation:** The rule is "passed implies up-to-date threat model". The grants service lacks an up-to-date threat model, so by contraposition it cannot have passed - conclusion (b) follows. But the licensing service having a threat model does not prove it passed: having a threat model is a necessary consequence of passing, not a sufficient proof of it. Concluding (a) is the classic fallacy of affirming the consequent. In practice this discipline matters when you communicate assurance findings to senior stakeholders: stating only what the evidence supports, and no more, is how you retain credibility when gaining support for architectural topics with high levels of risk and impact.

#### Question 8 (moderate) - Prioritising assurance effort

You have one assurance slot this week and four requests. Your organisation's stated risk appetite prioritises citizen data protection first, then service continuity, then cost. The requests:

- (a) Review a caching change to an internal staff rota tool.
- (b) Review a new third-party data-sharing integration that will transmit citizen case records to an external supplier.
- (c) Review a proposal to renegotiate a hosting contract to save 8% next year.
- (d) Review a minor version upgrade of a logging library in a well-tested pipeline.

Which review should take the slot?

**Answer: (b).**

**Explanation:** Apply the stated priority order mechanically before applying instinct. Option (b) is the only request touching citizen data leaving the organisation's boundary - squarely in the top priority tier, with high impact and high uncertainty. Option (c) is cost, the lowest tier. Options (a) and (d) are low-risk changes with limited blast radius. The trap in questions like this is being drawn to the item that feels most familiar or most technically interesting; the assessment is checking that you can prioritise using the organisation's declared appetite rather than personal preference. That is exactly how you support wider organisational objectives beyond your immediate goals.

#### Question 9 (hard) - Fault diagnosis from partial evidence

A citizen-facing service intermittently returns errors. Evidence gathered so far:

- Errors occur only between 09:00 and 10:00 on weekdays.
- The service calls three downstream APIs: Address Lookup, Payments, and Notifications.
- Address Lookup's dashboard shows a spike in response times from 08:55 to 10:05 on weekdays.
- Payments and Notifications show flat, healthy metrics all day.
- The service's own CPU and memory are stable at all times.
- A batch data-load job in another department runs 09:00-10:00 daily, including weekends.

Which hypothesis best fits all the evidence?

- (a) The service is under-provisioned for morning traffic.
- (b) The weekend-inclusive batch job is the root cause.
- (c) Slow responses from Address Lookup during its morning spike are causing the errors.
- (d) Payments is failing silently.

**Answer: (c).**

**Explanation:** Work by elimination against every piece of evidence. Option (a) is contradicted by stable CPU and memory. Option (b) fails the weekend test: the batch job runs seven days a week, but the errors happen only on weekdays, so the batch job's schedule does not match the symptom's schedule. Option (d) is contradicted by healthy Payments metrics and has no supporting evidence. Option (c) matches the time window almost exactly (08:55-10:05 envelops 09:00-10:00), matches the weekday-only pattern, and identifies a mechanism - downstream latency causing timeouts. Note the discipline: the best hypothesis must fit all the evidence, not just some of it. This is the reasoning you model when leading incident retrospectives across teams and coaching other architects in structured diagnosis.

#### Question 10 (hard) - Logical consistency of a target architecture

A draft target architecture states all four of the following:

1. "Every service must publish events to the central event bus."
2. "Services classified SECRET must not connect to the central event bus."
3. "The vetting service is classified SECRET."
4. "The vetting service is compliant with this target architecture."

Which statement, if removed, would make the remaining set consistent, while keeping the vetting service in scope?

- (a) Statement 1, or amend it to allow classification-based exceptions.
- (b) Statement 3.
- (c) Statement 4.
- (d) The set is already consistent.

**Answer: (a).**

**Explanation:** Follow the chain: statement 3 makes the vetting service SECRET; statement 2 then forbids it from the bus; statement 1 requires it on the bus; statement 4 asserts compliance with both, which is impossible. The set is inconsistent, ruling out (d). Removing statement 3 (b) would misstate a fact about the service rather than fix the architecture. Removing statement 4 (c) restores logical consistency but only by declaring the service non-compliant - it does not give the service any path to compliance, so the architecture remains unsatisfiable for it. The genuinely architectural fix is (a): amend the universal rule to admit principled exceptions. This mirrors real strategy design work: when a principle and a constraint collide, you refine the principle with an explicit exception mechanism rather than pretending the conflict away, and you feed that refinement back into your standards - developing or maintaining strategy in response to findings.

#### Question 11 (hard) - Capacity of a review board

Your Design Authority meets fortnightly and can hear at most 3 substantial reviews per meeting. There are 11 substantial reviews queued, and historically 2 new substantial reviews arrive per fortnight. Under the current arrangement, what happens to the queue over time, and what is the minimum per-meeting capacity needed for the queue to shrink?

- (a) The queue shrinks slowly; capacity is fine.
- (b) The queue grows without bound; capacity must be at least 2 per meeting to shrink it.
- (c) The queue shrinks by 1 per fortnight and clears in 11 meetings; capacity must exceed 2 per meeting to shrink, which it already does.
- (d) The queue is stable at 11; capacity must be 4 to shrink it.

**Answer: (c).**

**Explanation:** Net change per fortnight = arrivals minus capacity = 2 - 3 = -1, so the queue shrinks by one review per meeting cycle. Starting from 11 queued, and with 2 more arriving each cycle, the queue drains at 1 per cycle, taking 11 cycles to reach zero. For any queue to shrink, throughput must exceed arrival rate, so capacity must be strictly greater than 2 per meeting - the current 3 satisfies this. This is queueing logic applied to governance: when you contribute to the development of architectural governance and assurance, one of your quiet superpowers is spotting when a board's structure mathematically guarantees a growing backlog, and fixing the mechanism rather than exhorting people to work faster.

#### Question 12 (hard) - Reasoning about cross-government alignment

Three departments run their own address-lookup services. Facts:

- Departments X and Y use the national address register as their data source; Department Z maintains its own address list.
- A cross-government standard, mandatory for new builds only, requires use of the national address register.
- Department Z is planning a full rebuild of its service next year.
- Departments X and Y have no rebuild plans.

Which statement is best supported?

- (a) Department Z is currently in breach of the standard.
- (b) Department Z's planned rebuild will bring it into the standard's mandatory scope.
- (c) Departments X and Y are required by the standard to stay on the national register.
- (d) All three departments must converge on one shared service.

**Answer: (b).**

**Explanation:** The standard is mandatory for new builds only. Z's existing service predates that trigger, so (a) overstates - legacy systems are not in breach of a new-builds-only mandate. X and Y comply in practice, but the standard as described imposes nothing on existing services, so "required to stay" (c) is not supported. Nothing in the facts mandates convergence to a single shared service (d) - alignment of data sources is not the same as consolidation of services. Option (b) follows directly: a full rebuild is a new build, which brings Z into mandatory scope. Exploring the benefits of cross-government alignment, as your role requires, depends on exactly this precision about what standards do and do not mandate - overclaiming a mandate is one of the fastest ways to lose stakeholder trust.

#### Question 13 (hard) - Combined deduction under constraints

You must assign three architects - Priya, Sam, and Wen - to three workstreams: identity, payments, and data platform. Constraints:

- Priya cannot work on payments due to a prior supplier relationship (conflict of interest).
- Sam has asked to develop identity experience, and you have committed to one development request this quarter.
- Wen is the only one with current data platform accreditation, which the data platform workstream requires.

Which assignment satisfies all constraints?

- (a) Priya: identity; Sam: payments; Wen: data platform
- (b) Priya: data platform; Sam: identity; Wen: payments
- (c) Priya: identity; Sam: data platform; Wen: payments
- (d) Priya: payments; Sam: identity; Wen: data platform

**Answer: (a) - the only assignment that satisfies all the hard constraints, though it cannot honour Sam's development request.**

**Explanation:** Work from the hardest constraint. Wen must take data platform (accreditation), eliminating (b) and (c), which put Wen on payments. Between (a) and (d): (d) puts Priya on payments, violating her conflict of interest. That leaves (a): Priya on identity, Sam on payments, Wen on data platform - all hard constraints satisfied. Sam's development request is a soft preference, not a stated hard constraint, and with Wen locked to data platform and Priya barred from payments, no valid assignment can give Sam identity. The right leadership move, having deduced this, is to explain the constraint logic to Sam transparently and find another development route - mentoring within teams means being honest when the puzzle genuinely has only one solution. Assessments at your level often include one soft criterion precisely to see whether you can distinguish binding constraints from preferences.

### Preparation tips

A brief word of encouragement before the checklist: cognitive assessments reward exactly the habits you have spent your career building. You already decompose ambiguous problems, trace consequences across systems, and challenge inconsistent evidence in design reviews. Preparation for this assessment is therefore less about learning new tricks and more about doing familiar thinking under a clock, in a slightly artificial format. A few hours of deliberate practice - ideally spread across several days rather than crammed the night before - is usually enough to make the format feel routine, which frees your working memory for the reasoning itself.

- **Practise with your own artefacts.** Take two real ADRs from your organisation and deliberately hunt for tensions between them. Sketch a dependency graph from memory for a service you assure, then verify it. The test items are abstractions of this daily work, so the daily work is the best rehearsal.
- **Verbalise your deductions.** As a lead, you already explain reasoning to others; use that habit in the test. Silently naming the rule you are applying ("passed implies threat model; no threat model implies not passed") slows you down by seconds and protects you from classic fallacies.
- **Check every option against every fact.** The hard questions are engineered so that three options fit most of the evidence and one fits all of it. Eliminate systematically rather than pattern-matching to the first plausible answer.
- **Manage the clock like a portfolio.** Allocate rough time per question, bank the easy ones early, and be willing to flag and return. Speed-versus-accuracy reporting means an unanswered hard question costs less than three rushed easy ones answered wrongly.
- **Rest and set up properly.** Do the test somewhere quiet, on a reliable connection, with any permitted rough paper ready. Treat it with the same operational seriousness you would give a go-live.

### Common pitfalls

- **Stopping at first-order effects.** Tracing only direct dependencies or direct consequences when the question rewards second- and third-order reasoning across teams and domains.
- **Affirming the consequent.** Concluding "it passed" because a necessary condition of passing is present. Assessment writers love this fallacy; so do weak assurance reports.
- **Bringing outside knowledge into closed-world questions.** When a question defines a small world of facts, reason only inside it - just as you would when auditing a document trail.
- **Time-sink questions.** Spending five minutes on one intricate deduction while easier marks expire. Skip, flag, return.
- **Assuming later documents supersede earlier ones.** Recency is not authority - in test questions or in governance.
- **Confusing preferences with constraints.** Treating a stakeholder request as binding, or a binding rule as negotiable. Read the wording that signals which is which: "must" and "requires" versus "has asked" and "would prefer".

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment evaluates your ability to analyse, interpret, and make sound decisions using numerical data. It mimics the data-handling demands of your actual role, focusing on practical business arithmetic - percentages, ratios, cost comparisons, capacity figures - rather than abstract formulae. The inputs look like the tables and dashboards you already see: hosting cost breakdowns, options appraisals, service performance metrics, capacity plans, and programme budgets.

Most versions are strictly timed, often less than 90 seconds per question, and most allow or provide an onscreen calculator - the test prioritises interpretation over mental arithmetic. The skill being measured is not whether you can multiply; it is whether you can extract the right figures from a realistic dataset, apply the right operation, and sanity-check the result before committing to a decision.

For a lead technical architect, numbers are the currency of credibility. When you justify a design decision to a spend control board, challenge a supplier's capacity claim, or argue that a strategy will pay for itself over three years, your reasoning must survive scrutiny by finance colleagues and senior leaders. This assessment tests the numerical backbone of that reasoning: total cost of ownership comparisons, growth projections, utilisation and headroom calculations, error-rate analysis, and reading trends without being fooled by scale qualifiers or misleading baselines.

### What it measures for your role

Mapping the assessment dimensions to the skills in your role profile:

- **Making architectural decisions**: cost-benefit and total-cost-of-ownership questions test whether you can weigh options with medium risk and complexity using defensible arithmetic, and manage technical risk at the appropriate level - a wrong percentage in an options appraisal is an architectural risk.
- **Strategy design**: multi-year projection questions (compounding growth, cumulative savings, break-even points) test whether the roadmaps and plans you create to direct a strategy's implementation are numerically sound.
- **Architect for the whole context**: questions about trends across teams and services - defect rates, spend trajectories, shared platform utilisation - test whether you can track emerging issues over time from quantitative signals.
- **Technical design throughout the life cycle**: capacity, throughput, and availability calculations test the sizing judgements inside technical designs characterised by high risk, impact, and complexity.
- **Architecture communication**: several explanations here model how to narrate arithmetic clearly, because gaining support from business stakeholders for high-impact topics often comes down to walking non-specialists through the numbers without error or condescension.

### Practice questions

An onscreen calculator is assumed. Show yourself the working before checking each explanation - the arithmetic is written out in full.

#### Question 1 (easy) - Percentage change in hosting spend

Your programme's monthly cloud hosting bill was £84,000 in January and £96,600 in April. What is the percentage increase?

- (a) 12%
- (b) 15%
- (c) 12.6%
- (d) 18%

**Answer: (b) 15%.**

**Explanation:** Increase = £96,600 - £84,000 = £12,600. Percentage increase = 12,600 ÷ 84,000 = 0.15 = 15%. The classic error is dividing by the new value: 12,600 ÷ 96,600 ≈ 13.0%, which is closest to (c)'s distractor territory. Always divide the change by the original (baseline) value. In real spend reviews, using the wrong baseline understates growth - exactly the kind of error you should catch when assuring another team's business case.

#### Question 2 (easy) - Reading a utilisation table

Four services share a platform. Their allocated and used compute capacity (in vCPUs) is:

| Service | Allocated | Used |
|---|---|---|
| Identity | 120 | 96 |
| Payments | 200 | 170 |
| Casework | 80 | 28 |
| Notifications | 100 | 76 |

Which service has the lowest utilisation rate, and what is that rate?

- (a) Casework, 35%
- (b) Casework, 28%
- (c) Identity, 80%
- (d) Notifications, 76%

**Answer: (a) Casework, 35%.**

**Explanation:** Utilisation = used ÷ allocated. Identity: 96 ÷ 120 = 80%. Payments: 170 ÷ 200 = 85%. Casework: 28 ÷ 80 = 35%. Notifications: 76 ÷ 100 = 76%. Casework is lowest at 35%. Distractor (b) reads the raw used figure (28) as a percentage - a units error the table's layout invites. Spotting chronic under-utilisation like Casework's is how architects find consolidation savings across an organisation; spotting near-saturation like Payments' 85% is how you find the next capacity risk.

#### Question 3 (easy) - Ratio of change requests

Across your governance board's last quarter, change requests were approved, approved-with-conditions, or rejected in the ratio 5:3:1. The board handled 108 requests. How many were approved with conditions?

- (a) 12
- (b) 36
- (c) 60
- (d) 33

**Answer: (b) 36.**

**Explanation:** Total ratio parts = 5 + 3 + 1 = 9. Each part = 108 ÷ 9 = 12 requests. Approved-with-conditions = 3 parts = 3 × 12 = 36. (Cross-check: approved = 60, rejected = 12; 60 + 36 + 12 = 108.) Ratios crop up constantly in governance reporting; converting them back to absolute numbers before drawing conclusions - is 12 rejections a lot? out of how many? - is a habit worth modelling for the architects you lead.

#### Question 4 (moderate) - Total cost of ownership comparison

Two options for a case-management capability over 4 years:

- Option A (commercial product): £250,000 one-off implementation, plus licence and support of £180,000 per year.
- Option B (build on shared platform): £520,000 one-off build, plus running and maintenance of £95,000 per year.

Which option is cheaper over 4 years, and by how much?

- (a) Option A, by £70,000
- (b) Option B, by £70,000
- (c) Option B, by £90,000
- (d) Option A, by £25,000

**Answer: (c) Option B, by £90,000.**

**Explanation:** Option A: 250,000 + (4 × 180,000) = 250,000 + 720,000 = £970,000. Option B: 520,000 + (4 × 95,000) = 520,000 + 380,000 = £880,000. Difference = 970,000 - 880,000 = £90,000 in favour of Option B. Note how the answer flips with the time horizon: over 2 years, A costs £610,000 and B costs £710,000, so A wins. Whenever a supplier or a team shows you a cost comparison, your first assurance question should be "over what period?" - the horizon is often chosen to flatter a preferred option.

#### Question 5 (moderate) - Compound growth in API traffic

A cross-government API you steward handles 2.0 million requests per month and traffic is growing at 20% per month, compounding. The current platform configuration can sustain 4.0 million requests per month. In how many whole months will traffic first exceed capacity?

- (a) 3
- (b) 4
- (c) 5
- (d) 10

**Answer: (b) 4.**

**Explanation:** Compound month by month: after 1 month, 2.0 × 1.2 = 2.40m. After 2: 2.40 × 1.2 = 2.88m. After 3: 2.88 × 1.2 = 3.456m. After 4: 3.456 × 1.2 = 4.147m - above 4.0m for the first time. Distractor (c) comes from the linear shortcut "20% of 2m is 0.4m per month, so (4 - 2) ÷ 0.4 = 5 months"; compounding beats linear growth, so saturation arrives earlier. Distractor (d) misreads 20% as 10%. When you direct roadmaps, the difference between linear and compound assumptions determines whether the capacity work lands a quarter too late.

#### Question 6 (moderate) - Availability arithmetic

A citizen journey passes through three services in series. Over the last quarter each achieved: Service 1: 99.9% availability; Service 2: 99.5%; Service 3: 99.8%. Assuming failures are independent, what is the approximate end-to-end availability of the journey?

- (a) 99.9%
- (b) 99.5%
- (c) 99.2%
- (d) 99.73% (the average)

**Answer: (c) 99.2%.**

**Explanation:** Series availability multiplies: 0.999 × 0.995 × 0.998. Step by step: 0.999 × 0.995 = 0.994005. Then 0.994005 × 0.998 = 0.992017, i.e. about 99.2%. Distractor (d) - averaging - is the error you will most often see in real reports, and it always overstates a serial chain's reliability. Distractor (b) takes only the weakest link, ignoring that the other services also fail sometimes. This calculation is the quantitative heart of a very common lead-architect conversation: explaining to a service owner why their journey misses its availability target even though every individual team met theirs.

#### Question 7 (moderate) - Budget allocation across a strategy

Your technology strategy allocates a £2.4 million annual budget as follows: 45% to legacy remediation, 30% to shared platform development, 15% to innovation pilots, and the remainder to architecture community development (training, events, communities of practice). How much goes to community development, and how much to legacy remediation?

- (a) £240,000 and £1,080,000
- (b) £360,000 and £1,080,000
- (c) £240,000 and £1,200,000
- (d) £100,000 and £1,080,000

**Answer: (a) £240,000 and £1,080,000.**

**Explanation:** The remainder percentage = 100 - 45 - 30 - 15 = 10%. Community development = 0.10 × 2,400,000 = £240,000. Legacy remediation = 0.45 × 2,400,000 = £1,080,000. (Check: 30% = £720,000, 15% = £360,000; 1,080,000 + 720,000 + 360,000 + 240,000 = £2,400,000.) Distractor (b) confuses the 15% line with the remainder. Reading "the remainder" correctly is a small skill with large consequences: budget lines defined by subtraction are where allocation errors hide in real business cases.

#### Question 8 (moderate) - Defect rates across teams

Two delivery teams you assure report last quarter's figures:

| Team | Changes released | Changes causing incidents |
|---|---|---|
| Team Falcon | 240 | 18 |
| Team Heron | 60 | 6 |

A programme board paper states: "Team Falcon caused three times as many incidents as Team Heron and is therefore the riskier team." Is the conclusion sound?

- (a) Yes - 18 is three times 6.
- (b) No - Falcon's incident rate (7.5%) is lower than Heron's (10%), so per change released, Heron is riskier.
- (c) No - the teams cannot be compared at all.
- (d) Yes - but only if Falcon releases more next quarter.

**Answer: (b).**

**Explanation:** Falcon's rate = 18 ÷ 240 = 0.075 = 7.5%. Heron's rate = 6 ÷ 60 = 0.10 = 10%. Falcon releases four times as many changes and causes proportionally fewer incidents per change. The paper compares absolute counts across very different denominators - one of the most common statistical errors in governance reporting. Option (c) overcorrects: the teams can be compared, just on rates rather than counts. As a lead architect assuring services, part of your job is to challenge exactly this kind of misleading aggregate before a board acts on it; a team punished for shipping more is a team that will learn to ship less.

#### Question 9 (hard) - Break-even on a strategic investment

Your strategy proposes investing £900,000 in a shared integration platform. Once live, it saves each service that onboards an estimated £30,000 per year in duplicated integration costs. Onboarding follows the roadmap: 6 services in year 1, a further 10 in year 2, and a further 8 in year 3. Services save from the start of the year after they onboard. What is the first year in which cumulative savings exceed the initial investment?

- (a) Year 3
- (b) Year 4
- (c) Year 5
- (d) Year 2

**Answer: (b) Year 4.**

**Explanation:** Savings lag onboarding by a year. Year 2 savings: the 6 year-1 services save 6 × 30,000 = £180,000 (cumulative £180,000). Year 3: 16 services (6 + 10) save 16 × 30,000 = £480,000 (cumulative £660,000). Year 4: all 24 services save 24 × 30,000 = £720,000 (cumulative £1,380,000) - the first cumulative figure above £900,000. Distractor (a) forgets the one-year lag; distractor (d) forgets that savings accumulate over years rather than arriving at once. Multi-stage cumulative arithmetic like this underpins credible roadmaps: when you direct the implementation of a strategy, the board will remember the break-even year you promised.

#### Question 10 (hard) - Weighted scoring in an options appraisal

Your Design Authority scores three hosting options against weighted criteria (scores out of 10):

| Criterion | Weight | Option X | Option Y | Option Z |
|---|---|---|---|---|
| Security | 40% | 8 | 9 | 6 |
| Cost | 30% | 6 | 4 | 9 |
| Alignment with strategy | 30% | 7 | 8 | 5 |

Which option wins on weighted score, and what is its score?

- (a) Option X, 7.1
- (b) Option Y, 7.2
- (c) Option Z, 6.6
- (d) Option Y, 7.0

**Answer: (a) Option X, 7.1.**

**Explanation:** Option X: (0.4 × 8) + (0.3 × 6) + (0.3 × 7) = 3.2 + 1.8 + 2.1 = 7.1. Option Y: (0.4 × 9) + (0.3 × 4) + (0.3 × 8) = 3.6 + 1.2 + 2.4 = 7.0. Option Z: (0.4 × 6) + (0.3 × 9) + (0.3 × 5) = 2.4 + 2.7 + 1.5 = 6.6. Option X wins narrowly at 7.1. Notice that Y wins the most important single criterion yet loses overall because of its weak cost score - and that a small change in weights would flip the result (with security at 50% and the others at 25% each, Y beats X 7.5 to 7.25). Weighted scoring is only as objective as its weights; a mature architectural governance contribution is stress-testing the weights, not just checking the multiplication.

#### Question 11 (hard) - Interpreting a performance dashboard with scale qualifiers

A performance report says: "Monthly transactions rose from 1.2m to 1.5m over the year. Monthly cost rose from £180k to £210k over the same period." A colleague concludes costs are rising faster than demand. Check the claim: what happened to cost per transaction?

- (a) It rose from 15p to 14p - the claim is right.
- (b) It fell from 15p to 14p - the claim is wrong; unit cost improved.
- (c) It stayed flat at 15p.
- (d) It cannot be calculated from these figures.

**Answer: (b).**

**Explanation:** Start-of-year unit cost = £180,000 ÷ 1,200,000 = £0.15 = 15p. End-of-year unit cost = £210,000 ÷ 1,500,000 = £0.14 = 14p. Transactions grew 25% (1.2m to 1.5m) while cost grew about 16.7% (180 to 210), so unit economics improved: the claim is wrong. Note the scale qualifiers: mixing "m" (millions) and "k" (thousands) correctly is exactly where dashboard misreadings happen, and where distractor answers are built. Growth in absolute spend alongside falling unit cost is a healthy pattern for a scaling service - being able to make that argument in one sentence, with the two percentages, is high-value architecture communication with finance stakeholders.

#### Question 12 (hard) - Capacity headroom with seasonal peaks

A service you assure averages 300 requests per second (rps) but its annual peak - the first working day after a policy deadline - reaches 5.5 times the average. The platform currently sustains 1,500 rps. The team proposes autoscaling that raises sustained capacity by 40%. Will the proposal cover the peak, and what is the shortfall or surplus in rps?

- (a) Yes, with 450 rps to spare
- (b) No, short by 150 rps
- (c) No, short by 450 rps
- (d) Yes, exactly at capacity

**Answer: (a) Yes, with 450 rps to spare.**

**Explanation:** Work in two clean steps. Peak demand = 300 × 5.5 = 1,650 rps. Proposed capacity = 1,500 × 1.40 = 2,100 rps (that is, 1,500 plus 40% of 1,500, which is 600). Surplus = 2,100 - 1,650 = 450 rps, so the proposal covers the peak with headroom. The distractors are built from predictable slips: (b) comes from applying the 40% uplift to the average traffic instead of to the platform's capacity (300 × 1.4 = 420, which invites a muddled subtraction), and (c) comes from comparing the peak against the unimproved 1,500 rps and then mislabelling the direction of the gap. When your first pass lands on an answer that is not offered, or two readings of the question give different results, redo the arithmetic slowly rather than trusting momentum. Peak-to-average ratios are the standard way to reason about deadline-driven government services, where a year of quiet traffic says nothing about the one morning that matters - and where a lead architect is expected to ask "sized for the average or sized for the deadline?" before approving any capacity design.

#### Question 13 (hard) - Combining error rates across a pipeline

A data pipeline you are redesigning has two sequential validation stages. Stage 1 wrongly rejects 2% of valid records. Stage 2 wrongly rejects a further 3% of the valid records that reach it. Out of 200,000 valid records entering the pipeline, approximately how many are wrongly rejected in total?

- (a) 10,000
- (b) 9,880
- (c) 5,880
- (d) 4,000

**Answer: (b) 9,880.**

**Explanation:** Stage 1 wrongly rejects 2% of 200,000 = 4,000 records; 196,000 valid records proceed. Stage 2 wrongly rejects 3% of 196,000 = 5,880. Total wrongly rejected = 4,000 + 5,880 = 9,880. Distractor (a) adds the percentages first (5% of 200,000 = 10,000), ignoring that stage 2 only sees the survivors of stage 1; the error is small here but grows with the rates. Distractor (c) counts only stage 2, (d) only stage 1. Sequential filters, retries, and fallbacks all compose this way, and the difference between "add the rates" and "compose the rates" is exactly the kind of subtle numerical point a lead architect is expected to get right when signing off a high-impact technical design.

#### Question 14 (moderate) - Licence consolidation savings

Three teams independently hold licences for similar API management tools: Team A pays £42,000 per year, Team B pays £35,000, and Team C pays £28,000. A consolidated enterprise agreement covering all three teams' needs would cost £78,000 per year, plus a one-off migration cost of £36,000 shared across the teams. In the first year, does consolidation save money, and what is the position by the end of year two?

- (a) Year 1: £9,000 worse off; Year 2 cumulative: £18,000 better off
- (b) Year 1: £27,000 better off; Year 2 cumulative: £54,000 better off
- (c) Year 1: £9,000 worse off; Year 2 cumulative: £9,000 worse off
- (d) Year 1: £27,000 worse off; Year 2 cumulative: break even

**Answer: (a).**

**Explanation:** Current combined annual cost = 42,000 + 35,000 + 28,000 = £105,000. Consolidated annual cost = £78,000, an annual saving of £27,000. Year 1 position = 27,000 saved - 36,000 migration = £9,000 worse off. Year 2 adds another £27,000 of savings with no further migration cost: cumulative position = -9,000 + 27,000 = £18,000 better off. Distractor (b) ignores the migration cost entirely; (c) forgets that savings recur; (d) double-counts the migration. This shape - short-term cost for recurring saving - is the financial core of most cross-government alignment arguments you will make, and boards will expect you to state both the payback period and the steady-state saving without hesitation.

#### Question 15 (hard) - Proportional allocation of a shared platform's costs

A shared platform costs £600,000 per year to run and serves four services. Cost is recovered in proportion to each service's share of total requests. Annual request volumes are: identity 45 million, payments 30 million, casework 15 million, and notifications 60 million. What should the casework service pay, and what percentage of the total cost does the largest consumer bear?

- (a) £60,000; 40%
- (b) £150,000; 30%
- (c) £60,000; 45%
- (d) £90,000; 40%

**Answer: (a) £60,000; 40%.**

**Explanation:** Total volume = 45 + 30 + 15 + 60 = 150 million requests. Casework's share = 15 ÷ 150 = 10%, so casework pays 0.10 × 600,000 = £60,000. The largest consumer is notifications with 60 ÷ 150 = 40%, bearing 0.40 × 600,000 = £240,000. Distractor (c) confuses identity's volume (45m) with a percentage; (d) inflates casework's share by misreading the volume column. Cost-recovery models are where shared-platform strategies live or die: services will scrutinise their allocation line by line, and the architect who can rebuild the whole table from first principles in a meeting - total, share, multiply - is the one who keeps stakeholder support for the platform. It is also worth noticing what the model incentivises: charging purely by volume can discourage adoption by high-volume services, which is a strategic conversation, not an arithmetic one, but it starts from arithmetic everyone trusts.

### Preparation tips

- **Rehearse with real spreadsheets.** Take a genuine hosting bill, options appraisal, or capacity report from your work and ask yourself test-style questions: what is the percentage change, the unit cost, the break-even year? Familiar data lowers the cognitive load of the unfamiliar format.
- **Write the operation before the numbers.** Decide "change ÷ baseline" or "multiply availabilities" first, then plug in figures. Most wrong answers come from a correct calculation of the wrong quantity.
- **Master the five recurring patterns.** Percentage change from a baseline, weighted averages, compound growth, cost over a time horizon, and rate-versus-count comparisons cover the large majority of items at this level. Practise each until it is automatic.
- **Use the calculator for arithmetic, your head for sense-checking.** After each answer, ask whether the magnitude is plausible: a unit cost of £140 per transaction for a high-volume service should trigger an immediate re-check of scale qualifiers.
- **Bank easy marks first.** The test rewards accuracy across many questions more than heroics on one. If a multi-stage question is consuming your time budget, flag it and move on - you can return with a clear head.
- **Pace with a watch, not a feeling.** Under time pressure, people systematically underestimate how long a question has taken. Glance at the timer every three or four questions and adjust.

### Common pitfalls

- **Misreading chart and table labels.** Confusing monthly with annual data, or missing scale qualifiers like "in thousands" or "in millions" - the single most common cause of wrong answers on realistic datasets.
- **Wrong baseline for percentage change.** Dividing the change by the new value instead of the original, which understates increases and overstates decreases.
- **Averaging what should be multiplied.** End-to-end availability, compound growth, and sequential error rates all compose multiplicatively; taking the mean produces a flattering but false figure.
- **Comparing counts across different denominators.** "Team Falcon caused more incidents" means little until you normalise by volume.
- **Over-calculating.** Performing precise multi-decimal computations when estimation and rounding would identify the answer faster - options are usually spaced widely enough for a rounded calculation to discriminate.
- **Time-sink questions.** Getting anchored on one intricate multi-stage problem while several one-step questions go unanswered. At your level the discipline of triage should feel familiar: it is portfolio prioritisation on a five-second scale.
- **Trusting a flattering horizon.** Accepting a cost comparison, break-even claim, or savings projection without asking over what period it was calculated and what assumptions it carries. In tests this loses a mark; in options appraisals it loses millions. Make "over what period, on what assumptions?" your reflex first question for any headline figure - your own included.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment evaluates how well you understand, analyse, and draw correct conclusions from written material of the kind your role actually demands. The passages mirror your real reading load: technology standards, assurance reports, supplier correspondence, strategy papers, governance terms of reference, and policy excerpts. The questions then test whether you can extract exactly what the text says - no more, no less.

The dominant format is True / False / Cannot Say. "True" means the statement follows from the passage alone; "False" means the passage contradicts it; "Cannot Say" means the passage provides insufficient information either way. The discipline is strict: you must answer based only on the text provided, setting aside your own expert knowledge, however relevant it feels. Multiple-choice comprehension items - identifying the best summary, the author's main concern, or the precise scope of a rule - usually appear alongside.

Timing is tight, often under a minute per question, simulating the reality of absorbing a forty-page assurance pack the evening before a board. For a lead technical architect this assessment matters doubly. First, your decisions frequently hinge on the exact wording of standards and contracts - "must" versus "should", "services" versus "new services", "may" versus "will". Second, your communication duties mean you are often the person translating dense text for others; misreading it propagates your error across whole teams.

### What it measures for your role

- **Architecture communication**: comprehension items test the precision that lets you communicate with technical and non-technical stakeholders at all levels without distorting the source material, and to mediate difficult discussions where each side is quoting the same document differently.
- **Making architectural decisions**: True/False/Cannot Say items test whether you can determine exactly what a standard mandates, permits, or is silent about - the foundation of using architectural governance to make design decisions and manage technical risks at the appropriate level.
- **Architect for the whole context**: passages about cross-organisational policy test your ability to track external issues - new standards, changed guidance - and work out precisely what they mean for teams across the organisation.
- **Strategy design**: summary-selection items test whether you can identify the core intent of a strategy document, a prerequisite for defining strategies and visions that others will implement faithfully.
- **Technical design throughout the life cycle**: detail questions on design documentation test the close reading you need to lead and guide others in creating technical designs, and to give feedback that reflects what a document actually says.

### Practice questions

Read each passage carefully, then answer strictly from the text. Explanations point back to the exact wording.

#### Passage A - Technology standards policy excerpt

"All new digital services must complete a technical architecture review before entering public beta. Services already in public beta at the time this policy takes effect are exempt from this requirement, but must complete a review before entering live. The review board will publish its findings within ten working days of the review meeting. Where a service fails its review, the service may proceed to the next phase only with written approval from the Chief Technology Officer. Reviews are conducted against the current published version of the department's architecture principles."

#### Question 1 (easy)

True, False, or Cannot Say: "A new digital service must complete a technical architecture review before entering public beta."

**Answer: True.**

**Explanation:** This is a near-verbatim restatement of the first sentence: "All new digital services must complete a technical architecture review before entering public beta." When a statement tracks the passage word for word, resist the urge to hunt for a trick - some items simply verify careful reading.

#### Question 2 (easy)

True, False, or Cannot Say: "A service that was already in public beta when the policy took effect never needs a technical architecture review."

**Answer: False.**

**Explanation:** The passage says such services "are exempt from this requirement, but must complete a review before entering live." The exemption applies only to the pre-beta review; the word "but" introduces a surviving obligation. "Never needs a review" directly contradicts "must complete a review before entering live."

#### Question 3 (moderate)

True, False, or Cannot Say: "The Chief Technology Officer chairs the review board."

**Answer: Cannot Say.**

**Explanation:** The passage assigns the CTO one specific power - giving written approval when a service fails its review - and says nothing about who chairs the board. Chairing might seem plausible given the CTO's approval role, but plausibility is not text. This is the classic Cannot Say trap for senior professionals: your real-world experience of how boards are usually chaired supplies an answer the passage never gives.

#### Question 4 (moderate)

True, False, or Cannot Say: "A service that fails its review cannot proceed to the next phase."

**Answer: False.**

**Explanation:** The passage explicitly provides a route: a failed service "may proceed to the next phase only with written approval from the Chief Technology Officer." So proceeding is possible, though conditional. The statement's absolute "cannot" contradicts the conditional "may... only with". Reading conditional permissions accurately - what is barred, what is allowed with conditions - is the daily bread of architectural governance.

#### Question 5 (moderate)

True, False, or Cannot Say: "Review findings are published within ten working days of the service entering its next phase."

**Answer: False.**

**Explanation:** The passage anchors the ten working days to "the review meeting", not to any phase transition: "The review board will publish its findings within ten working days of the review meeting." The statement swaps the anchor event, which changes the obligation materially. Deadline anchors - "of the meeting", "of receipt", "of go-live" - are precisely where contracts and standards bite, and assessments test whether you notice them.

#### Passage B - Supplier email

"Dear architecture team, further to our meeting, I can confirm that the upgraded platform will support single sign-on integration from release 4.2, scheduled for March. Our roadmap also includes native audit logging, which we expect to ship in the release after 4.2, subject to prioritisation. Please note that customers on the standard support tier receive upgrades within three months of general availability, while premium tier customers receive them within two weeks. As discussed, your current contract is on the standard tier. We would be happy to discuss tier options at the quarterly review."

#### Question 6 (easy)

True, False, or Cannot Say: "The supplier has committed to shipping native audit logging in the release after 4.2."

**Answer: False.**

**Explanation:** The email hedges twice: the roadmap "includes" the feature, which the supplier "expect[s] to ship in the release after 4.2, subject to prioritisation." An expectation subject to prioritisation is not a commitment; the statement's word "committed" overstates the text. Distinguishing supplier commitments from supplier intentions is a core assurance skill - many a programme risk register has been undone by reading "we expect" as "we will."

#### Question 7 (moderate)

True, False, or Cannot Say: "If the organisation stays on its current support tier, it could receive release 4.2 as late as June."

**Answer: True.**

**Explanation:** Chain the facts: release 4.2 is "scheduled for March"; the organisation is "on the standard tier"; standard tier customers "receive upgrades within three months of general availability." March plus up to three months allows delivery as late as June. The statement says "could receive... as late as", which matches the within-three-months window. Note what would make this Cannot Say: if the statement asserted the organisation *will* receive it in June, the passage could not confirm that - "within three months" includes earlier delivery.

#### Question 8 (hard)

True, False, or Cannot Say: "Single sign-on integration is not available in any release before 4.2."

**Answer: Cannot Say.**

**Explanation:** The email says the upgraded platform "will support single sign-on integration from release 4.2." The word "from" tells you availability starting at 4.2, and in ordinary commercial usage it implies novelty - but the email never explicitly states that earlier releases lack the capability, and "will support... from" could describe a contractual support position rather than a technical first appearance. Strictly from the text, earlier availability is neither confirmed nor denied. This is a deliberately fine judgement: when an assessment item turns on an implication rather than a statement, the strict reading wins. In real supplier management you would resolve the ambiguity by asking, not by assuming - which is exactly the behaviour the strict reading trains.

#### Passage C - Assurance report extract

"The service assessment panel found that the team has a credible plan for scaling the service, supported by load testing at twice the forecast peak. However, the panel was not shown evidence that the disaster recovery plan has been exercised. The team stated that a recovery exercise took place in the spring, but the report of that exercise could not be located during the assessment. The panel recommends that the service proceed to live, conditional on the recovery exercise report being provided to the panel chair within twenty working days. If the report cannot be provided, a fresh recovery exercise must be conducted and observed by a member of the assurance team."

#### Question 9 (easy)

True, False, or Cannot Say: "The panel recommended that the service proceed to live unconditionally."

**Answer: False.**

**Explanation:** The recommendation is explicitly "conditional on the recovery exercise report being provided to the panel chair within twenty working days." The word "unconditionally" contradicts "conditional on". One-word differences of this kind carry whole governance regimes.

#### Question 10 (moderate)

True, False, or Cannot Say: "A disaster recovery exercise took place in the spring."

**Answer: Cannot Say.**

**Explanation:** The passage reports only that "the team stated that a recovery exercise took place in the spring" and that the report "could not be located". A reported claim is evidence that the claim was made, not that it is true - and the panel itself "was not shown evidence". The passage neither confirms the exercise happened nor denies it. Assessments at senior level lean heavily on this distinction between what a document asserts and what it merely attributes to someone; so does chairing any contested design review.

#### Question 11 (moderate)

True, False, or Cannot Say: "If the report cannot be provided within twenty working days, the service must be withdrawn from live."

**Answer: False.**

**Explanation:** The passage specifies a different consequence: "If the report cannot be provided, a fresh recovery exercise must be conducted and observed by a member of the assurance team." Withdrawal from live is not mentioned; the statement invents a sanction the text does not contain. Notice how easy it is to accept an invented consequence that feels proportionate - your sense of what a panel *would* do must not override what this panel *said*.

#### Question 12 (moderate) - Multiple choice

Which statement best summarises the panel's overall position?

- (a) The service is not ready for live because disaster recovery has never been tested.
- (b) The service demonstrated scaling readiness, but must evidence its disaster recovery exercising before the condition on its live recommendation is discharged.
- (c) The service passed all aspects of the assessment.
- (d) The panel could not reach a conclusion.

**Answer: (b).**

**Explanation:** Option (b) captures both findings: the positive ("a credible plan for scaling... supported by load testing at twice the forecast peak") and the gap ("not shown evidence that the disaster recovery plan has been exercised"), plus the conditional recommendation. Option (a) overstates - the exercise may have happened; the evidence is missing. Option (c) ignores the condition. Option (d) is contradicted by the clear recommendation. Summary questions reward the answer that preserves the text's balance; as the person who often writes these summaries for boards, you know that flattening a conditional into a pass or a fail is how assurance findings get distorted.

#### Passage D - Strategy paper excerpt

"Our target architecture reduces the department's twelve case-management systems to three within five years. Consolidation will proceed domain by domain, beginning with the two domains where contracts expire soonest. No system will be decommissioned until its successor has operated at full load for one complete reporting cycle. We anticipate savings of £3.2 million per year once consolidation completes, though these figures assume no significant change in caseload legislation. Departments wishing to join the shared arrangements later may do so, provided they adopt the common data standard in full."

#### Question 13 (moderate)

True, False, or Cannot Say: "The consolidation order is determined by contract expiry dates."

**Answer: Cannot Say.**

**Explanation:** Read the exact scope of the claim. The passage fixes only the starting point: consolidation begins "with the two domains where contracts expire soonest." It does not state the rule for ordering the remaining domains. The statement as written asserts that the whole order is determined by expiry dates - the text supports this for the first two domains only, and is silent about the rest. On the strict reading the full claim is neither confirmed nor contradicted: Cannot Say. If the statement had said "the first domains to consolidate are chosen by contract expiry", it would be True. Assessment items often turn on precisely this difference between a rule stated for a subset and a rule asserted for the whole - as do misreadings of real strategy papers by teams planning their own migration dates.

#### Question 14 (hard)

True, False, or Cannot Say: "The department will save £3.2 million per year from year five."

**Answer: Cannot Say.**

**Explanation:** Three hedges in the passage block this claim. First, savings are anticipated "once consolidation completes", and the target is consolidation "within five years" - completion could come earlier, and the passage does not promise savings begin at year five. Second, "we anticipate" is a forecast, not a commitment. Third, the figures explicitly "assume no significant change in caseload legislation." The statement converts a conditional forecast into a dated certainty; the passage neither confirms nor contradicts what will actually be saved or when. Translating hedged strategy language into what can honestly be promised to a minister or a spending review is a lead architect's regular duty - and the direction of error is almost always the one this question models.

#### Question 15 (hard)

True, False, or Cannot Say: "A department that refuses to adopt part of the common data standard cannot join the shared arrangements later."

**Answer: True.**

**Explanation:** The passage permits later joining "provided they adopt the common data standard in full." The proviso is exhaustive: adoption "in full" is the condition of entry. A department refusing part of the standard has, by definition, not adopted it in full, so the condition fails and the permission does not apply - the text's own rule excludes them. This is True by the passage's logic even though the passage never uses the word "refuse". Conditions expressed as provisos ("provided that...") are logically equivalent to exclusions of their negation; reading them both ways round quickly and correctly is a distinctive senior-level verbal skill, and it is also how you will defend the data standard's integrity when a would-be joiner asks for a partial exemption.

#### Passage E - Governance terms of reference

"The Technical Design Authority (TDA) meets weekly and is quorate when at least four voting members are present, of whom at least one must be from outside the programme under discussion. Decisions are made by consensus where possible; where consensus cannot be reached, the chair holds a casting vote. Decisions on matters classified as high risk require ratification by the Departmental Architecture Board at its next monthly meeting, and take provisional effect in the interim. Any member may request that a decision be escalated to the Departmental Architecture Board; such requests suspend the decision until the Board has considered it, except for decisions the chair designates as urgent, which remain in provisional effect during escalation."

#### Question 16 (moderate)

True, False, or Cannot Say: "A TDA meeting attended by four voting members from the programme under discussion is quorate."

**Answer: False.**

**Explanation:** Quoracy needs "at least four voting members... of whom at least one must be from outside the programme under discussion." Four members all from inside the programme satisfy the count but fail the independence condition, so the meeting is not quorate. Compound conditions - a number plus a composition rule - must be checked clause by clause; the statement is engineered to pass the first clause and fail the second. The independence clause, of course, exists for the same reason your assurance role does: decisions about a programme should not be made solely by that programme.

#### Question 17 (hard)

True, False, or Cannot Say: "A high-risk decision has no effect until the Departmental Architecture Board ratifies it."

**Answer: False.**

**Explanation:** The passage states that high-risk decisions "take provisional effect in the interim" - that is, between the TDA decision and Board ratification. "No effect until ratified" directly contradicts "provisional effect in the interim." The distinction between a decision that is suspended pending ratification and one that is provisionally effective pending ratification is worth real money and real risk in governance design: teams act on provisionally effective decisions. Reading which regime a terms-of-reference document establishes - and drafting the one you actually intend when you contribute to developing governance - turns on exactly this wording.

#### Question 18 (hard)

True, False, or Cannot Say: "If a member escalates a decision that the chair has designated as urgent, the decision is suspended until the Board considers it."

**Answer: False.**

**Explanation:** The escalation rule suspends decisions, "except for decisions the chair designates as urgent, which remain in provisional effect during escalation." The statement describes the general rule while ignoring the exception that the question's facts trigger: the decision at issue is designated urgent, so it remains in provisional effect rather than being suspended. Exception clauses introduced by "except for" reverse the outcome for their subset, and testing a rule against facts that fall inside the exception is a favourite construction of verbal assessments - and of the real disputes you will be asked to mediate when two members of a design authority read the same terms of reference differently.

#### Question 19 (moderate) - Multiple choice

According to the passage, which of the following is the chair of the TDA empowered to do?

- (a) Ratify high-risk decisions on behalf of the Departmental Architecture Board.
- (b) Prevent any member from escalating a decision.
- (c) Cast a deciding vote when consensus fails, and designate decisions as urgent.
- (d) Change the quoracy rules for a given meeting.

**Answer: (c).**

**Explanation:** The chair's two stated powers are the casting vote ("where consensus cannot be reached, the chair holds a casting vote") and urgency designation ("decisions the chair designates as urgent"). Ratification of high-risk decisions belongs to the Departmental Architecture Board, not the chair, ruling out (a). The passage gives "any member" an unqualified right to request escalation - urgency designation changes the effect of escalation, not the right to request it - so (b) overstates. Nothing in the text lets anyone vary quoracy, ruling out (d). Enumerating exactly which powers a document grants to which role, without inflation, is the same close reading you apply when defining or refining governance - and when reassuring a nervous stakeholder about what a design authority can and cannot impose on their team.

### Preparation tips

Before the checklist, a note on mindset. Verbal reasoning at this level is not a vocabulary test; it is a discipline test. Every wrong answer in the questions above comes from one of a small number of moves: importing outside knowledge, upgrading a hedge into a certainty, generalising a subset rule to the whole, missing an exception clause, or accepting an attributed claim as fact. You make none of these moves when you are being careful; the assessment simply checks that your carefulness survives time pressure. It is also worth remembering that the same moves, made in real documents, are how architectural misunderstandings propagate across teams - so this practice pays for itself twice.

- **Read the statement before re-reading the passage.** Identify exactly what would make it True, what would make it False, and hunt for that evidence. Aimless re-reading burns your minute.
- **Underline the operative words.** Must, may, should, only, all, from, within, provided that, subject to. Assessments build wrong answers by swapping these; so do bad contract summaries.
- **Rehearse the Cannot Say discipline.** Your expertise is the biggest hazard here: you know how review boards usually work, what suppliers usually mean, what panels usually do. Practise asking "where in the text?" and refusing any answer that lacks a line to point to - a habit that will also sharpen your assurance write-ups.
- **Watch for attribution.** "The team stated that X" confirms only the statement, never X. Passages about reports, claims, and meeting minutes use this constantly.
- **Practise on your own reading pile.** Take a standard or policy you handled this month and write three True/False/Cannot Say statements about it. Composing items teaches the patterns faster than answering them.
- **Keep calm about fine judgements.** One or two items in any professional-grade verbal test sit near the boundary. Give your best strict reading, answer, and move on - a single ambiguous item decides nothing.

### Common pitfalls

- **Bringing outside knowledge into the passage.** The most common failure for experienced professionals: answering from what is generally true in government rather than what this text says.
- **Confusing "likely" with "certain".** Treating a stated expectation, forecast, or anticipation as an established fact - the exact error in supplier-roadmap and strategy-savings questions.
- **Missing scope words.** Reading "new services" as "services", "the first two domains" as "all domains", or "in full" as "mostly". Scope words are where mandates live.
- **Swapped anchors and baselines.** Deadlines anchored to the wrong event ("of the meeting" versus "of go-live") read as trivial detail and score as wrong answers.
- **Answering the plausible instead of the textual.** Inventing proportionate-sounding consequences or governance arrangements the passage never states.
- **Poor time allocation.** Reading every passage exhaustively before seeing its questions. Skim for structure, read the statement, then target your close reading where the marks are.
- **Second-guessing a strict reading.** Having correctly concluded Cannot Say, talking yourself into True because the statement "must really be what they meant". Once you have checked the exact wording and found the passage silent, trust the method. The test rewards the discipline, and so does every contract negotiation, standards dispute, and assurance finding in which the difference between what a document says and what its author probably intended becomes the whole argument. Senior professionals lose more marks by overriding their own careful reading than by misreading in the first place - a pattern worth remembering the next time a supplier assures you that a clause "obviously" covers your use case.

## Workplace job-specific situational judgement assessment

### About this assessment

A workplace job-specific situational judgement assessment evaluates your decision-making, interpersonal skill, and professional conduct through realistic workplace dilemmas. Unlike logic or numerical tests, there is often no single objectively right answer; instead, some responses fit the role, the organisation's values, and the situation better than others. You will typically be asked to select the most effective and least effective actions from a set, or to rank or rate all the options from best to worst.

Timing is usually generous or absent, because the test measures natural judgement rather than speed. Scenarios are short but layered: they involve competing stakeholder interests, incomplete information, time pressure, and the tension between technically ideal and organisationally achievable outcomes - in other words, an ordinary week for a lead technical architect.

For your role, the scenarios draw on your real stakeholder landscape: delivery teams and their architects, service owners and product managers, senior responsible owners, security and data colleagues, commercial teams and suppliers, other government departments, and central assurance bodies. Strong answers consistently reflect UK public sector values - starting with user needs, working in the open with transparency, collaborating across boundaries, and taking accessibility and inclusion seriously - alongside the leadership behaviours in your role profile: justifying decisions openly, mentoring rather than commanding, mediating rather than escalating by default, and taking ownership of problems that cross team lines.

### What it measures for your role

- **Architecture communication**: scenarios test whether you can mediate between people in difficult architectural discussions, gain support for high-risk topics from business and technical stakeholders, and coach others in communicating - rather than winning arguments by authority.
- **Community collaboration**: scenarios probe how you handle team dynamics - using feedback well, spotting problems in how a group is working through mechanisms like Agile health checks, and stimulating the right responses rather than imposing fixes.
- **Making architectural decisions**: dilemmas test whether you use governance proportionately, address risks that span teams and domains, and distinguish decisions you should make from decisions you should guide others to make.
- **Architect for the whole context**: several scenarios pit your programme's immediate interests against wider organisational objectives, testing whether you act on emerging cross-cutting issues and influence colleagues beyond your own reporting lines.
- **Strategy design**: scenarios test how you respond when reality diverges from your roadmap - whether you update strategy in response to feedback and findings, or defend the plan for its own sake.
- **Technical design throughout the life cycle**: options often distinguish leaders who guide others to produce good designs from experts who quietly redo everyone's work - the mentoring and leadership behaviours your role level explicitly requires.

### Practice questions

For each scenario, decide the most effective and least effective responses before reading the discussion.

#### Question 1 (moderate) - The team that bypassed governance

You discover that a delivery team has selected and begun implementing a new message-queue technology without bringing the decision to the Technical Design Authority, contrary to the agreed governance process. The technology choice itself looks reasonable. The team's architect, whom you mentor, says the TDA queue was six weeks long and the team could not wait.

- (A) Instruct the team to halt work until the decision has been through the TDA properly.
- (B) Retrospectively review the decision with the team's architect, take it to the next TDA as a completed-decision review, and separately raise the six-week queue as a governance problem to fix.
- (C) Let it go - the choice is reasonable, and governance should not obstruct delivery.
- (D) Report the bypass to the programme director as a compliance breach.

**Most effective: (B). Least effective: (D).**

**Explanation:** Option (B) addresses both real problems: the decision gets proper scrutiny without punitive delay, and the root cause - a governance process too slow for delivery reality - is surfaced and owned. This reflects your role's expectation that you contribute to developing governance, not just enforce it, and it treats the architect you mentor as a partner in fixing the system. Option (A) is proportionate only if the decision carried serious risk; halting reasonable work purely to honour process ritual damages the credibility of governance itself. Option (C) is the mirror error: silence teaches every team that governance is optional, and the next bypassed decision may not be reasonable. Option (D) is least effective because it converts a fixable process failure into a blame event, poisons your mentoring relationship, and delegates upwards a problem that sits squarely within your remit. Transparency matters, but transparency means the TDA sees the decision - not that a director sees a culprit.

#### Question 2 (moderate) - Two architects in deadlock

Two architects on different teams have argued for three weeks about whether services in a shared journey should integrate via synchronous APIs or events. The disagreement has turned personal; their teams are now building incompatible assumptions. Both architects are capable, and each has privately asked you to overrule the other.

- (A) Make the decision yourself immediately and instruct both teams to comply.
- (B) Facilitate a structured session: agree the decision criteria first (user needs, coupling, failure modes, operability), have each architect argue the other's position, then drive to a decision with a recorded rationale - taking the decision yourself only if the session fails to produce one.
- (C) Tell them to work it out between themselves within a week or you will decide.
- (D) Split the difference: let each team use its preferred style and add a translation layer between them.

**Most effective: (B). Least effective: (D).**

**Explanation:** Option (B) is textbook architecture communication at lead level: mediating a difficult architectural discussion by moving it from positions to criteria, defusing the personal element (arguing the other's case rebuilds empathy and often reveals that both options are viable), and ensuring the outcome is a justified, communicated decision rather than a victory. It also models a repeatable method both architects can use next time - coaching through practice. Option (A) resolves the technology question but leaves the relationship broken and teaches both architects that deadlock gets escalated rewards. Option (C) is abdication dressed as empowerment: three weeks of failure predicts the fourth, and the deadline mainly adds fear. Option (D) is least effective because it purchases interpersonal peace with permanent architectural debt - an unnecessary translation layer that every future team must operate and understand. Design decisions should resolve conflicts, not embalm them.

#### Question 3 (hard) - The strategy your findings undermine

Eighteen months ago you defined a cloud migration strategy that the department approved and funded. New evidence - two spikes and a supplier announcement - now suggests one of the strategy's central assumptions is wrong, and following the current roadmap will cost significantly more than re-planning. Several senior stakeholders are personally invested in the strategy's success, and you wrote it.

- (A) Present the new evidence to the strategy's governance board promptly, with a candid assessment and a re-planning proposal, explicitly noting what the original strategy got right and what has changed.
- (B) Quietly adjust the roadmap's later phases so the problem never becomes visible, protecting confidence in the strategy.
- (C) Wait for the next annual strategy refresh, six months away, to fold in the new evidence through the normal cycle.
- (D) Ask a trusted peer architect to raise the concerns instead, so the challenge does not come from the strategy's own author.

**Most effective: (A). Least effective: (B).**

**Explanation:** Your role profile is explicit: develop or maintain strategy in response to feedback and findings. Option (A) does precisely that, with the transparency that public sector stewardship of public money demands, and it manages stakeholders like adults - the framing "what has changed" rather than "what was wrong" is accurate (the supplier announcement is genuinely new) and preserves confidence in the strategy process even as it revises the strategy content. Option (B) is least effective: concealing material evidence from a governance board is a serious integrity failure, and quiet roadmap surgery will be discovered by exactly the people whose trust you most need. Option (C) knowingly burns public money for six months to avoid an awkward conversation. Option (D) is subtler but still weak: it treats candour as reputationally dangerous, when an author revising their own strategy on evidence is one of the strongest credibility signals a lead architect can send - and the peer would be presenting evidence they do not fully own.

#### Question 4 (moderate) - The accessibility corner-cut

A delivery team you assure is under severe deadline pressure for a ministerial commitment. The service owner proposes descoping fixes to accessibility defects that affect screen-reader users, arguing they can be patched "shortly after launch" and affect "a small percentage of users." The technical work is not in your direct line, but you sit on the programme's design authority.

- (A) Accept the descoping - the service owner owns scope decisions, and launch dates for ministerial commitments are immovable.
- (B) State clearly at the design authority that launching with known screen-reader failures likely breaches accessibility regulations and excludes the users who often depend on the service most; ask for the defects to be treated as launch-blocking, and offer to help the team find scope elsewhere to protect the date.
- (C) Say nothing at the board but email the team's developers encouraging them to fix the defects anyway.
- (D) Escalate directly to the minister's office that the service will launch in a non-compliant state.

**Most effective: (B). Least effective: (C) - with (D) a close second-worst.**

**Explanation:** Option (B) does everything your role and public sector values require: it names the risk honestly in the right forum, grounds the objection in both legal duty and inclusion (accessibility is a user need, not a nice-to-have, and "small percentage" describes people, many of whom have no alternative channel), and - critically - engages with the delivery constraint by offering to find scope trade-offs elsewhere. Influence at lead level means solving the whole problem, not just voicing the principle. Option (A) mistakes deference for collaboration; assurance exists precisely for this moment. Option (C) is least effective because it is covert: it undermines the service owner, puts developers in an impossible position between their leadership and your quiet lobbying, and abandons the transparent, in-the-open working that gives architectural challenge its legitimacy. Option (D) is a dramatic overreach that skips every intermediate governance layer and destroys the working relationships you need for the next hundred decisions - escalation has its place, but only after the design authority route has actually failed.

#### Question 5 (moderate) - The struggling architect

An architect you lead has produced a technical design for a high-risk integration that is significantly below the standard needed: key failure modes unaddressed, no consideration of data protection requirements. The design review is in three days, and this architect has seemed withdrawn lately in team ceremonies. Your Agile health check for their team also showed declining scores this quarter.

- (A) Rewrite the design yourself tonight so the review goes well, and mention the changes to the architect afterwards.
- (B) Postpone the review, tell the architect the design is not ready, and have a private conversation that covers both the specific design gaps and, separately and supportively, how they are doing - then pair with them on the revision.
- (C) Let the design go to review as-is so the architect gets direct feedback from the panel, then discuss afterwards.
- (D) Raise the declining health-check scores at the team's next retrospective and let the team work out what to do.

**Most effective: (B). Least effective: (A).**

**Explanation:** The scenario braids three of your responsibilities: assuring a high-risk design, mentoring an individual, and acting on team-dynamic signals from health checks. Option (B) addresses all three - the design does not proceed unready (managing the technical risk), the feedback is direct but private (effective, lasting feedback is specific and preserves dignity), the withdrawn behaviour and declining scores are noticed and explored with care rather than diagnosed at a distance, and pairing on the revision converts a failure into a development opportunity. Option (A) is least effective: it ships a better document while teaching the architect nothing, signalling you do not trust them, hiding a capability problem from everyone including them, and setting a precedent that you are the team's overnight safety net - the opposite of providing leadership to other architects. Option (C) uses a public panel to deliver feedback you were unwilling to give privately; for someone already withdrawn, a public mauling risks real harm and the review wastes everyone's time on a known-unready design. Option (D) treats an individual welfare signal as a team process item, which is both ineffective and unkind.

#### Question 6 (hard) - Cross-government alignment versus programme pressure

You learn that another department is building an eligibility-checking capability nearly identical to one your programme is about to build. Joining forces could save both departments substantial money and improve consistency for citizens who interact with both services. However, aligning would delay your programme by an estimated three months, and your senior responsible owner (SRO) is measured on this year's delivery dates.

- (A) Proceed with your programme's own build - cross-government alignment is desirable but not your accountability, and the SRO's dates are.
- (B) Prepare a short, quantified options paper comparing build-alone against align-and-share (costs, delay, long-term savings, citizen impact), discuss it with your SRO first, and take it to the appropriate cross-government forum with your SRO's concerns represented honestly.
- (C) Commit your programme to the shared build in the cross-government forum, then inform the SRO of the new plan.
- (D) Suggest the other department adopt your programme's capability once you have built it, avoiding any delay to you.

**Most effective: (B). Least effective: (C).**

**Explanation:** Your role explicitly includes exploring the benefits of cross-government alignment and supporting wider objectives beyond your immediate goals - but exploring means evidencing and influencing, not unilaterally deciding. Option (B) does the work: it quantifies the trade-off so the decision is made on evidence, respects the SRO's legitimate accountability by engaging them before the wider forum, and puts the citizen benefit - consistency across services people use in sequence - on the table where it belongs. Option (C) is least effective because you have committed resources you do not own; even if the alignment is right, making it this way converts an ally (the SRO) into an opponent and teaches the organisation that architects cannot be trusted with delegated authority. Option (A) simply declines the leadership your role level exists to provide. Option (D) sounds collaborative but quietly optimises for your programme: it asks the other department to absorb all the alignment cost, having had no say in the design - the pattern that makes cross-government reuse offers so easy to refuse.

#### Question 7 (moderate) - The senior stakeholder who wants the shiny thing

A director general has returned from a conference enthusiastic about a specific vendor's AI platform and asks you to "put it in the architecture" for a flagship service. Your assessment is that the platform is immature for your use case, creates a significant lock-in risk, and duplicates capabilities the department already licenses. The DG is influential over your programme's funding.

- (A) Add the platform to the roadmap's later phases so the DG feels heard, expecting it to be quietly descoped later.
- (B) Book time with the DG; start from the outcome they care about, present your assessment plainly - including what the platform does well - propose a bounded evaluation pilot with clear success criteria as the evidence-based route, and record the decision openly.
- (C) Decline the request in writing, copying the CTO, citing the architecture principles the platform would breach.
- (D) Implement the request - senior sponsorship matters more than technical purity, and the architecture can absorb one suboptimal component.

**Most effective: (B). Least effective: (A).**

**Explanation:** Gaining support from business stakeholders on topics with high risk and impact is a named behaviour of your role, and option (B) shows how it is done: engaging with the DG's underlying goal rather than the specific technology, being honest about trade-offs in both directions, and converting enthusiasm into a controlled experiment whose criteria you agree in advance - so the eventual decision, either way, is shared and evidenced. Option (A) is least effective because it is dishonest in slow motion: the DG's expectation compounds while you plan to disappoint them, and when the descoping is noticed - it will be - you lose the trust that makes every future conversation work. Roadmaps are commitments communicated across an organisation, not diplomatic instruments. Option (C) may be technically right but is relationally maladroit as an opening move; leading with written refusal and an escalation copy treats a persuadable stakeholder as an adversary. Option (D) trades a durable architectural liability for temporary comfort and fails the duty of candid advice that justifies your role's existence.

#### Question 8 (moderate) - The health check nobody wants to discuss

Running your quarterly Agile health check across teams, you notice one team's scores for "confidence in technical direction" have dropped sharply, but in the follow-up session the team is quiet and the team's architect insists everything is fine. Two developers approach you privately afterwards: they believe the architect dismisses their concerns about accumulating shortcuts in the service's design, and morale is suffering.

- (A) Take the architect's word for it - the formal session found nothing actionable.
- (B) Tell the architect what the developers said so the three of them can sort it out directly.
- (C) Spend time with the team's work directly - join a design session, review recent decisions and their records - then coach the architect with specific observations about how concerns are being received, and agree how they will rebuild the feedback loop; check the signal again next quarter.
- (D) Move the two developers' concerns into the design authority's formal risk register to force the issue into governance.

**Most effective: (C). Least effective: (B).**

**Explanation:** Your community collaboration skill is explicit: use health checks to identify issues in team dynamics and help stimulate the right responses. Option (C) does this properly - it converts hearsay into first-hand observation (protecting both the architect from unfair judgement and the developers from being dismissed), addresses the real issue (how dissent is heard, not just this quarter's technical shortcuts), and works through coaching, which is how you provide leadership to other architects. The follow-up measurement closes the loop. Option (B) is least effective because it burns the two developers who trusted you with a private concern; identified to a defensive architect, they are exposed to exactly the dismissiveness they reported, and the team learns that speaking up is unsafe - the deepest damage available in this scenario. Option (A) privileges a comfortable formal signal over a credible informal one; quiet sessions after sharp score drops are themselves a finding. Option (D) reaches for governance machinery before leadership conversation, escalating a coaching problem into a compliance problem and likely entrenching the architect's defensiveness.

#### Question 9 (hard) - The incident that implicates your own decision

A significant outage hits a shared platform. The post-incident review reveals a contributing cause: an architectural decision you made a year ago, reasonable on the information available then, interacted badly with a later change no one connected to it. The review meeting is tomorrow; some attendees are already speculating about the cause in a way that points at the operations team.

- (A) At the review, state clearly and early that your design decision was a contributing cause, explain the reasoning at the time and what changed, and propose both the technical fix and a process improvement so future changes are checked against standing design assumptions.
- (B) Let the review run its course - if the analysis reaches your decision, acknowledge it then.
- (C) Before the meeting, brief your line manager privately so they hear it from you first, and ask them how much to disclose at the review.
- (D) Focus the review on the later change that triggered the failure, since your original decision was sound on the evidence available at the time.

**Most effective: (A). Least effective: (D).**

**Explanation:** Option (A) is transparency doing its real work. Naming your own decision's role early stops the room's speculation from settling unfairly on the operations team - a concrete act of leadership protection - and modelling blameless self-examination is the single most powerful way a senior figure shapes an organisation's incident culture. The pairing of technical fix and process improvement (checking changes against recorded design assumptions) turns the incident into feedback that refines your standards, exactly as your life-cycle design skill requires. Option (D) is least effective: it is deflection with a defensible-sounding rationale, and it knowingly lets blame drift toward colleagues. "Sound at the time" is precisely what you say while taking responsibility, not instead of it. Option (B) gambles the operations team's reputation on the review's thoroughness and forfeits the trust dividend of volunteering. Option (C) is not wrong to do as well, but as the main strategy it makes disclosure contingent on managerial comfort - candour in incident reviews should not be negotiable upward.

#### Question 10 (moderate) - Ranking: the supplier's tempting shortcut

A supplier building a critical integration proposes skipping the agreed contract-testing stage to recover two weeks of schedule, noting that their internal tests already cover the interfaces. The service goes live in six weeks. Rank the following responses from most to least effective.

- (A) Decline the proposal and require the contract-testing stage as agreed, explaining that independently verified interfaces are a condition of go-live for a critical integration, and work with the supplier to find schedule recovery elsewhere.
- (B) Accept the proposal but require the supplier to indemnify the department against integration defects.
- (C) Accept the proposal - the supplier knows their system best and the schedule matters.
- (D) Refer the proposal to the programme board without a recommendation.

**Answer - most to least effective: A, D, B, C.**

**Explanation:** (A) leads because it holds the technical risk line while engaging constructively with the supplier's real problem - the schedule - which is how durable commercial-technical relationships work; managing technical risk at the appropriate level sometimes means simply saying no, warmly. (D) is second: escalation to the board is at least transparent and keeps the decision in governance, but it delegates a judgement you are equipped and expected to make, and costs calendar time the schedule cannot spare. (B) ranks third because it mistakes a financial instrument for a technical control: an indemnity compensates the department after citizens have already experienced the failure - the harm a critical government integration must prevent is not primarily financial. (C) is last: it accepts an unverified critical interface on the supplier's self-assessment, surrendering the independent assurance that the testing stage exists to provide. Note the general pattern for ranking items: effectiveness usually tracks how well an option manages the actual risk, preserves transparency, and maintains the relationship - in that order.

### Preparation tips

- **Anchor yourself in the role's centre of gravity.** Before the test, re-read your role profile. At lead level the recurring themes are: work in the open, fix systems rather than blame people, coach rather than rescue, engage stakeholders before deciding for them, and put user needs - including accessibility - above delivery comfort. Options embodying these themes are usually strong.
- **Look for the option that solves the whole problem.** Weak options handle the technical issue but damage a relationship, or preserve harmony but bury a risk. The strongest option typically addresses the immediate issue, the root cause, and the people - as (B)-style answers above repeatedly do.
- **Beware flattering extremes.** Both "decisive" unilateral action and "collaborative" indefinite deferral can feel virtuous. Effectiveness usually lives between them: consult, then decide, then communicate.
- **Read the question stem precisely.** "Most effective" is not "what would you do" and not "what is most principled"; it asks what would actually work in that organisation. Rate each option on outcomes, not intentions.
- **Practise articulating why.** For each practice scenario, say aloud why the weakest option fails. The habit of naming the failure mode - covert, blaming, passive, scope-inflated - makes the patterns easy to spot under test conditions.
- **Be authentic.** These assessments also check fit. Answering as the leader you genuinely are, informed by the values above, produces more consistent responses than impersonating an imagined ideal - and consistency is itself scored on many instruments.

### Common pitfalls

- **Answering idealistically rather than practically.** Choosing the option that sounds noblest rather than the one that would actually work given the stakeholders and constraints described.
- **Selecting passive options.** Waiting, watching, referring without recommendation, or hoping a retrospective will surface it - assessments consistently punish delay dressed as diligence, and so does the role.
- **Escalating too early or too dramatically.** Skipping the conversation, the design authority, or the SRO to reach the most senior name in the scenario. Escalation is a tool of last resort, and using it first signals you cannot operate your own level's influence.
- **Rescuing instead of leading.** Quietly redoing others' work to protect short-term quality at the cost of capability, trust, and honest visibility of problems - the signature failure mode of technically excellent leads.
- **Ignoring the stated organisational values.** UK public sector scenarios reward user needs, transparency, collaboration, accessibility, and inclusion. An option that sacrifices any of these for schedule or comfort is rarely the intended best answer.
- **Betraying confidences and working covertly.** Naming private sources, lobbying around decision-makers, or making roadmap promises you plan to break. Any option built on someone not finding out is usually the least effective on the page.

## Conclusion

You have now worked through four substantial sets of practice material, each built directly from the duties and skills of your role as a lead technical architect: cognitive reasoning over decision records, dependency chains, and governance logic; numeric reasoning over budgets, capacity figures, availability chains, and cost-recovery models; verbal reasoning over standards, supplier correspondence, assurance reports, and terms of reference; and situational judgement across the stakeholder landscape you navigate every week - delivery teams, senior sponsors, suppliers, and cross-government partners.

If a theme runs through all four sections, it is this: the assessments measure, in compressed and timed form, the same disciplines your role already demands. Tracing consequences beyond the first hop. Dividing by the right baseline. Refusing to let plausibility substitute for evidence. Choosing the response that manages the risk, keeps the work transparent, and strengthens the people involved. You have been practising these disciplines throughout your career; the tests simply ask you to demonstrate them in miniature.

As next steps, consider three habits. First, revisit the questions you found hardest - not to memorise answers, but to name the reasoning move each one required; the moves recur, in tests and in the job. Second, fold this practice into your normal work: hunt for the contradiction in the next options paper you assure, recompute the next weighted scorecard you are shown, write three True/False/Cannot Say statements about the next standard you read. Third, share the practice: working through scenarios like these with the architects you mentor is an excellent community-of-practice exercise, and articulating why an option is weak is precisely the coaching skill your role profile asks you to develop in others.

Approach any real assessment rested, unhurried, and curious. A strong performance is not about being a different person under test conditions - it is about letting the judgement you exercise every day show up cleanly on the page. You lead the technical design of systems and services that matter to millions of people; that experience is your preparation. Good luck, and enjoy the continued journey of professional development.
