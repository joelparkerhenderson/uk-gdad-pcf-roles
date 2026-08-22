# Major Incident Manager - Psychometric Assessment Resources

## Introduction

Welcome. This guide has been written for you as a major incident manager working within the UK Government Digital and Data profession — the person who takes command when significant outages and crises threaten public services, who orchestrates workplace services, infrastructure, applications operators and communication managers into a single coherent response, and who, in some departments, also carries the responsibilities of head of service. Whether you are preparing for an internal assessment, a promotion board, a move into a new department, or simply benchmarking your own capability, this document will help you practise deliberately and reflect honestly.

Psychometric assessments are structured, standardised exercises that measure the mental capabilities and behavioural tendencies that predict success in a role. At your level, the assessments worth taking seriously are job-specific: they draw on the artefacts you genuinely command — major incident timelines, service hierarchies and dependency maps, availability and KPI reports, runbooks and continuity test results, change impact assessments, and communications to ministers' offices, press teams and the public — and the decisions you genuinely make, such as declaring or standing down a major incident, sequencing recovery across interdependent services, judging when a runbook should be followed and when it should be overridden, and holding a bridge call of twenty specialists to a single line of inquiry.

Why does this matter for your role in particular? Major incident management is decision-making under pressure, ambiguity and scrutiny. The cognitive load is real: you reason about partial, conflicting evidence from multiple teams while the clock runs and senior stakeholders demand certainty you do not yet have. The numeric load is real: impact quantification, availability arithmetic, KPI trade-offs and recovery-time projections are the currency of your escalation and reporting. The verbal load is real: you interpret continuity plans and severity definitions precisely under pressure, and you author or approve communications where a single ambiguous sentence can misinform thousands of users or an entire press office. And the judgement load is heaviest of all: command decisions about escalation, delegation, honesty under scrutiny, and the wellbeing and dynamics of the teams you lead are where major incident managers earn — or lose — trust.

The four assessments in this guide map directly onto those demands. Practising them sharpens exactly the capabilities your role depends on: recognising the failure pattern that connects five services, deducing recovery order from a dependency map, spotting the flaw in a confident hypothesis, quantifying impact defensibly, reading a severity matrix like a lawyer, and choosing the most effective command action when every option costs something.

This document is organised into four main assessment sections, each following the same pattern: an overview of what the assessment measures and why it matters at your level, a mapping of the assessment's dimensions to the specific skills in the major incident manager capability framework, a substantial set of practice questions with full worked explanations, practical preparation tips, and common pitfalls to avoid.

To get the most from it: read each "About this assessment" section first; attempt every question honestly before reading the explanation; treat each explanation as a masterclass in technique, not merely a marking key; and use the preparation tips as prompts for reflection on how you lead during real majors. Take your time. Let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive ability assessment measures the exact mental processes your role demands, using practical scenarios rather than abstract puzzles. For a major incident manager, that means questions built from dependency maps, incident timelines, conflicting diagnostic reports, runbook logic, severity criteria and recovery sequencing — the material of a live bridge call, compressed into assessment items.

Typical format: an online, timed test lasting 15 to 30 minutes, covering pattern recognition, logical deduction, error checking, prioritisation and applied problem solving. Scoring is objective against a norm group, frequently adaptive (questions get harder as you succeed), and reported to employers as accuracy and speed profiles rather than a single number. For senior operational roles, some employers pair the standard test with scenario-based extensions under deliberate time pressure, precisely because your working conditions include pressure as a feature.

At your level, cognitive assessment is less about raw processing and more about disciplined reasoning when information is incomplete, plausible stories are wrong, and everyone on the call is anchored on the first hypothesis. Leading the investigation and resolution of incidents means running a live epistemic process: keeping multiple hypotheses open, choosing the diagnostic action with the highest information yield, noticing when the evidence has quietly stopped supporting the working theory, and sequencing recovery so that dependencies, risks and user impact are all respected. The best major incident managers are not the fastest guessers; they are the most disciplined reasoners under load. That is exactly what these questions rehearse.

### How this assessment maps to your role

- **Pattern recognition** maps to **Incident management** and **Service focus**: leading investigation across significant outages requires seeing the bigger picture — recognising when alerts on separate services share one underlying cause, and how groups of services depend on shared underlying components.
- **Logical deduction** maps to **Incident management** and **Continuity management**: reasoning validly from symptoms, timelines and runbook preconditions to conclusions — and knowing what does not follow — is the core of command-quality diagnosis and of judging when a runbook applies.
- **Error checking** maps to **Asset and configuration management** and **Change management**: tracking and correcting information to protect assets, and analysing and assessing the impact of change, both require spotting the record, timeline entry or impact assessment that contradicts the rest.
- **Prioritisation** maps to **Ownership and initiative** and **Availability and capacity management**: taking accountability for issues, being proactive in searching for potential problems, and managing service components against business needs and KPIs all demand ranking by impact-weighted urgency across whole services, not single tickets.
- **Problem solving** maps to **Problem management** and your duty to report issues into problem management: decomposing a crisis into testable hypotheses, consulting specialists effectively, and determining preventative measures are structured problem solving under the harshest conditions your organisation offers.

### Practice questions

**Question 1 (easy) — Pattern recognition across service alerts**

At 07:55 your monitoring surface shows five alerts raised within four minutes: (1) case management application — database connection timeouts; (2) document store — slow writes; (3) staff intranet — normal; (4) payments service — database connection timeouts; (5) reporting warehouse — overnight load failed at 07:52. The case management application, payments service and reporting warehouse all use the shared database platform; the document store uses its own storage but authenticates via the shared platform. What is the most likely single point of failure?

- A) The case management application
- B) The shared database platform
- C) The staff intranet
- D) The document store's storage array

**Correct answer: B**

**Explanation:** Map each symptom to the dependency it exercises. Three consumers of the shared database platform fail with database-shaped symptoms (connection timeouts, failed load) inside one four-minute window; the document store — which only touches the platform for authentication — degrades rather than fails; and the intranet, which presumably does not depend on the platform, is healthy. The shared platform explains every observation, including the partial symptom on the partially dependent service and the health of the independent one. A and D each explain only one alert; C is not even symptomatic. The command habit this trains: when multiple services fail together, reach for the shared dependency that explains both the failures and the survivors — and use the survivors as evidence, not just the casualties.

**Question 2 (easy) — Deduction from severity criteria**

Your major incident criteria state: "Declare a major incident when (a) a critical service is fully unavailable, or (b) two or more critical services are significantly degraded, or (c) any incident attracts, or is likely to attract, ministerial or media attention." At 09:10, one critical service is significantly degraded (not unavailable), no other service is affected, and the press office rings to say a journalist has asked about the disruption. Must you declare?

- A) No — no criterion is met.
- B) Yes — criterion (a) is met.
- C) Yes — criterion (c) is met.
- D) Cannot determine without knowing the number of affected users.

**Correct answer: C**

**Explanation:** Test each criterion against the facts. (a) requires full unavailability of a critical service — the service is degraded, not unavailable, so (a) is not met. (b) requires two or more degraded critical services — only one is affected. But (c) triggers on actual or likely ministerial or media attention, and a journalist actively asking about the disruption is media attention already in progress. Criterion (c) is met, so declaration is mandatory — user numbers (D) are irrelevant because the criteria as written do not mention them. The professional point mirrors the logical one: media-attention triggers exist because reputational incidents are managed with the same rigour as technical ones, and a major incident manager who waits for technical thresholds while the press office burns has misread the rulebook. In assessments and on shift alike: apply each limb of a disjunctive rule independently and declare on the first that fires.

**Question 3 (easy) — Error checking an incident timeline**

A draft major incident timeline reads:

| Time | Entry |
|---|---|
| 06:30 | Overnight change to storage firmware completed successfully |
| 07:41 | First monitoring alert: database latency rising |
| 07:48 | Major incident declared |
| 07:44 | Bridge call opened |
| 08:03 | Storage vendor engaged |

Which entry most needs correction before the timeline is circulated?

- A) 06:30 — changes cannot complete that early
- B) 07:48 — declaration seems too fast
- C) 07:44 — the bridge call is recorded as opening before the major incident was declared
- D) 08:03 — vendors should be engaged sooner

**Correct answer: C**

**Explanation:** Scan for internal contradiction, not for judgements about what "seems" right. The rows are meant to be chronological, yet 07:44 appears after 07:48 — and substantively, a bridge call opening four minutes before declaration is possible in reality (calls are sometimes opened while declaring), so the fix may be reordering the rows or correcting a mistyped time; either way the entry as placed is wrong and will confuse every reader and every post-incident review. A, B and D are opinions about operational speed, not errors: nothing in the data forbids a 06:30 completion, a seven-minute declaration is commendably fast, and vendor engagement at 08:03 may be entirely reasonable. Timeline hygiene matters at your level because the timeline is the master evidence artefact — problem management, lessons-learned reviews and any external scrutiny all reason from it, and one out-of-order row undermines confidence in the rest.

**Question 4 (moderate) — Recovery sequencing from a dependency map**

Four components must be restored after a data-centre failover. Dependencies: the authentication service (A) depends on nothing; the database cluster (D) depends on nothing; the case application (C) depends on both A and D; the citizen-facing portal (P) depends on C and A. You have two restoration teams, each able to restore exactly one component at a time; each component takes one hour. What is the minimum total time to restore all four components?

- A) 1 hour
- B) 2 hours
- C) 3 hours
- D) 4 hours

**Correct answer: C**

**Explanation:** Draw the dependency layers before touching the clock. Layer 1: A and D have no prerequisites — with two teams, restore both in parallel during hour 1. Layer 2: C needs A and D, both now up — one team restores C during hour 2. The second team is idle in hour 2, because P's prerequisite C is not yet complete: P needs C and A, and C only finishes at the end of hour 2. Layer 3: P is restored in hour 3. Minimum total: 3 hours. The tempting answer B comes from parallelising P alongside C in hour 2, which the dependency P→C forbids — having a free team does not make a blocked task startable. In live failover the same error is costlier still: restoring a dependent service before its prerequisite does not save an hour, it adds one, because the dependent service fails its health checks and must be restarted after its prerequisite arrives. Layered restoration plans, with idle capacity accepted where dependencies dictate, are how **Continuity management** runbooks are actually written and tested — and questions like this reward candidates who draw the layers first and let the clock follow.

**Question 5 (moderate) — Hypothesis discipline on a bridge call**

Forty minutes into a major incident, the working hypothesis is "last night's firewall rule change broke application connectivity". Evidence so far: (i) the outage began roughly eight hours after the change window closed; (ii) rolling back the firewall change ten minutes ago has produced no improvement; (iii) the network team reports traffic is flowing normally through the firewall; (iv) the application vendor mentions a known memory defect triggered by month-end batch volumes — and today is the first working day of the month. What should you, as incident commander, direct next?

- A) Reapply and re-roll-back the firewall change to double-check the rollback was clean.
- B) Redirect the investigation toward the month-end batch/memory hypothesis, keeping the firewall line open only until the rollback's ineffectiveness is confirmed as clean.
- C) Continue with the firewall hypothesis — the change is the only thing that changed.
- D) Ask both teams to keep investigating their own theories independently for another hour.

**Correct answer: B**

**Explanation:** Score each hypothesis against all the evidence. The firewall theory now has three strikes: an eight-hour gap between change and failure (weak temporal fit), a rollback that changed nothing (the strongest disconfirmation available), and direct observation of normal traffic. The batch/memory theory fits the strongest unexplained fact — timing aligned with month-end — and comes with a vendor-confirmed mechanism. B follows the evidence while closing the old line cleanly rather than abandoning it ragged. C is anchoring: "the only thing that changed" was already tested by rollback and failed. A buys marginal confirmation at the cost of two more disruptive changes to a live estate. D abdicates the commander's core function — convergence: parallel investigation is healthy early, but forty minutes in, with discriminating evidence available, the commander's job is to focus effort where the evidence points. Leading the investigation and resolution of incidents — your **Incident management** skill — is precisely this: updating the room's beliefs at the speed of the evidence, not the speed of consensus.

