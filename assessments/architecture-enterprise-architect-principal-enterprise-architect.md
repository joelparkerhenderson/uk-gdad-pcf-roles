# Enterprise Architect (Principal Enterprise Architect) - Psychometric Assessment Resources

## Introduction

Welcome. This document is written for you: a principal enterprise architect working within the UK Government Digital and Data profession. You lead at the highest level of the architecture practice, and you are responsible for ensuring that enterprise strategy is developed, agreed and followed across business, technology and data domains. Whether you are preparing for an internal assessment, a promotion board, a move to another department, or you simply want to sharpen the mental disciplines that underpin your work, this resource is designed to help you practise, reflect and prepare with confidence.

Psychometric assessments are structured, standardised exercises that measure the mental capabilities and behavioural judgement that predict performance in a specific role. They are widely used across the Civil Service and the wider public sector because they are fair, evidence-based and job-relevant. For a principal enterprise architect, they are not abstract puzzles: a well-designed assessment for your role will ask you to interpret portfolio investment data, reason precisely about architectural principles and policy wording, spot inconsistencies in roadmaps and reference architectures, and exercise judgement in politically sensitive, high-stakes stakeholder situations. In other words, they test what you actually do.

This document contains four assessment guides, each aligned to a recognised assessment type:

1. **Workplace job-specific cognitive assessment** - pattern recognition, logical deduction, error checking and prioritisation using the artefacts you genuinely handle: roadmaps, capability models, transition states, governance decision logs and Digital Twin architectures.
2. **Workplace job-specific numeric reasoning assessment** - interpretation of budgets, portfolio metrics, supplier cost models, capacity figures and value-for-money analyses.
3. **Workplace job-specific verbal reasoning assessment** - precise comprehension of dense written material such as architectural principles, strategy papers, commercial frameworks and cross-government policy text.
4. **Workplace job-specific situational judgement assessment** - realistic dilemmas involving senior stakeholders, architecture communities, supplier decisions and strategic trade-offs, judged against UK public sector values.

Each guide explains what the assessment measures, maps it explicitly to the skills in your role profile, and then gives you a substantial set of practice questions with full worked explanations. Each guide closes with preparation tips and common pitfalls tailored to your level.

How should you use this resource? Three suggestions. First, practise under light time pressure: attempt each question before reading the answer, and note where your reasoning diverged from the explanation. Second, use the questions for self-reflection: many of the scenarios are drawn directly from the duties in your role profile, so they double as prompts for thinking about how you currently operate. Third, use it for preparation: if you have a real assessment coming up, work through one section per sitting rather than the whole document at once, and revisit the pitfalls the day before.

You operate at a level where clarity of thought under complexity is the core of the job. Treat this document as a gymnasium for exactly that. Good luck - and enjoy the practice.

## Advisory

"This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff."

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive assessment measures the exact mental processes your role demands, using practical workplace scenarios rather than abstract IQ-style items. For a principal enterprise architect, that means questions built around the artefacts you handle every week: enterprise roadmaps with 'as is', transitional and 'to be' states; capability models; architectural principles and standards; governance decision logs; dependency maps across portfolios and programmes; and the data structures that feed a Digital Twin of the organisation.

The typical format is online, timed, and multiple choice. Expect 15 to 30 minutes, with somewhere between 15 and 25 questions, so roughly a minute per question - though harder items reward two or three minutes and easier items should take thirty seconds. Scoring is objective and usually normed against a benchmark group of comparable professionals, and modern platforms often report speed and accuracy separately rather than a single figure. Some platforms adapt the difficulty as you go: answering well brings harder questions, which is a good sign, not a bad one.

Why does this matter for your role? Because at principal level, your value lies in seeing structure inside complexity: recognising that three programmes are unknowingly building the same capability, spotting the logical flaw in a transition plan before it costs a year, deducing the downstream consequences of a policy change on your reference architectures, and prioritising ruthlessly when everything is labelled critical. Cognitive assessments sample exactly these operations - pattern recognition, logical deduction, error checking, prioritisation and structured problem solving - under mild time pressure that simulates the pace of senior decision-making.

### What it measures for your role

Mapped against the skills in your role profile:

- **Enterprise architecture** and **Strategy design**: pattern recognition and abstraction - seeing the common capability across portfolios, connecting strategies, and detecting where organisation-wide changes drift from the architectural strategy.
- **Making architectural decisions**: logical deduction under high risk and complexity - reasoning correctly from principles, standards and constraints to a defensible decision, and identifying architectural risks across the organisation or wider government.
- **Problem definition and shaping**: structuring ambiguous, highly complex problems so that a solution can be created, challenging assumptions and spotting the hidden variable that changes the answer.
- **Architect for the whole context**: inference from trends - deducing the plausible impact of societal and industry shifts on the organisation and building resilience into architectural work.
- **Architecture communication** and **Community collaboration**: error checking - finding the inconsistency in a roadmap, decision log or Digital Twin dataset before it misleads senior stakeholders or the architecture community you lead.
- **Commercial perspective**: evaluating supplier and contractual options logically against weighted criteria.

### Practice questions

**Question 1 (easy) - Pattern recognition in a capability roadmap**

Your enterprise roadmap shows four capabilities progressing through maturity states: Initial → Repeatable → Defined → Managed → Optimising. The quarterly assessments read:

- Identity management: Initial, Repeatable, Defined, Managed
- Case management: Repeatable, Defined, Managed, Optimising
- Payments: Initial, Initial, Repeatable, Defined
- Data sharing: Defined, Managed, Optimising, Optimising

A fifth capability, Notifications, has read Initial, Repeatable, Repeatable over three quarters. Given the dominant pattern above, which projection for Notifications in quarters four and five is most consistent with the observed progression behaviour?

A) Repeatable, Repeatable
B) Defined, Managed
C) Managed, Optimising
D) Initial, Repeatable

**Correct answer: B.**

**Explanation:** The pattern across the portfolio is steady one-step progression per quarter, with occasional single-quarter plateaus (Payments plateaued at Initial, Notifications at Repeatable, Data sharing at Optimising - the ceiling). After a plateau, capabilities resume one-step progression; none regress and none skip levels. Notifications has just completed its plateau quarter, so the most consistent projection is one step per quarter: Defined, then Managed. Option C skips a level, D regresses, and A assumes an extended plateau for which there is no precedent in the data. This is the kind of trajectory reasoning you apply when judging whether a 'to be' state is achievable on the claimed timeline.

**Question 2 (easy) - Error checking a governance decision log**

You are quality-assuring the architecture governance decision log before it goes to the design authority. Four entries read:

1. ADR-114: "Approved reuse of the cross-government identity platform, subject to a Data Protection Impact Assessment, decision owner: Chief Data Officer."
2. ADR-115: "Approved exception to cloud-first principle for the legacy mainframe, expiry: 31 March 2027, decision owner: Principal Enterprise Architect."
3. ADR-116: "Rejected proposal to build a bespoke payments engine; directed reuse of GOV.UK Pay, decision owner: Principal Enterprise Architect."
4. ADR-117: "Approved exception to cloud-first principle for the legacy mainframe, expiry: 31 December 2026, decision owner: Head of Infrastructure."

Which single issue must be resolved before publication?

A) ADR-114 should not name the Chief Data Officer
B) ADR-115 and ADR-117 record contradictory versions of the same decision
C) ADR-116 should be an approval, not a rejection
D) ADR-117 has no expiry date

**Correct answer: B.**

**Explanation:** ADR-115 and ADR-117 both grant a cloud-first exception for the same legacy mainframe but record different expiry dates and different decision owners. A decision log that contradicts itself undermines architectural governance, because teams will cite whichever entry suits them. Option A is not a defect on the information given; C is a judgement call outside the log's internal consistency; D is factually wrong - ADR-117 does state an expiry. The discipline being tested is exact, line-level error checking of governance artefacts, which is central to leading and evolving architectural governance and assurance.

**Question 3 (moderate) - Logical deduction from architectural principles**

Your organisation has established these architectural principles:

- P1: Reuse before buy; buy before build.
- P2: All citizen-facing services must meet the government accessibility regulations.
- P3: Any new data store containing personal data requires an approved retention schedule.
- P4: Exceptions to any principle require design authority approval and a documented expiry.

A programme proposes building a bespoke appointment-booking service with a new personal-data store, citing urgency. No reuse assessment has been performed, no retention schedule exists, and no exception has been sought. Which statement follows necessarily from the principles?

A) The proposal must be rejected permanently
B) The proposal cannot proceed as submitted, but could proceed with either a reuse assessment showing no viable reuse or buy option, or approved exceptions - plus an approved retention schedule
C) The proposal can proceed if the programme director accepts the risk
D) The proposal complies with P2, so only P1 is at issue

**Correct answer: B.**

**Explanation:** Deduce carefully. P1 is breached because "build" was chosen without demonstrating that reuse and buy were exhausted - but P4 provides a lawful route around any principle via an approved, time-limited exception, so rejection need not be permanent (eliminating A). P3 is breached independently: a new personal-data store requires an approved retention schedule, and nothing in P4 removes that requirement's substance - an exception would itself need approval. C fails because programme-level risk acceptance is not the mechanism the principles define; only design authority approval is. D fails because P2's status is unknown (the accessibility posture was never stated - you cannot infer compliance from silence). B is the only option that follows necessarily. This mirrors real governance reasoning: knowing precisely what your principles do and do not entail, and which routes to compliance genuinely exist.

**Question 4 (moderate) - Prioritisation across portfolios**

You have capacity to personally lead exactly two interventions this quarter. Your assessment of four candidate interventions:

- W: Unblock a stalled cross-cutting identity capability on which three portfolios depend; without it, all three slip a quarter.
- X: Review a single programme's solution architecture that has already passed design authority with conditions.
- Y: Author the enterprise data strategy refresh, due to the executive committee in five months, with a capable deputy available to draft it.
- Z: Resolve an escalated dispute between two departments over ownership of a shared integration platform that is now blocking releases for both.

Applying the principle of maximising enterprise-wide flow of change while developing your community, which pair should you lead personally?

A) W and X
B) W and Z
C) X and Y
D) Y and Z

**Correct answer: B.**

**Explanation:** W and Z are the two items that are (i) blocking multiple teams now, and (ii) genuinely require principal-level authority - W is a cross-cutting dependency affecting three portfolios, and Z is an inter-departmental conflict that your role profile explicitly assigns to you: solving and unblocking issues between teams or departments at the highest level. X is already governed with conditions - delegable follow-up, not principal-level work. Y matters strategically but has a five-month runway and a capable deputy: delegating the draft develops the architecture community while you retain direction, which is exactly how a principal should multiply capacity. The trap options bundle one high-value item with one delegable item; prioritisation questions at this level test whether you distinguish urgency-plus-uniqueness from mere importance.

**Question 5 (moderate) - Dependency logic in transition states**

Your transition plan contains these constraints:

- The legacy CRM cannot be decommissioned until the new case management platform is live.
- The new case management platform cannot go live until the identity service is upgraded.
- The identity service upgrade and the data migration can run in parallel.
- The Digital Twin's operational view can only be trusted once both the data migration is complete and the legacy CRM is decommissioned.

The identity upgrade takes 2 quarters, case management go-live takes 1 quarter after identity completes, decommissioning takes 1 quarter after go-live, and data migration takes 3 quarters. Everything may start now. What is the earliest the Digital Twin's operational view can be trusted?

A) After 3 quarters
B) After 4 quarters
C) After 5 quarters
D) After 6 quarters

