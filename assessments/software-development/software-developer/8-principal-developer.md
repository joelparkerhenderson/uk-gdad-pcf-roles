# Principal Developer - Psychometric Assessment Resources

## Introduction

Welcome. This guide is written for you as a principal developer in the UK Government Digital and Data profession — someone who leads and plans development across large or multiple teams, who is either an expert across many technical areas or a specialist with very deep knowledge in one, and who uses that knowledge alongside related disciplines to keep several teams working effectively. Your role summary also names developing capability through internal mobility, career paths and recruitment, and identifying, testing and championing the adoption of emerging technologies.

On the technical track, the skills that define your level are demanding ones: designing systems characterised by high levels of risk, impact and business or technical complexity; controlling system design practice within an enterprise architecture; influencing industry-based models; developing implementation and procurement strategies consistent with business needs; and ensuring adherence to technical strategies, policies and standards.

The reasoning that produces good outcomes at this level is different in kind from what worked earlier. You are frequently the most technically informed person in the room, which means nobody will catch your errors. You make decisions whose consequences arrive in years, on systems whose behaviour under stress is not fully knowable, in organisations where the constraint is rarely technical. And you champion emerging technology, which requires the specific and uncomfortable discipline of being enthusiastic and rigorous about the same thing at once.

You may be preparing for a formal assessment, or you may simply want to re-examine judgement that has become fluent. Fluency is the risk. At principal level, wrong answers arrive with the same feeling of certainty as right ones, and the value of an exercise like this is in the questions where you were quick.

Three things shape everything that follows. First, high-impact system design is mostly about failure modes, and the useful question is what happens when a component behaves badly rather than when it works. Second, your influence operates through other people's decisions, which makes how you present reasoning as consequential as the reasoning. Third, championing a technology and evaluating it honestly are in tension, and holding both is a large part of the job.

The document has four assessment sections, each with an overview, a mapping to your skills, twelve questions with explanations, preparation tips and pitfalls.

Commit to an answer before reading each explanation.

Let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive assessment measures the reasoning your role demands, using material drawn from the role. At principal level that means architectural options with long-lived consequences, failure analysis across system boundaries, technology evaluation, procurement strategy and the design of standards that will govern multiple teams.

The format is typically fifteen to thirty minutes online, covering deduction, pattern recognition, error checking, prioritisation and applied problem solving, scored objectively against a norm group of comparable seniority. Adaptive tests escalate difficulty; acuity reports separate speed from accuracy.

Three things distinguish this section at your level.

The first is that complex systems fail in combinations. A single-cause analysis of a serious failure in a distributed system is usually incomplete, and the interesting question is which conditions had to hold simultaneously.

The second is that architectural decisions are best evaluated by their failure characteristics rather than their success characteristics. Two designs that both work will differ enormously in what they do when a dependency is slow, and slow is worse than down.

The third is that constraints at your level are rarely technical. A technically superior option that cannot be procured, staffed or operated is not superior, and treating organisational constraints as noise is the characteristic principal-level error.

### How this assessment maps to your role

- **Failure-mode reasoning** maps to **Systems design**, where you design for high risk and impact.
- **Multi-causal analysis** maps to **Service support** and **Availability and capacity management**.
- **Technology evaluation** maps to identifying, testing and championing emerging technologies.
- **Strategy and procurement reasoning** maps to developing implementation and procurement strategies.
- **Standards design** maps to **Modern development standards** and controlling design practice.
- **Security reasoning** maps to **Information security**, where you design and quality assure against threats.

### Practice questions

**Question 1 (easy) — Deduction from an architectural rule**

Your design standard states: "Services must not call each other synchronously across domain boundaries, except where the call is a read of reference data with a published cache policy." A service makes a synchronous cross-domain call. Which must be true?

- A) The standard was breached.
- B) It reads reference data.
- C) Either the call is a read of reference data with a published cache policy, or the standard was breached.
- D) The call should be made asynchronous.

**Correct answer: C**

**Explanation:** A rule with a compound exception plus a fact silent on the exception yields only the disjunction. Note the exception has two conjoined conditions — reference data *and* a published cache policy — so option B would be insufficient even if established. Option D prescribes rather than deduces. The practical corollary is that a standard whose exception depends on a published cache policy needs somewhere the policy is published, or it cannot be checked, and unenforceable standards are a design defect you own.

**Question 2 (easy) — Failure characteristics**

Two designs for a dependency call: A retries three times with a 5-second timeout; B fails immediately after one 1-second timeout and serves a cached value. Under a dependency that has become slow but not unavailable, which behaves better?

- A) Design A; retries improve success rates.
- B) Design B — a slow dependency under design A holds each request for up to 15 seconds while retrying, exhausting connection pools and threads and propagating the slowness upstream, whereas B degrades to a cached response in one second and keeps the calling service responsive.
- C) They are equivalent.
- D) Design A, provided the retries are exponentially backed off.

**Correct answer: B**

**Explanation:** Slow is worse than down, and this is the single most useful heuristic in distributed system design. A dependency returning errors quickly lets callers fail fast; a dependency that hangs consumes the caller's resources and turns one degraded service into several. Design A's fifteen-second worst case is a resource-exhaustion mechanism, and retries against a struggling dependency also add load precisely when it can least absorb it. Option D improves A meaningfully and does not change the fundamental problem that the caller waits. The general principle is that timeouts should be set by what the caller can afford, not by what the dependency might need.

**Question 3 (moderate) — Combination failures**

A serious outage occurred when a cache expired, a batch job was running, and a deployment was in progress. Individually, none of these has caused an issue before. What is the strongest analysis?

- A) The deployment caused it; it was the change.
- B) The failure required a conjunction, so the analysis should identify what resource the three shared — most likely database connections, CPU, or a lock — because the remedy for a conjunction failure is usually to isolate or bound the shared resource rather than to prevent any one of the three conditions.
- C) The batch job should not run during business hours.
- D) Deployments should not happen while batch jobs run.

**Correct answer: B**

**Explanation:** Three individually safe conditions combining is the classic signature of contention for a shared, unbounded resource, and finding that resource is what produces a fix that generalises. Options C and D each prevent one specific pairing and leave the underlying fragility untouched — there will be a fourth condition, and it will combine with two of these. This is also why single-cause incident reports on complex systems are usually wrong: they name the most recent change, which is necessary but not sufficient, and they conclude with a rule preventing that exact combination.

**Question 4 (moderate) — Championing an emerging technology**

You believe an emerging technology would significantly benefit several teams. What is the strongest way to champion it?

- A) Present the case to leadership with the benefits and a proposed rollout.
- B) Run a genuine test with a pre-agreed definition of what would count as failure, on a real workload rather than a demonstration, and publish the result either way — because a champion whose evaluations only ever succeed is discounted, and the credibility to get the next adoption through is worth more than this one.
- C) Pilot it in one team and expand if it goes well.
- D) Wait for another organisation to adopt it first.

