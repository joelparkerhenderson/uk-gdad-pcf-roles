# Enterprise Architect (Senior Enterprise Architect) - Psychometric Assessment Resources

## Introduction

Welcome. This document is a practical, role-specific preparation resource for psychometric assessments, written for you as a senior enterprise architect working within the UK Government Digital and Data (GDAD) Profession Capability Framework. Whether you are preparing for an internal progression board, applying for a new post in another department, or simply want to sharpen the mental skills your role demands, this guide is designed to help you practise, reflect, and walk into any assessment with confidence.

Psychometric assessments are structured, standardised exercises that measure the cognitive abilities, reasoning skills, and professional judgement that predict performance in a specific role. For a senior enterprise architect, that means far more than abstract puzzle-solving. Your role asks you to translate business strategy into business change and technical delivery; to own architecture visions, strategies, and roadmaps across 'as is', 'to be', and transitional states; to communicate complicated, complex, or risky architecture topics to senior stakeholders; and to make and guide architectural decisions characterised by medium risk and complexity. Assessments for roles like yours therefore concentrate on how you interpret dense strategic material, reason with budgets and capacity figures, spot inconsistencies in architectural artefacts, and exercise sound judgement in politically sensitive, multi-stakeholder situations.

This document is organised into four main assessment sections, each mirroring a common assessment type you may encounter:

1. **Workplace job-specific cognitive assessment** - pattern recognition, logical deduction, error checking, and prioritisation using the artefacts you genuinely handle: roadmaps, reference architectures, principles, and governance records.
2. **Workplace job-specific numeric reasoning assessment** - interpretation of budgets, licence costs, capacity figures, and value-for-money comparisons of the kind you weigh when recommending reuse, sustainability, and scalability.
3. **Workplace job-specific verbal reasoning assessment** - careful reading of strategies, standards, policies, and stakeholder correspondence, answered strictly from the text.
4. **Workplace job-specific situational judgement assessment** - realistic dilemmas involving lead architects, delivery teams, commercial colleagues, and senior business stakeholders.

Each section explains what the assessment measures, maps it explicitly to the skills in your role profile, provides a substantial set of practice questions with worked answers, and closes with preparation tips and common pitfalls.

How should you use this guide? First, work through the practice questions under realistic conditions - timed where suggested, without interruptions. Second, treat the worked explanations as self-reflection prompts: when your answer differs, ask whether the gap is knowledge, technique, or haste. Third, revisit the sections periodically; the reasoning habits assessed here are the same habits that make you effective day to day, so practice pays off twice. Take your time, be honest with yourself, and enjoy the process - you already use these skills every working day. This guide simply helps you demonstrate them under assessment conditions.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive ability assessment is a targeted psychometric test that measures the exact mental processes needed for your role, using practical workplace scenarios rather than abstract puzzles. For a senior enterprise architect, this means questions built around the artefacts you genuinely handle: enterprise roadmaps with transitional states, dependency maps across portfolios and programmes, architectural principles and their exceptions, governance decision logs, technology radar entries from horizon scanning, and reference architectures spanning business, technology, and data domains.

Typical format and timing: these assessments are usually delivered online, timed at 15 to 30 minutes, with objective scoring against a benchmark or norm group. Questions mimic everyday tasks and data formats of the actual job, and some modern platforms adapt question difficulty based on your previous answers. You will often receive short, ungraded practice questions first so you can get comfortable with the interface, and employers typically receive a breakdown of speed versus accuracy rather than a single score - so working steadily and accurately matters as much as working quickly.

Why does this matter for your role? Cognitive ability underpins nearly everything in the senior enterprise architect role profile. When you take a strategic view across all architectural domains, portfolios and programmes, you are performing multi-variable reasoning. When you identify influences or risks, you are pattern-matching weak signals against your mental model of the organisation's ecosystem and its interdependencies. When you assure that business, technology and data decisions align with the enterprise architecture strategy, you are error-checking complex artefacts against a reference. A well-designed cognitive assessment simply externalises these daily mental operations into scored questions.

### What it measures for your role

Mapping the standard cognitive dimensions to the named skills in your role profile:

- **Logical deduction and inference** maps to **Making architectural decisions**: making and guiding design decisions characterised by medium risk and complexity requires you to reason correctly from principles, constraints, and governance rules to conclusions - exactly what deductive items test.
- **Pattern recognition and trend detection** maps to **Architect for the whole context**: tracking emerging internal and external issues over time that could affect teams across the organisation is applied pattern recognition, as is your duty to carry out horizon scanning across industry and identify emerging trends.
- **Error checking and consistency analysis** maps to **Enterprise architecture** and **Making architectural decisions**: keeping 'as is', 'to be', and transitional-state views coherent, and spotting where a solution design contradicts an established principle, are error-checking tasks at enterprise scale.
- **Prioritisation and problem structuring** maps to **Problem definition and shaping**: framing problems of medium complexity so a solution can be created, and describing options so appropriate delivery methods can be decided, depend on the ability to decompose, order, and weigh factors quickly.
- **Working memory and information integration** maps to **Strategy design**: directing the implementation of a strategy through roadmaps and plans requires you to hold multiple moving parts - dependencies, funding windows, capability gaps - in mind simultaneously.

### Practice questions

Work through these under light time pressure - aim for two to three minutes per question. Full worked explanations follow each answer.

**Question 1 (easy) - Principle consistency check.** Your architecture principles catalogue includes: P1 "Reuse before buy, buy before build"; P2 "Data is shared across the organisation unless legally restricted"; P3 "All citizen-facing services must meet the government accessibility standard". A delivery team proposes building a bespoke document management system because "procurement takes too long", storing its data in an isolated silo "for simplicity". Which principles does the proposal breach?

A) P1 only
B) P1 and P2
C) P2 and P3
D) All three

**Correct answer: B.** Building bespoke when reuse or buy options have not been exhausted breaches P1; isolating data without a legal restriction breaches P2. Nothing in the scenario says the system is citizen-facing or inaccessible, so P3 is not demonstrably breached. The reasoning skill here is disciplined scope: assess only what the evidence supports, a habit central to architectural assurance where over-claiming breaches damages your credibility with delivery teams just as surely as missing them does.

**Question 2 (easy) - Transitional state ordering.** Your 'to be' architecture requires four changes: (1) migrate the case management system to the cloud platform; (2) decommission the legacy data centre; (3) establish the cloud landing zone; (4) re-platform the integration layer that the case management system depends on. Given that the data centre cannot close until everything hosted there has moved, and the case management system cannot migrate until its integration layer is re-platformed on the landing zone, what is the only valid sequence?

A) 3, 4, 1, 2
B) 3, 1, 4, 2
C) 4, 3, 1, 2
D) 1, 4, 3, 2

**Correct answer: A.** The landing zone (3) must exist before anything can be re-platformed onto it, so 3 precedes 4. The integration layer (4) must precede the case management migration (1), and decommissioning (2) must come last. This is a pure dependency-chain deduction - the same reasoning you apply when sequencing transitional states on a roadmap so delivery can proceed at pace without rework.

**Question 3 (moderate) - Horizon scanning signal classification.** During quarterly horizon scanning you log four signals: (i) a major cloud vendor announces end-of-support for a database version used by three of your programmes in 18 months; (ii) an emerging AI regulation is in early consultation, with legislation unlikely for three years; (iii) a competitor department has published a reusable identity component compatible with your stack; (iv) a niche vendor your organisation does not use has filed for insolvency. Using an impact-versus-urgency lens, which signal demands action in the current planning cycle?

A) (i)
B) (ii)
C) (iii)
D) (iv)

**Correct answer: A.** Signal (i) combines high impact (three programmes affected) with genuine urgency (18 months is short for coordinated migration across programmes, given funding and delivery lead times). Signal (ii) is high potential impact but low urgency - monitor and brief, do not mobilise. Signal (iii) is an opportunity worth evaluating (reuse principle) but not time-critical. Signal (iv) is low impact because there is no exposure. Senior enterprise architects add value precisely by ranking signals this way rather than treating every trend as equally pressing.

**Question 4 (moderate) - Error checking a decision log.** An architecture decision record (ADR) states: "Decision: adopt the corporate API gateway for all new integrations. Rationale: reduces per-integration cost from £45,000 to £12,000. Consequences: all seven in-flight programmes must migrate existing integrations within six months." Which element of this ADR contains a logical flaw?

A) The decision statement
B) The rationale
C) The consequences
D) None - the ADR is sound

**Correct answer: C.** The decision covers "all new integrations", yet the consequences impose migration of existing integrations - a scope mismatch between decision and consequence. The rationale may be accurate, and the decision itself is clear. Spotting scope drift between what was decided and what is being enacted is a core assurance skill: governance boards frequently approve one thing while delivery plans quietly implement another, and it is the enterprise architect who is expected to catch it.

**Question 5 (moderate) - Stakeholder logic puzzle.** You must brief four stakeholders - the Chief Digital Officer (CDO), the finance director, the lead architect, and a programme director - on a roadmap change, each in a separate meeting. Constraints: the lead architect must be briefed before the CDO (internal alignment first); the finance director will only meet after the programme director has confirmed the cost impact; the programme director insists on hearing the change after the lead architect has technically validated it. Who is briefed second?

A) The CDO
B) The programme director
C) The finance director
D) It cannot be determined

**Correct answer: D - but examine why.** The lead architect is definitively first (both the CDO chain and the programme-director chain require them earlier). After that, either the CDO or the programme director could be second: the CDO needs only the lead architect briefed first, and the programme director likewise. The constraints fix the lead architect first and the finance director after the programme director, but do not order the CDO relative to the programme director. Recognising when information is insufficient - rather than forcing a conclusion - is exactly the discipline you apply when stakeholder sequencing genuinely matters, such as pre-briefing before a design authority.

**Question 6 (moderate) - Capability pattern recognition.** Reviewing capability assessments across five business domains, you notice: domains that score low on "data governance maturity" also score low on "reporting timeliness" in four of five cases; the exception is the finance domain, which scores low on data governance but high on reporting timeliness because it operates a dedicated manual reconciliation team of nine staff. What is the most defensible inference?

A) Data governance maturity causes reporting timeliness
B) The correlation suggests a relationship worth investigating, and finance's exception suggests manual effort can mask the underlying weakness at a cost
C) Finance has solved data governance
D) Reporting timeliness is unrelated to data governance

**Correct answer: B.** Four-of-five co-occurrence is a correlation, not proof of causation - option A over-claims. Option C confuses compensating for a weakness with resolving it; the nine-person manual team is a workaround with an ongoing cost, a classic 'as is' pain point to surface on the roadmap. Option D ignores the pattern entirely. Enterprise architecture reasoning constantly involves reading patterns across domains while resisting premature causal claims - and spotting where hidden operational cost is masking architectural debt.