**Question 6 (moderate) — Error checking a change impact assessment**

A change impact assessment for an urgent certificate replacement states: (i) "Services affected: citizen portal only"; (ii) "The portal shares its certificate with the mobile API gateway"; (iii) "Rollback: reinstate previous certificate, 15 minutes"; (iv) "Risk if not actioned: certificate expires at midnight, portal unavailable thereafter". Which pair of statements is mutually inconsistent?

- A) (i) and (ii)
- B) (ii) and (iii)
- C) (iii) and (iv)
- D) (i) and (iv)

**Correct answer: A**

**Explanation:** Statement (ii) says the certificate is shared with the mobile API gateway; statement (i) claims only the portal is affected. Both cannot be true: replacing a shared certificate necessarily touches every service that presents it, so the impact scope in (i) understates the blast radius that (ii) itself discloses. (iii) and (iv) are each internally plausible and consistent with everything else. Catching this before approval matters twice over: operationally, the mobile API's consumers deserve warning and testing; procedurally, an impact assessment that contradicts itself signals the analysis was not finished — and your **Change management** skill at this level is exactly to analyse and assess the impact of change, not merely to file the form. Assessment items like this train the reviewing eye: read impact assessments as claims to be cross-checked against each other, not as boxes already ticked.

**Question 7 (moderate) — Prioritisation across concurrent majors**

An extraordinary morning: two incidents both meet major criteria. Incident X: the benefits payment calculation service is down; tonight's payment run deadline is 18:00; 40,000 citizens' payments depend on it; a tested manual fallback exists but takes six hours to execute and must therefore start by 12:00 if needed. Incident Y: the department's public website is defaced with offensive content; it is attracting social media attention; takedown is technically simple (under an hour) but requires security team coordination to preserve forensic evidence. It is 09:30. You have one deputy qualified to command a major. What is the most effective command structure?

- A) Command X yourself; delegate Y to your deputy with clear objectives (takedown with evidence preservation) and a reporting cadence.
- B) Command Y yourself — reputational incidents need the senior person; give X to the deputy.
- C) Command both yourself, alternating attention between bridge calls.
- D) Fully resolve Y first (it is quicker), then start X at about 10:30.

**Correct answer: A**

**Explanation:** Compare the incidents' command demands, not just their visibility. X carries the greater complexity and the harder decision: a hard 18:00 outcome deadline with an embedded 12:00 decision point (start the six-hour fallback or gamble on a fix) — that go/no-go call under uncertainty is exactly what your most senior judgement exists for, and 40,000 citizens' payments is the deeper harm. Y is serious but procedurally bounded: takedown plus evidence preservation is a well-defined objective a competent deputy can own, and delegating it with explicit objectives and a reporting cadence is a textbook use of **Community collaboration** — delegation with clarity is not abandonment. B assigns seniority by loudness: social media attention is real, but the deputy can silence it within the hour while you carry the decision that cannot be delegated safely. C is the classic senior failure mode — two half-commanded majors are worse than two commanded ones, because command is attention. D leaves X uncommanded for an hour of a nine-hour window containing a 12:00 decision gate — an unforced squandering of the scarcest resource, time before the gate. At assessment and in reality: allocate the senior mind to the decision only the senior mind can make.

**Question 8 (challenging) — Deduction under conflicting reports**

During a major, three teams report: the applications team says "the application is healthy; the database is refusing connections"; the database team says "the database is up and accepting connections; we can query it directly"; the network team says "no packet loss anywhere on the network". Assume all three reports are accurate about what each team actually tested. Which conclusion follows?

- A) At least one team is lying, since the reports contradict each other.
- B) The fault most plausibly lies in something between the application and the database that direct database access does not traverse — such as a connection pool, middleware layer, or authentication path — since each team's local test can be true while end-to-end connectivity fails.
- C) The database team's report proves the applications team is mistaken.
- D) The network team's report proves the fault is in the application code.

**Correct answer: B**

**Explanation:** The reports only contradict each other if they measure the same path — and they do not. The database team tested direct access (their own tools, their own credentials, possibly their own network segment); the application experiences the full end-to-end path: its connection pool, its middleware, its credentials and certificates, its route. All three reports can be simultaneously true if a component on the application's path — but not on the DBA's path — is failing: an exhausted connection pool, an expired service account, a middleware tier, a misbehaving load balancer that "no packet loss" does not exonerate (packets flow; sessions fail). A confuses difference of vantage with dishonesty. C and D each treat one team's local truth as global proof. The command skill here is precious: when accurate reports conflict, the fault usually lives in the untested gap between their vantage points — so your next direction is to test the application's actual path, credential and pool. This is leading investigation at its purest: constructing, from partial truths, the experiment that finds the whole one.

**Question 9 (challenging) — Runbook preconditions under pressure**

The continuity runbook for the case management service says: "Failover to the secondary site may be invoked when (i) the primary site is expected to be unavailable for more than four hours, AND (ii) data replication to the secondary is confirmed current within the last 15 minutes. If replication currency cannot be confirmed, failover requires the service owner's explicit acceptance of potential data loss." It is 10:00; the primary has been down an hour; the infrastructure lead estimates six more hours; the replication dashboard is itself unreachable, so currency cannot be confirmed; the service owner is reachable. What does the runbook require before failover?

- A) Nothing further — condition (i) is met and that suffices.
- B) Wait until the replication dashboard is restored, however long that takes.
- C) Obtain the service owner's explicit acceptance of potential data loss, because condition (ii) cannot be confirmed.
- D) Failover is forbidden outright when replication cannot be confirmed.

**Correct answer: C**

**Explanation:** Parse the rule's structure. The main clause requires (i) AND (ii). Condition (i) is met: one hour down plus six projected exceeds four hours. Condition (ii) fails — not because replication is known stale, but because it cannot be confirmed, and the runbook explicitly provides for exactly this case: unconfirmed currency converts the decision into one requiring the service owner's informed acceptance of potential data loss. So the runbook's answer is C: escalate the risk decision to its named owner, who is reachable. A ignores the conjunction. B invents a waiting requirement the runbook does not contain and burns the outage window. D misreads a conditional escalation as a prohibition. Two senior lessons: first, well-written runbooks anticipate their own measurement failures — your **Continuity management** duty to manage and test runbooks includes checking that they do; second, the commander's role in a data-loss decision is to frame it honestly for the accountable owner, not to absorb it silently or dodge it procedurally.

**Question 10 (challenging) — Spotting the survivorship error in a "pattern"**

Reviewing the last twelve majors, your deputy observes: "In nine of the twelve, we eventually found the cause was a recent change. So in future majors, we should spend the first hour exclusively investigating recent changes." Which is the strongest critique of this proposal?

- A) Twelve incidents is a reasonable sample, so the proposal is sound.
- B) The observation may be true, yet the policy still wrong: exclusive focus discards the 25% of majors with non-change causes, and even change-caused majors may present evidence (like Question 5's) that should redirect investigation early — a strong prior should weight the first hypotheses, not monopolise the first hour.
- C) The proposal is wrong because changes never cause majors.
- D) The proposal is wrong because past incidents tell us nothing about future ones.

**Correct answer: B**

**Explanation:** The deputy's base rate is genuinely useful — a 75% historical rate makes "recent change" the correct first hypothesis — but the leap from strong prior to exclusive first hour is where the reasoning breaks. Exclusivity has two costs: three of twelve majors would have spent their golden hour looking in the wrong place by policy; and even within the nine, disconfirming evidence (a clean rollback, a timing mismatch) should be allowed to redirect effort before the hour expires. The disciplined version is: start with change review as the leading line, in parallel with a broad evidence sweep, and let discriminating evidence update the allocation continuously. C and D are overcorrections that discard the data entirely — D in particular would forbid learning from incidents at all, which is the opposite of your **Problem management** duty to investigate patterns and trends. Assessment items like this test a distinctly senior skill: separating a true observation from the flawed policy someone builds on it, and repairing the policy rather than rubbishing the observation.

**Question 11 (challenging) — Applied problem solving: the intermittent major**

A critical service fails for three to five minutes at unpredictable intervals — roughly twice daily for a week. Each failure self-recovers before any team can capture diagnostics. The vendor requests "logs from during a failure window". Teams propose four approaches. Which offers the best expected diagnostic yield?

- A) Ask all teams to watch their dashboards more closely and react faster at the next failure.
- B) Configure continuous rolling capture (verbose logs, connection metrics, packet capture on relevant paths) with automatic preservation triggered by the failure signature, so the next failure documents itself.
- C) Restart all components nightly, which might make the failures stop.
- D) Schedule a maintenance window and attempt to reproduce the failure by load-testing production.

**Correct answer: B**

**Explanation:** The defining constraint is that the failure is shorter than any human reaction time — so any plan built on reacting (A) has already failed a week's worth of trials. B removes the human from the capture loop: instrumentation runs continuously, and the failure itself triggers preservation, converting the very unpredictability of the fault into a guarantee of evidence at the next occurrence. C is anti-diagnosis: if nightly restarts suppress the symptom, you have hidden a defect that will return — probably at scale, probably at the worst time — with nothing learned; masking a fault is not resolving a problem, and your **Problem management** skill exists precisely to prevent recurrence, not postpone it. D risks a self-inflicted major (load-testing production) to force what patience and instrumentation will capture safely. The senior insight: for intermittent faults, engineer the observation, not the observer — spend effort making the next occurrence informative rather than hoping the next occurrence is convenient. This is being proactive in searching for potential problems, applied with method.

**Question 12 (challenging) — KPI trade-off reasoning**

Two restoration options exist for a degraded document service, 90 minutes before the daily 16:00 peak. Option 1: full fix now — 2 hours' work, requiring 30 minutes of total outage during the work, service then fully restored at ~16:30, through peak on outage-then-full-service. Option 2: apply a partial mitigation — 20 minutes' work, no outage, service runs at 70% capacity through peak, full fix deferred to tonight's change window. The service's KPIs: availability (any total outage breaches it) and peak-hour throughput (70% capacity means slower processing but no failure). The business impact of a 30-minute total outage at 15:00 is queued casework that recovers within the day. What should you recommend, and on what reasoning?

- A) Option 1 — always fix fully at the first opportunity.
- B) Option 2 — it avoids a certain availability breach at the cost of a bounded, tolerable throughput degradation, and completes the full fix in a controlled window hours later.
- C) Option 1 — availability KPIs matter less than throughput KPIs.
- D) Neither — wait until after peak to decide.

**Correct answer: B**

**Explanation:** Structure the trade: Option 1 exchanges a certain 30-minute total outage (a definite availability breach, queued casework, users locked out) plus mid-afternoon change risk, for full capacity roughly at peak's midpoint. Option 2 exchanges 30% capacity through peak (degradation, no denial of service, no breach) for a few hours' deferral of the real fix into a proper change window — with lower execution risk, since 20 minutes of non-disruptive work now beats 2 hours of disruptive work against the clock. On both KPI arithmetic and risk shape, Option 2 dominates unless the 70% figure is unsafe — which the stem says it is not. A is a slogan, not an analysis: "fix fully first" ignores that timing is part of the fix. C inverts the stated KPI structure. D is the hidden worst answer: "wait to decide" is itself a decision — it forfeits Option 2's 20-minute window and drifts toward peak with nothing mitigated. This is **Availability and capacity management** as your framework defines it — managing service components against business needs and KPIs — expressed as a single command decision, and it rehearses the recommendation you would defend afterwards to the service owner in plain numbers.

### Preparation tips

