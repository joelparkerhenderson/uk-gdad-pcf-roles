# Enterprise Architect (Lead Enterprise Architect) - Psychometric Assessment Resources

## Introduction

Welcome. This resource is written for you as a lead enterprise architect working within the UK Government Digital and Data profession. Whether you are preparing for an internal assessment, benchmarking yourself against the demands of your role, or supporting members of your architecture community through their own development, this document gives you a structured, practical way to engage with the four psychometric assessment types most relevant to your work.

Psychometric assessments are standardised instruments that measure the mental capabilities and behavioural tendencies that underpin professional performance. For a role at your level, they are rarely about raw processing speed alone. Instead, they probe the qualities that distinguish effective strategic leadership: the ability to reason clearly through ambiguous, multi-domain problems; to interpret financial, capacity and performance data with confidence; to extract precise meaning from dense policy and standards documentation; and to exercise sound judgement in high-stakes situations involving senior stakeholders across enterprises.

You already do these things daily. You own the enterprise architecture vision, strategy and roadmaps across business, technology and data perspectives. You establish architectural principles, policies and standards. You mediate difficult architectural discussions, guide investment decisions towards reuse, sustainability and scalability, and horizon scan for emerging trends and risks. This document simply reframes those familiar activities as assessment material, so that when you encounter a formal psychometric exercise, the format feels as natural as the content.

The document is organised into four main sections, each covering one assessment type:

1. **Workplace job-specific cognitive assessment** - logical reasoning, pattern recognition, error checking and prioritisation using the artefacts you genuinely handle: roadmaps, reference architectures, decision records and transition plans.
2. **Workplace job-specific numeric reasoning assessment** - interpretation of budgets, supplier costs, capacity figures, portfolio metrics and value-for-money calculations.
3. **Workplace job-specific verbal reasoning assessment** - precise comprehension of standards, policies, board papers and stakeholder correspondence.
4. **Workplace job-specific situational judgement assessment** - realistic dilemmas drawn from the stakeholder landscape of a lead enterprise architect in UK government.

Each section explains what the assessment measures, maps it to the specific skills in your role profile, provides a substantial bank of worked practice questions at varying difficulty levels, and closes with preparation tips and common pitfalls.

Use this resource actively. Attempt each question before reading the explanation, note where your reasoning diverged from the worked answer, and treat any recurring divergence as a development signal rather than a failure. You may also find the question bank useful when coaching enterprise architects in your teams, since developing the architecture community is itself part of your role. Take your time, work through it in sittings that suit you, and enjoy the process.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive ability assessment measures the exact mental processes needed for your role, using practical scenarios and data drawn from the work itself rather than abstract puzzles. For a lead enterprise architect, that means reasoning over roadmaps, transition states, architectural principles, governance rules, dependency maps and decision records - the artefacts through which you translate business strategy into business change and technical delivery.

These assessments are typically timed, often 15 to 30 minutes online, and scored objectively against a benchmark or norm group. Questions are validated to predict job success without bias, and many modern platforms adapt question difficulty based on your previous answers. Employers usually receive a breakdown of speed versus accuracy rather than a single score, which matters for you: at lead level, accuracy of reasoning across complex, interdependent material generally counts for more than raw pace, though you should still practise working briskly.

Expect a short set of ungraded practice questions before the assessment begins, so you can get comfortable with the interface. Use them fully - even experienced leaders benefit from settling into the rhythm of a timed format before the scored items start.

### What it measures for your role

Mapped against the skills in your role profile, a cognitive assessment probes:

- **Enterprise architecture** and **Strategy design**: can you hold 'as is', 'to be' and transitional states in mind simultaneously, reason about the ordering of change, and spot where a proposed sequence of deliveries breaks a dependency? Questions test whether you can connect strategies or visions across an organisation logically, not just rhetorically.
- **Making architectural decisions**: deductive reasoning from architectural principles, policies and standards to a specific design decision; identifying which governance rule applies, and detecting when a decision record contradicts itself or the standards it cites.
- **Problem definition and shaping**: framing a problem characterised by high complexity so that a solution can be created requires isolating the true constraints from the noise. Cognitive items test exactly this - separating relevant from irrelevant information under time pressure.
- **Architect for the whole context**: pattern recognition across trend data, and inference about how societal and industry shifts might impact the organisation.
- **Commercial perspective**: logical evaluation of supplier options and contractual constraints, where multiple conditions must hold at once.
- **Prioritisation for delivery at pace**: several items below ask you to identify priorities for change under competing constraints, mirroring your duty to enable delivery at pace.

### Practice questions

**Question 1 (easy) - Principle hierarchy**

Your organisation's architectural principles state: (1) "Reuse before buy; buy before build." (2) "All citizen-facing services must meet the accessibility standard." (3) "Where principles conflict, the accessibility principle takes precedence."

A programme team finds a reusable internal component for document upload, but it fails the accessibility standard. A commercial product passes the accessibility standard. Building in-house would also pass, at higher cost.

Which option is most consistent with the principles?

A. Reuse the internal component, because reuse takes precedence.
B. Buy the commercial product.
C. Build in-house, because it guarantees compliance.
D. Escalate to the architecture review board before any decision.

**Correct answer: B.**

**Explanation:** Principle 3 makes accessibility override the reuse hierarchy, so the non-compliant internal component (A) is eliminated. Between the remaining compliant options, principle 1 still applies: buy before build, so B beats C. Option D is tempting - governance is real - but the question asks which option is most consistent with the stated principles, and the principles resolve the conflict without escalation. Assessments at lead level frequently include a plausible "escalate" distractor to test whether you apply rules you already have before deferring upwards.

**Question 2 (easy) - Transition state sequencing**

A roadmap defines four transition states for retiring a legacy case-management system:

- State W: new platform live for one pilot business unit.
- State X: legacy system read-only; all new cases on the new platform.
- State Y: data migration of historical cases completed.
- State Z: legacy system decommissioned.

The design rules say: no business unit can move until the pilot completes; the legacy system cannot become read-only until every unit has moved; decommissioning requires both read-only status and completed migration.

Which sequence is valid?

A. W, Y, X, Z
B. W, X, Y, Z
C. X, W, Y, Z
D. W, Z, X, Y

**Correct answer: Both A and B satisfy the stated rules; if only one may be chosen, B is the conventional answer expected - but check the rules carefully: A is also permitted because migration (Y) has no stated dependency on read-only status (X). The best single answer as written is B.**

**Explanation:** This item illustrates a common cognitive-test trap: rules you assume versus rules stated. W must come first (pilot before movement). Z must come last (needs X and Y). The only genuinely constrained ordering question is whether Y may precede X - and the stated rules do not forbid it. In a live assessment, choose the option that violates nothing: if both A and B appear, re-read the rules for a dependency you missed; if the test permits only one answer, prefer the sequence that also matches operational common sense (migrating after write-freeze avoids re-migration), which is B. Lead-level tests reward noticing that the constraint set underdetermines the answer - exactly the skill of challenging requirements and assumptions named in your Problem definition and shaping skill.

**Question 3 (moderate) - Error checking a roadmap extract**

You are assuring a portfolio roadmap before it goes to the investment board. An extract reads:

| Initiative | Start | End | Depends on | Funding status |
|---|---|---|---|---|
| Identity platform v2 | Apr 2026 | Mar 2027 | - | Approved |
| Case system replacement | Jan 2027 | Dec 2027 | Identity platform v2 (complete) | Approved |
| Data sharing gateway | Jun 2026 | May 2027 | Case system replacement (live) | Pending |
| Legacy archive service | Jan 2028 | Jun 2028 | Data sharing gateway (live) | Approved |

Which single entry contains the logical error?

A. Identity platform v2
B. Case system replacement
C. Data sharing gateway
D. Legacy archive service

**Correct answer: C.**