**Correct answer: B**

**Explanation:** The two words carrying the weight are "pre-agreed" and "either way". A pilot without a prior failure criterion nearly always succeeds, because the people running it want it to and there is always a favourable interpretation available. Option B makes the evaluation capable of producing a negative result, which is the only thing that makes a positive one worth anything. Option C is close and is the standard approach, and its weakness is exactly the missing failure criterion. Option A advocates before evidence. Option D is the risk-averse posture that makes a principal developer's technology role pointless.

**Question 5 (moderate) — Organisational constraint**

The technically strongest option for a new platform requires skills your organisation does not have and cannot easily recruit. What is the strongest analysis?

- A) Choose it anyway; technical quality matters most.
- B) A platform the organisation cannot operate is not the strongest option — operability by the people who will actually run it is a design criterion, not a compromise — so the real comparison is between the second option and the first plus a credible, funded plan to build the capability, and the second usually wins.
- C) Choose the second option.
- D) Outsource operation of the first.

**Correct answer: B**

**Explanation:** The framing in option B is what distinguishes principal-level judgement: operability is part of the design, not a constraint imposed on it. A system nobody in the organisation can debug at 3am is a bad system regardless of its architecture. Option B also keeps the first option live under the one condition that would make it viable — a funded capability plan — which is occasionally the right answer, particularly if the skills are strategically valuable. Option C reaches the usual conclusion without the reasoning, and misses the case where building capability is right. Option D moves the problem and creates a dependency on a supplier for something you cannot evaluate.

**Question 6 (moderate) — Standard design across many teams**

You are designing a standard that will apply to twelve teams with varying maturity. What is the strongest approach?

- A) Set the standard at the level the best teams already achieve.
- B) Separate what must be uniform from what can vary — interfaces, security controls and data handling usually must; internal practices usually need not — because a standard that constrains internal choices costs twelve teams daily for benefits that mostly accrue at boundaries.
- C) Set the standard at the level most teams can currently meet.
- D) Let each team set its own standards.

**Correct answer: B**

**Explanation:** The useful question is not how demanding a standard should be but what it should cover, and the answer follows from where the cost of divergence falls. Divergent interfaces, security controls and data handling impose costs on everyone else; divergent internal testing practices mostly do not. Option B applies that test. Option A sets a bar most teams will fail and creates widespread non-compliance, which then normalises. Option C sets a bar that changes nothing. Option D abandons the coordination that is the point of having a principal-level design authority.

**Question 7 (harder) — Reading a procurement trade-off**

A supplier product would deliver a required capability in three months; building it would take nine. The product's licence permits use only within your department, and there is a plausible future need to share the capability across government. What is the strongest analysis?

- A) Buy it; six months is decisive.
- B) The licence restriction is the deciding factor if cross-government sharing is likely, since a capability that cannot be shared may need rebuilding later at full cost plus migration — so the question is how firm that future need is, and whether the licence can be negotiated, before the six-month difference means anything.
- C) Build it; government capabilities should be reusable.
- D) Buy it now and build a replacement later.

**Correct answer: B**

**Explanation:** The six-month difference is the visible variable and the licence term is the one that determines total cost. If cross-government sharing is genuinely likely, buying means paying for the product and then building anyway, with a migration on top — so the comparison is not three months against nine but three months against nine plus the probability-weighted cost of doing it twice. Option B also identifies the practical move, which is to test whether the licence is negotiable, since suppliers frequently have public-sector terms that are not on the standard price list. Option D describes the expensive outcome as though it were a plan. Option C applies a principle without weighing the likelihood.

**Question 8 (harder) — Diagnosing across a boundary**

Two teams each report that their service is behaving correctly, yet a user journey spanning both fails intermittently. What is the strongest first step?

- A) Ask both teams to investigate more thoroughly.
- B) Establish whether the two services agree on the contract at the point of failure — the commonest cause of "both services are fine" is a difference in interpretation at the boundary, such as timeout expectations, retry semantics, or what a particular response code means — and get a single trace across both services rather than two sets of logs.
- C) Add monitoring to the journey.
- D) Assume it is a network problem.

**Correct answer: B**

**Explanation:** "Both components are behaving correctly and the system is failing" almost always means the components have different models of the interface. The concrete candidates are worth knowing: mismatched timeouts, where the caller gives up before the callee finishes; retry semantics against a non-idempotent operation; or disagreement about whether a status code means retry or fail. Option B names them and prescribes the diagnostic that actually resolves cross-boundary problems, which is a single correlated trace — two teams reading their own logs will each continue to conclude they are fine. Option A repeats what has failed. Option C is useful and slow. Option D guesses.

**Question 9 (harder) — Evaluating a claim about scale**

A team proposes a design and states it will "scale horizontally". What is the strongest challenge?

- A) Ask for load test results.
- B) Ask what does not scale horizontally in the design — there is always something, usually a database, a shared lock, a sequence generator or a coordination service — because the useful information is where the ceiling is and at what load it is reached, not whether the stateless tier can be replicated.
- C) Accept it; horizontal scaling is well understood.
- D) Ask about the cost at scale.

**Correct answer: B**

**Explanation:** "Scales horizontally" is almost always a claim about the application tier, which is the easy part, and the system's actual limit lives in the shared component behind it. Option B asks the question that locates the ceiling, and the candidates listed are where it usually is. This matters because a design that scales to ten times current load is fine and one that scales to 1.5 times is a problem, and both are described identically by the phrase in the proposal. Option A is a good follow-up and load tests typically explore a range someone chose in advance, which is not the same as finding the ceiling. Option D is a real question about a different thing.

**Question 10 (harder) — A pattern across incidents**

Across a year, seven significant incidents occurred in four different services. In six of the seven, the initial alert was for a symptom in a service downstream of the actual fault. What is the strongest conclusion?

- A) The services need better alerting.
- B) The pattern indicates that faults are being detected by their consequences rather than at source, which suggests the failing components lack health signals of their own — so the improvement is instrumentation at the point of failure and dependency-aware alerting, and the current mean time to diagnose is being inflated by teams starting their investigation in the wrong service.
- C) The incident response process is too slow.
- D) Six out of seven is not a large enough sample.

**Correct answer: B**

**Explanation:** The consistency of the pattern is the finding: six of seven is a systemic property of the monitoring, not a coincidence. Detecting faults downstream means every incident begins with a team investigating a service that is working correctly, which adds a fixed diagnostic cost to every incident and explains a great deal of mean-time-to-resolve without anyone doing anything wrong. Option B names both remedies. Option A is directionally right and unspecific — "better alerting" could mean more alerts, which would make this worse. Option C addresses a symptom of the same cause. Option D declines a clear signal.

**Question 11 (harder) — Deciding what not to design**

You are asked to design a system to handle a business process that is itself under review and may change substantially within a year. What is the strongest approach?