- **Rebuild dependency maps from memory.** Sketch your critical services and their shared underlying components, then verify against the real architecture. Fluency with the map is what makes multi-service pattern questions — and multi-service majors — fast.
- **Practise hypothesis bookkeeping.** In your next incident reviews, reconstruct which hypotheses were live at each point and what evidence killed each one. This trains the update discipline that Questions 5, 8 and 10 reward.
- **Read your own runbooks adversarially.** For each, ask: what are the preconditions, what happens when a precondition cannot be measured, and who owns each embedded risk decision? You will improve at precondition questions and improve the runbooks — your continuity duty either way.
- **Time-box your practice harshly.** Senior candidates lose marks by over-verifying easy items and starving hard ones. Practise allocating: easy items fast and once; hard items with your full method.
- **Do a daily reasoning drill during quiet weeks.** Ten minutes of mixed deduction and sequencing items keeps the machinery warm between majors, exactly as continuity tests keep failover warm between disasters.
- **Review your errors by mechanism, not by topic.** "I anchored", "I missed a conjunction", "I trusted an unordered timeline" — naming the mechanism is what prevents recurrence. You would accept nothing less from a post-incident review.

### Common pitfalls to avoid

- **Anchoring on the first plausible cause.** The question (and the bridge call) will feed you a tidy story early. Score every hypothesis against all the evidence, and treat a failed rollback as the strong disconfirmation it is.
- **Treating vantage-point conflicts as contradictions.** When two accurate reports disagree, look for the untested gap between them rather than deciding whom to believe.
- **Misparsing AND/OR in criteria and runbooks.** Conjunctions, disjunctions and explicit exception clauses decide declaration, failover and escalation questions. Parse the structure before applying the facts.
- **Parallelising across a dependency.** In sequencing questions, idle capacity is sometimes correct. Restoring a dependent component early does not save time; it costs a restart.
- **Confusing suppression with resolution.** Options that make symptoms stop without explaining them (nightly restarts, quiet workarounds) are traps in cognitive items and in problem management alike.
- **Letting seniority or loudness set priority.** Media noise, senior attention and dramatic symptoms all pull attention; impact, deadlines and decision points should allocate it. Command the incident that needs commanding.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment measures your ability to interpret, manipulate and draw defensible conclusions from the numerical material your role actually produces: impact quantifications, availability and KPI reports, incident and recovery-time arithmetic, capacity projections, cost-of-outage calculations, and post-incident trend data. Calculators are normally permitted; the test measures whether you select the right calculation and read data accurately, not mental arithmetic for its own sake.

Typical format: 20 to 35 minutes, 15 to 25 questions, each presenting a table, chart or short data narrative followed by multiple-choice options. Senior-level versions lean toward multi-step items — weighted figures, compound comparisons, projections with stated assumptions — and toward interpretation traps: the plausible number computed on the wrong base, the average that hides the tail, the trend read from too few points.

For a major incident manager, numbers are command instruments. During a major, your impact statement — how many users, which business functions, what statutory or payment deadlines are exposed — sets the response's scale and seniority; a wrong figure mis-sizes the whole response. Your recovery decisions weigh options measured in minutes of outage, percentages of capacity, and probabilities of failure. After the incident, your reporting converts downtime into availability arithmetic against KPIs, and your problem management submissions argue with recurrence counts and cost figures. If you also act as head of service, KPI portfolios and capacity headroom become your standing responsibility rather than your incident-time reading. Employers test numeric reasoning at this level because senior operational judgement without numerical honesty is confident guesswork — and because your numbers are repeated upward, to service owners, directors and ministers' offices, usually without anyone re-checking them.

### How this assessment maps to your role

- **Availability and KPI arithmetic** maps to **Availability and capacity management**: managing service components to meet business needs and KPIs means converting fluently between availability percentages, downtime minutes, and breach thresholds — in both directions, under time pressure.
- **Impact quantification** maps to **Incident management** and **Ownership and initiative**: leading investigation and resolution includes stating impact defensibly — user counts, affected functions, exposure to deadlines — and being accountable for those figures afterwards.
- **Trend and recurrence analysis** maps to **Problem management**: initiating investigation of patterns and trends, and making the case for preventative measures, is done with recurrence counts, rates and costs.
- **Projection and headroom reasoning** maps to **Availability and capacity management** and **Continuity management**: capacity forecasts and recovery-time arithmetic (including runbook timings you are required to test) are projections with assumptions you must surface.
- **Reading and weighting mixed tables** maps to **Service focus**: seeing the bigger picture across groups of services requires combining per-service figures correctly — weighted, not naively averaged.
- **Cost-benefit framing** maps to **Change management** and your reporting into problem management: analysing and assessing the impact of change, and arguing for fixes, both reduce to honest cost and payback arithmetic.

### Practice questions

**Question 1 (easy) — Downtime allowance from an availability target**

A critical service has a 99.9% monthly availability target. The month has 30 days (720 hours). How many minutes of unplanned downtime are allowed before the target is breached?

- A) 7.2 minutes
- B) 43.2 minutes
- C) 72 minutes
- D) 432 minutes

**Correct answer: B**

**Explanation:** Allowed downtime = (100% − 99.9%) × total time = 0.1% of 720 hours. Step 1: 0.001 × 720 = 0.72 hours. Step 2: 0.72 × 60 = 43.2 minutes. Sanity check: 1% of 720 hours would be 7.2 hours (432 minutes), so 0.1% must be a tenth of that — 43.2 minutes. Options A and D are the classic decimal-shift errors in each direction. Knowing this conversion cold changes your live decision-making: when a fix option involves "about 30 minutes of outage", you know immediately that it consumes most of a 99.9% service's monthly allowance — which is exactly the calculation behind recommending a mitigation instead.

**Question 2 (easy) — Impact quantification across user groups**

An outage affects three user groups: 1,200 caseworkers (fully unable to work), 3,000 office staff (email delayed but working), and 450 contact-centre agents (fully unable to work). For your impact statement, how many users are fully unable to work, and what percentage of the total affected population (to the nearest whole per cent) is that?

- A) 1,650 users; 35%
- B) 1,650 users; 55%
- C) 4,650 users; 100%
- D) 1,200 users; 26%

**Correct answer: A**

**Explanation:** Step 1: fully unable = 1,200 + 450 = 1,650. Step 2: total affected population = 1,200 + 3,000 + 450 = 4,650. Step 3: 1,650 ÷ 4,650 = 0.3548… ≈ 35%. The impact statement should carry both figures with their distinction intact: "4,650 users affected, of whom 1,650 (35%) cannot work at all." Collapsing the distinction in either direction misleads — "4,650 affected" alone overstates severity; "1,650 affected" alone understates reach. Defensible impact numbers, with severity strata explicit, are the foundation of correctly sized major responses and of your accountability for them afterwards.

**Question 3 (easy) — Reading a KPI table for breaches**

The monthly service report shows:

| Service | Availability target | Actual | Peak-hour response target | Actual |
|---|---|---|---|---|
| Case management | 99.5% | 99.7% | < 2.0 s | 2.4 s |
| Payments | 99.9% | 99.9% | < 1.5 s | 1.3 s |
| Document store | 99.0% | 98.8% | < 3.0 s | 2.1 s |

How many KPI breaches does the table show in total?

- A) 1
- B) 2
- C) 3
- D) 4

**Correct answer: B**

**Explanation:** Check all six cells against their targets. Case management: availability 99.7% vs 99.5% — met; response 2.4 s against a "< 2.0 s" target — breach. Payments: 99.9% vs 99.9% — met exactly (equalling an availability floor meets it); 1.3 s vs < 1.5 s — met. Document store: 98.8% vs 99.0% — breach; 2.1 s vs < 3.0 s — met. Total: 2 breaches, on different services and different KPI types. The reading discipline — every cell, correct comparator, noting that "< 2.0" is a ceiling while availability is a floor — is the same care you apply before signing a report that a director will quote. Note also the service-level insight: the healthiest headline service (Case management, availability exceeded) still breached its user-experienced response KPI; availability alone is not user experience.

**Question 4 (moderate) — Recovery-time arithmetic against a deadline**

At 11:00 a payments service fails. The payment run must complete by 18:00 and takes 3.5 hours once started. Two recovery options: Option A — repair in place, estimated 2 hours with 70% confidence, else a further 2 hours (total 4). Option B — failover to secondary, a tested 1.5-hour runbook with high confidence, plus 30 minutes of data verification before the run can start. For each option, what is the latest completion time of the payment run if things go to plan, and which option risks missing the deadline in its slow case?

- A) A: 16:30 on plan, and its slow case misses the deadline; B: 16:30 on plan.
- B) A: 15:00 on plan, no risk; B: 17:00 on plan.
- C) A: 16:30 on plan, no risk; B: 15:30 on plan.
- D) Both options miss the deadline in all cases.

**Correct answer: A**

**Explanation:** Work each timeline. Option A on plan: repair 11:00 → 13:00; run 13:00 → 16:30 — done 90 minutes early. Option A slow case: repair 11:00 → 15:00; run 15:00 → 18:30 — misses the 18:00 deadline by 30 minutes, with 30% probability. Option B: failover 11:00 → 12:30, verification → 13:00; run 13:00 → 16:30 — same on-plan finish as A, but from a tested runbook with high confidence and no slow branch that breaches. So A's description in option A is correct: both finish 16:30 on plan, and only Option A's slow case misses. The decision insight this arithmetic exposes: the options tie on the happy path, so the choice is really about the tail — a 30% chance of breaching a statutory-style deadline versus a tested procedure's small residual risk. Timeline arithmetic that explicitly computes the bad branch, not just the plan, is what separates a defensible command decision from optimism — and it is why runbook timings must be tested (your **Continuity management** duty), because untested timings make this arithmetic fiction.

**Question 5 (moderate) — Weighted availability across a service group**

As head of service you report a combined availability figure for a service group, weighted by user base: Service X — 10,000 users, 99.8% availability; Service Y — 30,000 users, 99.2%; Service Z — 10,000 users, 99.6%. What is the user-weighted availability (to two decimal places), and how does it compare with the simple average?

- A) 99.53% weighted; equal to the simple average
- B) 99.40% weighted; lower than the simple average of 99.53%
- C) 99.53% weighted; higher than the simple average of 99.40%
- D) 99.20% weighted; lower than the simple average of 99.53%

**Correct answer: B**

**Explanation:** Step 1: total users = 10,000 + 30,000 + 10,000 = 50,000. Step 2: weighted sum = (10,000 × 99.8) + (30,000 × 99.2) + (10,000 × 99.6) = 998,000 + 2,976,000 + 996,000 = 4,970,000. Step 3: weighted availability = 4,970,000 ÷ 50,000 = 99.40%. Step 4: simple average = (99.8 + 99.2 + 99.6) ÷ 3 = 298.6 ÷ 3 = 99.53%. The weighted figure is lower because the worst-performing service carries 60% of the users — the simple average hides exactly the users who suffered most. Choosing the weighting basis is not cosmetic: user-weighted figures represent experienced availability, and reporting the flattering simple average instead would misinform every reader. **Service focus** at your level means the group-level number must be built the way users experience it.

**Question 6 (moderate) — Recurrence rate and the case for a fix**

An intermittent fault caused majors in February, April, May, and July (it is now mid-August). Each major costs an estimated £42,000 in lost productivity and response effort. The vendor's permanent fix requires a £60,000 professional services engagement plus a tested 4-hour outage (cost ~£8,000). On current frequency, roughly how long does it take the fix to pay for itself?

- A) About 1 month
- B) About 2.5 months
- C) About 5 months
- D) About 10 months

**Correct answer: B**

