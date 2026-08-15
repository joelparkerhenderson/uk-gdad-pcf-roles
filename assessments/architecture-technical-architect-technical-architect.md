# Technical Architect - Psychometric Assessment Resources

## Introduction

Welcome! This guide has been created especially for you as a technical architect working within the UK Government Digital and Data profession. Whether you are preparing for an internal assessment, applying for a new post, or simply want to sharpen the mental skills that underpin your day-to-day work, this document will help you practise, reflect, and build confidence.

Psychometric assessments are structured, standardised exercises that measure the mental capabilities and behavioural tendencies that predict success in a specific role. For a technical architect, that means far more than abstract puzzle-solving. Your role asks you to undertake structured analysis of technical issues and translate that analysis into technical designs. You are consulted about design, you provide design patterns, you identify deeper issues that need fixing, and you look for opportunities to collaborate and reuse components while communicating with both technical and non-technical stakeholders. Every one of those duties draws on measurable cognitive and behavioural skills: spotting patterns, reasoning through logic, interpreting numbers, reading dense documents accurately, and making sound judgements under pressure.

This document is organised into four assessment areas, each mapped to the real skills in your role profile:

1. **Workplace job-specific cognitive assessment** — pattern recognition, logical deduction, error checking, and problem solving using the artefacts you handle every day: architecture diagrams, design documents, dependency maps, and technology roadmaps.
2. **Workplace job-specific numeric reasoning assessment** — interpreting capacity figures, cloud hosting costs, performance metrics, and programme budgets, the numbers behind sound architectural decisions.
3. **Workplace job-specific verbal reasoning assessment** — reading and drawing accurate conclusions from standards, policies, governance papers, and stakeholder emails.
4. **Workplace job-specific situational judgement assessment** — navigating realistic dilemmas involving delivery teams, governance boards, suppliers, and non-technical stakeholders.

Each section explains what the assessment measures, maps it to your named role skills, gives you a substantial set of practice questions with fully worked answers, and closes with preparation tips and common pitfalls to avoid.

How should you use this guide? Work through it at your own pace. Try each question honestly before reading the answer, then study the worked explanation even when you got it right — the reasoning method matters more than the result. Use the questions for self-reflection too: ask yourself where you felt confident, where you hesitated, and what that tells you about your development priorities. Assessments reward calm, methodical thinking, and that is a skill you can absolutely practise and improve. Good luck — you have more of these skills already than you may realise.

## Advisory

"This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff."

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive ability assessment is a targeted psychometric test that measures the exact mental processes needed for your role, rather than abstract intelligence. Instead of generic puzzles, it uses practical workplace scenarios and data formats drawn from the everyday work of a technical architect: solution design documents, dependency diagrams, integration sequences, error logs, and technology roadmaps.

Typical format and timing: these tests are usually delivered online and timed, most commonly 15 to 30 minutes, with objective scoring against a benchmark or norm group. Some platforms are adaptive, adjusting question difficulty based on your previous answers, and most provide a few short, ungraded practice questions first so you can get used to the interface. Employers usually receive a breakdown of speed versus accuracy rather than a single score, so working carefully matters as much as working quickly.

Why does this matter for a technical architect? Your role level description says you are responsible for the design and build of technical architecture, and that you undertake structured analysis of technical issues, translating this analysis into technical designs that describe a solution. Structured analysis is cognition in action: decomposing a messy problem, spotting the pattern beneath the symptoms, checking designs for internal contradictions, and deducing the consequences of a change before it happens. A cognitive assessment is essentially a compressed, measurable version of what you do when a delivery team brings you a tangled integration problem and asks "what is actually going wrong here?"

### What it measures for your role

The assessment dimensions map directly onto the skills named in your role profile:

- **Technical design throughout the life cycle** — logical deduction and problem solving mirror your duty to create technical designs characterised by managed levels of risk, impact, and complexity, and to adapt a technical design if needed during delivery. Questions test whether you can trace cause and effect through a system and spot where a design breaks.
- **Making architectural decisions** — error checking and consistency checking reflect your duty to identify and address architectural risks relevant to your team or domain, for example business, data, or security risks. Questions ask you to find the flaw, the contradiction, or the unmanaged risk in a set of statements or a design.
- **Architect for the whole context** — pattern recognition reflects your duty to track emerging issues, strategies, roadmaps, patterns and technologies over time to assess opportunities and risks. Questions test whether you can extrapolate a trend or spot a recurring structure.
- **Strategy design** — prioritisation and rule-application questions reflect your duty to use architectural principles, patterns, and constraints when appropriate, and to challenge requirements and assumptions.
- **Architecture communication** — several questions use written design statements from mixed technical and non-technical sources, reflecting your duty to listen to the needs of technical and business stakeholders and achieve agreement across them.

### Practice questions

Work through each question before reading the answer. The reasoning method in each explanation is the real lesson.

**Question 1 (easy) — Pattern recognition in versioned releases**

A government service platform follows a strict release pattern for its API. Recent releases were versioned: 2.3.1, 2.3.2, 2.4.0, 2.4.1, 2.4.2, 2.5.0, 2.5.1. Patch releases fix defects without changing the interface; minor releases add capability. Following the established pattern, which release comes next if the team ships one more defect fix and then one new capability?

- A) 2.5.2 then 2.6.0
- B) 2.6.0 then 2.6.1
- C) 2.5.2 then 2.5.3
- D) 3.0.0 then 3.0.1

**Correct answer: A**

**Explanation:** The pattern shows two patch releases after each minor release, then a new minor version with the patch counter reset to zero. A defect fix after 2.5.1 increments the patch number to 2.5.2; the following new capability increments the minor number and resets the patch, giving 2.6.0. Option D would imply a breaking change, which nothing in the scenario supports. This is the same disciplined reading of semantic versioning you apply when providing design patterns for API management.

**Question 2 (easy) — Logical deduction from design rules**

Your organisation's architecture principles state: (1) All citizen-facing services must be hosted on the approved cloud platform. (2) Any service holding OFFICIAL-SENSITIVE data must use the encrypted storage pattern. (3) Services on the approved cloud platform may use either the standard or the encrypted storage pattern. A new citizen-facing benefits calculator holds OFFICIAL-SENSITIVE data. Which statement must be true?

- A) The service must be hosted on the approved cloud platform and use the standard storage pattern.
- B) The service must be hosted on the approved cloud platform and use the encrypted storage pattern.
- C) The service may be hosted anywhere as long as it uses the encrypted storage pattern.
- D) The service cannot be built because the rules conflict.

**Correct answer: B**

**Explanation:** Rule 1 applies because the service is citizen-facing, so the approved cloud platform is mandatory. Rule 2 applies because the data is OFFICIAL-SENSITIVE, so encrypted storage is mandatory. Rule 3 confirms the two requirements are compatible, since the approved platform permits the encrypted pattern. There is no conflict; both constraints simply stack. Applying multiple architectural constraints simultaneously and checking they compose is core to making architectural decisions with managed levels of risk.

**Question 3 (moderate) — Error checking a dependency map**

You are reviewing a dependency statement for a case-management solution before a design review. The document states:

1. Service A depends on Service B.
2. Service B depends on Service C.
3. Service C depends on Service D.
4. Service D has no dependencies.
5. Service C can be deployed independently of all other services.

Which two statements are mutually inconsistent?

- A) 1 and 2
- B) 2 and 5
- C) 3 and 5
- D) 3 and 4

**Correct answer: C**

**Explanation:** Statement 3 says Service C depends on Service D, meaning C cannot function, and generally cannot be deployed as a working unit, independently of D. Statement 5 claims C can be deployed independently of all other services. Those two claims cannot both be true. Statement 2 (B depends on C) does not contradict statement 5, because other services depending on C does not constrain C's own deployability. Spotting exactly this kind of contradiction before it reaches a governance board is what "identify deeper issues that need fixing" looks like in practice.

**Question 4 (moderate) — Prioritisation under constraint**

Four technical issues land on your desk on the same morning. You can address only one before midday:

- Issue W: A design flaw in a service going live in three weeks; fixing it later doubles the cost.
- Issue X: An outage on a live citizen-facing service; the incident team has asked for architectural advice within the hour.
- Issue Y: A request to review a design pattern for a project starting next quarter.
- Issue Z: A recurring minor defect in an internal tool, raised for the third time.

Which is the most defensible order of priority for your morning?

- A) W, X, Y, Z
- B) X, W, Z, Y
- C) Z, X, W, Y
- D) X, Y, W, Z

**Correct answer: B**

**Explanation:** Live citizen impact with an explicit one-hour request (X) outranks everything: harm is occurring now and you have been directly asked. W is next because it is time-sensitive and cost escalates with delay. Z, though minor, is recurring — a signal of a deeper issue worth a brief look, consistent with your duty to identify deeper issues that need fixing — and comes ahead of Y, which has a full quarter of lead time. Option A ignores the live incident's urgency; option D defers a costly known flaw behind a next-quarter review. Prioritisation questions reward reasoning about impact, urgency, and irreversibility together, not any single factor.

**Question 5 (moderate) — Sequence logic in a migration plan**

A legacy system migration has five steps with these constraints: Data cleansing must finish before data migration begins. The new platform must be provisioned before data migration begins. User training can start any time after platform provisioning. The legacy system can be decommissioned only after data migration is complete and user training is complete. Which of the following orderings is valid?

- A) Provision platform → data cleansing → data migration → user training → decommission legacy
- B) Data cleansing → data migration → provision platform → user training → decommission legacy
- C) Provision platform → user training → decommission legacy → data cleansing → data migration
- D) Data cleansing → user training → provision platform → data migration → decommission legacy

**Correct answer: A**

**Explanation:** Check each constraint against option A: cleansing precedes migration (yes), provisioning precedes migration (yes), training follows provisioning (yes), decommissioning follows both migration and training (yes). Option B migrates data before the platform exists. Option C decommissions the legacy system before any data has been migrated. Option D starts user training before the platform is provisioned. This is dependency ordering — exactly the reasoning you use when providing guidance and support to teams using technical designs throughout the life cycle, where a plausible-looking plan can hide an impossible sequence.

**Question 6 (moderate) — Pattern recognition in incident data**

Over six weeks, a payments integration logged these timeout incidents: Week 1: 2, Week 2: 4, Week 3: 8, Week 4: 16, Week 5: 32. The delivery team says "it's random noise; volumes are flat." What is the strongest logical conclusion?

- A) The incidents are random because timeouts always vary week to week.
- B) The incidents double weekly despite flat volumes, indicating a systematic worsening cause, and week 6 will likely see around 64 if nothing changes.
- C) The team is right; five data points cannot show a pattern.
- D) The platform must be under a denial-of-service attack.

