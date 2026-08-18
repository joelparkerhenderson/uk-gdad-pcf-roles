# Chief Technology Officer - Psychometric Assessment Resources

## Introduction

Welcome. This document is written for you: a Chief Technology Officer working within the UK Government Digital and Data profession. As the organisation's technology strategist, you make decisions about technical direction, work closely with other senior leaders, and carry accountability for strategy, architecture, resilience, innovation, risk, capability, and delivery. Psychometric assessments at your level are not about catching you out on trivia; they are structured ways of examining how you think, how you reason with evidence, and how you exercise judgement under the kinds of pressure that come with executive responsibility.

Psychometric assessments are standardised exercises that measure mental capabilities and behavioural tendencies. In senior public sector recruitment and development, they are commonly used alongside interviews, staff engagement exercises, and portfolio reviews because they add an objective, comparable signal about how a candidate processes information and makes decisions. For a Chief Technology Officer, that signal matters a great deal: your decisions about technology strategy, architecture investment, and risk appetite shape services that citizens depend on, budgets that run into the millions, and the working lives of large multidisciplinary teams.

This document is organised into four main assessment sections, each of which mirrors a type of assessment you may encounter:

1. **Workplace job-specific cognitive assessment** — how you recognise patterns, deduce conclusions, check for errors, and prioritise using the artefacts a CTO genuinely handles: strategy papers, architecture decisions, risk registers, and delivery plans.
2. **Workplace job-specific numeric reasoning assessment** — how you interpret budgets, capacity figures, availability metrics, and total cost of ownership comparisons, and how you use them to make sound financial decisions for technology.
3. **Workplace job-specific verbal reasoning assessment** — how precisely you read dense material such as spend control policies, security advisories, supplier correspondence, and board papers, and how carefully you distinguish what a text actually says from what you might assume.
4. **Workplace job-specific situational judgement assessment** — how you respond to realistic executive dilemmas involving ministers, boards, suppliers, security incidents, and your own leadership team, judged against UK public sector values such as user needs, transparency, collaboration, accessibility, and inclusion.

Each section explains what the assessment measures, maps it to the capabilities your role demands, provides substantial practice questions with full worked explanations, and closes with preparation tips and common pitfalls.

How should you use this document? Three ways. First, as practice: attempt each question honestly before reading the explanation. Second, as self-reflection: notice which question styles feel effortless and which feel effortful, because that tells you something useful about your own habits of thought. Third, as preparation: if you are facing an assessed selection process — for example, for a permanent secretary-sponsored digital leadership post — this material will make the formats familiar so that on the day your attention goes to the content, not the mechanics.

Take your time, enjoy the challenge, and treat every explanation as a small coaching conversation. Let's begin.

## Advisory

"This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff."

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive ability assessment measures the mental processes that predict performance in a particular role, using scenarios and data drawn from that role rather than abstract puzzles. Unlike a generic IQ test, every stimulus is something you might plausibly encounter at your desk: a dependency map for a migration programme, a risk register with an inconsistency buried in it, a set of architecture principles that do not quite hold together, or four urgent demands competing for the same afternoon.

For a Chief Technology Officer, the cognitive assessment typically examines pattern recognition (spotting trends and anomalies in operational and delivery data), logical deduction (drawing valid conclusions from policies, dependencies, and constraints), error checking (finding the flaw in a board paper before the board does), prioritisation (ordering competing demands defensibly), and structured problem solving (decomposing a messy strategic situation into decidable parts).

The typical format is online and timed, usually 15 to 30 minutes, with objective scoring against a norm group of comparable senior professionals. Some platforms adapt question difficulty to your answers. Employers usually receive a breakdown of speed versus accuracy rather than a single number, so working carefully and steadily is a legitimate strategy — you are not obliged to race.

Why does this matter for your role? Because a CTO's cognitive errors are expensive. A misread dependency delays a national service. An unchecked figure in a business case misleads a spending review. A poorly ordered set of priorities burns your best engineers on the wrong problem. The assessment is a compressed, low-stakes rehearsal of exactly those moments.

### What it measures for your role

Your role summary lists six named skills, and the cognitive assessment touches every one of them:

- **Strategic technology planning** — logical deduction and prioritisation questions test whether you can hold a multi-year strategy in mind and reason about sequencing, dependencies, and trade-offs, exactly as you must when you create a technology strategy and vision aligned with the organisation's broader strategy.
- **Technology architecture** — pattern and consistency questions use architecture principles, dependency maps, and infrastructure diagrams, reflecting your duty to put in place a technology architecture that provides reliable and permanent infrastructure.
- **Technology evaluation** — matrix-reasoning and rule-application questions mirror the structured evaluation you perform when you assess the organisation's range of technologies and decide which technologies it needs.
- **Innovation in digital, data and technology** — problem-solving items test whether you can reason about novel situations where precedent is thin, which is the cognitive core of enabling the organisation to adopt new technologies that offer value.
- **Financial decision making for technology** — error-checking items frequently use financial artefacts, because a CTO must catch arithmetic and logical flaws in investment cases before endorsing them.
- **Capability building for digital, data and technology** — prioritisation scenarios include people and skills constraints, reflecting your duty to ensure people have the tools, technical skills, and working environment they need.

The assessment also reflects your operational duties: ensuring systems are continuously operational and resistant to attacks and disasters, working within appropriate levels of risk, and creating working practices that support effective delivery.

### Practice questions

Work through these honestly before reading each explanation. Difficulty labels are a guide, not a guarantee — senior candidates often find the "easy" items the most instructive, because they reveal habits of skim-reading.

**Question 1 (easy) — Prioritisation.**
It is 14:00 on a Tuesday. Four items land on you at once:

- A: Your service desk reports that the citizen-facing payments service is degraded, with error rates climbing from 2% to 9% over the last hour.
- B: A minister's private office asks for a briefing note on your cloud strategy by Friday.
- C: A supplier account director requests an "urgent" meeting about contract renewal, which expires in five months.
- D: Your head of security wants ten minutes today to discuss a vulnerability scan result rated "medium" affecting an internal HR tool.

Which do you address first, and which last?

**Answer: First A; last C.**

**Explanation:** A is a live degradation of a citizen-facing service — it threatens your duty to keep systems continuously operational, it is worsening, and executive attention (even if only to confirm incident command is functioning) is warranted immediately. D is same-day but bounded: a medium-rated internal vulnerability deserves its ten minutes today, after A is in hand. B has a Friday deadline; it is important but schedulable. C is the only item with neither citizen impact nor a near deadline: five months before expiry, a supplier's "urgent" is commercial choreography, not your emergency. The trap is letting the word "minister" in B or "urgent" in C override a structured reading of impact and time-criticality.

**Question 2 (easy) — Pattern recognition.**
Your monthly count of priority-1 incidents across the estate reads: January 4, February 6, March 5, April 7, May 6, June 8, July 7. If the pattern continues, what is the most likely August figure?

**Answer: 9.**

**Explanation:** The sequence alternates +2 then −1: 4→6 (+2), 6→5 (−1), 5→7 (+2), 7→6 (−1), 6→8 (+2), 8→7 (−1). The next step is +2, giving 9. Notice the executive-level point hiding in the arithmetic: despite the sawtooth, the underlying trend rises by one incident per two-month cycle. A CTO who reports "July is down on June" without noticing the trend line has read the noise and missed the signal.

**Question 3 (moderate) — Logical deduction from dependencies.**
Your migration programme has five workstreams. The rules are: Identity must complete before Payments starts. Payments and Case Management can run in parallel, but both need Hosting complete first. Reporting cannot start until Case Management completes. Hosting starts immediately. Which of the following must be true?

- A: Reporting is the last workstream to finish.
- B: Identity can run in parallel with Hosting.
- C: Payments cannot start until Identity and Hosting are both complete.
- D: Case Management must finish before Payments finishes.

**Answer: B and C are both deducible; C is the strongest single answer if only one is allowed.**

**Explanation:** Nothing in the rules makes Identity depend on Hosting, so Identity can indeed run alongside Hosting (B holds). Payments has two stated prerequisites — Identity complete, Hosting complete — so C follows directly. A is not forced: Reporting must follow Case Management, but if Case Management finishes early and Payments runs long, Payments could finish last, so A is only possible, not necessary. D has no support at all — the rules never sequence Case Management relative to Payments' finish. The discipline being tested is one you use whenever you challenge a delivery plan: distinguishing what a dependency map *requires* from what a Gantt chart *happens to show*.

**Question 4 (moderate) — Error checking.**
A board paper you are about to endorse states: "Our estate comprises 240 applications. 25% are cloud-hosted (60 applications), 55% remain on-premises (132 applications), and the remainder, 20% (52 applications), are hosted by third parties." Identify the error.

**Answer: The third-party figure is wrong: 20% of 240 is 48, not 52.**

**Explanation:** Check each claim: 25% of 240 = 60 (correct); 55% of 240 = 132 (correct); percentages 25 + 55 + 20 = 100 (consistent); but 20% of 240 = 48. Alternatively, 240 − 60 − 132 = 48. The paper's counts total 244, four applications more than the stated estate. This is precisely the class of error that erodes a board's confidence in a technology function: not strategic misjudgement, but an unchecked reconciliation. In assessments, when a passage offers both percentages and absolute numbers, always cross-foot them — the inconsistency is usually planted there.

**Question 5 (moderate) — Sequencing under constraints.**
You must schedule four activities in a single change window: (1) apply the database patch, (2) take the pre-change backup, (3) run the smoke tests, (4) switch traffic back to the primary site. The rules: the backup must precede the patch; smoke tests must follow the patch; traffic must return only after smoke tests pass. A colleague proposes: patch, backup, smoke tests, traffic switch. What is wrong, and what is the correct order?

**Answer: The proposal patches before backing up, so a failed patch would have no clean restore point. Correct order: backup, patch, smoke tests, traffic switch.**

**Explanation:** The stated rule "backup precedes patch" exists for a reason your resilience duty makes vivid: the backup is the rollback insurance for the patch. The colleague's order satisfies the other two rules but violates the first, and it is the violation with the worst failure mode — irreversibility. Assessment questions of this type reward you for checking every constraint mechanically rather than pattern-matching to "roughly the right shape". In real change advisory boards, the same mechanical check is what separates assurance from theatre.

**Question 6 (moderate) — Matrix reasoning for technology evaluation.**
You are evaluating three platforms against four criteria. A platform must meet ALL mandatory criteria and at least one desirable criterion to be shortlisted. Mandatory: (i) meets the National Cyber Security Centre cloud security principles; (ii) offers UK data residency. Desirable: (iii) open standards APIs; (iv) exit costs under £200,000.

- Platform X: meets i, ii, iv but not iii.
- Platform Y: meets i, iii, iv but not ii.
- Platform Z: meets i, ii but neither iii nor iv.