**Explanation:** Step 1: recurrence rate — 4 majors in the roughly 6 months from February to July ≈ 0.67 majors per month. Step 2: expected monthly cost = 0.67 × £42,000 ≈ £28,000. Step 3: total fix cost = £60,000 + £8,000 = £68,000. Step 4: payback = £68,000 ÷ £28,000 ≈ 2.4 months — about 2.5 months. The framing lessons: include the outage cost in the fix's price (honesty cuts both ways), and derive the rate from the observed window rather than assuming monthly recurrence. A payback under a quarter turns "expensive vendor engagement" into an easy approval — this is your **Problem management** reporting duty expressed in the only language budget holders reliably hear. It is also worth stating the assumption out loud in any real paper: "on current frequency" — if recurrence is seasonal or worsening, the case is respectively weaker or stronger, and saying so protects your credibility either way.

**Question 7 (moderate) — Percentage change with a shifting base**

Major incident counts: 2023 — 16; 2024 — 12; first half of 2025 — 9. A board paper drafts the claim: "Majors fell 25% in 2024 and are on track to rise 50% in 2025." Check both figures. Which is correct?

- A) Both figures are correct as stated.
- B) The 25% fall is correct; the 2025 claim should be a projected rise of 50% (9 × 2 = 18 vs 12) — both correct, but the second is a projection resting on an assumption of a uniform rate, which the paper should state.
- C) The 25% fall is wrong; it should be 33%.
- D) Both figures are wrong.

**Correct answer: B**

**Explanation:** First figure: change from 16 to 12 = −4; −4 ÷ 16 = −25%. Correct (a fall of 4 on a base of 16 — the base is the earlier year). Second figure: annualising the half-year — 9 × 2 = 18; change from 12 to 18 = +6; 6 ÷ 12 = +50%. Arithmetically correct — but it is a projection, not a measurement: it assumes the second half repeats the first, ignoring seasonality (many estates see change-freeze quiet periods) and any improvement work now landing. B is the answer because it validates both computations and names the hidden assumption. This is precisely the discipline your reporting needs at board level: the difference between "majors rose 50%" and "majors are on track to rise 50% if current rates continue" is the difference between a fact and a forecast — and senior readers will act on whichever you write.

**Question 8 (moderate) — Bridge-call arithmetic: staffing a rota**

A prolonged major requires a 24-hour incident command presence for an estimated 4 more days (96 hours). Command shifts must be no longer than 8 hours, and no individual may work more than one shift in any 24-hour period. You have yourself and three qualified deputies. Can the rota be staffed within the rules, and with how much slack?

- A) No — you are one person short.
- B) Yes — exactly, with zero slack: 12 shifts over 4 days, 3 per day, 4 people covering with one person resting each day.
- C) Yes — 96 hours needs 12 eight-hour shifts; each person may work one shift per day, so 4 people offer 16 person-shifts over 4 days, leaving 4 spare person-shifts of slack.
- D) Cannot be determined.

**Correct answer: C**

**Explanation:** Step 1: shifts needed = 96 ÷ 8 = 12. Step 2: capacity — each of 4 people can work at most 1 shift per 24 hours, so per day capacity = 4 person-shifts against a need of 3; over 4 days, capacity = 16 against a need of 12. Step 3: slack = 16 − 12 = 4 person-shifts — one person fully rested each day, rotating. So the rota is feasible with meaningful slack — option C. B's arithmetic of need is right but its "zero slack" conclusion miscounts capacity. The command relevance: slack is not waste — it is what absorbs sickness, extends the response if day 5 arrives, and lets you schedule yourself off the overnight before the recovery decision that needs your sharpest judgement. Sustainable incident command is a capacity calculation, and leaders who staff rotas to zero slack are planning to fail on the first perturbation — a direct application of **Availability and capacity management** thinking to your own team.

**Question 9 (challenging) — Post-incident analysis: means, medians and the tail**

Last quarter's eight majors had durations (hours): 1.5, 2, 2, 2.5, 3, 3, 4, 14. The 14-hour major involved a failed failover. A draft report says: "Average major duration was 4 hours, well above our 3-hour objective; overall response performance has deteriorated." What do the data actually support?

- A) The report is right: the mean of 4 hours shows general deterioration.
- B) The mean is 4.0 hours, but the median is 2.75 and seven of eight majors met or beat the 3-hour objective (durations at or under 3, with one at 4); the accurate story is strong typical performance plus one severe outlier whose specific cause (failed failover) needs targeted investigation.
- C) The outlier should be deleted from the data and the objective declared met.
- D) The median should be reported as 3.5 hours.

**Correct answer: B**

**Explanation:** Step 1: mean = (1.5 + 2 + 2 + 2.5 + 3 + 3 + 4 + 14) ÷ 8 = 32 ÷ 8 = 4.0 hours. Step 2: median — order the values and average the 4th and 5th: (2.5 + 3) ÷ 2 = 2.75 hours. Step 3: distribution check — six durations ≤ 3, one at 4, one at 14. The mean is dragged a full hour above the median by a single incident, so "general deterioration" misdescribes a distribution where typical performance is comfortably inside the objective. But C is the opposite sin: the outlier is the most important data point in the set — a 14-hour major caused by a failed failover is a continuity-management finding demanding its own investigation (why did the tested runbook fail?), not a row to delete. B reports mean and median together, characterises the tail honestly, and routes the outlier to targeted action. This is post-incident numeracy at command level: summary statistics are for describing the many; investigation is for the one.

**Question 10 (challenging) — Capacity projection with a step change**

A platform's peak-day utilisation: March 58%, April 62%, May 66%, June 70%. In September, a departmental programme will migrate a workload expected to add 12 percentage points of utilisation at once. The platform requires remedial action before utilisation reaches 90%. Assuming the linear trend continues and the migration lands in September as planned, when does utilisation first reach or exceed 90%, and what is the earliest sensible month for remedial action to be complete?

- A) Reaches 90% in December; action can wait until November.
- B) Reaches ~94% in September (82% trend + 12 migration); remedial action must be complete before September — i.e. by August.
- C) Reaches 90% in October; action by September.
- D) The migration is irrelevant to the projection.

**Correct answer: B**

**Explanation:** Step 1: trend = 4 percentage points per month (58 → 62 → 66 → 70). Step 2: project the organic trend — July 74%, August 78%, September 82%. Step 3: add the September step change: 82% + 12 = 94%, breaching the 90% threshold immediately upon migration. Step 4: therefore the remediation must be finished before the migration lands — complete by August, and the capacity work should be scheduled now, since infrastructure lead times consume months. A and C are what the projection looks like if you forget the step change and extrapolate the line alone: organic trend crosses 90% in November-December, which feels comfortably distant and is dangerously wrong. The senior habit: projections must carry known future events, not just historical gradients — your **Availability and capacity management** skill at KPI level, and the difference between preventing a September major and commanding one. Being proactive in searching for potential problems is, often, exactly this piece of arithmetic done in July.

**Question 11 (challenging) — Comparing incident sources with rates, not counts**

Analysis of 60 majors over two years attributes: 24 to failed changes, 18 to hardware failures, 12 to capacity exhaustion, 6 to external/supplier causes. Over the period there were 4,800 changes, 1,200 monitored hardware assets, and 40 capacity-managed platforms. A colleague concludes: "Changes are our biggest problem — they cause 40% of majors." What refinement do the rates suggest?

- A) The colleague is fully right: 40% of majors makes change the top priority on every measure.
- B) Per opportunity, failed changes caused a major at a rate of 0.5% (24 ÷ 4,800), hardware at 1.5% (18 ÷ 1,200), and capacity at 30% (12 ÷ 40): change is the biggest contributor by volume, but capacity-managed platforms have by far the highest per-unit rate of producing majors — both views should steer investment.
- C) Hardware is the biggest problem because assets are numerous.
- D) The rates cannot be computed from the data given.

**Correct answer: B**

**Explanation:** Compute each rate. Changes: 24 ÷ 4,800 = 0.005 = 0.5% of changes end in a major. Hardware: 18 ÷ 1,200 = 0.015 = 1.5% of assets produced a major. Capacity: 12 ÷ 40 = 0.30 = 30% — nearly a third of capacity-managed platforms generated a major over the period. The colleague's 40% (24 ÷ 60) is true as a share of majors and useful for sizing response demand; but for targeting prevention, the per-opportunity rates tell a different story — the change process is actually performing at 99.5% per change, while capacity management is failing on 3 platforms in 10. The mature reading uses both: volume tells you where majors come from; rates tell you which process is sickest per exposure. This dual lens is **Problem management** analytics done properly, and it is exactly the level of numerical argument expected when your findings will redirect another team's budget.

**Question 12 (challenging) — Expected value under uncertainty at the decision gate**

It is 11:30 at the gate from Question 4's world: a fix attempt is underway. If you let it continue, the engineering lead estimates a 60% chance it completes by 13:00 (payment run finishes 16:30, fully clean) and a 40% chance it fails, at which point invoking the 2-hour failover means the run starts at 15:30 and finishes 19:00 — missing the 18:00 statutory deadline. Alternatively, you can abandon the fix now and invoke failover immediately: run starts 14:00, finishes 17:30 — meeting the deadline with certainty but abandoning a fix that is probably about to succeed. Missing the deadline triggers statutory consequences you have been directed to treat as unacceptable. What should you decide, and on what reasoning?

- A) Let the fix continue — 60% is better than even, so it is the rational gamble.
- B) Invoke failover now: the 40% branch leads to an outcome classed as unacceptable, and no probability of a cleaner fix justifies a material chance of an unacceptable outcome when a certain acceptable path exists; the fix can be completed later in a controlled window.
- C) Let the fix continue until 12:30, then decide.
- D) Split resources: half continue the fix, half prepare failover, decide at 13:00.

**Correct answer: B**

**Explanation:** This is expected-value reasoning with a constraint, and the constraint decides it. Compute the branches: continue-fix yields {60%: finish 16:30, ideal} and {40%: finish 19:00, deadline missed}. Failover-now yields {100%: finish 17:30, acceptable}. If all outcomes were merely costs, you might weigh 0.6 × ideal + 0.4 × breach against certain-acceptable. But the stem states the breach is to be treated as unacceptable — a constraint, not a cost — and against a hard constraint, the correct arithmetic is not the average outcome but the probability of violating it: 40% versus 0%. B is the only option that drives that probability to zero while noting the fix is deferred, not lost. A maximises the average and ignores the constraint — the exact error boards remember. C re-times the gate: check its arithmetic — deciding at 12:30 after a failed fix means failover completes 14:30, run finishes… 14:30 + 3.5 = 18:00 exactly, a knife-edge with zero margin for the verification step, so C converts a safe decision into a gamble on perfection. D sounds prudent but does not change the timeline logic if failover genuinely takes 2 hours from invocation (preparation may trim minutes; the stem gives no basis to assume more). The command lesson, transferable to every gate: identify which outcomes are constraints rather than costs, and spend probability protecting the constraint. Your accountability — **Ownership and initiative** at this level — is precisely for that allocation.

### Preparation tips

- **Memorise the availability ladder.** For a 720-hour month: 99% ≈ 7.2 hours, 99.5% ≈ 3.6 hours, 99.9% ≈ 43 minutes, 99.95% ≈ 22 minutes of allowed downtime. Instant conversions power both test answers and live trade-offs.
- **Always compute the bad branch.** For any recovery option, practise timing the failure path, not just the plan. Assessment items and real gates are both decided in the tail.
- **Weight before you average.** Any time you combine figures across services, teams or months, ask "what is the right weighting basis — users, volume, time?" and show it. Unweighted averages of unequal groups are the most common senior-level trap.
- **Name your assumptions in projections.** "If current rates continue", "assuming the migration lands in September" — writing the assumption is both test technique (it identifies the right answer) and board-paper hygiene.
- **Rebuild one real report monthly.** Take an availability or majors report you signed and recompute every figure from raw data. It keeps your arithmetic honest and occasionally finds real errors before someone else does.
- **Practise rates versus counts deliberately.** For any "biggest problem" claim, compute both the share of incidents and the per-opportunity rate. Having both moves ready is what makes your analysis better than the draft in front of you.

