# Security Architect (Lead Security Architect) - Psychometric Assessment Resources

## Introduction

Welcome. This document is written for you: a lead security architect working within the UK Government Digital and Data profession. You undertake complex, high-risk work, often across several projects at once. You interact with senior stakeholders across departments, lead the technical design of systems and services, act as the point of escalation for architects in lower grade roles, and develop the vision, principles and strategy that guide security architecture for a project or technology. Psychometric assessments are increasingly used at this level of seniority — for promotion boards, cross-government moves, senior recruitment campaigns, and structured professional development — and this resource is designed to help you approach them with confidence.

A psychometric assessment is a structured, standardised way of measuring the mental capabilities and behavioural tendencies that predict performance in a specific role. For a lead security architect, that means far more than abstract puzzles. Well-designed assessments for your role probe how you reason about complex system architectures, how you interpret risk data and security metrics, how precisely you read policy and standards documents, and how you exercise judgement when senior stakeholders, delivery pressure and security risk pull in different directions. In other words, they measure the very things your role summary describes: analysis, communication, designing secure systems, enabling and informing risk-based decisions, research and innovation, security technology, and understanding the security implications of transformation.

This document is organised into four main sections, one for each assessment type you are most likely to encounter:

- **Workplace job-specific cognitive assessment** — pattern recognition, logical deduction, error checking and prioritisation using artefacts you genuinely handle, such as architecture diagrams, threat models and assurance findings.
- **Workplace job-specific numeric reasoning assessment** — interpreting vulnerability metrics, risk scores, security budgets, capacity figures and programme data.
- **Workplace job-specific verbal reasoning assessment** — drawing accurate conclusions from dense passages such as security policies, standards, assurance reports and stakeholder correspondence.
- **Workplace job-specific situational judgement assessment** — realistic dilemmas involving senior stakeholders, escalations from junior architects, risk tolerance decisions and cross-department influence.

Each section explains what the assessment measures, maps it explicitly to the skills in your role profile, provides a substantial set of practice questions with worked answers, and closes with preparation tips and common pitfalls.

How should you use it? Three ways. First, as practice: work through the questions under light time pressure and compare your reasoning with the explanations. Second, as self-reflection: notice which question types feel effortful, because those point to development areas. Third, as preparation: revisit the tips and pitfalls shortly before any real assessment. You already operate at a senior level; treat this as a structured rehearsal of thinking you do every day, made explicit and measurable. Good luck — you are better prepared for these assessments than you may think.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive assessment measures the exact mental processes your role demands, using practical scenarios and data drawn from the work itself rather than abstract puzzles. Unlike a generic IQ test, every item mimics an everyday task or data format from the job: for you, that means reasoning over system architecture diagrams, security patterns, control frameworks, assurance findings, escalation queues and threat models. Assessments of this kind are typically delivered online, timed at around 15 to 30 minutes, and objectively scored against a benchmark or norm group of comparable professionals. Some platforms are adaptive, adjusting question difficulty as you answer, and most provide short ungraded practice items so you can get used to the interface before the clock starts.

For a lead security architect, cognitive ability is not an academic nicety — it is the engine of the role. When you work out subtle security needs, you are doing pattern recognition. When you decide between two candidate architectures by tracing the consequences of each, you are doing logical deduction. When you review a junior architect's design and spot the one trust boundary that has been drawn in the wrong place, you are doing error checking. When you triage escalations from several projects at once, you are doing prioritisation under constraint. A well-built cognitive assessment simply samples these processes in compressed, standardised form, and employers at your level read the results as a breakdown of speed versus accuracy rather than a single number.

### What it measures for your role

Mapping the standard cognitive dimensions onto the skills named in your role profile:

- **Logical deduction and problem solving** map to **Designing secure systems** ("design and review system architectures through the development of patterns and principles") and **Security technology** ("explain complex system architectures"; "identify and explain how easy or difficult it will be to exploit vulnerabilities"). Items ask you to infer what must be true about a system given a set of architectural constraints, or to reason about exploitability from a chain of conditions.
- **Pattern recognition** maps to **Analysis** ("monitor the analysis of a technical solution and ensure analysis is reused for similar problem sets") and to your duty to "produce particular patterns and support quality assurance". Items ask you to spot the common structure across several incidents, designs or findings.
- **Error checking** maps to your quality assurance duty and to being "the point of escalation for architects in lower grade roles" — the person who catches what others miss in rule sets, diagrams and control mappings.
- **Prioritisation and decision-making under constraint** map to your duty to "understand the impact of decisions, balancing requirements and deciding between approaches" and to **Enabling and informing risk-based decisions** ("work with higher impact or more complex risks, advising on the impact and whether it's within risk tolerance").
- **Rule application and abstraction** map to **Understanding security implications of transformation** ("interpret and apply understanding across a complex area") — taking a principle stated once and applying it correctly to a novel case.

### Practice questions

Work through these under light time pressure — around two to three minutes each. Full explanations follow every answer; the reasoning matters more than the score.

**Question 1 (easy) — Rule application.** Your department's security principles state: (1) all services handling OFFICIAL data must authenticate users before granting access; (2) any service exposed to the public internet must sit behind the departmental web application firewall (WAF); (3) internal-only services may use the legacy single sign-on until March. A junior architect proposes a new citizen-facing form service that handles OFFICIAL data, is exposed to the internet, and uses the legacy single sign-on. Which principles does the proposal breach?

- A) Principle 1 only
- B) Principle 3 only
- C) Principle 3, and possibly Principle 2 depending on the design
- D) None, provided the service launches before March

**Answer: C.** Principle 3 permits legacy single sign-on only for internal-only services; a citizen-facing service is not internal-only, so using legacy SSO breaches that condition regardless of the launch date — which rules out D. Principle 1 is not necessarily breached: the proposal may still authenticate users (using the wrong mechanism is a Principle 3 problem, not a Principle 1 problem). Principle 2 requires the WAF for internet-exposed services, and the proposal as stated says nothing about the WAF, so it is possibly breached depending on the design. The disciplined reading — checking exactly which condition each principle attaches to — is the same care you apply when reviewing designs against published patterns.

**Question 2 (easy) — Error checking.** You are quality-assuring a firewall rule table extracted from a junior architect's design. The stated intent is: "Only the app tier may reach the database tier, on port 5432 only."

| Rule | Source | Destination | Port | Action |
|------|--------|-------------|------|--------|
| 1 | App tier | DB tier | 5432 | Allow |
| 2 | App tier | DB tier | 22 | Allow |
| 3 | Any | DB tier | Any | Deny |

Which rule contradicts the stated intent?

- A) Rule 1
- B) Rule 2
- C) Rule 3
- D) None — the table matches the intent

**Answer: B.** Rule 1 implements the intent exactly. Rule 3 is the correct default-deny backstop. Rule 2, however, allows the app tier to reach the database tier on port 22 (SSH), which violates "on port 5432 only". This is the classic quality assurance catch: a rule that looks operationally convenient (someone wanted SSH access for maintenance) but silently widens the trust relationship beyond the documented pattern. In an assessment, read the intent statement first, then test every row against it — do not assume the table is mostly right.

**Question 3 (moderate) — Logical deduction.** A legacy case-management system is being assessed. You know the following, all of which are true: if the system stores citizen data unencrypted at rest, it fails the data-handling standard; the system fails the data-handling standard or it passed last year's assurance review (or both); the system did not pass last year's assurance review. What can you validly conclude?

- A) The system stores citizen data unencrypted at rest
- B) The system fails the data-handling standard
- C) The system encrypts citizen data at rest
- D) Nothing can be concluded about the standard

**Answer: B.** From "fails the standard OR passed last year's review" and "did not pass last year's review", the disjunction forces the other branch: the system fails the data-handling standard. Note what you cannot conclude: A does not follow, because unencrypted storage is a sufficient condition for failing, not a necessary one — the system might fail the standard for a completely different reason. C fails for the same reason. This distinction between sufficient and necessary conditions is exactly the reasoning you use when advising whether a finding proves a control gap or merely suggests one possible cause.

**Question 4 (moderate) — Pattern recognition across incidents.** Reviewing four security findings from different projects, you note: Project A — API gateway accepted expired client certificates; Project B — batch transfer service accepted files signed with a revoked key; Project C — single sign-on accepted session tokens after staff offboarding; Project D — admin portal locked out users after three failed login attempts. Which project's finding does NOT share the common underlying pattern?

- A) Project A
- B) Project B
- C) Project C
- D) Project D

**Answer: D.** Projects A, B and C all show the same structural weakness: a credential or trust artefact (certificate, signing key, session token) continuing to be honoured after it should have been invalidated — a failure to check revocation or expiry at time of use. Project D describes a lockout control operating, arguably correctly; it is not a stale-trust failure. Recognising this shared structure is precisely the "ensure analysis is reused for similar problem sets" behaviour in your Analysis skill: one root-cause pattern, one reusable remediation pattern (validate trust artefacts at time of use), applied across three projects rather than three bespoke fixes.

**Question 5 (moderate) — Prioritisation.** It is Monday morning and four items await you. (1) A junior architect on Project Alpha has escalated a disagreement with a delivery manager about whether a penetration test can be deferred; the design freeze is Wednesday. (2) A vendor briefing on a new secure enclave technology is scheduled for 14:00 today and could inform your strategy paper due next month. (3) Project Beta's live service has a newly published critical vulnerability in an internet-facing component, with exploit code circulating. (4) Your quarterly patterns review with the architecture community is due Friday. Which ordering best reflects sound prioritisation?

- A) 3, 1, 2, 4
- B) 1, 3, 4, 2
- C) 3, 2, 1, 4
- D) 2, 3, 1, 4

**Answer: A.** Item 3 is a live, exploitable, internet-facing critical vulnerability — the highest and most time-sensitive risk, so it comes first. Item 1 is next: it is an escalation you specifically own as the point of escalation for lower-grade architects, and it has a hard deadline (Wednesday's design freeze) that makes it more urgent than either remaining item. Item 2 is time-boxed today but is an input to work due next month; attending is valuable but sacrificing it costs little compared to items 3 and 1. Item 4 has the longest runway. The pattern to internalise: order by risk impact and irreversibility first, then by deadline proximity, then by strategic value — never by which item arrived most recently or shouts loudest.

**Question 6 (moderate) — Rule application with exceptions.** Your pattern library states: "Pattern P-12 (zero trust service access) applies to all new internal services. Exception: services classified as legacy-integration may instead use Pattern P-07 (segmented network access), provided they are scheduled for decommissioning within 24 months and do not process SECRET data." A team proposes a new internal service, classified legacy-integration, decommissioning in 30 months, processing OFFICIAL data, built on Pattern P-07. Is the proposal compliant?

- A) Yes — legacy-integration services may always use P-07
- B) Yes — it does not process SECRET data, so the exception applies
- C) No — the 30-month decommissioning date invalidates the exception, so P-12 applies
- D) No — legacy-integration services may not be new services