Which platforms are shortlisted?

**Answer: Only Platform X.**

**Explanation:** X meets both mandatory criteria and one desirable (iv) — shortlisted. Y fails mandatory criterion ii; no quantity of desirable strengths can rescue a mandatory failure, so Y is out regardless of its attractive API story. Z meets both mandatory criteria but zero desirables, failing the "at least one desirable" rule. The cognitive skill is applying a rule set exactly as written, resisting the halo effect of a platform that is impressive on the wrong dimensions. This mirrors your technology evaluation duty: procurement challenges collapse when evaluation criteria are applied elastically.

**Question 7 (challenging) — Deduction from assurance rules.**
Your assurance framework states: "Every service handling citizen data must have a current security review. Any service without a current security review must not receive new feature funding. Services in public beta always handle citizen data." Given these rules, which conclusion is valid?

- A: A service in public beta that lacks a current security review must not receive new feature funding.
- B: A service with a current security review handles citizen data.
- C: A service that receives new feature funding has a current security review.
- D: Both A and C.

**Answer: D — both A and C are valid.**

**Explanation:** A: public beta → handles citizen data (rule 3); lacking a review while handling citizen data breaches rule 1, and rule 2 independently blocks funding for any service without a current review — so A follows. C is the contrapositive of rule 2: "no review → no funding" is logically equivalent to "funding → review", so C is valid. B commits the converse error: rule 1 says citizen data → review, not review → citizen data; a purely internal tool could have a review too. Executives are routinely offered converse-error reasoning in papers ("we funded it, so it must have been assured") — this question trains the reflex to reject it.

**Question 8 (moderate) — Consistency checking across architecture principles.**
Your draft architecture principles include: (1) "Buy before build: prefer commodity products for common needs." (2) "All citizen-facing services must run on our shared hosting platform." (3) "Teams may choose any hosting arrangement that meets security baselines." (4) "Data is stored once and reused via APIs." Which pair of principles is in direct tension, and how would you resolve it?

**Answer: Principles 2 and 3 conflict — one mandates a single platform for citizen-facing services, the other grants free choice. Resolve by scoping: principle 3 should apply only to non-citizen-facing workloads, or principle 2 should be stated as the constraint that overrides principle 3.**

**Explanation:** Read each principle as a logical rule. Principle 2 is a universal obligation over citizen-facing services; principle 3 is a universal permission over all services, including citizen-facing ones. A team could invoke 3 to do what 2 forbids. Principles 1 and 4 are independent of the conflict — 1 concerns sourcing, 4 concerns data design. Neither contradicts hosting rules. The resolution technique — make the scope of each rule explicit and define precedence — is exactly how you, as the owner of technology architecture, prevent governance stalemates. Assessments plant these tensions to see whether you read principles as slogans or as rules with logical consequences.

**Question 9 (challenging) — Critical path reasoning.**
A data centre exit has these tasks and durations: Network links (6 weeks, no prerequisites); Landing zone build (4 weeks, needs Network links); Application remediation (10 weeks, no prerequisites); Migration waves (8 weeks, needs both Landing zone build and Application remediation); Decommissioning (3 weeks, needs Migration waves). What is the minimum total duration, and which single task should you accelerate to shorten the programme?

**Answer: 21 weeks; accelerate Application remediation.**

**Explanation:** Two paths lead into Migration waves. Path one: Network links (6) + Landing zone (4) = 10 weeks. Path two: Application remediation = 10 weeks. Both arrive at week 10 — the paths are tied. Then Migration waves (8) takes you to week 18, and Decommissioning (3) to week 21. Because the two feeding paths are tied at 10 weeks, accelerating either alone helps only until it drops below the other; strictly, you must accelerate both to gain schedule. But the question asks which *single task* to accelerate: within path one, acceleration must be split across two tasks, whereas Application remediation is a single 10-week task on its own path — yet shortening it alone leaves the 10-week network-plus-landing-zone path binding. The best defensible single answer is Application remediation *combined with the recognition that the benefit is capped* — and a strong candidate says exactly that. Assessments at executive level increasingly reward answers that state the limits of an intervention, because real programme boards need that honesty. If the options are only the five tasks, choose Application remediation and note the tie.

**Question 10 (moderate) — Rule application under spend controls.**
Your governance requires: technology spend above £100,000 needs CTO approval; above £1 million needs investment committee approval in addition; any spend on a service in public beta needs the service owner's sign-off regardless of amount. A team requests £850,000 for capacity upgrades to a service in public beta. Whose approvals are required?

**Answer: CTO approval and service owner sign-off; the investment committee is not required.**

**Explanation:** £850,000 exceeds £100,000, so CTO approval applies. It does not exceed £1 million, so the investment committee rule is not triggered — "above £1 million" is a strict threshold, and assessments frequently test whether you respect thresholds literally rather than rounding up out of caution. The public beta condition triggers the service owner's sign-off independently of the amount. Answering "all three, to be safe" is wrong in a rule-application question: adding approvals not required by the rules is a governance failure of a different kind — it slows delivery, which conflicts with your duty to create working practices that support effective delivery.

**Question 11 (challenging) — Pattern recognition in capacity data.**
Your platform team reports peak concurrent users at month end: March 12,000; April 13,200; May 14,520; June 15,972. Your infrastructure comfortably supports 21,000 concurrent users. In which month does peak demand first exceed capacity if the pattern continues?

**Answer: September.**

**Explanation:** Each month grows by 10%: 12,000 × 1.1 = 13,200; × 1.1 = 14,520; × 1.1 = 15,972. Continuing: July = 17,569 (15,972 × 1.1, rounded); August = 19,326; September = 21,259 — the first figure above 21,000. The reasoning skill is recognising multiplicative rather than additive growth: a candidate who reads the differences (+1,200, +1,320, +1,452) as "roughly +1,300 a month" projects August = 19,900 and September = 21,200 — and still lands on September, but with less confidence and more arithmetic. Recognising the generative rule (10% compound) is faster and more reliable, and it is the same recognition that tells a CTO when a capacity plan needs re-platforming rather than incremental hardware.

**Question 12 (challenging) — Deduction from policy statements.**
Three statements from your risk framework: "If a system is business-critical, it must have a tested disaster recovery plan. No system with an untested disaster recovery plan may be classed as resilient. The customer portal is classed as resilient." What can you validly conclude about the customer portal?

- A: It is business-critical.
- B: Its disaster recovery plan has been tested.
- C: It has a disaster recovery plan, and that plan has been tested.
- D: Nothing can be concluded.

**Answer: C.**

**Explanation:** Statement two, contraposed: if a system is classed as resilient, it does not have an untested disaster recovery plan. There are two ways to lack an untested plan: have a tested plan, or have no plan at all. Here is where careful reading pays: "a system with an untested disaster recovery plan" excludes systems with no plan — so strictly, the portal either has a tested plan or has no plan. Can we rule out "no plan"? Only if the portal is business-critical, which nothing states — so a pedantic logician might argue B and C overreach. However, in the answer set given, C is the intended and best-supported conclusion under the natural reading that "resilient" classification presupposes a recovery plan exists and statement two ensures it is tested. A is a converse error: business-criticality implies a tested plan requirement, not the reverse. This question deliberately sits at the boundary of formal logic and natural reading — assessment designers use such items sparingly, but senior candidates meet them, and the winning approach is to choose the best-supported option rather than hunting for a perfect one.

**Question 13 (moderate) — Problem decomposition.**
Staff survey results show engineers rate "tools and working environment" at 54% satisfaction, against a civil service technology benchmark of 71%. You have budget for exactly one intervention this quarter. Free-text comments cluster as: slow laptops (38% of comments), blocked access to modern developer tools (31%), noisy office (17%), outdated training (14%). Your asset register shows laptops were refreshed eight months ago to a high specification. What is the most logical first step?

**Answer: Investigate why high-specification laptops are performing slowly (for example, security agent configuration or virtual desktop constraints) before spending on any intervention.**

**Explanation:** The largest complaint cluster (slow laptops) contradicts a known fact (recent high-spec refresh). When your two most reliable data sources conflict, the logical move is to resolve the contradiction, because it changes which intervention is right: if endpoint security tooling is throttling machines, buying newer laptops (the surface reading) wastes the budget, while reconfiguring agents could fix the top complaint at minimal cost — freeing funds for the second cluster, tool access. This mirrors your capability-building duty: the felt experience of tooling is an evidence question before it is a spending question. Assessments reward candidates who notice contradictions between datasets rather than acting on the loudest number.

**Question 14 (challenging) — Fault diagnosis logic.**
Overnight, three alerts fired: the API gateway reported elevated latency from 02:10; the database cluster reported a failover at 02:05; the identity service reported no anomalies. Citizen-facing error rates rose at 02:12 and recovered at 02:40, when the gateway latency also normalised. The database failover completed successfully at 02:08 according to its logs. Which explanation best fits all the evidence?

- A: The identity service silently failed, causing gateway latency.
- B: The database failover caused a brief connection storm that the gateway absorbed as latency, which subsided as connection pools re-established.
- C: The gateway failed independently, coincidentally at the same time as the database failover.
- D: Citizen error rates caused the gateway latency.

**Answer: B.**

**Explanation:** Test each hypothesis against the timeline. A contradicts the evidence: the identity service reported no anomalies, and while silent failures happen, A explains neither why the trouble began three to five minutes after a documented database event nor why it resolved without any identity-side action. C requires a coincidence and ignores the natural causal chain from a 02:05 failover to 02:10 latency. D reverses cause and effect — error rates are a downstream symptom, and they rose *after* the latency began. B fits every data point: failover at 02:05, completion at 02:08, connection re-establishment producing gateway latency from 02:10, citizen impact from 02:12, and gradual recovery as pools stabilised by 02:40. The reasoning pattern — prefer the hypothesis that explains all the evidence with the fewest coincidences — is the core of executive incident review, where you must challenge teams whose preferred explanation conveniently exonerates their own component.

### Preparation tips

- **Rehearse with your own artefacts.** Take a real (suitably anonymised) board paper, risk register, or dependency map and interrogate it: what must be true, what cannot be true, what does not follow? Ten minutes a day of this converts your daily work into assessment practice.
- **Practise the contrapositive.** Many executive-level deduction items turn on "if no review, then no funding" being equivalent to "if funding, then review". Drill this until it is reflexive.
- **Cross-foot every table.** Whenever a stimulus gives both percentages and absolute numbers, verify they reconcile. Planted inconsistencies are the assessment designer's favourite trick, and reconciliation takes seconds.
- **Verbalise your prioritisation logic.** For ranking questions, articulate the criteria first (citizen impact, irreversibility, deadline proximity, escalation cost) and then apply them. A stated framework beats intuition under time pressure.
- **Manage the clock like an incident.** Allocate time per question at the start, and treat an overrun the way you would treat a breached service level: cut losses, flag it, move on, return if capacity allows.
- **Stay rested and unhurried.** At your level, the differentiator is rarely raw speed; it is composure. Take the assessment when you are fresh, in a quiet space, exactly as you would protect time for a major investment decision.