- A) Design for the current process and accept rework.
- B) Design for the parts that will not change and defer the rest — the data the process operates on and the integrations at its edges are usually stable, while the sequencing and rules are what is under review — and be explicit that flexibility in the volatile parts costs something and is being bought deliberately.
- C) Design a highly configurable system that can handle any process.
- D) Wait for the review to conclude.

**Correct answer: B**

**Explanation:** Option B applies the right distinction, which is between the stable substrate and the volatile logic, and it names the cost honestly. Option C is the trap and it is the response most likely to be proposed: a fully configurable process engine is far more expensive to build, much harder to understand, and typically still fails to accommodate the change that actually arrives, because the dimension of variation nobody anticipated is the one the review produces. Generality bought speculatively is usually wasted. Option A may be right if the rework is genuinely cheap. Option D is available only if the timeline permits, and the scenario implies it does not.

**Question 12 (harder) — Influencing without authority**

You believe a programme outside your control is heading for a serious technical problem. You have no formal role in it. What is the strongest approach?

- A) Raise it formally through governance.
- B) Take it to the people making the decision, privately and with the specific technical reasoning and what would falsify it — because an outside technical challenge arriving through governance is heard as an attack on a programme's competence, and the same content delivered directly is usually heard as help.
- C) Say nothing; it is not your programme.
- D) Document your concern for the record.

**Correct answer: B**

**Explanation:** The content and the channel are separable, and the channel largely determines whether the content lands. Option B keeps the concern technical, gives the programme the chance to act without a public loss of face, and — crucially — includes what would show you wrong, which is what distinguishes a colleague raising a concern from an outsider passing judgement. Option A may become necessary and is a poor opening move, since a governance challenge puts the programme in a defensive posture from which it cannot easily concede. Option D is self-protective and does nothing for the outcome. Option C wastes the expertise that is the reason for your role.

### Preparation tips

- **Evaluate designs by their failure characteristics.** Slow is worse than down.
- **Look for the shared resource behind a conjunction failure.**
- **Set a failure criterion before piloting a technology.**
- **Treat operability by your organisation as a design criterion.**
- **Ask what a standard must cover before asking how demanding it should be.**
- **Ask what does not scale in a design that "scales horizontally".**
- **Distinguish the stable substrate from the volatile logic.**
- **Choose the channel deliberately when raising a concern outside your remit.**

### Common pitfalls to avoid

- **Single-cause analysis of a conjunction failure.**
- **Piloting a technology you champion with no definition of failure.**
- **Treating organisational constraints as noise.**
- **Setting a standard at the level only the best teams meet.**
- **Accepting "scales horizontally" without locating the ceiling.**
- **Building a configurable engine to absorb unspecified future change.**
- **Opening a cross-programme technical concern through governance.**
- **Letting a six-month delivery difference decide a procurement with a licence restriction.**

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment tests whether you can reach a defensible conclusion from operational and financial data at speed. At principal level the data is what shapes multi-year decisions: capacity models, reliability budgets, total cost of ownership, procurement comparisons and the volumetrics of systems that do not yet exist.

The format is typically fifteen to twenty-five minutes with a calculator, mixing computational items with items asking what the data supports. The second kind matters more at your level, because you are usually the person whose numeric claim nobody in the room can check.

Three habits are worth naming.

The first is that you are frequently reasoning about a system that does not exist yet, from volumetrics somebody estimated. The right response is to establish what the answer is sensitive to and bound it, rather than to compute a precise figure from an invented input.

The second is that costs at your level compound over years and include operation, not just build. A comparison that stops at delivery cost is the wrong comparison.

The third is that reliability arithmetic is multiplicative across dependencies, which produces figures that surprise people, and you are the person expected to know that before the design is committed.

### How this assessment maps to your role

- **Reliability composition** maps to **Systems design** and **Availability and capacity management**.
- **Capacity modelling** maps to managing service components against KPIs.
- **Total cost of ownership** maps to developing implementation and procurement strategies.
- **Volumetrics under uncertainty** maps to designing systems of high complexity.
- **Process and throughput metrics** map to **Development process optimisation**.
- **Security risk quantification** maps to **Information security**.

### Practice questions

*Table 1 — Component availability, current architecture*

| Component | Measured availability | Calls per user request |
|---|---|---|
| API gateway | 99.99% | 1 |
| Identity service | 99.95% | 1 |
| Core service | 99.9% | 1 |
| Reference data service | 99.5% | 1 |
| Database cluster | 99.99% | 1 |

**Question 1 (easy) — Reading a table**

Which component is least available?

- A) Core service
- B) Reference data service
- C) Identity service
- D) API gateway

**Correct answer: B**

**Explanation:** The reference data service at 99.5% is an order of magnitude less available than the gateway and database at 99.99%. Worth noting immediately that 99.5% is about 3.6 hours of downtime a month, which is a great deal, and that reference data is exactly the kind of component that could tolerate caching.

**Question 2 (easy) — Availability in minutes**

How much monthly downtime does 99.5% availability allow, in a 30-day month?

- A) About 43 minutes
- B) About 3.6 hours
- C) About 22 minutes
- D) About 7 hours

**Correct answer: B**

**Explanation:** 43,200 minutes × 0.005 = 216 minutes = 3.6 hours. The reference points worth holding: 99.9% ≈ 43 minutes, 99.95% ≈ 22 minutes, 99.99% ≈ 4.3 minutes, 99.5% ≈ 3.6 hours. The last is the one people underestimate, because 99.5% sounds close to 99.9% and is eight times worse.

**Question 3 (moderate) — Composed availability**

If a user request requires all five components in Table 1 to be available, what is the approximate composed availability?

- A) About 99.9%
- B) About 99.33%
- C) About 99.5%
- D) About 99.7%

**Correct answer: B**

**Explanation:** Multiply: 0.9999 × 0.9995 × 0.999 × 0.995 × 0.9999 = 0.99330, about 99.33%. Serial dependencies multiply, so the composed system is worse than its worst component — a fact that surprises people every time and is the reason this calculation belongs at design time. 99.33% is roughly 4.8 hours of downtime a month. Note how the arithmetic points at the fix: the reference data service contributes nearly all the loss, so caching it takes the composed figure to about 99.83% on its own.

**Question 4 (moderate) — Redundancy**

If the reference data service were made redundant with two independent instances each at 99.5%, what is the approximate availability of the pair, assuming either alone is sufficient?

- A) 99.75%
- B) 99.9975%
- C) 99.5%
- D) 99.95%

**Correct answer: B**

**Explanation:** For parallel redundancy, compute the probability both fail: 0.005 × 0.005 = 0.000025, so availability is 1 − 0.000025 = 99.9975%. Redundancy in parallel multiplies the failure probabilities, which is why it produces such dramatic improvements. The critical caveat is the word "independent": if both instances share a datastore, a network segment, a deployment or a configuration source, the failures are correlated and the real figure is nowhere near this. In practice the shared dependency is usually what fails, which is why measured availability of redundant pairs rarely approaches the theoretical number.