**Answer: C.** The exception has two conjoined conditions: decommissioning within 24 months AND not processing SECRET data. The service meets the second (OFFICIAL is not SECRET) but fails the first (30 months exceeds 24). Both conditions must hold for the exception; failing either returns the service to the default rule, P-12. Option B is the classic trap — satisfying one condition of a conjunction and stopping there. Option D invents a restriction the text does not contain. When you quality-assure designs against patterns, this is the discipline: enumerate every condition of an exception and test each one independently.

**Question 7 (moderate) — Deductive sequencing.** A programme is migrating five services (V, W, X, Y, Z) to a new hosting platform, and security constraints dictate ordering: X must migrate before Z, because Z depends on X's identity service. Y cannot migrate until the new platform's protective monitoring is live, which happens only after W migrates (W carries the monitoring stack). V must migrate last, as it is the legacy audit consolidator. W must migrate before X to provide monitoring coverage for X's migration. Which service migrates second?

- A) W
- B) X
- C) Y
- D) It cannot be determined from the constraints

**Answer: D.** List the binding constraints: W before X (monitoring coverage for X's migration), X before Z (identity dependency), Y after W (Y needs monitoring live, which W provides), and V last. W must therefore be first: X, Z and Y all sit somewhere after it, and V is fifth. But is the second slot forced? Test candidate orderings. W, X, Y, Z, V satisfies every constraint — X second. W, Y, X, Z, V also satisfies every constraint: W precedes X, X precedes Z, Y follows W, V is last — Y second. Two valid orderings put different services second, so the second position cannot be determined from the constraints given. Option B is the trap for candidates who chain W → X → Z into a single rigid sequence and forget that "W before X" does not mean "W immediately before X". Before answering "X must be second" in any sequencing item, actively try to construct a counterexample ordering; if one exists, the answer is "cannot be determined". The same habit — trying to break your own conclusion — is what separates a design review that finds subtle security needs from one that rubber-stamps the obvious.

**Question 8 (hard) — Exploitability reasoning.** A system has four conditions relevant to a known vulnerability class: (1) the vulnerable library version is present; (2) the vulnerable function is reachable from user-controlled input; (3) exploitation requires an authenticated session; (4) sessions are issued only to staff with hardware tokens. An attacker has stolen one staff member's password but not their hardware token. Given only these facts, which statement is the strongest correct claim about exploitability?

- A) The system is exploitable, because the vulnerable library is present
- B) The system is not exploitable by this attacker via this path, because condition 4 blocks session issuance
- C) The system is not vulnerable, because the attacker lacks a token
- D) The system is exploitable because passwords are compromised

**Answer: B.** Distinguish vulnerability (a weakness exists: conditions 1 and 2 hold) from exploitability by a given attacker via a given path (all conditions in the chain must be satisfiable by that attacker). This attacker cannot obtain an authenticated session because sessions require a hardware token the attacker lacks; the chain breaks at condition 3 via condition 4. Option A confuses presence with exploitability. Option C overreaches: the system is still vulnerable (the weakness exists, and a different attacker — say, an insider with a token — could exploit it). Option D ignores the token requirement entirely. Precisely this framing — "how easy or difficult it will be to exploit vulnerabilities", scoped to attacker capability and path — is named in your Security technology skill, and it is what turns a raw scanner finding into risk advice a senior stakeholder can act on.

**Question 9 (hard) — Balancing requirements.** You must choose between two architectures for a new inter-departmental data-sharing service. Architecture 1: centralised broker — strong central policy enforcement and audit, single point of failure, requires every department to trust the broker operator, delivery estimate 9 months. Architecture 2: federated point-to-point — no central trust dependency, each department enforces its own policy, audit is fragmented across departments, delivery estimate 5 months. The programme's non-negotiable requirements are: a complete cross-department audit trail for every data exchange, and delivery within 12 months. Which is the stronger conclusion?

- A) Architecture 2, because it delivers four months sooner
- B) Architecture 1, because only it satisfies the complete audit trail requirement as described
- C) Either, because both deliver within 12 months
- D) Neither, because both have weaknesses

**Answer: B.** Both architectures meet the 12-month constraint, so delivery speed cannot be the deciding factor between compliant options — it is a tiebreaker only among designs that satisfy every non-negotiable. The complete cross-department audit trail is non-negotiable, and as described, Architecture 2 produces fragmented audit across departments, failing that requirement; Architecture 1 satisfies it. Option A optimises a negotiable attribute at the cost of a non-negotiable one — the most common failure mode in architecture decision records. Option D confuses "has weaknesses" with "fails requirements"; every real architecture has weaknesses, and your job, as the role profile says, is "balancing requirements and deciding between approaches", not waiting for a flawless option. The single point of failure and broker-trust issues in Architecture 1 are real, but they are risks to manage (resilience patterns, governance of the broker), not requirement failures.

**Question 10 (hard) — Pattern abstraction.** Three projects submit designs for your review. Project 1 terminates TLS at an edge load balancer, then forwards traffic unencrypted across a shared internal network to the application. Project 2 decrypts field-level encrypted records at an integration layer, then writes them to a shared message queue in plaintext for the consuming service. Project 3 validates user input at the web front end, then passes it to backend microservices that perform no further validation. What single reusable principle, if adopted as a pattern, would address the underlying weakness in all three designs?

- A) Encrypt all data at rest
- B) Do not rely on an upstream boundary — re-establish security properties (encryption, validation) at each internal trust boundary
- C) Use TLS 1.3 everywhere
- D) Centralise all security controls at the network edge

**Answer: B.** The shared structure is that each design establishes a security property at one boundary and then assumes it persists downstream: transport encryption stops at the edge (Project 1), data confidentiality stops at the integration layer (Project 2), input validation stops at the front end (Project 3). The abstraction is the zero-trust-flavoured principle that security properties must be re-established at each internal trust boundary rather than inherited. Option A addresses only data at rest, which is not even the failure in Projects 1 and 3. Option C fixes transport for Project 1 only. Option D is the anti-pattern itself, stated as if it were a cure. Extracting one principle from several concrete failures — and publishing it as a pattern so the analysis is reused for similar problem sets — is the core of your "produce particular patterns" duty.

**Question 11 (moderate) — Error checking under time pressure.** A junior architect's data-flow diagram lists six flows for a payments-adjacent service. The accompanying control mapping asserts: "All flows crossing the internet boundary are mutually authenticated with mTLS." The flows are: F1 browser to public API (internet, TLS with server auth only); F2 public API to internal queue (internal, mTLS); F3 internal queue to processor (internal, mTLS); F4 processor to third-party payment provider (internet, mTLS); F5 processor to internal database (internal, TLS server auth); F6 monitoring agent to external SaaS dashboard (internet, API key over TLS). How many flows contradict the assertion?

- A) One (F1)
- B) Two (F1 and F6)
- C) Three (F1, F5 and F6)
- D) Four (F1, F2, F5, F6)

**Answer: B.** The assertion is scoped to flows crossing the internet boundary: F1, F4 and F6. F4 uses mTLS — compliant. F1 uses server-authenticated TLS only — not mutual — contradiction. F6 uses an API key over one-way TLS — not mutual authentication at the transport layer — contradiction. F5 lacks mTLS but is internal, so it falls outside the assertion's scope (it may be a design concern, but it does not contradict this claim). The trap in option C is exactly the scope error the question tests: flagging F5 means you checked the control but not the boundary condition attached to it. Assessments reward, and design reviews demand, testing each item against the full claim — control AND scope — not the control alone.

**Question 12 (hard) — Deciding between approaches with incomplete information.** An emerging technology team proposes adopting confidential computing enclaves for a sensitive analytics workload. Known: enclaves would remove the hosting provider from the trust boundary for data in use; the technology is new to your organisation; two of your five current security engineers have relevant skills; the vendor's attestation service has had one publicly disclosed flaw, since patched; the alternative is your established pattern of strict segregation plus contractual controls, which the risk owner has previously accepted for similar workloads. The risk owner asks for your recommendation this week; a full evaluation would take three months. Which recommendation best reflects lead-level judgement?

- A) Adopt enclaves now — removing the provider from the trust boundary is strictly better
- B) Reject enclaves — new technology with a disclosed flaw is too risky
- C) Recommend the established pattern for this workload now, and initiate a time-boxed evaluation of enclaves as a candidate future pattern, reporting findings to the risk owner
- D) Delay the decision three months until the evaluation completes

**Answer: C.** The decision has a deadline (this week) that option D ignores — delaying a decision the risk owner needs is itself a decision, and an unmanaged one. Option A treats a security property improvement as decisive while ignoring delivery risk: limited in-house skills, organisational novelty and immature operational experience are genuine risks that a lead architect must weigh, not dismiss. Option B commits the opposite error, treating novelty and one patched flaw as disqualifying, which would freeze all innovation — contrary to your Research and innovation skill ("identify new technologies and design the use of these in the business context"). Option C satisfies the immediate need with a pattern already within risk tolerance, while structuring the innovation work properly: time-boxed, evidence-producing, and feeding a future pattern decision. It also models the behaviour your role profile describes — justifying and communicating design decisions rather than merely making them.

**Question 13 (moderate) — Working out subtle security needs.** A transformation programme is replacing paper-based benefit appeals with a digital service. The overt security requirements cover authentication, encryption and audit. During review you consider second-order effects. Which of the following is the most significant subtle security need the overt requirements miss?

- A) The digital service will need a privacy notice
- B) Appeal metadata (who appealed, when, how often) becomes aggregable at scale, creating a new sensitive dataset and insider-browsing risk that paper files never presented
- C) The service should use a content delivery network for performance
- D) Users will need password reset functionality

**Answer: B.** Options A and D are real but routine — any competent checklist captures them, so they are not "subtle". Option C is a performance concern, not a security need. Option B identifies an emergent property of digitisation: information that was practically obscure when distributed across paper files in local offices becomes a queryable, aggregable dataset. That changes the threat model (insider browsing, bulk exfiltration, inference about vulnerable individuals) and demands controls — fine-grained access on a need-to-know basis, anomalous-query detection, aggregation limits — that no requirement explicitly asked for. Surfacing needs like this is exactly what "work out subtle security needs" means at your level, and it is where transformation programmes most depend on your Understanding security implications of transformation skill.

### Preparation tips

- **Rehearse with your own artefacts.** The best practice material is the work itself: take a recent design review, an architecture decision record, or a set of assurance findings, and consciously reconstruct the reasoning — what were the conditions, which were necessary versus sufficient, what would falsify the conclusion? Ten minutes of this daily sharpens exactly what the assessment measures.
- **Practise the counterexample habit.** For every "must be true" conclusion you reach, spend fifteen seconds trying to construct a case where it is false. As Question 7 showed, apparently forced conclusions often dissolve; assessments at senior level deliberately include items where "cannot be determined" is correct.
- **Manage the clock like an escalation queue.** With 15 to 30 minutes for the whole test, treat each question like triage: if an item resists you after ninety seconds, flag it and move on. Banking easier points first is prioritisation — a skill being measured even when no question names it.
- **Read scopes and conditions before content.** Most error-checking items hide the answer in a scope qualifier ("flows crossing the internet boundary", "within 24 months", "internal-only"). Underline or mentally isolate the qualifiers first, then evaluate items against them.
- **Trust your professional maturity.** You resolve harder ambiguities than these in real design authority meetings. Arrive rested, do the platform's ungraded practice items to settle into the interface, and treat the test as a compressed working day.

