# Delivery Manager - Psychometric Assessment Resources

## Introduction

Welcome! This guide has been created for you as a delivery manager in the UK Government Digital and Data profession. You may be preparing for an internal assessment or promotion board, applying for a new post, benchmarking your own capability, or simply curious about how psychometric assessments relate to the work you do every day. Whatever your reason, this document is designed to help you practise deliberately, reflect honestly, and walk into any assessment with confidence.

Psychometric assessments are structured, standardised exercises that measure the cognitive abilities and behavioural judgement that predict success in a role. For a delivery manager, well-designed job-specific assessments go far beyond abstract puzzles. They use the artefacts you genuinely handle — sprint and flow metrics, burndown and cumulative flow data, dependency maps, budget reports, supplier correspondence, service standard guidance, and stakeholder communications — and they simulate the decisions you genuinely make: selecting the right delivery method for a context, diagnosing where flow is breaking down, balancing cost against value, deciding when and how to escalate, and choosing what to say to a difficult room.

Why do these assessments matter for your role in particular? As a delivery manager, you are accountable for the performance of the team. You build and maintain teams, identify obstacles and help the team overcome them, focus effort on what matters most to the delivery of products and services, and coach others in Agile and Lean tools and techniques. Every one of those accountabilities rests on the abilities these assessments measure. Diagnosing an obstacle is applied cognitive reasoning. Providing delivery confidence is numeric reasoning about velocity, capacity, and forecasts. Interpreting the needs of technical and non-technical stakeholders is verbal reasoning under real conditions. And almost everything else — the coaching conversations, the escalation calls, the difficult discussions you host — is situational judgement.

This document is organised into four main assessment sections:

1. A workplace job-specific cognitive assessment — pattern recognition, logical deduction, error checking, prioritisation, and problem solving using delivery artefacts.
2. A workplace job-specific numeric reasoning assessment — percentages, rates, averages, forecasts, budgets, and flow metrics, with every calculation worked step by step.
3. A workplace job-specific verbal reasoning assessment — comprehension and inference from the passages a delivery manager actually reads: guidance extracts, supplier letters, governance papers, and reports.
4. A workplace job-specific situational judgement assessment — realistic dilemmas of team leadership, stakeholder management, and escalation, with most-effective and least-effective formats.

Each section follows the same pattern: an overview of what the assessment measures and why employers use it for this role, a mapping of the assessment's dimensions to the named skills in your capability framework, a substantial set of practice questions progressing from easy to challenging with full worked explanations, then preparation tips and common pitfalls.

To get the most from this guide: attempt each question honestly before reading the answer — commit to a choice in writing first. Treat every explanation as a short lesson, even when you answered correctly, because the reasoning technique is the real content. And connect what you practise here back to your day job; you will find that almost every question is a tidied-up version of something that has already crossed your desk.

Find a quiet hour, bring a notepad, and let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive assessment measures the mental processes your role demands, using practical workplace material rather than abstract items. Instead of shape sequences, you will reason about flow metrics, working agreements, dependency chains, release rules, and delivery data — and you will be asked to do so quickly and accurately.

The typical format is an online, timed test of 15 to 30 minutes covering pattern recognition, logical deduction, error checking, prioritisation, and applied problem solving. Scoring is objective against a norm group, and many modern platforms are adaptive: questions get harder as you answer correctly, so a test that feels increasingly difficult is usually a test going well. Employers typically receive a profile of accuracy and speed rather than a single number, which means working both carefully and briskly matters. Ungraded practice items are normally offered before the timed section begins.

Employers use cognitive assessments for delivery managers because the role is, at its core, structured noticing and reasoning under time pressure. A delivery manager who can look at a cumulative flow diagram and locate the bottleneck, hear three stand-up updates and detect the contradiction, or hold four constraints in mind while re-planning a release, converts raw information into team performance. The assessment simulates those demands in miniature: it rewards reading the given rules exactly, applying all of them, and resisting the pull of assumption.

At your level, expect scenarios about independent delivery and coordination: you are the person accountable for the team's performance, running its cadence, managing dependencies that cross team boundaries, and deciding what to fix, what to delegate, and what to escalate.

### How this assessment maps to your role

Each cognitive dimension corresponds to named skills in your role summary:

- **Pattern recognition** maps to **Agile and Lean practices**: helping teams measure, evaluate and visualise outcomes means seeing the recurring signal in noisy delivery data — a widening band on a cumulative flow diagram, a retro theme that keeps returning, a dependency that slips every quarter.
- **Logical deduction** maps to **Planning** and **Maintaining delivery momentum**: managing complex internal and external dependencies is sustained conditional reasoning — if the platform release slips, then the integration window moves, then the assessment date is at risk.
- **Error checking** maps to **Making a process work** and **Financial management**: identifying unnecessarily complicated processes, and monitoring cost and budget, both depend on spotting the inconsistency — the process step that contradicts another, the report line that does not reconcile.
- **Prioritisation** maps to your accountability to focus the team on what is most important to the delivery of products and services, and to **Planning**: prioritising the most important or high value tasks in a live environment where urgency and impact rarely align neatly.
- **Applied problem solving** maps to **Life cycle management** and **Team dynamics and collaboration**: identifying whether a product should move to the next phase, and recognising and dealing with issues in a team, are both exercises in decomposing a messy situation into a tractable decision.

### Practice questions

**Question 1 (easy) — Pattern recognition in flow data**

Your team's board shows the count of work items in each state at the end of each of the last four weeks:

| Week | To do | In progress | In review | Done (cumulative) |
|---|---|---|---|---|
| 1 | 20 | 4 | 2 | 10 |
| 2 | 18 | 4 | 5 | 12 |
| 3 | 16 | 4 | 9 | 13 |
| 4 | 15 | 4 | 13 | 14 |

Which state shows the clearest unhealthy trend?

- A) To do
- B) In progress
- C) In review
- D) Done

**Correct answer: C**

**Explanation:** Read each column as a time series. "To do" falls steadily (20, 18, 16, 15) — work is being pulled, which is healthy. "In progress" is stable at 4 — a consistent level of work in progress. "Done" rises each week, though note the rate is slowing (10, 12, 13, 14: increments of 2, 1, 1). The unmistakable signal is "In review": 2, 5, 9, 13 — items are entering review far faster than they are leaving it, and the queue is compounding weekly. This is the classic bottleneck signature on a cumulative flow view: one band widening while throughput flattens. Your **Agile and Lean practices** skill — helping teams measure, evaluate and visualise outcomes — is exactly this reading: the team looks busy, work in progress looks controlled, yet finished value is slowing because review capacity does not match development capacity. The follow-up in real life would be a team conversation about review practice: pairing on reviews, review-before-new-work agreements, or work-in-progress limits that include the review column.

**Question 2 (easy) — Logical deduction from a working agreement**

Your team's definition of done states: "A story is done only when its code is peer reviewed, its automated tests pass, and the product owner has accepted it in the demo environment." At the review, a developer says story S is done. Later you learn the product owner has not yet seen story S. Which conclusion must be true?

- A) The developer lied.
- B) Story S's tests failed.
- C) Story S does not meet the definition of done as stated.
- D) The definition of done is too strict.

**Correct answer: C**

**Explanation:** The definition is a conjunction of three conditions: peer review, passing tests, and product owner acceptance. Product owner acceptance has not happened, so at least one required condition is unmet, and the story cannot meet the definition — that is option C, and it follows necessarily. Option A over-reaches: the developer may sincerely believe "done" means "code complete"; a mistaken claim is not a lie, and the distinction matters for how you handle it. Option B invents a fact about tests the scenario never mentions. Option D is an opinion, not a deduction. The workplace parallel is precise: definitions of done exist so that "done" is a fact, not a feeling, and your role in maintaining that shared language is part of providing the transparent framework in which teams deliver. The constructive follow-up is not an accusation but a calibration: a brief reminder of what the team agreed "done" means, and curiosity about whether the agreement still serves the team.

**Question 3 (easy) — Error checking a delivery report**

Before sending your monthly report, you re-read this paragraph:

"The team completed 58 of 64 planned points (91%). Both quarterly objectives remain on track. The payments integration is blocked pending supplier credentials, which we expect within a week; this blocks objective 2's final milestone. No risks require escalation this month."

Which two sentences are in tension with each other?

- A) Sentences 1 and 2
- B) Sentences 2 and 3
- C) Sentences 3 and 4
- D) Sentences 1 and 4

**Correct answer: B**

**Explanation:** Sentence 2 claims both objectives are on track. Sentence 3 states that a live blocker "blocks objective 2's final milestone." An objective whose final milestone is currently blocked by an external dependency may still be recoverable, but reporting it as unqualifiedly "on track" while simultaneously describing its blocker is internally inconsistent — a reader cannot tell which sentence to believe. (Sentence 4 is at least defensible: a blocker with a credible one-week resolution may genuinely not need escalation yet, though a careful writer would connect it explicitly.) The fix is a sentence like: "Objective 2 is at risk pending supplier credentials expected within a week; we will escalate if they slip." Reporting on delivery — named in your **Financial management** skill as reporting on financial delivery, and implicit in providing delivery confidence — depends on this internal-consistency check. Stakeholders forgive amber; they do not forgive discovering that green and amber were both asserted in the same paragraph.

**Question 4 (moderate) — Prioritisation across competing demands**

It is 9:00 on Monday. Four items compete for your attention:

1. The team's deployment pipeline has been failing since Friday evening; nothing can be released, and a fix for a live defect affecting users is waiting to go out.
2. A director's office has asked for delivery data for a parliamentary question response, needed by 16:00 today.
3. Sprint planning is at 11:00 and the backlog has not been refined for it.
4. A supplier's project manager wants to discuss a contract variation this week.

Which sequencing is most defensible?

- A) 2, 1, 3, 4 — parliamentary business always comes first
- B) 1, 2, 3, 4 — unblock the user-affecting release, get the PQ data moving, then prepare planning, then schedule the supplier
- C) 3, 1, 2, 4 — the nearest meeting first
- D) 1, 3, 2, 4 — team ceremonies outrank external requests

**Correct answer: B**

**Explanation:** Weigh impact and urgency together, and consider what each item needs from you specifically. Item 1 has live user harm accumulating (a defect fix is stuck behind a broken pipeline) — your first action is to confirm the right people are on it and remove anything blocking them, which may take fifteen minutes of your time, not a morning. Item 2 has a hard same-day deadline and statutory seriousness; once item 1 is in motion, get the PQ data underway — much of it may be delegable, but you own its accuracy. Item 3 matters by 11:00; a pragmatic delivery manager can also negotiate — planning can start with the refined portion or shift an hour if genuinely necessary. Item 4 says "this week": schedule it. Option A treats the PQ as pre-empting live user harm, but the PQ deadline is 16:00 — sequencing the pipeline first costs the PQ nothing. Options C and D prioritise by proximity and by category respectively, rather than by impact. Note the deeper technique, which mirrors your accountability to focus the team on what is most important: sequence by impact-weighted urgency, and spend your personal effort where only you can act, delegating the rest.

**Question 5 (moderate) — Pattern recognition in recurring impediments**

