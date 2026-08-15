# Security Architect (Principal Security Architect) - Psychometric Assessment Resources

## Introduction

Welcome. This document is a practical, self-directed resource to help you prepare for psychometric assessments relevant to your role as a Principal Security Architect within the UK Government Digital and Data (GDAD) profession. Whether you are preparing for an internal promotion board, a move to another department, an external opportunity, or simply want to sharpen the mental toolkit you rely on every day, this guide is designed for you.

Psychometric assessments are structured, standardised exercises that measure the underlying capabilities a role demands: how quickly and accurately you process information, how you reason with numbers and language, and how you exercise judgement in realistic workplace situations. At principal level, these assessments are rarely about raw speed alone. Assessors want evidence that you can absorb complex, ambiguous material — a board paper on cyber risk, a supplier's architecture proposal, a set of vulnerability metrics — and reach sound, defensible conclusions under time pressure. That is, in essence, a compressed version of what you already do when you set security strategy across an organisation, act as a point of escalation for senior risk owners, and make architectural decisions on services of high complexity and risk.

This document is organised into four assessment areas, each aligned to your role's skills as defined in the GDAD Profession Capability Framework:

1. **Workplace job-specific cognitive assessment** — pattern recognition, logical deduction, error checking and prioritisation using the artefacts a principal security architect genuinely handles: architecture diagrams, control frameworks, firewall rule sets and threat models.
2. **Workplace job-specific numeric reasoning assessment** — interpreting risk metrics, security programme budgets, remediation statistics and capacity figures, and reasoning about cost-benefit trade-offs in controls.
3. **Workplace job-specific verbal reasoning assessment** — drawing precise conclusions from dense written material such as security policies, assurance reports, legal guidance and senior stakeholder correspondence.
4. **Workplace job-specific situational judgement assessment** — exercising professional judgement in realistic dilemmas involving senior risk owners, delivery teams, suppliers and cross-government stakeholders.

Each section explains what the assessment measures, maps it explicitly to your role's skills, provides a substantial set of practice questions with worked answers, and closes with preparation tips and common pitfalls. Work through the questions actively: attempt each one before reading the explanation, note where your reasoning diverged, and revisit those areas. Used this way, the document supports practice, self-reflection and preparation in equal measure.

You bring deep expertise to this material already. Treat these exercises as an opportunity to make that expertise visible under assessment conditions — and enjoy the process.

## Advisory

"This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff."

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive ability assessment is a targeted psychometric test that measures the exact mental processes your role demands, using practical workplace scenarios rather than abstract puzzles. Unlike a generic IQ test, every stimulus mimics the everyday tasks and data formats of the actual job — for a Principal Security Architect, that means architecture diagrams, control mappings, access rules, vulnerability data and threat models. Assessments of this kind are typically delivered online, timed at around 15 to 30 minutes, objectively scored against a norm group, and validated so that questions predict job success without bias.

For a principal-level role, cognitive assessments carry particular weight because the role is defined by decision quality on services of high complexity and risk. When you set a long-term security strategy across the breadth of an organisation, you are performing sustained acts of pattern recognition (what recurs across these systems?), logical deduction (what must follow if this trust assumption fails?), error checking (which of these configurations contradicts the stated principle?) and prioritisation (which of these unprecedented problems do we solve first?). The assessment compresses those acts into short, sharply timed items. Expect a mixture of diagrammatic reasoning, rule-based deduction, consistency checking across documents, and ordering or scheduling problems. Modern platforms may adapt difficulty to your answers, and employers usually receive a breakdown of speed versus accuracy rather than a single score — so disciplined accuracy matters as much as pace.

### What it measures for your role

The assessment dimensions map directly onto the skills in your role profile:

- **Analysis.** Items that ask you to monitor a changing technical environment — a revised architecture, a new dependency, an altered data flow — and judge whether risks remain at acceptable levels or whether a previous decision must be revisited. Pattern-recognition and consistency-checking questions exercise exactly this.
- **Designing secure systems.** Deduction items built on system architectures test your ability to lead design and review of solutions to complex problems by reasoning from patterns and principles: given these components, trust boundaries and controls, what necessarily holds, and what has been violated?
- **Security technology.** Fault-finding items reflect your ability to explain complex system architectures and to identify how easy or difficult it would be to exploit a vulnerability, tracing exploit paths through layered controls.
- **Enabling and informing risk-based decisions.** Prioritisation items mirror your work applying risk methodologies at the most complex levels: ranking findings, sequencing remediations, and deciding what to escalate.
- **Understanding security implications of transformation.** Several items place a policy or process change alongside a technical estate and ask what logically follows — the cognitive core of challenging and leading changes to policy to support business outcomes.

### Practice questions

**Question 1 (easy) — Pattern recognition in firewall rule sets**

You are reviewing a perimeter rule set migrated between platforms. The original policy intent is: "Only the presentation tier may accept inbound internet traffic; the application tier accepts traffic only from the presentation tier; the database tier accepts traffic only from the application tier." The migrated rules are:

1. ALLOW internet -> presentation:443
2. ALLOW presentation -> application:8443
3. ALLOW application -> database:5432
4. ALLOW internet -> application:8443
5. DENY all (default)

Which rule violates the policy intent?

A) Rule 1
B) Rule 2
C) Rule 4
D) Rule 5

**Correct answer: C.**

**Explanation:** The intent permits internet traffic only to the presentation tier. Rules 1–3 each match one sentence of the intent, and rule 5 is the standard default deny. Rule 4 allows the internet to reach the application tier directly, bypassing the presentation tier — a classic tiering violation introduced during migration. At principal level you would also note the systemic lesson: migrations need automated policy-intent checking, not line-by-line eyeballing. In the assessment, though, the task is simply rapid, accurate matching of rules to stated intent.

**Question 2 (easy) — Logical deduction from security principles**

Your organisation's architecture principles state: "All services handling OFFICIAL data must authenticate service-to-service calls using mutual TLS. Services that cannot support mutual TLS must be placed behind an authenticating proxy." Service X handles OFFICIAL data and does not use mutual TLS. Which conclusion is logically required?

A) Service X is non-compliant with the principles.
B) Service X must be behind an authenticating proxy to be compliant.
C) Service X does not handle OFFICIAL data.
D) Service X must be decommissioned.

**Correct answer: B.**

**Explanation:** The principles offer a compliant alternative: services that cannot support mutual TLS must sit behind an authenticating proxy. So the absence of mutual TLS does not by itself establish non-compliance (eliminating A); it establishes a conditional obligation. C contradicts the given facts, and D is not stated anywhere. The trap in this item is jumping to "non-compliant" — the same trap that exists in real reviews when a control's stated exception path is overlooked. Deduction items reward reading the whole rule, including its escape clauses.

**Question 3 (moderate) — Error checking a control mapping**

You are quality-assuring a mapping of controls to requirements before it goes to a senior risk owner. The requirements say:

- R1: All administrative access must use multi-factor authentication (MFA).
- R2: All administrative actions must be logged to a central, tamper-evident store.
- R3: Administrative sessions must time out after 15 minutes of inactivity.

The submitted mapping says:

- R1 -> "Privileged access workstations issued to all administrators."
- R2 -> "All administrative actions logged to the central SIEM with write-once storage."
- R3 -> "Administrative sessions time out after 15 minutes of inactivity."

Which mapping is faulty?

A) R1
B) R2
C) R3
D) None of them

**Correct answer: A.**

**Explanation:** R2's mapping matches: central SIEM with write-once storage is a tamper-evident central store. R3's mapping restates the requirement exactly. R1, however, requires MFA, and the mapped control describes privileged access workstations — a valuable hardening measure, but not an authentication factor requirement. A control can be good and still not satisfy the requirement it is mapped to. Error-checking items at this level test whether you verify the logical fit between requirement and control rather than being satisfied by security-flavoured language. This is precisely the discipline you apply when you direct and influence others on best practice: plausible is not the same as compliant.

**Question 4 (moderate) — Exploit-path reasoning**

A system has these facts: (i) the public web front end runs in Environment A; (ii) Environment A can initiate connections only to the API gateway in Environment B; (iii) the API gateway validates a signed token on every request; (iv) the signing key is stored in a hardware security module (HSM) in Environment C; (v) Environment B has no route to Environment C except the HSM's signing interface. An attacker fully compromises the web front end. Which asset can the attacker reach directly?

A) The signing key material in the HSM
B) The API gateway, presenting requests without valid tokens
C) Arbitrary services in Environment B
D) Environment C's management plane

**Correct answer: B.**

**Explanation:** From the compromised front end, the only permitted connection is to the API gateway (fact ii), so C and D fall away immediately. The attacker can present requests to the gateway, but without a validly signed token those requests fail validation (fact iii) — reaching the gateway is not the same as passing through it. Key material inside an HSM is not extractable via a signing interface (facts iv–v), so A fails. The correct answer describes exactly what the attacker can touch: the gateway itself, unauthenticated. This mirrors your day job of identifying and explaining how easy or difficult it will be to exploit vulnerabilities — the assessment version simply asks you to trace reachability strictly from the stated facts.

**Question 5 (moderate) — Prioritisation under a risk methodology**

Your methodology scores findings as Impact (1–5) multiplied by Likelihood (1–5), and mandates that any finding on an internet-facing service has its likelihood raised by one point before scoring. Four findings await triage:

- F1: Internal HR system, Impact 4, Likelihood 3.
- F2: Internet-facing payments service, Impact 4, Likelihood 3.
- F3: Internet-facing content site, Impact 2, Likelihood 5.
- F4: Internal data warehouse, Impact 5, Likelihood 2.

Which finding should be remediated first?

A) F1
B) F2
C) F3
D) F4

**Correct answer: B.**

**Explanation:** Apply the internet-facing adjustment before multiplying. F2 becomes 4 × 4 = 16. F3 becomes 2 × 5 = 10 (likelihood is already at the maximum of 5, so the uplift cannot exceed the scale). F1 is 4 × 3 = 12 and F4 is 5 × 2 = 10. The ordering is F2 (16), F1 (12), F3 and F4 (10). The item tests two things: faithful application of a stated methodology, including its adjustment rule and its scale boundary, and resistance to intuition — many candidates reach for F4 because "impact 5" sounds worst. Applying risk methodologies at the most complex levels means following the method even when a single salient number tempts you elsewhere.

**Question 6 (moderate) — Sequencing a dependency chain**

You are planning the enforcement rollout of a zero trust architecture. The workstream dependencies are: identity provider consolidation must finish before device compliance signals can be integrated; device compliance signals must be integrated before conditional access policies can be enforced; network micro-segmentation can run in parallel with everything except that it must finish before legacy VPN decommissioning; conditional access enforcement must also precede legacy VPN decommissioning. Which task can begin immediately alongside identity provider consolidation?

A) Device compliance signal integration
B) Conditional access enforcement
C) Network micro-segmentation
D) Legacy VPN decommissioning

**Correct answer: C.**