### Common pitfalls

- **Assuming the artefact is mostly right.** In real reviews you extend professional courtesy; in an assessment, every table, diagram description and rule set should be treated as potentially wrong until each element is verified against the stated intent.
- **Importing outside knowledge.** You know more about security architecture than any test passage states. Answer strictly from the given conditions — if the question does not say the WAF is absent, its absence is "possible", not "true".
- **Confusing vulnerability with exploitability, and sufficiency with necessity.** Several question styles specifically bait these conflations, because they are the errors that matter most in real risk advice.
- **Time-sink questions.** Getting absorbed in one intricate multi-constraint item and leaving three easy items unanswered is the most common way strong candidates underperform. Skip and return.
- **Overthinking easy items.** At lead level you may suspect traps everywhere. Some questions are simply direct; answer them directly and save your scepticism for items that explicitly involve exceptions, scopes or "cannot be determined" options.


## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment evaluates your ability to analyse, interpret and make sound decisions using numerical data of the kind your role genuinely produces. It mimics the data-handling demands of the job rather than testing abstract mathematics: the inputs are tables, dashboards, budgets and schedules, and the operations are percentages, ratios, rates, weighted comparisons and cost-benefit estimations. Most assessments allow or provide an on-screen calculator, because the skill being measured is interpretation — extracting the right figures, applying the right operation, and sanity-checking the result — rather than mental arithmetic. Time limits are strict, typically around a minute to ninety seconds per question, simulating the pace at which you scan a metrics pack before a board meeting.

For a lead security architect, numbers are the language in which risk, assurance and investment arguments are won or lost. You advise risk owners on whether high-impact risks sit within tolerance — which means reading likelihood and impact figures and residual-risk calculations critically. You justify design decisions to senior stakeholders across departments — which means comparing costs, capacity figures and remediation timelines. You drive the collection of information that is used and analysed — which means knowing when a metric is misleading, when a percentage hides a denominator problem, and when a vendor's headline figure does not survive arithmetic. This assessment samples all of that in standardised form.

### What it measures for your role

- **Interpreting risk and vulnerability metrics** maps to **Enabling and informing risk-based decisions** ("work with higher impact or more complex risks, advising on the impact and whether it's within risk tolerance"; "apply different risk methodologies in proportion to the risk"). Expect items on risk scores, likelihood-impact products, residual risk and tolerance thresholds.
- **Analysing collected data critically** maps to **Analysis** ("drive the collection of information that is used and analysed"; "review solutions and identify areas for change"). Expect items on trend tables, percentage changes and metrics whose definitions matter.
- **Costing and comparing architectural options** maps to your duty to "understand the impact of decisions, balancing requirements and deciding between approaches" and to "research and apply innovative security architecture solutions... and be able to justify and communicate design decisions". Expect budget tables, total-cost comparisons and capacity calculations.
- **Evaluating exploitability and exposure at scale** maps to **Security technology** ("identify and explain how easy or difficult it will be to exploit vulnerabilities") — patch coverage rates, exposure windows, and fleet-level percentages.
- **Communicating figures accurately** maps to **Communication** ("effectively translate and accurately communicate security and risk implications to technical and non-technical stakeholders") — several items test whether a numerical claim someone else made is actually supported by the data.

### Practice questions

An on-screen calculator is assumed. Aim for ninety seconds per question; every explanation shows the arithmetic in full.

**Question 1 (easy) — Percentage of estate patched.** Your protective monitoring pack reports that of 1,240 servers in scope, 1,054 have received the critical patch released 14 days ago. What percentage of the estate remains unpatched, to one decimal place?

- A) 12.4%
- B) 15.0%
- C) 85.0%
- D) 18.6%

**Answer: B.** Unpatched servers: 1,240 − 1,054 = 186. As a percentage: 186 ÷ 1,240 = 0.15, so 15.0%. Option C is the patched percentage (1,054 ÷ 1,240 = 85.0%) — the classic complement error. Option A misreads 186 as 12.4% by dividing by 1,500. When you report exposure to a risk owner, the unpatched fraction is the risk-bearing figure; always confirm which side of the split a question (or a dashboard) is asking for.

**Question 2 (easy) — Risk score arithmetic.** Your department scores risks as likelihood (1–5) multiplied by impact (1–5), with a tolerance threshold of 12: scores above 12 must be escalated to the risk owner. A supplier-compromise risk is assessed at likelihood 4, impact 4. After a proposed control, likelihood falls to 2 and impact is unchanged. What are the current and residual scores, and does the residual score require escalation?

- A) 16 and 8; no escalation needed for the residual risk
- B) 16 and 8; escalation still required
- C) 8 and 16; no escalation needed
- D) 20 and 10; no escalation needed

**Answer: A.** Current: 4 × 5 is a misread — impact is 4, so 4 × 4 = 16, which exceeds 12 and requires escalation now. Residual: 2 × 4 = 8, which is at or below the threshold of 12, so the residual risk does not itself require escalation. This mirrors your daily practice of advising "whether it's within risk tolerance": the arithmetic is trivial, but assessments check you attach the threshold test to the right figure (residual, not current) and read the matrix axes correctly.

**Question 3 (moderate) — Percentage change in findings.** Quarterly assurance reviews across your three projects produced these finding counts:

| Project | Q1 findings | Q2 findings |
|---------|-------------|-------------|
| Alpha | 48 | 36 |
| Beta | 20 | 27 |
| Gamma | 32 | 29 |

Which statement is correct?

- A) Alpha improved by 25%, Beta worsened by 35%, Gamma improved by about 9.4%
- B) Alpha improved by 33%, Beta worsened by 26%, Gamma improved by 3%
- C) Alpha improved by 25%, Beta worsened by 26%, Gamma improved by 9.4%
- D) Total findings fell by 25% across the portfolio

**Answer: A.** Alpha: (48 − 36) ÷ 48 = 12 ÷ 48 = 25% decrease. Beta: (27 − 20) ÷ 20 = 7 ÷ 20 = 35% increase. Gamma: (32 − 29) ÷ 32 = 3 ÷ 32 ≈ 9.4% decrease. The trap in option B is computing Alpha's change against the new value (12 ÷ 36 = 33%) and Beta's against the new value (7 ÷ 27 ≈ 26%) — percentage change is always measured against the starting value. Option D fails: totals are 100 and 92, a fall of 8%, not 25%. When your metrics pack goes to senior stakeholders, exactly this base-value error is the most common way figures get miscommunicated.

**Question 4 (moderate) — Security budget allocation.** Your programme's annual security budget is £2.4 million, allocated 45% to engineering remediation, 25% to assurance and testing, 20% to tooling licences, and the remainder to training. Mid-year, the tooling allocation is cut by 15% of its own value and the savings are moved to training. How much does training receive for the year?

- A) £240,000
- B) £312,000
- C) £72,000
- D) £288,000

**Answer: B.** Original allocations: remainder for training = 100% − 45% − 25% − 20% = 10%, so training = 0.10 × £2,400,000 = £240,000. Tooling = 0.20 × £2,400,000 = £480,000. The cut is 15% of tooling's own value: 0.15 × £480,000 = £72,000. Training therefore receives £240,000 + £72,000 = £312,000. Option A forgets the transfer; option C is the transfer alone; option D applies 20% × £2.4m × 0.6 confusion. Note the phrase "15% of its own value" — assessments (and finance papers) distinguish percentage-of-part from percentage-of-whole, and misreading it changes your answer materially.

**Question 5 (moderate) — Exposure window.** A critical vulnerability was published at 09:00 on Monday 2 March. Your fleet telemetry shows patching proceeded at a constant rate and reached 100% of the 800 affected hosts at 17:00 on Friday 6 March (104 hours later). Assuming a constant patch rate, for how many host-hours was the estate exposed in total?

- A) 83,200 host-hours
- B) 41,600 host-hours
- C) 800 host-hours
- D) 10,400 host-hours

**Answer: B.** With patching at a constant rate from 800 exposed hosts down to 0 over 104 hours, the average number of exposed hosts across the window is (800 + 0) ÷ 2 = 400. Total exposure = 400 hosts × 104 hours = 41,600 host-hours. Option A (800 × 104) assumes every host stayed exposed the whole window — that would be the case only if all patching happened at the end. This triangular-area reasoning is genuinely useful in your role: it is how you compare remediation strategies (fast start versus big-bang weekend patching) when advising on the impact of vulnerability response options.

**Question 6 (moderate) — Ratio of architects to projects.** Your architecture community has 4 lead architects, 10 security architects and 6 associate architects, supporting 45 active projects. Governance guidance states projects per (non-associate) architect should not exceed 3.5. A transformation programme will add 12 projects and 2 security architects. After the change, is the guidance met?

- A) Yes — the ratio falls to 3.0
- B) Yes — the ratio is exactly 3.5
- C) No — the ratio rises to about 3.56
- D) No — the ratio rises to 4.75

**Answer: C.** Non-associate architects now: 4 leads + 10 security architects = 14; after the change: 14 + 2 = 16. Projects after the change: 45 + 12 = 57. Ratio: 57 ÷ 16 = 3.5625 ≈ 3.56, which exceeds the 3.5 guidance. The quickest safe method is to compute the threshold value itself: 16 architects × 3.5 = 56 projects, and 57 > 56, so the guidance is breached. Options engineered to sit just either side of a threshold (56 versus 57 projects) are a favourite assessment device; eyeballing the division invites the near-miss answer B, while computing the threshold and comparing protects you. One project over the line is still over the line — as you would tell any programme trying to squeeze past a governance gate. Also confirm who counts: the guidance scopes to non-associate architects, so the 6 associates are excluded from the denominator, and including them (22 architects, ratio 2.59) would silently answer a different question.

**Question 7 (hard) — Total cost of ownership comparison.** You are comparing two options for a cross-government secure gateway, over a three-year appraisal period. Option A: build — £900,000 up-front build cost, £150,000 per year to operate, and a one-off £120,000 assurance cost in year 1. Option B: buy — no build cost, £480,000 per year licence and operation, minus a negotiated 10% discount on the licence element (£400,000 of the £480,000) in each of years 2 and 3. Which option is cheaper over three years, and by how much?

- A) Option A, by £330,000
- B) Option B, by £110,000
- C) Option A, by £410,000
- D) Option B, by £70,000