**Correct answer: B**

**Explanation:** The series 2, 4, 8, 16, 32 is a clean doubling pattern. Random noise does not produce consistent exponential growth, and flat transaction volumes rule out demand as the driver, so something systematic — perhaps a growing queue, a resource leak, or degrading dependency — is worsening. Option D leaps to a specific cause the data cannot establish; the data shows a pattern, not a mechanism. The disciplined move, which B captures, is to name the pattern, project it, and investigate the cause. Tracking emerging issues over time to assess risks is precisely this skill.

**Question 7 (moderate) — Reuse logic**

Your role asks you to look for opportunities to collaborate and reuse components. Three teams each need a document-upload capability. Team 1 needs virus scanning and a 50 MB limit. Team 2 needs virus scanning and a 50 MB limit. Team 3 needs virus scanning, a 500 MB limit, and video transcoding. A colleague proposes building one shared component that meets all three requirement sets in full. Which reasoning is most sound?

- A) Build the full shared component; one component is always cheaper than three.
- B) Build a shared core (virus scanning, configurable size limit) that all three teams reuse, and let Team 3 add transcoding as an extension, because the common subset is stable while transcoding is a single-team need.
- C) Build three separate components; teams should never share code.
- D) Refuse Team 3's requirements so the shared component stays simple.

**Correct answer: B**

**Explanation:** The logical structure here is set intersection: virus scanning and size limiting are common to all three; transcoding belongs to one. Forcing single-team functionality into a shared component (option A) couples all three teams to complexity two of them never use and makes the shared thing harder to govern. Option C forfeits genuine reuse of the common subset. Option D solves the architecture's problem by breaking a team's legitimate need, inverting your purpose. B maximises reuse where requirements genuinely intersect and isolates divergence at the edge — the standard pattern reasoning behind component reuse.

**Question 8 (hard) — Deduction with layered rules**

A security review of your design must satisfy all of these governance rules: (1) If a service processes personal data, it must complete a Data Protection Impact Assessment (DPIA). (2) If a DPIA identifies high residual risk, the design must go to the architecture review board. (3) Any service integrating with the legacy HR system must go to the architecture review board regardless of other factors. (4) Services that go to the architecture review board cannot ship in the current quarter. Your service processes personal data, its DPIA found low residual risk, and it integrates with the legacy HR system. Which conclusion is valid?

- A) The service can ship this quarter because the DPIA found low residual risk.
- B) The service must go to the review board and cannot ship this quarter, because of rule 3 and rule 4.
- C) The service does not need a DPIA because the risk is low.
- D) The rules are contradictory, so the architect may choose freely.

**Correct answer: B**

**Explanation:** Trace each rule. Rule 1 fires: personal data means a DPIA, which was done. Rule 2 does not fire: residual risk is low. But rule 3 fires independently: legacy HR integration forces review board attendance "regardless of other factors". Rule 4 then chains from rule 3: board attendance blocks a current-quarter ship. Option A makes the classic error of letting one satisfied rule (rule 2 not triggering) obscure another that triggers independently. When you engage with architectural governance and assurance to manage decisions and risks, this is the skill: rules compose, and the strictest applicable path wins.

**Question 9 (hard) — Fault diagnosis from symptoms**

A citizen-facing service intermittently returns stale data. The architecture is: browser → CDN cache (60-second TTL) → API gateway → application → database read replica (replication lag normally under 1 second). Investigation shows: the CDN is correctly honouring its TTL; the API gateway adds no caching; replication lag spiked to 15 minutes during the incident windows. Which is the most logical diagnosis?

- A) The CDN TTL is too long and should be reduced to 10 seconds.
- B) The staleness is caused by replication lag: reads served from the replica during lag spikes return data up to 15 minutes old, far exceeding anything the CDN could cause.
- C) The API gateway is secretly caching responses.
- D) Users' browsers are caching pages locally.

**Correct answer: B**

**Explanation:** Quantify each candidate cause. The CDN can serve data at most 60 seconds old — noticeable, but not the reported staleness during incidents. The gateway is confirmed non-caching, eliminating C without evidence to reopen it. D cannot explain a fleet-wide, time-correlated pattern. Replication lag of 15 minutes during exactly the incident windows both matches the magnitude and correlates in time — the two hallmarks of a genuine cause. Option A "fixes" a component that is behaving correctly, adding load without addressing the fault. Structured analysis of technical issues means matching the size and timing of the symptom to the size and timing of the cause.

**Question 10 (hard) — Logical consistency across stakeholder requirements**

Three stakeholders give you requirements for a data-sharing platform. The business owner: "Every access to a citizen record must be approved by a caseworker before the data is released." The service manager: "Automated partner systems must be able to retrieve records in under two seconds, twenty-four hours a day." The security lead: "No standing approvals; every approval must be case-by-case and recorded." Which statement best describes the requirement set?

- A) The requirements are compatible as written.
- B) The requirements conflict: case-by-case human approval before release cannot coexist with unattended two-second automated retrieval, so the conflict must be surfaced and negotiated.
- C) The security lead's requirement should be silently dropped as impractical.
- D) The service manager's requirement should be silently dropped as unrealistic.

**Correct answer: B**

**Explanation:** Deduce the joint consequence: two-second, round-the-clock automated retrieval leaves no room for a human caseworker in the request path; case-by-case approval with no standing approvals puts a human in every request path. Both cannot hold for the same access. The reasoning failure in options C and D is not the analysis but the behaviour: an architect who silently drops a requirement has stopped listening to the needs of technical and business stakeholders and started overruling them. Your role is to detect the logical incompatibility, make it visible, and help stakeholders choose — perhaps pre-approved access categories, or a fast path for certain record types — achieving agreement rather than assuming it.

**Question 11 (moderate) — Spotting the unstated assumption**

A delivery team proposes: "Our new notifications component handled 1,000 messages per minute in the test environment, therefore it will comfortably handle production, which peaks at 800 messages per minute." As the consulted architect, which unstated assumption most needs checking?

- A) That messages exist in production.
- B) That the test environment matches production in the ways that matter — data volumes, message sizes, concurrent services, infrastructure sizing, and downstream latency.
- C) That the team ran the test on a weekday.
- D) That 800 is smaller than 1,000.

**Correct answer: B**

**Explanation:** The argument's logical bridge is "test performance predicts production performance", which holds only if the environments are equivalent in the relevant respects. Test environments are routinely smaller, quieter, and loaded with cleaner data than production; a component that manages 1,000 messages per minute alone on an idle cluster may buckle at 500 when competing for resources against live workloads with production-sized payloads. Options A, C, and D are either trivially true or irrelevant. Challenging requirements and assumptions is explicitly part of your strategy design skill — and the highest-value assumptions to challenge are the invisible ones holding up a confident conclusion.

**Question 12 (hard) — Multi-step problem solving with constraints**

You must place four services (P, Q, R, S) across two hosting zones (Zone 1 and Zone 2) under these constraints: P and Q must not share a zone (they are each other's disaster-recovery pair). R must be in the same zone as S (they share a low-latency link). S must not be in Zone 1 (its data residency approval covers Zone 2 only). Q requires a hardware security module, available only in Zone 1. Where must each service go?

- A) P: Zone 1; Q: Zone 2; R: Zone 1; S: Zone 2
- B) P: Zone 2; Q: Zone 1; R: Zone 2; S: Zone 2
- C) P: Zone 2; Q: Zone 1; R: Zone 1; S: Zone 2
- D) The constraints cannot all be satisfied.

**Correct answer: B**

**Explanation:** Work from the hardest constraints inward. Q needs the hardware security module, so Q is in Zone 1. P must not share with Q, so P is in Zone 2. S cannot be in Zone 1, so S is in Zone 2. R must be with S, so R is in Zone 2. That yields exactly option B, and every constraint checks out. Option A breaks the hardware security module constraint; option C separates R from S. The method — fix the most constrained element first, then propagate — is how you make placement, sequencing, and technology decisions with managed complexity rather than trial and error.

**Question 13 (moderate) — Recognising a recurring anti-pattern**

Across three project reviews you note: Project 1 built its own user-authentication code rather than using the platform's identity service, and later failed a security test. Project 2 built its own PDF-generation library rather than using the shared component, and now carries an unpatched vulnerability. Project 3 proposes building its own address-lookup service rather than integrating the national address gateway. What is the most useful pattern-level observation?

- A) All three projects have weak developers.
- B) There is a recurring organisational pattern of rebuilding available components, which repeatedly introduces security and maintenance risk; the response should address why teams avoid reuse, not just block Project 3.
- C) Project 3 should simply be blocked and the pattern will stop.
- D) Coincidence; three cases prove nothing.

**Correct answer: B**

**Explanation:** Pattern recognition at the architectural level means abstracting from instances to structure: three independent teams making the same class of decision with the same class of consequence is a systemic signal, not three accidents. Option C treats the symptom — the third instance — while leaving the generating cause (perhaps components that are hard to discover, poorly documented, or slow to get access to) untouched, guaranteeing a Project 4. Option A attributes to individuals what the pattern suggests is environmental. Identifying deeper issues that need fixing, and looking for opportunities to collaborate and reuse components, converge exactly here.

**Question 14 (easy) — Error checking a design summary**

A design summary states: "The service will store citizen documents for seven years, in line with the retention policy. Documents are deleted automatically after five years. Retention is fully policy-compliant." What is wrong?

- A) Nothing; the summary is consistent.
- B) The stated retention period (seven years) contradicts the stated deletion behaviour (five years), so the compliance claim is unsupported.
- C) Seven years is too long for any policy.
- D) Automatic deletion is never acceptable.

**Correct answer: B**

**Explanation:** Two sentences apart, the document commits to keeping documents for seven years and to deleting them after five. The third sentence then asserts compliance, which cannot be true of both behaviours at once. Assessments love this format because real design documents accumulate exactly these drift errors as sections are edited by different hands at different times. Careful error checking before a document reaches governance is a small habit with a large payoff.

### Preparation tips

- **Practise with your own artefacts.** Take a real design document, dependency diagram, or set of architecture principles and interrogate it: what must be true, what cannot be true, what is assumed? This builds exactly the muscles the test measures, using material you already understand.
- **Verbalise your deduction chains.** For each practice question, say the reasoning out loud: "Rule 3 fires, therefore board review, therefore no ship this quarter." Explicit chains are faster and less error-prone under time pressure than intuition, and they mirror how you already explain decisions to stakeholders.
- **Learn to bank easy marks.** These tests report speed and accuracy. Answer the questions you find quick first, flag the heavy multi-constraint ones, and return. One stubborn placement puzzle should never cost you four easier questions.
- **Do the ungraded practice questions properly.** Most platforms offer a short warm-up. Use it to settle nerves and learn the interface — where the timer sits, how to flag questions — so no attention is wasted on mechanics during the scored section.
- **Rest beats cramming.** Cognitive throughput is measurably better when you are rested and calm. Prepare steadily in the days before, then protect your sleep the night before. You reason for a living; the assessment samples a skill you exercise daily.