**Question 7 (challenging) - Multi-constraint prioritisation.** Your architecture team of four (including you) has capacity for three major engagements this quarter. Five are requested: (a) assurance review of a £30m programme at a critical gate this quarter; (b) developing the data architecture strategy, already two quarters late, and blocking two programmes' designs; (c) a proof of concept on an emerging technology the CDO is personally enthusiastic about; (d) supporting a procurement worth £8m that closes next quarter; (e) refreshing the architecture principles, last updated four years ago. Using value, urgency, and risk reduction as criteria, which three should you select?

A) a, b, c
B) a, b, d
C) b, c, e
D) a, c, d

**Correct answer: B.** Engagement (a) is both urgent (gate this quarter) and high risk-reduction (£30m exposure). Engagement (b) is urgent by virtue of blocking two programmes - deferral compounds delay across the portfolio. Engagement (d) closes next quarter but procurement input must precede closure, and £8m of commercial exposure with sourcing-strategy implications outranks the remaining options. Engagement (c) is attractive but sponsor enthusiasm is not a value case; the disciplined answer is to shape it for next quarter with a clear problem definition. Engagement (e) matters but has waited four years and carries no date. Note the professional subtlety: declining (c) requires managing the CDO's expectations - which is why prioritisation questions for senior roles usually carry a stakeholder dimension inside the logic.

**Question 8 (challenging) - Roadmap inconsistency detection.** A programme's transition plan states: "Transitional state TS1 (March): payments capability moves to the shared platform; legacy payments module enters read-only mode. Transitional state TS2 (June): customer records migrate to the master data service; legacy payments module decommissioned. Transitional state TS3 (September): reporting layer switches to the master data service as its sole source." A separate risk log entry, written by the same programme, says: "Risk 14: reporting layer currently reads live transaction data directly from the legacy payments module; no mitigation required because migration is sequenced." Which inconsistency should you challenge?

A) TS1 and TS2 are in the wrong order
B) The legacy payments module is decommissioned in TS2, but the reporting layer does not switch away from it until TS3
C) Risk 14 should not be on the risk log at all
D) Customer records cannot migrate before payments

**Correct answer: B.** If the reporting layer reads directly from the legacy payments module (per Risk 14) and that module is decommissioned in June (TS2), then between June and September the reporting layer has lost a live data source - yet the plan does not switch reporting until TS3. Risk 14's claim that "no mitigation is required because migration is sequenced" is therefore false: the sequencing is precisely the problem. Options A and D assert dependencies the text does not establish. This item mirrors one of the highest-value activities in your role: cross-referencing artefacts produced by different people at different times and finding where they silently contradict each other.

**Question 9 (challenging) - Deductive reasoning from governance rules.** Your architectural governance framework states: "Rule G1: decisions with medium or high risk require design authority approval. Rule G2: decisions affecting more than one domain require an impact assessment before approval. Rule G3: an impact assessment is valid for 90 days." A decision is classified medium risk, affects the technology and data domains, and its impact assessment was completed 120 days ago. The delivery team argues the decision can proceed because the design authority approved it in principle 60 days ago. Can the decision validly proceed under the rules?

A) Yes - design authority approval is the only hard requirement
B) Yes - approval in principle within 90 days satisfies all rules
C) No - the impact assessment has expired, so the precondition for valid approval has lapsed
D) Cannot say - the rules do not cover approval in principle

**Correct answer: C.** Work the chain: medium risk triggers G1 (approval required); two domains trigger G2 (impact assessment required before approval); G3 renders a 120-day-old assessment invalid. An approval whose precondition has lapsed is unsafe to rely on - the disciplined reading is that the assessment must be refreshed. Option D is tempting because "approval in principle" is indeed undefined, but the expired assessment settles the question regardless of how the approval is characterised. In governance reasoning, look for the constraint that decides the matter independently of the ambiguous ones - it lets you give delivery teams a clear answer instead of a lawyerly shrug.

**Question 10 (challenging) - Analogy and abstraction across domains.** Your organisation solved integration sprawl in the technology domain by introducing an API gateway with a published catalogue, standard contracts, and usage monitoring. The data domain now suffers an analogous problem: dozens of teams take ad-hoc extracts from source systems, each negotiating access separately, with no visibility of who consumes what. Which intervention is the closest structural analogue to the gateway solution?

A) Mandate that all extracts be approved by the data governance board
B) Establish a data-sharing platform with a published data catalogue, standard access contracts, and consumption monitoring
C) Build a single enterprise data warehouse containing all data
D) Prohibit ad-hoc extracts

**Correct answer: B.** The gateway pattern's essence is a mediated, catalogued, contract-based, observable point of access - option B reproduces all four properties in the data domain. Option A adds governance without infrastructure (approval boards do not create visibility or standard contracts). Option C changes where data lives rather than how access is mediated, and is a far larger commitment than the analogy requires. Option D removes the problem's symptom without offering the legitimate consumers a route, so shadow extracts will simply go underground. Recognising the deep structure of a pattern and transplanting it across business, technology, and data perspectives is a signature enterprise architecture skill.

**Question 11 (moderate) - Working memory and integration.** Hold these facts in mind: the grants programme depends on the identity platform; the identity platform upgrade completes in Q3; the grants programme go-live is committed for Q2; the tax programme also depends on the identity platform but not on the upgrade; a temporary identity workaround exists but has only been security-assured for internal users; the grants programme serves external citizens. What is the critical conclusion?

A) The tax programme must delay to Q3
B) The grants programme can go live in Q2 using the workaround
C) The grants programme has an unresolved dependency conflict: its Q2 go-live precedes the Q3 upgrade, and the workaround is not assured for its external users
D) The identity upgrade should be cancelled

**Correct answer: C.** Integrating all six facts: grants needs the upgraded platform (Q3) but launches Q2; the only bridge is the workaround; the workaround's assurance covers internal users only; grants serves external citizens. Therefore the workaround does not close the gap, and an unresolved conflict exists that must be escalated - either accelerate the upgrade, extend the assurance, or move the go-live. Option B fails on the assurance scope; option A drags in the tax programme, which is unaffected by the upgrade. Assessments use items like this to test whether you can hold several conditional facts simultaneously without dropping one - the daily reality of managing interdependencies across an ecosystem.

**Question 12 (challenging) - Problem framing selection.** The operations director tells you: "Our contact centre is drowning - we need a new CRM." Initial discovery shows 60% of calls are people chasing the status of applications that are processed on paper forms, with a six-week backlog. Which problem framing best enables a solution to be created?

A) "The contact centre needs a modern CRM with better call routing"
B) "Citizens cannot see the status of their applications, and processing is slow, generating avoidable contact; we should examine status visibility and processing throughput before contact-centre tooling"
C) "The organisation needs a digital transformation"
D) "The contact centre needs more staff"

**Correct answer: B.** Option B reframes the presenting request (a CRM) into the underlying causal chain the evidence supports - slow paper processing plus no status visibility drives avoidable demand - while explicitly sequencing what to examine first. Option A accepts the solution as the problem statement, the most common framing failure. Option C is so broad it enables nothing. Option D treats a symptom. Your skill profile explicitly includes framing problems characterised by medium complexity so that a solution can be created, and describing options so appropriate delivery methods can be decided; this question is that skill in miniature, and it also illustrates why architects who challenge the presenting request respectfully - with evidence - earn stakeholder trust.

**Question 13 (moderate) - Number-series reasoning in a capacity context.** Monthly active users of a shared platform over six months: 12,000; 14,400; 17,280; 20,736; 24,883; 29,860. The platform's assured capacity ceiling is 51,600 users. Following the established pattern, in approximately how many further months does usage reach the ceiling?

A) 2 months
B) 3 months
C) 5 months
D) 7 months

**Correct answer: B.** Each month grows by 20% (12,000 × 1.2 = 14,400, and so on). Continuing: month 7 ≈ 35,832; month 8 ≈ 42,998; month 9 ≈ 51,598 - effectively the ceiling. That is three further months beyond the six shown. Recognising geometric rather than linear growth is the crux: a linear reader averages ~3,572 users/month and wrongly concludes six months of headroom, precisely the misjudgement that causes scalability crises. Recommending scalability before it is urgent is part of guiding the organisation to sound technology decisions.

**Question 14 (moderate) - Error checking a reference architecture mapping.** A reference architecture lists four mandatory capabilities for any citizen-facing service: identity verification, payment handling, notification, and audit logging. A solution design document maps its components as follows: "GOV-ID module → identity verification; PayGate connector → payment handling; AuditTrail service → notification; MessageHub → audit logging." Assuming each named component genuinely provides what its name suggests, what is wrong?

A) A mandatory capability is missing entirely
B) Two components are mapped to the wrong capabilities
C) The design has too many components
D) Nothing - the mapping is complete and correct

**Correct answer: B.** All four capabilities appear, and all four components are present, but AuditTrail (by name, an audit logging component) is mapped to notification, while MessageHub (by name, a messaging/notification component) is mapped to audit logging - the last two mappings are transposed. This is the kind of clerical-looking error that slips through governance because every box is ticked; only a reader who checks each pairing, not just the coverage, catches it. Assurance quality lives in exactly this level of attention.

**Question 15 (challenging) - Syllogistic reasoning about standards.** Consider three statements from your standards library: "All services handling personal data must complete a data protection impact assessment (DPIA). Some legacy services handle personal data. No service that has completed a DPIA may store data outside approved regions." A colleague concludes: "Therefore some legacy services may not store data outside approved regions." Is the conclusion valid?

A) Yes - it follows necessarily from the statements
B) No - it assumes legacy services have actually completed their DPIAs
C) No - legacy services are exempt from standards
D) Cannot say - the statements contradict each other

**Correct answer: B.** The chain requires: some legacy services handle personal data → those services *must complete* a DPIA → services that *have completed* a DPIA cannot store data outside approved regions. The gap is between obligation and fact: "must complete" does not entail "have completed". If a legacy service is non-compliant (no DPIA done), the third rule's restriction does not yet formally bite it, even though it should. The colleague's conclusion describes the intended end state, not what the statements strictly entail. Spotting the difference between "the rules require X" and "X is true" is essential when you assure compliance claims - a programme saying "we are covered by the standard" is not the same as the standard's conditions actually having been met.

### Preparation tips

- **Practise with your own artefacts.** Take a real roadmap, decision log, or principles catalogue (suitably anonymised) and interrogate it: which entries contradict each other? Which dependencies are implicit? This builds exactly the muscles the assessment tests, and it improves your day job simultaneously.
- **Rehearse dependency chains on paper.** For sequencing questions, sketch a quick directed graph rather than reasoning purely in your head - under time pressure, externalising the structure prevents dropped constraints.
- **Calibrate your pace.** With 15 to 30 minutes for a full test, budget roughly a minute per item, banking time on easy items. If an item resists you for 90 seconds, flag it and move on; adaptive scoring rewards steady accuracy over heroic struggles with a single hard item.
- **Read the question stem before the scenario details.** Knowing what is being asked lets you extract only the relevant constraints - a technique that mirrors how you skim a 40-page solution design for the three pages that matter to assurance.
- **Trust your professional instincts, then verify.** As a senior practitioner, your first read of a governance or sequencing item is usually right; use remaining seconds to check the one constraint you might have skipped, rather than second-guessing the whole chain.

