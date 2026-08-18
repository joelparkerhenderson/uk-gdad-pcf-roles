# Service Transition Manager - Psychometric Assessment Resources

## Introduction

Welcome. This guide has been written for you as a service transition manager working within the UK Government Digital and Data profession. Whether you are preparing for an internal assessment, applying for a new post, benchmarking your capability against your role profile, or simply interested in how psychometric assessments connect to the work you do, this document will help you practise deliberately and build genuine confidence.

Psychometric assessments are structured, standardised exercises that measure the cognitive abilities and behavioural tendencies that predict success in a role. For a service transition manager, that means far more than abstract puzzles. The assessments described here are job-specific: they draw on the artefacts you genuinely handle — service acceptance criteria, go-live recommendations, early-life support plans, change impact assessments, incident trend reports, configuration baselines, and readiness evidence from multiple teams — and the judgements you genuinely make, such as determining whether a product is fit for purpose, recommending go or no-go with defensible reasoning, and ensuring the wider IT operations community actually understands the acceptance criteria they will be held to.

Why do these assessments matter for your role in particular? You sit at the decision point of every transition. Analysts gather evidence; suppliers make claims; project teams push for dates; operations teams brace for what lands on them. You are the person who weighs all of it and makes a recommendation that others rely on. That is a role built on accurate reasoning under pressure: spotting the inconsistency in an evidence pack, reading a trend table correctly before it becomes an incident spike, extracting the exact commitment from a carefully worded supplier report, and choosing the most effective course of action when a go-live decision is contested. Cognitive, numeric, verbal, and situational judgement assessments map directly onto those four demands — which is precisely why employers use them for roles like yours.

This document is organised into four main assessment sections, each following the same pattern: an overview of what the assessment measures and why it matters for your role, a mapping of the assessment's dimensions to the specific skills in your role summary, a substantial set of practice questions with full worked explanations, practical preparation tips, and common pitfalls to avoid.

To get the most from it: first, read each "About this assessment" section so the formats hold no surprises. Second, attempt every practice question honestly — commit to an answer before reading the explanation. Third, treat each explanation as a mini-lesson; the reasoning walkthroughs are written to hand you reusable technique, not just the right letter. Fourth, connect what you practise back to your work: every question here is a stylised version of a judgement you have made or will make, and noticing that connection is what makes practice stick.

Assessments reward preparation far more than they reward raw talent, and preparation is entirely within your control. Work through this guide steadily, revisit what you get wrong, and you will walk into any assessment — and your next go/no-go review — sharper for it. Let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive assessment measures the mental processes your role demands, using realistic workplace material rather than abstract puzzles. For a service transition manager, that means questions built from acceptance evidence, dependency plans, configuration baselines, incident data, and the competing constraints of a live transition — and tasks that mirror your real reasoning: detecting inconsistencies, deducing consequences from rules, sequencing under dependencies, and prioritising when everything claims to be urgent.

The typical format is an online, timed test of 15 to 30 minutes with 15 to 30 multiple-choice questions covering pattern recognition, logical deduction, error checking, prioritisation, and applied problem solving. Scoring is objective against a norm group, and many platforms adapt difficulty to your performance — a test that feels progressively harder is usually going well. Most platforms provide short ungraded warm-up questions so you can learn the interface without cost.

Employers use cognitive assessment for transition roles because your professional output is judgement, and judgement is only as good as the reasoning underneath it. When you determine whether a product is fit for purpose, you are integrating evidence from testing, security, operations, and users, and checking it for gaps and contradictions. When you make a go-live recommendation, you are reasoning about risk, dependency, and consequence — and your recommendation will be interrogated by people who want a different answer. When you assess readiness against agreed service acceptance criteria, you are performing systematic rule-application at scale. A cognitive assessment samples those processes in miniature, under time pressure, with a right answer — which is exactly what makes it predictive.

A useful mindset: treat the test the way you treat a readiness review. Establish the rules first, check the evidence against them, conclude only what the evidence supports, and manage your time across the whole set rather than perfecting any single item.

### How this assessment maps to your role

The assessment dimensions map directly to the named skills in your role summary:

- **Error checking** maps to your core duty of assessing readiness against agreed service acceptance criteria: fitness-for-purpose decisions rest on finding the mismatch, the gap, or the stale evidence in a pack assembled by people who believe it is complete.
- **Logical deduction** maps to your **Change management** skill — analysing and assessing the impact of change — and to your **Service management framework knowledge**: reasoning correctly from lifecycle rules and dependency chains to their consequences is applied deduction.
- **Pattern recognition** maps to your **Problem management** skill: initiating and monitoring actions to investigate patterns and trends means seeing the structure in incident data before it becomes an outage, and knowing when to consult specialists.
- **Prioritisation** maps to your **Incident management** skill — diagnosing and prioritising incidents — and to the daily reality of co-ordinating a transition: ranking competing demands by impact and urgency, defensibly.
- **Applied problem solving** maps to your **Service focus** skill: seeing the bigger picture across groups of services and investigating how to get the best from underlying services requires decomposing messy, interconnected situations into tractable reasoning.
- **Verification discipline** maps to your **Asset and configuration management** skill: maintaining secure configuration and accurate information, and verifying the location and state of IT assets, is error checking institutionalised.

### Practice questions

**Question 1 (easy) — Pattern recognition in a configuration baseline**

Your configuration baseline requires every production server record to follow the naming pattern: environment code (P for production), two-letter service code, hyphen, then a three-digit number — for example, PCS-001 for the case service. Reviewing a baseline extract you see:

1. PCS-001
2. PCS-002
3. PDM-001
4. SCS-003
5. PDM-002

Which entry breaks the pattern for a production baseline?

- A) Entry 2
- B) Entry 3
- C) Entry 4
- D) Entry 5

**Correct answer: C**

**Explanation:** State the rule in words before scanning: first character P, then two letters, hyphen, three digits. Entries 1, 2, 3 and 5 all begin with P and follow the format. Entry 4 begins with S — either a staging server has been recorded in the production baseline, or the record is misnamed; both possibilities matter. The reliable technique is to verbalise the pattern and then test each candidate against it one element at a time, rather than trusting a visual skim. In configuration management terms this is not pedantry: a staging record inside a production baseline corrupts every report, audit, and impact assessment built on that baseline — and verifying the state and identity of assets is explicitly your skill territory.

**Question 2 (easy) — Deduction from acceptance criteria**

Your service acceptance criteria state: "A product may be recommended for go-live only if all critical defects are closed AND early-life support arrangements are agreed." The project reports: "All critical defects are closed." Which conclusion is correct?

- A) You may recommend go-live.
- B) You may not recommend go-live.
- C) You cannot yet conclude either way — the early-life support condition must still be checked.
- D) Early-life support arrangements are probably agreed, since defect closure took longer.

**Correct answer: C**

**Explanation:** The criterion is a conjunction: both conditions must hold. One is confirmed; the other is simply unaddressed. Concluding "may recommend" (A) treats one condition as two; concluding "may not" (B) assumes the unchecked condition fails, which is equally unsupported; option D substitutes plausibility for verification. The disciplined answer is C — and then, in real life, a precise question: "show me the agreed early-life support plan." This structure recurs constantly in acceptance work because criteria are nearly always compound. The professional habit the question rehearses: enumerate the conditions, tick them independently, and never let one strong tick radiate confidence onto its neighbours.

**Question 3 (easy) — Error checking a go-live readiness summary**

A readiness summary states: "All 6 acceptance criteria are met. Evidence: (1) functional testing complete — report attached; (2) performance testing complete — report attached; (3) security assessment complete — certificate attached; (4) operations runbook delivered — link attached; (5) service desk training complete — register attached; (6) early-life support plan agreed — draft attached." What is wrong?

- A) Six criteria is too many for one summary.
- B) Criterion 6's evidence is a draft, which contradicts "agreed" — so the claim "all 6 met" is not supported.
- C) Criterion 3 should be a report, not a certificate.
- D) Nothing is wrong.

**Correct answer: B**

**Explanation:** Check each evidence item against the status word it is meant to support. Items 1 to 5 pair a completion claim with an artefact of completion. Item 6 pairs "agreed" with a draft — and a draft is by definition not yet agreed, so the headline "all 6 criteria are met" overstates by exactly one criterion. Options A and C invent standards the question does not give. The technique — match the evidence's own status against the claimed status, item by item — is the core mechanic of acceptance review, and the most common finding in real packs is precisely this one: a plan, briefing, or agreement claimed as done while its artefact is still marked draft, scheduled, or in review.

**Question 4 (moderate) — Prioritisation across a transition portfolio**

You are co-ordinating three transitions and it is 9:00 Monday. Four items compete:

1. Transition A's go/no-go review is tomorrow morning; your recommendation paper is half-written.
2. Transition B's project manager wants a meeting today to discuss re-planning a slipped test phase; go-live is six weeks away.
3. A major incident review this afternoon needs your input on whether last week's failed change followed the agreed implementation sequence — you have the evidence but have not reviewed it.
4. Transition C's supplier has sent revised acceptance evidence, requested for review "this week".

Which sequencing is most defensible?

- A) 1, 3, 2, 4
- B) 3, 1, 4, 2
- C) 1, 2, 3, 4
- D) 3, 1, 2, 4

**Correct answer: D**

**Explanation:** Two items have hard same-day or next-morning deadlines: the incident review is this afternoon and the recommendation paper is due tomorrow morning. Between them, the incident review comes first — its deadline lands first, your input is blocking a review that others attend, and the evidence check is bounded work. The recommendation paper takes the rest of the day. Item 2 comes next: a six-week horizon is comfortable, but a slipped test phase compounds if replanning waits, so a short meeting this week beats deferring it behind item 4's routine review, which has a soft "this week" deadline. Option A defers B's meeting behind C's evidence with no reason; option C sequences by list order, letting tomorrow's paper displace this afternoon's commitment; option B gets the first two right and then inverts the last two. The principle: sequence by deadline hardness first, then by how much a delay compounds.

**Question 5 (moderate) — Impact deduction across service dependencies**

Your dependency model records: the document service depends on the storage platform; the case service depends on the document service and the identity service; the reporting service depends on the case service's database replica but not on its application layer. A change will take the storage platform offline for two hours. Assuming the model is complete and dependencies are hard, which services will be unavailable during the window?

- A) Document service only
- B) Document service and case service
- C) Document service, case service, and reporting service
- D) All services including identity

**Correct answer: B**

