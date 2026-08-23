# Principal DevOps Engineer (Management) - Psychometric Assessment Resources

## Introduction

Welcome. This guide is written for you as a principal DevOps engineer in the management track of the UK Government Digital and Data profession. You lead and plan development across large or multiple teams and define the strategic vision for delivery. Your role summary names identifying, testing and championing the adoption of emerging technologies; ensuring that security, stability and capacity are embedded in the development and deployment of services; developing a team's capability by rewarding high performers; shaping career paths and recruiting the right talent; and identifying skills gaps and important dependencies within technical teams.

The skills attached to the level widen that further. You lead policy and strategy for service and capacity management. You set the strategy and manage resource allocation for solution development programmes, working with client functions to establish business requirements and to initiate and lead those programmes. You review the system designs of others to ensure appropriate technology selection, efficient use of resources and sound integration. And you lead others in applying modern development standards and information security practices.

The distinctive thing about DevOps at this level is that your work is mostly invisible when it succeeds. Nobody notices a deployment pipeline that does not break, an environment that is always available, a capacity plan that quietly absorbed a peak, or a security control that stopped something. What gets noticed is the outage — which means a large part of your job is making the case for work whose value is measured in things that did not happen.

The second distinctive thing is that you sit between development and operations in an organisation where those functions frequently have different incentives, different reporting lines and different definitions of success. A great deal of what you do is resolving that tension structurally rather than mediating it case by case.

You may be preparing for a formal assessment, or you may want to re-examine judgement that has become fluent. Fluency is worth checking, because feedback loops on platform and process decisions run in years.

The document has four assessment sections — cognitive, numeric reasoning, verbal reasoning and situational judgement — each with an overview, a mapping to your named skills, twelve practice questions with full explanations, preparation tips and common pitfalls.

Answer before reading, and note where you were fast.

Let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive assessment measures the reasoning your role demands, presented through role-realistic material. At principal level on the management track that means incident evidence, platform and pipeline design, capacity strategy, resource allocation and the design reviews you conduct on other people's work.

The format is typically fifteen to thirty minutes online, covering deduction, pattern recognition, error checking, prioritisation and applied problem solving, scored against a norm group of comparable seniority.

Three things distinguish this section at your level.

The first is that reliability problems are almost always about the system rather than the component. A service that fails every third month with a different proximate cause has one underlying property — insufficient isolation, unbounded resource use, or no back-pressure — and enumerating causes will not find it.

The second is that automation changes the shape of risk rather than removing it. An automated deployment removes human error from each deployment and creates the possibility of a single mistake propagating everywhere in ninety seconds, and the design question is what bounds the blast radius.

The third is that you spend a lot of time reviewing others' designs, where the useful skill is finding the assumption that has not been stated rather than the flaw that has been described.

### How this assessment maps to your role

- **Systemic failure analysis** maps to **Service support** and **Availability and capacity management**.
- **Design review** maps to **Systems design**, where you review others' designs.
- **Risk reasoning about automation** maps to **Information security** and embedding stability in deployment.
- **Strategy and allocation** map to **Development process optimisation**.
- **Capability and dependency reasoning** maps to identifying skills gaps and important dependencies.
- **Technology evaluation** maps to identifying, testing and championing emerging technologies.

### Practice questions

**Question 1 (easy) — Deduction from a deployment rule**

Your policy states: "A change may be deployed to production without a change record only where it is an automated rollback to the previously deployed version." A change was deployed with no change record. Which must be true?

- A) The policy was breached.
- B) It was an automated rollback.
- C) Either it was an automated rollback to the previously deployed version, or the policy was breached.
- D) The change should be reverted.

**Correct answer: C**

**Explanation:** A rule with an exception, plus a fact silent on the exception, gives only the disjunction. Options A and B each pick a branch. Option D prescribes an action rather than stating what must be true. The operational corollary is worth noting: if automated rollbacks are indistinguishable from unrecorded deployments in your audit trail, the policy is unenforceable, and that is a defect in a policy you own.

**Question 2 (easy) — Blast radius**

A team proposes fully automated deployment to all production regions simultaneously, replacing a manual region-by-region process. What is the strongest observation?

- A) Adopt it; automation reduces human error.
- B) It removes per-deployment human error and creates the possibility of a bad change reaching every region in one action, so the automation is only an improvement if it is paired with something that bounds the damage — staged rollout across regions, automated health checks between stages, and automatic rollback on failure.
- C) Reject it; manual gates provide safety.
- D) Automate it but keep a manual approval step.

**Correct answer: B**

**Explanation:** Automation is not safer or less safe in itself; it changes the distribution of outcomes, trading many small human errors for the possibility of one large uniform one. Option B names the three controls that make the trade favourable, and staged rollout with health-gated progression is what converts simultaneous deployment into something safer than the manual process it replaces. Option D is the common compromise and it reintroduces the human error while keeping the simultaneity, which is the worst combination. Option A takes the benefit without the design. Option C defends manual gates whose main safety property is slowness.

**Question 3 (moderate) — Recurring failures with different causes**

A platform has had four significant outages in a year, each with a different proximate cause: a certificate expiry, a full disk, a misconfigured limit and a dependency timeout. What is the strongest analysis?

- A) Four unrelated incidents; fix each cause.
- B) Four different proximate causes with the same consequence suggests a shared property — most likely that these conditions are not detected before they cause an outage — so the useful question is why a certificate approaching expiry, a disk approaching full and a limit set wrongly all first became visible as user-facing failures.
- C) The platform needs more monitoring.
- D) The team needs better operational discipline.

**Correct answer: B**

**Explanation:** The causes are unrelated and the pattern is not: each is a condition that develops gradually and observably before it fails, and in all four cases nobody saw it coming. That is a single systemic property — the absence of leading indicators and alerting on approach to a threshold — with one fix that covers all four and the next four as well. Option C is directionally right and unspecific; "more monitoring" often means more alerts on symptoms, which would not have helped here. Option A treats a pattern as coincidence. Option D blames people for not noticing what nothing was measuring.

**Question 4 (moderate) — Reviewing another team's design**

A team submits a design for review. It is thorough and well argued. What is the most useful thing to look for?

- A) Technical errors in the described approach.
- B) The assumptions the design does not state — expected volumes, what happens when a dependency is slow rather than down, who operates it at 3am, how it is rolled back — because a thorough design usually has correct reasoning from premises nobody has written down, and the premises are where the risk is.
- C) Whether it follows the organisation's standards.
- D) Whether the technology choices are appropriate.

**Correct answer: B**