### Common pitfalls

- **Halo reasoning in evaluation items.** Letting a platform's strength on desirable criteria excuse a mandatory failure. Mandatory means mandatory — in the test and in procurement.
- **Converse errors.** Concluding "funded, therefore assured" from "assurance is required for funding". Board papers commit this error weekly; do not import it into the assessment.
- **Reading noise as signal.** Reacting to the latest data point in a sawtooth series instead of the trend. Always ask what rule generates the sequence.
- **Over-approving in rule-application questions.** Adding approvals or steps "to be safe" when the rules do not require them. Precision is the competency being measured.
- **Time-sink questions.** Spending five minutes on one challenging deduction while three easy items go unanswered. The score rewards coverage with accuracy, not heroics on a single item.
- **Skim-reading thresholds.** Confusing "above £1 million" with "£1 million and above", or monthly with annual figures. Executive fluency with documents can breed a skimming habit; the assessment punishes it.


## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment evaluates your ability to analyse, interpret, and make sound decisions using numerical data of the kind your role genuinely produces. It focuses on business mathematics — percentages, ratios, cost comparisons, capacity figures, and trend projections — rather than abstract formulae. The question inputs are tables, budget lines, performance dashboards, and project schedules, and most assessments allow or provide an on-screen calculator, because the skill being measured is interpretation and decision-making, not mental arithmetic.

For a Chief Technology Officer, this assessment is unusually close to the day job. You steward a technology budget that must survive spending reviews; you compare total cost of ownership between hosting models; you read availability percentages and capacity projections and decide when to invest; you evaluate supplier pricing structures; and you translate all of it into advice that other senior leaders — who may not check your arithmetic — will act on. A CTO who misreads "in thousands" as "in millions", or who compares a three-year cost against a five-year cost, does not merely lose marks: they misdirect public money.

Typical format: online, strictly timed (often 20 to 30 minutes for 15 to 20 questions), multiple choice, with data presented in tables and charts. Time pressure is deliberate — it simulates reading a finance paper minutes before the investment committee starts. Accuracy under that pressure, and the judgement to estimate when estimation suffices, are both being measured.

One further point on level. At executive grade, numeric items are rarely hard because the mathematics is advanced — it almost never goes beyond percentages, ratios, weighted averages, and compound growth. They are hard because the *setup* is realistic: figures arrive in mixed units and mixed periods, some lines are protected and some are not, and the question quietly depends on choosing the right base or the right horizon. In other words, the difficulty is judgement wrapped around arithmetic, which is exactly the proportion you meet in a real investment committee paper. Approach every question by first deciding what comparison is actually being asked for, and only then reaching for the calculator.

### What it measures for your role

Mapped to the skills named in your role summary:

- **Financial decision making for technology** — the heart of this assessment. Budget allocation questions, total cost of ownership comparisons, payback and return-on-investment calculations, and spend-control arithmetic all test the numeracy beneath sound technology investment decisions.
- **Technology evaluation** — weighted scoring models and price-structure comparisons test whether you can turn supplier claims into comparable numbers, supporting your duty to evaluate the organisation's range of technologies and which technologies it needs.
- **Strategic technology planning** — growth projections, capacity forecasts, and multi-year cost models test the quantitative core of a strategy that must remain affordable and deliverable over several years.
- **Technology architecture** — availability percentages, capacity utilisation, and resilience costs test the numbers behind a reliable and permanent infrastructure.
- **Innovation in digital, data and technology** — payback-period questions reflect the discipline of funding innovation that offers value, within appropriate levels of risk.
- **Capability building for digital, data and technology** — workforce arithmetic (contractor ratios, day rates, training investment per head) tests the numbers behind ensuring people have the tools and skills they need.

### Practice questions

An on-screen calculator is assumed. Every explanation shows the arithmetic — check your working against it, not just your final answer.

**Question 1 (easy) — Budget shares.**
Your technology budget for the financial year is £24 million, allocated as: staff 45%, infrastructure and hosting 30%, software licences 15%, innovation fund 10%. How much is allocated to software licences, and how much more is spent on staff than on infrastructure and hosting?

**Answer: Licences £3.6 million; staff exceeds infrastructure by £3.6 million.**

**Explanation:** Licences: 15% of £24m = 0.15 × 24 = £3.6m. Staff: 0.45 × 24 = £10.8m. Infrastructure: 0.30 × 24 = £7.2m. Difference: £10.8m − £7.2m = £3.6m. The two answers coinciding at £3.6m is deliberate — assessments sometimes reuse a number to check you computed each part rather than pattern-matching. Sense-check: the four shares (10.8 + 7.2 + 3.6 + 2.4) total £24m. Always confirm allocations sum to the whole.

**Question 2 (easy) — Availability arithmetic.**
Your hosting contract guarantees 99.9% availability, measured monthly. In a 30-day month, what is the maximum downtime, in minutes, before the supplier breaches the guarantee?

**Answer: 43.2 minutes.**

**Explanation:** A 30-day month contains 30 × 24 × 60 = 43,200 minutes. The permitted downtime is 0.1% of that: 43,200 × 0.001 = 43.2 minutes. This tiny calculation carries strategic weight: when a supplier proposes "three nines" for a critical citizen service, you should be able to say instantly that it permits about three-quarters of an hour of outage every month, and decide whether that sits within your organisation's appropriate level of risk. For comparison, 99.99% would permit only 4.32 minutes.

**Question 3 (moderate) — Total cost of ownership.**
You are comparing hosting options for a case management system over three years. Option A (remain on-premises): hardware refresh £1,200,000 up front, plus operations of £20,000 per month. Option B (cloud): one-off migration cost of £150,000, plus £45,000 per month. Which is cheaper over three years, and by how much?

**Answer: Option B (cloud) is cheaper by £150,000.**

**Explanation:** Three years = 36 months. Option A: £1,200,000 + (36 × £20,000) = £1,200,000 + £720,000 = £1,920,000. Option B: £150,000 + (36 × £45,000) = £150,000 + £1,620,000 = £1,770,000. Difference: £1,920,000 − £1,770,000 = £150,000. Note the structure: the cheaper option has higher recurring costs but avoids the capital outlay — extend the horizon to five years and Option A becomes cheaper (A: £2,400,000; B: £2,850,000). Assessments love this crossover, and so do supplier pitches: always ask over what period a "saving" is claimed.

**Question 4 (moderate) — Percentage change in performance.**
Last quarter your estate logged 48 priority-1 incidents; this quarter, 36. Meanwhile, transaction volumes rose from 5.0 million to 6.0 million. Calculate the percentage change in incidents, and in incidents per million transactions.

**Answer: Incidents fell 25%; incidents per million transactions fell 37.5%.**

**Explanation:** Incident change: (36 − 48) ÷ 48 = −12 ÷ 48 = −0.25, a 25% reduction. Rate last quarter: 48 ÷ 5.0 = 9.6 per million. Rate this quarter: 36 ÷ 6.0 = 6.0 per million. Change: (6.0 − 9.6) ÷ 9.6 = −0.375, a 37.5% reduction. The normalised figure is the truer measure of resilience improvement because it controls for rising demand — exactly the framing you would want in a board report on your duty to keep systems continuously operational. Assessments reward candidates who understand *why* two correct percentages tell different stories.

**Question 5 (moderate) — Workforce ratios.**
Your engineering workforce is 240 people: 180 civil servants and 60 contractors. Contractors cost an average of £650 per day and work 220 days per year. (a) What is the ratio of civil servants to contractors? (b) What is the annual contractor cost? (c) If you move to a 5:1 ratio at the same total headcount, how many contractor roles convert to civil service posts?

**Answer: (a) 3:1. (b) £8,580,000. (c) 20 roles.**

**Explanation:** (a) 180:60 simplifies by dividing both by 60 → 3:1. (b) 60 × £650 × 220 = 60 × £143,000 = £8,580,000. (c) At 5:1 with 240 total, the workforce divides into 6 parts (5 + 1): 240 ÷ 6 = 40 contractors, so contractors fall from 60 to 40 — 20 conversions. This is capability-building arithmetic: the £8.58m figure lets you weigh conversion against contractor spend, and the ratio target expresses a strategic workforce ambition as a number you can track quarterly.

**Question 6 (moderate) — Licence cost comparison.**
You need a collaboration product for 3,000 users. Product A costs £8.50 per user per month. Product B costs £90 per user per year plus a flat platform fee of £25,000 per year. Which is cheaper annually, and by how much?

**Answer: Product B, by £11,000 per year.**

**Explanation:** Product A: £8.50 × 12 = £102 per user per year; × 3,000 users = £306,000. Product B: £90 × 3,000 = £270,000 + £25,000 platform fee = £295,000. Difference: £306,000 − £295,000 = £11,000. The critical step is normalising to the same period — monthly per-user pricing versus annual per-user pricing plus a flat fee is a classic supplier structure precisely because it resists quick comparison. Note also the sensitivity: at 2,000 users, A costs £204,000 and B costs £205,000, so A wins. A strong candidate notices that the answer depends on user count and asks how confident the 3,000 figure is.

**Question 7 (challenging) — Compound growth in storage.**
Your data platform holds 200 terabytes and is growing at 20% per year. Storage costs £15 per terabyte per month. (a) What volume do you project after three years? (b) What will the monthly storage bill be then, to the nearest pound?

**Answer: (a) 345.6 TB. (b) £5,184.**

**Explanation:** Compound growth: 200 × 1.2 = 240 TB after year one; 240 × 1.2 = 288 TB after year two; 288 × 1.2 = 345.6 TB after year three. Equivalently, 200 × 1.2³ = 200 × 1.728 = 345.6. Monthly bill: 345.6 × £15 = £5,184. The common error is additive projection — 20% of 200 is 40, so "200 + 120 = 320 TB" — which understates the true figure by 25.6 TB and, at scale, understates budgets materially. Compounding is the single most valuable pattern in strategic technology planning: demand, data, and technical debt all compound, and plans that assume straight lines run out of headroom early.

**Question 8 (moderate) — Capacity and effort planning.**
A legacy application migration requires 540 person-days of engineering effort. Your migration team has 9 engineers, each providing 15 productive days per month once meetings, support duties, and leave are accounted for. However, 2 engineers are seconded to an incident review for the whole of month one. Can the migration complete within four months? Show the arithmetic.