**Explanation:** Trace the chain from the changed component outward. Storage platform down → document service down (direct dependency). Document service down → case service down (it depends on the document service; its other dependency, identity, is irrelevant once one hard dependency fails). Case service down → reporting? Check the model's precision: reporting depends on the case service's database replica, not its application layer — and nothing says the replica depends on the storage platform or fails when the case application is down. So reporting stays up, and identity was never in the chain. Answer B. The question rewards reading the dependency model exactly as written rather than rounding it to "everything connected breaks". Impact assessment lives on that precision: over-scoping outage warnings costs credibility just as under-scoping costs users.

**Question 6 (moderate) — Spotting the trend that matters**

Reviewing incident data for a service in early-life support, you see weekly incident counts: 41, 38, 40, 37. Within those totals, incidents tagged "data quality": 4, 7, 11, 16. Which reading is correct?

- A) The service is stabilising — total incidents are trending down.
- B) Totals are roughly flat, but data-quality incidents are doubling roughly every fortnight and now drive over 40% of the total; the trend needs investigation before it dominates.
- C) The data is too noisy to conclude anything.
- D) Data-quality tagging has probably improved; the underlying position is unchanged.

**Correct answer: B**

**Explanation:** Look past the headline series to its composition. Totals drift within a narrow band (37–41): roughly flat. The tagged subset grows 4 → 7 → 11 → 16 — approaching a doubling pattern, and 16 of 37 is about 43% of the latest week. A flat total concealing an accelerating category means the rest of the incident mix is falling while one problem grows — the classic early-life-support signature of an emerging systemic defect. Option A reads only the totals; option C mistakes a clear sub-trend for noise; option D invents a measurement explanation with no supporting evidence (possible, but an investigation question, not a conclusion). This is your **Problem management** skill in data form: initiate and monitor actions to investigate patterns and trends — and the pattern worth initiating on is almost always inside the total, not on top of it.

**Question 7 (moderate) — Error checking early-life support arrangements**

An early-life support plan states: "Hypercare runs for four weeks from go-live (Monday 2 March). The supplier provides on-site support Monday to Friday during hypercare. Weekly service reviews occur every Friday, with the final review on Friday 27 March marking hypercare exit." What is the internal inconsistency?

- A) Four weeks from Monday 2 March ends Sunday 29 March, but the "final" review on Friday 27 March would occur before hypercare ends — leaving the last weekend inside hypercare but after the exit review.
- B) Suppliers never provide on-site support.
- C) Weekly reviews should be on Mondays.
- D) There is no inconsistency.

**Correct answer: A**

**Explanation:** Convert the words into dates and check them against each other. Four weeks from Monday 2 March spans 2–29 March, ending Sunday 29 March. The plan designates Friday 27 March's review as the exit marker — two days before the stated four weeks elapse, and with a weekend still inside the hypercare window but after the "final" review. Either hypercare is actually 3.8 weeks, or the exit review is mislabelled, or weekend cover for 28–29 March is unowned; the document must pick one. Options B and C impose outside opinions; the question asks for internal inconsistency — the document disagreeing with itself. Date arithmetic against stated durations is among the highest-yield checks in transition documents, because plans are edited by many hands and the dates drift apart from the durations quietly.

**Question 8 (moderate) — Sequencing a cutover under constraints**

A cutover requires five activities: final data sync (S), DNS switchover (D), smoke tests (T), service desk go-live comms (C), and supplier handover call (H). Constraints: (i) S must complete before D; (ii) T can only run after D; (iii) C must be sent before users can access the new service, i.e. before D completes; (iv) H must occur after T passes; (v) S takes 3 hours, D takes 1 hour, T takes 1 hour, C takes 30 minutes and can run in parallel with anything, H takes 30 minutes. If S starts at 18:00, what is the earliest H can finish?

- A) 22:30
- B) 23:00
- C) 23:30
- D) 22:00

**Correct answer: C**

**Explanation:** Build the critical path. S: 18:00–21:00. D: 21:00–22:00. T: 22:00–23:00. H: 23:00–23:30. C runs in parallel and needs only to be sent before D completes (22:00) — it can go at any point earlier, say during the sync, so it adds nothing to the path. Earliest H finish: 23:30. Option A forgets T; option D forgets both T and H's duration; option B forgets H takes 30 minutes. The method — identify which activities chain and which genuinely parallelise, then add only the chain — is exactly how you pressure-test a project's cutover plan, and the most common real-world planning error is the one options A and D model: treating a dependent activity as parallel because it is short.

**Question 9 (hard) — Multi-criteria fitness-for-purpose judgement**

A product presents this position at acceptance: functional tests 97% passed with no critical defects; performance meets targets except one report that runs 20% slow, used monthly by 3 internal analysts; security assessment clean; operations runbook complete; service desk trained; but the data migration reconciliation shows 1,200 of 480,000 records (0.25%) with mismatched address fields, correctable by a scripted fix in week one post-go-live. Your acceptance criteria require: no critical defects, performance targets met for citizen-facing functions, security clean, operations ready. Which recommendation is most defensible?

- A) No-go: performance and data are imperfect.
- B) Go, with conditions: the slow monthly report and the address-field fix are logged as accepted risks with owners and dates, since no acceptance criterion is breached — the slow report is not citizen-facing and the data mismatch is bounded, quantified, and has a remediation plan.
- C) Go, unconditionally: 97% is a high pass rate.
- D) Defer the decision until the product is perfect.

**Correct answer: B**

**Explanation:** Test the position against the criteria as written, not against an instinct for perfection. No critical defects: met. Performance for citizen-facing functions: met — the one slow report is internal and monthly, outside the criterion's scope. Security: met. Operations ready: met. No criterion is breached, so a no-go (A) would be imposing criteria retrospectively — a credibility-destroying move with project teams. But unconditional go (C) discards your leverage to ensure the two known imperfections are actually fixed: acceptance is the last moment you can attach conditions that anyone will honour. Option D confuses fitness for purpose with flawlessness; products transition with known, managed imperfections or they never transition at all. B is the professional answer: go, with the residual items converted into owned, dated, logged commitments. This is the judgement your role exists to make — and the structure (criteria check, scope check, residuals converted to conditions) is reusable for every acceptance you will ever run.

**Question 10 (hard) — Diagnosing a pattern across transitions**

Across your last four transitions you observe: transition 1 slipped two weeks (late security assessment); transition 2 went live on time but had a major incident in week one (unbriefed service desk); transition 3 slipped one week (late security assessment); transition 4 went live on time but early-life support was chaotic (runbook incomplete). Which single systemic hypothesis best explains the pattern, and what evidence would test it?

- A) Suppliers are underperforming; evidence: supplier contract reviews.
- B) Operations teams are resistant to change; evidence: staff surveys.
- C) Acceptance criteria are being engaged too late in the delivery lifecycle — security, service desk, and operations readiness all surface as last-minute surprises; evidence: check when in each project the criteria were first shared and when each readiness activity was scheduled versus when it was needed.
- D) The transitions were unlucky; evidence: none needed.

**Correct answer: C**

**Explanation:** Look for what the four failures share. Each is a different symptom — late security work, unbriefed desk, incomplete runbook — but every one is a readiness activity discovered late, either delaying go-live or degrading it. A single upstream cause explains all four: the criteria and their lead times are not reaching delivery teams early enough to be planned in. Option C also proposes a discriminating test: dates of criteria engagement versus dates of need — evidence that would confirm or kill the hypothesis. Options A and B each explain at most one symptom and carry an accusatory frame the data does not support; option D abandons analysis. Note the role connection: your duty is to ensure acceptance criteria are understood by the wider IT operations and delivery community — this question is the diagnostic case for why that duty exists. Pattern-and-trend investigation (your **Problem management** skill) applies to your own process, not just to live services.

**Question 11 (hard) — Reasoning under contradictory evidence**

Two evidence sources disagree. The supplier's performance report (dated 10 July, against release candidate RC3) shows all transactions under the 2-second threshold. Your analyst's spot-check (dated 18 July, against RC4 — the build actually proposed for go-live) shows the search transaction averaging 2.6 seconds. The supplier responds: "Our full test was rigorous; the spot-check environment was probably misconfigured." Which position is most defensible?

- A) Accept the supplier's full report — a rigorous full test outweighs a spot-check.
- B) Accept the spot-check — internal evidence always beats supplier evidence.
- C) Neither result validates RC4 yet: the rigorous test was against a superseded build, and the spot-check — while indicative and concerning — needs its environment verified; require a performance re-run against RC4 in a verified environment before acceptance.
- D) Split the difference and record search performance as 2.3 seconds.

**Correct answer: C**

**Explanation:** Evaluate each source on two axes: rigour and relevance. The supplier's test is rigorous but stale — RC3 is not the go-live build, and performance can regress between candidates; a rigorous answer to a superseded question validates nothing. The spot-check is relevant (RC4) but of unverified rigour — the supplier's environment challenge is self-serving but not impossible. So neither source, alone, evidences the criterion "RC4 meets performance targets", and the correct move is the one that repairs both axes at once: re-run against the right build in a verified environment. Options A and B each pick an axis and ignore the other; option D is the worst kind of resolution — averaging two measurements of different things produces a number that describes neither. Contradictory evidence is routine at acceptance; the reusable technique is to ask of every artefact "rigorous? relevant to this build, this environment, this criterion?" and to treat any "no" as a gap to close, not a debate to win.

**Question 12 (hard) — Co-ordination logic across teams**

Three teams must complete work before a shared go-live: the network team needs 10 working days and can start immediately; the security team needs 5 working days but cannot start until the network work is 60% complete; the training team needs 8 working days, cannot start until security has started, and must finish at least 2 working days before go-live to allow rota planning. What is the minimum number of working days from start to go-live?

- A) 15
- B) 16
- C) 17
- D) 23

**Correct answer: B**

**Explanation:** Work the dependencies numerically. Network: days 1–10; 60% complete after day 6. Security starts day 7, runs 5 days: days 7–11. Training starts when security starts — day 7 at the earliest — and runs 8 days: days 7–14. All work completes at the latest of: network day 10, security day 11, training day 14 → day 14. Training must finish at least 2 working days before go-live, so go-live is no earlier than day 14 + 2 = day 16. Check nothing else binds: network and security finish well before day 16. Answer: 16. Option A forgets the 2-day buffer; option C misplaces training's start at day 8 (it may start the same day security starts, day 7); option D adds all durations serially (10 + 5 + 8), ignoring the parallelism the constraints permit. This is the arithmetic core of your co-ordination duty: overlapping constraints are neither fully serial nor fully parallel, and the transition manager who computes the true critical path books go-live dates that survive contact with reality.

### Preparation tips