### Common pitfalls

- **Bringing outside knowledge into the question.** You may know that a real cloud platform behaves differently from the one described. Answer from the rules given, exactly as you would honour a stated constraint in a design review even while planning to challenge it afterwards.
- **Stopping at the first satisfied rule.** As in Question 8, one rule not firing does not mean no rule fires. Check every rule against the scenario before concluding — the strictest applicable path governs.
- **Confusing plausibility with deduction.** An answer that sounds like good practice may not follow from the given premises. The test asks what must be true, not what is usually sensible.
- **Time-sink questions.** Multi-constraint placement problems (like Question 12) can absorb five minutes. If a question resists after ninety seconds, flag it and move on; return with fresh eyes if time allows.
- **Rushing the reading.** Many errors are reading errors, not reasoning errors. The scenario's small print — "regardless of other factors", "independently of all other services" — usually decides the answer, just as small print in a standards document decides a compliance question.


## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment evaluates your ability to analyse, interpret, and make logical decisions using numerical data. It deliberately mimics the data-handling demands of your actual role: not abstract formulae, but the business mathematics of technical architecture — hosting costs, capacity figures, performance metrics, licensing comparisons, and migration budgets, presented as tables, charts, and short datasets.

Typical format and timing: these tests present real-world business data — graphs, cost tables, project schedules — and ask questions built on percentages, ratios, conversions, and cost-benefit estimation. Most assessments allow or provide an onscreen calculator, because the point is interpretation rather than mental arithmetic. Time limits are strict, typically around a minute to ninety seconds per question, so quick and accurate data extraction matters as much as calculation.

Why does this matter for a technical architect? Numbers sit underneath almost every architectural decision you make. Creating technical designs characterised by managed levels of risk, impact, and complexity means being able to say what a design costs, what load it must carry, and what happens to both when demand doubles. Assessing opportunities and risks from emerging technologies means comparing options quantitatively, not just qualitatively. And communicating with non-technical stakeholders very often means translating a technical choice into a financial or performance number they can weigh. An architect who cannot interrogate a cost table or a latency chart is negotiating blind.

### What it measures for your role

- **Making architectural decisions** — cost-benefit comparisons, risk-weighted estimates, and total-cost-of-ownership calculations reflect your duty to make architectural design decisions characterised by managed levels of risk and complexity. Several questions ask you to choose between options using the numbers alone.
- **Technical design throughout the life cycle** — capacity, throughput, and performance questions reflect your duty to create designs with managed impact, and to adapt a technical design if needed during delivery when the measured numbers diverge from the assumed ones.
- **Architect for the whole context** — trend and trajectory questions (growth rates, cost curves) reflect your duty to track emerging issues and technologies over time to assess opportunities and risks.
- **Strategy design** — budget and roadmap questions reflect your duty to support the implementation of a strategy or vision, for example by using a roadmap or plan, where phasing and affordability are numerical questions.
- **Architecture communication** — every explanation in this section shows how to express the arithmetic in plain terms, because achieving agreement with non-technical stakeholders usually means walking them through the numbers.

### Practice questions

An onscreen calculator is normally allowed; feel free to use one. What matters is choosing the right calculation and reading the data accurately. All figures are illustrative.

**Question 1 (easy) — Percentage change in hosting cost**

Your service's monthly cloud hosting bill was £12,400 in March. In April, after you introduced auto-scaling, it fell to £9,920. What was the percentage reduction?

- A) 15%
- B) 20%
- C) 25%
- D) 24.8%

**Correct answer: B**

**Explanation:** Reduction = £12,400 − £9,920 = £2,480. Percentage reduction = £2,480 ÷ £12,400 = 0.20 = 20%. A common slip is dividing by the new figure (£2,480 ÷ £9,920 = 25%, option C); percentage change is always measured against the starting value. When you report a saving to a service owner, this distinction is exactly what keeps your numbers credible.

**Question 2 (easy) — Capacity headroom**

A service handles a peak of 3,600 requests per minute. The platform is currently provisioned for 4,500 requests per minute. What percentage headroom does the design have at peak?

- A) 20%
- B) 25%
- C) 80%
- D) 900%

**Correct answer: B**

**Explanation:** Headroom = (4,500 − 3,600) ÷ 3,600 = 900 ÷ 3,600 = 0.25 = 25%. The provisioned capacity exceeds peak demand by a quarter of that demand. Option A comes from dividing by the capacity instead of the demand (900 ÷ 4,500 = 20%); both framings appear in real capacity documents, so always state which base you are using. Quantified headroom is one of the clearest ways to describe managed risk in a technical design.

**Question 3 (moderate) — Comparing two hosting options**

You are choosing between two options for a case-management service over a three-year period.

| Cost item | Option A (public cloud) | Option B (managed platform) |
|---|---|---|
| Setup (one-off) | £18,000 | £45,000 |
| Monthly running cost | £6,500 | £5,200 |
| Annual support contract | £12,000 | £6,000 |

Which option is cheaper over three years, and by how much?

- A) Option A, by £9,800
- B) Option B, by £2,200
- C) Option B, by £37,800
- D) Option A, by £27,000

**Correct answer: C**

**Explanation:** Option A: £18,000 + (£6,500 × 36 months = £234,000) + (£12,000 × 3 = £36,000) = £288,000. Option B: £45,000 + (£5,200 × 36 = £187,200) + (£6,000 × 3 = £18,000) = £250,200. Difference = £288,000 − £250,200 = £37,800 in Option B's favour. The trap is anchoring on the setup cost, where A looks £27,000 cheaper (option D reflects that partial view); over the full period, B's lower running costs dominate. Total cost of ownership over the whole life cycle, not the sticker price, is the architecturally sound comparison.

**Question 4 (moderate) — Ratios in team allocation**

Your programme has 24 engineers split across build, integration, and support work in the ratio 4:2:2. The programme board asks what a shift to 3:3:2 would mean. How many engineers move, and from where to where?

- A) 3 engineers move from build to integration
- B) 2 engineers move from build to integration
- C) 3 engineers move from support to integration
- D) No engineers move; the ratios are equivalent

**Correct answer: A**

**Explanation:** Current ratio 4:2:2 has 8 parts across 24 engineers, so each part is 3 engineers: build 12, integration 6, support 6. The new ratio 3:3:2 also has 8 parts of 3: build 9, integration 9, support 6. Build falls from 12 to 9 and integration rises from 6 to 9, so 3 engineers move from build to integration; support is unchanged. Identifying the best team makeup depending on the situation — part of your community collaboration skill — often starts with exactly this arithmetic.

**Question 5 (moderate) — Reading a performance table**

Four API endpoints report the following monthly figures:

| Endpoint | Requests (thousands) | Errors | Mean response (ms) |
|---|---|---|---|
| /search | 840 | 4,200 | 320 |
| /submit | 210 | 1,680 | 610 |
| /status | 1,260 | 2,520 | 95 |
| /documents | 420 | 3,780 | 480 |

Which endpoint has the highest error rate?

- A) /search
- B) /submit
- C) /status
- D) /documents

**Correct answer: D**

**Explanation:** Error rate = errors ÷ requests. Note the scale qualifier: requests are in thousands. /search: 4,200 ÷ 840,000 = 0.50%. /submit: 1,680 ÷ 210,000 = 0.80%. /status: 2,520 ÷ 1,260,000 = 0.20%. /documents: 3,780 ÷ 420,000 = 0.90%. /documents is highest at 0.90%. The raw error count would point at /search (option A), and the slowest response time would point at /submit (option B) — but the question asks for rate. Missing a "(thousands)" qualifier, or answering an adjacent question rather than the one asked, are the two most common table-reading errors in these assessments and in real dashboard reviews alike.

**Question 6 (moderate) — Percentage growth and forecasting**

Registrations on a digital service grew from 50,000 in the first quarter to 60,000 in the second quarter, then to 72,000 in the third. If this quarterly growth rate continues, roughly how many registrations should the architecture support in the fourth quarter?

- A) 84,000
- B) 86,400
- C) 79,200
- D) 92,000

**Correct answer: B**

**Explanation:** Growth from 50,000 to 60,000 is ×1.2 (20%); from 60,000 to 72,000 is also ×1.2. Constant multiplicative growth gives the fourth quarter as 72,000 × 1.2 = 86,400. Option A assumes linear growth of a flat 12,000 per quarter, which understates a compounding trend. Whether growth is linear or compounding is exactly what you must judge when tracking emerging issues over time: the same three data points imply very different capacity plans a year out (linear: 122,000; compounding: about 179,000).

**Question 7 (hard) — Availability arithmetic**

A service's availability target is 99.5% measured monthly. In a 30-day month (720 hours), the service suffered outages of 1 hour 30 minutes, 45 minutes, and 1 hour 15 minutes. Did it meet the target, and what availability did it achieve?

- A) Yes; it achieved approximately 99.51%
- B) No; it achieved approximately 99.31%
- C) Yes; it achieved approximately 99.72%
- D) No; it achieved approximately 98.95%

**Correct answer: A**

**Explanation:** Total downtime = 90 + 45 + 75 minutes = 210 minutes = 3.5 hours. Availability = (720 − 3.5) ÷ 720 = 716.5 ÷ 720 ≈ 0.99514 = 99.51%. The allowed downtime at 99.5% is 0.5% of 720 hours = 3.6 hours, so 3.5 hours of outage just squeaks inside the target. This is worth internalising: at 99.5% monthly you have roughly three and a half hours of budget; at 99.9% only about 43 minutes. When you set or accept an availability figure in a design, you are committing someone to a downtime budget, and being fluent in the conversion is part of managing risk explicitly.

**Question 8 (hard) — Migration budget with contingency**

A legacy migration is estimated at £480,000 base cost. Governance requires a 15% contingency on the base cost, and the supplier's charges attract VAT at 20% on £300,000 of the base (the remainder is internal staff cost, no VAT, and no VAT applies to the contingency). What total budget should you request?

- A) £612,000
- B) £552,000
- C) £660,000
- D) £618,000

**Correct answer: A**