**Answer: No — after four months, 510 of the 540 person-days are done; completion falls early in month five.**

**Explanation:** Month one: 7 engineers × 15 days = 105 person-days. Months two to four: 9 × 15 = 135 person-days each, so 3 × 135 = 405. Total after four months: 105 + 405 = 510, leaving 30 person-days outstanding — about a week of the full team's capacity, landing the finish in the first days of month five. Two executive lessons: first, productive capacity is 15 days per month, not 21 or 22 — assessments (and optimistic delivery plans) often smuggle in gross rather than net capacity; second, a small early loss (30 person-days in month one) translates directly into a late finish unless recovered deliberately. When a programme director tells you a slipped month can be "absorbed", this is the arithmetic to request.

**Question 9 (challenging) — Payback period on automation.**
Your operations team proposes an automation platform costing £480,000 to implement. It will save £20,000 per month in manual effort and allow you to cancel a monitoring contract worth £120,000 per year. (a) What is the total annual saving? (b) What is the payback period in months? (c) What is the three-year net benefit?

**Answer: (a) £360,000 per year. (b) 16 months. (c) £600,000.**

**Explanation:** (a) Effort saving: £20,000 × 12 = £240,000; plus the contract, £120,000; total £360,000 per year. (b) Monthly saving: £20,000 + (£120,000 ÷ 12 = £10,000) = £30,000. Payback: £480,000 ÷ £30,000 = 16 months. (c) Three-year savings: £360,000 × 3 = £1,080,000; minus the £480,000 investment = £600,000 net. A payback within two years usually clears public sector investment thresholds comfortably, but a strong answer also names the assumptions: the £20,000 monthly saving must be *cashable or redeployable* to be real, and the contract cancellation must be contractually possible at month zero. Assessment explanations rarely demand this nuance, but interviews that follow the assessment often do.

**Question 10 (moderate) — Weighted supplier scoring.**
Your evaluation weights four criteria: functional fit 40%, security 30%, cost 20%, support 10%. Scores out of 100: Vendor X — functional 70, security 80, cost 60, support 90. Vendor Y — functional 85, security 60, cost 70, support 60. Compute each weighted total. Who wins, and what should you check before announcing the result?

**Answer: X scores 73, Y scores 72 — X wins by one point, so check the scoring's sensitivity and any minimum security threshold before relying on the result.**

**Explanation:** X: (70 × 0.4) + (80 × 0.3) + (60 × 0.2) + (90 × 0.1) = 28 + 24 + 12 + 9 = 73. Y: (85 × 0.4) + (60 × 0.3) + (70 × 0.2) + (60 × 0.1) = 34 + 18 + 14 + 6 = 72. A one-point margin on a 100-point weighted scale is inside the noise of any scoring panel: shift the security weight from 30% to 25% (giving the 5% to functional fit) and Y wins 72.75 to 72.5. A CTO's numeric fluency includes knowing when a computed difference is *decision-grade* and when it demands a sensitivity check — and noticing that Y's security score of 60 might fail a minimum threshold regardless of the total. The arithmetic is the start of the evaluation, not its end.

**Question 11 (challenging) — Budget reduction with protected lines.**
The finance director asks you to model an 8% reduction on your £30 million technology budget. Two lines are contractually or strategically protected: the security operations centre (£5 million) and committed hosting contracts (£7 million). (a) What cash reduction is required? (b) What percentage cut must the unprotected budget absorb? (c) If staff costs are £12 million of the unprotected budget and you decide staff will absorb cuts only at half the rate of non-staff lines, what percentage cut applies to each?

**Answer: (a) £2.4 million. (b) 13.33%. (c) Staff 10%, non-staff 20%.**

**Explanation:** (a) 8% of £30m = £2.4m. (b) Protected lines total £5m + £7m = £12m, leaving £18m unprotected; £2.4m ÷ £18m = 0.1333 = 13.33%. (c) Let non-staff lines take rate r and staff take half that rate, r/2. The non-staff unprotected budget is £18m − £12m = £6m. The cut must satisfy: £12m × (r/2) + £6m × r = £2.4m, which simplifies to 6r + 6r = 12r = 2.4 (in millions), so r = 0.20. Check: staff £12m × 10% = £1.2m; non-staff £6m × 20% = £1.2m; total £2.4m as required. The trap in this question is applying the headline 8% to the unprotected lines — a rushed reading produces "staff 8%, non-staff 16%", which recovers only £1.92m and leaves you £480,000 short at the spending review. Protected lines concentrate pain on what remains: if your finance director protects 40% of your budget, an 8% headline is a 13.33% real cut, and your leadership team deserves to hear the real number.

**Question 12 (moderate) — Unit cost improvement.**
Before re-platforming, your payments service processed 2.1 million transactions per month at a platform cost of £315,000 per month. After re-platforming, it processes 2.4 million transactions at £252,000 per month. Calculate the cost per transaction before and after, and the percentage improvement.

**Answer: £0.15 before; £0.105 after; a 30% reduction in unit cost.**

**Explanation:** Before: £315,000 ÷ 2,100,000 = £0.15 per transaction. After: £252,000 ÷ 2,400,000 = £0.105. Improvement: (0.15 − 0.105) ÷ 0.15 = 0.045 ÷ 0.15 = 0.30 = 30%. Notice that total cost fell only 20% (£315k → £252k), while unit cost fell 30% because volume rose simultaneously. Unit cost is the honest efficiency metric for a scaling service, and it is the number that makes the innovation case: "we spent £X re-platforming and now every transaction costs 30% less" is the sentence that wins the next investment. Presenting only the 20% total saving undersells your own programme.

**Question 13 (challenging) — Expected value in the innovation fund.**
Your innovation fund can back exactly one proposal this quarter. Proposal One: a £250,000 pilot with an estimated 30% chance of unlocking £2,000,000 in annual savings (and zero saving if it fails). Proposal Two: a £250,000 rollout of a proven tool with a near-certain £400,000 annual saving. (a) What is the expected annual saving of each? (b) Which would you fund, and what beyond expected value should inform the choice?

**Answer: (a) Proposal One £600,000; Proposal Two £400,000. (b) Expected value favours One, but the decision legitimately depends on risk appetite, affordability of failure, and what each option teaches the organisation.**

**Explanation:** (a) One: 0.30 × £2,000,000 = £600,000 expected annual saving. Two: approximately 1.0 × £400,000 = £400,000. (b) On expected value alone, One is 50% better. But expected value is an average over many trials, and you are running one trial: with 70% probability, One returns nothing and you have spent £250,000 of public money on a failed pilot. Your duty to work within appropriate levels of risk cuts both ways — an organisation that only ever funds Proposal Two never innovates, while one that always chases the big multiple gambles recklessly. A defensible executive answer computes both figures correctly, states the risk trade-off explicitly, and considers portfolio context: if this is the fund's only bet, Two's certainty may dominate; if it is one of eight bets across the year, One's expected value logic strengthens. Assessments increasingly include one question like this to see whether candidates treat probability as information rather than decoration. A useful check on your own reasoning: multiply out the downside as well as the upside. Proposal One's downside is a 70% chance of losing £250,000 for nothing; Proposal Two's downside is the £200,000 of expected value forgone. Naming both numbers is what turns a preference into an argument you can defend at the committee table.

**Question 14 (moderate) — Valuing resilience investment.**
Without a disaster recovery capability, your flagship service expects two major outages per year, each costing an estimated £250,000 in recovery effort, lost productivity, and remediation. A disaster recovery arrangement costs £300,000 per year and would reduce the expectation to one outage every two years, with the cost per outage falling to £50,000 because failover contains the damage. (a) What is the expected annual outage cost with and without the investment? (b) What is the net annual benefit of investing?

**Answer: (a) £500,000 without; £25,000 with. (b) £175,000 net benefit per year.**

**Explanation:** (a) Without: 2 outages × £250,000 = £500,000 expected annual cost. With: 0.5 outages per year (one every two years) × £50,000 = £25,000. (b) The investment reduces expected outage cost by £500,000 − £25,000 = £475,000, at a cost of £300,000, so the net benefit is £475,000 − £300,000 = £175,000 per year. This is the arithmetic behind your duty to make systems resistant to attacks and disasters: resilience spending looks like pure cost until you price the risk it retires. A complete answer also notes what expected value hides — reputational harm and citizen detriment are not in the £250,000 figure, so the true case is stronger than the arithmetic alone suggests.

**Question 15 (easy) — Reading a delivery dashboard.**
Your quarterly dashboard shows a programme with 40 milestones: 22 delivered, 8 on track, 6 at risk, and the remainder overdue. (a) How many milestones are overdue? (b) What percentage of all milestones are either at risk or overdue? (c) If half the at-risk milestones slip to overdue next quarter and nothing else changes, what will the overdue percentage be?

**Answer: (a) 4. (b) 25%. (c) 17.5%.**

**Explanation:** (a) 40 − 22 − 8 − 6 = 4 overdue. (b) At risk plus overdue: 6 + 4 = 10; 10 ÷ 40 = 0.25 = 25%. (c) Half of 6 at-risk milestones is 3; overdue becomes 4 + 3 = 7; 7 ÷ 40 = 0.175 = 17.5%. The question is easy on purpose: dashboard arithmetic is where executives are most tempted to trust the RAG colours without checking the counts. A dashboard whose categories do not sum to the total, or whose percentages are computed on delivered milestones rather than all milestones, misleads a board in seconds — and you are the person the board relies on to have checked.

### Preparation tips

- **Normalise before you compare.** Train yourself to convert everything to the same period (per year), the same unit (per user, per transaction, per terabyte), and the same base (percentage of what?) before comparing. Most planted traps dissolve at this step.
- **Rebuild one real business case.** Take a technology investment case your organisation has actually approved and re-derive its numbers: the payback period, the percentage savings, the totals. This is the highest-fidelity practice available to you, and it occasionally finds real errors.
- **Practise the three core moves.** Percentage change ((new − old) ÷ old), compound growth (multiply repeatedly, never add), and weighted averages (multiply each score by its weight, then sum). These three account for the large majority of executive-level numeric items.
- **Estimate first, compute second.** Before calculating, guess the order of magnitude. If your computed answer is wildly off your estimate, one of them is wrong — and under time pressure, catching that beats speed.
- **Use the calculator deliberately.** Key in long figures once, carefully, rather than three times quickly. Transcription errors, not conceptual errors, cost senior candidates the most marks.
- **Say the units out loud.** Per month or per year; per user or per transaction; thousands or millions; percentage points or percent. Most wrong answers at senior level are unit errors wearing the costume of calculation errors, and naming the units before computing prevents nearly all of them.
- **Watch the clock, keep moving.** A multi-stage question you cannot crack in two and a half minutes should be skipped and revisited. Coverage with accuracy outscores perfection on a subset.