**Explanation:** The data sharing gateway starts in June 2026 and ends in May 2027, yet it depends on the case system replacement being live - which does not finish until December 2027. A project cannot complete seven months before its prerequisite. Check the others: the case system replacement starts January 2027, before the identity platform completes in March 2027 - but its dependency is on completion, and starting work before a dependency completes is common (the error test is whether it *ends* impossibly or claims the dependency at the wrong point; strictly, its stated dependency "complete" before start makes B arguable, but C's violation is unambiguous because the entire initiative finishes before its prerequisite exists). The legacy archive service starts after its dependency is live. When two candidates look flawed, pick the unambiguous contradiction - assessments score the clearest error.

**Question 4 (moderate) - Governance deduction**

Your architectural governance framework states: "All decisions rated high-risk must be assured by the design authority. Any decision involving citizen data crossing organisational boundaries is rated high-risk. Decisions assured by the design authority must have a recorded options analysis."

A team's decision record proposes sharing citizen data with another department and contains no options analysis. Which conclusion follows necessarily?

A. The decision must be rejected.
B. The decision record is not yet compliant with governance.
C. The team failed to consult stakeholders.
D. The design authority has not reviewed the decision.

**Correct answer: B.**

**Explanation:** Chain the rules: citizen data crossing organisational boundaries → high-risk → design authority assurance required → recorded options analysis required. The record lacks an options analysis, so it cannot yet satisfy governance: B follows necessarily. A goes too far - non-compliance means the record must be remediated, not that the decision is substantively wrong. C introduces facts not in evidence. D is unsupported: the design authority may have reviewed it and requested the missing analysis; we cannot know. This is classic syllogistic reasoning dressed in your governance clothing - resist conclusions that feel operationally plausible but are not entailed.

**Question 5 (moderate) - Prioritising change initiatives**

You must recommend which one of four initiatives to accelerate to enable delivery at pace. Constraints: the accelerated initiative must not require new funding this year, must unblock at least two other programmes, and must not depend on the outcome of the pending machinery-of-government change.

- Initiative P: unblocks three programmes; needs £2m new funding; independent of the MoG change.
- Initiative Q: unblocks two programmes; funded from existing budget; scope fixed regardless of the MoG change.
- Initiative R: unblocks four programmes; funded; its target operating model will be redrawn if the MoG change proceeds.
- Initiative S: unblocks one programme; funded; independent of the MoG change.

Which do you recommend?

A. P B. Q C. R D. S

**Correct answer: B.**

**Explanation:** Apply the constraints as filters. P fails the funding constraint. R fails the MoG-independence constraint - its benefit case is contingent on a decision outside your control, exactly the sort of dependency your horizon-scanning duty teaches you to treat as risk. S passes both hard constraints but unblocks only one programme, failing the "at least two" threshold. Q passes all three constraints. Note the design of the distractors: R offers the biggest headline benefit, and assessments deliberately test whether you let magnitude override constraint satisfaction. As a lead enterprise architect recommending reuse, sustainability and scalability to achieve value for money and reduce risk, constraint discipline is the assessed behaviour.

**Question 6 (moderate) - Dependency logic across domains**

Four capability teams report these facts: the payments capability can go live only if the identity capability is live; the notifications capability can go live independently; the reporting capability requires both payments and notifications to be live. Currently, identity is live and nothing else is.

Which statement must be true?

A. Payments can go live now.
B. Reporting can go live once payments is live.
C. Reporting cannot go live before notifications.
D. Notifications must go live before payments.

**Correct answer: C.** (A is also true as stated - see explanation for how to choose.)

**Explanation:** Test each option against the facts. A: identity is live, so payments *can* go live now - true. C: reporting requires notifications, so it cannot precede it - also true, and true in all possible worlds regardless of what happens next. B is false as stated because reporting also needs notifications. D is false: no ordering between notifications and payments is required. When a test presents two true options, prefer the one framed as a necessity ("must be true") that holds unconditionally: A describes a current possibility that could be invalidated by additional unstated constraints (e.g. an embargo), while C is entailed purely by the dependency structure. Strong candidates at your level verbalise the dependency graph mentally and check entailment, not plausibility.

**Question 7 (moderate) - Reference architecture reuse**

Your reference architecture catalogue records: every service in Domain A uses the shared identity pattern; some services in Domain B use the shared identity pattern; no service using the shared identity pattern stores credentials locally.

Which conclusion is valid?

A. No service in Domain B stores credentials locally.
B. Some services in Domain B do not store credentials locally.
C. Every service in Domain A is in Domain B.
D. Some services in Domain A store credentials locally.

**Correct answer: B.**

**Explanation:** The services in Domain B that use the shared identity pattern - and "some" guarantees at least one exists - cannot store credentials locally, so at least some Domain B services do not store credentials locally: B is valid. A overreaches: services in Domain B that do not use the pattern are unconstrained by the stated rules. C invents a relationship between domains that nothing supports. D contradicts the rules: all Domain A services use the pattern, and pattern users never store credentials locally. This is categorical logic wearing your catalogue's clothes; drawing a quick mental Venn diagram of "pattern users" inside "no local credentials" resolves it in seconds. In assurance work, the same discipline stops you claiming compliance for an estate when your evidence covers only a subset of it.

**Question 8 (moderate) - Internal consistency of a decision record**

An architecture decision record submitted to your design authority states:

1. "We selected the department's shared hosting platform to maximise reuse."
2. "The service will run in the supplier's proprietary cloud, as required by the supplier's licence."
3. "This decision carries low risk because it introduces no new hosting arrangements."
4. "Exit costs are minimal because the workload is containerised on the shared platform."

Which pair of statements is contradictory?

A. 1 and 4
B. 1 and 2
C. 3 and 4
D. 2 and 4

**Correct answer: B.**

**Explanation:** Statement 1 claims the service uses the department's shared hosting platform; statement 2 says it runs in the supplier's proprietary cloud. A workload cannot have its primary hosting in both, so the record contradicts itself at its core claim. Statements 2 and 4 (option D) are in tension too - containerisation "on the shared platform" sits oddly with proprietary-cloud hosting - but that tension is derivative of the primary contradiction between 1 and 2, and D describes an inconsistency of detail rather than of the decision itself. Statement 3 is *false* if 2 is true (a proprietary cloud is a new hosting arrangement), but false-given-another-statement is not the same as a direct contradiction between the pair named. Error-checking items reward locating the root inconsistency; in real assurance, sending the record back citing 1 versus 2 forces the team to clarify the actual design, after which the other defects resolve or crystallise.

**Question 9 (challenging) - Supplier selection under joint constraints**

You are evaluating four suppliers for an enterprise integration platform. Mandatory constraints: the supplier must support open standards; must offer exit assistance in the contract; and must not require a minimum term longer than three years. Desirable: UK data residency.

- Supplier 1: open standards; exit assistance; five-year minimum term; UK residency.
- Supplier 2: open standards; no exit assistance; two-year term; UK residency.
- Supplier 3: open standards; exit assistance; three-year term; residency in an adequacy-agreement country.
- Supplier 4: proprietary interfaces with an open-standards roadmap; exit assistance; one-year term; UK residency.

Which supplier satisfies all mandatory constraints?

A. Supplier 1 B. Supplier 2 C. Supplier 3 D. Supplier 4

**Correct answer: C.**

**Explanation:** Work the mandatory constraints as a strict filter before even glancing at desirables. Supplier 1 fails the term constraint (five years exceeds three; "not longer than three" permits exactly three). Supplier 2 fails exit assistance. Supplier 4 fails open standards - a roadmap is a promise, not present compliance, and treating vendor roadmaps as delivered capability is a classic commercial-perspective error your role profile explicitly guards against when identifying, evaluating and selecting suppliers. Supplier 3 passes all three mandatory constraints; UK residency is only desirable, so its absence cannot disqualify. The trap is Supplier 1: it wins on desirables and on three of four attributes, and time-pressured candidates pattern-match to "best overall" instead of "satisfies all mandatory". Mandatory means mandatory - the same discipline that underpins defensible procurement decisions and value for money.

**Question 10 (challenging) - Horizon-scanning inference**

Your horizon-scanning summary records four observed trends and your analysts' confidence in each:

| Trend | Direction | Confidence | Time to impact |
|---|---|---|---|
| T1: AI-assisted casework tooling maturing | Rising | High | 1-2 years |
| T2: Legacy skills market shrinking | Rising cost | High | Now |
| T3: Quantum-safe cryptography mandates | Emerging | Medium | 3-5 years |
| T4: Citizen expectation of real-time services | Rising | High | Now |

Your strategy review can add exactly one new cross-cutting capability to the roadmap's first transition state (next 18 months). Which trend most strongly justifies a first-transition-state response, based only on the table?

A. T1, because AI tooling is maturing fastest.
B. T2, because the cost pressure is high-confidence and already landing.
C. T3, because cryptographic change takes longest to execute.
D. T4, because citizen expectation is the ultimate driver of strategy.

**Correct answer: B.**

**Explanation:** The question restricts you to the table: combine confidence with time-to-impact. T2 is high confidence and impacting *now* - a shrinking legacy skills market raises the cost and risk of every year the 'as is' estate survives, which directly threatens transitional states. T4 is also high confidence and current, but it is a demand signal rather than a delivery risk, and the table gives no basis to prefer it over T2's immediate cost exposure - whereas T2's "rising cost, now" makes the case for near-term action explicit. T1 is 1-2 years away; responding is plausible but not *most strongly justified* for the first transition state. C contains a genuinely good architectural instinct - long-lead changes need early starts - but the table rates T3 medium confidence and 3-5 years out, so on the given evidence it earns a watching brief, not the single first-state slot. Notice the distractors reward outside knowledge and enthusiasm; the assessed skill is disciplined inference from the evidence in front of you.

**Question 11 (challenging) - Scheduling the design authority**

You chair a design authority that must review five decisions (D1-D5) across three weekly sessions, at most two decisions per session. Constraints: D1 must be reviewed before D3 (D3 builds on D1's outcome). D2 and D4 cannot share a session (same presenting team). D5 must be in the final session (awaiting supplier information). D4 must be reviewed in the first or second session (contract deadline).

If D1 and D2 are reviewed in session one, which allocation of the remaining decisions is valid?

A. Session two: D3 and D4; session three: D5.
B. Session two: D3 and D5; session three: D4.
C. Session two: D4 only; session three: D3, D5 and a carried-over item.
D. Session three: D3, D4 and D5.

**Correct answer: A.**

**Explanation:** Check A against every constraint: D1 precedes D3 (session one before session two) - satisfied. D2 and D4 are in different sessions - satisfied. D5 sits alone in the final session - satisfied. D4 is in session two - satisfied. Two-per-session limit - satisfied. B breaks the D5-final-session rule and the D4 deadline. C implies three items in session three, breaching the capacity limit. D places three decisions in one session and D4 outside its deadline. Multi-constraint scheduling items reward a mechanical, constraint-by-constraint check rather than holistic impressions - the same habit that makes your architectural governance credible: assurance is the systematic verification that every applicable rule is met, not a general feeling that the plan looks sensible.

**Question 12 (challenging) - Applying a policy exception rule**

Your standards policy states: "Deviations from an architectural standard are permitted only where (a) a time-bound exception is approved by the design authority, (b) a remediation plan exists, and (c) the deviation does not affect citizen data. Deviations affecting citizen data require, in addition, approval from the data governance board."

A team deviates from the API standard for a service processing citizen data. They hold design authority approval, a remediation plan, and data governance board approval. Is the deviation permitted?

A. Yes - all required approvals and the plan are in place.
B. No - condition (c) prohibits any deviation affecting citizen data.
C. Cannot be determined - the policy is internally contradictory.
D. No - the API standard cannot be subject to exceptions.

**Correct answer: A (reading the policy as a whole), though a strictly literal reading supports C - the strongest defensible answer in a test is A.**

**Explanation:** Read literally, sentence one makes (c) a necessary condition, which would make sentence two - which plainly contemplates permitted deviations affecting citizen data with an extra approval - incoherent. The established interpretive principle, in policy drafting as in law, is to read provisions so that both have effect: sentence two operates as a carve-out that modifies (c), adding a fourth requirement for citizen-data cases. The team meets all four: time-bound design authority approval, remediation plan, and data governance board approval for the citizen-data aspect. B applies sentence one while ignoring sentence two. C is the answer a logician might give, and noticing the drafting defect is genuinely valuable - in real life you would fix the wording, since you own the principles, policies and standards - but assessments expect the coherent whole-text reading. D invents a rule. This item mirrors a daily reality of your role: standards are texts, texts have defects, and leaders resolve them purposively while initiating the correction.

**Question 13 (moderate) - Pattern recognition in capability maturity**

Annual maturity scores (1-5) for four cross-cutting capabilities over three years:

| Capability | Year 1 | Year 2 | Year 3 |
|---|---|---|---|
| API management | 2 | 3 | 4 |
| Data governance | 3 | 3 | 3 |
| Cloud hosting | 1 | 3 | 5 |
| Service resilience | 4 | 3 | 2 |

If each capability's trend continues for one more year, which capability will have the *lowest* score in Year 4?

A. API management
B. Data governance
C. Cloud hosting
D. Service resilience

**Correct answer: D.**

**Explanation:** Extrapolate each arithmetic pattern one step. API management rises by one per year: 2, 3, 4 → 5. Data governance is flat: 3. Cloud hosting rises by two: 1, 3, 5 → 7, though on a 1-5 scale it caps at 5 - either way it is not lowest. Service resilience falls by one per year: 4, 3, 2 → 1, the lowest projected score. The strategic reading matters as much as the arithmetic: a capability quietly degrading by one maturity point a year while headline capabilities improve is exactly the pattern a lead enterprise architect's assurance radar should catch, because resilience erosion is a cross-cutting risk affecting every portfolio that depends on it. Simple trend items like this appear early in adaptive tests; answer them quickly and accurately to bank time for the multi-constraint questions.

### Preparation tips

- **Practise with your own artefacts.** Take a real (suitably anonymised) roadmap, decision record or dependency map and quiz yourself: what must be true, what cannot be true, what is underdetermined? This builds the entailment habit that cognitive tests measure.
- **Separate "stated" from "assumed".** Several questions above turn on constraints candidates import from experience. Before answering, ask: is that rule in the text, or in my head? Your skill in helping others challenge requirements and assumptions is precisely the muscle to use.
- **Filter with hard constraints first.** For prioritisation and selection items, eliminate options that violate any mandatory condition before comparing merits. It is faster and more accurate.
- **Manage the clock at leader pace.** Aim for a steady rhythm; if an item resists you for ninety seconds, flag it and move on. Accuracy across the paper beats heroics on one question.
- **Warm up before the session.** Ten minutes of practice items immediately beforehand measurably steadies early-question performance, and the early questions often calibrate adaptive difficulty.

### Common pitfalls

- **Choosing the plausible over the entailed.** Operationally sensible answers that the given rules do not support are the most common wrong answers at senior level. The test rewards deduction, not experience-flavoured intuition.
- **Letting magnitude trump constraints.** The option with the biggest benefit often fails a mandatory condition - by design.
- **Over-escalating.** "Refer it to the board" distractors punish leaders who defer decisions the stated rules already resolve.
- **Time-sink questions.** Multi-constraint items can absorb minutes; getting stuck on one instead of banking easier marks is the classic error-checking trap.
- **Missing scale and scope qualifiers.** "Some", "all", "only", "no later than", "not longer than" - each word changes the logic. Read quantifiers twice.


## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment evaluates your ability to analyse, interpret and make sound decisions using numerical data in the formats your role actually handles. It emphasises business mathematics - percentages, ratios, cost comparisons, capacity figures and trend calculations - rather than abstract formulae. Most assessments allow or provide an on-screen calculator, because the assessed skill is interpretation and decision-making, not mental arithmetic. Expect strict time limits, typically around a minute to ninety seconds per question, which rewards quick, accurate extraction of the right numbers from tables, charts and dashboards.

For a lead enterprise architect, the data will look like investment cases, supplier pricing schedules, cloud consumption reports, portfolio dashboards, workforce plans and sustainability metrics. Your duty to guide the organisation towards reuse, sustainability and scalability "to achieve value for money and reduce risk" is, at bottom, a quantitative claim: you must be able to demonstrate, with defensible numbers, why one architectural direction creates more value than another. Numeric reasoning assessments simulate exactly that demonstration under time pressure.

### What it measures for your role

Mapped to your role profile, numeric items test:

- **Commercial perspective**: evaluating supplier bids, comparing contractual pricing models, calculating total cost of ownership and exit costs, and recognising when a headline price conceals a worse whole-life cost. Identifying, evaluating and selecting appropriate suppliers is a numbers-first discipline.
- **Enterprise architecture** and **Strategy design**: quantifying 'as is' versus 'to be' - run costs, capacity headroom, service volumes - and modelling what each transition state costs and saves. Advocating for resources requires arithmetic that survives scrutiny by finance directors.
- **Making architectural decisions**: weighing options where risk and cost trade off, and reading portfolio metrics well enough to spot when a decision's assumptions no longer hold.
- **Architect for the whole context**: interpreting trend data - market rates, energy prices, demand growth - and projecting their impact, which is horizon scanning expressed numerically.
- **Leading teams and developing the community**: workforce and capacity planning for the architects you lead, including full-time-equivalent calculations and coverage ratios.

### Practice questions

**Question 1 (easy) - Budget percentage change**

Your architecture function's budget was £2.4m last year. This year it is £2.7m. What is the percentage increase?

A. 11.1% B. 12.5% C. 8.9% D. 15.0%

**Correct answer: B.**

**Explanation:** Percentage increase = (new − old) ÷ old × 100 = (2.7 − 2.4) ÷ 2.4 × 100 = 0.3 ÷ 2.4 × 100 = 12.5%. The common error is dividing by the new figure: 0.3 ÷ 2.7 = 11.1%, which is exactly distractor A. Always divide by the baseline - the value you are measuring change *from*. Wrong-denominator distractors appear throughout numeric tests, so build the reflex of asking "change relative to what?" before you calculate.

**Question 2 (easy) - Licence cost comparison**

Two collaboration platforms are quoted for 1,500 users. Platform A costs £8.50 per user per month. Platform B costs £96 per user per year plus a flat £18,000 annual service charge. Which is cheaper over one year, and by how much?

A. Platform A, by £9,000
B. Platform B, by £9,000
C. Platform A, by £18,000
D. Platform B, by £4,500

**Correct answer: A.**

**Explanation:** Platform A: £8.50 × 12 = £102 per user per year; × 1,500 users = £153,000. Platform B: £96 × 1,500 = £144,000; plus £18,000 service charge = £162,000. Difference: £162,000 − £153,000 = £9,000 in favour of Platform A. The trap is anchoring on the per-user figures alone (£96 < £102 suggests B) and forgetting the flat charge - a miniature version of the whole-life-cost discipline your commercial perspective skill demands. Always normalise both options to the same total, same period, before comparing.

**Question 3 (moderate) - Quantifying reuse savings**

Five programmes each plan to build their own document-processing capability at £320,000 per build. A shared capability would cost £700,000 to build once, plus £40,000 per programme to integrate. How much would the shared approach save across all five programmes?

A. £900,000 B. £700,000 C. £1,100,000 D. £500,000

**Correct answer: B.**

**Explanation:** Cost of five separate builds: 5 × £320,000 = £1,600,000. Cost of the shared approach: £700,000 + (5 × £40,000) = £700,000 + £200,000 = £900,000. Saving: £1,600,000 − £900,000 = £700,000. Distractor A is the shared-approach total cost mistaken for the saving - a classic misread of what the question asks. This is the core arithmetic behind your duty to recommend reuse to achieve value for money: the argument that persuades an investment board is precisely this calculation, stated with both totals visible so the board can verify it in seconds.

**Question 4 (moderate) - Cloud consumption dashboard**

Your quarterly cloud report shows (figures in £ thousands):

| Portfolio | Q1 spend | Q2 spend | Committed discount applied? |
|---|---|---|---|
| Citizen services | 180 | 216 | Yes |
| Case management | 240 | 228 | Yes |
| Data platform | 120 | 162 | No |
| Corporate systems | 60 | 66 | Yes |

Which portfolio had the largest *percentage* increase in spend from Q1 to Q2?

A. Citizen services B. Case management C. Data platform D. Corporate systems

**Correct answer: C.**

**Explanation:** Calculate each change relative to Q1. Citizen services: (216 − 180) ÷ 180 = 36 ÷ 180 = 20%. Case management: (228 − 240) ÷ 240 = −5% (a decrease). Data platform: (162 − 120) ÷ 120 = 42 ÷ 120 = 35%. Corporate systems: (66 − 60) ÷ 60 = 10%. The largest percentage increase is the data platform at 35%, even though citizen services grew more in absolute pounds (£36k versus £42k - actually data platform also grew more absolutely; check both when options are close). The discount column is deliberate noise: it invites a story ("no discount explains the growth") but the question asks only for the percentage calculation. Extracting the relevant columns and ignoring narrative bait is a scored behaviour in dashboard-based items.

**Question 5 (moderate) - Weighted supplier evaluation**

Your evaluation model weights criteria: technical fit 40%, cost 30%, exit provisions 20%, sustainability 10%. Two suppliers score (out of 100 per criterion):

| Criterion | Supplier X | Supplier Y |
|---|---|---|
| Technical fit | 80 | 70 |
| Cost | 60 | 85 |
| Exit provisions | 70 | 60 |
| Sustainability | 50 | 90 |

What are the weighted totals, and who wins?

A. X: 69, Y: 74.5 - Y wins
B. X: 69, Y: 74.5 - X wins
C. X: 65, Y: 76.25 - Y wins
D. X: 69, Y: 76.5 - Y wins

**Correct answer: A.**

**Explanation:** Supplier X: (80 × 0.4) + (60 × 0.3) + (70 × 0.2) + (50 × 0.1) = 32 + 18 + 14 + 5 = 69. Supplier Y: (70 × 0.4) + (85 × 0.3) + (60 × 0.2) + (90 × 0.1) = 28 + 25.5 + 12 + 9 = 74.5. Y wins on the weighted model despite X's stronger technical fit, because Y's advantages sit in heavily and moderately weighted criteria (cost) and a lightly weighted one where the gap is large (sustainability). Note how option B pairs correct arithmetic with the wrong conclusion - always read the full option, not just the numbers. Weighted scoring is the standard machinery of public sector procurement evaluation, so fluency here directly serves your supplier-selection duties.

**Question 6 (moderate) - Portfolio investment ratio**

The change budget of £18m is allocated across three horizons in the ratio 3:2:1 (run-improvement : transformation : innovation). The innovation allocation is then cut by a third. How much does innovation receive?

A. £3m B. £2m C. £1m D. £4m

**Correct answer: B.**

**Explanation:** The ratio 3:2:1 has 3 + 2 + 1 = 6 parts, so one part = £18m ÷ 6 = £3m. Innovation initially receives one part: £3m. A cut of one third removes £3m × 1/3 = £1m, leaving £2m. Distractor A is the pre-cut figure; distractor C is the size of the cut mistaken for the remainder. Ratio-then-adjustment questions are two-step by design: candidates under time pressure frequently stop after the first step, so make it a habit to re-read the question stem after calculating - "how much does innovation receive?" refers to the post-cut position.

**Question 7 (moderate) - Build versus buy over five years**

Building a capability in-house costs £900,000 up front plus £150,000 per year to run. Buying a product costs £120,000 up front plus £280,000 per year in licences and support. Over a five-year appraisal period, which option is cheaper, and by how much?

A. Build, by £130,000
B. Buy, by £130,000
C. Build, by £470,000
D. They cost the same

**Correct answer: B.**

**Explanation:** Compute both whole-life totals. Build: £900,000 + (5 × £150,000) = £900,000 + £750,000 = £1,650,000. Buy: £120,000 + (5 × £280,000) = £120,000 + £1,400,000 = £1,520,000. Buy is cheaper by £1,650,000 − £1,520,000 = £130,000. Cross-check with the difference method: the up-front difference favours Buy by £780,000; the annual run-cost difference favours Build by £130,000 per year; break-even is therefore £780,000 ÷ £130,000 = 6 years. Over a five-year appraisal period, Build has not yet caught up, so Buy wins by £780,000 − (5 × £130,000) = £130,000 - the same answer by both routes. The strategic point matters as much as the arithmetic: the appraisal period drives the conclusion. At six years the options are equal, and beyond six the build option wins. Flagging that sensitivity - "this recommendation reverses if the service lives longer than six years" - is exactly the value a lead enterprise architect adds to an investment board discussion, because whole-life horizons for government services are frequently longer than standard appraisal windows.

**Question 8 (challenging) - Cost per transaction with demand growth**

A legacy service processes 2.0 million transactions a year at a run cost of £3.2m. The replacement platform will cost £2.6m a year to run and is expected to handle 25% more transactions as digital uptake grows. What is the cost per transaction for each, and what is the percentage reduction?

A. £1.60 vs £1.04; 35% reduction
B. £1.60 vs £1.30; 18.75% reduction
C. £1.60 vs £1.04; 56% reduction
D. £1.28 vs £1.04; 18.75% reduction

**Correct answer: A.**

**Explanation:** Legacy: £3,200,000 ÷ 2,000,000 = £1.60 per transaction. Replacement volume: 2,000,000 × 1.25 = 2,500,000 transactions. Replacement: £2,600,000 ÷ 2,500,000 = £1.04 per transaction. Reduction: (1.60 − 1.04) ÷ 1.60 = 0.56 ÷ 1.60 = 35%. Distractor B forgets the volume growth (2.6 ÷ 2.0 = £1.30). Distractor C divides by the wrong base (0.56 ÷ 1.04 ≈ 54-56%). Unit-cost framing is one of the most persuasive value-for-money arguments available to you, because it captures both the numerator (cheaper platform) and denominator (scalability absorbing growth) - the two halves of your duty to recommend scalability and value for money in one metric.

**Question 9 (challenging) - Architecture community capacity**

You lead a community of enterprise and domain architects. Your coverage model requires 1 architect full-time-equivalent (FTE) per 2 major programmes and 1 FTE per 5 minor projects. The portfolio contains 8 major programmes and 15 minor projects. You have 6 architects, but one is seconded half-time to a cross-government initiative and another spends 20% of their time on community development. How many FTEs short (or over) are you?

A. 1.7 FTEs short B. 0.7 FTEs short C. Exactly sufficient D. 1.0 FTE short

**Correct answer: A.**

**Explanation:** Calculate demand first. Major programmes: 8 ÷ 2 = 4.0 FTEs. Minor projects: 15 ÷ 5 = 3.0 FTEs. Total demand = 7.0 FTEs. Now supply: 6 architects = 6.0 FTEs nominal. Deduct the half-time secondment (−0.5) and the 20% community development commitment (−0.2): available supply = 6.0 − 0.5 − 0.2 = 5.3 FTEs. Shortfall = 7.0 − 5.3 = 1.7 FTEs. Distractor B counts only the secondment and the community time as the shortfall itself; distractor D rounds the deductions and forgets one of them. Two further points make this more than an arithmetic drill. First, in a real resourcing case, define what counts as available capacity *before* calculating - a reviewer could argue community development is funded demand rather than a supply deduction, and that definitional choice, not the arithmetic, is what finance and HR colleagues will challenge. Second, the answer is the opening of a leadership conversation, not the end: a 1.7 FTE gap against a 7.0 FTE demand is roughly 24% under-coverage, which you might address through prioritisation of programmes, recruitment, or developing capability in the community - all levers explicitly within your role.

**Question 10 (challenging) - Sustainability metrics**

Your hosting estate consumes 1,200 MWh a year, of which 65% is attributable to legacy data centres and the rest to cloud. The decommissioning plan will cut legacy consumption by 40% in year one. Cloud consumption will rise by 10% in the same year. What is the estate's total consumption after year one?

A. 930 MWh B. 1,020 MWh C. 900 MWh D. 942 MWh

**Correct answer: A.**

**Explanation:** Legacy share: 1,200 × 0.65 = 780 MWh. Cloud share: 1,200 − 780 = 420 MWh. After year one: legacy = 780 × 0.60 = 468 MWh; cloud = 420 × 1.10 = 462 MWh. Total = 468 + 462 = 930 MWh. Distractor B applies the 40% cut to only half of legacy or mixes the percentages; distractor C applies a flat 25% cut to the whole estate. The strategic insight embedded in the numbers is worth noticing: after one year, cloud and legacy consumption are nearly equal, so the second year's sustainability narrative must shift from "kill legacy" to "optimise cloud" - the kind of inflection point your horizon scanning should surface before the annual report does. Sustainability arithmetic increasingly appears in public sector investment cases, and your recommendation duty explicitly includes sustainability alongside reuse and scalability.

**Question 11 (challenging) - Multi-year decommissioning savings**

Decommissioning a legacy estate costs £1.8m spread evenly over years one and two. It eliminates run costs of £1.1m per year from the start of year two. Ignoring discounting, in which year does the cumulative position first turn positive (savings exceed costs)?

A. Year 2 B. Year 3 C. Year 4 D. Year 5

**Correct answer: B.**

**Explanation:** Track the cumulative position year by year. Year 1: costs £0.9m, savings £0 → cumulative −£0.9m. Year 2: costs £0.9m, savings £1.1m → net +£0.2m in-year; cumulative −£0.9m + £0.2m = −£0.7m. Year 3: no further costs, savings £1.1m → cumulative −£0.7m + £1.1m = +£0.4m. The cumulative position first turns positive in year 3. Distractor A rewards noticing the first positive in-year figure (year 2) and confusing it with the cumulative break-even - a distinction that matters enormously in investment cases, where a programme can be "profitable this year" yet still under water overall. Being crisp about cumulative versus in-year positions is part of making your long-term strategy financially credible to the senior stakeholders you network with.

**Question 12 (moderate) - Reading percentage points correctly**

A dashboard reports that reuse of shared components across new services rose from 32% to 44% after your reference architecture was mandated. Which statement is accurate?

A. Reuse rose by 12%
B. Reuse rose by 12 percentage points, a 37.5% relative increase
C. Reuse rose by 44%
D. Reuse rose by 37.5 percentage points

**Correct answer: B.**

**Explanation:** The absolute change is 44 − 32 = 12 *percentage points*. The relative change is 12 ÷ 32 = 0.375 = 37.5%. Option A commits the ubiquitous points-versus-percent conflation; C confuses the new level with the change; D swaps the two correct numbers. This distinction is not pedantry: "reuse rose 12%" and "reuse rose 37.5%" tell a board two very different stories about the same data, and as the leader who owns the enterprise architecture strategy, the credibility of your metrics narrative depends on using these terms precisely - and on gently correcting them when a paper you are assuring does not.

**Question 13 (moderate) - Programme performance metrics**

A quarterly portfolio report shows delivery confidence across your programmes:

| Quarter | Programmes rated Green | Amber | Red | Total |
|---|---|---|---|---|
| Q1 | 6 | 8 | 2 | 16 |
| Q2 | 9 | 7 | 4 | 20 |

A board member claims: "Delivery confidence has improved - Green programmes are up 50%." Is the proportion of Green programmes actually higher in Q2?

A. Yes - Green rose from 37.5% to 45% of the portfolio
B. No - Green fell as a proportion because the portfolio grew
C. Yes - Green rose from 30% to 56%
D. Cannot be calculated from the table

**Correct answer: A.**

**Explanation:** Q1 Green proportion: 6 ÷ 16 = 37.5%. Q2 Green proportion: 9 ÷ 20 = 45%. So the proportion genuinely improved, and the board member's absolute claim is also arithmetically true (6 → 9 is a 50% rise in count). But run the same check on Red: 2 ÷ 16 = 12.5% in Q1 versus 4 ÷ 20 = 20% in Q2 - Red *doubled* in count and rose as a proportion too. The portfolio polarised: more Green and more Red, with Amber shrinking from 50% to 35%. The assessed skill is refusing to let one favourable statistic stand in for the whole picture. When you assure portfolio reporting for senior stakeholders, insisting that proportions accompany counts - and that all rating movements are shown, not just the flattering one - is basic numerical hygiene that protects the board from a partially true narrative.

**Question 14 (challenging) - Contract pricing tiers**

A supplier's API gateway contract prices monthly calls in tiers: the first 10 million calls at £0.020 per call, the next 20 million at £0.012 per call, and all further calls at £0.008 per call. Your integration strategy forecasts 42 million calls per month once three departments share the platform. What is the forecast monthly cost?

A. £336,000 B. £536,000 C. £456,000 D. £344,000

**Correct answer: B.**

**Explanation:** Work the tiers in order. Tier 1: 10,000,000 × £0.020 = £200,000. Tier 2: 20,000,000 × £0.012 = £240,000. Tier 3: the remaining 42 − 10 − 20 = 12 million calls at £0.008 = £96,000. Total: £200,000 + £240,000 + £96,000 = £536,000. Distractor A prices all 42 million calls at the top-tier rate of £0.008 - the "marginal rate" fallacy familiar from income tax confusion, and by far the most common error with tiered pricing. Distractor C misallocates the tier boundaries. Note the commercial insight the correct structure reveals: the *average* cost per call is £536,000 ÷ 42,000,000 ≈ £0.0128, while the *marginal* cost of the next call is £0.008. When you advocate consolidating more departments onto the shared platform - reuse achieving value for money - the marginal rate is your argument: each additional consumer joins at the cheapest tier, making the per-call economics better for everyone. Fluency with tiered pricing is core to identifying appropriate contractual frameworks and evaluating suppliers.

**Question 15 (moderate) - Averages and what they hide**

Your architecture review board's cycle-time report says decisions took an average of 12 working days last quarter, against a 15-day service standard. The underlying data for the 10 decisions is: 3, 4, 4, 5, 5, 6, 7, 8, 28, 50 days. A colleague concludes: "We're comfortably within standard." Which statement best characterises the position?

A. The conclusion is sound - the average of 12 days is under the 15-day standard
B. The conclusion is misleading - the median is 5.5 days but two decisions breached the standard badly, and 20% of decisions breaching is the real story
C. The report is arithmetically wrong - the average of these figures is not 12
D. The median of 12 days shows typical performance is at the limit of the standard

**Correct answer: B.**

**Explanation:** First verify the arithmetic: 3 + 4 + 4 + 5 + 5 + 6 + 7 + 8 + 28 + 50 = 120; 120 ÷ 10 = 12, so the average is correct and C fails. The median (average of the 5th and 6th values: (5 + 6) ÷ 2 = 5.5 days) shows typical decisions are fast - so D misstates the median. But two decisions took 28 and 50 days, both breaching the 15-day standard: 2 of 10 is a 20% breach rate, and the 50-day case is more than three times the standard. Option A is arithmetically true and managerially hollow: an average comfortably under target can coexist with a fifth of customers experiencing serious breaches, because the many fast decisions subsidise the mean. B captures the full picture. The professional application is immediate: when you report governance performance to senior stakeholders, pair the average with the distribution - median, breach count and worst case - or the report will assure everyone while the two aggrieved programme directors brief against your design authority in the corridor.

### Preparation tips

- **Rebuild the reflexes, not the theory.** You almost certainly know percentages, ratios and weighted averages; what decays is speed. Do short daily drills for a week or two before any assessment - ten questions in fifteen minutes - rather than a single long cramming session.
- **Always identify the baseline.** Most wrong answers in percentage questions come from dividing by the wrong figure. Say to yourself: change relative to what?
- **Normalise before comparing.** Convert all options to the same units, the same period and the same scope (per user, per year, whole-life) before judging which is bigger.
- **Use the calculator for arithmetic, not for thinking.** Set up the calculation on paper or in your head first; the calculator then just executes. Candidates who "explore" with the calculator burn time.
- **Practise with your own management information.** Take a real cloud consumption report or portfolio dashboard and generate three questions from it. As a leader you will also find this doubles as excellent coaching material for the architects you develop.
- **Bank the easy marks.** Answer the one-step items quickly and confidently, leaving time for multi-step total-cost and break-even questions.

### Common pitfalls

- **Misreading scale qualifiers.** "£ thousands", "MWh", "per quarter" - a missed qualifier wrecks an otherwise perfect calculation. Read table headers and footnotes first.
- **Confusing percentage points with percentages.** As Question 12 shows, this is the most common numeracy error in management reporting, and test writers know it.
- **Stopping after step one.** Two-step questions (ratio then adjustment, total then difference) are designed so that the intermediate result appears among the options.
- **Anchoring on headline prices.** Per-unit prices without flat charges, up-front costs without run costs, in-year savings without cumulative positions - each is a half-truth the full calculation corrects.
- **Time-sink questions.** A single complex break-even item can consume five questions' worth of time. Flag, skip, return.
- **Over-calculating.** Sometimes rounding and estimation identify the only plausible option in seconds; precision to the pound is not always required to select A over C.


## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment evaluates how well you understand, analyse and draw correct conclusions from written business information, using passages that mirror the reading demands of your actual role. For a lead enterprise architect, that means standards documents, governance policies, board papers, supplier correspondence, strategy extracts and horizon-scanning reports - dense, formal texts where a single qualifier changes the meaning.

The dominant format asks you to judge statements against a passage as **True** (the passage logically entails the statement), **False** (the passage logically contradicts the statement), or **Cannot Say** (the passage provides insufficient information either way). The discipline is strict: you answer from the text alone, setting aside everything you know from experience. Some assessments add multiple-choice comprehension items - identifying the best summary, the author's core argument, or the precise scope of a stated rule. Timing is tight, often under a minute per question, simulating the reality of absorbing a board paper minutes before you must speak to it.

This strictness is not artificial. As the owner of architectural principles, policies and standards, you are professionally accountable for what documents *actually say*, as distinct from what their authors meant or what readers assume. Assurance, in the end, is verbal reasoning applied with consequences.

### What it measures for your role

Mapped to your role profile, verbal items test:

- **Architecture communication**: before you can communicate with technical and non-technical stakeholders at all levels, or mediate difficult architectural discussions, you must first extract precisely what a text claims - and register what it deliberately does not claim. Misreading a position paper before mediating a dispute is fatal to the mediation.
- **Making architectural decisions** and governance: standards and policies are texts. Judging whether a proposal complies means reading both with precision, including scope clauses, exceptions and definitions.
- **Problem definition and shaping**: distinguishing what a problem statement asserts from what it assumes is the verbal core of challenging requirements and assumptions - a coaching behaviour named explicitly in your skills.
- **Architect for the whole context**: horizon-scanning sources - industry reports, analyst notes, policy consultations - reward readers who separate evidenced findings from vendor spin and speculation.
- **Commercial perspective**: contract schedules and supplier responses are precisely the genre where "shall", "may", "reasonable endeavours" and "subject to" carry financial weight.

### Practice questions

**Passage A - Extract from a draft hosting standard**

*"All new digital services must be hosted on the department's approved cloud platforms unless a written exemption is granted by the design authority. Exemptions will normally be granted only where a service processes data classified above OFFICIAL, or where a statutory obligation requires physical hosting within a specified facility. Services hosted under an exemption must be reviewed annually. Existing services are out of scope of this standard, but owners of existing services are encouraged to plan migration to approved platforms as part of their lifecycle planning. This standard does not apply to services operated by arm's-length bodies."*

**Question 1 (easy) - True / False / Cannot Say**

"A new digital service processing OFFICIAL data must be hosted on an approved cloud platform unless it holds a written exemption."

**Correct answer: True.**

**Explanation:** The first sentence states the rule for all new digital services: approved platforms unless a written exemption is granted. A service processing OFFICIAL data is a new digital service like any other; the passage's mention of data "classified above OFFICIAL" concerns when exemptions are *normally granted*, not who the baseline rule covers. The statement simply restates the rule as applied to one case, so the passage entails it. Notice how the classification detail tempts you to overthink an easy item - the rule sentence alone answers the question.

**Question 2 (moderate) - True / False / Cannot Say**

"An exemption cannot be granted to a service that processes only OFFICIAL data and has no statutory hosting obligation."

**Correct answer: False.**

**Explanation:** The passage says exemptions "will *normally* be granted only where" the two conditions apply. "Normally" explicitly leaves room for abnormal cases: the text contemplates exemptions outside the two listed grounds, even if they are unusual. The statement's "cannot" asserts an absolute prohibition, which the passage contradicts by its own qualifier. This is the single most examined word-class in verbal reasoning - modal and frequency qualifiers ("normally", "may", "typically", "in most cases") - and it is also the language of every real standard you will ever draft or assure. If the drafter had meant an absolute rule, the word "normally" would not be there; as a standards owner, you would either strike the word or accept the discretion it creates.

**Question 3 (moderate) - True / False / Cannot Say**

"The majority of the department's existing services do not run on approved cloud platforms."

**Correct answer: Cannot Say.**

**Explanation:** The passage places existing services out of scope and encourages migration planning, but it gives no information about how many existing services currently run on approved platforms. The encouragement to migrate might *suggest* some do not, but suggestion is not entailment, and "the majority" is a quantified claim the text nowhere supports or denies. Candidates who work in real departments often "know" the answer from experience - and that outside knowledge is precisely what the Cannot Say option exists to catch. Answer from the four corners of the text.

**Question 4 (moderate) - Multiple choice**

Which of the following services is clearly outside the scope of the standard?

A. A new service processing data above OFFICIAL
B. A new service run by an arm's-length body
C. An exempted service awaiting annual review
D. A new service with a statutory hosting obligation

**Correct answer: B.**

**Explanation:** The final sentence excludes services operated by arm's-length bodies from the standard entirely. Option A is within scope - it is a candidate for exemption, which is a mechanism *of* the standard, not an escape from it; the same logic covers D. Option C is squarely governed by the standard's annual review requirement. The distinction between "out of scope" and "in scope but exempted" is one professionals blur constantly, and blurring it has governance consequences: exempted services carry obligations (annual review), whereas out-of-scope services carry none under this text. Precision about scope clauses is bread-and-butter work when you establish and assure architectural policies.

**Passage B - Email from a programme director**

*"Thank you for your team's assurance report on our casework programme. We accept the finding that our integration design deviates from the published API standard. However, we do not accept that remediation must be completed before our beta assessment. The standard itself was updated after our alpha phase began, and our supplier has confirmed that conforming now would add at least twelve weeks to the schedule and approximately £400,000 in cost. We propose instead a time-bound exception, with remediation scheduled for the first quarter after national rollout. We would welcome the design authority's early view, since our beta assessment is booked for 14 November and our contract with the supplier includes a break clause that must be exercised, if at all, by 30 September."*

**Question 5 (easy) - True / False / Cannot Say**

"The programme director denies that the integration design deviates from the API standard."

**Correct answer: False.**

**Explanation:** The email says the opposite in terms: "We accept the finding that our integration design deviates from the published API standard." What the director disputes is not the deviation but the *timing of remediation*. Separating "accepts the finding, disputes the consequence" is a fundamental reading skill for anyone who mediates architectural disputes: the parties usually agree on more than their tone suggests, and identifying the genuinely contested proposition - here, remediation before beta versus after rollout - is the first act of mediation.

**Question 6 (challenging) - True / False / Cannot Say**

"Conforming to the standard before beta would cost the programme £400,000."

**Correct answer: Cannot Say.**

**Explanation:** Read the provenance and the hedging carefully. The £400,000 figure is (a) the *supplier's* confirmation, not an established fact the email author verifies; and (b) qualified as "approximately", attached to conforming "now". The passage tells you what the supplier *has claimed*; it does not entail that the claim is true. A statement that "the supplier has stated conforming would cost approximately £400,000" would be True; the statement as written asserts the cost as fact, which the text neither establishes nor contradicts - hence Cannot Say. This distinction is commercially loaded: suppliers quoting the cost of compliance have an interest in the number, and a lead enterprise architect assessing an exception request should notice that the only cost evidence in play is the interested party's own estimate.

**Question 7 (challenging) - Multiple choice**

Which pair of dates creates the time pressure the director wants the design authority to appreciate?

A. The alpha start date and the beta assessment date
B. The beta assessment date and the rollout date
C. The break clause deadline and the beta assessment date
D. The standard's update date and the break clause deadline

**Correct answer: C.**

**Explanation:** The email closes by juxtaposing two hard dates: the beta assessment "booked for 14 November" and a supplier break clause that "must be exercised, if at all, by 30 September". The design authority's view is needed early because the programme must decide whether to keep or break the supplier contract *before* it knows the beta outcome - the break deadline precedes the assessment by six weeks. That is the squeeze. Option A describes background (when the standard changed relative to alpha), relevant to the fairness argument but not the deadline pressure; B involves a rollout date the email never gives; D pairs dates the email does not connect. Extracting the operative deadline structure from polite prose is exactly the skill you deploy when senior stakeholders write to you seeking decisions - the request is rarely in the sentence that looks most important.

**Passage C - Extract from a technology strategy board paper**

*"The strategy commits us to reducing the number of case-management systems from eleven to three by the end of the spending review period. Consolidation will proceed portfolio by portfolio, beginning with the two portfolios whose systems share a common supplier. Savings are projected at £6.2m per year once consolidation completes, though the paper's sensitivity analysis shows savings could fall to £3.9m if data migration proves more complex than the discovery phase indicated. No service will be migrated during its statutory peak period. The board is asked to note that this consolidation depends on the identity programme delivering federation capability by the third quarter; should that slip, the timeline, but not the target, would need to be revised."*

**Question 8 (easy) - True / False / Cannot Say**

"The strategy aims to reduce the number of case-management systems by eight."

**Correct answer: True.**

**Explanation:** Eleven systems reducing to three is a reduction of 11 − 3 = 8. The statement paraphrases the commitment arithmetically rather than verbatim, and paraphrase-with-arithmetic is a standard verbal-item device: the passage entails the statement even though the number eight never appears in the text. Verify the subtraction rather than scanning for the literal figure - scanning would wrongly suggest Cannot Say.

**Question 9 (moderate) - True / False / Cannot Say**

"If the identity programme's federation capability is delayed, the consolidation target of three systems will be reduced."

**Correct answer: False.**

**Explanation:** The final sentence addresses this exact contingency: should the identity capability slip, "the timeline, but not the target, would need to be revised". The statement claims the *target* would change; the passage states the target would not. The sentence's structure - "the timeline, but not the target" - is a contrastive construction that assessment writers love, because a hurried reader registers "revised" and misses which noun it governs. In board papers, these contrastive clauses often carry the paper's real risk position; reading them precisely is part of assuring that decisions are aligned with strategy.

**Question 10 (challenging) - True / False / Cannot Say**

"Annual savings from consolidation will be at least £3.9m."

**Correct answer: Cannot Say.**

**Explanation:** The paper *projects* £6.2m and shows a sensitivity case of £3.9m if migration proves more complex. Projections and sensitivity ranges are statements about expectations, not guarantees about outcomes; the text does not entail that actual savings will reach even the lower figure - migration could be worse than the modelled sensitivity, the consolidation could fail, or costs could change for unmodelled reasons. Nor does the passage contradict the statement. So the honest verdict is Cannot Say. This is a subtle but important calibration: treat modelled floors as facts and you will misbrief your board. The passage licenses "savings are projected between £3.9m and £6.2m", nothing stronger - and a lead enterprise architect's credibility with finance colleagues rests on exactly this discipline about what numbers do and do not promise.

**Question 11 (moderate) - Multiple choice**

Which factor determines the order in which portfolios are consolidated first?

A. The size of projected savings in each portfolio
B. Whether the portfolios' systems share a common supplier
C. The complexity of each portfolio's data migration
D. Each portfolio's statutory peak period

**Correct answer: B.**

**Explanation:** The passage states consolidation begins "with the two portfolios whose systems share a common supplier". Option D governs *when migrations may not occur* (not during statutory peaks) - a constraint on scheduling, not on ordering priority; C appears only in the sensitivity analysis; A is never linked to sequencing. Multiple-choice comprehension items often work this way: every option quotes something genuinely in the passage, and the test is whether you attach each fact to the right question. It is the same skill as reading a programme plan and knowing which constraint drives the critical path and which merely shapes it.

**Passage D - Extract from an industry horizon-scanning report**

*"Across the public sector, adoption of AI-assisted decision-support tooling has moved from pilots to production in at least a dozen large organisations this year. Vendors claim productivity gains of 20 to 40 per cent in casework triage, although independent evaluations remain scarce and two published studies report gains at the lower end of that range only after significant process redesign. Regulators have signalled that assurance frameworks for algorithmic decision support are likely within two years. Organisations that have established cross-functional architecture and data governance forums report smoother adoption than those treating AI tooling as a conventional software procurement."*

**Question 12 (moderate) - True / False / Cannot Say**

"Independent evaluations confirm productivity gains of 20 to 40 per cent in casework triage."

**Correct answer: False.**

**Explanation:** The 20-40% range is what *vendors claim*. The passage then explicitly undercuts the statement: independent evaluations are scarce, and the two that exist report gains "at the lower end of that range only after significant process redesign". Independent evidence therefore does not confirm the full claimed range - the passage contradicts the statement's attribution of the 20-40% figure to independent evaluation. Distinguishing vendor claims from independent evidence is the very heart of horizon scanning done well; a lead enterprise architect who briefs a board with vendor numbers presented as verified findings has failed at exactly the point this item tests.

**Question 13 (moderate) - True / False / Cannot Say**

"Regulatory assurance frameworks for algorithmic decision support will be introduced within two years."

**Correct answer: Cannot Say.**

**Explanation:** The passage reports that regulators "have signalled" frameworks are "likely within two years". Signals of likelihood are neither promises nor facts: the statement converts a hedged forecast into a definite future event, which the text neither entails nor contradicts. Compare Question 12, where the text actively undercut the claim - here it simply stops short of the claim. Getting the True/False/Cannot Say boundary right in forecast-laden text is a distinctive senior-level skill, because your strategy documents must respond to likely futures without asserting them; you would write "we anticipate regulatory assurance requirements and are building capacity accordingly", never "regulation arrives in 2028".

**Question 14 (challenging) - Multiple choice**

Which conclusion is best supported by the passage as a whole?

A. AI-assisted tooling should be procured like conventional software to control cost
B. Organisations with cross-functional governance forums are better positioned to adopt AI tooling
C. Productivity gains from AI tooling are guaranteed after process redesign
D. Regulators have prohibited algorithmic decision support pending assurance frameworks

**Correct answer: B.**

**Explanation:** The final sentence states that organisations with cross-functional architecture and data governance forums "report smoother adoption" - directly supporting B, and only B. Option A contradicts the same sentence, which frames conventional-procurement treatment as the *less* successful pattern. C converts "two studies report gains... after significant process redesign" into a guarantee, a double overreach (two studies, and "report" not "guarantee"). D invents a prohibition from a signal about future frameworks. Note how the correct option is also the modest one: "better positioned" mirrors the passage's careful "report smoother adoption". In best-supported-conclusion items, the option whose strength matches the evidence's strength usually wins - the same calibration you apply when turning horizon-scanning material into strategy recommendations.

**Passage E - Extract from a supplier's contract schedule**

*"The Supplier shall provide exit assistance for a period of six months from the date of any termination notice, at the day rates set out in Schedule 4. Exit assistance shall include the extraction of all Customer Data in an open, documented format, and knowledge transfer sessions not exceeding twenty days in aggregate. The Supplier may, at its discretion, provide additional transition services beyond those described in this Schedule, subject to agreement of a statement of work. Nothing in this Schedule obliges the Supplier to license, or to procure the licensing of, any proprietary tooling to the Customer or to any replacement supplier. For the avoidance of doubt, the obligations in this Schedule survive expiry of the Agreement."*

**Question 15 (moderate) - True / False / Cannot Say**

"The supplier is obliged to provide knowledge transfer sessions totalling twenty days."

**Correct answer: False.**

**Explanation:** The schedule obliges knowledge transfer "not exceeding twenty days in aggregate" - twenty days is a *ceiling*, not a commitment. The statement converts a maximum into an entitlement of exactly twenty days, which the text contradicts: the supplier could discharge the obligation with substantially fewer days provided knowledge transfer is genuinely included. Ceilings dressed as promises are among the most expensive misreadings in commercial documents, and spotting them is central to your skill in identifying appropriate contractual frameworks. If your exit plan assumes twenty days, your plan rests on words the contract does not contain.

**Question 16 (challenging) - True / False / Cannot Say**

"If the agreement expires without a termination notice, the supplier has no exit assistance obligations."

**Correct answer: Cannot Say.**

**Explanation:** Two clauses pull in different directions and neither settles the question. The first sentence ties the six-month assistance *period* to "the date of any termination notice", suggesting notice triggers the clock; the final sentence says the schedule's obligations "survive expiry of the Agreement", suggesting obligations exist in expiry scenarios too - but the text never states what starts the assistance period, or what assistance is owed, when the agreement simply expires. The passage neither entails nor contradicts the statement; it is genuinely underspecified, which is itself the professionally important discovery. In a real supplier evaluation you would flag this drafting gap for commercial colleagues before signature, because ambiguity discovered at exit time is negotiating leverage handed to the supplier.

**Question 17 (moderate) - Multiple choice**

A replacement supplier asks whether they will receive licences for the incumbent's proprietary migration tooling. Based only on the schedule, the accurate answer is:

A. Yes - exit assistance includes all tooling needed for transition
B. Yes - but only for six months from the termination notice
C. No - the schedule expressly states the supplier is not obliged to license proprietary tooling to a replacement supplier
D. The schedule does not address tooling for replacement suppliers

**Correct answer: C.**

**Explanation:** The fourth sentence answers directly: "Nothing in this Schedule obliges the Supplier to license, or to procure the licensing of, any proprietary tooling to the Customer *or to any replacement supplier*." Option D fails precisely because the schedule *does* address the point - candidates who skim past the double-negative construction ("nothing... obliges") often mistake an express carve-out for silence. A and B assert entitlements the text disclaims. Note the practical consequence a lead enterprise architect would draw: since proprietary tooling is not owed, your exit strategy must rest on the obligations that *are* owed - open-format data extraction and documented knowledge transfer - which is an argument for designing architectures that never depend on the incumbent's tooling in the first place.

### Preparation tips

- **Read the statement before re-reading the passage.** Identify the exact claim being tested, then hunt the passage for entailment or contradiction. Reading the passage exhaustively first wastes time on tight limits.
- **Interrogate qualifiers.** Circle (mentally) every "normally", "may", "at least", "only", "unless", "likely" - the answer almost always turns on one of them. This mirrors how you should read standards you assure.
- **Rehearse the Cannot Say discipline.** The hardest habit for experienced leaders is suppressing what you know. Practise saying: "true in the world, perhaps - but is it in this text?"
- **Distinguish claims from attributed claims.** "X is true" and "the supplier states X" are different propositions. Track who asserts what, exactly as you would in a contested design review.
- **Practise on your genre.** Spend fifteen minutes with a real standard, board paper or analyst report, drafting three True/False/Cannot Say statements about it. Writing items is the fastest way to internalise how they work - and produces coaching material for your architecture community.
- **Keep pace steady.** Under one minute per question means one careful pass, one decision, no lingering. Trust your first well-reasoned judgement.

### Common pitfalls

- **Importing outside knowledge.** Your expertise in government hosting, procurement and AI policy is an asset everywhere except here. The test measures reading, not knowledge, and marks your knowledge as error when it overrides the text.
- **Confusing "likely" with "will".** Forecast language converted into certainty - in either direction - is the most common cause of wrong True/Cannot Say calls in strategy-flavoured passages.
- **Missing contrastive structure.** "The timeline, but not the target" - hurried readers attach the verb to the wrong noun. Slow down at commas.
- **Treating suggestion as entailment.** A passage that encourages migration does not state that migration has not happened; implication you infer is not information the text gives.
- **Scanning for literal words.** Paraphrase and arithmetic restatement ("reduce by eight") defeat keyword scanning; verify meaning, not vocabulary.
- **Answer pattern anxiety.** Three Cannot Says in a row feels wrong and drives second-guessing. Distributions are not evidence; judge each item independently.


## Workplace job-specific situational judgement assessment

### About this assessment

A workplace job-specific situational judgement assessment evaluates decision-making, interpersonal effectiveness and professional conduct by presenting realistic dilemmas from your working world and asking how you would respond. Unlike cognitive, numeric or verbal tests, there is often no single objectively right answer; instead, responses are scored against what effective performance looks like for this role in this culture. Formats include choosing the **most effective** and **least effective** actions from a set, or ranking all options from best to worst. Timing is usually generous or absent, because the instrument measures natural judgement rather than speed.

For a lead enterprise architect in UK government, the scoring frame is well defined even where answers are debatable: Civil Service values (integrity, honesty, objectivity, impartiality), the public sector's commitment to user needs, accessibility, inclusion and transparency, and the behaviours your role profile names - gaining support for high-risk architectural positions, mediating difficult discussions, coaching others, collaborating across organisations, and holding the long-term strategy steady while enabling delivery at pace. Effective options tend to be active rather than passive, collaborative rather than unilateral, transparent rather than expedient, and to address root causes rather than symptoms - while remaining proportionate and politically intelligent.

The scenarios below are drawn from the stakeholder landscape you genuinely occupy: programme directors, investment boards, supplier executives, domain architects you lead, cross-government peers and delivery teams under pressure.

### What it measures for your role

Mapped to your role profile, situational items test:

- **Architecture communication**: gaining support from business and technical stakeholders for topics with high risk, impact and complexity; mediating between people in difficult architectural discussions rather than ruling by authority.
- **Community collaboration** and leading teams: developing the architecture community, adapting feedback so it is effective and lasting, spotting problems in team dynamics and stimulating the right responses.
- **Making architectural decisions**: using governance and assurance proportionately - neither bypassing it for speed nor hiding behind it to avoid a decision.
- **Strategy design** and **Enterprise architecture**: holding the enterprise vision steady under pressure from local optimisation, while staying genuinely open to evidence that the strategy needs to change.
- **Commercial perspective**: managing supplier relationships with integrity, especially where hospitality, information asymmetry or contractual pressure create ethical exposure.
- **Architect for the whole context** and **Problem definition and shaping**: responding to horizon-scanning signals proportionately, and framing problems before prescribing solutions.

### Practice questions

**Question 1 (moderate) - The resistant programme director**

A major programme is designing a bespoke customer-data store, in conflict with the enterprise strategy's designated master-data platform. The programme director tells you privately: "Your platform will slow us down by months. I'm accountable for delivery, not your roadmap. We're proceeding as planned." The programme's business case was approved before the strategy was published.

Which response is most effective, and which least effective?

A. Remind the director that the strategy is mandated, and notify the design authority that the programme is non-compliant.
B. Explore the director's delivery concerns in detail, then jointly assess what a compliant design would really cost the programme - and what transitional arrangement could work if the gap is genuine.
C. Allow the programme to proceed, noting the deviation in the architecture risk register for later remediation.
D. Escalate to the director's senior responsible owner, recommending the programme be paused until it aligns.

**Most effective: B. Least effective: C.**

**Explanation:** B does what your role profile calls gaining support for architectural topics with high risk and complexity: it treats the director's concern as data, tests whether the conflict is as stark as claimed, and looks for a transitional state - the everyday tool of enterprise architecture - that serves both delivery pace and strategic coherence. It also honours the awkward fact that the business case predates the strategy, which makes collaborative transition, not enforcement, the fair opening move. A leads with compulsion and turns a solvable design conversation into a governance confrontation; it may become necessary, but as a first move it squanders influence. D similarly escalates before engaging, spending senior capital on a dispute you have not yet tried to resolve - weak, though defensible later. C is least effective because it is passive in both directions: it neither helps the programme nor protects the enterprise, converting a live decision into silent strategic debt while appearing to act. Registers record risks; they do not manage them.

**Question 2 (moderate) - Two architects in deadlock**

Two senior domain architects in your community have argued for weeks over the integration approach for a shared capability - one favouring event streaming, the other APIs. The disagreement has turned personal: they now avoid each other's design reviews, and delivery teams are receiving contradictory guidance. Both are technically credible.

Rank the following actions from most to least effective:

A. Chair a structured session where each must present the *other's* proposal fairly, then agree evaluation criteria against the actual quality attributes required, before any decision.
B. Make the decision yourself as lead architect and instruct both to implement it.
C. Ask the two to resolve it between themselves within a fortnight and report back.
D. Split the decision by domain, letting each use their preferred approach in their own area.

**Correct ranking: A, B, C, D.**

**Explanation:** A is textbook mediation of a difficult architectural discussion: steelmanning breaks the personal deadlock by forcing each party to inhabit the other's reasoning, and agreeing criteria before deciding relocates the argument from identity to evidence - modelling exactly the coaching in architecture communication your role profile expects. B ranks second, perhaps surprisingly: teams are receiving contradictory guidance, so a clear decision has genuine value, and making guided design decisions is your job - but imposed answers leave the relationship rupture untreated and forfeit a development opportunity, so it is a serviceable second, not a first. C has the appearance of empowerment but ignores what you have observed: they have already had weeks and the dynamic has turned personal; unassisted, a fortnight more likely deepens the trench. D is least effective because it resolves the conflict by damaging the architecture - a shared capability with two integration philosophies is a fragmentation decision dressed as diplomacy, imposing permanent cost on every future consumer to avoid one difficult conversation.

**Question 3 (challenging) - The board member's conference enthusiasm**

At an investment board, a non-executive member announces they have seen "a transformative AI platform" at a conference, have arranged a follow-up with the vendor's account director, and propose the department pilot it immediately, adding: "We can't let procurement bureaucracy make us miss this." Several board members are visibly enthusiastic. You know the product category is promising, but this vendor's claims are unverified and a direct award may breach procurement rules.

Which response is most effective, and which least effective?

A. Welcome the board's appetite for the technology, and propose channelling it through a short structured market assessment that tests this vendor against alternatives and keeps the department's procurement position safe.
B. State that adopting unassessed vendor products would breach procurement rules and architectural governance, and advise the board against proceeding.
C. Stay silent in the meeting and raise concerns afterwards with the board chair privately.
D. Agree to the pilot but limit it to synthetic data so no citizen data is at risk.

**Most effective: A. Least effective: D.**

**Explanation:** A performs the distinctive lead-architect move: it preserves the genuinely valuable signal (board-level appetite for innovation, which you spend most of your time trying to create) while inserting the discipline - competitive assessment, governance, procurement propriety - that protects the department. It gains support rather than demanding compliance, and reflects your horizon-scanning duty: the category may be right even if this vendor is not. B is correct in substance but spends its correctness poorly: framing the answer purely as prohibition casts architecture and procurement as the "bureaucracy" the member complained about, hardening the room against you. C fails the moment: silent in public, critical in private is the inverse of transparent advice, and by the time you reach the chair, momentum and a vendor meeting already exist. D is least effective because it accepts the flawed premise - a sole-vendor commitment on conference enthusiasm - and merely gilds it with a technical safeguard; synthetic data protects citizens but not the procurement position, not value for money, and not the precedent that governance yields to enthusiasm. A safeguard on an unsound decision is still an unsound decision.

**Question 4 (easy) - The struggling architect**

An enterprise architect you line-manage has had two consecutive design proposals rejected by the design authority. You learn they have privately described the authority as "a rubber-stamp club that hates new ideas" and are now avoiding submitting a third proposal, letting their programme drift. They are talented but relatively new to enterprise-level work.

Which response is most effective, and which least effective?

A. Review the two rejected proposals with them, identify the specific gaps the authority cited, and offer to pre-review the third proposal together before submission.
B. Tell them the design authority's standards are non-negotiable and they need to raise their game.
C. Submit the third proposal on their behalf to shield them while they rebuild confidence.
D. Suggest they observe several design authority sessions for other proposals, then debrief with you on what successful submissions do differently.

**Most effective: A (with D a strong complement). Least effective: C.**

**Explanation:** A is direct, developmental and specific: it converts rejection into a coaching artefact, addresses the actual quality gap, and re-engages the architect with the governance process rather than around it - adapting feedback so it is "effective and lasting", in your skill profile's words. D is also genuinely strong and pairs well with A; it ranks slightly behind only because observation without addressing the two live rejections leaves the immediate programme drift and the corrosive narrative untouched. B states a truth in a way designed to be useless: it offers no path from here to competence and will likely convert private cynicism into open disengagement. C is least effective despite its kindness: it removes the learning opportunity, signals to the design authority that the architect cannot operate at level, quietly confirms the architect's belief that the process is unbeatable, and leaves you doing their job - developing the architecture community means building capability, not substituting for it.

**Question 5 (challenging) - The horizon-scanning bombshell**

Three months before a flagship case-management platform completes rollout, your horizon scanning surfaces credible evidence that the platform vendor is negotiating to be acquired by a company whose licensing practices have, elsewhere, doubled costs and closed open interfaces within two years. Nothing is confirmed publicly. The programme team is exhausted and morale is fragile; the SRO is preparing celebratory communications.

Which response is most effective, and which least effective?

A. Say nothing until the acquisition is confirmed - acting on rumours risks destabilising a successful delivery.
B. Brief the SRO privately on the evidence and its confidence level, and commission a quiet, proportionate piece of work on contractual protections and exit-cost exposure, without disrupting the rollout.
C. Advise pausing the final rollout phase until the vendor's ownership position is clarified.
D. Circulate the intelligence to the programme team and architecture community so everyone can factor it into their work.

**Most effective: B. Least effective: A.**

**Explanation:** B is proportionate to both the evidence and the stakes: it moves the intelligence to the accountable person with its uncertainty honestly labelled, and converts anxiety into a concrete, low-drama task - reviewing licence terms, exit provisions and cost exposure - that is worth doing under almost any outcome. This is horizon scanning discharged as your role intends: identifying an emerging trend's potential impact and preparing the organisation, not predicting the future. C is disproportionate on current evidence: pausing a near-complete rollout on an unconfirmed negotiation inflicts certain delivery and morale costs against a speculative risk, and would spend your credibility badly if the acquisition evaporates. D confuses transparency with broadcast: unverified market intelligence circulated widely will leak, distort, alarm an exhausted team and possibly touch market-sensitive territory - senior information handling means matching audience to need. A is least effective because "wait for confirmation" is precisely the failure mode horizon scanning exists to prevent: by the time an acquisition is public, contractual leverage has gone. Doing nothing with credible intelligence is a decision, and the worst one available.

**Question 6 (moderate) - The cross-government request**

A lead architect in another department emails you: they are starting a similar transformation and ask for your reference architectures, your supplier evaluation materials, and an hour of your time. Your team is stretched, your materials contain some department-specific commercial details, and there is no formal mechanism obliging you to help.

Which response is most effective, and which least effective?

A. Decline politely, explaining your team's capacity constraints, and suggest they consult published cross-government guidance.
B. Send everything as-is immediately - cross-government collaboration should be frictionless.
C. Agree to the conversation, share the reference architectures after removing commercially sensitive content, and propose a recurring exchange between your two architecture communities.
D. Ask them to route the request through formal inter-departmental channels to protect both departments.

**Most effective: C. Least effective: A.**

**Explanation:** C embodies two skills your profile names explicitly: working with people outside your organisation to inform policies, strategies and standards, and actively networking as part of community collaboration. It handles the genuine constraint (commercial sensitivity) with judgement rather than using it as a shield, and converts a one-off favour into a durable channel - which is how reuse and shared learning across government actually take root, and which will repay your own horizon scanning many times over. B is generous but careless: supplier evaluation materials with commercial details shared unredacted could prejudice procurements in both departments; enthusiasm does not excuse the information-handling lapse. D is not wrong so much as needlessly bureaucratic for knowledge-sharing between professionals - formality has its place for data sharing and joint procurement, but invoking it for reference architectures signals defensiveness. A is least effective: it treats a strategic opportunity as an inbox burden, models insularity to the community you are supposed to develop, and contradicts the collaborative posture UK government digital strategy expects of its senior architects. Capacity is real, but an hour invested in cross-government reuse is close to the definition of leverage.

**Question 7 (challenging) - The supplier's invitation**

The account director of a supplier currently bidding for your integration platform contract invites you to an all-expenses-paid two-day "architecture executive summit" at an attractive venue, noting that "several of your peers from other departments are attending" and that there will be "an early preview of our product roadmap - valuable input for your strategy."

Which response is most effective, and which least effective?

A. Decline the invitation, citing the live procurement, record the approach per your department's gifts and hospitality process, and inform the commercial team.
B. Attend, but pay your own expenses so no hospitality is received.
C. Decline the invitation but ask the supplier to send the roadmap preview privately so you keep the strategic insight.
D. Accept - roadmap intelligence is legitimate horizon scanning, and peer networking benefits the department.

**Most effective: A. Least effective: C.**

**Explanation:** During a live procurement, the only safe posture is visible, recorded distance. A does everything right: declines, creates a record, and puts the commercial team on notice that the supplier is cultivating decision-makers mid-bid - protecting the procurement's integrity, the department, and you. B misdiagnoses the problem as merely financial: paying your own way removes the hospitality but not the selective access and perceived favouritism of summiting with a bidding supplier. D dresses the conflict in your own professional vocabulary - horizon scanning is a real duty, which is what makes this distractor dangerous, but roadmap intelligence must come through channels available on equal terms, such as structured market engagement open to all bidders. C is least effective because it is the least honest option: it performs propriety publicly while privately extracting the exclusive benefit, potentially handing the other bidders grounds for challenge and, if surfaced, reading as concealment. In situational judgement terms, options combining the appearance of integrity with its absence score below options that are openly wrong.

**Question 8 (moderate) - The governance bypass**

You discover that a delivery team, with their programme architect's knowledge, deployed a significant integration into production without the design authority review your standards require - to hit a ministerial deadline. The integration appears to work. The programme architect says: "We'd have missed the date. I made a judgement call. I was going to bring it to the authority retrospectively."

Rank the following actions from most to least effective:

A. Commission an immediate retrospective review of the deployed integration, and separately examine with the community why the governance path could not operate at ministerial pace - fixing the process if it genuinely cannot.
B. Require the integration to be rolled back until it passes design authority review.
C. Accept the retrospective review offer and take no further action, since the integration works.
D. Formally reprimand the programme architect to deter future bypasses.

**Correct ranking: A, D, C, B.**

**Explanation:** A addresses both live risks: the unassured integration (reviewed now, remediated if needed) and the systemic condition that produced the bypass - because a governance process that cannot serve a ministerial deadline will be bypassed again, by someone, soon. Contributing to the development of governance and assurance is in your skill profile precisely because governance must earn its place at delivery pace. D ranks second with caveats: accountability matters and the architect knowingly bypassed mandated assurance, but leading with formal sanction while the process itself was arguably unworkable risks teaching the community to hide deviations rather than surface them - better folded into A's response than fired alone. C is passivity dressed as pragmatism: "it works" is exactly what unassured systems look like until they do not, and accepting retrospective review as the norm converts your standards into suggestions. B is least effective: rolling back a working, ministerially significant service inflicts certain public harm to remedy a procedural failure - proportionality is a public sector value too, and governance that punishes citizens to discipline teams will lose the argument it most needs to win.

**Question 9 (moderate) - The accessibility trade-off**

Facing an in-year budget cut, a finance-led review proposes descoping the assisted-digital and accessibility work from a service replacement programme, noting "the online channel meets the needs of 92% of users, and the remaining features can follow in a future phase - saving £600,000 this year." The service is used by many vulnerable citizens. You are asked, as the architecture voice on the review board, for your position.

Which response is most effective, and which least effective?

A. Support the descope, on the condition that the future phase is formally committed in the roadmap.
B. Oppose the descope, explaining that accessibility is a legal and policy obligation rather than a feature, quantifying the exposure - complaints, assisted-channel costs, rework, legal risk - and proposing alternative savings from the architecture, such as descoping a duplicative component or deferring a non-statutory integration.
C. Oppose the descope on principle and state that architecture cannot endorse the programme if it proceeds.
D. Abstain, noting that accessibility scope is a business decision outside architecture's remit.

**Most effective: B. Least effective: D.**

**Explanation:** B does three things that mark senior effectiveness: it reframes the issue correctly (accessibility for public services is an obligation under UK equality law and government service standards, not a deferrable enhancement - "92% of users" means excluding precisely the citizens most likely to depend on the service); it speaks finance's language by quantifying the true cost of the descope; and it does the constructive work of finding the £600,000 somewhere less harmful - which is exactly what taking a strategic view across domains and recommending value for money means in practice. C shares B's principle but not its craft: ultimatums without alternatives invite the board to route around architecture, and gaining support for high-risk positions is the skill being tested. A is the seductive middle: a "committed future phase" during a budget cut is a promise the next budget cut will collect - and the exposure exists in the interim. D is least effective: user needs, inclusion and legal compliance are not outside the remit of the person who owns the enterprise view from business, technology and data perspectives; abstention here is abdication with paperwork.

**Question 10 (challenging) - The strategy under fire**

Eighteen months into the three-year enterprise strategy you authored, a new chief operating officer tells senior leadership the strategy is "yesterday's thinking", citing an analyst report favouring a radically different platform philosophy, and proposes commissioning an external consultancy to redraft it. Some of the COO's criticisms touch weaknesses you privately recognise; others misread what the strategy says. Delivery teams are unsettled and two programmes have quietly paused decisions "pending strategic clarity".

Which response is most effective, and which least effective?

A. Defend the strategy robustly at leadership level, correcting the misreadings and noting the delivery progress made against it.
B. Propose to leadership a structured, time-boxed strategy review that you lead with the COO as co-sponsor, taking the analyst report and delivery evidence as inputs, with an explicit interim decision rule so paused programmes can proceed.
C. Support the external consultancy commission and offer your team's cooperation.
D. Continue delivering to the current strategy while the debate resolves itself at leadership level.

**Most effective: B. Least effective: D.**

**Explanation:** B treats the strategy as what your role profile says it is: something owned, evolved and defended on evidence - not a personal artefact. Co-sponsoring with the COO converts an adversary into a joint owner of the outcome; time-boxing and the interim decision rule address the quietly accruing damage (paused programmes) that every other option ignores; and taking the criticisms as inputs honours the ones you know are valid. This is strategy design as the profession defines it - connecting and enabling, removing blockers - performed under political pressure. A defends the parts worth defending but positions you as the strategy's advocate rather than the organisation's, and leaves the valid criticisms to be discovered by others later, at greater cost to you. C outsources your core accountability at the first challenge; external perspectives can help within a review you shape, but wholesale redrafting by consultants signals the enterprise architecture function cannot do its job. D is least effective despite feeling dutiful: "carry on while leadership argues" abandons the field precisely when the organisation needs strategic clarity, leaves the paused programmes bleeding, and lets the strategy's fate be settled by whoever shows up - the opposite of taking a leading role in the overall direction of business and digital capabilities.

### Preparation tips

- **Anchor in the published values.** Re-read the Civil Service Code and the Government Digital Service Standard before an assessment. Scoring keys for public sector situational tests are built from user needs, integrity, transparency, accessibility, inclusion and collaboration - the vocabulary of your professional world.
- **Look for the option that treats people as capable.** At lead level, strong answers usually engage, coach or co-create before they instruct, escalate or shield. Options that do someone's thinking for them - or take their work away - rarely score well.
- **Check every option for what it ignores.** The least effective answer is often the one that quietly abandons a live harm: the paused programmes, the excluded users, the unassured integration. Ask of each option: what does this leave bleeding?
- **Distinguish first moves from last resorts.** Escalation, formal sanction and refusal are legitimate tools that score badly as opening moves. Many items test sequencing judgement, not whether you know the tool exists.
- **Be yourself, calibrated.** Situational assessments measure your natural judgement; gaming them produces inconsistent profiles. Your preparation is reflection - on mediations that worked, escalations you mistimed, feedback that lasted - not memorising "correct" personas.
- **Practise with your community.** Run one of these scenarios in an architecture community session and compare rankings. The discussion is superb development for your architects, and articulating *why* an option is weaker sharpens exactly the judgement the assessment measures.

### Common pitfalls

- **Choosing the idealistic over the effective.** "Consult everyone extensively" sounds virtuous and scores poorly when the scenario demands proportionate action at pace. Effectiveness in context is the criterion.
- **Selecting passive options.** Waiting for confirmation, noting risks in registers, abstaining, letting debates resolve themselves - passivity dressed as prudence is the most consistently penalised pattern.
- **Over-escalating.** Options that transfer the problem upward before you have engaged with it directly signal avoidance, not governance. Escalation earns its place after engagement, or when authority genuinely exceeds yours.
- **Under-weighting integrity risks.** Hospitality from bidding suppliers, selective private benefits, silence in meetings followed by corridor lobbying - senior scenarios probe whether propriety survives when it is inconvenient.
- **Solving the technical problem and missing the human one.** Imposed decisions, however architecturally sound, that leave conflicts and capability gaps untreated are second-tier answers in a role defined by influence and community development.
- **Ignoring the stated context.** Details like "the business case predates the strategy", "morale is fragile" or "nothing is confirmed publicly" are not scenery - they are the scenario writer telling you what the effective answer must accommodate.

## Conclusion

You have worked through a substantial body of practice material: logical and analytical reasoning over roadmaps, principles and decision records; numerical interpretation of budgets, supplier pricing, capacity plans and sustainability metrics; precise reading of standards, board papers, contract schedules and horizon-scanning reports; and judgement calls drawn from the real stakeholder terrain of a lead enterprise architect - resistant programme directors, enthusiastic board members, deadlocked architects, bidding suppliers and strategies under fire.

If one theme runs through all four assessment types, it is this: the disciplines they measure are the disciplines your role already demands. Deducing only what the evidence entails, verifying whole-life numbers before recommending, reading what a text actually says, and choosing the proportionate, transparent, capability-building response under pressure - these are not test-taking tricks but the daily craft of owning an enterprise architecture vision and leading the people who deliver it.

Treat your practice results as a development map. Where you were consistently strong, trust that strength and make it available to others - coaching your architecture community with material like this is squarely within your role, and teaching a discipline deepens it. Where you diverged from the worked answers, be curious rather than critical: a pattern of imported assumptions, skipped second steps or premature escalation, once named, is straightforward to correct - and correcting it improves your board papers, your assurance judgements and your mediations, not just your scores.

Before any formal assessment, give yourself the basics: short, regular practice in the preceding weeks rather than a single cram; the published values of the profession fresh in your mind; rest, and enough time to settle before the timer starts. During it, work steadily, bank the accessible marks, and let difficult items go rather than defending them at the cost of the paper.

You operate at a level where judgement is the job. Everything in this document has simply been judgement, rehearsed. Prepare well, approach the assessment with the same calm authority you bring to a difficult design review, and keep investing in the professional development of yourself and the community you lead. Good luck - you are better prepared than you were when you started reading.