**Explanation:** Contingency = 15% × £480,000 = £72,000. VAT = 20% × £300,000 = £60,000. Total = £480,000 + £72,000 + £60,000 = £612,000. The most common error is applying both percentages to the full base and to each other — for example 20% VAT on the whole £480,000 gives £96,000 and option D territory. Multi-component budgets require applying each percentage strictly to its own stated base. Supporting the implementation of a strategy through a costed roadmap depends on getting these compositions right, because a budget request you cannot defend line by line will not survive its first governance board.

**Question 9 (hard) — Cost per transaction comparison**

Two integration patterns are proposed for a document-checking service expected to handle 2.4 million checks per year.

| | Pattern X (per-call API) | Pattern Y (batch platform) |
|---|---|---|
| Fixed annual platform cost | £24,000 | £150,000 |
| Cost per check | £0.09 | £0.02 |

At what annual volume do the two patterns cost the same, and which is cheaper at the expected volume?

- A) Break-even at 1.8 million checks; Pattern Y is cheaper at 2.4 million
- B) Break-even at 1.8 million checks; Pattern X is cheaper at 2.4 million
- C) Break-even at 1.4 million checks; Pattern Y is cheaper at 2.4 million
- D) Break-even at 2.6 million checks; Pattern X is cheaper at 2.4 million

**Correct answer: A**

**Explanation:** Set the totals equal: £24,000 + £0.09V = £150,000 + £0.02V, so £0.07V = £126,000, giving V = 1.8 million checks. At the expected 2.4 million: Pattern X costs £24,000 + £216,000 = £240,000; Pattern Y costs £150,000 + £48,000 = £198,000. Y is cheaper by £42,000 per year. Break-even analysis is one of the most useful tools you have for pattern selection, because it converts "it depends" into "it depends on volume, and here is the crossover point" — a formulation both technical and non-technical stakeholders can act on.

**Question 10 (moderate) — Storage growth**

A case-file store currently holds 18 TB and grows by 0.6 TB per month. The current platform tier is capped at 25 TB, and procurement of the next tier takes four months from initiation. Approximately when must you initiate procurement to avoid hitting the cap?

- A) Immediately; the cap will be reached in about 4 months
- B) In about 4 months; the cap will be reached in about 8 months
- C) In about 8 months; the cap will be reached in about 12 months
- D) In about 7 months; the cap will be reached in about 11 months

**Correct answer: D**

**Explanation:** Remaining capacity = 25 − 18 = 7 TB. At 0.6 TB per month, that lasts 7 ÷ 0.6 ≈ 11.7 months, so the cap is reached in roughly 11 to 12 months. Subtracting the four-month procurement lead time means initiating around month 7. Option B undercounts the runway; option A wastes budget by procuring far earlier than needed. Working the lead time backwards from the constraint is the core arithmetic of life-cycle planning: a design is only characterised by managed risk if its consumables — storage, certificates, licences, capacity — are projected forward and diarised.

**Question 11 (moderate) — Interpreting a licensing table**

Software licences for an integration platform cost £1,200 per user per year for the first 50 users, and £900 per user per year for each user beyond 50. Your programme needs licences for 74 users. A supplier quotes £88,800. Is the quote correct?

- A) Yes, the quote is correct
- B) No; the correct figure is £81,600
- C) No; the correct figure is £66,600
- D) No; the correct figure is £86,400

**Correct answer: B**

**Explanation:** First 50 users: 50 × £1,200 = £60,000. Remaining 24 users: 24 × £900 = £21,600. Total = £81,600. The supplier's £88,800 equals 74 × £1,200 — the full rate applied to every user, ignoring the volume discount tier. Checking a quote against its own pricing rules is basic commercial hygiene for an architect: errors of exactly this shape are common, they are always in someone's favour, and finding one in review is far cheaper than finding it at invoice time.

**Question 12 (hard) — Weighing risk numerically**

Two designs are compared for a payments component. Design M has an estimated 2% annual probability of a major incident costing £250,000 in remediation and lost service. Design N reduces that probability to 0.5% but costs £6,000 more per year to run. On expected annual cost alone, which design is preferable, and by how much?

- A) Design M, by £2,250 per year
- B) Design N, by £1,250 per year
- C) Design N, by £4,750 per year
- D) They are equal

**Correct answer: A**

**Explanation:** Expected incident cost for M = 2% × £250,000 = £5,000 per year. For N = 0.5% × £250,000 = £1,250 per year, plus the £6,000 extra running cost, giving a total expected annual cost of £7,250. Comparing the two: M's £5,000 against N's £7,250 makes M cheaper by £2,250 per year on expected cost alone. Options B and C both arise from forgetting to add N's extra running cost or M's incident exposure to the comparison. In real decision-making, remember that expected value is a starting point, not the whole story: a public body may rationally pay above expected value to reduce the chance of a catastrophic, trust-damaging incident, because impact on citizens and on public confidence is not captured by remediation cost alone. Identifying and addressing architectural risks — business, data, or security — means knowing both the arithmetic and its limits, and being able to say explicitly which considerations sit outside the numbers.

**Question 13 (easy) — Unit conversion in an SLA**

A partner's service level agreement promises a maximum response time of 800 milliseconds. Your end-to-end budget for the whole transaction is 2.5 seconds, and your own processing consumes 1.9 seconds. Can the partner call fit within your budget?

- A) Yes, with 200 ms to spare
- B) No, it exceeds the budget by 200 ms
- C) Yes, exactly on budget
- D) Cannot be determined

**Correct answer: B**

**Explanation:** Available budget for the partner call = 2.5 s − 1.9 s = 0.6 s = 600 ms. The partner may take up to 800 ms, which exceeds the 600 ms available by 200 ms. The conversion trap is comparing 800 ms against 2.5 s directly and concluding there is ample room. Latency budgets are additive along the call chain, and keeping all figures in one unit before comparing is the discipline. This is the arithmetic behind adapting a technical design during delivery: when a dependency's measured performance breaks the budget, the design, the budget, or the dependency has to change.

**Question 14 (moderate) — Weighted scoring of options**

Your options appraisal scores three candidate technologies against weighted criteria. Scores are out of 10; weights sum to 100%.

| Criterion (weight) | Tech J | Tech K | Tech L |
|---|---|---|---|
| Fit with existing skills (30%) | 8 | 5 | 6 |
| Running cost (40%) | 6 | 9 | 7 |
| Community and support maturity (30%) | 7 | 6 | 9 |

Which technology has the highest weighted score?

- A) Tech J
- B) Tech K
- C) Tech L
- D) J and L tie

**Correct answer: C**

**Explanation:** Tech J: (8 × 0.3) + (6 × 0.4) + (7 × 0.3) = 2.4 + 2.4 + 2.1 = 6.9. Tech K: (5 × 0.3) + (9 × 0.4) + (6 × 0.3) = 1.5 + 3.6 + 1.8 = 6.9. Tech L: (6 × 0.3) + (7 × 0.4) + (9 × 0.3) = 1.8 + 2.8 + 2.7 = 7.3. Tech L wins at 7.3, with J and K tied behind on 6.9 — a nice illustration that the highest single score (K's 9 on running cost) does not decide a weighted comparison. Weighted scoring models appear constantly in options papers; being able to compute, check, and — importantly — explain sensitivity ("K wins if the running-cost weight rises above 47%") strengthens both your decisions and your stakeholder conversations.

**Question 15 (hard) — Throughput against a fixed deadline**

A document-processing pipeline receives a batch of 72,000 documents at 06:00 each day. Processing must finish by 12:00 to meet a downstream statutory deadline. Each processing node handles 40 documents per minute, and for resilience reasons nodes can only be added in pairs. The current design has 4 nodes. Does the current design meet the deadline, and if not, what is the minimum compliant node count?

- A) Yes; 4 nodes finish with 90 minutes to spare
- B) No; 6 nodes are the minimum that meets the deadline
- C) No; 8 nodes are the minimum that meets the deadline
- D) Yes; 4 nodes finish exactly at 12:00

**Correct answer: B**

**Explanation:** The processing window is 06:00 to 12:00 = 360 minutes. Four nodes process 4 × 40 = 160 documents per minute, so the batch takes 72,000 ÷ 160 = 450 minutes — 90 minutes past the deadline, so the current design fails. Now find the minimum: the required rate is 72,000 ÷ 360 = 200 documents per minute, which needs 200 ÷ 40 = 5 nodes. But nodes are added in pairs from the current 4, so 5 is not an available configuration; the next compliant count is 6. Check: 6 × 40 = 240 documents per minute, 72,000 ÷ 240 = 300 minutes, finishing at 11:00 with an hour to spare. Notice the two-step structure: the pure arithmetic answer (5 nodes) is not the design answer (6 nodes) because a real constraint — pairing for resilience — rules the arithmetic optimum out. Capacity questions in assessments, as in designs, reward candidates who apply the stated constraints after the calculation, not just the calculation itself.

**Question 16 (moderate) — Phased migration percentages**

A migration roadmap moves 240 services to the strategic platform in three phases. Phase 1 moves 25% of the services; Phase 2 moves 40% of the remainder; Phase 3 moves everything left. How many services move in each phase?

- A) 60, 96, 84
- B) 60, 72, 108
- C) 80, 96, 64
- D) 60, 84, 96

**Correct answer: B**

**Explanation:** Phase 1: 25% × 240 = 60 services, leaving 180. Phase 2: 40% of the remainder = 40% × 180 = 72 services, leaving 108. Phase 3: the remaining 108. Check: 60 + 72 + 108 = 240. The trap is option A, which applies Phase 2's 40% to the original 240 (giving 96) rather than to the remainder — the phrase "of the remainder" changes the base, exactly as qualifying phrases change the base in real roadmap documents. Supporting the implementation of a strategy by using a roadmap or plan means being able to turn phase percentages into concrete counts that teams can resource, and to spot when someone else's plan has quietly mixed its bases.

### Preparation tips

- **Rebuild fluency with percentages, ratios, and rates.** Almost every question reduces to one of these three. Practise until "percentage change against the original value", "parts of a ratio", and "quantity per unit" are automatic, so your thinking time goes on interpretation.
- **Practise reading tables before calculating.** Give yourself ten seconds per table to note units, scale qualifiers ("in thousands"), time periods, and row/column meanings before touching the numbers. Most wrong answers are extraction errors, not calculation errors.
- **Use estimation to sanity-check.** Before computing 4,200 ÷ 840,000, estimate: 4,200 out of 840,000 is about 5 in 1,000, so around 0.5%. If your precise answer lands far from your estimate, one of them contains a slip.
- **Work with your own numbers.** Pull up a real hosting bill, a capacity dashboard, or a licensing quote from your programme and interrogate it: cost per transaction, growth rate, headroom, break-even. Practice on familiar material transfers directly.
- **Manage the clock deliberately.** With roughly a minute per question, a three-minute question is three questions lost. Answer, flag, or skip within your budget, and return to flagged questions at the end.

