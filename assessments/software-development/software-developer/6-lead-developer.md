# Lead Developer - Psychometric Assessment Resources

## Introduction

Welcome. This guide is written for you as a lead developer in the UK Government Digital and Data profession — someone who leads development on one or a small number of related project teams, guides the ways in which the team works, is proficient in a wide range of technical systems, and is involved in identifying appropriate technology and approaches, including deciding when software should be written at all. Your role also names maintaining technical responsibility for all stages and iterations of a software development project, advising on how standards and methods should be applied, and setting the team's standards for programming tools and techniques.

That last cluster is what distinguishes this level. You are no longer accountable only for what you write; you are accountable for what the team writes, for the standards it writes to, and for the technical decisions that shape everything downstream of them. And the phrase "deciding when software should be written" deserves particular attention, because the most consequential decision a lead developer makes is frequently not how to build something but whether to.

You may be facing a formal assessment as part of a selection process, or you may want to re-examine reasoning that has become fluent enough to be worth checking. At your level the risk is not gaps in technical knowledge but that judgement has become automatic, automatic judgement feels certain, and fewer people around you are positioned to challenge it.

Three features of the role shape everything that follows. First, you make decisions whose costs arrive later and land on other people — a framework choice, a data model, an integration pattern — which means reasoning about reversibility matters more than reasoning about elegance. Second, you are the technical voice in rooms where the other participants cannot evaluate what you say, so the honest expression of uncertainty carries unusual weight. Third, you set standards, and a standard is a decision made once and paid for by everybody, every day, for as long as it stands.

The document has four main sections: a cognitive assessment, a numeric reasoning assessment, a verbal reasoning assessment, and a situational judgement assessment. Each provides an overview, a mapping to your named skills, twelve practice questions with full explanations, preparation tips, and common pitfalls.

Commit before reading each explanation, and attend particularly where you were quick and sure.

Let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive assessment measures the reasoning your role demands, presented through practical materials rather than abstract puzzles. At lead level the materials are architectural options, incident evidence, technology choices, standards decisions and the work of the team you are responsible for.

The format is typically an online test of fifteen to thirty minutes covering pattern recognition, logical deduction, error checking, prioritisation and applied problem solving. Scoring is objective against a norm group of comparable seniority. Adaptive platforms raise difficulty after correct answers, and acuity reports distinguish speed from accuracy.

Three things distinguish this section at your level.

The first is that decisions are weighted by reversibility rather than by size. A choice you can undo in a week deserves a quick decision; a data model, a public interface or a framework will be lived with for years, and the reasoning that matters is about which kind you are making before you make it.

The second is that the interesting questions concern mechanisms. When a team keeps producing the same defect, the cause is usually structural — a standard that is unfollowable, a review that happens too late, a framework default, or a missing piece of tooling — and fixing instances leaves it in place.

The third is that "should this be written?" is a live question. Government builds a great deal of software that duplicates something existing, and a lead who cannot evaluate build-versus-reuse honestly will build.

### How this assessment maps to your role

The cognitive dimensions map onto the skills named in your role summary:

- **Deduction under incomplete evidence** maps to **Programming and build (software engineering)**, where technical responsibility across all stages includes diagnosing what went wrong.
- **Systemic diagnosis** maps to **Development process optimisation**, where you identify optimisation opportunities.
- **Technology evaluation** maps to your role level's involvement in identifying appropriate technology and deciding when software should be written.
- **Prioritisation and reversibility** map to **Systems design** and **Availability and capacity management**.
- **Standards judgement** maps to **Modern development standards**, where you advise on how standards should be applied and set team standards.
- **Security reasoning** maps to **Information security**.

### Practice questions

**Question 1 (easy) — Deduction from a governance rule**

Your standard states: "A service may be deployed to production only with a passing full test suite, unless the deployment is a rollback to a previously deployed version." A developer reports deploying without a passing suite. Which must be true?

- A) The standard was breached.
- B) It was a rollback.
- C) Either it was a rollback to a previously deployed version, or the standard was breached.
- D) The deployment should be reverted.

**Correct answer: C**

**Explanation:** A conditional with a stated exception, plus facts silent on the exception, licenses only the disjunction. Options A and B each assume a branch. Option D prescribes an action rather than stating what must be true, and the question asks the latter — worth noticing because at this level a sensible action is frequently offered as a distractor in a logic item and may well be what you would do. Only C holds. Note also that you own this standard, which gives the ambiguity a practical edge: if rollbacks routinely bypass the suite and nobody records which deployments were rollbacks, your own standard is unauditable, and that is a defect in the standard rather than in the developer.

**Question 2 (easy) — Reversibility**

Your team must choose between two approaches for storing a new entity: extending an existing table, or creating a new service with its own datastore. Both are viable. What is the most important consideration?

- A) Which performs better.
- B) Which is easier to undo — extending a table is a change you can iterate on for months, while a separate service with its own datastore creates an integration boundary, a deployment unit and a data migration problem that will be expensive to reverse once anything depends on it.
- C) Which the team prefers.
- D) Which is faster to build.

**Correct answer: B**

**Explanation:** Both options may be defensible on their merits, and the asymmetry in reversibility is what should decide a decision made under uncertainty. Extending a table is a decision you can revisit; splitting out a service creates boundaries that other things immediately attach to, and unpicking it later means coordinating data migration with every consumer. That does not make the split wrong — sometimes it is clearly right — but it does mean it needs a stronger justification, and "we could always change it later" is true of one option and not the other. Option A matters and is usually the easier thing to change afterwards. Option D optimises for the smallest cost in the decision. Option C is a real consideration and not a criterion.

**Question 3 (moderate) — Diagnosing recurring defects**

Three developers on your team have each introduced the same class of bug in a month: unhandled null values from an external API. What is the strongest diagnosis?

- A) The three need to be more careful.
- B) Three people making the same mistake independently indicates a structural cause — most likely that the API's contract does not document which fields are optional, or that the client code has no type-level representation of optionality — so the remedy is in the contract, the generated client, or a type system feature rather than in individual attentiveness.
- C) Code review should be stricter.
- D) Add null checks in review.

**Correct answer: B**

**Explanation:** Three independent occurrences of the same defect is the signature of a structural cause, and the plausibility of blaming carelessness is exactly what makes that answer tempting and useless — people do not become collectively careless about one specific thing in one month. Option B names the realistic candidates and they imply different remedies: an undocumented contract needs fixing at the source, a hand-written client needs generating from a schema, and a language with optionality in the type system can make the class of bug unrepresentable. Option A is the weakest available response to any recurring defect. Option C asks reviewers to catch mechanically what a type system or a generated client would catch automatically. Option D fixes instances forever.

**Question 4 (moderate) — Deciding whether to write software**

A team needs a workflow engine for a multi-step approval process. Building one would take about six weeks. What is the strongest approach?

- A) Build it; six weeks is manageable and a bespoke fit is better.
- B) Establish what exists first — an existing internal capability, an open-source engine, or a simpler pattern that avoids needing an engine at all — because a workflow engine is a long-lived commitment whose real cost is years of maintenance and understanding rather than six weeks of construction, and "we need an engine" is frequently the wrong framing for a process with four steps.
- C) Buy a commercial product.
- D) Build a minimal version and extend it.