### Common pitfalls to avoid

- **Wrong base, right arithmetic.** Percentage change uses the earlier value; shares use the relevant total; rates use the opportunity population. Most wrong options are correct calculations on the wrong denominator.
- **Averaging what should be weighted.** A simple average across unequal services flatters or slanders the estate. If group sizes differ, weight — and say by what.
- **Reading the mean as the typical case.** One 14-hour major drags the mean far above the median. Report both, and treat the outlier as a finding, not noise — and never delete it to pass an objective.
- **Extrapolating through known events.** A linear trend that ignores a scheduled migration, seasonal peak or change freeze is a confident path to a September major. Projections carry known futures.
- **Optimising the average across a hard constraint.** When an outcome is unacceptable rather than expensive, minimise its probability — do not let a favourable expected value smuggle a 40% breach past you.
- **Presenting projections as measurements.** "On track to rise 50%" and "rose 50%" are different claims. Senior readers act on your wording; keep forecasts labelled as forecasts.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment measures how precisely you extract, weigh and act on written information of the kind your role turns on: major incident procedures, continuity plans, severity and escalation criteria, supplier contracts and bulletins, post-incident review extracts, and — distinctively at your level — communications drafted for audiences ranging from engineers to ministers' offices. The core format presents a passage followed by statements to classify as **True** (supported by the passage), **False** (contradicted by it), or **Cannot say** (the passage is silent or insufficient). Senior versions add inference items, argument evaluation, and judgement about which draft communication is fit for its audience and moment.

Typical format: 15 to 25 minutes, 20 to 30 items across several passages, frequently adaptive. The governing discipline is strict textual reasoning: you answer from the passage alone, suspending your own operational knowledge even where the passage differs from how your department works.

For a major incident manager, verbal precision is a command competency with unusually high stakes. Severity criteria, runbook preconditions and contractual support terms are all texts, and during a crisis you apply them at reading speed with no margin for paraphrase drift — the difference between "may" and "must", or between "and" and "or", decides declarations and failovers. Equally weighty is what you write and approve: situation reports repeated verbatim upward, public status messages, and briefings where an ambiguous sentence becomes tomorrow's misleading headline. If you serve as head of service, add supplier obligations and performance clauses to the texts you must read like a lawyer. Employers test verbal reasoning at this level because the role concentrates textual risk: you are frequently the last reader before a text becomes an action, and the last writer before words become the organisation's position.

### How this assessment maps to your role

- **Precise reading of criteria and runbooks** maps to **Incident management** and **Continuity management**: leading investigation and resolution within declared procedures, and managing and testing runbooks, require exact parsing of conditions, exceptions and obligations.
- **True/False/Cannot say discipline** maps to **Ownership and initiative** and **Asset and configuration management**: taking accountability includes never asserting more than the evidence states — in records, reports and reviews alike.
- **Inference and argument evaluation** maps to **Problem management** and **Community collaboration**: post-incident reviews and team retrospectives (including Agile health checks) demand separating what evidence supports from what frustration or advocacy asserts, and adapting feedback so it is effective and lasting.
- **Audience-fit communication judgement** maps to **User focus** and your collaboration with communication managers: championing users, distinguishing user needs from user desires, and approving public messaging all require knowing what a specific audience needs a text to do.
- **Contract and supplier text comprehension** maps to **Change management** and **Service focus**: assessing the impact of changes and getting the best from underlying services often turns on exactly what a supplier document does and does not commit to.

### Practice questions

**Passage 1 (for Questions 1-4):**

"A major incident must be declared by the on-call major incident manager when any severity 1 criterion is met. Severity 1 criteria are: complete loss of a critical service during its service hours; data loss or corruption affecting live citizen data; or a security breach with confirmed unauthorised access. Where an incident meets no severity 1 criterion but the on-call major incident manager judges that coordinated multi-team response is required, they may declare a major incident at their discretion. Once declared, a major incident may be stood down only by the major incident manager currently in command, and only after service is restored or the incident is reclassified. All declarations and stand-downs must be recorded in the major incident log within one hour."

**Question 1 (easy) — True, False, or Cannot say**

Statement: "A complete loss of a critical service outside its service hours requires a severity 1 declaration."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** The criterion is "complete loss of a critical service during its service hours". An outage outside service hours does not meet that criterion as written, so declaration is not required by it — the statement asserts a requirement the passage's wording excludes. Note the precision: the passage does not forbid a discretionary declaration (the discretion clause might still apply), but the statement claims a severity 1 requirement, which the qualifying phrase "during its service hours" defeats. Reading temporal qualifiers at full weight is exactly how you avoid declaring — or failing to declare — on a misremembered criterion at 03:00.

**Question 2 (easy) — True, False, or Cannot say**

Statement: "An incident that meets no severity 1 criterion can still become a declared major incident."

- A) True
- B) False
- C) Cannot say

**Correct answer: A**

**Explanation:** The discretion clause states it directly: where no severity 1 criterion is met but the on-call major incident manager judges that coordinated multi-team response is required, "they may declare a major incident at their discretion". The statement is supported verbatim. The design logic is worth internalising even though the test only asks for the classification: criteria-based triggers catch the predictable catastrophes, and the discretion clause exists because real crises do not always read the criteria first. Knowing precisely where your discretion begins — and that it is a "may", not a "must" — is part of commanding within the procedure rather than around it.

**Question 3 (moderate) — True, False, or Cannot say**

Statement: "A deputy who takes over command of a major incident may stand it down once service is restored."

- A) True
- B) False
- C) Cannot say

**Correct answer: A**

**Explanation:** Track the passage's exact words: stand-down is reserved to "the major incident manager currently in command". A deputy who has taken over command is, by that description, the manager currently in command — the passage allocates the power to the office of current command, not to the individual who declared. With service restored, the stated condition is also met. So the statement is supported: True. The tempting wrong answer is Cannot say, from doubting whether deputies count — but the passage's own phrase resolves it; the classification turns on matching the statement to the rule's actual terms rather than to an assumed org chart. In live handovers this is not pedantry: who currently holds command authority, and what powers transfer with it, must be answerable from the procedure's text in one read.

**Question 4 (moderate) — Inference**

Which is the best inference about the design of this procedure?

- A) It aims to make declaration fast and low-friction while keeping stand-down controlled and accountable.
- B) It assumes security breaches are the most common major incidents.
- C) It exists mainly to generate log entries for audit.
- D) It distrusts on-call managers, which is why discretion is limited.

**Correct answer: A**

**Explanation:** Look at the asymmetry the rules create: declaration has multiple automatic triggers plus personal discretion — many doors in; stand-down has a single authorised actor and explicit preconditions — one guarded door out. That asymmetry embodies a principle: over-declaring is recoverable, premature stand-down is not, so the procedure biases toward response and against relaxation. A captures this. B infers frequency from mere listing order. C mistakes the recording clause — an accountability mechanism — for the purpose. D reads the discretion clause backwards: granting personal discretion to declare is an expression of trust, not its absence. Inference items at this level reward reading a procedure the way its author thought: asking what failure mode each clause is built to prevent.

**Passage 2 (for Questions 5-7):**

"Under the support contract, the supplier will respond to severity 1 tickets within 30 minutes at any hour, and will provide continuous effort until resolution. Severity assignment is made by the customer at ticket creation and may be challenged by the supplier only after resolution. On-site attendance, where required, will be provided within four hours for data-centre locations and within eight hours for other sites. The contract excludes faults arising from customer modifications not approved by the supplier. Service credits accrue for each missed response target in a quarter, capped at 10% of the quarterly support charge."

**Question 5 (easy) — True, False, or Cannot say**

Statement: "The supplier may downgrade a ticket's severity while the incident is still open."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** The passage grants severity assignment to the customer at creation and permits the supplier to challenge it "only after resolution". Challenging — let alone changing — severity mid-incident is therefore excluded by the word "only". The statement contradicts the text: False. Operationally, this is a clause worth knowing cold during a live major: a supplier voice on the bridge suggesting "this is really a severity 2" changes nothing about their contractual obligation to continuous effort, and you can say so with the contract's own words — the quiet power of precise reading in **Service focus** terms: getting the best from underlying services includes their contracts.

**Question 6 (moderate) — True, False, or Cannot say**

Statement: "If a severity 1 fault at a regional office requires on-site attendance, the supplier must attend within four hours."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** The four-hour commitment applies to "data-centre locations"; other sites — which a regional office is — carry an eight-hour commitment. The statement assigns the data-centre timescale to a non-data-centre site, contradicting the passage: False. The error mechanism is transposing the favourable number onto the sympathetic case — precisely how contract terms get misquoted on bridge calls and in escalation emails, usually in good faith, always at a cost: an escalation built on a misread entitlement collapses when the supplier corrects it, and takes your credibility with it. When response commitments are tiered, the tier is part of the fact.

**Question 7 (challenging) — True, False, or Cannot say**

Statement: "A fault caused by a customer modification will not accrue service credits, even if the supplier responds late."

- A) True
- B) False
- C) Cannot say

**Correct answer: C**

**Explanation:** Two clauses are in play and the passage does not connect them. The exclusion clause removes "faults arising from customer modifications not approved by the supplier" from contract coverage — but the statement's phrase "a customer modification" does not tell us whether this one was unapproved; approved modifications are outside the exclusion. Moreover, even for an excluded fault, the passage does not state what happens to response-target credits on a ticket the supplier nonetheless handled late — coverage exclusion and credit accrual are related but the text never joins them. Since the statement's conclusion depends on both an unstated fact (approval status) and an unstated rule (how exclusions interact with credits), the disciplined verdict is Cannot say. This is the hardest and most valuable verbal skill for a senior reader: noticing when a confident-sounding claim quietly bridges a gap the document leaves open — the gaps are where disputes, and post-incident arguments, live.

**Passage 3 (for Questions 8-9):**

"Post-incident review of the 14 March outage found that the secondary site's database had been running an incompatible minor version for six weeks before the failover attempt, causing the failover to fail. The version drift was introduced by an emergency patch applied to the primary site only. Monitoring compared primary and secondary availability but not version parity. The review recommends automated version-parity checking, inclusion of failover execution in quarterly continuity tests, and explicit version-parity verification as a precondition in the failover runbook. The review notes that the incident's duration would likely have been under one hour, rather than nine, had failover succeeded."

**Question 8 (easy) — True, False, or Cannot say**

Statement: "The failover failed because the emergency patch was applied to the secondary site."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** The passage says the drift arose from a patch "applied to the primary site only" — the secondary's problem was not receiving the patch, leaving it on an incompatible version. The statement inverts the mechanism: False. This inversion is worth a moment's reflection beyond the test: it is exactly the kind of subtle misretelling that hardens into folklore after an incident ("the patch broke the secondary") and then misdirects the fix (patch controls on the secondary, rather than parity enforcement between sites). Precision in the review's causal chain is what makes its recommendations aim at the right target — and repeating that chain accurately is part of your reporting duty into **Problem management**.

**Question 9 (challenging) — True, False, or Cannot say**

Statement: "Quarterly continuity tests were being performed before the incident, but did not include executing failover."

- A) True
- B) False
- C) Cannot say

**Correct answer: C**

**Explanation:** The review recommends "inclusion of failover execution in quarterly continuity tests". Tempting inference: quarterly tests existed but lacked failover execution. But examine what the sentence actually commits to — a recommendation phrased this way is compatible with quarterly tests existing without failover execution, and also with quarterly tests not currently existing at all (the recommendation would then establish both the cadence and the content). The passage never states that quarterly tests were already being performed. Since the statement asserts a specific past practice the text does not confirm, the verdict is Cannot say. This is a precision distinction — between what a recommendation implies about the present and what it merely proposes for the future — and it matters in your **Continuity management** world: reading "we recommend testing X quarterly" as evidence that a testing regime already exists is how assurance gaps survive reviews.