**Explanation:** Your role names reviewing others' designs, and a well-argued design has usually already had its explicit reasoning checked by its authors. The value you add is in the unstated: a design that is correct at 200 requests a second and was never told it will see 2,000; a failure mode assumed to be binary; an operational burden nobody has agreed to carry. Option B lists the four that recur most. Options C and D are genuine review criteria and both are usually addressed in a thorough submission — they are the checks, not the insight.

**Question 5 (moderate) — Capacity strategy**

You are setting capacity policy across a portfolio of services. What is the strongest basis?

- A) A standard utilisation target that all services must stay below.
- B) A requirement that each service states its peak factor and its failure headroom — what utilisation looks like at peak with one instance lost — because a single utilisation target means nothing across services with different load profiles, and the number that predicts outages is headroom at peak, not average utilisation.
- C) Automatic scaling for all services.
- D) A standard over-provisioning factor.

**Correct answer: B**

**Explanation:** Average utilisation is the number people report because it is easy, and it is close to uninformative: a service at 40% average with a peak factor of 3 is in trouble, and one at 70% with a flat profile is fine. Option B asks for the two figures that actually predict failure and puts the reasoning in the hands of the teams who know their load shapes. Option C is a useful mechanism and not a policy, and auto-scaling has its own limits — it does not help when the constraint is a database connection pool or a licence. Options A and D apply uniform numbers to non-uniform services.

**Question 6 (moderate) — A skills dependency**

You identify that one engineer is the only person who understands the deployment pipeline for four critical services. What is the strongest response?

- A) Document the pipeline.
- B) Reduce the dependency by having someone else do the work with them — running deployments, handling an incident, making a change — because documentation captures what the person thought to write down and the risk is in what they do without thinking, which only transfers through doing.
- C) Recruit a second pipeline specialist.
- D) Simplify the pipeline.

**Correct answer: B**

**Explanation:** Your role names identifying important dependencies within technical teams, and the remedy for tacit knowledge is practice rather than prose. Documentation is genuinely useful and reliably incomplete in exactly the places that matter at 3am, because the expert does not know which of their actions are non-obvious. Option B transfers capability by exercising it. Option D is often the best long-term answer — a pipeline only one person understands is usually too complicated — and it is slower. Option C adds a person to a system that would still have concentrated knowledge, now in two heads.

**Question 7 (harder) — An emerging technology**

You believe a new deployment technology would substantially improve your platform. What is the strongest way to champion it?

- A) Build the case and propose adoption.
- B) Run a real trial with a pre-agreed definition of failure, on a genuine workload rather than a demonstration, and publish the outcome either way — because a champion whose evaluations always succeed is discounted, and the credibility to get the next adoption approved is worth more than this one.
- C) Pilot it with one team and expand if it goes well.
- D) Wait until it is more established.

**Correct answer: B**

**Explanation:** The two load-bearing words are "pre-agreed" and "either way". A pilot without a prior failure criterion nearly always succeeds, because the people running it want it to and there is always a favourable reading available. Option B makes a negative result possible, which is the only thing that makes a positive result informative. Option C is the standard approach and its weakness is precisely the missing criterion. Option A advocates ahead of evidence. Option D declines the role your summary names.

**Question 8 (harder) — Competing explanations under incident conditions**

A service degrades sharply. Two changes went out in the last hour: a configuration change to connection limits, and a new version of a shared library. What is the strongest sequence?

- A) Revert the configuration change; it is the more likely cause.
- B) Revert both if both are cleanly revertible and restore service first, then identify the cause from the artefacts in a safe environment — because during a degradation the goal is restoration rather than diagnosis, and reverting one of two candidates has an even chance of leaving the problem live while consuming the time you had.
- C) Roll back the library version.
- D) Increase the connection limits further.

**Correct answer: B**

**Explanation:** Restoring service and diagnosing are different activities and doing them in the wrong order costs users. Option B reverts everything reversible, which returns to a known-good state, and preserves the ability to diagnose afterwards from logs, metrics and the artefacts themselves. The condition matters: "if both are cleanly revertible" — a library change usually is, and a configuration change usually is, but if either has side effects the calculation changes and you need to know that before acting. Options A and C guess. Option D changes a parameter during an incident on an unconfirmed diagnosis.

**Question 9 (harder) — A process metric that will be gamed**

You are considering measuring teams on deployment frequency, with a target of increasing it. What is the strongest observation?

- A) It is a good measure; frequent deployment correlates with high performance.
- B) The correlation is real and using it as a target creates pressure on the cheapest thing to change, which is how work is split into deployments rather than how quickly it reaches users — so the measure will rise without the underlying capability improving, and pairing it with lead time and change failure rate makes it much harder to move without real improvement.
- C) It should not be measured.
- D) It should be combined with other measures.

**Correct answer: B**

**Explanation:** Deployment frequency is a genuinely good indicator and a poor sole target, because splitting one deployment into four is far easier than deploying four times as much value. Option B names the gaming route and the specific remedy, which is why these metrics are conventionally used as a set — lead time and change failure rate are much harder to improve by re-slicing the same work. Option D is the same idea without the mechanism, which matters because "combine with other measures" could mean combining with equally gameable ones. Option C discards a useful indicator.

**Question 10 (harder) — Security embedded in delivery**

You want security checks embedded in the deployment pipeline rather than performed as a separate review. What most determines whether this works?

- A) Choosing the right scanning tools.
- B) The signal-to-noise ratio of what the checks report — a pipeline check that produces many findings teams cannot act on gets bypassed within a month, so the design question is which classes of finding block a deployment and which are reported without blocking.
- C) Making the checks mandatory.
- D) Training teams in secure development.

**Correct answer: B**

**Explanation:** Automated security checks fail for one dominant reason: they flood teams with findings that are unactionable, unreachable in practice, or in third-party dependencies with no fix available, and a check that blocks deployment on those gets an exemption, an override or a quietly disabled step. Option B identifies the actual design decision, which is triage — a small set of high-confidence findings block, everything else is visible but non-blocking. Option C is what produces the bypass. Option A matters less than how the output is handled. Option D is valuable and separate.

**Question 11 (harder) — Allocating a scarce platform team**

Three programmes need platform work next quarter and you can serve roughly two. What is the strongest basis for deciding?

- A) The programme with the largest claimed benefit.
- B) What each loses by waiting a quarter, and whether any of the three could be served by something self-service rather than by the team — because the highest-value platform work is usually the piece that removes the need for the platform team to be involved next time.
- C) First come, first served.
- D) Split the team across all three.

**Correct answer: B**