- **Practise on your own artefacts.** Take a recent readiness pack and run the checks from this section deliberately: status-word versus evidence-status, date arithmetic versus stated durations, dependency chains traced exactly as written. Twenty minutes of conscious practice per week compounds quickly.
- **Verbalise rules and criteria before applying them.** Compound criteria fail silently when read as single conditions. Say the ANDs out loud.
- **Draw the chain.** For dependency and sequencing questions, sketch the path with times on it. The critical path is a visual object; working memory alone drops links under time pressure.
- **Decompose composed data.** Whenever a total is offered, ask what its components are doing. Flat headlines hide accelerating categories — in tests and in early-life support alike.
- **Time-box per question.** In a 25-question, 25-minute test, a stubborn item gets flagged and revisited. Protect the whole set; that is portfolio management applied to a test.
- **Warm up with the ungraded questions.** Learn the interface, the flag button, and the timer position before the scoring starts.

### Common pitfalls to avoid

- **Letting one strong tick validate its neighbours.** Five criteria evidenced and one drafted is not "all six met". Check independently, always.
- **Rounding dependency models to "everything breaks".** Impact follows the model as written — over-scoping costs credibility exactly as under-scoping costs users.
- **Judging fitness for purpose against perfection.** The criteria are the standard. Imposing unwritten standards at the gate — in either direction — is the fastest way to lose the confidence of delivery teams.
- **Accepting rigorous evidence about the wrong thing.** A thorough test of a superseded build answers a superseded question. Rigour and relevance are separate checks.
- **Adding durations serially when constraints permit overlap.** And its twin: paralleling activities that actually chain. Compute the path; do not intuit it.
- **Reading only the headline series.** The trend that matters is usually inside the total. Decompose before you conclude "stable".

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment measures how accurately and confidently you interpret and manipulate the numbers your role runs on. It is not an examination in mathematics: the toolkit is percentages, ratios, averages, rates, percentage change, and the disciplined reading of tables and charts. What makes it job-specific is the data — for a service transition manager, that means test pass rates, defect closure velocities, availability and SLA figures, incident trends, capacity projections, and the migration reconciliation counts on which go-live recommendations rest.

The typical format is an online, timed test of 20 to 30 minutes with 15 to 25 multiple-choice questions, each built around a small data set. Calculators are almost always permitted, rough working is expected, and many platforms adapt difficulty to performance. Results are normed against people at a comparable level, and employers typically see accuracy and pace separately.

Employers test numeric reasoning for transition roles because your recommendations are, underneath the prose, numeric claims. "Testing is sufficiently complete" is a pass rate and a defect severity distribution. "The service is stable enough to exit early-life support" is an incident trend and a backlog trajectory. "Migration succeeded" is a reconciliation percentage with a bounded error. When you present a go-live recommendation, someone in the room will probe the numbers — and when a supplier presents theirs, the person probing should be you. The role demands not advanced mathematics but numerical scepticism: recomputing headline figures from raw counts, refusing averaged percentages across unequal groups, and projecting trends against thresholds before they arrive.

A practical reassurance: virtually every question reduces to three moves — part-of-whole, comparison, and division-by-count — plus care about which base you divide by. Master the moves, always ask "percentage of what?", sense-check each answer against the data's range, and the format holds no traps you cannot handle. The questions below build that fluency on your genuine working material.

### How this assessment maps to your role

- **Pass rates, severity distributions and reconciliation percentages** map to your core duty of assessing readiness against acceptance criteria: acceptance thresholds are numeric, and fitness-for-purpose judgements begin with verifying claimed figures from raw counts.
- **Availability, SLA and KPI arithmetic** maps to your **Availability and capacity management** skill: managing service components against business needs and KPIs means converting between downtime minutes and availability percentages, and projecting utilisation against triggers.
- **Trend analysis** maps to your **Problem management** and **Incident management** skills: diagnosing and prioritising incidents, and investigating patterns and trends, are quantitative acts — rates, compositions, and trajectories.
- **Impact quantification** maps to your **Change management** skill: assessing the impact of change means counting affected users, transactions, and services, and expressing risk as proportions a decision-maker can weigh.
- **Asset and estate figures** map to your **Asset and configuration management** skill: verifying the location and state of assets produces reconciliations, and reconciliations are arithmetic with consequences.
- **Evidence-grade numbers for decisions** map to your go-live recommendation duty and your **User focus** skill: quantified user impact ("18% of citizen transactions") is what turns a concern into a decision input.

### Practice questions

**Question 1 (easy) — Verifying a claimed pass rate**

A supplier's summary claims a "98% pass rate". The detailed report shows 540 tests executed, 522 passed. Is the claim accurate?

- A) Yes — the pass rate is 98%
- B) No — the pass rate is about 96.7%
- C) No — the pass rate is 95%
- D) Cannot be determined

**Correct answer: B**

**Explanation:** Recompute from raw counts: 522 ÷ 540 = 0.9667, or about 96.7% — not 98%. A quick route: 18 tests failed, and 18 ÷ 540 = 1 ÷ 30 ≈ 3.3% failed, so about 96.7% passed. The gap between 96.7% and 98% may or may not matter against your threshold, but the discrepancy itself always matters: a summary that inflates its own detail by 1.3 points invites the question "what else is rounded up?" Recomputing one headline figure from raw counts is the single fastest credibility check you can run on any evidence pack — thirty seconds, and it tells you how much scrutiny the rest deserves.

**Question 2 (easy) — Availability target arithmetic**

A service has a 99.7% monthly availability target. In a 30-day month (43,200 minutes), what is the maximum downtime permitted, in minutes?

- A) About 43 minutes
- B) About 86 minutes
- C) About 130 minutes
- D) About 300 minutes

**Correct answer: C**

**Explanation:** Permitted downtime = (100% − 99.7%) × total minutes = 0.3% × 43,200. Compute: 1% of 43,200 = 432; 0.3% = 432 × 0.3 = 129.6 — about 130 minutes. Option A corresponds to a 99.9% target, option B to 99.8%, option D to roughly 99.3%. Fluency in both directions of this conversion is core transition literacy: when a proposed maintenance window is 90 minutes and the availability target leaves 130 for the whole month, you can immediately see that one overrunning change could consume the month's entire error budget — which is exactly the kind of quantified observation that sharpens a go-live recommendation or an early-life support review.

**Question 3 (easy) — Average resolution time**

Five priority-2 incidents during early-life support took 3, 5, 4, 6 and 7 hours to resolve. What is the mean resolution time?

- A) 4 hours
- B) 5 hours
- C) 6 hours
- D) 25 hours

**Correct answer: B**

**Explanation:** Sum: 3 + 5 + 4 + 6 + 7 = 25. Divide by count: 25 ÷ 5 = 5 hours. Option D is the total; re-read what the question asks before answering. Sense-check: the mean must lie between the minimum (3) and maximum (7) — 5 does. One professional refinement worth carrying: with small samples, also glance at the spread (3 to 7 hours here). A mean of 5 with a widening spread tells a different operational story from a tight cluster at 5, and early-life support reviews are exactly where that difference starts mattering — a single 7-hour resolution may breach an SLA that the mean comfortably hides.

**Question 4 (easy) — Migration reconciliation percentage**

A data migration transferred 384,000 records; reconciliation matched 383,232 exactly. What percentage of records failed to reconcile?

- A) 0.02%
- B) 0.2%
- C) 2%
- D) 0.5%

**Correct answer: B**

**Explanation:** Unreconciled = 384,000 − 383,232 = 768 records. Percentage = 768 ÷ 384,000 = 0.002 = 0.2%. A tidy route: 1% of 384,000 is 3,840; 768 is a fifth of that, and a fifth of 1% is 0.2%. Watch the decimal discipline — options A, B and C differ only by factors of ten, and misplaced decimals are the dominant error in percentage questions under time pressure. In acceptance terms, 0.2% is 768 real records: the percentage sizes the problem, but the count sizes the remediation, and a good recommendation quotes both ("0.2% — 768 records — scripted fix owned by the data team, due week one").

**Question 5 (moderate) — Defect closure velocity against a deadline**

Eighteen must-fix defects remain, with go/no-go in 8 working days. Closure over the last 10 working days totalled 20 defects. Is the current velocity sufficient, and with what margin?

- A) Yes — projected closures of 16 exceed 18 with margin
- B) No — at 2 per day, projected closures are 16 against 18 needed, a shortfall of 2
- C) Yes — 20 closed exceeds 18 remaining
- D) No — the shortfall is 10 defects

**Correct answer: B**

**Explanation:** Velocity = 20 ÷ 10 = 2 defects per working day. Projection over 8 days: 2 × 8 = 16 closures against 18 needed — a shortfall of 2. Option C compares a past total to a future requirement, which is meaningless without the time dimension; option A miscounts 16 as exceeding 18; option D invents a number. The managerial reading matters as much as the arithmetic: a shortfall of 2 at constant velocity is a warning, not a verdict — the levers are scope (are all 18 genuinely must-fix?), capacity (can velocity rise?), and time (can the gate move?). Quantifying the gap precisely is what turns a vague "we're worried about the defect burn-down" into a decision-ready statement: "on current velocity we land 2 short; here are the three levers."

**Question 6 (moderate) — Combining test results across suppliers**

Two suppliers contribute to one release. Supplier A ran 250 tests with 92% passing; supplier B ran 750 tests with 96% passing. What is the overall pass rate?

- A) 94%
- B) 95%
- C) 95.5%
- D) 96%

**Correct answer: B**

**Explanation:** Rebuild counts before combining. Supplier A: 92% of 250 = 230 passed. Supplier B: 96% of 750 = 720 passed. Combined: (230 + 720) ÷ (250 + 750) = 950 ÷ 1,000 = 95%. The tempting error is the unweighted average (92 + 96) ÷ 2 = 94% (option A), which treats a 250-test contribution as equal to a 750-test one. Sense-check: the combined rate must sit between the two component rates, weighted toward the larger group — 95% sits three-quarters of the way from 92% to 96%, matching B's three-quarters share of the tests. Multi-supplier transitions produce exactly this arithmetic, and the difference between 94% and 95% can sit precisely on an acceptance threshold — recompute, never average.

**Question 7 (moderate) — Percentage change in incident volumes across go-live**

A service averaged 32 incidents per week before a major release. In the three weeks after go-live it logged 44, 41 and 47 incidents. What is the percentage increase of the post-release average over the pre-release average?

- A) 27.5%
- B) 37.5%
- C) 44%
- D) 12%

**Correct answer: B**

**Explanation:** Post-release average = (44 + 41 + 47) ÷ 3 = 132 ÷ 3 = 44 incidents per week. Increase = 44 − 32 = 12. Percentage increase = 12 ÷ 32 = 0.375 = 37.5%. Divide by the pre-release base (32), not the new value — 12 ÷ 44 ≈ 27.3% is the classic wrong turn (option A), and option D reports the raw difference as a percentage. A sustained 37.5% rise three weeks in is a strong early-life support signal that should shape your exit recommendation: quantified before-and-after comparison is precisely how "the service feels rockier since go-live" becomes an evidenced position that survives challenge at a service review.