**Correct answer: B.**

**Explanation:** Trace the two chains. Chain one: identity upgrade (quarters 1-2) → case management go-live (quarter 3) → legacy CRM decommissioned (quarter 4). Chain two: data migration runs in parallel from the start (quarters 1-3). The Digital Twin view requires both chains complete: max(4, 3) = 4 quarters. Option C or D result from serialising work the constraints allow in parallel; A ignores the decommissioning dependency. Critical-path deduction like this underpins your ownership of 'as is', transitional and 'to be' states - and your responsibility for a trustworthy Digital Twin, which is only as good as the sequencing logic behind it.

**Question 6 (moderate) - Spotting duplicated capability across programmes**

Reviewing three programme architectures, you note the following components:

- Programme Alpha: citizen identity verification, document upload, address lookup, payment collection.
- Programme Beta: business identity verification, document upload, company registry lookup, grant disbursement.
- Programme Gamma: citizen identity verification, appointment booking, address lookup, payment collection.

Your reference architecture designates identity verification, address lookup and payments as shared enterprise capabilities. Which conclusion is best supported?

A) All three programmes are fully compliant with the reference architecture
B) Document upload should immediately be designated a shared capability
C) There is prima facie duplication of at least three shared-capability builds across programmes, requiring a reuse investigation before further build funding
D) Programme Beta is the only compliant programme

**Correct answer: C.**

**Explanation:** Identity verification appears in all three programmes, address lookup in two, and payment collection in two - all three are designated shared enterprise capabilities, yet each programme lists them as components of its own architecture, which is prima facie evidence of duplicated build. The data does not tell you whether the programmes are consuming a shared service or building their own, which is precisely why C says "prima facie... requiring a reuse investigation" rather than asserting non-compliance outright - and why A and D overreach the evidence. B is a plausible future action (document upload appears twice) but the pattern evidence is weaker and "immediately" overstates it. The tested skill is recommending reuse to achieve value for money and reduce risk - and knowing the difference between a signal and a verdict.

**Question 7 (moderate) - Inference from horizon scanning signals**

Your horizon scan notes four signals:

1. Two major cloud providers have announced UK sovereign cloud regions launching within 18 months.
2. A draft EU regulation, likely to influence UK policy, tightens rules on cross-border transfer of citizen data.
3. Your largest hosting contract expires in 20 months.
4. The Digital Twin programme requires data residency guarantees it currently lacks.

Which synthesis represents the strongest architectural inference?

A) The signals are unrelated and should be tracked separately
B) The contract expiry is a risk; the other signals are context only
C) The convergence of sovereign cloud availability, tightening data-transfer policy and the contract expiry creates a strategic window to align re-procurement with data residency requirements, resolving the Digital Twin gap
D) The organisation should immediately migrate all workloads to a sovereign region

**Correct answer: C.**

**Explanation:** The heart of horizon scanning at principal level is synthesis: individually, each signal is mildly interesting; together they define a decision window. Sovereign regions become available (signal 1) shortly before your contract expires (signal 3); policy direction (signal 2) suggests residency requirements will harden; the Digital Twin already needs residency guarantees (signal 4). Re-procurement is the natural lever to satisfy all of them at once. A ignores the convergence, B underweights policy risk, and D jumps from inference to commitment without any options analysis, breaching the discipline of making decisions characterised by high risk and complexity only after shaping the problem. Anticipating changes to policy and building resilience through your architectural work is exactly this move.

**Question 8 (hard) - Logical consistency of a strategy cascade**

An executive strategy paper asserts:

- S1: "All new services will be cloud-native by 2028."
- S2: "The department will reduce total technology spend by 20% by 2028."
- S3: "No service currently rated 'critical' will undergo re-platforming before 2027."
- S4: "Three of the five services rated 'critical' are hosted on end-of-life on-premises infrastructure whose extended support costs double every year from 2026."

Which statement identifies the genuine tension in this cascade?

A) S1 contradicts S3, because cloud-native mandates re-platforming critical services immediately
B) S3 combined with S4 places the spend-reduction goal in S2 at risk, because deferring re-platforming of critical services locks in escalating support costs during the very window when savings must accrue
C) S2 and S1 are incompatible, because cloud migration always increases spend
D) There is no tension; the statements are mutually consistent

**Correct answer: B.**

**Explanation:** Test each claimed conflict. A fails because S1 governs new services only - it imposes nothing on existing critical services, so it cannot contradict S3. C asserts an "always" that is neither stated nor true. The real tension is a timing interaction: S3 forbids re-platforming critical services before 2027, S4 says three of them sit on infrastructure whose support costs double annually from 2026, and S2 demands a 20% spend reduction by 2028. Deferral therefore guarantees a cost spike inside the savings window - the strategies are not formally contradictory, but jointly high-risk, which is what D misses. Detecting interactions between individually reasonable strategic statements is the essence of defining and connecting strategies across the organisation, and of assuring that business, technology and data decisions align with enterprise architecture strategy.

**Question 9 (hard) - Error checking Digital Twin data lineage**

Your Digital Twin ingests four feeds. The lineage register states:

- Feed 1 (asset inventory): refreshed daily; last refresh yesterday; owner: Infrastructure.
- Feed 2 (service performance): refreshed hourly; last refresh 3 hours ago; owner: Operations.
- Feed 3 (organisation structure): refreshed monthly; last refresh 6 weeks ago; owner: HR.
- Feed 4 (financial actuals): refreshed weekly; last refresh 5 days ago; owner: Finance.

The Twin's dashboard displays a "data currency: all green" banner. Which feeds contradict the banner?

A) Feeds 2 and 3
B) Feed 3 only
C) Feeds 2, 3 and 4
D) Feeds 1 and 4

**Correct answer: A.**

**Explanation:** Compare each feed's stated cadence with its actual last refresh. Feed 1: daily cadence, refreshed yesterday - compliant. Feed 2: hourly cadence, last refreshed 3 hours ago - two missed cycles, non-compliant. Feed 3: monthly cadence, last refreshed 6 weeks ago - overdue by two weeks, non-compliant. Feed 4: weekly cadence, refreshed 5 days ago - within cycle, compliant. So exactly Feeds 2 and 3 contradict the "all green" banner. The common error is anchoring on absolute elapsed time (3 hours "sounds" fresh, 5 days "sounds" stale) instead of elapsed time relative to declared cadence. As the role accountable for the creation, maintenance and consumption of the Digital Twin, this relative-freshness check is precisely how you keep senior stakeholders from trusting a stale picture.

**Question 10 (hard) - Problem shaping: finding the real constraint**

Two departments escalate to you: their shared integration platform "lacks capacity", and each demands funding for its own replacement. Your investigation finds: platform utilisation peaks at 61%; the release calendar allows each department only one deployment window per month; both departments' releases have queued behind each other's failed changes twice this quarter; and the platform team is fully staffed but spends 70% of its time on manual regression testing.

Which problem framing best fits the evidence?

A) A capacity problem: the platform needs more compute
B) A funding problem: each department should procure its own platform
C) A flow problem: constrained release windows and slow manual testing create queuing that presents as "capacity", so the intervention is test automation and decoupled deployment, not duplication
D) A people problem: the platform team is understaffed

**Correct answer: C.**

**Explanation:** Check each framing against the evidence. Utilisation peaking at 61% directly refutes A - the machines are not the constraint. The team is fully staffed, refuting D; the constraint is where their time goes (70% manual regression), not headcount. B would duplicate a shared capability, breaching reuse-first, and would not fix the queuing dynamics anyway. The observed symptoms - monthly windows, releases queuing behind failed changes, testing consuming most team capacity - are classic flow constraints; automating regression and decoupling deployments attacks the actual bottleneck. This is the skill your profile calls leading the framing of a problem characterised by high complexity so that a solution can be created - and helping others challenge requirements ("we need our own platform") and assumptions ("it's a capacity issue").

**Question 11 (hard) - Deductive reasoning on standards applicability**

Your standards catalogue states:

- All services handling personal data must use the enterprise identity service, unless granted an exception.
- Services classified OFFICIAL-SENSITIVE must additionally implement enhanced monitoring.
- Exceptions cannot be granted to services classified OFFICIAL-SENSITIVE.
- Service Q handles personal data and holds a current exception from using the enterprise identity service.

Which conclusion follows necessarily?

A) Service Q implements enhanced monitoring
B) Service Q is not classified OFFICIAL-SENSITIVE
C) Service Q does not handle personal data
D) Service Q must adopt the enterprise identity service within 12 months

**Correct answer: B.**

**Explanation:** Work the logic: Service Q holds a current exception. Rule three states exceptions cannot be granted to OFFICIAL-SENSITIVE services. Therefore, since Q has a valid exception, Q cannot be OFFICIAL-SENSITIVE - B follows by modus tollens. A depends on Q being OFFICIAL-SENSITIVE, which we have just disproved. C contradicts the stated facts. D invents a time limit found nowhere in the rules. Assessments at this level deliberately include attractive options that import plausible-sounding policy details (like "12 months") that the text never establishes; representing architectural governance within wider governance, including legal and commercial forums, demands exactly this precision about what rules do and do not say.

**Question 12 (hard) - Prioritising architectural risks across government**

Your cross-government risk review identifies four architectural risks. Impact and likelihood are scored 1-5; controls are noted:

- R1: Single supplier holds all integration IP. Impact 5, Likelihood 2. No exit plan exists.
- R2: Two departments' data models for citizens are diverging. Impact 3, Likelihood 5. A data standards board exists but has not met for a year.
- R3: An emerging technology adopted by one team lacks security accreditation. Impact 4, Likelihood 3. Accreditation is underway.
- R4: A shared platform's sole architect is retiring in 3 months. Impact 4, Likelihood 5. No succession plan.

Using expected exposure (impact x likelihood) adjusted for control status, which two risks should lead your intervention plan?

A) R1 and R3
B) R2 and R4
C) R1 and R4
D) R3 and R2

**Correct answer: B.**

**Explanation:** Compute raw exposure: R1 = 10, R2 = 15, R3 = 12, R4 = 20. Then adjust for controls: R3 already has a mitigation in flight (accreditation underway), reducing its residual priority; R2's nominal control (the standards board) is dormant, so its raw score stands or worsens; R1 and R4 have no controls, but R1's raw exposure (10) is the lowest of the four. Highest residual exposures are R4 (20, uncontrolled, and time-bound by the retirement date) and R2 (15, control failed). R1's severity feels alarming because impact 5 draws the eye - a classic trap; likelihood 2 and a 10 raw score place it behind both. Identifying and addressing architectural risks across the organisation or wider government means ranking by evidence, not by which risk sounds most dramatic, while still scheduling R1's exit plan next.

**Question 13 (moderate) - Sequence logic for community development**

You are designing a development pathway for your enterprise architecture community. The modules and their prerequisites: Foundations (no prerequisite); Domain architecture (requires Foundations); Architecture communication (requires Foundations); Governance practice (requires Domain architecture); Strategic advising (requires both Architecture communication and Governance practice). Each architect can complete one module per quarter. What is the minimum number of quarters for a new architect to reach Strategic advising?

A) 3
B) 4
C) 5
D) 6

**Correct answer: C.**