**Explanation:** Micro-segmentation's only stated constraint is that it must complete before VPN decommissioning; nothing prevents it starting at once, in parallel with identity work. Device compliance integration (A) waits on identity consolidation; conditional access (B) waits on device compliance; VPN decommissioning (D) waits on both micro-segmentation and conditional access, making it last. Scheduling items like this reflect the strategic sequencing you perform when setting a long-term strategy across the breadth of the organisation: the skill is separating genuine dependencies from assumed ones.

**Question 7 (moderate) — Spotting the inconsistent artefact**

Three artefacts describe the same service. The architecture diagram shows citizen data flowing from the web tier to a UK-hosted database only. The data protection impact assessment (DPIA) states all citizen data is stored and processed in the UK. The infrastructure-as-code repository contains a module provisioning a read-replica of the database in an EU region for analytics. Assuming the repository reflects what is actually deployed, which single statement is best supported?

A) The DPIA is accurate and the diagram is wrong.
B) The diagram and DPIA are both inconsistent with the deployed reality.
C) The repository module must be a mistake.
D) Citizen data is not processed in the EU.

**Correct answer: B.**

**Explanation:** If a read-replica in an EU region is deployed, citizen data is stored (and plausibly processed) outside the UK. That contradicts the DPIA's "stored and processed in the UK" and the diagram's "UK-hosted database only" — both artefacts are inconsistent with reality, so B holds. A is half right at best, C assumes facts not given (the module may be deliberate but undocumented), and D contradicts the stated deployment. This is the assessment version of monitoring changes in the technical environment and assessing whether previous decisions need revisiting: documentation drift is itself a finding.

**Question 8 (moderate) — Abstract pattern with a security flavour**

A sequence of access-review cycles reduces standing privileged accounts as follows: 640, 320, 160, 80. A new joint programme then adds 24 privileged accounts, after which the halving pattern resumes. How many standing privileged accounts remain two cycles after the programme's accounts were added?

A) 20
B) 26
C) 40
D) 52

**Correct answer: B.**

**Explanation:** The pattern halves each cycle: 640 -> 320 -> 160 -> 80. Adding 24 gives 104. Two further halvings: 104 -> 52 -> 26. Option D is the trap for stopping after one cycle; A ignores the added accounts; C halves before adding. Sequence items reward writing the state at each step rather than holding it all mentally — the same habit that makes staged migration plans reviewable.

**Question 9 (hard) — Deduction across trust boundaries**

Consider four statements about a cross-government data-sharing platform: (1) Every consuming department signs a data-sharing agreement before receiving an API key. (2) Some API keys have been issued to analytics suppliers acting on behalf of departments. (3) No analytics supplier has signed a data-sharing agreement directly. (4) Every entity holding an API key can query citizen records. Which conclusion must be true?

A) Some entities can query citizen records without having signed a data-sharing agreement directly.
B) Analytics suppliers are in breach of the platform's rules.
C) Every department has an analytics supplier.
D) Citizen records have been accessed inappropriately.

**Correct answer: A.**

**Explanation:** From (2), some suppliers hold keys; from (3), none signed an agreement directly; from (4), key holders can query records. Therefore some entities (the suppliers) can query citizen records without a direct agreement — A follows necessarily. B does not follow: statement (1) binds departments before key issuance, and the rules as stated may permit issuance to agents under a department's agreement; nothing establishes a breach. C generalises far beyond "some". D confuses capability with action — being able to query is not evidence of inappropriate access. This is a syllogistic reasoning item dressed in your daily subject matter: the discipline is deducing only what the premises force, exactly as when you challenge a pattern by exposing what its assumptions do and do not guarantee.

**Question 10 (hard) — Fault diagnosis from layered evidence**

An internal service intermittently rejects legitimate requests with authentication errors. Facts: (i) errors began the same week a certificate authority (CA) rotation was completed; (ii) errors occur only on requests routed through the older of two load balancer pools; (iii) both pools terminate TLS; (iv) the newer pool's trust store was updated during the rotation; (v) service logs show "unknown issuer" on failing requests. What is the most probable cause?

A) The client applications are presenting expired certificates.
B) The older load balancer pool's trust store still lacks the new CA certificate.
C) The CA rotation reissued certificates with weak keys.
D) The service's session timeout is too aggressive.

**Correct answer: B.**

**Explanation:** Work the evidence like a truth table. "Unknown issuer" (v) points to a trust-store gap, not expiry (which would log as expired, eliminating A) and not key strength (C would fail validation differently and constantly, not by route). The fault correlates with one pool only (ii), and we are told the newer pool's trust store was updated (iv) — the natural inference is the older pool's was not. D cannot explain issuer errors at all. The item measures convergent fault diagnosis: intersecting several partial observations to isolate the single explanation consistent with all of them, the same reasoning you use when solving unprecedented issues and problems as the recognised expert in the room.

**Question 11 (hard) — Prioritisation with constrained capacity**

Your remediation squad can absorb 8 units of work this sprint. Five remediations are candidates: R1 (6 units, closes a critical internet-facing flaw), R2 (4 units, closes a high internal flaw), R3 (2 units, closes a high internet-facing flaw), R4 (3 units, unblocks a dependent programme but closes no flaw), R5 (2 units, closes two medium flaws). Policy requires all critical internet-facing flaws to be scheduled before anything else. Which combination best uses the sprint?

A) R1 and R3
B) R1 and R5
C) R2, R3 and R5
D) R1, R3 and R5

**Correct answer: A.**

**Explanation:** Policy forces R1 (6 units) in first, leaving 2 units. Both R3 and R5 fit the remaining capacity, so the choice between A and B is on merit: R3 closes a high-severity internet-facing flaw; R5 closes two mediums. Under any standard risk methodology a high internet-facing exposure outranks two mediums, so R3 wins and A is correct. C violates the policy by omitting R1; D exceeds capacity (6 + 2 + 2 = 10). The item combines a hard constraint, an arithmetic constraint and a judgement call — the everyday shape of directing remediation across several projects at once.

**Question 12 (hard) — Detecting a broken inference in someone else's analysis**

A supplier's assurance report argues: "Penetration testing found no exploitable vulnerabilities in the externally facing components. Therefore the service is secure against external attack." As reviewer, which single observation most precisely identifies the logical flaw?

A) Penetration tests are always superficial.
B) Absence of findings in the tested scope is evidence about that scope at that time, not proof of security against all external attack.
C) The supplier has a commercial incentive to report favourably.
D) Internal components were not tested.

**Correct answer: B.**

**Explanation:** The argument commits the classic leap from "no vulnerabilities found" to "no vulnerabilities exist", and from a bounded scope and moment to a universal claim. B names that flaw exactly. A is an overgeneralisation and untrue as stated. C attacks motive, not logic — it may warrant scrutiny but does not identify the inferential gap. D raises scope but misfires: the conclusion concerned external attack, and the external components were tested; the flaw is the strength of the inference, not the choice of scope. Items like this test the precision of your critique — essential when you successfully respond to challenges and when your review comments set precedents that other architects will follow.

**Question 13 (hard) — Transformation logic**

A department plans to replace its on-premises case-management system with a SaaS product. Current policy states: "Systems processing special category data must undergo a security architecture review before any data migration." Facts: the case-management system processes health data; the SaaS migration plan schedules data migration for March; no security architecture review is scheduled. If the plan proceeds unchanged, which statement must be true in March?

A) The migration will fail technically.
B) The department will act inconsistently with its own policy.
C) The SaaS product is insecure.
D) The policy will have been changed.

**Correct answer: B.**

**Explanation:** Health data is special category data, so the policy's condition applies; migrating without the required review is, by definition, action inconsistent with the policy. Nothing in the facts supports a technical failure (A) or any judgement about the SaaS product's actual security (C). D describes one way the inconsistency could be avoided, but the question stipulates the plan proceeds unchanged. The item rehearses the core cognitive move behind understanding security implications of transformation: hold the policy and the plan side by side and state precisely where they collide — no more, no less.

**Question 14 (moderate) — Odd one out in security patterns**

Four approved patterns are summarised for a pattern library review. Three share a common structural property; one does not. Which is the odd one out?

A) Pattern P1: external requests pass through an edge proxy that authenticates before any backend is reached.
B) Pattern P2: batch file transfers land in a quarantine zone and are scanned before entering the processing network.
C) Pattern P3: third-party webhooks are received by a broker that validates signatures before forwarding internally.
D) Pattern P4: internal microservices call each other directly, with each service logging requests after processing them.

**Correct answer: D.**

**Explanation:** P1, P2 and P3 all share the structural property of mediated ingress: an intermediary validates or sanitises inbound material before it touches the protected zone. P4 has no intermediary and its control (logging) is detective and applied after processing, not preventative and applied before. Classification items like this test whether you can abstract the structural principle from surface detail — the essence of defining and challenging patterns and principles. Note that P4 is not necessarily wrong as a design; it is simply structurally unlike the others, and the question asks only for the odd one out.

**Question 15 (hard) — Multi-document consistency under change**

A new national policy requires that "authentication events for public-facing services must be retained for 24 months". Your organisation's current standard mandates 12 months' retention, your flagship citizen service is configured for 12 months, and its storage budget was approved on that basis. Which set of artefacts must change for the organisation to become compliant, assuming the service remains public-facing?

A) Only the service configuration
B) Only the organisational standard
C) The organisational standard and the service configuration, with the budget likely to need revisiting
D) The national policy

**Correct answer: C.**

**Explanation:** Compliance requires actual retention of 24 months, so the service configuration must change. Leaving the organisational standard at 12 months would leave internal doctrine contradicting national policy and would mislead every future service built to it, so the standard must change too. Doubling retention has storage cost implications, so the approved budget is "likely to need revisiting" — the question's careful wording matters, because the budget is a consequence rather than a compliance artefact. A fixes one service but leaves the standard wrong; B fixes doctrine but not reality; D is outside your gift. This item rehearses cascade analysis: tracing a single policy change through standards, configurations and resources — the daily mechanics of leading change regarding factors that feed into analysis.

### Preparation tips

- **Rehearse with your own artefacts.** Spend ten minutes a day reading a firewall rule set, control mapping or architecture decision record and asking: what does this force, what does it forbid, what is inconsistent? You are converting daily expertise into timed-test fluency.
- **Practise stating rules before applying them.** In each item above, the winning move was restating the given rule precisely, then testing options against it. Under time pressure, one careful read beats three anxious skims.
- **Track state on paper.** For sequence, scheduling and capacity items, jot the state after each step. Principal-level candidates lose marks not to difficulty but to mental juggling.
- **Manage the clock strategically.** With 15 to 30 minutes for the whole test, allocate roughly a minute per item, bank the easy ones fast, and flag rather than fight any item that stalls you.
- **Do the platform's practice items.** Most providers offer ungraded warm-ups; use them to absorb the interface so no working memory is wasted on navigation.

### Common pitfalls