**Explanation:** Two criteria, and the second is the one specific to a platform function. Cost of delay is the general allocation criterion. The self-service question is what stops a platform team becoming a permanent bottleneck: if one of the three requests is a variant of something requested repeatedly, building the self-service version serves that programme and every future one. Option D is the fairness reflex and serves three programmes badly while the team loses time to context switching. Option A trusts self-reported benefits from parties competing for the resource. Option C ignores all available information.

**Question 12 (harder) — Rewarding high performers**

You want to recognise a team member whose work on reliability has been exceptional. What is the strongest approach?

- A) Give them public recognition at a team event.
- B) Make the impact visible in concrete terms — what changed, what stopped happening, what it was worth — and pair recognition with something that has durable value to them, such as scope, a route to the next role, or a conference talk, because reliability work is invisible by nature and the recognition that matters most is that its value was seen and counted.
- C) Nominate them for an award.
- D) Give them a bonus if one is available.

**Correct answer: B**

**Explanation:** Reliability work has a specific recognition problem: its output is the absence of events, so it does not appear in delivery metrics and the person doing it often suspects nobody noticed. Option B addresses that directly by making the impact legible, which is worth more than the recognition itself — and then attaches something with a future in it. Options A, C and D are all reasonable and are moments rather than trajectories; a bonus is spent, and scope or a route to the next role is not. Your role names rewarding high performers and shaping career paths, and the strongest version connects the two.

### Preparation tips

- **Ask what bounds the blast radius before approving automation.**
- **Read four outages with four causes as one detection failure.**
- **Look for the unstated assumptions in a thorough design.**
- **Ask for peak factor and failure headroom, not average utilisation.**
- **Transfer tacit knowledge by doing, not by documenting.**
- **Set a failure criterion before piloting a technology.**
- **Ask how a metric would be gamed before making it a target.**
- **Design pipeline security checks around what blocks and what does not.**

### Common pitfalls to avoid

- **Adding a manual approval to a simultaneous automated deployment.**
- **Treating unrelated proximate causes as unrelated incidents.**
- **Reverting one of two candidate changes during a degradation.**
- **Setting a uniform utilisation target across dissimilar services.**
- **Answering a single-person dependency with documentation alone.**
- **Blocking deployments on low-confidence security findings.**
- **Splitting a platform team across three programmes.**
- **Recognising invisible work with a moment rather than a trajectory.**

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment tests whether you can reach a defensible conclusion from operational and financial data at speed. At principal level on the management track the data is availability and error budgets, pipeline throughput, infrastructure cost, capacity models and the business cases attached to platform investment.

The format is typically fifteen to twenty-five minutes with a calculator, mixing computation with interpretation. Interpretation carries more weight at your level, because you are usually the person expected to notice that a number does not mean what the slide says it means.

Three habits are worth naming.

The first is that availability arithmetic composes multiplicatively across serial dependencies, which produces figures people find surprising, and you are expected to know them before the design is committed.

The second is that infrastructure cost scales with provisioned capacity rather than with used capacity, so a utilisation figure and a cost figure are different conversations.

The third is that error budgets are consumed over time, so the meaningful measure is burn rate against elapsed window rather than a total compared to a threshold.

### How this assessment maps to your role

- **Availability and error budgets** map to **Availability and capacity management**, where you lead policy and strategy.
- **Capacity modelling** maps to embedding capacity in development and deployment.
- **Pipeline metrics** map to **Development process optimisation**.
- **Infrastructure cost** maps to managing resource allocation.
- **Security risk quantification** maps to **Information security**.
- **Integration volumetrics** map to **Systems integration**.

### Practice questions

*Table 1 — Platform components, measured availability last quarter*

| Component | Availability | In request path |
|---|---|---|
| Load balancer | 99.99% | Yes |
| Auth service | 99.95% | Yes |
| Application tier | 99.9% | Yes |
| Cache | 99.7% | Yes (fail-open) |
| Primary database | 99.95% | Yes |

**Question 1 (easy) — Availability in minutes**

How much downtime does 99.9% availability allow in a 30-day month?

- A) About 22 minutes
- B) About 43 minutes
- C) About 4.3 minutes
- D) About 2 hours

**Correct answer: B**

**Explanation:** 43,200 minutes × 0.001 = 43.2 minutes. Worth holding instantly at your level: 99.9% ≈ 43 minutes a month, 99.95% ≈ 22, 99.99% ≈ 4.3, 99.5% ≈ 3.6 hours. You will be asked in meetings whether a proposed target is achievable, and the answer often turns on whether one bad deployment consumes the whole month's budget.

**Question 2 (easy) — Least available component**

Which component contributes most to unavailability?

- A) Load balancer
- B) Cache
- C) Application tier
- D) Auth service

**Correct answer: B**

**Explanation:** The cache at 99.7% is the least available, roughly 2.2 hours of downtime a month. Note the qualifier in the table, though: the cache is marked fail-open, meaning requests proceed without it. So it is the least available component and, if fail-open genuinely works, it is not in the critical path for availability — which is exactly the distinction the next question tests.

**Question 3 (moderate) — Composed availability**

What is the approximate composed availability of the four components that are not fail-open?

- A) About 99.79%
- B) About 99.9%
- C) About 99.5%
- D) About 99.95%

**Correct answer: A**

**Explanation:** Multiply the four hard dependencies: 0.9999 × 0.9995 × 0.999 × 0.9995 = 0.99790, about 99.79%, or roughly 91 minutes of downtime a month. Serial dependencies multiply, so the composed system is worse than any individual component — which surprises people every time and is why the calculation belongs in a design review rather than in a post-incident report. Note the cache is excluded because it fails open; if that fail-open path were untested, the real figure would be 0.9979 × 0.997 = 99.49%, and the difference between those two numbers is entirely a matter of whether someone has verified the behaviour.

**Question 4 (moderate) — Error budget burn**

A service has a 99.95% monthly target. Eighteen days into a 30-day month it has used 17 minutes of downtime. Is it on track?

- A) Yes; the budget is about 22 minutes and it has used 17.
- B) No — the budget is about 21.6 minutes, and 17 minutes used in 18 days is a burn rate of 0.94 minutes a day, projecting to about 28 minutes over the month, which overshoots by roughly 30%.
- C) Yes, comfortably.
- D) There is not enough information.

**Correct answer: B**

**Explanation:** 43,200 × 0.0005 = 21.6 minutes for the month. 17 minutes in 18 days is 0.944/day; over 30 days that projects to 28.3 minutes. The service is 60% through the month and has consumed 79% of the budget. Options A and C compare a running total to a threshold, which is the standard error-budget mistake — a budget spent over time has to be measured against elapsed proportion, and by that measure this one is already off track.