*Table 2 — Two platform options, five-year view (£000)*

| | Option A (build) | Option B (supplier) |
|---|---|---|
| Year 1 build/setup | 900 | 150 |
| Annual licence | 0 | 260 |
| Annual operation | 180 | 60 |
| Annual support staff | 120 | 40 |
| Exit/migration cost | 0 | 200 |

**Question 5 (moderate) — Five-year total**

What is the approximate five-year total cost of Option A?

- A) £1,900,000
- B) £2,400,000
- C) £1,500,000
- D) £2,100,000

**Correct answer: B**

**Explanation:** Build £900k, plus five years of operation (5 × £180k = £900k), plus five years of support staff (5 × £120k = £600k). Total: £900k + £900k + £600k = £2,400,000. Note that the build cost everyone quotes is £900k, barely a third of the lifetime figure — recurring operation and staffing together cost £1.5m over the period, and a comparison that stops at the build line is not a comparison at all.

**Question 6 (moderate) — Comparing the options**

What is the approximate five-year total for Option B, including exit?

- A) £2,000,000
- B) £2,150,000
- C) £1,800,000
- D) £2,400,000

**Correct answer: B**

**Explanation:** Setup £150k, plus five years of licence (5 × £260k = £1,300k), operation (5 × £60k = £300k) and support staff (5 × £40k = £200k), plus exit £200k. Total: 150 + 1,300 + 300 + 200 + 200 = £2,150,000. Against Option A's £2,400,000, the supplier option is about £250k cheaper over five years — considerably closer than the build-cost comparison (£900k versus £150k) suggests, and the gap would reverse over a longer horizon since Option A's annual cost is £300k against Option B's £360k. The horizon chosen decides this comparison, which is worth saying out loud whenever one is presented to you.

**Question 7 (moderate) — Sensitivity**

Over what approximate period do the two options in Table 2 cost the same, ignoring exit costs?

- A) About 8 years
- B) About 12 years
- C) About 5 years
- D) About 20 years

**Correct answer: B**

**Explanation:** Option A: £900k + £300k/year. Option B: £150k + £360k/year. Setting them equal: 900 + 300n = 150 + 360n, so 750 = 60n, n = 12.5 years. The build option overtakes at around twelve and a half years, which is longer than most platforms survive — a useful thing to know, and a useful thing to say, because "build pays back in year thirteen" reframes a debate conducted in terms of principle. Being able to produce this figure quickly is more valuable than any argument about build versus buy in the abstract.

**Question 8 (harder) — Capacity model under uncertainty**

You are sizing a new service. The estimated user base is "between 50,000 and 200,000" with peak concurrency estimated at 3% to 8%. What is the strongest approach?

- A) Size for the midpoint: 125,000 users at 5.5% concurrency.
- B) Recognise that the range spans 1,500 to 16,000 concurrent users — more than a tenfold difference — so a point estimate is meaningless, and the right output is a design that can scale across the range plus an identification of what would let you narrow it, since the cost of the two extremes differs enormously.
- C) Size for the maximum: 200,000 at 8%.
- D) Size for the minimum and scale later.

**Correct answer: B**

**Explanation:** 50,000 × 3% = 1,500; 200,000 × 8% = 16,000. The two independent uncertainties compound, and a tenfold range in concurrent load is a different system, not a different capacity setting. Option B says what the honest answer is: this is not yet a sizing question, it is a question about which of two systems you are building, and the useful work is narrowing the estimate. Option A produces a single number that is probably wrong in a direction nobody has considered. Option C over-provisions by up to a factor of ten. Option D risks a launch failure. The presentation matters as much as the analysis — a stakeholder given a midpoint will treat it as settled.

**Question 9 (harder) — Error rate and volume**

A service handles 4 million requests a day. A proposed change would introduce a failure mode affecting an estimated 0.02% of requests. How many requests per day would be affected, and does the figure matter?

- A) 80 per day; negligible.
- B) 800 per day, which is a small percentage and a large number of people — at that volume a "negligible" failure rate produces roughly 24,000 affected requests a month, so whether it matters depends entirely on what the failure does to the user, not on the percentage.
- C) 8,000 per day; unacceptable.
- D) 80,000 per day.

**Correct answer: B**

**Explanation:** 4,000,000 × 0.0002 = 800 per day. The arithmetic is the smaller half of the item. At high volume, percentages are actively misleading in conversation: 0.02% sounds like a rounding error and describes 800 people a day, or 24,000 a month, each of whom experienced something. Whether that is acceptable depends on whether the failure means a retry or a lost benefit application. Converting rates into absolute counts before discussing them is one of the more valuable habits at your level, precisely because you are usually talking to people who will hear the percentage.

**Question 10 (harder) — What the data supports**

After a caching layer was introduced, mean response time fell from 340ms to 120ms and error rates rose from 0.05% to 0.4%. What is the strongest conclusion?

- A) The cache is a success; latency improved substantially.
- B) The latency improvement is large and the eightfold error increase needs explaining before the change can be called a success — the plausible mechanisms are cache-related failures, stale data causing downstream validation failures, or added infrastructure introducing its own faults, and which one it is determines whether this is fixable or inherent.
- C) The cache should be removed.
- D) The two changes are unrelated.

**Correct answer: B**

**Explanation:** Both figures moved substantially and reporting only the favourable one is the specific failure this item tests. An eightfold error increase is not noise. Option B names the candidate mechanisms because they have very different implications: a misconfigured cache is fixable in an afternoon, whereas stale data breaking downstream validation may be intrinsic to caching this particular data. Option A is how this result gets presented. Option C discards a large genuine benefit before diagnosis. Option D asserts independence for two changes that arrived together.

**Question 11 (harder) — Throughput ceiling**

A design processes messages through a queue. Producers generate 12,000 messages per minute at peak. Each consumer handles 400 messages per minute, and the design specifies 25 consumers. What is the position?

- A) Comfortable; 25 consumers handle 10,000 per minute.
- B) Under-provisioned at peak: 25 × 400 = 10,000 per minute against 12,000 arriving, so the queue grows by 2,000 messages per minute for the duration of the peak and only drains afterwards — which may be acceptable if the peak is short and latency-tolerant, and is a design fault if it is not.
- C) Comfortable; queues absorb bursts.
- D) Under-provisioned; 40 consumers are needed.

**Correct answer: B**

**Explanation:** Consumption capacity is 10,000/minute against 12,000/minute arriving, a deficit of 2,000/minute. Option B computes it and then asks the right follow-up, which is whether the backlog matters — a ten-minute peak produces a 20,000-message backlog that clears in ten minutes at off-peak rates, and whether that is fine depends entirely on what the messages are. Option A does the multiplication and stops before comparing. Option C states a true property of queues as though it removed the arithmetic. Option D gets the direction right and prescribes a number without asking whether the backlog is a problem.