**Explanation:** The trap here is treating this as a pure critical-path question. If two modules could be taken in parallel, the longest prerequisite chain (Foundations → Domain architecture → Governance practice → Strategic advising) would give four quarters, and Architecture communication would slot alongside - hence the tempting answer B. But one architect can complete only one module per quarter, so every module occupies its own quarter: five modules stand between a new starter and completing Strategic advising, and all five are mandatory (Strategic advising requires both branches). The best any ordering can do is: Q1 Foundations, Q2 Domain architecture, Q3 Architecture communication (or Governance practice's prerequisite order swapped), Q4 Governance practice, Q5 Strategic advising - five quarters. The lesson: identify whether the binding constraint is the dependency graph or the resource limit. Here the resource limit (one module per quarter) dominates, exactly as a single shared platform team, not the plan's logic, often dominates a transition timeline. Developing the architecture community includes designing pathways whose durations are honest about such constraints.

### Preparation tips

- **Practise with your own artefacts.** Take a real roadmap, decision log or dependency map and interrogate it: what is the critical path, where are the contradictions, which two items would you personally lead? You will recognise the question styles instantly in the live test.
- **Rehearse relative checks, not absolute ones.** Freshness relative to cadence, exposure relative to controls, progress relative to pattern. Assessments at principal level almost always hide the answer in a ratio or comparison, not a raw figure.
- **Time-box each item.** Around a minute per question on average; bank the easy ones fast, and give recovered time to the multi-constraint items. If an item resists you after two and a half minutes, select your best elimination-based answer, flag it if the platform allows, and move on.
- **Read the stem's quantifiers like a lawyer.** "All new services", "unless granted an exception", "necessarily follows" - at your level the test is rarely the arithmetic; it is whether you noticed which words constrain the answer.
- **Do a short warm-up.** Ten minutes of logic puzzles or one practice set immediately before the assessment measurably reduces slow starts. Arrive rested; senior candidates most often underperform through fatigue and overconfidence, not ability.

### Common pitfalls

- **Importing outside knowledge.** You know how government architecture "really works" - but the question's rules are the whole universe. Answer from the material given, exactly as you would hold a programme to the written standard rather than to folklore.
- **Anchoring on dramatic details.** Impact-5 risks, "urgent" programmes and large numbers draw attention away from the option the logic actually supports. Compute before you commit.
- **Serialising parallel work.** In dependency questions, the most common wrong answer comes from adding durations that the constraints allow to overlap. Sketch the chains.
- **The time-sink question.** One fiendish multi-stage item can consume a quarter of your window. Skipping it and returning is a strategy decision - make it deliberately, the way you would triage an overloaded governance agenda.
- **First-instinct lock-in.** As Question 13 demonstrated, a fast plausible answer can survive right up until you check it. Build a five-second verification pass into every answer: does my choice satisfy every stated constraint?

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment evaluates how well you analyse, interpret and make sound decisions using numerical data drawn from your actual working context. It is business mathematics, not abstract mathematics: percentages, ratios, weighted comparisons, cost projections and capacity figures, presented in the tables, dashboards and financial summaries a principal enterprise architect genuinely encounters. Most assessments allow or provide an on-screen calculator, because the skill being measured is interpretation and decision quality, not mental arithmetic.

Expect a strict time limit - commonly 20 to 30 minutes for 15 to 20 questions - and inputs such as portfolio budget tables, supplier pricing schedules, cloud consumption reports, benefits-realisation dashboards and Digital Twin data-quality metrics. Questions typically require two or three extraction-and-calculation steps: find the right figures, combine them correctly, and compare the result against options or a threshold.

For your role, numeric fluency is not optional polish; it is how architectural argument becomes executive decision. When you recommend reuse over build, the recommendation stands or falls on a defensible cost comparison. When you guide the organisation towards sustainability and scalability, you quantify consumption trajectories. When you advise on supplier selection, you evaluate weighted commercial scores. When you present the case for retiring legacy estate to a spending review, the numbers must survive scrutiny by finance directors. An assessment of this kind samples exactly that capability: can you move from a dense table to a correct, decision-ready figure, quickly and without being misled?

### What it measures for your role

Mapped against the skills in your role profile:

- **Commercial perspective**: evaluating and selecting suppliers using weighted criteria, comparing contractual frameworks by total cost, and spotting when a headline price hides a lifetime cost.
- **Making architectural decisions**: quantifying risk exposure and cost consequences so that decisions characterised by high risk and complexity rest on evidence.
- **Enterprise architecture** and **Strategy design**: portfolio-level arithmetic - budget allocations, benefits realisation, spend-reduction trajectories and the value-for-money case for reuse, sustainability and scalability.
- **Architect for the whole context**: interpreting trend data from horizon scanning - adoption curves, cost curves for emerging technologies, and energy or carbon figures.
- **Ownership of the Digital Twin**: data-quality and coverage percentages, refresh-rate compliance, and capacity metrics for the platforms that feed it.
- **Architecture communication**: translating calculations into figures senior stakeholders can trust - which requires you to get them right first.

### Practice questions

**Question 1 (easy) - Percentage change in portfolio spend**

Your technology portfolio spent £48.0m last financial year. The spending plan for this year is £42.0m. What percentage reduction does the plan represent?

A) 6.0%
B) 12.5%
C) 14.3%
D) 87.5%

**Correct answer: B.**

**Explanation:** Reduction = £48.0m - £42.0m = £6.0m. Percentage reduction = 6.0 / 48.0 x 100 = 12.5%. The classic error is dividing by the new figure (6.0 / 42.0 = 14.3%, option C) instead of the original. Always divide the change by the starting value. Option D is the ratio of new to old spend (42/48 = 87.5%) - the amount remaining, not the reduction.

**Question 2 (easy) - Reuse versus build**

A programme proposes building a document-verification component for £850,000 with annual running costs of £120,000. The shared enterprise component can be consumed for an onboarding cost of £150,000 plus £95,000 per year. Over a four-year horizon, how much does reuse save?

A) £700,000
B) £800,000
C) £570,000
D) £1,330,000

**Correct answer: B.**

**Explanation:** Build: £850,000 + (4 x £120,000) = £850,000 + £480,000 = £1,330,000. Reuse: £150,000 + (4 x £95,000) = £150,000 + £380,000 = £530,000. Saving = £1,330,000 - £530,000 = £800,000. Option A is the difference in one-off costs only (£850k - £150k); C is the reuse total minus a misread; D is the build total mistaken for the saving. This is the core value-for-money arithmetic behind "recommend reuse... to achieve value for money and reduce risk" - always compare totals over a stated horizon, never headline build costs alone.

**Question 3 (moderate) - Weighted supplier evaluation**

You are moderating a supplier evaluation for an integration platform. Scores (out of 10) and weightings:

| Criterion | Weight | Supplier A | Supplier B | Supplier C |
|---|---|---|---|---|
| Technical capability | 40% | 8 | 7 | 9 |
| Cost | 30% | 6 | 9 | 5 |
| Sustainability | 15% | 7 | 6 | 8 |
| Exit provisions | 15% | 5 | 8 | 6 |

Which supplier wins on weighted score?

A) Supplier A
B) Supplier B
C) Supplier C
D) A and B tie

**Correct answer: B.**

**Explanation:** Supplier A: (8 x 0.40) + (6 x 0.30) + (7 x 0.15) + (5 x 0.15) = 3.20 + 1.80 + 1.05 + 0.75 = 6.80. Supplier B: (7 x 0.40) + (9 x 0.30) + (6 x 0.15) + (8 x 0.15) = 2.80 + 2.70 + 0.90 + 1.20 = 7.60. Supplier C: (9 x 0.40) + (5 x 0.30) + (8 x 0.15) + (6 x 0.15) = 3.60 + 1.50 + 1.20 + 0.90 = 7.20. B wins with 7.60. Note the instinct trap: C has the best technical score and A "feels" balanced, but the weighting model rewards B's cost and exit strength. Identifying, evaluating and selecting appropriate suppliers means letting the agreed weighting model decide - and knowing the arithmetic well enough to challenge a model that produces perverse results.

**Question 4 (moderate) - Legacy support cost escalation**

Extended support for a legacy platform costs £1.2m this year and doubles each year. Re-platforming would cost a one-off £5.5m and could complete at the end of year 2, eliminating support costs from year 3 onwards. If you re-platform, you pay support for years 1 and 2 plus the re-platforming cost. What is the total cost by the end of year 4 for each path?

A) Stay: £18.0m; Re-platform: £9.1m
B) Stay: £9.6m; Re-platform: £9.1m
C) Stay: £18.0m; Re-platform: £11.5m
D) Stay: £12.0m; Re-platform: £8.2m

**Correct answer: A.**

**Explanation:** Staying: support costs are £1.2m, £2.4m, £4.8m, £9.6m across years 1-4, totalling £18.0m. Re-platforming: support in years 1-2 (£1.2m + £2.4m = £3.6m) plus £5.5m one-off = £9.1m, with nothing in years 3-4. Option B mistakes year 4's single-year support cost (£9.6m) for the four-year total - a common misreading of "doubles each year". This doubling-cost pattern is exactly the one in strategic tension questions: the arithmetic shows why deferring re-platforming can quietly destroy a spend-reduction target.

**Question 5 (moderate) - Cloud consumption and sustainability**

Your Digital Twin's analytics workload consumes 180,000 compute-hours per quarter at £0.42 per hour. Right-sizing is projected to cut consumption by 25%, and moving to a greener region adds 5% to the unit rate but reduces the workload's carbon footprint by 40%. If both changes are made, what is the new quarterly compute cost?

A) £75,600
B) £59,535
C) £56,700
D) £79,380

**Correct answer: B.**

**Explanation:** New consumption: 180,000 x 0.75 = 135,000 hours. New rate: £0.42 x 1.05 = £0.441 per hour. New cost: 135,000 x £0.441 = £59,535. Option A is the original cost (180,000 x £0.42 = £75,600); C applies the consumption cut but not the rate rise; D applies the rate rise but not the consumption cut. The carbon figure is context, not calculation - assessments often include a number you do not need, to test extraction discipline. Recommending sustainability alongside value for money means being able to show that the green option here costs £16,065 less per quarter than the status quo, not more.

**Question 6 (moderate) - Benefits realisation ratio**

A transformation programme claimed benefits of £24m over three years for costs of £15m. At the two-year review, realised benefits are £11m against costs to date of £12m. Assuming the remaining £3m of budgeted cost is spent, what annual benefit must year 3 deliver for the programme to achieve a benefit-cost ratio of at least 1.4?

A) £10m
B) £13m
C) £9m
D) £6.5m

**Correct answer: A.**

**Explanation:** Total cost = £12m + £3m = £15m. Required total benefits for a ratio of 1.4 = 1.4 x £15m = £21m. Benefits already realised = £11m, so year 3 must deliver £21m - £11m = £10m. Option B works towards the original £24m claim; C and D result from ratio errors (using 1.4 x remaining cost, or halving). Note the strategic insight the arithmetic reveals: year 3 must deliver nearly as much benefit as the first two years combined - a signal you would challenge hard when assuring that decisions align with enterprise strategy, and exactly the kind of quantified scepticism senior stakeholders expect from you.

**Question 7 (moderate) - Capacity headroom for a shared platform**

A shared integration platform handles a peak of 5,400 transactions per second (tps) against a tested capacity of 9,000 tps. Two new consuming services are due: one adds a projected peak of 1,800 tps, the other 1,350 tps. Your standard requires 25% headroom above projected peak at all times. After onboarding both services, is the standard met?

A) Yes - projected peak is 8,550 tps, within capacity
B) No - projected peak of 8,550 tps leaves only 5% headroom, breaching the 25% standard
C) Yes - headroom is measured against average load, not peak
D) No - the platform is already over capacity today

**Correct answer: B.**