*Table 2 — Deployment pipeline, monthly figures across four teams*

| Team | Deployments | Mean lead time (hours) | Change failure rate | Mean time to restore (min) |
|---|---|---|---|---|
| North | 62 | 4.2 | 6% | 22 |
| South | 18 | 31.0 | 17% | 96 |
| East | 44 | 8.5 | 9% | 41 |
| West | 9 | 74.0 | 22% | 180 |

**Question 5 (easy) — Reading the table**

Which team has the highest change failure rate?

- A) South
- B) West
- C) East
- D) North

**Correct answer: B**

**Explanation:** West at 22%, ahead of South at 17%. West also has the fewest deployments, the longest lead time and by far the longest restore time — the four measures move together, which is the well-documented pattern: teams that deploy rarely deploy large changes, which fail more often and take longer to diagnose because more changed at once.

**Question 6 (moderate) — Failed deployments per month**

Approximately how many failed deployments occur across all four teams each month?

- A) About 9
- B) About 13
- C) About 20
- D) About 6

**Correct answer: B**

**Explanation:** North 62 × 0.06 = 3.7; South 18 × 0.17 = 3.1; East 44 × 0.09 = 4.0; West 9 × 0.22 = 2.0. Total ≈ 12.8, so about 13 a month. Note that North has the most failed deployments in absolute terms despite the lowest failure rate, simply because it deploys most — which is why the rate rather than the count is the meaningful comparison, and why a target on the count would push teams towards deploying less.

**Question 7 (moderate) — Downtime from failures**

Approximately how many minutes of restoration time does West consume per month, and how does it compare with North?

- A) 360 minutes against 81 — West spends over four times as long restoring, despite deploying seven times less often.
- B) 180 minutes against 22.
- C) 360 minutes against 220.
- D) 90 minutes against 81.

**Correct answer: A**

**Explanation:** West: 9 deployments × 22% = 2.0 failures × 180 minutes = 356, about 360 minutes. North: 62 × 6% = 3.7 failures × 22 minutes = 82, about 81 minutes. So West spends roughly 4.4 times as long in a degraded state while deploying a seventh as often. This is the arithmetic that answers the objection that frequent deployment is risky — the data says the opposite, and being able to produce it quickly is worth more than the argument.

**Question 8 (harder) — Infrastructure cost and utilisation**

A service runs 40 instances at £120 each per month, averaging 30% CPU. A proposal is to reduce to 24 instances. What is the strongest assessment?

- A) It saves £1,920 a month and utilisation rises to 50%, which is still comfortable.
- B) It saves £1,920 a month and the relevant check is peak behaviour, not average — at 30% average with an unknown peak factor, 24 instances could be over capacity at peak, and the calculation needed is peak load across 23 instances, allowing for one failure.
- C) It saves £1,920 and should be adopted.
- D) It saves £768 a month.

**Correct answer: B**

**Explanation:** The saving is 16 × £120 = £1,920 a month, and the arithmetic is the easy part. Option A computes the new average utilisation correctly — total work is 40 × 30% = 1,200 percentage-points, over 24 instances is 50% — and then treats average as the criterion, which is the error. If the peak factor is 2, peak on 24 instances is 100% with no headroom at all, and losing one instance at peak puts the remaining 23 over 104%. Option B asks for the figure that decides it. Right-sizing on average utilisation is one of the more reliable ways to cause an outage while reporting a cost saving.

**Question 9 (harder) — Payback on pipeline work**

Reducing South's lead time would need about four weeks of one engineer's time. South's 18 monthly deployments each wait an average of 31 hours, of which an estimated 24 hours is queueing. What is the strongest framing?

- A) The saving is 18 × 24 = 432 hours a month, so it pays back immediately.
- B) 432 hours a month of elapsed waiting is not 432 hours of engineer time — work waits while people do other things — so the honest case rests on faster feedback, smaller changes and a lower failure rate rather than on recovered hours, and stating it as recovered hours will be challenged and lose.
- C) Four weeks is too much for one team.
- D) The saving cannot be quantified.

**Correct answer: B**

**Explanation:** This is the commonest overstatement in pipeline business cases and it is worth getting right, because it is easily refuted and taking it into a meeting damages an argument that is otherwise strong. Elapsed queueing time is mostly not lost engineer time; people work on other things while a change waits. The real benefits are faster feedback while context is fresh, smaller batches, and the failure-rate improvement visible in Table 2's correlation between lead time and change failure rate. Option B makes the defensible case. Option D gives up on quantification that is available in the failure and restore figures.

**Question 10 (harder) — Interpreting a change**

After introducing automated canary deployments, change failure rate fell from 12% to 5% and mean lead time rose from 6 hours to 9 hours. What is the strongest interpretation?

- A) A clear success; failures more than halved.
- B) A favourable trade to assess rather than a clear win — failures fell by 58% at the cost of 50% longer lead time, and whether that is worth it depends on what a failure costs against what three extra hours of feedback delay costs, which for most services favours the canary but should be stated rather than assumed.
- C) A failure; lead time is a key metric.
- D) The two are unrelated.

**Correct answer: B**

**Explanation:** Both numbers moved and reporting only the favourable one is the specific habit this item tests. Option B does the comparison and states the criterion, which is the relative cost of a production failure against three hours of delayed feedback — for a public service handling money or benefits, that comparison heavily favours the canary, and saying so explicitly is more persuasive than presenting one number. Option A hides half the result. Option C inverts the same error. Option D denies a causal link that the mechanism plainly supplies.

**Question 11 (harder) — Capacity for a new integration**

A new integration will process 3.2 million records a night in a 5-hour window. Each worker handles 45 records per second. How many workers are needed, with no headroom?

- A) About 4
- B) About 20
- C) About 8
- D) About 45

**Correct answer: A**

**Explanation:** The window is 5 × 3,600 = 18,000 seconds. Required throughput: 3,200,000 / 18,000 = 178 records per second. At 45 per worker: 178 / 45 = 3.95, so 4 workers with no headroom at all — which means any worker failure, any slow period, or any growth in volume breaks the window. A sensible provision would be 6, giving room for one failure and roughly 35% volume growth. The point of the item is that this calculation belongs at design time, and the commonest failure is discovering it during the first full-volume run.

**Question 12 (harder) — Quantifying a reliability investment**

A proposed resilience change costs £180,000 to build and £30,000 a year to run. It would prevent an outage class that has occurred twice in three years, each time costing an estimated £400,000 in lost processing and recovery. What is the strongest analysis?