### Common pitfalls

- **Bringing outside knowledge into closed-logic items.** You know how enterprise architecture "should" work; the test asks what follows from the stated rules. If the scenario's governance framework differs from your department's, reason from the scenario.
- **Over-claiming from correlations.** Pattern-recognition items often bait a causal conclusion from co-occurring observations. Choose the option that says "investigate" over the one that says "proven" unless the logic is airtight.
- **Losing time to a single multi-stage item.** The classic time sink: a question with four constraints and a table. Flag, skip, return. A senior candidate's undoing is rarely ability - it is spending five minutes proving they can solve the hardest item while three easy ones go unanswered.
- **Misreading scope words.** "All new integrations" versus "all integrations"; "must" versus "should"; "more than one domain" versus "one or more domains". Assessment writers - like policy writers - hide the answer in quantifiers and modal verbs.
- **Ignoring the speed-versus-accuracy report.** Because employers see accuracy and pace separately, wild guessing to finish damages your accuracy profile. Prefer educated elimination: discarding two options and choosing between the remainder is measurably better than random selection.


## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment evaluates your ability to analyse, interpret, and make logical decisions using numerical data, mimicking the data-handling demands of your actual role. It focuses on business mathematics - percentages, ratios, cost comparisons, capacity figures - rather than abstract formulas. For a senior enterprise architect in UK government, that means the numbers you genuinely encounter: programme budgets and spend profiles, licence and hosting cost comparisons, total cost of ownership over spending review periods, capacity and utilisation figures for shared platforms, benefits projections in business cases, and the value-for-money arithmetic behind reuse-versus-build recommendations.

Typical format and timing: questions present real-world data as tables, charts, or short briefings, under a strict time limit - often around a minute to ninety seconds per question. Most assessments allow or provide an onscreen calculator, because the test prioritises interpretation over mental arithmetic: the challenge is extracting the right figures quickly and applying the right operation, not long division. Expect scale qualifiers ("in thousands", "per quarter"), multi-step calculations, and distractor answers that reward common mistakes.

Why does this matter for your role? Your role profile asks you to guide the organisation to make appropriate business, technology and data decisions by recommending reuse, sustainability and scalability, to achieve value for money and reduce risk. Every one of those recommendations ultimately rests on numbers: what does duplication cost, what does the transition cost, when does the investment break even, how much headroom does the platform have. Your commercial perspective skill - understanding sourcing strategies and commercial processes - likewise depends on comparing bids, models, and cost structures numerically. Senior stakeholders will probe your figures; the finance director will certainly recalculate them. Numeric fluency is what lets your strategic advice survive that scrutiny.

### What it measures for your role

Mapping numeric reasoning dimensions to the named skills in your role profile:

- **Cost comparison and value-for-money analysis** maps to **Commercial perspective**: understanding different sourcing strategies and when to apply them requires comparing licence models, evaluating total cost of ownership across contract terms, and spotting when a cheaper unit price hides a costlier structure.
- **Percentages, growth rates, and trend projection** maps to **Architect for the whole context** and **Strategy design**: tracking issues over time, projecting platform demand, and building credible roadmaps all require you to reason about rates of change and compounding.
- **Budget and resource arithmetic** maps to **Making architectural decisions**: architectural risks that affect multiple teams or domains are frequently financial at root - overruns, duplicated spend, unfunded transitions - and quantifying them is how you get them addressed at the appropriate level.
- **Ratio and utilisation analysis** maps to **Enterprise architecture**: designing the technology, people, process and other elements needed to achieve organisational objectives means reasoning about capacity ratios, team allocation, and consolidation savings.
- **Interpreting data presented by others** maps to **Architecture communication**: when a programme presents benefits figures to a board, you are often the person expected to validate or challenge them on the spot.

### Practice questions

An onscreen calculator is assumed. Aim for 90 seconds per question; the arithmetic is shown in full in each explanation.

**Question 1 (easy) - Percentage of budget.** A transformation portfolio has a total budget of £48 million. The enterprise architecture function's allocation is £1.92 million. What percentage of the portfolio budget is allocated to enterprise architecture?

A) 2.5%
B) 4%
C) 4.8%
D) 5%

**Correct answer: B.** £1.92m ÷ £48m = 0.04 = 4%. A quick sanity check: 10% of £48m is £4.8m; half of that (5%) is £2.4m; £1.92m is a bit less, so the answer must be below 5% - which eliminates C and D instantly. Answer C (4.8%) is the classic distractor formed by mis-dividing £48m by 10 and anchoring on the digits.

**Question 2 (easy) - Consolidation saving.** Your 'as is' analysis finds four business units each running a separate document management contract costing £220,000, £185,000, £240,000 and £155,000 per year respectively. A consolidated enterprise contract would cost £560,000 per year. What is the annual saving from consolidation?

A) £200,000
B) £240,000
C) £280,000
D) £320,000

**Correct answer: B.** Current total: £220,000 + £185,000 + £240,000 + £155,000 = £800,000. Saving: £800,000 − £560,000 = £240,000 per year, a 30% reduction. This is the arithmetic core of the reuse recommendation you make constantly: quantify the duplication first, because "we could consolidate" persuades no one, while "we are paying £240,000 a year for duplication" reaches the board agenda.

**Question 3 (moderate) - Total cost of ownership comparison.** You are comparing two options for a case management capability over a four-year term. Option A (SaaS): £380,000 per year subscription, £150,000 one-off implementation. Option B (build on the shared platform): £520,000 development in year 1, then £160,000 per year running costs in years 2 to 4, plus £90,000 per year platform contribution in all four years. Which option is cheaper over four years, and by how much?

A) Option A, by £150,000
B) Option B, by £310,000
C) Option B, by £330,000
D) Option A, by £90,000

**Correct answer: B.** Option A: (£380,000 × 4) + £150,000 = £1,520,000 + £150,000 = £1,670,000. Option B: £520,000 development + (£160,000 × 3 years of running costs) + (£90,000 × 4 years of platform contribution) = £520,000 + £480,000 + £360,000 = £1,360,000. Difference: £1,670,000 − £1,360,000 = £310,000, so option B is cheaper by £310,000. The traps are all in period counting: "years 2 to 4" is three years of running costs, not four (a slip that adds £160,000 to B), while the platform contribution runs all four years, not three (a slip that removes £90,000). Counting contract periods correctly is the single most common total-cost-of-ownership error in real business cases, and assessments test it deliberately because architects who miscount contract years approve flawed comparisons.

**Question 4 (moderate) - Percentage change in unit cost.** A shared API platform cost £900,000 to run last year and processed 150 million calls. This year it costs £1,080,000 and processed 240 million calls. What has happened to the cost per million calls?

A) Increased by 20%
B) Decreased by 20%
C) Decreased by 25%
D) Decreased by 33%

**Correct answer: C.** Last year: £900,000 ÷ 150 = £6,000 per million calls. This year: £1,080,000 ÷ 240 = £4,500 per million calls. Change: (£4,500 − £6,000) ÷ £6,000 = −£1,500 ÷ £6,000 = −25%. Note the trap in option A: total cost rose 20% (£900k → £1,080k), and a hurried reader reports that. The strategically meaningful figure - the one that demonstrates the platform's scalability and value for money - is unit cost, which fell 25% because volume grew faster than cost. Presenting unit economics rather than raw totals is exactly how you make the case for shared capabilities to sceptical budget holders.

**Question 5 (moderate) - Ratio allocation.** Your architecture community comprises 36 architects allocated across domains in the ratio 5:3:1 for solution, data, and security architecture respectively. The target operating model requires the ratio to become 4:3:2 with the same headcount. How many architects must move into security architecture?

A) 4
B) 6
C) 8
D) 12

**Correct answer: A.** Current: ratio parts 5+3+1 = 9; each part = 36 ÷ 9 = 4 architects. So security currently has 1 × 4 = 4. Target: parts 4+3+2 = 9; each part = 4. Security target: 2 × 4 = 8. Movement needed: 8 − 4 = 4 architects. Developing the architecture community is one of your duties, and workforce rebalancing questions like this - expressed in ratios in target operating model documents - are a realistic slice of that work. The distractor 8 is the target headcount rather than the change; always check whether the question asks for the new level or the delta.

**Question 6 (moderate) - Compound growth and capacity.** A hosting platform currently runs at 5,200 transaction-units of demand against an assured capacity of 9,000 units. Demand is growing at 15% per year, compounding. In which year does demand first exceed assured capacity?

A) Year 3
B) Year 4
C) Year 5
D) Year 6

**Correct answer: B.** Year 1: 5,200 × 1.15 = 5,980. Year 2: 5,980 × 1.15 = 6,877. Year 3: 6,877 × 1.15 = 7,908.55. Year 4: 7,908.55 × 1.15 = 9,094.8 - above 9,000. So the ceiling is breached in year 4. A linear approximation (5,200 + 780/year) wrongly suggests year 5 (5,200 + 4×780 = 8,320; +5×780 = 9,100), which is the trap: compounding accelerates, and the whole point of recommending scalability early is that intuition trained on straight lines underestimates exponential demand. When you brief this to a board, the difference between "we have five years" and "we have four" is a full spending-review cycle of lead time.

**Question 7 (challenging) - Benefits realisation shortfall.** A programme's business case promised benefits of £2.4 million per year once live, with go-live at the start of year 2 of a five-year appraisal period (so four years of benefits). Delivery slipped six months, and realised benefits are running at 70% of forecast. What total benefit should now be expected over the appraisal period, compared with the original promise?

A) £5.88m expected versus £9.6m promised
B) £6.72m expected versus £9.6m promised
C) £5.88m expected versus £12m promised
D) £6.72m expected versus £12m promised

**Correct answer: A.** Original promise: £2.4m × 4 years = £9.6m. Revised: the six-month slip leaves 3.5 years of benefits; at 70% of the £2.4m run-rate, that is £2.4m × 0.7 × 3.5 = £1.68m × 3.5 = £5.88m. Comparison: £5.88m versus £9.6m - a shortfall of £3.72m, or about 39%. The distractors: £6.72m ignores the slip (£1.68m × 4), and £12m wrongly counts five years of benefits. When you assure business, technology and data decisions, recomputing the benefits case after slippage is often the fastest way to show a board that a "minor delay" has material value-for-money consequences.

**Question 8 (challenging) - Sourcing strategy comparison.** You are advising on sourcing for an integration capability needed for five years. Three models are quoted. Model 1 (commodity cloud service): £0.008 per transaction, no fixed fee. Model 2 (managed service): £350,000 per year fixed, includes up to 60 million transactions per year, then £0.004 per additional transaction. Model 3 (framework call-off with a supplier): £480,000 per year fixed, unlimited transactions. Forecast volume is 90 million transactions per year. Which model is cheapest per year at forecast volume?

A) Model 1
B) Model 2
C) Model 3
D) Models 2 and 3 are equal