**Correct answer: B**

**Explanation:** Your role names deciding when software should be written, and this is the shape of that decision. The six-week figure is the visible cost and the smallest one: a bespoke workflow engine must be maintained, documented, understood by every future developer, and extended every time the process changes, which is a permanent tax. Option B also questions the framing, which is the part most often skipped — a four-step approval process usually does not need an engine, it needs a state field and some validation, and the word "engine" has arrived from somewhere and is doing work nobody has examined. Option D is the tempting middle and is how bespoke engines actually get built, one extension at a time. Option C may be right and is a decision to make after establishing the need, not before.

**Question 5 (moderate) — Competing explanations under incident conditions**

After a release, error rates rise from 0.1% to 3%. The release contained a database migration and a change to retry logic. What is the strongest sequence?

- A) Revert the retry change first, since retries affect error rates directly.
- B) Establish whether the migration is reversible before deciding — if it is not, reverting the release is not available and the response must be a forward fix, which changes the whole approach; if it is, revert everything, restore service, and identify the cause in a safe environment.
- C) Revert the whole release.
- D) Increase the retry limit.

**Correct answer: B**

**Explanation:** Option C is the standard incident response and this scenario contains the fact that defeats it: a database migration may not be reversible, and attempting to revert a release containing one can turn a degraded service into a corrupted one. Establishing that first takes a minute and determines everything afterwards. If the migration is reversible, C becomes correct and B says so. If it is not, the team needs a forward fix and should stop discussing reverting immediately. Option A guesses between two candidates with a 50% chance of leaving the problem in place. Option D changes behaviour during an incident on an unconfirmed diagnosis, and increasing retries against a struggling dependency is a reliable way to make things worse.

**Question 6 (moderate) — Setting a team standard**

You are considering mandating a linting rule that would flag a pattern your team uses inconsistently. What is the strongest approach?

- A) Enable it and fix the existing violations.
- B) Establish what the pattern costs before mandating anything — if it produces real defects, enable the rule with the existing code grandfathered so the team is not blocked by a large cleanup; if it is a stylistic preference, a rule adds friction to every commit for no defect reduction.
- C) Discuss it at a retrospective.
- D) Enable it as a warning.

**Correct answer: B**

**Explanation:** A linting rule is a standard you are imposing on every commit indefinitely, which makes the question whether it prevents something rather than whether you prefer it. Option B asks that first and then handles the practical obstacle that sinks most rule adoptions: enabling a rule across an existing codebase produces hundreds of violations, and a team facing that either disables the rule or spends a week on cleanup instead of delivery. Grandfathering existing code and enforcing on new code gets the benefit immediately at no cost. Option D is a reasonable middle and warnings that nobody fixes train people to ignore warnings generally, which is worse than not having the rule. Option C is a good addition and does not answer whether the rule is worth having.

**Question 7 (moderate) — Technical advice to a non-technical stakeholder**

A service owner asks whether a proposed feature is "technically possible". It is possible and would require substantial rework of an existing component. What is the strongest response?

- A) Yes, it is possible.
- B) Say that it is possible and describe the cost and the consequence — roughly how much rework, what else would be delayed, and what risk the rework introduces — because "is it possible" is almost never the question somebody means, and answering it literally gives them a yes that they will reasonably treat as an estimate.
- C) Say it is possible but difficult.
- D) Say no, given the cost.

**Correct answer: B**

**Explanation:** Almost everything is technically possible, so a literal yes conveys nothing and is heard as encouragement. Option B answers what the person actually needs to decide, and the three elements matter: the scale of the rework, the opportunity cost, and the risk, because a service owner weighing a feature against other work cannot do so without them. Option C is honest and unquantified, and "difficult" is interpreted very differently by different listeners — some hear "a fortnight" and some hear "no". Option D substitutes your judgement for theirs on a trade-off that is theirs to make. This is the specific communication failure that leads to technical teams being seen as obstructive or as over-promising, depending on which way they lean.

**Question 8 (harder) — Scoping the impact of a defect**

You discover that a shared library your team maintains has been silently truncating strings longer than 255 characters for eight months. Four services use it. What is the strongest first step?

- A) Fix the library and release a new version.
- B) Establish the blast radius before deciding anything — which of the four services pass long strings, whether the truncated values were stored, whether anything downstream consumed them, and whether any user-visible data has been silently corrupted — because the fix is small and the remediation may not be.
- C) Notify the four services.
- D) Add validation that rejects long strings.

**Correct answer: B**

**Explanation:** The library fix is the easy part. Silent truncation over eight months means data may be wrong in four services' datastores, in anything downstream that consumed it, and in anything a person has read and acted on — and the word "silently" is doing the damage, because nothing errored and nobody knows which records are affected. Option B establishes the scope, which determines whether this is a patch release or a data remediation exercise with user-facing consequences. Option C is necessary and belongs after you can tell the four services something useful about their exposure. Option D changes silent corruption into visible rejection, which is better behaviour and does nothing about the eight months already stored, and may break services currently relying on the truncation.

**Question 9 (harder) — Technology evaluation**

Your team proposes adopting a new framework that would make a current pain point substantially easier. It is well regarded, three years old, and maintained by a small team. What is the strongest analysis?

- A) Adopt it; the benefit is real and the framework is well regarded.
- B) Weigh the benefit against the commitment: adopting a framework is a decision the service lives with for years, so the questions are what happens if maintenance stops, how much of the codebase would depend on it, how reversible the adoption is, and whether the pain point could be addressed with something more boring — because the cost of being wrong is not the migration but the years of running on something unmaintained.
- C) Reject it; three years is too new.
- D) Adopt it in one service as a trial.

**Correct answer: B**

**Explanation:** The strongest analysis frames it as a long-lived commitment rather than a tooling choice, and the questions in option B are the ones that determine the risk: a framework touching every file is a different proposition from one confined to a boundary, and the answer to "what if maintenance stops" ranges from an inconvenience to a rewrite. Option D is a genuinely good move and is the second-best answer here, because a trial in one service both tests the benefit and limits the exposure — but it belongs after the analysis rather than instead of it, since a trial that succeeds creates momentum for adoption whether or not the maintenance question was ever answered. Option C applies a rule without reasoning. Option A weighs the upside only.

**Question 10 (harder) — A metric that misleads**

Your team's test suite takes 40 minutes, and a developer proposes parallelising it to 8 minutes. The suite currently fails intermittently about once in fifteen runs. What is the strongest observation?

- A) Parallelising is a clear win.
- B) Parallelising a suite with an existing intermittent failure is likely to make the intermittency worse, since many flaky tests are caused by shared state or ordering dependencies that parallel execution exposes more often — so the intermittency should be diagnosed first, or the speed-up will arrive alongside a suite nobody trusts.
- C) The suite should be split rather than parallelised.
- D) The intermittency should be handled with retries.

**Correct answer: B**