**Answer: B.** Option A total: £900,000 + (3 × £150,000) + £120,000 = £900,000 + £450,000 + £120,000 = £1,470,000. Option B: year 1 = £480,000; years 2 and 3 each = £480,000 − (0.10 × £400,000) = £480,000 − £40,000 = £440,000. Total = £480,000 + £440,000 + £440,000 = £1,360,000. Option B is cheaper by £1,470,000 − £1,360,000 = £110,000. Follow the arithmetic rather than the instinct that "build must eventually win": over a short three-year appraisal window, up-front build costs often do not amortise, which is exactly the argument you must be able to make (or counter) when justifying design decisions at spending reviews. Note also that the discount applies only to the licence element (£400,000, not the full £480,000) and only in years 2 and 3 — partial scopes like this are where marking schemes separate careful readers from fast ones, and option D is precisely the answer you get if you discount the full £480,000 in all three years.

**Question 8 (hard) — Weighted risk methodology.** You are applying a proportionate methodology to compare three complex risks. Each is scored on three weighted factors: exploitability (weight 0.5), business impact (weight 0.3) and detectability gap (weight 0.2), each factor scored 1–10.

| Risk | Exploitability | Business impact | Detectability gap |
|------|----------------|-----------------|-------------------|
| R1: unpatched VPN concentrator | 8 | 6 | 4 |
| R2: supplier with weak offboarding | 5 | 9 | 7 |
| R3: shadow SaaS data flows | 6 | 5 | 9 |

Which risk has the highest weighted score, and what is that score?

- A) R1, with 6.6
- B) R2, with 6.6
- C) R3, with 6.3
- D) R1 and R2 tie at 6.6

**Answer: D.** R1: (8 × 0.5) + (6 × 0.3) + (4 × 0.2) = 4.0 + 1.8 + 0.8 = 6.6. R2: (5 × 0.5) + (9 × 0.3) + (7 × 0.2) = 2.5 + 2.7 + 1.4 = 6.6. R3: (6 × 0.5) + (5 × 0.3) + (9 × 0.2) = 3.0 + 1.5 + 1.8 = 6.3. R1 and R2 tie exactly at 6.6, so D is correct — and options A and B are each "half right", which is how assessments punish candidates who compute one row and stop. The professional lesson runs deeper: a tie between a technically driven risk (R1) and a people-and-process risk (R2) is where a scoring model stops helping and your judgement about "which methodology in proportion to the risk" takes over. A weighted score is an input to your advice, never a substitute for it.

**Question 9 (moderate) — Interpreting a vendor's claim.** A vendor claims its detection platform "reduces mean time to detect (MTTD) by 60%". Your current MTTD is 40 hours. Pilot data from your own environment shows the platform detected 18 of 24 simulated intrusions, with detection times (for those 18) averaging 22 hours. Which statement most accurately reflects your pilot evidence?

- A) The pilot confirms the 60% claim
- B) The pilot shows a 45% MTTD reduction on detected intrusions, but 25% of simulated intrusions were not detected at all
- C) The pilot shows MTTD worsened
- D) The pilot detected 75% of intrusions, confirming the claim

**Answer: B.** Reduction on detected intrusions: (40 − 22) ÷ 40 = 18 ÷ 40 = 45%, not 60%. Detection coverage: 18 ÷ 24 = 75% detected, so 6 ÷ 24 = 25% undetected. Option B captures both facts. Option A accepts the marketing figure over your own data. Option D conflates coverage with the time-reduction claim — 75% coverage says nothing about the 60% MTTD assertion, and an average computed only over detected cases silently excludes the worst outcomes (never detected). Spotting that a headline metric is conditioned on a favourable subset is a core skill when you "drive the collection of information that is used and analysed", and it is exactly the kind of scrutiny your Research and innovation skill demands before a new technology enters the organisation.

**Question 10 (hard) — Capacity and throughput for a security service.** Your new central authentication service must handle peak demand from four departments: 3,200, 4,800, 2,000 and 6,000 requests per minute respectively, with departmental peaks assumed to coincide. Each service node sustains 1,500 requests per minute at the required latency. Resilience policy requires the estate to tolerate the loss of any two nodes while still serving the full coincident peak. How many nodes must you provision?

- A) 11
- B) 12
- C) 13
- D) 14

**Answer: C.** Coincident peak: 3,200 + 4,800 + 2,000 + 6,000 = 16,000 requests per minute. Nodes needed to serve that: 16,000 ÷ 1,500 = 10.67, round up to 11 (10 nodes give only 15,000). Resilience: the full peak must survive the loss of any two nodes, so provision 11 + 2 = 13. Option A ignores resilience; option B adds only one spare; option D over-provisions. The two-step structure — compute the service requirement with a ceiling (never round capacity down), then add the failure allowance — recurs constantly in security infrastructure sizing, from HSM clusters to logging pipelines, and getting the rounding direction wrong is the most common real-world error.

**Question 11 (moderate) — Reading a trend table critically.** A dashboard shows phishing reports per month: January 120, February 132, March 178, April 165. A senior stakeholder says: "Reports rose every month in the first quarter — our awareness campaign, launched 1 March, is clearly failing." Which numerical observation most directly challenges that conclusion?

- A) April's figure fell 7.3% from March, and reports are a measure of staff reporting behaviour, which the campaign aims to increase — rising reports may indicate success
- B) February's rise was only 10%
- C) The Q1 total is 430
- D) March's rise was 34.8%

**Answer: A.** The arithmetic in A: (178 − 165) ÷ 178 = 13 ÷ 178 ≈ 7.3% fall in April; and the conceptual point is decisive — "phishing reports" counts staff reporting emails, so an awareness campaign is designed to push it up, not down. More reports can mean better detection behaviour, not more phishing. Options B, C and D are all arithmetically true (February: 12 ÷ 120 = 10%; total: 120 + 132 + 178 = 430; March: 46 ÷ 132 ≈ 34.8%) but none challenges the stakeholder's inference. This is the numeric face of your Communication skill: translating what a metric actually measures for a non-technical stakeholder — and correcting a wrong reading without the numbers descending into a spreadsheet argument.

**Question 12 (moderate) — Cost per finding remediated.** Two remediation approaches were piloted. Approach 1 (dedicated security sprint): cost £84,000, closed 105 findings. Approach 2 (embedded fix-forward in feature teams): cost £61,200, closed 68 findings. However, 15 of Approach 2's closures were later reopened on retest. Using net closures, what is the cost per finding for each approach, and which is more cost-effective?

- A) £800 vs £900; Approach 1
- B) £800 vs £1,155; Approach 1
- C) £800 vs £1,155; Approach 2
- D) £933 vs £1,155; Approach 1

**Answer: B.** Approach 1: £84,000 ÷ 105 = £800 per finding. Approach 2 net closures: 68 − 15 = 53; £61,200 ÷ 53 = £1,154.7 ≈ £1,155 per finding. Approach 1 is more cost-effective on this measure. Option A uses gross closures for Approach 2 (£61,200 ÷ 68 = £900) — ignoring the reopened findings, which is exactly the quality signal a lead architect should insist on capturing. The deeper habit: whenever a unit-cost comparison is presented to you, ask what counts in the denominator and whether "done" was verified. Quality assurance of remediation is part of your patterns-and-QA duty, and the numbers only mean something if the denominator is honest.

**Question 13 (hard) — Compound growth in demand.** Security review requests to your team are growing 20% per quarter, compounding. This quarter you received 150 requests. Your team's capacity is fixed at 220 reviews per quarter. In how many quarters will demand first exceed capacity, and what backlog accrues in that first exceeding quarter?

- A) 2 quarters; backlog of 4
- B) 3 quarters; backlog of 39
- C) 3 quarters; backlog of 20
- D) 4 quarters; backlog of 91

**Answer: B.** Compound forward from 150: after 1 quarter, 150 × 1.2 = 180; after 2 quarters, 180 × 1.2 = 216; after 3 quarters, 216 × 1.2 = 259.2 ≈ 259. Demand first exceeds 220 in quarter 3, with backlog 259 − 220 = 39 (option C's 20 comes from misusing 240, the linear figure). Option A stops at 216, which is still under capacity — the near-threshold trap again. The strategic reading matters for your role: compounding demand against fixed capacity is the numerical argument for the very things your role profile expects you to build — reusable patterns, empowered lower-grade architects, and triage criteria — because hiring alone rarely compounds at 20% per quarter.

**Question 14 (easy) — Availability percentage.** Your protective monitoring platform's contract requires 99.5% monthly availability. In a 30-day month (720 hours), the platform was down for one incident of 4.5 hours. Was the service level met?

- A) Yes — availability was 99.38%
- B) No — availability was 99.38%
- C) Yes — availability was 99.63%
- D) No — availability was 98.5%

**Answer: B.** Downtime fraction: 4.5 ÷ 720 = 0.00625 = 0.625%. Availability: 100% − 0.625% = 99.375% ≈ 99.38%, which is below the 99.5% requirement — so the service level was not met. Option A pairs the right arithmetic with the wrong conclusion (99.38 < 99.5; the comparison is the whole point). The permitted downtime at 99.5% is 0.005 × 720 = 3.6 hours, so a 4.5-hour outage breaches it by 54 minutes. Computing the allowance first (3.6 hours) is usually faster and safer than computing the achieved percentage — a technique worth rehearsing, since monitoring and logging platforms underpin the assurance chains you advise risk owners about.

### Preparation tips

- **Refresh the small toolkit, not the big one.** Percentage change against the correct base, percentage-of-part versus percentage-of-whole, weighted averages, ceilings when sizing capacity, and compound growth cover almost everything at this level. Thirty minutes of deliberate practice on each pays off more than general maths revision.
- **Compute thresholds, then compare.** For any question with a tolerance, target or service level, calculate the threshold value in absolute terms first (56 projects, 3.6 hours, score of 12) and compare the scenario against it. It is faster and it defuses near-miss distractor options.
- **Interrogate denominators.** Before dividing, ask: net or gross? Detected cases only, or all cases? Which population is in scope? Most hard items at senior level hide their difficulty in the denominator, because that is where real dashboards hide theirs too.
- **Use the calculator for arithmetic, not for thinking.** Set up the operation on paper or in your head first, then compute. Candidates who reach for the calculator before framing the question make base-value and scope errors at speed.
- **Practise with your own metrics pack.** Take a recent vulnerability report, budget line or assurance dashboard and set yourself three questions about it: a percentage change, a threshold comparison, and a unit-cost calculation. Data you find realistic is data you will read fastest under time pressure — and this doubles as preparation for your next risk owner briefing, where the same figures will be read aloud and someone will ask you what they mean.
- **Explain one calculation aloud each day.** The role requires you to communicate risk figures to non-technical stakeholders; rehearsing the arithmetic in plain spoken English — "one in seven servers is still exposed, and at the current rate that closes by Friday" — cements both the calculation and the translation, and the assessments reward candidates who genuinely understand what each number is doing.

### Common pitfalls