- **Answering from expertise instead of from the stimulus.** Your deep technical knowledge will sometimes suggest a "better" answer than the facts given support. Assessments score deduction from the material provided — as Question 9's option D showed, capability is not action.
- **Missing exception clauses in rules.** Real policies and test items alike contain "unless" and "must instead" branches; skimming past them turns right answers wrong (Question 2).
- **Being seduced by security-flavoured language.** A control described impressively may still fail to satisfy the requirement it is mapped against (Question 3).
- **Time-sink items.** One stubborn multi-stage item can cost you three easier ones. Skip, flag, return.
- **Ignoring scale boundaries and adjustments.** Methodology items often hide a capped scale or a mandated uplift (Question 5); apply every stated rule before computing.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment evaluates your ability to analyse, interpret and make sound decisions using numerical data drawn from the target role — business mathematics rather than abstract formulae. Question inputs are the tables, budgets, dashboards and schedules you genuinely encounter: for a Principal Security Architect, that means security programme budgets, vulnerability and patching metrics, incident statistics, licensing and capacity figures, and cost-benefit comparisons of controls. The mathematics itself stays deliberately practical — percentages, ratios, weighted averages, rates of change and cost estimations — because the test prioritises interpretation over mental gymnastics. Most platforms allow or provide an on-screen calculator, and nearly all impose a strict time limit, so quick, accurate data extraction matters as much as computation.

At principal level, numeric fluency underpins credibility. When you recommend security design up to an organisational or inter-organisational level, the case usually turns on numbers: what a control costs against the loss expectancy it reduces, whether a remediation trajectory will meet a compliance deadline, how a budget should be apportioned across competing programmes. Senior risk owners trust architects who can move between a technical judgement and its quantified consequence without hesitation. The assessment simulates exactly that movement, repeatedly, under time pressure.

### What it measures for your role

- **Enabling and informing risk-based decisions.** Loss-expectancy calculations, risk-score arithmetic and cost-benefit items reflect applying risk methodologies at the most complex levels — and presenting outcomes senior risk owners can act on.
- **Analysis.** Trend and threshold items (is the patching rate sufficient? has the risk profile shifted beyond tolerance?) mirror monitoring changes in the technical environment and assessing whether risks remain acceptable.
- **Communication (security architect).** Several items ask which figure best supports a message to a board or senior stakeholder — numeracy in service of accurately communicating security and risk implications at the most senior levels.
- **Research and innovation.** Technology-adoption items compare costs, capacity and benefit across candidate technologies, echoing how you validate and adopt new technologies for the business context.
- **Designing secure systems.** Capacity and scaling items quantify design consequences: throughput of an inspection layer, storage for logging, headroom in an authentication service.

### Practice questions

**Question 1 (easy) — Percentage of estate patched**

Your organisation runs 4,800 servers. A monthly report shows 4,272 have the latest critical security patches applied. What percentage of the estate remains unpatched?

A) 8%
B) 11%
C) 12%
D) 89%

**Correct answer: B.**

**Explanation:** Unpatched servers: 4,800 − 4,272 = 528. As a percentage: 528 ÷ 4,800 = 0.11 = 11%. Option D (89%) is the patched proportion — the classic misread of which quantity was asked for. On dashboard questions, always confirm whether the question wants the compliant or non-compliant share before calculating.

**Question 2 (easy) — Budget share**

The annual cyber security programme budget is £3.6 million, split as: monitoring and response 35%, identity and access 25%, architecture and design 20%, training 10%, contingency 10%. How much is allocated to architecture and design?

A) £360,000
B) £600,000
C) £720,000
D) £900,000

**Correct answer: C.**

**Explanation:** 20% of £3.6 million = 0.20 × 3,600,000 = £720,000. A quick sanity check: 10% is £360,000, so 20% must be double that. Options A and D are the 10% and 25% shares — distractors built from adjacent rows of the same table, a standard trick in budget items. Extract the right row before touching the calculator.

**Question 3 (easy) — Ratio of findings**

A security architecture review across three major programmes yields 45 findings: 9 critical, 18 high and 18 medium. What is the ratio of critical to high to medium findings in its simplest form?

A) 9:18:18
B) 1:2:2
C) 1:3:3
D) 2:4:5

**Correct answer: B.**

**Explanation:** Divide each figure by the greatest common divisor, 9: 9 ÷ 9 = 1, 18 ÷ 9 = 2, 18 ÷ 9 = 2, giving 1:2:2. Option A is correct but not in simplest form — read the question's exact requirement. Ratio items are quick marks if you resist overthinking: find the common divisor and reduce.

**Question 4 (moderate) — Annualised loss expectancy**

You are comparing two controls for a payments service. Without controls, a data-breach event is estimated at £2.4 million per occurrence with an annual rate of occurrence of 0.25. Control A costs £180,000 per year and reduces the annual rate of occurrence to 0.05. What is the net annual benefit of Control A?

A) £120,000
B) £300,000
C) £420,000
D) £480,000

**Correct answer: B.**

**Explanation:** Annualised loss expectancy (ALE) before: £2,400,000 × 0.25 = £600,000. ALE after: £2,400,000 × 0.05 = £120,000. Risk reduction: £600,000 − £120,000 = £480,000. Net benefit after control cost: £480,000 − £180,000 = £300,000. Option D is the gross reduction (forgetting the control's cost); option A is the residual ALE. Loss-expectancy arithmetic is the quantitative backbone of enabling risk-based decisions — practise until the before/after/net sequence is automatic.

**Question 5 (moderate) — Comparing remediation velocity**

Two delivery groups report vulnerability remediation over a quarter. Group Alpha opened the quarter with 320 high-severity findings and closed 272. Group Beta opened with 190 and closed 152. Which group closed the greater proportion of its findings, and by how many percentage points?

A) Alpha, by 5 percentage points
B) Beta, by 5 percentage points
C) Alpha, by 8 percentage points
D) They closed equal proportions

**Correct answer: A.**

**Explanation:** Alpha: 272 ÷ 320 = 0.85 = 85%. Beta: 152 ÷ 190 = 0.80 = 80%. Alpha leads by 85 − 80 = 5 percentage points. Note the language: a difference between two percentages is expressed in percentage points, not per cent. Comparing rates rather than raw counts is exactly how you assess performance across several projects fairly — Beta closed fewer findings but also had fewer to close.

**Question 6 (moderate) — Logging storage capacity**

A new policy doubles authentication-log retention from 12 to 24 months. The flagship citizen service generates 45 GB of authentication logs per month, and log volume is expected to grow 20% year on year from month 13. Approximately how much storage is needed for the full 24-month retention window, assuming the first 12 months at the current rate and months 13–24 at the grown rate?

A) 540 GB
B) 1,080 GB
C) 1,188 GB
D) 1,296 GB

**Correct answer: C.**

**Explanation:** Months 1–12: 45 GB × 12 = 540 GB. Months 13–24 at 20% growth: 45 × 1.2 = 54 GB per month; 54 × 12 = 648 GB. Total: 540 + 648 = 1,188 GB. Option B ignores growth (45 × 24); option D wrongly applies growth to all 24 months. Capacity questions reward splitting the timeline at the point where the rate changes — the same discipline as costing a retention policy change before you recommend it.

**Question 7 (moderate) — Weighted risk score across an estate**

Your risk methodology weights services by criticality: gold services carry weight 3, silver weight 2, bronze weight 1. The estate has 5 gold services with an average risk score of 12, 10 silver services averaging 9, and 25 bronze services averaging 6. What is the criticality-weighted average risk score across the estate?

A) 7.5
B) 8.5
C) 9.0
D) 9.5

**Correct answer: B.**

**Explanation:** Each tier contributes (number of services × weight × average score) to the numerator and (number of services × weight) to the denominator. Numerator: (5 × 3 × 12) + (10 × 2 × 9) + (25 × 1 × 6) = 180 + 180 + 150 = 510. Denominator: (5 × 3) + (10 × 2) + (25 × 1) = 15 + 20 + 25 = 60. Weighted average: 510 ÷ 60 = 8.5. Option C is the trap of averaging the three tier averages ((12 + 9 + 6) ÷ 3 = 9.0), which ignores both service counts and weights. Option A is the simple per-service average with no criticality weighting ((60 + 90 + 150) ÷ 40 = 7.5). Weighted aggregation is how a single estate-level figure is honestly built for a senior risk owner — and knowing which wrong method produces which wrong number is how you challenge a misleading dashboard when you see one.

**Question 8 (moderate) — Percentage change in incidents**

Reportable security incidents fell from 84 in the previous financial year to 63 this year. Meanwhile the number of monitored services grew from 120 to 150. Which statement is numerically correct?

A) Incidents fell 25% while incidents per service fell 40%
B) Incidents fell 25% while incidents per service fell 25%
C) Incidents fell 21% while incidents per service fell 30%
D) Incidents fell 33% while incidents per service fell 44%

**Correct answer: A.**

**Explanation:** Incident change: (84 − 63) ÷ 84 = 21 ÷ 84 = 0.25 = 25% fall. Incidents per service: before, 84 ÷ 120 = 0.70; after, 63 ÷ 150 = 0.42. Change: (0.70 − 0.42) ÷ 0.70 = 0.28 ÷ 0.70 = 0.40 = 40% fall. Both parts of A hold. This two-layer structure — a raw change and a normalised change — is precisely the framing you would take to a board: the estate grew, so the per-service improvement is even stronger than the headline. Choosing the right denominator is a communication decision as much as a mathematical one.

**Question 9 (hard) — Cost-benefit across candidate technologies**

You are validating two candidate technologies for organisation-wide secrets management. Option X: licence £220,000 per year, implementation £150,000 one-off, and it is expected to remove £90,000 per year of manual key-rotation effort. Option Y: licence £140,000 per year, implementation £310,000 one-off, removing £70,000 per year of effort. Over a three-year appraisal period, which option costs less in net terms, and by how much?

A) Option X, by £30,000
B) Option Y, by £30,000
C) Option Y, by £20,000
D) They cost the same

**Correct answer: C.**

**Explanation:** Option X over three years: licences 3 × £220,000 = £660,000, plus £150,000 implementation = £810,000; minus savings 3 × £90,000 = £270,000; net £540,000. Option Y: licences 3 × £140,000 = £420,000, plus £310,000 implementation = £730,000; minus savings 3 × £70,000 = £210,000; net £520,000. Option Y is cheaper by £540,000 − £520,000 = £20,000. The structure to internalise is (recurring × years) + one-off − (savings × years), applied identically to both options before comparing. Common slips are omitting one option's implementation cost, or applying the savings to only one side. Also notice how sensitive the result is to the appraisal period: over five years, X's lower running cost pulls it back to £1,100,000 + £150,000 − £450,000 = £800,000 against Y's £700,000 + £310,000 − £350,000 = £660,000 — Y still wins, but you should always state the appraisal window when you present a technology recommendation, because the honest answer can flip with the horizon.

**Question 10 (hard) — Remediation trajectory against a deadline**

A compliance deadline in 6 months requires all 900 currently outstanding legacy findings to be closed. The programme closes findings at 120 per month, but new findings arise at 30 per month. At these rates, how many findings will remain at the deadline, and what monthly closure rate would have been needed to reach zero exactly?

A) 360 remaining; 180 per month needed
B) 180 remaining; 150 per month needed
C) 360 remaining; 150 per month needed
D) 540 remaining; 180 per month needed