You keep an impediment log. Over six sprints, entries include: sprint 1 — "waiting for security review (5 days)"; sprint 2 — "test environment refresh delayed (3 days)"; sprint 3 — "waiting for security review (4 days)"; sprint 4 — "waiting for security review (6 days)", "test environment refresh delayed (2 days)"; sprint 5 — "key stakeholder unavailable for sign-off (4 days)"; sprint 6 — "waiting for security review (5 days)". What is the most valuable conclusion to draw?

- A) The team raises too many impediments and should be more self-sufficient.
- B) Security review waits are a systemic pattern costing roughly a week most sprints, and warrant a structural fix rather than sprint-by-sprint chasing.
- C) Sprint 5 shows stakeholder availability is the biggest problem.
- D) The impediments are varied, so no pattern exists.

**Correct answer: B**

**Explanation:** Tally the log. Security review waits appear in four of six sprints (1, 3, 4, 6), costing 4–6 days each time — a persistent, expensive pattern. Environment delays appear twice; stakeholder availability once. Option B correctly identifies the dominant recurring impediment and, crucially, draws the right kind of conclusion: a problem that recurs at this frequency has stopped being an incident and become a system property, so the response should be structural — for example, agreeing a review service-level expectation with the security team, booking review slots at sprint start, shifting security engagement earlier ("shifting left"), or raising the capacity question with the security team's management. Option A blames the messenger. Option C promotes a single occurrence over a four-time pattern. Option D mistakes "some variety" for "no signal." This is the cognitive core of **Making a process work** — identifying organisational processes that repeatedly tax delivery — and of **Maintaining delivery momentum**: chasing the same impediment every sprint is motion; removing its cause is progress.

**Question 6 (moderate) — Deduction with release constraints**

Release rules for your service: (i) releases happen only on Tuesdays and Thursdays; (ii) a release requires a completed regression run, which takes two full working days and must finish before release day; (iii) no releases during the last week of the fiscal quarter; (iv) the change advisory board (CAB) must approve on the working day immediately before release. The regression run starts Monday of week 1. The last week of the quarter is week 2. What is the earliest possible release day?

- A) Thursday of week 1
- B) Tuesday of week 2
- C) Tuesday of week 3
- D) Thursday of week 3

**Correct answer: A**

**Explanation:** Apply each rule in sequence. Rule (ii): regression starts Monday and takes two full working days — Monday and Tuesday — finishing end of Tuesday, week 1. The release must be after that, so Wednesday onward. Rule (i): the next permitted day is Thursday of week 1. Rule (iv): CAB approval must happen the working day before — Wednesday of week 1 — which is possible; nothing in the scenario prevents it. Rule (iii): week 1 is not the quarter's last week (week 2 is), so Thursday of week 1 is not embargoed. All four rules are satisfied by Thursday of week 1 — option A. The distractors reward incomplete reasoning: B falls in the embargoed week; C and D are what you get if you assume the embargo or the CAB step forces a longer delay than it does. The lesson runs both ways: check every rule, but also do not invent constraints the rules do not contain. Over-constraining a plan delays value just as surely as under-constraining it risks failure — a balance your **Planning** skill navigates constantly.

**Question 7 (moderate) — Error checking a dependency map**

Your programme's dependency register contains these entries for your team (Team A):

| ID | Statement |
|---|---|
| 1 | Team A needs the identity API from Team B by 1 June. |
| 2 | Team B will deliver the identity API on 15 June. |
| 3 | Team A's payment milestone, which requires the identity API, is due 10 June. |
| 4 | The programme plan lists Team A's payment milestone as green. |

Assuming entries 1–3 are accurate, what is wrong with entry 4?

- A) Nothing; milestones can be green while dependencies are outstanding.
- B) The milestone cannot credibly be green: its required dependency arrives five days after the milestone's due date.
- C) Entry 4 should say the milestone is complete.
- D) Entry 2 must be wrong, because Team B is always late.

**Correct answer: B**

**Explanation:** Chain the dates. The payment milestone (due 10 June) requires the identity API. The API arrives 15 June — five days after the milestone needs it. Unless something changes, the milestone will be missed; a green status asserts the opposite of what the register's own entries imply. That is option B. Option A describes a real situation (outstanding dependencies with credible dates can coexist with green) but not this one, where the dates are already incompatible. Option C confuses status with completion. Option D generalises beyond the data. This is a reasoning pattern worth naming: internal contradiction between a plan's status and its own recorded facts. Registers and RAG reports drift apart because they are updated by different people at different times, and the delivery manager who cross-checks them — then raises the discrepancy factually with the milestone owner and the programme office — is doing precisely what managing complex internal and external dependencies means. The constructive output is not "your report is wrong" but "these three entries can't all be true; which needs updating, and what's our recovery option?"

**Question 8 (moderate) — Problem solving with work-in-progress limits**

Your team of five developers has agreed a work-in-progress (WIP) limit of one item per developer plus one team buffer — six items maximum in progress. A stakeholder urgently requests a small, genuinely time-critical fix. The board currently shows six items in progress. The team asks how to proceed without breaking their agreement. Which option best respects both the urgency and the team's system?

- A) Add the fix as a seventh item; limits are guidelines.
- B) Refuse the fix until an item finishes, whatever that takes.
- C) Apply the team's expedite approach: pause or finish one current item to make room, make the trade visible on the board, and review at the retro whether an explicit expedite lane policy is needed.
- D) Have the most junior developer do the fix secretly, off the board.

**Correct answer: C**

**Explanation:** WIP limits exist to protect flow — more items in progress means slower completion for everything — but a limit with no mechanism for genuine urgency will simply be broken under pressure, eroding the whole agreement. Option C threads the needle: the urgent item enters, but something else visibly pauses to pay for it, so the limit's protective function survives and the cost of the interruption is explicit rather than hidden. The retro follow-up turns an improvised exception into a deliberate policy (many teams adopt a formal expedite lane with strict entry criteria). Option A quietly abolishes the limit — the first untracked exception invites the tenth. Option B honours the rule but not its purpose; rules serve delivery, not the reverse, and your role summary is explicit about guiding teams to focus on outcomes over process. Option D is the worst of all worlds: invisible work, an overloaded junior colleague, and a board that no longer tells the truth. The general principle — make exceptions visible and priced, never silent and free — applies to far more than WIP limits.

**Question 9 (challenging) — Multi-constraint scheduling**

You must schedule four events in one five-day week (Monday–Friday): sprint review (R), retrospective (T), sprint planning (P), and a stakeholder demo (D). Constraints: (i) R must occur before T, and T before P — review, then retro, then planning; (ii) the product owner attends R, P, and D, but is away Monday and Tuesday; (iii) D must be at least two days after R, to act on review feedback; (iv) at most one of these events per day. On which day must the demo (D) take place?

- A) Wednesday
- B) Thursday
- C) Friday
- D) It cannot be scheduled this week

**Correct answer: D**

**Explanation:** Work the constraints exhaustively. The product owner attends R, P, and D, and is away Monday–Tuesday, so R, P, and D must each fall on Wednesday, Thursday, or Friday. Constraint (i) orders R before T before P. T does not need the product owner, but it must sit strictly after R, and R cannot occur before Wednesday — so T cannot be earlier than Thursday. With one event per day (constraint iv), the only arrangement for the ordered trio is R on Wednesday, T on Thursday, P on Friday. That fills all three available product-owner days — and D still needs one of them. Re-check constraint (iii) for completeness: D must be at least two days after R; with R on Wednesday, D could only be Friday — but Friday is taken by P. Every path exhausts the week, so the demo cannot be scheduled this week: option D. This question deliberately punishes pattern-matching ("the answer is probably Friday") and rewards exhaustive checking — if you selected Friday, the missed step was verifying the candidate against the one-event-per-day rule. Real planning weeks are exactly like this: sometimes the honest output of scheduling reasoning is "this does not fit — something must move," and saying so early, then negotiating which constraint to relax (a second event on one day? the demo early next week?), is a planning skill, not a failure.

**Question 10 (challenging) — Diagnosing a velocity anomaly**

Your team's velocity over eight sprints: 30, 31, 29, 30, 44, 45, 43, 46. The jump coincides with sprint 5, when the team switched estimation approach after two new members joined. The product owner is delighted: "The team is 50% faster!" Stakeholders want the roadmap re-forecast using velocity 45. What is the soundest interpretation?

- A) The team became 50% more productive; re-forecast with 45.
- B) The scale changed: post-sprint-5 points are not the same unit as pre-sprint-5 points, so compare forecasts only within the new baseline, and re-estimate remaining roadmap work in the new scale before re-forecasting.
- C) The new members caused the increase; velocity will keep rising.
- D) Velocity is meaningless and should not inform forecasts.

**Correct answer: B**

**Explanation:** Velocity is a relative measure: points mean whatever the estimating team's current calibration makes them mean. A step-change that coincides exactly with a change in estimation approach and team composition is far more plausibly a re-calibration of the unit than a 50% productivity leap — genuine productivity changes of that size do not arrive in one sprint and hold steady. The tell is the pattern itself: two flat plateaus (≈30, then ≈44–46) with a single step between them, rather than a gradual climb. Option B draws the correct operational conclusion: the new baseline is internally consistent (44–46 is stable), so forecasting is fine provided the remaining backlog is estimated in the same new scale — mixing old-scale backlog estimates with new-scale velocity would inflate the forecast dangerously. Option A commits that exact error. Option C asserts a cause and a trend the data cannot support. Option D overcorrects into nihilism; helping teams measure, evaluate and visualise outcomes includes knowing what a measure can and cannot say. The stakeholder conversation this implies — gently deflating "50% faster!" without deflating the team — is your **Communicating between the technical and non-technical** skill applied to metrics.

**Question 11 (challenging) — Prioritising by cost of delay**

Four items sit at the top of the backlog. The team can complete roughly one per sprint. You facilitate a prioritisation discussion using these agreed facts:

1. Item W: saves the operations team £8,000 per month once live; no deadline.
2. Item X: required for a regulation taking effect in four sprints; the service cannot legally operate without it after that date.
3. Item Y: fixes a defect causing 2% of users to fail a journey they can currently complete by phone at extra operational cost of about £3,000 per month.
4. Item Z: a director's pet reporting feature, requested often, with no measured value.

Which ordering best reflects cost of delay and risk?

- A) Z, X, W, Y — seniority first
- B) X, W, Y, Z — legal deadline first (it consumes the available runway), then highest monthly saving, then the smaller saving, then the unmeasured request
- C) W, Y, X, Z — money first, compliance later
- D) X, Y, W, Z — legal first, then user-facing defect, then savings, then the request

**Correct answer: B**

**Explanation:** Start with X: a hard legal deadline four sprints out, with one item deliverable per sprint, means X must start within the next sprint or two to hold any buffer — deadline items consume runway even when their value feels less tangible than cash. Then compare W and Y on cost of delay: each sprint of delay to W forgoes £8,000; each sprint of delay to Y costs about £3,000 plus a degraded (but not blocked) user journey. On the stated facts, W's monthly cost of delay is higher, so W precedes Y — though note this is the closest call in the set, and a team could defensibly weigh the user experience harm in Y more heavily if evidence showed greater impact; option D fails not because caring about users is wrong but because it ignores the quantified comparison the scenario provides. Z, with no measured value, goes last pending evidence — and the honest conversation with the director is about measuring its value, not about rank. Option C's error is starker than it looks: delaying X risks the service's legal ability to operate, a category of harm money comparisons do not capture. This is your **Planning** skill — prioritising the most important or high value tasks using data — and your **Financial management** skill of balancing cost versus value, exercised together.