### Common pitfalls

- **Misreading scale qualifiers.** Confusing "£ thousands" with "£ millions", or monthly with annual figures. At CTO level the numbers are large enough that this error survives sense-checking unless you actively look for the qualifier.
- **Comparing unlike periods.** Setting a three-year cost against a five-year cost, or a monthly price against an annual one. Suppliers structure prices to invite exactly this mistake.
- **Additive thinking about compound growth.** Projecting 20% annual growth as a straight line. Three years of compounding is 72.8% growth, not 60% — the gap widens every year.
- **Percentage-of-the-wrong-base errors.** An 8% cut to a budget with protected lines is a much deeper cut to the unprotected remainder; a 50% increase followed by a 50% decrease is a net 25% loss. Always ask: percentage of what?
- **Over-calculating.** Computing to three decimal places when the options differ by 20%. Estimation and elimination are faster and equally correct.
- **Treating computed rankings as decisive.** A one-point weighted-score margin or a marginal cost difference is often within the noise of the inputs. The numerate move is to report the margin *and* its fragility.


## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment evaluates how well you understand, analyse, and draw correct conclusions from written material of the kind your role requires you to read — and, crucially, whether you can answer based strictly on what a text says rather than on what you already know or expect. The classic format presents a dense passage followed by statements you must judge **True** (the passage says or logically entails this), **False** (the passage contradicts this), or **Cannot Say** (the passage provides insufficient information either way). Multiple-choice comprehension questions — best summary, author's main point, correct application of a stated rule — round out the format. Timing is tight, often under a minute per question, simulating the pace at which senior papers actually arrive.

For a Chief Technology Officer, this is not an abstract skill. You read spend control policies whose thresholds decide what you can approve; supplier letters whose careful phrasing conceals commercial positioning; security advisories where the difference between "is being exploited" and "could be exploited" changes your evening plans; audit reports whose findings you must neither overstate nor understate to your board; and draft strategies where a single ambiguous sentence will be quoted back at you for three years. Reading precisely — and knowing exactly what a document does *not* say — is an executive survival skill, and the profession's habit of quoting documents back verbatim makes it more so.

Typical format: online and timed, commonly 15 to 25 minutes for 20 to 30 questions, with passages of one to two paragraphs each carrying two to four questions. Scoring is objective and normed against comparable senior professionals, and — as with the cognitive assessment — many platforms report accuracy and speed separately, so a careful, complete reading strategy is a legitimate route to a strong score.

The particular discipline of "Cannot Say" deserves emphasis at your level. Senior leaders carry enormous background knowledge, which is precisely what the assessment asks you to suspend. When a passage about a supplier's price rise says nothing about your contract's termination clause, the correct answer about termination is Cannot Say — even though you, in real life, would know your contract. The test rewards epistemic discipline: distinguishing what this document establishes from what you believe.

### What it measures for your role

Mapped to the skills named in your role summary:

- **Strategic technology planning** — comprehension questions on strategy and policy passages test whether you extract commitments, conditions, and exclusions accurately, the raw material of a technology strategy aligned to organisational objectives.
- **Technology evaluation** — supplier correspondence and product documentation passages test whether you can separate verifiable claims from marketing inference when you evaluate which technologies the organisation needs.
- **Financial decision making for technology** — spend policy and contract passages test precise reading of thresholds, conditions, and obligations before money moves.
- **Technology architecture** — standards and assurance passages test whether you apply written rules to specific systems exactly as drafted.
- **Innovation in digital, data and technology** — passages about emerging technology guidance test whether you can identify what is permitted, prohibited, or simply unaddressed — the space where innovation happens.
- **Capability building for digital, data and technology** — workforce policy passages test accurate extraction of rules that affect your people's tools, skills, and working environment.

### Practice questions

Answer each question using only the passage above it. Resist everything you know from outside the text.

**Passage A — Cloud policy extract.**
*"All new services must adopt public cloud hosting unless a documented exemption is approved by the Chief Technology Officer. Exemptions may be granted only where a service processes data classified above OFFICIAL, where latency requirements cannot be met from available cloud regions, or where total costs over five years demonstrably exceed on-premises alternatives. Exemptions must be reviewed every two years. Services granted an exemption before this policy's effective date retain it until their next scheduled review. This policy does not apply to services scheduled for decommissioning within twelve months."*

**Question 1 (easy) — True / False / Cannot Say.**
"A new service processing data classified above OFFICIAL is automatically exempt from public cloud hosting."

**Answer: False.**

**Explanation:** The passage says exemptions "may be granted only where" one of three conditions holds. Data classification above OFFICIAL is a necessary gateway to an exemption, not an automatic grant: the exemption still requires "a documented exemption... approved by the Chief Technology Officer". "May be granted" signals discretion; "automatically" contradicts it. Precision about permission-words (may, must, only, unless) is the entire game in policy passages.

**Question 2 (moderate) — True / False / Cannot Say.**
"A service that will be decommissioned in nine months may remain on-premises without a CTO-approved exemption."

**Answer: True.**

**Explanation:** The final sentence states the policy "does not apply to services scheduled for decommissioning within twelve months." Nine months is within twelve, so the policy — including its exemption machinery — does not bind that service, and no exemption is needed. Note the reasoning direction: the question is answerable purely from the scope clause. Candidates who skim past scope clauses and dive into the exemption conditions answer this one wrongly, in tests and in governance boards alike.

**Question 3 (moderate) — True / False / Cannot Say.**
"Exemptions granted after the policy's effective date must be reviewed every two years."

**Answer: True.**

**Explanation:** "Exemptions must be reviewed every two years" is stated without qualification, so it covers all exemptions under the policy. The sentence about pre-existing exemptions ("retain it until their next scheduled review") addresses continuity, not frequency, and does not carve post-effective-date exemptions out of the two-year rule. The distractor logic here is juxtaposition: placing a special-case sentence next to a general rule tempts readers to infer an exception that the text never draws.

**Question 4 (moderate) — Multiple choice.**
Which statement best captures the policy's overall effect?

- A: Public cloud is mandatory for all services without exception.
- B: Public cloud is the default for new services, with a controlled, reviewable exemption route and a scope exclusion for soon-to-close services.
- C: The CTO may exempt any service from cloud hosting at their discretion.
- D: On-premises hosting is prohibited once a service's exemption expires.

**Answer: B.**

**Explanation:** A overstates: exemptions and the decommissioning exclusion both exist. C overstates the discretion: the CTO may approve exemptions *only* within the three listed conditions. D goes beyond the text: the passage never states what happens when an exemption expires. B alone matches the passage's structure — default rule, bounded exemptions, periodic review, scope exclusion. "Best summary" questions reward the option that neither adds nor subtracts.

**Passage B — Supplier letter.**
*"Further to our review of the managed hosting agreement, we write to advise that from 1 April our unit prices will increase by 9%, reflecting energy and labour cost inflation. As a valued strategic customer, you are eligible for our Loyalty Adjustment, which caps your effective increase at 6% in exchange for a twenty-four-month term extension. Please note that our standard terms permit annual price revisions in line with our published rate card. We remain committed to supporting your transformation objectives and would welcome a meeting to discuss additional service tiers that many customers in your sector have found valuable."*

**Question 5 (easy) — True / False / Cannot Say.**
"The supplier is raising unit prices by 9% from 1 April."

**Answer: True.**

**Explanation:** Stated directly: "from 1 April our unit prices will increase by 9%". The only care needed is not to confuse the headline increase with the conditional 6% cap, which applies only if the customer accepts the term extension. First-line facts are often tested precisely because later, more interesting sentences overwrite them in the reader's memory.

**Question 6 (challenging) — True / False / Cannot Say.**
"Accepting the Loyalty Adjustment would save the customer 3% of current spend."

**Answer: Cannot Say.**

**Explanation:** The arithmetic is tempting: a 6% rise instead of a 9% rise looks like a saving of 3 percentage points, and if the customer's entire spend consisted of unit prices applied to an unchanged volume, the cash saving would indeed equal 3% of current spend (on £1,000,000, prices would rise to £1,060,000 rather than £1,090,000 — a £30,000 difference). But examine what the passage actually quantifies: *unit prices*, not total spend. Nothing in the letter establishes that future volumes will match current volumes, or that every charge in the agreement is a unit price subject to the increase — managed hosting agreements commonly include fixed fees, and the letter is silent. The statement quantifies spend; the passage quantifies unit prices; bridging that gap requires assumptions the text does not supply. The disciplined answer is therefore Cannot Say. This is the hardest habit in verbal reasoning for numerate executives: the more easily you can *compute* a plausible figure, the more alert you must be to whether the text actually licenses the computation.

**Question 7 (moderate) — True / False / Cannot Say.**
"The customer can terminate the agreement rather than accept the price increase."

**Answer: Cannot Say.**

**Explanation:** The letter mentions standard terms permitting annual price revisions, but says nothing about termination rights, break clauses, or the customer's options on refusal. In reality you would check the contract; in the assessment, the passage is your entire universe, and it is silent. This is the classic Cannot Say trap for senior leaders: your professional instinct supplies the missing clause, and the test measures whether you notice yourself doing it.

**Passage C — Security advisory.**
*"A critical vulnerability has been identified in a widely deployed application server component. Exploitation requires network access to the management interface, which is disabled by default in versions 4.2 and later. We are aware of active exploitation against internet-exposed management interfaces. Organisations running versions earlier than 4.2 should apply the vendor patch immediately; organisations on 4.2 or later should verify that the management interface remains disabled and apply the patch within their normal cycle. There is currently no evidence of exploitation where the management interface is not exposed to the internet."*

**Question 8 (moderate) — True / False / Cannot Say.**
"Systems running version 4.2 with the management interface disabled are not vulnerable."

**Answer: Cannot Say.**

**Explanation:** The advisory says the interface is "disabled by default" in 4.2+, that exploitation "requires network access to the management interface", and that there is "no evidence of exploitation" without internet exposure. Careful reading: exploitation requires network access to the interface — not necessarily *internet* access. An internal attacker with network reach might exploit an enabled interface; but the statement posits the interface is *disabled*, and exploitation requires access to it. Does a disabled interface make exploitation impossible? The advisory strongly implies risk is contained, and instructs patching "within their normal cycle" — language of reduced urgency, not of safety. It never states that disabled means invulnerable, and the vulnerability itself is in the component, not the interface configuration. "Not vulnerable" is a stronger claim than the text makes. Cannot Say. In security communications, the gap between "no evidence of exploitation" and "not exploitable" is exactly where executive misjudgement lives — advisories are drafted with that distinction deliberately, and this assessment style tests whether you honour it.

**Question 9 (easy) — True / False / Cannot Say.**
"Active exploitation has been observed against internet-exposed management interfaces."