### Common pitfalls

- **Misreading chart and table labels.** Confusing monthly with annual data, or missing "in thousands", flips an answer completely — as in Question 5, where the requests column is in thousands and the errors column is not.
- **Using the wrong base for a percentage.** Percentage change is measured against the starting value; headroom against demand or capacity gives different figures. State your base, in tests and in design documents alike.
- **Over-calculating.** When options are far apart, estimation and rounding find the answer faster than long division. Precision is only worth its time cost when the options are close together.
- **Anchoring on one figure in a multi-part cost.** Setup cost, running cost, and support cost must all enter a total-cost comparison, as in Question 3. Partial comparisons produce confident wrong answers.
- **Time-sink questions.** Multi-stage problems like break-even analysis reward a clear method; without one, they consume minutes. If the path is not visible quickly, flag and move on rather than grinding.


## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment evaluates how well you understand, analyse, and draw correct conclusions from written business information. It mirrors the exact reading demands of your role: dense passages built from the kinds of documents a technical architect reads daily — technology standards, governance policies, design review minutes, supplier correspondence, and service assessments.

Typical format and timing: you are given a passage and a series of statements, and for each statement you must answer **True** (the passage supports it), **False** (the passage contradicts it), or **Cannot Say** (the passage provides insufficient information either way). Some questions are multiple-choice comprehension instead. Two rules define the format: you must answer based strictly on the text provided, ignoring outside knowledge, and you are under time pressure — usually less than a minute per question.

Why does this matter for a technical architect? Words are your working material as much as systems are. A misread sentence in a security standard becomes a non-compliant design; a governance condition skimmed too quickly becomes a blocked release; an ambiguous requirement accepted without challenge becomes six weeks of rework. Your role asks you to listen to the needs of technical and business stakeholders, to engage with architectural governance and assurance, and to challenge requirements and assumptions — every one of those begins with reading precisely what a document actually says, as distinct from what you expected it to say.

### What it measures for your role

- **Architecture communication** — comprehension questions reflect your duty to listen to the needs of technical and business stakeholders and to achieve agreement with technical and non-technical stakeholders; you cannot represent a position accurately if you have not extracted it accurately.
- **Making architectural decisions** — True/False/Cannot Say discipline mirrors your duty to engage with architectural governance and assurance: governance documents are binding on their exact wording, and the gap between "must", "should", and "may" is where compliance lives.
- **Strategy design** — inference questions reflect your duty to challenge requirements and assumptions; spotting what a strategy document implies, assumes, or carefully avoids saying is a core reading skill.
- **Architect for the whole context** — passages drawn from roadmaps and multi-team plans reflect your duty to identify how other teams contribute to delivering outcomes through change.
- **Technical design throughout the life cycle** — detail questions reflect the precision needed when a design document's exact words will guide delivery teams for months.

### Practice questions

For each passage, answer the statements strictly from the text. Resist your professional knowledge: the test measures what the passage supports, not what is true in the world.

**Passage 1 — Technology standard extract**

"All new services must use the department's approved API gateway for external integrations. Services with existing point-to-point integrations may continue to operate them until their next major upgrade, at which point they must migrate to the gateway. Exemptions may be granted by the architecture review board where migration cost is demonstrated to exceed £100,000, and any exemption must be reviewed annually. The gateway supports REST and event-based integration styles; SOAP-based integration is not supported and no exemption route exists for it."

**Question 1 (easy):** True, False, or Cannot Say: A new service may use a point-to-point integration for an external connection if it is cheaper than the gateway.

**Correct answer: False**

**Explanation:** The first sentence is unconditional for new services: "All new services must use the department's approved API gateway for external integrations." The continuation allowance applies only to "existing point-to-point integrations", and the cost-based exemption route relates to migration cost for those existing integrations. Nothing in the passage offers a cost-based route for a new service to avoid the gateway. The statement contradicts the passage, so it is False, not Cannot Say.

**Question 2 (moderate):** True, False, or Cannot Say: A service with an existing point-to-point integration that has never had a major upgrade may still be operating that integration.

**Correct answer: True**

**Explanation:** The passage says existing point-to-point integrations "may continue to operate them until their next major upgrade". If the trigger — a major upgrade — has not occurred, the permission to continue still stands. The passage directly supports the possibility. Notice the reasoning is conditional: the test rewards tracing the exact trigger conditions in a policy, precisely as you would when advising a team whether a standard bites on their situation.

**Question 3 (moderate):** True, False, or Cannot Say: The architecture review board has granted at least one exemption.

**Correct answer: Cannot Say**

**Explanation:** The passage says exemptions "may be granted" and sets the conditions, but it never states that any exemption has actually been granted. Asserting that one has been granted goes beyond the text; asserting that none has would equally go beyond it. This is the signature Cannot Say pattern: a rule's existence tells you nothing about its usage. In governance discussions, keeping "what the policy permits" separate from "what has actually happened" is exactly this discipline.

**Question 4 (moderate):** True, False, or Cannot Say: A service whose only feasible integration style is SOAP could obtain an exemption if migration costs exceed £100,000.

**Correct answer: False**

**Explanation:** The final sentence is explicit: "SOAP-based integration is not supported and no exemption route exists for it." The £100,000 exemption applies to migration cost for point-to-point integrations, not to unsupported integration styles. The statement contradicts the passage's direct wording. In a timed test, candidates who remember the exemption clause but not its scope pick True — a reminder to check which rule a condition belongs to before applying it.

**Passage 2 — Design review minutes**

"The review board considered the proposed case-management design. The board noted that the design reuses the department's document-storage component and commended this. Concerns were raised that the proposed database technology, while well understood by the current team, is approaching end of vendor support in 2028. The board approved the design on condition that a supported database version is adopted before public beta, and asked the team to return with a revised data model addressing the duplication of citizen records between the case and correspondence stores. The board did not consider security aspects, which are reserved for the separate security assurance process."

**Question 5 (easy):** True, False, or Cannot Say: The board rejected the design.

**Correct answer: False**

**Explanation:** The passage states "The board approved the design on condition that...". Conditional approval is still approval; the design was not rejected. Candidates sometimes read a list of concerns and conditions as a rejection, but the operative verb in the passage is "approved". Reading the decision separately from the commentary around it is a skill you use every time you relay a governance outcome to a delivery team accurately.

**Question 6 (moderate):** True, False, or Cannot Say: The design will pass the security assurance process.

**Correct answer: Cannot Say**

**Explanation:** The passage explicitly says the board "did not consider security aspects" and that these are reserved for a separate process. The passage therefore offers no evidence in either direction about the security outcome. Neither the approval nor the commendation transfers to a process that has not happened in the text. Boundary-spotting of exactly this kind matters when you communicate outcomes: "approved by the review board" and "fully assured" are different claims, and conflating them misleads stakeholders.

**Question 7 (hard):** True, False, or Cannot Say: The board's database condition must be satisfied before the service enters public beta.

**Correct answer: True**

**Explanation:** The condition reads "a supported database version is adopted before public beta". The statement paraphrases this precisely: the adoption must precede public beta. Nothing is added or dropped. Hard True questions often look suspiciously easy, which tempts candidates into hunting for a hidden trap and answering Cannot Say. The discipline is symmetrical: do not add meaning, and do not withhold agreement when the text plainly supports the statement.

**Question 8 (moderate) — multiple choice:** Which of the following best summarises the board's view of the component reuse in the design?

- A) The board required the reuse to be removed.
- B) The board viewed the reuse positively.
- C) The board expressed no opinion on reuse.
- D) The board conditioned approval on further reuse.

**Correct answer: B**

**Explanation:** The passage says the board "noted that the design reuses the department's document-storage component and commended this". Commending is explicit positive judgement, so B is directly supported. Option D is a subtle distractor: the board attached conditions, but about the database and the data model, not about reuse. Attaching the right condition to the right subject — who required what, about which part of the design — is exactly the precision that minutes and assessment questions both demand.

**Passage 3 — Email from a service owner**

"Thanks for the options paper. I can see the event-driven approach is more scalable, but I'm worried about the timeline. Our statutory deadline is 1 April and we cannot move it. If the event-driven design adds more than four weeks to delivery, we'd rather take the simpler design now and revisit scalability next year, provided that doesn't lock us in. I should also say the minister's office has taken an interest in this service, so we may be asked for extra reporting at short notice. Can you confirm which option keeps our choices open?"

**Question 9 (moderate):** True, False, or Cannot Say: The service owner prefers the simpler design.

**Correct answer: Cannot Say**

**Explanation:** The preference expressed is conditional: the simpler design is preferred only "if the event-driven design adds more than four weeks to delivery", and even then only "provided that doesn't lock us in". The passage does not say whether the four-week condition holds, so no unconditional preference can be extracted. Reading stakeholder emails for their exact conditional structure — rather than compressing them into "they want the simple option" — is central to listening to the needs of business stakeholders and representing them faithfully in design discussions.

**Question 10 (easy):** True, False, or Cannot Say: The statutory deadline can be moved if the event-driven design requires it.

**Correct answer: False**

**Explanation:** The email states plainly: "Our statutory deadline is 1 April and we cannot move it." The statement directly contradicts this. Note that your outside knowledge — deadlines do sometimes move in real programmes — is irrelevant; the test, like a written stakeholder position, binds you to what was actually said.

**Question 11 (hard):** True, False, or Cannot Say: The service owner has asked the architect to recommend the event-driven design.

**Correct answer: False**

**Explanation:** The concluding request is: "Can you confirm which option keeps our choices open?" That is a request for an assessment of optionality, not a request to recommend the event-driven design. Candidates often mark this Cannot Say, reasoning that the owner's intent is unclear — but the statement claims a specific request was made, and the passage records a different request, which makes the claim contradict the text as written. When a question asserts that someone asked for X and the text shows they asked for Y, the answer is False.

**Passage 4 — Extract from a departmental architecture strategy**

"Over the next three years the department will consolidate its eleven case-management systems onto no more than three strategic platforms. Consolidation decisions will be led by business capability mapping rather than by technology age alone. Teams should prefer configuration over customisation on strategic platforms; customisation requires a documented decision recording the ongoing cost of ownership it creates. The strategy does not mandate a single supplier, and the department will maintain at least two strategic platforms from different suppliers to preserve commercial leverage. Progress will be reviewed every six months by the design authority."

**Question 12 (moderate):** True, False, or Cannot Say: Under the strategy, the department could end up with exactly two case-management platforms.

**Correct answer: True**