**Question 12 (harder) — Risk quantification**

A security control would cost £150,000 a year. It mitigates a risk estimated at a 5% annual chance of an incident costing £1.5m. What is the strongest analysis?

- A) Implement it; the risk is £75,000 a year expected loss, less than the control.
- B) The expected annual loss is £75,000 against a £150,000 control, so on expected value alone it fails — but expected value is the wrong sole criterion for a low-probability high-impact risk, since the organisation may be unable to absorb a £1.5m single event, and the estimates themselves are soft enough that the comparison is not decisive.
- C) Do not implement it; the expected loss is half the cost.
- D) Implement it; security is not optional.

**Correct answer: B**

**Explanation:** 5% × £1.5m = £75,000 expected annual loss, against a £150,000 control — so a pure expected-value comparison rejects it, and option A states the arithmetic correctly and then draws the opposite conclusion, which is worth catching. Option B does the arithmetic and then declines to treat it as decisive, for two good reasons: variance matters when a single event could exceed what the organisation can absorb, and both the 5% and the £1.5m are estimates with wide error bars. That is the honest position. Option C follows the arithmetic mechanically. Option D refuses the analysis entirely.

### Preparation tips

- **Multiply availabilities for serial dependencies, and failure probabilities for parallel ones.**
- **Check whether redundant components share a dependency before trusting the parallel figure.**
- **Total the recurring costs across the horizon before comparing to a build cost.**
- **Compute the crossover point when comparing build against buy.**
- **Convert percentages into absolute counts at high volume.**
- **Compound independent uncertainty ranges before offering a point estimate.**
- **Report the unfavourable metric alongside the favourable one.**
- **Compute expected loss and then say why it is not the only criterion.**

### Common pitfalls to avoid

- **Assuming composed availability is as good as the worst component.**
- **Trusting a parallel redundancy figure with correlated failures.**
- **Comparing build cost to licence cost without operation and exit.**
- **Offering a midpoint estimate across a tenfold range.**
- **Describing 800 affected users a day as 0.02%.**
- **Presenting a latency improvement without the error increase.**
- **Treating a queue as absorbing a sustained deficit.**
- **Deciding a low-probability high-impact risk on expected value alone.**

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment tests whether you can determine exactly what written material establishes. At principal level the material is technical strategy, architecture governance, procurement terms, security standards and cross-organisational agreements — documents that allocate authority and create obligations.

The commonest format gives a passage and asks you to mark statements True, False or Cannot Say. True means the passage establishes it, False means it contradicts it, Cannot Say means neither — irrespective of what you know. Deep expertise is the main hazard, because you will supply from experience what the passage has not said.

Three specifics matter at your level.

The first is that governance documents allocate authority precisely. "Approves", "endorses", "is consulted", "is informed" and "may direct" are different powers, and acting on a misreading is a governance failure rather than a technical one.

The second is that strategy documents are frequently written to sound more binding than they are, and distinguishing a commitment from an aspiration is a skill with real consequences.

The third is that procurement and licensing prose defines scope narrowly and by exception, and a permission granted for one purpose does not extend to a neighbouring one.

### How this assessment maps to your role

- **Reading governance and authority** maps to controlling system design practice within an enterprise architecture.
- **Reading strategy** maps to ensuring adherence to technical strategies and policies.
- **Reading procurement and licence terms** maps to developing procurement strategies.
- **Reading security standards** maps to **Information security**.
- **Reading service and integration agreements** maps to **Systems integration**.
- **Precision in communication** maps to providing technical advice to stakeholders.

### Practice questions

*Passage A — for Questions 1 to 4*

"The design authority approves architectural decisions with cross-departmental impact. Decisions confined to a single service are made by the service's technical lead, who must notify the design authority where the decision departs from a published pattern. The design authority may direct that a decision within a single service be brought to it for approval, where in its view the decision sets a precedent. The chief technology officer endorses the design authority's decisions and may return a decision for reconsideration once, with reasons; a decision returned and reaffirmed by the design authority stands."

**Question 1 (easy)**

Statement: A decision confined to a single service is made by the service's technical lead.

- A) True
- B) False
- C) Cannot Say

**Correct answer: A**

**Explanation:** Stated directly. Note the two qualifications that follow — a notification duty for departures from a published pattern, and the design authority's power to call a decision in — neither of which changes who makes the decision by default.

**Question 2 (moderate)**

Statement: The chief technology officer can overturn a decision of the design authority.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The passage contradicts this. The CTO "endorses" decisions and "may return a decision for reconsideration once, with reasons", and "a decision returned and reaffirmed by the design authority stands". So the CTO has a single power of return, not a veto, and the last clause is there to close exactly this inference. Reading "endorses" as approval-with-power-to-refuse is the natural error, and endorsement here is a formal step rather than a gate.

**Question 3 (moderate)**

Statement: A technical lead making a decision that follows a published pattern within a single service has no obligation to notify the design authority.

- A) True
- B) False
- C) Cannot Say

**Correct answer: A**

**Explanation:** The notification duty is qualified: notify "where the decision departs from a published pattern". Following the pattern means the qualifier is not met, so the obligation does not arise. The passage establishes this by the structure of the condition. Note this says nothing about whether the design authority might still call the decision in under its precedent power, which is a separate mechanism not dependent on notification.

**Question 4 (harder)**

Statement: The design authority can require a single-service decision to come to it for approval only where the decision departs from a published pattern.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The passage contradicts the word "only". The call-in power is conditioned on the design authority's view that the decision "sets a precedent", which is a different and independent test from departing from a published pattern — a decision could follow every pattern and still set a precedent, and could depart from a pattern without setting one. The statement imports the condition attached to the notification duty and applies it to the call-in power. Conflating two conditions attached to two different mechanisms is a common and consequential misreading of governance text.

*Passage B — for Questions 5 to 8*

"The departmental technology strategy states that new services will adopt the shared platform where it meets their needs. Services with requirements the platform cannot meet may build alternative arrangements, subject to approval by the design authority and an assessment of whole-life cost. The strategy anticipates that the majority of new services will be on the shared platform within three years. Existing services are not required to migrate, although migration is encouraged where a service is undergoing substantial redevelopment. The platform's roadmap is set by the platform team in consultation with a user group drawn from adopting services."

**Question 5 (easy)**

Statement: A new service whose requirements the shared platform cannot meet may build an alternative arrangement.

- A) True
- B) False
- C) Cannot Say

**Correct answer: A**

**Explanation:** Stated directly, with two conditions attached: design authority approval and a whole-life cost assessment. The permission exists; it is gated.

**Question 6 (moderate)**