**Question 10 (moderate) — Audience-fit communication judgement**

Ninety minutes into a major outage of a citizen-facing service, the press office asks for a public status message. Which draft is most fit for purpose?

- A) "We are aware some users are experiencing intermittent service degradation and are working to remediate the root cause via our major incident process."
- B) "The [service name] is currently unavailable. We are working to restore it and will post an update by 15:00. If your application deadline is today, call 0800 XXX XXXX — deadlines affected by this outage will not disadvantage you."
- C) "Due to a database platform failure during a failover sequence, engineers are executing recovery runbook 7B. ETA uncertain."
- D) "We apologise unreservedly for this unacceptable failure and will publish a full investigation."

**Correct answer: B**

**Explanation:** A public status message during an outage has one job: tell affected citizens what is true, what to do, and when they will hear more. B does all three in plain language — names the plain fact ("currently unavailable" — honest, unlike A's minimising "some users… intermittent degradation"), commits to an update time, and, crucially, addresses the highest-stakes user need: people facing deadlines, with both a route (phone) and a reassurance that removes panic. That reassurance line is **User focus** doing real work — it addresses the need behind the fear, exactly the user-need-versus-desire distinction your framework names. A is fog: hedged scope and process vocabulary that informs no one. C is an engineering update mispublished to citizens — accurate, useless, and mildly alarming. D performs contrition before facts are known and answers none of the reader's questions. In assessment and in the press office alike: the best draft is the one whose reader finishes it knowing what to do. Your partnership with communication managers works precisely when you supply that content.

**Question 11 (moderate) — Evaluating an argument in a post-incident review**

In a heated review, an infrastructure lead argues: "The outage lasted nine hours only because the service desk logged it as a priority 2 for the first forty minutes. If tickets were always logged as priority 1 by default, majors would be caught immediately. We should make priority 1 the default for all infrastructure tickets." Which is the strongest evaluation of this argument?

- A) Agree: earlier detection would have helped, so the default change follows.
- B) The premise about the forty-minute delay may be true and worth fixing, but the remedy does not follow: defaulting all tickets to priority 1 destroys the prioritisation signal itself, burying real majors among false ones; the targeted fix is better triage criteria or automated detection for major-pattern symptoms.
- C) Reject everything: the misclassification clearly had no effect on duration.
- D) The argument is invalid because infrastructure leads cannot comment on service desk process.

**Correct answer: B**

**Explanation:** Separate the argument's layers. Its factual premise (forty minutes at the wrong priority) is granted; its causal claim (this extended the outage) is plausible though "only because" overstates — nine hours had other causes, as any failed-failover review shows; and its remedy commits the classic alarm fallacy: if everything is priority 1, nothing is, and the signal the lead wants amplified is destroyed by amplifying it everywhere. B grants what deserves granting, names the overstatement, and redirects to remedies that actually target the failure mode (triage criteria, automated detection). C mirrors the original error in reverse — dismissing a real finding to win the argument. D attacks standing rather than substance, the move most corrosive to review culture. At your level, this evaluation skill is live in every lessons-learned session you chair: your **Community collaboration** skill of adapting feedback so it is effective and lasting means extracting the valid 40 minutes from the invalid remedy — and saying both aloud.

**Question 12 (challenging) — Precision in an upward brief**

You must brief a director's office in writing, mid-incident. Facts you hold: service down since 09:12; cause not yet confirmed, storage failure suspected; failover declined at 10:00 because replication currency could not be confirmed and the service owner declined the data-loss risk; vendor engaged 09:40, on-site ETA 13:00; restoration estimate "by 17:00" from the infrastructure lead, described by them as "reasonable confidence, not a commitment". Which sentence for the brief's summary line is most accurate and most useful?

- A) "Service will be restored by 17:00."
- B) "Restoration is currently estimated by 17:00 (assessed as reasonable confidence, not yet a commitment); cause suspected but unconfirmed; failover was considered and declined at 10:00 to avoid uncontrolled data loss; vendor on site from 13:00."
- C) "Restoration time cannot be estimated, as the cause is unconfirmed."
- D) "The incident is under control and further updates will follow."

**Correct answer: B**

**Explanation:** An upward brief must transmit the decision-relevant state without upgrading or downgrading any fact's certainty. B preserves every epistemic label the facts carry: the estimate stays an estimate with its stated confidence; the suspected cause stays suspected; the failover decision is reported with its reason — pre-empting the director's inevitable "why not failover?" with the honest answer that it was a considered risk decision, not an oversight; and the vendor milestone gives the next observable event. A upgrades an estimate into a commitment — the single most damaging transformation in upward reporting, because the director will repeat it, and at 17:05 the incident acquires a second front. C downgrades honest uncertainty into refusal, discarding a usable estimate the room needs for planning. D is reassurance without content — it borrows trust and repays nothing. The verbal skill being tested is calibrated language: reporting not just facts but each fact's degree of certainty, unchanged. That calibration is **Ownership and initiative** in written form: accountability includes accountability for what your sentences let others believe.

### Preparation tips

- **Drill the three verdicts until reflexive.** True = supported; False = contradicted; Cannot say = the text is silent or incomplete. At senior level, most lost marks are Cannot-say items answered from experience — the better you know operations, the more deliberately you must suspend that knowledge.
- **Parse structure before content.** For any criteria, runbook or contract passage, mark the operators — and/or, only, unless, may/must, "during", "after resolution" — before reading the statements. The questions are built on the operators.
- **Practise on your own procedures and contracts.** Take a page of your major incident procedure or a supplier schedule and write five statements: two true, two false, one undecidable. This doubles as an audit — ambiguities you find are ambiguities to fix.
- **Rehearse calibrated language.** Rewrite three recent status updates, labelling every claim as fact, estimate or assumption. The habit transfers directly to both test items and upward briefs.
- **Read recommendations forensically.** For any review extract, ask: what does this recommendation prove about the present, and what does it merely propose? Question 9's trap is everywhere in real reviews.
- **Time-box and flag.** Thirty to forty-five seconds per statement; flag and return rather than siege. Verbal sections reward steady throughput over heroic sieges of single items.

### Common pitfalls to avoid

- **Answering from the profession instead of the passage.** Where the passage's procedure differs from your department's, the passage governs. Every senior candidate knows this rule; the discipline is applying it at speed.
- **Confusing False with Cannot say.** False needs contradiction. A claim the passage merely fails to support — however implausible operationally — is Cannot say.
- **Transposing tiered numbers.** Four hours for data centres, eight for other sites; thirty minutes for severity 1. Tiered commitments are misquoted by attaching the best tier to the case at hand. The tier is part of the fact.
- **Reading recommendations as descriptions.** "We recommend quarterly testing" does not establish that testing — or its absence — currently exists in any particular form.
- **Upgrading certainty in communications.** Estimates become commitments, suspicions become causes, one misreported step at a time. In clear-writing items, prefer the option that preserves every fact's epistemic label.
- **Choosing the most polished-sounding draft.** Fluency is not fitness. The right communication is the one that serves its specific audience's next decision — citizens' actions, a director's planning — not the one with the smoothest vocabulary.

## Workplace job-specific situational judgement assessment

### About this assessment

A situational judgement test (SJT) presents realistic workplace scenarios and asks you to judge the effectiveness of possible responses. For senior operational roles there is rarely a provably correct answer; responses are scored against the pooled judgement of experienced practitioners and the organisation's professional behaviours. Formats include most-effective, most-and-least-effective, full ranking, and independent effectiveness ratings per option.

Typical format: 12 to 25 scenarios in 25 to 40 minutes. At major incident manager level, the scenarios concentrate where your role concentrates: command decisions under uncertainty, delegation and span of control, honesty under senior scrutiny, managing exhausted teams and difficult team dynamics, handling suppliers and press attention, resisting pressure to cut corners, and the trade-offs between restoring fast, restoring safely, and telling the truth about both. Employers use SJTs at this level because technical mastery and even cognitive brilliance do not predict who will hold a calm bridge, delegate without abandoning, brief upward without spin, stand a major down at the right moment, and leave the team stronger after the crisis than before it.

The behaviours being assessed align with the values of the Government Digital and Data profession, weighted for seniority: user focus (outcomes for citizens and staff, not optics), collaboration (across workplace services, infrastructure, applications, communications and suppliers), ownership (accountability that does not migrate downward when things go wrong), sound escalation and de-escalation (upward, sideways and to problem management, with honest information), and inclusion (a command style that gets the quietest expert's knowledge into the decision). As you judge each option, ask the command version of the standard question: what happens to the users, the team, the truth, and the next incident if I do this?

### How this assessment maps to your role

- **Command and delegation dilemmas** map to **Incident management** and **Community collaboration**: leading the investigation and resolution of incidents through others — briefing, delegating, converging a bridge call, and correcting team dynamics in real time.
- **Accountability dilemmas** map to **Ownership and initiative**: taking accountability for issues that occur, including in front of directors and reviews, and being proactive about potential problems even when raising them is unwelcome.
- **Risk and shortcut dilemmas** map to **Change management** and **Continuity management**: assessing the impact of emergency changes honestly, respecting runbook preconditions, and refusing pressure to gamble with data or safety margins.
- **Handover and reporting dilemmas** map to **Problem management** and your defined duty to report issues into problem management: what you pass on, how honestly, and whether prevention actually happens.
- **Communication dilemmas** map to **User focus** and your collaboration with communication managers: championing users when their interests conflict with institutional comfort, and distinguishing user needs from stakeholder desires.
- **Wellbeing and sustainability dilemmas** map to **Community collaboration** and **Availability and capacity management**: identifying issues through team health checks, adapting feedback so it lasts, and managing your team's capacity like the critical component it is.

### Practice questions

**Question 1 (easy) — The pressure to stand down early**

Six hours into a declared major, service is restored on a workaround; root cause is unknown and the fix that failed earlier has not been explained. A director messages: "Service is up — stand the major down so we can tell the Permanent Secretary's office it's over." What is the most effective response?

- A) Stand the major down as asked; it can always be re-declared if the service fails again.
- B) Keep the major open, and reply explaining that service is restored on an unexplained workaround with recurrence risk; propose language for the Permanent Secretary's office that is both accurate and reassuring: "service restored, monitoring closely, root cause under investigation."
- C) Stand it down but privately tell the team to keep working as if it were still open.
- D) Refuse without explanation; stand-down is your call, not the director's.

**Correct answer: B**

**Explanation:** The stand-down decision is yours in most frameworks precisely so that it tracks operational reality rather than reporting convenience — and the operational reality is an unexplained fault held at bay by a workaround. B keeps the response posture matched to the risk and solves the director's actual problem, which is legitimate: they need something true and calm to say upward, and you supply it. That is what upward collaboration looks like — meeting the need behind the request rather than the request itself. A dissolves the response structure while the hazard persists; re-declaration after a recurrence costs the spin-up time majors exist to eliminate, plus credibility. C is the worst of both: the official record now lies, the team gets ambiguous authority, and the director unknowingly misinforms upward — a trust time-bomb. D may be procedurally correct and is relationally ruinous; command authority exercised without explanation spends influence you will need. Senior SJTs repeatedly test this exact move: hold the substantive line, and do the stakeholder's legitimate job for them while holding it.

**Question 2 (easy) — Delegating under load**

Ninety minutes into a two-service major, you are personally deep in the database diagnostics — you know this platform better than anyone on the call — while the bridge drifts: two teams are duplicating work, the communications manager has had no update for forty minutes, and the incident log has fallen behind. What is the most effective correction?

- A) Keep leading the diagnostics — cause-finding is the critical path — and catch the coordination up afterwards.
- B) Hand the diagnostics to the database lead with a clear brief, and resume command: reset the bridge's lines of inquiry, give communications an update and a cadence, and appoint a scribe for the log.
- C) Do both by alternating: five minutes of diagnostics, five of coordination.
- D) Ask the communications manager to run the bridge while you continue the diagnostics.