- **Misreading scale qualifiers and units.** Confusing "per month" with "per quarter", missing "in thousands", or mixing hosts with host-hours. Read the column headers and units before the numbers.
- **Percentage-change base errors.** Measuring change against the new value instead of the original. If findings fall from 48 to 36, that is a 25% improvement, not 33%.
- **Answering the complement.** Computing the patched percentage when asked for the unpatched, availability when asked about breach. Re-read the question stem after calculating, before selecting.
- **Over-calculating.** Some items yield to estimation: if the choices are far apart, rounding 259.2 to 260 loses nothing. Save precision for items whose options sit close together — those near-threshold designs are exactly where care pays.
- **Time-sink questions.** A multi-stage cost model can consume five minutes you need elsewhere. Flag it, harvest the quicker items, and return. Unanswered easy questions are the most expensive mistake in any timed numeric test.


## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment evaluates how well you understand, analyse and draw correct conclusions from written material of the kind your role actually handles. The passages mirror your real reading load: security policies, technical standards, assurance and audit reports, supplier correspondence, governance papers and ministerial-adjacent briefings. The dominant question format is True / False / Cannot Say — you must judge each statement strictly against the passage, ignoring everything you know from outside it — supplemented by multiple-choice comprehension items on the main argument, tone or implication of a text. Timing is tight, usually under a minute per question once you have read the passage, which simulates scanning a forty-page assurance report an hour before a design authority meeting.

Why does this matter at your level? Because at lead level, words are the primary instrument of your influence. You "effectively translate and accurately communicate security and risk implications to technical and non-technical stakeholders"; you "feed back on policy and requirements"; you are starting to influence "policy and process, business architecture, and legal and political implications". Every one of those behaviours depends on reading precisely — knowing exactly what a policy mandates versus merely encourages, what an assurance finding proves versus suggests, and what a stakeholder's carefully worded email commits them to versus leaves open. Precision reading is also the foundation of precision writing, and your design decisions live or die by how they are recorded.

### What it measures for your role

- **Extracting obligations from policy and standards** maps to **Analysis** ("feed back on policy and requirements") and **Understanding security implications of transformation** ("start influencing policy and process... and legal and political implications"). Expect passages from security policies and standards, with statements testing whether you can separate "must" from "should" and scope from aspiration.
- **Reading assurance and risk material critically** maps to **Enabling and informing risk-based decisions** — items test whether a conclusion about risk is supported by the text or smuggled in from assumption.
- **Interpreting stakeholder communication** maps to **Communication (security architect)** ("manage stakeholder expectations and be flexible, adapting to stakeholder reactions to reach consensus") — passages include emails and meeting notes where tone and commitment must be judged from wording alone.
- **Understanding technical claims** maps to **Security technology** ("explain complex system architectures") and **Research and innovation** ("contribute to and inform developments on security properties in technology") — passages include vendor white papers and technology briefings where the gap between claim and evidence is the point.
- **Justifying decisions in writing** maps to your duty to "justify and communicate design decisions" — comprehension items ask what an architecture decision record actually argues, as opposed to what it might be assumed to argue.

### Practice questions

For True / False / Cannot Say items, use these definitions. True: the statement follows from the passage alone. False: the passage contradicts the statement. Cannot Say: the passage neither confirms nor contradicts it, however plausible it seems.

**Passage 1 — Departmental cryptography policy (extract).** "All new services processing personal data must encrypt that data in transit using protocols approved by the departmental cryptographic standards board. Services must encrypt personal data at rest unless the service owner has documented an exception approved by the Chief Information Security Officer (CISO). Exceptions expire after twelve months and may be renewed only once. Legacy services are expected to achieve compliance with this policy at their next major re-procurement. The standards board reviews approved protocols annually and may withdraw approval where weaknesses are identified."

**Question 1 (easy).** True, False, or Cannot Say: A new service processing personal data may store that data unencrypted at rest indefinitely, provided the CISO approves an exception.

**Answer: False.** The passage states that exceptions "expire after twelve months and may be renewed only once", which caps any exception at twenty-four months. "Indefinitely" is directly contradicted. Note the discipline: the question is not whether unencrypted storage is ever permissible (it is, temporarily, with an approved exception) but whether it can be indefinite — one word carries the whole answer, exactly as one word often carries a policy obligation.

**Question 2 (easy).** True, False, or Cannot Say: The departmental cryptographic standards board approves encryption protocols for data in transit.

**Answer: True.** The first sentence requires in-transit encryption "using protocols approved by the departmental cryptographic standards board". The board's approval role for transit protocols is stated explicitly. This is a straightforward retrieval item — assessments include them, and at your level the risk is overthinking: do not go hunting for a trap that is not there.

**Question 3 (moderate).** True, False, or Cannot Say: A legacy service processing personal data is currently in breach of this policy if it does not encrypt data at rest.

**Answer: False.** Read carefully: legacy services "are expected to achieve compliance... at their next major re-procurement". The policy therefore does not treat an unencrypted legacy service as currently in breach; it sets a future compliance point. The statement asserts a current breach, which the passage's transitional provision contradicts. Many candidates answer True by importing the general rule and ignoring the transitional clause, and some answer Cannot Say from caution — but the passage does speak to the question, and what it says undercuts the claim of a present breach. Transitional and grandfathering clauses are precisely what you check when feeding back on policy, because they determine what programmes must fund now versus later.

**Question 4 (moderate).** True, False, or Cannot Say: TLS 1.3 is one of the protocols approved by the standards board.

**Answer: Cannot Say.** The passage never names any protocol. You know from professional experience that TLS 1.3 would almost certainly be approved — and that knowledge is exactly what you must set aside. The passage confirms only that a board approves protocols and reviews them annually. This item type is the purest test of the "answer from the text alone" rule, and it is where subject-matter experts underperform novices unless they consciously suppress outside knowledge.

**Passage 2 — Assurance review findings (extract).** "The review examined the citizen identity platform against the agreed control set. Fourteen controls were assessed as fully effective, four as partially effective, and two as ineffective. Both ineffective controls relate to privileged access management: session recording was not enabled for two of the seven administrative gateways, and quarterly access recertification had not been completed for the March cycle. The review team notes that the platform team had already identified the recertification lapse and scheduled remediation prior to the review commencing. No evidence of exploitation of either weakness was identified during the review period. The review did not assess controls relating to the pending supplier migration, which will be examined separately."

**Question 5 (easy).** True, False, or Cannot Say: The review found that most assessed controls were fully effective.

**Answer: True.** Fourteen of twenty assessed controls (14 + 4 + 2 = 20) were fully effective; fourteen is more than half of twenty. Simple arithmetic embedded in text is common in verbal items — confirm the total before judging proportion words such as "most", "few" or "a minority".

**Question 6 (moderate).** True, False, or Cannot Say: The privileged access weaknesses were exploited during the review period.

**Answer: False — with a crucial nuance worth rehearsing.** The passage says "no evidence of exploitation... was identified during the review period". Strictly, absence of identified evidence is not proof of absence, and in your professional risk advice you would never equate the two. But the verbal reasoning convention judges the statement against what the passage asserts: the statement claims exploitation occurred, and the passage provides no support for it while actively asserting that none was found. Under test conventions the expected answer is **False**; a defensible purist could argue Cannot Say. When a real test presents this shape, prefer the reading the passage actively supports — and in your day job, keep making the distinction the test glosses over, because "no evidence of exploitation" versus "no exploitation" is exactly the kind of risk implication you are paid to translate accurately for stakeholders.

**Question 7 (moderate).** True, False, or Cannot Say: The platform team learned of the recertification lapse from the review.

**Answer: False.** The passage states the platform team "had already identified the recertification lapse and scheduled remediation prior to the review commencing". The statement directly contradicts this sequence. Timeline reversals are a favourite distractor: when a passage establishes an order of events, expect at least one statement to quietly reverse it.

**Question 8 (hard).** True, False, or Cannot Say: The citizen identity platform's supplier migration controls are ineffective.

**Answer: Cannot Say.** The review explicitly did not assess controls relating to the supplier migration — they "will be examined separately". Nothing in the passage supports any judgement about them, favourable or unfavourable. The trap is proximity: the passage discusses ineffective controls and mentions the migration in the same breath, and a fast reader pattern-matches "ineffective" onto "migration". Scoping statements — what a review did not cover — are among the most consequential sentences in any assurance report you will ever quality-assure, because unexamined scope is where residual risk hides.

**Question 9 (moderate) — multiple choice.** Which statement best characterises the overall tenor of the assurance findings in Passage 2?

- A) The platform is fundamentally insecure and requires immediate escalation
- B) The control environment is largely effective, with material weaknesses concentrated in privileged access management, partially mitigated by the team's own detection and planned remediation
- C) The review exonerates the platform team of all weaknesses
- D) The findings are invalid because the supplier migration was excluded

**Answer: B.** Fourteen of twenty controls fully effective supports "largely effective"; both ineffective controls sit in privileged access management, supporting "concentrated"; the team's prior self-identification and scheduled remediation supports "partially mitigated". Option A overstates — nothing in the text supports "fundamentally insecure". Option C overstates in the opposite direction — two controls were ineffective. Option D confuses a scope limitation with invalidity. Summarising an assurance report in one fair sentence is precisely the skill you use when briefing a senior risk owner who will read nothing but your summary.

**Passage 3 — Email from a programme director.** "Thank you for your paper on the proposed zero trust access pattern. I recognise the long-term case and I am not opposed in principle. However, the programme's position is that we cannot absorb the migration effort this financial year while the case-handling replacement remains our critical path. If your team can demonstrate that the pattern can be adopted for the two new services without touching the legacy estate, and that doing so will not add more than two weeks to their delivery schedules, I am willing to take a revised proposal to the programme board in November. I should say plainly that several board members remain unconvinced that the current controls are deficient, and a proposal framed as remediation of deficiency will meet resistance that a proposal framed as enabling the new services may not."

**Question 10 (moderate).** True, False, or Cannot Say: The programme director opposes the zero trust access pattern.

**Answer: False.** She writes that she recognises "the long-term case" and is "not opposed in principle", and she offers a concrete route to the programme board in November. The passage contradicts the claim of opposition. What she opposes is absorbing the migration effort this financial year — an objection to timing and scope, not to the pattern. Distinguishing opposition to a proposal from opposition to its current framing is the daily craft of "adapting to stakeholder reactions to reach consensus", and this item rewards reading her position rather than her hesitations.

**Question 11 (hard).** True, False, or Cannot Say: The programme board will approve the proposal if it is framed as enabling the new services.

**Answer: Cannot Say.** The director says such framing "may not" meet the resistance that a deficiency-remediation framing would — a comparative judgement about resistance, not a prediction of approval. No sentence commits the board to approving anything, and the director controls only what she takes to the board, not the outcome. Candidates who conflate "will face less resistance" with "will be approved" turn a conditional, hedged offer into a guarantee — exactly the over-reading that damages stakeholder trust when it appears in your write-up of a meeting.

**Question 12 (moderate) — multiple choice.** What conditions must be met before the director will take a revised proposal to the programme board?