**Question 12 (challenging) — Spotting the flawed improvement argument**

At a retro, a team member argues: "Our defect count doubled in the two sprints after we started pairing on complex stories. Pairing is clearly hurting quality — we should stop." You recall two relevant facts: the team also began recording defects in the tracker (instead of fixing them silently) at the same time as the pairing experiment, and the two sprints in question included the riskiest integration work of the quarter. What is the strongest response to the argument?

- A) Agree: the numbers speak for themselves, and doubling is decisive.
- B) Point out that two simultaneous changes (defect recording and work risk profile) confound the comparison, so the defect count cannot yet attribute cause; propose a fairer evaluation before deciding.
- C) Overrule the discussion: pairing is best practice and is not up for debate.
- D) Compromise by pairing half as often, splitting the difference.

**Correct answer: B**

**Explanation:** The argument commits a classic causal error: attributing an outcome change to one intervention when at least two other things changed simultaneously. Recording defects that were previously fixed silently would raise the measured count with no change in real quality — a measurement artefact. Riskier integration work would plausibly raise genuine defects regardless of pairing. With three candidate causes, the doubling supports no attribution at all yet. Option B names the confounds and proposes the professional remedy: a fairer evaluation — for example, comparing escaped defects (found after release) rather than recorded ones, or comparing against similar-risk work, or simply running the experiment longer. Option A accepts the flawed inference. Option C wins the argument by authority and loses the team's ownership of its own practice — the opposite of encouraging experimentation and reflective practice, which your **Agile and Lean practices** skill requires. Option D treats a causal question as a negotiation. The transferable technique: when a metric moves, list everything that changed in the same window before crediting or blaming any one of them. Retrospectives run on this discipline; so do supplier performance reviews and benefits claims.

### Preparation tips

- **Practise on your own team's artefacts.** Once a week, read your board's flow data, your dependency register, and your latest report with an assessor's eye: what pattern, contradiction, or unsupported claim is hiding in plain sight? This is free, role-perfect practice.
- **Apply every rule, then stop.** Multi-constraint questions are lost in two ways: missing a rule, and inventing one. After choosing an answer, run each stated constraint against it once — and nothing more.
- **Name the reasoning pattern.** Bottleneck signature, internal contradiction, confounded comparison, changed measurement scale, cost of delay. Recognising the pattern by name halves the solving time, in tests and in meetings.
- **Rehearse under mild time pressure.** Three questions in six minutes, then review. Speed comes from familiarity, not rushing.
- **Distinguish "must be true" from "probably true."** Deduction questions reward only what the given facts guarantee. Your workplace intuition is a hypothesis generator, not an answer key.
- **Review errors for process, not content.** When you get a practice question wrong, identify the step that failed — misread rule, skipped constraint, wrong direction of comparison — and write it down. Your error log is your syllabus.

### Common pitfalls to avoid

- **Diagnosing from busyness rather than queues.** In flow questions, the bottleneck is where work accumulates, not where people look idle or overloaded.
- **Accepting a status that contradicts its own evidence.** Green milestones with incompatible dependency dates, "on track" beside a described blocker — cross-check statuses against their underlying facts.
- **Treating a step-change in a metric as a performance change.** First ask whether the measurement, the scale, or the work mix changed.
- **Stopping at the first satisfying answer.** Verify your candidate against every constraint — especially the unglamorous ones like "one event per day."
- **Letting seniority or recency drive prioritisation.** Impact-weighted urgency, informed by cost of delay, is the defensible ordering logic.
- **Rushing early questions.** Adaptive tests build your score on them, and careless errors there are the most expensive kind.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment measures how accurately and confidently you work with the numbers your role genuinely produces: velocity and throughput, capacity, burn rates, budgets, supplier costs, defect rates, and forecast arithmetic. It is not a mathematics exam. The operations are percentages, ratios, averages, rates, and differences — but applied to realistic delivery data, under time pressure, where selecting the right figures from a table matters as much as the arithmetic itself.

The typical format is online and timed: 20 to 30 minutes for 15 to 25 questions, each presenting data (a table, chart description, or figures embedded in text) followed by a calculation or comparison. Scoring is objective, and platforms usually report accuracy and pace separately. An on-screen calculator is often permitted — check the instructions, and practise both with and without one.

Employers use numeric assessments for delivery managers because the role's credibility runs on numbers handled well. "Provide delivery confidence" — a phrase taken directly from your skill framework — is a numeric claim: it means being able to say, with working shown, whether the plan fits the capacity, whether the burn rate fits the budget, and whether the trend supports the forecast. A delivery manager who mis-reads a percentage in a governance paper, or forecasts from an inflated average, spends the team's credibility. One who can quickly and correctly say "that supplier option costs £4,300 more over the quarter" or "our throughput supports March, not January" earns the team room to work.

Every worked answer below shows its arithmetic step by step. Follow the steps even when you get the answer right — the method under time pressure is the skill being trained.

### How this assessment maps to your role

- **Percentages, ratios and proportions** map to **Agile and Lean practices** (helping teams measure, evaluate and visualise outcomes) and to reporting on delivery: completion rates, defect ratios, and utilisation are the everyday units of delivery conversation.
- **Averages, medians and trends** map to **Planning**: using data to inform planning means choosing the representative number — and knowing when an average misleads.
- **Rate and capacity arithmetic** maps to **Maintaining delivery momentum**: managing pace and tempo quantitatively — throughput per week, capacity after leave, time to drain a queue.
- **Budget and cost calculations** map to **Financial management**: monitoring cost and budget, balancing cost versus value, and reporting financial delivery all reduce to day rates, run rates, variances, and comparisons done correctly.
- **Supplier cost comparison** maps to **Commercial management**: as the point of contact for contracted suppliers, you sanity-check quotes, extensions, and variations before they reach commercial colleagues.
- **Reading tables and charts** maps to **Communicating between the technical and non-technical**: translating a data table into one accurate sentence for a stakeholder is a numeric act before it is a verbal one.

### Practice questions

**Question 1 (easy) — Sprint completion percentage**

Your team planned 55 points and completed 44. What percentage of the plan was completed?

- A) 75%
- B) 80%
- C) 82%
- D) 85%

**Correct answer: B**

**Explanation:** Completion percentage = completed ÷ planned × 100.

Step 1: 44 ÷ 55 = 0.8.
Step 2: 0.8 × 100 = 80%.

The team completed 80% of its plan. A quick mental route: 55 × 0.8 = 44, confirming the division. Keep the direction of division firmly in mind — completed over planned — because inverting it gives 55 ÷ 44 = 1.25, and "125%" should immediately look wrong for a sprint that left work unfinished. In reporting, pair the percentage with the absolute numbers ("44 of 55 points") so readers of different fluency levels can each anchor on what they trust.

**Question 2 (easy) — Average throughput**

Your team finished 12, 15, 11, 14, and 13 work items in the last five weeks. What is the average weekly throughput?

- A) 12 items
- B) 12.5 items
- C) 13 items
- D) 14 items

**Correct answer: C**

**Explanation:** Average = total ÷ number of periods.

Step 1: 12 + 15 = 27.
Step 2: 27 + 11 = 38.
Step 3: 38 + 14 = 52.
Step 4: 52 + 13 = 65.
Step 5: 65 ÷ 5 = 13.

Average throughput is 13 items per week. Throughput (finished items per period) is often more robust than story-point velocity for forecasting, because it does not depend on estimation calibration — a point worth remembering from the cognitive section's velocity-anomaly question. With a stable average like this (the weekly values sit tightly between 11 and 15), simple forecasts are defensible: 39 remaining items ÷ 13 per week ≈ 3 weeks, with the usual caveats about stability and scope.

**Question 3 (easy) — Capacity after absences**

Your team has 6 members and the sprint is 10 working days. One member is on leave all sprint, another for 4 days, and a public holiday removes 1 day for everyone present (assume the fully absent member's holiday is already covered by their leave). How many person-days of capacity remain?

- A) 41 person-days
- B) 42 person-days
- C) 45 person-days
- D) 46 person-days

**Correct answer: A**

**Explanation:** Build up from the maximum.

Step 1: Maximum = 6 × 10 = 60 person-days.
Step 2: Fully absent member: −10. Running total 50.
Step 3: Partial leave: −4. Running total 46.
Step 4: Public holiday: the 5 members not fully absent each lose 1 day: −5. Running total 41.

Capacity is 41 person-days — about two-thirds of the naive 60. The most common error is step 4: subtracting 6 (forgetting the fully absent member cannot lose a day twice) gives 40; subtracting 1 (treating the holiday as one day total rather than one day per person) gives 45, option C. Capacity questions reward slow, explicit accounting of who loses what. In sprint planning, this arithmetic is the difference between a commitment the team can honour and a quiet overcommitment — ensuring teams plan appropriately for their capacity is named in your **Planning** skill.

**Question 4 (easy) — Budget run rate**

Your team's budget for a 6-month period is £480,000. After 2 months, £172,000 has been spent. If spending continues at the same monthly rate, what will the total spend be at 6 months?

- A) £480,000
- B) £498,000
- C) £516,000
- D) £524,000

**Correct answer: C**

**Explanation:** Find the monthly rate, then project.

Step 1: Monthly rate = £172,000 ÷ 2 = £86,000 per month.
Step 2: Projected total = £86,000 × 6 = £516,000.

Projected spend is £516,000 against a £480,000 budget — an overspend of £36,000 (7.5% over) if nothing changes. This is the core of budget monitoring: not "how much have we spent?" but "where does the current rate land us?" Your **Financial management** skill lists monitoring cost and budget and knowing when to escalate — and this calculation is precisely the escalation trigger: a run rate pointing £36,000 over, identified at month 2, leaves four months to correct course (reduce spend to (480,000 − 172,000) ÷ 4 = £77,000 per month) or to seek a variance early. Run-rate projections surfaced at month 5 leave no such options.

**Question 5 (moderate) — Defect rate comparison**

Two releases are compared:

| Release | Stories shipped | Defects found in 30 days |
|---|---|---|
| 1 | 40 | 6 |
| 2 | 55 | 7 |

Which release had the lower defect rate per story, and what was it?

- A) Release 1, at 0.15 defects per story
- B) Release 2, at 0.127 defects per story
- C) Release 1, at 0.13 defects per story
- D) Release 2, at 0.15 defects per story

**Correct answer: B**

**Explanation:** Rate = defects ÷ stories.

Step 1: Release 1: 6 ÷ 40 = 0.15 defects per story.
Step 2: Release 2: 7 ÷ 55 = 0.1272… ≈ 0.127 defects per story.
Step 3: Compare: 0.127 < 0.15, so Release 2 has the lower rate.

Release 2 shipped more defects in absolute terms (7 vs 6) but at a lower rate, because it shipped 37.5% more stories. This absolute-versus-rate distinction is one of the most common sources of misleading delivery commentary: "defects went up" is true and yet quality per story improved. When you help teams measure and evaluate outcomes, insist on the denominator. A governance slide that reports defect counts without shipment volume invites exactly the wrong conclusion — and correcting that gently is part of translating between technical reality and non-technical audiences.