**Question 8 (moderate) — Reading a stacked evidence table**

| Criterion | Items required | Items evidenced | Items outstanding |
|---|---|---|---|
| Testing | 12 | 11 | 1 |
| Security | 8 | 8 | 0 |
| Operations | 10 | 7 | 3 |
| Data | 6 | 5 | 1 |

Which statement is accurate?

- A) 86% of all required items are evidenced, with operations the weakest area at 70%.
- B) 92% of items are evidenced, with data the weakest area.
- C) 86% of items are evidenced, with testing the weakest area.
- D) The table contains an arithmetic inconsistency.

**Correct answer: A**

**Explanation:** Verify the rows first: 11+1=12 ✓, 8+0=8 ✓, 7+3=10 ✓, 5+1=6 ✓ — internally consistent, eliminating D. Totals: required = 12+8+10+6 = 36; evidenced = 11+8+7+5 = 31. Overall: 31 ÷ 36 ≈ 0.861 — 86%. Weakest area by proportion: testing 11/12 ≈ 92%, security 8/8 = 100%, operations 7/10 = 70%, data 5/6 ≈ 83% — operations, at 70%. Option A states both correctly. Note that "weakest" is a proportional judgement, not a raw count of outstanding items — though here operations leads on both. The two-step habit — verify the table's internal arithmetic, then compute the comparative figures — is exactly how readiness dashboards should be read before they are believed, particularly when the dashboard was assembled by the team it evaluates.

**Question 9 (moderate) — Capacity projection to a trigger**

A platform's peak concurrent users have grown: 1,800 (March), 1,980 (April), 2,178 (May) — 10% growth each month. The platform's tested capacity is 3,200 concurrent users, and your standard requires remedial action when peak load is projected to exceed 85% of tested capacity within three months. Is the trigger met at the end of May?

- A) No — 2,178 is only 68% of capacity.
- B) Yes — projecting 10% monthly growth gives about 2,899 in August, which exceeds the 2,720 trigger level.
- C) No — the projection for August is below the trigger level.
- D) Yes — any growth trend requires remedial action.

**Correct answer: B**

**Explanation:** Trigger level: 85% of 3,200 = 2,720 concurrent users. Project three months forward from May at 10% compound growth: June 2,178 × 1.1 = 2,395.8; July ≈ 2,635.4; August ≈ 2,898.9. August's ~2,899 exceeds 2,720, so a breach is projected within the three-month window — the trigger is met and remedial action is due now. Option A answers about the present when the standard asks about the projection; option C is the same computation done wrong (a common slip is applying 10% simple rather than compound growth: 2,178 + 3×218 = 2,832 — which still breaches, so C fails either way); option D replaces the standard with anxiety. Compound projection against thresholds is the arithmetic heart of your **Availability and capacity management** skill: the point of the standard is to buy remediation time before users feel the ceiling.

**Question 10 (hard) — Severity-weighted defect position**

Your acceptance framework scores open defects by severity: critical = 10 points, major = 4, minor = 1, and requires a total defect score of 25 or below for a go recommendation. The current log: 1 critical, 3 major, 8 minor. The project proposes closing the critical and one major before the gate. If they succeed, what is the score at the gate, and does it meet the threshold?

- A) 30 now, 16 at the gate — meets the threshold
- B) 30 now, 20 at the gate — does not meet
- C) 26 now, 12 at the gate — meets
- D) 34 now, 16 at the gate — meets

**Correct answer: A**

**Explanation:** Current score: (1 × 10) + (3 × 4) + (8 × 1) = 10 + 12 + 8 = 30. Proposed closures remove one critical (−10) and one major (−4): 30 − 14 = 16. Against a threshold of 25 or below: 16 meets it. Option A carries both computations correctly. The framework itself deserves a manager's appreciation: severity weighting encodes the judgement that one critical outweighs eight minors (10 > 8), so teams cannot game the gate by closing easy minors while the critical festers — and the arithmetic shows the only efficient route to the threshold runs through the severe defects. When you explain a gate decision to a project, walking through this weighted arithmetic is how the decision stops feeling arbitrary and starts feeling like the framework working as designed.

**Question 11 (hard) — Asset estate reconciliation across sources**

The configuration management database (CMDB) lists 1,250 production servers. A discovery scan finds 1,282 servers responding in production network ranges. Cross-matching shows 1,214 servers present in both sources. How many servers are in the CMDB but not found by the scan, how many were found but are absent from the CMDB, and which situation is the more urgent security concern?

- A) 36 unfound; 68 unregistered; the 68 unregistered are the more urgent security concern
- B) 68 unfound; 36 unregistered; the 68 unfound are more urgent
- C) 36 unfound; 68 unregistered; the 36 unfound are more urgent
- D) 32 unfound; 32 unregistered; both equal

**Correct answer: A**

**Explanation:** Work from the intersection. In CMDB but not scanned: 1,250 − 1,214 = 36 (recorded servers not responding — possibly decommissioned without record-keeping, or offline). Scanned but not in CMDB: 1,282 − 1,214 = 68 (live servers nobody's records own). Option D falls for differencing the two totals (1,282 − 1,250 = 32), which conflates two distinct populations — the intersection, not the difference of totals, is the reconciliation anchor. On urgency: the 68 unregistered servers are running in production with no recorded owner, no patch accountability, and no place in any impact assessment — unknown and live beats known and silent as a security exposure, which options B and C invert. This is your **Asset and configuration management** skill as arithmetic with consequences: maintain accurate information, verify the state of assets, and treat the unowned live estate as the finding that moves first.

**Question 12 (hard) — Early-life support exit: reading the full table**

| Week | Incidents | Resolved in SLA | P1 incidents | User satisfaction |
|---|---|---|---|---|
| 1 | 52 | 44 | 2 | 71% |
| 2 | 45 | 40 | 1 | 74% |
| 3 | 38 | 35 | 1 | 78% |
| 4 | 33 | 32 | 0 | 81% |

Exit criteria: weekly incidents below 35; SLA resolution rate at or above 92%; no P1 incidents in the final fortnight; satisfaction above 80%. Which criteria are met in week 4, and is exit supported?

- A) All four are met — exit supported.
- B) Three are met, but a P1 in week 3 breaches the final-fortnight condition — exit not yet supported.
- C) Two are met — incidents and satisfaction; SLA and P1 conditions fail.
- D) Exit is unsupported because week 1 performance was poor.

**Correct answer: B**

**Explanation:** Check each criterion against its own definition — including its time window. Incidents: 33 < 35 ✓. SLA rate: 32 ÷ 33 = 0.9697 ≈ 97% ≥ 92% ✓. Satisfaction: 81% > 80% ✓. P1 condition: "no P1 in the final fortnight" means weeks 3 and 4 together — week 3 logged one P1, so the condition fails despite week 4's zero. Three of four met; exit not yet supported (typically: one more clean week re-satisfies the fortnight window). Option A reads the P1 criterion against week 4 alone — the classic window error; option C mis-computes the SLA rate (perhaps 32 ÷ 35, using the wrong denominator); option D judges against history the criteria do not reference. The transferable lesson: criteria carry their own measurement windows and denominators, and exit recommendations survive scrutiny only when each criterion is checked on its own terms — trend-shaped optimism ("everything is improving!") is not the same as criteria met.

### Preparation tips

- **Recompute one live headline per week.** Take a claimed pass rate, availability figure, or reconciliation percentage from a real pack and derive it from raw counts. It is perfect test practice and periodically a genuine finding.
- **Drill both directions of availability arithmetic.** Percentage to minutes and minutes to percentage, for 99.5/99.7/99.8/99.9% against a 43,200-minute month. Transition conversations move faster when these are reflexes.
- **Write the method before touching the calculator.** "(new − old) ÷ old"; "rebuild counts, then combine"; "trigger level first, then gap, then gap ÷ rate". Naming the method defeats calculator autopilot.
- **Sense-check against structural limits.** Averages sit within the range; combined rates sit between components, nearer the larger; a percentage of anything cannot exceed 100. Two seconds per question, several marks per test.
- **Practise compound growth.** Two or three steps of ×1.1 done cleanly covers most projection questions — and most capacity conversations.
- **Mind the decimals on small percentages.** 0.2% versus 2% is a factor-of-ten error and a completely different go-live conversation. Say the magnitude in words ("about one in five hundred") as a check.

### Common pitfalls to avoid

- **Averaging percentages across unequal groups.** Rebuild the counts. The larger group drags the truth toward itself, and suppliers' summary slides rarely mention group sizes.
- **Dividing by the wrong base.** Percentage change uses the starting value; SLA rates use the incidents-in-scope denominator; reconciliation uses the register. Interrogate every denominator.
- **Ignoring measurement windows.** "No P1 in the final fortnight" is not "no P1 this week". Criteria carry their windows with them; check the window before the value.
- **Comparing a past total to a future requirement.** Twenty closed last fortnight says nothing about eighteen needed next week until you convert both to rates over time.
- **Simple-growth projections for compound phenomena.** User load and data volumes compound; adding a flat increment per month understates the curve exactly when it matters.
- **Reporting percentages without counts (or counts without percentages).** 0.2% sizes the risk; 768 records sizes the fix. Decision-grade numbers carry both.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment measures how precisely you read, interpret, and draw conclusions from written material — and for a service transition manager, written material is the medium of the job. Acceptance criteria, supplier contracts and reports, service level agreements, ITIL-aligned process documents, go-live recommendations, and the carefully drafted emails of people who want a particular decision: your role is conducted through documents whose exact wording carries operational and commercial weight.

The dominant format is true / false / cannot say: a short passage followed by statements you judge as definitely true (stated or necessarily following), definitely false (contradicted), or indeterminable (the passage is silent). Supporting formats include best-summary questions, logical-completion questions, and clear-writing judgements. A typical test runs 15 to 25 minutes with 20 to 30 questions across several passages, scored against a norm group.

The discipline the format demands — answer from the passage alone — is the same discipline your role demands. You know how transitions usually go; the question is what this contract actually commits the supplier to, what this SLA actually measures, what this acceptance report actually evidences. Professional experience whispers plausible inferences, and the format trains you to hold the line between what a document says and what you expect it to say. That line is where acceptance disputes, SLA arguments, and supplier negotiations are won and lost.

Employers test verbal reasoning for transition roles for a further reason: you are also a producer of consequential text. Your go-live recommendations are read by senior decision-makers who were not in the detail; your acceptance criteria must be understood identically by every team held to them — your role summary makes that understanding your explicit duty. Reading precisely and writing unambiguously are one competence viewed from two sides, and this assessment samples both.