**Explanation:** The sequencing is the point. Parallel execution changes ordering and increases contention on shared resources, which are the two commonest causes of intermittent test failures — so a suite failing once in fifteen sequentially may fail once in four in parallel, and the team will have traded 32 minutes of waiting for a suite whose failures they start ignoring. That last consequence is the serious one: a suite people do not trust stops catching regressions, which is a worse position than a slow suite. Option B says this. Option D is least useful, because retries on a parallelised suite mask exactly the race conditions that may also occur in production. Option A takes the speed-up without the consequence. Option C is a reasonable alternative and does not address the intermittency either.

**Question 11 (harder) — Reading the distribution of a problem**

Across the last year, five production incidents were caused by configuration errors during deployment. All five were on Friday afternoons, all by experienced developers. What is the strongest response?

- A) Introduce a rule against Friday deployments.
- B) The concentration is diagnostic: five configuration errors by experienced people at the same time of week suggests a process that depends on care at the point when people have least of it — so the useful question is what part of deployment is manual and error-prone, and whether it can be automated or validated, since a Friday rule leaves the fragility in place for Thursday.
- C) Require a second person to check deployments.
- D) Remind the team to be careful on Fridays.

**Correct answer: B**

**Explanation:** The Friday pattern is real information and the wrong conclusion to draw from it. Experienced developers making configuration errors clustered at the end of the week points at a deployment process with a manual step that requires attention, and the timing tells you when attention runs out rather than what the defect is. Option B looks for the manual step, and the remedies — validating configuration before deployment, generating it rather than editing it, failing fast on a malformed value — remove the class of error entirely. Option A is the popular response and displaces the risk to Thursday afternoon while costing the team a day of deployment capacity every week. Option C adds a person to a fragile process. Option D is the weakest available response to any recurring error.

**Question 12 (harder) — Technical responsibility across stages**

A component your team built two years ago is now maintained by another team. They report a defect and ask you to fix it, since you wrote it. What is the strongest response?

- A) Fix it; you know the code.
- B) Help them fix it rather than fixing it for them — pairing on the diagnosis, explaining the design decisions that are not obvious from the code — because fixing it yourself is faster once and leaves them unable to maintain something they own, and the second request will follow within a month.
- C) Decline; it is their component now.
- D) Fix it and document it afterwards.

**Correct answer: B**

**Explanation:** The immediate ask is reasonable and granting it directly creates a dependency that neither team wants. Option B is slower once and resolves the underlying problem, which is that a team owns a component they cannot maintain — and the specific value you can add is the part not visible in the code, which is why particular decisions were made and what constraints shaped them. That knowledge is what a handover usually fails to transfer, and pairing on a real defect is the most effective way to transfer it. Option D is close and weaker, because documentation written after the fact by somebody solving it alone captures the fix rather than the reasoning. Option A is helpful and creates the next request. Option C is defensible on ownership and unhelpful, and the relationship costs more than the afternoon.

### Preparation tips

- **Ask which decisions are reversible before spending time on which are optimal.**
- **Read three occurrences of one defect as a structural cause.**
- **Question the framing of a build request.** "We need an engine" often means "we need a state field".
- **Check reversibility of a migration before proposing a revert.**
- **Grandfather existing code when introducing a rule.** A large cleanup kills adoption.
- **Answer the question behind "is it possible".** Cost, opportunity cost and risk.
- **Establish blast radius before treating a defect as a fix.**
- **Read the timing of clustered incidents as evidence about the process, not the people.**

### Common pitfalls to avoid

- **Treating recurring defects as carelessness.**
- **Reverting a release containing an irreversible migration.**
- **Adopting a framework on its merits without weighing the commitment.**
- **Parallelising a suite with unexplained intermittency.**
- **Enabling a rule as a warning nobody fixes.**
- **Answering "is it technically possible" literally.**
- **Banning Friday deployments instead of fixing the fragility.**
- **Fixing another team's component for them.**

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment tests whether you can extract a defensible conclusion from operational data under time pressure. At lead level the data is what you actually use: availability figures, latency distributions, throughput and capacity numbers, cost projections, and delivery estimates you are asked to defend.

The format is typically fifteen to twenty-five minutes, calculator permitted, with tables and charts followed by multiple-choice items. Some are computational and some ask what the data does and does not support, and the second kind is where senior candidates separate.

Three habits matter particularly.

The first is checking magnitude before precision. A lead developer challenging a capacity plan in a meeting needs to know whether a number is roughly right, and an order-of-magnitude error is the one that causes damage.

The second is that averages across dissimilar things are almost always misleading. Average latency across endpoints, average CPU across instances, average velocity across sprints — each hides the distribution that contains the actual information.

The third is that capacity questions are about headroom under peak, not utilisation under average, and the two differ by a factor that surprises people.

### How this assessment maps to your role

- **Availability and reliability arithmetic** maps to **Availability and capacity management**.
- **Distribution reasoning** maps to **Systems design**, where percentile behaviour drives design decisions.
- **Capacity and headroom** maps to your responsibility for capacity planning.
- **Cost and effort estimation** maps to your role's involvement in deciding when software should be written.
- **Defect and quality metrics** map to **Development process optimisation**.
- **Integration volumetrics** map to **Systems integration**.

### Practice questions

*Table 1 — Endpoint latency, last 7 days*

| Endpoint | Requests/day | Median (ms) | 95th (ms) | 99th (ms) |
|---|---|---|---|---|
| /search | 400,000 | 120 | 900 | 2,400 |
| /profile | 150,000 | 45 | 110 | 180 |
| /submit | 60,000 | 200 | 650 | 1,100 |
| /status | 390,000 | 12 | 30 | 55 |

**Question 1 (easy) — Reading a table**

Which endpoint has the largest gap between its median and its 99th percentile?

- A) /search
- B) /submit
- C) /profile
- D) /status

**Correct answer: A**

**Explanation:** /search: 2,400 − 120 = 2,280 ms. /submit: 1,100 − 200 = 900 ms. /profile: 180 − 45 = 135 ms. /status: 55 − 12 = 43 ms. /search has by far the largest gap, and a twenty-fold spread between median and 99th percentile indicates something bimodal — most likely a cache with a high hit rate, where hits return in around 120 ms and misses do real work. That is a design fact you can read off the table.

**Question 2 (easy) — Weighted total**

Approximately how many requests per day do these four endpoints handle in total?

- A) About 600,000
- B) About 1,000,000
- C) About 1,400,000
- D) About 800,000

**Correct answer: B**

**Explanation:** 400,000 + 150,000 + 60,000 + 390,000 = 1,000,000. The arithmetic is easy and the point of the item is that this total is the denominator for anything you compute afterwards — an error rate, a cost per request, a percentage of traffic affected by a change. Getting a running sense of total volume before answering anything else is a habit worth having.

**Question 3 (easy) — Availability minutes**

A service with a 99.95% monthly availability target. Roughly how many minutes of downtime does that allow in a 30-day month?

- A) About 5 minutes
- B) About 22 minutes
- C) About 44 minutes
- D) About 2 minutes

**Correct answer: B**

**Explanation:** A 30-day month is 43,200 minutes. 0.05% of 43,200 = 21.6 minutes, so about 22. Worth committing to memory at this level: 99.9% is about 43 minutes a month, 99.95% about 22, 99.99% about 4.3. These numbers should be instant, because you will be asked in meetings whether a proposed target is achievable, and the answer depends heavily on whether a single deployment gone wrong consumes the entire monthly budget.