**Question 6 (moderate) — Percentage change in cycle time**

Median cycle time fell from 8 days to 5 days after the team adopted WIP limits. What is the percentage reduction?

- A) 30%
- B) 37.5%
- C) 40%
- D) 60%

**Correct answer: B**

**Explanation:** Percentage change = (old − new) ÷ old × 100.

Step 1: Reduction = 8 − 5 = 3 days.
Step 2: 3 ÷ 8 = 0.375.
Step 3: 0.375 × 100 = 37.5%.

Cycle time fell by 37.5%. Two distractors are built from classic errors: 60% comes from dividing 3 by 5 (the new value) instead of 8 (the original); 40% comes from rounding 37.5 carelessly or computing 5 ÷ 8 = 62.5% and subtracting sloppily. Always divide the change by the starting value. Note also the word "median" — cycle-time distributions are usually skewed by a few long-running items, so the median is the honest typical value, and quoting it (rather than a mean dragged upward by outliers) is the statistically fair way to describe the improvement the team earned.

**Question 7 (moderate) — Weighted cost of a blended team**

A team consists of 3 civil servants at an average cost of £400 per day each, and 2 contractors at £700 per day each. What is the team's total cost for a 10-day sprint, and what percentage of that cost is contractor cost?

- A) £26,000 total; 54% contractor
- B) £26,000 total; 50% contractor
- C) £25,000 total; 56% contractor
- D) £24,000 total; 58% contractor

**Correct answer: A**

**Explanation:** Compute each component.

Step 1: Civil servants per day: 3 × £400 = £1,200.
Step 2: Contractors per day: 2 × £700 = £1,400.
Step 3: Team per day: £1,200 + £1,400 = £2,600.
Step 4: Sprint total: £2,600 × 10 = £26,000.
Step 5: Contractor share: contractor sprint cost = £1,400 × 10 = £14,000; share = 14,000 ÷ 26,000 = 0.538… ≈ 54%.

Total £26,000, of which about 54% is contractor cost — despite contractors being only 40% of the headcount. That gap between headcount share and cost share is exactly what finance and commercial colleagues will ask about, and understanding it is part of balancing cost versus value: if the two contractors hold scarce skills that unblock the other three people, 54% of cost may be excellent value; if they are doing commodity work, this arithmetic is the opening line of a conversation about the team's shape and a case for building civil servant capability.

**Question 8 (moderate) — Reading a burnup with scope change**

A feature's burnup chart shows: total scope started at 100 points; at the end of week 4, completed work is 40 points and total scope has risen to 120 points. The team completes 10 points per week. Assuming scope stays at 120, how many more weeks to completion, and what did the scope change add to the timeline?

- A) 8 more weeks; the scope change added 2 weeks
- B) 8 more weeks; the scope change added 4 weeks
- C) 6 more weeks; the scope change added 2 weeks
- D) 12 more weeks; the scope change added 2 weeks

**Correct answer: A**

**Explanation:** Work from the current position.

Step 1: Remaining work = 120 − 40 = 80 points.
Step 2: Weeks remaining = 80 ÷ 10 = 8 weeks.
Step 3: Timeline effect of scope change: the added scope is 120 − 100 = 20 points; at 10 points per week that is 20 ÷ 10 = 2 additional weeks compared with the original scope.

Eight more weeks, of which two are attributable to scope growth. Burnup charts are precisely the visual that makes this conversation easy: the completion line climbs steadily while the scope line's jump visibly pushes the intersection point out. When stakeholders ask "why has the date moved?", the numerically literate answer separates the causes — "throughput is on plan; the date moved because scope grew 20%" — which keeps the discussion on scope decisions (a product owner conversation) rather than on team performance (a morale-damaging misdiagnosis). Presenting that distinction clearly is delivery confidence in its most concrete form.

**Question 9 (moderate) — Supplier variation cost check**

A supplier contract runs 60 days at £600 per day. The supplier proposes a variation: extend by 15 days, but with a revised rate of £650 per day applying to the extension days only. Commercial colleagues ask you to confirm the variation's cost and the new contract total. What are they?

- A) Variation £9,000; new total £45,000
- B) Variation £9,750; new total £45,750
- C) Variation £9,750; new total £48,750
- D) Variation £10,000; new total £46,000

**Correct answer: B**

**Explanation:** Keep the original and the variation separate.

Step 1: Original contract = 60 × £600 = £36,000.
Step 2: Variation = 15 × £650 = £9,750.
Step 3: New total = £36,000 + £9,750 = £45,750.

The variation costs £9,750 and the new total is £45,750. Distractor C (£48,750) comes from wrongly applying the new £650 rate to all 75 days — the single most common error when rates change mid-contract, and one worth double-checking in real variation paperwork, because supplier quotes occasionally make the same "error" in their own favour. Distractor A applies the old rate to the extension. As the team's point of contact for contracted suppliers, being the person who catches a £3,000 discrepancy before signature is a quiet but real contribution — and knowing how and when to escalate to commercial specialists starts with knowing the numbers are wrong.

**Question 10 (challenging) — Forecasting a queue drain**

A service's support queue holds 180 tickets. New tickets arrive at 40 per week. The team resolves 55 per week. The service owner asks: "When will the queue be cleared, and what backlog remains after 6 weeks?" Assuming stable rates, what do you tell them?

- A) Cleared in about 12 weeks; 90 tickets remain at 6 weeks
- B) Cleared in about 12 weeks; 60 tickets remain at 6 weeks
- C) Cleared in about 4.5 weeks; 0 tickets remain at 6 weeks
- D) Cleared in about 3.3 weeks; 0 tickets remain at 6 weeks

**Correct answer: A**

**Explanation:** The queue drains at the net rate, not the resolution rate.

Step 1: Net drain rate = 55 − 40 = 15 tickets per week.
Step 2: Time to clear = 180 ÷ 15 = 12 weeks.
Step 3: Backlog at 6 weeks = 180 − (15 × 6) = 180 − 90 = 90 tickets.

About 12 weeks to clear, with 90 tickets still queued at the halfway point. Distractor D (180 ÷ 55 ≈ 3.3 weeks) ignores arrivals entirely — the classic error; C compounds it with rounding generosity. This net-rate structure appears everywhere in delivery: backlogs, defect queues, user research participant pipelines, even recruitment. Two further points make the answer genuinely useful to the service owner: sensitivity (if arrivals rise to 50, the net rate halves to 5 and clearance stretches to 36 weeks — the forecast is fragile to small rate changes) and options (raising resolution capacity or reducing arrivals through root-cause fixes both attack the same subtraction). Presenting a forecast with its fragility attached is what providing delivery confidence means — confidence in the analysis, not false certainty in the number.

**Question 11 (challenging) — Budget variance with committed spend**

At the end of month 4 of a 12-month budget of £900,000, your report shows: actual spend to date £310,000; additionally, purchase orders already committed but not yet invoiced total £85,000. The finance partner asks for (a) the uncommitted budget remaining and (b) the average monthly spend available for the remaining 8 months if all commitments are honoured. What are they?

- A) £590,000 remaining; £73,750 per month
- B) £505,000 remaining; £63,125 per month
- C) £505,000 remaining; £73,750 per month
- D) £590,000 remaining; £63,125 per month

**Correct answer: B**

**Explanation:** Committed spend is spoken-for money and must be deducted.

Step 1: Total accounted for = actual + committed = £310,000 + £85,000 = £395,000.
Step 2: Uncommitted remaining = £900,000 − £395,000 = £505,000.
Step 3: Monthly available = £505,000 ÷ 8 = £63,125 per month.

The uncommitted budget is £505,000, or £63,125 per month for the remaining 8 months. Distractor A ignores commitments in both parts (900,000 − 310,000 = 590,000; ÷ 8 = 73,750), and the mixed distractors C and D catch those who deduct commitments in one step but not the other — consistency between numerator and conclusion is the check. The actual-versus-committed distinction is fundamental to real budget monitoring: teams that track only invoiced spend routinely "discover" overcommitment months late, because the money was promised long before it was billed. For comparison, the team's actual burn rate so far is £310,000 ÷ 4 = £77,500 per month — well above the £63,125 now available — so this report should trigger exactly the escalation conversation your **Financial management** skill describes: the current rate does not fit the remaining envelope, and either spend falls or the variance is raised now.

**Question 12 (challenging) — Choosing the representative metric**

Your team's last 10 completed items had cycle times (days): 2, 3, 3, 3, 4, 4, 5, 5, 6, 25. A stakeholder asks: "How long does an item typically take, and can you commit that a new item will be done within 10 days?" Which answer is most defensible?

- A) "The average is 6 days, so 10 days is guaranteed."
- B) "Typically about 4 days (median); 9 of the last 10 items finished within 6 days, so 10 days is a reasonable expectation, though roughly 1 in 10 recent items has run far longer — we should understand that outlier before promising."
- C) "The average is 6 days, so most items take about 6 days."
- D) "We cannot say anything; the data is too variable."

**Correct answer: B**

**Explanation:** Compute both central measures.

Step 1: Mean = (2+3+3+3+4+4+5+5+6+25) ÷ 10 = 60 ÷ 10 = 6 days.
Step 2: Median = average of 5th and 6th ordered values = (4 + 4) ÷ 2 = 4 days.
Step 3: Distribution check: 9 of 10 items finished in 6 days or fewer; one took 25.

The mean (6) is pulled up by a single outlier and describes almost no actual item; the median (4) describes the typical experience. For the commitment question, percentile thinking beats averages: 90% of recent items finished within 6 days, which supports 10 days as a reasonable service expectation — but the honest answer names the tail, because the stakeholder's real question is about risk, and roughly 1 item in 10 recently blew far past any reasonable bound. Option A converts an average into a guarantee, a category error with a built-in future apology. Option C says "most items take about 6 days" when in fact 6 of 10 took 4 or fewer. Option D wastes usable data. Option B models the full skill: right measure (median), right framing for commitments (percentiles and ranges, not point estimates), and a flagged investigation of the outlier — which is where the team's next improvement probably lives. This is using data to inform planning, exactly as your **Planning** skill describes it.

### Preparation tips

- **Drill the five core structures:** share of total, percentage change, weighted cost, net rate (arrivals minus completions), and run-rate projection. Nearly every delivery-numeric question is one of these wearing different clothes.
- **Write the formula before the numbers.** One line — "change ÷ original" — prevents the two most common errors (wrong denominator, wrong direction) before they happen.
- **Use your own delivery data weekly.** Compute your team's real throughput average, budget run rate, and cycle-time median. Familiar structures answer faster under test pressure.
- **Check answers against sense.** A queue draining faster than its resolution rate, a completion percentage over 100 with work left over, an extension costing more than the whole original contract — each should trip an alarm before you commit.
- **Keep precision until the last step.** Round at the end; intermediate rounding is how 37.5% becomes a wrong option.
- **Practise reading tables under time.** Give yourself 30 seconds to state a table's message in one sentence before touching the question — most table errors are selection errors, not arithmetic errors.

### Common pitfalls to avoid