Statement: Existing services undergoing substantial redevelopment must migrate to the shared platform.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The passage contradicts "must": existing services "are not required to migrate", and migration is "encouraged" where substantial redevelopment is under way. Encouragement is not a requirement, and the passage states the non-requirement explicitly before adding the encouragement. This is the shape of a great deal of strategy prose — a firm-sounding sentence that on inspection creates no obligation.

**Question 7 (moderate)**

Statement: The majority of new services will be on the shared platform within three years.

- A) True
- B) False
- C) Cannot Say

**Correct answer: C**

**Explanation:** The passage says the strategy "anticipates" this. An anticipation is a forecast, and the passage establishes that the forecast exists rather than that the outcome will occur. Marking True treats a document's expectation as a fact about the world, which is the specific error strategy documents most reliably induce — they are written in a register that makes projections read as commitments.

**Question 8 (harder)**

Statement: An adopting service can require a feature to be added to the platform roadmap.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The passage assigns roadmap authority to the platform team "in consultation with a user group drawn from adopting services". Consultation is not control, and the roadmap is explicitly set by the platform team — so an adopting service has an input mechanism and not a requirement power. The passage does more than omit the power; it allocates the decision elsewhere, which is what makes this False rather than Cannot Say.

*Passage C — for Questions 9 to 12*

"The licence grants the customer a non-exclusive right to use the software for internal business purposes at the sites listed in Schedule 1. Use at additional sites requires a variation to this agreement. The customer may make copies for backup and disaster recovery purposes only. The customer may not permit access by any third party, except that access by a contractor engaged by the customer, working under the customer's direction and bound by equivalent confidentiality obligations, is permitted for the duration of the engagement. The supplier will provide security patches for the supported version for the term of the agreement, and is not obliged to provide patches for any version the customer has modified."

**Question 9 (moderate)**

Statement: The customer may allow a contractor to access the software.

- A) True
- B) False
- C) Cannot Say

**Correct answer: A**

**Explanation:** The passage establishes this through the exception to the third-party prohibition, subject to three conditions: engaged by the customer, working under the customer's direction, and bound by equivalent confidentiality obligations, for the duration of the engagement. The permission is real and narrow. All three conditions are conjunctive, which is worth noticing — a contractor engaged by a different organisation, however trusted, is not covered.

**Question 10 (moderate)**

Statement: The customer may use the software at a new site opened during the term.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The licence is granted for "the sites listed in Schedule 1", and "use at additional sites requires a variation to this agreement". A new site is an additional site, so use there without a variation is outside the licence. The passage contradicts the unqualified statement. This is the kind of term that is straightforward to read and routinely breached in practice, because nobody rereads the licence when the estate changes.

**Question 11 (harder)**

Statement: The supplier will not provide security patches if the customer has modified the software.

- A) True
- B) False
- C) Cannot Say

**Correct answer: C**

**Explanation:** The passage says the supplier "is not obliged to provide patches for any version the customer has modified", which removes an obligation without establishing a refusal. The supplier may well patch anyway, as a commercial matter. The distinction between "is not obliged to" and "will not" is precisely the kind that determines whether you can rely on something, and treating the absence of an obligation as a prohibition is the natural misreading. Note the practical significance: if you are planning a modification, the passage tells you that you would be relying on the supplier's goodwill rather than on the contract.

**Question 12 (harder)**

Statement: The customer may make a copy of the software to use in a test environment.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The passage permits copies "for backup and disaster recovery purposes only", and the word "only" excludes other purposes including testing. A test environment is neither backup nor disaster recovery. The passage contradicts the statement. This is a genuinely common operational breach, and the item is here because it is the kind of restriction a principal developer needs to notice at design time — an architecture assuming a full non-production copy of a licensed product may be unlicensable as designed.

### Preparation tips

- **Distinguish approves, endorses, consults, is informed, and may direct.**
- **Check whether a condition attached to one mechanism has been imported into another.**
- **Read "anticipates" and "expects" as forecasts, not commitments.**
- **Read "is not obliged to" as removing a duty, not creating a prohibition.**
- **Treat conjunctive conditions as all required.**
- **Watch for "only" — it excludes everything unnamed.**
- **Check that a permission covers the case you have in mind, not a neighbouring one.**
- **Note when a power is allocated elsewhere, which makes a statement False rather than Cannot Say.**

### Common pitfalls to avoid

- **Reading endorsement as a veto.**
- **Reading encouragement as a requirement.**
- **Treating a strategy's projection as an established outcome.**
- **Reading consultation as control over a roadmap.**
- **Extending a site licence to a new site.**
- **Treating an absent obligation as a refusal.**
- **Assuming a backup-only copying right permits test environments.**

## Workplace job-specific situational judgement assessment

### About this assessment

A workplace job-specific situational judgement assessment presents realistic scenarios and asks you to identify effective and ineffective responses. At principal level the scenarios involve influence without direct authority, decisions with long-horizon consequences, disagreement with senior people, and the recurring problem that you are usually right and being right is not sufficient.

The commonest formats ask for the most and least effective response, or ratings for each. Scoring is against a key derived from experienced practitioners at comparable seniority, so the target is professional consensus.

Three patterns run through the strong answers.

The first is that your technical authority is a finite resource and spending it on the wrong things leaves nothing for the right ones. A principal developer who objects to everything is routed around.

The second is that being the most informed person in the room creates an obligation to make your reasoning legible, including its uncertainty. Confident assertion from someone nobody can check is how organisations acquire expensive mistakes.

The third is that you are frequently working through people you do not manage, over timescales longer than anyone's attention, which means the durable move is usually to change what people can see rather than to win an argument.

### How this assessment maps to your role

- **Influence and technical advice** map to providing technical advice to stakeholders.
- **Design authority** maps to controlling system design practice.
- **Capability development** maps to facilitating internal mobility, shaping career paths and recruiting.
- **Technology adoption** maps to identifying, testing and championing emerging technologies.
- **Security leadership** maps to leading others in using appropriate information security practices.
- **Cross-team coordination** maps to keeping multiple teams working effectively.

### Practice questions

**Question 1 (easy) — A design you consider wrong**

A team presents a design you think is a mistake. They have thought about it and disagree with you. What is the most effective response?

- A) Direct them to change it; you have design authority.
- B) Set out specifically what you think will go wrong and under what conditions, ask what they expect to happen in those conditions, and treat a good answer as evidence you were wrong — because a testable prediction converts an authority dispute into a question, and you are sometimes the one who is mistaken.
- C) Let them proceed; it is their service.
- D) Escalate to their lead.

**Correct answer: B**

**Explanation:** A specific prediction — "under sustained load above X, this will exhibit Y" — is the most useful thing you can contribute, because it can be checked, it teaches the reasoning rather than the conclusion, and it leaves room for you to be wrong. Option B does this. Option A wins today and costs you the team's engagement, and design authority used as a first resort stops being consulted. Option C abandons the role. Option D routes around the people you disagree with, which is the least repairable of the four.

**Question 2 (easy) — A technology you championed is struggling**