**Question 4 (moderate) — Weighted average latency**

Using Table 1, what is the approximate request-weighted median latency across all four endpoints?

- A) About 94 ms
- B) About 71 ms
- C) About 120 ms
- D) About 45 ms

**Correct answer: B**

**Explanation:** Weight each median by request volume: (400,000 × 120) + (150,000 × 45) + (60,000 × 200) + (390,000 × 12) = 48,000,000 + 6,750,000 + 12,000,000 + 4,680,000 = 71,430,000 ms-requests. Divide by 1,000,000 requests = 71.4 ms. This is option B; option A at 94 ms is the simple unweighted mean of the four medians (120 + 45 + 200 + 12) / 4 = 94.25, which is the trap. The weighted figure is lower because /status, the second-highest-volume endpoint, is very fast. Note also that a weighted average of medians is not a true overall median, which is a distinction worth holding onto — it is an approximation useful for comparison, not a statistic you should quote as the service's median.

**Question 5 (moderate) — Capacity headroom**

A service runs on 8 instances averaging 45% CPU. Peak traffic is 2.3 times average. If you lose one instance during peak, what is the approximate CPU on the remaining instances?

- A) About 104%
- B) About 118%
- C) About 90%
- D) About 76%

**Correct answer: B**

**Explanation:** At average load, total CPU work = 8 × 45% = 360 percentage-points. At peak this becomes 360 × 2.3 = 828. Spread across 7 remaining instances: 828 / 7 = 118%. Over 100%, meaning the service cannot absorb a single instance failure at peak — it will queue, latency will climb and it will probably cascade. Option A (104%) comes from spreading peak across all 8 (828/8 = 103.5%), which already exceeds capacity and shows the service is under-provisioned even without a failure. That is the real finding here: 45% average CPU sounds comfortable and is not, because average utilisation tells you nothing about peak headroom.

**Question 6 (moderate) — Error budget**

A service has a 99.9% availability target over 30 days. Twelve days in, it has consumed 31 minutes of downtime. Is it on track?

- A) Yes, it is under the monthly budget.
- B) No — the monthly budget is about 43 minutes, and consuming 31 of them in the first 12 days is a burn rate of roughly 2.6 minutes a day, which projects to about 78 minutes over 30 days, nearly double the budget.
- C) Yes, since 31 is less than 43.
- D) There is not enough information.

**Correct answer: B**

**Explanation:** 0.1% of 43,200 minutes = 43.2 minutes. Consumed 31 in 12 days = 2.58 minutes/day; over 30 days that projects to 77.5 minutes. The service is on course to miss the target by a wide margin, and it currently looks fine to anyone comparing a single number against a threshold. Options A and C make exactly that comparison, which is the commonest error-budget mistake — a budget is consumed over time, so the meaningful measure is burn rate against elapsed proportion of the window. Twelve days is 40% of the month and 31 minutes is 72% of the budget.

*Table 2 — Build and test pipeline, monthly*

| Stage | Runs/month | Mean duration (min) | Failure rate |
|---|---|---|---|
| Compile | 1,200 | 3 | 4% |
| Unit tests | 1,150 | 11 | 9% |
| Integration tests | 1,046 | 24 | 14% |
| Deploy to staging | 900 | 6 | 3% |

**Question 7 (moderate) — Pipeline time**

Approximately how many hours per month does the integration test stage consume?

- A) About 250 hours
- B) About 420 hours
- C) About 150 hours
- D) About 600 hours

**Correct answer: B**

**Explanation:** 1,046 runs × 24 minutes = 25,104 minutes = 418.4 hours, so about 420. That is a substantial figure and the reason it is worth computing: integration tests consume more pipeline time than the other three stages combined (compile 60 hours, unit tests 211 hours, staging deploy 90 hours = 361 hours), which tells you where optimisation effort would pay. This is the kind of arithmetic that turns a vague sense that "the pipeline is slow" into a specific target.

**Question 8 (harder) — Compound pass rate**

Using Table 2, what proportion of pipeline runs starting at compile reach the end of staging deployment successfully?

- A) About 70%
- B) About 74%
- C) About 78%
- D) About 86%

**Correct answer: B**

**Explanation:** Multiply the pass rates: 0.96 × 0.91 × 0.86 × 0.97 = 0.7288, about 73%, closest to option B. The naive approach of adding the failure rates (4 + 9 + 14 + 3 = 30%, giving 70%) gets close here because the rates are small, and diverges as rates grow — worth knowing which method is correct rather than relying on the approximation. The substantive point is that roughly one run in four does not make it through, which is a meaningful drag on the team's throughput even before you ask how much of that 27% is genuine defect detection versus flakiness.

**Question 9 (harder) — Cost of a decision**

Your team is considering caching a downstream API call. The call currently happens 400,000 times a day at £0.0004 each. A cache with a 70% hit rate would cost £180 a month to run. What is the approximate monthly saving?

- A) About £3,180
- B) About £1,180
- C) About £4,800
- D) About £2,180

**Correct answer: A**

**Explanation:** Current cost: 400,000 × £0.0004 = £160/day = £4,800/month (30 days). A 70% hit rate removes 70% of the calls, saving £3,360/month. Subtract the £180 cache cost: net saving £3,180. Option C is the gross monthly spend without any cache. The arithmetic is straightforward and the item is here because build-versus-buy and optimise-versus-leave-alone decisions turn on figures like these, and a lead who can produce them in a meeting is considerably more persuasive than one who says caching would probably help.

**Question 10 (harder) — Interpreting a defect trend**

Defects found in production per month: Jan 14, Feb 12, Mar 15, Apr 9, May 6, Jun 5. The team introduced automated integration tests in March. What is the strongest conclusion?

- A) The tests reduced defects by about 64%.
- B) Production defects fell after March, which is consistent with the tests working, but the series is short, the fall began in April rather than immediately, and nothing here rules out other changes over the same period — the honest statement is that the data is encouraging and does not establish causation.
- C) The tests had no effect.
- D) The trend will continue downward.

**Correct answer: B**

**Explanation:** The fall from 15 to 5 is real and the causal claim is not established by six data points around a single intervention. Option A computes a real percentage (5 vs 14 is a 64% reduction) and attributes it, which is the specific overreach the item tests — and it is the version most likely to appear in a slide deck. Option B states what the data supports and names the reasons for caution: a short series, a one-month lag, and no control for anything else that changed. Option D extrapolates a trend that has no reason to continue indefinitely. What would strengthen the case is defect data broken down by whether the integration tests could plausibly have caught them.

**Question 11 (harder) — Throughput under a constraint**

An integration processes records in batches. Each batch of 500 records takes 90 seconds. A daily file contains 240,000 records and the processing window is 4 hours. Does it fit?

- A) Yes, comfortably.
- B) No — 240,000 records is 480 batches at 90 seconds each, which is 43,200 seconds or 12 hours, three times the available window.
- C) Yes, just.
- D) It depends on the hardware.

**Correct answer: B**