**Correct answer: B.** Model 1: 90,000,000 × £0.008 = £720,000. Model 2: £350,000 + (30,000,000 excess × £0.004) = £350,000 + £120,000 = £470,000. Model 3: £480,000. Model 2 wins by £10,000 per year over Model 3, and by £250,000 over Model 1. But note what a senior architect adds beyond the arithmetic: Model 2's advantage is fragile - at 92.5 million transactions it equals Model 3 (£350,000 + 32.5m × £0.004 = £480,000), so if growth is expected, the unlimited model may be the lower-risk recommendation. Assessments score the calculation; boards reward the sensitivity analysis. Understanding when each sourcing structure wins is precisely the commercial perspective skill in your profile.

**Question 9 (challenging) - Break-even analysis for a reuse platform.** Building a reusable notification component costs £600,000 up front and £100,000 per year to operate. Each programme that adopts it avoids building its own equivalent at £180,000 one-off plus £45,000 per year running costs, but pays a £25,000 per year usage charge to the platform. Over a three-year horizon, how many adopting programmes are needed for the organisation as a whole to break even?

A) 3
B) 4
C) 5
D) 6

**Correct answer: A.** Platform cost over three years: £600,000 + (3 × £100,000) = £900,000. Per-programme saving over three years: avoided £180,000 + (3 × £45,000) = £315,000; minus usage charges paid (3 × £25,000 = £75,000) = £240,000 net saving per programme. (The usage charge is an internal transfer, but treating it as a programme cost and platform revenue nets out; the simplest whole-organisation view: each adopter avoids £315,000 of duplicated spend.) Whole-organisation break-even: £900,000 ÷ £315,000 = 2.86, so three programmes. If the question instead asked when the platform's own funding balances (revenue £75,000 per adopter versus £900,000 cost), the answer would be 12 - which is why being precise about whose costs and whose savings you are counting matters enormously when you present a reuse business case. The distractor 4 comes from using the £240,000 figure (£900,000 ÷ £240,000 = 3.75 → 4), i.e. double-counting the internal charge; a defensible alternative model, but not the whole-organisation view the question asks for. In assessments, read the framing ("the organisation as a whole") carefully - it selects the model.

**Question 10 (moderate) - Reading a utilisation table.** A capacity report for three shared platforms shows: Platform Alpha - 640 of 800 compute units used; Platform Beta - 552 of 600 units used; Platform Gamma - 900 of 1,500 units used. Governance policy requires remedial action when utilisation exceeds 85%. Which platforms require action?

A) Alpha only
B) Beta only
C) Alpha and Beta
D) All three

**Correct answer: B.** Alpha: 640 ÷ 800 = 80%. Beta: 552 ÷ 600 = 92%. Gamma: 900 ÷ 1,500 = 60%. Only Beta exceeds the 85% threshold. The trap is anchoring on absolute headroom: Alpha has only 160 units spare while Gamma has 600, and Beta's 48 spare units look small but must be judged against its total. Percentages, not absolute gaps, drive threshold policies - and when you report platform risk to a board, converting to the policy's own metric avoids exactly this misreading.

**Question 11 (moderate) - Weighted scoring of options.** An options appraisal scores three architecture options against three criteria with weights: strategic alignment (weight 50%), cost (30%), delivery risk (20%). Scores out of 10: Option X - alignment 9, cost 4, risk 5. Option Y - alignment 6, cost 8, risk 7. Option Z - alignment 8, cost 6, risk 7. Which option wins on weighted score?

A) Option X
B) Option Y
C) Option Z
D) X and Z tie

**Correct answer: C.** Option X: (9 × 0.5) + (4 × 0.3) + (5 × 0.2) = 4.5 + 1.2 + 1.0 = 6.7. Option Y: (6 × 0.5) + (8 × 0.3) + (7 × 0.2) = 3.0 + 2.4 + 1.4 = 6.8. Option Z: (8 × 0.5) + (6 × 0.3) + (7 × 0.2) = 4.0 + 1.8 + 1.4 = 7.2. Z wins at 7.2, with Y at 6.8 and X at 6.7. Two lessons ride on this arithmetic. First, the mechanical one: unweighted totals mislead - X's raw total (18) trails Y's (21) and Z's (21), and Y and Z tie on raw scores, so only the weighted calculation separates them. Second, the professional one: X scores highest on the heaviest criterion yet still loses, because weak cost and risk scores drag it down; when weighted scores land within a few tenths of each other, as Y and X do here, the honest conclusion is that the weighting assumptions - not the arithmetic - are doing the deciding, and a senior architect surfaces that to the board rather than letting a spreadsheet artefact pick the enterprise's direction.

**Question 12 (easy) - Scale qualifiers.** A finance table headed "Programme spend (£000s)" shows the architecture workstream at 1,250 for the year against a budget of 1,400. How much budget remains, in pounds?

A) £150
B) £15,000
C) £150,000
D) £1,500,000

**Correct answer: C.** The figures are in thousands: spend £1,250,000 against budget £1,400,000, leaving £150,000. Misreading scale qualifiers is the most frequently cited pitfall in numeric assessments, and it has an exact workplace analogue: quoting a figure a thousand times too small (or large) in a board paper is the kind of error that undermines an otherwise excellent architectural argument. Always read the table header before the table.

**Question 13 (challenging) - Multi-step budget reconciliation.** A programme allocates its £3.6 million annual budget as: 45% delivery teams, 25% licences and hosting, 15% architecture and design, 15% contingency. Mid-year, licence costs rise by 20% and the increase is funded entirely from contingency. What percentage of the original contingency remains?

A) 40%
B) 50%
C) 60%
D) 66.7%

**Correct answer: D.** Licences: 25% of £3.6m = £900,000. A 20% rise adds £180,000. Contingency: 15% of £3.6m = £540,000. Remaining: £540,000 − £180,000 = £360,000. As a percentage of original contingency: £360,000 ÷ £540,000 = 0.667 = 66.7%. The distractor 60% comes from confusing "the increase equals a third of contingency" with "a third remains". Chained percentage questions reward writing each intermediate figure down - exactly as you would when checking a programme's mid-year reforecast before it reaches the investment board.

**Question 14 (moderate) - Interpreting a trend for horizon scanning.** Industry analyst data shows adoption of a new integration standard among comparable public sector organisations: year 1 - 4%; year 2 - 9%; year 3 - 19%; year 4 - 38%. If the pattern of roughly doubling continues, in which year would adoption first exceed 75%, and what should you advise?

A) Year 5; advise immediate wholesale migration
B) Year 5; advise preparing a position: assess impact, pilot, and sequence adoption on the roadmap
C) Year 6; advise waiting until adoption is universal
D) Year 4; the threshold is already passed

**Correct answer: B.** Doubling from 38% gives roughly 76% in year 5, crossing the 75% threshold. The advisory half of the question distinguishes senior candidates: option A over-reacts (wholesale migration on trend data alone ignores cost and risk), option C under-reacts (waiting forfeits the planning advantage that horizon scanning exists to provide). Option B reflects your actual duty: carry out horizon scanning, identify the trend's potential impact and opportunity, and convert it into roadmap-ready recommendations - measured, evidenced, and timed.

**Question 15 (moderate) - Sustainability arithmetic.** Your sustainability assessment compares hosting estates. The legacy data centre consumes 1,800 MWh per year with a power usage effectiveness (PUE) of 2.0; the cloud region achieving the same computing output would consume 750 MWh with a PUE of 1.25. The IT equipment's useful energy is total consumption divided by PUE. By what percentage does the migration reduce total energy consumption?

A) 37.5%
B) 58.3%
C) 33.3%
D) 62.5%

**Correct answer: B.** Total consumption falls from 1,800 MWh to 750 MWh: reduction = (1,800 − 750) ÷ 1,800 = 1,050 ÷ 1,800 = 0.583 = 58.3%. The PUE figures are context (they explain why the cloud estate is more efficient - less energy lost to cooling and overhead per unit of useful computing) but the question asks about total consumption, so the calculation needs only the headline figures. Distractor D (62.5%) comes from comparing useful energy (1,800 ÷ 2.0 = 900 versus 750 ÷ 1.25 = 600; reduction 300 ÷ 900 = 33.3% - which is distractor C) incorrectly, and 37.5% from mixing the two bases. Recommending sustainability is an explicit duty in your role profile, and energy arithmetic like this is increasingly standard in government business cases - including knowing which figure answers which question.

**Question 16 (challenging) - Risk exposure quantification.** Your architectural risk register quantifies three risks affecting multiple teams. Risk R1: probability 40%, financial impact £750,000. Risk R2: probability 15%, impact £2,400,000. Risk R3: probability 60%, impact £500,000. A mitigation costing £180,000 would halve the probability of R2 and reduce R3's impact by £200,000. What is the change in total expected exposure, net of the mitigation cost?

A) Reduction of £300,000
B) Reduction of £120,000
C) Reduction of £480,000
D) Increase of £60,000

**Correct answer: B.** Before: R1 = 0.4 × £750,000 = £300,000; R2 = 0.15 × £2,400,000 = £360,000; R3 = 0.6 × £500,000 = £300,000; total £960,000. After: R1 unchanged at £300,000; R2 = 0.075 × £2,400,000 = £180,000; R3 = 0.6 × £300,000 = £180,000; total £660,000. Gross reduction: £960,000 − £660,000 = £300,000 (distractor A stops here). Net of the £180,000 mitigation cost: £300,000 − £180,000 = £120,000. The mitigation is worth doing, but by a slimmer margin than the gross figure suggests - and presenting the net figure is what makes your recommendation trustworthy when the finance director checks it. Using expected-value arithmetic to manage technical risks at the appropriate level is the quantitative backbone of the architectural governance contribution named in your skills.

### Preparation tips

- **Rebuild the arithmetic of a real business case.** Take a recent options appraisal or benefits case from your portfolio and recompute its totals, unit costs, and break-even points from the raw figures. This is the most role-faithful practice available, and you will occasionally find real errors - which is its own reward.
- **Drill the core operations until they are automatic.** Percentage change ((new − old) ÷ old), compound growth (multiply repeatedly, never add), weighted averages, and ratio splits cover most items. Speed comes from recognising which operation applies, not from calculating faster.
- **Write intermediate results down.** Multi-step items punish mental chaining. Even with an onscreen calculator, jot each intermediate figure; transcription is cheaper than recomputation.
- **Practise reading tables before questions.** Spend the first ten seconds on headers, units, and scale qualifiers ("£000s", "per quarter", "cumulative"). Most wrong answers are extraction errors, not calculation errors.
- **Use estimation to sanity-check.** Before selecting an answer, ask whether its magnitude is plausible. If a "saving" exceeds the original budget, or a percentage lands above 100% where it should not, you have caught an error worth ten seconds.
- **Keep calm about the calculator.** These tests measure interpretation, not arithmetic virtuosity. As a senior professional you interpret financial data weekly; the assessment is a time-compressed version of a familiar task.

### Common pitfalls