A technology you advocated for is causing a team difficulty. They are frustrated. What is the most effective response?

- A) Help them work through the difficulties.
- B) Help with the immediate difficulties and establish honestly whether this is a learning curve or a genuine mismatch, and say which you think it is — because if the technology is wrong for this case, you are the person best placed to say so and the least likely to be believed if you wait.
- C) Suggest they persevere; adoption is always difficult early.
- D) Support them in reverting to the previous approach.

**Correct answer: B**

**Explanation:** Both halves matter. The immediate help is what the team needs today; the honest assessment is what your role requires. The distinction between a learning curve and a mismatch is the substantive question and it usually has an answer if you look — a learning curve produces difficulties that decline, a mismatch produces recurring friction in the same place. Option C is what an advocate says by default and is precisely the response that makes future advocacy discounted. Option D concedes without diagnosis. Option A is good and stops short of the judgement only you can offer.

**Question 3 (moderate) — Pressure to approve a design**

A programme under time pressure asks you to approve a design you have significant concerns about. Delay would be costly and visible. What is the most effective response?

- A) Approve it; the delay cost is real and your concerns are judgement calls.
- B) Separate the concerns that are genuinely blocking from those that are preferences, approve conditional on the blocking ones being addressed with a named owner and date, and record what you are accepting — because an unconditional approval on a design you believe is flawed is the version that gets quoted back later, and a conditional one keeps the programme moving.
- C) Refuse to approve until the concerns are resolved.
- D) Approve it and note your concerns for the record.

**Correct answer: B**

**Explanation:** The discipline in option B is the separation, and it is what makes the rest work: most "significant concerns" contain one or two that genuinely matter and several that reflect how you would have done it. Conditional approval with named owners and dates lets the programme proceed while keeping the real risks live. Option D is the common response and is close to worthless — a noted concern with no owner and no date changes nothing and reads as covering yourself. Option C treats all concerns as blocking. Option A abandons the judgement you are there to exercise.

**Question 4 (moderate) — A capability gap**

You identify that no team in the organisation has the skills to operate a technology now central to three services. What is the most effective response?

- A) Arrange training.
- B) Make the gap visible as a risk with its consequences — what happens at 3am when the person who knows it is unavailable — and propose a specific remedy with a cost, whether that is training, recruitment, internal mobility, or reducing dependence on the technology.
- C) Recruit a specialist.
- D) Reduce reliance on the technology.

**Correct answer: B**

**Explanation:** Your role names developing capability, and the effective first move is making an invisible risk visible in terms that get funded. The 3am framing is not rhetorical — it is the concrete form of the risk and it is what makes a general concern land. Option B then offers options with costs, which is what turns a raised risk into a decision. Options A, C and D are each possible remedies presented without the analysis that would show which is right; training is slow, recruitment is uncertain, and reducing dependence may be expensive, and choosing between them requires knowing the scale of the exposure.

**Question 5 (moderate) — An emerging technology with organisational appetite**

Senior leadership is enthusiastic about adopting a technology you have evaluated and found unsuitable for your context. What is the most effective response?

- A) Set out your evaluation and recommend against it.
- B) Present the evaluation in terms of the specific conditions under which the technology works well and the ways your context differs — because leadership enthusiasm usually comes from a real success story elsewhere, and showing why that context differs is far more persuasive than a negative recommendation, which invites the reading that you are resistant.
- C) Suggest a pilot to demonstrate the problems.
- D) Comply; leadership has decided.

**Correct answer: B**

**Explanation:** The framing decides whether this is heard. Leadership enthusiasm is nearly always downstream of a genuine case study, and disputing the technology implicitly disputes that case study, which is unwinnable and unnecessary. Option B accepts the success and locates the difference — different scale, different data, different operating model — which lets everyone change position without anyone being wrong. Option A is honest and adversarially framed. Option C spends months proving something you already know and creates the risk that the pilot succeeds narrowly. Option D abandons the role.

**Question 6 (moderate) — Two teams building the same thing**

You discover two teams independently building substantially the same capability. Both are partway through. What is the most effective response?

- A) Stop one and have it adopt the other's.
- B) Get both teams together to establish whether the capabilities are genuinely the same — they frequently differ in ways that matter and are invisible from outside — and if they are, decide which continues on the technical merits and what the other team gets in return, because the team that stops has lost weeks and needs something better than being told to stop.
- C) Let both continue; consolidation later.
- D) Have a third team build a shared version.

**Correct answer: B**

**Explanation:** Two things are usually wrong with the obvious response. First, the capabilities often are not the same — they look identical from a distance and differ in the requirements that drove them — and consolidating them produces something serving neither well. Second, whichever team stops has genuinely lost work, and how that is handled determines whether anyone tells you about a duplication next time. Option B addresses both. Option A skips the check and the aftermath. Option C accepts the waste. Option D adds a third party and a coordination problem to a problem of coordination.

**Question 7 (harder) — Contradicting a senior stakeholder in public**

In a large meeting, a director makes a technical claim that is wrong and that will lead to a poor decision. What is the most effective response?

- A) Correct it immediately; the decision matters.
- B) Add the correcting information without framing it as a correction — supplying the relevant fact and its implication rather than contradicting the person — and follow up directly afterwards if the decision is still heading the wrong way, because the goal is the decision rather than the record of who was right.
- C) Say nothing and raise it afterwards.
- D) Ask a question that leads them to the correct position.

**Correct answer: B**

**Explanation:** Option B gets the information into the room, which is necessary, without a public contradiction that makes retreat costly for the director and hardens the position. The phrasing difference is small and does most of the work: "worth noting that X, which would mean Y" lands where "that's not right" does not. Option D is a reasonable technique and can read as manipulative if transparent, and it often fails to get the actual fact stated. Option A prioritises correctness over outcome. Option C risks the decision being made in the meeting, which is frequently what large meetings are for.

**Question 8 (harder) — A long-horizon risk nobody wants to fund**

You judge that a core system will become unsupportable in about three years. Nothing is failing now and there is no appetite to act. What is the most effective response?

- A) Raise it annually until someone acts.
- B) Convert the judgement into something dated and visible — the specific dates on which support ends, versions go out of security patching, or skills become unavailable — and get it onto a risk register with an owner, because "will become unsupportable" is arguable and "loses security patches in March 2029" is a fact people can plan against.
- C) Accept it; the organisation has decided.
- D) Escalate to the board.

**Correct answer: B**

**Explanation:** The reason nothing is happening is that the risk is expressed as a judgement, and judgements about three-year horizons lose to problems happening now. Option B converts it into dated facts with an owner, which is the form that survives your absence and appears in front of people at planning time. This is the single most useful technique for long-horizon technical risk. Option A relies on your persistence and stops when you leave. Option D spends significant credibility on something not yet urgent, and will be received as alarmism. Option C is the passive version of an answer.