**Explanation:** Projected peak: 5,400 + 1,800 + 1,350 = 8,550 tps. The standard requires capacity of at least 8,550 x 1.25 = 10,687.5 tps, but tested capacity is 9,000 tps - a shortfall. Equivalently, actual headroom is (9,000 - 8,550) / 8,550 = 5.3%, far below 25%. Option A confuses "within capacity" with "meets the headroom standard" - the precise distinction your standards exist to enforce. C invents a different measurement basis; D is factually wrong (5,400 < 9,000 today). Scalability guidance is only as good as the arithmetic behind it: this is how you convert a standard into a concrete onboarding decision - onboard one service now, or expand capacity first.

**Question 8 (moderate) - Digital Twin data coverage**

Your Digital Twin aims to represent 100% of the organisation's 2,400 technology assets. Current coverage: infrastructure assets 92% of 1,500; application assets 75% of 640; data assets 60% of 260. What is the overall coverage percentage, to the nearest whole number?

A) 76%
B) 84%
C) 86%
D) 79%

**Correct answer: B.**

**Explanation:** Covered assets: infrastructure 0.92 x 1,500 = 1,380; applications 0.75 x 640 = 480; data 0.60 x 260 = 156. Total covered = 1,380 + 480 + 156 = 2,016. Coverage = 2,016 / 2,400 = 0.84 = 84%. The tempting shortcut - averaging the three percentages, (92 + 75 + 60) / 3 = 75.7% ≈ 76%, option A - is wrong because the categories differ enormously in size: infrastructure's 1,500 assets must weigh more than data's 260. This is the weighted-average trap, and it appears constantly in real coverage, compliance and adoption reporting. As the owner of the Digital Twin's creation, maintenance and consumption, you will present coverage figures to boards; the difference between a naive average and a weighted one is the difference between a defensible figure and an embarrassing correction.

**Question 9 (hard) - Ratio reasoning on architecture community growth**

Your architecture community has 45 members: enterprise, solution and technical architects in the ratio 2:4:9. The strategy requires the enterprise-to-solution ratio to reach 1:1.5 within two years while the technical architect headcount stays fixed. If solution architect numbers stay fixed too, how many additional enterprise architects must you develop or recruit?

A) 2
B) 4
C) 6
D) 8

**Correct answer: A.**

**Explanation:** Ratio 2:4:9 across 45 people means each ratio unit is 45 / 15 = 3 people: 6 enterprise, 12 solution, 27 technical architects. Target enterprise:solution = 1:1.5 with solution fixed at 12 means enterprise must reach 12 / 1.5 = 8. Additional needed = 8 - 6 = 2. Option C comes from misreading the target as 1.5:1 (which would need 18 enterprise architects, +12 - not an option, prompting a second look); B and D come from unit errors. Multi-step ratio questions reward writing down the intermediate headcounts rather than manipulating ratios in your head - and this particular calculation is one you will genuinely perform when growing the community with a workforce plan.

**Question 10 (hard) - Total cost of ownership across contractual frameworks**

Two contractual routes exist for a five-year platform deal:

- Framework F: £2.0m per year, fixed, with a 10% discount on years 4 and 5 if renewed after year 3; renewal probability estimated at 80%.
- Framework G: £1.6m per year for years 1-2, then £2.3m per year for years 3-5, with an exit break at end of year 2 costing £0.4m if exercised; probability of exercising the break estimated at 25%.

Using expected values over five years (assume if G's break is exercised, years 3-5 cost £2.1m per year with a replacement service instead), which route has the lower expected total cost, and by approximately how much?

A) F, by about £0.4m
B) G, by about £0.2m
C) F, by about £1.2m
D) G, by about £0.6m

**Correct answer: A.**

**Explanation:** Work each path fully. Framework F: years 1-3 = 3 x £2.0m = £6.0m. Years 4-5 with renewal (probability 0.8) cost 2 x £1.8m = £3.6m (10% discount on £2.0m); without renewal (0.2) they cost 2 x £2.0m = £4.0m. Expected years 4-5 = 0.8 x £3.6m + 0.2 x £4.0m = £2.88m + £0.80m = £3.68m. Expected total F = £6.0m + £3.68m = £9.68m. Framework G: years 1-2 = 2 x £1.6m = £3.2m in all cases. No break (probability 0.75): years 3-5 = 3 x £2.3m = £6.9m, path total £10.1m. Break exercised (0.25): £0.4m exit + 3 x £2.1m = £6.7m, path total £9.9m. Expected total G = 0.75 x £10.1m + 0.25 x £9.9m = £7.575m + £2.475m = £10.05m. F is cheaper by £10.05m - £9.68m = £0.37m, approximately £0.4m - option A. Option B is what you get if you forget F's renewal discount is only 10% probable to fail and treat G's cheaper early years as decisive; D anchors on G's low years 1-2 price - the headline-price trap. Expected-value questions with probabilistic branches are where senior candidates most often lose marks, not through method but through rushing the branch arithmetic: write out each path, multiply by its probability, and only then compare. Identifying appropriate contractual frameworks in real procurements involves exactly this expected-cost discipline, plus the judgement the numbers cannot give you.

**Question 11 (moderate) - Interpreting a performance dashboard**

The Digital Twin service dashboard shows monthly figures for a critical API: January: 12.4m calls, 99.95% availability; February: 11.8m calls, 99.99% availability; March: 14.6m calls, 99.90% availability. Your published standard is 99.95% availability in every month. Approximately how many minutes of downtime did March represent (assume a 31-day month), and did March breach the standard?

A) About 45 minutes; breach
B) About 22 minutes; no breach
C) About 45 minutes; no breach
D) About 4.5 minutes; breach

**Correct answer: A.**

**Explanation:** March minutes: 31 x 24 x 60 = 44,640. Downtime = (100% - 99.90%) x 44,640 = 0.001 x 44,640 = 44.64 minutes, about 45 minutes. The standard requires 99.95% in every month; March achieved 99.90%, which is below it - a breach. Note that call volume is a distractor: availability standards bind on percentage uptime, not traffic. Option B halves the downtime and wrongly averages the quarter; C computes correctly but misapplies the standard; D slips a decimal place - the most common error with availability percentages, where each "nine" changes the answer tenfold. Presenting service health to boards demands exactly this fluency in converting between percentages and human-meaningful minutes.

**Question 12 (hard) - Spend-reduction trajectory**

Your strategy commits to reducing annual technology spend from £60m to £48m over three years, with reductions phased 20% of the total in year 1, 30% in year 2, and 50% in year 3. At the end of year 2, actual annual spend is £56.5m. How far behind the planned trajectory is the organisation, in £m of annual spend?

A) £0.5m
B) £2.5m
C) £6.0m
D) £8.5m

**Correct answer: B.**

**Explanation:** Total planned reduction = £60m - £48m = £12m. By end of year 2, planned cumulative reduction = (20% + 30%) x £12m = 50% x £12m = £6m, so planned annual spend = £60m - £6m = £54m. Actual = £56.5m. Behind by £56.5m - £54m = £2.5m. Option A compares against a linear (equal-thirds) phasing; C is the total planned-to-date reduction, not the shortfall; D measures against the final £48m target, which is not due until year 3. Phased trajectories are the standard shape of spending-review commitments, and reading them correctly is essential when you report strategy delivery to the executive - being £2.5m adrift halfway is a very different conversation from being £8.5m adrift.

**Question 13 (hard) - Emerging technology adoption cost curve**

Horizon scanning suggests a new integration technology's unit cost is falling 15% per year, from £200 per unit today. Your organisation would need 5,000 units. Adopting now also incurs a £350,000 early-adopter integration cost, which falls to £150,000 if you wait two years. Ignoring benefits timing, what is the difference in total adoption cost between adopting now and adopting in two years?

A) Adopting now costs £477,500 more
B) Adopting now costs £277,500 more
C) The two options cost the same
D) Adopting in two years costs £200,000 more

**Correct answer: A.**

**Explanation:** Now: 5,000 x £200 = £1,000,000 + £350,000 = £1,350,000. In two years: unit cost = £200 x 0.85 x 0.85 = £200 x 0.7225 = £144.50; units cost 5,000 x £144.50 = £722,500; plus £150,000 integration = £872,500. Difference = £1,350,000 - £872,500 = £477,500. Option B compounds the price decline only one year (£170 per unit); D looks only at the integration-cost difference in the wrong direction. Two disciplines matter: compound the percentage decline (not 30% off), and include both cost components. The strategic judgement - whether two years of foregone benefit outweighs £477,500 - is yours to argue; the assessment tests whether the number you argue from is right.

**Question 14 (easy) - Meeting the community training budget**

You have a £90,000 development budget for your 45-strong architecture community. A certification pathway costs £2,400 per person. You want to certify as many people as possible while retaining at least £15,000 for community events. How many architects can you certify?

A) 37
B) 31
C) 32
D) 30

**Correct answer: B.**

**Explanation:** Available for certification = £90,000 - £15,000 = £75,000. £75,000 / £2,400 = 31.25, and you cannot certify a quarter of a person, so 31. Option A ignores the events reserve (90,000 / 2,400 = 37.5 → 37); C rounds 31.25 up, which would breach the budget by £1,800; D over-rounds down. Two habits: subtract reservations before dividing, and always round down when the unit is a whole person or licence. Growing the community within a real budget makes this the least hypothetical question in this section.

**Question 15 (moderate) - Carbon and cost trade-off for sustainability reporting**

Two data centre options for a workload: Option P consumes 480 MWh per year at £185 per MWh with a carbon intensity of 0.18 tonnes CO2e per MWh. Option Q consumes 520 MWh per year at £160 per MWh with a carbon intensity of 0.05 tonnes CO2e per MWh. Your sustainability standard prices carbon internally at £80 per tonne for decision-making. Including the internal carbon price, which option has the lower total annual decision cost, and by how much?

A) P, by £5,600
B) Q, by £10,432
C) Q, by £5,600
D) P, by £3,312

**Correct answer: B.**

**Explanation:** Option P: energy cost = 480 x £185 = £88,800; carbon = 480 x 0.18 = 86.4 tonnes, priced at 86.4 x £80 = £6,912; total decision cost = £95,712. Option Q: energy cost = 520 x £160 = £83,200; carbon = 520 x 0.05 = 26 tonnes, priced at 26 x £80 = £2,080; total decision cost = £85,280. Q is lower by £95,712 - £85,280 = £10,432. Option C is the energy-cost difference alone (£88,800 - £83,200 = £5,600), the answer you reach if you forget to price the carbon at all; A and D reverse the direction by mishandling Q's higher consumption. Two durable lessons: apply the internal carbon price to both options symmetrically, and remember that higher energy consumption does not automatically mean higher total cost once unit rates and carbon intensity differ. Guiding the organisation on sustainability to achieve value for money depends on exactly this combined cost-and-carbon calculation, which you will present in investment cases and sustainability reports.

### Preparation tips

- **Rebuild your extraction habit.** Most errors at your level are extraction errors, not calculation errors: the wrong row, the wrong year, "per quarter" read as "per year", or a percentage of the wrong base. Before calculating, state to yourself exactly which figures you need and where they are.
- **Practise with the artefacts you already read.** Spending review submissions, supplier pricing schedules, cloud billing reports and benefits dashboards are ideal practice material - convert real figures into questions of the forms above.
- **Master five operations cold.** Percentage change from the correct base; compound growth and decline; weighted averages; expected values across probabilistic branches; and totals over a stated horizon. Nearly every question in a role-specific numeric test for a senior architect is one of these wearing different clothes.
- **Use the calculator for arithmetic, your head for structure.** Decide the calculation shape before touching the calculator; the time cost of a wrong structure is ten times the time cost of slow keying.
- **Sanity-check magnitudes.** A downtime figure of 4.5 minutes versus 45 minutes, a saving of £0.4m versus £4m - order-of-magnitude checks catch decimal slips that plausibility alone will not.