- A) Adopt it; £400,000 exceeds the cost.
- B) The expected annual loss is about £267,000 (two events in three years at £400,000), against £30,000 annual running cost and a £180,000 one-off — so it pays back within the first year on expected value, though both the frequency and the impact are estimates and the case should say so.
- C) Reject it; £180,000 is a large capital cost.
- D) There is not enough information.

**Correct answer: B**

**Explanation:** Two events in three years is 0.67 events a year; at £400,000 each that is £267,000 expected annual loss. Against £180,000 build plus £30,000 a year, the investment is recovered inside the first year and saves roughly £237,000 a year afterwards. That is a strong case and stating the soft estimates openly makes it stronger rather than weaker, because a reviewer who finds an unstated assumption discounts everything. Option A reaches the right answer by comparing one event's cost to the build cost, ignoring the running cost and the frequency. Option D declines a calculation the question supports.

### Preparation tips

- **Memorise the availability minutes.**
- **Multiply availabilities across serial dependencies.**
- **Check whether a fail-open path has actually been tested before excluding it.**
- **Measure error budgets as burn rate against elapsed window.**
- **Right-size on peak with failure headroom, never on average.**
- **Do not claim elapsed queue time as recovered engineer hours.**
- **Report both metrics when a change moves two.**
- **Do throughput arithmetic at design time and provision headroom.**

### Common pitfalls to avoid

- **Comparing consumed error budget to the monthly total without elapsed time.**
- **Assuming composed availability matches the weakest component.**
- **Reducing instance count on average utilisation.**
- **Presenting queueing hours as staff savings.**
- **Reporting a failure-rate improvement without the lead time cost.**
- **Comparing failed deployment counts across teams with different volumes.**
- **Provisioning a batch window with no headroom.**

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment tests whether you can determine exactly what written material establishes. At principal level on the management track the material is service level agreements, change management policy, security standards, supplier terms and governance frameworks.

The commonest format gives a passage and asks you to mark statements True, False or Cannot Say. True means the passage establishes it, False means it contradicts it, and Cannot Say means neither — regardless of what you know from running these systems. Your operational experience is the main hazard, because you will supply the usual arrangement where the passage describes this one.

Three specifics matter at your level.

The first is that service level agreements define availability with precise exclusions — planned maintenance, customer-caused outages, force majeure — and the exclusions determine what a percentage actually promises.

The second is that change management policy allocates authority narrowly: who may approve what, in which circumstances, and what must be recorded.

The third is that security standards attach obligations to classifications and environments, and a control required in one context is frequently not required in a neighbouring one.

### How this assessment maps to your role

- **Reading service level agreements** maps to **Availability and capacity management**, where you lead policy and strategy.
- **Reading change policy** maps to embedding stability in deployment.
- **Reading security standards** maps to **Information security**.
- **Reading supplier terms** maps to resource allocation and procurement.
- **Reading governance frameworks** maps to leading programmes.
- **Precision in written advice** maps to advising stakeholders.

### Practice questions

*Passage A — for Questions 1 to 4*

"The supplier warrants monthly availability of at least 99.9%, measured as the proportion of five-minute intervals in which the service responded successfully to the monitoring probe. Availability is calculated excluding planned maintenance windows notified at least five working days in advance, and excluding periods of unavailability caused by the customer's own systems or network. Planned maintenance may not exceed eight hours in any calendar month. Where availability falls below the warranted level, the customer is entitled to a service credit calculated in accordance with Schedule 4. Service credits are the customer's sole remedy for availability failures, except in the case of a failure below 95% in any month, where the customer may additionally terminate on 30 days' notice."

**Question 1 (easy)**

Statement: The supplier warrants monthly availability of at least 99.9%.

- A) True
- B) False
- C) Cannot Say

**Correct answer: A**

**Explanation:** Stated directly. Note the measurement definition that follows — five-minute intervals against a monitoring probe — which is what the 99.9% actually refers to, and which is considerably less demanding than measuring real user requests. A service can be badly degraded for real users while responding successfully to a probe every five minutes.

**Question 2 (moderate)**

Statement: Eight hours of planned maintenance in a month would count against the 99.9% availability figure.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The passage contradicts this: availability is calculated "excluding planned maintenance windows notified at least five working days in advance". Properly notified maintenance is outside the measurement. This is a substantial practical point — eight hours is roughly 1.1% of a month, so a service could be unavailable for eight notified hours plus 43 minutes of unplanned downtime and still report 99.9% availability. Note the exclusion depends on the notice being given; maintenance taken without five working days' notice is not excluded.

**Question 3 (moderate)**

Statement: If availability falls to 97% in a month, the customer may terminate the agreement.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The passage contradicts this. Service credits are "the customer's sole remedy for availability failures, except in the case of a failure below 95% in any month", where termination becomes available. 97% is above 95%, so the exception is not triggered and credits remain the sole remedy. The threshold matters, and reading "sole remedy" without finding the exception, or finding the exception without checking the threshold, both produce the wrong answer.

**Question 4 (harder)**

Statement: A period of unavailability caused by a failure in the customer's network would reduce the reported availability figure.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The passage excludes "periods of unavailability caused by the customer's own systems or network" from the calculation. So a customer-network failure does not reduce the reported figure. The passage contradicts the statement directly. Worth noticing operationally: the exclusion means the reported number can diverge substantially from what users experienced, and who determines causation is not addressed by this passage at all.

*Passage B — for Questions 5 to 8*

"Standard changes are pre-approved and may be implemented by any authorised engineer without further approval, provided they are recorded within one working day. Normal changes require approval by the change advisory board, which meets weekly. Emergency changes may be implemented with the approval of the on-call incident manager, and must be presented to the next change advisory board for retrospective review. A change may be classified as standard only where it has been implemented successfully at least five times as a normal change and has an approved implementation procedure. The change advisory board reviews the standard change catalogue quarterly and may remove a change type from it."

**Question 5 (easy)**

Statement: Standard changes require approval before implementation.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The passage contradicts this: standard changes "are pre-approved and may be implemented by any authorised engineer without further approval". The pre-approval is the point of the category. The recording obligation within one working day is a separate duty and does not amount to prior approval.

**Question 6 (moderate)**

Statement: A change implemented successfully four times as a normal change can be classified as standard.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The passage requires "at least five times", so four does not satisfy the condition. Note also that the five-implementation requirement is one of two conjunctive conditions — there must also be an approved implementation procedure — so even five successful implementations would not be sufficient on their own. The statement fails on the first condition alone.

**Question 7 (moderate)**

Statement: An emergency change does not need change advisory board involvement.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The passage contradicts this: emergency changes "must be presented to the next change advisory board for retrospective review". The board's involvement is deferred, not removed. Reading an emergency route as bypassing governance entirely is the natural error, and the retrospective review is precisely what makes the emergency route safe to have.