- A) The pattern must be adopted across the legacy estate within two weeks
- B) The pattern must be shown adoptable for the two new services without touching the legacy estate, adding no more than two weeks to their delivery schedules
- C) The board members must first agree the current controls are deficient
- D) The case-handling replacement must complete first

**Answer: B.** The email states both conditions in a single conditional sentence: adoption "for the two new services without touching the legacy estate" and "not add more than two weeks to their delivery schedules". Option A garbles the two-week condition into a migration deadline. Option C reverses the director's advice — she suggests avoiding the deficiency framing precisely because the board is unconvinced. Option D confuses the stated reason for this year's constraint with a precondition for the November proposal. Extracting exact conditions from stakeholder correspondence is what allows you to meet them — and to hold others to them.

**Passage 4 — Vendor white paper (extract).** "Our platform applies homomorphic encryption to enable computation on encrypted datasets, meaning sensitive data need never be decrypted during analysis. In benchmark tests conducted by our engineering team, query latency on encrypted data averaged 3.2 times that of equivalent plaintext queries, an overhead our customers in regulated sectors have found acceptable for batch analytical workloads. The platform is undergoing evaluation against the relevant national cyber security guidance, and we anticipate alignment being confirmed in the coming months. Adoption by three European government agencies demonstrates the platform's suitability for public sector deployment."

**Question 13 (moderate).** True, False, or Cannot Say: The platform has been confirmed as aligned with the relevant national cyber security guidance.

**Answer: False.** The passage says the platform "is undergoing evaluation" and the vendor "anticipate[s] alignment being confirmed in the coming months". Confirmation has not happened; the statement asserts it has, which the passage contradicts. Vendor prose is engineered so that anticipated outcomes read like achieved ones on a fast skim — "undergoing evaluation" sits one careless read away from "evaluated". Your Research and innovation skill — identifying new technologies and designing their use in the business context — begins with refusing that careless read.

**Question 14 (hard).** True, False, or Cannot Say: The benchmark tests were independently conducted.

**Answer: False.** The passage attributes the benchmarks to "our engineering team" — the vendor's own. The statement claims independence, which the passage's attribution contradicts. A subtle point: if the passage had not named who conducted the tests, the answer would be Cannot Say; it is the explicit attribution that makes it False. Provenance of evidence is a detail you weigh every time you evaluate a security technology claim, and assessments reward noticing who is speaking, not just what is said.

**Question 15 (hard) — multiple choice.** Which is the strongest criticism of the white paper's final sentence ("Adoption by three European government agencies demonstrates the platform's suitability for public sector deployment")?

- A) It does not name the agencies
- B) It treats adoption as demonstrating suitability — adoption by others is evidence of their decisions, not proof the platform suits your context, requirements or risk tolerance
- C) European agencies are irrelevant to UK deployment
- D) Three is too small a number to be statistically significant

**Answer: B.** The sentence's logical flaw is the leap from "others adopted it" to "it is suitable" — adoption decisions by unnamed agencies, with unknown requirements, workloads and risk appetites, cannot demonstrate suitability for your deployment. Option A is a fair transparency quibble but not the core flaw; even named agencies would not repair the inference. Option C overcorrects — other governments' experience can be relevant evidence, just not demonstrative proof. Option D imports a statistical frame the claim never invoked. Dismantling an argument at its inferential joint, rather than at its surface details, is what "successfully respond to challenges" looks like when the challenge runs in the other direction — when you are the one challenging.

**Passage 5 — Draft security principle for consultation.** "Principle 7: Security decisions should be made at the lowest competent level. Teams should resolve routine security questions using published patterns and guardrails without escalation. Questions involving novel technology, cross-departmental data sharing, or departures from published patterns must be escalated to the lead security architect. The lead security architect may delegate any decision except those involving departures from statutory obligations, which must be referred to the Senior Information Risk Owner. This principle does not remove any team's accountability for the security of what it builds."

**Question 16 (moderate).** True, False, or Cannot Say: Under Principle 7, the lead security architect may delegate a decision involving cross-departmental data sharing.

**Answer: True.** Cross-departmental data sharing questions must be escalated to the lead security architect — but once there, the principle says the lead "may delegate any decision except those involving departures from statutory obligations". Cross-departmental data sharing is not in the non-delegable category, so delegation is permitted. Two rules interact here: an escalation rule (what must come to you) and a delegation rule (what you may pass on), and the statement is judged against their combination. Multi-rule interaction items reward the same layered reading you apply when policies, patterns and legal obligations overlap on a single design.

**Question 17 (easy).** True, False, or Cannot Say: Escalating a security question to the lead security architect transfers accountability for the security of the service to the architect.

**Answer: False.** The final sentence states plainly: "This principle does not remove any team's accountability for the security of what it builds." Escalation routes decisions; it does not transfer accountability. This sentence exists in the draft precisely because people assume otherwise — and when you feed back on policy drafts, you are often the one insisting such a sentence goes in.

**Passage 6 — Transformation programme briefing (extract).** "The programme will consolidate eleven departmental case-management systems onto a single shared platform over three years. Phase one migrates the four systems that hold no special category data. The business case assumes decommissioning savings of £3.1 million per year once all eleven systems are retired, and these savings are already committed against future budgets. Legal advice received in May confirmed that three of the remaining seven systems process data under distinct statutory regimes, and that a data-sharing framework will be required before their records can co-exist on shared infrastructure. The programme board has asked the security architecture team to advise whether logical separation on the shared platform would satisfy the framework's likely requirements, noting that physical separation would reduce the projected savings by an amount not yet quantified."

**Question 18 (moderate).** True, False, or Cannot Say: The decommissioning savings of £3.1 million per year will be achieved.

**Answer: Cannot Say.** The passage says the business case assumes these savings and that they are "already committed against future budgets" — a statement about planning and commitment, not about achievement. Indeed, the final sentence flags a scenario (physical separation) that would reduce them by an unquantified amount, so the outcome is explicitly open. Committed is not achieved; assumed is not delivered. Reading a business case this way is central to understanding the security implications of transformation: your advice on separation directly shapes whether a number the organisation has already spent on paper can be realised.

**Question 19 (hard).** True, False, or Cannot Say: A data-sharing framework is required before any of the eleven systems can migrate to the shared platform.

**Answer: False.** The framework requirement attaches to "three of the remaining seven systems" that "process data under distinct statutory regimes" — and specifically before their records can co-exist on shared infrastructure. Phase one, migrating four systems holding no special category data, carries no stated framework precondition. The statement over-generalises a condition from three systems to all eleven, which the passage's structure contradicts. Precision about which obligations attach to which systems is exactly the legal-and-political-implications reading your role increasingly demands.

**Question 20 (moderate) — multiple choice.** What has the programme board actually asked of the security architecture team?

- A) To design the data-sharing framework
- B) To advise whether logical separation on the shared platform would satisfy the framework's likely requirements
- C) To quantify the savings reduction from physical separation
- D) To approve the migration of the remaining seven systems

**Answer: B.** The request is stated verbatim in the final sentence. Option A confuses advising against a framework's likely requirements with authoring the framework — a scope inflation that, accepted silently, would commit your team to legal drafting it should not own. Option C is the board's own noted caveat, not the request. Option D appears nowhere. Restating a stakeholder's request in its exact scope — before you respond to it — is the first move of managing expectations, and test items reward the same exactness.

### Preparation tips

- **Drill the Cannot Say discipline.** The single highest-value habit is asking, for every statement: where exactly in the passage is this confirmed or contradicted? If you cannot point to the words, the answer is Cannot Say — no matter how confident your professional instincts are. As a domain expert you carry more outside knowledge into these tests than most candidates, which makes this discipline more important for you, not less.
- **Mark the modal verbs.** Must, should, may, expected to, anticipated: policy meaning lives in these words, and so do test answers. Question 3 turned on "are expected to"; Question 16 turned on "may delegate any decision except". Read them the way you read them in a real standard — because that is what the test simulates.
- **Watch attribution and timeline.** Who conducted the tests? What happened before the review commenced? When a passage establishes provenance or sequence, expect a statement that quietly alters it.
- **Read the statement before re-reading the passage.** Under time pressure, read the passage once for structure, then locate each statement's subject and scan for the governing sentence. Hunting keywords beats re-reading, and it mirrors how you actually interrogate a long assurance report.
- **Practise on your genuine reading load.** Take a policy extract, a supplier white paper and a stakeholder email from your own inbox, write three True/False/Cannot Say statements for each, and answer them a day later. Self-authored items teach you where ambiguity comes from — a bonus for your own drafting.

### Common pitfalls

- **Importing expertise.** The most dangerous pitfall for senior specialists. You know what NCSC guidance says, what TLS versions are current, what good privileged access management looks like — and none of it is admissible. Only the passage counts.
- **Confusing "no evidence found" with "did not happen", and "anticipated" with "achieved".** Passages at this level are written to test exactly these gaps, because real assurance reports and vendor papers contain them.
- **Over-reading stakeholder language.** "Willing to take a revised proposal to the board" is not "the board will approve". Conditional, hedged commitments must be recorded as exactly what they are.
- **Missing scope statements.** "The review did not assess..." changes what every other sentence can support. Scope sentences are short, dull and decisive — in tests and in the assurance reports you quality-assure.
- **Spending too long on the first read.** Candidates who try to memorise a dense passage before seeing the questions run out of time. Skim for structure, then let each statement direct your re-reading.


## Workplace job-specific situational judgement assessment

### About this assessment

A workplace job-specific situational judgement assessment evaluates your decision-making, interpersonal effectiveness and professional conduct through realistic workplace dilemmas. Unlike cognitive or numeric tests, there is rarely a single objectively right answer: several responses may be defensible, but one aligns best with the values of the organisation and the demands of the role. For your role, that means dilemmas about escalations from junior architects, senior stakeholders resisting security advice, risk decisions under delivery pressure, cross-departmental influence, and the tension between innovation and assurance. Response formats are usually "select the most effective and least effective actions" or "rank all options from best to worst". Timing is generous or absent — the assessment measures your natural judgement, not your speed.

At lead level, situational judgement is arguably the assessment closest to your actual job. Your role profile is dominated by behavioural expectations: interacting with senior stakeholders across departments, reaching and influencing a wide range of people across larger teams and communities, being the point of escalation for lower-grade architects, managing stakeholder expectations and adapting to reach consensus, and advising risk owners on whether complex risks sit within tolerance. The scoring frame for UK public sector assessments reflects public sector values: focus on user needs, transparency and openness, collaboration across boundaries, accessibility and inclusion, and evidence-based decision-making. Options that hoard information, bypass accountable owners, delay decisions without cause, or optimise personal convenience over service outcomes score poorly — however efficient they might feel in the moment.

### What it measures for your role