- **Misreading chart and table labels** - confusing monthly with annual data, or ignoring scale qualifiers like "in thousands" or "in millions". For an architect this maps to the real-world discipline of checking whether a platform cost is per environment or per service.
- **Over-calculating** - performing precise multi-decimal work when estimation and elimination would identify the answer faster. If three options are impossible on magnitude alone, choose the fourth and bank the time.
- **Time-sink questions** - getting stuck on a single multi-stage problem instead of skipping it and returning. One abandoned hard item costs four points less than four unattempted easy ones.
- **Period-counting errors** - "years 2 to 4" is three years; a five-year appraisal with go-live in year 2 gives four years of benefits. Contracts, licences, and benefit streams all hinge on inclusive counting.
- **Answering the wrong question** - computing the new value when the delta is asked, the total when the unit cost is asked, or the platform's break-even when the organisation's is asked. Re-read the final sentence of the question before committing.
- **Anchoring on absolute numbers when the policy is expressed in percentages** (or vice versa) - thresholds, utilisation rules, and tolerance bands live in the metric they are written in; convert to that metric before judging.


## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment evaluates how well you understand, analyse, and draw correct conclusions from written business information, mirroring the exact reading and comprehension demands of your role. Passages use relevant terminology - in your case, strategy documents, architectural standards, governance terms of reference, policy extracts, and senior stakeholder correspondence - and you must answer based strictly on the text provided, deliberately setting aside your outside knowledge.

The classic format presents a dense passage followed by statements you judge as **True** (the passage logically supports it), **False** (the passage contradicts it), or **Cannot Say** (the passage provides insufficient information either way). Multiple-choice comprehension items - "which statement best summarises the author's position?" - often appear alongside. Timing is tight: typically less than a minute per question, simulating workplace deadlines where you must extract exactly what a document commits to before a meeting starts.

Why does this matter for your role? Reading with forensic precision is arguably the most understated skill in enterprise architecture. You lead the communication of complicated, complex or risky architecture topics; you cannot do that safely if you have misread what a strategy actually promises or what a standard actually mandates. You assure that decisions align with the enterprise architecture strategy - which requires knowing precisely what the strategy says, as opposed to what everyone assumes it says. You establish architectural principles, policies and standards, where a single ambiguous modal verb ("should" versus "must") changes what delivery teams are obliged to do. And in stakeholder negotiations, the difference between "the department will adopt the platform" and "the department intends to adopt the platform" can be the difference between a dependency you can plan on and one you cannot. Verbal reasoning assessments compress all of this into scored practice.

### What it measures for your role

Mapping verbal reasoning dimensions to the named skills in your role profile:

- **Precise extraction of obligations and commitments** maps to **Making architectural decisions** and your duty to establish architectural principles, policies and standards: governance rests on what documents actually require, and "must", "should", "may", and "intends to" each create different obligations.
- **Distinguishing stated fact from inference and assumption** maps to **Architecture communication**: managing stakeholder expectations effectively begins with not over-reading what stakeholders have committed to in writing, and not letting others over-read what you have written.
- **Summarising dense material accurately** maps to **Architecture communication** and **Strategy design**: adapting your message to your audience requires first compressing a document without distorting it - executive summaries that subtly overstate a strategy are a leading cause of downstream misalignment.
- **Detecting contradiction and consistency across text** maps to **Enterprise architecture** and **Architect for the whole context**: strategies, standards, and programme documents written by different authors at different times routinely conflict, and finding those conflicts is core assurance work.
- **Reading commercial and policy language** maps to **Commercial perspective**: contract schedules, framework terms, and sourcing policies are exactly the kind of dense prose these tests simulate.

### Practice questions

For each passage, judge the statements strictly on the text. Explanations point back to the exact wording.

**Passage 1 - extract from a departmental digital strategy:**

"The department will consolidate its application estate from 340 systems to fewer than 200 by the end of the spending review period. Consolidation decisions will be guided by the enterprise architecture principles, in particular reuse of existing platforms. Where a system supports a statutory function, decommissioning will require ministerial notification. The department intends to adopt the cross-government notification platform for all new services, subject to a satisfactory security assessment. No system will be decommissioned without a transition plan approved by the design authority."

**Question 1 (easy).** True, False, or Cannot Say: "The department has committed to reducing its application estate to fewer than 200 systems by the end of the spending review period."

**Correct answer: True.** The passage states the department "will consolidate its application estate from 340 systems to fewer than 200 by the end of the spending review period". "Will" expresses a firm commitment, and the statement reproduces the target and timeframe accurately. Note what makes this True rather than Cannot Say: the statement adds nothing beyond the text - no interpretation, no extra conditions.

**Question 2 (moderate).** True, False, or Cannot Say: "The department has committed to adopting the cross-government notification platform for all new services."

**Correct answer: False.** The passage says the department "intends to adopt" the platform "subject to a satisfactory security assessment". An intention subject to a condition is not a commitment; the statement drops both the softer verb and the caveat. This is the single most valuable distinction in the whole assessment for your role: when you build roadmaps on other organisations' documents, conditional intentions must never be recorded as dependencies you can rely on. (If you judged this Cannot Say, note that the passage does give enough information: it tells us the adoption is conditional, which directly contradicts the unconditional commitment claimed.)

**Question 3 (moderate).** True, False, or Cannot Say: "Decommissioning a system that supports a statutory function requires ministerial approval."

**Correct answer: False.** The passage requires ministerial *notification*, not approval. Notification means informing; approval means obtaining consent. The statement substitutes a stronger obligation than the text creates. Architects live and die by such distinctions - a governance process that requires notifying a board is materially different from one requiring the board's sign-off, and conflating them either blocks delivery unnecessarily or exposes the organisation to challenge.

**Question 4 (moderate).** True, False, or Cannot Say: "The design authority has approved transition plans for the systems decommissioned so far."

**Correct answer: Cannot Say.** The passage establishes a rule - "no system will be decommissioned without a transition plan approved by the design authority" - but says nothing about whether any systems have been decommissioned yet, or whether the rule has been followed in practice. A rule's existence tells you nothing about historical compliance. This mirrors the assurance trap flagged in the cognitive section: "the standard requires X" does not entail "X has happened".

**Question 5 (easy).** Which of the following best summarises the passage's approach to consolidation?

A) Consolidation at maximum speed, with all constraints removed
B) Principle-guided consolidation with governance safeguards for statutory functions and transitions
C) Consolidation delegated entirely to delivery teams
D) A freeze on all decommissioning until the security assessment completes

**Correct answer: B.** The passage pairs a numeric consolidation target with three safeguards: principle-guided decisions ("guided by the enterprise architecture principles"), ministerial notification for statutory systems, and design authority approval of transition plans. Option A ignores the safeguards, option C contradicts the central governance role, and option D wrongly attaches the security assessment (which conditions notification-platform adoption) to decommissioning generally. Summary items reward mapping each clause of the correct option back to a specific sentence.

**Passage 2 - extract from an architectural standard:**

"All application programming interfaces (APIs) exposed beyond a service boundary must be registered in the enterprise API catalogue before first production use. Internal APIs, defined as those consumed solely within a single service boundary, should be registered but are exempt from mandatory review. The architecture review board may grant a time-limited exemption from registration where a supplier contract predates this standard; such exemptions must be recorded in the exemptions register and expire after no more than twelve months. Exempted APIs remain subject to the security standard."

**Question 6 (moderate).** True, False, or Cannot Say: "An internal API that is never registered breaches this standard."

**Correct answer: False.** For internal APIs the standard says they "should be registered" - a recommendation - and explicitly exempts them from mandatory review. "Should" does not create a breachable obligation in the way "must" does; failing to follow a "should" is non-adoption of guidance, not a breach of a mandatory requirement. The contrast with the first sentence ("must be registered") is deliberate, and assessments - like standards authors - expect you to notice the modal shift between adjacent sentences.

**Question 7 (challenging).** True, False, or Cannot Say: "An API exposed beyond a service boundary under a supplier contract signed after this standard came into force can be granted a registration exemption by the architecture review board."

**Correct answer: False.** The exemption power is conditioned on "a supplier contract [that] predates this standard". A contract signed after the standard came into force does not predate it, so the stated basis for exemption is absent. Read carefully: the board "may grant" exemptions only in the circumstance described; the passage offers no other exemption route. The trap is over-generalising the board's discretion - "may grant" feels permissive, but the permission is scoped by its "where" clause.

**Question 8 (challenging).** True, False, or Cannot Say: "An API with a valid registration exemption is not required to comply with the security standard."

**Correct answer: False.** The final sentence states plainly: "Exempted APIs remain subject to the security standard." The statement contradicts it directly. This item is easy once spotted, but under time pressure many candidates stop reading a passage once they have answered earlier questions from it; the last sentence of a standard is often where the sting lives - in real standards just as in assessments.

**Passage 3 - email from a programme director to the senior enterprise architect:**

"Thanks for the assurance report. I accept the finding that our integration approach diverges from the target architecture, and we will bring a revised design to the review board next month. However, I want to be clear that the divergence was approved by the previous lead architect in 2023 as a tactical measure, and my team has delivered against that approved position in good faith. Any remediation cost beyond the £250,000 we have already provisioned would need to come from portfolio contingency, which I understand is heavily committed. I would welcome your support in presenting a phased remediation option to the board rather than the immediate cutover your report recommends."

**Question 9 (moderate).** True, False, or Cannot Say: "The programme director disputes the finding that the integration approach diverges from the target architecture."

**Correct answer: False.** The email opens: "I accept the finding that our integration approach diverges from the target architecture." Acceptance is the opposite of dispute. Under time pressure, the email's generally defensive tone can mislead you into inferring a dispute; the discipline is to check the claim against the actual words, not the mood. Stakeholders very often accept findings while contesting remedies - reading which of the two is being contested is essential to managing expectations effectively.

**Question 10 (challenging).** True, False, or Cannot Say: "Portfolio contingency is insufficient to fund remediation beyond the programme's £250,000 provision."

**Correct answer: Cannot Say.** The director says contingency "is heavily committed", and frames this as his understanding ("which I understand is..."). "Heavily committed" is not "insufficient" - a heavily committed fund may still have enough uncommitted balance for this remediation - and the claim is second-hand. The passage gives neither the contingency's size nor the remediation cost. Treating a stakeholder's characterisation as established fact is precisely how architects get blindsided in board meetings; verify with the portfolio office before repeating it.

**Question 11 (moderate).** True, False, or Cannot Say: "The divergence was approved as a tactical measure in 2023."

**Correct answer: Cannot Say.** The director *asserts* the previous lead architect approved it in 2023, but the passage provides no corroboration - no decision record, no confirmation from the architecture function. A careful reader distinguishes "the email states X happened" from "X happened". Strictly, the passage tells you only what the director claims. In assessment terms, statements about the world reported inside a passage by an interested party are classic Cannot Say material; in workplace terms, this is why you check the decision log before the board meeting - and why maintaining a complete decision log protects everyone, including delivery teams acting in good faith.

**Question 12 (moderate).** What is the programme director primarily requesting?

A) That the assurance finding be withdrawn
B) That the architect support a phased remediation option instead of immediate cutover
C) Additional funding of £250,000
D) An apology for the previous lead architect's decision