**Question 8 (harder)**

Statement: A change type in the standard catalogue will remain there unless it causes an incident.

- A) True
- B) False
- C) Cannot Say

**Correct answer: C**

**Explanation:** The passage says the board "reviews the standard change catalogue quarterly and may remove a change type from it", without stating any grounds for removal. So removal could follow an incident, a procedural change, a technology retirement, or the board's judgement — the passage neither establishes that an incident is required nor that it is not. The statement asserts a specific condition on a discretionary power the passage leaves unconditioned.

*Passage C — for Questions 9 to 12*

"Secrets used by production services must be stored in the approved secrets management service and must be rotated at least every 90 days. Secrets used only in non-production environments must be stored in the approved service but are not subject to the rotation requirement, provided that no non-production environment holds production data. Where a non-production environment holds production data, it is treated as production for the purposes of this standard. Access to production secrets is granted on the approval of the service owner and is reviewed quarterly. A secret that has been exposed must be rotated immediately and the exposure reported to the security team within 24 hours."

**Question 9 (moderate)**

Statement: Secrets used only in non-production environments must be rotated every 90 days.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The passage contradicts this, conditionally: non-production secrets "are not subject to the rotation requirement, provided that no non-production environment holds production data". The statement asserts the requirement unconditionally. Note the proviso is broad — it refers to *no* non-production environment holding production data, not merely the environment in question, which is a stricter condition than a quick reading suggests.

**Question 10 (moderate)**

Statement: A test environment containing a copy of production data must have its secrets rotated every 90 days.

- A) True
- B) False
- C) Cannot Say

**Correct answer: A**

**Explanation:** The passage establishes this: "Where a non-production environment holds production data, it is treated as production for the purposes of this standard", and production secrets must be rotated at least every 90 days. The reclassification clause does the work, and it is the clause most often missed — teams copy production data into test environments routinely and rarely notice that doing so changes the environment's classification under standards like this one.

**Question 11 (moderate)**

Statement: An exposed secret must be reported to the security team before it is rotated.

- A) True
- B) False
- C) Cannot Say

**Correct answer: C**

**Explanation:** The passage requires immediate rotation and reporting within 24 hours, which strongly implies rotation comes first, and it does not state an order. Rotating immediately and reporting within 24 hours are compatible with reporting first if the report takes a moment. The passage establishes both obligations and their deadlines without establishing a sequence, so the statement asserting a required order is not supported — nor is it contradicted.

**Question 12 (harder)**

Statement: Access to non-production secrets is reviewed quarterly.

- A) True
- B) False
- C) Cannot Say

**Correct answer: C**

**Explanation:** The passage says "access to production secrets is granted on the approval of the service owner and is reviewed quarterly". It says nothing about the governance of access to non-production secrets — there may be a quarterly review, a different arrangement, or none. The scoping word is "production", and the passage's silence on the other case is genuine silence rather than an implied negative. Note the contrast with Question 9, where the passage explicitly addressed non-production and created an exemption; here it simply does not mention it.

### Preparation tips

- **Check how availability is measured and what is excluded.**
- **Find the threshold attached to an exception to a sole remedy.**
- **Read a deferred approval as approval, not as a bypass.**
- **Check both limbs of a conjunctive condition.**
- **Look for reclassification clauses that change which rules apply.**
- **Distinguish an unconditioned discretionary power from a conditioned one.**
- **Check whether two obligations with deadlines also specify an order.**
- **Note when a scoping word limits a clause to one case.**

### Common pitfalls to avoid

- **Reading a warranted availability percentage as covering planned maintenance.**
- **Missing the threshold on a termination right.**
- **Treating an emergency change route as bypassing governance.**
- **Reading a non-production exemption as unconditional.**
- **Overlooking that production data reclassifies an environment.**
- **Inferring a sequence from two deadlines.**
- **Extending a rule stated for production to non-production.**

## Workplace job-specific situational judgement assessment

### About this assessment

A workplace job-specific situational judgement assessment presents realistic scenarios and asks you to identify effective and ineffective responses. At principal level on the management track the scenarios involve incident leadership, standing between delivery pressure and operational risk, allocating a platform capability everyone wants, and developing people whose best work is invisible.

The commonest formats ask for the most and least effective response, or for ratings. Scoring is against a key derived from experienced practitioners at comparable seniority.

Three patterns run through the strong answers.

The first is that during an incident the priority is restoration and the priority afterwards is learning, and mixing the two degrades both. Diagnosing while users are affected costs users; hunting for a responsible individual afterwards costs you the next honest account.

The second is that you are frequently the person saying no to something someone wants urgently, and the effective form of that is making the risk visible and decidable rather than refusing.

The third is that your teams do work that is noticed only when it fails, which puts an unusual weight on your ability to make its value legible to people who will otherwise never see it.

### How this assessment maps to your role

- **Incident leadership** maps to **Service support** and **Availability and capacity management**.
- **Balancing delivery and stability** maps to embedding security, stability and capacity in delivery.
- **Resource allocation** maps to **Development process optimisation**.
- **Capability and recognition** map to rewarding high performers and shaping career paths.
- **Security leadership** maps to **Information security**.
- **Client relationships** map to working with client functions to establish requirements.

### Practice questions

**Question 1 (easy) — During an incident**

A major incident is in progress. Two engineers are debating the root cause while the service remains degraded. What is the most effective response?

- A) Let them continue; identifying the cause will resolve it.
- B) Redirect to restoration — revert what is revertible, fail over what can fail over, and get the service back — and hold the root cause discussion afterwards with the evidence preserved, because the debate can be settled at leisure and the degradation cannot.
- C) Decide the root cause yourself.
- D) Escalate for more people.

**Correct answer: B. Least effective: D**

**Explanation:** Restoration and diagnosis are different activities and doing them in the wrong order costs users directly. Option B redirects and preserves the evidence, which is what makes the later diagnosis possible. Option D is least effective: adding people to a live incident increases coordination cost, and a crowded incident channel is slower than a small one. Option C makes a call on incomplete information and may send the effort in a wrong direction. Option A allows a debate to continue while the service is down.

**Question 2 (easy) — After an incident**

A post-incident review is drifting towards identifying who made the mistake. What is the most effective response?

- A) Let it run; accountability matters.
- B) Redirect it to the conditions that made the mistake possible and consequential — what made the wrong action easy, what allowed it to reach production, why it was not caught — because a review that finds a person stops there, and the same conditions will produce the same outcome with a different person.
- C) Move the discussion to a private setting.
- D) Remind everyone the review is blameless.