**Correct answer: A.**

**Explanation:** Net closure per month: 120 − 30 = 90. Over 6 months: 90 × 6 = 540 closed, leaving 900 − 540 = 360. To clear 900 in 6 months requires a net rate of 900 ÷ 6 = 150 per month; with 30 new findings arriving monthly, gross closure must be 150 + 30 = 180 per month. Option C mixes the two figures — the commonest error is forgetting that the required rate is gross while the 150 is net. Trajectory arithmetic like this is how you tell a senior stakeholder, months in advance and with confidence, that a deadline will be missed without intervention — far more persuasive than an unquantified warning.

**Question 11 (hard) — Authentication service capacity**

An authentication service handles a peak of 3,200 requests per second (rps). A new national campaign is forecast to multiply peak load by 2.5. Each service node sustains 500 rps, and resilience policy requires the estate to tolerate the loss of 2 nodes while still serving peak load. How many nodes must be provisioned?

A) 16
B) 17
C) 18
D) 20

**Correct answer: C.**

**Explanation:** New peak: 3,200 × 2.5 = 8,000 rps. Nodes needed to serve it: 8,000 ÷ 500 = 16. The resilience policy requires peak service even with 2 nodes lost, so provision 16 + 2 = 18. Option A ignores resilience; option B adds only one spare; option D over-provisions beyond the stated policy. Note the reasoning order: size for load first, then apply the failure-tolerance rule. Capacity items reward translating a design principle ("N+2") into arithmetic exactly — the quantitative face of designing secure, resilient systems.

**Question 12 (hard) — Interpreting a phishing-simulation table**

A quarterly phishing simulation reports results by directorate:

| Directorate | Staff | Clicked link | Reported email |
|---|---|---|---|
| Operations | 1,200 | 180 | 420 |
| Policy | 800 | 96 | 360 |
| Digital | 600 | 48 | 330 |
| Finance | 400 | 72 | 100 |

Which directorate has the worst click rate, and what is it?

A) Operations, 15%
B) Finance, 18%
C) Operations, 18%
D) Finance, 15%

**Correct answer: B.**

**Explanation:** Click rates: Operations 180 ÷ 1,200 = 15%; Policy 96 ÷ 800 = 12%; Digital 48 ÷ 600 = 8%; Finance 72 ÷ 400 = 18%. Finance is worst at 18%. The raw-count trap is Operations, whose 180 clicks are the largest absolute number but sit on the largest denominator. As a follow-up insight you might also compute reporting rates (Digital leads at 55%) — the sort of second-order reading that turns a table into a targeted awareness strategy for the directorates that need it.

**Question 13 (hard) — Blended day-rate for a strategy team**

To define the organisation's security architecture strategy you assemble a team: 1 principal architect at £950 per day for 40 days, 2 senior architects at £750 per day for 60 days each, and 1 analyst at £450 per day for 30 days. What is the total cost, and what is the blended average day-rate across all person-days worked, to the nearest pound?

A) £141,500 total; £745 blended rate
B) £141,500 total; £725 blended rate
C) £128,000 total; £745 blended rate
D) £151,500 total; £797 blended rate

**Correct answer: A.**

**Explanation:** Costs: principal 950 × 40 = £38,000; seniors 750 × 60 × 2 = £90,000; analyst 450 × 30 = £13,500. Total: 38,000 + 90,000 + 13,500 = £141,500. Person-days: 40 + 120 + 30 = 190. Blended rate: 141,500 ÷ 190 = £744.7, rounding to £745. The frequent slip is forgetting to double the senior architects' days (option C) or averaging the three day-rates without weighting (950 + 750 + 450) ÷ 3 = £717 — close to option B's distractor. Resourcing arithmetic supports the leadership dimension of your role: strategies are staffed, and staffing is costed.

**Question 14 (hard) — Risk appetite threshold**

The organisation's risk appetite statement caps aggregate residual risk for the citizen-facing portfolio at 220 points. Current portfolio: Service A 68 points, Service B 54, Service C 47, Service D 39. A proposed new service E would enter at 34 points; simultaneously, a planned control uplift will cut Service A's score by 25%. If both changes proceed, does the portfolio stay within appetite, and with what headroom or excess?

A) Within appetite, 5 points of headroom
B) Within appetite, 15 points of headroom
C) Exceeds appetite by 5 points
D) Exceeds appetite by 17 points

**Correct answer: C.**

**Explanation:** First apply the uplift: 25% of 68 is 17, so Service A falls to 68 − 17 = 51. Then aggregate all five services: 51 + 54 + 47 + 39 + 34. Sum stepwise: 51 + 54 = 105; 105 + 47 = 152; 152 + 39 = 191; 191 + 34 = 225. Against a cap of 220, the portfolio exceeds appetite by 225 − 220 = 5 points. Option D is the result of forgetting the control uplift entirely (68 keeps its full value: 242 − 220 = 22, close to but not exactly 17 — the distractor also assumes a partial misread). Option A is the mirror-image error of subtracting the excess from the wrong side and calling it headroom. The professional consequence matters as much as the arithmetic: a proposal can be individually sensible and still breach aggregate appetite, so the correct architectural advice is not "reject service E" but "sequence the changes" — deliver the uplift first, or find 5 further points of reduction elsewhere. Quantified aggregate positions are exactly what makes you trusted by senior risk owners as an expert: you can show not just that the portfolio breaches appetite, but by how much and which lever closes the gap.

**Question 15 (moderate) — Encryption migration progress**

A cross-government programme requires all 250 legacy interfaces to move to current TLS standards. At the last checkpoint, 40% were fully migrated, 30% were in testing, and the rest had not started. Of those in testing, one third are expected to fail and need rework averaging 10 additional days each. How many interfaces have not started, and how many total rework days are expected from the testing group?

A) 75 not started; 250 rework days
B) 75 not started; 750 rework days
C) 100 not started; 250 rework days
D) 100 not started; 750 rework days

**Correct answer: A.**

**Explanation:** Migrated: 40% of 250 = 100. In testing: 30% of 250 = 75. Not started: 250 − 100 − 75 = 75 (or 30% of 250, since 100% − 40% − 30% = 30%). Rework: one third of the 75 in testing is 25 interfaces; 25 × 10 days = 250 rework days. Option D compounds two errors — subtracting only the migrated interfaces (giving 150, then misreading) and multiplying the whole testing group by 10 days. Multi-stage percentage items reward computing each population explicitly before applying the per-unit figure; a one-line running total in your notes prevents the fractions drifting. This is the arithmetic of programme oversight: the same three numbers — done, in flight, not started — anchor every honest status report you give a senior stakeholder.

**Question 16 (hard) — Vulnerability scanning coverage and false positives**

Your scanning platform covers 5,400 of the organisation's 6,000 assets. Across covered assets it raises 1,800 findings, of which 15% are historically false positives. The security team can validate 60 findings per week. Approximately how many weeks of validation work does the true-positive backlog represent, and what percentage of the total asset estate is unscanned?

A) 25.5 weeks; 10% unscanned
B) 30 weeks; 10% unscanned
C) 25.5 weeks; 11% unscanned
D) 30 weeks; 6% unscanned

**Correct answer: A.**

**Explanation:** True positives: 1,800 × (1 − 0.15) = 1,800 × 0.85 = 1,530. Validation time: 1,530 ÷ 60 = 25.5 weeks. Unscanned assets: 6,000 − 5,400 = 600; as a percentage of the estate, 600 ÷ 6,000 = 10%. Option B forgets to remove false positives (1,800 ÷ 60 = 30); option C divides the unscanned count by the covered population (600 ÷ 5,400 ≈ 11%) rather than the whole estate — a denominator error worth studying, because both figures are defensible in different sentences and only the question's wording ("of the total asset estate") settles which is wanted. Strategically, the two answers belong together in the same board message: a six-month validation backlog and a tenth of the estate invisible to scanning are jointly a capacity argument, and quantifying them is what turns "we need more resource" into a decision-ready case.

**Question 17 (moderate) — Percentage points versus per cent**

The proportion of new services adopting the approved security patterns rose from 60% last year to 75% this year. Which pair of statements correctly describes the change?

A) A rise of 15 percentage points, which is a 25% relative increase
B) A rise of 15%, which is 15 percentage points
C) A rise of 25 percentage points, which is a 15% relative increase
D) A rise of 15 percentage points, which is a 15% relative increase

**Correct answer: A.**

**Explanation:** The absolute change is 75 − 60 = 15 percentage points. The relative change is 15 ÷ 60 = 0.25 = 25%. Options B and D blur the two measures — the most common numerical-communication error in management reporting. As the person who presents adoption metrics for the patterns you set, being crisp about this distinction protects your credibility: "up 25%" and "up 15 percentage points" describe the same improvement, and a careless mixture of the two invites challenge in exactly the forums where you can least afford it.

### Preparation tips

- **Drill the core operations.** Percentages, percentage change, ratios, weighted averages and rate × time problems cover the vast majority of items. Ten minutes of daily drill restores speed quickly, even for experienced professionals.
- **Rebuild your own dashboards by hand.** Take a real (suitably anonymised) vulnerability or budget report and recompute its headline figures. You will internalise the before/after/net pattern that loss-expectancy and cost-benefit items rely on.
- **Write the extraction step down.** Most errors happen while lifting numbers from the table, not during calculation. Note the figures you extract, with units, then compute.
- **Watch units and scale qualifiers.** "In thousands", "per month" versus "per year", GB versus TB, per cent versus percentage points: one missed qualifier invalidates perfect arithmetic.
- **Estimate before you calculate.** A rough order-of-magnitude guess catches decimal slips instantly, and at your level estimation is also a professional credibility skill in live meetings.
- **Use the on-screen calculator efficiently.** Practise with the same style of calculator the platform provides; fumbling the interface costs more time than the mathematics.

### Common pitfalls

- **Misreading chart and table labels.** Confusing monthly with annual data, or missing scale qualifiers, is the most common failure mode in numerical tests — and the distractors are usually built from exactly those misreads.
- **Answering the complement.** Computing the patched share when the question asked for the unpatched share (Question 1). Re-read the final sentence of the stem before answering.
- **Forgetting a cost or a count.** Net-benefit items expect control costs subtracted (Question 4); team-cost items expect every team member counted (Question 13).
- **Confusing net and gross rates.** When new findings arrive while old ones close, the required closure rate is gross, not net (Question 10).
- **Over-calculating.** If options are far apart, estimation and rounding reach the answer faster than exact long division. Precision is for close options only.
- **Time-sink questions.** A single multi-stage item is never worth three unanswered easy ones. Flag it, move on, return if time allows.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment evaluates how well you understand, analyse and draw correct conclusions from written business information, mirroring the exact reading demands of the role. Passages use the industry's real terminology — for a Principal Security Architect, that means security policies, national guidance, assurance and audit reports, supplier correspondence and board papers. The defining discipline is fact-based logic: you must answer strictly from the text provided, ignoring outside knowledge, however expert. Most items require a verdict of True (the passage supports the statement), False (the passage contradicts it) or Cannot Say (the passage provides insufficient information), supplemented by multiple-choice comprehension. Timing is tight — typically under a minute per question — to simulate workplace deadlines.