**Answer: True.**

**Explanation:** Verbatim: "We are aware of active exploitation against internet-exposed management interfaces." The statement is a near-direct quotation. In a timed test, bank questions like this in seconds and spend the saved time on items like Question 8. Part of verbal reasoning skill is calibrating effort: recognising when a statement maps directly onto the text and when it requires inference.

**Question 10 (moderate) — Multiple choice.**
For an estate running version 4.1 with the management interface not exposed to the internet, what does the advisory direct?

- A: Apply the patch within the normal cycle, since there is no internet exposure.
- B: Apply the vendor patch immediately.
- C: Upgrade to version 4.2 rather than patching.
- D: Disable the management interface instead of patching.

**Answer: B.**

**Explanation:** The advisory's instruction is keyed to version, not to exposure: "organisations running versions earlier than 4.2 should apply the vendor patch immediately." Version 4.1 is earlier than 4.2, so immediate patching applies. The "no evidence of exploitation where the interface is not exposed" sentence describes the threat picture; it does not soften the instruction for pre-4.2 versions. A distinguishes exposure, C and D invent remediations the text never offers. Applying written rules exactly as keyed — by version, by classification, by threshold — is a recurring executive reading task, because your teams will quote your reading back to auditors. If you chose A, notice the exact mechanism of the error: you blended two different sentences — one giving an instruction keyed to version, one describing evidence keyed to exposure — into a single softer rule the advisory never wrote. Blending is the verbal equivalent of the numeric wrong-base error, and slowing down for one extra sentence-level check eliminates it.

**Passage D — Internal audit extract.**
*"The audit examined twelve business-critical systems. Seven rely on technologies that the vendors no longer support. Of these seven, four have documented remediation plans funded in the current financial year; the remaining three have plans that are documented but unfunded. The audit found no evidence that unsupported technology has yet caused a service outage. However, unsupported components cannot receive security patches, and the audit therefore assesses the residual risk as high. The audit recommends that the technology leadership present a prioritised funding proposal to the executive committee within three months. Management has accepted this recommendation."*

**Question 11 (easy) — True / False / Cannot Say.**
"A majority of the audited business-critical systems rely on unsupported technology."

**Answer: True.**

**Explanation:** Seven of twelve rely on unsupported technologies; seven is more than half of twelve (which would be six), so "a majority" is textually supported. The only work here is converting "seven of twelve" into the ordinary meaning of "majority" — a legitimate, minimal inference. True/False/Cannot Say allows arithmetic and standard word meanings; what it forbids is imported facts.

**Question 12 (challenging) — True / False / Cannot Say.**
"Three business-critical systems have no remediation plan."

**Answer: False.**

**Explanation:** The passage says the remaining three "have plans that are documented but unfunded." Unfunded is not the same as non-existent: all seven affected systems have documented plans; four are funded, three are not. The statement contradicts the text, so it is False — not Cannot Say. Candidates sometimes reach for Cannot Say whenever a statement feels slippery; the discipline is symmetrical. Choose False only when the text contradicts the statement, and here it does, explicitly. Executives make the mirror-image error in real governance: reporting "three systems have no plan" upward when the true position is "three plans await funding" — a difference that changes the ask you make of the executive committee.

**Question 13 (moderate) — True / False / Cannot Say.**
"Unsupported technology has caused at least one service outage."

**Answer: False.**

**Explanation:** The passage states the audit "found no evidence that unsupported technology has yet caused a service outage." Strictly, "no evidence found" is not logical proof of absence — but in the True/False/Cannot Say convention, the statement is judged against the passage, and the passage's only relevant content weighs against the statement. Standard marking treats this as False rather than Cannot Say because the text directly addresses and negates the claim as far as its knowledge extends; contrast Question 8, where the text never addressed the claim at all. Feel the difference between these two items — the text speaking against a claim versus the text being silent — and you have mastered the format's central distinction.

**Question 14 (moderate) — Multiple choice.**
What is the audit's central reasoning for assessing residual risk as high despite no outages having occurred?

- A: Because seven systems outnumber the five fully supported ones.
- B: Because unsupported components cannot receive security patches, so the exposure persists regardless of outage history.
- C: Because three remediation plans are unfunded.
- D: Because management accepted the recommendation.

**Answer: B.**

**Explanation:** The passage links its risk assessment with "however" and "therefore": no outages *however* unsupported components cannot receive security patches, *therefore* residual risk is high. The causal connective tells you exactly which fact drives the conclusion. A is arithmetic without causation; C aggravates the position but is not the stated reason; D is a consequence, not a cause. Tracing connectives — however, therefore, because, unless — is the fastest reliable route to "main reasoning" answers, and it is the same skill you use when a 60-page outline business case must be challenged on its actual argument rather than its executive summary.

**Passage E — Draft technology strategy extract.**
*"Over the next three years we will consolidate our application estate, reducing duplication and retiring systems that no longer earn their keep. We will adopt emerging technologies where they demonstrably improve outcomes for users, and only after evaluation against our published criteria. Our workforce plan will grow permanent engineering capability, reducing reliance on contingent labour as permanent capacity increases. Nothing in this strategy commits the organisation to specific procurements, which remain subject to spend controls and commercial approval. Progress will be reported to the executive committee quarterly, with an independent review at the eighteen-month point."*

**Question 15 (moderate) — True / False / Cannot Say.**
"The strategy commits the organisation to reducing contractor numbers within the first year."

**Answer: Cannot Say.**

**Explanation:** The strategy commits to "reducing reliance on contingent labour as permanent capacity increases" — a direction conditioned on permanent growth, with no timetable attached to the reduction. The three-year horizon frames the whole strategy, but nothing assigns the contractor reduction to the first year, and "reliance" is not the same measurable object as "numbers". The passage neither confirms nor contradicts a first-year reduction in headcount terms, so Cannot Say. Strategy documents are drafted with exactly this deliberate looseness; reading them precisely means noticing which commitments carry dates and metrics and which carry only direction.

**Question 16 (easy) — True / False / Cannot Say.**
"An independent review of progress is planned at the eighteen-month point."

**Answer: True.**

**Explanation:** Verbatim from the final sentence: "with an independent review at the eighteen-month point." The one nuance worth pausing on is that "review of progress" fairly paraphrases the sentence's subject, since the clause attaches to progress reporting. This is a direct-retrieval item; answer it in seconds and move on.

**Question 17 (challenging) — Multiple choice.**
A colleague summarises the strategy as: "We will adopt emerging technologies over the next three years." What is the most accurate criticism of this summary?

- A: It is wrong, because the strategy prohibits emerging technology adoption.
- B: It omits the strategy's conditions: adoption only where user outcomes demonstrably improve and only after evaluation against published criteria.
- C: It is accurate but incomplete, because it fails to mention quarterly reporting.
- D: It is wrong, because adoption decisions rest with the executive committee.

**Answer: B.**

**Explanation:** The strategy's sentence about emerging technology is conditional twice over: "where they demonstrably improve outcomes for users, and only after evaluation against our published criteria." A summary that drops both conditions converts a governed commitment into an open-ended one — the classic distortion that later appears in supplier decks as "your strategy says you will adopt emerging technology". A is false: the strategy permits conditional adoption. C misidentifies the flaw: the omission of reporting arrangements is trivial beside the omission of the conditions. D invents a decision right the passage never assigns — the executive committee receives progress reports; nothing says it approves adoptions. The verbal skill here is auditing a paraphrase against its source, which is precisely what you do when a board paper cites your strategy in support of a proposal the strategy does not actually license.

### Preparation tips

- **Read the statement before re-reading the passage.** Identify precisely what the statement claims — its subject, its quantifier (all, some, only), its strength (is, may, must) — then hunt the passage for text that supports or contradicts exactly that. This is faster and more accurate than absorbing the passage first and answering from memory.
- **Practise on your real inbox.** Take a supplier letter, a policy circular, or an audit extract from your working week and write three statements about it: one True, one False, one Cannot Say. Composing items teaches the distinctions faster than answering them.
- **Master the permission-words.** May, must, only, unless, subject to, notwithstanding: policy and contract passages turn on these. When you see one, slow down deliberately — assessments place the pivot of the question there.
- **Rehearse suspending expertise.** Your knowledge of hosting, security, and procurement is exactly what Cannot Say questions exploit. Before answering, ask: "Is my evidence in this passage, or in my career?" Only the former counts.
- **Distinguish silence from denial.** Text that never addresses a claim gives Cannot Say; text that speaks against it gives False. Drill this pair until the difference is instant — it is the single most commonly confused distinction at every level of seniority.
- **Notice connectives and conditions.** However, therefore, unless, provided that, where, only after: these small words carry the logical structure of a passage, and "main reasoning" and rule-application questions are almost always answered by tracing them rather than by re-reading the whole text.
- **Keep pace without panic.** At under a minute per question, bank the direct-quotation items quickly and invest your time in the inference items. Calibrated effort, not uniform effort, wins timed verbal tests.

### Common pitfalls

- **Importing outside knowledge.** Answering from what you know about cloud contracts, security advisories, or audit practice instead of from the passage. The more senior you are, the stronger this pull.
- **Confusing "likely" with "stated".** Treating a probable real-world outcome as a textual fact. The passage saying a risk "may materialise" never supports a statement that it "will".
- **Overusing Cannot Say.** Reaching for Cannot Say whenever a statement requires any thought. If the text contradicts the statement — even via one careful step — the answer is False.
- **Missing scope and effective-date clauses.** Policy passages often begin or end with sentences defining what the policy does not cover; questions target them because hurried readers skip them.
- **Being led by tone.** A reassuring supplier letter or a calm advisory can carry sharp obligations; an alarming passage can commit to nothing. Judge the propositions, not the mood.
- **Re-reading the whole passage for every question.** Time management collapses. Scan for the statement's keywords, read that sentence and its neighbours carefully, and answer.


## Workplace job-specific situational judgement assessment

### About this assessment

A workplace job-specific situational judgement assessment evaluates decision-making, interpersonal skill, and professional conduct by presenting realistic workplace dilemmas and asking how you would respond. Unlike the cognitive, numeric, and verbal assessments, there is usually no single objectively right answer; instead, several responses may seem reasonable, and the scoring reflects how closely your choices align with the values, priorities, and behavioural standards of the organisation and role. Formats vary: you may be asked to pick the **most effective** and **least effective** actions from a set, to rank all options from best to worst, or to rate each option's effectiveness independently. Timing is usually generous or absent, because the assessment measures natural judgement, not speed.

For a Chief Technology Officer in UK government, the dilemmas are executive-shaped: pressure from ministers and boards, security incidents with public visibility, supplier relationships worth millions, tensions between delivery deadlines and engineering health, and the daily work of advocating for technology among senior leaders who own other priorities. Your responses are read against UK public sector values — meeting user needs, transparency, collaboration across boundaries, accessibility and inclusion — and against the standing expectations of senior civil service leadership: honesty, integrity, objectivity, and impartiality.