**Correct answer: B. Least effective: A**

**Explanation:** Option B does the redirect and says what to redirect to, which is the part that makes it work — "blameless" as a stated value does nothing without the specific questions that produce systemic findings. Option A is least effective because a review that identifies an individual produces no change to the system and reliably ensures the next incident is described less honestly. Option D names the principle without supplying the alternative and tends to be ignored within two minutes. Option C removes the discussion from the people who would learn from it.

**Question 3 (moderate) — Delivery pressure against a stability risk**

A programme wants to deploy a substantial change the day before a peak period. You judge the risk to be significant. What is the most effective response?

- A) Refuse; deploying before peak is poor practice.
- B) State the risk concretely — what could fail, how likely, what the impact would be during peak, and how long recovery would take — and put the decision to whoever owns the service's risk, offering the alternatives of deploying after peak or deploying behind a feature toggle that can be turned off.
- C) Allow it; the programme owns its delivery.
- D) Allow it with a rollback plan.

**Correct answer: B. Least effective: C**

**Explanation:** The decision belongs to the risk owner and your job is to ensure it is made knowingly, with the alternatives visible. Option B's third element matters most: a feature toggle frequently resolves the whole tension by decoupling deployment from activation, and it is the option most often not considered under time pressure. Option C is least effective because it treats a risk you can see and they cannot as somebody else's problem. Option D is reasonable and thin — a rollback plan for a peak-period failure still means an outage during peak. Option A removes the risk owner from their own decision.

**Question 4 (moderate) — A team bypassing the pipeline**

You discover a team has been deploying directly to production, bypassing the pipeline, for two months. What is the most effective response?

- A) Stop the practice immediately and require pipeline use.
- B) Find out why before anything else — a team bypassing a pipeline for two months is usually working around something specific, such as a stage that fails unpredictably or takes too long for urgent fixes — because if the pipeline is genuinely unusable for their case, enforcing it just moves the workaround somewhere less visible.
- C) Report it as a compliance breach.
- D) Add technical controls preventing direct deployment.

**Correct answer: B. Least effective: C**

**Explanation:** Two months of workaround by a capable team is information about the pipeline. Option B gets it, and the likely findings are actionable — a flaky stage, a missing emergency path, or a delay incompatible with their operational reality. Option C is least effective: treating it as a compliance matter before understanding it guarantees you never hear about the next workaround, and does not fix the pipeline. Option D is likely part of the eventual answer and, applied first, forces the team into a process that does not work for them. Option A is the same problem in softer form.

**Question 5 (moderate) — Recognising invisible work**

An engineer has spent six months on reliability improvements. There have been no incidents in their area, and their contribution is not visible in any delivery metric. What is the most effective response?

- A) Thank them and note it in their appraisal.
- B) Make the value legible — quantify what changed, such as the failure classes now impossible or the incidents that would have occurred at the previous rate — and put that in front of the people who make promotion and resourcing decisions, because invisible work stays invisible unless someone converts it into something countable.
- C) Give them public credit at a team meeting.
- D) Move them onto more visible work.

**Correct answer: B. Least effective: D**

**Explanation:** The structural problem is that success in reliability work looks like nothing happening, and the person doing it is disadvantaged in every process that counts outputs. Option B fixes that by producing the count, which serves them and also protects the work itself from being deprioritised. Option D is least effective — it solves their visibility problem by stopping the valuable work, and tells everyone that reliability work is a career dead end. Options A and C are good and insufficient: neither reaches the people making decisions about promotion or headcount.

**Question 6 (moderate) — A client function's stated requirement**

A client function insists that a new service must have 99.99% availability. What is the most effective response?

- A) Design for 99.99%.
- B) Establish what drives the figure — what happens to users or to the business during an outage, and at what duration it becomes serious — because 99.99% is four minutes a month and the cost of the last increment is very high, and the underlying need is frequently about the duration of a single outage rather than about annual uptime.
- C) Explain that 99.99% is expensive.
- D) Propose 99.9% as more realistic.

**Correct answer: B. Least effective: D**

**Explanation:** Availability targets are almost always stated rather than derived, and the derivation usually reveals something different — that a two-hour outage would be serious and a five-minute one would not, which is a statement about recovery time rather than about availability percentage. Option B recovers the actual requirement. Option D is least effective: countering one arbitrary number with another arbitrary number turns a requirements conversation into a negotiation, and you have conceded that the figure is the thing being discussed. Option C leads with cost, which sounds obstructive. Option A commits to an expensive target nobody has justified.

**Question 7 (harder) — A security finding nobody wants**

A security assessment finds a significant vulnerability in a platform component. Fixing it requires a migration the organisation has no appetite for. What is the most effective response?

- A) Escalate until it is funded.
- B) Set out the exposure in concrete terms — what an attacker could do, what access they would need, what data is reachable — and the options with their costs, including interim mitigations that reduce the risk without the migration, then get a named risk acceptance from whoever is accountable if nothing is done.
- C) Implement the interim mitigations and move on.
- D) Note the finding on the risk register.

**Correct answer: B. Least effective: D**

**Explanation:** Option B does the three things available: makes the risk concrete enough to be evaluated, offers the middle path that usually exists, and ensures that a decision to accept the risk is made explicitly by someone accountable rather than by inertia. The named acceptance is the part most often skipped and it is what converts a warning into a decision. Option D is least effective: a risk register entry with no owner and no decision is where findings go to be forgotten, and it will be found again after an incident. Option C is useful and leaves the residual risk unowned. Option A escalates before quantifying.

**Question 8 (harder) — Allocating a platform team**

Four programmes want platform work next quarter and you can serve two. All four are pressing. What is the most effective response?

- A) Serve the two with the strongest business cases.
- B) Decide on cost of delay and on whether any request could be met by something self-service, tell all four the decision and the reasoning, and be explicit with the two that are not served about what that means for them — because a platform team's worst outcome is four programmes each getting a third of what they need.
- C) Split the team's time across all four.
- D) Ask the programmes to agree priority between themselves.

**Correct answer: B. Least effective: C**

**Explanation:** Option B decides, explains, and adds the platform-specific criterion — the highest-value work is often the piece that removes the need to ask next time. Telling the unsuccessful two explicitly what it means for them is what lets them replan rather than wait. Option C is least effective: splitting a platform team four ways loses time to context switching and delivers four partial capabilities, which is worse for everyone than two complete ones. Option D delegates your decision to parties with no basis for deciding it, and the most assertive programme wins. Option A uses self-reported cases as the sole criterion.