**Explanation:** The target is "no more than three strategic platforms", and the department "will maintain at least two strategic platforms from different suppliers". Two satisfies both bounds — at least two, no more than three — so the outcome is permitted by the text. The skill here is combining two separated numerical constraints into the range they jointly define, exactly as you would when reconciling a strategy document's targets before building a roadmap that supports its implementation.

**Question 13 (moderate):** True, False, or Cannot Say: Customisation on a strategic platform is prohibited.

**Correct answer: False**

**Explanation:** The strategy says teams "should prefer configuration over customisation" and that "customisation requires a documented decision". A practice that requires documentation is regulated, not prohibited; the passage's own wording presupposes customisation can happen. This is the must/should/may discrimination that governance reading turns on: "prefer" plus a documentation requirement is a controlled allowance, and translating it as a ban misstates the policy — in the test and in a design review alike.

**Question 14 (hard):** True, False, or Cannot Say: The design authority can change the three-platform target at its six-monthly reviews.

**Correct answer: Cannot Say**

**Explanation:** The passage says progress "will be reviewed every six months by the design authority", but it says nothing about the review's powers: whether it can amend targets, or only monitor progress against them, is not stated. Assuming a governance body can change what it reviews imports outside knowledge of how such bodies often work. The passage neither supports nor contradicts the statement, so Cannot Say. Distinguishing "what a body does" from "what it is empowered to decide" is a distinction you rely on whenever you engage with architectural governance and assurance.

**Question 15 (moderate) — multiple choice:** According to the passage, what must accompany a decision to customise a strategic platform?

- A) Approval from the design authority
- B) A documented decision recording the ongoing cost of ownership created
- C) A six-month review period
- D) Agreement from at least two suppliers

**Correct answer: B**

**Explanation:** The passage states customisation "requires a documented decision recording the ongoing cost of ownership it creates" — option B nearly verbatim. Options A, C, and D each recombine real elements of the passage (the design authority, six-monthly reviews, two suppliers) with the wrong subject. Recombination distractors are the most common trap in verbal tests precisely because every ingredient looks familiar; the defence is to point back to the exact sentence that answers the question, which is also the habit that makes your own citations of standards and strategies trustworthy.

**Passage 5 — Supplier statement on a shared component**

"The identity verification component will be provided as a managed service. The supplier guarantees 99.9% monthly availability, excluding scheduled maintenance windows, which will be announced at least ten working days in advance and will take place outside the hours of 07:00 to 19:00 on working days. The supplier will remediate critical vulnerabilities within 48 hours of disclosure. Where a consuming service requires data residency within the United Kingdom, this can be accommodated at additional cost. The supplier's roadmap includes support for delegated authority relationships, expected in the next major release, although this feature has not yet entered development."

**Question 16 (easy):** True, False, or Cannot Say: Scheduled maintenance could take place at 08:00 on a Saturday.

**Correct answer: True**

**Explanation:** The exclusion window is "outside the hours of 07:00 to 19:00 on working days". A Saturday is not a working day, so the 07:00–19:00 restriction does not apply, and 08:00 on a Saturday is permitted by the stated rule. Many candidates answer False by reading "outside 07:00 to 19:00" as an absolute daily rule and missing the qualifier "on working days". Qualifiers that scope a rule — to certain days, services, or classifications — are where careful readers earn their marks, in tests and in supplier contracts alike.

**Question 17 (moderate):** True, False, or Cannot Say: UK data residency is included in the standard service.

**Correct answer: False**

**Explanation:** The passage says UK data residency "can be accommodated at additional cost". Something available only at additional cost is by definition not included in the standard offering, so the statement contradicts the text. This is precisely the sort of clause that matters when you assess a shared component for reuse across teams: a capability being available is not the same as it being included, and the difference lands in someone's budget.

**Question 18 (hard):** True, False, or Cannot Say: Support for delegated authority relationships will be delivered in the next major release.

**Correct answer: Cannot Say**

**Explanation:** The roadmap "includes" the feature and it is "expected in the next major release", but the passage also notes it "has not yet entered development". An expectation about an undeveloped feature is not a commitment that it will be delivered; equally, the passage does not say it will not be. The statement asserts a definite future outcome that the text presents only as expected, so the passage neither supports nor contradicts it — Cannot Say. Tracking emerging technologies and supplier roadmaps to assess opportunities and risks depends on exactly this discrimination between a roadmap promise, an expectation, and a delivered capability.

**Passage 6 — Service assessment report extract**

"The service met the majority of the Service Standard points assessed. The panel found strong evidence of user research informing the design of the application journey. However, the panel was not assured that the technology choices support iteration: the case-routing rules are embedded in supplier-configured workflow, meaning rule changes currently require a supplier change request with a typical turnaround of four weeks. The panel recommends that rule logic be moved to a department-controlled configuration layer before the next assessment. The team indicated that this work is feasible within two sprints, although the technical architect noted it depends on an API the supplier has committed to deliver next quarter. The service may proceed to public beta; the recommendation will be reviewed at the live assessment."

**Question 19 (easy):** True, False, or Cannot Say: The service failed the assessment.

**Correct answer: False**

**Explanation:** The passage says the service "met the majority of the Service Standard points assessed" and, decisively, "may proceed to public beta". A report can carry criticism and a recommendation while still permitting progression; the outcome sentence, not the tone of the findings, states the result. This mirrors Question 5's lesson at a different altitude: separate the decision from the commentary, in assessments and in assessment reports alike.

**Question 20 (moderate):** True, False, or Cannot Say: Moving the rule logic to a department-controlled configuration layer can be completed within two sprints.

**Correct answer: Cannot Say**

**Explanation:** The team "indicated that this work is feasible within two sprints", but the architect "noted it depends on an API the supplier has committed to deliver next quarter". A feasibility claim with an unresolved external dependency is not a supported statement that the work can be completed in two sprints — but neither does the passage contradict it, since the API may arrive as committed. The honest reading is that the outcome is contingent on facts the passage does not settle. Reporting a team estimate together with its dependency, rather than either one alone, is exactly the balanced communication your role requires.

**Question 21 (moderate):** True, False, or Cannot Say: Under the current arrangement, changing a case-routing rule takes about four weeks.

**Correct answer: True**

**Explanation:** The passage states that "rule changes currently require a supplier change request with a typical turnaround of four weeks". The statement paraphrases this directly, with "about" fairly rendering "typical". The word "currently" matters: the statement is about the present arrangement, which the passage describes explicitly. Had the statement claimed rule changes "will always" take four weeks, the recommended configuration layer would have made it Cannot Say — one modal word separates the two answers, which is the entire discipline of this test in miniature.

**Question 22 (moderate) — multiple choice:** According to the passage, when will the panel's recommendation be reviewed?

- A) Before the service enters public beta
- B) When the supplier delivers the committed API
- C) At the live assessment
- D) Two sprints after the report

**Correct answer: C**

**Explanation:** The final sentence states: "the recommendation will be reviewed at the live assessment." Options A, B, and D each borrow a genuine time reference from elsewhere in the passage — beta progression, the supplier's API quarter, the two-sprint estimate — and attach it to the wrong event. This is the recombination pattern from Question 15 again, and the same defence applies: find the sentence whose subject is actually the review, and answer from that sentence alone. In your working life this is the difference between telling a team "governance will check this before beta" and the accurate "governance will check this at live" — a difference of months in their planning.

### Preparation tips

- **Train the True/False/Cannot Say reflex.** For each statement ask two questions in order: does the passage support this? If not, does the passage contradict it? Only if both answers are no is it Cannot Say. Practising this two-step keeps you from drifting into general-knowledge judgements.
- **Read the statement before re-reading the passage.** Skim the passage once for structure, then let each statement send you back to the specific sentence that decides it. Hunting with a target is much faster than repeated full readings within the tight time limit.
- **Mark the modal verbs.** "Must", "should", "may", "can", "will" carry the legal weight in policy text. In practice runs, underline them; in the test, notice them deliberately. Most False answers hinge on a modal or a qualifier like "only", "unless", or "at least".
- **Practise on real governance text.** The Technology Code of Practice, the Service Standard, and your department's architecture principles are ideal material: pick a paragraph and write three statements — one True, one False, one Cannot Say — then defend each from the wording. This builds the exact skill and deepens your professional reading at the same time.
- **Keep calm about "obvious" answers.** Some statements really are plainly True. Overthinking every question into Cannot Say costs marks just as surely as careless assumption does. Trust the text when it speaks clearly.

### Common pitfalls

- **Making assumptions from professional knowledge.** You know how API gateways, review boards, and suppliers usually behave. The test — like a contract — binds you to the words on the page. If the passage does not say it, you cannot use it.
- **Confusing "likely" with "stated".** A passage saying a risk "may materialise" does not support a statement that it "will". Treating a possibility as a fact is the single most common verbal reasoning error, and the same slip in a design document overstates your evidence.
- **Recombining passage elements.** Distractors weld a real detail to the wrong subject — the right condition on the wrong rule, the right body with the wrong power. Always trace which sentence governs the statement before answering.
- **Spending too long reading the whole text first.** With under a minute per question, scan for structure, then search for the keywords in each statement. Deep reading of every clause up front is a time sink.
- **Letting the scenario's stakes sway your reading.** A passage about ministers or statutory deadlines feels urgent, but urgency does not change what the text says. Answer the reading question, not the situational one — the situational judgement section is next.


## Workplace job-specific situational judgement assessment

### About this assessment

A workplace job-specific situational judgement assessment evaluates your decision-making, interpersonal skill, and professional conduct. Unlike logic or numeric tests, it presents realistic workplace dilemmas and asks how you would respond, to see how well your behavioural choices align with the role's demands and your organisation's values. There is usually no single objectively right answer in the mathematical sense — several responses may seem reasonable — but some responses fit the role and the culture demonstrably better than others.

Typical format and timing: each question gives a short scenario — a conflict, an ethical dilemma, or an operational challenge — followed by several possible actions. You are asked either to select the **most effective** and **least effective** actions, or to rank or rate all the options from best to worst. These assessments are usually untimed or generously timed, because they measure natural judgement rather than speed.

Why does this matter for a technical architect? Look at how much of your role profile is about people. You look for opportunities to collaborate, communicating with both technical and non-technical stakeholders. You contribute to the work of others, motivate and empower teams, create the right environment for teams to work in, and recognise and deal with issues. You provide support in discussions about architectural topics within a multidisciplinary team, and you work with others to make architectural design decisions. Almost none of that is solitary technical work; it is judgement exercised among colleagues, stakeholders, and governance bodies, often under delivery pressure. In a UK public sector context, that judgement is also expected to reflect the values your profession works by: putting user needs first, working in the open with transparency, collaborating across teams and disciplines, and building services that are accessible and inclusive.

### What it measures for your role