**Correct answer: B.** The email's closing sentence carries the request: "I would welcome your support in presenting a phased remediation option to the board rather than the immediate cutover your report recommends." Everything before it is context-setting and gentle pressure (good faith, prior approval, constrained funding) building towards that ask. Options A, C, and D are not requested anywhere. Identifying the operative ask inside a diplomatically padded email is a daily senior-architect skill - and knowing that the padding is advocacy, not evidence, is its twin.

**Passage 4 - extract from a cross-government platform's terms of adoption:**

"Departments adopting the platform receive a service level commitment of 99.5% monthly availability, measured at the platform boundary. The commitment excludes downtime arising from a department's own configuration and from scheduled maintenance windows notified at least ten working days in advance. Departments may not modify platform core components. Extensions developed by a department must pass the platform conformance test suite before deployment, and the platform team may withdraw an extension that degrades shared service performance, giving five working days' notice except where degradation is severe."

**Question 13 (moderate).** True, False, or Cannot Say: "If severe degradation occurs, the platform team may withdraw a department's extension without five working days' notice."

**Correct answer: True.** The notice obligation applies "except where degradation is severe" - the exception removes the five-day notice requirement in severe cases. The statement restates that exception accurately. Exception clauses are where assessment writers - and contract drafters - concentrate their traps; a reader who stops at "giving five working days' notice" answers False and plans a dependency on notice they may not get.

**Question 14 (challenging).** True, False, or Cannot Say: "A month in which the platform is unavailable for 0.6% of the time, entirely due to an unnotified emergency maintenance window, breaches the service level commitment."

**Correct answer: True.** Work the exclusions: the commitment excludes (a) downtime from the department's own configuration and (b) scheduled maintenance notified at least ten working days in advance. An *unnotified emergency* maintenance window meets neither exclusion - it is not the department's configuration, and it was not notified ten working days ahead - so its downtime counts against availability. 0.6% unavailability means 99.4% availability, below the 99.5% commitment; therefore breached. Two-step items like this (classify the downtime, then apply the threshold) reward methodical reading over speed, and they replicate exactly how you would assess a supplier's claim that an outage "doesn't count".

**Question 15 (easy).** True, False, or Cannot Say: "Departments are permitted to modify platform core components if their extension passes the conformance test suite."

**Correct answer: False.** "Departments may not modify platform core components" is unconditional. The conformance test suite governs *extensions*, a different category. The statement smuggles a permission from one clause into a prohibition in another - a manoeuvre you will recognise from delivery teams creatively interpreting standards, and one that verbal reasoning tests simulate constantly.

**Passage 5 - extract from a sourcing policy note prepared by the commercial team:**

"For technology capabilities assessed as commodity, the default sourcing route is an existing cross-government framework, and any departure from the default requires a written value-for-money justification approved by the commercial director. Capabilities assessed as differentiating may be sourced through single-supplier negotiation only where fewer than three capable suppliers exist on relevant frameworks; otherwise a competition must be run. The architecture function is responsible for the commodity-versus-differentiating assessment and must record its rationale in the sourcing decision log. Assessments older than eighteen months must be refreshed before being relied upon for a new procurement. Nothing in this policy overrides the department's obligations under public procurement regulations."

**Question 16 (moderate).** True, False, or Cannot Say: "A commodity capability may be sourced outside a cross-government framework."

**Correct answer: True.** The framework route is described as "the default", and the passage explicitly provides for departure: "any departure from the default requires a written value-for-money justification approved by the commercial director." A route that can be departed from with justification and approval is permitted, conditionally. Candidates who answer False have read "default" as "mandatory" - an upgrade error. Candidates who answer Cannot Say have missed that the departure mechanism is stated in the text itself. Understanding when each sourcing route applies, and who must approve exceptions, is the commercial perspective skill in your profile rendered as a reading task.

**Question 17 (challenging).** True, False, or Cannot Say: "A differentiating capability with four capable suppliers on relevant frameworks may be sourced through single-supplier negotiation if the commercial director approves."

**Correct answer: False.** Single-supplier negotiation for differentiating capabilities is permitted "only where fewer than three capable suppliers exist on relevant frameworks; otherwise a competition must be run". Four suppliers is not fewer than three, so a competition is mandatory. The commercial director's approval power appears in a different clause - departures from the framework default for *commodity* capabilities - and grants no authority here. The trap combines two clauses that both mention commercial authority; keeping each power attached to its own conditions is exactly how you must read delegation schemes and governance terms of reference.

**Question 18 (moderate).** True, False, or Cannot Say: "The architecture function's assessment of a capability, made two years ago, can be relied upon for a new procurement provided the sourcing decision log records its rationale."

**Correct answer: False.** "Assessments older than eighteen months must be refreshed before being relied upon for a new procurement." Two years exceeds eighteen months, so the assessment must be refreshed regardless of how well its rationale was recorded. The statement offers a plausible-sounding substitute condition (the decision log) that the text never accepts as an alternative to refreshing. Watch for answers that satisfy *a* requirement in the passage rather than *the* requirement in play.

**Question 19 (easy).** Which statement best captures the relationship between this policy and public procurement regulations?

A) The policy takes precedence over the regulations
B) The regulations apply only when the policy is silent
C) The policy operates subject to the regulations, which it does not override
D) The passage does not address the relationship

**Correct answer: C.** The final sentence states: "Nothing in this policy overrides the department's obligations under public procurement regulations." Internal policy sits beneath the law - a hierarchy you rely on when a delivery team argues that an internal exemption also disposes of a regulatory duty. Once again the last sentence of the passage does decisive work, which is a drafting habit worth internalising both as a reader and as an author of architectural policies and standards.

**Question 20 (challenging).** True, False, or Cannot Say: "The commercial team, rather than the architecture function, decides whether a capability is commodity or differentiating."

**Correct answer: False.** The passage assigns the assessment explicitly: "The architecture function is responsible for the commodity-versus-differentiating assessment." The fact that the policy note was *prepared by* the commercial team describes its authorship, not the allocation of the decision. Separating who wrote a document from who holds the responsibilities it describes sounds trivial, but under a minute of time pressure the framing sentence ("prepared by the commercial team") primes exactly this confusion - and in real organisations, authorship of a policy is routinely mistaken for ownership of its decisions.

### Preparation tips

- **Read the statement before re-reading the passage.** Skim the passage once for structure, then let each statement direct you back to the specific sentence that decides it. Hunting keywords beats re-reading wholesale - the same technique you use to assure a 60-page design against a two-page standard.
- **Build a modal-verb reflex.** Train yourself to flag "must", "should", "may", "will", "intends to", and "subject to" automatically as you read. Most True/False/Cannot Say items for professional roles turn on exactly these words, and so do most governance disputes.
- **Rehearse the Cannot Say discipline.** Cannot Say means the passage neither supports nor contradicts the statement. Practise articulating *why*: "the passage states an obligation, not whether it was met", "the claim is reported by an interested party", "the quantity is not given". If you can name the gap, you can trust the answer.
- **Suspend your expertise deliberately.** You know more about architecture governance than any passage will state. Before answering, ask: "is my evidence in the text, or in my experience?" Only the text scores.
- **Practise on authentic material.** Government strategies, technology codes of practice, service standards, and framework agreements are freely published; take a paragraph and write your own True/False/Cannot Say statements. Composing items teaches the traps faster than answering them.
- **Manage the clock by passage, not by question.** Passages amortise reading cost across their questions, so never abandon a passage after reading it - answer all its items before moving on.
- **Verbalise borderline judgements in one sentence.** When torn between False and Cannot Say, force yourself to complete one of two sentences: "the passage contradicts this because it says..." or "the passage is silent on this because it never addresses...". If you cannot complete either sentence with a quotation or a named gap, re-read the decisive clause once more. This thirty-second habit converts vague unease into an auditable judgement - the same move you make when you challenge a design document in review and need to point at the exact sentence that fails.
- **Warm up immediately before the test.** Verbal precision degrades when cold. Ten minutes with any dense document - reading one paragraph and stating exactly what it does and does not commit to - primes the forensic reading mode the assessment rewards, just as you would skim the papers before chairing a review board.

### Common pitfalls

- **Making assumptions** - bringing personal or professional knowledge instead of relying only on the provided text. For experienced architects this is the dominant failure mode: the more senior you are, the more plausible your assumptions feel.
- **Confusing likelihood with fact** - a passage saying an outcome is "expected" or "intended" does not make it true; "the department intends to adopt" is not "the department will adopt", and neither is "the department has adopted".
- **Upgrading or downgrading obligations** - reading "notification" as "approval", "should" as "must", or "may grant where X" as "may grant". Restate the obligation in the text's own strength before judging the statement.
- **Missing exceptions and final clauses** - exclusions, carve-outs, and the last sentence of a passage decide a disproportionate share of items, because that is how real standards and contracts are drafted too.
- **Treating reported claims as established facts** - when a passage quotes a stakeholder's assertion, the fact established is that the assertion was made, not that it is true.
- **Poor time management** - spending too long on a first full read instead of scanning for the keywords each statement puts in play. Under a minute per question, technique is the difference between finishing and guessing the final third.


## Workplace job-specific situational judgement assessment

### About this assessment

A workplace job-specific situational judgement assessment evaluates your decision-making, interpersonal skills, and professional conduct by presenting realistic workplace dilemmas and asking how you would respond. Unlike logic or numeric tests, there is no single objectively right answer computed from data: several responses may seem reasonable, but one aligns best with the organisation's values and the demands of the role. For a senior enterprise architect in UK government, the scenarios draw on your real stakeholder landscape - lead architects, delivery teams, programme directors, commercial colleagues, security teams, and senior business leaders - and your real tensions: pace versus assurance, tactical delivery versus strategic coherence, influence without direct authority.

Response formats vary. The most common ask you to select the **most effective** and **least effective** actions from a set, or to **rank or rate** all options from best to worst. Timing is usually untimed or generous, because these assessments measure natural judgement rather than speed. Scoring compares your choices against a key derived from experienced practitioners and the organisation's values - in the UK public sector context, that means user needs, transparency, collaboration, accessibility, and inclusion, alongside the Civil Service values of integrity, honesty, objectivity, and impartiality.

Why does this matter for your role? Almost every duty in your role profile is exercised through other people. You lead and influence delivery of cross-cutting capabilities; you consult and support collaboration across the business; you advocate on behalf of teams; you manage stakeholder expectations; you develop the architecture community. Enterprise architects hold little formal authority over the programmes they guide - judgement about *how* to intervene, *when* to escalate, and *whose* interests to weigh is the operating system of the role. Situational judgement assessments make that judgement visible and comparable.

### What it measures for your role

Mapping situational judgement dimensions to the named skills in your role profile:

- **Stakeholder management and influence** maps to **Architecture communication**: leading communication of complicated, complex or risky topics with technical and non-technical stakeholders, adapting your message to your audience, and managing expectations - most scenarios test whether you inform, consult, persuade, or escalate at the right moment.
- **Collaboration and community behaviour** maps to **Community collaboration**: working collaboratively in a group, giving feedback that is effective and lasting, spotting problems in team dynamics and rectifying them - including through Agile health checks.
- **Balancing local and enterprise interests** maps to **Architect for the whole context**: supporting wider organisational objectives beyond your immediate goals, and influencing colleagues across the organisation to solve or mitigate problems.
- **Escalation and governance judgement** maps to **Making architectural decisions**: using architectural governance and assurance at the appropriate level - neither smothering delivery in process nor letting multi-team risks pass unaddressed.
- **Strategic stewardship** maps to **Strategy design** and your role-level duty to play a part in successful delivery of the long-term strategy: protecting the strategy's intent while adapting it in response to feedback and findings.
- **Commercial propriety** maps to **Commercial perspective**: knowing the appropriate internal contacts and processes when situations acquire commercial dimensions.

### Practice questions

For each scenario, decide your answer before reading the ratings. The explanations discuss why each option is stronger or weaker against UK public sector values.

**Question 1 (moderate) - The principle-breaching programme with air cover.** A high-profile programme, personally sponsored by a director general, plans to procure a solution that duplicates an existing enterprise platform, breaching the reuse principle you established. The programme director tells you: "The DG wants this delivered this year. Raise objections and you'll be seen as blocking." Choose the MOST and LEAST effective actions.

A) Document the breach in the assurance record but take no further action, noting you were overruled.
B) Meet the programme director to understand the drivers, quantify the duplication cost and delivery impact of both routes, and present the comparison to the programme board and design authority with options - including a time-limited exception with convergence conditions.
C) Email the director general directly, copying the programme director, stating the programme is in breach of enterprise architecture policy.
D) Agree to support the procurement in exchange for the programme funding a later migration to the enterprise platform.

**Most effective: B. Least effective: A.** Option B does everything the role demands: it seeks to understand before opposing (collaboration), converts an abstract principle into evidence a board can weigh (value for money, transparency), routes the decision through legitimate governance rather than personality, and offers a pragmatic middle path - the time-limited exception - that respects delivery pressure while protecting the strategy. Option A is worst because silent documentation is self-protective rather than organisation-protective: the risk lands on citizens and taxpayers while the assurance record protects only you. Option C escalates over the programme director's head before attempting resolution, spending political capital and breaching the collaborative norm - escalation is legitimate, but as a next step, not a first one. Option D trades governance for a promise: informal side-deals subvert transparent decision-making, and unfunded "later migrations" rarely happen. Note the general pattern, which recurs across senior-architect scenarios: understand, quantify, offer options, use governance - in that order.

**Question 2 (moderate) - The struggling community member.** In the architecture community you help develop, a mid-level architect has presented two poorly-prepared design reviews in a row. Other architects have begun quietly excluding them from discussions. You are not their line manager. Choose the MOST and LEAST effective actions.

A) Speak with them privately, share specific observations about the two reviews, ask what is getting in the way, and offer to pair on preparing the next review.
B) Raise their performance with their line manager so it can be addressed through formal channels.
C) Do nothing; performance management is not your responsibility, and intervening could overstep.
D) At the next community session, use the two reviews as anonymised examples of what a design review should avoid.

**Most effective: A. Least effective: D.** Option A embodies the community collaboration skill: feedback that is specific, private, curious about causes, and paired with practical support is the kind that is "effective and lasting". It also addresses the exclusion dynamic at its root. Option B is not wrong as a later step - especially if causes are beyond your reach - but jumping straight to formal channels without speaking to the person first is neither collaborative nor proportionate, and it forfeits the trust your community role depends on. Option C mistakes the absence of line authority for the absence of responsibility: developing the architecture community is explicitly in your role, and inclusion is a public sector value under active threat here (colleagues are being excluded). Option D is worst: "anonymised" examples that everyone can attribute are public humiliation dressed as teaching; it would entrench the exclusion, poison psychological safety in the community, and teach every member that presenting carries reputational risk - the opposite of a learning culture.

**Question 3 (challenging) - The tactical decision that is quietly becoming permanent.** Eighteen months ago, the design authority approved a "temporary" point-to-point integration for one programme, with a condition to migrate to the enterprise integration platform "within twelve months". The migration has not happened; meanwhile two further teams have copied the pattern, citing the first approval as precedent. The original programme's architect tells you the migration budget was reallocated and the team considers the matter closed. Choose the MOST and LEAST effective actions.

A) Raise the expired condition and its spreading precedent at the design authority, with a proposed remediation path and sequencing for all three teams, and ask the authority to reaffirm or consciously revise the target position.
B) Instruct the two newer teams to stop using the pattern immediately, since their designs were never individually approved.
C) Accept the reality: three teams now use the pattern, so update the target architecture to make point-to-point integration an approved standard.
D) Ask the original programme to reinstate its migration budget before the next planning round, and revisit the issue then.

**Most effective: A. Least effective: C.** This scenario tests stewardship of the long-term strategy against the slow erosion that actually kills enterprise architectures - not dramatic breaches, but expired conditions nobody polices. Option A treats the governance system as the instrument: it surfaces the expired condition transparently, addresses all three teams rather than scapegoating one, brings a constructive remediation proposal rather than bare complaint, and - crucially - invites the authority to *consciously* decide, preserving the legitimacy of whatever position results. Option B has the right instinct on the newer teams but exercises authority you may not have, and an abrupt instruction without a migration path simply drives the pattern underground. Option D is the passive option in disguise: it accepts a twelve-month delay on a condition already six months overdue, and its remedy depends on a team that considers the matter closed. Option C is least effective because it converts drift into doctrine: revising strategy in response to findings is legitimate (your strategy design skill explicitly includes it), but doing so *because policing failed* rewards non-compliance and signals that any condition can be outlasted. If the pattern genuinely merits a place in the target architecture, that case should be made on its merits at the design authority - which is what option A enables.

**Question 4 (moderate) - The horizon-scanning enthusiasm problem.** After your horizon-scanning briefing on an emerging technology, a business director becomes enthusiastic and announces to their leadership team that they will pilot it next quarter, naming your briefing as the endorsement. You assess the technology as promising but immature, with significant data protection questions unresolved. Choose the MOST and LEAST effective actions.

A) Let the pilot proceed; enthusiasm for emerging technology is rare and valuable, and the pilot will surface the issues naturally.
B) Meet the director promptly: affirm the interest, clarify what your briefing did and did not conclude, and offer to co-shape a bounded proof of concept with explicit success criteria and data protection guardrails.
C) Send a written correction to the director's leadership team stating that your briefing was not an endorsement.
D) Raise the matter with the data protection officer so the pilot is blocked before it gains momentum.

**Most effective: B. Least effective: A.** Option B captures the senior-architect balancing act: horizon scanning exists to create exactly this kind of appetite, so the response protects the relationship and the energy while correcting the record and installing guardrails - converting a risky announcement into a governed experiment. It manages expectations directly with the stakeholder, which is your communication skill in action. Option A is least effective because it lets a known misrepresentation of your professional advice stand and allows unresolved data protection questions to ride on organisational enthusiasm - issues surfacing "naturally" in a pilot involving personal data is a euphemism for incidents. Option C corrects the record but by the most face-costing route available, embarrassing the director in front of their leadership team before any private conversation; expect the relationship - and your future influence in that directorate - to pay for it. Option D outsources your judgement to a control function as a blocking manoeuvre: involving the data protection officer is right, but as part of shaping the work (as in B), not as a way to kill it by proxy without ever speaking to the director.

**Question 5 (moderate) - Conflicting stakeholders on strategy.** You are drafting the data architecture strategy. The finance director wants consolidation onto a single analytics platform to cut licence spend; the operations director insists their domain's specialised tooling is non-negotiable; the lead architect - your senior - is on extended leave and unreachable for three weeks, and the strategy is due at the investment board in four. Choose the MOST and LEAST effective actions.

A) Delay the strategy until the lead architect returns, informing the investment board secretariat of a one-month slip.
B) Draft the strategy reflecting the finance director's position, since value for money will carry the board.
C) Convene both directors (or their deputies), map the genuine requirements behind each position, and draft a strategy with a consolidation default plus criteria-based exceptions - documenting the trade-offs openly for the board and briefing the lead architect's delegate.
D) Draft two alternative strategies, one per director, and let the investment board choose.

**Most effective: C. Least effective: D.** Option C works the actual skill set: strategy design that aligns with organisational objectives, stakeholder collaboration to assure decisions are aligned, and a defensible middle structure - a default with transparent, criteria-based exceptions - that converts a personality conflict into an architectural policy. It also respects governance continuity by briefing the lead architect's delegate: supporting lead architects is your role level's defining relationship, and their absence does not suspend it. Option A treats the deadline as the variable and your judgement as unavailable - but a senior enterprise architect exists precisely to progress strategy within agreed guardrails when seniors are away; a full month's slip to the investment board for an avoidable reason damages the function's credibility. Option B mistakes advocacy for analysis: adopting one stakeholder's position wholesale because it "will carry the board" is neither objective nor durable - the operations director's requirements will resurface as delivery-time exceptions. Option D is least effective because it abdicates the architect's core value: boards commission architects to integrate competing concerns into a recommendation; presenting two partisan drafts exports your job to a committee, guarantees a loser who never bought in, and signals that the architecture function cannot synthesise - an impression that outlasts the decision.

**Question 6 (challenging) - The commercial boundary.** During a procurement you are supporting, a supplier's account director - whom you know well from a previous programme - invites you to dinner and mentions they could "walk you through their roadmap privately, so your evaluation has the full picture". The procurement is live, and you sit on the evaluation panel. Choose the MOST and LEAST effective actions.

A) Accept, but keep the conversation general and pay for your own meal.
B) Decline the dinner, explain that a live procurement restricts contact to the formal channels, log the approach with the commercial team, and suggest the supplier submit roadmap material through the procurement portal so all bidders are treated equally.
C) Decline the dinner without explanation and mention it to no one.
D) Ask a colleague who is not on the evaluation panel to attend the dinner instead and brief you afterwards.

**Most effective: B. Least effective: D.** Option B demonstrates the commercial perspective skill precisely: understanding commercial processes means knowing that during a live procurement, information flows through formal channels so that no bidder gains privileged access, and knowing the appropriate internal contacts means logging the approach with the commercial team - protecting you, the supplier relationship, and the procurement's integrity simultaneously. Redirecting the roadmap material into the portal preserves the useful information while equalising it. Option A fails regardless of who pays: the impropriety is the private information channel, not the meal's cost. Option C avoids the immediate risk but conceals the approach - if the supplier later makes similar approaches to others, the pattern stays invisible, and your unexplained refusal does nothing to educate the supplier about process. Option D is least effective because it launders the impropriety through a colleague: the private briefing still reaches an evaluator, now with an extra person implicated and a step of deniability added - which makes it worse than the original offer, converting a boundary problem into a scheme. Transparency is the value under test, and D is its inversion.

**Question 7 (moderate) - Agile health check reveals a dynamic problem.** An Agile health check you run with a delivery team surfaces that the team's architect is overruling developers' design proposals without discussion, and velocity and morale are falling. The architect is technically strong, respected by governance boards, and reports to a different manager. Choose the MOST and LEAST effective actions.