### How this assessment maps to your role

- **Precise comprehension** maps to your core duty of assessing readiness against agreed criteria: "agreed", "delivered", "tested", and "operational" are different claims, and acceptance decisions turn on which one a document actually makes.
- **True / false / cannot say discipline** maps to your go-live recommendation duty: a recommendation distinguishes what is evidenced, what is contradicted by evidence, and what remains unknown — the format's three verdicts, applied at the decision that matters most.
- **Inference control** maps to your **Change management** and **Incident management** skills: impact assessments and incident diagnoses must follow from documented facts, with hypotheses labelled as hypotheses.
- **Reading process and framework documents** maps to your **Service management framework knowledge**: ITIL lifecycle texts, continuity procedures, and SLA schedules are dense conditional documents, and applying them starts with parsing them exactly.
- **Clear-writing judgement** maps to your duty to ensure acceptance criteria are understood by the wider IT operations community: criteria that admit two readings will be met in the cheaper of the two, and the drafting skill this assessment samples is your main defence.
- **Reading user evidence faithfully** maps to your **User focus** skill: user research summaries support decisions only when read without over-extension — a discipline identical to "cannot say".

### Practice questions

For questions 1 to 5, read this extract from a service acceptance policy:

> "A go-live recommendation must be produced by the service transition manager for every major release. The recommendation must state whether each acceptance criterion is met, partially met, or not met, and must list all conditions attached to a 'go' recommendation. Where any criterion is not met, a 'go' recommendation may still be made if the residual risk has been formally accepted by the service owner. The final go/no-go decision rests with the service owner, not the service transition manager. Recommendations must be circulated at least two working days before the go/no-go review, except for emergency releases, which follow the expedited process defined in the emergency change procedure."

**Question 1 (easy) — True / false / cannot say**

Statement: "The service transition manager makes the final go/no-go decision."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** The passage is explicit: "The final go/no-go decision rests with the service owner, not the service transition manager." The statement is directly contradicted — false. This distinction is worth internalising well beyond the test: you produce the recommendation; the service owner owns the decision. Documents that confuse recommenders with deciders create exactly the accountability fog that post-incident reviews spend weeks untangling, and test writers love the recommender/decider swap because real organisations get it wrong so often. Where a statement swaps the actors around a decision, check the passage's exact allocation of the verb.

**Question 2 (easy) — True / false / cannot say**

Statement: "A 'go' recommendation is impossible if any acceptance criterion is not met."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** The passage provides an explicit route: where a criterion is not met, go "may still be made if the residual risk has been formally accepted by the service owner". The statement's "impossible" denies that route, contradicting the passage — false. Note the passage's own precision: the route requires formal acceptance, by a named role, of the specific residual risk. That is a controlled exception, not a loophole — and knowing the difference is daily currency in your role. Absolute words in test statements ("impossible", "always", "never") should send you hunting for the passage's exception clauses; policies at this level almost always have them, and they are almost always conditional.

**Question 3 (moderate) — True / false / cannot say**

Statement: "For an emergency release, the recommendation need not be circulated two working days in advance."

- A) True
- B) False
- C) Cannot say

**Correct answer: A**

**Explanation:** The two-day circulation rule carries an explicit carve-out: "except for emergency releases, which follow the expedited process". It follows necessarily that the two-day requirement does not bind emergency releases — true. What you cannot conclude is what the expedited process does require (same-day circulation? verbal briefing?): the passage delegates that to another document. The statement wisely claims only the exemption, not the replacement — had it said "emergency releases require no recommendation at all", the answer would be cannot say, since the expedited process's content is undisclosed. Reading exception clauses for exactly what they except — no more — is a skill contracts and SLAs reward richly.

**Question 4 (moderate) — True / false / cannot say**

Statement: "Recommendations must classify each criterion using a three-state scale."

- A) True
- B) False
- C) Cannot say

**Correct answer: A**

**Explanation:** The passage requires each criterion to be stated as "met, partially met, or not met" — three states, exhaustively listed. The statement paraphrases this accurately, so it is true. This question trains paraphrase-matching: verbal tests frequently restate passage content in different words, and your task is to check semantic equivalence rather than verbatim match. "Three-state scale" = three named states; "classify each criterion" = "state whether each criterion is". Where paraphrase questions go wrong is scope creep — had the statement said "a three-state scale defined by ITIL", the added attribution would push it to cannot say. Match meaning, then check nothing extra has been smuggled in.

**Question 5 (moderate) — Best summary**

Which sentence best summarises the passage?

- A) Service owners produce go-live recommendations for major releases.
- B) The transition manager recommends with stated criterion statuses and conditions, unmet criteria require formally accepted residual risk for a 'go', the service owner decides, and standard releases need two days' notice with emergencies expedited.
- C) Go-live decisions require all criteria to be met at least two days before review.
- D) Emergency releases are exempt from go-live recommendations.

**Correct answer: B**

**Explanation:** Sketch the passage's skeleton: who recommends (transition manager), what the recommendation contains (three-state statuses, conditions), the unmet-criterion route (formal risk acceptance), who decides (service owner), timing (two days, emergency exception). Option B compresses all five elements without distortion. Option A swaps producer and decider. Option C invents a requirement (all criteria met) the passage explicitly declines to impose, and garbles the timing rule. Option D over-extends the exception: emergencies are exempt from the two-day circulation, not from recommendation — the passage says they follow an expedited process, not no process. Summaries fail by omission, distortion, or over-extension; checking a candidate summary against the skeleton catches all three. The same check applies to the executive summary of your own recommendation papers.

For questions 6 to 9, read this extract from a supplier's transition status report:

> "Data migration rehearsal two completed on 4 September. Of the 1.9 million records migrated in rehearsal, 99.4% reconciled automatically; the residual records have been categorised, and remediation scripts for the two largest categories have been written and are in test. We anticipate full remediation coverage before cutover. Training delivery is complete for the north and midlands regions; the southern region's sessions are scheduled for the week commencing 15 September. The service desk knowledge base has been drafted and reviewed by our technical authors. We remain confident in the cutover date of 29 September, subject to the outstanding dependency on the department completing network changes at the southern sites, which remains outside our control."

**Question 6 (easy) — True / false / cannot say**

Statement: "The second migration rehearsal reconciled 99.4% of records automatically."

- A) True
- B) False
- C) Cannot say

**Correct answer: A**

**Explanation:** Stated directly: rehearsal two, 1.9 million records, "99.4% reconciled automatically". Locate, match, bank the mark. Then — as a professional reflex rather than a test requirement — notice what the sentence's precision quietly establishes: 0.6% of 1.9 million is 11,400 records requiring remediation, a count the report chooses not to state. Suppliers' reports often carry their most important numbers implicitly, as percentages of figures stated elsewhere; the reader who multiplies them out is the reader who arrives at the review knowing the size of the remediation task before the meeting starts.

**Question 7 (moderate) — True / false / cannot say**

Statement: "Remediation scripts exist for all categories of unreconciled records."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** The report says scripts "for the two largest categories have been written and are in test" — and that the supplier "anticipates" full coverage before cutover. Scripts for the two largest categories, with the rest anticipated, entails that scripts do not yet exist for all categories: the statement is contradicted — false. Watch the verbs stage by stage: written ≠ tested ≠ deployed; and "anticipate" is a forecast, not a status. This report is professionally drafted precisely to blur those stages into an impression of near-completeness. Your acceptance criteria will ask for verified remediation of all categories; mapping each category to its evidence stage — the reading this question rehearses — is exactly how you will interrogate the real thing.

**Question 8 (moderate) — True / false / cannot say**

Statement: "The service desk knowledge base has been approved by the department's service desk team."

- A) True
- B) False
- C) Cannot say

**Correct answer: C**

**Explanation:** The report says the knowledge base was "drafted and reviewed by our technical authors" — the supplier's own staff. It says nothing about the department's service desk team: no approval, no rejection, no involvement. The statement is neither confirmed nor contradicted — cannot say. The trap is treating "reviewed" as satisfying "approved by [someone else]": the passage's review was performed by a different party than the statement names, and review by the producing organisation is a different assurance event from approval by the consuming one. In acceptance terms this distinction is the whole game: supplier self-review is necessary and radically insufficient, and criteria should name the approving party for exactly this reason. When a statement upgrades both the verb and the actor, check each separately.

**Question 9 (hard) — Reading the risk structure**

Judged strictly on the report's content, which is the most accurate characterisation of the cutover confidence expressed?

- A) Unconditional — the supplier confirms 29 September.
- B) Conditional on a dependency the supplier controls.
- C) Conditional on a dependency the supplier explicitly places outside its control — departmental network changes at the southern sites — meaning the risk sits with the department's own delivery.
- D) The supplier expresses no confidence in the date.

**Correct answer: C**

**Explanation:** The confidence sentence carries its own caveat: "subject to the outstanding dependency on the department completing network changes... which remains outside our control." That is a conditional confidence, with the condition assigned — pointedly — to the customer. Option A reads the confidence and skips the "subject to"; option D reads the caveat and skips the confidence; option B misassigns the dependency's ownership. The professional layer: this sentence is doing contractual work. If cutover slips because of the network changes, the supplier has this report on record locating the cause on the department's side. A transition manager reads such sentences twice — once for status, once for risk allocation — and responds in kind: confirm the network change plan's dates in writing, or the slippage narrative is already written for you. Also connect the caveat to the earlier detail: the southern region is simultaneously the site of unfinished training and the unfinished network work — the report's two risks cluster geographically, which the report never points out.

For questions 10 to 12, read this extract from a service management framework text:

> "The purpose of the change enablement practice is to maximise the number of successful service and product changes by ensuring that risks have been properly assessed, authorising changes to proceed, and managing the change schedule. Change authority should be assigned to the person or group best positioned to assess the risk of a particular change type: low-risk standard changes may be pre-authorised, while significant changes may require authorisation at board level. Centralising all change authority in a single body regardless of change type tends to increase delay without improving risk assessment, because the central body lacks context for many changes it reviews."

**Question 10 (moderate) — True / false / cannot say**

Statement: "According to the passage, the purpose of change enablement is to minimise the number of changes made to services."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** The passage states the purpose is to "maximise the number of successful service and product changes" — an enabling framing, not a restricting one. The statement inverts it: minimising changes is close to the opposite of maximising successful ones. False. The inversion is worth dwelling on because it is a live cultural fault line in service management: change practices exist to make change safe and frequent, not rare — a misreading that turns transition teams into departments of "no". As the person accountable for ensuring criteria and processes are understood by wider IT operations, you will correct this exact misreading in real conversations; the test question is that correction in miniature.

**Question 11 (moderate) — Logical completion**