### Common pitfalls

- **Misreading scale qualifiers.** "In thousands", "per quarter", "FTE-months": a single missed qualifier invalidates a perfect calculation. Circle (mentally or literally) every unit before you begin.
- **Percentage-base errors.** Dividing the change by the new value instead of the original, or applying two successive percentages additively rather than compounding. Questions are engineered so those errors land exactly on a wrong option.
- **Over-calculating.** Some questions yield to estimation: if three options are of the wrong magnitude, a rough calculation identifies the answer in seconds. Precision is a tool, not a virtue, under time pressure.
- **The time-sink question.** Multi-branch expected-value items (like Question 10) can absorb five minutes. If you spot one early, consider banking the simpler questions first - test navigation is itself a prioritisation exercise.
- **Forcing a match.** When your computed value is not among the options, do not silently bend your arithmetic towards the nearest choice. Recheck extraction first; if your figure stands, pick the nearest option and move on. In the live workplace, that same discipline - report the discrepancy rather than reconcile it away - protects the integrity of every dashboard you own.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment evaluates how accurately you understand, analyse and draw conclusions from written material of the kind your role actually generates and consumes. The passages are not literary; they are the dense, consequential prose of your working life: architectural principles and standards documents, strategy papers, governance terms of reference, commercial framework guidance, cross-government policy circulars, and emails from senior stakeholders whose exact wording matters.

The dominant format is a passage followed by statements you must classify as **True** (the passage says or necessarily implies it), **False** (the passage contradicts it), or **Cannot Say** (the passage provides insufficient information either way) - answered strictly from the text, ignoring everything you happen to know. Some assessments add multiple-choice comprehension items: identifying the best summary, the author's main claim, or the precise obligation a clause creates. Timing is brisk - often under a minute per question - simulating the reality of absorbing a forty-page strategy paper the evening before a board.

Why does this matter at principal level? Because words are your governance instruments. The difference between "services must use the enterprise identity platform" and "services should normally use the enterprise identity platform" is the difference between a mandate and a preference - and you are the person who writes, interprets and defends such clauses. You mediate difficult architectural discussions in which each side quotes documents selectively; you assure that decisions align with strategy by testing them against the strategy's actual words; you represent architectural governance in legal and commercial forums where imprecise reading has contractual consequences. This assessment measures the precision of reading on which all of that rests.

### What it measures for your role

Mapped against the skills in your role profile:

- **Architecture communication**: extracting exactly what a document claims, so you can communicate it faithfully to technical and non-technical stakeholders at all levels, and mediate accurately when parties dispute what a text means.
- **Making architectural decisions**: distinguishing what a standard mandates, permits and is silent on - the foundation of defensible governance and of representing architecture within legal and commercial governance.
- **Strategy design**: reading strategy documents closely enough to define and connect strategies across the organisation without importing meaning that is not there.
- **Commercial perspective**: parsing contractual framework guidance and supplier terms with the precision that evaluation and selection demand.
- **Architect for the whole context**: reading policy signals and industry analyses accurately - separating what a trend report establishes from what it merely suggests.
- **Problem definition and shaping**: identifying stated requirements versus assumptions in problem statements, and helping others challenge both.

### Practice questions

**Passage 1 - Architectural principles policy (for Questions 1-4)**

"All programmes within the department must submit a conceptual architecture to the Design Authority before their business case is approved. Programmes classified as minor - those with total lifetime cost below £1 million and no new processing of personal data - are exempt from this requirement, though they must still register their intended technology choices in the enterprise repository. The Design Authority will assess conceptual architectures against the department's published principles, and may grant time-limited exceptions to any principle except those relating to security and accessibility, which cannot be waived under any circumstances. Where an exception is granted, the programme must record a remediation plan in the enterprise repository within 20 working days. The Design Authority meets fortnightly, and urgent submissions may be considered out of committee at the discretion of the chair, who is the principal enterprise architect."

**Question 1 (easy)**

True, False, or Cannot Say: "A programme with a lifetime cost of £800,000 that introduces new processing of personal data is exempt from submitting a conceptual architecture."

**Correct answer: False.**

**Explanation:** The exemption requires both conditions: lifetime cost below £1 million *and* no new processing of personal data. This programme meets the cost condition but fails the personal-data condition, so it is not "minor" and is not exempt. The trap is reading the two conditions as alternatives ("or") rather than as a conjunction ("and"). In governance drafting and reading alike, conjunctions and disjunctions are where compliance arguments are won and lost.

**Question 2 (easy)**

True, False, or Cannot Say: "The Design Authority can grant a time-limited exception to the department's accessibility principles."

**Correct answer: False.**

**Explanation:** The passage states exceptions may be granted "to any principle except those relating to security and accessibility, which cannot be waived under any circumstances." An accessibility exception is therefore expressly excluded - the statement contradicts the text. Note how the question tests whether you carried the exclusion clause with you rather than remembering only the permissive headline "may grant time-limited exceptions to any principle". Accessibility as an unwaivable requirement also reflects genuine UK public sector obligations, which is why passages like this feel familiar.

**Question 3 (moderate)**

True, False, or Cannot Say: "The Design Authority meets more often when there are many urgent submissions."

**Correct answer: Cannot Say.**

**Explanation:** The passage says the authority meets fortnightly and that urgent submissions "may be considered out of committee at the discretion of the chair". Out-of-committee consideration is not a meeting, and nothing states that meeting frequency changes with demand. The statement is plausible - many real boards do flex their cadence - but plausibility is precisely what Cannot Say exists to punish. The passage neither confirms nor contradicts the claim, so the disciplined answer is Cannot Say. Bringing outside operational knowledge into the text is the single most common verbal reasoning error among experienced professionals, because your experience is usually right - just not admissible.

**Question 4 (moderate)**

True, False, or Cannot Say: "A minor programme granted an exception must record a remediation plan within 20 working days."

**Correct answer: Cannot Say.**

**Explanation:** Follow the logic of the passage carefully. Minor programmes are exempt from submitting conceptual architectures; exceptions are granted in the course of the Design Authority assessing conceptual architectures. The passage never describes a route by which a minor programme would receive an exception, so the premise of the statement sits outside what the text establishes. It does not contradict the passage (False would overreach), and it is not confirmed by it (True would overreach) - the passage simply does not address exceptions for minor programmes. Cannot Say. This is a subtle item: the 20-day requirement is genuinely in the text, which lures you towards True; the question is whether the *whole* conditional statement is supported.

**Passage 2 - Strategy paper extract (for Questions 5-8)**

"The department's target architecture will consolidate eleven case management systems onto a single platform by 2029. Consolidation is expected to reduce annual licence spend by £6.2 million and to release an estimated 40 full-time-equivalent staff from duplicative support activity, who will be redeployed to priority services. The programme's first tranche, covering the three largest systems, begins next April and carries the majority of the technical risk, as these systems hold the department's oldest data. Early market engagement suggests at least four suppliers could deliver the platform, though no procurement decision has been taken. The consolidation depends on the successful completion of the data standards workstream, which is currently rated amber. Should the data standards workstream fail, the consolidation timeline would need to be reassessed."

**Question 5 (easy)**

True, False, or Cannot Say: "The consolidation programme will reduce annual licence spend by £6.2 million."

**Correct answer: Cannot Say.**

**Explanation:** The passage says consolidation "is expected to reduce" annual licence spend by £6.2 million. An expectation is not an accomplished or guaranteed fact; the statement as worded asserts the reduction *will* happen. The text neither guarantees the saving (so not True) nor casts doubt on it (so not False). This modality distinction - "will" versus "is expected to", "must" versus "should" - is a signature verbal reasoning test point, and it is also the exact skill you use when assuring benefits claims in business cases: expected benefits are hypotheses, not facts, and your reading should never quietly upgrade them.

**Question 6 (moderate)**

True, False, or Cannot Say: "The first tranche includes the systems holding the department's oldest data."

**Correct answer: True.**

**Explanation:** The passage states the first tranche covers "the three largest systems" and that it "carries the majority of the technical risk, as these systems hold the department's oldest data". The connective "as these systems" ties the oldest data directly to the tranche-one systems. The statement is therefore established by the text. Notice what makes this item easy to get wrong at speed: the age of data is mentioned in a subordinate clause explaining risk, not in the main description of the tranche - accurate reading means harvesting facts wherever the sentence deposits them.

**Question 7 (moderate)**

True, False, or Cannot Say: "A procurement framework has been selected for the platform."

**Correct answer: Cannot Say.**

**Explanation:** The passage reports early market engagement and that "at least four suppliers could deliver the platform, though no procurement decision has been taken." No procurement *decision* has been taken - but the statement asks about selecting a procurement *framework*. Is framework selection a procurement decision? The text does not define the boundary, and a careful reader does not supply one. Nothing confirms a framework has been selected; nothing explicitly denies it unless you equate the two terms, which the passage does not license. Cannot Say. If you answered False, you made a defensible-sounding leap - and defensible-sounding leaps are what this format is engineered to detect, just as commercial documents in real life punish readers who treat adjacent terms as synonyms.

**Question 8 (hard)**

Which of the following best states the logical relationship the passage establishes between the data standards workstream and the consolidation?

A) The consolidation cannot begin until the data standards workstream completes
B) The consolidation's success depends on the data standards workstream, and failure of that workstream would trigger a timeline reassessment
C) The data standards workstream is rated amber because of consolidation risks
D) The consolidation will fail if the data standards workstream remains amber

**Correct answer: B.**

**Explanation:** The passage states: "The consolidation depends on the successful completion of the data standards workstream" and "Should the data standards workstream fail, the consolidation timeline would need to be reassessed." B restates both claims without addition. A converts a dependency for overall success into a sequencing constraint on *beginning* - the text says tranche one begins next April regardless. C reverses the direction of explanation: the passage never says why the workstream is amber. D escalates "timeline would need to be reassessed" into "will fail", and converts the current amber rating into failure. Reading dependencies precisely - what depends on what, and what consequence follows from what trigger - is the daily work of owning transition states and assuring strategy delivery.

**Passage 3 - Commercial framework guidance (for Questions 9-11)**

"Departments procuring cloud services should use the Crown framework as the default route. Use of an alternative route is permitted only where the department can demonstrate that the framework cannot meet an essential requirement, and such use must be approved by the commercial director before contract award. Framework call-off contracts are limited to a maximum initial term of 36 months, extendable once by up to 12 months where the extension delivers demonstrable value for money. Suppliers on the framework have committed to the government's supply chain transparency standards; departments remain responsible for verifying compliance for their specific call-off. Nothing in this guidance removes a department's obligations under public procurement regulations."

**Question 9 (easy)**

True, False, or Cannot Say: "A department may use an alternative procurement route without any approval, provided the framework cannot meet an essential requirement."

**Correct answer: False.**

**Explanation:** The passage imposes two conditions for an alternative route: demonstrating that the framework cannot meet an essential requirement, *and* approval by the commercial director before contract award. The statement claims the first condition alone suffices "without any approval", directly contradicting the approval requirement. When you advise programmes on contractual routes, this compound-condition structure - substantive test plus authorisation step - is the norm, and collapsing it to a single condition is exactly the misreading that creates procurement risk.