**Explanation:** 240,000 / 500 = 480 batches. 480 × 90 seconds = 43,200 seconds = 12 hours. The window is 4 hours, so the process needs to be three times faster or run three-way parallel, and that is a design constraint to establish before building rather than discover in production. The arithmetic is simple; what makes it a lead-level item is that this calculation should happen at design time, and the commonest failure is that nobody does it until the first full-volume run. Option D is the answer that sounds prudent and defers the calculation that is available right now.

**Question 12 (harder) — Estimation under uncertainty**

You are asked for an estimate on a piece of work. Your team's last six comparable items took 4, 5, 6, 6, 9 and 21 days. What is the most defensible thing to say?

- A) About 6 days, the median.
- B) Give a range with the tail acknowledged: most comparable items took 4 to 9 days, one took 21, so plan for around 6 to 9 days and note there is a real chance of a much longer outcome if this item turns out to resemble the 21-day one — and say what would make it that one.
- C) About 8.5 days, the mean.
- D) 21 days, to be safe.

**Correct answer: B**

**Explanation:** The distribution has a long right tail, which is the normal shape for software estimates, and a single number discards the information that matters most. The mean (8.5) is pulled up by the outlier and describes none of the actual outcomes; the median (6) describes the typical case and hides the tail entirely. Option B gives the range, names the tail explicitly, and adds the most useful part — what would make this item the long one — which converts an estimate into something a stakeholder can act on and a team can monitor. Option D pads to the worst case, which destroys your credibility on the five occasions out of six when it finishes early.

### Preparation tips

- **Memorise the availability minutes.** 99.9% ≈ 43 min/month, 99.95% ≈ 22, 99.99% ≈ 4.3.
- **Weight averages by volume.** The unweighted mean is the standard distractor.
- **Compute peak headroom, not average utilisation.** Multiply by the peak factor, then remove an instance.
- **Track error budgets as burn rate against elapsed time.**
- **Multiply pass rates rather than adding failure rates.**
- **Do volumetric arithmetic at design time.**
- **Give ranges with the tail named.**
- **Check magnitude first.**

### Common pitfalls to avoid

- **Averaging medians across endpoints of very different volumes.**
- **Reading 45% average CPU as comfortable headroom.**
- **Comparing consumed error budget to the total without regard to elapsed time.**
- **Attributing a fall in defects to a single intervention.**
- **Quoting a mean from a long-tailed distribution.**
- **Deferring throughput arithmetic to "it depends on the hardware".**
- **Reporting a saving gross of its running cost.**

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment tests whether you can determine precisely what a piece of written material establishes. At lead level the material is specifications, architecture decision records, security standards, supplier documentation and incident reports — prose written to be binding, where a misread has consequences.

The commonest format presents a passage followed by statements to be marked True, False or Cannot Say. The rule is strict: True means the passage establishes it, False means the passage contradicts it, and Cannot Say means the passage neither establishes nor contradicts it — regardless of what you know professionally. Your expertise is the main hazard here, because you will frequently know the answer from experience while the passage remains silent.

Three specifics matter at your level.

The first is that "may", "should" and "must" are terms of art in specification prose, and treating them loosely is how requirements get misimplemented. Must is mandatory; should is a strong recommendation from which deviation is permitted with justification; may is optional.

The second is scope. Requirements are qualified — by system, by data classification, by environment — and the qualifier limits what the requirement establishes about anything else.

The third is that exceptions define boundaries. An exception for one thing tells you the rule applies to everything else, and does not tell you the exception extends to a neighbouring case.

### How this assessment maps to your role

- **Reading normative language precisely** maps to **Modern development standards**, where you advise on how standards apply.
- **Scope and qualification** map to **Information security**, where controls are scoped by classification.
- **Distinguishing evidence from inference** maps to **Programming and build**, where incident reports must be read for what they establish.
- **Reading supplier and interface documentation** maps to **Systems integration**.
- **Reading service commitments** maps to **Availability and capacity management** and **Service support**.
- **Communicating precisely** maps to your responsibility for technical advice to stakeholders.

### Practice questions

*Passage A — for Questions 1 to 4*

"Every service handling data classified OFFICIAL-SENSITIVE must encrypt data at rest using an approved algorithm, and must log all access to that data for a minimum of twelve months. Services handling data classified OFFICIAL should encrypt data at rest, and must log access where the data includes personal information. Access logs must be stored separately from the data they describe. Where a service is hosted in a supplier-managed environment, the supplier's encryption implementation may be accepted in place of the service's own, provided the supplier holds current certification against the standard named in Annex C. This exception does not extend to logging obligations, which remain the responsibility of the service team in all cases."

**Question 1 (easy)**

Statement: A service handling OFFICIAL-SENSITIVE data must encrypt data at rest.

- A) True
- B) False
- C) Cannot Say

**Correct answer: A**

**Explanation:** Stated directly in the first sentence, using "must". This is the baseline item and everything afterwards complicates it.

**Question 2 (easy)**

Statement: A service handling OFFICIAL data that contains no personal information is not required to log access.

- A) True
- B) False
- C) Cannot Say

**Correct answer: A**

**Explanation:** For OFFICIAL data, the logging obligation is qualified: "must log access where the data includes personal information". Without personal information the qualifier is not met, so the obligation does not apply. The passage establishes this by the structure of the qualification rather than by a direct statement, which is what makes it slightly more than trivial. Note that the passage says nothing about whether logging would be a good idea anyway, and the question is about requirement.

**Question 3 (moderate)**

Statement: A service handling OFFICIAL data is not required to encrypt data at rest.

- A) True
- B) False
- C) Cannot Say

**Correct answer: A**

**Explanation:** The passage uses "should" for OFFICIAL data encryption and "must" for OFFICIAL-SENSITIVE. In normative prose those are different obligations: "should" is a strong recommendation permitting justified deviation, and the deliberate contrast with "must" in the immediately preceding sentence confirms the distinction is intentional. So encryption is not required for OFFICIAL, though it is expected. The pull towards False comes from professional instinct — you would encrypt it — and the passage is asking what it says.

**Question 4 (moderate)**

Statement: A service in a supplier-managed environment whose supplier holds current Annex C certification may rely on the supplier for its access logging.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The passage contradicts this explicitly: "This exception does not extend to logging obligations, which remain the responsibility of the service team in all cases." The final sentence exists precisely to close this inference, and the phrase "in all cases" removes any remaining room. This is the item that rewards reading to the end of the passage, since everything before the last sentence points the other way.

*Passage B — for Questions 5 to 8*

"The incident began at 09:12 when the payment service started returning HTTP 503 responses. Monitoring alerted at 09:14. The on-call engineer identified elevated connection counts to the primary database and, at 09:31, restarted the connection pool, after which error rates returned to normal within two minutes. A release had been deployed at 08:55 which changed the pool's maximum size from 40 to 120. The change had been made to address timeouts reported during the previous week's peak. No load testing was carried out against the new configuration. The database's configured maximum connection limit is 150, shared across four services."

**Question 5 (easy)**

Statement: The incident was detected by monitoring before it was reported by a user.

- A) True
- B) False
- C) Cannot Say

**Correct answer: C**

**Explanation:** The passage says monitoring alerted at 09:14 and says nothing about user reports at all — there may have been one at 09:13, or none. The statement compares two things when the passage documents only one. This is the commonest Cannot Say shape: a plausible-sounding comparison where one side is simply absent from the text.