A) Share the health-check themes with the whole team, including the architect, and facilitate a session agreeing how design decisions will be made and challenged.
B) Report the architect's behaviour to their line manager, recommending they be moved to a less team-facing role.
C) Quietly advise the developers to route their proposals through you so they get a fair hearing.
D) Take no action; velocity fluctuates, and the architect's designs are technically sound.

**Most effective: A. Least effective: C.** Your community collaboration skill explicitly includes identifying issues through Agile health checks and helping to stimulate the right responses - and the right response to a decision-making dynamic is to fix the decision-making process with the people in it. Option A treats the health check's findings transparently, keeps the architect inside the solution rather than casting them as the accused, and produces a durable artefact: an agreed way of working that outlives personalities. Option B escalates before any direct feedback has been attempted and proposes a punitive outcome on one health check's evidence - disproportionate, and a message to every team that health checks are surveillance. Option D ignores a leading indicator your role exists to catch: falling morale plus suppressed technical dissent is how design quality quietly dies even when today's decisions are sound. Option C is least effective because it institutionalises the dysfunction: routing proposals through you creates a shadow decision path, undermines the architect without ever giving them feedback, makes the team dependent on your patronage, and violates the transparency the health check was meant to serve. Interventions that feel kind but bypass the real conversation are a recurring least-effective pattern in situational judgement tests - and in careers.

**Question 8 (challenging) - The accessibility late-discovery.** Four weeks before a citizen-facing service's public launch, an assurance review you commission finds the chosen front-end framework - selected by the programme against your team's earlier advice - cannot meet the accessibility standard for screen-reader users without significant rework. The programme director proposes launching on schedule and fixing accessibility in the next quarter, noting that "only a small percentage of users are affected". Rank the following actions from most to least effective.

A) Support the launch with a public accessibility statement, a funded and dated remediation plan, and an assisted-digital route for affected users - only if the standard's owner and the service's senior responsible owner formally accept the exception.
B) Advise that the launch be delayed until screen-reader users can complete the service journey, presenting the delivery, legal, and reputational costs of both options to the programme board.
C) Escalate your concern in writing to the senior responsible owner and the departmental accessibility lead, stating that the proposed launch does not meet the service standard.
D) Accept the programme director's plan, since the launch date is their accountability, and record your advice in the assurance log.

**Most effective ranking: B, C, A, D.** Option B ranks first because it does the senior-architect job completely: it takes a values-anchored position - accessibility and inclusion are not percentage games; citizens who use screen readers are exactly whom the standard protects - while presenting the decision-makers with a full, quantified comparison through the proper board. Option C ranks second: written escalation to the accountable owner and the accessibility lead is legitimate and may be necessary, but as a standalone act it transmits concern without offering the board a decision framework - it is B minus the constructive half. Option A ranks third: exceptions processes exist, and a formally accepted exception with funded remediation and an assisted-digital route is how mature organisations handle genuine emergencies - but ranking it above B would mean reaching for the exception before advocating for compliance, inverting the standard's intent; A is the fallback if B's advice is heard and overruled. Option D is least effective: "it's their accountability" plus a defensive log entry is the abdication pattern - the assurance record exists to improve decisions, not to insulate the assurer, and a senior architect who watches an inaccessible service launch with a tidy paper trail has optimised for the wrong outcome entirely.

**Question 9 (moderate) - Credit and visibility.** At a cross-government event, a peer from another department presents an integration approach strikingly similar to one your team shared with them informally six months ago, without attribution. Your team members notice and are aggrieved. Choose the MOST and LEAST effective actions.

A) Raise it publicly in the Q&A, asking the presenter to acknowledge your team's contribution.
B) Speak with the peer privately afterwards: note the similarity, express that your team would value acknowledgement, and propose presenting the next iteration jointly - then tell your team how you have advocated for them.
C) Advise your team to stop sharing work informally with other departments.
D) Let it go entirely; government works best when ideas circulate freely, and attribution is vanity.

**Most effective: B. Least effective: C.** Advocating on behalf of a team to other stakeholders is verbatim in your communication skill, and option B does it without collateral damage: a private conversation preserves the cross-department relationship, the joint-presentation proposal converts grievance into shared platform, and closing the loop with your team addresses the actual wound - their sense that their work vanished unseen. Option A defends the team but at maximum public cost; ambushing a presenter in Q&A poisons a relationship your organisation needs, and cross-government collaboration runs on exactly these relationships. Option D half-understands something true - ideas should circulate - but ignores that your team's morale and your duty to advocate for them are real; sustained uncredited extraction is how sharing cultures die. Option C is least effective because it institutionalises that death: walling your team off from informal exchange punishes the whole ecosystem for one lapse, contradicts the community-building and cross-enterprise networking your role level explicitly requires, and teaches your team that generosity is a mistake. The values at stake - collaboration and openness - survive option A bruised; they do not survive option C.

**Question 10 (challenging) - The strategy feedback you did not want.** Six months after the enterprise architecture strategy you helped author was published, adoption metrics show two of five business domains fully engaged, two partially, and one openly working around it. Feedback from the workaround domain says the strategy's mandated patterns "fit central government transaction services, not our operational field work". Your lead architect, protective of the strategy, is inclined to tighten enforcement. Choose the MOST and LEAST effective actions.

A) Support tightened enforcement; a strategy that bends to every objection is not a strategy.
B) Commission a structured review of the workaround domain's cases, testing whether the mandated patterns genuinely fail their context, and bring the findings - with options ranging from targeted pattern variants to firmer adoption support - to the lead architect and governance board.
C) Quietly allow the workaround domain an unofficial exemption to keep the peace while the other four domains embed.
D) Rewrite the strategy to remove the mandates, making all patterns advisory.

**Most effective: B. Least effective: C.** Your strategy design skill explicitly includes developing or maintaining strategy in response to feedback and findings - option B is that sentence operationalised: it treats the workaround as data rather than defiance, tests the claim empirically before either enforcing or amending, and gives the lead architect an evidence base instead of a loyalty test. It also plays your role-level part - supporting the lead architect in ensuring the strategy is developed, agreed and followed - by improving their options rather than simply executing their first instinct. Option A enforces before diagnosing: if the patterns genuinely fail operational field contexts, tightened enforcement converts one workaround domain into a resistance movement with a legitimate grievance. Option D over-corrects identically in the other direction: dissolving mandates because one domain objects abandons the four domains that invested in compliance, and an all-advisory strategy directs nothing. Option C is least effective because it is invisible governance: an unofficial exemption is a decision nobody made, recorded nowhere, defensible to no one - it undermines the strategy's legitimacy for the compliant domains the moment it becomes known (it always becomes known), and it denies the workaround domain the legitimate exemption or pattern variant a transparent process might actually grant them. Transparency is not a nicety of public sector architecture; it is the mechanism by which strategies retain consent.

### Preparation tips

- **Anchor on the role's centre of gravity: influence through legitimate process.** Across scenarios, the strong options share a shape - understand first, quantify or evidence the concern, offer constructive options, and route decisions through transparent governance. Options that skip to enforcement, concealment, or unilateral action score poorly however efficient they feel.
- **Rehearse the public sector value set explicitly.** Before the assessment, write down: user needs, transparency, collaboration, accessibility, inclusion, integrity, objectivity. For each practice scenario, ask which values are in tension - the best answer usually honours the value under greatest threat without sacrificing the others.
- **Watch for the "protective paperwork" trap.** Options that document, log, or record your position *instead of acting* recur throughout senior-role tests. Records matter, but as instruments of transparent decision-making - not as personal insurance.
- **Distinguish escalation timing, not escalation legitimacy.** Escalation is almost never wrong in principle; it is frequently wrong as a *first* move. The strong pattern is direct conversation, then constructive proposal, then escalation with evidence.
- **Answer as the role, not as your current organisation.** If your department's culture tolerates informal exemptions or heroic unilateralism, set that aside: the scoring key reflects the framework's values, and so should your choices.
- **Take the generous timing seriously.** With little time pressure, read every option fully before rating any - the least effective option is often written to look superficially similar to the most effective one, differing in a single mechanism (private versus public, transparent versus quiet, with the person versus about the person).

### Common pitfalls

- **Answering idealistically rather than effectively** - choosing what sounds noble ("refuse all compromise on principle") over what practically protects users and value for money. Time-limited exceptions with conditions, for example, are often stronger answers than absolute refusals.
- **Selecting passive options** - delaying, deferring to someone's return, logging without acting, or letting a pilot "surface issues naturally". Passivity dressed as patience is the most heavily penalised pattern in senior-role situational judgement tests.
- **Ignoring the organisation's culture and values** - UK public sector scoring keys weight collaboration, transparency, and inclusion heavily; aggressive individual heroics that might score well in some commercial cultures score poorly here.
- **Bypassing the person concerned** - reporting, escalating, or engineering around a colleague before any direct conversation. Almost every scenario involving a person's behaviour rewards talking with them first.
- **Solving the relationship and ignoring the risk, or vice versa** - the strongest options handle both (correct the record and preserve the enthusiasm; decline the dinner and log the approach). If your chosen option addresses only one axis, look for the option that addresses two.
- **Forgetting whose interests the role serves** - when torn between options, ask which one the citizen, the taxpayer, and the long-term strategy would vote for. Enterprise architecture exists to protect exactly the interests that have no seat in the meeting.


## Conclusion

Well done for working through this guide. You have covered the four assessment types most relevant to your work as a senior enterprise architect: cognitive ability exercised on roadmaps, principles, and governance artefacts; numeric reasoning applied to budgets, capacity, sourcing models, and value-for-money cases; verbal reasoning tested against strategies, standards, and stakeholder correspondence; and situational judgement examined through the stakeholder dilemmas that fill your real calendar.

Two threads run through everything you have practised. The first is precision: counting contract years correctly, distinguishing "notification" from "approval", separating what a document states from what an interested party asserts. The second is judgement anchored in values: transparency over quiet workarounds, evidence over advocacy, direct conversation over engineered avoidance, and the interests of users, citizens, and the long-term strategy over the convenience of the moment. These are not test-taking tricks - they are the working habits of the role itself, which is why practising for the assessment and getting better at the job turn out to be the same activity.

As next steps, consider revisiting the questions you found hardest after a week's gap - spaced repetition consolidates technique far better than a single pass. Practise with authentic material: published government strategies, technology codes of practice, and your own (anonymised) options appraisals make excellent raw material for self-testing. If you can, exchange practice scenarios with peers in your architecture community; composing questions teaches you more than answering them, and it doubles as the community development your role calls for.

Finally, keep perspective. Psychometric assessments sample your abilities on one day, under one format; they do not define you, and a disappointing practice score is simply information about where to focus next. You operate every day at the intersection of strategy, technology, data, and people - demanding work that has already built the capabilities these assessments measure. Prepare well, rest before the real thing, read every question as carefully as you would read a supplier contract, and trust the professional judgement you have spent your career developing. Good luck - and enjoy the continued learning that preparation like this always brings.