For your role, this assessment matters because language is your primary instrument of influence. You effectively translate and accurately communicate security and risk implications at the most senior levels, across technical and non-technical stakeholders; you challenge and lead changes to policy, which means reading policy with forensic precision; you respond to challenges, which requires knowing exactly what a document does and does not claim. A principal architect who conflates "should" with "must", or a stated intention with a delivered fact, will misadvise a senior risk owner sooner or later. The Cannot Say category deserves special respect: it rewards the professional humility of recognising when a text underdetermines a conclusion — the same judgement you exercise when an assurance report is silent on the one point that matters.

In format terms, expect a series of short passages, each followed by two to five statements or questions, delivered online with a countdown timer. Scores are typically normed against a professional comparison group, and many platforms report accuracy and speed separately. The practice set below follows that structure: six passages spanning the document types your role reads weekly, with difficulty labels so you can calibrate where your time goes.

### What it measures for your role

- **Communication (security architect).** Every item tests precise reading of the kind of material you translate for senior stakeholders; several passages are written at board-paper register, and the questions probe whether nuance survives your reading.
- **Understanding security implications of transformation.** Policy and legal-guidance passages test extraction of obligations, permissions and exceptions — the raw material of challenging and leading changes to policy and processes.
- **Enabling and informing risk-based decisions.** Assurance-report passages test whether you can state exactly what evidence establishes, a precondition for being trusted by senior risk owners as an expert.
- **Analysis.** Contrast-and-compare items across passages test monitoring changes in the written environment: what changed between the old standard and the new, and what follows.
- **Research and innovation.** One passage style summarises an emerging technology's security properties, testing careful reading of claims versus demonstrated results — the core of validating new technologies responsibly.

### Practice questions

**Passage 1 — Extract from an organisational security standard**

"All new digital services must complete a security architecture review before public beta. Services handling special category data must additionally obtain senior risk owner sign-off before private beta. Where a service reuses an approved architectural pattern without modification, the review may be conducted as a desk-based assessment. Reviews conducted more than twelve months before public beta must be refreshed. This standard does not apply to services procured as commodity software-as-a-service, which follow the third-party assurance process."

**Question 1 (easy).** True, False or Cannot Say: "A new digital service that reuses an approved pattern without modification is exempt from security architecture review."

**Correct answer: False.**

**Explanation:** The passage says such a service's review "may be conducted as a desk-based assessment" — a lighter form of review, not an exemption. The review obligation stands; only its format changes. Watch for statements that upgrade a concession into an exemption: the difference between "lighter-touch" and "not required" is precisely the kind of distinction you police in real standards.

**Question 2 (easy).** True, False or Cannot Say: "Commodity software-as-a-service products receive no security scrutiny."

**Correct answer: False.**

**Explanation:** The passage states such services "follow the third-party assurance process". Being out of scope of this standard is not the same as receiving no scrutiny; the text names the alternative route explicitly. The statement contradicts the passage, so the answer is False rather than Cannot Say.

**Question 3 (moderate).** True, False or Cannot Say: "A service handling special category data needs senior risk owner sign-off before public beta."

**Correct answer: True.**

**Explanation:** The passage requires sign-off before private beta, and private beta precedes public beta in the standard service lifecycle the passage assumes (review "before public beta", sign-off "before private beta" as an additional, earlier gate). If sign-off must exist before private beta, it necessarily exists before public beta. This item rewards careful sequencing of the stated gates. Note the strict-reading caution: the conclusion follows from the passage's own ordering of the two beta phases, not from outside knowledge.

**Question 4 (moderate).** True, False or Cannot Say: "Desk-based assessments are less rigorous than full security architecture reviews."

**Correct answer: Cannot Say.**

**Explanation:** The passage permits a desk-based format in defined circumstances but says nothing about relative rigour. Your professional experience may insist desk-based reviews are lighter — and that instinct is exactly what this item is designed to catch. The text neither supports nor contradicts the claim, so Cannot Say is the only defensible verdict. Answering from expertise rather than from the passage is the single most common failure mode for senior specialists in verbal reasoning tests.

**Passage 2 — Board paper on cyber risk**

"The department's residual cyber risk remains within appetite this quarter, although the margin has narrowed for the third consecutive quarter. The principal driver is the delayed decommissioning of the legacy case-management estate, now forecast to complete in Q4 rather than Q2. The security architecture team has compensated with additional network segmentation, which the chief information security officer considers proportionate on an interim basis. Should decommissioning slip beyond Q4, the accounting officer will be asked to formally accept the elevated risk or fund accelerated migration. No exploitation of the legacy estate has been detected to date."

**Question 5 (moderate).** True, False or Cannot Say: "The department's cyber risk is currently outside appetite."

**Correct answer: False.**

**Explanation:** The opening sentence states residual risk "remains within appetite this quarter". The narrowing margin signals a trend, not a breach. Distinguishing a deteriorating trajectory from a crossed threshold is a distinction you make constantly when communicating risk at senior levels — and the passage's own words settle it here.

**Question 6 (moderate).** True, False or Cannot Say: "The legacy estate has not been compromised."

**Correct answer: Cannot Say.**

**Explanation:** The passage says "no exploitation of the legacy estate has been detected to date". Absence of detection is not absence of compromise: an undetected intrusion is entirely consistent with the text. The statement makes a stronger claim than the passage supports, so the verdict is Cannot Say. This is the verbal-reasoning twin of the assurance-logic trap in the cognitive section — and a distinction you would insist on in any assurance report you countersign.

**Question 7 (moderate).** Multiple choice: According to the passage, what happens if decommissioning slips beyond Q4?

A) The accounting officer must fund accelerated migration.
B) The accounting officer will be asked either to formally accept the elevated risk or to fund accelerated migration.
C) The chief information security officer will withdraw support for the interim controls.
D) The department will breach its risk appetite.

**Correct answer: B.**

**Explanation:** The passage presents a disjunction: formal acceptance or funding acceleration. Option A collapses the disjunction into one branch; C invents a consequence the text nowhere states (the CISO's view is described as "proportionate on an interim basis", with no withdrawal threatened); D predicts a breach the passage does not assert — it describes a decision point, not an outcome. Preserving disjunctions faithfully is essential in escalation papers: the moment "accept or fund" becomes "must fund", you have misbriefed your accounting officer.

**Question 8 (hard).** True, False or Cannot Say: "The additional network segmentation was implemented because decommissioning was delayed."

**Correct answer: True.**

**Explanation:** The passage identifies the delayed decommissioning as "the principal driver" of the narrowed margin and states the team "has compensated with additional network segmentation". The word "compensated" ties the segmentation to the delay as its cause. This item rewards tracking causal language — driver, compensated, interim — across sentences. If the passage had merely listed both facts without the causal verb, Cannot Say would have been correct; the presence of "compensated" is what licenses True.

**Passage 3 — Supplier assurance report extract**

"The supplier's platform encrypts customer data at rest using keys managed in a certified hardware security module. Encryption in transit is enforced for all external interfaces; internal service-to-service traffic is encrypted where the deployment architecture supports it. The supplier commits to notifying customers of any personal data breach within 48 hours of becoming aware. Penetration testing is conducted annually by an independent firm; the most recent test identified two medium-severity findings, both of which the supplier states have been remediated. Remediation evidence was not reviewed as part of this assessment."

**Question 9 (moderate).** True, False or Cannot Say: "All traffic within the supplier's platform is encrypted."

**Correct answer: False.**

**Explanation:** The passage carves out internal traffic: it is encrypted "where the deployment architecture supports it", which entails there are architectures where it is not. "All external interfaces" plus a conditional internal statement cannot support "all traffic". Qualifier-spotting — where, unless, to the extent that — is the heart of reading supplier assurances, because those qualifiers are exactly where the residual risk lives.

**Question 10 (hard).** True, False or Cannot Say: "The two medium-severity findings from the most recent penetration test have been fixed."

**Correct answer: Cannot Say.**

**Explanation:** The passage reports that "the supplier states" the findings have been remediated, and immediately adds that remediation evidence "was not reviewed as part of this assessment". A claim attributed to an interested party, explicitly unverified, cannot ground True; nothing contradicts it either, so it is not False. Cannot Say precisely captures the evidential position — and noticing attribution ("the supplier states") is a professional reflex this item deliberately tests. In your real reviews, this is the sentence you would flag for evidence before relying on it.

**Question 11 (hard).** True, False or Cannot Say: "The supplier will notify customers within 48 hours of a personal data breach occurring."

**Correct answer: False.**

**Explanation:** The commitment runs from the supplier "becoming aware" of a breach, not from the breach occurring. A breach could occur weeks before detection, making the statement's timeline materially different from the passage's. This is a distinction with heavy legal and contractual weight — awareness-based clocks versus occurrence-based clocks — and the passage's wording contradicts the statement's version, so the answer is False rather than Cannot Say.

**Passage 4 — Emerging technology briefing**

"Confidential computing enclaves protect data in use by isolating computation within hardware-attested environments. Early adopters in the financial sector report that enclave attestation adds measurable latency, although published benchmarks vary widely by workload. Proponents argue the technology could eventually remove the need to trust cloud infrastructure administrators. Current implementations, however, depend on the correctness of the processor vendor's firmware, and several attestation bypass vulnerabilities have been disclosed and patched in the last three years. Government pilots have so far been limited to non-production analytics workloads."

**Question 12 (moderate).** True, False or Cannot Say: "Confidential computing removes the need to trust cloud infrastructure administrators."

**Correct answer: False.**

**Explanation:** The passage attributes this as a future possibility argued by proponents ("could eventually remove"), and immediately undercuts it for current implementations, which "depend on the correctness of the processor vendor's firmware". The statement asserts as accomplished fact what the passage frames as advocacy about the future; the passage's present-tense caveats contradict it. Distinguishing a proponent's claim from an established property is the exact skill you use when validating new technologies for adoption across the organisation.

**Question 13 (moderate).** True, False or Cannot Say: "Government organisations have used confidential computing in production services."

**Correct answer: False.**

**Explanation:** The passage states government pilots "have so far been limited to non-production analytics workloads". Production use by government is thereby contradicted, not merely unaddressed — so False, not Cannot Say. Read scope-limiting phrases ("so far", "limited to") carefully: they are doing precise work, and the verdict turns on them.

**Question 14 (hard).** Multiple choice: Which statement best summarises the passage's overall position on confidential computing?

A) A mature technology ready for sensitive government workloads.
B) A promising technology whose current trust and performance caveats warrant measured adoption.
C) A flawed technology that has repeatedly failed in practice.
D) A technology whose only obstacle is latency.

**Correct answer: B.**