- **Community collaboration** — scenarios about team conflict, credit, empowerment, and team makeup map to your duties to motivate and empower teams, create the right environment for teams to work in, identify the best team makeup depending on the situation, and recognise and deal with issues.
- **Architecture communication** — scenarios about disagreement, jargon, and stakeholder alignment map to your duties to listen to the needs of technical and business stakeholders and to achieve agreement using different architecture representations.
- **Making architectural decisions** — scenarios about risk, escalation, and governance map to your duties to make decisions with managed levels of risk and to engage with architectural governance and assurance.
- **Architect for the whole context** — scenarios about cross-team dependencies map to your duty to align your work with other architects and technical professionals and to identify how other teams contribute to delivering outcomes.
- **Strategy design and Technical design throughout the life cycle** — scenarios about challenging requirements and adapting designs during delivery map to your duties to challenge requirements and assumptions and to adapt a technical design if needed during delivery.

### Practice questions

For each scenario, decide your answer before reading the discussion. The explanations matter more than the "score": they show the reasoning a strong technical architect applies.

**Question 1 (moderate) — The team building around your design**

A delivery team has started building from your technical design. Two sprints in, the tech lead tells you they have hit a problem: the message queue you specified cannot guarantee the ordering the case-workflow needs, and they have quietly begun building a workaround that adds significant complexity. Choose the MOST and LEAST effective responses.

- A) Thank the tech lead for raising it, review the ordering requirement together, and adapt the design openly — updating the design record so other teams learn from the change.
- B) Insist the team implement the design as written, since it was approved at review and changing it now would undermine governance.
- C) Let the workaround continue since the team is closest to the problem, and note it for the next design review in a month.
- D) Take over the implementation of the messaging layer yourself to make sure it is done properly.

**Most effective: A. Least effective: B.**

**Explanation:** Your role explicitly includes adapting a technical design if needed during delivery — a design that meets governance but not the workflow's real ordering requirement is a design with an unmanaged risk. Option A treats the tech lead's disclosure as the valuable signal it is, fixes the design at the design level, and works in the open so the change benefits others: collaboration, transparency, and reuse in one move. Option B is least effective because it weaponises governance against reality; the team will either build something that fails or keep hiding workarounds, and both outcomes damage trust and the service. Option C abdicates the architectural decision, letting complexity accrete silently for a month. Option D solves today's problem while disempowering the team — the opposite of motivate and empower — and makes you a single point of failure.

**Question 2 (moderate) — Non-technical stakeholder pressure**

A senior operational manager, frustrated after a slow procurement, tells you in a programme meeting: "Just tell us which product to buy. All this options analysis is architecture for its own sake." The room looks at you. Choose the MOST and LEAST effective responses.

- A) Give a firm product recommendation on the spot to show responsiveness.
- B) Acknowledge the frustration, explain in plain terms what specific risk the remaining analysis retires — for example lock-in or data migration cost — and offer a firm decision date the manager can plan around.
- C) Explain that architectural governance requires the full options framework and the timescale cannot change.
- D) Suggest the manager raise the concern with your head of profession if they are unhappy with the method.

**Most effective: B. Least effective: D.**

**Explanation:** Option B does the two things your communication skill demands at once: it listens to the needs of a business stakeholder — the real need is predictability, not a product name — and it translates architectural work into a consequence the stakeholder cares about, converting "analysis" from apparent obstruction into visible risk management, with a date as the concrete commitment. Option A buys momentary approval by gambling the decision quality the analysis exists to protect. Option C answers a relationship problem with a process citation, hearing the words but not the need. Option D is least effective: deflecting a frustrated stakeholder up the hierarchy in a public meeting abandons the conversation your role exists to hold, and signals that challenge is unwelcome rather than valued.

**Question 3 (hard) — Discovering a security risk near a deadline**

Reviewing an integration two weeks before a heavily publicised go-live, you find that a partner data feed is authenticated but not encrypted in transit, contrary to your department's security standard. The delivery manager says: "Raising this now will delay launch. Nobody outside would ever know. Can we log it as a post-launch improvement?" Choose the MOST and LEAST effective responses.

- A) Agree to log it post-launch, since the data is only moderately sensitive and the deadline is high-profile.
- B) Report the issue immediately through the security assurance route, and simultaneously work with the team on the fastest compliant fix — assessing whether encryption can be enabled without slipping the date.
- C) Refuse to discuss timescales until the issue is fixed, and state that launch cannot happen.
- D) Quietly fix it yourself in the integration configuration without telling anyone, avoiding both delay and alarm.

**Most effective: B. Least effective: A.**

**Explanation:** Identifying and addressing architectural risks — explicitly including security — and engaging with governance and assurance are duties of your role, and option B honours both while staying delivery-minded: escalate honestly and attack the fix in parallel, because a standards breach in transit encryption is often quick to remediate. Option A is least effective: it makes concealment of a known standards violation a planning decision, on the reasoning "nobody would know" — the inverse of public sector transparency, and a personal acceptance of a risk that belongs with the accountable assurance route. Option C is directionally principled but needlessly adversarial; it removes your expertise from the solution just when it is most useful. Option D fixes the technology and breaks the system: undocumented changes near go-live create their own risks, and hiding both problem and fix denies the organisation the chance to learn how the gap arose.

**Question 4 (moderate) — Two architects, two patterns**

You discover that another architect in a neighbouring programme has specified a different integration pattern for connecting to the same national system your teams use, duplicating effort and creating two things to maintain. You believe your pattern is stronger. Choose the MOST and LEAST effective responses.

- A) Continue with your pattern; their programme is not your responsibility.
- B) Email their programme director recommending your pattern be adopted across both programmes.
- C) Contact the architect directly, compare the two patterns openly against both programmes' needs, and agree either a common pattern or documented reasons for divergence — sharing the outcome with the wider architecture community.
- D) Raise the duplication at the architecture review board without speaking to the architect first.

**Most effective: C. Least effective: A.**

**Explanation:** Aligning your work with the work being done by other architects and technical professionals is the first behaviour listed under architect for the whole context, and option C enacts it: peer-to-peer, evidence-based, open to the possibility that their pattern wins or that both are justified, and finishing with community-level sharing so the reuse opportunity is not lost. Option A is least effective because it knowingly leaves duplication and divergence in place — the precise failure your whole-context skill exists to prevent. Option B skips the peer conversation and converts a technical comparison into a political escalation, presupposing your pattern's superiority. Option D uses governance as a first resort where collaboration was available; boards are for decisions that peers cannot resolve, and arriving without having tried looks like manoeuvring, not assurance.

**Question 5 (moderate) — A struggling team member**

A developer on a team you support has been assigned the implementation of a complex caching design you produced. They are visibly struggling, sprint velocity is dropping, and other team members are quietly working around them. The team's delivery manager has not noticed yet. Choose the MOST and LEAST effective responses.

- A) Pair with the developer on the design's trickiest parts, check whether the design itself is harder than it needs to be, and give the delivery manager a quiet, factual heads-up so support can be arranged.
- B) Ask the delivery manager to reassign the work to a stronger developer before the sprint fails.
- C) Say nothing; team performance is the delivery manager's job, not the architect's.
- D) Rework the design yourself into something simpler and hand it back without comment.

**Most effective: A. Least effective: C.**

**Explanation:** Your community collaboration skill asks you to contribute to the work of others, motivate and empower teams, and recognise and deal with issues — option A does all three, and adds the architect's distinctive move: asking whether the design's complexity, not the developer's ability, is the real issue. Creating the right environment includes making your own artefacts humane to implement. Option C is least effective because "not my job" leaves a person sinking, a team compensating in silence, and a design possibly at fault — recognising and dealing with issues is in your profile precisely so this is your job. Option B may eventually be right, but as a first move it solves the sprint by labelling a person, without diagnosis. Option D fixes the artefact while communicating nothing; wordlessly replacing someone's work teaches no one anything and can humiliate.

**Question 6 (hard) — Ranking: the accessibility late-add**

Three weeks before a public beta assessment, a user researcher reports that the document viewer in the design fails with screen readers. The component came from a supplier library you specified. The delivery manager proposes shipping and fixing it "in a later iteration". Rank ALL FOUR responses from most to least effective.

- A) Support shipping as planned; accessibility can be iterated like any other feature.
- B) Treat it as a blocking defect: work with the researcher to define the failing cases, identify whether a fix, configuration change, or alternative component can land before beta, and make the risk visible to the service owner either way.
- C) Replace the supplier library immediately with an in-house viewer the team would build from scratch.
- D) Ask the supplier for their accessibility conformance evidence and a fix timeline, and feed that into the decision.

**Most effective ranking: B, D, C, A.**

**Explanation:** Accessibility is not an optional feature in UK government services; it is a legal and Service Standard obligation, and screen-reader failure excludes real users from a public service. B leads because it treats the issue with the seriousness it carries while staying solution-focused and transparent to the accountable owner. D is a strong supporting move — the component is the supplier's, and their evidence and timeline materially change the options — but on its own it waits where B acts. C at least takes the problem seriously, but a from-scratch rebuild three weeks before beta swaps a known defect for an unknown quantity of new risk, ignoring the managed-complexity discipline of your decision-making skill. A is least effective: "iterate accessibility later" ships a service that excludes users at launch, and inclusion deferred is inclusion denied for everyone affected in the meantime.

**Question 7 (moderate) — Credit in front of the board**

At a programme board, a senior stakeholder praises "the architect's elegant integration design" for a recent success. In fact, the key idea came from a mid-level engineer on the delivery team during a whiteboard session you facilitated. Choose the MOST and LEAST effective responses.

- A) Accept the praise gracefully; correcting the record would be awkward and the team knows the truth.
- B) Briefly credit the engineer by name, note that the design emerged from the team session, and offer to have the engineer present the approach to a future board or community of practice.
- C) Say nothing at the board but privately thank the engineer afterwards.
- D) Interrupt to give a detailed history of exactly who contributed which idea.

**Most effective: B. Least effective: A.**

**Explanation:** Option B costs one sentence and pays in every currency your role trades in: the engineer feels seen (motivate and empower teams), the board learns that good design comes from collaborative sessions the architect creates (create the right environment for teams), and offering a presentation slot converts credit into a development opportunity. Option A is least effective because absorbing a team member's credit in a senior forum — even passively — corrodes exactly the trust your facilitation depends on; and the team does know the truth, which is precisely the problem. Option C preserves your comfort, not the engineer's visibility; private thanks do not undo public misattribution. Option D over-corrects into a tangent the board does not need; precision about credit does not require a full genealogy of the whiteboard.

**Question 8 (hard) — The strategy you disagree with**