**Correct answer: B**

**Explanation:** The scenario is a role-integrity test. Command is a full-time function: while you were being the best database engineer on the call, the actual command outputs — deconflicted workstreams, informed communications, a current log — all failed, and those failures compound (duplicated work wastes specialists; silent communications invite senior interference; a stale log corrupts the eventual review). B restores each function to its right owner: the database lead takes the technical thread you were hoarding — with a proper brief, so nothing is lost — and you take back the only role no one else on the call can hold. A doubles down on the inversion; your expertise is real, which is exactly why it is seductive and exactly why the delegation must be deliberate. C gives both functions the attention of neither. D hands command to the person whose own function is currently starved of what only command can supply. The senior principle SJTs reward: do the job only you can do, and delegate the job you would love to do — **Community collaboration** as command discipline.

**Question 3 (moderate) — The exhausted specialist**

At hour ten of a major, your lead applications specialist — the only person who understands the failing component — is making uncharacteristic mistakes: she has twice given the wrong config path and just snapped at a colleague. A candidate fix is ready to apply; she insists she is "fine to see it through". What is the most effective action?

- A) Let her apply the fix — she knows the component best, and the fix is ready.
- B) Stand her down for a mandatory rest now, and pause the fix until she returns.
- C) Have her brief a second engineer to execute the fix while she supervises from rest of the keyboard — reviewing, not typing — then send her off shift with a defined return time once the fix lands.
- D) Replace her with an engineer from another team and proceed at full speed.

**Correct answer: C**

**Explanation:** Two facts are simultaneously true: her knowledge is currently irreplaceable, and her execution is demonstrably degraded — two wrong paths and visible irritability are error signatures, not personality. C separates what fatigue destroys (fine motor accuracy, attention) from what it degrades more slowly (recognition, judgement): a fresh engineer's hands, her supervising eyes, and a structured brief that also — not incidentally — transfers some of the knowledge that made her a single point of failure. Then rest, with a defined return, because hour ten is rarely the end. A accepts a degraded operator executing a critical change on a wounded service — the highest-risk moment of the entire incident entrusted to the shakiest hands available. B protects her and abandons the fix unnecessarily; total pause is the right call only when no safe execution path exists, and one does. D discards the only component knowledge in the building at the moment of maximum need. This is **Availability and capacity management** applied to humans — your team is a service component with a utilisation limit — and the fatigue-management behaviour senior SJTs specifically probe: neither hero-worship nor benching, but redesigning the task around the impairment.

**Question 4 (moderate) — Honest uncertainty at the director's briefing**

Forty minutes in, you join a hastily convened directors' call. The facts: cause unknown, two hypotheses under investigation, restoration estimate not yet possible. A director presses: "Just give me a time. Worst case. Anything." What is the most effective response?

- A) Give a generous worst case — "no later than 20:00" — so expectations are safely anchored.
- B) Say an estimate now would be a guess; explain what is being investigated, commit to a first real estimate by a stated time ("by 12:30, when the storage diagnostics complete"), and state the decision point that estimate will inform.
- C) Repeat "no estimate is possible" until the director stops asking.
- D) Give the engineering team's most optimistic figure, flagged as optimistic.

**Correct answer: B**

**Explanation:** The director's demand is a need wearing the wrong request: they must plan — staff redeployment, upward briefings, possibly public lines — and planning needs a time. B refuses to fabricate the number while fully serving the need: a bounded wait ("estimate by 12:30"), a reason the wait is real (diagnostics in progress), and the shape of what the estimate will unlock. That is calibrated honesty with a service wrapper. A feels prudent and is a trap twice over: an invented worst case anchors the entire organisation's planning on fiction, and when 20:00 proves wrong in either direction, your numbers are discounted for the rest of the incident — you have spent credibility to buy forty minutes of quiet. D launders a best case through a caveat that will be stripped off at the first retelling; optimistic figures travel upward faster than their flags. C is honest and useless — stonewalling without an alternative simply teaches directors to go around you. The scored behaviour is the senior version of **Ownership and initiative**: owning not just the incident but what the organisation is allowed to believe about it, minute by minute.

**Question 5 (moderate) — The supplier on the bridge**

Three hours into a major involving a supplier's storage platform, the supplier's engineer on the bridge is capable but their account manager keeps interjecting: hinting the fault may be "environmental, not product", asking for the incident's severity to be revisited, and requesting that all findings be routed through them before being logged. What is the most effective handling?

- A) Remove the supplier from the bridge entirely and communicate by email.
- B) Keep the engineer on the technical thread; move the account manager to a separate commercial track with a named owner and agreed update times; log all findings in your incident record as normal, and note the contract governs severity.
- C) Comply with the routing request to keep the supplier cooperative — you need their engineer.
- D) Challenge the account manager's motives openly on the bridge so the record shows who obstructed.

**Correct answer: B**

**Explanation:** Untangle the two supplier presences: an engineer contributing to resolution, and an account manager conducting early liability defence — the "environmental" hints, the severity revisiting, the request to filter findings are all positioning for a future commercial conversation. B keeps what serves the incident and relocates what does not: the commercial track is not banished but given its proper venue, owner and cadence (that is supplier collaboration, honestly structured), while the evidence chain — your incident log — remains yours and complete, which both the restoration and any later dispute require. A punishes the useful engineer for the account manager's behaviour and slows diagnosis. C trades the integrity of your incident record for cooperation you are contractually entitled to anyway — and filtered findings will be curated findings. D wins a moment and poisons a partnership, on the record, while the service is still down. **Service focus** at your level explicitly includes getting the best out of underlying services — and their vendors — which sometimes means protecting the technical relationship from the commercial one in real time.

**Question 6 (moderate) — The uncomfortable pattern you spotted first**

Reviewing dashboards on a quiet Friday, you notice the authentication platform's error rate has doubled each week for three weeks — still tiny in absolute terms, but the doubling is regular, and that platform fronts every critical service. The platform team's lead, senior to you in tenure and prickly about turf, closed a similar concern last month as "monitoring noise". What is the most effective action?

- A) Log it informally and wait — at the current rate you have another two or three weeks before user impact, and the platform is not yours.
- B) Take the data to the platform lead directly: the specific trend, the doubling period, the projected threshold-crossing date — and jointly agree an investigation before it reaches user impact, raising a problem record so the pattern is tracked whatever the outcome of the conversation.
- C) Escalate immediately over the platform lead's head to their head of function, attaching the previous "noise" dismissal.
- D) Declare a pre-emptive major incident to force attention onto the platform.

**Correct answer: B**

**Explanation:** This scenario tests whether "be proactive in searching for potential problems" survives contact with organisational friction. The data pattern — regular doubling on a universal dependency — is precisely the kind that turns into a multi-service major on the week everyone was almost ready; your **Ownership and initiative** and **Problem management** skills both point at acting now, and acting now means engaging, not filing. B does it with the two features that make proactivity effective rather than merely righteous: evidence in the platform team's own terms (trend, period, projected crossing), and a formal problem record so the concern has institutional memory — if the conversation goes nowhere, the record is the legitimate, non-personal escalation path. A knowingly spends the entire safety margin as a courtesy to turf. C makes the first move an ambush, converting a data conversation into a status conflict and guaranteeing the next anomaly you spot gets defended against rather than investigated. D abuses the major incident mechanism — it commands attention exactly once at the cost of every future declaration's credibility. Senior SJTs score this pattern consistently: direct, evidenced, respectful engagement, backed by process, beating both patience and force.

**Question 7 (challenging) — The emergency change with a missing step**

At 02:00, restoring a payments-critical service requires an emergency change. The engineer's plan is sound but skips the pre-change configuration backup "to save twenty minutes" — the service has been down four hours and everyone wants it back. The change modifies the same subsystem whose state is not fully understood. What is the most effective decision?

- A) Approve the plan as offered — twenty minutes matters after a four-hour outage.
- B) Require the backup step, framing it on the bridge in decision terms: twenty minutes buys a guaranteed rollback path on a subsystem we do not fully understand; without it, a failed change converts a four-hour outage into an unbounded one.
- C) Reject the emergency change entirely and wait for the morning change board.
- D) Approve skipping the backup but have the engineer document that the risk was accepted.

**Correct answer: B**

**Explanation:** Compute the asymmetry the fatigue on the bridge is hiding: the backup costs twenty known minutes; its absence costs nothing if the change succeeds and potentially everything if it fails — on a subsystem whose current state is explicitly not understood, which is precisely the condition under which changes fail surprisingly and rollbacks get improvised at 03:00 from memory. B pays the small premium and — the senior detail — narrates the reasoning aloud, which keeps the exhausted bridge aligned and teaches the decision pattern for next time. A is the tired room's answer; four hours of sunk outage does not change the forward-looking arithmetic. C overcorrects into paralysis: the emergency change process exists exactly for 02:00 payments-critical restorations, and deferring to morning abandons users to procedure. D is the most seductive wrong answer on the card: documentation redistributes blame, not risk — the outage that follows a failed unrollbackable change is identical with or without the signed note. Your **Change management** skill at this level is analysing and assessing impact for real, and **Continuity management** is why the rollback path is sacred: the strongest answer buys insurance with minutes and says why in one sentence.

**Question 8 (challenging) — Most and least effective: the morning after declaration**

A major was declared at 06:40 for a citizen-facing service; it is now 08:30, investigation is progressing, and the daily operations review — attended by all service leads — begins at 09:00. Consider four actions for the 09:00 slot:

1. Send a deputy to the operations review with a two-minute prepared summary and authority to answer scope questions, while you remain in command.
2. Attend the review yourself to show senior presence, leaving the bridge to run itself for forty minutes.
3. Skip any presence at the review; the major incident process makes the review irrelevant today.
4. Have the incident log emailed to all attendees in lieu of any spoken update.

Which pairing is correct?

- A) Most effective: 1; least effective: 2
- B) Most effective: 2; least effective: 3
- C) Most effective: 1; least effective: 3
- D) Most effective: 4; least effective: 2

**Correct answer: C**

**Explanation:** Action 1 is clearly strongest: the organisation's coordination forum gets an accurate, bounded briefing from someone empowered to answer, and command remains continuous — delegation with a brief and authority, the same pattern as Question 2. The least-effective judgement is the discriminating step. Action 2 costs forty minutes of command during active investigation — bad, but it delivers real information to the forum; its failure mode is absence from the bridge. Action 4 is lazy and noisy (a raw log dumped on twenty leads informs almost no one), but it transmits something. Action 3 alone delivers nothing and severs the connection deliberately: every service lead plans their day around stale rumour, dependent services make uninformed choices, and the major incident process — which exists to improve the organisation's coordination — is used as a reason to abandon it. Providing nothing beats providing badly only in the rare case where the something is actively false; here the log is merely unhelpful, while silence is a coordination vacuum. So most: 1, least: 3 — option C. The scored senior habit: majors do not suspend the organisation's other rhythms; command includes feeding them deliberately at low cost.

**Question 9 (challenging) — When your own decision was the mistake**

The post-incident review of last week's nine-hour major is being drafted. Reconstructing the timeline, you realise that your own 10:15 decision — holding the failover for ninety minutes while a fix was attempted — was based on your misreading of the replication dashboard: replication was current, failover was safe, and the incident could have ended seven hours earlier. Only you have noticed; the draft attributes the delay to "tooling ambiguity". What is the most effective action?

- A) Let the draft stand — the dashboard genuinely is ambiguous, the outcome cannot be changed, and command confidence matters for future incidents.
- B) Correct the record: state that you misread the dashboard, that failover was in fact safe at 10:15, and pair it with the systemic finding — the dashboard's presentation invited the misreading — so the review yields both an honest timeline and a fix that protects the next commander.
- C) Quietly ask the review author to soften the section further so no decision is singled out.
- D) Add the correction but attribute the misreading to "the bridge team's collective assessment".