**Explanation:** The passage balances promise (protection of data in use, proponents' trust argument) against caveats (latency, firmware dependence, disclosed-and-patched bypasses, non-production pilots only). Option A overstates maturity against the explicit non-production limitation; C overstates failure — vulnerabilities were "disclosed and patched", and nothing "failed in practice"; D reduces multiple caveats to one. Summary items reward weighing every clause, exactly as you would when contributing to developments on security properties in technology and briefing others on whether to adopt.

**Question 15 (hard).** True, False or Cannot Say: "Enclave attestation latency makes confidential computing unsuitable for citizen-facing transactional services."

**Correct answer: Cannot Say.**

**Explanation:** The passage reports measurable latency with benchmarks that "vary widely by workload" — it never evaluates suitability for any service class, let alone citizen-facing transactional ones. The statement may align with your engineering instinct, but the text underdetermines it entirely. Senior specialists lose most verbal-reasoning marks on exactly this pattern: a plausible professional inference dressed as a textual conclusion. The passage's silence is the answer.

**Passage 5 — Email from a programme director**

"Thank you for your review of the identity platform design. I accept the recommendation to defer the biometric enrolment feature until the privacy assessment concludes, though I remain concerned about the impact on our published roadmap. On the federation question, my technical lead disagrees with your assessment that the proposed token lifetime creates undue risk; she believes the compensating monitoring controls are sufficient. I would like your team and hers to reach a joint position before the design authority meets on the 14th. Separately, the Cabinet Office has asked whether our pattern could be reused by two other departments; I have said we are open to this in principle, subject to your view on the security implications of multi-tenancy. Funding for phase two is not yet confirmed."

**Question 16 (easy).** True, False or Cannot Say: "The programme director has rejected the recommendation to defer biometric enrolment."

**Correct answer: False.**

**Explanation:** The email says "I accept the recommendation to defer" — an explicit acceptance, with a concern noted alongside it. Accepting-with-reservations is still accepting; the statement contradicts the text directly. Under time pressure, candidates sometimes let the word "concerned" colour the whole sentence, but the verdict rests on the operative verb.

**Question 17 (moderate).** True, False or Cannot Say: "The technical lead believes the token lifetime creates undue risk."

**Correct answer: False.**

**Explanation:** The passage says the technical lead "disagrees with your assessment that the proposed token lifetime creates undue risk" and considers the compensating controls sufficient. Her stated position is the opposite of the statement. This item rewards careful tracking of who holds which view in multi-party correspondence — the everyday texture of managing stakeholder expectations across high-risk work, where misattributing a position can derail a design authority meeting.

**Question 18 (moderate).** True, False or Cannot Say: "The pattern will be reused by two other departments."

**Correct answer: Cannot Say.**

**Explanation:** The Cabinet Office has "asked whether" the pattern could be reused; the director is open "in principle, subject to your view on the security implications of multi-tenancy". Everything is conditional and prospective: an enquiry, an in-principle openness, an unresolved security question. Nothing asserts the reuse will happen, and nothing rules it out. Cannot Say captures the position exactly — and spotting how many contingencies stand between an enquiry and an outcome is a reading skill you use every time cross-government reuse is floated.

**Question 19 (hard).** Multiple choice: What has the programme director actually asked the recipient to do before the 14th?

A) Accept the technical lead's position on token lifetime.
B) Work with the technical lead's team to reach a joint position on the federation question.
C) Complete the privacy assessment for biometric enrolment.
D) Confirm the security implications of multi-tenancy for the Cabinet Office.

**Correct answer: B.**

**Explanation:** The only request with the 14th as its deadline is "I would like your team and hers to reach a joint position before the design authority meets on the 14th", concerning the federation disagreement. Option A prejudges the outcome of that joint work; C attaches the recipient to an assessment the email treats as an external dependency; D is a request in substance ("subject to your view") but carries no date and is framed as "separately". Extracting the precise ask, owner and deadline from senior correspondence is a core communication discipline — the difference between responding to what was written and what was skimmed.

**Question 20 (hard).** True, False or Cannot Say: "Phase two of the programme will be cancelled if funding is not confirmed."

**Correct answer: Cannot Say.**

**Explanation:** The email states only that "funding for phase two is not yet confirmed". It draws no consequence — no cancellation, no delay, no contingency plan. Any inference about what unconfirmed funding leads to comes from your experience of programmes, not from this text. The passage is silent, so Cannot Say. Notice how the final sentences of correspondence often carry these unadorned facts; the test — and good stakeholder management — is resisting the urge to complete the story on the author's behalf.

**Passage 6 — Internal audit finding and management response**

"Finding 7 (medium): The organisation's security architecture principles have not been formally reviewed since publication three years ago, although individual patterns have been updated on an ad hoc basis. Audit testing of ten recent solution designs found that eight referenced the principles; of these, six evidenced full alignment and two documented approved exceptions. The remaining two designs made no reference to the principles. Management response: accepted. The principal security architect will establish an annual review cycle for the principles, with the first review completing within six months. The two non-referencing designs pre-date the current governance process and will be assessed retrospectively only if they are materially changed."

**Question 21 (moderate).** True, False or Cannot Say: "The audit found that two solution designs breached the security architecture principles."

**Correct answer: False.**

**Explanation:** Careful separation of categories is everything here. Of the ten designs, eight referenced the principles: six fully aligned and two with documented approved exceptions — an approved exception is compliance with the governance process, not a breach. The remaining two made no reference to the principles, which is a documentation and governance gap; the audit text does not say those designs breached the principles' content, and indeed it says nothing about their substantive alignment at all. The statement asserts a breach the passage never records, and misreads "approved exceptions" or "no reference" as violations. In audit language, these distinctions carry real consequences — a "breach" finding would demand a different management response entirely.

**Question 22 (moderate).** True, False or Cannot Say: "The principles will be reviewed every year from now on."

**Correct answer: Cannot Say.**

**Explanation:** The management response commits the principal security architect to establish an annual review cycle, with the first review inside six months. A commitment to establish a cycle is a statement of intention, not a report of an operating fact — management responses are promises, and audit follow-up exists precisely because promises are not always kept. The passage neither confirms the cycle will actually run every year nor contradicts it. Candidates who answer True are converting a planned control into an operating one — exactly the error your own assurance reviews are designed to catch.

**Question 23 (hard).** True, False or Cannot Say: "The two designs that did not reference the principles will never be assessed against them."

**Correct answer: False.**

**Explanation:** The response states they "will be assessed retrospectively only if they are materially changed". That establishes a condition under which they will be assessed — so "never" is contradicted by the passage's own terms. The subtlety is the direction of the conditional: "only if materially changed" means no assessment without material change, but it explicitly provides a route to assessment. A statement of "never" requires the passage to close every route, and it does not. Compare Question 22: there, the future was left genuinely open (Cannot Say); here, the statement makes an absolute claim the text's conditional directly refutes (False). Discriminating between the two is the highest-value skill in this question format.

### Preparation tips

- **Read the statement first, then hunt the passage.** With under a minute per item, scanning for the statement's key terms beats reading every passage exhaustively before seeing the question.
- **Rank the verdict by evidence, not plausibility.** Ask in order: does the text assert this (True)? Does the text contradict it (False)? Otherwise Cannot Say — no matter how professionally confident you feel.
- **Highlight qualifiers and attributions.** Words like may, must, where, so far, states, considers, could eventually decide most items. Train yourself to underline them on the first pass; every one of the hard items above turned on such a word.
- **Practise on your own document diet.** Take a paragraph from a policy, an assurance report or NCSC-style guidance and write three statements about it — one True, one False, one Cannot Say. Composing items is the fastest way to internalise how they are built.
- **Respect the clock.** Verbal items are deliberately dense; if a verdict is not emerging within your time budget, choose your best-supported option, flag it, and move on.

### Common pitfalls

- **Importing expert knowledge.** The most dangerous pitfall for a principal architect: you know how desk-based reviews, breach clocks and enclaves really work, and the test scores only what the passage says (Questions 4, 10, 15).
- **Confusing "not detected" with "did not happen".** Detection language, awareness clocks and unverified claims each create a gap between the text and the world; the test lives in that gap (Questions 6, 10, 11).
- **Upgrading likelihoods and proposals into facts.** "Could eventually", "forecast to", "proponents argue" are not accomplished outcomes (Question 12).
- **Collapsing disjunctions and exceptions.** "Accept or fund" is not "must fund"; "may be desk-based" is not "exempt" (Questions 1, 7).
- **Overusing Cannot Say as a refuge.** When the passage's own wording contradicts a statement — even subtly, as with the breach-notification clock — the answer is False. Cannot Say is for genuine silence, not for discomfort.

## Workplace job-specific situational judgement assessment

### About this assessment

A workplace job-specific situational judgement assessment evaluates decision-making, interpersonal skill and professional conduct through realistic workplace dilemmas. Unlike logic or numeric tests, there is rarely a single objectively right answer: several responses may seem reasonable, and the scoring reflects which behaviours best fit the organisation's values and the demands of the role. Response formats typically ask you to select the most effective and least effective actions from a set, or to rank or rate every option. Timing is usually generous or absent, because the assessment targets your natural judgement rather than your speed.

For a Principal Security Architect, the situational judgement assessment is arguably the most role-authentic of the four. Your effectiveness at this level depends less on producing artefacts yourself and more on how you act as a point of escalation, manage senior stakeholder expectations under constrained timescales, respond to challenge, influence important business and architectural decisions, and further the profession by setting an example. The dilemmas below are calibrated to UK public sector values — user needs, transparency, collaboration, accessibility and inclusion — alongside the specific trust relationship you hold with senior risk owners. When judging options, favour actions that address the root issue, keep risk owners genuinely informed, preserve relationships while telling the truth, and strengthen the organisation's capability rather than just resolving today's incident. Be wary of options that are passive, that pass a problem elsewhere without ownership, or that are idealistic in a way that would not survive contact with a real programme.

### What it measures for your role

- **Communication (security architect).** Scenarios test translating security implications for the most senior audiences, responding to challenge without defensiveness, and managing expectations across high-risk work under constrained timescales.
- **Enabling and informing risk-based decisions.** Several dilemmas turn on the boundary between your advisory role and the risk owner's decision rights — the trust that makes you the recognised escalation point.
- **Designing secure systems and Security technology.** Scenarios about patterns, review findings and exploitability judgements test how you set direction and create precedents while keeping delivery moving.
- **Research and innovation.** Dilemmas about new technologies and engagement with the broader security community test measured advocacy versus enthusiasm, and generosity with expertise.
- **Analysis and Understanding security implications of transformation.** Scenarios involving changing environments and policy collisions test when to revisit previous decisions and how to challenge policy constructively.

### Practice questions

**Question 1 (moderate) — The risk owner who wants a shortcut**

A director (the senior risk owner) tells you privately that a ministerial commitment requires a citizen-facing service to launch in three weeks. Your architecture review found that the service's fraud-detection controls are incomplete, and you judge the residual risk to be well above the organisation's stated appetite. The director asks you to "soften the language" in your review so the launch decision is easier to defend.

A) Refuse and immediately email the accounting officer describing the director's request.
B) Decline to change your professional assessment, explain that accurate wording protects the director as decision-maker, and offer to add a clear statement of options — launch with specified interim controls and a dated remediation plan, or delay — so the risk decision is explicit and well-supported.
C) Soften the language as asked, since the director owns the risk and the decision is theirs.
D) Keep the wording but quietly delay issuing the report until after the launch decision has been made.