**Question 6 (moderate)**

Statement: The release deployed at 08:55 caused the incident.

- A) True
- B) False
- C) Cannot Say

**Correct answer: C**

**Explanation:** The evidence is strong — a pool size change from 40 to 120 seventeen minutes before failure, against a database limit of 150 shared by four services, with elevated connection counts observed — and the passage does not state causation. Everything present is consistent with the release exhausting the shared connection limit, and that is an inference you would be right to draw professionally and right to mark Cannot Say here. Note also that restarting the pool resolved the symptom without reverting the configuration, which is a fact that slightly complicates the obvious story and is worth noticing.

**Question 7 (moderate)**

Statement: The database's connection limit could be exceeded if all four services opened their maximum configured connections simultaneously.

- A) True
- B) False
- C) Cannot Say

**Correct answer: C**

**Explanation:** Tempting, and the passage gives you only one of the four numbers you need. It states the payment service's new maximum is 120 and the database limit is 150, but says nothing about the other three services' pool configurations. If they are tiny the sum might still exceed 150, but you cannot establish it from the passage — and the discipline is that a near-certainty is not what the format asks for.

**Question 8 (harder)**

Statement: The engineer resolved the incident exactly 19 minutes after monitoring alerted.

- A) True
- B) False
- C) Cannot Say

**Correct answer: C**

**Explanation:** The restart was at 09:31, 17 minutes after the 09:14 alert, and error rates returned to normal "within two minutes" — so resolution was somewhere between about 09:31 and 09:33, which is between 17 and 19 minutes after the alert. Exactly 19 is the upper end of that range: possible, not established, and not contradicted either. The word doing the work is "within", which sets a bound rather than a duration, and if you computed 09:14 to 09:33 and answered True, that is the habit worth catching — the arithmetic is right and it is arithmetic on a maximum.

*Passage C — for Questions 9 to 12*

"The framework's long-term support release is maintained for three years from general availability, during which security patches are issued for critical and high-severity vulnerabilities. Medium and low-severity issues are addressed in the current release only. After the support period ends, no patches of any severity are issued. Organisations requiring extended support may purchase it, subject to a minimum commitment of two years. Extended support covers critical vulnerabilities only. The vendor advises that extended support is intended to provide time for migration rather than as a long-term operating model, and reserves the right to decline renewal beyond a single extended term."

**Question 9 (moderate)**

Statement: A medium-severity vulnerability in a long-term support release will not be patched in that release.

- A) True
- B) False
- C) Cannot Say

**Correct answer: A**

**Explanation:** The passage states that during the support period patches cover "critical and high-severity" vulnerabilities, and that "medium and low-severity issues are addressed in the current release only". The long-term support release is by definition not the current release, so a medium-severity issue is not patched in it. The passage establishes this, and it is a fact with real operational weight: a team running an LTS release for stability is accepting an unpatched medium-severity backlog.

**Question 10 (moderate)**

Statement: An organisation can purchase extended support for one year.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The passage states a "minimum commitment of two years", which contradicts a one-year purchase. Straightforward, and it is the kind of contractual detail that changes a migration plan — a team hoping to buy nine months of breathing space is actually committing to two years of cost.

**Question 11 (harder)**

Statement: An organisation could remain on a long-term support release for seven years with critical vulnerabilities patched throughout.

- A) True
- B) False
- C) Cannot Say

**Correct answer: C**

**Explanation:** Three years of standard support plus a two-year extended term is five years, which leaves the seventh year unaccounted for. Whether a second extended term is possible is genuinely unresolved by the passage: the vendor "reserves the right to decline renewal beyond a single extended term", which establishes that renewal may be declined and does not establish that it always will be. So seven years is neither established nor contradicted. Answering False by treating the reserved right as a prohibition is the natural error, and the distinction between "may decline" and "will not offer" is exactly the kind that matters when you are relying on the answer for a migration timeline.

**Question 12 (harder)**

Statement: The vendor recommends against using extended support as a long-term operating model.

- A) True
- B) False
- C) Cannot Say

**Correct answer: A**

**Explanation:** The passage says extended support "is intended to provide time for migration rather than as a long-term operating model", attributed to the vendor's advice. That is a recommendation against long-term use, expressed through a statement of intent rather than through the word "recommend" — and reading it as merely descriptive would miss what the sentence is doing. The surrounding context supports the reading: the vendor also limits coverage to critical vulnerabilities and reserves the right to decline renewal, both of which are consistent with actively discouraging long-term reliance.

### Preparation tips

- **Treat must, should and may as distinct obligations.**
- **Read to the end before answering.** Final sentences often close the obvious inference.
- **Check whether both sides of a comparison appear in the passage.**
- **Mark strong causal evidence as Cannot Say when causation is not stated.**
- **Watch bounding language.** "Within two minutes" is a maximum, not a duration.
- **Distinguish "may decline" from "will not offer".**
- **Count the numbers a claim needs before treating it as computable.**
- **Notice when a qualifier limits an obligation.**

### Common pitfalls to avoid

- **Reading "should" as mandatory.**
- **Extending an exception past its stated boundary.**
- **Marking a well-evidenced cause as True.**
- **Treating a reserved right as a prohibition.**
- **Computing with numbers the passage does not supply.**
- **Answering from professional knowledge rather than the text.**
- **Taking a hedged recovery time as a precise figure.**

## Workplace job-specific situational judgement assessment

### About this assessment

A workplace job-specific situational judgement assessment presents realistic scenarios from your role and asks you to rank or select responses. At lead level the scenarios involve technical authority, disagreement with people senior to you, decisions with consequences you will not personally absorb, and the recurring problem of holding a standard when holding it is expensive.

The commonest formats ask you to pick the most effective and least effective response, or to rate each on a scale. Scoring is against a key derived from experienced practitioners in comparable roles, so the target is professional consensus rather than your personal style.

Three patterns run through the strong answers at this level.

The first is that you own the consequences of technical decisions even when someone else made the call, which means the useful move is usually to make the consequence visible and decidable rather than to accept it silently or to refuse.

The second is that your standards apply to you most visibly. A lead who exempts themselves from the standard they set has repealed it, whatever the documentation says.

The third is that escalation is a tool with a cost. Used well it resolves a decision at the level that owns it; used as a first response it removes your ability to be trusted with disagreements.

### How this assessment maps to your role

- **Holding standards under pressure** maps to **Modern development standards** and your role in setting team standards.
- **Technical advice to stakeholders** maps to that named responsibility.
- **Team leadership and development** maps to guiding the ways in which the team works.
- **Incident handling** maps to **Service support** and **Availability and capacity management**.
- **Security judgement** maps to **Information security**.
- **Integration and dependency management** map to **Systems integration**.

### Practice questions

**Question 1 (easy) — A shortcut under deadline**

Two days before a release, meeting the date requires skipping the accessibility testing your standard requires. What is the most effective response?

- A) Skip the testing and add it after release.
- B) Tell the service owner what skipping it means — that accessibility defects would reach users and the service would be non-compliant — and let them decide with the trade-off visible, while offering what partial testing is possible in the time.
- C) Refuse to release without the testing.
- D) Do the testing and miss the date.