**Question 10 (moderate)**

True, False, or Cannot Say: "The maximum total duration of a framework call-off contract, including any extension, is 48 months."

**Correct answer: True.**

**Explanation:** The passage limits the initial term to a maximum of 36 months, "extendable once by up to 12 months". Maximum total = 36 + 12 = 48 months, and "extendable once" excludes stacking further extensions. The statement follows necessarily from the text - this is True by arithmetic-on-the-words, a hybrid item style common in role-specific tests for senior professionals. Note the qualifier discipline: the extension is conditional on demonstrable value for money, but the statement asks only about the *maximum possible* duration, so the condition does not disturb the conclusion.

**Question 11 (hard)**

True, False, or Cannot Say: "Because framework suppliers have committed to supply chain transparency standards, departments need not verify transparency compliance for their own call-offs."

**Correct answer: False.**

**Explanation:** The passage states the suppliers' commitment and then immediately assigns residual responsibility: "departments remain responsible for verifying compliance for their specific call-off." The statement's inference - commitment implies no verification duty - is the precise inference the text forecloses. This pattern, where a general assurance coexists with an undiminished local duty, recurs throughout government commercial and security documents; assessments use it because weaker readers let the reassuring first clause eclipse the obligating second clause. As the person representing architectural governance within commercial governance, you will often be the one reminding a programme board that the second clause exists.

**Passage 4 - Email from a director-general (for Questions 12-14)**

"Thank you for the enterprise architecture roadmap. I support the overall direction, particularly the emphasis on reusing cross-government platforms. However, I am not yet persuaded by the proposed pace of legacy decommissioning: the paper assumes stable funding across the spending review period, which is not an assumption I can endorse at this stage. Before I put this to the executive committee, I would like the architecture team to model a variant in which capital funding falls by a fifth from year two, and to indicate which decommissioning milestones would move and by how long. I would also welcome a clearer articulation of the risks of *not* proceeding at the proposed pace, as I suspect the committee will focus on the costs of action and underweight the costs of inaction."

**Question 12 (easy)**

True, False, or Cannot Say: "The director-general opposes the roadmap's emphasis on reuse."

**Correct answer: False.**

**Explanation:** The email says: "I support the overall direction, particularly the emphasis on reusing cross-government platforms." The statement asserts the opposite of an explicit endorsement - "particularly" marks reuse as the element most supported, not opposed. Fast readers sometimes tag the whole email as critical because its centre of gravity is a challenge; accurate reading separates what the sender supports, what they question, and what they request. That triage is precisely how you should read - and write - senior stakeholder correspondence.

**Question 13 (moderate)**

True, False, or Cannot Say: "The director-general has rejected the assumption of stable funding."

**Correct answer: False.**

**Explanation:** The wording is "not an assumption I can endorse at this stage" - a withholding of endorsement, explicitly time-qualified, not a rejection. The email then commissions analysis of a downside variant, which is consistent with keeping both funding scenarios open. "Has rejected" contradicts the deliberately suspended position the text states. This distinction is not pedantry: briefing your team that the DG "rejected" the funding assumption would send them to redraft the wrong document. Senior communication runs on exactly these graduated verbs - endorse, support, not yet persuaded, cannot endorse at this stage - and verbal reasoning tests reward candidates who refuse to round them off.

**Question 14 (moderate)**

What does the director-general ask the architecture team to produce? Select the most complete and accurate answer.

A) A revised roadmap with slower decommissioning
B) A funding-reduction variant showing a 20% capital fall from year two, the affected decommissioning milestones and their delays, plus a clearer articulation of the risks of not proceeding at the proposed pace
C) A business case for stable funding across the spending review period
D) A paper for the executive committee on the costs of inaction

**Correct answer: B.**

**Explanation:** The email contains two requests: model a variant "in which capital funding falls by a fifth from year two" indicating "which decommissioning milestones would move and by how long", and provide "a clearer articulation of the risks of *not* proceeding at the proposed pace". B captures both, translating "a fifth" correctly as 20%. A invents a decision the DG has not made - they asked for analysis, not a slower roadmap. C reverses the request: the DG questions stable funding rather than seeking a case for it. D confuses the DG's prediction about the committee's focus with a commissioned deliverable. Extracting a complete, faithful action list from senior correspondence is a core architecture communication skill - incomplete extraction ("we did the funding variant") is how teams disappoint stakeholders while believing they complied.

**Passage 5 - Industry trend report extract (for Questions 15-16)**

"Adoption of digital twin technology among European public sector organisations doubled between 2023 and 2025, although it remains concentrated in transport and utilities. Analysts attribute the acceleration primarily to falling sensor and integration costs, with regulatory pressure a secondary factor. Organisations reporting the greatest value from digital twins were those that had first invested in data governance: twins built on poorly governed data frequently produced confident but misleading operational pictures. The report cautions that vendor claims about 'out of the box' twins should be treated with scepticism, since in every case studied, integration effort exceeded initial vendor estimates. The report does not examine central government departments specifically."

**Question 15 (moderate)**

True, False, or Cannot Say: "Central government departments that adopt digital twins experience integration effort exceeding vendor estimates."

**Correct answer: Cannot Say.**

**Explanation:** The report found that integration effort exceeded vendor estimates "in every case studied" - but its final sentence states it "does not examine central government departments specifically." The statement asks about a population the report explicitly excludes from its evidence base. Generalising from studied cases to an unstudied population may be reasonable professional judgement - indeed, as the owner of a departmental Digital Twin, you would prudently *plan* for integration overruns - but verbal reasoning verdicts are about what the text establishes, and the text deliberately fences off this population. Cannot Say. This item rehearses a horizon-scanning discipline: when you brief the board on industry trends, distinguishing "the evidence covers us" from "the evidence is suggestive for us" is what makes your briefings trustworthy.

**Question 16 (hard)**

Which conclusion is best supported by the passage?

A) Regulatory pressure is the main driver of digital twin adoption
B) Digital twins produce misleading operational pictures
C) Prior investment in data governance was associated with greater reported value from digital twins
D) Public sector digital twin adoption doubled in transport and utilities between 2023 and 2025

**Correct answer: C.**

**Explanation:** The passage states that organisations "reporting the greatest value... were those that had first invested in data governance" - C restates this association precisely, without upgrading it to causation. A inverts the stated ranking: falling costs were primary, regulation secondary. B strips a conditional finding of its condition - only twins "built on poorly governed data" frequently misled. D relocates the doubling: adoption doubled across European public sector organisations overall, while transport and utilities describe where adoption is *concentrated*, not where it doubled. Each wrong option is a subtle misassignment of a true fragment - the exact failure mode of hurried executive summaries, and the reason your role profile pairs horizon scanning with the judgement to report it accurately.

### Preparation tips

- **Train the three-way verdict.** True/False/Cannot Say is a discipline, not a reading style you already have. Practise daily with short passages: the key move is asking "does the text *establish* this?" rather than "is this *believable*?". At your level of expertise, Cannot Say is the answer you will most often get wrong, because you know too much.
- **Read the statement first, then hunt.** Under time pressure, read the question statement, identify its load-bearing terms, and scan the passage for exactly those terms and their qualifiers. Full leisurely reading of every passage is a luxury the clock rarely allows.
- **Mark modality and quantifiers as you read.** "Must", "should", "may", "expected to", "all", "only", "unless", "at this stage" - these small words decide most answers. This mirrors how you already read standards and contracts; the assessment simply measures whether you do it reliably at speed.
- **Practise on your own corpus.** Take a real principles document, framework guidance note or strategy paper and write five True/False/Cannot Say statements about it. Writing items teaches you to see the traps from the setter's side - and sharpens your own governance drafting.
- **Protect your pace.** Around 45-60 seconds per item: if a verdict will not settle, choose your best answer, note it, and move on. A flagged guess costs one mark at most; a three-minute deliberation costs three questions.
- **Rehearse the two overreach checks.** Before answering True, ask: does the passage establish *every* element of the statement, including its conditions and its population? Before answering False, ask: does the passage actually *contradict* the statement, or merely fail to support it? Most wrong answers at senior level are overreaches in one of these two directions, and the two questions take five seconds each. Statements built from true fragments wrongly combined - the right fact attached to the wrong population, condition or timeframe - are the setter's favourite construction, and only element-by-element checking defeats them.

### Common pitfalls

- **Importing expert knowledge.** You know how design authorities, procurement frameworks and spending reviews actually behave. The test's universe is the passage alone; every time your experience supplies a missing fact, you drift from True or False towards an unearned verdict. Cannot Say exists precisely for statements your experience wants to confirm.
- **Rounding off modality.** Upgrading "is expected to" into "will", "not yet persuaded" into "rejects", or "should normally" into "must". The passage's hedges are data, not noise.
- **Letting the reassuring clause eclipse the obligating clause.** Compound sentences often grant with one hand and oblige with the other; weaker readers remember the grant. Read to the full stop.
- **Treating adjacent terms as synonyms.** "Procurement decision" versus "procurement framework", "meeting" versus "out-of-committee consideration", "exemption" versus "exception". Precision about near-synonyms is both a test discipline and the daily grammar of governance.
- **Verdict drift across a question set.** After three consecutive Cannot Say answers, candidates start avoiding it, suspecting a pattern. Item writers know this. Judge each statement on its own text - the same independence you would demand of an assurance review.

## Workplace job-specific situational judgement assessment

### About this assessment

A workplace job-specific situational judgement assessment evaluates decision-making, interpersonal skill and professional conduct by presenting realistic workplace dilemmas and asking which responses are most and least effective. Unlike the cognitive, numeric and verbal assessments, there is rarely a single objectively right answer; instead, responses are scored against the values and behaviours the organisation needs from someone in your role. Formats vary: choose the most effective and least effective actions from four or five options; rank all options from best to worst; or rate each option's effectiveness on a scale. Timing is usually generous or absent, because the assessment targets natural judgement rather than speed.

For a principal enterprise architect, the scenarios are political, strategic and human: a director-general who wants to bypass governance, two departments at war over a shared platform, a supplier relationship souring at the worst moment, an architecture community losing faith in its leadership, a horizon-scanning insight nobody wants to hear. Your role profile is explicit that you network and communicate with senior stakeholders, mediate difficult architectural discussions, unblock issues between departments at the highest level, and inspire other architects. Situational judgement assessments sample precisely those behaviours.

Scoring in UK public sector contexts typically rewards options that serve user needs and the long-term public interest, act transparently, collaborate rather than command, uphold standards without rigidity, address problems at their root, and develop others. Options that are passive, evasive, political in the self-serving sense, or that sacrifice long-term integrity for short-term comfort score poorly - as do idealistic options that ignore practical reality.

### What it measures for your role

Mapped against the skills in your role profile:

- **Architecture communication**: gaining support from business and technical stakeholders for high-risk, high-impact architectural positions; mediating between people in difficult architectural discussions.
- **Community collaboration**: solving and unblocking issues between teams or departments at the highest level; coaching on team dynamics and conflict resolution while building the community.
- **Making architectural decisions**: holding a defensible line under pressure; leading and evolving governance without becoming an obstacle; escalating well.
- **Strategy design** and **Enterprise architecture**: protecting the long-term strategy while enabling delivery at pace; advocating for resources and removing blockers.
- **Commercial perspective**: handling supplier relationships and evaluations with integrity.
- **Architect for the whole context** and **Problem definition and shaping**: responding to external signals wisely, and refusing to solve the wrong problem quickly.

### Practice questions