- **Stakeholder influence and consensus-building** maps directly to **Communication (security architect)**: "manage stakeholder expectations and be flexible, adapting to stakeholder reactions to reach consensus" and "successfully respond to challenges". Expect dilemmas where your technically correct position is resisted and the effective response is neither capitulation nor escalation-by-default.
- **Risk advice under pressure** maps to **Enabling and informing risk-based decisions**: "work with higher impact or more complex risks, advising on the impact and whether it's within risk tolerance". Expect dilemmas separating your advisory role from the risk owner's decision rights.
- **Leadership of the architecture community** maps to your duties to "be the point of escalation for architects in lower grade roles" and to "develop vision, principles and strategy". Expect dilemmas about developing people versus doing their work for them.
- **Innovation with responsibility** maps to **Research and innovation**: "identify new technologies and design the use of these in the business context" and "engage with the broader security community". Expect dilemmas balancing exploration against assurance and openness.
- **Transformation judgement** maps to **Understanding security implications of transformation**: "start influencing policy and process, business architecture, and legal and political implications". Expect dilemmas where security intersects with legal duties, budgets and departmental politics.

### Practice questions

For each scenario, decide which option is MOST effective and which is LEAST effective before reading the analysis. The explanations discuss every option, because the reasoning between the extremes is where judgement lives.

**Question 1 (moderate) — The deadline versus the penetration test.** A delivery manager on one of your projects tells you, copied to the senior responsible owner (SRO), that the planned penetration test must be dropped to hit a ministerially announced launch date. The service handles citizen financial data. The junior security architect on the project has objected and escalated to you.

- A) Reply to all, stating that the test is mandatory and the launch must slip.
- B) Meet the delivery manager to understand the constraint, then present the SRO with options and their risk implications — for example a scoped pre-launch test of the highest-risk components with a full test immediately after launch, alongside the risks of launching untested — and record the SRO's decision.
- C) Accept the delivery manager's decision; the launch date is a ministerial commitment and outranks testing.
- D) Tell the junior architect to log the risk in the risk register and take no further action.

**Most effective: B. Least effective: C.** Option B does everything the role demands: it treats the delivery constraint as real rather than adversarial, generates options rather than a binary, quantifies risk implications so the accountable owner can decide, and creates a record — the essence of "advising on the impact and whether it's within risk tolerance" while managing stakeholder expectations. Option A may feel principled, but declaring the launch "must slip" by reply-all exceeds your authority (the SRO owns that trade-off), corners the delivery manager publicly, and forfeits the consensus your role exists to build; it is the second-weakest option. Option C is least effective: it abandons the security advisory role entirely, leaves citizen financial data untested against a known launch, and teaches the junior architect that escalation to you is pointless. Option D is passive — a register entry without advice is bureaucratic cover, not risk enablement, and it fails the junior architect who escalated in good faith.

**Question 2 (moderate) — The junior architect's flawed design.** A security architect two grades below you asks you to review their proposed design for a data-exchange service before it goes to the design authority tomorrow. You spot a significant flaw: the design trusts an upstream partner's input validation. The architect has clearly worked hard and is visibly anxious about the review.

- A) Rewrite the design yourself tonight so it passes.
- B) Point out the flaw, explain the principle it violates (re-establish security properties at each trust boundary), work through the fix with them so they can present it as their own, and suggest they add the case to the community's pattern examples.
- C) Let the design go forward unchanged; the design authority will catch the flaw, and that is what the process is for.
- D) Tell them the design is fine to avoid denting their confidence, and quietly flag the flaw to the design authority chair.

**Most effective: B. Least effective: D.** Option B fixes the design, develops the architect, and converts one project's flaw into a reusable community lesson — the full expression of being "the point of escalation" while developing people and patterns. Option A fixes tonight's problem and creates next month's: the architect learns nothing, and your span of control becomes the community's bottleneck. Option C gambles a real service on a review catching what you already caught, and wastes the design authority's time on a preventable finding — process is a backstop, not a substitute for leadership. Option D is least effective because it is dishonest twice over: it deceives the architect ("the design is fine"), then engineers their public failure at the authority while destroying trust in you if either deception surfaces. Transparency is a public sector value precisely because options like D corrode everything they touch.

**Question 3 (hard) — The risk owner who wants a different answer.** You have advised that a proposed supplier integration carries a risk beyond the department's stated tolerance: the supplier's offboarding controls are weak, and the integration would give them standing access to a sensitive dataset. The risk owner, a director under pressure to deliver a shared-services commitment, asks you to "take another look and see if the risk can be scored lower".

- A) Rescore the risk lower; the risk owner has the authority to set risk appetite, and maintaining the relationship matters for future influence.
- B) Restate your assessment with the evidence behind it, make clear the scoring is yours to advise and the acceptance decision is theirs to make and document, and offer to explore additional controls — such as time-bounded credentials and enhanced monitoring — that could genuinely bring the risk within tolerance.
- C) Refuse to discuss it further and copy your assessment to the director's superior.
- D) Agree to re-examine the evidence, and if nothing has changed, quietly leave the score as it is without telling the director.

**Most effective: B. Least effective: A.** Option B holds the line that matters — the integrity of your professional assessment — while opening the door that should be open: real risk reduction through additional controls, and a properly documented acceptance decision if the director chooses to proceed. It separates advisory and ownership roles exactly as "enabling and informing risk-based decisions" requires. Option A is least effective: rescoring evidence-based advice to suit authority corrupts the entire risk system — every future score from your team becomes negotiable, and the sensitive dataset is exposed with the paper trail claiming it is not. Option C escalates before influence is exhausted, treats a pressured director as an adversary, and spends trust you will need across departments for years; escalation may eventually be right, but as a later resort with the director informed. Option D avoids confrontation by deception-through-silence: the director believes a re-examination is under way and will discover, at the worst moment, that the answer never changed and nobody said so.

**Question 4 (moderate) — The conference disclosure.** At a security community conference, a peer from another department describes, over coffee, an architectural weakness in a shared cross-government platform your department also consumes — apparently not yet reported through any formal channel. They mention it casually and move on.

- A) Report the weakness promptly through your department's and the platform's appropriate security channels, tell your peer you are doing so and encourage them to report it through their own channel too.
- B) Say nothing; it is the other department's information and their responsibility to report.
- C) Post an anonymised description to the cross-government security community forum to crowdsource opinions on severity.
- D) Quietly implement compensating controls for your own department's use of the platform, without reporting.

**Most effective: A. Least effective: C.** Option A does the two things that matter: gets the weakness to the people who can fix it, with provenance, and preserves transparency with your peer — telling them you will report is both courteous and coalition-building, exactly the "engage with the broader security community" behaviour your role names. Option B mistakes courtesy for responsibility: once you know about a weakness in a platform your department consumes, sitting on it is a personal failure to protect your users. Option D protects your department while leaving every other consuming department exposed — a collaboration failure dressed as diligence. Option C is least effective: broadcasting an unreported weakness, even anonymised, to a wide forum before the platform owner knows maximises the chance of hostile discovery while formal remediation has not begun. Responsible disclosure runs through owners first, communities later.

**Question 5 (hard) — The strategy nobody asked for.** You believe your organisation needs a security architecture strategy for its expanding use of machine-learning services: three projects are independently making inconsistent security decisions about model access, training data and third-party APIs. No one has commissioned a strategy, your own project portfolio is full, and the chief architect is preoccupied with a data centre exit.

- A) Draft a comprehensive sixty-page strategy in your own time and circulate it widely for adoption.
- B) Raise the inconsistency at the chief architect's community meeting, propose a short interim position — three or four binding principles for ML security decisions — and volunteer to lead a small working group from across the three projects to draft it for the chief architect's endorsement.
- C) Do nothing until a strategy is commissioned; working uncommissioned wastes effort.
- D) Advise each of the three projects separately as they ask, keeping your guidance consistent yourself.

**Most effective: B. Least effective: C.** Option B is what "develop vision, principles and strategy for one project or technology" looks like in practice: it names the problem where governance can see it, right-sizes the response (interim principles now, not a treatise), borrows legitimacy properly (the chief architect's endorsement), and builds the cross-project coalition that makes principles stick. Option A produces an artefact without a mandate — sixty uncommissioned pages circulated widely reads as empire-building, and its length guarantees it will not be read; effort is not influence. Option D is the quiet failure mode: your personal consistency helps the projects that happen to ask, scales exactly as far as your calendar, and leaves the structural inconsistency intact. Option C is least effective because it watches an identified, growing risk while waiting for permission to care — leads are expected to shape the agenda, not queue for it.

**Question 6 (moderate) — The accessibility objection.** Your proposed authentication pattern for a citizen-facing service mandates an authenticator app as the second factor. In review, a user researcher presents evidence that a significant minority of the service's users — disproportionately older and lower-income — do not have smartphones capable of running the app, and that assisted-digital routes are already strained.

- A) Keep the pattern as designed; security requirements cannot be compromised for edge cases.
- B) Withdraw the second factor requirement for this service to keep it accessible.
- C) Thank the researcher, and revise the pattern to offer equivalent-strength alternative factors — for example voice or SMS with compensating fraud controls, or a supported in-person route — explicitly documenting the accessibility requirement so the pattern library carries it to every future service.
- D) Suggest the accessibility problem is the service team's to solve, since your remit is security.

**Most effective: C. Least effective: A.** Option C treats the user researcher's evidence as a design input, not an obstacle — which is what focusing on user needs means when you hold the pattern pen. It preserves the security property (a second factor of equivalent strength, with compensating controls where channels are weaker) while meeting the users the service exists for, and it fixes the pattern library so the lesson propagates — your "produce particular patterns" duty working as intended. Option A is least effective: calling a significant, evidenced minority "edge cases" fails accessibility and inclusion obligations that are legal duties for government services, not preferences, and it entrenches the failure in a reusable pattern. Option B swings to the opposite failure, abandoning a security control for a citizen service rather than redesigning it. Option D is a remit dodge: security patterns that ignore how real users authenticate are not finished security work, and boundary-drawing in review meetings is the opposite of the cross-boundary collaboration your level requires.

**Question 7 (hard) — The pattern challenged in public.** At a cross-departmental architecture forum, a well-regarded principal engineer from another department publicly challenges a security pattern you authored, arguing its mandated network segmentation is obsolete in a zero trust model and "adds cost for theatre". Several attendees visibly agree. You believe the pattern remains right for the environments it targets, but the engineer's critique has genuine force for newer platforms.

- A) Defend the pattern point by point, and note that it went through proper governance and that forum criticism is not the route to change it.
- B) Acknowledge publicly the critique's force for newer platforms, distinguish the legacy environments where the segmentation still earns its cost, and invite the engineer to co-author a revision that scopes the pattern explicitly — bringing it back through governance.
- C) Withdraw the pattern for review, telling the forum it will return once the critique is resolved.
- D) Concede in the meeting that the pattern is probably outdated, to keep the room's goodwill.