- **Ignoring the denominator.** Absolute counts (defects, spend, tickets) mislead without their base. Rates and shares are what comparisons need.
- **Forecasting with the gross rate instead of the net rate.** Queues drain at completions minus arrivals.
- **Applying a revised rate to the whole contract** instead of only the varied portion — and its sibling, applying discounts whose conditions are not met.
- **Treating committed-but-uninvoiced money as available.** Deduct commitments before declaring headroom.
- **Quoting the mean of a skewed distribution as "typical."** Check the median and the spread first; one outlier can move a mean by days.
- **Turning estimates into guarantees.** Averages support expectations and ranges, never promises. Say what the data supports and no more.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment measures how precisely you extract meaning, test claims, and draw inferences from written material — using the document types a delivery manager actually reads: Service Standard guidance, governance papers, supplier correspondence, assessment reports, policy extracts, and internal emails. A passage is presented; questions then probe what it states, implies, and does not settle.

The dominant format is "true / false / cannot say": judged strictly against the passage, is a statement definitely true, definitely false, or undeterminable? Supporting formats include best-summary selection, strongest-inference identification, purpose-of-passage questions, and clear-writing judgement. Tests typically run 15 to 25 minutes for 15 to 30 questions — enough time to read properly, not enough to read twice carelessly.

Employers use verbal reasoning tests for delivery managers because the role is a communications switchboard with accountability attached. You listen to and interpret the needs of technical and non-technical stakeholders and manage their expectations — which begins with reading their words exactly. You relay guidance to the team, supplier commitments to commercial colleagues, and team status to governance forums, and every relay is an opportunity to add distortion or remove it. The test isolates that skill: can you hold the line between what a text says, what it implies, and what you merely assume?

The cardinal rule: answer only from the passage. "Cannot say" is the correct answer whenever the passage does not settle a statement — even when your professional experience shouts an answer. This maps directly to a workplace discipline you already know matters: the difference between "the supplier committed to 12 May" and "I think they meant 12 May" is the difference between information and rumour, and teams plan on what you relay.

### How this assessment maps to your role

- **Precise comprehension** maps to **Communicating between the technical and non-technical**: interpreting stakeholder needs and managing expectations starts with extracting exactly what was written — including conditions, exclusions, and hedges.
- **True/false/cannot-say discipline** maps to **Maintaining delivery momentum**: when you address risks, issues and dependencies whose ownership sits outside the team, the facts you relay must be facts; a mis-relayed supplier commitment becomes a plan built on air.
- **Inference** maps to **Life cycle management**: service standards and phase guidance state principles; deciding whether your service should move to the next phase requires sound inference from guidance to your situation, without over-reading.
- **Reading conditions and exceptions** maps to **Commercial management** and **Financial management**: contracts, spend controls, and variation clauses are structured as conditions; applying them correctly is first a reading task.
- **Clear-writing judgement** maps to your accountability for reporting and escalation: providing delivery confidence in writing, hosting difficult discussions with pre-reads, and reporting financial delivery all reward the plain, specific, actionable sentence over the defensive fog.

### Practice questions

Passage for Questions 1–4 (adapted service guidance):

"Teams must carry out user research throughout the service's development, not only at the start. During public beta, the service must be available to all users who need it, though teams may use a phased rollout to manage risk, provided the phasing criteria are published. A service may not charge users a fee during beta unless the equivalent non-digital channel already charges one. Before a service can move from beta to live, it must meet the performance targets agreed at its beta assessment, and the team must show that the service can operate sustainably without the continued presence of its original developers."

**Question 1 (easy) — True, false, or cannot say**

Statement: "User research is only required at the start of a service's development."

- A) True
- B) False
- C) Cannot say
- D) True during beta only

**Correct answer: B**

**Explanation:** The passage's opening sentence states the exact opposite: research must happen "throughout the service's development, not only at the start." The statement contradicts the text directly, so it is false. Direct-contradiction questions are the easiest verbal items, but they exist on real tests because skim-readers lose them: the eye catches "user research" and "at the start" and assembles a false match. Read the polarity words — "not only" — as carefully as the content words. In role terms, this is the guidance you would quote when a stakeholder proposes cutting research after discovery "because we've done that phase": the guidance anticipates and forbids precisely that reading.

**Question 2 (easy) — True, false, or cannot say**

Statement: "A team may roll out its public beta in phases if it publishes the phasing criteria."

- A) True
- B) False
- C) Cannot say
- D) Only with ministerial approval

**Correct answer: A**

**Explanation:** The passage permits phased rollout "to manage risk, provided the phasing criteria are published." The statement restates permission plus its condition accurately, so it is true. Option D imports an approval step the passage never mentions — a reminder that added conditions are as wrong as removed ones. Notice the structure worth internalising: permission-with-condition ("may X, provided Y"). When you relay such rules to your team, keep the condition welded to the permission — "we can phase, and that means publishing our criteria" — because a relayed rule that sheds its condition becomes misinformation with your name on it.

**Question 3 (moderate) — True, false, or cannot say**

Statement: "A service whose non-digital channel is free may not charge users during beta."

- A) True
- B) False
- C) Cannot say
- D) False, because beta services may always charge

**Correct answer: A**

**Explanation:** The rule: no fees during beta "unless the equivalent non-digital channel already charges one." Apply it to the statement's case: the non-digital channel is free, so the exception does not apply, and the prohibition stands — the service may not charge. The statement is true. This is a two-step verbal item: identify the general rule, then check whether the stated case falls inside the exception. The "unless" clause is where the reasoning happens; candidates who read only the main clause answer correctly here by luck, and then miss the mirror-image question where the exception does apply. Contractual and spend-control language leans heavily on "unless," "except," and "provided that" — as the point of contact for suppliers and a monitor of budgets, your reading of exception clauses has direct financial consequences.

**Question 4 (moderate) — Strongest inference**

Which of the following is best supported by the passage?

- A) Services with high staff turnover during beta may struggle to pass the live assessment.
- B) The performance targets for live are set by the live assessment panel.
- C) Phased rollout is mandatory during public beta.
- D) Beta services must be free for all users.

**Correct answer: A**

**Explanation:** Test each option. B misattributes: targets are "agreed at its beta assessment," not set at live. C converts a permission ("may use a phased rollout") into a mandate. D ignores the non-digital-channel exception — some beta services may lawfully charge. A requires a genuine inference but a modest one: the passage demands that a service "operate sustainably without the continued presence of its original developers"; a team that churned heavily during beta may find that knowledge left with the leavers, making that demonstration harder. The passage does not state this, but it supports it as a likely difficulty — and the question asks for the best-supported option, not a certainty. Calibrated inference is the skill: stronger than literalism (refusing all inference), weaker than speculation (option B's invented mechanism). It is also precisely the reading you perform on guidance when advising your team what an assessment panel will probe.

Passage for Questions 5–7 (a supplier letter):

"Further to our meeting of 3 March, we confirm the revised delivery approach. The data migration tooling will be delivered in two tranches: tranche 1 (extract and validation modules) by 30 April, and tranche 2 (load and reconciliation modules) within six weeks of tranche 1's acceptance. Please note that acceptance testing of each tranche is your responsibility and must complete within 10 working days of delivery; delays in acceptance will move tranche 2's delivery date accordingly. The revised approach does not change the contract value. Should your department require the optional archival module discussed at the meeting, this would be subject to a separate change request and quotation."

**Question 5 (easy) — Fact identification**

According to the letter, which of the following is the supplier's responsibility?

- A) Acceptance testing of each tranche
- B) Delivering the load and reconciliation modules in tranche 2
- C) Raising the change request for the archival module
- D) Completing acceptance within 10 working days

**Correct answer: B**

**Explanation:** Sort the letter's obligations by owner. The supplier: delivers tranche 1 by 30 April, and tranche 2 within six weeks of tranche 1's acceptance — option B is theirs. The department (you): acceptance testing of each tranche, within 10 working days of delivery — options A and D belong to your side, and the letter says so explicitly ("acceptance testing ... is your responsibility"). Option C is undetermined: the letter says the module "would be subject to a separate change request" without assigning who raises it. Obligation-sorting is the essential first read of any commercial letter, because every unnoticed obligation on your side is a schedule risk you now own — here, your acceptance-testing capacity in early May directly controls the supplier's tranche 2 clock, which is exactly the kind of dependency you would surface in sprint planning immediately.

**Question 6 (moderate) — True, false, or cannot say**

Statement: "If the department takes 15 working days to accept tranche 1, tranche 2 will be delivered later than it otherwise would have been."

- A) True
- B) False
- C) Cannot say
- D) False, because the contract value does not change

**Correct answer: A**

**Explanation:** Chain the letter's clauses. Tranche 2 is due "within six weeks of tranche 1's acceptance" — the clock starts at acceptance, not delivery. Acceptance "must complete within 10 working days," and "delays in acceptance will move tranche 2's delivery date accordingly." Taking 15 working days exceeds the 10-day window by 5 days, so acceptance happens later than the envisaged schedule, and tranche 2's date — anchored to acceptance — moves out with it. The letter states this consequence explicitly, so the statement is true. Option D confuses money with time: an unchanged contract value says nothing about dates. The practical import is sharp: your team's testing capacity is now on the critical path. A delivery manager reading this letter properly walks out with an action — book acceptance-testing capacity for the first week of May — and a risk-register entry, which is what managing external dependencies through careful reading looks like.

**Question 7 (moderate) — True, false, or cannot say**

Statement: "The archival module will cost more than the current contract value."

- A) True
- B) False
- C) Cannot say
- D) True, because change requests always add cost

**Correct answer: C**

**Explanation:** The letter says only that the archival module "would be subject to a separate change request and quotation." No price is stated; no comparison with the contract value is possible. It is tempting to reason commercially — separate quotations usually mean additional cost — but "usually" is experience, not text, and the statement makes a specific quantitative claim ("more than the current contract value") that no reading of the letter can verify. The answer is "cannot say," and option D's "always" is the giveaway of an overreach. The workplace discipline is identical: when your product owner asks "what would archival cost?", the only honest relay of this letter is "unpriced — it needs a change request and a quote." Inventing even a directionally sensible number at that moment would contaminate planning with fiction — and the assessment is testing whether you are the kind of reader who does that.

Passage for Questions 8–10 (an internal governance extract):

"The programme board considered the service's request to extend private beta by eight weeks. The board noted that the team's velocity had stabilised and that the outstanding accessibility issues, while reduced from eleven to four, included two assessed as high severity. The board agreed the extension in principle, subject to two conditions: first, that the two high-severity accessibility issues are resolved before any extension period begins; second, that the team presents a revised benefits profile at the next board. The board declined the associated request for two additional developers, citing the funding envelope, but invited a re-submission alongside the revised benefits profile."

**Question 8 (easy) — True, false, or cannot say**

Statement: "The board approved the eight-week extension unconditionally."

- A) True
- B) False
- C) Cannot say
- D) True in principle

**Correct answer: B**

**Explanation:** The board "agreed the extension in principle, subject to two conditions" — resolution of the high-severity accessibility issues before the extension begins, and a revised benefits profile at the next board. "Subject to two conditions" is the direct negation of "unconditionally," so the statement is false. Option D is a trap of half-reading: "in principle" appears in the text, but the statement's operative word is "unconditionally," which the text contradicts. Governance minutes turn on exactly these qualifiers — "agreed in principle," "subject to," "noted" versus "approved" — and relaying "the board approved our extension!" to the team, when two conditions gate it, sets up a painful correction later. Precision in the relay is the delivery manager's job; the minutes mean what they say, not what the team hopes.