**Question 1 (moderate) - The DG wants to skip governance**

A director-general sponsoring a politically high-profile programme tells you the programme will not submit its solution architecture to the design authority: "We don't have time for your committee - the minister has announced the date." The architecture, from what you have glimpsed, duplicates an existing cross-government platform.

A) Agree to waive the review, given the ministerial commitment, and note your concerns in an email for the record.
B) Insist the programme joins the next scheduled design authority meeting and warn that you will escalate non-attendance to the permanent secretary.
C) Offer an expedited, focused review within the week - out of committee, under your chair's discretion - targeting only the highest-risk decisions, including the apparent duplication, and explain that this protects the minister's date better than discovering the duplication in eighteen months.
D) Ask your team to review the architecture quietly from the documents you can obtain, without telling the DG, and raise issues only if you find something serious.

**Most effective: C. Least effective: A.**

**Explanation:** C demonstrates the judgement your role exists to provide: governance that flexes its process while holding its purpose. It uses a legitimate mechanism (urgent out-of-committee consideration), concentrates scrutiny where risk lives, and - critically - reframes governance as protecting the DG's own objective, which is how you gain support from senior stakeholders for high-risk topics. A is least effective: it converts your accountability into a defensive paper trail, abandons the value-for-money duty to challenge duplication, and teaches every future programme that ministerial announcements dissolve assurance. B holds the line but rigidly: leading with escalation threats damages a senior relationship you need, and treats process as the point rather than the risk. D is covert and passive - reviewing without access or candour produces weak assurance and, if discovered, corrodes the transparency on which your influence depends.

**Question 2 (moderate) - Two departments, one platform, open warfare**

Two departments co-fund a shared integration platform. Department X accuses Department Y of consuming disproportionate capacity; Y accuses X of blocking its releases. Both have escalated to you, each demanding you rule in their favour, and both have hinted they will withdraw funding if the ruling goes against them. Your analysis suggests the platform's real problem is an outdated capacity model that neither department has seen.

A) Rule quickly in favour of the department whose case is marginally stronger, to show governance is decisive.
B) Convene both departments' leads, share the capacity analysis openly, and facilitate agreement on a revised capacity model and funding formula - explicitly framing the platform as a shared asset whose failure harms both.
C) Escalate the dispute to the chief digital officer to make the ruling, since funding threats exceed your authority.
D) Propose splitting the platform so each department controls its own instance, ending the conflict permanently.

**Most effective: B. Least effective: D.**

**Explanation:** B is the textbook expression of your role profile: solving and unblocking issues between departments at the highest level, mediating difficult discussions, and using evidence to move a conflict from positions ("rule for me") to interests (a platform both can rely on). Sharing the analysis openly models transparency and dissolves the zero-sum framing. D is least effective: it resolves the interpersonal conflict by destroying the enterprise asset - duplicating infrastructure, doubling run costs, and contradicting reuse and value-for-money principles; it is the seductive option because it ends the noise, which is exactly why assessments include it. A decides on the wrong basis (decisiveness over root cause) and leaves the capacity-model defect to regenerate conflict. C prematurely surrenders a dispute you have both the mandate and the analysis to resolve; escalation may come later, but as a considered step, not a reflex.

**Question 3 (hard) - The strategy you inherited is wrong**

Three months into your post, your horizon scanning and supplier analysis convince you that a central pillar of the enterprise strategy - a five-year commitment to a particular platform ecosystem, agreed by the executive committee last year - is becoming a strategic risk: the vendor's roadmap has pivoted away from your use cases and its UK public sector investment is shrinking. Your predecessor championed the commitment, several senior stakeholders are invested in it, and delivery teams are mid-migration.

A) Continue implementing the agreed strategy; revisiting an executive decision after one year would undermine confidence in architectural leadership.
B) Prepare a concise evidence pack - vendor roadmap shifts, investment signals, exposure analysis and costed options including staying the course - test it with the CDO and one or two trusted stakeholders, then bring a recommendation to the executive committee for a strategy review.
C) Quietly instruct architects to steer new designs away from the ecosystem while the official strategy remains unchanged, avoiding a difficult executive conversation.
D) Announce at the next architecture community meeting that the strategy is no longer sound and that a change of direction is coming.

**Most effective: B. Least effective: C.**

**Explanation:** B does what "responsible for ensuring the strategy is developed, agreed and followed" actually means: strategy is a living decision, and the same governance that agreed it is the legitimate route to revising it. Evidence first, options honestly costed (including "stay the course" - real options analysis is not advocacy), soundings taken to test the argument and build support, then the formal forum. This is horizon scanning converted into strategic action. C is least effective: it creates a shadow strategy - official documents say one thing, real guidance says another - destroying the assurance function you lead, confusing delivery teams mid-migration, and hiding a material risk from the executives accountable for it. A confuses stewardship with inertia; leadership credibility suffers more from riding a known-bad commitment than from correcting one. D is honest but wrongly sequenced: announcing a strategy change to the community before the executive has decided undermines the executive, alarms delivery teams, and could leak - candour without process is not transparency.

**Question 4 (moderate) - The supplier evaluation you are pressured to tilt**

You are the architectural authority on a supplier evaluation panel for a major platform. A senior commercial colleague suggests, informally, that the incumbent supplier "would be the smoothest outcome" and asks whether your technical scoring "has any flexibility", noting the incumbent's transition costs would be lower.

A) Score all bids strictly against the published criteria, document your rationale, and tell your colleague plainly that scores are not flexible - while noting that transition cost, if it is a legitimate factor, belongs in the weighted criteria openly, not in adjusted technical scores.
B) Adjust your technical scores marginally within defensible bounds, since transition cost is a genuine consideration and the difference is small.
C) Report your colleague to the commercial director immediately for attempting to influence the evaluation.
D) Withdraw from the panel to avoid any appearance of impropriety.

**Most effective: A. Least effective: B.**

**Explanation:** A holds the two lines that matter: evaluation integrity (scores reflect evidence against published criteria - the foundation of lawful, fair procurement) and constructive redirection (if transition cost matters, the transparent remedy is to weight it openly, a genuinely useful commercial-perspective insight). It also handles the colleague directly and proportionately, preserving the working relationship while leaving no ambiguity. B is least effective: "marginal flexibility" in scoring is precisely how procurement challenge and legal risk are born; a small dishonesty in a regulated process is not small. C escalates before communicating - the informal comment deserves a clear direct response first, with escalation held in reserve if pressure persists or hardens. D abandons the panel's architectural expertise, solving your reputational exposure by degrading the evaluation - withdrawal is for genuine conflicts of interest, not for moments that require a spine.

**Question 5 (moderate) - The community is fracturing**

Your architecture community survey shows morale falling: solution architects in delivery programmes say enterprise architecture "issues edicts from the centre", governance feels like "marking homework", and two respected architects have resigned citing lack of growth. Your principals disagree about the response: one urges tightening standards enforcement, another suggests disbanding central review entirely.

A) Run a series of listening sessions, then co-design changes with the community: rotate delivery architects through governance panels, create explicit development pathways, and shift reviews towards earlier, collaborative engagement - reporting back publicly on what changed and why.
B) Tighten enforcement: falling morale does not change the fact that standards exist to be followed, and consistency will restore respect.
C) Disband central review and devolve architectural decisions fully to programmes, eliminating the source of resentment.
D) Commission an external consultancy to review the architecture operating model and await its report before acting.

**Most effective: A. Least effective: C.**

**Explanation:** A embodies the community leadership your role profile demands: developing the architecture community, coaching on team dynamics, inspiring other architects and supporting multiple communities and teams. Its specific moves matter - rotating delivery architects through governance converts critics into participants; development pathways answer the resignation signal; earlier engagement changes governance from inspection to collaboration; public report-back builds the trust that surveys alone never do. C is least effective: it abolishes the assurance mechanism the organisation needs (and your role is accountable for) to appease sentiment - organisation-wide alignment with strategy does not happen by hope. B misdiagnoses a relationship problem as a compliance problem and will accelerate the resignations. D is not wrong to seek evidence, but as the whole response it outsources leadership and delays action on signals that are already clear enough to act on - external perspective can support, not replace, your engagement.

**Question 6 (hard) - Delivery at pace versus the transition plan**

A flagship service must meet a legally mandated go-live in four months. Its programme director asks your blessing for a tactical solution that bypasses the enterprise integration platform, writing directly to a legacy database that your transition plan retires next year. Without the tactical route, the programme will likely miss the statutory date; with it, the decommissioning on which two other programmes depend may slip.

A) Refuse: the transition plan protects the whole enterprise, and one programme's deadline cannot compromise it.
B) Approve the tactical solution as an explicit, time-limited architectural exception - with a funded remediation plan agreed now, decommissioning impact assessed and communicated to the two dependent programmes, and the exception recorded and tracked through governance.
C) Approve it informally to keep things moving, and rely on the programme's goodwill to fix it later.
D) Tell the programme director to take the choice to the executive committee, since statutory deadlines versus architecture is not yours to weigh.

**Most effective: B. Least effective: C.**

**Explanation:** B is architectural governance working as designed: enabling delivery at pace while managing enterprise risk explicitly. The elements are the answer - *time-limited* and *funded remediation agreed now* prevent the tactical becoming permanent (the fate of most undocumented workarounds); impact assessment and communication to dependent programmes honours your cross-portfolio accountability; formal recording keeps the exception visible and enforceable. A treats the plan as more important than the outcomes it serves; a statutory obligation missed for architectural purity is a failure of judgement, not a triumph of standards. D abdicates: weighing exactly these trade-offs is what a principal enterprise architect is for - you may still inform the executive, but with a recommendation, not a shrug. C is least effective: an informal approval creates unmanaged risk, invisible to governance, with no lever when "later" never comes - it is A's opposite vice, and more common.

**Question 7 (moderate) - The emerging technology bandwagon**

Following intense media coverage, your CDO asks you to "get us an agentic AI strategy by month end" and suggests announcing three flagship AI deployments at a sector conference. Your horizon scanning suggests genuine medium-term potential, but the proposed deployments target services whose data quality you know to be poor, and no assurance framework for AI decisions yet exists in your organisation.

A) Deliver what is asked: draft the strategy and support the three announcements - momentum and visible ambition attract funding.
B) Advise the CDO against any AI work until data quality and assurance frameworks are fully mature.
C) Bring the CDO a differentiated proposal: announce a credible programme that starts with one deployment on a well-governed service, pairs it with building the AI assurance framework and a data-quality remediation for the weaker services, and positions the organisation as responsibly ambitious - and be candid about why the original three deployments would likely fail publicly.
D) Draft the strategy as requested, but privately brief your architecture community that the deployments should be slow-walked.

**Most effective: C. Least effective: D.**

**Explanation:** C is horizon scanning discharged with integrity: it neither surfs the hype (A) nor hides behind caution (B), but converts an executive's enthusiasm into a sequenced, evidence-based programme - identifying the real trend and its opportunity while being candid about failure modes on poorly governed data. It gives the CDO a *better* announcement, which is what gaining support from stakeholders for complex topics looks like in practice. A sets the organisation up for visible failure on your professional advice - the medium-term cost to both the mission and your credibility dwarfs the short-term comfort. B overcorrects: "nothing until everything is mature" ignores the option of starting safely and building maturity in parallel, and will simply cause the work to happen without you. D is least effective: formally complying while covertly undermining is the worst of both worlds - dishonest to the CDO, corrosive to the community you are asking to conspire, and fatal to trust when it surfaces, as it will.

**Question 8 (moderate) - The cross-government standards request**