**Correct answer: B. Least effective: A**

**Explanation:** The date belongs to the service owner and the consequence belongs to users, which makes your job to ensure the decision is made by the right person with the right information rather than made silently by you. Option B does that and adds the constructive part — partial testing is worth more than none and may resolve the question. Option A is least effective because it makes the decision invisibly, and "add it after release" reliably becomes never. Option C removes the owner from a decision that is theirs. Option D makes the opposite unilateral call.

**Question 2 (easy) — A junior developer's approach**

A junior developer on your team proposes an approach that will work but is more complicated than necessary. What is the most effective response?

- A) Tell them to use the simpler approach.
- B) Ask what led them to it before offering the alternative — they may have identified a constraint you have not, and if they have not, the reasoning behind the simpler approach is the part worth transferring rather than the instruction.
- C) Let them build it; they will learn.
- D) Rewrite it yourself.

**Correct answer: B. Least effective: D**

**Explanation:** Option B costs a conversation and buys two things: the possibility that they are right, and a developer who can make the judgement themselves next time. Option A transfers the answer without the reasoning, which works once. Option D is least effective — it removes the work, teaches nothing, and tells the team that their code becomes yours when you disagree with it. Option C treats every lesson as worth its full cost, which for an approach that merely works is an expensive way to learn something a five-minute conversation would convey.

**Question 3 (moderate) — Disagreeing with an architect**

An enterprise architect specifies an integration pattern you believe will not perform at the required volume. What is the most effective response?

- A) Implement it as specified; the architect has the authority.
- B) Raise the concern with the specific numbers — the expected volume, the pattern's likely throughput, and where you expect it to break — and propose a quick test to settle it, since a disagreement between two informed opinions is resolvable with evidence and a disagreement of assertions is not.
- C) Implement a different pattern that works.
- D) Escalate to your line manager.

**Correct answer: B. Least effective: C**

**Explanation:** You may be wrong, and the way to find out is a test rather than a debate. Option B converts a clash of authority into a question with an answer, which is both more likely to reach the right outcome and considerably easier for the architect to accept than being contradicted. Option C is least effective: deviating silently from a specification breaks the architecture, is discovered later at higher cost, and destroys the trust that lets you be listened to next time. Option A implements something you expect to fail. Option D escalates a technical disagreement to someone who cannot evaluate it, before trying the direct route.

**Question 4 (moderate) — Security finding in a senior colleague's code**

Reviewing a pull request from a developer considerably more senior than you, you find a SQL injection vulnerability. What is the most effective response?

- A) Approve it and raise the issue separately.
- B) Block the merge and explain the specific vulnerability with the input that would exploit it, treating it as a normal review finding — because the standard does not vary by author, and a concrete exploit is a technical observation rather than a challenge to anyone's competence.
- C) Fix it yourself and merge.
- D) Ask a security specialist to review it.

**Correct answer: B. Least effective: A**

**Explanation:** This is a straightforward review finding that feels difficult only because of the seniority, and treating it as normal is both correct and the least awkward path. Naming the specific input that exploits it keeps the conversation technical. Option A is least effective — approving code with a known injection vulnerability puts it in production, and the separate conversation happens after the risk is live. Option C removes the author's chance to see the defect and takes ownership of their change. Option D is a reasonable addition and an evasion as the primary response, since you have already identified the problem and outsourcing the message does not make it land better.

**Question 5 (moderate) — Team velocity question from a delivery manager**

A delivery manager asks why the team's velocity dropped for two sprints. The cause is that the team spent the time on a necessary refactor of a fragile component. What is the most effective response?

- A) Explain that velocity is a poor measure.
- B) Say directly what the time went on and why it was necessary — the component's failure rate, what it was blocking, what it now enables — so the drop reads as a deliberate investment with a return rather than as unexplained slowness.
- C) Say the team was working on technical debt.
- D) Apologise and commit to recovering the velocity.

**Correct answer: B. Least effective: D**

**Explanation:** The delivery manager needs to explain the two sprints to someone else, and option B gives them something explicable and true. The specifics matter: "technical debt" (option C) is a phrase that has been used to justify so much that it now conveys almost nothing to a non-technical listener, whereas "this component caused four of our last six incidents and blocked the feature you asked for" is immediately legible. Option D is least effective because it accepts the framing that the work was a failure and commits to a number rather than to outcomes. Option A is true and reads as deflection when offered instead of an answer.

**Question 6 (moderate) — A standard you set is being ignored**

You introduced a standard requiring architecture decision records for significant technical choices. Three months on, nobody writes them, including you. What is the most effective response?

- A) Remind the team of the standard.
- B) Start with why it is not being followed, including by you — if the format is too heavy, or the trigger for "significant" is unclear, or the records are never read, then the standard is unfollowable and the fix is to change it; and your own non-compliance is the strongest available evidence about which.
- C) Make the records a required part of the review process.
- D) Drop the standard.

**Correct answer: B. Least effective: A**

**Explanation:** A standard that nobody follows, including its author, is telling you something about the standard rather than about the team's discipline. Option B investigates before enforcing and names the specific candidates: too heavy a format, an unclear trigger, or no readership — each with a different remedy. Your own non-compliance is the diagnostic detail worth being honest about, because you had the most reason to comply. Option A is least effective, since a reminder about a standard nobody can follow produces a fortnight of compliance and then the same position. Option C might work and might just add friction to an unfollowable process. Option D discards a genuine need without testing whether a lighter version would work.

**Question 7 (harder) — Pressure to under-report**

Following an incident, a senior stakeholder asks you to describe the root cause in the report as "an unforeseen combination of circumstances". You know it was a configuration error your team made. What is the most effective response?

- A) Write it as requested; the stakeholder is senior.
- B) Write the report accurately and say why: an incident report exists so the organisation can prevent recurrence, an inaccurate cause prevents that, and a team that reports its own errors accurately is the reason the reporting is worth anything — while offering to discuss how the finding is presented, which is a legitimate concern and a separate one from what it says.
- C) Refuse and escalate.
- D) Write it vaguely to satisfy both.

**Correct answer: B. Least effective: D**

**Explanation:** The stakeholder's concern is probably about how the team looks, which is real and addressable through presentation and framing — but not through changing what the report says happened. Option B holds the line on accuracy while engaging with the legitimate part of the concern, which is both the right answer and the one most likely to be accepted. Option D is least effective because deliberate vagueness is the version that is hardest to challenge and does the same damage: the organisation cannot act on a cause it cannot identify, and vagueness is what makes the same incident recur. Option A produces a false record. Option C may become necessary and skips the conversation that usually resolves it.

**Question 8 (harder) — An underperforming team member**

A developer on your team consistently produces work that needs substantial rework. The team is beginning to route around them. What is the most effective response?

- A) Raise it with their line manager.
- B) Talk to them directly first, with specific examples, and establish what is going on — the cause could be a knowledge gap, an unclear brief, something outside work, or a genuine mismatch, and the response differs entirely by cause — while recognising that the team routing around them is a problem needing action either way.
- C) Give them simpler work.
- D) Pair with them on everything.

**Correct answer: B. Least effective: C**