**Most effective: B. Least effective: D.**

**Explanation:** Option B holds the professional line — your assessment is your assessment — while doing the constructive work of a trusted adviser: reframing the situation so the risk owner can make a lawful, explicit, defensible decision, potentially including a risk-accepted launch with interim controls. It respects the decision rights of the risk owner without corrupting the evidence base, which is the heart of enabling risk-based decisions and of being trusted by senior risk owners. Option A escalates before attempting resolution, damaging the relationship and skipping the director's opportunity to step back; escalation is a tool you hold, not your first move. Option C corrupts the record and would erode the very trust that makes your role work. Option D is the least effective: it is passive, deceptive in effect, leaves the decision uninformed, and abandons both the service's users and the director. Transparency delayed past the decision point is transparency denied.

**Question 2 (moderate) — Challenged in front of the board**

At an architecture and investment board, a well-regarded chief technology officer from another directorate publicly challenges your recommended security pattern for inter-departmental data exchange, calling it "gold-plating that will delay every programme in the portfolio". Several board members visibly agree. You are confident in the pattern, which reflects lessons from a serious incident elsewhere in government.

A) Restate the pattern's requirements more firmly and remind the board of your authority over security architecture.
B) Acknowledge the delivery concern as legitimate, briefly explain the specific threat and incident evidence behind the pattern, and propose taking an action to work with the CTO's team on a delivery-friendly implementation profile, reporting back to the board.
C) Withdraw the pattern for further consultation to avoid conflict at the board.
D) Say nothing substantive at the board and lobby individual members afterwards to overrule the CTO.

**Most effective: B. Least effective: D.**

**Explanation:** Option B models exactly what "successfully respond to challenges" means at principal level: it treats challenge as information, not attack; it grounds the pattern in threat and evidence rather than authority; and it converts a public standoff into a collaborative piece of work with a report-back, preserving both the pattern's integrity and the relationship. Option A leans on positional authority — the weakest form of influence and one that invites quiet non-compliance across the portfolio. Option C rewards volume over evidence: withdrawing a well-founded pattern because the room frowned teaches the organisation that security requirements are negotiable by mood. Option D is least effective because it combines silence at the accountable forum with behind-the-scenes manoeuvring — the opposite of transparency, and corrosive to board governance. Influence at your level is built on evidence offered openly and follow-through delivered visibly.

**Question 3 (moderate) — The unprecedented vulnerability**

A researcher responsibly discloses a novel vulnerability class affecting an authentication component used by your organisation and, you suspect, by several other departments. No public exploit exists yet. Your team can design a mitigation within days, but confirming the full cross-government exposure would take longer. The researcher plans to publish in 30 days.

A) Design and deploy your organisation's mitigation, and keep the details internal until the researcher publishes.
B) Ask the researcher to delay publication indefinitely while a full cross-government assessment is completed.
C) Deploy your mitigation, share the vulnerability details and your mitigation design through the appropriate national and cross-government security channels, and coordinate timelines so other departments can act before publication.
D) Escalate to your director and await instructions before taking any technical action.

**Most effective: C. Least effective: A.**

**Explanation:** Option C does everything the role demands: it protects your own organisation promptly, treats the 30-day window as a coordination clock, and uses recognised channels so other departments benefit from your team's mitigation design — furthering the profession and demonstrating best practice beyond your organisation, exactly as your role profile describes. Option B is unrealistic and unfair to a researcher already acting responsibly; indefinite delay requests damage the cooperative disclosure ecosystem government relies on. Option D confuses escalation with abdication: you inform leadership, certainly, but a principal architect is the expert whose recommendation leadership needs, and technical mitigation should not idle in a queue. Option A is least effective despite containing real action, because it knowingly leaves peer departments exposed to a vulnerability you could help them fix — a failure of the collaboration and transparency values that cross-government security depends on, and a decision you would struggle to defend after publication day.

**Question 4 (hard) — The strategy nobody asked for**

You joined six months ago as the organisation's first principal security architect. Security decisions are made programme-by-programme; there is no organisation-wide security architecture strategy, and each programme's architects defend their local choices. Your remit letter mentions "setting direction", but no one has asked you for a strategy, and programme directors are focused on delivery dates.

A) Write a comprehensive strategy yourself and issue it through the design authority as mandatory.
B) Spend time with each programme's architects and directors to map current decisions, pain points and duplicated effort; draft strategic principles that demonstrably solve problems they recognise; then take the draft through open consultation to the design authority for endorsement.
C) Wait until a security incident or audit finding creates demand for a strategy.
D) Ask your director to instruct programme directors to comply with a strategy you will write.

**Most effective: B. Least effective: C.**

**Explanation:** Setting "a strategy that can be used in the long term and across the breadth of the organisation" — your role's own words — requires legitimacy as much as content. Option B builds the strategy out of the organisation's real problems, gives every future adopter a stake in it, and uses the design authority for endorsement rather than imposition; strategies adopted this way outlive their authors. Option A produces a document with your name on it and little else: mandates without engagement generate exemption requests, not alignment. Option D borrows hierarchical force instead of building influence, and positions the strategy as your director's instruction rather than the profession's direction — brittle the moment attention moves elsewhere. Option C is least effective: waiting for an incident to create your mandate is passive, gambles users' data on organisational learning-by-failure, and abdicates precisely the leadership the role was created to provide.

**Question 5 (hard) — The legacy decision that no longer holds**

Two years ago, before your tenure, the organisation accepted the risk of running a legacy payments component without modern authentication, based on an assessment that exploitation required physical network access. You learn that a planned office relocation will move that network segment onto shared building infrastructure, and separately that exploit tooling for this component's weakness is now freely available. The original risk acceptance has 18 months left before its scheduled review.

A) Respect the existing risk acceptance until its scheduled review date, as reopening it early would undermine the risk-management process.
B) Quietly instruct the relocation programme to exclude that network segment, avoiding the need to reopen the risk decision.
C) Document how the two environmental changes invalidate the original assessment's assumptions, brief the current risk owner promptly with updated exploitability analysis and options, and trigger an early review of the acceptance.
D) Post the issue to the architecture review board's backlog for consideration in its normal cycle.

**Most effective: C. Least effective: A.**

**Explanation:** This scenario is your Analysis skill in dilemma form: "monitor changes in the technical environment and assess whether risks are still at acceptable levels or whether previous decisions need to be revisited." Option C does exactly that — it identifies that both load-bearing assumptions (physical access requirement, absence of tooling) have failed, quantifies the new exploitability, and returns the decision to the accountable owner without delay. Option B contains a genuinely useful mitigation idea, but executed "quietly" it hides a material risk change from its owner and leaves the invalid acceptance on the books; the mitigation belongs inside option C's briefing as one of the options. Option D treats an invalidated risk acceptance as routine backlog — a pace mismatch with freely available exploit tooling. Option A is least effective because it mistakes process formalism for risk management: a scheduled review date is an administrative convenience, not a reason to leave a decision standing after its factual basis has collapsed. Risk acceptances are conditional on their assumptions; when the assumptions die, the acceptance needs re-deciding.

**Question 6 (moderate) — The junior architect's flawed design**

A talented junior security architect on a high-profile programme presents a design at your cross-organisation review forum. The design contains a significant flaw in its session-management approach that could expose citizen data. The junior architect is visibly proud of the work, and their programme director is in the room.

A) Identify the flaw plainly but constructively in the forum — since the forum exists to catch exactly this — framing it as a hard problem, crediting the design's strengths, and offering to pair with them on the fix.
B) Say nothing in the forum and email the flaw to their programme director afterwards.
C) Approve the design to protect the junior architect's confidence, and fix the flaw quietly later.
D) Ask pointed questions in the forum until the junior architect discovers the flaw themselves, however long that takes.

**Most effective: A. Least effective: C.**

**Explanation:** Your role makes you an exemplar: how you handle this moment teaches every architect present what review culture is. Option A keeps the forum honest — flaws are found where finding them is the point — while modelling that critique targets designs, not people; crediting strengths and offering to pair converts a correction into development. Option B undermines the forum's purpose and, worse, routes the criticism through the person's boss rather than to them — a trust-damaging move disguised as tact. Option D has a socratic charm but is theatre at a junior colleague's expense in front of their director; used briefly it can work, but "however long that takes" makes it an ordeal. Option C is least effective: it puts citizen data at risk to spare feelings, falsifies the review's outcome, and denies the architect the feedback they need to grow. Kindness that suppresses safety-relevant truth is not kindness — and an approval you privately intend to unpick is a precedent you never want to set.

**Question 7 (hard) — Constrained timescales, senior expectations**

A permanent secretary's office asks you, at 16:00, for "a one-page view of whether the new data-sharing platform is safe to announce tomorrow morning". The platform's architecture review is 80% complete: the finished portions are sound, but the review of its consent-management integration — the politically sensitive part — is unfinished. Your team could work overnight but would still only reach partial coverage.

A) Provide a one-pager stating the platform is safe, since the completed 80% found no major issues.
B) Provide a one-pager that states precisely what has been reviewed and found sound, what remains unreviewed — naming the consent-management integration — and what could be said safely in tomorrow's announcement, offering a completion date for the rest.
C) Reply that the review is incomplete and no view can be given until it finishes.
D) Ask your team to work overnight to finish as much as possible before answering.

**Most effective: B. Least effective: A.**

**Explanation:** This is expectation management "across high risk and complexity or under constrained timescales" in its purest form. Option B answers the actual question senior leaders need answered — what can be said tomorrow — with precision about the evidence's boundaries; it converts an unfinished review into usable, honest advice and gives the office the means to calibrate the announcement's wording. That is translation of security implications at the most senior levels. Option C is truthful but unhelpful: "no view" abandons the stakeholder at the moment of need, when a bounded view exists and is valuable. Option D burns the team for marginal coverage without first establishing what the office actually needs — and still answers late. Option A is least effective and professionally dangerous: it converts 80% coverage into a 100% assurance, on exactly the axis (consent management) most likely to attract scrutiny. If the unreviewed integration later fails publicly, the record will show you certified safety you had not established — the single fastest way to destroy the trust your role runs on.

**Question 8 (moderate) — The shiny new technology**

Your chief digital officer returns from an industry conference enthusiastic about an AI-driven security operations product and asks you to "get it adopted this quarter". Your initial reading suggests genuine promise for alert triage, but the product processes telemetry in the vendor's cloud, and its claims about detection rates come solely from the vendor's marketing material.

A) Support the CDO's timeline and begin procurement, since executive sponsorship for security investment is rare and valuable.
B) Decline adoption on the grounds that vendor marketing claims are unreliable.
C) Welcome the interest, propose a time-boxed evaluation this quarter — independent validation of detection claims, a data-protection and telemetry-residency assessment, and a bounded pilot on non-sensitive alert streams — and agree with the CDO what evidence would justify full adoption.
D) Ask the vendor to present directly to the security team so they can decide.