Two features distinguish executive situational judgement from junior versions. First, escalation changes meaning: for a junior analyst, escalating is often the model answer, but you *are* the escalation point — options that pass a problem upward or sideways score poorly unless the issue genuinely exceeds your remit. Second, your choices are read as signals: how you handle one supplier, one incident, or one whistleblower teaches your entire organisation what you really value, and the strongest answers show awareness of that shadow you cast.

### What it measures for your role

Mapped to the skills named in your role summary:

- **Strategic technology planning** — dilemmas where short-term pressure collides with the strategy you set, testing whether you defend direction while staying pragmatic.
- **Financial decision making for technology** — scenarios about spending under pressure, sunk costs, and value for public money.
- **Technology evaluation** — dilemmas involving supplier influence, procurement fairness, and evidence-based selection.
- **Innovation in digital, data and technology** — scenarios balancing the duty to adopt valuable new technology against working within appropriate levels of risk.
- **Technology architecture** — dilemmas where governance is bypassed or resilience is traded for speed, testing your stewardship of reliable, permanent infrastructure.
- **Capability building for digital, data and technology** — scenarios about team health, skills investment, and the working environment your engineers experience.

The scenarios also draw directly on your stated duties: advocating for technology as part of the broader strategy, keeping systems continuously operational and resistant to attack, and creating working practices that support effective delivery.

### Practice questions

For each scenario, decide your answer before reading the discussion. The labels "most effective" and "least effective" reflect mainstream UK public sector executive expectations.

**Question 1 (moderate) — The minister's favourite product.**
After a supplier demonstration at a departmental event, a minister's special adviser tells you the minister was "very impressed" with an AI-powered case-triage product and would like to see it adopted quickly. Your evaluation pipeline has not assessed the product, and a competing procurement is mid-flight. Options:

- A: Commit to adopting the product within three months to maintain ministerial confidence.
- B: Explain the evaluation and procurement position, offer a rapid, structured assessment of the product against your published criteria, and brief the minister's office on the process and timeline.
- C: Quietly instruct the procurement team to re-weight criteria so the demonstrated product scores well.
- D: Decline to engage, noting that ministers should not influence technology choices.

**Most effective: B. Least effective: C.**

**Explanation:** B does everything the role demands at once: it protects procurement integrity, takes the ministerial interest seriously rather than dismissing it, channels enthusiasm into your legitimate evaluation machinery, and communicates transparently — advocating for good technology governance as part of the broader strategy. C is the least effective by a wide margin: rigging evaluation criteria is a procurement integrity breach that exposes the department legally and ethically; it converts political enthusiasm into institutional misconduct. A capitulates — committing before evaluation abandons your technology evaluation duty and sets a precedent that demonstrations outrank evidence. D is principled in tone but wrong in practice: ministers legitimately set priorities, and a CTO who refuses engagement loses the influence the role exists to exercise. The executive move is almost always B's shape: honour the interest, protect the process, and make the process fast enough to be credible.

**Question 2 (challenging) — Mid-launch security disclosure.**
Two days before a heavily publicised national service launch, your security team reports a vulnerability in an authentication component. Exploitation is difficult and there is no evidence of compromise, but a fix requires four days of work and re-testing. The programme director argues the launch must proceed with monitoring, and the fix can follow next week. Options:

- A: Proceed with the launch as planned, with enhanced monitoring, and schedule the fix for the following week.
- B: Delay the launch until the fix is applied and re-tested, and explain the reason candidly to the board and communications team.
- C: Convene your security lead, the programme director, and the senior risk owner immediately; require a written assessment of exploitability, impact, and mitigations; then decide launch-versus-delay against the organisation's stated risk appetite — and own the decision personally.
- D: Ask the programme director to make the final call, since delivery accountability sits with the programme.

**Most effective: C. Least effective: D.**

**Explanation:** C reflects mature executive risk management: the honest answer to "launch or delay" depends on facts the scenario deliberately leaves quantified only loosely, so the strongest action assembles those facts fast, tests them against an *explicit* risk appetite — your duty is to work within appropriate levels of risk, which requires knowing what those levels are — and locates the decision where it belongs: with you. It is decisive without being premature. B is defensible and scores well; its weakness is deciding before the structured assessment, potentially delaying a national launch on a risk that assessment might show to be well-mitigated — though its instinct for candour is exactly right. A accepts a known authentication weakness into a high-profile launch on the programme's schedule logic rather than a security judgement; monitoring detects exploitation but does not prevent it. D is the least effective: security risk acceptance for a citizen-facing service is a CTO-level accountability, and delegating it to the person with the strongest incentive to launch is an abdication dressed as respect for delivery. Assessors read D-type options harshly at executive level — they signal a leader who avoids owning hard calls.

**Question 3 (moderate) — Legacy versus transformation at the executive committee.**
At budget-setting, the executive committee is enthusiastic about funding a visible digital transformation programme but proposes cutting your legacy remediation budget by 60% to pay for it. You know three business-critical systems depend on unsupported components. Options:

- A: Accept the cut; transformation has stronger executive support and you can revisit remediation next year.
- B: Present the risk in service terms — which citizen services fail, how long recovery takes, what an outage costs — propose a rebalanced package that funds the highest-risk remediation alongside a slightly slower transformation, and ask the committee to record the residual risk if it still prefers the cut.
- C: Refuse to implement the cut and escalate to the permanent secretary.
- D: Accept the cut publicly but quietly divert transformation funding to remediation during the year.

**Most effective: B. Least effective: D.**

**Explanation:** B is textbook executive advocacy: it translates technical risk into the outcome language other leaders own, offers a constructive compromise rather than a binary, and — critically — uses the risk register properly by asking the committee to *own* the residual risk it chooses. That last element reflects transparency and collective government: committees may legitimately accept technology risk, but they must do so knowingly. D is the least effective: diverting funds against a committee decision is a governance and propriety breach that destroys the trust a CTO's influence depends on — worse than the risk it tries to fix, because it is dishonest rather than merely wrong. A fails the advocacy duty: silently accepting a cut you believe endangers business-critical services is the quiet abdication the role exists to prevent. C skips steps: escalation may eventually be right, but leaping over the committee before making the case within it burns collegial capital and signals you cannot influence peers — a core executive competency.

**Question 4 (moderate) — The engineer who went around the hierarchy.**
A mid-level engineer emails you directly, bypassing two management layers, to warn that a delivery team is disabling automated security tests to hit a deadline, and says their concerns were dismissed by their line manager. Options:

- A: Forward the email to the engineer's director and ask them to handle it.
- B: Thank the engineer, verify the claim quickly through your assurance channels, address the practice if confirmed, and separately examine why the concern did not surface through normal routes — while ensuring the engineer faces no reprisal.
- C: Reprimand the engineer for bypassing their management chain, and remind staff of proper escalation routes.
- D: Investigate the delivery team immediately and publicly, making an example of the disabled tests.

**Most effective: B. Least effective: C.**

**Explanation:** B handles all three layers of the situation: the immediate risk (disabled security tests on a deadline-driven team is credible and checkable), the systemic failure (a valid concern was dismissed below you — your working practices are not surfacing risk, which is your duty to fix), and the cultural signal (how this engineer is treated will teach every engineer whether raising concerns is safe). C is the least effective because it punishes the messenger: it converts a safety-culture asset into a warning to stay silent, and assessors read it as the single most damaging executive behaviour in the set — worse even than D's heavy-handedness, because C suppresses future information flow entirely. A is weak: it may be procedurally tidy, but it routes the concern back toward the chain that dismissed it, without verification or protection for the engineer. D acts on an unverified claim and optimises for spectacle over learning; public blame will fix one team's tests and teach fifty teams to hide problems better.

**Question 5 (challenging) — The lock-in renewal.**
A strategically important platform contract expires in seven months. The incumbent offers a 15% discount for immediate renewal of a five-year term. Your architecture team believes an open procurement could yield better long-term value and reduce lock-in, but switching costs are real and a procurement would be tight in seven months. Options:

- A: Accept the discounted renewal; the saving is concrete and the timeline risk is real.
- B: Run a rapid options appraisal — total costs of renewal versus competition including switching costs, market alternatives, and a negotiated shorter renewal as a bridge — and take the recommendation through commercial governance.
- C: Reject the incumbent's offer outright and launch an open procurement immediately to demonstrate market fairness.
- D: Renew for five years but ask the supplier to add contractual exit clauses.

**Most effective: B. Least effective: A.**

**Explanation:** B is the disciplined technology evaluation and financial decision-making answer: the genuinely open question is whether 15% off the incumbent's price beats the market, net of switching costs — a question you answer with analysis, not instinct, and legitimise through commercial governance. The bridge option (a short renewal buying time for a proper competition) is the move experienced CTOs reach for and assessors reward. A is the least effective here: a five-year commitment made under deadline pressure, without market testing, converts a supplier's pricing tactic into half a decade of deepened lock-in — the discount is visible, the forgone value invisible, and the seven-month clock was the supplier's design, not your constraint. C mistakes procedure for strategy: launching a procurement you may not be able to run well in the time available creates continuity risk without ensuring better value. D negotiates the right thing (exit provisions) inside the wrong decision — it accepts the five-year term before establishing whether any renewal is the right answer.

**Question 6 (moderate) — Outsourcing versus capability.**
A fellow director, frustrated by digital delivery timescales, proposes outsourcing an entire service line's technology to a single systems integrator, arguing "we should focus on policy, not engineering". You believe this would hollow out capability you have spent two years building. Options:

- A: Oppose the proposal in the executive committee, presenting evidence on long-term costs, intelligent-client risk, and the delivery record of your in-house teams — and propose an alternative that addresses the director's underlying frustration about pace.
- B: Support the proposal to preserve the relationship with a key peer.
- C: Agree to outsource, but insist your architecture team retains design authority.
- D: Lobby other board members privately against the proposal before the meeting so it fails without your fingerprints.

**Most effective: A. Least effective: D.**

**Explanation:** A does the whole job: it engages openly in collective decision-making, brings evidence rather than turf defence, and — the mark of a strong answer — treats the peer's frustration as a legitimate signal to address rather than an attack to repel. Your capability-building duty is not an entitlement to in-house delivery; it obliges you to show that in-house capability delivers value, and to fix pace problems where they are real. D is the least effective: covert lobbying to defeat a colleague without visible argument corrodes the collective trust an executive team runs on; even when it works, everyone eventually learns how it worked, and your influence becomes something peers defend against. B trades a strategic capability judgement for short-term comfort — an abdication of the advocacy your role exists to provide. C is partially defensible but concedes the substance while keeping a symbol: design authority without engineering capability becomes a rubber stamp within a contract cycle.