**Explanation:** You cannot choose a response without knowing the cause, and the person most likely to know it has not been asked. Option B starts there with specifics rather than impressions, and notes the second problem — the team's workaround — which will harden into permanent exclusion if left. Option C is least effective: it looks kind, removes any path to improvement, is immediately obvious to the person, and confirms to the team that this developer is not to be relied on. Option D is unsustainable and may be part of a plan. Option A is appropriate if the direct conversation does not resolve it, and going first to the line manager makes a solvable problem formal.

**Question 9 (harder) — A dependency that will not be ready**

Another team's API, which your delivery depends on, is now three weeks late with no revised date. Your own deadline has not moved. What is the most effective response?

- A) Wait; there is nothing you can do.
- B) Establish what is actually blocked versus what can proceed against a stub or contract, get the dependency's real position rather than its stated one, and make the delivery risk explicit to whoever owns your deadline — with the options, which are usually to move the date, cut scope, or build a temporary alternative.
- C) Build your own version of the API.
- D) Escalate to senior management.

**Correct answer: B. Least effective: A**

**Explanation:** Option B does the three things available: reduce the blockage by working against an agreed contract, replace an unreliable date with a real one, and hand the deadline owner a decision with options rather than a problem. The options matter — a deadline holder given only bad news will pick something, and it is better if you framed the choices. Option A is least effective because a known risk that nobody has been told about becomes a surprise failure, and the surprise is the part that is unforgivable. Option C commits weeks to duplicate work before establishing whether it is needed. Option D may follow and is premature before you have the dependency's real position.

**Question 10 (harder) — Your own technical decision has aged badly**

An architectural decision you made eighteen months ago is now causing the team significant friction. A newer team member proposes replacing it. What is the most effective response?

- A) Defend the decision; it was right at the time.
- B) Engage with the proposal on its merits and say plainly that the original decision has not aged well — the constraints it was made under, what has changed, and what replacing it would cost now — because your visible willingness to have your own decisions revisited is what makes it safe for anyone else to raise one.
- C) Agree to the replacement.
- D) Ask them to write a proposal.

**Correct answer: B. Least effective: A**

**Explanation:** The decision may well have been right at the time and is causing friction now, and both can be true without either being a defence. Option B gets to the substance and models something the team needs to see: that decisions are revisable and raising one is not an attack. That signal is worth more than the specific outcome, because a team that cannot challenge the lead's architecture accumulates problems silently. Option A is least effective — it is the natural reaction, it usually wins because you have the authority, and it teaches the team not to bother. Option C over-corrects and skips the cost analysis. Option D is a reasonable process step and can read as a delaying tactic if it substitutes for a view.

**Question 11 (harder) — Adopting a technology you dislike**

Your organisation mandates a technology platform you consider a poor fit for your service. The decision is made and not open for reconsideration. What is the most effective response?

- A) Comply and say nothing further.
- B) Implement it properly while documenting the specific costs you expect — the concrete ones, in performance, effort or operability — so that the organisation has evidence when the decision is next reviewed, and so your team is not left with an implementation deliberately made worse by your reservations.
- C) Comply minimally and build workarounds.
- D) Continue arguing the case.

**Correct answer: B. Least effective: C**

**Explanation:** The decision is settled, which changes what a good response looks like: you implement it well, and you record the evidence. Option B does both, and the second half matters because platform decisions are reviewed, and the review will be evidence-free unless someone gathered any. Option C is least effective — a deliberately half-hearted implementation plus workarounds gives you the worst of both, a platform you dislike implemented badly, and your team maintains the result. Option A is compliant and throws away the evidence. Option D spends credibility relitigating something closed, which costs you influence on the decisions still open.

**Question 12 (harder) — Deciding not to build**

Your team is enthusiastic about building an internal tool that would genuinely help them. You believe an existing product would do the job. What is the most effective response?

- A) Direct them to use the existing product.
- B) Put the comparison to them honestly — what the existing product does and does not do, what building would cost to build and then to maintain indefinitely — and make the decision with them, because the maintenance cost is the part that enthusiasm reliably discounts and the part they will bear.
- C) Let them build it; team motivation matters.
- D) Approve a timeboxed prototype.

**Correct answer: B. Least effective: C**

**Explanation:** Deciding when software should be written is explicitly your responsibility, and the strongest version of it is a decision the team reaches with you rather than one imposed. Option B supplies the missing information, which is almost always the ongoing maintenance cost — teams estimate the build and rarely the years afterwards, and it is their years. Option C is least effective: motivation is real and is not a reason to commit the team to maintaining something indefinitely, and a lead who cannot say this is a lead whose service accumulates bespoke tooling. Option A reaches a likely-correct answer in the way that teaches nothing and invites resentment. Option D is a reasonable move if the comparison is genuinely close, and here it is not.

### Preparation tips

- **Make trade-offs visible to whoever owns the decision.**
- **Convert authority disagreements into testable questions.**
- **Apply standards identically regardless of the author's seniority.**
- **Read a standard nobody follows as a defect in the standard.**
- **Hold accuracy in incident reports; negotiate presentation, not content.**
- **Ask about the cause before choosing a response to underperformance.**
- **Name the maintenance cost when the team wants to build something.**
- **Let your own decisions be revisited visibly.**

### Common pitfalls to avoid

- **Making a scope or quality trade-off silently.**
- **Deviating from a specification rather than challenging it.**
- **Approving code with a known vulnerability to avoid awkwardness.**
- **Answering a velocity question with "technical debt".**
- **Writing a deliberately vague incident cause.**
- **Giving an underperforming colleague simpler work.**
- **Implementing a mandated platform half-heartedly.**
- **Defending your own past decision because it is yours.**

## Conclusion

You have worked through four assessments pitched at lead developer level, and the shape of what they test is worth naming.

The cognitive section kept returning to the same structural question: is this decision reversible, and is this defect an instance or a pattern? Three developers making the same mistake is a structural cause. Five configuration errors on Friday afternoons is a fragile process, not a careless team. A framework choice is a multi-year commitment rather than a tooling preference. And the question your role names explicitly — should this software be written at all — usually turns out to be a question about whether the framing is right, because a four-step approval process rarely needs an engine.

The numeric section was about the arithmetic you are expected to do in the room: availability minutes, peak headroom against average utilisation, error budgets as burn rate, volumetrics at design time rather than at first full-volume run. The recurring trap was the average that hides its distribution, and the recurring skill was giving a range with the tail named rather than a single number that is wrong in a predictable direction.

The verbal section was an exercise in reading normative prose exactly: must, should and may as distinct obligations; exceptions that stop where they say they stop; "within two minutes" as a bound; "may decline" as something short of a prohibition. Your professional knowledge is the main obstacle in that format, because you keep knowing things the passage has not said.

The situational judgement section circled the particular difficulty of your level, which is technical authority you hold without formal power. The strong answers made consequences visible and decidable, converted disagreements into evidence, applied standards without regard to who wrote the code, and treated your own past decisions as revisable in public.

If you take one thing from this, take the pattern that the strongest responses were rarely the decisive ones. They were the ones that got the right decision made by the right person with the information they needed — which is most of what leading development actually consists of.

Good luck. You are in a role where careful reasoning compounds, and this is worth the time you have given it.