**Question 9 (moderate) — True, false, or cannot say**

Statement: "The team will present a revised benefits profile at the next board."

- A) True
- B) False
- C) Cannot say
- D) True, because the board ordered it

**Correct answer: C**

**Explanation:** Careful: the board made a revised benefits profile a condition of the extension. Whether the team will present one depends on facts outside the passage — chiefly, whether the team pursues the extension at all. If the team abandons the extension request, the condition never binds. The passage states what must happen for the extension, not what will happen. So the statement, as a prediction of fact, cannot be verified: "cannot say." This is the subtlest true/false/cannot-say distinction — conditions versus predictions — and option D shows the failure mode: converting "condition of approval" into "order." Contract clauses, spend approvals, and assessment conditions all share this structure. The precise relay to your team is: "if we want the extension, we must resolve the two accessibility issues first and bring a revised benefits profile" — obligations attached to a choice, not commands in the void.

**Question 10 (moderate) — Purpose and accurate summary**

Which sentence best summarises the extract for your team's channel?

- A) "Board says no to everything — extension refused and no new developers."
- B) "Extension agreed in principle with two gates: fix the two high-severity accessibility issues before it starts, and bring a revised benefits profile to next board. Developer request declined for now but can be re-submitted with the benefits profile."
- C) "Great news — extension approved! Also we should probably look at accessibility at some point."
- D) "The board discussed our beta. More details to follow."

**Correct answer: B**

**Explanation:** Score each against fidelity, completeness, and usefulness. Option B captures every decision with its qualifiers: conditional agreement, both conditions stated as gates, the declined-but-reopenable developer request — and it is phrased so the team knows exactly what must happen next. Option A inverts the main outcome (the extension was agreed in principle, not refused) and misses the invitation to re-submit. Option C inflates the outcome, demotes a hard precondition to a vague aspiration, and would leave the team blindsided when the extension cannot start. Option D relays nothing. The pattern for summarising governance outcomes: every decision, every condition, every door left open — and no editorial optimism or pessimism. Managing expectations, as your **Communicating between the technical and non-technical** skill puts it, is mostly done in sentences like these; teams calibrate their morale and their plans on your summaries, so the summary must be true.

**Question 11 (challenging) — Condition stacking**

Passage: "Spend approval is delegated to service teams for individual items under £10,000, provided the cumulative delegated spend in the quarter remains under £40,000. Items between £10,000 and £50,000 require director approval. Any item connected to a live commercial dispute requires legal review regardless of value. Delegated approvals must be logged within five working days."

Your team wants to purchase £8,500 of load-testing services. This quarter the team has already used £34,000 of delegated spend. The supplier concerned is in a live commercial dispute with the department over an unrelated contract. What does the purchase require?

- A) Nothing beyond logging — it is under £10,000.
- B) Director approval only, because cumulative spend would exceed £40,000.
- C) Legal review, and director-level (non-delegated) approval because the cumulative delegated cap would be breached — plus logging if any delegated route is used.
- D) Legal review only; the item value is within delegation.

**Correct answer: C**

**Explanation:** Stack the conditions one at a time. Value test: £8,500 is under £10,000 — delegation is available on value alone. Cumulative test: £34,000 + £8,500 = £42,500, which breaches the £40,000 quarterly cap — so the delegated route fails, pushing the item to approval above the team (the passage's structure implies director-level handling for non-delegable items). Dispute test: the supplier is in a live commercial dispute, so legal review is required "regardless of value" — this condition operates independently and cannot be escaped by any approval route. Option A checks one condition of three. Option D checks two. Option B catches the cap but misses the dispute clause. The reading skill is refusing to stop at the first satisfied condition: rules with multiple gates require every gate checked, and the "regardless of value" phrase is the drafter's warning that this gate ignores the others. This is the verbal counterpart of the numeric variation-check question — and in the real workplace the two arrive together, in the same email, on a Friday afternoon.

**Question 12 (challenging) — Evaluating an argument in a report**

A report to you argues: "We should extend the contract with Supplier P. Their delivery this year has been strong: all six milestones were met. Switching suppliers would incur procurement costs and a three-month onboarding delay. Supplier Q, the likely alternative, has no experience with our department. Therefore extending with P is the only responsible option."

Which is the most accurate critical assessment of this argument?

- A) The argument is sound; six met milestones settle the matter.
- B) The argument offers relevant evidence for extension but overstates its conclusion: switching costs and P's record support extension, yet "only responsible option" ignores unexamined factors — P's pricing for the extension, market comparison, and whether Q's departmental inexperience actually matters for this work.
- C) The argument is worthless because it comes from someone who prefers P.
- D) The argument fails because milestone delivery is irrelevant to contract decisions.

**Correct answer: B**

**Explanation:** Separate the evidence from the conclusion's strength. The evidence is genuinely relevant: a clean milestone record, real switching costs, and an onboarding delay all legitimately favour extension. But the conclusion — "the only responsible option" — claims necessity, and the argument nowhere examines the considerations that could defeat it: what P proposes to charge for the extension (incumbents sometimes price in their advantage), whether the market offers materially better value, and whether Q's lack of departmental experience is relevant to this specific work or merely familiar-sounding. Option B credits the evidence while catching the overreach — the calibrated response. Option A mistakes relevant evidence for sufficient evidence. Option C commits the ad hominem error: motive does not invalidate evidence. Option D overcorrects into dismissing plainly relevant performance data. As a delivery manager you both read and write arguments like this — in your case for getting good value from contracts and knowing when to involve commercial specialists — and the professional standard is exactly option B's: state what the evidence supports, then name what remains unexamined before anyone signs.

### Preparation tips

- **Read the passage fully before the questions.** Question-first reading trains keyword hunting, which is precisely how condition words ("unless," "provided," "in principle," "regardless of value") get missed.
- **Underline qualifiers as you read.** Modality ("must," "may," "should"), conditions ("if," "unless," "subject to"), and scope ("all," "only," "each tranche") decide most answers.
- **Practise "cannot say" on real documents.** Take a governance minute or supplier email, write four statements about it, and classify them strictly. The undeterminable ones train the discipline tests reward most.
- **Distinguish conditions from predictions.** "Must do X to get Y" never means "will do X." This single distinction resolves the hardest true/false/cannot-say items.
- **Sort obligations by owner when reading commercial text.** Ours, theirs, unassigned — every unnoticed obligation on your side is a hidden schedule risk, in the test and in the contract.
- **Summarise real documents in two sentences, then check fidelity.** Every decision, every condition, every open door, no editorial spin. This is simultaneously test practice and the core writing skill of your role.

### Common pitfalls to avoid

- **Answering from professional experience instead of the passage.** Your commercial instincts ("separate quotes always cost more") are the leading cause of wrong "true" answers.
- **Shedding conditions in the relay.** "Agreed in principle, subject to..." is not "approved." "May, provided..." is not "can." Carry the qualifier or carry the blame.
- **Stopping at the first satisfied gate.** Multi-condition rules require every gate checked — especially clauses marked "regardless of."
- **Converting permissions into mandates** (or inferring mandates from conditions). "May phase" does not mean "must phase"; "condition of approval" does not mean "ordered."
- **Judging arguments by their source or their fluency.** Evaluate the evidence-to-conclusion gap; a well-written report can still overclaim, and a clumsy one can be right.
- **Summarising with optimism or pessimism.** Both distort. Fidelity first; encouragement can wrap an accurate summary, never replace it.

## Workplace job-specific situational judgement assessment

### About this assessment

A situational judgement test (SJT) presents realistic scenarios from the role and asks you to evaluate possible responses — most effective, least effective, best-and-worst pairings, or effectiveness ratings for each option. Responses are scored against the consensus of experienced practitioners and occupational psychologists about what works in the role, anchored to professional behaviours: user focus, honesty and transparency, team empowerment, early and proportionate escalation, inclusion, and sustainable delivery.

Typical format: online, 20 to 35 minutes, 10 to 20 scenarios, often untimed or generously timed because the construct is judgement, not speed. Unlike cognitive items, several options may be defensible; the scoring rewards recognising which is most effective, which is actively harmful, and which are merely mediocre.

Employers weight SJTs heavily for delivery managers because judgement is the role's irreducible core. You are accountable for the performance of the team — but you deliver through influence, facilitation, and coaching rather than authority over the work itself. Whether to intervene in a team conflict or let it resolve; whether a slipping date is a team conversation, a stakeholder message, or an escalation; how to respond when someone senior pressures the report — these calls, repeated daily, are the job. The SJT samples them.

At your level, expect scenarios about independent delivery and coordination: you run the team's world largely without supervision, you own the interfaces to product, stakeholders, suppliers, and governance, and you coach and mentor team members and others in Agile and Lean practice. The best answers consistently act early, involve the right people, keep information honest, and strengthen the team's own capability rather than substituting for it.

### How this assessment maps to your role

- **Team leadership scenarios** map to **Team dynamics and collaboration**: building motivated teams, recognising and dealing with issues, creating the environment for delivery, and getting the team makeup right for the situation.
- **Coaching scenarios** map to your accountability to coach and mentor both team members and others in Agile and Lean tools — the SJT tests whether you build capability or create dependence.
- **Escalation and blocker scenarios** map to **Maintaining delivery momentum**: addressing risks, issues and dependencies including where ownership exists outside the team, and choosing the escalation rung that resolves without inflaming.
- **Stakeholder and reporting scenarios** map to **Communicating between the technical and non-technical** and **Financial management**: managing expectations, hosting difficult discussions, reporting delivery honestly, and knowing how and when to escalate financial issues.
- **Process and improvement scenarios** map to **Making a process work** and **Agile and Lean practices**: challenging unnecessarily complicated processes, guiding teams through change, and encouraging experimentation and reflective practice.
- **Life cycle scenarios** map to **Life cycle management**: judging when a product should move phase, and ensuring development matches the standards each phase demands.

### Practice questions

**Question 1 (easy) — The failing new starter**

A developer who joined the team six weeks ago is visibly struggling: their work is regularly reworked by others, and two teammates have separately mentioned it to you. The developer seems unaware of the concern. What is the most effective response?

- A) Wait until the end of probation; the formal process will handle it.
- B) Have a prompt, private, specific conversation with the developer about what you are seeing, understand their view, and agree support — pairing, clearer expectations, or training — with a follow-up date.
- C) Quietly route all complex work away from them so the problem stops surfacing.
- D) Raise it in the team retro so everyone can give them feedback together.

**Correct answer: B**

**Explanation:** The governing principles are early, direct, kind intervention and genuine curiosity before conclusion. Option B addresses the issue while it is small, with the person, privately, and pairs candour with support — the developer may be missing context, drowning in an unfamiliar stack, or dealing with something outside work, and each cause implies a different remedy. The follow-up date converts good intentions into accountability. Option A outsources a leadership conversation to a bureaucratic deadline, wasting weeks of the developer's opportunity to improve and the team's patience. Option C hides the problem, caps the developer's growth, silently overloads others, and guarantees a harder conversation later. Option D ambushes a struggling person in a group setting — retros improve the system, not individuals' performance, and using them for the latter poisons their safety. Recognising and dealing with issues in the team is your named skill; the test is whether you deal with them at the human scale first.