**Question 9 (harder) — A security decision with a business cost**

A proposed control would materially reduce a security risk and add friction to a heavily used journey. The service owner does not want it. What is the most effective response?

- A) Insist; security risks are not negotiable.
- B) Establish what the risk actually is in concrete terms — what an attacker could do, how hard it would be, and what the consequence would be — and what the friction costs in measurable terms, then put both to whoever is accountable for the service's risk, because this is a genuine trade-off and the decision belongs to the risk owner rather than to either of you.
- C) Accept the service owner's decision.
- D) Propose a lighter control.

**Correct answer: B**

**Explanation:** Security controls and usability are genuinely in tension and pretending otherwise costs you credibility on the occasions when a control really is non-negotiable. Option B quantifies both sides and routes the decision to the person accountable, which is both correct governance and the way to get a decision that sticks. Option D is frequently the right outcome and belongs after the analysis, since a lighter control proposed immediately concedes the risk assessment before making it. Option A treats a trade-off as an absolute. Option C defers to the party with the least interest in the risk.

**Question 10 (harder) — Recruiting for capability**

You are asked to help recruit for a role requiring deep expertise in an area where the market is thin and the salary band is below market rate. What is the most effective response?

- A) Recruit as best you can within the band.
- B) Say plainly that the role as specified is unlikely to be filled, and offer the alternatives — a different shape of role that a strong generalist could grow into, a contract arrangement while capability is built, or a case for the band — because months spent failing to recruit is the most expensive of the available outcomes and the least visible.
- C) Ask for the band to be raised.
- D) Recommend a contractor.

**Correct answer: B**

**Explanation:** The failure mode here is silent and slow: a role that will not fill stays open for six months, the work does not happen, and nobody records the cost. Option B names the problem immediately and offers three routes, which is more useful than any one of them — and the first, reshaping the role for someone who can grow into it, is the option most often overlooked and frequently the best, since deep expertise in a thin market is often more reliably built than bought. Options C and D are single remedies offered without the analysis. Option A proceeds with a plan you expect to fail.

**Question 11 (harder) — Your own architecture is the constraint**

A system you designed four years ago is now the main constraint on several teams' delivery. Replacing it would be a substantial programme. What is the most effective response?

- A) Defend the design; it met the requirements at the time.
- B) Set out clearly what the constraint is costing across the teams and what the options are, including the honest assessment that the original design assumptions no longer hold — and take yourself out of the decision if you can, because a recommendation about your own work carries a discount you cannot argue away.
- C) Propose the replacement programme.
- D) Suggest incremental improvements.

**Correct answer: B**

**Explanation:** Option B does the analysis and handles the credibility problem directly rather than pretending it does not exist. Whichever way you argue — for replacement or against — your view of your own architecture is discounted, and acknowledging that openly is more effective than trying to be persuasive despite it. The specific move of getting an independent assessment is what makes the recommendation actionable. Option A is the reflex and is usually true and irrelevant, since the question is what to do now. Option C may well be right and coming from you it will be read as either guilt or empire-building. Option D may be right and needs the same independent test.

**Question 12 (harder) — Evidence against a standard you set**

Data suggests a standard you introduced across twelve teams is producing significant cost with little measurable benefit. What is the most effective response?

- A) Review the data carefully; measurement of standards is difficult.
- B) Publish the finding, including that it is your standard, and either withdraw it or reduce its scope to where the benefit is demonstrable — because twelve teams paying daily for something with no measurable benefit is a real cost, and a principal developer who withdraws their own standard on evidence makes every subsequent standard more credible.
- C) Improve the measurement to capture the benefits.
- D) Retain it; some benefits are not measurable.

**Correct answer: B**

**Explanation:** The cost is certain, distributed and daily; the benefit is unmeasured. That asymmetry is what should decide it, and option B allows the right resolution — narrowing to where the benefit shows rather than abandoning wholesale. The credibility argument is not sentimental: standards work through voluntary compliance far more than enforcement, and teams comply with standards set by someone they have seen withdraw one. Option D is true in general and is the argument that keeps every unproductive standard in place. Option C is legitimate and becomes indistinguishable from motivated reasoning when the person improving the measurement owns the standard. Option A is a reasonable step and incomplete as a response.

### Preparation tips

- **Convert a design disagreement into a testable prediction.**
- **Separate blocking concerns from preferences before approving anything.**
- **Express long-horizon risk as dated facts with an owner.**
- **Locate the difference in context rather than disputing a success story.**
- **Quantify both sides of a security-usability trade-off and route it to the risk owner.**
- **Say early when a role as specified will not fill.**
- **Get an independent assessment when the subject is your own work.**
- **Add correcting information without framing it as a correction.**

### Common pitfalls to avoid

- **Using design authority as a first resort.**
- **Noting a concern for the record with no owner or date.**
- **Advising perseverance with a technology you championed.**
- **Consolidating two apparently duplicate capabilities without checking they are the same.**
- **Contradicting a senior stakeholder publicly.**
- **Raising a three-year risk as a judgement rather than a date.**
- **Recruiting into a role you expect not to fill.**
- **Retaining your own standard on unmeasurable benefits.**

## Conclusion

You have worked through four assessments pitched at principal developer on the technical track, and the themes are worth drawing out.

The cognitive section kept returning to failure. Designs are best distinguished by what they do when a dependency is slow rather than when it works, because slow is worse than down. Serious failures in complex systems are conjunctions, and the useful question is what resource the conditions shared. A standard whose exception cannot be checked is unenforceable. And the technically superior option your organisation cannot operate is not the superior option — operability is a design criterion, not a compromise.

The numeric section was the arithmetic that decides architecture: availabilities multiply in series and failure probabilities multiply in parallel, so a composed system is worse than its worst component and a redundant pair is far better than its members — provided the failures really are independent, which they usually are not. Lifetime cost swamps build cost. Compounding uncertainty ranges produce tenfold spans that no midpoint can represent. And at four million requests a day, 0.02% is 800 people.

The verbal section was about the documents that allocate your authority and constrain your options. Endorsement is not a veto. Consultation is not control. "Anticipates" is a forecast. "Is not obliged to" removes a duty without creating a prohibition. And a copying right granted for backup "only" does not stretch to a test environment, however routine that has become.

The situational judgement section was about influence, which is most of what this role runs on. The strong answers converted authority disputes into testable predictions, separated blocking concerns from preferences, turned long-horizon judgements into dated facts on a risk register, and handled the credibility discount on your own work by naming it rather than arguing past it.

If one thread runs through all four, it is that being right is the entry requirement rather than the achievement. The reasoning in this document was mostly about making correct conclusions legible, checkable and actionable by people who cannot verify them — and about staying genuinely open to the possibility that the conclusion is wrong, which at your level almost nobody else is positioned to tell you.

Good luck. This is demanding work, and the care you have taken here is exactly the kind that compounds across the systems and teams you influence.