According to the passage, centralising all change authority in a single body tends to:

- A) Improve risk assessment at the cost of some delay
- B) Increase delay without improving risk assessment, because the central body lacks context for many changes
- C) Reduce delay by standardising decisions
- D) Work well for low-risk changes only

**Correct answer: B**

**Explanation:** The final sentence states it verbatim: centralisation "tends to increase delay without improving risk assessment, because the central body lacks context". Option B reproduces claim and reason together. Option A concedes the delay but invents an assessment benefit the passage explicitly denies — the most tempting distractor, because it matches a common real-world intuition ("surely central review is more rigorous"). Options C and D contradict the passage outright. The question form — complete the claim with its stated reason — rewards reading arguments as claim-plus-mechanism rather than as isolated assertions. The mechanism ("lacks context") is also the practically useful part: it tells you the remedy is assigning authority to where context lives, which is precisely the passage's design principle and a principle worth applying when you design acceptance gates.

**Question 12 (hard) — Clear-writing judgement**

You are drafting an acceptance criterion for service desk readiness, to be met identically by every future project. Which drafting is most effective?

- A) "The service desk should be appropriately prepared for the new service in good time before go-live."
- B) "Service desk readiness activities will be progressed in accordance with relevant best practice."
- C) "At least five working days before go-live: all service desk staff rostered for go-live week have completed the training module; the knowledge base articles for the service are published and approved by the service desk manager; and a named service desk escalation contact for early-life support is recorded in the support plan."
- D) "The service desk must be fully ready, with comprehensive training and complete documentation, to the satisfaction of all stakeholders."

**Correct answer: C**

**Explanation:** A criterion is effective when two independent readers must reach the same met/not-met verdict. Option C achieves that through three properties: a deadline ("at least five working days before go-live"), verifiable events ("completed the training module", "published"), and named approvers and artefacts ("approved by the service desk manager", "recorded in the support plan"). Option A is unverifiable twice over — "appropriately" and "in good time" are opinions wearing adverbs. Option B commits to activity, not outcome: "progressed in accordance with best practice" can be claimed by any project that held a meeting. Option D sounds strict and is actually the weakest: "fully", "comprehensive", and "to the satisfaction of all stakeholders" create an undefined, unbounded test that either blocks everything or — in practice — collapses into negotiation at the gate. Your role summary makes criteria understood by wider IT operations your duty; understanding follows from verifiability, and C is the only draft a future project can build a plan against. Vague criteria are not gentler — they are disputes scheduled for the worst possible week.

### Preparation tips

- **Read one consequential document per week at test discipline.** A supplier report or SLA schedule: list what it states, what it rules out, and what it leaves unsaid. The third list is where your review questions come from — and it is the "cannot say" muscle.
- **Track verbs and actors separately.** Drafted/reviewed/approved is a verb ladder; supplier/department/service owner is an actor list. Claims upgrade themselves along both axes — check each.
- **Hunt exception clauses.** When a statement uses "always", "never", or "impossible", the passage's "except", "unless", or "may still" usually decides the answer.
- **Multiply out implicit numbers.** 0.6% of 1.9 million is 11,400 — reports state the flattering form; compute the operational one.
- **Sketch the skeleton before judging summaries.** Five elements in the passage means the best summary carries five; count what each option drops or distorts.
- **Draft criteria with the two-reader test.** For every criterion you write, ask whether two strangers must reach the same verdict. It improves your documents and your eye for everyone else's.

### Common pitfalls to avoid

- **Importing operational experience into the passage.** You know what usually happens after a rehearsal; the question is what this report says happened. Silence is "cannot say", however experienced your hunch.
- **Letting confidence language stand in for status.** "We remain confident" plus a caveat is a conditional claim with allocated risk — read the condition, not the mood.
- **Merging the verb ladder.** Written is not tested; reviewed is not approved; anticipated is not done. Each rung is a different evidence state, in tests and at gates.
- **Missing who performed the verb.** Supplier self-review versus customer approval is an actor distinction that changes the assurance value entirely.
- **Over-extending exceptions.** Exempt from two-day circulation is not exempt from recommendation. Exceptions except exactly what they name.
- **Preferring impressive vagueness in writing questions.** "Fully ready to the satisfaction of all stakeholders" is not rigour — it is a dispute deferred. The verifiable draft wins, every time.

## Workplace job-specific situational judgement assessment

### About this assessment

A situational judgement test (SJT) presents realistic workplace dilemmas and asks you to identify the most effective — and sometimes least effective — responses. It measures professional judgement: not what you know, but how you weigh competing pressures, when you escalate, how you handle people, and whether the interests of users and the integrity of the process survive contact with deadline pressure and organisational politics.

Typical formats: choose the most effective of four responses; identify most and least effective; rank all options; or rate each response independently. Timing is generous — usually 20 to 30 minutes for 15 to 20 scenarios — because judgement, not speed, is the construct. Scoring compares your responses against a key developed with experienced practitioners and occupational psychologists, usually anchored to a behaviour framework: for GDAD roles, expect user focus, collaboration, ownership, honest communication, appropriate escalation, and inclusion.

For a service transition manager, the SJT is arguably the most job-relevant assessment of the four. Your decisions are rarely private calculations; they are positions taken among stakeholders with conflicting interests — project managers with dates to hit, suppliers with contracts to defend, operations teams with services to protect, service owners with outcomes to deliver, and users with no seat at the table. The scenarios below reflect that reality at your level: you have real authority over recommendations and co-ordination, you operate independently, and your judgement calls shape both individual transitions and the credibility of the transition process itself.

A note on what scoring keys reward at this level: not deference, and not heroics. The consistently high-scoring pattern is evidence-based positions held with civility, early and specific escalation, decisions routed to their proper owners with full information, team issues addressed rather than absorbed, and user impact kept visible in every trade-off. The explanations below name these behaviours explicitly, so that you finish this section with a working model of effective transition judgement — useful in the test, and more useful on the Monday after it.

### How this assessment maps to your role

- **Decision-integrity scenarios** map to your core duty of making go-live, early-life support, and service acceptance recommendations: the test probes whether your recommendations stay evidence-based under pressure from dates, hierarchy, and sunk cost.
- **Escalation and ownership scenarios** map to your **Ownership and topic** skill — owning an issue until it is resolved, mitigated, or properly transferred — applied at a level where you are often the escalation point as well as the escalator.
- **Team scenarios** map to your **Community collaboration** skill: motivating and empowering teams, creating the right environment, identifying the best team makeup, and recognising and dealing with issues — including conflict between the teams you co-ordinate.
- **Incident and problem scenarios** map to your **Incident management** and **Problem management** skills: diagnosing and prioritising under pressure, consulting specialists effectively, and converting recurring symptoms into systemic fixes.
- **Communication scenarios** map to your duty to ensure acceptance criteria are understood by wider IT operations: several scenarios test how you handle misunderstanding, disagreement, and the difference between informing people and being understood.
- **User-impact scenarios** map to your **User focus** skill: identifying and engaging users, and using quantitative and qualitative evidence to keep user outcomes decisive when they conflict with organisational convenience.

### Practice questions

**Question 1 (easy) — The sponsor wants a different recommendation**

Your draft recommendation for tomorrow's go/no-go is "no-go": the operations runbook is untested and the service desk untrained — two acceptance criteria unmet with no formal risk acceptance. The programme sponsor calls: "The director has announced this date publicly. I need your recommendation to be go." What is the most effective response?

- A) Change the recommendation to go — the sponsor outranks you and owns the political risk.
- B) Keep the recommendation as the evidence dictates, explain to the sponsor exactly what would change it (risk acceptance by the service owner, or the two criteria met), and offer to work with the teams today to close what can be closed before the review.
- C) Withdraw the recommendation entirely and let the review decide without one.
- D) Change the recommendation to go but note your private disagreement in an email to yourself.

**Correct answer: B**

**Explanation:** Your recommendation is an evidence product; the sponsor's call is pressure, not evidence. Option B holds the professional line while doing everything legitimately possible to help: the sponsor learns precisely what routes exist to a defensible go — including the formal risk-acceptance route your acceptance policy provides — and you offer real effort toward closing the gaps. That is firmness plus service, and it keeps the decision where it belongs, with the service owner deciding on accurate information. Option A converts your role into decoration; when the untrained desk fails in week one, "the sponsor asked" will protect no one — least of all users. Option C abandons your duty precisely when it is hardest, which is when it matters. Option D is A with a guilty conscience: the record that reaches the decision is still false to your analysis. The rewarded behaviours: evidence-based integrity, constructive assistance, proper decision routing.

**Question 2 (easy) — Two of your transitions collide**

You co-ordinate two transitions that have just landed on the same weekend: transition A's cutover was planned for months; transition B's has slipped onto the same dates, and both need the same database administration team, which cannot support both. Both project managers insist theirs cannot move. What is the most effective first action?

- A) Let the two project managers negotiate it between themselves.
- B) Establish the facts — what each cutover needs from the shared team, hour by hour, and what each slip would cost — then convene both PMs with the resource owner, propose the sequencing the facts best support, and escalate jointly with a recommendation if agreement fails.
- C) Award the weekend to transition A because it planned first.
- D) Ask the database team to work continuously across both cutovers.

**Correct answer: B**

**Explanation:** This is the co-ordination core of your role, and the effective pattern is facts, then forum, then — if needed — escalation with a recommendation. Option B builds the factual base first (perhaps the conflict is narrower than it appears: the hour-by-hour view often reveals partial compatibility), brings the parties and the resource owner into one conversation, and prepares the honest fallback: a joint escalation carrying your recommendation, not a shrug. Option A outsources co-ordination — your actual job — to the two parties least able to resolve it, since each holds only half the picture and all of the incentive. Option C uses an arbitrary tiebreaker before establishing whether the conflict is even real; "planned first" may be the right answer, but as a conclusion from impact analysis, not a substitute for it. Option D resolves the calendar by spending the people — a fatigued DBA team across two consecutive cutovers converts a scheduling conflict into an operational risk for both services. Rewarded behaviours: fact-finding before positioning, collaborative resolution, escalation with analysis attached.

**Question 3 (easy) — The criteria nobody read**

At a readiness review, it becomes clear the project team has never seen the service acceptance criteria: they planned against their own definition of done, and two criteria — operations documentation and support-model sign-off — have no corresponding work. The project manager is embarrassed and asks for the criteria to be "flexed this once". What is the most effective response?

- A) Flex the criteria — the gap is partly your process's fault for not reaching them.
- B) Hold the criteria, work with the PM to size the genuinely missing work and replan honestly, and separately fix the systemic gap — build criteria briefing into project initiation so no future team meets them at the review.
- C) Hold the criteria and let the project fail the review as a lesson to others.
- D) Report the project manager's planning failure to the programme board.