**Question 9 (harder) — Pressure to weaken a control**

A programme asks you to grant standing production database access to three developers to speed up debugging. What is the most effective response?

- A) Refuse; standing production access is not acceptable.
- B) Address the underlying need rather than the request — they need to diagnose production problems, and the routes to that are better logging, a production-like environment with realistic data, or time-bound audited access granted on demand — because standing access is a permanent risk granted to solve an intermittent problem.
- C) Grant it with audit logging.
- D) Grant it for a limited period.

**Correct answer: B. Least effective: C**

**Explanation:** The request is a solution and the need behind it is legitimate, which is why refusing outright fails — they still cannot debug, and they will find another route. Option B names three ways to meet the need without a standing grant, and just-in-time audited access is usually the one that satisfies everyone. Option C is least effective because it grants the permanent risk and adds a control that records what happened without preventing anything, while making everyone feel the issue was addressed. Option D is better and tends to become permanent through renewal. Option A refuses without solving.

**Question 10 (harder) — A capability gap you cannot recruit for**

Your platform depends on a technology for which the market is thin and your pay bands are below market rate. Two of your three specialists have left in a year. What is the most effective response?

- A) Make the case for higher pay bands.
- B) Treat it as a strategic dependency question rather than a recruitment problem — if you cannot staff a technology sustainably, the honest options are to build the capability internally over time, to buy it as a managed service, or to migrate away, and continuing to run something you cannot staff is the option nobody chooses explicitly but everyone drifts into.
- C) Recruit contractors.
- D) Train existing staff.

**Correct answer: B. Least effective: C**

**Explanation:** Two departures in a year against a thin market is not a recruitment problem you can solve by recruiting harder, and option B reframes it as the strategic question it is. Naming the drift is the useful part: nobody decides to run a critical platform with no sustainable staffing, and organisations do it constantly by treating each departure as a separate vacancy. Option C is least effective as a strategy — contractors are the most expensive route, they carry the knowledge out with them, and they defer the decision indefinitely while making it look handled. Options A and D are both real components of a plan and neither is the decision.

**Question 11 (harder) — Evidence against your own platform decision**

A platform choice you led two years ago is now the main source of operational toil for three teams. What is the most effective response?

- A) Defend it; the decision was right given what was known.
- B) Put the toil in front of people in measurable terms — hours a month, incidents attributable, what teams cannot do because of it — say plainly that the original assumptions have not held, and get someone other than you to assess the options, because a recommendation about your own decision carries a discount you cannot argue away.
- C) Propose a migration.
- D) Invest in reducing the toil within the current platform.

**Correct answer: B. Least effective: A**

**Explanation:** Option B quantifies the problem, is honest about the decision, and handles the credibility issue by removing yourself from the recommendation. That last move is what makes the analysis actionable — whatever you recommend about your own platform choice will be read as defensiveness or as guilt. Option A is least effective: it is probably true and entirely beside the point, since the question is what to do now, and defending it teaches three teams that the toil is permanent. Options C and D are both plausible answers that should come out of an independent assessment rather than from you.

**Question 12 (harder) — Reporting reliability honestly**

A director asks you to summarise platform reliability for a board paper. The figures are good on availability and poor on time to restore. What is the most effective response?

- A) Report availability; it is the headline metric.
- B) Report both, with the point that they say different things — the platform rarely fails and takes a long time to recover when it does, which is a specific and fixable problem — because a board given only the favourable metric will not fund the work the unfavourable one points at.
- C) Report availability and mention restore time if asked.
- D) Report the combined picture as "mixed".

**Correct answer: B. Least effective: A**

**Explanation:** Option B reports honestly and does the more valuable thing, which is to interpret: high availability with slow recovery is a recognisable pattern with known remedies — better runbooks, faster rollback, improved observability — and naming it turns two numbers into a proposal. Option A is least effective because it is the version that gets you thanked now and leaves the restore-time problem unfunded until it causes a serious incident, at which point the board will ask what you knew. Option C is the same omission with a fallback. Option D characterises without informing.

### Preparation tips

- **Restore first, diagnose afterwards, preserve the evidence.**
- **Redirect a post-incident review to conditions with specific questions.**
- **Offer the feature toggle when deployment timing is the argument.**
- **Ask why a team is working around a process before enforcing it.**
- **Convert invisible reliability work into something countable.**
- **Derive availability targets from outage consequences.**
- **Get a named risk acceptance when a finding will not be fixed.**
- **Reframe an unstaffable technology as a strategic dependency.**

### Common pitfalls to avoid

- **Adding people to a live incident.**
- **Letting a review identify a person.**
- **Countering an arbitrary availability target with another number.**
- **Treating a pipeline bypass as a compliance breach first.**
- **Moving an engineer off reliability work to make them visible.**
- **Granting standing production access with audit logging.**
- **Recruiting contractors as an answer to a structural staffing problem.**
- **Reporting the favourable metric only.**

## Conclusion

You have worked through four assessments pitched at principal DevOps engineer on the management track, and the themes are worth drawing together.

The cognitive section kept returning to systems rather than instances. Four outages with four different causes is one detection failure. Automation does not remove risk; it trades many small errors for the possibility of one large uniform one, which makes blast radius the design question. A thorough design's risk lives in the assumptions it did not state. And a single-person dependency is not fixed by documentation, because the expert does not know which of their actions are the non-obvious ones.

The numeric section was the arithmetic that decides platform work: availabilities multiplying across serial dependencies, error budgets as burn rate rather than totals, peak headroom rather than average utilisation, and the correlation in the deployment table showing that the team deploying least spends four times as long in a degraded state. It also included the discipline of not overclaiming — queueing hours are not recovered staff hours, and a business case that says they are will lose to the first person who notices.

The verbal section was about the documents that define what you are actually promised and permitted. An availability warranty excluding notified maintenance promises considerably less than it appears to. An emergency change route defers governance rather than removing it. And copying production data into a test environment reclassifies that environment under most security standards, which is the clause teams miss most often.

The situational judgement section was about standing between delivery pressure and operational risk. The strong answers restored before diagnosing, redirected reviews from people to conditions, made risks concrete and got them explicitly accepted by someone accountable, and addressed the need behind a request for standing production access rather than the request itself.

If one thread runs through all four, it is the visibility problem. Your teams' best work produces nothing observable, which means a large share of your job is converting absence into evidence — incidents that did not happen, capacity that absorbed a peak, an attack surface that closed. Nobody else in the organisation will do that translation, and the funding, the recognition and the credibility all depend on it.

Good luck. This is work that only shows when it is missing, and the care you have taken here is exactly the kind that keeps it from showing.