**Most effective: B. Least effective: D.** Option B is "successfully respond to challenges" in its complete form: it neither capitulates nor entrenches, it makes the honest technical distinction (the pattern is right somewhere, not everywhere), and it converts a public critic into a co-author — turning a status contest into reusable work, with governance preserved. Option A defends process instead of substance; hiding behind governance when a critique has technical force reads as exactly that, and it squanders a chance to improve the pattern. Option C over-corrects: withdrawing a live pattern on the strength of one exchange creates a governance vacuum for every project currently building against it. Option D is least effective because it is neither true (you believe the pattern remains right for its target environments) nor consequential (goodwill bought by conceding what you believe is false costs your credibility and leaves projects without guidance) — consensus built on an untruth is not consensus, and your authority as an evidence-led adviser is the asset everything else depends on.

**Question 8 (moderate) — The shadow innovation.** You discover that a talented engineer on one of your projects has, without approval, built a working prototype that sends production log data to a third-party AI service to triage security alerts — and it works impressively well. The logs include internal hostnames and, occasionally, user identifiers.

- A) Report the engineer for a data-handling breach and require the prototype's immediate deletion.
- B) Praise the initiative and let the prototype keep running on production data while you seek retrospective approval.
- C) Stop the production data flow immediately, assess what data was exposed and trigger any required incident process, then work with the engineer to rebuild the evaluation properly — synthetic or sanitised data, an assessed supplier route — and sponsor it as a candidate innovation if it survives due diligence.
- D) Quietly stop the data flow and tell no one, to protect the engineer.

**Most effective: C. Least effective: B.** Option C keeps every plate spinning that must not drop: the ongoing exposure stops now, the past exposure is honestly assessed through proper process (user identifiers went to a third party — that may carry reporting obligations), and the innovation is preserved through a legitimate route, with you as sponsor rather than executioner. That is the balance your Research and innovation skill demands — identifying new technologies and designing their use in the business context, where "in the business context" means lawfully and assuredly. Option B is least effective: it endorses continuing exposure of production data, including user identifiers, to an unassessed third party — every day it runs is a bigger breach, and retrospective approval cannot retroactively unshare data. Option A protects the data but executes the messenger: it teaches the whole team to hide the next prototype, which is how shadow IT becomes systemic. Option D compounds the original failure with a cover-up — transparency obligations do not bend for likeable engineers, and the unassessed exposure may require disclosure regardless of anyone's intentions.

**Question 9 (moderate) — The competing escalations.** Two escalations reach you within an hour, and you can substantively address only one today. Escalation one: a junior architect on Project North reports the delivery team plans to go live on Friday without implementing the agreed logging controls; the service processes health-adjacent data. Escalation two: a senior developer on Project South complains that a security architect's review comments were dismissive in tone and the team is now reluctant to engage with security reviews at all.

- A) Take North today — an imminent go-live with missing controls on sensitive data is time-critical — and send South a same-day acknowledgement with a concrete commitment for this week, making clear you take the relationship damage seriously.
- B) Take South today — relationships are strategic and controls can be retrofitted after go-live.
- C) Handle North today and ignore South; teams complain about review tone all the time.
- D) Delegate North to the junior architect who raised it, and spend today on South.

**Most effective: A. Least effective: D.** Option A gets the triage right and — the detail that separates it from C — treats the second escalation as real. North is time-boxed by Friday's go-live and carries concrete risk to sensitive data; South is serious but not deteriorating by the hour. The same-day acknowledgement with a specific commitment costs minutes and preserves exactly the relationship the complaint says is fraying. Option C makes the identical prioritisation and then fumbles it: a team already "reluctant to engage with security reviews" that is then ignored becomes a team that stops engaging — and unengaged teams are tomorrow's shadow decisions. Option B inverts the urgency: "controls can be retrofitted after go-live" is the reasoning your junior architect escalated to you to prevent. Option D is least effective because it returns the North escalation to the person who escalated it — the junior architect raised it precisely because their grade lacks the leverage to stop a determined delivery team; sending it back is escalation theatre and leaves them exposed on Friday with nothing changed.

**Question 10 (hard) — The transformation shortcut with legal implications.** A transformation programme director tells you the programme intends to reuse an existing data-processing agreement to cover a new analytics capability that combines citizen datasets in ways the original agreement never contemplated. "Legal reviewed the original agreement two years ago," the director says, "and re-opening it would cost us three months. Your architecture works either way — I need you to stay in your lane on this one."

- A) Stay in your lane as instructed; data-processing agreements are a legal matter, and you have no legal qualification.
- B) Tell the director you will not sign off any architecture until legal re-reviews the agreement.
- C) Explain that the combination of datasets changes the processing in ways that are material to both security architecture and the agreement's coverage, put your concern and its rationale in writing to the director, and recommend a scoped legal question — which need not take three months — while flagging that you will need to note the open issue in the design's risk documentation either way.
- D) Raise the issue directly with the departmental data protection officer without telling the director.

**Most effective: C. Least effective: A.** Option C does the lead-level move: it rejects the "lane" framing on the merits — your role profile explicitly extends to "legal and political implications" of transformation, and new combinations of citizen data are squarely a security architecture concern — while keeping the director inside the conversation and offering a proportionate path (a scoped question, not a three-month re-opening). Putting the rationale in writing and noting the issue in risk documentation is transparency, not aggression: the record exists whichever way the director decides, which is precisely what keeps decisions honest. Option A is least effective: accepting the lane-marking means the one professional who has noticed that the processing has materially changed agrees to un-notice it — and "I was told it was legal's problem" protects neither citizens nor you. Option B may become necessary, but as an opening move it converts a resolvable disagreement into an ultimatum before proportionate options are explored. Option D reaches the right kind of authority the wrong way: going around the director covertly, before telling them your concern in writing, spends trust that the written, transparent route in C preserves — escalate openly if C fails, not secretly instead of it.

**Question 11 (moderate) — Ranking: the vision rollout.** You have drafted security architecture principles for your programme's next three years, endorsed by the chief architect. Now you must make them real across four delivery teams, two of which have never worked with a security architect. Rank these four first moves from most to least effective.

- A) Email the principles document to all four teams and ask them to confirm compliance within a month.
- B) Run a working session with each team on their current designs, showing where each principle changes a live decision and where their existing practice already complies.
- C) Build the principles into the design review checklist and reject non-compliant designs at the next review cycle.
- D) Recruit one interested engineer from each team as a security champion, brief them deeply, and support them to socialise the principles inside their teams.

**Most effective ranking: B, D, C, A.** B leads because principles land when teams see them deciding something real — their designs, their decisions — and because crediting existing compliant practice ("you already do this") converts principles from imposition into recognition; this is "reach and influence a wide range of people" done in person, where influence actually happens. D is a strong second and the best long-term multiplier — champions sustain what workshops start — but as a first move it delegates the initial encounter with the principles to people who have not yet internalised them; it works best immediately after B. C has a place — enforcement gives principles teeth — but leading with rejection teaches two teams whose first-ever experience of security architecture would be a failed review that security is a gate, not a partner; it earns its keep once B and D have built understanding. A is least effective: an emailed document with a compliance deadline is a broadcast, not influence — it will be skimmed, filed and confirmed without being read, achieving the appearance of adoption while changing nothing, which is worse than changing nothing visibly.

### Preparation tips

- **Anchor on role, values and rights.** For every option, ask three questions. Whose decision is this — am I advising, deciding or overreaching? Which public sector values does this option serve or betray — user needs, transparency, collaboration, accessibility, inclusion? What does this option teach the people watching — junior architects, delivery teams, stakeholders? The best option usually scores well on all three.
- **Beware the satisfying option.** At senior level, the tempting wrong answers are the ones that feel decisive: the reply-all correction, the design rewritten overnight, the covert escalation. Effectiveness in your role is usually the option that keeps the most people inside the conversation while the risk is still controlled.
- **Least effective is often passive or deceptive.** Across published assessments, the lowest-scoring options overwhelmingly either delay without cause, pass the problem to someone who cannot solve it, or involve any form of deception — including deception by silence. If an option hides information from someone entitled to it, it is a strong candidate for least effective.
- **Read the scenario's constraints as data.** "Copied to the SRO", "goes to the design authority tomorrow", "committed against future budgets" — these details define what the effective option must handle. Options that ignore a stated constraint are rarely the answer.
- **Calibrate against your best real decisions.** Before the assessment, recall three situations you handled well — an escalation, a resisted recommendation, a public challenge — and articulate why what you did worked. You are not learning new behaviour for this test; you are making your existing judgement explicit and consistent.

### Common pitfalls

- **Answering idealistically rather than effectively.** "Halt everything until it is perfect" sounds principled and scores poorly, because it ignores the legitimate pressures — delivery, budgets, ministerial commitments — that the effective option must work with, not wish away.
- **Choosing personal heroics over system leadership.** Rewriting the junior architect's design, absorbing every escalation yourself, being the sole guardian of consistency: these options flatter your competence and fail your role, which is to build a community and patterns that work when you are not in the room.
- **Escalating too early — or too covertly.** Escalation is a legitimate tool that scores badly when used before influence is attempted, or behind the back of the person concerned. The pattern that scores well is: engage, document, offer options, then escalate openly if needed.
- **Ignoring the values frame.** UK public sector assessments score against user needs, transparency, collaboration, accessibility and inclusion. An option that is operationally efficient but opaque, exclusionary or user-hostile will rank lower than its efficiency suggests it should.
- **Forgetting who owns the risk.** Several dilemmas at this level turn on the line between advising on risk and accepting it. Options where you silently absorb a risk decision that belongs to a risk owner — or force one that is yours to advise on — are consistently marked down.

## Conclusion

You have worked through a substantial set of resources: an orientation to psychometric assessment at lead level, and four full practice sections — cognitive, numeric reasoning, verbal reasoning and situational judgement — each built from the real substance of your role. The scenarios you reasoned through were not generic: they were firewall rule tables and trust boundaries, risk scores and remediation budgets, policy extracts and assurance findings, resistant directors and anxious junior architects. If they felt familiar, that is the point — and it is also the encouragement to take away. These assessments measure thinking you already do every working day.

A few closing thoughts. First, treat your results — in practice and in any real assessment — as information, not verdict. A slow patch on percentage-change arithmetic or a hesitation over Cannot Say items is a development note for a week of deliberate practice, nothing more. Second, notice how consistently the four assessments converge on a small set of professional virtues: read the exact words, test conclusions against evidence, respect scope and thresholds, keep people inside the conversation, and remember who owns each decision. Strengthening any one of these strengthens your performance across all four assessments — and across the job itself. Third, keep practising in the medium of your actual work. Your metrics packs, policy drafts, assurance reports and stakeholder emails are a permanently refreshed question bank; ten minutes of deliberate, explicit reasoning about them each day is worth more than any commercial practice set.

Finally, remember what these assessments are for. They exist because roles like yours matter: the systems you shape carry citizens' data, benefits, health records and trust. The same care you have just practised — precise reading, honest numbers, disciplined logic, humane judgement — is what earns you the influence your role profile describes: reaching people across teams and communities, shaping policy and strategy, and being the escalation point others rely on. You are well prepared. Keep developing, keep engaging with your professional community, and walk into any assessment the way you walk into a design authority meeting: prepared, curious, and confident in the quality of your reasoning.