A cross-government working group invites you to help shape a new interoperability standard. Participation would consume meaningful time from you and two of your best architects, with no direct benefit to this year's delivery commitments. Your own department's adoption of the standard, once published, would eventually be mandatory. Your delivery directors object to losing the capacity.

A) Decline: your obligation is to your department's delivery commitments, and the standard will arrive whether or not you help shape it.
B) Participate personally at a minimal level, but keep your architects fully on delivery.
C) Commit yourself and one architect, negotiating with delivery directors by making the exchange explicit: influence over a standard the department must eventually adopt is cheaper than retrofitting to a standard shaped without you - and the assignment develops the architect.
D) Send your two best architects full-time and absorb the delivery impact without discussion.

**Most effective: C. Least effective: A.**

**Explanation:** C reflects several strands of your role profile at once: working with people outside your organisation to inform policies, strategies and standards; anticipating policy change and building resilience; advocating for resources; and developing the community through a genuinely stretching assignment. Crucially, it treats the delivery directors as stakeholders to persuade with an argument - the retrofit-cost logic - rather than as obstacles. A is least effective precisely because the standard *will* arrive regardless: declining trades permanent influence over a future mandatory constraint for temporary delivery comfort, the definition of strategic short-sightedness in a role charged with the long-term view. B keeps a token seat but forfeits the development opportunity and most of the influence. D gets the participation right and the leadership wrong: absorbing significant capacity loss "without discussion" ignores legitimate delivery concerns and spends trust you will need later.

**Question 9 (hard) - The Digital Twin tells an unwelcome truth**

Your Digital Twin's consolidated view reveals that a major programme's reported status - green, on budget - is inconsistent with its actual resource consumption and integration progress, which suggest a six-month slippage. The programme director, a peer with strong executive relationships, tells you the Twin's data "must be wrong", declines to investigate, and asks you not to raise it before their gateway review in three weeks.

A) Agree to wait until after the gateway review, since the programme director knows their programme best.
B) Verify the Twin's data lineage and calculations first; if the finding stands, share the analysis with the programme director and offer to investigate discrepancies jointly before the review - being clear that if the divergence cannot be reconciled, you are obliged to ensure the gateway review sees accurate data.
C) Email the gateway review panel immediately with the Twin's findings, copying the programme director.
D) Quietly adjust the Twin's dashboard to exclude the disputed programme, pending resolution.

**Most effective: B. Least effective: D.**

**Explanation:** B sequences integrity correctly. First, verify - the programme director's challenge that the data "must be wrong" deserves a genuine test, and your accountability for the Twin's maintenance means its credibility rests on exactly such verification. Second, engage the peer with evidence and a collaborative offer - mediation before escalation. Third, state the boundary transparently: a gateway review proceeding on data you know to be misleading implicates your professional integrity, and saying so plainly is respectful, not hostile. D is least effective: suppressing inconvenient data from the organisation's decision-support asset is the one act that destroys the Twin's entire purpose - worse than any single wrong number, because it makes the instrument itself untrustworthy. A converts a three-week delay into complicity with a potentially misleading review. C is transparent but skips verification and peer engagement, maximising relationship damage while risking that you escalate a data error.

**Question 10 (moderate) - Coaching a struggling enterprise architect**

An enterprise architect you manage has excellent technical judgement but is losing stakeholder support: their design authority interventions are experienced as lectures, and a programme director has asked for them to be replaced on a key programme. The architect believes the stakeholders are the problem.

A) Replace them on the programme as requested and reassign them to internal standards work where interpersonal friction matters less.
B) Share the specific feedback candidly, help them see the pattern, and coach them: observe their next sessions, model reframing techniques yourself, agree behavioural changes to practise, and review progress - while asking the programme director for a defined period to demonstrate change.
C) Defend your architect to the programme director: technical rigour inevitably creates friction, and stakeholders must adapt.
D) Send them on a communication training course and consider the matter addressed.

**Most effective: B. Least effective: C.**

**Explanation:** B is what "coach and support others in architecture communication" and "inspire other enterprise architects" mean in practice: specific feedback (not vague encouragement), joint diagnosis of the pattern the architect cannot yet see, active modelling by you - the community's most senior communicator - deliberate practice, and a negotiated runway with the stakeholder, which also respects the programme director's legitimate concern. A solves this quarter's friction by discarding a developable person and telling your community that stakeholder difficulties end careers rather than trigger support. C is least effective: it endorses the architect's own misdiagnosis, alienates a programme director whose request was not unreasonable, and abandons the coaching duty entirely - technical rigour and stakeholder respect are complements, not substitutes, and pretending otherwise is the oldest failure mode in architecture. D mistakes an input for an outcome; unaccompanied training rarely shifts behaviour that feedback and practice have not touched.

**Question 11 (hard) - Ranking under funding pressure**

Mid-year budget cuts force you to drop one of four enterprise architecture commitments. Rank the options from most defensible to least defensible cut:

1. Pause the reference architecture refresh for a stable, well-understood domain.
2. Cancel the architecture community's development programme for the year.
3. Stop horizon scanning and external engagement for two quarters.
4. Suspend architectural assurance reviews for in-flight programmes.

A) 1, 3, 2, 4
B) 4, 1, 2, 3
C) 1, 2, 3, 4
D) 3, 1, 4, 2

**Most defensible ranking: A (1, 3, 2, 4).**

**Explanation:** Work by marginal risk. Option 1 is the most defensible cut: a stable, well-understood domain's documentation refresh has the lowest cost of delay - the knowledge exists; the artefact is merely ageing. Option 3 is painful but time-bounded: two quarters of reduced horizon scanning raises the risk of missing an external signal, yet the capability restarts intact - though at principal level you would keep a minimal personal watch regardless. Option 2 cuts deeper: cancelling development for a year sends a lasting signal to a community whose morale and retention you steward, and capability lost to resignations does not restart on budget recovery - which is why it ranks as less defensible than the time-bounded scanning pause. Option 4 is the least defensible: suspending assurance for in-flight programmes removes risk control exactly where money is being spent fastest, and undetected architectural failures compound - the cut that costs most precisely when budgets are tightest. Rankings like this test whether you can articulate *why* one harm exceeds another: cost of delay, reversibility, signal effects and risk exposure, not sentiment.

**Question 12 (moderate) - The minister's advisor wants a name**

At a cross-government event, a special advisor asks you informally which of two departments' architectural approaches is "better", making clear the answer may inform a ministerial view on where a new flagship service should be built. You know both architectures well; one is genuinely stronger for this service's needs, but the comparison is nuanced and the weaker department is six months into promising improvements.

A) Name the stronger department plainly - candour with decision-makers is part of the job.
B) Decline to compare departments and change the subject.
C) Offer the substance rather than a verdict: describe the service's architectural requirements, the strengths each department brings against them and the trajectory of both, and offer a proper written assessment through the appropriate channel if the comparison is genuinely informing the decision.
D) Praise both departments equally to avoid any risk.

**Most effective: C. Least effective: D.**

**Explanation:** C threads the needle that senior architects must thread constantly: being genuinely useful to decision-makers while keeping consequential advice within channels that allow nuance, evidence and fairness. An informal verdict at an event (A) strips out exactly the context - service-specific fit, improvement trajectory - that makes your judgement worth having, and a hallway sentence may travel further and harder than you intend; candour is right, but candour includes the caveats. D is least effective because it is a small dishonesty: you *do* have a professional view, and flattening it into diplomatic mush deprives the decision of the expertise your role exists to provide - while still leaving the advisor to decide on worse information. B is honest but unhelpfully closed; declining to answer *and* declining to offer a proper route abandons influence your organisation needs you to exercise. Networking and communicating with senior stakeholders across enterprises means exactly this: substance over verdicts, channels over corridors, usefulness over evasion.

### Preparation tips

- **Anchor on the role, not on yourself.** Answer as the principal enterprise architect the organisation needs, exercising the accountabilities in your role profile - community development, strategy stewardship, governance integrity - even where your personal style might differ.
- **Look for the option that fixes the root cause and preserves the relationship.** Strong options usually combine candour, evidence, an appropriate channel and a constructive path forward. If an option is honest but relationship-destroying, or smooth but evasive, keep looking.
- **Check the sequencing.** Many scenarios turn on order: verify before challenging, engage the peer before escalating, take soundings before the committee, respond directly before reporting. The right actions in the wrong order score as poorly as wrong actions.
- **Beware the seductive extremes.** The rigid enforcement option and the total capitulation option are both usually wrong; so are "quietly work around it" options - covert action almost always scores worst in public sector scoring, because it defeats transparency.
- **Rehearse with real dilemmas.** Take three difficult situations from your own last year and write four response options for each, then rank them and articulate why. The articulation - cost of delay, reversibility, trust effects - is the skill being scored.

### Common pitfalls

- **Choosing the idealistic answer over the effective one.** "Refuse all compromise on standards" sounds principled but ignores the statutory deadline, the user need or the political reality. Assessors at this level score for wise trade-offs, not purity.
- **Selecting passive or deferring options.** Waiting for the consultancy report, passing the decision to the executive, agreeing to stay silent for three weeks - options that delay, defer or delegate the core judgement consistently score poorly for a role defined by leading at the highest level.
- **Covert workarounds.** Shadow strategies, quiet dashboard edits, informal approvals and private slow-walking instructions appear in these assessments because they are common in real organisations - and they are reliably the least effective option against public sector values of transparency and accountability.
- **Ignoring the development dimension.** Scenarios involving your community or your architects almost always contain a coaching opportunity; options that discard people or skip the feedback conversation miss behaviours your role profile names explicitly.
- **Forgetting whose values are being scored.** UK public sector scoring rewards user needs, value for money, transparency, collaboration, accessibility and inclusion. If two options both seem effective, prefer the one a citizen watching the decision would trust more.

## Conclusion

Well done for working through this resource. You have covered the four assessment types most relevant to your role: cognitive reasoning with the roadmaps, decision logs, dependency chains and Digital Twin data you genuinely own; numeric reasoning across supplier evaluations, legacy cost curves, benefits realisation and sustainability trade-offs; verbal reasoning against the principles documents, strategy papers, commercial guidance and senior correspondence whose exact wording is your working material; and situational judgement in the political, human and strategic dilemmas that define leadership at principal level.

If one theme runs through all four, it is this: the disciplines these assessments measure are the same disciplines that make you effective in post. Checking freshness against cadence, refusing to upgrade "expected to" into "will", computing before committing, verifying before challenging, engaging before escalating - these are simultaneously test techniques and professional habits. Time spent practising them is never wasted, whatever the assessment outcome.

As next steps, consider three things. First, revisit the questions you found hardest after a week's gap; durable improvement shows in the second attempt, not the first. Second, practise generatively: writing your own questions from your organisation's real artefacts - a genuine decision log, a live supplier schedule, last month's board paper - deepens the skill far more than consuming questions alone, and produces material you can share with your architecture community. Third, treat this as part of your continuing professional development: the GDAD capability framework, your department's learning offer and communities of practice across government all provide routes to keep growing, and as a principal you multiply every improvement by modelling it for others.

Assessments can feel like a test of worth. They are not; they are a snapshot of practised skills, and skills respond to practice. You operate at a level where clear thinking under complexity is the job itself - approach any assessment as another day of doing what you already do, with a little more polish and a lot less mystery. Good luck. You are better prepared than you were when you started this document, and that is the entire point.

---

*Professional development tip: revisit this resource periodically as your role evolves, and share it with colleagues who are developing towards this role level.*