**Most effective: C. Least effective: A.**

**Explanation:** Your role profile asks you to "research, identify, validate and adopt new technologies" — validation is the step that separates innovation from fashion. Option C preserves the CDO's momentum (a real asset, as option A observes) while installing exactly the controls a principal architect exists to provide: independent evidence for claims, a residency and data-protection assessment for the telemetry question, and a bounded pilot that limits downside. Crucially it also pre-agrees the adoption criteria, turning a potential future conflict into a shared decision framework. Option B wastes the sponsorship and substitutes cynicism for validation — marketing claims are to be tested, not merely distrusted. Option D outsources an architectural judgement to a vendor presentation, the least reliable evidence format available. Option A is least effective: committing procurement before validating claims or assessing where sensitive telemetry flows inverts the entire risk-based approach, and a failed high-profile adoption would also poison the well for the next genuinely good technology.

**Question 9 (moderate) — Sharing beyond the organisation**

You have developed a well-tested architectural approach for securing cross-departmental API integrations, refined through two years of production use. A security community of practice spanning government invites you to present it, and a former colleague at another department asks for your working documents. Your programme director worries that sharing might "give away our advantage" and expose weaknesses to scrutiny.

A) Present a high-level version publicly but decline to share the working documents.
B) Explain to the director that furthering the profession is part of your role and government security improves collectively; review the materials to remove any genuinely sensitive specifics; then present and share the sanitised documents, inviting scrutiny as a strength.
C) Decline both invitations to respect the director's concern.
D) Share everything as-is, since transparency across government overrides the director's view.

**Most effective: B. Least effective: C.**

**Explanation:** Your role explicitly includes furthering the profession and "demonstrating and sharing best practice within and outside the organisation", and engaging with the broader security community. Option B does this while taking the director's concern seriously in the one way it is legitimate: genuinely sensitive operational specifics (exact configurations, known residual weaknesses, incident details) should be sanitised before sharing. It also reframes scrutiny correctly — peer challenge hardens patterns, and a pattern that cannot survive community review should not be a pattern. Option A is a defensible half-measure but hoards the useful substance; departments do not compete on security, and "advantage" is the wrong frame for public service. Option D shares recklessly, ignoring that some content may truly need redaction, and steamrolls a stakeholder you need for future sharing. Option C is least effective: it treats a misplaced concern as a veto, fails the profession-building duty of the role, and models exactly the insularity that keeps government departments solving the same security problems separately.

**Question 10 (hard) — The policy collision**

A new government-wide digital policy requires all citizen-facing services to offer a fully offline, paper-based channel. Your fraud-risk analysis shows the paper channel, as specified, would bypass the digital identity verification that currently prevents an estimated £4 million of annual fraud, and the policy's implementation guidance is silent on compensating controls. Your organisation's policy team plans to implement the guidance as written.

A) Implement the policy as written, since government-wide policy overrides local risk concerns.
B) Advise your organisation to refuse to implement the paper channel until the policy is amended.
C) Prepare a quantified analysis of the fraud exposure and design candidate compensating controls for the paper channel; work with your policy team to implement the channel safely; and feed the gap and your proposed controls back to the policy's owners through formal channels so the guidance improves for every department.
D) Implement the policy but document your objection in the risk register for the record.

**Most effective: C. Least effective: B.**

**Explanation:** The paper channel serves genuine user needs — accessibility and inclusion for citizens who cannot or will not transact digitally — so the goal is to deliver it safely, not to defeat it. Option C is your "understanding security implications of transformation" skill operating exactly as specified: challenging and leading changes to policy and processes to support business outcomes, with legal and political awareness. It secures the local implementation with compensating controls, and — the distinctly principal-level move — exports the fix upstream so every department inherits better guidance. Option A abdicates the analysis you uniquely can provide; policies are implemented by people who notice their gaps. Option D is compliance theatre: a documented objection mitigates nothing and protects only its author. Option B is least effective because refusing a lawful, user-serving government-wide policy positions security as an obstacle to inclusion, is politically untenable, and forfeits the influence you would otherwise have over how the channel is secured. The strongest security voices in government are the ones that make required things safe, not the ones that say no to requirements.

**Question 11 (moderate) — The exploitability disagreement**

Your team's penetration testers rate a finding in a citizen-service API as critical, recommending an emergency change freeze. The delivery team's lead engineer argues the finding is theoretical because exploitation requires an authenticated session with elevated scopes, which external attackers cannot obtain. You review the technical detail and conclude exploitation is harder than the testers assess but easier than the engineer believes: a mid-complexity chain via a partner integration could reach it.

A) Back the testers' critical rating to be safe, and support the change freeze.
B) Back the engineer's assessment to keep delivery moving, and downgrade the finding.
C) Publish your own analysis of the realistic exploit chain, re-rate the finding accordingly with the partner-integration path named, and agree a proportionate response — an expedited fix on the partner integration path rather than a full freeze — explaining your reasoning to both teams.
D) Commission an external third party to re-test before taking any position.

**Most effective: C. Least effective: B.**

**Explanation:** "Identify and explain how easy or difficult it will be to exploit vulnerabilities" is a named skill of your role, and this scenario tests whether you will actually exercise it when both easier paths — deference to caution (A) or to delivery (B) — are available. Option C does the expert work: it replaces two partial assessments with a concrete exploit-chain analysis, produces a rating both sides can interrogate, and matches the response to the real attack path, protecting users without an unnecessary freeze. It also models intellectual honesty — agreeing with neither camp entirely — which is what makes an escalation point trusted. Option A is safe-looking but wrong: systematically inflating ratings burns delivery goodwill and trains the organisation to discount security severities. Option D defers a judgement you are qualified and paid to make; external validation has its place, but as a supplement to your analysis, not a substitute under time pressure. Option B is least effective because it downgrades a genuinely reachable vulnerability on the strength of an incomplete threat model, leaving citizen data exposed to the path you yourself identified.

**Question 12 (hard) — Ranking under pressure: the breach briefing**

A supplier hosting one of your services reports a confirmed breach of their environment overnight; it is not yet known whether your organisation's data was reached. A morning news story speculates that it was. Your director asks you to lead the technical response and to advise on external communications. Rank these four actions from first to last:

1. Establish, with the supplier, exactly which environments and data stores were reached, and instrument your own ingress points from the supplier for signs of lateral movement.
2. Draft a public statement asserting that no citizen data has been affected, to calm the coverage.
3. Brief the director and communications team on what is known, unknown, and being done to find out — with a timescale for the next update.
4. Review the supplier's contractual breach-notification obligations and evidence-preservation duties, and formally invoke them.

**Correct ranking: 1, 3, 4, 2 — with action 2 executed only in amended form.**

**Explanation:** Action 1 comes first because every subsequent decision — communications, legal, regulatory — depends on establishing the technical facts, and your own network's exposure is time-critical. Action 3 follows immediately: senior stakeholders and communicators need the known/unknown/next-update structure early, and providing it is exactly the translation duty of your role; note that 1 and 3 in practice run nearly in parallel, but a briefing with zero facts serves no one, so a first pass at 1 precedes 3. Action 4 is important but less time-critical by hours: invoking contractual duties formalises cooperation and preserves evidence, and benefits from the initial facts gathered in 1. Action 2 as written should never be executed: asserting "no citizen data affected" before the facts are established is precisely the overclaim that converts a supplier's breach into your organisation's credibility crisis. The defensible version — "we are investigating, here is what we know and when we will update" — belongs to the communications team, informed by your action-3 briefing. Situational judgement scoring rewards spotting that one option is not merely last, but wrong in its stated form.

### Preparation tips

- **Judge from the role, not from the ideal.** Before each scenario, re-anchor: you are the organisation's most senior security architecture voice, an escalation point, an exemplar. Options that would suit a hands-off consultant or a compliance clerk are rarely right for you.
- **Look for the option that addresses the root issue and keeps the risk owner informed.** Across the questions above, winning options share a shape: do the expert analysis, tell the truth with precision, give the decision-maker real options, and strengthen the system for next time.
- **Practise articulating why the weaker options are weaker.** In live assessments (and interviews) you may be asked to justify ratings; the discipline of naming the specific failure — passivity, overclaim, borrowed authority, hidden information — sharpens your choices.
- **Calibrate against public sector values.** User needs, transparency, collaboration, accessibility and inclusion decided several items above (notably Questions 3, 9 and 10). If two options seem close, the one that serves users and openness usually scores higher.
- **Do not overcorrect into idealism.** The scoring favours practically effective behaviour: option C in Question 10 beats a principled refusal precisely because it delivers the policy safely rather than dying on a procedural hill.

### Common pitfalls

- **Answering idealistically rather than effectively.** Choosing what sounds noble (refusing, escalating, freezing everything) over what actually reduces risk and moves the organisation forward.
- **Selecting passive options.** Waiting for scheduled reviews, posting to backlogs, deferring to external testers, or staying silent at the accountable forum — these consistently score as least effective because they delay action and diffuse ownership.
- **Passing the problem along.** Routing feedback through someone's boss, awaiting instructions you should be shaping, or outsourcing judgements the role exists to make.
- **Overclaiming certainty.** Softened reports, premature "safe to launch" one-pagers and "no data affected" statements are the role-specific catastrophic options; the assessment nearly always includes one, and it is nearly always the least effective.
- **Ignoring the culture you are scored against.** UK public sector scenarios reward collaboration across departments, openness to scrutiny and service of user needs — behaviours a purely commercial framing ("give away our advantage") will misjudge.

## Conclusion

You have now worked through the four assessment areas most relevant to your role as a Principal Security Architect: cognitive ability, numeric reasoning, verbal reasoning and situational judgement. Along the way you have traced exploit paths through layered controls, recomputed loss expectancies and remediation trajectories, dissected assurance reports clause by clause, and weighed the judgement calls that come with being an escalation point, an exemplar and a strategy-setter.

If a theme runs through all four sections, it is this: the assessments do not test something separate from your job — they compress it. The same discipline that makes you effective in a design authority (state the rule precisely, follow the evidence, respect what the material does and does not establish, choose the action that addresses the root issue) is what earns marks under timed conditions. That should be encouraging. You are not preparing to become someone else for a test; you are practising making your existing expertise visible at speed.

As next steps, consider revisiting the questions you found hardest after a week's gap and checking whether your reasoning has stabilised; timing yourself on a full section to build comfort with the clock; and composing a few questions of your own from documents you handle daily, which is the quickest way to internalise how items are constructed. Where a section exposed a genuine gap — perhaps ratio fluency, or the discipline of Cannot Say — a little deliberate practice goes much further than general rereading.

Finally, keep this preparation connected to your wider professional development. The skills rehearsed here — analysis, communication at the most senior levels, risk-based decision support, secure design leadership, research and innovation — are the same ones the GDAD framework asks you to demonstrate and grow. Sharing what you learn, inside and outside your organisation, is both part of your role and one of the best ways to consolidate it. Approach the assessment with the same calm, evidence-led confidence you bring to a board paper or a breach briefing, and you will represent your expertise well. Good luck — you are better prepared than you think.