Your department publishes a technology strategy naming a specific vendor platform as strategic for all new case-management work. Your analysis for a current project suggests the platform fits poorly: its licensing model triples cost at your project's scale, a fact the strategy's authors did not examine. Your project starts build in six weeks. Choose the MOST and LEAST effective responses.

- A) Follow the strategy; it is published, and consistency across the department matters more than one project's costs.
- B) Design around the strategy quietly, choosing a different platform and hoping the divergence is not noticed until it is too late to reverse.
- C) Document the cost analysis, take it to the strategy's owners and your architectural governance route as a challenge with evidence, and ask for either an exemption or a strategy revision — while preparing a compliant fallback design in parallel.
- D) Escalate to your project's senior responsible owner that the strategy is wrong and ask them to overrule it.

**Most effective: C. Least effective: B.**

**Explanation:** Your strategy design skill explicitly includes challenging requirements and assumptions and identifying opportunities to develop strategy — a strategy is a living instrument, and evidence that its assumptions fail at your scale is a contribution, not a rebellion. Option C challenges through the front door with evidence, respects governance, and manages delivery risk with a parallel fallback: exactly what making architectural decisions with managed levels of risk looks like when the risk is strategic. Option B is least effective because covert divergence breaks trust in both directions — the strategy owners lose the feedback that would improve the strategy, and your project carries an unapproved position that may be unwound at maximum cost. Option A treats consistency as an absolute, spending public money on known-poor fit without even testing whether the strategy's owners would grant an exemption. Option D reaches for hierarchy before governance; the SRO may become involved, but starting there bypasses the process designed to weigh precisely this kind of evidence.

**Question 9 (moderate) — The meeting that excludes its audience**

You are supporting a discussion between your delivery team and a policy team about a new eligibility-checking service. Ten minutes in, the technical discussion is deep into API schemas and event topologies; the policy colleagues have gone silent and one is checking email. A decision that needs their input is scheduled for the end of the meeting. Choose the MOST and LEAST effective responses.

- A) Let the technical discussion run; the policy team can raise questions at the end if anything is unclear.
- B) Pause the discussion, restate the decision in service terms — what citizens would experience and what the policy constraints are — and use a simple diagram or example case to bring both groups into the same conversation before returning to technical detail.
- C) Suggest the policy team leave and be consulted by email afterwards, since the current material is technical.
- D) Ask the tech lead to slow down and define each acronym as they go.

**Most effective: B. Least effective: C.**

**Explanation:** Creating and using different architecture representations to communicate effectively with technical and non-technical stakeholders is the heart of your communication skill, and option B is that skill in action: changing the representation — from schemas to a citizen journey and an example case — is what re-admits the people whose input the decision needs. Option C is least effective: it converts a communication failure into a structural exclusion, and a decision needing policy input taken without live policy engagement is a decision with an unmanaged business risk. Option A leaves disengaged stakeholders to re-enter unaided at the moment of maximum consequence. Option D treats vocabulary as the problem when representation is; slower jargon is still jargon, and the meeting's clock is finite.

**Question 10 (hard) — Reuse versus the deadline**

A team you support needs an address-lookup capability. A cross-government component exists, but its onboarding process takes six weeks and the team's deadline is five. Building a quick local integration would take one week, but adds another duplicate to the landscape and carries its own assurance burden. Rank ALL FOUR responses from most to least effective.

- A) Start the cross-government onboarding immediately, and in parallel ask the component's owners whether the timeline can compress and your programme whether the deadline has any flexibility, deciding at the last responsible moment.
- B) Build the local integration now and plan a migration to the shared component in a named later phase, recording the decision and the duplication openly.
- C) Build the local integration now and leave the shared component for some future team to consider.
- D) Miss the deadline in order to onboard to the shared component, informing the programme afterwards.

**Most effective ranking: A, B, C, D.**

**Explanation:** A leads because it refuses the false binary: five-versus-six weeks is close enough that either number may move, and the last responsible moment is the disciplined point to decide — this is looking for opportunities to reuse components while managing delivery risk rather than sacrificing either. B is a legitimate second: sometimes the numbers will not move, and a documented, scheduled, transparent tactical build is an honest managed-risk decision — the openness and the named migration phase are what make it defensible. C contains the same build as B but without the honesty or the plan; undocumented tactical solutions are how landscapes fill with duplicates, and the gap between B and C is precisely the record and the commitment. D is least effective: unilaterally missing a deadline and informing the programme afterwards takes a decision that belongs to the programme — the trade-off between time and reuse is a business decision you inform, not one you impose.

**Question 11 (moderate) — The heated design review**

In a design review you are facilitating, a discussion between two senior developers about database technology turns personal: one dismisses the other's proposal as "the kind of thing you'd expect from someone who's never run production". The room goes quiet. Choose the MOST and LEAST effective responses.

- A) Move to the next agenda item to defuse the tension.
- B) Intervene immediately: name the standard ("we critique designs, not people"), restate the technical disagreement neutrally as a pair of trade-offs, and invite evidence on both — then follow up privately with the individual afterwards.
- C) Let it pass in the meeting but report the developer to their line manager afterwards.
- D) Side with whichever proposal you independently consider stronger, ending the argument with an architectural ruling.

**Most effective: B. Least effective: A.**

**Explanation:** Creating the right environment for teams to work in is not an abstract duty; it is made or lost in moments like this. Option B protects the person, preserves the technical disagreement — which is valuable and must survive the intervention — and models the norm publicly so the whole room learns it, with the private follow-up handling the individual dimension proportionately. Option A is least effective: moving on tells everyone present that personal attacks carry no cost in your reviews, taxing every future contribution from anyone less senior or less confident — psychological safety, once visibly unenforced, is expensive to rebuild. Option C outsources to hierarchy what the moment needed from facilitation, and does nothing for the person attacked in front of the room. Option D resolves the technology question while ratifying the behaviour; even the "winner" learns that contempt works.

**Question 12 (moderate) — The pattern request you cannot yet answer**

A delivery team asks you to recommend a pattern for offline-capable mobile working — an area where you have limited direct experience. Their planning session is on Friday. Choose the MOST and LEAST effective responses.

- A) Recommend the pattern used in a case study you once read, presented confidently so the team can proceed.
- B) Tell the team offline patterns are out of scope for architecture and they should decide themselves.
- C) Be candid about the limits of your current knowledge, spend the available days consulting the architecture community and published government patterns, and bring the team a reasoned starting position on Friday with its uncertainties labelled.
- D) Ask for the planning session to be postponed a month so you can research thoroughly.

**Most effective: C. Least effective: A.**

**Explanation:** Option C combines intellectual honesty with usefulness on the team's timeline: consulting the community is your community collaboration skill working in the other direction — contributing to and drawing from the work of others — and a starting position with labelled uncertainties is genuinely more useful to a planning session than false confidence or nothing. Option A is least effective because confident authority attached to unvalidated knowledge is the most damaging thing an architect can supply; teams build on your certainty, and a wrong pattern presented as settled can misdirect months of work. Option B abandons a team that asked for exactly the support your role exists to provide. Option D values your thoroughness over their momentum; a month's delay for a starting recommendation inverts the proportionality of managed risk.

### Preparation tips

- **Anchor on the role's behaviours, not generic management advice.** Before a situational judgement test, re-read your role profile. The strongest options almost always express a listed behaviour: empowering rather than replacing, adapting designs openly, challenging through governance, communicating in the stakeholder's terms.
- **Look for the option that is both principled and delivery-minded.** Public sector scenarios reward responses that hold the standard and help the team meet it. Options that are principled but obstructive, or helpful but silent about risk, usually rank second and third.
- **Check who owns the decision.** Many scenarios hinge on whether a choice is yours to make alone. Options where you quietly absorb a decision that belongs to a team, an owner, or a governance route — even competently — usually rank low.
- **Rehearse with colleagues.** Talk through dilemmas like these with other architects or your community of practice. Hearing where experienced peers diverge sharpens your sense of which considerations dominate, and it doubles as genuine professional development.
- **Answer as your best working self.** Do not try to guess an idealised persona; assessors calibrate against effective real-world behaviour. The candidate who would raise the risk, credit the engineer, and still care about the deadline is the candidate they are looking for.

### Common pitfalls

- **Answering idealistically rather than effectively.** "Stop everything until it is perfect" sounds virtuous but ignores practical delivery; the strongest options manage both the standard and the timeline, as in the security and accessibility scenarios above.
- **Selecting passive options.** Choices that delay action, hand the problem to someone else, or wait for the next scheduled meeting consistently rank poorly. Architects are consulted because they engage; deferral is rarely the effective move.
- **Ignoring the values context.** UK public sector scenarios reward transparency, user focus, accessibility, inclusion, and collaboration. An option that is commercially astute but conceals a risk, or efficient but excludes users or colleagues, will rank below one that is open and inclusive.
- **Over-escalating or under-escalating.** Going straight to a director, a board, or a line manager before trying the direct conversation ranks low; so does keeping to yourself a risk that belongs with assurance. Match the response to the smallest forum that can genuinely resolve the issue.
- **Solving the technology and ignoring the people.** Several scenarios contain a technically correct action that damages trust — the silent fix, the wordless redesign, the architectural ruling that ends a fight. If an option repairs the system but not the relationship, keep looking.


## Conclusion

Well done for working through this guide. You have covered a lot of ground: cognitive exercises built from the dependency maps, design rules, and fault diagnoses of real architectural work; numeric reasoning across hosting costs, capacity plans, availability budgets, and options appraisals; verbal reasoning against the standards, minutes, emails, and strategies that shape your decisions; and situational judgement across the team, stakeholder, and governance dilemmas that fill an architect's week.

If one theme runs through all four sections, it is this: the assessments are not testing something separate from your job — they are your job, distilled. Structured analysis, careful reading, honest arithmetic, and principled judgement among people are exactly what it means to undertake structured analysis of technical issues, to communicate with technical and non-technical stakeholders, to make architectural decisions with managed risk, and to create the right environment for teams. Every practice question you worked through was also a small rehearsal of the role itself.

What next? Treat your results as a map, not a verdict. If the numeric section felt slow, spend time each week with a real cost table or capacity dashboard until the arithmetic is automatic. If Cannot Say questions caught you out, practise on genuine policy text — precision will repay you in every governance conversation. If a situational scenario made you pause, take it to your architecture community of practice and hear how peers would act; those conversations are professional development of the best kind. Revisit this guide after a few weeks and notice what has become easier — improvement in these skills is real, measurable, and well within your control.

Approach any formal assessment rested, unhurried, and confident that the abilities being measured are ones you exercise every working day. You design systems for a living; trust yourself to reason clearly about a few dozen questions. Good luck — and keep building, keep challenging, and keep collaborating.