**Question 2 (easy) — The optimistic status demand**

Your programme manager, preparing for a quarterly review, says: "I need your milestone to show green this week — the deputy director is presenting to the board." The milestone is genuinely amber: a dependency has slipped and recovery is possible but not assured. What is the most effective response?

- A) Report green; recovery is possible, so green is arguably true.
- B) Report amber with a crisp recovery narrative: what slipped, the recovery plan, the decision point at which it becomes red, and what help would accelerate it — and offer to brief the programme manager before the review.
- C) Report red to create pressure for help.
- D) Ask the product owner to make the call so it is not your name on it.

**Correct answer: B**

**Explanation:** Honest reporting with a forward story is the strongest pattern available. Option B keeps the status truthful — amber with a credible plan is respectable and boards know it — and does the programme manager a genuine favour: a briefed presenter with a recovery narrative looks better, not worse, than one whose green turns red a fortnight later in front of the same board. The offer to brief converts a compliance tussle into an alliance. Option A starts a debt that compounds: if recovery fails, the record shows you asserted green against known facts, and your future ambers will be read as reds. Option C corrupts the signal in the other direction — statuses are information, not leverage, and gaming them teaches everyone to ignore them. Option D abdicates an accountability that is squarely yours: providing delivery confidence, including uncomfortable confidence. Note what the best option adds beyond honesty: the decision point ("red if the credentials miss the 14th") makes the amber actionable rather than anxious.

**Question 3 (easy) — Coaching versus rescuing**

Your team's newest ceremony facilitator — a tester who volunteered to run retrospectives — is running a flat, awkward session. Energy is low, two people are on laptops, and a dominant voice is steering every topic. The tester glances at you. What is the most effective response in the moment?

- A) Take over the facilitation smoothly to save the session.
- B) Support without seizing: model participation from your seat — put your own laptop away pointedly, contribute, and offer one light assist ("Could we hear from folks who haven't spoken?") — then debrief generously with the tester afterwards, helping them design their next session.
- C) Let it fail completely so the lesson lands.
- D) Announce that retros will return to you until further notice.

**Correct answer: B**

**Explanation:** The tension is real: the session has value at stake, and so does the facilitator's development. Option B protects both — light-touch assists from a participant's chair (an inclusion question is the least intrusive rescue available) keep the session serviceable while leaving the tester visibly in charge, and the developmental payload is delivered afterwards, privately, framed around their next attempt. This is what coaching and mentoring team members means in practice: building the team's capability to run itself, which multiplies you; rescuing, which merely substitutes for them, subtracts. Option A saves twenty minutes and costs a facilitator — the tester learns that faltering means removal, and the team learns facilitation belongs to you. Option C sacrifices the team's time to a lesson that a debrief could teach more kindly. Option D converts one wobbly session into a permanent regression, publicly. The SJT pattern: options that build capability with a safety net beat both rescue and abandonment.

**Question 4 (moderate) — The supplier's slipping signal**

A supplier delivering a critical integration has given three consecutive weekly updates that are technically compliant but increasingly vague, and their lead engineer — previously in every call — has stopped attending. The contractual milestone is five weeks away. Your commercial colleague is on leave for a fortnight. What is the most effective response?

- A) Wait for the milestone; the contract will speak for itself if they miss.
- B) Request a working-level demonstration of current progress this week, name your observations factually to the supplier's manager ("three vague updates, lead engineer absent — help me understand where things stand"), brief your commercial colleague's cover, and record the pattern in the risk log.
- C) Email the supplier's account director threatening contract termination.
- D) Ask your developers to build a contingency version in parallel, without telling the supplier.

**Correct answer: B**

**Explanation:** Vague updates plus vanished expertise is a recognised early-warning signature, and five weeks is enough time to act but not to waste. Option B applies proportionate pressure through evidence: a working demonstration is the one update format that cannot be vague, the factual framing invites explanation rather than defensiveness (the engineer may be ill, or reassigned — which is itself a contractual conversation), and briefing the commercial cover plus logging the risk builds the record that later steps would need. This is taking responsibility for the supplier relationship — your **Commercial management** skill — while respecting its boundaries: pressure now, escalation ready. Option A converts an early warning into a milestone failure with five weeks of foregone options. Option C deploys the heaviest weapon on the thinnest evidence, likely without authority, and poisons a relationship that may only need managing. Option D spends real team capacity on secret duplication — and if discovered, hands the supplier a grievance and destroys the trust the recovery will need. Watch the escalation ladder: evidence, conversation, record, then commercial machinery — each rung earned by the one below.

**Question 5 (moderate) — Two strong engineers at war**

Your two most senior engineers have entrenched positions on a significant architectural choice. Debate has curdled: the last design session ended with sarcasm, the rest of the team has gone quiet, and work touching the disputed area is slowing. Both engineers are talented and neither is obviously wrong. What is the most effective response?

- A) Decide the architecture yourself to end the argument.
- B) Separate the dispute's technical and human layers: get the two to agree the decision criteria and a decision mechanism with a date (spike and measure, architecture review, or tech lead ruling), facilitate that process — and privately address the sarcasm and its effect on the team with each of them as a behaviour issue, whatever the technical outcome.
- C) Let them fight it out; conflict between experts is healthy.
- D) Move one of them to another team to dissolve the tension.

**Correct answer: B**

**Explanation:** Two problems are entangled, and the option that names this wins. The technical disagreement is legitimate and may even be valuable — but it currently lacks a resolution mechanism, so it recycles; agreeing criteria and a decision process with a date converts an identity contest into an evaluable question, which is how strong engineers can lose an argument without losing face. The behavioural layer — sarcasm, a silenced team, slowed work — is separately real and needs the private, specific conversation regardless of who turns out to be right. Option A resolves the question but not the conflict, overrides the team's technical ownership on a matter where you are not the expert, and teaches both engineers that deadlock summons a parental decision. Option C mistakes curdled conflict for creative conflict — the team's silence is the tell that safety has already been damaged, and understanding team dynamics means reading exactly that signal. Option D destroys team capability to avoid a conversation, and relocates the pattern rather than resolving it. Your role's language for this — recognising and dealing with issues, helping create the right environment — is precisely the two-layer work of option B.

**Question 6 (moderate) — The process you are told to add**

A central PMO instructs your team to complete a new 14-field weekly reporting template, most of which duplicates data already visible on the team's board and in existing reports. The team is irritated; the PMO analyst is firm ("everyone must comply"). What is the most effective response?

- A) Refuse: the team's time is too valuable for duplicate bureaucracy.
- B) Comply silently and absorb the cost forever.
- C) Comply initially while engaging the PMO constructively: understand what decisions the template feeds, demonstrate where existing data already answers them, and propose a lighter automated alternative — escalating the duplication cost through your management line if the constructive route stalls.
- D) Delegate the template to the newest team member and move on.

**Correct answer: C**

**Explanation:** This is your **Making a process work** skill in its purest form: identifying and challenging organisational processes that are unnecessarily complicated — where "challenge" is a verb of engagement, not defiance. Option C sequences it correctly: comply first (open non-compliance by one team invites a governance fight you will lose, and the PMO analyst is an instruction-carrier, not the decision-maker), then challenge the process on its own terms — every report exists to feed decisions, and showing that the decisions are already served by existing data is the argument that actually kills duplicate templates. The automated-alternative proposal gives the PMO a face-saving yes. The escalation clause matters too: if constructive engagement stalls, the cost (say, two hours weekly across every team in the programme) is a legitimate issue for your management line, raised with numbers. Option A wins a morning and loses the relationship — and probably the argument. Option B teaches the organisation that compliance is free, guaranteeing more templates. Option D quietly converts an organisational problem into a junior colleague's burden, which is both unkind and invisible — the worst combination.

**Question 7 (moderate) — Mid-sprint scope pressure from the product owner**

Your product owner, under pressure from their director, wants to inject a significant new feature into the current sprint, displacing committed work the team has half-finished. This is the third consecutive sprint they have done this. The team's morale and the sprint metrics are visibly degrading. What is the most effective response?

- A) Refuse all mid-sprint changes on principle; the sprint is sacred.
- B) Accept the change; the product owner owns priority.
- C) Handle the instance and the pattern separately: facilitate a quick trade-off decision on this feature with the team (what drops, what breaks, what it costs), then address the recurring pattern with the product owner directly — showing the three-sprint data on abandoned work and degraded flow, and jointly redesigning intake so genuine urgency has a route that does not shred every sprint.
- D) Tell the team to absorb the feature on top of existing commitments; morale will recover.

**Correct answer: C**

**Explanation:** Both single-note answers fail. Option A defends a ceremony against the business it serves — sometimes the director's urgency is real, and a delivery manager who cannot flex looks like an obstacle. Option B honours the product owner's authority over what but surrenders your accountability for how the team performs — and three sprints of data say the current how is destructive. Option C makes today's decision properly (the product owner chooses with the costs visible — trade-offs, not additions) and then does the real work: the pattern conversation, held with data rather than complaint. "In the last three sprints we have abandoned 31 points of half-done work; our cycle time has doubled" is a sentence a product owner under pressure can take to their director; "the team is unhappy" is not. The joint redesign — an expedite policy, a protected-capacity buffer, faster sprint cadence, or flow-based planning — turns adversaries into co-designers, which is what managing expectations and facilitating delivery flow jointly require. Option D is the burnout option: invisible overwork to reconcile irreconcilable commitments, the precise opposite of a sustainable pace.

**Question 8 (moderate) — The health check you don't like**

You run an anonymous team health check. Most dimensions are fine, but "psychological safety" and "learning" score notably low — which surprises and stings, because you pride yourself on both. A comment reads: "Disagreeing with the DM's process ideas doesn't feel worth the hassle." What is the most effective response?

- A) Treat the result as noise; anonymous surveys attract grumbling.
- B) Identify who wrote the comment so you can resolve it with them.
- C) Share the results with the team transparently, including the uncomfortable ones; name your own part without defensiveness ("this says pushing back on me feels costly — I want to change that"); invite concrete suggestions through channels that do not require confronting you; and change something visible, then re-measure.
- D) Run the health check again next month, hoping for better numbers.

**Correct answer: C**

**Explanation:** A low psychological-safety score is self-verifying: dismissing it (A) demonstrates the very unsafety it reports, and hunting the commenter (B) is the catastrophic version — it converts anonymity into a trap and would end honest feedback permanently. Option D is measurement without intervention, which changes nothing but the team's confidence in surveys. Option C is the behaviour the scores are asking for: transparency about uncomfortable data models the safety being requested; owning your part specifically ("pushing back on me feels costly") shows the message landed without triggering defence; offering low-confrontation channels (written suggestions, a facilitated session you leave, a trusted intermediary) respects that the deficit cannot be fixed by demanding people be brave; and the visible change plus re-measure closes the loop that makes feedback worth giving. This is your role summary's own language — identifying issues through health checks and helping stimulate the right responses, encouraging reflective practice — applied to the hardest subject available: yourself. SJT scoring consistently rewards leaders who metabolise criticism into visible change; it consistently punishes both dismissal and defensiveness dressed as diligence.

**Question 9 (challenging) — The phase-gate temptation**