**Correct answer: B**

**Explanation:** This is the purest accountability item on the card, and the option design is instructive. B contains two inseparable halves: the personal correction (I misread; failover was safe) and the systemic finding (the display invited the misreading) — and the pairing is not self-protection, it is what makes the review true and useful: reviews that name only systems produce fixes nobody urgently owns, and reviews that name only people produce fear instead of fixes. A hides behind a half-truth — the ambiguity is real, which is exactly why it deserves to be in the record attached to its consequence, not deployed as camouflage; and the "command confidence" argument is precisely backwards, because teams extend most confidence to commanders whose accounts survive checking. C converts an omission into a conspiracy with a witness who now knows how you handle your own errors — and will remember it when handling theirs. D is A wearing B's clothes: a correction that redistributes your error to your team is worse than silence, because it teaches everyone on that bridge what accountability upward costs them personally. **Ownership and initiative** — take accountability for issues that occur — is tested nowhere more directly than when you are the issue, and senior SJT keys are ruthless about it: the top answer is always the one where the error's owner and the system's flaw are both named, by you, first.

**Question 10 (challenging) — The quiet dissent on the bridge**

Ninety minutes in, the bridge has converged confidently on a fix: restart the application cluster, expected outage extension fifteen minutes. As you are about to authorise, you notice a junior infrastructure engineer — invited for local knowledge, silent all call — type a few words into the chat and delete them unsent (the typing indicator gave it away). The senior engineers are unanimous and time is pressing. What is the most effective action?

- A) Proceed — unanimous senior judgement should not be delayed for an unsent message that may have been nothing.
- B) Pause authorisation for one minute and invite the engineer directly and safely: "Before I authorise — Sam, you know this cluster locally; anything we should check first?" Then weigh whatever surfaces on its merits.
- C) Note the hesitation and ask the engineer about it privately after the restart completes.
- D) Ask the whole bridge "any objections?" and proceed on the ensuing silence.

**Correct answer: B**

**Explanation:** The deleted message is data: someone with uniquely local knowledge composed a concern and then judged the bridge unsafe for it — juniority, unanimity and time pressure forming exactly the silence machine that incident histories blame afterwards. B spends sixty seconds converting that silence into information, and the phrasing does the real work: named invitation (broadcast questions do not reach the person who already self-censored), credential attached ("you know this cluster locally" — reframing speaking as contributing expertise, not raising objection), and before the irreversible action. If the concern is trivial, you lose a minute; if it is "the cluster's restart script fails when node 3 is primary" — the kind of thing only local knowledge holds — you have prevented the fifteen-minute outage becoming the second major of the day. A prices the minute above the information, which inverts their actual values. C collects the lesson after the exam. D is the ritual that produced the silence being asked to cure it — "any objections?" into unanimity-plus-hierarchy is how bridges launder consensus. This is **Community collaboration** at command grade — using your position to identify issues in team dynamics and rectify them in the moment — and it doubles as **User focus**: the users' interests were in that unsent message.

**Question 11 (challenging) — Handover into problem management that actually lands**

The major is resolved on a permanent-looking fix, but investigation revealed three systemic issues: the failover runbook has an untested branch, monitoring missed the failure's leading indicator for forty minutes, and an undocumented dependency links this service to two others. The team is exhausted; the natural move is to close the incident and "capture it all in the review". Last quarter, two similar reviews produced recommendations that were never actioned. What is the most effective closure approach?

- A) Close the incident and write a thorough review document, trusting the review process despite its recent record.
- B) Keep the major incident open until all three systemic issues are fixed.
- C) Close the incident, but before stand-down convert each systemic issue into a specific problem record with a named owner and a review date, and use your working relationship with problem management to agree priority — noting the two unactioned reviews as evidence for why this time the records go in with owners attached.
- D) Fix the three issues yourself over the coming weeks, since handoffs keep failing.

**Correct answer: C**

**Explanation:** The scenario's sting is the base rate: this organisation's review-to-action pipeline demonstrably leaks, so the naive process answer (A) has a known failure probability you were just told about — trusting a process against its own recent evidence is not diligence, it is ritual. C re-engineers the handoff at the moment of maximum leverage: before stand-down, while the incident's authority still commands attention, each issue becomes a problem record — the artefact with institutional memory — carrying the two properties unactioned recommendations lack: a named owner and a date. Citing the two failed reviews is not blame; it is exactly the pattern-evidence your **Problem management** skill exists to use, applied to the meta-process. B misuses the major incident structure as a project tracker, burning an exhausted team's on-call posture for weeks of systemic work — majors are for response, problems are for prevention, and your role description says precisely this: manage the crisis, report issues to problem management. D is the heroic anti-pattern with a schedule: three systemic fixes across runbooks, monitoring and architecture are not one person's evening work, and every one you absorb personally confirms the broken pipeline as acceptable. The senior behaviour being scored: closing an incident well means engineering its lessons' survival, not just recording them.

**Question 12 (challenging) — Ranking under public pressure**

Mid-afternoon during a visible outage of a citizen-facing service, four demands arrive within five minutes: (1) the press office needs a quote approved in ten minutes for a journalist's deadline; (2) the restoration workstream needs your go/no-go on a recovery step that is safe but will visibly extend the outage banner by thirty minutes; (3) a minister's private office asks for a call-back "this hour" for a briefing; (4) the service desk reports call volumes have tripled and asks permission to activate the overflow script. Rank the order in which you address them.

- A) 3, 1, 2, 4 — political first, media second, technical third, operational last
- B) 2, 4, 1, 3 — restoration decision first (it is on the critical path and everything else describes it), overflow script second (two minutes, immediately stops user-facing harm), press quote third (deadline inside ten minutes, and now describable accurately), minister's call fourth (inside the hour, and now brief-able with the decisions made)
- C) 1, 3, 2, 4 — external audiences first, in deadline order
- D) 4, 2, 1, 3 — operational calm first, then decisions, then audiences

**Correct answer: B**

**Explanation:** Rank by dependency and deadline, not by the seniority of the asker. The recovery go/no-go (2) is the keystone: it sits on the critical path — every minute of delay extends the outage minute for minute — and, decisively, its outcome changes the content of items 1 and 3 (both the quote and the ministerial briefing must describe the recovery plan and the new timeline; approving a quote before the decision risks approving fiction). The overflow script (4) is a two-minute authorisation that immediately improves thousands of citizens' experience of the outage — maximum harm reduction per unit of your time, and it cannot wait behind two conversations. The press quote (1) has the tightest external deadline and comes third, now accurate. The minister's office (3) has the widest window ("this hour") and lands last precisely so the briefing is complete: decisions made, mitigation active, media line settled — which is what that audience actually needs, and a call-back at minute twenty-five with substance serves them better than a call-back at minute five with none. A and C order by rank and visibility — the perennial senior-SJT trap — and both would have you describing an undecided plan to the most consequential audiences. D gets the first two right in spirit but delays the deadline-bound quote behind an unhurried decision sequence. The scored pattern, one sentence: make the decision that everything else reports on, stop the bleeding you can stop in minutes, then serve external audiences in deadline order with the truth you have just finished making. That is **User focus**, **Ownership and initiative**, and collaboration with communication managers, compressed into five minutes of sequencing.

### Preparation tips

- **Judge options by their failure modes.** For each response, ask "what is the worst thing this can cause, and how likely is it?" The least-effective option is usually the one that can actively mislead, silence, or destroy an option — not the one that merely adds little.
- **Rehearse the accountability reflex.** Practise saying, in writing and aloud, "I made this call; it was wrong because X; here is what changes." Question 9's pattern appears in most senior SJTs, and hesitation there is expensive in tests and careers alike.
- **Audit your delegation instincts.** After each real incident, list what you did personally and ask which items only you could have done. If the list of "only me" items is short and the list of things you did anyway is long, Questions 2 and 8 are your practice ground.
- **Script your calibrated phrases.** "Estimate by 12:30, not a commitment"; "restored on a workaround, root cause open"; "I need the backup step because…" — having honest formulations ready under pressure is a trainable skill, and SJT options are largely distinguished by exactly these formulations.
- **Practise the one-minute inclusion move.** In your next three meetings, deliberately invite one named quiet expert before a decision closes. The habit that scores in Question 10 is built in calm rooms, not on bridges.
- **Study your organisation's failed handoffs.** Where do review recommendations actually die — no owner, no date, no priority, no follow-up? Knowing the local leak makes Question 11-type answers concrete rather than theoretical.

### Common pitfalls to avoid

- **Ordering by seniority instead of dependency.** Ministers, directors and journalists pull attention; critical-path decisions and user harm should allocate it. The strongest answers serve senior audiences later and better.
- **Confusing documentation with mitigation.** "Note that the risk was accepted" changes who is blamed, not what happens. Options that paper over an unmitigated risk are consistent low-scorers.
- **Treating honesty and reassurance as opposites.** The top-scoring communication options are almost always both: accurate content, calm framing, a committed next update. Pure comfort and pure stonewalling both lose marks.
- **Letting sunk outage time drive forward decisions.** "We've been down four hours" is not a reason to skip the backup step, gamble the deadline, or push the exhausted specialist. Forward-looking arithmetic only.
- **Using the major incident mechanism as a lever.** Pre-emptive declarations to force attention, majors held open to track project work, stand-downs timed for reporting convenience — every misuse of the mechanism spends its credibility. Keep the tool sharp by keeping it honest.
- **Solving team dynamics after the incident.** The deleted chat message, the interrupting account manager, the drifting bridge — senior SJTs place these mid-incident because that is when they must be handled. "Address it in the wash-up" is usually the second-best answer wearing a sensible face.

## Conclusion

Well done for working through this guide in full. You have covered the four assessment families — cognitive, numeric, verbal and situational judgement — and forty-eight practice questions built deliberately from the materials of your command: dependency maps and severity criteria, availability arithmetic and recovery timelines, runbook preconditions and supplier contracts, and the human decisions of bridges, briefings and post-incident truth-telling.

A few threads are worth carrying away. First, the same disciplines score in assessments and in majors: keep hypotheses honest and update them at the speed of the evidence; compute the bad branch, not just the plan; parse the operators in every criterion and contract before applying the facts; preserve each fact's degree of certainty as it travels upward; and when judging what to do, weigh what each option does to the users, the team, the truth, and the next incident. Practising for a test at this level is indistinguishable from rehearsing command.

Second, assessments measure trained performance, not fixed ability — and senior candidates often under-practise, assuming experience will carry them. Experience supplies the judgement; practice supplies the speed and the discipline under artificial constraints. Short, regular sessions — attempt honestly, then study the explanation as a debrief — will move your scores the way rehearsed runbooks move recovery times. Review your errors by mechanism ("I anchored", "I averaged unweighted", "I upgraded an estimate") exactly as you would review an incident.

Third, connect the practice to your development and your team's. The capabilities exercised here — evidence discipline, numerical honesty, calibrated communication, inclusive command — are the ones that distinguish major incident managers who are merely experienced from those who are trusted with the largest crises, and they are also the substance of head-of-service responsibility where your role carries it. Consider folding what you have practised into how you coach your deputies: the delegation patterns, the calibrated phrases, the one-minute inclusion move, and the handover engineering that makes lessons survive. A command capability that lives in one person is a single point of failure; your framework's collaboration skills exist precisely to replicate it.

Finally, be encouraged. You hold one of the most demanding operational roles in government digital services: when the worst days happen, you are the person the organisation turns to for order, honesty and restoration. Working through a guide like this — carefully, question by question — is exactly the proactive ownership your profession values. Walk into any assessment rested and confident that you have practised on material that mirrors the real thing, because you have. Good luck — and may your majors be rare, short, and well-commanded.