**Correct answer: B**

**Explanation:** Two problems arrive together — this project's gap, and the process gap that produced it — and option B is the only response that solves both without sacrificing either. The criteria exist to protect live service; flexing them because they were not read (option A) would make ignorance of the criteria the cheapest route through them, an incentive no transition process survives. But your role summary makes criteria understanding across wider IT operations your explicit duty, so the systemic half of B is not generosity — it is your job, and this review just handed you the evidence for prioritising it. Option C protects the criteria and wastes the lesson: reviews are gates, not punishments, and "pour encourager les autres" thinking damages the collaborative relationships that get future criteria read. Option D escalates blame before attempting resolution — and the blame is partly structural anyway. Rewarded behaviours: standards held, help given, root cause owned, no scapegoating.

**Question 4 (moderate) — Least effective: the supplier's engineer tells you something off the record**

At a working session, the supplier's lead engineer quietly tells you: "Between us — the performance fixes are cosmetic. The architecture can't hit the targets at your user volumes. My management won't put that in writing." The formal supplier position remains that performance targets will be met. Which response is LEAST effective?

- A) Commission an independent load test at production volumes before acceptance, so the question is settled by evidence rather than by either account.
- B) Raise the discrepancy with the supplier's management, without naming the engineer, and require evidence-based reassurance.
- C) Dismiss the conversation — it was informal, and the formal position is what counts.
- D) Note the risk in your own log and increase scrutiny of the performance evidence at the gate.

**Correct answer: C**

**Explanation:** Hunt for the option that most endangers the service. Option C is it: it privileges the format of information over its content. An engineer with direct knowledge has told you the formal position may be false; "it wasn't in writing" changes the evidential weight, not the risk. Dismissing it entirely means walking into acceptance with a known, specific, credible doubt unexamined. Option A is the strongest response — it resolves the contradiction with independent evidence and protects the engineer completely, since load testing at production volumes is a defensible ask on any major transition. Option B is legitimate escalation handled with appropriate source protection, though it risks a rehearsed reassurance. Option D is weaker but still rational: the risk enters your record and sharpens the gate. The professional principles: informal intelligence is a trigger for verification, never for either blind belief or blind dismissal — and protecting people who tell you uncomfortable truths is how you keep being told them.

**Question 5 (moderate) — The analyst who missed something big**

A week before go-live, you discover that your service readiness analyst — capable, hardworking, recently promoted — signed off the backup-and-restore criterion without evidence: no restore test was ever run. When you ask, they admit they assumed the supplier's backup configuration screenshots were sufficient and did not want to bother you with questions during a busy month. What is the most effective response?

- A) Take the criterion back, run the restore test properly, and say nothing further — everyone makes mistakes.
- B) Correct the record immediately, get the restore test scheduled this week, and hold a candid, blame-aware conversation with the analyst: what "evidence" means for each criterion type, and why questions are never an imposition — then check whether other criteria they signed share the same weakness.
- C) Remove sign-off authority from the analyst and re-verify everything they have ever touched.
- D) Report the failure to HR as a conduct issue.

**Correct answer: B**

**Explanation:** Three obligations arrive at once — the service (a live criterion is unevidenced days before go-live), the record (a sign-off is false), and the person (a promising analyst has revealed a correctable gap in judgement and a worrying reluctance to ask). Option B discharges all three in the right order: record corrected, test scheduled, teaching conversation held, and — the step that separates managers from firefighters — a bounded check of whether the same misunderstanding infects their other sign-offs. The conversation matters as much as the correction: "didn't want to bother you" is a culture signal, and your **Community collaboration** skill (create the right environment; motivate and empower) means fixing the environment that made silence feel safer than questions. Option A fixes today's criterion and guarantees a repeat, while leaving the analyst's other sign-offs unexamined. Option C punishes proportionately to your fear rather than to the evidence — it converts a development moment into a demotion and teaches your team to hide mistakes. Option D outsources a management conversation to a disciplinary process, destroying trust for no service benefit. Rewarded pattern: fix the record, fix the risk, grow the person, check the blast radius.

**Question 6 (moderate) — Early-life support is being starved**

Your early-life support plan for a just-launched service commits the project's developers to two weeks of dedicated incident support. Three days in, the delivery director quietly reassigns half of them to the next project, saying: "The service is green — you're overstaffed." Incident volumes are indeed low, but the service has not yet faced its first weekly batch run or month-end peak. What is the most effective response?

- A) Accept the reassignment — the current data supports it.
- B) Push back with the plan's rationale: the support commitment was sized for the known risk events still ahead (first batch run, month-end), not for the quiet days between them; propose a compromise if genuine — staged release of developers tied to passing those events — and escalate to the service owner if the commitment is simply overridden.
- C) Escalate immediately to the service owner without speaking to the delivery director first.
- D) Say nothing but keep a record showing you objected, in case the batch run fails.

**Correct answer: B**

**Explanation:** The reassignment reasons from three quiet days; the plan reasoned from the service's risk calendar — and the whole point of early-life support sizing is that risk arrives on schedule (batch runs, month-end) rather than uniformly. Option B re-makes that argument to the person who acted, which is both correct sequencing and respectful of their legitimate interest (the next project is real too); it offers an evidence-based compromise — staged release tied to surviving the actual risk events — and it is honest about the escalation path if the plan's commitments are simply void. This is your recommendation duty extended into early-life support: commitments you accepted evidence against are commitments you defend. Option A mistakes the absence of load for the absence of risk. Option C skips the direct conversation that resolves most of these situations and spends escalation capital unnecessarily. Option D is the worst kind of prudence — a private record that protects you at the precise cost of not protecting the service; if the batch run fails half-staffed, your unsent objection helped nobody. Rewarded behaviours: defend evidence-based plans, negotiate with the risk calendar, escalate transparently when commitments are overridden.

**Question 7 (moderate) — The incident during cutover**

Mid-cutover, 23:30. The data migration is 70% complete when the monitoring dashboard shows a priority-1 incident on an unrelated live service — one your operations counterparts also support, and their team is stretched. Your cutover team includes two engineers with exactly the skills the P1 needs. The cutover window closes at 06:00; losing the engineers for two hours makes the window tight but probably achievable. What is the most effective response?

- A) Refuse to release the engineers — the cutover window is committed.
- B) Release both engineers immediately without conditions — P1s outrank everything.
- C) Contact the incident manager, establish whether your two engineers are genuinely the best available option, and if so release them with a defined recall condition; simultaneously re-plan the remaining cutover activities to protect the critical path and identify your no-go-back point.
- D) Pause the entire cutover until the P1 is resolved.

**Correct answer: C**

**Explanation:** Two live commitments genuinely conflict, and the effective response is neither absolutism (A and B each pick one commitment and abandon judgement) nor paralysis (D creates a second failure to keep the first one company). Option C does what a transition manager at your level is for: it verifies the need is real before paying for it (perhaps the incident team has alternatives — establish, don't assume), bounds the concession (defined recall condition, so the cutover's fate stays managed), and immediately converts the new constraint into a re-planned critical path with an explicit no-go-back point — the moment after which you either complete or roll back cleanly. That last element is the professional core: cutover safety is not "will we finish?" but "will we always be in a state we can safely exit from?" This is your **Incident management** skill (prioritise across services, not just within one) operating alongside your co-ordination duty, and your **Service focus** skill's bigger picture: both services belong to the same public. Rewarded behaviours: verify before conceding, bound what you concede, re-plan explicitly, protect reversibility.

**Question 8 (moderate) — Least effective: the criteria dispute in public**

At a programme board, an experienced delivery manager attacks your acceptance criteria as "gold-plating that delays value", citing a criterion requiring tested rollback for every release. Several board members look persuaded. Which response is LEAST effective?

- A) Explain the criterion's rationale with a concrete example — the release last year that a tested rollback converted from a nine-hour outage into a twenty-minute blip — and offer to review any criterion's cost-benefit with evidence, through the agreed change process for the framework.
- B) Acknowledge the cost the criterion imposes, and commit to examining whether lighter-weight rollback evidence could serve low-risk release types.
- C) Tell the board that the criteria are mandated and not open for discussion.
- D) Invite the delivery manager to bring specific instances where the criterion cost more than it protected, as input to the next framework review.

**Correct answer: C**

**Explanation:** Options A, B and D share a structure: they defend the framework's substance while keeping its authority open to evidence — rationale with a worked example (A), proportionality honestly examined (B), and challenge converted into structured input (D). Any of them can win the room, and together they model how standards survive: by being defensible, not by being undiscussable. Option C is the least effective precisely because it may work today — the board may back down — while teaching every attender that the criteria rest on assertion rather than reason. Undiscussable standards accumulate quiet workarounds; the next challenge happens not at a board you attend but in a corridor you don't. Your duty that criteria be understood by wider IT operations includes understood as reasonable — and "mandated, not open for discussion" is the sentence that ends understanding. The behavioural principle: authority spent defending standards from scrutiny is authority lost; standards that invite scrutiny and survive it stop being attacked.

**Question 9 (hard) — What the user data says versus what the deadline needs**

A replacement benefits-claim service is at the acceptance gate. All technical criteria are met. But the user research completed last week shows that claimants over 65 — 22% of the service's users — fail the new identity-verification step at three times the rate of other groups, mostly abandoning their claims entirely rather than phoning the helpline. The old service is contractually decommissioned in six weeks, and each week of delay costs a substantial extension fee. The service owner asks for your recommendation. What is the most effective position?

- A) Recommend go — technical criteria are all met, and user experience can be improved post-launch.
- B) Recommend no-go until the verification step is redesigned, whatever the extension costs.
- C) Recommend a conditional position built on the evidence: quantify the harm (claims abandoned per week by the affected group, against the extension fee), and present the service owner with worked options — go with an immediate assisted-digital route and monitored abandonment thresholds that trigger intervention, or a short paid extension to fix the step — with your assessment of which best serves users and value together.
- D) Recommend go, and ask the helpline to expect increased call volumes.

**Correct answer: C**

**Explanation:** This scenario is the role at its hardest: every criterion on paper is met, and the service is still not fit for purpose for one user in five — the acceptance framework's letter and its purpose have come apart. Option A hides behind the letter: "user experience" understates what the data shows, which is protected-characteristic users abandoning benefit claims — harm, not friction, and exactly what your **User focus** skill exists to keep decisive. Option B honours the users and abandons the arithmetic: "whatever the costs" is not a recommendation, it is a value judgement pre-empting the service owner's actual decision — and a paid extension has user costs too, since the old service presumably had its own failings. Option C does the transition manager's real job: it converts the dilemma into a quantified decision — abandoned claims per week versus extension fees, with mitigation options costed and consequenced — and routes it, with a stated professional view, to the decision's owner. Note what C refuses to do: it will not let the decision be made without the user data on the table, and it will not make the service owner's decision for them. Option D is A with the harm relabelled as a staffing forecast. Rewarded behaviours: user evidence kept decisive, trade-offs quantified rather than absorbed, decisions routed with recommendations attached, and no false comfort in "criteria met".