**Question 7 (moderate) — Accessibility found late.**
A week before a planned public launch, accessibility testing reveals that the new service fails multiple requirements: screen reader navigation is broken in the core journey. The delivery team proposes launching anyway with a "we are improving accessibility" statement, fixing issues over the following two months. Marketing materials have gone out. Options:

- A: Launch as planned with the statement; two months is a short delay for full accessibility.
- B: Delay the public launch until the core journey is accessible, keep the existing service running, and reset the launch communications — while commissioning a review of why accessibility surfaced only in the final week.
- C: Launch on time but add a dedicated telephone support line for affected users.
- D: Launch a "private beta" instead, restricting access to invited users, to avoid the accessibility obligation while fixing the issues.

**Most effective: B. Least effective: A (with D a close second-worst).**

**Explanation:** B reflects the two non-negotiables in play: public services must work for everyone — a broken screen-reader journey excludes the very users with least alternative — and a service that fails accessibility requirements at launch exposes the organisation legally and reputationally. The second half of B is what elevates it at executive level: finding the systemic cause (accessibility tested last, not continuously) is the CTO's actual job; the launch decision is merely triage. A is least effective: it launches a service that knowingly excludes disabled users, treats a legal requirement as a communications problem, and prices marketing sunk costs above user needs — the exact inversion of public sector values. C mistakes a workaround for inclusion: a phone line is not equivalent access, and assessors recognise it as mitigation theatre. D is gaming: relabelling a launch to dodge an obligation fails the transparency test and would not survive scrutiny; it scores nearly as badly as A because it adds bad faith to the exclusion.

**Question 8 (challenging) — The exhausted platform team.**
Your platform team has carried three major incidents, a data centre migration, and a hiring freeze in six months. Their lead tells you privately that two senior engineers are close to resigning and on-call rotas are unsustainable. Meanwhile, the transformation programme needs the same team for a critical dependency next quarter. Options:

- A: Ask the team to push through one more quarter, offering overtime payments and a recovery period afterwards.
- B: Rebalance now: pause or resequence the transformation dependency, fix the on-call rota immediately (even by buying external cover), press to lift the hiring freeze for this team, and tell the transformation board plainly why.
- C: Tell the team lead to manage morale within existing resources; every team is stretched.
- D: Escalate the hiring freeze to the executive committee and await its decision before changing anything.

**Most effective: B. Least effective: C.**

**Explanation:** B treats the situation as what it is: an operational risk to continuously operational systems (an exhausted platform team is a resilience problem, not just an HR one), a capability risk (senior engineers leaving takes years to reverse), and a delivery risk (the transformation dependency fails anyway if the team breaks). Acting on the rota immediately, resequencing demand, and being transparent with the transformation board honours both your capability-building duty and your delivery duty — and accepts the political cost of saying no, which is what the salary is for. C is the least effective: it normalises unsustainable working practices, ignores a direct warning from the person best placed to know, and — when the resignations land — will be remembered as the moment leadership was told and did nothing. A buys a quarter with money that does not restore sleep; overtime payments do not fix on-call unsustainability, and "recovery afterwards" rarely survives contact with the next programme. D does one right thing (challenging the freeze) while deferring everything within your own power; executives who wait for committees to fix what they can fix today score poorly.

**Question 9 (moderate) — The failed innovation pilot.**
An innovation pilot you personally sponsored — a machine-learning tool for document processing — has failed its evaluation: accuracy is below the threshold and running costs are double the estimate. The board paper on the innovation fund is due, and a colleague suggests describing the pilot as "delivering valuable learning and progressing to a second phase". Options:

- A: Report the pilot as failed against its published criteria, state the cost, capture the genuine lessons, and recommend closure — using the report to reinforce that the fund's discipline is what makes future pilots trustworthy.
- B: Accept the colleague's framing; boards fund optimism, and the fund's future depends on this paper.
- C: Report it as failed but attribute the failure primarily to the supplier's technology to protect the fund's standing.
- D: Extend the pilot for three months with revised targets, giving it a chance to earn a better report.

**Most effective: A. Least effective: B.**

**Explanation:** A is the answer that makes innovation sustainable in the public sector. Pilots exist to generate decision-grade evidence cheaply; a pilot that fails and is *closed* is the system working, and reporting it plainly is what earns the fund its licence to take the next risk. The strongest executive answers convert the failure into institutional credibility: "we set criteria, we measured, we stopped" is the sentence that persuades boards to keep funding experiments — working within appropriate levels of risk in its truest form. B is the least effective: dressing failure as progress is a transparency breach that, once discovered (and cost overruns are always discovered), taxes every future claim you make; it also traps the organisation into a second phase justified only by the sentence that announced it. C is honest about the outcome but dishonest about the cause; blame-shifting to suppliers erodes the relationships and the internal accountability that evaluation depends on. D is disguised sunk-cost reasoning: revising targets after the results are known inverts the discipline that makes evaluation meaningful.

**Question 10 (challenging) — The peer who bypassed architecture governance.**
You discover that a director-level peer has signed a contract for a customer-data platform without any architecture review, creating a second citizen-record store that conflicts with your "store data once" principle. The contract is signed; the supplier has started work. Options:

- A: Demand the contract be cancelled and the peer be formally reprimanded for bypassing governance.
- B: Talk to the peer first to understand what need drove the bypass; then bring the platform into architecture governance retrospectively — assessing integration options, containment, or negotiated exit — and separately fix the gap that let a technology contract be signed without review, taking the systemic lesson (not the individual) to the executive committee.
- C: Ignore it; the contract is signed, and challenging a peer will damage the relationship.
- D: Instruct your architecture team to refuse all integration work with the new platform until it passes review.

**Most effective: B. Least effective: C.**

**Explanation:** B works all three problems in the right order. First, the need: governance bypasses usually signal an unmet need moving faster than your processes — understanding it prevents recurrence better than punishment. Second, the technical reality: the contract exists; the architecture duty now is minimising harm through integration, containment, or exit analysis, not pretending the decision can be unmade by indignation. Third, the system: a technology contract reached signature without architecture review, which means your governance is advisory when it should be embedded in commercial approval — that is the fixable, valuable lesson, and taking it forward as a systems failure rather than a personal one preserves the collaboration you need from every other director watching. C is the least effective: it accepts both a live architectural harm (duplicate citizen records breed inconsistency, cost, and data protection risk) and a precedent that governance is optional for anyone senior enough — the combination quietly ends your architecture authority. A optimises for being right over being effective: cancellation may be impossible or wasteful, and leading with reprimand converts a fixable governance gap into an executive feud. D weaponises your team in a peer conflict, harming users and delivery to make a point — assessors read it as passive aggression with public money.

### Preparation tips

- **Anchor on published values.** UK public sector situational judgement is scored against user needs, transparency, collaboration, accessibility, and inclusion, plus the Civil Service values of honesty, integrity, objectivity, and impartiality. Before the assessment, write each value on one line and sketch what it looks like at CTO level — then use them as your scoring rubric for every option.
- **Look for the option that does three jobs.** The strongest executive answers usually address the immediate risk, the systemic cause, and the cultural signal simultaneously. Options that fix only the surface problem are rarely the "most effective".
- **Beware of both extremes.** Options that capitulate (accept the cut, launch anyway, sign the renewal) and options that confront maximally (refuse, reprimand, cancel) usually bracket the best answer, which engages, evidences, and preserves relationships while holding the line.
- **Own what is yours.** At your level, delegating a risk decision downward or waiting for a committee to act on something within your power scores badly. Ask of every option: is this decision genuinely someone else's, or am I being offered a comfortable exit?
- **Read the least-effective question as carefully as the most.** Marks are often lost by mistaking a merely weak option for the actively harmful one. Harm usually involves dishonesty, suppressing information, punishing messengers, or excluding users — weigh those above simple ineffectiveness.
- **Rehearse with your own history.** Recall five real dilemmas from your career and write down what you did, what worked, and what you would change. Assessments reward the judgement that reflection builds; this is the most efficient preparation available to a senior candidate.

### Common pitfalls

- **Answering idealistically rather than effectively.** Choosing the option that sounds noblest ("refuse on principle") rather than the one that would actually work in a real department. Assessors want practical wisdom, not purity.
- **Selecting passive options.** Choices that delay action, refer the problem onward, or wait for others score poorly at executive level — you are the person others escalate to.
- **Ignoring the values context.** Answering as a commercial-sector CTO might — optimising for speed and market position — without weighing transparency, accessibility, inclusion, and public money. The public sector frame changes several answers.
- **Punishing messengers and managing optics.** Options that suppress bad news, blame suppliers or juniors, or relabel failure as success are consistently scored as least effective, even when they look pragmatic.
- **Over-escalating.** Treating the permanent secretary or executive committee as the answer to problems within your own authority. Escalation is for genuine remit boundaries, not discomfort.
- **Forgetting the watching organisation.** Every option teaches your teams what you value. Options that get today's result at the cost of tomorrow's information flow — or of the safety people feel in raising concerns — are traps laid for exactly this role.


## Conclusion

You have now worked through four substantial assessment types, each built from the real material of a Chief Technology Officer's working life: dependency maps and assurance rules in the cognitive section; budgets, total cost of ownership, and capacity projections in the numeric section; policies, supplier letters, advisories, and audit extracts in the verbal section; and the genuinely hard dilemmas — ministers, security calls, exhausted teams, failed pilots, and peers who bypass governance — in the situational judgement section.

If you attempted the questions honestly before reading the explanations, you have done something more valuable than test preparation: you have audited your own habits of thought. Perhaps you discovered that you cross-foot tables instinctively but reach for Cannot Say too rarely; or that your numeric reasoning is sharp but your first instinct in dilemmas is a shade more confrontational than effective. That self-knowledge is the real yield of this document. Assessments come and go; the reasoning habits they measure are the ones you use every day, in every board paper, incident call, and investment decision.

As next steps, three suggestions. First, revisit the questions you found hardest in a week's time — spaced repetition works for reasoning patterns just as it does for facts. Second, practise on live material: your own inbox, business cases, and risk registers are an inexhaustible question bank, and interrogating them sharpens both your assessment performance and your actual governance. Third, keep building the muscles this document exercised — precision reading, compound-growth intuition, contrapositive logic, and values-anchored judgement — because they compound like everything else worth investing in.

Whatever assessed process brought you here, approach it with confidence. You operate daily at a level of complexity that these assessments can only sample. Prepare well, rest well, read every question as carefully as you would read a contract, and let the quality of your thinking show. Your organisation — and the citizens its services exist for — benefit every time a technology leader reasons this carefully. Good luck.