Your service is due its beta assessment in three weeks. The team lead privately tells you that a load-testing shortcut means the performance figures in the assessment evidence pack reflect a smaller dataset than the pack implies — not fabricated, but flattering. Fixing the testing honestly would take two weeks and might produce worse numbers, risking the assessment date. The product owner says: "The pack is technically accurate. Let's not volunteer confusion." What is the most effective response?

- A) Proceed with the current pack; it is technically accurate and the date matters.
- B) Insist the evidence be corrected or clearly caveated, run the honest load tests now, and if the results or timing put the assessment at risk, tell the assessment team early and reschedule if needed — treating the standard as the point, not the gate.
- C) Proceed with the pack but mention the caveat verbally if an assessor happens to ask.
- D) Report the product owner to the SRO for attempted deception.

**Correct answer: B**

**Explanation:** Strip the euphemism: an evidence pack that "implies" a larger dataset than was tested is designed to mislead, and "technically accurate" is the tell — accuracy that requires the adjective is not the kind assessments exist to check. Option B holds the professional line with proportionate machinery: correct or caveat the evidence, generate honest data, and communicate early with the assessment team — who deal with rescheduling routinely and deal with discovered misrepresentation much less kindly. The deeper logic is your **Life cycle management** skill: ensuring the product is developed in line with the appropriate service standards for a phase means the assessment is a check on reality for the users' benefit, not an obstacle to sneak past; a service that passes on flattering performance data fails in production, publicly, later. Option A buys three weeks now at the price of the service's operational credibility and your own. Option C is the fig-leaf option — a caveat that depends on being asked is a caveat withheld. Option D rockets past every intermediate step: the product owner has made an argument, not committed an act; the first response to a bad argument is a better argument, and escalation becomes proportionate only if the misleading pack is actually forced through over your stated objection.

**Question 10 (challenging) — The finance discrepancy**

Reviewing the monthly finance report, you notice the supplier line shows £48,000 against a purchase order you believe was £36,000. Checking, you find a second, unfamiliar PO for £12,000 raised against your team's cost centre, approved by a programme-level manager, for "delivery support services" you cannot identify. What is the most effective response?

- A) Assume it is legitimate — programme managers can raise POs — and move on.
- B) Adjust your report to exclude the £12,000 so your team's figures look right.
- C) Query it factually and promptly: ask the approving manager what the PO covers, tell your finance partner you are verifying it, and document the exchange — escalating through your management line if the explanation does not resolve it.
- D) Raise a fraud allegation with internal audit immediately.

**Correct answer: C**

**Explanation:** An unexplained £12,000 on your cost centre is a discrepancy, and discrepancies have a spectrum of explanations — a miscoded but legitimate cross-charge, an agreed programme recharge nobody told you about, an administrative error, or (rarely) something worse. Option C responds to the discrepancy, not to a presumed explanation: a factual query to the approver ("this PO is on my cost centre and I can't identify the service — can you help me understand it?") resolves the innocent majority of cases in one email; looping in the finance partner keeps the monitoring record clean; documentation protects everyone; and the escalation clause covers the remainder. This is precisely your **Financial management** skill — monitoring cost and budget and understanding how and when to escalate: the trigger is an unexplained variance, the first action is verification, and the ladder runs query, finance partner, management line, and only then formal machinery. Option A abandons cost monitoring exactly when it is being tested. Option B is the actively dangerous choice: it falsifies your report to route around a discrepancy, converting someone else's possible error into your definite one. Option D deploys the gravest allegation available before asking a single question — if the PO is an unglamorous recharge, you have accused a colleague of fraud over an email's worth of due diligence.

**Question 11 (challenging) — The improvement that isn't landing**

Three months ago you introduced WIP limits and cycle-time tracking with a team that was initially willing. The metrics have genuinely improved — cycle time is down 30% — but grumbling has grown: two developers call the limits "micromanagement by dashboard," and this week the team simply ignored the limit twice. You believe the practice is working. What is the most effective response?

- A) Enforce the limits more firmly; the data proves they work.
- B) Drop the limits; a practice the team rejects is not worth the friction.
- C) Bring the tension to the team openly: show the cycle-time improvement, acknowledge the felt cost honestly, and ask the team to decide — keep, adapt, or replace the practice — while being clear about the outcome (flow) that any replacement must serve.
- D) Keep the limits but stop publishing the metrics so the dashboard resentment fades.

**Correct answer: C**

**Explanation:** The trap in this scenario is the true fact: the practice is working, and option A leans on that truth to justify imposition — but a practice held in place against a team's will is already failing on a longer clock; the ignored limits are the leading indicator, and enforcement converts passive resistance into a standing conflict about who owns the team's process. Option B swings to the other failure: abandoning a demonstrated improvement at the first friction teaches that grumbling beats evidence. Option C holds both truths — the data and the discontent — and puts the decision where your role summary says it belongs: you recognise, reflect and adapt when something does not work, you encourage experimentation, and you help the team find a process that works for them, with the outcome (flow) as the non-negotiable and the mechanism as the team's choice. Teams routinely redesign their way to something better than the original (per-person limits instead of column limits, or explicit expedite rules) precisely because the constraint became theirs. Option D treats information as the problem — hiding the metrics keeps the practice and discards the transparency that justified it, managing perception instead of reality. Coaching, in the end, is option C's shape: evidence on the table, ownership handed over, outcome held firm.

**Question 12 (challenging) — Choosing least effective: the failing dependency**

A platform team outside your control owns an API your team needs in four weeks. Their delivery manager has just told you, informally, that they are likely to be six weeks late. Your milestone, and two other teams' milestones, depend on it. Which response is the LEAST effective?

- A) Confirm the facts with the platform team, then promptly inform your product owner and the affected teams, and convene a joint conversation about re-sequencing, interim options (stubs, mocks, phased integration), and what help might accelerate the platform work.
- B) Update your plan and risk log, and re-plan the team's next sprints around work that does not depend on the API.
- C) Keep the information to yourself for now — it was informal, it may improve, and alarming stakeholders early could create pressure the platform team resents.
- D) Escalate the cross-team impact through the programme's governance route with the facts and options, so the priority call is made by people who own the trade-off.

**Correct answer: C**

**Explanation:** Least-effective format — three options are sound and complementary; find the harmful one. Option C sits on materially significant information because of its informality: but informal early warnings are the most valuable signal in dependency management precisely because they arrive while options still exist, and the correct response to informality is verification (option A's first move), not suppression. Silence for even a fortnight burns the response time of three teams, converts a manageable re-sequence into a crisis, and — when the delay surfaces anyway — reveals that you knew, which spends trust you will want later. The "pressure they resent" rationale inverts the real dynamic: platform teams resent late-discovered fury far more than early structured help. Options A, B, and D are the healthy triad in sequence: verify and communicate (A), adapt what you control (B), and route the cross-team trade-off to its legitimate owners (D) — which is exactly your skill definition of addressing dependencies where ownership exists outside the team. If you hesitated between C and D, note the difference: D moves information toward the people who can act on it; C moves it away from everyone. In delivery, information ages like fish — the least effective option is always the one that stores it.

### Preparation tips

- **Anchor on the behaviours, not the personalities.** Honest information flow, early action, team empowerment, proportionate escalation, sustainable pace, inclusion. Score each option against these before choosing.
- **Use the two-layer check.** Many scenarios entangle a technical/process problem with a human one (Questions 5, 8, 11). The best option usually addresses both, separately and appropriately.
- **Practise the escalation ladder consciously:** direct conversation → evidence and record → involve the natural owner (product owner, commercial, finance) → management line → formal governance. The best option is usually the lowest rung that actually resolves the issue; the worst options skip rungs in either direction.
- **Interrogate the flattering option.** Options that protect appearances — yours, the team's, the report's — are systematically penalised. If an option's main benefit is looking better, discard it.
- **Read the stem twice for most/least polarity.** The least-effective format plants three good options as distractors; polarity misreads are the cheapest marks lost on any SJT.
- **Debrief against reality.** For each practice scenario, recall the nearest real situation you have faced and compare what you actually did. The gap, either direction, is your development plan.

### Common pitfalls to avoid

- **Choosing decisive-looking drama.** Terminations threatened, decisions seized, formal allegations fired first — the assertive-sounding option is usually the over-escalation. Proportion beats theatre.
- **Choosing conflict-avoidant patience.** "Wait and see" scores badly whenever the scenario contains a live signal — vague updates, an unexplained PO, a struggling colleague. Patience with a signal is neglect.
- **Solving people problems with process, or process problems with pressure.** Match the remedy to the layer: behaviour conversations for behaviour, mechanism design for mechanism.
- **Rescuing when the moment calls for coaching.** Options where you take over — facilitation, decisions, the work itself — trade the team's growth for your comfort, and the scoring knows it.
- **Sitting on information to manage others' feelings.** Early, verified, structured communication of bad news is the single most consistently rewarded behaviour in delivery SJTs.
- **Letting a true fact justify a wrong move.** "The metrics improved" (Q11) and "the pack is technically accurate" (Q9) are both true — and both are deployed in-scenario to defend the ineffective option. Truth of a premise is not effectiveness of an action.

## Conclusion

Congratulations on working all the way through this guide — that was a demanding set of exercises, and completing them properly is itself evidence of the disciplined, reflective practice that distinguishes strong delivery managers.

Consider what you have covered. In the cognitive section, you read flow data for bottleneck signatures, cross-checked statuses against their own evidence, applied multi-constraint rules exhaustively, separated measurement changes from performance changes, and prioritised by cost of delay rather than seniority or noise. In the numeric section, you worked run rates, net drain rates, weighted team costs, committed-versus-actual budgets, and percentile-based commitments — with every step written out, because the method under pressure is the skill. In the verbal section, you practised holding the line between what a document states, implies, and leaves unsettled: conditions welded to permissions, governance qualifiers carried intact, arguments credited for their evidence and challenged for their overreach. And in the situational judgement section, you rehearsed the real weight of the role: honest ambers with recovery narratives, coaching instead of rescuing, pattern conversations held with data, evidence packs kept honest, and information moved promptly toward the people who can act on it.

None of this was generic test technique. Every scenario was a tidied version of the situations your accountability for team performance already generates — which means the practice pays twice: in any formal assessment you sit, and in the daily quality of your boards, forecasts, reports, and judgement calls.

Three suggestions for what to do next. First, space the practice: return to your weakest section in a fortnight and attempt the questions cold; retention lives in the second pass. Second, move the techniques into your actual artefacts this week — read your own dependency register the way you read Question 7's, test your next status report for internal consistency, and try the two-layer check on a live team tension. Third, teach it: coaching others is in your role summary, and explaining to a newer delivery manager why the median beats the mean for cycle times, or why "agreed in principle" is not "approved," will consolidate your own command of it faster than any re-reading.

Finally, keep the assessments themselves in proportion. They sample your thinking on one day, through one format; they do not measure your relationships, your resilience, or the trust your teams place in you — and every capability they do measure is trainable, as you have just demonstrated by training it. The path from here — senior delivery manager, head of delivery — runs on exactly the habits you have been practising: honest numbers, exact reading, early conversations, and judgement that serves users and teams over appearances.

Good luck with your assessment. On the evidence of the effort you have just put in, you will be well prepared — and your team is fortunate to have a delivery manager who takes their own development this seriously.