**Question 10 (hard) — The pattern across your own portfolio**

Preparing your quarterly report, you notice that across nine transitions this year, the three that went worst shared one feature: operations teams first engaged with the service less than a month before go-live. The three smoothest had operations engaged from design onward. Your report goes to the head of IT operations, who has previously said "ops can't spare people for projects that might not ship." What is the most effective use of this finding?

- A) Include the correlation in your report with the six data points, cost the three bad transitions (incident volumes, early-life overruns, delayed benefits), acknowledge the head of operations' resourcing constraint, and propose a bounded experiment: token operations engagement (two hours weekly) from design stage on the next two transitions, measured against the same outcomes.
- B) Leave it out — the head of operations has already made their position clear.
- C) Present the correlation as proof that the head of operations' policy caused the failures.
- D) Share the finding informally with project managers so they can each lobby operations separately.

**Correct answer: A**

**Explanation:** You hold a genuine pattern — six data points across your own portfolio, the classic "initiate and monitor actions to investigate patterns and trends" of your **Problem management** skill, applied to the transition process itself. Option A converts it into organisational change with every persuasion principle working for it: the data is offered as correlation, not accusation (nine transitions is suggestive, not proof — intellectual honesty here is also tactical wisdom); the costs are quantified in the currency the reader cares about; the reader's stated constraint is treated as real rather than as resistance; and the proposal is small enough to say yes to — two hours weekly, two transitions, measured. That last property is the craft: findings become change when the first step is cheaper than the argument. Option B lets a prior objection veto evidence the objector has never seen — the head of operations opined about resourcing in general, not about your six data points. Option C overclaims causation and converts a potential ally into a defendant; even if you are right, the report becomes about the accusation, not the fix. Option D fragments a systemic finding into uncoordinated lobbying, spending the evidence without ever presenting it properly — and ensures the head of operations first hears the finding as corridor rumour. Rewarded behaviours: evidence over anecdote, honest claim-sizing, constraints respected, proposals sized to succeed.

**Question 11 (hard) — The handover that isn't one**

You are six weeks from leaving for a new role. Your flagship transition — a two-year programme entering its critical phase — will be handed to a successor who has not yet been recruited. The programme director suggests: "Just write everything down; whoever comes can read it." You know from experience that the transition's real risks live in unwritten context: which supplier commitments are soft, which stakeholders need pre-meetings, why the cutover plan has a strange-looking constraint. What is the most effective response?

- A) Write the comprehensive handover document as asked — it is the best available option.
- B) Propose a structured transfer instead of a document alone: identify an interim owner now from the existing team, brief them into the critical relationships and soft knowledge over your remaining weeks, record the genuinely writable material, and schedule a post-departure call for the eventual successor — putting this plan to the director with the specific risks a document-only handover leaves uncovered.
- C) Delay your departure until a successor is recruited and fully inducted.
- D) Leave detailed documentation and your personal phone number, and tell the team to call you.

**Correct answer: B**

**Explanation:** This is your **Ownership and topic** skill at its most senior interpretation: owning an issue until a new owner is found — where the issue is the transition itself, and "found" means genuinely equipped, not merely appointed. Option B is built on an accurate theory of knowledge transfer: documents carry facts; relationships and judgement transfer person-to-person, over time, or not at all. Naming an interim owner from the existing team converts your remaining six weeks from documentation time into apprenticeship time, and putting the risk analysis to the director respects their authority while correcting their model — "write everything down" fails not because writing is useless but because the riskiest knowledge is precisely the kind that doesn't write. Option A complies with a plan you have good reason to believe insufficient, without saying so: agreeable, and a disservice. Option C sacrifices your own legitimate career move to an organisational gap you did not create and cannot indefinitely fill — and "fully inducted" has no defined end. Option D privatises the safety net: informal, unfunded, dependent on your goodwill and availability, and structurally guaranteed to decay. Rewarded behaviours: honest risk analysis of proposed plans, ownership defined by outcomes not gestures, succession treated as a transition to be managed — because it is one.

**Question 12 (hard) — The quiet disagreement in your own team**

In your transition team's retrospective, a pattern surfaces: your two analysts consistently rate the team's psychological safety lower than everyone else, and one comments that "findings get softened between our drafts and the final reports." Reviewing recent papers, you realise it is partly true — you have been moderating their more alarming language before reviews, believing you were calibrating tone. They have experienced it as being overruled. What is the most effective response?

- A) Explain to the analysts why calibration is necessary and that they will understand when more senior.
- B) Stop editing their sections entirely — publish their drafts verbatim to restore trust.
- C) Acknowledge the pattern openly in the team, distinguish the two things that have been happening (legitimate calibration of language versus changing the substance of findings), agree a visible rule — substance changes only with the finding's author, and disagreements escalate as joint positions showing both views — and invite them to flag the next instance in real time.
- D) Treat the retrospective feedback as a team-dynamics issue for the analysts to work through themselves.

**Correct answer: C**

**Explanation:** The scenario hands you an uncomfortable finding about yourself, with the same structure as any other finding: evidence (ratings, the comment, your own review of the papers), a mechanism (edits experienced as overruling), and a fix to design. Option C treats it exactly as your professional standards would treat a service problem — acknowledged openly, decomposed accurately, remedied structurally. The decomposition is the craft: calibrating tone is a legitimate senior function; changing what a finding says is a different act, and the rule "substance moves only with the author, disagreements travel as joint positions" separates them visibly — protecting both the quality of reports and the ownership of the people who write them. The real-time flagging invitation converts the fix from promise to practice. Option A answers evidence with hierarchy — "you'll understand when senior" is the sentence that stops retrospectives being honest ever again. Option B swings from over-editing to abdication: your calibration adds genuine value, and abandoning quality control to purchase goodwill trades one team dysfunction for another. Option D outsources a problem whose cause sits in your own editing practice — the analysts cannot fix it because they did not create it. This is **Community collaboration** at your level: creating the right environment includes repairing it when the damage traces to you. Rewarded behaviours: non-defensive response to feedback, accurate problem decomposition, structural fixes over reassurance, and modelling the evidence-handling you require of others.

### Preparation tips

- **Study your behaviour framework, then map these scenarios to it.** User focus, collaboration, ownership, honesty, escalation, inclusion — every scenario above rewards a recognisable combination. Naming the combination is what makes unseen scenarios readable.
- **Rehearse the conditional-recommendation structure.** Quantify, present options with consequences, state your view, route to the decision owner. It resolves half the hardest scenarios in this test and most of the hardest weeks in this job.
- **Practise the direct-conversation-first rule.** Before escalating past someone, the effective options almost always try one specific, deadline-explicit conversation with them. Note how often the least effective options skip it — in both directions.
- **Distinguish the record from the relationship.** High-scoring responses protect both, in that order: correct the record, then repair the relationship with candour. Options that trade the record for comfort score poorly without exception.
- **Do a pre-mortem on your instincts.** Read each scenario, commit to an answer, then ask: "if this went wrong, what would the review say I missed?" It reliably surfaces the option-set's hidden risk — usually the one the correct answer addresses.
- **Answer as your consistent professional self.** SJTs include consistency measures, and gaming a persona both underperforms and misdescribes you. Considered, honest answers pattern best.

### Common pitfalls to avoid

- **Absolutism in genuine dilemmas.** "The window is committed" and "P1s outrank everything" are both abdications of judgement. Effective responses verify, bound, and re-plan — they hold both commitments as long as possible.
- **Hiding behind met criteria.** When evidence shows harm the criteria missed, "technically compliant" scores as poorly in the test as it performs in public services. The criteria serve the purpose, not the reverse.
- **Escalating before the direct conversation — or instead of it.** Skipping the person who acted wastes the cheapest resolution route and spends escalation capital you will want later.
- **Protecting people from accountability, or punishing them past it.** Silent fixes and disciplinary referrals are twin failures; the effective middle is correction plus development plus a bounded check of the blast radius.
- **Private records instead of timely objections.** Documentation that exists to protect you at the moment it fails to protect the service is the pattern scoring keys punish most reliably.
- **Winning rooms by closing them.** "Mandated, not open for discussion" and "you'll understand when senior" end conversations and start workarounds. Standards and seniority survive scrutiny or they don't survive.

## Conclusion

You have now worked through a complete, role-specific practice programme — and if you attempted the questions honestly before reading the explanations, you have done something more valuable than test preparation: you have rehearsed the core judgements of service transition management in concentrated form.

Consider what the four sections have exercised. The cognitive section drilled the verification and reasoning habits that fitness-for-purpose decisions rest on: checking evidence status against claimed status, tracing dependency models exactly as written, computing critical paths rather than intuiting them, and holding the line between what evidence supports and what pressure prefers. The numeric section rebuilt the arithmetic of your recommendations — pass rates recomputed from raw counts, availability converted between percentages and minutes, velocities projected against deadlines, and reconciliations anchored on intersections rather than totals — the numerical scepticism that lets you probe a supplier's figures before the review probes yours. The verbal section sharpened your reading of the documents your role runs on: verb ladders and actor swaps, exception clauses read for exactly what they except, confidence language separated from status, and criteria drafted so that two strangers must reach the same verdict. And the situational judgement section mapped the behavioural terrain of your level — evidence-based positions held with civility, escalation done transparently and in sequence, decisions quantified and routed to their owners, teams repaired rather than managed around, and users kept decisive when every organisational pressure points the other way.

If you are preparing for a specific assessment, structure the next fortnight simply: short sessions, spaced out; wrong answers revisited and re-explained in your own words; light time pressure added only once accuracy is stable; and a rested, quiet, well-set-up test day. Familiarity with format plus practised technique removes most of what makes assessments feel hazardous — what remains is the same professional judgement you exercise every week, sampled under a clock.

Beyond the test, let this guide double as a development mirror. The techniques here are the observable behaviours of transition management done well: the recomputed headline, the two-reader criterion, the conditional recommendation, the escalation with analysis attached. Each one is usable in your very next review — and each use compounds, because the transition manager who is known for precise evidence, defensible recommendations, and fair dealing accumulates the one asset the role cannot function without: the confidence of everyone who relies on the recommendation being right.

Prepare steadily, trust your practice, and take pride in what the role protects — services that go live safely, operations teams that inherit what they were promised, and users who never learn your name because nothing went wrong. Good luck.
